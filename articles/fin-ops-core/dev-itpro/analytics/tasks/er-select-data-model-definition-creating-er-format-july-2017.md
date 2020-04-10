---
title: Datu modeļu definīciju atlase, veidojot formātus
description: Lai izpildītu šīs procedūras darbības, vispirms izpildiet procedūrau “ER Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu”.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 374c31b5ea9160fba773e82f658e8de05c67cab4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143250"
---
# <a name="select-data-model-definitions-when-you-create-formats"></a><span data-ttu-id="2bb84-103">Datu modeļu definīciju atlase, veidojot formātus</span><span class="sxs-lookup"><span data-stu-id="2bb84-103">Select data model definitions when you create formats</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2bb84-104">Lai izpildītu šīs procedūras darbības, vispirms izpildiet procedūrau “ER Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu”.</span><span class="sxs-lookup"><span data-stu-id="2bb84-104">To complete the steps in this procedure, you must first complete the procedure, ER Create a configuration provider and mark it as active.</span></span> 

<span data-ttu-id="2bb84-105">Šajā procedūrā parādīts, kā modeļa saknes vienumu var atlasīt kā datu modeļa definīciju ievietošanai elektroniskā pārskata (ER) formāta konfigurācijā, kas paredzēta elektronisko dokumentu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="2bb84-105">This procedure shows how a model's root item can be selected as a data model definition for inserting an Electronic reporting (ER) format configuration that is designed to generate electronic documents.</span></span> <span data-ttu-id="2bb84-106">Šajā procedūrā jūs pievienosit jaunu ER formāta konfigurāciju parauga uzņēmumam “Litware, Inc.”.</span><span class="sxs-lookup"><span data-stu-id="2bb84-106">In this procedure, you will add a new ER format configuration for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="2bb84-107">Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma.</span><span class="sxs-lookup"><span data-stu-id="2bb84-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="2bb84-108">Darbības var veikt, izmantojot jebkuru datu kopu.</span><span class="sxs-lookup"><span data-stu-id="2bb84-108">The steps can be completed by using any dataset.</span></span>

1. <span data-ttu-id="2bb84-109">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="2bb84-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="2bb84-110">Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam “Litware, Inc.” ir pieejams un ir atzīmēts kā aktīvs.</span><span class="sxs-lookup"><span data-stu-id="2bb84-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="2bb84-111">Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas aprakstītas procedūrā “Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu”.</span><span class="sxs-lookup"><span data-stu-id="2bb84-111">If you don't see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  
2. <span data-ttu-id="2bb84-112">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="2bb84-112">Click Reporting configurations.</span></span>

## <a name="add-a-new-er-data-model-configuration"></a><span data-ttu-id="2bb84-113">Pievienot jaunu ER datu modeļa konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="2bb84-113">Add a new ER data model configuration</span></span>
1. <span data-ttu-id="2bb84-114">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2bb84-114">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="2bb84-115">Mēs pievienojam jaunu ER modeļa konfigurāciju, kas satur datu modeli, kurš paredzēts lietošanai kā datu avots ER pārskatu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="2bb84-115">We add a new ER model configuration containing a data model that is designed to be used as data source for generation ER reports.</span></span>  
2. <span data-ttu-id="2bb84-116">Laukā Nosaukums ierakstiet “Maksājuma modelis (fiktīvs)”.</span><span class="sxs-lookup"><span data-stu-id="2bb84-116">In the Name field, type 'Payment model (fictitious)'.</span></span>
    * <span data-ttu-id="2bb84-117">Maksājuma modelis (fiktīvs)</span><span class="sxs-lookup"><span data-stu-id="2bb84-117">Payment model (fictitious)</span></span>  
3. <span data-ttu-id="2bb84-118">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="2bb84-118">Click Create configuration.</span></span>
4. <span data-ttu-id="2bb84-119">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="2bb84-119">Click Designer.</span></span>
    * <span data-ttu-id="2bb84-120">Atveriet ER veidotāju, lai norādītu šīs konfigurācijas datu modeļa struktūru.</span><span class="sxs-lookup"><span data-stu-id="2bb84-120">Open the ER designer to specify the structure of data model of this configuration.</span></span>  
    * <span data-ttu-id="2bb84-121">Pieņemsim, ka mēs noformējam datu modeli maksājumu biznesa jomai, lai atbalstītu 2 maksājumu metodes — kredīta pārskaitījumu un tiešo debetu.</span><span class="sxs-lookup"><span data-stu-id="2bb84-121">Assume that we design the data model for payments business domain to support 2 payment methods – credit transfer and direct debit ones.</span></span>  
