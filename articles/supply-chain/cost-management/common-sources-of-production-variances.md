---
title: "Ražošanas noviržu vispārējo iemeslu analīze"
description: "Šajā rakstā ir izskaidroti dažādi tipiski visu ražošanas noviržu veidu iemesli."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostTrans
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f8eea27edaa97150ceb2c36996177395cba8bdb9
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="common-sources-of-production-variances"></a><span data-ttu-id="5a709-103">Ražošanas noviržu vispārējo iemeslu analīze</span><span class="sxs-lookup"><span data-stu-id="5a709-103">Common sources of production variances</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5a709-104">Šajā rakstā ir izskaidroti dažādi tipiski visu ražošanas noviržu veidu iemesli.</span><span class="sxs-lookup"><span data-stu-id="5a709-104">This article explains various typical sources of each type of production variance.</span></span> 

<span data-ttu-id="5a709-105">Tālāk norādīti daži tipiski **partijas lieluma** noviržu iemesli.</span><span class="sxs-lookup"><span data-stu-id="5a709-105">Here are some typical sources of a **lot size** variance:</span></span>

-   <span data-ttu-id="5a709-106">Preču daudzums ražošanas pasūtījumam atšķiras no aprēķina daudzuma, kas tiek izmantots standarta izmaksu aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="5a709-106">The good quantity for a production order differs from the calculation quantity that is used in the standard cost calculation.</span></span> <span data-ttu-id="5a709-107">Daudzums nodrošina pamatojumu amortizēšanas konstantām izmaksām.</span><span class="sxs-lookup"><span data-stu-id="5a709-107">The quantity provides the basis for amortizing constant costs.</span></span>
-   <span data-ttu-id="5a709-108">Konstanto izmaksu vērtība ražošanas pasūtījumā atšķiras no konstantām izmaksām, kas tiek izmantotas standarta izmaksu aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="5a709-108">The value of constant costs on the production order differs from the constant costs that are used in the standard cost calculation.</span></span> <span data-ttu-id="5a709-109">Konstantas izmaksas ražošanas pasūtījumā var atšķirties dažādu iemeslu dēļ.</span><span class="sxs-lookup"><span data-stu-id="5a709-109">The constant costs on the production order can differ for several reasons.</span></span> <span data-ttu-id="5a709-110">Piemēram, konstantas izmaksas var norādīt uz tālāk minētajiem faktoriem.</span><span class="sxs-lookup"><span data-stu-id="5a709-110">For example, the constant costs might reflect the following factors:</span></span>
    -   <span data-ttu-id="5a709-111">Manuāli veiktas izmaiņas ražošanas materiālu komplektā (MK) vai maršrutā</span><span class="sxs-lookup"><span data-stu-id="5a709-111">Manual changes to the production bill of materials (BOM) or route</span></span>
    -   <span data-ttu-id="5a709-112">Atšķirīgas MK vai maršruta versijas atlase, izveidojot ražošanas pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="5a709-112">The selection of a different BOM version or route version when you create the production order</span></span>
    -   <span data-ttu-id="5a709-113">Krājumam piešķirtās MK vai maršruta versijas plānotas tehnoloģiskas izmaiņas</span><span class="sxs-lookup"><span data-stu-id="5a709-113">Planned engineering changes to the BOM version or route version that is assigned to the item</span></span>

<span data-ttu-id="5a709-114">Tālāk norādīti daži tipiski **ražošanas cenas** noviržu iemesli.</span><span class="sxs-lookup"><span data-stu-id="5a709-114">Here are some typical sources of a **production price** variance:</span></span>

