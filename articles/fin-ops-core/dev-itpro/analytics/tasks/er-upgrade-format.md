---
title: ER Jaunināt savu formātu, pieņemot šī formāta jaunu bāzes versiju
description: Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var uzturēt formāta konfigurāciju Elektroniskajos pārskatos (ER).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 17fe6d772040c73959685920743225c128421951
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684264"
---
# <a name="er-upgrade-your-format-by-adopting-a-new-base-version-of-that-format"></a><span data-ttu-id="07ee9-103">ER Jaunināt savu formātu, pieņemot šī formāta jaunu bāzes versiju</span><span class="sxs-lookup"><span data-stu-id="07ee9-103">ER Upgrade your format by adopting a new, base version of that format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="07ee9-104">Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var uzturēt formāta konfigurāciju Elektroniskajos pārskatos (ER).</span><span class="sxs-lookup"><span data-stu-id="07ee9-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can maintain an Electronic reporting (ER) format configuration.</span></span> <span data-ttu-id="07ee9-105">Šī procedūra skaidro kā var izveidot pielāgotu formātu versiju, balstoties uz formātu, kas saņemts no konfigurācijas sniedzēja (CP).</span><span class="sxs-lookup"><span data-stu-id="07ee9-105">This procedure explains how a custom version of a format can be created based on the format received from a configuration provider (CP).</span></span> <span data-ttu-id="07ee9-106">Tas arī skaidro, kā pieņemt jaunu, šī formāta bāzes versiju.</span><span class="sxs-lookup"><span data-stu-id="07ee9-106">It also explains how to adopt a new, base version of that format.</span></span>

<span data-ttu-id="07ee9-107">Lai veiktu šīs darbības, vispirms jāveic darbības procedūrās "Izveidot konfigurācijas nodrošinātāju un iezīmēt to kā aktīvu" un "Izmantot izveidoto formātu, lai ģenerētu elektroniskos dokumentus maksājumiem".</span><span class="sxs-lookup"><span data-stu-id="07ee9-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" and "Use created format to generate electronic documents for payments" procedures.</span></span> <span data-ttu-id="07ee9-108">Šīs darbības var veikt uzņēmumā GBSI.</span><span class="sxs-lookup"><span data-stu-id="07ee9-108">These steps can be performed in the GBSI company.</span></span>

## <a name="select-format-configuration-for-customization"></a><span data-ttu-id="07ee9-109">Atlasiet formāta konfigurāciju pielāgošanai</span><span class="sxs-lookup"><span data-stu-id="07ee9-109">Select format configuration for customization</span></span>
1. <span data-ttu-id="07ee9-110">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="07ee9-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="07ee9-111">Šajā piemērā parauga uzņēmums “Litware, Inc.” (https://www.litware.com) ir konfigurācijas nodrošinātājs, kas atbalsta formāta konfigurācijas elektroniskajiem maksājumiem attiecībā uz konkrētu valsti.</span><span class="sxs-lookup"><span data-stu-id="07ee9-111">In this example, sample company Litware, Inc. (https://www.litware.com) will act as a configuration provider that supports format configurations for electronic payments for a particular country.</span></span>    <span data-ttu-id="07ee9-112">Parauga uzņēmums “Proseware, Inc.” (http://www.proseware.com) darbosies kā “Litware, Inc.” nodrošinātās formāta konfigurācijas patērētājs.</span><span class="sxs-lookup"><span data-stu-id="07ee9-112">Sample company Proseware, Inc. (http://www.proseware.com) will act as a consumer of the format configuration that Litware, Inc. provided.</span></span> <span data-ttu-id="07ee9-113">Proseware, Inc. izmanto formātus noteiktos attiecīgās valsts reģionos.</span><span class="sxs-lookup"><span data-stu-id="07ee9-113">Proseware, Inc. uses formats in certain regions of that country.</span></span>  
2. <span data-ttu-id="07ee9-114">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="07ee9-114">Click Reporting configurations.</span></span>
3. <span data-ttu-id="07ee9-115">Noklikšķiniet uz Rādīt filtrus.</span><span class="sxs-lookup"><span data-stu-id="07ee9-115">Click Show filters.</span></span>
4. <span data-ttu-id="07ee9-116">Lietojiet šādus filtrus: Ievadiet “BAKS (UK fiktīvs)” filtra vērtību laukā “Nosaukums”, izmantojot filtra operatoru “sākas ar”.</span><span class="sxs-lookup"><span data-stu-id="07ee9-116">Apply the following filters: Enter a filter value of "BACS (UK fictitious)" on the "Name" field using the "begins with" filter operator.</span></span>
  
    <span data-ttu-id="07ee9-117">Atlasītā BAKS (UK fiktīvs) formāta konfigurācija pieder nodrošinātājam Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="07ee9-117">The selected format configuration BACS (UK fictitious) is owned by provider Litware, Inc.</span></span>  

