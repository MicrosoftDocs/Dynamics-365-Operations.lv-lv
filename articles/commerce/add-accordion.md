---
title: Akordeona modulis
description: Šajā tēmā aplūkoti Accordion moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: a08441f5dffa9c2c65b304d0265dd107a838a685
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206611"
---
# <a name="accordion-module"></a><span data-ttu-id="d893c-103">Akordeona modulis</span><span class="sxs-lookup"><span data-stu-id="d893c-103">Accordion module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d893c-104">Šajā tēmā aplūkoti Accordion moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d893c-104">This topic covers accordion modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d893c-105">Akordeona moduļi ir konteineram līdzīgi moduļi, ko izmanto informācijas vai moduļu organizēšanai lapā, nodrošinot saliekamu atvilktnei līdzīgu iespēju.</span><span class="sxs-lookup"><span data-stu-id="d893c-105">Accordion modules are container-like modules that are used to organize the information or modules on a page by providing a collapsible drawer-like capability.</span></span> <span data-ttu-id="d893c-106">Akordeona moduli var izmantot jebkurā lapā.</span><span class="sxs-lookup"><span data-stu-id="d893c-106">An accordion module can be used on any page.</span></span>

<span data-ttu-id="d893c-107">Katrā akordeona modulī var pievienot vienu vai vairākus akordeona krājumu moduļus.</span><span class="sxs-lookup"><span data-stu-id="d893c-107">Inside every accordion module, one or more accordion item modules can be added.</span></span> <span data-ttu-id="d893c-108">Katrs akordeona krājumu modulis attēlo saliekamu atvilktni.</span><span class="sxs-lookup"><span data-stu-id="d893c-108">Each accordion item module represents a collapsible drawer.</span></span> <span data-ttu-id="d893c-109">Katrā akordeona krājuma modulī var pievienot vienu vai vairākus moduļus.</span><span class="sxs-lookup"><span data-stu-id="d893c-109">Inside every accordion item module, one or more modules can be added.</span></span> <span data-ttu-id="d893c-110">Moduļu veidiem, kurus var pievienot akordeona krājuma modulim, nav ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="d893c-110">There are no restrictions on the types of modules that can be added to an accordion item module.</span></span>

<span data-ttu-id="d893c-111">Attēlā zemāk redzams akordeona moduļa piemērs, kas tiek izmantots informācijas organizēšanai veikala bieži uzdoto jautājumu (FAQ) lapā.</span><span class="sxs-lookup"><span data-stu-id="d893c-111">The following image shows an example of an accordion module that is used to organize information on a store's frequently asked questions (FAQ) page.</span></span>

