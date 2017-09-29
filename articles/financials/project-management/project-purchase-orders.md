---
title: "Projektam paredzēti pirkšanas pasūtījumi"
description: "Šajā rakstā ir aprakstītas dažādas metodes, ko var izmantot, lai izveidotu projektam paredzētus pirkšanas pasūtījumus. Izmantojamā metode ir atkarīga no pirkšanas pasūtījuma mērķa, kad iepirktie krājumi tiek patērēti un to izmaksas tiek attiecinātas uz projektu."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: 985a57ae9fb116b1c4514b836b35c5da0f8838fd
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2017

---

# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="d3752-104">Projektam paredzēti pirkšanas pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="d3752-104">Purchase orders for a project</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d3752-105">Šajā rakstā ir aprakstītas dažādas metodes, ko var izmantot, lai izveidotu projektam paredzētus pirkšanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="d3752-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="d3752-106">Izmantojamā metode ir atkarīga no pirkšanas pasūtījuma mērķa, kad iepirktie krājumi tiek patērēti un to izmaksas tiek attiecinātas uz projektu.</span><span class="sxs-lookup"><span data-stu-id="d3752-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

<span data-ttu-id="d3752-107">Programmatūras Microsoft Dynamics 365 for Finance and Operations izdevumā Enterprise varat izmantot vairākas metodes, lai izveidotu projekta pirkšanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="d3752-107">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, you can use multiple methods to create purchase orders for a project.</span></span> <span data-ttu-id="d3752-108">Izmantojamā metode ir atkarīga no pirkšanas pasūtījuma mērķa, kad iepirktie krājumi tiek patērēti un kad iepirkto krājumu izmaksas tiek attiecinātas uz projektu.</span><span class="sxs-lookup"><span data-stu-id="d3752-108">The method that you use depends on the purpose of the purchase order, when the purchased items are consumed, and when the purchased items are charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="d3752-109">Pirkšanas pasūtījuma izveides metodes</span><span class="sxs-lookup"><span data-stu-id="d3752-109">Methods for creating a purchase order</span></span>

<span data-ttu-id="d3752-110">Lai izveidotu pirkšanas pasūtījumu projektu vadības un uzskaites modulī, var izmantot vienu no tālāk aprakstītajām metodēm.</span><span class="sxs-lookup"><span data-stu-id="d3752-110">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="d3752-111">Pirkšanas pasūtījuma mērķis nosaka, kad pirkšanas pasūtījums tiek izmantots, un, līdz ar to, kad krājumu izmaksas tiek attiecinātas uz projektu.</span><span class="sxs-lookup"><span data-stu-id="d3752-111">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d3752-112">Metode</span><span class="sxs-lookup"><span data-stu-id="d3752-112">Method</span></span></th>
<th><span data-ttu-id="d3752-113">Mērķis</span><span class="sxs-lookup"><span data-stu-id="d3752-113">Purpose</span></span></th>
<th><span data-ttu-id="d3752-114">Krājumu patēriņš</span><span class="sxs-lookup"><span data-stu-id="d3752-114">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d3752-115">Izveidojiet pirkšanas pasūtījumu tieši no projekta.</span><span class="sxs-lookup"><span data-stu-id="d3752-115">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="d3752-116">Izmantojiet šo metodi, lai iegādātos krājumus ārējam kreditoram izmantošanai projektā.</span><span class="sxs-lookup"><span data-stu-id="d3752-116">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="d3752-117">Pirkšanas pasūtījumu var izveidot divējādi.</span><span class="sxs-lookup"><span data-stu-id="d3752-117">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="d3752-118">No paša projekta.</span><span class="sxs-lookup"><span data-stu-id="d3752-118">From the project itself.</span></span> <span data-ttu-id="d3752-119">Šajā gadījumā projekts ir jau definēts pirkšanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="d3752-119">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="d3752-120">Pārejot uz projekta pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="d3752-120">By navigating to the project purchase order.</span></span> <span data-ttu-id="d3752-121">Jums ir jāizvēlas gan kreditors, gan projekts, kuram veidot pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="d3752-121">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="d3752-122">Krājumus izmanto, kad kreditora rēķins tiek atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="d3752-122">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3752-123">Izveidot pirkšanas pasūtījumu no pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="d3752-123">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="d3752-124">Izmantojiet šo metodi, ja vēlaties pirkt krājumus, veidojot pārdošanas pasūtījumu no projekta.</span><span class="sxs-lookup"><span data-stu-id="d3752-124">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="d3752-125">Krājumus izmanto, kad tiek izveidots pārdošanas pasūtījuma rēķins debitoram.</span><span class="sxs-lookup"><span data-stu-id="d3752-125">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3752-126">Izveidot pirkšanas pasūtījumu no krājumu vajadzības.</span><span class="sxs-lookup"><span data-stu-id="d3752-126">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="d3752-127">Izmantojiet šo metodi, ja vēlaties pirkt krājumus, izveidojot krājumu vajadzību no projekta.</span><span class="sxs-lookup"><span data-stu-id="d3752-127">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="d3752-128">Krājumus izmanto, atjauninot krājumu vajadzības pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="d3752-128">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="d3752-129">Kad jaunināt kreditora rēķinu vai pavadzīmi, tiek parādīta uzvedne ar aicinājumu atjaunināt krājumu vajadzības pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="d3752-129">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="d3752-130">Plašāku informāciju skatiet šeit: [Saņemt pirkšanas pasūtījuma krājumus no krājumu vajadzības](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="d3752-130">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>