5. <span data-ttu-id="07ee9-118">Noklikšķiniet uz Rādīt filtrus.</span><span class="sxs-lookup"><span data-stu-id="07ee9-118">Click Show filters.</span></span>
6. <span data-ttu-id="07ee9-119">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="07ee9-119">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="07ee9-120">Šo formāta versiju ar statusu Pabeigts uzņēmums Proseware, Inc. izmanto pielāgošanai.</span><span class="sxs-lookup"><span data-stu-id="07ee9-120">The version of the format with the status of Completed will be used by Proseware, Inc. for customization.</span></span>  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a><span data-ttu-id="07ee9-121">Izveidojiet jaunu konfigurāciju jūsu elektroniskā dokumenta pielāgotajam formātam</span><span class="sxs-lookup"><span data-stu-id="07ee9-121">Create a new configuration for your custom format of electronic document</span></span>
<span data-ttu-id="07ee9-122">Proseware, Inc. saņēma BACS (UK fiktīvs) konfigurācijas versiju 1.1, kurā ietverts sākotnējais formāts elektronisko maksājumu dokumentu ģenerēšanai no Litware, Inc. saskaņā ar attiecīgo pakalpojuma abonementu.</span><span class="sxs-lookup"><span data-stu-id="07ee9-122">Proseware, Inc. received version 1.1 of BACS (UK fictitious) configuration that contains the initial format to generate electronic payment documents from Litware, Inc. in accordance to their service subscription.</span></span> <span data-ttu-id="07ee9-123">Proseware, Inc. vēlas sākt lietot šo metodi kā standartu savā valstī, tomēr ir nepieciešama pielāgošana, lai nodrošinātu atbalstu noteiktām reģionālajām prasībām.</span><span class="sxs-lookup"><span data-stu-id="07ee9-123">Proseware, Inc. wants to start using this as a standard for their country but some customization is required to support specific regional requirements.</span></span> <span data-ttu-id="07ee9-124">Proseware, Inc. arī vēlas saglabāt iespēju jaunināt pielāgotu formātu, tiklīdz Litware, Inc. piedāvā jaunu tā versiju (ar izmaiņām, kas nodrošina atbalstu jaunām valstij raksturīgām prasībām), kā arī vēlas veikt jaunināšanu ar pēc iespējas zemākām izmaksām.</span><span class="sxs-lookup"><span data-stu-id="07ee9-124">Proseware, Inc. also wants to keep the ability to upgrade a custom format as soon as a new version of it (with changes to support new country-specific requirements) comes from Litware, Inc. and they want to perform this upgrade with the lowest cost.</span></span>  

<span data-ttu-id="07ee9-125">Lai to izdarītu, Proseware, Inc. ir jāizveido konfigurācija, kā bāzi izmantojot Litware, Inc konfigurāciju BACS (UK fiktīvs).</span><span class="sxs-lookup"><span data-stu-id="07ee9-125">To do this, Proseware, Inc. needs to create a configuration using the Litware, Inc. configuration BACS (UK fictitious) as a base.</span></span>  

1. <span data-ttu-id="07ee9-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="07ee9-126">Close the page.</span></span>
2. <span data-ttu-id="07ee9-127">Atlasiet Proseware, Inc., lai to padarītu par aktīvu nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="07ee9-127">Select Proseware, Inc. to make it an active provider.</span></span>
3. <span data-ttu-id="07ee9-128">Noklikšķiniet uz Iestatīt aktīvu.</span><span class="sxs-lookup"><span data-stu-id="07ee9-128">Click Set active.</span></span>
4. <span data-ttu-id="07ee9-129">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="07ee9-129">Click Reporting configurations.</span></span>
5. <span data-ttu-id="07ee9-130">Kokā izvērsiet “Maksājumi (vienkāršotais modelis)”.</span><span class="sxs-lookup"><span data-stu-id="07ee9-130">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="07ee9-131">Kokā atlasiet 'Maksājumi (vienkāršotais modelis)\BAKS (UK fiktīvs)'.</span><span class="sxs-lookup"><span data-stu-id="07ee9-131">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="07ee9-132">Atlasiet konfigurāciju BACS (UK fiktīvs) no Litware, Inc. Uzņēmums Proseware, Inc. izmantos versiju 1.1. kā pielāgotās versijas bāzi.</span><span class="sxs-lookup"><span data-stu-id="07ee9-132">Select the BACS (UK fictitious) configuration from Litware, Inc. Proseware, Inc. will use version 1.1 as a base for the custom version.</span></span>  

7. <span data-ttu-id="07ee9-133">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="07ee9-133">Click Create configuration to open the drop dialog.</span></span>

    <span data-ttu-id="07ee9-134">Tas jums ļauj izveidot jaunu konfigurāciju pielāgotam maksājuma formātam.</span><span class="sxs-lookup"><span data-stu-id="07ee9-134">This lets you create a new configuration for a custom payment format.</span></span>  

8. <span data-ttu-id="07ee9-135">Jaunajā laukā, ievadiet 'Atvasināt no nosaukuma: BAKS (UK fiktīvs), Litware, Inc.'.</span><span class="sxs-lookup"><span data-stu-id="07ee9-135">In the New field, enter 'Derive from Name: BACS (UK fictitious), Litware, Inc.'.</span></span>

    <span data-ttu-id="07ee9-136">Atlasiet opciju Atvasināt, lai apstiprinātu BAKS (UK fiktīvs) izmantošanu kā pamatu pielāgotas versijas veidošanai.</span><span class="sxs-lookup"><span data-stu-id="07ee9-136">Select the Derive option to confirm the usage of BACS (UK fictitious) as the base for creating the custom version.</span></span>  

