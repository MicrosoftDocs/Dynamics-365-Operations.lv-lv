---
title: Atbalsta pievienošana satura piegādes tīklam (CDN)
description: Šajā tēmā aprakstīts, kā pievienot satura piegādes tīklu savai Microsoft Dynamics 365 Commerce videi.
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 59277323e0995f59d3a451395a038fa3708274eb
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936834"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="88d22-103">Atbalsta pievienošana satura piegādes tīklam (CDN)</span><span class="sxs-lookup"><span data-stu-id="88d22-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="88d22-104">Šajā tēmā aprakstīts, kā pievienot satura piegādes tīklu savai Microsoft Dynamics 365 Commerce videi.</span><span class="sxs-lookup"><span data-stu-id="88d22-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="88d22-105">Iestatot e-komercijas vidi programmā Dynamics 365 Commerce, varat konfigurēt to, lai varētu strādāt ar savu CDN pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="88d22-105">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="88d22-106">Jūsu pielāgoto domēnu var iespējot jūsu e-komercijas vides nodrošināšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="88d22-106">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="88d22-107">Alternatīvi varat izmantot pakalpojuma pieprasījumu, lai to iestatītu pēc nodrošināšanas procesa pabeigšanas.</span><span class="sxs-lookup"><span data-stu-id="88d22-107">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="88d22-108">E-komercijas vides nodrošināšanas process ģenerē resursdatora nosaukumu, kas ir saistīts ar vidi.</span><span class="sxs-lookup"><span data-stu-id="88d22-108">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="88d22-109">Šim resursdatora nosaukumam ir šāds formāts, kur \<*e-commerce-tenant-name*\> ir jūsu vides nosaukums.</span><span class="sxs-lookup"><span data-stu-id="88d22-109">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="88d22-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="88d22-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="88d22-111">Resursdatora nosaukums vai galapunkts, kas tiek ģenerēts nodrošināšanas procesā, atbalsta drošligzdu slāņa (SSL) sertifikātu tikai \*. commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="88d22-111">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="88d22-112">Tas neatbalsta SSL pielāgotiem domēniem.</span><span class="sxs-lookup"><span data-stu-id="88d22-112">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="88d22-113">Tāpēc jums ir jāpārtrauc SSL pielāgotiem domēniem savā CDN un jāpārsūta datplūsma no CDN uz resursdatora nosaukumu vai galapunktu, ko Komercija ir ģenerējusi.</span><span class="sxs-lookup"><span data-stu-id="88d22-113">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="88d22-114">Turklāt *statika* (JavaScript vai kaskādes stila lapu \[CSS\] faili) no Komercijas tiek nodrošināti no Komercijas ģenerētā galapunkta (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="88d22-114">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="88d22-115">Statiku var saglabāt kešatmiņā tikai tad, ja resursdatora nosaukums vai galapunkts, ko ģenerējusi Komercija, tiek novietots pēc CDN.</span><span class="sxs-lookup"><span data-stu-id="88d22-115">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="88d22-116">SSL iestatīšana</span><span class="sxs-lookup"><span data-stu-id="88d22-116">Set up SSL</span></span>

<span data-ttu-id="88d22-117">Pēc tam, kad jūs sniedzat savu Commerce vidi kopā ar sniegto pielāgoto domēnu, vai pēc tam, kad jūs nodrošināt pielāgotu domēnu jūsu videi, izmantojot pakalpojuma pieprasījumu, norādiet savu pielāgoto domēnu resursdatora nosaukumam vai galapunktam, ko ģenerēja Commerce.</span><span class="sxs-lookup"><span data-stu-id="88d22-117">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, you need to work with the Commerce onboarding team to plan the DNS changes.</span></span>

<span data-ttu-id="88d22-118">Kā iepriekš tika minēts, ģenerētais resursdatora nosaukums vai galapunkts atbalsta SSL sertifikātu tikai attiecībā uz \*. commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="88d22-118">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="88d22-119">Tas neatbalsta SSL pielāgotiem domēniem.</span><span class="sxs-lookup"><span data-stu-id="88d22-119">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="88d22-120">CDN pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="88d22-120">CDN services</span></span>

<span data-ttu-id="88d22-121">Jebkuru CDN pakalpojumu var izmantot ar Komercijas vidi.</span><span class="sxs-lookup"><span data-stu-id="88d22-121">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="88d22-122">Tālāk ir sniegti divi piemēri.</span><span class="sxs-lookup"><span data-stu-id="88d22-122">Here are two examples:</span></span>

