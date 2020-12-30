---
title: ER Izveidotā formāta komponentus kartēt uz datu modeļa elementiem (2016. novembris)
description: Nākamajā procedūrā ir parādīts, kā lietotājs ar lomu Sistēmas administrators vai lomu Elektroniskā pārskata izstrādātājs datu modeļa elementus var kartēt uz izveidotās elektronisko pārskatu veidošanas (Electronic reporting — ER) konfigurācijas komponentiem, kas nosaka elektroniskā dokumenta formātu maksājumu biznesa jomai.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 109a6736196b6ed3d1445a9f1a70c5f2b9d5af58
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684335"
---
# <a name="er-map-components-of-the-created-format-to-data-model-elements-november-2016"></a><span data-ttu-id="b4ce3-103">ER Izveidotā formāta komponentus kartēt uz datu modeļa elementiem (2016. novembris)</span><span class="sxs-lookup"><span data-stu-id="b4ce3-103">ER Map components of the created format to data model elements (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b4ce3-104">Nākamajā procedūrā ir parādīts, kā lietotājs ar lomu Sistēmas administrators vai lomu Elektroniskā pārskata izstrādātājs datu modeļa elementus var kartēt uz izveidotās elektronisko pārskatu veidošanas (Electronic reporting — ER) konfigurācijas komponentiem, kas nosaka elektroniskā dokumenta formātu maksājumu biznesa jomai.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-104">The following procedure shows how a user in either the System administrator or Electronic reporting developer role can map data model elements to components of the created Electronic reporting (ER) configuration, which defines an electronic document format for the payments business domain.</span></span> <span data-ttu-id="b4ce3-105">Šis formāts vēlāk tiks lietots, lai ģenerētu elektroniskos dokumentus maksājumu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-105">This format will be used later to generate electronic documents for processing payments.</span></span> <span data-ttu-id="b4ce3-106">Šajā piemērā jūs izveidosiet formāta konfigurāciju parauga uzņēmumam 'Litware, Inc.'.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-106">In this example, you will create a format configuration for the sample company, 'Litware, Inc.'.</span></span> <span data-ttu-id="b4ce3-107">Šīs darbības var veikt jebkurā uzņēmumā, jo ER konfigurācijas tiek koplietotas visos uzņēmumos.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-107">These steps can be performed in any company as ER configurations are shared for all companies.</span></span> <span data-ttu-id="b4ce3-108">Lai izpildītu šīs darbības, vispirms ir jāizpilda uzdevuma ceļvedī "Izveidot formāta konfigurāciju" aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-108">To complete these steps, you must first complete the steps in the "Create a format configuration" task guide.</span></span>


## <a name="select-a-format-configuration"></a><span data-ttu-id="b4ce3-109">Atlasīt formāta konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="b4ce3-109">Select a format configuration</span></span>
1. <span data-ttu-id="b4ce3-110">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="b4ce3-111">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="b4ce3-112">Kokā izvērsiet “Maksājumi (vienkāršotais modelis)”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-112">In the tree, expand 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="b4ce3-113">Kokā atlasiet 'Maksājumi (vienkāršotais modelis)\BAKS (UK fiktīvs)'.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-113">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
5. <span data-ttu-id="b4ce3-114">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-114">Click Designer.</span></span>

