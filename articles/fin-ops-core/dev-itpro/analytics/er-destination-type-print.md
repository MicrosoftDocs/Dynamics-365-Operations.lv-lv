---
title: ER galamērķa printera tips
description: Šajā tēmā sniegta informācija par to, kā konfigurēt arhīva mērķi katrai MAPEI vai FAILA komponentam elektronisko pārskatu (ER) formātā.
author: NickSelin
ms.date: 02/24/2021
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
ms.openlocfilehash: 7749a458020de664d00e81ccf0e480ae459da617
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894008"
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

[![ER printera galamērķa līdzekļa ieslēgšana līdzekļu pārvaldībā](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Piemērojamība

Galamērķi **Printeris** var konfigurēt tikai tādiem failu komponentiem, kas tiek izmantoti izlaides ģenerēšanai drukājamā PDF formātā (PDF faila apvienošanas vai PDF failu formāta elementi) vai Microsoft Office Excel/Word formātā (Excel fails). Kad izvade tiek ģenerēta PDF formātā, tā tiek nosūtīta uz printeri. Ja izvade tiek ģenerēta Microsoft Office formātā, tā tiek automātiski konvertēta PDF formātā un pēc tam nosūtīta uz printeri.

### <a name="limitations"></a>Ierobežojumi

Galamērķis **Printeris** ir ieviests tikai mākoņa izvietojumiem.

### <a name="use-the-printer-destination"></a>Galamērķa Printeris izmantošana

1. Lai nosūtītu ģenerēto dokumentu uz printeri, atlasiet opcijai **Iespējots** iestatījumu **Jā**.
2. Laukā **Printera nosaukums** atlasiet nepieciešamo tīkla printeri.
3. Atlasiet opcijai **Vai saglabāt drukāšanas arhīvā?** iestatījumu **Jā**, lai saglabātu ģenerēto izvadi drukāšanas arhīvā un tas būtu pieejams turpmākai drukāšanai. Lai vēlāk piekļūtu arhivētai izvadei, dodieties uz **Organizācijas administrēšana** \> **Pieprasījumi un pārskati** \> **Pārskatu arhīvs**.

[![Galamērķa Printeris izmantošana](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> Konfigurējot galamērķi **Printeris**, opcijai **Pārveidot PDF formātā** nav jābūt ieslēgtai. PDF pārvēršana drukāšanas nolūkiem notiks arī tad, ja opcija ir izslēgta.

Lai izmantotu konkrētu [lapas orientāciju](electronic-reporting-destinations.md#SelectPdfPageOrientation), drukājot izejošo dokumentu Excel formātā, ir jāieslēdz opcija **Konvertēt PDF formātā**. Ja opcija **Konvertēt PDF formātā** ir iestatīta uz **Jā**, kļūst pieejams lauks **Lapas orientācija**. Laukā **Lapas orientācija** var atlasīt lapas orientāciju.

## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko pārskatu veidošanas (ER) apskats](general-electronic-reporting.md)
- [Elektroniskās pārskatu veidošanas (ER) adresāti](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]