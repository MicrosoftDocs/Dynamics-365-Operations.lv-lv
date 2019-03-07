---
title: Ražošanas plūsmas versijas deaktivizēšana
description: Kad aktīva ražošanas plūsmas versija vairs nav vajadzīga, to var deaktivizēt.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 091cafd02bd568323e586373fc8b0f983afee343
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "340756"
---
# <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="444ba-103">Ražošanas plūsmas versijas deaktivizēšana</span><span class="sxs-lookup"><span data-stu-id="444ba-103">Deactivate a production flow version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="444ba-104">Kad aktīva ražošanas plūsmas versija vairs nav vajadzīga, to var deaktivizēt.</span><span class="sxs-lookup"><span data-stu-id="444ba-104">When an active production flow version is no longer needed, it can be deactivated.</span></span> <span data-ttu-id="444ba-105">Šo opciju var izmantot tikai, ja visi kanban nosacījumi un darbības ir beigušās, un netiks aktivizētas atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="444ba-105">You should only use this option if all kanban rules and activities have ended and will not be activated again.</span></span> <span data-ttu-id="444ba-106">Ņemiet vērā, ka visu kanban noteikumu beigu datumi, kas attiecas uz šo ražošanas plūsmas versiju, tiks atjaunināti ar pašreizējo datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="444ba-106">Note that the expiry date of all kanban rules related to this production flow version will be updated with the current date and time.</span></span> 

<span data-ttu-id="444ba-107">Lai modificētu aktīvo ražošanas plūsmas versiju, jāapsver iespēju iestatīt beigu datumu aktīvajai versijai, un izveidot jaunu versiju.</span><span class="sxs-lookup"><span data-stu-id="444ba-107">To modify an active production flow version, consider setting an expiry date for the active version and create a new version.</span></span> <span data-ttu-id="444ba-108">Tas ļaus jums turpināt ražošanas darbības, vienlaikus gatavojot jauno versiju un saistītos kanban noteikumus.</span><span class="sxs-lookup"><span data-stu-id="444ba-108">This will allow you to continue your production operations while preparing the new version and related kanban rules.</span></span> 

<span data-ttu-id="444ba-109">Lai izbeigtu aktīvas ražošanas plūsmas versiju, jums nepieciešams iestatīt beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="444ba-109">To expire an active production flow version, you need to set an expiry date.</span></span> <span data-ttu-id="444ba-110">Šajā ziņā deaktivizēšana būs vairāk kā izņēmums, nevis nosacījums.</span><span class="sxs-lookup"><span data-stu-id="444ba-110">In that sense, deactivation is more like an exception than a rule.</span></span> 

<span data-ttu-id="444ba-111">Šai procedūrai ir nepieciešama ražošanas plūsma ar versiju, kas var tikt deaktivizēta.</span><span class="sxs-lookup"><span data-stu-id="444ba-111">For this procedure you need a production flow with a version that can be deactivated.</span></span> <span data-ttu-id="444ba-112">Nemēģiniet šo ražošanas vidē, ja neesat 100% pārliecināts, ka versija ir pilnībā novecojusi.</span><span class="sxs-lookup"><span data-stu-id="444ba-112">Do not try this in a production environment unless you are 100% positive that the version is fully obsolete.</span></span>


## <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="444ba-113">Ražošanas plūsmas versijas deaktivizēšana</span><span class="sxs-lookup"><span data-stu-id="444ba-113">Deactivate a production flow version</span></span>
1. <span data-ttu-id="444ba-114">Pārejiet uz sadaļu Ražošanas kontrole > Iestatījumi > Racionālās ražošanas plūsma > Ražošanas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="444ba-114">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="444ba-115">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="444ba-115">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="444ba-116">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="444ba-116">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="444ba-117">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="444ba-117">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="444ba-118">Noklikšķiniet uz Deaktivizēt.</span><span class="sxs-lookup"><span data-stu-id="444ba-118">Click Deactivate.</span></span>
    * <span data-ttu-id="444ba-119">Neturpiniet, ja neesat 100% pārliecināts, ka šī ražošanas plūsmas versija ir novecojusi.</span><span class="sxs-lookup"><span data-stu-id="444ba-119">Do not proceed if you are not 100% positive that this production flow version is obsolete.</span></span> <span data-ttu-id="444ba-120">Noklikšķinot uz Ok (Labi), beidzas visi aktīvie kanban nosacījumi, un tiek nekavējoties pārtrauktas visas ražošanas un papildināšanas darbības ar šo ražošanas plūsmas versiju.</span><span class="sxs-lookup"><span data-stu-id="444ba-120">Clicking Ok will expire all active kanban rules and put an immediate stop to all production and replenishment activities of this production flow version.</span></span>  
6. <span data-ttu-id="444ba-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="444ba-121">Click OK.</span></span>

