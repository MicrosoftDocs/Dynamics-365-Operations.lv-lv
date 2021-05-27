---
title: Kartes modulis
description: Šajā tēmā ir apskatīti kartes moduļi un aprakstīts, kā tos konfigurēt programmā Microsoft Dynamics 365 Commerce.
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 659211f3a74c38389f991cd2385366d175b0c7c0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020263"
---
# <a name="map-module"></a><span data-ttu-id="e1e5e-103">Kartes modulis</span><span class="sxs-lookup"><span data-stu-id="e1e5e-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="e1e5e-104">Šajā tēmā ir apskatīti kartes moduļi un aprakstīts, kā tos konfigurēt programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e1e5e-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e1e5e-105">Kartes modulī tiek parādītas veikalu atrašanās vietas interaktīvajā kartē, kas tiek atveidota, izmantojot [Bing kartes V8 tīmekļa kontroli](/bingmaps/v8-web-control/).</span><span class="sxs-lookup"><span data-stu-id="e1e5e-105">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="e1e5e-106">Nepieciešama Bing karšu API atslēga, un tā ir jāpievieno kopīgo parametru lapā pakalpojumā Commerce headquarters.</span><span class="sxs-lookup"><span data-stu-id="e1e5e-106">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="e1e5e-107">Karšu moduļi sniedz dažādus skatus, piemēram, Ceļa, Gaisa un Ielas skatu, ko lietotāji var atlasīt, lai skatītu kartes atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="e1e5e-107">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="e1e5e-108">Tās pieļauj arī tādas mijiedarbības kā tālummaiņa un lietotāja atrašanās vietas izmantošana.</span><span class="sxs-lookup"><span data-stu-id="e1e5e-108">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="e1e5e-109">Kartes modulis darbojas savienojumā ar veikala atlasītāja moduli, lai noteiktu to veikalu ģeogrāfiskās atrašanās vietas, kas ir jāatveido kartē.</span><span class="sxs-lookup"><span data-stu-id="e1e5e-109">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="e1e5e-110">Veikala atlasītājs un karšu moduļi mijiedarbojas kad lietotājs atlasa veikalu vienā no šiem moduļiem vietnes lapā.</span><span class="sxs-lookup"><span data-stu-id="e1e5e-110">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="e1e5e-111">Karšu moduļus var pagarināt citiem scenārijiem, kas nav saistīti ar veikala atlasītāja moduļiem.</span><span class="sxs-lookup"><span data-stu-id="e1e5e-111">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="e1e5e-112">Tomēr moduļa pielāgošana ir obligāta.</span><span class="sxs-lookup"><span data-stu-id="e1e5e-112">However, module customization is required.</span></span>

> [!NOTE]
> <span data-ttu-id="e1e5e-113">Kartes modulis ir pieejams Dynamics 365 Commerce 10.0.13 laidienā.</span><span class="sxs-lookup"><span data-stu-id="e1e5e-113">The map module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="e1e5e-114">Attēlā zemāk redzams piemērs kartes modulim, kas tiek izmantots veikala atrašanās vietas lapā.</span><span class="sxs-lookup"><span data-stu-id="e1e5e-114">The following image shows an example of a map module that is used on a store locations page.</span></span>

