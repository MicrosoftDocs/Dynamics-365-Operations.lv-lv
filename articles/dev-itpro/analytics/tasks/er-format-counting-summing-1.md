--- 
title: "Inventarizācijas un summēšanas formāta izveide"
description: "Tālāk aprakstītajos soļos ir izskaidrots, kā sistēmas lietotājs, kam ir piešķirta administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektronisko pārskatu sagatavošanas (ER) formātu, lai veiktu uzskaiti un summēšanu, izmantojot jau izveidotās teksta izvades datus."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c20f2190e6480b6586d8102c489633d748d85a95
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---
# <a name="create-format-for-counting-and-summing"></a><span data-ttu-id="103b8-103">Inventarizācijas un summēšanas formāta izveide</span><span class="sxs-lookup"><span data-stu-id="103b8-103">Create format for counting and summing</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="103b8-104">Tālāk aprakstītajos soļos ir izskaidrots, kā sistēmas lietotājs, kam ir piešķirta administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektronisko pārskatu sagatavošanas (ER) formātu, lai veiktu uzskaiti un summēšanu, izmantojot jau izveidotās teksta izvades datus.</span><span class="sxs-lookup"><span data-stu-id="103b8-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="103b8-105">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="103b8-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="103b8-106">Lai veiktu šīs darbības, vispirms veiciet "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu" procedūras darbības.</span><span class="sxs-lookup"><span data-stu-id="103b8-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="103b8-107">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="103b8-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="103b8-108">Iegūt piekļuvi korporācijas Microsoft nodrošināto konfigurāciju sarakstam</span><span class="sxs-lookup"><span data-stu-id="103b8-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="103b8-109">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="103b8-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="103b8-110">Pārliecinieties, vai "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="103b8-110">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="103b8-111">ir pieejams un atzīmēts kā aktīvs.</span><span class="sxs-lookup"><span data-stu-id="103b8-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="103b8-112">Atlasiet Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="103b8-112">Select the “Litware, Inc.”</span></span> <span data-ttu-id="103b8-113">nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="103b8-113">provider.</span></span>
3. <span data-ttu-id="103b8-114">Noklikšķiniet uz Repozitoriji.</span><span class="sxs-lookup"><span data-stu-id="103b8-114">Click Repositories.</span></span>
    * <span data-ttu-id="103b8-115">Ja tipa “Operācijas resursi” repozitorijs jau pastāv, izlaidiet pašreizējā apakšuzdevuma pārējos soļus.</span><span class="sxs-lookup"><span data-stu-id="103b8-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="103b8-116">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="103b8-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="103b8-117">Laukā Konfigurācijas repozitorija tips ievadiet Operācijas resursi.</span><span class="sxs-lookup"><span data-stu-id="103b8-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="103b8-118">Noklikšķiniet uz Izveidot repozitoriju.</span><span class="sxs-lookup"><span data-stu-id="103b8-118">Click Create repository.</span></span>
7. <span data-ttu-id="103b8-119">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="103b8-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="103b8-120">Iegūt piekļuvi korporācijas Microsoft nodrošinātajām Intrastat konfigurācijām</span><span class="sxs-lookup"><span data-stu-id="103b8-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="103b8-121">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="103b8-121">Click Open.</span></span>
2. <span data-ttu-id="103b8-122">Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="103b8-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="103b8-123">Noklikšķiniet uz Importēt.</span><span class="sxs-lookup"><span data-stu-id="103b8-123">Click Import.</span></span>
    * <span data-ttu-id="103b8-124">Noklikšķiniet uz Atlasītās konfigurācijas versijas 1.1 importēšana.</span><span class="sxs-lookup"><span data-stu-id="103b8-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="103b8-125">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="103b8-125">Click Yes.</span></span>
5. <span data-ttu-id="103b8-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="103b8-126">Close the page.</span></span>
6. <span data-ttu-id="103b8-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="103b8-127">Close the page.</span></span>
7. <span data-ttu-id="103b8-128">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="103b8-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="103b8-129">Kokā struktūrā izvērsiet 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="103b8-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="103b8-130">Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="103b8-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>


