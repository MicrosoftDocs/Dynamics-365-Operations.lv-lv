---
title: Cenu, atlaižu un līgumu problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar cenām, atlaidēm un līgumiem.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 14fdddabde7739cbf9ba0fcee0fa0b8b816e74dd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007370"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a>Cenu, atlaižu un līgumu problēmu novēršana

Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar cenām, atlaidēm un līgumiem.

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a>Nevar sasaistīt pirkšanas līgumu ar pirkšanas pasūtījuma rindu pēc pirkšanas pasūtījuma izveides.

Pirkšanas līgums ar pirkšanas pasūtījumu ir jāsaista pirkšanas pasūtījuma izveides laikā. Pretējā gadījumā pirkšanas pasūtījuma rindas nevar saistīt ar pirkšanas līguma rindām.

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>Kāda pārbaude parāda ziņojumu “Atjauniniet cenas un atlaides, kas ievadītas manuāli vai ārējā dokumentā”?

Mainot nosūtīšanas datumu, var saņemt ziņojumu ar tekstu “Atjauniniet cenas un atlaides, kas ievadītas manuāli vai ārējā dokumentā.” Šis ziņojums tiek parādīts, jo, mainot nosūtīšanas datumu, var rasties cits tirdzniecības vai pārdošanas līgums un tas var izraisīt cenu izmaiņas. Nosūtīšanas datuma maiņa var ietekmēt arī noliktavas grafikus un citu saistīto informāciju.

Ziņojums tiek parādīts katru reizi, kad tiek mainīti datumi vai citi parametri. Ziņojuma mērķis ir pārliecināties, vai esat informēts par cenu izmaiņām, kas var rasties šo izmaiņu dēļ.

