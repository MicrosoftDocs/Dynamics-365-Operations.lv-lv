---
title: "Numuru sērijas"
description: "Numuru sērijas tiek izmantotas, lai ģenerētu lasāmus, unikālus identifikatorus pamatdatu ierakstiem un transakciju ierakstiem, kam ir nepieciešami identifikatori."
author: MargoC
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 63bf043124797b328116fd7951913eaeda6ff97b
ms.openlocfilehash: 8e3899e1ad5f4be754687c0e2d59348e7a773fd8
ms.contentlocale: lv-lv
ms.lasthandoff: 01/12/2018

---

# <a name="number-sequences"></a><span data-ttu-id="fe81f-103">Numuru sērijas</span><span class="sxs-lookup"><span data-stu-id="fe81f-103">Number sequences</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="fe81f-104">Numuru sērijas tiek izmantotas, lai ģenerētu lasāmus, unikālus identifikatorus pamatdatu ierakstiem un transakciju ierakstiem, kam ir nepieciešami identifikatori.</span><span class="sxs-lookup"><span data-stu-id="fe81f-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="fe81f-105">Pamatdatu ieraksts vai darījuma ieraksts, kam nepieciešams identifikators, tiek saukts par *atsauci*.</span><span class="sxs-lookup"><span data-stu-id="fe81f-105">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span>

<span data-ttu-id="fe81f-106">Pirms atsaucei varat izveidot jaunus ierakstus, ir jāiestata numuru sērija un tā jāsaista ar atsauci.</span><span class="sxs-lookup"><span data-stu-id="fe81f-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="fe81f-107">Numuru sēriju iestatīšanai ieteicams izmantot lapas sadaļā **Organizācijas administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="fe81f-107">We recommend that you use the pages in **Organization administration** to set up number sequences.</span></span> <span data-ttu-id="fe81f-108">Ja ir nepieciešami modelim raksturīgi iestatījumi, varat kādā modulī izmantot parametru lapu, lai šajā modulī esošajām atsaucēm norādītu numuru sērijas.</span><span class="sxs-lookup"><span data-stu-id="fe81f-108">If module-specific settings are required, you can use the parameters page in a module to specify number sequences for the references in that module.</span></span> <span data-ttu-id="fe81f-109">Piemēram, sadaļā **Debitori** un **Debitori** varat iestatīt numuru sēriju grupas, lai konkrētas numuru sērijas piešķirtu konkrētiem debitoriem vai kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="fe81f-109">For example, in **Accounts receivable** and **Accounts payable**, you can set up number sequence groups to allocate specific number sequences to specific customers or vendors.</span></span> 

<span data-ttu-id="fe81f-110">Iestatot numuru sēriju, ir jānorāda tvērums, kas nosaka, kura organizācija šo numuru sēriju izmanto.</span><span class="sxs-lookup"><span data-stu-id="fe81f-110">When you set up a number sequence, you must specify a scope, which defines which organization uses the number sequence.</span></span> <span data-ttu-id="fe81f-111">Tvērums var būt **Koplietots**, **Uzņēmums**, **Juridiska persona** vai **Pārvaldības struktūrvienība**.</span><span class="sxs-lookup"><span data-stu-id="fe81f-111">The scope can be **Shared**, **Company**, **Legal entity**, or **Operating unit**.</span></span> <span data-ttu-id="fe81f-112">Tvērumus **Juridiskā persona** un **Uzņēmums** var kombinēt ar iestatījumu **Finanšu kalendāra periods**, lai izveidotu vēl specifiskākas numuru sērijas.</span><span class="sxs-lookup"><span data-stu-id="fe81f-112">**Legal entity** and **Company** scopes can be combined with **Fiscal calendar period** to create even more specific number sequences.</span></span> 

