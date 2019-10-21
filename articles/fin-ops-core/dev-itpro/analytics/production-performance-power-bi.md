---
title: Power BI satura pakotne Ražošanas veiktspēja
description: Šajā tēmā ir aprakstīts, kas ir iekļauts Power BI satura pakotnē Ražošanas veiktspēja. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī ir sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.
author: AndersGirke
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ProductionPerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9e2613a9adf60699a1c20b780e1acf2afb99d37d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182880"
---
# <a name="production-performance-power-bi-content"></a>Power BI satura pakotne Ražošanas veiktspēja

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kas ir iekļauts Microsoft Power BI satura pakotnē **Ražošanas veiktspēja**. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī ir sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.

## <a name="overview"></a>Pārskats

Power BI satura pakotne **Ražošanas veiktspēja** ir paredzēts ražošanas vadītājiem vai organizācijas darbiniekiem, kuri ir atbildīgi par ražošanas kontroli.

Iekļautie pārskati sniedz iespēju izmantot pakalpojumu Power BI, lai uzraudzītu ražošanas darbību veiktspēju attiecībā uz savlaicīgu izpildi, kvalitāti un izmaksām. Pārskatos tiek izmantoti transakciju dati no ražošanas pasūtījumiem un partijas pasūtījumiem, un tie nodrošina uzņēmuma ražošanas metrikas apkopojuma un metrikas sadalījuma pēc produkta un resursa skatus.

Power BI satura pakotne sniedz ieskatu par organizācijas spēju savlaicīgi un pilnībā izpildīt ražošanas procesus. Nākotnes veiktspēja tiek prognozēta, pamatojoties uz ražošanas plāniem. Visaptveroši pārskati sniedz detalizētu ieskatu par produktu brāķiem, ko izraisa ražošana, kā arī par brāķu proporcijām attiecībā uz resursiem un operācijām.

Šī Power BI satura pakotne sniedz arī iespēju analizēt ražošanas novirzes. Ražošanas novirzes tiek aprēķinātas kā novērtēto izmaksu un realizēto izmaksu starpība. Ražošanas novirzes tiek aprēķinātas, ja ražošanas pasūtījumiem vai partijas pasūtījumiem ir statuss **Pabeigts**.

Power BI satura pakotnē **Ražošanas veiktspēja** ir iekļauti dati no ražošanas pasūtījumiem un partijas pasūtījumiem. Pārskatos nav iekļauti dati, kas ir saistīti ar Kanban ražošanām.

