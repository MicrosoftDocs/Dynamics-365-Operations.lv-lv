---
title: Pirkšanas izpildpasūtījumu izveide no pirkšanas līguma
description: Šajā procedūrā parādīts, kā izmantot pirkšanas līgumu, veidojot pirkšanas pasūtījumu.
author: kamaybac
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd3f837590cd7fe09ad385d0baac6c16fcf145d0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812263"
---
# <a name="create-a-purchase-release-order-from-a-purchase-agreement"></a><span data-ttu-id="1d117-103">Pirkšanas izpildpasūtījumu izveide no pirkšanas līguma</span><span class="sxs-lookup"><span data-stu-id="1d117-103">Create a purchase release order from a purchase agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1d117-104">Šajā procedūrā parādīts, kā izmantot pirkšanas līgumu, veidojot pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="1d117-104">This procedure shows how to use a purchase agreement when you create a purchase order.</span></span> <span data-ttu-id="1d117-105">Pirkšanas līgums jālieto, veidojot pirkšanas pasūtījumu, jo pastāv vispārīgi nosacījumi, kas jāiekopē pirkšanas pasūtījuma virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="1d117-105">The purchase agreement has to be applied when you create the purchase order because there are general terms that should be copied to the purchase order header.</span></span> <span data-ttu-id="1d117-106">Šo uzdevumu parasti veic pirkšanas aģents.</span><span class="sxs-lookup"><span data-stu-id="1d117-106">Typically this task would be carried out by a purchasing agent.</span></span> <span data-ttu-id="1d117-107">Kā šī ceļveža priekšnosacījums, jums jābūt spēkā pirkšanas līgumam ar uz preču daudzumu attiecināmam saistībām kreditoram un krājumiem.</span><span class="sxs-lookup"><span data-stu-id="1d117-107">As a prerequisite for this guide, you must have an effective purchase agreement with a product quantity commitment for a vendor and items.</span></span> <span data-ttu-id="1d117-108">To pašu procedūru var izmantot, ja ir pirkšanas līgums ar cita veida saistībām.</span><span class="sxs-lookup"><span data-stu-id="1d117-108">The same procedure can be used if you have a purchase agreement with other types of commitments.</span></span> <span data-ttu-id="1d117-109">Šo ceļvedi varat izpildīt paraugdatu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="1d117-109">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="1d117-110">Ja jūs izmantojat USMF, vispirms var palaist ceļvedi "Pirkšanas līguma izveide", lai iestatītu šim ceļvedim vajadzīgos priekšnoteikumus.</span><span class="sxs-lookup"><span data-stu-id="1d117-110">If you're using USMF, you can run the "Create a purchase agreement" guide first to set up the necessary preconditions for this guide.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="1d117-111">Pirkšanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="1d117-111">Create a purchase order</span></span>
1. <span data-ttu-id="1d117-112">**Navigācijas rūtī** ejiet uz **Darbvietas > Pirkšanas pasūtījuma sagatavošana**.</span><span class="sxs-lookup"><span data-stu-id="1d117-112">In the **Navigation pane**, go to **Workspaces > Purchase order preparation**.</span></span> 
2. <span data-ttu-id="1d117-113">Klikšķiniet uz **Jauns pirkšanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="1d117-113">Click **New purchase order**.</span></span>
3. <span data-ttu-id="1d117-114">Laukā **Kreditora konts** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="1d117-114">In the **Vendor account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="1d117-115">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="1d117-115">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="1d117-116">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1d117-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="1d117-117">Izvērsiet kopsavilkuma cilni **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="1d117-117">Expand the **General** fastTab.</span></span>
7. <span data-ttu-id="1d117-118">Laukā **Pirkuma līgums** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="1d117-118">In the **Purchase agreement** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="1d117-119">Visi pieejamie kreditora līgumi ir uzskaitīti šeit.</span><span class="sxs-lookup"><span data-stu-id="1d117-119">All available agreements for the vendor are listed here.</span></span> <span data-ttu-id="1d117-120">Atrodiet efektīvo līgumu, kuru vēlaties izmantot.</span><span class="sxs-lookup"><span data-stu-id="1d117-120">Find the effective agreement that you want to use.</span></span>  
8. <span data-ttu-id="1d117-121">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1d117-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="1d117-122">Noklikšķiniet uz pogas **Jā**.</span><span class="sxs-lookup"><span data-stu-id="1d117-122">Click **Yes**.</span></span>
10. <span data-ttu-id="1d117-123">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1d117-123">Click **OK**.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="1d117-124">Rindas pievienošana</span><span class="sxs-lookup"><span data-stu-id="1d117-124">Add a line</span></span>
1. <span data-ttu-id="1d117-125">Laukā **Krājuma kods** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="1d117-125">In the **Item number** field, type a value.</span></span> <span data-ttu-id="1d117-126">Ja saistībās ir noteikta krājumu vai novietojuma dimensijas, lai izmantotu līgumu, tās pašas vērtības ir jāievada pirkšanas pasūtījuma rindā.</span><span class="sxs-lookup"><span data-stu-id="1d117-126">If there are specific inventory or location dimensions on the commitment you must enter the same values on the purchase order line to make use of the agreement.</span></span>  
2. <span data-ttu-id="1d117-127">Laukā **Vieta** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="1d117-127">In the **Site** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="1d117-128">Vieta var jau būt aizpildīta ar noklusēto vērtību no pasūtījuma vai kreditora.</span><span class="sxs-lookup"><span data-stu-id="1d117-128">The site may already be populated with the default value from the order, or from the vendor.</span></span> <span data-ttu-id="1d117-129">Ja tā notiek, izlaidiet šo darbību.</span><span class="sxs-lookup"><span data-stu-id="1d117-129">If this is the case, skip this step.</span></span>  
3. <span data-ttu-id="1d117-130">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="1d117-130">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="1d117-131">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1d117-131">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="1d117-132">Laukā **Daudzums** ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="1d117-132">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="1d117-133">Pārbaudiet, vai no saistībām tiek nokopēta cena.</span><span class="sxs-lookup"><span data-stu-id="1d117-133">Validate that the price is copied from the commitment.</span></span>  

