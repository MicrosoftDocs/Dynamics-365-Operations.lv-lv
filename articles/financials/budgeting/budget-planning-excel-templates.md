---
title: Budžeta plānošanas veidnes programmai Excel
description: Šajā tēmā ir aprakstīts, ka izveidot Microsoft Excel veidnes, ko var izmantot kopā ar budžeta plāniem.
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanSetLayout
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f931853b4c7ff7c21e1d6362319b776a54697088
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834227"
---
# <a name="budget-planning-templates-for-excel"></a>Budžeta plānošanas veidnes programmai Excel

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, ka izveidot Microsoft Excel veidnes, ko var izmantot kopā ar budžeta plāniem.

Šajā tēmā ir parādīts, ka izveidot Excel veidnes, kuras tiks izmantotas ar budžeta plāniem, izmantojot standarta demonstrācijas datu kopu un piesakoties lietotājam ar administratora tiesībām. Papildinformāciju par darbu ar budžeta plānošanu skatiet sadaļā [Budžeta plānošanas apskats.](budget-planning-overview-configuration.md) Lai apgūtu moduļa konfigurēšanas un lietošanas pamatprincipus, varat izpildīt arī apmācību [Budžeta plānošana 101](budget-plan.md).

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>Ģenerēt darblapu, izmantojot budžeta plāna dokumenta izkārtojumu

Budžeta plāna dokumentus var skatīt un rediģēt, izmantojot vienu vai vairākus izkārtojumus. Ar katru izkārtojumu var būt saistīta budžeta plāna dokumenta veidne, lai šos budžeta plāna datus skatītu un rediģētu Excel darblapā. Šajā tēmā budžeta plāna dokumenta veidne tiks ģenerēta, izmantojot jau esošu izkārtojuma konfigurāciju. 

1. Atveriet sadaļu **Budžeta plānu saraksts** (**Budžeta veidošana** &gt; **Budžeta plāni**). 
2. Noklikšķiniet uz **Jauns**, lai izveidotu jaunu budžeta plāna dokumentu. 

   [![Budžeta plānu saraksts](./media/bpt11-1024x552.png)](./media/bpt11.png) 

3. Izmantojiet rindas opciju **Pievienot**, lai pievienotu rindas. Noklikšķiniet uz **Izkārtojumi**, lai skatītu budžeta plāna dokumenta izkārtojuma konfigurāciju. 

   [![Budžeta plānu pievienošana](./media/bpt2-1024x274.png)](./media/bpt2.png) 

Izkārtojuma konfigurāciju varat pārskatīt un pēc nepieciešamības koriģēt. 
1. Dodieties uz **Veidne** &gt; **Ģenerēt**, lai izveidotu Excel failu šim izkārtojumam. 
2. Kad veidne ir ģenerēta, pārejiet uz **Veidne** &gt; **Skatīt**, lai atvērtu un pārskatītu budžeta plāna dokumenta veidni. Šo Excel failu varat saglabāt lokālajā diskā. 

[![Saglabāt kā](./media/bpt3-1024x545.png)](./media/bpt3.png)

> [!NOTE] 
> Kad ar budžeta plāna dokumenta izkārtojumu ir saistīta Excel veidne, šo izkārtojumu vairs nevar rediģēt. Lai izkārtojumu modificētu, izdzēsiet piesaistītās Excel veidnes failu un ģenerējiet to no jauna. Tas ir nepieciešams tādēļ, lai izkārtojuma un darblapas lauki būtu sinhronizēti. 

Excel veidnē būs visi elementi no budžeta plāna dokumenta izkārtojuma, kur kolonnas **Pieejams darblapā** vērtība ir iestatīta uz Patiess. Excel veidnē nav atļauta elementu pārklāšanās. Piemēram, ja izkārtojumā ietilpst kolonnas Pieprasījums Q1, Pieprasījums Q2, Pieprasījums Q3 un Pieprasījums Q4, un kopīgā pieprasījuma kolonna, kas pārstāv visu četru ceturkšņu kolonnu summu, tad Excel veidnē lietošanai ir pieejamas tikai ceturkšņa kolonnas vai kopējā kolonna. Atjaunināšanas laikā Excel fails nevar atjaunināt kolonnas, kas pārklājas, jo tabulā esošie dati varētu kļūt novecojuši vai neprecīzi.

