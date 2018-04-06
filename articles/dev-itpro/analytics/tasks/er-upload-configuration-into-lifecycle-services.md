--- 
title: "Augšupielādēt konfigurācijas informāciju no Lifecycle Services elektronisko pārskatu veidošanai (ER)"
description: "Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var izveidot jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurāciju un to augšupielādēt pakalpojumos Microsoft Lifecycle Services (LCS)."
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3d9c2192bac8477e9c9376aab3e3b561da777569
ms.contentlocale: lv-lv
ms.lasthandoff: 03/26/2018

---
# <a name="upload-a-configuration-into-lifecycle-services-for-electronic-reporting-er"></a><span data-ttu-id="15546-103">Augšupielādēt konfigurācijas informāciju no Lifecycle Services elektronisko pārskatu veidošanai (ER)</span><span class="sxs-lookup"><span data-stu-id="15546-103">Upload a configuration into Lifecycle Services for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="15546-104">Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var izveidot jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurāciju un to augšupielādēt pakalpojumos Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="15546-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration and upload it into Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="15546-105">Šajā piemērā jūs izveidosiet konfigurācijas un augšupielādēsiet to pakalpojumos LCS parauga uzņēmumam Litware, Inc. Šīs darbības var veikt jebkurā uzņēmumā, jo ER konfigurācijas ir kopīgas visiem uzņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="15546-105">In this example, you will create a configuration and upload it to LCS for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="15546-106">Lai veiktu šīs darbības, vispirms veiciet "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu" procedūras darbības.</span><span class="sxs-lookup"><span data-stu-id="15546-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="15546-107">Lai izpildītu šīs darbības, ir nepieciešama arī piekļuve pakalpojumiem LCS.</span><span class="sxs-lookup"><span data-stu-id="15546-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="15546-108">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="15546-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="15546-109">Atlasiet Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="15546-109">Select ‘Litware, Inc.’</span></span> <span data-ttu-id="15546-110">un iestatiet to kā aktīvu.</span><span class="sxs-lookup"><span data-stu-id="15546-110">and set it as active.</span></span>
3. <span data-ttu-id="15546-111">Noklikšķiniet uz Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="15546-111">Click Configurations.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="15546-112">Jaunas datu modeļa konfigurācijas izveide</span><span class="sxs-lookup"><span data-stu-id="15546-112">Create a new data model configuration</span></span>
1. <span data-ttu-id="15546-113">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="15546-113">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="15546-114">Jūs izveidosiet konfigurāciju, kas satur parauga datu modeli elektroniskajiem dokumentiem.</span><span class="sxs-lookup"><span data-stu-id="15546-114">You will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="15546-115">Šī datu modeļa konfigurācija vēlāk tiks augšupielādēta pakalpojumos LCS.</span><span class="sxs-lookup"><span data-stu-id="15546-115">This data model configuration will be uploaded into LCS later.</span></span>  
2. <span data-ttu-id="15546-116">Laukā Nosaukums ierakstiet “Parauga modeļa konfigurācija”.</span><span class="sxs-lookup"><span data-stu-id="15546-116">In the Name field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="15546-117">Parauga modeļa konfigurācija</span><span class="sxs-lookup"><span data-stu-id="15546-117">Sample model configuration</span></span>  
3. <span data-ttu-id="15546-118">Laukā Apraksts ierakstiet “Parauga modeļa konfigurācija”.</span><span class="sxs-lookup"><span data-stu-id="15546-118">In the Description field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="15546-119">Parauga modeļa konfigurācija</span><span class="sxs-lookup"><span data-stu-id="15546-119">Sample model configuration</span></span>  
4. <span data-ttu-id="15546-120">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="15546-120">Click Create configuration.</span></span>
5. <span data-ttu-id="15546-121">Noklikšķiniet uz Modeļa veidotājs.</span><span class="sxs-lookup"><span data-stu-id="15546-121">Click Model designer.</span></span>
6. <span data-ttu-id="15546-122">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="15546-122">Click New.</span></span>
7. <span data-ttu-id="15546-123">Laukā Nosaukums ierakstiet “Ieejas punkts”.</span><span class="sxs-lookup"><span data-stu-id="15546-123">In the Name field, type 'Entry point'.</span></span>
    * <span data-ttu-id="15546-124">Ieejas punkts</span><span class="sxs-lookup"><span data-stu-id="15546-124">Entry point</span></span>  
