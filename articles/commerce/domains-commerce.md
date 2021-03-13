---
title: Domēni programmā Dynamics 365 Commerce
description: Šajā tēmā aprakstīts, kā domēni tiek apstrādāti programmā Microsoft Dynamics 365 Commerce.
author: BrShoo
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: BrShoo
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: d855f2164e4ee0f0cdb220787eb96217523137e3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010251"
---
# <a name="domains-in-dynamics-365-commerce"></a><span data-ttu-id="e72de-103">Domēni programmā Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e72de-103">Domains in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e72de-104">Šajā tēmā aprakstīts, kā domēni tiek apstrādāti programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e72de-104">This topic describes how domains are handled in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e72de-105">Domēni ir tīmekļa adreses, ko izmanto, lai naviģētu uz Dynamics 365 Commerce vietnēm tīmekļa pārlūkā.</span><span class="sxs-lookup"><span data-stu-id="e72de-105">Domains are web addresses used to navigate to Dynamics 365 Commerce sites in a web browser.</span></span> <span data-ttu-id="e72de-106">Jūs kontrolējat sava domēna pārvaldību ar izvēlēto domēna nosaukuma servera (Domain Name Server - DNS) nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="e72de-106">You control management of your domain with a chosen Domain Name Server (DNS) provider.</span></span> <span data-ttu-id="e72de-107">Domēniem ir atsauces visā Dynamics 365 Commerce vietnes veidotājā, lai koordinētu, kā vietnei varēs piekļūt pēc publicēšanas.</span><span class="sxs-lookup"><span data-stu-id="e72de-107">Domains are referenced throughout Dynamics 365 Commerce site builder to coordinate how a site will be accessed when published.</span></span> <span data-ttu-id="e72de-108">Šajā tēmā ir aplūkots, kā tiek apstrādāti domēni un kā uz tiem tiek sniegtas atsauces visā Commerce vietnes izstrādes un palaišanas cikla laikā.</span><span class="sxs-lookup"><span data-stu-id="e72de-108">This topic reviews how domains are handled and referenced throughout the lifecycle of the Commerce site development and launch.</span></span>

## <a name="provisioning-and-supported-host-names"></a><span data-ttu-id="e72de-109">Nodrošināšana un atbalstītie resursdatoru nosaukumi</span><span class="sxs-lookup"><span data-stu-id="e72de-109">Provisioning and supported host names</span></span>

<span data-ttu-id="e72de-110">Nodrošinot e-komercijas vidi [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), tiek izmantots lodziņš **Atbalstītie resursdatora nosaukumi** e-komercijas nodrošināšanas ekrānā, lai ievadītu domēnus, kas tiks saistīti ar izvietoto Commerce vidi.</span><span class="sxs-lookup"><span data-stu-id="e72de-110">When provisioning an e-commerce environment in [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), the **Supported host names** box on the e-commerce provisioning screen is used to enter domains that will be associated with the deployed Commerce environment.</span></span> <span data-ttu-id="e72de-111">Šie domēni būs uz klientu vērsti domēna nosaukuma servera (DNS) nosaukumi, kuros tiks viesotas e-komercijas vietnes.</span><span class="sxs-lookup"><span data-stu-id="e72de-111">These domains will be the customer-facing Domain Name Server (DNS) names where e-commerce websites will be hosted.</span></span> <span data-ttu-id="e72de-112">Ievadot domēnu šajā posmā, netiek sākta domēna trafika pāradresācija uz Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e72de-112">Entering a domain at this stage does not start diverting traffic for the domain to Dynamics 365 Commerce.</span></span> <span data-ttu-id="e72de-113">Trafiks domēnam tiks maršrutēts uz Commerce galapunktu, kad DNS CNAME ieraksts tiek atjaunināts, lai izmantotu Commerce galapunktu ar šo domēnu.</span><span class="sxs-lookup"><span data-stu-id="e72de-113">Traffic for a domain will only be routed to the Commerce endpoint when the DNS CNAME record is updated to use the Commerce endpoint with the domain.</span></span>

> [!NOTE]
> <span data-ttu-id="e72de-114">Vairākus domēnus var ievadīt lodziņā **Atbalstītie resursdatora nosaukumi** , atdalot tos ar semikolu.</span><span class="sxs-lookup"><span data-stu-id="e72de-114">Multiple domains can be entered into the **Supported host names** box by separating them with semi-colons.</span></span>

