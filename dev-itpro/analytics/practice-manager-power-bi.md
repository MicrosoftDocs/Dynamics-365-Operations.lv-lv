---
title: "Power BI satura pakotne Prakses pārvaldnieks"
description: "Šajā tēmā ir aprakstīts, kas ir iekļauts Power BI satura pakotnē Prakses pārvaldnieks. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti satura pakotnē, un ir sniegta informācija par satura pakotnes izveidei izmantoto datu modeli un elementiem."
author: knelson
manager: AnnBe
ms.date: 04/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer/IT Pro
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.dyn365.intro: 2017/04/27
ms.dyn365.version: 
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0f2a1a9df8e5036c60b74b8a710e606b0b1e312a
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="practice-manager-power-bi-content"></a>Power BI satura pakotne Prakses pārvaldnieks

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīts, kas ir iekļauts Microsoft Power BI satura pakotnē **Prakses pārvaldnieks**. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.

## <a name="overview"></a>Pārskats

Power BI satura pakotne **Prakses pārvaldnieks** ir izveidota prakses pārvaldnieku un projektu vadītāju vajadzībām. Tā nodrošina galvenos rādītājus, kas ir saistīti ar organizācijas pašreizējo projektu. Informācijas panelis sniedz pārskatu par projektiem un saistītajiem debitoriem. Lai veidotu pārskatu par noteiktām juridiskajām personām, var izmantot pārskata līmeņa filtru. Šī Power BI satura pakotne nodrošina datu izgūšanu no Microsoft Dynamics 365 for Operations projekta uzskaites apkopošanas mērījumiem.

Power Bi satura pakotnē **Prakses pārvaldnieks** ir ietvertas piecas pārskata lapas: viena kopsavilkuma lapa un četras lapas, kurās ir sniegta detalizēta informācija par projekta izmaksu, ieņēmumu, nopelnītās vērtības pārvaldības un laika rādītājiem, kas ir norādīti atbilstoši dažādām dimensijām.

Visas satura pakotnē ietvertās summas ir norādītas sistēmas valūtā. Sistēmas valūtu varat iestatīt lapā **Sistēmas parametri**.

## <a name="accessing-the-power-bi-content"></a>Piekļūšana Power BI saturam

Power BI satura pakotne **Prakses vadītājs** ir pieejama Microsoft Dynamics Lifecycle Services (LCS) koplietojamo līdzekļu bibliotēkā. Papildinformāciju par to, kā lejupielādēt šo satura pakotni un izveidot tās savienojumu ar Dynamics 365 for Operations datiem, skatiet tēmā [Power BI saturs LCS no Microsoft un jūsu partneriem](power-bi-content-microsoft-partners.md).