## <a name="map-format-components-to-data-model-elements"></a><span data-ttu-id="b4ce3-115">Formātā komponentu kartēšana datu modeļa elementos</span><span class="sxs-lookup"><span data-stu-id="b4ce3-115">Map format components to data model elements</span></span>
1. <span data-ttu-id="b4ce3-116">Noklikšķiniet uz Izvērst/sakļaut.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-116">Click Expand/collapse.</span></span>
2. <span data-ttu-id="b4ce3-117">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-117">Click the Mapping tab.</span></span>
3. <span data-ttu-id="b4ce3-118">Koka struktūrā izvērsiet elementu “modelis”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-118">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="b4ce3-119">Koka struktūrā atlasiet zaru “Xml\Ziņojums\ProcessingDate\DateTime”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-119">In the tree, select 'Xml\Message\ProcessingDate\DateTime'.</span></span>
5. <span data-ttu-id="b4ce3-120">Koka struktūrā atlasiet zaru “modelis\ProcessingDateTime”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-120">In the tree, select 'model\ProcessingDateTime'.</span></span>
6. <span data-ttu-id="b4ce3-121">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-121">Click Bind.</span></span>
7. <span data-ttu-id="b4ce3-122">Koka struktūrā atlasiet zaru “Xml\Ziņojums\MessageId\Virkne”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-122">In the tree, select 'Xml\Message\MessageId\String'.</span></span>
8. <span data-ttu-id="b4ce3-123">Koka struktūrā atlasiet zaru “modelis\MessageIdentification”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-123">In the tree, select 'model\MessageIdentification'.</span></span>
9. <span data-ttu-id="b4ce3-124">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-124">Click Bind.</span></span>
10. <span data-ttu-id="b4ce3-125">Kokā izvērsiet sadaļu “modelis\Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-125">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="b4ce3-126">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Summa\Virkne”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-126">In the tree, select 'Xml\Message\Payments\Item\Amount\String'.</span></span>
12. <span data-ttu-id="b4ce3-127">Koka struktūrā atlasiet zaru “modelis\Maksājumi\InstructedAmount”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-127">In the tree, select 'model\Payments\InstructedAmount'.</span></span>
13. <span data-ttu-id="b4ce3-128">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-128">Click Bind.</span></span>
14. <span data-ttu-id="b4ce3-129">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\TransDate\DateTime”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-129">In the tree, select 'Xml\Message\Payments\Item\TransDate\DateTime'.</span></span>
15. <span data-ttu-id="b4ce3-130">Koka struktūrā atlasiet zaru “modelis\Maksājumi\TransactionDate”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-130">In the tree, select 'model\Payments\TransactionDate'.</span></span>
16. <span data-ttu-id="b4ce3-131">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-131">Click Bind.</span></span>
17. <span data-ttu-id="b4ce3-132">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Apraksts\Virkne”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-132">In the tree, select 'Xml\Message\Payments\Item\Description\String'.</span></span>
18. <span data-ttu-id="b4ce3-133">Kokā atlasiet “modelis\Maksājumi\Apraksts”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-133">In the tree, select 'model\Payments\Description'.</span></span>
19. <span data-ttu-id="b4ce3-134">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-134">Click Bind.</span></span>
20. <span data-ttu-id="b4ce3-135">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Valūta\Virkne”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-135">In the tree, select 'Xml\Message\Payments\Item\Currency\String'.</span></span>
21. <span data-ttu-id="b4ce3-136">Koka struktūrā atlasiet elementu “modelis\Maksājumi\Valūta”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-136">In the tree, select 'model\Payments\Currency'.</span></span>
22. <span data-ttu-id="b4ce3-137">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-137">Click Bind.</span></span>
23. <span data-ttu-id="b4ce3-138">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\ID”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-138">In the tree, select 'Xml\Message\Payments\Item\Id'.</span></span>
24. <span data-ttu-id="b4ce3-139">Koka struktūrā atlasiet zaru “modelis\Maksājumi\End2EndID”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-139">In the tree, select 'model\Payments\End2EndID'.</span></span>
25. <span data-ttu-id="b4ce3-140">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-140">Click Bind.</span></span>
26. <span data-ttu-id="b4ce3-141">Kokā izvērsiet sadaļu “modelis\Maksājumi\Kreditors”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-141">In the tree, expand 'model\Payments\Creditor'.</span></span>
27. <span data-ttu-id="b4ce3-142">Kokā izvērsiet elementu “modelis\Maksājumi\Kreditors\Konts“.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-142">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
28. <span data-ttu-id="b4ce3-143">Kokā izvērsiet elementu “modelis\Maksājumi\Kreditors\Aģents“.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-143">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
29. <span data-ttu-id="b4ce3-144">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Nosaukums\Virkne”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-144">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
30. <span data-ttu-id="b4ce3-145">Kokā atlasiet “modelis\Maksājumi\Kreditors\Nosaukums”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-145">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
31. <span data-ttu-id="b4ce3-146">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-146">Click Bind.</span></span>
32. <span data-ttu-id="b4ce3-147">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka\RoutingNumber\Virkne”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber\String'.</span></span>
33. <span data-ttu-id="b4ce3-148">Koka struktūrā atlasiet zaru “modelis\Maksājumi\Kreditors\Aģents\RoutingNumber”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-148">In the tree, select 'model\Payments\Creditor\Agent\RoutingNumber'.</span></span>
34. <span data-ttu-id="b4ce3-149">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-149">Click Bind.</span></span>
35. <span data-ttu-id="b4ce3-150">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka\AccountNumber\Virkne”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-150">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber\String'.</span></span>
36. <span data-ttu-id="b4ce3-151">Kokā atlasiet “modelis\Maksājumi\Kreditors\Konts\Numurs”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-151">In the tree, select 'model\Payments\Creditor\Account\Number'.</span></span>
37. <span data-ttu-id="b4ce3-152">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-152">Click Bind.</span></span>
38. <span data-ttu-id="b4ce3-153">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Nosaukums\Virkne”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-153">In the tree, select 'Xml\Message\Payments\Item\Payer\Name\String'.</span></span>
39. <span data-ttu-id="b4ce3-154">Kokā izvērsiet sadaļu “modelis\Maksājumi\Debitors”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-154">In the tree, expand 'model\Payments\Debtor'.</span></span>
40. <span data-ttu-id="b4ce3-155">Kokā izvērsiet elementu “modelis\Maksājumi\Debitors\Konts“.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-155">In the tree, expand 'model\Payments\Debtor\Account'.</span></span>
41. <span data-ttu-id="b4ce3-156">Kokā izvērsiet sadaļu “modelis\Maksājumi\Debitors\Aģents”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-156">In the tree, expand 'model\Payments\Debtor\Agent'.</span></span>
42. <span data-ttu-id="b4ce3-157">Kokā atlasiet “modelis\Maksājumi\Debitors\Nosaukums”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-157">In the tree, select 'model\Payments\Debtor\Name'.</span></span>
43. <span data-ttu-id="b4ce3-158">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-158">Click Bind.</span></span>
44. <span data-ttu-id="b4ce3-159">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Banka\RoutingNumber\Virkne”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-159">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber\String'.</span></span>
45. <span data-ttu-id="b4ce3-160">Koka struktūrā atlasiet zaru “modelis\Maksājumi\Debitors\Aģents\RoutingNumber”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-160">In the tree, select 'model\Payments\Debtor\Agent\RoutingNumber'.</span></span>
46. <span data-ttu-id="b4ce3-161">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-161">Click Bind.</span></span>
47. <span data-ttu-id="b4ce3-162">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Banka\AccountNumber\Virkne”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-162">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber\String'.</span></span>
48. <span data-ttu-id="b4ce3-163">Kokā atlasiet “modelis\Maksājumi\Debitors\Konts\Numurs”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-163">In the tree, select 'model\Payments\Debtor\Account\Number'.</span></span>
49. <span data-ttu-id="b4ce3-164">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-164">Click Bind.</span></span>
50. <span data-ttu-id="b4ce3-165">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-165">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="b4ce3-166">Kokā atlasiet “modelis\Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-166">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="b4ce3-167">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-167">Click Bind.</span></span>
53. <span data-ttu-id="b4ce3-168">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-168">Click Save.</span></span>

