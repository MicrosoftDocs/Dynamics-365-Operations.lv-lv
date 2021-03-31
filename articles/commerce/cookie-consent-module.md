---
title: Sīkfailu piekrišanas modulis
description: Šajā tēmā aplūkoti sīkdatņu piekrišanas moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 57c8876f1faf08ce965ccd796551996a8651e2eb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213942"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="b22f5-103">Sīkfailu piekrišanas modulis</span><span class="sxs-lookup"><span data-stu-id="b22f5-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b22f5-104">Šajā tēmā aplūkoti sīkdatņu piekrišanas moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b22f5-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b22f5-105">Sīkfailu piekrišanas modulis liek vietnes lietotājiem skaidri sniegt piekrišanu, lai atļautu sīkfailus jebkuram līdzeklim vai modulim, kas izseko pārlūka sīkfailus.</span><span class="sxs-lookup"><span data-stu-id="b22f5-105">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="b22f5-106">Piekrišana ir nepieciešama pirmoreiz, kad vietnes lietotājs pārlūko vietni jaunā pārlūka sesijā.</span><span class="sxs-lookup"><span data-stu-id="b22f5-106">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="b22f5-107">Kad tiek saņemts piekrišana, tā tiek izsekota, un vietnes lietotājs vairs netiks brīdināts par piekrišanu.</span><span class="sxs-lookup"><span data-stu-id="b22f5-107">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="b22f5-108">Lai iegūtu papildinformāciju, skatiet [Sīkfailu piekrišana](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="b22f5-108">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="b22f5-109">Ja vietnes lietotāja sīkfailu piekrišana netiek saņemta, tad visi līdzekļi vai moduļi, kuriem nepieciešama sīkfailu piekrišana, netiks renderēti lapā.</span><span class="sxs-lookup"><span data-stu-id="b22f5-109">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="b22f5-110">Piemēram, izrakstīšanās modulis, sociālās koplietošanas modulis un vēlamās krātuves līdzeklis prasa sīkfailu piekrišanu un netiks renderēti, ja vietnes lietotāja piekrišana nav saņemta.</span><span class="sxs-lookup"><span data-stu-id="b22f5-110">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="b22f5-111">Sīkdatņu piekrišanas moduli var konfigurēt lapas galvenes fragmentā, lai to varētu ieviest, kad tiek ielādēta lapa.</span><span class="sxs-lookup"><span data-stu-id="b22f5-111">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="b22f5-112">Sīkfaila piekrišanas modulim ir jābūt skaidram ziņojumam, kas informē vietnes lietotāju par sīkfailu izmantošanu vietnē, un tam jāsniedz saite uz vietnes konfidencialitātes lapu.</span><span class="sxs-lookup"><span data-stu-id="b22f5-112">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="b22f5-113">Sekojošajā attēlā ir parādīts sīkfailu piekrišanas ziņojuma piemērs ar saiti uz vietnes konfidencialitātes politikas lapu, kas tiek rādīta vietnes lapas galvenē.</span><span class="sxs-lookup"><span data-stu-id="b22f5-113">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="b22f5-114">![Sīkfailu piekrišanas moduļa piemērs](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="b22f5-114">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="b22f5-115">Sīkfailu piekrišanas moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="b22f5-115">Cookie consent module properties</span></span>

| <span data-ttu-id="b22f5-116">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="b22f5-116">Property name</span></span>             | <span data-ttu-id="b22f5-117">Vērtība</span><span class="sxs-lookup"><span data-stu-id="b22f5-117">Value</span></span>                 | <span data-ttu-id="b22f5-118">Apraksts</span><span class="sxs-lookup"><span data-stu-id="b22f5-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="b22f5-119">Bagātināts teksts</span><span class="sxs-lookup"><span data-stu-id="b22f5-119">Rich Text</span></span>                  | <span data-ttu-id="b22f5-120">Bagātināts teksts</span><span class="sxs-lookup"><span data-stu-id="b22f5-120">Rich Text</span></span> | <span data-ttu-id="b22f5-121">Norāda bagātināta teksta paziņojumu vietnes lietotājiem, ka vietne izmanto pārlūkprogrammas sīkfailus un ka lietotājiem ir jāakceptē sīkfailu izmantošana vietnei, lai tā būtu pilnībā funkcionāla.</span><span class="sxs-lookup"><span data-stu-id="b22f5-121">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="b22f5-122">Saites</span><span class="sxs-lookup"><span data-stu-id="b22f5-122">Links</span></span> | <span data-ttu-id="b22f5-123">Vietrādis URL</span><span class="sxs-lookup"><span data-stu-id="b22f5-123">URL</span></span> | <span data-ttu-id="b22f5-124">Vienu vai vairākas saites var pievienot vietnes konfidencialitātes lapai, kas apraksta sīkfailus, kas tiek izsekoti vietnē.</span><span class="sxs-lookup"><span data-stu-id="b22f5-124">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="b22f5-125">Pievienot sīkfailu piekrišanas moduli vietnes lapām</span><span class="sxs-lookup"><span data-stu-id="b22f5-125">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="b22f5-126">Lai efektīvi pievienotu sīkfailu piekrišanas moduli vairākām vietnes lapām, to var pievienot koplietojamās lapas galvenes fragmentam.</span><span class="sxs-lookup"><span data-stu-id="b22f5-126">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="b22f5-127">Kad galvenes fragments ir pievienots visām vietnes lapām, sīkfailu piekrišanas paziņojums tiks automātiski atveidots, pirmoreiz, kad vietnes lietotājs naviģē uz jebkuru vietnes lapu.</span><span class="sxs-lookup"><span data-stu-id="b22f5-127">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="b22f5-128">Papildinformāciju par galveņu fragmentiem un moduļiem skatiet šeit: [Galvenes modulis](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="b22f5-128">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b22f5-129">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="b22f5-129">Additional resources</span></span>

[<span data-ttu-id="b22f5-130">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="b22f5-130">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b22f5-131">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="b22f5-131">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="b22f5-132">Sīkfailu atbilstība</span><span class="sxs-lookup"><span data-stu-id="b22f5-132">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]