---
title: Saīsinātas izdošanas krājuma atkārtotas sadales iestatīšana
description: Šajā tēmā ir izskaidrots, kā ļaut noliktavas darbiniekiem ātri atrast alternatīvas atrašanās vietas, ja atrašanās vietā, uz kuru viņi tika novirzīti, nav pietiekami daudz krājumu.
author: ShylaThompson
manager: tfehr
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab8baf846d65e6fefe9ca575b5af5a2dbceac666
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976892"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="98650-103">Saīsinātas izdošanas krājuma atkārtotas sadales iestatīšana</span><span class="sxs-lookup"><span data-stu-id="98650-103">Set up short picking item reallocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="98650-104">Šajā procedūrā ir izskaidrots, kā ļaut noliktavas darbiniekiem ātri atrast alternatīvas atrašanās vietas, ja atrašanās vietā, uz kuru viņi tika novirzīti, nav pietiekami daudz krājumu.</span><span class="sxs-lookup"><span data-stu-id="98650-104">This procedure shows how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> 

<span data-ttu-id="98650-105">Atkārtotas sadales procesu kontrolē **Darba izņēmums** un izmanto noliktavā **nodarbinātais.**</span><span class="sxs-lookup"><span data-stu-id="98650-105">The reallocation process is controlled by a **Work exception** and used by the warehouse **worker.**</span></span>

<span data-ttu-id="98650-106">Ir iespējams izmantot automātisku, manuālu vai šos abus atkārtotas sadales procesus.</span><span class="sxs-lookup"><span data-stu-id="98650-106">It is possible to use Automatic, Manual, or both reallocation processes:</span></span>

- <span data-ttu-id="98650-107">Automātiska atkārtota sadale — novietojuma direktīvas tiek izmantotas, lai noteiktu, vai preces ir pieejamas citā atrašanās vietā.</span><span class="sxs-lookup"><span data-stu-id="98650-107">Automatic reallocation - Location directives are used to determine if the goods are available at another location.</span></span> <span data-ttu-id="98650-108">Ja tas ir iespējams, darbs tiks atjaunināts un noliktavas darbinieks tiks novirzīts uz alternatīvu atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="98650-108">If possible, the work will be updated and the warehouse user will be directed to the alternative location.</span></span>
- <span data-ttu-id="98650-109">Manuāla atkārtota sadale — ļauj noliktavas darbiniekam izvēlēties no vienas vai vairākām atrašanās vietām, kurās ir nerezervēti preču daudzumi.</span><span class="sxs-lookup"><span data-stu-id="98650-109">Manual reallocation - Allows the warehouse user to select from one or more locations with unreserved quantities of goods.</span></span> 
- <span data-ttu-id="98650-110">Automātiska un manuāla — ja sistēma nevar veikt automātisku atkārtotu sadali, un ir pieejamas atrašanās vietas ar nerezervētiem daudzumiem, lietotājam tiks rādīts uzaicinājums atlasīt atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="98650-110">Automatic and manual - If the system is unable to perform an automatic reallocation, and locations are available with unreserved quantities, the user will be prompted to select a location.</span></span>

## <a name="set-up-work-exceptions"></a><span data-ttu-id="98650-111">Iestatīt darba izņēmumus</span><span class="sxs-lookup"><span data-stu-id="98650-111">Set up work exceptions</span></span>
<span data-ttu-id="98650-112">Ir iespējams definēt vairākus darba izņēmumus ar dažādām krājumu pārdales politikām, kas ļauj noliktavas darbiniekam izvēlieties vienu, pamatojoties uz kravas apstrādes vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="98650-112">It's possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>

