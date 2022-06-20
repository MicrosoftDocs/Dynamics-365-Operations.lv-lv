---
title: Power BI satura pakotne Izmaksu pārvaldība
description: Šajā rakstā ir aprakstīts, kas ir iekļauts Izmaksu pārvaldības Power BI saturā.
author: ShylaThompson
ms.date: 03/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, CostObjectWithLowestAccuracy, CostVarianceChart, CostObjectWithLowestTurn
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 98c0097c2df25bafc842c9828d8ff282f5f683a5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876868"
---
# <a name="cost-management-power-bi-content"></a>Power BI satura pakotne Izmaksu pārvaldība

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Pārskats

**Izmaksu pārvaldības** Microsoft Power BI saturs ir paredzēts krājuma grāmatvežiem vai organizācijas indivīdiem, kuri atbild par vai ir ieinteresēti krājuma stāvoklī vai darba progresā (WIP), vai kuri atbild par vai ir ieinteresēti standarta izmaksu variāciju analīzē.

Šī Power BI satura pakotne nodrošina kategorizētu formātu, kas palīdz uzraudzīt krājumu veiktspēju un vizualizēt izmaksu plūsmu caur tiem. Varat gūt vadības ieskatus, piemēram, par apgrozījuma koeficientu, dienu skaitu, kurā krājumi ir pieejami, precizitāti un “ABC klasifikāciju” jūsu izvēlētajā uzkrātajā līmenī (uzņēmums, krājums, krājumu grupa vai vieta). Informāciju, kas ir pieejama, var arī izmantot kā finanšu pārskata detalizētu papildinājumu.

Power BI satura pakotne ir veidota, pamatojoties uz apkopoto mērījumu **CostObjectStatementCacheMonthly**, kura galvenais datu avots ir tabula **CostObjectStatementCache**. Šo tabulu pārvalda datu kopas kešatmiņas struktūra. Pēc noklusējuma šī tabula tiek atjaunināta ik pēc 24 stundām, bet datu kopas kešatmiņas konfigurācijā varat mainīt atjaunināšanas biežumu vai iespējot manuālu atjaunināšanu. Manuālo atjaunināšanu var palaist darbvietā **Izmaksu administrēšana** vai darbvietā **Izmaksu analīze**.

Ikreiz, kad tiek atjaunināta tabula **CostObjectStatementCache**, ir jāatjaunina apkopotais mērījums **CostObjectStatementCacheMonthly**, un tikai pēc tam drīkst atjaunināt Power BI vizualizācijās ietvertos datus.

## <a name="accessing-the-power-bi-content"></a>Piekļuve Power BI satura pakotnei

Power BI satura pakotne **Izmaksu pārvaldība** tiek rādīta darbvietās **Izmaksu administrēšana** un **Izmaksu analīze**.

Darbvietā **Izmaksu administrēšana** ir šādas cilnes:

- **Apskats** – šajā cilnē ir parādīti pieteikumu dati.
- **Krājumu uzskaites statuss** – šajā cilnē ir parādīts Power BI saturs.
- **Ražošanas uzskaites statuss** – šajā cilnē ir parādīts Power BI saturs.

Darbvietā **Izmaksu analīze** ir šādas cilnes:

- **Apskats** – šajā cilnē ir parādīti pieteikumu dati.
- **Krājumu uzskaites analīze** – šajā cilnē ir parādīts Power BI saturs.
- **Ražošanas uzskaites analīze** – šajā cilnē ir parādīts Power BI saturs.
- **Standarta izmaksu novirzes analīze** – šajā cilnē ir parādīts Power BI saturs.

## <a name="report-pages-that-are-included-in-the-power-bi-content"></a>Power BI satura pakotnē iekļautās pārskatu lapas

Power BI satura pakotnē **Izmaksu pārvaldība** ir ietvertas vairākas pārskatu lapas, kurās ir iekļauta rādītāju kopa. Šie rādītāji tiek vizualizēti kā diagrammas, elementi un tabulas. 

Tālāk esošajās tabulās ir sniegts apskats par vizualizācijām Power BI satura pakotnē **Izmaksu pārvaldība**.

### <a name="inventory-accounting-status"></a>Krājumu uzskaites statuss

