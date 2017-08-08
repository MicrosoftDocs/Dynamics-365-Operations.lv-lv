---
title: "Ražošanas veiktspējas Power BI saturs"
description: "Šajā tēmā ir aprakstīts, kas ir iekļauts ražošanas veiktspējas Power BI saturā. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem."
author: sericks
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: d3f5d48683c13d1affa88dd44727639cd6158c73
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---

# <a name="production-performance-power-bi-content"></a>Ražošanas veiktspējas Power BI saturs

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kas ir iekļauts **ražošanas veiktspējas** Microsoft Power BI saturā. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.

## <a name="overview"></a>Pārskats

**Ražošanas veiktspējas** Power BI saturs paredzēts ražošanas vadītājiem vai organizācijas darbiniekiem, kuri ir atbildīgi par ražošanas kontroli.

Iekļautajos pārskatos varat izmantot Power BI, lai uzraudzītu ražošanas darbību veiktspēju attiecībā uz savlaicīgu izpildi, kvalitāti un izmaksām. Pārskatos tiek izmantoti transakciju dati no ražošanas pasūtījumiem un partijas pasūtījumiem, un tie nodrošina uzņēmuma ražošanas metrikas apkopojuma un metrikas sadalījuma pēc produkta un resursa skatus.

Power BI saturs izceļ organizācijas spēju savlaicīgi un pilnībā izpildīt ražošanas procesus. Nākotnes veiktspēja tiek prognozēta, pamatojoties uz ražošanas plāniem. Visaptveroši pārskati sniedz detalizētu ieskatu par produktu brāķiem, ko izraisa ražošana, kā arī par brāķu proporcijām attiecībā uz resursiem un operācijām.

Šis Power BI saturs ļauj arī analizēt ražošanas novirzes. Ražošanas novirzes tiek aprēķinātas kā novērtēto izmaksu un realizēto izmaksu starpība. Ražošanas novirzes tiek aprēķinātas, ja ražošanas pasūtījumiem vai partijas pasūtījumiem ir statuss **Pabeigts**.

**Ražošanas veiktspējas** Power BI saturā ir iekļauti dati no ražošanas pasūtījumiem un partijas pasūtījumiem. Pārskatos nav iekļauti dati, kas ir saistīti ar Kanban ražošanām.

