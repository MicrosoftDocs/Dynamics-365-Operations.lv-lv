---
title: Cilnes modulis
description: Šajā tēmā aplūkoti cilnes moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8375c33bd6ffd3004cfc9d7b686d9a0edc77cdef
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209231"
---
# <a name="tab-module"></a><span data-ttu-id="fff7f-103">Cilnes modulis</span><span class="sxs-lookup"><span data-stu-id="fff7f-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fff7f-104">Šajā tēmā aplūkoti cilnes moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fff7f-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="fff7f-105">Cilnes moduļi ir konteineram līdzīgi moduļi, kas tiek izmantoti, lai organizētu informāciju vietnes lapā cilnēs.</span><span class="sxs-lookup"><span data-stu-id="fff7f-105">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="fff7f-106">Tos var izmantot visās lapās, kurās informācija ir jāsniedz cilnēs.</span><span class="sxs-lookup"><span data-stu-id="fff7f-106">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="fff7f-107">Katrā cilnes modulī var pievienot vienu vai vairākus cilnes krājumu moduļus.</span><span class="sxs-lookup"><span data-stu-id="fff7f-107">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="fff7f-108">Katrs cilnes krājuma modulis pārstāv vienu cilni. Katrā cilnes krājuma modulī var pievienot vienu vai vairākus moduļus.</span><span class="sxs-lookup"><span data-stu-id="fff7f-108">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="fff7f-109">Moduļu veidiem, kurus var pievienot cilnes krājuma modulim, nav ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="fff7f-109">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="fff7f-110">Attēlā zemāk redzams cilnes moduļa piemērs vietas lapā.</span><span class="sxs-lookup"><span data-stu-id="fff7f-110">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="fff7f-111">Šajā piemērā ir atlasīta cilne **Piegāde**.</span><span class="sxs-lookup"><span data-stu-id="fff7f-111">In this example, the **Shipping** tab selected.</span></span>

