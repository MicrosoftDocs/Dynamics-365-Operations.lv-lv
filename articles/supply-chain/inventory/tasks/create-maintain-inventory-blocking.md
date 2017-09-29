---
title: "Krājumu aizturēšanas izveide un uzturēšana"
description: "Šajā procedūrā parādīts, kā citos izejošos pirmdokumentos neļaut rezervēt fiziski rīcībā esošus krājumus, izmantojot krājumu aizturēšanu."
author: perlynne
manager: AnnBe
ms.date: 12/02/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 7272349cf16b9459823a752b8d3df915f42606ef
ms.contentlocale: lv-lv
ms.lasthandoff: 09/12/2017

---
# <a name="create-and-maintain-inventory-blocking"></a><span data-ttu-id="bb671-103">Krājumu aizturēšanas izveide un uzturēšana</span><span class="sxs-lookup"><span data-stu-id="bb671-103">Create and maintain inventory blocking</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bb671-104">Šajā procedūrā parādīts, kā citos izejošos pirmdokumentos neļaut rezervēt fiziski rīcībā esošus krājumus, izmantojot krājumu aizturēšanu.</span><span class="sxs-lookup"><span data-stu-id="bb671-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="bb671-105">Šo procedūru varat palaist demonstrācijas datu uzņēmumā USMF, izmantojot piemēra vērtības.</span><span class="sxs-lookup"><span data-stu-id="bb671-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="bb671-106">Pirms šīs procedūras uzsākšanas, jums ir jābūt pieejamiem fiziski rīcībā esošiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="bb671-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="bb671-107">Krājumu bloķēšanas izveide</span><span class="sxs-lookup"><span data-stu-id="bb671-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="bb671-108">Dodieties uz Krājumu vadība > Periodiskie uzdevumi > Krājumu bloķēšana.</span><span class="sxs-lookup"><span data-stu-id="bb671-108">Go to Inventory management > Periodic tasks > Inventory blocking.</span></span>
2. <span data-ttu-id="bb671-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="bb671-109">Click New.</span></span>
3. <span data-ttu-id="bb671-110">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="bb671-110">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="bb671-111">Sarakstā atlasiet krājumu, kuru vēlaties izmantot.</span><span class="sxs-lookup"><span data-stu-id="bb671-111">In the list, select the item you want to choose.</span></span>
    * <span data-ttu-id="bb671-112">Atlasiet krājuma numuru no fiziski rīcībā esošiem krājumiem, kuru vēlaties bloķēt.</span><span class="sxs-lookup"><span data-stu-id="bb671-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="bb671-113">Ja izmantojat USMF, varat atlasīt krājumu M9201.</span><span class="sxs-lookup"><span data-stu-id="bb671-113">If you’re using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="bb671-114">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="bb671-114">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="bb671-115">Ja lietojat krājumu M9201, ir jāatlasa mazāk par 200 vienībām.</span><span class="sxs-lookup"><span data-stu-id="bb671-115">If you’re using item M9201, you need to select less than 200.</span></span>  
6. <span data-ttu-id="bb671-116">Pārslēdziet sadaļas Krājumu dimensijas paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="bb671-116">Toggle the expansion of the Inventory dimensions section.</span></span>
7. <span data-ttu-id="bb671-117">Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="bb671-117">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="bb671-118">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="bb671-118">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="bb671-119">Ja izmantojat krājumu M9201, varat atlasīt 51. noliktavu.</span><span class="sxs-lookup"><span data-stu-id="bb671-119">If you’re using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="bb671-120">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="bb671-120">Click Save.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="bb671-121">Krājumu bloķēšanas nosacījumu atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="bb671-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="bb671-122">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="bb671-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="bb671-123">Atjauniniet krājumu daudzuma lauku, lai atspoguļotu bloķējamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="bb671-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="bb671-124">Ievadiet datumu laukā Prognozētais datums.</span><span class="sxs-lookup"><span data-stu-id="bb671-124">In the Expected date field, enter a date.</span></span>
    * <span data-ttu-id="bb671-125">Varat norādīt, kad bloķētie krājumi varētu kļūt pieejami rezervācijai, norādot paredzamo datumu.</span><span class="sxs-lookup"><span data-stu-id="bb671-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="bb671-126">Ja krājumu bloķēšanai ir atlasīta opcija Paredzamā saņemšana, kā tas ir pēc noklusējuma, manuāli izveidojot bloķēšanas pavēli, šis datums tiks attēlots paredzamajā transakcijā.</span><span class="sxs-lookup"><span data-stu-id="bb671-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="bb671-127">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="bb671-127">Click Save.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="bb671-128">Krājuma bloķēšanas noņemšana</span><span class="sxs-lookup"><span data-stu-id="bb671-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="bb671-129">Noklikšķiniet uz Dzēst.</span><span class="sxs-lookup"><span data-stu-id="bb671-129">Click Delete.</span></span>
2. <span data-ttu-id="bb671-130">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="bb671-130">Click Yes.</span></span>
3. <span data-ttu-id="bb671-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="bb671-131">Close the page.</span></span>

