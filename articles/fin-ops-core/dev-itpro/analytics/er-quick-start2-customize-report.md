---
title: Koriģēt ER formātu pielāgota elektroniskā dokumenta ģenerēšanai
description: Šajā tēmā ir paskaidrots, kā koriģēt Microsoft nodrošināto elektronisko pārskatu (ER) formātu, lai tas ģenerētu pielāgotu elektronisko dokumentu.
author: NickSelin
manager: AnnBe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 67763b29744c4262249ef1ec04e7df490b31fe5b
ms.sourcegitcommit: 1e6a7b50596eaf9d965e0155f3f2c50f7f50747e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/22/2020
ms.locfileid: "3498105"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a><span data-ttu-id="0066e-103">Koriģēt ER formātu pielāgota elektroniskā dokumenta ģenerēšanai</span><span class="sxs-lookup"><span data-stu-id="0066e-103">Adjust an ER format to generate a custom electronic document</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0066e-104">Šīs tēmas procedūrās ir paskaidrots, kā lietotājs sistēmas administratora vai elektronisko pārskatu funkcionālā konsultanta lomā var veikt šos uzdevumus:</span><span class="sxs-lookup"><span data-stu-id="0066e-104">The procedures in this topic explain how a user in the System Administrator or Electronic Reporting Functional Consultant role can perform these tasks:</span></span>

