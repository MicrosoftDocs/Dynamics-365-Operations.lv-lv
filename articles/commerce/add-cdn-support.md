---
title: Atbalsta pievienošana satura piegādes tīklam (CDN)
description: Šajā tēmā aprakstīts, kā pievienot satura piegādes tīklu savai Microsoft Dynamics 365 Commerce videi.
author: brianshook
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d653b072eca134c765a5db5659b228648fc13c4a
ms.sourcegitcommit: 3fe4d9a33447aa8a62d704fbbf18aeb9cb667baa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/12/2021
ms.locfileid: "5582723"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="5626d-103">Atbalsta pievienošana satura piegādes tīklam (CDN)</span><span class="sxs-lookup"><span data-stu-id="5626d-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5626d-104">Šajā tēmā aprakstīts, kā pievienot satura piegādes tīklu savai Microsoft Dynamics 365 Commerce videi.</span><span class="sxs-lookup"><span data-stu-id="5626d-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="5626d-105">Iestatot e-komercijas vidi programmā Dynamics 365 Commerce, varat konfigurēt to, lai varētu strādāt ar savu CDN pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="5626d-105">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="5626d-106">Jūsu pielāgoto domēnu var iespējot jūsu e-komercijas vides nodrošināšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="5626d-106">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="5626d-107">Alternatīvi varat izmantot pakalpojuma pieprasījumu, lai to iestatītu pēc nodrošināšanas procesa pabeigšanas.</span><span class="sxs-lookup"><span data-stu-id="5626d-107">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="5626d-108">E-komercijas vides nodrošināšanas process ģenerē resursdatora nosaukumu, kas ir saistīts ar vidi.</span><span class="sxs-lookup"><span data-stu-id="5626d-108">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="5626d-109">Šim resursdatora nosaukumam ir šāds formāts, kur \<*e-commerce-tenant-name*\> ir jūsu vides nosaukums.</span><span class="sxs-lookup"><span data-stu-id="5626d-109">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="5626d-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="5626d-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="5626d-111">Resursdatora nosaukums vai galapunkts, kas tiek ģenerēts nodrošināšanas procesā, atbalsta drošligzdu slāņa (SSL) sertifikātu tikai \*. commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="5626d-111">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="5626d-112">Tas neatbalsta SSL pielāgotiem domēniem.</span><span class="sxs-lookup"><span data-stu-id="5626d-112">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="5626d-113">Tāpēc jums ir jāpārtrauc SSL pielāgotiem domēniem savā CDN un jāpārsūta datplūsma no CDN uz resursdatora nosaukumu vai galapunktu, ko Komercija ir ģenerējusi.</span><span class="sxs-lookup"><span data-stu-id="5626d-113">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="5626d-114">Turklāt *statika* (JavaScript vai kaskādes stila lapu \[CSS\] faili) no Komercijas tiek nodrošināti no Komercijas ģenerētā galapunkta (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="5626d-114">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="5626d-115">Statiku var saglabāt kešatmiņā tikai tad, ja resursdatora nosaukums vai galapunkts, ko ģenerējusi Komercija, tiek novietots pēc CDN.</span><span class="sxs-lookup"><span data-stu-id="5626d-115">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="5626d-116">SSL iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5626d-116">Set up SSL</span></span>

<span data-ttu-id="5626d-117">Lai palīdzētu nodrošināt, ka SSL ir iestatīts un ka statika saglabāta kešatmiņā, jums ir jākonfigurē savs CDN, lai tas būtu saistīts ar resursdatora nosaukumu, ko ģenerēja Komercija jūsu videi.</span><span class="sxs-lookup"><span data-stu-id="5626d-117">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="5626d-118">Sekojošais modelis ir arī jāsaglabā kešatmiņā tikai statikai.</span><span class="sxs-lookup"><span data-stu-id="5626d-118">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="5626d-119">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="5626d-119">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="5626d-120">Pēc tam, kad jūs sniedzat savu Komercijas vidi kopā ar sniegto pielāgoto domēnu, vai pēc tam, kad jūs nodrošināt pielāgotu domēnu jūsu videi, izmantojot pakalpojuma pieprasījumu, norādiet savu pielāgoto domēnu resursdatora nosaukumam vai galapunktam, ko ģenerējusi Komercija.</span><span class="sxs-lookup"><span data-stu-id="5626d-120">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="5626d-121">Kā iepriekš tika minēts, ģenerētais resursdatora nosaukums vai galapunkts atbalsta SSL sertifikātu tikai attiecībā uz \*. commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="5626d-121">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="5626d-122">Tas neatbalsta SSL pielāgotiem domēniem.</span><span class="sxs-lookup"><span data-stu-id="5626d-122">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="5626d-123">CDN pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="5626d-123">CDN services</span></span>

