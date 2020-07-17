---
title: Atjaunināto ER konfigurāciju versiju importēšana
description: Šajā tēmā ir paskaidrots, kā importēt atjauninātās elektronisko pārskatu (ER) konfigurāciju versijas no konfigurācijas pakalpojuma globālā repozitorija.
author: NickSelin
manager: AnnBe
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4f167a0209713b5bca0cefe0135abd46a149a515
ms.sourcegitcommit: 1e6a7b50596eaf9d965e0155f3f2c50f7f50747e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/22/2020
ms.locfileid: "3498104"
---
# <a name="import-updated-versions-of-er-configurations"></a><span data-ttu-id="bb9f5-103">Atjaunināto ER konfigurāciju versiju importēšana</span><span class="sxs-lookup"><span data-stu-id="bb9f5-103">Import updated versions of ER configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb9f5-104">Elektroniskā pārskata (ER) [repozitoriji](general-electronic-reporting.md#Repository) tiek izmantoti, lai koplietotu [ER konfigurācijas](general-electronic-reporting.md#Configuration).</span><span class="sxs-lookup"><span data-stu-id="bb9f5-104">Electronic reporting (ER) [repositories](general-electronic-reporting.md#Repository) are used to share [ER configurations](general-electronic-reporting.md#Configuration).</span></span> <span data-ttu-id="bb9f5-105">Varat [importēt](download-electronic-reporting-configuration-lcs.md) ER konfigurācijas no dažādiem repozitorijiem savā Microsoft Dynamics 365 Finance instancē.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-105">You can [import](download-electronic-reporting-configuration-lcs.md) ER configurations from different repositories into your instance of Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="bb9f5-106">Importējot ER konfigurācijas, [konfigurācijas nodrošinātāji](general-electronic-reporting.md#Provider) var publicēt jaunas [versijas](general-electronic-reporting.md#component-versioning) repozitorijus, lai tos varētu koplietot.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-106">When you import ER configurations, [configuration providers](general-electronic-reporting.md#Provider) can publish new [versions](general-electronic-reporting.md#component-versioning) repositories so that they can be shared.</span></span>

<span data-ttu-id="bb9f5-107">Šajā tēmā ir paskaidrots, kā importēt atjauninātās ER konfigurāciju versijas no konfigurācijas pakalpojuma globālā repozitorija.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-107">This topic explains how to import updated versions of ER configurations from the Global repository of the Configuration service.</span></span> <span data-ttu-id="bb9f5-108">Plašāku informāciju skatiet [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, konfigurācijas pakalpojums](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span><span class="sxs-lookup"><span data-stu-id="bb9f5-108">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="review-the-available-updated-versions"></a><span data-ttu-id="bb9f5-109">Pieejamo atjaunināto versiju pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="bb9f5-109">Review the available updated versions</span></span>

1. <span data-ttu-id="bb9f5-110">Pierakstieties programmatūrā Finance, izmantojot vienu no šīm lomām:</span><span class="sxs-lookup"><span data-stu-id="bb9f5-110">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="bb9f5-111">Elektroniskā pārskata izstrādātājs</span><span class="sxs-lookup"><span data-stu-id="bb9f5-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="bb9f5-112">Elektronisko pārskatu veidošanas funkcionālais konsultants</span><span class="sxs-lookup"><span data-stu-id="bb9f5-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="bb9f5-113">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="bb9f5-113">System administrator</span></span>

2. <span data-ttu-id="bb9f5-114">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-114">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="bb9f5-115">Lapas **Lokalizācijas konfigurācijas** sadaļā **Saistītās saites** atlasiet **Importēt konfigurāciju versiju atjauninājumus**.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-115">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>

    ![Lokalizācijas konfigurāciju lapa](./media/er-download-updated-versions-global-repo1.png)

4. <span data-ttu-id="bb9f5-117">Dialoglodziņa **Importēt elektronisko pārskatu konfigurāciju versiju atjauninājumus** laukā **Izpildes režīms** atlasiet **Tikai pieejamos atjauninājumus**.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-117">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Only show available updates**.</span></span> <span data-ttu-id="bb9f5-118">Tad atl. **Labi**.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-118">Then select **OK**.</span></span> 

    ![Izpildes režīma lauks iestatīts uz Tikai pieejamos atjauninājumus](./media/er-download-updated-versions-global-repo2.png)

