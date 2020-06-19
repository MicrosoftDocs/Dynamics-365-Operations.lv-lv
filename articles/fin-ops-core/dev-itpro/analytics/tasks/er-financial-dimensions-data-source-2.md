---
title: ER finanšu dimensijas, kuras izmanto kā datu avotu (2. daļa. Modeļa kartēšana)
description: Tālāk ir paskaidrots kā lietotājs, kam piešķirta loma sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3aabd622d15917d7e4549d0b0679aa20231c5815
ms.sourcegitcommit: d9125c20b21459076e4fd92fd9ebfe2e53a0431b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/27/2020
ms.locfileid: "3406524"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a><span data-ttu-id="50289-103">ER finanšu dimensijas, kuras izmanto kā datu avotu (2. daļa. Modeļa kartēšana)</span><span class="sxs-lookup"><span data-stu-id="50289-103">ER Use financial dimensions as a data source (Part 2 - Model mapping)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="50289-104">Tālāk ir paskaidrots kā lietotājs, kam piešķirta loma sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="50289-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="50289-105">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="50289-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="50289-106">Lai izpildītu šos soļus, vispirms ir jāpabeidz soļi, kas aprakstīti procedūrā "ER Finanšu dimensijas, ko izmanto kā datu avotu (1. daļa: datu modeļa izveide)".</span><span class="sxs-lookup"><span data-stu-id="50289-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 1: Design data model" procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="50289-107">Pievienot nepieciešamos datu avotus modeļa kartēšanai</span><span class="sxs-lookup"><span data-stu-id="50289-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="50289-108">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="50289-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="50289-109">Koka struktūrā atlasiet 'Finanšu dimensiju parauga modelis'.</span><span class="sxs-lookup"><span data-stu-id="50289-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="50289-110">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="50289-110">Click Designer.</span></span>
4. <span data-ttu-id="50289-111">Noklikšķiniet uz Kartēšanas modelis datu avotam.</span><span class="sxs-lookup"><span data-stu-id="50289-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="50289-112">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="50289-112">Click New.</span></span>
6. <span data-ttu-id="50289-113">Laukā Definīcija, atlasiet Ieraksts.</span><span class="sxs-lookup"><span data-stu-id="50289-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="50289-114">Laukā Nosaukums ierakstiet 'Dimensiju datu kartēšana'.</span><span class="sxs-lookup"><span data-stu-id="50289-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="50289-115">Laukā Apraksts ierakstiet 'Dimensiju datu kartēšana'.</span><span class="sxs-lookup"><span data-stu-id="50289-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="50289-116">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="50289-116">Click Save.</span></span>
10. <span data-ttu-id="50289-117">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="50289-117">Click Designer.</span></span>
11. <span data-ttu-id="50289-118">Kokā atlasiet 'Dynamics 365 for Operations\Tabula'.</span><span class="sxs-lookup"><span data-stu-id="50289-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="50289-119">Noklikšķiniet uz Pievienot sakni.</span><span class="sxs-lookup"><span data-stu-id="50289-119">Click Add root.</span></span>
13. <span data-ttu-id="50289-120">Laukā Nosaukums ierakstiet "Uzņēmums".</span><span class="sxs-lookup"><span data-stu-id="50289-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="50289-121">Laukā Tabula ierakstiet "CompanyInfo".</span><span class="sxs-lookup"><span data-stu-id="50289-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="50289-122">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="50289-122">Click OK.</span></span>
16. <span data-ttu-id="50289-123">Koka struktūrā atlasiet 'Funkcijas\Detalizēta informācija par finanšu dimensijām'.</span><span class="sxs-lookup"><span data-stu-id="50289-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="50289-124">Noklikšķiniet uz Pievienot sakni.</span><span class="sxs-lookup"><span data-stu-id="50289-124">Click Add root.</span></span>
    * <span data-ttu-id="50289-125">Šis datu avots norāda finanšu dimensiju sfēru, kas tiks definēta jebkuram pārskatam, kas tiks izmantots šajā modelī kā datu avots.</span><span class="sxs-lookup"><span data-stu-id="50289-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="50289-126">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="50289-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="50289-127">Atlasiet Jā laukā Jautāt dimensijas.</span><span class="sxs-lookup"><span data-stu-id="50289-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="50289-128">Atlasiet Jā, lai lietotājs varētu atlasīt dimensijas Lietotāja dialoglodziņā izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="50289-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="50289-129">Ja iestatīts uz Nē, visas pašreizējās instances finanšu dimensijas tiks izmantotas pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="50289-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="50289-130">Finanšu dimensiju atlases laukā atlasiet 'Juridiska persona'.</span><span class="sxs-lookup"><span data-stu-id="50289-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="50289-131">Atlasiet Visu, lai lietotājs varētu atlasīt vēlamo dimensiju pašreizējai instancei laukā Uzmeklēšana.</span><span class="sxs-lookup"><span data-stu-id="50289-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="50289-132">Atlasiet juridisko personu, lai lietotājs varētu atlasīt dimensijas uzņēmumam laukā Uzmeklēšana.</span><span class="sxs-lookup"><span data-stu-id="50289-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="50289-133">Atlasīt Dimensiju, lai lietotājs varētu atlasīt dimensijas, izmantojot vienu dimensiju kopu.</span><span class="sxs-lookup"><span data-stu-id="50289-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="50289-134">Atlasiet Jā laukā Jautāt galveno kontu.</span><span class="sxs-lookup"><span data-stu-id="50289-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="50289-135">Iestatiet 'Jautāt galveno kontu' uz Jā, lai atļautu lietotājiem atlasīt galveno kontu kā daļu no dimensiju saraksta.</span><span class="sxs-lookup"><span data-stu-id="50289-135">Set 'Ask for main account' to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="50289-136">Ja ir iestatīts uz Nē, galvenais konts netiks iekļauts dimensiju sarakstā, un opcija 'Vai galvenais konts ir obligāts' ir iespējota.</span><span class="sxs-lookup"><span data-stu-id="50289-136">If set to No, the main account will not be included to the list of dimensions and the 'Is main account mandatory' option is enabled.</span></span> <span data-ttu-id="50289-137">Ja opcija 'Vai galvenais konts ir obligāts' ir iestatīta uz Jā, iekļaujiet galveno kontu dimensiju sarakstā, neatkarīgi no lietotāja veiktās atlases.</span><span class="sxs-lookup"><span data-stu-id="50289-137">If "Is main account mandatory' is set to Yes, include the main account in the list of dimensions regardless of the user's selection.</span></span>  
