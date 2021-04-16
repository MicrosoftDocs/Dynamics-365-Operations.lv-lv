---
title: Krājumu reģistrēšana uzlabotā noliktavā aktivizētam krājumam, izmantojot krājumu saņemšanas žurnālu
description: Šajā tēmā parādīts, kā reģistrēt krājumus, izmantojot krājumu saņemšanas žurnālu, ja izmantojat papildu noliktavas vadības procesus.
author: ShylaThompson
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c58aa1cec6c0bfe33fa1ef90267dcd8ac1218157
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830838"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="2b37f-103">Krājumu reģistrēšana uzlabotā noliktavā aktivizētam krājumam, izmantojot krājumu saņemšanas žurnālu</span><span class="sxs-lookup"><span data-stu-id="2b37f-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2b37f-104">Šajā tēmā parādīts, kā reģistrēt krājumus, izmantojot krājumu saņemšanas žurnālu, ja izmantojat papildu noliktavas vadības procesus.</span><span class="sxs-lookup"><span data-stu-id="2b37f-104">This topic presents a scenario that shows how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="2b37f-105">Tas parasti būtu jāveic saņemšanas darbiniekam.</span><span class="sxs-lookup"><span data-stu-id="2b37f-105">This would usually be done by a receiving clerk.</span></span>

## <a name="enable-sample-data"></a><span data-ttu-id="2b37f-106">Iespējot datu paraugu</span><span class="sxs-lookup"><span data-stu-id="2b37f-106">Enable sample data</span></span>

<span data-ttu-id="2b37f-107">Lai šajā scenārijā darbotos, izmantojot šajā tēmā norādītos parauga ierakstus un vērtības, ir jāizmanto sistēma, kurā ir instalēti standarta demonstrācijas dati, un pirms sākšanas ir jāatlasa *USMF* juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="2b37f-107">To work through this scenario using the sample records and values specified in this topic, you must be using a system where the standard demo data is installed, and you must select the *USMF* legal entity before you begin.</span></span>

<span data-ttu-id="2b37f-108">Tā vietā varat strādāt šajā scenārijā, aizstājot vērtības no saviem datiem, ja vien jums ir pieejami šādi dati:</span><span class="sxs-lookup"><span data-stu-id="2b37f-108">You can instead work through this scenario by substituting values from your own data provided that you have the following data available:</span></span>

- <span data-ttu-id="2b37f-109">Jums jābūt apstiprinātam pirkšanas pasūtījumam ar atvērtu pirkšanas pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="2b37f-109">You must have a confirmed purchase order with an open purchase order line.</span></span>
- <span data-ttu-id="2b37f-110">Rindas vienībai ir jābūt esošā krājumā.</span><span class="sxs-lookup"><span data-stu-id="2b37f-110">The item on the line must be stocked.</span></span> <span data-ttu-id="2b37f-111">Tā nedrīkst izmantot preces variantus, un tai nedrīkst būt izsekošanas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="2b37f-111">It must not use product variants, and must not have tracking dimensions.</span></span>
- <span data-ttu-id="2b37f-112">Krājuma vienībai jābūt saistītai ar noliktavas dimensijas grupu, kas iespējo noliktavas pārvaldības apstrādi.</span><span class="sxs-lookup"><span data-stu-id="2b37f-112">The item must be associated with a storage dimension group that has warehouse management process enabled.</span></span>
- <span data-ttu-id="2b37f-113">Izmantojamajai noliktavai ir jābūt iespējotiem noliktavas vadības procesiem un saņemšanai izmantojamajam novietojumam jānotiek numuru zīmju pārbaudei.</span><span class="sxs-lookup"><span data-stu-id="2b37f-113">The warehouse that's used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span>

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a><span data-ttu-id="2b37f-114">Izveidot krājumu saņemšanas žurnāla virsrakstu, kas izmanto noliktavas pārvaldību</span><span class="sxs-lookup"><span data-stu-id="2b37f-114">Create an item arrival journal header that uses warehouse management</span></span>

<span data-ttu-id="2b37f-115">Šajā scenārijā parādīts, kā izveidot krājumu saņemšanas žurnāla virsrakstu, kas izmanto noliktavas pārvaldību:</span><span class="sxs-lookup"><span data-stu-id="2b37f-115">The following scenario shows how to create an item arrival journal header that uses warehouse management:</span></span>

