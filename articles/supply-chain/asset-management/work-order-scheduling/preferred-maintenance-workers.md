---
title: Iestatīt vēlamos uzturēšanas speciālistus
description: Šajā tēmā paskaidrots, kā uzstādīt vēlamos uzturēšanas speciālistus programmā Asset Management.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkerPreferred
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c0637609a34890360a3b81355a8d21ef1b9faf8c
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888933"
---
# <a name="set-up-preferred-maintenance-workers"></a><span data-ttu-id="af92c-103">Iestatīt vēlamos uzturēšanas speciālistus</span><span class="sxs-lookup"><span data-stu-id="af92c-103">Set up preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="af92c-104">Darba pasūtījuma plānošanas laikā jūs varat dot priekšroku tam, kuri uzturēšanas speciālisti vai speciālistu grupa ir piešķirti, lai izpildītu darba pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="af92c-104">During work order scheduling, you can make a preference regarding which maintenance worker or worker group is allocated to complete the work order.</span></span> <span data-ttu-id="af92c-105">Šīs funkcionalitātes lietošana nav obligāta, taču tā var jums palīdzēt izvēlēties kvalificētāko uzturēšanas speciālistu, kurš pabeigtu darbu, pamatojoties uz speciālista prasmēm un kompetenci.</span><span class="sxs-lookup"><span data-stu-id="af92c-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="af92c-106">Ieplānoti tiks vienīgi tie uzturēšanas speciālisti, kuri ir pieejami plānošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="af92c-106">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="af92c-107">Ja vēlamā uzturēšanas speciālista uzstādījums plānošanas laikā atbilst darba pasūtījumam, taču uzturēšanas speciālists ir piešķirts citiem darbiem, darba pasūtījums tiks ieplānots citam pieejamajam uzturēšanas speciālistam.</span><span class="sxs-lookup"><span data-stu-id="af92c-107">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another available maintenance worker.</span></span>

