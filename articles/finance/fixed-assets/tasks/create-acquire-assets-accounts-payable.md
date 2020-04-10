---
title: Līdzekļu izveide un iegūšana no kreditoriem
description: Šis uzdevuma ceļvedis apraksta pamatlīdzekļa izveidi un iegādi, izmantojot pirkšanas procesu.
author: saraschi2
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7cb9a37c65fb8eab4db6084b91a71c13a45ba42c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142873"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="1b25f-103">Līdzekļu izveide un iegūšana no kreditoriem</span><span class="sxs-lookup"><span data-stu-id="1b25f-103">Create and acquire assets from Accounts payable</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1b25f-104">Šis uzdevuma ceļvedis apraksta pamatlīdzekļa izveidi un iegādi, izmantojot pirkšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="1b25f-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span>  <span data-ttu-id="1b25f-105">Tas izmanto grāmatveža un kreditoriem maksājamo rēķinu darbinieka lomas, kā arī demonstrācijas uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="1b25f-105">It uses the Accountant and Accounts payable clerks and the demo company USMF .</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="1b25f-106">Pamatlīdzekļu parametru iestatīšana</span><span class="sxs-lookup"><span data-stu-id="1b25f-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="1b25f-107">**Navigācijas rūtī** ejiet uz **Moduļi > Pamatlīdzekļi > Iestatīšana> Pamatlīdzekļu parametri**.</span><span class="sxs-lookup"><span data-stu-id="1b25f-107">In the **Navigation pane**, go to **Modules > Fixed assets > Setup > Fixed assets parameters**.</span></span>
2. <span data-ttu-id="1b25f-108">Izvērsiet kopsavilkuma cilni **Pirkuma pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="1b25f-108">Expand the **Purchase orders** fastTab.</span></span>
3. <span data-ttu-id="1b25f-109">Atzīmējiet izvēles rūtiņu **Atļaut līdzekļu iegādi no pirkšanas**.</span><span class="sxs-lookup"><span data-stu-id="1b25f-109">Check the **Allow asset acquisition from Purchasing** checkbox.</span></span>
4. <span data-ttu-id="1b25f-110">Atzīmējiet izvēles rūtiņu **Izveidot līdzekli produkta saņemšanas vai rēķina publicēšanas laikā**.</span><span class="sxs-lookup"><span data-stu-id="1b25f-110">Check the **Create asset during product receipt or invoice posting** checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="1b25f-111">Jauna kreditora rēķina izveide</span><span class="sxs-lookup"><span data-stu-id="1b25f-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="1b25f-112">**Navigācijas rūtī** pārejiet uz sadaļu **Moduļi > Kreditori > Darbvietas > Piegādātāju rēķina ieraksts**.</span><span class="sxs-lookup"><span data-stu-id="1b25f-112">In the **Navigation pane**, go to **Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="1b25f-113">Klikšķiniet uz **Jauns piegādātāja rēķins**.</span><span class="sxs-lookup"><span data-stu-id="1b25f-113">Click **New vendor invoice**.</span></span>
3. <span data-ttu-id="1b25f-114">Laukā **Rēķina konts** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="1b25f-114">In the **Invoice account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="1b25f-115">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1b25f-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="1b25f-116">Laukā **Numurs** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="1b25f-116">In the **Number** field, type a value.</span></span>
6. <span data-ttu-id="1b25f-117">Laukā **Publicēšanas datums** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="1b25f-117">In the **Posting date** field, enter a date.</span></span>
7. <span data-ttu-id="1b25f-118">Nokl. **Piev. r.**</span><span class="sxs-lookup"><span data-stu-id="1b25f-118">Click **Add line**.</span></span>
8. <span data-ttu-id="1b25f-119">Laukā **Krājuma kods** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="1b25f-119">In the **Item number** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="1b25f-120">Pamatlīdzekļu iegādei var tikt izmantoti vai nu noliktavā neesoši krājumi vai sagādes kategorijas.</span><span class="sxs-lookup"><span data-stu-id="1b25f-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="1b25f-121">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1b25f-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="1b25f-122">Laukā **Daudzums** ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="1b25f-122">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="1b25f-123">Viena rēķina rinda izveidos tikai vienu pamatlīdzekli neatkarīgi no daudzuma.</span><span class="sxs-lookup"><span data-stu-id="1b25f-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span> <span data-ttu-id="1b25f-124">Rēķina daudzuma lauka vērtība tiks pārnesta uz pamatlīdzekļa daudzumu.</span><span class="sxs-lookup"><span data-stu-id="1b25f-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="1b25f-125">Laukā **Vienības cena** ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="1b25f-125">In the **Unit price** field, enter a number.</span></span>
12. <span data-ttu-id="1b25f-126">Izvērsiet kopsavilkuma cilni **Detalizēta informācija par rindu**.</span><span class="sxs-lookup"><span data-stu-id="1b25f-126">Expand the **Line details** fastTab.</span></span>
13. <span data-ttu-id="1b25f-127">Noklikšķiniet uz cilnes **Pamatlīdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="1b25f-127">Click the **Fixed assets** tab.</span></span>
14. <span data-ttu-id="1b25f-128">Atzīmējiet izvēles rūtiņu **Izveidot jaunu pamatlīdzekli**.</span><span class="sxs-lookup"><span data-stu-id="1b25f-128">Check the **Create a new fixed asset** checkbox.</span></span>
15. <span data-ttu-id="1b25f-129">Laukā **Pamatlīdzekļu grupa** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="1b25f-129">In the **Fixed asset group** field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="1b25f-130">Sarakstā atlasiet pamatlīdzekļu grupu, kura tiks izmantota jauna pamatlīdzekļa izveidei.</span><span class="sxs-lookup"><span data-stu-id="1b25f-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="1b25f-131">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1b25f-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="1b25f-132">Noklikšķiniet uz **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="1b25f-132">Click **Post**.</span></span> <span data-ttu-id="1b25f-133">Pamatlīdzeklis tiks izveidots un iegūts, iegrāmatojot rēķinu.</span><span class="sxs-lookup"><span data-stu-id="1b25f-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  