-   <span data-ttu-id="5a709-115">Izmaksu kategorija (un tās izmaksu kategorijas cena) maršrutēšanas operācijas ziņotajam patēriņam atšķiras no izmaksu kategorijas, ko izmanto standarta izmaksu aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="5a709-115">The cost category (and cost category price) for the reported consumption of a routing operation differs from the cost category that is used in standard cost calculation.</span></span>
-   <span data-ttu-id="5a709-116">Aktīvā izmaksa izmaksu kategorijas cenai atšķiras no izmaksu kategorijas cenas, ko izmanto standarta izmaksu aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="5a709-116">The active cost for the cost category price differs from the cost category price that is used in standard cost calculation.</span></span>

<span data-ttu-id="5a709-117">Tālāk norādīti daži tipiski **ražošanas daudzuma** noviržu iemesli.</span><span class="sxs-lookup"><span data-stu-id="5a709-117">Here are some typical sources of a **production quantity** variance:</span></span>

-   <span data-ttu-id="5a709-118">Materiāla komponenta pārmērīga vai nepietiekama izsniegšana.</span><span class="sxs-lookup"><span data-stu-id="5a709-118">You over-issue or under-issue a material component.</span></span>
-   <span data-ttu-id="5a709-119">Pārskatā norādīts pārsniegts vai nepietiekams maršrutēšanas operācijas laiks.</span><span class="sxs-lookup"><span data-stu-id="5a709-119">You over-report or under-report the time for a routing operation.</span></span>
-   <span data-ttu-id="5a709-120">Pārmērīga vai nepietiekama pamata krājuma, kas saistītas ar pasūtījuma daudzumu, derīga daudzuma saņemšana.</span><span class="sxs-lookup"><span data-stu-id="5a709-120">You over-receive or under-receive the good quantity of the parent item, relative to the order quantity.</span></span> <span data-ttu-id="5a709-121">Tomēr komponenti tiek izsniegti un darbības tiek reģistrētas pilnībā atkarībā no ražošanas pasūtījumā noradītā pasūtījuma daudzuma.</span><span class="sxs-lookup"><span data-stu-id="5a709-121">However, you issue components and report operations completely, based on the order quantity for the production order.</span></span>

<span data-ttu-id="5a709-122">Tālāk norādīti daži tipiski **ražošanas aizstāšanas** noviržu iemesli.</span><span class="sxs-lookup"><span data-stu-id="5a709-122">Here are some typical sources of a **production substitution** variance:</span></span>

-   <span data-ttu-id="5a709-123">Tiek izdots materiāla komponents, kas nav ražošanas MK.</span><span class="sxs-lookup"><span data-stu-id="5a709-123">You issue a material component that isn't on the production BOM.</span></span>
-   <span data-ttu-id="5a709-124">Ražošanas materiālu komplektam (MK) manuāli tiek pievienots komponents, reģistrējot to kā patērētu.</span><span class="sxs-lookup"><span data-stu-id="5a709-124">You manually add a component to the production BOM and report that component as consumed.</span></span>
-   <span data-ttu-id="5a709-125">Krājums tiek reģistrēts kā patērēts, bet netiek manuāli pievienots ražošanas MK.</span><span class="sxs-lookup"><span data-stu-id="5a709-125">You report an item as consumed but don't manually add it to the production BOM.</span></span>
-   <span data-ttu-id="5a709-126">Operācija tiek manuāli pievienota ražošanas maršrutam, reģistrējot to kā par patērētu.</span><span class="sxs-lookup"><span data-stu-id="5a709-126">You manually add an operation to the production route and report that operation as consumed.</span></span>
-   <span data-ttu-id="5a709-127">Izveidojot ražošanas pasūtījumu, tiek atlasīta MK versija, kas atšķiras no tās, ko izmanto standarta izmaksu aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="5a709-127">When you create the production order, you select a BOM version that differs from the BOM version that is used in the standard cost calculation.</span></span>
-   <span data-ttu-id="5a709-128">Izveidojot ražošanas pasūtījumu, tiek atlasīta maršruta versija, kas atšķiras no tās, ko izmanto standarta izmaksu aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="5a709-128">When you create the production order, you select a route version that differs from the route version that is used in the standard cost calculation.</span></span>





