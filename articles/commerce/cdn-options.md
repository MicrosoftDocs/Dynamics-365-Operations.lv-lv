---
title: Satura pieg'ades tīkla ieviešanas opcijas
description: Šajā tēmā pārskatītas dažādas opcijas satura piegādes tīkla (CDN) ieviešanai, kuru var izmantot ar Microsoft Dynamics 365 Commerce vidēm. Šīs opcijas ietver vietējās, Commerce nodrošinātās Azure Front Door instances un klientam piederošās Azure Front Door instances.
author: BrianShook
manager: AnnBe
ms.date: 03/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ae0769b7e19f80244186c51454444c499c5e497f
ms.sourcegitcommit: 3fe4d9a33447aa8a62d704fbbf18aeb9cb667baa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/12/2021
ms.locfileid: "5582807"
---
# <a name="content-delivery-network-implementation-options"></a><span data-ttu-id="f471a-104">Satura pieg'ades tīkla ieviešanas opcijas</span><span class="sxs-lookup"><span data-stu-id="f471a-104">Content delivery network implementation options</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f471a-105">Šajā tēmā pārskatītas dažādas opcijas satura piegādes tīkla (CDN) ieviešanai, kuru var izmantot ar Microsoft Dynamics 365 Commerce vidēm.</span><span class="sxs-lookup"><span data-stu-id="f471a-105">This topic reviews the different options for content delivery network (CDN) implementation that can be used with Microsoft Dynamics 365 Commerce environments.</span></span> <span data-ttu-id="f471a-106">Šīs opcijas ietver vietējās, Commerce nodrošinātās Azure Front Door instances un klientam piederošās Azure Front Door instances.</span><span class="sxs-lookup"><span data-stu-id="f471a-106">These options include native, Commerce-provided instances of Azure Front Door and customer-owned instances of Azure Front Door.</span></span>

<span data-ttu-id="f471a-107">Commerce klientiem ir vairākas opcijas, kad viņi lemj, kuru CDN pakalpojumu izmantot savā Commerce vidē.</span><span class="sxs-lookup"><span data-stu-id="f471a-107">Commerce customers have several options when they are considering which CDN service to use with their Commerce environment.</span></span> <span data-ttu-id="f471a-108">Commerce tiek izlaista ar Azure Front Door pamata atbalstu, kas ietver pamata mitināšanu un pielāgoto domēnu prasības.</span><span class="sxs-lookup"><span data-stu-id="f471a-108">Commerce is released with basic Azure Front Door support that covers basic hosting and custom domain requirements.</span></span> <span data-ttu-id="f471a-109">Uzņēmumiem, kuri vēlas vairāk kontroles un konkrētākas drošības iespējas, piemēram, tīmekļa lietojumprogrammas ugunsmūri (WAF), vislabāk varētu būt lietot vai nu klientam piederošu Azure Front Door instanci vai ārēju CDN pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="f471a-109">For companies that want more control and more specific security abilities, such as a web application firewall (WAF), the best option might be to use either a customer-owned instance of Azure Front Door or an external CDN service.</span></span>

<span data-ttu-id="f471a-110">Ar Commerce vidēm var izmantot šādas trīs CDN ieviešanas opcijas:</span><span class="sxs-lookup"><span data-stu-id="f471a-110">The following three CDN implementation options can be used with Commerce environments:</span></span>

- <span data-ttu-id="f471a-111">Commerce nodrošināta Azure Front Door instance</span><span class="sxs-lookup"><span data-stu-id="f471a-111">The Commerce-provided instance of Azure Front Door</span></span>
- <span data-ttu-id="f471a-112">Klientam piederoša Azure Front Door instance (paaugstinātai kontrolei un papildu drošības līdzekļiem)</span><span class="sxs-lookup"><span data-stu-id="f471a-112">A customer-owned instance of Azure Front Door (for increased control and additional security features)</span></span>
- <span data-ttu-id="f471a-113">Ārējs CDN pakalpojums</span><span class="sxs-lookup"><span data-stu-id="f471a-113">An external CDN service</span></span>

