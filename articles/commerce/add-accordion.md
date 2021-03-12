---
title: Akordeona modulis
description: Šajā tēmā tiek stāstīts par akordeona moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 28cb9d2e450ff1c05d4faa5cac343e03ef051437
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986108"
---
# <a name="accordion-module"></a><span data-ttu-id="9ce7d-103">Akordeona modulis</span><span class="sxs-lookup"><span data-stu-id="9ce7d-103">Accordion module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9ce7d-104">Šajā tēmā tiek stāstīts par akordeona moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-104">This topic covers accordion modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9ce7d-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="9ce7d-105">Overview</span></span>

<span data-ttu-id="9ce7d-106">Akordeona moduļi ir konteineram līdzīgi moduļi, ko izmanto informācijas vai moduļu organizēšanai lapā, nodrošinot saliekamu atvilktnei līdzīgu iespēju.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-106">Accordion modules are container-like modules that are used to organize the information or modules on a page by providing a collapsible drawer-like capability.</span></span> <span data-ttu-id="9ce7d-107">Akordeona moduli var izmantot jebkurā lapā.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-107">An accordion module can be used on any page.</span></span>

<span data-ttu-id="9ce7d-108">Katrā akordeona modulī var pievienot vienu vai vairākus akordeona krājumu moduļus.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-108">Inside every accordion module, one or more accordion item modules can be added.</span></span> <span data-ttu-id="9ce7d-109">Katrs akordeona krājumu modulis attēlo saliekamu atvilktni.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-109">Each accordion item module represents a collapsible drawer.</span></span> <span data-ttu-id="9ce7d-110">Katrā akordeona krājuma modulī var pievienot vienu vai vairākus moduļus.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-110">Inside every accordion item module, one or more modules can be added.</span></span> <span data-ttu-id="9ce7d-111">Moduļu veidiem, kurus var pievienot akordeona krājuma modulim, nav ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-111">There are no restrictions on the types of modules that can be added to an accordion item module.</span></span>

<span data-ttu-id="9ce7d-112">Attēlā zemāk redzams akordeona moduļa piemērs, kas tiek izmantots informācijas organizēšanai veikala bieži uzdoto jautājumu (FAQ) lapā.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-112">The following image shows an example of an accordion module that is used to organize information on a store's frequently asked questions (FAQ) page.</span></span>

