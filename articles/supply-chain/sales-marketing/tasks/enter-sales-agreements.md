--- 
title: "Pārdošanas līgumu ievade"
description: "Šajā procedūrā ir parādīts, kā izveidot pārdošanas līgumu, saskaņā ar kuru kāds no jūsu debitoriem apņemsies iegādāties preces par iepriekš norunāto summu, par to saņemot īpašas atlaides."
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: a609cfa6e34159e1037e9c046a3f1658baecbebf
ms.contentlocale: lv-lv
ms.lasthandoff: 09/11/2018

---
# <a name="enter-sales-agreements"></a><span data-ttu-id="f4d30-103">Pārdošanas līgumu ievade</span><span class="sxs-lookup"><span data-stu-id="f4d30-103">Enter sales agreements</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f4d30-104">Šajā procedūrā ir parādīts, kā izveidot pārdošanas līgumu, saskaņā ar kuru kāds no jūsu debitoriem apņemsies iegādāties preces par</span><span class="sxs-lookup"><span data-stu-id="f4d30-104">This procedure shows you how to create a sales agreement that commits one of your customers to buy a product for an</span></span>

<span data-ttu-id="f4d30-105">iepriekš norunāto summu, par to saņemot īpašas atlaides.</span><span class="sxs-lookup"><span data-stu-id="f4d30-105">agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="f4d30-106">Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="f4d30-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="f4d30-107">Pārdošanas līguma virsraksta iestatīšana</span><span class="sxs-lookup"><span data-stu-id="f4d30-107">Set up sales agreement header</span></span>
1. <span data-ttu-id="f4d30-108">Dodieties uz sadaļu Pārdošana un mārketings > Pārdošanas līgumi > Pārdošanas līgumi.</span><span class="sxs-lookup"><span data-stu-id="f4d30-108">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="f4d30-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="f4d30-109">Click New.</span></span>
3. <span data-ttu-id="f4d30-110">Laukā Debitora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f4d30-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f4d30-111">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f4d30-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f4d30-112">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f4d30-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f4d30-113">Laukā Pārdošanas līgumu klasifikācija noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="f4d30-113">In the Sales agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f4d30-114">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f4d30-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f4d30-115">Izvērsiet sadaļu Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="f4d30-115">Expand the General section.</span></span>
9. <span data-ttu-id="f4d30-116">Laukā Noklusējuma saistības atlasiet Uz preču vērtību attiecināmas saistības.</span><span class="sxs-lookup"><span data-stu-id="f4d30-116">In the Default commitment field, select 'Product value commitment'.</span></span>
    * <span data-ttu-id="f4d30-117">Saistību veids ir obligāts kritērijs, kas ir jāpiešķir līgumam, lai definētu, kā līgums tiks izpildīts.</span><span class="sxs-lookup"><span data-stu-id="f4d30-117">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="f4d30-118">Izmantojot četrus iepriekš definētus veidus, var iestatīt klienta saistību mērķi, kas tiek izteikts kā daudzums vai vērtība.</span><span class="sxs-lookup"><span data-stu-id="f4d30-118">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="f4d30-119">Daudzuma saistību veidu var lietot tikai noteiktām precēm, bet vērtību veidus var lietot konkrētu vai vispārīga veida preču pārdošanā.</span><span class="sxs-lookup"><span data-stu-id="f4d30-119">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
