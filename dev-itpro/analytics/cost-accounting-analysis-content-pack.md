---
title: "Izmaksu uzskaites analīze Power BI saturu"
description: "Šajā tēmā ir aprakstīts, iekļauto izmaksu uzskaites analīze Power BI saturu. To skaidro kā piekļūt varas BI atskaites un sniedz informāciju par datu modelis un vienībām, kas tika izmantoti, lai veidotu saturu."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 50e7bd92ee693f59fd013226aee22bd1a54c81e2
ms.lasthandoff: 03/31/2017


---

# <a name="cost-accounting-analysis-power-bi-content"></a>Izmaksu uzskaites analīze Power BI saturu

Šajā tēmā ir aprakstīts, iekļauto izmaksu uzskaites analīze Power BI saturu. To skaidro kā piekļūt varas BI atskaites un sniedz informāciju par datu modelis un vienībām, kas tika izmantoti, lai veidotu saturu.

<a name="overview"></a>Pārskats
--------

**Izmaksu uzskaites analīze** Microsoft Power BI saturs ir paredzēts izmaksu kontrolieri vai ikviens, kurš ir atbildīgs par veicot izmaksu kontroles organizācija. Tā ietver galvenajiem rādītājiem, piemēram, izmaksas, apjoma un izmaksu likmi faktiskajām izmaksām, izmaksu budžets un elastīgās budžeta izmaksas. Tas izmanto Microsoft Dynamics 365 darījumu datus no izmaksu uzskaites darbības un nodrošina kopējo izmaksu viedokļa visai organizācijai vienā pārskata valūtā. Vadītāji var datus filtrēt pēc izmaksu objektiem, lai veiktu to struktūrvienībām, izmaksu kontrolei pat tad, ja organizācija var būt vairākas juridiskās personas. Jo **izmaksu uzskaites analīze** Power BI saturu iezīmē atšķirības starp faktiskajām izmaksām un budžetā paredzētajām izmaksām, vadītāji var paziņot par pozitīvās un negatīvās tendences to operatīvo vienību. Vadītāji var detalizēti izmaksu elementu hierarhiju vai atsevišķu izmaksu elementus, iegūt detalizētu ieskatu par to, kā izmaksu dispersijas notikusi, un tad veikt efektīvu rīcību. **Izmaksu uzskaites analīze** Power BI satura, let's izmaksas grāmatveži analizēt, kā izmaksu plūsmu caur izmaksu objektus visā organizācijā. Plašāku informāciju par izmaksu uzskaiti skatiet rakstā [izmaksu uzskaites mājas lapā](/dynamics365/operations/financials/cost-accounting/cost-accounting-home-page.md). Nosakot piekļuves līmeņa drošības izmaksu uzskaitē un apvienojot to ar jaudu BI rindu līmeņa drošību, piekļuvi var piešķirt visas izmaksas objekta īpašniekiem līdz **izmaksu uzskaites analīze** BI enerģijas saturu. Visu datu vizualizācijas būs tad tikt filtrētas par piekļuves līmenis, kas kontrolē izmaksu uzskaitē. Lai uzzinātu vairāk par drošības piekļuves līmeni un rindu līmeņa drošību, skatiet [iestatīt drošības izmaksu uzskaites satura pilnvaras BI](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Piekļuvi saturam Power BI
Jūs varat atrast **izmaksu uzskaites analīze** Power BI satura bibliotēkā Shared aktīvu programmā Microsoft Dynamics Lifecycle Services (LCS). Plašāku informāciju par to, kā lejupielādēt saturu un savienojiet to ar savu dinamiku 365 darbības datiem, skatiet [Power BI saturu no Microsoft un partneri LCS](power-bi-content-microsoft-partners.md). **Piezīme:** KB4011327 * * * * ir priekšnoteikums, lai **izmaksu uzskaites analīze** BI enerģijas saturu.  Pēc pieteikšanās Lifecycle Services, jūs varat piekļūt KB šeit: <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metriku, kas iekļauti barošanas BI saturu
Saturs ietver virkni atskaišu lappusēm. Katras lappuses sastāv no metriku, kas iztēlojās kā diagrammas, flīzes un tabulas. Tālāk redzamajā tabulā sniegts pārskats par vizualizāciju, **izmaksu uzskaites analīze** BI enerģijas saturu.