1. <span data-ttu-id="2b37f-116">Pārliecinieties, vai sistēmā ir apstiprināts pirkšanas pasūtījums, kas neatbilst iepriekšējā sadaļā aprakstītajām prasībām.</span><span class="sxs-lookup"><span data-stu-id="2b37f-116">Make sure your system contains a confirmed purchase order that fulfils the requirements outlined in the previous section.</span></span> <span data-ttu-id="2b37f-117">Šis scenārijs izmanto pirkšanas pasūtījumu uzņēmumam *USMF*, kreditora kontam *1001*, noliktavai *51*, ar pasūtījuma rindu *10 PL* (10 paletes) ar krājumu numuru *M9200*.</span><span class="sxs-lookup"><span data-stu-id="2b37f-117">This scenario uses a purchase order for company *USMF*, vendor account *1001*, warehouse *51*, with an order line for *10 PL* (10 pallets) of item number *M9200*.</span></span>
1. <span data-ttu-id="2b37f-118">Pierakstiet izmantojamo pirkuma pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="2b37f-118">Make a note of the purchase order number that you will use.</span></span>
1. <span data-ttu-id="2b37f-119">Dodieties uz **Krājumu pārvaldība \> Žurnāla ieraksti \> Krājumu saņemšana \> Krājumu saņemšana**.</span><span class="sxs-lookup"><span data-stu-id="2b37f-119">Go to **Inventory management \> Journal entries \> Item arrival \> Item arrival**.</span></span>
1. <span data-ttu-id="2b37f-120">Atlasiet **Jauns** darbību rūtī.</span><span class="sxs-lookup"><span data-stu-id="2b37f-120">Select **New** on the Action Pane.</span></span>
1. <span data-ttu-id="2b37f-121">Atveras dialoglodziņš **Izveidot noliktavas pārvaldības žurnālu**.</span><span class="sxs-lookup"><span data-stu-id="2b37f-121">The **Create warehouse management journal** dialog box opens.</span></span> <span data-ttu-id="2b37f-122">Laukā **Nosaukums** atlasiet žurnāla nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="2b37f-122">Select a journal name in the **Name** field.</span></span>
    - <span data-ttu-id="2b37f-123">Ja izmantojat uzņēmuma *USMF* paraugdatus, atlasiet *WHS*.</span><span class="sxs-lookup"><span data-stu-id="2b37f-123">If you are using *USMF* sample data, select *WHS*.</span></span>
    - <span data-ttu-id="2b37f-124">Ja izmantojat savus datus, izvēlei žurnālam **Pārbaudīt izdošanas vietu** jābūt iestatītam uz *Nē* un **Karantīnas pārvaldība** jāiestata uz *Nē*.</span><span class="sxs-lookup"><span data-stu-id="2b37f-124">If you're using your own data, the journal you choose must have **Check picking location** set to *No* and **Quarantine management** set to *No*.</span></span>
1. <span data-ttu-id="2b37f-125">Iestatiet **Atsauci** *Pirkšanas pasūtījumam*.</span><span class="sxs-lookup"><span data-stu-id="2b37f-125">Set **Reference** to *Purchase order*.</span></span>
1. <span data-ttu-id="2b37f-126">Iestatiet **Konta numuru** uz *1001*.</span><span class="sxs-lookup"><span data-stu-id="2b37f-126">Set **Account number** to *1001*.</span></span>
1. <span data-ttu-id="2b37f-127">Iestatiet **Numuru** pirkšanas pasūtījuma numuram, kuru esat identificējis šim uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="2b37f-127">Set **Number** to the number of the purchase order that you identified for this exercise.</span></span>

    <span data-ttu-id="2b37f-128">![Krājumu saņemšanas žurnāls](../media/item-arrival-journal-header.png "Krājumu saņemšanas žurnāls")</span><span class="sxs-lookup"><span data-stu-id="2b37f-128">![Item arrival journal](../media/item-arrival-journal-header.png "Item arrival journal")</span></span>

