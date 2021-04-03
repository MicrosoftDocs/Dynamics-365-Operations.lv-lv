---
title: Jauna e-tirdzniecības nomnieka izvietošana
description: Šajā tēmā ir aprakstīts, kā izvietot jaunu Dynamics 365 Commerce e-komercijas vietni, izmantojot Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 07/02/2020
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
ms.openlocfilehash: d31e3e7248809a00ad51183b80205d1351567ab3
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477880"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="fec89-103">Jauna e-tirdzniecības nomnieka izvietošana</span><span class="sxs-lookup"><span data-stu-id="fec89-103">Deploy a new e-commerce tenant</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fec89-104">Šajā tēmā ir aprakstīts, kā izvietot jaunu Dynamics 365 Commerce e-komercijas vietni, izmantojot Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="fec89-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="fec89-105">Microsoft Dynamics Lifecycle Services (LCS) ir mākonī balstīta sadarbības darbvieta, ko partneri un klienti var izmantot, lai pārvaldītu savus projektus un vides, skatīt jaunāko informāciju par Microsoft Dynamics precēm un līdzekļiem, kā arī izveidotu, izsekotu un pārlūkotu atbalsta incidentus.</span><span class="sxs-lookup"><span data-stu-id="fec89-105">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="fec89-106">E-komercijas pārvaldības līdzekļi ir integrēti LCS.</span><span class="sxs-lookup"><span data-stu-id="fec89-106">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="fec89-107">Lai uzzinātu vairāk par LCS skatiet [Lifecycle Services lietotāja rokasgrāmatā](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="fec89-107">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="fec89-108">Darba sākšana</span><span class="sxs-lookup"><span data-stu-id="fec89-108">Get started</span></span>

