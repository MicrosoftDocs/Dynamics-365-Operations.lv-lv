---
title: Krājuma bloķēšanas izveide un uzturēšana
description: Šajā procedūrā parādīts, kā citos izejošos pirmdokumentos neļaut rezervēt fiziski rīcībā esošus krājumus, izmantojot krājumu aizturēšanu.
author: perlynne
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 12c6e047e15aaab157e6de70f4a09f500af2965f
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383462"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="07314-103">Krājuma bloķēšanas izveide un uzturēšana</span><span class="sxs-lookup"><span data-stu-id="07314-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="07314-104">Šajā procedūrā parādīts, kā citos izejošos pirmdokumentos neļaut rezervēt fiziski rīcībā esošus krājumus, izmantojot krājumu aizturēšanu.</span><span class="sxs-lookup"><span data-stu-id="07314-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="07314-105">Šo procedūru varat palaist demonstrācijas datu uzņēmumā USMF, izmantojot piemēra vērtības.</span><span class="sxs-lookup"><span data-stu-id="07314-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="07314-106">Pirms šīs procedūras uzsākšanas, jums ir jābūt pieejamiem fiziski rīcībā esošiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="07314-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="07314-107">Krājumu bloķēšanas izveide</span><span class="sxs-lookup"><span data-stu-id="07314-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="07314-108">**Navigācijas rūtī** ejiet uz **Moduļi > Krājumu pārvaldība > Periodiskie uzdevumi > Krājumu bloķēšana**.</span><span class="sxs-lookup"><span data-stu-id="07314-108">In the **Navigation pane**, go to **Modules > Inventory management > Periodic tasks > Inventory blocking**.</span></span>
2. <span data-ttu-id="07314-109">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="07314-109">Click **New**.</span></span>
3. <span data-ttu-id="07314-110">Laukā **Krājuma kods** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="07314-110">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="07314-111">Sarakstā atlasiet krājumu, kuru vēlaties izmantot.</span><span class="sxs-lookup"><span data-stu-id="07314-111">In the list, select the item you want to choose.</span></span> <span data-ttu-id="07314-112">Atlasiet krājuma numuru no fiziski rīcībā esošiem krājumiem, kuru vēlaties bloķēt.</span><span class="sxs-lookup"><span data-stu-id="07314-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="07314-113">Ja izmantojat USMF, varat atlasīt krājumu M9201.</span><span class="sxs-lookup"><span data-stu-id="07314-113">If you're using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="07314-114">Laukā **Daudzums** ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="07314-114">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="07314-115">Ja lietojat krājumu M9201, ir jāatlasa mazāk par 200 vienībām.</span><span class="sxs-lookup"><span data-stu-id="07314-115">If you're using item M9201, you need to select less than 200.</span></span>
6. <span data-ttu-id="07314-116">Izvērsiet kopsavilkuma cilni **Krājumu izmēri**.</span><span class="sxs-lookup"><span data-stu-id="07314-116">Expand the **Inventory dimensions** fastTab.</span></span>
7. <span data-ttu-id="07314-117">Laukā **Noliktava** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="07314-117">In the **Warehouse** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="07314-118">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="07314-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="07314-119">Ja izmantojat krājumu M9201, varat atlasīt 51. noliktavu.</span><span class="sxs-lookup"><span data-stu-id="07314-119">If you're using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="07314-120">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="07314-120">Click **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="07314-121">Krājumu bloķēšanas nosacījumu atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="07314-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="07314-122">Kopsavilkuma cilnē **Vispārīgi** laukā **Daudzums** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="07314-122">In the **General** fastTab, in the **Quantity** field, enter a number.</span></span> <span data-ttu-id="07314-123">Atjauniniet krājumu daudzuma lauku, lai atspoguļotu bloķējamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="07314-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="07314-124">Laukā **Paredzamais datums** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="07314-124">In the **Expected date** field, enter a date.</span></span> <span data-ttu-id="07314-125">Varat norādīt, kad bloķētie krājumi varētu kļūt pieejami rezervācijai, norādot paredzamo datumu.</span><span class="sxs-lookup"><span data-stu-id="07314-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="07314-126">Ja krājumu bloķēšanai ir atlasīta opcija Paredzamā saņemšana, kā tas ir pēc noklusējuma, manuāli izveidojot bloķēšanas pavēli, šis datums tiks attēlots paredzamajā transakcijā.</span><span class="sxs-lookup"><span data-stu-id="07314-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="07314-127">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="07314-127">Click **Save**.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="07314-128">Krājuma bloķēšanas noņemšana</span><span class="sxs-lookup"><span data-stu-id="07314-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="07314-129">**Darbību rūtī** noklikšķiniet uz **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="07314-129">On the **Action Pane**, click **Delete**.</span></span>
2. <span data-ttu-id="07314-130">Noklikšķiniet uz pogas **Jā**.</span><span class="sxs-lookup"><span data-stu-id="07314-130">Click **Yes**.</span></span>
3. <span data-ttu-id="07314-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="07314-131">Close the page.</span></span>

