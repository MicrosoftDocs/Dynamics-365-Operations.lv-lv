---
title: "Power BI saturs Izmaksu uzskaites analīze"
description: "Šajā tēmā ir aprakstīts, kas ir iekļauts Power BI saturā Izmaksu uzskaites analīze. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: be4165f58b17bed0b0984b760fd8eea09267a251
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="cost-accounting-analysis-power-bi-content"></a>Power BI saturs Izmaksu uzskaites analīze

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīts, kas ir iekļauts Power BI saturā Izmaksu uzskaites analīze. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.

<a name="overview"></a>Pārskats
--------

Microsoft Power BI saturs **Izmaksu uzskaites analīze** ir paredzēts izmaksu kontrolierim vai ikvienam, kurš ir atbildīgs par organizācijas izmaksu kontroles veikšanu. Tā ietver galvenos rādītājus, piemēram, izmaksas, lielumu un izmaksu likmi pēc faktiskajām izmaksām, budžeta izmaksām un elastīgajām budžeta izmaksām. Tā lieto transakciju datus no izmaksu uzskaites programmā Microsoft Dynamics 365 for Operations un sniedz apkopotu skatu uz izmaksām visai organizācijai vienā pārskata valūtā. Vadītāji var datus filtrēt pēc izmaksu objektiem, lai veiktu savu organizatorisko vienību izmaksu kontroli pat tad, ja organizācijā ietilpst vairākas juridiskās personas. Tā kā Power BI saturs **Izmaksu uzskaites analīze** izceļ novirzes starp faktiskajām un budžetā paredzētajām izmaksām, vadītāji var tikt informēti par savu organizatorisko vienību pozitīvajām un negatīvajām tendencēm. Vadītāji var detalizēti skatīt informāciju līdz pat izmaksu elementu hierarhijām vai atsevišķiem izmaksu elementiem, lai gūtu detalizētu ieskatu par to, kā izmaksu novirzes ir radušās, un pēc tam efektīvi rīkoties. Power BI saturs **Izmaksu uzskaites analīze** grāmatvežiem ļauj analizēt veidu, kā izmaksas plūst caur visas organizācijas izmaksu objektiem. Lai uzzinātu papildinformāciju par izmaksu uzskaiti, skatiet [izmaksu uzskaites sākumlapu](/dynamics365/operations/financials/cost-accounting/cost-accounting-home-page). Izmaksu uzskaitē definējot piekļuves līmeņa drošību un to kombinējot ar rindas līmeņa drošību pakalpojumā Power BI, visiem izmaksu objektu īpašniekiem varat sniegt piekļuvi Power BI saturam **Izmaksu uzskaites analīze**. Pēc tam visi vizualizācijās esošie dati tiks filtrēti, pamatojoties uz piekļuves līmeni, kurš ir kontrolēts izmaksu uzskaitē. Lai uzzinātu papildinformāciju par piekļuves līmeņa drošību un rindas līmeņa drošību, skatiet rakstu [Iestatīt drošību Power BI saturam Izmaksu analīze](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Piekļūšana Power BI saturam
Power BI saturs **Izmaksu uzskaites analīze** ir atrodama Microsoft Dynamics Lifecycle Services (LCS) koplietojamo līdzekļu bibliotēkā. Papildinformāciju par to, kā lejupielādēt šo satura pakotni un to savienot ar saviem Dynamics 365 for Operations datiem, skatiet rakstā [Power BI saturs LCS no Microsoft un jūsu partneriem](power-bi-content-microsoft-partners.md). 

> PIEZĪME. **KB4011327** ir priekšnosacījums šim Power BI saturam. Kad esat pierakstījies pakalpojumos Lifecycle Services, tad KB varat piekļūt šeit: <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI saturā iekļautā metrika
Saturā ietilpst pārskatu lapu komplekts. Katra lapa sastāv no rādītāju kopas, kuri ir vizualizēti kā diagrammas, elementi un tabulas. Nākamajā tabulā ir sniegts apskats par vizualizācijām Power BI saturā **Izmaksu uzskaites analīze**.

| Pārskata lapa                      | Diagramma                                                                                                                         | Elements                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Izmaksu kontrole pēc finanšu perioda    | Faktiskās izmaksas un budžeta izmaksas pēc izmaksu elementu hierarhijas līmeņa                                                                   | Faktiskās izmaksas pret budžeta izmaksām                    |
|                                  | Budžeta novirze pēc izmaksu elementu hierarhijas līmeņa                                                                               | Faktisko izmaksu likme pret budžeta izmaksu likmi          |
|                                  | 10 galvenās budžeta novirzes procentos pēc izmaksu elementa                                                                          | Faktiskais lielums pret budžeta lielumu          |
| Izmaksu kontrole pēc līdzšinējā gada     | Faktiskās izmaksas un budžeta izmaksas pēc kalendārā gada perioda                                                                           | Faktiskās izmaksas pret budžeta izmaksām                    |
|                                  | Budžeta novirze pēc kalendārā gada perioda                                                                                       | Faktisko izmaksu likme pret budžeta izmaksu likmi          |
|                                  | 10 galvenās budžeta novirzes procentos pēc izmaksu elementa                                                                          | Faktiskais lielums pret budžeta lielumu          |
| Izmaksu likme pēc finanšu gada         | Faktisko izmaksu likme pēc izmaksu uzvedības                                                                                             | Faktisko izmaksu likme pret budžeta izmaksu likmi          |
|                                  | Faktisko izmaksu likme, budžeta izmaksu likmes novirze, budžeta izmaksu likmes procenti un budžeta izmaksu likme pēc izmaksu elementu hierarhijas līmeņa | Faktiskais lielums pret budžeta lielumu          |
|                                  | Budžeta novirze pēc izmaksu elementu hierarhijas līmeņa                                                                               |                                               |
|                                  | 10 galvenās budžeta novirzes procentos pēc izmaksu elementa                                                                          |                                               |
| Elastīgais budžets pēc finanšu perioda | Faktiskās izmaksas, budžeta izmaksas un elastīgās budžeta izmaksas pēc izmaksu elementu hierarhijas līmeņa                                             | Faktiskais lielums pret budžeta lielumu          |
|                                  | Budžeta novirze un elastīgā budžeta novirze pēc izmaksu elementu hierarhijas līmeņa                                                  | Faktiskās izmaksas pret elastīgajām budžeta izmaksām           |
|                                  | Faktiskās izmaksas, budžeta izmaksas un elastīgās budžeta izmaksas pēc izmaksu uzvedības un izmaksu elementu hierarhijas līmeņa                                  | Faktisko izmaksu likme pret elastīgā budžeta izmaksu likmi |
| Izmaksu pārskats pēc finanšu perioda  | Faktiskās izmaksas pēc izmaksu elementu hierarhijas līmeņa un izmaksu objekta dimensijas elementa nosaukuma                                             |                                               |
|                                  | Faktiskās izmaksas pēc izmaksu objekta dimensijas elementa nosaukuma un izmaksu elementa dimensijas elementa nosaukuma                                       |                                               |

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
Lai aizpildītu pārskatu lapas Power BI saturā **Izmaksu uzskaites analīze**, tiek lietoti Dynamics 365 for Operations dati. Šie dati tiek attēloti kā apkopoti mērījumi, kuri pa posmiem tiek izveidoti elementu krātuvē, kas ir analīzes veikšanai optimizēta Microsoft SQL datu bāze. Papildinformāciju skatiet tēmā [Apskats par Power BI integrāciju elementu krātuvē](power-bi-integration-entity-store.md). Kā satura pamats tiek izmantoti tālāk norādītie galvenie apkopošanas mērījumi.

| Elements                  | Galvenais apkopošanas mērījums | Datu avots programmai Dynamics 365 for Operations | Lauks     | Apraksts                                   |
|-------------------------|---------------------------|---------------------------------------------|-----------|-----------------------------------------------|
| Izmaksu uzskaites ieraksti | SUM(Summa)               | CAMDATAAggregatedCostEntry                  | Summa    | Summa izmaksu uzskaites virsgrāmatas valūtā |
| Statistikas ieraksti     | SUM(Lielums)            | CAMDATAAggregatedStatisctialEntry           | Lielums |                                               |

Nākamajā tabulā ir parādīts, kā galvenie apkopošanas mērījumi tiek izmantoti, lai satura datu kopā izveidotu vairākus aprēķinātos mērus.

| Mērs                                       | Kā šis mērs tiek aprēķināts                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Faktiskās izmaksas                                   | CALCULATE(“Izmaksu uzskaites ieraksti”\[Mērs\], “Transakciju versijas”\[ISSOURCEVERSIONBUDGET\_VALUE\] = 0)            |
| Budžeta izmaksas                                   | CALCULATE(“Izmaksu uzskaites ieraksti”\[Mērs\], “Transakciju versijas”\[ISSOURCEVERSIONBUDGET\_VALUE\] = 1)            |
| Budžeta izmaksu novirze                          | \[Budžeta izmaksas\] - \[Faktiskās izmaksas\]                                                                                      |
| Budžeta novirze procentos                    | IF(\[Budžeta izmaksas\] = 0, blank(), \[Budžeta novirze\] / \[Budžeta izmaksas\])                                                |
| Faktiskais lielums                              | CALCULATE(“Statistikas ieraksti”\[FullMagnitude\], “Transakciju versijas”\[ISSOURCEVERSIONBUDGET\_VALUE\] = 0)          |
| Budžeta lielums                              | CALCULATE(\[FullMagnitude\], “Transakciju versijas”\[ISSOURCEVERSIONBUDGET\_VALUE\] = 1)                               |
| Statistiskā budžeta novirze                   | \[Budžeta lielums\] - \[Faktiskais lielums\]                                                                            |
| Statistiskā budžeta novirze procentos        | IF(\[Budžeta lielums\] = 0, blank(), \[Statistiskā budžeta novirze\] / \[Budžeta lielums\])                          |
| Faktiskā izmaksu likme                              | IF(\[Faktiskais lielums\] = 0, BLANK(), \[Faktiskās izmaksas\] / \[Faktiskais lielums\])                                          |
| Budžeta izmaksu likme                              | IF(\[Budžeta lielums\] = 0, BLANK(), \[Budžeta izmaksas\] / \[Budžeta lielums\])                                          |
| Budžeta izmaksu likmes novirze                     | \[Budžeta izmaksu likme\] - \[Faktisko izmaksu likme\]                                                                            |
| Budžeta izmaksu likmes novirze procentos          | IF(\[Budžeta izmaksas\] = 0, blank(), \[Budžeta izmaksu likmes novirze\] / \[Budžeta izmaksu likme\])                                 |
| Fiksētas budžeta izmaksas                             | CALCULATE(\[Budžeta izmaksas\], “Izmaksu uzskaites ieraksti”\[COSTBEHAVIOR\] = 1)                                              |
| Mainīgās budžeta izmaksas                          | CALCULATE(\[Budžeta izmaksas\], “Izmaksu uzskaites ieraksti”\[COSTBEHAVIOR\] = 2)                                              |
| Fiksētas elastīgā budžeta izmaksas                    | \[Fiksētās budžeta izmaksas\]                                                                                                  |
| Mainīgās elastīgā budžeta izmaksas                 | IF(\[Budžeta lielums\] = 0, BLANK(), (\[Mainīgās budžeta izmaksas\] / \[Budžeta lielums\]) \* \[Faktiskais lielums\])       |
| Elastīgā budžeta izmaksas                          | \[Fiksētās elastīgā budžeta izmaksas\] + \[Mainīgās elastīgā budžeta izmaksas\]                                                     |
| Elastīgā budžeta novirze                      | \[Elastīgā budžeta izmaksas\] - \[Faktiskās izmaksas\]                                                                             |
| Elastīgā budžeta novirze procentos           | IF(\[Elastīgā budžeta izmaksas\] = 0, BLANK(), \[Elastīgā budžeta novirze\] / \[Elastīgā budžeta izmaksas\])                     |
| Elastīgā budžeta izmaksu likme                     | IF(\[Faktiskais lielums\] = 0, BLANK(), \[Elastīgā budžeta izmaksas\] / \[Faktiskais lielums\])                                 |
| Elastīgā budžeta izmaksu likmes novirze            | \[Elastīgā budžeta izmaksu likme\] - \[Faktisko izmaksu likme\]                                                                   |
| Elastīgā budžeta izmaksu likmes novirze procentos | IF(\[Elastīgā budžeta izmaksu likme\] = 0, BLANK(), \[Elastīgā budžeta izmaksu likmes novirze\] / \[Elastīgā budžeta izmaksu likme\]) |

Tālāk norādītās galvenās dimensijas tiek lietotas kā filtri, lai apkopošanas mērījumus sadalītu, iegūstot lielāku granularitāti un sniedzot dziļākus analītiskos ieskatus.

| Elements                             | Atribūtu piemēri                                                                                               |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Izmaksu uzskaites virsgrāmatas            | Izmaksu uzskaites virsgrāmata                                                                                               |
| Izmaksu vadības ierīces                 | Izmaksu vadības ierīces nosaukums                                                                                               |
| Izmaksu elementu dimensijas            | Izmaksu elementa dimensijas nosaukums, izmaksu elementa dimensijas elementa nosaukums, izmaksu elementa dimensijas elementa apraksts          |
| Izmaksu objekta dimensijas             | Izmaksu objekta dimensijas nosaukums, izmaksu objekta dimensijas elementa nosaukums, izmaksu objekta dimensijas elementa apraksts              |
| Statiskās dimensijas             | Statistiskās dimensijas nosaukums, statistiskās dimensijas elementa nosaukums, statistiskās dimensijas elementa apraksts              |
| Izmaksu objektu dimensiju hierarhijas  | Izmaksu objekta dimensiju hierarhijas nosaukums, izmaksu objekta dimensiju hierarhijas līmenis, izmaksu objekta dimensiju hierarhiju koks    |
| Izmaksu elementu dimensiju hierarhijas | Izmaksu elementa dimensiju hierarhijas nosaukums, izmaksu elementa dimensiju hierarhijas līmenis, izmaksu elementa dimensiju hierarhiju koks |
| Statistisko dimensiju hierarhijas  | Statistisko dimensiju hierarhijas nosaukums, statistisko dimensiju hierarhijas līmenis, statistisko dimensiju hierarhiju koks    |
| Transakcijas versijas               | Versijas nosaukums                                                                                                         |
| Finanšu kalendāri                   | Kalendārs, Kalendāra apraksts                                                                                       |
| Finanšu gadi                       | Kalendārais gads                                                                                                        |
| Finanšu periodi                     | Kalendārā gada periods                                                                                                 |

## <a name="additional-resources"></a>Papildu resursi
Šeit norādītas dažas noderīgas saites, kas ir saistītas ar elementiem un Power BI satura izveidi:

-   [Datu elementi](..\data-entities\data-entities.md)
-   [Organizācijas satura pakotnes izveide](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datu modelēšana, izmantojot Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI elementu pievienošana darbvietām](configure-power-bi-integration.md)
-   [Drošības iestatīšana Power BI saturam Izmaksu uzskaite](setup-security-cost-accounting-content-pack.md)




