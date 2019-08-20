---
title: Lauku aprakstu skatīšana un eksportēšana
description: Šajā rakstā ir paskaidrots, ka skatīt lauku aprakstus un kā lietot lapu Lauku apraksti, lai eksportētu aprakstus.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a94f7ab9df19200754e39ba5a46f13bfdb1a3ab
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/02/2019
ms.locfileid: "1852109"
---
# <a name="view-and-export-field-descriptions"></a><span data-ttu-id="e03c9-103">Lauku aprakstu skatīšana un eksportēšana</span><span class="sxs-lookup"><span data-stu-id="e03c9-103">View and export field descriptions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e03c9-104">Šajā rakstā ir paskaidrots, ka skatīt lauku aprakstus un kā lietot lapu Lauku apraksti, lai eksportētu aprakstus.</span><span class="sxs-lookup"><span data-stu-id="e03c9-104">This article describes how to view field descriptions and how to use the Field descriptions page to export descriptions.</span></span>

<span data-ttu-id="e03c9-105">Programmatūrā Microsoft Dynamics 365 for Finance and Operations tiek nodrošināti apraksti par dažiem sarežģītākajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="e03c9-105">Microsoft Dynamics 365 for Finance and Operations has descriptions for some of the more complex fields.</span></span> <span data-ttu-id="e03c9-106">Šie apraksti tiek parādīti, kad novietojat peles kursoru uz lauka.</span><span class="sxs-lookup"><span data-stu-id="e03c9-106">These descriptions appear when you hover over a field.</span></span> <span data-ttu-id="e03c9-107">Aprakstus varat skatīt un eksportēt lapā **Lauku apraksti**.</span><span class="sxs-lookup"><span data-stu-id="e03c9-107">You can also view and export descriptions on the **Field descriptions** page.</span></span>

<span data-ttu-id="e03c9-108">Ne visām lapām ir lauku apraksti.</span><span class="sxs-lookup"><span data-stu-id="e03c9-108">Not all pages have field descriptions.</span></span> <span data-ttu-id="e03c9-109">Mēs vēlamies sniegt aprakstus tikai sarežģītākajiem laukiem, nevis tiem, kuru lietojums ir acīmredzams.</span><span class="sxs-lookup"><span data-stu-id="e03c9-109">We want to provide descriptions only for the more complex fields, not where the use of the field is obvious.</span></span> <span data-ttu-id="e03c9-110">Tādēļ dažās lapās nav neviena lauka apraksta, dažās lapās ir daži apraksti, bet dažās no sarežģītākajām lapām, piemēram, daudzās parametru lapās, ir daudz aprakstu.</span><span class="sxs-lookup"><span data-stu-id="e03c9-110">Therefore, some pages don't have any field descriptions, some pages have a few descriptions, and some of the more complex pages, such as many of the parameters pages, have many descriptions.</span></span>

<span data-ttu-id="e03c9-111">Ja jums ir piekļuve Finance and Operations izstrādes videi, varat pievienot jaunus lauku aprakstus un pielāgot esošos aprakstus.</span><span class="sxs-lookup"><span data-stu-id="e03c9-111">If you have access to the Finance and Operations development environment, you can add new field descriptions and customize existing descriptions.</span></span> <span data-ttu-id="e03c9-112">Piemēram, lauka aprakstam varat pievienot uzņēmumam specifisku informāciju.</span><span class="sxs-lookup"><span data-stu-id="e03c9-112">For example, you can add company-specific information to a field description.</span></span> <span data-ttu-id="e03c9-113">Papildinformāciju skatiet rakstā [Pielāgot lauka palīdzību](../../dev-itpro/user-interface/customize-field-help.md).</span><span class="sxs-lookup"><span data-stu-id="e03c9-113">For more information, see [Customize field help](../../dev-itpro/user-interface/customize-field-help.md).</span></span>

## <a name="see-field-descriptions-in-the-user-interface"></a><span data-ttu-id="e03c9-114">Skatīt lauku aprakstus lietotāja interfeisā</span><span class="sxs-lookup"><span data-stu-id="e03c9-114">See field descriptions in the user interface</span></span>