Power BI satura pakotnes implementēšanas demonstrāciju skatiet tēmā [Power BI saturs pakalpojumā Dynamics Lifecycle Services no Microsoft un jūsu partneriem](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI satura pakotnē iekļautie pārskati

Tālāk esošajā tabulā ir sniegta detalizēta informācija par rādītājiem, kas ir iekļauti katrā Power BI satura pakotnes **Prakses pārvaldnieks** pārskata lapā.

| Pārskata lapa                                          | Metrika               |
|------------------------------------------------------|-----------------------------------------------|
| Informācijas panelis  | Izveidotie projekti<br>Novērtētais projektu skaits<br>Notiekošo projektu skaits<br>Projektu skaits pa stadijām<br>Projektu skaits pa pilsētām<br>Faktiskie ieņēmumi pa debitoriem<br>Budžeta bruto peļņa pa projektiem<br>Pārskats par iegūtās vērtības pārvaldību |
| Izmaksas                                                 | Faktisko un budžeta izmaksu salīdzinājums pa mēnešiem<br>Faktisko un budžeta izmaksu salīdzinājums pa gadiem<br>Faktisko un budžeta izmaksu salīdzinājums pa kategorijām<br>Faktiskās izmaksas pa transakciju veidiem       |
| Ieņēmumi                                              | Faktiskie ieņēmumi pa mēnešiem<br>Faktiskie ieņēmumi pa pasta indeksiem<br>Faktisko un budžeta ieņēmumu salīdzinājums pa kategorijām<br>Faktiskie ieņēmumi pa debitoru nozarēm        |
| EVM                                                  | Izmaksu un grafika veiktspējas rādītājs pa projektiem                 |
| Stundas                                                | Faktisko apmaksājamo izmantoto stundu, faktisko apmaksājamo neproduktīvo stundu un budžeta stundu salīdzinājums<br>Faktisko apmaksājamo izmantoto stundu un faktisko apmaksājamo neproduktīvo stundu salīdzinājums pa projektiem<br>Faktisko apmaksājamo izmantoto stundu un faktisko apmaksājamo neproduktīvo stundu salīdzinājums pa resursiem<br>Faktisko apmaksājamo stundu koeficients pa projektiem<br>Faktisko apmaksājamo stundu koeficients pa resursiem |

Diagrammas un elementus attiecībā uz visiem šiem pārskatiem var filtrēt un piespraust pie informācijas paneļa. Plašāku informāciju par filtrēšanu un piespraušanu programmatūrā Power BI skatiet tēmā [Informācijas paneļa izveide un konfigurēšana](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Varat arī izmantot pamata datu eksportēšanas funkciju, lai eksportētu vizualizācijā apkopotos pamata datus.

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana

Power BI satura pakotnes **Prakses pārvaldnieks** pārskatu lapu aizpildīšanai tiek lietoti Dynamics 365 for Operations dati. Šie dati tiek attēloti kā apkopoti mērījumi, kuri pa posmiem tiek izveidoti elementu krātuvē, kas ir analīzes veikšanai optimizēta Microsoft SQL datu bāze. Papildinformāciju skatiet tēmā [Apskats par Power BI integrāciju elementu krātuvē](power-bi-integration-entity-store.md).

Tālāk esošajās sadaļās ir paskaidroti apkopošanas mērījumi, kas tiek izmantoti katrā elementā.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Elements: ProjectAccountingCube_ActualHourUtilization
**Datu avots**: ProjEmplTrans

| Galvenais apkopošanas mērījums                | Lauks                                | apraksts                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualBillableUtilizedHours              | Sum(ActualUtilizationBillableRate)   | Faktisko apmaksājamo izmantoto stundu kopsumma |
| ActualBillableBurdenHours                | Sum(ActualBurdenBillableRate)        | Faktisko sloga koeficientu kopsumma             |

### <a name="entity-projectaccountingcubeactuals"></a>Elements: ProjectAccountingCube_Actuals
**Datu avots**: ProjTransPosting

| Galvenais apkopošanas mērījums                | Lauks                                | apraksts                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualRevenue                            |     Sum(ActualRevenue)               |  Visu transakciju grāmatoto ieņēmumu kopsumma |   
| ActualCost   |                             Sum(ActualCost)           |    Visu transakciju veidu grāmatoto izmaksu kopsumma    |

### <a name="entity-projectaccountingcubecustomer"></a>Elements: ProjectAccountingCube_Customer
**Datu avots**: CustTable

| Galvenais apkopošanas mērījums                | Lauks                                | apraksts                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    Projektu skaits        |   COUNTA(ProjectAccountingCube_Projects[PROJECTS])       |         Pieejamo projektu skaits    |


### <a name="entity-projectaccountingcubeforecasts"></a>Elements: ProjectAccountingCube_Forecasts
**Datu avots**: ProjTransBudget

| Galvenais apkopošanas mērījums                | Lauks                                | apraksts                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    BudgetCost    |       Sum(BudgetCost)  |       Visu transakciju veidu prognozēto izmaksu kopsumma     |
|     BudgetRevenue    |         Sum(BudgetRevenue)    |    Prognozēto gūto/rēķinos iekļauto ieņēmumu kopsumma         |
|BudgetGrossMargin | Sum(BudgetGrossMargin) |Prognozēto ieņēmumu kopsummas un prognozēto izdevumu kopsummas starpība

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Elements: ProjectAccountingCube_ProjectPlanCostsView
**Datu avots**: Project

| Galvenais apkopošanas mērījums                | Lauks                                | apraksts                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|      PlannedCost      |        Sum(SumOfTotalCostPrice)   | Visu plānotus uzdevumus ietverošo projekta transakciju veidu novērtētas izmaksu cenas kopsumma |

### <a name="entity-projectaccountingcubeprojects"></a>Elements: ProjectAccountingCube_Projects
**Datu avots**: Project

| Galvenais apkopošanas mērījums                | Lauks                                | apraksts                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|   Izmaksu veiktspējas rādītājs  |ProjectAccountingCube_Projects[Iegūtā vērtība] / ProjectAccountingCube_Projects[Pabeigto uzdevumu faktisko izdevumu kopsumma] |     Iegūtās vērtības kopsummas un faktisko izmaksu kopsummas dalījuma aprēķins|
|  Grafika veiktspējas rādītājs |ProjectAccountingCube_Projects[Iegūtā vērtība] / ProjectAccountingCube_Projects[Pabeigto uzdevumu plānoto izdevumu kopsumma]|Iegūtās vērtības kopsummas un plānoto izmaksu kopsummas dalījuma aprēķins |
|Pabeigtā darba procentuālā vērtība |Pabeigtā darba procentuālā vērtība = ProjectAccountingCube_Projects[Pabeigto uzdevumu faktisko izdevumu kopsumma] / (ProjectAccountingCube_Projects[Pabeigto uzdevumu faktisko izmaksu kopsumma] + ProjectAccountingCube_Projects[Projekta plānoto izdevumu kopsumma] – ProjectAccountingCube_Projects[Pabeigto uzdevumu plānoto izmaksu kopsumma])|Kopējā pabeigtā darba procentuālā vērtība, pamatojoties uz pabeigto uzdevumu faktisko izmaksu un projekta plānoto izmaksu kopsummu.|
|Projekta faktisko apmaksājamo stundu koeficients|ProjectAccountingCube_Projects[Projekta faktisko apmaksājamo izmantoto stundu kopsumma] / (ProjectAccountingCube_Projects[Projekta faktisko apmaksājamo izmantoto stundu kopsumma] + ProjectAccountingCube_Projects[Projekta faktisko apmaksājamo neproduktīvo stundu kopsumma])|Faktisko apmaksājamo stundu kopsumma, pamatojoties uz izmantoto un neproduktīvo stundu summu|
|Iegūtā vērtība|ProjectAccountingCube_Projects[Projekta plānoto izmaksu kopsumma] * ProjectAccountingCube_Projects[Pabeigtā darba procentuālā vērtība]|Plānoto izmaksu kopsummas un pabeigtā darba procentuālās vērtības reizinājums|

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Elements: ProjectAccountingCube_TotalEstimatedCosts 
**Datu avots**: ProjTable

| Galvenais apkopošanas mērījums                | Lauks                                | apraksts                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| CompletedActivityPlannedCost  |  Sum(TotalCostPrice)  |   Visu pabeigtus uzdevumus ietverošo projekta transakciju veidu novērtētas izmaksu cenas kopsumma|

## <a name="additional-resources"></a>Papildu resursi

Šeit norādītas dažas noderīgas saites, kas ir saistītas ar elementiem un Power BI satura izveidi:

- [Datu elementi](/dynamics365/operations/dev-itpro/data-entities/data-entities)
- [Organizācijas satura pakotnes izveide](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
- [Datu modelēšana, izmantojot Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
- [Power BI integrācijas konfigurēšana darbvietām](configure-power-bi-integration.md)