<span data-ttu-id="e72de-115">Sekojošajā attēlā redzams LCS e-komercijas nodrošināšanas ekrāns ar iezīmētu lodziņu **Atbalstītie resursdatora nosaukumi**.</span><span class="sxs-lookup"><span data-stu-id="e72de-115">The following illustration shows the LCS e-commerce provisioning screen with the **Supported host names** box highlighted.</span></span> 

![LCS e-komercijas nodrošināšanas ekrāns ar izceltu lodziņu **Atbalstītie resursdatora nosaukumi**](./media/Domains_ProvisioningeCommerceScreen.png)

<span data-ttu-id="e72de-117">Varat izveidot pakalpojuma pieprasījumu, lai videi pievienotu papildu domēnus, ja nodrošināšana jau ir notikusi.</span><span class="sxs-lookup"><span data-stu-id="e72de-117">You can create a service request to add additional domains to an environment if provisioning has already occurred.</span></span> <span data-ttu-id="e72de-118">Lai izveidotu pakalpojuma pieprasījumu LCS, jūsu vidē atveriet **Atbalsts \> Atbalsta jautājumi** un atlasiet **Iesniegt incidentu**.</span><span class="sxs-lookup"><span data-stu-id="e72de-118">To create a service request in LCS, within your environment go to **Support \> Support issues** and select **Submit an incident**.</span></span>

## <a name="commerce-generated-urls"></a><span data-ttu-id="e72de-119">Commerce ģenerētie vietrāži URL</span><span class="sxs-lookup"><span data-stu-id="e72de-119">Commerce-generated URLs</span></span>

<span data-ttu-id="e72de-120">Kad tiek nodrošināta Dynamics 365 Commerce e-komercijas vide, Commerce ģenerēs vietrādi URL, kas būs vides darba adrese.</span><span class="sxs-lookup"><span data-stu-id="e72de-120">When provisioning a Dynamics 365 Commerce e-commerce environment, Commerce will generate a URL that will be the working address for the environment.</span></span> <span data-ttu-id="e72de-121">Šim vietrādim URL ir atsauce uz e-komercijas vietnes saiti, kas norādīta LCS pēc vides nodrošināšanas.</span><span class="sxs-lookup"><span data-stu-id="e72de-121">This URL is referenced in the e-commerce site link shown in LCS after the environment is provisioned.</span></span> <span data-ttu-id="e72de-122">Commerce ģenerētie vietrāži URL ir `https://<e-commerce tenant name>.commerce.dynamics.com`formātā , kur e-komercijas nomnieka nosaukums ir nosaukums, kas ievadīts LCS Commerce videi.</span><span class="sxs-lookup"><span data-stu-id="e72de-122">A Commerce-generated URL is in the format `https://<e-commerce tenant name>.commerce.dynamics.com`, where the e-commerce tenant name is the name entered in LCS for the Commerce environment.</span></span>

<span data-ttu-id="e72de-123">Ražošanas vietnes resursdatoru nosaukumus var izmantot arī smilškastes vidē.</span><span class="sxs-lookup"><span data-stu-id="e72de-123">You can use production site host names in a sandbox environment as well.</span></span> <span data-ttu-id="e72de-124">Šī opcija ir ideāli piemērota, ja kopēsit vietni no smilškastes vides uz ražošanu.</span><span class="sxs-lookup"><span data-stu-id="e72de-124">This option is ideal when you will be copying a site from a sandbox environment to production.</span></span>

## <a name="site-setup"></a><span data-ttu-id="e72de-125">Vietnes iestatījumi</span><span class="sxs-lookup"><span data-stu-id="e72de-125">Site setup</span></span>

<span data-ttu-id="e72de-126">Pēc e-komercijas vides nodrošināšanas ir jāiestata vietnes Commerce vietņu veidotājā, lai saistītu savu vietni ar darba URL.</span><span class="sxs-lookup"><span data-stu-id="e72de-126">After your e-commerce environment is provisioned, you must set up your site in Commerce site builder to associate your site to the working URL.</span></span>

<span data-ttu-id="e72de-127">Pirmoreiz iestatot vietni vietnes veidotājā, tiks atvērts dialoglodziņš **Vietnes iestatīšana** .</span><span class="sxs-lookup"><span data-stu-id="e72de-127">When you first set up a site in site builder, the **Setup your Site** dialog box will appear.</span></span>

<span data-ttu-id="e72de-128">Sekojošajā attēlā ir parādīts dialoglodziņš **Vietnes iestatīšana** vietnei ar nosaukumu "noklusējums", kad piekļūstat vietnei pirmo reizi vietnes veidotājā.</span><span class="sxs-lookup"><span data-stu-id="e72de-128">The following illustration shows the **Setup your Site** dialog box for a site named "default" when you access the site for the first time in site builder.</span></span>

