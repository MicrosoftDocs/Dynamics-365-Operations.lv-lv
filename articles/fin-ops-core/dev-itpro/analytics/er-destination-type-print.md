---
title: ER galamērķa printera tips
description: Šajā tēmā sniegta informācija par to, kā konfigurēt arhīva mērķi katrai MAPEI vai FAILA komponentam elektronisko pārskatu (ER) formātā.
author: NickSelin
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 2513fc4f86519c71602089cd46e9757813b1a708
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388292"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>Printera mērķis

[!include [banner](../includes/banner.md)]

Varat nosūtīt ģenerētu dokumentu tieši uz tīkla printeri, lai veiktu tiešo drukāšanu.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms sākat, vispirms jāinstalē un jākonfigurē dokumentu maršrutēšanas aģents un pēc tam jāreģistrē tīkla printeri. Plašāku informāciju skatiet tēmā [Dokumentu maršrutēšanas aģenta instalēšana, lai iespējotu tīkla drukāšanu](./install-document-routing-agent.md)

## <a name="make-the-printer-destination-available"></a>Galamērķa printera pieejamības nodrošināšana

Lai nodrošinātu galamērķa **Printeris** pieejamību pašreizējā Microsoft Dynamics 365 Finance instancē, dodieties uz darbvietu **Līdzekļu pārvaldība** un ieslēdziet tālāk norādītos līdzekļus norādītajā secībā.

1. Elektronisko pārskatu izejošo dokumentu konvertēšana no Microsoft Office dokumentu formāta uz PDF formātu
2. Dokumentu maršrutēšanas aģents kā izejošo dokumentu elektronisko pārskatu veidošanas adresāts

[![ER printera galamērķa līdzekļa ieslēgšana līdzekļu pārvaldībā.](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Piemērojamība

#### <a name="pdf-printing"></a>PDF drukāšana

Finance versijās pirms versijas 10.0.18 printera **mērķi var konfigurēt tikai failu komponentiem, kas tiek izmantoti,** lai ģenerētu izvadi drukājamā PDF formātā (**PDF apvienošanās** vai **PDF faila** formāta elementi) vai Microsoft Office Excel Word formātā (**Excel faila** formāta elements). Kad izvade tiek ģenerēta PDF formātā, tā tiek nosūtīta uz printeri. Kad izvade tiek ģenerēta Office formātā, **izmantojot Excel faila** formāta elementu, tā tiek automātiski konvertēta PDF formātā un pēc tam nosūtīta uz printeri.

Tomēr no versijas 10.0.18 varat konfigurēt **printera** mērķi elementam **Common file** format. Šis formāta elements galvenokārt tiek izmantots, lai ģenerētu izvadi TXT vai XML formātā. Er formātu, kas satur **kopējā faila** formāta elementu, var konfigurēt kā saknes formāta elementu un **binārā satura** formāta elementu kā vienīgo ligzdoto elementu zem tā. Šādā gadījumā elements Common file **format izveidos izvadi formātā,** kas norādīts ar saistījumu, kuru konfigurējat binārā **satura** formāta elementam. Piemēram, varat konfigurēt šo saistījumu, lai aizpildītu [šo](tasks/er-document-management-files-5.md#modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format) elementu ar dokumentu pārvaldības [pielikuma saturu](../../fin-ops/organization-administration/configure-document-management.md) PDF vai Office (Excel vai Word) formātā. Izvadi var izdrukāt, izmantojot konfigurēto **printera** mērķi. 

> [!NOTE]
> Atlasot CommonFile **\\ formāta elementu printera** mērķa konfigurēšanai **, projektēšanas laikā nav iespējams garantēt, ka atlasītais elements radīs izvadi PDF formātā vai izvadē, ko var** konvertēt PDF formātā. Tāpēc tiek parādīts šāds brīdinājuma ziņojums: "Lūdzu, pārliecinieties, vai atlasītā formāta komponenta ģenerēto izvadi var pārvērst par PDF failu. Pretējā gadījumā noņemiet atzīmi no opcijas "Konvertēt uz PDF"." Ir jāveic darbības, lai novērstu izpildlaika problēmas, ja drukāšanai izpildlaikā ir nodrošināta izvade, kas nav PDF izvade vai izvade, kas nav PDF izvade. Ja vēlaties saņemt izvadi Office (Excel vai Word) formātā, **ir jāatlasa opcija Konvertēt uz PDF**.
>
> Versijā 10.0.26 un jaunākās versijās, lai izmantotu **opciju Konvertēt uz PDF**, konfigurētā **printera** mērķa dokumenta maršrutēšanas tipa **parametram** ir jāatlasa **PDF**.

#### <a name="zpl-printing"></a>ZPL druka

Versijā 10.0.26 un jaunākās versijās varat konfigurēt **printera mērķi CommonFile** **formāta elementam\\, atlasot** ZPL **parametram** Dokumenta maršrutēšanas **tips**. Šādā gadījumā **opcija Konvertēt uz PDF** izpildlaikā tiek ignorēta, un TXT vai XML izvade tiek nosūtīta tieši uz atlasīto printeri, izmantojot dokumentu maršrutēšanas aģenta (DRA [) zebras programmēšanas valodas (ZPL) līgumu](install-document-routing-agent.md). Izmantojiet šo līdzekli ER formātam, kas attēlo ZPL II uzlīmju izkārtojumu, lai drukātu dažādas etiķetes.

[![Parametra Dokumenta maršrutēšanas tipa iestatīšana dialoglodziņā Mērķa iestatījumi.](./media/ER_Destinations-SetDocumentRoutingType.png)](./media/ER_Destinations-SetDocumentRoutingType.png)

Papildinformāciju par šo līdzekli skatiet rakstā [Jauna ER risinājuma noformēšana ZPL uzlīmju drukāšanai](er-design-zpl-labels.md).

### <a name="limitations"></a>Ierobežojumi

Galamērķis **Printeris** ir ieviests tikai mākoņa izvietojumiem.

### <a name="use-the-printer-destination"></a>Galamērķa Printeris izmantošana

1. Lai nosūtītu ģenerēto dokumentu uz printeri, atlasiet opcijai **Iespējots** iestatījumu **Jā**.
2. Laukā **Printera nosaukums** atlasiet nepieciešamo tīkla printeri.
3. Atlasiet opcijai **Vai saglabāt drukāšanas arhīvā?** iestatījumu **Jā**, lai saglabātu ģenerēto izvadi drukāšanas arhīvā un tas būtu pieejams turpmākai drukāšanai. Lai vēlāk piekļūtu arhivētai izvadei, dodieties uz **Organizācijas administrēšana** \> **Pieprasījumi un pārskati** \> **Pārskatu arhīvs**.

[![Galamērķa Printeris izmantošana.](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> Konfigurējot galamērķi **Printeris**, opcijai **Pārveidot PDF formātā** nav jābūt ieslēgtai. PDF pārvēršana drukāšanas nolūkiem notiks arī tad, ja opcija ir izslēgta.

Lai izmantotu konkrētu [lapas orientāciju](electronic-reporting-destinations.md#SelectPdfPageOrientation), drukājot izejošo dokumentu Excel formātā, ir jāieslēdz opcija **Konvertēt PDF formātā**. Ja opcija **Konvertēt PDF formātā** ir iestatīta uz **Jā**, kļūst pieejams lauks **Lapas orientācija**. Laukā **Lapas orientācija** var atlasīt lapas orientāciju.

## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko pārskatu veidošanas (ER) apskats](general-electronic-reporting.md)
- [Elektroniskās pārskatu veidošanas (ER) adresāti](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
