---
title: Commerce hierarhijas
description: Šajā rakstā ir aprakstītas hierarhijas programmā Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager, EcoResCategoryHierarchyFactbox
audience: Application User
ms.reviewer: josaw
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a2cc766b0fd358d82187a5c0368005896fbb7769
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251381"
---
# <a name="commerce-hierarchies"></a><span data-ttu-id="4ee6b-103">Commerce hierarhijas</span><span class="sxs-lookup"><span data-stu-id="4ee6b-103">Commerce hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4ee6b-104">Šajā rakstā ir aprakstītas hierarhijas programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-104">This article describes hierarchies in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4ee6b-105">Varat izveidot kategoriju hierarhiju, lai sakārtotu preces, ko pārdodat pa saviem kanāliem.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-105">You can create a category hierarchy to organize the products that you sell through your channels.</span></span> <span data-ttu-id="4ee6b-106">Varat izmantot preču hierarhijas, lai dalītu preces kategorijās vai grupās.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-106">You can use product hierarchies to categorize or group products.</span></span> <span data-ttu-id="4ee6b-107">Šīs preces tad var izmantot preču klāstu un klientu lojalitātes programmu izveidei.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="4ee6b-108">Var arī piešķirt preces īpašības un rekvizītus, piešķirt cenu struktūru, iekļaut preces preču reklamēšanas pasākumos, kā arī izmantot preces pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="4ee6b-109">Varat izveidot vienu kategoriju hierarhiju, lai pārstāvētu visas preces un kategorijas jūsu uzņēmumā, un pēc tam izmantot šo kategoriju hierarhiju vairākiem mērķiem.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-109">You can create one category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="4ee6b-110">Varat arī izveidot vairākas kategoriju hierarhijas īpašiem nolūkiem, piemēram, preču veicināšanas pasākumiem.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-110">Alternatively, you can create multiple category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="4ee6b-111">Veidojot preču hierarhiju, jāpiešķir kategoriju hierarhijas tips, lai noteiktu kategoriju hierarhijas mērķi.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-111">When you create a product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="4ee6b-112">Piemēram: pārlūkojot preces pēc kategorijas tiešsaistē vai pārdošanas punktā (POS), atsauce tiks norādīta tikai uz tām preču hierarhijām, kurām piešķirts tips **Commerce navigācijas hierarhija**.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-112">For example, only product hierarchies that are assigned the **Commerce navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="hierarchy-types"></a><span data-ttu-id="4ee6b-113">Hierarhijas veidi</span><span class="sxs-lookup"><span data-stu-id="4ee6b-113">Hierarchy types</span></span>

<span data-ttu-id="4ee6b-114">Nākamajā tabulā ir norādīti pieejamo kategoriju hierarhijas tipi un katra tipa vispārējais mērķis.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-114">The following table lists the types of category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="4ee6b-115">Kategoriju hierarhijas tips</span><span class="sxs-lookup"><span data-stu-id="4ee6b-115">Category hierarchy type</span></span>       | <span data-ttu-id="4ee6b-116">Nolūks</span><span class="sxs-lookup"><span data-stu-id="4ee6b-116">Purpose</span></span> |
|-------------------------------|---------|
| <span data-ttu-id="4ee6b-117">Preču hierarhija</span><span class="sxs-lookup"><span data-stu-id="4ee6b-117">Product hierarchy</span></span>      | <span data-ttu-id="4ee6b-118">Izmantojiet šo hierarhijas tipu, lai definētu vispārējo savas organizācijas preču hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="4ee6b-119">Varat izmantot šo hierarhijas tipu preču virzīšanai tirgū, cenu noteikšanai un reklamēšanas pasākumiem, kā arī ziņojumu izveides un preču klāsta plānošanai.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="4ee6b-120">Šim hierarhijas tipam var piešķirt tikai vienu preču hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-120">Only one product hierarchy can be assigned this hierarchy type.</span></span> |
| <span data-ttu-id="4ee6b-121">Papildu hierarhija</span><span class="sxs-lookup"><span data-stu-id="4ee6b-121">Supplemental hierarchy</span></span> | <span data-ttu-id="4ee6b-122">Lietojiet šo hierarhijas tipu papildu kategoriju hierarhijām, kuras vēlaties izveidot.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-122">Use this hierarchy type for any additional category hierarchies that you want to create.</span></span> <span data-ttu-id="4ee6b-123">Pavasarī, piemēram, jūs reklamējat peldkostīmus.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="4ee6b-124">Tādēļ varat iekļaut peldkostīmus atsevišķā kategoriju hierarhijā un veikt reklāmas cenu noteikšanu uz dažādu preču kategorijām.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="4ee6b-125">Navigācijas hierarhija</span><span class="sxs-lookup"><span data-stu-id="4ee6b-125">Navigation hierarchy</span></span>   | <span data-ttu-id="4ee6b-126">Lietojiet šo hierarhijas tipu preču grupēšanai un kārtošanai kategorijās tā, lai preces var pārlūkot tiešsaistē vai POS.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span> |

<span data-ttu-id="4ee6b-127">Izmantojot kategoriju hierarhiju savu preču kārtošanai, varat iestatīt un uzturēt preces īpašības un rekvizītus kategorijas līmenī.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-127">By using a category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="4ee6b-128">Šīs īpašības un rekvizīti ietver preču dimensijas iestatījumus un POS iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="4ee6b-129">Jebkādas preces, ko piešķirat kategorijām, automātiski pārmantos jūsu definētas īpašības un rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="4ee6b-130">Varat arī vienlaikus nokopēt preču rekvizītu iestatījumus vairākām precēm atlasītā kategorijā.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]