![Dialoglodziņš **Vietnes iestatīšana**](./media/Domains_SetupyoursiteScreen.png)

<span data-ttu-id="e72de-130">Lodziņš **Atlasīt domēnu** ļauj saistīt vienu no atbalstītajiem resursdatora nosaukumiem, kas tiek nodrošināti jūsu vietnei LCS, jūsu vietnei vietnes veidotājā.</span><span class="sxs-lookup"><span data-stu-id="e72de-130">The **Select a domain** box allows you to associate one of the supported host names provided for your site in LCS to your site in site builder.</span></span>

<span data-ttu-id="e72de-131">Lodziņu **Ceļš** var atstāt tukšu, vai var pievienot papildu ceļu virkni, kas tiks parādīta darba vietrādī URL.</span><span class="sxs-lookup"><span data-stu-id="e72de-131">The **Path** box can be left blank, or an additional path string can be added that will be reflected in your working URL.</span></span> <span data-ttu-id="e72de-132">Atstājot lodziņu **Ceļš** tukšu, pamata Commerce ģenerēts vietrādis URL tiek saistīts ar vietni, kas tiek iestatīta vietnes veidotājā.</span><span class="sxs-lookup"><span data-stu-id="e72de-132">Leaving the **Path** box blank associates the base Commerce-generated URL with the site being set up in site builder.</span></span> <span data-ttu-id="e72de-133">Ceļiem ir jābūt unikāliem katram vietņu/domēnu pārim.</span><span class="sxs-lookup"><span data-stu-id="e72de-133">Paths must be unique for each site/domain pair.</span></span> <span data-ttu-id="e72de-134">Izvēlētās vietnes un domēna ietvaros tikai viena vietne vidē var izmantot tukšu ceļu vai būt saistītai ar unikālu ceļu virkni.</span><span class="sxs-lookup"><span data-stu-id="e72de-134">Within the site and domain selected, only one site in the environment can use the blank path or be associated with a unique path string.</span></span> <span data-ttu-id="e72de-135">Jebkura virkne, kas pievienota laukam **Ceļš** vietnes iestatīšanas laikā, kļūs par pamata Commerce ģenerēta vietrāža URL apakšceļu, kas tiek izmantots, lai piekļūtu vietnei tīmekļa pārlūkprogrammā.</span><span class="sxs-lookup"><span data-stu-id="e72de-135">Any string added to the **Path** field during site setup will become a subpath of the base Commerce-generated URL used to access the site in a web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="e72de-136">Ceļš tiek saukts arī par **Atbilstības ceļš**, kad tiek pievienots kanāls vietnes veidotāja konfigurācijas sadaļā **Vietnes iestatījumi \> Kanāli** .</span><span class="sxs-lookup"><span data-stu-id="e72de-136">The path is also known as the **Match path** when adding a channel in the **Site Settings \> Channels** configuration section of site builder.</span></span>

<span data-ttu-id="e72de-137">Piemēram, ja vietnes veidotājā ir vietne, kas saukta "fabrikam", kas atrodas e-komercijas nomniekā ar nosaukumu "xyz", un, ja iestatāt vietni ar tukšu ceļu, piekļūsiet publicētajam vietnes saturam tīmekļa pārlūkā, dodoties tieši uz pamata Commerce ģenerēto vietrādi URL:</span><span class="sxs-lookup"><span data-stu-id="e72de-137">For example, if you have a site in site builder called "fabrikam" in an e-commerce tenant named "xyz," and if you set up the site with a blank path, then you would access the published site content in a web browser by going directly to the base Commerce-generated URL:</span></span>

`https://xyz.commerce.dynamics.com`

<span data-ttu-id="e72de-138">Pārmaiņus, ja šīs vietnes uzstādīšanas laikā esat pievienojis ceļu “fabrikam”, publicētajam vietnes saturam var piekļūt tīmekļa pārlūkprogrammā, izmantojot šādu vietrādi URL:</span><span class="sxs-lookup"><span data-stu-id="e72de-138">Alternately, if you had added a path of "fabrikam" during this same site's setup, you would access the published site content in a web browser using the following URL:</span></span>

`https://xyz.commerce.dynamics.com/fabrikam`

