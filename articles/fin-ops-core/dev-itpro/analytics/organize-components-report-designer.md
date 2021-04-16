---
title: Pārskatu komponentu organizēšana pārskatu noformētājā
description: Šajā rakstā ir paskaidrots, kā sakārtot esošas atskaites, veidošanas blokus un objektus atskaišu veidotājā.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cb3e09ad849b250ed3f1d7aec910b44d591cb88e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751636"
---
# <a name="organize-report-components-in-report-designer"></a><span data-ttu-id="24cbf-103">Organizēt atskaites komponentus atskaišu veidotājā</span><span class="sxs-lookup"><span data-stu-id="24cbf-103">Organize report components in report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24cbf-104">Kad esat izveidojuši veidošanas blokus un ģenerējuši atskaites, ir noderīgi šos objektus sakārtot, lai lietotāji tos varētu vienkāršāk atrast.</span><span class="sxs-lookup"><span data-stu-id="24cbf-104">After you've designed building blocks and generated reports, it's helpful to organize these objects so that they are easier for users to locate.</span></span> <span data-ttu-id="24cbf-105">Šajā rakstā ir paskaidrots, kā sakārtot esošas atskaites, veidošanas blokus un objektus atskaišu veidotājā.</span><span class="sxs-lookup"><span data-stu-id="24cbf-105">This article explains how to organize existing reports, building blocks, and objects in report designer.</span></span>

<span data-ttu-id="24cbf-106">Atskaišu veidotājā varat pārdēvēt mapes, atskaites, veidošanas blokus un citus objektus, lai palīdzētu kārtot savus failus.</span><span class="sxs-lookup"><span data-stu-id="24cbf-106">You can rename folders, reports, building blocks, and other objects in report designer to help organize your files.</span></span> <span data-ttu-id="24cbf-107">Atkarībā no pārdēvētā objekta tipa, iespējams, ir nepieciešams atjaunināt saistības ar šo objektu.</span><span class="sxs-lookup"><span data-stu-id="24cbf-107">Depending on the type of object that you rename, you might have to update associations with that object.</span></span>

## <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="24cbf-108">Pārdēvējiet mapi vai veidošanas bloku Pārskata veidotājā</span><span class="sxs-lookup"><span data-stu-id="24cbf-108">Rename a folder or building block in Report Designer</span></span>
<span data-ttu-id="24cbf-109">Pārskatu veidotājā varat pārdēvēt mapes, pārskatu definīcijas, rindu definīcijas, kolonnu definīcijas un pārskatu koku definīcijas.</span><span class="sxs-lookup"><span data-stu-id="24cbf-109">In Report Designer, you can rename folders, report definitions, row definitions, column definitions, and reporting tree definitions.</span></span>

### <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="24cbf-110">Mapes vai veidošanas bloka pārdēvēšana pārskatu veidotājā</span><span class="sxs-lookup"><span data-stu-id="24cbf-110">Rename a folder or building block in Report Designer</span></span>

1. <span data-ttu-id="24cbf-111">Pārskatu veidotājā izmantojiet navigācijas rūti, lai atrastu pārdēvējamo mapi vai objektu.</span><span class="sxs-lookup"><span data-stu-id="24cbf-111">In Report Designer, use the navigation pane to locate the folder or object to rename.</span></span>
2. <span data-ttu-id="24cbf-112">Ar peles labo pogu noklikšķiniet uz mapes vai objekta, un pēc tam noklikšķiniet uz **Pārdēvēt**.</span><span class="sxs-lookup"><span data-stu-id="24cbf-112">Right-click the folder or object, and then click **Rename**.</span></span> <span data-ttu-id="24cbf-113">Lauks **Nosaukums** navigācijas rūtī kļūst pieejams.</span><span class="sxs-lookup"><span data-stu-id="24cbf-113">The **Name** field in the navigation pane becomes available.</span></span>
3. <span data-ttu-id="24cbf-114">Ierakstiet jauno nosaukumu, un tad nospiediet taustiņu Enter.</span><span class="sxs-lookup"><span data-stu-id="24cbf-114">Type a new name, and then press Enter.</span></span>
4. <span data-ttu-id="24cbf-115">Ja veidošanas bloks ir rindas definīcija, kolonnas definīcija vai atskaišu koka definīcija, tad jums ir nepieciešams atjaunināt pārējos veidošanas blokus, kas ar to ir saistīti.</span><span class="sxs-lookup"><span data-stu-id="24cbf-115">If the building block is a row definition, column definition, or reporting tree definition, you must update other building blocks that are associated with it.</span></span> <span data-ttu-id="24cbf-116">Ar peles labo pogu noklikšķiniet uz veidošanas bloka, kuru pārdēvēt 3. darbībā, atlasiet vienumu **Saistības** un pēc tam sarakstā atlasiet vienumu, lai to atjauninātu.</span><span class="sxs-lookup"><span data-stu-id="24cbf-116">Right-click the building block that you renamed in step 3, select **Associations**, and then select an item in the list to update it.</span></span>
5. <span data-ttu-id="24cbf-117">Atkārtojiet 4. soli, līdz visi saistītie krājumi tiks atjaunināti.</span><span class="sxs-lookup"><span data-stu-id="24cbf-117">Repeat step 4 until all associated items are updated.</span></span>

