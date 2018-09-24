---
title: "Organizēt atskaites komponentus atskaišu veidotājā"
description: "Kad esat izveidojuši veidošanas blokus un ģenerējuši atskaites, ir noderīgi šos objektus sakārtot, lai lietotāji tos varētu vienkāršāk atrast. Šajā rakstā ir paskaidrots, kā sakārtot esošas atskaites, veidošanas blokus un objektus atskaišu veidotājā."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: c9772d45cf9d9941dd8fe0de13ce624ea3aa3b53
ms.contentlocale: lv-lv
ms.lasthandoff: 09/22/2018

---

# <a name="organize-report-components-in-report-designer"></a><span data-ttu-id="90a24-104">Organizēt atskaites komponentus atskaišu veidotājā</span><span class="sxs-lookup"><span data-stu-id="90a24-104">Organize report components in report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90a24-105">Kad esat izveidojuši veidošanas blokus un ģenerējuši atskaites, ir noderīgi šos objektus sakārtot, lai lietotāji tos varētu vienkāršāk atrast.</span><span class="sxs-lookup"><span data-stu-id="90a24-105">After you've designed building blocks and generated reports, it's helpful to organize these objects so that they are easier for users to locate.</span></span> <span data-ttu-id="90a24-106">Šajā rakstā ir paskaidrots, kā sakārtot esošas atskaites, veidošanas blokus un objektus atskaišu veidotājā.</span><span class="sxs-lookup"><span data-stu-id="90a24-106">This article explains how to organize existing reports, building blocks, and objects in report designer.</span></span>

<span data-ttu-id="90a24-107">Atskaišu veidotājā varat pārdēvēt mapes, atskaites, veidošanas blokus un citus objektus, lai palīdzētu kārtot savus failus.</span><span class="sxs-lookup"><span data-stu-id="90a24-107">You can rename folders, reports, building blocks, and other objects in report designer to help organize your files.</span></span> <span data-ttu-id="90a24-108">Atkarībā no pārdēvētā objekta tipa, iespējams, ir nepieciešams atjaunināt saistības ar šo objektu.</span><span class="sxs-lookup"><span data-stu-id="90a24-108">Depending on the type of object that you rename, you might have to update associations with that object.</span></span>

## <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="90a24-109">Pārdēvējiet mapi vai veidošanas bloku Pārskata veidotājā</span><span class="sxs-lookup"><span data-stu-id="90a24-109">Rename a folder or building block in Report Designer</span></span>
<span data-ttu-id="90a24-110">Pārskatu veidotājā varat pārdēvēt mapes, pārskatu definīcijas, rindu definīcijas, kolonnu definīcijas un pārskatu koku definīcijas.</span><span class="sxs-lookup"><span data-stu-id="90a24-110">In Report Designer, you can rename folders, report definitions, row definitions, column definitions, and reporting tree definitions.</span></span>

> [!NOTE]
> <span data-ttu-id="90a24-111">Kad pārdēvējat kādu veidošanas bloku, ir jāatjaunina visas atskaišu definīcijas, kas izmanto šo veidošanas bloku.</span><span class="sxs-lookup"><span data-stu-id="90a24-111">When you rename a building block, you must update any reporting definitions that use the building block.</span></span> <span data-ttu-id="90a24-112">Pretējā gadījumā nevar ģenerēt jaunu atskaiti.</span><span class="sxs-lookup"><span data-stu-id="90a24-112">Otherwise, a new report can't be generated.</span></span>

### <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="90a24-113">Pārdēvējiet mapi vai veidošanas bloku Pārskata veidotājā</span><span class="sxs-lookup"><span data-stu-id="90a24-113">Rename a folder or building block in Report Designer</span></span>

