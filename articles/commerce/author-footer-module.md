---
title: Kājenes modulis
description: Šajā tēmā ir aprakstīti kājenes moduļi un kā tos autorēt programmā Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6dd9f214fbeeeaabadac4853916363c20a3288ca
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761205"
---
# <a name="footer-module"></a><span data-ttu-id="1b444-103">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="1b444-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="1b444-104">Šajā tēmā ir ietverti kājenes moduļi un ir aprakstīts, kā tos izveidot programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1b444-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1b444-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="1b444-105">Overview</span></span>

<span data-ttu-id="1b444-106">Kājenes modulis ir īpašs konteiners, kas tiek izmantots, lai viesotu moduļus, kas parādās lapas kājenē.</span><span class="sxs-lookup"><span data-stu-id="1b444-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="1b444-107">Piemēram, tas var ietvert saites uz dažādām lapām visā vietnē, piemēram, lapu **Sazinieties ar mums** un **Veikala politikas**.</span><span class="sxs-lookup"><span data-stu-id="1b444-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="1b444-108">Attēlā zemāk redzams kājenes moduļa piemērs vietas lapā.</span><span class="sxs-lookup"><span data-stu-id="1b444-108">The following image shows an example of a footer module on a site page.</span></span>

![Kājenes moduļa piemērs](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="1b444-110">Kājenes moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="1b444-110">Footer module properties</span></span> 

<span data-ttu-id="1b444-111">Līdzīgi kā lielākajā daļā konteineru, kājenes modulis atbalsta rekvizītus virsrakstam un platumam.</span><span class="sxs-lookup"><span data-stu-id="1b444-111">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="1b444-112">Tas atbalsta arī vairāku kājeņu kategorijas moduļu pievienošanu.</span><span class="sxs-lookup"><span data-stu-id="1b444-112">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="1b444-113">Katrs pievienotais kājenes modulis tiek atveidots kā kolonna kājenes modulī.</span><span class="sxs-lookup"><span data-stu-id="1b444-113">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="1b444-114">Kājenes modulī pieejamie moduļi</span><span class="sxs-lookup"><span data-stu-id="1b444-114">Modules available in a footer module</span></span>

<span data-ttu-id="1b444-115">**Kājenes elementi** — kājenes elementu modulis var ietvert virsrakstu, attēlu un saiti.</span><span class="sxs-lookup"><span data-stu-id="1b444-115">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="1b444-116">Virsrakstu var izmantot vai nu atsevišķi, vai kopā ar attēlu un saiti.</span><span class="sxs-lookup"><span data-stu-id="1b444-116">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="1b444-117">Katru saiti kājenē var konfigurēt tā, lai tajā būtu tikai teksts (piemēram, saites “Sazinieties ar mums” un “Konfidencialitāte”) vai tā, lai tajā būtu gan teksts, gan attēls (piemēram, sociālo mediju saites).</span><span class="sxs-lookup"><span data-stu-id="1b444-117">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="1b444-118">**Atpakaļ uz augšu** – modulis Atpakaļ uz augšu sniedz saiti ātrai navigācijai uz lapas augšdaļu.</span><span class="sxs-lookup"><span data-stu-id="1b444-118">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="1b444-119">Ir nepieciešams galamērķis.</span><span class="sxs-lookup"><span data-stu-id="1b444-119">A destination is required.</span></span> <span data-ttu-id="1b444-120">Noklusējuma galamērķa vērtība ir \#, kas novirza lietotāju uz lapas augšdaļu.</span><span class="sxs-lookup"><span data-stu-id="1b444-120">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="1b444-121">Kājenes moduļa izveide</span><span class="sxs-lookup"><span data-stu-id="1b444-121">Create a footer module</span></span>

1. <span data-ttu-id="1b444-122">Dodieties uz **Fragmenti** un atlasiet **Jauns**, lai izveidotu jaunu fragmentu.</span><span class="sxs-lookup"><span data-stu-id="1b444-122">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="1b444-123">Dialoglodziņā **Jauns fragments** atlasiet moduli **Konteiners**, ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1b444-123">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="1b444-124">Slotā **Noklusējuma konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="1b444-124">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1b444-125">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Kājenes kategorija** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1b444-125">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1b444-126">Slotā **Kājenes kategorija** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="1b444-126">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1b444-127">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Kājenes elements** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1b444-127">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1b444-128">Atlasiet slotu **Kājenes elements** un pēc tam rekvizītu rūtī labajā pusē pēc nepieciešamības konfigurējiet virsrakstu, saiti, saites tekstu un attēlu.</span><span class="sxs-lookup"><span data-stu-id="1b444-128">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="1b444-129">Pievienojiet vairāk kājenes elementu, katram atkārtojot darbības, sākot no 5. līdz 7. darbībai.</span><span class="sxs-lookup"><span data-stu-id="1b444-129">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="1b444-130">Lai kājenei pievienotu saiti “atpakaļ uz augšu”, atlasiet daudzpunkti (**...**) slotā **Kājenes kategorija** un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="1b444-130">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="1b444-131">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Atpakaļ uz augšu** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1b444-131">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1b444-132">Atlasiet slotu **Atpakaļ uz augšu** un pēc tam rekvizītu rūtī labajā pusē pēc nepieciešamības konfigurējiet tekstu un citus moduļa rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="1b444-132">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="1b444-133">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="1b444-133">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="1b444-134">Lai palīdzētu nodrošināt, ka galvene parādās katrā lapā, veiciet šīs darbības katrā lapas veidnē, kas tiek izveidota šai vietnei.</span><span class="sxs-lookup"><span data-stu-id="1b444-134">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="1b444-135">Moduļa **Noklusējuma lapa** slotā **Kājene** pievienojiet jūsu izveidoto kājenes fragmentu.</span><span class="sxs-lookup"><span data-stu-id="1b444-135">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="1b444-136">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="1b444-136">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="1b444-137">Pievienojot fragmentu lapu veidnēm, jūs palīdzēsiet nodrošināt, ka kājene tiek atveidota katrā lapā.</span><span class="sxs-lookup"><span data-stu-id="1b444-137">By adding the fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1b444-138">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="1b444-138">Additional resources</span></span>

[<span data-ttu-id="1b444-139">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="1b444-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1b444-140">Container modulis</span><span class="sxs-lookup"><span data-stu-id="1b444-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="1b444-141">Iegādes lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="1b444-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="1b444-142">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="1b444-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="1b444-143">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="1b444-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="1b444-144">Pasūtījuma apstiprinājuma modelis</span><span class="sxs-lookup"><span data-stu-id="1b444-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="1b444-145">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="1b444-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="1b444-146">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="1b444-146">Footer module</span></span>](author-footer-module.md)