<span data-ttu-id="98650-113">Šīs procedūras izveidošanai tika izmantots demonstrācijas datu uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="98650-113">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="98650-114">Sadaļā **Navigācijas rūts** pārejiet uz **Noliktavas pārvaldība > Iestatīšana > Darba > Darba izņēmumi**.</span><span class="sxs-lookup"><span data-stu-id="98650-114">In the **Navigation pane**, go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="98650-115">Klikšķiniet **Jauns**</span><span class="sxs-lookup"><span data-stu-id="98650-115">Click **New**</span></span> 
3. <span data-ttu-id="98650-116">Laukā **Darba izņēmuma kods** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="98650-116">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="98650-117">Šis ir izņēmuma nosaukums.</span><span class="sxs-lookup"><span data-stu-id="98650-117">This will be the title of this exception .</span></span> <span data-ttu-id="98650-118">Piemēram, Saīsinātas izdošanas rokasgrāmata.</span><span class="sxs-lookup"><span data-stu-id="98650-118">For example, Short picking manual.</span></span>
4. <span data-ttu-id="98650-119">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="98650-119">In the **Description** field, type a value.</span></span> <span data-ttu-id="98650-120">Šis ir izņēmuma lietojuma īss apraksts.</span><span class="sxs-lookup"><span data-stu-id="98650-120">This will be a short description of the usage of this exception.</span></span> <span data-ttu-id="98650-121">Piemēram, Saīsinātā izdošana — krājums nav pieejams.</span><span class="sxs-lookup"><span data-stu-id="98650-121">For example, Short picking - item not available.</span></span>
5. <span data-ttu-id="98650-122">Veida laukā **Izņēmums** atlasiet **Saīsinātā izdošana**.</span><span class="sxs-lookup"><span data-stu-id="98650-122">In the **Exception** type field, select **Short pick**.</span></span>
6. <span data-ttu-id="98650-123">Atlasiet izvēles rūtiņu **Krājumu koriģēšana**.</span><span class="sxs-lookup"><span data-stu-id="98650-123">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="98650-124">Ja atlasīsit šo opciju, krājumi tiks automātiski noregulēti uz vērtību 0 saīsinātas izdošanas atrašanās vietā.</span><span class="sxs-lookup"><span data-stu-id="98650-124">If selected, inventory will automatically be adjusted to 0 at the short picked location.</span></span>
7. <span data-ttu-id="98650-125">Laukā **Noklusējuma korekcijas veida kods** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="98650-125">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="98650-126">Piemēram, USMF varat atlasīt **Noņemt Res Adj Out**. Katrs korekcijas tipa kods ietver četrus raksturlielumus: nosaukumu, aprakstu, krājumu žurnāla nosaukumu un **Noņemt rezervācijas**.</span><span class="sxs-lookup"><span data-stu-id="98650-126">For example, in USMF you can select **Remove Res Adj Out**. Each Adjustment type code contains four characteristics: name, description, inventory journal name, and **Remove reservations**.</span></span> <span data-ttu-id="98650-127">Ja ir iespējota opcija **Noņemt rezervācijas**, saīsināti izdotā pasūtījuma rindas rezervācijas tiks noņemtas.</span><span class="sxs-lookup"><span data-stu-id="98650-127">If **Remove reservations** is enabled, the short-picked order line's reservations will be removed.</span></span>  
8. <span data-ttu-id="98650-128">Laukā **Krājumu atkārtota sadale** atlasiet vērtību, piemēram, Manuāla.</span><span class="sxs-lookup"><span data-stu-id="98650-128">In the **Item reallocation** field, select a value, such as Manual.</span></span> <span data-ttu-id="98650-129">Ja atlasāt Manuāls vai Automātisks un manuāls, noliktavas darbiniekam jāļauj izmantot manuālu atkārtotu sadali.</span><span class="sxs-lookup"><span data-stu-id="98650-129">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="98650-130">Iestatīt darbinieku manuālas krājuma atkārtotas sadales izmantošanai</span><span class="sxs-lookup"><span data-stu-id="98650-130">Set up a worker to use manual item reallocation</span></span>

<span data-ttu-id="98650-131">Šīs procedūras izveidošanai tika izmantots demonstrācijas datu uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="98650-131">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="98650-132">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="98650-132">Close the page.</span></span>
2. <span data-ttu-id="98650-133">Sadaļā **Navigācijas rūts** pārejiet uz **Noliktavas pārvaldība > Iestatīšana > Nodarbinātais**.</span><span class="sxs-lookup"><span data-stu-id="98650-133">In the **Navigation pane**, go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="98650-134">Noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="98650-134">Click **Edit**.</span></span>
4. <span data-ttu-id="98650-135">Sarakstā atlasiet nodarbināto.</span><span class="sxs-lookup"><span data-stu-id="98650-135">In the list, select worker.</span></span> <span data-ttu-id="98650-136">Piemēram, Jūlija Funderburka.</span><span class="sxs-lookup"><span data-stu-id="98650-136">For example, Julia Funderburk.</span></span>
5. <span data-ttu-id="98650-137">Izvērsiet kopsavilkuma cilni **Lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="98650-137">Expand the **Users** FastTab.</span></span>
6. <span data-ttu-id="98650-138">Sarakstā atlasiet **Lietotāja ID**.</span><span class="sxs-lookup"><span data-stu-id="98650-138">In the list, select a **User ID**.</span></span> <span data-ttu-id="98650-139">Piemēram, 24.</span><span class="sxs-lookup"><span data-stu-id="98650-139">For example, 24.</span></span>
7. <span data-ttu-id="98650-140">Izvērsiet kopsavilkuma cilni **Darbs**.</span><span class="sxs-lookup"><span data-stu-id="98650-140">Expand the **Work** FastTab.</span></span>
8. <span data-ttu-id="98650-141">Laukā **Atļaut manuālu krājuma atkārtotu sadali** atlasiet vērtību **Jā**.</span><span class="sxs-lookup"><span data-stu-id="98650-141">Select **Yes** in the **Allow manual item reallocation** field.</span></span>
