---
title: Izveidot uzturēšanas pieprasījumus
description: Šajā tēmā izskaidrots, kā izveidot uzturēšanas pieprasījumu Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: af67d320f14fc6c3d28eec47de402ba645eea06d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836786"
---
# <a name="create-maintenance-requests"></a><span data-ttu-id="16065-103">Izveidot uzturēšanas pieprasījumus</span><span class="sxs-lookup"><span data-stu-id="16065-103">Create maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="16065-104">Uzturēšanas pieprasījumus var izmantot, ja uzturēšanas darbinieki vai ražošanas darbinieki atklāj, ka aprīkojumam nepieciešams remonts, bet remonta darbus nevar veikt uzreiz.</span><span class="sxs-lookup"><span data-stu-id="16065-104">Maintenance requests can be used if maintenance workers or production workers discover that equipment requires repair, but the repair job can't be done right away.</span></span>

<span data-ttu-id="16065-105">**Piemērs:** kamēr uzturēšanas darbiniece veic remontu, viņa atklāj, ka ir nepieciešama cita līdzekļa tajā pašā atrašanās vietā apkope.</span><span class="sxs-lookup"><span data-stu-id="16065-105">**Example:** While a maintenance worker is making a repair, she discovers that another asset at the same location must be serviced.</span></span> <span data-ttu-id="16065-106">Taču uzturēšanas darbiniecei nav ne laika, ne nepieciešamo rezerves daļu, lai veiktu remonta darbus.</span><span class="sxs-lookup"><span data-stu-id="16065-106">However, the maintenance worker doesn't have the time or the required spare parts to do the repair job.</span></span> <span data-ttu-id="16065-107">Tāpēc viņa izveido uzturēšanas pieprasījumu līdzeklim un ievada īsu problēmas aprakstu.</span><span class="sxs-lookup"><span data-stu-id="16065-107">Therefore, she creates a maintenance request on the asset and enters a short description of the issue.</span></span>

<span data-ttu-id="16065-108">Sadaļa **Aktīvie uzturēšanas pieprasījumi** rūtī **Saistītā informācija**, kas atrodas lapas **Visi līdzekļi** vai **Aktīvie līdzekļi** labajā pusē (**Līdzekļu pārvaldība** \> **Kopīgi** \> **Līdzekļi** \> **Visi līdzekļi** vai **Aktīvie līdzekļi**) rāda aktīvos uzturēšanas pieprasījumus, kas ir pievienoti atlasītajam līdzeklim.</span><span class="sxs-lookup"><span data-stu-id="16065-108">The **Active maintenance requests** section of the **Related information** pane on the right side of the **All assets** or **Active assets** page (**Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**) shows the active maintenance requests that are attached to the selected asset.</span></span>