<span data-ttu-id="f471a-114">Trīs CDN ieviešanas opcijas nodrošina tikai dinamisku HTML saturu no pielāgotiem domēniem.</span><span class="sxs-lookup"><span data-stu-id="f471a-114">All three CDN implementation options deliver only dynamic HTML content from custom domains.</span></span> <span data-ttu-id="f471a-115">Commerce automātiski apstrādā visus JavaScript, Stila lapu kaskadēšanu (CSS), attēlus, videoklipus un citu statisku saturu, izmantojot Microsoft pārvaldītus CDN.</span><span class="sxs-lookup"><span data-stu-id="f471a-115">Commerce automatically handles all JavaScript, Cascading Style Sheets (CSS), images, video, and other static content through Microsoft-managed CDNs.</span></span> <span data-ttu-id="f471a-116">Jūsu izvēlētā opcija nosaka pieejamās darbības iespējas, vadības iespējas un papildu drošības iespējas.</span><span class="sxs-lookup"><span data-stu-id="f471a-116">The option that you choose determines the operational capabilities, control capabilities, and additional security capabilities that are available.</span></span>

<span data-ttu-id="f471a-117">Šajā attēlā parādīts Commerce arhitektūras pārskats.</span><span class="sxs-lookup"><span data-stu-id="f471a-117">The following illustration shows an overview of the Commerce architecture.</span></span>

![Commerce arhitektūras pārskats](media/Commerce_CDN-Option_ComparisonModels.png)

<span data-ttu-id="f471a-119">Papildu informāciju par to, kā iestatīt Azure Front Door instanci savai Commerce vietnei, skatiet tēmā [CDN atbalsta pievienošana](add-cdn-support.md).</span><span class="sxs-lookup"><span data-stu-id="f471a-119">For more information about how to set up an instance of Azure Front Door for your Commerce site, see [Add CDN Support](add-cdn-support.md).</span></span>

## <a name="use-the-commerce-provided-azure-front-door-instance"></a><span data-ttu-id="f471a-120">Commerce nodrošinātas Azure Front Door instances izmantošana</span><span class="sxs-lookup"><span data-stu-id="f471a-120">Use the Commerce-provided Azure Front Door instance</span></span>

<span data-ttu-id="f471a-121">Šajā tabulā uzskaitītas Commerce nodrošinātas Azure Front Door instances lietošanas priekšrocības un trūkumi satura galapunktu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="f471a-121">The following table lists the pros and cons of using the Commerce-provided instance of Azure Front Door to manage content endpoints.</span></span>

| <span data-ttu-id="f471a-122">Priekšrocības</span><span class="sxs-lookup"><span data-stu-id="f471a-122">Pros</span></span> | <span data-ttu-id="f471a-123">Trūkumi</span><span class="sxs-lookup"><span data-stu-id="f471a-123">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="f471a-124">Instance ir iekļauta Commerce izmaksās.</span><span class="sxs-lookup"><span data-stu-id="f471a-124">The instance is included in the Commerce cost.</span></span></li><li><span data-ttu-id="f471a-125">Tā kā instanci pārvalda Commerce darba grupa, ir nepieciešama mazāka uzturēšana un ir kopīgas iestatīšanas darbības.</span><span class="sxs-lookup"><span data-stu-id="f471a-125">Because the instance is managed by the Commerce team, less maintenance is required, and there are shared setup steps.</span></span></li><li><span data-ttu-id="f471a-126">Azure viesotā infrastruktūra ir mērogojama, droša un uzticama.</span><span class="sxs-lookup"><span data-stu-id="f471a-126">The Azure-hosted infrastructure is scalable, secure, and reliable.</span></span></li><li><span data-ttu-id="f471a-127">Drošligzdu slāņa (SSL) sertifikātam ir nepieciešama vienreizēja iestatīšana, un tas tiek atjaunināts automātiski.</span><span class="sxs-lookup"><span data-stu-id="f471a-127">The Secure Sockets Layer (SSL) certificate requires a one-time setup and is automatically renewed.</span></span></li><li><span data-ttu-id="f471a-128">Instances kļūdas un novirzes no normas uzrauga Commerce darba grupa.</span><span class="sxs-lookup"><span data-stu-id="f471a-128">The instance is monitored for errors and anomalies by the Commerce team.</span></span></li></ul> | <ul><li><span data-ttu-id="f471a-129">WAF netiek atbalstīts.</span><span class="sxs-lookup"><span data-stu-id="f471a-129">A WAF isn't supported.</span></span></li><li><span data-ttu-id="f471a-130">Nav konkrētu pielāgojumu vai iestatīšanas pielāgojumu.</span><span class="sxs-lookup"><span data-stu-id="f471a-130">There are no specific customizations or setting adjustments.</span></span></li><li><span data-ttu-id="f471a-131">Instances atjauninājumi vai izmaiņas ir atkarīgas no Commerce darba grupas.</span><span class="sxs-lookup"><span data-stu-id="f471a-131">The instance depends on the Commerce team for updates or changes.</span></span></li><li><span data-ttu-id="f471a-132">Apex domēniem ir vajadzīga atsevišķa Azure Front Door instance, lai tos integrētu ar Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="f471a-132">A separate Azure Front Door instance is required for apex domains, and extra work is required to integrate apex domains with Azure DNS.</span></span></li><li><span data-ttu-id="f471a-133">Klientam netiek nodrošināta telemetrija par atbildēm sekundē (RPS) vai kļūdu rādītāju.</span><span class="sxs-lookup"><span data-stu-id="f471a-133">No telemetry about responses per second (RPS) or the error rate is provided to the customer.</span></span></li></ul> |

