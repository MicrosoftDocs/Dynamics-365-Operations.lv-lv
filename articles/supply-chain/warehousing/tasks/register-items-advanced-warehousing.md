--- 
title: "Krājumu reģistrēšana uzlabotā noliktavā aktivizētam krājumam, izmantojot krājumu saņemšanas žurnālu"
description: "Šajā procedūrā parādīts, kā reģistrēt krājumus, izmantojot krājumu saņemšanas žurnālu, ja izmantojat papildu noliktavas vadības procesus."
author: BibiSp
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 09d5d61a1950a5ab341d3bb3c814b6985d5e910e
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="df6df-103">Krājumu reģistrēšana uzlabotā noliktavā aktivizētam krājumam, izmantojot krājumu saņemšanas žurnālu</span><span class="sxs-lookup"><span data-stu-id="df6df-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="df6df-104">Šajā procedūrā parādīts, kā reģistrēt krājumus, izmantojot krājumu saņemšanas žurnālu, ja izmantojat papildu noliktavas vadības procesus.</span><span class="sxs-lookup"><span data-stu-id="df6df-104">This procedure shows you how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="df6df-105">Tas parasti būtu jāveic saņemšanas darbiniekam.</span><span class="sxs-lookup"><span data-stu-id="df6df-105">This would usually be done by a receiving clerk.</span></span> 

<span data-ttu-id="df6df-106">Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="df6df-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="df6df-107">Tad pirms šī ceļveža uzsākšanas pārliecinieties, ka jums ir apstiprināts pirkšanas pasūtījums ar atvērtu pirkšanas pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="df6df-107">You need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="df6df-108">Rindas vienībai ir jābūt esošai krājumā, tā nedrīkst lietot preču variantus, un tai nedrīkst būt izsekošanas dimensiju.</span><span class="sxs-lookup"><span data-stu-id="df6df-108">The item on the line must be stocked, and it must not use product variants, and must not have tracking dimensions.</span></span> <span data-ttu-id="df6df-109">Krājuma vienībai jābūt saistītai ar papildu noliktavas vadības procesu, kurš ir aktīvs noliktavas dimensijas grupai.</span><span class="sxs-lookup"><span data-stu-id="df6df-109">And the item needs to be associated with a warehouse management process enabled storage dimension group.</span></span> <span data-ttu-id="df6df-110">Izmantojamajai noliktavai ir jābūt iespējotiem noliktavas vadības procesiem un saņemšanai izmantojamajam novietojumam jānotiek numuru zīmju pārbaudei.</span><span class="sxs-lookup"><span data-stu-id="df6df-110">The warehouse that’s used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span> <span data-ttu-id="df6df-111">Ja jūs izmantojat USMF, varat izmantot uzņēmuma kontu 1001, noliktavu 51 un krājumu M9200, lai izveidotu savu PP.</span><span class="sxs-lookup"><span data-stu-id="df6df-111">If you’re using USMF, you can use company account 1001, Warehouse 51, and item M9200 to create your PO.</span></span> 

<span data-ttu-id="df6df-112">Pierakstiet izveidotā pirkšanas pasūtījuma numuru, un atzīmējiet arī krājuma kodu un vietu, kas izmantoti pirkšanas pasūtījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="df6df-112">Make a note of the number of the purchase order that you create, and also note the item number and the site that you used for your purchase order line.</span></span>


## <a name="create-an-item-arrival-journal-header"></a><span data-ttu-id="df6df-113">Krājumu saņemšanas žurnāla virsraksta izveide</span><span class="sxs-lookup"><span data-stu-id="df6df-113">Create an item arrival journal header</span></span>
1. <span data-ttu-id="df6df-114">Dodieties uz Krājumu saņemšana.</span><span class="sxs-lookup"><span data-stu-id="df6df-114">Go to Item arrival.</span></span>
2. <span data-ttu-id="df6df-115">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="df6df-115">Click New.</span></span>
3. <span data-ttu-id="df6df-116">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="df6df-116">In the Name field, type a value.</span></span>
    * <span data-ttu-id="df6df-117">Ja izmantojat USMF, varat ierakstīt WHS.</span><span class="sxs-lookup"><span data-stu-id="df6df-117">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="df6df-118">Ja izmantojat citus datus, izvēlētajam žurnālam ir jābūt šādiem rekvizītiem: Pārbaudīt izdošanas vietu vērtībai ir jābūt Nē un Karantīnas pārraudzība vērtībai ir jābūt Nē.</span><span class="sxs-lookup"><span data-stu-id="df6df-118">If you’re using other data, the journal whose name you choose has to have the following properties: Check picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="df6df-119">Laukā Numurs ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="df6df-119">In the Number field, type a value.</span></span>
