---
title: Uzturēšanas pieprasījumi
description: Šajā tēmā sniegts pārskats par uzturēšanas pieprasījumu pārvaldību Līdzekļu pārvaldībā
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 56d4abee451e6e22b9b9cc2fd36a13648202e7df
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847440"
---
# <a name="maintenance-requests"></a><span data-ttu-id="9655a-103">Uzturēšanas pieprasījumi</span><span class="sxs-lookup"><span data-stu-id="9655a-103">Maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="9655a-104">Uzturēšanas pieprasījumi ir piezīmes vai deklarācijas, kas izveidotas, lai paziņotu vadītājam vai plānotājam, ka līdzeklim var būt nepieciešams uzturēšanas vai labošanas darbs, taču neveidojot darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="9655a-104">Maintenance requests are notes or declarations that are created to notify a manager or planner that an asset might require a maintenance or repair job, but without creating a work order.</span></span> <span data-ttu-id="9655a-105">Ja uzturēšanas pieprasījuma saturs tiek uzskatīts par derīgu, pēc tam var izveidot darba pasūtījumu, pamatojoties uz uzturēšanas pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="9655a-105">If the contents of a maintenance request are considered valid, a work order can then be created based on the maintenance request.</span></span>

<span data-ttu-id="9655a-106">Uzturēšanas pieprasījumus var izveidot jebkuram līdzeklim Līdzekļu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="9655a-106">Maintenance requests can be created for any asset in Asset Management.</span></span> <span data-ttu-id="9655a-107">Atkarībā no tā, kā jūsu uzņēmums izmanto uzturēšanas pieprasījumus, var izveidot dažādus uzturēšanas pieprasījumu veidus.</span><span class="sxs-lookup"><span data-stu-id="9655a-107">Various types of maintenance requests can be created, depending on how your company uses maintenance requests.</span></span> <span data-ttu-id="9655a-108">Daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="9655a-108">Here are some examples:</span></span>

- <span data-ttu-id="9655a-109">Uzturēšanas pieprasījumi</span><span class="sxs-lookup"><span data-stu-id="9655a-109">Maintenance requests</span></span>
- <span data-ttu-id="9655a-110">Piezīmes</span><span class="sxs-lookup"><span data-stu-id="9655a-110">Notes</span></span>
- <span data-ttu-id="9655a-111">Labojumi vai uzlabojumi</span><span class="sxs-lookup"><span data-stu-id="9655a-111">Corrections or enhancements</span></span>
- <span data-ttu-id="9655a-112">Investīcijas</span><span class="sxs-lookup"><span data-stu-id="9655a-112">Investments</span></span>
- <span data-ttu-id="9655a-113">Labošana noliktavā (Šis veids tiek izmantots, ja saņemat līdzekļus no citas atrašanās vietas, lai varētu veikt uzturēšanas vai labošanas darbu, un pēc tam atgriežat līdzekli, kad darbs ir pabeigts.)</span><span class="sxs-lookup"><span data-stu-id="9655a-113">Depot repair (This type is used when you receive assets from another location so that you can do a maintenance or repair job, and you then return the asset after the job is completed.)</span></span>

## <a name="view-maintenance-requests"></a><span data-ttu-id="9655a-114">Skatīt uzturēšanas pieprasījumus</span><span class="sxs-lookup"><span data-stu-id="9655a-114">View maintenance requests</span></span>

<span data-ttu-id="9655a-115">Lai skatītu uzturēšanas pieprasījumus, atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Uzturēšanas pieprasījumi** \> **Visi uzturēšanas pieprasījumi**, **Aktīvie ctive uzturēšanas pieprasījumi** vai **Mani funkcionālā novietojuma uzturēšanas pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="9655a-115">To view maintenance requests, select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests**, **Active maintenance requests**, or **My functional location maintenance requests**.</span></span> <span data-ttu-id="9655a-116">Katrā saraksta lapā ir redzama daļa no informācijas, kas saistīta ar uzturēšanas pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="9655a-116">Each list page shows some of the information that is related to a maintenance request.</span></span>

