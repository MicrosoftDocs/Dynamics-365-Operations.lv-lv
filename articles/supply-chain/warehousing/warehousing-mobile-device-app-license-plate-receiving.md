---
title: Numura zīmes saņemšana, izmantojot noliktavas programmu
description: Šajā tēmā skaidrots, kā iestatīt noliktavas programmu, lai atbalstītu numura zīmes saņemšanas procesa izmantošanu, lai saņemtu fizisko krājumu.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 7d5ac6598ab80ece0164d7c92f5d84e91d21b385
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346380"
---
# <a name="license-plate-receiving-via-the-warehousing-app"></a><span data-ttu-id="09fdd-103">Numura zīmes saņemšana, izmantojot noliktavas programmu</span><span class="sxs-lookup"><span data-stu-id="09fdd-103">License plate receiving via the warehousing app</span></span>

<span data-ttu-id="09fdd-104">Šajā tēmā skaidrots, kā iestatīt noliktavas programmu, lai tā atbalstītu numura zīmes saņemšanas procesa izmantošanu, lai saņemtu fizisko krājumu.</span><span class="sxs-lookup"><span data-stu-id="09fdd-104">This topic explains how to set up the warehousing app so that it supports using a license plate receiving process to receive physical inventory.</span></span>

<span data-ttu-id="09fdd-105">Jūs varat izmantot šo funkcionalitāti, lai ātri ierakstītu ienākošo krājumu saņemšanu, kas ir saistīts ar iepriekšējo paziņojums par nosūtīšanu (ASN).</span><span class="sxs-lookup"><span data-stu-id="09fdd-105">You can use this functionality to quickly record the receipt of inbound inventory that is related to an advance ship notice (ASN).</span></span> <span data-ttu-id="09fdd-106">Sistēma automātiski izveido ASN, kad noliktavas pārvaldības procesi tiek izmantoti, lai nosūtītu pārsūtīšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="09fdd-106">The system automatically creates an ASN when warehouse management processes are used to ship a transfer order.</span></span> <span data-ttu-id="09fdd-107">Pirkšanas pasūtījuma procesam ASN var tikt manuāli reģistrēts, vai to var automātiski importēt, izmantojot ienākošo ASN datu elementa procesu.</span><span class="sxs-lookup"><span data-stu-id="09fdd-107">For the purchase order process, an ASN can be manually recorded, or it can be automatically imported by using an inbound ASN data entity process.</span></span>

<span data-ttu-id="09fdd-108">ASN dati ir saistīti ar noslodzēm un kravām, izmantojot *iepakošanas struktūras*, kur paletes (standarta numura zīmes) var ietvert gadījumus (ligzdotas numura zīmes).</span><span class="sxs-lookup"><span data-stu-id="09fdd-108">The ASN data is linked to loads and shipments via the *packing structures*, where pallets (parent license plates) can contain cases (nested license plates).</span></span>

> [!NOTE]
> <span data-ttu-id="09fdd-109">Lai samazinātu krājumu transakciju skaitu, kad tiek izmantotas iepakojuma struktūras, kurām ir ligzdotas numura zīmes, sistēma reģistrē fiziskos rīcībā esošos krājumus uz pamatnumura zīmes.</span><span class="sxs-lookup"><span data-stu-id="09fdd-109">To reduce the number of inventory transactions when packing structures that have nested license plates are used, the system records the physical on-hand inventory on the parent license plate.</span></span> <span data-ttu-id="09fdd-110">Lai izraisītu fizisko rīcībā esošo krājumu pārvietošanu no pamatnumura zīmes uz ligzdotajām numura zīmēm, kas balstītas uz iepakojuma struktūras datiem, mobilajai ierīcei ir jānorāda izvēlnes elements, kas ir atkarīgs no *Ligzdotu licenču plāksnīšu iepakošanas* darba izveides procesiem.</span><span class="sxs-lookup"><span data-stu-id="09fdd-110">To trigger the movement of the physical on-hand inventory from the parent license plate to the nested license plates, based on the packing structure data, the mobile device must provide a menu item that is based on the *Pack to nested license plates* work creation process.</span></span>

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a><span data-ttu-id="09fdd-111">Rādīt vai izlaist saņemšanas kopsavilkuma lapu</span><span class="sxs-lookup"><span data-stu-id="09fdd-111">Show or skip the receiving summary page</span></span>

