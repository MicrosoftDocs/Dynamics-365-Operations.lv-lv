---
title: Power BI satura pakotne Skaidras naudas apskats
description: Šajā tēmā ir aprakstīta Power BI satura pakotne Skaidras naudas apskats. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti saturā, un ir sniegta informācija par satura izveidei izmantoto datu modeli un elementiem.
author: saraschi2
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: d070ddd350bc1ca9edb311cfd9f015aca1e7cc78
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897456"
---
# <a name="cash-overview-power-bi-content"></a>Power BI satura pakotne Skaidras naudas apskats

[!include [banner](../includes/banner.md)]

Šajā aprakstīts Microsoft Power BI saturs **Skaidras naudas apskats**. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti saturā, un ir sniegta informācija par satura izveidei izmantoto datu modeli un elementiem.

## <a name="overview"></a>Pārskats

Power BI satura pakotne **Skaidras naudas apskats** ir izveidota personām, kuras ir atbildīgas par skaidru naudu savā organizācijā. Power BI satura pakotne **Skaidras naudas apskats** nodrošina naudas plūsmas pārskatāmību. Tas nodrošina arī prognozes, kas var palīdzēt pieņemt labākus lēmumus un tādējādi uzlabot naudas plūsmas rādītājus. Var analizēt skaidro naudu pēc juridiskās personas, valūtas un bankas konta, lai labāk saprastu pārpalikumus un iztrūkumus.

## <a name="setup-needed-to-view-power-bi-content"></a>Power BI satura skatīšanai nepieciešamie iestatījumi

Lai dati tiktu rādīti darbvietu **Skaidras naudas apskats** un **Bankas pārvaldība** Power BI vizuālajos līdzekļos, ir jāveic tālāk norādītā iestatīšana.

1. Dodieties uz **Sistēmas administrēšana > Iestatīšana > Sistēmas parametri** un iestatiet parametrus **Sistēmas valūta** un **Sistēmas maiņas kurss**.
2. Lai validētu finanšu kalendāra datumus, kas piešķirti aktīvajam laika periodam, dodieties uz **Virsgrāmata > Kalendāri > Finanšu kalendāri**.
3. Dodieties uz **Virsgrāmata > Iestatīšana > Virsgrāmata**, lai iestatītu vienumu **Uzskaites valūta** un **Maiņas kursa tips**.
4. Nosakiet maiņas kursu starp transakciju valūtām un uzskaites valūtu, starp uzskaites valūtu un sistēmas valūtu, starp uzskaites valūtu un bankas valūtām. Lai to izdarītu, dodieties uz **Virsgrāmata > Valūtas > Valūtas maiņas kursi**.
5. Konfigurējiet un palaidiet rīku Naudas plūsmas prognozēšana. Plašāku informāciju par to, kā iestatīt rīku Naudas plūsmas prognozēšana, skatiet tēmā [Naudas plūsmas prognozēšana](./cash-flow-forecasting.md). 
6. Dodieties uz **Sistēmas administrēšana > Iestatīšana > Elementu krātuve** un atsvaidziniet apkopošanas mērījumu **LedgerCovLiquidityMeasurement**.

## <a name="accessing-the-power-bi-content"></a>Piekļuve Power BI satura pakotnei

Power BI satura pakotnes **Skaidras naudas apskats** pārskati tiek rādīti darbvietās **Skaidras naudas apskats** un **Bankas pārvaldība**.

Lai skatītu naudas plūsmas prognožu pārskatus ar datiem, jums vispirms ir jāpalaiž prognožu aprēķina process, izmantojot apgabalā Naudas un bankas pārvaldība esošo funkciju **Aprēķināt naudas plūsmas prognozes**. Šī funkcija ir jāaizpilda katram prognozē ietvertajam uzņēmumam.  Pēc tam ir jāatsvaidzina apkopošanas mērījums LedgerCovLiquidityMeasurement lapā **Elementu krātuve**.  

