---
title: Budžeta noteikta pirkšanas pasūtījuma izveide
description: Izmantojiet šo procedūru, lai izveidotu pirkšanas pasūtījumu, kurā ir pārbaudīts pieejamais budžets.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e82e40d67547f5932a4805f2580e8c9f58def284
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569987"
---
# <a name="create-a-purchase-order-governed-by-budget"></a><span data-ttu-id="0174c-103">Budžeta noteikta pirkšanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="0174c-103">Create a purchase order governed by budget</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0174c-104">Izmantojiet šo procedūru, lai izveidotu pirkšanas pasūtījumu, kurā ir pārbaudīts pieejamais budžets.</span><span class="sxs-lookup"><span data-stu-id="0174c-104">Use this procedure to create a purchase order that is checked for available budget.</span></span> <span data-ttu-id="0174c-105">Šajā ierakstā tiek izmantots USMF demonstrācijas datu uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="0174c-105">This recording uses the USMF demo data company.</span></span>


## <a name="review-the-budget-control-configuration"></a><span data-ttu-id="0174c-106">Budžeta kontroles konfigurācijas pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="0174c-106">Review the budget control configuration</span></span>
1. <span data-ttu-id="0174c-107">Dodieties uz Budžeta veidošana > Iestatīšana > Budžeta kontrole > Budžeta kontroles konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="0174c-107">Go to Budgeting > Setup > Budget control > Budget control configuration.</span></span>
2. <span data-ttu-id="0174c-108">Noklikšķiniet uz cilnes Pieejamie budžeta līdzekļi.</span><span class="sxs-lookup"><span data-stu-id="0174c-108">Click the Budget funds available tab.</span></span>
3. <span data-ttu-id="0174c-109">Noklikšķiniet uz cilnes Dokumenti un žurnāli.</span><span class="sxs-lookup"><span data-stu-id="0174c-109">Click the Documents and journals tab.</span></span>
4. <span data-ttu-id="0174c-110">Noklikšķiniet uz cilnes Definēt budžeta kontroles kārtulas.</span><span class="sxs-lookup"><span data-stu-id="0174c-110">Click the Define budget control rules tab.</span></span>
5. <span data-ttu-id="0174c-111">Noklikšķiniet uz cilnes Definēt budžeta grupas.</span><span class="sxs-lookup"><span data-stu-id="0174c-111">Click the Define budget groups tab.</span></span>
6. <span data-ttu-id="0174c-112">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0174c-112">Close the page.</span></span>

## <a name="create-the-purchase-order-header"></a><span data-ttu-id="0174c-113">Izveidojiet pirkšanas pasūtījuma virsrakstu</span><span class="sxs-lookup"><span data-stu-id="0174c-113">Create the purchase order header</span></span>
1. <span data-ttu-id="0174c-114">Dodieties uz Sagāde un avoti > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="0174c-114">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="0174c-115">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="0174c-115">Click New.</span></span>
3. <span data-ttu-id="0174c-116">Ievadiet vai atlasiet vērtību laukā kreditora konts.</span><span class="sxs-lookup"><span data-stu-id="0174c-116">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="0174c-117">Izvērsiet sadaļu Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="0174c-117">Expand the General section.</span></span>
5. <span data-ttu-id="0174c-118">Laukā Uzskaites datums iestatiet datumu "2016-01-01".</span><span class="sxs-lookup"><span data-stu-id="0174c-118">In the Accounting date field, set the date to '2016-01-01'.</span></span>
6. <span data-ttu-id="0174c-119">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0174c-119">Click OK.</span></span>

## <a name="add-a-purchase-order-line"></a><span data-ttu-id="0174c-120">Pievienojiet pirkšanas pasūtījuma rindu</span><span class="sxs-lookup"><span data-stu-id="0174c-120">Add a purchase order line</span></span>
1. <span data-ttu-id="0174c-121">Sagādes kategorijas laukā ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0174c-121">In the Procurement category field, enter or select a value.</span></span>
2. <span data-ttu-id="0174c-122">Vienumam Daudzums iestatiet vērtību “2”.</span><span class="sxs-lookup"><span data-stu-id="0174c-122">Set Quantity to '2'.</span></span>
3. <span data-ttu-id="0174c-123">Laukā Vienība ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0174c-123">In the Unit field, enter or select a value.</span></span>
4. <span data-ttu-id="0174c-124">Iestatiet vienuma Vienības cena vērtību "10000".</span><span class="sxs-lookup"><span data-stu-id="0174c-124">Set Unit price to '10000'.</span></span>
5. <span data-ttu-id="0174c-125">Noklikšķiniet uz Finanšu dati.</span><span class="sxs-lookup"><span data-stu-id="0174c-125">Click Financials.</span></span>
6. <span data-ttu-id="0174c-126">Noklikšķiniet uz Sadalīt summas.</span><span class="sxs-lookup"><span data-stu-id="0174c-126">Click Distribute amounts.</span></span>
7. <span data-ttu-id="0174c-127">Laukā Virsgrāmatas konts norādiet vērtību "601300-001-023--".</span><span class="sxs-lookup"><span data-stu-id="0174c-127">In the Ledger account field, specify the value '601300-001-023--'.</span></span>
8. <span data-ttu-id="0174c-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0174c-128">Close the page.</span></span>

## <a name="perform-budget-checking"></a><span data-ttu-id="0174c-129">Veikt budžeta pārbaudi</span><span class="sxs-lookup"><span data-stu-id="0174c-129">Perform budget checking</span></span>
1. <span data-ttu-id="0174c-130">Noklikšķiniet uz Finanšu dati.</span><span class="sxs-lookup"><span data-stu-id="0174c-130">Click Financials.</span></span>
2. <span data-ttu-id="0174c-131">Noklikšķiniet uz Veikt budžeta pārbaudi.</span><span class="sxs-lookup"><span data-stu-id="0174c-131">Click Perform budget checking.</span></span>
3. <span data-ttu-id="0174c-132">Noklikšķiniet uz Finanšu dati.</span><span class="sxs-lookup"><span data-stu-id="0174c-132">Click Financials.</span></span>
4. <span data-ttu-id="0174c-133">Noklikšķiniet uz Skatīt budžeta pārbaudes kļūdas vai brīdinājumus.</span><span class="sxs-lookup"><span data-stu-id="0174c-133">Click Budget check errors or warnings.</span></span>
5. <span data-ttu-id="0174c-134">Noklikšķiniet uz Aizvērt.</span><span class="sxs-lookup"><span data-stu-id="0174c-134">Click Close.</span></span>