1. <span data-ttu-id="90a24-114">Pārskatu veidotājā, izmantojiet navigācijas rūti, lai atrastu mapi vai objektu pārdēvēšanai.</span><span class="sxs-lookup"><span data-stu-id="90a24-114">In Report Designer, use the navigation pane to locate the folder or object to rename.</span></span>
2. <span data-ttu-id="90a24-115">Ar peles labo pogu noklikšķiniet uz mapes vai objekta, un pēc tam noklikšķiniet uz **Pārdēvēt**.</span><span class="sxs-lookup"><span data-stu-id="90a24-115">Right-click the folder or object, and then click **Rename**.</span></span> <span data-ttu-id="90a24-116">Lauks **Nosaukums** navigācijas rūtī kļūst pieejams.</span><span class="sxs-lookup"><span data-stu-id="90a24-116">The **Name** field in the navigation pane becomes available.</span></span>
3. <span data-ttu-id="90a24-117">Ierakstiet jauno nosaukumu, un tad nospiediet taustiņu Enter.</span><span class="sxs-lookup"><span data-stu-id="90a24-117">Type a new name, and then press Enter.</span></span>
4. <span data-ttu-id="90a24-118">Ja veidošanas bloks ir rindas definīcija, kolonnas definīcija vai atskaišu koka definīcija, tad jums ir nepieciešams atjaunināt pārējos veidošanas blokus, kas ar to ir saistīti.</span><span class="sxs-lookup"><span data-stu-id="90a24-118">If the building block is a row definition, column definition, or reporting tree definition, you must update other building blocks that are associated with it.</span></span> <span data-ttu-id="90a24-119">Ar peles labo pogu noklikšķiniet uz veidošanas bloka, kuru pārdēvēt 3. darbībā, atlasiet vienumu **Saistības** un pēc tam sarakstā atlasiet vienumu, lai to atjauninātu.</span><span class="sxs-lookup"><span data-stu-id="90a24-119">Right-click the building block that you renamed in step 3, select **Associations**, and then select an item in the list to update it.</span></span>
5. <span data-ttu-id="90a24-120">Atkārtojiet 4. soli, līdz visi saistītie krājumi tiks atjaunināti.</span><span class="sxs-lookup"><span data-stu-id="90a24-120">Repeat step 4 until all associated items are updated.</span></span>

## <a name="create-and-manage-report-groups"></a><span data-ttu-id="90a24-121">Izveidojiet un pārvaldiet pārskatu grupas.</span><span class="sxs-lookup"><span data-stu-id="90a24-121">Create and manage report groups</span></span>
<span data-ttu-id="90a24-122">Pārskatu definīcijas iespējams grupēt, lai vienlaicīgi izveidotu vairākus pārskatus.</span><span class="sxs-lookup"><span data-stu-id="90a24-122">You can group report definitions to generate multiple reports at the same time.</span></span> <span data-ttu-id="90a24-123">Lai izveidotu, modificētu, dzēstu un ģenerētu atskaišu grupas, ir nepieciešama veidotāja vai administratora loma.</span><span class="sxs-lookup"><span data-stu-id="90a24-123">To create, modify, delete, and generate report groups, you must have the designer or administrator role.</span></span> <span data-ttu-id="90a24-124">Lietotāji, kam ir ģeneratora loma, var ģenerēt atskaišu grupas, kā arī atskaišu grupām var modificēt lietotāju atskaišu definīciju iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="90a24-124">Users who have the generator role can generate report groups and can also modify the user report definitions setting for report groups.</span></span>

### <a name="create-a-report-group"></a><span data-ttu-id="90a24-125">Pārskata grupas izveidošana</span><span class="sxs-lookup"><span data-stu-id="90a24-125">Create a report group</span></span>

