--- 
title: "Pirkšanas izpildpasūtījumu izveide no pirkšanas līguma"
description: "Šajā procedūrā parādīts, kā izmantot pirkšanas līgumu, veidojot pirkšanas pasūtījumu."
author: mkirknel
manager: AnnBe
ms.date: 12/04/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cecda03dd4d224d4319f2b0b196560389bb54195
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-release-order-from-a-purchase-agreement"></a><span data-ttu-id="d9321-103">Pirkšanas izpildpasūtījumu izveide no pirkšanas līguma</span><span class="sxs-lookup"><span data-stu-id="d9321-103">Create a purchase release order from a purchase agreement</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d9321-104">Šajā procedūrā parādīts, kā izmantot pirkšanas līgumu, veidojot pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="d9321-104">This procedure shows how to use a purchase agreement when you create a purchase order.</span></span> <span data-ttu-id="d9321-105">Pirkšanas līgums jālieto, veidojot pirkšanas pasūtījumu, jo pastāv vispārīgi nosacījumi, kas jāiekopē pirkšanas pasūtījuma virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="d9321-105">The purchase agreement has to be applied when you create the purchase order because there are general terms that should be copied to the purchase order header.</span></span> <span data-ttu-id="d9321-106">Šo uzdevumu parasti veic pirkšanas aģents.</span><span class="sxs-lookup"><span data-stu-id="d9321-106">Typically this task would be carried out by a purchasing agent.</span></span> <span data-ttu-id="d9321-107">Kā šī ceļveža priekšnosacījums, jums jābūt spēkā pirkšanas līgumam ar uz preču daudzumu attiecināmam saistībām kreditoram un krājumiem.</span><span class="sxs-lookup"><span data-stu-id="d9321-107">As a prerequisite for this guide, you must have an effective purchase agreement with a product quantity commitment for a vendor and items.</span></span> <span data-ttu-id="d9321-108">To pašu procedūru var izmantot, ja ir pirkšanas līgums ar cita veida saistībām.</span><span class="sxs-lookup"><span data-stu-id="d9321-108">The same procedure can be used if you have a purchase agreement with other types of commitments.</span></span> <span data-ttu-id="d9321-109">Šo ceļvedi varat izpildīt demonstrācijas datu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="d9321-109">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="d9321-110">Ja jūs izmantojat USMF, vispirms var palaist ceļvedi "Pirkšanas līguma izveide", lai iestatītu šim ceļvedim vajadzīgos priekšnoteikumus.</span><span class="sxs-lookup"><span data-stu-id="d9321-110">If you’re using USMF, you can run the “Create a purchase agreement” guide first to set up the necessary preconditions for this guide.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="d9321-111">Pirkšanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="d9321-111">Create a purchase order</span></span>
1. <span data-ttu-id="d9321-112">Atveriet pirkšanas pasūtījumu sagatavošanas darbvietu.</span><span class="sxs-lookup"><span data-stu-id="d9321-112">Open the purchase order preparation workspace.</span></span>
2. <span data-ttu-id="d9321-113">Noklikšķiniet uz Jauns pirkšanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="d9321-113">Click New purchase order.</span></span>
3. <span data-ttu-id="d9321-114">Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d9321-114">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d9321-115">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d9321-115">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d9321-116">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d9321-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d9321-117">Pārslēdziet sadaļas Vispārīgi paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="d9321-117">Toggle the expansion of the General section.</span></span>
7. <span data-ttu-id="d9321-118">Laukā Pirkšanas līgums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="d9321-118">In the Purchase agreement field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d9321-119">Visi pieejamie kreditora līgumi ir uzskaitīti šeit.</span><span class="sxs-lookup"><span data-stu-id="d9321-119">All available agreements for the vendor are listed here.</span></span> <span data-ttu-id="d9321-120">Atrodiet efektīvo līgumu, kuru vēlaties izmantot.</span><span class="sxs-lookup"><span data-stu-id="d9321-120">Find the effective agreement that you want to use.</span></span>  
8. <span data-ttu-id="d9321-121">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d9321-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d9321-122">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="d9321-122">Click Yes.</span></span>
10. <span data-ttu-id="d9321-123">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d9321-123">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="d9321-124">Rindas pievienošana</span><span class="sxs-lookup"><span data-stu-id="d9321-124">Add a line</span></span>
1. <span data-ttu-id="d9321-125">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d9321-125">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="d9321-126">Ja saistībās ir noteikta krājumu vai novietojuma dimensijas, lai izmantotu līgumu, tās pašas vērtības ir jāievada pirkšanas pasūtījuma rindā.</span><span class="sxs-lookup"><span data-stu-id="d9321-126">If there are specific inventory or location dimensions on the commitment you must enter the same values on the purchase order line to make use of the agreement.</span></span>  
2. <span data-ttu-id="d9321-127">Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d9321-127">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d9321-128">Vieta var jau būt aizpildīta ar noklusēto vērtību no pasūtījuma vai kreditora.</span><span class="sxs-lookup"><span data-stu-id="d9321-128">The site may already be populated with the default value from the order, or from the vendor.</span></span> <span data-ttu-id="d9321-129">Ja tā notiek, izlaidiet šo darbību.</span><span class="sxs-lookup"><span data-stu-id="d9321-129">If this is the case, skip this step.</span></span>  
3. <span data-ttu-id="d9321-130">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d9321-130">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="d9321-131">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d9321-131">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d9321-132">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="d9321-132">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="d9321-133">Pārbaudiet, vai no saistībām tiek nokopēta cena.</span><span class="sxs-lookup"><span data-stu-id="d9321-133">Validate that the price is copied from the commitment.</span></span>  

