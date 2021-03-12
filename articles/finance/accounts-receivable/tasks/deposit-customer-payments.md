---
title: Debitora maksājumu deponējums
description: Debitora maksājumu depozīts.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9221101581a6a130889b7c941ca228070a000c56
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003160"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="3afae-103">Debitora maksājumu deponējums</span><span class="sxs-lookup"><span data-stu-id="3afae-103">Deposit customer payments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3afae-104">Debitora maksājumu depozīts.</span><span class="sxs-lookup"><span data-stu-id="3afae-104">Deposit customer payments.</span></span> <span data-ttu-id="3afae-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="3afae-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="3afae-106">Pārejiet uz sadaļu **Navigācijas rūts > Moduļi > Debitori > Maksājumi > Maksājumu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="3afae-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="3afae-107">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="3afae-107">Select **New**.</span></span>
3. <span data-ttu-id="3afae-108">Laukā **Nosaukums** nolaižamajā izvēlnē atlasiet **CustPay**.</span><span class="sxs-lookup"><span data-stu-id="3afae-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="3afae-109">Atlasiet **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="3afae-109">Select **Lines**.</span></span>
5. <span data-ttu-id="3afae-110">Laukā **Uzņēmums** atlasiet klientu, par kuru ierakstāt maksājumu.</span><span class="sxs-lookup"><span data-stu-id="3afae-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="3afae-111">Laukā **Kredīts** ievadiet maksājuma summu.</span><span class="sxs-lookup"><span data-stu-id="3afae-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="3afae-112">Ja vēlaties, varat atstāt summas lauku tukšu, tad sistēma to aprēķinās, atlasot apmaksātos rēķinus.</span><span class="sxs-lookup"><span data-stu-id="3afae-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="3afae-113">Ievadiet vērtību laukā **Maksājuma atsauce**.</span><span class="sxs-lookup"><span data-stu-id="3afae-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="3afae-114">Maksājuma atsauce varētu būt ievadāmā maksājuma čeka numurs.</span><span class="sxs-lookup"><span data-stu-id="3afae-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="3afae-115">Maksājuma atsauce ir nepieciešama, lai iekļautu maksājumu depozīta kvītī.</span><span class="sxs-lookup"><span data-stu-id="3afae-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="3afae-116">Atzīmējiet rūtiņu Izmantot depozīta kvīti.</span><span class="sxs-lookup"><span data-stu-id="3afae-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="3afae-117">Ja maksājums ir jāiekļauj depozītā, nomainiet šo iestatījumu uz Jā.</span><span class="sxs-lookup"><span data-stu-id="3afae-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="3afae-118">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="3afae-118">Select **New**.</span></span>
10. <span data-ttu-id="3afae-119">Laukā **Uzņēmums** atlasiet klientu nākamajam maksājumam.</span><span class="sxs-lookup"><span data-stu-id="3afae-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="3afae-120">Laukā **Kredīts** ievadiet maksājuma summu.</span><span class="sxs-lookup"><span data-stu-id="3afae-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="3afae-121">Ievadiet vērtību laukā **Maksājuma atsauce**.</span><span class="sxs-lookup"><span data-stu-id="3afae-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="3afae-122">Atzīmējiet rūtiņu **Izmantot depozīta kvīti**.</span><span class="sxs-lookup"><span data-stu-id="3afae-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="3afae-123">Atlasiet **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="3afae-123">Select **Post**.</span></span> <span data-ttu-id="3afae-124">Maksājumi ir jāiegrāmato pirms depozīta kvīts izveides.</span><span class="sxs-lookup"><span data-stu-id="3afae-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="3afae-125">Tas ir nepieciešams, lai nodrošinātu, ka pēc depozīta kvīts izveides maksājumi netiek mainīti.</span><span class="sxs-lookup"><span data-stu-id="3afae-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="3afae-126">Atlasiet **Funkcijas**.</span><span class="sxs-lookup"><span data-stu-id="3afae-126">Select **Functions**.</span></span>
16. <span data-ttu-id="3afae-127">Atlasiet **Depozīta kvīts**.</span><span class="sxs-lookup"><span data-stu-id="3afae-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="3afae-128">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3afae-128">Select **OK**.</span></span> <span data-ttu-id="3afae-129">Pirmā lapa tiek izmantota, lai izveidotu depozīta kvīti.</span><span class="sxs-lookup"><span data-stu-id="3afae-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="3afae-130">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3afae-130">Select **OK**.</span></span> <span data-ttu-id="3afae-131">Otrais solis ir depozīta kvīts drukāšana, bet šis solis nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="3afae-131">The second step is to print the deposit slip, but this step is not required.</span></span>  

