---
title: Kājenes modulis
description: Šajā tēmā ir aprakstīti kājenes moduļi un kā tos autorēt programmā Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: 51f8d26d6223dcd1f6961058cd9d772a67c69670
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269640"
---
# <a name="footer-module"></a><span data-ttu-id="47fc0-103">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="47fc0-103">Footer module</span></span>  


[!include [banner](includes/banner.md)]

<span data-ttu-id="47fc0-104">Šajā tēmā ir ietverti kājenes moduļi un ir aprakstīts, kā tos izveidot programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="47fc0-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="47fc0-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="47fc0-105">Overview</span></span>

<span data-ttu-id="47fc0-106">Kājenes modulis ir īpašs konteiners, kas tiek izmantots, lai viesotu moduļus, kas parādās lapas kājenē.</span><span class="sxs-lookup"><span data-stu-id="47fc0-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="47fc0-107">Piemēram, tas var ietvert saites uz dažādām lapām visā vietnē, piemēram, lapu **Sazinieties ar mums** un **Veikala politikas**.</span><span class="sxs-lookup"><span data-stu-id="47fc0-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

## <a name="footer-module-properties"></a><span data-ttu-id="47fc0-108">Kājenes moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="47fc0-108">Footer module properties</span></span> 

<span data-ttu-id="47fc0-109">Līdzīgi kā lielākajā daļā konteineru, kājenes modulis atbalsta rekvizītus virsrakstam un platumam.</span><span class="sxs-lookup"><span data-stu-id="47fc0-109">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="47fc0-110">Tas atbalsta arī vairāku kājeņu kategorijas moduļu pievienošanu.</span><span class="sxs-lookup"><span data-stu-id="47fc0-110">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="47fc0-111">Katrs pievienotais kājenes modulis tiek atveidots kā kolonna kājenes modulī.</span><span class="sxs-lookup"><span data-stu-id="47fc0-111">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="47fc0-112">Kājenes modulī pieejamie moduļi</span><span class="sxs-lookup"><span data-stu-id="47fc0-112">Modules available in a footer module</span></span>

<span data-ttu-id="47fc0-113">**Kājenes elementi** — kājenes elementu modulis var ietvert virsrakstu, attēlu un saiti.</span><span class="sxs-lookup"><span data-stu-id="47fc0-113">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="47fc0-114">Virsrakstu var izmantot vai nu atsevišķi, vai kopā ar attēlu un saiti.</span><span class="sxs-lookup"><span data-stu-id="47fc0-114">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="47fc0-115">Katru saiti kājenē var konfigurēt tā, lai tajā būtu tikai teksts (piemēram, saites “Sazinieties ar mums” un “Konfidencialitāte”) vai tā, lai tajā būtu gan teksts, gan attēls (piemēram, sociālo mediju saites).</span><span class="sxs-lookup"><span data-stu-id="47fc0-115">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="47fc0-116">**Atpakaļ uz augšu** – modulis Atpakaļ uz augšu sniedz saiti ātrai navigācijai uz lapas augšdaļu.</span><span class="sxs-lookup"><span data-stu-id="47fc0-116">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="47fc0-117">Ir nepieciešams galamērķis.</span><span class="sxs-lookup"><span data-stu-id="47fc0-117">A destination is required.</span></span> <span data-ttu-id="47fc0-118">Noklusējuma galamērķa vērtība ir #, kas novirza lietotāju uz lapas augšdaļu.</span><span class="sxs-lookup"><span data-stu-id="47fc0-118">The default destination value is #, which takes the user to the top of the page.</span></span>

## <a name="author-a-footer-module"></a><span data-ttu-id="47fc0-119">Kājenes moduļa autorēšana</span><span class="sxs-lookup"><span data-stu-id="47fc0-119">Author a footer module</span></span>