<span data-ttu-id="e03c9-115">Lauku aprakstus varat apskatīt, virzot peles kursoru pār attiecīgo lauku.</span><span class="sxs-lookup"><span data-stu-id="e03c9-115">You can view field descriptions by hovering over a field.</span></span> <span data-ttu-id="e03c9-116">Ja apraksts nav pieejams, kad novietojat peles kursoru uz lauka, jūs redzat lauka nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="e03c9-116">If no description is available, you see the field name when you hover over the field.</span></span>

> [!NOTE]
> <span data-ttu-id="e03c9-117">Programmā Dynamics AX 7.0 (2016. gada februāris) lauku aprakstus var skatīt tikai lapā **Lauku apraksti**.</span><span class="sxs-lookup"><span data-stu-id="e03c9-117">In Dynamics AX 7.0 (February 2016), field descriptions can be viewed only on the **Field descriptions** page.</span></span>

<span data-ttu-id="e03c9-118">Nākamajā attēlā ir parādīts lauka apraksts, kas ir redzams, kad novietojat peles kursoru uz lauka **Bloķēt krājumus inventarizācijas laikā**.</span><span class="sxs-lookup"><span data-stu-id="e03c9-118">The following illustration shows the field description that appears when you hover over the **Lock items during count** field.</span></span>

<span data-ttu-id="e03c9-119">[![Lauka apraksta piemērs](./media/field-description.png)](./media/field-description.png)</span><span class="sxs-lookup"><span data-stu-id="e03c9-119">[![Example of a field description](./media/field-description.png)](./media/field-description.png)</span></span>

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a><span data-ttu-id="e03c9-120">Izmantot lapu Lauku apraksti, lai skatītu un eksportētu lauku palīdzību</span><span class="sxs-lookup"><span data-stu-id="e03c9-120">Use the Field descriptions page to view and export field help</span></span>

<span data-ttu-id="e03c9-121">Lapa **Lauku apraksti** jums ļauj skatīt un eksportēt lauku aprakstus.</span><span class="sxs-lookup"><span data-stu-id="e03c9-121">The **Field descriptions** page lets you view and export field descriptions.</span></span> <span data-ttu-id="e03c9-122">Jūs varat redzēt aprakstus, kas ir pieejami vienā lapā vienlaicīgi.</span><span class="sxs-lookup"><span data-stu-id="e03c9-122">You can see the descriptions that are available for one page at a time.</span></span>

### <a name="view-the-descriptions-for-a-page"></a><span data-ttu-id="e03c9-123">Skatīt lapas aprakstus</span><span class="sxs-lookup"><span data-stu-id="e03c9-123">View the descriptions for a page</span></span>

<span data-ttu-id="e03c9-124">Lai skatītu aprakstus kādai lapai, izpildiet šo darbību.</span><span class="sxs-lookup"><span data-stu-id="e03c9-124">To view the descriptions for a page, follow this step.</span></span>

- <span data-ttu-id="e03c9-125">Laukā **Atlasīt lapu** ierakstiet lapas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="e03c9-125">In the **Select a page** field, type the name of the page.</span></span> <span data-ttu-id="e03c9-126">Varat arī noklikšķināt uz bultiņas, lai atvērtu lapu sarakstu, un pēc tam pārlūkot vai filtrēt šo sarakstu.</span><span class="sxs-lookup"><span data-stu-id="e03c9-126">Alternatively, click the arrow to open a list of all the pages, and then browse or filter the list.</span></span>

<span data-ttu-id="e03c9-127">Var izmantot lapas nosaukumu, kas tiek rādīts lietotāja interfeisā (UI) (piemēram, **Debitori**), vai lapas koda nosaukumu (AOT nosaukumu), kas ir pieejams, kad ar peles labo pogu noklikšķināt uz lapas (piemēram, **CustTable**).</span><span class="sxs-lookup"><span data-stu-id="e03c9-127">You can use either the name of the page that is shown in the user interface (UI) (for example, **Customers**) or the code name (AOT name) that's available when you right-click a page (for example, **CustTable**).</span></span>

