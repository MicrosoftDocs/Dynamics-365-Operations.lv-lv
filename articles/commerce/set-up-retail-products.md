---
title: Iestatīt Retail preces
description: Šajā rakstā ir aprakstīts, kā iestatīt mazumtirdzniecības preces programmā Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailProductAndCategoryWorkspace, EcoResProductDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e8f624f5feb8ee8f641a9b35ae31bdfe38e5e0ce
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023300"
---
# <a name="set-up-retail-products"></a><span data-ttu-id="0ef62-103">Mazumtirdzniecības preču iestatīšana</span><span class="sxs-lookup"><span data-stu-id="0ef62-103">Set up retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0ef62-104">Šajā rakstā ir aprakstīts, kā iestatīt preces programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0ef62-104">This article describes how to set up products in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0ef62-105">Lai preces varētu piedāvāt atkārtošanai pārdošanai savos komercijas kanālos, šīs preces ir jāizveido un jākonfigurē.</span><span class="sxs-lookup"><span data-stu-id="0ef62-105">Before you can offer products for resale in your commerce channels, you must create and configure the products.</span></span> <span data-ttu-id="0ef62-106">Commerce izveido organizācijas līmeņa preces preču šablonā.</span><span class="sxs-lookup"><span data-stu-id="0ef62-106">Commerce creates organization-wide products in the product master.</span></span> <span data-ttu-id="0ef62-107">Varat izveidot preces, definēt preču rekvizītus un atribūtus, un piešķirt šīs preces komercijas kategoriju hierarhijām.</span><span class="sxs-lookup"><span data-stu-id="0ef62-107">You can create the products, define the product properties and attributes, and assign the products to commerce category hierarchies.</span></span> <span data-ttu-id="0ef62-108">Lai preces padarītu pieejamas saviem kanāliem un tās pievienotu aktīvam preču klāstam, šīs preces ir jāizlaiž juridiskajām personām, kurās tās ir pieejamas.</span><span class="sxs-lookup"><span data-stu-id="0ef62-108">To make the products available to your channels and add them to an active assortment, you must release the products to the legal entities where they are available.</span></span> <span data-ttu-id="0ef62-109">Lai iestatītu preces, ko pārdodat, izmantojot kanālus, veiciet tālāk norādītos uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="0ef62-109">To set up the products that you sell by using channels, complete the following tasks.</span></span>

