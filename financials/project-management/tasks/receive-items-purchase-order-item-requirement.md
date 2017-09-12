--- 
title: "Pirkšanas pasūtījuma krājumu saņemšana no krājumu vajadzības"
description: "Šajā procedūrā ir parādīts, kā saņemt pirkšanas pasūtījuma krājumus no krājumu vajadzības."
author: KimANelson
manager: AnnBe
ms.date: 02/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7c9093439c4c0c4645d96ad97ba56f31026ec334
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="b6292-103">Pirkšanas pasūtījuma krājumu saņemšana no krājumu vajadzības</span><span class="sxs-lookup"><span data-stu-id="b6292-103">Receive items on purchase order from item requirement</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b6292-104">Šajā procedūrā ir parādīts, kā saņemt pirkšanas pasūtījuma krājumus no krājumu vajadzības.</span><span class="sxs-lookup"><span data-stu-id="b6292-104">This procedure shows how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="b6292-105">Ja krājumu darījuma vietā izmantojat krājuma vajadzību, varat plānot piegādi tieši pirms krājuma faktiskās izmantošanas, izveidot pirkšanas pasūtījumu, iekļaut krājumu tirdzniecības līguma struktūrā un iekļaut krājuma vajadzību ražošanas plānošanā.</span><span class="sxs-lookup"><span data-stu-id="b6292-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="b6292-106">Šajā uzdevumā tiek izmantota USSI datu kopa.</span><span class="sxs-lookup"><span data-stu-id="b6292-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="b6292-107">Dodieties uz Projektu vadība un uzskaite > Projekti > Visi projekti.</span><span class="sxs-lookup"><span data-stu-id="b6292-107">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="b6292-108">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b6292-108">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="b6292-109">Darbību rūtī noklikšķiniet uz Plānot.</span><span class="sxs-lookup"><span data-stu-id="b6292-109">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="b6292-110">Noklikšķiniet uz Krājumu vajadzības.</span><span class="sxs-lookup"><span data-stu-id="b6292-110">Click Item requirements.</span></span>
5. <span data-ttu-id="b6292-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b6292-111">Click New.</span></span>
6. <span data-ttu-id="b6292-112">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="b6292-112">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="b6292-113">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b6292-113">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="b6292-114">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="b6292-114">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="b6292-115">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b6292-115">Click Save.</span></span>
10. <span data-ttu-id="b6292-116">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="b6292-116">On the Action Pane, click Manage.</span></span>
11. <span data-ttu-id="b6292-117">Noklikšķiniet uz Funkcijas.</span><span class="sxs-lookup"><span data-stu-id="b6292-117">Click Functions.</span></span>
12. <span data-ttu-id="b6292-118">Noklikšķiniet uz Izveidot pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="b6292-118">Click Create purchase order.</span></span>
13. <span data-ttu-id="b6292-119">Atzīmējiet izvēles rūtiņu Iekļaut.</span><span class="sxs-lookup"><span data-stu-id="b6292-119">Select the Include check box.</span></span>
14. <span data-ttu-id="b6292-120">Ievadiet vai atlasiet vērtību laukā kreditora konts.</span><span class="sxs-lookup"><span data-stu-id="b6292-120">In the Vendor account field, enter or select a value.</span></span>
15. <span data-ttu-id="b6292-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="b6292-121">Click OK.</span></span>
16. <span data-ttu-id="b6292-122">Pārejiet uz sadaļu Kreditori > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="b6292-122">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
17. <span data-ttu-id="b6292-123">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b6292-123">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="b6292-124">Darbību rūtī noklikšķiniet uz Pirkt.</span><span class="sxs-lookup"><span data-stu-id="b6292-124">On the Action Pane, click Purchase.</span></span>
19. <span data-ttu-id="b6292-125">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="b6292-125">Click Confirm.</span></span>
20. <span data-ttu-id="b6292-126">Darbību rūtī noklikšķiniet uz Saņemt.</span><span class="sxs-lookup"><span data-stu-id="b6292-126">On the Action Pane, click Receive.</span></span>
21. <span data-ttu-id="b6292-127">Noklikšķiniet uz Produktu ieejas plūsma.</span><span class="sxs-lookup"><span data-stu-id="b6292-127">Click Product receipt.</span></span>
22. <span data-ttu-id="b6292-128">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="b6292-128">In the list, mark the selected row.</span></span>
23. <span data-ttu-id="b6292-129">Laukā Produktu ieejas plūsma ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b6292-129">In the Product receipt field, type a value.</span></span>
24. <span data-ttu-id="b6292-130">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="b6292-130">Click OK.</span></span>


