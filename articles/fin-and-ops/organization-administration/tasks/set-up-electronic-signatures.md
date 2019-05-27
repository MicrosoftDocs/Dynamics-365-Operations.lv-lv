---
title: Elektronisko parakstu iestatīšana
description: Izmantojiet šo procedūru, lai iestatītu elektroniskos parakstus.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysConfiguration, SIGParameters, SIGReasonCode, SIGProcSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eb6bf529b1e94d598e219482f182140402f2928a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545526"
---
# <a name="set-up-electronic-signatures"></a><span data-ttu-id="d45b8-103">Elektronisko parakstu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d45b8-103">Set up electronic signatures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d45b8-104">Izmantojiet šo procedūru, lai iestatītu elektroniskos parakstus.</span><span class="sxs-lookup"><span data-stu-id="d45b8-104">Use this procedure to set up electronic signatures.</span></span> <span data-ttu-id="d45b8-105">Elektroniskais paraksts apstiprina personas identitāti, kas gatavojas sākt vai apstiprināt skaitļošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="d45b8-105">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="d45b8-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir DAT.</span><span class="sxs-lookup"><span data-stu-id="d45b8-106">The demo data company used to create this procedure is DAT.</span></span>


## <a name="enable-the-electronic-signature-configuration-key"></a><span data-ttu-id="d45b8-107">Elektroniskā paraksta konfigurācijas atslēgas iespējošana</span><span class="sxs-lookup"><span data-stu-id="d45b8-107">Enable the Electronic signature configuration key</span></span>
1. <span data-ttu-id="d45b8-108">Pārejiet uz sadaļu Sistēmas administrēšana > Iestatījumi > Licences konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="d45b8-108">Go to System administration > Setup > License configuration.</span></span>
2. <span data-ttu-id="d45b8-109">Kokā izvērsiet sadaļu “Administrēšana”.</span><span class="sxs-lookup"><span data-stu-id="d45b8-109">In the tree, expand 'Administration'.</span></span>
    * <span data-ttu-id="d45b8-110">Pārbaudiet, vai izvēles rūtiņa Elektroniskais paraksts ir atzīmēta.</span><span class="sxs-lookup"><span data-stu-id="d45b8-110">Verify that the Electronic signature check box is selected.</span></span>  
    * <span data-ttu-id="d45b8-111">Ja izvēles rūtiņa Elektroniskais paraksts nav atzīmēta, jums ir jāiespējo uzturēšanas režīms.</span><span class="sxs-lookup"><span data-stu-id="d45b8-111">If the Electronic signature check box is not selected, you must enable maintenance mode.</span></span> <span data-ttu-id="d45b8-112">Uzturēšanas režīmu šajā vidē var iespējot, palaižot uzturēšanas darbu no Lifecycle Services vai lokāli izmantojot rīku Deployment.Setup.</span><span class="sxs-lookup"><span data-stu-id="d45b8-112">Maintenance mode can be enabled in this environment by running a maintenance job from Lifecycle Services, or by using the Deployment.Setup tool locally.</span></span>  
3. <span data-ttu-id="d45b8-113">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d45b8-113">Close the page.</span></span>

## <a name="set-up-electronic-signature-parameters"></a><span data-ttu-id="d45b8-114">Elektronisko parakstu parametru iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d45b8-114">Set up electronic signature parameters</span></span>
1. <span data-ttu-id="d45b8-115">Pārejiet uz sadaļu Organizācijas administrēšana > Iestatījumi > Elektroniskais paraksts > Elektroniskā paraksta parametri.</span><span class="sxs-lookup"><span data-stu-id="d45b8-115">Go to Organization administration > Setup > Electronic signature > Electronic signature parameters.</span></span>
2. <span data-ttu-id="d45b8-116">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="d45b8-116">Click Edit.</span></span>
3. <span data-ttu-id="d45b8-117">Laukā Paziņojums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d45b8-117">In the Notice field, type a value.</span></span>
    * <span data-ttu-id="d45b8-118">Ievadiet paziņojumu, ko parakstītāji saņem, kad tiek pieprasīts paraksts.</span><span class="sxs-lookup"><span data-stu-id="d45b8-118">Enter the notice that signers will receive when a signature is requested.</span></span> <span data-ttu-id="d45b8-119">Var ievadīt jebkādu tekstu.</span><span class="sxs-lookup"><span data-stu-id="d45b8-119">You can enter any text.</span></span> <span data-ttu-id="d45b8-120">Parasti šis teksts parāda lietotājiem, ko nozīmē elektroniska dokumenta parakstīšana.</span><span class="sxs-lookup"><span data-stu-id="d45b8-120">Typically, this text tells the user what it means to sign a document electronically.</span></span>  
    * <span data-ttu-id="d45b8-121">Ja vēlaties ievadīt paziņojuma tekstu papildu valodās, noklikšķiniet uz pogas Tulkojumi.</span><span class="sxs-lookup"><span data-stu-id="d45b8-121">If you want to enter the Notice text in additional languages, click the Translations button.</span></span>  
