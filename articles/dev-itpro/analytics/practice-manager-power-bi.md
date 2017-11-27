---
title: "Power BI satura pakotne Prakses pārvaldnieks"
description: "Šajā tēmā ir aprakstīts, kas ir iekļauts Power BI satura pakotnē Prakses pārvaldnieks. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti saturā, un ir sniegta informācija par satura izveidei izmantoto datu modeli un elementiem."
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3462ef1bbde9a98ac6a7bc9a5c54e58ff98559c8
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="practice-manager-power-bi-content"></a>Power BI satura pakotne Prakses pārvaldnieks

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kas ir iekļauts Microsoft Power BI satura pakotnē **Prakses pārvaldnieks**. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.

## <a name="overview"></a>Pārskats

Power BI satura pakotne **Prakses pārvaldnieks** ir izveidota prakses pārvaldnieku un projektu vadītāju vajadzībām. Tā nodrošina galvenos rādītājus, kas ir saistīti ar organizācijas pašreizējo projektu. Informācijas panelis sniedz pārskatu par projektiem un saistītajiem debitoriem. Lai veidotu pārskatu par noteiktām juridiskajām personām, var izmantot pārskata līmeņa filtru. Šim Power BI saturam dati tiek izvilkti no projekta uzskaites apkopojuma mērījumiem.

Power BI **Prakses pārvaldnieks** saturā ir ietvertas piecas pārskata lapas: viena kopsavilkuma lapa un četras lapas, kurās ir sniegta detalizēta informācija par projekta izmaksu, ieņēmumu, nopelnītās vērtības pārvaldības un laika rādītājiem, kas ir sadalīti dažādās dimensijās.

Visas satura pakotnē ietvertās summas ir norādītas sistēmas valūtā. Sistēmas valūtu varat iestatīt lapā **Sistēmas parametri**.

## <a name="accessing-the-power-bi-content"></a>Piekļūšana Power BI saturam
Ja izmantojat programmatūru Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (2017. gada jūlijs), tad Power BI saturs **Prakses pārvaldnieks** tiek rādīts darbvietā **Projekta pārvaldība**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI satura pakotnē iekļautie pārskati

Tālāk esošajā tabulā ir sniegta detalizēta informācija par rādītājiem, kas ir iekļauti katrā Power BI satura pakotnes **Prakses pārvaldnieks** pārskata lapā.

| Pārskata lapa       | Metrika |
|-------------------|---------|
| Projektu pārskats | <ul><li>Izveidotie projekti</li><li>Novērtētais projektu skaits</li><li>Notiekošo projektu skaits</li><li>Projektu skaits pa stadijām</li><li>Projektu skaits pa pilsētām</li><li>Faktiskie ieņēmumi pa debitoriem</li><li>Budžeta bruto peļņa pa projektiem</li><li>Pārskats par iegūtās vērtības pārvaldību</li></ul> |
| Izmaksas              | <ul><li>Faktisko un budžeta izmaksu salīdzinājums pa mēnešiem</li><li>Faktisko un budžeta izmaksu salīdzinājums pa gadiem</li><li>Faktisko un budžeta izmaksu salīdzinājums pa kategorijām</li><li>Faktiskās izmaksas pa transakciju veidiem</li></ul> |
| Ieņēmumi           | <ul><li>Faktiskie ieņēmumi pa mēnešiem</li><li>Faktiskie ieņēmumi pa pasta indeksiem</li><li>Faktisko un budžeta ieņēmumu salīdzinājums pa kategorijām</li><li>Faktiskie ieņēmumi pa debitoru nozarēm</li></ul> |
| EVM               | Izmaksu un grafika veiktspējas rādītājs pa projektiem |
| Stundas             | <ul><li>Faktisko apmaksājamo izmantoto stundu, faktisko apmaksājamo neproduktīvo stundu un budžeta stundu salīdzinājums</li><li>Faktisko apmaksājamo izmantoto stundu un faktisko apmaksājamo neproduktīvo stundu salīdzinājums pa projektiem</li><li>Faktisko apmaksājamo izmantoto stundu un faktisko apmaksājamo neproduktīvo stundu salīdzinājums pa resursiem</li><li>Faktisko apmaksājamo stundu koeficients pa projektiem</li><li>Faktisko apmaksājamo stundu koeficients pa resursiem</li></ul> |

