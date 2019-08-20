---
title: Automātiskās kravas saskaņošanas iestatīšana
description: Šajā procedūrā parādīts kā iestatīt datus automātiskai kravas saskaņošanai.
author: ShylaThompson
manager: AnnBe
ms.date: 10/16/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 057d1b3a1b5294c75f02f4ed443ae6f525ac6b83
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837618"
---
# <a name="set-up-automatic-freight-reconciliation"></a><span data-ttu-id="c6e3c-103">Automātiskās kravas saskaņošanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="c6e3c-103">Set up automatic freight reconciliation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c6e3c-104">Šajā procedūrā parādīts kā iestatīt datus automātiskai kravas saskaņošanai.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-104">This procedure shows how to set up data for automatic freight reconciliation.</span></span> <span data-ttu-id="c6e3c-105">To parasti veic noliktavas pārvaldnieks.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-105">This is typically done by a warehouse manager.</span></span> <span data-ttu-id="c6e3c-106">Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-106">You can use this procedure in demo data company USMF.</span></span>


## <a name="set-up-the-freight-bill-type"></a><span data-ttu-id="c6e3c-107">Kravas pavadzīmes veida iestatīšana</span><span class="sxs-lookup"><span data-stu-id="c6e3c-107">Set up the freight bill type</span></span>
1. <span data-ttu-id="c6e3c-108">Dodieties uz Transportēšanas pārvaldība > Iestatīšana > Kravas saskaņošana > Kravas pavadzīmes veids.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-108">Go to Transportation management > Setup > Freight reconciliation > Freight bill type.</span></span>
    * <span data-ttu-id="c6e3c-109">Kravas pavadzīmes tips nosaka kā jāsaskaņo kravas pavadzīmes un pārvadātāja rēķinus.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-109">The freight bill type defines how freight bills and carrier invoices  should be matched.</span></span>  
2. <span data-ttu-id="c6e3c-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-110">Click New.</span></span>
3. <span data-ttu-id="c6e3c-111">Laukā Kravas pavadzīmes veids ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-111">In the Freight bill type field, type a value.</span></span>
4. <span data-ttu-id="c6e3c-112">Laukā Programmas komplektācija ierakstiet “Microsoft.Dynamics.Ax.Tms.dll”.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-112">In the Engine assembly field, type 'Microsoft.Dynamics.Ax.Tms.dll'.</span></span>
    * <span data-ttu-id="c6e3c-113">Tā ir standarta Transportēšanas pārvaldības atbilstoša programmas koda bibliotēka.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-113">This is the standard Transportation management matching engine code library.</span></span>  
5. <span data-ttu-id="c6e3c-114">Laukā Programmas klase ierakstiet “Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer”.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-114">In the Engine class field, type 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.</span></span>
    * <span data-ttu-id="c6e3c-115">Tā ir standarta Transportēšanas pārvaldības atbilstoša programmas koda klase.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-115">This is the standard Transportation management matching engine class.</span></span>  
6. <span data-ttu-id="c6e3c-116">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-116">Click New.</span></span>
7. <span data-ttu-id="c6e3c-117">Laukā Apraksts atlasiet vērtību, kas atbilst kravas pavadzīmei un pārvadātāja rēķinam.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-117">In the Description field, choose the value that should match on the freight bill and the carrier invoice.</span></span>  
8. <span data-ttu-id="c6e3c-118">Laukā Nepieciešama saskaņošana atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-118">In the Match required field, select 'Yes'.</span></span>
    * <span data-ttu-id="c6e3c-119">Ja iestatāt šajā laukā Jā, tas nozīmē, ka vērtībai, kas ir atlasīta laukā Apraksts ir jāatbilst gan kravas pavadzīmei, gan pārvadātāja rēķinam.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-119">If you set this field to Yes this means that the value selected in the Description field needs to match on both the freight bill and the carrier invoice.</span></span> <span data-ttu-id="c6e3c-120">Ja iestatāt Nē, lauks var būt tukšs vienā no tiem.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-120">If you set it to No, the field can be blank on one of these.</span></span>  
9. <span data-ttu-id="c6e3c-121">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-121">Click Save.</span></span>

## <a name="set-up-the-freight-bill-type-assignment"></a><span data-ttu-id="c6e3c-122">Kravas pavadzīmes veida piešķires iestatīšana</span><span class="sxs-lookup"><span data-stu-id="c6e3c-122">Set up the freight bill type assignment</span></span>
1. <span data-ttu-id="c6e3c-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-123">Close the page.</span></span>
2. <span data-ttu-id="c6e3c-124">Dodieties uz Transportēšanas pārvaldība > Iestatīšana > Kravas saskaņošana > Kravas pavadzīmes veida piešķires.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-124">Go to Transportation management > Setup > Freight reconciliation > Freight bill type assignments.</span></span>
    * <span data-ttu-id="c6e3c-125">Kravas pavadzīmes veida piešķire tiek izmantota, lai norādītu, kuras kravas pavadzīmes veids tiek izmantots noteiktam pārvadātājam.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-125">The freight bill type assignment is used to specify which freight bill type is used for a particular carrier.</span></span>   
