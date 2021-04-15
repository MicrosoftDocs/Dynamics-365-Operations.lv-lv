---
title: Pirkšanas līguma izveide
description: Šajā tēmā aprakstīta pirkšanas līguma izveide.
author: kamaybac
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19bfbe7bc78f08dbbc6f9924313749a46672e202
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812330"
---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="d7374-103">Pirkšanas līguma izveide</span><span class="sxs-lookup"><span data-stu-id="d7374-103">Create a purchase agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d7374-104">Šajā tēmā aprakstīta pirkšanas līguma izveide.</span><span class="sxs-lookup"><span data-stu-id="d7374-104">This topic guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="d7374-105">Parasti to veic pirkšanas pārvaldnieks.</span><span class="sxs-lookup"><span data-stu-id="d7374-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="d7374-106">Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="d7374-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="d7374-107">Pirms sākt, jāiestata pirkšanas līgumu klasifikācijas.</span><span class="sxs-lookup"><span data-stu-id="d7374-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="d7374-108">Kad esat izveidojis vienošanos, to var izmantot, veidojot PP, un šādi pirkšanas līguma nosacījumi tiks kopēti virsrakstā un jebkurās pasūtījuma rindās, kuras līgums ietekmē.</span><span class="sxs-lookup"><span data-stu-id="d7374-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="d7374-109">Jauna pirkšanas līguma izveide</span><span class="sxs-lookup"><span data-stu-id="d7374-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="d7374-110">Ejiet uz **Navigācijas rūts > Moduļi > Iepirkumi un ārpakalpojumi > Pirkšanas līgumi >Pirkšanas līgumi**.</span><span class="sxs-lookup"><span data-stu-id="d7374-110">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase agreements > Purchase agreements**.</span></span>
2. <span data-ttu-id="d7374-111">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="d7374-111">Click **New**.</span></span>
3. <span data-ttu-id="d7374-112">Laukā **Piegādātāja konts** atlasiet nolaižamo izvēlni un atlasiet vēlamā ieraksta rindu.</span><span class="sxs-lookup"><span data-stu-id="d7374-112">In the **Vendor account** field, select the drop-down menu and select the row of the desired record.</span></span>
4. <span data-ttu-id="d7374-113">Laukā **Pirkšanas līguma klasifikācija** atlasiet nolaižamo izvēlni un atlasiet vēlamā ieraksta rindu.</span><span class="sxs-lookup"><span data-stu-id="d7374-113">In the **Purchase agreement classification** field, select the drop-down menu and select the row of the desired record.</span></span>
5. <span data-ttu-id="d7374-114">Izvērsiet kopsavilkuma cilni **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="d7374-114">Expand the **General** FastTab.</span></span>
6. <span data-ttu-id="d7374-115">Laukā **Izbeigšanās datums** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="d7374-115">In the **Expiration date** field, enter a date.</span></span>

    - <span data-ttu-id="d7374-116">Beigu datums būs noklusējuma datums visām saistību rindām un noteiks, cik ilgi katra saistība ir spēkā.</span><span class="sxs-lookup"><span data-stu-id="d7374-116">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  