![1. attēls](media/01-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="9655a-118">Izmantojiet saraksta lapu **Mani funkcionālā novietojuma uzturēšanas pieprasījumi**, lai skatītu uzturēšanas pieprasījumu sarakstu, kas ietver vai nu funkcionālos novietojumus, ar kuriem esat saistīts kā darbinieks vai līdzekļus, kas ir uzstādīti funkcionālajos novietojumos, ar kuriem esat saistīts kā darbinieks.</span><span class="sxs-lookup"><span data-stu-id="9655a-118">Use the **My functional location maintenance requests** list page to view a list of maintenance requests that contain either functional locations that you're related to as a worker or assets that are installed on functional locations that you're related to as a worker.</span></span> <span data-ttu-id="9655a-119">(Informāciju par to, kā iestatīt funkcionālos novietojumus uzturēšanas darbiniekiem, skatiet sadaļā [Uzturēšanas darbinieki un darbinieku grupas](../setup-for-objects/workers-and-worker-groups.md).)</span><span class="sxs-lookup"><span data-stu-id="9655a-119">(For information about how to set up functional locations on maintenance workers, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).)</span></span>
> 
> <span data-ttu-id="9655a-120">Kaut arī debitora konta informācija ir pieejama Līdzekļu pakalpojumu pārvaldībā (ārējā uzturēšana), tā nav pieejama Līdzekļu pārvaldībā (iekšējā uzturēšana).</span><span class="sxs-lookup"><span data-stu-id="9655a-120">Although customer account information is available in Asset Service Management (external maintenance), it isn't available in Asset Management (internal maintenance).</span></span>

<span data-ttu-id="9655a-121">Lai atvērtu ieraksta detalizētu skatu saraksta lapā **Visi uzturēšanas pieprasījumu**, režģa skatā atlasiet saiti kolonnā **Uzturēšanas pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="9655a-121">To open the details view of a record, on the **All maintenance requests** list page, in the grid view, select a link in the **Maintenance request** column.</span></span>

![2. attēls](media/02-manage-maintenance-requests.png)

<span data-ttu-id="9655a-123">Pogas darbības rūtī ir sakārtotas cilnēs.</span><span class="sxs-lookup"><span data-stu-id="9655a-123">The buttons on the Action Pane are organized on tabs.</span></span> <span data-ttu-id="9655a-124">Nākamajā tabulā ir īsi aprakstītas pogas, kas saistītas ar Līdzekļu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="9655a-124">The following table briefly describes the buttons that are related to Asset Management.</span></span>

