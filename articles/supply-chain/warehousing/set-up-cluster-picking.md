---
title: Klastera izdošanas iestatīšana
description: Šajā tēmā ir aprakstīts, kā iestatīt klastera izdošanu un kā piemērot krājumu apstiprinājumu ar klastera izdošanu.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm, WHSWorkCluster
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b3df8cf5e63fe97925f17001e836a41c703dfc9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239234"
---
# <a name="set-up-cluster-picking"></a><span data-ttu-id="d0a27-103">Klastera izdošanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d0a27-103">Set up cluster picking</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d0a27-104">Šajā tēmā aprakstīts, kā darbiniekiem nodrošināt iespēju izmantot mobilās ierīces izdošanas darbu grupēšanai klasteros, lai krājumus varētu izdot no vienas atrašanās vietas vienlaikus vairākiem darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="d0a27-104">This topic describes how to enable workers to use their mobile devices to group picking work into clusters, so that they can pick items from a single location for multiple work orders at the same time.</span></span> <span data-ttu-id="d0a27-105">To dēvē par *klastera izdošanu*.</span><span class="sxs-lookup"><span data-stu-id="d0a27-105">This is called *cluster picking*.</span></span>

## <a name="about-cluster-picking"></a><span data-ttu-id="d0a27-106">Par klastera izdošanu</span><span class="sxs-lookup"><span data-stu-id="d0a27-106">About cluster picking</span></span>

<span data-ttu-id="d0a27-107">Kad darba pasūtījumi ir nodoti nosūtīšanai uz noliktavu, darbinieks var izmantot mobilo ierīci, lai pasūtījumus piešķirtu klasterim.</span><span class="sxs-lookup"><span data-stu-id="d0a27-107">After work orders are released to the warehouse, the worker can use a mobile device to assign the orders to a cluster.</span></span> <span data-ttu-id="d0a27-108">Klasterī darbiniekam tiks organizēts izdošanas darbs.</span><span class="sxs-lookup"><span data-stu-id="d0a27-108">The cluster will organize the picking work for the worker.</span></span> <span data-ttu-id="d0a27-109">Kad darba pasūtījums ir piešķirts klasterim, darbiniekam jāizmanto klastera izdošana, lai izpildītu pasūtījuma izdošanas darbu.</span><span class="sxs-lookup"><span data-stu-id="d0a27-109">When a work order is assigned to a cluster, the worker must use cluster picking to perform the picking work for the order.</span></span> <span data-ttu-id="d0a27-110">Darbinieks nevar izmantot citas izdošanas metodes.</span><span class="sxs-lookup"><span data-stu-id="d0a27-110">The worker cannot use other picking methods.</span></span> <span data-ttu-id="d0a27-111">Ja darba pasūtījums tiek piešķirts klasterim kļūdas dēļ, darbiniekam klasteris ir jāsadala un pēc tam tas no jauna jāizveido.</span><span class="sxs-lookup"><span data-stu-id="d0a27-111">If a work order is assigned to a cluster by mistake, the worker must break the cluster and then re-create it.</span></span>

<span data-ttu-id="d0a27-112">Ja nepieciešams, darbinieks var nodot klasteri citam darbiniekam.</span><span class="sxs-lookup"><span data-stu-id="d0a27-112">If needed, a worker can pass a cluster to another worker.</span></span> <span data-ttu-id="d0a27-113">Tādējādi klastera statuss tiek mainīts uz Nodots.</span><span class="sxs-lookup"><span data-stu-id="d0a27-113">This changes the cluster status to Passed.</span></span> <span data-ttu-id="d0a27-114">Kad nodarbinātais izmanto mobilo ierīci, lai norādītu, ka izdošanas un izvietošanas darbs ir pabeigts, sūtījums vai krava ir jāapstiprina klientā.</span><span class="sxs-lookup"><span data-stu-id="d0a27-114">When the worker uses a mobile device to indicate that the picking and put away work is completed, the shipment or load must be confirmed in the client.</span></span>

## <a name="enable-cluster-picking"></a><span data-ttu-id="d0a27-115">Klastera izdošanas iespējošana</span><span class="sxs-lookup"><span data-stu-id="d0a27-115">Enable cluster picking</span></span>

<span data-ttu-id="d0a27-116">Lai iespējotu klastera izdošanu, jāveic tālāk norādītie iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="d0a27-116">To enable cluster picking, you must set up the following:</span></span>