1. <span data-ttu-id="2b37f-129">Atlasiet **Labi**, lai izveidotu žurnāla galveni.</span><span class="sxs-lookup"><span data-stu-id="2b37f-129">Select the **OK** to create the journal header.</span></span>
1. <span data-ttu-id="2b37f-130">Sadaļā **Žurnāla rindas** atlasiet **Pievienot rindu** un ievadiet šādus datus:</span><span class="sxs-lookup"><span data-stu-id="2b37f-130">In the **Journal lines** section, select **Add line** and enter the following data:</span></span>
    - <span data-ttu-id="2b37f-131">**Krājuma numurs** – iestatiet uz *M9200*.</span><span class="sxs-lookup"><span data-stu-id="2b37f-131">**Item number** – Set to *M9200*.</span></span> <span data-ttu-id="2b37f-132">**Vieta**, **Noliktava** un **Daudzums** tiks iestatīti, pamatojoties uz krājumu darbības datiem 10 paletēm (1000 ea.).</span><span class="sxs-lookup"><span data-stu-id="2b37f-132">The **Site**, **Warehouse**, and **Quantity** will get set based on the inventory transaction data for the 10 pallets (1000 ea.).</span></span>
    - <span data-ttu-id="2b37f-133">**Novietojums** – iestatīts uz *001*.</span><span class="sxs-lookup"><span data-stu-id="2b37f-133">**Location** – Set to  *001*.</span></span> <span data-ttu-id="2b37f-134">Šis konkrētais novietojums neizseko numura zīmes.</span><span class="sxs-lookup"><span data-stu-id="2b37f-134">This specific location does not track license plates.</span></span>

    <span data-ttu-id="2b37f-135">![Krājumu saņemšanas žurnāla rinda](../media/item-arrival-journal-line.png "Krājumu saņemšanas žurnāla rinda")</span><span class="sxs-lookup"><span data-stu-id="2b37f-135">![Item arrival journal line](../media/item-arrival-journal-line.png "Item arrival journal line")</span></span>

    > [!NOTE]
    > <span data-ttu-id="2b37f-136">Lauks **Datums** nosaka datumu, kurā šī krājuma rīcībā esošais daudzums tiks reģistrēts krājumos.</span><span class="sxs-lookup"><span data-stu-id="2b37f-136">The **Date** field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    >
    > <span data-ttu-id="2b37f-137">**Laidiena ID** ierakstīs sistēma, ja tā varēs to unikāli identificēt no sniegtās informācijas.</span><span class="sxs-lookup"><span data-stu-id="2b37f-137">The **Lot ID** will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="2b37f-138">Pretējā gadījumā jums būs tas jāievada manuāli.</span><span class="sxs-lookup"><span data-stu-id="2b37f-138">Otherwise you will have to enter this manually.</span></span> <span data-ttu-id="2b37f-139">Tas ir obligāts lauks, kas savieno šo reģistrāciju ar noteiktu pirmdokumenta rindu.</span><span class="sxs-lookup"><span data-stu-id="2b37f-139">This is a required field, which links this registration to a specific source document line.</span></span>  

1. <span data-ttu-id="2b37f-140">Darbību rūtī atlasiet **Pārbaudīt**.</span><span class="sxs-lookup"><span data-stu-id="2b37f-140">Select **Validate** on the Action Pane.</span></span> <span data-ttu-id="2b37f-141">Šādi tiek pārbaudīts, vai žurnāls ir gatavs grāmatošanai.</span><span class="sxs-lookup"><span data-stu-id="2b37f-141">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="2b37f-142">Ja pārbaude neizdodas, jums būs jāatrisina kļūdas pirms žurnālu varēs grāmatot.</span><span class="sxs-lookup"><span data-stu-id="2b37f-142">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
1. <span data-ttu-id="2b37f-143">Atveras dialoglodziņš **Pārbaudīt žurnālu**.</span><span class="sxs-lookup"><span data-stu-id="2b37f-143">The **Check journal** dialog box opens.</span></span> <span data-ttu-id="2b37f-144">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2b37f-144">Select **OK**.</span></span>
1. <span data-ttu-id="2b37f-145">Pārskatīt ziņojuma joslu.</span><span class="sxs-lookup"><span data-stu-id="2b37f-145">Review the message bar.</span></span> <span data-ttu-id="2b37f-146">Tajā vajadzētu būt ziņojumam par operācijas pabeigšanu.</span><span class="sxs-lookup"><span data-stu-id="2b37f-146">There should be a message denoting that the operation was completed.</span></span>  
1. <span data-ttu-id="2b37f-147">Darbību rūtī atlasiet **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="2b37f-147">Select **Post** on the Action Pane.</span></span>
1. <span data-ttu-id="2b37f-148">Atveras dialoglodziņš **Grāmatot žurnālu**.</span><span class="sxs-lookup"><span data-stu-id="2b37f-148">The **Post journal** dialog box opens.</span></span> <span data-ttu-id="2b37f-149">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2b37f-149">Select **OK**.</span></span>
1. <span data-ttu-id="2b37f-150">Pārskatīt ziņojuma joslu.</span><span class="sxs-lookup"><span data-stu-id="2b37f-150">Review the message bar.</span></span> <span data-ttu-id="2b37f-151">Tajā vajadzētu būt ziņojumam par operācijas pabeigšanu.</span><span class="sxs-lookup"><span data-stu-id="2b37f-151">There should be messages denoting that the operation completed.</span></span>
1. <span data-ttu-id="2b37f-152">Atlasiet **Funkcijas > Produktu saņemšana** darbību rūtī, lai atjauninātu pirkšanas pasūtījuma rindu un grāmatotu produktu saņemšanu.</span><span class="sxs-lookup"><span data-stu-id="2b37f-152">Select **Functions > Product receipt** on the Action Pane to update the purchase order line and post a product receipt.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
