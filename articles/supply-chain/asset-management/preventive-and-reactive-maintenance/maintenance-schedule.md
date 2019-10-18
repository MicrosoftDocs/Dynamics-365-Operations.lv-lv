---
title: Uzturēšanas grafiks
description: Šajā tēmā ir paskaidrotas uzturēšanas grafiks programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: af2152b334b51db48b60aa966ab49bf480c29bbc
ms.sourcegitcommit: 6476f27c8d3dced7c2e9a7344a4e378b51a1983e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/27/2019
ms.locfileid: "1922141"
---
# <a name="maintenance-schedule"></a><span data-ttu-id="04d50-103">Uzturēšanas grafiks</span><span class="sxs-lookup"><span data-stu-id="04d50-103">Maintenance schedule</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="04d50-104">Uzturēšanas grafiks satur sarakstu ar visiem paredzamajiem preventīvajiem uzturēšanas plāniem, uzturēšanas pieprasījumiem un uzturēšanas cikliem, kuri ir jāveic. Dažas grafika rindas var konvertēt darba pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="04d50-104">The maintenance schedule contains a list of all the expected preventive maintenance plans, maintenance requests, and maintenance rounds to be carried out. Some schedule lines may have been converted to work orders.</span></span>

<span data-ttu-id="04d50-105">Četri uzturēšanas grafika skati ir nedaudz atšķirīgi, atkarībā no tā, kuras uzturēšanas grafika rindas vēlaties redzēt.</span><span class="sxs-lookup"><span data-stu-id="04d50-105">The four maintenance schedule views are slightly different, depending on which maintenance schedule lines you want to see.</span></span>

| <span data-ttu-id="04d50-106">Izvēlnes elements</span><span class="sxs-lookup"><span data-stu-id="04d50-106">Menu item</span></span>                  | <span data-ttu-id="04d50-107">Satura apraksts</span><span class="sxs-lookup"><span data-stu-id="04d50-107">Description of contents</span></span>                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04d50-108">Viss uzturēšanas grafiks</span><span class="sxs-lookup"><span data-stu-id="04d50-108">All maintenance schedule</span></span>       | <span data-ttu-id="04d50-109">Tiek uzrādītas visas uzturēšanas grafika rindas.</span><span class="sxs-lookup"><span data-stu-id="04d50-109">All maintenance schedule lines are shown.</span></span>     |
| <span data-ttu-id="04d50-110">Mans līdzekļu grafiks</span><span class="sxs-lookup"><span data-stu-id="04d50-110">My asset schedule</span></span>        | <span data-ttu-id="04d50-111">Visas uzturēšanas grafika rindas, kas satur līdzekļus, kas instalēti funkcionālajā novietojumā, ar kuru esat saistīts kā speciālists (uzstādītas sadaļā [Uzturēšanas speciālisti un speciālistu grupas](../setup-for-objects/workers-and-worker-groups.md)) tiek parādītas šajā sarakstā.</span><span class="sxs-lookup"><span data-stu-id="04d50-111">All maintenance schedule lines containing assets installed on functional locations to which you are related as a worker (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)) are shown in this list.</span></span> |
| <span data-ttu-id="04d50-112">Atvērt uzturēšanas grafika rindas</span><span class="sxs-lookup"><span data-stu-id="04d50-112">Open maintenance schedule lines</span></span> | <span data-ttu-id="04d50-113">Uzturēšanas grafika rindas ar statusu "Izveidota" - kas nozīmē, ka tās vēl nav konvertētas darba pasūtījumā vai atceltas - tiek uzrādītas šajā sarakstā.</span><span class="sxs-lookup"><span data-stu-id="04d50-113">Maintenance schedule lines with status "Created" - meaning they have not yet been converted to a work order or discarded - are shown in this list.</span></span>                                            |
| <span data-ttu-id="04d50-114">Atvērt uzturēšanas grafika kopas</span><span class="sxs-lookup"><span data-stu-id="04d50-114">Open maintenance schedule pools</span></span> | <span data-ttu-id="04d50-115">Uzturēšanas grafika rindas, kuras ir saistītas ar darba pasūtījumu kopu, tiek uzrādītas šajā sarakstā.</span><span class="sxs-lookup"><span data-stu-id="04d50-115">Maintenance schedule lines related to a work order pool are shown in this list.</span></span>                                                                                                                  |

