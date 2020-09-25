---
title: Navigācijas izvēlnes modulis
description: Šajā tēmā tiek stāstīts par navigācijas izvēlnes moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 9f66bbe7bf436ab6360dda7d92d6d51e47eedf16
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761406"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="c3bd0-103">Navigācijas izvēlnes modulis</span><span class="sxs-lookup"><span data-stu-id="c3bd0-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="c3bd0-104">Šajā tēmā tiek stāstīts par navigācijas izvēlnes moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c3bd0-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c3bd0-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="c3bd0-105">Overview</span></span>

<span data-ttu-id="c3bd0-106">Navigācijas izvēlnes moduļu primārais nolūks ir ļaut vietnes lietotājiem pārlūkot preces un vietnes lapas atbilstoši programmā Dynamics 365 Commerce Headquarters noteiktajai kanāla navigācijas hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="c3bd0-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="c3bd0-107">Navigācijas izvēlnes modulī konfigurētie krājumi parādās kā vietnes galvenes navigācija.</span><span class="sxs-lookup"><span data-stu-id="c3bd0-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="c3bd0-108">Navigācijas izvēlnes moduļi atbalsta arī statiskus izvēlnes elementus, kas ir saistīti ar citām e-komercijas vietnēm.</span><span class="sxs-lookup"><span data-stu-id="c3bd0-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="c3bd0-109">Navigācijas izvēlnes moduli var pievienot lapas galvenes modulim.</span><span class="sxs-lookup"><span data-stu-id="c3bd0-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="c3bd0-110">Tēmā Fabrikam navigācijas izvēlne pēc noklusējuma rāda divus līmeņus.</span><span class="sxs-lookup"><span data-stu-id="c3bd0-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="c3bd0-111">Tēmā Starter navigācijas izvēlne pēc noklusējuma rāda trīs līmeņus.</span><span class="sxs-lookup"><span data-stu-id="c3bd0-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="c3bd0-112">Lai mainītu uz līmeņu skaitu, tēmā ir nepieciešams skata paplašinājums.</span><span class="sxs-lookup"><span data-stu-id="c3bd0-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="c3bd0-113">Sekojošajā attēlā redzams vietnes Fabrikam navigācijas izvēlnes piemērs ar diviem kategoriju hierarhijas līmeņiem un dažiem statiskiem izvēlnes elementiem.</span><span class="sxs-lookup"><span data-stu-id="c3bd0-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="c3bd0-114">![Navigācijas izvēlnes moduļa piemērs](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="c3bd0-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="c3bd0-115">Navigācijas izvēlnes moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="c3bd0-115">Navigation menu module properties</span></span>

| <span data-ttu-id="c3bd0-116">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="c3bd0-116">Property name</span></span>             | <span data-ttu-id="c3bd0-117">Vērtība</span><span class="sxs-lookup"><span data-stu-id="c3bd0-117">Value</span></span>                 | <span data-ttu-id="c3bd0-118">Apraksts</span><span class="sxs-lookup"><span data-stu-id="c3bd0-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="c3bd0-119">Modulis</span><span class="sxs-lookup"><span data-stu-id="c3bd0-119">Source</span></span>                  | <span data-ttu-id="c3bd0-120">**Mazumtirdzniecība**, **Manuāla autorēšana**, **Mazumtirdzniecība un manuāla autorēšana**</span><span class="sxs-lookup"><span data-stu-id="c3bd0-120">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="c3bd0-121">Vērtība **Mazumtirdzniecība** ļauj navigācijas izvēlnē parādīt kanāla navigācijas hierarhiju no Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="c3bd0-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="c3bd0-122">Vērtība **Manuālā autorēšana** ļauj pārraudzīt statiskos izvēlnes vienumus.</span><span class="sxs-lookup"><span data-stu-id="c3bd0-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="c3bd0-123">Vērtība **Mazumtirdzniecība un manuālā autorēšana** ļauj kombinēt abas.</span><span class="sxs-lookup"><span data-stu-id="c3bd0-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="c3bd0-124">Rādīt kategoriju attēlus</span><span class="sxs-lookup"><span data-stu-id="c3bd0-124">Show category images</span></span> | <span data-ttu-id="c3bd0-125">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="c3bd0-125">**True** or **False**</span></span>    | <span data-ttu-id="c3bd0-126">Ja iespējots, šis rekvizīts parāda kategoriju attēlus navigācijas izvēlnē, kā definēts Commerce Headquarters katrai kategorijai.</span><span class="sxs-lookup"><span data-stu-id="c3bd0-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="c3bd0-127">Pievienots Commerce izlaidumā 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="c3bd0-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="c3bd0-128">Statisks izvēlnes elements</span><span class="sxs-lookup"><span data-stu-id="c3bd0-128">Static menu item</span></span>| <span data-ttu-id="c3bd0-129">Vērtību masīvs</span><span class="sxs-lookup"><span data-stu-id="c3bd0-129">Array of values</span></span>| <span data-ttu-id="c3bd0-130">Statiski izvēlnes elementi, kas saista izvēlnes elementa nosaukumu ar saiti uz statisku vietnes lapu.</span><span class="sxs-lookup"><span data-stu-id="c3bd0-130">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="c3bd0-131">Varat izveidot izvēlnes elementus zem citiem izvēlnes elementiem.</span><span class="sxs-lookup"><span data-stu-id="c3bd0-131">You can create menu items below other menu items.</span></span> <span data-ttu-id="c3bd0-132">Pēc noklusējuma statiskās izvēlnes parādās saknes līmenī, un tās tiks pievienotas kanālu navigācijas hierarhijai, ja tāda pastāv.</span><span class="sxs-lookup"><span data-stu-id="c3bd0-132">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |

<span data-ttu-id="c3bd0-133">Sekojošajā attēlā redzams kategorijas attēla piemērs, kas parādīts Fabrikam vietnes navigācijas izvēlnē.</span><span class="sxs-lookup"><span data-stu-id="c3bd0-133">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="c3bd0-134">![Navigācijas izvēlnes moduļa piemērs ar kategoriju attēliem](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="c3bd0-134">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="c3bd0-135">Navigācijas izvēlnes moduļa pievienošana galvenes modulim</span><span class="sxs-lookup"><span data-stu-id="c3bd0-135">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="c3bd0-136">Detalizētu informāciju par navigācijas izvēlnes moduļa pievienošanu galvenes modulim skatiet [Galvenes modulis](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="c3bd0-136">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c3bd0-137">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="c3bd0-137">Additional resources</span></span>

[<span data-ttu-id="c3bd0-138">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="c3bd0-138">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c3bd0-139">Pirkšanas lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="c3bd0-139">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="c3bd0-140">Sīkfailu atbilstība</span><span class="sxs-lookup"><span data-stu-id="c3bd0-140">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="c3bd0-141">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="c3bd0-141">Header module</span></span>](author-header-module.md)
