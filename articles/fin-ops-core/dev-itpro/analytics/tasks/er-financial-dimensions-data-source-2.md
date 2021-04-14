---
title: ER finanšu dimensijas, kuras izmanto kā datu avotu (2. daļa. Modeļa kartēšana)
description: Šajā tēmā ir aprakstīts, kā konfigurēt elektronisko pārskatu (ER) modeli, lai finanšu dimensijas izmantotu kā datu avotu ER pārskatiem. (2. daļa)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e6f5ffbebdfcd9f945e6237904d80e8734b0220
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752440"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a><span data-ttu-id="85d5e-104">ER finanšu dimensijas, kuras izmanto kā datu avotu (2. daļa. Modeļa kartēšana)</span><span class="sxs-lookup"><span data-stu-id="85d5e-104">ER Use financial dimensions as a data source (Part 2 - Model mapping)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="85d5e-105">Tālāk ir paskaidrots kā lietotājs, kam piešķirta loma sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="85d5e-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="85d5e-106">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="85d5e-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="85d5e-107">Lai izpildītu šos soļus, vispirms ir jāpabeidz soļi, kas aprakstīti procedūrā "ER Finanšu dimensijas, ko izmanto kā datu avotu (1. daļa: datu modeļa izveide)".</span><span class="sxs-lookup"><span data-stu-id="85d5e-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 1: Design data model" procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="85d5e-108">Pievienot nepieciešamos datu avotus modeļa kartēšanai</span><span class="sxs-lookup"><span data-stu-id="85d5e-108">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="85d5e-109">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="85d5e-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="85d5e-110">Koka struktūrā atlasiet 'Finanšu dimensiju parauga modelis'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="85d5e-111">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="85d5e-111">Click Designer.</span></span>
4. <span data-ttu-id="85d5e-112">Noklikšķiniet uz Kartēšanas modelis datu avotam.</span><span class="sxs-lookup"><span data-stu-id="85d5e-112">Click Map model to datasource.</span></span>
5. <span data-ttu-id="85d5e-113">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="85d5e-113">Click New.</span></span>
6. <span data-ttu-id="85d5e-114">Laukā Definīcija, atlasiet Ieraksts.</span><span class="sxs-lookup"><span data-stu-id="85d5e-114">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="85d5e-115">Laukā Nosaukums ierakstiet 'Dimensiju datu kartēšana'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-115">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="85d5e-116">Laukā Apraksts ierakstiet 'Dimensiju datu kartēšana'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-116">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="85d5e-117">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="85d5e-117">Click Save.</span></span>
10. <span data-ttu-id="85d5e-118">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="85d5e-118">Click Designer.</span></span>
11. <span data-ttu-id="85d5e-119">Kokā atlasiet 'Dynamics 365 for Operations\Tabula'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-119">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="85d5e-120">Noklikšķiniet uz Pievienot sakni.</span><span class="sxs-lookup"><span data-stu-id="85d5e-120">Click Add root.</span></span>
13. <span data-ttu-id="85d5e-121">Laukā Nosaukums ierakstiet "Uzņēmums".</span><span class="sxs-lookup"><span data-stu-id="85d5e-121">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="85d5e-122">Laukā Tabula ierakstiet "CompanyInfo".</span><span class="sxs-lookup"><span data-stu-id="85d5e-122">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="85d5e-123">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="85d5e-123">Click OK.</span></span>
16. <span data-ttu-id="85d5e-124">Koka struktūrā atlasiet 'Funkcijas\Detalizēta informācija par finanšu dimensijām'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-124">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="85d5e-125">Noklikšķiniet uz Pievienot sakni.</span><span class="sxs-lookup"><span data-stu-id="85d5e-125">Click Add root.</span></span>
    * <span data-ttu-id="85d5e-126">Šis datu avots norāda finanšu dimensiju sfēru, kas tiks definēta jebkuram pārskatam, kas tiks izmantots šajā modelī kā datu avots.</span><span class="sxs-lookup"><span data-stu-id="85d5e-126">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="85d5e-127">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="85d5e-127">In the Name field, type a value.</span></span>
