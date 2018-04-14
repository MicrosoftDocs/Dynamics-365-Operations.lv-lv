---
title: "Atjaunināt standarta izmaksas ražošanas vidē"
description: "Šajā rakstā ir sniegti norādījumi par to, kā atjaunināt standarta izmaksas ar ražošanu vidē."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8dceb6ee278d222106e7f44b0aeea55a7a1b3f22
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="update-standard-costs-in-a-manufacturing-environment"></a><span data-ttu-id="c98db-103">Atjaunināt standarta izmaksas ražošanas vidē</span><span class="sxs-lookup"><span data-stu-id="c98db-103">Update standard costs in a manufacturing environment</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="c98db-104">Šajā rakstā ir sniegti norādījumi par to, kā atjaunināt standarta izmaksas ar ražošanu vidē.</span><span class="sxs-lookup"><span data-stu-id="c98db-104">This article provides guidance about how to update standard costs in a manufacturing environment.</span></span> 

<span data-ttu-id="c98db-105">Atjauninājumi var attiekties uz jauniem krājumiem, izmaksu kategorijām un netiešo izmaksu aprēķinu formulām.</span><span class="sxs-lookup"><span data-stu-id="c98db-105">Updates can reflect new items, cost categories, or indirect cost calculation formulas.</span></span> <span data-ttu-id="c98db-106">Tie var attiekties uz labojumiem un izmaksu izmaiņām.</span><span class="sxs-lookup"><span data-stu-id="c98db-106">They can also reflect corrections and cost changes.</span></span> <span data-ttu-id="c98db-107">Atjauninājuma veids ietekmē darbības, kas ir jāveic, lai atjauninātu standarta izmaksas, kā aprakstīts tālāk aprakstītajos gadījumos.</span><span class="sxs-lookup"><span data-stu-id="c98db-107">The type of update affects the steps that you must complete to update standard costs, as illustrated in the following cases:</span></span>

-   <span data-ttu-id="c98db-108">Ievadiet paredzamās pirkto krājumu standarta izmaksu izmaiņas, pēc tam izmainiet krājumu izmaksu ierakstu statusu **Aktīvs** attiecīgajā datumā.</span><span class="sxs-lookup"><span data-stu-id="c98db-108">Enter expected standard cost changes for purchased items, and then change the status of the item cost records to **Active** on the appropriate date.</span></span> <span data-ttu-id="c98db-109">Tomēr nepārrēķiniet ražoto krājumu, kas izmanto pirktos krājumus, izmaksas.</span><span class="sxs-lookup"><span data-stu-id="c98db-109">However, don't recalculate the costs of manufactured items that use the purchased items.</span></span>
-   <span data-ttu-id="c98db-110">Ievadiet jauna, pirkta krājuma standarta izmaksas, bet nepārrēķiniet ražoto krājumu izmaksas ar materiālu komplekta (MK) versiju, kurā jaunais pirktais krājums ir iekļauts kā komponents.</span><span class="sxs-lookup"><span data-stu-id="c98db-110">Enter standard costs for a new purchased item, but don't recalculate the costs of manufactured items that have a bill of materials (BOM) version that contains the new purchased item as a component.</span></span>
-   <span data-ttu-id="c98db-111">Izlabojiet vai izmainiet pirktā krājuma izmaksas, vai arī izmainiet pirktajam krājumam piešķirto izmaksu grupu un aprēķiniet visu ražoto krājumu izmaksas ar MK versiju, kas iekļauj pirkto krājumu kā komponentu.</span><span class="sxs-lookup"><span data-stu-id="c98db-111">Correct or change the cost of a purchased item, or change the cost group that is assigned to a purchased item, and calculate the cost for all manufactured items that have a BOM version that contains the purchased item as a component.</span></span>
-   <span data-ttu-id="c98db-112">Izmainiet izmaksu kategorijas izmaksas un aprēķiniet visu ražoto krājumu izmaksas ar maršrutēšanas versiju, kas iekļauj izmaksu kategoriju izmantojošās maršrutēšanas darbības.</span><span class="sxs-lookup"><span data-stu-id="c98db-112">Change the cost for a cost category, and calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="c98db-113">Izmainiet izmaksu kategorijas, kas ir piešķirtas maršrutēšanas darbībām vai izmaksu grupai, kas ir piešķirta izmaksu kategorijām.</span><span class="sxs-lookup"><span data-stu-id="c98db-113">Change the cost categories that are assigned to routing operations or the cost group that is assigned to cost categories.</span></span> <span data-ttu-id="c98db-114">Pēc tam aprēķiniet visu ražoto krājumu izmaksas ar maršrutēšanas versiju, kas iekļauj izmaksu kategoriju izmantojošās maršrutēšanas darbības.</span><span class="sxs-lookup"><span data-stu-id="c98db-114">Then calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="c98db-115">Izmainiet netiešo izmaksu aprēķināšanas formulu un aprēķiniet visu ražoto krājumu izmaksas, kuras ietekmē šīs izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="c98db-115">Change an indirect cost calculation formula, and calculate the cost for all manufactured items that are affected by the change.</span></span>
-   <span data-ttu-id="c98db-116">Izmainiet vai pievienojiet ražota krājuma ražošanas vietu un aprēķiniet krājuma ražošanas izmaksas vietai.</span><span class="sxs-lookup"><span data-stu-id="c98db-116">Change or add a manufacturing site for a manufactured item, and calculate the item's manufactured cost for the site.</span></span>
-   <span data-ttu-id="c98db-117">Aprēķiniet vai pārrēķiniet ražotā krājuma izmaksas un pārrēķiniet visu ražoto krājumu izmaksas ar MK versiju, kas iekļauj ražoto krājumu kā komponentu.</span><span class="sxs-lookup"><span data-stu-id="c98db-117">Calculate, or recalculate, the cost for a manufactured item, and recalculate the cost for all manufactured items that have a BOM version that contains the manufactured item as a component.</span></span>
-   <span data-ttu-id="c98db-118">Aprēķiniet jauna ražotā krājuma izmaksas, ņemot vērā tam noteiktos, apstiprinātos, aktīvā MK un maršruta datus.</span><span class="sxs-lookup"><span data-stu-id="c98db-118">Calculate costs for a new manufactured item, based on its defined, approved, and active BOM and route information.</span></span>

<span data-ttu-id="c98db-119">Katrs gadījums pieprasa nopietnus apsvērumus par to, kā atjaunināt standarta izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="c98db-119">Each case requires careful consideration about how to update standard costs.</span></span>