1. <span data-ttu-id="90a24-126">Atskaišu veidotāja navigācijas rūtī noklikšķiniet uz **Atskaišu grupas**.</span><span class="sxs-lookup"><span data-stu-id="90a24-126">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="90a24-127">Izvēlnē **Fails** noklikšķiniet uz **Jauns** &gt; **Pārskatu grupas definīcija**, lai skatītāja logā atvērtu jaunu pārskatu grupu.</span><span class="sxs-lookup"><span data-stu-id="90a24-127">On the **File** menu, click **New** &gt; **Report Group Definition** to open a new report group in the viewer window.</span></span> <span data-ttu-id="90a24-128">Varat arī noklikšķināt uz rīkjoslas pogas **Pārskatu grupa** ![Pārskatu grupa](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Pārskatu grupa").</span><span class="sxs-lookup"><span data-stu-id="90a24-128">Alternatively, click the **Report Group** button ![Report Group](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Report Group") on the toolbar.</span></span>
3. <span data-ttu-id="90a24-129">Noklikšķiniet uz cilnes **Pārskatu grupa**. Lai šī pārskata izveidošanai ignorētu informāciju par atsevišķu pārskatu definīcijām, atzīmējiet izvēles rūtiņu **Ignorēt uzņēmuma, detalizētas informācijas un datuma iestatījumus no atsevišķām pārskatu definīcijām**.</span><span class="sxs-lookup"><span data-stu-id="90a24-129">Click the **Report Group** tab. To override the information on the individual report definitions for the generation of this report, select the **Override company, detail, and date settings from individual report definitions** check box.</span></span> <span data-ttu-id="90a24-130">Uzņēmuma nosaukums, detalizētības līmenis, provizoriskie iestatījumi un datuma informācija tiek ievadīta automātiski, bet jūs varat veikt atjauninājumus.</span><span class="sxs-lookup"><span data-stu-id="90a24-130">The company name, detail level, provisional setting, and date information are entered automatically, but you can make updates.</span></span>
4. <span data-ttu-id="90a24-131">Lai ģenerētu vairākas atskaites, kurās ir redzamas atskaišu valūtas, atzīmējiet izvēles rūtiņu **Ietvert visas atskaišu valūtas**.</span><span class="sxs-lookup"><span data-stu-id="90a24-131">To generate multiple reports that show the reporting currencies, select the **Include all reporting currencies** check box.</span></span> <span data-ttu-id="90a24-132">Pēc tam varat piekļūt vairākiem skatiem, tīmekļa skatītājā noklikšķinot uz pogas **Valūta**, kas skatāt šo atskaiti.</span><span class="sxs-lookup"><span data-stu-id="90a24-132">You can then access multiple views by clicking the **Currency** button in the Web Viewer when you view the report.</span></span>
5. <span data-ttu-id="90a24-133">Laukā **Atskaites grupā** noklikšķiniet uz **Pievienot**, lai atlasītu atskaites, ko iekļaut atskaišu grupā.</span><span class="sxs-lookup"><span data-stu-id="90a24-133">In the **Reports in group** field, click **Add** to select the reports to include in the report group.</span></span> <span data-ttu-id="90a24-134">Lai dialoglodziņā **Pievienot** atlasītu vairākas atskaites, atskaišu atlasīšanas laikā turiet nospiestu taustiņu Ctrl.</span><span class="sxs-lookup"><span data-stu-id="90a24-134">To select multiple reports in the **Add** dialog box, hold down the Ctrl key while you select reports.</span></span> <span data-ttu-id="90a24-135">Kad esat beidzis atlasīt atskaites, noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="90a24-135">When you've finished selecting reports, click **OK**.</span></span>
6. <span data-ttu-id="90a24-136">Noklikšķiniet uz **Fails** &gt; **Saglabāt**, lai saglabātu jauno pārskatu grupu.</span><span class="sxs-lookup"><span data-stu-id="90a24-136">Click **File** &gt; **Save** to save the new report group.</span></span>

### <a name="modify-a-report-group"></a><span data-ttu-id="90a24-137">Modificēt pārskata grupu</span><span class="sxs-lookup"><span data-stu-id="90a24-137">Modify a report group</span></span>

1. <span data-ttu-id="90a24-138">Atskaišu veidotāja navigācijas rūtī noklikšķiniet uz **Atskaišu grupas**.</span><span class="sxs-lookup"><span data-stu-id="90a24-138">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="90a24-139">Veiciet dubultklikšķi uz pārskata grupas, lai modificētu to.</span><span class="sxs-lookup"><span data-stu-id="90a24-139">Double-click the report group to modify.</span></span>
3. <span data-ttu-id="90a24-140">Cilnē **Atskaišu grupa** veiciet nepieciešamās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="90a24-140">On the **Report Group** tab, make the changes that you want.</span></span>
4. <span data-ttu-id="90a24-141">Izvēlnē **Fails** noklikšķiniet uz **Saglabāt**, lai saglabātu modificēto pārskatu grupu, vai arī noklikšķiniet uz rīkjoslas pogas **Saglabāt** ![Saglabāt](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Saglabāt").</span><span class="sxs-lookup"><span data-stu-id="90a24-141">On the **File** menu, click **Save** to save the modified report group, Alternatively, click the **Save** button ![Save](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Save") on the toolbar.</span></span>