Demonstrācijas nolūkos varat pievienot naudas plūsmas prognožu demonstrācijas datus, izmantojot modulī Demonstrācijas dati esošo lapu **Ģenerēt datus**.  Šis skripts ievietos datus naudas plūsmas prognožu tabulās, lai ātri aizpildītu pārskatiem nepieciešamo informāciju.  Šis modulis ir pieejams tikai tad, ja vidē ir izvietots demonstrācijas datu komplekta modelis. 

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI satura pakotnē iekļautie pārskati

Tālāk esošajā tabulā ir sniegta detalizēta informācija par rādītājiem, kas ir iekļauti katrā Power BI satura pakotnes **Skaidras naudas apskats** pārskata lapā.

| Pārskats                                | Saturs |
|---------------------------------------|----------|
| Naudas pārskats — visi uzņēmumi         | <ul><li>Ieejas un izejas plūsmas sistēmas valūtā</li><li>Prognozētās bilances noteiktā valūtā</li><li>Kopējā bankas bilance sistēmas valūtā</li><li>Bilance pēc juridiskās personas</li><li>Šodienas faktiskās un prognozētās bilances salīdzinājums bankas konta valūtā</li></ul> |
| Naudas pārskats — pašreizējais uzņēmums       | <ul><li>Ieejas un izejas plūsmas uzskaites valūtā</li><li>Prognozētās bilances noteiktā valūtā</li><li>Kopējā bankas bilance uzskaites valūtā</li><li>Šodienas faktiskās un prognozētās bilances salīdzinājums bankas konta valūtā</li></ul> |
| Naudas plūsmas prognoze — visi uzņēmumi    | <ul><li>Ieejas un izejas plūsmas sistēmas valūtā</li><li>Kopsavilkums par ikdienas prognozi</li><li>Detalizēta informācija prognozi</li></ul> |
| Naudas plūsmas prognoze — pašreizējais uzņēmums | <ul><li>Ieejas un izejas plūsmas uzskaites valūtā</li><li>Kopsavilkums par ikdienas prognozi</li><li>Detalizēta informācija prognozi</li></ul> |
| Prognoze noteiktā valūtā                     | <ul><li>Prognozētās bilances noteiktā valūtā</li><li>Ikdienas kopsavilkums noteiktā valūtā</li><li>Detalizēta informācija prognozi</li></ul> |
| Bankas bilances                         | <ul><li>Kopējā bankas bilance sistēmas valūtā</li><li>Bilance pēc juridiskās personas</li><li>Šodienas faktiskās un prognozētās bilances salīdzinājums bankas konta valūtā</li><li>Bilance pēc bankas konta</li><li>Bilance pēc valūtas</li></ul> |


## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana

Tālāk esošajā tabulā ir norādīti elementi, kas tiek izmantoti Power BI satura pakotnes **Skaidras naudas apskats** izveidei.

| Elements                                                                          | Saturs |
|---------------------------------------------------------------------------------|----------|
| LedgerCovLiquidityMeasurement\_Company                                          | Uzņēmumi, pēc kuriem pārskatus filtrēt |
| LedgerCovLiquidityMeasurement\_Date                                             | Datumi pārskatu filtrēšanai |
| LedgerCovLiquidityMeasurement\_LedgerCovForecastActual                          | Faktiskās bankas bilances un pēdējās prognozētās bankas bilances salīdzinājums |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidity                               | Detalizēta informācija par prognozēto transakciju |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany    | Kopsavilkums par skaidras naudas ieejas un izejas plūsmām un bilanci katra uzņēmuma uzskaites valūtā |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise | Kopsavilkums par skaidras naudas ieejas un izejas plūsmām un bilanci sistēmas valūtā visiem uzņēmumiem |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency            | Kopsavilkums par transakcijas neto summu un bilanci noteiktās valūtās, izmantojot transakcijas valūtu |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]