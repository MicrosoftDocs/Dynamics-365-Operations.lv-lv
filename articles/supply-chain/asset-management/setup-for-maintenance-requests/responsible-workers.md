---
title: Atbildīgie uzturēšanas speciālisti
description: Šajā tēmā izskaidrots, kā iestatīt uzturēšanas pieprasījumu veidus Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkerResponsible
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1330aa04a57809ff34dcca9791f8fb0a93c8d71
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808452"
---
# <a name="responsible-maintenance-workers"></a><span data-ttu-id="b2fc1-103">Atbildīgie uzturēšanas speciālisti</span><span class="sxs-lookup"><span data-stu-id="b2fc1-103">Responsible maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b2fc1-104">Atbildīgi uzturēšanas speciālisti var būt saistīti ar līdzekļu veidiem, līdzekļiem, funkcionālajiem novietojumiem, uzturēšanas darbu veidu kategorijām, uzturēšanas darbu veidiem, uzturēšanas darbu veida variantiem un tirdzniecību.</span><span class="sxs-lookup"><span data-stu-id="b2fc1-104">Responsible maintenance workers can be related to asset types, assets, functional locations, maintenance job type categories, maintenance job types, maintenance job type variants, and trades.</span></span> <span data-ttu-id="b2fc1-105">Tos var izmantot darba pasūtījumos un uzturēšanas pieprasījumos, lai norādītu prioritāti uzturēšanas speciālistiem, kuriem jābūt atbildīgiem par darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="b2fc1-105">They can be used on work orders and maintenance requests to indicate a preference about the maintenance workers who should be responsible for a work order.</span></span> <span data-ttu-id="b2fc1-106">(Tomēr šie uzturēšanas speciālisti ne vienmēr ir tie paši darbinieki, kuri ir ieplānoti darba pasūtījuma veikšanai.) Šīs funkcionalitātes izmantošana nav obligāta.</span><span class="sxs-lookup"><span data-stu-id="b2fc1-106">(However, those maintenance workers aren't necessarily the same workers who are scheduled to carry out the work order.) Use of this functionality is optional.</span></span> <span data-ttu-id="b2fc1-107">Piemēram, to var izmantot, lai atlasītu atbildīgos darbiniekus vai darbinieku grupas konkrētiem darba veidiem vai darba apgabaliem.</span><span class="sxs-lookup"><span data-stu-id="b2fc1-107">For example, it can be used to select responsible workers or worker groups for specific work types or work areas.</span></span>

<span data-ttu-id="b2fc1-108">Darba pasūtījuma dzīves cikla vai uzturēšanas pieprasījuma dzīves ciklā laikā atbildīgos uzturēšanas speciālistus var mainīt vai atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="b2fc1-108">During a work order lifecycle or a maintenance request lifecycle, responsible maintenance workers can be changed or updated.</span></span> <span data-ttu-id="b2fc1-109">Šī maiņa vai atjaunināšana var būt saistīta, piemēram, ar izmaiņām uzturēšanas pieprasījuma dzīves cikla stāvoklī vai darba pasūtījuma dzīves cikla stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="b2fc1-109">This change or update might be related to, for example, a change in the maintenance request lifecycle state or the work order lifecycle state.</span></span>

<span data-ttu-id="b2fc1-110">Darba pasūtījuma plānošanas laikā iestatīšana lapā **Atbildīgie uzturēšanas speciālisti** *netiek* izmantota.</span><span class="sxs-lookup"><span data-stu-id="b2fc1-110">The setup on the **Responsible maintenance workers** page is *not* used during work order scheduling.</span></span>

> [!NOTE]
> <span data-ttu-id="b2fc1-111">Līdzekļu pārvaldībā var arī iestatīt *vēlamus* uzturēšanas speciālistus, kuri var tikt piešķirti darba pasūtījumiem darba pasūtījumu plānošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="b2fc1-111">In Asset Management, you can also set up *preferred* maintenance workers who might be allocated to work orders during work order scheduling.</span></span>