<span data-ttu-id="e03c9-128">Informāciju par dažādajiem veidiem, kā filtrēt lapu sarakstu, skatiet vēlākā šī raksta sadaļā “Lapas meklēšana”.</span><span class="sxs-lookup"><span data-stu-id="e03c9-128">For information about the various ways to filter the list of pages, see the "Searching for a page" section later in this article.</span></span>

<span data-ttu-id="e03c9-129">Ja opciju **Iekļaut laukus bez apraksta** iestatāt uz **Jā**, tad tiek rādīti visi šajā lapā esošie lauki, pat ja tiem nav lauka apraksta.</span><span class="sxs-lookup"><span data-stu-id="e03c9-129">If you set the **Include fields without a description** option to **Yes**, all the fields on the page are shown, even if they don't have a field description.</span></span>

### <a name="export-the-descriptions-for-a-page"></a><span data-ttu-id="e03c9-130">Eksportēt lapas aprakstus</span><span class="sxs-lookup"><span data-stu-id="e03c9-130">Export the descriptions for a page</span></span>

<span data-ttu-id="e03c9-131">Lai eksportētu aprakstus kādai lapai, izpildiet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="e03c9-131">To export the descriptions for a page, follow these steps.</span></span>

1. <span data-ttu-id="e03c9-132">Laukā **Atlasīt lapu** atlasiet kādu lapu.</span><span class="sxs-lookup"><span data-stu-id="e03c9-132">In the **Select a page** field, select a page.</span></span>
2. <span data-ttu-id="e03c9-133">Noklikšķiniet uz pogas **Atvērt programmā Microsoft Office** augšējā labajā stūrī un pēc tam noklikšķiniet uz **FieldDescriptionTmp**.</span><span class="sxs-lookup"><span data-stu-id="e03c9-133">Click the **Open in Microsoft Office** button in the upper-right corner, and then click **FieldDescriptionTmp**.</span></span>

### <a name="searching-for-a-page"></a><span data-ttu-id="e03c9-134">Lapas meklēšana</span><span class="sxs-lookup"><span data-stu-id="e03c9-134">Searching for a page</span></span>

<span data-ttu-id="e03c9-135">Pastāv vairāki veidi, kā meklēt lapu laukā **Atlasīt lapu**.</span><span class="sxs-lookup"><span data-stu-id="e03c9-135">There are several ways to search for a page in the **Select a page** field.</span></span> <span data-ttu-id="e03c9-136">Daudzos gadījumos ir jānoklikšķina uz bultiņas laukā **Atlasīt lapu**, lai atvērtu nolaižamo sarakstu, un pēc tam jāatlasa no filtrētā lapu saraksta.</span><span class="sxs-lookup"><span data-stu-id="e03c9-136">In many cases, you must click the arrow in the **Select a page** field to open the drop-down list, and then select from a filtered list of pages.</span></span>