1. <span data-ttu-id="0ef62-110">**Definējiet preču hierarhiju.**</span><span class="sxs-lookup"><span data-stu-id="0ef62-110">**Define a product hierarchy.**</span></span> <span data-ttu-id="0ef62-111">Izmantojot programmā Commerce pieejamos kategoriju hierarhijas līdzekļus, varat definēt mazumtirdzniecības kategoriju hierarhijas, lai grupētu un kategorizētu preces, ko izplatāt mazumtirdzniecības kanālos.</span><span class="sxs-lookup"><span data-stu-id="0ef62-111">By using the category hierarchy features in Commerce, you can define category hierarchies to group and categorize the products that you distribute to your channels.</span></span> <span data-ttu-id="0ef62-112">Kategorijas līmenī var definēt lietotāja definētos un sistēmas atribūtus.</span><span class="sxs-lookup"><span data-stu-id="0ef62-112">User-defined and system attributes can be defined at the category level.</span></span> <span data-ttu-id="0ef62-113">Pēc tam visas ar kategoriju saistītās preces pārmanto šos atribūtus.</span><span class="sxs-lookup"><span data-stu-id="0ef62-113">Then, all products that are assigned to the category inherit those attributes.</span></span> <span data-ttu-id="0ef62-114">Var definēt vairākas kategoriju hierarhijas, un katru preci var piešķirt vairākām hierarhijām.</span><span class="sxs-lookup"><span data-stu-id="0ef62-114">Multiple category hierarchies can be defined, and each product can be assigned to multiple hierarchies.</span></span> <span data-ttu-id="0ef62-115">Taču vienā hierarhijā katru preci var piešķirt tikai vienai kategorijai.</span><span class="sxs-lookup"><span data-stu-id="0ef62-115">However, in a single hierarchy, each product can be assigned to only one category.</span></span>
2. <span data-ttu-id="0ef62-116">**Pievienojiet preces un preču variantus preces šablonam.**</span><span class="sxs-lookup"><span data-stu-id="0ef62-116">**Add products and product variants to the product master.**</span></span> <span data-ttu-id="0ef62-117">Preces šablonam pievienotās preces veido globālu preču sarakstu.</span><span class="sxs-lookup"><span data-stu-id="0ef62-117">Products that are added to the product master represent a global list of products.</span></span> <span data-ttu-id="0ef62-118">Varat manuāli pievienot preces pa vienai vai importēt preču datus no kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="0ef62-118">You can add products manually, one at a time, or you can import product data from your vendors.</span></span>
3. <span data-ttu-id="0ef62-119">**Izlaidiet preci juridiskajam personām.**</span><span class="sxs-lookup"><span data-stu-id="0ef62-119">**Release the products to legal entities.**</span></span> <span data-ttu-id="0ef62-120">Jūsu kanālos var padarīt pieejamas tikai tās preces, kas ir izdotas juridiskām personām.</span><span class="sxs-lookup"><span data-stu-id="0ef62-120">Only products that have been released to legal entities can be made available to your channels.</span></span> <span data-ttu-id="0ef62-121">Pirmo reizi definējot preci, tā tiek definēta organizācijas līmenī.</span><span class="sxs-lookup"><span data-stu-id="0ef62-121">When you first define a product, you define it on an organization-wide level.</span></span> <span data-ttu-id="0ef62-122">Pēc tam varat atlasīt vienu vai vairākas juridiskas personas, kam izlaist preci.</span><span class="sxs-lookup"><span data-stu-id="0ef62-122">You can then select one or more legal entities to release the product to.</span></span> <span data-ttu-id="0ef62-123">Pēc tam prece kļūst pieejama vairākos kanālos jūsu organizācijā.</span><span class="sxs-lookup"><span data-stu-id="0ef62-123">The product then becomes available to multiple channels across your organization.</span></span> <span data-ttu-id="0ef62-124">Varat izmantot šo funkcionalitāti, lai vienreiz izveidotu preci, vienuviet pievienotu un atjauninātu preces atribūtus un rekvizītus un pēc tam izplatītu preci savas organizācijas kanālos, kur tā ir pieejama.</span><span class="sxs-lookup"><span data-stu-id="0ef62-124">You can use this functionality to create a product one time, add and update product attributes and properties in one place, and then distribute the product across your organization, to the channels where it's available.</span></span>
4. <span data-ttu-id="0ef62-125">**Pievienojiet preces klāstiem.**</span><span class="sxs-lookup"><span data-stu-id="0ef62-125">**Add products to assortments.**</span></span> <span data-ttu-id="0ef62-126">Klāsts ir preču kopa, ko piedāvājat savos kanālos.</span><span class="sxs-lookup"><span data-stu-id="0ef62-126">An assortment represents a collection of products that you offer in your channels.</span></span> <span data-ttu-id="0ef62-127">Varat definēt vienu vai vairākus klāstus un katru preci varat piešķirt vienam vai vairākiem klāstiem.</span><span class="sxs-lookup"><span data-stu-id="0ef62-127">You can define one or more assortments, and each product can be assigned to one or more assortments.</span></span> <span data-ttu-id="0ef62-128">Lai piešķirtu preces kanāliem, jūs piešķirat klāstus šiem kanāliem.</span><span class="sxs-lookup"><span data-stu-id="0ef62-128">To assign products to channels, you assign the assortments to those channels.</span></span> <span data-ttu-id="0ef62-129">Kad izveidojat klāstu, varat pievienot preces, kas vēl nav izlaistas juridiskai personai.</span><span class="sxs-lookup"><span data-stu-id="0ef62-129">When you create an assortment, you can add products that haven't yet been released to a legal entity.</span></span> <span data-ttu-id="0ef62-130">Taču, lai preces varētu padarīt pieejamas kanālos, šīs preces vispirms ir jāizlaiž juridiskai personai.</span><span class="sxs-lookup"><span data-stu-id="0ef62-130">However, you must release the products to a legal entity before those products can be made available to the channels.</span></span>
5. <span data-ttu-id="0ef62-131">**Pievienojiet preces navigācijas hierarhijām.**</span><span class="sxs-lookup"><span data-stu-id="0ef62-131">**Add products to navigation hierarchies.**</span></span> <span data-ttu-id="0ef62-132">Lai preces varētu pārlūkot tiešsaistē vai pārdošanas punktā (POS), vispirms tās ir jākategorizē Commerce navigācijas hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="0ef62-132">Before products can be browsed online or in point of sale (POS), they must be categorized in a Commerce navigation hierarchy.</span></span>
6. <span data-ttu-id="0ef62-133">**Pievienojiet preces katalogiem.**</span><span class="sxs-lookup"><span data-stu-id="0ef62-133">**Add products to catalogs.**</span></span> <span data-ttu-id="0ef62-134">Lai gan šī darbība nav obligāta, ja izmantojat POS, lai izmantotu tiešsaistes veikalus, precēm ir jābūt iekļautām vismaz vienā katalogā.</span><span class="sxs-lookup"><span data-stu-id="0ef62-134">Although this step is optional for POS, online stores require that products be included in at least one catalog.</span></span>