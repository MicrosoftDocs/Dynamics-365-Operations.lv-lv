---
title: Dinamisku e-komercijas lapu izveide, pamatojoties uz URL parametriem
description: Šajā tēmā aprakstīts, kā iestatīts Microsoft Dynamics 365 Commerce e-komercijas lapu, kura var apkalpot dinamisku saturu, pamatojoties URL parametros.
author: StuHarg
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8f59b80880e6947e1b45c110df0e78d4bdd57c5d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795815"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a><span data-ttu-id="bf4e4-103">Dinamisku e-komercijas lapu izveide, pamatojoties uz URL parametriem</span><span class="sxs-lookup"><span data-stu-id="bf4e4-103">Create dynamic e-commerce pages based on URL parameters</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bf4e4-104">Šajā tēmā aprakstīts, kā iestatīts Microsoft Dynamics 365 Commerce e-komercijas lapu, kura var apkalpot dinamisku saturu, pamatojoties URL parametros.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-104">This topic describes how to set up a Microsoft Dynamics 365 Commerce e-commerce page that can serve dynamic content, based on URL parameters.</span></span>

<span data-ttu-id="bf4e4-105">E-komercijas lapu var konfigurēt, lai tā kalpotu dažādam saturam, pamatojoties uz segmentu vietrāža URL ceļā.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-105">An e-commerce page can be configured to serve different content, based on a segment in the URL path.</span></span> <span data-ttu-id="bf4e4-106">Tāpēc šī lapa ir pazīstama kā dinamiskā lapa.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-106">Therefore, the page is known as a dynamic page.</span></span> <span data-ttu-id="bf4e4-107">Segments tiek izmantots kā parametrs lapas satura izgūšanai.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-107">The segment is used as a parameter to retrieve the page content.</span></span> <span data-ttu-id="bf4e4-108">Piemēram, lapa, kas ir nosaukta par **blog\_viewer**, tiek izveidota un saistīta ar URL `https://fabrikam.com/blog`.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-108">For example, a page that is named **blog\_viewer** is created and associated with the URL `https://fabrikam.com/blog`.</span></span> <span data-ttu-id="bf4e4-109">Pēc tam šo lapu var izmantot, lai parādītu dažādu saturu, balstoties uz pēdējo segmentu URL ceļā.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-109">This page can then be used to show different content, based on the last segment in the URL path.</span></span> <span data-ttu-id="bf4e4-110">Piemēram, pēdējais segments vietrādī URL `https://fabrikam.com/blog/article-1` ir **article-1**.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-110">For example, the last segment in the URL `https://fabrikam.com/blog/article-1` is **article-1**.</span></span>

<span data-ttu-id="bf4e4-111">Atsevišķas pielāgotas lapas, kas ignorē dinamisko lapu, var tikt saistītas arī ar segmentiem vietrāža URL ceļā.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-111">Separate custom pages that override the dynamic page can also be associated with segments in the URL path.</span></span> <span data-ttu-id="bf4e4-112">Piemēram, lapa, kas ir nosaukta par **blog\_summary**, tiek izveidota un saistīta ar URL `https://fabrikam.com/blog/about-this-blog`.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-112">For example, a page that is named **blog\_summary** is created and associated with the URL `https://fabrikam.com/blog/about-this-blog`.</span></span> <span data-ttu-id="bf4e4-113">Kad tiek pieprasīts šis URL, tiek atgriezta **bloga\_kopsavilkuma** lapa, kas ir saistīta ar **/about-this-blog** parametru, nevis **blog\_viewer** lapa.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-113">When this URL is requested, the **blog\_summary** page that is associated with the **/about-this-blog** parameter is returned instead of the **blog\_viewer** page.</span></span>

> [!NOTE]
> <span data-ttu-id="bf4e4-114">Dinamisko lapu satura viesošanas, izgūšanas un rādīšanas funkcionalitāte tiek īstenota, izmantojot pielāgotu moduli.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-114">The functionality for hosting, retrieving, and showing dynamic page content is implemented by using a custom module.</span></span> <span data-ttu-id="bf4e4-115">Papildinformāciju skatiet šeit: [Tiešsaistes kanāla paplašināmība](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="bf4e4-115">For more information, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="set-up-a-dynamic-e-commerce-page"></a><span data-ttu-id="bf4e4-116">Dinamiskās e-komercijas lapas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="bf4e4-116">Set up a dynamic e-commerce page</span></span>

