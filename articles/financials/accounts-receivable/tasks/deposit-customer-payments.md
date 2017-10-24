--- 
title: "Debitora maksājumu deponējums"
description: "Debitora maksājumu depozīts."
author: ShivamPandey-msft
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
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dbf21bd5df70cd80e4fe3f2f5d699aa82b62423b
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="deposit-customer-payments"></a><span data-ttu-id="9c380-103">Debitora maksājumu deponējums</span><span class="sxs-lookup"><span data-stu-id="9c380-103">Deposit customer payments</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9c380-104">Debitora maksājumu depozīts.</span><span class="sxs-lookup"><span data-stu-id="9c380-104">Deposit customer payments.</span></span> <span data-ttu-id="9c380-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="9c380-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="9c380-106">Pārejiet uz sadaļu Debitori > Maksājumi > Maksājumu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="9c380-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="9c380-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9c380-107">Click New.</span></span>
3. <span data-ttu-id="9c380-108">Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="9c380-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="9c380-109">Atlasiet maksājuma žurnālu.</span><span class="sxs-lookup"><span data-stu-id="9c380-109">Select the payment journal.</span></span> 
5. <span data-ttu-id="9c380-110">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="9c380-110">Click Lines.</span></span>
6. <span data-ttu-id="9c380-111">Laukā Konts atlasiet debitoru, kuram vēlaties ierakstīt maksājumu.</span><span class="sxs-lookup"><span data-stu-id="9c380-111">In the Account field, select the Customer for whom you are recording the payment.</span></span>
7. <span data-ttu-id="9c380-112">Ievadiet maksājuma summu laukā Kredīts.</span><span class="sxs-lookup"><span data-stu-id="9c380-112">In the Credit field, enter the amount of the payment.</span></span>
    * <span data-ttu-id="9c380-113">Ja vēlaties, varat atstāt summas lauku tukšu, tad sistēma to aprēķinās, atlasot apmaksātos rēķinus.</span><span class="sxs-lookup"><span data-stu-id="9c380-113">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
8. <span data-ttu-id="9c380-114">Ierakstiet vērtību laukā Maksājuma atsauce.</span><span class="sxs-lookup"><span data-stu-id="9c380-114">In the Payment reference field, type a value.</span></span>
    * <span data-ttu-id="9c380-115">Maksājuma atsauce varētu būt ievadāmā maksājuma čeka numurs.</span><span class="sxs-lookup"><span data-stu-id="9c380-115">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="9c380-116">Maksājuma atsauce ir nepieciešama, lai iekļautu maksājumu depozīta kvītī.</span><span class="sxs-lookup"><span data-stu-id="9c380-116">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
9. <span data-ttu-id="9c380-117">Atzīmējiet rūtiņu Izmantot depozīta kvīti.</span><span class="sxs-lookup"><span data-stu-id="9c380-117">Mark the box Use a deposit slip.</span></span>
    * <span data-ttu-id="9c380-118">Ja maksājums ir jāiekļauj depozītā, nomainiet šo iestatījumu uz Jā.</span><span class="sxs-lookup"><span data-stu-id="9c380-118">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
10. <span data-ttu-id="9c380-119">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9c380-119">Click New.</span></span>
11. <span data-ttu-id="9c380-120">Laukā Konts atlasiet debitoru nākamajam maksājumam.</span><span class="sxs-lookup"><span data-stu-id="9c380-120">In the Account field, select the Customer for the next payment.</span></span>
12. <span data-ttu-id="9c380-121">Ievadiet maksājuma summu laukā Kredīts.</span><span class="sxs-lookup"><span data-stu-id="9c380-121">In the Credit field, enter the payment amount.</span></span>
13. <span data-ttu-id="9c380-122">Ierakstiet vērtību laukā Maksājuma atsauce.</span><span class="sxs-lookup"><span data-stu-id="9c380-122">In the Payment reference field, type a value.</span></span>
14. <span data-ttu-id="9c380-123">Atzīmējiet rūtiņu Izmantot depozīta kvīti.</span><span class="sxs-lookup"><span data-stu-id="9c380-123">Mark the box Use a deposit slip.</span></span>
15. <span data-ttu-id="9c380-124">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="9c380-124">Click Post.</span></span>
    * <span data-ttu-id="9c380-125">Maksājumi ir jāiegrāmato pirms depozīta kvīts izveides.</span><span class="sxs-lookup"><span data-stu-id="9c380-125">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="9c380-126">Tas ir nepieciešams, lai nodrošinātu, ka pēc depozīta kvīts izveides maksājumi netiek mainīti.</span><span class="sxs-lookup"><span data-stu-id="9c380-126">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
16. <span data-ttu-id="9c380-127">Noklikšķiniet uz Funkcijas.</span><span class="sxs-lookup"><span data-stu-id="9c380-127">Click Functions.</span></span>
17. <span data-ttu-id="9c380-128">Noklikšķiniet uz Depozīta kvīts.</span><span class="sxs-lookup"><span data-stu-id="9c380-128">Click Deposit slip.</span></span>
18. <span data-ttu-id="9c380-129">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9c380-129">Click OK.</span></span>
    * <span data-ttu-id="9c380-130">Pirmā lapa tiek izmantota, lai izveidotu depozīta kvīti.</span><span class="sxs-lookup"><span data-stu-id="9c380-130">The first page is used to create the deposit slip.</span></span>  
19. <span data-ttu-id="9c380-131">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9c380-131">Click OK.</span></span>
    * <span data-ttu-id="9c380-132">Otrais solis ir depozīta kvīts drukāšana, bet šis solis nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="9c380-132">The second step is to print the deposit slip, but this step is not required.</span></span>  


