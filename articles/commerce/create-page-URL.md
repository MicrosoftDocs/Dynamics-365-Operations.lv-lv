---
title: Lapas vietrāža URL izveide
description: Šajā tēmā ir ietvertas pamata koncepcijas un procedūras lapas URL izveidei jūsu vietnē.
author: bicyclingfool
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 98743d8948669f32d3c74e1915c7ed53db81141c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795695"
---
# <a name="create-a-page-url"></a><span data-ttu-id="db551-103">Lapas vietrāža URL izveide</span><span class="sxs-lookup"><span data-stu-id="db551-103">Create a page URL</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="db551-104">Šajā tēmā ir ietvertas pamata koncepcijas un procedūras lapas URL izveidei jūsu vietnē.</span><span class="sxs-lookup"><span data-stu-id="db551-104">This topic covers the basic concepts and procedures for creating a page URL on your site.</span></span>

<span data-ttu-id="db551-105">Pilns vai absolūts vietrādis URL, kas norāda uz jūsu vietnes lapu, sastāv no atšķirīgām daļām.</span><span class="sxs-lookup"><span data-stu-id="db551-105">The full, or absolute, URL that points to a page on your site consists of distinct parts.</span></span> <span data-ttu-id="db551-106">Piemēram, vietrādim URL `https://www.contoso.com/en-us/contactus` ir šādas daļas.</span><span class="sxs-lookup"><span data-stu-id="db551-106">For example, the URL `https://www.contoso.com/en-us/contactus` has the following parts:</span></span>

- <span data-ttu-id="db551-107">`https://www.contoso.com`– HTTP protokols un vietnes domēns.</span><span class="sxs-lookup"><span data-stu-id="db551-107">`https://www.contoso.com` – The HTTP protocol and the site's domain.</span></span>
- <span data-ttu-id="db551-108">`/en-us`– vietnes valodas ceļš.</span><span class="sxs-lookup"><span data-stu-id="db551-108">`/en-us` – The site's language path.</span></span>
- <span data-ttu-id="db551-109">`/contactus`– relatīvais URL lapai **Sazinieties ar mums**.</span><span class="sxs-lookup"><span data-stu-id="db551-109">`/contactus` – The relative URL for the **Contact Us** page.</span></span> <span data-ttu-id="db551-110">Relatīvais URL, ko sauc arī par URL *rindu*.</span><span class="sxs-lookup"><span data-stu-id="db551-110">A relative URL is also known as a URL *slug*.</span></span>

<span data-ttu-id="db551-111">Iestatot vietni, jūs izveidojat savas vietnes domēnu un izvēles valodas ceļu.</span><span class="sxs-lookup"><span data-stu-id="db551-111">You establish your site's domain and optional language path when you set up the site.</span></span> <span data-ttu-id="db551-112">Savai vietnei varat pievienot vairāk domēnu un valodu ceļu, izmantojot tiešsaistes veikalus vietnes iestatījumos.</span><span class="sxs-lookup"><span data-stu-id="db551-112">You can add more domains and language paths to your site through the online stores page in the site's settings.</span></span>

<span data-ttu-id="db551-113">Lapas URL rinda pastāv kā savrupa entītija vietnes autorēšanas vidē.</span><span class="sxs-lookup"><span data-stu-id="db551-113">The URL slug for a page exists as a standalone entity in the site authoring environment.</span></span> <span data-ttu-id="db551-114">Lapas vietrādis URL sastāv no divām daļām: nosaukuma, kas apzīmē URL rindu, un norādes uz lapu vai nu jūsu vietnē, vai ārējā vietnē.</span><span class="sxs-lookup"><span data-stu-id="db551-114">A page URL consists of two parts: a name that represents the URL slug, and a pointer to a page on either your site or an external site.</span></span> <span data-ttu-id="db551-115">Lapas vietrādi URL var arī konfigurēt tā, lai tas darbotos kā novirzīšanas vietrādis uz citu lapu vai nu jūsu vietnē, vai ārējā vietnē.</span><span class="sxs-lookup"><span data-stu-id="db551-115">A page URL can also be configured to act as a redirect to another page on either your site or an external site.</span></span>

