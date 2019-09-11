---
title: Atgādinājuma vēstuļu apstrāde
description: Šajā tēmā ir parādīts, kā izveidot, izdrukāt un grāmatot atgādinājuma vēstules.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 326d9375670cb4f4990a4f7070bf923a28b2c025
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867659"
---
# <a name="process-collection-letters"></a><span data-ttu-id="31034-103">Atgādinājuma vēstuļu apstrāde</span><span class="sxs-lookup"><span data-stu-id="31034-103">Process collection letters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="31034-104">Šajā tēmā ir parādīts, kā izveidot, izdrukāt un grāmatot atgādinājuma vēstules.</span><span class="sxs-lookup"><span data-stu-id="31034-104">This topic shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="31034-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="31034-105">This task uses the USMF demo company.</span></span>

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="31034-106">Atgādinājuma vēstuļu secības iestatīšana grāmatošanas metodē</span><span class="sxs-lookup"><span data-stu-id="31034-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="31034-107">Ejiet uz **Navigācijas rūts > Moduļi > Kredīts un atgūšana > Iestatīšana >Klientu grāmatošanas profili.**</span><span class="sxs-lookup"><span data-stu-id="31034-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="31034-108">Noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="31034-108">Click **Edit**.</span></span>
3. <span data-ttu-id="31034-109">Atlasiet no nolaižamā saraksta atgādinājuma vēstuļu secību.</span><span class="sxs-lookup"><span data-stu-id="31034-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="31034-110">Ja atgādinājuma vēstules par transakcijām nevēlaties ģenerēt, izmantojot šo grāmatošanas metodi, atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="31034-110">If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
4. <span data-ttu-id="31034-111">Izvērsiet cilni **Tabulas ierobežojumi**, lai mainītu veidu, kādā tiek apstrādātas atgādinājuma vēstules.</span><span class="sxs-lookup"><span data-stu-id="31034-111">Expand the **Table restrictions** tab to change the way that collection letters are processed.</span></span> <span data-ttu-id="31034-112">Ja šajā laukā ir iestatīts **Jā**, atgādinājuma vēstules tiks izveidotas šai grāmatošanas metodei.</span><span class="sxs-lookup"><span data-stu-id="31034-112">If this field is set to **Yes**, then collection letters will be created for this posting profile.</span></span>  

## <a name="create-collection-letters"></a><span data-ttu-id="31034-113">Izveidot atgādinājuma vēstules</span><span class="sxs-lookup"><span data-stu-id="31034-113">Create collection letters</span></span>
1. <span data-ttu-id="31034-114">Ejiet uz **Navigācijas rūts > Moduļi > Kredīts un atgūšana > Atgādinājuma vēstule > Izveidot atgādinājuma vēstules**.</span><span class="sxs-lookup"><span data-stu-id="31034-114">Go to **Navigation pane > Modules > Credit and collections > Collection letter > Create collection letters**.</span></span>
2. <span data-ttu-id="31034-115">Atlasiet transakciju veidus, par ko apkoposit vēstules.</span><span class="sxs-lookup"><span data-stu-id="31034-115">Select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="31034-116">Aprēķinā tiks iekļautas visas šiem tipiem atbilstošās atvērtās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="31034-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="31034-117">Laukā **Atgādinājuma vēstule** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="31034-117">In the **Collection letter** field, select an option.</span></span>
4. <span data-ttu-id="31034-118">Laukā **Atgādinājuma vēstules datums** ievadiet atgādinājuma vēstules datumu.</span><span class="sxs-lookup"><span data-stu-id="31034-118">In the **Collection letter date** field, enter the date of the collection letter.</span></span>
5. <span data-ttu-id="31034-119">Atlasiet grāmatošanas metodi, ja mainījāt **Izmantot grāmatošanas metodi no** uz **Atlasīt**.</span><span class="sxs-lookup"><span data-stu-id="31034-119">Select a posting profile if you changed **Use posting profile from** to **Select**.</span></span> <span data-ttu-id="31034-120">Ir divas grāmatošanas profilu opcijas:</span><span class="sxs-lookup"><span data-stu-id="31034-120">There are two posting profile options:</span></span>   

   - <span data-ttu-id="31034-121">**Konts** — katram procentu paziņojumam lietojiet debitora kontam piešķirto grāmatošanas metodi.</span><span class="sxs-lookup"><span data-stu-id="31034-121">**Account** – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   
   - <span data-ttu-id="31034-122">**Atlasīt** — lietojiet grāmatošanas metodi, kuru atlasījāt laukā **Grāmatošanas metode**.</span><span class="sxs-lookup"><span data-stu-id="31034-122">**Select** – Use the posting profile that you select in the **Posting profile** field.</span></span>  

