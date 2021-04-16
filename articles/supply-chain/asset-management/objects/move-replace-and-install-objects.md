---
title: Līdzekļu pārvietošana, aizstāšana un uzstādīšana
description: Šajā tēmā paskaidrots, kā pārvietot, aizstāt un uzstādīt līdzekļus Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectReplace, EntAssetObjectInstallLookup, EntAssetObjectMove, EntAssetObjectTableEditSubObjects
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6d7a9c86029505602c562a3de4d2f52eace866f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808548"
---
# <a name="move-replace-and-install-assets"></a><span data-ttu-id="13fe4-103">Līdzekļu pārvietošana, aizstāšana un uzstādīšana</span><span class="sxs-lookup"><span data-stu-id="13fe4-103">Move, replace, and install assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="13fe4-104">Šajā tēmā paskaidrots, kā pārvietot, aizstāt un uzstādīt līdzekļus Līdzekļu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="13fe4-104">This topic explains how to move, replace, and install assets in Asset Management.</span></span> <span data-ttu-id="13fe4-105">Varat izveidot atsevišķus līdzekļus, kas nav saistīti ar citiem līdzekļiem, vai arī varat izveidot līdzekļu struktūru, kas ietver primāro līdzekli (augšējā līmeņa līdzeklis) un saistītos pakārtotos līdzekļus (apakšlīdzekļus).</span><span class="sxs-lookup"><span data-stu-id="13fe4-105">You can create individual assets that have no relations to other assets, or you can create an asset structure that includes a parent asset (top-level asset) and related child assets (sub-assets).</span></span> <span data-ttu-id="13fe4-106">Līdzekļu pārvaldībā ir trīs pieejas, kā pārvietot un mainīt līdzekļa atrašanās vietu:</span><span class="sxs-lookup"><span data-stu-id="13fe4-106">In Asset Management, there are three approaches to moving and changing the location of an asset:</span></span>

- <span data-ttu-id="13fe4-107">**Pārvietot** — pārvietojiet līdzekļus uz citu līdzekļu struktūru vai uz citu atrašanās vietu tajā pašā līdzekļu struktūrā.</span><span class="sxs-lookup"><span data-stu-id="13fe4-107">**Move** – Move an asset either to another asset structure or to another location in the same asset structure.</span></span>
- <span data-ttu-id="13fe4-108">**Aizstāt** — īslaicīgi noņemt līdzekli no līdzekļu struktūras, lai to varētu labot vai atjaunot, un pēc tam vēlāk pievienot atjaunoto līdzekli atpakaļ līdzekļu struktūrai.</span><span class="sxs-lookup"><span data-stu-id="13fe4-108">**Replace** – Temporarily remove an asset from an asset structure so that it can be repaired or refurbished, and then add the refurbished asset back to the asset structure later.</span></span> <span data-ttu-id="13fe4-109">Varat arī neatgriezeniski aizstāt izmantotu līdzekli ar jaunu līdzekli.</span><span class="sxs-lookup"><span data-stu-id="13fe4-109">Alternatively, permanently replace a used asset with a new asset.</span></span>
- <span data-ttu-id="13fe4-110">**Uzstādīt** — uzstādīt līdzekli un visus saistītos pakārtotos līdzekļus funkcionālā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="13fe4-110">**Install** – Install a parent asset and any related child assets on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="13fe4-111">Līdzeklis, kuru pārvietojat, aizstājat vai uzstādāt, var būt saistīts ar citu funkcionālo novietojumu.</span><span class="sxs-lookup"><span data-stu-id="13fe4-111">The asset that you move, replace, or install might be related to another functional location.</span></span> <span data-ttu-id="13fe4-112">Šādā gadījumā līdzeklis var izmantot funkcionālā novietojuma finanšu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="13fe4-112">In that case, the asset might use financial dimensions of the functional location.</span></span> <span data-ttu-id="13fe4-113">Lapā **Funkcionālā novietojuma veidi** varat iestatīt finanšu dimensiju izmantošanu funkcionālajos novietojumos.</span><span class="sxs-lookup"><span data-stu-id="13fe4-113">On the **Functional location types** page, you set up the handling of financial dimensions on functional locations.</span></span>

