---
title: "Budžeta plānošanas veidnes programmai Excel"
description: "Šajā tēmā ir aprakstīts, kā izveidot Microsoft Excel veidnes, kuras var izmantot ar budžeta plāniem."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 0e2eb6e7c130f03edbf60a185d397d94b5d61d7d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-templates-for-excel"></a>Budžeta plānošanas veidnes programmai Excel

Šajā tēmā ir aprakstīts, kā izveidot Microsoft Excel veidnes, kuras var izmantot ar budžeta plāniem.

Šī tēma rāda, kā izveidot Excel veidnes, kas tiks izmantots ar budžeta plāniem, izmantojot standarta demo datu kopu un Admin lietotāja pieteikšanās. Lai iegūtu papildu informāciju par budžeta plānošanu, skatiet [budžeta plānošana biznesam.](budget-planning-overview-configuration.md) Jūs varat arī sekot [budžeta plānošanas 101](budget-plan.md) pamācību, lai uzzinātu pamata moduļa konfigurācijas un lietošanas principi.

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>Ģenerētu budžeta plāna dokumenta izkārtojumu, izmantojot darblapas
Budžeta plāna dokumentus var skatīt un rediģēt, izmantojot vienu vai vairākus izkārtojumus. Katrs izkārtojums var būt saistītais budžeta plāna dokumenta veidne skatīt un rediģēt budžeta plāna datus Excel darblapā. Šajā tēmā, budžeta plānu dokumentu veidnes ģenerēs esošu izkārtojumu konfigurāciju. Atvērts **budžeta plānu saraksts** (**budžeta līdzekļu**&gt;**budžeta plāni**). Noklikšķiniet uz **New**, lai izveidotu jaunu budžeta plānu dokumentu. [![bpt1](./media/bpt11-1024x552.png)](./media/bpt11.png) 

Izmantojiet **pievienot** līniju opciju, lai pievienotu rindas. Noklikšķiniet uz **izkārtojumi** budžeta plāna dokumenta izkārtojuma konfigurāciju var apskatīt. 
[![bpt2](./media/bpt2-1024x274.png)](./media/bpt2.png) 

Var pārskatīt izkārtojumu konfigurācijas un pielāgot pēc vajadzības. Dodieties uz **veidnes**&gt;**Generate** izveidot Excel failu, ko šis izkārtojums. Kad tiek ģenerēts veidnes, dodieties uz **veidnes**&gt;**View** atvērt un pārskatīt budžeta plāna dokumenta veidni. Excel failu var saglabāt lokālajā diskā. [![bpt3](./media/bpt3-1024x545.png)](./media/bpt3.png) 

> [!NOTE] 
> Budžeta plāna dokumenta izkārtojumu nevar labot pēc tam, kad programmas Excel veidne ir saistīta ar to. Lai mainītu izkārtojumu, to nenodzēšat kā _ arī saistīto Excel veidni un atjaunot to. Tas ir vajadzīgs, lai saglabātu laukus izkārtojumā un darblapas sinhronizētas. 

Excel veidne satur visus elementus no budžeta plāna dokumenta izkārtojumu, kur **pieejams darblapā** kolonna ir iestatīts uz True. Excel veidnei nav atļauts izmantot pārklājošos elementu. Piemēram, ja izkārtojums satur pieprasījumu Q1, pieprasījuma Q2, pieprasījuma Q3 un pieprasījuma Q4 kolonnas un kopējā pieprasījuma kolonna, kas pārstāv visas 4 ceturkšņa kolonnas summa, tikai ceturkšņa kolonnās vai kolonnu summa ir pieejams izmantot Excel veidnes. Excel failu nevar atjaunināt pārklājas kolonnas atjaunināšanas laikā tāpēc, ka tabulas datus varētu kļūt par novecojušu un neprecīzi.

[![bpt4](./media/bpt4-1024x615.png)](./media/bpt4.png)

> [!NOTE] 
> Lai novērstu potenciālas problēmas, kas saistītas ar izmantojot Excel budžeta plānu datu skatīšanai un rediģēšanai, viens un tas pats lietotājs būtu pieteicies gan dinamiku 365 operācijas un datu savienotājs Microsoft Dynamics Office pievienojumprogramma.

## <a name="add-a-header-to-budget-plan-document-template"></a>Budžeta plāna dokumenta veidnei pievienotu galveni
Lai pievienotu galvenes informāciju, atlasiet augšējo rindu Excel failā un ievietot tukšu rindu. Noklikšķiniet uz **Design**, **datu savienotājs** pievienot galvenes lauki Excel failā.

[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png) 

Šajā **Design** tab, * * * * noklikšķiniet **pievienot** laukus un pēc tam atlasiet **BudgetPlanHeader** vienība datu avotu.

[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)

Novietojiet kursoru uz vajadzīgo vietu Excel failā. Noklikšķiniet uz **pievienot etiķetes** pievienot lauka etiķetes uz atlasīto atrašanās vietu. Atlasiet **pievienot vērtību** pievienot lauka vērtību uz izvēlēto vietu. Noklikšķiniet uz **darīts** slēgt dizainers.

## <a name="bpt7mediabpt7pngmediabpt7png"></a>[![bpt7](./media/bpt7.png)](./media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Aprēķinātas kolonnas pievienošana budžeta plāna dokumenta veidne tabula
--------------------------------------------------------------