9. <span data-ttu-id="07ee9-137">Laukā Nosaukums ierakstiet 'BAKS (UK fiktīvs pielāgots)'.</span><span class="sxs-lookup"><span data-stu-id="07ee9-137">In the Name field, type 'BACS (UK fictitious custom)'.</span></span>
10. <span data-ttu-id="07ee9-138">Laukā Apraksts ierakstiet “BAKS kreditora maksājums (UK fiktīvs pielāgots)”.</span><span class="sxs-lookup"><span data-stu-id="07ee9-138">In the Description field, type 'BACS vendor payment (UK fictitious custom)'.</span></span>

    <span data-ttu-id="07ee9-139">Šeit tiek automātiski ievadīts aktīvais konfigurācijas nodrošinātājs (Proseware, Inc.).</span><span class="sxs-lookup"><span data-stu-id="07ee9-139">The active configuration provider (Proseware, Inc.) is automatically entered here.</span></span> <span data-ttu-id="07ee9-140">Šis nodrošinātājs varēs uzturēt šo konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="07ee9-140">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="07ee9-141">Citi nodrošinātāji var izmantot šo konfigurāciju, bet nevar uzturēt to.</span><span class="sxs-lookup"><span data-stu-id="07ee9-141">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

11. <span data-ttu-id="07ee9-142">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="07ee9-142">Click Create configuration.</span></span>

## <a name="customize-your-format-for-the-electronic-document"></a><span data-ttu-id="07ee9-143">Pielāgojiet jūsu elektroniskā dokumenta formātu</span><span class="sxs-lookup"><span data-stu-id="07ee9-143">Customize your format for the electronic document</span></span>
1. <span data-ttu-id="07ee9-144">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="07ee9-144">Click Designer.</span></span>
2. <span data-ttu-id="07ee9-145">Noklikšķiniet uz Izvērst/sakļaut.</span><span class="sxs-lookup"><span data-stu-id="07ee9-145">Click Expand/collapse.</span></span>
3. <span data-ttu-id="07ee9-146">Noklikšķiniet uz Izvērst/sakļaut.</span><span class="sxs-lookup"><span data-stu-id="07ee9-146">Click Expand/collapse.</span></span>
4. <span data-ttu-id="07ee9-147">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka”.</span><span class="sxs-lookup"><span data-stu-id="07ee9-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="07ee9-148">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="07ee9-148">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="07ee9-149">Kokā atlasiet "XML\Elements".</span><span class="sxs-lookup"><span data-stu-id="07ee9-149">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="07ee9-150">Laukā Nosaukums ierakstiet "IBAN".</span><span class="sxs-lookup"><span data-stu-id="07ee9-150">In the Name field, type 'IBAN'.</span></span>
8. <span data-ttu-id="07ee9-151">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="07ee9-151">Click OK.</span></span>
9. <span data-ttu-id="07ee9-152">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka\IBAN”.</span><span class="sxs-lookup"><span data-stu-id="07ee9-152">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\IBAN'.</span></span>
10. <span data-ttu-id="07ee9-153">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="07ee9-153">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="07ee9-154">Kokā atlasiet elementu “Teksts\Virkne”.</span><span class="sxs-lookup"><span data-stu-id="07ee9-154">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="07ee9-155">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="07ee9-155">Click OK.</span></span>
13. <span data-ttu-id="07ee9-156">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Nosaukums\Virkne”.</span><span class="sxs-lookup"><span data-stu-id="07ee9-156">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="07ee9-157">Ievadiet '60' laukā Maksimālais garums.</span><span class="sxs-lookup"><span data-stu-id="07ee9-157">In the Maximum length field, enter '60'.</span></span>
15. <span data-ttu-id="07ee9-158">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="07ee9-158">Click the Mapping tab.</span></span>
16. <span data-ttu-id="07ee9-159">Koka struktūrā izvērsiet elementu “modelis”.</span><span class="sxs-lookup"><span data-stu-id="07ee9-159">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="07ee9-160">Kokā izvērsiet sadaļu “modelis\Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="07ee9-160">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="07ee9-161">Kokā izvērsiet sadaļu “modelis\Maksājumi\Kreditors”.</span><span class="sxs-lookup"><span data-stu-id="07ee9-161">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="07ee9-162">Kokā izvērsiet elementu “modelis\Maksājumi\Kreditors\Konts“.</span><span class="sxs-lookup"><span data-stu-id="07ee9-162">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
20. <span data-ttu-id="07ee9-163">Koka struktūrā atlasiet zaru “modelis\Maksājumi\Kreditors\Konts\IBAN”.</span><span class="sxs-lookup"><span data-stu-id="07ee9-163">In the tree, select 'model\Payments\Creditor\Account\IBAN'.</span></span>
21. <span data-ttu-id="07ee9-164">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums = model.Payments\Kreditors\Banka\IBAN\Virkne”.</span><span class="sxs-lookup"><span data-stu-id="07ee9-164">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\IBAN\String'.</span></span>
22. <span data-ttu-id="07ee9-165">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="07ee9-165">Click Bind.</span></span>
23. <span data-ttu-id="07ee9-166">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="07ee9-166">Click Save.</span></span>

## <a name="validate-the-customized-format"></a><span data-ttu-id="07ee9-167">Pārbaudiet pielāgoto formātu</span><span class="sxs-lookup"><span data-stu-id="07ee9-167">Validate the customized format</span></span>
1. <span data-ttu-id="07ee9-168">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="07ee9-168">Click Validate.</span></span>

    <span data-ttu-id="07ee9-169">Pārbaudiet pielāgotā formāta izkārtojumu un datu kartējuma izmaiņas, lai pārliecinātos, ka visi saistījumi ir pareizi.</span><span class="sxs-lookup"><span data-stu-id="07ee9-169">Validate the customized format layout and data mapping changes to make sure that all bindings are okay.</span></span>  