<span data-ttu-id="fe81f-113">Numuru sēriju formāti sastāv no segmentiem.</span><span class="sxs-lookup"><span data-stu-id="fe81f-113">Number sequence formats consist of segments.</span></span> <span data-ttu-id="fe81f-114">Numuru sērijas, kuru tvērums nav **Koplietots**, var ietvert tvērumam atbilstošus segmentus.</span><span class="sxs-lookup"><span data-stu-id="fe81f-114">Number sequences with a scope other than **Shared** can contain segments that correspond to the scope.</span></span> <span data-ttu-id="fe81f-115">Piemēram, numuru sērija ar tvērumu **Juridiska persona** var ietvert juridiskas personas segmentu.</span><span class="sxs-lookup"><span data-stu-id="fe81f-115">For example, a number sequence with a scope of **Legal entity** can contain a legal entity segment.</span></span> <span data-ttu-id="fe81f-116">Ja numuru sērijas formātā ietilpst tvēruma segments, konkrēta ieraksta tvērumu varat identificēt, skatoties uz tā numuru.</span><span class="sxs-lookup"><span data-stu-id="fe81f-116">By including a scope segment in the number sequence format, you can identify the scope of a particular record by looking at its number.</span></span> 

<span data-ttu-id="fe81f-117">Turklāt segmentiem, kas atbilst tvērumiem, numuru sērijas formāti var ietvert segmentus **Konstante** un **Burti un cipari**.</span><span class="sxs-lookup"><span data-stu-id="fe81f-117">In addition to segments that correspond to scopes, number sequence formats can contain **Constant** and **Alphanumeric segments**.</span></span> <span data-ttu-id="fe81f-118">Segments **Konstante** ietver nemainīgu burtu, skaitļu vai simbolu kopu.</span><span class="sxs-lookup"><span data-stu-id="fe81f-118">A **Constant** segment contains a set of letters, numbers, or symbols that does not change.</span></span> <span data-ttu-id="fe81f-119">Segments **Burti un cipari** ietver burtu vai ciparu kopu, kas tiek palielināta katru reizi, kad tiek izmantots numurs.</span><span class="sxs-lookup"><span data-stu-id="fe81f-119">An **Alphanumeric** segment contains a set of letters or numbers that increment every time that a number is used.</span></span> <span data-ttu-id="fe81f-120">Izmantojiet restītes simbolu (\#), lai apzīmētu pieaugošus numurus, un simbolu &, lai apzīmētu pieaugošus burtus.</span><span class="sxs-lookup"><span data-stu-id="fe81f-120">Use a number sign (\#) to represent incrementing numbers and an ampersand (&) to represent incrementing letters.</span></span> <span data-ttu-id="fe81f-121">Piemēram, izmantojot formātu \#\#\#\#\#\_2017, tiek izveidota sērija 00001\_2017, 00002\_2017 utt.</span><span class="sxs-lookup"><span data-stu-id="fe81f-121">For example, the format \#\#\#\#\#\_2017 creates the sequence 00001\_2017, 00002\_2017, and so on.</span></span>

<a name="number-sequence-examples"></a><span data-ttu-id="fe81f-122">Numuru sēriju piemēri</span><span class="sxs-lookup"><span data-stu-id="fe81f-122">Number sequence examples</span></span>
------------------------

<span data-ttu-id="fe81f-123">Tālāk sniegtajos piemēros ir parādīts, kā izmantot segmentus, lai izveidotu numuru sēriju formātus.</span><span class="sxs-lookup"><span data-stu-id="fe81f-123">The following examples show how to use segments to create number sequence formats.</span></span> <span data-ttu-id="fe81f-124">Šajos piemēros ir īpaši parādītas tvēruma segmentu izmantošanas ietekmes.</span><span class="sxs-lookup"><span data-stu-id="fe81f-124">In particular, the examples demonstrate the effects of using scope segments.</span></span>

### <a name="expense-report-numbers"></a><span data-ttu-id="fe81f-125">Izdevumu pārskatu numuri</span><span class="sxs-lookup"><span data-stu-id="fe81f-125">Expense report numbers</span></span>

<span data-ttu-id="fe81f-126">Nākamajā piemērā izdevumu pārskatu numuri tiek iestatīti juridiskajai personai ar nosaukumu **CS**.</span><span class="sxs-lookup"><span data-stu-id="fe81f-126">In the following example, expense report numbers are set up for the legal entity that is titled **CS**.</span></span> 

- <span data-ttu-id="fe81f-127">**Joma:** Ceļošana un izdevumi</span><span class="sxs-lookup"><span data-stu-id="fe81f-127">**Area:** Travel and expense</span></span> 
- <span data-ttu-id="fe81f-128">**Atsauce:** Izdevumu pārskata numurs</span><span class="sxs-lookup"><span data-stu-id="fe81f-128">**Reference:** Expense report number</span></span> 
- <span data-ttu-id="fe81f-129">**Tvērums:** Juridiskā persona</span><span class="sxs-lookup"><span data-stu-id="fe81f-129">**Scope:** Legal entity</span></span> 
- <span data-ttu-id="fe81f-130">**Juridiskā persona:** CS</span><span class="sxs-lookup"><span data-stu-id="fe81f-130">**Legal entity:** CS</span></span>

| <span data-ttu-id="fe81f-131">Segmenti</span><span class="sxs-lookup"><span data-stu-id="fe81f-131">Segments</span></span>  | <span data-ttu-id="fe81f-132">Segmenta tips</span><span class="sxs-lookup"><span data-stu-id="fe81f-132">Segment type</span></span> | <span data-ttu-id="fe81f-133">Vērtība</span><span class="sxs-lookup"><span data-stu-id="fe81f-133">Value</span></span>     |
|-----------|--------------|-----------|
| <span data-ttu-id="fe81f-134">1. segments</span><span class="sxs-lookup"><span data-stu-id="fe81f-134">Segment 1</span></span> | <span data-ttu-id="fe81f-135">Juridiska persona</span><span class="sxs-lookup"><span data-stu-id="fe81f-135">Legal entity</span></span> | <span data-ttu-id="fe81f-136">CS</span><span class="sxs-lookup"><span data-stu-id="fe81f-136">CS</span></span>        |
| <span data-ttu-id="fe81f-137">2. segments</span><span class="sxs-lookup"><span data-stu-id="fe81f-137">Segment 2</span></span> | <span data-ttu-id="fe81f-138">Konstants</span><span class="sxs-lookup"><span data-stu-id="fe81f-138">Constant</span></span>     | <span data-ttu-id="fe81f-139">-EXPENSE-</span><span class="sxs-lookup"><span data-stu-id="fe81f-139">-EXPENSE-</span></span> |
| <span data-ttu-id="fe81f-140">3. segments</span><span class="sxs-lookup"><span data-stu-id="fe81f-140">Segment 3</span></span> | <span data-ttu-id="fe81f-141">Burtciparu</span><span class="sxs-lookup"><span data-stu-id="fe81f-141">Alphanumeric</span></span> | \#\#\#\#  |

<span data-ttu-id="fe81f-142">**Formatēta numura piemērs**: CS-EXPENSE-0039</span><span class="sxs-lookup"><span data-stu-id="fe81f-142">**Example of formatted number**: CS-EXPENSE-0039</span></span> 

<span data-ttu-id="fe81f-143">Līdzīgu numuru sērijas formātu varat iestatīt citām juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="fe81f-143">You can set up a similar number sequence format for other legal entities.</span></span> <span data-ttu-id="fe81f-144">Juridiskajai personai ar nosaukumu, piemēram, **RW**, ja maināt tikai juridiskās personas segmenta vērtību, formatētais numurs ir RW-EXPENSE-0039.</span><span class="sxs-lookup"><span data-stu-id="fe81f-144">For example, for a legal entity that is named **RW**, if you change only the value of the legal entity segment, the formatted number is RW-EXPENSE-0039.</span></span> <span data-ttu-id="fe81f-145">Citām juridiskajām personām varat mainīt arī visu numuru sērijas formātu.</span><span class="sxs-lookup"><span data-stu-id="fe81f-145">You can also change the whole number sequence format for other legal entities.</span></span> <span data-ttu-id="fe81f-146">Varat, piemēram, izlaist juridiskās personas tvēruma segmentu, lai izveidotu formatētu numuru, piemēram, Exp-0001.</span><span class="sxs-lookup"><span data-stu-id="fe81f-146">For example, you can omit the legal entity scope segment to create a formatted number such as Exp-0001.</span></span>

### <a name="sales-order-numbers"></a><span data-ttu-id="fe81f-147">Pārdošanas pasūtījumu numuri</span><span class="sxs-lookup"><span data-stu-id="fe81f-147">Sales order numbers</span></span>

<span data-ttu-id="fe81f-148">Nākamajā piemērā pārdošanas pasūtījumu numuri ir iestatīti uzņēmumam, kura ID ir **CEU**.</span><span class="sxs-lookup"><span data-stu-id="fe81f-148">In the following example, sales order numbers are set up for the company ID **CEU**.</span></span> 

- <span data-ttu-id="fe81f-149">**Joma:** Pārdošana</span><span class="sxs-lookup"><span data-stu-id="fe81f-149">**Area:** Sales</span></span> 
- <span data-ttu-id="fe81f-150">**Atsauce:** Pārdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="fe81f-150">**Reference:** Sales order</span></span> 
- <span data-ttu-id="fe81f-151">**Tvērums:** Uzņēmums</span><span class="sxs-lookup"><span data-stu-id="fe81f-151">**Scope:** Company</span></span> 
- <span data-ttu-id="fe81f-152">**Uzņēmums:** CEU</span><span class="sxs-lookup"><span data-stu-id="fe81f-152">**Company:** CEU</span></span>

| <span data-ttu-id="fe81f-153">Segmenti</span><span class="sxs-lookup"><span data-stu-id="fe81f-153">Segments</span></span>  | <span data-ttu-id="fe81f-154">Segmenta veids</span><span class="sxs-lookup"><span data-stu-id="fe81f-154">Segment type</span></span> | <span data-ttu-id="fe81f-155">Vērtība</span><span class="sxs-lookup"><span data-stu-id="fe81f-155">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="fe81f-156">1. segments</span><span class="sxs-lookup"><span data-stu-id="fe81f-156">Segment 1</span></span> | <span data-ttu-id="fe81f-157">Konstants</span><span class="sxs-lookup"><span data-stu-id="fe81f-157">Constant</span></span>     | <span data-ttu-id="fe81f-158">SO-</span><span class="sxs-lookup"><span data-stu-id="fe81f-158">SO-</span></span>      |
| <span data-ttu-id="fe81f-159">2. segments</span><span class="sxs-lookup"><span data-stu-id="fe81f-159">Segment 2</span></span> | <span data-ttu-id="fe81f-160">Burtciparu</span><span class="sxs-lookup"><span data-stu-id="fe81f-160">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="fe81f-161">**Formatēta numura piemērs**: SO-0029</span><span class="sxs-lookup"><span data-stu-id="fe81f-161">**Example of formatted number**: SO-0029</span></span> 

<span data-ttu-id="fe81f-162">Kaut arī tvēruma segments nav iekļauts šajā formāts, numerācija tiek restartēta katram uzņēmuma ID.</span><span class="sxs-lookup"><span data-stu-id="fe81f-162">Even though a scope segment is not included in the format, numbering restarts for each company ID.</span></span> <span data-ttu-id="fe81f-163">Ja izmantojat vienu formātu visiem uzņēmumu ID, tie paši numuri tiek izmantoti katrā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="fe81f-163">If you use the same format for all company IDs, the same numbers are used in each company.</span></span> <span data-ttu-id="fe81f-164">Piemēram, pārdošanas pasūtījuma numurs SO-0029 tiek izmantots katrā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="fe81f-164">For example, sales order number SO-0029 is used in each company.</span></span> <span data-ttu-id="fe81f-165">Citu uzņēmumu ID varat mainīt arī visu numuru sērijas formātu.</span><span class="sxs-lookup"><span data-stu-id="fe81f-165">You can also change the whole number sequence format for other company IDs.</span></span>

### <a name="purchase-requisition-numbers"></a><span data-ttu-id="fe81f-166">Pirkšanas pieprasījumu numuri</span><span class="sxs-lookup"><span data-stu-id="fe81f-166">Purchase requisition numbers</span></span>

<span data-ttu-id="fe81f-167">Nākamajā piemērā pirkšanas pieprasījumu numuri tiek izmantoti visas organizācijas līmenī.</span><span class="sxs-lookup"><span data-stu-id="fe81f-167">In the following example, purchase requisition numbers are organization-wide.</span></span> 

- <span data-ttu-id="fe81f-168">**Joma:** Pirkšana</span><span class="sxs-lookup"><span data-stu-id="fe81f-168">**Area:** Purchase</span></span> 
- <span data-ttu-id="fe81f-169">**Atsauce:** Pirkšanas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="fe81f-169">**Reference:** Purchase requisition</span></span> 
- <span data-ttu-id="fe81f-170">**Tvērums:** Koplietots</span><span class="sxs-lookup"><span data-stu-id="fe81f-170">**Scope:** Shared</span></span>

| <span data-ttu-id="fe81f-171">Segmenti</span><span class="sxs-lookup"><span data-stu-id="fe81f-171">Segments</span></span>  | <span data-ttu-id="fe81f-172">Segmenta veids</span><span class="sxs-lookup"><span data-stu-id="fe81f-172">Segment type</span></span> | <span data-ttu-id="fe81f-173">Vērtība</span><span class="sxs-lookup"><span data-stu-id="fe81f-173">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="fe81f-174">1. segments</span><span class="sxs-lookup"><span data-stu-id="fe81f-174">Segment 1</span></span> | <span data-ttu-id="fe81f-175">Konstants</span><span class="sxs-lookup"><span data-stu-id="fe81f-175">Constant</span></span>     | <span data-ttu-id="fe81f-176">Req</span><span class="sxs-lookup"><span data-stu-id="fe81f-176">Req</span></span>      |
| <span data-ttu-id="fe81f-177">2. segments</span><span class="sxs-lookup"><span data-stu-id="fe81f-177">Segment 2</span></span> | <span data-ttu-id="fe81f-178">Burtciparu</span><span class="sxs-lookup"><span data-stu-id="fe81f-178">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="fe81f-179">**Formatēta numura piemērs**: Req0052</span><span class="sxs-lookup"><span data-stu-id="fe81f-179">**Example of formatted number**: Req0052</span></span> 

<span data-ttu-id="fe81f-180">Tā kā tvērums ir **Koplietots**, šis numuru sērijas formāts tiek izmantots visā organizācijā.</span><span class="sxs-lookup"><span data-stu-id="fe81f-180">Because the scope is **Shared**, the number sequence format is used across the organization.</span></span> <span data-ttu-id="fe81f-181">Dažādām organizācijas daļām nevarat iestatīt atšķirīgus numuru sēriju formātus.</span><span class="sxs-lookup"><span data-stu-id="fe81f-181">You cannot set up different number sequence formats for different parts of the organization.</span></span> 

<a name="performance-considerations-for-number-sequences"></a><span data-ttu-id="fe81f-182">Ar numuru sēriju veiktspēju saistītie apsvērumi</span><span class="sxs-lookup"><span data-stu-id="fe81f-182">Performance considerations for number sequences</span></span>
-----------------------------------------------

<span data-ttu-id="fe81f-183">Pirms iestatāt numuru sērijas, ņemiet vērā tālāk sniegto informāciju par to, kā numuru sēriju konfigurācija var ietekmēt sistēmas veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="fe81f-183">Consider the following information about how the configuration of number sequences can affect system performance before you set up number sequences.</span></span>

### <a name="continuous-and-non-continuous-number-sequences"></a><span data-ttu-id="fe81f-184">Nepārtrauktas numuru sērijas un numuru sērijas ar pārtraukumiem</span><span class="sxs-lookup"><span data-stu-id="fe81f-184">Continuous and non-continuous number sequences</span></span>

<span data-ttu-id="fe81f-185">Numuru sērijas var būt nepārtrauktas vai ar pārtraukumiem.</span><span class="sxs-lookup"><span data-stu-id="fe81f-185">Number sequences can be continuous or non-continuous.</span></span> <span data-ttu-id="fe81f-186">Nepārtrauktā numuru sērijā netiek izlaists neviens numurs, bet numurus nedrīkst izmantot secīgi.</span><span class="sxs-lookup"><span data-stu-id="fe81f-186">A continuous number sequence does not skip any numbers, but numbers may not be used sequentially.</span></span> <span data-ttu-id="fe81f-187">Numuru sērijās ar pārtraukumiem numuri tiek izmantoti secīgi, bet numuru sērija numurus var izlaist.</span><span class="sxs-lookup"><span data-stu-id="fe81f-187">Numbers from a non-continuous number sequence are used sequentially, but the number sequence may skip numbers.</span></span> <span data-ttu-id="fe81f-188">Piemēram, ja lietotājs atceļ darījumu, numurs tiek izveidots, bet netiek lietots.</span><span class="sxs-lookup"><span data-stu-id="fe81f-188">For example, if a user cancels a transaction, a number is generated, but not used.</span></span> <span data-ttu-id="fe81f-189">Nepārtrauktā numuru sērijā šis numurs vēlāk tiek izmantots atkal.</span><span class="sxs-lookup"><span data-stu-id="fe81f-189">In a continuous number sequence, that number is recycled later.</span></span> <span data-ttu-id="fe81f-190">Numuru sērijā ar pārtraukumiem šis numurs vairs netiek izmantots.</span><span class="sxs-lookup"><span data-stu-id="fe81f-190">In a non-continuous number sequence, the number is not used.</span></span> 

<span data-ttu-id="fe81f-191">Nepārtrauktas numuru sērijas parasti ir nepieciešamas ārējiem dokumentiem, piemēram, pirkšanas pasūtījumiem, pārdošanas pasūtījumiem un rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="fe81f-191">Continuous number sequences are typically required for external documents, such as purchase orders, sales orders, and invoices.</span></span> <span data-ttu-id="fe81f-192">Tomēr nepārtrauktas numuru sērijas var negatīvi ietekmēt sistēmas atbildes laikus, jo sistēmai numurs no datu bāzes ir jāpieprasa katru reizi, kad tiek izveidots jauns dokuments vai ieraksts.</span><span class="sxs-lookup"><span data-stu-id="fe81f-192">However, continuous number sequences can adversely affect system response times because the system must request a number from the database every time that a new document or record is created.</span></span> 

<span data-ttu-id="fe81f-193">Ja izmantojat numuru sēriju ar pārtraukumiem, varat iespējot vienumu **Numuru rezervēšana** kopsavilkuma cilnē **Veiktspēja**, kas atrodas lapā **Numuru sērijas**.</span><span class="sxs-lookup"><span data-stu-id="fe81f-193">If you use a non-continuous number sequence, you can enable **Preallocation** on the **Performance** FastTab of the **Number sequences** page.</span></span> <span data-ttu-id="fe81f-194">Ja norādāt rezervēto numuru daudzumu, sistēma atlasa šos numurus un saglabā tos atmiņā.</span><span class="sxs-lookup"><span data-stu-id="fe81f-194">When you specify a quantity of numbers to preallocate, the system selects those numbers and stores them in memory.</span></span> <span data-ttu-id="fe81f-195">Jauni numuri no datu bāzes tiek pieprasīti tikai pēc tam, kad ir izmantots šis rezervētais daudzums.</span><span class="sxs-lookup"><span data-stu-id="fe81f-195">New numbers are requested from the database only after the preallocated quantity has been used.</span></span> 

<span data-ttu-id="fe81f-196">Ja vien nav ar likumu noteiktas prasības izmantot nepārtrauktas numuru sērijas, labākas veiktspējas nolūkos ieteicams izmantot numuru sērijas ar pārtraukumiem.</span><span class="sxs-lookup"><span data-stu-id="fe81f-196">Unless there is a regulatory requirement that you use continuous number sequences, we recommend that you use non-continuous number sequences for better performance.</span></span>

### <a name="automatic-cleanup-of-number-sequences"></a><span data-ttu-id="fe81f-197">Automātiskā numuru sēriju tīrīšana</span><span class="sxs-lookup"><span data-stu-id="fe81f-197">Automatic cleanup of number sequences</span></span>

<span data-ttu-id="fe81f-198">Ja rodas elektropadeves traucējumi, programmas kļūda vai citas neparedzētas kļūmes, sistēma nevar automātiski pārstrādāt nepārtraukto numuru secību numurus.</span><span class="sxs-lookup"><span data-stu-id="fe81f-198">In case of a power failure, an application error, or other unexpected failure, the system cannot recycle numbers automatically for continuous number sequences.</span></span> <span data-ttu-id="fe81f-199">Lai atgūtu zaudētos numurus, manuāli vai automātiski varat palaist tīrīšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="fe81f-199">You can run the cleanup process manually or automatically to recover the lost numbers.</span></span> 

<span data-ttu-id="fe81f-200">Kad plānojat tīrīšanas procesu, rūpīgi apsveriet servera lietojumu.</span><span class="sxs-lookup"><span data-stu-id="fe81f-200">Carefully consider server usage when you plan the cleanup process.</span></span> <span data-ttu-id="fe81f-201">Mēs iesakām veikt tīrīšanu kā pakešuzdevumu ārpus sastrēgumstundām.</span><span class="sxs-lookup"><span data-stu-id="fe81f-201">We recommend that you perform the cleanup as a batch job during non-peak hours.</span></span>