19. <span data-ttu-id="85d5e-128">Atlasiet Jā laukā Jautāt dimensijas.</span><span class="sxs-lookup"><span data-stu-id="85d5e-128">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="85d5e-129">Atlasiet Jā, lai lietotājs varētu atlasīt dimensijas Lietotāja dialoglodziņā izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="85d5e-129">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="85d5e-130">Ja iestatīts uz Nē, visas pašreizējās instances finanšu dimensijas tiks izmantotas pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="85d5e-130">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="85d5e-131">Finanšu dimensiju atlases laukā atlasiet 'Juridiska persona'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-131">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="85d5e-132">Atlasiet Visu, lai lietotājs varētu atlasīt vēlamo dimensiju pašreizējai instancei laukā Uzmeklēšana.</span><span class="sxs-lookup"><span data-stu-id="85d5e-132">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="85d5e-133">Atlasiet juridisko personu, lai lietotājs varētu atlasīt dimensijas uzņēmumam laukā Uzmeklēšana.</span><span class="sxs-lookup"><span data-stu-id="85d5e-133">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="85d5e-134">Atlasīt Dimensiju, lai lietotājs varētu atlasīt dimensijas, izmantojot vienu dimensiju kopu.</span><span class="sxs-lookup"><span data-stu-id="85d5e-134">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="85d5e-135">Atlasiet Jā laukā Jautāt galveno kontu.</span><span class="sxs-lookup"><span data-stu-id="85d5e-135">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="85d5e-136">Iestatiet 'Jautāt galveno kontu' uz Jā, lai atļautu lietotājiem atlasīt galveno kontu kā daļu no dimensiju saraksta.</span><span class="sxs-lookup"><span data-stu-id="85d5e-136">Set 'Ask for main account' to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="85d5e-137">Ja ir iestatīts uz Nē, galvenais konts netiks iekļauts dimensiju sarakstā, un opcija 'Vai galvenais konts ir obligāts' ir iespējota.</span><span class="sxs-lookup"><span data-stu-id="85d5e-137">If set to No, the main account will not be included to the list of dimensions and the 'Is main account mandatory' option is enabled.</span></span> <span data-ttu-id="85d5e-138">Ja opcija 'Vai galvenais konts ir obligāts' ir iestatīta uz Jā, iekļaujiet galveno kontu dimensiju sarakstā, neatkarīgi no lietotāja veiktās atlases.</span><span class="sxs-lookup"><span data-stu-id="85d5e-138">If "Is main account mandatory' is set to Yes, include the main account in the list of dimensions regardless of the user's selection.</span></span>  
22. <span data-ttu-id="85d5e-139">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="85d5e-139">Click OK.</span></span>
<span data-ttu-id="85d5e-140">![ER modeļa kartēšanas noformētāja lapa](../media/er-financial-dimensions-guides-model-mapping1.png)</span><span class="sxs-lookup"><span data-stu-id="85d5e-140">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping1.png)</span></span>
23. <span data-ttu-id="85d5e-141">Kokā atlasiet 'Dynamics 365 for Operations\Tabulas ieraksti'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-141">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="85d5e-142">Noklikšķiniet uz Pievienot sakni.</span><span class="sxs-lookup"><span data-stu-id="85d5e-142">Click Add root.</span></span>
25. <span data-ttu-id="85d5e-143">Laukā Nosaukums ierakstiet 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-143">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="85d5e-144">Laukā Pieprasīt vaicājumu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="85d5e-144">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="85d5e-145">Laukā Tabula ievadiet 'LedgerJournalTable'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-145">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="85d5e-146">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="85d5e-146">Click OK.</span></span>
<span data-ttu-id="85d5e-147">![ER modeļa kartēšanas noformētāja lapa](../media/er-financial-dimensions-guides-model-mapping2.png)</span><span class="sxs-lookup"><span data-stu-id="85d5e-147">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping2.png)</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="85d5e-148">Kartēt datu modeļa elementus pievienotajiem datu avotiem</span><span class="sxs-lookup"><span data-stu-id="85d5e-148">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="85d5e-149">Kokā izvērsiet 'Žurnāls'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-149">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="85d5e-150">Kokā izvērsiet 'Žurnāls\Darbība'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-150">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="85d5e-151">Kokā izvērsiet 'Žurnāls\Darbība\Dimensiju dati'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-151">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="85d5e-152">Kokā izvērsiet 'Dimensiju iestatījums'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-152">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="85d5e-153">Kokā izvērsiet 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-153">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="85d5e-154">Kokā izvērsiet "LedgerJournal\<Relations".</span><span class="sxs-lookup"><span data-stu-id="85d5e-154">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="85d5e-155">Kokā izvērsiet "LedgerJournal\<Relations\LedgerJournalTrans".</span><span class="sxs-lookup"><span data-stu-id="85d5e-155">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="85d5e-156">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Voucher".</span><span class="sxs-lookup"><span data-stu-id="85d5e-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="85d5e-157">Kokā atlasiet 'Žurnāls\Darbība\Dokuments'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-157">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="85d5e-158">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="85d5e-158">Click Bind.</span></span>
11. <span data-ttu-id="85d5e-159">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)".</span><span class="sxs-lookup"><span data-stu-id="85d5e-159">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="85d5e-160">Ņemiet vērā, ka visām iestatītajām atsaucēm uz finanšu dimensijām, piemēram, LedgerDimension, ir pieejams attiecīgais datu avota vienums (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="85d5e-160">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="85d5e-161">Šī datu avota vienums nodrošina finanšu dimensijas no dimensiju kopas kā ierakstu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="85d5e-161">This data source item offers the financial dimensions of that dimensions set as the record's list.</span></span>  
12. <span data-ttu-id="85d5e-162">Kokā izvērsiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)".</span><span class="sxs-lookup"><span data-stu-id="85d5e-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="85d5e-163">Kokā izvērsiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions".</span><span class="sxs-lookup"><span data-stu-id="85d5e-163">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="85d5e-164">Kokā izvērsiet "LedgerJournal\\<Relācijas\LedgerJournalTrans\Konts.Dimensija(LedgerDimension.Dimension)\Galvenais konts un dimensijas\Vērtība".</span><span class="sxs-lookup"><span data-stu-id="85d5e-164">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="85d5e-165">Kokā izvērsiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition".</span><span class="sxs-lookup"><span data-stu-id="85d5e-165">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="85d5e-166">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name".</span><span class="sxs-lookup"><span data-stu-id="85d5e-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="85d5e-167">Kokā atlasiet 'Žurnāls\Darbība\Dimensiju dati\Nosaukums'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-167">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="85d5e-168">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="85d5e-168">Click Bind.</span></span>
19. <span data-ttu-id="85d5e-169">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description".</span><span class="sxs-lookup"><span data-stu-id="85d5e-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="85d5e-170">Kokā atlasiet 'Žurnāls\Darbība\Dimensiju dati\Apraksts'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-170">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="85d5e-171">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="85d5e-171">Click Bind.</span></span>
22. <span data-ttu-id="85d5e-172">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code".</span><span class="sxs-lookup"><span data-stu-id="85d5e-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="85d5e-173">Kokā atlasiet 'Žurnāls\Darbība\Dimensiju dati\Kods'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-173">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="85d5e-174">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="85d5e-174">Click Bind.</span></span>
25. <span data-ttu-id="85d5e-175">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions".</span><span class="sxs-lookup"><span data-stu-id="85d5e-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="85d5e-176">Kokā atlasiet 'Žurnāls\Darbība\Dimensiju dati'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-176">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="85d5e-177">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="85d5e-177">Click Bind.</span></span>
<span data-ttu-id="85d5e-178">![ER modeļa kartēšanas noformētāja lapa](../media/er-financial-dimensions-guides-model-mapping3.png)</span><span class="sxs-lookup"><span data-stu-id="85d5e-178">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping3.png)</span></span>
28. <span data-ttu-id="85d5e-179">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)".</span><span class="sxs-lookup"><span data-stu-id="85d5e-179">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="85d5e-180">Kokā atlasiet 'Žurnāls\Darbība\Debets'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-180">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="85d5e-181">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="85d5e-181">Click Bind.</span></span>
31. <span data-ttu-id="85d5e-182">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)".</span><span class="sxs-lookup"><span data-stu-id="85d5e-182">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="85d5e-183">Kokā atlasiet 'Žurnāls\Darbība\Datums'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-183">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="85d5e-184">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="85d5e-184">Click Bind.</span></span>
34. <span data-ttu-id="85d5e-185">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)".</span><span class="sxs-lookup"><span data-stu-id="85d5e-185">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="85d5e-186">Kokā atlasiet 'Žurnāls\Darbība\Valūta'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-186">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="85d5e-187">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="85d5e-187">Click Bind.</span></span>
37. <span data-ttu-id="85d5e-188">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)".</span><span class="sxs-lookup"><span data-stu-id="85d5e-188">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="85d5e-189">Kokā atlasiet 'Žurnāls\Darbība\Kredīts'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-189">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="85d5e-190">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="85d5e-190">Click Bind.</span></span>
40. <span data-ttu-id="85d5e-191">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans".</span><span class="sxs-lookup"><span data-stu-id="85d5e-191">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="85d5e-192">Kokā atlasiet 'Žurnāls\Darbība'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-192">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="85d5e-193">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="85d5e-193">Click Bind.</span></span>
43. <span data-ttu-id="85d5e-194">Kokā atlasiet 'LedgerJournal\Žurnāla iedaļas numurs(JournalNum)'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-194">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="85d5e-195">Kokā atlasiet 'Žurnāls\Iedaļa'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-195">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="85d5e-196">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="85d5e-196">Click Bind.</span></span>
46. <span data-ttu-id="85d5e-197">Kokā atlasiet 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-197">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="85d5e-198">Kokā atlasiet 'Žurnāls'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-198">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="85d5e-199">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="85d5e-199">Click Bind.</span></span>
49. <span data-ttu-id="85d5e-200">Kokā izvērsiet 'Dimensijas'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-200">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="85d5e-201">Kokā izvērsiet 'Dimensijas\Galvenais konts un dimensijas'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-201">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="85d5e-202">Kokā izvērsiet 'Dimensijas\Galvenais konts un dimensijas\Definīcija'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-202">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="85d5e-203">Kokā atlasiet 'Dimensijas\Galvenais konts un dimensijas\Definīcija\Nosaukums'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-203">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="85d5e-204">Kokā izvērsiet 'Dimensiju iestatīšana\Kods'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-204">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="85d5e-205">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="85d5e-205">Click Bind.</span></span>
55. <span data-ttu-id="85d5e-206">Kokā atlasiet 'Dimensijas\Galvenais konts un dimensijas\Definīcija\Pārskata kolonnas nosaukums'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-206">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="85d5e-207">Kokā atlasiet 'Dimensiju iestatīšana\Nosaukums'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-207">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="85d5e-208">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="85d5e-208">Click Bind.</span></span>
58. <span data-ttu-id="85d5e-209">Kokā atlasiet 'Dimensijas\Galvenais konts un dimensijas'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-209">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="85d5e-210">Kokā atlasiet 'Dimensiju iestatīšana'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-210">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="85d5e-211">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="85d5e-211">Click Bind.</span></span>
61. <span data-ttu-id="85d5e-212">Kokā atlasiet 'Uzņēmums'.</span><span class="sxs-lookup"><span data-stu-id="85d5e-212">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="85d5e-213">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="85d5e-213">Click Edit.</span></span>
63. <span data-ttu-id="85d5e-214">Laukā expressionAsStringText field ievadiet 'Uzņēmums.'atrast()'.'nosaukums()''.</span><span class="sxs-lookup"><span data-stu-id="85d5e-214">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="85d5e-215">Uzņēmums.'atrast()'.'nosaukums()'</span><span class="sxs-lookup"><span data-stu-id="85d5e-215">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="85d5e-216">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="85d5e-216">Click Save.</span></span>
<span data-ttu-id="85d5e-217">![ER modeļa kartēšanas noformētāja lapa](../media/er-financial-dimensions-guides-model-mapping4.png)</span><span class="sxs-lookup"><span data-stu-id="85d5e-217">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping4.png)</span></span>
65. <span data-ttu-id="85d5e-218">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="85d5e-218">Close the page.</span></span>
66. <span data-ttu-id="85d5e-219">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="85d5e-219">Click Save.</span></span>
67. <span data-ttu-id="85d5e-220">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="85d5e-220">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="85d5e-221">Pabeigt šo modeļa melnraksta versiju</span><span class="sxs-lookup"><span data-stu-id="85d5e-221">Complete this draft model's version</span></span>
1. <span data-ttu-id="85d5e-222">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="85d5e-222">Close the page.</span></span>
2. <span data-ttu-id="85d5e-223">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="85d5e-223">Close the page.</span></span>
3. <span data-ttu-id="85d5e-224">Noklikšķiniet uz Mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="85d5e-224">Click Change status.</span></span>
4. <span data-ttu-id="85d5e-225">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="85d5e-225">Click Complete.</span></span>
5. <span data-ttu-id="85d5e-226">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="85d5e-226">Click OK.</span></span>
<span data-ttu-id="85d5e-227">![ER modeļa kartēšanas noformētāja lapa](../media/er-financial-dimensions-guides-model-mapping5.png)</span><span class="sxs-lookup"><span data-stu-id="85d5e-227">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping5.png)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]