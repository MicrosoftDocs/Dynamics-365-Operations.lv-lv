---
title: Pārdošanas līgumu ievade
description: Šajā procedūrā ir parādīts, kā izveidot pārdošanas līgumu, saskaņā ar kuru kāds no jūsu debitoriem apņemsies iegādāties preces par iepriekš norunāto summu, par to saņemot īpašas atlaides.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c415faaf68fda677f08305dce0ed3f2ed32ee050
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834104"
---
# <a name="enter-sales-agreements"></a><span data-ttu-id="cb75b-103">Pārdošanas līgumu ievade</span><span class="sxs-lookup"><span data-stu-id="cb75b-103">Enter sales agreements</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cb75b-104">Šajā procedūrā ir parādīts, kā izveidot pārdošanas līgumu, saskaņā ar kuru kāds no jūsu debitoriem apņemsies iegādāties preces par iepriekš norunāto summu, par to saņemot īpašas atlaides.</span><span class="sxs-lookup"><span data-stu-id="cb75b-104">This procedure shows you how to create a sales agreement that commits one of your customers to buy a product for an agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="cb75b-105">Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="cb75b-105">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="cb75b-106">Pārdošanas līguma virsraksta iestatīšana</span><span class="sxs-lookup"><span data-stu-id="cb75b-106">Set up sales agreement header</span></span>
1. <span data-ttu-id="cb75b-107">Dodieties uz sadaļu Pārdošana un mārketings > Pārdošanas līgumi > Pārdošanas līgumi.</span><span class="sxs-lookup"><span data-stu-id="cb75b-107">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="cb75b-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="cb75b-108">Click New.</span></span>
3. <span data-ttu-id="cb75b-109">Laukā Debitora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="cb75b-109">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="cb75b-110">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="cb75b-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="cb75b-111">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="cb75b-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="cb75b-112">Laukā Pārdošanas līgumu klasifikācija noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="cb75b-112">In the Sales agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="cb75b-113">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="cb75b-113">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="cb75b-114">Izvērsiet sadaļu Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="cb75b-114">Expand the General section.</span></span>
9. <span data-ttu-id="cb75b-115">Laukā Noklusējuma saistības atlasiet Uz preču vērtību attiecināmas saistības.</span><span class="sxs-lookup"><span data-stu-id="cb75b-115">In the Default commitment field, select 'Product value commitment'.</span></span>
    * <span data-ttu-id="cb75b-116">Saistību veids ir obligāts kritērijs, kas ir jāpiešķir līgumam, lai definētu, kā līgums tiks izpildīts.</span><span class="sxs-lookup"><span data-stu-id="cb75b-116">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="cb75b-117">Izmantojot četrus iepriekš definētus veidus, var iestatīt klienta saistību mērķi, kas tiek izteikts kā daudzums vai vērtība.</span><span class="sxs-lookup"><span data-stu-id="cb75b-117">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="cb75b-118">Daudzuma saistību veidu var lietot tikai noteiktām precēm, bet vērtību veidus var lietot konkrētu vai vispārīga veida preču pārdošanā.</span><span class="sxs-lookup"><span data-stu-id="cb75b-118">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