![Akordeona moduļa piemērs](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a><span data-ttu-id="d893c-113">Akordeona moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="d893c-113">Accordion module properties</span></span>

| <span data-ttu-id="d893c-114">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="d893c-114">Property name</span></span> | <span data-ttu-id="d893c-115">Vērtības</span><span class="sxs-lookup"><span data-stu-id="d893c-115">Values</span></span> | <span data-ttu-id="d893c-116">apraksts</span><span class="sxs-lookup"><span data-stu-id="d893c-116">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="d893c-117">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="d893c-117">Heading</span></span> | <span data-ttu-id="d893c-118">Teksts</span><span class="sxs-lookup"><span data-stu-id="d893c-118">Text</span></span> | <span data-ttu-id="d893c-119">Šis rekvizīts norāda neobligātu teksta virsrakstu akordeona modulim.</span><span class="sxs-lookup"><span data-stu-id="d893c-119">This property specifies an optional text heading for the accordion module.</span></span> |
| <span data-ttu-id="d893c-120">Izvērst visus</span><span class="sxs-lookup"><span data-stu-id="d893c-120">Expand All</span></span> | <span data-ttu-id="d893c-121">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="d893c-121">**True** or **False**</span></span> | <span data-ttu-id="d893c-122">Ja vērtība ir iestatīta uz **Patiess**, izvēršanas/sakļaušanas funkcionalitāte ir ieslēgta, lai visus akordeona moduļa krājumus varētu izvērst un sakļaut.</span><span class="sxs-lookup"><span data-stu-id="d893c-122">If the value is set to **True**, expand/collapse functionality is turned on, so that all items in the accordion module can be expanded and collapsed.</span></span> |
| <span data-ttu-id="d893c-123">Mijiedarbības stils</span><span class="sxs-lookup"><span data-stu-id="d893c-123">Interaction Style</span></span> | <span data-ttu-id="d893c-124">**Neatkarīgs** vai **Izvērst tikai vienu krājumu**</span><span class="sxs-lookup"><span data-stu-id="d893c-124">**Independent** or **Expand one item only**</span></span> | <span data-ttu-id="d893c-125">Šis rekvizīts definē mijiedarbības stilu akordeona krājumiem.</span><span class="sxs-lookup"><span data-stu-id="d893c-125">This property defines the style of interaction for accordion items.</span></span> <span data-ttu-id="d893c-126">Ja vērtība ir iestatīta uz **Neatkarīgs**, katru akordeona krājumu var izvērst vai sakļaut neatkarīgi no citiem.</span><span class="sxs-lookup"><span data-stu-id="d893c-126">If the value is set to **Independent**, each accordion item can be expanded or collapsed independently.</span></span> <span data-ttu-id="d893c-127">Ja vērtība ir iestatīta uz **Izvērst tikai vienu krājumu**, vienlaicīgi var izvērst tikai vienu krājumu.</span><span class="sxs-lookup"><span data-stu-id="d893c-127">If the value is set to **Expand one item only**, only one item can be expanded at a time.</span></span> <span data-ttu-id="d893c-128">Krājumus izvēršot, iepriekš izvērstie krājumi tiek sakļauti.</span><span class="sxs-lookup"><span data-stu-id="d893c-128">As items are expanded, previously expanded items are collapsed.</span></span> |

## <a name="accordion-item-module-properties"></a><span data-ttu-id="d893c-129">Akordeona krājuma moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="d893c-129">Accordion item module properties</span></span>

| <span data-ttu-id="d893c-130">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="d893c-130">Property name</span></span> | <span data-ttu-id="d893c-131">Vērtības</span><span class="sxs-lookup"><span data-stu-id="d893c-131">Values</span></span> | <span data-ttu-id="d893c-132">apraksts</span><span class="sxs-lookup"><span data-stu-id="d893c-132">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="d893c-133">Nosaukums</span><span class="sxs-lookup"><span data-stu-id="d893c-133">Title</span></span> | <span data-ttu-id="d893c-134">Teksts</span><span class="sxs-lookup"><span data-stu-id="d893c-134">Text</span></span> | <span data-ttu-id="d893c-135">Šis rekvizīts norāda virsraksta tekstu akordeona krājuma modulim.</span><span class="sxs-lookup"><span data-stu-id="d893c-135">This property specifies the title text for the accordion item module.</span></span> <span data-ttu-id="d893c-136">Atlasot virsraksta reģionu, lietotāji var izvērst vai sakļaut sadaļu.</span><span class="sxs-lookup"><span data-stu-id="d893c-136">By selecting the title region, users can expand or collapse the section.</span></span> |
| <span data-ttu-id="d893c-137">Izvērst pēc noklusējuma</span><span class="sxs-lookup"><span data-stu-id="d893c-137">Expand by default</span></span> | <span data-ttu-id="d893c-138">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="d893c-138">**True** or **False**</span></span> | <span data-ttu-id="d893c-139">Ja vērtība ir iestatīta uz **Patiess**, akordeona krājums tiek izvērsts pēc noklusējuma, ielādējot lapu.</span><span class="sxs-lookup"><span data-stu-id="d893c-139">If the value is set to **True**, the accordion item is expanded by default when the page is loaded.</span></span> |

## <a name="add-an-accordion-module-to-a-faq-page"></a><span data-ttu-id="d893c-140">Akordeona moduļa pievienošana FAQ lapā</span><span class="sxs-lookup"><span data-stu-id="d893c-140">Add an accordion module to a FAQ page</span></span>

<span data-ttu-id="d893c-141">Lai pievienotu akordeona moduli FAQ lapai un iestatītu tās rekvizītus vietņu veidotājā, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="d893c-141">To add an accordion module to a FAQ page and set its properties in site builder, follow these steps.</span></span>

1. <span data-ttu-id="d893c-142">Dodieties uz **Lapas** un izmantojiet Fabrikam mārketinga veidni (vai jebkuru veidni, kurai nav ierobežojumu), lai izveidotu jaunu lapu, kuras nosaukums ir **Veikala FAQ**.</span><span class="sxs-lookup"><span data-stu-id="d893c-142">Go to **Pages**, and use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store FAQ**.</span></span>
1. <span data-ttu-id="d893c-143">**Noklusējuma lapas** slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="d893c-143">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d893c-144">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d893c-144">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d893c-145">Slotā **Konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="d893c-145">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d893c-146">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Akordeona krājums** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d893c-146">In the **Add Module** dialog box, select the **Accordion** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d893c-147">Akordeona moduļa rekvizītu rūtī atlasiet blakus zīmuļa simbolam **Virsraksts**.</span><span class="sxs-lookup"><span data-stu-id="d893c-147">In the property pane of the accordion module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="d893c-148">Dialoglodziņa **Virsraksts** sadaļā **Virsraksta teksts** ievadiet **Bieži uzdotie jautājumi**.</span><span class="sxs-lookup"><span data-stu-id="d893c-148">In the **Heading** dialog box, under **Heading Text**, enter **Frequently asked questions**.</span></span> <span data-ttu-id="d893c-149">Tad atl. **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d893c-149">Then select **OK**.</span></span>
1. <span data-ttu-id="d893c-150">Akordeona moduļa rekvizītu rūtī atzīmējiet izvēles rūtiņu **Rādīt izvērstu visu** un pēc tam laukā **Saziņas stils** atlasiet **Neatkarīgs**.</span><span class="sxs-lookup"><span data-stu-id="d893c-150">In the property pane of the accordion module, select the **Show expand all** check box, and then, in the **Interaction style** field, select **Independent**.</span></span>
1. <span data-ttu-id="d893c-151">Slotā **Akordeons** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="d893c-151">In the **Accordion** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d893c-152">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Akordeona krājums** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d893c-152">In the **Add Module** dialog box, select the **Accordion item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d893c-153">Akordeona krājuma moduļa rekvizītu rūtī sadaļā **Nosaukums** ievadiet virsraksta tekstu (piemēram, **Kā darbojas atgriešana?**).</span><span class="sxs-lookup"><span data-stu-id="d893c-153">In the property pane of the accordion item module, under **Title**, enter title text (for example, **How do returns work?**).</span></span>
1. <span data-ttu-id="d893c-154">Slotā **Akordeona krājums** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="d893c-154">In the **Accordion item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d893c-155">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Teksta bloks** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d893c-155">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d893c-156">Teksta bloka moduļa rekvizītu rūtī ievadiet teksta rindkopu (piemēram, **Atgriešana ir jāapstrādā, izmantojot zvanu centru. Sazinieties ar 1-800-FABRIKAM atgriešanai. Precēm ir 30 dienu atgriešanas politika. Atgriešanas ir jāuzsāk šajā laika posmā**).</span><span class="sxs-lookup"><span data-stu-id="d893c-156">In the property pane of the text block module, enter a paragraph of text (for example, **Returns must be processed via the call center. Contact 1-800-FABRIKAM for returns. Products have a 30-day return policy. Returns must be initiated within this time frame.**).</span></span>
1. <span data-ttu-id="d893c-157">Slotā **Akordeons** pievienojiet vēl dažus akordeona krājumu moduļus.</span><span class="sxs-lookup"><span data-stu-id="d893c-157">In the **Accordion** slot, add a few more accordion item modules.</span></span> <span data-ttu-id="d893c-158">Katrā akordeona krājuma modulī pievienojiet teksta bloka moduli, kam ir saturs.</span><span class="sxs-lookup"><span data-stu-id="d893c-158">In each accordion item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="d893c-159">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="d893c-159">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="d893c-160">Lapā tiks parādīts akordeona modulis ar pievienoto saturu.</span><span class="sxs-lookup"><span data-stu-id="d893c-160">The page will show an accordion module that has the content that you added.</span></span>
1. <span data-ttu-id="d893c-161">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="d893c-161">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d893c-162">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d893c-162">Additional resources</span></span>

[<span data-ttu-id="d893c-163">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="d893c-163">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d893c-164">Konteinera modulis</span><span class="sxs-lookup"><span data-stu-id="d893c-164">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="d893c-165">Cilnes modulis</span><span class="sxs-lookup"><span data-stu-id="d893c-165">Tab module</span></span>](add-tab.md)

[<span data-ttu-id="d893c-166">Teksta bloka modulis</span><span class="sxs-lookup"><span data-stu-id="d893c-166">Text block module</span></span>](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]