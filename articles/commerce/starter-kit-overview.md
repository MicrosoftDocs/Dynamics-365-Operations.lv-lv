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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: fcb0c2317315308de51d8247d23a930f10c3de6f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234297"
---
# <a name="module-library-overview"></a><span data-ttu-id="eb6c4-103">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="eb6c4-103">Module library overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="eb6c4-104">Šajā tēmā ir sniegts apskats par Microsoft Dynamics 365 Commerce moduļu bibliotēku.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-104">This topic presents an overview of the Microsoft Dynamics 365 Commerce module library.</span></span>

<span data-ttu-id="eb6c4-105">Dynamics 365 Commerce moduļu bibliotēka ir moduļu kopums, ko var izmantot, lai izveidotu e-komercijas vietni.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-105">The Dynamics 365 Commerce module library is a collection of modules that can be used to build an e-Commerce website.</span></span> <span data-ttu-id="eb6c4-106">Moduļos ir gan lietotāja interfeisa (UI) aspekti, gan funkcionālās uzvedības aspekti.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-106">Modules have both user interface (UI) aspects and functional behavior aspects.</span></span>

<span data-ttu-id="eb6c4-107">Tēmas var lietot moduļu bibliotēkas moduļiem, lai mainītu to izskatu un iespaidu.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-107">Themes can be applied to the modules in the module library to change their look and feel.</span></span> <span data-ttu-id="eb6c4-108">Tēmas izmanto stila lapas kaskadēšanu (CSS).</span><span class="sxs-lookup"><span data-stu-id="eb6c4-108">The themes use Cascading Style Sheets (CSS).</span></span> <span data-ttu-id="eb6c4-109">Fiktīvas e-komercijas vietnes, kuras nosaukums ir “Fabrikam”, dizains tiek sniegts kā moduļu bibliotēkas daļa, un to var izmantot kā atsauci.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-109">A theme for a fictitious e-Commerce site that is named "Fabrikam" is provided as part of the module library and can be used as a reference.</span></span>

## <a name="module-library-modules"></a><span data-ttu-id="eb6c4-110">Moduļu bibliotēkas moduļi</span><span class="sxs-lookup"><span data-stu-id="eb6c4-110">Module library modules</span></span>

<span data-ttu-id="eb6c4-111">Moduļu bibliotēkā ir iekļauti tālāk norādītie moduļu tipi:</span><span class="sxs-lookup"><span data-stu-id="eb6c4-111">The following types of modules are provided in the module library:</span></span>

