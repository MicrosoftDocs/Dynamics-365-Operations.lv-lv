---
title: Atpakaļceļa modulis
description: Šajā tēmā aplūkoti Breadcrumb moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/20/2020
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
ms.openlocfilehash: e7b7cff280d8c6bcb09f2f59d96ec415b9cc1167
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796202"
---
# <a name="breadcrumb-module"></a><span data-ttu-id="12bdc-103">Atpakaļceļa modulis</span><span class="sxs-lookup"><span data-stu-id="12bdc-103">Breadcrumb module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="12bdc-104">Šajā tēmā aplūkoti Breadcrumb moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="12bdc-104">This topic covers breadcrumb modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="12bdc-105">Atpakaļceļa moduļi tiek izmantoti, lai nodrošinātu sekundāro navigāciju vietas lapās.</span><span class="sxs-lookup"><span data-stu-id="12bdc-105">Breadcrumb modules are used to provide secondary navigation on site pages.</span></span> <span data-ttu-id="12bdc-106">Parasti tie tiek parādīti lapas augšmalā zem virsraksta.</span><span class="sxs-lookup"><span data-stu-id="12bdc-106">They are typically shown at the top of a page, below the header.</span></span> <span data-ttu-id="12bdc-107">Kaut arī atpakaļceļa moduļus var pievienot jebkurai lapai, tie visbiežāk tiek izmantoti produktu informācijas lapās (PDP), lai parādītu preču kategoriju hierarhiju un nodrošinātu ātru veidu, kā pārvietoties vietnē.</span><span class="sxs-lookup"><span data-stu-id="12bdc-107">Although breadcrumb modules can be added to any page, they are most often used on product details pages (PDPs), to show the product category hierarchy and provide a quick way to move around a site.</span></span> <span data-ttu-id="12bdc-108">Atpakaļceļa moduli var izmantot arī, lai parādītu saiti "Atgriezties pie rezultātiem", kad lietotāji atver PDP no meklēšanas vai saraksta lapas.</span><span class="sxs-lookup"><span data-stu-id="12bdc-108">A breadcrumb module can also be used to show a "Back to results" link when users open a PDP from a search or list page.</span></span> <span data-ttu-id="12bdc-109">Šādā veidā lietotāji var ātri atgriezties filtrētā saraksta lapā, lai turpinātu iepirkšanos.</span><span class="sxs-lookup"><span data-stu-id="12bdc-109">In this way, users can quickly return to their filtered list page to continue shopping.</span></span>

<span data-ttu-id="12bdc-110">Lapās, kurās ir preču kategorijas konteksts, piemēram, PDP un kategoriju lapas, atpakaļceļa moduļi rāda kategoriju hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="12bdc-110">On pages that have product category context, such as PDPs and category pages, breadcrumb modules show the category hierarchy.</span></span> <span data-ttu-id="12bdc-111">Lapās, kurām nav kategorijas konteksta, atpakaļceļa moduļi pēc noklusējuma rāda **&lt;Vietnes sakne&gt; / &lt;Pašreizējā lapa&gt;**.</span><span class="sxs-lookup"><span data-stu-id="12bdc-111">On pages that don't have category context, breadcrumb modules show **&lt;Site root&gt; / &lt;Current page&gt;** by default.</span></span> <span data-ttu-id="12bdc-112">Atpakaļceļa moduļus var arī manuāli konfigurēt citos vietņu lapu veidos, lai parādītu saites uz noteiktām lapām attiecīgajā vietnē.</span><span class="sxs-lookup"><span data-stu-id="12bdc-112">Breadcrumb modules can also be manually configured on other types of site pages to show links to specific pages on the site.</span></span>

> [!NOTE]
> <span data-ttu-id="12bdc-113">Atpakaļceļa modulis ir pieejams Dynamics 365 Commerce 10.0.12 laidienā.</span><span class="sxs-lookup"><span data-stu-id="12bdc-113">The breadcrumb module is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

