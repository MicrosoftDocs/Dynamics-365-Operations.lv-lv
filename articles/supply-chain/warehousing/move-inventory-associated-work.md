---
title: Krājumu kustība noliktavas pārvaldībā, ja ar tiem ir saistīts darbs
description: Šajā tēmā ir aprakstīts, kā jūs varat iestatīt un lietot vienību izdošanas apstiprināšanas funkciju mobilajā ierīcē.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b58678ada7d6c3a2fb2af131418d2bb97ee5512
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226031"
---
# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a><span data-ttu-id="d301e-103">Krājumu kustība noliktavas pārvaldībā, ja ar tiem ir saistīts darbs</span><span class="sxs-lookup"><span data-stu-id="d301e-103">Movement of inventory with associated work in Warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d301e-104">Izmantojot krājumu kustību, varat izlemt, kuriem noliktavas darbiniekiem ir atļauts pārvietot rezervētos krājumus.</span><span class="sxs-lookup"><span data-stu-id="d301e-104">Using movement of inventory, you can decide which warehouse workers are allowed to move reserved inventory.</span></span> <span data-ttu-id="d301e-105">Tas nodrošina elastību regulētās noliktavās, kur varat izlemt, ka kādam darbiniekam netiek ļauts izvēlēties jaunu izdošanas novietojumu jau izveidotam izdošanas darbam.</span><span class="sxs-lookup"><span data-stu-id="d301e-105">This provides a flexibility in regulated warehouses where you can decide to not allow a worker to choose a new pick location for pick work that is already created.</span></span> <span data-ttu-id="d301e-106">Turklāt noliktavas pārvaldniekam tā ļauj kontrolēt to, kuras iespējas ir jāpiešķir dažiem mazāk pieredzējušiem darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="d301e-106">It also allows a warehouse manager to control which capabilities some less experienced workers should have.</span></span>

<span data-ttu-id="d301e-107">Noliktavas darbinieku ikdienas operāciju pārvaldīšanas elastība var noderēt tālāk norādītajos scenārijos.</span><span class="sxs-lookup"><span data-stu-id="d301e-107">The flexibility to manage the daily operations of warehouse workers can be useful in scenarios such as these:</span></span>

## <a name="scenario-1"></a><span data-ttu-id="d301e-108">1. scenārijs</span><span class="sxs-lookup"><span data-stu-id="d301e-108">Scenario 1</span></span>
<span data-ttu-id="d301e-109">Uzņēmumam ir relatīvi maza saņemšanas zona, un tā ir pārslogota ar paletēm un kastēm, kas gaida izvietošanu.</span><span class="sxs-lookup"><span data-stu-id="d301e-109">A company has a relatively small receiving area, and it’s congested with pallets and boxes awaiting put away.</span></span> <span data-ttu-id="d301e-110">Pašreizējā dienā ir paredzēts piegādāt lielu sūtījumu, tādēļ saņemšanas darbinieks izlemj atbrīvot saņemšanas zonu, dažas paletes pārvietojot uz sekundāru ienākošo sagatavošanas zonu.</span><span class="sxs-lookup"><span data-stu-id="d301e-110">A large shipment is expected on the current day, so the receiving clerk decides to clear up the receiving area by moving some of the pallets to a secondary inbound staging area.</span></span>

## <a name="scenario-2"></a><span data-ttu-id="d301e-111">2. scenārijs</span><span class="sxs-lookup"><span data-stu-id="d301e-111">Scenario 2</span></span>
<span data-ttu-id="d301e-112">Pieredzējis noliktavas darbinieks pamana iespēju noliktavā krājumus konsolidēt vienā novietojumā, nevis tos sadalīt 3 netālu esošos novietojumos ar nelielu daudzumu katrā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="d301e-112">An experienced warehouse worker notices an opportunity in a warehouse to consolidate items in one location instead of having them divided across 3 nearby locations with little quantity on each.</span></span> <span data-ttu-id="d301e-113">Šis darbinieks vēlas konsolidēt daudzumu, katra šī novietojuma krājumus pārvietojot uz to pašu novietojumu un tajā pašā noliktavas vienībā.</span><span class="sxs-lookup"><span data-stu-id="d301e-113">The worker wants to consolidate the quantity by moving items from each of these locations into the same location and onto the same license plate.</span></span>

## <a name="scenario-3"></a><span data-ttu-id="d301e-114">3. scenārijs</span><span class="sxs-lookup"><span data-stu-id="d301e-114">Scenario 3</span></span>
<span data-ttu-id="d301e-115">Palete gaida sūtījumu sagatavošanas novietojumā, piemēram, STAGE01, kas atrodas netālu no BAYDOOR01.</span><span class="sxs-lookup"><span data-stu-id="d301e-115">A pallet is awaiting shipment in a staging location, such as STAGE01, which is near BAYDOOR01.</span></span> <span data-ttu-id="d301e-116">Taču sakarā ar plānu izmaiņām kravas auto pienākšana tiek plānota novietojumā BAYDOOR04.</span><span class="sxs-lookup"><span data-stu-id="d301e-116">However, due to a change of plans the truck is scheduled to arrive at BAYDOOR04.</span></span> <span data-ttu-id="d301e-117">Nosūtīšanas darbinieks ir informēts par to, un viņam ir jānodrošina, ka kravas automašīnai nav jāgaida iekraušana no STAGE01.</span><span class="sxs-lookup"><span data-stu-id="d301e-117">The shipping clerk is aware of this and needs to ensure that the truck does not have to wait to be loaded from STAGE01.</span></span> <span data-ttu-id="d301e-118">Nosūtīšanas darbinieks izlemj krājumus šajā sūtījumā no STAGE01 pārvietot uz STAGE04, kas ir tuvāk jaunajam mērķim.</span><span class="sxs-lookup"><span data-stu-id="d301e-118">The shipping clerk decides to move the items in that shipment from STAGE01 to STAGE04, which is closer to the new destination.</span></span>

