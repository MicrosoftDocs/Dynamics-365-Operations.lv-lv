--- 
title: "ER Importēt konfigurāciju no Lifecycle Services"
description: "Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var importēt jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācijas versiju no Microsoft Lifecycle Services (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 036d7e7e3f79e0945d6fef866a30edd41e688c07
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2018

---

# <a name="er-import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="c6484-103">ER Importēt konfigurāciju no Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="c6484-103">ER Import a configuration from Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c6484-104">Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var importēt jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācijas versiju no Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="c6484-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="c6484-105">Šajā piemērā jūs atlasīsiet vēlamo ER konfigurācijas versiju un importēsiet to parauga uzņēmumam Litware, Inc. Šīs darbības var veikt jebkurā uzņēmumā, jo ER konfigurācijas tiek koplietotas visos uzņēmumos.</span><span class="sxs-lookup"><span data-stu-id="c6484-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="c6484-106">Lai izpildītu šīs darbības, jums vispirms ir jāizpilda procedūras “Augšupielādēt ER konfigurāciju pakalpojumos Lifecycle Services” darbības.</span><span class="sxs-lookup"><span data-stu-id="c6484-106">To complete these steps, you must first complete the steps in the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="c6484-107">Lai izpildītu šīs darbības, ir nepieciešama arī piekļuve pakalpojumiem LCS.</span><span class="sxs-lookup"><span data-stu-id="c6484-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="c6484-108">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="c6484-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="c6484-109">Noklikšķiniet uz Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="c6484-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="c6484-110">Dzēst koplietotu datu modeļa konfigurācijas versiju</span><span class="sxs-lookup"><span data-stu-id="c6484-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="c6484-111">Koka struktūrā atlasiet “Parauga modeļa konfigurācija”.</span><span class="sxs-lookup"><span data-stu-id="c6484-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="c6484-112">Parauga datu modeļa konfigurācijas pirmā versija tiek izveidota un pakalpojumos LCS tiek publicēta, izpildot procedūru “Augšupielādēt ER konfigurāciju pakalpojumos Lifecycle Services”.</span><span class="sxs-lookup"><span data-stu-id="c6484-112">The first version of a sample data model configuration has been created and published to LCS during the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="c6484-113">Šajā procedūrā jūs dzēsīsiet šo ER konfigurācijas versiju.</span><span class="sxs-lookup"><span data-stu-id="c6484-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="c6484-114">Šī parauga datu modeļa konfigurācijas versija vēlāk tiks importēta no LCS.</span><span class="sxs-lookup"><span data-stu-id="c6484-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="c6484-115">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c6484-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c6484-116">Atlasiet šīs konfigurācijas versiju, kuras statuss ir “Koplietots”.</span><span class="sxs-lookup"><span data-stu-id="c6484-116">Select the version of this configuration that is in the ‘Shared’ status.</span></span> <span data-ttu-id="c6484-117">Šis statuss norāda, ka konfigurācija ir publicēta pakalpojumos LCS.</span><span class="sxs-lookup"><span data-stu-id="c6484-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="c6484-118">Noklikšķiniet uz Mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="c6484-118">Click Change status.</span></span>
4. <span data-ttu-id="c6484-119">Noklikšķiniet uz Pārtraukt.</span><span class="sxs-lookup"><span data-stu-id="c6484-119">Click Discontinue.</span></span>
    * <span data-ttu-id="c6484-120">Atlasītās versijas statusu no “Koplietots” mainiet uz “Pārtraukts”, lai tā kļūtu pieejama dzēšanai.</span><span class="sxs-lookup"><span data-stu-id="c6484-120">Change the status of the selected version from ‘Shared’ to ‘Discontinued’ to make it available for deletion.</span></span>  
5. <span data-ttu-id="c6484-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="c6484-121">Click OK.</span></span>
6. <span data-ttu-id="c6484-122">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c6484-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c6484-123">Atlasiet šīs konfigurācijas versiju, kuras statuss ir “Pārtraukts”.</span><span class="sxs-lookup"><span data-stu-id="c6484-123">Select the version of this configuration that has a status of ‘Discontinued’.</span></span>  
7. <span data-ttu-id="c6484-124">Noklikšķiniet uz Dzēst.</span><span class="sxs-lookup"><span data-stu-id="c6484-124">Click Delete.</span></span>
8. <span data-ttu-id="c6484-125">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="c6484-125">Click Yes.</span></span>
    * <span data-ttu-id="c6484-126">Ņemiet vērā, ka atlasītajai datu modeļa konfigurācijai ir pieejama tikai melnraksta 2. versija.</span><span class="sxs-lookup"><span data-stu-id="c6484-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="c6484-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c6484-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="c6484-128">Importēt koplietotu datu modeļa konfigurācijas versiju no LCS</span><span class="sxs-lookup"><span data-stu-id="c6484-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="c6484-129">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="c6484-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c6484-130">Atveriet sarakstu ar repozitorijiem, kas paredzēti “Litware, Inc.”</span><span class="sxs-lookup"><span data-stu-id="c6484-130">Open the list of repositories for the ‘Litware, Inc.’</span></span> <span data-ttu-id="c6484-131">konfigurācijas nodrošinātājam.</span><span class="sxs-lookup"><span data-stu-id="c6484-131">configuration provider.</span></span>  
2. <span data-ttu-id="c6484-132">Noklikšķiniet uz Repozitoriji.</span><span class="sxs-lookup"><span data-stu-id="c6484-132">Click Repositories.</span></span>
3. <span data-ttu-id="c6484-133">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="c6484-133">Click Open.</span></span>
    * <span data-ttu-id="c6484-134">Atlasiet LCS repozitoriju un atveriet to.</span><span class="sxs-lookup"><span data-stu-id="c6484-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="c6484-135">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="c6484-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c6484-136">Versiju sarakstā atlasiet konfigurācijas “Parauga modeļa konfigurācija” pirmo versiju.</span><span class="sxs-lookup"><span data-stu-id="c6484-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="c6484-137">Noklikšķiniet uz Importēt.</span><span class="sxs-lookup"><span data-stu-id="c6484-137">Click Import.</span></span>
6. <span data-ttu-id="c6484-138">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="c6484-138">Click Yes.</span></span>
    * <span data-ttu-id="c6484-139">Apstipriniet atlasītās versijas importēšanu no LCS.</span><span class="sxs-lookup"><span data-stu-id="c6484-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="c6484-140">Ņemiet vērā, ka informatīvais ziņojums (virs formas) apstiprina, ka atlasītās versijas importēšana ir sekmīgi pabeigta.</span><span class="sxs-lookup"><span data-stu-id="c6484-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="c6484-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c6484-141">Close the page.</span></span>
8. <span data-ttu-id="c6484-142">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c6484-142">Close the page.</span></span>
9. <span data-ttu-id="c6484-143">Noklikšķiniet uz Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="c6484-143">Click Configurations.</span></span>
10. <span data-ttu-id="c6484-144">Koka struktūrā atlasiet “Parauga modeļa konfigurācija”.</span><span class="sxs-lookup"><span data-stu-id="c6484-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="c6484-145">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c6484-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c6484-146">Atlasiet šīs konfigurācijas versiju, kuras statuss ir “Koplietots”.</span><span class="sxs-lookup"><span data-stu-id="c6484-146">Select the version of this configuration that has a status of ‘Shared’.</span></span>  
    * <span data-ttu-id="c6484-147">Ņemiet vērā, ka tagad atlasītajai datu modeļa konfigurācijai ir pieejama arī koplietotā 1. versija.</span><span class="sxs-lookup"><span data-stu-id="c6484-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  


