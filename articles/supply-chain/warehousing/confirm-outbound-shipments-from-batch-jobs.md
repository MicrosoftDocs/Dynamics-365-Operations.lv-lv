---
title: Apstiprināt izejošos sūtījumus no pakešuzdevumiem
description: Šajā tēmā aprakstīts, kā iestatīt pakešuzdevumu, kas automātiski apstiprina izejošos pārvedumu sūtījumus kravām, kas ir gatavas sūtīšanai.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 48257967ce360b1d4969124411d5976b807bf9e4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996305"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a><span data-ttu-id="72b23-103">Apstiprināt izejošos sūtījumus no pakešuzdevumiem</span><span class="sxs-lookup"><span data-stu-id="72b23-103">Confirm outbound shipments from batch jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72b23-104">Šajā tēmā aprakstīts, kā iestatīt pakešuzdevumu, kas automātiski apstiprina izejošos pārvedumu sūtījumus kravām, kas ir gatavas sūtīšanai.</span><span class="sxs-lookup"><span data-stu-id="72b23-104">This topic describes how to set up a batch job that automatically confirms outbound transfer-order shipments for ready-to-ship loads.</span></span> <span data-ttu-id="72b23-105">Šeit aprakstītais pakešuzdevums attiecas tikai uz pārvedumu sūtījumiem, nevis uz pārdošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="72b23-105">The batch job described here only applies to transfer order shipments, not to sales orders.</span></span>

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a><span data-ttu-id="72b23-106">Iespējojiet funkciju Apstiprināt izejošos sūtījumus no pakešuzdevumiem</span><span class="sxs-lookup"><span data-stu-id="72b23-106">Enable the Confirm outbound shipments from batch jobs feature</span></span>

<span data-ttu-id="72b23-107">Lai varētu izmantot šo līdzekli, tam vispirms jābūt iespējotam sistēmā.</span><span class="sxs-lookup"><span data-stu-id="72b23-107">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="72b23-108">Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lapu, lai pārbaudītu līdzekļa statusu un iespējotu to pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="72b23-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="72b23-109">Funkcija tiek norādīta kā:</span><span class="sxs-lookup"><span data-stu-id="72b23-109">The feature is listed as:</span></span>

- <span data-ttu-id="72b23-110">**Modulis** - *Noliktavas pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="72b23-110">**Module** - *Warehouse management*</span></span>
- <span data-ttu-id="72b23-111">**Funkcijas nosaukums** - *Apstiprināt izejošos sūtījumus no pakešuzdevumiem*</span><span class="sxs-lookup"><span data-stu-id="72b23-111">**Feature name** - *Confirm outbound shipments from batch jobs*</span></span>

## <a name="process-outbound-shipments"></a><span data-ttu-id="72b23-112">Apstrādāt izejošos sūtījumus</span><span class="sxs-lookup"><span data-stu-id="72b23-112">Process outbound shipments</span></span>

<span data-ttu-id="72b23-113">Lai iestatītu ieplānotu pakešuzdevumu, lai palaistu izejošo sūtījuma apstiprinājumu kravām, kas ir gatavas nosūtīšanai:</span><span class="sxs-lookup"><span data-stu-id="72b23-113">To set up a scheduled batch job to run the outbound shipment confirmation for loads that are ready to ship:</span></span>

1. <span data-ttu-id="72b23-114">Dodieties uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Apstrādāt izejošos sūtījumus**.</span><span class="sxs-lookup"><span data-stu-id="72b23-114">Go to **Warehouse management \> Periodic tasks \> Process outbound shipments**.</span></span>
1. <span data-ttu-id="72b23-115">Atveras dialoglodziņš **Apstiprināt sūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="72b23-115">The **Confirm shipment** dialog box opens.</span></span> <span data-ttu-id="72b23-116">Kopsavilkuma cilnē **Ieraksti, kas jāiekļauj** atlasiet **Filtrs**.</span><span class="sxs-lookup"><span data-stu-id="72b23-116">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="72b23-117">Atveras vaicājumu redaktora dialoglodziņš.</span><span class="sxs-lookup"><span data-stu-id="72b23-117">The query editor dialog box opens.</span></span> <span data-ttu-id="72b23-118">Cilnē **Diapazons** pievienojiet rindu ar sekojošajām vērtībām:</span><span class="sxs-lookup"><span data-stu-id="72b23-118">On the **Range** tab, add a row with the following values:</span></span>
    - <span data-ttu-id="72b23-119">**Tabula** - *Kravas*</span><span class="sxs-lookup"><span data-stu-id="72b23-119">**Table** - *Loads*</span></span>
    - <span data-ttu-id="72b23-120">**Atvasinātā tabula** - *Kravas*</span><span class="sxs-lookup"><span data-stu-id="72b23-120">**Derived table** - *Loads*</span></span>
    - <span data-ttu-id="72b23-121">**Lauks** - *Kravas statuss*</span><span class="sxs-lookup"><span data-stu-id="72b23-121">**Field** - *Load status*</span></span>
    - <span data-ttu-id="72b23-122">**Kritēriji** - *Ielādētie*</span><span class="sxs-lookup"><span data-stu-id="72b23-122">**Criteria** - *Loaded*</span></span>
1. <span data-ttu-id="72b23-123">Atlasiet **Labi**, lai atgrieztos dialoglodziņā **Apstiprināt sūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="72b23-123">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="72b23-124">Kopsavilkuma cilnē **Palaist fonā** iestatiet **Partijas apstrādi** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="72b23-124">On the **Run in the background** FastTab, set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="72b23-125">Kopsavilkuma cilnē **Palaist fonā** atlasiet **Periodiskums**.</span><span class="sxs-lookup"><span data-stu-id="72b23-125">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="72b23-126">Atveras dialoglodziņš **Definēt periodiskumu**.</span><span class="sxs-lookup"><span data-stu-id="72b23-126">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="72b23-127">Iestatiet izpildes grafiku, kas nepieciešams jūsu biznesam.</span><span class="sxs-lookup"><span data-stu-id="72b23-127">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="72b23-128">Atlasiet **Labi**, lai atgrieztos dialoglodziņā **Apstiprināt sūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="72b23-128">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="72b23-129">Dialoglodziņā **Apstiprināt nosūtīšanu** atlasiet **Labi**, lai pievienotu pakešuzdevumu partijas rindai.</span><span class="sxs-lookup"><span data-stu-id="72b23-129">Select **OK** on the **Confirm shipment** dialog box to add the batch job to the batch queue.</span></span>

<span data-ttu-id="72b23-130">Plašāku informāciju par pakešdatu apstrādi skatiet [Partijas apstrādes pārskats](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span><span class="sxs-lookup"><span data-stu-id="72b23-130">For more information, see [Batch processing overview](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span></span>
