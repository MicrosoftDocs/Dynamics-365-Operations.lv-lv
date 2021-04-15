---
title: Sociālās koplietošanas modulis
description: Šajā tēmā tiek stāstīts par sociālās koplietošanas moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: c34410a8c817de9fed350bf2cd2dd918a37c230f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795361"
---
# <a name="social-share-module"></a><span data-ttu-id="596df-103">Sociālo tīklu dalīšanās modulis</span><span class="sxs-lookup"><span data-stu-id="596df-103">Social share module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="596df-104">Šajā tēmā tiek stāstīts par sociālās koplietošanas moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="596df-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="596df-105">Sociālās koplietošanas moduļi ļauj lietotājiem koplietot e-komercijas vietnes lapas vietrāžus URL tādos sociālos plašsaziņas līdzekļos kā Facebook, Twitter, Pinterest un LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="596df-105">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="596df-106">Vietnes lapas vietrāžus URL var koplietot arī pa e-pastu.</span><span class="sxs-lookup"><span data-stu-id="596df-106">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="596df-107">Sociālās koplietošanas moduļi bieži tiek izmantoti preču informācijas lapās (PDPs), lai palīdzētu lietotājiem koplietot produktu informāciju.</span><span class="sxs-lookup"><span data-stu-id="596df-107">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="596df-108">Katrs sociālās koplietošanas modulis ir konteiners sociālās koplietošanas krājumu moduļiem.</span><span class="sxs-lookup"><span data-stu-id="596df-108">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="596df-109">Katru sociālās koplietošanas krājuma moduli var konfigurēt, lai norādītu uz noteiktu sociālo plašsaziņas līdzekļu vietni.</span><span class="sxs-lookup"><span data-stu-id="596df-109">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="596df-110">Integrācija ar Facebook, Twitter, Pinterest, LinkedIn un e-pastu tiek atbalstīta ārpus lodziņa.</span><span class="sxs-lookup"><span data-stu-id="596df-110">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="596df-111">Kad vietnes lietotājs atlasa sociālā plašsaziņas līdzekļa simbolu, attiecīgajai sociālo mediju vietnei tiek palaists HTML iFrame.</span><span class="sxs-lookup"><span data-stu-id="596df-111">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="596df-112">Programmā iFrame lietotājs var pierakstīties un publicēt apskatīto lapas saturu.</span><span class="sxs-lookup"><span data-stu-id="596df-112">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="596df-113">Katra sociālo mediju platforma var izsekot sīkfailus, tāpēc šim modulim ir nepieciešams, lai vietnes lietotāji pieņemtu sīkfailu piekrišanas paziņojuma ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="596df-113">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="596df-114">Ja sīkfailu piekrišana nav pieņemta, modulis lapā tiks paslēpts.</span><span class="sxs-lookup"><span data-stu-id="596df-114">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="596df-115">Lai iegūtu papildinformāciju, skatiet [Sīkfailu piekrišana](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="596df-115">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="596df-116">Sekojošajā attēlā ir parādīts sociālās koplietošanas moduļa piemērs, kas tiek izmantots preces informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="596df-116">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![Sociālās koplietošanas moduļa piemērs](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="596df-118">Sociālās koplietošanas moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="596df-118">Social share module properties</span></span>

| <span data-ttu-id="596df-119">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="596df-119">Property name</span></span>             | <span data-ttu-id="596df-120">Vērtība</span><span class="sxs-lookup"><span data-stu-id="596df-120">Value</span></span>                 | <span data-ttu-id="596df-121">Apraksts</span><span class="sxs-lookup"><span data-stu-id="596df-121">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="596df-122">Paraksts</span><span class="sxs-lookup"><span data-stu-id="596df-122">Caption</span></span>                  | <span data-ttu-id="596df-123">Teksts</span><span class="sxs-lookup"><span data-stu-id="596df-123">Text</span></span> | <span data-ttu-id="596df-124">Šis rekvizīts norāda moduļa parakstu.</span><span class="sxs-lookup"><span data-stu-id="596df-124">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="596df-125">Orientācija</span><span class="sxs-lookup"><span data-stu-id="596df-125">Orientation</span></span> | <span data-ttu-id="596df-126">**Horizontāli** vai **Vertikāli**</span><span class="sxs-lookup"><span data-stu-id="596df-126">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="596df-127">Šis rekvizīts nosaka sociālo mediju vienumu izkārtojuma orientāciju.</span><span class="sxs-lookup"><span data-stu-id="596df-127">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="596df-128">Sociālās koplietošanas vienuma moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="596df-128">Social share item module properties</span></span>
| <span data-ttu-id="596df-129">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="596df-129">Property name</span></span>             | <span data-ttu-id="596df-130">Vērtība</span><span class="sxs-lookup"><span data-stu-id="596df-130">Value</span></span>                 | <span data-ttu-id="596df-131">Apraksts</span><span class="sxs-lookup"><span data-stu-id="596df-131">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="596df-132">Sociālie mediji</span><span class="sxs-lookup"><span data-stu-id="596df-132">Social media</span></span>              | <span data-ttu-id="596df-133">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span><span class="sxs-lookup"><span data-stu-id="596df-133">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span></span> | <span data-ttu-id="596df-134">Nolaižamā izvēlne ar sociālo mediju platformu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="596df-134">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="596df-135">Icon</span><span class="sxs-lookup"><span data-stu-id="596df-135">Icon</span></span> |<span data-ttu-id="596df-136">Attēls</span><span class="sxs-lookup"><span data-stu-id="596df-136">Image</span></span>    | <span data-ttu-id="596df-137">Tas būs attēls, kas tiks rādīta attiecīgajiem sociālajiem medijiem.</span><span class="sxs-lookup"><span data-stu-id="596df-137">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="596df-138">Lai iegūtu ieteicamo attēlu, ko izmantot katrai platformai, skatiet sociālo mediju platformas SDK.</span><span class="sxs-lookup"><span data-stu-id="596df-138">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="596df-139">Sociālās koplietošanas moduļa pievienošana pirkšanas lodziņa modulim</span><span class="sxs-lookup"><span data-stu-id="596df-139">Add a social share module to a buy box module</span></span>