1. <span data-ttu-id="16065-109">Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Uzturēšanas pieprasījumi** \> **Visi uzturēšanas pieprasījumi** vai **Aktīvie uzturēšanas pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="16065-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="16065-110">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="16065-110">Select **New**.</span></span>
3. <span data-ttu-id="16065-111">Dialoglodziņā **Izveidot pieprasījumu** laukā **Uzturēšanas pieprasījuma veids** atlasiet uzturēšanas pieprasījuma veidu.</span><span class="sxs-lookup"><span data-stu-id="16065-111">In the **Create request** dialog box, in the **Maintenance request type** field, select the type of maintenance request.</span></span> <span data-ttu-id="16065-112">Tiek ieteikts noklusētais veids.</span><span class="sxs-lookup"><span data-stu-id="16065-112">A default type is suggested.</span></span>
4. <span data-ttu-id="16065-113">Laukā **Apraksts** ievadiet nosaukumu vai virsrakstu, kas īsumā apraksta uzturēšanas pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="16065-113">In the **Description** field, enter a name or title that briefly describes the maintenance request.</span></span>
5. <span data-ttu-id="16065-114">Laukā **Funkcionālais novietojums** un **Līdzeklis** atlasiet funkcionālo novietojumu vai līdzekli, vai arī funkcionālā novietojuma un līdzekļa kombināciju pēc vajadzības.</span><span class="sxs-lookup"><span data-stu-id="16065-114">In the **Functional location** and **Asset** fields, select a functional location or an asset, or a combination of a functional location and an asset, as you require.</span></span> <span data-ttu-id="16065-115">Varat izveidot uzturēšanas pieprasījumu, neatlasot līdzekli, un līdzekli var pievienot uzturēšanas pieprasījumam vēlāk.</span><span class="sxs-lookup"><span data-stu-id="16065-115">You can create a maintenance request without selecting an asset, and the asset can be added to the maintenance request later.</span></span> <span data-ttu-id="16065-116">Ja uzturēšanas darbinieks, kurš ir pierakstījies, ir saistīts ar resursu, kas saistīts ar līdzekli, automātiski tiek iestatīts lauks **Līdzeklis**.</span><span class="sxs-lookup"><span data-stu-id="16065-116">If the maintenance worker who is signed in is related to a resource that is related to an asset, the **Asset** field is automatically set.</span></span>

    <span data-ttu-id="16065-117">Ja atlasītajam līdzeklim jau ir pievienots uzturēšanas pieprasījums, dialoglodziņa **Izveidot pieprasījumu** augšpusē tiek parādīta ziņojumu josla, lai informētu jūs par esošā uzturēšanas pieprasījuma ID.</span><span class="sxs-lookup"><span data-stu-id="16065-117">If a maintenance request is already attached to the selected asset, a message bar appears at the top of the **Create request** dialog box to notify you about the ID of the existing maintenance request.</span></span> <span data-ttu-id="16065-118">Ziņojumu josla arī informē jūs, ja uz līdzekli attiecas garantijas līgums.</span><span class="sxs-lookup"><span data-stu-id="16065-118">A message bar also notifies you if the asset is covered by a warranty agreement.</span></span>

6. <span data-ttu-id="16065-119">Laukā **Pakalpojumu līmenis** atlasiet pakalpojumu līmeni, kas norāda pieprasījuma steidzamību.</span><span class="sxs-lookup"><span data-stu-id="16065-119">In the **Service level** field, select a service level that indicates the urgency of the request.</span></span>
7. <span data-ttu-id="16065-120">Ja atlasījāt līdzekli 5. solī, varat izmantot laukus **Kļūmes simtoms**, **Kļūmes apgabals** un **Kļūmes veids**, lai izveidotu kļūmes reģistrāciju.</span><span class="sxs-lookup"><span data-stu-id="16065-120">If you selected an asset in step 5, you can use the **Fault symptom**, **Fault area**, and **Fault type** fields to create a fault registration.</span></span>
8. <span data-ttu-id="16065-121">Ja uzturēšanas pieprasījums ir izraisījis uzturēšanas dīkstāvi, ievadiet sākuma datumu un dīkstāves laiku.</span><span class="sxs-lookup"><span data-stu-id="16065-121">If the maintenance request has caused maintenance downtime, enter the start date and time of the downtime.</span></span>

    <span data-ttu-id="16065-122">Lauks **Sācis...** tiek automātiski iestatīts uz jūsu vārda.</span><span class="sxs-lookup"><span data-stu-id="16065-122">The **Started by** field is automatically set to your name.</span></span>

10. <span data-ttu-id="16065-123">Lauks **Faktiskais sākums** automātiski tiek iestatīts uz pašreizējo datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="16065-123">The **Actual start** field is automatically set to the current date and time.</span></span> <span data-ttu-id="16065-124">Tomēr, jūs varat mainīt vērtību pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="16065-124">However, you can change the value as you require.</span></span>
11. <span data-ttu-id="16065-125">Laukā **Piezīmes** ievadiet visas nepieciešamās papildu piezīmes.</span><span class="sxs-lookup"><span data-stu-id="16065-125">In the **Notes** field, enter any additional notes that are required.</span></span>
12. <span data-ttu-id="16065-126">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="16065-126">Select **OK**.</span></span>