<span data-ttu-id="f471a-134">Šajā attēlā parādīta Commerce nodrošinātas Azure Front Door instances arhitektūra.</span><span class="sxs-lookup"><span data-stu-id="f471a-134">The following illustration shows the architecture of the Commerce-provided Azure Front Door instance.</span></span>

![Commerce nodrošinātas Azure Front Door instance](media/Commerce_CDN-Option_CommerceFrontDoor.png)

## <a name="use-a-customer-owned-azure-front-door-instance"></a><span data-ttu-id="f471a-136">Izmantojiet klientam piederošu Azure Front Door instanci</span><span class="sxs-lookup"><span data-stu-id="f471a-136">Use a customer-owned Azure Front Door instance</span></span>

<span data-ttu-id="f471a-137">Šajā tabulā uzskaitītas klientam piederošas Azure Front Door instances lietošanas priekšrocības un trūkumi satura galapunktu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="f471a-137">The following table lists the pros and cons of using a customer-owned instance of Azure Front Door to manage content endpoints.</span></span>

| <span data-ttu-id="f471a-138">Priekšrocības</span><span class="sxs-lookup"><span data-stu-id="f471a-138">Pros</span></span> | <span data-ttu-id="f471a-139">Trūkumi</span><span class="sxs-lookup"><span data-stu-id="f471a-139">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="f471a-140">Iestatīšana ir droša un viegli pārvaldāma.</span><span class="sxs-lookup"><span data-stu-id="f471a-140">Setup is secure and easy to manage.</span></span></li><li><span data-ttu-id="f471a-141">Azure viesotā infrastruktūra ir mērogojama, droša un uzticama.</span><span class="sxs-lookup"><span data-stu-id="f471a-141">The Azure-hosted infrastructure is scalable, secure, and reliable.</span></span></li><li><span data-ttu-id="f471a-142">Instance atļauj WAF intergrāciju un detalizētas kārtulas vadīklas detalizētākai drošībai, kura ir pielāgota konkrēti jūsu vietnes vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="f471a-142">The instance allows for WAF integration and granular rule controls for finer-grade security that is tuned specifically for your site.</span></span></li><li><span data-ttu-id="f471a-143">Instance nodrošina detalizētāku SSL sertifikātu vadību (kā klientiem piederošu, tā arī Azure Front Door pārvaldītu) un domēnu saistīšanu.</span><span class="sxs-lookup"><span data-stu-id="f471a-143">The instance allows for finer control of SSL certificates (both customer-owned and Azure Front Door–managed) and domain linking.</span></span></li><li><span data-ttu-id="f471a-144">Instance nodrošina Apex domēna risinājumu, ja tam tiek izveidots tiešs pāra savienojums ar Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="f471a-144">The instance offers an apex domain solution if it's paired directly with Azure DNS.</span></span></li><li><span data-ttu-id="f471a-145">Tiek nodrošināta telemetrija un brīdināšana.</span><span class="sxs-lookup"><span data-stu-id="f471a-145">Telemetry and alerting are provided.</span></span></li><li><span data-ttu-id="f471a-146">Drošligzdu slāņa (SSL) sertifikātam ir nepieciešama vienreizēja iestatīšana, un tas tiek atjaunināts automātiski.</span><span class="sxs-lookup"><span data-stu-id="f471a-146">The SSL certificate requires a one-time setup and is automatically renewed.</span></span></li></ul> | <ul><li><span data-ttu-id="f471a-147">Instance ir pašpārvaldīta.</span><span class="sxs-lookup"><span data-stu-id="f471a-147">The instance is self-managed.</span></span></li><li><span data-ttu-id="f471a-148">Ir nepieciešama sākotnējā zināšanu uzņemšana.</span><span class="sxs-lookup"><span data-stu-id="f471a-148">Initial knowledge ramp-up is required.</span></span></li></ul> |

