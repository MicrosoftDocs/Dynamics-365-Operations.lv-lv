---
title: Sūtījumu nevar apstiprināt nepabeigta vai trūkstoša darba dēļ
description: Sūtījumu nevar apstiprināt nepabeigta vai trūkstoša darba dēļ
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: da6388d433d6021a99840ae9781c717db1b540a9
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938512"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a><span data-ttu-id="e6a91-103">Sūtījumu nevar apstiprināt nepabeigta vai trūkstoša darba dēļ</span><span class="sxs-lookup"><span data-stu-id="e6a91-103">You can't confirm a shipment because of incomplete or missing work</span></span>

<span data-ttu-id="e6a91-104">Kļūdas kods: WAX515</span><span class="sxs-lookup"><span data-stu-id="e6a91-104">Error code: WAX515</span></span>

## <a name="symptoms"></a><span data-ttu-id="e6a91-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="e6a91-105">Symptoms</span></span>

<span data-ttu-id="e6a91-106">Mēģinot apstiprināt kravu, sistēma rāda šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="e6a91-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="e6a91-107">Kravas %1 nosūtīšanu nevarēja apstiprināt, jo bija jāpabeidz visi ar kravu saistītie darbi.</span><span class="sxs-lookup"><span data-stu-id="e6a91-107">The shipment for load %1 could not be confirmed because all work for the load must be complete.</span></span>

<span data-ttu-id="e6a91-108">Tādēļ kravas nosūtīšanu nevar apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="e6a91-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="e6a91-109">Iemesls</span><span class="sxs-lookup"><span data-stu-id="e6a91-109">Cause</span></span>

<span data-ttu-id="e6a91-110">Krava vai sūtījums pašlaik ir stāvoklī, kad sūtījuma apstiprināšana neizdodas.</span><span class="sxs-lookup"><span data-stu-id="e6a91-110">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="e6a91-111">Pirms varat apstiprināt sūtījumu, kravai ir jāpastāv vismaz dažiem darbiem, un visiem darbiem ir jābūt statusam *Slēgts* vai *Atcelts*.</span><span class="sxs-lookup"><span data-stu-id="e6a91-111">Before you can confirm the shipment, at least some work must exist for the load, and all that work must have a status of *Closed* or *Canceled*.</span></span>

## <a name="resolution"></a><span data-ttu-id="e6a91-112">Novēršana</span><span class="sxs-lookup"><span data-stu-id="e6a91-112">Resolution</span></span>

<span data-ttu-id="e6a91-113">Pārbaudiet ar kravu vai sūtījumu saistītos pārdošanas pasūtījumus vai pārsūtīšanas pasūtījumus un pārliecinieties, ka viss saistītais darbs ir pabeigts vai atcelts.</span><span class="sxs-lookup"><span data-stu-id="e6a91-113">Check the related sales orders or transfer orders for the load or shipment, and make sure that all the related work has been completed or canceled.</span></span>

<span data-ttu-id="e6a91-114">Varat strādāt ar sūtījumiem un kravām vairākās lapās.</span><span class="sxs-lookup"><span data-stu-id="e6a91-114">You can work with shipments and loads on several pages.</span></span> <span data-ttu-id="e6a91-115">Tālāk ir sniegti daži piemēri.</span><span class="sxs-lookup"><span data-stu-id="e6a91-115">The following subsections provide a few examples.</span></span>

### <a name="all-loads-page"></a><span data-ttu-id="e6a91-116">Visu kravu lapa</span><span class="sxs-lookup"><span data-stu-id="e6a91-116">All loads page</span></span>

1. <span data-ttu-id="e6a91-117">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.</span><span class="sxs-lookup"><span data-stu-id="e6a91-117">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="e6a91-118">Izvēlieties kravu, kam nevar apstiprināt nosūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e6a91-118">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="e6a91-119">Darbību rūtī cilnē **Kravas** grupā **Saistīta informācija** atlasiet **Darbs**.</span><span class="sxs-lookup"><span data-stu-id="e6a91-119">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="e6a91-120">Pārbaudiet katra darba ID statusu.</span><span class="sxs-lookup"><span data-stu-id="e6a91-120">Inspect the status of each work ID.</span></span> <span data-ttu-id="e6a91-121">Sekojiet katram darba ID, kura statuss nav *Slēgts* vai *Atcelts*.</span><span class="sxs-lookup"><span data-stu-id="e6a91-121">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="e6a91-122">Kad katram darba ID statuss *Slēgts* vai *Atcelts*, mēģiniet vēlreiz apstiprināt sūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e6a91-122">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-shipments-page"></a><span data-ttu-id="e6a91-123">Visu sūtījumu lapa</span><span class="sxs-lookup"><span data-stu-id="e6a91-123">All shipments page</span></span>

1. <span data-ttu-id="e6a91-124">Dodieties uz **Noliktavas pārvaldība \> Sūtījumi\> Visi sūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="e6a91-124">Go to **Warehouse management \> Shipments\> All shipments**.</span></span>
1. <span data-ttu-id="e6a91-125">Izvēlieties sūtījumu, ko nevar apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="e6a91-125">Select the shipment that can't be confirmed.</span></span>
1. <span data-ttu-id="e6a91-126">Darbību rūtī cilnē **Sūtījumi** grupā **Darbs** atlasiet **Detalizēta informācija par darbu**.</span><span class="sxs-lookup"><span data-stu-id="e6a91-126">On the Action Pane, on the **Shipments** tab, in the **Work** group, select **Work details**.</span></span>
1. <span data-ttu-id="e6a91-127">Pārbaudiet katra darba ID statusu.</span><span class="sxs-lookup"><span data-stu-id="e6a91-127">Inspect the status of each work ID.</span></span> <span data-ttu-id="e6a91-128">Sekojiet katram darba ID, kura statuss nav *Slēgts* vai *Atcelts*.</span><span class="sxs-lookup"><span data-stu-id="e6a91-128">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="e6a91-129">Kad katram darba ID statuss *Slēgts* vai *Atcelts*, mēģiniet vēlreiz apstiprināt sūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e6a91-129">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-work-page"></a><span data-ttu-id="e6a91-130">Visa darba lapa</span><span class="sxs-lookup"><span data-stu-id="e6a91-130">All work page</span></span>

1. <span data-ttu-id="e6a91-131">Dodieties uz **Noliktavas pārvaldība \> Darbs\> Viss darbs**.</span><span class="sxs-lookup"><span data-stu-id="e6a91-131">Go to **Warehouse management \> Work\> All work**.</span></span>
1. <span data-ttu-id="e6a91-132">Atlasiet darbu pasūtījuma numuram, kam nevar apstiprināt sūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e6a91-132">Select the work for the order number that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="e6a91-133">Darbību rūtī, cilnē **Sūtījums**, grupā **Sūtījums** atlasiet **Apstiprināt sūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="e6a91-133">On the Action Pane, on the **Shipment** tab, in the **Shipment** group, select **Confirm shipment**.</span></span>
1. <span data-ttu-id="e6a91-134">Pārbaudiet katra darba ID statusu.</span><span class="sxs-lookup"><span data-stu-id="e6a91-134">Inspect the status of each work ID.</span></span> <span data-ttu-id="e6a91-135">Sekojiet katram darba ID, kura statuss nav *Slēgts* vai *Atcelts*.</span><span class="sxs-lookup"><span data-stu-id="e6a91-135">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="e6a91-136">Kad katram darba ID statuss *Slēgts* vai *Atcelts*, mēģiniet vēlreiz apstiprināt sūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e6a91-136">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>