<span data-ttu-id="596df-140">Lai pirkšanas lodziņa modulim pievienotu sociālās koplietošanas moduli, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="596df-140">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="596df-141">Vietnē Fabrikam atlasiet **Lapas** un pēc tam atlasiet lapu **DefaultPDP**, lai atvērtu informāciju par preču lapu.</span><span class="sxs-lookup"><span data-stu-id="596df-141">In the Fabrikam site, select **Pages**, and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="596df-142">Slotā **Buybox (obligāti)** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="596df-142">In the **Buybox (required)** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="596df-143">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Sociālā koplietošana** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="596df-143">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="596df-144">Slotā **Sociālā koplietošana** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="596df-144">In the **Social Share** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="596df-145">Dialoglodziņā **Pievienot moduli** atlasiet moduli **SocialShare** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="596df-145">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="596df-146">Moduļa **SocialShare** rekvizītu rūtī, sadaļā **Orientācija** atlasiet **Horizontāli**.</span><span class="sxs-lookup"><span data-stu-id="596df-146">In the properties pane of the **SocialShare** module, under **Orientation**, select **Horizontal**.</span></span> <span data-ttu-id="596df-147">Pēc nepieciešamības, pievienojiet parakstu.</span><span class="sxs-lookup"><span data-stu-id="596df-147">Add a caption as needed.</span></span>
1. <span data-ttu-id="596df-148">Slotā **SocialShare** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="596df-148">In the **SocialShare** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="596df-149">Dialoglodziņā **Pievienot moduli** atlasiet moduli **SocialShareItem** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="596df-149">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="596df-150">Moduļa **SocialShareItem** rekvizītu rūtī, sadaļā **Sociālie mediji** atlasiet **Facebook**.</span><span class="sxs-lookup"><span data-stu-id="596df-150">In the properties pane of the **SocialShareItem** module, under **Social Media**, select **Facebook**.</span></span>
1. <span data-ttu-id="596df-151">Moduļa **SocialShareItem** rekvizītu rūtī, sadaļā **Ikona** atlasiet **+ Pievienot attēlu**.</span><span class="sxs-lookup"><span data-stu-id="596df-151">In the properties pane of the **SocialShareItem** module, under **Icon**, select **+ Add an image**.</span></span>
1. <span data-ttu-id="596df-152">Dialoglodziņā **Multivides atlasītājs** atlasiet logotipa attēlu Facebook un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="596df-152">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="596df-153">Ja nav Facebook logotipa attēla, atlasiet **Augšupielādēt jaunu multivides vienumu**, lai augšupielādētu šo vienumu.</span><span class="sxs-lookup"><span data-stu-id="596df-153">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="596df-154">Pēc nepieciešamības pievienojiet un konfigurējiet papildu **SocialShareItem** moduļus.</span><span class="sxs-lookup"><span data-stu-id="596df-154">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="596df-155">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="596df-155">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="596df-156">Lapā tiks parādīts sociālās koplietošanas modulis.</span><span class="sxs-lookup"><span data-stu-id="596df-156">The page will show the social share module.</span></span>
1. <span data-ttu-id="596df-157">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="596df-157">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="596df-158">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="596df-158">Additional resources</span></span>

[<span data-ttu-id="596df-159">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="596df-159">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="596df-160">Pirkšanas lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="596df-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="596df-161">Sīkfailu atbilstība</span><span class="sxs-lookup"><span data-stu-id="596df-161">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]