4. <span data-ttu-id="d45b8-122">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d45b8-122">Click Save.</span></span>
5. <span data-ttu-id="d45b8-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d45b8-123">Close the page.</span></span>

## <a name="set-up-reason-codes-for-electronic-signatures"></a><span data-ttu-id="d45b8-124">Pamatojuma kodu iestatīšana elektroniskajiem parakstiem</span><span class="sxs-lookup"><span data-stu-id="d45b8-124">Set up reason codes for electronic signatures</span></span>
1. <span data-ttu-id="d45b8-125">Pārejiet uz sadaļu Organizācijas administrēšana > Iestatījumi > Elektroniskais paraksts > Elektroniskā paraksta pamatojuma kodi.</span><span class="sxs-lookup"><span data-stu-id="d45b8-125">Go to Organization administration > Setup > Electronic signature > Electronic signature reason codes.</span></span>
2. <span data-ttu-id="d45b8-126">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d45b8-126">Click New.</span></span>
    * <span data-ttu-id="d45b8-127">Jums jāiestata pamatojuma kodi, pirms izmantojat elektroniskos parakstus.</span><span class="sxs-lookup"><span data-stu-id="d45b8-127">You must set up reason codes before using electronic signatures.</span></span> <span data-ttu-id="d45b8-128">Parakstot dokumentu, nepieciešams derīgs pamatojuma kods.</span><span class="sxs-lookup"><span data-stu-id="d45b8-128">A valid reason code is required when signing a document.</span></span>     <span data-ttu-id="d45b8-129">Parakstītājs atlasa pamatojuma kodu, lai norādītu elektroniskā paraksta mērķi.</span><span class="sxs-lookup"><span data-stu-id="d45b8-129">A signer selects a reason code to indicate the purpose of an electronic signature.</span></span> <span data-ttu-id="d45b8-130">Piemēram, pamatojuma kodu var izmantot, lai norādītu uz juridisku apstiprinājumu.</span><span class="sxs-lookup"><span data-stu-id="d45b8-130">For example, a reason code could be used to indicate legal approval.</span></span>  
3. <span data-ttu-id="d45b8-131">Laukā Pamatojuma kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d45b8-131">In the Reason code field, type a value.</span></span>
4. <span data-ttu-id="d45b8-132">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d45b8-132">In the Description field, type a value.</span></span>
    * <span data-ttu-id="d45b8-133">Ja nepieciešams, ievadiet papildu pamatojuma kodus.</span><span class="sxs-lookup"><span data-stu-id="d45b8-133">Enter additional reason codes, if needed.</span></span>  
5. <span data-ttu-id="d45b8-134">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d45b8-134">Click Save.</span></span>
6. <span data-ttu-id="d45b8-135">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d45b8-135">Close the page.</span></span>