> <span data-ttu-id="90a24-142">[PIEZĪME] Ja esat ieplānojis atskaites, lai tās tiktu ģenerētas noteiktos intervālos, varat ignorēt šos iestatījumus un ģenerēt atskaiti nekavējoties.</span><span class="sxs-lookup"><span data-stu-id="90a24-142">[NOTE] If you've scheduled reports so that they are generated at set intervals, you can override those settings and generate a report immediately.</span></span>

### <a name="generate-a-report-group-report"></a><span data-ttu-id="90a24-143">Izveidot pārskata grupu pārskatu</span><span class="sxs-lookup"><span data-stu-id="90a24-143">Generate a report group report</span></span>

1. <span data-ttu-id="90a24-144">Atskaišu veidotāja navigācijas rūtī noklikšķiniet uz **Atskaišu grupas**.</span><span class="sxs-lookup"><span data-stu-id="90a24-144">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="90a24-145">Atveriet pārskata grupu, lai izveidotu.</span><span class="sxs-lookup"><span data-stu-id="90a24-145">Open the report group to generate.</span></span>
3. <span data-ttu-id="90a24-146">Noklikšķiniet uz pogas **Ģenerēt pārskatu** ![Ģenerēt pārskatu](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Ģenerēt pārskatu"), lai ģenerētu pārskatus.</span><span class="sxs-lookup"><span data-stu-id="90a24-146">Click the **Generate Report** button ![Generate Report](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Generate Report") to generate reports.</span></span>

### <a name="delete-a-report-group"></a><span data-ttu-id="90a24-147">Grupas pārskata dzēšana</span><span class="sxs-lookup"><span data-stu-id="90a24-147">Delete a report group</span></span>

1. <span data-ttu-id="90a24-148">Atskaišu veidotāja navigācijas rūtī noklikšķiniet uz **Atskaišu grupas**.</span><span class="sxs-lookup"><span data-stu-id="90a24-148">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="90a24-149">Ar peles labo pogu noklikšķiniet uz dzēšamās atskaišu grupas un pēc tam atlasiet vienumu **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="90a24-149">Right-click the report group to delete, and then select **Delete**.</span></span>
3. <span data-ttu-id="90a24-150">Kad tiek parādīts apstiprinājuma ziņojums, noklikšķiniet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="90a24-150">When a confirmation message appears, click **Yes**.</span></span>

