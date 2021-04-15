---
title: Akordeona modulis
description: Šajā tēmā aplūkoti Accordion moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: ba973299291276fe48d82360e203ca28f02aaffb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796274"
---
# <a name="accordion-module"></a><span data-ttu-id="d2756-103">Akordeona modulis</span><span class="sxs-lookup"><span data-stu-id="d2756-103">Accordion module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d2756-104">Šajā tēmā aplūkoti Accordion moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d2756-104">This topic covers accordion modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d2756-105">Akordeona moduļi ir konteineram līdzīgi moduļi, ko izmanto informācijas vai moduļu organizēšanai lapā, nodrošinot saliekamu atvilktnei līdzīgu iespēju.</span><span class="sxs-lookup"><span data-stu-id="d2756-105">Accordion modules are container-like modules that are used to organize the information or modules on a page by providing a collapsible drawer-like capability.</span></span> <span data-ttu-id="d2756-106">Akordeona moduli var izmantot jebkurā lapā.</span><span class="sxs-lookup"><span data-stu-id="d2756-106">An accordion module can be used on any page.</span></span>

<span data-ttu-id="d2756-107">Katrā akordeona modulī var pievienot vienu vai vairākus akordeona krājumu moduļus.</span><span class="sxs-lookup"><span data-stu-id="d2756-107">Inside every accordion module, one or more accordion item modules can be added.</span></span> <span data-ttu-id="d2756-108">Katrs akordeona krājumu modulis attēlo saliekamu atvilktni.</span><span class="sxs-lookup"><span data-stu-id="d2756-108">Each accordion item module represents a collapsible drawer.</span></span> <span data-ttu-id="d2756-109">Katrā akordeona krājuma modulī var pievienot vienu vai vairākus moduļus.</span><span class="sxs-lookup"><span data-stu-id="d2756-109">Inside every accordion item module, one or more modules can be added.</span></span> <span data-ttu-id="d2756-110">Moduļu veidiem, kurus var pievienot akordeona krājuma modulim, nav ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="d2756-110">There are no restrictions on the types of modules that can be added to an accordion item module.</span></span>

<span data-ttu-id="d2756-111">Attēlā zemāk redzams akordeona moduļa piemērs, kas tiek izmantots informācijas organizēšanai veikala bieži uzdoto jautājumu (FAQ) lapā.</span><span class="sxs-lookup"><span data-stu-id="d2756-111">The following image shows an example of an accordion module that is used to organize information on a store's frequently asked questions (FAQ) page.</span></span>

