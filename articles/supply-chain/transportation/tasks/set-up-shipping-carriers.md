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
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 124f7473cbdae8890f74115d461603f50cc58be8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004881"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="200ad-103">Sūtījumu pārvadātāju iestatīšana</span><span class="sxs-lookup"><span data-stu-id="200ad-103">Set up shipping carriers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="200ad-104">Šajā tēmā parādīts, kā iestatīt nosūtījuma pārvadātāju un definēt tādu informāciju kā pakalpojums, piegādes režīms, transportēšanas norēķini, transportēšanas ierobežojumi un nosūtīšanas likme.</span><span class="sxs-lookup"><span data-stu-id="200ad-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="200ad-105">Transportēšanas koordinators pēc tam var piešķirt nosūtījuma pārvadātāju ienākošai vai izejošai kravai.</span><span class="sxs-lookup"><span data-stu-id="200ad-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="200ad-106">Jauna nosūtījumu pārvadātāja izveide</span><span class="sxs-lookup"><span data-stu-id="200ad-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="200ad-107">Pārejiet uz **Navigācijas rūts > Moduļi > Transportēšanas pārvaldība > Iestatīšana > Pārvadātāji > Sūtījumu pārvadātāji**.</span><span class="sxs-lookup"><span data-stu-id="200ad-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="200ad-108">Atlasiet **Jauns** darbību rūtī.</span><span class="sxs-lookup"><span data-stu-id="200ad-108">Select **New** on the Action Pane.</span></span>
3. <span data-ttu-id="200ad-109">Ierakstiet vērtību laukā **Sūtījumu pārvadātājs**.</span><span class="sxs-lookup"><span data-stu-id="200ad-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="200ad-110">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="200ad-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="200ad-111">Laukā **Režīms** atlasiet opciju no nolaižamās izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="200ad-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="200ad-112">Vispārējās informācijas ievade par nosūtījumu pārvadātāju</span><span class="sxs-lookup"><span data-stu-id="200ad-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="200ad-113">Pārslēdziet sadaļas **Pārskats** paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="200ad-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="200ad-114">Atzīmējiet vai noņemiet atzīmi no izvēles rūtiņas **Aktivizēt nosūtīšanas pārvadātāju**.</span><span class="sxs-lookup"><span data-stu-id="200ad-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="200ad-115">Laukā **Kreditora konts** atlasiet opciju no nolaižamās izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="200ad-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="200ad-116">Atlasiet kreditora kontu, kuram piešķirt nosūtījuma pārvadātāju.</span><span class="sxs-lookup"><span data-stu-id="200ad-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="200ad-117">Atlasiet opciju laukā **Transportēšanas norēķinu veids**.</span><span class="sxs-lookup"><span data-stu-id="200ad-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="200ad-118">Atlasiet **Manuāli**, lai izmantotu transportēšanas norēķinu lapu, vai atlasiet **EDI**, lai atjauninātu norēķinus, izmantojot elektronisko datu apmaiņu (EDI).</span><span class="sxs-lookup"><span data-stu-id="200ad-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="200ad-119">Atzīmējiet vai noņemiet atzīmi no izvēles rūtiņas **Aktivizēt pārvadātāja vērtējumu**.</span><span class="sxs-lookup"><span data-stu-id="200ad-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="200ad-120">Nepieciešamo pakalpojumu izveide sūtījumu pārvadātājam</span><span class="sxs-lookup"><span data-stu-id="200ad-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="200ad-121">Pārslēdziet sadaļas **Pakalpojumi** paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="200ad-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="200ad-122">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="200ad-122">Select **New**.</span></span>
3. <span data-ttu-id="200ad-123">Ierakstiet vērtību laukā **Pārvadātāja pakalpojums**.</span><span class="sxs-lookup"><span data-stu-id="200ad-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="200ad-124">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="200ad-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="200ad-125">Laukā **Pārvadāšanas metode** atlasiet opciju no nolaižamās izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="200ad-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="200ad-126">Iestatiet pārvadātāja adresi (nav obligāti)</span><span class="sxs-lookup"><span data-stu-id="200ad-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="200ad-127">Pārslēdziet sadaļas **Adreses** izvēršanu.</span><span class="sxs-lookup"><span data-stu-id="200ad-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="200ad-128">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="200ad-128">Select **New**.</span></span>
3. <span data-ttu-id="200ad-129">Laukā **Nosaukums vai apraksts** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="200ad-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="200ad-130">Laukā **Valsts/reģions** atlasiet opciju no nolaižamās izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="200ad-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="200ad-131">Laukā **Pasta indekss** atlasiet opciju no nolaižamās izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="200ad-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="200ad-132">Laukā **Iela** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="200ad-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="200ad-133">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="200ad-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="200ad-134">Iestatiet nosūtījumu pārvadātāja novērtēšanas profilu</span><span class="sxs-lookup"><span data-stu-id="200ad-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="200ad-135">Pārslēdziet sadaļas **Novērtējuma profili** izvēršanu.</span><span class="sxs-lookup"><span data-stu-id="200ad-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="200ad-136">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="200ad-136">Select **New**.</span></span>
3. <span data-ttu-id="200ad-137">Ierakstiet vērtību laukā **Novērtējuma profils**.</span><span class="sxs-lookup"><span data-stu-id="200ad-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="200ad-138">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="200ad-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="200ad-139">Laukā **Vieta** atlasiet opciju no nolaižamās izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="200ad-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="200ad-140">Laukā **Noliktava** atlasiet opciju no nolaižamās izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="200ad-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="200ad-141">Laukā **Likmes noteikšanas programma** atlasiet opciju no nolaižamās izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="200ad-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="200ad-142">Atlasiet likmes noteikšanas programmu, kura atbilst līgumam, kas jums noslēgts ar pārvadātāju.</span><span class="sxs-lookup"><span data-stu-id="200ad-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="200ad-143">Laukā **Likmes šablons** atlasiet opciju no nolaižamās izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="200ad-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="200ad-144">Laukā **Pārvadājumu ilguma noteikšanas programma** atlasiet opciju no nolaižamās izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="200ad-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="200ad-145">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="200ad-145">Select **Save**.</span></span>