## <a name="create-a-page-url"></a><span data-ttu-id="db551-116">Lapas vietrāža URL izveide</span><span class="sxs-lookup"><span data-stu-id="db551-116">Create a page URL</span></span>

<span data-ttu-id="db551-117">Ir divi veidi, kā izveidot lapu vietrāžus URL.</span><span class="sxs-lookup"><span data-stu-id="db551-117">There are two ways to create page URLs:</span></span>

- <span data-ttu-id="db551-118">Automātiski, veidojot lapu</span><span class="sxs-lookup"><span data-stu-id="db551-118">Automatically, when you create a page</span></span>
- <span data-ttu-id="db551-119">Manuāli, no **vietrāžu URL** lapas</span><span class="sxs-lookup"><span data-stu-id="db551-119">Manually, from the **URLs** page</span></span>

### <a name="create-a-page-url-when-you-create-a-page"></a><span data-ttu-id="db551-120">Lapas vietrāža URL izveide, veidojot lapu</span><span class="sxs-lookup"><span data-stu-id="db551-120">Create a page URL when you create a page</span></span>

<span data-ttu-id="db551-121">Veidojot jaunu lapu un **URL** laukā norādot nosaukumu, lapas vietrādis URL, kas norāda uz šo lapu, tiek automātiski izveidots **URL** lapā.</span><span class="sxs-lookup"><span data-stu-id="db551-121">If you provide a name in the **URL** field when you create a new page, a page URL that points to that page is automatically created on the **URLs** page.</span></span> <span data-ttu-id="db551-122">Pēc tam, kad publicējāt vietrādi URL un lapu, uz ko tas norāda, vietnes lietotāji (jūsu klienti) var piekļūt ar vietrādi URL saistītajai lapai.</span><span class="sxs-lookup"><span data-stu-id="db551-122">After you publish the URL and the page that it points to, site users (your customers) can access the page that is associated with the URL.</span></span>

> [!NOTE]
> <span data-ttu-id="db551-123">Ja publicējat vietrādi URL, nepublicējot lapu, uz kuru tas norāda, tad vietnes lietotāji, mēģinot piekļūt lapai, saņem kļūdu 404.</span><span class="sxs-lookup"><span data-stu-id="db551-123">If you publish a URL without publishing the page that it points to, site users receive a 404 error when they try to access the page.</span></span> <span data-ttu-id="db551-124">Ja publicējat lapu, nepublicējot vietrādi URL, kas norāda uz to, lapai nevar piekļūt, izmantojot vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="db551-124">If you publish a page without publishing the URL that points to it, the page can't be accessed by using a URL.</span></span>

### <a name="manually-create-a-page-url"></a><span data-ttu-id="db551-125">Lapas vietrāža URL manuālā izveide</span><span class="sxs-lookup"><span data-stu-id="db551-125">Manually create a page URL</span></span>

<span data-ttu-id="db551-126">Veidojot jaunas lapas, nav nepieciešams norādīt lapas vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="db551-126">When you create new pages, you aren't required to specify a page URL.</span></span> <span data-ttu-id="db551-127">Ja vietrāža URL lauks tiek atstāts tukšs, tad lapa tiek izveidota nesaistītā stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="db551-127">If you leave the URL field blank, the page is created in an unlinked state.</span></span> <span data-ttu-id="db551-128">Šādā gadījumā klienti nevarēs piekļūt lapai, pat ja tā ir publicēta.</span><span class="sxs-lookup"><span data-stu-id="db551-128">In this case, customers won't be able to access the page, even if it's published.</span></span> <span data-ttu-id="db551-129">Lai padarītu lapu pieejamu, ir manuāli jāizveido vietrādis URL un tas ir jāsaista ar lapu.</span><span class="sxs-lookup"><span data-stu-id="db551-129">To make the page accessible, you must manually create the URL and link it to the page.</span></span>

<span data-ttu-id="db551-130">Lai manuāli izveidotu lapas vietrādi URL, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="db551-130">To manually create the page URL for a page, follow these steps.</span></span>