## <a name="validate-format-mapping"></a><span data-ttu-id="b4ce3-169">Validēt formāta kartējumu</span><span class="sxs-lookup"><span data-stu-id="b4ce3-169">Validate format mapping</span></span>
1. <span data-ttu-id="b4ce3-170">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-170">Click Validate.</span></span>
    * <span data-ttu-id="b4ce3-171">Validējiet jauno kartēšanu, lai pārliecinātos, ka visi saistījumi ir pareizi.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-171">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="b4ce3-172">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-172">Close the page.</span></span>

## <a name="change-status-of-the-current-version-of-format-configuration"></a><span data-ttu-id="b4ce3-173">Formāta konfigurācijas pašreizējās versijas statusa maiņa</span><span class="sxs-lookup"><span data-stu-id="b4ce3-173">Change status of the current version of format configuration</span></span>
<span data-ttu-id="b4ce3-174">Nākamajās darbībās jūs formāta konfigurācijas statusu no Melnraksts mainīsiet uz Pabeigts, lai to padarītu pieejamu maksājuma dokumentu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-174">In the next steps, you'll change the status of the format configuration from Draft to Completed to make it available for payment document generation.</span></span>  
1. <span data-ttu-id="b4ce3-175">Noklikšķiniet uz Mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-175">Click Change status.</span></span>
2. <span data-ttu-id="b4ce3-176">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-176">Click Complete.</span></span>
3. <span data-ttu-id="b4ce3-177">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-177">In the Description field, type a value.</span></span>
    * <span data-ttu-id="b4ce3-178">Piemēram, “1. versija”.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-178">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="b4ce3-179">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-179">Click OK.</span></span>
