---
title: ER galamērķa printera tips
description: Šajā rakstā skaidrots, kā var konfigurēt printera mērķi katrai mapei vai faila komponentam elektronisko pārskatu (ER) formātā.
author: kfend
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: 7e01476b85c6c35d7c36c90db4d64ab2a2930fec
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271740"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>Printera mērķis

[!include [banner](../includes/banner.md)]

Varat nosūtīt ģenerētu dokumentu tieši uz tīkla printeri, lai veiktu tiešo drukāšanu.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms sākat, vispirms jāinstalē un jākonfigurē dokumentu maršrutēšanas aģents un pēc tam jāreģistrē tīkla printeri. Plašāku informāciju skatiet tēmā [Dokumentu maršrutēšanas aģenta instalēšana, lai iespējotu tīkla drukāšanu](./install-document-routing-agent.md)

## <a name="make-the-printer-destination-available"></a>Galamērķa printera pieejamības nodrošināšana

Lai printera **mērķis** Microsoft Dynamics būtu pieejams pašreizējā 365 Finansu instancē, **dodieties** uz līdzekļu pārvaldības darbvietu un slēdziet šādus līdzekļus šādā secībā:

1. Elektronisko pārskatu izejošo dokumentu konvertēšana no Microsoft Office dokumentu formāta uz PDF formātu
2. Dokumentu maršrutēšanas aģents kā izejošo dokumentu elektronisko pārskatu veidošanas adresāts

[![ER printera galamērķa līdzekļa ieslēgšana līdzekļu pārvaldībā.](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Piemērojamība

#### <a name="pdf-printing"></a>PDF drukāšana

Finanšu versijās pirms versijas 10.0.18 printera mērķi var konfigurēt tikai failu komponentiem, **kas** tiek izmantoti izvadei drukājamā PDF formātā (**PDF apvienošanas** **vai PDF** failu formāta elementi) Microsoft Office Excel un Word formātā (**Excel faila** formāta elements). Kad izvade ir izveidota PDF formātā, tā tiek nosūtīta uz printeri. Kad izvade tiek ģenerēta Office formātā, **izmantojot Excel** faila formāta elementu, tas automātiski tiek pārveidots PDF formātā un pēc tam nosūtīts uz printeri.

Tomēr no versijas 10.0.18 varat konfigurēt **printera** mērķi kopēja faila **formāta** elementam. Šis formāta elements lielākoties tiek izmantots, lai ģenerētu izvadi TXT vai XML formātā. Varat konfigurēt **ER** **formātu, kas kopējā faila formāta elementu satur kā saknes formāta elementu un Bināro** satura formāta elementu kā vienīgais ligzdotais elements zem tā. Šajā gadījumā kopējā faila formāta **elements** izveidos izvadi formātā, kas norādīts ar saistījumu, ko **konfigurējat Binārā satura formāta** elementam. Piemēram, varat konfigurēt [šo](tasks/er-document-management-files-5.md#modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format)[saistīšanu](../../fin-ops/organization-administration/configure-document-management.md), lai aizpildītu šo elementu ar dokumentu pārvaldības pielikuma saturu PDF vai Office (Excel vai Word) formātā. Varat izdrukāt izvades informāciju, izmantojot konfigurēto printera **mērķi**. 

> [!NOTE]
> Kad izvēlaties **\\** **Kopējā** faila formāta elementu, lai konfigurētu Printera mērķi, nav veida, kā nodrošināt, ka izvēlētajam elementam jāražo izvade PDF formātā vai izvade, ko var konvertēt PDF formātā. Tāpēc jūs saņemat šādu brīdinājuma ziņojumu: "Lūdzu, pārliecinieties, ka atlasītā formāta komponenta ģenerēto izvadi var pārvērst PDF formātā. Pretējā gadījumā noņemiet atzīmi no opcijas Pārvērst par PDF." Jāveic darbības, lai palīdzētu novērst izpildlaika problēmas, ja izpildlaikā tiek nodrošināta drukāšanai, kas nav PDF vai nav PDF konvertējama izvade. Ja vēlaties saņemt izvades informāciju Office (Excel vai Word) formātā, **jābūt atlasītai opcijai Pārvērst par PDF**.
>
> Versijā 10.0.26 un jaunākā versijā, lai izmantotu opciju Pārvērst par PDF, **ir jāatlasa PDF** **konfigurētā** printera mērķa dokumentu maršrutēšanas **tipa parametram.** **·**

#### <a name="zpl-printing"></a>ZPL drukāšana

Versijā 10.0.26 un jaunākā versijā varat konfigurēt printera mērķi kopējam faila formāta elementam, **·** **\\** atlasot ZPL **dokumentu** maršrutēšanas tipa parametram.**·** Šajā gadījumā **izpildlaikā opcija Pārvērst par PDF** tiek ignorēta, un TXT vai XML izvade tiek nosūtīta tieši uz atlasīto printeri, izmantojot Līgumu Par Papildmaksu programmēšanas valodu (ZPL), [kas atrodas Dokumentu maršrutēšanas aģentam (DRA).](install-document-routing-agent.md) Izmantojiet šo funkciju ER formātam, kas parāda ZPL II etiķetes izkārtojumu dažādu etiķešu drukāšanai.

[![Dokumentu maršrutēšanas tipa parametra iestatīšana dialoglodziņā Mērķa iestatījumi.](./media/ER_Destinations-SetDocumentRoutingType.png)](./media/ER_Destinations-SetDocumentRoutingType.png)

Plašāku informāciju par šo līdzekli skatiet Izstrādājiet [jaunu ER risinājumu ZPL etiķešu drukāšanai](er-design-zpl-labels.md).

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
