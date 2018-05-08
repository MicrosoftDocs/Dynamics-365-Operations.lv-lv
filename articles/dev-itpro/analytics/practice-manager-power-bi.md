---
title: "Power BI satura pakotne Prakses pārvaldnieks"
description: "Šajā tēmā ir aprakstīts, kas ir iekļauts Power BI satura pakotnē Prakses pārvaldnieks. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti saturā, un ir sniegta informācija par satura izveidei izmantoto datu modeli un elementiem."
author: KimANelson
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ProjManagementWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: aac6439bb54b3b9cab066b06c01763e880efef8e
ms.openlocfilehash: 44f017fc3460b83b730f2f7c909c6b88480dd918
ms.contentlocale: lv-lv
ms.lasthandoff: 12/18/2017

---

# <a name="practice-manager-power-bi-content"></a>Power BI satura pakotne Prakses pārvaldnieks

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kas ir iekļauts Microsoft Power BI satura pakotnē **Prakses pārvaldnieks**. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.

## <a name="overview"></a>Pārskats

Power BI satura pakotne **Prakses pārvaldnieks** ir izveidota prakses pārvaldnieku un projektu vadītāju vajadzībām. Tā nodrošina galvenos rādītājus, kas ir saistīti ar organizācijas pašreizējo projektu. Informācijas panelis sniedz pārskatu par projektiem un saistītajiem debitoriem. Lai veidotu pārskatu par noteiktām juridiskajām personām, var izmantot pārskata līmeņa filtru. Šim Power BI saturam dati tiek izvilkti no projekta uzskaites apkopojuma mērījumiem.

Power BI **Prakses pārvaldnieks** saturā ir ietvertas piecas pārskata lapas: viena kopsavilkuma lapa un četras lapas, kurās ir sniegta detalizēta informācija par projekta izmaksu, ieņēmumu, nopelnītās vērtības pārvaldības un laika rādītājiem, kas ir sadalīti dažādās dimensijās.

Visas satura pakotnē ietvertās summas ir norādītas sistēmas valūtā. Sistēmas valūtu varat iestatīt lapā **Sistēmas parametri**.

## <a name="accessing-the-power-bi-content"></a>Piekļūšana Power BI saturam

Power BI satura pakotne **Prakses pārvaldnieks** tiek rādīta darbvietā **Projektu pārvaldība**.


## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI satura pakotnē iekļautie pārskati

Tālāk esošajā tabulā ir sniegta detalizēta informācija par rādītājiem, kas ir iekļauti katrā Power BI satura pakotnes **Prakses pārvaldnieks** pārskata lapā.

| Pārskata lapa       | Metrika |
|-------------------|---------|
| Projektu pārskats | <ul><li>Izveidotie projekti</li><li>Novērtētais projektu skaits</li><li>Notiekošo projektu skaits</li><li>Faktiskie ieņēmumi pa debitoriem</li><li>Budžeta bruto peļņa pa projektiem</li><li>Pārskats par iegūtās vērtības pārvaldību</li></ul> |
| Izmaksas              | <ul><li>Faktisko un budžeta izmaksu salīdzinājums pa mēnešiem</li><li>Faktisko un budžeta izmaksu salīdzinājums pa gadiem</li><li>Faktisko un budžeta izmaksu salīdzinājums pa kategorijām</li><li>Faktiskās izmaksas pa transakciju veidiem</li></ul> |
| Ieņēmumi           | <ul><li>Faktiskie ieņēmumi pa mēnešiem</li><li>Faktiskie ieņēmumi pa pasta indeksiem</li><li>Faktisko un budžeta ieņēmumu salīdzinājums pa kategorijām</li><li>Faktiskie ieņēmumi pa debitoru nozarēm</li></ul> |
| EVM               | Izmaksu un grafika veiktspējas rādītājs pa projektiem |
| Stundas             | <ul><li>Faktisko apmaksājamo izmantoto stundu, faktisko apmaksājamo neproduktīvo stundu un budžeta stundu salīdzinājums</li><li>Faktisko apmaksājamo izmantoto stundu un faktisko apmaksājamo neproduktīvo stundu salīdzinājums pa projektiem</li><li>Faktisko apmaksājamo izmantoto stundu un faktisko apmaksājamo neproduktīvo stundu salīdzinājums pa resursiem</li><li>Faktisko apmaksājamo stundu koeficients pa projektiem</li><li>Faktisko apmaksājamo stundu koeficients pa resursiem</li></ul> |

