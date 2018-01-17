---
title: "Power BI satura pakotne Naudas pārskats"
description: "Šajā tēmā ir aprakstīta Power BI satura pakotne Naudas pārskats. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti saturā, un ir sniegta informācija par satura izveidei izmantoto datu modeli un elementiem."
author: saraschi2
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: cb43245afe578341251b140383a3b03ba2abd962
ms.openlocfilehash: 5d02a009ca988f91a212e467d4f9784248bbae76
ms.contentlocale: lv-lv
ms.lasthandoff: 12/19/2017

---

# <a name="cash-overview-power-bi-content"></a>Power BI satura pakotne Naudas pārskats

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstīta Power BI satura pakotne **Naudas pārskats**. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti saturā, un ir sniegta informācija par satura izveidei izmantoto datu modeli un elementiem.

## <a name="overview"></a>Pārskats

Power BI satura pakotne **Naudas pārskats** ir izveidota personām, kuras ir atbildīgas par skaidru naudu savā organizācijā. Power BI satura pakotne **Naudas pārskats** nodrošina piekļuvi informācijai par naudas plūsmu. Tas nodrošina arī prognozes, kas var palīdzēt pieņemt labākus lēmumus un tādējādi uzlabot naudas plūsmas rādītājus. Var analizēt skaidro naudu pēc juridiskās personas, valūtas un bankas konta, lai labāk saprastu pārpalikumus un iztrūkumus.

## <a name="accessing-the-power-bi-content"></a>Piekļūšana Power BI saturam

Pārskati no Power BI satura pakotnes **Naudas pārskats** tiek rādīti darbvietās **Naudas pārskats** un **Bankas pārvaldība**.

Lai skatītu naudas plūsmas prognožu pārskatus ar datiem, jums vispirms ir jāpalaiž prognožu aprēķina process, izmantojot apgabalā Naudas un bankas pārvaldība esošo funkciju **Aprēķināt naudas plūsmas prognozes**.  Šī funkcija ir jāaizpilda katram prognozē ietvertajam uzņēmumam.  Pēc tam ir jāatsvaidzina apkopošanas mērījums LedgerCovLiquidityMeasurement lapā **Elementu krātuve**.  

Demonstrācijas nolūkos varat pievienot naudas plūsmas prognožu demonstrācijas datus, izmantojot modulī Demonstrācijas dati esošo lapu **Ģenerēt datus**.  Šis skripts ievietos datus naudas plūsmas prognožu tabulās, lai ātri aizpildītu pārskatiem nepieciešamo informāciju.  Šis modulis ir pieejams tikai tad, ja vidē ir izvietots demonstrācijas datu komplekta modelis. 

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



