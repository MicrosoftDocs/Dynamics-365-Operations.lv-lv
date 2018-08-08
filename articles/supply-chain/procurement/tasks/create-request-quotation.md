--- 
title: "Piedāvājuma pieprasījuma izveide"
description: "Šajā procedūrā ir parādīts, kā izveidot piedāvājuma pieprasījumu."
author: mkirknel
manager: AnnBe
ms.date: 11/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: f9927e291916ed1d7f0b706e5920d73835dc2755
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-request-for-quotation"></a><span data-ttu-id="464ce-103">Piedāvājuma pieprasījuma izveide</span><span class="sxs-lookup"><span data-stu-id="464ce-103">Create a request for quotation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="464ce-104">Šajā procedūrā ir parādīts, kā izveidot piedāvājuma pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="464ce-104">This procedure shows you how to create a request for quotation.</span></span> <span data-ttu-id="464ce-105">Parasti to veic pirkšanas aģents.</span><span class="sxs-lookup"><span data-stu-id="464ce-105">This would typically be done by a purchasing agent.</span></span> <span data-ttu-id="464ce-106">Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="464ce-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="464ce-107">Pirms sākšanas ir jāiestata lūguma tipi.</span><span class="sxs-lookup"><span data-stu-id="464ce-107">You need to have set up solicitation types before you start.</span></span> <span data-ttu-id="464ce-108">Kad esat pabeidzis šo uzdevumu un esat izveidojis un nosūtījis kādu PP, varat ievadīt atbildes katram kreditoram, salīdzināt tās un piešķirt līgumu.</span><span class="sxs-lookup"><span data-stu-id="464ce-108">Once you’ve completed this task and you’ve created and sent an RFQ you can then enter the replies per vendor, compare them, and award the contract.</span></span>


## <a name="prepare-a-new-rfq"></a><span data-ttu-id="464ce-109">Sagatavot jaunu PP</span><span class="sxs-lookup"><span data-stu-id="464ce-109">Prepare a new RFQ</span></span>
1. <span data-ttu-id="464ce-110">Dodieties uz Sagāde un avoti > Piedāvājumu pieprasījumi > Visi piedāvājumu pieprasījumi.</span><span class="sxs-lookup"><span data-stu-id="464ce-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="464ce-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="464ce-111">Click New.</span></span>
    * <span data-ttu-id="464ce-112">Ir pieejami tālāk uzskaitītie pirkšanas tipi. Pirkšanas pasūtījums (šis ir noklusējuma tips): dokuments, kas apstiprina piedāvājumu iegādāties preces vai pieņem piedāvājumu pārdot preces apmaiņā pret maksājumu.</span><span class="sxs-lookup"><span data-stu-id="464ce-112">The following purchase types are available: Purchase order (this is the default): a document that confirms the offer to buy products, or the acceptance of an offer to sell products in exchange for payment.</span></span> <span data-ttu-id="464ce-113">Pirkšanas pieprasījums: šis tips tiek atlasīts automātiski, ja PP izveidojat tieši no pirkšanas pieprasījuma.</span><span class="sxs-lookup"><span data-stu-id="464ce-113">Purchase requisition: this type is automatically selected if you create an RFQ directly from a purchase requisition.</span></span> <span data-ttu-id="464ce-114">Ja šo opciju atlasāt manuāli, tiek parādīts kļūdas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="464ce-114">If you manually select this option, you’ll get an error.</span></span> <span data-ttu-id="464ce-115">Pirkšanas līgums: līgums par noteikta preču daudzuma vai preču vērtības iegādi laika gaitā.</span><span class="sxs-lookup"><span data-stu-id="464ce-115">Purchase agreement: an agreement to purchase a specific quantity or value of product over time.</span></span> <span data-ttu-id="464ce-116">Ja atlasāt šo opciju, ir jāatlasa datumu diapazons, kas attiecas uz šo pirkšanas līgumu.</span><span class="sxs-lookup"><span data-stu-id="464ce-116">If you select this option, you must select the date range that applies to the purchase agreement.</span></span>  
