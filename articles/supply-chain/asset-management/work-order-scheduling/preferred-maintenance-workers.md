---
title: Iestatīt vēlamos uzturēšanas speciālistus
description: Šajā tēmā paskaidrots, kā uzstādīt vēlamos uzturēšanas speciālistus programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
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
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887415"
---
# <a name="preferred-maintenance-workers"></a><span data-ttu-id="a1ae0-103">Vēlamie uzturēšanas speciālisti</span><span class="sxs-lookup"><span data-stu-id="a1ae0-103">Preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="a1ae0-104">Jūs varat dot priekšroku uzturēšanas speciālistiem, kuri ir piešķirti, lai izpildītu darba pasūtījumus darba pasūtījuma plānošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-104">You can make a preference regarding which maintenance workers are allocated to complete work orders during work order scheduling.</span></span> <span data-ttu-id="a1ae0-105">Šīs funkcionalitātes lietošana nav obligāta, taču tā var jums palīdzēt izvēlēties kvalificētāko uzturēšanas speciālistu, kurš pabeigtu darbu, pamatojoties uz speciālista prasmēm un kompetenci.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="a1ae0-106">Tādējādi darba pasūtījuma plānošanas laikā tiek izmantots uzstādījums **Vēlamie uzturēšanas speciālisti**, lai noteiktu vai konkrētu uzturēšanas speciālistu vai speciālistu grupu vajadzētu ieplānot darba pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-106">Therefore, during work order scheduling, the setup in **Preferred maintenance workers** is used to determine if a specific maintenance worker or worker group should be scheduled for a work order.</span></span> <span data-ttu-id="a1ae0-107">Ieplānoti tiks vienīgi tie uzturēšanas speciālisti, kuri ir pieejami plānošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-107">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="a1ae0-108">Ja vēlamā uzturēšanas speciālista uzstādījums plānošanas laikā atbilst darba pasūtījumam, taču uzturēšanas speciālists ir piešķirts citiem darbiem, darba pasūtījums tiks ieplānots citam uzturēšanas speciālistam, kurš ir pieejams.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-108">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another, available, maintenance worker.</span></span>

<span data-ttu-id="a1ae0-109">Iekams jūs varat uzstādīt vēlamos uzturēšanas speciālistus, jums ir vispirms jāuzstāda tie uzturēšanas speciālisti un speciālistu grupas, kurām vajadzētu būt pieejamām atlasei.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-109">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups that should be available for selection.</span></span> <span data-ttu-id="a1ae0-110">Skatiet sadaļu [Uzturēšanas speciālisti un speciālistu grupas](../setup-for-objects/workers-and-worker-groups.md), kurā aprakstīts, kā uzstādīt uzturēšanas speciālistus un speciālistu grupas.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-110">Refer to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md) for a description on how to set up maintenance workers and worker groups.</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="a1ae0-111">Vēlamo speciālistu uzstādīšana.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-111">Set up preferred workers</span></span>

<span data-ttu-id="a1ae0-112">Vēlamais uzturēšanas speciālists vai speciālistu grupa var būt saistīti ar konkrētu</span><span class="sxs-lookup"><span data-stu-id="a1ae0-112">A preferred maintenance worker or worker group can be related to a specific</span></span>

- <span data-ttu-id="a1ae0-113">tirdzniecība</span><span class="sxs-lookup"><span data-stu-id="a1ae0-113">trade</span></span>  
- <span data-ttu-id="a1ae0-114">uzturēšanas darba tipa variantu</span><span class="sxs-lookup"><span data-stu-id="a1ae0-114">maintenance job type variant</span></span>  
- <span data-ttu-id="a1ae0-115">uzturēšanas darba tipu</span><span class="sxs-lookup"><span data-stu-id="a1ae0-115">maintenance job type</span></span>  
- <span data-ttu-id="a1ae0-116">uzturēšanas darba tipa kategoriju</span><span class="sxs-lookup"><span data-stu-id="a1ae0-116">maintenance job type category</span></span>  
- <span data-ttu-id="a1ae0-117">aktīvs</span><span class="sxs-lookup"><span data-stu-id="a1ae0-117">asset</span></span>  
- <span data-ttu-id="a1ae0-118">līdzekļa tipu</span><span class="sxs-lookup"><span data-stu-id="a1ae0-118">asset type</span></span>  

