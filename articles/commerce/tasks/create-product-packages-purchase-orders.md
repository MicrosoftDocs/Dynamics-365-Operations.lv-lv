---
title: Preču iepakojumu izveide pirkšanas pasūtījumiem
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
ms.openlocfilehash: 2b0084c6b4acbf14e3afec552575d5be26114237
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414098"
---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="0b0be-103">Preču iepakojumu izveide pirkšanas pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="0b0be-103">Create product packages for purchase orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b0be-104">Šajā procedūrā ir aprakstīts, ka izveidot preču pakotni un izmantot to pirkšanas pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="0b0be-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="0b0be-105">Pirkšanas pasūtījums tiks izmantots, lai izveidotu pasūtījumu iepriekš definētai preču kopai.</span><span class="sxs-lookup"><span data-stu-id="0b0be-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="0b0be-106">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="0b0be-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="0b0be-107">Preču pakotnes izveide</span><span class="sxs-lookup"><span data-stu-id="0b0be-107">Create a product package</span></span>
1. <span data-ttu-id="0b0be-108">Pārejiet uz sadaļu Mazumtirdzniecība un tirdzniecība > Krājumu pārvaldība > Papildināšana > Preču pakotnes.</span><span class="sxs-lookup"><span data-stu-id="0b0be-108">Go to Retail and Commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="0b0be-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="0b0be-109">Click New.</span></span>
3. <span data-ttu-id="0b0be-110">Laukā Pakotnes numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="0b0be-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="0b0be-111">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="0b0be-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0b0be-112">Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0b0be-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="0b0be-113">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0b0be-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="0b0be-114">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="0b0be-114">Click Add.</span></span>
8. <span data-ttu-id="0b0be-115">Laukā Krājuma kods ierakstiet 0160.</span><span class="sxs-lookup"><span data-stu-id="0b0be-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="0b0be-116">Laukā Lielums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="0b0be-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="0b0be-117">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0b0be-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="0b0be-118">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="0b0be-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="0b0be-119">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="0b0be-119">Click Add.</span></span>
13. <span data-ttu-id="0b0be-120">Laukā Krājuma kods ierakstiet 0160.</span><span class="sxs-lookup"><span data-stu-id="0b0be-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="0b0be-121">Laukā Varianta numurs noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="0b0be-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="0b0be-122">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0b0be-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="0b0be-123">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="0b0be-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="0b0be-124">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="0b0be-124">Click Add.</span></span>
18. <span data-ttu-id="0b0be-125">Laukā Krājuma kods ierakstiet 0175.</span><span class="sxs-lookup"><span data-stu-id="0b0be-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="0b0be-126">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="0b0be-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="0b0be-127">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="0b0be-127">Click Save.</span></span>
21. <span data-ttu-id="0b0be-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0b0be-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="0b0be-129">Iepakojuma pievienošana pirkšanas pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="0b0be-129">Add package to purchase order</span></span>
1. <span data-ttu-id="0b0be-130">Pārejiet uz sadaļu Kreditori > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="0b0be-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="0b0be-131">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="0b0be-131">Click New.</span></span>
3. <span data-ttu-id="0b0be-132">Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0b0be-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="0b0be-133">Sarakstā atlasiet to pašu kreditoru, kam iepriekš tika izveidota preču pakotne, ja kreditors tika atlasīts.</span><span class="sxs-lookup"><span data-stu-id="0b0be-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="0b0be-134">Pārslēdziet sadaļas Vispārīgi paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="0b0be-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="0b0be-135">Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0b0be-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0b0be-136">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0b0be-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="0b0be-137">Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0b0be-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="0b0be-138">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0b0be-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="0b0be-139">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="0b0be-139">Click OK.</span></span>
11. <span data-ttu-id="0b0be-140">Pārslēdziet sadaļas Detalizēta rindas informācija paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="0b0be-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="0b0be-141">Noklikšķiniet uz cilnes Preču pakotnes.</span><span class="sxs-lookup"><span data-stu-id="0b0be-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="0b0be-142">Noklikšķiniet uz Pirkšanas pasūtījuma rinda.</span><span class="sxs-lookup"><span data-stu-id="0b0be-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="0b0be-143">Noklikšķiniet uz Izveidot rindas, izmantojot pakotni.</span><span class="sxs-lookup"><span data-stu-id="0b0be-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="0b0be-144">Sarakstā atrodiet un atlasiet preču pakotni, kas tika izveidota iepriekšējā darbībā.</span><span class="sxs-lookup"><span data-stu-id="0b0be-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="0b0be-145">Laukā Daudzums ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="0b0be-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="0b0be-146">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="0b0be-146">Click Create.</span></span>
18. <span data-ttu-id="0b0be-147">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="0b0be-147">Click Save.</span></span>

