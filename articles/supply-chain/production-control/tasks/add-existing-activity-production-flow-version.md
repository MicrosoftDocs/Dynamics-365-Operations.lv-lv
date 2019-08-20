---
title: Esošas aktivitātes pievienošana ražošanas plūsmas versijai
description: Izveidojot jaunu ražošanas plūsmu versijas, varat izvēlēties, vai jaunajai versijai pievienot aktivitātes, kas izveidots vecākām versijām.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityAddExisting, PlanActivityAddExistingLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 315a82ce3502164fcf7813e866fb3dc1806d03d7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843965"
---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a><span data-ttu-id="b724c-103">Esošas aktivitātes pievienošana ražošanas plūsmas versijai</span><span class="sxs-lookup"><span data-stu-id="b724c-103">Add an existing activity to a production flow version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b724c-104">Izveidojot jaunu ražošanas plūsmu versijas, varat izvēlēties, vai jaunajai versijai pievienot aktivitātes, kas izveidots vecākām versijām.</span><span class="sxs-lookup"><span data-stu-id="b724c-104">When creating new versions of production flows, you can choose to add activities created for the older versions, to the new version.</span></span> <span data-ttu-id="b724c-105">Šajā procedūrā ir aprakstīts, kā izveidot esošās ražošanas plūsmas jaunu versiju, nekopējot aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="b724c-105">This procedure shows how a new version is created for an existing production flow, without copying the activities.</span></span> <span data-ttu-id="b724c-106">Nākamajā darbībā esoša aktivitāte tiek pievienota jaunajai versijai.</span><span class="sxs-lookup"><span data-stu-id="b724c-106">In the next step, an existing activity is added to the new version.</span></span> 

<span data-ttu-id="b724c-107">Lai varētu izpildīt šo uzdevumu, ir nepieciešama ražošanas plūsma ar jau izveidotu versiju un aktivitātēm.</span><span class="sxs-lookup"><span data-stu-id="b724c-107">This task requires production flow with version and activities already created.</span></span>


## <a name="create-a-new-production-flow-version"></a><span data-ttu-id="b724c-108">Izveidojiet jaunu ražošanas plūsmas versiju</span><span class="sxs-lookup"><span data-stu-id="b724c-108">Create a new production flow version</span></span>
1. <span data-ttu-id="b724c-109">Pārejiet uz sadaļu Ražošanas kontrole > Iestatījumi > Racionālās ražošanas plūsma > Ražošanas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="b724c-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="b724c-110">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b724c-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b724c-111">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b724c-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b724c-112">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="b724c-112">Click Edit.</span></span>
5. <span data-ttu-id="b724c-113">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="b724c-113">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="b724c-114">Laukā Beigu datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="b724c-114">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="b724c-115">Ņemiet vērā, ka pirms jaunas ražošanas plūsmas versijas izveidošanas ir jāpārbauda aktīvās versijas derīguma termiņa beigu datums un laiks.</span><span class="sxs-lookup"><span data-stu-id="b724c-115">Note that before you create a new production flow version, make sure to check the expiration date and time of the active version.</span></span> <span data-ttu-id="b724c-116">Jaunā versija tiks izveidota ar spēkā stāšanās datumu, kas ir saistīts ar atlasītas versijas derīguma termiņa beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="b724c-116">The new version will be created with an effective start date, which connects to the expiry date of the selected version.</span></span>  
7. <span data-ttu-id="b724c-117">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b724c-117">Click Add.</span></span>
8. <span data-ttu-id="b724c-118">Laukā Kopēt no versijas atlasiet Nē.</span><span class="sxs-lookup"><span data-stu-id="b724c-118">Select No in the Copy from version field.</span></span>
    * <span data-ttu-id="b724c-119">Ja lielākā daļa kopētās versijas aktivitāšu tiks aizstātas ar jaunām aktivitātēm, atlasiet Nē, lai sāktu darbu, izmantojot tukšu versiju.</span><span class="sxs-lookup"><span data-stu-id="b724c-119">Select No to start with an empty version if most of the activities of the copied version will be replaced by new activities.</span></span> <span data-ttu-id="b724c-120">Aktivitāšu veidlapā manuāli pievienojiet neizmainītās aktivitātes funkcijai Pievienot esošo.</span><span class="sxs-lookup"><span data-stu-id="b724c-120">Add the unchanged activities to the Add existing function in the activity form manually.</span></span>  
9. <span data-ttu-id="b724c-121">Laukā Dublēt Kanban nosacījumus atlasiet Nē.</span><span class="sxs-lookup"><span data-stu-id="b724c-121">Select No in the Duplicate kanban rules field.</span></span>
    * <span data-ttu-id="b724c-122">Ja aktivitātes jaunajā versijā netiek kopētas, Kanban nosacījumus nevar kopēt jebkurā jaunās versijas izveides brīdī.</span><span class="sxs-lookup"><span data-stu-id="b724c-122">When the activities are not copied to the new version, it is not possible to copy the kanban rules at the time of creation of the new version.</span></span>   <span data-ttu-id="b724c-123">Tā vietā Kanban nosacījumu formā vēlāk var izmantot aizstāšanas Kanban funkcijas izveidi, lai aizstātu iepriekšējās ražošanas plūsmas versijas Kanban nosacījumus ar Kanban nosacījumiem, izmantojot jaunās versijas aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="b724c-123">Instead you will use the create replacement kanban function later in the kanban rule form, to replace kanban rules of the old production flow version with kanban rules using the activities of the new version.</span></span>  
10. <span data-ttu-id="b724c-124">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="b724c-124">Click OK.</span></span>
11. <span data-ttu-id="b724c-125">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b724c-125">In the list, find and select the desired record.</span></span>

## <a name="add-an-existing-activity"></a><span data-ttu-id="b724c-126">Pievienot esošu aktivitāti</span><span class="sxs-lookup"><span data-stu-id="b724c-126">Add an existing activity</span></span>
1. <span data-ttu-id="b724c-127">Noklikšķiniet uz Aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="b724c-127">Click Activities.</span></span>
2. <span data-ttu-id="b724c-128">Noklikšķiniet uz Pievienot esošu, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b724c-128">Click Add existing to open the drop dialog.</span></span>
    * <span data-ttu-id="b724c-129">Atrodiet un atlasiet esošu aktivitāti, kas jāpievieno jaunajai ražošanas plūsmas versijai.</span><span class="sxs-lookup"><span data-stu-id="b724c-129">Find and select an existing activity to be added to the new production flow version.</span></span>  <span data-ttu-id="b724c-130">Ņemiet vērā, ka sarakstā ir redzamas visas aktivitātes, kas ir izveidotas plūsmas visu iepriekšējo versiju konkrētajai ražošanas plūsmai.</span><span class="sxs-lookup"><span data-stu-id="b724c-130">Note that the list shows all activities that have been created for this production flow for all previous versions of the flow.</span></span>  
3. <span data-ttu-id="b724c-131">Ievadiet vai atlasiet vērtību laukā Aktivitāte.</span><span class="sxs-lookup"><span data-stu-id="b724c-131">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="b724c-132">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="b724c-132">Click OK.</span></span>

