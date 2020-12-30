---
title: Importēt konfigurāciju no Lifecycle Services
description: Šajā tēmā ir izskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var importēt jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācijas versiju no Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c43cdce8d073f04a3158c8beb13a5376e669a4c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684455"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="5acbf-103">Importēt konfigurāciju no Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="5acbf-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5acbf-104">Šajā tēmā ir izskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var importēt jaunu [Elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācija](../general-electronic-reporting.md#Configuration) versiju no [projekta līmeņa līdzekļu bibliotēka](../../lifecycle-services/asset-library.md) Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="5acbf-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="5acbf-105">Šajā piemērā jūs atlasīsiet vēlamo ER konfigurācijas versiju un importēsiet to parauga uzņēmumam ar nosaukumu Litware, Inc. Šīs darbības var pabeigt jebkurā uzņēmumā, jo ER konfigurācijas tiek koplietotas visos uzņēmumos.</span><span class="sxs-lookup"><span data-stu-id="5acbf-105">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="5acbf-106">Lai izpildītu šīs darbības, jums vispirms ir jāizpilda procedūras [Augšupielādēt ER konfigurāciju pakalpojumos Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="5acbf-106">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="5acbf-107">Ir nepieciešama arī piekļuve LCS.</span><span class="sxs-lookup"><span data-stu-id="5acbf-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="5acbf-108">Pierakstieties programmā, izmantojot vienu no šīm lomām:</span><span class="sxs-lookup"><span data-stu-id="5acbf-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="5acbf-109">Elektroniskā pārskata izstrādātājs</span><span class="sxs-lookup"><span data-stu-id="5acbf-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="5acbf-110">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="5acbf-110">System administrator</span></span>

2. <span data-ttu-id="5acbf-111">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="5acbf-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="5acbf-112">Atlasiet **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="5acbf-112">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="5acbf-113">Pārliecinieties, vai pašreizējais Dynamics 365 Finance lietotājs ir tāda LCS projekta biedrs, kurā ir ietverta tā līdzekļu bibliotēka, kurai lietotājs vēlas [piekļūt](../../lifecycle-services/asset-library.md#asset-library-support) , lai importētu ER konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="5acbf-113">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="5acbf-114">Jūs nevarat piekļūt LCS projektam no ER repozitorija, kas pārstāv citu domēnu, nevis to domēnu, kas tiek izmantots programmā Finance.</span><span class="sxs-lookup"><span data-stu-id="5acbf-114">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="5acbf-115">Ja jūs mēģināt, tiks rādīts tukšs LCS projektu saraksts, un jūs nevarēsiet importēt ER konfigurācijas no projekta līmeņa līdzekļu bibliotēkas uz LCS.</span><span class="sxs-lookup"><span data-stu-id="5acbf-115">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="5acbf-116">Lai piekļūtu projekta līmeņa līdzekļu bibliotēkām no ER repozitorija, kas tiek izmantots, lai importētu ER konfigurācijas, piesakieties programmai Finance, izmantojot lietotāja akreditācijas datus, kas pieder nomniekam (domēns), kam ir nodrošināta pašreizējā Finance instance.</span><span class="sxs-lookup"><span data-stu-id="5acbf-116">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="5acbf-117">Dzēst koplietotu datu modeļa konfigurācijas versiju</span><span class="sxs-lookup"><span data-stu-id="5acbf-117">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="5acbf-118">Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Modeļa konfigurācijas paraugs**.</span><span class="sxs-lookup"><span data-stu-id="5acbf-118">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="5acbf-119">Jūs izveidojāt parauga datu modeļa konfigurācijas pirmo versiju un publicējāt to LCS, kad pabeidzāt darbības [Augšupielādēt ER konfigurāciju pakalpojumos Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="5acbf-119">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="5acbf-120">Šajā procedūrā jūs dzēsīsiet to ER konfigurācijas versiju.</span><span class="sxs-lookup"><span data-stu-id="5acbf-120">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="5acbf-121">Vēlāk šajā tēmā šo versiju importēsit no LCS.</span><span class="sxs-lookup"><span data-stu-id="5acbf-121">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="5acbf-122">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="5acbf-122">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="5acbf-123">Šajā piemērā atlasiet konfigurācijas versiju, kuras statuss ir **Koplietots**.</span><span class="sxs-lookup"><span data-stu-id="5acbf-123">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="5acbf-124">Šis statuss norāda, ka konfigurācija ir publicēta pakalpojumos LCS.</span><span class="sxs-lookup"><span data-stu-id="5acbf-124">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="5acbf-125">Atlasiet **Mainīt statusu**.</span><span class="sxs-lookup"><span data-stu-id="5acbf-125">Select **Change status**.</span></span>
4. <span data-ttu-id="5acbf-126">Atlasiet **Pārtraukt**.</span><span class="sxs-lookup"><span data-stu-id="5acbf-126">Select **Discontinue**.</span></span>

    <span data-ttu-id="5acbf-127">Mainot atlasītās versijas statusu no **Koplietots** uz **Pārtraukts**, versiju padara pieejamu dzēšanai.</span><span class="sxs-lookup"><span data-stu-id="5acbf-127">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="5acbf-128">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5acbf-128">Select **OK**.</span></span>
6. <span data-ttu-id="5acbf-129">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="5acbf-129">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="5acbf-130">Šajā piemērā atlasiet konfigurācijas versiju, kuras statuss ir **Pārtraukts**.</span><span class="sxs-lookup"><span data-stu-id="5acbf-130">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="5acbf-131">Atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="5acbf-131">Select **Delete**.</span></span>
8. <span data-ttu-id="5acbf-132">Atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="5acbf-132">Select **Yes**.</span></span>

    <span data-ttu-id="5acbf-133">Ievērojiet, ka atlasītajai datu modeļa konfigurācijai tagad ir pieejama tikai melnraksta 2. versija.</span><span class="sxs-lookup"><span data-stu-id="5acbf-133">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="5acbf-134">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5acbf-134">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="5acbf-135">Importēt koplietotu datu modeļa konfigurācijas versiju no LCS</span><span class="sxs-lookup"><span data-stu-id="5acbf-135">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="5acbf-136">Dodieties uz **Organizācijas administrēšana \> Darbvietas \> Elektronisko atskaišu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="5acbf-136">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="5acbf-137">Sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="5acbf-137">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="5acbf-138">Elementā **Litware, Inc.** atlasiet **Repozitoriji**.</span><span class="sxs-lookup"><span data-stu-id="5acbf-138">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="5acbf-139">Tagad var atvērt sarakstu ar repozitorijiem, kas paredzēti Litware, Inc. konfigurācijas nodrošinātājam.</span><span class="sxs-lookup"><span data-stu-id="5acbf-139">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="5acbf-140">Atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="5acbf-140">Select **Open**.</span></span>

    <span data-ttu-id="5acbf-141">Šajā piemērā atlasiet **LCS** repozitoriju un atveriet to.</span><span class="sxs-lookup"><span data-stu-id="5acbf-141">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="5acbf-142">Jums ir jābūt [piekļuve](#accessconditions) LCS projektam un līdzekļu bibliotēkai, kuram var piekļūt atlasītais ER repozitorijs.</span><span class="sxs-lookup"><span data-stu-id="5acbf-142">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="5acbf-143">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="5acbf-143">In the list, mark the selected row.</span></span>

    <span data-ttu-id="5acbf-144">Šā piemēra versiju sarakstā atlasiet konfigurācijas **Parauga modeļa konfigurācija** pirmo versiju.</span><span class="sxs-lookup"><span data-stu-id="5acbf-144">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="5acbf-145">Atlasiet **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="5acbf-145">Select **Import**.</span></span>
7. <span data-ttu-id="5acbf-146">Atlasiet **Jā** , lai apstiprinātu atlasītās versijas importēšanu no LCS.</span><span class="sxs-lookup"><span data-stu-id="5acbf-146">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="5acbf-147">Informatīvs ziņojums apstiprina, ka atlasītā versija tika veiksmīgi importēta.</span><span class="sxs-lookup"><span data-stu-id="5acbf-147">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="5acbf-148">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5acbf-148">Close the page.</span></span>
9. <span data-ttu-id="5acbf-149">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5acbf-149">Close the page.</span></span>
10. <span data-ttu-id="5acbf-150">Atlasiet **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="5acbf-150">Select **Configurations**.</span></span>
11. <span data-ttu-id="5acbf-151">Koka struktūrā atlasiet **Parauga modeļa konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="5acbf-151">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="5acbf-152">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="5acbf-152">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="5acbf-153">Šajā piemērā atlasiet konfigurācijas versiju, kuras statuss ir **Koplietots**.</span><span class="sxs-lookup"><span data-stu-id="5acbf-153">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="5acbf-154">Ievērojiet, ka tagad atlasītajai datu modeļa konfigurācijai ir pieejama arī koplietotā 1. versija.</span><span class="sxs-lookup"><span data-stu-id="5acbf-154">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>