| Atskaites lapu                      | Diagramma                                                                                                                         | Elements                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Izmaksu kontrole finanšu periodu    | Faktisko un budžeta izmaksas pa izmaksu elementu hierarhijas līmenī                                                                   | Faktiskās izmaksas vs budžeta izmaksas                    |
|                                  | Budžeta starpības izmaksu elementu hierarhijas līmeni                                                                               | Faktisko izmaksu likme vs budžeta izmaksu likme          |
|                                  | Top 10 budžeta dispersijas procentus izmaksu elements                                                                          | Faktisko apjomu vs budžeta apjoms          |
| Izmaksu kontrole, gada rādītāji uz šodienu     | Faktiskās un budžeta izmaksas par kalendāra gada periodu                                                                           | Faktiskās izmaksas vs budžeta izmaksas                    |
|                                  | Budžeta variācijas par kalendāra gada periodu                                                                                       | Faktisko izmaksu likme vs budžeta izmaksu likme          |
|                                  | Top 10 budžeta dispersijas procentus izmaksu elements                                                                          | Faktisko apjomu vs budžeta apjoms          |
| Izmaksu līmenis pēc finanšu gada         | Faktisko izmaksu likme izmaksu uzvedību                                                                                             | Faktisko izmaksu likme vs budžeta izmaksu likme          |
|                                  | Faktisko izmaksu likme budžeta izmaksu likmju dispersija, budžeta izmaksu procentu likmi un budžeta izmaksu likme par izmaksu elementu hierarhijas līmeni | Faktisko apjomu vs budžeta apjoms          |
|                                  | Budžeta starpības izmaksu elementu hierarhijas līmeni                                                                               |                                               |
|                                  | Top 10 budžeta dispersijas procentus izmaksu elements                                                                          |                                               |
| Elastīgo budžetu ar fiskālo periodu | Faktiskās izmaksas, budžeta izmaksas un elastīgu budžetu izmaksas pa izmaksu elementu hierarhijas līmenī                                             | Faktisko apjomu vs budžeta apjoms          |
|                                  | Budžeta dispersiju un elastīgu budžetu dispersijas izmaksu elementu hierarhijas līmeni                                                  | Faktiskās izmaksas vs elastīgās budžeta izmaksas           |
|                                  | Faktiskajām izmaksām, budžeta izmaksas un elastīgu izmaksas pa izmaksu uzvedību un izmaksu līmeņa elements hierarhijā                                  | Faktisko izmaksu likme vs elastīga budžeta izmaksu likme |
| Finanšu periodu izmaksu deklarācija  | Faktiskās izmaksas, izmaksu elements hierarhijas līmenim un izmaksas objekta dimensiju dalībnieka vārds                                             |                                               |
|                                  | Faktiskās izmaksas izmaksas objekta dimensiju dalībnieka vārds un izmaksu elementu dimensijas dalībnieka vārds                                       |                                               |

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
Dinamika 365 darbības datiem tiek izmantota atskaites lapas aizpildīšanai **izmaksu uzskaites analīze** BI enerģijas saturu. Šie dati tiek attēlots kā apkopojuma mērījumus, kas ir iestudētas entītiju krātuvē, kas ir Microsoft SQL datu bāzi, kas ir optimizēta analytics. Lai iegūtu papildinformāciju, skatiet [pārskats par strāvas BI integrācija ar entītiju veikalā](power-bi-integration-entity-store.md). Šādus galvenos apkopojuma mērījumus izmanto par saturu pamatu.

