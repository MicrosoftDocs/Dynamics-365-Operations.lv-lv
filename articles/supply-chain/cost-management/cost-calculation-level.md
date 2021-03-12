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
ms.openlocfilehash: 42088d8c005cf3fc04e768f1b8e8c8ca0b8c6993
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967736"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="32cc0-104">Izmaksu aprēķina līmenis</span><span class="sxs-lookup"><span data-stu-id="32cc0-104">Cost calculation level</span></span>

<span data-ttu-id="32cc0-105">Materiālu komplekta (MK) līmenis ar nosaukumu **Izmaksu aprēķina līmenis** tā aprēķinos neietver ražošanas pasūtījumus un partijas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="32cc0-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="32cc0-106">Sistēma izmanto šo līmeni, kad tā veic izmaksu aprēķinus izmaksu aprēķināšanas versijās.</span><span class="sxs-lookup"><span data-stu-id="32cc0-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="32cc0-107">Tādos procesos kā pārrēķins un krājumu slēgšana, sistēma to vietā izmanto **Izmaksu līmeņa** MK līmeni.</span><span class="sxs-lookup"><span data-stu-id="32cc0-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="32cc0-108">Tālāk minētajā vienkāršajā scenārijā ir parādītas atšķirības starp **Izmaksu aprēķina līmeņa** MK līmeni un **Izmaksu aprēķināšanas līmeņa** MK līmeni.</span><span class="sxs-lookup"><span data-stu-id="32cc0-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="32cc0-109">Jums ir trīs preces: A, B un C. Prece C ir preces B komponents, un prece B ir preces A komponents.</span><span class="sxs-lookup"><span data-stu-id="32cc0-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="32cc0-110">**Izmaksu aprēķināšanas līmenis** piešķir šādus MK līmeņus:</span><span class="sxs-lookup"><span data-stu-id="32cc0-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="32cc0-111">**Prece A:** 0</span><span class="sxs-lookup"><span data-stu-id="32cc0-111">**Product A:** 0</span></span>
    - <span data-ttu-id="32cc0-112">**Prece B:** 1</span><span class="sxs-lookup"><span data-stu-id="32cc0-112">**Product B:** 1</span></span>
    - <span data-ttu-id="32cc0-113">**Prece C:** 2</span><span class="sxs-lookup"><span data-stu-id="32cc0-113">**Product C:** 2</span></span>

- <span data-ttu-id="32cc0-114">**Izmaksu aprēķina** piešķir šādus MK līmeņus:</span><span class="sxs-lookup"><span data-stu-id="32cc0-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="32cc0-115">**Prece A:** 0</span><span class="sxs-lookup"><span data-stu-id="32cc0-115">**Product A:** 0</span></span>
    - <span data-ttu-id="32cc0-116">**Prece B:** 1</span><span class="sxs-lookup"><span data-stu-id="32cc0-116">**Product B:** 1</span></span>
    - <span data-ttu-id="32cc0-117">**Prece C:** 2</span><span class="sxs-lookup"><span data-stu-id="32cc0-117">**Product C:** 2</span></span>

<span data-ttu-id="32cc0-118">Pēc tam tiek izveidots ražošanas pasūtījuma precei C, un prece A tiek pievienota ražošanas pasūtījuma MK.</span><span class="sxs-lookup"><span data-stu-id="32cc0-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="32cc0-119">Pēc tam, kad pasūtījums tiek aplēsts, MK līmeņi tiek atjaunināti šādi:</span><span class="sxs-lookup"><span data-stu-id="32cc0-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="32cc0-120">**Izmaksu aprēķināšanas līmenis** piešķir šādus MK līmeņus:</span><span class="sxs-lookup"><span data-stu-id="32cc0-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="32cc0-121">**Prece B:** 1</span><span class="sxs-lookup"><span data-stu-id="32cc0-121">**Product B:** 1</span></span>
    - <span data-ttu-id="32cc0-122">**Prece C:** 2</span><span class="sxs-lookup"><span data-stu-id="32cc0-122">**Product C:** 2</span></span>
    - <span data-ttu-id="32cc0-123">**Prece A:** 3</span><span class="sxs-lookup"><span data-stu-id="32cc0-123">**Product A:** 3</span></span>

- <span data-ttu-id="32cc0-124">**Izmaksu aprēķina** piešķir šādus MK līmeņus:</span><span class="sxs-lookup"><span data-stu-id="32cc0-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="32cc0-125">**Prece A:** 0</span><span class="sxs-lookup"><span data-stu-id="32cc0-125">**Product A:** 0</span></span>
    - <span data-ttu-id="32cc0-126">**Prece B:** 1</span><span class="sxs-lookup"><span data-stu-id="32cc0-126">**Product B:** 1</span></span>
    - <span data-ttu-id="32cc0-127">**Prece C:** 2</span><span class="sxs-lookup"><span data-stu-id="32cc0-127">**Product C:** 2</span></span>

<span data-ttu-id="32cc0-128">Šī uzvedība nodrošina, ka ražošanas pasūtījuma MK izmaiņas neietekmē turpmākos izmaksu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="32cc0-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>