- <span data-ttu-id="e03c9-137">Ierakstiet daļēju nosaukumu un pēc tam atveriet nolaižamo sarakstu, lai atlasītu no filtrētā lapu saraksta.</span><span class="sxs-lookup"><span data-stu-id="e03c9-137">Type part of the name, and then open the drop-down list to select from a filtered list of pages.</span></span>
- <span data-ttu-id="e03c9-138">Atveriet nolaižamo sarakstu un pēc tam noklikšķiniet uz virsraksta **Lapas nosaukums** saraksta augšpusē vai uz virsraksta **Lapas AOT nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="e03c9-138">Open the drop-down list, and then click either the **Page name** heading at the top of the list or the **Page AOT name** heading.</span></span> <span data-ttu-id="e03c9-139">Tiek parādīts dialoglodziņš, kur varat izmantot papildu filtrēšanas opcijas, piemēram, **Lapas nosaukums sākas ar**.</span><span class="sxs-lookup"><span data-stu-id="e03c9-139">A dialog box appears, where you can use advanced filtering options, such as **Page name begins with**.</span></span>
- <span data-ttu-id="e03c9-140">Ierakstiet pilnu lapas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="e03c9-140">Type the full name of the page.</span></span> <span data-ttu-id="e03c9-141">Ja izmantojat šo opciju, ieteicams atvērt nolaižamo sarakstu un apskatīt, kas vēl ir pieejams šajā sarakstā pat tad, ja tiek rādīti lauku apraksti.</span><span class="sxs-lookup"><span data-stu-id="e03c9-141">When you use this option, it's best to open the drop-down list and see what else is in the list, even if field descriptions are shown.</span></span>

    - <span data-ttu-id="e03c9-142">Ja nosaukumam ir viena precīza atbilstība, tiek rādīti lauku apraksti šai lapai.</span><span class="sxs-lookup"><span data-stu-id="e03c9-142">If there is a single exact match to the name, the field descriptions for that page are shown.</span></span>
    - <span data-ttu-id="e03c9-143">Ja ir vairākas precīzas atbilstības, netiek rādīts neviens apraksts.</span><span class="sxs-lookup"><span data-stu-id="e03c9-143">If there is more than one exact match, no descriptions are shown.</span></span> <span data-ttu-id="e03c9-144">Jums ir jāatver nolaižamais saraksts un jāatlasa nepieciešamā lapa.</span><span class="sxs-lookup"><span data-stu-id="e03c9-144">You must open the drop-down list and select the page that you want.</span></span>
    - <span data-ttu-id="e03c9-145">Ja ierakstītais nosaukums ir daļa no citas lapas nosaukuma, tiek rādīti apraksti jūsu lapai.</span><span class="sxs-lookup"><span data-stu-id="e03c9-145">If the name that you typed is part of the name of another page, you see the descriptions for your page.</span></span> <span data-ttu-id="e03c9-146">Taču, ja atverat nolaižamo sarakstu, varat redzēt papildu lapas, kas ietver šo nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="e03c9-146">However, if you open the drop-down list, you see additional pages that contain that name.</span></span>

<span data-ttu-id="e03c9-147">Piemēram, nekādi apraksti netiek rādīti, kad laukā **Atlasīt lapu** ierakstāt **Inventarizācija**.</span><span class="sxs-lookup"><span data-stu-id="e03c9-147">For example, no descriptions are shown when you type **Counting** in the **Select a page** field.</span></span> <span data-ttu-id="e03c9-148">Jūs atverat nolaižamo sarakstu un redzat, ka pastāv divas lapas, kuru nosaukums ir **Inventarizācija**, un vairākas lapas, kuru nosaukumā ir ietverts vārds “Inventarizācija”.</span><span class="sxs-lookup"><span data-stu-id="e03c9-148">You open the drop-down list, and see that there are two pages that have the name **Counting** and several pages that contain the word "Counting" in the name.</span></span> <span data-ttu-id="e03c9-149">Ja atlasāt lapu, kuras AOT nosaukums ir **InventJournalCount**, tiek rādīti lauku nosaukumi šai lapai.</span><span class="sxs-lookup"><span data-stu-id="e03c9-149">If you select the page that has the AOT name **InventJournalCount**, the field descriptions are shown for that page.</span></span> <span data-ttu-id="e03c9-150">Taču, ja atkal atverat nolaižamo sarakstu, jūs redzat, ka sarakstā tagad ir visas lapas, kurām kā daļa no to AOT lapas nosaukuma ir “InventJournalCount”.</span><span class="sxs-lookup"><span data-stu-id="e03c9-150">However, if you open the drop-down list again, you will see that the list now contains all pages that have "InventJournalCount" as part of their AOT name.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="e03c9-151">Problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="e03c9-151">Troubleshooting</span></span>

<span data-ttu-id="e03c9-152">Šajā sadaļā ir sniegta informācija, lai jums palīdzētu novērst problēmas, kas varētu rasties, izmantojot lauku aprakstus.</span><span class="sxs-lookup"><span data-stu-id="e03c9-152">This section provides information to help you troubleshoot issues that you might encounter when you use field descriptions.</span></span>

### <a name="i-cant-find-a-field-description"></a><span data-ttu-id="e03c9-153">Nevar atrast lauka aprakstu</span><span class="sxs-lookup"><span data-stu-id="e03c9-153">I can't find a field description</span></span>