| Elements                  | Kopējais mērījumu | Datu avotu dinamiku 365 operācijām | Lauks     | apraksts                                   |
|-------------------------|---------------------------|---------------------------------------------|-----------|-----------------------------------------------|
| Izmaksu uzskaites ierakstus | SUM(Amount)               | CAMDATAAggregatedCostEntry                  | Summa    | Summa valūtā izmaksu uzskaites Virsgrāmatas |
| Statistikas ieraksti     | SUM(Magnitude)            | CAMDATAAggregatedStatisctialEntry           | Lielums |                                               |

Tabulā ir parādīts, kā galveno apkopoto mērījumus izmanto, lai izveidotu vairākas aprēķinātie līdzekļi satura dataset.

| Mērs                                       | Kā pasākums tiek aprēķināta                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Faktiskās izmaksas                                   | APRĒĶINĀT ('izmaksu uzskaites ierakstus'\[pasākuma\], "Darījuma versijas"\[ISSOURCEVERSIONBUDGET\_vērtību\] = 0)            |
| Budžeta izmaksas                                   | APRĒĶINĀT ('izmaksu uzskaites ierakstus'\[pasākuma\], "Darījuma versijas"\[ISSOURCEVERSIONBUDGET\_vērtību\] = 1)            |
| Budžets, izmaksu dispersijas                          | \[Budžeta izmaksu\] - \[faktiskās izmaksas\]                                                                                      |
| Budžeta dispersijas procentus                    | IF (\[budžeta izmaksu\] = 0, blank(), \[budžeta dispersijas\] / \[budžeta izmaksu\])                                                |
| Faktiskais apjoms                              | APRĒĶINĀT ('Statistikas ieraksti'\[FullMagnitude\], "Darījuma versijas"\[ISSOURCEVERSIONBUDGET\_vērtību\] = 0)          |
| Budžeta apjoms                              | APRĒĶINĀT (\[FullMagnitude\], "Darījuma versijas"\[ISSOURCEVERSIONBUDGET\_vērtību\] = 1)                               |
| Budžetu statistisko dispersiju                   | \[Budžeta apjoms\] - \[faktiskais apjoms\]                                                                            |
| Budžeta statistikas dispersijas procentus        | IF (\[budžeta apjoms\] = 0, blank(), \[budžetu statistisko dispersiju\] / \[budžeta apjoms\])                          |
| Faktiskā izmaksu likme                              | IF (\[faktiskais apjoms\] = 0, BLANK(), \[faktisko izmaksu\] / \[faktiskais apjoms\])                                          |
| Budžeta izmaksu likme                              | IF (\[budžeta apjoms\] = 0, BLANK(), \[budžeta izmaksu\] / \[budžeta apjoms\])                                          |
| Budžeta izmaksu likmju dispersija                     | \[Budžeta izmaksu likme\] - \[faktisko izmaksu likme\]                                                                            |
| Budžets, izmaksu dispersijas procentu likmi          | IF (\[budžeta izmaksu\] = 0, blank(), \[budžeta izmaksu likmju dispersija\] / \[budžeta izmaksu likme\])                                 |
| Fiksēts budžeta izmaksas                             | APRĒĶINĀT (\[budžeta izmaksu\], 'Izmaksu grāmatvedības ieraksti'\[COSTBEHAVIOR\] = 1)                                              |
| Mainīgs budžeta izmaksas                          | APRĒĶINĀT (\[budžeta izmaksu\], 'Izmaksu grāmatvedības ieraksti'\[COSTBEHAVIOR\] = 2)                                              |
| Noteikta elastīga budžeta izmaksas                    | \[Fiksēts budžeta izmaksas\]                                                                                                  |
| Elastīgi mainīgo budžeta izmaksas                 | IF (\[budžeta apjoms\] = 0, BLANK(), (\[mainīgs budžeta izmaksu\] / \[budžeta apjoms\]) \*\[faktiskais apjoms\])       |
| Elastīgās budžeta izmaksas                          | \[Noteikta elastīga budžeta izmaksu\] + \[elastīgi mainīgo budžeta izmaksas\]                                                     |
| Elastīgā budžeta dispersija                      | \[Elastīgās budžeta izmaksas\] - \[faktiskās izmaksas\]                                                                             |
| Elastīgā budžeta dispersijas procentus           | IF (\[elastīgās budžeta izmaksas\] = 0, BLANK(), \[elastīgo budžetu dispersijas\] / \[elastīgās budžeta izmaksas\])                     |
| Elastīgā budžeta izmaksu likme                     | IF (\[faktiskais apjoms\] = 0, BLANK(), \[elastīgās budžeta izmaksas\] / \[faktiskais apjoms\])                                 |
| Elastīga budžeta izmaksu likmju dispersija            | \[Elastīgā budžeta izmaksu likme\] - \[faktisko izmaksu likme\]                                                                   |
| Elastīgā budžeta izmaksu procentu likmi dispersija | IF (\[elastīga budžeta izmaksu likme\] = 0, BLANK(), \[elastīga budžeta izmaksu likmju dispersija\] / \[elastīga budžeta izmaksu likme\]) |

