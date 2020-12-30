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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1742582057cc912d8e6f90eb14e9e4cdcd193608
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684719"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="949f2-103">ER formāta konfigurēšana, lai veiktu uzskaiti un summēšanu (1. daļa. Formāta izveide)</span><span class="sxs-lookup"><span data-stu-id="949f2-103">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="949f2-104">Tālāk aprakstītajos soļos ir izskaidrots, kā sistēmas lietotājs, kam ir piešķirta administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektronisko pārskatu sagatavošanas (ER) formātu, lai veiktu uzskaiti un summēšanu, izmantojot jau izveidotās teksta izvades datus.</span><span class="sxs-lookup"><span data-stu-id="949f2-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="949f2-105">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="949f2-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="949f2-106">Lai izpildītu tālāk norādītās darbības, vispirms izpildiet darbības, kas aprakstītas procedūrā "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu".</span><span class="sxs-lookup"><span data-stu-id="949f2-106">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="949f2-107">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="949f2-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="949f2-108">Iegūt piekļuvi korporācijas Microsoft nodrošināto konfigurāciju sarakstam</span><span class="sxs-lookup"><span data-stu-id="949f2-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="949f2-109">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="949f2-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="949f2-110">Pārliecinieties, vai "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="949f2-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="949f2-111">ir pieejams un atzīmēts kā aktīvs.</span><span class="sxs-lookup"><span data-stu-id="949f2-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="949f2-112">Atlasiet "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="949f2-112">Select the "Litware, Inc."</span></span> <span data-ttu-id="949f2-113">nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="949f2-113">provider.</span></span>
3. <span data-ttu-id="949f2-114">Noklikšķiniet uz Repozitoriji.</span><span class="sxs-lookup"><span data-stu-id="949f2-114">Click Repositories.</span></span>
    * <span data-ttu-id="949f2-115">Ja tipa “Operācijas resursi” repozitorijs jau pastāv, izlaidiet pašreizējā apakšuzdevuma pārējos soļus.</span><span class="sxs-lookup"><span data-stu-id="949f2-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="949f2-116">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="949f2-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="949f2-117">Laukā Konfigurācijas repozitorija tips ievadiet Operācijas resursi.</span><span class="sxs-lookup"><span data-stu-id="949f2-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="949f2-118">Noklikšķiniet uz Izveidot repozitoriju.</span><span class="sxs-lookup"><span data-stu-id="949f2-118">Click Create repository.</span></span>
7. <span data-ttu-id="949f2-119">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="949f2-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="949f2-120">Iegūt piekļuvi korporācijas Microsoft nodrošinātajām Intrastat konfigurācijām</span><span class="sxs-lookup"><span data-stu-id="949f2-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="949f2-121">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="949f2-121">Click Open.</span></span>
2. <span data-ttu-id="949f2-122">Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="949f2-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="949f2-123">Noklikšķiniet uz Importēt.</span><span class="sxs-lookup"><span data-stu-id="949f2-123">Click Import.</span></span>
    * <span data-ttu-id="949f2-124">Noklikšķiniet uz Atlasītās konfigurācijas versijas 1.1 importēšana.</span><span class="sxs-lookup"><span data-stu-id="949f2-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="949f2-125">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="949f2-125">Click Yes.</span></span>
5. <span data-ttu-id="949f2-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="949f2-126">Close the page.</span></span>
6. <span data-ttu-id="949f2-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="949f2-127">Close the page.</span></span>
7. <span data-ttu-id="949f2-128">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="949f2-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="949f2-129">Kokā struktūrā izvērsiet 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="949f2-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="949f2-130">Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="949f2-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>

