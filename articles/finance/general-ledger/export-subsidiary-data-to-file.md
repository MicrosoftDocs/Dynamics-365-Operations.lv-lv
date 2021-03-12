---
title: Filiāļu datu eksportēšana uz failiem
description: Šajā tēmā skaidrots, kā sagatavoties eksportēt datus no Microsoft Dynamics 365 Finance un pēc tam importēt tos konsolidētā juridiskajā personā.
author: jinniew
manager: AnnBe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 179a401178935b8a76d6718a7fb1f63e08344f50
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968683"
---
# <a name="export-subsidiary-data-to-files"></a><span data-ttu-id="32025-103">Filiāļu datu eksportēšana uz failiem</span><span class="sxs-lookup"><span data-stu-id="32025-103">Export subsidiary data to files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32025-104">Jūs izmantojat lapu **Eksportēt** (**Sistēmas administrēšana \> Darbvietas \>Importēt/eksportēt**), lai sagatavotu filiāli datu eksportēšanai uz failiem, kurus pēc tam var importēt konsolidētā juridiskajā personā.</span><span class="sxs-lookup"><span data-stu-id="32025-104">You use the **Export** page (**System administration \> Workspaces \> Import/Export**) to prepare to export subsidiary data to files that can then be imported into a consolidated legal entity.</span></span> <span data-ttu-id="32025-105">Papildinformāciju par importēšanas un eksportēšanas procesiem skatiet [Datu importēšanas un eksportēšanas darbu apskatā](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="32025-105">For more information about the import and export processes, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>

