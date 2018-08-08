--- 
title: "Līdzekļu izveide un iegūšana modulī Kreditori"
description: "Šis uzdevuma ceļvedis apraksta pamatlīdzekļa izveidi un iegādi, izmantojot pirkšanas procesu."
author: saraschi2
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 298e2386e5cfe8ac1abaaea53b0d2d686e76da87
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="4fb6d-103">Līdzekļu izveide un iegūšana modulī Kreditori</span><span class="sxs-lookup"><span data-stu-id="4fb6d-103">Create and acquire assets from accounts payable</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4fb6d-104">Šis uzdevuma ceļvedis apraksta pamatlīdzekļa izveidi un iegādi, izmantojot pirkšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span> <span data-ttu-id="4fb6d-105">Tas izmanto grāmatveža un kreditoriem maksājamo rēķinu darbinieka lomas, kā arī demonstrācijas uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-105">It uses the Accountant and Accounts payable clerks and the demo company USMF.</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="4fb6d-106">Pamatlīdzekļu parametru iestatīšana</span><span class="sxs-lookup"><span data-stu-id="4fb6d-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="4fb6d-107">Pārejiet uz sadaļu Pamatlīdzekļi > Iestatījumi > Pamatlīdzekļu parametri.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-107">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="4fb6d-108">Izvērsiet vai sakļaujiet sadaļu Pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-108">Expand or collapse the Purchase orders section.</span></span>
3. <span data-ttu-id="4fb6d-109">Atzīmējiet izvēles rūtiņu Atļaut līdzekļu iegādi no Pirkšanas.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-109">Check the Allow asset acquisition from Purchasing checkbox.</span></span>
4. <span data-ttu-id="4fb6d-110">Atzīmējiet izvēles rūtiņu Izveidot līdzekli produktu ieejas plūsmas vai rēķina grāmatošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-110">Check the Create asset during product receipt or invoice posting checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="4fb6d-111">Jauna kreditora rēķina izveide</span><span class="sxs-lookup"><span data-stu-id="4fb6d-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="4fb6d-112">Pārejiet uz sadaļu Kreditori > Darbvietas > Kreditora rēķina ieraksts.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-112">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="4fb6d-113">Noklikšķiniet uz Jauns kreditora rēķins.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-113">Click New vendor invoice.</span></span>
3. <span data-ttu-id="4fb6d-114">Laukā Rēķina konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-114">In the Invoice account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4fb6d-115">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="4fb6d-116">Laukā Numurs ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-116">In the Number field, type a value.</span></span>
6. <span data-ttu-id="4fb6d-117">Ievadiet datumu laukā Grāmatošanas datums.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-117">In the Posting date field, enter a date.</span></span>
7. <span data-ttu-id="4fb6d-118">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-118">Click Add line.</span></span>
8. <span data-ttu-id="4fb6d-119">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4fb6d-120">Pamatlīdzekļu iegādei var tikt izmantoti vai nu noliktavā neesoši krājumi vai sagādes kategorijas.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="4fb6d-121">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="4fb6d-122">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="4fb6d-123">Viena rēķina rinda izveidos tikai vienu pamatlīdzekli neatkarīgi no daudzuma.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span>  <span data-ttu-id="4fb6d-124">Rēķina daudzuma lauka vērtība tiks pārnesta uz pamatlīdzekļa daudzumu.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="4fb6d-125">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-125">In the Unit price field, enter a number.</span></span>
12. <span data-ttu-id="4fb6d-126">Izvērsiet vai sakļaujiet sadaļu Detalizēta rindas informācija.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-126">Expand or collapse the Line details section.</span></span>
13. <span data-ttu-id="4fb6d-127">Noklikšķiniet uz cilnes Pamatlīdzekļi.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-127">Click the Fixed assets tab.</span></span>
14. <span data-ttu-id="4fb6d-128">Atzīmējiet izvēles rūtiņu Izveidot jaunu pamatlīdzekli..</span><span class="sxs-lookup"><span data-stu-id="4fb6d-128">Check the Create a new fixed asset checkbox.</span></span>
15. <span data-ttu-id="4fb6d-129">Laukā Pamatlīdzekļa grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-129">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="4fb6d-130">Sarakstā atlasiet pamatlīdzekļu grupu, kura tiks izmantota jauna pamatlīdzekļa izveidei.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="4fb6d-131">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="4fb6d-132">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-132">Click Post.</span></span>
    * <span data-ttu-id="4fb6d-133">Pamatlīdzeklis tiks izveidots un iegūts, iegrāmatojot rēķinu.</span><span class="sxs-lookup"><span data-stu-id="4fb6d-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  


