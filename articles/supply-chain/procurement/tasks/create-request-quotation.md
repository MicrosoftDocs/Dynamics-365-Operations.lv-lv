---
title: Piedāvājuma pieprasījuma izveide
description: Šajā procedūrā ir parādīts, kā izveidot piedāvājuma pieprasījumu.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchCreateRFQCase, InventLocationIdLookup, PurchRFQCaseTable, InventItemIdLookupSimple, EcoResCategorySingleLookup, UnitOfMeasureLookup, PurchRFQEditLines, PurchRFQEditLinesPrintOptions, VendRFQJournal, SrsReportViewerForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4c09149fcbe5731126c2e48a37fafdf71c1d49df
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "334454"
---
# <a name="create-a-request-for-quotation"></a><span data-ttu-id="132e0-103">Piedāvājuma pieprasījuma izveide</span><span class="sxs-lookup"><span data-stu-id="132e0-103">Create a request for quotation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="132e0-104">Šajā procedūrā ir parādīts, kā izveidot piedāvājuma pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="132e0-104">This procedure shows you how to create a request for quotation.</span></span> <span data-ttu-id="132e0-105">Parasti to veic pirkšanas aģents.</span><span class="sxs-lookup"><span data-stu-id="132e0-105">This would typically be done by a purchasing agent.</span></span> <span data-ttu-id="132e0-106">Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="132e0-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="132e0-107">Pirms sākšanas ir jāiestata lūguma tipi.</span><span class="sxs-lookup"><span data-stu-id="132e0-107">You need to have set up solicitation types before you start.</span></span> <span data-ttu-id="132e0-108">Kad esat pabeidzis šo uzdevumu un esat izveidojis un nosūtījis kādu PP, varat ievadīt atbildes katram kreditoram, salīdzināt tās un piešķirt līgumu.</span><span class="sxs-lookup"><span data-stu-id="132e0-108">Once you’ve completed this task and you’ve created and sent an RFQ you can then enter the replies per vendor, compare them, and award the contract.</span></span>


## <a name="prepare-a-new-rfq"></a><span data-ttu-id="132e0-109">Sagatavot jaunu PP</span><span class="sxs-lookup"><span data-stu-id="132e0-109">Prepare a new RFQ</span></span>
1. <span data-ttu-id="132e0-110">Dodieties uz Sagāde un avoti > Piedāvājumu pieprasījumi > Visi piedāvājumu pieprasījumi.</span><span class="sxs-lookup"><span data-stu-id="132e0-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="132e0-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="132e0-111">Click New.</span></span>
    * <span data-ttu-id="132e0-112">Ir pieejami tālāk uzskaitītie pirkšanas tipi. Pirkšanas pasūtījums (šis ir noklusējuma tips): dokuments, kas apstiprina piedāvājumu iegādāties preces vai pieņem piedāvājumu pārdot preces apmaiņā pret maksājumu.</span><span class="sxs-lookup"><span data-stu-id="132e0-112">The following purchase types are available: Purchase order (this is the default): a document that confirms the offer to buy products, or the acceptance of an offer to sell products in exchange for payment.</span></span> <span data-ttu-id="132e0-113">Pirkšanas pieprasījums: šis tips tiek atlasīts automātiski, ja PP izveidojat tieši no pirkšanas pieprasījuma.</span><span class="sxs-lookup"><span data-stu-id="132e0-113">Purchase requisition: this type is automatically selected if you create an RFQ directly from a purchase requisition.</span></span> <span data-ttu-id="132e0-114">Ja šo opciju atlasāt manuāli, tiek parādīts kļūdas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="132e0-114">If you manually select this option, you’ll get an error.</span></span> <span data-ttu-id="132e0-115">Pirkšanas līgums: līgums par noteikta preču daudzuma vai preču vērtības iegādi laika gaitā.</span><span class="sxs-lookup"><span data-stu-id="132e0-115">Purchase agreement: an agreement to purchase a specific quantity or value of product over time.</span></span> <span data-ttu-id="132e0-116">Ja atlasāt šo opciju, ir jāatlasa datumu diapazons, kas attiecas uz šo pirkšanas līgumu.</span><span class="sxs-lookup"><span data-stu-id="132e0-116">If you select this option, you must select the date range that applies to the purchase agreement.</span></span>  