2. <span data-ttu-id="07ee9-170">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="07ee9-170">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a><span data-ttu-id="07ee9-171">Mainīt pielāgotā formāta konfigurācijas pašreizējās versijas statusu</span><span class="sxs-lookup"><span data-stu-id="07ee9-171">Change the status of the current version of the custom format configuration</span></span>
<span data-ttu-id="07ee9-172">Izveidotās formāta konfigurācijas statusu no Melnraksts mainiet uz Pabeigts, lai to padarītu pieejamu maksājumu dokumenta ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="07ee9-172">Change the status of the designed format configuration from Draft to Completed to make it available for payment document generation.</span></span>  

1. <span data-ttu-id="07ee9-173">Noklikšķiniet uz Mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="07ee9-173">Click Change status.</span></span>

    <span data-ttu-id="07ee9-174">Ņemiet vērā, ka atlasītās konfigurācijas pašreizējai versijai ir statuss Melnraksts.</span><span class="sxs-lookup"><span data-stu-id="07ee9-174">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="07ee9-175">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="07ee9-175">Click Complete.</span></span>
3. <span data-ttu-id="07ee9-176">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="07ee9-176">In the Description field, type a value.</span></span>
4. <span data-ttu-id="07ee9-177">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="07ee9-177">Click OK.</span></span>
5. <span data-ttu-id="07ee9-178">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="07ee9-178">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="07ee9-179">Ņemiet vērā, ka izveidotā konfigurācija tiek saglabāta kā pabeigta versija 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="07ee9-179">Note that the created configuration is saved as completed version 1.1.1.</span></span> <span data-ttu-id="07ee9-180">Tas nozīmē, ka tā ir 1. versija pielāgotajam formātam BAKS (UK fiktīvs pielāgots), kura ir balstīta uz formāta BAKS (UK fiktīvs) 1. versiju, kas ir balstīta uz datu modeļa Maksājumi (vienkāršots modelis) 1. versiju.</span><span class="sxs-lookup"><span data-stu-id="07ee9-180">This means it is version 1 of the custom BACS (UK fictitious custom) format, which is based on version 1 of the BACS (UK fictitious) format, which is based on version 1 of the Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-to-generate-payment-files"></a><span data-ttu-id="07ee9-181">Pārbaudiet pielāgoto formātu, lai ģenerētu maksājuma failus</span><span class="sxs-lookup"><span data-stu-id="07ee9-181">Test the customized format to generate payment files</span></span>
<span data-ttu-id="07ee9-182">Paralēlā Finance and Operations sesijā izpildiet procedūrā "Lietot izveidoto formātu, lai ģenerētu elektroniskos dokumentus maksājumiem" norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="07ee9-182">Complete the steps in the "Use created format to generate electronic documents for payments" procedure in a parallel Finance and Operations session.</span></span> <span data-ttu-id="07ee9-183">Atlasiet BAKS (UK fiktīvs pielāgots) formātu elektronisko maksājumu metodes parametros.</span><span class="sxs-lookup"><span data-stu-id="07ee9-183">Select the BACS (UK fictitious custom) format in electronic payment method parameters.</span></span> <span data-ttu-id="07ee9-184">Pārliecinieties, ka izveidotais maksājuma fails satur nesen ieviesto XML mezglu ar IBAN kodu, saskaņā ar reģionālajām prasībām.</span><span class="sxs-lookup"><span data-stu-id="07ee9-184">Make sure that the created payment file contains the recently introduced XML node presenting IBAN code in accordance to regional requirements.</span></span>  

## <a name="update-the-existing-country-specific-configuration"></a><span data-ttu-id="07ee9-185">Atjauniniet esošo valstij specifisko konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="07ee9-185">Update the existing country-specific configuration</span></span>
<span data-ttu-id="07ee9-186">Uzņēmumam Litware, Inc. jāveic BACS (UK fiktīvs) konfigurācijas jaunināšana un jāievieš jaunās valstij raksturīgās prasības attiecībā uz elektroniskā dokumenta formāta pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="07ee9-186">Litware, Inc. needs to update the BACS (UK fictitious) configuration and adopt new country requirements for managing the format of the electronic document.</span></span> <span data-ttu-id="07ee9-187">Vēlāk, tas tiks ietverts jaunā šīs konfigurācijas versijā, kas tiks piedāvāta pakalpojuma abonentiem, ieskaitot Proseware, Inc.</span><span class="sxs-lookup"><span data-stu-id="07ee9-187">Later, this will be enclosed in a new version of this configuration that will be offered for service subscribers, including Proseware, Inc.</span></span>  

<span data-ttu-id="07ee9-188">Ar reālo pakalpojumu sniegšanu saistītajos procesos katra jauna BACS (UK fiktīvs) versija var tikt importēta uzņēmumā Proseware, Inc. no Litware, Inc. konfigurāciju LCS repozitorija.</span><span class="sxs-lookup"><span data-stu-id="07ee9-188">In real service provision related processes, each new version of BACS (UK fictitious) can be imported by Proseware, Inc. from Litware, Inc. configurations' LCS repository.</span></span> <span data-ttu-id="07ee9-189">Šajā procedūrā mēs simulēsim to, atjauninot BAKS (UK fiktīvs) pakalpojuma sniedzēja vārdā.</span><span class="sxs-lookup"><span data-stu-id="07ee9-189">In this procedure we will simulate this by updating BACS (UK fictitious) on behalf of a service provider.</span></span>  