[![Paraugs](./media/bpt4-1024x615.png)](./media/bpt4.png)

> [!NOTE] 
> Lai nepieļautu iespējamas problēmas saistībā ar budžeta plāna datu skatīšanu un rediģēšanu, izmantojot programmu Excel, programmā Microsoft Dynamics 365 for Finance and Operations un Microsoft Dynamics Office pievienojumprogrammā Datu savienotājs ir jāpiesakās vienam un tam pašam lietotājam.

## <a name="add-a-header-to-budget-plan-document-template"></a>Pievienot galveni budžeta plāna dokumenta veidnei
Lai pievienotu galvenes informāciju, atlasiet augšējo rindu Excel failā un ievietojiet tukšas rindas. Programmā **Datu savienotājs** noklikšķiniet uz **Dizains**, lai Excel failam pievienotu galvenes laukus.

[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png) 

Cilnē **Dizains** noklikšķiniet uz **Pievienot laukus** un pēc tam kā elementa datu avotu atlasiet vienumu **BudgetPlanHeader**.

[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)

Ar kursoru norādiet uz vēlamo vietu Excel failā. Noklikšķiniet uz **Pievienot etiķeti**, lai atlasītajai vietai pievienotu lauka etiķeti. Atlasiet vienumu **Pievienot vērtību**, lai atlasītajai vietai pievienotu šo vērtības lauku. Lai aizvērtu noformētāju, noklikšķiniet uz **Gatavs**.

## <a name="bpt7mediabpt7pngmediabpt7png"></a>[![bpt7](./media/bpt7.png)](./media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Pievienot aprēķinātu kolonnu budžeta plāna dokumenta veidnes tabulai
--------------------------------------------------------------

Pēc tam ģenerētajai budžeta plāna dokumenta veidnei tiks pievienotas aprēķinātas kolonnas. Kolonna **Kopējais pieprasījums**, kurā ir kolonnu Pieprasījums Q1: Pieprasījums Q4 summa, un kolonna **Korekcija**, kas kolonnu **Kopējais pieprasījums** pārrēķina pēc sākotnēji definēta koeficienta.

Programmā **Datu savienotājs** noklikšķiniet uz **Dizains**, lai tabulai pievienotu kolonnas. Noklikšķiniet uz **Rediģēt** blakus datu avotam **BudgetPlanWorksheet**, lai sāktu pievienot kolonnas.

[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png) 

Atlasītajā lauku grupā tiek rādītas veidnē pieejamās kolonnas. Noklikšķiniet uz **Formula**, lai pievienotu jaunu kolonnu. Jaunajai kolonnai piešķiriet nosaukumu un pēc tam ielīmējiet formulu laukā **Formula**. Noklikšķiniet uz **Atjaunināt**, lai šo kolonnu ievietotu.