5. <span data-ttu-id="bb9f5-120">Pārskatiet saņemtos ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-120">Review the messages that you receive.</span></span> <span data-ttu-id="bb9f5-121">Šie ziņojumi sniedz tālāk norādīto informāciju par ER konfigurācijām pašreizējā Finance instancē un to, kā tās salīdzināt ar globālā repozitorija saturu:</span><span class="sxs-lookup"><span data-stu-id="bb9f5-121">These messages provide the following information about the ER configurations in the current Finance instance and how they compare to the content of the Global repository:</span></span>

    - <span data-ttu-id="bb9f5-122">Kopējais ER konfigurāciju skaits</span><span class="sxs-lookup"><span data-stu-id="bb9f5-122">The total number of ER configurations</span></span>
    - <span data-ttu-id="bb9f5-123">ER konfigurācijas, kas neatrodas globālajā repozitorijā</span><span class="sxs-lookup"><span data-stu-id="bb9f5-123">ER configurations that aren't present in the Global repository</span></span>
    - <span data-ttu-id="bb9f5-124">ER konfigurācijas, kurām jaunākā versija jau ir pieejama pašreizējā Finance instancē (skatiet visu ER konfigurāciju sarakstu, atlasot saiti **Ziņojuma informācija**.)</span><span class="sxs-lookup"><span data-stu-id="bb9f5-124">ER configurations for which the latest version is already available in the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![“Šo konfigurāciju jaunākās versijas jau ir importētas” ziņojums un ziņojuma informācija](./media/er-download-updated-versions-global-repo3.png)

    - <span data-ttu-id="bb9f5-126">ER konfigurācijas, kurām jaunākā versija jau ir pieejama globālajā repozitorijā un var tikt importēta pašreizējā Finance instancē (skatiet visu ER konfigurāciju sarakstu, atlasot saiti **Ziņojuma informācija**.)</span><span class="sxs-lookup"><span data-stu-id="bb9f5-126">ER configurations for which the latest version is available in the Global repository and can be imported into the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![“Pieejamie atjauninājumi” ziņojums un ziņojuma informācija](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a><span data-ttu-id="bb9f5-128">Pieejamo atjaunināto versiju importēšana</span><span class="sxs-lookup"><span data-stu-id="bb9f5-128">Import available updated versions</span></span>

1. <span data-ttu-id="bb9f5-129">Pierakstieties programmatūrā Finance, izmantojot vienu no šīm lomām:</span><span class="sxs-lookup"><span data-stu-id="bb9f5-129">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="bb9f5-130">Elektroniskā pārskata izstrādātājs</span><span class="sxs-lookup"><span data-stu-id="bb9f5-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="bb9f5-131">Elektronisko pārskatu veidošanas funkcionālais konsultants</span><span class="sxs-lookup"><span data-stu-id="bb9f5-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="bb9f5-132">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="bb9f5-132">System administrator</span></span>

2. <span data-ttu-id="bb9f5-133">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-133">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="bb9f5-134">Lapas **Lokalizācijas konfigurācijas** sadaļā **Saistītās saites** atlasiet **Importēt konfigurāciju versiju atjauninājumus**.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-134">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>
4. <span data-ttu-id="bb9f5-135">Dialoglodziņa **Importēt elektronisko pārskatu konfigurāciju versiju atjauninājumus** laukā **Izpildes režīms** atlasiet **Importēt jaunākos atjauninājumus**, lai importētu ER konfigurācijas jaunākās versijas no globālā repozitorija pašreizējā Finance instancē.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-135">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Import latest updates** to import the latest versions of ER configurations from the Global repository into the current Finance instance.</span></span>
5. <span data-ttu-id="bb9f5-136">Lai ieplānotu pakešuzdevumu importēšanai, kopsavilkuma cilnē **Palaist fonā** iestatiet opciju **Pakešapstrāde** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-136">To schedule a batch job for the import, on the **Run in the background** FastTab, set the **Batch processing** option to **Yes**.</span></span> <span data-ttu-id="bb9f5-137">Importēšanu var atkārtot periodiski, konfigurējot nepieciešamo periodiskumu.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-137">If you want to repeat the import periodically, configure the required recurrence.</span></span>

    ![Izpildes režīma lauks iestatīts uz Importēt jaunākos atjauninājumus](./media/er-download-updated-versions-global-repo5.png)

6. <span data-ttu-id="bb9f5-139">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-139">Select **OK**.</span></span>
7. <span data-ttu-id="bb9f5-140">Lai uzzinātu, kādas konfigurāciju versijas ir importētas, veiciet vienu no šīm darbībām:</span><span class="sxs-lookup"><span data-stu-id="bb9f5-140">To learn what configuration versions have been imported, follow one of these steps:</span></span>

    - <span data-ttu-id="bb9f5-141">Ja importēšana tiek veikta interaktīvi, neizmantojot pakešuzdevumu, pārskatiet saņemtos ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-141">If you run the import interactively instead of using a batch job, review the messages that you receive.</span></span>

        ![Interaktīvās importēšanas laikā saņemtie ziņojumi](./media/er-download-updated-versions-global-repo6.png)

    - <span data-ttu-id="bb9f5-143">Ja importēšana tiek veikta pakešveida režīmā, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="bb9f5-143">If you run the import in batch mode, follow these steps:</span></span>

        1. <span data-ttu-id="bb9f5-144">Dodieties uz **Vispārīgi** \> **Pieprasījumi** \> **Pakešuzdevumi** \> **Mani pakešuzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-144">Go to **Common** \> **Inquiries** \> **Batch jobs** \> **My batch jobs**.</span></span>
        2. <span data-ttu-id="bb9f5-145">Meklējiet un atlasiet **Importēt elektronisko pārskatu konfigurāciju versiju atjauninājumus** darbu un pēc tam darbību rūts cilnē **Pakešuzdevums** atlasiet **Pakešuzdevumu vēsture**, lai skatītu darba vēsturi.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-145">Find and select the **Import electronic reporting configurations versions updates** job, and then, on the Action Pane, on the **Batch job** tab, select **Batch job history** to view the job history.</span></span>
        3. <span data-ttu-id="bb9f5-146">Lapā **Pakešuzdevumu vēsture** atlasiet **Žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-146">On the **Batch job history** page, select **Log**.</span></span> <span data-ttu-id="bb9f5-147">Tad, saņemtajā ziņojumā atlasiet **Ziņojuma informācija**, lai skatītu darbu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-147">Then, in the message that you receive, select the **Message details** link to view the job log.</span></span>

        ![Darbu žurnāls](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> <span data-ttu-id="bb9f5-149">Nav ieteicams ieplānot periodisku pakešuzdevumu, lai importētu atjauninātās ER konfigurāciju versijas tieši no globālā repozitorija ražošanas vidē, jo importētās versijas nekavējoties būs pieejamas lietošanai.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-149">We don't recommend that you schedule a recurring batch job to import updated versions of ER configurations directly from the Global repository into a production environment, because the imported versions will immediately be available for use.</span></span> <span data-ttu-id="bb9f5-150">Tā vietā izmantojiet iespēju ER konfigurāciju versijas izvietot smilškastes vidē.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-150">Instead, use this approach to deploy versions of ER configurations to a sandbox environment.</span></span> <span data-ttu-id="bb9f5-151">Pēc tam tos var novērtēt smilškastes vidē, pirms tie tiek izvietoti ražošanas vidē.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-151">They can then be evaluated in the sandbox environment before they are deployed to a production environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bb9f5-152">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="bb9f5-152">Additional resources</span></span>

- [<span data-ttu-id="bb9f5-153">Elektronisko pārskatu veidošanas (ER) apskats</span><span class="sxs-lookup"><span data-stu-id="bb9f5-153">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="bb9f5-154">Elektronisko pārskatu (ER) konfigurāciju lejupielāde no konfigurācijas pakalpojuma globālā repozitorija</span><span class="sxs-lookup"><span data-stu-id="bb9f5-154">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)
