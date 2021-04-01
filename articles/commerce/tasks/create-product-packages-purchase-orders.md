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
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d16c5c576ce6b35687fb7edab835d52f6f58e6a0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256977"
---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="db10e-103">Preču iepakojumu izveide pirkšanas pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="db10e-103">Create product packages for purchase orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db10e-104">Šajā procedūrā ir aprakstīts, ka izveidot preču pakotni un izmantot to pirkšanas pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="db10e-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="db10e-105">Pirkšanas pasūtījums tiks izmantots, lai izveidotu pasūtījumu iepriekš definētai preču kopai.</span><span class="sxs-lookup"><span data-stu-id="db10e-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="db10e-106">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="db10e-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="db10e-107">Preču pakotnes izveide</span><span class="sxs-lookup"><span data-stu-id="db10e-107">Create a product package</span></span>
1. <span data-ttu-id="db10e-108">Pārejiet uz sadaļu Mazumtirdzniecība un tirdzniecība > Krājumu pārvaldība > Papildināšana > Preču pakotnes.</span><span class="sxs-lookup"><span data-stu-id="db10e-108">Go to Retail and Commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="db10e-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="db10e-109">Click New.</span></span>
3. <span data-ttu-id="db10e-110">Laukā Pakotnes numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="db10e-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="db10e-111">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="db10e-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="db10e-112">Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="db10e-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="db10e-113">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="db10e-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="db10e-114">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="db10e-114">Click Add.</span></span>
8. <span data-ttu-id="db10e-115">Laukā Krājuma kods ierakstiet 0160.</span><span class="sxs-lookup"><span data-stu-id="db10e-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="db10e-116">Laukā Lielums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="db10e-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="db10e-117">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="db10e-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="db10e-118">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="db10e-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="db10e-119">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="db10e-119">Click Add.</span></span>
13. <span data-ttu-id="db10e-120">Laukā Krājuma kods ierakstiet 0160.</span><span class="sxs-lookup"><span data-stu-id="db10e-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="db10e-121">Laukā Varianta numurs noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="db10e-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="db10e-122">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="db10e-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="db10e-123">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="db10e-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="db10e-124">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="db10e-124">Click Add.</span></span>
18. <span data-ttu-id="db10e-125">Laukā Krājuma kods ierakstiet 0175.</span><span class="sxs-lookup"><span data-stu-id="db10e-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="db10e-126">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="db10e-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="db10e-127">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="db10e-127">Click Save.</span></span>
21. <span data-ttu-id="db10e-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="db10e-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="db10e-129">Iepakojuma pievienošana pirkšanas pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="db10e-129">Add package to purchase order</span></span>
1. <span data-ttu-id="db10e-130">Pārejiet uz sadaļu Kreditori > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="db10e-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="db10e-131">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="db10e-131">Click New.</span></span>
3. <span data-ttu-id="db10e-132">Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="db10e-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="db10e-133">Sarakstā atlasiet to pašu kreditoru, kam iepriekš tika izveidota preču pakotne, ja kreditors tika atlasīts.</span><span class="sxs-lookup"><span data-stu-id="db10e-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="db10e-134">Pārslēdziet sadaļas Vispārīgi paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="db10e-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="db10e-135">Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="db10e-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="db10e-136">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="db10e-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="db10e-137">Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="db10e-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="db10e-138">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="db10e-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="db10e-139">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="db10e-139">Click OK.</span></span>
11. <span data-ttu-id="db10e-140">Pārslēdziet sadaļas Detalizēta rindas informācija paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="db10e-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="db10e-141">Noklikšķiniet uz cilnes Preču pakotnes.</span><span class="sxs-lookup"><span data-stu-id="db10e-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="db10e-142">Noklikšķiniet uz Pirkšanas pasūtījuma rinda.</span><span class="sxs-lookup"><span data-stu-id="db10e-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="db10e-143">Noklikšķiniet uz Izveidot rindas, izmantojot pakotni.</span><span class="sxs-lookup"><span data-stu-id="db10e-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="db10e-144">Sarakstā atrodiet un atlasiet preču pakotni, kas tika izveidota iepriekšējā darbībā.</span><span class="sxs-lookup"><span data-stu-id="db10e-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="db10e-145">Laukā Daudzums ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="db10e-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="db10e-146">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="db10e-146">Click Create.</span></span>
18. <span data-ttu-id="db10e-147">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="db10e-147">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]