---
title: ER galamērķa printera tips
description: Šajā tēmā ir izskaidrots, kā konfigurēt galamērķa printeri katram MAPES vai FAILA komponentam elektroniskās ziņošanas (ER) formātā, kas ir konfigurēts izejošo dokumentu ģenerēšanai vai nu PDF, vai Microsoft Office formātā (Excel\Word).
author: NickSelin
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 148da191ce4ea99c237895c40ec007a1aa0cd537
ms.sourcegitcommit: 0d9ca44b48fb2e33d8160faccc1e6bd932e58934
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150796"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>Galamērķa printeris

[!include [banner](../includes/banner.md)]

Varat nosūtīt ģenerētu dokumentu tieši uz tīkla printeri, lai veiktu tiešo drukāšanu.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms sākat, vispirms jāinstalē un jākonfigurē dokumentu maršrutēšanas aģents un pēc tam jāreģistrē tīkla printeri. Plašāku informāciju skatiet tēmā [Dokumentu maršrutēšanas aģenta instalēšana, lai iespējotu tīkla drukāšanu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent)

## <a name="make-the-printer-destination-available"></a>Galamērķa printera pieejamības nodrošināšana

Lai nodrošinātu galamērķa **Printeris** pieejamību pašreizējā Microsoft Dynamics 365 Finance instancē, dodieties uz darbvietu **Līdzekļu pārvaldība** un ieslēdziet tālāk norādītos līdzekļus norādītajā secībā.

1. Elektronisko pārskatu izejošo dokumentu konvertēšana no Microsoft Office dokumentu formāta uz PDF formātu
2. Dokumentu maršrutēšanas aģents kā izejošo dokumentu elektronisko pārskatu veidošanas adresāts

[![ER printera galamērķa līdzekļa ieslēgšana līdzekļu pārvaldībā](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Piemērojamība

Galamērķi **Printeris** var konfigurēt tikai tādiem failu komponentiem, kas tiek izmantoti izlaides ģenerēšanai drukājamā PDF formātā (PDF faila apvienošanas vai PDF failu formāta elementi) vai Microsoft Office Excel/Word formātā (Excel fails). Kad izvade tiek ģenerēta PDF formātā, tā tiek nosūtīta uz printeri. Ja izvade tiek ģenerēta Microsoft Office formātā, tā tiek automātiski konvertēta PDF formātā un pēc tam nosūtīta uz printeri.

### <a name="limitations"></a>Ierobežojumi

Šis līdzeklis ir priekšskatījuma līdzeklis, un tas ir pakļauts lietošanas noteikumiem, kas aprakstīti sadaļā [Microsoft Dynamics 365 priekšskatījumu papildu lietošanas noteikumi](https://go.microsoft.com/fwlink/?linkid=2105274).

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