22. <span data-ttu-id="50289-138">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="50289-138">Click OK.</span></span>
<span data-ttu-id="50289-139">![ER modeļa kartēšanas noformētāja lapa](../media/er-financial-dimensions-guides-model-mapping1.png)</span><span class="sxs-lookup"><span data-stu-id="50289-139">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping1.png)</span></span>
23. <span data-ttu-id="50289-140">Kokā atlasiet 'Dynamics 365 for Operations\Tabulas ieraksti'.</span><span class="sxs-lookup"><span data-stu-id="50289-140">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="50289-141">Noklikšķiniet uz Pievienot sakni.</span><span class="sxs-lookup"><span data-stu-id="50289-141">Click Add root.</span></span>
25. <span data-ttu-id="50289-142">Laukā Nosaukums ierakstiet 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="50289-142">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="50289-143">Laukā Pieprasīt vaicājumu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="50289-143">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="50289-144">Laukā Tabula ievadiet 'LedgerJournalTable'.</span><span class="sxs-lookup"><span data-stu-id="50289-144">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="50289-145">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="50289-145">Click OK.</span></span>
<span data-ttu-id="50289-146">![ER modeļa kartēšanas noformētāja lapa](../media/er-financial-dimensions-guides-model-mapping2.png)</span><span class="sxs-lookup"><span data-stu-id="50289-146">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping2.png)</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="50289-147">Kartēt datu modeļa elementus pievienotajiem datu avotiem</span><span class="sxs-lookup"><span data-stu-id="50289-147">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="50289-148">Kokā izvērsiet 'Žurnāls'.</span><span class="sxs-lookup"><span data-stu-id="50289-148">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="50289-149">Kokā izvērsiet 'Žurnāls\Darbība'.</span><span class="sxs-lookup"><span data-stu-id="50289-149">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="50289-150">Kokā izvērsiet 'Žurnāls\Darbība\Dimensiju dati'.</span><span class="sxs-lookup"><span data-stu-id="50289-150">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="50289-151">Kokā izvērsiet 'Dimensiju iestatījums'.</span><span class="sxs-lookup"><span data-stu-id="50289-151">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="50289-152">Kokā izvērsiet 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="50289-152">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="50289-153">Kokā izvērsiet "LedgerJournal\<Relations".</span><span class="sxs-lookup"><span data-stu-id="50289-153">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="50289-154">Kokā izvērsiet "LedgerJournal\<Relations\LedgerJournalTrans".</span><span class="sxs-lookup"><span data-stu-id="50289-154">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="50289-155">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Voucher".</span><span class="sxs-lookup"><span data-stu-id="50289-155">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="50289-156">Kokā atlasiet 'Žurnāls\Darbība\Dokuments'.</span><span class="sxs-lookup"><span data-stu-id="50289-156">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="50289-157">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50289-157">Click Bind.</span></span>
11. <span data-ttu-id="50289-158">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)".</span><span class="sxs-lookup"><span data-stu-id="50289-158">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="50289-159">Ņemiet vērā, ka visām iestatītajām atsaucēm uz finanšu dimensijām, piemēram, LedgerDimension, ir pieejams attiecīgais datu avota vienums (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="50289-159">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="50289-160">Šī datu avota vienums nodrošina finanšu dimensijas no dimensiju kopas kā ierakstu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="50289-160">This data source item offers the financial dimensions of that dimensions set as the record's list.</span></span>  
12. <span data-ttu-id="50289-161">Kokā izvērsiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)".</span><span class="sxs-lookup"><span data-stu-id="50289-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="50289-162">Kokā izvērsiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions".</span><span class="sxs-lookup"><span data-stu-id="50289-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="50289-163">Kokā izvērsiet "LedgerJournal\\<Relācijas\LedgerJournalTrans\Konts.Dimensija(LedgerDimension.Dimension)\Galvenais konts un dimensijas\Vērtība".</span><span class="sxs-lookup"><span data-stu-id="50289-163">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="50289-164">Kokā izvērsiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition".</span><span class="sxs-lookup"><span data-stu-id="50289-164">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="50289-165">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name".</span><span class="sxs-lookup"><span data-stu-id="50289-165">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="50289-166">Kokā atlasiet 'Žurnāls\Darbība\Dimensiju dati\Nosaukums'.</span><span class="sxs-lookup"><span data-stu-id="50289-166">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="50289-167">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50289-167">Click Bind.</span></span>
19. <span data-ttu-id="50289-168">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description".</span><span class="sxs-lookup"><span data-stu-id="50289-168">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="50289-169">Kokā atlasiet 'Žurnāls\Darbība\Dimensiju dati\Apraksts'.</span><span class="sxs-lookup"><span data-stu-id="50289-169">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="50289-170">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50289-170">Click Bind.</span></span>
22. <span data-ttu-id="50289-171">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code".</span><span class="sxs-lookup"><span data-stu-id="50289-171">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="50289-172">Kokā atlasiet 'Žurnāls\Darbība\Dimensiju dati\Kods'.</span><span class="sxs-lookup"><span data-stu-id="50289-172">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="50289-173">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50289-173">Click Bind.</span></span>
25. <span data-ttu-id="50289-174">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions".</span><span class="sxs-lookup"><span data-stu-id="50289-174">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="50289-175">Kokā atlasiet 'Žurnāls\Darbība\Dimensiju dati'.</span><span class="sxs-lookup"><span data-stu-id="50289-175">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="50289-176">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50289-176">Click Bind.</span></span>
<span data-ttu-id="50289-177">![ER modeļa kartēšanas noformētāja lapa](../media/er-financial-dimensions-guides-model-mapping3.png)</span><span class="sxs-lookup"><span data-stu-id="50289-177">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping3.png)</span></span>
28. <span data-ttu-id="50289-178">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)".</span><span class="sxs-lookup"><span data-stu-id="50289-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="50289-179">Kokā atlasiet 'Žurnāls\Darbība\Debets'.</span><span class="sxs-lookup"><span data-stu-id="50289-179">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="50289-180">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50289-180">Click Bind.</span></span>
31. <span data-ttu-id="50289-181">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)".</span><span class="sxs-lookup"><span data-stu-id="50289-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="50289-182">Kokā atlasiet 'Žurnāls\Darbība\Datums'.</span><span class="sxs-lookup"><span data-stu-id="50289-182">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="50289-183">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50289-183">Click Bind.</span></span>
34. <span data-ttu-id="50289-184">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)".</span><span class="sxs-lookup"><span data-stu-id="50289-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="50289-185">Kokā atlasiet 'Žurnāls\Darbība\Valūta'.</span><span class="sxs-lookup"><span data-stu-id="50289-185">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="50289-186">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50289-186">Click Bind.</span></span>
37. <span data-ttu-id="50289-187">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)".</span><span class="sxs-lookup"><span data-stu-id="50289-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="50289-188">Kokā atlasiet 'Žurnāls\Darbība\Kredīts'.</span><span class="sxs-lookup"><span data-stu-id="50289-188">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="50289-189">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50289-189">Click Bind.</span></span>
40. <span data-ttu-id="50289-190">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans".</span><span class="sxs-lookup"><span data-stu-id="50289-190">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="50289-191">Kokā atlasiet 'Žurnāls\Darbība'.</span><span class="sxs-lookup"><span data-stu-id="50289-191">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="50289-192">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50289-192">Click Bind.</span></span>
43. <span data-ttu-id="50289-193">Kokā atlasiet 'LedgerJournal\Žurnāla iedaļas numurs(JournalNum)'.</span><span class="sxs-lookup"><span data-stu-id="50289-193">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="50289-194">Kokā atlasiet 'Žurnāls\Iedaļa'.</span><span class="sxs-lookup"><span data-stu-id="50289-194">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="50289-195">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50289-195">Click Bind.</span></span>
46. <span data-ttu-id="50289-196">Kokā atlasiet 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="50289-196">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="50289-197">Kokā atlasiet 'Žurnāls'.</span><span class="sxs-lookup"><span data-stu-id="50289-197">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="50289-198">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50289-198">Click Bind.</span></span>
49. <span data-ttu-id="50289-199">Kokā izvērsiet 'Dimensijas'.</span><span class="sxs-lookup"><span data-stu-id="50289-199">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="50289-200">Kokā izvērsiet 'Dimensijas\Galvenais konts un dimensijas'.</span><span class="sxs-lookup"><span data-stu-id="50289-200">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="50289-201">Kokā izvērsiet 'Dimensijas\Galvenais konts un dimensijas\Definīcija'.</span><span class="sxs-lookup"><span data-stu-id="50289-201">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="50289-202">Kokā atlasiet 'Dimensijas\Galvenais konts un dimensijas\Definīcija\Nosaukums'.</span><span class="sxs-lookup"><span data-stu-id="50289-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="50289-203">Kokā izvērsiet 'Dimensiju iestatīšana\Kods'.</span><span class="sxs-lookup"><span data-stu-id="50289-203">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="50289-204">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50289-204">Click Bind.</span></span>
55. <span data-ttu-id="50289-205">Kokā atlasiet 'Dimensijas\Galvenais konts un dimensijas\Definīcija\Pārskata kolonnas nosaukums'.</span><span class="sxs-lookup"><span data-stu-id="50289-205">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="50289-206">Kokā atlasiet 'Dimensiju iestatīšana\Nosaukums'.</span><span class="sxs-lookup"><span data-stu-id="50289-206">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="50289-207">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50289-207">Click Bind.</span></span>
58. <span data-ttu-id="50289-208">Kokā atlasiet 'Dimensijas\Galvenais konts un dimensijas'.</span><span class="sxs-lookup"><span data-stu-id="50289-208">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="50289-209">Kokā atlasiet 'Dimensiju iestatīšana'.</span><span class="sxs-lookup"><span data-stu-id="50289-209">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="50289-210">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50289-210">Click Bind.</span></span>
61. <span data-ttu-id="50289-211">Kokā atlasiet 'Uzņēmums'.</span><span class="sxs-lookup"><span data-stu-id="50289-211">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="50289-212">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="50289-212">Click Edit.</span></span>
63. <span data-ttu-id="50289-213">Laukā expressionAsStringText field ievadiet 'Uzņēmums.'atrast()'.'nosaukums()''.</span><span class="sxs-lookup"><span data-stu-id="50289-213">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="50289-214">Uzņēmums.'atrast()'.'nosaukums()'</span><span class="sxs-lookup"><span data-stu-id="50289-214">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="50289-215">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="50289-215">Click Save.</span></span>
<span data-ttu-id="50289-216">![ER modeļa kartēšanas noformētāja lapa](../media/er-financial-dimensions-guides-model-mapping4.png)</span><span class="sxs-lookup"><span data-stu-id="50289-216">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping4.png)</span></span>
65. <span data-ttu-id="50289-217">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="50289-217">Close the page.</span></span>
66. <span data-ttu-id="50289-218">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="50289-218">Click Save.</span></span>
67. <span data-ttu-id="50289-219">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="50289-219">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="50289-220">Pabeigt šo modeļa melnraksta versiju</span><span class="sxs-lookup"><span data-stu-id="50289-220">Complete this draft model's version</span></span>
1. <span data-ttu-id="50289-221">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="50289-221">Close the page.</span></span>
2. <span data-ttu-id="50289-222">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="50289-222">Close the page.</span></span>
3. <span data-ttu-id="50289-223">Noklikšķiniet uz Mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="50289-223">Click Change status.</span></span>
4. <span data-ttu-id="50289-224">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="50289-224">Click Complete.</span></span>
5. <span data-ttu-id="50289-225">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="50289-225">Click OK.</span></span>
<span data-ttu-id="50289-226">![ER modeļa kartēšanas noformētāja lapa](../media/er-financial-dimensions-guides-model-mapping5.png)</span><span class="sxs-lookup"><span data-stu-id="50289-226">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping5.png)</span></span>
