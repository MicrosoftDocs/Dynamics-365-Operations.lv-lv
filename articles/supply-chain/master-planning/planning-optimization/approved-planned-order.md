---
title: Skatīt, pārvaldīt un apstiprināt plānotos pasūtījumus
description: Šajā tēmā ir sniegta informācija par to, kā skatīt, pārvaldīt un apstiprināt plānotos pasūtījumus plānošanas optimizācijā.
author: ChristianRytt
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 3b9b5274481e693f9fa05eb084ec5505ce5bc2eb
ms.sourcegitcommit: 9283caad2d0636f98579c995784abec19fda2e3f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935661"
---
# <a name="view-manage-and-approve-planned-orders"></a><span data-ttu-id="52543-103">Skatīt, pārvaldīt un apstiprināt plānotos pasūtījumus</span><span class="sxs-lookup"><span data-stu-id="52543-103">View, manage, and approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="52543-104">Šajā tēmā ir sniegta informācija par to, kā skatīt, pārvaldīt un apstiprināt plānotos pasūtījumus plānošanas optimizācijā.</span><span class="sxs-lookup"><span data-stu-id="52543-104">This topic provides information about how to view, manage, and approve planned orders in Planning Optimization.</span></span>

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a><span data-ttu-id="52543-105">Skatīt un pārvaldīt plānotos pasūtījumus</span><span class="sxs-lookup"><span data-stu-id="52543-105">View and manage planned orders</span></span>

<span data-ttu-id="52543-106">Plānotos pasūtījumus var skatīt un pārvaldīt jebkurā plānoto pasūtījumu saraksta lapā.</span><span class="sxs-lookup"><span data-stu-id="52543-106">You can view and manage planned orders on any planned orders list page.</span></span> <span data-ttu-id="52543-107">Atkarībā no plānotā pasūtījuma tipa, ar kuru vēlaties strādāt, dodieties uz vienu no šīm vietām:</span><span class="sxs-lookup"><span data-stu-id="52543-107">Go to one of the following places, depending on the type of planned orders that you want to work with:</span></span>

- <span data-ttu-id="52543-108">Vispārējā plānošana \> Darbvietas \> Vispārējā plānošana</span><span class="sxs-lookup"><span data-stu-id="52543-108">Master planning \> Workspaces \> Master planning</span></span>
- <span data-ttu-id="52543-109">Vispārējā plānošana \> Vispārējā plānošana \> Plānotie pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="52543-109">Master planning \> Master planning \> Planned orders</span></span>
- <span data-ttu-id="52543-110">Ražošanas kontrole \> Ražošanas pasūtījumi \> Plānotie ražošanas pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="52543-110">Production control \> Production orders \> Planned production orders</span></span>
- <span data-ttu-id="52543-111">Sagāde un avoti \> Pirkšanas pasūtījumi \> Plānotie pirkšanas pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="52543-111">Procurement and sourcing \> Purchase orders \> Planned purchase orders</span></span>
- <span data-ttu-id="52543-112">Krājumu pārvaldība \> Ienākošie pasūtījumi \> Plānotie pārvedumi</span><span class="sxs-lookup"><span data-stu-id="52543-112">Inventory management \> Inbound orders \> Planned transfers</span></span>
- <span data-ttu-id="52543-113">Krājumu pārvaldība \> Izējošie pasūtījumi \> Plānotie pārvedumi</span><span class="sxs-lookup"><span data-stu-id="52543-113">Inventory management \> Outbound orders \> Planned transfers</span></span>

## <a name="view-and-edit-the-status-of-planned-orders"></a><span data-ttu-id="52543-114">Skatiet un rediģēt plānoto pasūtījumu statusu</span><span class="sxs-lookup"><span data-stu-id="52543-114">View and edit the status of planned orders</span></span>

<span data-ttu-id="52543-115">Jūs varat izmantot katra plānotā pasūtījuma lauku **Statuss**, lai palīdzētu atsekot norises gaitu vai izmainīt plānotā pasūtījuma apstrādes veidu.</span><span class="sxs-lookup"><span data-stu-id="52543-115">You can use the **Status** field of each planned order to help track your progress or change how a planned order will be processed.</span></span> <span data-ttu-id="52543-116">Ir pieejami sekojošas **Statuss** vērtības:</span><span class="sxs-lookup"><span data-stu-id="52543-116">The following **Status** values are available:</span></span>

