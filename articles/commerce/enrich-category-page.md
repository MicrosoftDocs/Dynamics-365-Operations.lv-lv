---
title: Kategorijas ielādes lapas papildināšana
description: Šajā tēma ir ietverta kategorijas lapu papildināšana Dynamics 365 Commerce.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5e18439fc0e91619cade33b83b87be0d5c4d1040
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799015"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="083a2-103">Kategorijas ielādes lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="083a2-103">Enrich a category landing page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="083a2-104">Šajā tēma ir ietverta kategorijas lapu papildināšana Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="083a2-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="083a2-105">Commerce nodrošina noklusējuma kategorijas mērķlapu, kas tiek izmantota, kad tiek parādīti kategorijas dati.</span><span class="sxs-lookup"><span data-stu-id="083a2-105">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="083a2-106">Noklusējuma kategorijas lapa satur obligātos elementus, piemēram, uzlabotājus, kategorizētas preces izvietošanu, šķirošanas iespējas, izvēles kopsavilkumu un lappušu numerācijas vadīklas.</span><span class="sxs-lookup"><span data-stu-id="083a2-106">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="083a2-107">Tomēr, tā vietā, lai izmantotu noklusējuma kategorijas lapu, iespējams, vēlēsieties izmantot "papildinātu" kategorijas mērķlapu, kam ir vairāk satura un specifiskāki elementi.</span><span class="sxs-lookup"><span data-stu-id="083a2-107">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="083a2-108">Parasta papildināšana var ietvert kategorijai specifiska mārketinga satura pievienošanu kategorijas lapai.</span><span class="sxs-lookup"><span data-stu-id="083a2-108">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="083a2-109">Šis saturs var ietvert vairāku preces izvietošanu dažādās kategorijās papildu pārdošanas nolūkam, redakcijas sarakstus, attēlus, video un citu tekstu.</span><span class="sxs-lookup"><span data-stu-id="083a2-109">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="083a2-110">Varat vai nu modificēt noklusējuma kategorijas lapu, vai definēt citu kategorijas lapu noteiktai kategorijai.</span><span class="sxs-lookup"><span data-stu-id="083a2-110">You can either modify the default category page or define a different category page for a specific category.</span></span>

![Bagātināta kategorijas ielādes lapa](./media/CategoryLandingPages.png)

<span data-ttu-id="083a2-112">Commerce vietnes veidotājā lapa **Prece** ietver kategoriju sarakstu no kanāla, kas piešķirts vietnei.</span><span class="sxs-lookup"><span data-stu-id="083a2-112">In Commerce site builder, the **Products** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="083a2-113">Ja kategorijas lapai atlasīts statuss **Papildināts**, šī kategorijas lapa ir tikusi papildināta.</span><span class="sxs-lookup"><span data-stu-id="083a2-113">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="083a2-114">Pretējā gadījumā kategorijai tiek izmantota noklusējuma kategorijas lapa un saturs.</span><span class="sxs-lookup"><span data-stu-id="083a2-114">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="083a2-115">Varat priekšskatīt gan papildinātas, gan nepapildinātas kategorijas lapas, atlasot kategorijas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="083a2-115">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="083a2-116">Lai papildinātu kategorijas lapu, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="083a2-116">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="083a2-117">Lapā **Preces** atlasiet tās kategorijas nosaukumu, kurai vēlaties papildināt kategorijas lapu.</span><span class="sxs-lookup"><span data-stu-id="083a2-117">On the **Products** page, select the name of the category for which you want to enrich the category page.</span></span> <span data-ttu-id="083a2-118">Lapas redaktorā tiek atvērta atlasītās kategorijas noklusējuma kategorijas lapa.</span><span class="sxs-lookup"><span data-stu-id="083a2-118">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="083a2-119">Atlasiet **Papildināt kategorijas lapu**.</span><span class="sxs-lookup"><span data-stu-id="083a2-119">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="083a2-120">Atlasiet papildinātās kategorijas lapas veidni.</span><span class="sxs-lookup"><span data-stu-id="083a2-120">Select a template for the enriched category page.</span></span> <span data-ttu-id="083a2-121">Ja izdarāt tikai nelielas izmaiņas, varat atlasīt noklusējuma kategorijas lapu.</span><span class="sxs-lookup"><span data-stu-id="083a2-121">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="083a2-122">Vai arī varat atlasīt noteiktas kategorijas lapas veidni.</span><span class="sxs-lookup"><span data-stu-id="083a2-122">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="083a2-123">Kad atlasāt veidni, tiek atvērts lapas redaktors, un atlasītā veidne tiek izmantota, lai izveidotu jaunu kategorijas lapu atlasītajai kategorijai.</span><span class="sxs-lookup"><span data-stu-id="083a2-123">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="083a2-124">Lapa tiek izrakstīta jums, un tagad varat veikt savas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="083a2-124">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="083a2-125">Moduļi, kas izmanto kategorijas specifikācijas datus, izmanto datus no atlasītās kategorijas.</span><span class="sxs-lookup"><span data-stu-id="083a2-125">Modules that use category specification data use the data from your selected category.</span></span> <span data-ttu-id="083a2-126">Jūsu atlasītā veidnes iestatījumi nosaka izmaiņas, ko varat veikt.</span><span class="sxs-lookup"><span data-stu-id="083a2-126">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="083a2-127">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="083a2-127">Additional resources</span></span>

[<span data-ttu-id="083a2-128">Esošās vietnes lapas modificēšana</span><span class="sxs-lookup"><span data-stu-id="083a2-128">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="083a2-129">Jaunas vietnes lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="083a2-129">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="083a2-130">Lapas izkārtojumu atlase</span><span class="sxs-lookup"><span data-stu-id="083a2-130">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="083a2-131">SEO metadatu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="083a2-131">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="083a2-132">Lapas saglabāšana, priekšskatīšana un publicēšana</span><span class="sxs-lookup"><span data-stu-id="083a2-132">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="083a2-133">Preces lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="083a2-133">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="083a2-134">Lapas satura pieejamības pārbaude</span><span class="sxs-lookup"><span data-stu-id="083a2-134">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="083a2-135">Dinamisko e-komercijas lapu izveidošana, pamatojoties uz URL parametriem</span><span class="sxs-lookup"><span data-stu-id="083a2-135">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
