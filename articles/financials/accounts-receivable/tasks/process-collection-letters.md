--- 
title: "Atgādinājuma vēstuļu apstrāde"
description: "Šajā procedūrā parādīts, kā izveidot, izdrukāt un grāmatot atgādinājuma vēstules."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dc837ea6513992a5f94e48baa366e279df297866
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="process-collection-letters"></a><span data-ttu-id="9a180-103">Atgādinājuma vēstuļu apstrāde</span><span class="sxs-lookup"><span data-stu-id="9a180-103">Process collection letters</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9a180-104">Šajā procedūrā parādīts, kā izveidot, izdrukāt un grāmatot atgādinājuma vēstules.</span><span class="sxs-lookup"><span data-stu-id="9a180-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="9a180-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="9a180-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="9a180-106">Atgādinājuma vēstuļu secības iestatīšana grāmatošanas metodē</span><span class="sxs-lookup"><span data-stu-id="9a180-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="9a180-107">Pārejiet uz sadaļu Kredīts un iekasēšana > Iestatījumi > Debitoru grāmatošanas metodes.</span><span class="sxs-lookup"><span data-stu-id="9a180-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="9a180-108">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="9a180-108">Click Edit.</span></span>
    * <span data-ttu-id="9a180-109">Atlasiet no nolaižamā saraksta atgādinājuma vēstuļu secību.</span><span class="sxs-lookup"><span data-stu-id="9a180-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="9a180-110">Ja atgādinājuma vēstules nevēlaties ģenerēt darbībām, izmantojot šo grāmatošanas metodi, atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="9a180-110">If you do not want generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="9a180-111">Tabulas ierobežojumu cilnē varat mainīt veidu, kā tiek apstrādātas atgādinājuma vēstules.</span><span class="sxs-lookup"><span data-stu-id="9a180-111">The table restriction tab allows you to change the way that collection letters are processed.</span></span> <span data-ttu-id="9a180-112">Ja šajā laukā ir iestatīts Jā, atgādinājuma vēstules tiks izveidotas šai grāmatošanas metodei.</span><span class="sxs-lookup"><span data-stu-id="9a180-112">If this field is set to Yes, then collection letters will be created for this posting profile.</span></span>  
3. <span data-ttu-id="9a180-113">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9a180-113">Close the page.</span></span>

## <a name="create-collection-letters"></a><span data-ttu-id="9a180-114">Izveidot atgādinājuma vēstules</span><span class="sxs-lookup"><span data-stu-id="9a180-114">Create collection letters</span></span>
1. <span data-ttu-id="9a180-115">Pārejiet uz sadaļu Kredīts un iekasēšana > Atgādinājuma vēstule > Izveidot atgādinājuma vēstules.</span><span class="sxs-lookup"><span data-stu-id="9a180-115">Go to Credit and collections > Collection letter > Create collection letters.</span></span>
    * <span data-ttu-id="9a180-116">Atlasiet darbību veidus, kam apkoposit vēstules.</span><span class="sxs-lookup"><span data-stu-id="9a180-116">You must select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="9a180-117">Aprēķinā tiks iekļautas visas šiem tipiem atbilstošās atvērtās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="9a180-117">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="9a180-118">Laukā Atgādinājuma vēstule, atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="9a180-118">In the Collection letter field, select an option.</span></span>
3. <span data-ttu-id="9a180-119">Ievadiet atgādinājuma vēstules datumu.</span><span class="sxs-lookup"><span data-stu-id="9a180-119">Enter the date of the collection letter.</span></span>
    * <span data-ttu-id="9a180-120">Pieejamas ir divas grāmatošanas metodes opcijas: Konts — izmantot grāmatošanas metodi, kas ir piešķirta debitora kontam attiecībā uz visiem procentu paziņojumiem.</span><span class="sxs-lookup"><span data-stu-id="9a180-120">There are two posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="9a180-121">Atlasīt — lietojiet grāmatošanas profilu, kas ir atlasīts laukā Grāmatošanas metode.</span><span class="sxs-lookup"><span data-stu-id="9a180-121">Select – Use the posting profile that you select in the Posting profile field.</span></span>  
    * <span data-ttu-id="9a180-122">Atlasiet grāmatošanas metodi, ja mainījāt “Izmantojiet grāmatošanas metodi no” uz “Atlasīt”.</span><span class="sxs-lookup"><span data-stu-id="9a180-122">Select a posting profile if you changed "Use posting profile from" to "Select".</span></span>  
