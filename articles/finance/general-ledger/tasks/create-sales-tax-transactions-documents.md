---
title: PVN transakcijas izveide dokumentos
description: Dokumentu PVN tiek aprēķināts, dokumenta rindās norādot PVN grupu un krājuma PVN grupu.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bdc4b5c31d9a478a5226ae6b5e8c776de3b661dd
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144839"
---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="d2f64-103">PVN transakcijas izveide dokumentos</span><span class="sxs-lookup"><span data-stu-id="d2f64-103">Create sales tax transactions on documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d2f64-104">Dokumentu PVN tiek aprēķināts, dokumenta rindās norādot PVN grupu un krājuma PVN grupu.</span><span class="sxs-lookup"><span data-stu-id="d2f64-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="d2f64-105">Tās tiek noteiktas pēc noklusējuma no pamatdatiem, bet, ja nepieciešams, tās var mainīt manuāli.</span><span class="sxs-lookup"><span data-stu-id="d2f64-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="d2f64-106">Aprēķināto PVN var pārbaudīt rindas un dokumenta līmenī.</span><span class="sxs-lookup"><span data-stu-id="d2f64-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="d2f64-107">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="d2f64-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="d2f64-108">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="d2f64-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="d2f64-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d2f64-109">Click New.</span></span>
3. <span data-ttu-id="d2f64-110">Laukā Debitora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d2f64-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d2f64-111">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d2f64-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d2f64-112">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d2f64-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d2f64-113">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="d2f64-113">Click OK.</span></span>
7. <span data-ttu-id="d2f64-114">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="d2f64-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="d2f64-115">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d2f64-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="d2f64-116">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d2f64-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="d2f64-117">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="d2f64-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="d2f64-118">Izvērsiet vai sakļaujiet sadaļu Detalizēta rindas informācija.</span><span class="sxs-lookup"><span data-stu-id="d2f64-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="d2f64-119">Noklikšķiniet uz cilnes Iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="d2f64-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="d2f64-120">Laukā Krājuma PVN grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d2f64-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="d2f64-121">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d2f64-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="d2f64-122">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d2f64-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="d2f64-123">Noklikšķiniet uz Finanšu dati.</span><span class="sxs-lookup"><span data-stu-id="d2f64-123">Click Financials.</span></span>
17. <span data-ttu-id="d2f64-124">Noklikšķiniet uz Pārdošanas nodoklis.</span><span class="sxs-lookup"><span data-stu-id="d2f64-124">Click Sales tax.</span></span>
18. <span data-ttu-id="d2f64-125">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d2f64-125">Click OK.</span></span>
19. <span data-ttu-id="d2f64-126">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="d2f64-126">Click Add line.</span></span>
20. <span data-ttu-id="d2f64-127">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="d2f64-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="d2f64-128">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d2f64-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="d2f64-129">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d2f64-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="d2f64-130">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d2f64-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="d2f64-131">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="d2f64-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="d2f64-132">Laukā Krājuma PVN grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d2f64-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="d2f64-133">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d2f64-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="d2f64-134">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d2f64-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="d2f64-135">Darbību rūtī noklikšķiniet uz Pārdot.</span><span class="sxs-lookup"><span data-stu-id="d2f64-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="d2f64-136">Noklikšķiniet uz Pārdošanas nodoklis.</span><span class="sxs-lookup"><span data-stu-id="d2f64-136">Click Sales tax.</span></span>
30. <span data-ttu-id="d2f64-137">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d2f64-137">Click OK.</span></span>

