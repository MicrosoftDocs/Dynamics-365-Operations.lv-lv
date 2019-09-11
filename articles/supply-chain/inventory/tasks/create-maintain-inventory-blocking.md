---
title: Krājuma bloķēšanas izveide un uzturēšana
description: Šajā procedūrā parādīts, kā citos izejošos pirmdokumentos neļaut rezervēt fiziski rīcībā esošus krājumus, izmantojot krājumu aizturēšanu.
author: perlynne
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2485eaf31226b11106895074ae0ad95e561777b
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916603"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="eb57d-103">Krājuma bloķēšanas izveide un uzturēšana</span><span class="sxs-lookup"><span data-stu-id="eb57d-103">Create and maintain an inventory blocking</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eb57d-104">Šajā procedūrā parādīts, kā citos izejošos pirmdokumentos neļaut rezervēt fiziski rīcībā esošus krājumus, izmantojot krājumu aizturēšanu.</span><span class="sxs-lookup"><span data-stu-id="eb57d-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="eb57d-105">Šo procedūru varat palaist demonstrācijas datu uzņēmumā USMF, izmantojot piemēra vērtības.</span><span class="sxs-lookup"><span data-stu-id="eb57d-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="eb57d-106">Pirms šīs procedūras uzsākšanas, jums ir jābūt pieejamiem fiziski rīcībā esošiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="eb57d-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="eb57d-107">Krājumu bloķēšanas izveide</span><span class="sxs-lookup"><span data-stu-id="eb57d-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="eb57d-108">**Navigācijas rūtī** ejiet uz **Moduļi > Krājumu pārvaldība > Periodiskie uzdevumi > Krājumu bloķēšana**.</span><span class="sxs-lookup"><span data-stu-id="eb57d-108">In the **Navigation pane**, go to **Modules > Inventory management > Periodic tasks > Inventory blocking**.</span></span>
2. <span data-ttu-id="eb57d-109">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="eb57d-109">Click **New**.</span></span>
3. <span data-ttu-id="eb57d-110">Laukā **Krājuma kods** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="eb57d-110">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="eb57d-111">Sarakstā atlasiet krājumu, kuru vēlaties izmantot.</span><span class="sxs-lookup"><span data-stu-id="eb57d-111">In the list, select the item you want to choose.</span></span> <span data-ttu-id="eb57d-112">Atlasiet krājuma numuru no fiziski rīcībā esošiem krājumiem, kuru vēlaties bloķēt.</span><span class="sxs-lookup"><span data-stu-id="eb57d-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="eb57d-113">Ja izmantojat USMF, varat atlasīt krājumu M9201.</span><span class="sxs-lookup"><span data-stu-id="eb57d-113">If you’re using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="eb57d-114">Laukā **Daudzums** ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="eb57d-114">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="eb57d-115">Ja lietojat krājumu M9201, ir jāatlasa mazāk par 200 vienībām.</span><span class="sxs-lookup"><span data-stu-id="eb57d-115">If you’re using item M9201, you need to select less than 200.</span></span>
6. <span data-ttu-id="eb57d-116">Izvērsiet kopsavilkuma cilni **Krājumu izmēri**.</span><span class="sxs-lookup"><span data-stu-id="eb57d-116">Expand the **Inventory dimensions** fastTab.</span></span>
7. <span data-ttu-id="eb57d-117">Laukā **Noliktava** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="eb57d-117">In the **Warehouse** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="eb57d-118">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="eb57d-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="eb57d-119">Ja izmantojat krājumu M9201, varat atlasīt 51. noliktavu.</span><span class="sxs-lookup"><span data-stu-id="eb57d-119">If you’re using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="eb57d-120">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="eb57d-120">Click **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="eb57d-121">Krājumu bloķēšanas nosacījumu atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="eb57d-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="eb57d-122">Kopsavilkuma cilnē **Vispārīgi** laukā **Daudzums** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="eb57d-122">In the **General** fastTab, in the **Quantity** field, enter a number.</span></span> <span data-ttu-id="eb57d-123">Atjauniniet krājumu daudzuma lauku, lai atspoguļotu bloķējamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="eb57d-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="eb57d-124">Laukā **Paredzamais datums** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="eb57d-124">In the **Expected date** field, enter a date.</span></span> <span data-ttu-id="eb57d-125">Varat norādīt, kad bloķētie krājumi varētu kļūt pieejami rezervācijai, norādot paredzamo datumu.</span><span class="sxs-lookup"><span data-stu-id="eb57d-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="eb57d-126">Ja krājumu bloķēšanai ir atlasīta opcija Paredzamā saņemšana, kā tas ir pēc noklusējuma, manuāli izveidojot bloķēšanas pavēli, šis datums tiks attēlots paredzamajā transakcijā.</span><span class="sxs-lookup"><span data-stu-id="eb57d-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="eb57d-127">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="eb57d-127">Click **Save**.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="eb57d-128">Krājuma bloķēšanas noņemšana</span><span class="sxs-lookup"><span data-stu-id="eb57d-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="eb57d-129">**Darbību rūtī** noklikšķiniet uz **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="eb57d-129">On the **Action pane**, click **Delete**.</span></span>
2. <span data-ttu-id="eb57d-130">Noklikšķiniet uz pogas **Jā**.</span><span class="sxs-lookup"><span data-stu-id="eb57d-130">Click **Yes**.</span></span>
3. <span data-ttu-id="eb57d-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="eb57d-131">Close the page.</span></span>

