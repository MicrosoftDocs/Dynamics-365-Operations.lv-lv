--- 
title: "Atgādinājuma vēstuļu apstrāde"
description: "Šajā procedūrā parādīts, kā izveidot, izdrukāt un grāmatot atgādinājuma vēstules."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/04/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.translationtype: HT
ms.sourcegitcommit: 18eaadf417ce6d0aacf0b13b3e4f857e06031e66
ms.openlocfilehash: 8a3f74d2891c050294e089eae14ba2386449d7c9
ms.contentlocale: lv-lv
ms.lasthandoff: 01/22/2019

---
# <a name="process-collection-letters"></a><span data-ttu-id="5f78a-103">Atgādinājuma vēstuļu apstrāde</span><span class="sxs-lookup"><span data-stu-id="5f78a-103">Process collection letters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5f78a-104">Šajā procedūrā parādīts, kā izveidot, izdrukāt un grāmatot atgādinājuma vēstules.</span><span class="sxs-lookup"><span data-stu-id="5f78a-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="5f78a-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="5f78a-105">This task uses the USMF demo company.</span></span>

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="5f78a-106">Atgādinājuma vēstuļu secības iestatīšana grāmatošanas metodē</span><span class="sxs-lookup"><span data-stu-id="5f78a-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="5f78a-107">Pārejiet uz sadaļu **Kredīts un iekasēšana > Iestatījumi > Debitoru grāmatošanas metodes**.</span><span class="sxs-lookup"><span data-stu-id="5f78a-107">Go to **Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="5f78a-108">Noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="5f78a-108">Click **Edit**.</span></span>
3. <span data-ttu-id="5f78a-109">Atlasiet no nolaižamā saraksta atgādinājuma vēstuļu secību.</span><span class="sxs-lookup"><span data-stu-id="5f78a-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="5f78a-110">Ja atgādinājuma vēstules par transakcijām nevēlaties ģenerēt, izmantojot šo grāmatošanas metodi, atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="5f78a-110">If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
4. <span data-ttu-id="5f78a-111">Izvērsiet tabulas ierobežojumu cilni, lai mainītu veidu, kā tiek apstrādātas atgādinājuma vēstules.</span><span class="sxs-lookup"><span data-stu-id="5f78a-111">Expand the table restriction tab to change the way that collection letters are processed.</span></span> <span data-ttu-id="5f78a-112">Ja šajā laukā ir iestatīts **Jā**, atgādinājuma vēstules tiks izveidotas šai grāmatošanas metodei.</span><span class="sxs-lookup"><span data-stu-id="5f78a-112">If this field is set to **Yes**, then collection letters will be created for this posting profile.</span></span>  

## <a name="create-collection-letters"></a><span data-ttu-id="5f78a-113">Izveidot atgādinājuma vēstules</span><span class="sxs-lookup"><span data-stu-id="5f78a-113">Create collection letters</span></span>
1. <span data-ttu-id="5f78a-114">Pārejiet uz sadaļu **Kredīts un iekasēšana > Atgādinājuma vēstule > Izveidot atgādinājuma vēstules**.</span><span class="sxs-lookup"><span data-stu-id="5f78a-114">Go to **Credit and collections > Collection letter > Create collection letters**.</span></span>
2. <span data-ttu-id="5f78a-115">Atlasiet transakciju veidus, par ko apkoposit vēstules.</span><span class="sxs-lookup"><span data-stu-id="5f78a-115">Select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="5f78a-116">Aprēķinā tiks iekļautas visas šiem tipiem atbilstošās atvērtās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="5f78a-116">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="5f78a-117">Laukā **Atgādinājuma vēstule** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="5f78a-117">In the **Collection letter** field, select an option.</span></span>
3. <span data-ttu-id="5f78a-118">Ievadiet atgādinājuma vēstules datumu.</span><span class="sxs-lookup"><span data-stu-id="5f78a-118">Enter the date of the collection letter.</span></span>
4. <span data-ttu-id="5f78a-119">Atlasiet grāmatošanas metodi, ja mainījāt **Izmantot grāmatošanas metodi no** uz **Atlasīt**.</span><span class="sxs-lookup"><span data-stu-id="5f78a-119">Select a posting profile if you changed **Use posting profile from** to **Select**.</span></span> <span data-ttu-id="5f78a-120">Ir divas grāmatošanas profilu opcijas:</span><span class="sxs-lookup"><span data-stu-id="5f78a-120">There are two posting profile options:</span></span>   
   - <span data-ttu-id="5f78a-121">**Konts** — katram procentu paziņojumam lietojiet debitora kontam piešķirto grāmatošanas metodi.</span><span class="sxs-lookup"><span data-stu-id="5f78a-121">**Account** – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   
   - <span data-ttu-id="5f78a-122">**Atlasīt** — lietojiet grāmatošanas metodi, kuru atlasījāt laukā **Grāmatošanas metode**.</span><span class="sxs-lookup"><span data-stu-id="5f78a-122">**Select** – Use the posting profile that you select in the **Posting profile** field.</span></span>  
