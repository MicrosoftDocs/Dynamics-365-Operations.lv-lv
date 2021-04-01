---
title: Pirkšanas izpildpasūtījumu izveide no pirkšanas līguma
description: Šajā procedūrā parādīts, kā izmantot pirkšanas līgumu, veidojot pirkšanas pasūtījumu.
author: RichardLuan
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f4e9a0551c0755fd006fc030d2e1bf4f28efe951
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211961"
---
# <a name="create-a-purchase-release-order-from-a-purchase-agreement"></a><span data-ttu-id="716d2-103">Pirkšanas izpildpasūtījumu izveide no pirkšanas līguma</span><span class="sxs-lookup"><span data-stu-id="716d2-103">Create a purchase release order from a purchase agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="716d2-104">Šajā procedūrā parādīts, kā izmantot pirkšanas līgumu, veidojot pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="716d2-104">This procedure shows how to use a purchase agreement when you create a purchase order.</span></span> <span data-ttu-id="716d2-105">Pirkšanas līgums jālieto, veidojot pirkšanas pasūtījumu, jo pastāv vispārīgi nosacījumi, kas jāiekopē pirkšanas pasūtījuma virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="716d2-105">The purchase agreement has to be applied when you create the purchase order because there are general terms that should be copied to the purchase order header.</span></span> <span data-ttu-id="716d2-106">Šo uzdevumu parasti veic pirkšanas aģents.</span><span class="sxs-lookup"><span data-stu-id="716d2-106">Typically this task would be carried out by a purchasing agent.</span></span> <span data-ttu-id="716d2-107">Kā šī ceļveža priekšnosacījums, jums jābūt spēkā pirkšanas līgumam ar uz preču daudzumu attiecināmam saistībām kreditoram un krājumiem.</span><span class="sxs-lookup"><span data-stu-id="716d2-107">As a prerequisite for this guide, you must have an effective purchase agreement with a product quantity commitment for a vendor and items.</span></span> <span data-ttu-id="716d2-108">To pašu procedūru var izmantot, ja ir pirkšanas līgums ar cita veida saistībām.</span><span class="sxs-lookup"><span data-stu-id="716d2-108">The same procedure can be used if you have a purchase agreement with other types of commitments.</span></span> <span data-ttu-id="716d2-109">Šo ceļvedi varat izpildīt paraugdatu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="716d2-109">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="716d2-110">Ja jūs izmantojat USMF, vispirms var palaist ceļvedi "Pirkšanas līguma izveide", lai iestatītu šim ceļvedim vajadzīgos priekšnoteikumus.</span><span class="sxs-lookup"><span data-stu-id="716d2-110">If you're using USMF, you can run the "Create a purchase agreement" guide first to set up the necessary preconditions for this guide.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="716d2-111">Pirkšanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="716d2-111">Create a purchase order</span></span>
1. <span data-ttu-id="716d2-112">**Navigācijas rūtī** ejiet uz **Darbvietas > Pirkšanas pasūtījuma sagatavošana**.</span><span class="sxs-lookup"><span data-stu-id="716d2-112">In the **Navigation pane**, go to **Workspaces > Purchase order preparation**.</span></span> 
2. <span data-ttu-id="716d2-113">Klikšķiniet uz **Jauns pirkšanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="716d2-113">Click **New purchase order**.</span></span>
3. <span data-ttu-id="716d2-114">Laukā **Kreditora konts** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="716d2-114">In the **Vendor account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="716d2-115">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="716d2-115">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="716d2-116">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="716d2-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="716d2-117">Izvērsiet kopsavilkuma cilni **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="716d2-117">Expand the **General** fastTab.</span></span>
7. <span data-ttu-id="716d2-118">Laukā **Pirkuma līgums** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="716d2-118">In the **Purchase agreement** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="716d2-119">Visi pieejamie kreditora līgumi ir uzskaitīti šeit.</span><span class="sxs-lookup"><span data-stu-id="716d2-119">All available agreements for the vendor are listed here.</span></span> <span data-ttu-id="716d2-120">Atrodiet efektīvo līgumu, kuru vēlaties izmantot.</span><span class="sxs-lookup"><span data-stu-id="716d2-120">Find the effective agreement that you want to use.</span></span>  
8. <span data-ttu-id="716d2-121">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="716d2-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="716d2-122">Noklikšķiniet uz pogas **Jā**.</span><span class="sxs-lookup"><span data-stu-id="716d2-122">Click **Yes**.</span></span>
10. <span data-ttu-id="716d2-123">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="716d2-123">Click **OK**.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="716d2-124">Rindas pievienošana</span><span class="sxs-lookup"><span data-stu-id="716d2-124">Add a line</span></span>
1. <span data-ttu-id="716d2-125">Laukā **Krājuma kods** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="716d2-125">In the **Item number** field, type a value.</span></span> <span data-ttu-id="716d2-126">Ja saistībās ir noteikta krājumu vai novietojuma dimensijas, lai izmantotu līgumu, tās pašas vērtības ir jāievada pirkšanas pasūtījuma rindā.</span><span class="sxs-lookup"><span data-stu-id="716d2-126">If there are specific inventory or location dimensions on the commitment you must enter the same values on the purchase order line to make use of the agreement.</span></span>  
2. <span data-ttu-id="716d2-127">Laukā **Vieta** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="716d2-127">In the **Site** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="716d2-128">Vieta var jau būt aizpildīta ar noklusēto vērtību no pasūtījuma vai kreditora.</span><span class="sxs-lookup"><span data-stu-id="716d2-128">The site may already be populated with the default value from the order, or from the vendor.</span></span> <span data-ttu-id="716d2-129">Ja tā notiek, izlaidiet šo darbību.</span><span class="sxs-lookup"><span data-stu-id="716d2-129">If this is the case, skip this step.</span></span>  
3. <span data-ttu-id="716d2-130">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="716d2-130">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="716d2-131">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="716d2-131">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="716d2-132">Laukā **Daudzums** ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="716d2-132">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="716d2-133">Pārbaudiet, vai no saistībām tiek nokopēta cena.</span><span class="sxs-lookup"><span data-stu-id="716d2-133">Validate that the price is copied from the commitment.</span></span>  