![Veikala atlasītāja moduļa piemērs](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="e1e5e-116">Moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="e1e5e-116">Module properties</span></span>

| <span data-ttu-id="e1e5e-117">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="e1e5e-117">Property name</span></span>             | <span data-ttu-id="e1e5e-118">Vērtība</span><span class="sxs-lookup"><span data-stu-id="e1e5e-118">Value</span></span>                 | <span data-ttu-id="e1e5e-119">apraksts</span><span class="sxs-lookup"><span data-stu-id="e1e5e-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="e1e5e-120">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="e1e5e-120">Heading</span></span> | <span data-ttu-id="e1e5e-121">Teksts</span><span class="sxs-lookup"><span data-stu-id="e1e5e-121">Text</span></span> | <span data-ttu-id="e1e5e-122">Moduļa virsraksts.</span><span class="sxs-lookup"><span data-stu-id="e1e5e-122">The heading for the module.</span></span> |
| <span data-ttu-id="e1e5e-123">Spraudītes opcijas: noklusējuma ikona</span><span class="sxs-lookup"><span data-stu-id="e1e5e-123">Pushpin options: Default icon</span></span> | <span data-ttu-id="e1e5e-124">Attēls</span><span class="sxs-lookup"><span data-stu-id="e1e5e-124">Image</span></span> | <span data-ttu-id="e1e5e-125">Spraudītes simbola attēls, ko izmantot veikaliem, kas tiek parādīti kartē.</span><span class="sxs-lookup"><span data-stu-id="e1e5e-125">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="e1e5e-126">Spraudītes opcijas: aktīva ikona</span><span class="sxs-lookup"><span data-stu-id="e1e5e-126">Pushpin options: Active icon</span></span> | <span data-ttu-id="e1e5e-127">Attēls</span><span class="sxs-lookup"><span data-stu-id="e1e5e-127">Image</span></span> | <span data-ttu-id="e1e5e-128">Spraudītes simbola attēls, ko izmantot veikalam, kas tiek atlasīts kartē.</span><span class="sxs-lookup"><span data-stu-id="e1e5e-128">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="e1e5e-129">Spraudītes opcijas: noklusējuma ikonas krāsa</span><span class="sxs-lookup"><span data-stu-id="e1e5e-129">Pushpin options: Default icon color</span></span> | <span data-ttu-id="e1e5e-130">Rakstzīmju virkne</span><span class="sxs-lookup"><span data-stu-id="e1e5e-130">Character string</span></span> | <span data-ttu-id="e1e5e-131">Spraudītes simbolu krāsas teksts vai heksadecimālā vērtība kartē.</span><span class="sxs-lookup"><span data-stu-id="e1e5e-131">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="e1e5e-132">Spraudītes opcijas: aktīvās ikonas krāsa</span><span class="sxs-lookup"><span data-stu-id="e1e5e-132">Pushpin options: Active icon color</span></span> | <span data-ttu-id="e1e5e-133">Rakstzīmju virkne</span><span class="sxs-lookup"><span data-stu-id="e1e5e-133">Character string</span></span> | <span data-ttu-id="e1e5e-134">Atlasītās spraudītes simbolu krāsas teksts vai heksadecimālā vērtība kartē.</span><span class="sxs-lookup"><span data-stu-id="e1e5e-134">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="e1e5e-135">Rādīt indeksu</span><span class="sxs-lookup"><span data-stu-id="e1e5e-135">Show index</span></span> | <span data-ttu-id="e1e5e-136">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="e1e5e-136">**True** or **False**</span></span> | <span data-ttu-id="e1e5e-137">Ja šis rekvizīts ir iestatīts kā **Patiess**, katrs spraudītes simbols, kas norāda veikalu, rādīs indeksu.</span><span class="sxs-lookup"><span data-stu-id="e1e5e-137">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="e1e5e-138">Šis indekss atbildīs indeksam saraksta skatā, ko rāda veikala atlasītāja modulis.</span><span class="sxs-lookup"><span data-stu-id="e1e5e-138">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="e1e5e-139">Pievienot atļautos kartējuma vietrāžus URL uz vietnes satura drošības politikas direktīvām</span><span class="sxs-lookup"><span data-stu-id="e1e5e-139">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="e1e5e-140">Lai karšu modulis darbotos ar Bing kartēm, ir jānodrošina, ka ir atļauti šādi kartēšanas vietrāži URL jūsu vietnes satura drošības politikā (CSP).</span><span class="sxs-lookup"><span data-stu-id="e1e5e-140">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed per your site's content security policy (CSP).</span></span> <span data-ttu-id="e1e5e-141">Šis iestatījums tiek veikts Commerce vietnes veidotājā, pievienojot atļautos vietrāžus URL dažādām vietnes CSP direktīvām (piemēram, **img-src**).</span><span class="sxs-lookup"><span data-stu-id="e1e5e-141">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="e1e5e-142">Papildinformāciju skatiet [Satura drošības politika](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="e1e5e-142">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="e1e5e-143">**connect-src** direktīvai pievienojiet **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="e1e5e-143">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="e1e5e-144">**img-src** direktīvai pievienojiet **&#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="e1e5e-144">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="e1e5e-145">**script-src** direktīvai pievienojiet **&#42;.bing.com, &#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="e1e5e-145">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="e1e5e-146">**script style-src** direktīvai pievienojiet **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="e1e5e-146">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="e1e5e-147">Mapes moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="e1e5e-147">Add a map module to a page</span></span>

<span data-ttu-id="e1e5e-148">Lai iegūtu detalizētu informāciju par to, kā konfigurēt kartes moduli lapā, skatiet [Veikala atlasītāja modulis](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="e1e5e-148">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="e1e5e-149">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e1e5e-149">Additional resources</span></span>

[<span data-ttu-id="e1e5e-150">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="e1e5e-150">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e1e5e-151">Pirkšanas lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="e1e5e-151">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="e1e5e-152">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="e1e5e-152">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e1e5e-153">Veikalu atlasītāja modulis</span><span class="sxs-lookup"><span data-stu-id="e1e5e-153">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="e1e5e-154">Bing karšu pārvaldība organizācijā</span><span class="sxs-lookup"><span data-stu-id="e1e5e-154">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="e1e5e-155">Bing karšu V8 tīmekļa kontrole</span><span class="sxs-lookup"><span data-stu-id="e1e5e-155">Bing Maps V8 Web Control</span></span>](/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]