Ziņojums ir tirdzniecības līguma novērtēšanas (TAE) uzvedne. Pilnu aprakstu skatiet [Tirdzniecības līguma novērtēšanas politikas](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>Pirkšanas pasūtījuma kvīts neietver visas maksas.

### <a name="reproduce-the-issue"></a>Problēmas atveide

Nākamajā procedūrā ir parādīts viens šīs problēmas atveides veids.

1. Lapā **Sagādes un avotu parametri** cilnē **Piegāde** pārliecinieties, vai opcija **Produktu ieejas plūsmas maksu ģenerēšana** ir iestatīta uz *Jā*.
1. Izveidojiet pirkšanas pasūtījumu, kurā ietvertas maksas.
1. Apstipriniet pirkšanas pasūtījumu.
1. Saņemiet pirkšanas pasūtījumu.
1. Apskatiet kvīts kopsummu un salīdziniet to ar prognozēto kopsummu.
1. Ievērojiet, ka pirkšanas pasūtījuma kvītī nav ietvertas visas maksas.

### <a name="issue-resolution"></a>Problēmas risinājums

Risinājums ir atkarīgs no veida, kādā ir iestatītas papildmaksas. Lai iegūtu informāciju par to, kā iestatīt papildmaksas, kas atbilst jūsu prasībām, skatiet šo emuāra ierakstu: [Papildmaksu grāmatošana produktu ieejas plūsmas laikā](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a>Tirdzniecības līgumu cenas un atlaides netiek lietotas pārdošanas vai pirkšanas pasūtījuma rindās, kas ir importētas, izmantojot datu pārvaldību.

### <a name="issue-description"></a>Problēmas apraksts

Pārdošanas vai pirkšanas pasūtījuma rindām piemērojamie tirdzniecības līgumi netiek lietoti rindās, kas ir importētas, izmantojot datu pārvaldību. Tomēr tie paši tirdzniecības līgumi tiek lietoti pārdošanas vai pirkšanas pasūtījuma rindās, kas ir izveidotas manuāli.

### <a name="reason-for-the-issue"></a>Problēmas iemesls

Ja pirkšanas pasūtījuma rindās, kas ir importētas, izmantojot datu pārvaldību, jau ir iekļauta cenas informācija, tirdzniecības līgums šīm rindām netiks pārvērtēts. Piemēram, ja rindai ir iestatīta **Rindas atlaide procentos** vai kāda no cenu un atlaižu vērtībām, tad tirdzniecības līgumi šai rindai netiks meklēti.

### <a name="issue-workaround"></a>Problēmas aprisinājums

Šāda darbība ir paredzama un ir līdzīga gan pārdošanas pasūtījumiem, gan pirkšanas pasūtījumiem.

Kā aprisinājumu, importējiet pirkšanas pasūtījuma rindas bez cenas informācijas iestatīšanas. Pēc tam tiks lietoti tirdzniecības līgumi, un pirkšanas pasūtījuma rindas tiks atjauninātas, pamatojoties uz definētajiem tirdzniecības līgumiem.

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>Kreditora atlaide netiek uzkrāta, pamatojoties uz rēķiniem.

### <a name="issue-description"></a>Problēmas apraksts

Ja iegrāmatotajiem rēķiniem ir atšķirīgi izpildes datumi, šie rēķini netiek atspoguļoti no tiem ģenerētajās kreditoru atlaidēs.

### <a name="issue-resolution"></a>Problēmas risinājums

Aprēķinot kreditora atlaidi, izpildes datums netiek ņemts vērā. Apsveriet iespēju pielāgot sistēmu tā, lai izpildes datums un saistība ar rēķinu būtu skaidrāka attiecībā uz faktisko kreditora atlaidi.

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>Vienības cenas pirkšanas pasūtījumos netiek aprēķinātas, pamatojoties uz vienību pārveidošanu.

### <a name="issue-description"></a>Problēmas apraksts

Mainot vienību pirkšanas pasūtījumā, tirdzniecības līguma cenas netiek pārrēķinātas atbilstoši vienības pārveidošanas definīcijām.

### <a name="issue-resolution"></a>Problēmas risinājums

Cenas vienmēr tiek iegūtas no tirdzniecības līgumiem (vai citiem cenas iestatījumiem sistēmā, piemēram, pārdošanas līgumiem vai krājuma cenām), un tās tiek noteiktas vienībai.

Ja pasūtījuma rindā ir mainīta vienība, sistēma meklē jaunās vienības cenu un to piemēro. Ja vienības cena netiek atrasta, sistēma cenu nepiemēro. Vienības pārveidošanu nevar izmantot, lai pārrēķinātu cenu citā vienībā. Teorētiski desmit kastes par vienas kastes cenu var nebūt vienāds ar vienas kastes desmitkārtīgu cenu.

### <a name="issue-workaround"></a>Problēmas aprisinājums

Viens no veidiem, kā atrisināt šo problēmu, ir pārliecināties, vai tiks izmantoti tirdzniecības līgumi vienībām, kuras, iespējams, tiks izmantotas krājuma pasūtījuma rindās.

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a>Tirdzniecības līgumos rodas valūtas konvertēšanas problēmas.

Tirdzniecības līgumu cenas netiek pārrēķinātas atbilstoši valūtai, ja valūta pirkšanas pasūtījumā atšķiras.

Līdzeklis *Vispārējā valūta* ļauj noteikt cenas un atlaides tikai vienā valūtā. Pēc tam varat konvertēt uz citām valūtām, pēc nepieciešamības. Turklāt, pēc konvertēšanas, līdzekli var automātiski lietot noapaļošanai uz leju.

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a>Atverot Pirkšanas līguma lapu rindas skata režīmā, to nevar personalizēt, rindas pārskatā pievienojot lauku Cenas vienība.

Dažus līguma struktūras kopīgotos laukus nevar iekļaut personalizācijās. Šis ierobežojums rodas ieviestā datu modeļa dēļ. Tāpēc nav iespējams personalizēt lauku **Cenas vienība**.

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a>Pirkšanas līguma maksimālais ierobežojums nav spēkā pirkšanas pieprasījumā.

### <a name="issue-description"></a>Problēmas apraksts

Kad pirkšanas pieprasījums ir saistīts ar pirkšanas līgumu, pirkšanas līguma maksimālais ierobežojums nav spēkā pirkšanas pieprasījumā. Noklusējuma cenas informācija ir ievadīta pareizi, tomēr pirkšanas pieprasījumā nevar pasūtīt vairāk par pirkšanas līguma maksimālo ierobežojumu.

### <a name="issue-resolution"></a>Problēmas risinājums

Šāda darbība ir paredzama. Tā kā pieprasījumi ne vienmēr tiek apstiprināti, daudzums vai summa pirkšanas līgumā nav jārezervē. Tādējādi netiks sasniegts pirkšanas līguma maksimālais ierobežojums.

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a>Tirdzniecības līgumus var izveidot no noraidītajiem piedāvājumu pieprasījumiem (PP). Tādējādi sistēma neliedz tirdzniecības līgumu žurnālu izveidi, ja PP rinda nav pieņemta.

Tirdzniecības līgumus var izveidot jebkurai atbildei uz piedāvājuma pieprasījumu (PP) neatkarīgi no tā, vai tie ir pieņemti vai noraidīti. Papildinformāciju skatiet rakstā [Piedāvājuma pieprasījumu (PP) pārskats](request-quotations.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]