## <a name="require-electronic-signatures-for-existing-processes"></a><span data-ttu-id="d45b8-136">Elektronisko parakstu pieprasīšana esošajiem procesiem</span><span class="sxs-lookup"><span data-stu-id="d45b8-136">Require electronic signatures for existing processes</span></span>
1. <span data-ttu-id="d45b8-137">Pārejiet uz sadaļu Organizācijas administrēšana > Iestatījumi > Elektroniskais paraksts > Elektroniskā paraksta prasības.</span><span class="sxs-lookup"><span data-stu-id="d45b8-137">Go to Organization administration > Setup > Electronic signature > Electronic signature requirements.</span></span>
2. <span data-ttu-id="d45b8-138">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d45b8-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d45b8-139">Atlasiet procesu, kam nepieciešami elektroniskie paraksti.</span><span class="sxs-lookup"><span data-stu-id="d45b8-139">Select a process that requires electronic signatures.</span></span>  
3. <span data-ttu-id="d45b8-140">Atlasiet vai notīriet izvēles rūtiņu Nepieciešamais paraksts.</span><span class="sxs-lookup"><span data-stu-id="d45b8-140">Select or clear the Signature required check box.</span></span>
    * <span data-ttu-id="d45b8-141">Atkārtojiet šīs darbības katram procesam, kas prasa elektronisko parakstu.</span><span class="sxs-lookup"><span data-stu-id="d45b8-141">Repeat these steps for each process that requires electronic signatures.</span></span>  
4. <span data-ttu-id="d45b8-142">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d45b8-142">Click Save.</span></span>

## <a name="create-a-custom-requirement-for-electronic-signatures"></a><span data-ttu-id="d45b8-143">Pielāgoto elektronisko parakstu prasību izveidošana</span><span class="sxs-lookup"><span data-stu-id="d45b8-143">Create a custom requirement for electronic signatures</span></span>
1. <span data-ttu-id="d45b8-144">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d45b8-144">Click New.</span></span>
2. <span data-ttu-id="d45b8-145">Atlasiet vai notīriet izvēles rūtiņu Nepieciešamais paraksts.</span><span class="sxs-lookup"><span data-stu-id="d45b8-145">Select or clear the Signature required check box.</span></span>
3. <span data-ttu-id="d45b8-146">Laukā Nosaukums ievadiet procesa nosaukumu, kuram nepieciešami elektroniskie paraksti.</span><span class="sxs-lookup"><span data-stu-id="d45b8-146">In the Name field, enter a name for the process that requires electronic signatures.</span></span>
4. <span data-ttu-id="d45b8-147">Laukā Tabulas nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d45b8-147">In the Table name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d45b8-148">Sarakstā atrodiet un atlasiet tabulu, kur saglabāti parakstāmie dati.</span><span class="sxs-lookup"><span data-stu-id="d45b8-148">In the list, find and select the table where the data that must be signed is stored.</span></span>
6. <span data-ttu-id="d45b8-149">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d45b8-149">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="d45b8-150">Laukā Lauka nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d45b8-150">In the Field name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="d45b8-151">Sarakstā atrodiet un atlasiet tabulas lauku, ko vēlaties uzraudzīt.</span><span class="sxs-lookup"><span data-stu-id="d45b8-151">In the list, find and select the field in the table that you want to monitor.</span></span>
9. <span data-ttu-id="d45b8-152">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d45b8-152">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d45b8-153">Norādiet, kad pieprasīt parakstus.</span><span class="sxs-lookup"><span data-stu-id="d45b8-153">Specify when a signature is required.</span></span>     <span data-ttu-id="d45b8-154">Atlasiet Vienmēr, ja paraksts ir nepieciešams katru reizi, kad mainās laukā esošie dati.</span><span class="sxs-lookup"><span data-stu-id="d45b8-154">Select Always if a signature is required when the data in the field changes.</span></span>     <span data-ttu-id="d45b8-155">Atlasiet Tikai, ja paraksts ir nepieciešams tikai noteiktos apstākļos.</span><span class="sxs-lookup"><span data-stu-id="d45b8-155">Select Only if a signature is required only under certain conditions.</span></span> <span data-ttu-id="d45b8-156">Ja atlasāt Tikai, jāatlasa arī viena no šīm opcijām: Ja ir ievietots ieraksts, Kad tiek atjaunināts ieraksts vai Kad ieraksts tiek dzēsts.</span><span class="sxs-lookup"><span data-stu-id="d45b8-156">If you select Only, you must also select one of the following options: When a record is inserted, When a record is updated, or When a record is deleted.</span></span>  
10. <span data-ttu-id="d45b8-157">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d45b8-157">Click Save.</span></span>
11. <span data-ttu-id="d45b8-158">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d45b8-158">Close the page.</span></span>

