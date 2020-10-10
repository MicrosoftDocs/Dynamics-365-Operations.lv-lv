---
title: Moduļu bibliotēkas pārskats
description: Šajā tēmā ir sniegts apskats par Microsoft Dynamics 365 Commerce moduļu bibliotēku.
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
ms.openlocfilehash: dfc52dd8e14bb2e9f2f9c026ee0e058aee4cedcb
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817830"
---
# <a name="module-library-overview"></a><span data-ttu-id="99ddd-103">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="99ddd-103">Module library overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="99ddd-104">Šajā tēmā ir sniegts apskats par Microsoft Dynamics 365 Commerce moduļu bibliotēku.</span><span class="sxs-lookup"><span data-stu-id="99ddd-104">This topic presents an overview of the Microsoft Dynamics 365 Commerce module library.</span></span>

## <a name="overview"></a><span data-ttu-id="99ddd-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="99ddd-105">Overview</span></span>

<span data-ttu-id="99ddd-106">Dynamics 365 Commerce moduļu bibliotēka ir moduļu kopums, ko var izmantot, lai izveidotu e-komercijas vietni.</span><span class="sxs-lookup"><span data-stu-id="99ddd-106">The Dynamics 365 Commerce module library is a collection of modules that can be used to build an e-Commerce website.</span></span> <span data-ttu-id="99ddd-107">Moduļos ir gan lietotāja interfeisa (UI) aspekti, gan funkcionālās uzvedības aspekti.</span><span class="sxs-lookup"><span data-stu-id="99ddd-107">Modules have both user interface (UI) aspects and functional behavior aspects.</span></span>

<span data-ttu-id="99ddd-108">Tēmas var lietot moduļu bibliotēkas moduļiem, lai mainītu to izskatu un iespaidu.</span><span class="sxs-lookup"><span data-stu-id="99ddd-108">Themes can be applied to the modules in the module library to change their look and feel.</span></span> <span data-ttu-id="99ddd-109">Tēmas izmanto stila lapas kaskadēšanu (CSS).</span><span class="sxs-lookup"><span data-stu-id="99ddd-109">The themes use Cascading Style Sheets (CSS).</span></span> <span data-ttu-id="99ddd-110">Fiktīvas e-komercijas vietnes, kuras nosaukums ir “Fabrikam”, dizains tiek sniegts kā moduļu bibliotēkas daļa, un to var izmantot kā atsauci.</span><span class="sxs-lookup"><span data-stu-id="99ddd-110">A theme for a fictitious e-Commerce site that is named "Fabrikam" is provided as part of the module library and can be used as a reference.</span></span>

## <a name="module-library-modules"></a><span data-ttu-id="99ddd-111">Moduļu bibliotēkas moduļi</span><span class="sxs-lookup"><span data-stu-id="99ddd-111">Module library modules</span></span>

<span data-ttu-id="99ddd-112">Moduļu bibliotēkā ir iekļauti tālāk norādītie moduļu tipi:</span><span class="sxs-lookup"><span data-stu-id="99ddd-112">The following types of modules are provided in the module library:</span></span>

