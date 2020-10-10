---
title: Atpakaļceļa modulis
description: Šajā tēmā tiek stāstīts par atpakaļceļa moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7c6f215c3a7539cc16b0d72594702e6bdde7c58e
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817114"
---
# <a name="breadcrumb-module"></a><span data-ttu-id="ab39f-103">Atpakaļceļa modulis</span><span class="sxs-lookup"><span data-stu-id="ab39f-103">Breadcrumb module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ab39f-104">Šajā tēmā tiek stāstīts par atpakaļceļa moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ab39f-104">This topic covers breadcrumb modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ab39f-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="ab39f-105">Overview</span></span>

<span data-ttu-id="ab39f-106">Atpakaļceļa moduļi tiek izmantoti, lai nodrošinātu sekundāro navigāciju vietas lapās.</span><span class="sxs-lookup"><span data-stu-id="ab39f-106">Breadcrumb modules are used to provide secondary navigation on site pages.</span></span> <span data-ttu-id="ab39f-107">Parasti tie tiek parādīti lapas augšmalā zem virsraksta.</span><span class="sxs-lookup"><span data-stu-id="ab39f-107">They are typically shown at the top of a page, below the header.</span></span> <span data-ttu-id="ab39f-108">Kaut arī atpakaļceļa moduļus var pievienot jebkurai lapai, tie visbiežāk tiek izmantoti produktu informācijas lapās (PDP), lai parādītu preču kategoriju hierarhiju un nodrošinātu ātru veidu, kā pārvietoties vietnē.</span><span class="sxs-lookup"><span data-stu-id="ab39f-108">Although breadcrumb modules can be added to any page, they are most often used on product details pages (PDPs), to show the product category hierarchy and provide a quick way to move around a site.</span></span> <span data-ttu-id="ab39f-109">Atpakaļceļa moduli var izmantot arī, lai parādītu saiti "Atgriezties pie rezultātiem", kad lietotāji atver PDP no meklēšanas vai saraksta lapas.</span><span class="sxs-lookup"><span data-stu-id="ab39f-109">A breadcrumb module can also be used to show a "Back to results" link when users open a PDP from a search or list page.</span></span> <span data-ttu-id="ab39f-110">Šādā veidā lietotāji var ātri atgriezties filtrētā saraksta lapā, lai turpinātu iepirkšanos.</span><span class="sxs-lookup"><span data-stu-id="ab39f-110">In this way, users can quickly return to their filtered list page to continue shopping.</span></span>

<span data-ttu-id="ab39f-111">Lapās, kurās ir preču kategorijas konteksts, piemēram, PDP un kategoriju lapas, atpakaļceļa moduļi rāda kategoriju hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="ab39f-111">On pages that have product category context, such as PDPs and category pages, breadcrumb modules show the category hierarchy.</span></span> <span data-ttu-id="ab39f-112">Lapās, kurām nav kategorijas konteksta, atpakaļceļa moduļi pēc noklusējuma rāda **&lt;Vietnes sakne&gt; / &lt;Pašreizējā lapa&gt;**.</span><span class="sxs-lookup"><span data-stu-id="ab39f-112">On pages that don't have category context, breadcrumb modules show **&lt;Site root&gt; / &lt;Current page&gt;** by default.</span></span> <span data-ttu-id="ab39f-113">Atpakaļceļa moduļus var arī manuāli konfigurēt citos vietņu lapu veidos, lai parādītu saites uz noteiktām lapām attiecīgajā vietnē.</span><span class="sxs-lookup"><span data-stu-id="ab39f-113">Breadcrumb modules can also be manually configured on other types of site pages to show links to specific pages on the site.</span></span>

> [!NOTE]
> <span data-ttu-id="ab39f-114">Atpakaļceļa modulis ir pieejams Dynamics 365 Commerce 10.0.12 laidienā.</span><span class="sxs-lookup"><span data-stu-id="ab39f-114">The breadcrumb module is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

