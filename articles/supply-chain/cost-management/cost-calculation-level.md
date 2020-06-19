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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 52b77e794ee38add556ac01d62c973b38c48a548
ms.sourcegitcommit: a3cd2783ae120ac6681431c010b9b126a9ca7d94
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410966"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="fa78d-104">Izmaksu aprēķina līmenis</span><span class="sxs-lookup"><span data-stu-id="fa78d-104">Cost calculation level</span></span>

<span data-ttu-id="fa78d-105">Materiālu komplekta (MK) līmenis ar nosaukumu **Izmaksu aprēķina līmenis** tā aprēķinos neietver ražošanas pasūtījumus un partijas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="fa78d-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="fa78d-106">Sistēma izmanto šo līmeni, kad tā veic izmaksu aprēķinus izmaksu aprēķināšanas versijās.</span><span class="sxs-lookup"><span data-stu-id="fa78d-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="fa78d-107">Tādos procesos kā pārrēķins un krājumu slēgšana, sistēma to vietā izmanto **Izmaksu līmeņa** MK līmeni.</span><span class="sxs-lookup"><span data-stu-id="fa78d-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="fa78d-108">Tālāk minētajā vienkāršajā scenārijā ir parādītas atšķirības starp **Izmaksu aprēķina līmeņa** MK līmeni un **Izmaksu aprēķināšanas līmeņa** MK līmeni.</span><span class="sxs-lookup"><span data-stu-id="fa78d-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="fa78d-109">Jums ir trīs preces: A, B un C. Prece C ir preces B komponents, un prece B ir preces A komponents.</span><span class="sxs-lookup"><span data-stu-id="fa78d-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="fa78d-110">**Izmaksu aprēķināšanas līmenis** piešķir šādus MK līmeņus:</span><span class="sxs-lookup"><span data-stu-id="fa78d-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="fa78d-111">**Prece A:** 0</span><span class="sxs-lookup"><span data-stu-id="fa78d-111">**Product A:** 0</span></span>
    - <span data-ttu-id="fa78d-112">**Prece B:** 1</span><span class="sxs-lookup"><span data-stu-id="fa78d-112">**Product B:** 1</span></span>
    - <span data-ttu-id="fa78d-113">**Prece C:** 2</span><span class="sxs-lookup"><span data-stu-id="fa78d-113">**Product C:** 2</span></span>

- <span data-ttu-id="fa78d-114">**Izmaksu aprēķina** piešķir šādus MK līmeņus:</span><span class="sxs-lookup"><span data-stu-id="fa78d-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="fa78d-115">**Prece A:** 0</span><span class="sxs-lookup"><span data-stu-id="fa78d-115">**Product A:** 0</span></span>
    - <span data-ttu-id="fa78d-116">**Prece B:** 1</span><span class="sxs-lookup"><span data-stu-id="fa78d-116">**Product B:** 1</span></span>
    - <span data-ttu-id="fa78d-117">**Prece C:** 2</span><span class="sxs-lookup"><span data-stu-id="fa78d-117">**Product C:** 2</span></span>

<span data-ttu-id="fa78d-118">Pēc tam tiek izveidots ražošanas pasūtījuma precei C, un prece A tiek pievienota ražošanas pasūtījuma MK.</span><span class="sxs-lookup"><span data-stu-id="fa78d-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="fa78d-119">Pēc tam, kad pasūtījums tiek aplēsts, MK līmeņi tiek atjaunināti šādi:</span><span class="sxs-lookup"><span data-stu-id="fa78d-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="fa78d-120">**Izmaksu aprēķināšanas līmenis** piešķir šādus MK līmeņus:</span><span class="sxs-lookup"><span data-stu-id="fa78d-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="fa78d-121">**Prece B:** 1</span><span class="sxs-lookup"><span data-stu-id="fa78d-121">**Product B:** 1</span></span>
    - <span data-ttu-id="fa78d-122">**Prece C:** 2</span><span class="sxs-lookup"><span data-stu-id="fa78d-122">**Product C:** 2</span></span>
    - <span data-ttu-id="fa78d-123">**Prece A:** 3</span><span class="sxs-lookup"><span data-stu-id="fa78d-123">**Product A:** 3</span></span>

- <span data-ttu-id="fa78d-124">**Izmaksu aprēķina** piešķir šādus MK līmeņus:</span><span class="sxs-lookup"><span data-stu-id="fa78d-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="fa78d-125">**Prece A:** 0</span><span class="sxs-lookup"><span data-stu-id="fa78d-125">**Product A:** 0</span></span>
    - <span data-ttu-id="fa78d-126">**Prece B:** 1</span><span class="sxs-lookup"><span data-stu-id="fa78d-126">**Product B:** 1</span></span>
    - <span data-ttu-id="fa78d-127">**Prece C:** 2</span><span class="sxs-lookup"><span data-stu-id="fa78d-127">**Product C:** 2</span></span>

<span data-ttu-id="fa78d-128">Šī uzvedība nodrošina, ka ražošanas pasūtījuma MK izmaiņas neietekmē turpmākos izmaksu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="fa78d-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>
