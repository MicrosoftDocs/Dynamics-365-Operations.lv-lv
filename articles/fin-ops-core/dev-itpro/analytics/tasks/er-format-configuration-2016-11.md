---
title: ER Izveidot formāta konfigurāciju (2016. gada novembris)
description: Šajā tēmā skaidrots, kā izveidot formāta konfigurāciju elektroniskajiem pārskatiem (ER).
author: NickSelin
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8cb86c1486223e982f8cbddc8eadaaf1c8ced4f8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565194"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="d844e-103">ER Izveidot formāta konfigurāciju (2016. gada novembris)</span><span class="sxs-lookup"><span data-stu-id="d844e-103">ER Create a format configuration (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d844e-104">Šajā tēmā ir paskaidrots, kā lietotājs Sistēmas administratora vai Elektronisko pārskatu izstrādātāja lomā var izveidot Elektroniskā pārskata (EK) formāta konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="d844e-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="d844e-105">Šī formāta konfigurāciju noteiks to elektronisko dokumentu formātu, kas tiek izmantoti maksājumu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="d844e-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="d844e-106">Šajā piemērā jāuzveido parauga uzņēmuma Litware, Inc. formāta konfigurācija. Lai varētu veikt šīs darbības, vispirms jāizpilda procedūrā "Modeļa kartēšana izvēlētajos datu avotos" aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="d844e-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the "Map model to selected datasources" procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="d844e-107">Jaunas formāta konfigurācijas izveide</span><span class="sxs-lookup"><span data-stu-id="d844e-107">Create a new format configuration</span></span>
1. <span data-ttu-id="d844e-108">Pārejiet uz sadaļu **Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="d844e-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="d844e-109">Noklikšķiniet uz **Pārskatu veidošanas konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="d844e-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="d844e-110">Kokā atlasiet **Maksājumi (vienkāršotais modelis)**.</span><span class="sxs-lookup"><span data-stu-id="d844e-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="d844e-111">Noklikšķiniet uz **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d844e-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="d844e-112">Ja neredzat opciju **Izveidot konfigurāciju**, ir jāiespējo noformēšanas režīms lapā **Elektronisko pārskatu veidošanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="d844e-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="d844e-113">Laukā **Jauns** ievadiet **Format based on data model PaymentModel**.</span><span class="sxs-lookup"><span data-stu-id="d844e-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="d844e-114">Laukā **Nosaukums** ierakstiet **BAKS (UK fiktīvs)**.</span><span class="sxs-lookup"><span data-stu-id="d844e-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="d844e-115">Laukā **Apraksts** ierakstiet **BAKS kreditora maksājuma formāts (UK fiktīvs)**.</span><span class="sxs-lookup"><span data-stu-id="d844e-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="d844e-116">Šeit tiek automātiski ievadīts aktīvais konfigurācijas nodrošinātājs.</span><span class="sxs-lookup"><span data-stu-id="d844e-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="d844e-117">Šis nodrošinātājs varēs uzturēt šo konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="d844e-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="d844e-118">Citi nodrošinātāji var izmantot šo konfigurāciju, bet nevar uzturēt to.</span><span class="sxs-lookup"><span data-stu-id="d844e-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="d844e-119">Var definēt noteiktu elektroniskā dokumenta formātu.</span><span class="sxs-lookup"><span data-stu-id="d844e-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="d844e-120">Atstājiet šo lauku tukšu, ja vēlaties atlasīt formātu izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="d844e-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="d844e-121">Ievadiet vai atlasiet kādu vērtību laukā **Datu modeļa definīcija**.</span><span class="sxs-lookup"><span data-stu-id="d844e-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="d844e-122">Klikšķiniet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="d844e-122">Click **Create configuration**.</span></span> <span data-ttu-id="d844e-123">Tika izveidota jauna konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="d844e-123">A new configuration has been created.</span></span> <span data-ttu-id="d844e-124">Melnraksta versiju var izmantot, lai saglabātu dizaina formātu elektronisko dokumentu pārvaldībai.</span><span class="sxs-lookup"><span data-stu-id="d844e-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="d844e-125">Elektroniskā dokumenta formāta noformēšana</span><span class="sxs-lookup"><span data-stu-id="d844e-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="d844e-126">Noklikšķiniet uz **Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="d844e-126">Click **Designer**.</span></span>
2. <span data-ttu-id="d844e-127">Noklikšķiniet uz **Pievienot sakni**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d844e-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="d844e-128">Kokā atlasiet **Vispārīgi\Fails**.</span><span class="sxs-lookup"><span data-stu-id="d844e-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="d844e-129">Laukā **Nosaukums** ierakstiet **Xml**.</span><span class="sxs-lookup"><span data-stu-id="d844e-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="d844e-130">Laukā **Kodēšana** ierakstiet **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="d844e-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="d844e-131">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-131">Click **OK**.</span></span>
7. <span data-ttu-id="d844e-132">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="d844e-132">Click **Add**.</span></span>
8. <span data-ttu-id="d844e-133">Kokā atlasiet **XML\Elements**.</span><span class="sxs-lookup"><span data-stu-id="d844e-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="d844e-134">Laukā **Nosaukums** ierakstiet **Ziņojums**.</span><span class="sxs-lookup"><span data-stu-id="d844e-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="d844e-135">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-135">Click **OK**.</span></span>
11. <span data-ttu-id="d844e-136">Kokā atlasiet **Xml\Ziņojums**.</span><span class="sxs-lookup"><span data-stu-id="d844e-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="d844e-137">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="d844e-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="d844e-138">Laukā **Nosaukums** ievadiet **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="d844e-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="d844e-139">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-139">Click **OK**.</span></span>
15. <span data-ttu-id="d844e-140">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="d844e-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="d844e-141">Laukā Nosaukums ierakstiet **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="d844e-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="d844e-142">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-142">Click **OK**.</span></span>
18. <span data-ttu-id="d844e-143">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="d844e-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="d844e-144">Laukā **Nosaukums** ierakstiet **Maksājumi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="d844e-145">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-145">Click **OK**.</span></span>
21. <span data-ttu-id="d844e-146">Kokā atlasiet **Xml\Ziņojums\Maksājumi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="d844e-147">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="d844e-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="d844e-148">Laukā **Nosaukums** ierakstiet **Krājums**.</span><span class="sxs-lookup"><span data-stu-id="d844e-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="d844e-149">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-149">Click **OK**.</span></span>
25. <span data-ttu-id="d844e-150">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums**.</span><span class="sxs-lookup"><span data-stu-id="d844e-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="d844e-151">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="d844e-151">Click **Add**.</span></span>
27. <span data-ttu-id="d844e-152">Kokā atlasiet **XML\Atribūts**.</span><span class="sxs-lookup"><span data-stu-id="d844e-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="d844e-153">Laukā Nosaukums ierakstiet **Id**.</span><span class="sxs-lookup"><span data-stu-id="d844e-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="d844e-154">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-154">Click **OK**.</span></span>
30. <span data-ttu-id="d844e-155">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="d844e-155">Click **Add**.</span></span>
31. <span data-ttu-id="d844e-156">Kokā atlasiet **XML\Elements**.</span><span class="sxs-lookup"><span data-stu-id="d844e-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="d844e-157">Laukā Nosaukums ierakstiet **Kreditors**.</span><span class="sxs-lookup"><span data-stu-id="d844e-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="d844e-158">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-158">Click **OK**.</span></span>
34. <span data-ttu-id="d844e-159">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Kreditors**.</span><span class="sxs-lookup"><span data-stu-id="d844e-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="d844e-160">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="d844e-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="d844e-161">Laukā Nosaukums ierakstiet **Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="d844e-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="d844e-162">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-162">Click **OK**.</span></span>
38. <span data-ttu-id="d844e-163">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="d844e-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="d844e-164">Laukā **Nosaukums** ierakstiet **Banka**.</span><span class="sxs-lookup"><span data-stu-id="d844e-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="d844e-165">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-165">Click **OK**.</span></span>
41. <span data-ttu-id="d844e-166">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka**.</span><span class="sxs-lookup"><span data-stu-id="d844e-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="d844e-167">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="d844e-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="d844e-168">Laukā **Nosaukums** ierakstiet **RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="d844e-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="d844e-169">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-169">Click **OK**.</span></span>
45. <span data-ttu-id="d844e-170">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="d844e-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="d844e-171">Laukā **Nosaukums** ierakstiet **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="d844e-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="d844e-172">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-172">Click **OK**.</span></span>
48. <span data-ttu-id="d844e-173">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Kreditors**.</span><span class="sxs-lookup"><span data-stu-id="d844e-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="d844e-174">Noklikšķiniet uz **Kopēt**.</span><span class="sxs-lookup"><span data-stu-id="d844e-174">Click **Copy**.</span></span>
50. <span data-ttu-id="d844e-175">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums**.</span><span class="sxs-lookup"><span data-stu-id="d844e-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="d844e-176">Noklikšķiniet uz **Ielīmēt**.</span><span class="sxs-lookup"><span data-stu-id="d844e-176">Click **Paste**.</span></span>
52. <span data-ttu-id="d844e-177">Laukā **Nosaukums** ierakstiet **Maksātājs**.</span><span class="sxs-lookup"><span data-stu-id="d844e-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="d844e-178">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums**.</span><span class="sxs-lookup"><span data-stu-id="d844e-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="d844e-179">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="d844e-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="d844e-180">Laukā **Nosaukums** ierakstiet **Valūta**.</span><span class="sxs-lookup"><span data-stu-id="d844e-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="d844e-181">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-181">Click **OK**.</span></span>
57. <span data-ttu-id="d844e-182">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="d844e-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="d844e-183">Laukā **Nosaukums** ierakstiet **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="d844e-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="d844e-184">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-184">Click **OK**.</span></span>
60. <span data-ttu-id="d844e-185">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="d844e-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="d844e-186">Laukā Nosaukums ierakstiet **TransDate**.</span><span class="sxs-lookup"><span data-stu-id="d844e-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="d844e-187">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-187">Click **OK**.</span></span>
63. <span data-ttu-id="d844e-188">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="d844e-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="d844e-189">Laukā Nosaukums ierakstiet **Summa**.</span><span class="sxs-lookup"><span data-stu-id="d844e-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="d844e-190">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="d844e-191">Formātā komponentu sagatavošana kartēšanai datu modeļa elementos</span><span class="sxs-lookup"><span data-stu-id="d844e-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="d844e-192">Kokā atlasiet **Xml\Ziņojums\ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="d844e-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="d844e-193">Noklikšķiniet uz **Pievienot**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d844e-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="d844e-194">Kokā atlasiet **Teksts\DateTime**.</span><span class="sxs-lookup"><span data-stu-id="d844e-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="d844e-195">Laukā **Formāts** ierakstiet **gggg-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="d844e-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="d844e-196">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-196">Click **OK**.</span></span>
6. <span data-ttu-id="d844e-197">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\TransDate**.</span><span class="sxs-lookup"><span data-stu-id="d844e-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="d844e-198">Noklikšķiniet uz **Pievienot DateTime**.</span><span class="sxs-lookup"><span data-stu-id="d844e-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="d844e-199">Laukā **Formāts** ierakstiet **gggg-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="d844e-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="d844e-200">Tipa **DateTime** laukā atlasiet **Datums**.</span><span class="sxs-lookup"><span data-stu-id="d844e-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="d844e-201">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-201">Click **OK**.</span></span>
11. <span data-ttu-id="d844e-202">Kokā atlasiet **Xml\Ziņojums\MessageId**.</span><span class="sxs-lookup"><span data-stu-id="d844e-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="d844e-203">Noklikšķiniet uz **Pievienot**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d844e-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="d844e-204">Kokā atlasiet **Teksts\Virkne**.</span><span class="sxs-lookup"><span data-stu-id="d844e-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="d844e-205">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-205">Click **OK**.</span></span>
15. <span data-ttu-id="d844e-206">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="d844e-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="d844e-207">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="d844e-207">Click **Add String**.</span></span>
17. <span data-ttu-id="d844e-208">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-208">Click **OK**.</span></span>
18. <span data-ttu-id="d844e-209">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="d844e-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="d844e-210">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="d844e-210">Click **Add String**.</span></span>
20. <span data-ttu-id="d844e-211">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-211">Click **OK**.</span></span>
21. <span data-ttu-id="d844e-212">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="d844e-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="d844e-213">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="d844e-213">Click **Add String**.</span></span>
23. <span data-ttu-id="d844e-214">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-214">Click **OK**.</span></span>
24. <span data-ttu-id="d844e-215">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="d844e-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="d844e-216">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="d844e-216">Click **Add String**.</span></span>
26. <span data-ttu-id="d844e-217">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-217">Click **OK**.</span></span>
27. <span data-ttu-id="d844e-218">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Banka\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="d844e-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="d844e-219">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="d844e-219">Click **Add String**.</span></span>
29. <span data-ttu-id="d844e-220">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-220">Click **OK**.</span></span>
30. <span data-ttu-id="d844e-221">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Banka\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="d844e-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="d844e-222">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="d844e-222">Click **Add String**.</span></span>
32. <span data-ttu-id="d844e-223">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-223">Click **OK**.</span></span>
33. <span data-ttu-id="d844e-224">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Valūta**.</span><span class="sxs-lookup"><span data-stu-id="d844e-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="d844e-225">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="d844e-225">Click **Add String**.</span></span>
35. <span data-ttu-id="d844e-226">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-226">Click **OK**.</span></span>
36. <span data-ttu-id="d844e-227">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="d844e-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="d844e-228">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="d844e-228">Click **Add String**.</span></span>
38. <span data-ttu-id="d844e-229">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-229">Click **OK**.</span></span>
39. <span data-ttu-id="d844e-230">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Summa**.</span><span class="sxs-lookup"><span data-stu-id="d844e-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="d844e-231">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="d844e-231">Click **Add String**.</span></span>
41. <span data-ttu-id="d844e-232">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d844e-232">Click **OK**.</span></span>
42. <span data-ttu-id="d844e-233">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d844e-233">Click **Save**.</span></span>
43. <span data-ttu-id="d844e-234">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d844e-234">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]