## <a name="pages-and-urls"></a><span data-ttu-id="e72de-139">Lapas un vietrāži URL</span><span class="sxs-lookup"><span data-stu-id="e72de-139">Pages and URLs</span></span>

<span data-ttu-id="e72de-140">Pēc tam, kad jūsu vietne ir iestatīta ar ceļu, visi vietrāži URL, kas saistīti ar lapām vietnes veidotājā, vietnei tiks balstīti uz darba vietrādi URL (Commerce ģenerēto vietrādi URL vai Commerce ģenerēto vietrādi URL un ceļu).</span><span class="sxs-lookup"><span data-stu-id="e72de-140">After your site is set up with a path, all URLs associated with pages in site builder will build on the working URL (the Commerce-generated URL, or the Commerce-generated URL plus the path) for the site.</span></span> <span data-ttu-id="e72de-141">Jauna vietrāža URL izveide vietnes veidotājā (**URL /> +Jauns**), atlasot lapu no saraksta, dialoglodziņā **Jauns vietrādis URL** un ievadot URL ceļu šai lapai, šis vietrādis URL tiks saistīts ar atlasīto lapu.</span><span class="sxs-lookup"><span data-stu-id="e72de-141">Creating a new URL in site builder (**URLS /> +New**) by selecting a page from the list in the **New URL** dialog box and entering the URL path for that page will associate that URL with the selected page.</span></span> <span data-ttu-id="e72de-142">URL ceļa vērtība pēc tam, lai piekļūtu lapai, tiek pievienota vietnes darba vietrādim URL un ir apzīmēta kā `./<URL path>` URL sarakstā lapā **Vietrāži URL** vietnes veidotājā.</span><span class="sxs-lookup"><span data-stu-id="e72de-142">The URL path value then appends to the site's working URL to access the page, and is labeled as `./<URL path>` in the URL list of the **URLs** page in site builder.</span></span>

<span data-ttu-id="e72de-143">Sekojošajā attēlā redzams dialoglodziņš **Jauns vietrādis URL** vietnes veidotājā ar URL ceļa piemēru.</span><span class="sxs-lookup"><span data-stu-id="e72de-143">The following illustration shows the **New URL** dialog box in site builder with an example URL path highlighted.</span></span> 

![Dialoglodziņš **Jauns vietrādis URL** vietnes veidotājā](./media/Domains_PageSetup2a.png)

<span data-ttu-id="e72de-145">Sekojošajā attēlā redzama lapa **Vietrāži URL** vietnes veidotājā ar URL piemēru, kas ir izcelts sarakstā.</span><span class="sxs-lookup"><span data-stu-id="e72de-145">The following illustration shows the **URLs** page in site builder with an example URL highlighted in the list.</span></span>