## <a name="move-asset"></a><span data-ttu-id="13fe4-114">Līdzekļa pārvietošana</span><span class="sxs-lookup"><span data-stu-id="13fe4-114">Move asset</span></span>

<span data-ttu-id="13fe4-115">Izmantojiet funkciju **Pārvietot līdzekli**, lai pārvietotu līdzekli uz citu līdzekļu struktūru vai uz citu atrašanās vietu tajā pašā līdzekļu struktūrā.</span><span class="sxs-lookup"><span data-stu-id="13fe4-115">Use the **Move asset** function to move an asset either to another asset structure or to another location in the same asset structure.</span></span> <span data-ttu-id="13fe4-116">Varat arī pārvietot līdzekli no līdzekļu struktūras, lai tas kļūtu par patstāvīgu līdzekli, kam nav struktūras attiecību.</span><span class="sxs-lookup"><span data-stu-id="13fe4-116">You can also move an asset out of an asset structure so that it becomes a standalone asset that has no structure relations.</span></span>

> [!NOTE]
> <span data-ttu-id="13fe4-117">Nelietojiet šo funkciju, ja līdzekļi tiek laboti vai īslaicīgi aizstāti.</span><span class="sxs-lookup"><span data-stu-id="13fe4-117">Don't use this function if assets are being repaired or temporarily replaced.</span></span> <span data-ttu-id="13fe4-118">Tā vietā izmantojiet funkciju **Aizstāt līdzekli**, kas aprakstīts tālāk šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="13fe4-118">Instead, use the **Replace asset** functionality that is described later in this topic.</span></span>

1. <span data-ttu-id="13fe4-119">Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Līdzekļi** \> **Visi līdzekļi** vai **Aktīvie līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="13fe4-119">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="13fe4-120">Sarakstā atlasiet līdzekli, kuru pārvietot.</span><span class="sxs-lookup"><span data-stu-id="13fe4-120">In the list, select the asset to move.</span></span> <span data-ttu-id="13fe4-121">Ja līdzeklim ir pakārtotie līdzekļi, jūs pārvietojat arī šos līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="13fe4-121">If the asset has child assets, you also move those assets.</span></span>
3. <span data-ttu-id="13fe4-122">Atlasiet **Pārvietot līdzekli**.</span><span class="sxs-lookup"><span data-stu-id="13fe4-122">Select **Move asset**.</span></span>
4. <span data-ttu-id="13fe4-123">Lai pārvietotu līdzekli tā, lai tas kļūtu par līdzekļa struktūras sastāvdaļu, atlasiet jauno līdzekli laukā **Primārais līdzeklis**.</span><span class="sxs-lookup"><span data-stu-id="13fe4-123">To move the asset so that it becomes part of an asset structure, select the new parent asset in the **Parent asset** field.</span></span> <span data-ttu-id="13fe4-124">Ja pārvietojat pakārtotu līdzekli un vēlaties to padarīt par patstāvīgu līdzekli, kam nav struktūras attiecību, atstājiet lauku **Primārais līdzeklis** tukšu.</span><span class="sxs-lookup"><span data-stu-id="13fe4-124">If you're moving a child asset, and you want to make it a standalone asset that has no structure relations, leave the **Parent asset** field blank.</span></span>
5. <span data-ttu-id="13fe4-125">Pēc noklusējuma lauks **Ir spēkā** automātiski tiek iestatīts uz pašreizējo datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="13fe4-125">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="13fe4-126">Tomēr jūs varat atlasīt citu datumu un laiku, no kura līdzekļa pārvietošana ir spēkā.</span><span class="sxs-lookup"><span data-stu-id="13fe4-126">However, you can select a different date and time that the asset move is valid from.</span></span>
6. <span data-ttu-id="13fe4-127">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13fe4-127">Select **OK**.</span></span>

## <a name="replace-asset"></a><span data-ttu-id="13fe4-128">Līdzekļu aizstāšana</span><span class="sxs-lookup"><span data-stu-id="13fe4-128">Replace asset</span></span>

