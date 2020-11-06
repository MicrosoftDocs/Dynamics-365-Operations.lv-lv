---
title: Navigācijas izvēlnes modulis
description: Šajā tēmā tiek stāstīts par navigācijas izvēlnes moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b0e8168ca9ec9ca68011650a73cc09983deca645
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055741"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="403c3-103">Navigācijas izvēlnes modulis</span><span class="sxs-lookup"><span data-stu-id="403c3-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="403c3-104">Šajā tēmā tiek stāstīts par navigācijas izvēlnes moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="403c3-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="403c3-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="403c3-105">Overview</span></span>

<span data-ttu-id="403c3-106">Navigācijas izvēlnes moduļu primārais nolūks ir ļaut vietnes lietotājiem pārlūkot preces un vietnes lapas atbilstoši programmā Dynamics 365 Commerce Headquarters noteiktajai kanāla navigācijas hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="403c3-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="403c3-107">Navigācijas izvēlnes modulī konfigurētie krājumi parādās kā vietnes galvenes navigācija.</span><span class="sxs-lookup"><span data-stu-id="403c3-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="403c3-108">Navigācijas izvēlnes moduļi atbalsta arī statiskus izvēlnes elementus, kas ir saistīti ar citām e-komercijas vietnēm.</span><span class="sxs-lookup"><span data-stu-id="403c3-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="403c3-109">Navigācijas izvēlnes moduli var pievienot lapas galvenes modulim.</span><span class="sxs-lookup"><span data-stu-id="403c3-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="403c3-110">Tēmā Fabrikam navigācijas izvēlne pēc noklusējuma rāda divus līmeņus.</span><span class="sxs-lookup"><span data-stu-id="403c3-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="403c3-111">Tēmā Starter navigācijas izvēlne pēc noklusējuma rāda trīs līmeņus.</span><span class="sxs-lookup"><span data-stu-id="403c3-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="403c3-112">Lai mainītu uz līmeņu skaitu, tēmā ir nepieciešams skata paplašinājums.</span><span class="sxs-lookup"><span data-stu-id="403c3-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="403c3-113">Sekojošajā attēlā redzams vietnes Fabrikam navigācijas izvēlnes piemērs ar diviem kategoriju hierarhijas līmeņiem un dažiem statiskiem izvēlnes elementiem.</span><span class="sxs-lookup"><span data-stu-id="403c3-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="403c3-114">![Navigācijas izvēlnes moduļa piemērs](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="403c3-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="403c3-115">Navigācijas izvēlnes moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="403c3-115">Navigation menu module properties</span></span>

| <span data-ttu-id="403c3-116">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="403c3-116">Property name</span></span>             | <span data-ttu-id="403c3-117">Vērtība</span><span class="sxs-lookup"><span data-stu-id="403c3-117">Value</span></span>                 | <span data-ttu-id="403c3-118">Apraksts</span><span class="sxs-lookup"><span data-stu-id="403c3-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="403c3-119">Modulis</span><span class="sxs-lookup"><span data-stu-id="403c3-119">Source</span></span>                  | <span data-ttu-id="403c3-120">**Mazumtirdzniecība** , **Manuāla autorēšana** , **Mazumtirdzniecība un manuāla autorēšana**</span><span class="sxs-lookup"><span data-stu-id="403c3-120">**Retail** , **Manual authoring** , **Retail and manual authoring**</span></span> | <span data-ttu-id="403c3-121">Vērtība **Mazumtirdzniecība** ļauj navigācijas izvēlnē parādīt kanāla navigācijas hierarhiju no Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="403c3-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="403c3-122">Vērtība **Manuālā autorēšana** ļauj pārraudzīt statiskos izvēlnes vienumus.</span><span class="sxs-lookup"><span data-stu-id="403c3-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="403c3-123">Vērtība **Mazumtirdzniecība un manuālā autorēšana** ļauj kombinēt abas.</span><span class="sxs-lookup"><span data-stu-id="403c3-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="403c3-124">Rādīt kategoriju attēlus</span><span class="sxs-lookup"><span data-stu-id="403c3-124">Show category images</span></span> | <span data-ttu-id="403c3-125">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="403c3-125">**True** or **False**</span></span>    | <span data-ttu-id="403c3-126">Ja iespējots, šis rekvizīts parāda kategoriju attēlus navigācijas izvēlnē, kā definēts Commerce Headquarters katrai kategorijai.</span><span class="sxs-lookup"><span data-stu-id="403c3-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="403c3-127">Pievienots Commerce izlaidumā 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="403c3-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="403c3-128">Vairāku līmeņu navigācijas izvēlnes iespējošana</span><span class="sxs-lookup"><span data-stu-id="403c3-128">Enable multi-level navigation menu</span></span> | <span data-ttu-id="403c3-129">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="403c3-129">**True** or **False**</span></span> | <span data-ttu-id="403c3-130">Kad šis rekvizīts ir iespējots, navigācijas izvēlne var parādīt vairākus navigācijas hierarhijas līmeņus.</span><span class="sxs-lookup"><span data-stu-id="403c3-130">When this property is enabled, the navigation menu can show multiple levels of the navigation hierarchy.</span></span> <span data-ttu-id="403c3-131">Šis līdzeklis ir pieejams Dynamics 365 Commerce laidienā 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="403c3-131">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="403c3-132">Līmeņu skaits</span><span class="sxs-lookup"><span data-stu-id="403c3-132">Number of levels</span></span> | <span data-ttu-id="403c3-133">vesels skaitlis</span><span class="sxs-lookup"><span data-stu-id="403c3-133">integer</span></span> | <span data-ttu-id="403c3-134">Šis rekvizīts nosaka līmeņu skaitu, kas jāparāda, ja rekvizīts **Iespējot vairāklīmeņu navigācijas izvēlnes** ir iestatīts uz **Patiess**.</span><span class="sxs-lookup"><span data-stu-id="403c3-134">This property defines the numbers of levels that should be shown if the **Enable multilevel navigation menu** property is set to **True**.</span></span> |
| <span data-ttu-id="403c3-135">Statisks izvēlnes elements</span><span class="sxs-lookup"><span data-stu-id="403c3-135">Static menu item</span></span>| <span data-ttu-id="403c3-136">Vērtību masīvs</span><span class="sxs-lookup"><span data-stu-id="403c3-136">Array of values</span></span>| <span data-ttu-id="403c3-137">Statiski izvēlnes elementi, kas saista izvēlnes elementa nosaukumu ar saiti uz statisku vietnes lapu.</span><span class="sxs-lookup"><span data-stu-id="403c3-137">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="403c3-138">Varat izveidot izvēlnes elementus zem citiem izvēlnes elementiem.</span><span class="sxs-lookup"><span data-stu-id="403c3-138">You can create menu items below other menu items.</span></span> <span data-ttu-id="403c3-139">Pēc noklusējuma statiskās izvēlnes parādās saknes līmenī, un tās tiks pievienotas kanālu navigācijas hierarhijai, ja tāda pastāv.</span><span class="sxs-lookup"><span data-stu-id="403c3-139">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |
| <span data-ttu-id="403c3-140">Rādīt saknes izvēlni</span><span class="sxs-lookup"><span data-stu-id="403c3-140">Show root menu</span></span> | <span data-ttu-id="403c3-141">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="403c3-141">**True** or **False**</span></span> | <span data-ttu-id="403c3-142">Kad šis rekvizīts ir iespējots, navigācijas izvēlni var definēt ar pielāgotu sakni (piemēram, **Iepirkties tūlīt** ).</span><span class="sxs-lookup"><span data-stu-id="403c3-142">When this property is enabled, the navigation menu can be defined under a custom root (for example, **Shop now** ).</span></span> <span data-ttu-id="403c3-143">Šis līdzeklis ir pieejams Dynamics 365 Commerce laidienā 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="403c3-143">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="403c3-144">Saknes izvēlne</span><span class="sxs-lookup"><span data-stu-id="403c3-144">Root menu</span></span> | <span data-ttu-id="403c3-145">virkne</span><span class="sxs-lookup"><span data-stu-id="403c3-145">string</span></span> | <span data-ttu-id="403c3-146">Šo rekvizītu var izmantot, lai definētu tekstu pielāgotai saknei, ja rekvizīts **Rādīt saknes izvēlni** ir iestatīts uz **Patiess**.</span><span class="sxs-lookup"><span data-stu-id="403c3-146">This property can be used to define text for a custom root if the **Show root menu** property is set to **True**.</span></span> |

<span data-ttu-id="403c3-147">Sekojošajā attēlā redzams kategorijas attēla piemērs, kas parādīts Fabrikam vietnes navigācijas izvēlnē.</span><span class="sxs-lookup"><span data-stu-id="403c3-147">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="403c3-148">![Navigācijas izvēlnes moduļa piemērs ar kategoriju attēliem](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="403c3-148">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="403c3-149">Navigācijas izvēlnes moduļa pievienošana galvenes modulim</span><span class="sxs-lookup"><span data-stu-id="403c3-149">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="403c3-150">Detalizētu informāciju par navigācijas izvēlnes moduļa pievienošanu galvenes modulim skatiet [Galvenes modulis](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="403c3-150">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="403c3-151">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="403c3-151">Additional resources</span></span>

[<span data-ttu-id="403c3-152">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="403c3-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="403c3-153">Atpakaļceļa modulis</span><span class="sxs-lookup"><span data-stu-id="403c3-153">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="403c3-154">Vietas atlasītāja modulis</span><span class="sxs-lookup"><span data-stu-id="403c3-154">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="403c3-155">Pirkšanas lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="403c3-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="403c3-156">Sīkfailu atbilstība</span><span class="sxs-lookup"><span data-stu-id="403c3-156">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="403c3-157">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="403c3-157">Header module</span></span>](author-header-module.md)
