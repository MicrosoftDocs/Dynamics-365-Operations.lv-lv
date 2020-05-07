---
title: Preces lapas papildināšana
description: Šajā tēmā aprakstīts, kā papildināt preces lapu Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 12508a80c440894ec6e2073b5e550846480e6c45
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269824"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="28d71-103">Preces lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="28d71-103">Enrich a product page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="28d71-104">Šajā tēmā aprakstīts, kā papildināt preces lapu Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="28d71-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="28d71-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="28d71-105">Overview</span></span>

<span data-ttu-id="28d71-106">Pēc noklusējuma jūsu vietne izmanto vispārējo lapu, lai parādītu preces datus.</span><span class="sxs-lookup"><span data-stu-id="28d71-106">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="28d71-107">Šajā lapā ir ietverta pamatinformācija par preci un vadīklas, kas nepieciešamas tās pārdošanai.</span><span class="sxs-lookup"><span data-stu-id="28d71-107">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="28d71-108">Tomēr varat papildināt no Tirdzniecības mēroga vienības servera nākošo informāciju ar papildu attēliem vai tekstu par konkrēto preci.</span><span class="sxs-lookup"><span data-stu-id="28d71-108">However, you can supplement the information that comes from the Commerce Scale Unit with additional images or text for a specific product.</span></span> <span data-ttu-id="28d71-109">Šis process ir pazīstams kā preces lapas papildināšana.</span><span class="sxs-lookup"><span data-stu-id="28d71-109">This process is known as enriching the product page.</span></span>

<span data-ttu-id="28d71-110">Daudzos gadījumos jums vajadzēs savām precēm izmantot specifisku papildu saturu.</span><span class="sxs-lookup"><span data-stu-id="28d71-110">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="28d71-111">Kad autorēšanas rīkā dosieties uz **Mazumtirdzniecība un komercija**, redzēsiet preču sarakstu no kanāla, kas ir piešķirts vietnei.</span><span class="sxs-lookup"><span data-stu-id="28d71-111">When you go to **Retail and Commerce** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="28d71-112">Šajā sarakstā kolonna **Papildināts** norāda, vai preces lapa par preci ir papildināta.</span><span class="sxs-lookup"><span data-stu-id="28d71-112">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="28d71-113">Ja kolonnā izdarīta atzīme, šai precei ir papildināta preces lapa.</span><span class="sxs-lookup"><span data-stu-id="28d71-113">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="28d71-114">Ja atzīme nav izdarīta, precei tiek izmantota noklusējuma preces lapa un saturs.</span><span class="sxs-lookup"><span data-stu-id="28d71-114">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="28d71-115">Varat priekšskatīt gan papildinātas, gan nepapildinātas preces lapas, sarakstā atlasot preces nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="28d71-115">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="28d71-116">Preces lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="28d71-116">Enrich a product page</span></span>

<span data-ttu-id="28d71-117">Lai papildinātu preces lapu, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="28d71-117">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="28d71-118">Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).</span><span class="sxs-lookup"><span data-stu-id="28d71-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="28d71-119">Navigācijas rūtī kreisajā pusē atlasiet **Preces**.</span><span class="sxs-lookup"><span data-stu-id="28d71-119">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="28d71-120">Atlasiet jebkuru preci, kurai nav papildinātas preces lapas.</span><span class="sxs-lookup"><span data-stu-id="28d71-120">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="28d71-121">Darbību rūtī atlasiet **Papildināt preces lapu**.</span><span class="sxs-lookup"><span data-stu-id="28d71-121">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="28d71-122">Atlasiet **PDP veidne** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="28d71-122">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="28d71-123">Lapas strukturējuma kokā kreisajā izvērsiet slotu **Galvenais**.</span><span class="sxs-lookup"><span data-stu-id="28d71-123">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="28d71-124">Atlasiet daudzpunktes pogu (**...**) slotam **Galvenais** un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="28d71-124">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="28d71-125">Atlasiet **2. konteiners** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="28d71-125">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="28d71-126">Atlasiet daudzpunktes pogu **2. konteiners** un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="28d71-126">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="28d71-127">Atlasiet **Līdzeklis** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="28d71-127">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="28d71-128">Rekvizītu rūtī labajā pusē laukā **Bagātināts teksts** ievadiet atjaunināto preces aprakstu.</span><span class="sxs-lookup"><span data-stu-id="28d71-128">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="28d71-129">Laukā **Virsraksts** ievadiet virsraksta tekstu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="28d71-129">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="28d71-130">Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="28d71-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="28d71-131">Laukā **Komentāri** ievadiet **Papildināta prece** un pēc tam atlasiet **Labi**,</span><span class="sxs-lookup"><span data-stu-id="28d71-131">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="28d71-132">Atlasiet **Priekšskatījums**, lai priekšskatītu papildinātās preces lapu.</span><span class="sxs-lookup"><span data-stu-id="28d71-132">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="28d71-133">Kad esat pabeidzis, aizveriet priekšskatījuma cilni, lai atgrieztos autorēšanas rīkā.</span><span class="sxs-lookup"><span data-stu-id="28d71-133">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="28d71-134">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="28d71-134">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="28d71-135">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="28d71-135">Additional resources</span></span>

[<span data-ttu-id="28d71-136">Esošās vietnes lapas modificēšana</span><span class="sxs-lookup"><span data-stu-id="28d71-136">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="28d71-137">Jaunas vietnes lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="28d71-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="28d71-138">Lapas izkārtojumu atlase</span><span class="sxs-lookup"><span data-stu-id="28d71-138">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="28d71-139">SEO metadatu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="28d71-139">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="28d71-140">Lapas saglabāšana, priekšskatīšana un publicēšana</span><span class="sxs-lookup"><span data-stu-id="28d71-140">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="28d71-141">Kategorijas ielādes lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="28d71-141">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="28d71-142">Lapas satura pieejamības pārbaude</span><span class="sxs-lookup"><span data-stu-id="28d71-142">Verify page content accessibility</span></span>](verify-accessibility.md)
