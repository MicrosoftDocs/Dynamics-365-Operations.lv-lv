---
title: Atbalsta pievienošana satura piegādes tīklam (CDN)
description: Šajā tēmā ir aprakstīts, kā pievienot satura piegādes tīklu (CDN) jūsu Microsoft Dynamics 365 Commerce videi.
author: brianshook
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bf5a0da2803f985e6c0c04dd9916977397173d11
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001626"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="9fc48-103">Atbalsta pievienošana satura piegādes tīklam (CDN)</span><span class="sxs-lookup"><span data-stu-id="9fc48-103">Add support for a content delivery network (CDN)</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9fc48-104">Šajā tēmā ir aprakstīts, kā pievienot satura piegādes tīklu (CDN) jūsu Microsoft Dynamics 365 Commerce videi.</span><span class="sxs-lookup"><span data-stu-id="9fc48-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="9fc48-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="9fc48-105">Overview</span></span>

<span data-ttu-id="9fc48-106">Iestatot e-komercijas vidi programmā Dynamics 365 Commerce, varat konfigurēt to, lai varētu strādāt ar savu CDN pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="9fc48-106">When you set up an e-Commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="9fc48-107">Jūsu pielāgoto domēnu var iespējot jūsu E-komercijas vides nodrošināšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="9fc48-107">Your custom domain can be enabled during the provisioning process for your e-Commerce environment.</span></span> <span data-ttu-id="9fc48-108">Alternatīvi varat izmantot pakalpojuma pieprasījumu, lai to iestatītu pēc nodrošināšanas procesa pabeigšanas.</span><span class="sxs-lookup"><span data-stu-id="9fc48-108">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="9fc48-109">E-komercijas vides nodrošināšanas process ģenerē resursdatora nosaukumu, kas ir saistīts ar vidi.</span><span class="sxs-lookup"><span data-stu-id="9fc48-109">The provisioning process for the e-Commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="9fc48-110">Šim resursdatora nosaukumam ir šāds formāts, kur *e-komercijas nomnieka nosaukums* ir jūsu vides nosaukums.</span><span class="sxs-lookup"><span data-stu-id="9fc48-110">This host name has the following format, where *e-commerce-tenant-name* is the name of your environment:</span></span>