## <a name="look-up-the-commitment"></a><span data-ttu-id="1d117-134">Saistību uzmeklēšana</span><span class="sxs-lookup"><span data-stu-id="1d117-134">Look up the commitment</span></span>
1. <span data-ttu-id="1d117-135">Noklikšķiniet uz **Atjaunināt rindu**.</span><span class="sxs-lookup"><span data-stu-id="1d117-135">Click **Update line**.</span></span>
2. <span data-ttu-id="1d117-136">Noklikšķiniet uz **Pievienots**.</span><span class="sxs-lookup"><span data-stu-id="1d117-136">Click **Attached**.</span></span> <span data-ttu-id="1d117-137">Šeit var saņemt detalizētu informāciju par pirkšanas līgumu.</span><span class="sxs-lookup"><span data-stu-id="1d117-137">Here you can get details for the purchase agreement.</span></span> <span data-ttu-id="1d117-138">Piemēram, jūs varat redzēt cenu un vai cena un atlaide ir fiksētas, kas nozīmē, ka, mainot cenu vai atlaidi pirkšanas pasūtījumā uz citu vērtību, nekā saistībās, sistēma noņems saiti, lai pirkšanas pasūtījuma rinda neizpildītu saistības.</span><span class="sxs-lookup"><span data-stu-id="1d117-138">For example, you can see the price and whether the price and discount are fixed, which means that if you change price or discount on the purchase order to a different value than on the commitment, the system will remove the link so the purchase order line does not fulfill the commitment.</span></span> <span data-ttu-id="1d117-139">Varat apskatīt arī, vai ir atlasīta opcija Sasniegts maksimums, kas nozīmē, ka saistību daudzumu nevar pārsniegt, summējot visus pirkumus, kas izpilda saistības.</span><span class="sxs-lookup"><span data-stu-id="1d117-139">You can also see if the Max is enforced option is selected, which means that the quantity on the commitment cannot be exceeded by summing all of the purchases that fulfill the commitment.</span></span>  
3. <span data-ttu-id="1d117-140">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1d117-140">Close the page.</span></span>

## <a name="look-up-the-purchase-agreement"></a><span data-ttu-id="1d117-141">Pirkšanas līguma uzmeklēšana</span><span class="sxs-lookup"><span data-stu-id="1d117-141">Look up the purchase agreement</span></span>
1. <span data-ttu-id="1d117-142">**Darbību rūtī** noklikšķiniet uz **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="1d117-142">On the **Action Pane**, click **General**.</span></span>
2. <span data-ttu-id="1d117-143">Klikšķiniet uz **Pirkuma līgums**.</span><span class="sxs-lookup"><span data-stu-id="1d117-143">Click **Purchase agreement**.</span></span>
3. <span data-ttu-id="1d117-144">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1d117-144">Close the page.</span></span>
4. <span data-ttu-id="1d117-145">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1d117-145">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]