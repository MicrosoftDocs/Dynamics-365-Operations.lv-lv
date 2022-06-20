---
title: (ER) konfigurāciju noformēšana, lai ģenerētu atskaites Word formātā
description: Šajā rakstā skaidrots, kā lietotāji var konfigurēt jaunu elektronisko pārskatu (ER) formātu, lai ģenerētu pārskatus kā Microsoft Word dokumentus.
author: NickSelin
ms.date: 12/17/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: caf87659ca4ceb7b25aa43e09893d2a0ef014884
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893017"
---
# <a name="design-a-new-er-configuration-to-generate-reports-in-word-format"></a>(ER) konfigurāciju noformēšana, lai ģenerētu atskaites Word formātā

[!include [banner](../includes/banner.md)]

Lai pārskatus izveidotu kā Microsoft Word dokumentus, jāizveido pārskatu veidne, izmantojot, piemēram, Word datora programmu. Šajā attēlā ir parādīta kontroles pārskata parauga veidne, kuru var ģenerēt, lai parādītu informāciju par apstrādātajiem kreditoru maksājumiem.

![Kontroles pārskata parauga veidne Word darbvirsmas programmā.](./media/er-design-configuration-word-image1.png)

Lai Word dokumentu izmantotu kā veidni pārskatiem Word formātā, jūs varat konfigurēt jaunu [elektronisko pārskatu (ER)](general-electronic-reporting.md) [risinājumu](er-quick-start1-new-solution.md). Šim risinājumam jāietver ER konfigurācija [,](general-electronic-reporting.md#Configuration) kas satur ER formāta komponentu.

> [!NOTE]
> Veidojot jaunu ER formāta konfigurāciju, lai veidotu pārskatus Word formātā, jāatlasa **Word** kā formāta tips nolaižamajā dialoglodziņā **Izveidot konfigurāciju** vai arī jāatstāj lauks **Formāta tips** tukšs.

![Pielāgota formāta pievienošana konfigurācija lapā Konfigurācijas.](./media/er-design-configuration-word-image2.gif)

Risinājuma ER formāta komponentam jāietver **Excel\\Faila** formāta elements, un formāta elementam jābūt saistītam ar Word dokumentu, kas izpildlaikā tiks izmantots kā veidne ģenerētajiem pārskatiem. Lai konfigurētu ER formāta komponentu, jāatver izveidotās ER konfigurācijas [melnraksta versija](general-electronic-reporting.md#component-versioning) ER formāta veidotājā. Pēc tam pievienojiet **Excel\\Faila** elementu, pievienojiet savu Word veidni rediģējamā ER formātam un saistiet šo veidni ar pievienoto **Excel\\Faila** elementu.

> [!NOTE]
> Manuāli pievienojot veidni, jāizmanto [dokumenta veids](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types), kas ir [konfigurēts](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) ER parametros to uzglabāšanai.

![Veidnes pievienošana formātu veidotāja lapā.](./media/er-design-configuration-word-image3.gif)

Varat pievienot **Excel\\Diapazons** un **Excel\\Šūna** ligzdotos elementus **Excel\\Faila** elementam, lai norādītu datu struktūru, kas izpildlaikā tiks ievadīti ģenerētos pārskatos. Pēc tam šie elementi jāsaista ar datu avotiem rediģējamā ER formātā, lai norādītu faktiskos datus, kas izpildlaikā tiks ievadīti ģenerētos pārskatos.

![Ligzdoto elementu pievienošana un Formātu noformētāja lapā.](./media/er-design-configuration-word-image4.gif)

Kad saglabājat izmaiņas ER formātā izstrādes laikā, hierarhiskā formāta struktūra tiek saglabāta pievienotajā Word veidnē kā [pielāgota XML daļa](/visualstudio/vsto/custom-xml-parts-overview) ar nosaukumu **Pārskats**. Jums ir jāpiekļūšana modificētai veidnei, lejupielādējiet to no Finanses, saglabājiet to lokāli un atveriet to Word darbvirsmas programmā. Šajā attēlā ir parādīta lokāli saglabātā parauga veidne kontroles pārskatam, kurā ir ietverta **Pārskata** pielāgotā XML daļa.

![Pārskata parauga veidnes priekšskatīšana Word darbvirsmas programmā.](./media/er-design-configuration-word-image5.gif)

Izpildlaikā tiek darbināti **Excel\\Diapazona** un **Excel\\Šūnu** formāta elementu saistījumi, dati, kurus piegāda katrs saistījums, tiek iekļauti ģenerētajā Word dokumentā kā atsevišķs **Pārskata** pielāgotās XML daļas lauks. Lai ģenerētajā dokumentā ievadītu pielāgotās XML daļas lauku vērtības, word veidnei jāpievieno atbilstošās Word [satura vadīklas](/office/client-developer/word/content-controls-in-word), lai tās būtu kā vietturi izpildlaikā aizpildītajiem datiem. Lai norādītu, kā tiek aizpildītas satura vadīklas, kartējiet katru satura vadīklu uz **Pārskata** pielāgotās XML daļas atbilstošo lauku.

![Satura vadīklu pievienošana un kartēšana Word darbvirsmas programmā.](./media/er-design-configuration-word-image6.gif)

Pēc tam rediģējama ER formāta oriģinālā Word veidne ir jāaizstāj ar modificēto veidni, kas tagad satur Word satura kontroles, kas tika kartētas uz **Pārskata** pielāgotās XML daļas laukiem.

![Veidnes aizvietošana formātu veidotāja lapā.](./media/er-design-configuration-word-image7.gif)

Izpildot konfigurēto ER formātu, pievienotā Word veidne tiek izmantota, lai ģenerētu jaunu pārskatu. Faktiskie dati tiek glabāti Word pārskatā kā pielāgota XML daļa ar nosaukumu **Pārskats**. Kad ir atvērts ģenerētais pārskats, Word satura vadīklas tiek aizpildītas ar datiem no **Pārskata** pielāgotās XML daļas.

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

**Jautājums:** Es konfigurēju ER formātu, lai izdrukātu Word dokumentu, kas satur uzņēmuma adresi. Šī ER formāta Word veidnē es ievietoju bagātinātā teksta satura vadīklu, lai uzrādītu uzņēmuma adresi. Finansēs es ievadīju uzņēmuma adresi kā daudzrindu tekstu un atlasīju **Ievadīt**, lai pievienotu atgriešanu katrā ievadītajā rindā. Tāpēc es sagaidu, ka uzņēmuma adrese ģenerētos dokumentos parādīsies kā daudzrindu teksts. Tomēr adrese tiek parādīta kā atsevišķa teksta rinda, kurā ir īpaši simboli, nevis atgriešanas. Kas nav pareizi ar maniem iestatījumiem?

**Atbilde:** Tā vietā, lai izmantotu bagātinātā teksta satura kontroli, kontroles rekvizītos ir jāizmanto vienkārša teksta satura kontrole un jāatlasa izvēles rūtiņa **Atļaut atgriešanu (vairāku vērtību)**.

## <a name="additional-resources"></a>Papildu resursi

- [ER konfigurāciju ar Excel veidnēm atkārtota izmantošana, lai veidotu pārskatus Word formātā](./tasks/er-design-configuration-word-2016-11.md)
- [Iegulstiet attēlus un formas jūsu ģenerētajos dokumentos, izmantojot ER](electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