![Izpildīt lietotāja plūsmas opciju politikas plūsmā](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a><span data-ttu-id="e72de-147">Domēni vietnes veidotājā</span><span class="sxs-lookup"><span data-stu-id="e72de-147">Domains in site builder</span></span>

<span data-ttu-id="e72de-148">Atbalstīto resursdatoru nosaukumu vērtības ir pieejamas, lai, iestatot vietni, tās būtu saistītas kā domēns.</span><span class="sxs-lookup"><span data-stu-id="e72de-148">The supported host names values are available to be associated as a domain when setting up a site.</span></span> <span data-ttu-id="e72de-149">Atlasot atbalstītā resursdatora nosaukuma vērtību kā domēnu, tiks parādīts izvēlētais domēns, uz kuru ir atsauce vietņu veidotājā.</span><span class="sxs-lookup"><span data-stu-id="e72de-149">When selecting a supported host name value as the domain, you will see the chosen domain referenced throughout site builder.</span></span> <span data-ttu-id="e72de-150">Šis domēns ir tikai atsauce Commerce vidē, dzīvā datplūsma šim domēnam vēl netiks pārsūtīta uz Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e72de-150">This domain is only a reference within the Commerce environment, live traffic for that domain will not yet be forwarded to Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e72de-151">Ja strādājat ar vietnēm vietnes veidotājā, ja jums ir divas vietnes, kas iestatītas ar diviem dažādiem domēniem, varat pievienot atribūtu **?domēns=** jūsu darba vietrādim URL, lai piekļūtu publicētajai vietnes informācijai pārlūkprogrammā.</span><span class="sxs-lookup"><span data-stu-id="e72de-151">When working with sites in site builder, if you have two sites set up with two different domains, you can append the **?domain=** attribute to your working URL to access the published site content in a browser.</span></span>

<span data-ttu-id="e72de-152">Piemēram, vide "xyz" ir nodrošināta, un divas vietnes ir izveidotas un saistītas ar vietnes veidotāju: viens ar domēnu `www.fabrikam.com` un otrs ar domēnu `www.constoso.com`.</span><span class="sxs-lookup"><span data-stu-id="e72de-152">For example, environment "xyz" has been provisioned, and two sites have been created and associated in site builder: one with the domain `www.fabrikam.com` and the other with the domain `www.constoso.com`.</span></span> <span data-ttu-id="e72de-153">Katra vietne tika iestatīta, izmantojot tukšu ceļu.</span><span class="sxs-lookup"><span data-stu-id="e72de-153">Each site was set up using a blank path.</span></span> <span data-ttu-id="e72de-154">Šīm divām vietnem pēc tam var piekļūt tīmekļa pārlūkprogrammā, lietojot atribūtu **?domēns=** :</span><span class="sxs-lookup"><span data-stu-id="e72de-154">These two sites could then be accessed in a web browser as follows using the **?domain=** attribute:</span></span>
- `https://xyz.commerce.dynamics.com?domain=www.fabrikam.com`
- `https://xyz.commerce.dynamics.com?domain=www.contoso.com`

<span data-ttu-id="e72de-155">Ja domēna vaicājuma virkne netiek norādīta vidē ar vairākiem domēniem, Commerce izmanto pirmo norādīto domēnu.</span><span class="sxs-lookup"><span data-stu-id="e72de-155">When a domain query string is not given in an environment with multiple domains provided, Commerce uses the first domain you provided.</span></span> <span data-ttu-id="e72de-156">Piemēram, ja ceļš "fabrikam" vietas iestatīšanas laikā tika nodrošināts pirmais, vietrādi URL `https://xyz.commerce.dynamics.com` var izmantot, lai piekļūtu publicētajai vietnes satura vietnei `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="e72de-156">For example, if the path "fabrikam" was provided first during site setup, the URL `https://xyz.commerce.dynamics.com` could be used to access the published site content site for `www.fabrikam.com`.</span></span>

## <a name="traffic-forwarding-in-production"></a><span data-ttu-id="e72de-157">Satiksmes pārsūtīšana ražošanā</span><span class="sxs-lookup"><span data-stu-id="e72de-157">Traffic forwarding in production</span></span>

<span data-ttu-id="e72de-158">Varat simulēt vairākus domēnus, izmantojot domēna vaicājuma virknes parametrus pašā commerce.dynamics.com galapunktā.</span><span class="sxs-lookup"><span data-stu-id="e72de-158">You can simulate multiple domains using domain query string parameters on the commerce.dynamics.com endpoint itself.</span></span> <span data-ttu-id="e72de-159">Bet, ja jums ir jābūt tiešraidē ražošanā, jums ir jānosūta trafiks jūsu pielāgotajam domēnam uz `<e-commerce tenant name>.commerce.dynamics.com` galapunktu.</span><span class="sxs-lookup"><span data-stu-id="e72de-159">But when you need to go live in production, you must forward the traffic for your custom domain to the `<e-commerce tenant name>.commerce.dynamics.com` endpoint.</span></span>

<span data-ttu-id="e72de-160">Galapunkts `<e-commerce tenant name>.commerce.dynamics.com` neatbalsta pielāgotus domēna drošligzdu slāņus (Secure Sockets Layers - SSLs), tāpēc ir jāiestata pielāgoti domēni, izmantojot front door pakalpojumu vai satura piegādes tīklu (content delivery network - CDN).</span><span class="sxs-lookup"><span data-stu-id="e72de-160">The `<e-commerce tenant name>.commerce.dynamics.com` endpoint does not support custom domain Secure Sockets Layers (SSLs), so you must set up custom domains using a front door service or content delivery network (CDN).</span></span> 

<span data-ttu-id="e72de-161">Lai iestatītu pielāgotus domēnus, izmantojot front door pakalpojumu vai CDN, ir divas opcijas:</span><span class="sxs-lookup"><span data-stu-id="e72de-161">To set up custom domains using a front door service or CDN, you have two options:</span></span>

- <span data-ttu-id="e72de-162">Iestatiet front door pakalpojumu, piemēram, Azure Front Door, lai apstrādātu priekšgala trafiku un pievienotos jūsu Commerce videi.</span><span class="sxs-lookup"><span data-stu-id="e72de-162">Set up a front door service like Azure Front Door to handle front-end traffic and connect to your Commerce environment.</span></span> <span data-ttu-id="e72de-163">Tas nodrošina lielāku kontroli pār domēnu un sertifikātu pārvaldību, kā arī detalizētākas drošības politikas.</span><span class="sxs-lookup"><span data-stu-id="e72de-163">This provides greater control over domain and certificate management and more granular security policies.</span></span>
- <span data-ttu-id="e72de-164">Izmantot Commerce nodrošināto Azure Front Door instanci.</span><span class="sxs-lookup"><span data-stu-id="e72de-164">Use the Commerce-supplied Azure Front Door instance.</span></span> <span data-ttu-id="e72de-165">Tas prasa koordinēt darbību ar Dynamics 365 Commerce grupu domēna verifikācijai un iegūt SSL sertifikātus jūsu ražošanas domēnam.</span><span class="sxs-lookup"><span data-stu-id="e72de-165">This requires coordinating action with the Dynamics 365 Commerce team for domain verification and obtaining SSL certificates for your production domain.</span></span>

<span data-ttu-id="e72de-166">Informāciju par to, kā tieši iestatīt CDN pakalpojumu, skatiet [Pievienot atbalstu satura piegādes tīklam (CDN)](add-cdn-support.md).</span><span class="sxs-lookup"><span data-stu-id="e72de-166">For information about how to set up a CDN service directly, see [Add support for a content delivery network (CDN)](add-cdn-support.md).</span></span>

<span data-ttu-id="e72de-167">Lai izmantotu Commerce nodrošināto Azure Front Door instanci, jums ir jāizveido pakalpojuma pieprasījums pēc palīdzības CDN iestatīšanā no Commerce ievadapmācības grupas.</span><span class="sxs-lookup"><span data-stu-id="e72de-167">To use the Commerce-supplied Azure Front Door instance, you must create a service request for CDN setup assistance from the Commerce onboarding team.</span></span> 

- <span data-ttu-id="e72de-168">Jums būs jānorāda uzņēmuma nosaukums, ražošanas domēns, vides ID un ražošanas e-komercijas nomnieka nosaukums.</span><span class="sxs-lookup"><span data-stu-id="e72de-168">You will need to provide your company name, the production domain, environment ID, and production e-commerce tenant name.</span></span> 
- <span data-ttu-id="e72de-169">Jums būs jāapstiprina, ja šis ir esošs domēns (tiek izmantots pašreiz aktīvajai vietnei) vai jauns domēns.</span><span class="sxs-lookup"><span data-stu-id="e72de-169">You will need to confirm if this is an existing domain (used for a currently active site) or a new domain.</span></span> 
- <span data-ttu-id="e72de-170">Jaunam domēnam domēna verifikāciju un SSL sertifikātu var iegūt vienā solī.</span><span class="sxs-lookup"><span data-stu-id="e72de-170">For a new domain, the domain verification and SSL certificate can be achieved in a single step.</span></span> 
- <span data-ttu-id="e72de-171">Domēnam, kas apkalpo esošu vietni, ir jāveic daudzpakāpju process, lai izveidotu domēna verifikāciju un SSL sertifikātu.</span><span class="sxs-lookup"><span data-stu-id="e72de-171">For a domain serving an existing website, there is a multistep process required to establish the domain verification and SSL certificate.</span></span> <span data-ttu-id="e72de-172">Šim procesam ir 7 darba dienu pakalpojuma līmeņa vienošanās (service level agreement - SLA) domēnam, lai nokļūtu tiešraidē, jo tas ietver vairākus secīgus soļus.</span><span class="sxs-lookup"><span data-stu-id="e72de-172">This process has a 7-working-day service level agreement (SLA) for a domain to go live, because it includes multiple sequential steps.</span></span>

<span data-ttu-id="e72de-173">Lai izveidotu pakalpojuma pieprasījumu LCS, jūsu vidē atveriet **Atbalsts \> Atbalsta jautājumi** un atlasiet **Iesniegt incidentu**.</span><span class="sxs-lookup"><span data-stu-id="e72de-173">To create a service request in LCS, within your environment go to **Support \> Support issues** and select **Submit an incident**.</span></span>

> [!NOTE]
> <span data-ttu-id="e72de-174">Pielāgoti domēni ar SSL tiek atbalstīti tikai ražošanas vidēs.</span><span class="sxs-lookup"><span data-stu-id="e72de-174">Custom domains with SSL are only supported on production environments.</span></span> <span data-ttu-id="e72de-175">Neražošanas vidēm, piemēram, smilškastes un lietotāja akceptēšanas pārbaudes (user acceptance testing - UAT) vidēm, izmantojiet Commerce ģenerēto vietrādi URL, lai piekļūtu publicētajam saturam tīmekļa pārlūkprogrammā.</span><span class="sxs-lookup"><span data-stu-id="e72de-175">For non-production environments such as sandbox and user acceptance testing (UAT), use the Commerce-generated URL to access published content in a web browser.</span></span>

## <a name="ssl-certificate-process"></a><span data-ttu-id="e72de-176">SSL sertifikāta process</span><span class="sxs-lookup"><span data-stu-id="e72de-176">SSL certificate process</span></span>

<span data-ttu-id="e72de-177">Kad pakalpojuma pieprasījums ir iesniegts, Commerce grupa ar jums koordinēs tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="e72de-177">When a service request is filed, the Commerce team will coordinate the following steps with you.</span></span>

<span data-ttu-id="e72de-178">Jauniem domēniem:</span><span class="sxs-lookup"><span data-stu-id="e72de-178">For new domains:</span></span>
- <span data-ttu-id="e72de-179">Commerce grupa iestatīs Azure Front Door instanci (Commerce viesota).</span><span class="sxs-lookup"><span data-stu-id="e72de-179">The Commerce team will set up the Azure Front Door instance (Commerce-hosted).</span></span>
- <span data-ttu-id="e72de-180">Pēc tam Commerce grupa nodrošinās CNAME ierakstu, lai norādītu jūsu pielāgoto domēnu.</span><span class="sxs-lookup"><span data-stu-id="e72de-180">The Commerce team will then provide the CNAME record to point your custom domain.</span></span>
- <span data-ttu-id="e72de-181">Pēc CNAME ieraksta atjaunināšanas Commerce viesota Azure Front Door instance varēs pārbaudīt domēna īpašumtiesības un iegūt SSL sertifikātu.</span><span class="sxs-lookup"><span data-stu-id="e72de-181">After the CNAME record is updated, the Commerce-hosted Azure Front Door instance will be able to verify the domain ownership and get the SSL certificate.</span></span>

<span data-ttu-id="e72de-182">Esošajiem/aktīvajiem domēniem:</span><span class="sxs-lookup"><span data-stu-id="e72de-182">For existing/active domains:</span></span>
- <span data-ttu-id="e72de-183">Commerce grupa dos norādījumus pievienot `afdverify.<custom-domain>` CNAME ierakstu, lai to sniegtu jūsu domēna DNS nodrošinātājam.</span><span class="sxs-lookup"><span data-stu-id="e72de-183">The Commerce team will instruct you to add an `afdverify.<custom-domain>` CNAME record to provide to your domain DNS provider.</span></span>
- <span data-ttu-id="e72de-184">Pēc pabeigšanas, Commerce grupa pievienos domēnu Azure Front Door instancei un nodrošinās papildu DNS TXT ierakstus, kas jāpievieno domēna DNS.</span><span class="sxs-lookup"><span data-stu-id="e72de-184">When complete, the Commerce team will add the domain to the Azure Front Door instance and provide additional DNS TXT records to be added to the DNS for the domain.</span></span>
- <span data-ttu-id="e72de-185">Kad TXT ieraksti ir pabeigti, Commerce grupa pabeigs Azure Front Door atjauninājumus domēnam, kas iestatīs SSL sertifikātu.</span><span class="sxs-lookup"><span data-stu-id="e72de-185">After the TXT records are completed, the Commerce team will complete the Azure Front Door updates for the domain that will set up the SSL certificate.</span></span>

## <a name="apex-domains"></a><span data-ttu-id="e72de-186">Apeksa domēni</span><span class="sxs-lookup"><span data-stu-id="e72de-186">Apex domains</span></span>

<span data-ttu-id="e72de-187">Commerce nodrošinātā Azure Front Door instance neatbalsta apeksa domēnus (saknes domēnus, kas nesatur apakšdomēnus).</span><span class="sxs-lookup"><span data-stu-id="e72de-187">The Commerce-supplied Azure Front Door instance does not support apex domains (root domains that do not contain subdomains).</span></span> <span data-ttu-id="e72de-188">Lai atrisinātu apeksa domēnus, ir nepieciešama IP adrese, un Commerce Azure Front Door instance pastāv tikai ar virtuāliem galapunktiem.</span><span class="sxs-lookup"><span data-stu-id="e72de-188">Apex domains require an IP address to resolve, and the Commerce Azure Front Door instance exists with virtual endpoints only.</span></span> <span data-ttu-id="e72de-189">Lai izmantotu apeksa domēnu, ir divas opcijas:</span><span class="sxs-lookup"><span data-stu-id="e72de-189">To use an apex domain, you have two options:</span></span>

- <span data-ttu-id="e72de-190">**1. opcija** - Izmantojiet DNS nodrošinātāju, lai novirzītu apeksa domēnu uz "www" domēnu.</span><span class="sxs-lookup"><span data-stu-id="e72de-190">**Option 1** - Use your DNS provider to redirect the apex domain to a "www" domain.</span></span> <span data-ttu-id="e72de-191">Piemēram, fabrikam.com pārvirza uz `www.fabrikam.com` , kur `www.fabrikam.com` ir CNAME ieraksts, kas norāda uz Commerce viesotu Azure Front Door instanci.</span><span class="sxs-lookup"><span data-stu-id="e72de-191">For example, fabrikam.com redirects to `www.fabrikam.com` where `www.fabrikam.com` is the CNAME record that points to the Commerce-hosted Azure Front Door instance.</span></span>

- <span data-ttu-id="e72de-192">**2. opcija** - Iestatiet CDN/front door instanci uz savu instanci, lai viesotu apeksa domēnu.</span><span class="sxs-lookup"><span data-stu-id="e72de-192">**Option 2** - Set up a CDN/front door instance on your own to host the apex domain.</span></span>

> [!NOTE]
> <span data-ttu-id="e72de-193">Ja izmantojat Azure Front Door, jums ir arī jāiestata Azure DNS tajā pašā abonementā.</span><span class="sxs-lookup"><span data-stu-id="e72de-193">If you are using Azure Front Door, you must also set up an Azure DNS in the same subscription.</span></span> <span data-ttu-id="e72de-194">Apeksa domēns, kas viesots Azure DNS, var norādīt uz jūsu Azure Front Door kā uz aizstājvārda ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e72de-194">The apex domain hosted on Azure DNS can point to your Azure Front Door as an alias record.</span></span> <span data-ttu-id="e72de-195">Šis ir vienīgais risinājums, tā kā apeksa domēniem vienmēr ir jānorāda IP adrese.</span><span class="sxs-lookup"><span data-stu-id="e72de-195">This is the only work around, as apex domains must always point to an IP address.</span></span>

  ## <a name="additional-resources"></a><span data-ttu-id="e72de-196">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e72de-196">Additional resources</span></span>

  [<span data-ttu-id="e72de-197">Jauna e-tirdzniecības nomnieka izvietošana</span><span class="sxs-lookup"><span data-stu-id="e72de-197">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

  [<span data-ttu-id="e72de-198">Tiešsaistes veikala kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="e72de-198">Set up an online store channel</span></span>](online-stores.md)

  [<span data-ttu-id="e72de-199">E-komercijas vietnes izveide</span><span class="sxs-lookup"><span data-stu-id="e72de-199">Create an e-commerce site</span></span>](create-ecommerce-site.md)

  [<span data-ttu-id="e72de-200">Vietnes Dynamics 365 Commerce saistīšana ar tiešsaistes kanālu</span><span class="sxs-lookup"><span data-stu-id="e72de-200">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

  [<span data-ttu-id="e72de-201">Failu robots.txt pārvaldība</span><span class="sxs-lookup"><span data-stu-id="e72de-201">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

  [<span data-ttu-id="e72de-202">Novirzīšanas URL lielapjoma augšupielāde</span><span class="sxs-lookup"><span data-stu-id="e72de-202">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

  [<span data-ttu-id="e72de-203">B2C nomnieka iestatīšana programmā Commerce</span><span class="sxs-lookup"><span data-stu-id="e72de-203">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

  [<span data-ttu-id="e72de-204">Pielāgotu lapu iestatīšana lietotāja pieteikumiem</span><span class="sxs-lookup"><span data-stu-id="e72de-204">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

  [<span data-ttu-id="e72de-205">Vairāku B2C nomnieku konfigurēšana Commerce vidē</span><span class="sxs-lookup"><span data-stu-id="e72de-205">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

  [<span data-ttu-id="e72de-206">Atbalsta pievienošana satura piegādes tīklam (CDN)</span><span class="sxs-lookup"><span data-stu-id="e72de-206">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

  [<span data-ttu-id="e72de-207">Veikala noteikšanas iespējošana pēc atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="e72de-207">Enable location-based store detection</span></span>](enable-store-detection.md)
