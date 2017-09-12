--- 
title: "Importēt konfigurāciju no Lifecycle Services elektronisko pārskatu veidošanai (ER)"
description: "Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var importēt jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācijas versiju no Microsoft Lifecycle Services (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 05/13/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0ea1e70f94e4b81919512127578d5927b36db56f
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="import-a-configuration-from-lifecycle-services-for-electronic-reporting-er"></a><span data-ttu-id="6fab6-103">Importēt konfigurāciju no Lifecycle Services elektronisko pārskatu veidošanai (ER)</span><span class="sxs-lookup"><span data-stu-id="6fab6-103">Import a configuration from Lifecycle Services for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6fab6-104">Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var importēt jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācijas versiju no Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6fab6-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="6fab6-105">Šajā piemērā jūs atlasīsiet vēlamo ER konfigurācijas versiju un importēsiet to parauga uzņēmumam Litware, Inc. Šīs darbības var veikt jebkurā uzņēmumā, jo ER konfigurācijas tiek koplietotas visos uzņēmumos.</span><span class="sxs-lookup"><span data-stu-id="6fab6-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="6fab6-106">Lai izpildītu šīs darbības, jums vispirms ir jāizpilda procedūras “Augšupielādēt ER konfigurāciju pakalpojumos Lifecycle Services” darbības.</span><span class="sxs-lookup"><span data-stu-id="6fab6-106">To complete these steps, you must first complete the steps in the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="6fab6-107">Lai izpildītu šīs darbības, ir nepieciešama arī piekļuve pakalpojumiem LCS.</span><span class="sxs-lookup"><span data-stu-id="6fab6-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="6fab6-108">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="6fab6-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="6fab6-109">Noklikšķiniet uz Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="6fab6-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="6fab6-110">Dzēst koplietotu datu modeļa konfigurācijas versiju</span><span class="sxs-lookup"><span data-stu-id="6fab6-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="6fab6-111">Koka struktūrā atlasiet “Parauga modeļa konfigurācija”.</span><span class="sxs-lookup"><span data-stu-id="6fab6-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="6fab6-112">Parauga datu modeļa konfigurācijas pirmā versija tiek izveidota un pakalpojumos LCS tiek publicēta, izpildot procedūru “Augšupielādēt ER konfigurāciju pakalpojumos Lifecycle Services”.</span><span class="sxs-lookup"><span data-stu-id="6fab6-112">The first version of a sample data model configuration has been created and published to LCS during the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="6fab6-113">Šajā procedūrā jūs dzēsīsiet šo ER konfigurācijas versiju.</span><span class="sxs-lookup"><span data-stu-id="6fab6-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="6fab6-114">Šī parauga datu modeļa konfigurācijas versija vēlāk tiks importēta no LCS.</span><span class="sxs-lookup"><span data-stu-id="6fab6-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="6fab6-115">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="6fab6-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6fab6-116">Atlasiet šīs konfigurācijas versiju, kuras statuss ir “Koplietots”.</span><span class="sxs-lookup"><span data-stu-id="6fab6-116">Select the version of this configuration that is in the ‘Shared’ status.</span></span> <span data-ttu-id="6fab6-117">Šis statuss norāda, ka konfigurācija ir publicēta pakalpojumos LCS.</span><span class="sxs-lookup"><span data-stu-id="6fab6-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="6fab6-118">Noklikšķiniet uz Mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="6fab6-118">Click Change status.</span></span>
4. <span data-ttu-id="6fab6-119">Noklikšķiniet uz Pārtraukt.</span><span class="sxs-lookup"><span data-stu-id="6fab6-119">Click Discontinue.</span></span>
    * <span data-ttu-id="6fab6-120">Atlasītās versijas statusu no “Koplietots” mainiet uz “Pārtraukts”, lai tā kļūtu pieejama dzēšanai.</span><span class="sxs-lookup"><span data-stu-id="6fab6-120">Change the status of the selected version from ‘Shared’ to ‘Discontinued’ to make it available for deletion.</span></span>  