## <a name="look-up-the-commitment"></a><span data-ttu-id="d9321-134">Saistību uzmeklēšana</span><span class="sxs-lookup"><span data-stu-id="d9321-134">Look up the commitment</span></span>
1. <span data-ttu-id="d9321-135">Noklikšķiniet uz Labot rindu.</span><span class="sxs-lookup"><span data-stu-id="d9321-135">Click Update line.</span></span>
2. <span data-ttu-id="d9321-136">Noklikšķiniet uz Piesaistīts.</span><span class="sxs-lookup"><span data-stu-id="d9321-136">Click Attached.</span></span>
    * <span data-ttu-id="d9321-137">Šeit var saņemt detalizētu informāciju par pirkšanas līgumu.</span><span class="sxs-lookup"><span data-stu-id="d9321-137">Here you can get details for the purchase agreement.</span></span> <span data-ttu-id="d9321-138">Piemēram, jūs varat redzēt cenu un vai cena un atlaide ir fiksētas, kas nozīmē, ka, mainot cenu vai atlaidi pirkšanas pasūtījumā uz citu vērtību, nekā saistībās, sistēma noņems saiti, lai pirkšanas pasūtījuma rinda neizpildītu saistības.</span><span class="sxs-lookup"><span data-stu-id="d9321-138">For example, you can see the price and whether the price and discount are fixed, which means that if you change price or discount on the purchase order to a different value than on the commitment, the system will remove the link so the purchase order line does not fulfill the commitment.</span></span> <span data-ttu-id="d9321-139">Varat apskatīt arī, vai ir atlasīta opcija Sasniegts maksimums, kas nozīmē, ka saistību daudzumu nevar pārsniegt, summējot visus pirkumus, kas izpilda saistības.</span><span class="sxs-lookup"><span data-stu-id="d9321-139">You can also see if the Max is enforced option is selected, which means that the quantity on the commitment cannot be exceeded by summing all of the purchases that fulfill the commitment.</span></span>  
3. <span data-ttu-id="d9321-140">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d9321-140">Close the page.</span></span>

## <a name="look-up-the-purchase-agreement"></a><span data-ttu-id="d9321-141">Pirkšanas līguma uzmeklēšana</span><span class="sxs-lookup"><span data-stu-id="d9321-141">Look up the purchase agreement</span></span>
1. <span data-ttu-id="d9321-142">Darbību rūtī noklikšķiniet uz Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="d9321-142">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="d9321-143">Noklikšķiniet uz Pirkšanas līgums.</span><span class="sxs-lookup"><span data-stu-id="d9321-143">Click Purchase agreement.</span></span>
3. <span data-ttu-id="d9321-144">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d9321-144">Close the page.</span></span>
4. <span data-ttu-id="d9321-145">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d9321-145">Close the page.</span></span>


