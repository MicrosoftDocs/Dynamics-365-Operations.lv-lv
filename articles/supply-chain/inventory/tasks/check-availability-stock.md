---
title: Krājumu pieejamības pārbaude
description: Šajā procedūrā parādīts, kā pārbaudīt rīcībā esošos un fiziski rīcībā esošos krājumus noteiktam krājuma kodam.
author: ShylaThompson
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e76c123ffbeb33cbc3ba01b4b2758208ed0c445f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204221"
---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="8460d-103">Krājumu pieejamības pārbaude</span><span class="sxs-lookup"><span data-stu-id="8460d-103">Check the availability of stock</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8460d-104">Šajā procedūrā parādīts, kā pārbaudīt rīcībā esošos un fiziski rīcībā esošos krājumus noteiktam krājuma kodam.</span><span class="sxs-lookup"><span data-stu-id="8460d-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="8460d-105">Aprakstīts arī tas, kā iegūt piegādes informāciju, kas saistīta ar krājumu.</span><span class="sxs-lookup"><span data-stu-id="8460d-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="8460d-106">Fiziskie rīcībā esošie krājumi ir rīcībā esoši krājumi, kas ir pieejami, tas ir, tie ir nopirkti, saņemti un reģistrēti.</span><span class="sxs-lookup"><span data-stu-id="8460d-106">Physical on-hand inventory is the on-hand inventory that's available – that is, it's purchased, received and registered.</span></span> <span data-ttu-id="8460d-107">Rīcībā esošie krājumi ietver pieejamos rīcībā esošos krājumus, kā arī krājumus, kas ir pasūtīti un tiek gaidīti, bet vēl nav saņemti vai nav reģistrēti.</span><span class="sxs-lookup"><span data-stu-id="8460d-107">On-hand inventory includes the available on-hand inventory, but also the inventory that's been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="8460d-108">Šo procedūru var izmēģināt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="8460d-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="8460d-109">Ja izmantojat USMF varat izmantot piemēra vērtības, kas parādītas.</span><span class="sxs-lookup"><span data-stu-id="8460d-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="8460d-110">Šos uzdevumus parasti veic noliktavas darbinieks.</span><span class="sxs-lookup"><span data-stu-id="8460d-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="8460d-111">Krājuma rīcībā esošo krājumu pārbaude</span><span class="sxs-lookup"><span data-stu-id="8460d-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="8460d-112">Pārejiet uz **Navigācijas rūts > Moduļi > Krājumu vadība > Uzziņas un pārskati > Rīcībā esošie krājumi**.</span><span class="sxs-lookup"><span data-stu-id="8460d-112">Go to **Navigation pane > Modules > Inventory management > Inquiries and reports > On-hand inventory**.</span></span>
2. <span data-ttu-id="8460d-113">Atlasiet rindu **Krājuma numurs**.</span><span class="sxs-lookup"><span data-stu-id="8460d-113">Select the **Item number** row.</span></span> <span data-ttu-id="8460d-114">Lai izpildītu vaicājumu rīcībā esošiem krājumiem pēc krājuma koda, atlasiet rindu, kur tabulai ir iestatīti **Rīcībā esošie krājumi** un laukā ir iestatīts **Krājuma kods**.</span><span class="sxs-lookup"><span data-stu-id="8460d-114">To query the on-hand inventory by item number, select the row where the Table is set to **On-hand inventory** and Field is set to **Item** number.</span></span>
3. <span data-ttu-id="8460d-115">Laukā **Kritēriji** atlasiet krājumu, kuram vēlaties izpildīt vaicājumu.</span><span class="sxs-lookup"><span data-stu-id="8460d-115">In the **Criteria** field, select the item you want to query.</span></span> <span data-ttu-id="8460d-116">Ja lietojat demonstrācijas datu uzņēmumu USMF, varat atlasīt “M9201”.</span><span class="sxs-lookup"><span data-stu-id="8460d-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="8460d-117">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8460d-117">Click **OK**.</span></span>
5. <span data-ttu-id="8460d-118">**Darbību rūtī** noklikšķiniet uz **Dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="8460d-118">On the **Action pane**, click **Dimensions**.</span></span> <span data-ttu-id="8460d-119">Cilne **Dimensijas** ļauj atlasīt, cik daudz informācijas vēlaties redzēt par jūsu rīcībā esošajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="8460d-119">The **Dimensions** tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="8460d-120">Ja jums ir nepieciešami dati, kas attiecas uz rezervāciju, ir jāattēlo visas krājumu dimensijas krājumiem, kas izmanto papildu noliktavas (WHS) procesus.</span><span class="sxs-lookup"><span data-stu-id="8460d-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WHS) processes.</span></span>
6. <span data-ttu-id="8460d-121">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8460d-121">Click **OK**.</span></span>
7. <span data-ttu-id="8460d-122">**Darbību rūtī** noklikšķiniet uz **Saistītā informācija**.</span><span class="sxs-lookup"><span data-stu-id="8460d-122">On the **Action Pane**, click **Related information**.</span></span> <span data-ttu-id="8460d-123">Ja šī opcija nav redzama, iespējams, ir nepieciešams noklikšķināt uz elipses pogas (...), lai redzētu papildu darbību rūts opcijas.</span><span class="sxs-lookup"><span data-stu-id="8460d-123">If you don't see this option, you may need to click on the Ellipsis button (…) to see additional action pane options.</span></span>
8. <span data-ttu-id="8460d-124">Noklikšķiniet uz **Piegādes pārskats**.</span><span class="sxs-lookup"><span data-stu-id="8460d-124">Click **Supply overview**.</span></span> <span data-ttu-id="8460d-125">Cilne **Piegādes pārskats** sniedz piegādes informāciju noteiktam krājumam, piemēram, rīcībā esošo daudzumu, izpildes laiku un kreditora informāciju.</span><span class="sxs-lookup"><span data-stu-id="8460d-125">The **Supply overview** tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="8460d-126">Izvērsiet sadaļu **Rīcībā esošs**.</span><span class="sxs-lookup"><span data-stu-id="8460d-126">Expand the **On-hand** section.</span></span>
10. <span data-ttu-id="8460d-127">Izvērsiet sadaļu **Piegādātāji**.</span><span class="sxs-lookup"><span data-stu-id="8460d-127">Expand the **Vendors** section.</span></span>
11. <span data-ttu-id="8460d-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="8460d-128">Close the page.</span></span>
12. <span data-ttu-id="8460d-129">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="8460d-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="8460d-130">Fizisko rīcībā esošo krājumu pārbaude</span><span class="sxs-lookup"><span data-stu-id="8460d-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="8460d-131">Pārejiet uz **Navigācijas rūts > Moduļi > Npliktava vadība > Uzziņas un pārskati > Fiziskie rīcībā esošie krājumi**.</span><span class="sxs-lookup"><span data-stu-id="8460d-131">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > Physical on-hand inventory**.</span></span>
2. <span data-ttu-id="8460d-132">Laukā **Krājuma kods** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8460d-132">In the **Item number** field, type a value.</span></span> <span data-ttu-id="8460d-133">Laukus Vieta un Noliktava var izmantot krājumu sarakstu filtrēšanai.</span><span class="sxs-lookup"><span data-stu-id="8460d-133">You can use the Site and Warehouse fields to filter the list of items.</span></span> 
3. <span data-ttu-id="8460d-134">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="8460d-134">Refresh the page.</span></span>
4. <span data-ttu-id="8460d-135">Darbību rūtī **Darbību rūtī** noklikšķiniet uz **Parādīt dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="8460d-135">On the **Action pane**, click **Display Dimensions**.</span></span> <span data-ttu-id="8460d-136">Cilne Dimensiju ekrāns ļauj atlasīt, cik daudz informācijas vēlaties redzēt par jūsu rīcībā esošajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="8460d-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>
5. <span data-ttu-id="8460d-137">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8460d-137">Click **OK**.</span></span>
6. <span data-ttu-id="8460d-138">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="8460d-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="8460d-139">Rīcībā esošo krājumu pārbaude pēc atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="8460d-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="8460d-140">Pārejiet uz **Navigācijas rūts > Moduļi > Npliktava vadība > Uzziņas un pārskati > Fiziskie rīcībā esošie pēc atrašanās vietas**.</span><span class="sxs-lookup"><span data-stu-id="8460d-140">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > On hand by location**.</span></span>
2. <span data-ttu-id="8460d-141">Laukā **Noliktava** atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8460d-141">In the **Warehouse** field, type a value.</span></span> <span data-ttu-id="8460d-142">Ja jūs izmantojat USMF demonstrācijas datus uzņēmuma, varat izmantot '51'.</span><span class="sxs-lookup"><span data-stu-id="8460d-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="8460d-143">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="8460d-143">Refresh the page.</span></span>
4. <span data-ttu-id="8460d-144">Noklikšķiniet uz **Parādīt dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="8460d-144">Click **Display Dimensions**.</span></span>
5. <span data-ttu-id="8460d-145">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8460d-145">Click **OK**.</span></span>
6. <span data-ttu-id="8460d-146">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="8460d-146">Close the page.</span></span>

