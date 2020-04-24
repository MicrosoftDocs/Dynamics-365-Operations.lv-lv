---
title: Sūtījumu pārvadātāju iestatīšana
description: Šajā tēmā parādīts, kā iestatīt nosūtījuma pārvadātāju un definēt tādu informāciju kā pakalpojums, piegādes režīms, transportēšanas norēķini, transportēšanas ierobežojumi un nosūtīšanas likme.
author: ShylaThompson
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e6a29dce877a53d125c5a151da6cfbb13d46b29
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201598"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="a527b-103">Sūtījumu pārvadātāju iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a527b-103">Set up shipping carriers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a527b-104">Šajā tēmā parādīts, kā iestatīt nosūtījuma pārvadātāju un definēt tādu informāciju kā pakalpojums, piegādes režīms, transportēšanas norēķini, transportēšanas ierobežojumi un nosūtīšanas likme.</span><span class="sxs-lookup"><span data-stu-id="a527b-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="a527b-105">Transportēšanas koordinators pēc tam var piešķirt nosūtījuma pārvadātāju ienākošai vai izejošai kravai.</span><span class="sxs-lookup"><span data-stu-id="a527b-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="a527b-106">Jauna nosūtījumu pārvadātāja izveide</span><span class="sxs-lookup"><span data-stu-id="a527b-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="a527b-107">Pārejiet uz **Navigācijas rūts > Moduļi > Transportēšanas pārvaldība > Iestatīšana > Pārvadātāji > Sūtījumu pārvadātāji**.</span><span class="sxs-lookup"><span data-stu-id="a527b-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="a527b-108">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="a527b-108">Select **New** in the Action pane.</span></span>
3. <span data-ttu-id="a527b-109">Ierakstiet vērtību laukā **Sūtījumu pārvadātājs**.</span><span class="sxs-lookup"><span data-stu-id="a527b-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="a527b-110">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a527b-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="a527b-111">Laukā **Režīms** atlasiet opciju no nolaižamās izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="a527b-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="a527b-112">Vispārējās informācijas ievade par nosūtījumu pārvadātāju</span><span class="sxs-lookup"><span data-stu-id="a527b-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="a527b-113">Pārslēdziet sadaļas **Pārskats** paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="a527b-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="a527b-114">Atzīmējiet vai noņemiet atzīmi no izvēles rūtiņas **Aktivizēt nosūtīšanas pārvadātāju**.</span><span class="sxs-lookup"><span data-stu-id="a527b-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="a527b-115">Laukā **Kreditora konts** atlasiet opciju no nolaižamās izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="a527b-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="a527b-116">Atlasiet kreditora kontu, kuram piešķirt nosūtījuma pārvadātāju.</span><span class="sxs-lookup"><span data-stu-id="a527b-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="a527b-117">Atlasiet opciju laukā **Transportēšanas norēķinu veids**.</span><span class="sxs-lookup"><span data-stu-id="a527b-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="a527b-118">Atlasiet **Manuāli**, lai izmantotu transportēšanas norēķinu lapu, vai atlasiet **EDI**, lai atjauninātu norēķinus, izmantojot elektronisko datu apmaiņu (EDI).</span><span class="sxs-lookup"><span data-stu-id="a527b-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="a527b-119">Atzīmējiet vai noņemiet atzīmi no izvēles rūtiņas **Aktivizēt pārvadātāja vērtējumu**.</span><span class="sxs-lookup"><span data-stu-id="a527b-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="a527b-120">Nepieciešamo pakalpojumu izveide sūtījumu pārvadātājam</span><span class="sxs-lookup"><span data-stu-id="a527b-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="a527b-121">Pārslēdziet sadaļas **Pakalpojumi** paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="a527b-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="a527b-122">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="a527b-122">Select **New**.</span></span>
3. <span data-ttu-id="a527b-123">Ierakstiet vērtību laukā **Pārvadātāja pakalpojums**.</span><span class="sxs-lookup"><span data-stu-id="a527b-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="a527b-124">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a527b-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="a527b-125">Laukā **Pārvadāšanas metode** atlasiet opciju no nolaižamās izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="a527b-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="a527b-126">Iestatiet pārvadātāja adresi (nav obligāti)</span><span class="sxs-lookup"><span data-stu-id="a527b-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="a527b-127">Pārslēdziet sadaļas **Adreses** izvēršanu.</span><span class="sxs-lookup"><span data-stu-id="a527b-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="a527b-128">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="a527b-128">Select **New**.</span></span>
3. <span data-ttu-id="a527b-129">Laukā **Nosaukums vai apraksts** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a527b-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="a527b-130">Laukā **Valsts/reģions** atlasiet opciju no nolaižamās izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="a527b-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="a527b-131">Laukā **Pasta indekss** atlasiet opciju no nolaižamās izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="a527b-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="a527b-132">Laukā **Iela** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a527b-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="a527b-133">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="a527b-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="a527b-134">Iestatiet nosūtījumu pārvadātāja novērtēšanas profilu</span><span class="sxs-lookup"><span data-stu-id="a527b-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="a527b-135">Pārslēdziet sadaļas **Novērtējuma profili** izvēršanu.</span><span class="sxs-lookup"><span data-stu-id="a527b-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="a527b-136">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="a527b-136">Select **New**.</span></span>
3. <span data-ttu-id="a527b-137">Ierakstiet vērtību laukā **Novērtējuma profils**.</span><span class="sxs-lookup"><span data-stu-id="a527b-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="a527b-138">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a527b-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="a527b-139">Laukā **Vieta** atlasiet opciju no nolaižamās izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="a527b-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="a527b-140">Laukā **Noliktava** atlasiet opciju no nolaižamās izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="a527b-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="a527b-141">Laukā **Likmes noteikšanas programma** atlasiet opciju no nolaižamās izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="a527b-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="a527b-142">Atlasiet likmes noteikšanas programmu, kura atbilst līgumam, kas jums noslēgts ar pārvadātāju.</span><span class="sxs-lookup"><span data-stu-id="a527b-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="a527b-143">Laukā **Likmes šablons** atlasiet opciju no nolaižamās izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="a527b-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="a527b-144">Laukā **Pārvadājumu ilguma noteikšanas programma** atlasiet opciju no nolaižamās izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="a527b-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="a527b-145">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="a527b-145">Select **Save**.</span></span>