- <span data-ttu-id="eb6c4-112">**Konteinera modulis** — konteinera modulis ir vienkāršs modulis, kas darbojas kā resursdators citiem moduļiem.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-112">**Container module** – A container module is a simple module that acts as a host for other modules.</span></span> <span data-ttu-id="eb6c4-113">Tas kontrolē moduļu izkārtojumu, kas atrodas tajā.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-113">It controls the layout of the modules that are inside it.</span></span>
- <span data-ttu-id="eb6c4-114">**Mārketinga moduļi** — mārketinga moduļi ietver satura bloka, teksta bloka, video atskaņotāja un karuseļa moduļus.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-114">**Marketing modules** – Marketing modules include content block, text block, video player, and carousel modules.</span></span> <span data-ttu-id="eb6c4-115">Visus šos moduļus var izmantot, lai parādītu saturu.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-115">All these modules can be used to showcase content.</span></span> <span data-ttu-id="eb6c4-116">Tos var ievietot jebkurā lapā un tos vada dati no Satura pārvaldības sistēmas (CMS), un tos var ievietot jebkurā lapā.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-116">They can be put on any page and are driven by data from the content management system (CMS).</span></span>
- <span data-ttu-id="eb6c4-117">**Galveņu un kājeņu moduļi** — galveņu un kājeņu moduļi ir redzami visu vietnes lapu galvenē un kājenē.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-117">**Header and footer modules** – Header and footer modules appear in the header and footer of all site pages.</span></span> <span data-ttu-id="eb6c4-118">Šos moduļus var konfigurēt pēc nepieciešamības, izmantojot rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-118">These modules can be configured as required through properties.</span></span>
- <span data-ttu-id="eb6c4-119">**Meklēšanas moduļi** — preces var skatīt, izmantojot meklēšanas moduli galvenē.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-119">**Search modules** – Products can be discovered by using the search module in the header.</span></span> <span data-ttu-id="eb6c4-120">Meklēšanas rezultāti parādās meklēšanas rezultātu lapā.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-120">Search results appear on the search results page.</span></span> <span data-ttu-id="eb6c4-121">Preces var skatīt arī kategorijas lapās, kas ir paredzētas katrai kategorijai, kas tiek atbalstīta kanāla navigācijas hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-121">Products can also be discovered on category pages, which are dedicated pages for each category that is supported in the channel navigation hierarchy.</span></span> <span data-ttu-id="eb6c4-122">Turklāt precizētos moduļus var izmantot, lai turpmāk filtrētu rezultātus meklēšanas rezultātos un kategoriju lapās.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-122">In addition, refiner modules can be used to further filter results on search results and category pages.</span></span>
- <span data-ttu-id="eb6c4-123">**Preces detalizētas informācijas lapas moduļi** — preces detalizētas informācijas lapas izmanto vairākus moduļus, lai parādītu preces informāciju.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-123">**Product details page modules** – Product details pages use several modules to show product information.</span></span> <span data-ttu-id="eb6c4-124">Pirkšanas kastes modulis ļauj klientiem skatīt preces un pievienot tās grozam.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-124">The buy box module lets customers view products and add them to the cart.</span></span> <span data-ttu-id="eb6c4-125">Citi moduļi, piemēram, tehniskās specifikācijas modulis parāda informāciju par preci.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-125">Other modules, such as the tech specs module, show the product details.</span></span> <span data-ttu-id="eb6c4-126">Vērtējumu un pārskatu moduli var izmantot, lai apskatītu un sniegtu pārskatus.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-126">The ratings and reviews module can used to view and provide reviews.</span></span>
- <span data-ttu-id="eb6c4-127">**Modulis Pirkt tiešsaistē un paņemt veikalā** — šis modulis ir integrēts ar Bing kartēm.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-127">**Buy online pick up in store module** – The buy online pick up in store module is integrated with Bing Maps.</span></span> <span data-ttu-id="eb6c4-128">To var izmantot, lai atrastu tuvumā esošos veikalus, kuros klienti var saņemt preces, ko tie iegādājušies.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-128">It can be used to find nearby stores where customers can pick up products that they have purchased.</span></span>
- <span data-ttu-id="eb6c4-129">**Pirkšanas moduļi** — pirkšanas moduļi ietver iepirkumu grozu moduli, ko var izmantot, lai pievienotu vienumus grozam.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-129">**Purchase modules** – Purchase modules include the cart module, which can be used to add items to the cart.</span></span> <span data-ttu-id="eb6c4-130">Norēķināšanās modulī tiek ietverta piegādes adrese, piegādes opcijas, dāvanu karte, lojalitātes programma un kredītkartes informācija, lai varētu apstrādāt pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-130">The checkout module captures the shipping address, delivery options, and gift card, loyalty program, and credit card information, so that an order can be processed.</span></span> <span data-ttu-id="eb6c4-131">Pēc tam, kad pasūtījums ir veikts, var izmantot pasūtījuma apstiprināšanas moduli, lai parādītu detalizētu informāciju par apstiprinājumu.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-131">After an order is placed, the order confirmation module can be used to show the confirmation details.</span></span>
- <span data-ttu-id="eb6c4-132">**Konta pārvaldības moduļi** — pierakstīšanās modulis ļaut klientiem pieteikties esošā kontā, un reģistrēšanās modulis ļauj izveidot jaunu kontu.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-132">**Account management modules** – The sign-in module lets customers sign in to an existing account, and the sign-up module lets them create a new account.</span></span> <span data-ttu-id="eb6c4-133">Kad konts ir izveidots, pasūtījumu vēstures modulis var tikt izmantots neseno pasūtījumu apskatīšanai, un pasūtījuma informācijas modulis var tikt izmantots pasūtījuma informācijas skatīšanai.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-133">After an account is created, the order history module can be used to view recent orders, and the order details module can be used to view order details.</span></span>
- <span data-ttu-id="eb6c4-134">**Ieteikumu modulis** — ieteikumi tiek parādīti, izmantojot preču izvietošanas moduli.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-134">**Recommendations module** – Recommendations are shown by using the product placement module.</span></span> <span data-ttu-id="eb6c4-135">Šis modulis atbalsta algoritmiskos un redakcijas sarakstus, kas var tikt izrādīti jebkurā lapā.</span><span class="sxs-lookup"><span data-stu-id="eb6c4-135">This module supports algorithmic and editorial lists that can be showcased on any page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eb6c4-136">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="eb6c4-136">Additional resources</span></span>

[<span data-ttu-id="eb6c4-137">Container modulis</span><span class="sxs-lookup"><span data-stu-id="eb6c4-137">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="eb6c4-138">Pirkšanas lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="eb6c4-138">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="eb6c4-139">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="eb6c4-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="eb6c4-140">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="eb6c4-140">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="eb6c4-141">Pasūtījuma apstiprinājuma modelis</span><span class="sxs-lookup"><span data-stu-id="eb6c4-141">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="eb6c4-142">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="eb6c4-142">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="eb6c4-143">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="eb6c4-143">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]