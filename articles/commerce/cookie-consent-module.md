---
title: Sīkfailu piekrišanas modulis
description: Šajā tēmā tiek stāstīts par sīkfailu piekrišanas moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 842096c6e3045e434aced9642c86690e2ff7483a
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761408"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="53969-103">Sīkfailu piekrišanas modulis</span><span class="sxs-lookup"><span data-stu-id="53969-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="53969-104">Šajā tēmā tiek stāstīts par sīkfailu piekrišanas moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="53969-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="53969-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="53969-105">Overview</span></span>

<span data-ttu-id="53969-106">Sīkfailu piekrišanas modulis liek vietnes lietotājiem skaidri sniegt piekrišanu, lai atļautu sīkfailus jebkuram līdzeklim vai modulim, kas izseko pārlūka sīkfailus.</span><span class="sxs-lookup"><span data-stu-id="53969-106">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="53969-107">Piekrišana ir nepieciešama pirmoreiz, kad vietnes lietotājs pārlūko vietni jaunā pārlūka sesijā.</span><span class="sxs-lookup"><span data-stu-id="53969-107">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="53969-108">Kad tiek saņemts piekrišana, tā tiek izsekota, un vietnes lietotājs vairs netiks brīdināts par piekrišanu.</span><span class="sxs-lookup"><span data-stu-id="53969-108">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="53969-109">Lai iegūtu papildinformāciju, skatiet [Sīkfailu piekrišana](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="53969-109">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="53969-110">Ja vietnes lietotāja sīkfailu piekrišana netiek saņemta, tad visi līdzekļi vai moduļi, kuriem nepieciešama sīkfailu piekrišana, netiks renderēti lapā.</span><span class="sxs-lookup"><span data-stu-id="53969-110">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="53969-111">Piemēram, izrakstīšanās modulis, sociālās koplietošanas modulis un vēlamās krātuves līdzeklis prasa sīkfailu piekrišanu un netiks renderēti, ja vietnes lietotāja piekrišana nav saņemta.</span><span class="sxs-lookup"><span data-stu-id="53969-111">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="53969-112">Sīkdatņu piekrišanas moduli var konfigurēt lapas galvenes fragmentā, lai to varētu ieviest, kad tiek ielādēta lapa.</span><span class="sxs-lookup"><span data-stu-id="53969-112">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="53969-113">Sīkfaila piekrišanas modulim ir jābūt skaidram ziņojumam, kas informē vietnes lietotāju par sīkfailu izmantošanu vietnē, un tam jāsniedz saite uz vietnes konfidencialitātes lapu.</span><span class="sxs-lookup"><span data-stu-id="53969-113">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="53969-114">Sekojošajā attēlā ir parādīts sīkfailu piekrišanas ziņojuma piemērs ar saiti uz vietnes konfidencialitātes politikas lapu, kas tiek rādīta vietnes lapas galvenē.</span><span class="sxs-lookup"><span data-stu-id="53969-114">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="53969-115">![Sīkfailu piekrišanas moduļa piemērs](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="53969-115">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="53969-116">Sīkfailu piekrišanas moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="53969-116">Cookie consent module properties</span></span>

| <span data-ttu-id="53969-117">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="53969-117">Property name</span></span>             | <span data-ttu-id="53969-118">Vērtība</span><span class="sxs-lookup"><span data-stu-id="53969-118">Value</span></span>                 | <span data-ttu-id="53969-119">Apraksts</span><span class="sxs-lookup"><span data-stu-id="53969-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="53969-120">Bagātināts teksts</span><span class="sxs-lookup"><span data-stu-id="53969-120">Rich Text</span></span>                  | <span data-ttu-id="53969-121">Bagātināts teksts</span><span class="sxs-lookup"><span data-stu-id="53969-121">Rich Text</span></span> | <span data-ttu-id="53969-122">Norāda bagātināta teksta paziņojumu vietnes lietotājiem, ka vietne izmanto pārlūkprogrammas sīkfailus un ka lietotājiem ir jāakceptē sīkfailu izmantošana vietnei, lai tā būtu pilnībā funkcionāla.</span><span class="sxs-lookup"><span data-stu-id="53969-122">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="53969-123">Saites</span><span class="sxs-lookup"><span data-stu-id="53969-123">Links</span></span> | <span data-ttu-id="53969-124">Vietrādis URL</span><span class="sxs-lookup"><span data-stu-id="53969-124">URL</span></span> | <span data-ttu-id="53969-125">Vienu vai vairākas saites var pievienot vietnes konfidencialitātes lapai, kas apraksta sīkfailus, kas tiek izsekoti vietnē.</span><span class="sxs-lookup"><span data-stu-id="53969-125">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="53969-126">Pievienot sīkfailu piekrišanas moduli vietnes lapām</span><span class="sxs-lookup"><span data-stu-id="53969-126">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="53969-127">Lai efektīvi pievienotu sīkfailu piekrišanas moduli vairākām vietnes lapām, to var pievienot koplietojamās lapas galvenes fragmentam.</span><span class="sxs-lookup"><span data-stu-id="53969-127">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="53969-128">Kad galvenes fragments ir pievienots visām vietnes lapām, sīkfailu piekrišanas paziņojums tiks automātiski atveidots, pirmoreiz, kad vietnes lietotājs naviģē uz jebkuru vietnes lapu.</span><span class="sxs-lookup"><span data-stu-id="53969-128">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="53969-129">Papildinformāciju par galveņu fragmentiem un moduļiem skatiet šeit: [Galvenes modulis](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="53969-129">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="53969-130">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="53969-130">Additional resources</span></span>

[<span data-ttu-id="53969-131">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="53969-131">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="53969-132">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="53969-132">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="53969-133">Sīkfailu atbilstība</span><span class="sxs-lookup"><span data-stu-id="53969-133">Cookie compliance</span></span>](cookie-compliance.md)