- <span data-ttu-id="99ddd-113">**Konteinera modulis** — konteinera modulis ir vienkāršs modulis, kas darbojas kā resursdators citiem moduļiem.</span><span class="sxs-lookup"><span data-stu-id="99ddd-113">**Container module** – A container module is a simple module that acts as a host for other modules.</span></span> <span data-ttu-id="99ddd-114">Tas kontrolē moduļu izkārtojumu, kas atrodas tajā.</span><span class="sxs-lookup"><span data-stu-id="99ddd-114">It controls the layout of the modules that are inside it.</span></span>
- <span data-ttu-id="99ddd-115">**Mārketinga moduļi** — mārketinga moduļi ietver satura bloka, teksta bloka, video atskaņotāja un karuseļa moduļus.</span><span class="sxs-lookup"><span data-stu-id="99ddd-115">**Marketing modules** – Marketing modules include content block, text block, video player, and carousel modules.</span></span> <span data-ttu-id="99ddd-116">Visus šos moduļus var izmantot, lai parādītu saturu.</span><span class="sxs-lookup"><span data-stu-id="99ddd-116">All these modules can be used to showcase content.</span></span> <span data-ttu-id="99ddd-117">Tos var ievietot jebkurā lapā un tos vada dati no Satura pārvaldības sistēmas (CMS), un tos var ievietot jebkurā lapā.</span><span class="sxs-lookup"><span data-stu-id="99ddd-117">They can be put on any page and are driven by data from the content management system (CMS).</span></span>
- <span data-ttu-id="99ddd-118">**Galveņu un kājeņu moduļi** — galveņu un kājeņu moduļi ir redzami visu vietnes lapu galvenē un kājenē.</span><span class="sxs-lookup"><span data-stu-id="99ddd-118">**Header and footer modules** – Header and footer modules appear in the header and footer of all site pages.</span></span> <span data-ttu-id="99ddd-119">Šos moduļus var konfigurēt pēc nepieciešamības, izmantojot rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="99ddd-119">These modules can be configured as required through properties.</span></span>
- <span data-ttu-id="99ddd-120">**Meklēšanas moduļi** — preces var skatīt, izmantojot meklēšanas moduli galvenē.</span><span class="sxs-lookup"><span data-stu-id="99ddd-120">**Search modules** – Products can be discovered by using the search module in the header.</span></span> <span data-ttu-id="99ddd-121">Meklēšanas rezultāti parādās meklēšanas rezultātu lapā.</span><span class="sxs-lookup"><span data-stu-id="99ddd-121">Search results appear on the search results page.</span></span> <span data-ttu-id="99ddd-122">Preces var skatīt arī kategorijas lapās, kas ir paredzētas katrai kategorijai, kas tiek atbalstīta kanāla navigācijas hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="99ddd-122">Products can also be discovered on category pages, which are dedicated pages for each category that is supported in the channel navigation hierarchy.</span></span> <span data-ttu-id="99ddd-123">Turklāt precizētos moduļus var izmantot, lai turpmāk filtrētu rezultātus meklēšanas rezultātos un kategoriju lapās.</span><span class="sxs-lookup"><span data-stu-id="99ddd-123">In addition, refiner modules can be used to further filter results on search results and category pages.</span></span>
- <span data-ttu-id="99ddd-124">**Preces detalizētas informācijas lapas moduļi** — preces detalizētas informācijas lapas izmanto vairākus moduļus, lai parādītu preces informāciju.</span><span class="sxs-lookup"><span data-stu-id="99ddd-124">**Product details page modules** – Product details pages use several modules to show product information.</span></span> <span data-ttu-id="99ddd-125">Pirkšanas kastes modulis ļauj klientiem skatīt preces un pievienot tās grozam.</span><span class="sxs-lookup"><span data-stu-id="99ddd-125">The buy box module lets customers view products and add them to the cart.</span></span> <span data-ttu-id="99ddd-126">Citi moduļi, piemēram, tehniskās specifikācijas modulis parāda informāciju par preci.</span><span class="sxs-lookup"><span data-stu-id="99ddd-126">Other modules, such as the tech specs module, show the product details.</span></span> <span data-ttu-id="99ddd-127">Vērtējumu un pārskatu moduli var izmantot, lai apskatītu un sniegtu pārskatus.</span><span class="sxs-lookup"><span data-stu-id="99ddd-127">The ratings and reviews module can used to view and provide reviews.</span></span>
- <span data-ttu-id="99ddd-128">**Modulis Pirkt tiešsaistē un paņemt veikalā** — šis modulis ir integrēts ar Bing kartēm.</span><span class="sxs-lookup"><span data-stu-id="99ddd-128">**Buy online pick up in store module** – The buy online pick up in store module is integrated with Bing Maps.</span></span> <span data-ttu-id="99ddd-129">To var izmantot, lai atrastu tuvumā esošos veikalus, kuros klienti var saņemt preces, ko tie iegādājušies.</span><span class="sxs-lookup"><span data-stu-id="99ddd-129">It can be used to find nearby stores where customers can pick up products that they have purchased.</span></span>
- <span data-ttu-id="99ddd-130">**Pirkšanas moduļi** — pirkšanas moduļi ietver iepirkumu grozu moduli, ko var izmantot, lai pievienotu vienumus grozam.</span><span class="sxs-lookup"><span data-stu-id="99ddd-130">**Purchase modules** – Purchase modules include the cart module, which can be used to add items to the cart.</span></span> <span data-ttu-id="99ddd-131">Norēķināšanās modulī tiek ietverta piegādes adrese, piegādes opcijas, dāvanu karte, lojalitātes programma un kredītkartes informācija, lai varētu apstrādāt pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="99ddd-131">The checkout module captures the shipping address, delivery options, and gift card, loyalty program, and credit card information, so that an order can be processed.</span></span> <span data-ttu-id="99ddd-132">Pēc tam, kad pasūtījums ir veikts, var izmantot pasūtījuma apstiprināšanas moduli, lai parādītu detalizētu informāciju par apstiprinājumu.</span><span class="sxs-lookup"><span data-stu-id="99ddd-132">After an order is placed, the order confirmation module can be used to show the confirmation details.</span></span>
- <span data-ttu-id="99ddd-133">**Konta pārvaldības moduļi** — pierakstīšanās modulis ļaut klientiem pieteikties esošā kontā, un reģistrēšanās modulis ļauj izveidot jaunu kontu.</span><span class="sxs-lookup"><span data-stu-id="99ddd-133">**Account management modules** – The sign-in module lets customers sign in to an existing account, and the sign-up module lets them create a new account.</span></span> <span data-ttu-id="99ddd-134">Kad konts ir izveidots, pasūtījumu vēstures modulis var tikt izmantots neseno pasūtījumu apskatīšanai, un pasūtījuma informācijas modulis var tikt izmantots pasūtījuma informācijas skatīšanai.</span><span class="sxs-lookup"><span data-stu-id="99ddd-134">After an account is created, the order history module can be used to view recent orders, and the order details module can be used to view order details.</span></span>
- <span data-ttu-id="99ddd-135">**Ieteikumu modulis** — ieteikumi tiek parādīti, izmantojot preču izvietošanas moduli.</span><span class="sxs-lookup"><span data-stu-id="99ddd-135">**Recommendations module** – Recommendations are shown by using the product placement module.</span></span> <span data-ttu-id="99ddd-136">Šis modulis atbalsta algoritmiskos un redakcijas sarakstus, kas var tikt izrādīti jebkurā lapā.</span><span class="sxs-lookup"><span data-stu-id="99ddd-136">This module supports algorithmic and editorial lists that can be showcased on any page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="99ddd-137">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="99ddd-137">Additional resources</span></span>

[<span data-ttu-id="99ddd-138">Container modulis</span><span class="sxs-lookup"><span data-stu-id="99ddd-138">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="99ddd-139">Pirkšanas lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="99ddd-139">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="99ddd-140">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="99ddd-140">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="99ddd-141">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="99ddd-141">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="99ddd-142">Pasūtījuma apstiprinājuma modelis</span><span class="sxs-lookup"><span data-stu-id="99ddd-142">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="99ddd-143">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="99ddd-143">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="99ddd-144">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="99ddd-144">Footer module</span></span>](author-footer-module.md)