4. <span data-ttu-id="9a180-123">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="9a180-123">Expand the Records to include section.</span></span>
5. <span data-ttu-id="9a180-124">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="9a180-124">Click Filter.</span></span>
6. <span data-ttu-id="9a180-125">Laukā Kritēriji ievadiet Debitora ID.</span><span class="sxs-lookup"><span data-stu-id="9a180-125">In the Criteria field, In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="9a180-126">Piemēram, ievadiet US-001.</span><span class="sxs-lookup"><span data-stu-id="9a180-126">For example, enter 'US-001'..</span></span>
7. <span data-ttu-id="9a180-127">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9a180-127">Click OK.</span></span>
8. <span data-ttu-id="9a180-128">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9a180-128">Click OK.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="9a180-129">Atgādinājuma vēstuļu izdruka</span><span class="sxs-lookup"><span data-stu-id="9a180-129">Print collection letters</span></span>
1. <span data-ttu-id="9a180-130">Pārejiet uz sadaļu Kredīts un iekasēšana > Atgādinājuma vēstule > Pārskatīt un apstrādāt atgādinājuma vēstules.</span><span class="sxs-lookup"><span data-stu-id="9a180-130">Go to Credit and collections > Collection letter > Review and process collection letters.</span></span>
2. <span data-ttu-id="9a180-131">Laukā Statuss atlasiet Izveidots.</span><span class="sxs-lookup"><span data-stu-id="9a180-131">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="9a180-132">Laukā Drukāts atlasiet Nav drukāts.</span><span class="sxs-lookup"><span data-stu-id="9a180-132">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="9a180-133">Klikšķiniet Drukāt.</span><span class="sxs-lookup"><span data-stu-id="9a180-133">Click Print.</span></span>
5. <span data-ttu-id="9a180-134">Noklikšķiniet uz atgādinājuma vēstules piezīmes.</span><span class="sxs-lookup"><span data-stu-id="9a180-134">Click Collection letter note.</span></span>
6. <span data-ttu-id="9a180-135">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="9a180-135">Expand the Records to include section.</span></span>
7. <span data-ttu-id="9a180-136">Grāmatošanas robeždatuma ievadīšana</span><span class="sxs-lookup"><span data-stu-id="9a180-136">Enter the cutoff date for postings</span></span>
8. <span data-ttu-id="9a180-137">Noklikšķiniet uz Labi, lai drukātu atgādinājuma vēstuli.</span><span class="sxs-lookup"><span data-stu-id="9a180-137">Click OK to print the collection letter.</span></span>

## <a name="post-the-collection-letter"></a><span data-ttu-id="9a180-138">Atgādinājuma vēstules grāmatošana</span><span class="sxs-lookup"><span data-stu-id="9a180-138">Post the collection letter</span></span>
1. <span data-ttu-id="9a180-139">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="9a180-139">Click Post.</span></span>
2. <span data-ttu-id="9a180-140">Ievadiet atgādinājuma vēstules grāmatošanas datumu.</span><span class="sxs-lookup"><span data-stu-id="9a180-140">Enter the posting date for the collection letter.</span></span>
3. <span data-ttu-id="9a180-141">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="9a180-141">Expand the Records to include section.</span></span>
4. <span data-ttu-id="9a180-142">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9a180-142">Click OK.</span></span>
5. <span data-ttu-id="9a180-143">Laukā Statuss atlasiet Iegrāmatots.</span><span class="sxs-lookup"><span data-stu-id="9a180-143">In the Status field, select 'Posted'.</span></span>
6. <span data-ttu-id="9a180-144">Laukā Drukāts atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="9a180-144">In the Printed field, select an option.</span></span>