- <span data-ttu-id="d0a27-117">**Klastera profili** – norādiet, vai automātiski ģenerēt klastera ID, izmantojamo pozīciju skaitu, kad klasterus sadalīt, kā izveidot izdošanas darba secību un kā šo darbu pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="d0a27-117">**Cluster profiles** – Specify whether to automatically generate cluster   IDs, the number of positions to use, when to break clusters, and how to   sequence and verify the picking work.</span></span>

- <span data-ttu-id="d0a27-118">**Darbu veidnes** — definējiet, kā izveidot izdošanas darbu klastera izdošanai.</span><span class="sxs-lookup"><span data-stu-id="d0a27-118">**Work templates** – Define how to create the picking work for cluster   picking.</span></span>

- <span data-ttu-id="d0a27-119">**Novietojuma direktīvas** — norādiet, no kurienes saņemt krājumus un kur tos novietot.</span><span class="sxs-lookup"><span data-stu-id="d0a27-119">**Location directives** – Specify where to pick items from, and where to put   them.</span></span>

- <span data-ttu-id="d0a27-120">**Mobilās ierīces izvēlnes vienumi** — konfigurējiet mobilās ierīces izvēlnes vienumu, lai izmantotu esošu darbu, ko novirzījusi klastera izdošana.</span><span class="sxs-lookup"><span data-stu-id="d0a27-120">**Mobile device menu items** – Configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="d0a27-121">Pēc tam izvēlnes vienums jāpievieno mobilās ierīces izvēlnei, lai tas tiktu parādīts mobilajās ierīcēs.</span><span class="sxs-lookup"><span data-stu-id="d0a27-121">You must then add the menu item to a mobile device menu so that it is displayed on mobile devices.</span></span>

- <span data-ttu-id="d0a27-122">**Noliktavas vadības parametri** — norādiet izmantojamo numuru sēriju, ja vēlaties klasteriem ģenerēt identifikatorus.</span><span class="sxs-lookup"><span data-stu-id="d0a27-122">**Warehouse management parameters** – Specify the number sequence to use if   you want to generate identifiers for clusters.</span></span>

## <a name="set-up-a-cluster-profile"></a><span data-ttu-id="d0a27-123">Klastera profila iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d0a27-123">Set up a cluster profile</span></span>

<span data-ttu-id="d0a27-124">Lai iestatītu klastera profilu, veiciet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="d0a27-124">To set up a cluster profile, follow these steps:</span></span>

1. <span data-ttu-id="d0a27-125">Noklikšķiniet uz **Noliktavas vadība** \> **Iestatīšana** \> **Mobilā ierīce** \>  **Klastera profili**.</span><span class="sxs-lookup"><span data-stu-id="d0a27-125">Click **Warehouse management** \> **Setup** \> **Mobile device** \>  **Cluster profiles**.</span></span>

1. <span data-ttu-id="d0a27-126">Noklikšķiniet uz **Jauns**, lai izveidotu jaunu profilu.</span><span class="sxs-lookup"><span data-stu-id="d0a27-126">Click **New** to create a new profile.</span></span>

1. <span data-ttu-id="d0a27-127">Noklikšķiniet uz **Izveidot klasteri** un sadaļā **Klastera kārtošana** noklikšķiniet uz **Jauns**, lai klasterim iestatītu kārtošanas kritērijus.</span><span class="sxs-lookup"><span data-stu-id="d0a27-127">Click **Create cluster** and, under **Cluster sorting**, click **New** to set up the sorting criteria for the cluster.</span></span> <span data-ttu-id="d0a27-128">Kārtošanas kritēriji kontrolē kārtību, kādā darbinieks veiks izdošanas darbu.</span><span class="sxs-lookup"><span data-stu-id="d0a27-128">The sorting criteria control the order in which the worker will perform the picking work.</span></span> <span data-ttu-id="d0a27-129">Varat pievienot tik daudz kritērijus, cik nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="d0a27-129">You can add as many criteria as needed.</span></span>

1. <span data-ttu-id="d0a27-130">Laukā **Sērijas numurs** ievadiet numuru, lai definētu kārtību, kādā tiek apstrādāti kārtošanas kritēriji.</span><span class="sxs-lookup"><span data-stu-id="d0a27-130">In the **Sequence number** field, enter a number to define the order in  which the sorting criteria are processed.</span></span>