![Cilnes moduļa piemērs](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="fff7f-113">Cilnes moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="fff7f-113">Tab module properties</span></span>

| <span data-ttu-id="fff7f-114">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="fff7f-114">Property name</span></span> | <span data-ttu-id="fff7f-115">Vērtības</span><span class="sxs-lookup"><span data-stu-id="fff7f-115">Values</span></span> | <span data-ttu-id="fff7f-116">apraksts</span><span class="sxs-lookup"><span data-stu-id="fff7f-116">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="fff7f-117">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="fff7f-117">Heading</span></span> | <span data-ttu-id="fff7f-118">Teksts</span><span class="sxs-lookup"><span data-stu-id="fff7f-118">Text</span></span> | <span data-ttu-id="fff7f-119">Šis rekvizīts norāda neobligātu teksta virsrakstu cilnes modulim.</span><span class="sxs-lookup"><span data-stu-id="fff7f-119">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="fff7f-120">Aktīvās cilnes indekss</span><span class="sxs-lookup"><span data-stu-id="fff7f-120">Active Tab Index</span></span> | <span data-ttu-id="fff7f-121">Skaits</span><span class="sxs-lookup"><span data-stu-id="fff7f-121">Number</span></span> | <span data-ttu-id="fff7f-122">Šis rekvizīts norāda cilni, kas pēc noklusējuma ir jāaktivizē, kad tiek ielādēta lapa.</span><span class="sxs-lookup"><span data-stu-id="fff7f-122">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="fff7f-123">Ja nav norādīta vērtība, pēc noklusējuma ir aktīvs ir pirmais cilnes elements.</span><span class="sxs-lookup"><span data-stu-id="fff7f-123">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="fff7f-124">Cilnes krājuma moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="fff7f-124">Tab item module properties</span></span>

| <span data-ttu-id="fff7f-125">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="fff7f-125">Property name</span></span> | <span data-ttu-id="fff7f-126">Vērtības</span><span class="sxs-lookup"><span data-stu-id="fff7f-126">Values</span></span> | <span data-ttu-id="fff7f-127">apraksts</span><span class="sxs-lookup"><span data-stu-id="fff7f-127">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="fff7f-128">Nosaukums</span><span class="sxs-lookup"><span data-stu-id="fff7f-128">Title</span></span> | <span data-ttu-id="fff7f-129">Teksts</span><span class="sxs-lookup"><span data-stu-id="fff7f-129">Text</span></span> | <span data-ttu-id="fff7f-130">Šis rekvizīts norāda virsraksta tekstu krājuma modulim.</span><span class="sxs-lookup"><span data-stu-id="fff7f-130">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="fff7f-131">Cilnes moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="fff7f-131">Add a tab module to a page</span></span>

<span data-ttu-id="fff7f-132">Lai pievienotu cilnes moduli lapai un iestatītu rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="fff7f-132">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="fff7f-133">Izmantojiet Fabrikam mārketinga veidni (vai jebkuru veidni, kurai nav ierobežojumu), lai izveidotu jaunu lapu, kuras nosaukums ir **Veikala politiku lapa**.</span><span class="sxs-lookup"><span data-stu-id="fff7f-133">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="fff7f-134">**Noklusējuma lapas** slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="fff7f-134">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fff7f-135">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="fff7f-135">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="fff7f-136">Slotā **Konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="fff7f-136">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fff7f-137">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Cilne** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="fff7f-137">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="fff7f-138">Cilnes moduļa rekvizītu rūtī atlasiet blakus zīmuļa simbolam **Virsraksts**.</span><span class="sxs-lookup"><span data-stu-id="fff7f-138">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="fff7f-139">Dialoglodziņa **Virsraksts** sadaļā **Virsraksta teksts** ievadiet virsraksta tekstu (piemēram, **Politikas**).</span><span class="sxs-lookup"><span data-stu-id="fff7f-139">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="fff7f-140">Tad atl. **Labi**.</span><span class="sxs-lookup"><span data-stu-id="fff7f-140">Then select **OK**.</span></span>
1. <span data-ttu-id="fff7f-141">Slotā **Cilne** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="fff7f-141">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fff7f-142">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Cilnes krājums** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="fff7f-142">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="fff7f-143">Cilnes krājuma moduļa rekvizītu rūtī sadaļā **Nosaukums** ievadiet virsraksta tekstu (piemēram, **Piegāde**).</span><span class="sxs-lookup"><span data-stu-id="fff7f-143">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="fff7f-144">Slotā **Cilnes krājums** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="fff7f-144">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fff7f-145">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Teksta bloks** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="fff7f-145">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="fff7f-146">Teksta bloka moduļa rekvizītu rūtī pievienojiet tekstu sadaļā **Bagātinātais teksts** un ievadiet teksta rindkopu.</span><span class="sxs-lookup"><span data-stu-id="fff7f-146">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="fff7f-147">Slotā **Cilne** pievienojiet vēl dažus cilnes krājumu moduļus, kuriem ir virsraksti.</span><span class="sxs-lookup"><span data-stu-id="fff7f-147">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="fff7f-148">Katrā cilnes krājuma modulī pievienojiet teksta bloka moduli, kam ir saturs.</span><span class="sxs-lookup"><span data-stu-id="fff7f-148">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="fff7f-149">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="fff7f-149">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="fff7f-150">Lapā tiks parādīts cilnes modulis, kas satur cilnes krājumu moduļus, kuriem ir jūsu pievienotais saturs.</span><span class="sxs-lookup"><span data-stu-id="fff7f-150">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="fff7f-151">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="fff7f-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fff7f-152">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="fff7f-152">Additional resources</span></span>

[<span data-ttu-id="fff7f-153">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="fff7f-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="fff7f-154">Konteinera modulis</span><span class="sxs-lookup"><span data-stu-id="fff7f-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="fff7f-155">Akordeona modulis</span><span class="sxs-lookup"><span data-stu-id="fff7f-155">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="fff7f-156">Teksta bloka modulis</span><span class="sxs-lookup"><span data-stu-id="fff7f-156">Text block module</span></span>](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]