<span data-ttu-id="a1ae0-119">vai šo atlašu kombināciju.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-119">or a combination of those selections.</span></span> <span data-ttu-id="a1ae0-120">Jo vairāk atlašu veicat vienam un tam pašam ierakstam, jo konkrētāks būs jūsu iestatījums.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-120">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="a1ae0-121">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Uzstādījums** > **Speciālisti** > **Vēlamie uzturēšanas speciālisti**.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-121">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="a1ae0-122">Noklikšķiniet uz **Jauns**, lai izveidotu jaunu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-122">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="a1ae0-123">Vispirms izveidojiet "noklusējuma" uzturēšanas speciālista vai speciālistu grupas uzstādījumu, kuriem nav atlašu laukos, kas augstāk norādīti aizzīmju sarakstā.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-123">Start by creating a "default" maintenance worker or worker group setup that has no selections in the fields shown in the bullet list above.</span></span> <span data-ttu-id="a1ae0-124">Tas nozīmē, ka jūs varat izdarīt atlasi vienīgi laukos **Vēlamā uzturēšanas speciālistu grupa** vai **Vēlamais uzturēšanas speciālists**.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-124">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="a1ae0-125">Attēlā zemāk ir redzams piemērs pirmajam ierakstam, kurā kā vēlamā uzturēšanas speciālistu grupa ir atlasīta "Pieprasījumi".</span><span class="sxs-lookup"><span data-stu-id="a1ae0-125">In the figure below, you see an example in the first record in which "Requests" is selected as preferred maintenance worker group.</span></span>

>[!NOTE]
><span data-ttu-id="a1ae0-126">Darba pasūtījuma plānošanas laikā tiks izmantots noklusējuma uzstādījums, ja neviena cita konkrētāka kombinācija neatbildīs darba pasūtījuma saturam darba pasūtījuma plānošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-126">The default setup will be used during work order scheduling in case no other, more specific, combination matches the contents of the work order during work order scheduling.</span></span>

4. <span data-ttu-id="a1ae0-127">Atkārtojiet 2. darbību, lai izveidotu jaunu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-127">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="a1ae0-128">Veiciet nepieciešamo atlasi atkarībā no vēlamā speciālista vai speciālistu grupas detalizācijas līmeņa.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-128">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> <span data-ttu-id="a1ae0-129">*Piemērs:* Attēlā zemāk sestais ieraksts - uzturēšanas speciālists Šons Ričardsons - ir atlasīts kā vēlamais speciālists.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-129">*Example:* In the figure below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="a1ae0-130">Viņš tiks automātiski atlasīts darba pasūtījuma plānošanas laikā, kura ietver līdzekli "CH-BP1-03-02" un uzturēšanas darba tipu "Iekārtu novērtējums", ja viņš būs pieejams plānotajā laikā.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-130">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintennace job type "Facility assessment", if he is available at the scheduled time.</span></span>

>[!NOTE]
><span data-ttu-id="a1ae0-131">Parasti, kad darba pasūtījuma plānošanas laikā tiek atlasīts vēlamais uzturēšanas speciālists, programma Asset Management iziet cauri visiem ierakstiem **Vēlamie uzturēšanas speciālisti**, lai pārbaudītu, vai nav iespējamas atbilstības, vienmēr pārbaudot viskonkrētāko kombināciju.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-131">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="a1ae0-132">Tas nozīmē, ka, ja nav atrasta atbilstība, tiek izmantots "noklusējuma" ieraksts ar atlasi vai nu laukā **Vēlamā uzturēšanas speciālistu grupa** vai **Vēlamais uzturēšanas speciālists**.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-132">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>


![1. attēls](media/02-work-order-scheduling.png)

<span data-ttu-id="a1ae0-134">Jūs varat arī uzstādīt atbildīgos uzturēšanas speciālistus, kurus var atlasīt, kad tiek izveidots uzturēšanas pieprasījums vai darba pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-134">You can also set up responsible maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="a1ae0-135">Laukos **Visi darba pasūtījumi** un **Visi uzturēšanas pieprasījumi** jūs varat rediģēt atlasi, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-135">In **All work orders** and **All maintenance requests**, you can edit the selection, if required.</span></span> <span data-ttu-id="a1ae0-136">Papildinformāciju skatiet [Atbildīgie uzturēšanas speciālisti](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="a1ae0-136">Refer to [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md) for more information.</span></span>

<span data-ttu-id="a1ae0-137">Darba pasūtījuma plānošanas laikā, tiek aprēķināti dažādi rezultāti, lai noteiktu, kuriem speciālistiem vajadzētu pabeigt darbus, kas saistīti ar darba pasūtījumu (šie rezultāti tiek uzstādīti, dodoties uz **Līdzekļu pārvaldības parametri** > **Darba pasūtījumu plānošanas** saiti).</span><span class="sxs-lookup"><span data-stu-id="a1ae0-137">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="a1ae0-138">Ja divi vai vairāk vēlamie uzturēšanas speciālisti vai atbildīgie uzturēšanas speciālisti darba pasūtījuma plānošanas laikā saņem vienādu rezultātu, viens speciālists tiek atlasīts nejauši.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-138">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="a1ae0-139">Pretējā gadījumā darba pasūtījuma pabeigšanai vienmēr tiek piešķirts speciālists ar augstāko rezultātu.</span><span class="sxs-lookup"><span data-stu-id="a1ae0-139">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

