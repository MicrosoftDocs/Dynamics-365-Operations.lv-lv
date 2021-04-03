---
title: Izmaksu aprēķina līmenis
description: Šajā tēmā aprakstīts materiālu komplekta (MK) līmenis, kura nosaukums ir Izmaksu aprēķina līmenis. Šis MK līmenis tā aprēķinos neietver ražošanas un partijas pasūtījumus.
author: AndersGirke
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 1cfbbb6aadbd24a0352776285f6c60ff10f59549
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251030"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="13c2b-104">Izmaksu aprēķina līmenis</span><span class="sxs-lookup"><span data-stu-id="13c2b-104">Cost calculation level</span></span>

<span data-ttu-id="13c2b-105">Materiālu komplekta (MK) līmenis ar nosaukumu **Izmaksu aprēķina līmenis** tā aprēķinos neietver ražošanas pasūtījumus un partijas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="13c2b-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="13c2b-106">Sistēma izmanto šo līmeni, kad tā veic izmaksu aprēķinus izmaksu aprēķināšanas versijās.</span><span class="sxs-lookup"><span data-stu-id="13c2b-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="13c2b-107">Tādos procesos kā pārrēķins un krājumu slēgšana, sistēma to vietā izmanto **Izmaksu līmeņa** MK līmeni.</span><span class="sxs-lookup"><span data-stu-id="13c2b-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="13c2b-108">Tālāk minētajā vienkāršajā scenārijā ir parādītas atšķirības starp **Izmaksu aprēķina līmeņa** MK līmeni un **Izmaksu aprēķināšanas līmeņa** MK līmeni.</span><span class="sxs-lookup"><span data-stu-id="13c2b-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="13c2b-109">Jums ir trīs preces: A, B un C. Prece C ir preces B komponents, un prece B ir preces A komponents.</span><span class="sxs-lookup"><span data-stu-id="13c2b-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="13c2b-110">**Izmaksu aprēķināšanas līmenis** piešķir šādus MK līmeņus:</span><span class="sxs-lookup"><span data-stu-id="13c2b-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="13c2b-111">**Prece A:** 0</span><span class="sxs-lookup"><span data-stu-id="13c2b-111">**Product A:** 0</span></span>
    - <span data-ttu-id="13c2b-112">**Prece B:** 1</span><span class="sxs-lookup"><span data-stu-id="13c2b-112">**Product B:** 1</span></span>
    - <span data-ttu-id="13c2b-113">**Prece C:** 2</span><span class="sxs-lookup"><span data-stu-id="13c2b-113">**Product C:** 2</span></span>

- <span data-ttu-id="13c2b-114">**Izmaksu aprēķina** piešķir šādus MK līmeņus:</span><span class="sxs-lookup"><span data-stu-id="13c2b-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="13c2b-115">**Prece A:** 0</span><span class="sxs-lookup"><span data-stu-id="13c2b-115">**Product A:** 0</span></span>
    - <span data-ttu-id="13c2b-116">**Prece B:** 1</span><span class="sxs-lookup"><span data-stu-id="13c2b-116">**Product B:** 1</span></span>
    - <span data-ttu-id="13c2b-117">**Prece C:** 2</span><span class="sxs-lookup"><span data-stu-id="13c2b-117">**Product C:** 2</span></span>

<span data-ttu-id="13c2b-118">Pēc tam tiek izveidots ražošanas pasūtījuma precei C, un prece A tiek pievienota ražošanas pasūtījuma MK.</span><span class="sxs-lookup"><span data-stu-id="13c2b-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="13c2b-119">Pēc tam, kad pasūtījums tiek aplēsts, MK līmeņi tiek atjaunināti šādi:</span><span class="sxs-lookup"><span data-stu-id="13c2b-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="13c2b-120">**Izmaksu aprēķināšanas līmenis** piešķir šādus MK līmeņus:</span><span class="sxs-lookup"><span data-stu-id="13c2b-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="13c2b-121">**Prece B:** 1</span><span class="sxs-lookup"><span data-stu-id="13c2b-121">**Product B:** 1</span></span>
    - <span data-ttu-id="13c2b-122">**Prece C:** 2</span><span class="sxs-lookup"><span data-stu-id="13c2b-122">**Product C:** 2</span></span>
    - <span data-ttu-id="13c2b-123">**Prece A:** 3</span><span class="sxs-lookup"><span data-stu-id="13c2b-123">**Product A:** 3</span></span>

- <span data-ttu-id="13c2b-124">**Izmaksu aprēķina** piešķir šādus MK līmeņus:</span><span class="sxs-lookup"><span data-stu-id="13c2b-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="13c2b-125">**Prece A:** 0</span><span class="sxs-lookup"><span data-stu-id="13c2b-125">**Product A:** 0</span></span>
    - <span data-ttu-id="13c2b-126">**Prece B:** 1</span><span class="sxs-lookup"><span data-stu-id="13c2b-126">**Product B:** 1</span></span>
    - <span data-ttu-id="13c2b-127">**Prece C:** 2</span><span class="sxs-lookup"><span data-stu-id="13c2b-127">**Product C:** 2</span></span>

<span data-ttu-id="13c2b-128">Šī uzvedība nodrošina, ka ražošanas pasūtījuma MK izmaiņas neietekmē turpmākos izmaksu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="13c2b-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]