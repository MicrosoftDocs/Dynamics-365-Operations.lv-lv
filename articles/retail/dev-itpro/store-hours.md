---
title: Veikala darbalaika izveide un atjaunināšana
description: Šajā tēmā ir aprakstīts, kā izveidot un atjaunināt darbalaiku programmā Retail Headquarters.
author: josaw1
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 811d499a3eb8133e5ffd29bb4ae6a0c57708accd
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023446"
---
# <a name="create-and-update-store-hours"></a><span data-ttu-id="6e1cf-103">Veikala darbalaika izveide un atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="6e1cf-103">Create and update store hours</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="6e1cf-104">Kopsavilkums</span><span class="sxs-lookup"><span data-stu-id="6e1cf-104">Overview</span></span>

<span data-ttu-id="6e1cf-105">Vienā vietā mazumtirgotāji var izveidot, uzturēt un pārvaldīt veikala darbalaiku dažādiem veikaliem visos ģeogrāfiskajos reģionos.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-105">From a single place, retailers can create, maintain, and manage the store hours for different stores across geographic regions.</span></span> <span data-ttu-id="6e1cf-106">Veikala darbalaiks var tikt rādīts pārdošanas punkta (POS) termināļos.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-106">The store hours can then be shown on point of sale (POS) terminals.</span></span> <span data-ttu-id="6e1cf-107">Šādā veidā kasieri var koplietot veikala darbalaiku ar klientiem un labāk palīdzēt pircējiem, kas interesējas par krājumiem citos veikalos.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-107">In this way, cashiers can share store hours with customers and better help shoppers who are interested in inventory in other stores.</span></span> <span data-ttu-id="6e1cf-108">Veikala darbalaiku var drukāt arī ieejas plūsmās, ja klienti vēlas atgriezties veikalā vēlāk.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-108">The store hours can also be printed on receipts, in case customers want to return to the store later.</span></span>

<span data-ttu-id="6e1cf-109">Vairākus darbalaikus ir iespējams konfigurēt dažādos kanālos.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-109">Multiple store hours can be configured across different channels.</span></span> <span data-ttu-id="6e1cf-110">Šie kanāli ietver fiziskus veikalus, zvanu centrus, mobilās ierīces un e-komercijas vietnes.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-110">These channels include brick-and-mortar stores, call centers, mobile devices, and e-Commerce sites.</span></span>

<span data-ttu-id="6e1cf-111">Ja klientam ir paņemšanas pasūtījums citam veikalam, kasieris var izvēlēties datumus, kad paņemšana būs pieejama šajā veikalā.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-111">If a customer has a pickup order for a different store, the cashier can select dates when the pickup will be available in that store.</span></span> <span data-ttu-id="6e1cf-112">Veikala uzmeklēšanā tiks sniegta atsauce uz datumiem un veikalu laikiem.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-112">The store lookup will provide a reference to the dates and store times.</span></span> <span data-ttu-id="6e1cf-113">Kasieris var atlasīt datumu un vietu, kā arī izdrukāt saņemšanas kvīti, kurā iekļauts veikala darbalaiks.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-113">The cashier can select a date and location, and can also print a pickup receipt that includes the store hours.</span></span>

<span data-ttu-id="6e1cf-114">Šī funkcionalitāte ir pieejama tikai programmas Microsoft Dynamics 365 Retail versijā 8.1.2 un jaunākās.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-114">This functionality is available in Microsoft Dynamics 365 Retail versions 8.1.2 and later.</span></span>

## <a name="configure-store-hours"></a><span data-ttu-id="6e1cf-115">Veikala darba laika konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="6e1cf-115">Configure store hours</span></span>

<span data-ttu-id="6e1cf-116">Izpildiet tālāk norādītās darbības, lai konfigurētu veikala darbalaiku.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-116">Follow these steps to configure store hours.</span></span>

1. <span data-ttu-id="6e1cf-117">Pārejiet uz **Mazumtirdzniecība** \> **Kanāla iestatīšana** \> **Veikala darbalaiks**.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-117">Go to **Retail** \> **Channel Setup** \> **Store hours**.</span></span>
2. <span data-ttu-id="6e1cf-118">Atlasiet **Jauns**, lai izveidotu jaunu veikala darbalaika veidni.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-118">Select **New** to create a new store hours template.</span></span> <span data-ttu-id="6e1cf-119">Lai izmantotu esošu veidni, atlasiet veidni kreisajā rūtī.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-119">To use an existing template, select the template in the left pane.</span></span>
3. <span data-ttu-id="6e1cf-120">Dialoglodziņā **Pievienot diapazonu** definējiet datuma diapazonu, veikala darbalaiku un nepieciešamās brīvdienas.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-120">In the **Add range** dialog box, define the date range, the store hours, and any holidays that are required.</span></span>

    - <span data-ttu-id="6e1cf-121">Ja veikala darbalaiks nemainās, atlasiet **Nekad nebeidzas** laukā **Beigu datums**.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-121">If store hours don't change, select **Never ends** in the **End date** field.</span></span>
    - <span data-ttu-id="6e1cf-122">Ja veikala darbalaiks ir noteikts mēnesis, nedēļa vai diena, iestatiet atbilstošos datumus laukos **Sākuma datums** un **Beigu datums**.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-122">If the store hours are for a specific month, week, or day, set the appropriate dates in the **Start Date** and **End date** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6e1cf-123">Varat izveidot vairākas veidnes, kuru sākuma un beigu datumi pārklājas.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-123">You can create multiple templates that have overlapping start and end dates.</span></span> <span data-ttu-id="6e1cf-124">Tāpēc jūs, piemēram, varat noteikt veikala darbalaiku veikaliem dažādās laika joslās.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-124">Therefore, you can, for example, define store hours for stores in different time zones.</span></span>

    <span data-ttu-id="6e1cf-125">![Dialoglodziņš Pievienot diapazonu](../dev-itpro/media/Storehours1.png "Dialoglodziņš Pievienot diapazonu")</span><span class="sxs-lookup"><span data-stu-id="6e1cf-125">![Add range dialog box](../dev-itpro/media/Storehours1.png "Add range dialog box")</span></span>

