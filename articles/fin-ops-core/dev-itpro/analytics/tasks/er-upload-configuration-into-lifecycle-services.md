---
title: Augšupielādēt konfigurāciju pakalpojumos Lifecycle Services
description: Šajā tēmā ir izskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var izveidot jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurāciju un augšupielādēt to programmā Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ebafb52882fd33f4f0ef140c5d23d3288af97a2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684167"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="3285f-103">Augšupielādēt konfigurāciju pakalpojumos Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="3285f-103">Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3285f-104">Šajā tēmā ir izskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var izveidot jaunu [Elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācija](../general-electronic-reporting.md#Configuration) un augšupielādēt to programmā [projekta līmeņa līdzekļu bibliotēka](../../lifecycle-services/asset-library.md) Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="3285f-104">This topic explains how a user in the System administrator or Electronic reporting developer role can create a new [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) and upload it into the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="3285f-105">Šajā piemērā jūs izveidosiet konfigurācijas un augšupielādēsiet to pakalpojumos LCS parauga uzņēmumam ar nosaukumu Litware, Inc. Šīs darbības var pabeigt jebkurā uzņēmumā, jo ER konfigurācijas ir kopīgas visiem uzņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="3285f-105">In this example, you will create a configuration and upload it into LCS for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="3285f-106">Lai izpildītu tālāk norādītās darbības, vispirms izpildiet darbības [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="3285f-106">To complete these steps, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="3285f-107">Ir nepieciešama arī piekļuve LCS.</span><span class="sxs-lookup"><span data-stu-id="3285f-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="3285f-108">Pierakstieties programmā, izmantojot vienu no šīm lomām:</span><span class="sxs-lookup"><span data-stu-id="3285f-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="3285f-109">Elektroniskā pārskata izstrādātājs</span><span class="sxs-lookup"><span data-stu-id="3285f-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="3285f-110">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="3285f-110">System administrator</span></span>

2. <span data-ttu-id="3285f-111">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="3285f-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="3285f-112">Atlasiet vienumu **Litware, Inc.** un atzīmējiet to kā **Aktīvs**.</span><span class="sxs-lookup"><span data-stu-id="3285f-112">Select **Litware, Inc.**, and mark it as **Active**.</span></span>
4. <span data-ttu-id="3285f-113">Atlasiet **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="3285f-113">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="3285f-114">Pārliecinieties, vai pašreizējais Dynamics 365 Finance lietotājs ir tāda LCS projekta biedrs, kurā ir ietverta tā [Līdzekļu bibliotēka](../../lifecycle-services/asset-library.md#asset-library-support) , ko izmanto ER konfigurāciju importēšanai.</span><span class="sxs-lookup"><span data-stu-id="3285f-114">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the [Asset library](../../lifecycle-services/asset-library.md#asset-library-support) that is used to import ER configurations.</span></span>
>
> <span data-ttu-id="3285f-115">Jūs nevarat piekļūt LCS projektam no ER repozitorija, kas pārstāv citu domēnu, nevis to domēnu, kas tiek izmantots programmā Finance.</span><span class="sxs-lookup"><span data-stu-id="3285f-115">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="3285f-116">Ja jūs mēģināt, tiks rādīts tukšs LCS projektu saraksts, un jūs nevarēsiet importēt ER konfigurācijas no projekta līmeņa līdzekļu bibliotēkas uz LCS.</span><span class="sxs-lookup"><span data-stu-id="3285f-116">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="3285f-117">Lai piekļūtu projekta līmeņa līdzekļu bibliotēkām no ER repozitorija, kas tiek izmantots, lai importētu ER konfigurācijas, piesakieties programmai Finance, izmantojot lietotāja akreditācijas datus, kas pieder nomniekam (domēns), kam ir nodrošināta pašreizējā Finance instance.</span><span class="sxs-lookup"><span data-stu-id="3285f-117">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="3285f-118">Jaunas datu modeļa konfigurācijas izveide</span><span class="sxs-lookup"><span data-stu-id="3285f-118">Create a new data model configuration</span></span>

1. <span data-ttu-id="3285f-119">Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="3285f-119">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="3285f-120">Lapā **Konfigurācijas** atlasiet **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="3285f-120">On the **Configurations** page, select **Create configuration** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="3285f-121">Šajā piemērā jūs izveidosiet konfigurāciju, kas satur parauga datu modeli elektroniskajiem dokumentiem.</span><span class="sxs-lookup"><span data-stu-id="3285f-121">In this example, you will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="3285f-122">Šī datu modeļa konfigurācija vēlāk tiks augšupielādēta pakalpojumos LCS.</span><span class="sxs-lookup"><span data-stu-id="3285f-122">This data model configuration will be uploaded into LCS later.</span></span>

3. <span data-ttu-id="3285f-123">Laukā **Nosaukums** ievādiet **Parauga modeļa konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="3285f-123">In the **Name** field, enter **Sample model configuration**.</span></span>
4. <span data-ttu-id="3285f-124">Laukā **Apraksts** ievādiet **Parauga modeļa konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="3285f-124">In the **Description** field, enter **Sample model configuration**.</span></span>
5. <span data-ttu-id="3285f-125">Atlasiet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="3285f-125">Select **Create configuration**.</span></span>
6. <span data-ttu-id="3285f-126">Atlasiet **Modeļa veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="3285f-126">Select **Model designer**.</span></span>
7. <span data-ttu-id="3285f-127">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="3285f-127">Select **New**.</span></span>
8. <span data-ttu-id="3285f-128">Laukā **Nosaukums** ievadiet **Ieejas punkts**.</span><span class="sxs-lookup"><span data-stu-id="3285f-128">In the **Name** field, enter **Entry point**.</span></span>
9. <span data-ttu-id="3285f-129">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="3285f-129">Select **Add**.</span></span>
10. <span data-ttu-id="3285f-130">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="3285f-130">Select **Save**.</span></span>
11. <span data-ttu-id="3285f-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3285f-131">Close the page.</span></span>
12. <span data-ttu-id="3285f-132">Atlasiet **Mainīt statusu**.</span><span class="sxs-lookup"><span data-stu-id="3285f-132">Select **Change status**.</span></span>
13. <span data-ttu-id="3285f-133">Atlasiet **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="3285f-133">Select **Complete**.</span></span>
14. <span data-ttu-id="3285f-134">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3285f-134">Select **OK**.</span></span>
15. <span data-ttu-id="3285f-135">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3285f-135">Close the page.</span></span>

## <a name="register-a-new-repository"></a><span data-ttu-id="3285f-136">Reģistrēt jaunu repozitoriju</span><span class="sxs-lookup"><span data-stu-id="3285f-136">Register a new repository</span></span>

1. <span data-ttu-id="3285f-137">Dodieties uz **Organizācijas administrēšana \> Darbvietas \> Elektronisko atskaišu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="3285f-137">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="3285f-138">Sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="3285f-138">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="3285f-139">Elementā **Litware, Inc.** atlasiet **Repozitoriji**.</span><span class="sxs-lookup"><span data-stu-id="3285f-139">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="3285f-140">Tagad var atvērt sarakstu ar repozitorijiem, kas paredzēti Litware, Inc. konfigurācijas nodrošinātājam.</span><span class="sxs-lookup"><span data-stu-id="3285f-140">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="3285f-141">Atlasiet **Pievienot**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="3285f-141">Select **Add** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="3285f-142">Tagad varat pievienot jaunu repozitoriju.</span><span class="sxs-lookup"><span data-stu-id="3285f-142">You can now add a new repository.</span></span>

5. <span data-ttu-id="3285f-143">Laukā **Konfigurācijas repozitorija ievade** atlasiet **LCS**.</span><span class="sxs-lookup"><span data-stu-id="3285f-143">In the **Configuration repository enter** field, select **LCS**.</span></span>
6. <span data-ttu-id="3285f-144">Atlasiet **Izveidot repozitoriju**.</span><span class="sxs-lookup"><span data-stu-id="3285f-144">Select **Create repository**.</span></span>
7. <span data-ttu-id="3285f-145">Laukā **Projekts** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3285f-145">In the **Project** field, enter or select a value.</span></span>

    <span data-ttu-id="3285f-146">Šim piemēram atlasiet vēlāmo LCS projektu.</span><span class="sxs-lookup"><span data-stu-id="3285f-146">For this example, select the desired LCS project.</span></span> <span data-ttu-id="3285f-147">Jums ir nepieciešama [piekļuve](#accessconditions) šim projektam.</span><span class="sxs-lookup"><span data-stu-id="3285f-147">You must have [access](#accessconditions) to the project.</span></span>

8. <span data-ttu-id="3285f-148">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3285f-148">Select **OK**.</span></span>

    <span data-ttu-id="3285f-149">Pabeidziet jauna repozitorija ierakstu.</span><span class="sxs-lookup"><span data-stu-id="3285f-149">Complete a new repository entry.</span></span>

9. <span data-ttu-id="3285f-150">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="3285f-150">In the list, mark the selected row.</span></span>

    <span data-ttu-id="3285f-151">Šajā piemērā atlasiet **LCS** repozitorija ierakstu.</span><span class="sxs-lookup"><span data-stu-id="3285f-151">For this example, select the **LCS** repository record.</span></span>

    <span data-ttu-id="3285f-152">Ievērojiet, ka reģistrēto repozitoriju ir iezīmējis pašreizējais nodrošinātājs.</span><span class="sxs-lookup"><span data-stu-id="3285f-152">Note that a registered repository is marked by the current provider.</span></span> <span data-ttu-id="3285f-153">Citiem vārdiem, tikai konfigurācijas, kas pieder šim nodrošinātājam, var tikt ievietotas šajā repozitorijā un tāpēc augšupielādētas atlasītajā LCS projektā.</span><span class="sxs-lookup"><span data-stu-id="3285f-153">In other words, only configurations that are owned by that provider can be put in this repository and therefore uploaded into the selected LCS project.</span></span>

10. <span data-ttu-id="3285f-154">Atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="3285f-154">Select **Open**.</span></span>

    <span data-ttu-id="3285f-155">Atverat repozitoriju, lai skatītu sarakstu ar ER konfigurācijām.</span><span class="sxs-lookup"><span data-stu-id="3285f-155">You open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="3285f-156">Ja atlasītais projekts vēl nav lietots ER konfigurāciju koplietošanai, saraksts būs tukšs.</span><span class="sxs-lookup"><span data-stu-id="3285f-156">If the selected project hasn't yet been used for ER configurations sharing, the list will be empty.</span></span>

11. <span data-ttu-id="3285f-157">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3285f-157">Close the page.</span></span>
12. <span data-ttu-id="3285f-158">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3285f-158">Close the page.</span></span>

## <a name="upload-a-configuration-into-lcs"></a><span data-ttu-id="3285f-159">Konfigurācijas augšupielāde pakalpojumā LCS</span><span class="sxs-lookup"><span data-stu-id="3285f-159">Upload a configuration into LCS</span></span>

1. <span data-ttu-id="3285f-160">Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="3285f-160">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="3285f-161">Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Modeļa konfigurācijas paraugs**.</span><span class="sxs-lookup"><span data-stu-id="3285f-161">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="3285f-162">Ir jāatlasa izveidota konfigurācija, kas jau ir pabeigta.</span><span class="sxs-lookup"><span data-stu-id="3285f-162">You must select a created configuration that has been already completed.</span></span>

3. <span data-ttu-id="3285f-163">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="3285f-163">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="3285f-164">Šajā piemērā atlasiet atlasītās konfigurācijas versiju, kuras statuss ir **Pabaigts**.</span><span class="sxs-lookup"><span data-stu-id="3285f-164">For this example, select the version of the selected configuration that has a status of **Completed**.</span></span>

4. <span data-ttu-id="3285f-165">Atlasiet **Mainīt statusu**.</span><span class="sxs-lookup"><span data-stu-id="3285f-165">Select **Change status**.</span></span>
5. <span data-ttu-id="3285f-166">Atlasiet **Koplietot**.</span><span class="sxs-lookup"><span data-stu-id="3285f-166">Select **Share**.</span></span>

    <span data-ttu-id="3285f-167">Konfigurācijas statuss tiek mainīts no **Pabeigts** uz **Koplietots** , kad konfigurācija tiek publicēta LCS.</span><span class="sxs-lookup"><span data-stu-id="3285f-167">The status of the configuration is changed from **Completed** to **Shared** when the configuration is published in LCS.</span></span>

6. <span data-ttu-id="3285f-168">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3285f-168">Select **OK**.</span></span>
7. <span data-ttu-id="3285f-169">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="3285f-169">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="3285f-170">Šajā piemērā atlasiet konfigurācijas versiju, kuras statuss ir **Koplietots**.</span><span class="sxs-lookup"><span data-stu-id="3285f-170">For this example, select the configuration version that has a status of **Shared**.</span></span>

    <span data-ttu-id="3285f-171">Ņemiet vērā, ka atlasītās versijas statuss no **Pabeigts** ir mainīts uz **Koplietots**.</span><span class="sxs-lookup"><span data-stu-id="3285f-171">Note that the status of the selected version was changed from **Completed** to **Shared**.</span></span>

8. <span data-ttu-id="3285f-172">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3285f-172">Close the page.</span></span>
9. <span data-ttu-id="3285f-173">Atlasiet **Repozitoriji**.</span><span class="sxs-lookup"><span data-stu-id="3285f-173">Select **Repositories**.</span></span>

    <span data-ttu-id="3285f-174">Tagad var atvērt sarakstu ar repozitorijiem, kas paredzēti Litware, Inc. konfigurācijas nodrošinātājam.</span><span class="sxs-lookup"><span data-stu-id="3285f-174">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

10. <span data-ttu-id="3285f-175">Atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="3285f-175">Select **Open**.</span></span>

    <span data-ttu-id="3285f-176">Šajā piemērā atlasiet **LCS** repozitoriju un atveriet to.</span><span class="sxs-lookup"><span data-stu-id="3285f-176">For this example, select the **LCS** repository, and open it.</span></span>

    <span data-ttu-id="3285f-177">Ievērojiet, ka atlasītā konfigurācija tiek rādīta kā atlasītā LCS projekta līdzeklis.</span><span class="sxs-lookup"><span data-stu-id="3285f-177">Notice that the selected configuration is shown as an asset of the selected LCS project.</span></span>

11. <span data-ttu-id="3285f-178">Atvēriet LCS, pārejot uz <https://lcs.dynamics.com>.</span><span class="sxs-lookup"><span data-stu-id="3285f-178">Open LCS by going to <https://lcs.dynamics.com>.</span></span>
12. <span data-ttu-id="3285f-179">Atvēriet projektu, kas iepriekš tika izmantots repozitorija reģistrācijai.</span><span class="sxs-lookup"><span data-stu-id="3285f-179">Open a project that was used earlier for repository registration.</span></span>
13. <span data-ttu-id="3285f-180">Atveriet projekta līdzekļu bibliotēku.</span><span class="sxs-lookup"><span data-stu-id="3285f-180">Open the Asset library of the project.</span></span>
14. <span data-ttu-id="3285f-181">Atlasiet **GER konfigurācija** līdzekļa veidu.</span><span class="sxs-lookup"><span data-stu-id="3285f-181">Select the **GER configuration** asset type.</span></span>

    <span data-ttu-id="3285f-182">Ir jāuzskaita jūsu augšupielādētā ER konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="3285f-182">The ER configuration that you uploaded should be listed.</span></span>

    <span data-ttu-id="3285f-183">Ņemiet vērā, ka augšupielādēto LCS konfigurāciju var importēt citā instancē, ja nodrošinātājiem ir piekļuve šim LCS projektam.</span><span class="sxs-lookup"><span data-stu-id="3285f-183">Note that the uploaded LCS configuration can be imported into another instance if providers have access to this LCS project.</span></span>