5. <span data-ttu-id="b4ce3-180">Atlasiet pašreizējās konfigurācijas pabeigto versiju.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-180">Select completed version of the current configuration.</span></span>
    * <span data-ttu-id="b4ce3-181">Ņemiet vērā, ka konfigurācija tiek saglabāta kā pabeigta versija 1.1. Tā ir formāta versija 1, kas ir balstīta uz datu modeļa versiju 1.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-181">Note that the configuration is saved as completed version 1.1: version 1 of the format based on the version 1 of the data model.</span></span>  

## <a name="define-effective-date-for-completed-version-of-format"></a><span data-ttu-id="b4ce3-182">Spēkā stāšanās datuma definēšana formāta pabeigtajai versijai</span><span class="sxs-lookup"><span data-stu-id="b4ce3-182">Define effective date for completed version of format</span></span>
<span data-ttu-id="b4ce3-183">Katru formāta versiju var konfigurēt, kā pieejamu lietošanai, sākot ar noteiktu datumu.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-183">Each format version can be configured as available for usage starting from a certain date.</span></span> <span data-ttu-id="b4ce3-184">Ja noteiktā datumā ir aktīvas vairākas formāta versijas, tad lietošanai tiek atlasīts visjaunākais formāts (pamatojoties uz versijas numuru).</span><span class="sxs-lookup"><span data-stu-id="b4ce3-184">When more than one format version is active on a certain date, the latest format (based on version number) will be selected for usage.</span></span> <span data-ttu-id="b4ce3-185">Pareizās versijas atlasīšanai tiek lietota sesijas datuma vērtība.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-185">The session date value is used for proper version selection.</span></span>  

## <a name="restrict-access-to-created-format-from-companies"></a><span data-ttu-id="b4ce3-186">Ierobežot piekļuvi izveidotajam formātam no uzņēmumiem</span><span class="sxs-lookup"><span data-stu-id="b4ce3-186">Restrict access to created format from companies</span></span>
1. <span data-ttu-id="b4ce3-187">Izvērsiet sadaļu ISO valsts/reģiona kodi.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-187">Expand the ISO Country/region codes section.</span></span>
    * <span data-ttu-id="b4ce3-188">Piekļuvi katram formātam var ierobežot, identificējot konkrētas valstis/reģionus, kuros formāts tiek piemērots.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-188">Each format access can be restricted by identifying particular countries/regions in which a format is applicable.</span></span> <span data-ttu-id="b4ce3-189">Ja attiecīgā formāta valstu/reģionu saraksts ir tukšs, tad šo formātu var lietot jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-189">When the list of countries/regions for particular format is empty, this format can be used in any company.</span></span> <span data-ttu-id="b4ce3-190">Ja valstu/reģionu sarakstā ir iekļauti kādi ISO valsts/reģiona kodi, tad šo formātu uzņēmumos var lietot tikai tad, ja uzņēmuma primārā adrese atrodas attiecīgajā valstī/reģionā.</span><span class="sxs-lookup"><span data-stu-id="b4ce3-190">When some ISO country/region codes are inserted in the list of countries/regions, the format can only be use in companies if the primary address is in the country/region.</span></span>  