1. <span data-ttu-id="db551-131">Lapā **Vietrāži URL** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="db551-131">On the **URLs** page, select **New**.</span></span>
1. <span data-ttu-id="db551-132">Izvēlieties vietnes lapu, kuru saistīt ar vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="db551-132">Select the site page to associate with the URL.</span></span>
1. <span data-ttu-id="db551-133">Ievadiet URL rindu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="db551-133">Enter the URL slug, and then select **OK**.</span></span>

<span data-ttu-id="db551-134">Šajā brīdī URL ir melnraksta statusā.</span><span class="sxs-lookup"><span data-stu-id="db551-134">At this point, the URL is in a draft state.</span></span> <span data-ttu-id="db551-135">Tas ir jāpublicē, pirms vietnes lietotāji var piekļūt saistītajai lapai.</span><span class="sxs-lookup"><span data-stu-id="db551-135">It must be published before site users can access the associated page.</span></span>

## <a name="update-a-page-url"></a><span data-ttu-id="db551-136">Lapas vietrāža URL atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="db551-136">Update a page URL</span></span>

<span data-ttu-id="db551-137">Lai atjauninātu lapas URL mērķa lapu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="db551-137">To update the target page of a page URL, follow these steps.</span></span>

1. <span data-ttu-id="db551-138">Lapā **Vietrāži URL** atlasiet vietrādi URL atjaunināšanai.</span><span class="sxs-lookup"><span data-stu-id="db551-138">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="db551-139">Rekvizītu rūtī labajā pusē atlasiet daudzpunktes pogu (**...**) blakus mērķa lapas laukam.</span><span class="sxs-lookup"><span data-stu-id="db551-139">In the property pane on the right, select the ellipsis button (**...**) next to the target page field.</span></span>
1. <span data-ttu-id="db551-140">Dialoglodziņā atlasiet citu lapu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="db551-140">In the dialog box, select a different page, and then select **OK**.</span></span>
1. <span data-ttu-id="db551-141">Saglabājiet un publicējiet vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="db551-141">Save and publish the URL.</span></span>

## <a name="redirect-a-page-url"></a><span data-ttu-id="db551-142">Lapas vietrāža URL novirzīšana</span><span class="sxs-lookup"><span data-stu-id="db551-142">Redirect a page URL</span></span>

<span data-ttu-id="db551-143">Dažreiz, iespējams, vēlēsieties, lai klienti redzētu citu lapu, kad viņi pieprasa specifisku vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="db551-143">Sometimes, you might want your customers to view a different page when they request a specific URL.</span></span> <span data-ttu-id="db551-144">Šādos gadījumos bieži vislabākā un vienkāršākā metode ir mainīt lapu, uz kuru norāda lapas vietrādis URL.</span><span class="sxs-lookup"><span data-stu-id="db551-144">In these cases, the best and easiest approach is often to change the page that the page URL points to.</span></span> <span data-ttu-id="db551-145">Tomēr jums, iespējams, ir likumīgi iemesli izmantot HTTP 301 vai 3023 pārvirzīšanu, lai novirzītu pieprasījumus uz citu vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="db551-145">However, you might have legitimate reasons for using HTTP 301 or 3023 redirects to redirect requests for a URL to a different URL.</span></span>

<span data-ttu-id="db551-146">Lai novirzītu vietrādi URL uz citu vietrādi URL, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="db551-146">To redirect a URL to a different URL, follow these steps.</span></span>