<span data-ttu-id="ab39f-115">Attēlā zemāk parādīts atpakaļceļa moduļa piemērs, kas parāda kategoriju hierarhiju PDP.</span><span class="sxs-lookup"><span data-stu-id="ab39f-115">The following image shows an example of a breadcrumb module that shows the category hierarchy on a PDP.</span></span>

![Atpakaļceļa moduļa piemērs](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a><span data-ttu-id="ab39f-117">Atpakaļceļa moduļa iestatījumi</span><span class="sxs-lookup"><span data-stu-id="ab39f-117">Breadcrumb module settings</span></span>

<span data-ttu-id="ab39f-118">Atpakaļceļa modulis balstās uz iestatījumu **Atpakaļceļa rādīšanas veids PDP**, kas ir definēts vietnes vietņu veidotājā **Vietnes iestatījumi \> Paplašinājumi**.</span><span class="sxs-lookup"><span data-stu-id="ab39f-118">The breadcrumb module relies on the **Breadcrumb display type on PDP** setting, which is defined at **Site Settings \> Extensions** in site builder.</span></span> <span data-ttu-id="ab39f-119">Šim iestatījumam ir pieejamas trīs vērtības.</span><span class="sxs-lookup"><span data-stu-id="ab39f-119">This setting has three possible values:</span></span>

- <span data-ttu-id="ab39f-120">**Rādīt kategoriju hierarhiju** — ja ir atlasīta šī vērtība, atpakaļceļa modulis parāda pilnu kategoriju hierarhiju precei, kas tiek skatīta PDP.</span><span class="sxs-lookup"><span data-stu-id="ab39f-120">**Show category hierarchy** – When this value is selected, the breadcrumb module will show the full category hierarchy of the product that is viewed on the PDP.</span></span>
- <span data-ttu-id="ab39f-121">**Rādīt atpakaļ pie rezultātiem** — ja atlasīta šī vērtība, atpakaļceļa modulis rādīs "Atpakaļ pie rezultātiem" saiti PDP, ja lietotājs ir atvēris PDP no moduļa, kas ļauj izveidot saiti "Atpakaļ pie rezultātiem".</span><span class="sxs-lookup"><span data-stu-id="ab39f-121">**Show back to results** – When this value is selected, the breadcrumb module will show a "Back to results" link on a PDP if the user opened the PDP from a module that allows for a "Back to results" link.</span></span> <span data-ttu-id="ab39f-122">Šī funkcionalitāte ir pieejama, ja lietotāji veic navigāciju no kategorijas, meklēšanas, saraksta un rekomendāciju saraksta lapas.</span><span class="sxs-lookup"><span data-stu-id="ab39f-122">This functionality is available when users navigate from category, search, list, and recommendation lists pages.</span></span> <span data-ttu-id="ab39f-123">Lai atbalstītu šo funkcionalitāti, preču kolekciju un meklēšanas rezultātu moduļiem ir rekvizīts, kas ir nosaukts **Atļaut atgriešanos pie rezultātiem PDP**.</span><span class="sxs-lookup"><span data-stu-id="ab39f-123">To support this functionality, product collection and search results modules have a property that is named **Allow back to results on PDP**.</span></span> <span data-ttu-id="ab39f-124">Šis rekvizīts sniedz jums elastību, lai definētu, kuriem moduļiem jāatbalsta "Atpakaļ pie rezultātiem" saites funkcionalitāte PDP.</span><span class="sxs-lookup"><span data-stu-id="ab39f-124">This property gives you the flexibility to define which modules should support the "Back to results" link functionality on the PDP.</span></span> <span data-ttu-id="ab39f-125">Piemēram, kad tiek atlasīta opcija **Rādīt atgriešanos pie rezultātiem** atpakaļceļa moduļa iestatījumam **Atpakaļceļa rādīšanas veids PDP**, un opcija **Ļaut atgriezties pie rezultātiem PDP** ir atlasīta meklēšanas lapas meklēšanas rezultātu modulim, saite "Atpakaļ pie rezultātiem" tiks parādīta, kad lietotāji no meklēšanas lapas pāriet uz PDP.</span><span class="sxs-lookup"><span data-stu-id="ab39f-125">For example, when **Show back to results** is selected for the **Breadcrumb display type on PDP** setting of the breadcrumb module, and **Allow back to results on PDP** is selected for the search page search results module, a "Back to results" link will be shown when users navigate from the search page to a PDP.</span></span>
- <span data-ttu-id="ab39f-126">**Rādīt kategoriju hierarhiju un atgriezties pie rezultātiem** — šī vērtība ir iepriekšējo divu vērtību kombinācija.</span><span class="sxs-lookup"><span data-stu-id="ab39f-126">**Show category hierarchy and back to results** – This value is a combination of the previous two.</span></span> <span data-ttu-id="ab39f-127">Atlasot šo vērtību, atpakaļceļa modulis parāda gan pilnu kategoriju hierarhiju, gan saiti "Atgriezties pie rezultātiem" (ja tā ir konfigurēta) PDP.</span><span class="sxs-lookup"><span data-stu-id="ab39f-127">When this value is selected, the breadcrumb module will show both the full category hierarchy and a "Back to results" link (if it's configured) on a PDP.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ab39f-128">Šie iestatījumi ir pieejami Dynamics 365 Commerce 10.0.12 laidienā.</span><span class="sxs-lookup"><span data-stu-id="ab39f-128">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="ab39f-129">Ja veicat atjaunināšanu no vecākas Dynamics 365 Commerce versijas, ir manuāli jāatjaunina fails appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="ab39f-129">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="ab39f-130">Norādījumus par faila appsettings.json atjaunināšanu skatiet [SDK un moduļu bibliotēkas atjauninājumi](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="ab39f-130">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="breadcrumb-module-properties"></a><span data-ttu-id="ab39f-131">Atpakaļceļa moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="ab39f-131">Breadcrumb module properties</span></span>

| <span data-ttu-id="ab39f-132">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="ab39f-132">Property name</span></span> | <span data-ttu-id="ab39f-133">Vērtības</span><span class="sxs-lookup"><span data-stu-id="ab39f-133">Values</span></span> | <span data-ttu-id="ab39f-134">Apraksts</span><span class="sxs-lookup"><span data-stu-id="ab39f-134">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="ab39f-135">Sakne</span><span class="sxs-lookup"><span data-stu-id="ab39f-135">Root</span></span> | <span data-ttu-id="ab39f-136">Teksts vai saite</span><span class="sxs-lookup"><span data-stu-id="ab39f-136">Text or link</span></span>| <span data-ttu-id="ab39f-137">Šis neobligātais rekvizīts norāda saites tekstu un saites mērķi atpakaļceļa vietas saknei.</span><span class="sxs-lookup"><span data-stu-id="ab39f-137">This optional property specifies link text and a link target for the breadcrumb site root.</span></span> <span data-ttu-id="ab39f-138">Ja šis rekvizīts nav konfigurēts, sakne netiks definēta.</span><span class="sxs-lookup"><span data-stu-id="ab39f-138">If this property isn't configured, no root will be defined.</span></span> |
| <span data-ttu-id="ab39f-139">Atpakaļceļa saite</span><span class="sxs-lookup"><span data-stu-id="ab39f-139">Breadcrumb link</span></span> | <span data-ttu-id="ab39f-140">Saistīt</span><span class="sxs-lookup"><span data-stu-id="ab39f-140">Link</span></span> | <span data-ttu-id="ab39f-141">Šis neobligātais rekvizīts norāda saites manuāli konfigurētam atpakaļceļam, ja šīs saites ir nepieciešamas.</span><span class="sxs-lookup"><span data-stu-id="ab39f-141">This optional property specifies links for a manually configured breadcrumb, if these links are required.</span></span> <span data-ttu-id="ab39f-142">Saites parādās tādā secībā, kādā tās ir uzskaitītas.</span><span class="sxs-lookup"><span data-stu-id="ab39f-142">Links appear in the order that they are listed in.</span></span> |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a><span data-ttu-id="ab39f-143">Atpakaļceļa moduļa pievienošana jaunā lapā</span><span class="sxs-lookup"><span data-stu-id="ab39f-143">Add a breadcrumb module to a new page</span></span>

<span data-ttu-id="ab39f-144">Lai pievienotu atpakaļceļa moduli PDP un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="ab39f-144">To add a breadcrumb module to a PDP and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="ab39f-145">Dodieties uz **Vietnes iestatījumi/> paplašinājumi** un pēc tam atlasiet **Rādīt kategoriju hierarhiju** iestatījumam **Atpakaļceļa rādīšanas veids PDP**.</span><span class="sxs-lookup"><span data-stu-id="ab39f-145">Go to **Site Settings /> Extensions**, and then, for the **Breadcrumb display type on PDP** setting, select **Show category hierarchy**.</span></span>
1. <span data-ttu-id="ab39f-146">Atveriet **Veidnes** un atlasiet PDP veidni.</span><span class="sxs-lookup"><span data-stu-id="ab39f-146">Go to **Templates**, and select the PDP template.</span></span>
1. <span data-ttu-id="ab39f-147">Slotā **Konteiners**, kas satur lodziņu pirkšanas lodziņu, atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="ab39f-147">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="ab39f-148">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Atpakaļceļs** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ab39f-148">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="ab39f-149">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="ab39f-149">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="ab39f-150">Dodieties uz **Lapas** un atveriet PDP, kas izmanto PDP veidni.</span><span class="sxs-lookup"><span data-stu-id="ab39f-150">Go to **Pages**, and open a PDP that uses the PDP template.</span></span> <span data-ttu-id="ab39f-151">Ja PDP vēl nepastāv, izveidojiet to.</span><span class="sxs-lookup"><span data-stu-id="ab39f-151">If a PDP doesn't yet exist, create one.</span></span>
1. <span data-ttu-id="ab39f-152">Slotā **Konteiners**, kas satur lodziņu pirkšanas lodziņu, atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="ab39f-152">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="ab39f-153">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Atpakaļceļs** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ab39f-153">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="ab39f-154">Slota **Atpakaļceļš** rekvizītu rūtī sadaļā **Saknes** atlasiet **Saites teksts**.</span><span class="sxs-lookup"><span data-stu-id="ab39f-154">In the properties pane of the **Breadcrumb** slot, under **Root**, select **Link text**.</span></span>
1. <span data-ttu-id="ab39f-155">Dialoglodziņā **Saites teksts** ievadiet **Sākums** un pēc tam sadaļā **Saites mērķis** atlasiet **Pievienot saiti**.</span><span class="sxs-lookup"><span data-stu-id="ab39f-155">In the **Link text** dialog box, enter **Home**, and then, under **Link target**, select **Add a link**.</span></span>
1. <span data-ttu-id="ab39f-156">Dialoglodziņā **Pievienot saiti** atlasiet saiti atpakaļceļa saknei un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ab39f-156">In the **Add a link** dialog box, select a link for the breadcrumb root, and then select **OK**.</span></span>
1. <span data-ttu-id="ab39f-157">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="ab39f-157">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="ab39f-158">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="ab39f-158">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ab39f-159">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ab39f-159">Additional resources</span></span>

[<span data-ttu-id="ab39f-160">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="ab39f-160">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ab39f-161">Noklusējuma kategorijas ielādes lapas un meklēšanas rezultātu lapas apskats</span><span class="sxs-lookup"><span data-stu-id="ab39f-161">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="ab39f-162">Preču kolekcijas moduļi</span><span class="sxs-lookup"><span data-stu-id="ab39f-162">Product collection modules</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="ab39f-163">Pirkšanas lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="ab39f-163">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="ab39f-164">SDK un moduļu bibliotēkas atjauninājumi</span><span class="sxs-lookup"><span data-stu-id="ab39f-164">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
