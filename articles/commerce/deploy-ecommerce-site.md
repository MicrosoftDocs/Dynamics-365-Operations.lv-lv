---
title: Jauna e-tirdzniecības nomnieka izvietošana
description: Šajā tēmā ir aprakstīts, kā izvietot jaunu e-tirdzniecības nomnieku, izmantojot Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: 6d7dfcaf244260de5f39a1201ec1ea78e94351e7
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001787"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="fc2be-103">Jauna e-tirdzniecības nomnieka izvietošana</span><span class="sxs-lookup"><span data-stu-id="fc2be-103">Deploy a new e-Commerce tenant</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="fc2be-104">Šajā tēmā ir aprakstīts, kā izvietot jaunu e-tirdzniecības vietni, izmantojot Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="fc2be-104">This topic describes how to deploy a new e-Commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="fc2be-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="fc2be-105">Overview</span></span>

<span data-ttu-id="fc2be-106">Microsoft Dynamics Lifecycle Services (LCS) ir mākonī balstīta sadarbības darbvieta, ko partneri un klienti var izmantot, lai pārvaldītu savus projektus un vides, skatīt jaunāko informāciju par Microsoft Dynamics precēm un līdzekļiem, kā arī izveidotu, izsekotu un pārlūkotu atbalsta incidentus.</span><span class="sxs-lookup"><span data-stu-id="fc2be-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="fc2be-107">E-tirdzniecības pārvaldības līdzekļi ir integrēti LCS.</span><span class="sxs-lookup"><span data-stu-id="fc2be-107">E-Commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="fc2be-108">Lai uzzinātu vairāk par LCS skatiet [Lifecycle Services lietotāja rokasgrāmatā](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="fc2be-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="fc2be-109">Sākt darbu</span><span class="sxs-lookup"><span data-stu-id="fc2be-109">Get started</span></span>

