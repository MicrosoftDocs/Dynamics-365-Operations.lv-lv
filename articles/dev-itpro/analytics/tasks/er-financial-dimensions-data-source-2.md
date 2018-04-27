--- 
title: "Modeļu kartēšana, lai finanšu dimensijas izmantotu kā datu avotu"
description: "Tālāk ir paskaidrots kā lietotājs, kam piešķirta loma sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c26713a8a391f9f10a6e24f6619c24c1615d4560
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---
# <a name="map-models--to-use-financial-dimensions-as-a-data-source"></a><span data-ttu-id="a8b2b-103">Modeļu kartēšana, lai finanšu dimensijas izmantotu kā datu avotu</span><span class="sxs-lookup"><span data-stu-id="a8b2b-103">Map models  to use financial dimensions as a data source</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a8b2b-104">Tālāk ir paskaidrots kā lietotājs, kam piešķirta loma sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="a8b2b-105">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="a8b2b-106">Lai izpildītu šos soļus, vispirms ir jāpabeidz soļi, kas aprakstīti procedūrā "ER Finanšu dimensijas, ko izmanto kā datu avotu" (1. daļa: datu modeļa izveide).</span><span class="sxs-lookup"><span data-stu-id="a8b2b-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 1: Design data model” procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="a8b2b-107">Pievienot nepieciešamos datu avotus modeļa kartēšanai</span><span class="sxs-lookup"><span data-stu-id="a8b2b-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="a8b2b-108">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a8b2b-109">Koka struktūrā atlasiet 'Finanšu dimensiju parauga modelis'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="a8b2b-110">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-110">Click Designer.</span></span>
4. <span data-ttu-id="a8b2b-111">Noklikšķiniet uz Kartēšanas modelis datu avotam.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="a8b2b-112">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-112">Click New.</span></span>
6. <span data-ttu-id="a8b2b-113">Laukā Definīcija, atlasiet Ieraksts.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="a8b2b-114">Laukā Nosaukums ierakstiet 'Dimensiju datu kartēšana'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="a8b2b-115">Laukā Apraksts ierakstiet 'Dimensiju datu kartēšana'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="a8b2b-116">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-116">Click Save.</span></span>
10. <span data-ttu-id="a8b2b-117">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-117">Click Designer.</span></span>
11. <span data-ttu-id="a8b2b-118">Kokā atlasiet "Dynamics 365 for Operations\Table".</span><span class="sxs-lookup"><span data-stu-id="a8b2b-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="a8b2b-119">Noklikšķiniet uz Pievienot sakni.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-119">Click Add root.</span></span>
13. <span data-ttu-id="a8b2b-120">Laukā Nosaukums ierakstiet "Uzņēmums".</span><span class="sxs-lookup"><span data-stu-id="a8b2b-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="a8b2b-121">Laukā Tabula ierakstiet "CompanyInfo".</span><span class="sxs-lookup"><span data-stu-id="a8b2b-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="a8b2b-122">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-122">Click OK.</span></span>
16. <span data-ttu-id="a8b2b-123">Koka struktūrā atlasiet 'Funkcijas\Detalizēta informācija par finanšu dimensijām'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="a8b2b-124">Noklikšķiniet uz Pievienot sakni.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-124">Click Add root.</span></span>
    * <span data-ttu-id="a8b2b-125">Šis datu avots norāda finanšu dimensiju sfēru, kas tiks definēta jebkuram pārskatam, kas tiks izmantots šajā modelī kā datu avots.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="a8b2b-126">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="a8b2b-127">Atlasiet Jā laukā Jautāt dimensijas.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="a8b2b-128">Atlasiet Jā, lai lietotājs varētu atlasīt dimensijas Lietotāja dialoglodziņā izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="a8b2b-129">Ja iestatīts uz Nē, visas pašreizējās instances finanšu dimensijas tiks izmantotas pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="a8b2b-130">Finanšu dimensiju atlases laukā atlasiet 'Juridiska persona'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="a8b2b-131">Atlasiet Visu, lai lietotājs varētu atlasīt vēlamo dimensiju pašreizējai instancei laukā Uzmeklēšana.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="a8b2b-132">Atlasiet juridisko personu, lai lietotājs varētu atlasīt dimensijas uzņēmumam laukā Uzmeklēšana.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="a8b2b-133">Atlasīt Dimensiju, lai lietotājs varētu atlasīt dimensijas, izmantojot vienu dimensiju kopu.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="a8b2b-134">Atlasiet Jā laukā Jautāt galveno kontu.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="a8b2b-135">Iestatiet “Jautāt galveno kontu” uz Jā, lai atļautu lietotājiem atlasīt galveno kontu kā daļu no dimensiju saraksta.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-135">Set ‘Ask for main account’ to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="a8b2b-136">Ja ir iestatīts uz Nē, galvenais konts netiks iekļauts dimensiju sarakstā, un opcija “Vai galvenais konts ir obligāts” ir iespējota.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-136">If set to No, the main account will not be included to the list of dimensions and the ‘Is main account mandatory’ option is enabled.</span></span> <span data-ttu-id="a8b2b-137">Ja opcija “Vai galvenais konts ir obligāts” ir iestatīta uz Jā, iekļaujiet galveno kontu dimensiju sarakstā, neatkarīgi no lietotāja veiktās atlases.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-137">If “Is main account mandatory’ is set to Yes, include the main account in the list of dimensions regardless of the user’s selection.</span></span>  
