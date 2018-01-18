---
title: "Zvanu centra funkcionalitāte"
description: "Šajā tēmā ir sniegts pārskats par zvanu centra pārdošanas funkcionalitāti programmā Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 55bad891f9295eca6b0bf39847ede890b7294370
ms.contentlocale: lv-lv
ms.lasthandoff: 01/17/2018

---

# <a name="call-center-functionality"></a><span data-ttu-id="a5afe-103">Zvanu centra funkcionalitāte</span><span class="sxs-lookup"><span data-stu-id="a5afe-103">Call center functionality</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="a5afe-104">Šajā rakstā ir sniegts pārskats par zvanu centra pārdošanas funkcionalitāti programmatūrā Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="a5afe-104">This article provides an overview of the call center sales functionality in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="a5afe-105">Programmatūra Dynamics 365 for Retail atbalsta zvanu centru izmantošanu kā mazumtirdzniecības kanāla veidu.</span><span class="sxs-lookup"><span data-stu-id="a5afe-105">Dynamics 365 for Retail supports call centers as a type of retail channel.</span></span> <span data-ttu-id="a5afe-106">Zvanu centrā darbinieki pa tālruni no klientiem saņem pasūtījumus un izveido pārdošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="a5afe-106">In a call center, workers take orders from customers over the phone and create sales orders.</span></span> <span data-ttu-id="a5afe-107">Zvanu centra funkcionalitāte ietver līdzekļus, kas ir veidoti ar mērķi vienkāršot tālruņa pasūtījumu pieņemšanu un debitoru pakalpojumu nodrošināšanu visā pasūtījumu izpildes procesā.</span><span class="sxs-lookup"><span data-stu-id="a5afe-107">Call center functionality includes features that are designed to make it easier to take phone orders and handle customer service throughout the order fulfillment process.</span></span> <span data-ttu-id="a5afe-108">Piemēram, zvanu centra darbinieki var ievadīt maksājuma informāciju tieši pārdošanas pasūtījumā, un var apskatīt detalizētu izmaksu un maksājumu kopsavilkumu, pirms viņi iesniedz pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="a5afe-108">For example, call center workers can enter payment information directly into the sales order, and can view a detailed summary of charges and payments before they submit the order.</span></span> <span data-ttu-id="a5afe-109">Darbiniekiem ir iespējas kontrolēt izcenojumu, un no **Pārdošanas pasūtījuma** formas viņi var piekļūt dažādai informācijai par debitoriem, precēm un cenām.</span><span class="sxs-lookup"><span data-stu-id="a5afe-109">Workers also have options for controlling pricing, and can access various data about customers, products, and prices from the **Sales order** page.</span></span> <span data-ttu-id="a5afe-110">Zvanu centriem ir arī uzlabota funkcionalitāte debitoru vēstures un pasūtījuma statusa izsekošanai.</span><span class="sxs-lookup"><span data-stu-id="a5afe-110">Additionally, call centers have enhanced functionality for tracking customer history and order status.</span></span> <span data-ttu-id="a5afe-111">Katram zvanu centram var būt savi lietotāji, maksājuma metodes, cenu grupas, finanšu dimensijas un piegādes veidi.</span><span class="sxs-lookup"><span data-stu-id="a5afe-111">Each call center can have its own users, payment methods, price groups, financial dimensions, and modes of delivery.</span></span> <span data-ttu-id="a5afe-112">Šīs opcijas var konfigurēt zvanu centra izveides brīdī.</span><span class="sxs-lookup"><span data-stu-id="a5afe-112">You can configure these options when you create the call center.</span></span> <span data-ttu-id="a5afe-113">Turklāt varat izmantot lapu **Zvanu centrs**, lai iespējotu vai atspējotu šādas līdzekļu grupas, kas ir unikālas zvanu centriem:</span><span class="sxs-lookup"><span data-stu-id="a5afe-113">Additionally, you can use the **Call center** page to enable or disable the following groups of features that are unique to call centers:</span></span>