![Akordeona moduļa piemērs](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a><span data-ttu-id="d2756-113">Akordeona moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="d2756-113">Accordion module properties</span></span>

| <span data-ttu-id="d2756-114">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="d2756-114">Property name</span></span> | <span data-ttu-id="d2756-115">Vērtības</span><span class="sxs-lookup"><span data-stu-id="d2756-115">Values</span></span> | <span data-ttu-id="d2756-116">apraksts</span><span class="sxs-lookup"><span data-stu-id="d2756-116">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="d2756-117">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="d2756-117">Heading</span></span> | <span data-ttu-id="d2756-118">Teksts</span><span class="sxs-lookup"><span data-stu-id="d2756-118">Text</span></span> | <span data-ttu-id="d2756-119">Šis rekvizīts norāda neobligātu teksta virsrakstu akordeona modulim.</span><span class="sxs-lookup"><span data-stu-id="d2756-119">This property specifies an optional text heading for the accordion module.</span></span> |
| <span data-ttu-id="d2756-120">Izvērst visus</span><span class="sxs-lookup"><span data-stu-id="d2756-120">Expand All</span></span> | <span data-ttu-id="d2756-121">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="d2756-121">**True** or **False**</span></span> | <span data-ttu-id="d2756-122">Ja vērtība ir iestatīta uz **Patiess**, izvēršanas/sakļaušanas funkcionalitāte ir ieslēgta, lai visus akordeona moduļa krājumus varētu izvērst un sakļaut.</span><span class="sxs-lookup"><span data-stu-id="d2756-122">If the value is set to **True**, expand/collapse functionality is turned on, so that all items in the accordion module can be expanded and collapsed.</span></span> |
| <span data-ttu-id="d2756-123">Mijiedarbības stils</span><span class="sxs-lookup"><span data-stu-id="d2756-123">Interaction Style</span></span> | <span data-ttu-id="d2756-124">**Neatkarīgs** vai **Izvērst tikai vienu krājumu**</span><span class="sxs-lookup"><span data-stu-id="d2756-124">**Independent** or **Expand one item only**</span></span> | <span data-ttu-id="d2756-125">Šis rekvizīts definē mijiedarbības stilu akordeona krājumiem.</span><span class="sxs-lookup"><span data-stu-id="d2756-125">This property defines the style of interaction for accordion items.</span></span> <span data-ttu-id="d2756-126">Ja vērtība ir iestatīta uz **Neatkarīgs**, katru akordeona krājumu var izvērst vai sakļaut neatkarīgi no citiem.</span><span class="sxs-lookup"><span data-stu-id="d2756-126">If the value is set to **Independent**, each accordion item can be expanded or collapsed independently.</span></span> <span data-ttu-id="d2756-127">Ja vērtība ir iestatīta uz **Izvērst tikai vienu krājumu**, vienlaicīgi var izvērst tikai vienu krājumu.</span><span class="sxs-lookup"><span data-stu-id="d2756-127">If the value is set to **Expand one item only**, only one item can be expanded at a time.</span></span> <span data-ttu-id="d2756-128">Krājumus izvēršot, iepriekš izvērstie krājumi tiek sakļauti.</span><span class="sxs-lookup"><span data-stu-id="d2756-128">As items are expanded, previously expanded items are collapsed.</span></span> |

## <a name="accordion-item-module-properties"></a><span data-ttu-id="d2756-129">Akordeona krājuma moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="d2756-129">Accordion item module properties</span></span>

| <span data-ttu-id="d2756-130">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="d2756-130">Property name</span></span> | <span data-ttu-id="d2756-131">Vērtības</span><span class="sxs-lookup"><span data-stu-id="d2756-131">Values</span></span> | <span data-ttu-id="d2756-132">apraksts</span><span class="sxs-lookup"><span data-stu-id="d2756-132">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="d2756-133">Nosaukums</span><span class="sxs-lookup"><span data-stu-id="d2756-133">Title</span></span> | <span data-ttu-id="d2756-134">Teksts</span><span class="sxs-lookup"><span data-stu-id="d2756-134">Text</span></span> | <span data-ttu-id="d2756-135">Šis rekvizīts norāda virsraksta tekstu akordeona krājuma modulim.</span><span class="sxs-lookup"><span data-stu-id="d2756-135">This property specifies the title text for the accordion item module.</span></span> <span data-ttu-id="d2756-136">Atlasot virsraksta reģionu, lietotāji var izvērst vai sakļaut sadaļu.</span><span class="sxs-lookup"><span data-stu-id="d2756-136">By selecting the title region, users can expand or collapse the section.</span></span> |
| <span data-ttu-id="d2756-137">Izvērst pēc noklusējuma</span><span class="sxs-lookup"><span data-stu-id="d2756-137">Expand by default</span></span> | <span data-ttu-id="d2756-138">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="d2756-138">**True** or **False**</span></span> | <span data-ttu-id="d2756-139">Ja vērtība ir iestatīta uz **Patiess**, akordeona krājums tiek izvērsts pēc noklusējuma, ielādējot lapu.</span><span class="sxs-lookup"><span data-stu-id="d2756-139">If the value is set to **True**, the accordion item is expanded by default when the page is loaded.</span></span> |

## <a name="add-an-accordion-module-to-a-faq-page"></a><span data-ttu-id="d2756-140">Akordeona moduļa pievienošana FAQ lapā</span><span class="sxs-lookup"><span data-stu-id="d2756-140">Add an accordion module to a FAQ page</span></span>

<span data-ttu-id="d2756-141">Lai pievienotu akordeona moduli FAQ lapai un iestatītu tās rekvizītus vietņu veidotājā, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="d2756-141">To add an accordion module to a FAQ page and set its properties in site builder, follow these steps.</span></span>

1. <span data-ttu-id="d2756-142">Dodieties uz **Lapas** un izmantojiet Fabrikam mārketinga veidni (vai jebkuru veidni, kurai nav ierobežojumu), lai izveidotu jaunu lapu, kuras nosaukums ir **Veikala FAQ**.</span><span class="sxs-lookup"><span data-stu-id="d2756-142">Go to **Pages**, and use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store FAQ**.</span></span>
1. <span data-ttu-id="d2756-143">**Noklusējuma lapas** slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="d2756-143">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d2756-144">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d2756-144">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d2756-145">Slotā **Konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="d2756-145">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d2756-146">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Akordeona krājums** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d2756-146">In the **Add Module** dialog box, select the **Accordion** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d2756-147">Akordeona moduļa rekvizītu rūtī atlasiet blakus zīmuļa simbolam **Virsraksts**.</span><span class="sxs-lookup"><span data-stu-id="d2756-147">In the property pane of the accordion module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="d2756-148">Dialoglodziņa **Virsraksts** sadaļā **Virsraksta teksts** ievadiet **Bieži uzdotie jautājumi**.</span><span class="sxs-lookup"><span data-stu-id="d2756-148">In the **Heading** dialog box, under **Heading Text**, enter **Frequently asked questions**.</span></span> <span data-ttu-id="d2756-149">Tad atl. **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d2756-149">Then select **OK**.</span></span>
1. <span data-ttu-id="d2756-150">Akordeona moduļa rekvizītu rūtī atzīmējiet izvēles rūtiņu **Rādīt izvērstu visu** un pēc tam laukā **Saziņas stils** atlasiet **Neatkarīgs**.</span><span class="sxs-lookup"><span data-stu-id="d2756-150">In the property pane of the accordion module, select the **Show expand all** check box, and then, in the **Interaction style** field, select **Independent**.</span></span>
1. <span data-ttu-id="d2756-151">Slotā **Akordeons** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="d2756-151">In the **Accordion** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d2756-152">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Akordeona krājums** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d2756-152">In the **Add Module** dialog box, select the **Accordion item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d2756-153">Akordeona krājuma moduļa rekvizītu rūtī sadaļā **Nosaukums** ievadiet virsraksta tekstu (piemēram, **Kā darbojas atgriešana?**).</span><span class="sxs-lookup"><span data-stu-id="d2756-153">In the property pane of the accordion item module, under **Title**, enter title text (for example, **How do returns work?**).</span></span>
1. <span data-ttu-id="d2756-154">Slotā **Akordeona krājums** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="d2756-154">In the **Accordion item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d2756-155">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Teksta bloks** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d2756-155">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d2756-156">Teksta bloka moduļa rekvizītu rūtī ievadiet teksta rindkopu (piemēram, **Atgriešana ir jāapstrādā, izmantojot zvanu centru. Sazinieties ar 1-800-FABRIKAM atgriešanai. Precēm ir 30 dienu atgriešanas politika. Atgriešanas ir jāuzsāk šajā laika posmā**).</span><span class="sxs-lookup"><span data-stu-id="d2756-156">In the property pane of the text block module, enter a paragraph of text (for example, **Returns must be processed via the call center. Contact 1-800-FABRIKAM for returns. Products have a 30-day return policy. Returns must be initiated within this time frame.**).</span></span>
1. <span data-ttu-id="d2756-157">Slotā **Akordeons** pievienojiet vēl dažus akordeona krājumu moduļus.</span><span class="sxs-lookup"><span data-stu-id="d2756-157">In the **Accordion** slot, add a few more accordion item modules.</span></span> <span data-ttu-id="d2756-158">Katrā akordeona krājuma modulī pievienojiet teksta bloka moduli, kam ir saturs.</span><span class="sxs-lookup"><span data-stu-id="d2756-158">In each accordion item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="d2756-159">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="d2756-159">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="d2756-160">Lapā tiks parādīts akordeona modulis ar pievienoto saturu.</span><span class="sxs-lookup"><span data-stu-id="d2756-160">The page will show an accordion module that has the content that you added.</span></span>
1. <span data-ttu-id="d2756-161">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="d2756-161">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d2756-162">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d2756-162">Additional resources</span></span>

[<span data-ttu-id="d2756-163">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="d2756-163">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d2756-164">Konteinera modulis</span><span class="sxs-lookup"><span data-stu-id="d2756-164">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="d2756-165">Cilnes modulis</span><span class="sxs-lookup"><span data-stu-id="d2756-165">Tab module</span></span>](add-tab.md)

[<span data-ttu-id="d2756-166">Teksta bloka modulis</span><span class="sxs-lookup"><span data-stu-id="d2756-166">Text block module</span></span>](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]