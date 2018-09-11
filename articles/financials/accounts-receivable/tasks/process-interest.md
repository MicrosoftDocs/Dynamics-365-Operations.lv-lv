--- 
title: "Procentu apstrāde"
description: "Šajā procedūrā parādīts, kā izveidot, izdrukāt un grāmatot procentu paziņojumus."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 582ebdc6e9481487dcc45b6e212c5d0f8c9f1fc1
ms.contentlocale: lv-lv
ms.lasthandoff: 09/11/2018

---
# <a name="process-interest"></a><span data-ttu-id="068b1-103">Procentu apstrāde</span><span class="sxs-lookup"><span data-stu-id="068b1-103">Process interest</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="068b1-104">Šajā procedūrā parādīts, kā izveidot, izdrukāt un grāmatot procentu paziņojumus.</span><span class="sxs-lookup"><span data-stu-id="068b1-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="068b1-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="068b1-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="068b1-106">Iestatiet grāmatošanas metodes procentus.</span><span class="sxs-lookup"><span data-stu-id="068b1-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="068b1-107">Pārejiet uz sadaļu Kredīts un iekasēšana > Iestatījumi > Debitoru grāmatošanas metodes.</span><span class="sxs-lookup"><span data-stu-id="068b1-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="068b1-108">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="068b1-108">Click Edit.</span></span>
    * <span data-ttu-id="068b1-109">Nolaižamajā sarakstā atlasiet procentu kodu.</span><span class="sxs-lookup"><span data-stu-id="068b1-109">Select an interest code from the drop-down list.</span></span> <span data-ttu-id="068b1-110">Ja nevēlaties veikt procentu aprēķinu transakcijām, izmantojot šo grāmatošanas metodi, atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="068b1-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="068b1-111">Cilnē Tabulas ierobežojums varat mainīt veidu, kā tiek apstrādāti procenti.</span><span class="sxs-lookup"><span data-stu-id="068b1-111">The Table restriction tab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="068b1-112">Ja šajā laukā ir iestatīts Jā, procenti šai grāmatošanas metodei tiks aprēķināti.</span><span class="sxs-lookup"><span data-stu-id="068b1-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="068b1-113">Aprēķināt procentus</span><span class="sxs-lookup"><span data-stu-id="068b1-113">Calculate interest</span></span>
1. <span data-ttu-id="068b1-114">Pārejiet uz sadaļu Kredīts un iekasēšana > Procenti > Izveidot procentu paziņojumus.</span><span class="sxs-lookup"><span data-stu-id="068b1-114">Go to Credit and collections > Interest > Create interest notes.</span></span>
    * <span data-ttu-id="068b1-115">Atlasiet transakciju veidus, kuriem aprēķināsit procentus.</span><span class="sxs-lookup"><span data-stu-id="068b1-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="068b1-116">Aprēķinā tiks iekļautas visas šiem tipiem atbilstošās atvērtās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="068b1-116">All of the open transactions for these types will be included in the calculation.</span></span>  
    * <span data-ttu-id="068b1-117">Ja atlasāt Procenti, aprēķināsit procentus par procentiem.</span><span class="sxs-lookup"><span data-stu-id="068b1-117">If you select Interest, you will calculate interest on interest.</span></span> <span data-ttu-id="068b1-118">Pirms šo transakciju pievienošanas, iespējams, vēlēsities pārbaudīt likumus, kas regulē procentu aprēķināšanu procentiem.</span><span class="sxs-lookup"><span data-stu-id="068b1-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
    * <span data-ttu-id="068b1-119">Procenti tiks aprēķināti no šī datuma līdz datumam, kas norādīts laukā Datums līdz.</span><span class="sxs-lookup"><span data-stu-id="068b1-119">Interest will be calculated from this date to the "To date".</span></span> <span data-ttu-id="068b1-120">Ja jums nav specifiskas vērtības laukā Datums no, tad visi neiegrāmatotie procentu paziņojumi tiks atcelti un procenti tiks pārrēķināti no transakcijas datuma.</span><span class="sxs-lookup"><span data-stu-id="068b1-120">If you do not specific a "From date", then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>  
