---
title: Meklēšanas rezultātu modulis
description: Šajā tēmā tiek stāstīts par meklēšanas rezultātu moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5d852fe1a81b1e42484bc49ae136ef8613a2d3a5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254773"
---
# <a name="search-results-module"></a><span data-ttu-id="d9139-103">Meklēšanas rezultātu modulis</span><span class="sxs-lookup"><span data-stu-id="d9139-103">Search results module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="d9139-104">Šajā tēmā tiek stāstīts par meklēšanas rezultātu moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d9139-104">This topic covers search results modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d9139-105">Meklēšanas rezultātu modulis atgriež preču meklēšanas rezultātus un piemērojamo preču rafinētāju sarakstu.</span><span class="sxs-lookup"><span data-stu-id="d9139-105">The search results module returns product search results and a list of applicable refiners for the products.</span></span> <span data-ttu-id="d9139-106">Meklēšanas rezultātu moduļus Dynamics 365 Commerce vietnēs var izmantot, lai atveidotu lapas šādiem scenārijiem:</span><span class="sxs-lookup"><span data-stu-id="d9139-106">Search results modules on Dynamics 365 Commerce sites can be used to render pages for the following scenarios:</span></span>

- <span data-ttu-id="d9139-107">Meklēšanas rezultāti, ko uzsāka lietotāja meklēšana</span><span class="sxs-lookup"><span data-stu-id="d9139-107">Search results that are initiated by a user search</span></span>
- <span data-ttu-id="d9139-108">Meklēšanas rezultāti, kas norāda noteiktu preču kopu, piemēram, "Pirkt līdzīgas preces"</span><span class="sxs-lookup"><span data-stu-id="d9139-108">Search results that show a specific set of products, such as "Shop similar looks"</span></span>
- <span data-ttu-id="d9139-109">Preču saraksti, kas pieder noteiktai kategorijai</span><span class="sxs-lookup"><span data-stu-id="d9139-109">Lists of products that belong to a category</span></span>