## <a name="create-and-manage-report-groups"></a><span data-ttu-id="24cbf-118">Izveidojiet un pārvaldiet pārskatu grupas.</span><span class="sxs-lookup"><span data-stu-id="24cbf-118">Create and manage report groups</span></span>
<span data-ttu-id="24cbf-119">Pārskatu definīcijas iespējams grupēt, lai vienlaicīgi izveidotu vairākus pārskatus.</span><span class="sxs-lookup"><span data-stu-id="24cbf-119">You can group report definitions to generate multiple reports at the same time.</span></span> <span data-ttu-id="24cbf-120">Lai izveidotu, modificētu, dzēstu un ģenerētu atskaišu grupas, ir nepieciešama veidotāja vai administratora loma.</span><span class="sxs-lookup"><span data-stu-id="24cbf-120">To create, modify, delete, and generate report groups, you must have the designer or administrator role.</span></span> <span data-ttu-id="24cbf-121">Lietotāji, kam ir ģeneratora loma, var ģenerēt atskaišu grupas, kā arī atskaišu grupām var modificēt lietotāju atskaišu definīciju iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="24cbf-121">Users who have the generator role can generate report groups and can also modify the user report definitions setting for report groups.</span></span>

### <a name="create-a-report-group"></a><span data-ttu-id="24cbf-122">Pārskata grupas izveidošana</span><span class="sxs-lookup"><span data-stu-id="24cbf-122">Create a report group</span></span>

