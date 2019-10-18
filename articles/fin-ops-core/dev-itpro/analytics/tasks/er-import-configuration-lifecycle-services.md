---
title: ER Importēt konfigurāciju no Lifecycle Services
description: Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var importēt jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācijas versiju no Microsoft Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0830707885e8ed52581aa789df0279d78e3a9c10
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184834"
---
# <a name="er-import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="40e90-103">ER Importēt konfigurāciju no Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="40e90-103">ER Import a configuration from Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="40e90-104">Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var importēt jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācijas versiju no Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="40e90-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="40e90-105">Šajā piemērā jūs atlasīsiet vēlamo ER konfigurācijas versiju un importēsiet to parauga uzņēmumam Litware, Inc. Šīs darbības var veikt jebkurā uzņēmumā, jo ER konfigurācijas tiek koplietotas visos uzņēmumos.</span><span class="sxs-lookup"><span data-stu-id="40e90-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="40e90-106">Lai izpildītu šīs darbības, jums vispirms ir jāizpilda procedūras “Augšupielādēt ER konfigurāciju pakalpojumos Lifecycle Services” darbības.</span><span class="sxs-lookup"><span data-stu-id="40e90-106">To complete these steps, you must first complete the steps in the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="40e90-107">Lai izpildītu šīs darbības, ir nepieciešama arī piekļuve pakalpojumiem LCS.</span><span class="sxs-lookup"><span data-stu-id="40e90-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="40e90-108">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="40e90-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="40e90-109">Noklikšķiniet uz Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="40e90-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="40e90-110">Dzēst koplietotu datu modeļa konfigurācijas versiju</span><span class="sxs-lookup"><span data-stu-id="40e90-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="40e90-111">Koka struktūrā atlasiet “Parauga modeļa konfigurācija”.</span><span class="sxs-lookup"><span data-stu-id="40e90-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="40e90-112">Parauga datu modeļa konfigurācijas pirmā versija tiek izveidota un pakalpojumos LCS tiek publicēta, izpildot procedūru “Augšupielādēt ER konfigurāciju pakalpojumos Lifecycle Services”.</span><span class="sxs-lookup"><span data-stu-id="40e90-112">The first version of a sample data model configuration has been created and published to LCS during the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="40e90-113">Šajā procedūrā jūs dzēsīsiet šo ER konfigurācijas versiju.</span><span class="sxs-lookup"><span data-stu-id="40e90-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="40e90-114">Šī parauga datu modeļa konfigurācijas versija vēlāk tiks importēta no LCS.</span><span class="sxs-lookup"><span data-stu-id="40e90-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="40e90-115">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="40e90-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="40e90-116">Atlasiet šīs konfigurācijas versiju, kuras statuss ir “Koplietots”.</span><span class="sxs-lookup"><span data-stu-id="40e90-116">Select the version of this configuration that is in the ‘Shared’ status.</span></span> <span data-ttu-id="40e90-117">Šis statuss norāda, ka konfigurācija ir publicēta pakalpojumos LCS.</span><span class="sxs-lookup"><span data-stu-id="40e90-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="40e90-118">Noklikšķiniet uz Mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="40e90-118">Click Change status.</span></span>
4. <span data-ttu-id="40e90-119">Noklikšķiniet uz Pārtraukt.</span><span class="sxs-lookup"><span data-stu-id="40e90-119">Click Discontinue.</span></span>
    * <span data-ttu-id="40e90-120">Atlasītās versijas statusu no “Koplietots” mainiet uz “Pārtraukts”, lai tā kļūtu pieejama dzēšanai.</span><span class="sxs-lookup"><span data-stu-id="40e90-120">Change the status of the selected version from ‘Shared’ to ‘Discontinued’ to make it available for deletion.</span></span>  