<span data-ttu-id="f471a-149">Šajā attēlā parādīta Commerce infrastruktūra, kas ietver klientam piederošu Azure Front Door instanci.</span><span class="sxs-lookup"><span data-stu-id="f471a-149">The following illustration shows a Commerce infrastructure that includes a customer-owned Azure Front Door instance.</span></span>

![Commerce infrastruktūra, kas ietver klientam piederošu Azure Front Door instanci](media/Commerce_CDN-Option_CustomerOwnedAzureFrontDoor.png)

## <a name="use-an-external-cdn-service"></a><span data-ttu-id="f471a-151">Ārēja CDN pakalpojuma izmantošana</span><span class="sxs-lookup"><span data-stu-id="f471a-151">Use an external CDN service</span></span>

<span data-ttu-id="f471a-152">Šajā tabulā uzskaitītas ārēja CDN pakalpojuma lietošanas priekšrocības un trūkumi satura galapunktu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="f471a-152">The following table lists the pros and cons of using an external CDN service to manage content endpoints.</span></span>

| <span data-ttu-id="f471a-153">Priekšrocības</span><span class="sxs-lookup"><span data-stu-id="f471a-153">Pros</span></span> | <span data-ttu-id="f471a-154">Trūkumi</span><span class="sxs-lookup"><span data-stu-id="f471a-154">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="f471a-155">Šī opcija ir noderīga, ja esošais domēns jau tiek viesots ārējā CDN.</span><span class="sxs-lookup"><span data-stu-id="f471a-155">This option is useful when the existing domain is already hosted on an external CDN.</span></span></li><li><span data-ttu-id="f471a-156">Konkurentu CDN (piemēram, Akamai) var būt vairāk WAF iespēju.</span><span class="sxs-lookup"><span data-stu-id="f471a-156">Competitor CDNs (for example, Akamai) might have more WAF capabilities.</span></span></li></ul> | <ul><li><span data-ttu-id="f471a-157">Ir nepieciešams atsevišķs līgums un papildu izmaksas.</span><span class="sxs-lookup"><span data-stu-id="f471a-157">A separate contract and additional costing are required.</span></span></li><li><span data-ttu-id="f471a-158">SSL var radīt papildu izmaksas.</span><span class="sxs-lookup"><span data-stu-id="f471a-158">SSL might incur additional costs.</span></span></li><li><span data-ttu-id="f471a-159">Tā kā pakalpojums ir šķirts no Azure mākoņa struktūras, ir jāpārvalda papildu infrastruktūra.</span><span class="sxs-lookup"><span data-stu-id="f471a-159">Because the service is separate from the Azure cloud structure, additional infrastructure must be managed.</span></span></li><li><span data-ttu-id="f471a-160">Pakalpojumam var būt nepieciešamas ilgākas investīcijas galapunkta un drošības iestatīšanā.</span><span class="sxs-lookup"><span data-stu-id="f471a-160">The service might require longer time investments in endpoint and security setup.</span></span></li><li><span data-ttu-id="f471a-161">Pakalpojums tiek pašpārvaldīts.</span><span class="sxs-lookup"><span data-stu-id="f471a-161">The service is self-managed.</span></span></li><li><span data-ttu-id="f471a-162">Pakalpojums tiek pašuzraudzīts.</span><span class="sxs-lookup"><span data-stu-id="f471a-162">The service is self-monitored.</span></span></li></ul> |

<span data-ttu-id="f471a-163">Šajā attēlā parādīta Commerce infrastruktūra, kas ietver klientam ārēju CDN pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="f471a-163">The following illustration shows a Commerce infrastructure that includes an external CDN service.</span></span>

![Commerce infrastruktūra, kas ietver klientam ārēju CDN pakalpojumu](media/Commerce_CDN-Option_ExternalFrontDoor.png)

## <a name="additional-resources"></a><span data-ttu-id="f471a-165">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="f471a-165">Additional resources</span></span>

[<span data-ttu-id="f471a-166">Atbalsta pievienošana satura piegādes tīklam (CDN)</span><span class="sxs-lookup"><span data-stu-id="f471a-166">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