10. <span data-ttu-id="f4d30-120">Laukā Beigu datums iestatiet datumu nākotnē, kad beidzas līguma termiņš.</span><span class="sxs-lookup"><span data-stu-id="f4d30-120">In the Expiration date field, set the date to a future date when you want the agreement to expire.</span></span>
11. <span data-ttu-id="f4d30-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f4d30-121">Click OK.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="f4d30-122">Uz preču vērtību attiecināmo saistību rindu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="f4d30-122">Set up product value commitment lines</span></span>
1. <span data-ttu-id="f4d30-123">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="f4d30-123">Click Add line.</span></span>
2. <span data-ttu-id="f4d30-124">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f4d30-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="f4d30-125">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f4d30-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="f4d30-126">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f4d30-126">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f4d30-127">Līgumam izvēlēto saistību veids ietekmē to, kāda veida informāciju var ievadīt līguma rindās.</span><span class="sxs-lookup"><span data-stu-id="f4d30-127">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="f4d30-128">Piemēram, vērtību līgumam ir jānorāda kopējā neto summa (saskaņotajā valūtā), par kuru debitors apņēmās nopirkt no jums preces.</span><span class="sxs-lookup"><span data-stu-id="f4d30-128">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="f4d30-129">Šajā piemērā rindas lauks Daudzums un Vienības nav pieejams, jo debitoram tiek izveidots līgums saistībā ar preces ar konkrētu vērtību iegādi.</span><span class="sxs-lookup"><span data-stu-id="f4d30-129">In this example the Quantity and Unit fields on the line are unavailable because you’re creating an agreement for the customer to buy a specific value of a product.</span></span>   
5. <span data-ttu-id="f4d30-130">Laukā Neto summa ievadiet naudas summu, ko debitors apņēmās samaksāt.</span><span class="sxs-lookup"><span data-stu-id="f4d30-130">In the Net amount field, enter the monetary amount that the customer has committed to buying.</span></span>
6. <span data-ttu-id="f4d30-131">Laukā Atlaides procents ievadiet procentuālo vērtību, kas tiks lietota debitora pārdošanas pasūtījuma rindām, kas ir piesaistītas ar šim līgumam.</span><span class="sxs-lookup"><span data-stu-id="f4d30-131">In the Discount percent field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
7. <span data-ttu-id="f4d30-132">Izvērsiet sadaļu Detalizēta informācija par rindu.</span><span class="sxs-lookup"><span data-stu-id="f4d30-132">Expand the Line details section.</span></span>
8. <span data-ttu-id="f4d30-133">Laukā Sasniegts maksimums atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="f4d30-133">Select Yes in the Max is enforced field.</span></span>
    * <span data-ttu-id="f4d30-134">Atlasot Sasniegts maksimums, visu to pārdošanas pasūtījuma rindu kopsumma, kurās izmanto īpašas saistību cenas, atlaides un/vai maksāšanas nosacījumus, nedrīkst pārsniegt saistībās norādīto summu.</span><span class="sxs-lookup"><span data-stu-id="f4d30-134">Selecting Max is enforced means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    * <span data-ttu-id="f4d30-135">Minimālā un maksimālā izlaišanas summa norāda to vērtību diapazonu, kas ir jāpārdod katrā pārdošanas pasūtījumā, kas izmanto atlasīto līgumu.</span><span class="sxs-lookup"><span data-stu-id="f4d30-135">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
9. <span data-ttu-id="f4d30-136">Izvērsiet sadaļu Pārdošanas līguma virsraksts.</span><span class="sxs-lookup"><span data-stu-id="f4d30-136">Expand the Sales agreement header section.</span></span>
    * <span data-ttu-id="f4d30-137">Ja vien līguma statuss nav iestatīts uz Ir spēkā, pārdošanas pasūtījumus nevar saistīt ar līgumu, tādēļ tie nevar sekmēt šī līguma izpildi.</span><span class="sxs-lookup"><span data-stu-id="f4d30-137">Unless the status of the agreement is set to Effective, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="f4d30-138">Šajā posmā statusu var mainīt manuāli.</span><span class="sxs-lookup"><span data-stu-id="f4d30-138">You can change the status manually at this stage.</span></span> <span data-ttu-id="f4d30-139">Tomēr statuss parasti ir jāmaina tad, kad apstiprināt debitora līgumu.</span><span class="sxs-lookup"><span data-stu-id="f4d30-139">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
10. <span data-ttu-id="f4d30-140">Darbības rūtī noklikšķiniet uz vienuma Pārdošanas līgums.</span><span class="sxs-lookup"><span data-stu-id="f4d30-140">On the Action Pane, click Sales agreement.</span></span>
11. <span data-ttu-id="f4d30-141">Noklikšķiniet uz Apstiprinājums.</span><span class="sxs-lookup"><span data-stu-id="f4d30-141">Click Confirmation.</span></span>
    * <span data-ttu-id="f4d30-142">Pārliecinieties, vai opcijai Atzīmēt līgumu kā efektīvu ir iestatīts Jā.</span><span class="sxs-lookup"><span data-stu-id="f4d30-142">Make sure that the Mark agreement as effective option is set to Yes.</span></span>  
12. <span data-ttu-id="f4d30-143">Laukā Drukāt pārskatu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="f4d30-143">Select Yes in the Print report field.</span></span>
13. <span data-ttu-id="f4d30-144">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f4d30-144">Click OK.</span></span>
14. <span data-ttu-id="f4d30-145">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f4d30-145">Close the page.</span></span>
    * <span data-ttu-id="f4d30-146">Tagad līgums ir spēkā un varat sākt piesaistīt līgumam debitora pasūtījumus atbilstoši mērķim.</span><span class="sxs-lookup"><span data-stu-id="f4d30-146">The agreement is now effective and you can start linking the customer's orders to the agreement, to offset against the committed target.</span></span>  