<span data-ttu-id="09fdd-112">Jūs varat izmantot līdzekli *Kontrolēt, vai mobilajās ierīcēs tiktu parādīta saņemšanas kopsavilkuma lapa*, lai izmantotu papildu detalizēto noliktavu programmu plūsmu kā daļu no numura zīmes saņemšanas procesa.</span><span class="sxs-lookup"><span data-stu-id="09fdd-112">You can use the *Control whether to display a receiving summary page on mobile devices* feature to take advantage of an additional detailed warehousing app flow as part of the license plate receiving process.</span></span>

<span data-ttu-id="09fdd-113">Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="09fdd-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="09fdd-114">Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="09fdd-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="09fdd-115">Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:</span><span class="sxs-lookup"><span data-stu-id="09fdd-115">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="09fdd-116">**Modulis:** *Noliktavas vadība*</span><span class="sxs-lookup"><span data-stu-id="09fdd-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="09fdd-117">**Līdzekļa nosaukums:** *kontrolē, vai mobilajās ierīcēs tiek parādīta saņemšanas kopsavilkuma lapa*</span><span class="sxs-lookup"><span data-stu-id="09fdd-117">**Feature name:** *Control whether to display a receiving summary page on mobile devices*</span></span>

<span data-ttu-id="09fdd-118">Kad šis līdzeklis ir ieslēgts, mobilās ierīces izvēlnes vienumi numura zīmes saņemšanas vai numura zīmes saņemšanas un izvietošanas laikā nodrošinās iestatījumu **Parādīt saņemšanas kopsavilkuma lapu**.</span><span class="sxs-lookup"><span data-stu-id="09fdd-118">When this feature is turned on, mobile device menu items for license plate receiving or license plate receiving and put-away will provide a **Display receiving summary page** setting.</span></span> <span data-ttu-id="09fdd-119">Šim iestatījumam ir šādas opcijas:</span><span class="sxs-lookup"><span data-stu-id="09fdd-119">This setting has the following options:</span></span>

- <span data-ttu-id="09fdd-120">**Rādīt detalizētu kopsavilkumu** — veicot numura zīmes saņemšanu, darbinieki redzēs papildu lapu, kas parāda pilnu ASN informāciju.</span><span class="sxs-lookup"><span data-stu-id="09fdd-120">**Display a detailed summary** – During license plate receiving, workers will see an extra page that shows the full ASN information.</span></span>
- <span data-ttu-id="09fdd-121">**Izlaist kopsavilkumu** — darbinieki neredzēs pilnu ASN informāciju.</span><span class="sxs-lookup"><span data-stu-id="09fdd-121">**Skip the summary** – Workers won't see the full ASN information.</span></span> <span data-ttu-id="09fdd-122">Noliktavas darbinieki arī saņemšanas procesa laikā nevarēs iestatīt izvietojuma kodu vai pievienot izņēmumus.</span><span class="sxs-lookup"><span data-stu-id="09fdd-122">Warehouse workers also won't be able to set a disposition code or add exceptions during the receiving process.</span></span>

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a><span data-ttu-id="09fdd-123">Nepieļaut nodošanas pasūtījuma nosūtīto numura zīmju izmantošanu noliktavās, kas nav galamērķa noliktava</span><span class="sxs-lookup"><span data-stu-id="09fdd-123">Prevent transfer order–shipped license plates from being used at warehouses other than the destination warehouse</span></span>

<span data-ttu-id="09fdd-124">Nevar izmantot numura zīmes saņemšanas procesu, ja ASN ietver numura zīmes ID, kas jau eksistē un kam ir fiziski rīcībā esošie dati noliktavas atrašanās vietā, kas atšķiras no noliktavas atrašanās vietas, kur notiek numura zīmes reģistrācija.</span><span class="sxs-lookup"><span data-stu-id="09fdd-124">A license plate receiving process can't be used if an ASN contains a license plate ID that already exists and has physical on-hand data at a warehouse location other than the warehouse location where the license plate registration is occurring.</span></span>