3. <span data-ttu-id="c6e3c-126">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-126">Click New.</span></span>
4. <span data-ttu-id="c6e3c-127">Laukā Režīms ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-127">In the Mode field, enter or select a value.</span></span>
5. <span data-ttu-id="c6e3c-128">Laukā Sūtījumu pārvadātājs ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-128">In the Shipping carrier field, enter or select a value.</span></span>
6. <span data-ttu-id="c6e3c-129">Laukā Kravas pavadzīmes veids atlasiet kravas pavadzīmes veidu, ko izveidojāt agrāk.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-129">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
7. <span data-ttu-id="c6e3c-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-130">Close the page.</span></span>

## <a name="set-up-the-audit-master"></a><span data-ttu-id="c6e3c-131">Audita šablona iestatīšana</span><span class="sxs-lookup"><span data-stu-id="c6e3c-131">Set up the audit master</span></span>
1. <span data-ttu-id="c6e3c-132">Dodieties uz Transportēšanas pārvaldība > Iestatīšana > Kravas saskaņošana > Audita šablons.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-132">Go to Transportation management > Setup > Freight reconciliation > Audit master.</span></span>
    * <span data-ttu-id="c6e3c-133">Audita šablons nosaka tolerances ierobežojumus automātiskai kravas saskaņošanai.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-133">The audit master defines the tolerance limits for automatic freight reconciliation.</span></span> <span data-ttu-id="c6e3c-134">Tas norāda par cik daudz var atšķirties naudas summas kravas pavadzīmē un pārvadātāja rēķinā, un joprojām pieļaut saskaņošanu.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-134">It specifies by how much the monetary amounts on the freight bill and the carrier invoice can differ and still allow reconciliation to occur.</span></span> <span data-ttu-id="c6e3c-135">Tas arī nosaka kā apstrādāt neatbilstības.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-135">It also defines how to handle discrepancies.</span></span>  
2. <span data-ttu-id="c6e3c-136">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-136">Click New.</span></span>
3. <span data-ttu-id="c6e3c-137">Laukā Audita šablona ID ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-137">In the Audit master ID field, type a value.</span></span>
4. <span data-ttu-id="c6e3c-138">Laukā Sūtījumu pārvadātājs atlasiet to pašu sūtījumu pārvadātāju, kā to darījāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-138">In the Shipping carrier  field, select the same shipping carrier as you did earlier.</span></span>
5. <span data-ttu-id="c6e3c-139">Laukā Kravas pavadzīmes veids atlasiet kravas pavadzīmes veidu, ko izveidojāt agrāk.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-139">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
6. <span data-ttu-id="c6e3c-140">Izvērsiet sadaļu Tolerance.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-140">Expand the Tolerance section.</span></span>
7. <span data-ttu-id="c6e3c-141">Laukā Minimālais tolerances līmenis ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-141">In the Minimum tolerance level field, enter a number.</span></span>
8. <span data-ttu-id="c6e3c-142">Laukā Maksimālās tolerances līmenis ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-142">In the Maximum tolerance level field, enter a number.</span></span>
9. <span data-ttu-id="c6e3c-143">Izvērsiet sadaļu Rezultāts.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-143">Expand the Result section.</span></span>
10. <span data-ttu-id="c6e3c-144">Laukā Pārmaksas iemesla kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-144">In the Overpayment reason code field, enter or select a value.</span></span>
    * <span data-ttu-id="c6e3c-145">Ja naudas summas atšķiras no kravas pavadzīmes un pārvadātāja rēķina, pārmaksas un nepilnas samaksas iemesla kodi norāda kontus, kuros nepieciešams reģistrēt starpību, ja vien starpība nepārsniedz tolerances līmeņus.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-145">If the monetary amounts differ on the freight bill and the carrier invoice, the overpayment and underpayment reason codes specify the accounts that the difference should be registered on, as long as the difference is within the tolerance levels.</span></span>  
11. <span data-ttu-id="c6e3c-146">Laukā Nepilnas samaksas iemesla kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-146">In the Underpayment reason code field, enter or select a value.</span></span>
12. <span data-ttu-id="c6e3c-147">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c6e3c-147">Close the page.</span></span>