1. <span data-ttu-id="32025-106">Juridiskas personas izveidošana konsolidācijas procesam.</span><span class="sxs-lookup"><span data-stu-id="32025-106">Create a legal entity for the consolidation process.</span></span> <span data-ttu-id="32025-107">Informāciju par to, kā izveidot juridiskās personas, skatiet sadaļā [Juridiskas personas izveidošana](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span><span class="sxs-lookup"><span data-stu-id="32025-107">For information about how to create legal entities, see [Create a legal entity](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span></span> <span data-ttu-id="32025-108">Papildinformāciju skatiet sadaļās [Juridiskas personas sagatavošana izmantošanai konsolidācijas procesā](prepare-company-for-consolidation.md) un [Meitasuzņēmuma juridiskās personas konsolidācijas iestatīšana](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="32025-108">For more information, see [Prepare a legal entity for use in the consolidation process](prepare-company-for-consolidation.md) and [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span> 

2. <span data-ttu-id="32025-109">Dodieties uz **Konsolidācijas \> Eksportēt uzņēmuma bilances**.</span><span class="sxs-lookup"><span data-stu-id="32025-109">Go to **Consolidations \> Export company balances**.</span></span> <span data-ttu-id="32025-110">Lapas **Eksportēt uzņēmuma bilances** cilnē **Kritēriji** norādiet informāciju par konsolidāciju, iestatot tālāk esošos laukus.</span><span class="sxs-lookup"><span data-stu-id="32025-110">On the **Export company balances** page, on the **Criteria** tab, specify the details of the consolidation by setting the following fields.</span></span>

    | <span data-ttu-id="32025-111">Lauks</span><span class="sxs-lookup"><span data-stu-id="32025-111">Field</span></span>                             | <span data-ttu-id="32025-112">Apraksts</span><span class="sxs-lookup"><span data-stu-id="32025-112">Description</span></span> |
    |-----------------------------------|-------|
    | <span data-ttu-id="32025-113">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="32025-113">Main account</span></span>                      | <span data-ttu-id="32025-114">Norādiet konsolidācijas kontus.</span><span class="sxs-lookup"><span data-stu-id="32025-114">Specify the accounts to consolidate.</span></span> <span data-ttu-id="32025-115">Lai iekļautu visus kontus, atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="32025-115">To include all accounts, leave this field blank.</span></span> |
    | <span data-ttu-id="32025-116">Izmantot šādu konsolidācijas kontu</span><span class="sxs-lookup"><span data-stu-id="32025-116">Use consolidation account</span></span>         | <span data-ttu-id="32025-117">Ja esat norādījuši konsolidācijas kontus, iestatiet šo opciju uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="32025-117">If you've specified consolidation accounts, set this option to **Yes**.</span></span> |
    | <span data-ttu-id="32025-118">Atlasīt konsolidācijas kontu no</span><span class="sxs-lookup"><span data-stu-id="32025-118">Select consolidation account from</span></span> | <span data-ttu-id="32025-119">Atlasiet **Galveno kontu** vai **Konsolidācijas kontu grupu**.</span><span class="sxs-lookup"><span data-stu-id="32025-119">Select either **Main account** or **Consolidation account group**.</span></span> |
    | <span data-ttu-id="32025-120">Konsolidācijas kontu grupa</span><span class="sxs-lookup"><span data-stu-id="32025-120">Consolidation account group</span></span>       | <span data-ttu-id="32025-121">Izvēlieties konsolidācijas kontu grupu izvēlētajam konsolidācijas kontam.</span><span class="sxs-lookup"><span data-stu-id="32025-121">Select a consolidation account group for the consolidation account that you selected.</span></span> |
    | <span data-ttu-id="32025-122">Konsolidācijas periods</span><span class="sxs-lookup"><span data-stu-id="32025-122">Consolidation period</span></span>              | <span data-ttu-id="32025-123">Norādiet konsolidācijas "no" un "līdz" datumus.</span><span class="sxs-lookup"><span data-stu-id="32025-123">Specify "from" and "to" dates for the consolidation.</span></span> |
    | <span data-ttu-id="32025-124">Ietvert faktiskās summas</span><span class="sxs-lookup"><span data-stu-id="32025-124">Include actual amounts</span></span>            | <span data-ttu-id="32025-125">Iestatiet šo opciju uz **Jā**, lai iekļautu faktiskos kontus.</span><span class="sxs-lookup"><span data-stu-id="32025-125">Set this option to **Yes** to include actual amounts.</span></span> |
    | <span data-ttu-id="32025-126">Ietvert budžeta summas</span><span class="sxs-lookup"><span data-stu-id="32025-126">Include budget amounts</span></span>            | <span data-ttu-id="32025-127">Iestatiet šo opciju uz **Jā**, lai ietvertu budžeta summas konsolidācijās.</span><span class="sxs-lookup"><span data-stu-id="32025-127">Set this option to **Yes** to include budget amounts in consolidations.</span></span> |
    | <span data-ttu-id="32025-128">Budžeta modeļi</span><span class="sxs-lookup"><span data-stu-id="32025-128">Budget models</span></span>                     | <span data-ttu-id="32025-129">Norādiet iekļaujamā budžeta modeli.</span><span class="sxs-lookup"><span data-stu-id="32025-129">Specify the budget model to include.</span></span> |

3. <span data-ttu-id="32025-130">Cilnē **Finanšu dimensijas** norādiet konsolidācijas datus:</span><span class="sxs-lookup"><span data-stu-id="32025-130">On the **Financial dimensions** tab, specify the details of the consolidation:</span></span>

    - <span data-ttu-id="32025-131">Norādiet finanšu dimensiju informāciju, kam jābūt pārsūtītai no meitasuzņēmuma kontu darījumiem uz darījumiem konsolidētajā juridiskajā personā.</span><span class="sxs-lookup"><span data-stu-id="32025-131">Specify the financial dimension information that should be transferred from the transactions in the subsidiary accounts to the transactions in the consolidated legal entity.</span></span>
    - <span data-ttu-id="32025-132">Atlasiet finanšu dimensijas sarakstā.</span><span class="sxs-lookup"><span data-stu-id="32025-132">Select financial dimensions in the list.</span></span>
    - <span data-ttu-id="32025-133">Norādiet pareizu specifikāciju katrai konsolidētai finanšu dimensijai.</span><span class="sxs-lookup"><span data-stu-id="32025-133">Identify the correct specification for each financial dimension that is consolidated.</span></span> <span data-ttu-id="32025-134">Pieejamās opcijas ietver **Dimensiju**, **Grupas dimensiju**, **Uzņēmuma kontus** un **Kontu**.</span><span class="sxs-lookup"><span data-stu-id="32025-134">The available options include **Dimension**, **Group dimension**, **Company accounts**, and **Account**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="32025-135">**Grupas dimensijas** opcija ļauj definēt dimensijas vērtību, ko izmanto uzņēmumu grupa, kas tiek konsolidēta.</span><span class="sxs-lookup"><span data-stu-id="32025-135">The **Group dimension** option lets you define the dimension value that is used by the group of companies that is being consolidated.</span></span>

    - <span data-ttu-id="32025-136">Norādiet konsolidējamo segmenta pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="32025-136">Specify the segment order to consolidate in.</span></span>

4. <span data-ttu-id="32025-137">Cilnē **Juridiskās personas** izpildiet šos soļus, lai norādītu juridisko personu, kuru eksportējat:</span><span class="sxs-lookup"><span data-stu-id="32025-137">On the **Legal entities** tab, follow these steps to specify the legal entity that you're exporting:</span></span>

    1. <span data-ttu-id="32025-138">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="32025-138">Select **New**.</span></span>
    2. <span data-ttu-id="32025-139">Laukā **Avota juridiskā persona** ievadiet juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="32025-139">In the **Source legal entity** field, enter the legal entity.</span></span>

        <span data-ttu-id="32025-140">Ja vairākiem meitasuzņēmumiem, kas atrodas vienā datu bāzē, atbilst tie paši kritēriji, ir iespējams pārsūtīt datus no šiem meitasuzņēmumiem uz atsevišķiem eksporta failiem vienā transakcijā:</span><span class="sxs-lookup"><span data-stu-id="32025-140">If the same criteria apply to several subsidiaries that are in the same database, you can transfer data from those subsidiaries to separate export files in a single operation:</span></span>

        1. <span data-ttu-id="32025-141">Izveidojiet rindu katrai meitasuzņēmuma juridiskajai iestādei, kuras konti tiks eksportēti uz failiem.</span><span class="sxs-lookup"><span data-stu-id="32025-141">Create a line for each subsidiary legal entity for which accounts should be exported to files.</span></span> <span data-ttu-id="32025-142">Šie faili vēlāk tiks importēti konsolidētajā juridiskajā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="32025-142">These files will be imported into the consolidated legal entity later.</span></span>
        2. <span data-ttu-id="32025-143">Katrai filiālei ievadiet filiāles nosaukumu un eksporta faila nosaukumu, kurš tiks izveidots eksporta uzdevuma veikšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="32025-143">For each subsidiary, enter the subsidiary name and the name of the export file that will be created during the export job.</span></span>

    3. <span data-ttu-id="32025-144">Laukā **Konvertēšanas starpības konta tips** atlasiet **Peļņa un zaudējumi** vai **Bilance**.</span><span class="sxs-lookup"><span data-stu-id="32025-144">In **Account type of conversion differences** field, Select **Profit and loss** or **Balance sheet**.</span></span>
    4. <span data-ttu-id="32025-145">Ievadiet nosaukumu eksporta failam, kas tiks izveidots.</span><span class="sxs-lookup"><span data-stu-id="32025-145">Enter a file name for the export file that will be created.</span></span>

5. <span data-ttu-id="32025-146">Atlasiet **Labi**, lai palaistu eksportu.</span><span class="sxs-lookup"><span data-stu-id="32025-146">Select **OK** to run the export.</span></span>

<span data-ttu-id="32025-147">Kad eksports ir pabeigts, parādās ziņojums, kas uzskaita ierakstu daudzumu, kas tikuši saglabāti katrā failā.</span><span class="sxs-lookup"><span data-stu-id="32025-147">When the export is completed, you receive a message that shows the number of records that were saved in each file.</span></span> <span data-ttu-id="32025-148">Pēc tam failus varat importēt konsolidētajā juridiskajā personā.</span><span class="sxs-lookup"><span data-stu-id="32025-148">You can then import the files into the consolidated legal entity.</span></span>