1. <span data-ttu-id="d0a27-131">Laukā **Lauka nosaukums** atlasiet lauku, kas noteiks kārtošanu.</span><span class="sxs-lookup"><span data-stu-id="d0a27-131">In the **Field name** field, select the field that will determine the sorting.</span></span> <span data-ttu-id="d0a27-132">Piemēram, atlasot lauku **WMSLocationId**, darbs tiks kārtots pēc atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="d0a27-132">For example, if you select the **WMSLocationId** field, the work will be sorted by location.</span></span>

1. <span data-ttu-id="d0a27-133">Laukā **Kārtošana** atlasiet vienu no tālāk norādītajām opcijām.</span><span class="sxs-lookup"><span data-stu-id="d0a27-133">In the **Sorting** field, select one of the following options.</span></span>

| <span data-ttu-id="d0a27-134">**Opcija**</span><span class="sxs-lookup"><span data-stu-id="d0a27-134">**Option**</span></span>     | <span data-ttu-id="d0a27-135">**Apraksts**</span><span class="sxs-lookup"><span data-stu-id="d0a27-135">**Description**</span></span>                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0a27-136">**Pieaugošā secībā**</span><span class="sxs-lookup"><span data-stu-id="d0a27-136">**Ascending**</span></span>  | <span data-ttu-id="d0a27-137">Izdošanas darbs tiek kārtots augošā secībā, pamatojoties uz kārtošanas kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="d0a27-137">Picking work is sequenced in ascending order based on the sorting criteria.</span></span> <span data-ttu-id="d0a27-138">Piemēram, ja kā kārtošanas kritērijus izmantojat lauku **WMSLocationId** un vietas ID ir 1, 2, 3 un 4, izdošana vispirms notiks no 4. atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="d0a27-138">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 4 first.</span></span> |
| <span data-ttu-id="d0a27-139">**Dilstošā kārtībā**</span><span class="sxs-lookup"><span data-stu-id="d0a27-139">**Descending**</span></span> | <span data-ttu-id="d0a27-140">Izdošanas darbs tiek kārtots dilstošā secībā, pamatojoties uz kārtošanas kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="d0a27-140">Picking work is sequenced in descending order based on the sorting criteria.</span></span> <span data-ttu-id="d0a27-141">Piemēram, ja kā kārtošanas kritērijus izmantojat lauku **WMSLocationId** un vietas ID ir 1, 2, 3 un 4, izdošana vispirms notiks no 1. atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="d0a27-141">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 1 first.</span></span> |

## <a name="item-confirmation"></a><span data-ttu-id="d0a27-142">Krājuma apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="d0a27-142">Item confirmation</span></span>

<span data-ttu-id="d0a27-143">Ja tiek lietota klasteru izdošana, ir svarīgi veikt krājumu apstiprināšanu, lai pārbaudītu klasteriem pievienotos krājumus.</span><span class="sxs-lookup"><span data-stu-id="d0a27-143">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="d0a27-144">Varat pārbaudīt klastera izdošanā ietvertos krājumus klastera izdošanas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="d0a27-144">You can verify items in cluster picking during the cluster picking process.</span></span> <span data-ttu-id="d0a27-145">Iestatīšana tiek veikta, pamatojoties uz preču svītrkodu iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="d0a27-145">The setup is based on the product bar code setup.</span></span>

### <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="d0a27-146">Krājumu pārbaudes klastera izdošanai iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d0a27-146">Set up item verification with cluster picking</span></span>

1. <span data-ttu-id="d0a27-147">Mobilās ierīces izvēlnes vienumā atveriet iestatīšanas formu darba apstiprināšanai:  **Noliktavas pārvaldība** \> **Noliktavas pārvaldība** \> **Iestatījumi** \>  **Mobilā ierīce** \> **Mobilās ierīces izvēlnes vienumi**.</span><span class="sxs-lookup"><span data-stu-id="d0a27-147">On a mobile device menu item, open the setup form for work confirmation:  **Warehouse management** \> **Warehouse management** \> **Setup** \>  **Mobile device** \> **Mobile device menu items**.</span></span>

1. <span data-ttu-id="d0a27-148">Mobilās ierīces izvēlnes vienumā atveriet sadaļu **Darba apstiprinājuma iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="d0a27-148">From the mobile device menu item, open **Work confirmation setup**.</span></span> <span data-ttu-id="d0a27-149">Opcija **Preces apstiprināšana** jums ļauj skenēšanas laikā mobilajā ierīcē pārbaudīt katru krājumu vienību.</span><span class="sxs-lookup"><span data-stu-id="d0a27-149">The **Product confirmation** option allows you to verify each piece of inventory from the mobile device when scanned.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]