<span data-ttu-id="d9139-110">Papildinformāciju par kategoriju un meklēšanas rezultātu lapām skatiet [Noklusējuma kategorijas ielādes lapa un meklēšanas rezultātu lapas apskats](category-search-page-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d9139-110">For more information about category and search results pages, see [Default category landing page and search results page overview](category-search-page-overview.md).</span></span>

<span data-ttu-id="d9139-111">Sekojošajā attēlā redzams kategorijas meklēšanas rezultātu lapas piemērs Fabrikam vietnē.</span><span class="sxs-lookup"><span data-stu-id="d9139-111">The following illustration shows an example of a search results page for a category on the Fabrikam site.</span></span>

![Meklēšanas rezultātu lapas piemērs Fabrikam vietnē](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a><span data-ttu-id="d9139-113">Meklēšanas rezultātu moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="d9139-113">Search results module properties</span></span>

<span data-ttu-id="d9139-114">Tabulā zemāk uzskaitīti meklēšanas rezultātu moduļu rekvizīti un to vērtības un apraksti.</span><span class="sxs-lookup"><span data-stu-id="d9139-114">The following table lists the properties of search result modules, together with their values and descriptions.</span></span>

| <span data-ttu-id="d9139-115">Rekvizīts</span><span class="sxs-lookup"><span data-stu-id="d9139-115">Property</span></span> | <span data-ttu-id="d9139-116">Vērtības</span><span class="sxs-lookup"><span data-stu-id="d9139-116">Values</span></span> | <span data-ttu-id="d9139-117">Apraksts</span><span class="sxs-lookup"><span data-stu-id="d9139-117">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="d9139-118">Vienumi lapā</span><span class="sxs-lookup"><span data-stu-id="d9139-118">Items per page</span></span> | <span data-ttu-id="d9139-119">Vesels skaitlis</span><span class="sxs-lookup"><span data-stu-id="d9139-119">Integer</span></span> | <span data-ttu-id="d9139-120">Krājumu skaits, kas jāparāda katrā lapā.</span><span class="sxs-lookup"><span data-stu-id="d9139-120">The number of items that should be shown on each page.</span></span> |
| <span data-ttu-id="d9139-121">Atļaut balstīties uz PDP</span><span class="sxs-lookup"><span data-stu-id="d9139-121">Allow back on PDP</span></span> | <span data-ttu-id="d9139-122">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="d9139-122">**True** or **False**</span></span> | <span data-ttu-id="d9139-123">Ja šis rekvizīts ir iestatīts uz **Patiess**, kad lietotājs atlasa preci meklēšanas rezultātu lapā, atpakaļceļa navigācija uz preces informācijas lapu, kas ir atvērta, parādīs saiti "Atpakaļ uz rezultātiem".</span><span class="sxs-lookup"><span data-stu-id="d9139-123">If this property is set to **True**, when a user selects a product on the search results page, the breadcrumb navigation on the product details page (PDP) that is opened will show a "Back to results" link.</span></span> |
| <span data-ttu-id="d9139-124">Izvērst precizētājus</span><span class="sxs-lookup"><span data-stu-id="d9139-124">Expand Refiners</span></span> | <span data-ttu-id="d9139-125">**Viss**, **1**, **2**, **3**, or **4**</span><span class="sxs-lookup"><span data-stu-id="d9139-125">**All**, **1**, **2**, **3**, or **4**</span></span> | <span data-ttu-id="d9139-126">Galveno rafinētāju skaits, kas jāizvērš, kad lapa ir ielādēta.</span><span class="sxs-lookup"><span data-stu-id="d9139-126">The number of top refiners that should be expanded when a page is loaded.</span></span> <span data-ttu-id="d9139-127">Piemēram, ja šis rekvizīts ir iestatīts uz **3**, tiks izvērsti pirmie trīs rafinētāji lapā.</span><span class="sxs-lookup"><span data-stu-id="d9139-127">For example, if this property is set to **3**, the first three refiners on the page will be expanded.</span></span> |
| <span data-ttu-id="d9139-128">Paslēpt kategoriju hierarhijas attēlojumu</span><span class="sxs-lookup"><span data-stu-id="d9139-128">Hide category hierarchy display</span></span> | <span data-ttu-id="d9139-129">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="d9139-129">**True** or **False**</span></span> | <span data-ttu-id="d9139-130">Ja šis rekvizīts ir iestatīts uz **Patiess**, lapā parādītā kategoriju hierarhija tiks paslēpta.</span><span class="sxs-lookup"><span data-stu-id="d9139-130">If this property is set to **True**, the category hierarchy display on the page will be hidden.</span></span> <span data-ttu-id="d9139-131">Šis rekvizīts būtu jāiestata uz **Patiess**, ja izmantojat [atpakaļceļa moduli](add-breadcrumb.md), lai rādītu kategoriju hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="d9139-131">This property should be set to **True** if you're using the [breadcrumb module](add-breadcrumb.md) to show the category hierarchy.</span></span>|
| <span data-ttu-id="d9139-132">Meklēšanas rezultātos iekļaut produkta atribūtus</span><span class="sxs-lookup"><span data-stu-id="d9139-132">Include product attributes in search results</span></span> | <span data-ttu-id="d9139-133">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="d9139-133">**True** or **False**</span></span> | <span data-ttu-id="d9139-134">Ja šis rekvizīts ir iestatīts uz **Patiess**, meklēšanas rezultātos precēm tiks atgriezti atribūti.</span><span class="sxs-lookup"><span data-stu-id="d9139-134">If this property is set to **True**, attributes will be returned for the products in the search results.</span></span> <span data-ttu-id="d9139-135">Lai arī šos atribūtus var parādīt Commerce vietnē, nepieciešams paplašinājums.</span><span class="sxs-lookup"><span data-stu-id="d9139-135">Although these attributes can be shown on a Commerce site, an extension is required.</span></span>|
| <span data-ttu-id="d9139-136">Rādīt piederības cenas</span><span class="sxs-lookup"><span data-stu-id="d9139-136">Show affiliation prices</span></span> | <span data-ttu-id="d9139-137">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="d9139-137">**True** or **False**</span></span> | <span data-ttu-id="d9139-138">Ja šis rekvizīts ir iestatīts uz **Patiess**, preču piederības cenas tiks rādītas meklēšanas rezultātos, kad lietotājs, kurš ir pierakstījies, pārlūko lapu.</span><span class="sxs-lookup"><span data-stu-id="d9139-138">If this property is set to **True**, affiliation prices for products will be shown in the search results when a signed-in user browses the page.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="d9139-139">Dynamics 365 Commerce 10.0.16 laidienā un jaunākos laidienos konfigurāciju **Rādīt piederības cenas** var izmantot, lai lapā parādītu piederības cenas lapā.</span><span class="sxs-lookup"><span data-stu-id="d9139-139">In the Dynamics 365 Commerce 10.0.16 release and later, the **Show affiliation prices** configuration can be used to show affiliation prices on the page.</span></span>

## <a name="supported-modules"></a><span data-ttu-id="d9139-140">Atbalstītie moduļi</span><span class="sxs-lookup"><span data-stu-id="d9139-140">Supported modules</span></span>

<span data-ttu-id="d9139-141">Meklēšanas rezultātu modulis atbalsta [ātro skatu moduli](quick-view-module.md), kas ļauj lietotājiem skatīt preces informāciju un pievienot vienumus grozam no meklēšanas rezultātu lapas.</span><span class="sxs-lookup"><span data-stu-id="d9139-141">The search results module supports the [quick view module](quick-view-module.md), which lets users view product information and add items to the cart from the search results page.</span></span>

## <a name="add-a-search-results-module-to-a-category-page"></a><span data-ttu-id="d9139-142">Pievienot meklēšanas rezultātu moduli kategorijas lapai</span><span class="sxs-lookup"><span data-stu-id="d9139-142">Add a search results module to a category page</span></span>

<span data-ttu-id="d9139-143">Lai pievienotu meklēšanas rezultātu moduli kategorijas lapai, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="d9139-143">To add a search results module to a category page, follow these steps.</span></span>

1. <span data-ttu-id="d9139-144">Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.</span><span class="sxs-lookup"><span data-stu-id="d9139-144">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="d9139-145">Dialoglodziņā **Jauna veidne** ievadiet nosaukumu **Meklēt rezultātus** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d9139-145">In the **New template** dialog box, enter the name **Search results**, and then select **OK**.</span></span>
1. <span data-ttu-id="d9139-146">Slotā **Pamatteksts** atlasiet daudzpunkti (...) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="d9139-146">In the **Body** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d9139-147">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Noklusējuma lapa** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d9139-147">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d9139-148">Moduļa **Noklusējuma lapa** slotā **Galvenais** atlasiet daudzpunkti (...) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="d9139-148">In the **Main** slot of the **Default Page** module, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d9139-149">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d9139-149">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d9139-150">Slotā **Konteiners** atlasiet daudzpunkti (...) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="d9139-150">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d9139-151">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Atpakaļceļs** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d9139-151">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d9139-152">Rekvizītu rūtī **Atpakaļceļš** ievadiet vērtību **1** opcijai **Min. atkārtošanās skaits**.</span><span class="sxs-lookup"><span data-stu-id="d9139-152">In the **Breadcrumb** properties pane, enter the value **1** for **Min Occurs**.</span></span>
1. <span data-ttu-id="d9139-153">Slotā **Konteiners** atlasiet daudzpunkti (...) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="d9139-153">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d9139-154">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Meklēšanas rezultāti** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d9139-154">In the **Add Module** dialog box, select the **Search results** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d9139-155">Rekvizītu rūtī **Meklēšanas rezultāti** ievadiet vērtību **1** opcijai **Min. atkārtošanās skaits** un pēc tam iestatiet visus citus nepieciešamos meklēšanas rezultātu modulim.</span><span class="sxs-lookup"><span data-stu-id="d9139-155">In the **Search results** properties pane, enter the value **1** for **Min Occurs**, and then set any other required properties for the search results module.</span></span> <span data-ttu-id="d9139-156">Iestatot šos rekvizītus veidnē, pārliecinieties, ka visi konkrētas kategorijas lapas pielāgojumi automātiski ietvers šos iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="d9139-156">By setting these properties in the template, you ensure that any customizations to a specific category page will automatically include these settings.</span></span>
1. <span data-ttu-id="d9139-157">Atlasiet **Pabeigt rediģēšanu** un pēc tam atlasiet **Publicēt**, lai publicētu veidni.</span><span class="sxs-lookup"><span data-stu-id="d9139-157">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>
1. <span data-ttu-id="d9139-158">Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.</span><span class="sxs-lookup"><span data-stu-id="d9139-158">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="d9139-159">Dialoglodziņā **Izvēlēties veidni** atlasiet iepriekš izveidoto veidni **Meklēšanas rezultāti**, ievadiet **Kategorijas lapa** opcijai **Lapas nosaukums** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d9139-159">In the **Choose a template** dialog box, select the **Search results** template that you created, enter **Category page** for **Page name**, and then select **OK**.</span></span> <span data-ttu-id="d9139-160">Tā kā visas vērtības ir iestatītas veidnē, lapa ir gatava publicēšanai.</span><span class="sxs-lookup"><span data-stu-id="d9139-160">Because all the values are set in the template, the page is ready to be published.</span></span>
1. <span data-ttu-id="d9139-161">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="d9139-161">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d9139-162">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d9139-162">Additional resources</span></span>

[<span data-ttu-id="d9139-163">Noklusējuma kategorijas reklāmas mērķlapas un meklēšanas rezultātu lapas pārskats</span><span class="sxs-lookup"><span data-stu-id="d9139-163">Default category landing page and search results page overview</span></span>](category-search-page-overview.md)

[<span data-ttu-id="d9139-164">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="d9139-164">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d9139-165">Ātrā skata modulis</span><span class="sxs-lookup"><span data-stu-id="d9139-165">Quick view module</span></span>](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]