5. <span data-ttu-id="6fab6-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="6fab6-121">Click OK.</span></span>
6. <span data-ttu-id="6fab6-122">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="6fab6-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6fab6-123">Atlasiet šīs konfigurācijas versiju, kuras statuss ir “Pārtraukts”.</span><span class="sxs-lookup"><span data-stu-id="6fab6-123">Select the version of this configuration that has a status of ‘Discontinued’.</span></span>  
7. <span data-ttu-id="6fab6-124">Noklikšķiniet uz Dzēst.</span><span class="sxs-lookup"><span data-stu-id="6fab6-124">Click Delete.</span></span>
8. <span data-ttu-id="6fab6-125">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="6fab6-125">Click Yes.</span></span>
    * <span data-ttu-id="6fab6-126">Ņemiet vērā, ka atlasītajai datu modeļa konfigurācijai ir pieejama tikai melnraksta 2. versija.</span><span class="sxs-lookup"><span data-stu-id="6fab6-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="6fab6-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6fab6-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="6fab6-128">Importēt koplietotu datu modeļa konfigurācijas versiju no LCS</span><span class="sxs-lookup"><span data-stu-id="6fab6-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="6fab6-129">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="6fab6-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6fab6-130">Atveriet sarakstu ar repozitorijiem, kas paredzēti “Litware, Inc.”</span><span class="sxs-lookup"><span data-stu-id="6fab6-130">Open the list of repositories for the ‘Litware, Inc.’</span></span> <span data-ttu-id="6fab6-131">konfigurācijas nodrošinātājam.</span><span class="sxs-lookup"><span data-stu-id="6fab6-131">configuration provider.</span></span>  
2. <span data-ttu-id="6fab6-132">Noklikšķiniet uz Repozitoriji.</span><span class="sxs-lookup"><span data-stu-id="6fab6-132">Click Repositories.</span></span>
3. <span data-ttu-id="6fab6-133">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="6fab6-133">Click Open.</span></span>
    * <span data-ttu-id="6fab6-134">Atlasiet LCS repozitoriju un atveriet to.</span><span class="sxs-lookup"><span data-stu-id="6fab6-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="6fab6-135">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="6fab6-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6fab6-136">Versiju sarakstā atlasiet konfigurācijas “Parauga modeļa konfigurācija” pirmo versiju.</span><span class="sxs-lookup"><span data-stu-id="6fab6-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="6fab6-137">Noklikšķiniet uz Importēt.</span><span class="sxs-lookup"><span data-stu-id="6fab6-137">Click Import.</span></span>
6. <span data-ttu-id="6fab6-138">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="6fab6-138">Click Yes.</span></span>
    * <span data-ttu-id="6fab6-139">Apstipriniet atlasītās versijas importēšanu no LCS.</span><span class="sxs-lookup"><span data-stu-id="6fab6-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="6fab6-140">Ņemiet vērā, ka informatīvais ziņojums (virs formas) apstiprina, ka atlasītās versijas importēšana ir sekmīgi pabeigta.</span><span class="sxs-lookup"><span data-stu-id="6fab6-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="6fab6-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6fab6-141">Close the page.</span></span>
8. <span data-ttu-id="6fab6-142">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6fab6-142">Close the page.</span></span>
9. <span data-ttu-id="6fab6-143">Noklikšķiniet uz Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="6fab6-143">Click Configurations.</span></span>
10. <span data-ttu-id="6fab6-144">Koka struktūrā atlasiet “Parauga modeļa konfigurācija”.</span><span class="sxs-lookup"><span data-stu-id="6fab6-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="6fab6-145">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="6fab6-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6fab6-146">Atlasiet šīs konfigurācijas versiju, kuras statuss ir “Koplietots”.</span><span class="sxs-lookup"><span data-stu-id="6fab6-146">Select the version of this configuration that has a status of ‘Shared’.</span></span>  
    * <span data-ttu-id="6fab6-147">Ņemiet vērā, ka tagad atlasītajai datu modeļa konfigurācijai ir pieejama arī koplietotā 1. versija.</span><span class="sxs-lookup"><span data-stu-id="6fab6-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  