5. <span data-ttu-id="5f78a-123">Izvērsiet sadaļu **Iekļaujamie ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="5f78a-123">Expand the **Records to include** section.</span></span>
6. <span data-ttu-id="5f78a-124">Noklikšķiniet uz **Filtrēt**.</span><span class="sxs-lookup"><span data-stu-id="5f78a-124">Click **Filter**.</span></span>
7. <span data-ttu-id="5f78a-125">Laukā **Kritērijs** ievadiet debitora ID.</span><span class="sxs-lookup"><span data-stu-id="5f78a-125">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="5f78a-126">Piemēram, ievadiet US-001.</span><span class="sxs-lookup"><span data-stu-id="5f78a-126">For example, enter 'US-001'.</span></span>
8. <span data-ttu-id="5f78a-127">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5f78a-127">Click **OK**.</span></span>
9. <span data-ttu-id="5f78a-128">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5f78a-128">Click **OK**.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="5f78a-129">Atgādinājuma vēstuļu izdruka</span><span class="sxs-lookup"><span data-stu-id="5f78a-129">Print collection letters</span></span>
1. <span data-ttu-id="5f78a-130">Pārejiet uz sadaļu **Kredīts un iekasēšana > Atgādinājuma vēstule > Pārskatīt un apstrādāt atgādinājuma vēstules**.</span><span class="sxs-lookup"><span data-stu-id="5f78a-130">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span>
2. <span data-ttu-id="5f78a-131">Laukā **Statuss** atlasiet **Izveidots**.</span><span class="sxs-lookup"><span data-stu-id="5f78a-131">In the **Status** field, select **Created**.</span></span>
3. <span data-ttu-id="5f78a-132">Laukā **Drukāts** atlasiet **Nav drukāts**.</span><span class="sxs-lookup"><span data-stu-id="5f78a-132">In the **Printed** field, select **Not printed**.</span></span>
4. <span data-ttu-id="5f78a-133">Klikšķiniet **Drukāt**.</span><span class="sxs-lookup"><span data-stu-id="5f78a-133">Click **Print**.</span></span>
5. <span data-ttu-id="5f78a-134">Noklikšķiniet uz **Atgādinājuma vēstules piezīmes**.</span><span class="sxs-lookup"><span data-stu-id="5f78a-134">Click **Collection letter note**.</span></span>
6. <span data-ttu-id="5f78a-135">Izvērsiet sadaļu **Iekļaujamie ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="5f78a-135">Expand the **Records to include** section.</span></span>
7. <span data-ttu-id="5f78a-136">Ievadiet grāmatošanas robeždatumu.</span><span class="sxs-lookup"><span data-stu-id="5f78a-136">Enter the cutoff date for postings.</span></span>
8. <span data-ttu-id="5f78a-137">Noklikšķiniet uz **Labi**, lai drukātu atgādinājuma vēstuli.</span><span class="sxs-lookup"><span data-stu-id="5f78a-137">Click **OK** to print the collection letter.</span></span>
9. <span data-ttu-id="5f78a-138">Grāmatojiet atgādinājuma vēstuli.</span><span class="sxs-lookup"><span data-stu-id="5f78a-138">Post the collection letter.</span></span>
   1. <span data-ttu-id="5f78a-139">Noklikšķiniet uz **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="5f78a-139">Click **Post**.</span></span>
   2. <span data-ttu-id="5f78a-140">Ievadiet atgādinājuma vēstules grāmatošanas datumu.</span><span class="sxs-lookup"><span data-stu-id="5f78a-140">Enter the posting date for the collection letter.</span></span>
   3. <span data-ttu-id="5f78a-141">Izvērsiet sadaļu **Iekļaujamie ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="5f78a-141">Expand the **Records to include** section.</span></span>
   4. <span data-ttu-id="5f78a-142">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5f78a-142">Click **OK**.</span></span>
   5. <span data-ttu-id="5f78a-143">Laukā **Statuss** atlasiet **Iegrāmatots**.</span><span class="sxs-lookup"><span data-stu-id="5f78a-143">In the **Status** field, select **Posted**.</span></span>
   6. <span data-ttu-id="5f78a-144">Laukā **Drukāts** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="5f78a-144">In the **Printed** field, select an option.</span></span>