- <span data-ttu-id="52543-117">**Neapstrādāts** - Kad vispārējā plānošana ģenerē plānotos pasūtījumus, tiem tiek piešķirts statuss.</span><span class="sxs-lookup"><span data-stu-id="52543-117">**Unprocessed** – When master planning generates planned orders, they are given this status.</span></span> <span data-ttu-id="52543-118">Plānotie pasūtījumi, kam ir šis statuss tiks dzēsti nākamās plānošanas izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="52543-118">Planned orders that have this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="52543-119">**Pabeigts** – šis statuss norāda, ka plānotais pasūtījums ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="52543-119">**Completed** – This status indicates that the planned order has been completed.</span></span> <span data-ttu-id="52543-120">Ja izvēlaties neapstiprināt plānoto pasūtījumu, varat manuāli mainīt tā statusu uz *Pabeigts*.</span><span class="sxs-lookup"><span data-stu-id="52543-120">If you decide not to firm a planned order, you can manually change its status to *Completed*.</span></span> <span data-ttu-id="52543-121">Ievērojiet, ka sistēma izturas vienādi pret statusiem *Neapstrādāts* un *Pabeigts*.</span><span class="sxs-lookup"><span data-stu-id="52543-121">Note that the system treats the *Unprocessed* and *Completed* statuses in the same way.</span></span>
- <span data-ttu-id="52543-122">**Apstiprināts** – šis statuss norāda, ka plānotais pasūtījums ir apstiprināts apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="52543-122">**Approved** – This status indicates that the planned order is approved for firming.</span></span> <span data-ttu-id="52543-123">Ja vēlaties apstiprināt plānoto pasūtījumu, varat mainīt tā statusu uz *Apstiprināts*.</span><span class="sxs-lookup"><span data-stu-id="52543-123">If you want to firm a planned order, you can change its status to *Approved*.</span></span> <span data-ttu-id="52543-124">Ja vēlaties saglabāt rediģējumus, kas veikti plānotajam pasūtījumam, vai, ja plānojat apstiprināt plānoto pasūtījumu, mainiet tā statusu uz *Apstiprināts*.</span><span class="sxs-lookup"><span data-stu-id="52543-124">If you want to keep the edits that have been made to a planned order, or if you're planning to firm a planned order, change its status to *Approved*.</span></span> <span data-ttu-id="52543-125">Plānotie pasūtījumi ar statusu *Apstiprināts* tiek uzskatīti par fiksētiem un paredzamiem piegādēm pēc vispārējās plānošanas.</span><span class="sxs-lookup"><span data-stu-id="52543-125">Planned orders that have a status of *Approved* are considered fixed and expected supply by master planning.</span></span> <span data-ttu-id="52543-126">Tāpēc tie netiek modificēti vai dzēsti vēlāku vispārējās plānošanas palaišanas laikā.</span><span class="sxs-lookup"><span data-stu-id="52543-126">Therefore, they aren't modified or deleted during later master planning runs.</span></span> <span data-ttu-id="52543-127">Lai to panāktu, plānošanas loģika kopē plānotos pasūtījumus ar statusu *Apstiprinātos* no vecās plāna versijas uz jauno plāna versiju vispārējās plānošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="52543-127">To achieve this behavior, the planning logic copies planned orders that have a status of *Approved* from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="52543-128">Ievērojiet, ka plānotie pasūtījumi, kuru statuss ir *Apstiprināts*\* plānotie pasūtījumi tiek uzskatīti par piegādēm tikai noteiktajā galvenājā plānā.</span><span class="sxs-lookup"><span data-stu-id="52543-128">Note that planned orders that have a status of *Approved*\* are considered supply only within the specific master plan.</span></span>

