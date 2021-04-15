---
title: ER Izveidot formāta konfigurāciju (2016. gada novembris)
description: Šajā tēmā skaidrots, kā izveidot formāta konfigurāciju elektroniskajiem pārskatiem (ER).
author: NickSelin
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
ms.openlocfilehash: 46686b9e4f6197f565a324a9d03cbb695b6a933b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749073"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="7aeee-103">ER Izveidot formāta konfigurāciju (2016. gada novembris)</span><span class="sxs-lookup"><span data-stu-id="7aeee-103">ER Create a format configuration (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7aeee-104">Šajā tēmā ir paskaidrots, kā lietotājs Sistēmas administratora vai Elektronisko pārskatu izstrādātāja lomā var izveidot Elektroniskā pārskata (EK) formāta konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="7aeee-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="7aeee-105">Šī formāta konfigurāciju noteiks to elektronisko dokumentu formātu, kas tiek izmantoti maksājumu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="7aeee-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="7aeee-106">Šajā piemērā jāuzveido parauga uzņēmuma Litware, Inc. formāta konfigurācija. Lai varētu veikt šīs darbības, vispirms jāizpilda procedūrā "Modeļa kartēšana izvēlētajos datu avotos" aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="7aeee-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the "Map model to selected datasources" procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="7aeee-107">Jaunas formāta konfigurācijas izveide</span><span class="sxs-lookup"><span data-stu-id="7aeee-107">Create a new format configuration</span></span>
1. <span data-ttu-id="7aeee-108">Pārejiet uz sadaļu **Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="7aeee-109">Noklikšķiniet uz **Pārskatu veidošanas konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="7aeee-110">Kokā atlasiet **Maksājumi (vienkāršotais modelis)**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="7aeee-111">Noklikšķiniet uz **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="7aeee-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="7aeee-112">Ja neredzat opciju **Izveidot konfigurāciju**, ir jāiespējo noformēšanas režīms lapā **Elektronisko pārskatu veidošanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="7aeee-113">Laukā **Jauns** ievadiet **Format based on data model PaymentModel**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="7aeee-114">Laukā **Nosaukums** ierakstiet **BAKS (UK fiktīvs)**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="7aeee-115">Laukā **Apraksts** ierakstiet **BAKS kreditora maksājuma formāts (UK fiktīvs)**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="7aeee-116">Šeit tiek automātiski ievadīts aktīvais konfigurācijas nodrošinātājs.</span><span class="sxs-lookup"><span data-stu-id="7aeee-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="7aeee-117">Šis nodrošinātājs varēs uzturēt šo konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="7aeee-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="7aeee-118">Citi nodrošinātāji var izmantot šo konfigurāciju, bet nevar uzturēt to.</span><span class="sxs-lookup"><span data-stu-id="7aeee-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="7aeee-119">Var definēt noteiktu elektroniskā dokumenta formātu.</span><span class="sxs-lookup"><span data-stu-id="7aeee-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="7aeee-120">Atstājiet šo lauku tukšu, ja vēlaties atlasīt formātu izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="7aeee-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="7aeee-121">Ievadiet vai atlasiet kādu vērtību laukā **Datu modeļa definīcija**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="7aeee-122">Klikšķiniet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-122">Click **Create configuration**.</span></span> <span data-ttu-id="7aeee-123">Tika izveidota jauna konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="7aeee-123">A new configuration has been created.</span></span> <span data-ttu-id="7aeee-124">Melnraksta versiju var izmantot, lai saglabātu dizaina formātu elektronisko dokumentu pārvaldībai.</span><span class="sxs-lookup"><span data-stu-id="7aeee-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="7aeee-125">Elektroniskā dokumenta formāta noformēšana</span><span class="sxs-lookup"><span data-stu-id="7aeee-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="7aeee-126">Noklikšķiniet uz **Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-126">Click **Designer**.</span></span>
2. <span data-ttu-id="7aeee-127">Noklikšķiniet uz **Pievienot sakni**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="7aeee-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="7aeee-128">Kokā atlasiet **Vispārīgi\Fails**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="7aeee-129">Laukā **Nosaukums** ierakstiet **Xml**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="7aeee-130">Laukā **Kodēšana** ierakstiet **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="7aeee-131">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-131">Click **OK**.</span></span>
7. <span data-ttu-id="7aeee-132">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-132">Click **Add**.</span></span>
8. <span data-ttu-id="7aeee-133">Kokā atlasiet **XML\Elements**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="7aeee-134">Laukā **Nosaukums** ierakstiet **Ziņojums**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="7aeee-135">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-135">Click **OK**.</span></span>
11. <span data-ttu-id="7aeee-136">Kokā atlasiet **Xml\Ziņojums**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="7aeee-137">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="7aeee-138">Laukā **Nosaukums** ievadiet **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="7aeee-139">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-139">Click **OK**.</span></span>
15. <span data-ttu-id="7aeee-140">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="7aeee-141">Laukā Nosaukums ierakstiet **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="7aeee-142">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-142">Click **OK**.</span></span>
18. <span data-ttu-id="7aeee-143">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="7aeee-144">Laukā **Nosaukums** ierakstiet **Maksājumi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="7aeee-145">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-145">Click **OK**.</span></span>
21. <span data-ttu-id="7aeee-146">Kokā atlasiet **Xml\Ziņojums\Maksājumi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="7aeee-147">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="7aeee-148">Laukā **Nosaukums** ierakstiet **Krājums**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="7aeee-149">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-149">Click **OK**.</span></span>
25. <span data-ttu-id="7aeee-150">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="7aeee-151">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-151">Click **Add**.</span></span>
27. <span data-ttu-id="7aeee-152">Kokā atlasiet **XML\Atribūts**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="7aeee-153">Laukā Nosaukums ierakstiet **Id**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="7aeee-154">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-154">Click **OK**.</span></span>
30. <span data-ttu-id="7aeee-155">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-155">Click **Add**.</span></span>
31. <span data-ttu-id="7aeee-156">Kokā atlasiet **XML\Elements**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="7aeee-157">Laukā Nosaukums ierakstiet **Kreditors**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="7aeee-158">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-158">Click **OK**.</span></span>
34. <span data-ttu-id="7aeee-159">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Kreditors**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="7aeee-160">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="7aeee-161">Laukā Nosaukums ierakstiet **Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="7aeee-162">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-162">Click **OK**.</span></span>
38. <span data-ttu-id="7aeee-163">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="7aeee-164">Laukā **Nosaukums** ierakstiet **Banka**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="7aeee-165">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-165">Click **OK**.</span></span>
41. <span data-ttu-id="7aeee-166">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="7aeee-167">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="7aeee-168">Laukā **Nosaukums** ierakstiet **RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="7aeee-169">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-169">Click **OK**.</span></span>
45. <span data-ttu-id="7aeee-170">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="7aeee-171">Laukā **Nosaukums** ierakstiet **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="7aeee-172">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-172">Click **OK**.</span></span>
48. <span data-ttu-id="7aeee-173">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Kreditors**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="7aeee-174">Noklikšķiniet uz **Kopēt**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-174">Click **Copy**.</span></span>
50. <span data-ttu-id="7aeee-175">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="7aeee-176">Noklikšķiniet uz **Ielīmēt**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-176">Click **Paste**.</span></span>
52. <span data-ttu-id="7aeee-177">Laukā **Nosaukums** ierakstiet **Maksātājs**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="7aeee-178">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="7aeee-179">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="7aeee-180">Laukā **Nosaukums** ierakstiet **Valūta**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="7aeee-181">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-181">Click **OK**.</span></span>
57. <span data-ttu-id="7aeee-182">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="7aeee-183">Laukā **Nosaukums** ierakstiet **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="7aeee-184">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-184">Click **OK**.</span></span>
60. <span data-ttu-id="7aeee-185">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="7aeee-186">Laukā Nosaukums ierakstiet **TransDate**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="7aeee-187">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-187">Click **OK**.</span></span>
63. <span data-ttu-id="7aeee-188">Noklikšķiniet uz **Pievienot elementu**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="7aeee-189">Laukā Nosaukums ierakstiet **Summa**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="7aeee-190">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="7aeee-191">Formātā komponentu sagatavošana kartēšanai datu modeļa elementos</span><span class="sxs-lookup"><span data-stu-id="7aeee-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="7aeee-192">Kokā atlasiet **Xml\Ziņojums\ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="7aeee-193">Noklikšķiniet uz **Pievienot**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="7aeee-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="7aeee-194">Kokā atlasiet **Teksts\DateTime**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="7aeee-195">Laukā **Formāts** ierakstiet **gggg-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="7aeee-196">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-196">Click **OK**.</span></span>
6. <span data-ttu-id="7aeee-197">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\TransDate**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="7aeee-198">Noklikšķiniet uz **Pievienot DateTime**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="7aeee-199">Laukā **Formāts** ierakstiet **gggg-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="7aeee-200">Tipa **DateTime** laukā atlasiet **Datums**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="7aeee-201">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-201">Click **OK**.</span></span>
11. <span data-ttu-id="7aeee-202">Kokā atlasiet **Xml\Ziņojums\MessageId**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="7aeee-203">Noklikšķiniet uz **Pievienot**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="7aeee-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="7aeee-204">Kokā atlasiet **Teksts\Virkne**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="7aeee-205">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-205">Click **OK**.</span></span>
15. <span data-ttu-id="7aeee-206">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="7aeee-207">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-207">Click **Add String**.</span></span>
17. <span data-ttu-id="7aeee-208">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-208">Click **OK**.</span></span>
18. <span data-ttu-id="7aeee-209">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="7aeee-210">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-210">Click **Add String**.</span></span>
20. <span data-ttu-id="7aeee-211">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-211">Click **OK**.</span></span>
21. <span data-ttu-id="7aeee-212">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="7aeee-213">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-213">Click **Add String**.</span></span>
23. <span data-ttu-id="7aeee-214">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-214">Click **OK**.</span></span>
24. <span data-ttu-id="7aeee-215">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="7aeee-216">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-216">Click **Add String**.</span></span>
26. <span data-ttu-id="7aeee-217">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-217">Click **OK**.</span></span>
27. <span data-ttu-id="7aeee-218">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Banka\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="7aeee-219">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-219">Click **Add String**.</span></span>
29. <span data-ttu-id="7aeee-220">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-220">Click **OK**.</span></span>
30. <span data-ttu-id="7aeee-221">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Banka\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="7aeee-222">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-222">Click **Add String**.</span></span>
32. <span data-ttu-id="7aeee-223">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-223">Click **OK**.</span></span>
33. <span data-ttu-id="7aeee-224">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Valūta**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="7aeee-225">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-225">Click **Add String**.</span></span>
35. <span data-ttu-id="7aeee-226">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-226">Click **OK**.</span></span>
36. <span data-ttu-id="7aeee-227">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="7aeee-228">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-228">Click **Add String**.</span></span>
38. <span data-ttu-id="7aeee-229">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-229">Click **OK**.</span></span>
39. <span data-ttu-id="7aeee-230">Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Summa**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="7aeee-231">Noklikšķiniet uz **Pievienot virkni**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-231">Click **Add String**.</span></span>
41. <span data-ttu-id="7aeee-232">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-232">Click **OK**.</span></span>
42. <span data-ttu-id="7aeee-233">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="7aeee-233">Click **Save**.</span></span>
43. <span data-ttu-id="7aeee-234">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7aeee-234">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]