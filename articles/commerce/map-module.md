---
title: Kartes modulis
description: Šajā tēmā ir apskatīti kartes moduļi un aprakstīts, kā tos konfigurēt programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: d2cbc67a186a76647a4f7ddc7942b15d3e469ece
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817210"
---
# <a name="map-module"></a><span data-ttu-id="4d5c6-103">Kartes modulis</span><span class="sxs-lookup"><span data-stu-id="4d5c6-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="4d5c6-104">Šajā tēmā ir apskatīti kartes moduļi un aprakstīts, kā tos konfigurēt programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4d5c6-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4d5c6-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="4d5c6-105">Overview</span></span>

<span data-ttu-id="4d5c6-106">Kartes modulī tiek parādītas veikalu atrašanās vietas interaktīvajā kartē, kas tiek atveidota, izmantojot [Bing kartes V8 tīmekļa kontroli](https://docs.microsoft.com/bingmaps/v8-web-control/).</span><span class="sxs-lookup"><span data-stu-id="4d5c6-106">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="4d5c6-107">Nepieciešama Bing karšu API atslēga, un tā ir jāpievieno kopīgo parametru lapā pakalpojumā Commerce headquarters.</span><span class="sxs-lookup"><span data-stu-id="4d5c6-107">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="4d5c6-108">Karšu moduļi sniedz dažādus skatus, piemēram, Ceļa, Gaisa un Ielas skatu, ko lietotāji var atlasīt, lai skatītu kartes atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="4d5c6-108">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="4d5c6-109">Tās pieļauj arī tādas mijiedarbības kā tālummaiņa un lietotāja atrašanās vietas izmantošana.</span><span class="sxs-lookup"><span data-stu-id="4d5c6-109">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="4d5c6-110">cKartes modulis darbojas savienojumā ar veikala atlasītāja moduli, lai noteiktu to veikalu ģeogrāfiskās atrašanās vietas, kas ir jāatveido kartē.</span><span class="sxs-lookup"><span data-stu-id="4d5c6-110">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="4d5c6-111">Veikala atlasītājs un karšu moduļi mijiedarbojas kad lietotājs atlasa veikalu vienā no šiem moduļiem vietnes lapā.</span><span class="sxs-lookup"><span data-stu-id="4d5c6-111">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="4d5c6-112">Karšu moduļus var pagarināt citiem scenārijiem, kas nav saistīti ar veikala atlasītāja moduļiem.</span><span class="sxs-lookup"><span data-stu-id="4d5c6-112">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="4d5c6-113">Tomēr moduļa pielāgošana ir obligāta.</span><span class="sxs-lookup"><span data-stu-id="4d5c6-113">However, module customization is required.</span></span>

> [!NOTE]
> <span data-ttu-id="4d5c6-114">Kartes modulis ir pieejams Dynamics 365 Commerce 10.0.13 laidienā.</span><span class="sxs-lookup"><span data-stu-id="4d5c6-114">The map module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="4d5c6-115">Attēlā zemāk redzams piemērs kartes modulim, kas tiek izmantots veikala atrašanās vietas lapā.</span><span class="sxs-lookup"><span data-stu-id="4d5c6-115">The following image shows an example of a map module that is used on a store locations page.</span></span>

![Veikala atlasītāja moduļa piemērs](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="4d5c6-117">Moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="4d5c6-117">Module properties</span></span>

| <span data-ttu-id="4d5c6-118">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="4d5c6-118">Property name</span></span>             | <span data-ttu-id="4d5c6-119">Vērtība</span><span class="sxs-lookup"><span data-stu-id="4d5c6-119">Value</span></span>                 | <span data-ttu-id="4d5c6-120">apraksts</span><span class="sxs-lookup"><span data-stu-id="4d5c6-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="4d5c6-121">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="4d5c6-121">Heading</span></span> | <span data-ttu-id="4d5c6-122">Teksts</span><span class="sxs-lookup"><span data-stu-id="4d5c6-122">Text</span></span> | <span data-ttu-id="4d5c6-123">Moduļa virsraksts.</span><span class="sxs-lookup"><span data-stu-id="4d5c6-123">The heading for the module.</span></span> |
| <span data-ttu-id="4d5c6-124">Spraudītes opcijas: noklusējuma ikona</span><span class="sxs-lookup"><span data-stu-id="4d5c6-124">Pushpin options: Default icon</span></span> | <span data-ttu-id="4d5c6-125">Attēls</span><span class="sxs-lookup"><span data-stu-id="4d5c6-125">Image</span></span> | <span data-ttu-id="4d5c6-126">Spraudītes simbola attēls, ko izmantot veikaliem, kas tiek parādīti kartē.</span><span class="sxs-lookup"><span data-stu-id="4d5c6-126">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="4d5c6-127">Spraudītes opcijas: aktīva ikona</span><span class="sxs-lookup"><span data-stu-id="4d5c6-127">Pushpin options: Active icon</span></span> | <span data-ttu-id="4d5c6-128">Attēls</span><span class="sxs-lookup"><span data-stu-id="4d5c6-128">Image</span></span> | <span data-ttu-id="4d5c6-129">Spraudītes simbola attēls, ko izmantot veikalam, kas tiek atlasīts kartē.</span><span class="sxs-lookup"><span data-stu-id="4d5c6-129">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="4d5c6-130">Spraudītes opcijas: noklusējuma ikonas krāsa</span><span class="sxs-lookup"><span data-stu-id="4d5c6-130">Pushpin options: Default icon color</span></span> | <span data-ttu-id="4d5c6-131">Rakstzīmju virkne</span><span class="sxs-lookup"><span data-stu-id="4d5c6-131">Character string</span></span> | <span data-ttu-id="4d5c6-132">Spraudītes simbolu krāsas teksts vai heksadecimālā vērtība kartē.</span><span class="sxs-lookup"><span data-stu-id="4d5c6-132">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="4d5c6-133">Spraudītes opcijas: aktīvās ikonas krāsa</span><span class="sxs-lookup"><span data-stu-id="4d5c6-133">Pushpin options: Active icon color</span></span> | <span data-ttu-id="4d5c6-134">Rakstzīmju virkne</span><span class="sxs-lookup"><span data-stu-id="4d5c6-134">Character string</span></span> | <span data-ttu-id="4d5c6-135">Atlasītās spraudītes simbolu krāsas teksts vai heksadecimālā vērtība kartē.</span><span class="sxs-lookup"><span data-stu-id="4d5c6-135">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="4d5c6-136">Rādīt indeksu</span><span class="sxs-lookup"><span data-stu-id="4d5c6-136">Show index</span></span> | <span data-ttu-id="4d5c6-137">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="4d5c6-137">**True** or **False**</span></span> | <span data-ttu-id="4d5c6-138">Ja šis rekvizīts ir iestatīts kā **Patiess**, katrs spraudītes simbols, kas norāda veikalu, rādīs indeksu.</span><span class="sxs-lookup"><span data-stu-id="4d5c6-138">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="4d5c6-139">Šis indekss atbildīs indeksam saraksta skatā, ko rāda veikala atlasītāja modulis.</span><span class="sxs-lookup"><span data-stu-id="4d5c6-139">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="4d5c6-140">Pievienot atļautos kartējuma vietrāžus URL uz vietnes satura drošības politikas direktīvām</span><span class="sxs-lookup"><span data-stu-id="4d5c6-140">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="4d5c6-141">Lai karšu modulis darbotos ar Bing kartēm, ir jānodrošina, ka ir atļauti šādi kartēšanas vietrāži URL (pazīstami arī kā "iekļauti baltajā sarakstā") jūsu vietnes satura drošības politikā (CSP).</span><span class="sxs-lookup"><span data-stu-id="4d5c6-141">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed (also known as "whitelisted") per your site's content security policy (CSP).</span></span> <span data-ttu-id="4d5c6-142">Šis iestatījums tiek veikts Commerce vietnes veidotājā, pievienojot atļautos vietrāžus URL dažādām vietnes CSP direktīvām (piemēram, **img-src**).</span><span class="sxs-lookup"><span data-stu-id="4d5c6-142">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="4d5c6-143">Papildinformāciju skatiet [Satura drošības politika](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="4d5c6-143">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="4d5c6-144">**connect-src** direktīvai pievienojiet **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="4d5c6-144">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="4d5c6-145">**img-src** direktīvai pievienojiet **&#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="4d5c6-145">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="4d5c6-146">**script-src** direktīvai pievienojiet **&#42;.bing.com, &#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="4d5c6-146">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="4d5c6-147">**script style-src** direktīvai pievienojiet **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="4d5c6-147">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="4d5c6-148">Mapes moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="4d5c6-148">Add a map module to a page</span></span>

<span data-ttu-id="4d5c6-149">Lai iegūtu detalizētu informāciju par to, kā konfigurēt kartes moduli lapā, skatiet [Veikala atlasītāja modulis](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="4d5c6-149">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="4d5c6-150">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="4d5c6-150">Additional resources</span></span>

[<span data-ttu-id="4d5c6-151">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="4d5c6-151">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4d5c6-152">Pirkšanas lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="4d5c6-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="4d5c6-153">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="4d5c6-153">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="4d5c6-154">Veikalu atlasītāja modulis</span><span class="sxs-lookup"><span data-stu-id="4d5c6-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="4d5c6-155">Bing karšu pārvaldība organizācijā</span><span class="sxs-lookup"><span data-stu-id="4d5c6-155">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="4d5c6-156">Bing karšu V8 tīmekļa kontrole</span><span class="sxs-lookup"><span data-stu-id="4d5c6-156">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)
