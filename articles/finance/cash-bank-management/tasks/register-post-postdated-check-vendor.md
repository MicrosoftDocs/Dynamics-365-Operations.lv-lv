---
title: Ar iepriekšēju datumu datētu čeku reģistrēšana un grāmatošana kreditoram
description: Izmantojiet žurnāla dokumentu, lai reģistrētu informāciju ar iepriekšēju datumu datētam čekam, pirms čeku izsniedzat kreditoram.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ffd482facc629e65a79f328cb237fd72f6f6b5c5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225325"
---
# <a name="register-and-post-a-postdated-check-for-a-vendor"></a><span data-ttu-id="c3713-103">Ar iepriekšēju datumu datētu čeku reģistrēšana un grāmatošana kreditoram</span><span class="sxs-lookup"><span data-stu-id="c3713-103">Register and post a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c3713-104">Izmantojiet žurnāla dokumentu, lai reģistrētu informāciju ar iepriekšēju datumu datētam čekam, pirms čeku izsniedzat kreditoram.</span><span class="sxs-lookup"><span data-stu-id="c3713-104">You can register the details of a postdated check before you issue the check to a vendor by using the journal voucher.</span></span> <span data-ttu-id="c3713-105">Var arī grāmatot ar iepriekšēju datumu datēto čeku un ģenerētu finanšu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="c3713-105">You can also post the postdated check and generate financial transactions.</span></span> <span data-ttu-id="c3713-106">Pirms reģistrējat un grāmatojat ar iepriekšēju datumu datētu čeku, ko esat saņēmis no kreditora, izpildiet tālāk norādīto uzdevumu:</span><span class="sxs-lookup"><span data-stu-id="c3713-106">Before you register and post a postdated check from a vendor, complete the following task:</span></span> 

<span data-ttu-id="c3713-107">Iestatiet ar iepriekšēju datumu datētus čekus lapā Kases un bankas pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="c3713-107">Set up postdated checks in the Cash and bank management page.</span></span> 



<span data-ttu-id="c3713-108">Šī uzdevuma izpildei nepieciešama loma Kasieris.</span><span class="sxs-lookup"><span data-stu-id="c3713-108">The role of this task guides is Treasurer.</span></span> <span data-ttu-id="c3713-109">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="c3713-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="c3713-110">Dodieties uz Parādi kreditoriem > Maksājumi > Maksājumu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="c3713-110">Go to Acounts payable > Payments > Payment journal</span></span>
2. <span data-ttu-id="c3713-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="c3713-111">Click New.</span></span>
3. <span data-ttu-id="c3713-112">Laukā Nosaukums ierakstiet VendPay.</span><span class="sxs-lookup"><span data-stu-id="c3713-112">In the Name field, type 'VendPay'.</span></span>
4. <span data-ttu-id="c3713-113">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="c3713-113">Click Lines.</span></span>
5. <span data-ttu-id="c3713-114">Laukā Konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="c3713-114">In the Account field, specify the desired values.</span></span>
6. <span data-ttu-id="c3713-115">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="c3713-115">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="c3713-116">Laukā Debets ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="c3713-116">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="c3713-117">Laukā Maksāšanas metode noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="c3713-117">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c3713-118">Maksāšanas tipa atlasīšana ar iepriekšēju datumu datētajam čekam</span><span class="sxs-lookup"><span data-stu-id="c3713-118">Select the method of payment for the postdated check</span></span>  
9. <span data-ttu-id="c3713-119">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c3713-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="c3713-120">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c3713-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="c3713-121">Noklikšķiniet uz cilnes Ar iepriekšēju datumu datēti čeki.</span><span class="sxs-lookup"><span data-stu-id="c3713-121">Click the Postdated checks tab.</span></span>
12. <span data-ttu-id="c3713-122">Laukā Čeka numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c3713-122">In the Check number field, type a value.</span></span>
    * <span data-ttu-id="c3713-123">Ievadiet vai rediģējiet ar iepriekšēju datumu datētā čeka numuru.</span><span class="sxs-lookup"><span data-stu-id="c3713-123">Enter or modify the number of the postdated check.</span></span>  
13. <span data-ttu-id="c3713-124">Laukā Izdevēja bankas nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c3713-124">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="c3713-125">Ievadiet ildinformāciju par izdevēja banku.</span><span class="sxs-lookup"><span data-stu-id="c3713-125">enter the bank details for the issuing bank.</span></span>  
14. <span data-ttu-id="c3713-126">Noklikšķiniet uz cilnes Saraksts.</span><span class="sxs-lookup"><span data-stu-id="c3713-126">Click the List tab.</span></span>
15. <span data-ttu-id="c3713-127">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="c3713-127">Click Post.</span></span>
16. <span data-ttu-id="c3713-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c3713-128">Close the page.</span></span>
17. <span data-ttu-id="c3713-129">Noklikšķiniet uz cilnes Ar iepriekšēju datumu datēti čeki.</span><span class="sxs-lookup"><span data-stu-id="c3713-129">Click the Postdated checks tab.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]