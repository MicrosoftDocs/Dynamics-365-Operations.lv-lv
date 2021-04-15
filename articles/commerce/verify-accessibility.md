---
title: Lapas satura pieejamības pārbaude
description: Šajā tēmā ir aprakstīts, kā pārbaudīt lapas satura pieejamību programmā Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 885696c13b0e5353e6dbd9dc21cf075d5e301786
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791635"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="4ad6a-103">Lapas satura pieejamības pārbaude</span><span class="sxs-lookup"><span data-stu-id="4ad6a-103">Verify page content accessibility</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4ad6a-104">Šajā tēmā ir aprakstīts, kā pārbaudīt lapas satura pieejamību programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4ad6a-105">Kad esat pabeidzis izmainīt lapu, nepieciešams pārliecinieties, vai saturs ir pieejams ikvienam tīmekļa lietotājam.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-105">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="4ad6a-106">Commerce autorēšanas rīkos varat viegli pārbaudīt lapas satura pieejamību, izmantojot integrēto pakalpojumu [Microsoft Accessibility Insights](https://accessibilityinsights.io/).</span><span class="sxs-lookup"><span data-stu-id="4ad6a-106">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="4ad6a-107">Šis pakalpojums pārbauda jūsu lapas saturu, izmantojot jaunākās [Globālā tīmekļa konsorcija (World Wide Web Consortium — W3C) pieejamības](https://www.w3.org/standards/webdesign/accessibility) vadlīnijas.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-107">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="4ad6a-108">Lai varētu to izmantot, jāieslēdz [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integrācija nomnieka vai vietnes līmenī.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-108">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="4ad6a-109">Microsoft Accessibility Insights ieslēgšana visām jūsu nomnieka vietnēm</span><span class="sxs-lookup"><span data-stu-id="4ad6a-109">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="4ad6a-110">Lai ieslēgtu [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integrāciju visām jūsu nomnieka Commerce vietnēm, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-110">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="4ad6a-111">Lai piekļūtu nomnieka iestatījumiem, jums ir jāpierakstās Commerce kā sistēmas administratoram.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-111">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="4ad6a-112">Pierakstieties Commerce kā sistēmas administrators.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-112">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="4ad6a-113">Kreisās puses navigācijas rūtī atlasiet **Nomnieka iestatījumi** (blakus zobrata simbolam), lai to izvērstu.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-113">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="4ad6a-114">**Nomnieka iestatījumi** atlasiet **Līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-114">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="4ad6a-115">Iestatiet opciju **Pieejamības pārbaude** kā **Ieslēgts**.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-115">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="4ad6a-116">Microsoft Accessibility Insights ieslēgšana vienai vietnei</span><span class="sxs-lookup"><span data-stu-id="4ad6a-116">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="4ad6a-117">Lai ieslēgtu [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integrāciju vienai Commerce vietnei, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-117">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="4ad6a-118">Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).</span><span class="sxs-lookup"><span data-stu-id="4ad6a-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="4ad6a-119">Kreisās puses navigācijas rūtī atlasiet **Vietnes iestatījumi**, lai to izvērstu.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-119">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="4ad6a-120">**Vietnes iestatījumi** atlasiet **Līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-120">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="4ad6a-121">Iestatiet opciju **Pieejamības pārbaude** kā **Ieslēgts**.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-121">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="4ad6a-122">Sākumlapas satura pieejamības pārbaude</span><span class="sxs-lookup"><span data-stu-id="4ad6a-122">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="4ad6a-123">Lai izmantotu integrēto [Microsoft Accessibility Insights](https://accessibilityinsights.io/) pakalpojumu sākumlapas satura skenēšanai un pārbaudei Commerce, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-123">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="4ad6a-124">Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).</span><span class="sxs-lookup"><span data-stu-id="4ad6a-124">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="4ad6a-125">Kreisās puses navigācijas rūtī atlasiet **Lapas**.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-125">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="4ad6a-126">Atrodiet un atlasiet sākumlapu, lai to atvērtu to lapas redaktorā.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-126">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="4ad6a-127">Komandjoslā atlasiet **Pārbaudīt pieejamību**.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-127">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="4ad6a-128">Tiek parādīta lapa **Pārbaudīt pieejamību**.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-128">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="4ad6a-129">Pēc skenēšanas pabeigšanas apskatiet pārskata saturu.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-129">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="4ad6a-130">Ja kāda pārbaude nav izdevusies, atlasiet katru neizdevušos pārbaudes vienumu, lai to izvērstu un varētu skatīt detalizētu informāciju.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-130">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="4ad6a-131">Lai pēc pārskata apskatīšanas to aizvērtu, ritiniet līdz lapas **Pārbaudīt pieejamību** apakšai un atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-131">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4ad6a-132">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="4ad6a-132">Additional resources</span></span>

[<span data-ttu-id="4ad6a-133">Esošās vietnes lapas modificēšana</span><span class="sxs-lookup"><span data-stu-id="4ad6a-133">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="4ad6a-134">Jaunas vietnes lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="4ad6a-134">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="4ad6a-135">Lapas izkārtojumu atlase</span><span class="sxs-lookup"><span data-stu-id="4ad6a-135">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="4ad6a-136">SEO metadatu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="4ad6a-136">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="4ad6a-137">Lapas saglabāšana, priekšskatīšana un publicēšana</span><span class="sxs-lookup"><span data-stu-id="4ad6a-137">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="4ad6a-138">Preces lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="4ad6a-138">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="4ad6a-139">Kategorijas ielādes lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="4ad6a-139">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="4ad6a-140">Dinamisko e-komercijas lapu izveidošana, pamatojoties uz URL parametriem</span><span class="sxs-lookup"><span data-stu-id="4ad6a-140">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