3. <span data-ttu-id="464ce-117">Laukā Dokumenta nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="464ce-117">In the Document title field, type a value.</span></span>
4. <span data-ttu-id="464ce-118">Laukā Lūguma tips ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="464ce-118">In the Solicitation type field, enter or select a value.</span></span>
    * <span data-ttu-id="464ce-119">Ja ar lūguma veidu ir saistīta kāda punktu skaitīšanas metode, tad tā būs punktu skaitīšanas noklusējuma metode jūsu veidotajam PP.</span><span class="sxs-lookup"><span data-stu-id="464ce-119">If a scoring method is associated with the solicitation type, this will be the default scoring method for the RFQ that you’re creating.</span></span> <span data-ttu-id="464ce-120">Punktu skaitīšanas metodi vēlāk var mainīt.</span><span class="sxs-lookup"><span data-stu-id="464ce-120">It is possible to change the scoring method later.</span></span>  
    * <span data-ttu-id="464ce-121">Laukā Piegādes datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="464ce-121">In the Delivery date field, enter a date.</span></span>  
    * <span data-ttu-id="464ce-122">Atlasiet datumu, līdz kuram vēlaties saņemt krājumus.</span><span class="sxs-lookup"><span data-stu-id="464ce-122">Select the date by which you want to receive the items.</span></span>  
    * <span data-ttu-id="464ce-123">Laukā Beigu datums un laiks ievadiet kādu datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="464ce-123">In the Expiration date and time field, enter a date and time.</span></span>  
    * <span data-ttu-id="464ce-124">Norādiet datumu un laiku, līdz kuram kreditoram ir jāatbild uz attiecīgo PP.</span><span class="sxs-lookup"><span data-stu-id="464ce-124">Specify the date and time by which vendors must respond to the RFQ.</span></span>  
5. <span data-ttu-id="464ce-125">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="464ce-125">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="464ce-126">Piegādes adrese pēc noklusējuma ir noliktavas adrese.</span><span class="sxs-lookup"><span data-stu-id="464ce-126">The delivery address will default to the warehouse address.</span></span>  
6. <span data-ttu-id="464ce-127">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="464ce-127">Click OK.</span></span>

## <a name="add-lines"></a><span data-ttu-id="464ce-128">Pievienot rindas</span><span class="sxs-lookup"><span data-stu-id="464ce-128">Add lines</span></span>
    * <span data-ttu-id="464ce-129">Kad esat norādījis pamatinformāciju par savu PP, ir jānorāda preces vai pakalpojumi, par kuriem vēlaties saņemt kreditoru priekšlikumus.</span><span class="sxs-lookup"><span data-stu-id="464ce-129">After you’ve specified the basic information about your RFQ, you specify the goods or services that you want vendors to bid on.</span></span> <span data-ttu-id="464ce-130">Noklusējuma rindas tips ir Krājums.</span><span class="sxs-lookup"><span data-stu-id="464ce-130">Item is the default line type.</span></span>   
1. <span data-ttu-id="464ce-131">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="464ce-131">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="464ce-132">Ja izmantojat USMF, varat atlasīt T0020.</span><span class="sxs-lookup"><span data-stu-id="464ce-132">If you're using USMF, you can select T0020.</span></span>  
2. <span data-ttu-id="464ce-133">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="464ce-133">In the Quantity field, enter a number.</span></span>
3. <span data-ttu-id="464ce-134">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="464ce-134">Click Add line.</span></span>
4. <span data-ttu-id="464ce-135">Laukā Rindas tips atlasiet “Kategorija”.</span><span class="sxs-lookup"><span data-stu-id="464ce-135">In the Line type field, select 'Category'.</span></span>
    * <span data-ttu-id="464ce-136">Varat izmantot rindas tipu Kategorija, lai izveidotu PP neuzskaitāmām precēm vai pakalpojumiem.</span><span class="sxs-lookup"><span data-stu-id="464ce-136">You can use the Category line type to create RFQs for non-inventory goods or services.</span></span> <span data-ttu-id="464ce-137">Pēc tam ir nepieciešams preču vai pakalpojumu tipu atlasīt no sagādes kategoriju hierarhijas.</span><span class="sxs-lookup"><span data-stu-id="464ce-137">You then need to select the type of goods or services from a hierarchy of procurement categories.</span></span>  