<span data-ttu-id="5626d-124">Jebkuru CDN pakalpojumu var izmantot ar Komercijas vidi.</span><span class="sxs-lookup"><span data-stu-id="5626d-124">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="5626d-125">Tālāk ir sniegti divi piemēri.</span><span class="sxs-lookup"><span data-stu-id="5626d-125">Here are two examples:</span></span>

- <span data-ttu-id="5626d-126">**Microsoft Azure optimālās ieejas pakalpojums** — Azure CDN risinājums.</span><span class="sxs-lookup"><span data-stu-id="5626d-126">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="5626d-127">Papildinformāciju par Azure optimālās ieejas pakalpojumu skatiet tēmā [Azure optimālās ieejas pakalpojuma dokumentācija](https://docs.microsoft.com/azure/frontdoor/)</span><span class="sxs-lookup"><span data-stu-id="5626d-127">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="5626d-128">**Akamai dinamisks vietnes paātrinātājs** – papildinformāciju skatiet tēmā [Dinamisks vietnes paātrinātājs](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="5626d-128">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="5626d-129">CDN iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5626d-129">CDN setup</span></span>

<span data-ttu-id="5626d-130">CDN iestatīšanas process sastāv no šīm vispārīgajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="5626d-130">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="5626d-131">Pievienojiet priekšgala resursdatoru.</span><span class="sxs-lookup"><span data-stu-id="5626d-131">Add a front-end host.</span></span>
1. <span data-ttu-id="5626d-132">Konfigurējiet aizmugursistēmas kopu.</span><span class="sxs-lookup"><span data-stu-id="5626d-132">Configure a backend pool.</span></span>
1. <span data-ttu-id="5626d-133">Iestatiet kārtulas maršrutēšanai un saglabāšanai kešatmiņā.</span><span class="sxs-lookup"><span data-stu-id="5626d-133">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="5626d-134">Priekšgala resursdatora pievienošana</span><span class="sxs-lookup"><span data-stu-id="5626d-134">Add a front-end host</span></span>

<span data-ttu-id="5626d-135">Jebkuru CDN pakalpojumu var izmantot, bet, piemēram, šajā tēmā tiek izmantots Azure optimālās ieejas pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="5626d-135">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="5626d-136">Lai iegūtu informāciju par to, kā iestatīt Azure optimālās ieejas pakalpojumu, skatiet tēmu [Īsa pamācība: izveidojiet optimālo ieeju augstas pieejamības globālai tīmekļa lietojumprogrammai](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="5626d-136">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="5626d-137">Aizmugursistēmas kopas konfigurēšana Azure optimālās ieejas pakalpojumā</span><span class="sxs-lookup"><span data-stu-id="5626d-137">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="5626d-138">Lai konfigurētu aizmugursistēmas kopu Azure optimālās ieejas pakalpojumā, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="5626d-138">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="5626d-139">Pievienojiet **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** aizmugursistēmas kopai kā pielāgotu resursdatoru, kam ir tukšs aizmugursistēmas resursdatora virsraksts.</span><span class="sxs-lookup"><span data-stu-id="5626d-139">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has an empty backend host header.</span></span>
1. <span data-ttu-id="5626d-140">Zem **Slodzes līdzsvarošana** atstājiet noklusējuma vērtības.</span><span class="sxs-lookup"><span data-stu-id="5626d-140">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="5626d-141">Šajā attēlā redzams dialoglodziņš **Pievienot aizmugursistēmu** Azure optimālās ieejas pakalpojumā ar ievadīto aizmugursistēmas resursdatora virsrakstu.</span><span class="sxs-lookup"><span data-stu-id="5626d-141">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![Pievienot aizmugursistēmas kopas dialoglodziņu](./media/CDN_BackendPool.png)

<span data-ttu-id="5626d-143">Šajā attēlā redzams dialoglodziņš **Pievienot aizmugursistēmas kopa** Azure optimālās ieejas pakalpojumā ar noklusējuma noslodzes balansēšanas vērtībām.</span><span class="sxs-lookup"><span data-stu-id="5626d-143">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![c](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="5626d-145">Kārtulu iestatīšāna Azure optimālās ieejas pakalpojumā</span><span class="sxs-lookup"><span data-stu-id="5626d-145">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="5626d-146">Lai uzstādītu maršrutēšanas kārtulu Azure optimālās ieejas pakalpojumā, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="5626d-146">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="5626d-147">Pievienojiet maršrutēšanas kārtulu.</span><span class="sxs-lookup"><span data-stu-id="5626d-147">Add a routing rule.</span></span>
1. <span data-ttu-id="5626d-148">Laukā **Nosaukums** ievadiet **noklusējuma**.</span><span class="sxs-lookup"><span data-stu-id="5626d-148">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="5626d-149">Laukā **Pieņemtais protokols** atlasiet **HTTP un HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="5626d-149">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="5626d-150">Laukā **Priekšgala resursdatori** ievadiet **dynamics-ecom-tenant-name.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="5626d-150">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="5626d-151">Zem **Modeļi saskaņošanai** augšējā laukā ievadiet **/\***.</span><span class="sxs-lookup"><span data-stu-id="5626d-151">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="5626d-152">Sadaļā **Maršruta dati** iestatiet opciju **Maršruta tips** uz **Pārsūtīt**.</span><span class="sxs-lookup"><span data-stu-id="5626d-152">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="5626d-153">Laukā **Aizmugursistēmas kopa** atlasiet **e-komercijas aizmugursistēma**.</span><span class="sxs-lookup"><span data-stu-id="5626d-153">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="5626d-154">**Pārsūtīšanas protokola** lauka grupā atlasiet opciju **Saskaņot pieprasījumu**.</span><span class="sxs-lookup"><span data-stu-id="5626d-154">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="5626d-155">Iestatiet opciju **URL pārrakstīšana** uz **Atspējots**.</span><span class="sxs-lookup"><span data-stu-id="5626d-155">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="5626d-156">Iestatiet opciju **Saglabāšana kešatmiņā** uz **Atspējots**.</span><span class="sxs-lookup"><span data-stu-id="5626d-156">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="5626d-157">Lai iestatītu kešošanas kārtulu Azure optimālās ieejas pakalpojumā, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="5626d-157">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="5626d-158">Pievienojiet kešošanas kārtulu.</span><span class="sxs-lookup"><span data-stu-id="5626d-158">Add a caching rule.</span></span>
1. <span data-ttu-id="5626d-159">Laukā **Nosaukums** ievadiet **statika**.</span><span class="sxs-lookup"><span data-stu-id="5626d-159">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="5626d-160">Laukā **Pieņemtais protokols** atlasiet **HTTP un HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="5626d-160">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="5626d-161">Laukā **Priekšgala resursdatori** ievadiet **dynamics-ecom-tenant-name.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="5626d-161">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="5626d-162">Zem **Modeļi saskaņošanai**, augšējā laukā, **/\_msdyn365/\_scnr/\***.</span><span class="sxs-lookup"><span data-stu-id="5626d-162">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="5626d-163">Sadaļā **Maršruta dati** iestatiet opciju **Maršruta tips** uz **Pārsūtīt**.</span><span class="sxs-lookup"><span data-stu-id="5626d-163">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="5626d-164">Laukā **Aizmugursistēmas kopa** atlasiet **e-komercijas aizmugursistēma**.</span><span class="sxs-lookup"><span data-stu-id="5626d-164">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="5626d-165">**Pārsūtīšanas protokola** lauka grupā atlasiet opciju **Saskaņot pieprasījumu**.</span><span class="sxs-lookup"><span data-stu-id="5626d-165">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="5626d-166">Iestatiet opciju **URL pārrakstīšana** uz **Atspējots**.</span><span class="sxs-lookup"><span data-stu-id="5626d-166">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="5626d-167">Iestatiet opciju **Saglabāšana kešatmiņā** uz **Atspējots**.</span><span class="sxs-lookup"><span data-stu-id="5626d-167">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="5626d-168">Laukā **Vaicājuma virknes kešošanas uzvedība** atlasiet **Saglabāt kešatmiņā katru unikālo vietrādi URL**.</span><span class="sxs-lookup"><span data-stu-id="5626d-168">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="5626d-169">**Dinamiskās saspiešanas** lauka grupā atlasiet opciju **Iespējots**.</span><span class="sxs-lookup"><span data-stu-id="5626d-169">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="5626d-170">Šajā attēlā redzams dialoglodziņš **Pievienot kārtulu** Azure optimālās ieejas pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="5626d-170">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![Dialoglodziņš Kārtulas pievienošana](./media/CDN_CachingRule.png)

> [!WARNING]
> <span data-ttu-id="5626d-172">Ja domēns, ko izmantosiet, jau ir aktīvs un dzīvs, izveidojiet atbalsta biļeti no **Atbalsta** elementa, kas atrodas [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/), lai saņemtu palīdzību nākamajiem soļiem.</span><span class="sxs-lookup"><span data-stu-id="5626d-172">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="5626d-173">Papildinformāciju skatiet sadaļā [Iegūt atbalstu Finance and Operations programmām vai Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="5626d-173">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="5626d-174">Ja jūsu domēns ir jauns un nav jau esošs domēns, varat pievienot pielāgotu domēnu Azure optimālās ieejas pakalpojuma konfigurācijai.</span><span class="sxs-lookup"><span data-stu-id="5626d-174">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="5626d-175">Tas ļaus tīmekļa datplūsmu vadīt tieši uz jūsu vietni, izmantojot Azure optimālās ieejas instanci.</span><span class="sxs-lookup"><span data-stu-id="5626d-175">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="5626d-176">Lai pievienotu pielāgotu domēnu (piemēram, `www.fabrikam.com`), jums ir jākonfigurē Kanoniskais nosaukums (CNAME) domēnam.</span><span class="sxs-lookup"><span data-stu-id="5626d-176">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="5626d-177">Šajā attēlā redzams dialoglodziņš **CNAME konfigurācija** Azure optimālās ieejas pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="5626d-177">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![CNAME konfigurācijas dialoglodziņš](./media/CNAME_Configuration.png)

<span data-ttu-id="5626d-179">Varat izmantot Azure optimālās ieejas pakalpojumu, lai pārvaldītu sertifikātu, vai arī varat izmantot savu sertifikātu pielāgotajam domēnam.</span><span class="sxs-lookup"><span data-stu-id="5626d-179">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="5626d-180">Šajā attēlā redzams dialoglodziņš **Pielāgota domēna HTTPS** Azure optimālās ieejas pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="5626d-180">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Pielāgota domēna HTTPS dialoglodziņš](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="5626d-182">Lai iegūtu detalizētas instrukcijas par pielāgota domēna pievienošanu Azure optimālās ieejas pakalpojumu, skatiet sadaļu [Pievienot pielāgotu domēnu jūsu optimālās ieejas pakalpojumam](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="5626d-182">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="5626d-183">Tagad jūsu CDN ir jābūt pareizi konfigurētam, lai to varētu izmantot kopā ar jūsu Komercijas vietni.</span><span class="sxs-lookup"><span data-stu-id="5626d-183">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5626d-184">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="5626d-184">Additional resources</span></span>

[<span data-ttu-id="5626d-185">Satura piegādes tīkla ieviešanas opcijas</span><span class="sxs-lookup"><span data-stu-id="5626d-185">Content delivery network implementation options</span></span>](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