<span data-ttu-id="12bdc-114">Attēlā zemāk parādīts atpakaļceļa moduļa piemērs, kas parāda kategoriju hierarhiju PDP.</span><span class="sxs-lookup"><span data-stu-id="12bdc-114">The following image shows an example of a breadcrumb module that shows the category hierarchy on a PDP.</span></span>

![Atpakaļceļa moduļa piemērs](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a><span data-ttu-id="12bdc-116">Atpakaļceļa moduļa iestatījumi</span><span class="sxs-lookup"><span data-stu-id="12bdc-116">Breadcrumb module settings</span></span>

<span data-ttu-id="12bdc-117">Atpakaļceļa modulis balstās uz iestatījumu **Atpakaļceļa rādīšanas veids PDP**, kas ir definēts vietnes vietņu veidotājā **Vietnes iestatījumi \> Paplašinājumi**.</span><span class="sxs-lookup"><span data-stu-id="12bdc-117">The breadcrumb module relies on the **Breadcrumb display type on PDP** setting, which is defined at **Site Settings \> Extensions** in site builder.</span></span> <span data-ttu-id="12bdc-118">Šim iestatījumam ir pieejamas trīs vērtības.</span><span class="sxs-lookup"><span data-stu-id="12bdc-118">This setting has three possible values:</span></span>

- <span data-ttu-id="12bdc-119">**Rādīt kategoriju hierarhiju** — ja ir atlasīta šī vērtība, atpakaļceļa modulis parāda pilnu kategoriju hierarhiju precei, kas tiek skatīta PDP.</span><span class="sxs-lookup"><span data-stu-id="12bdc-119">**Show category hierarchy** – When this value is selected, the breadcrumb module will show the full category hierarchy of the product that is viewed on the PDP.</span></span>
- <span data-ttu-id="12bdc-120">**Rādīt atpakaļ pie rezultātiem** — ja atlasīta šī vērtība, atpakaļceļa modulis rādīs "Atpakaļ pie rezultātiem" saiti PDP, ja lietotājs ir atvēris PDP no moduļa, kas ļauj izveidot saiti "Atpakaļ pie rezultātiem".</span><span class="sxs-lookup"><span data-stu-id="12bdc-120">**Show back to results** – When this value is selected, the breadcrumb module will show a "Back to results" link on a PDP if the user opened the PDP from a module that allows for a "Back to results" link.</span></span> <span data-ttu-id="12bdc-121">Šī funkcionalitāte ir pieejama, ja lietotāji veic navigāciju no kategorijas, meklēšanas, saraksta un rekomendāciju saraksta lapas.</span><span class="sxs-lookup"><span data-stu-id="12bdc-121">This functionality is available when users navigate from category, search, list, and recommendation lists pages.</span></span> <span data-ttu-id="12bdc-122">Lai atbalstītu šo funkcionalitāti, preču kolekciju un meklēšanas rezultātu moduļiem ir rekvizīts, kas ir nosaukts **Atļaut atgriešanos pie rezultātiem PDP**.</span><span class="sxs-lookup"><span data-stu-id="12bdc-122">To support this functionality, product collection and search results modules have a property that is named **Allow back to results on PDP**.</span></span> <span data-ttu-id="12bdc-123">Šis rekvizīts sniedz jums elastību, lai definētu, kuriem moduļiem jāatbalsta "Atpakaļ pie rezultātiem" saites funkcionalitāte PDP.</span><span class="sxs-lookup"><span data-stu-id="12bdc-123">This property gives you the flexibility to define which modules should support the "Back to results" link functionality on the PDP.</span></span> <span data-ttu-id="12bdc-124">Piemēram, kad tiek atlasīta opcija **Rādīt atgriešanos pie rezultātiem** atpakaļceļa moduļa iestatījumam **Atpakaļceļa rādīšanas veids PDP**, un opcija **Ļaut atgriezties pie rezultātiem PDP** ir atlasīta meklēšanas lapas meklēšanas rezultātu modulim, saite "Atpakaļ pie rezultātiem" tiks parādīta, kad lietotāji no meklēšanas lapas pāriet uz PDP.</span><span class="sxs-lookup"><span data-stu-id="12bdc-124">For example, when **Show back to results** is selected for the **Breadcrumb display type on PDP** setting of the breadcrumb module, and **Allow back to results on PDP** is selected for the search page search results module, a "Back to results" link will be shown when users navigate from the search page to a PDP.</span></span>
- <span data-ttu-id="12bdc-125">**Rādīt kategoriju hierarhiju un atgriezties pie rezultātiem** — šī vērtība ir iepriekšējo divu vērtību kombinācija.</span><span class="sxs-lookup"><span data-stu-id="12bdc-125">**Show category hierarchy and back to results** – This value is a combination of the previous two.</span></span> <span data-ttu-id="12bdc-126">Atlasot šo vērtību, atpakaļceļa modulis parāda gan pilnu kategoriju hierarhiju, gan saiti "Atgriezties pie rezultātiem" (ja tā ir konfigurēta) PDP.</span><span class="sxs-lookup"><span data-stu-id="12bdc-126">When this value is selected, the breadcrumb module will show both the full category hierarchy and a "Back to results" link (if it's configured) on a PDP.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="12bdc-127">Šie iestatījumi ir pieejami Dynamics 365 Commerce 10.0.12 laidienā.</span><span class="sxs-lookup"><span data-stu-id="12bdc-127">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="12bdc-128">Ja veicat atjaunināšanu no vecākas Dynamics 365 Commerce versijas, ir manuāli jāatjaunina fails appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="12bdc-128">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="12bdc-129">Norādījumus par faila appsettings.json atjaunināšanu skatiet [SDK un moduļu bibliotēkas atjauninājumi](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="12bdc-129">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="breadcrumb-module-properties"></a><span data-ttu-id="12bdc-130">Atpakaļceļa moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="12bdc-130">Breadcrumb module properties</span></span>

| <span data-ttu-id="12bdc-131">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="12bdc-131">Property name</span></span> | <span data-ttu-id="12bdc-132">Vērtības</span><span class="sxs-lookup"><span data-stu-id="12bdc-132">Values</span></span> | <span data-ttu-id="12bdc-133">Apraksts</span><span class="sxs-lookup"><span data-stu-id="12bdc-133">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="12bdc-134">Sakne</span><span class="sxs-lookup"><span data-stu-id="12bdc-134">Root</span></span> | <span data-ttu-id="12bdc-135">Teksts vai saite</span><span class="sxs-lookup"><span data-stu-id="12bdc-135">Text or link</span></span>| <span data-ttu-id="12bdc-136">Šis neobligātais rekvizīts norāda saites tekstu un saites mērķi atpakaļceļa vietas saknei.</span><span class="sxs-lookup"><span data-stu-id="12bdc-136">This optional property specifies link text and a link target for the breadcrumb site root.</span></span> <span data-ttu-id="12bdc-137">Ja šis rekvizīts nav konfigurēts, sakne netiks definēta.</span><span class="sxs-lookup"><span data-stu-id="12bdc-137">If this property isn't configured, no root will be defined.</span></span> |
| <span data-ttu-id="12bdc-138">Atpakaļceļa saite</span><span class="sxs-lookup"><span data-stu-id="12bdc-138">Breadcrumb link</span></span> | <span data-ttu-id="12bdc-139">Saistīt</span><span class="sxs-lookup"><span data-stu-id="12bdc-139">Link</span></span> | <span data-ttu-id="12bdc-140">Šis neobligātais rekvizīts norāda saites manuāli konfigurētam atpakaļceļam, ja šīs saites ir nepieciešamas.</span><span class="sxs-lookup"><span data-stu-id="12bdc-140">This optional property specifies links for a manually configured breadcrumb, if these links are required.</span></span> <span data-ttu-id="12bdc-141">Saites parādās tādā secībā, kādā tās ir uzskaitītas.</span><span class="sxs-lookup"><span data-stu-id="12bdc-141">Links appear in the order that they are listed in.</span></span> |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a><span data-ttu-id="12bdc-142">Atpakaļceļa moduļa pievienošana jaunā lapā</span><span class="sxs-lookup"><span data-stu-id="12bdc-142">Add a breadcrumb module to a new page</span></span>

<span data-ttu-id="12bdc-143">Lai pievienotu atpakaļceļa moduli PDP un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="12bdc-143">To add a breadcrumb module to a PDP and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="12bdc-144">Dodieties uz **Vietnes iestatījumi \> Paplašinājumi** un pēc tam atlasiet **Rādīt kategoriju hierarhija** iestatījumam **Atpakaļceļa rādīšanas veids PDP**.</span><span class="sxs-lookup"><span data-stu-id="12bdc-144">Go to **Site Settings \> Extensions**, and then, for the **Breadcrumb display type on PDP** setting, select **Show category hierarchy**.</span></span>
1. <span data-ttu-id="12bdc-145">Atveriet **Veidnes** un atlasiet PDP veidni.</span><span class="sxs-lookup"><span data-stu-id="12bdc-145">Go to **Templates**, and select the PDP template.</span></span>
1. <span data-ttu-id="12bdc-146">Slotā **Konteiners**, kas satur lodziņu pirkšanas lodziņu, atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="12bdc-146">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="12bdc-147">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Atpakaļceļs** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="12bdc-147">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="12bdc-148">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="12bdc-148">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="12bdc-149">Dodieties uz **Lapas** un atveriet PDP, kas izmanto PDP veidni.</span><span class="sxs-lookup"><span data-stu-id="12bdc-149">Go to **Pages**, and open a PDP that uses the PDP template.</span></span> <span data-ttu-id="12bdc-150">Ja PDP vēl nepastāv, izveidojiet to.</span><span class="sxs-lookup"><span data-stu-id="12bdc-150">If a PDP doesn't yet exist, create one.</span></span>
1. <span data-ttu-id="12bdc-151">Slotā **Konteiners**, kas satur lodziņu pirkšanas lodziņu, atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="12bdc-151">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="12bdc-152">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Atpakaļceļs** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="12bdc-152">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="12bdc-153">Slota **Atpakaļceļš** rekvizītu rūtī sadaļā **Saknes** atlasiet **Saites teksts**.</span><span class="sxs-lookup"><span data-stu-id="12bdc-153">In the properties pane of the **Breadcrumb** slot, under **Root**, select **Link text**.</span></span>
1. <span data-ttu-id="12bdc-154">Dialoglodziņā **Saites teksts** ievadiet **Sākums** un pēc tam sadaļā **Saites mērķis** atlasiet **Pievienot saiti**.</span><span class="sxs-lookup"><span data-stu-id="12bdc-154">In the **Link text** dialog box, enter **Home**, and then, under **Link target**, select **Add a link**.</span></span>
1. <span data-ttu-id="12bdc-155">Dialoglodziņā **Pievienot saiti** atlasiet saiti atpakaļceļa saknei un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="12bdc-155">In the **Add a link** dialog box, select a link for the breadcrumb root, and then select **OK**.</span></span>
1. <span data-ttu-id="12bdc-156">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="12bdc-156">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="12bdc-157">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="12bdc-157">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="12bdc-158">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="12bdc-158">Additional resources</span></span>

[<span data-ttu-id="12bdc-159">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="12bdc-159">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="12bdc-160">Navigācijas izvēlnes modulis</span><span class="sxs-lookup"><span data-stu-id="12bdc-160">Navigation menu module</span></span>](nav-menu-module.md)

[<span data-ttu-id="12bdc-161">Vietņu atlasītāja modulis</span><span class="sxs-lookup"><span data-stu-id="12bdc-161">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="12bdc-162">Noklusējuma kategorijas ielādes lapas un meklēšanas rezultātu lapas apskats</span><span class="sxs-lookup"><span data-stu-id="12bdc-162">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="12bdc-163">Preču kolekcijas moduļi</span><span class="sxs-lookup"><span data-stu-id="12bdc-163">Product collection modules</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="12bdc-164">Pirkšanas lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="12bdc-164">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="12bdc-165">SDK un moduļu bibliotēkas atjauninājumi</span><span class="sxs-lookup"><span data-stu-id="12bdc-165">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]