Diagrammas un elementus attiecībā uz visiem šiem pārskatiem var filtrēt un piespraust pie informācijas paneļa. Plašāku informāciju par filtrēšanu un piespraušanu programmatūrā Power BI skatiet tēmā [Informācijas paneļa izveide un konfigurēšana](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Varat arī izmantot pamata datu eksportēšanas funkciju, lai eksportētu vizualizācijā apkopotos pamata datus.

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana

**Prakses pārvaldnieka** Power BI satura pārskatu lapu aizpildīšanai tiek lietots tālāk minētie dati. Šie dati tiek attēloti kā apkopoti mērījumi, kas tiek sagatavoti elementu krātuvē. Elementu krātuve ir analīzei optimizēta Microsoft SQL Server datu bāze. Papildinformāciju skatiet tēmā [Apskats par Power BI integrāciju elementu krātuvē](power-bi-integration-entity-store.md).

Tālāk esošajās sadaļās ir paskaidroti apkopošanas mērījumi, kas tiek izmantoti katrā elementā.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Elements: ProjectAccountingCube\_ActualHourUtilization
**Datu avots:** ProjEmplTrans

| Galvenais apkopošanas mērījums      | Lauks                              | Apraksts |
|--------------------------------|------------------------------------|-------------|
| Faktiskās apmaksājamās izmantotās stundas | Sum(ActualUtilizationBillableRate) | Faktisko apmaksājamo izmantoto stundu kopsumma. |
| Faktiskās apmaksājamās neproduktīvās stundas   | Sum(ActualBurdenBillableRate)      | Faktisko sloga koeficientu kopsumma. |

### <a name="entity-projectaccountingcubeactuals"></a>Elements: ProjectAccountingCube\_Actuals
**Datu avots:** ProjTransPosting

| Galvenais apkopošanas mērījums | Lauks              | Apraksts |
|---------------------------|--------------------|-------------|
| Faktiskie ieņēmumi            | Sum(ActualRevenue) | Visu transakciju grāmatoto ieņēmumu kopsumma. |
| Faktiskās izmaksas               | Sum(ActualCost)    | Visu transakciju veidu grāmatoto izmaksu kopsumma. |

### <a name="entity-projectaccountingcubecustomer"></a>Elements: ProjectAccountingCube\_Customer
**Datu avots:** CustTable

| Galvenais apkopošanas mērījums | Lauks                                             | Apraksts |
|---------------------------|---------------------------------------------------|-------------|
| Projektu skaits        | COUNTA(ProjectAccountingCube\_Projects[PROJECTS]) | Pieejamo projektu skaits. |


### <a name="entity-projectaccountingcubeforecasts"></a>Elements: ProjectAccountingCube\_Forecasts
**Datu avots:** ProjTransBudget

| Galvenais apkopošanas mērījums | Lauks                  | Apraksts |
|---------------------------|------------------------|-------------|
| Budžeta izmaksas               | Sum(BudgetCost)        | Visu transakciju veidu prognozēto izmaksu kopsumma. |
| Budžeta ieņēmumi            | Sum(BudgetRevenue)     | Prognozēto gūto/rēķinos iekļauto ieņēmumu kopsumma. |
| Budžeta bruto peļņa       | Sum(BudgetGrossMargin) | Prognozēto ieņēmumu kopsummas un prognozēto izdevumu kopsummas starpība. |

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Elements: ProjectAccountingCube\_ProjectPlanCostsView
**Datu avots:** projekts

| Galvenais apkopošanas mērījums | Lauks                    | Apraksts |
|---------------------------|--------------------------|-------------|
| Plānotās izmaksas              | Sum(SumOfTotalCostPrice) | Visu plānotus uzdevumus ietverošo projekta transakciju veidu novērtētas izmaksu cenas kopsumma. |

### <a name="entity-projectaccountingcubeprojects"></a>Elements: ProjectAccountingCube\_Projects
**Datu avots:** projekts

| Galvenais apkopošanas mērījums    | Lauks | Apraksts |
|------------------------------|-------|-------------|
| Izmaksu veiktspējas rādītājs       | ProjectAccountingCube\_Projects[Iegūtā vērtība] ÷ ProjectAccountingCube\_Projects[Pabeigto uzdevumu faktisko izmaksu kopsumma] | Iegūtās vērtības kopsummas un faktisko izmaksu kopsummas dalījuma aprēķins. |
| Grafika veiktspējas rādītājs   | ProjectAccountingCube\_Projects[Iegūtā vērtība] ÷ ProjectAccountingCube\_Projects[Pabeigto uzdevumu plānoto izmaksu kopsumma] | Iegūtās vērtības kopsummas un faktisko plānoto izmaksu kopsummas dalījuma aprēķins. |
| Pabeigtā darba procentuālā vērtība | Pabeigtā darba procentuālā vērtība = ProjectAccountingCube\_Projects[Pabeigto uzdevumu faktisko izmaksu kopsumma] ÷ (ProjectAccountingCube\_Projects[Pabeigto uzdevumu faktisko izmaksu kopsumma] + ProjectAccountingCube\_Projects[Projekta plānoto izmaksu kopsumma] – ProjectAccountingCube\_Projects[Pabeigto uzdevumu plānoto izmaksu kopsumma]) | Kopējā pabeigtā darba procentuālā vērtība, pamatojoties uz pabeigto uzdevumu faktisko izmaksu un projekta plānoto izmaksu kopsummu. |
| Faktisko apmaksājamo stundu koeficients  | ProjectAccountingCube\_Projects[Projekta faktisko apmaksājamo izmantoto stundu kopsumma] ÷ (ProjectAccountingCube\_Projects[Projekta faktisko apmaksājamo izmantoto stundu kopsumma] + ProjectAccountingCube\_Projects[Projekta faktisko apmaksājamo neproduktīvo stundu kopsumma]) | Faktisko apmaksājamo stundu kopsumma, pamatojoties uz izmantoto stundu un papildstundu skaitu. |
| Iegūtā vērtība                 | ProjectAccountingCube\_Projects[Projekta plānoto izmaksu kopsumma] × ProjectAccountingCube\_Projects[Pabeigtā darba procentuālā vērtība] | Plānoto izmaksu kopsummas un pabeigtā darba procentuālās vērtības reizinājums. |

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Elements: ProjectAccountingCube\_TotalEstimatedCosts 
**Datu avots:** ProjTable


|    Galvenais apkopošanas mērījums    |        Lauks        |                                          Apraksts                                           |
|---------------------------------|---------------------|------------------------------------------------------------------------------------------------|
| Pabeigtās aktivitātes plānotās izmaksas | Sum(TotalCostPrice) | Visu pabeigtus uzdevumus ietverošo projekta transakciju veidu novērtētas izmaksu cenas kopsumma. |