5. <span data-ttu-id="464ce-138">Sagādes kategorijas laukā ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="464ce-138">In the Procurement category field, enter or select a value.</span></span>
6. <span data-ttu-id="464ce-139">Laukā Preces nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="464ce-139">In the Product name field, type a value.</span></span>
7. <span data-ttu-id="464ce-140">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="464ce-140">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="464ce-141">Laukā Vienība ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="464ce-141">In the Unit field, enter or select a value.</span></span>

## <a name="add-vendors"></a><span data-ttu-id="464ce-142">Pievienot kreditorus</span><span class="sxs-lookup"><span data-stu-id="464ce-142">Add vendors</span></span>
1. <span data-ttu-id="464ce-143">Noklikšķiniet uz Virsraksts, lai no rindu skata pārslēgtu uz virsrakstu skatu.</span><span class="sxs-lookup"><span data-stu-id="464ce-143">Click Header to change from the Lines view to the Header view.</span></span> 
2. <span data-ttu-id="464ce-144">Izvērsiet sadaļu Kreditors.</span><span class="sxs-lookup"><span data-stu-id="464ce-144">Expand the Vendor section.</span></span>
3. <span data-ttu-id="464ce-145">Noklikšķiniet uz Automātiski pievienot kreditorus.</span><span class="sxs-lookup"><span data-stu-id="464ce-145">Click Auto-add vendors.</span></span>
    * <span data-ttu-id="464ce-146">Kreditorus saviem PP varat pievienot automātiski, ņemot vērā pieprasīto krājumu sagādes kategoriju.</span><span class="sxs-lookup"><span data-stu-id="464ce-146">You can add vendors to the RFQ automatically, based on the procurement category of the items requested.</span></span> <span data-ttu-id="464ce-147">Ja rindās iekļautajām kategorijām nav apstiprināts neviens kreditors, tad kreditorus varat pievienot manuāli.</span><span class="sxs-lookup"><span data-stu-id="464ce-147">If there are no vendors approved for the categories included in the lines you can add vendors manually.</span></span>  
4. <span data-ttu-id="464ce-148">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="464ce-148">Click Add.</span></span>
5. <span data-ttu-id="464ce-149">Ievadiet vai atlasiet vērtību laukā kreditora konts.</span><span class="sxs-lookup"><span data-stu-id="464ce-149">In the Vendor account field, enter or select a value.</span></span>
6. <span data-ttu-id="464ce-150">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="464ce-150">Click Add.</span></span>
7. <span data-ttu-id="464ce-151">Ievadiet vai atlasiet vērtību laukā kreditora konts.</span><span class="sxs-lookup"><span data-stu-id="464ce-151">In the Vendor account field, enter or select a value.</span></span>
    * <span data-ttu-id="464ce-152">Kad kreditors ir atlasīts, statuss kļūst par Izveidots.</span><span class="sxs-lookup"><span data-stu-id="464ce-152">Once you’ve selected a vendor, the status is Created.</span></span> <span data-ttu-id="464ce-153">Tas nozīmē, ka kreditora informācija ir saglabāta PP, bet PP nav nosūtīts kreditoram.</span><span class="sxs-lookup"><span data-stu-id="464ce-153">This means that the vendor information has been saved in the RFQ, but you have not sent the RFQ to the vendor.</span></span> <span data-ttu-id="464ce-154">Jūs varat kreditoru pievienot piedāvājuma pieprasījumam neatkarīgi no kreditora statusa.</span><span class="sxs-lookup"><span data-stu-id="464ce-154">You can add a vendor to an RFQ regardless of the vendor status.</span></span>  