5. <span data-ttu-id="df6df-120">Laukā Vieta ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="df6df-120">In the Site field, type a value.</span></span>
    * <span data-ttu-id="df6df-121">Atlasiet vietu, ko izmantojat pirkšanas pasūtījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="df6df-121">Select the site that you used for your purchase order line.</span></span> <span data-ttu-id="df6df-122">Tā kalpos kā noklusējuma vērtība, kas pēc noklusējuma tiks lietota visām žurnāla rindām.</span><span class="sxs-lookup"><span data-stu-id="df6df-122">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="df6df-123">Ja izmantojāt USMF noliktavu 51, izvēlieties vietu 5.</span><span class="sxs-lookup"><span data-stu-id="df6df-123">If you used warehouse 51 in USMF, choose site 5.</span></span>  
6. <span data-ttu-id="df6df-124">Laukā Noliktava ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="df6df-124">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="df6df-125">Atlasiet derīgu noliktavu atlasītajai vietai.</span><span class="sxs-lookup"><span data-stu-id="df6df-125">Select a valid warehouse for the site that you’ve selected.</span></span> <span data-ttu-id="df6df-126">Tā kalpos kā noklusējuma vērtība, kas pēc noklusējuma tiks lietota visām žurnāla rindām.</span><span class="sxs-lookup"><span data-stu-id="df6df-126">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="df6df-127">Ja jūs izmantojat parauga vērtības no USMF, atlasiet 51.</span><span class="sxs-lookup"><span data-stu-id="df6df-127">If you’re using the example values in USMF, select 51.</span></span>  
7. <span data-ttu-id="df6df-128">Ierakstiet vērtību laukā Vieta.</span><span class="sxs-lookup"><span data-stu-id="df6df-128">In the Location field, type a value.</span></span>
    * <span data-ttu-id="df6df-129">Atlasiet derīgu novietojumu atlasītajā noliktavā.</span><span class="sxs-lookup"><span data-stu-id="df6df-129">Select a valid location in the warehouse that you’ve selected.</span></span> <span data-ttu-id="df6df-130">Novietojums ir jāsasaista ar novietojuma profilu, ko kontrolē numura zīmes.</span><span class="sxs-lookup"><span data-stu-id="df6df-130">The location has to be associated with a location profile, which is license plate controlled.</span></span> <span data-ttu-id="df6df-131">Tā kalpos kā noklusējuma vērtība, kas pēc noklusējuma tiks lietota visām žurnāla rindām.</span><span class="sxs-lookup"><span data-stu-id="df6df-131">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="df6df-132">Ja jūs izmantojat parauga vērtības no USMF, atlasiet Bulk-008.</span><span class="sxs-lookup"><span data-stu-id="df6df-132">If you’re using the example values in USMF, select Bulk-008.</span></span>  