<span data-ttu-id="52543-129">Lai mainītu atsevišķa plānotā pasūtījuma statusu, [atveriet jebkuru plānoto pasūtījumu saraksta lapu](#view-planned-orders), atveriet pasūtījumu un tad izpildiet vienu no tālāk minētajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="52543-129">To change the status of a single planned order, [open any planned orders list page](#view-planned-orders), open the order, and then follow one of these steps:</span></span>

- <span data-ttu-id="52543-130">Kopsavilkuma cilnē **Vispārīgi** mainiet lauka **Statuss** vērtību.</span><span class="sxs-lookup"><span data-stu-id="52543-130">On the **General** FastTab, change the value of the **Status** field.</span></span>
- <span data-ttu-id="52543-131">Darbību rūtī cilnē **Plānotais pasūtījums** grupā **Process** atlasiet **Mainīt statusu**.</span><span class="sxs-lookup"><span data-stu-id="52543-131">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="52543-132">Darbību rūtī atlasiet **Apstiprināt**, lai atzīmētu pasūtījumu kā apstiprinātu.</span><span class="sxs-lookup"><span data-stu-id="52543-132">On the Action Pane, select **Approve** to mark the order as approved.</span></span>

<span data-ttu-id="52543-133">Lai vienlaicīgi mainītu vairāku plānoto pasūtījumu statusu, [atveriet jebkuru plānoto pasūtījumu saraksta lapu](#view-planned-orders), atzīmējiet izvēles rūtiņu katram pasūtījumam, kuru vēlaties mainīt, un pēc tam izpildiet vienu no šīm darbībām:</span><span class="sxs-lookup"><span data-stu-id="52543-133">To change the status of several planned orders at the same time, [open any planned orders list page](#view-planned-orders), select the check box for each order that you want to change, and then follow one of these steps:</span></span>

- <span data-ttu-id="52543-134">Darbību rūtī cilnē **Plānotais pasūtījums** grupā **Process** atlasiet **Mainīt statusu**.</span><span class="sxs-lookup"><span data-stu-id="52543-134">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="52543-135">Darbību rūtī atlasiet **Apstiprināt**, lai atzīmētu pasūtījumus kā apstiprinātus.</span><span class="sxs-lookup"><span data-stu-id="52543-135">On the Action Pane, select **Approve** to mark the orders as approved.</span></span>

## <a name="approve-planned-orders"></a><span data-ttu-id="52543-136">Plānoto pasūtījumu apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="52543-136">Approve planned orders</span></span>

<span data-ttu-id="52543-137">Plānoto pasūtījumu apstiprināšana ir neobligāts solis apstiprināta pasūtījuma izveides procesā no plānotā pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="52543-137">Approval of planned orders is an optional step in the process of creating a firmed order from a planned order.</span></span>

<span data-ttu-id="52543-138">Šajā attēlā parādīts, kā var izmantot vērtību **Statuss**, kas ir piešķirta katram plānotajam pasūtījumam, lai ieviestu apstiprināšanas darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="52543-138">The following illustration shows how you can use the **Status** value that is assigned to each planned order to implement an approval workflow.</span></span> <span data-ttu-id="52543-139">Lai ieviestu apstiprināšanas procesu, manuāli pielāgojiet vērtību **Statuss** katram plānotajam pasūtījumam, kā aprakstīts iepriekšējā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="52543-139">To implement an approval process, manually adjust the **Status** value for each planned order as described in the previous section.</span></span>

![Plānotā pasūtījumu plūsma](media/approved-planned-orders-1.png)

> [!TIP]
> <span data-ttu-id="52543-141">Modificētus plānotos pasūtījumus ieteicams apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="52543-141">We recommend that you approve any modified planned orders.</span></span> <span data-ttu-id="52543-142">Pretējā gadījumā nākamās plānošanas darbības laikā labojumi tiks ignorēti un pārrakstīti.</span><span class="sxs-lookup"><span data-stu-id="52543-142">Otherwise, the edits will be ignored and overwritten by the next planning run.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="52543-143">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="52543-143">Additional resources</span></span>

- [<span data-ttu-id="52543-144">Plānoto pasūtījumu apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="52543-144">Firm planned orders</span></span>](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
