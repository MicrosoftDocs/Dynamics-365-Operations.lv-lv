---
title: Procentu apstrāde
description: Šajā procedūrā parādīts, kā izveidot, izdrukāt un grāmatot procentu paziņojumus.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 093fbd23f9fcaf62db9988a98a94b8cebf582768
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140149"
---
# <a name="process-interest"></a><span data-ttu-id="511f7-103">Procentu apstrāde</span><span class="sxs-lookup"><span data-stu-id="511f7-103">Process interest</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="511f7-104">Šajā procedūrā parādīts, kā izveidot, izdrukāt un grāmatot procentu paziņojumus.</span><span class="sxs-lookup"><span data-stu-id="511f7-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="511f7-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="511f7-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="511f7-106">Iestatiet grāmatošanas metodes procentus.</span><span class="sxs-lookup"><span data-stu-id="511f7-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="511f7-107">**Navigācijas rūtī** ejiet uz **Moduļi > Kredīts un atgūšana > Iestatīšana >Klientu grāmatošanas profili**.</span><span class="sxs-lookup"><span data-stu-id="511f7-107">In the **Navigation pane**, go to **Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="511f7-108">Noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="511f7-108">Click **Edit**.</span></span>
3. <span data-ttu-id="511f7-109">Kopsavilkuma cilnē **Uzstādīšana**, laukā **Procentu kods** ievadiet procentu kodu no nolaižamā saraksta.</span><span class="sxs-lookup"><span data-stu-id="511f7-109">In the **Setup fastTab**, in the **Interest code** field, select an interest code from the drop-down list.</span></span> <span data-ttu-id="511f7-110">Ja nevēlaties veikt procentu aprēķinu transakcijām, izmantojot šo grāmatošanas metodi, atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="511f7-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span> <span data-ttu-id="511f7-111">Kopsavilkuma cilne **Tabulas ierobežojumi** ļauj jums mainīt veidu, kādā tiek apstrādāti procenti.</span><span class="sxs-lookup"><span data-stu-id="511f7-111">The **Table restriction** fastTab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="511f7-112">Ja šajā laukā ir iestatīts Jā, procenti šai grāmatošanas metodei tiks aprēķināti.</span><span class="sxs-lookup"><span data-stu-id="511f7-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="511f7-113">Aprēķināt procentus</span><span class="sxs-lookup"><span data-stu-id="511f7-113">Calculate interest</span></span>
1. <span data-ttu-id="511f7-114">**Navigācijas rūtī** ejiet uz **Moduļi > Kredīts un atgūšana > Soda nauda >Izveidot soda naudas piezīmes**.</span><span class="sxs-lookup"><span data-stu-id="511f7-114">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Create interest notes**.</span></span>
2. <span data-ttu-id="511f7-115">Atlasiet transakciju veidus, kuriem aprēķināsit procentus.</span><span class="sxs-lookup"><span data-stu-id="511f7-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="511f7-116">Aprēķinā tiks iekļautas visas šiem tipiem atbilstošās atvērtās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="511f7-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="511f7-117">Ja iestatāt **Procentus** uz 'Jā', jūs aprēķināsit procentus par procentiem.</span><span class="sxs-lookup"><span data-stu-id="511f7-117">If you set **Interest** to 'Yes', you will calculate interest on interest.</span></span> <span data-ttu-id="511f7-118">Pirms šo transakciju pievienošanas, iespējams, vēlēsities pārbaudīt likumus, kas regulē procentu aprēķināšanu procentiem.</span><span class="sxs-lookup"><span data-stu-id="511f7-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
4. <span data-ttu-id="511f7-119">Laukā **Datums no** ievadiet datumu, no kura tiks aprēķināti procenti.</span><span class="sxs-lookup"><span data-stu-id="511f7-119">In the **From date** field, enter a date from which the interest will be calculated.</span></span> <span data-ttu-id="511f7-120">Ja jums nav konkrēta **Datuma no**, tad visi negrāmatotie procentu paziņojumi tiks atcelti un procenti tiks atkārtoti aprēķināti no darījuma datuma.</span><span class="sxs-lookup"><span data-stu-id="511f7-120">If you do not specific a **From date**, then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>
5. <span data-ttu-id="511f7-121">Laukā **Datums līdz** ievadiet datumu, līdz kuram tiktu aprēķināti procenti.</span><span class="sxs-lookup"><span data-stu-id="511f7-121">In the **To date** field, enter a date to which the interest would be calculated.</span></span>
6. <span data-ttu-id="511f7-122">Laukā **Izmantot grāmatošanas profilu no** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="511f7-122">In the **Use posting profile from** field, select an option.</span></span> <span data-ttu-id="511f7-123">Ir trīs grāmatošanas profila opcijas:</span><span class="sxs-lookup"><span data-stu-id="511f7-123">There are three posting profile options:</span></span>
    - <span data-ttu-id="511f7-124">Konts — katram procentu paziņojumam lietojiet debitora kontam piešķirto grāmatošanas metodi.</span><span class="sxs-lookup"><span data-stu-id="511f7-124">Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span> 
    - <span data-ttu-id="511f7-125">Atlasīt — lietojiet grāmatošanas profilu, kas ir atlasīts laukā Grāmatošanas metode.</span><span class="sxs-lookup"><span data-stu-id="511f7-125">Select – Use the posting profile that you select in the Posting profile field.</span></span>
    - <span data-ttu-id="511f7-126">Transakcija — izmantot katram procentu paziņojumam atsevišķu grāmatošanas metodi transakcijām, par kurām tiek aprēķināti procenti.</span><span class="sxs-lookup"><span data-stu-id="511f7-126">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="511f7-127">Transakcijām, kurām nav piešķirta grāmatošanas metode, tiek izmantota grāmatošanas metode, kura ir norādīta veidlapas Debitoru parametri apgabalā Virsgrāmata un PVN formā.</span><span class="sxs-lookup"><span data-stu-id="511f7-127">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