8. <span data-ttu-id="15546-125">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="15546-125">Click Add.</span></span>
9. <span data-ttu-id="15546-126">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="15546-126">Click Save.</span></span>
10. <span data-ttu-id="15546-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="15546-127">Close the page.</span></span>
11. <span data-ttu-id="15546-128">Noklikšķiniet uz Mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="15546-128">Click Change status.</span></span>
12. <span data-ttu-id="15546-129">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="15546-129">Click Complete.</span></span>
13. <span data-ttu-id="15546-130">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="15546-130">Click OK.</span></span>

## <a name="register-a-new--repository"></a><span data-ttu-id="15546-131">Reģistrēt jaunu repozitoriju</span><span class="sxs-lookup"><span data-stu-id="15546-131">Register a new  repository</span></span>
1. <span data-ttu-id="15546-132">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="15546-132">Close the page.</span></span>
2. <span data-ttu-id="15546-133">Noklikšķiniet uz Repozitoriji.</span><span class="sxs-lookup"><span data-stu-id="15546-133">Click Repositories.</span></span>
    * <span data-ttu-id="15546-134">Šādi jums tiek ļauts atvērt sarakstu ar repozitorijiem, kas paredzēti konfigurācijas nodrošinātājam Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="15546-134">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
3. <span data-ttu-id="15546-135">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="15546-135">Click Add to open the drop dialog.</span></span>
    * <span data-ttu-id="15546-136">Tas jums ļauj pievienot jaunu repozitoriju.</span><span class="sxs-lookup"><span data-stu-id="15546-136">This allows you to add a new repository.</span></span>  
4. <span data-ttu-id="15546-137">Laukā Konfigurācijas repozitorija tips atlasiet LCS.</span><span class="sxs-lookup"><span data-stu-id="15546-137">In the Configuration repository type field, select LCS.</span></span>
5. <span data-ttu-id="15546-138">Noklikšķiniet uz Izveidot repozitoriju.</span><span class="sxs-lookup"><span data-stu-id="15546-138">Click Create repository.</span></span>
6. <span data-ttu-id="15546-139">Laukā Projekts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="15546-139">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="15546-140">Atlasiet vēlamo LCS projektu.</span><span class="sxs-lookup"><span data-stu-id="15546-140">Select the desired LCS project.</span></span> <span data-ttu-id="15546-141">Jums ir nepieciešama piekļuve šim projektam.</span><span class="sxs-lookup"><span data-stu-id="15546-141">You must have access to the project.</span></span>  
7. <span data-ttu-id="15546-142">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="15546-142">Click OK.</span></span>
    * <span data-ttu-id="15546-143">Pabeidziet jauna repozitorija ierakstu.</span><span class="sxs-lookup"><span data-stu-id="15546-143">Complete a new repository entry.</span></span>  
8. <span data-ttu-id="15546-144">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="15546-144">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="15546-145">Atlasiet LCS repozitorija ierakstu.</span><span class="sxs-lookup"><span data-stu-id="15546-145">Select the LCS repository record.</span></span>  
    * <span data-ttu-id="15546-146">Ņemiet vērā, ka reģistrētais repozitorijs ir atzīmēts ar pašreizējo nodrošinātāju — tas nozīmē, ka šajā repozitorijā var novietot — un līdz ar to atlasītajā LCS projektā var augšupielādēt — tikai konfigurācijas, kas pieder šim nodrošinātājam.</span><span class="sxs-lookup"><span data-stu-id="15546-146">Note that a registered repository is marked by the current provider meaning that the only configurations owned by that provider can be placed to this repository and, consequently, uploaded into the selected LCS project.</span></span>  
9. <span data-ttu-id="15546-147">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="15546-147">Click Open.</span></span>
    * <span data-ttu-id="15546-148">Atveriet repozitoriju, lai skatītu sarakstu ar ER konfigurācijām.</span><span class="sxs-lookup"><span data-stu-id="15546-148">Open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="15546-149">Tas būs tukšs, ja šis projekts vēl nav lietots ER konfigurāciju koplietošanai.</span><span class="sxs-lookup"><span data-stu-id="15546-149">It will be empty if this project has not yet been used for ER configurations sharing.</span></span>  
10. <span data-ttu-id="15546-150">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="15546-150">Close the page.</span></span>
11. <span data-ttu-id="15546-151">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="15546-151">Close the page.</span></span>

