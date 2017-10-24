---
title: "Budžeta plānošanas veidnes programmai Excel"
description: "Šajā tēmā ir aprakstīts, ka izveidot Microsoft Excel veidnes, kuras var izmantot ar budžeta plāniem."
author: ryansandness
manager: AnnBe
ms.date: 07/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7cec40859a8c68cb8a9751c5531c67cef7706258
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="budget-planning-templates-for-excel"></a><span data-ttu-id="c6acc-103">Budžeta plānošanas veidnes programmai Excel</span><span class="sxs-lookup"><span data-stu-id="c6acc-103">Budget planning templates for Excel</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c6acc-104">Šajā tēmā ir aprakstīts, ka izveidot Microsoft Excel veidnes, kuras var izmantot ar budžeta plāniem.</span><span class="sxs-lookup"><span data-stu-id="c6acc-104">This topic describes how to create Microsoft Excel templates that can be used with budget plans.</span></span>

<span data-ttu-id="c6acc-105">Šajā tēmā ir parādīts, ka izveidot Excel veidnes, kuras tiks izmantotas ar budžeta plāniem, izmantojot standarta demonstrācijas datu kopu un piesakoties lietotājam ar administratora tiesībām.</span><span class="sxs-lookup"><span data-stu-id="c6acc-105">This topic shows how to create Excel templates that will be used with budget plans using the standard demo data set and the Admin user login.</span></span> <span data-ttu-id="c6acc-106">Papildinformāciju par darbu ar budžeta plānošanu skatiet sadaļā [Budžeta plānošanas apskats.](budget-planning-overview-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="c6acc-106">For more information about budget planning, see [Budget planning overview.](budget-planning-overview-configuration.md)</span></span> <span data-ttu-id="c6acc-107">Lai apgūtu moduļa konfigurēšanas un lietošanas pamatprincipus, varat izpildīt arī apmācību [Budžeta plānošana 101](budget-plan.md).</span><span class="sxs-lookup"><span data-stu-id="c6acc-107">You can also follow the [Budget planning 101](budget-plan.md) tutorial to learn basic module configuration and usage principles.</span></span>

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a><span data-ttu-id="c6acc-108">Ģenerēt darblapu, izmantojot budžeta plāna dokumenta izkārtojumu</span><span class="sxs-lookup"><span data-stu-id="c6acc-108">Generate a worksheet using budget plan document layout</span></span>

<span data-ttu-id="c6acc-109">Budžeta plāna dokumentus var skatīt un rediģēt, izmantojot vienu vai vairākus izkārtojumus.</span><span class="sxs-lookup"><span data-stu-id="c6acc-109">Budget plan documents can be viewed and edited using one or more layouts.</span></span> <span data-ttu-id="c6acc-110">Ar katru izkārtojumu var būt saistīta budžeta plāna dokumenta veidne, lai šos budžeta plāna datus skatītu un rediģētu Excel darblapā.</span><span class="sxs-lookup"><span data-stu-id="c6acc-110">Each layout can have an associated budget plan document template to view and edit the budget plan data in an Excel worksheet.</span></span> <span data-ttu-id="c6acc-111">Šajā tēmā budžeta plāna dokumenta veidne tiks ģenerēta, izmantojot jau esošu izkārtojuma konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="c6acc-111">In this topic, a budget plan document template will be generated using an existing layout configuration.</span></span> 

1. <span data-ttu-id="c6acc-112">Atveriet sadaļu **Budžeta plānu saraksts** (**Budžeta veidošana** &gt; **Budžeta plāni**).</span><span class="sxs-lookup"><span data-stu-id="c6acc-112">Open the **Budget plans list** (**Budgeting** &gt; **Budget plans**).</span></span> 
2. <span data-ttu-id="c6acc-113">Noklikšķiniet uz **Jauns**, lai izveidotu jaunu budžeta plāna dokumentu.</span><span class="sxs-lookup"><span data-stu-id="c6acc-113">Click **New** to create a new budget plan document.</span></span> 

  <span data-ttu-id="c6acc-114">[![Budžeta plānu saraksts](./media/bpt11-1024x552.png)](./media/bpt11.png)</span><span class="sxs-lookup"><span data-stu-id="c6acc-114">[![Budget plans list](./media/bpt11-1024x552.png)](./media/bpt11.png)</span></span> 

3. <span data-ttu-id="c6acc-115">Izmantojiet rindas opciju **Pievienot**, lai pievienotu rindas.</span><span class="sxs-lookup"><span data-stu-id="c6acc-115">Use the **Add** line option to add lines.</span></span> <span data-ttu-id="c6acc-116">Noklikšķiniet uz **Izkārtojumi**, lai skatītu budžeta plāna dokumenta izkārtojuma konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="c6acc-116">Click **Layouts** to view the budget plan document layout configuration.</span></span> 

  <span data-ttu-id="c6acc-117">[![Budžeta plānu pievienošana](./media/bpt2-1024x274.png)](./media/bpt2.png)</span><span class="sxs-lookup"><span data-stu-id="c6acc-117">[![Budget plans add](./media/bpt2-1024x274.png)](./media/bpt2.png)</span></span> 

<span data-ttu-id="c6acc-118">Izkārtojuma konfigurāciju varat pārskatīt un pēc nepieciešamības koriģēt.</span><span class="sxs-lookup"><span data-stu-id="c6acc-118">You can review the layout configuration and adjust it as needed.</span></span> 
1. <span data-ttu-id="c6acc-119">Dodieties uz **Veidne** &gt; **Ģenerēt**, lai izveidotu Excel failu šim izkārtojumam.</span><span class="sxs-lookup"><span data-stu-id="c6acc-119">Go to **Template** &gt; **Generate** to create an Excel file for this layout.</span></span> 
2. <span data-ttu-id="c6acc-120">Kad veidne ir ģenerēta, pārejiet uz **Veidne** &gt; **Skatīt**, lai atvērtu un pārskatītu budžeta plāna dokumenta veidni.</span><span class="sxs-lookup"><span data-stu-id="c6acc-120">After the template is generated, go to **Template** &gt; **View** to open and review the budget plan document template.</span></span> <span data-ttu-id="c6acc-121">Šo Excel failu varat saglabāt lokālajā diskā.</span><span class="sxs-lookup"><span data-stu-id="c6acc-121">You can save the Excel file to your local drive.</span></span> 

<span data-ttu-id="c6acc-122">[![Saglabāt kā](./media/bpt3-1024x545.png)](./media/bpt3.png)</span><span class="sxs-lookup"><span data-stu-id="c6acc-122">[![Save as](./media/bpt3-1024x545.png)](./media/bpt3.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="c6acc-123">Kad ar budžeta plāna dokumenta izkārtojumu ir saistīta Excel veidne, šo izkārtojumu vairs nevar rediģēt.</span><span class="sxs-lookup"><span data-stu-id="c6acc-123">The Budget plan document layout cannot be edited after an Excel template is associated with it.</span></span> <span data-ttu-id="c6acc-124">Lai izkārtojumu modificētu, izdzēsiet piesaistītās Excel veidnes failu un ģenerējiet to no jauna.</span><span class="sxs-lookup"><span data-stu-id="c6acc-124">To modify the layout, delete the associated Excel template file and regenerate it.</span></span> <span data-ttu-id="c6acc-125">Tas ir nepieciešams tādēļ, lai izkārtojuma un darblapas lauki būtu sinhronizēti.</span><span class="sxs-lookup"><span data-stu-id="c6acc-125">This is required to keep the fields in the layout and the worksheet synchronized.</span></span> 

<span data-ttu-id="c6acc-126">Excel veidnē būs visi elementi no budžeta plāna dokumenta izkārtojuma, kur kolonnas **Pieejams darblapā** vērtība ir iestatīta uz Patiess.</span><span class="sxs-lookup"><span data-stu-id="c6acc-126">The Excel template will contain all of the elements from the budget plan document layout, where the **Available in Worksheet** column is set to True.</span></span> <span data-ttu-id="c6acc-127">Excel veidnē nav atļauta elementu pārklāšanās.</span><span class="sxs-lookup"><span data-stu-id="c6acc-127">Overlapping elements are not allowed in the Excel template.</span></span> <span data-ttu-id="c6acc-128">Piemēram, ja izkārtojumā ietilpst kolonnas Pieprasījums Q1, Pieprasījums Q2, Pieprasījums Q3 un Pieprasījums Q4, un kopīgā pieprasījuma kolonna, kas pārstāv visu četru ceturkšņu kolonnu summu, tad Excel veidnē lietošanai ir pieejamas tikai ceturkšņa kolonnas vai kopējā kolonna.</span><span class="sxs-lookup"><span data-stu-id="c6acc-128">For example, if the layout contains Request Q1, Request Q2, Request Q3, and Request Q4 columns, and a total request column that represents a sum of all 4 quarterly columns, only the quarterly columns or total column is available to be used in the Excel template.</span></span> <span data-ttu-id="c6acc-129">Atjaunināšanas laikā Excel fails nevar atjaunināt kolonnas, kas pārklājas, jo tabulā esošie dati varētu kļūt novecojuši vai neprecīzi.</span><span class="sxs-lookup"><span data-stu-id="c6acc-129">The Excel file cannot update overlapping columns during the update because data in the table could become out of date and inaccurate.</span></span>

<span data-ttu-id="c6acc-130">[![Paraugs](./media/bpt4-1024x615.png)](./media/bpt4.png)</span><span class="sxs-lookup"><span data-stu-id="c6acc-130">[![Example](./media/bpt4-1024x615.png)](./media/bpt4.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="c6acc-131">Lai nepieļautu iespējamas problēmas saistībā ar budžeta plāna datu skatīšanu un rediģēšanu, izmantojot programmu Excel, vienam un tam pašam lietotājam ir jāpiesakās gan programmatūras Microsoft Dynamics 365 for Finance and Operations izdevumā Enterprise, gan Microsoft Dynamics Office pievienojumprogrammā Datu savienotājs.</span><span class="sxs-lookup"><span data-stu-id="c6acc-131">To avoid potential issues with viewing and editing budget plan data using Excel, the same user should be logged into both Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and the Microsoft Dynamics Office Add-in Data Connector.</span></span>

## <a name="add-a-header-to-budget-plan-document-template"></a><span data-ttu-id="c6acc-132">Pievienot galveni budžeta plāna dokumenta veidnei</span><span class="sxs-lookup"><span data-stu-id="c6acc-132">Add a header to budget plan document template</span></span>
<span data-ttu-id="c6acc-133">Lai pievienotu galvenes informāciju, atlasiet augšējo rindu Excel failā un ievietojiet tukšas rindas.</span><span class="sxs-lookup"><span data-stu-id="c6acc-133">To add header information, select the top row in the Excel file and insert empty rows.</span></span> <span data-ttu-id="c6acc-134">Programmā **Datu savienotājs** noklikšķiniet uz **Dizains**, lai Excel failam pievienotu galvenes laukus.</span><span class="sxs-lookup"><span data-stu-id="c6acc-134">Click **Design** in the **Data Connector** to add header fields to the Excel file.</span></span>

<span data-ttu-id="c6acc-135">[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png)</span><span class="sxs-lookup"><span data-stu-id="c6acc-135">[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png)</span></span> 

<span data-ttu-id="c6acc-136">Cilnē **Dizains** noklikšķiniet uz **Pievienot laukus** un pēc tam kā elementa datu avotu atlasiet vienumu **BudgetPlanHeader**.</span><span class="sxs-lookup"><span data-stu-id="c6acc-136">In the **Design** tab, click **Add** fields, and then select **BudgetPlanHeader** as the entity data source.</span></span>

<span data-ttu-id="c6acc-137">[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)</span><span class="sxs-lookup"><span data-stu-id="c6acc-137">[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)</span></span>

<span data-ttu-id="c6acc-138">Ar kursoru norādiet uz vēlamo vietu Excel failā.</span><span class="sxs-lookup"><span data-stu-id="c6acc-138">Point the cursor to the desired location in the Excel file.</span></span> <span data-ttu-id="c6acc-139">Noklikšķiniet uz **Pievienot etiķeti**, lai atlasītajai vietai pievienotu lauka etiķeti.</span><span class="sxs-lookup"><span data-stu-id="c6acc-139">Click **Add label** to add the field label to the selected location.</span></span> <span data-ttu-id="c6acc-140">Atlasiet vienumu **Pievienot vērtību**, lai atlasītajai vietai pievienotu šo vērtības lauku.</span><span class="sxs-lookup"><span data-stu-id="c6acc-140">Select **Add Value** to add the value field to the selected place.</span></span> <span data-ttu-id="c6acc-141">Lai aizvērtu noformētāju, noklikšķiniet uz **Gatavs**.</span><span class="sxs-lookup"><span data-stu-id="c6acc-141">Click **Done** to close the designer.</span></span>

## <a name="bpt7mediabpt7pngmediabpt7png"></a><span data-ttu-id="c6acc-142">[![bpt7](./media/bpt7.png)](./media/bpt7.png)</span><span class="sxs-lookup"><span data-stu-id="c6acc-142">[![bpt7](./media/bpt7.png)](./media/bpt7.png)</span></span>

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a><span data-ttu-id="c6acc-143">Pievienot aprēķinātu kolonnu budžeta plāna dokumenta veidnes tabulai</span><span class="sxs-lookup"><span data-stu-id="c6acc-143">Add a calculated column to budget plan document template table</span></span>
--------------------------------------------------------------

<span data-ttu-id="c6acc-144">Pēc tam ģenerētajai budžeta plāna dokumenta veidnei tiks pievienotas aprēķinātas kolonnas.</span><span class="sxs-lookup"><span data-stu-id="c6acc-144">Next, calculated columns will be added to generated budget plan document template.</span></span> <span data-ttu-id="c6acc-145">Kolonna **Kopējais pieprasījums**, kurā ir kolonnu Pieprasījums Q1: Pieprasījums Q4 summa, un kolonna **Korekcija**, kas kolonnu **Kopējais pieprasījums** pārrēķina pēc sākotnēji definēta koeficienta.</span><span class="sxs-lookup"><span data-stu-id="c6acc-145">A **Total request** column, which summarizes Request Q1: Request Q4 columns, and an **Adjustment** column, which recalculates the **Total Request** column by a predefined factor.</span></span>

<span data-ttu-id="c6acc-146">Programmā **Datu savienotājs** noklikšķiniet uz **Dizains**, lai tabulai pievienotu kolonnas.</span><span class="sxs-lookup"><span data-stu-id="c6acc-146">Click **Design** in the **Data connector** to add columns to the table.</span></span> <span data-ttu-id="c6acc-147">Noklikšķiniet uz **Rediģēt** blakus datu avotam **BudgetPlanWorksheet**, lai sāktu pievienot kolonnas.</span><span class="sxs-lookup"><span data-stu-id="c6acc-147">Click **Edit** next to **BudgetPlanWorksheet** data source to start adding columns.</span></span>

<span data-ttu-id="c6acc-148">[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png)</span><span class="sxs-lookup"><span data-stu-id="c6acc-148">[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png)</span></span> 

<span data-ttu-id="c6acc-149">Atlasītajā lauku grupā tiek rādītas veidnē pieejamās kolonnas.</span><span class="sxs-lookup"><span data-stu-id="c6acc-149">The selected field group displays the columns that are available in the template.</span></span> <span data-ttu-id="c6acc-150">Noklikšķiniet uz **Formula**, lai pievienotu jaunu kolonnu.</span><span class="sxs-lookup"><span data-stu-id="c6acc-150">Click **Formula** to add a new column.</span></span> <span data-ttu-id="c6acc-151">Jaunajai kolonnai piešķiriet nosaukumu un pēc tam ielīmējiet formulu laukā **Formula**.</span><span class="sxs-lookup"><span data-stu-id="c6acc-151">Name the new column and then paste the formula into the **Formula** field.</span></span> <span data-ttu-id="c6acc-152">Noklikšķiniet uz **Atjaunināt**, lai šo kolonnu ievietotu.</span><span class="sxs-lookup"><span data-stu-id="c6acc-152">Click **Update** to insert the column.</span></span>

<span data-ttu-id="c6acc-153">[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)</span><span class="sxs-lookup"><span data-stu-id="c6acc-153">[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="c6acc-154">Lai formulu definētu, izveidojiet šo formulu izklājlapā un pēc tam to iekopējiet logā **Dizains**.</span><span class="sxs-lookup"><span data-stu-id="c6acc-154">To define the formula, create the formula in the spreadsheet, and then copy it to the **Design** window.</span></span> <span data-ttu-id="c6acc-155">Ar programmatūru Dynamics 365 for Finance and Operations saistītai tabulai parasti tiek piešķirts nosaukums “AXTable1”.</span><span class="sxs-lookup"><span data-stu-id="c6acc-155">A Finance and Operations bound table will typically be named "AXTable1".</span></span> <span data-ttu-id="c6acc-156">Piemēram, lai izklājlapā apkopotu kolonnas Pieprasījums Q1 : Pieprasījums Q4, tiek izmantota formula = AxTable1\[Pieprasījums Q1\]+AxTable1\[Pieprasījums Q2\]+AxTable1\[Pieprasījums Q3\]+AxTable1\[Pieprasījums Q4\].</span><span class="sxs-lookup"><span data-stu-id="c6acc-156">For example, to summarize Request Q1 : Request Q4 columns in the spreadsheet, the formula = AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\].</span></span>

<span data-ttu-id="c6acc-157">Atkārtojiet šīs darbības, lai ievietotu kolonnu **Korekcija**.</span><span class="sxs-lookup"><span data-stu-id="c6acc-157">Repeat these steps to insert the **Adjustment** column.</span></span> <span data-ttu-id="c6acc-158">Šai kolonnai izmantojiet formulu = AxTable1\[Kopējais pieprasījums\]\*$I$1.</span><span class="sxs-lookup"><span data-stu-id="c6acc-158">Use formula = AxTable1\[Total request\]\*$I$1 for this column.</span></span> <span data-ttu-id="c6acc-159">Šādi šūnā I1 esošā vērtība tiks izmantota reizināšanai ar vērtībām kolonnā **Kopējais pieprasījums**, lai aprēķinātu korekcijas summas.</span><span class="sxs-lookup"><span data-stu-id="c6acc-159">This will take the value in cell I1 and multiply the values in the **Total request** column to calculate adjustment amounts.</span></span>

<span data-ttu-id="c6acc-160">Saglabājiet un aizveriet Excel failu.</span><span class="sxs-lookup"><span data-stu-id="c6acc-160">Save and close the Excel file.</span></span> <span data-ttu-id="c6acc-161">Atgriezieties programmatūrā Dynamics 365 for Finance and Operations un sadaļā **Izkārtojumi** noklikšķiniet uz **Veidne &gt; Augšupielādēt**, lai saglabāto Excel veidni augšupielādētu lietošanai budžeta plānā.</span><span class="sxs-lookup"><span data-stu-id="c6acc-161">Return to Finance and Operations, and in **Layouts**, click **Template &gt; Upload** to upload the saved Excel template to be used for the budget plan.</span></span> 

<span data-ttu-id="c6acc-162">[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png)</span><span class="sxs-lookup"><span data-stu-id="c6acc-162">[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png)</span></span> 

<span data-ttu-id="c6acc-163">Aizvediet slīdni **Izkārtojumi**.</span><span class="sxs-lookup"><span data-stu-id="c6acc-163">Close the **Layouts** slider.</span></span> <span data-ttu-id="c6acc-164">Dokumentā **Budžeta plāns** noklikšķiniet uz **Darblapa**, lai dokumentu skatītu un rediģētu programmā Excel.</span><span class="sxs-lookup"><span data-stu-id="c6acc-164">In **Budget plan** document, click **Worksheet** to view and edit the document in Excel.</span></span> <span data-ttu-id="c6acc-165">Ņemiet vērā, ka koriģētā Excel veidne tika izmantota, lai izveidotu šo budžeta plāna darblapu, un aprēķinātās kolonnas tiek atjauninātas, izmantojot iepriekšējās darbībās definētās formulas.</span><span class="sxs-lookup"><span data-stu-id="c6acc-165">Note that the adjusted Excel template was used to create this budget plan worksheet and calculated columns are updated using the formulas that were defined in the previous steps.</span></span> 

<span data-ttu-id="c6acc-166">[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)</span><span class="sxs-lookup"><span data-stu-id="c6acc-166">[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)</span></span>

## <a name="tips--tricks-for-creating-budget-plan-templates"></a><span data-ttu-id="c6acc-167">Padomi un ieteikumi par budžeta plāna veidņu izveidošanu</span><span class="sxs-lookup"><span data-stu-id="c6acc-167">Tips & tricks for creating budget plan templates</span></span>
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a><span data-ttu-id="c6acc-168">Vai budžeta plāna veidnei var pievienot un lietot papildu datu avotus?</span><span class="sxs-lookup"><span data-stu-id="c6acc-168">Can I add and use additional data sources to a budget plan template?</span></span>

<span data-ttu-id="c6acc-169">Jā, varat izmantot izvēlni **Dizains**, lai tai pašai vai citām Excel veidnes lapām pievienotu papildu elementus.</span><span class="sxs-lookup"><span data-stu-id="c6acc-169">Yes, you can use the **Design** menu to add additional entities to the same or other sheets in the Excel template.</span></span> <span data-ttu-id="c6acc-170">Varat, piemēram, pievienot datu avotu **BudgetPlanProposedProject**, lai izveidotu un uzturētu sarakstu ar piedāvātajiem projektiem, tajā pašā laikā strādājot ar budžeta plāna datiem programmā Excel.</span><span class="sxs-lookup"><span data-stu-id="c6acc-170">For example, you can add the **BudgetPlanProposedProject** data source to create and maintain a list of proposed projects at the same time when working with budget plan data in Excel.</span></span> <span data-ttu-id="c6acc-171">Ņemiet vēra, ka lielapjoma datu avotu iekļaušana var ietekmēt Excel darbgrāmatas veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="c6acc-171">Note that including high-volume data sources might impact performance of the Excel workbook.</span></span> 

<span data-ttu-id="c6acc-172">Programmā **Datu savienotājs** varat izmantot opciju **Filtrs**, lai papildu datu avotiem pievienotu vēlamos filtrus.</span><span class="sxs-lookup"><span data-stu-id="c6acc-172">You can use the **Filter** option in the **Data Connector** to add desired filters to additional data sources.</span></span>

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a><span data-ttu-id="c6acc-173">Vai programmā Datu savienotājs citiem lietotājiem varu slēpt opciju Dizains?</span><span class="sxs-lookup"><span data-stu-id="c6acc-173">Can I hide the Design option in the Data connector for other users?</span></span>

<span data-ttu-id="c6acc-174">Jā, atveriet programmas **Datu savienotājs** opcijas, lai opciju **Dizains** paslēptu no citiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="c6acc-174">Yes, open the **Data Connector** options to hide the **Design** option from other users.</span></span>

<span data-ttu-id="c6acc-175">[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)</span><span class="sxs-lookup"><span data-stu-id="c6acc-175">[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)</span></span>

<span data-ttu-id="c6acc-176">Izvērsiet sadaļu **Datu savienotāja opcijas** un noņemiet atzīmi izvēles rūtiņai **Iespējot dizainu**.</span><span class="sxs-lookup"><span data-stu-id="c6acc-176">Expand **Data connector options** and clear the **Enable design** check box.</span></span> <span data-ttu-id="c6acc-177">Šādi opcija **Dizains** tiks paslēpta no programmas **Datu savienotājs** loga.</span><span class="sxs-lookup"><span data-stu-id="c6acc-177">This will hide the **Design** option from the **Data connector**.</span></span>

<span data-ttu-id="c6acc-178">[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)</span><span class="sxs-lookup"><span data-stu-id="c6acc-178">[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)</span></span>

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a><span data-ttu-id="c6acc-179">Vai varu nepieļaut, ka lietotāji nejauši aizver datu savienotāju, kamēr strādā ar datiem?</span><span class="sxs-lookup"><span data-stu-id="c6acc-179">Can I prevent users from accidently closing the Data connector while working with data?</span></span>

<span data-ttu-id="c6acc-180">Ieteicams veidni bloķēt, lai nepieļautu, ka lietotāji to aizver.</span><span class="sxs-lookup"><span data-stu-id="c6acc-180">We recommend locking the template to prevent users from closing it.</span></span> <span data-ttu-id="c6acc-181">Lai ieslēgtu bloķēšanu, noklikšķiniet uz **Datu savienotājs**, un labā augšējā stūrī kļūst redzama bultiņa.</span><span class="sxs-lookup"><span data-stu-id="c6acc-181">To turn on the lock, click the **Data connector**, in the top right corner an arrow appears.</span></span> 

<span data-ttu-id="c6acc-182">[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png)</span><span class="sxs-lookup"><span data-stu-id="c6acc-182">[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png)</span></span> 

<span data-ttu-id="c6acc-183">Noklikšķiniet uz šīs bultiņas, lai atvērtu papildu izvēlni.</span><span class="sxs-lookup"><span data-stu-id="c6acc-183">Click the arrow for an additional menu.</span></span> <span data-ttu-id="c6acc-184">Atlasiet vienumu **Bloķēt**.</span><span class="sxs-lookup"><span data-stu-id="c6acc-184">Select **Lock**.</span></span>

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a><span data-ttu-id="c6acc-185">[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)</span><span class="sxs-lookup"><span data-stu-id="c6acc-185">[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)</span></span>

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a><span data-ttu-id="c6acc-186">Vai savām budžeta plāna veidnēm varu lietot citus Excel līdzekļus, piemēram, šūnu formatēšanu, krāsas, nosacījumformatēšanu un diagrammas?</span><span class="sxs-lookup"><span data-stu-id="c6acc-186">Can I use other Excel features, like cell formatting, colors, conditional formatting, and charts with my budget plan templates?</span></span>

<span data-ttu-id="c6acc-187">Jā, budžeta plāna veidnēs darbojas vairums Excel standarta iespēju.</span><span class="sxs-lookup"><span data-stu-id="c6acc-187">Yes, most of the standard Excel capabilities will work in budget plan templates.</span></span> <span data-ttu-id="c6acc-188">Ieteicams lietot krāsu kodējumu, lai tikai lasāmās kolonnas lietotāji varētu atšķirt no rediģējamajām.</span><span class="sxs-lookup"><span data-stu-id="c6acc-188">We recommend using color-coding for users to distinguish between read-only and editable columns.</span></span> <span data-ttu-id="c6acc-189">Nosacījumformatēšanu var izmantot, lai izceltu budžeta problemātiskos apgabalus.</span><span class="sxs-lookup"><span data-stu-id="c6acc-189">Conditional formatting can be used to highlight problematic areas of the budget.</span></span> <span data-ttu-id="c6acc-190">Kolonnu kopsummas var ērti attēlot, virs tabulas izmantojot Excel standarta formulas.</span><span class="sxs-lookup"><span data-stu-id="c6acc-190">Column totals can easily be presented by using standard Excel formulas above the table.</span></span>

<span data-ttu-id="c6acc-191">Varat arī izveidot un lietot rakurstabulas un diagrammas budžeta datu papildu grupēšanai un vizualizēšanai.</span><span class="sxs-lookup"><span data-stu-id="c6acc-191">You can also create and use pivot tables and charts for additional groupings and visualizations of budget data.</span></span> <span data-ttu-id="c6acc-192">Cilnē **Dati**, grupā **Savienojumi** noklikšķiniet uz **Atsvaidzināt visu** un pēc tam noklikšķiniet uz **Savienojuma rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="c6acc-192">On the **Data** tab, in the **Connections** group, click **Refresh All**, and then click **Connection Properties**.</span></span> <span data-ttu-id="c6acc-193">Noklikšķiniet uz cilnes **Lietojums**. Sadaļā **Atsvaidzināt** atzīmējiet izvēles rūtiņu **Atsvaidzināt datus faila atvēršanas laikā**.</span><span class="sxs-lookup"><span data-stu-id="c6acc-193">Click the **Usage** tab. Under **Refresh**, select the **Refresh data when opening the file** check box.</span></span> 

<span data-ttu-id="c6acc-194">[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)</span><span class="sxs-lookup"><span data-stu-id="c6acc-194">[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)</span></span>




