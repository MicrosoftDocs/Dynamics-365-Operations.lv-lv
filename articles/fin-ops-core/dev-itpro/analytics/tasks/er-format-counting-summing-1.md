---
title: ER formāta konfigurēšana, lai veiktu uzskaiti un summēšanu (1. daļa. Formāta izveide)
description: Šajā tēmā ir aprakstīts, kā konfigurēt elektronisko pārskatu formātu, lai to skaitītu un summētu, pamatojoties uz jau ģenerētā teksta izvades datiem. (1. daļa)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 64bf9f48319029e835f9e3fe2b888625100cc408
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565146"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="fee7c-104">ER formāta konfigurēšana, lai veiktu uzskaiti un summēšanu (1. daļa. Formāta izveide)</span><span class="sxs-lookup"><span data-stu-id="fee7c-104">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fee7c-105">Tālāk aprakstītajos soļos ir izskaidrots, kā sistēmas lietotājs, kam ir piešķirta administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektronisko pārskatu sagatavošanas (ER) formātu, lai veiktu uzskaiti un summēšanu, izmantojot jau izveidotās teksta izvades datus.</span><span class="sxs-lookup"><span data-stu-id="fee7c-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="fee7c-106">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="fee7c-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="fee7c-107">Lai izpildītu tālāk norādītās darbības, vispirms izpildiet darbības, kas aprakstītas procedūrā "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu".</span><span class="sxs-lookup"><span data-stu-id="fee7c-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="fee7c-108">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="fee7c-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="fee7c-109">Iegūt piekļuvi korporācijas Microsoft nodrošināto konfigurāciju sarakstam</span><span class="sxs-lookup"><span data-stu-id="fee7c-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="fee7c-110">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="fee7c-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="fee7c-111">Pārliecinieties, vai "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="fee7c-111">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="fee7c-112">ir pieejams un atzīmēts kā aktīvs.</span><span class="sxs-lookup"><span data-stu-id="fee7c-112">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="fee7c-113">Atlasiet "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="fee7c-113">Select the "Litware, Inc."</span></span> <span data-ttu-id="fee7c-114">nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="fee7c-114">provider.</span></span>
3. <span data-ttu-id="fee7c-115">Noklikšķiniet uz Repozitoriji.</span><span class="sxs-lookup"><span data-stu-id="fee7c-115">Click Repositories.</span></span>
    * <span data-ttu-id="fee7c-116">Ja tipa “Operācijas resursi” repozitorijs jau pastāv, izlaidiet pašreizējā apakšuzdevuma pārējos soļus.</span><span class="sxs-lookup"><span data-stu-id="fee7c-116">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="fee7c-117">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="fee7c-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="fee7c-118">Laukā Konfigurācijas repozitorija tips ievadiet Operācijas resursi.</span><span class="sxs-lookup"><span data-stu-id="fee7c-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="fee7c-119">Noklikšķiniet uz Izveidot repozitoriju.</span><span class="sxs-lookup"><span data-stu-id="fee7c-119">Click Create repository.</span></span>
7. <span data-ttu-id="fee7c-120">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="fee7c-120">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="fee7c-121">Iegūt piekļuvi korporācijas Microsoft nodrošinātajām Intrastat konfigurācijām</span><span class="sxs-lookup"><span data-stu-id="fee7c-121">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="fee7c-122">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="fee7c-122">Click Open.</span></span>
2. <span data-ttu-id="fee7c-123">Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="fee7c-123">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="fee7c-124">Noklikšķiniet uz Importēt.</span><span class="sxs-lookup"><span data-stu-id="fee7c-124">Click Import.</span></span>
    * <span data-ttu-id="fee7c-125">Noklikšķiniet uz Atlasītās konfigurācijas versijas 1.1 importēšana.</span><span class="sxs-lookup"><span data-stu-id="fee7c-125">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="fee7c-126">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="fee7c-126">Click Yes.</span></span>
5. <span data-ttu-id="fee7c-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fee7c-127">Close the page.</span></span>
6. <span data-ttu-id="fee7c-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fee7c-128">Close the page.</span></span>
7. <span data-ttu-id="fee7c-129">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="fee7c-129">Click Reporting configurations.</span></span>
8. <span data-ttu-id="fee7c-130">Kokā struktūrā izvērsiet 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="fee7c-130">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="fee7c-131">Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="fee7c-131">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]