- <span data-ttu-id="0066e-105">Konfigurēt parametrus [Elektronisko pārskatu (ER) veidošanas struktūrai](general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="0066e-105">Configure parameters for the [Electronic reporting (ER) framework](general-electronic-reporting.md).</span></span>
- <span data-ttu-id="0066e-106">Importēt Microsoft nodrošinātās ER konfigurācijas un izmantot, lai ģenerētu maksājuma failu, kamēr [kreditora maksājums](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) tiek apstrādāts.</span><span class="sxs-lookup"><span data-stu-id="0066e-106">Import ER configurations that are provided by Microsoft and used to generate a payment file while a [vendor payment](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) is being processed.</span></span>
- <span data-ttu-id="0066e-107">Izveidot Microsoft nodrošinātās standarta ER formāta konfigurācijas pielāgotu versiju.</span><span class="sxs-lookup"><span data-stu-id="0066e-107">Create a custom version of a standard ER format configuration that is provided by Microsoft.</span></span>
- <span data-ttu-id="0066e-108">Modificēt pielāgoto ER formāta konfigurāciju, lai tā ģenerētu maksājuma failus, kas atbilst noteiktas bankas prasībām.</span><span class="sxs-lookup"><span data-stu-id="0066e-108">Modify the custom ER format configuration so that it generates payment files that meets the requirements of a specific bank.</span></span>
- <span data-ttu-id="0066e-109">Pieņemt standarta ER formāta konfigurācijā veiktās izmaiņas pielāgotajā ER formāta konfigurācijā.</span><span class="sxs-lookup"><span data-stu-id="0066e-109">Adopt changes that are made to the standard ER format configuration in the custom ER format configuration.</span></span>

<span data-ttu-id="0066e-110">Visas tālāk norādītās procedūras var veikt uzņēmumā **GBSI**.</span><span class="sxs-lookup"><span data-stu-id="0066e-110">All the following procedures can be done in the **GBSI** company.</span></span> <span data-ttu-id="0066e-111">Kodēšana nav nepieciešama.</span><span class="sxs-lookup"><span data-stu-id="0066e-111">No coding is required.</span></span>

- [<span data-ttu-id="0066e-112">ER struktūras konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="0066e-112">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="0066e-113">Konfigurējiet ER parametrus</span><span class="sxs-lookup"><span data-stu-id="0066e-113">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="0066e-114">ER konfigurācijas nodrošinātāja aktivizēšana</span><span class="sxs-lookup"><span data-stu-id="0066e-114">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="0066e-115">ER konfigurācijas nodrošinātāju saraksta pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="0066e-115">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="0066e-116">Jauna ER konfigurācijas nodrošinātāja pievienošana</span><span class="sxs-lookup"><span data-stu-id="0066e-116">Add a new ER configuration provider</span></span>](#ActivateProvider)
        - [<span data-ttu-id="0066e-117">ER konfigurācijas nodrošinātāja aktivizēšana</span><span class="sxs-lookup"><span data-stu-id="0066e-117">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="0066e-118">Standarta ER formāta konfigurāciju importēšana</span><span class="sxs-lookup"><span data-stu-id="0066e-118">Import the standard ER format configurations</span></span>](#ImportERSolution1)

    - [<span data-ttu-id="0066e-119">Standarta ER konfigurāciju importēšana</span><span class="sxs-lookup"><span data-stu-id="0066e-119">Import the standard ER configurations</span></span>](#ImportERFormat1)
    - [<span data-ttu-id="0066e-120">Importēto ER konfigurāciju pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="0066e-120">Review the imported ER configurations</span></span>](#ReviewImportedERSolution)

- [<span data-ttu-id="0066e-121">Kreditora maksājuma sagatavošana apstrādei</span><span class="sxs-lookup"><span data-stu-id="0066e-121">Prepare a vendor payment for processing</span></span>](#PrepareVendorPayment)

    - [<span data-ttu-id="0066e-122">Bankas informācijas pievienošana kreditora kontam</span><span class="sxs-lookup"><span data-stu-id="0066e-122">Add bank information for a vendor account</span></span>](#AddBankAccount)
    - [<span data-ttu-id="0066e-123">Kreditora maksājuma ievadīšana</span><span class="sxs-lookup"><span data-stu-id="0066e-123">Enter a vendor payment</span></span>](#EnterVendorPayment)

- [<span data-ttu-id="0066e-124">Kreditora maksājuma apstrādāšana, izmantojot standarta ER formātu</span><span class="sxs-lookup"><span data-stu-id="0066e-124">Process a vendor payment by using the standard ER format</span></span>](#ProcessVendorPayment1)

    - [<span data-ttu-id="0066e-125">Elektroniskā maksājuma metodes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="0066e-125">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment1)
    - [<span data-ttu-id="0066e-126">Kreditora maksājuma apstrādāšana</span><span class="sxs-lookup"><span data-stu-id="0066e-126">Process a vendor payment</span></span>](#ProcessPayment1)

- [<span data-ttu-id="0066e-127">Standarta ER formāta pielāgošana</span><span class="sxs-lookup"><span data-stu-id="0066e-127">Customize the standard ER format</span></span>](#CustomizeProvidedFormat)

    - [<span data-ttu-id="0066e-128">Pielāgota formāta izveidošana</span><span class="sxs-lookup"><span data-stu-id="0066e-128">Create a custom format</span></span>](#DeriveProvidedFormat)
    - [<span data-ttu-id="0066e-129">Pielāgota formāta rediģēšana</span><span class="sxs-lookup"><span data-stu-id="0066e-129">Edit a custom format</span></span>](#ConfigureDerivedFormat)
    - [<span data-ttu-id="0066e-130">Pielāgota formāta atzīmēšana kā izpildāms</span><span class="sxs-lookup"><span data-stu-id="0066e-130">Mark a custom format as runnable</span></span>](#MarkFormatRunnable)

- [<span data-ttu-id="0066e-131">Kreditora maksājuma apstrādāšana, izmantojot pielāgotu ER formātu</span><span class="sxs-lookup"><span data-stu-id="0066e-131">Process a vendor payment by using the custom ER format</span></span>](#ProcessVendorPayment2)

    - [<span data-ttu-id="0066e-132">Elektroniskā maksājuma metodes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="0066e-132">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment2)
    - [<span data-ttu-id="0066e-133">Kreditora maksājuma apstrādāšana</span><span class="sxs-lookup"><span data-stu-id="0066e-133">Process a vendor payment</span></span>](#ProcessPayment2)

- [<span data-ttu-id="0066e-134">Jaunas standarta ER formāta konfigurācijas versijas importēšana</span><span class="sxs-lookup"><span data-stu-id="0066e-134">Import new versions of the standard ER format configurations</span></span>](#ImportERSolution2)

    - [<span data-ttu-id="0066e-135">Jaunas standarta ER konfigurācijas versijas importēšana</span><span class="sxs-lookup"><span data-stu-id="0066e-135">Import new versions of the standard ER configurations</span></span>](#ImportERFormat2)
    - [<span data-ttu-id="0066e-136">Importētās ER formāta konfigurācijas pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="0066e-136">Review the imported ER format configurations</span></span>](#ReviewImportedERFormat)

- [<span data-ttu-id="0066e-137">Importētā formāta jaunās versijas izmaiņu pieņemšana pielāgotajā formātā</span><span class="sxs-lookup"><span data-stu-id="0066e-137">Adopt the changes in the new version of an imported format in a custom format</span></span>](#AdoptNewBaseVersion)

    - [<span data-ttu-id="0066e-138">Pielāgotā formāta pašreizējās melnraksta versijas pabeigšana</span><span class="sxs-lookup"><span data-stu-id="0066e-138">Complete the current draft version of a custom format</span></span>](#CompleteDerivedFormat)
    - [<span data-ttu-id="0066e-139">Pielāgotā formāta pārvietošana uz jaunu bāzes versiju</span><span class="sxs-lookup"><span data-stu-id="0066e-139">Rebase a custom format to a new base version</span></span>](#RebaseDerivedFormat)
    - [<span data-ttu-id="0066e-140">Kreditora maksājuma apstrādāšana, izmantojot pārveidotu ER formātu</span><span class="sxs-lookup"><span data-stu-id="0066e-140">Process a vendor payment by using a rebased ER format</span></span>](#ProcessPayment3)

- [<span data-ttu-id="0066e-141">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="0066e-141">Additional resources</span></span>](#References)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a><span data-ttu-id="0066e-142">ER struktūras konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="0066e-142">Configure the ER framework</span></span>

<span data-ttu-id="0066e-143">Kā lietotājam elektronisko pārskatu funkcionālā konsultanta lomā, jums ir jākonfigurē minimāls ER parametru kopums, pirms varat sākt izmantot ER struktūru, lai veidotu standarta ER formāta pielāgotu versiju.</span><span class="sxs-lookup"><span data-stu-id="0066e-143">As a user in the Electronic Reporting Functional Consultant role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design a custom version of a standard ER format.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="0066e-144">Konfigurējiet ER parametrus</span><span class="sxs-lookup"><span data-stu-id="0066e-144">Configure ER parameters</span></span>

1. <span data-ttu-id="0066e-145">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="0066e-145">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="0066e-146">Lapas **Lokalizācijas konfigurācijas** sadaļā **Saistītās saites** atlasiet **Elektronisko pārskatu veidošanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="0066e-146">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="0066e-147">Lapas **Elektronisko pārskatu veidošanas parametri** cilnē **Vispārīgi** iestatiet opciju **Iespējot noformēšanas režīmu** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="0066e-147">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="0066e-148">Cilnē **Pielikumi** iestatiet šādus parametrus:</span><span class="sxs-lookup"><span data-stu-id="0066e-148">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="0066e-149">Laukā **Konfigurācijas** atlasiet veidu **Fails** uzņēmumam **USMF**.</span><span class="sxs-lookup"><span data-stu-id="0066e-149">In the **Configurations** field, select the **File** type for the **USMF** company.</span></span>
    - <span data-ttu-id="0066e-150">Laukos **Darbu arhīvs**, **Pagaidu**, **Bāzlīnija** un **Citi** atlasiet veidu **Fails**.</span><span class="sxs-lookup"><span data-stu-id="0066e-150">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="0066e-151">Papildinformāciju par ER parametriem skatiet sadaļā [ER struktūras konfigurēšana](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0066e-151">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="0066e-152">ER konfigurācijas nodrošinātāja aktivizēšana</span><span class="sxs-lookup"><span data-stu-id="0066e-152">Activate an ER configuration provider</span></span>

<span data-ttu-id="0066e-153">Katra pievienotā ER konfigurācija tiek atzīmēta kā piederoša ER konfigurācijas nodrošinātājam.</span><span class="sxs-lookup"><span data-stu-id="0066e-153">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="0066e-154">Šim nolūkam tiek izmantots ER konfigurācijas nodrošinātājs, kas ir aktivizēts **Elektroniskie pārskati** darbvietā.</span><span class="sxs-lookup"><span data-stu-id="0066e-154">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="0066e-155">Tāpēc, pirms sākat pievienot vai rediģēt ER konfigurācijas, jums ir jāaktivizē ER konfigurācijas nodrošinātājs **Elektroniskie pārskati** darbvietā.</span><span class="sxs-lookup"><span data-stu-id="0066e-155">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="0066e-156">Tikai ER konfigurācijas īpašnieks var to rediģēt.</span><span class="sxs-lookup"><span data-stu-id="0066e-156">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="0066e-157">Tāpēc, pirms ER konfigurācija var tikt rediģēta, darbvietā **Elektroniskie pārskati** ir jāaktivizē atbilstošais ER konfigurācijas nodrošinātājs.</span><span class="sxs-lookup"><span data-stu-id="0066e-157">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="0066e-158">ER konfigurācijas nodrošinātāju saraksta pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="0066e-158">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="0066e-159">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="0066e-159">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="0066e-160">Lapas **Lokalizācijas konfigurācijas** sadaļā **Saistītās saites** atlasiet **Konfigurācijas nodrošinātāji**.</span><span class="sxs-lookup"><span data-stu-id="0066e-160">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="0066e-161">Lapā **Konfigurācijas nodrošinātāju tabula** katram nodrošinātāja ierakstam ir unikāls nosaukums un URL.</span><span class="sxs-lookup"><span data-stu-id="0066e-161">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="0066e-162">Pārskatiet šīs lapas saturu.</span><span class="sxs-lookup"><span data-stu-id="0066e-162">Review the contents of this page.</span></span> <span data-ttu-id="0066e-163">Ja ieraksts **Litware, Inc.** (`https://www.litware.com`) jau pastāv, izlaidiet nākamo procedūru, [Jauna ER konfigurācijas nodrošinātāja pievienošana](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="0066e-163">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="0066e-164">Jauna ER konfigurācijas nodrošinātāja pievienošana</span><span class="sxs-lookup"><span data-stu-id="0066e-164">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="0066e-165">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="0066e-165">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="0066e-166">Lapas **Lokalizācijas konfigurācijas** sadaļā **Saistītās saites** atlasiet **Konfigurācijas nodrošinātāji**.</span><span class="sxs-lookup"><span data-stu-id="0066e-166">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="0066e-167">Lapā **Konfigurācijas nodrošinātāji** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="0066e-167">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="0066e-168">Laukā **Nosaukums** ievadiet **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="0066e-168">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="0066e-169">Laukā **Interneta adrese** ievadiet `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="0066e-169">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="0066e-170">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0066e-170">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="0066e-171">ER konfigurācijas nodrošinātāja aktivizēšana</span><span class="sxs-lookup"><span data-stu-id="0066e-171">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="0066e-172">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="0066e-172">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="0066e-173">Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Litware, Inc.** un pēc tam atlasiet **Iestatīt kā aktīvu**.</span><span class="sxs-lookup"><span data-stu-id="0066e-173">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="0066e-174">Papildinformāciju par ER konfigurācijas nodrošinātājiem skatiet sadaļā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="0066e-174">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a><span data-ttu-id="0066e-175">Standarta ER formāta konfigurāciju importēšana</span><span class="sxs-lookup"><span data-stu-id="0066e-175">Import the standard ER format configurations</span></span>

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a><span data-ttu-id="0066e-176">Standarta ER konfigurāciju importēšana</span><span class="sxs-lookup"><span data-stu-id="0066e-176">Import the standard ER configurations</span></span>

<span data-ttu-id="0066e-177">Lai pievienotu standarta ER konfigurācijas savai pašreizējai Microsoft Dynamics 365 Finance instancei, jums tās ir jāimportē no šai instancei konfigurētā ER [repozitorija](general-electronic-reporting.md#Repository).</span><span class="sxs-lookup"><span data-stu-id="0066e-177">To add the standard ER configurations to your current instance of Microsoft Dynamics 365 Finance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that was configured for that instance.</span></span>

1. <span data-ttu-id="0066e-178">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="0066e-178">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="0066e-179">Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Microsoft** un pēc tam atlasiet **Repozitoriji**, lai skatītu Microsoft nodrošinātāja repozitoriju sarakstu.</span><span class="sxs-lookup"><span data-stu-id="0066e-179">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="0066e-180">Lapā **Konfigurācijas repozitoriji** atlasiet repozitoriju ar veidu **Globāls** un pēc tam atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="0066e-180">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="0066e-181">Ja tiek pieprasīta autorizācija savienojumam ar Regulatory Configuration Service, izpildiet autorizācijas norādījumus.</span><span class="sxs-lookup"><span data-stu-id="0066e-181">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="0066e-182">Lapā **Konfigurācijas repozitorijs** konfigurācijas koka skata kreisajā rūtī atlasiet **BACS (UK)** formāta konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="0066e-182">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="0066e-183">Kopsavilkuma cilnē **Versijas** izvēlieties atlasītās ER formāta konfigurācijas **1.1** versiju.</span><span class="sxs-lookup"><span data-stu-id="0066e-183">On the **Versions** FastTab, select version **1.1** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="0066e-184">Atlasiet **Importēt**, lai lejupielādētu atlasīto versiju no globālā repozitorija uz pašreizējo Finance instanci.</span><span class="sxs-lookup"><span data-stu-id="0066e-184">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![Konfigurācijas repozitorijas lapa.](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> <span data-ttu-id="0066e-186">Ja rodas problēmas ar piekļuvi [globālajam repozitorijam](er-download-configurations-global-repo.md), tā vietā varat [lejupielādēt konfigurācijas](download-electronic-reporting-configuration-lcs.md) no Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="0066e-186">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from Microsoft Dynamics Lifecycle Services (LCS) instead.</span></span>

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a><span data-ttu-id="0066e-187">Importēto ER konfigurāciju pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="0066e-187">Review the imported ER configurations</span></span>

1. <span data-ttu-id="0066e-188">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="0066e-188">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="0066e-189">Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="0066e-189">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="0066e-190">Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Maksājuma modelis**.</span><span class="sxs-lookup"><span data-stu-id="0066e-190">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**.</span></span>
4. <span data-ttu-id="0066e-191">Ņemiet vērā, ka papildus atlasītajam **BACS (UK)** ER formātam tika importētas arī citas nepieciešamās ER konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="0066e-191">Notice that, in addition to the selected **BACS (UK)** ER format, other required ER configurations were imported.</span></span> <span data-ttu-id="0066e-192">Pārliecinieties, vai konfigurācijas kokā ir pieejamas šādas ER konfigurācijas:</span><span class="sxs-lookup"><span data-stu-id="0066e-192">Make sure that the following ER configurations are available in the configuration tree:</span></span>

    - <span data-ttu-id="0066e-193">**Maksājuma modelis** — šajā konfigurācijā ir norādīts [datu modeļa](general-electronic-reporting.md#data-model-and-model-mapping-components) ER komponents, kas parāda maksājuma biznesa domēna datu struktūru.</span><span class="sxs-lookup"><span data-stu-id="0066e-193">**Payment model** – This configuration contains the [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that represents the data structure of the payment business domain.</span></span>
    - <span data-ttu-id="0066e-194">**Maksājuma modeļa kartēšana 1611** — šajā konfigurācijā ir norādīta [modeļa kartēšana](general-electronic-reporting.md#data-model-and-model-mapping-components) ER komponentam, kas apraksta, kā datu modelis tiek aizpildīts ar programmas datiem izpildlaikā.</span><span class="sxs-lookup"><span data-stu-id="0066e-194">**Payment model mapping 1611** – This configuration contains the [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that describes how the data model is filled in with application data at runtime.</span></span>
    - <span data-ttu-id="0066e-195">**BACS (UK)** — šajā konfigurācijā ir norādīts [formāts](general-electronic-reporting.md#FormatComponentOutbound) un formāta kartēšanas ER komponenti.</span><span class="sxs-lookup"><span data-stu-id="0066e-195">**BACS (UK)** – This configuration contains the [format](general-electronic-reporting.md#FormatComponentOutbound) and format mapping ER components.</span></span> <span data-ttu-id="0066e-196">Formāta komponents norāda atskaites izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="0066e-196">The format component specifies the report layout.</span></span> <span data-ttu-id="0066e-197">Formāta kartēšanas komponents satur modeļa datu avotu un norāda, kā atskaites izkārtojums tiek aizpildīts, izmantojot šo datu avotu izpildlaikā.</span><span class="sxs-lookup"><span data-stu-id="0066e-197">The format mapping component contains the model data source and specifies how the report layout is filled in by using this data source at runtime.</span></span>

![Lapa Konfigurācijas](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a><span data-ttu-id="0066e-199">Kreditora maksājuma sagatavošana apstrādei</span><span class="sxs-lookup"><span data-stu-id="0066e-199">Prepare a vendor payment for processing</span></span>

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a><span data-ttu-id="0066e-200">Bankas informācijas pievienošana kreditora kontam</span><span class="sxs-lookup"><span data-stu-id="0066e-200">Add bank information for a vendor account</span></span>

<span data-ttu-id="0066e-201">Kreditora kontam ir jāpievieno bankas informācija, kas vēlāk tiks norādīta reģistrētā maksājumā.</span><span class="sxs-lookup"><span data-stu-id="0066e-201">You must add bank information for a vendor account that will be referred to later in a registered payment.</span></span>

1. <span data-ttu-id="0066e-202">Dodieties uz **Kreditori** \> **Kreditori** \> **Visi kreditori**.</span><span class="sxs-lookup"><span data-stu-id="0066e-202">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="0066e-203">Lapā **Visi kreditori** atlasiet kreditora kontu **GB_SI_000001** un pēc tam darbību rūts cilnē **Kreditors** grupā **Iestatīt** atlasiet **Banku konti**.</span><span class="sxs-lookup"><span data-stu-id="0066e-203">On the **All vendors** page, select the **GB_SI_000001** vendor account, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="0066e-204">Lapā **Kreditora banku konti** atlasiet **Jauns** un pēc tam ievadiet tālāk norādīto informāciju:</span><span class="sxs-lookup"><span data-stu-id="0066e-204">On the **Vendor bank accounts** page, select **New**, and then enter the following information:</span></span>

    1. <span data-ttu-id="0066e-205">Laukā **Bankas konts** ievadiet **GBP OPER**.</span><span class="sxs-lookup"><span data-stu-id="0066e-205">In the **Bank account** field, enter **GBP OPER**.</span></span>
    2. <span data-ttu-id="0066e-206">Laukā **Bankas grupas** atlasiet **BankGBP**.</span><span class="sxs-lookup"><span data-stu-id="0066e-206">In the **Bank groups** field, select **BankGBP**.</span></span>
    3. <span data-ttu-id="0066e-207">Laukā **Bankas konta numurs** ievadiet **202015**.</span><span class="sxs-lookup"><span data-stu-id="0066e-207">In the **Bank account number** field, enter **202015**.</span></span>
    4. <span data-ttu-id="0066e-208">Laukā **SWIFT kods** ievadiet <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span><span class="sxs-lookup"><span data-stu-id="0066e-208">In the **SWIFT code** field, enter <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span></span>
    5. <span data-ttu-id="0066e-209">Laukā **IBAN** ievadiet **GB33BUKB20201555555555**.</span><span class="sxs-lookup"><span data-stu-id="0066e-209">In the **IBAN** field, enter **GB33BUKB20201555555555**.</span></span>
    6. <span data-ttu-id="0066e-210">Laukā **Reģistrācijas numurs** saglabājiet noklusējuma vērtību <a id="DefineRoutingNumber"></a>**123456**.</span><span class="sxs-lookup"><span data-stu-id="0066e-210">In the **Routing number** field, keep the default value, <a id="DefineRoutingNumber"></a>**123456**.</span></span>

    ![Lapa Kreditora banku konti](./media/er-quick-start2-bank-account.png)

4. <span data-ttu-id="0066e-212">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0066e-212">Select **Save**.</span></span>
5. <span data-ttu-id="0066e-213">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0066e-213">Close the page.</span></span>
6. <span data-ttu-id="0066e-214">Lapā **Visi kreditori** atveriet kreditora kontu **GB_SI_000001**.</span><span class="sxs-lookup"><span data-stu-id="0066e-214">On the **All vendors** page, open the **GB_SI_000001** vendor account.</span></span>
7. <span data-ttu-id="0066e-215">Ja nepieciešams, lapā informācija par kreditoru atlasiet **Rediģēt**, lai lapu varētu rediģēt.</span><span class="sxs-lookup"><span data-stu-id="0066e-215">On the vendor details page, select **Edit** to make the page editable, if required.</span></span>
8. <span data-ttu-id="0066e-216">Kopsavilkuma cilnē **Maksājums**, laukā **Bankas konts** atlasiet **GBP OPER**.</span><span class="sxs-lookup"><span data-stu-id="0066e-216">On the **Payment** FastTab, in the **Bank account** field, select **GBP OPER**.</span></span>

    ![Lapa Informācija par kreditoru](./media/er-quick-start2-bank-account-reference.png)

9. <span data-ttu-id="0066e-218">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0066e-218">Select **Save**.</span></span>
10. <span data-ttu-id="0066e-219">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0066e-219">Close the page.</span></span>

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a><span data-ttu-id="0066e-220">Kreditora maksājuma ievadīšana</span><span class="sxs-lookup"><span data-stu-id="0066e-220">Enter a vendor payment</span></span>

<span data-ttu-id="0066e-221">Ir nepieciešams ievadīt jaunu kreditora maksājumu, izmantojot [maksājuma priekšlikumu](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal).</span><span class="sxs-lookup"><span data-stu-id="0066e-221">You must enter a new vendor payment by using a [payment proposal](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal).</span></span>

1. <span data-ttu-id="0066e-222">Dodieties uz **Kreditori** \> **Maksājumi** \> **Kreditora maksājumu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="0066e-222">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="0066e-223">Lapā **Kreditora maksājumu žurnāls** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="0066e-223">On the **Vendor payment journal** page, select **New**.</span></span>
3. <span data-ttu-id="0066e-224">Laukā **Nosaukums** atlasiet **VendPay**.</span><span class="sxs-lookup"><span data-stu-id="0066e-224">In the **Name** field, select **VendPay**.</span></span>
4. <span data-ttu-id="0066e-225">Atlasiet **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="0066e-225">Select **Lines**.</span></span>
5. <span data-ttu-id="0066e-226">Atlasiet **Maksājuma priekšlikums** \> **Izveidot maksājuma priekšlikumu**.</span><span class="sxs-lookup"><span data-stu-id="0066e-226">Select **Payment proposal** \> **Create payment proposal**.</span></span>
6. <span data-ttu-id="0066e-227">Dialoglodziņā **Kreditora maksājuma priekšlikums** konfigurējiet nosacījumus, lai filtrētu tikai **GB_SI_000001** kreditora konta ierakstus, un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0066e-227">In the **Vendor payment proposal** dialog box, configure conditions to filter for records for the **GB_SI_000001** vendor account only, and then select **OK**.</span></span>
7. <span data-ttu-id="0066e-228">Atlasiet rindu rēķinam **00000007_Inv** un pēc tam atlasiet **Izveidot maksājumu**.</span><span class="sxs-lookup"><span data-stu-id="0066e-228">Select the line for the **00000007_Inv** invoice, and then select **Create payment**.</span></span>

    ![Kreditora maksājuma priekšlikuma dialoglodziņš](./media/er-quick-start2-payment-proposal.png)

8. <span data-ttu-id="0066e-230">Pārbaudiet, vai ievadītais maksājums ir konfigurēts, lai izmantotu **elektroniska** maksājuma metodi.</span><span class="sxs-lookup"><span data-stu-id="0066e-230">Verify that the payment that is entered is configured to use the **Electronic** method of payment.</span></span>

    ![Kreditora maksājumu lapa](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a><span data-ttu-id="0066e-232">Kreditora maksājuma apstrādāšana, izmantojot standarta ER formātu</span><span class="sxs-lookup"><span data-stu-id="0066e-232">Process a vendor payment by using the standard ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a><span data-ttu-id="0066e-233">Elektroniskā maksājuma metodes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="0066e-233">Set up the electronic payment method</span></span>

<span data-ttu-id="0066e-234">Elektroniskā maksājuma metode ir jākonfigurē, lai tā izmantotu importēto ER formāta konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="0066e-234">You must configure the electronic method of payment so that it uses the imported ER format configuration.</span></span>

1. <span data-ttu-id="0066e-235">Dodieties uz **Kreditori** \> **Maksājuma iestatīšana** \> **Maksājuma metodes**.</span><span class="sxs-lookup"><span data-stu-id="0066e-235">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="0066e-236">Lapā **Maksājuma metodes – kreditori**, kreisajā rūtī atlasiet maksājuma metodi **Elektronisks**.</span><span class="sxs-lookup"><span data-stu-id="0066e-236">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="0066e-237">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="0066e-237">Select **Edit**.</span></span>
4. <span data-ttu-id="0066e-238">Kopsavilkuma cilnē **Faila formāti** iestatiet opciju **Vispārīgs elektroniskās eksportēšanas formāts** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="0066e-238">On the **File formats** FastTab, set the **General electronic Export format** option to **Yes**.</span></span>
5. <span data-ttu-id="0066e-239">Laukā **Eksporta formāta konfigurācija** atlasiet **BACS (UK)** formāta konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="0066e-239">In the **Export format configuration** field, select the **BACS (UK)** format configuration.</span></span>

    ![Lapa Maksājuma metodes – kreditori](./media/er-quick-start2-method-of-payment1.png)

6. <span data-ttu-id="0066e-241">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0066e-241">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a><span data-ttu-id="0066e-242">Kreditora maksājuma apstrādāšana</span><span class="sxs-lookup"><span data-stu-id="0066e-242">Process a vendor payment</span></span>

1. <span data-ttu-id="0066e-243">Dodieties uz **Kreditori** \> **Maksājumi** \> **Kreditora maksājumu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="0066e-243">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="0066e-244">Lapā **Kreditora maksājumu žurnāls** atlasiet iepriekš pievienoto maksājumu žurnālu un pēc tam atlasiet **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="0066e-244">On the **Vendor payment journal** page, select the payment journal that you added earlier, and then select **Lines**.</span></span>
3. <span data-ttu-id="0066e-245">Lapā **Kreditora maksājumi** atlasiet **Ģenerēt maksājumus**.</span><span class="sxs-lookup"><span data-stu-id="0066e-245">On the **Vendor payments** page, select **Generate payments**.</span></span>
4. <span data-ttu-id="0066e-246">Dialoglodziņā **Ģenerēt maksājumus** ievadiet tālāk norādīto informāciju:</span><span class="sxs-lookup"><span data-stu-id="0066e-246">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="0066e-247">Laukā **Maksājuma metode** atlasiet **Elektronisks**.</span><span class="sxs-lookup"><span data-stu-id="0066e-247">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="0066e-248">Laukā **Bankas konts** atlasiet **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="0066e-248">In the **Bank account** field, select **GBSI OPER**.</span></span>

5. <span data-ttu-id="0066e-249">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0066e-249">Select **OK**.</span></span>
6. <span data-ttu-id="0066e-250">Dialoglodziņā **Elektronisko pārskatu parametri** iestatiet opciju **Drukāt kontroles pārskatu** uz **Jā** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0066e-250">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    ![Elektronisko pārskatu parametru dialoga lapa](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > <span data-ttu-id="0066e-252">Papildus maksājuma failam tagad varat ģenerēt arī kontroles pārskatu.</span><span class="sxs-lookup"><span data-stu-id="0066e-252">In addition to the payment file, you can now generate the control report.</span></span>

7. <span data-ttu-id="0066e-253">Lejupielādējiet zip failu un pēc tam no tā izvelciet tālāk norādītos failus:</span><span class="sxs-lookup"><span data-stu-id="0066e-253">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="0066e-254">Kontroles pārskats Excel formātā</span><span class="sxs-lookup"><span data-stu-id="0066e-254">The control report in Excel format</span></span>
    - <span data-ttu-id="0066e-255">Maksājuma fails TXT formāta</span><span class="sxs-lookup"><span data-stu-id="0066e-255">The payment file in TXT format</span></span>

        <span data-ttu-id="0066e-256">Ņemiet vērā, ka saskaņā ar sniegtā ER formāta [struktūru](#PositionRoutingNumber) maksājuma rinda ģenerētajā failā sākas ar reģistrācijas numuru, kas [definēts](#DefineRoutingNumber) konfigurētajam bankas kontam.</span><span class="sxs-lookup"><span data-stu-id="0066e-256">Notice that, in accordance with the [structure](#PositionRoutingNumber) of the provided ER format, the payment line in the generated file starts with the routing number that was [defined](#DefineRoutingNumber) for the configured bank account.</span></span>

        ![Maksājuma fails TXT formāta](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a><span data-ttu-id="0066e-258">Standarta ER formāta pielāgošana</span><span class="sxs-lookup"><span data-stu-id="0066e-258">Customize the standard ER format</span></span>

<span data-ttu-id="0066e-259">Šajā sadaļā sniegtā piemēra ietvaros, jūs vēlaties izmantot korporācijas Microsoft nodrošinātās ER konfigurācijas, lai ģenerētu kreditora maksājumu failus BACS formātā, bet ir jāpievieno pielāgojums, lai atbalstītu noteiktas bankas prasības.</span><span class="sxs-lookup"><span data-stu-id="0066e-259">For the example that is shown in this section, you want to use the ER configurations that are provided by Microsoft to generate vendor payment files in BACS format, but you must add a customization to support the requirements of a specific bank.</span></span> <span data-ttu-id="0066e-260">Jūs vēlaties arī varēt jaunināt savu pielāgoto formātu, kad būs pieejamas jaunas ER konfigurāciju versijas.</span><span class="sxs-lookup"><span data-stu-id="0066e-260">You also want to be able to upgrade your custom format when new versions of ER configurations become available.</span></span> <span data-ttu-id="0066e-261">Tomēr jūs vēlaties veikt jaunināšanu ar pēc iespējas zemākām izmaksām.</span><span class="sxs-lookup"><span data-stu-id="0066e-261">However, you want to be able to do the upgrade at the lowest cost.</span></span>

<span data-ttu-id="0066e-262">Šādā gadījumā, kā Litware, Inc. pārstāvim, jums ir jāizveido (jāatvasina) jauna ER formāta konfigurācija, izmantojot Microsoft nodrošināto **BACS (UK)** konfigurāciju kā bāzi.</span><span class="sxs-lookup"><span data-stu-id="0066e-262">In this case, as the representative of Litware, Inc., you must create (derive) a new ER format configuration by using the **BACS (UK)** Microsoft-provided configuration as a base.</span></span>

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a><span data-ttu-id="0066e-263">Pielāgota formāta izveidošana</span><span class="sxs-lookup"><span data-stu-id="0066e-263">Create a custom format</span></span>

1. <span data-ttu-id="0066e-264">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="0066e-264">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0066e-265">Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Maksājuma modelis** un pēc tam atlasiet **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="0066e-265">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span> <span data-ttu-id="0066e-266">Litware, Inc. izmantos šīs ER formāta konfigurācijas versiju 1.1 kā pielāgotās versijas bāzi.</span><span class="sxs-lookup"><span data-stu-id="0066e-266">Litware, Inc. will use version 1.1 of this ER format configuration as the base for the custom version.</span></span>
3. <span data-ttu-id="0066e-267">Atlasiet **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="0066e-267">Select **Create configuration** to open the drop-down dialog box.</span></span> <span data-ttu-id="0066e-268">Varat izmantot šo dialoglodziņu, lai izveidotu jaunu konfigurāciju pielāgotam maksājuma formātam.</span><span class="sxs-lookup"><span data-stu-id="0066e-268">You can use this dialog box to create a new configuration for a custom payment format.</span></span>
4. <span data-ttu-id="0066e-269">Lauka grupā **Jauns** atlasiet opciju **Atvasināt no nosaukuma: BACS (UK), Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="0066e-269">In the **New** field group, select the **Derive from Name: BACS (UK), Microsoft** option.</span></span>
5. <span data-ttu-id="0066e-270">Laukā **Nosaukums** ievadiet **BACS (UK pielāgots)**.</span><span class="sxs-lookup"><span data-stu-id="0066e-270">In the **Name** field, enter **BACS (UK custom)**.</span></span>

    ![Izveidot konfigurācijas nolaižamo dialoglodziņu](./media/er-quick-start2-add-derived-format.png)

6. <span data-ttu-id="0066e-272">Atlasiet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="0066e-272">Select **Create configuration**.</span></span>

<span data-ttu-id="0066e-273">ER formāta konfigurācijas **BACS (UK pielāgots)** versija 1.1.1 ir izveidota.</span><span class="sxs-lookup"><span data-stu-id="0066e-273">Version 1.1.1 of the **BACS (UK custom)** ER format configuration is created.</span></span> <span data-ttu-id="0066e-274">Šīs versijas [statuss](general-electronic-reporting.md#component-versioning) ir **Melnraksts** un to var rediģēt.</span><span class="sxs-lookup"><span data-stu-id="0066e-274">This version has a [status](general-electronic-reporting.md#component-versioning) of **Draft** and can be edited.</span></span> <span data-ttu-id="0066e-275">Pielāgotā ER formāta pašreizējais saturs atbilst Microsoft nodrošinātā formāta saturam.</span><span class="sxs-lookup"><span data-stu-id="0066e-275">The current content of your custom ER format matches the content of the format that is provided by Microsoft.</span></span>

![Lapa Konfigurācijas](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a><span data-ttu-id="0066e-277">Pielāgota formāta rediģēšana</span><span class="sxs-lookup"><span data-stu-id="0066e-277">Edit a custom format</span></span>

<span data-ttu-id="0066e-278">Jums ir jākonfigurē pielāgotais formāts, lai tas atbilstu bankas noteiktajām prasībām.</span><span class="sxs-lookup"><span data-stu-id="0066e-278">You must configure your custom format so that it meets bank-specific requirements.</span></span> <span data-ttu-id="0066e-279">Piemēram, banka var pieprasīt, lai ģenerētie maksājumu faili ietver Vispasaules Starpbanku finanšu telekomunikāciju sabiedrības (SWIFT) kodu bankai, kurai tiek piešķirta aģenta loma apstrādātā kreditora maksājumā.</span><span class="sxs-lookup"><span data-stu-id="0066e-279">For example, a bank might require that payment files that are generated include the Society for Worldwide Interbank Financial Telecommunication (SWIFT) code of a bank that is assigned the agent role in the processed vendor payment.</span></span> <span data-ttu-id="0066e-280">SWIFT kodi ir starptautiski bankas kodi, kas identificē noteiktas bankas visā pasaulē.</span><span class="sxs-lookup"><span data-stu-id="0066e-280">SWIFT codes are international bank codes that identify specific banks worldwide.</span></span> <span data-ttu-id="0066e-281">Tos sauc arī par banku identifikācijas kodiem (BIC).</span><span class="sxs-lookup"><span data-stu-id="0066e-281">They are also known as Bank Identifier Codes (BICs).</span></span> <span data-ttu-id="0066e-282">SWIFT kodam jābūt 11 rakstzīmes garam un tas ir jāievada ģenerētā maksājuma faila katras maksājuma rindas sākumā.</span><span class="sxs-lookup"><span data-stu-id="0066e-282">The SWIFT code must be 11 characters long, and it must be entered at the beginning of every payment line in a generated payment file.</span></span>

1. <span data-ttu-id="0066e-283">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="0066e-283">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0066e-284">Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Maksājuma modelis** un pēc tam atlasiet **BACS (UK pielāgots)**.</span><span class="sxs-lookup"><span data-stu-id="0066e-284">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="0066e-285">Kopsavilkuma cilnē **Versijas** izvēlieties atlasītās konfigurācijas **1.1.1** versiju.</span><span class="sxs-lookup"><span data-stu-id="0066e-285">On the **Versions** FastTab, select version **1.1.1** of the selected configuration.</span></span>
4. <span data-ttu-id="0066e-286">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="0066e-286">Select **Designer**.</span></span>
5. <span data-ttu-id="0066e-287">Lapā **Formāta veidotājs** atlasiet **Rādīt detalizēti**, lai skatītu papildinformāciju par formāta elementiem.</span><span class="sxs-lookup"><span data-stu-id="0066e-287">On the **Format designer** page, select **Show details** to view more information about the format elements.</span></span>
6. <span data-ttu-id="0066e-288">Izvērsiet un pārskatiet šādus elementus:</span><span class="sxs-lookup"><span data-stu-id="0066e-288">Expand and review the following elements:</span></span>

    - <span data-ttu-id="0066e-289">Veids **Mape**, elements **BACSReportsFolder**.</span><span class="sxs-lookup"><span data-stu-id="0066e-289">The **BACSReportsFolder** element of the **Folder** type.</span></span> <span data-ttu-id="0066e-290">Šis elements tiek izmantots, lai ģenerētu izvadi ZIP formātā.</span><span class="sxs-lookup"><span data-stu-id="0066e-290">This element is used to generate output in ZIP format.</span></span>
    - <span data-ttu-id="0066e-291">Veids **Fails**, elements **fails**.</span><span class="sxs-lookup"><span data-stu-id="0066e-291">The **file** element of the **File** type.</span></span> <span data-ttu-id="0066e-292">Šis elements tiek izmantots, lai ģenerētu maksājuma failu TXT formātā.</span><span class="sxs-lookup"><span data-stu-id="0066e-292">This element is used to generate a payment file in TXT format.</span></span>
    - <span data-ttu-id="0066e-293">Veids **Secība**, elements **transakcijas**.</span><span class="sxs-lookup"><span data-stu-id="0066e-293">The **transactions** element of the **Sequence** type.</span></span> <span data-ttu-id="0066e-294">Šis elements tiek izmantots, lai maksājuma failā ģenerētu vienu maksājuma rindu.</span><span class="sxs-lookup"><span data-stu-id="0066e-294">This element is used to generate a single payment line in a payment file.</span></span>
    - <span data-ttu-id="0066e-295">Veids **Secība**, elements **transakcija**.</span><span class="sxs-lookup"><span data-stu-id="0066e-295">The **transaction** element of the **Sequence** type.</span></span> <span data-ttu-id="0066e-296">Šis elements tiek izmantots, lai viena maksājuma rindai ģenerētu atsevišķus laukus.</span><span class="sxs-lookup"><span data-stu-id="0066e-296">This element is used to generate individual fields of a single payment line.</span></span>

7. <span data-ttu-id="0066e-297">Atlasiet elementu **transakcija**.</span><span class="sxs-lookup"><span data-stu-id="0066e-297">Select the **transaction** element.</span></span>

    ![Transakcijas elements ER operāciju veidotājā](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > <span data-ttu-id="0066e-299">Nodrošinātais pārskats ir konfigurēts, lai <a id="PositionRoutingNumber"></a>katra maksājuma rinda sākas ar bankas reģistrācijas numuru.</span><span class="sxs-lookup"><span data-stu-id="0066e-299">The provided report is configured so that <a id="PositionRoutingNumber"></a>every payment line starts with the bank routing number.</span></span> <span data-ttu-id="0066e-300">Šim nolūkam tiek izmantots **vendBankRouteNum** formāta elements.</span><span class="sxs-lookup"><span data-stu-id="0066e-300">The **vendBankRouteNum** format element is used for this purpose.</span></span> 

8. <span data-ttu-id="0066e-301">Atlasiet **Pievienot** un pēc tam atlasiet **Teksts\\Virkne** formāta elementa veidu, kuru pievienojat:</span><span class="sxs-lookup"><span data-stu-id="0066e-301">Select **Add**, and then select the **Text\\String** type of the format element that you're adding:</span></span>

    1. <span data-ttu-id="0066e-302">Laukā **Nosaukums** ievadiet **vendBankSWIFT**.</span><span class="sxs-lookup"><span data-stu-id="0066e-302">In the **Name** field, enter **vendBankSWIFT**.</span></span>
    2. <span data-ttu-id="0066e-303">Laukā **Minimālais garums** ievadiet **11**.</span><span class="sxs-lookup"><span data-stu-id="0066e-303">In the **Minimum length** field, enter **11**.</span></span>
    3. <span data-ttu-id="0066e-304">Laukā **Maksimālais garums** ievadiet **11**.</span><span class="sxs-lookup"><span data-stu-id="0066e-304">In the **Maximum length** field, enter **11**.</span></span>
    4. <span data-ttu-id="0066e-305">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0066e-305">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0066e-306">Elements **vendBankSWIFT** tiks izmantots, lai ģenerētajos failos ievadītu kreditora bankas SWIFT kodu.</span><span class="sxs-lookup"><span data-stu-id="0066e-306">The **vendBankSWIFT** element will be used to enter the SWIFT code of a vendor bank in generated files.</span></span>

9. <span data-ttu-id="0066e-307">Formāta struktūras kokā atlasiet **vendBankSWIFT**.</span><span class="sxs-lookup"><span data-stu-id="0066e-307">In the format structure tree, select **vendBankSWIFT**.</span></span>
10. <span data-ttu-id="0066e-308">Atlasiet **Pārvietot uz augšu**, lai pārvietotu atlasīto formāta elementu par vienu līmeni uz augšu.</span><span class="sxs-lookup"><span data-stu-id="0066e-308">Select **Move up** to move the selected format element up one level.</span></span> <span data-ttu-id="0066e-309">Atkārtojiet šo darbību, līdz **vendBankSWIFT** elements ir <a id="PositionSWIFTCode"></a>pirmais elements zem pamatelementa **transakcija**.</span><span class="sxs-lookup"><span data-stu-id="0066e-309">Repeat this step until the **vendBankSWIFT** element is the <a id="PositionSWIFTCode"></a>first element under the parent **transaction** element.</span></span>

    ![VendBankSWIFT kā pirmais elements zem transakcijas ER operāciju veidotājā](./media/er-quick-start2-derived-format1.png)

11. <span data-ttu-id="0066e-311">Kamēr formāta struktūras kokā joprojām ir atlasīts **vendBankSWIFT**, atlasiet cilni **Kartēšana** un pēc tam izvērsiet **modeļa** datu avotu.</span><span class="sxs-lookup"><span data-stu-id="0066e-311">While the **vendBankSWIFT** is still selected in the format structure tree, select the **Mapping** tab, and then expand the **model** data source.</span></span>
12. <span data-ttu-id="0066e-312">Izvērsiet **model.Payment** \> **model.Payment.CreditorAgent** un atlasiet datu avota lauku **model.Payment.CreditorAgent.BICFI**.</span><span class="sxs-lookup"><span data-stu-id="0066e-312">Expand **model.Payment** \> **model.Payment.CreditorAgent**, and select the **model.Payment.CreditorAgent.BICFI** data source field.</span></span> <span data-ttu-id="0066e-313">Šis datu avota lauks atklāj tā kreditora bankas SWIFT kodu, kam tiek piešķirta aģenta loma apstrādātā kreditora maksājumā.</span><span class="sxs-lookup"><span data-stu-id="0066e-313">This data source field exposes the SWIFT code of a vendor bank that is assigned the agent role in the processed vendor payment.</span></span>
13. <span data-ttu-id="0066e-314">Atlasiet **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="0066e-314">Select **Bind**.</span></span> <span data-ttu-id="0066e-315">Formāta elements **vendBankSWIFT** tagad ir saistīts ar datu avota lauku **model.Payment.CreditorAgent.BICFI**, lai SWIFT kodi tiktu ievadīti ģenerētajos maksājuma failos.</span><span class="sxs-lookup"><span data-stu-id="0066e-315">The **vendBankSWIFT** format element is now bound with the **model.Payment.CreditorAgent.BICFI** data source field, so that SWIFT codes will be entered in generated payment files.</span></span>

    ![Formāta elements vendBankSWIFT saistīts ar datu avota lauku model.Payment.CreditorAgent.BICFI ER operāciju veidotājā](./media/er-quick-start2-derived-format2.png)

14. <span data-ttu-id="0066e-317">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0066e-317">Select **Save**.</span></span>
15. <span data-ttu-id="0066e-318">Aizveriet veidotāja lapu.</span><span class="sxs-lookup"><span data-stu-id="0066e-318">Close the designer page.</span></span>

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a><span data-ttu-id="0066e-319">Pielāgota formāta atzīmēšana kā izpildāms</span><span class="sxs-lookup"><span data-stu-id="0066e-319">Mark a custom format as runnable</span></span>

<span data-ttu-id="0066e-320">Tagad, kad ir izveidota pielāgotā formāta pirmā versija un tai ir statuss **Melnraksts**, varat to palaist testēšanas nolūkos.</span><span class="sxs-lookup"><span data-stu-id="0066e-320">Now that the first version of your custom format has been created and has a status of **Draft**, you can run it for testing purposes.</span></span> <span data-ttu-id="0066e-321">Lai palaistu pārskatu, kreditora maksājums ir jāapstrādā, izmantojot maksāšanas metodi, kas attiecas uz pielāgoto ER formātu.</span><span class="sxs-lookup"><span data-stu-id="0066e-321">To run the report, you must process a vendor payment by using the payment method that refers to your custom ER format.</span></span> <span data-ttu-id="0066e-322">Pēc noklusējuma, izsaucot ER formātu no programmas, tiek [ņemtas vērā](general-electronic-reporting.md#component-versioning) tikai tās versijas, kuru statuss ir **Pabeigts** vai **Koplietots**.</span><span class="sxs-lookup"><span data-stu-id="0066e-322">By default, when you call an ER format from the application, only versions that have a status of **Completed** or **Shared** are [considered](general-electronic-reporting.md#component-versioning).</span></span> <span data-ttu-id="0066e-323">Šī darbība neļauj izmantot ER formātus, kuri nav pabeigti.</span><span class="sxs-lookup"><span data-stu-id="0066e-323">This behavior helps prevent ER formats that have unfinished designs from being used.</span></span> <span data-ttu-id="0066e-324">Tomēr testējot, programmai var likt izmantot ER formāta versiju ar statusu **Melnraksts**.</span><span class="sxs-lookup"><span data-stu-id="0066e-324">However, for your test runs, you can force the application to use the version of your ER format that has a status of **Draft**.</span></span> <span data-ttu-id="0066e-325">Šādā veidā var pielāgot pašreizējo formāta versiju, ja ir nepieciešamas kādas modifikācijas.</span><span class="sxs-lookup"><span data-stu-id="0066e-325">In this way, you can adjust the current format version if any modifications are required.</span></span> <span data-ttu-id="0066e-326">Papildinformāciju skatiet sadaļā [Piemērojamība](electronic-reporting-destinations.md#applicability).</span><span class="sxs-lookup"><span data-stu-id="0066e-326">For more information, see [Applicability](electronic-reporting-destinations.md#applicability).</span></span>

<span data-ttu-id="0066e-327">Lai izmantotu ER formāta melnraksta versiju, jums jāatzīmē ER formāts.</span><span class="sxs-lookup"><span data-stu-id="0066e-327">To use the draft version of an ER format, you must explicitly mark the ER format.</span></span>

1. <span data-ttu-id="0066e-328">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="0066e-328">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0066e-329">Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.</span><span class="sxs-lookup"><span data-stu-id="0066e-329">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="0066e-330">Dialoglodziņā **Lietotāja parametri** iestatiet opciju **Palaist iestatījumus** uz **Jā** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0066e-330">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
4. <span data-ttu-id="0066e-331">Atlasiet **Rediģēt**, lai pašreizējo lapu varētu rediģēt pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="0066e-331">Select **Edit** to make the current page editable, as required.</span></span>
5. <span data-ttu-id="0066e-332">Konfigurācijas koka skata kreisajā rūtī atlasiet **BACS (UK pielāgots)**.</span><span class="sxs-lookup"><span data-stu-id="0066e-332">In the configuration tree in the left pane, select **BACS (UK custom)**.</span></span>
6. <span data-ttu-id="0066e-333">Iestatiet opciju **Palaist melnrakstu** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="0066e-333">Set the **Run Draft** option to **Yes**.</span></span>

    ![Melnraksta opcijas palaišana lapā konfigurācijas](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a><span data-ttu-id="0066e-335">Kreditora maksājuma apstrādāšana, izmantojot pielāgotu ER formātu</span><span class="sxs-lookup"><span data-stu-id="0066e-335">Process a vendor payment by using the custom ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a><span data-ttu-id="0066e-336">Elektroniskā maksājuma metodes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="0066e-336">Set up the electronic payment method</span></span>

<span data-ttu-id="0066e-337">Elektroniskā maksājuma metode ir jākonfigurē, lai pielāgotais ER formāts tiktu izmantots kreditora maksājumu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="0066e-337">You must configure the electronic method of payment so that your custom ER format is used to process vendor payments.</span></span>

1. <span data-ttu-id="0066e-338">Dodieties uz **Kreditori** \> **Maksājuma iestatīšana** \> **Maksājuma metodes**.</span><span class="sxs-lookup"><span data-stu-id="0066e-338">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="0066e-339">Lapā **Maksājuma metodes – kreditori**, kreisajā rūtī atlasiet maksājuma metodi **Elektronisks**.</span><span class="sxs-lookup"><span data-stu-id="0066e-339">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="0066e-340">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="0066e-340">Select **Edit**.</span></span>
4. <span data-ttu-id="0066e-341">Kopsavilkuma cilnē **Faila formāts** iestatiet opciju **Vispārīgs elektroniskās eksportēšanas formāts** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="0066e-341">On the **File format** FastTab, set the **General electronic export format** option to **Yes**.</span></span>
5. <span data-ttu-id="0066e-342">Laukā **Eksporta formāta konfigurācija** atlasiet **BACS (UK pielāgots)** formāta konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="0066e-342">In the **Export format configuration** field, select the **BACS (UK custom)** format configuration.</span></span>

    ![Lapa Maksājuma metodes – kreditori](./media/er-quick-start2-method-of-payment2.png)

6. <span data-ttu-id="0066e-344">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0066e-344">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a><span data-ttu-id="0066e-345">Kreditora maksājuma apstrādāšana</span><span class="sxs-lookup"><span data-stu-id="0066e-345">Process a vendor payment</span></span>

1. <span data-ttu-id="0066e-346">Dodieties uz **Kreditori** \> **Maksājumi** \> **Kreditora maksājumu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="0066e-346">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="0066e-347">Lapā **Kreditora maksājumu žurnāls** atlasiet iepriekš izveidoto maksājumu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="0066e-347">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="0066e-348">Atlasiet **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="0066e-348">Select **Lines**.</span></span>
4. <span data-ttu-id="0066e-349">Lapā **Kreditora maksājumi** virs režģa atlasiet **Maksājuma statuss** \> **Nav**.</span><span class="sxs-lookup"><span data-stu-id="0066e-349">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="0066e-350">Atlasiet **Ģenerēt maksājumu**.</span><span class="sxs-lookup"><span data-stu-id="0066e-350">Select **Generate payment**.</span></span>
6. <span data-ttu-id="0066e-351">Dialoglodziņā **Ģenerēt maksājumus** ievadiet tālāk norādīto informāciju:</span><span class="sxs-lookup"><span data-stu-id="0066e-351">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="0066e-352">Laukā **Maksājuma metode** atlasiet **Elektronisks**.</span><span class="sxs-lookup"><span data-stu-id="0066e-352">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="0066e-353">Laukā **Bankas konts** atlasiet **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="0066e-353">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="0066e-354">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0066e-354">Select **OK**.</span></span>
8. <span data-ttu-id="0066e-355">Dialoglodziņā **Elektronisko pārskatu parametri** iestatiet opciju **Drukāt kontroles pārskatu** uz **Jā** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0066e-355">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0066e-356">Papildus maksājuma failam varat ģenerēt tikai kontroles pārskatu.</span><span class="sxs-lookup"><span data-stu-id="0066e-356">In addition to the payment file, you can generate only the control report.</span></span>

9. <span data-ttu-id="0066e-357">Lejupielādējiet zip failu un pēc tam no tā izvelciet tālāk norādītos failus:</span><span class="sxs-lookup"><span data-stu-id="0066e-357">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="0066e-358">Kontroles pārskats Excel formātā</span><span class="sxs-lookup"><span data-stu-id="0066e-358">The control report in Excel format</span></span>
    - <span data-ttu-id="0066e-359">Maksājuma fails TXT formāta</span><span class="sxs-lookup"><span data-stu-id="0066e-359">The payment file in TXT format</span></span>

        <span data-ttu-id="0066e-360">Ņemiet vērā, ka saskaņā ar pielāgotā ER formāta struktūru, maksājuma rinda ģenerētajā failā tagad [sākas](#PositionSWIFTCode) ar SWIFT kodu, kas tika [ievadīts](#DefineSWIFTCode) kreditora bankas kontam, kura maksājums ir apstrādāts.</span><span class="sxs-lookup"><span data-stu-id="0066e-360">Notice that, in accordance with the structure of your custom ER format, the payment line in the generated file now [starts](#PositionSWIFTCode) with the SWIFT code that was [entered](#DefineSWIFTCode) for the bank account of the vendor whose payment has been processed.</span></span>

        ![Maksājuma fails TXT formāta](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a><span data-ttu-id="0066e-362">Jaunas standarta ER formāta konfigurācijas versijas importēšana</span><span class="sxs-lookup"><span data-stu-id="0066e-362">Import new versions of the standard ER format configurations</span></span>

<span data-ttu-id="0066e-363">Šajā sadaļā sniegtā piemēra ietvaros, jūs saņemat ziņojumu par zināšanu bāzes rakstu [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span><span class="sxs-lookup"><span data-stu-id="0066e-363">For the example that is shown in this section, you receive a notification about Knowledge Base article [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span></span> <span data-ttu-id="0066e-364">Šis paziņojums informē par Microsoft publicētu jaunu **BACS (UK)** ER formāta versiju.</span><span class="sxs-lookup"><span data-stu-id="0066e-364">This notification informs you about the new version of the **BACS (UK)** ER format that has been published by Microsoft.</span></span> <span data-ttu-id="0066e-365">Papildus kontroles pārskatam, šī jaunā versija ļauj lietotājiem ģenerēt maksājuma izziņas pārskatu un dalības piezīmes pārskatu, kamēr kreditora maksājums tiek apstrādāts.</span><span class="sxs-lookup"><span data-stu-id="0066e-365">In addition to the control report, this new version lets users generate the payment advice report and the attending note report while a vendor payment is being processed.</span></span> <span data-ttu-id="0066e-366">Noteikti izmēģiniet šo funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="0066e-366">You want to start to use that functionality.</span></span>

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a><span data-ttu-id="0066e-367">Jaunas standarta ER konfigurācijas versijas importēšana</span><span class="sxs-lookup"><span data-stu-id="0066e-367">Import new versions of the standard ER configurations</span></span>

<span data-ttu-id="0066e-368">Lai ER konfigurācijas jaunās versijas pievienotu pašreizējai Finance instancei, jums tās ir jāimportē no konfigurētā ER [repozitorija](general-electronic-reporting.md#Repository).</span><span class="sxs-lookup"><span data-stu-id="0066e-368">To add new versions of the ER configurations to the current Finance instance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that you've configured.</span></span>

1. <span data-ttu-id="0066e-369">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="0066e-369">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="0066e-370">Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Microsoft** un pēc tam atlasiet **Repozitoriji**, lai skatītu Microsoft nodrošinātāja repozitoriju sarakstu.</span><span class="sxs-lookup"><span data-stu-id="0066e-370">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="0066e-371">Lapā **Konfigurācijas repozitoriji** atlasiet repozitoriju ar veidu **Globāls** un pēc tam atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="0066e-371">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="0066e-372">Ja tiek pieprasīta autorizācija savienojumam ar Regulatory Configuration Service, izpildiet autorizācijas norādījumus.</span><span class="sxs-lookup"><span data-stu-id="0066e-372">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="0066e-373">Lapā **Konfigurācijas repozitorijs** konfigurācijas koka skata kreisajā rūtī atlasiet **BACS (UK)** formāta konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="0066e-373">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="0066e-374">Kopsavilkuma cilnē **Versijas** izvēlieties atlasītās ER formāta konfigurācijas **3.3** versiju.</span><span class="sxs-lookup"><span data-stu-id="0066e-374">On the **Versions** FastTab, select version **3.3** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="0066e-375">Atlasiet **Importēt**, lai lejupielādētu atlasīto versiju no globālā repozitorija uz pašreizējo Finance instanci.</span><span class="sxs-lookup"><span data-stu-id="0066e-375">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![Konfigurācijas repozitorijas lapa.](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> <span data-ttu-id="0066e-377">Ja rodas problēmas ar piekļuvi [globālajam repozitorijam](er-download-configurations-global-repo.md), tā vietā varat [lejupielādēt konfigurācijas](download-electronic-reporting-configuration-lcs.md) no LCS.</span><span class="sxs-lookup"><span data-stu-id="0066e-377">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from LCS instead.</span></span>

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a><span data-ttu-id="0066e-378">Importētās ER formāta konfigurācijas pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="0066e-378">Review the imported ER format configurations</span></span>

1. <span data-ttu-id="0066e-379">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="0066e-379">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="0066e-380">Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="0066e-380">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="0066e-381">Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Maksājuma modelis** un pēc tam atlasiet **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="0066e-381">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span>
4. <span data-ttu-id="0066e-382">Kopsavilkuma cilnē **Versijas** atlasiet versiju **3.3**.</span><span class="sxs-lookup"><span data-stu-id="0066e-382">On the **Versions** FastTab, select version **3.3**.</span></span>
5. <span data-ttu-id="0066e-383">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="0066e-383">Select **Designer**.</span></span>
6. <span data-ttu-id="0066e-384">Lapā **Formāta veidotājs** izvērsiet formāta elementu **BACSReportsFolder**.</span><span class="sxs-lookup"><span data-stu-id="0066e-384">On the **Format designer** page, expand the **BACSReportsFolder** format element.</span></span>
7.  <span data-ttu-id="0066e-385">Ņemiet vērā, ka versija 3.3 ietver formāta elementu **PaymentAdviceReport**, kas tiek izmantots, lai ģenerētu maksājuma izziņas pārskatu, apstrādājot kreditora maksājumu.</span><span class="sxs-lookup"><span data-stu-id="0066e-385">Notice that version 3.3 contains the **PaymentAdviceReport** format element that is used to generate a payment advice report when a vendor payment is processed.</span></span>

    ![PaymentAdviceReport formāta elements ER operāciju veidotājā](./media/er-quick-start2-imported-solution2.png)

8. <span data-ttu-id="0066e-387">Aizveriet veidotāja lapu.</span><span class="sxs-lookup"><span data-stu-id="0066e-387">Close the designer page.</span></span>

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a><span data-ttu-id="0066e-388">Importētā formāta jaunās versijas izmaiņu pieņemšana pielāgotajā formātā</span><span class="sxs-lookup"><span data-stu-id="0066e-388">Adopt the changes in the new version of an imported format in a custom format</span></span>

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a><span data-ttu-id="0066e-389">Pielāgotā formāta pašreizējās melnraksta versijas pabeigšana</span><span class="sxs-lookup"><span data-stu-id="0066e-389">Complete the current draft version of a custom format</span></span>

<span data-ttu-id="0066e-390">Ja vēlaties saglabāt pašreizējo pielāgotā formāta stāvokli, pabeidziet melnraksta versiju 1.1.1, mainot statusu no **Melnraksts** uz **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="0066e-390">If you want to keep the current state of your custom format, complete the draft version 1.1.1 by changing its status from **Draft** to **Completed**.</span></span>

1. <span data-ttu-id="0066e-391">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="0066e-391">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="0066e-392">Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="0066e-392">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="0066e-393">Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Maksājuma modelis**, izvērsiet **BACS (UK)** un pēc tam atlasiet **BACS (UK pielāgots)**.</span><span class="sxs-lookup"><span data-stu-id="0066e-393">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, expand **BACS (UK)**, and then select **BACS (UK custom)**.</span></span>
4. <span data-ttu-id="0066e-394">Kopsavilkuma cilnē **Versijas** atlasiet **Mainīt statusu** \> **Pabeigts** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0066e-394">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="0066e-395">Versijas 1.1.1 statuss tiek mainīts no **Melnraksts** uz **Pabeigts** un versija kļūst tikai lasāma.</span><span class="sxs-lookup"><span data-stu-id="0066e-395">The status of version 1.1.1 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="0066e-396">Ir pievienota jauna rediģējama versija, 1.1.2, un tās statuss ir **Melnraksts**.</span><span class="sxs-lookup"><span data-stu-id="0066e-396">A new editable version, 1.1.2, has been added and has a status of **Draft**.</span></span> <span data-ttu-id="0066e-397">Varat izmantot šo versiju, lai veiktu turpmākās izmaiņas pielāgotajā ER formātā.</span><span class="sxs-lookup"><span data-stu-id="0066e-397">You can use this version to make further changes in your custom ER format.</span></span>

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a><span data-ttu-id="0066e-398">Pielāgotā formāta pārvietošana uz jaunu bāzes versiju</span><span class="sxs-lookup"><span data-stu-id="0066e-398">Rebase a custom format to a new base version</span></span>

<span data-ttu-id="0066e-399">Lai pielāgojumam sāktu izmantot jauno versijas 3.3 formāta funkcionalitāti **BACS (UK)**, ir jāmaina pielāgotās konfigurācijas **BACS (UK pielāgots)** bāzes konfigurācijas versija.</span><span class="sxs-lookup"><span data-stu-id="0066e-399">To start to use the new functionality of version 3.3 of the **BACS (UK)** format in your customization, you must change the base configuration version for the custom configuration, **BACS (UK custom)**.</span></span> <span data-ttu-id="0066e-400">Šis process tiek saukts par [pārbāzēšanu](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span><span class="sxs-lookup"><span data-stu-id="0066e-400">This process is known as [rebasing](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span></span> <span data-ttu-id="0066e-401">1.1 **BACS (UK)** versijas vietā, izmantojiet 3.3 versiju.</span><span class="sxs-lookup"><span data-stu-id="0066e-401">Instead of version 1.1 of **BACS (UK)**, use version 3.3.</span></span>

1. <span data-ttu-id="0066e-402">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="0066e-402">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0066e-403">Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Maksājuma modelis** un pēc tam atlasiet **BACS (UK pielāgots)**.</span><span class="sxs-lookup"><span data-stu-id="0066e-403">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="0066e-404">Kopsavilkuma cilnē **Versijas** atlasiet versiju **1.1.2** un pēc tam atlasiet **Pārveidot**.</span><span class="sxs-lookup"><span data-stu-id="0066e-404">On the **Versions** FastTab, select version **1.1.2**, and then select **Rebase**.</span></span>
4. <span data-ttu-id="0066e-405">Dialoglodziņā **Pārveidošana** laukā **Mērķa versija** atlasiet bāzes konfigurācijas versiju **3.3**, lai to lietotu kā jauno bāzi, un izmantotu, lai atjauninātu konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="0066e-405">In the **Rebase** dialog box, in the **Target version** field, select version **3.3** of the base configuration to apply it as the new base and use it to update the configuration.</span></span>

    ![Dialoglodziņš Pārskatīt](./media/er-quick-start2-rebase1.png)

5. <span data-ttu-id="0066e-407">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0066e-407">Select **OK**.</span></span>
6. <span data-ttu-id="0066e-408">Ņemiet vērā, ka melnraksta versijas numurs ir mainīts no **1.1.2** uz **3.3.2**, lai atspoguļotu izmaiņas bāzes versijā.</span><span class="sxs-lookup"><span data-stu-id="0066e-408">Notice that the number of the draft version has been changed from **1.1.2** to **3.3.2** to reflect the change in the base version.</span></span>

    <span data-ttu-id="0066e-409">Sapludinot pielāgotu versiju un jaunu bāzes versiju, var tikt konstatēti konflikti formāta izmaiņu dēļ, ko nevar sapludināt automātiski.</span><span class="sxs-lookup"><span data-stu-id="0066e-409">When the custom version and a new base version are merged, some conflicts might be discovered because of format changes that can't be merged automatically.</span></span>

    ![Pārveidota konfigurācija ar konfliktiem lapā Konfigurācijas](./media/er-quick-start2-rebase2.png)

    <span data-ttu-id="0066e-411">Ja tiek konstatēti konflikti, tie ir manuāli jāatrisina formāta veidotājā.</span><span class="sxs-lookup"><span data-stu-id="0066e-411">If conflicts are discovered, they must be manually resolved in the format designer.</span></span>

7. <span data-ttu-id="0066e-412">Kopsavilkuma cilnē **Versijas** atlasiet versiju **3.3.2**.</span><span class="sxs-lookup"><span data-stu-id="0066e-412">On the **Versions** FastTab, select version **3.3.2**.</span></span>
8. <span data-ttu-id="0066e-413">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="0066e-413">Select **Designer**.</span></span>
9. <span data-ttu-id="0066e-414">Lapā **Formāta veidotājs** kopsavilkuma cilnē **Detalizēti** atlasiet pārveides konflikta ierakstu un pēc tam atlasiet **Lietot bāzes vērtību**.</span><span class="sxs-lookup"><span data-stu-id="0066e-414">On the **Format designer** page, on the **Details** FastTab, select a rebase conflict record, and then select **Apply base value**.</span></span>

    ![Pārveides konflikta ieraksts ER operāciju veidotājā](./media/er-quick-start2-rebase3.png)

10. <span data-ttu-id="0066e-416">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0066e-416">Select **Save**.</span></span>

    <span data-ttu-id="0066e-417">Pārveides konflikta ierakstam vairs nevajadzētu parādīties kopsavilkuma cilnē **Detalizēti**.</span><span class="sxs-lookup"><span data-stu-id="0066e-417">The rebase conflict record should no longer appear on the **Details** FastTab.</span></span>

    ![Konflikts atrisināts ER operāciju veidotājā](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > <span data-ttu-id="0066e-419">Konflikts tika atrisināts, apstiprinot, ka bāzes modeļa 3. versija ir jālieto šajā ER formātā.</span><span class="sxs-lookup"><span data-stu-id="0066e-419">You resolved the conflict by confirming that version 3 of the base model must be used in this ER format.</span></span>

11. <span data-ttu-id="0066e-420">Izvērsiet **BACSReportsFolder** \> **fails** \> **transakcijas** \> **transakcija**.</span><span class="sxs-lookup"><span data-stu-id="0066e-420">Expand **BACSReportsFolder** \> **file** \> **transactions** \> **transaction**.</span></span>
12. <span data-ttu-id="0066e-421">Ņemiet vērā, ka cilnē **Kartēšana** jūsu pielāgotā ER formāta versija 3.3.2 ietver gan pielāgojumu (formāta elementu **vendBankSWIFT** un tā saistījumu), gan bāzes ER formāta versijas 3.3 jauno funkcionalitāti, ko nodrošina Microsoft (formāta elementu **PaymentAdviceReport** kopā ar tā ligzdotajiem elementiem un konfigurētajiem saistījumiem).</span><span class="sxs-lookup"><span data-stu-id="0066e-421">On the **Mapping** tab, notice that version 3.3.2 of your custom ER format contains both your customization (the **vendBankSWIFT** format element and its binding) and the new functionality of version 3.3 of the base ER format that was provided by Microsoft (the **PaymentAdviceReport** format element together with its nested elements and configured bindings).</span></span> <span data-ttu-id="0066e-422">Veicot dažus peles klikšķus, esat pieņēmis jaunas bāzes versijas modifikācijas, sapludinot tās ar pielāgojumu.</span><span class="sxs-lookup"><span data-stu-id="0066e-422">In just a few mouse clicks, you adopted the modifications of a new base version by merging them with your customization.</span></span>

    ![Sapludināts formāts ER operāciju veidotājā](./media/er-quick-start2-rebase5.png)

13. <span data-ttu-id="0066e-424">Aizveriet veidotāja lapu.</span><span class="sxs-lookup"><span data-stu-id="0066e-424">Close the designer page.</span></span>

> [!NOTE]
> <span data-ttu-id="0066e-425">Pārveides darbība ir atgriezeniska.</span><span class="sxs-lookup"><span data-stu-id="0066e-425">The rebase action is reversible.</span></span> <span data-ttu-id="0066e-426">Lai atceltu pārveidi, atlasiet formāta **BACS (UK pielāgots)** versiju **1.1.1** kopsavilkuma cilnē **Versijas** un pēc tam atlasiet **Iegūt šo versiju**.</span><span class="sxs-lookup"><span data-stu-id="0066e-426">To cancel this rebase, select version **1.1.1** of the **BACS (UK custom)** format on the **Versions** FastTab, and then select **Get this version**.</span></span> <span data-ttu-id="0066e-427">Versija 3.3.2 tiks pārnumurēta par 1.1.2 un melnraksta versijas 1.1.2 saturs atbildīs versijas 1.1.1 saturam.</span><span class="sxs-lookup"><span data-stu-id="0066e-427">Version 3.3.2 will then be renumbered 1.1.2, and the content of draft version 1.1.2 will match the content of version 1.1.1.</span></span>

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a><span data-ttu-id="0066e-428">Kreditora maksājuma apstrādāšana, izmantojot pārveidotu ER formātu</span><span class="sxs-lookup"><span data-stu-id="0066e-428">Process a vendor payment by using a rebased ER format</span></span>

1. <span data-ttu-id="0066e-429">Dodieties uz **Kreditori** \> **Maksājumi** \> **Kreditora maksājumu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="0066e-429">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="0066e-430">Lapā **Kreditora maksājumu žurnāls** atlasiet iepriekš izveidoto maksājumu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="0066e-430">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="0066e-431">Atlasiet **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="0066e-431">Select **Lines**.</span></span>
4. <span data-ttu-id="0066e-432">Lapā **Kreditora maksājumi** virs režģa atlasiet **Maksājuma statuss** \> **Nav**.</span><span class="sxs-lookup"><span data-stu-id="0066e-432">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="0066e-433">Atlasiet **Ģenerēt maksājumu**.</span><span class="sxs-lookup"><span data-stu-id="0066e-433">Select **Generate payment**.</span></span>
6. <span data-ttu-id="0066e-434">Dialoglodziņā **Ģenerēt maksājumus** ievadiet tālāk norādīto informāciju:</span><span class="sxs-lookup"><span data-stu-id="0066e-434">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="0066e-435">Laukā **Maksājuma metode** atlasiet **Elektronisks**.</span><span class="sxs-lookup"><span data-stu-id="0066e-435">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="0066e-436">Laukā **Bankas konts** atlasiet **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="0066e-436">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="0066e-437">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0066e-437">Select **OK**.</span></span>
8. <span data-ttu-id="0066e-438">Dialoglodziņā **Elektronisko pārskatu parametri** ievadiet tālāk norādīto informāciju:</span><span class="sxs-lookup"><span data-stu-id="0066e-438">In the **Electronic report parameters** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="0066e-439">Iestatiet opciju **Drukāt kontroles pārskatu** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="0066e-439">Set the **Print control report** option to **Yes**.</span></span>
    - <span data-ttu-id="0066e-440">Iestatiet opciju **Drukāt maksājuma izziņu** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="0066e-440">Set the **Print payment advice** option to **Yes**.</span></span>

    ![Dialoglodziņš Elektronisko pārskatu parametri](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > <span data-ttu-id="0066e-442">Papildus maksājuma failam tagad varat ģenerēt gan kontroles pārskatu, gan maksājuma izziņas pārskatu.</span><span class="sxs-lookup"><span data-stu-id="0066e-442">In addition to the payment file, you can now generate both the control report and the payment advice report.</span></span>

9. <span data-ttu-id="0066e-443">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0066e-443">Select **OK**.</span></span>
10. <span data-ttu-id="0066e-444">Lejupielādējiet zip failu un pēc tam no tā izvelciet tālāk norādītos failus:</span><span class="sxs-lookup"><span data-stu-id="0066e-444">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="0066e-445">Kontroles pārskats Excel formātā</span><span class="sxs-lookup"><span data-stu-id="0066e-445">The control report in Excel format</span></span>
    - <span data-ttu-id="0066e-446">Maksājuma izziņas pārskats Excel formātā</span><span class="sxs-lookup"><span data-stu-id="0066e-446">The payment advice report in Excel format</span></span>

        ![Maksājuma izziņas pārskats Excel formātā](./media/er-quick-start2-payment-advice-report.png)

    - <span data-ttu-id="0066e-448">Maksājuma fails TXT formāta</span><span class="sxs-lookup"><span data-stu-id="0066e-448">The payment file in TXT format</span></span>

        <span data-ttu-id="0066e-449">Ņemiet vērā, ka maksājuma rinda ģenerētajā failā sākas ar SWIFT kodu, kas tika ievadīts kreditora bankas kontam, kura maksājums ir apstrādāts.</span><span class="sxs-lookup"><span data-stu-id="0066e-449">Notice that the payment line in the generated file starts  with the SWIFT code that was entered for the bank account of a vendor whose payment has been processed.</span></span>

        ![Maksājuma fails TXT formāta](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a><span data-ttu-id="0066e-451">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="0066e-451">Additional resources</span></span>

- [<span data-ttu-id="0066e-452">Elektronisko pārskatu veidošanas apskats</span><span class="sxs-lookup"><span data-stu-id="0066e-452">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="0066e-453">ER konfigurāciju lejupielāde no Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="0066e-453">Download ER configurations from Lifecycle Services</span></span>](download-electronic-reporting-configuration-lcs.md)
- [<span data-ttu-id="0066e-454">ER konfigurāciju lejupielāde no konfigurācijas pakalpojuma globālā repozitorija</span><span class="sxs-lookup"><span data-stu-id="0066e-454">Download ER configurations from Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)