1. <span data-ttu-id="07ee9-190">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="07ee9-190">Close the page.</span></span>
2. <span data-ttu-id="07ee9-191">Atlasiet pakalpojumu sniedzēju Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="07ee9-191">Select Litware, inc. provider.</span></span>
3. <span data-ttu-id="07ee9-192">Noklikšķiniet uz Iestatīt aktīvu.</span><span class="sxs-lookup"><span data-stu-id="07ee9-192">Click Set active.</span></span>
4. <span data-ttu-id="07ee9-193">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="07ee9-193">Click Reporting configurations.</span></span>
5. <span data-ttu-id="07ee9-194">Kokā izvērsiet “Maksājumi (vienkāršotais modelis)”.</span><span class="sxs-lookup"><span data-stu-id="07ee9-194">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="07ee9-195">Kokā atlasiet 'Maksājumi (vienkāršotais modelis)\BAKS (UK fiktīvs)'.</span><span class="sxs-lookup"><span data-stu-id="07ee9-195">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="07ee9-196">Melnraksta versija BACS (UK fiktīvs), kas pieder Litware, Inc., tiek atlasīta, lai veiktu izmaiņas atbilstoši jaunajām valstij raksturīgajām prasībām.</span><span class="sxs-lookup"><span data-stu-id="07ee9-196">The draft version owned by Litware, Inc. provider BACS (UK fictitious) is selected to bring in changes to support new country-specific requirements.</span></span>  

## <a name="localize-the-base-format-of-the-electronic-document"></a><span data-ttu-id="07ee9-197">Lokalizējiet elektroniskā dokumenta pamatformātu</span><span class="sxs-lookup"><span data-stu-id="07ee9-197">Localize the base format of the electronic document</span></span>
<span data-ttu-id="07ee9-198">Pieņemsim, ka pastāv jaunas valstij raksturīgās prasības, kuru atbalsts jānodrošina uzņēmumam Litware:</span><span class="sxs-lookup"><span data-stu-id="07ee9-198">Assume that there are new country-specific requirements to be supported by Litware, Inc.:</span></span>  

- <span data-ttu-id="07ee9-199">Vērtība, kas paredzēta kreditora bankas SWIFT kodam katrā maksājuma transakcijā.</span><span class="sxs-lookup"><span data-stu-id="07ee9-199">A value for the creditor's bank SWIFT code in each payment transaction.</span></span>
- <span data-ttu-id="07ee9-200">Ģenerēšanas failā pastāv 100 rakstzīmju ierobežojums kreditora nosaukuma teksta garumam.</span><span class="sxs-lookup"><span data-stu-id="07ee9-200">A limit of 100 characters for the length of text for the vendor's name in a generating file.</span></span>  
- <span data-ttu-id="07ee9-201">Jaunas valstij specifiskas prasības</span><span class="sxs-lookup"><span data-stu-id="07ee9-201">New country-specific requirements</span></span>  
- <span data-ttu-id="07ee9-202">Atlasiet vēlamās konfigurācijas melnraksta versiju, lai ieviestu nepieciešamās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="07ee9-202">Select the draft version of the desired configuration to introduce required changes.</span></span>  


1. <span data-ttu-id="07ee9-203">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="07ee9-203">Click Designer.</span></span>
2. <span data-ttu-id="07ee9-204">Noklikšķiniet uz Izvērst/sakļaut.</span><span class="sxs-lookup"><span data-stu-id="07ee9-204">Click Expand/collapse.</span></span>
3. <span data-ttu-id="07ee9-205">Noklikšķiniet uz Izvērst/sakļaut.</span><span class="sxs-lookup"><span data-stu-id="07ee9-205">Click Expand/collapse.</span></span>
4. <span data-ttu-id="07ee9-206">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka”.</span><span class="sxs-lookup"><span data-stu-id="07ee9-206">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="07ee9-207">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="07ee9-207">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="07ee9-208">Kokā atlasiet "XML\Elements".</span><span class="sxs-lookup"><span data-stu-id="07ee9-208">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="07ee9-209">Laukā Nosaukums ierakstiet "SWIFT".</span><span class="sxs-lookup"><span data-stu-id="07ee9-209">In the Name field, type 'SWIFT'.</span></span>
8. <span data-ttu-id="07ee9-210">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="07ee9-210">Click OK.</span></span>
9. <span data-ttu-id="07ee9-211">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka\SWIFT”.</span><span class="sxs-lookup"><span data-stu-id="07ee9-211">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\SWIFT'.</span></span>
10. <span data-ttu-id="07ee9-212">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="07ee9-212">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="07ee9-213">Kokā atlasiet elementu “Teksts\Virkne”.</span><span class="sxs-lookup"><span data-stu-id="07ee9-213">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="07ee9-214">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="07ee9-214">Click OK.</span></span>
13. <span data-ttu-id="07ee9-215">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Nosaukums\Virkne”.</span><span class="sxs-lookup"><span data-stu-id="07ee9-215">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="07ee9-216">Ievadiet '100' laukā Maksimālais garums.</span><span class="sxs-lookup"><span data-stu-id="07ee9-216">In the Maximum length field, enter '100'.</span></span>
15. <span data-ttu-id="07ee9-217">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="07ee9-217">Click the Mapping tab.</span></span>
16. <span data-ttu-id="07ee9-218">Koka struktūrā izvērsiet elementu “modelis”.</span><span class="sxs-lookup"><span data-stu-id="07ee9-218">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="07ee9-219">Kokā izvērsiet sadaļu “modelis\Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="07ee9-219">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="07ee9-220">Kokā izvērsiet sadaļu “modelis\Maksājumi\Kreditors”.</span><span class="sxs-lookup"><span data-stu-id="07ee9-220">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="07ee9-221">Kokā izvērsiet elementu “modelis\Maksājumi\Kreditors\Aģents“.</span><span class="sxs-lookup"><span data-stu-id="07ee9-221">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
20. <span data-ttu-id="07ee9-222">Koka struktūrā atlasiet zaru “modelis\Maksājumi\Kreditors\Aģents\SWIFT”.</span><span class="sxs-lookup"><span data-stu-id="07ee9-222">In the tree, select 'model\Payments\Creditor\Agent\SWIFT'.</span></span>
21. <span data-ttu-id="07ee9-223">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums = model.Payments\Kreditors\Banka\SWIFT\Virkne”.</span><span class="sxs-lookup"><span data-stu-id="07ee9-223">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\SWIFT\String'.</span></span>
22. <span data-ttu-id="07ee9-224">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="07ee9-224">Click Bind.</span></span>
23. <span data-ttu-id="07ee9-225">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="07ee9-225">Click Save.</span></span>