5. <span data-ttu-id="2bb84-122">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2bb84-122">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="2bb84-123">Laukā Nosaukums ierakstiet “Maksājumi — kredīta pārskaitījums”.</span><span class="sxs-lookup"><span data-stu-id="2bb84-123">In the Name field, type 'Payments – credit transfer'.</span></span>
    * <span data-ttu-id="2bb84-124">Maksājumi — kredīta pārskaitījums</span><span class="sxs-lookup"><span data-stu-id="2bb84-124">Payments – credit transfer</span></span>  
7. <span data-ttu-id="2bb84-125">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="2bb84-125">Click Add.</span></span>
8. <span data-ttu-id="2bb84-126">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2bb84-126">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="2bb84-127">Laukā Jauns zars ievadiet “Modeļa sakne”.</span><span class="sxs-lookup"><span data-stu-id="2bb84-127">In the New node as a field, enter 'Model root'.</span></span>
10. <span data-ttu-id="2bb84-128">Laukā Nosaukums ierakstiet “Maksājumi — tiešais debets”.</span><span class="sxs-lookup"><span data-stu-id="2bb84-128">In the Name field, type 'Payments – direct debit'.</span></span>
    * <span data-ttu-id="2bb84-129">Maksājumi — tiešais debets</span><span class="sxs-lookup"><span data-stu-id="2bb84-129">Payments – direct debit</span></span>  
11. <span data-ttu-id="2bb84-130">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="2bb84-130">Click Add.</span></span>
12. <span data-ttu-id="2bb84-131">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="2bb84-131">Click Save.</span></span>
13. <span data-ttu-id="2bb84-132">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2bb84-132">Close the page.</span></span>
14. <span data-ttu-id="2bb84-133">Noklikšķiniet uz Mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="2bb84-133">Click Change status.</span></span>
    * <span data-ttu-id="2bb84-134">Pabeidziet modeļa melnraksta versiju, lai to padarītu pieejamu jaunā modeļa kartējumos un formātos.</span><span class="sxs-lookup"><span data-stu-id="2bb84-134">Complete the draft version of the model to make it available in new model mappings and formats.</span></span>  
15. <span data-ttu-id="2bb84-135">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="2bb84-135">Click Complete.</span></span>
16. <span data-ttu-id="2bb84-136">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2bb84-136">Click OK.</span></span>

## <a name="start-to-enter-a-new-er-format-configuration"></a><span data-ttu-id="2bb84-137">Sākt ievadīt jaunu ER formāta konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="2bb84-137">Start to enter a new ER format configuration</span></span>
1. <span data-ttu-id="2bb84-138">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2bb84-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="2bb84-139">Laukā Jauns ievadiet “Uz datu modeli Maksājuma modelis (fiktīvs) balstīts formāts”.</span><span class="sxs-lookup"><span data-stu-id="2bb84-139">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="2bb84-140">Ievadiet vai atlasiet kādu vērtību laukā Datu modelis.</span><span class="sxs-lookup"><span data-stu-id="2bb84-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="2bb84-141">Ņemiet vērā, ka visi saknes vienumi ar atlasīto datu modeli pašlaik ir pieejami atlasei kā datu modeļa definīcijas.</span><span class="sxs-lookup"><span data-stu-id="2bb84-141">Note that all root items of the selected data model are currently available for selection as a data model definition.</span></span> <span data-ttu-id="2bb84-142">Varat turpināt noformēt formātu, izmantojot jebkuru no nepieciešamajiem datu modeļa saknes vienumiem.</span><span class="sxs-lookup"><span data-stu-id="2bb84-142">You can continue to design your format by using any of the required root items of the data model.</span></span> <span data-ttu-id="2bb84-143">Varat turpināt arī tad, ja atlasītajam saknes vienumam trūkst modeļa kartējuma.</span><span class="sxs-lookup"><span data-stu-id="2bb84-143">A missing model mapping for the selected root item doesn't prevent you from continuing.</span></span>  
4. <span data-ttu-id="2bb84-144">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2bb84-144">Close the page.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="2bb84-145">Pievienot jaunu ER datu modeļa kartējuma konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="2bb84-145">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="2bb84-146">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2bb84-146">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="2bb84-147">Laukā Jauns ievadiet “Uz datu modeli Maksājuma modelis (fiktīvs) balstīts modeļa kartējums”.</span><span class="sxs-lookup"><span data-stu-id="2bb84-147">In the New field, enter 'Model Mapping based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="2bb84-148">Laukā Nosaukums ierakstiet “Maksājuma modeļa kartējumi (fiktīvi)”.</span><span class="sxs-lookup"><span data-stu-id="2bb84-148">In the Name field, type 'Payment model mappings (fictitious)'.</span></span>
    * <span data-ttu-id="2bb84-149">Maksājuma modeļa kartējumi (fiktīvi)</span><span class="sxs-lookup"><span data-stu-id="2bb84-149">Payment model mappings (fictitious)</span></span>  
