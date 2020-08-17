---
title: Cilnes modulis
description: Šī tēma ietver cilnes moduļus un apraksta, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b4187dfd704c78d506d7840b04c986687fe807a3
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621017"
---
# <a name="tab-module"></a><span data-ttu-id="8348e-103">Cilnes modulis</span><span class="sxs-lookup"><span data-stu-id="8348e-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8348e-104">Šī tēma ietver cilnes moduļus un apraksta, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8348e-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8348e-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="8348e-105">Overview</span></span>

<span data-ttu-id="8348e-106">Cilnes moduļi ir konteineram līdzīgi moduļi, kas tiek izmantoti, lai organizētu informāciju vietnes lapā cilnēs.</span><span class="sxs-lookup"><span data-stu-id="8348e-106">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="8348e-107">Tos var izmantot visās lapās, kurās informācija ir jāsniedz cilnēs.</span><span class="sxs-lookup"><span data-stu-id="8348e-107">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="8348e-108">Katrā cilnes modulī var pievienot vienu vai vairākus cilnes krājumu moduļus.</span><span class="sxs-lookup"><span data-stu-id="8348e-108">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="8348e-109">Katrs cilnes krājuma modulis pārstāv vienu cilni. Katrā cilnes krājuma modulī var pievienot vienu vai vairākus moduļus.</span><span class="sxs-lookup"><span data-stu-id="8348e-109">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="8348e-110">Moduļu veidiem, kurus var pievienot cilnes krājuma modulim, nav ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="8348e-110">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="8348e-111">Attēlā zemāk redzams cilnes moduļa piemērs vietas lapā.</span><span class="sxs-lookup"><span data-stu-id="8348e-111">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="8348e-112">Šajā piemērā ir atlasīta cilne **Piegāde**.</span><span class="sxs-lookup"><span data-stu-id="8348e-112">In this example, the **Shipping** tab selected.</span></span>

![Cilnes moduļa piemērs](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="8348e-114">Cilnes moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="8348e-114">Tab module properties</span></span>

| <span data-ttu-id="8348e-115">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="8348e-115">Property name</span></span> | <span data-ttu-id="8348e-116">Vērtības</span><span class="sxs-lookup"><span data-stu-id="8348e-116">Values</span></span> | <span data-ttu-id="8348e-117">apraksts</span><span class="sxs-lookup"><span data-stu-id="8348e-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="8348e-118">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="8348e-118">Heading</span></span> | <span data-ttu-id="8348e-119">Teksts</span><span class="sxs-lookup"><span data-stu-id="8348e-119">Text</span></span> | <span data-ttu-id="8348e-120">Šis rekvizīts norāda neobligātu teksta virsrakstu cilnes modulim.</span><span class="sxs-lookup"><span data-stu-id="8348e-120">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="8348e-121">Aktīvās cilnes indekss</span><span class="sxs-lookup"><span data-stu-id="8348e-121">Active Tab Index</span></span> | <span data-ttu-id="8348e-122">Skaits</span><span class="sxs-lookup"><span data-stu-id="8348e-122">Number</span></span> | <span data-ttu-id="8348e-123">Šis rekvizīts norāda cilni, kas pēc noklusējuma ir jāaktivizē, kad tiek ielādēta lapa.</span><span class="sxs-lookup"><span data-stu-id="8348e-123">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="8348e-124">Ja nav norādīta vērtība, pēc noklusējuma ir aktīvs ir pirmais cilnes elements.</span><span class="sxs-lookup"><span data-stu-id="8348e-124">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="8348e-125">Cilnes krājuma moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="8348e-125">Tab item module properties</span></span>

| <span data-ttu-id="8348e-126">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="8348e-126">Property name</span></span> | <span data-ttu-id="8348e-127">Vērtības</span><span class="sxs-lookup"><span data-stu-id="8348e-127">Values</span></span> | <span data-ttu-id="8348e-128">apraksts</span><span class="sxs-lookup"><span data-stu-id="8348e-128">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="8348e-129">Nosaukums</span><span class="sxs-lookup"><span data-stu-id="8348e-129">Title</span></span> | <span data-ttu-id="8348e-130">Teksts</span><span class="sxs-lookup"><span data-stu-id="8348e-130">Text</span></span> | <span data-ttu-id="8348e-131">Šis rekvizīts norāda virsraksta tekstu krājuma modulim.</span><span class="sxs-lookup"><span data-stu-id="8348e-131">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="8348e-132">Cilnes moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="8348e-132">Add a tab module to a page</span></span>

<span data-ttu-id="8348e-133">Lai pievienotu cilnes moduli lapai un iestatītu rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="8348e-133">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="8348e-134">Izmantojiet Fabrikam mārketinga veidni (vai jebkuru veidni, kurai nav ierobežojumu), lai izveidotu jaunu lapu, kuras nosaukums ir **Veikala politiku lapa**.</span><span class="sxs-lookup"><span data-stu-id="8348e-134">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="8348e-135">**Noklusējuma lapas** slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="8348e-135">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8348e-136">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8348e-136">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="8348e-137">Slotā **Konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="8348e-137">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8348e-138">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Cilne** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8348e-138">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="8348e-139">Cilnes moduļa rekvizītu rūtī atlasiet blakus zīmuļa simbolam **Virsraksts**.</span><span class="sxs-lookup"><span data-stu-id="8348e-139">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="8348e-140">Dialoglodziņa **Virsraksts** sadaļā **Virsraksta teksts** ievadiet virsraksta tekstu (piemēram, **Politikas**).</span><span class="sxs-lookup"><span data-stu-id="8348e-140">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="8348e-141">Tad atl. **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8348e-141">Then select **OK**.</span></span>
1. <span data-ttu-id="8348e-142">Slotā **Cilne** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="8348e-142">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8348e-143">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Cilnes krājums** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8348e-143">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="8348e-144">Cilnes krājuma moduļa rekvizītu rūtī sadaļā **Nosaukums** ievadiet virsraksta tekstu (piemēram, **Piegāde**).</span><span class="sxs-lookup"><span data-stu-id="8348e-144">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="8348e-145">Slotā **Cilnes krājums** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="8348e-145">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8348e-146">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Teksta bloks** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8348e-146">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="8348e-147">Teksta bloka moduļa rekvizītu rūtī pievienojiet tekstu sadaļā **Bagātinātais teksts** un ievadiet teksta rindkopu.</span><span class="sxs-lookup"><span data-stu-id="8348e-147">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="8348e-148">Slotā **Cilne** pievienojiet vēl dažus cilnes krājumu moduļus, kuriem ir virsraksti.</span><span class="sxs-lookup"><span data-stu-id="8348e-148">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="8348e-149">Katrā cilnes krājuma modulī pievienojiet teksta bloka moduli, kam ir saturs.</span><span class="sxs-lookup"><span data-stu-id="8348e-149">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="8348e-150">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="8348e-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="8348e-151">Lapā tiks parādīts cilnes modulis, kas satur cilnes krājumu moduļus, kuriem ir jūsu pievienotais saturs.</span><span class="sxs-lookup"><span data-stu-id="8348e-151">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="8348e-152">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="8348e-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8348e-153">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="8348e-153">Additional resources</span></span>

[<span data-ttu-id="8348e-154">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="8348e-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8348e-155">Konteinera modulis</span><span class="sxs-lookup"><span data-stu-id="8348e-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="8348e-156">Akordeona modulis</span><span class="sxs-lookup"><span data-stu-id="8348e-156">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="8348e-157">Teksta bloka modulis</span><span class="sxs-lookup"><span data-stu-id="8348e-157">Text block module</span></span>](add-content-rich-block.md)