>[!NOTE]
><span data-ttu-id="04d50-116">Ja pasūtījuma grafika rinda ir ietverta vairākās darba pasūtījumu kopās (skatīt [Darba pasūtījumu kopas](../work-orders/work-order-pools.md)), katrai kopai tiek uzrādīts viens ieraksts opcijā **Atvērt uzturēšanas grafiku kopas**.</span><span class="sxs-lookup"><span data-stu-id="04d50-116">If a maintenance schedule line is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="04d50-117">Tas tiek darīts, lai optimizētu filtrēšanas opcijas darba pasūtījumu kopām.</span><span class="sxs-lookup"><span data-stu-id="04d50-117">This is done to optimize filtering options on work order pools.</span></span>

<span data-ttu-id="04d50-118">Lai atvērtu uzturēšanas grafiku:</span><span class="sxs-lookup"><span data-stu-id="04d50-118">To open a maintenance schedule:</span></span>

1. <span data-ttu-id="04d50-119">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Vispārīgi** > **Uzturēšanas grafiks** > **Visi uzturēšanas grafiki** vai **Atvērt uzturēšanas grafika rindas** vai **Atvērt uzturēšanas grafika kopas**.</span><span class="sxs-lookup"><span data-stu-id="04d50-119">Click **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="04d50-120">Lai atjauninātu uzturēšanas grafiku, noklikšķiniet uz **Uzturēšanas plāns** vai **Uzturēšanas cikli**.</span><span class="sxs-lookup"><span data-stu-id="04d50-120">To update the maintenance schedule, click **Maintenance plan** or **Maintenance rounds**.</span></span> 

3. <span data-ttu-id="04d50-121">Jūs varat rediģēt uzturēšanas grafika rindu, atlasot to un noklikšķinot uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="04d50-121">You can edit a maintenance schedule line by selecting it and clicking **Edit**.</span></span> <span data-ttu-id="04d50-122">Piemēram, jūs varat viegli atjaunināt servisa līmeni vai par darbu atbildīgo speciālistu.</span><span class="sxs-lookup"><span data-stu-id="04d50-122">For example, you can easily update the service level or the worker responsible for the job.</span></span> <span data-ttu-id="04d50-123">Jūs varat rediģēt vienīgi tās uzturēšanas grafika rindas, kuras vēl nav savienotas ar darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="04d50-123">You can only edit maintenance schedule lines that have not yet been connected to a work order.</span></span>

4. <span data-ttu-id="04d50-124">Jūs varat dzēst uzturēšanas grafika rindu, atlasot to saraksta lapā un noklikšķinot uz **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="04d50-124">You can delete a maintenance schedule line by selecting it in the list page and clicking **Delete**.</span></span>

5. <span data-ttu-id="04d50-125">Jūs varat atcelt uzturēšanas grafika rindu, atlasot to saraksta lapā un noklikšķinot uz **Atcelt**.</span><span class="sxs-lookup"><span data-stu-id="04d50-125">You can discard a maintenance schedule line by selecting it in the list page and clicking **Discard**.</span></span> <span data-ttu-id="04d50-126">Šī funkcija ir noderīga, ja, piemēram, līdzeklim ir 2000 km uzturēšanas plāns un 10 000 km uzturēšanas plāns.</span><span class="sxs-lookup"><span data-stu-id="04d50-126">This function is useful if, for example, an asset has a 2,000 km maintenance plan and a 10,000 km maintenance plan.</span></span> <span data-ttu-id="04d50-127">Tādā gadījumā jūs varat vēlēties atcelt rindu, kas izveidota no 2000 km uzturēšanas plāna, ja tas sakrīt ar 10 000 km, 20 000 km, 30 000 km u.t.t.</span><span class="sxs-lookup"><span data-stu-id="04d50-127">Then, you may want to discard the line created from the 2,000 km maintenance plan when it coincides with 10,000 km, 20,000 km, 30,000 km, and so on.</span></span> <span data-ttu-id="04d50-128">Ja jūs atceļat uzturēšanas grafika rindu, kas ir saistīta ar uzturēšanas plānu, šī rinda nekad vairs neparādīsies, kad šis uzturēšanas plāns tiek ieplānots.</span><span class="sxs-lookup"><span data-stu-id="04d50-128">If you discard a maintenance schedule line related to a maintenance plan, that line will never again appear when that maintenance plan is scheduled.</span></span>

