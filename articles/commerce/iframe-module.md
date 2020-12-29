---
title: Iframe modulis
description: Šajā tēmā tiek stāstīts par iframe moduli un aprakstīts, kā to pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 4afd8f60938c99d1981be1625ef28f91d9e4bb4c
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665400"
---
# <a name="iframe-module"></a><span data-ttu-id="1e3c4-103">Iframe modulis</span><span class="sxs-lookup"><span data-stu-id="1e3c4-103">Iframe module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1e3c4-104">Šajā tēmā tiek stāstīts par iframe moduli un aprakstīts, kā to pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-104">This topic covers the iframe module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1e3c4-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="1e3c4-105">Overview</span></span>

<span data-ttu-id="1e3c4-106">Iframe modulis nodrošina iframe (iekļauts kadrs), kas vieso ārējo saturu vietnē.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-106">An iframe module provides an iframe (inline frame) that hosts external content on a site.</span></span> <span data-ttu-id="1e3c4-107">Piemēram, to var izmantot, lai viesotu YouTube video vai PDF failu skatītāju jebkurā vietnes lapā.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-107">For example, it can be used to host a YouTube video or a PDF file viewer on any site page.</span></span> 

<span data-ttu-id="1e3c4-108">Iframe modulim nepieciešams mērķa URL.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-108">An iframe module requires a target URL.</span></span> <span data-ttu-id="1e3c4-109">Tad tas vieso mērķa lapas saturu, kas atrodas HTML **iframe** elementā.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-109">It then hosts the content of the target page inside an HTML **iframe** element.</span></span> <span data-ttu-id="1e3c4-110">Ārējiem URL jābūt atļautajā sarakstā katras vietnes satura drošības politikas (CSP) direktīvām.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-110">External URLs must be on the allow list per the site's content security policy (CSP) directives.</span></span> <span data-ttu-id="1e3c4-111">Iframe saturam ir jāatļauj vietrāžus URL, izmantojot **frame-ancestor** direktīvu.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-111">For iframe content, URLs should be allowed by using the **frame-ancestor** directive.</span></span> <span data-ttu-id="1e3c4-112">Papildinformāciju skatiet [Pārvaldīt satura drošības politiku (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="1e3c4-112">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

> [!NOTE]
> <span data-ttu-id="1e3c4-113">Iframe modulis ir pieejams Dynamics 365 Commerce 10.0.13 laidienā.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-113">The iframe module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="1e3c4-114">Sekojošajā attēlā ir parādīti iframe moduļu piemēri, kas parāda ārējos videoklipus vietnes lapās.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-114">The following image shows examples of iframe modules that showcase external videos on site pages.</span></span>

![Piemērs iframe moduļiem, kas izrāda ārējos video](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a><span data-ttu-id="1e3c4-116">Iframe moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="1e3c4-116">Iframe module properties</span></span>

| <span data-ttu-id="1e3c4-117">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="1e3c4-117">Property name</span></span>             | <span data-ttu-id="1e3c4-118">Vērtība</span><span class="sxs-lookup"><span data-stu-id="1e3c4-118">Value</span></span>                 | <span data-ttu-id="1e3c4-119">apraksts</span><span class="sxs-lookup"><span data-stu-id="1e3c4-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="1e3c4-120">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="1e3c4-120">Heading</span></span> | <span data-ttu-id="1e3c4-121">Teksts</span><span class="sxs-lookup"><span data-stu-id="1e3c4-121">Text</span></span> | <span data-ttu-id="1e3c4-122">Moduļa virsraksts.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-122">The heading for the module.</span></span> |
| <span data-ttu-id="1e3c4-123">Mērķa URL</span><span class="sxs-lookup"><span data-stu-id="1e3c4-123">Target URL</span></span> | <span data-ttu-id="1e3c4-124">Vietrādis URL</span><span class="sxs-lookup"><span data-stu-id="1e3c4-124">URL</span></span> | <span data-ttu-id="1e3c4-125">Modulī viesotais vietrādis URL.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-125">The URL that is hosted in the module.</span></span> |
| <span data-ttu-id="1e3c4-126">Augstums</span><span class="sxs-lookup"><span data-stu-id="1e3c4-126">Height</span></span> | <span data-ttu-id="1e3c4-127">Skaitlis vai procenti</span><span class="sxs-lookup"><span data-stu-id="1e3c4-127">Number or percentage</span></span> | <span data-ttu-id="1e3c4-128">Moduļa augstums, pikseļos vai procentos.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-128">The height of the module, in pixels or as a percentage.</span></span> <span data-ttu-id="1e3c4-129">Piemēram, vērtība **100** tiks apstrādāta kā pikseļu skaits, un vērtība **100%** tiks apstrādāta kā procenti.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-129">For example, the value **100** will be treated as a number of pixels, and the value **100%** will be treated as a percentage.</span></span> |
| <span data-ttu-id="1e3c4-130">Aria etiķete</span><span class="sxs-lookup"><span data-stu-id="1e3c4-130">Aria label</span></span> | <span data-ttu-id="1e3c4-131">Teksts</span><span class="sxs-lookup"><span data-stu-id="1e3c4-131">Text</span></span> | <span data-ttu-id="1e3c4-132">Pieejamības nolūkiem var definēt Pieejamo bagātinātā interneta lietojumprogrammu (ARIA) etiķeti.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-132">An Accessible Rich Internet Applications (ARIA) label can be defined for accessibility purposes.</span></span> |

## <a name="add-an-iframe-module-to-a-page"></a><span data-ttu-id="1e3c4-133">Iframe moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="1e3c4-133">Add an iframe module to a page</span></span>

<span data-ttu-id="1e3c4-134">Lai lappusei pievienotu iframe moduli, lai parādītu ārējo videoklipu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-134">To add an iframe module to a page to show an external video, follow these steps.</span></span>

1. <span data-ttu-id="1e3c4-135">Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-135">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="1e3c4-136">Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukums** ievadiet **Mārketinga veidne** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-136">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="1e3c4-137">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-137">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="1e3c4-138">Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-138">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="1e3c4-139">Dialoglodziņā **Izvēlēties veidni** atlasiet veidni **Mārketinga veidne**.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-139">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="1e3c4-140">Sadaļā **Lapas nosaukums** ievadiet **Mārketinga lapa** pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-140">Under **Page name**, enter **Marketing page**, and then select **OK**.</span></span>
1. <span data-ttu-id="1e3c4-141">Jaunās lapas slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-141">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1e3c4-142">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-142">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1e3c4-143">Moduļa rekvizītu rūtī iestatiet **Platuma** vērtību, lai **Aizpildītu konteineru**.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-143">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="1e3c4-144">Slotā **Konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-144">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1e3c4-145">Dialoglodziņā **Pievienot moduli** atlasiet moduli **iframe** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-145">In the **Add Module** dialog box, select the **iframe** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1e3c4-146">Moduļa rekvizītu rūtī iestatiet **Mērķa URL** vērtību video ārējam vietrādim URL.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-146">In the module's properties pane, set the **Target URL** value to an external URL for a video.</span></span>
1. <span data-ttu-id="1e3c4-147">Pēc nepieciešamības iestatiet citus rekvizītus, kā **Virsraksts** un **Augstums**.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-147">Set other properties, such as **Heading** and **Height**, as you require.</span></span>
1. <span data-ttu-id="1e3c4-148">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-148">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="1e3c4-149">Dodieties uz vietnes mārketinga lapu.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-149">Go to the marketing page on your site.</span></span> <span data-ttu-id="1e3c4-150">Jums vajadzētu redzēt, ka video tiek atveidots iframe modulī.</span><span class="sxs-lookup"><span data-stu-id="1e3c4-150">You should see that the video is rendered in the iframe module.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="1e3c4-151">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="1e3c4-151">Additional resources</span></span>

[<span data-ttu-id="1e3c4-152">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="1e3c4-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1e3c4-153">Satura drošības politikas (CSP) pārvaldība</span><span class="sxs-lookup"><span data-stu-id="1e3c4-153">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