| <span data-ttu-id="9655a-125">Pogas nosaukums</span><span class="sxs-lookup"><span data-stu-id="9655a-125">Button name</span></span>                      | <span data-ttu-id="9655a-126">Apraksts</span><span class="sxs-lookup"><span data-stu-id="9655a-126">Description</span></span> |
|----------------------------------|-------------|
| <span data-ttu-id="9655a-127">Labot</span><span class="sxs-lookup"><span data-stu-id="9655a-127">Edit</span></span>                             | <span data-ttu-id="9655a-128">Rediģēt atlasīto uzturēšanas pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="9655a-128">Edit the selected maintenance request.</span></span> |
| <span data-ttu-id="9655a-129">Jauna</span><span class="sxs-lookup"><span data-stu-id="9655a-129">New</span></span>                              | <span data-ttu-id="9655a-130">Izveidot jaunu uzturēšanas pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="9655a-130">Create a new maintenance request.</span></span> |
| <span data-ttu-id="9655a-131">Dzēst</span><span class="sxs-lookup"><span data-stu-id="9655a-131">Delete</span></span>                           | <span data-ttu-id="9655a-132">Dzēst atlasīto uzturēšanas pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="9655a-132">Delete the selected maintenance request.</span></span> |
| <span data-ttu-id="9655a-133">Darba pasūtījumu kopa</span><span class="sxs-lookup"><span data-stu-id="9655a-133">Work order pool</span></span>                  | <span data-ttu-id="9655a-134">Pievienojiet atlasīto uzturēšanas pieprasījumu darba pasūtījumu kopai.</span><span class="sxs-lookup"><span data-stu-id="9655a-134">Connect the selected maintenance request to a work order pool.</span></span> |
| <span data-ttu-id="9655a-135">Darba pasūtījums</span><span class="sxs-lookup"><span data-stu-id="9655a-135">Work order</span></span>                       | <span data-ttu-id="9655a-136">Izveidojiet darba pasūtījumu, pamatojoties uz atlasīto uzturēšanas pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="9655a-136">Create a work order, based on the selected maintenance request.</span></span> |
| <span data-ttu-id="9655a-137">Līdzekļa defekts</span><span class="sxs-lookup"><span data-stu-id="9655a-137">Asset fault</span></span>                      | <span data-ttu-id="9655a-138">Noklikšķiniet uz **Līdzekļa defekti**, kur varat izveidot defektu reģistrāciju atlasītajā uzturēšanas pieprasījumā.</span><span class="sxs-lookup"><span data-stu-id="9655a-138">Click **Asset faults**, where you can create a fault registration on the selected maintenance request.</span></span> |
| <span data-ttu-id="9655a-139">Darba pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="9655a-139">Work orders</span></span>                      | <span data-ttu-id="9655a-140">Parādīt sarakstu ar visiem darba pasūtījumiem, kas ir saistīti ar atlasīto uzturēšanas pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="9655a-140">Show a list of all work orders that are connected to the selected maintenance request.</span></span> |
| <span data-ttu-id="9655a-141">Uzturēšanas pieprasījuma stāvokļa atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="9655a-141">Update maintenance request state</span></span> | <span data-ttu-id="9655a-142">Atjauniniet uzturēšanas pieprasījuma stāvokli.</span><span class="sxs-lookup"><span data-stu-id="9655a-142">Update the maintenance request state.</span></span> |
| <span data-ttu-id="9655a-143">Dzīves cikla stāvokļa žurnāls</span><span class="sxs-lookup"><span data-stu-id="9655a-143">Lifecycle state log</span></span>              | <span data-ttu-id="9655a-144">Skatiet žurnālu, kas rāda atlasītā uzturēšanas pieprasījuma dzīves cikla stāvokļus.</span><span class="sxs-lookup"><span data-stu-id="9655a-144">View a log that shows the lifecycle states of the selected maintenance request.</span></span> |
| <span data-ttu-id="9655a-145">Detalizēta informācija par uzturēšanas pieprasījumu</span><span class="sxs-lookup"><span data-stu-id="9655a-145">Maintenance request details</span></span>      | <span data-ttu-id="9655a-146">Izdrukājiet pārskatu, kas rāda detalizētu informāciju par atlasīto uzturēšanas pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="9655a-146">Print a report that shows details of the selected maintenance request.</span></span> |
| <span data-ttu-id="9655a-147">Patapinājuma līdzekļa nosūtīšana</span><span class="sxs-lookup"><span data-stu-id="9655a-147">Send loan asset</span></span>                  | <span data-ttu-id="9655a-148">Atlasiet patapinājuma līdzekli, kam vajadzētu būt pagaidu aizstājējam līdzeklim, kurš atlasīts atlasītajā uzturēšanas pieprasījumā.</span><span class="sxs-lookup"><span data-stu-id="9655a-148">Select a loan asset that should be a temporary replacement for the asset that is selected on the selected maintenance request.</span></span> |
| <span data-ttu-id="9655a-149">Patapinājuma līdzekļa atgriešana</span><span class="sxs-lookup"><span data-stu-id="9655a-149">Return loan asset</span></span>                | <span data-ttu-id="9655a-150">Reģistrējiet patapinājuma līdzekli kā atgrieztu.</span><span class="sxs-lookup"><span data-stu-id="9655a-150">Register the loan asset as returned.</span></span> |