6. <span data-ttu-id="31034-123">Izvērsiet sadaļu **Iekļaujamie ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="31034-123">Expand the **Records to include** section.</span></span>
7. <span data-ttu-id="31034-124">Atlasiet **Filtrēt**.</span><span class="sxs-lookup"><span data-stu-id="31034-124">Select **Filter**.</span></span>
8. <span data-ttu-id="31034-125">Laukā **Kritērijs** ievadiet debitora ID.</span><span class="sxs-lookup"><span data-stu-id="31034-125">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="31034-126">Piemēram, ievadiet US-001.</span><span class="sxs-lookup"><span data-stu-id="31034-126">For example, enter 'US-001'.</span></span>
9. <span data-ttu-id="31034-127">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="31034-127">Select **OK**.</span></span>
10. <span data-ttu-id="31034-128">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="31034-128">Select **OK**.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="31034-129">Atgādinājuma vēstuļu izdruka</span><span class="sxs-lookup"><span data-stu-id="31034-129">Print collection letters</span></span>
1. <span data-ttu-id="31034-130">Ejiet uz **Navigācijas rūts > Moduļi > Kredīts un atgūšana > Atgādinājuma vēstule > Atgādinājuma vēstuļu izskatīšana un apstrāde**.</span><span class="sxs-lookup"><span data-stu-id="31034-130">Go to **navigation pane > Modules > Credit and collections > Collection letter > Review and process collection letters**.</span></span>
2. <span data-ttu-id="31034-131">Laukā **Statuss** atlasiet **Izveidots**.</span><span class="sxs-lookup"><span data-stu-id="31034-131">In the **Status** field, select **Created**.</span></span>
3. <span data-ttu-id="31034-132">Laukā **Drukāts** atlasiet **Nav drukāts**.</span><span class="sxs-lookup"><span data-stu-id="31034-132">In the **Printed** field, select **Not printed**.</span></span>
4. <span data-ttu-id="31034-133">Atlasiet **Drukāt**.</span><span class="sxs-lookup"><span data-stu-id="31034-133">Select **Print**.</span></span>
5. <span data-ttu-id="31034-134">Atlasiet **Atgādinājuma vēstules piezīme**.</span><span class="sxs-lookup"><span data-stu-id="31034-134">Select **Collection letter note**.</span></span>
6. <span data-ttu-id="31034-135">Sadaļā **Parametri** ievadiet grāmatojumu robeždatumu.</span><span class="sxs-lookup"><span data-stu-id="31034-135">In the **Parameters** section, enter the cutoff date for postings.</span></span>
7. <span data-ttu-id="31034-136">Izvērsiet sadaļu **Iekļaujamie ieraksti** un ievadiet informāciju atgādinājuma vēstules piezīmē.</span><span class="sxs-lookup"><span data-stu-id="31034-136">Expand the **Records to include** section and enter the details of the Collection letter note.</span></span>
8. <span data-ttu-id="31034-137">Atlasiet **Labi**, lai izdrukātu atgādinājuma vēstuli.</span><span class="sxs-lookup"><span data-stu-id="31034-137">Select **OK** to print the collection letter.</span></span>
9. <span data-ttu-id="31034-138">Grāmatojiet atgādinājuma vēstuli.</span><span class="sxs-lookup"><span data-stu-id="31034-138">Post the collection letter.</span></span>

    1. <span data-ttu-id="31034-139">Atlasiet **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="31034-139">Select **Post**.</span></span>
    1. <span data-ttu-id="31034-140">Ievadiet atgādinājuma vēstules grāmatošanas datumu.</span><span class="sxs-lookup"><span data-stu-id="31034-140">Enter the posting date for the collection letter.</span></span>
    1. <span data-ttu-id="31034-141">Izvērsiet sadaļu **Iekļaujamie ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="31034-141">Expand the **Records to include** section.</span></span>
    1. <span data-ttu-id="31034-142">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="31034-142">Select **OK**.</span></span>
    1. <span data-ttu-id="31034-143">Laukā **Statuss** atlasiet **Iegrāmatots**.</span><span class="sxs-lookup"><span data-stu-id="31034-143">In the **Status** field, select **Posted**.</span></span>
    1. <span data-ttu-id="31034-144">Laukā **Drukāts** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="31034-144">In the **Printed** field, select an option.</span></span>

