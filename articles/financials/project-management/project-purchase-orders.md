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
ms.search.form: ProjTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 1797bc49877f1c8c06797083d1c7b76934675ba3
ms.contentlocale: lv-lv
ms.lasthandoff: 02/07/2018

---

# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="3198d-104">Projektam paredzēti pirkšanas pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="3198d-104">Purchase orders for a project</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3198d-105">Šajā rakstā ir aprakstītas dažādas metodes, ko var izmantot, lai izveidotu projektam paredzētus pirkšanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="3198d-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="3198d-106">Izmantojamā metode ir atkarīga no pirkšanas pasūtījuma mērķa, kad iepirktie krājumi tiek patērēti un to izmaksas tiek attiecinātas uz projektu.</span><span class="sxs-lookup"><span data-stu-id="3198d-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

<span data-ttu-id="3198d-107">Programmatūras Microsoft Dynamics 365 for Finance and Operations izdevumā Enterprise varat izmantot vairākas metodes, lai izveidotu projekta pirkšanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="3198d-107">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, you can use multiple methods to create purchase orders for a project.</span></span> <span data-ttu-id="3198d-108">Izmantojamā metode ir atkarīga no pirkšanas pasūtījuma mērķa, kad iepirktie krājumi tiek patērēti un kad iepirkto krājumu izmaksas tiek attiecinātas uz projektu.</span><span class="sxs-lookup"><span data-stu-id="3198d-108">The method that you use depends on the purpose of the purchase order, when the purchased items are consumed, and when the purchased items are charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="3198d-109">Pirkšanas pasūtījuma izveides metodes</span><span class="sxs-lookup"><span data-stu-id="3198d-109">Methods for creating a purchase order</span></span>

<span data-ttu-id="3198d-110">Lai izveidotu pirkšanas pasūtījumu projektu vadības un uzskaites modulī, var izmantot vienu no tālāk aprakstītajām metodēm.</span><span class="sxs-lookup"><span data-stu-id="3198d-110">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="3198d-111">Pirkšanas pasūtījuma mērķis nosaka, kad pirkšanas pasūtījums tiek izmantots, un, līdz ar to, kad krājumu izmaksas tiek attiecinātas uz projektu.</span><span class="sxs-lookup"><span data-stu-id="3198d-111">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3198d-112">Metode</span><span class="sxs-lookup"><span data-stu-id="3198d-112">Method</span></span></th>
<th><span data-ttu-id="3198d-113">Mērķis</span><span class="sxs-lookup"><span data-stu-id="3198d-113">Purpose</span></span></th>
<th><span data-ttu-id="3198d-114">Krājumu patēriņš</span><span class="sxs-lookup"><span data-stu-id="3198d-114">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3198d-115">Izveidojiet pirkšanas pasūtījumu tieši no projekta.</span><span class="sxs-lookup"><span data-stu-id="3198d-115">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="3198d-116">Izmantojiet šo metodi, lai iegādātos krājumus ārējam kreditoram izmantošanai projektā.</span><span class="sxs-lookup"><span data-stu-id="3198d-116">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="3198d-117">Pirkšanas pasūtījumu var izveidot divējādi.</span><span class="sxs-lookup"><span data-stu-id="3198d-117">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="3198d-118">No paša projekta.</span><span class="sxs-lookup"><span data-stu-id="3198d-118">From the project itself.</span></span> <span data-ttu-id="3198d-119">Šajā gadījumā projekts ir jau definēts pirkšanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="3198d-119">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="3198d-120">Pārejot uz projekta pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="3198d-120">By navigating to the project purchase order.</span></span> <span data-ttu-id="3198d-121">Jums ir jāizvēlas gan kreditors, gan projekts, kuram veidot pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="3198d-121">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="3198d-122">Krājumus izmanto, kad kreditora rēķins tiek atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="3198d-122">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3198d-123">Izveidot pirkšanas pasūtījumu no pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="3198d-123">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="3198d-124">Izmantojiet šo metodi, ja vēlaties pirkt krājumus, veidojot pārdošanas pasūtījumu no projekta.</span><span class="sxs-lookup"><span data-stu-id="3198d-124">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="3198d-125">Krājumus izmanto, kad tiek izveidots pārdošanas pasūtījuma rēķins debitoram.</span><span class="sxs-lookup"><span data-stu-id="3198d-125">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3198d-126">Izveidot pirkšanas pasūtījumu no krājumu vajadzības.</span><span class="sxs-lookup"><span data-stu-id="3198d-126">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="3198d-127">Izmantojiet šo metodi, ja vēlaties pirkt krājumus, izveidojot krājumu vajadzību no projekta.</span><span class="sxs-lookup"><span data-stu-id="3198d-127">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="3198d-128">Krājumus izmanto, atjauninot krājumu vajadzības pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="3198d-128">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="3198d-129">Kad jaunināt kreditora rēķinu vai pavadzīmi, tiek parādīta uzvedne ar aicinājumu atjaunināt krājumu vajadzības pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="3198d-129">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="3198d-130">Plašāku informāciju skatiet šeit: [Saņemt pirkšanas pasūtījuma krājumus no krājumu vajadzības](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="3198d-130">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>


