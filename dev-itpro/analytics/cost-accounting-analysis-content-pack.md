---
title: "Power BI saturs Izmaksu uzskaites analīze"
description: "Šajā tēmā ir aprakstīts, kas ir iekļauts Power BI saturā Izmaksu uzskaites analīze. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem."
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 1d19276331a4278f44ad14292ed434c49b74d727
ms.contentlocale: lv-lv
ms.lasthandoff: 06/13/2017

---

# <a name="cost-accounting-analysis-power-bi-content"></a>Power BI saturs Izmaksu uzskaites analīze

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kas ir iekļauts Microsoft Power BI satura pakotnē **Izmaksu uzskaites analīze**. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.

## <a name="overview"></a>Pārskats

Power BI satura pakotne **Izmaksu uzskaites analīze** ir paredzēta izmaksu kontrolieriem vai jebkurai personai, kura ir atbildīga par organizācijas izmaksu kontroles veikšanu. Tā ietver galvenos rādītājus, piemēram, izmaksas, lielumu un izmaksu likmi pēc faktiskajām izmaksām, budžeta izmaksām un elastīgajām budžeta izmaksām. Šajā satura pakotnē tiek izmantoti transakciju dati no moduļa **Izmaksu uzskaite**, un tā nodrošina apkopotu informāciju par izmaksām visas organizācijas ietvaros vienā pārskata valūtā. Vadītāji var datus filtrēt pēc izmaksu objektiem, lai veiktu savu organizatorisko vienību izmaksu kontroli pat tad, ja organizācijā ietilpst vairākas juridiskās personas. 

Tā kā satura pakotne **Izmaksu uzskaites analīze** izceļ novirzes starp faktiskajām un budžetā paredzētajām izmaksām, vadītāji var tikt informēti par savu organizatorisko vienību vēlamajām un nevēlamajām tendencēm. Vadītāji var skatīt detalizētu informāciju par izmaksu elementu hierarhijām vai atsevišķiem izmaksu elementiem. Tādējādi vadītāji var gūt detalizētu ieskatu par izmaksu nobīdes iemesliem un pēc tam efektīvi rīkoties. 

Satura pakotne **Izmaksu uzskaites analīze** sniedz grāmatvežiem iespēju analizēt izmaksu plūsmu caur izmaksu objektiem visas organizācijas ietvaros. 

Lai uzzinātu papildinformāciju par izmaksu uzskaiti, skatiet [izmaksu uzskaites sākumlapu](/dynamics365/unified-operations/financials/cost-accounting/cost-accounting-home-page). 

Izmaksu uzskaitē definējot piekļuves līmeņa drošību un to kombinējot ar rindas līmeņa drošību pakalpojumā Power BI, visiem izmaksu objektu īpašniekiem varat sniegt piekļuvi Power BI saturam **Izmaksu uzskaites analīze**. Pēc tam visi vizualizācijās esošie dati tiks filtrēti, pamatojoties uz piekļuves līmeni, kurš ir kontrolēts izmaksu uzskaitē. Lai uzzinātu papildinformāciju par piekļuves līmeņa drošību un rindas līmeņa drošību, skatiet rakstu [Iestatīt drošību Power BI saturam Izmaksu analīze](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Piekļūšana Power BI saturam
Power BI saturs **Izmaksu uzskaites analīze** ir atrodama Microsoft Dynamics Lifecycle Services (LCS) koplietojamo līdzekļu bibliotēkā. Papildinformāciju par to, kā lejupielādēt satura pakotni un ieviest to savā organizācijā, skatiet tēmā [Power BI saturs pakalpojumā LCS no Microsoft un jūsu partneriem](power-bi-content-microsoft-partners.md). Power BI satura pakotnes implementēšanas demonstrāciju skatiet tēmā [Power BI saturs pakalpojumā Dynamics Lifecycle Services no Microsoft un jūsu partneriem](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

Noteikti lejupielādējiet satura pakotni **Izmaksu uzskaites analīze**, kas ir paredzēta jūsu Microsoft Dynamics 365 versijai.

> [!NOTE]
> KB 4011327 ir viens no šīs Power BI satura pakotnes izmantošanas priekšnoteikumiem. Pēc pierakstīšanās pakalpojumā LCS varat piekļūt KB šeit: <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

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
Power BI satura pakotnes **Izmaksu uzskaites analīze** pārskatu lapu aizpildīšanai tiek izmantoti tālāk norādītie dati. Šie dati tiek attēloti kā apkopoti mērījumi, kas tiek sagatavoti elementu krātuvē. Elementu krātuve ir analīzei optimizēta Microsoft SQL Server datu bāze. Papildinformāciju skatiet tēmā [Apskats par Power BI integrāciju elementu krātuvē](power-bi-integration-entity-store.md). 

Kā satura pamats tiek izmantoti tālāk norādītie galvenie apkopošanas mērījumi.

| Elements                  | Galvenais apkopošanas mērījums | Dynamics 365 datu avots      | Lauks     | apraksts                                        |
|-------------------------|---------------------------|-----------------------------------|-----------|----------------------------------------------------|
| Izmaksu uzskaites ieraksti | SUM(Summa)               | CAMDATAAggregatedCostEntry        | Summa    | Summa izmaksu uzskaites virsgrāmatas valūtā. |
| Statistikas ieraksti     | SUM(Lielums)            | CAMDATAAggregatedStatisctialEntry | Lielums |                                                    |

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

