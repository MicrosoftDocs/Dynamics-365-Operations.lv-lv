---
title: Pirkšanas pasūtījuma krājumu saņemšana no krājumu vajadzības
description: Šajā tēmā ir aprakstīts, kā saņemt pirkšanas pasūtījuma krājumus no krājuma vajadzības.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7afdae65c5ae7e3196c6b9f142dd87aec39b5ea3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174424"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="2cf5d-103">Pirkšanas pasūtījuma krājumu saņemšana no krājumu vajadzības</span><span class="sxs-lookup"><span data-stu-id="2cf5d-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2cf5d-104">Šajā tēmā ir aprakstīts, kā saņemt pirkšanas pasūtījuma krājumus no krājuma vajadzības.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="2cf5d-105">Ja krājumu darījuma vietā izmantojat krājuma vajadzību, varat plānot piegādi tieši pirms krājuma faktiskās izmantošanas, izveidot pirkšanas pasūtījumu, iekļaut krājumu tirdzniecības līguma struktūrā un iekļaut krājuma vajadzību ražošanas plānošanā.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="2cf5d-106">Šajā uzdevumā tiek izmantota USSI datu kopa.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="2cf5d-107">Navigācijas rūtī atveriet **Moduļi > Projektu pārvaldība un uzskaite > Projekti > Visiem projekti**.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="2cf5d-108">Sarakstā atlasiet saiti vēlamajā rindā.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="2cf5d-109">Darbību rūtī atlasiet **Plāns**.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="2cf5d-110">Atlasiet vienumu **Krājumu vajadzības**.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="2cf5d-111">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-111">Select **New**.</span></span>
6. <span data-ttu-id="2cf5d-112">Juanā rindā ievadiet vai atlasiet vērtību laukā **Krājuma numurs**.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="2cf5d-113">Laukā **Daudzums** ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="2cf5d-114">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-114">Select **Save**.</span></span>
9. <span data-ttu-id="2cf5d-115">Darbību rūtī atlasiet **Pārvaldīt**.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="2cf5d-116">Atlasiet **Funkcijas**.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-116">Select **Functions**.</span></span>
11. <span data-ttu-id="2cf5d-117">Atlasiet **Izveidot pirkšanas pasūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="2cf5d-118">Atzīmējiet izvēles rūtiņu **Iekļaut visus**.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="2cf5d-119">Laukā **Kreditora konts** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="2cf5d-120">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-120">Select **OK**.</span></span>
15. <span data-ttu-id="2cf5d-121">Navigācijas rūtī atveriet **Moduļi > Kreditori > Pirkšanas pieprasījumi > Visi pirkšanas pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="2cf5d-122">Sarakstā atlasiet saiti vēlamajā rindā.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="2cf5d-123">Darbību rūtī atlasiet **Iegādāties**.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="2cf5d-124">Atlasiet **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="2cf5d-125">Darbību rūtī atlasiet **Saņemt**.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="2cf5d-126">Atlasiet **Preču ieejas plūsma**.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="2cf5d-127">Laukā **Prod. ieejas pl.** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="2cf5d-128">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2cf5d-128">Select **OK**.</span></span>