<span data-ttu-id="9fc48-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="9fc48-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="9fc48-112">Resursdatora nosaukums vai galapunkts, kas tiek ģenerēts nodrošināšanas procesā, atbalsta drošligzdu slāņa (SSL) sertifikātu tikai \*. commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="9fc48-112">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="9fc48-113">Tas neatbalsta SSL pielāgotiem domēniem.</span><span class="sxs-lookup"><span data-stu-id="9fc48-113">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="9fc48-114">Tāpēc jums ir jāpārtrauc SSL pielāgotiem domēniem savā CDN un jāpārsūta datplūsma no CDN uz resursdatora nosaukumu vai galapunktu, ko Komercija ir ģenerējusi.</span><span class="sxs-lookup"><span data-stu-id="9fc48-114">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="9fc48-115">Turklāt *statika* (JavaScript vai kaskādes stila lapu \[CSS\]faili) no Komercijas tiek nodrošināti no Komercijas ģenerētā galapunkta (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="9fc48-115">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="9fc48-116">Statiku var saglabāt kešatmiņā tikai tad, ja resursdatora nosaukums vai galapunkts, ko ģenerējusi Komercija, tiek novietots pēc CDN.</span><span class="sxs-lookup"><span data-stu-id="9fc48-116">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="9fc48-117">SSL iestatīšana</span><span class="sxs-lookup"><span data-stu-id="9fc48-117">Set up SSL</span></span>

<span data-ttu-id="9fc48-118">Lai palīdzētu nodrošināt, ka SSL ir iestatīts un ka statika saglabāta kešatmiņā, jums ir jākonfigurē savs CDN, lai tas būtu saistīts ar resursdatora nosaukumu, ko ģenerēja Komercija jūsu videi.</span><span class="sxs-lookup"><span data-stu-id="9fc48-118">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="9fc48-119">Sekojošais modelis ir arī jāsaglabā kešatmiņā tikai statikai.</span><span class="sxs-lookup"><span data-stu-id="9fc48-119">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="9fc48-120">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="9fc48-120">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="9fc48-121">Pēc tam, kad jūs sniedzat savu Komercijas vidi kopā ar sniegto pielāgoto domēnu, vai pēc tam, kad jūs nodrošināt pielāgotu domēnu jūsu videi, izmantojot pakalpojuma pieprasījumu, norādiet savu pielāgoto domēnu resursdatora nosaukumam vai galapunktam, ko ģenerējusi Komercija.</span><span class="sxs-lookup"><span data-stu-id="9fc48-121">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="9fc48-122">Kā iepriekš tika minēts, ģenerētais resursdatora nosaukums vai galapunkts atbalsta SSL sertifikātu tikai attiecībā uz \*. commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="9fc48-122">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="9fc48-123">Tas neatbalsta SSL pielāgotiem domēniem.</span><span class="sxs-lookup"><span data-stu-id="9fc48-123">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="9fc48-124">CDN pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="9fc48-124">CDN services</span></span>

<span data-ttu-id="9fc48-125">Jebkuru CDN pakalpojumu var izmantot ar Komercijas vidi.</span><span class="sxs-lookup"><span data-stu-id="9fc48-125">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="9fc48-126">Tālāk ir sniegti divi piemēri.</span><span class="sxs-lookup"><span data-stu-id="9fc48-126">Here are two examples:</span></span>

- <span data-ttu-id="9fc48-127">**Microsoft Azure optimālās ieejas pakalpojums** — Azure CDN risinājums.</span><span class="sxs-lookup"><span data-stu-id="9fc48-127">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="9fc48-128">Papildinformāciju par Azure optimālās ieejas pakalpojumu skatiet tēmā [Azure optimālās ieejas pakalpojuma dokumentācija](https://docs.microsoft.com/azure/frontdoor/)</span><span class="sxs-lookup"><span data-stu-id="9fc48-128">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="9fc48-129">**Akamai dinamisks vietnes paātrinātājs** – papildinformāciju skatiet tēmā [Dinamisks vietnes paātrinātājs](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="9fc48-129">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="9fc48-130">CDN iestatīšana</span><span class="sxs-lookup"><span data-stu-id="9fc48-130">CDN setup</span></span>

<span data-ttu-id="9fc48-131">CDN iestatīšanas process sastāv no šīm vispārīgajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="9fc48-131">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="9fc48-132">Pievienojiet priekšgala resursdatoru.</span><span class="sxs-lookup"><span data-stu-id="9fc48-132">Add a front-end host.</span></span>
1. <span data-ttu-id="9fc48-133">Konfigurējiet aizmugursistēmas kopu.</span><span class="sxs-lookup"><span data-stu-id="9fc48-133">Configure a back-end pool.</span></span>
1. <span data-ttu-id="9fc48-134">Iestatiet kārtulas maršrutēšanai un saglabāšanai kešatmiņā.</span><span class="sxs-lookup"><span data-stu-id="9fc48-134">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="9fc48-135">Priekšgala resursdatora pievienošana</span><span class="sxs-lookup"><span data-stu-id="9fc48-135">Add a front-end host</span></span>

<span data-ttu-id="9fc48-136">Jebkuru CDN pakalpojumu var izmantot, bet, piemēram, šajā tēmā tiek izmantots Azure optimālās ieejas pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="9fc48-136">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="9fc48-137">Lai iegūtu informāciju par to, kā iestatīt Azure optimālās ieejas pakalpojumu, skatiet tēmu [Īsa pamācība: izveidojiet optimālo ieeju augstas pieejamības globālai tīmekļa lietojumprogrammai](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="9fc48-137">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a><span data-ttu-id="9fc48-138">Aizmugursistēmas kopas konfigurēšana Azure optimālās ieejas pakalpojumā</span><span class="sxs-lookup"><span data-stu-id="9fc48-138">Configure a back-end pool in Azure Front Door Service</span></span>

<span data-ttu-id="9fc48-139">Lai konfigurētu aizmugursistēmas kopu Azure optimālās ieejas pakalpojumā, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="9fc48-139">To configure a back-end pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="9fc48-140">Pievienojiet **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** aizmugursistēmas kopai kā pielāgotu resursdatoru, kam ir tukšs aizmugursistēmas resursdatora virsraksts.</span><span class="sxs-lookup"><span data-stu-id="9fc48-140">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a back-end pool as a custom host that has an empty back-end host header.</span></span>
1. <span data-ttu-id="9fc48-141">Zem **Darbspējas zondes** laukā **Ceļš** ievadiet **/keepalive**.</span><span class="sxs-lookup"><span data-stu-id="9fc48-141">Under **Health probes**, in the **Path** field, enter **/keepalive**.</span></span>
1. <span data-ttu-id="9fc48-142">Laukā **Intervāli (sekundes)** ievadiet **255**.</span><span class="sxs-lookup"><span data-stu-id="9fc48-142">In the **Intervals (seconds)** field, enter **255**.</span></span>
1. <span data-ttu-id="9fc48-143">Zem **Slodzes līdzsvarošana** atstājiet noklusējuma vērtības.</span><span class="sxs-lookup"><span data-stu-id="9fc48-143">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="9fc48-144">Šajā attēlā redzams dialoglodziņš **Pievienot aizmugursistēmas kopu** Azure optimālās ieejas pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="9fc48-144">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service.</span></span>

![Pievienot aizmugursistēmas kopas dialoglodziņu](./media/CDN_BackendPool.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="9fc48-146">Kārtulu iestatīšāna Azure optimālās ieejas pakalpojumā</span><span class="sxs-lookup"><span data-stu-id="9fc48-146">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="9fc48-147">Lai uzstādītu maršrutēšanas kārtulu Azure optimālās ieejas pakalpojumā, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="9fc48-147">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="9fc48-148">Pievienojiet maršrutēšanas kārtulu.</span><span class="sxs-lookup"><span data-stu-id="9fc48-148">Add a routing rule.</span></span>
1. <span data-ttu-id="9fc48-149">Laukā **Nosaukums** ievadiet **noklusējuma**.</span><span class="sxs-lookup"><span data-stu-id="9fc48-149">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="9fc48-150">Laukā **Pieņemtais protokols** atlasiet **HTTP un HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="9fc48-150">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="9fc48-151">Laukā **Priekšgala resursdatori** ievadiet **dynamics-ecom-tenant-name.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="9fc48-151">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="9fc48-152">Zem **Modeļi saskaņošanai**augšējā laukā ievadiet **/\***.</span><span class="sxs-lookup"><span data-stu-id="9fc48-152">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="9fc48-153">Sadaļā **Maršruta dati** iestatiet opciju **Maršruta tips** uz **Pārsūtīt**.</span><span class="sxs-lookup"><span data-stu-id="9fc48-153">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="9fc48-154">Laukā **Aizmugursistēmas kopa** atlasiet **e-komercijas aizmugursistēma**.</span><span class="sxs-lookup"><span data-stu-id="9fc48-154">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="9fc48-155">**Pārsūtīšanas protokola** lauka grupā atlasiet opciju **Saskaņot pieprasījumu**.</span><span class="sxs-lookup"><span data-stu-id="9fc48-155">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="9fc48-156">Iestatiet opciju **URL pārrakstīšana** uz **Atspējots**.</span><span class="sxs-lookup"><span data-stu-id="9fc48-156">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="9fc48-157">Iestatiet opciju **Saglabāšana kešatmiņā** uz **Atspējots**.</span><span class="sxs-lookup"><span data-stu-id="9fc48-157">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="9fc48-158">Lai iestatītu kešošanas kārtulu Azure optimālās ieejas pakalpojumā, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="9fc48-158">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="9fc48-159">Pievienojiet kešošanas kārtulu.</span><span class="sxs-lookup"><span data-stu-id="9fc48-159">Add a caching rule.</span></span>
1. <span data-ttu-id="9fc48-160">Laukā **Nosaukums** ievadiet **statika**.</span><span class="sxs-lookup"><span data-stu-id="9fc48-160">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="9fc48-161">Laukā **Pieņemtais protokols** atlasiet **HTTP un HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="9fc48-161">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="9fc48-162">Laukā **Priekšgala resursdatori** ievadiet **dynamics-ecom-tenant-name.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="9fc48-162">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="9fc48-163">Zem **Modeļi saskaņošanai**, augšējā laukā, **/\_msdyn365/\_scnr/\***.</span><span class="sxs-lookup"><span data-stu-id="9fc48-163">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="9fc48-164">Sadaļā **Maršruta dati** iestatiet opciju **Maršruta tips** uz **Pārsūtīt**.</span><span class="sxs-lookup"><span data-stu-id="9fc48-164">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="9fc48-165">Laukā **Aizmugursistēmas kopa** atlasiet **e-komercijas aizmugursistēma**.</span><span class="sxs-lookup"><span data-stu-id="9fc48-165">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="9fc48-166">**Pārsūtīšanas protokola** lauka grupā atlasiet opciju **Saskaņot pieprasījumu**.</span><span class="sxs-lookup"><span data-stu-id="9fc48-166">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="9fc48-167">Iestatiet opciju **URL pārrakstīšana** uz **Atspējots**.</span><span class="sxs-lookup"><span data-stu-id="9fc48-167">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="9fc48-168">Iestatiet opciju **Saglabāšana kešatmiņā** uz **Atspējots**.</span><span class="sxs-lookup"><span data-stu-id="9fc48-168">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="9fc48-169">Laukā **Vaicājuma virknes kešošanas uzvedība** atlasiet **Saglabāt kešatmiņā katru unikālo vietrādi URL**.</span><span class="sxs-lookup"><span data-stu-id="9fc48-169">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="9fc48-170">**Dinamiskās saspiešanas** lauka grupā atlasiet opciju **Iespējots**.</span><span class="sxs-lookup"><span data-stu-id="9fc48-170">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="9fc48-171">Šajā attēlā redzams dialoglodziņš **Pievienot kārtulu** Azure optimālās ieejas pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="9fc48-171">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![Dialoglodziņš Kārtulas pievienošana](./media/CDN_CachingRule.png)

<span data-ttu-id="9fc48-173">Pēc šīs sākotnējās konfigurācijas izvietošanas ir jāpievieno jūsu pielāgots domēns Azure optimālās ieejas pakalpojuma konfigurācijai.</span><span class="sxs-lookup"><span data-stu-id="9fc48-173">After this initial configuration is deployed, you must add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="9fc48-174">Lai pievienotu pielāgotu domēnu (piemēram, `www.fabrikam.com`), jums ir jākonfigurē Kanoniskais nosaukums (CNAME) domēnam.</span><span class="sxs-lookup"><span data-stu-id="9fc48-174">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="9fc48-175">Šajā attēlā redzams dialoglodziņš **CNAME konfigurācija** Azure optimālās ieejas pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="9fc48-175">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![CNAME konfigurācijas dialoglodziņš](./media/CNAME_Configuration.png)

> [!NOTE]
> <span data-ttu-id="9fc48-177">Ja domēns, ko izmantosiet, jau ir aktīvs un izmantots, sazinieties ar atbalsta dienestu, lai iespējotu šo domēnu, izmantojot Azure optimālās ieejas pakalpojumu testa iestatīšanai.</span><span class="sxs-lookup"><span data-stu-id="9fc48-177">If the domain that you will use is already active and live, contact support to enable this domain with Azure Front Door Service to set up a test.</span></span>

<span data-ttu-id="9fc48-178">Varat izmantot Azure optimālās ieejas pakalpojumu, lai pārvaldītu sertifikātu, vai arī varat izmantot savu sertifikātu pielāgotajam domēnam.</span><span class="sxs-lookup"><span data-stu-id="9fc48-178">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="9fc48-179">Šajā attēlā redzams dialoglodziņš **Pielāgota domēna HTTPS** Azure optimālās ieejas pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="9fc48-179">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Pielāgota domēna HTTPS dialoglodziņš](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="9fc48-181">Tagad jūsu CDN ir jābūt pareizi konfigurētam, lai to varētu izmantot kopā ar jūsu Komercijas vietni.</span><span class="sxs-lookup"><span data-stu-id="9fc48-181">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9fc48-182">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="9fc48-182">Additional resources</span></span>

[<span data-ttu-id="9fc48-183">Domēna nosaukuma konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="9fc48-183">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="9fc48-184">Jaunas e-komercijas vietnes izvietošana</span><span class="sxs-lookup"><span data-stu-id="9fc48-184">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="9fc48-185">E-komercijas vietnes izveide</span><span class="sxs-lookup"><span data-stu-id="9fc48-185">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="9fc48-186">Tiešsaistes vietnes saistīšana ar kanālu</span><span class="sxs-lookup"><span data-stu-id="9fc48-186">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="9fc48-187">Failu robots.txt pārvaldība</span><span class="sxs-lookup"><span data-stu-id="9fc48-187">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="9fc48-188">Pielāgotu lapu iestatīšana lietotāja pieteikumiem</span><span class="sxs-lookup"><span data-stu-id="9fc48-188">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="9fc48-189">Veikala noteikšanas iespējošana pēc atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="9fc48-189">Enable location-based store detection</span></span>](enable-store-detection.md)