10. <span data-ttu-id="cb75b-119">Laukā Beigu datums iestatiet datumu nākotnē, kad beidzas līguma termiņš.</span><span class="sxs-lookup"><span data-stu-id="cb75b-119">In the Expiration date field, set the date to a future date when you want the agreement to expire.</span></span>
11. <span data-ttu-id="cb75b-120">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="cb75b-120">Click OK.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="cb75b-121">Uz preču vērtību attiecināmo saistību rindu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="cb75b-121">Set up product value commitment lines</span></span>
1. <span data-ttu-id="cb75b-122">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="cb75b-122">Click Add line.</span></span>
2. <span data-ttu-id="cb75b-123">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="cb75b-123">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="cb75b-124">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="cb75b-124">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="cb75b-125">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="cb75b-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cb75b-126">Līgumam izvēlēto saistību veids ietekmē to, kāda veida informāciju var ievadīt līguma rindās.</span><span class="sxs-lookup"><span data-stu-id="cb75b-126">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="cb75b-127">Piemēram, vērtību līgumam ir jānorāda kopējā neto summa (saskaņotajā valūtā), par kuru debitors apņēmās nopirkt no jums preces.</span><span class="sxs-lookup"><span data-stu-id="cb75b-127">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="cb75b-128">Šajā piemērā rindas lauks Daudzums un Vienības nav pieejams, jo debitoram tiek izveidots līgums saistībā ar preces ar konkrētu vērtību iegādi.</span><span class="sxs-lookup"><span data-stu-id="cb75b-128">In this example the Quantity and Unit fields on the line are unavailable because you’re creating an agreement for the customer to buy a specific value of a product.</span></span>   
5. <span data-ttu-id="cb75b-129">Laukā Neto summa ievadiet naudas summu, ko debitors apņēmās samaksāt.</span><span class="sxs-lookup"><span data-stu-id="cb75b-129">In the Net amount field, enter the monetary amount that the customer has committed to buying.</span></span>
6. <span data-ttu-id="cb75b-130">Laukā Atlaides procents ievadiet procentuālo vērtību, kas tiks lietota debitora pārdošanas pasūtījuma rindām, kas ir piesaistītas ar šim līgumam.</span><span class="sxs-lookup"><span data-stu-id="cb75b-130">In the Discount percent field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
7. <span data-ttu-id="cb75b-131">Izvērsiet sadaļu Detalizēta informācija par rindu.</span><span class="sxs-lookup"><span data-stu-id="cb75b-131">Expand the Line details section.</span></span>
8. <span data-ttu-id="cb75b-132">Laukā Sasniegts maksimums atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="cb75b-132">Select Yes in the Max is enforced field.</span></span>
    * <span data-ttu-id="cb75b-133">Atlasot Sasniegts maksimums, visu to pārdošanas pasūtījuma rindu kopsumma, kurās izmanto īpašas saistību cenas, atlaides un/vai maksāšanas nosacījumus, nedrīkst pārsniegt saistībās norādīto summu.</span><span class="sxs-lookup"><span data-stu-id="cb75b-133">Selecting Max is enforced means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    * <span data-ttu-id="cb75b-134">Minimālā un maksimālā izlaišanas summa norāda to vērtību diapazonu, kas ir jāpārdod katrā pārdošanas pasūtījumā, kas izmanto atlasīto līgumu.</span><span class="sxs-lookup"><span data-stu-id="cb75b-134">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
9. <span data-ttu-id="cb75b-135">Izvērsiet sadaļu Pārdošanas līguma virsraksts.</span><span class="sxs-lookup"><span data-stu-id="cb75b-135">Expand the Sales agreement header section.</span></span>
    * <span data-ttu-id="cb75b-136">Ja vien līguma statuss nav iestatīts uz Ir spēkā, pārdošanas pasūtījumus nevar saistīt ar līgumu, tādēļ tie nevar sekmēt šī līguma izpildi.</span><span class="sxs-lookup"><span data-stu-id="cb75b-136">Unless the status of the agreement is set to Effective, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="cb75b-137">Šajā posmā statusu var mainīt manuāli.</span><span class="sxs-lookup"><span data-stu-id="cb75b-137">You can change the status manually at this stage.</span></span> <span data-ttu-id="cb75b-138">Tomēr statuss parasti ir jāmaina tad, kad apstiprināt debitora līgumu.</span><span class="sxs-lookup"><span data-stu-id="cb75b-138">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
10. <span data-ttu-id="cb75b-139">Darbības rūtī noklikšķiniet uz vienuma Pārdošanas līgums.</span><span class="sxs-lookup"><span data-stu-id="cb75b-139">On the Action Pane, click Sales agreement.</span></span>
11. <span data-ttu-id="cb75b-140">Noklikšķiniet uz Apstiprinājums.</span><span class="sxs-lookup"><span data-stu-id="cb75b-140">Click Confirmation.</span></span>
    * <span data-ttu-id="cb75b-141">Pārliecinieties, vai opcijai Atzīmēt līgumu kā efektīvu ir iestatīts Jā.</span><span class="sxs-lookup"><span data-stu-id="cb75b-141">Make sure that the Mark agreement as effective option is set to Yes.</span></span>  
12. <span data-ttu-id="cb75b-142">Laukā Drukāt pārskatu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="cb75b-142">Select Yes in the Print report field.</span></span>
13. <span data-ttu-id="cb75b-143">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="cb75b-143">Click OK.</span></span>
14. <span data-ttu-id="cb75b-144">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cb75b-144">Close the page.</span></span>
    * <span data-ttu-id="cb75b-145">Tagad līgums ir spēkā un varat sākt piesaistīt līgumam debitora pasūtījumus atbilstoši mērķim.</span><span class="sxs-lookup"><span data-stu-id="cb75b-145">The agreement is now effective and you can start linking the customer's orders to the agreement, to offset against the committed target.</span></span>  