- <span data-ttu-id="88d22-123">**Microsoft Azure optimālās ieejas pakalpojums** — Azure CDN risinājums.</span><span class="sxs-lookup"><span data-stu-id="88d22-123">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="88d22-124">Papildinformāciju par Azure optimālās ieejas pakalpojumu skatiet tēmā [Azure optimālās ieejas pakalpojuma dokumentācija](/azure/frontdoor/)</span><span class="sxs-lookup"><span data-stu-id="88d22-124">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](/azure/frontdoor/).</span></span>
- <span data-ttu-id="88d22-125">**Akamai dinamisks vietnes paātrinātājs** – papildinformāciju skatiet tēmā [Dinamisks vietnes paātrinātājs](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="88d22-125">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="88d22-126">CDN iestatīšana</span><span class="sxs-lookup"><span data-stu-id="88d22-126">CDN setup</span></span>

<span data-ttu-id="88d22-127">CDN iestatīšanas process sastāv no šīm vispārīgajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="88d22-127">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="88d22-128">Pievienojiet priekšgala resursdatoru.</span><span class="sxs-lookup"><span data-stu-id="88d22-128">Add a front-end host.</span></span>
1. <span data-ttu-id="88d22-129">Konfigurējiet aizmugursistēmas kopu.</span><span class="sxs-lookup"><span data-stu-id="88d22-129">Configure a backend pool.</span></span>
1. <span data-ttu-id="88d22-130">Maršrutēšanas noteikumu iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="88d22-130">Set up rules for routing.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="88d22-131">Priekšgala resursdatora pievienošana</span><span class="sxs-lookup"><span data-stu-id="88d22-131">Add a front-end host</span></span>

<span data-ttu-id="88d22-132">Jebkuru CDN pakalpojumu var izmantot, bet, piemēram, šajā tēmā tiek izmantots Azure optimālās ieejas pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="88d22-132">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="88d22-133">Lai iegūtu informāciju par to, kā iestatīt Azure optimālās ieejas pakalpojumu, skatiet tēmu [Īsa pamācība: izveidojiet optimālo ieeju augstas pieejamības globālai tīmekļa lietojumprogrammai](/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="88d22-133">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="88d22-134">Aizmugursistēmas kopas konfigurēšana Azure optimālās ieejas pakalpojumā</span><span class="sxs-lookup"><span data-stu-id="88d22-134">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="88d22-135">Lai konfigurētu aizmugursistēmas kopu Azure optimālās ieejas pakalpojumā, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="88d22-135">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="88d22-136">Pievienojiet **&lt;ecom-nomnieka nosaukumu&gt;.commerce.dynamics.com** servera kopai kā pielāgotu resursdatoru, kam ir servera resursdatora virsraksts, kas ir tāds pats kā **&lt;ecom-nomnieka nosaukums&gt;.commerce.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="88d22-136">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has a backend host header that is the same as **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**.</span></span>
1. <span data-ttu-id="88d22-137">Zem **Slodzes līdzsvarošana** atstājiet noklusējuma vērtības.</span><span class="sxs-lookup"><span data-stu-id="88d22-137">Under **Load balancing**, leave the default values.</span></span>
1. <span data-ttu-id="88d22-138">Deaktivēt veselības pārbaudes aizmugursistēmas kopai.</span><span class="sxs-lookup"><span data-stu-id="88d22-138">Disable health checks for the backend pool.</span></span>

<span data-ttu-id="88d22-139">Šajā attēlā redzams dialoglodziņš **Pievienot aizmugursistēmu** Azure optimālās ieejas pakalpojumā ar ievadīto aizmugursistēmas resursdatora virsrakstu.</span><span class="sxs-lookup"><span data-stu-id="88d22-139">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![Pievienot aizmugursistēmas kopas dialoglodziņu](./media/CDN_BackendPool.png)

<span data-ttu-id="88d22-141">Šajā attēlā redzams dialoglodziņš **Pievienot aizmugursistēmas kopa** Azure optimālās ieejas pakalpojumā ar noklusējuma noslodzes balansēšanas vērtībām.</span><span class="sxs-lookup"><span data-stu-id="88d22-141">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![Pievienot aizmugursistēmas kopas dialoglodziņa turpinājumu](./media/CDN_BackendPool_2.png)

> [!NOTE]
> <span data-ttu-id="88d22-143">Noteikti atspējojiet **Veselības zondes**, iestatot savu Azure Front Door pakalpojumu pakalpojumam Commerce.</span><span class="sxs-lookup"><span data-stu-id="88d22-143">Be sure to disable **Health Probes** when setting up your own Azure Front Door service for Commerce.</span></span>


### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="88d22-144">Kārtulu iestatīšāna Azure optimālās ieejas pakalpojumā</span><span class="sxs-lookup"><span data-stu-id="88d22-144">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="88d22-145">Lai uzstādītu maršrutēšanas kārtulu Azure optimālās ieejas pakalpojumā, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="88d22-145">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="88d22-146">Pievienojiet maršrutēšanas kārtulu.</span><span class="sxs-lookup"><span data-stu-id="88d22-146">Add a routing rule.</span></span>
1. <span data-ttu-id="88d22-147">Laukā **Nosaukums** ievadiet **noklusējuma**.</span><span class="sxs-lookup"><span data-stu-id="88d22-147">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="88d22-148">Laukā **Pieņemtais protokols** atlasiet **HTTP un HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="88d22-148">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="88d22-149">Laukā **Priekšgala resursdatori** ievadiet **dynamics-ecom-tenant-name.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="88d22-149">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="88d22-150">Zem **Modeļi saskaņošanai** augšējā laukā ievadiet **/\***.</span><span class="sxs-lookup"><span data-stu-id="88d22-150">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="88d22-151">Sadaļā **Maršruta dati** iestatiet opciju **Maršruta tips** uz **Pārsūtīt**.</span><span class="sxs-lookup"><span data-stu-id="88d22-151">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="88d22-152">Laukā **Aizmugursistēmas kopa** atlasiet **e-komercijas aizmugursistēma**.</span><span class="sxs-lookup"><span data-stu-id="88d22-152">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="88d22-153">**Pārsūtīšanas protokola** lauka grupā atlasiet opciju **Saskaņot pieprasījumu**.</span><span class="sxs-lookup"><span data-stu-id="88d22-153">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="88d22-154">Iestatiet opciju **URL pārrakstīšana** uz **Atspējots**.</span><span class="sxs-lookup"><span data-stu-id="88d22-154">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="88d22-155">Iestatiet opciju **Saglabāšana kešatmiņā** uz **Atspējots**.</span><span class="sxs-lookup"><span data-stu-id="88d22-155">Set the **Caching** option to **Disabled**.</span></span>


> [!WARNING]
> <span data-ttu-id="88d22-156">Ja domēns, ko izmantosiet, jau ir aktīvs un dzīvs, izveidojiet atbalsta biļeti no **Atbalsta** elementa, kas atrodas [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/), lai saņemtu palīdzību nākamajiem soļiem.</span><span class="sxs-lookup"><span data-stu-id="88d22-156">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="88d22-157">Papildinformāciju skatiet sadaļā [Iegūt atbalstu Finance and Operations programmām vai Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="88d22-157">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="88d22-158">Ja jūsu domēns ir jauns un nav jau esošs domēns, varat pievienot pielāgotu domēnu Azure optimālās ieejas pakalpojuma konfigurācijai.</span><span class="sxs-lookup"><span data-stu-id="88d22-158">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="88d22-159">Tas ļaus tīmekļa datplūsmu vadīt tieši uz jūsu vietni, izmantojot Azure optimālās ieejas instanci.</span><span class="sxs-lookup"><span data-stu-id="88d22-159">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="88d22-160">Lai pievienotu pielāgotu domēnu (piemēram, `www.fabrikam.com`), jums ir jākonfigurē Kanoniskais nosaukums (CNAME) domēnam.</span><span class="sxs-lookup"><span data-stu-id="88d22-160">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="88d22-161">Šajā attēlā redzams dialoglodziņš **CNAME konfigurācija** Azure optimālās ieejas pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="88d22-161">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![CNAME konfigurācijas dialoglodziņš](./media/CNAME_Configuration.png)

<span data-ttu-id="88d22-163">Varat izmantot Azure optimālās ieejas pakalpojumu, lai pārvaldītu sertifikātu, vai arī varat izmantot savu sertifikātu pielāgotajam domēnam.</span><span class="sxs-lookup"><span data-stu-id="88d22-163">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="88d22-164">Šajā attēlā redzams dialoglodziņš **Pielāgota domēna HTTPS** Azure optimālās ieejas pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="88d22-164">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Pielāgota domēna HTTPS dialoglodziņš](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="88d22-166">Lai iegūtu detalizētas instrukcijas par pielāgota domēna pievienošanu Azure optimālās ieejas pakalpojumu, skatiet sadaļu [Pievienot pielāgotu domēnu jūsu optimālās ieejas pakalpojumam](/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="88d22-166">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="88d22-167">Tagad jūsu CDN ir jābūt pareizi konfigurētam, lai to varētu izmantot kopā ar jūsu Komercijas vietni.</span><span class="sxs-lookup"><span data-stu-id="88d22-167">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="88d22-168">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="88d22-168">Additional resources</span></span>

[<span data-ttu-id="88d22-169">Satura piegādes tīkla ieviešanas opcijas</span><span class="sxs-lookup"><span data-stu-id="88d22-169">Content delivery network implementation options</span></span>](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]