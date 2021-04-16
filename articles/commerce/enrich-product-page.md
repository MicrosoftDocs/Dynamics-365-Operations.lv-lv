---
title: Preces lapas papildināšana
description: Šajā tēmā aprakstīts, kā papildināt preces lapu Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6c1a9474ed514426386b1d7b4a72b62129cdb8a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799052"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="cf720-103">Preces lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="cf720-103">Enrich a product page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cf720-104">Šajā tēmā aprakstīts, kā papildināt preces lapu Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cf720-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="cf720-105">Pēc noklusējuma jūsu vietne izmanto vispārējo lapu, lai parādītu preces datus.</span><span class="sxs-lookup"><span data-stu-id="cf720-105">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="cf720-106">Šajā lapā ir ietverta pamatinformācija par preci un vadīklas, kas nepieciešamas tās pārdošanai.</span><span class="sxs-lookup"><span data-stu-id="cf720-106">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="cf720-107">Tomēr varat papildināt no Tirdzniecības mēroga vienības servera nākošo informāciju ar papildu attēliem vai tekstu par konkrēto preci.</span><span class="sxs-lookup"><span data-stu-id="cf720-107">However, you can supplement the information that comes from the Commerce Scale Unit with additional images or text for a specific product.</span></span> <span data-ttu-id="cf720-108">Šis process ir pazīstams kā preces lapas papildināšana.</span><span class="sxs-lookup"><span data-stu-id="cf720-108">This process is known as enriching the product page.</span></span>

<span data-ttu-id="cf720-109">Daudzos gadījumos jums vajadzēs savām precēm izmantot specifisku papildu saturu.</span><span class="sxs-lookup"><span data-stu-id="cf720-109">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="cf720-110">Kad autorēšanas rīkā dosieties uz **Mazumtirdzniecība un komercija**, redzēsiet preču sarakstu no kanāla, kas ir piešķirts vietnei.</span><span class="sxs-lookup"><span data-stu-id="cf720-110">When you go to **Retail and Commerce** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="cf720-111">Šajā sarakstā kolonna **Papildināts** norāda, vai preces lapa par preci ir papildināta.</span><span class="sxs-lookup"><span data-stu-id="cf720-111">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="cf720-112">Ja kolonnā izdarīta atzīme, šai precei ir papildināta preces lapa.</span><span class="sxs-lookup"><span data-stu-id="cf720-112">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="cf720-113">Ja atzīme nav izdarīta, precei tiek izmantota noklusējuma preces lapa un saturs.</span><span class="sxs-lookup"><span data-stu-id="cf720-113">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="cf720-114">Varat priekšskatīt gan papildinātas, gan nepapildinātas preces lapas, sarakstā atlasot preces nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="cf720-114">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="cf720-115">Preces lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="cf720-115">Enrich a product page</span></span>

<span data-ttu-id="cf720-116">Lai papildinātu preces lapu, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="cf720-116">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="cf720-117">Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).</span><span class="sxs-lookup"><span data-stu-id="cf720-117">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="cf720-118">Navigācijas rūtī kreisajā pusē atlasiet **Preces**.</span><span class="sxs-lookup"><span data-stu-id="cf720-118">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="cf720-119">Atlasiet jebkuru preci, kurai nav papildinātas preces lapas.</span><span class="sxs-lookup"><span data-stu-id="cf720-119">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="cf720-120">Darbību rūtī atlasiet **Papildināt preces lapu**.</span><span class="sxs-lookup"><span data-stu-id="cf720-120">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="cf720-121">Atlasiet **PDP veidne** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="cf720-121">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="cf720-122">Lapas strukturējuma kokā kreisajā izvērsiet slotu **Galvenais**.</span><span class="sxs-lookup"><span data-stu-id="cf720-122">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="cf720-123">Atlasiet daudzpunktes pogu (**...**) slotam **Galvenais** un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="cf720-123">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="cf720-124">Atlasiet **2. konteiners** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="cf720-124">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="cf720-125">Atlasiet daudzpunktes pogu **2. konteiners** un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="cf720-125">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="cf720-126">Atlasiet **Līdzeklis** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="cf720-126">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="cf720-127">Rekvizītu rūtī labajā pusē laukā **Bagātināts teksts** ievadiet atjaunināto preces aprakstu.</span><span class="sxs-lookup"><span data-stu-id="cf720-127">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="cf720-128">Laukā **Virsraksts** ievadiet virsraksta tekstu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="cf720-128">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="cf720-129">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="cf720-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="cf720-130">Laukā **Komentāri** ievadiet **Papildināta prece** un pēc tam atlasiet **Labi**,</span><span class="sxs-lookup"><span data-stu-id="cf720-130">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="cf720-131">Atlasiet **Priekšskatījums**, lai priekšskatītu papildinātās preces lapu.</span><span class="sxs-lookup"><span data-stu-id="cf720-131">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="cf720-132">Kad esat pabeidzis, aizveriet priekšskatījuma cilni, lai atgrieztos autorēšanas rīkā.</span><span class="sxs-lookup"><span data-stu-id="cf720-132">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="cf720-133">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="cf720-133">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cf720-134">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="cf720-134">Additional resources</span></span>

[<span data-ttu-id="cf720-135">Esošās vietnes lapas modificēšana</span><span class="sxs-lookup"><span data-stu-id="cf720-135">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="cf720-136">Jaunas vietnes lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="cf720-136">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="cf720-137">Lapas izkārtojumu atlase</span><span class="sxs-lookup"><span data-stu-id="cf720-137">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="cf720-138">SEO metadatu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="cf720-138">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="cf720-139">Lapas saglabāšana, priekšskatīšana un publicēšana</span><span class="sxs-lookup"><span data-stu-id="cf720-139">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="cf720-140">Kategorijas ielādes lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="cf720-140">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="cf720-141">Lapas satura pieejamības pārbaude</span><span class="sxs-lookup"><span data-stu-id="cf720-141">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="cf720-142">Dinamisko e-komercijas lapu izveidošana, pamatojoties uz URL parametriem</span><span class="sxs-lookup"><span data-stu-id="cf720-142">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
