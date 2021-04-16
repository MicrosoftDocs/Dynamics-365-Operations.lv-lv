---
title: Transportēšanas kravas daļēja nosūtīšana
description: Šajā tēmā ir paskaidrots, kā var daļēji nosūtīt kravu un atlikt kravas noslodzes plānošanu.
author: Mirzaab
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 179a784f1f02ed0840ba5219c350e274272b59eb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818948"
---
# <a name="partial-shipment-of-a-transport-load"></a><span data-ttu-id="73caf-103">Transportēšanas kravas daļēja nosūtīšana</span><span class="sxs-lookup"><span data-stu-id="73caf-103">Partial shipment of a transport load</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="73caf-104">Iestatot daļēju kravu nosūtīšanu, varat apstrādāt kravas gadījumos, kad noslodzi nevar noteikt, kamēr visas pārdošanas rindas nav pievienotas kravai.</span><span class="sxs-lookup"><span data-stu-id="73caf-104">By setting up partial shipment of loads, you can handle loads where the capacity can't be determined until all the sales lines have been added to a load.</span></span> <span data-ttu-id="73caf-105">Procesu var pabeigt, kad ir zināms precīzs palešu skaits.</span><span class="sxs-lookup"><span data-stu-id="73caf-105">The process can then be finalized when the exact pallet count is known.</span></span> <span data-ttu-id="73caf-106">Tādēļ nav jāizlemj, kuras paletes tiks piešķirtas kuram transportam, līdz brīdim, kad transportā fiziski tiek iekrauti izveidotie krājumi.</span><span class="sxs-lookup"><span data-stu-id="73caf-106">Therefore, you don't have to decide which pallets will be assigned to which transport until the moment when a transport is being physically loaded out of the staged inventory.</span></span>

<span data-ttu-id="73caf-107">Šis līdzeklis piedāvā alternatīvu stingrākas struktūras ieviešanai, kurā jums jānosaka, kuras paletes tiks piešķirtas kuram transportam, pirms var izveidot izdošanas darbu vai iekraušanas darbu.</span><span class="sxs-lookup"><span data-stu-id="73caf-107">This feature offers an alternative to the enforcement of a more rigid structure, where you must determine which pallets will be assigned to which transport before picking work or loading work can be created.</span></span> <span data-ttu-id="73caf-108">Tā vietā lietotāji var konfigurēt atsevišķas kravas daļējas nosūtīšanas apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="73caf-108">Instead, users can configure individual loads for a partial shipment confirmation.</span></span> <span data-ttu-id="73caf-109">Pēc tam var veikt transporta iekraušanas procesu attiecīgajām kravām.</span><span class="sxs-lookup"><span data-stu-id="73caf-109">The transport loading processes for those loads can then occur.</span></span> <span data-ttu-id="73caf-110">Tādēļ transportēšanas plānošanas nodaļa var plānot kravas, neņemot vērā atsevišķa transporta noslodzi.</span><span class="sxs-lookup"><span data-stu-id="73caf-110">Therefore, the transportation planning department can plan loads without having to consider the capacity of individual transports.</span></span>

<span data-ttu-id="73caf-111">Iekraušanas laikā darbinieki var definēt jaunu transportēšanas kravu, kurā var iekraut paleti.</span><span class="sxs-lookup"><span data-stu-id="73caf-111">At the time of loading, workers can define a new transport load that a pallet can be loaded to.</span></span> <span data-ttu-id="73caf-112">Vai arī tie var identificēt esošu transportēšanas kravu.</span><span class="sxs-lookup"><span data-stu-id="73caf-112">Alternatively, they can identify an existing transport load.</span></span> <span data-ttu-id="73caf-113">Šos datus var ierakstīt, izmantojot mobilo ierīci.</span><span class="sxs-lookup"><span data-stu-id="73caf-113">This data can be recorded via a mobile device.</span></span> <span data-ttu-id="73caf-114">Tādēļ vairāki noliktavas darbinieki var iekraut krājumus no tās pašas kravas vai dažādām kravām tajā pašā kravas automašīnas.</span><span class="sxs-lookup"><span data-stu-id="73caf-114">Therefore, several warehouse workers can load inventory from the same loads or different loads onto the same truck.</span></span> <span data-ttu-id="73caf-115">Pēc tam kravas var nosūtīt pilnībā vai daļēji.</span><span class="sxs-lookup"><span data-stu-id="73caf-115">The loads can then be fully or partially shipped.</span></span>

> [!NOTE] 
> <span data-ttu-id="73caf-116">Lai iekrautu krājumus no kravas noteiktā transportēšanas kravā un daļēji nosūtītu kravu, ir jāģenerē darbs, izmantojot iekraušanas klasi darba veidnē.</span><span class="sxs-lookup"><span data-stu-id="73caf-116">In order to load inventory from a load to a specific transport load and partially ship the load, work must be generated by using a loading class in a work template.</span></span> <span data-ttu-id="73caf-117">Parastu izdošanas darbu, kura tips ir **Izdošana**, nevar iekraut transportēšanas kravā, piemēram, kravas automašīnā.</span><span class="sxs-lookup"><span data-stu-id="73caf-117">Ordinary picking work of the **Picking** type can't be loaded to a transport load such as a truck.</span></span>

## <a name="set-up-transport-loads-for-partial-shipment"></a><span data-ttu-id="73caf-118">Transportēšanas kravu iestatīšana daļējai nosūtīšanai</span><span class="sxs-lookup"><span data-stu-id="73caf-118">Set up transport loads for partial shipment</span></span>