Diagrammas un elementus attiecībā uz visiem šiem pārskatiem var filtrēt un piespraust pie informācijas paneļa. Plašāku informāciju par filtrēšanu un piespraušanu programmatūrā Power BI skatiet tēmā [Informācijas paneļa izveide un konfigurēšana](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Varat arī izmantot pamata datu eksportēšanas funkciju, lai eksportētu vizualizācijā apkopotos pamata datus.

## <a name="extending-the-power-bi-content"></a>Power BI satura paplašināšana
Izmantojot pakalpojumā Microsoft Dynamics Lifecycle Services (LCS) pieejamās satura pakotnes, varat nodrošināt lielisku analīzes funkcionalitāti personām, kuras nepierakstās programmatūrā Microsoft Dynamics 365. Varat izmainīt šīs satura pakotnes, tajās ietverot citus pārskatus vai vizualizācijas, un pēc tam publicēt tās savā Power BI.com nomniekā analīzes veikšanai. 

**Prakses pārvaldnieka** Power BI saturs ir pieejams LCS koplietojamo līdzekļu bibliotēkā. Papildinformāciju par to, kā lejupielādēt satura pakotni un ieviest to savā organizācijā, skatiet tēmā [Power BI saturs pakalpojumā LCS no Microsoft un jūsu partneriem](power-bi-content-microsoft-partners.md). Power BI satura pakotnes implementēšanas demonstrāciju skatiet tēmā [Power BI saturs pakalpojumā Dynamics Lifecycle Services no Microsoft un jūsu partneriem](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

Noteikti lejupielādējiet **Prakses pārvaldnieka** saturu, kas attiecas uz izmantoto Dynamics 365 versiju.

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana

**Prakses pārvaldnieka** Power BI satura pārskatu lapu aizpildīšanai tiek lietots tālāk minētie dati. Šie dati tiek attēloti kā apkopoti mērījumi, kas tiek sagatavoti elementu krātuvē. Elementu krātuve ir analīzei optimizēta Microsoft SQL Server datu bāze. Papildinformāciju skatiet tēmā [Apskats par Power BI integrāciju elementu krātuvē](power-bi-integration-entity-store.md).

Tālāk esošajās sadaļās ir paskaidroti apkopošanas mērījumi, kas tiek izmantoti katrā elementā.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Elements: ProjectAccountingCube_ActualHourUtilization
**Datu avots:** ProjEmplTrans

| Galvenais apkopošanas mērījums      | Lauks                              | Apraksts | 
|--------------------------------|------------------------------------|-------------|
| Faktiskās apmaksājamās izmantotās stundas | Sum(ActualUtilizationBillableRate) | Faktisko apmaksājamo izmantoto stundu kopsumma. |
| Faktiskās apmaksājamās neproduktīvās stundas   | Sum(ActualBurdenBillableRate)      | Faktisko sloga koeficientu kopsumma. |

### <a name="entity-projectaccountingcubeactuals"></a>Elements: ProjectAccountingCube_Actuals
**Datu avots:** ProjTransPosting

| Galvenais apkopošanas mērījums | Lauks              | Apraksts | 
|---------------------------|--------------------|-------------|
| Faktiskie ieņēmumi            | Sum(ActualRevenue) | Visu transakciju grāmatoto ieņēmumu kopsumma. |   
| Faktiskās izmaksas               | Sum(ActualCost)    | Visu transakciju veidu grāmatoto izmaksu kopsumma. |

### <a name="entity-projectaccountingcubecustomer"></a>Elements: ProjectAccountingCube_Customer
**Datu avots:** CustTable

| Galvenais apkopošanas mērījums | Lauks                                            | Apraksts | 
|---------------------------|--------------------------------------------------|-------------|
| Projektu skaits        | COUNTA(ProjectAccountingCube_Projects[PROJECTS]) | Pieejamo projektu skaits. |


### <a name="entity-projectaccountingcubeforecasts"></a>Elements: ProjectAccountingCube_Forecasts
**Datu avots:** ProjTransBudget

| Galvenais apkopošanas mērījums | Lauks                  | Apraksts | 
|---------------------------|------------------------|-------------|
| Budžeta izmaksas               | Sum(BudgetCost)        | Visu transakciju veidu prognozēto izmaksu kopsumma. |
| Budžeta ieņēmumi            | Sum(BudgetRevenue)     | Prognozēto gūto/rēķinos iekļauto ieņēmumu kopsumma.  |
| Budžeta bruto peļņa       | Sum(BudgetGrossMargin) | Prognozēto ieņēmumu kopsummas un prognozēto izdevumu kopsummas starpība. |

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Elements: ProjectAccountingCube_ProjectPlanCostsView
**Datu avots:** projekts

| Galvenais apkopošanas mērījums | Lauks                    | Apraksts | 
|---------------------------|--------------------------|-------------|
| Plānotās izmaksas              | Sum(SumOfTotalCostPrice) | Visu plānotus uzdevumus ietverošo projekta transakciju veidu novērtētas izmaksu cenas kopsumma. |

### <a name="entity-projectaccountingcubeprojects"></a>Elements: ProjectAccountingCube_Projects
**Datu avots:** projekts

| Galvenais apkopošanas mērījums    | Lauks | Apraksts | 
|------------------------------|-------|-------------|
| Izmaksu veiktspējas rādītājs       | ProjectAccountingCube_Projects[Iegūtā vērtība] / ProjectAccountingCube_Projects[Pabeigto uzdevumu faktisko izdevumu kopsumma] | Iegūtās vērtības kopsummas un faktisko izmaksu kopsummas dalījuma aprēķins. |
| Grafika veiktspējas rādītājs   | ProjectAccountingCube_Projects[Iegūtā vērtība] / ProjectAccountingCube_Projects[Pabeigto uzdevumu plānoto izdevumu kopsumma] | Iegūtās vērtības kopsummas un faktisko plānoto izmaksu kopsummas dalījuma aprēķins. |
| Pabeigtā darba procentuālā vērtība | Pabeigtā darba procentuālā vērtība = ProjectAccountingCube_Projects[Pabeigto uzdevumu faktisko izdevumu kopsumma] / (ProjectAccountingCube_Projects[Pabeigto uzdevumu faktisko izmaksu kopsumma] + ProjectAccountingCube_Projects[Projekta plānoto izdevumu kopsumma] – ProjectAccountingCube_Projects[Pabeigto uzdevumu plānoto izmaksu kopsumma]) | Kopējā pabeigtā darba procentuālā vērtība, pamatojoties uz pabeigto uzdevumu faktisko izmaksu un projekta plānoto izmaksu kopsummu. |
| Faktisko apmaksājamo stundu koeficients  | ProjectAccountingCube_Projects[Projekta faktisko apmaksājamo izmantoto stundu kopsumma] / (ProjectAccountingCube_Projects[Projekta faktisko apmaksājamo izmantoto stundu kopsumma] + ProjectAccountingCube_Projects[Projekta faktisko apmaksājamo neproduktīvo stundu kopsumma]) | Faktisko apmaksājamo stundu kopsumma, pamatojoties uz izmantoto stundu un papildstundu skaitu. |
| Iegūtā vērtība                 | ProjectAccountingCube_Projects[Projekta plānoto izmaksu kopsumma] * ProjectAccountingCube_Projects[Pabeigtā darba procentuālā vērtība] | Plānoto izmaksu kopsummas un pabeigtā darba procentuālās vērtības reizinājums. |

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Elements: ProjectAccountingCube_TotalEstimatedCosts 
**Datu avots:** ProjTable

| Galvenais apkopošanas mērījums       | Lauks               | Apraksts | 
|---------------------------------|---------------------|-------------|
| Pabeigtās aktivitātes plānotās izmaksas | Sum(TotalCostPrice) | Visu pabeigtus uzdevumus ietverošo projekta transakciju veidu novērtētas izmaksu cenas kopsumma. |

