---
title: Papildu novietojuma zonas
description: Šajā tēmā ir sniegts pārskats par jaunajām novietojuma zonām, kas tika pievienotas Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 6cf81939989b8faffcda51bbbd5bc6b27aec7eea
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016312"
---
# <a name="additional-location-zones"></a><span data-ttu-id="cc5bd-103">Papildu novietojuma zonas</span><span class="sxs-lookup"><span data-stu-id="cc5bd-103">Additional location zones</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc5bd-104">Trīs jauni zonu lauki ir pieejami Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cc5bd-104">Three new zone fields are available in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="cc5bd-105">Noliktavas pārvaldnieki tos var izmantot, lai definētu papildu noliktavas organizācijas vai izkārtojumus.</span><span class="sxs-lookup"><span data-stu-id="cc5bd-105">Warehouse managers can use them to define additional warehouse organizations or layouts.</span></span> <span data-ttu-id="cc5bd-106">Jaunos zonu laukus var iestatīt manuāli, vai izmantojot vedni **Novietojuma iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="cc5bd-106">The new zone fields can be set either manually or by using the **Location setup** wizard.</span></span> <span data-ttu-id="cc5bd-107">Tos var izmantot jebkurā vaicājumā vai filtrēšanā, kas izmanto tabulu Novietojumi.</span><span class="sxs-lookup"><span data-stu-id="cc5bd-107">They can be used in any query or filtering that uses the Locations table.</span></span>

<span data-ttu-id="cc5bd-108">Lai izmantotu zonu laukus, papildu iestatījumi nav nepieciešami.</span><span class="sxs-lookup"><span data-stu-id="cc5bd-108">No additional setup is required to use the zone fields.</span></span>

## <a name="turn-on-the-additional-location-zone-feature"></a><span data-ttu-id="cc5bd-109">Līdzekļa Papildu novietojuma zona ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="cc5bd-109">Turn on the Additional location zone feature</span></span>

<span data-ttu-id="cc5bd-110">Lai varētu izmantot līdzekli *Papildu novietojuma zona* , tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="cc5bd-110">Before you can use the *Additional location zone* feature, it must be turned on in your system.</span></span> <span data-ttu-id="cc5bd-111">Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="cc5bd-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="cc5bd-112">Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:</span><span class="sxs-lookup"><span data-stu-id="cc5bd-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="cc5bd-113">**Modulis:** *Noliktavas vadība*</span><span class="sxs-lookup"><span data-stu-id="cc5bd-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="cc5bd-114">**Līdzekļa nosaukums:** *Papildu novietojuma zona*</span><span class="sxs-lookup"><span data-stu-id="cc5bd-114">**Feature name:** *Additional location zone*</span></span>

## <a name="use-location-zones"></a><span data-ttu-id="cc5bd-115">Novietojuma zonu izmantošana</span><span class="sxs-lookup"><span data-stu-id="cc5bd-115">Use location zones</span></span>

1. <span data-ttu-id="cc5bd-116">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Novietojuma iestatīšanas vednis**.</span><span class="sxs-lookup"><span data-stu-id="cc5bd-116">Go to **Warehouse management \> Setup \> Warehouse \> Location setup wizard**.</span></span>
2. <span data-ttu-id="cc5bd-117">Iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="cc5bd-117">Set the following values:</span></span>

    - <span data-ttu-id="cc5bd-118">Laukā **Noliktava** atlasiet _62_.</span><span class="sxs-lookup"><span data-stu-id="cc5bd-118">In the **Warehouse** field, select _62_.</span></span>
    - <span data-ttu-id="cc5bd-119">Laukā **Zonas ID** atlasiet _FLOOR_.</span><span class="sxs-lookup"><span data-stu-id="cc5bd-119">In the **Zone ID** field, select _FLOOR_.</span></span>
    - <span data-ttu-id="cc5bd-120">Laukā **Papildu zona 1** atlasiet _PICKZONE1_.</span><span class="sxs-lookup"><span data-stu-id="cc5bd-120">In the **Additional Zone 1** field, select _PICKZONE1_.</span></span>
    - <span data-ttu-id="cc5bd-121">Laukā **Papildu zona 2** atlasiet _WEBSHOP1_.</span><span class="sxs-lookup"><span data-stu-id="cc5bd-121">In the **Additional Zone 2** field, select _WEBSHOP1_.</span></span>
    - <span data-ttu-id="cc5bd-122">Laukā **Novietojuma profila ID** atlasiet _FLOOR_.</span><span class="sxs-lookup"><span data-stu-id="cc5bd-122">In the **Location profile ID** field, select _FLOOR_.</span></span>

3. <span data-ttu-id="cc5bd-123">Atlasiet rindu **Stāvs**.</span><span class="sxs-lookup"><span data-stu-id="cc5bd-123">Select the **Floor** line.</span></span>
4. <span data-ttu-id="cc5bd-124">Laukā **No numura** ievadiet _1_.</span><span class="sxs-lookup"><span data-stu-id="cc5bd-124">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="cc5bd-125">Laukā **Līdz numuram** ievadiet _3_.</span><span class="sxs-lookup"><span data-stu-id="cc5bd-125">In the **To number** field, enter _3_.</span></span>
5. <span data-ttu-id="cc5bd-126">Atlasiet rindu **Aile**.</span><span class="sxs-lookup"><span data-stu-id="cc5bd-126">Select the **Aisle** line.</span></span>
6. <span data-ttu-id="cc5bd-127">Laukā **No numura** ievadiet _1_.</span><span class="sxs-lookup"><span data-stu-id="cc5bd-127">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="cc5bd-128">Laukā **Līdz numuram** ievadiet _5_.</span><span class="sxs-lookup"><span data-stu-id="cc5bd-128">In the **To number** field, enter _5_.</span></span>
7. <span data-ttu-id="cc5bd-129">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="cc5bd-129">Select **Create**.</span></span>
8. <span data-ttu-id="cc5bd-130">Tiek saņemti ziņojumi, norādot, ka jaunie novietojumi ir pievienoti.</span><span class="sxs-lookup"><span data-stu-id="cc5bd-130">You receive messages that state that new locations have been added.</span></span> <span data-ttu-id="cc5bd-131">Atlasiet pogu **Rādīt ziņojumus** , lai skatītu ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="cc5bd-131">Select the **Show messages** button to view the messages.</span></span>
9. <span data-ttu-id="cc5bd-132">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Novietojums**.</span><span class="sxs-lookup"><span data-stu-id="cc5bd-132">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span> <span data-ttu-id="cc5bd-133">Jaunie novietojumi tiek parādīti sarakstā un visu zonu lauki ir pieejami (tas ir, esošas zonas lauks un jaunie papildu zonu lauki).</span><span class="sxs-lookup"><span data-stu-id="cc5bd-133">The new locations appear in the list, and all zone fields are available (that is, the existing zone field and the new additional zone fields).</span></span>
