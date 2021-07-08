---
title: Importēt konfigurāciju no Lifecycle Services
description: Šajā tēmā ir aprakstīts, kā no Microsoft Dynamics Lifecycle Services (LCS) importēt jaunu elektronisko pārskatu (ER) konfigurācijas versiju.
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b58ecb8a7d6f52631dbca7642a4acbcf6ff895a3
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270841"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="ac652-103">Importēt konfigurāciju no Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="ac652-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ac652-104">Šajā tēmā ir izskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var importēt jaunu [Elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācija](../general-electronic-reporting.md#Configuration) versiju no [projekta līmeņa līdzekļu bibliotēka](../../lifecycle-services/asset-library.md) Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="ac652-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ac652-105">LCS kā ER konfigurāciju glabāšanas repozitorija izmantošana ir [novecojusi](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="ac652-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="ac652-106">Papildinformāciju skatiet [Regulatory Configuration Service (RCS) — Lifecycle Services (LCS) krātuves nolietojums](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="ac652-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

<span data-ttu-id="ac652-107">Šajā piemērā jūs atlasīsiet vēlamo ER konfigurācijas versiju un importēsiet to parauga uzņēmumam ar nosaukumu Litware, Inc. Šīs darbības var pabeigt jebkurā uzņēmumā, jo ER konfigurācijas tiek koplietotas visos uzņēmumos.</span><span class="sxs-lookup"><span data-stu-id="ac652-107">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="ac652-108">Lai izpildītu šīs darbības, jums vispirms ir jāizpilda procedūras [Augšupielādēt ER konfigurāciju pakalpojumos Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="ac652-108">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="ac652-109">Ir nepieciešama arī piekļuve LCS.</span><span class="sxs-lookup"><span data-stu-id="ac652-109">Access to LCS is also required.</span></span>

1. <span data-ttu-id="ac652-110">Pierakstieties programmā, izmantojot vienu no šīm lomām:</span><span class="sxs-lookup"><span data-stu-id="ac652-110">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="ac652-111">Elektroniskā pārskata izstrādātājs</span><span class="sxs-lookup"><span data-stu-id="ac652-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="ac652-112">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="ac652-112">System administrator</span></span>

2. <span data-ttu-id="ac652-113">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="ac652-113">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="ac652-114">Atlasiet **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="ac652-114">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="ac652-115">Pārliecinieties, vai pašreizējais Dynamics 365 Finance lietotājs ir tāda LCS projekta biedrs, kurā ir ietverta tā līdzekļu bibliotēka, kurai lietotājs vēlas [piekļūt](../../lifecycle-services/asset-library.md#asset-library-support) , lai importētu ER konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="ac652-115">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="ac652-116">Jūs nevarat piekļūt LCS projektam no ER repozitorija, kas pārstāv citu domēnu, nevis to domēnu, kas tiek izmantots programmā Finance.</span><span class="sxs-lookup"><span data-stu-id="ac652-116">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="ac652-117">Ja jūs mēģināt, tiks rādīts tukšs LCS projektu saraksts, un jūs nevarēsiet importēt ER konfigurācijas no projekta līmeņa līdzekļu bibliotēkas uz LCS.</span><span class="sxs-lookup"><span data-stu-id="ac652-117">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="ac652-118">Lai piekļūtu projekta līmeņa līdzekļu bibliotēkām no ER repozitorija, kas tiek izmantots, lai importētu ER konfigurācijas, piesakieties programmai Finance, izmantojot lietotāja akreditācijas datus, kas pieder nomniekam (domēns), kam ir nodrošināta pašreizējā Finance instance.</span><span class="sxs-lookup"><span data-stu-id="ac652-118">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="ac652-119">Dzēst koplietotu datu modeļa konfigurācijas versiju</span><span class="sxs-lookup"><span data-stu-id="ac652-119">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="ac652-120">Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Modeļa konfigurācijas paraugs**.</span><span class="sxs-lookup"><span data-stu-id="ac652-120">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="ac652-121">Jūs izveidojāt parauga datu modeļa konfigurācijas pirmo versiju un publicējāt to LCS, kad pabeidzāt darbības [Augšupielādēt ER konfigurāciju pakalpojumos Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="ac652-121">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="ac652-122">Šajā procedūrā jūs dzēsīsiet to ER konfigurācijas versiju.</span><span class="sxs-lookup"><span data-stu-id="ac652-122">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="ac652-123">Vēlāk šajā tēmā šo versiju importēsit no LCS.</span><span class="sxs-lookup"><span data-stu-id="ac652-123">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="ac652-124">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="ac652-124">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="ac652-125">Šajā piemērā atlasiet konfigurācijas versiju, kuras statuss ir **Koplietots**.</span><span class="sxs-lookup"><span data-stu-id="ac652-125">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="ac652-126">Šis statuss norāda, ka konfigurācija ir publicēta pakalpojumos LCS.</span><span class="sxs-lookup"><span data-stu-id="ac652-126">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="ac652-127">Atlasiet **Mainīt statusu**.</span><span class="sxs-lookup"><span data-stu-id="ac652-127">Select **Change status**.</span></span>
4. <span data-ttu-id="ac652-128">Atlasiet **Pārtraukt**.</span><span class="sxs-lookup"><span data-stu-id="ac652-128">Select **Discontinue**.</span></span>

    <span data-ttu-id="ac652-129">Mainot atlasītās versijas statusu no **Koplietots** uz **Pārtraukts**, versiju padara pieejamu dzēšanai.</span><span class="sxs-lookup"><span data-stu-id="ac652-129">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="ac652-130">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ac652-130">Select **OK**.</span></span>
6. <span data-ttu-id="ac652-131">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="ac652-131">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="ac652-132">Šajā piemērā atlasiet konfigurācijas versiju, kuras statuss ir **Pārtraukts**.</span><span class="sxs-lookup"><span data-stu-id="ac652-132">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="ac652-133">Atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="ac652-133">Select **Delete**.</span></span>
8. <span data-ttu-id="ac652-134">Atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="ac652-134">Select **Yes**.</span></span>

    <span data-ttu-id="ac652-135">Ievērojiet, ka atlasītajai datu modeļa konfigurācijai tagad ir pieejama tikai melnraksta 2. versija.</span><span class="sxs-lookup"><span data-stu-id="ac652-135">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="ac652-136">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ac652-136">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="ac652-137">Importēt koplietotu datu modeļa konfigurācijas versiju no LCS</span><span class="sxs-lookup"><span data-stu-id="ac652-137">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="ac652-138">Dodieties uz **Organizācijas administrēšana \> Darbvietas \> Elektronisko atskaišu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="ac652-138">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="ac652-139">Sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="ac652-139">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="ac652-140">Elementā **Litware, Inc.** atlasiet **Repozitoriji**.</span><span class="sxs-lookup"><span data-stu-id="ac652-140">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="ac652-141">Tagad var atvērt sarakstu ar repozitorijiem, kas paredzēti Litware, Inc. konfigurācijas nodrošinātājam.</span><span class="sxs-lookup"><span data-stu-id="ac652-141">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="ac652-142">Atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="ac652-142">Select **Open**.</span></span>

    <span data-ttu-id="ac652-143">Šajā piemērā atlasiet **LCS** repozitoriju un atveriet to.</span><span class="sxs-lookup"><span data-stu-id="ac652-143">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="ac652-144">Jums ir jābūt [piekļuve](#accessconditions) LCS projektam un līdzekļu bibliotēkai, kuram var piekļūt atlasītais ER repozitorijs.</span><span class="sxs-lookup"><span data-stu-id="ac652-144">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="ac652-145">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="ac652-145">In the list, mark the selected row.</span></span>

    <span data-ttu-id="ac652-146">Šā piemēra versiju sarakstā atlasiet konfigurācijas **Parauga modeļa konfigurācija** pirmo versiju.</span><span class="sxs-lookup"><span data-stu-id="ac652-146">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="ac652-147">Atlasiet **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="ac652-147">Select **Import**.</span></span>
7. <span data-ttu-id="ac652-148">Atlasiet **Jā** , lai apstiprinātu atlasītās versijas importēšanu no LCS.</span><span class="sxs-lookup"><span data-stu-id="ac652-148">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="ac652-149">Informatīvs ziņojums apstiprina, ka atlasītā versija tika veiksmīgi importēta.</span><span class="sxs-lookup"><span data-stu-id="ac652-149">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="ac652-150">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ac652-150">Close the page.</span></span>
9. <span data-ttu-id="ac652-151">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ac652-151">Close the page.</span></span>
10. <span data-ttu-id="ac652-152">Atlasiet **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="ac652-152">Select **Configurations**.</span></span>
11. <span data-ttu-id="ac652-153">Koka struktūrā atlasiet **Parauga modeļa konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="ac652-153">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="ac652-154">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="ac652-154">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="ac652-155">Šajā piemērā atlasiet konfigurācijas versiju, kuras statuss ir **Koplietots**.</span><span class="sxs-lookup"><span data-stu-id="ac652-155">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="ac652-156">Ievērojiet, ka tagad atlasītajai datu modeļa konfigurācijai ir pieejama arī koplietotā 1. versija.</span><span class="sxs-lookup"><span data-stu-id="ac652-156">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