<span data-ttu-id="bf4e4-117">Lai iestatītu dinamisku e-komercijas lapu, ir jāizveido dinamiskā lapa, jāizveido pamata vietrādis URL un jākonfigurē maršruts dinamiskajā lapā.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-117">To set up a dynamic e-commerce page, you must create the dynamic page, create the base URL, and configure the route to the dynamic page.</span></span>

### <a name="create-the-page-that-will-serve-dynamic-content"></a><span data-ttu-id="bf4e4-118">Izveidot lapu, kurā tiks rādīts dinamisks saturs</span><span class="sxs-lookup"><span data-stu-id="bf4e4-118">Create the page that will serve dynamic content</span></span>

<span data-ttu-id="bf4e4-119">Lai izveidotu lapu, kurā tiks rādīts dinamisks saturs, izpildiet sekojošās darbības sadaļā [Pievienot jaunu vietnes lapu](add-new-page.md).</span><span class="sxs-lookup"><span data-stu-id="bf4e4-119">To create a page that will serve dynamic content, follow the steps in [Add a new site page](add-new-page.md).</span></span> <span data-ttu-id="bf4e4-120">Jūsu izveidotajai lapai būs nepieciešams ieviest moduli, kas izmanto pēdējo segmentu URL ceļā, lai izgūtu saturu no ārēja datu avota.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-120">The page that you create will require implementation of a module that uses the last segment in the URL path to retrieve content from an external data source.</span></span> <span data-ttu-id="bf4e4-121">Papildinformāciju par pielāgotu moduļa izstrādi skatiet sadaļā [Tiešsaistes kanāla paplašināmība](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="bf4e4-121">For more information about custom module development, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

### <a name="create-the-base-url-for-the-dynamic-page"></a><span data-ttu-id="bf4e4-122">Izveidot dinamiskās lapas pamata vietrādi URL</span><span class="sxs-lookup"><span data-stu-id="bf4e4-122">Create the base URL for the dynamic page</span></span>

<span data-ttu-id="bf4e4-123">Lai izveidotu pamata URL dinamiskajai lapai Commerce vietnes veidotājā, sekojiet šiem soļiem.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-123">To create the base URL for the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="bf4e4-124">Dodieties uz **Vietrāži URL** un atlasiet **Jauns \> Jauns URL**.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-124">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="bf4e4-125">Dialoglodziņā **Izveidot jaunu URL** atlasiet **Iekšējo lapu**.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-125">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="bf4e4-126">Sadaļā **URL ceļš** ievadiet ceļu, kas kalpos kā dinamiskās lapas sakne (šajā piemērā **/blog**).</span><span class="sxs-lookup"><span data-stu-id="bf4e4-126">Under **URL path**, enter the path that will serve as the root for the dynamic page (in this example, **/blog**).</span></span> <span data-ttu-id="bf4e4-127">Pēc tam atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-127">Then select **Next**.</span></span>
1. <span data-ttu-id="bf4e4-128">Dialoglodziņā **Atlasīt lapu** atlasiet izveidoto lapu, kura tiks rādīta kā dinamiskā lapa, un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-128">In the **Select a page** dialog box, select the page that you created to serve as the dynamic page, and then select **Save**.</span></span>
1. <span data-ttu-id="bf4e4-129">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-129">Select **Publish**.</span></span>

### <a name="configure-the-route-to-the-dynamic-page"></a><span data-ttu-id="bf4e4-130">Konfigurēt maršrutu uz dinamisko lapu</span><span class="sxs-lookup"><span data-stu-id="bf4e4-130">Configure the route to the dynamic page</span></span>

<span data-ttu-id="bf4e4-131">Lai konfigurētu maršrutu uz dinamisko lapu Commerce vietnes veidotājā, sekojiet šiem soļiem.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-131">To configure the route to the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="bf4e4-132">Dodieties uz **Vietnes iestatījumi \> Paplašinājumi**.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-132">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="bf4e4-133">Sadaļā **Parametrizēti URL ceļi** atlasiet **Pievienot** un pēc tam ievadiet URL ceļu, ko ievadījāt, kad izveidojāt URL (šajā piemērā **/blog**).</span><span class="sxs-lookup"><span data-stu-id="bf4e4-133">Under **Parameterized URL paths**, select **Add**, and then enter the URL path that you entered when you created the URL (in this example, **/blog**).</span></span>
1. <span data-ttu-id="bf4e4-134">Atlasiet **Saglabāt un publicēt**.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-134">Select **Save and publish**.</span></span>