5. <span data-ttu-id="40e90-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="40e90-121">Click OK.</span></span>
6. <span data-ttu-id="40e90-122">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="40e90-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="40e90-123">Atlasiet šīs konfigurācijas versiju, kuras statuss ir “Pārtraukts”.</span><span class="sxs-lookup"><span data-stu-id="40e90-123">Select the version of this configuration that has a status of ‘Discontinued’.</span></span>  
7. <span data-ttu-id="40e90-124">Noklikšķiniet uz Dzēst.</span><span class="sxs-lookup"><span data-stu-id="40e90-124">Click Delete.</span></span>
8. <span data-ttu-id="40e90-125">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="40e90-125">Click Yes.</span></span>
    * <span data-ttu-id="40e90-126">Ņemiet vērā, ka atlasītajai datu modeļa konfigurācijai ir pieejama tikai melnraksta 2. versija.</span><span class="sxs-lookup"><span data-stu-id="40e90-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="40e90-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="40e90-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="40e90-128">Importēt koplietotu datu modeļa konfigurācijas versiju no LCS</span><span class="sxs-lookup"><span data-stu-id="40e90-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="40e90-129">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="40e90-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="40e90-130">Atveriet sarakstu ar repozitorijiem, kas paredzēti “Litware, Inc.”</span><span class="sxs-lookup"><span data-stu-id="40e90-130">Open the list of repositories for the ‘Litware, Inc.’</span></span> <span data-ttu-id="40e90-131">konfigurācijas nodrošinātājam.</span><span class="sxs-lookup"><span data-stu-id="40e90-131">configuration provider.</span></span>  
2. <span data-ttu-id="40e90-132">Noklikšķiniet uz Repozitoriji.</span><span class="sxs-lookup"><span data-stu-id="40e90-132">Click Repositories.</span></span>
3. <span data-ttu-id="40e90-133">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="40e90-133">Click Open.</span></span>
    * <span data-ttu-id="40e90-134">Atlasiet LCS repozitoriju un atveriet to.</span><span class="sxs-lookup"><span data-stu-id="40e90-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="40e90-135">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="40e90-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="40e90-136">Versiju sarakstā atlasiet konfigurācijas “Parauga modeļa konfigurācija” pirmo versiju.</span><span class="sxs-lookup"><span data-stu-id="40e90-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="40e90-137">Noklikšķiniet uz Importēt.</span><span class="sxs-lookup"><span data-stu-id="40e90-137">Click Import.</span></span>
6. <span data-ttu-id="40e90-138">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="40e90-138">Click Yes.</span></span>
    * <span data-ttu-id="40e90-139">Apstipriniet atlasītās versijas importēšanu no LCS.</span><span class="sxs-lookup"><span data-stu-id="40e90-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="40e90-140">Ņemiet vērā, ka informatīvais ziņojums (virs formas) apstiprina, ka atlasītās versijas importēšana ir sekmīgi pabeigta.</span><span class="sxs-lookup"><span data-stu-id="40e90-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="40e90-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="40e90-141">Close the page.</span></span>
8. <span data-ttu-id="40e90-142">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="40e90-142">Close the page.</span></span>
9. <span data-ttu-id="40e90-143">Noklikšķiniet uz Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="40e90-143">Click Configurations.</span></span>
10. <span data-ttu-id="40e90-144">Koka struktūrā atlasiet “Parauga modeļa konfigurācija”.</span><span class="sxs-lookup"><span data-stu-id="40e90-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="40e90-145">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="40e90-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="40e90-146">Atlasiet šīs konfigurācijas versiju, kuras statuss ir “Koplietots”.</span><span class="sxs-lookup"><span data-stu-id="40e90-146">Select the version of this configuration that has a status of ‘Shared’.</span></span>  
    * <span data-ttu-id="40e90-147">Ņemiet vērā, ka tagad atlasītajai datu modeļa konfigurācijai ir pieejama arī koplietotā 1. versija.</span><span class="sxs-lookup"><span data-stu-id="40e90-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  

