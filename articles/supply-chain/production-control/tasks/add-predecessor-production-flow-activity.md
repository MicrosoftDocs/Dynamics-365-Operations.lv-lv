---
title: Pirmstecīgas aktivitātes pievienošana ražošanas plūsmai
description: Ražošanas plūsmas versijā visas aktivitātes ir jāsakārto noteiktā secībā.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 346dca110fde9ff7600f3e4606529c27289dfc97
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838779"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a><span data-ttu-id="c17e0-103">Pirmstecīgas aktivitātes pievienošana ražošanas plūsmai</span><span class="sxs-lookup"><span data-stu-id="c17e0-103">Add a predecessor to a production flow activity</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c17e0-104">Ražošanas plūsmas versijā visas aktivitātes ir jāsakārto noteiktā secībā.</span><span class="sxs-lookup"><span data-stu-id="c17e0-104">In a production flow version, all activities must be sequenced.</span></span> <span data-ttu-id="c17e0-105">Aktivitāte var ietvert vienu vai vairākas pirmstecīgas vai pēctecīgas aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="c17e0-105">An activity can have one or multiple predecessors or successors.</span></span> 

<span data-ttu-id="c17e0-106">Šajā procedūrā ir aprakstīts, kā saistīt pirmstecīgu aktivitāti ar aktivitāti.</span><span class="sxs-lookup"><span data-stu-id="c17e0-106">This procedure shows how to associate a predecessor to an activity.</span></span> 

<span data-ttu-id="c17e0-107">Lai veiktu šo uzdevumu jums ir nepieciešama ražošanas plūsma, kurai ir pieejama melnraksta versija ar vismaz divām aktivitātēm, kuras var pievienot.</span><span class="sxs-lookup"><span data-stu-id="c17e0-107">To perform this task, you need a production flow that has the Draft version with at least two activities that can be connected.</span></span> 

<span data-ttu-id="c17e0-108">Lai uzzinātu vairāk, izlasiet rakstu krājumu “Lean manufacturing ražošanas plūsmas un aktivitātes”.</span><span class="sxs-lookup"><span data-stu-id="c17e0-108">To learn more, read the white paper "Production flows and activities in lean manufacturing."</span></span>


## <a name="find-the-production-flow-and-version"></a><span data-ttu-id="c17e0-109">Meklēt ražošanas plūsmu un versiju</span><span class="sxs-lookup"><span data-stu-id="c17e0-109">Find the production flow and version</span></span>
1. <span data-ttu-id="c17e0-110">Pārejiet uz sadaļu Ražošanas kontrole > Iestatījumi > Racionālās ražošanas plūsma > Ražošanas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="c17e0-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="c17e0-111">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c17e0-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c17e0-112">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c17e0-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c17e0-113">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c17e0-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c17e0-114">Noklikšķiniet uz Aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="c17e0-114">Click Activities.</span></span>

## <a name="select-an-activity-and-add-a-predecessor"></a><span data-ttu-id="c17e0-115">Atlasīt aktivitāti un pievienot pirmstecīgu aktivitāti</span><span class="sxs-lookup"><span data-stu-id="c17e0-115">Select an activity and add a predecessor</span></span>
1. <span data-ttu-id="c17e0-116">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c17e0-116">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="c17e0-117">Noklikšķiniet uz Pievienot pirmstecīgu aktivitāti.</span><span class="sxs-lookup"><span data-stu-id="c17e0-117">Click Add predecessor.</span></span>
3. <span data-ttu-id="c17e0-118">Ievadiet vai atlasiet vērtību laukā Aktivitāte.</span><span class="sxs-lookup"><span data-stu-id="c17e0-118">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="c17e0-119">Laukā Cikla laika koeficients ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="c17e0-119">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="c17e0-120">Aktivitāšu relācijas noklusējuma cikla laika koeficients ir 1.</span><span class="sxs-lookup"><span data-stu-id="c17e0-120">The default cycle time ratio of an activity relation is 1.</span></span> <span data-ttu-id="c17e0-121">Tiek pieņemts, ka abas aktivitātes tiek sāktas ar vienādu tempu vai izgatavošanas laiku.</span><span class="sxs-lookup"><span data-stu-id="c17e0-121">This assumes that both activities run at the same pace or takt time.</span></span> <span data-ttu-id="c17e0-122">Ja pirmstecīgā aktivitāte tiek izpildīta ātrāk (īsāks izgatavošanas laiks), koeficientam ir jābūt zemākam par 1; ja pirmstecīgā aktivitāte tiek izpildīta ar lēnāk (lielāks izgatavošanas laiks) cikla laika koeficients ir lielāks par 1.</span><span class="sxs-lookup"><span data-stu-id="c17e0-122">If the predecessor runs at a higher pace (lower takt time), the ratio should be lower than 1, if the predecessor runs at a slower pace (higher takt time) the cycle time ratio is greater than 1.</span></span>  
5. <span data-ttu-id="c17e0-123">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="c17e0-123">Click OK.</span></span>

