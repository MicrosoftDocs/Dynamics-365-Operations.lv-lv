---
title: Elektronisko pārskatu veidošanas (ER) modeļu kartēšanas konfigurāciju izveide
description: Izmantojiet šo procedūru, lai izveidotu jaunu elektronisko pārskatu veidošanas (ER) modeļa kartējuma konfigurāciju un izmantotu iebūvētās ER funkcijas, lai nodrošinātu apkopoto aprēķinu efektivitāti.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c52f5d23f6c1cdad346a8a5e94535a4cba19057
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562884"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a><span data-ttu-id="b27b1-103">Elektronisko pārskatu veidošanas (ER) modeļu kartēšanas konfigurāciju izveide</span><span class="sxs-lookup"><span data-stu-id="b27b1-103">Create Electronic reporting (ER) model mapping configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b27b1-104">Izmantojiet šo procedūru, lai izveidotu jaunu elektronisko pārskatu veidošanas (ER) modeļa kartējuma konfigurāciju un izmantotu iebūvētās ER funkcijas, lai nodrošinātu apkopoto aprēķinu efektivitāti.</span><span class="sxs-lookup"><span data-stu-id="b27b1-104">Use this procedure to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="b27b1-105">Šajā procedūrā izveidosit konfigurāciju parauga uzņēmumam Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="b27b1-105">In this procedure, you will create a configuration for sample company, Litware, Inc.</span></span> 

<span data-ttu-id="b27b1-106">Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma.</span><span class="sxs-lookup"><span data-stu-id="b27b1-106">This procedure is created for uses with the assigned role of System administrator or Electronic reporting developer.</span></span>

<span data-ttu-id="b27b1-107">Šīs darbības var veikt, izmantojot jebkuru datu kopu.</span><span class="sxs-lookup"><span data-stu-id="b27b1-107">These steps can be completed using any dataset.</span></span> <span data-ttu-id="b27b1-108">Lai izpildītu tālāk norādītās darbības, vispirms izpildiet procedūras darbības “Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu”.</span><span class="sxs-lookup"><span data-stu-id="b27b1-108">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>

1. <span data-ttu-id="b27b1-109">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="b27b1-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="b27b1-110">Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam “Litware, Inc.” ir pieejams un ir atzīmēts kā aktīvs.</span><span class="sxs-lookup"><span data-stu-id="b27b1-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="b27b1-111">Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas aprakstītas procedūrā “Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu”.</span><span class="sxs-lookup"><span data-stu-id="b27b1-111">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>  
2. <span data-ttu-id="b27b1-112">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="b27b1-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="b27b1-113">Noklikšķiniet uz Rādīt filtrus.</span><span class="sxs-lookup"><span data-stu-id="b27b1-113">Click Show filters.</span></span>
4. <span data-ttu-id="b27b1-114">Laukā “Nosaukums” ievadiet filtra vērtību “Intrastat” un izmantojiet filtra operatoru “sākas ar”.</span><span class="sxs-lookup"><span data-stu-id="b27b1-114">In the "Name" field, enter the filter value, "Intrastat" and use the filter operator "begins with".</span></span>
    * <span data-ttu-id="b27b1-115">Lietojiet šo filtru, lai atrastu 'Intrastat' datu modeļa konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="b27b1-115">Apply this filter to find the 'Intrastat' data model configuration.</span></span> <span data-ttu-id="b27b1-116">Šis modelis jau var būt konfigurāciju kokā.</span><span class="sxs-lookup"><span data-stu-id="b27b1-116">This model may already exist in the configurations tree.</span></span> <span data-ttu-id="b27b1-117">Šādā gadījumā, izlaidiet nākamo apakšuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="b27b1-117">If it does, skip the next sub-task.</span></span>   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a><span data-ttu-id="b27b1-118">Iegūt piekļuvi korporācijas Microsoft nodrošinātajai Intrastat modeļa konfigurācijai</span><span class="sxs-lookup"><span data-stu-id="b27b1-118">Get the Intrastat model configuration provided by Microsoft</span></span>
