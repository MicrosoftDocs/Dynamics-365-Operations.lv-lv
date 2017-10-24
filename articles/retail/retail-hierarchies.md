---
title: "Mazumtirdzniecības hierarhijas"
description: "Šajā rakstā ir aprakstītas programmā Microsoft Dynamics 365 for Retail pieejamās mazumtirdzniecības hierarhijas."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 817696566473bc5f31a7ff11c04291351dfd4764
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="retail-hierarchies"></a><span data-ttu-id="5cb51-103">Mazumtirdzniecības hierarhijas</span><span class="sxs-lookup"><span data-stu-id="5cb51-103">Retail hierarchies</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="5cb51-104">Šajā rakstā ir aprakstītas programmā Microsoft Dynamics 365 for Retail pieejamās mazumtirdzniecības hierarhijas.</span><span class="sxs-lookup"><span data-stu-id="5cb51-104">This article describes retail hierarchies in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="5cb51-105">Varat izveidot mazumtirdzniecības kategoriju hierarhiju, lai sakārtotu preces, ko pārdodat mazumtirdzniecības kanālos.</span><span class="sxs-lookup"><span data-stu-id="5cb51-105">You can create a retail category hierarchy to organize the products that you sell through your retail channels.</span></span> <span data-ttu-id="5cb51-106">Varat izmantot mazumtirdzniecības preču hierarhijas, lai dalītu preces kategorijās vai grupās.</span><span class="sxs-lookup"><span data-stu-id="5cb51-106">You can use retail product hierarchies to categorize or group products.</span></span> <span data-ttu-id="5cb51-107">Šīs preces tad var izmantot preču klāstu un klientu lojalitātes programmu izveidei.</span><span class="sxs-lookup"><span data-stu-id="5cb51-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="5cb51-108">Var arī piešķirt preces īpašības un rekvizītus, piešķirt cenu struktūru, iekļaut preces preču reklamēšanas pasākumos, kā arī izmantot preces pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="5cb51-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="5cb51-109">Varat izveidot vienu mazumtirdzniecības kategoriju hierarhiju, lai pārstāvētu visas preces un kategorijas jūsu uzņēmumā, un pēc tam izmantot šo kategoriju hierarhiju vairākiem mērķiem.</span><span class="sxs-lookup"><span data-stu-id="5cb51-109">You can create one retail category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="5cb51-110">Varat arī izveidot vairākas mazumtirdzniecības kategoriju hierarhijas īpašiem nolūkiem, piemēram, preču reklamēšanas pasākumiem.</span><span class="sxs-lookup"><span data-stu-id="5cb51-110">Alternatively, you can create multiple retail category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="5cb51-111">Veidojot mazumtirdzniecības preču hierarhiju, jāpiešķir kategoriju hierarhijas tips, lai noteiktu kategoriju hierarhijas mērķi.</span><span class="sxs-lookup"><span data-stu-id="5cb51-111">When you create a retail product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="5cb51-112">Piemēram: pārlūkojot preces pēc kategorijas tiešsaistē vai pārdošanas punktā (POS), atsauce tiks norādīta tikai uz tām preču hierarhijām, kurām piešķirts tips **Mazumtirdzniecības navigācijas hierarhija**.</span><span class="sxs-lookup"><span data-stu-id="5cb51-112">For example, only product hierarchies that are assigned the **Retail navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="retail-hierarchy-types"></a><span data-ttu-id="5cb51-113">Mazumtirdzniecības hierarhijas tipi</span><span class="sxs-lookup"><span data-stu-id="5cb51-113">Retail hierarchy types</span></span>
<span data-ttu-id="5cb51-114">Nākamajā tabulā ir norādīti pieejamo mazumtirdzniecības kategoriju hierarhijas tipi un katra tipa vispārējais mērķis.</span><span class="sxs-lookup"><span data-stu-id="5cb51-114">The following table lists the types of retail category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="5cb51-115">Kategoriju hierarhijas tips</span><span class="sxs-lookup"><span data-stu-id="5cb51-115">Category hierarchy type</span></span>       | <span data-ttu-id="5cb51-116">Mērķis</span><span class="sxs-lookup"><span data-stu-id="5cb51-116">Purpose</span></span>                                                                                                                                                                                                                                                                                                            |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cb51-117">Mazumtirdzniecības preču hierarhija</span><span class="sxs-lookup"><span data-stu-id="5cb51-117">Retail product hierarchy</span></span>      | <span data-ttu-id="5cb51-118">Izmantojiet šo hierarhijas tipu, lai definētu vispārējo savas organizācijas preču hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="5cb51-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="5cb51-119">Varat izmantot šo hierarhijas tipu preču virzīšanai tirgū, cenu noteikšanai un reklamēšanas pasākumiem, kā arī ziņojumu izveides un preču klāsta plānošanai.</span><span class="sxs-lookup"><span data-stu-id="5cb51-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="5cb51-120">Šim hierarhijas tipam var piešķirt tikai vienu mazumtirdzniecības preču hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="5cb51-120">Only one retail product hierarchy can be assigned this hierarchy type.</span></span>                                       |
| <span data-ttu-id="5cb51-121">Papildu mazumtirdzniecības hierarhija</span><span class="sxs-lookup"><span data-stu-id="5cb51-121">Supplemental retail hierarchy</span></span> | <span data-ttu-id="5cb51-122">Lietojiet šo hierarhijas tipu papildu mazumtirdzniecības kategoriju hierarhijām, kuras vēlaties izveidot.</span><span class="sxs-lookup"><span data-stu-id="5cb51-122">Use this hierarchy type for any additional retail category hierarchies that you want to create.</span></span> <span data-ttu-id="5cb51-123">Pavasarī, piemēram, jūs reklamējat peldkostīmus.</span><span class="sxs-lookup"><span data-stu-id="5cb51-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="5cb51-124">Tādēļ varat iekļaut peldkostīmus atsevišķā kategoriju hierarhijā un veikt reklāmas cenu noteikšanu uz dažādu preču kategorijām.</span><span class="sxs-lookup"><span data-stu-id="5cb51-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="5cb51-125">Mazumtirdzniecības navigācijas hierarhija</span><span class="sxs-lookup"><span data-stu-id="5cb51-125">Retail navigation hierarchy</span></span>   | <span data-ttu-id="5cb51-126">Lietojiet šo hierarhijas tipu preču grupēšanai un kārtošanai kategorijās tā, lai preces var pārlūkot tiešsaistē vai POS.</span><span class="sxs-lookup"><span data-stu-id="5cb51-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span>                                                                                                                                                                                       |

<span data-ttu-id="5cb51-127">Izmantojot mazumtirdzniecības kategoriju hierarhiju savu preču kārtošanai, varat iestatīt un uzturēt preces īpašības un rekvizītus kategorijas līmenī.</span><span class="sxs-lookup"><span data-stu-id="5cb51-127">By using a retail category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="5cb51-128">Šīs īpašības un rekvizīti ietver preču dimensijas iestatījumus un POS iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="5cb51-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="5cb51-129">Jebkādas preces, ko piešķirat kategorijām, automātiski pārmantos jūsu definētas īpašības un rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="5cb51-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="5cb51-130">Varat arī vienlaikus nokopēt preču rekvizītu iestatījumus vairākām precēm atlasītā kategorijā.</span><span class="sxs-lookup"><span data-stu-id="5cb51-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>