## <a name="control-collection-letters-at-the-customer-level"></a><span data-ttu-id="5f78a-145">Atgādinājuma vēstuļu pārvaldība debitora līmenī</span><span class="sxs-lookup"><span data-stu-id="5f78a-145">Control collection letters at the customer level</span></span>
<span data-ttu-id="5f78a-146">Varat arī iestatīt atgādinājuma vēstules debitora līmenī, un tādējādi tiks izsekots katras transakcijas atgādinājuma vēstules kods, bet atgādinājuma vēstuļu apstrādes pamatā būs viens atgādinājuma vēstuļu līmenis, kas saglabāts par debitoru.</span><span class="sxs-lookup"><span data-stu-id="5f78a-146">You can also set up collection letters at the customer level so that the collection letter code for each transaction is tracked, but the collection letter processing will be based on a single collection letter level that is stored for the customer.</span></span> <span data-ttu-id="5f78a-147">Viena atgādinājuma vēstule ietvers visas debitora nokavētās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="5f78a-147">The single collection letter will contain all transactions that are overdue for the customer.</span></span> <span data-ttu-id="5f78a-148">Tā kā pagarinājuma dienas tagad tiek izsekotas debitora līmenī, nākamā atgādinājuma vēstule netiek nosūtīta, līdz nav pagājis nākamās atgādinājuma vēstules nosūtīšanai noteiktais pagarinājuma dienu skaits, pat ja transakcijas tiek nokavētas pēc pēdējās atgādinājuma vēstules nosūtīšanas.</span><span class="sxs-lookup"><span data-stu-id="5f78a-148">Because the grace days are now tracked on the customer level, the next collection letter will not be sent until the number of grace days has passed for the next collection letter in the sequence, even though transactions become overdue after the last collection letter was sent.</span></span> <span data-ttu-id="5f78a-149">Šī iespēja samazina katram klientam nosūtāmo atgādinājuma vēstuļu skaitu.</span><span class="sxs-lookup"><span data-stu-id="5f78a-149">This option reduces the number of collection letters you will send per customer.</span></span> 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a><span data-ttu-id="5f78a-150">Debitora iestatīšana atgādinājuma vēstuļu pārvaldībai debitora līmenī</span><span class="sxs-lookup"><span data-stu-id="5f78a-150">Set up the customer to control collection letters at the customer level</span></span>
1.  <span data-ttu-id="5f78a-151">Dodieties uz sadaļu **Kredīts un iekasēšana > Iestatījumi > Debitoru parādu parametri** un noklikšķiniet uz cilnes **Iekasēšana**.</span><span class="sxs-lookup"><span data-stu-id="5f78a-151">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2.  <span data-ttu-id="5f78a-152">Mainiet parametra **Izveidot atgādinājuma vēstuli katram** vērtību uz **Debitoram**.</span><span class="sxs-lookup"><span data-stu-id="5f78a-152">Change the value of **Create collection letter per** to **Customer**.</span></span> 
3.  <span data-ttu-id="5f78a-153">Pārejiet uz sadaļu **Kredīts un iekasēšana > Atgādinājuma vēstule > Pārskatīt un apstrādāt atgādinājuma vēstules**.</span><span class="sxs-lookup"><span data-stu-id="5f78a-153">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span> <span data-ttu-id="5f78a-154">Katram debitoram tiks izveidota tikai viena atgādinājuma vēstule ar visām nokavētajām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="5f78a-154">Only one collection letter will be generated for a customer with all the overdue transactions.</span></span>

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a><span data-ttu-id="5f78a-155">Maksājumu un kredītrēķinu ignorēšana, aprēķinot atgādinājuma vēstules kodu</span><span class="sxs-lookup"><span data-stu-id="5f78a-155">Ignore payments and credit memos when calculating the collection letter code</span></span>
<span data-ttu-id="5f78a-156">Ja maksājumus un kredītrēķinus iekļaujat transakcijās, kas tiks iekļautas atgādinājuma vēstulēs, var būt tādi maksājumi vai kredītrēķini, kas aktivizēs atgādinājuma vēstules izveidi.</span><span class="sxs-lookup"><span data-stu-id="5f78a-156">If you include payments and credit memos in the transactions that will be included in the collection letters, you may have payments or credit memos that will trigger a collection letter.</span></span> <span data-ttu-id="5f78a-157">Izmainot parametra **Ignorēt maksājumus un kredītrēķinus, aprēķinot atgādinājuma vēstules kodu** vērtību, varat pārvaldīt, kā maksājumi un kredītrēķini ietekmē atgādinājuma vēstules kodu.</span><span class="sxs-lookup"><span data-stu-id="5f78a-157">You can control how payments and credit memos control the collection letter code by changing the value of the **Ignore payments and credit memos when calculating the collection letter code** parameter.</span></span> 

<span data-ttu-id="5f78a-158">Lai ignorētu maksājumus un kredītrēķinus, aprēķinot atgādinājuma vēstules kodu, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="5f78a-158">To ignore payments and credit memos when calculating the collection letter code, do the following.</span></span>
1. <span data-ttu-id="5f78a-159">Dodieties uz sadaļu **Kredīts un iekasēšana > Iestatījumi > Debitoru parādu parametri** un noklikšķiniet uz cilnes **Iekasēšana**.</span><span class="sxs-lookup"><span data-stu-id="5f78a-159">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2. <span data-ttu-id="5f78a-160">Mainiet parametra **Ignorēt maksājumus un kredītrēķinus, aprēķinot atgādinājuma vēstules kodu vērtību** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="5f78a-160">Change the value of **Ignore payments and credit memos when calculating the collection letter code** to **Yes**.</span></span>