7. <span data-ttu-id="d7374-117">Laukā **Dokumenta nosaukums** ierakstiet pirkšanas līguma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="d7374-117">In the **Document title** field, type a name for your purchase agreement.</span></span>

    - <span data-ttu-id="d7374-118">Lauku **Noklusējuma saistības** atstājiet iestatītu kā **Produkta daudzuma saistības** (vai mainiet, ja tas tā nav iestatīts).</span><span class="sxs-lookup"><span data-stu-id="d7374-118">Leave the **Default commitment** field set to **Product quantity commitment** (or change it if it's not set to this).</span></span>  
    - <span data-ttu-id="d7374-119">Noklusējuma saistību vērtība nosaka jūsu opcijas līguma rindās.</span><span class="sxs-lookup"><span data-stu-id="d7374-119">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="d7374-120">Ja jums ir nepieciešams jauns saistību tips, veidojot līguma rindas, ir jāmaina noklusējuma saistības virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="d7374-120">If you need a new commitment type when you're creating the agreement lines, you need to change the default commitment on the header.</span></span> <span data-ttu-id="d7374-121">Ir 4 saistību veidi: **Produkta daudzuma saistības** noteiktam produkta daudzumam, **Produkta vērtības saistības** noteiktam produkta valūtas daudzumam, **Produkta kategorijas vērtības saistības** noteiktai valūtas summai iepirkuma kategorijā, kad vērtība var būt kataloga vienumam vai ne kataloga vienumam, **Vērtības saistība** noteiktam valūtas daudzumam, ko var sasniegt noteiktam produktam vai iepirkumu kategorijai.</span><span class="sxs-lookup"><span data-stu-id="d7374-121">There are 4 types of commitments: **Product quantity commitment** - for a specific quantity of a product; **Product value commitment** - for a specific currency amount of a product; **Product category value commitment** - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; **Value commitment** - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  

8. <span data-ttu-id="d7374-122">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d7374-122">Select **OK**.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="d7374-123">Saistību pievienošana</span><span class="sxs-lookup"><span data-stu-id="d7374-123">Add a commitment</span></span>
1. <span data-ttu-id="d7374-124">Atlasiet **Pievienot rindu**.</span><span class="sxs-lookup"><span data-stu-id="d7374-124">Select **Add line**.</span></span>
2. <span data-ttu-id="d7374-125">Laukā **Vienuma numurs** atlasiet vēlamo ierakstu nolaižamajā izvēlnē.</span><span class="sxs-lookup"><span data-stu-id="d7374-125">In the **Item number** field, select the desired record from the drop-down menu.</span></span>
3. <span data-ttu-id="d7374-126">Laukā **Daudzums** ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="d7374-126">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="d7374-127">Tas ir kopējais daudzums, kuru vienojāties iegādāties no kreditora.</span><span class="sxs-lookup"><span data-stu-id="d7374-127">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
4. <span data-ttu-id="d7374-128">Laukā **Vienības cena** ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="d7374-128">In the **Unit price** field, enter a number.</span></span>
5. <span data-ttu-id="d7374-129">Izvērsiet sadaļu **Detalizēta informācija par rindu**.</span><span class="sxs-lookup"><span data-stu-id="d7374-129">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="d7374-130">Opciju **Ir iestatīts maksimālais** iestatiet kā **Jā**.</span><span class="sxs-lookup"><span data-stu-id="d7374-130">Set the **Max is enforced** option to **Yes**.</span></span> <span data-ttu-id="d7374-131">Opcija **Ir iestatīts maksimālais** ierobežo saistības izmantošanu.</span><span class="sxs-lookup"><span data-stu-id="d7374-131">The **Max is enforced** option limits the use of the commitment.</span></span> <span data-ttu-id="d7374-132">Varat iegādāties tikai daudzumu, kas norādīts laukā **Daudzums** rindai.</span><span class="sxs-lookup"><span data-stu-id="d7374-132">You can only purchase up to the quantity that's specified in the **Quantity** field for the line.</span></span>  

## <a name="add-header-conditions"></a><span data-ttu-id="d7374-133">Virsraksta nosacījumu pievienošana</span><span class="sxs-lookup"><span data-stu-id="d7374-133">Add header conditions</span></span>
1. <span data-ttu-id="d7374-134">Darbību rūtī atlasiet **Opcijas**.</span><span class="sxs-lookup"><span data-stu-id="d7374-134">On the Action Pane, select **Options**.</span></span>
2. <span data-ttu-id="d7374-135">Atlasiet **Mainīt skatu**.</span><span class="sxs-lookup"><span data-stu-id="d7374-135">Select **Change view**.</span></span>
3. <span data-ttu-id="d7374-136">Atlasiet **Galvenes skats**.</span><span class="sxs-lookup"><span data-stu-id="d7374-136">Select **Header view**.</span></span>
4. <span data-ttu-id="d7374-137">Izvērsiet sadaļu **Noteikumi**.</span><span class="sxs-lookup"><span data-stu-id="d7374-137">Expand the **Terms** section.</span></span>
5. <span data-ttu-id="d7374-138">Laukā **Maksājumu metode** nolaižamajā sarakstā atlasiet vēlamo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d7374-138">In the **Method of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="d7374-139">Maksājuma nosacījumi no kreditora konta tiek šeit rādīti pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="d7374-139">The payment terms from the vendor account are shown here by default.</span></span>  
6. <span data-ttu-id="d7374-140">Laukā **Piegādes metode** nolaižamajā sarakstā atlasiet vēlamo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d7374-140">In the **Mode of delivery** field, select the desired record in the drop-down menu.</span></span>
7. <span data-ttu-id="d7374-141">Laukā **Piegādes noteikumi** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="d7374-141">In the **Delivery terms** field, select the drop-down button to open the lookup.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="d7374-142">Līguma apstiprināšana un aktivizēšana</span><span class="sxs-lookup"><span data-stu-id="d7374-142">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="d7374-143">Darbību rūtī atlasiet **Pirkšanas līgums**.</span><span class="sxs-lookup"><span data-stu-id="d7374-143">On the Action Pane, select **Purchase agreement**.</span></span>
2. <span data-ttu-id="d7374-144">Atlasiet **Apstiprināšana**.</span><span class="sxs-lookup"><span data-stu-id="d7374-144">Select **Confirmation**.</span></span> <span data-ttu-id="d7374-145">Iestatiet opciju **Atzīmēt līgumu kā spēkā esošu** kā **Jā**.</span><span class="sxs-lookup"><span data-stu-id="d7374-145">Set the **Mark agreement as effective** option to **Yes**.</span></span>  
3. <span data-ttu-id="d7374-146">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d7374-146">Select **OK**.</span></span>
4. <span data-ttu-id="d7374-147">Darbību rūtī atlasiet **Pirkšanas līgums**.</span><span class="sxs-lookup"><span data-stu-id="d7374-147">On the Action Pane, select **Purchase agreement**.</span></span>
5. <span data-ttu-id="d7374-148">Atlasiet **Pirkšanas līguma apstiprinājumi**.</span><span class="sxs-lookup"><span data-stu-id="d7374-148">Select **Purchase agreement confirmations**.</span></span> <span data-ttu-id="d7374-149">Opcija **Priekšskatījums/drukāt** ļauj drukāt pirkšanas līgumu, ko pēc tam drukāt un nosūtīt piegādātājam.</span><span class="sxs-lookup"><span data-stu-id="d7374-149">The **Preview/Print** option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="d7374-150">Ja atjaunināt līgumu vēlāk un atkārtoti to apstiprināt, abas versijas tiks parādītas šeit.</span><span class="sxs-lookup"><span data-stu-id="d7374-150">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="d7374-151">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d7374-151">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]