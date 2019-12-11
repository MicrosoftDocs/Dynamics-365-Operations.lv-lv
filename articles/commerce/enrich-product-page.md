---
title: Preces lapas papildināšana
description: Šajā tēmā aprakstīts, kā papildināt preces lapu Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: ef9e65b2027a41ca152afaf20ac2fb9a69cd9b96
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698146"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="07709-103">Preces lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="07709-103">Enrich a product page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="07709-104">Šajā tēmā aprakstīts, kā papildināt preces lapu Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="07709-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="07709-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="07709-105">Overview</span></span>

<span data-ttu-id="07709-106">Pēc noklusējuma jūsu vietne izmanto vispārējo lapu, lai parādītu preces datus.</span><span class="sxs-lookup"><span data-stu-id="07709-106">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="07709-107">Šajā lapā ir ietverta pamatinformācija par preci un vadīklas, kas nepieciešamas tās pārdošanai.</span><span class="sxs-lookup"><span data-stu-id="07709-107">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="07709-108">Tomēr varat papildināt no Retail servera nākošo informāciju ar papildu attēliem vai tekstu par konkrēto preci.</span><span class="sxs-lookup"><span data-stu-id="07709-108">However, you can supplement the information that comes from the Retail Server with additional images or text for a specific product.</span></span> <span data-ttu-id="07709-109">Šis process ir pazīstams kā preces lapas papildināšana.</span><span class="sxs-lookup"><span data-stu-id="07709-109">This process is known as enriching the product page.</span></span>

<span data-ttu-id="07709-110">Daudzos gadījumos jums vajadzēs savām precēm izmantot specifisku papildu saturu.</span><span class="sxs-lookup"><span data-stu-id="07709-110">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="07709-111">Kad autorēšanas rīkā dosieties uz **Mazumtirdzniecība**, redzēsiet preču sarakstu no kanāla, kas ir piešķirts vietnei.</span><span class="sxs-lookup"><span data-stu-id="07709-111">When you go to **Retail** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="07709-112">Šajā sarakstā kolonna **Papildināts** norāda, vai preces lapa par preci ir papildināta.</span><span class="sxs-lookup"><span data-stu-id="07709-112">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="07709-113">Ja kolonnā izdarīta atzīme, šai precei ir papildināta preces lapa.</span><span class="sxs-lookup"><span data-stu-id="07709-113">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="07709-114">Ja atzīme nav izdarīta, precei tiek izmantota noklusējuma preces lapa un saturs.</span><span class="sxs-lookup"><span data-stu-id="07709-114">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="07709-115">Varat priekšskatīt gan papildinātas, gan nepapildinātas preces lapas, sarakstā atlasot preces nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="07709-115">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="07709-116">Preces lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="07709-116">Enrich a product page</span></span>

<span data-ttu-id="07709-117">Lai papildinātu preces lapu, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="07709-117">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="07709-118">Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).</span><span class="sxs-lookup"><span data-stu-id="07709-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="07709-119">Navigācijas rūtī kreisajā pusē atlasiet **Preces**.</span><span class="sxs-lookup"><span data-stu-id="07709-119">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="07709-120">Atlasiet jebkuru preci, kurai nav papildinātas preces lapas.</span><span class="sxs-lookup"><span data-stu-id="07709-120">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="07709-121">Darbību rūtī atlasiet **Papildināt preces lapu**.</span><span class="sxs-lookup"><span data-stu-id="07709-121">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="07709-122">Atlasiet **PDP veidne** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="07709-122">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="07709-123">Lapas strukturējuma kokā kreisajā izvērsiet slotu **Galvenais**.</span><span class="sxs-lookup"><span data-stu-id="07709-123">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="07709-124">Atlasiet daudzpunktes pogu (**...**) slotam **Galvenais** un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="07709-124">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="07709-125">Atlasiet **2. konteiners** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="07709-125">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="07709-126">Atlasiet daudzpunktes pogu **2. konteiners** un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="07709-126">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="07709-127">Atlasiet **Līdzeklis** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="07709-127">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="07709-128">Rekvizītu rūtī labajā pusē laukā **Bagātināts teksts** ievadiet atjaunināto preces aprakstu.</span><span class="sxs-lookup"><span data-stu-id="07709-128">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="07709-129">Laukā **Virsraksts** ievadiet virsraksta tekstu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="07709-129">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="07709-130">Atlasiet **Saglabāt** un pēc tam **Pārbaudīt**.</span><span class="sxs-lookup"><span data-stu-id="07709-130">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="07709-131">Laukā **Komentāri** ievadiet **Papildināta prece** un pēc tam atlasiet **Labi**,</span><span class="sxs-lookup"><span data-stu-id="07709-131">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="07709-132">Atlasiet **Priekšskatījums**, lai priekšskatītu papildinātās preces lapu.</span><span class="sxs-lookup"><span data-stu-id="07709-132">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="07709-133">Kad esat pabeidzis, aizveriet priekšskatījuma cilni, lai atgrieztos autorēšanas rīkā.</span><span class="sxs-lookup"><span data-stu-id="07709-133">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="07709-134">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="07709-134">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="07709-135">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="07709-135">Additional resources</span></span>

[<span data-ttu-id="07709-136">Esošās vietnes lapas modificēšana</span><span class="sxs-lookup"><span data-stu-id="07709-136">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="07709-137">Jaunas vietnes lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="07709-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="07709-138">Lapas izkārtojumu atlase</span><span class="sxs-lookup"><span data-stu-id="07709-138">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="07709-139">SEO metadatu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="07709-139">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="07709-140">Lapas saglabāšana, priekšskatīšana un publicēšana</span><span class="sxs-lookup"><span data-stu-id="07709-140">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="07709-141">Kategorijas ielādes lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="07709-141">Enrich a category landing page</span></span>](enrich-category-page.md)