<span data-ttu-id="b2fc1-112">Pirms varat iestatīt atbildīgos uzturēšanas speciālistus, ir jāiestata darbinieki un uzturēšanas speciālistu grupas, kam jābūt pieejamiem atlasei.</span><span class="sxs-lookup"><span data-stu-id="b2fc1-112">Before you can set up responsible maintenance workers, you must set up the workers and maintenance worker groups that should be available for selection.</span></span> <span data-ttu-id="b2fc1-113">Informāciju par to, kā iestatīt darbiniekus un uzturēšanas speciālistu grupas, skatiet nodaļā [Uzturēšanas speciālisti un speciālistu grupas](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="b2fc1-113">For information about how to set up workers and maintenance worker groups, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-responsible-maintenance-workers"></a><span data-ttu-id="b2fc1-114">Iestatīt atbildīgos uzturēšanas speciālistus</span><span class="sxs-lookup"><span data-stu-id="b2fc1-114">Set up responsible maintenance workers</span></span>

1. <span data-ttu-id="b2fc1-115">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Speciālisti** \> **Atbildīgie uzturēšanas speciālisti**.</span><span class="sxs-lookup"><span data-stu-id="b2fc1-115">Select **Asset management** \> **Setup** \> **Workers** \> **Responsible maintenance workers**.</span></span>
2. <span data-ttu-id="b2fc1-116">Atlasiet **Jauns**, lai izveidotu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b2fc1-116">Select **New** to create a record.</span></span>
3. <span data-ttu-id="b2fc1-117">Vispirms izveidojiet noklusējuma atbildīgo uzturēšanas speciālistu vai atbildīgo uzturēšanas speciālistu grupas iestatījumu, kur iestatāt tikai lauku **Atbildīgo uzturēšanas speciālistu grupa** un/vai lauku **Atbildīgais darbinieks**.</span><span class="sxs-lookup"><span data-stu-id="b2fc1-117">First create a default responsible maintenance worker or responsible maintenance worker group setup, where you set only the **Responsible maintenance worker group** field and/or the **Responsible worker** field.</span></span> <span data-ttu-id="b2fc1-118">Atlikušos laukus atstājiet tukšus.</span><span class="sxs-lookup"><span data-stu-id="b2fc1-118">Leave the remaining fields blank.</span></span> <span data-ttu-id="b2fc1-119">Šis noklusējuma iestatījums tiks izmantots darba pasūtījuma plānošanā, ja neviena cita specifiska kombinācija neatbilst darba pasūtījuma saturam.</span><span class="sxs-lookup"><span data-stu-id="b2fc1-119">This default setup will be used during work order scheduling if no other, more specific combination matches the contents of the work order.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b2fc1-120">Uzturēšanas pieprasījuma izveides laikā, kad atbildīgais uzturēšanas speciālists vai atbildīgo uzturēšanas speciālistu grupa tiek darīta pieejama atlasei lapā **Visi uzturēšanas pieprasījumi**, Līdzekļu pārvaldība iziet cauri visiem atbildīgo uzturēšanas speciālistu ierakstiem, lai pārbaudītu iespējamu atbilstību.</span><span class="sxs-lookup"><span data-stu-id="b2fc1-120">During creation of a maintenance request, when a responsible maintenance worker or responsible maintenance worker group is made available for selection on the **All maintenance requests** page, Asset Management goes through all responsible maintenance worker records to check for a possible match.</span></span> <span data-ttu-id="b2fc1-121">Tā vienmēr vispirms pārbauda visraksturīgāko kombināciju.</span><span class="sxs-lookup"><span data-stu-id="b2fc1-121">It always checks the most specific combination first.</span></span> <span data-ttu-id="b2fc1-122">Citiem vārdiem sakot, Līdzekļu pārvaldība vispirms pārbauda atbilstību laukam **Tirdzniecība**.</span><span class="sxs-lookup"><span data-stu-id="b2fc1-122">In other words, Asset Management first checks for a match for the **Trade** field.</span></span> <span data-ttu-id="b2fc1-123">Ja atbilstība netiek atrasta, tā meklē atbilstību laukam **Uzturēšanas darba veida variants**.</span><span class="sxs-lookup"><span data-stu-id="b2fc1-123">If no match is found, it checks for a match for the **Maintenance job type variant** field.</span></span> <span data-ttu-id="b2fc1-124">Ja atbilstība netiek atrasta, tā meklē atbilstību laukam **Uzturēšanas darba veids** un tā tālāk.</span><span class="sxs-lookup"><span data-stu-id="b2fc1-124">If no match is found, it checks for a match for the **Maintenance job type** field, and so on.</span></span> <span data-ttu-id="b2fc1-125">Kā varat redzēt lapas izkārtojumā, šī uzvedība nozīmē, ka, lai atrastu visspecifiskāko kombināciju, Līdzekļu pārvaldība pārbauda katru ierakstu no labās puses uz kreiso, meklējot atbilstību (vispirms **Tirdzniecība**, tad **Uzturēšana darba veida variants**, tad **Uzturēšanas darba veids**, tad **uzturēšanas darba veidu kategorija**, tad **Funkcionālais novietojums**, tad **Līdzeklis** un visbeidzot **Līdzekļu veids**).</span><span class="sxs-lookup"><span data-stu-id="b2fc1-125">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match (first **Trade**, then **Maintenance job type variant**, then **Maintenance job type**, then **Maintenance job type category**, then **Functional location**, then **Asset**, and finally **Asset type**).</span></span> <span data-ttu-id="b2fc1-126">Ja atbilstība netiek atrasta, tiek izmantots "noklusējuma" ieraksts, kam nav atlases iespēju šajos septiņos laukos.</span><span class="sxs-lookup"><span data-stu-id="b2fc1-126">If no match is found, the default record that has no selections in those seven fields is used.</span></span>

<span data-ttu-id="b2fc1-127">Nākamajā attēlā ir parādīts sarakstu lapas **Atbildīgie uzturēšanas speciālisti** piemērs.</span><span class="sxs-lookup"><span data-stu-id="b2fc1-127">The following illustration shows an example of the **Responsible maintenance workers** page.</span></span>

![Atbildīgas uzturēšanas nodarbināto lapa](media/08-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]