## <a name="validate-the-localized-format"></a><span data-ttu-id="07ee9-226">Validēt lokalizēto formātu</span><span class="sxs-lookup"><span data-stu-id="07ee9-226">Validate the localized format</span></span>
1. <span data-ttu-id="07ee9-227">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="07ee9-227">Click Validate.</span></span>
2. <span data-ttu-id="07ee9-228">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="07ee9-228">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a><span data-ttu-id="07ee9-229">Pamatformāta konfigurācijas pašreizējās versijas statusa maiņa</span><span class="sxs-lookup"><span data-stu-id="07ee9-229">Change the status of the current version of the base format configuration</span></span>
<span data-ttu-id="07ee9-230">Nomainiet atjauninātā pamatformāta konfigurācijas statusu no Melnraksts uz Pabeigts, lai to padarītu pieejamu maksājumu dokumentu ģenerēšanai, un formāts konfigurācijas atjauninājumiem, kas izriet no tās.</span><span class="sxs-lookup"><span data-stu-id="07ee9-230">Change the status of the updated base format configuration from Draft to Completed to make it available for generation of payment documents and updates of format configurations derived from it.</span></span>  

1. <span data-ttu-id="07ee9-231">Noklikšķiniet uz Mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="07ee9-231">Click Change status.</span></span>

    <span data-ttu-id="07ee9-232">Ņemiet vērā, ka atlasītās konfigurācijas pašreizējai versijai ir statuss Melnraksts.</span><span class="sxs-lookup"><span data-stu-id="07ee9-232">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="07ee9-233">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="07ee9-233">Click Complete.</span></span>
3. <span data-ttu-id="07ee9-234">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="07ee9-234">In the Description field, type a value.</span></span>
4. <span data-ttu-id="07ee9-235">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="07ee9-235">Click OK.</span></span>
5. <span data-ttu-id="07ee9-236">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="07ee9-236">In the list, find and select the desired record.</span></span>

## <a name="change-the-base-version-for-the-custom-format-configuration"></a><span data-ttu-id="07ee9-237">Mainiet bāzes versiju pielāgota formāta konfigurācijai</span><span class="sxs-lookup"><span data-stu-id="07ee9-237">Change the base version for the custom format configuration</span></span>

<span data-ttu-id="07ee9-238">Proseware, Inc. tiek informēts, ka ir pieejama jauna BACS (UK fiktīvs) konfigurācijas versija 1.2 elektronisko maksājumu dokumentu ģenerēšanai saskaņā ar nesen izziņotajām valstij raksturīgajām prasībām.</span><span class="sxs-lookup"><span data-stu-id="07ee9-238">Proseware, Inc. is informed that a new version 1.2 of BACS (UK fictitious) configuration is available to generate electronic payment documents in accordance to recently announced country-specific requirements.</span></span> <span data-ttu-id="07ee9-239">Proseware, Inc. vēlas sākt to izmantot kā standartu valstij.</span><span class="sxs-lookup"><span data-stu-id="07ee9-239">Proseware, Inc. wants to start using it as a standard for the country.</span></span>  

<span data-ttu-id="07ee9-240">Lai to izdarītu, uzņēmumam Proseware, Inc. ir jāmaina pielāgotās konfigurācijas BACS (UK fiktīvs, pielāgots) bāzes konfigurācijas versiju.</span><span class="sxs-lookup"><span data-stu-id="07ee9-240">To do this, Proseware, Inc. needs to change the base configuration version for the custom configuration BACS (UK fictitious custom).</span></span> <span data-ttu-id="07ee9-241">1.1 BAKS (UK fiktīvs) versijas vietā, izmantojiet jauno 1.2 versiju.</span><span class="sxs-lookup"><span data-stu-id="07ee9-241">Instead of version 1.1 of BACS (UK fictitious) use new version 1.2.</span></span>  