7. <span data-ttu-id="511f7-128">Izvērtiet cilni **Iekļaujamie ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="511f7-128">Expand the **Records to include** fastTab.</span></span>
8. <span data-ttu-id="511f7-129">Noklikšķiniet uz **Filtrēt**.</span><span class="sxs-lookup"><span data-stu-id="511f7-129">Click **Filter**.</span></span>
9. <span data-ttu-id="511f7-130">Laukā **Kritērijs** ievadiet debitora ID.</span><span class="sxs-lookup"><span data-stu-id="511f7-130">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="511f7-131">Piemēram, ievadiet US-001.</span><span class="sxs-lookup"><span data-stu-id="511f7-131">For example, enter 'US-001'.</span></span>
6. <span data-ttu-id="511f7-132">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="511f7-132">Click **OK**.</span></span>
7. <span data-ttu-id="511f7-133">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="511f7-133">Click **OK**.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="511f7-134">Drukāt procentu paziņojumus</span><span class="sxs-lookup"><span data-stu-id="511f7-134">Print interest notes</span></span>
1. <span data-ttu-id="511f7-135">**Navigācijas rūtī** ejiet uz **Moduļi > Kredīts un atgūšana > Procenti >Izskatīt un apstrādāt procentu piezīmes**.</span><span class="sxs-lookup"><span data-stu-id="511f7-135">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Review and process interest notes**.</span></span>
2. <span data-ttu-id="511f7-136">Laukā **Statuss** atlasiet 'Izveidots'.</span><span class="sxs-lookup"><span data-stu-id="511f7-136">In the **Status** field, select 'Created'.</span></span>
3. <span data-ttu-id="511f7-137">Laukā **Drukāts** atlasiet 'Nav drukāts'.</span><span class="sxs-lookup"><span data-stu-id="511f7-137">In the **Printed** field, select 'Not printed'.</span></span>
4. <span data-ttu-id="511f7-138">Noklikšķiniet uz **Drukāt**.</span><span class="sxs-lookup"><span data-stu-id="511f7-138">Click **Print**.</span></span>
5. <span data-ttu-id="511f7-139">Izvērtiet cilni **Iekļaujamie ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="511f7-139">Expand the **Records to include** fastTab.</span></span>
6. <span data-ttu-id="511f7-140">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="511f7-140">Click **OK**.</span></span>
7. <span data-ttu-id="511f7-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="511f7-141">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="511f7-142">Procentu paziņojuma grāmatošana</span><span class="sxs-lookup"><span data-stu-id="511f7-142">Post the interest note</span></span>
1. <span data-ttu-id="511f7-143">Atlasiet procentu paziņojumu, kas ir gatavs grāmatošanai (statuss ir Izveidots).</span><span class="sxs-lookup"><span data-stu-id="511f7-143">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="511f7-144">Noklikšķiniet uz **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="511f7-144">Click **Post**.</span></span>
3. <span data-ttu-id="511f7-145">Ievadiet procentu paziņojuma grāmatošanas datumu.</span><span class="sxs-lookup"><span data-stu-id="511f7-145">Enter the posting date for the interest note.</span></span> <span data-ttu-id="511f7-146">Lai katram procentu paziņojumam izveidotu Virsgrāmatas transakciju, atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="511f7-146">Select Yes to create a general ledger transaction for each interest note.</span></span> <span data-ttu-id="511f7-147">Ja neatlasāt vērtību Jā, visi debitora procentu paziņojumu procenti tiek uzkrāti un grāmatoti Virsgrāmatā vienā transakcijā.</span><span class="sxs-lookup"><span data-stu-id="511f7-147">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="511f7-148">Izvērtiet cilni **Iekļaujamie ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="511f7-148">Expand the **Records to include** fastTab.</span></span>
5. <span data-ttu-id="511f7-149">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="511f7-149">Click **OK**.</span></span>
6. <span data-ttu-id="511f7-150">Laukā **Statuss** atlasiet 'Iegrāmatots'.</span><span class="sxs-lookup"><span data-stu-id="511f7-150">In the **Status** field, select 'Posted'.</span></span>