<span data-ttu-id="af92c-108">Iekams jūs varat uzstādīt vēlamos uzturēšanas speciālistus, jums ir vispirms jāuzstāda tie uzturēšanas speciālisti un speciālistu grupas.</span><span class="sxs-lookup"><span data-stu-id="af92c-108">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups.</span></span> <span data-ttu-id="af92c-109">Lai uzzinātu, kā uzstādīt uzturēšanas speciālistus un speciālistu grupas, skatiet sadaļu [Uzturēšanas speciālisti un speciālistu grupas](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="af92c-109">For a description about how to set up maintenance workers and worker groups, see to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="af92c-110">Vēlamo speciālistu uzstādīšana.</span><span class="sxs-lookup"><span data-stu-id="af92c-110">Set up preferred workers</span></span>

<span data-ttu-id="af92c-111">Vēlamais uzturēšanas speciālists vai speciālistu grupa var būt saistīti ar vienu vai vairākiem no šiem:</span><span class="sxs-lookup"><span data-stu-id="af92c-111">A preferred maintenance worker or worker group can be related to one or more of the following:</span></span>

- <span data-ttu-id="af92c-112">tirdzniecība</span><span class="sxs-lookup"><span data-stu-id="af92c-112">trade</span></span>  
- <span data-ttu-id="af92c-113">uzturēšanas darba tipa variantu</span><span class="sxs-lookup"><span data-stu-id="af92c-113">maintenance job type variant</span></span>  
- <span data-ttu-id="af92c-114">uzturēšanas darba tipu</span><span class="sxs-lookup"><span data-stu-id="af92c-114">maintenance job type</span></span>  
- <span data-ttu-id="af92c-115">uzturēšanas darba tipa kategoriju</span><span class="sxs-lookup"><span data-stu-id="af92c-115">maintenance job type category</span></span>  
- <span data-ttu-id="af92c-116">aktīvs</span><span class="sxs-lookup"><span data-stu-id="af92c-116">asset</span></span>  
- <span data-ttu-id="af92c-117">līdzekļa tipu</span><span class="sxs-lookup"><span data-stu-id="af92c-117">asset type</span></span>  

<span data-ttu-id="af92c-118">Jo vairāk atlašu veicat vienam un tam pašam ierakstam, jo konkrētāks būs jūsu iestatījums.</span><span class="sxs-lookup"><span data-stu-id="af92c-118">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="af92c-119">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Uzstādījums** > **Speciālisti** > **Vēlamie uzturēšanas speciālisti**.</span><span class="sxs-lookup"><span data-stu-id="af92c-119">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="af92c-120">Noklikšķiniet uz **Jauns**, lai izveidotu jaunu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="af92c-120">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="af92c-121">Sāciet ar "noklusējuma" uzturēšanas speciālista vai speciālistu grupas izveidi.</span><span class="sxs-lookup"><span data-stu-id="af92c-121">Start by creating a "default" maintenance worker or worker group.</span></span> <span data-ttu-id="af92c-122">Tas nozīmē, ka jūs varat izdarīt atlasi vienīgi laukos **Vēlamā uzturēšanas speciālistu grupa** vai **Vēlamais uzturēšanas speciālists**.</span><span class="sxs-lookup"><span data-stu-id="af92c-122">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="af92c-123">Ekrānuzņēmumā zemāk ir redzams piemērs pirmajam ierakstam, kurā kā **Vēlamā uzturēšanas speciālistu grupa** ir atlasīta "Pieprasījumi".</span><span class="sxs-lookup"><span data-stu-id="af92c-123">In the screenshot below, you see an example in the first record in which "Requests" is selected as **Preferred maintenance worker group**.</span></span>

    [!NOTE] <span data-ttu-id="af92c-124">Noklusējuma iestatījums tiks izmantots darba pasūtījuma plānošanā, ja neviena cita specifiska kombinācija neatbilst darba pasūtījuma saturam.</span><span class="sxs-lookup"><span data-stu-id="af92c-124">The default setup will be used during work order scheduling if no other, more specific, combination matches the contents of the work order.</span></span>

4. <span data-ttu-id="af92c-125">Atkārtojiet 2. darbību, lai izveidotu jaunu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="af92c-125">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="af92c-126">Veiciet nepieciešamo atlasi atkarībā no vēlamā speciālista vai speciālistu grupas detalizācijas līmeņa.</span><span class="sxs-lookup"><span data-stu-id="af92c-126">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> 

    <span data-ttu-id="af92c-127">*Piemērs:* Ekrānuzņēmumā zemāk sestais ieraksts - uzturēšanas speciālists Šons Ričardsons - ir atlasīts kā vēlamais speciālists.</span><span class="sxs-lookup"><span data-stu-id="af92c-127">*Example:* In the screenshot below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="af92c-128">Viņš tiks automātiski atlasīts darba pasūtījuma plānošanas laikā, kura ietver līdzekli "CH-BP1-03-02" un uzturēšanas darba veidu "Iekārtu novērtējums", ja viņš būs pieejams plānotajā laikā.</span><span class="sxs-lookup"><span data-stu-id="af92c-128">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintenance job type "Facility assessment", if he is available at the scheduled time.</span></span>

    [!NOTE] <span data-ttu-id="af92c-129">Parasti, kad darba pasūtījuma plānošanas laikā tiek atlasīts vēlamais uzturēšanas speciālists, programma Asset Management iziet cauri visiem ierakstiem **Vēlamie uzturēšanas speciālisti**, lai pārbaudītu, vai nav iespējamas atbilstības, vienmēr pārbaudot viskonkrētāko kombināciju.</span><span class="sxs-lookup"><span data-stu-id="af92c-129">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="af92c-130">Tas nozīmē, ka, ja nav atrasta atbilstība, tiek izmantots "noklusējuma" ieraksts ar atlasi vai nu laukā **Vēlamā uzturēšanas speciālistu grupa** vai **Vēlamais uzturēšanas speciālists**.</span><span class="sxs-lookup"><span data-stu-id="af92c-130">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>

![1. attēls](media/02-work-order-scheduling.png)

<span data-ttu-id="af92c-132">Jūs varat arī uzstādīt *atbildīgos* uzturēšanas speciālistus, kurus var atlasīt, kad tiek izveidots uzturēšanas pieprasījums vai darba pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="af92c-132">You can also set up *responsible* maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="af92c-133">Jūs varat rediģēt atlasi laukos **Visi darba pasūtījumi** un **Visi uzturēšanas pieprasījumi**, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="af92c-133">You can edit the selection in **All work orders** and **All maintenance requests**, if required.</span></span> <span data-ttu-id="af92c-134">Papildinformāciju skatiet lapā [Atbildīgie uzturēšanas speciālisti](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="af92c-134">For more information, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

<span data-ttu-id="af92c-135">Darba pasūtījuma plānošanas laikā, tiek aprēķināti dažādi rezultāti, lai noteiktu, kuriem speciālistiem vajadzētu pabeigt darbus, kas saistīti ar darba pasūtījumu (šie rezultāti tiek uzstādīti, dodoties uz **Līdzekļu pārvaldības parametri** > **Darba pasūtījumu plānošanas** saiti).</span><span class="sxs-lookup"><span data-stu-id="af92c-135">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="af92c-136">Ja divi vai vairāk vēlamie uzturēšanas speciālisti vai atbildīgie uzturēšanas speciālisti darba pasūtījuma plānošanas laikā saņem vienādu rezultātu, viens speciālists tiek atlasīts nejauši.</span><span class="sxs-lookup"><span data-stu-id="af92c-136">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="af92c-137">Pretējā gadījumā darba pasūtījuma pabeigšanai vienmēr tiek piešķirts speciālists ar augstāko rezultātu.</span><span class="sxs-lookup"><span data-stu-id="af92c-137">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