## <a name="look-up-the-commitment"></a><span data-ttu-id="716d2-134">Saistību uzmeklēšana</span><span class="sxs-lookup"><span data-stu-id="716d2-134">Look up the commitment</span></span>
1. <span data-ttu-id="716d2-135">Noklikšķiniet uz **Atjaunināt rindu**.</span><span class="sxs-lookup"><span data-stu-id="716d2-135">Click **Update line**.</span></span>
2. <span data-ttu-id="716d2-136">Noklikšķiniet uz **Pievienots**.</span><span class="sxs-lookup"><span data-stu-id="716d2-136">Click **Attached**.</span></span> <span data-ttu-id="716d2-137">Šeit var saņemt detalizētu informāciju par pirkšanas līgumu.</span><span class="sxs-lookup"><span data-stu-id="716d2-137">Here you can get details for the purchase agreement.</span></span> <span data-ttu-id="716d2-138">Piemēram, jūs varat redzēt cenu un vai cena un atlaide ir fiksētas, kas nozīmē, ka, mainot cenu vai atlaidi pirkšanas pasūtījumā uz citu vērtību, nekā saistībās, sistēma noņems saiti, lai pirkšanas pasūtījuma rinda neizpildītu saistības.</span><span class="sxs-lookup"><span data-stu-id="716d2-138">For example, you can see the price and whether the price and discount are fixed, which means that if you change price or discount on the purchase order to a different value than on the commitment, the system will remove the link so the purchase order line does not fulfill the commitment.</span></span> <span data-ttu-id="716d2-139">Varat apskatīt arī, vai ir atlasīta opcija Sasniegts maksimums, kas nozīmē, ka saistību daudzumu nevar pārsniegt, summējot visus pirkumus, kas izpilda saistības.</span><span class="sxs-lookup"><span data-stu-id="716d2-139">You can also see if the Max is enforced option is selected, which means that the quantity on the commitment cannot be exceeded by summing all of the purchases that fulfill the commitment.</span></span>  
3. <span data-ttu-id="716d2-140">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="716d2-140">Close the page.</span></span>

## <a name="look-up-the-purchase-agreement"></a><span data-ttu-id="716d2-141">Pirkšanas līguma uzmeklēšana</span><span class="sxs-lookup"><span data-stu-id="716d2-141">Look up the purchase agreement</span></span>
1. <span data-ttu-id="716d2-142">**Darbību rūtī** noklikšķiniet uz **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="716d2-142">On the **Action Pane**, click **General**.</span></span>
2. <span data-ttu-id="716d2-143">Klikšķiniet uz **Pirkuma līgums**.</span><span class="sxs-lookup"><span data-stu-id="716d2-143">Click **Purchase agreement**.</span></span>
3. <span data-ttu-id="716d2-144">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="716d2-144">Close the page.</span></span>
4. <span data-ttu-id="716d2-145">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="716d2-145">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]