8. <span data-ttu-id="df6df-133">Ar peles labo pogu noklikšķiniet uz nolaižamās bultiņas laukā Numura zīme un pēc tam atlasiet Skatīt detalizētu informāciju.</span><span class="sxs-lookup"><span data-stu-id="df6df-133">Right-click on the drop-down arrow in the License plate field and then select View details.</span></span>
9. <span data-ttu-id="df6df-134">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="df6df-134">Click New.</span></span>
10. <span data-ttu-id="df6df-135">Laukā Numura zīme ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="df6df-135">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="df6df-136">Pierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="df6df-136">Make a note of the value.</span></span>  
11. <span data-ttu-id="df6df-137">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="df6df-137">Click Save.</span></span>
12. <span data-ttu-id="df6df-138">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="df6df-138">Close the page.</span></span>
13. <span data-ttu-id="df6df-139">Laukā Numura zīme ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="df6df-139">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="df6df-140">Ievadiet tikko izveidotās numura zīmes vērtību.</span><span class="sxs-lookup"><span data-stu-id="df6df-140">Enter the value of the license plate that you just created.</span></span> <span data-ttu-id="df6df-141">Tā kalpos kā noklusējuma vērtība, kas pēc noklusējuma tiks lietota visām žurnāla rindām.</span><span class="sxs-lookup"><span data-stu-id="df6df-141">This will serve as a default value, which will default to all lines in the journal.</span></span>  
14. <span data-ttu-id="df6df-142">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="df6df-142">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="df6df-143">Rindas pievienošana</span><span class="sxs-lookup"><span data-stu-id="df6df-143">Add a line</span></span>
1. <span data-ttu-id="df6df-144">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="df6df-144">Click Add line.</span></span>
2. <span data-ttu-id="df6df-145">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="df6df-145">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="df6df-146">Ievadiet krājuma kodu, kas tika izmantots pirkšanas pasūtījuma rindā.</span><span class="sxs-lookup"><span data-stu-id="df6df-146">Enter the item number that you used on the purchase order line.</span></span>  
3. <span data-ttu-id="df6df-147">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="df6df-147">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="df6df-148">Ievadiet daudzumu, kuru vēlaties reģistrēt</span><span class="sxs-lookup"><span data-stu-id="df6df-148">Enter the quantity that you want to register.</span></span>  
    * <span data-ttu-id="df6df-149">Lauks Datums nosaka datumu, kurā šī krājuma rīcībā esošais daudzums tiks reģistrēts krājumos.</span><span class="sxs-lookup"><span data-stu-id="df6df-149">The Date field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    * <span data-ttu-id="df6df-150">Laidiena ID ierakstīs sistēma, ja tā varēs to unikāli identificēt no sniegtās informācijas.</span><span class="sxs-lookup"><span data-stu-id="df6df-150">The lot ID will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="df6df-151">Pretējā gadījumā jums būs tas jāpievieno manuāli.</span><span class="sxs-lookup"><span data-stu-id="df6df-151">Otherwise you will have to add this manually.</span></span> <span data-ttu-id="df6df-152">Tas ir obligāts lauks, kas savieno šo reģistrāciju ar noteiktu pirmdokumenta rindu.</span><span class="sxs-lookup"><span data-stu-id="df6df-152">This is a mandatory field, which links this registration to a specific source document line.</span></span>  

## <a name="complete-the-registration"></a><span data-ttu-id="df6df-153">Reģistrācijas veikšana</span><span class="sxs-lookup"><span data-stu-id="df6df-153">Complete the registration</span></span>
1. <span data-ttu-id="df6df-154">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="df6df-154">Click Validate.</span></span>
    * <span data-ttu-id="df6df-155">Šādi tiek pārbaudīts, vai žurnāls ir gatavs grāmatošanai.</span><span class="sxs-lookup"><span data-stu-id="df6df-155">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="df6df-156">Ja pārbaude neizdodas, jums būs jāatrisina kļūdas pirms žurnālu varēs grāmatot.</span><span class="sxs-lookup"><span data-stu-id="df6df-156">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
2. <span data-ttu-id="df6df-157">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="df6df-157">Click OK.</span></span>
    * <span data-ttu-id="df6df-158">Kad esat noklikšķinājis uz Labi, pārbaudiet ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="df6df-158">After you clicked OK, check the message.</span></span> <span data-ttu-id="df6df-159">Tajā vajadzētu būt ziņojumam, kas ziņo, ka ar žurnālu ir viss kārtībā.</span><span class="sxs-lookup"><span data-stu-id="df6df-159">There should be a message saying that the journal is OK.</span></span>  
3. <span data-ttu-id="df6df-160">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="df6df-160">Click Post.</span></span>
4. <span data-ttu-id="df6df-161">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="df6df-161">Click OK.</span></span>
    * <span data-ttu-id="df6df-162">Kad esat noklikšķinājis uz Labi, pārbaudiet ziņojumu joslu.</span><span class="sxs-lookup"><span data-stu-id="df6df-162">After you have clicked OK, check the message bar.</span></span> <span data-ttu-id="df6df-163">Tajā vajadzētu būt ziņojumam par operācijas pabeigšanu.</span><span class="sxs-lookup"><span data-stu-id="df6df-163">There should be a message saying that the operation completed.</span></span>  
5. <span data-ttu-id="df6df-164">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="df6df-164">Close the page.</span></span>