| Pārskata lapa                               | Vizualizēšana                                   |
|-------------------------------------------|-------------------------------------------------|
| Krājumu apskats                        | Sākuma bilance                               |
|                                           | Neto apgrozījums                                      |
|                                           | Neto izmaiņas %                                    |
|                                           | Beigu bilance                                  |
|                                           | Krājumu precizitāte                              |
|                                           | Krājumu apgrozījuma koeficients                        |
|                                           | Dienas, kad pieejami krājumi                          |
|                                           | Aktīvā prece periodā                        |
|                                           | Aktīvo izmaksu objekti periodā                   |
|                                           | Bilance pēc krājumu grupas                           |
|                                           | Bilance pēc vietas                                 |
|                                           | Pārskats pēc kategorijas                           |
|                                           | Neto izmaiņas pēc ceturkšņa                           |
| Krājumu apskats pēc vietas un krājumu grupas | Krājumu precizitāte pēc vietas                      |
|                                           | Krājumu apgrozījuma koeficients pēc vietas                |
|                                           | Krājumu beigu bilance pēc vietas                |
|                                           | Krājumu precizitāte pēc krājumu grupas                |
|                                           | Krājumu apgrozījuma koeficients pēc krājumu grupas          |
|                                           | Krājumu beigu bilance pēc vietas un krājumu grupas |
| Inventarizācijas akts                       | Inventarizācijas akts                             |
| Inventarizācijas akts pēc vietas               | Inventarizācijas akts pēc vietas                     |
| Inventarizācijas akts pēc preču hierarhijas  | Inventarizācijas akts                             |
| Inventarizācijas akts pēc preču hierarhijas  | Inventarizācijas akts pēc vietas                     |

### <a name="manufacturing-accounting-status"></a>Ražošanas uzskaites statuss

| Pārskata lapa                | Vizualizēšana                       |
|----------------------------|-------------------------------------|
| NP apskats ŠG           | Sākuma bilance                   |
|                            | Neto apgrozījums                          |
|                            | Neto izmaiņas %                        |
|                            | Beigu bilance                      |
|                            | NP apgrozījuma koeficients                  |
|                            | Dienas, kad pieejama NP                    |
|                            | Aktīvo izmaksu objekts periodā        |
|                            | Neto izmaiņas pēc resursu grupas        |
|                            | Bilance pēc vietas                     |
|                            | Pārskats pēc kategorijas               |
|                            | Neto izmaiņas pēc ceturkšņa               |
| NP pārskats              | Sākuma bilance                   |
|                            | Beigu bilance                      |
|                            | NP pārskats pēc kategorijas           |
| NP pārskats pēc vietas      | Sākuma bilance                   |
|                            | Beigu bilance                      |
|                            | NP pārskats pēc kategorijas un vietas  |
| NP pārskats pēc hierarhijas | Sākuma bilance                   |
|                            | Beigu bilance                      |
|                            | NP pārskats pēc kategoriju hierarhijas |

### <a name="inventory-accounting-analysis"></a>Krājumu uzskaites analīze

| Pārskata lapa        | Vizualizēšana                                                                |
|--------------------|------------------------------------------------------------------------------|
| Detalizēta krājuma informācija  | Pirmie 10 resursi pēc beigu bilances                                           |
|                    | Pirmie 10 resursi pēc neto izmaiņu pieauguma                                      |
|                    | Pirmie 10 resursi pēc neto izmaiņu samazinājuma                                      |
|                    | Pirmie 10 resursi pēc krājumu apgrozījuma koeficienta                                 |
|                    | Resursi pēc zema krājumu apgrozījuma koeficienta un beigu bilances virs sliekšņa |
|                    | Pirmie 10 resursi pēc zemas precizitātes                                             |
| ABC klasifikācija | Krājumu beigu bilance                                                     |
|                    | Patērētais materiāls                                                            |
|                    | Pārdots (PPPI)                                                                  |
| Krājumu tendences   | Krājumu beigu bilance                                                     |
|                    | Krājumu neto izmaiņas                                                         |
|                    | Krājumu apgrozījuma koeficients                                                     |
|                    | Krājumu precizitāte                                                           |

### <a name="manufacturing-accounting-analysis"></a>Ražošanas uzskaites analīze

| Pārskata lapa | Vizualizēšana      |
|-------------|--------------------|
| NP tendences  | NP beigu bilance |
|             | NP neto izmaiņas     |
|             | NP apgrozījuma koeficients |

### <a name="std-cost-variance-analysis"></a>Standarta izmaksu novirzes analīze

| Pārskata lapa                             | Vizualizēšana                                        |
|-----------------------------------------|------------------------------------------------------|
| Pirkšanas cenas novirze (standarta izmaksas) ŠG | Sagādāto krājumu bilance                                     |
|                                         | Pirkšanas cenas novirze                              |
|                                         | Pirkšanas cenas novirzes koeficients                        |
|                                         | Novirze pēc krājumu grupas                               |
|                                         | Novirze pēc vietas                                     |
|                                         | Pirkšanas cena pēc ceturkšņa                            |
|                                         | Pirkšanas cena pēc ceturkšņa un krājumu grupas             |
|                                         | Pirmie 10 resursi pēc nelabvēlīga pirkšanas cenas koeficienta |
|                                         | Pirmie 10 resursi pēc labvēlīga pirkšanas cenas koeficienta   |
| Ražošanas novirze (standarta izmaksas) ŠG     | Ražošanas izmaksas                                    |
|                                         | Ražošanas novirze                                  |
|                                         | Ražošanas novirzes koeficients                            |
|                                         | Novirze pēc krājumu grupas                               |
|                                         | Novirze pēc vietas                                     |
|                                         | Ražošanas novirze pēc ceturkšņa                       |
|                                         | Ražošanas novirze pēc ceturkšņa un novirzes tipa     |
|                                         | Pirmie 10 resursi pēc nelabvēlīgas ražošanas novirzes  |
|                                         | Pirmie 10 resursi pēc labvēlīgas ražošanas novirzes    |

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana

Programmas dati tiek izmantoti, lai aizpildītu pārskatu lapas **Izmaksu pārvaldības** Power BI satura pakotnē. Šie dati tiek parādīti kā apkopoti mērījumi, kuri ir pieejami elementu krātuvē, kas ir analīzes veikšanai optimizēta Microsoft SQL Server datu bāze. Papildinformāciju skatiet rakstā [Power BI integrācija elementu krātuvē](power-bi-integration-entity-store.md).

Power BI satura pakotnes izveidei tiek izmantoto tālāk norādīto objektu galvenie apkopotie mērījumi.

| Objekts                          | Galvenie apkopošanas mērījumi | Dynamics 365 for Finance and Operations datu avots | Lauks               |
|---------------------------------|----------------------------|----------------------------------------|---------------------|
| CostObjectStatementCacheMonthly | Daudzums                     | CostObjectStatementCache               | Daudzums              |
| CostObjectStatementCacheMonthly | Daudzums                   | CostObjectStatementCache               | Daudzums                 |
| CostInventoryAccountingKPIGoal  | AnnualInventoryTurn        | CostInventoryAccountingKPIGoal         | AnnualInventoryTurn |
| CostInventoryAccountingKPIGoal  | InventoryAccuracy          | CostInventoryAccountingKPIGoal         | InventoryAccuracy   |

Tālāk esošajā tabulā ir norādīti galvenie aprēķinātie mērījumi Power BI satura pakotnē.

| Mērs                            | Aprēķins |
|------------------------------------|-------------|
| Sākuma bilance                  | Sākuma bilance = \[Beigu bilance\]-\[Neto izmaiņas\] |
| Sākuma bilances daudzums             | Sākuma bilances daudzums = \[Beigu bilance daudzums\]-\[Neto izmaiņu daudzums\] |
| Beigu bilance                     | Beigu bilance = (CALCULATE(SUM(\[Amount\]), FILTER(ALL(FiscalCalendar) ,FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\])))) |
| Beigu bilances daudzums                | Beigu bilances daudzums = CALCULATE(SUM(\[QTY\]), FILTER(ALL(FiscalCalendar),FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\]))) |
| Neto apgrozījums                         | Neto izmaiņas = SUM(\[AMOUNT\]) |
| Neto izmaiņu daudzums                    | Neto izmaiņu daudzums = SUM(\[QTY\]) |
| Krājumu apgrozījuma koeficients pēc summas | Krājumu apgrozījuma koeficients pēc summas = if(OR(\[Krājumu vidējā bilance\] \<= 0, \[Inventory sold or consumed issues\] \>= 0), 0, ABS(\[Pārdoto vai patērēto krājumu izejošās plūsmas\])/\[Krājumu vidējā bilance\]) |
| Krājumu vidējā bilance          | Krājumu vidējā bilance = ((\[Beigu bilance\] + \[Sākuma bilance\]) / 2) |
| Dienas, kad pieejami krājumi             | Dienas, kad pieejami krājumi = 365 / CostObjectStatementEntries\[Krājumu apgrozījuma koeficients pēc summas\] |
| Krājumu precizitāte                 | Krājumu precizitāte pēc summas = IF (\[Beigu bilance\] \<= 0, IF(OR(\[Inventory counted amount\] \<\> 0, \[Beigu bilance\] \< 0), 0, 1), MAX(0, (\[Beigu bilance\] - ABS(\[Krājumu skaita summa\]))/\[Beigu bilance\])) |

Tālāk minētās galvenās dimensijas tiek izmantotas kā filtri, lai sadalītu apkopošanas mērījumus, iegūstot lielāku granularitāti un sniedzot dziļākus analītiskos ieskatus.


| Elements                                                  | Atribūtu piemēri                          |
|---------------------------------------------------------|-------------------------------------------------|
| Preces                                                | Preces numurs, Preces nosaukums, Vienība, Krājumu grupas |
| Kategoriju hierarhijas (piešķirtas lomai Izmaksu pārvaldība) | Kategoriju hierarhija, Kategorijas līmenis              |
| Juridiskas personas                                          | Juridisko personu nosaukumi                              |
| Finanšu kalendāri                                        | Finanšu kalendārs, Gads, Ceturksnis, Periods, Mēnesis   |
| Atrašanās vieta                                                    | ID, Nosaukums, Adrese, Rajons, Valsts               |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