22. <span data-ttu-id="a8b2b-138">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-138">Click OK.</span></span>
23. <span data-ttu-id="a8b2b-139">Kokā atlasiet "Dynamics 365 for Operations\Table records".</span><span class="sxs-lookup"><span data-stu-id="a8b2b-139">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="a8b2b-140">Noklikšķiniet uz Pievienot sakni.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-140">Click Add root.</span></span>
25. <span data-ttu-id="a8b2b-141">Laukā Nosaukums ierakstiet 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-141">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="a8b2b-142">Laukā Pieprasīt vaicājumu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-142">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="a8b2b-143">Laukā Tabula ievadiet 'LedgerJournalTable'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-143">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="a8b2b-144">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-144">Click OK.</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="a8b2b-145">Kartēt datu modeļa elementus pievienotajiem datu avotiem</span><span class="sxs-lookup"><span data-stu-id="a8b2b-145">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="a8b2b-146">Kokā izvērsiet 'Žurnāls'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-146">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="a8b2b-147">Kokā izvērsiet 'Žurnāls\Darbība'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-147">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="a8b2b-148">Kokā izvērsiet 'Žurnāls\Darbība\Dimensiju dati'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-148">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="a8b2b-149">Kokā izvērsiet 'Dimensiju iestatījums'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-149">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="a8b2b-150">Kokā izvērsiet 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-150">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="a8b2b-151">Kokā izvērsiet "LedgerJournal\<Relations".</span><span class="sxs-lookup"><span data-stu-id="a8b2b-151">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="a8b2b-152">Kokā izvērsiet "LedgerJournal\<Relations\LedgerJournalTrans".</span><span class="sxs-lookup"><span data-stu-id="a8b2b-152">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="a8b2b-153">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Voucher".</span><span class="sxs-lookup"><span data-stu-id="a8b2b-153">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="a8b2b-154">Kokā atlasiet 'Žurnāls\Darbība\Dokuments'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-154">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="a8b2b-155">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-155">Click Bind.</span></span>
11. <span data-ttu-id="a8b2b-156">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)".</span><span class="sxs-lookup"><span data-stu-id="a8b2b-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="a8b2b-157">Ņemiet vērā, ka visām iestatītajām atsaucēm uz finanšu dimensijām, piemēram, LedgerDimension, ir pieejams attiecīgais datu avota vienums (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="a8b2b-157">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="a8b2b-158">Šī datu avota vienums nodrošina finanšu dimensijas no dimensiju kopas kā ierakstu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-158">This data source item offers the financial dimensions of that dimensions set as the record’s list.</span></span>  
12. <span data-ttu-id="a8b2b-159">Kokā izvērsiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)".</span><span class="sxs-lookup"><span data-stu-id="a8b2b-159">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="a8b2b-160">Kokā izvērsiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions".</span><span class="sxs-lookup"><span data-stu-id="a8b2b-160">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="a8b2b-161">Kokā izvērsiet "LedgerJournal\\<Relācijas\LedgerJournalTrans\Konts.Dimensija(LedgerDimension.Dimension)\Galvenais konts un dimensijas\Vērtība".</span><span class="sxs-lookup"><span data-stu-id="a8b2b-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="a8b2b-162">Kokā izvērsiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition".</span><span class="sxs-lookup"><span data-stu-id="a8b2b-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="a8b2b-163">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name".</span><span class="sxs-lookup"><span data-stu-id="a8b2b-163">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="a8b2b-164">Kokā atlasiet 'Žurnāls\Darbība\Dimensiju dati\Nosaukums'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-164">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="a8b2b-165">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-165">Click Bind.</span></span>
19. <span data-ttu-id="a8b2b-166">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description".</span><span class="sxs-lookup"><span data-stu-id="a8b2b-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="a8b2b-167">Kokā atlasiet 'Žurnāls\Darbība\Dimensiju dati\Apraksts'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-167">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="a8b2b-168">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-168">Click Bind.</span></span>
22. <span data-ttu-id="a8b2b-169">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code".</span><span class="sxs-lookup"><span data-stu-id="a8b2b-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="a8b2b-170">Kokā atlasiet 'Žurnāls\Darbība\Dimensiju dati\Kods'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-170">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="a8b2b-171">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-171">Click Bind.</span></span>
25. <span data-ttu-id="a8b2b-172">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions".</span><span class="sxs-lookup"><span data-stu-id="a8b2b-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="a8b2b-173">Kokā atlasiet 'Žurnāls\Darbība\Dimensiju dati'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-173">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="a8b2b-174">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-174">Click Bind.</span></span>
28. <span data-ttu-id="a8b2b-175">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)".</span><span class="sxs-lookup"><span data-stu-id="a8b2b-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="a8b2b-176">Kokā atlasiet 'Žurnāls\Darbība\Debets'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-176">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="a8b2b-177">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-177">Click Bind.</span></span>
31. <span data-ttu-id="a8b2b-178">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)".</span><span class="sxs-lookup"><span data-stu-id="a8b2b-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="a8b2b-179">Kokā atlasiet 'Žurnāls\Darbība\Datums'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-179">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="a8b2b-180">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-180">Click Bind.</span></span>
34. <span data-ttu-id="a8b2b-181">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)".</span><span class="sxs-lookup"><span data-stu-id="a8b2b-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="a8b2b-182">Kokā atlasiet 'Žurnāls\Darbība\Valūta'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-182">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="a8b2b-183">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-183">Click Bind.</span></span>
37. <span data-ttu-id="a8b2b-184">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)".</span><span class="sxs-lookup"><span data-stu-id="a8b2b-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="a8b2b-185">Kokā atlasiet 'Žurnāls\Darbība\Kredīts'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-185">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="a8b2b-186">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-186">Click Bind.</span></span>
40. <span data-ttu-id="a8b2b-187">Kokā atlasiet "LedgerJournal\<Relations\LedgerJournalTrans".</span><span class="sxs-lookup"><span data-stu-id="a8b2b-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="a8b2b-188">Kokā atlasiet 'Žurnāls\Darbība'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-188">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="a8b2b-189">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-189">Click Bind.</span></span>
43. <span data-ttu-id="a8b2b-190">Kokā atlasiet 'LedgerJournal\Žurnāla iedaļas numurs(JournalNum)'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-190">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="a8b2b-191">Kokā atlasiet 'Žurnāls\Iedaļa'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-191">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="a8b2b-192">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-192">Click Bind.</span></span>
46. <span data-ttu-id="a8b2b-193">Kokā atlasiet 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-193">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="a8b2b-194">Kokā atlasiet 'Žurnāls'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-194">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="a8b2b-195">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-195">Click Bind.</span></span>
49. <span data-ttu-id="a8b2b-196">Kokā izvērsiet 'Dimensijas'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-196">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="a8b2b-197">Kokā izvērsiet 'Dimensijas\Galvenais konts un dimensijas'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-197">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="a8b2b-198">Kokā izvērsiet 'Dimensijas\Galvenais konts un dimensijas\Definīcija'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-198">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="a8b2b-199">Kokā atlasiet 'Dimensijas\Galvenais konts un dimensijas\Definīcija\Nosaukums'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-199">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="a8b2b-200">Kokā izvērsiet 'Dimensiju iestatīšana\Kods'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-200">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="a8b2b-201">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-201">Click Bind.</span></span>
55. <span data-ttu-id="a8b2b-202">Kokā atlasiet 'Dimensijas\Galvenais konts un dimensijas\Definīcija\Pārskata kolonnas nosaukums'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="a8b2b-203">Kokā atlasiet 'Dimensiju iestatīšana\Nosaukums'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-203">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="a8b2b-204">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-204">Click Bind.</span></span>
58. <span data-ttu-id="a8b2b-205">Kokā atlasiet 'Dimensijas\Galvenais konts un dimensijas'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-205">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="a8b2b-206">Kokā atlasiet 'Dimensiju iestatīšana'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-206">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="a8b2b-207">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-207">Click Bind.</span></span>
61. <span data-ttu-id="a8b2b-208">Kokā atlasiet 'Uzņēmums'.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-208">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="a8b2b-209">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-209">Click Edit.</span></span>
63. <span data-ttu-id="a8b2b-210">Laukā expressionAsStringText field ievadiet 'Uzņēmums.'atrast()'.'nosaukums()''.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-210">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="a8b2b-211">Uzņēmums.'atrast()'.'nosaukums()'</span><span class="sxs-lookup"><span data-stu-id="a8b2b-211">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="a8b2b-212">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-212">Click Save.</span></span>
65. <span data-ttu-id="a8b2b-213">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-213">Close the page.</span></span>
66. <span data-ttu-id="a8b2b-214">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-214">Click Save.</span></span>
67. <span data-ttu-id="a8b2b-215">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-215">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="a8b2b-216">Pabeigt šo modeļa melnraksta versiju</span><span class="sxs-lookup"><span data-stu-id="a8b2b-216">Complete this draft model’s version</span></span>
1. <span data-ttu-id="a8b2b-217">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-217">Close the page.</span></span>
2. <span data-ttu-id="a8b2b-218">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-218">Close the page.</span></span>
3. <span data-ttu-id="a8b2b-219">Noklikšķiniet uz Mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-219">Click Change status.</span></span>
4. <span data-ttu-id="a8b2b-220">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-220">Click Complete.</span></span>
5. <span data-ttu-id="a8b2b-221">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a8b2b-221">Click OK.</span></span>