6. <span data-ttu-id="04d50-129">Jūs varat atlasīt uzturēšanas rindu skaitu sadaļā **Visi uzturēšanas grafiki** un noklikšķināt uz **Darba pasūtījumu kopa**, ja jūs vēlaties, lai visas atlasītās rindas tiek iekļautas vienā darba pasūtījumu kopā.</span><span class="sxs-lookup"><span data-stu-id="04d50-129">You can select a number of maintenance schedule lines in **All maintenance schedule** and click **Work order pool**, if you want all selected lines to be included in the same work order pool.</span></span>

7. <span data-ttu-id="04d50-130">Jūs varat atlasīt uzturēšanas rindas sadaļā **Visi uzturēšanas grafiki** vai **Atvērt uzturēšanas grafiku rindas** vai **Atvērt uzturēšanas grafiku kopas** un noklikšķināt uz **Pielāgot grafiku**, ja vēlaties veikt vienādus pielāgojumus vairākām rindām.</span><span class="sxs-lookup"><span data-stu-id="04d50-130">You can select a number of maintenance schedule lines in **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** and click **Adjust schedule** if you want to make the same adjustments on several lines.</span></span> <span data-ttu-id="04d50-131">Jūs varat mainīt paredzamos sākuma un beigu datumus, servisa līmeni un atbildīgo uzturēšanas speciālistu grupu vai atbildīgo uzturēšanas speciālistu, kas ir saistīts ar atlasītajām uzturēšanas grafika rindām.</span><span class="sxs-lookup"><span data-stu-id="04d50-131">You can change expected start and end dates, service level, and the responsible maintenance worker group or responsible maintenance worker related to the selected maintenance schedule lines.</span></span>

- <span data-ttu-id="04d50-132">Kad uzturēšanas grafika rinda ir saistīta ar darba pasūtījumu, darba pasūtījuma ID tiks uzrādīts laukā **Darba pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="04d50-132">When a maintenance schedule line has been related to a work order, the work order ID will be displayed in the **Work order** field.</span></span>  
- <span data-ttu-id="04d50-133">Detalizētajā skatā **Visi līdzekļi** kopsavilkuma cilnē **Līdzekļu uzturēšanas plāni** jūs varat līdzeklim atlasīt uzturēšanas plānu.</span><span class="sxs-lookup"><span data-stu-id="04d50-133">In **All assets** details view > **Asset maintenance plans** FastTab, you can select maintenance plans for the asset.</span></span> <span data-ttu-id="04d50-134">Pēc tam, ja dzēšat uzturēšanas plāna rindu, kas saistīta ar līdzekli sadaļā **Visi līdzekļi**, jūs varat arī automātiski dzēst visas uzturēšanas grafika rindas ar statusu "Izveidota", kuras ir izveidotas, pamatojoties uz šo pašu uzturēšanas plānu.</span><span class="sxs-lookup"><span data-stu-id="04d50-134">Later, if you delete a maintenance plan line related to an asset in **All assets**, you also automatically delete all maintenance schedule lines with status "Created" that have been created based on that maintenance plan.</span></span> <span data-ttu-id="04d50-135">Skatīt arī [Izveidot līdzekli](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="04d50-135">See also [Create an asset](../objects/create-an-object.md).</span></span>

<span data-ttu-id="04d50-136">Ilustrācijā zemāk uzrādīta saraksta lapa **Visi uzturēšanas grafiki**.</span><span class="sxs-lookup"><span data-stu-id="04d50-136">The illustration below shows the **All maintenance schedule** list page.</span></span>

![1. attēls](media/16-preventive-maintenance.png)

