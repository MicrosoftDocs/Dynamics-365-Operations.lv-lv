---
title: "Power BI satura pakotne Naudas pārskats"
description: "Šajā tēmā ir aprakstīta Power BI satura pakotne Naudas pārskats. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti saturā, un ir sniegta informācija par satura izveidei izmantoto datu modeli un elementiem."
author: saraschi2
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: e969c2033463d565ce782c7dc8cfc4b458349289
ms.contentlocale: lv-lv
ms.lasthandoff: 06/20/2017

---

# <a name="cash-overview-power-bi-content"></a>Power BI satura pakotne Naudas pārskats

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstīta Power BI satura pakotne **Naudas pārskats**. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti saturā, un ir sniegta informācija par satura izveidei izmantoto datu modeli un elementiem.

## <a name="overview"></a>Pārskats

Power BI satura pakotne **Naudas pārskats** ir izveidota personām, kuras ir atbildīgas par skaidru naudu savā organizācijā. Power BI satura pakotne **Naudas pārskats** nodrošina piekļuvi informācijai par naudas plūsmu. Tas nodrošina arī prognozes, kas var palīdzēt pieņemt labākus lēmumus un tādējādi uzlabot naudas plūsmas rādītājus. Var analizēt skaidro naudu pēc juridiskās personas, valūtas un bankas konta, lai labāk saprastu pārpalikumus un iztrūkumus.

## <a name="accessing-the-power-bi-content"></a>Piekļūšana Power BI saturam

Ja lietojat programmatūras Dynamics 365 for Finance and Operation izdevuma Enterprise 2017. gada jūlija atjauninājumu, Power BI satura pakotnes **Naudas pārskats** pārskati tiek rādīti darbvietās **Naudas pārskats** un **Banku vadība**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI satura pakotnē iekļautie pārskati
Tālāk esošajā tabulā ir sniegta detalizēta informācija par rādītājiem, kas ir iekļauti katrā Power BI satura pakotnes **Naudas pārskats** pārskata lapā.

| Pārskats                                | Saturs |
|---------------------------------------|----------|
| Naudas pārskats — visi uzņēmumi         | <ul><li>Ieejas un izejas plūsmas sistēmas valūtā</li><li>Prognozētās bilances noteiktā valūtā</li><li>Kopējā bankas bilance sistēmas valūtā</li><li>Bilance pēc juridiskās personas</li><li>Šodienas faktiskās un prognozētās bilances salīdzinājums bankas konta valūtā</li></ul> |
| Naudas pārskats — pašreizējais uzņēmums       | <ul><li>Ieejas un izejas plūsmas uzskaites valūtā</li><li>Prognozētās bilances noteiktā valūtā</li><li>Kopējā bankas bilance uzskaites valūtā</li><li>Šodienas faktiskās un prognozētās bilances salīdzinājums bankas konta valūtā</li></ul> |
| Naudas plūsmas prognoze — visi uzņēmumi    | <ul><li>Ieejas un izejas plūsmas sistēmas valūtā</li><li>Kopsavilkums par ikdienas prognozi</li><li>Detalizēta informācija prognozi</li></ul> |
| Naudas plūsmas prognoze — pašreizējais uzņēmums | <ul><li>Ieejas un izejas plūsmas uzskaites valūtā</li><li>Kopsavilkums par ikdienas prognozi</li><li>Detalizēta informācija prognozi</li></ul> |
| Prognoze noteiktā valūtā                     | <ul><li>Prognozētās bilances noteiktā valūtā</li><li>Ikdienas kopsavilkums noteiktā valūtā</li><li>Detalizēta informācija prognozi</li></ul> |
| Bankas bilances                         | <ul><li>Kopējā bankas bilance sistēmas valūtā</li><li>Bilance pēc juridiskās personas</li><li>Šodienas faktiskās un prognozētās bilances salīdzinājums bankas konta valūtā</li><li>Bilance pēc bankas konta</li><li>Bilance pēc valūtas</li></ul> |

## <a name="extending-the-power-bi-content"></a>Power BI satura paplašināšana
Izmantojot pakalpojumā Lifecycle Services (LCS) pieejamās satura pakotnes, varat nodrošināt lieliskus analīzes datus personām, kuras nepiesakās programmatūrā Dynamics 365. Šīs satura pakotnes var izmainīt, tajās ietverot citus pārskatus vai vizualizācijas, un pēc tam publicēt jūsu Power BI.com nomniekā analīzes veikšanai. 

Power BI satura pakotne **Naudas pārskats** ir pieejama LCS koplietojamo līdzekļu bibliotēkā. Papildinformāciju par to, kā lejupielādēt satura pakotni un ieviest to savā organizācijā, skatiet tēmā [Power BI saturs pakalpojumā LCS no Microsoft un jūsu partneriem](/dynamics365/unified-operations/dev-itpro/analytics/power-bi-content-microsoft-partners). Power BI satura pakotnes implementēšanas demonstrāciju skatiet tēmā [Power BI saturs pakalpojumā Dynamics Lifecycle Services no Microsoft un jūsu partneriem](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana

Tālāk esošajā tabulā ir norādīti elementi, kas ir izmantoti Power BI satura pakotnes **Naudas pārskats** izveidei.

| Elements                                                                          | Saturs |
|---------------------------------------------------------------------------------|----------|
| LedgerCovLiquidityMeasurement\_Company                                          | Uzņēmumi, pēc kuriem pārskatus filtrēt |
| LedgerCovLiquidityMeasurement\_Date                                             | Datumi pārskatu filtrēšanai |
| LedgerCovLiquidityMeasurement\_LedgerCovForecastActual                          | Faktiskās bankas bilances un pēdējās prognozētās bankas bilances salīdzinājums |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidity                               | Detalizēta informācija par prognozēto transakciju |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany    | Kopsavilkums par skaidras naudas ieejas un izejas plūsmām un bilanci katra uzņēmuma uzskaites valūtā |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise | Kopsavilkums par skaidras naudas ieejas un izejas plūsmām un bilanci sistēmas valūtā visiem uzņēmumiem |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency            | Kopsavilkums par transakcijas neto summu un bilanci noteiktās valūtās, izmantojot transakcijas valūtu |

Šie elementi tika izmantoti, lai datu modelī izveidotu aprēķinātus mērus. Pēc tam šie aprēķinātie mēri tiek lietoti, lai aprēķinātu diagrammas un pārskatus, kas tiek izmantoti Power BI satura pakotnē **Naudas pārskats**. Lai pārskatos vai informācijas panelī ietvertu papildu aprēķinus, varat lejupielādēt Power BI failu no pakalpojuma LCS un izmainīt to. Šis fails ir noklusējuma datu modelis, kas tika izmantots satura pakotnes izveidei. Kad esat pabeidzis izmaiņu veikšanu, varat izveidot organizācijas satura pakotni un informācijas paneļus, kas satur jūsu pievienoto informāciju.


