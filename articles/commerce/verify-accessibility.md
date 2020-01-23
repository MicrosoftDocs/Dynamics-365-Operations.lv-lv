---
title: Lapas satura pieejamības pārbaude
description: Šajā tēmā ir aprakstīts, kā pārbaudīt lapas satura pieejamību Microsoft Dynamics 365 Commerce.
author: arotkin
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: arotkin
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 70604ed16d72e519724aeb2c33bd4a91a8b26c8c
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/09/2020
ms.locfileid: "2946045"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="733bf-103">Lapas satura pieejamības pārbaude</span><span class="sxs-lookup"><span data-stu-id="733bf-103">Verify page content accessibility</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="733bf-104">Šajā tēmā ir aprakstīts, kā pārbaudīt lapas satura pieejamību Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="733bf-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="733bf-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="733bf-105">Overview</span></span>

<span data-ttu-id="733bf-106">Kad esat pabeidzis izmainīt lapu, nepieciešams pārliecinieties, vai saturs ir pieejams ikvienam tīmekļa lietotājam.</span><span class="sxs-lookup"><span data-stu-id="733bf-106">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="733bf-107">Commerce autorēšanas rīkos varat viegli pārbaudīt lapas satura pieejamību, izmantojot integrēto pakalpojumu [Microsoft Accessibility Insights](https://accessibilityinsights.io/).</span><span class="sxs-lookup"><span data-stu-id="733bf-107">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="733bf-108">Šis pakalpojums pārbauda jūsu lapas saturu, izmantojot jaunākās [Globālā tīmekļa konsorcija (World Wide Web Consortium — W3C) pieejamības](https://www.w3.org/standards/webdesign/accessibility) vadlīnijas.</span><span class="sxs-lookup"><span data-stu-id="733bf-108">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="733bf-109">Lai varētu to izmantot, jāieslēdz [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integrācija nomnieka vai vietnes līmenī.</span><span class="sxs-lookup"><span data-stu-id="733bf-109">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="733bf-110">Microsoft Accessibility Insights ieslēgšana visām jūsu nomnieka vietnēm</span><span class="sxs-lookup"><span data-stu-id="733bf-110">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="733bf-111">Lai ieslēgtu [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integrāciju visām jūsu nomnieka Commerce vietnēm, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="733bf-111">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="733bf-112">Lai piekļūtu nomnieka iestatījumiem, jums ir jāpierakstās Commerce kā sistēmas administratoram.</span><span class="sxs-lookup"><span data-stu-id="733bf-112">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="733bf-113">Pierakstieties Commerce kā sistēmas administrators.</span><span class="sxs-lookup"><span data-stu-id="733bf-113">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="733bf-114">Kreisās puses navigācijas rūtī atlasiet **Nomnieka iestatījumi** (blakus zobrata simbolam), lai to izvērstu.</span><span class="sxs-lookup"><span data-stu-id="733bf-114">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="733bf-115">**Nomnieka iestatījumi** atlasiet **Līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="733bf-115">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="733bf-116">Iestatiet opciju **Pieejamības pārbaude** kā **Ieslēgts**.</span><span class="sxs-lookup"><span data-stu-id="733bf-116">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="733bf-117">Microsoft Accessibility Insights ieslēgšana vienai vietnei</span><span class="sxs-lookup"><span data-stu-id="733bf-117">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="733bf-118">Lai ieslēgtu [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integrāciju vienai Commerce vietnei, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="733bf-118">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="733bf-119">Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).</span><span class="sxs-lookup"><span data-stu-id="733bf-119">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="733bf-120">Kreisās puses navigācijas rūtī atlasiet **Vietnes iestatījumi**, lai to izvērstu.</span><span class="sxs-lookup"><span data-stu-id="733bf-120">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="733bf-121">**Vietnes iestatījumi** atlasiet **Līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="733bf-121">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="733bf-122">Iestatiet opciju **Pieejamības pārbaude** kā **Ieslēgts**.</span><span class="sxs-lookup"><span data-stu-id="733bf-122">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="733bf-123">Sākumlapas satura pieejamības pārbaude</span><span class="sxs-lookup"><span data-stu-id="733bf-123">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="733bf-124">Lai izmantotu integrēto [Microsoft Accessibility Insights](https://accessibilityinsights.io/) pakalpojumu sākumlapas satura skenēšanai un pārbaudei Commerce, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="733bf-124">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="733bf-125">Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).</span><span class="sxs-lookup"><span data-stu-id="733bf-125">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="733bf-126">Kreisās puses navigācijas rūtī atlasiet **Lapas**.</span><span class="sxs-lookup"><span data-stu-id="733bf-126">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="733bf-127">Atrodiet un atlasiet sākumlapu, lai to atvērtu to lapas redaktorā.</span><span class="sxs-lookup"><span data-stu-id="733bf-127">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="733bf-128">Komandjoslā atlasiet **Pārbaudīt pieejamību**.</span><span class="sxs-lookup"><span data-stu-id="733bf-128">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="733bf-129">Tiek parādīta lapa **Pārbaudīt pieejamību**.</span><span class="sxs-lookup"><span data-stu-id="733bf-129">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="733bf-130">Pēc skenēšanas pabeigšanas apskatiet pārskata saturu.</span><span class="sxs-lookup"><span data-stu-id="733bf-130">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="733bf-131">Ja kāda pārbaude nav izdevusies, atlasiet katru neizdevušos pārbaudes vienumu, lai to izvērstu un varētu skatīt detalizētu informāciju.</span><span class="sxs-lookup"><span data-stu-id="733bf-131">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="733bf-132">Lai pēc pārskata apskatīšanas to aizvērtu, ritiniet līdz lapas **Pārbaudīt pieejamību** apakšai un atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="733bf-132">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="733bf-133">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="733bf-133">Additional resources</span></span>

[<span data-ttu-id="733bf-134">Esošās vietnes lapas modificēšana</span><span class="sxs-lookup"><span data-stu-id="733bf-134">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="733bf-135">Jaunas vietnes lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="733bf-135">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="733bf-136">Lapas izkārtojumu atlase</span><span class="sxs-lookup"><span data-stu-id="733bf-136">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="733bf-137">SEO metadatu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="733bf-137">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="733bf-138">Lapas saglabāšana, priekšskatīšana un publicēšana</span><span class="sxs-lookup"><span data-stu-id="733bf-138">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="733bf-139">Preces lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="733bf-139">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="733bf-140">Kategorijas ielādes lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="733bf-140">Enrich a category landing page</span></span>](enrich-category-page.md)