![Izveidot uzturēšanas pieprasījumu](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a><span data-ttu-id="16065-128">Turpmāka uzturēšanas pieprasījumu apstrāde</span><span class="sxs-lookup"><span data-stu-id="16065-128">Subsequent processing of maintenance requests</span></span>

<span data-ttu-id="16065-129">Pēc uzturēšanas pieprasījuma izveides, bet pirms tā pārveidošanas par darba pasūtījumu, tajā ir jāatjaunina dažāda informācija.</span><span class="sxs-lookup"><span data-stu-id="16065-129">After a maintenance request is created, but before it's converted to a work order, various information should be updated on it.</span></span> <span data-ttu-id="16065-130">Parasti šo uzdevumu pabeidz plānotājs vai cits administratīvais darbinieks.</span><span class="sxs-lookup"><span data-stu-id="16065-130">Typically, a planner or another administrative employee completes this task.</span></span>

- <span data-ttu-id="16065-131">Lapā **Visi uzturēšanas pieprasījumi** vai **Aktīvie uzturēšanas pieprasījumi** atlasiet pieprasījumu, ar kuru strādāt, un pēc tam atlasiet **Rediģēt.**</span><span class="sxs-lookup"><span data-stu-id="16065-131">On the **All maintenance requests** or **Active maintenance requests** page, select the request to work with, and then select **Edit**.</span></span>

<span data-ttu-id="16065-132">Detalizētas informācijas skatā varat atjaunināt dažādu informāciju.</span><span class="sxs-lookup"><span data-stu-id="16065-132">In the details view, you can update various information.</span></span> <span data-ttu-id="16065-133">Daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="16065-133">Here are some examples:</span></span>

- <span data-ttu-id="16065-134">Atlasiet un pārbaudiet līdzekli.</span><span class="sxs-lookup"><span data-stu-id="16065-134">Select and verify the asset.</span></span> <span data-ttu-id="16065-135">Ja vēlāk ir jāatlasa cits līdzeklis, varat iestatīt opciju **Līdzeklis verificēts** uz **Nē.**</span><span class="sxs-lookup"><span data-stu-id="16065-135">If you must select a different asset later, you can set the **Asset verified** option to **No**.</span></span>
- <span data-ttu-id="16065-136">Atlasiet atbildīgo uzturēšanas darbinieku grupu un/vai atbildīgo uzturēšanas darbinieku.</span><span class="sxs-lookup"><span data-stu-id="16065-136">Select a responsible maintenance worker group and/or a responsible maintenance worker.</span></span> <span data-ttu-id="16065-137">Papildinformāciju par nepieciešamajiem iestatījumiem skatiet sadaļā [Atbildīgie uzturēšanas darbinieki](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="16065-137">For more information about the required setup, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>
- <span data-ttu-id="16065-138">Atlasiet uzturēšanas darba veidu un, ja šī informācija ir būtiska, saistīto uzturēšanas darba variantu un darba tirdzniecību.</span><span class="sxs-lookup"><span data-stu-id="16065-138">Select a maintenance job type and, if this information is relevant, a related maintenance job variant and a job trade.</span></span>
- <span data-ttu-id="16065-139">Laukos **Platums** un **Garums** ievadiet ģeogrāfiskās koordinātas.</span><span class="sxs-lookup"><span data-stu-id="16065-139">In the **Latitude** and **Longitude** fields, enter geographic coordinates.</span></span> <span data-ttu-id="16065-140">Visas koordinātas, kas tiek pievienotas uzturēšanas pieprasījumam, tiek automātiski pārsūtītas uz saistīto darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="16065-140">Any coordinates that are added to a maintenance request are automatically transferred to a related work order.</span></span> 

![Uzturēšanas pieprasījuma atjaunināšana](media/04-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="16065-142">Ja atlasāt līdzekli, veidojot uzturēšanas pieprasījumu, varat līdzeklim pievienot vienu kļūmi.</span><span class="sxs-lookup"><span data-stu-id="16065-142">If you select an asset when you create a maintenance request, you can add one fault to the asset.</span></span> <span data-ttu-id="16065-143">Pēc uzturēšanas pieprasījuma izveides varat pievienot vairāk kļūmju — kā nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="16065-143">After the maintenance request has been created, you can add more faults, as you require.</span></span> <span data-ttu-id="16065-144">Lai pievienotu kļūmes, atlasiet **Līdzekļa kļūme** lapā **Visi uzturēšanas pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="16065-144">To add faults, select **Asset fault** on the **All maintenance requests** page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]