4. <span data-ttu-id="6e1cf-126">Saistiet veikals darbalaika veidni ar veikaliem, kur tā tiks izmantota.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-126">Associate the store hours template with the stores where it will be used.</span></span> <span data-ttu-id="6e1cf-127">Dialoglodziņā **Izvēlēties organizācijas mezglus**, atlasiet veikalus, reģionus un organizācijas, ar kurām veidne jāsaista.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-127">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>

    - <span data-ttu-id="6e1cf-128">Ar katru veikalu var saistīt tikai vienu veikala darbalaika veidni.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-128">Only one store hours template can be associated with each store.</span></span>
    - <span data-ttu-id="6e1cf-129">Izmantojiet bulttaustiņus, lai atlasītu veikalus, reģionus vai organizācijas.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-129">Use the arrow buttons to select stores, regions, or organizations.</span></span> <span data-ttu-id="6e1cf-130">Kalendārs būs pieejams veikaliem vai veikalu grupām, un tas atsaucei būs redzams pārdošanas punktos.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-130">The calendar will be available to the stores or store groups, and it will be visible at the POS for reference.</span></span>

    <span data-ttu-id="6e1cf-131">![Dialoglodziņš Izvēlēties organizāciju mezglus](../dev-itpro/media/Storehours2.png "Dialoglodziņš Izvēlēties organizāciju mezglus")</span><span class="sxs-lookup"><span data-stu-id="6e1cf-131">![Choose organization nodes dialog box](../dev-itpro/media/Storehours2.png "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="6e1cf-132">Lapā **Izplatīšanas grafiks** izpildiet uzdevumus **1070** un **1090**, lai veikala darbalaiks būtu redzams pārdošanas punktos.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-132">On the **Distribution schedule** page, run the **1070** and **1090** jobs to make the store hours available to the POS.</span></span>

## <a name="add-store-hours-to-printed-receipts"></a><span data-ttu-id="6e1cf-133">Veikala darbalaika pievienošana drukātajām kvītīm</span><span class="sxs-lookup"><span data-stu-id="6e1cf-133">Add store hours to printed receipts</span></span>

<span data-ttu-id="6e1cf-134">Veiciet šīs darbības, lai pievienotu veikala darbalaiku drukātajām pārdošanas punkta kvītīm.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-134">Follow these steps to add store hours to the printed POS receipts.</span></span>

1. <span data-ttu-id="6e1cf-135">Atveriet kvīšu noformētāju.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-135">Open the receipt designer.</span></span>
2. <span data-ttu-id="6e1cf-136">Atlasiet **Kājene** apakšējā kreisajā stūrī.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-136">Select **Footer** in the lower-left corner.</span></span>
3. <span data-ttu-id="6e1cf-137">Velciet elementu **Veikala darbalaiks** no kreisās rūts līdz kājenei kvīts veidnes apakšā.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-137">Drag the **Store hours** element from the left pane to the footer at the bottom of the receipt template.</span></span>
4. <span data-ttu-id="6e1cf-138">Jūs varat rediģēt noklusējuma etiķeti elementā **Veikala darbalaiks**, kā vēlaties.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-138">You can edit the default label on the **Store hours** element as you require.</span></span>
5. <span data-ttu-id="6e1cf-139">Saglabājiet kvīti un aizveriet kvīšu noformētāju.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-139">Save the receipt, and close the receipt designer.</span></span>
6. <span data-ttu-id="6e1cf-140">Lapā **Izplatīšanas grafiks** izpildiet uzdevumus **1070** un **1090**.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-140">On the **Distribution schedule** page, run the **1070** and **1090** jobs.</span></span>
7. <span data-ttu-id="6e1cf-141">Pierakstieties pārdošanas punktā (POS).</span><span class="sxs-lookup"><span data-stu-id="6e1cf-141">Sign in to the POS.</span></span>
8. <span data-ttu-id="6e1cf-142">Izpildiet pārdošanu un izdrukājiet kvīti.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-142">Complete a sale, and select to print a receipt.</span></span>

<span data-ttu-id="6e1cf-143">Tagad pārdošanas punktu kvītis ietver veikala darbalaiku.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-143">POS receipts now include the store hours.</span></span> <span data-ttu-id="6e1cf-144">Ja veidnē tika iekļautas brīvdienas, tās tiek parādītas kvītī.</span><span class="sxs-lookup"><span data-stu-id="6e1cf-144">If any holidays were included in the template, they are shown on the receipt.</span></span>

<span data-ttu-id="6e1cf-145">![Kvīts piemērs](../dev-itpro/media/Storehours3.png "Kvīts piemērs")</span><span class="sxs-lookup"><span data-stu-id="6e1cf-145">![Receipt example](../dev-itpro/media/Storehours3.png "Receipt example")</span></span>