## <a name="report-group-tab-controls"></a><span data-ttu-id="90a24-151">Atskaišu grupas cilnes vadīklas</span><span class="sxs-lookup"><span data-stu-id="90a24-151">Report Group tab controls</span></span>
<span data-ttu-id="90a24-152">Nākamajā tabulā ir aprakstītas vadīklas cilnē **Atskaišu grupa**.</span><span class="sxs-lookup"><span data-stu-id="90a24-152">The following table describes the controls on the **Report Group** tab.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="90a24-153">Kontrole</span><span class="sxs-lookup"><span data-stu-id="90a24-153">Control</span></span></th>
<th><span data-ttu-id="90a24-154">Apraksts</span><span class="sxs-lookup"><span data-stu-id="90a24-154">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90a24-155">Atsevišķu pārskatu definīcijās ignorēt uzņēmuma, detalizētas informācijas un datuma iestatījumus</span><span class="sxs-lookup"><span data-stu-id="90a24-155">Override company, detail, and date settings from individual report definitions</span></span></td>
<td><span data-ttu-id="90a24-156">Atlasiet šo izvēles rūtiņu, lai ignorētu atsevišķu pārskatu definīcijas šajā pārskata grupā, tikai šo pārskatu veidošanai.</span><span class="sxs-lookup"><span data-stu-id="90a24-156">Select this check box to override individual report definitions of the reports in this report group for the generation of these reports only.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90a24-157">Uzņēmuma nosaukums</span><span class="sxs-lookup"><span data-stu-id="90a24-157">Company name</span></span></td>
<td><span data-ttu-id="90a24-158">Atlasiet kompāniju, kas jāizmanto pārskatos.</span><span class="sxs-lookup"><span data-stu-id="90a24-158">Select the company to use for the reports.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90a24-159">Detalizācijas līmenis</span><span class="sxs-lookup"><span data-stu-id="90a24-159">Detail level</span></span></td>
<td><span data-ttu-id="90a24-160">Norādiet detalizētības līmeni, kāds ir iekļauts atskaitēs.</span><span class="sxs-lookup"><span data-stu-id="90a24-160">Specify the level of detail that the reports include.</span></span>
<ul>
<li><span data-ttu-id="90a24-161"><strong>Finanšu</strong> — augstākā līmeņa kopsavilkuma pārskats.</span><span class="sxs-lookup"><span data-stu-id="90a24-161"><strong>Financial</strong> − A high-level summary report.</span></span> <span data-ttu-id="90a24-162">Jūs nevarat rakties līdz kontiem un dimensijām, izņemot tos kontus un dimensijas, kas ir pievienoti, izmantojot atskaišu koku.</span><span class="sxs-lookup"><span data-stu-id="90a24-162">You can&#39;t drill down to accounts and dimensions, except for those accounts and dimensions that have been added through a reporting tree.</span></span></li>
<li><span data-ttu-id="90a24-163"><strong>Finanšu un Konts</strong> — pārskats, kas satur augsta līmeņa kopsavilkumu un detalizētu informāciju par kontu.</span><span class="sxs-lookup"><span data-stu-id="90a24-163"><strong>Financial &amp; Account</strong> − A report that contains a high-level summary and account details.</span></span></li>
<li><span data-ttu-id="90a24-164"><strong>Finanšu, Konts un Transakcija</strong> — pārskats, kas satur augsta līmeņa kopsavilkumu un detalizētu informāciju par transakciju.</span><span class="sxs-lookup"><span data-stu-id="90a24-164"><strong>Financial, Account, &amp; Transaction</strong> − A report that contains a high-level summary and transaction details.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="90a24-165">Provizorisks</span><span class="sxs-lookup"><span data-stu-id="90a24-165">Provisional</span></span></td>
<td><span data-ttu-id="90a24-166">Norādiet aktivitāšu tipus, kas ir iekļauti atskaitēs.</span><span class="sxs-lookup"><span data-stu-id="90a24-166">Specify the types of activity that the reports include.</span></span>
<ul>
<li><span data-ttu-id="90a24-167"><strong>Tikai grāmatotās darbības</strong> — ietverti tikai darījumi un bilances, kas ir grāmatoti jūsu finanšu datos.</span><span class="sxs-lookup"><span data-stu-id="90a24-167"><strong>Posted activity only</strong> − Include only the transactions and balances that are posted in your financial data.</span></span></li>
<li><span data-ttu-id="90a24-168"><strong>Grāmatotās un negrāmatotās darbības</strong> — ietverti visi darījumi un bilances, kas ir ievadīti un grāmatoti jūsu finanšu datos.</span><span class="sxs-lookup"><span data-stu-id="90a24-168"><strong>Posted and unposted activity</strong> − Include all the transactions and balances that are entered and posted in your financial data.</span></span></li>
<li><span data-ttu-id="90a24-169"><strong>Tikai negrāmatotās darbības</strong> — ietverti tikai tie darījumi, kuri ir ievadīti, bet vēl nav iegrāmatoti jūsu finanšu datos.</span><span class="sxs-lookup"><span data-stu-id="90a24-169"><strong>Unposted activity only</strong> − Include only the transactions that are entered, but not yet posted, in your financial data.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="90a24-170">Iekļaut visas pārskatu veidošanas valūtas</span><span class="sxs-lookup"><span data-stu-id="90a24-170">Include all reporting currencies</span></span></td>
<td><span data-ttu-id="90a24-171">Šeit ir uzskaitītas visas papildu atskaišu valūtas, kas ir konfigurētas jūsu Microsoft Dynamics ERP sistēmā.</span><span class="sxs-lookup"><span data-stu-id="90a24-171">Any additional reporting currencies that are configured in your Microsoft Dynamics ERP system are listed here.</span></span> <span data-ttu-id="90a24-172">Atzīmējiet šo izvēles rūtiņu, lai ģenerētu papildu atskaites norādītajās valūtās.</span><span class="sxs-lookup"><span data-stu-id="90a24-172">Select this check box to generate additional reports in the currencies that are indicated.</span></span> <span data-ttu-id="90a24-173">Lai skatītu šos pārskatus, pakalpojumā Tīmekļa skatītājs noklikšķiniet uz pogas <strong>Valūta</strong> un pēc tam atlasiet valūtu.</span><span class="sxs-lookup"><span data-stu-id="90a24-173">To view these reports in the Web Viewer, click the <strong>Currency</strong> button, and then select a currency.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90a24-174">Datuma informācija netiek saglabāta ar pārskata definīciju</span><span class="sxs-lookup"><span data-stu-id="90a24-174">Date information not saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="90a24-175">Bāzes periods</span><span class="sxs-lookup"><span data-stu-id="90a24-175">Base period</span></span></li>
<li><span data-ttu-id="90a24-176">Bāzes gads</span><span class="sxs-lookup"><span data-stu-id="90a24-176">Base year</span></span></li>
<li><span data-ttu-id="90a24-177">Ietvertais periods</span><span class="sxs-lookup"><span data-stu-id="90a24-177">Period covered</span></span></li>
</ul>
<span data-ttu-id="90a24-178">Ar atskaites definīciju tiek saglabāti tikai noklusējuma bāzes perioda iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="90a24-178">Only default base period settings are saved with the report definition.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90a24-179">Datuma informācija tiek saglabāta ar pārskata definīciju</span><span class="sxs-lookup"><span data-stu-id="90a24-179">Date information saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="90a24-180">Pārskata datums</span><span class="sxs-lookup"><span data-stu-id="90a24-180">Report date</span></span></li>
<li><span data-ttu-id="90a24-181">Noklusējuma bāzes periods</span><span class="sxs-lookup"><span data-stu-id="90a24-181">Default base period</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="90a24-182">Pārskati grupā</span><span class="sxs-lookup"><span data-stu-id="90a24-182">Reports in group</span></span></td>
<td><span data-ttu-id="90a24-183">Pievienot, noņemt un atkārtoti pasūtīt pārskatus pārskata grupā.</span><span class="sxs-lookup"><span data-stu-id="90a24-183">Add, remove, and re-order reports in the report group.</span></span>
<ul>
<li><span data-ttu-id="90a24-184">Lai pārskatu grupai pievienotu pārskatu definīcijas, atveriet pārskatu grupu, veicot dubultklikšķi uz tās, un pēc tam noklikšķiniet uz <strong>Pievienot</strong>.</span><span class="sxs-lookup"><span data-stu-id="90a24-184">To add report definitions to the report group, double-click the report group to open it, and then click <strong>Add</strong>.</span></span> <span data-ttu-id="90a24-185">Atlasiet pārskatu grupai pievienojamos pārskatus un pēc tam noklikšķiniet uz <strong>Labi</strong>.</span><span class="sxs-lookup"><span data-stu-id="90a24-185">Select the reports to include in the report group, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="90a24-186">Lai no pārskatu grupas noņemtu pārskatu, atlasiet vēlamo pārskatu un pēc tam noklikšķiniet uz <strong>Noņemt</strong>.</span><span class="sxs-lookup"><span data-stu-id="90a24-186">To remove a report from the report group, select it, and then click <strong>Remove</strong>.</span></span></li>
<li><span data-ttu-id="90a24-187">Lai mainītu secību, kādā atskaites tiek ģenerētas, sarakstā atlasiet kādu atskaiti un pēc tam noklikšķiniet uz <strong>Pārvietot uz augšu</strong> vai <strong>Pārvietot uz leju</strong>.</span><span class="sxs-lookup"><span data-stu-id="90a24-187">To modify the order that the reports are generated in, select a report in the list, and then click <strong>Move up</strong> or <strong>Move down</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="90a24-188">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="90a24-188">Additional resources</span></span>

[<span data-ttu-id="90a24-189">Finanšu pārskati</span><span class="sxs-lookup"><span data-stu-id="90a24-189">Financial reporting</span></span>](financial-reporting-intro.md)