<span data-ttu-id="fec89-109">Pirms e-komercijas inicializēšanas ir jāinicializē projekts, vide un Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="fec89-109">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="fec89-110">Lai veiktu inicializēšanu LCS, jums jābūt vai nu projekta īpašnieka vai vides pārvaldnieka lomas atļaujai.</span><span class="sxs-lookup"><span data-stu-id="fec89-110">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="fec89-111">Tiek atbalstītas ražošanas un smilškastes vides topoloģijas.</span><span class="sxs-lookup"><span data-stu-id="fec89-111">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="fec89-112">Lai iegūtu vairāk informācijas par vidi, skatiet [Vides plānošana](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="fec89-112">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="fec89-113">Lai iegūtu vairāk informācijas par RCSU, skatiet [Inicializēt Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="fec89-113">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="fec89-114">E-komercijas inicializēšana</span><span class="sxs-lookup"><span data-stu-id="fec89-114">Initialize e-commerce</span></span>

<span data-ttu-id="fec89-115">Izmantojiet šo procedūru, lai esošajā vidē inicializētu e-komercijas līdzekli.</span><span class="sxs-lookup"><span data-stu-id="fec89-115">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="fec89-116">Pirms sākt, pārliecinieties, ka jums ir tālāk minētā nepieciešamā informācija.</span><span class="sxs-lookup"><span data-stu-id="fec89-116">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="fec89-117">Izmantojamais RCSU.</span><span class="sxs-lookup"><span data-stu-id="fec89-117">The RCSU that will be used.</span></span>
- <span data-ttu-id="fec89-118">Microsoft Azure Active Directory drošības grupa, kas tiks izmantota e-komercijas sistēmas administratoriem.</span><span class="sxs-lookup"><span data-stu-id="fec89-118">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="fec89-119">Microsoft Azure Active Directory drošības grupa, kas tiks izmantota vērtējumu un apskatu moderatoriem.</span><span class="sxs-lookup"><span data-stu-id="fec89-119">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="fec89-120">Domēni, kas tiks saistīti ar vidi.</span><span class="sxs-lookup"><span data-stu-id="fec89-120">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="fec89-121">Pēc izvēles papildus varat ievākt tālāk minēto informāciju.</span><span class="sxs-lookup"><span data-stu-id="fec89-121">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="fec89-122">Azure AD bizness–patērētājs (B2C) informācija:</span><span class="sxs-lookup"><span data-stu-id="fec89-122">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="fec89-123">Nomnieka nosaukums.</span><span class="sxs-lookup"><span data-stu-id="fec89-123">Tenant Name.</span></span>
    - <span data-ttu-id="fec89-124">Klienta ID.</span><span class="sxs-lookup"><span data-stu-id="fec89-124">Client ID.</span></span>
    - <span data-ttu-id="fec89-125">Pielāgotā domēna pieteikšanās.</span><span class="sxs-lookup"><span data-stu-id="fec89-125">Login Custom Domain.</span></span>
    - <span data-ttu-id="fec89-126">Atbildes URL.</span><span class="sxs-lookup"><span data-stu-id="fec89-126">Reply URL.</span></span>
    - <span data-ttu-id="fec89-127">Parakstīšanās un pierakstīšanās politikas ID.</span><span class="sxs-lookup"><span data-stu-id="fec89-127">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="fec89-128">Paroles atiestatīšanas politikas ID.</span><span class="sxs-lookup"><span data-stu-id="fec89-128">Reset password Policy ID.</span></span>
    - <span data-ttu-id="fec89-129">Profila rediģēšanas politikas ID.</span><span class="sxs-lookup"><span data-stu-id="fec89-129">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="fec89-130">Šo informāciju var pievienot vēlāk, izmantojot pakalpojuma pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="fec89-130">This information can be added later, through a service request.</span></span>

<span data-ttu-id="fec89-131">Pēc tam, kad ievākta nepieciešamā informācija, veiciet tālāk minētās darbības, lai inicializētu e-komerciju.</span><span class="sxs-lookup"><span data-stu-id="fec89-131">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="fec89-132">Pierakstieties [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="fec89-132">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="fec89-133">Atveriet projektu, kas satur vidi, kurā vēlaties inicializēt e-komerciju.</span><span class="sxs-lookup"><span data-stu-id="fec89-133">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="fec89-134">Sadaļā **Vides** atlasiet vidi.</span><span class="sxs-lookup"><span data-stu-id="fec89-134">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="fec89-135">Sadaļā **Vides līdzekļi** atlasiet saiti **Mazumtirdzniecības pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="fec89-135">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="fec89-136">Cilnē **E-tirdzniecība** atlasiet **Iestatīt**.</span><span class="sxs-lookup"><span data-stu-id="fec89-136">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="fec89-137">Parādās dialoglodziņš, kur jāievada informācija, kas nepieciešama nodrošināšanai.</span><span class="sxs-lookup"><span data-stu-id="fec89-137">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="fec89-138">Ievadiet nepieciešamo informāciju un pēc tam dodieties uz nākamo lapu.</span><span class="sxs-lookup"><span data-stu-id="fec89-138">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="fec89-139">Nākamajā lapā ievadiet nepieciešamo informāciju un pēc iesniedziet veidlapu.</span><span class="sxs-lookup"><span data-stu-id="fec89-139">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="fec89-140">Notiks atgriešanās atpakaļ cilnē **E-tirdzniecība**, kur ir jābūt redzamam, ka inicializēšana ir uzsākta.</span><span class="sxs-lookup"><span data-stu-id="fec89-140">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="fec89-141">Lai skatītu inicializēšanas statusu, vai nu nospiediet **Atsvaidzināt**, vai arī vēlāk atgriezieties cilnē **E-tirdzniecība**.</span><span class="sxs-lookup"><span data-stu-id="fec89-141">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="fec89-142">Kad e-komercija tiek inicializēta no LCS, sistēma nodrošina vairākus komponentus, kas nepieciešami e-komercijai, un saista tos ar vidi.</span><span class="sxs-lookup"><span data-stu-id="fec89-142">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="fec89-143">Kad nodrošināšana pabeigta, tiek atjaunināta cilne **E-komercija** lapā **Mazumtirdzniecības pārvaldība**, lai atspoguļotu nodrošināšanu.</span><span class="sxs-lookup"><span data-stu-id="fec89-143">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="fec89-144">Lapa parāda jaunākās pielāgošanas izvietošanas un visu citu notiekošo izvietošanu statusu.</span><span class="sxs-lookup"><span data-stu-id="fec89-144">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="fec89-145">Tajā ir arī saites uz e-komercijas vietni un e-komercijas vietnes veidotāju, kurā vietnes tiek autorētas.</span><span class="sxs-lookup"><span data-stu-id="fec89-145">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="fec89-146">Piekļuve Commerce vietnes veidotājam</span><span class="sxs-lookup"><span data-stu-id="fec89-146">Access Commerce site builder</span></span>

<span data-ttu-id="fec89-147">Lai piekļūtu Commerce vietnes veidotājam, dodieties uz cilni **Komercija** LCS lapā **Mazumtirdziecības pārvaldība** un atlasiet saiti **e-komercijas vietnes pārvaldības rīks**.</span><span class="sxs-lookup"><span data-stu-id="fec89-147">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="fec89-148">Vietnes veidotāja izvietošanas lapa tiek parādīts nomnieka līmeņa skatījums.</span><span class="sxs-lookup"><span data-stu-id="fec89-148">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="fec89-149">No šīs lapas iespējams veikt tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="fec89-149">From this page, you can:</span></span>

- <span data-ttu-id="fec89-150">Modificēt nomnieka līmeņa iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="fec89-150">Modify tenant-level settings.</span></span>
- <span data-ttu-id="fec89-151">Doties uz jebkuru jūsu izveidoto vietni, un jums ir atļauja to apskatīt.</span><span class="sxs-lookup"><span data-stu-id="fec89-151">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="fec89-152">Piekļuves apskatu funkcijas, piemēram, regulēšanu un ziņošanu.</span><span class="sxs-lookup"><span data-stu-id="fec89-152">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="fec89-153">Izveidot jaunu vietni.</span><span class="sxs-lookup"><span data-stu-id="fec89-153">Create a new site.</span></span> <span data-ttu-id="fec89-154">Papildinformāciju par to, kā izveidot jaunu vietni, skatiet sadaļā [E-komercijas vietnes izveide](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="fec89-154">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="fec89-155">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="fec89-155">Additional resources</span></span>

[<span data-ttu-id="fec89-156">Domēna nosaukuma konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="fec89-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="fec89-157">E-komercijas vietnes izveide</span><span class="sxs-lookup"><span data-stu-id="fec89-157">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="fec89-158">Vietnes Dynamics 365 Commerce saistīšana ar tiešsaistes kanālu</span><span class="sxs-lookup"><span data-stu-id="fec89-158">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="fec89-159">Failu robots.txt pārvaldība</span><span class="sxs-lookup"><span data-stu-id="fec89-159">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="fec89-160">Novirzīšanas URL lielapjoma augšupielāde</span><span class="sxs-lookup"><span data-stu-id="fec89-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="fec89-161">B2C nomnieka iestatīšana programmā Commerce</span><span class="sxs-lookup"><span data-stu-id="fec89-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="fec89-162">Pielāgotu lapu iestatīšana lietotāja pieteikumiem</span><span class="sxs-lookup"><span data-stu-id="fec89-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="fec89-163">Vairāku B2C nomnieku konfigurēšana Commerce vidē</span><span class="sxs-lookup"><span data-stu-id="fec89-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="fec89-164">Atbalsta pievienošana satura piegādes tīklam (CDN)</span><span class="sxs-lookup"><span data-stu-id="fec89-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="fec89-165">Veikala noteikšanas iespējošana pēc atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="fec89-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