### <a name="current-limitations"></a><span data-ttu-id="d301e-119">Pašreizējie ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="d301e-119">Current limitations</span></span>

<span data-ttu-id="d301e-120">Pārvietot varat tikai tādas darba rezervācijas, kas ir Pārdošanas pasūtījums, Pārsūtīšanas pasūtījuma izejas plūsma, Pārsūtīšanas pasūtījuma ieejas plūsma, Pirkšanas pasūtījums un Papildināšanas darbs.</span><span class="sxs-lookup"><span data-stu-id="d301e-120">The work reservations that you can move are limited to Sales order, Transfer order issue, Transfer order receipt, Purchase order, and Replenishment work.</span></span>

<span data-ttu-id="d301e-121">Krājumu pārvietošana ir ierobežota, lai novērstu darba rindu dalīšanu.</span><span class="sxs-lookup"><span data-stu-id="d301e-121">Moving items is restricted to prevent splitting of work lines.</span></span> <span data-ttu-id="d301e-122">Tas nozīmē, ka gadījumā, ja jums ir darba rinda 100 gab. krājumiem A no novietojuma Loc1, tad nevarat no turienes uz citu novietojumu pārvietot tikai 30 gab. šī krājuma A.</span><span class="sxs-lookup"><span data-stu-id="d301e-122">This means that if you have a work line for 100 pcs of item A from location Loc1, you won’t be able to move only 30 pcs of item A from there to another location.</span></span> <span data-ttu-id="d301e-123">Tas izraisītu esošās darba rindas dalīšanu uz 30 un 70, jo novietojumi tagad ir dažādi.</span><span class="sxs-lookup"><span data-stu-id="d301e-123">This would lead to a split of the existing work line to 30 and 70, because the locations are now different.</span></span>

<span data-ttu-id="d301e-124">Sagatavošanas posmu scenārijiem, kur noliktavas vienība, no kuras jūs pārvietojat preces vai uz kuru jūs pārvietojat preces, darba pasūtījumam tiek iestatīta kā Mērķa LP, un ir atļauta tikai visas LP kustība, lai nesadalītu mērķa LP.</span><span class="sxs-lookup"><span data-stu-id="d301e-124">For staging scenarios, where the license plate you move the goods from or the license plate you move the goods to, are set as a Target LP for a work order, only movement of the entire LP is allowed, so as not to break up the Target LP.</span></span>
<span data-ttu-id="d301e-125">Pašlaik tiek atbalstītas tikai ekspromta kustības.</span><span class="sxs-lookup"><span data-stu-id="d301e-125">Only the ad hoc movement is currently supported.</span></span> <span data-ttu-id="d301e-126">Tas nozīmē, ka nevar pārvietot rezervētus krājumus, izmantojot kustību ar veidnes mobilās ierīces izvēlnes vienumiem.</span><span class="sxs-lookup"><span data-stu-id="d301e-126">That means that you will not be able to move reserved inventory through the movement by template mobile device menu items.</span></span>

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a><span data-ttu-id="d301e-127">Rezervēto krājumu pārvietošanas atļaujas iestatīšana atsevišķiem darbiniekiem</span><span class="sxs-lookup"><span data-stu-id="d301e-127">Set up permission to move reserved inventory for individual workers</span></span>

<span data-ttu-id="d301e-128">Darbiniekam, kuram vēlaties atļaut pārvietot rezervētus krājumus, sadaļā **Noliktavas vadība** > **Iestatīšana** > **Nodarbinātais** atzīmējiet izvēles rūtiņu **Atļaut krājumu kustību, ja ar tiem ir saistīts darbs**.</span><span class="sxs-lookup"><span data-stu-id="d301e-128">For the worker who should be allowed to move reserved inventory, select the **Allow movement of inventory with work associated** check box under **Warehouse management** > **Setup** > **Worker**.</span></span>  

### <a name="backported"></a><span data-ttu-id="d301e-129">Pārnests uz vecāku versiju</span><span class="sxs-lookup"><span data-stu-id="d301e-129">Backported</span></span>

<span data-ttu-id="d301e-130">Šis līdzeklis ir arī pārnests uz versiju Microsoft Dynamics AX 2012 R3, kā arī būs pieejams CU12 ietvaros.</span><span class="sxs-lookup"><span data-stu-id="d301e-130">This feature has also been back-ported to Microsoft Dynamics AX 2012 R3 and will be available as part of CU12.</span></span>
<span data-ttu-id="d301e-131">To var arī lejupielādēt atsevišķi, izmantojot KB numur 3192548.</span><span class="sxs-lookup"><span data-stu-id="d301e-131">It can also be downloaded individually through KB number 3192548.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]