![Akordeona moduļa piemērs](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a><span data-ttu-id="9ce7d-114">Akordeona moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="9ce7d-114">Accordion module properties</span></span>

| <span data-ttu-id="9ce7d-115">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="9ce7d-115">Property name</span></span> | <span data-ttu-id="9ce7d-116">Vērtības</span><span class="sxs-lookup"><span data-stu-id="9ce7d-116">Values</span></span> | <span data-ttu-id="9ce7d-117">apraksts</span><span class="sxs-lookup"><span data-stu-id="9ce7d-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="9ce7d-118">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="9ce7d-118">Heading</span></span> | <span data-ttu-id="9ce7d-119">Teksts</span><span class="sxs-lookup"><span data-stu-id="9ce7d-119">Text</span></span> | <span data-ttu-id="9ce7d-120">Šis rekvizīts norāda neobligātu teksta virsrakstu akordeona modulim.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-120">This property specifies an optional text heading for the accordion module.</span></span> |
| <span data-ttu-id="9ce7d-121">Izvērst visus</span><span class="sxs-lookup"><span data-stu-id="9ce7d-121">Expand All</span></span> | <span data-ttu-id="9ce7d-122">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="9ce7d-122">**True** or **False**</span></span> | <span data-ttu-id="9ce7d-123">Ja vērtība ir iestatīta uz **Patiess**, izvēršanas/sakļaušanas funkcionalitāte ir ieslēgta, lai visus akordeona moduļa krājumus varētu izvērst un sakļaut.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-123">If the value is set to **True**, expand/collapse functionality is turned on, so that all items in the accordion module can be expanded and collapsed.</span></span> |
| <span data-ttu-id="9ce7d-124">Mijiedarbības stils</span><span class="sxs-lookup"><span data-stu-id="9ce7d-124">Interaction Style</span></span> | <span data-ttu-id="9ce7d-125">**Neatkarīgs** vai **Izvērst tikai vienu krājumu**</span><span class="sxs-lookup"><span data-stu-id="9ce7d-125">**Independent** or **Expand one item only**</span></span> | <span data-ttu-id="9ce7d-126">Šis rekvizīts definē mijiedarbības stilu akordeona krājumiem.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-126">This property defines the style of interaction for accordion items.</span></span> <span data-ttu-id="9ce7d-127">Ja vērtība ir iestatīta uz **Neatkarīgs**, katru akordeona krājumu var izvērst vai sakļaut neatkarīgi no citiem.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-127">If the value is set to **Independent**, each accordion item can be expanded or collapsed independently.</span></span> <span data-ttu-id="9ce7d-128">Ja vērtība ir iestatīta uz **Izvērst tikai vienu krājumu**, vienlaicīgi var izvērst tikai vienu krājumu.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-128">If the value is set to **Expand one item only**, only one item can be expanded at a time.</span></span> <span data-ttu-id="9ce7d-129">Krājumus izvēršot, iepriekš izvērstie krājumi tiek sakļauti.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-129">As items are expanded, previously expanded items are collapsed.</span></span> |

## <a name="accordion-item-module-properties"></a><span data-ttu-id="9ce7d-130">Akordeona krājuma moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="9ce7d-130">Accordion item module properties</span></span>

| <span data-ttu-id="9ce7d-131">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="9ce7d-131">Property name</span></span> | <span data-ttu-id="9ce7d-132">Vērtības</span><span class="sxs-lookup"><span data-stu-id="9ce7d-132">Values</span></span> | <span data-ttu-id="9ce7d-133">apraksts</span><span class="sxs-lookup"><span data-stu-id="9ce7d-133">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="9ce7d-134">Nosaukums</span><span class="sxs-lookup"><span data-stu-id="9ce7d-134">Title</span></span> | <span data-ttu-id="9ce7d-135">Teksts</span><span class="sxs-lookup"><span data-stu-id="9ce7d-135">Text</span></span> | <span data-ttu-id="9ce7d-136">Šis rekvizīts norāda virsraksta tekstu akordeona krājuma modulim.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-136">This property specifies the title text for the accordion item module.</span></span> <span data-ttu-id="9ce7d-137">Atlasot virsraksta reģionu, lietotāji var izvērst vai sakļaut sadaļu.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-137">By selecting the title region, users can expand or collapse the section.</span></span> |
| <span data-ttu-id="9ce7d-138">Izvērst pēc noklusējuma</span><span class="sxs-lookup"><span data-stu-id="9ce7d-138">Expand by default</span></span> | <span data-ttu-id="9ce7d-139">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="9ce7d-139">**True** or **False**</span></span> | <span data-ttu-id="9ce7d-140">Ja vērtība ir iestatīta uz **Patiess**, akordeona krājums tiek izvērsts pēc noklusējuma, ielādējot lapu.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-140">If the value is set to **True**, the accordion item is expanded by default when the page is loaded.</span></span> |

## <a name="add-an-accordion-module-to-a-faq-page"></a><span data-ttu-id="9ce7d-141">Akordeona moduļa pievienošana FAQ lapā</span><span class="sxs-lookup"><span data-stu-id="9ce7d-141">Add an accordion module to a FAQ page</span></span>

<span data-ttu-id="9ce7d-142">Lai pievienotu akordeona moduli FAQ lapai un iestatītu tās rekvizītus vietņu veidotājā, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-142">To add an accordion module to a FAQ page and set its properties in site builder, follow these steps.</span></span>

1. <span data-ttu-id="9ce7d-143">Dodieties uz **Lapas** un izmantojiet Fabrikam mārketinga veidni (vai jebkuru veidni, kurai nav ierobežojumu), lai izveidotu jaunu lapu, kuras nosaukums ir **Veikala FAQ**.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-143">Go to **Pages**, and use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store FAQ**.</span></span>
1. <span data-ttu-id="9ce7d-144">**Noklusējuma lapas** slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-144">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9ce7d-145">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-145">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="9ce7d-146">Slotā **Konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-146">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9ce7d-147">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Akordeona krājums** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-147">In the **Add Module** dialog box, select the **Accordion** module, and then select **OK**.</span></span>
1. <span data-ttu-id="9ce7d-148">Akordeona moduļa rekvizītu rūtī atlasiet blakus zīmuļa simbolam **Virsraksts**.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-148">In the property pane of the accordion module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="9ce7d-149">Dialoglodziņa **Virsraksts** sadaļā **Virsraksta teksts** ievadiet **Bieži uzdotie jautājumi**.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-149">In the **Heading** dialog box, under **Heading Text**, enter **Frequently asked questions**.</span></span> <span data-ttu-id="9ce7d-150">Tad atl. **Labi**.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-150">Then select **OK**.</span></span>
1. <span data-ttu-id="9ce7d-151">Akordeona moduļa rekvizītu rūtī atzīmējiet izvēles rūtiņu **Rādīt izvērstu visu** un pēc tam laukā **Saziņas stils** atlasiet **Neatkarīgs**.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-151">In the property pane of the accordion module, select the **Show expand all** check box, and then, in the **Interaction style** field, select **Independent**.</span></span>
1. <span data-ttu-id="9ce7d-152">Slotā **Akordeons** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-152">In the **Accordion** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9ce7d-153">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Akordeona krājums** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-153">In the **Add Module** dialog box, select the **Accordion item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="9ce7d-154">Akordeona krājuma moduļa rekvizītu rūtī sadaļā **Nosaukums** ievadiet virsraksta tekstu (piemēram, **Kā darbojas atgriešana?**).</span><span class="sxs-lookup"><span data-stu-id="9ce7d-154">In the property pane of the accordion item module, under **Title**, enter title text (for example, **How do returns work?**).</span></span>
1. <span data-ttu-id="9ce7d-155">Slotā **Akordeona krājums** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-155">In the **Accordion item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9ce7d-156">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Teksta bloks** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-156">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="9ce7d-157">Teksta bloka moduļa rekvizītu rūtī ievadiet teksta rindkopu (piemēram, **Atgriešana ir jāapstrādā, izmantojot zvanu centru. Sazinieties ar 1-800-FABRIKAM atgriešanai. Precēm ir 30 dienu atgriešanas politika. Atgriešanas ir jāuzsāk šajā laika posmā**).</span><span class="sxs-lookup"><span data-stu-id="9ce7d-157">In the property pane of the text block module, enter a paragraph of text (for example, **Returns must be processed via the call center. Contact 1-800-FABRIKAM for returns. Products have a 30-day return policy. Returns must be initiated within this time frame.**).</span></span>
1. <span data-ttu-id="9ce7d-158">Slotā **Akordeons** pievienojiet vēl dažus akordeona krājumu moduļus.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-158">In the **Accordion** slot, add a few more accordion item modules.</span></span> <span data-ttu-id="9ce7d-159">Katrā akordeona krājuma modulī pievienojiet teksta bloka moduli, kam ir saturs.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-159">In each accordion item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="9ce7d-160">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-160">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="9ce7d-161">Lapā tiks parādīts akordeona modulis ar pievienoto saturu.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-161">The page will show an accordion module that has the content that you added.</span></span>
1. <span data-ttu-id="9ce7d-162">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="9ce7d-162">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9ce7d-163">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="9ce7d-163">Additional resources</span></span>

[<span data-ttu-id="9ce7d-164">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="9ce7d-164">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="9ce7d-165">Konteinera modulis</span><span class="sxs-lookup"><span data-stu-id="9ce7d-165">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="9ce7d-166">Cilnes modulis</span><span class="sxs-lookup"><span data-stu-id="9ce7d-166">Tab module</span></span>](add-tab.md)

[<span data-ttu-id="9ce7d-167">Teksta bloka modulis</span><span class="sxs-lookup"><span data-stu-id="9ce7d-167">Text block module</span></span>](add-content-rich-block.md)