3. <span data-ttu-id="132e0-117">Laukā Dokumenta nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="132e0-117">In the Document title field, type a value.</span></span>
4. <span data-ttu-id="132e0-118">Laukā Lūguma tips ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="132e0-118">In the Solicitation type field, enter or select a value.</span></span>
    * <span data-ttu-id="132e0-119">Ja ar lūguma veidu ir saistīta kāda punktu skaitīšanas metode, tad tā būs punktu skaitīšanas noklusējuma metode jūsu veidotajam PP.</span><span class="sxs-lookup"><span data-stu-id="132e0-119">If a scoring method is associated with the solicitation type, this will be the default scoring method for the RFQ that you’re creating.</span></span> <span data-ttu-id="132e0-120">Punktu skaitīšanas metodi vēlāk var mainīt.</span><span class="sxs-lookup"><span data-stu-id="132e0-120">It is possible to change the scoring method later.</span></span>  
    * <span data-ttu-id="132e0-121">Laukā Piegādes datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="132e0-121">In the Delivery date field, enter a date.</span></span>  
    * <span data-ttu-id="132e0-122">Atlasiet datumu, līdz kuram vēlaties saņemt krājumus.</span><span class="sxs-lookup"><span data-stu-id="132e0-122">Select the date by which you want to receive the items.</span></span>  
    * <span data-ttu-id="132e0-123">Laukā Beigu datums un laiks ievadiet kādu datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="132e0-123">In the Expiration date and time field, enter a date and time.</span></span>  
    * <span data-ttu-id="132e0-124">Norādiet datumu un laiku, līdz kuram kreditoram ir jāatbild uz attiecīgo PP.</span><span class="sxs-lookup"><span data-stu-id="132e0-124">Specify the date and time by which vendors must respond to the RFQ.</span></span>  
5. <span data-ttu-id="132e0-125">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="132e0-125">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="132e0-126">Piegādes adrese pēc noklusējuma ir noliktavas adrese.</span><span class="sxs-lookup"><span data-stu-id="132e0-126">The delivery address will default to the warehouse address.</span></span>  
6. <span data-ttu-id="132e0-127">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="132e0-127">Click OK.</span></span>

## <a name="add-lines"></a><span data-ttu-id="132e0-128">Pievienot rindas</span><span class="sxs-lookup"><span data-stu-id="132e0-128">Add lines</span></span>
    * <span data-ttu-id="132e0-129">Kad esat norādījis pamatinformāciju par savu PP, ir jānorāda preces vai pakalpojumi, par kuriem vēlaties saņemt kreditoru priekšlikumus.</span><span class="sxs-lookup"><span data-stu-id="132e0-129">After you’ve specified the basic information about your RFQ, you specify the goods or services that you want vendors to bid on.</span></span> <span data-ttu-id="132e0-130">Noklusējuma rindas tips ir Krājums.</span><span class="sxs-lookup"><span data-stu-id="132e0-130">Item is the default line type.</span></span>   
1. <span data-ttu-id="132e0-131">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="132e0-131">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="132e0-132">Ja izmantojat USMF, varat atlasīt T0020.</span><span class="sxs-lookup"><span data-stu-id="132e0-132">If you're using USMF, you can select T0020.</span></span>  
2. <span data-ttu-id="132e0-133">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="132e0-133">In the Quantity field, enter a number.</span></span>
3. <span data-ttu-id="132e0-134">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="132e0-134">Click Add line.</span></span>
4. <span data-ttu-id="132e0-135">Laukā Rindas tips atlasiet “Kategorija”.</span><span class="sxs-lookup"><span data-stu-id="132e0-135">In the Line type field, select 'Category'.</span></span>
    * <span data-ttu-id="132e0-136">Varat izmantot rindas tipu Kategorija, lai izveidotu PP neuzskaitāmām precēm vai pakalpojumiem.</span><span class="sxs-lookup"><span data-stu-id="132e0-136">You can use the Category line type to create RFQs for non-inventory goods or services.</span></span> <span data-ttu-id="132e0-137">Pēc tam ir nepieciešams preču vai pakalpojumu tipu atlasīt no sagādes kategoriju hierarhijas.</span><span class="sxs-lookup"><span data-stu-id="132e0-137">You then need to select the type of goods or services from a hierarchy of procurement categories.</span></span>  
