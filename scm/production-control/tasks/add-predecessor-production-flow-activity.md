--- 
title: "Pirmstecīgas aktivitātes pievienošana ražošanas plūsmai"
description: "Ražošanas plūsmas versijā visas aktivitātes ir jāsakārto noteiktā secībā."
author: cvocph
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 352c601e9de00d08bf994807d445fe91c8278557
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a><span data-ttu-id="f7bbe-103">Pirmstecīgas aktivitātes pievienošana ražošanas plūsmai</span><span class="sxs-lookup"><span data-stu-id="f7bbe-103">Add a predecessor to a production flow activity</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f7bbe-104">Ražošanas plūsmas versijā visas aktivitātes ir jāsakārto noteiktā secībā.</span><span class="sxs-lookup"><span data-stu-id="f7bbe-104">In a production flow version, all activities must be sequenced.</span></span> <span data-ttu-id="f7bbe-105">Aktivitāte var ietvert vienu vai vairākas pirmstecīgas vai pēctecīgas aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="f7bbe-105">An activity can have one or multiple predecessors or successors.</span></span> 

<span data-ttu-id="f7bbe-106">Šajā procedūrā ir aprakstīts, kā saistīt pirmstecīgu aktivitāti ar aktivitāti.</span><span class="sxs-lookup"><span data-stu-id="f7bbe-106">This procedure shows how to associate a predecessor to an activity.</span></span> 

<span data-ttu-id="f7bbe-107">Lai veiktu šo uzdevumu jums ir nepieciešama ražošanas plūsma, kurai ir pieejama melnraksta versija ar vismaz divām aktivitātēm, kuras var pievienot.</span><span class="sxs-lookup"><span data-stu-id="f7bbe-107">To perform this task, you need a production flow that has the Draft version with at least two activities that can be connected.</span></span> 

<span data-ttu-id="f7bbe-108">Lai uzzinātu vairāk, izlasiet rakstu krājumu “Lean manufacturing ražošanas plūsmas un aktivitātes”.</span><span class="sxs-lookup"><span data-stu-id="f7bbe-108">To learn more, read the white paper "Production flows and activities in lean manufacturing."</span></span>


## <a name="find-the-production-flow-and-version"></a><span data-ttu-id="f7bbe-109">Meklēt ražošanas plūsmu un versiju</span><span class="sxs-lookup"><span data-stu-id="f7bbe-109">Find the production flow and version</span></span>
1. <span data-ttu-id="f7bbe-110">Pārejiet uz sadaļu Ražošanas kontrole > Iestatījumi > Racionālās ražošanas plūsma > Ražošanas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="f7bbe-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="f7bbe-111">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f7bbe-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f7bbe-112">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f7bbe-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f7bbe-113">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f7bbe-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f7bbe-114">Noklikšķiniet uz Aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="f7bbe-114">Click Activities.</span></span>

## <a name="select-an-activity-and-add-a-predecessor"></a><span data-ttu-id="f7bbe-115">Atlasīt aktivitāti un pievienot pirmstecīgu aktivitāti</span><span class="sxs-lookup"><span data-stu-id="f7bbe-115">Select an activity and add a predecessor</span></span>
1. <span data-ttu-id="f7bbe-116">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f7bbe-116">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="f7bbe-117">Noklikšķiniet uz Pievienot pirmstecīgu aktivitāti.</span><span class="sxs-lookup"><span data-stu-id="f7bbe-117">Click Add predecessor.</span></span>
3. <span data-ttu-id="f7bbe-118">Ievadiet vai atlasiet vērtību laukā Aktivitāte.</span><span class="sxs-lookup"><span data-stu-id="f7bbe-118">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="f7bbe-119">Laukā Cikla laika koeficients ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="f7bbe-119">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="f7bbe-120">Aktivitāšu relācijas noklusējuma cikla laika koeficients ir 1.</span><span class="sxs-lookup"><span data-stu-id="f7bbe-120">The default cycle time ratio of an activity relation is 1.</span></span> <span data-ttu-id="f7bbe-121">Tiek pieņemts, ka abas aktivitātes tiek sāktas ar vienādu tempu vai izgatavošanas laiku.</span><span class="sxs-lookup"><span data-stu-id="f7bbe-121">This assumes that both activities run at the same pace or takt time.</span></span> <span data-ttu-id="f7bbe-122">Ja pirmstecīgā aktivitāte tiek izpildīta ātrāk (īsāks izgatavošanas laiks), koeficientam ir jābūt zemākam par 1; ja pirmstecīgā aktivitāte tiek izpildīta ar lēnāk (lielāks izgatavošanas laiks) cikla laika koeficients ir lielāks par 1.</span><span class="sxs-lookup"><span data-stu-id="f7bbe-122">If the predecessor runs at a higher pace (lower takt time), the ratio should be lower than 1, if the predecessor runs at a slower pace (higher takt time) the cycle time ratio is greater than 1.</span></span>  
5. <span data-ttu-id="f7bbe-123">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f7bbe-123">Click OK.</span></span>


