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
ms.openlocfilehash: e76c3d1f46e31dcd2171682a629dabe5bf5db418
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204152"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="1ecb2-103">Krājuma bloķēšanas izveide un uzturēšana</span><span class="sxs-lookup"><span data-stu-id="1ecb2-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1ecb2-104">Šajā procedūrā parādīts, kā citos izejošos pirmdokumentos neļaut rezervēt fiziski rīcībā esošus krājumus, izmantojot krājumu aizturēšanu.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="1ecb2-105">Šo procedūru varat palaist demonstrācijas datu uzņēmumā USMF, izmantojot piemēra vērtības.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="1ecb2-106">Pirms šīs procedūras uzsākšanas, jums ir jābūt pieejamiem fiziski rīcībā esošiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="1ecb2-107">Krājumu bloķēšanas izveide</span><span class="sxs-lookup"><span data-stu-id="1ecb2-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="1ecb2-108">**Navigācijas rūtī** ejiet uz **Moduļi > Krājumu pārvaldība > Periodiskie uzdevumi > Krājumu bloķēšana**.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-108">In the **Navigation pane**, go to **Modules > Inventory management > Periodic tasks > Inventory blocking**.</span></span>
2. <span data-ttu-id="1ecb2-109">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-109">Click **New**.</span></span>
3. <span data-ttu-id="1ecb2-110">Laukā **Krājuma kods** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-110">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="1ecb2-111">Sarakstā atlasiet krājumu, kuru vēlaties izmantot.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-111">In the list, select the item you want to choose.</span></span> <span data-ttu-id="1ecb2-112">Atlasiet krājuma numuru no fiziski rīcībā esošiem krājumiem, kuru vēlaties bloķēt.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="1ecb2-113">Ja izmantojat USMF, varat atlasīt krājumu M9201.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-113">If you're using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="1ecb2-114">Laukā **Daudzums** ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-114">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="1ecb2-115">Ja lietojat krājumu M9201, ir jāatlasa mazāk par 200 vienībām.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-115">If you're using item M9201, you need to select less than 200.</span></span>
6. <span data-ttu-id="1ecb2-116">Izvērsiet kopsavilkuma cilni **Krājumu izmēri**.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-116">Expand the **Inventory dimensions** fastTab.</span></span>
7. <span data-ttu-id="1ecb2-117">Laukā **Noliktava** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-117">In the **Warehouse** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="1ecb2-118">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="1ecb2-119">Ja izmantojat krājumu M9201, varat atlasīt 51. noliktavu.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-119">If you're using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="1ecb2-120">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-120">Click **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="1ecb2-121">Krājumu bloķēšanas nosacījumu atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="1ecb2-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="1ecb2-122">Kopsavilkuma cilnē **Vispārīgi** laukā **Daudzums** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-122">In the **General** fastTab, in the **Quantity** field, enter a number.</span></span> <span data-ttu-id="1ecb2-123">Atjauniniet krājumu daudzuma lauku, lai atspoguļotu bloķējamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="1ecb2-124">Laukā **Paredzamais datums** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-124">In the **Expected date** field, enter a date.</span></span> <span data-ttu-id="1ecb2-125">Varat norādīt, kad bloķētie krājumi varētu kļūt pieejami rezervācijai, norādot paredzamo datumu.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="1ecb2-126">Ja krājumu bloķēšanai ir atlasīta opcija Paredzamā saņemšana, kā tas ir pēc noklusējuma, manuāli izveidojot bloķēšanas pavēli, šis datums tiks attēlots paredzamajā transakcijā.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="1ecb2-127">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-127">Click **Save**.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="1ecb2-128">Krājuma bloķēšanas noņemšana</span><span class="sxs-lookup"><span data-stu-id="1ecb2-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="1ecb2-129">**Darbību rūtī** noklikšķiniet uz **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-129">On the **Action pane**, click **Delete**.</span></span>
2. <span data-ttu-id="1ecb2-130">Noklikšķiniet uz pogas **Jā**.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-130">Click **Yes**.</span></span>
3. <span data-ttu-id="1ecb2-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1ecb2-131">Close the page.</span></span>