5. <span data-ttu-id="132e0-138">Sagādes kategorijas laukā ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="132e0-138">In the Procurement category field, enter or select a value.</span></span>
6. <span data-ttu-id="132e0-139">Laukā Preces nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="132e0-139">In the Product name field, type a value.</span></span>
7. <span data-ttu-id="132e0-140">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="132e0-140">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="132e0-141">Laukā Vienība ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="132e0-141">In the Unit field, enter or select a value.</span></span>

## <a name="add-vendors"></a><span data-ttu-id="132e0-142">Pievienot kreditorus</span><span class="sxs-lookup"><span data-stu-id="132e0-142">Add vendors</span></span>
1. <span data-ttu-id="132e0-143">Noklikšķiniet uz Virsraksts, lai no rindu skata pārslēgtu uz virsrakstu skatu.</span><span class="sxs-lookup"><span data-stu-id="132e0-143">Click Header to change from the Lines view to the Header view.</span></span> 
2. <span data-ttu-id="132e0-144">Izvērsiet sadaļu Kreditors.</span><span class="sxs-lookup"><span data-stu-id="132e0-144">Expand the Vendor section.</span></span>
3. <span data-ttu-id="132e0-145">Noklikšķiniet uz Automātiski pievienot kreditorus.</span><span class="sxs-lookup"><span data-stu-id="132e0-145">Click Auto-add vendors.</span></span>
    * <span data-ttu-id="132e0-146">Kreditorus saviem PP varat pievienot automātiski, ņemot vērā pieprasīto krājumu sagādes kategoriju.</span><span class="sxs-lookup"><span data-stu-id="132e0-146">You can add vendors to the RFQ automatically, based on the procurement category of the items requested.</span></span> <span data-ttu-id="132e0-147">Ja rindās iekļautajām kategorijām nav apstiprināts neviens kreditors, tad kreditorus varat pievienot manuāli.</span><span class="sxs-lookup"><span data-stu-id="132e0-147">If there are no vendors approved for the categories included in the lines you can add vendors manually.</span></span>  
4. <span data-ttu-id="132e0-148">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="132e0-148">Click Add.</span></span>
5. <span data-ttu-id="132e0-149">Ievadiet vai atlasiet vērtību laukā kreditora konts.</span><span class="sxs-lookup"><span data-stu-id="132e0-149">In the Vendor account field, enter or select a value.</span></span>
6. <span data-ttu-id="132e0-150">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="132e0-150">Click Add.</span></span>
7. <span data-ttu-id="132e0-151">Ievadiet vai atlasiet vērtību laukā kreditora konts.</span><span class="sxs-lookup"><span data-stu-id="132e0-151">In the Vendor account field, enter or select a value.</span></span>
    * <span data-ttu-id="132e0-152">Kad kreditors ir atlasīts, statuss kļūst par Izveidots.</span><span class="sxs-lookup"><span data-stu-id="132e0-152">Once you’ve selected a vendor, the status is Created.</span></span> <span data-ttu-id="132e0-153">Tas nozīmē, ka kreditora informācija ir saglabāta PP, bet PP nav nosūtīts kreditoram.</span><span class="sxs-lookup"><span data-stu-id="132e0-153">This means that the vendor information has been saved in the RFQ, but you have not sent the RFQ to the vendor.</span></span> <span data-ttu-id="132e0-154">Jūs varat kreditoru pievienot piedāvājuma pieprasījumam neatkarīgi no kreditora statusa.</span><span class="sxs-lookup"><span data-stu-id="132e0-154">You can add a vendor to an RFQ regardless of the vendor status.</span></span>  

