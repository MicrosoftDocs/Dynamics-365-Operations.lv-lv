---
title: ER formāta konfigurēšana, lai veiktu uzskaiti un summēšanu (1. daļa. Formāta izveide)
description: Tālāk aprakstītajos soļos ir izskaidrots, kā sistēmas lietotājs, kam ir piešķirta administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektronisko pārskatu sagatavošanas (ER) formātu, lai veiktu uzskaiti un summēšanu, izmantojot jau izveidotās teksta izvades datus.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e85109cd0448383ba231cbec1bdeeb9dcd2db805
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550790"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="8ecce-103">ER formāta konfigurēšana, lai veiktu uzskaiti un summēšanu (1. daļa. Formāta izveide)</span><span class="sxs-lookup"><span data-stu-id="8ecce-103">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8ecce-104">Tālāk aprakstītajos soļos ir izskaidrots, kā sistēmas lietotājs, kam ir piešķirta administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektronisko pārskatu sagatavošanas (ER) formātu, lai veiktu uzskaiti un summēšanu, izmantojot jau izveidotās teksta izvades datus.</span><span class="sxs-lookup"><span data-stu-id="8ecce-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="8ecce-105">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="8ecce-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="8ecce-106">Lai veiktu šīs darbības, vispirms veiciet "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu" procedūras darbības.</span><span class="sxs-lookup"><span data-stu-id="8ecce-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="8ecce-107">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="8ecce-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="8ecce-108">Iegūt piekļuvi korporācijas Microsoft nodrošināto konfigurāciju sarakstam</span><span class="sxs-lookup"><span data-stu-id="8ecce-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="8ecce-109">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="8ecce-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="8ecce-110">Pārliecinieties, vai "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="8ecce-110">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="8ecce-111">ir pieejams un atzīmēts kā aktīvs.</span><span class="sxs-lookup"><span data-stu-id="8ecce-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="8ecce-112">Atlasiet Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="8ecce-112">Select the “Litware, Inc.”</span></span> <span data-ttu-id="8ecce-113">nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="8ecce-113">provider.</span></span>
3. <span data-ttu-id="8ecce-114">Noklikšķiniet uz Repozitoriji.</span><span class="sxs-lookup"><span data-stu-id="8ecce-114">Click Repositories.</span></span>
    * <span data-ttu-id="8ecce-115">Ja tipa “Operācijas resursi” repozitorijs jau pastāv, izlaidiet pašreizējā apakšuzdevuma pārējos soļus.</span><span class="sxs-lookup"><span data-stu-id="8ecce-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="8ecce-116">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8ecce-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="8ecce-117">Laukā Konfigurācijas repozitorija tips ievadiet Operācijas resursi.</span><span class="sxs-lookup"><span data-stu-id="8ecce-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="8ecce-118">Noklikšķiniet uz Izveidot repozitoriju.</span><span class="sxs-lookup"><span data-stu-id="8ecce-118">Click Create repository.</span></span>
7. <span data-ttu-id="8ecce-119">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="8ecce-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="8ecce-120">Iegūt piekļuvi korporācijas Microsoft nodrošinātajām Intrastat konfigurācijām</span><span class="sxs-lookup"><span data-stu-id="8ecce-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="8ecce-121">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="8ecce-121">Click Open.</span></span>
2. <span data-ttu-id="8ecce-122">Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="8ecce-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="8ecce-123">Noklikšķiniet uz Importēt.</span><span class="sxs-lookup"><span data-stu-id="8ecce-123">Click Import.</span></span>
    * <span data-ttu-id="8ecce-124">Noklikšķiniet uz Atlasītās konfigurācijas versijas 1.1 importēšana.</span><span class="sxs-lookup"><span data-stu-id="8ecce-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="8ecce-125">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="8ecce-125">Click Yes.</span></span>
5. <span data-ttu-id="8ecce-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="8ecce-126">Close the page.</span></span>
6. <span data-ttu-id="8ecce-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="8ecce-127">Close the page.</span></span>
7. <span data-ttu-id="8ecce-128">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="8ecce-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="8ecce-129">Kokā struktūrā izvērsiet 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="8ecce-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="8ecce-130">Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="8ecce-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>