## <a name="accessing-the-power-bi-content"></a>Piekļūšana Power BI saturam
Ja izmantojat Microsoft Dynamics 365 for Finance and Operations izdevumu Enterprise 2017. gada jūlija atjauninājumu, **ražošanas veiktspējas** Power BI saturs tiek rādīts lapā **Ražošanas veiktspēja** (**Ražošanas kontrole** > **Pieprasījumi un pārskati** > **Ražošanas veiktspējas analīze** > **Ražošanas veiktspēja**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI saturā iekļautā metrika

**Ražošanas veiktspējas** Power BI saturā ir iekļauta pārskata lapu kopa. Katra lapa sastāv no rādītāju kopas, kuri ir vizualizēti kā diagrammas, elementi un tabulas.

Zemāk norādītajā tabulā ir sniegts pārskats par vizualizācijām, kas ir iekļautas.

| Pārskata lapa                                | Diagrammas                                               | Elementi |
|--------------------------------------------|------------------------------------------------------|-------|
| Ražošanas veiktspēja                     | <ul><li>Ražošanu skaits pēc datuma</li><li>Ražošanu skaits pēc preces un krājumu grupas</li><li>Plānoto ražošanu skaits pēc datuma</li><li>Apakšējās 10 preces pēc savlaicīgas un pilnīgas izpildes</li></ul> | <ul><li>Pasūtījumu kopskaits</li><li>Savlaicīgi un pilnībā, %</li><li>Nepilnīgi, %</li><li>Pirms termiņa, %</li><li>Nokavēts termiņš, %</li></ul> |
| Brāķi pēc preces                         | <ul><li>Brāķa proporcija (miljonās daļas) pēc datuma</li><li>Brāķa proporcija (miljonās daļas) pēc preces un krājumu grupas</li><li>Saražotais daudzums pēc datuma</li><li>Pirmās 10 preces pēc faktiskās likmes</li></ul> | <ul><li>Brāķa proporcija (miljonās daļas)</li><li>Brāķa daudzums</li><li>Kopējais daudzums</li></ul> |
| Brāķa tendences pēc preces                   | Brāķa proporcija (miljonās daļas) pēc saražotā daudzuma | Brāķa proporcija (miljonās daļas) |
| Brāķi pēc resursa                        | <ul><li>Brāķa proporcija (miljonās daļas) pēc datuma</li><li>Brāķa proporcija (miljonās daļas) pēc resursa un vietas</li><li>Brāķa proporcija (miljonās daļas) pēc darbības</li><li>Pirmie 10 resursi pēc brāķa proporcijas</li></ul> | Brāķa daudzums |
| Brāķa tendences pēc resursa                  | Brāķa proporcija (miljonās daļas) pēc apstrādātā daudzuma | |
| Darba pasūtījuma cenas ražošanas novirzes | <ul><li>Ražošanas novirzes pēc datuma un izmaksu grupas veida</li><li>Ražošanas novirzes pēc vietas un izmaksu grupas veida</li><li>Pirmās 10 preces ar nelabvēlīgu ražošanas novirzi</li><li>Pirmās 10 preces ar nelabvēlīgu ražošanas novirzi pēc resursa</li></ul> | <ul><li>Realizētās izmaksas</li><li>Ražošanas novirze</li><li>Ražošanas novirze, %</li></ul> |

## <a name="extending-the-power-bi-content"></a>Power BI satura paplašināšana
Izmantojot pakalpojumā Microsoft Dynamics Lifecycle Services (LCS) pieejamās satura pakotnes, varat nodrošināt lielisku analīzes funkcionalitāti personām, kuras nepierakstās programmatūrā Microsoft Dynamics 365. Varat izmainīt šīs satura pakotnes, tajās ietverot citus pārskatus vai vizualizācijas, un pēc tam publicēt tās savā Power BI.com nomniekā analīzes veikšanai.

**Ražošanas veiktspējas** Power BI saturs ir pieejams LCS koplietojamo līdzekļu bibliotēkā. Papildinformāciju par to, kā lejupielādēt satura pakotni un ieviest to savā organizācijā, skatiet tēmā [Power BI saturs pakalpojumā LCS no Microsoft un jūsu partneriem](power-bi-content-microsoft-partners.md). Power BI satura pakotnes implementēšanas demonstrāciju skatiet tēmā [Power BI saturs pakalpojumā Dynamics Lifecycle Services no Microsoft un jūsu partneriem](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

Noteikti lejupielādējiet **ražošanas veiktspējas** saturu, kas attiecas uz izmantoto Dynamics 365 versiju.

> [!NOTE]
> Ja izmantojat Microsoft Dynamics 365 for Operations versiju 1611, šī Power BI satura izmantošanas priekšnosacījums ir KB 4011327. Ja esat pierakstījies LCS, tad KB varat piekļūt šeit: https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana

**Ražošanas veiktspējas** Power BI satura pārskatu lapās tiek lietoti tālāk minētie dati. Šie dati tiek attēloti kā apkopoti mērījumi, kas tiek sagatavoti elementu krātuvē. Elementu krātuve ir analīzei optimizēta Microsoft SQL Server datu bāze. Papildinformāciju par elementu veikalu lasiet emuārā [Power BI integrācija elementu krātuvē programmatūrā Dynamics](power-bi-integration-entity-store.md).

Sekojošajā tabulā redzami galvenie apkopošanas mērījumi, kas tiek izmantoti kā Power BI satura pamatdati.

| Elements                   | Galvenie apkopošanas mērījumi  | Dynamics 365 for Finance and Operations datu avots | Lauks              |
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
| Ražošanas novirze, %   | SUM(Ražošanas novirze [Ražošanas novirze])/SUM(Ražošanas novirze [Novērtētās izmaksas]) |
| Visi plānotie pasūtījumi       | COUNTROWS(Plānotais ražošanas pasūtījums) |
| Agri                    | COUNTROWS (FILTER(Plānotais ražošanas pasūtījums, Plānotais ražošanas pasūtījums[Plānotais beigu datums] \< Plānotais ražošanas pasūtījums[Vajadzības datums])) |
| Vēlu                     | COUNTROWS (FILTER(Plānotais ražošanas pasūtījums, Plānotais ražošanas pasūtījums[Plānotais beigu datums] \> Plānotais ražošanas pasūtījums[Vajadzības datums])) |
| Savlaicīgi                  | COUNTROWS (FILTER(Plānotais ražošanas pasūtījums, Plānotais ražošanas pasūtījums[Plānotais beigu datums] = Plānotais ražošanas pasūtījums[Vajadzības datums])) |
| Savlaicīgi, %                | IF (Plānotais ražošanas pasūtījums[Savlaicīgi] \<\> 0, Plānotais ražošanas pasūtījums[Savlaicīgi], IF (Plānotais ražošanas pasūtījums[Visi plānotie pasūtījumi] \<\> 0, 0, BLANK()) ) / Plānotais ražošanas pasūtījums[Visi plānotie pasūtījumi] |
| Pabeigta                | COUNTROWS(FILTER(Ražošanas pasūtījums, Ražošanas pasūtījums[Ir RAF'ed] = TRUE)) |
| Brāķa proporcija (miljonās daļas)     | IF(Ražošanas pasūtījums[Kopējais daudzums] = 0, BLANK(), (SUM(Ražošanas pasūtījums[Brāķa daudzums]) /Ražošanas pasūtījums[Kopējais daudzums]) \* 1000000) |
| Ražošanas proporcija ar nokavētu termiņu  | 'Ražošanas pasūtījums'[Nokavēts termiņš \#] /Ražošanas pasūtījums[Pabeigts] |
| Pirms termiņa un pilnībā          | COUNTROWS(FILTER(Ražošanas pasūtījums, Ražošanas pasūtījums[Pilnībā] = TRUE && Ražošanas pasūtījums[Pirms termiņa] = TRUE)) |
| Pirms termiņa \#                 | COUNTROWS(FILTER(Ražošanas pasūtījums, Ražošanas pasūtījums[Pirms termiņa] = TRUE)) |
| Pirms termiņa, %                  | IFERROR( IF(Ražošanas pasūtījums[Pirms termiņa \#] \<\> 0, Ražošanas pasūtījums[Pirms termiņa \#], IF(Ražošanas pasūtījums[Pasūtījumu kopskaits] = 0, BLANK(), 0)) / Ražošanas pasūtījums[Pasūtījumu kopskaits], BLANK()) |
| Nepabeigts               | COUNTROWS(FILTER(Ražošanas pasūtījums, Ražošanas pasūtījums[Pilnībā] = FALSE && Ražošanas pasūtījums[Ir RAF'ed] = TRUE)) |
| Nepilnīgi, %             | IFERROR( IF(Ražošanas pasūtījums[Nepilnīgs] \<\> 0, Ražošanas pasūtījums[Nepilnīgs], IF(Ražošanas pasūtījums[Pasūtījumu kopskaits] = 0, BLANK(), 0)) / Ražošanas pasūtījums[Pasūtījumu kopskaits], BLANK()) |
| Nokavēts termiņš               | Ražošanas pasūtījums[Ir RAF'ed] = TRUE && Ražošanas pasūtījums[Piegādātā vērtība] = 1 |
| Pirms termiņa                 | Ražošanas pasūtījums[Is RAF'ed] = TRUE && Ražošanas pasūtījums[Kavētās dienas] \< 0 |
| Ir pilnībā               | Ražošanas pasūtījums[Derīgais daudzums] \>= Ražošanas pasūtījums[Plānotais daudzums] |
| Ir RAF'ed                | Ražošanas pasūtījums[Ražošanas statusa vērtība] = 5 \|\| Ražošanas pasūtījums[Ražošanas statusa vērtība] = 7 |
| Nokavēts termiņš un pilnībā           | COUNTROWS(FILTER(Ražošanas pasūtījums, Ražošanas pasūtījums[Ir pilnībā] = TRUE && Ražošanas pasūtījums[Nokavēts termiņš] = TRUE)) |
| Nokavēts termiņš \#                  | COUNTROWS(FILTER(Ražošanas pasūtījums, Ražošanas pasūtījums[Nokavēts termiņš] = TRUE)) |
| Nokavēts termiņš, %                   | IFERROR( IF(Ražošanas pasūtījums[Nokavēts termiņš \#] \<\> 0, Ražošanas pasūtījums[Nokavēts termiņš \#], IF(Ražošanas pasūtījums[Pasūtījumu kopskaits] = 0, BLANK(), 0)) / Ražošanas pasūtījums[Pasūtījumu kopskaits], BLANK()) |
| Savlaicīgi un pilnībā        | COUNTROWS(FILTER(Ražošanas pasūtījums, Ražošanas pasūtījums[Pilnībā] = TRUE && Ražošanas pasūtījums[Nokavēts termiņš] = FALSE && Ražošanas pasūtījums[Pirms termiņa] = FALSE)) |
| Savlaicīgi un pilnībā, %      | IFERROR( IF(Ražošanas pasūtījums[Savlaicīgi un pilnībā] \<\> 0, Ražošanas pasūtījums[Savlaicīgi un pilnībā], IF(Ražošanas pasūtījums[Pabeigts] = 0, BLANK(), 0)) / Ražošanas pasūtījums[Pabeigts], BLANK()) |
| Pasūtījumu kopskaits             | COUNTROWS(Ražošanas pasūtījums) |
| Kopējais daudzums           | SUM(Ražošanas pasūtījums[Derīgais daudzums]) + SUM(Ražošanas pasūtījums[Brāķa daudzums]) |
| Brāķa proporcija (miljonās daļas)        | IF(Maršruta darbības[Apstrādātais daudzums] = 0, BLANK(), (SUM(Maršruta darbības[Brāķa daudzums]) / Maršruta darbības[Apstrādātais daudzums]) \* 1000000) |
| Apvienotā brāķa proporcija (miljonās daļas) | IF(Maršruta darbības[Kopējais apvienotais daudzums] = 0, BLANK(), (SUM(Maršruta darbības[Brāķa daudzums]) / Maršruta darbības[Kopējais apvienotais daudzums]) \* 1000000) |
| Apstrādātais daudzums       | SUM(Maršruta darbības[Derīgais daudzums]) + SUM(Maršruta darbības[Brāķa daudzums]) |
| Kopējais apkopotais daudzums     | SUM(Ražošanas pasūtījums[Derīgais daudzums]) + SUM(Maršruta darbības[Brāķa daudzums]) |

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

## <a name="additional-resources"></a>Papildu resursi

Šeit norādītas dažas noderīgas saites, kas ir saistītas ar elementiem un Power BI satura izveidi:

- [Datu elementi](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities.md)
- [Organizācijas satura pakotnes izveide](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
- [Datu modelēšana, izmantojot Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
- [Power BI elementu pievienošana darbvietām](/dynamics365/unified-operations/dev-itpro/analytics/configure-power-bi-integration)