[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> Lai formulu definētu, izveidojiet šo formulu izklājlapā un pēc tam to iekopējiet logā **Dizains**. Ar programmatūru Dynamics 365 for Finance and Operations saistītai tabulai parasti tiek piešķirts nosaukums “AXTable1”. Piemēram, lai izklājlapā apkopotu kolonnas Pieprasījums Q1 : Pieprasījums Q4, tiek izmantota formula = AxTable1\[Pieprasījums Q1\]+AxTable1\[Pieprasījums Q2\]+AxTable1\[Pieprasījums Q3\]+AxTable1\[Pieprasījums Q4\].

Atkārtojiet šīs darbības, lai ievietotu kolonnu **Korekcija**. Šai kolonnai izmantojiet formulu = AxTable1\[Kopējais pieprasījums\]\*$I$1. Šādi šūnā I1 esošā vērtība tiks izmantota reizināšanai ar vērtībām kolonnā **Kopējais pieprasījums**, lai aprēķinātu korekcijas summas.

Saglabājiet un aizveriet Excel failu. Atgriezieties programmatūrā Dynamics 365 for Finance and Operations un sadaļā **Izkārtojumi** noklikšķiniet uz **Veidne &gt; Augšupielādēt**, lai saglabāto Excel veidni augšupielādētu lietošanai budžeta plānā. 

[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png) 

Aizvediet slīdni **Izkārtojumi**. Dokumentā **Budžeta plāns** noklikšķiniet uz **Darblapa**, lai dokumentu skatītu un rediģētu programmā Excel. Ņemiet vērā, ka koriģētā Excel veidne tika izmantota, lai izveidotu šo budžeta plāna darblapu, un aprēķinātās kolonnas tiek atjauninātas, izmantojot iepriekšējās darbībās definētās formulas. 

[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>Padomi un ieteikumi par budžeta plāna veidņu izveidošanu
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Vai budžeta plāna veidnei var pievienot un lietot papildu datu avotus?

Jā, varat izmantot izvēlni **Dizains**, lai tai pašai vai citām Excel veidnes lapām pievienotu papildu elementus. Varat, piemēram, pievienot datu avotu **BudgetPlanProposedProject**, lai izveidotu un uzturētu sarakstu ar piedāvātajiem projektiem, tajā pašā laikā strādājot ar budžeta plāna datiem programmā Excel. Ņemiet vēra, ka lielapjoma datu avotu iekļaušana var ietekmēt Excel darbgrāmatas veiktspēju. 

Programmā **Datu savienotājs** varat izmantot opciju **Filtrs**, lai papildu datu avotiem pievienotu vēlamos filtrus.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Vai programmā Datu savienotājs citiem lietotājiem varu slēpt opciju Dizains?

Jā, atveriet programmas **Datu savienotājs** opcijas, lai opciju **Dizains** paslēptu no citiem lietotājiem.

[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)

Izvērsiet sadaļu **Datu savienotāja opcijas** un noņemiet atzīmi izvēles rūtiņai **Iespējot dizainu**. Šādi opcija **Dizains** tiks paslēpta no programmas **Datu savienotājs** loga.

[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Vai varu nepieļaut, ka lietotāji nejauši aizver datu savienotāju, kamēr strādā ar datiem?

Ieteicams veidni bloķēt, lai nepieļautu, ka lietotāji to aizver. Lai ieslēgtu bloķēšanu, noklikšķiniet uz **Datu savienotājs**, un labā augšējā stūrī kļūst redzama bultiņa. 

[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Noklikšķiniet uz šīs bultiņas, lai atvērtu papildu izvēlni. Atlasiet vienumu **Bloķēt**.

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a>[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>Vai savām budžeta plāna veidnēm varu lietot citus Excel līdzekļus, piemēram, šūnu formatēšanu, krāsas, nosacījumformatēšanu un diagrammas?

Jā, budžeta plāna veidnēs darbojas vairums Excel standarta iespēju. Ieteicams lietot krāsu kodējumu, lai tikai lasāmās kolonnas lietotāji varētu atšķirt no rediģējamajām. Nosacījumformatēšanu var izmantot, lai izceltu budžeta problemātiskos apgabalus. Kolonnu kopsummas var ērti attēlot, virs tabulas izmantojot Excel standarta formulas.

Varat arī izveidot un lietot rakurstabulas un diagrammas budžeta datu papildu grupēšanai un vizualizēšanai. Cilnē **Dati**, grupā **Savienojumi** noklikšķiniet uz **Atsvaidzināt visu** un pēc tam noklikšķiniet uz **Savienojuma rekvizīti**. Noklikšķiniet uz cilnes **Lietojums**. Sadaļā **Atsvaidzināt** atzīmējiet izvēles rūtiņu **Atsvaidzināt datus faila atvēršanas laikā**. 

[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)