1. <span data-ttu-id="47fc0-120">Navigācijas rūtī atlasiet **Fragmenti** un pēc tam atlasiet **Jaunas lapas fragments**.</span><span class="sxs-lookup"><span data-stu-id="47fc0-120">In the navigation pane, select **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="47fc0-121">Dialoglodziņā **Jaunas lapas fragments** atlasiet kājenes moduli, ievadiet lapas fragmenta nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="47fc0-121">In the **New Page Fragment** dialog box, select the footer module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="47fc0-122">Strukturējuma kokā pa kreisi atlasiet daudzpunktes pogu (**...**) kājenes modulim un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="47fc0-122">In the outline tree on the left, select the ellipsis button (**...**) for the footer module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="47fc0-123">Dialoglodziņā **Pievienot moduli** atlasiet kājenes kategorijas moduli un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="47fc0-123">In the **Add Module** dialog box, select the footer category module, and then select **OK**.</span></span>
1. <span data-ttu-id="47fc0-124">Strukturējuma kokā atlasiet daudzpunktes pogu kājenes kategorijas modulim un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="47fc0-124">In the outline tree, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="47fc0-125">Dialoglodziņā **Pievienot moduli** atlasiet kājenes elementa moduli un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="47fc0-125">In the **Add Module** dialog box, select the footer item module, and then select **OK**.</span></span>
1. <span data-ttu-id="47fc0-126">Struktūras kokā atlasiet kājenes elementa moduli.</span><span class="sxs-lookup"><span data-stu-id="47fc0-126">In the outline tree, select the footer item module.</span></span> <span data-ttu-id="47fc0-127">Pēc tam rekvizītu rūtī labajā pusē pēc nepieciešamības konfigurējiet virsrakstu, saiti, saites tekstu un attēlu.</span><span class="sxs-lookup"><span data-stu-id="47fc0-127">Then, in the properties pane on the right, configure the heading, link and link text, and image as you require.</span></span>
1. <span data-ttu-id="47fc0-128">Pievienojiet vairāk kājenes elementu, atkārtojiet darbības, sākot no 5. līdz 7. darbībai</span><span class="sxs-lookup"><span data-stu-id="47fc0-128">To add more footer items, repeat steps 5 through 7.</span></span>
1. <span data-ttu-id="47fc0-129">Lai kājenei pievienotu saiti “atpakaļ uz augšu”, atlasiet daudzpunktes pogu kājenes kategorijas modulim un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="47fc0-129">To add a "back to top" link to your footer, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="47fc0-130">Dialoglodziņā **Pievienot moduli** atlasiet moduli Atpakaļ uz augšu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="47fc0-130">In the **Add Module** dialog box, select the back to top module, and then select **OK**.</span></span>
1. <span data-ttu-id="47fc0-131">Struktūras kokā atlasiet moduli Atpakaļ uz augšu.</span><span class="sxs-lookup"><span data-stu-id="47fc0-131">In the outline tree, select the back to top module.</span></span> <span data-ttu-id="47fc0-132">Pēc tam rekvizītu rūtī labajā pusē pēc nepieciešamības konfigurējiet moduli Atpakaļ uz augšu.</span><span class="sxs-lookup"><span data-stu-id="47fc0-132">Then, in the properties pane on the right, configure the back to top module as you require.</span></span>
1. <span data-ttu-id="47fc0-133">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapas fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="47fc0-133">Select **Save**, select **Finish editing** to check in the page fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="47fc0-134">Katrā lapas veidnē, kas izveidota vietnei, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="47fc0-134">On every page template that has been created for the site, follow these steps.</span></span>

1. <span data-ttu-id="47fc0-135">Kājenes modulī noklusējuma lapas **Galvenajā** slotā pievienojiet jūsu izveidoto kājenes fragmentu.</span><span class="sxs-lookup"><span data-stu-id="47fc0-135">In the **Main** slot of the default page, in the footer module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="47fc0-136">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="47fc0-136">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="47fc0-137">Pievienojot lapas fragmentu lapu veidnēm, jūs palīdzēsiet nodrošināt, ka kājene tiek atveidota katrā lapā.</span><span class="sxs-lookup"><span data-stu-id="47fc0-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="47fc0-138">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="47fc0-138">Additional resources</span></span>

[<span data-ttu-id="47fc0-139">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="47fc0-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="47fc0-140">Container modulis</span><span class="sxs-lookup"><span data-stu-id="47fc0-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="47fc0-141">Iegādes lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="47fc0-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="47fc0-142">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="47fc0-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="47fc0-143">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="47fc0-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="47fc0-144">Pasūtījuma apstiprinājuma modelis</span><span class="sxs-lookup"><span data-stu-id="47fc0-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="47fc0-145">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="47fc0-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="47fc0-146">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="47fc0-146">Footer module</span></span>](author-footer-module.md)