1. <span data-ttu-id="24cbf-123">Atskaišu veidotāja navigācijas rūtī noklikšķiniet uz **Atskaišu grupas**.</span><span class="sxs-lookup"><span data-stu-id="24cbf-123">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="24cbf-124">Izvēlnē **Fails** noklikšķiniet uz **Jauns** &gt; **Pārskatu grupas definīcija**, lai skatītāja logā atvērtu jaunu pārskatu grupu.</span><span class="sxs-lookup"><span data-stu-id="24cbf-124">On the **File** menu, click **New** &gt; **Report Group Definition** to open a new report group in the viewer window.</span></span> <span data-ttu-id="24cbf-125">Varat arī noklikšķināt uz rīkjoslas pogas **Pārskatu grupa** ![Pārskatu grupa](media/report-group.gif "Pārskatu grupa").</span><span class="sxs-lookup"><span data-stu-id="24cbf-125">Alternatively, click the **Report Group** button ![Report Group](media/report-group.gif "Report Group") on the toolbar.</span></span>
3. <span data-ttu-id="24cbf-126">Noklikšķiniet uz cilnes **Pārskatu grupa**. Lai šī pārskata izveidošanai ignorētu informāciju par atsevišķu pārskatu definīcijām, atzīmējiet izvēles rūtiņu **Ignorēt uzņēmuma, detalizētas informācijas un datuma iestatījumus no atsevišķām pārskatu definīcijām**.</span><span class="sxs-lookup"><span data-stu-id="24cbf-126">Click the **Report Group** tab. To override the information on the individual report definitions for the generation of this report, select the **Override company, detail, and date settings from individual report definitions** check box.</span></span> <span data-ttu-id="24cbf-127">Uzņēmuma nosaukums, detalizētības līmenis, provizoriskie iestatījumi un datuma informācija tiek ievadīta automātiski, bet jūs varat veikt atjauninājumus.</span><span class="sxs-lookup"><span data-stu-id="24cbf-127">The company name, detail level, provisional setting, and date information are entered automatically, but you can make updates.</span></span>
4. <span data-ttu-id="24cbf-128">Lai ģenerētu vairākas atskaites, kurās ir redzamas atskaišu valūtas, atzīmējiet izvēles rūtiņu **Ietvert visas atskaišu valūtas**.</span><span class="sxs-lookup"><span data-stu-id="24cbf-128">To generate multiple reports that show the reporting currencies, select the **Include all reporting currencies** check box.</span></span> <span data-ttu-id="24cbf-129">Pēc tam varat piekļūt vairākiem skatiem, tīmekļa skatītājā noklikšķinot uz pogas **Valūta**, kas skatāt šo atskaiti.</span><span class="sxs-lookup"><span data-stu-id="24cbf-129">You can then access multiple views by clicking the **Currency** button in the Web Viewer when you view the report.</span></span>
5. <span data-ttu-id="24cbf-130">Laukā **Atskaites grupā** noklikšķiniet uz **Pievienot**, lai atlasītu atskaites, ko iekļaut atskaišu grupā.</span><span class="sxs-lookup"><span data-stu-id="24cbf-130">In the **Reports in group** field, click **Add** to select the reports to include in the report group.</span></span> <span data-ttu-id="24cbf-131">Lai dialoglodziņā **Pievienot** atlasītu vairākas atskaites, atskaišu atlasīšanas laikā turiet nospiestu taustiņu Ctrl.</span><span class="sxs-lookup"><span data-stu-id="24cbf-131">To select multiple reports in the **Add** dialog box, hold down the Ctrl key while you select reports.</span></span> <span data-ttu-id="24cbf-132">Kad esat beidzis atlasīt atskaites, noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="24cbf-132">When you've finished selecting reports, click **OK**.</span></span>
6. <span data-ttu-id="24cbf-133">Noklikšķiniet uz **Fails** &gt; **Saglabāt**, lai saglabātu jauno pārskatu grupu.</span><span class="sxs-lookup"><span data-stu-id="24cbf-133">Click **File** &gt; **Save** to save the new report group.</span></span>

### <a name="modify-a-report-group"></a><span data-ttu-id="24cbf-134">Modificēt pārskata grupu</span><span class="sxs-lookup"><span data-stu-id="24cbf-134">Modify a report group</span></span>

1. <span data-ttu-id="24cbf-135">Atskaišu veidotāja navigācijas rūtī noklikšķiniet uz **Atskaišu grupas**.</span><span class="sxs-lookup"><span data-stu-id="24cbf-135">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="24cbf-136">Veiciet dubultklikšķi uz pārskata grupas, lai modificētu to.</span><span class="sxs-lookup"><span data-stu-id="24cbf-136">Double-click the report group to modify.</span></span>
3. <span data-ttu-id="24cbf-137">Cilnē **Atskaišu grupa** veiciet nepieciešamās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="24cbf-137">On the **Report Group** tab, make the changes that you want.</span></span>
4. <span data-ttu-id="24cbf-138">Izvēlnē **Fails** noklikšķiniet uz **Saglabāt**, lai saglabātu modificēto pārskatu grupu, vai arī noklikšķiniet uz rīkjoslas pogas **Saglabāt** ![Saglabāt](media/save.gif "Saglabāt").</span><span class="sxs-lookup"><span data-stu-id="24cbf-138">On the **File** menu, click **Save** to save the modified report group, Alternatively, click the **Save** button ![Save](media/save.gif "Save") on the toolbar.</span></span>