1. <span data-ttu-id="b27b1-119">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b27b1-119">Close the page.</span></span>
2. <span data-ttu-id="b27b1-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b27b1-120">Close the page.</span></span>
3. <span data-ttu-id="b27b1-121">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="b27b1-121">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
4. <span data-ttu-id="b27b1-122">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b27b1-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b27b1-123">Atlasiet elementu Microsoft nodrošinātājs.</span><span class="sxs-lookup"><span data-stu-id="b27b1-123">Select the Microsoft provider tile.</span></span>  
5. <span data-ttu-id="b27b1-124">Noklikšķiniet uz Repozitoriji.</span><span class="sxs-lookup"><span data-stu-id="b27b1-124">Click Repositories.</span></span>
    * <span data-ttu-id="b27b1-125">Noklikšķiniet uz Repozitoriji elementā Microsoft nodrošinātājs.</span><span class="sxs-lookup"><span data-stu-id="b27b1-125">Click Repositories in the Microsoft provider tile.</span></span>  
6. <span data-ttu-id="b27b1-126">Noklikšķiniet uz Rādīt filtrus.</span><span class="sxs-lookup"><span data-stu-id="b27b1-126">Click Show filters.</span></span>
7. <span data-ttu-id="b27b1-127">Laukā “Tipa nosaukums” ievadiet filtra vērtību “resursi” un izmantojiet filtra operatoru “satur”.</span><span class="sxs-lookup"><span data-stu-id="b27b1-127">In the "Type name" field, enter the filter value, "resources" and use the filter operator "contains".</span></span> 
8. <span data-ttu-id="b27b1-128">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="b27b1-128">Click Open.</span></span>
9. <span data-ttu-id="b27b1-129">Kokā atlasiet “Intrastat modelis”.</span><span class="sxs-lookup"><span data-stu-id="b27b1-129">In the tree, select 'Intrastat model'.</span></span>
10. <span data-ttu-id="b27b1-130">Noklikšķiniet uz Importēt.</span><span class="sxs-lookup"><span data-stu-id="b27b1-130">Click Import.</span></span>
11. <span data-ttu-id="b27b1-131">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="b27b1-131">Click Yes.</span></span>
    * <span data-ttu-id="b27b1-132">Jūs importējāt ER modeļa konfigurāciju, kas satur datu modeli, kuru izmantosit, lai izpētītu, kā var izmantot jauno ER funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="b27b1-132">You imported the ER model configuration that contains the data model that you will use to explore how the new ER functionality can be used.</span></span>  
12. <span data-ttu-id="b27b1-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b27b1-133">Close the page.</span></span>
13. <span data-ttu-id="b27b1-134">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b27b1-134">Close the page.</span></span>
14. <span data-ttu-id="b27b1-135">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="b27b1-135">Click Reporting configurations.</span></span>

## <a name="add-a-new-model-mapping-configuration"></a><span data-ttu-id="b27b1-136">Pievienot jaunu modeļa kartējuma konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="b27b1-136">Add a new model mapping configuration</span></span>
1. <span data-ttu-id="b27b1-137">Kokā atlasiet “Intrastat modelis”.</span><span class="sxs-lookup"><span data-stu-id="b27b1-137">In the tree, select 'Intrastat model'.</span></span>
2. <span data-ttu-id="b27b1-138">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b27b1-138">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="b27b1-139">Laukā Jauns ievadiet “Uz datu modeli Intrastat balstīts modeļa kartējums”.</span><span class="sxs-lookup"><span data-stu-id="b27b1-139">In the New field, enter 'Model Mapping based on data model Intrastat'.</span></span>
4. <span data-ttu-id="b27b1-140">Laukā Nosaukums ierakstiet “Intrastat parauga kartēšana”.</span><span class="sxs-lookup"><span data-stu-id="b27b1-140">In the Name field, type 'Intrastat sample mapping'.</span></span>
    * <span data-ttu-id="b27b1-141">Intrastat parauga kartēšana</span><span class="sxs-lookup"><span data-stu-id="b27b1-141">Intrastat sample mapping</span></span>  
5. <span data-ttu-id="b27b1-142">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="b27b1-142">Click Create configuration.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]