<span data-ttu-id="e03c9-154">Mēs pievienojam aprakstus sarežģītākajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="e03c9-154">We're in the process of adding descriptions for the more complex fields.</span></span> <span data-ttu-id="e03c9-155">Ja jums ir nepieciešama palīdzība par noteiktu lauku, lūdzu, ziņojiet mums, pievienojot komentāru šai tēmai.</span><span class="sxs-lookup"><span data-stu-id="e03c9-155">If you require help for a particular field, let us know by adding a comment for this topic.</span></span>

### <a name="the-field-description-isnt-helpful"></a><span data-ttu-id="e03c9-156">Šis lauka apraksts nav noderīgs</span><span class="sxs-lookup"><span data-stu-id="e03c9-156">The field description isn't helpful</span></span>

<span data-ttu-id="e03c9-157">Ziņojiet mums, pievienojot komentāru šai tēmai.</span><span class="sxs-lookup"><span data-stu-id="e03c9-157">Let us know by adding a comment for this topic.</span></span> <span data-ttu-id="e03c9-158">Ja varat, aprakstiet papildinformāciju, kas jums ir nepieciešama.</span><span class="sxs-lookup"><span data-stu-id="e03c9-158">If you can, describe the additional information that you require.</span></span>

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a><span data-ttu-id="e03c9-159">Nevar atrast kādu lauku lapā Lauku apraksti</span><span class="sxs-lookup"><span data-stu-id="e03c9-159">I can't find a field on the Field descriptions page</span></span>

<span data-ttu-id="e03c9-160">Lai lapā parādītu visus laukus, opciju **Iekļaut laukus bez apraksta** iestatiet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="e03c9-160">To show all the fields on a page, set the **Include fields without a description** option to **Yes**.</span></span> <span data-ttu-id="e03c9-161">Noklikšķiniet uz lauka **Atlasīt lapu**, lai pārliecinātos, ka esat atlasījis pareizo lapu.</span><span class="sxs-lookup"><span data-stu-id="e03c9-161">Click the **Select a page** field to verify that you've selected the correct page.</span></span> <span data-ttu-id="e03c9-162">Ja jūsu ierakstītais nosaukums ir daļa no cita lauka nosaukuma, iespējams, esat atlasījis lapu, kurai ir garāks nosaukums.</span><span class="sxs-lookup"><span data-stu-id="e03c9-162">If the name that you typed is part of another field name, you might have selected the page that has the longer name.</span></span>

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a><span data-ttu-id="e03c9-163">Nevar atrast kādu lapu lapā Lauku apraksti</span><span class="sxs-lookup"><span data-stu-id="e03c9-163">I can't find a page on the Field descriptions page</span></span>

<span data-ttu-id="e03c9-164">Informāciju par dažādajiem veidiem, kā atrast lapas, skatiet agrākā šī raksta sadaļā “Lapu meklēšana”.</span><span class="sxs-lookup"><span data-stu-id="e03c9-164">For information about the various way to find pages, see the "Searching for pages" section earlier in this article.</span></span> <span data-ttu-id="e03c9-165">Ja ierakstījāt precīzu lapas nosaukumu, iespējams, lauku apraksti netiek rādīti, ja šāds nosaukums ir vairākām lapām.</span><span class="sxs-lookup"><span data-stu-id="e03c9-165">If you've typed the exact name of the page, the field descriptions might not be shown if more than one page has the same name.</span></span> <span data-ttu-id="e03c9-166">Noklikšķiniet uz bultiņas laukā **Atlasīt lapu**, lai atvērtu filtrētu sarakstu ar pieejamajām lapām.</span><span class="sxs-lookup"><span data-stu-id="e03c9-166">Click the arrow in the **Select a page** field to open a filtered list of the pages that are available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e03c9-167">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e03c9-167">Additional resources</span></span>

[<span data-ttu-id="e03c9-168">Pielāgot lauku palīdzību</span><span class="sxs-lookup"><span data-stu-id="e03c9-168">Customize field help</span></span>](../../dev-itpro/user-interface/customize-field-help.md)