<span data-ttu-id="13fe4-129">Izmantojiet funkciju **Aizstāt līdzekli** saistībā ar nolietota līdzekļa remontu, renovāciju vai pastāvīgu aizstāšanu ar jaunu līdzekli.</span><span class="sxs-lookup"><span data-stu-id="13fe4-129">Use the **Replace asset** function in connection with repairs, refurbishment, or permanent replacement of a worn-out asset by a new asset.</span></span> <span data-ttu-id="13fe4-130">Šī funkcija tiek izmantota, lai aizstātu pakārtotos līdzekļus līdzekļu struktūrā.</span><span class="sxs-lookup"><span data-stu-id="13fe4-130">This function is used to replace child assets in an asset structure.</span></span> <span data-ttu-id="13fe4-131">Primārajiem līdzekļiem (t.i., līdzekļiem, kuriem pašlaik nav primārā līdzekļa), šo aizstāšanu veic funkcionālajā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="13fe4-131">For parent assets (that is, assets that don't currently have a parent asset), this replacement is done on a functional location.</span></span> <span data-ttu-id="13fe4-132">Plašāku informāciju par to, kā aizstāt primāros līdzekļus funkcionālajā novietojumā, skatiet nodaļu [Līdzekļu uzstādīšana funkcionālajos novietojumos](../functional-locations/install-objects-on-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="13fe4-132">For more information about how to replace parent assets on a functional location, see [Install assets on functional locations](../functional-locations/install-objects-on-functional-locations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="13fe4-133">Ja labošanas cehs ir saistīts ar jūsu ražošanas nodaļu, varat izveidot funkcionālos novietojumus, piemēram, **Remonts**, **Brāķis** un **Glabāšana**, lai pārvaldītu līdzekļu remontu un aizstāšanu.</span><span class="sxs-lookup"><span data-stu-id="13fe4-133">If a repair shop is related to your production department, you can create functional locations such as **Repair**, **Scrap**, and **Storage** to handle the repair and replacement of assets.</span></span>

1. <span data-ttu-id="13fe4-134">Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Līdzekļi** \> **Visi līdzekļi** vai **Aktīvie līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="13fe4-134">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="13fe4-135">Sarakstā atlasiet aizstājamo pakārtoto līdzekli.</span><span class="sxs-lookup"><span data-stu-id="13fe4-135">In the list, select the child asset to replace.</span></span> <span data-ttu-id="13fe4-136">Ja līdzeklim ir pakārtotie līdzekļi, jūs aizstājat arī šos līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="13fe4-136">If the asset has child assets, you also replace those assets.</span></span>
3. <span data-ttu-id="13fe4-137">Atlasiet **Aizstāt līdzekli**.</span><span class="sxs-lookup"><span data-stu-id="13fe4-137">Select **Replace asset**.</span></span>

    <span data-ttu-id="13fe4-138">Lauks **Struktūras maiņa** rāda pēdējo datumu un laiku, kad atlasītais līdzeklis un saistītie pakārtotie līdzekļi tika pārvietoti līdzekļu struktūrā.</span><span class="sxs-lookup"><span data-stu-id="13fe4-138">The **Structure change** field shows the last date and time that the selected asset and related child assets were moved in the asset structure.</span></span>

4. <span data-ttu-id="13fe4-139">Sadaļā **Atlasītais līdzeklis** laukā **Mērķa funkcionālais novietojums** atlasiet funkcionālo novietojumu, uz kuru pārvietot līdzekli.</span><span class="sxs-lookup"><span data-stu-id="13fe4-139">In the **Selected asset** section, in the **Target functional location** field, select the functional location to move the asset to.</span></span> <span data-ttu-id="13fe4-140">Piemēram, atlasiet **Remonta** vai **Brāķa** atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="13fe4-140">For example, select the **Repair** or **Scrap** location.</span></span>

    <span data-ttu-id="13fe4-141">Sadaļā **Primārais līdzeklis** lauks **Ir spēkā** rāda pēdējo datumu un laiku, kad līdzeklis un saistītie pakārtotie līdzekļi tika uzstādīti vai pārvietoti pašreizējā funkcionālajā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="13fe4-141">In the **Parent asset** section, the **Effective** field shows the last date and time that the parent asset and related child assets were installed or moved on the current functional location.</span></span>

5. <span data-ttu-id="13fe4-142">Sadaļā **Jauns līdzeklis** laukā **Līdzeklis** atlasiet līdzekli, ko ievietot kā pagaidu vai pastāvīgu aizstājēju atlasītajam līdzeklim.</span><span class="sxs-lookup"><span data-stu-id="13fe4-142">In the **New asset** section, in the **Asset** field, select the asset to insert as a temporary or permanent replacement for the selected asset.</span></span> <span data-ttu-id="13fe4-143">Šis līdzeklis pašreiz var atrasties citā funkcionālajā novietojumā, piemēram, **Glabāšanā**.</span><span class="sxs-lookup"><span data-stu-id="13fe4-143">This asset might currently be located on another functional location, such as **Storage**.</span></span>
7. <span data-ttu-id="13fe4-144">Sadaļā **Ir spēkā no** lauks **Ir spēkā** pēc noklusējuma tiek iestatīts uz pašreizējo datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="13fe4-144">In the **Effective from** section, the **Effective** field is set to the current date and time by default.</span></span> <span data-ttu-id="13fe4-145">Tomēr jūs varat atlasīt citu datumu un laiku, no kura līdzekļa aizstāšana ir spēkā.</span><span class="sxs-lookup"><span data-stu-id="13fe4-145">However, you can select a different date and time that the asset replacement is valid from.</span></span>
8. <span data-ttu-id="13fe4-146">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13fe4-146">Select **OK**.</span></span>

## <a name="install-asset"></a><span data-ttu-id="13fe4-147">Līdzekļa uzstādīšana</span><span class="sxs-lookup"><span data-stu-id="13fe4-147">Install asset</span></span>

<span data-ttu-id="13fe4-148">Izmantojiet funkciju **Uzstādīt līdzekli**, lai uzstādītu līdzekļu struktūru funkcionālajā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="13fe4-148">Use the **Install asset** function to install an asset structure on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="13fe4-149">Vienmēr atlasiet primāro līdzekli.</span><span class="sxs-lookup"><span data-stu-id="13fe4-149">Always select a parent asset.</span></span> <span data-ttu-id="13fe4-150">Primārais līdzeklis un saistītie pakārtotie līdzekļi tiks pārvietoti uz atlasīto funkcionālo novietojumu.</span><span class="sxs-lookup"><span data-stu-id="13fe4-150">The parent asset and related child assets will be moved to the selected functional location.</span></span>

1. <span data-ttu-id="13fe4-151">Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Līdzekļi** \> **Visi līdzekļi** vai **Aktīvie līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="13fe4-151">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="13fe4-152">Sarakstā atlasiet primāro līdzekli, kuru uzstādīt citā funkcionālajā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="13fe4-152">In the list, select the parent asset to install on another functional location.</span></span>
3. <span data-ttu-id="13fe4-153">Atlasiet **Uzstādīt līdzekli**.</span><span class="sxs-lookup"><span data-stu-id="13fe4-153">Select **Install asset**.</span></span>

    <span data-ttu-id="13fe4-154">Sadaļa **Atribūti** rāda līdzekļa atribūtus, kas ir iestatīti primārajam līdzeklim.</span><span class="sxs-lookup"><span data-stu-id="13fe4-154">The **Attributes** section shows the asset attributes that are set up on the parent asset.</span></span>

4. <span data-ttu-id="13fe4-155">Laukā **Funkcionālais novietojums** atlasiet jauno atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="13fe4-155">In the **Functional location** field, select the new location.</span></span>
5. <span data-ttu-id="13fe4-156">Pēc noklusējuma lauks **Ir spēkā** automātiski tiek iestatīts uz pašreizējo datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="13fe4-156">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="13fe4-157">Tomēr jūs varat atlasīt citu datumu un laiku, no kura līdzekļu struktūras uzstādīšana ir spēkā.</span><span class="sxs-lookup"><span data-stu-id="13fe4-157">However, you can select a different date and time that the installation on the asset structure is valid from.</span></span>
6. <span data-ttu-id="13fe4-158">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13fe4-158">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]