Šādi galvenie izmēri tiek izmantoti kā filtri, šķēle apkopojuma mērījumus, lai panāktu lielāku detalizācijas un nodrošinātu dziļāku analītisku ieskatu.

| Elements                             | Atribūtu piemēri                                                                                               |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Izmaksu uzskaites virsgrāmatas            | Izmaksu uzskaites virsgrāmata                                                                                               |
| Izmaksu vadības ierīces                 | Izmaksu vadības ierīces nosaukums                                                                                               |
| Izmaksu elementu dimensijas            | Izmaksu elementi dimensijas nosaukums, izmaksu elementu dimensijas dalībnieka vārds, izmaksu elementu dimensijas dalībvalstis aprakstu          |
| Izmaksu objekta dimensijas             | Izmaksas objekta dimensijas nosaukums, izmaksas objekta dimensiju dalībnieka vārds, izmaksas objekta dimensiju dalībvalstu apraksts              |
| Statiskās dimensijas             | Statistikas dimensijas nosaukums, statistikas dimensiju dalībnieka vārds, statistikas dimensiju dalībvalstu apraksts              |
| Izmaksas objekta dimensiju hierarhijas  | Izmaksas objekta dimensiju hierarhijā nosaukums, izmaksas objekta dimensiju hierarhijas līmenī, izmaksas objekta dimensiju hierarhijas koks    |
| Izmaksu elementu dimensiju hierarhijas | Izmaksu elementu dimensiju hierarhijas vārdu, izmaksu elementu dimensiju hierarhijas līmenī, izmaksu elementu dimensiju hierarhijas koks |
| Statistikas dimensiju hierarhijas  | Statistikas dimensiju hierarhijas vārdu, statistikas dimensiju hierarhijas līmenī, statistikas dimensiju hierarhijas koks    |
| Transakcijas versijas               | Versijas nosaukums                                                                                                         |
| Finanšu kalendāri                   | Kalendārs, Kalendārs apraksta                                                                                       |
| Finanšu gadu                       | Kalendārais gads                                                                                                        |
| Finanšu periodi                     | Kalendārā gada laikā                                                                                                 |

## <a name="additional-resources"></a>Papildu resursi
Šeit norādītas dažas noderīgas saites, kas ir saistītas ar elementiem un Power BI satura izveidi:

-   [Datu elementi](..\data-entities\data-entities.md)
-   [Organizācijas satura pakotnes izveide](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datu modelēšana, izmantojot Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI elementu pievienošana darbvietām](configure-power-bi-integration.md)
-   [Izmaksu uzskaites satura drošības uzstādīšana Power BI](setup-security-cost-accounting-content-pack.md)