-   <span data-ttu-id="a5afe-114">**Pasūtījuma veikšana** – šajā grupā iekļauti līdzekļi, kas attiecas uz maksājumiem un pasūtījuma pabeigšanu lapā **Pārdošanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="a5afe-114">**Order completion** – This group includes features that are related to payments and order completion on the **Sales order** page.</span></span>
-   <span data-ttu-id="a5afe-115">**Vadītā pārdošana** – šajā grupā ir iekļauti līdzekļi, kas saistīti ar pirmkodiem, skriptiem un kataloga pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="a5afe-115">**Directed selling** – This group includes features that are related to source codes, scripts, and catalog requests.</span></span>

<span data-ttu-id="a5afe-116">Iespējojot šos līdzekļus zvanu centra iestatījumos, lapā **Pārdošanas pasūtījums** tie ir pieejami lietotājiem, kuri ir saistīti ar šo zvanu centru.</span><span class="sxs-lookup"><span data-stu-id="a5afe-116">After you enable these features in the call center settings, they are available on the **Sales order** page to users who are associated with the call center.</span></span> <span data-ttu-id="a5afe-117">Lielākai daļai no šiem līdzekļiem pirms to izmantošanas nepieciešami papildu iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="a5afe-117">Most of these features require additional setup before they can be used.</span></span> <span data-ttu-id="a5afe-118">Pirms lietotāji var izveidot zvanu centra pasūtījumus, jums šie lietotāji ir jāpievieno zvanu centram kā zvanu centra lietotājus.</span><span class="sxs-lookup"><span data-stu-id="a5afe-118">Before users can create call center orders, you must add those users to the call center as call center users.</span></span> <span data-ttu-id="a5afe-119">Šis solis iespējo zvanu centra kanālam raksturīgu konfigurāciju un funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="a5afe-119">This step enables the call center channel-specific configuration and functionality.</span></span> <span data-ttu-id="a5afe-120">Daži funkcionalitātes piemēri, kas kļūst pieejami:</span><span class="sxs-lookup"><span data-stu-id="a5afe-120">Here are some examples of the functionality that becomes available:</span></span>

-   <span data-ttu-id="a5afe-121">Līdzeklis Vadītā pārdošana nodrošina pa tālruni veiktās pārdošanas scenāriju un preču attēlu konfigurēšanas iespējas, lai palīdzētu pārdevējiem pieņemt pasūtījumus un vadītu šo procesu.</span><span class="sxs-lookup"><span data-stu-id="a5afe-121">Guided selling provides configuration options for tele-sales scripts and product images to help and guide sales clerks while they take orders.</span></span>
-   <span data-ttu-id="a5afe-122">Pasūtījumi nevar būt pabeigti, kamēr pārdošanas darbinieki nav ieguvuši vismaz vienu maksājuma metodi.</span><span class="sxs-lookup"><span data-stu-id="a5afe-122">Orders can't be completed until sales clerks have captured at least one payment method.</span></span>
-   <span data-ttu-id="a5afe-123">Papildu pārdošanas un šķērspārdošanas noteikumus var konfigurēt, lai atgādinātu pārdošanas darbiniekiem veicināt konkrētu produktu klientam.</span><span class="sxs-lookup"><span data-stu-id="a5afe-123">Upsell and cross-sell rules can be configured to prompt sales clerks to promote specific products to the customer.</span></span>
-   <span data-ttu-id="a5afe-124">Pārdošanas darbinieki var tvert kataloga avota kodu, no kura debitors veic pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="a5afe-124">Sales clerks can capture the source code for the catalog that a customer is ordering from.</span></span>
-   <span data-ttu-id="a5afe-125">Pārdošanas darbinieki pasūtījumam var pievienot mazumtirgotāja kuponus.</span><span class="sxs-lookup"><span data-stu-id="a5afe-125">Sales clerks can add a retailer's coupons to the order.</span></span>
-   <span data-ttu-id="a5afe-126">Pārdošanas darbinieki var pārdot nepārtrauktības programmas.</span><span class="sxs-lookup"><span data-stu-id="a5afe-126">Sales clerks can sell continuity programs.</span></span>
-   <span data-ttu-id="a5afe-127">Pasūtījumus var manuāli vai automātiski aizturēt, lai norādītu, ka pirms pasūtījuma apstrādes ir nepieciešama papildu izmeklēšana.</span><span class="sxs-lookup"><span data-stu-id="a5afe-127">Orders can be put on hold manually or automatically, to indicate that additional investigation is required before the order can be processed.</span></span>