<span data-ttu-id="fc2be-110">Pirms e-tirdzniecības inicializēšanas ir jāinicializē projekts, vide un Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="fc2be-110">Before you can initialize e-Commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="fc2be-111">Lai veiktu inicializēšanu LCS, jums jābūt vai nu projekta īpašnieka vai vides pārvaldnieka lomas atļaujai.</span><span class="sxs-lookup"><span data-stu-id="fc2be-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="fc2be-112">Tiek atbalstītas ražošanas un smilškastes vides topoloģijas.</span><span class="sxs-lookup"><span data-stu-id="fc2be-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="fc2be-113">Lai iegūtu vairāk informācijas par vidi, skatiet [Vides plānošana](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="fc2be-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="fc2be-114">Lai iegūtu vairāk informācijas par RCSU, skatiet [Retail Cloud Scale Unit inicializēšana](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="fc2be-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="fc2be-115">E-tirdzniecības inicializēšana</span><span class="sxs-lookup"><span data-stu-id="fc2be-115">Initialize e-Commerce</span></span>

<span data-ttu-id="fc2be-116">Izmantojiet šo procedūru, lai esošajā vidē inicializētu e-tirdzniecības līdzekli.</span><span class="sxs-lookup"><span data-stu-id="fc2be-116">Use this procedure to initialize the e-Commerce feature in an existing environment.</span></span>

<span data-ttu-id="fc2be-117">Pirms sākt, pārliecinieties, ka jums ir tālāk minētā nepieciešamā informācija.</span><span class="sxs-lookup"><span data-stu-id="fc2be-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="fc2be-118">Izmantojamais RCSU.</span><span class="sxs-lookup"><span data-stu-id="fc2be-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="fc2be-119">Microsoft Azure Active Directory drošības grupa, kas tiks izmantota e-tirdzniecības sistēmas administratoriem.</span><span class="sxs-lookup"><span data-stu-id="fc2be-119">The Microsoft Azure Active Directory security group that will be used for e-Commerce system admins.</span></span>
- <span data-ttu-id="fc2be-120">Microsoft Azure Active Directory drošības grupa, kas tiks izmantota vērtējumu un apskatu moderatoriem.</span><span class="sxs-lookup"><span data-stu-id="fc2be-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="fc2be-121">Domēni, kas tiks saistīti ar vidi.</span><span class="sxs-lookup"><span data-stu-id="fc2be-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="fc2be-122">Pēc izvēles papildus varat ievākt tālāk minēto informāciju.</span><span class="sxs-lookup"><span data-stu-id="fc2be-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="fc2be-123">Azure AD bizness–patērētājs (B2C) informācija:</span><span class="sxs-lookup"><span data-stu-id="fc2be-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="fc2be-124">Nomnieka nosaukums.</span><span class="sxs-lookup"><span data-stu-id="fc2be-124">Tenant Name.</span></span>
    - <span data-ttu-id="fc2be-125">Klienta ID.</span><span class="sxs-lookup"><span data-stu-id="fc2be-125">Client ID.</span></span>
    - <span data-ttu-id="fc2be-126">Pielāgotā domēna pieteikšanās.</span><span class="sxs-lookup"><span data-stu-id="fc2be-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="fc2be-127">Atbildes URL.</span><span class="sxs-lookup"><span data-stu-id="fc2be-127">Reply URL.</span></span>
    - <span data-ttu-id="fc2be-128">Parakstīšanās un pierakstīšanās politikas ID.</span><span class="sxs-lookup"><span data-stu-id="fc2be-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="fc2be-129">Paroles atiestatīšanas politikas ID.</span><span class="sxs-lookup"><span data-stu-id="fc2be-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="fc2be-130">Profila rediģēšanas politikas ID.</span><span class="sxs-lookup"><span data-stu-id="fc2be-130">Edit Profile Policy ID.</span></span>

[!NOTE]
<span data-ttu-id="fc2be-131">Šo informāciju var pievienot vēlāk, izmantojot pakalpojuma pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="fc2be-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="fc2be-132">Pēc tam, kad ievākta nepieciešamā informācija, veiciet tālāk minētās darbības, lai inicializētu e-tirdzniecību.</span><span class="sxs-lookup"><span data-stu-id="fc2be-132">After you've collected the required information, follow these steps to initialize e-Commerce.</span></span>

1. <span data-ttu-id="fc2be-133">Pierakstieties [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="fc2be-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="fc2be-134">Atveriet projektu, kas satur vidi, kurā vēlaties inicializēt e-tirdzniecību.</span><span class="sxs-lookup"><span data-stu-id="fc2be-134">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="fc2be-135">Sadaļā **Vides** atlasiet vidi.</span><span class="sxs-lookup"><span data-stu-id="fc2be-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="fc2be-136">Sadaļā **Vides līdzekļi**atlasiet saiti **Mazumtirdzniecības pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="fc2be-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="fc2be-137">Cilnē **E-tirdzniecība** atlasiet **Iestatīt**.</span><span class="sxs-lookup"><span data-stu-id="fc2be-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="fc2be-138">Parādās dialoglodziņš, kur jāievada informācija, kas nepieciešama nodrošināšanai.</span><span class="sxs-lookup"><span data-stu-id="fc2be-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="fc2be-139">Ievadiet nepieciešamo informāciju un pēc tam dodieties uz nākamo lapu.</span><span class="sxs-lookup"><span data-stu-id="fc2be-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="fc2be-140">Nākamajā lapā ievadiet nepieciešamo informāciju un pēc iesniedziet veidlapu.</span><span class="sxs-lookup"><span data-stu-id="fc2be-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="fc2be-141">Notiks atgriešanās atpakaļ cilnē **E-tirdzniecība**, kur ir jābūt redzamam, ka inicializēšana ir uzsākta.</span><span class="sxs-lookup"><span data-stu-id="fc2be-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="fc2be-142">Lai skatītu inicializēšanas statusu, vai nu nospiediet **Atsvaidzināt**, vai arī vēlāk atgriezieties cilnē **E-tirdzniecība**.</span><span class="sxs-lookup"><span data-stu-id="fc2be-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="fc2be-143">Kad e-tirdzniecība tiek inicializēta no LCS, sistēma nodrošina vairākus komponentus, kas nepieciešami e-tirdzniecībai, un saista tos ar vidi.</span><span class="sxs-lookup"><span data-stu-id="fc2be-143">When e-Commerce is initialized from LCS, the system provisions several components that are required for e-Commerce and associates them with the environment.</span></span> <span data-ttu-id="fc2be-144">Kad nodrošināšana pabeigta, tiek atjaunināta cilne **E-komercija** lapā **Mazumtirdzniecības pārvaldība**, lai atspoguļotu nodrošināšanu.</span><span class="sxs-lookup"><span data-stu-id="fc2be-144">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="fc2be-145">Lapa parāda jaunākās pielāgošanas izvietošanas un visu citu notiekošo izvietošanu statusu.</span><span class="sxs-lookup"><span data-stu-id="fc2be-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="fc2be-146">Tajā ir arī saites uz e-komercijas vietni un e-komercijas vietnes veidotāju, kurā vietnes tiek autorētas.</span><span class="sxs-lookup"><span data-stu-id="fc2be-146">It also includes links to the e-Commerce site and the e-Commerce site builder where sites are authored.</span></span>

## <a name="access-site-builder"></a><span data-ttu-id="fc2be-147">Piekļuve vietnes veidotājam</span><span class="sxs-lookup"><span data-stu-id="fc2be-147">Access site builder</span></span>

<span data-ttu-id="fc2be-148">Lai piekļūtu vietnes veidotājam, dodieties uz cilni **Komercija** LCS lapā **Mazumtirdziecības pārvaldība** un atlasiet saiti **e-komercijas vietnes pārvaldības rīks**.</span><span class="sxs-lookup"><span data-stu-id="fc2be-148">To access site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="fc2be-149">Vietnes veidotāja izvietošanas lapa tiek parādīts nomnieka līmeņa skatījums.</span><span class="sxs-lookup"><span data-stu-id="fc2be-149">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="fc2be-150">No šīs lapas iespējams veikt tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="fc2be-150">From this page, you can:</span></span>

- <span data-ttu-id="fc2be-151">Modificēt nomnieka līmeņa iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="fc2be-151">Modify tenant-level settings.</span></span>
- <span data-ttu-id="fc2be-152">Doties uz jebkuru jūsu izveidoto vietni, un jums ir atļauja to apskatīt.</span><span class="sxs-lookup"><span data-stu-id="fc2be-152">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="fc2be-153">Piekļuves apskatu funkcijas, piemēram, regulēšanu un ziņošanu.</span><span class="sxs-lookup"><span data-stu-id="fc2be-153">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="fc2be-154">Izveidot jaunu vietni.</span><span class="sxs-lookup"><span data-stu-id="fc2be-154">Create a new site.</span></span> <span data-ttu-id="fc2be-155">Papildinformāciju par to, kā izveidot jaunu vietni, skatiet sadaļā [E-komercijas vietnes izveide](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="fc2be-155">For more information about how to create a new site, see [Create an e-Commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="fc2be-156">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="fc2be-156">Additional resources</span></span>

[<span data-ttu-id="fc2be-157">Domēna nosaukuma konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="fc2be-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="fc2be-158">E-komercijas vietnes izveide</span><span class="sxs-lookup"><span data-stu-id="fc2be-158">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="fc2be-159">Tiešsaistes vietnes saistīšana ar kanālu</span><span class="sxs-lookup"><span data-stu-id="fc2be-159">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="fc2be-160">robots.txt failu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="fc2be-160">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="fc2be-161">Pielāgotu lapu iestatīšana lietotāja pieteikumiem</span><span class="sxs-lookup"><span data-stu-id="fc2be-161">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="fc2be-162">Atbalsta pievienošana satura piegādes tīklam (CDN)</span><span class="sxs-lookup"><span data-stu-id="fc2be-162">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="fc2be-163">Veikala noteikšanas iespējošana pēc atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="fc2be-163">Enable location-based store detection</span></span>](enable-store-detection.md)