<span data-ttu-id="73caf-119">Kravu daļējas nosūtīšanas iestatīšana sastāv no divām procedūrām.</span><span class="sxs-lookup"><span data-stu-id="73caf-119">The setup for partial shipment of loads consists of the following two procedures.</span></span>

### <a name="set-the-loading-strategy"></a><span data-ttu-id="73caf-120">Iekraušanas stratēģijas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="73caf-120">Set the loading strategy</span></span>

<span data-ttu-id="73caf-121">Ir jāiespējo daļēja iekraušana, iestatot iekraušanas stratēģiju.</span><span class="sxs-lookup"><span data-stu-id="73caf-121">You must enable partial loading by setting the loading strategy.</span></span> <span data-ttu-id="73caf-122">Varat iestatīt iekraušanas stratēģiju pēc tam, kad esat izveidojis kravu.</span><span class="sxs-lookup"><span data-stu-id="73caf-122">You can set the loading strategy after you've created a load.</span></span>

1. <span data-ttu-id="73caf-123">Atlasiet **Noliktavas pārvaldība** \> **Kravas** \> **Visas kravas**.</span><span class="sxs-lookup"><span data-stu-id="73caf-123">Select **Warehouse management** \> **Loads** \> **All loads**.</span></span>
2. <span data-ttu-id="73caf-124">Atlasiet kravu un pēc tam noklikšķiniet uz **Galvene**.</span><span class="sxs-lookup"><span data-stu-id="73caf-124">Select a load, and then click **Header**.</span></span>
3. <span data-ttu-id="73caf-125">Laukā **Iekraušanas stratēģija** atlasiet **Atļauta daļējas kravas sūtīšana**.</span><span class="sxs-lookup"><span data-stu-id="73caf-125">In the **Loading strategy** field, select **Partial load shipping allowed**.</span></span>

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a><span data-ttu-id="73caf-126">Izvēlnes elementa izveide transportēšanas kravu iekraušanai</span><span class="sxs-lookup"><span data-stu-id="73caf-126">Create a menu item for loading of transport loads</span></span>

<span data-ttu-id="73caf-127">Ir jāizveido jauns izvēlnes elements, kas ļauj veikt transportēšanas kravu iekraušanu.</span><span class="sxs-lookup"><span data-stu-id="73caf-127">You must create a new menu item that enables transport loads to be loaded.</span></span> <span data-ttu-id="73caf-128">Transportēšanas kravas ļauj grupēt darba rindas no vienas vai vairākām kravām.</span><span class="sxs-lookup"><span data-stu-id="73caf-128">A transport load lets you group work lines from one load or multiple loads.</span></span> <span data-ttu-id="73caf-129">Visu, kas tiek pievienots transportēšanas kravai, pēc tam var nosūtīt, izmantojot mobilo skeneri.</span><span class="sxs-lookup"><span data-stu-id="73caf-129">Everything that is added to the transport load can then be shipped by using a mobile scanner.</span></span>

1. <span data-ttu-id="73caf-130">Atlasiet **Noliktavas pārvaldība** \> **Iestatīšana** \> **Mobilā ierīce** \> **Mobilās ierīces izvēlnes elementi**.</span><span class="sxs-lookup"><span data-stu-id="73caf-130">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="73caf-131">Atlasiet **Jauns** un pēc tam laukā **Režīms** atlasiet **Darbs**.</span><span class="sxs-lookup"><span data-stu-id="73caf-131">Select **New**, and then, in the **Mode** field, select **Work**.</span></span>
3. <span data-ttu-id="73caf-132">Iestatiet opciju **Izmantot esošo darbu** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="73caf-132">Set the **Use existing work** option to **Yes**.</span></span>
4. <span data-ttu-id="73caf-133">Cilnes **Vispārīgi** laukā **Novirzītājs** atlasiet **Transporta iekraušana**.</span><span class="sxs-lookup"><span data-stu-id="73caf-133">On the **General** tab, in the **Directed by** field, select **Transport loading**.</span></span>
5. <span data-ttu-id="73caf-134">Lai iespējotu sūtījuma apstiprinājumu, izmantojot mobilo skeneri, laukā **Atļautais nosūtīšanas apstiprināšanas tips** atlasiet vienumu **Transportēšanas krava**.</span><span class="sxs-lookup"><span data-stu-id="73caf-134">To enable shipment confirmation on a mobile scanner, in the **Allowed ship confirmation type** field, select **Transport load**.</span></span>

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a><span data-ttu-id="73caf-135">Transportēšanas kravas nosūtīšanas apstiprināšana no klienta</span><span class="sxs-lookup"><span data-stu-id="73caf-135">Confirm shipment of a transport load from the client</span></span>

<span data-ttu-id="73caf-136">Šis iestatījums ļauj apstiprināt nosūtīšanai tādas transportēšanas kravas, kurās ir pilna vai daļēja krava.</span><span class="sxs-lookup"><span data-stu-id="73caf-136">This setup lets you confirm a transport load that includes a full load or a partially loaded load to be shipped.</span></span>

1. <span data-ttu-id="73caf-137">Atlasiet **Noliktavas pārvaldība** \> **Kravas** \> **Transportēšanas kravas**.</span><span class="sxs-lookup"><span data-stu-id="73caf-137">Select **Warehouse management** \> **Loads** \> **Transport loads**.</span></span>
2. <span data-ttu-id="73caf-138">Darbību rūtī, cilnē **Nosūtīt un saņemt**, grupā **Apstiprināt** atlasiet **Transportēšana**.</span><span class="sxs-lookup"><span data-stu-id="73caf-138">On the Action Pane, on the **Ship and receive** tab, in the **Confirm** group, select **Transport**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]