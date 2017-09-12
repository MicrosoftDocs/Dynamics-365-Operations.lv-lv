--- 
title: "Ar iepriekšēju datumu datētu čeku reģistrēšana un grāmatošana kreditoram"
description: "Izmantojiet žurnāla dokumentu, lai reģistrētu informāciju ar iepriekšēju datumu datētam čekam, pirms čeku izsniedzat kreditoram."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8689421d3281f93af9298f777f92c5c3b2c1c86c
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="register-and-post-a-postdated-check-for-a-vendor"></a><span data-ttu-id="47e89-103">Ar iepriekšēju datumu datētu čeku reģistrēšana un grāmatošana kreditoram</span><span class="sxs-lookup"><span data-stu-id="47e89-103">Register and post a postdated check for a vendor</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="47e89-104">Izmantojiet žurnāla dokumentu, lai reģistrētu informāciju ar iepriekšēju datumu datētam čekam, pirms čeku izsniedzat kreditoram.</span><span class="sxs-lookup"><span data-stu-id="47e89-104">You can register the details of a postdated check before you issue the check to a vendor by using the journal voucher.</span></span> <span data-ttu-id="47e89-105">Var arī grāmatot ar iepriekšēju datumu datēto čeku un ģenerētu finanšu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="47e89-105">You can also post the postdated check and generate financial transactions.</span></span> <span data-ttu-id="47e89-106">Pirms reģistrējat un grāmatojat ar iepriekšēju datumu datētu čeku, ko esat saņēmis no kreditora, izpildiet tālāk norādīto uzdevumu:</span><span class="sxs-lookup"><span data-stu-id="47e89-106">Before you register and post a postdated check from a vendor, complete the following task:</span></span> 

<span data-ttu-id="47e89-107">Iestatiet ar iepriekšēju datumu datētus čekus lapā Kases un bankas pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="47e89-107">Set up postdated checks in the Cash and bank management page.</span></span> 



<span data-ttu-id="47e89-108">Šī uzdevuma izpildei nepieciešama loma Kasieris.</span><span class="sxs-lookup"><span data-stu-id="47e89-108">The role of this task guides is Treasurer.</span></span> <span data-ttu-id="47e89-109">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="47e89-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="47e89-110">Dodieties uz Parādi kreditoriem > Maksājumi > Maksājumu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="47e89-110">Go to Acounts payable > Payments > Payment journal</span></span>
2. <span data-ttu-id="47e89-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="47e89-111">Click New.</span></span>
3. <span data-ttu-id="47e89-112">Laukā Nosaukums ierakstiet VendPay.</span><span class="sxs-lookup"><span data-stu-id="47e89-112">In the Name field, type 'VendPay'.</span></span>
4. <span data-ttu-id="47e89-113">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="47e89-113">Click Lines.</span></span>
5. <span data-ttu-id="47e89-114">Laukā Konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="47e89-114">In the Account field, specify the desired values.</span></span>
6. <span data-ttu-id="47e89-115">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="47e89-115">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="47e89-116">Laukā Debets ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="47e89-116">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="47e89-117">Laukā Maksāšanas metode noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="47e89-117">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="47e89-118">Maksāšanas tipa atlasīšana ar iepriekšēju datumu datētajam čekam</span><span class="sxs-lookup"><span data-stu-id="47e89-118">Select the method of payment for the postdated check</span></span>  
9. <span data-ttu-id="47e89-119">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="47e89-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="47e89-120">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="47e89-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="47e89-121">Noklikšķiniet uz cilnes Ar iepriekšēju datumu datēti čeki.</span><span class="sxs-lookup"><span data-stu-id="47e89-121">Click the Postdated checks tab.</span></span>
12. <span data-ttu-id="47e89-122">Laukā Čeka numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="47e89-122">In the Check number field, type a value.</span></span>
    * <span data-ttu-id="47e89-123">Ievadiet vai rediģējiet ar iepriekšēju datumu datētā čeka numuru.</span><span class="sxs-lookup"><span data-stu-id="47e89-123">Enter or modify the number of the postdated check.</span></span>  
13. <span data-ttu-id="47e89-124">Laukā Izdevēja bankas nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="47e89-124">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="47e89-125">Ievadiet ildinformāciju par izdevēja banku.</span><span class="sxs-lookup"><span data-stu-id="47e89-125">enter the bank details for the issuing bank.</span></span>  
14. <span data-ttu-id="47e89-126">Noklikšķiniet uz cilnes Saraksts.</span><span class="sxs-lookup"><span data-stu-id="47e89-126">Click the List tab.</span></span>
15. <span data-ttu-id="47e89-127">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="47e89-127">Click Post.</span></span>
16. <span data-ttu-id="47e89-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="47e89-128">Close the page.</span></span>
17. <span data-ttu-id="47e89-129">Noklikšķiniet uz cilnes Ar iepriekšēju datumu datēti čeki.</span><span class="sxs-lookup"><span data-stu-id="47e89-129">Click the Postdated checks tab.</span></span>


