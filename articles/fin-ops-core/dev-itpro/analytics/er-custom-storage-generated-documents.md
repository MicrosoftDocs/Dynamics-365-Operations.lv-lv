---
title: Pielāgotas glabāšanas vietas norādīšana ģenerētajiem dokumentiem
description: Šajā rakstā ir izskaidrots, kā paplašināt glabāšanas vietu sarakstu dokumentiem, ko ģenerē elektroniskie pārskatu (ER) formāti.
author: kfend
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: 83ee74cf590fe559ae18161d68b38dff54ab7fbc
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268761"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a>Pielāgotas glabāšanas vietas norādīšana ģenerētajiem dokumentiem

[!include[banner](../includes/banner.md)]

Elektronisko pārskatu veidošanas (ER) struktūras lietojumprogrammas interfeiss (API) ļauj paplašināt ER formātu ģenerēto dokumentu glabāšanas vietu sarakstu. Šajā rakstā ir iekļauts galveno uzdevumu apskats, kas ir jāveic, lai pievienotu pielāgotu glabāšanas vietu.

## <a name="prerequisites"></a>Priekšnosacījumi

Jums jāizvieto topoloģija, kas atbalsta pastāvīgu būvēšanu. (Papildinformāciju skatiet tēmā [Tādu topoloģiju izvietošana, kuras atbalsta pastāvīgu būvēšanu un testu automatizēšanu](/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) Jums jābūt piekļuvei šai topoloģijai kādā no tālāk minētajām lomām:

- Elektroniskā pārskata izstrādātājs
- Elektronisko pārskatu veidošanas funkcionālais konsultants
- Sistēmas administrators

Jums jābūt arī piekļuvei šīs topoloģijas izstrādes videi.

## <a name="create-or-import-an-er-format-configuration"></a>ER formāta konfigurācijas izveide vai importēšana

Pašreizējā topoloģijā [izveidojiet jaunu ER formātu](tasks/er-format-configuration-2016-11.md), lai ģenerētu dokumentus, kuriem plānojat pievienot pielāgotu glabāšanas vietu. Vai arī [importējiet šajā topoloģijā jau izveidotu ER formātu](general-electronic-reporting-manage-configuration-lifecycle.md).

![Formāta veidotāja lapa.](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> ER formātā, ko izveidojat vai importējat, jābūt vismaz vienam no šādiem formāta elementiem:
>
> - Fails
> - Mape
> - Apvienotājs
> - Pielikums

## <a name="create-a-new-document-type"></a>Jauna dokumenta tipa izveide

Lai norādītu, kā tiek maršrutēti EP formāta ģenerētie dokumenti, jums ir jākonfigurē [Elektronisko paziņojumu (EP) galamērķi](electronic-reporting-destinations.md). Katram ER galamērķim, kas ir konfigurēts tā, lai ģenerētos dokumentus saglabātu kā failus, jums ir jānorāda dokumentu pārvaldības struktūras dokumenta veids. Lai maršrutētu dokumentus, ko ģenerē dažādi ER formāti, var lietot dažādus dokumentu veidus.

1. Pievienojiet jaunu [dokumenta veidu](../../fin-ops/organization-administration/configure-document-management.md) ER formātam, ko iepriekš izveidojāt vai importējāt. Nākamajā ilustrācijā dokumenta veids ir **FileX**.
2. Lai atšķirtu šo dokumenta veidu no citiem dokumentu veidiem, iekļaujiet konkrētu atslēgvārdu tā nosaukumā. Piemēram, nākamajā ilustrācijā nosaukums ir **(LOCAL) folder** ((LOKĀLA) mape).
3. Laukā **Klase** norādiet **Pievienot failu**.
4. Laukā **Grupa** norādiet **Fails**.

![Lapa Dokumentu tipi.](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> Dokumentu veidi ir atkarīgi no uzņēmuma. Lai izmantotu ER formātu ar konfigurēto galamērķi vairākos uzņēmumos, jums ir jākonfigurē atsevišķs dokumenta veids katram uzņēmumam.

## <a name="review-source-code"></a>Pirmkoda pārskatīšana

Pārskatiet metodes **insertFile()** kodu klasei **ERDocuManagement**. Ievērojiet, ka tiek parādīts notikums **AttachingFile()**, kamēr ierakstam tiek pievienots ģenerētais fails.


```xpp
/// <summary>
/// Inserts file as attachment in Document Management.
/// </summary>
/// <param name = "_owner">A record as the attachment owner.</param>
/// <param name = "_stream">The file stream.</param>
/// <param name = "_filePath">The file path with name.</param>
/// <param name = "_attachmentName">The name of file attachment.</param>
/// <returns>The reference to inserted file.</returns>
[Hookable(false)]
public DocuRef insertFile(
    Common _owner, 
    System.IO.Stream _stream, 
    str _filePath, 
    str _attachmentName, 
    DocuTypeId _docuTypeId)
{
    DocuRef docuRef;
    if (_stream)
    {
        DocuType::createDefaults();
        if (!this.isDocuTypeValid(_docuTypeId))
        {
            throw error(strFmt("@ElectronicReporting:DocuTypeIsNotValid", _docuTypeId));
        }
        var args = ERDocuManagementAttachingFileEventArgs::construct(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        ERDocuManagementEvents::onAttachingFile(args);
        if (args.isHandled())
        {
            docuRef = args.getDocuRef();
        }
        else
        {
            docuRef = this.attachFile(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        }
    }
    return docuRef;
}
```

Notikums **AttachingFile()** tiek parādīts, kad tiek apstrādāti tālāk norādītie ER galamērķi.

- **Arhīvs** — ja tiek izmantots šis galamērķis, tabulā ERFormatMappingRunJobTable tiek izveidots jauns ieraksts par izpildīto ER formātu. Lauks **Arhivēts** šajā ierakstā ir iestatīts uz **Aplams**. Ja ER formāts ir veiksmīgi izpildīts, ģenerētais dokuments tiek pievienots šim ierakstam, un tiek parādīts notikums **AttachingFile()**. Dokumenta veids, kas atlasīts šajā ER galamērķī, nosaka pievienotā faila glabāšanas vietu (Microsoft Azure krātuve vai Microsoft SharePoint mape).
- **Darbu arhīvs** — ja tiek izmantots šis galamērķis, tabulā ERFormatMappingRunJobTable tiek izveidots jauns ieraksts par izpildīto ER formātu. Lauks **Arhivēts** šajā ierakstā ir iestatīts uz **Pareizs**. Ja ER formāts ir veiksmīgi izpildīts, ģenerētais dokuments tiek pievienots šim ierakstam, un tiek parādīts notikums **AttachingFile()**. Dokumenta veids, kas ir konfigurēts ER parametros, nosaka pievienotā faila glabāšanas vietu (Azure krātuve vai SharePoint mape).

![Elektronisko pārskatu veidošanas parametru lapa.](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a>ER galamērķa konfigurēšana

1. Konfigurējiet arhivēto galamērķi vienam no iepriekš minētajiem izveidotā vai importētā ER formāta elementiem (fails, mape, apvienotājs vai pielikums). Norādes skatiet tēmā [ER galamērķu konfigurēšana](/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).
2. Izmantojiet dokumenta veidu, kuru iepriekš pievienojāt konfigurētajam galamērķim. (Piemēram, šajā dokumentā dokumenta tips ir **Faila nosaukums**.)

![Dialoglodziņš Galamērķu iestatījumi.](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a>Pirmkoda modificēšana

1. Pievienojiet jaunu klasi savam Microsoft Visual Studio projektam un ievadiet kodu, lai abonētu notikumu **AttachingFile()**, kas tika minēts iepriekš. (Papildinformāciju par izmantoto paplašināmības modeli skatiet tēmā [Atbildēšana, izmantojot EventHandlerResult](/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) Piemēram, jaunai klasei ievadiet kodu, kas veic tālāk norādītās darbības.

    1. Saglabājiet ģenerētos failus vietējās failu sistēmas mapē serverī, kurā darbojas pakalpojums Application Object Server (AOS).
    2. Saglabājiet šos ģenerētos failus tikai tad, ja tiek izmantots jaunais dokumenta veids (piemēram, veids **FileX**, kura nosaukumā ir atslēgvārds “(LOCAL)”), kamēr fails tiek pievienots ierakstam ER izpildes darbu žurnālā.

    ```xpp
    class ERDocuSubscriptionSample
    {
        void new()
        {
        }
        [SubscribesTo(classStr(ERDocuManagementEvents), 
        staticDelegateStr(ERDocuManagementEvents, 
        attachingFile))]
        public static void ERDocuManagementEvents_attachingFile(ERDocuManagementAttachingFileEventArgs _args)
        {
            if (!_args.isHandled())
            {
                DocuType docuType = DocuType::find(_args.getDocuTypeId());
                if (strContains(docuType.Name, '(LOCAL)'))
                {
                    _args.markAsHandled();
                    var stream = _args.getStream();
                    if (stream.CanSeek)
                    {
                        stream.Seek(0, System.IO.SeekOrigin::Begin);
                    }
                    using (var localStream = System.IO.File::OpenWrite(@'c:\0\' + _args.getAttachmentName()))
                    {
                        stream.CopyTo(localStream);
                    }
                }
            }
        }
    }
    ```

2. Atjaunojiet savu projektu

## <a name="run-the-er-format-that-you-created-or-imported"></a>Izveidotā vai importētā ER formāta palaišana

1. Izpildiet izveidoto vai importēto ER formātu.
2. Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Elektronisko pārskatu veidošanas darbi**. Atrodiet ierakstu, kas bija izveidots šim izpildes darbam un kuram ir pievienots ģenerētais fails.
3. Izpētiet vietējo mapi **c:\\0**, lai atrastu pašu ģenerēto failu.

## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko pārskatu (ER) galamērķi](electronic-reporting-destinations.md)
- [Lietojumprogrammas Paplašināmība sākumlapa](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