2. <span data-ttu-id="068b1-121">Ievadiet procentu paziņojuma datumu.</span><span class="sxs-lookup"><span data-stu-id="068b1-121">Enter the date of the interest note.</span></span>
    * <span data-ttu-id="068b1-122">Pieejamas ir trīs grāmatošanas metodes opcijas: Konts — izmantot grāmatošanas metodi, kas ir piešķirta debitora kontam attiecībā uz visiem procentu paziņojumiem.</span><span class="sxs-lookup"><span data-stu-id="068b1-122">There are three posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="068b1-123">Atlasīt — lietojiet grāmatošanas profilu, kas ir atlasīts laukā Grāmatošanas metode.</span><span class="sxs-lookup"><span data-stu-id="068b1-123">Select – Use the posting profile that you select in the Posting profile field.</span></span>   <span data-ttu-id="068b1-124">Transakcija — izmantot katram procentu paziņojumam atsevišķu grāmatošanas metodi transakcijām, par kurām tiek aprēķināti procenti.</span><span class="sxs-lookup"><span data-stu-id="068b1-124">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="068b1-125">Transakcijām, kurām nav piešķirta grāmatošanas metode, tiek izmantota grāmatošanas metode, kura ir norādīta veidlapas Debitoru parametri apgabalā Virsgrāmata un PVN formā.</span><span class="sxs-lookup"><span data-stu-id="068b1-125">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
    * <span data-ttu-id="068b1-126">Ja mainījāt Izmantot grāmatošanas metodi no lauka vērtību uz Atlasīt, atlasiet šeit grāmatošanas metodi.</span><span class="sxs-lookup"><span data-stu-id="068b1-126">Select a posting profile here if you changed "Use posting profile from" to "Select".</span></span>  
3. <span data-ttu-id="068b1-127">Izvērsiet vai sakļaujiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="068b1-127">Expand or collapse the Records to include section.</span></span>
4. <span data-ttu-id="068b1-128">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="068b1-128">Click Filter.</span></span>
5. <span data-ttu-id="068b1-129">Laukā Kritērijs ievadiet klienta ID.</span><span class="sxs-lookup"><span data-stu-id="068b1-129">In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="068b1-130">Piemēram, ievadiet US-001.</span><span class="sxs-lookup"><span data-stu-id="068b1-130">For example, enter 'US-001'..</span></span>
6. <span data-ttu-id="068b1-131">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="068b1-131">Click OK.</span></span>
7. <span data-ttu-id="068b1-132">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="068b1-132">Click OK.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="068b1-133">Drukāt procentu paziņojumus</span><span class="sxs-lookup"><span data-stu-id="068b1-133">Print interest notes</span></span>
1. <span data-ttu-id="068b1-134">Pārejiet uz sadaļu Kredīts un iekasēšana > Procenti > Pārskatīt un apstrādāt procentu paziņojumus.</span><span class="sxs-lookup"><span data-stu-id="068b1-134">Go to Credit and collections > Interest > Review and process interest notes.</span></span>
2. <span data-ttu-id="068b1-135">Laukā Statuss atlasiet Izveidots.</span><span class="sxs-lookup"><span data-stu-id="068b1-135">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="068b1-136">Laukā Drukāts atlasiet Nav drukāts.</span><span class="sxs-lookup"><span data-stu-id="068b1-136">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="068b1-137">Klikšķiniet Drukāt.</span><span class="sxs-lookup"><span data-stu-id="068b1-137">Click Print.</span></span>
5. <span data-ttu-id="068b1-138">Izvērsiet vai sakļaujiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="068b1-138">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="068b1-139">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="068b1-139">Click OK.</span></span>
7. <span data-ttu-id="068b1-140">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="068b1-140">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="068b1-141">Procentu paziņojuma grāmatošana</span><span class="sxs-lookup"><span data-stu-id="068b1-141">Post the interest note</span></span>
1. <span data-ttu-id="068b1-142">Atlasiet procentu paziņojumu, kas ir gatavs grāmatošanai (statuss ir Izveidots).</span><span class="sxs-lookup"><span data-stu-id="068b1-142">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="068b1-143">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="068b1-143">Click Post.</span></span>
3. <span data-ttu-id="068b1-144">Ievadiet procentu paziņojuma grāmatošanas datumu.</span><span class="sxs-lookup"><span data-stu-id="068b1-144">Enter the posting date for the interest note.</span></span>
    * <span data-ttu-id="068b1-145">Lai katram procentu paziņojumam izveidotu Virsgrāmatas transakciju, atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="068b1-145">Select Yes to create a general ledger transaction for each interest note.</span></span>     <span data-ttu-id="068b1-146">Ja neatlasāt vērtību Jā, visi debitora procentu paziņojumu procenti tiek uzkrāti un grāmatoti Virsgrāmatā vienā transakcijā.</span><span class="sxs-lookup"><span data-stu-id="068b1-146">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="068b1-147">Izvērsiet vai sakļaujiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="068b1-147">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="068b1-148">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="068b1-148">Click OK.</span></span>
6. <span data-ttu-id="068b1-149">Laukā Statuss atlasiet Iegrāmatots.</span><span class="sxs-lookup"><span data-stu-id="068b1-149">In the Status field, select 'Posted'.</span></span>