## <a name="upload-configuration-into-lcs"></a><span data-ttu-id="15546-152">Augšupielādēt konfigurāciju pakalpojumos LCS</span><span class="sxs-lookup"><span data-stu-id="15546-152">Upload configuration into LCS</span></span>
1. <span data-ttu-id="15546-153">Noklikšķiniet uz Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="15546-153">Click Configurations.</span></span>
2. <span data-ttu-id="15546-154">Koka struktūrā atlasiet “Parauga modeļa konfigurācija”.</span><span class="sxs-lookup"><span data-stu-id="15546-154">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="15546-155">Atlasiet izveidotu konfigurāciju, kas jau pabeigta.</span><span class="sxs-lookup"><span data-stu-id="15546-155">Select a created configuration that has been already completed.</span></span>  
3. <span data-ttu-id="15546-156">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="15546-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="15546-157">Atlasiet atlasītās konfigurācijas versiju, kuras statuss ir “Pabeigts”.</span><span class="sxs-lookup"><span data-stu-id="15546-157">Select the version of the selected configuration with the status of ‘Completed’.</span></span>  
4. <span data-ttu-id="15546-158">Noklikšķiniet uz Mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="15546-158">Click Change status.</span></span>
5. <span data-ttu-id="15546-159">Noklikšķiniet uz Koplietot.</span><span class="sxs-lookup"><span data-stu-id="15546-159">Click Share.</span></span>
    * <span data-ttu-id="15546-160">Kad konfigurācija ir publicēta pakalpojumos LCS, tās statuss no “Pabeigts” mainās uz “Koplietots”.</span><span class="sxs-lookup"><span data-stu-id="15546-160">The configuration status will change from ‘Completed’ to ‘Shared’ when it is published in LCS.</span></span>  
6. <span data-ttu-id="15546-161">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="15546-161">Click OK.</span></span>
7. <span data-ttu-id="15546-162">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="15546-162">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="15546-163">Atlasiet konfigurācijas versiju, kuras statuss ir “Koplietots”.</span><span class="sxs-lookup"><span data-stu-id="15546-163">Select the configuration version with the status of 'Shared'.</span></span>  
    * <span data-ttu-id="15546-164">Ņemiet vērā, ka atlasītās versijas statuss no “Pabeigts” ir mainīts uz “Koplietots”.</span><span class="sxs-lookup"><span data-stu-id="15546-164">Note that the status of the selected version has changed from ‘Completed’ to ‘Shared’.</span></span>  
8. <span data-ttu-id="15546-165">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="15546-165">Close the page.</span></span>
9. <span data-ttu-id="15546-166">Noklikšķiniet uz Repozitoriji.</span><span class="sxs-lookup"><span data-stu-id="15546-166">Click Repositories.</span></span>
    * <span data-ttu-id="15546-167">Šādi jums tiek ļauts atvērt sarakstu ar repozitorijiem, kas paredzēti konfigurācijas nodrošinātājam Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="15546-167">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
10. <span data-ttu-id="15546-168">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="15546-168">Click Open.</span></span>
    * <span data-ttu-id="15546-169">Atlasiet LCS repozitoriju un atveriet to.</span><span class="sxs-lookup"><span data-stu-id="15546-169">Select the LCS repository and open it.</span></span>  
    * <span data-ttu-id="15546-170">Ņemiet vērā, ka atlasītā konfigurācija tiek rādīta kā atlasītā LCS projekta līdzeklis.</span><span class="sxs-lookup"><span data-stu-id="15546-170">Note that the selected configuration is shown as an asset of the selected LCS project.</span></span>  
    * <span data-ttu-id="15546-171">Atveriet LCS, izmantojot vietni https://lcs.dynamics.com. Atveriet iepriekš repozitorija reģistrēšanai izmantoto projektu, atveriet šī projekta sadaļu “Līdzekļu bibliotēka” un izvērsiet līdzekļa tipa “GER konfigurācija” saturu; šeit ir pieejama augšupielādētā ER konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="15546-171">Open LCS using https://lcs.dynamics.com. Open a project that was used earlier for repository registration, open the ‘Asset library’ of this project, and expand the content of the ‘GER configuration’ asset type – the uploaded ER configuration will be available.</span></span> <span data-ttu-id="15546-172">Ņemiet vērā, ka augšupielādēto LCS konfigurāciju var importēt citā programmas Microsoft Dynamics 365 for Finance and Operations instancē, ja nodrošinātājiem ir piekļuve šim LCS projektam.</span><span class="sxs-lookup"><span data-stu-id="15546-172">Note that the uploaded LCS configuration can be imported to another Microsoft Dynamics 365 for Finance and Operations instance if providers have access to this LCS project.</span></span>  


