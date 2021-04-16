---
title: PVN transakcijas izveide dokumentos
description: Dokumentu PVN tiek aprēķināts, dokumenta rindās norādot PVN grupu un krājuma PVN grupu.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 061949dedde763c188e13c07cec750895cbef175
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836989"
---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="a8a67-103">PVN transakcijas izveide dokumentos</span><span class="sxs-lookup"><span data-stu-id="a8a67-103">Create sales tax transactions on documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a8a67-104">Dokumentu PVN tiek aprēķināts, dokumenta rindās norādot PVN grupu un krājuma PVN grupu.</span><span class="sxs-lookup"><span data-stu-id="a8a67-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="a8a67-105">Tās tiek noteiktas pēc noklusējuma no pamatdatiem, bet, ja nepieciešams, tās var mainīt manuāli.</span><span class="sxs-lookup"><span data-stu-id="a8a67-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="a8a67-106">Aprēķināto PVN var pārbaudīt rindas un dokumenta līmenī.</span><span class="sxs-lookup"><span data-stu-id="a8a67-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="a8a67-107">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="a8a67-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="a8a67-108">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="a8a67-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="a8a67-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a8a67-109">Click New.</span></span>
3. <span data-ttu-id="a8a67-110">Laukā Debitora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="a8a67-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a8a67-111">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a8a67-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="a8a67-112">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a8a67-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="a8a67-113">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="a8a67-113">Click OK.</span></span>
7. <span data-ttu-id="a8a67-114">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="a8a67-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="a8a67-115">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="a8a67-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="a8a67-116">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a8a67-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="a8a67-117">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="a8a67-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="a8a67-118">Izvērsiet vai sakļaujiet sadaļu Detalizēta rindas informācija.</span><span class="sxs-lookup"><span data-stu-id="a8a67-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="a8a67-119">Noklikšķiniet uz cilnes Iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="a8a67-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="a8a67-120">Laukā Krājuma PVN grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="a8a67-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="a8a67-121">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a8a67-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="a8a67-122">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a8a67-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="a8a67-123">Noklikšķiniet uz Finanšu dati.</span><span class="sxs-lookup"><span data-stu-id="a8a67-123">Click Financials.</span></span>
17. <span data-ttu-id="a8a67-124">Noklikšķiniet uz Pārdošanas nodoklis.</span><span class="sxs-lookup"><span data-stu-id="a8a67-124">Click Sales tax.</span></span>
18. <span data-ttu-id="a8a67-125">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a8a67-125">Click OK.</span></span>
19. <span data-ttu-id="a8a67-126">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="a8a67-126">Click Add line.</span></span>
20. <span data-ttu-id="a8a67-127">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="a8a67-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="a8a67-128">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="a8a67-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="a8a67-129">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a8a67-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="a8a67-130">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a8a67-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="a8a67-131">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="a8a67-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="a8a67-132">Laukā Krājuma PVN grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="a8a67-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="a8a67-133">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a8a67-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="a8a67-134">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a8a67-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="a8a67-135">Darbību rūtī noklikšķiniet uz Pārdot.</span><span class="sxs-lookup"><span data-stu-id="a8a67-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="a8a67-136">Noklikšķiniet uz Pārdošanas nodoklis.</span><span class="sxs-lookup"><span data-stu-id="a8a67-136">Click Sales tax.</span></span>
30. <span data-ttu-id="a8a67-137">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a8a67-137">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]