## <a name="send-the-rfq-to-vendors"></a><span data-ttu-id="132e0-155">Sūtīšana PP kreditoriem</span><span class="sxs-lookup"><span data-stu-id="132e0-155">Send the RFQ to vendors</span></span>
1. <span data-ttu-id="132e0-156">Noklikšķiniet uz Sūtīt.</span><span class="sxs-lookup"><span data-stu-id="132e0-156">Click Send.</span></span>
    * <span data-ttu-id="132e0-157">Lapā Piedāvājuma pieprasījuma sūtīšana pārbaudiet, vai sarakstā uzskaitītie kreditori ir tie kreditori, kuriem ir jāsaņem šis PP.</span><span class="sxs-lookup"><span data-stu-id="132e0-157">In the Sending request for quotation page, check that the vendors in the list are the ones that you want to receive the RFQ.</span></span>  
2. <span data-ttu-id="132e0-158">Klikšķiniet Drukāt.</span><span class="sxs-lookup"><span data-stu-id="132e0-158">Click Print.</span></span>
    * <span data-ttu-id="132e0-159">Izmantojot šo dialoglodziņu, varat drukāt PP.</span><span class="sxs-lookup"><span data-stu-id="132e0-159">This dialog allows you to print the RFQ.</span></span> <span data-ttu-id="132e0-160">Ja izlemjat drukāt atbilžu lapu, tās saturs tiek definēts lapā Sagādes un avotu parametri.</span><span class="sxs-lookup"><span data-stu-id="132e0-160">If you choose to print a reply sheet, the contents of this are defined in Procurement and Sourcing parameters.</span></span> <span data-ttu-id="132e0-161">Lai izvēlētos, kā drukāt atbilžu lapas, kad esat atvēris dialoglodziņu Drukāt, noklikšķiniet uz Papildu drukāšanas opcijas.</span><span class="sxs-lookup"><span data-stu-id="132e0-161">To choose how to print reply sheets, once you’ve opened the Print dialog, click Advanced printing options.</span></span> <span data-ttu-id="132e0-162">Katram kreditoram tiks drukāts viens PP, kas satur rindas, kuru statuss ir Izveidots vai Nosūtīts.</span><span class="sxs-lookup"><span data-stu-id="132e0-162">One RFQ will be printed for each vendor containing the lines that have the status of Created or Sent.</span></span> <span data-ttu-id="132e0-163">Atceltas rindas un rindas ar reģistrētām atbildēm netiks drukātas.</span><span class="sxs-lookup"><span data-stu-id="132e0-163">Canceled lines and lines with registered replies will not be printed.</span></span>   
3. <span data-ttu-id="132e0-164">Noklikšķiniet uz Atcelt.</span><span class="sxs-lookup"><span data-stu-id="132e0-164">Click Cancel.</span></span>
4. <span data-ttu-id="132e0-165">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="132e0-165">Click OK.</span></span>
5. <span data-ttu-id="132e0-166">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="132e0-166">Close the page.</span></span>
6. <span data-ttu-id="132e0-167">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="132e0-167">Close the page.</span></span>

## <a name="view-the-rfq-journal"></a><span data-ttu-id="132e0-168">Skatīt PP žurnālu</span><span class="sxs-lookup"><span data-stu-id="132e0-168">View the RFQ journal</span></span>
1. <span data-ttu-id="132e0-169">Dodieties uz Sagāde un avoti > Piedāvājumu pieprasījumi > Piedāvājuma pieprasījuma sekojums > Piedāvājuma pieprasījumu žurnāli.</span><span class="sxs-lookup"><span data-stu-id="132e0-169">Go to Procurement and sourcing > Requests for quotations > Request for quotations follow-up > Request for quotation journals.</span></span>
2. <span data-ttu-id="132e0-170">Noklikšķiniet uz Priekšskatīt/Drukāt.</span><span class="sxs-lookup"><span data-stu-id="132e0-170">Click Preview/Print.</span></span>
3. <span data-ttu-id="132e0-171">Noklikšķiniet uz Oriģināla priekšskatījums.</span><span class="sxs-lookup"><span data-stu-id="132e0-171">Click Original preview.</span></span>
4. <span data-ttu-id="132e0-172">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="132e0-172">Close the page.</span></span>
5. <span data-ttu-id="132e0-173">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="132e0-173">Close the page.</span></span>