4. <span data-ttu-id="2bb84-150">Ievadiet vai atlasiet kādu vērtību laukā Datu modelis.</span><span class="sxs-lookup"><span data-stu-id="2bb84-150">In the Data model definition field, enter or select a value.</span></span>
5. <span data-ttu-id="2bb84-151">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="2bb84-151">Click Create configuration.</span></span>

## <a name="design-er-model-mappings"></a><span data-ttu-id="2bb84-152">Veidot ER modeļu kartējumus</span><span class="sxs-lookup"><span data-stu-id="2bb84-152">Design ER model mappings</span></span>
1. <span data-ttu-id="2bb84-153">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="2bb84-153">Click Designer.</span></span>
    * <span data-ttu-id="2bb84-154">Izmantojiet ER izstrādes rīku, lai norādītu nepieciešamo saknes vienumu modeļa kartējumus.</span><span class="sxs-lookup"><span data-stu-id="2bb84-154">Use the ER designer to specify the model mappings for the required root items.</span></span>  
2. <span data-ttu-id="2bb84-155">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="2bb84-155">Click Designer.</span></span>
    * <span data-ttu-id="2bb84-156">Simulējiet atlasītā modeļa kartējums iestatīšanu atlasītājam modeļa saknes vienumam.</span><span class="sxs-lookup"><span data-stu-id="2bb84-156">Simulate setting of selected model mapping for the selected model's root item.</span></span>  
3. <span data-ttu-id="2bb84-157">Kokā atlasiet 'Dynamics 365 for Operations\Tabulas ieraksti'.</span><span class="sxs-lookup"><span data-stu-id="2bb84-157">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
4. <span data-ttu-id="2bb84-158">Noklikšķiniet uz Pievienot sakni.</span><span class="sxs-lookup"><span data-stu-id="2bb84-158">Click Add root.</span></span>
5. <span data-ttu-id="2bb84-159">Laukā Nosaukums ierakstiet “Virsgrāmata”.</span><span class="sxs-lookup"><span data-stu-id="2bb84-159">In the Name field, type 'Ledger'.</span></span>
6. <span data-ttu-id="2bb84-160">Laukā Tabula ierakstiet 'LedgerJournalTrans'.</span><span class="sxs-lookup"><span data-stu-id="2bb84-160">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="2bb84-161">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="2bb84-161">LedgerJournalTrans</span></span>  
7. <span data-ttu-id="2bb84-162">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2bb84-162">Click OK.</span></span>
8. <span data-ttu-id="2bb84-163">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="2bb84-163">Click Save.</span></span>
9. <span data-ttu-id="2bb84-164">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2bb84-164">Close the page.</span></span>
10. <span data-ttu-id="2bb84-165">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2bb84-165">Close the page.</span></span>

## <a name="start-to-enter-another-new-er-format-configuration"></a><span data-ttu-id="2bb84-166">Sākt ievadīt citu jaunu ER formāta konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="2bb84-166">Start to enter another new ER format configuration</span></span>
1. <span data-ttu-id="2bb84-167">Koka struktūrā atlasiet “Maksājuma modelis (fiktīvs)”.</span><span class="sxs-lookup"><span data-stu-id="2bb84-167">In the tree, select 'Payment model (fictitious)'.</span></span>
2. <span data-ttu-id="2bb84-168">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2bb84-168">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="2bb84-169">Laukā Jauns ievadiet “Uz datu modeli Maksājuma modelis (fiktīvs) balstīts formāts”.</span><span class="sxs-lookup"><span data-stu-id="2bb84-169">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
4. <span data-ttu-id="2bb84-170">Ievadiet vai atlasiet kādu vērtību laukā Datu modelis.</span><span class="sxs-lookup"><span data-stu-id="2bb84-170">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="2bb84-171">Ņemiet vērā, ka tagad ir pieejams tikai viens saknes vienums, lai kartētu programmas datu avotus.</span><span class="sxs-lookup"><span data-stu-id="2bb84-171">Note that now only one root item is available to map to the application data sources.</span></span> <span data-ttu-id="2bb84-172">Kad ir ieviests vismaz viens modeļa kartējums, kā modeļa definīciju ER formāta pievienošanas laikā var atlasīt tikai modeļa saknes vienumus, kas ir kartēti programmas datu avotiem.</span><span class="sxs-lookup"><span data-stu-id="2bb84-172">When at least one model mapping is introduced, only the model's root items that are mapped to application data sources can be selected as a model definition while the ER format is added.</span></span>   
5. <span data-ttu-id="2bb84-173">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2bb84-173">Close the page.</span></span>