1. <span data-ttu-id="07ee9-242">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="07ee9-242">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="07ee9-243">Atlasiet nodrošinātāju Proseware, Inc., lai iestatītu to kā aktīvu.</span><span class="sxs-lookup"><span data-stu-id="07ee9-243">Select the Proseware, Inc. provider to mark it as active.</span></span>
3. <span data-ttu-id="07ee9-244">Noklikšķiniet uz Iestatīt aktīvu.</span><span class="sxs-lookup"><span data-stu-id="07ee9-244">Click Set active.</span></span>
4. <span data-ttu-id="07ee9-245">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="07ee9-245">Click Reporting configurations.</span></span>
5. <span data-ttu-id="07ee9-246">Kokā izvērsiet “Maksājumi (vienkāršotais modelis)”.</span><span class="sxs-lookup"><span data-stu-id="07ee9-246">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="07ee9-247">Kokā izvērsiet 'Maksājumi (vienkāršotais modelis)\BAKS (UK fiktīvs)'.</span><span class="sxs-lookup"><span data-stu-id="07ee9-247">In the tree, expand 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
7. <span data-ttu-id="07ee9-248">Kokā atlasiet 'Maksājumi (vienkāršotais modelis)\BAKS (UK fiktīvs)\BAKS (UK fiktīvs pielāgots)'.</span><span class="sxs-lookup"><span data-stu-id="07ee9-248">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)\BACS (UK fictitious custom)'.</span></span>

    <span data-ttu-id="07ee9-249">Atlasiet BACS (UK fiktīvs pielāgots) konfigurāciju, kas pieder Proseware, Inc.</span><span class="sxs-lookup"><span data-stu-id="07ee9-249">Select the BACS (UK fictitious custom) configuration, which is owned by Proseware, Inc.</span></span>  

    <span data-ttu-id="07ee9-250">Izmantojiet atlasītās konfigurācijas melnraksta versiju, lai ieviestu nepieciešamās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="07ee9-250">Use the draft version of the selected configuration to introduce required changes.</span></span>  

8. <span data-ttu-id="07ee9-251">Noklikšķiniet uz Pārskatīt.</span><span class="sxs-lookup"><span data-stu-id="07ee9-251">Click Rebase.</span></span>

    <span data-ttu-id="07ee9-252">Atlasiet pamata konfigurācijas jauno 1.2 versiju, lai to lietotu kā jaunu bāzi konfigurācijas atjaunināšanai.</span><span class="sxs-lookup"><span data-stu-id="07ee9-252">Select the new version 1.2 of the base configuration to be applied as a new base for updating the configuration.</span></span>  

9. <span data-ttu-id="07ee9-253">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="07ee9-253">Click OK.</span></span>

    <span data-ttu-id="07ee9-254">Ņemiet vērā, ka tika atklāti daži konflikti starp pielāgotas versijas un jaunas bāzes versijas sapludināšanu, kas nozīmē formāta izmaiņas, kuras nevar sapludināt automātiski.</span><span class="sxs-lookup"><span data-stu-id="07ee9-254">Note that some conflicts have been discovered between merging the custom version and a new base version representing some format changes that can't be merged automatically.</span></span>  

## <a name="resolve-rebase-conflicts"></a><span data-ttu-id="07ee9-255">Atrisiniet pārskatījuma konfliktus</span><span class="sxs-lookup"><span data-stu-id="07ee9-255">Resolve rebase conflicts</span></span>
1. <span data-ttu-id="07ee9-256">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="07ee9-256">Click Designer.</span></span>
    
    <span data-ttu-id="07ee9-257">Ņemiet vērā, ka izmaiņas kreditora nosaukuma teksta garuma ierobežojumā nevar tik atrisinātas automātiski.</span><span class="sxs-lookup"><span data-stu-id="07ee9-257">Note that changes to the vendor's name text length limit couldn't be resolved automatically.</span></span> <span data-ttu-id="07ee9-258">Tāpēc tas ir norādīts konfliktu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="07ee9-258">Therefore, this is presented in a conflicts list.</span></span> <span data-ttu-id="07ee9-259">Katram konfliktam ar tipu Atjauninājums ir pieejamas šādas opcijas: - Lietot iepriekšējo bāzes vērtību (poga virs režģa), lai izmantotu iepriekšējo pamata versijas vērtību (mūsu gadījumā: 0).</span><span class="sxs-lookup"><span data-stu-id="07ee9-259">For each conflict of type Update, the following options are available:  - Apply a prior base value (button on top of the grid) to bring in the previous base version value (0 in our case).</span></span>  <span data-ttu-id="07ee9-260">- Piemērot bāzes vērtību (poga virs režģa), lai izmantotu jaunu pamata versijas vērtību (100 mūsu gadījumā).</span><span class="sxs-lookup"><span data-stu-id="07ee9-260">- Apply a base value (button on top of the grid) to bring in the new base version value (100 in our case).</span></span>  <span data-ttu-id="07ee9-261">- Paturiet savu (pielāgotu) vērtību (mūsu gadījumā tā ir 60).</span><span class="sxs-lookup"><span data-stu-id="07ee9-261">- Keep your own (custom) value (60 in our case).</span></span>  <span data-ttu-id="07ee9-262">Noklikšķiniet uz Lietot bāzes vērtību, lai pielietotu valstij raksturīgo 100 rakstzīmju limitu kreditora nosaukuma teksta garumam.</span><span class="sxs-lookup"><span data-stu-id="07ee9-262">Click Apply base value to apply a country-specific limit of 100 characters for vendor's name text length.</span></span>  

    <span data-ttu-id="07ee9-263">Ņemiet vēra, ka uzņēmumā Proseware, Inc. and Litware, Inc. tiek izmantotas pielāgotas un lokālas šī formāta versijas, izmantojot IBAN un SWIFT kodus ar saistītiem komponentiem, kas automātiski tiek apvienoti pārvaldības formātā.</span><span class="sxs-lookup"><span data-stu-id="07ee9-263">Note that Proseware, Inc. and Litware, Inc. have custom and local versions of this format using IBAN and SWIFT codes with related components that are automatically merged in the managing format.</span></span>  

