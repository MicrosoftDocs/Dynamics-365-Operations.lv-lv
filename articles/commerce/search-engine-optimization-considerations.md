---
title: Meklētājprogrammas optimizēšanas (SEO) apsvērumi jūsu vietnei
description: Šī tēma attiecas uz meklēšanas programmas optimizācijas (SEO) apsvērumiem jūsu vietnē no izstrādes līdz ražošanai.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c4d1a4a1b14f7af1db1c53bd9ee1993cc9187609
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254797"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a><span data-ttu-id="d37d1-103">Meklētājprogrammas optimizēšanas (SEO) apsvērumi jūsu vietnei</span><span class="sxs-lookup"><span data-stu-id="d37d1-103">Search engine optimization (SEO) considerations for your site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d37d1-104">Šī tēma attiecas uz meklēšanas programmas optimizācijas (SEO) apsvērumiem jūsu vietnē no izstrādes līdz ražošanai.</span><span class="sxs-lookup"><span data-stu-id="d37d1-104">This topic covers earch engine optimization (SEO) considerations for your site from development to production.</span></span>

## <a name="a-site-that-is-under-development"></a><span data-ttu-id="d37d1-105">Vietne, kas tiek izstrādāta</span><span class="sxs-lookup"><span data-stu-id="d37d1-105">A site that is under development</span></span>

<span data-ttu-id="d37d1-106">Kamēr vietne tiek izstrādāta, visām vietnes lapām jābūt **NOINDEX** un **NOFOLLOW** meta tagiem, lai meklēšanas programmas neatzīmē jūs vietnes lapas un veikala izstrādes versijas jūsu savā kešatmiņā.</span><span class="sxs-lookup"><span data-stu-id="d37d1-106">While a site is under development, all site pages should have the **NOINDEX** and **NOFOLLOW** meta tags, so that search engines don't index the pages and store development versions of your site in their cache.</span></span> <span data-ttu-id="d37d1-107">Lai veiktu šo konfigurāciju, ir jāpievieno noklusējuma meta tagu modulis vietnes lapas veidnei.</span><span class="sxs-lookup"><span data-stu-id="d37d1-107">To do this configuration, you must add the default meta tags module to the site page template.</span></span> <span data-ttu-id="d37d1-108">Noklusējuma meta tagu rekvizīti tad būs pieejami SEO rekvizītu sadaļā lapas redaktorā.</span><span class="sxs-lookup"><span data-stu-id="d37d1-108">The default meta tags properties will then be available in the SEO properties section in the page editor.</span></span> <span data-ttu-id="d37d1-109">Varat izmantot šos rekvizītus, lai pārvaldītu meta tagus.</span><span class="sxs-lookup"><span data-stu-id="d37d1-109">You can use these properties to manage the meta tags.</span></span>

## <a name="soft-launch-of-a-site"></a><span data-ttu-id="d37d1-110">Vietnes viegla palaišana</span><span class="sxs-lookup"><span data-stu-id="d37d1-110">Soft launch of a site</span></span>

<span data-ttu-id="d37d1-111">“Vieglas palaišanas” laikā vietne ir pieejama ierobežotai auditorijai vai tirgum, pirms tiek veikta pilna palaišana.</span><span class="sxs-lookup"><span data-stu-id="d37d1-111">During a "soft launch," a website is made available to a limited audience or market before the full launch occurs.</span></span> <span data-ttu-id="d37d1-112">Ja jūs veicat savas tīmekļa vietnes vieglo palaišanu, jums vajadzētu apsvērt iespēju atstāt **NOINDEX** meta tagus.</span><span class="sxs-lookup"><span data-stu-id="d37d1-112">If you do a soft launch of your website, you should consider leaving the **NOINDEX** meta tags in place.</span></span> <span data-ttu-id="d37d1-113">Šādā veidā jūs palīdzēsiet nodrošināt, ka vieglā palaišana joprojām ir ierobežota ar ierobežotu auditoriju, ko vēlaties sasniegt.</span><span class="sxs-lookup"><span data-stu-id="d37d1-113">In this way, you help guarantee that the soft launch remains restricted to the limited audience that you want to reach.</span></span>

## <a name="a-site-that-is-in-production"></a><span data-ttu-id="d37d1-114">Vietne, kas ir ražošanā</span><span class="sxs-lookup"><span data-stu-id="d37d1-114">A site that is in production</span></span>

