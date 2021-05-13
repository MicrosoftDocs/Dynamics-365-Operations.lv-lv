---
title: Nevar apstiprināt sūtījumu, jo nav izdoti krājumi
description: Nevar apstiprināt sūtījumu, jo nav izdoti krājumi
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
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938511"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="ba365-103">Nevar apstiprināt sūtījumu, jo nav izdoti krājumi</span><span class="sxs-lookup"><span data-stu-id="ba365-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="ba365-104">Kļūdas kods: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="ba365-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="ba365-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="ba365-105">Symptoms</span></span>

<span data-ttu-id="ba365-106">Mēģinot apstiprināt kravu, sistēma rāda šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="ba365-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="ba365-107">Daļa noslodzei %1 nepieciešamo krājumu vēl nav izdoti un pārvietoti uz galīgo nosūtīšanas novietojumu.</span><span class="sxs-lookup"><span data-stu-id="ba365-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="ba365-108">Tādēļ kravas nosūtīšanu nevar apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="ba365-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="ba365-109">Iemesls</span><span class="sxs-lookup"><span data-stu-id="ba365-109">Cause</span></span>

<span data-ttu-id="ba365-110">Kravu vai sūtījumu nevar apstiprināt tās pašreizējā stāvoklī, jo var pastāvēt viens no tālāk norādītajiem nosacījumiem:</span><span class="sxs-lookup"><span data-stu-id="ba365-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="ba365-111">Saistītais darbs vēl nav izdots un pārvietots uz beigu nosūtīšanas vietu.</span><span class="sxs-lookup"><span data-stu-id="ba365-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="ba365-112">Izdotais darba daudzums nesaskan ar kravas rindā izveidoto darba daudzumu.</span><span class="sxs-lookup"><span data-stu-id="ba365-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>

## <a name="resolution"></a><span data-ttu-id="ba365-113">Novēršana</span><span class="sxs-lookup"><span data-stu-id="ba365-113">Resolution</span></span>

<span data-ttu-id="ba365-114">Pārbaudiet ar kravu vai sūtījumu saistītos pārdošanas pasūtījumus vai pārsūtīšanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="ba365-114">Check the related sales orders or transfer orders for the load or shipment.</span></span> <span data-ttu-id="ba365-115">Pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt.</span><span class="sxs-lookup"><span data-stu-id="ba365-115">Make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="ba365-116">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.</span><span class="sxs-lookup"><span data-stu-id="ba365-116">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="ba365-117">Izvēlieties kravu, kam nevar apstiprināt nosūtījumu.</span><span class="sxs-lookup"><span data-stu-id="ba365-117">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="ba365-118">Kopsavilkuma cilnē **Noslodzes rindas** atlasiet kravas rindas.</span><span class="sxs-lookup"><span data-stu-id="ba365-118">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="ba365-119">Atzīmējiet lauka **Darba izveidotais daudzums** vērtību.</span><span class="sxs-lookup"><span data-stu-id="ba365-119">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="ba365-120">Darbību rūtī cilnē **Kravas** grupā **Saistīta informācija** atlasiet **Darbs**.</span><span class="sxs-lookup"><span data-stu-id="ba365-120">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="ba365-121">Pārbaudiet, vai darbs ir pabeigts galīgās nosūtīšanas vietā un vai izdotais darba daudzums sakrīt ar izveidoto darba daudzumu kravas rindā.</span><span class="sxs-lookup"><span data-stu-id="ba365-121">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="ba365-122">Atkārtojiet šo procedūru visām kravas rindām, lai nodrošinātu visu kritēriju izpildi.</span><span class="sxs-lookup"><span data-stu-id="ba365-122">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>
