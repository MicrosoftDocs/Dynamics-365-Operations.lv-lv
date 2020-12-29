---
title: Pirmstecīgas aktivitātes pievienošana ražošanas plūsmai
description: Ražošanas plūsmas versijā visas aktivitātes ir jāsakārto noteiktā secībā.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c39cef1174439b42a072bd7fc1ac29ef31ecf864
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432510"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a><span data-ttu-id="febb7-103">Pirmstecīgas aktivitātes pievienošana ražošanas plūsmai</span><span class="sxs-lookup"><span data-stu-id="febb7-103">Add a predecessor to a production flow activity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="febb7-104">Ražošanas plūsmas versijā visas aktivitātes ir jāsakārto noteiktā secībā.</span><span class="sxs-lookup"><span data-stu-id="febb7-104">In a production flow version, all activities must be sequenced.</span></span> <span data-ttu-id="febb7-105">Aktivitāte var ietvert vienu vai vairākas pirmstecīgas vai pēctecīgas aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="febb7-105">An activity can have one or multiple predecessors or successors.</span></span> 

<span data-ttu-id="febb7-106">Šajā procedūrā ir aprakstīts, kā saistīt pirmstecīgu aktivitāti ar aktivitāti.</span><span class="sxs-lookup"><span data-stu-id="febb7-106">This procedure shows how to associate a predecessor to an activity.</span></span> 

<span data-ttu-id="febb7-107">Lai veiktu šo uzdevumu jums ir nepieciešama ražošanas plūsma, kurai ir pieejama melnraksta versija ar vismaz divām aktivitātēm, kuras var pievienot.</span><span class="sxs-lookup"><span data-stu-id="febb7-107">To perform this task, you need a production flow that has the Draft version with at least two activities that can be connected.</span></span> 

<span data-ttu-id="febb7-108">Lai uzzinātu vairāk, izlasiet rakstu krājumu “Lean manufacturing ražošanas plūsmas un aktivitātes”.</span><span class="sxs-lookup"><span data-stu-id="febb7-108">To learn more, read the white paper "Production flows and activities in lean manufacturing."</span></span>


## <a name="find-the-production-flow-and-version"></a><span data-ttu-id="febb7-109">Meklēt ražošanas plūsmu un versiju</span><span class="sxs-lookup"><span data-stu-id="febb7-109">Find the production flow and version</span></span>
1. <span data-ttu-id="febb7-110">Pārejiet uz sadaļu Ražošanas kontrole > Iestatījumi > Racionālās ražošanas plūsma > Ražošanas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="febb7-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="febb7-111">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="febb7-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="febb7-112">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="febb7-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="febb7-113">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="febb7-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="febb7-114">Noklikšķiniet uz Aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="febb7-114">Click Activities.</span></span>

## <a name="select-an-activity-and-add-a-predecessor"></a><span data-ttu-id="febb7-115">Atlasīt aktivitāti un pievienot pirmstecīgu aktivitāti</span><span class="sxs-lookup"><span data-stu-id="febb7-115">Select an activity and add a predecessor</span></span>
1. <span data-ttu-id="febb7-116">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="febb7-116">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="febb7-117">Noklikšķiniet uz Pievienot pirmstecīgu aktivitāti.</span><span class="sxs-lookup"><span data-stu-id="febb7-117">Click Add predecessor.</span></span>
3. <span data-ttu-id="febb7-118">Ievadiet vai atlasiet vērtību laukā Aktivitāte.</span><span class="sxs-lookup"><span data-stu-id="febb7-118">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="febb7-119">Laukā Cikla laika koeficients ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="febb7-119">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="febb7-120">Aktivitāšu relācijas noklusējuma cikla laika koeficients ir 1.</span><span class="sxs-lookup"><span data-stu-id="febb7-120">The default cycle time ratio of an activity relation is 1.</span></span> <span data-ttu-id="febb7-121">Tiek pieņemts, ka abas aktivitātes tiek sāktas ar vienādu tempu vai izgatavošanas laiku.</span><span class="sxs-lookup"><span data-stu-id="febb7-121">This assumes that both activities run at the same pace or takt time.</span></span> <span data-ttu-id="febb7-122">Ja pirmstecīgā aktivitāte tiek izpildīta ātrāk (īsāks izgatavošanas laiks), koeficientam ir jābūt zemākam par 1; ja pirmstecīgā aktivitāte tiek izpildīta ar lēnāk (lielāks izgatavošanas laiks) cikla laika koeficients ir lielāks par 1.</span><span class="sxs-lookup"><span data-stu-id="febb7-122">If the predecessor runs at a higher pace (lower takt time), the ratio should be lower than 1, if the predecessor runs at a slower pace (higher takt time) the cycle time ratio is greater than 1.</span></span>  
5. <span data-ttu-id="febb7-123">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="febb7-123">Click OK.</span></span>