2. <span data-ttu-id="07ee9-264">Noklikšķiniet uz Pievienot bāzes vērtību.</span><span class="sxs-lookup"><span data-stu-id="07ee9-264">Click Apply base value.</span></span>

    <span data-ttu-id="07ee9-265">Noklikšķiniet uz Lietot bāzes vērtību, lai pielietotu valstij raksturīgo 100 rakstzīmju limitu kreditora nosaukumiem.</span><span class="sxs-lookup"><span data-stu-id="07ee9-265">Click Apply base value to apply the country-specific limit of 100 characters for vendor names.</span></span>  

3. <span data-ttu-id="07ee9-266">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="07ee9-266">Click Save.</span></span>

    <span data-ttu-id="07ee9-267">Saglabājot formātu, no konfliktu saraksta tiks noņemti atrisinātie konflikti.</span><span class="sxs-lookup"><span data-stu-id="07ee9-267">Saving the format will remove resolved conflicts from the conflicts list.</span></span>  

4. <span data-ttu-id="07ee9-268">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="07ee9-268">Close the page.</span></span>

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a><span data-ttu-id="07ee9-269">Pielāgotā formāta konfigurācijas pašreizējās versijas statusa maiņa</span><span class="sxs-lookup"><span data-stu-id="07ee9-269">Change the status of the new version of the custom format configuration</span></span>
1. <span data-ttu-id="07ee9-270">Noklikšķiniet uz Mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="07ee9-270">Click Change status.</span></span>

    <span data-ttu-id="07ee9-271">Mainiet atjaunināta, pielāgota formāta konfigurācijas statusu no Melnraksts uz Pabeigts.</span><span class="sxs-lookup"><span data-stu-id="07ee9-271">Change the status of the updated, custom format configuration from Draft to Completed.</span></span> <span data-ttu-id="07ee9-272">Tas šo formāta konfigurāciju padara pieejamu maksājumu dokumentu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="07ee9-272">This will make the format configuration available for generating payment documents.</span></span> <span data-ttu-id="07ee9-273">Ņemiet vērā, ka atlasītās konfigurācijas pašreizējai versijai ir statuss Melnraksts.</span><span class="sxs-lookup"><span data-stu-id="07ee9-273">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="07ee9-274">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="07ee9-274">Click Complete.</span></span>
3. <span data-ttu-id="07ee9-275">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="07ee9-275">In the Description field, type a value.</span></span>
4. <span data-ttu-id="07ee9-276">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="07ee9-276">Click OK.</span></span>

    <span data-ttu-id="07ee9-277">Ņemiet vērā, ka izveidotās konfigurācija ir saglabāta kā pabeigta versija 1.2.2: bāzes BAKS (UK fiktīvs pielāgots) formāta versija 2, kas balstās uz bāzes BAKS (UK fiktīvs) formāta 2 versiju, kas balstās uz maksājumu (vienkāršots modelis) datu modeļa versiju 1.</span><span class="sxs-lookup"><span data-stu-id="07ee9-277">Note that the created configuration is saved as completed version 1.2.2: version 2 of base BACS (UK fictitious custom) format, which is based on version 2 of base BACS (UK fictitious) format, which is based on version 1 of Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-for-payment-files-generation"></a><span data-ttu-id="07ee9-278">Pārbaudiet pielāgoto formātu, lai ģenerētu maksājuma failus</span><span class="sxs-lookup"><span data-stu-id="07ee9-278">Test the customized format for payment files generation</span></span>
<span data-ttu-id="07ee9-279">Paralēlā Finance and Operations sesijā izpildiet procedūrā "Lietot izveidoto formātu, lai ģenerētu elektroniskos dokumentus maksājumiem" norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="07ee9-279">Complete the steps in the "Use created format to generate electronic documents for payments" procedure in parallel Finance and Operations session.</span></span> <span data-ttu-id="07ee9-280">Atlasiet izveidoto 'BAKS (UK fiktīvs pielāgots)' formātu elektronisko maksājumu metodes parametros.</span><span class="sxs-lookup"><span data-stu-id="07ee9-280">Select the created 'BACS (UK fictitious custom)' format in electronic payment method parameters.</span></span> <span data-ttu-id="07ee9-281">Pārliecinieties, vai izveidotais maksājuma fails satur Proseware, Inc. nesen ieviesto XML mezglu ar IBAN konta kodu, saskaņā ar reģionālajām prasībām.</span><span class="sxs-lookup"><span data-stu-id="07ee9-281">Make sure that the created payment file contains recently introduced by Proseware, Inc. XML node presenting IBAN account code in accordance to regional requirements.</span></span> <span data-ttu-id="07ee9-282">Failam arī jāsatur Litware, Inc. nesen ieviestais XML mezgls SWIFT bankas koda uzrādīšanai saskaņā ar valsts prasībām.</span><span class="sxs-lookup"><span data-stu-id="07ee9-282">The file also should contain the recently introduced by Litware, Inc. XML node presenting SWIFT bank code in accordance to country requirements.</span></span>  