## <a name="send-the-rfq-to-vendors"></a><span data-ttu-id="464ce-155">Sūtīšana PP kreditoriem</span><span class="sxs-lookup"><span data-stu-id="464ce-155">Send the RFQ to vendors</span></span>
1. <span data-ttu-id="464ce-156">Noklikšķiniet uz Sūtīt.</span><span class="sxs-lookup"><span data-stu-id="464ce-156">Click Send.</span></span>
    * <span data-ttu-id="464ce-157">Lapā Piedāvājuma pieprasījuma sūtīšana pārbaudiet, vai sarakstā uzskaitītie kreditori ir tie kreditori, kuriem ir jāsaņem šis PP.</span><span class="sxs-lookup"><span data-stu-id="464ce-157">In the Sending request for quotation page, check that the vendors in the list are the ones that you want to receive the RFQ.</span></span>  
2. <span data-ttu-id="464ce-158">Klikšķiniet Drukāt.</span><span class="sxs-lookup"><span data-stu-id="464ce-158">Click Print.</span></span>
    * <span data-ttu-id="464ce-159">Izmantojot šo dialoglodziņu, varat drukāt PP.</span><span class="sxs-lookup"><span data-stu-id="464ce-159">This dialog allows you to print the RFQ.</span></span> <span data-ttu-id="464ce-160">Ja izlemjat drukāt atbilžu lapu, tās saturs tiek definēts lapā Sagādes un avotu parametri.</span><span class="sxs-lookup"><span data-stu-id="464ce-160">If you choose to print a reply sheet, the contents of this are defined in Procurement and Sourcing parameters.</span></span> <span data-ttu-id="464ce-161">Lai izvēlētos, kā drukāt atbilžu lapas, kad esat atvēris dialoglodziņu Drukāt, noklikšķiniet uz Papildu drukāšanas opcijas.</span><span class="sxs-lookup"><span data-stu-id="464ce-161">To choose how to print reply sheets, once you’ve opened the Print dialog, click Advanced printing options.</span></span> <span data-ttu-id="464ce-162">Katram kreditoram tiks drukāts viens PP, kas satur rindas, kuru statuss ir Izveidots vai Nosūtīts.</span><span class="sxs-lookup"><span data-stu-id="464ce-162">One RFQ will be printed for each vendor containing the lines that have the status of Created or Sent.</span></span> <span data-ttu-id="464ce-163">Atceltas rindas un rindas ar reģistrētām atbildēm netiks drukātas.</span><span class="sxs-lookup"><span data-stu-id="464ce-163">Canceled lines and lines with registered replies will not be printed.</span></span>   
3. <span data-ttu-id="464ce-164">Noklikšķiniet uz Atcelt.</span><span class="sxs-lookup"><span data-stu-id="464ce-164">Click Cancel.</span></span>
4. <span data-ttu-id="464ce-165">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="464ce-165">Click OK.</span></span>
5. <span data-ttu-id="464ce-166">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="464ce-166">Close the page.</span></span>
6. <span data-ttu-id="464ce-167">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="464ce-167">Close the page.</span></span>

## <a name="view-the-rfq-journal"></a><span data-ttu-id="464ce-168">Skatīt PP žurnālu</span><span class="sxs-lookup"><span data-stu-id="464ce-168">View the RFQ journal</span></span>
1. <span data-ttu-id="464ce-169">Dodieties uz Sagāde un avoti > Piedāvājumu pieprasījumi > Piedāvājuma pieprasījuma sekojums > Piedāvājuma pieprasījumu žurnāli.</span><span class="sxs-lookup"><span data-stu-id="464ce-169">Go to Procurement and sourcing > Requests for quotations > Request for quotations follow-up > Request for quotation journals.</span></span>
2. <span data-ttu-id="464ce-170">Noklikšķiniet uz Priekšskatīt/Drukāt.</span><span class="sxs-lookup"><span data-stu-id="464ce-170">Click Preview/Print.</span></span>
3. <span data-ttu-id="464ce-171">Noklikšķiniet uz Oriģināla priekšskatījums.</span><span class="sxs-lookup"><span data-stu-id="464ce-171">Click Original preview.</span></span>
4. <span data-ttu-id="464ce-172">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="464ce-172">Close the page.</span></span>
5. <span data-ttu-id="464ce-173">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="464ce-173">Close the page.</span></span>