1. <span data-ttu-id="db551-147">Lapā **Vietrāži URL** atlasiet vietrādi URL atjaunināšanai.</span><span class="sxs-lookup"><span data-stu-id="db551-147">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="db551-148">Rekvizītu rūts labajā pusē atlasiet rekvizītu **Novirzīšana**.</span><span class="sxs-lookup"><span data-stu-id="db551-148">In the property pane on the right, select **Redirect**.</span></span>
1. <span data-ttu-id="db551-149">Novirzīšanai atlasiet galamērķi.</span><span class="sxs-lookup"><span data-stu-id="db551-149">Select a destination for the redirect:</span></span>

    - <span data-ttu-id="db551-150">Lai norādītu uz citu jūsu vietnes lapu, atlasiet **Iekšējais vietrādis URL**, atlasiet daudzpunktes pogu **(...**) un pēc tam atlasiet vietrādi URL, uz kuru veikt novirzīšanu.</span><span class="sxs-lookup"><span data-stu-id="db551-150">To point to another page on your site, select **Internal URL**, select the ellipsis button (**...**), and then select the URL to redirect to.</span></span>
    - <span data-ttu-id="db551-151">Lai norādītu uz lapu ārējā vietnē, atlasiet **Ārējais vietrādis URL** un pēc tam ievadiet pilnu vietrādi URL šai lapai.</span><span class="sxs-lookup"><span data-stu-id="db551-151">To point to a page on an external site, select **External URL**, and then enter the full URL for that page.</span></span> <span data-ttu-id="db551-152">Noteikti iekļaujiet protokolu.</span><span class="sxs-lookup"><span data-stu-id="db551-152">Be sure to include the protocol.</span></span> <span data-ttu-id="db551-153">Piemēram, ievadiet `https://domain.com/new/page`.</span><span class="sxs-lookup"><span data-stu-id="db551-153">For example, enter `https://domain.com/new/page`.</span></span> <span data-ttu-id="db551-154">Ja vietrādis URL jau novirza uz iekšējo vietrādi URL, jums ir jāatlasa **Noņemt atlasi** pirms varat ieiet ārējā vietrādī URL.</span><span class="sxs-lookup"><span data-stu-id="db551-154">If the URL already redirects to an internal URL, you must select **Clear selection** before you can enter an external URL.</span></span>

1. <span data-ttu-id="db551-155">Novirzīšanas tipa izvēle.</span><span class="sxs-lookup"><span data-stu-id="db551-155">Select a redirect type:</span></span>

    - <span data-ttu-id="db551-156">**Pastāvīga novirzīšana** (301) — atlasiet šo opciju, ja zināt, ka saturs tiek pārvietots uz visiem laikiem, un tas netiks atgriezts tā iepriekšējā vietrādī URL.</span><span class="sxs-lookup"><span data-stu-id="db551-156">**Permanent redirect (301)** – Select this option when you know that your content is moving permanently and won't revert to its previous URL.</span></span> <span data-ttu-id="db551-157">Meklētājprogrammas piešķirs novirzošā vietrāža URL meklētājprogrammas optimizācijas (SEO) vērtību vietrādim, uz kuru notiek novirzīšana, un atjauninās savu ierakstu, lai parādītu jauno vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="db551-157">Search engines will assign the search engine optimization (SEO) value of the redirecting URL to the URL that is being redirected to and update their record to show the new URL.</span></span> 
    - <span data-ttu-id="db551-158">**Pagaidu novirzīšana (302)** — atlasiet šo opciju, lai novirzītu datplūsmu, neatjauninot meklētājprogrammas.</span><span class="sxs-lookup"><span data-stu-id="db551-158">**Temporary redirect (302)** – Select this option to redirect traffic without updating search engines.</span></span> <span data-ttu-id="db551-159">Šo pieeju parasti izmanto, ja saturs drīz atgriezīsies uz iepriekšējo vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="db551-159">This approach is typically used if the content will soon revert to its previous URL.</span></span>

1. <span data-ttu-id="db551-160">Kad esat gatavs ieviest novirzīšanu, saglabājiet un publicējiet vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="db551-160">When you're ready to implement the redirect, save and publish the URL.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db551-161">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="db551-161">Additional resources</span></span>

[<span data-ttu-id="db551-162">Vietnes navigācijas pielāgošana</span><span class="sxs-lookup"><span data-stu-id="db551-162">Customize site navigation</span></span>](customize-site-navigation.md)

[<span data-ttu-id="db551-163">Jaunas vietnes lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="db551-163">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="db551-164">Domēna nosaukuma konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="db551-164">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="db551-165">Valodu pievienošana vietnei</span><span class="sxs-lookup"><span data-stu-id="db551-165">Add languages to your site</span></span>](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
