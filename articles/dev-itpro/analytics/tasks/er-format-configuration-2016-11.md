--- 
title: "ER Izveidot formāta konfigurāciju (2016. gada novembris)"
description: "Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izveidot formāta konfigurāciju Elektroniskajos pārskatos (ER)."
author: NickSelin
manager: AnnBe
ms.date: 11/27/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f004451a260b5be6c15c3975cd9e63ba9c1a7a2e
ms.openlocfilehash: 6fa5023a29c95ab9f10d8aacd51edc1a06c3c152
ms.contentlocale: lv-lv
ms.lasthandoff: 02/06/2019

---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="6d7c1-103">ER Izveidot formāta konfigurāciju (2016. gada novembris)</span><span class="sxs-lookup"><span data-stu-id="6d7c1-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6d7c1-104">Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izveidot formāta konfigurāciju Elektroniskajos pārskatos (ER).</span><span class="sxs-lookup"><span data-stu-id="6d7c1-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="6d7c1-105">Šī formāta konfigurāciju noteiks to elektronisko dokumentu formātu, kas tiek izmantoti maksājumu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="6d7c1-106">Šajā piemērā jāuzveido parauga uzņēmuma Litware, Inc. formāta konfigurācija. Lai varētu veikt šīs darbības, vispirms jāizpilda procedūrā “Modeļa kartēšana izvēlētajos datu avotos” aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="6d7c1-107">Jaunas formāta konfigurācijas izveide</span><span class="sxs-lookup"><span data-stu-id="6d7c1-107">Create a new format configuration</span></span>
1. <span data-ttu-id="6d7c1-108">Pārejiet uz sadaļu **Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="6d7c1-109">Noklikšķiniet uz **Pārskatu veidošanas konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="6d7c1-110">Kokā atlasiet **Maksājumi (vienkāršotais modelis)**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="6d7c1-111">Noklikšķiniet uz **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="6d7c1-112">Ja neredzat opciju **Izveidot konfigurāciju**, ir jāiespējo noformēšanas režīms lapā **Elektronisko pārskatu veidošanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="6d7c1-113">Laukā **Jauns** ievadiet **Uz datu modeli PaymentModel balstīts formātsl**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="6d7c1-114">Laukā **Nosaukums** ierakstiet **BAKS (UK fiktīvs)**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="6d7c1-115">Laukā **Apraksts** ierakstiet **BAKS kreditora maksājuma formāts (UK fiktīvs)**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="6d7c1-116">Šeit tiek automātiski ievadīts aktīvais konfigurācijas nodrošinātājs.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="6d7c1-117">Šis nodrošinātājs varēs uzturēt šo konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="6d7c1-118">Citi nodrošinātāji var izmantot šo konfigurāciju, bet nevar uzturēt to.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="6d7c1-119">Var definēt noteiktu elektroniskā dokumenta formātu.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="6d7c1-120">Atstājiet šo lauku tukšu, ja vēlaties atlasīt formātu izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="6d7c1-121">Ievadiet vai atlasiet kādu vērtību laukā **Datu modeļa definīcija**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="6d7c1-122">Klikšķiniet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-122">Click **Create configuration**.</span></span> <span data-ttu-id="6d7c1-123">Tika izveidota jauna konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-123">A new configuration has been created.</span></span> <span data-ttu-id="6d7c1-124">Melnraksta versiju var izmantot, lai saglabātu dizaina formātu elektronisko dokumentu pārvaldībai.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

 > [!NOTE]
 > <span data-ttu-id="6d7c1-125">Ja neredzat opciju **Izveidot konfigurāciju**, ir jāiespējo noformēšanas režīms lapā **Elektronisko pārskatu veidošanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-125">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span>


## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="6d7c1-126">Elektroniskā dokumenta formāta noformēšana</span><span class="sxs-lookup"><span data-stu-id="6d7c1-126">Design the format of an electronic document</span></span>
1. <span data-ttu-id="6d7c1-127">Noklikšķiniet uz **Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-127">Click **Designer**.</span></span>
2. <span data-ttu-id="6d7c1-128">Noklikšķiniet uz **Pievienot sakni**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-128">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="6d7c1-129">Kokā atlasiet **Vispārīgi\Fails**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-129">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="6d7c1-130">Laukā **Nosaukums** ierakstiet **Xml**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-130">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="6d7c1-131">Laukā **Kodēšana** ierakstiet **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-131">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="6d7c1-132">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-132">Click **OK**.</span></span>
7. <span data-ttu-id="6d7c1-133">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-133">Click **Add**.</span></span>
8. <span data-ttu-id="6d7c1-134">Kokā atlasiet **XML\Elements**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-134">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="6d7c1-135">Laukā **Nosaukums** ierakstiet **Ziņojums**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-135">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="6d7c1-136">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-136">Click **OK**.</span></span>
11. <span data-ttu-id="6d7c1-137">Kokā atlasiet **Xml\Ziņojums**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-137">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="6d7c1-138">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-138">Click **Add Element**.</span></span>
13. <span data-ttu-id="6d7c1-139">Laukā **Nosaukums** ievadiet **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-139">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="6d7c1-140">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-140">Click **OK**.</span></span>
15. <span data-ttu-id="6d7c1-141">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-141">Click **Add Element**.</span></span>
16. <span data-ttu-id="6d7c1-142">Laukā Nosaukums ierakstiet **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-142">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="6d7c1-143">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-143">Click **OK**.</span></span>
18. <span data-ttu-id="6d7c1-144">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-144">Click **Add Element**.</span></span>
19. <span data-ttu-id="6d7c1-145">Laukā **Nosaukums** ierakstiet **Maksājumi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-145">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="6d7c1-146">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-146">Click **OK**.</span></span>
21. <span data-ttu-id="6d7c1-147">Kokā atlasiet **Xml\Ziņojums\Maksājumi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-147">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="6d7c1-148">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-148">Click **Add Element**.</span></span>
23. <span data-ttu-id="6d7c1-149">Laukā **Nosaukums** ierakstiet **Krājums**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-149">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="6d7c1-150">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-150">Click **OK**.</span></span>
25. <span data-ttu-id="6d7c1-151">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-151">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="6d7c1-152">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-152">Click **Add**.</span></span>
27. <span data-ttu-id="6d7c1-153">Kokā atlasiet **XML\Atribūts**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-153">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="6d7c1-154">Laukā Nosaukums ierakstiet **Id**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-154">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="6d7c1-155">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-155">Click **OK**.</span></span>
30. <span data-ttu-id="6d7c1-156">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-156">Click **Add**.</span></span>
31. <span data-ttu-id="6d7c1-157">Kokā atlasiet **XML\Elements**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-157">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="6d7c1-158">Laukā Nosaukums ierakstiet **Kreditors**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-158">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="6d7c1-159">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-159">Click **OK**.</span></span>
34. <span data-ttu-id="6d7c1-160">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Kreditors**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-160">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="6d7c1-161">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-161">Click **Add Element**.</span></span>
36. <span data-ttu-id="6d7c1-162">Laukā Nosaukums ierakstiet **Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-162">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="6d7c1-163">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-163">Click **OK**.</span></span>
38. <span data-ttu-id="6d7c1-164">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-164">Click **Add Element**.</span></span>
39. <span data-ttu-id="6d7c1-165">Laukā **Nosaukums** ierakstiet **Banka**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-165">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="6d7c1-166">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-166">Click **OK**.</span></span>
41. <span data-ttu-id="6d7c1-167">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-167">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="6d7c1-168">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-168">Click **Add Element**.</span></span>
43. <span data-ttu-id="6d7c1-169">Laukā **Nosaukums** ierakstiet **RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-169">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="6d7c1-170">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-170">Click **OK**.</span></span>
45. <span data-ttu-id="6d7c1-171">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-171">Click **Add Element**.</span></span>
46. <span data-ttu-id="6d7c1-172">Laukā **Nosaukums** ierakstiet **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-172">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="6d7c1-173">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-173">Click **OK**.</span></span>
48. <span data-ttu-id="6d7c1-174">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Kreditors**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-174">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="6d7c1-175">Noklikšķiniet uz **Kopēt**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-175">Click **Copy**.</span></span>
50. <span data-ttu-id="6d7c1-176">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-176">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="6d7c1-177">Noklikšķiniet uz **Ielīmēt**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-177">Click **Paste**.</span></span>
52. <span data-ttu-id="6d7c1-178">Laukā **Nosaukums** ierakstiet **Maksātājs**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-178">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="6d7c1-179">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-179">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="6d7c1-180">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-180">Click **Add Element**.</span></span>
55. <span data-ttu-id="6d7c1-181">Laukā **Nosaukums** ierakstiet **Valūta**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-181">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="6d7c1-182">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-182">Click **OK**.</span></span>
57. <span data-ttu-id="6d7c1-183">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-183">Click **Add Element**.</span></span>
58. <span data-ttu-id="6d7c1-184">Laukā **Nosaukums** ierakstiet **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-184">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="6d7c1-185">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-185">Click **OK**.</span></span>
60. <span data-ttu-id="6d7c1-186">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-186">Click **Add Element**.</span></span>
61. <span data-ttu-id="6d7c1-187">Laukā Nosaukums ierakstiet **TransDate**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-187">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="6d7c1-188">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-188">Click **OK**.</span></span>
63. <span data-ttu-id="6d7c1-189">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-189">Click **Add Element**.</span></span>
64. <span data-ttu-id="6d7c1-190">Laukā Nosaukums ierakstiet **Summa**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-190">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="6d7c1-191">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-191">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="6d7c1-192">Formātā komponentu sagatavošana kartēšanai datu modeļa elementos</span><span class="sxs-lookup"><span data-stu-id="6d7c1-192">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="6d7c1-193">Kokā atlasiet **Xml\Ziņojums\ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-193">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="6d7c1-194">Noklikšķiniet uz **Pievienot**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-194">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="6d7c1-195">Kokā atlasiet **Teksts\DateTime**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-195">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="6d7c1-196">Laukā **Formāts** ierakstiet **gggg-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-196">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="6d7c1-197">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-197">Click **OK**.</span></span>
6. <span data-ttu-id="6d7c1-198">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\TransDate**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-198">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="6d7c1-199">Noklikšķiniet uz **Pievienot DateTime**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-199">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="6d7c1-200">Laukā **Formāts** ierakstiet **gggg-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-200">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="6d7c1-201">Tipa **DateTime** laukā atlasiet **Datums**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-201">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="6d7c1-202">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-202">Click **OK**.</span></span>
11. <span data-ttu-id="6d7c1-203">Kokā atlasiet **Xml\Ziņojums\MessageId**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-203">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="6d7c1-204">Noklikšķiniet uz **Pievienot**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-204">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="6d7c1-205">Kokā atlasiet **Teksts\Virkne**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-205">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="6d7c1-206">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-206">Click **OK**.</span></span>
15. <span data-ttu-id="6d7c1-207">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-207">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="6d7c1-208">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-208">Click **Add String**.</span></span>
17. <span data-ttu-id="6d7c1-209">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-209">Click **OK**.</span></span>
18. <span data-ttu-id="6d7c1-210">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-210">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="6d7c1-211">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-211">Click **Add String**.</span></span>
20. <span data-ttu-id="6d7c1-212">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-212">Click **OK**.</span></span>
21. <span data-ttu-id="6d7c1-213">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-213">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="6d7c1-214">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-214">Click **Add String**.</span></span>
23. <span data-ttu-id="6d7c1-215">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-215">Click **OK**.</span></span>
24. <span data-ttu-id="6d7c1-216">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-216">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="6d7c1-217">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-217">Click **Add String**.</span></span>
26. <span data-ttu-id="6d7c1-218">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-218">Click **OK**.</span></span>
27. <span data-ttu-id="6d7c1-219">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Banka\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-219">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="6d7c1-220">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-220">Click **Add String**.</span></span>
29. <span data-ttu-id="6d7c1-221">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-221">Click **OK**.</span></span>
30. <span data-ttu-id="6d7c1-222">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Banka\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-222">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="6d7c1-223">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-223">Click **Add String**.</span></span>
32. <span data-ttu-id="6d7c1-224">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-224">Click **OK**.</span></span>
33. <span data-ttu-id="6d7c1-225">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Valūta**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-225">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="6d7c1-226">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-226">Click **Add String**.</span></span>
35. <span data-ttu-id="6d7c1-227">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-227">Click **OK**.</span></span>
36. <span data-ttu-id="6d7c1-228">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-228">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="6d7c1-229">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-229">Click **Add String**.</span></span>
38. <span data-ttu-id="6d7c1-230">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-230">Click **OK**.</span></span>
39. <span data-ttu-id="6d7c1-231">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Summa**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-231">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="6d7c1-232">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-232">Click **Add String**.</span></span>
41. <span data-ttu-id="6d7c1-233">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-233">Click **OK**.</span></span>
42. <span data-ttu-id="6d7c1-234">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-234">Click **Save**.</span></span>
43. <span data-ttu-id="6d7c1-235">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6d7c1-235">Close the page.</span></span>