<span data-ttu-id="d37d1-115">Kad vietne ir ražošanā, jums jāpārliecinās, ka visas vietnes lapas ir pareizi atzīmētas.</span><span class="sxs-lookup"><span data-stu-id="d37d1-115">When a site is in production, you should make sure that all site pages are correctly tagged.</span></span> <span data-ttu-id="d37d1-116">Programma Microsoft Dynamics 365 Commerce izmanto informāciju, kas ievadīta lapā, lai padarītu visu SEO informāciju šajā lapā.</span><span class="sxs-lookup"><span data-stu-id="d37d1-116">Microsoft Dynamics 365 Commerce uses the information that is entered for a page to render all the SEO information on that page.</span></span> <span data-ttu-id="d37d1-117">Šie moduļi nodrošina šo funkcionalitāti: kategorijas lapas kopsavilkumu, saraksta lapas kopsavilkumu un preces lapas kopsavilkumu.</span><span class="sxs-lookup"><span data-stu-id="d37d1-117">The following modules provide this functionality: category page summary, list page summary, and product page summary.</span></span>

<span data-ttu-id="d37d1-118">Lai optimizētu meklēšanas programmas indeksēšanu, atveidošanas struktūra izmanto gan informāciju no SEO rekvizītiem, kas konfigurēti Dynamics 365 Commerce modulī, gan moduļa specifisko informāciju.</span><span class="sxs-lookup"><span data-stu-id="d37d1-118">To optimize search engine indexing, the rendering framework uses both information from the SEO properties that are configured in Dynamics 365 Commerce and module-specific information.</span></span> <span data-ttu-id="d37d1-119">Attiecībā uz vietni, kas ir ražošanā, jums jāpārliecinās, ka fails robots.txt ļauj indeksēt visu jūsu vietni un ka tā satur saites uz jūsu publicēto vietnes kartes dokumentu.</span><span class="sxs-lookup"><span data-stu-id="d37d1-119">For a site that is in production, you should make sure that the robots.txt file allows for indexing of your whole site, and that it contains links to your published site map document.</span></span> <span data-ttu-id="d37d1-120">Jums ir jāieslēdz vietnes kartes ģenerēšanas funkcionalitāte **Vietnes iestatījumi \> Vietnes kartes iespējotas**.</span><span class="sxs-lookup"><span data-stu-id="d37d1-120">You should turn on the site map generation functionality at **Site Settings \> Site maps enabled**.</span></span>

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a><span data-ttu-id="d37d1-121">Lapas SEO iestatījumi iekšējam priekšskatījumam, ierobežotas auditorijas un visas auditorijas</span><span class="sxs-lookup"><span data-stu-id="d37d1-121">Page SEO settings for internal preview, limited audiences, and all audiences</span></span>

<span data-ttu-id="d37d1-122">Tā kā Dynamics 365 Commerce atbalsta “ko redzat, to iegūstat”(WYSIWYG) autentificētus priekšskatījumus vizuālo lapu veidotājā, autori var sagatavot savu lapas saturu, neuztraucoties, ka šī informācija tiks rādīta vietnes apmeklētājiem.</span><span class="sxs-lookup"><span data-stu-id="d37d1-122">Because Dynamics 365 Commerce supports "what you see is what you get" (WYSIWYG) authenticated previews in visual page builder, authors can prepare their page content without having to worry that the information will become visible to site visitors.</span></span> <span data-ttu-id="d37d1-123">Ja lapa ir jāpublicē, bet tās pieejamībai jābūt ierobežotai, tai jābūt **NOINDEX** meta tagam, lai meklēšanas programmas to neindeksētu.</span><span class="sxs-lookup"><span data-stu-id="d37d1-123">If a page must be published, but its exposure must be limited, it should have the **NOINDEX** meta tag, so that it won't be indexed by search engines.</span></span> <span data-ttu-id="d37d1-124">Pēc tam, kad lapa ir gatava visām auditorijām, visiem pamata SEO metadatiem ir jābūt klātesošiem, lai palielinātu meklēšanas programmu indeksācijas efektivitāti.</span><span class="sxs-lookup"><span data-stu-id="d37d1-124">Then, when the page is ready for all audiences, all the basic SEO metadata should be present, to maximize the efficiency of search engine indexing.</span></span> <span data-ttu-id="d37d1-125">Turklāt **NOLIMIT** meta tags ir jānoņem.</span><span class="sxs-lookup"><span data-stu-id="d37d1-125">Additionally, the **NOLIMIT** meta tag should be removed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d37d1-126">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d37d1-126">Additional resources</span></span>

[<span data-ttu-id="d37d1-127">Lietotāju un lomu pārvaldība E-tirdzniecībā</span><span class="sxs-lookup"><span data-stu-id="d37d1-127">Manage e-Commerce users and roles</span></span>](manage-ecommerce-users-roles.md)

[<span data-ttu-id="d37d1-128">Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju</span><span class="sxs-lookup"><span data-stu-id="d37d1-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="d37d1-129">Satura drošības politikas (CSP) pārvaldība</span><span class="sxs-lookup"><span data-stu-id="d37d1-129">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]