<span data-ttu-id="bf4e4-135">Kad maršruts ir konfigurēts, visi pieprasījumi uz parametrizētu URL ceļu atgriezīs lapu, kas ir saistīta ar šo URL.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-135">After the route is configured, all requests to the parameterized URL path will return the page that is associated with that URL.</span></span> <span data-ttu-id="bf4e4-136">Ja jebkādi pieprasījumi ietver papildu segmentu, tiks atgriezta saistītā lapa, un lapas saturs tiks izgūts, kā parametru izmantojot segmentu.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-136">If any requests contain an additional segment, the associated page will be returned, and the page content will be retrieved by using the segment as a parameter.</span></span> <span data-ttu-id="bf4e4-137">Piemēram, `https://fabrikam.com/blog/article-1` atgriezīs **blog\_summary** lapu, un lapas saturs tiks izgūts, izmantojot **/article-1** parametru.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-137">For example, `https://fabrikam.com/blog/article-1` will return the **blog\_summary** page, and the page content will be retrieved by using the **/article-1** parameter.</span></span>

## <a name="override-a-parameterized-url-with-a-custom-page"></a><span data-ttu-id="bf4e4-138">Ignorēt parametrizētu URL ar pielāgotu lapu</span><span class="sxs-lookup"><span data-stu-id="bf4e4-138">Override a parameterized URL with a custom page</span></span>

<span data-ttu-id="bf4e4-139">Lai ignorētu parametrizētu URL ar pielāgotu lapu Commerce vietnes veidotājā, sekojiet šiem soļiem.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-139">To override a parameterized URL with a custom page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="bf4e4-140">Dodieties uz **Vietrāži URL** un atlasiet **Jauns \> Jauns URL**.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-140">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="bf4e4-141">Dialoglodziņā **Izveidot jaunu URL** atlasiet **Iekšējo lapu**.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-141">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="bf4e4-142">Sadaļā **URL ceļš** ievadiet ceļu, kas ietver ignorēšanas segmentu (šajā piemērā, **/blog/about-this-blog**).</span><span class="sxs-lookup"><span data-stu-id="bf4e4-142">Under **URL path**, enter the path that includes the segment to override (in this example, **/blog/about-this-blog**).</span></span> <span data-ttu-id="bf4e4-143">Pēc tam atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-143">Then select **Next**.</span></span>
1. <span data-ttu-id="bf4e4-144">Dialoglodziņā **Atlasīt lapu** atlasiet pielāgoto lapu un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-144">In the **Select a page** dialog box, select the custom page, and then select **Save**.</span></span>
1. <span data-ttu-id="bf4e4-145">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-145">Select **Publish**.</span></span>
1. <span data-ttu-id="bf4e4-146">Ja pielāgotā lapa vēl nav publicēta, atveriet lapas, dodieties uz **Lapas**, atlasiet pielāgoto lapu un tad atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-146">If the custom page hasn't yet been published, go to **Pages**, select the custom page, and then select **Publish**.</span></span>

<span data-ttu-id="bf4e4-147">Kad pielāgotā lapa ir publicēta, tā tiks apkalpota dinamiskās lapas, kam ir parametru saturs, vietā.</span><span class="sxs-lookup"><span data-stu-id="bf4e4-147">After the custom page is published, it will be served instead of the dynamic page that has parameterized content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bf4e4-148">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="bf4e4-148">Additional resources</span></span>

[<span data-ttu-id="bf4e4-149">Esošās vietnes lapas modificēšana</span><span class="sxs-lookup"><span data-stu-id="bf4e4-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="bf4e4-150">Jaunas vietnes lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="bf4e4-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="bf4e4-151">Lapas izkārtojumu atlase</span><span class="sxs-lookup"><span data-stu-id="bf4e4-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="bf4e4-152">SEO metadatu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="bf4e4-152">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="bf4e4-153">Lapas saglabāšana, priekšskatīšana un publicēšana</span><span class="sxs-lookup"><span data-stu-id="bf4e4-153">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="bf4e4-154">Preces lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="bf4e4-154">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="bf4e4-155">Kategorijas ielādes lapas papildināšana</span><span class="sxs-lookup"><span data-stu-id="bf4e4-155">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="bf4e4-156">Lapas satura pieejamības pārbaude</span><span class="sxs-lookup"><span data-stu-id="bf4e4-156">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="bf4e4-157">Tiešsaistes kanāla paplašināmība</span><span class="sxs-lookup"><span data-stu-id="bf4e4-157">Online channel extensibility</span></span>](e-commerce-extensibility/overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