## <a name="control-collection-letters-at-the-customer-level"></a><span data-ttu-id="31034-145">Atgādinājuma vēstuļu pārvaldība debitora līmenī</span><span class="sxs-lookup"><span data-stu-id="31034-145">Control collection letters at the customer level</span></span>
<span data-ttu-id="31034-146">Varat arī iestatīt atgādinājuma vēstules debitora līmenī, un tādējādi tiks izsekots katras transakcijas atgādinājuma vēstules kods, bet atgādinājuma vēstuļu apstrādes pamatā būs viens atgādinājuma vēstuļu līmenis, kas saglabāts par debitoru.</span><span class="sxs-lookup"><span data-stu-id="31034-146">You can also set up collection letters at the customer level so that the collection letter code for each transaction is tracked, but the collection letter processing will be based on a single collection letter level that is stored for the customer.</span></span> <span data-ttu-id="31034-147">Viena atgādinājuma vēstule ietvers visas debitora nokavētās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="31034-147">The single collection letter will contain all transactions that are overdue for the customer.</span></span> <span data-ttu-id="31034-148">Tā kā pagarinājuma dienas tagad tiek izsekotas debitora līmenī, nākamā atgādinājuma vēstule netiek nosūtīta, līdz nav pagājis nākamās atgādinājuma vēstules nosūtīšanai noteiktais pagarinājuma dienu skaits, pat ja transakcijas tiek nokavētas pēc pēdējās atgādinājuma vēstules nosūtīšanas.</span><span class="sxs-lookup"><span data-stu-id="31034-148">Because the grace days are now tracked on the customer level, the next collection letter will not be sent until the number of grace days has passed for the next collection letter in the sequence, even though transactions become overdue after the last collection letter was sent.</span></span> <span data-ttu-id="31034-149">Šī iespēja samazina katram klientam nosūtāmo atgādinājuma vēstuļu skaitu.</span><span class="sxs-lookup"><span data-stu-id="31034-149">This option reduces the number of collection letters you will send per customer.</span></span> 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a><span data-ttu-id="31034-150">Debitora iestatīšana atgādinājuma vēstuļu pārvaldībai debitora līmenī</span><span class="sxs-lookup"><span data-stu-id="31034-150">Set up the customer to control collection letters at the customer level</span></span>
1.  <span data-ttu-id="31034-151">Ejiet uz **Navigācijas rūts > Moduļi > Kredīts un atgūšana > Iestatīšana > Kreditoru parametri** un atlasiet cilni **Atgūšana**.</span><span class="sxs-lookup"><span data-stu-id="31034-151">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters** and select the **Collections** tab.</span></span> 
2.  <span data-ttu-id="31034-152">Mainiet parametra **Izveidot atgādinājuma vēstuli katram** vērtību uz **Debitoram**.</span><span class="sxs-lookup"><span data-stu-id="31034-152">Change the value of **Create collection letter per** to **Customer**.</span></span> 
3.  <span data-ttu-id="31034-153">Ejiet uz **Navigācijas rūts > Moduļi > Kredīts un atgūšana > Atgādinājuma vēstule > Atgādinājuma vēstuļu izskatīšana un apstrāde**.</span><span class="sxs-lookup"><span data-stu-id="31034-153">Go to **navigation pane > Modules > Credit and collections > Collection letter > Review and process collection letters**.</span></span> <span data-ttu-id="31034-154">Katram debitoram tiks izveidota tikai viena atgādinājuma vēstule ar visām nokavētajām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="31034-154">Only one collection letter will be generated for a customer with all the overdue transactions.</span></span>

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a><span data-ttu-id="31034-155">Maksājumu un kredītrēķinu ignorēšana, aprēķinot atgādinājuma vēstules kodu</span><span class="sxs-lookup"><span data-stu-id="31034-155">Ignore payments and credit memos when calculating the collection letter code</span></span>
<span data-ttu-id="31034-156">Ja maksājumus un kredītrēķinus iekļaujat transakcijās, kas tiks iekļautas atgādinājuma vēstulēs, var būt tādi maksājumi vai kredītrēķini, kas aktivizēs atgādinājuma vēstules izveidi.</span><span class="sxs-lookup"><span data-stu-id="31034-156">If you include payments and credit memos in the transactions that will be included in the collection letters, you may have payments or credit memos that will trigger a collection letter.</span></span> <span data-ttu-id="31034-157">Izmainot parametra **Ignorēt maksājumus un kredītrēķinus, aprēķinot atgādinājuma vēstules kodu** vērtību, varat pārvaldīt, kā maksājumi un kredītrēķini ietekmē atgādinājuma vēstules kodu.</span><span class="sxs-lookup"><span data-stu-id="31034-157">You can control how payments and credit memos control the collection letter code by changing the value of the **Ignore payments and credit memos when calculating the collection letter code** parameter.</span></span> 

<span data-ttu-id="31034-158">Lai ignorētu maksājumus un kredītrēķinus, aprēķinot atgādinājuma vēstules kodu, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="31034-158">To ignore payments and credit memos when calculating the collection letter code, do the following.</span></span>

1. <span data-ttu-id="31034-159">Ejiet uz **Navigācijas rūts > Moduļi > Kredīts un atgūšana > Iestatīšana > Kreditoru parametri** un noklikšķiniet uz cilnes **Atgūšana**.</span><span class="sxs-lookup"><span data-stu-id="31034-159">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2. <span data-ttu-id="31034-160">Mainiet parametra **Ignorēt maksājumus un kredītrēķinus, aprēķinot atgādinājuma vēstules kodu vērtību** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="31034-160">Change the value of **Ignore payments and credit memos when calculating the collection letter code** to **Yes**.</span></span>