> <span data-ttu-id="24cbf-139">[PIEZĪME] Ja esat ieplānojis atskaites, lai tās tiktu ģenerētas noteiktos intervālos, varat ignorēt šos iestatījumus un ģenerēt atskaiti nekavējoties.</span><span class="sxs-lookup"><span data-stu-id="24cbf-139">[NOTE] If you've scheduled reports so that they are generated at set intervals, you can override those settings and generate a report immediately.</span></span>

### <a name="generate-a-report-group-report"></a><span data-ttu-id="24cbf-140">Izveidot pārskata grupu pārskatu</span><span class="sxs-lookup"><span data-stu-id="24cbf-140">Generate a report group report</span></span>

1. <span data-ttu-id="24cbf-141">Atskaišu veidotāja navigācijas rūtī noklikšķiniet uz **Atskaišu grupas**.</span><span class="sxs-lookup"><span data-stu-id="24cbf-141">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="24cbf-142">Atveriet pārskata grupu, lai izveidotu.</span><span class="sxs-lookup"><span data-stu-id="24cbf-142">Open the report group to generate.</span></span>
3. <span data-ttu-id="24cbf-143">Noklikšķiniet uz pogas **Ģenerēt pārskatu** ![Ģenerēt pārskatu](media/generate-report.gif "Ģenerēt pārskatu"), lai ģenerētu pārskatus.</span><span class="sxs-lookup"><span data-stu-id="24cbf-143">Click the **Generate Report** button ![Generate Report](media/generate-report.gif "Generate Report") to generate reports.</span></span>

### <a name="delete-a-report-group"></a><span data-ttu-id="24cbf-144">Grupas pārskata dzēšana</span><span class="sxs-lookup"><span data-stu-id="24cbf-144">Delete a report group</span></span>

1. <span data-ttu-id="24cbf-145">Atskaišu veidotāja navigācijas rūtī noklikšķiniet uz **Atskaišu grupas**.</span><span class="sxs-lookup"><span data-stu-id="24cbf-145">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="24cbf-146">Ar peles labo pogu noklikšķiniet uz dzēšamās atskaišu grupas un pēc tam atlasiet vienumu **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="24cbf-146">Right-click the report group to delete, and then select **Delete**.</span></span>
3. <span data-ttu-id="24cbf-147">Kad tiek parādīts apstiprinājuma ziņojums, noklikšķiniet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="24cbf-147">When a confirmation message appears, click **Yes**.</span></span>

