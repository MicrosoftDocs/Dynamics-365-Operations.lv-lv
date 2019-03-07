---
title: Debitora maksājumu deponējums
description: Debitora maksājumu depozīts.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f58cebce20e8516dc918e0bad1e020ffd7f791ee
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "313386"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="71587-103">Debitora maksājumu deponējums</span><span class="sxs-lookup"><span data-stu-id="71587-103">Deposit customer payments</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="71587-104">Debitora maksājumu depozīts.</span><span class="sxs-lookup"><span data-stu-id="71587-104">Deposit customer payments.</span></span> <span data-ttu-id="71587-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="71587-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="71587-106">Pārejiet uz sadaļu Debitori > Maksājumi > Maksājumu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="71587-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="71587-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="71587-107">Click New.</span></span>
3. <span data-ttu-id="71587-108">Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="71587-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="71587-109">Atlasiet maksājuma žurnālu.</span><span class="sxs-lookup"><span data-stu-id="71587-109">Select the payment journal.</span></span> 
5. <span data-ttu-id="71587-110">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="71587-110">Click Lines.</span></span>
6. <span data-ttu-id="71587-111">Laukā Konts atlasiet debitoru, kuram vēlaties ierakstīt maksājumu.</span><span class="sxs-lookup"><span data-stu-id="71587-111">In the Account field, select the Customer for whom you are recording the payment.</span></span>
7. <span data-ttu-id="71587-112">Ievadiet maksājuma summu laukā Kredīts.</span><span class="sxs-lookup"><span data-stu-id="71587-112">In the Credit field, enter the amount of the payment.</span></span>
    * <span data-ttu-id="71587-113">Ja vēlaties, varat atstāt summas lauku tukšu, tad sistēma to aprēķinās, atlasot apmaksātos rēķinus.</span><span class="sxs-lookup"><span data-stu-id="71587-113">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
8. <span data-ttu-id="71587-114">Ierakstiet vērtību laukā Maksājuma atsauce.</span><span class="sxs-lookup"><span data-stu-id="71587-114">In the Payment reference field, type a value.</span></span>
    * <span data-ttu-id="71587-115">Maksājuma atsauce varētu būt ievadāmā maksājuma čeka numurs.</span><span class="sxs-lookup"><span data-stu-id="71587-115">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="71587-116">Maksājuma atsauce ir nepieciešama, lai iekļautu maksājumu depozīta kvītī.</span><span class="sxs-lookup"><span data-stu-id="71587-116">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
9. <span data-ttu-id="71587-117">Atzīmējiet rūtiņu Izmantot depozīta kvīti.</span><span class="sxs-lookup"><span data-stu-id="71587-117">Mark the box Use a deposit slip.</span></span>
    * <span data-ttu-id="71587-118">Ja maksājums ir jāiekļauj depozītā, nomainiet šo iestatījumu uz Jā.</span><span class="sxs-lookup"><span data-stu-id="71587-118">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
10. <span data-ttu-id="71587-119">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="71587-119">Click New.</span></span>
11. <span data-ttu-id="71587-120">Laukā Konts atlasiet debitoru nākamajam maksājumam.</span><span class="sxs-lookup"><span data-stu-id="71587-120">In the Account field, select the Customer for the next payment.</span></span>
12. <span data-ttu-id="71587-121">Ievadiet maksājuma summu laukā Kredīts.</span><span class="sxs-lookup"><span data-stu-id="71587-121">In the Credit field, enter the payment amount.</span></span>
13. <span data-ttu-id="71587-122">Ierakstiet vērtību laukā Maksājuma atsauce.</span><span class="sxs-lookup"><span data-stu-id="71587-122">In the Payment reference field, type a value.</span></span>
14. <span data-ttu-id="71587-123">Atzīmējiet rūtiņu Izmantot depozīta kvīti.</span><span class="sxs-lookup"><span data-stu-id="71587-123">Mark the box Use a deposit slip.</span></span>
15. <span data-ttu-id="71587-124">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="71587-124">Click Post.</span></span>
    * <span data-ttu-id="71587-125">Maksājumi ir jāiegrāmato pirms depozīta kvīts izveides.</span><span class="sxs-lookup"><span data-stu-id="71587-125">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="71587-126">Tas ir nepieciešams, lai nodrošinātu, ka pēc depozīta kvīts izveides maksājumi netiek mainīti.</span><span class="sxs-lookup"><span data-stu-id="71587-126">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
16. <span data-ttu-id="71587-127">Noklikšķiniet uz Funkcijas.</span><span class="sxs-lookup"><span data-stu-id="71587-127">Click Functions.</span></span>
17. <span data-ttu-id="71587-128">Noklikšķiniet uz Depozīta kvīts.</span><span class="sxs-lookup"><span data-stu-id="71587-128">Click Deposit slip.</span></span>
18. <span data-ttu-id="71587-129">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="71587-129">Click OK.</span></span>
    * <span data-ttu-id="71587-130">Pirmā lapa tiek izmantota, lai izveidotu depozīta kvīti.</span><span class="sxs-lookup"><span data-stu-id="71587-130">The first page is used to create the deposit slip.</span></span>  
19. <span data-ttu-id="71587-131">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="71587-131">Click OK.</span></span>
    * <span data-ttu-id="71587-132">Otrais solis ir depozīta kvīts drukāšana, bet šis solis nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="71587-132">The second step is to print the deposit slip, but this step is not required.</span></span>  