<span data-ttu-id="09fdd-125">Pārsūtīšanas pasūtījumu scenārijiem, kuros tranzīta noliktava neseko numura zīmēm (un tāpēc arī neseko līdzi katras numura zīmes fiziskajam inventāram uz vietas), varat izmantot līdzekli *Nepieļaut nodošanas pasūtījuma nosūtīto numura zīmju izmantošanu noliktavās, kas nav galamērķa noliktava*, lai novērstu to, ka fiziskas rīcībā esošas numura zīmes ir pieejamas tranzītā.</span><span class="sxs-lookup"><span data-stu-id="09fdd-125">For transfer order scenarios where the transit warehouse doesn't track license plates (and therefore also doesn't track physical on-hand inventory per license plate), you can use the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature to prevent physical on-hand updates of license plates that are in transit.</span></span>

<span data-ttu-id="09fdd-126">Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="09fdd-126">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="09fdd-127">Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="09fdd-127">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="09fdd-128">Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:</span><span class="sxs-lookup"><span data-stu-id="09fdd-128">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="09fdd-129">**Modulis:** *Noliktavas vadība*</span><span class="sxs-lookup"><span data-stu-id="09fdd-129">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="09fdd-130">**Līdzekļa nosaukums:** *Nepieļaut nodošanas pasūtījuma nosūtīto numura zīmju izmantošanu citās noliktavās, kas nav galamērķa noliktava*</span><span class="sxs-lookup"><span data-stu-id="09fdd-130">**Feature name:** *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse*</span></span>

<span data-ttu-id="09fdd-131">Lai pārvaldītu funkcionalitāti, kad šī funkcija ir pieejama, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="09fdd-131">To manage the functionality when this feature is available, follow these steps.</span></span>

1. <span data-ttu-id="09fdd-132">Doties uz **Noliktavas vadība\> Iestatīšana \> Noliktavas vadības parametri**.</span><span class="sxs-lookup"><span data-stu-id="09fdd-132">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="09fdd-133">Cilnē **Vispārīgi** kopsavilkuma cilnē **Numura zīmes**  iestatiet **Tranzīta noliktavas numura zīmes politikas** lauku uz vienu no šīm vērtībām:</span><span class="sxs-lookup"><span data-stu-id="09fdd-133">On the **General** tab, on the **License plates** FastTab, set the **Transit warehouse license plate policy** field to one of the following values:</span></span>

    - <span data-ttu-id="09fdd-134">**Atļaut nereģistrētas numura zīmes atkārtotu izmantošanu** — sistēma darbojas tādā pašā veidā, kā tas darbojas, kad līdzeklis *Nepieļaut nodošanas pasūtījuma nosūtīto numura zīmju izmantošanu citās noliktavās, kas nav galamērķa noliktava* nav pieejams.</span><span class="sxs-lookup"><span data-stu-id="09fdd-134">**Allow reuse of non-tracked license plate** – The system works the same way that it works when the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature isn't available.</span></span> <span data-ttu-id="09fdd-135">Šī vērtība ir noklusētais iestatījums, pirmoreiz aktivizējot līdzekli.</span><span class="sxs-lookup"><span data-stu-id="09fdd-135">This value is the default setting when you first activate the feature.</span></span>
    - <span data-ttu-id="09fdd-136">**Novērst nereģistrētas numura zīmju atkārtotu izmantošanu** - līdz pārsūtīšanas pasūtījuma saņemšanai mērķa noliktavā tiks atļauti tikai rīcībā esošie atjauninājumi, kas saistīti ar nosūtītajām numura zīmēm.</span><span class="sxs-lookup"><span data-stu-id="09fdd-136">**Prevent reuse of non-tracked license plate** – Only on-hand updates that are related to a shipped license plate will be allowed at the destination warehouse until the transfer order has been received.</span></span>

## <a name="more-information"></a><span data-ttu-id="09fdd-137">Papildinformācija</span><span class="sxs-lookup"><span data-stu-id="09fdd-137">More information</span></span>

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

<span data-ttu-id="09fdd-138">Papildinformāciju par mobilās ierīces izvēlnes elementiem skatiet [Mobilo ierīču iestatīšana noliktavas darbam](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="09fdd-138">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>