## <a name="report-group-tab-controls"></a><span data-ttu-id="24cbf-148">Atskaišu grupas cilnes vadīklas</span><span class="sxs-lookup"><span data-stu-id="24cbf-148">Report Group tab controls</span></span>
<span data-ttu-id="24cbf-149">Nākamajā tabulā ir aprakstītas vadīklas cilnē **Atskaišu grupa**.</span><span class="sxs-lookup"><span data-stu-id="24cbf-149">The following table describes the controls on the **Report Group** tab.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="24cbf-150">Kontrole</span><span class="sxs-lookup"><span data-stu-id="24cbf-150">Control</span></span></th>
<th><span data-ttu-id="24cbf-151">Apraksts</span><span class="sxs-lookup"><span data-stu-id="24cbf-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24cbf-152">Atsevišķu pārskatu definīcijās ignorēt uzņēmuma, detalizētas informācijas un datuma iestatījumus</span><span class="sxs-lookup"><span data-stu-id="24cbf-152">Override company, detail, and date settings from individual report definitions</span></span></td>
<td><span data-ttu-id="24cbf-153">Atlasiet šo izvēles rūtiņu, lai ignorētu atsevišķu pārskatu definīcijas šajā pārskata grupā, tikai šo pārskatu veidošanai.</span><span class="sxs-lookup"><span data-stu-id="24cbf-153">Select this check box to override individual report definitions of the reports in this report group for the generation of these reports only.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24cbf-154">Uzņēmuma nosaukums</span><span class="sxs-lookup"><span data-stu-id="24cbf-154">Company name</span></span></td>
<td><span data-ttu-id="24cbf-155">Atlasiet kompāniju, kas jāizmanto pārskatos.</span><span class="sxs-lookup"><span data-stu-id="24cbf-155">Select the company to use for the reports.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24cbf-156">Detalizācijas līmenis</span><span class="sxs-lookup"><span data-stu-id="24cbf-156">Detail level</span></span></td>
<td><span data-ttu-id="24cbf-157">Norādiet detalizētības līmeni, kāds ir iekļauts atskaitēs.</span><span class="sxs-lookup"><span data-stu-id="24cbf-157">Specify the level of detail that the reports include.</span></span>
<ul>
<li><span data-ttu-id="24cbf-158"><strong>Finanšu</strong> — augstākā līmeņa kopsavilkuma pārskats.</span><span class="sxs-lookup"><span data-stu-id="24cbf-158"><strong>Financial</strong> − A high-level summary report.</span></span> <span data-ttu-id="24cbf-159">Nevara&#39;t detalizēti skatīt kontus un dimensijas, izņemot tos kontus un dimensijas, kas ir pievienoti, izmantojot pārskatu koku.</span><span class="sxs-lookup"><span data-stu-id="24cbf-159">You can&#39;t drill down to accounts and dimensions, except for those accounts and dimensions that have been added through a reporting tree.</span></span></li>
<li><span data-ttu-id="24cbf-160"><strong>Finanšu &amp; Konts</strong> — pārskats, kas satur augsta līmeņa kopsavilkumu un detalizētu informāciju par kontu.</span><span class="sxs-lookup"><span data-stu-id="24cbf-160"><strong>Financial &amp; Account</strong> − A report that contains a high-level summary and account details.</span></span></li>
<li><span data-ttu-id="24cbf-161"><strong>Finanšu, Konts, &amp; Transakcija</strong> — pārskats, kas satur augsta līmeņa kopsavilkumu un detalizētu informāciju par transakciju.</span><span class="sxs-lookup"><span data-stu-id="24cbf-161"><strong>Financial, Account, &amp; Transaction</strong> − A report that contains a high-level summary and transaction details.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="24cbf-162">Provizorisks</span><span class="sxs-lookup"><span data-stu-id="24cbf-162">Provisional</span></span></td>
<td><span data-ttu-id="24cbf-163">Norādiet aktivitāšu tipus, kas ir iekļauti atskaitēs.</span><span class="sxs-lookup"><span data-stu-id="24cbf-163">Specify the types of activity that the reports include.</span></span>
<ul>
<li><span data-ttu-id="24cbf-164"><strong>Tikai grāmatotās darbības</strong> — ietverti tikai darījumi un bilances, kas ir grāmatoti jūsu finanšu datos.</span><span class="sxs-lookup"><span data-stu-id="24cbf-164"><strong>Posted activity only</strong> − Include only the transactions and balances that are posted in your financial data.</span></span></li>
<li><span data-ttu-id="24cbf-165"><strong>Grāmatotās un negrāmatotās darbības</strong> — ietverti visi darījumi un bilances, kas ir ievadīti un grāmatoti jūsu finanšu datos.</span><span class="sxs-lookup"><span data-stu-id="24cbf-165"><strong>Posted and unposted activity</strong> − Include all the transactions and balances that are entered and posted in your financial data.</span></span></li>
<li><span data-ttu-id="24cbf-166"><strong>Tikai negrāmatotās darbības</strong> — ietverti tikai tie darījumi, kuri ir ievadīti, bet vēl nav iegrāmatoti jūsu finanšu datos.</span><span class="sxs-lookup"><span data-stu-id="24cbf-166"><strong>Unposted activity only</strong> − Include only the transactions that are entered, but not yet posted, in your financial data.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="24cbf-167">Iekļaut visas pārskatu veidošanas valūtas</span><span class="sxs-lookup"><span data-stu-id="24cbf-167">Include all reporting currencies</span></span></td>
<td><span data-ttu-id="24cbf-168">Šeit ir norādītas visas papildu pārskatu valūtas, kas ir konfigurētas jūsu Microsoft Dynamics ERP sistēmā.</span><span class="sxs-lookup"><span data-stu-id="24cbf-168">Any additional reporting currencies that are configured in your Microsoft Dynamics ERP system are listed here.</span></span> <span data-ttu-id="24cbf-169">Atzīmējiet šo izvēles rūtiņu, lai ģenerētu papildu atskaites norādītajās valūtās.</span><span class="sxs-lookup"><span data-stu-id="24cbf-169">Select this check box to generate additional reports in the currencies that are indicated.</span></span> <span data-ttu-id="24cbf-170">Lai skatītu šos pārskatus, pakalpojumā Tīmekļa skatītājs noklikšķiniet uz pogas <strong>Valūta</strong> un pēc tam atlasiet valūtu.</span><span class="sxs-lookup"><span data-stu-id="24cbf-170">To view these reports in the Web Viewer, click the <strong>Currency</strong> button, and then select a currency.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24cbf-171">Datuma informācija netiek saglabāta ar pārskata definīciju</span><span class="sxs-lookup"><span data-stu-id="24cbf-171">Date information not saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="24cbf-172">Bāzes periods</span><span class="sxs-lookup"><span data-stu-id="24cbf-172">Base period</span></span></li>
<li><span data-ttu-id="24cbf-173">Bāzes gads</span><span class="sxs-lookup"><span data-stu-id="24cbf-173">Base year</span></span></li>
<li><span data-ttu-id="24cbf-174">Ietvertais periods</span><span class="sxs-lookup"><span data-stu-id="24cbf-174">Period covered</span></span></li>
</ul>
<span data-ttu-id="24cbf-175">Ar atskaites definīciju tiek saglabāti tikai noklusējuma bāzes perioda iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="24cbf-175">Only default base period settings are saved with the report definition.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24cbf-176">Datuma informācija tiek saglabāta ar pārskata definīciju</span><span class="sxs-lookup"><span data-stu-id="24cbf-176">Date information saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="24cbf-177">Pārskata datums</span><span class="sxs-lookup"><span data-stu-id="24cbf-177">Report date</span></span></li>
<li><span data-ttu-id="24cbf-178">Noklusējuma bāzes periods</span><span class="sxs-lookup"><span data-stu-id="24cbf-178">Default base period</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="24cbf-179">Pārskati grupā</span><span class="sxs-lookup"><span data-stu-id="24cbf-179">Reports in group</span></span></td>
<td><span data-ttu-id="24cbf-180">Pievienot, noņemt un atkārtoti pasūtīt pārskatus pārskata grupā.</span><span class="sxs-lookup"><span data-stu-id="24cbf-180">Add, remove, and re-order reports in the report group.</span></span>
<ul>
<li><span data-ttu-id="24cbf-181">Lai pārskatu grupai pievienotu pārskatu definīcijas, atveriet pārskatu grupu, veicot dubultklikšķi uz tās, un pēc tam noklikšķiniet uz <strong>Pievienot</strong>.</span><span class="sxs-lookup"><span data-stu-id="24cbf-181">To add report definitions to the report group, double-click the report group to open it, and then click <strong>Add</strong>.</span></span> <span data-ttu-id="24cbf-182">Atlasiet pārskatu grupai pievienojamos pārskatus un pēc tam noklikšķiniet uz <strong>Labi</strong>.</span><span class="sxs-lookup"><span data-stu-id="24cbf-182">Select the reports to include in the report group, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="24cbf-183">Lai no pārskatu grupas noņemtu pārskatu, atlasiet vēlamo pārskatu un pēc tam noklikšķiniet uz <strong>Noņemt</strong>.</span><span class="sxs-lookup"><span data-stu-id="24cbf-183">To remove a report from the report group, select it, and then click <strong>Remove</strong>.</span></span></li>
<li><span data-ttu-id="24cbf-184">Lai mainītu secību, kādā atskaites tiek ģenerētas, sarakstā atlasiet kādu atskaiti un pēc tam noklikšķiniet uz <strong>Pārvietot uz augšu</strong> vai <strong>Pārvietot uz leju</strong>.</span><span class="sxs-lookup"><span data-stu-id="24cbf-184">To modify the order that the reports are generated in, select a report in the list, and then click <strong>Move up</strong> or <strong>Move down</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="24cbf-185">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="24cbf-185">Additional resources</span></span>

[<span data-ttu-id="24cbf-186">Finanšu pārskatu veidošana</span><span class="sxs-lookup"><span data-stu-id="24cbf-186">Financial reporting</span></span>](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]