## <a name="accessing-the-power-bi-content"></a>Piekļuve Power BI satura pakotnei
Power BI satura pakotne **Ražošanas veiktspēja** tiek rādīta lapā **Ražošanas veiktspēja** (**Ražošanas kontrole** \> **Pieprasījumi un pārskati** \> **Ražošanas veiktspējas analīze** \> **Ražošanas veiktspēja**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI satura pakotnē iekļautie rādītāji

Power BI satura pakotnē **Ražošanas veiktspēja** ir iekļauta pārskata lapu kopa. Katra lapa sastāv no rādītāju kopas, kuri ir vizualizēti kā diagrammas, elementi un tabulas.

Zemāk norādītajā tabulā ir sniegts pārskats par vizualizācijām, kas ir iekļautas.

| Pārskata lapa                                | Diagrammas | Elementi |
|--------------------------------------------|--------|-------|
| Ražošanas veiktspēja                     | <ul><li>Ražošanu skaits pēc datuma</li><li>Ražošanu skaits pēc preces un krājumu grupas</li><li>Plānoto ražošanu skaits pēc datuma</li><li>Apakšējās 10 preces pēc savlaicīgas un pilnīgas izpildes</li></ul> | <ul><li>Pasūtījumu kopskaits</li><li>Savlaicīgi un pilnībā %</li><li>Nepilnīgi, %</li><li>Pirms termiņa, %</li><li>Nokavēts termiņš, %</li></ul> |
| Brāķi pēc preces                         | <ul><li>Brāķa proporcija (miljonās daļas) pēc datuma</li><li>Brāķa proporcija (miljonās daļas) pēc preces un krājumu grupas</li><li>Saražotais daudzums pēc datuma</li><li>Pirmās 10 preces pēc faktiskās likmes</li></ul> | <ul><li>Brāķa proporcija (miljonās daļas)</li><li>Brāķa daudzums</li><li>Kopējais daudzums</li></ul> |
| Brāķa tendences pēc preces                   | Brāķa proporcija (miljonās daļas) pēc saražotā daudzuma | Brāķa proporcija (miljonās daļas) |
| Brāķi pēc resursa                        | <ul><li>Brāķa proporcija (miljonās daļas) pēc datuma</li><li>Brāķa proporcija (miljonās daļas) pēc resursa un vietas</li><li>Brāķa proporcija (miljonās daļas) pēc darbības</li><li>Pirmie 10 resursi pēc brāķa proporcijas</li></ul> | Brāķa daudzums |
| Brāķa tendences pēc resursa                  | Brāķa proporcija (miljonās daļas) pēc apstrādātā daudzuma | |
| Darba pasūtījuma cenas ražošanas novirzes | <ul><li>Ražošanas novirzes pēc datuma un izmaksu grupas veida</li><li>Ražošanas novirzes pēc vietas un izmaksu grupas veida</li><li>Pirmās 10 preces ar nelabvēlīgu ražošanas novirzi</li><li>Pirmās 10 preces ar nelabvēlīgu ražošanas novirzi pēc resursa</li></ul> | <ul><li>Realizētās izmaksas</li><li>Ražošanas novirze</li><li>Ražošanas novirze, %</li></ul> |


## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana

Power BI satura pakotnes **Ražošanas veiktspēja** pārskatu lapās tiek izmantoti tālāk norādītie dati. Šie dati tiek attēloti kā apkopoti mērījumi, kas tiek sagatavoti elementu krātuvē. Elementu krātuve ir analīzei optimizēta Microsoft SQL Server datu bāze. Papildinformāciju par elementu krātuvi skatiet rakstā [Power BI integrācija elementu krātuvē](power-bi-integration-entity-store.md).

Tālāk esošajā tabulā ir norādīti galvenie apkopošanas mērījumi, kas tiek izmantoti Power BI satura pakotnes izveidei.

| Elements                   | Galvenie apkopošanas mērījumi  | Finance and Operations programmu datu avots | Lauks              |
|--------------------------|-----------------------------|----------------------------------------|--------------------|
| CostCalculation          | CostAmount                  | ProdCalcTransExpanded                  | CostAmount         |
| CostCalculation          | CostMarkup                  | ProdCalcTransExpanded                  | CostMarkup         |
| CostCalculation          | ActualCostAmount            | ProdCalcTransExpanded                  | RealCostAmount     |
| CostCalculation          | RealCostAdjustment          | ProdCalcTransExpanded                  | RealCostAdjustment |
| RouteTransactions        | ErrorQuantity               | ProdRouteTransExpanded                 | QtyError           |
| RouteTransactions        | GoodQuantity                | ProdRouteTransExpanded                 | QtyGood            |
| ProductionOrder          | DaysDelayed                 | ProdTableExpanded                      | DaysDelayed        |
| ProductionOrder          | LeadTime                    | ProdTableExpanded                      | LeadTime           |
| ProductionOrder          | PlannedLeadTime             | ProdTableExpanded                      | PlannedLeadTime    |
| ProductionOrder          | ProductionOrderCount        | ProdTableExpanded                      |                    |
| CoproductCostCalculation | CoproductCostAmount         | PmfCoByProdCalcTransExpanded           | CostAmount         |
| CoproductCostCalculation | CoproductCostMarkup         | PmfCoByProdCalcTransExpanded           | CostMarkup         |
| CoproductCostCalculation | CoproductRealCostAdjustment | PmfCoByProdCalcTransExpanded           | RealCostAdjustment |
| CoproductCostCalculation | CoproductActualCostAmount   | PmfCoByProdCalcTransExpanded           | RealCostAmount     |

Nākamajā tabulā ir parādīts, kā galvenie apkopošanas mērījumi tiek izmantoti, lai satura datu kopā izveidotu vairākus aprēķinātos mērus.

| Mērs                  | Kā šis mērs tiek aprēķināts |
|--------------------------|-------------------------------|
| Ražošanas novirze, %   | SUM(Ražošanas novirze\[Ražošanas novirze\])/SUM(Ražošanas novirze\[Novērtētās izmaksas\]) |
| Visi plānotie pasūtījumi       | COUNTROWS(Plānotais ražošanas pasūtījums) |
| Agri                    | COUNTROWS (FILTER(Plānotais ražošanas pasūtījums, Plānotais ražošanas pasūtījums\[Plānotais beigu datums\] \< Plānotais ražošanas pasūtījums\[Vajadzības datums\])) |
| Vēlu                     | COUNTROWS (FILTER(Plānotais ražošanas pasūtījums, Plānotais ražošanas pasūtījums\[Plānotais beigu datums\] \> Plānotais ražošanas pasūtījums\[Vajadzības datums\])) |
| Savlaicīgi                  | COUNTROWS (FILTER(Plānotais ražošanas pasūtījums, Plānotais ražošanas pasūtījums\[Plānotais beigu datums\] = Plānotais ražošanas pasūtījums\[Vajadzības datums\])) |
| Savlaicīgi, %                | IF (Plānotais ražošanas pasūtījums\[Savlaicīgi\] \<\> 0, Plānotais ražošanas pasūtījums\[Savlaicīgi\], IF (Plānotais ražošanas pasūtījums\[Visi plānotie pasūtījumi\] \<\> 0, 0, BLANK()) ) / Plānotais ražošanas pasūtījums\[Visi plānotie pasūtījumi\] |
| Gatavs                | COUNTROWS(FILTER(Ražošanas pasūtījums, Ražošanas pasūtījums\[Ir RAF'ed\] = TRUE)) |
| Brāķa proporcija (miljonās daļas)     | IF(Ražošanas pasūtījums\[Kopējais daudzums\] = 0, BLANK(), (SUM(Ražošanas pasūtījums\[Brāķa daudzums\]) /Ražošanas pasūtījums\[Kopējais daudzums\]) \* 1000000) |
| Ražošanas proporcija ar nokavētu termiņu  | 'Ražošanas pasūtījums'\[Nokavēts termiņš \#\] /'Ražošanas pasūtījums'\[Pabeigts\] |
| Pirms termiņa un pilnībā          | COUNTROWS(FILTER(Ražošanas pasūtījums, Ražošanas pasūtījums\[Pilnībā\] = TRUE && Ražošanas pasūtījums'\[Pirms termiņa\] = TRUE)) |
| Pirms termiņa \#                 | COUNTROWS(FILTER(Ražošanas pasūtījums, Ražošanas pasūtījums\[Pirms termiņa\] = TRUE)) |
| Pirms termiņa, %                  | IFERROR( IF(Ražošanas pasūtījums\[Pirms termiņa \#\] \<\> 0, Ražošanas pasūtījums\[Pirms termiņa \#\], IF(Ražošanas pasūtījums\[Pasūtījumu kopskaits\] = 0, BLANK(), 0)) / Ražošanas pasūtījums\[Pasūtījumu kopskaits\], BLANK()) |
| Nepabeigts               | COUNTROWS(FILTER(Ražošanas pasūtījums, Ražošanas pasūtījums\[Pilnībā\] = FALSE && Ražošanas pasūtījums\[Ir RAF'ed\] = TRUE)) |
| Nepilnīgi, %             | IFERROR( IF(Ražošanas pasūtījums\[Nepilnīgs\] \<\> 0, Ražošanas pasūtījums\[Nepilnīgs\], IF(Ražošanas pasūtījums\[Pasūtījumu kopskaits\] = 0, BLANK(), 0)) / Ražošanas pasūtījums\[Pasūtījumu kopskaits\], BLANK()) |
| Nokavēts termiņš               | Ražošanas pasūtījums\[Ir RAF'ed\] = TRUE && Ražošanas pasūtījums\[Piegādātā vērtība\] = 1 |
| Pirms termiņa                 | Ražošanas pasūtījums\[Is RAF'ed\] = TRUE && Ražošanas pasūtījums\[Kavētās dienas\] \< 0 |
| Ir pilnībā               | Ražošanas pasūtījums\[Derīgais daudzums\] \>= Ražošanas pasūtījums\[Plānotais daudzums\] |
| Ir RAF'ed                | Ražošanas pasūtījums\[Ražošanas statusa vērtība\] = 5 \|\| Ražošanas pasūtījums\[Ražošanas statusa vērtība\] = 7 |
| Nokavēts termiņš un pilnībā           | COUNTROWS(FILTER(Ražošanas pasūtījums, Ražošanas pasūtījums\[Ir pilnībā\] = TRUE && Ražošanas pasūtījums\[Nokavēts termiņš\] = TRUE)) |
| Nokavēts termiņš \#                  | COUNTROWS(FILTER(Ražošanas pasūtījums, Ražošanas pasūtījums\[Nokavēts termiņš\] = TRUE)) |
| Nokavēts termiņš, %                   | IFERROR( IF(Ražošanas pasūtījums\[Nokavēts termiņš \#\] \<\> 0, Ražošanas pasūtījums\[Nokavēts termiņš \#\], IF(Ražošanas pasūtījums\[Pasūtījumu kopskaits\] = 0, BLANK(), 0)) / Ražošanas pasūtījums\[Pasūtījumu kopskaits\], BLANK()) |
| Savlaicīgi un pilnībā        | COUNTROWS(FILTER(Ražošanas pasūtījums, Ražošanas pasūtījums\[Pilnībā\] = TRUE && Ražošanas pasūtījums\[Nokavēts termiņš\] = FALSE && Ražošanas pasūtījums\[Pirms termiņa\] = FALSE)) |
| Savlaicīgi un pilnībā, %      | IFERROR( IF(Ražošanas pasūtījums\[Savlaicīgi un pilnībā\] \<\> 0, Ražošanas pasūtījums\[Savlaicīgi un pilnībā\], IF(Ražošanas pasūtījums\[Pabeigts\] = 0, BLANK(), 0)) / Ražošanas pasūtījums\[Pabeigts\], BLANK()) |
| Pasūtījumu kopskaits             | COUNTROWS(Ražošanas pasūtījums) |
| Kopējais daudzums           | SUM(Ražošanas pasūtījums\[Derīgais daudzums\]) + SUM(Ražošanas pasūtījums\[Brāķa daudzums\]) |
| Brāķa proporcija (miljonās daļas)        | IF(Maršruta darbības\[Apstrādātais daudzums\] = 0, BLANK(), (SUM(Maršruta darbības\[Brāķa daudzums\]) / Maršruta darbības\[Apstrādātais daudzums\]) \* 1000000) |
| Apvienotā brāķa proporcija (miljonās daļas) | IF(Maršruta darbības\[Kopējais apvienotais daudzums\] = 0, BLANK(), (SUM(Maršruta darbības\[Brāķa daudzums\]) / Maršruta darbības\[Kopējais apvienotais daudzums\])\* 1000000) |
| Apstrādātais daudzums       | SUM(Maršruta darbības\[Derīgais daudzums\]) + SUM(Maršruta darbības\[Brāķa daudzums\]) |
| Kopējais apkopotais daudzums     | SUM(Ražošanas pasūtījums\[Derīgais daudzums\]) + SUM(Maršruta darbības\[Brāķa daudzums\]) |

Sekojošajā tabulā ir norādītās galvenās dimensijas, kas tiek izmantotas kā filtri, lai sadalītu apkopošanas mērījumus, iegūstot lielāku granularitāti un sniedzot dziļākus analītiskos ieskatus.

| Elements                    | Atribūtu piemēri                                        |
|---------------------------|---------------------------------------------------------------|
| Pabeigšanas datums | Pabeigšanas (RAF) dienas, mēneša un gada nobīde                 |
| Beigu datums                | Pabeigšanas mēneša nobīde un mēnesis                                  |
| Vajadzības datums          | Vajadzības datuma mēneša nobīde un vajadzības datums            |
| Maršruta darbības datums    | Maršruta darbības mēneša nobīde un datums                       |
| Atrašanās vietas                     | Vietu ID, vietas nosaukums, valsts un pilsēta                          |
| Elementi                  | ID un nosaukums                                                   |
| Resursi                 | Resursa ID, resursa nosaukums, resursa veids un resursu grupa |
| Preces                  | Preces numurs, preces nosaukums, krājuma ID un krājumu grupa         |