Nākamais, aprēķinātās kolonnas tiks pievienota izveidoto budžeta plāna dokumenta veidni. A **kopējā pieprasījuma** kolonnas, kas apkopo pieprasījuma Q1: pieprasījuma Q4 kolonnas un **korekcijas** kolonna, kas tiek pārrēķināta **kopējā pieprasījuma** kolonnu ar definētu koeficientu.

Noklikšķiniet uz **Design**, **datu savienotājs** lai tabulai pievienotu kolonnas. Noklikšķiniet uz **rediģēt** blakus **BudgetPlanWorksheet** sākt kolonnu pievienošana datu avotam.

[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png) 

Kolonnas, kas pieejamas veidnes parāda atlasīto lauku grupu. Noklikšķiniet uz **Formula** jaunas kolonnas pievienošana. Jaunās kolonnas nosaukumu un pēc tam ielīmējot formulu par **Formula** lauks. Noklikšķiniet uz **Update**, lai ievietotu kolonnu.

[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> Lai definētu formulu, izveidot formulas izklājlapā un pēc tam kopēt to uz **Design** logu. Dynamics 365 operāciju saistītās tabulas parasti nosaukums ir "AXTable1". Piemēram, lai apkopotu pieprasīt Q1: pieprasīt Q4 kolonnas izklājlapā, formula = AxTable1\[pieprasīt Q1\]+ AxTable1\[pieprasīt Q2\]+ AxTable1\[pieprasīt Q3\]+ AxTable1\[pieprasīt Q4\].

Atkārtojiet šīs darbības, lai ievietotu **korekcijas** kolonna. Izmantojiet formulu = AxTable1\[kopējā pieprasījuma\]\*$I$ 1, šajā kolonnā. Tas prasīs vērtība šūnā I1 un reizināt vērtības **kopējā pieprasījuma** kolonnu, lai aprēķinātu korekciju summas.

Saglabājiet un aizveriet Excel failā. Atgrieztos Dynamics 365 operācijām, kā arī **izkārtojumi**, noklikšķiniet uz **veidnes &gt;augšupielādēt** augšupielādēt saglabāta Excel veidne jāizmanto budžeta plānu. 

[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png) 

Tuvu **izkārtojumi** slīdni. Šajā **budžeta plānu** dokumentu, noklikšķiniet uz **darblapas** apskatīt un rediģēt programmā Excel dokuments. Ņemiet vērā, ka koriģētā Excel veidne tika izmantots, lai izveidotu budžeta plānu darblapā un aprēķinātās kolonnās tiek atjaunināti, izmantojot formulas, kas bija noteikts iepriekšējās darbības. 

[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>Tips & triki, lai izveidotu budžeta plānu veidnes
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Var pievienot un izmantot papildu datu avotiem, lai budžeta plānu veidni?

Jā, jūs varat izmantot **Design** izvēlni pievienot papildu vienības tajā pašā vai citās lapās Excel veidnei. Var pievienot, piemēram, **BudgetPlanProposedProject** datu avotu, lai izveidotu un uzturētu ierosināto projektu sarakstu, tajā pašā laikā, kad darbs ar budžeta plāna datiem programmā Excel. Ņemiet vērā, tostarp liela apjoma datu avotiem var ietekmēt sniegumu Excel darbgrāmatas. 

Var izmantot **filtra** opcija **datu savienotājs** vēlamos filtrus pievienot papildu datu avotiem.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Paslēpiet noformējuma opciju datu savienotājā citiem lietotājiem?

Jā, atveriet **datu savienotājs** opciju, lai paslēptu **Design** opciju no citiem lietotājiem.

[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)

Izvērsiet **savienotāju datu opcijas** un skaidri **Iespējot noformējuma** izvēles rūtiņu. Tas būs slēpt **Design** opciju no **datu savienotājs**.

[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Lietotājiem var liegt iespēju netīšām aizvēršana datu savienotāju, kamēr strādājat ar datu

Mēs iesakām bloķēšana veidnei, lai neļautu lietotājiem aizvērt to. Lai ieslēgtu bloķēšanas, noklikšķiniet uz **datu savienotājs**, augšējā labajā stūrī parādās bultiņa. 

[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Noklikšķiniet uz bultas, lai apskatītu papildu izvēlnes. Atlasiet **Lock**.

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a>[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>Var izmantot citas programmas Excel funkciju, piemēram, šūnu formatējumu, krāsas, nosacījumformatējumu un diagrammas, izmantojot manu budžeta plānu veidnes?

Jā, lielākā daļa no standarta Excel iespējas darbosies budžeta plānu veidnes. Mēs iesakām izmantot krāsu kodēšanas lietotājiem atšķirt tikai lasāms un rediģējamas kolonnas. Nosacījumformatēšanu var izmantot, lai izceltu budžeta problemātiskās jomas. Kolonnas kopsummas var viegli jāiesniedz, izmantojot standarta Excel formulas virs tabulas.

Var arī izveidot un izmantot papildu grupējumi un budžeta datu vizualizācijas pivot tabulās un diagrammās. Par **datu** cilni, jo **savienojumus** grupu, noklikšķiniet uz **atsvaidzināt visu**, un pēc tam noklikšķiniet uz **savienojuma rekvizīti**. Noklikšķiniet uz **izmantošanas** tab. Zem **atsvaidzināt**, izvēlieties **atverot failu, atsvaidzināt datus** izvēles rūtiņu. 

[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)


