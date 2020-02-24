---
title: " Preču iepakojumu izveide pirkšanas pasūtījumiem"
description: Šajā procedūrā ir aprakstīts, ka izveidot preču pakotni un izmantot to pirkšanas pasūtījumā.
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14e1fd19c6a27739ce9f57a4ab33f61e6baaeb2e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023282"
---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="8f85c-103"> Preču iepakojumu izveide pirkšanas pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="8f85c-103">Create product packages for purchase orders</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="8f85c-104">Šajā procedūrā ir aprakstīts, ka izveidot preču pakotni un izmantot to pirkšanas pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="8f85c-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="8f85c-105">Pirkšanas pasūtījums tiks izmantots, lai izveidotu pasūtījumu iepriekš definētai preču kopai.</span><span class="sxs-lookup"><span data-stu-id="8f85c-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="8f85c-106">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="8f85c-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="8f85c-107">Preču pakotnes izveide</span><span class="sxs-lookup"><span data-stu-id="8f85c-107">Create a product package</span></span>
1. <span data-ttu-id="8f85c-108">Pārejiet uz sadaļu Mazumtirdzniecība un tirdzniecība > Krājumu pārvaldība > Papildināšana > Preču pakotnes.</span><span class="sxs-lookup"><span data-stu-id="8f85c-108">Go to Retail and Commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="8f85c-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="8f85c-109">Click New.</span></span>
3. <span data-ttu-id="8f85c-110">Laukā Pakotnes numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8f85c-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="8f85c-111">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8f85c-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8f85c-112">Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="8f85c-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="8f85c-113">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="8f85c-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="8f85c-114">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="8f85c-114">Click Add.</span></span>
8. <span data-ttu-id="8f85c-115">Laukā Krājuma kods ierakstiet 0160.</span><span class="sxs-lookup"><span data-stu-id="8f85c-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="8f85c-116">Laukā Lielums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="8f85c-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="8f85c-117">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="8f85c-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="8f85c-118">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="8f85c-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="8f85c-119">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="8f85c-119">Click Add.</span></span>
13. <span data-ttu-id="8f85c-120">Laukā Krājuma kods ierakstiet 0160.</span><span class="sxs-lookup"><span data-stu-id="8f85c-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="8f85c-121">Laukā Varianta numurs noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="8f85c-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="8f85c-122">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="8f85c-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="8f85c-123">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="8f85c-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="8f85c-124">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="8f85c-124">Click Add.</span></span>
18. <span data-ttu-id="8f85c-125">Laukā Krājuma kods ierakstiet 0175.</span><span class="sxs-lookup"><span data-stu-id="8f85c-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="8f85c-126">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="8f85c-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="8f85c-127">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8f85c-127">Click Save.</span></span>
21. <span data-ttu-id="8f85c-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="8f85c-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="8f85c-129">Iepakojuma pievienošana pirkšanas pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="8f85c-129">Add package to purchase order</span></span>
1. <span data-ttu-id="8f85c-130">Pārejiet uz sadaļu Kreditori > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="8f85c-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="8f85c-131">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="8f85c-131">Click New.</span></span>
3. <span data-ttu-id="8f85c-132">Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="8f85c-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8f85c-133">Sarakstā atlasiet to pašu kreditoru, kam iepriekš tika izveidota preču pakotne, ja kreditors tika atlasīts.</span><span class="sxs-lookup"><span data-stu-id="8f85c-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="8f85c-134">Pārslēdziet sadaļas Vispārīgi paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="8f85c-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="8f85c-135">Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="8f85c-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="8f85c-136">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="8f85c-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="8f85c-137">Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="8f85c-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="8f85c-138">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="8f85c-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="8f85c-139">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="8f85c-139">Click OK.</span></span>
11. <span data-ttu-id="8f85c-140">Pārslēdziet sadaļas Detalizēta rindas informācija paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="8f85c-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="8f85c-141">Noklikšķiniet uz cilnes Preču pakotnes.</span><span class="sxs-lookup"><span data-stu-id="8f85c-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="8f85c-142">Noklikšķiniet uz Pirkšanas pasūtījuma rinda.</span><span class="sxs-lookup"><span data-stu-id="8f85c-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="8f85c-143">Noklikšķiniet uz Izveidot rindas, izmantojot pakotni.</span><span class="sxs-lookup"><span data-stu-id="8f85c-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="8f85c-144">Sarakstā atrodiet un atlasiet preču pakotni, kas tika izveidota iepriekšējā darbībā.</span><span class="sxs-lookup"><span data-stu-id="8f85c-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="8f85c-145">Laukā Daudzums ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="8f85c-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="8f85c-146">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="8f85c-146">Click Create.</span></span>
18. <span data-ttu-id="8f85c-147">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8f85c-147">Click Save.</span></span>

