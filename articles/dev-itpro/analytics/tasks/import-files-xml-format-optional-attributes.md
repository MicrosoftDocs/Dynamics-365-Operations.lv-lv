---
title: (RCS) Failu importēšana XML formātā ar neobligātiem atribūtiem
description: Šajā tēmā ir sniegta informācija par to, kā lietotājs var izveidot ER formāta konfigurāciju, lai importētu failus XML formātā ar neobligātiem atribūtiem.
author: NickSelin
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1290598d8dbd5b72d679ccf3e642e75b6dc3215
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/04/2019
ms.locfileid: "1727079"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="b78ee-103">(RCS) Failu importēšana XML formātā ar neobligātiem atribūtiem</span><span class="sxs-lookup"><span data-stu-id="b78ee-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b78ee-104">Nākamajās darbībās ir paskaidrots, kā lietotājs ar lomu “Sistēmas administrators” vai “Elektronisko pārskatu izstrādātājs” var izveidot ER formāta konfigurāciju, lai importētu XML formātā tādus failus, kuros ir neobligāti atribūti.</span><span class="sxs-lookup"><span data-stu-id="b78ee-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="b78ee-105">Lai veiktu šīs darbības, vispirms veiciet "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu" procedūras darbības.</span><span class="sxs-lookup"><span data-stu-id="b78ee-105">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="b78ee-106">Pirms sākšanas lejupielādējiet un lokāli saglabājiet failu IncomingDocumentToLearnHowToHandleOptionalAttributes.xml no [Microsoft lejupielādes centra](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="b78ee-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.  <span data-ttu-id="b78ee-107">Dodieties uz **Visas darbvietas** > **Elektroniskie pārskati**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.  <span data-ttu-id="b78ee-108">Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam Litware, Inc. ir pieejams un ir atzīmēts kā **Aktīvs**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="b78ee-109">Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas ir aprakstītas procedūrā [Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="b78ee-109">If you don’t see this configuration provider, complete the steps in the procedure [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.  <span data-ttu-id="b78ee-110">Noklikšķiniet uz **Pārskatu veidošanas konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="b78ee-111">Jaunas datu modeļa konfigurācijas izveide</span><span class="sxs-lookup"><span data-stu-id="b78ee-111">Create a new data model configuration</span></span>
1.  <span data-ttu-id="b78ee-112">Noklikšķiniet uz **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b78ee-112">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="b78ee-113">Laukā **Nosaukums** ierakstiet “Modelis XML faila importēšanai”.</span><span class="sxs-lookup"><span data-stu-id="b78ee-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.  <span data-ttu-id="b78ee-114">Klikšķiniet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-114">Click **Create configuration**.</span></span>
4.  <span data-ttu-id="b78ee-115">Noklikšķiniet uz **Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-115">Click **Designer**.</span></span>
5.  <span data-ttu-id="b78ee-116">Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b78ee-116">Click **New** to open the drop dialog.</span></span>
6.  <span data-ttu-id="b78ee-117">Laukā **Nosaukums** ierakstiet “Sakne”.</span><span class="sxs-lookup"><span data-stu-id="b78ee-117">In the **Name** field, type 'Root'.</span></span>
7.  <span data-ttu-id="b78ee-118">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-118">Click **Add**.</span></span>
8.  <span data-ttu-id="b78ee-119">Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b78ee-119">Click **New** to open the drop dialog.</span></span>
9.  <span data-ttu-id="b78ee-120">Laukā **Nosaukums** ierakstiet “Saraksts”.</span><span class="sxs-lookup"><span data-stu-id="b78ee-120">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="b78ee-121">Laukā **Vienuma veids** atlasiet **Ierakstu saraksts**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-121">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="b78ee-122">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-122">Click **Add**.</span></span>
12. <span data-ttu-id="b78ee-123">Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b78ee-123">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="b78ee-124">Laukā **Nosaukums** ierakstiet “Kods”.</span><span class="sxs-lookup"><span data-stu-id="b78ee-124">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="b78ee-125">Laukā **Vienuma veids** atlasiet **Virkne**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-125">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="b78ee-126">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-126">Click **Add**.</span></span>
16. <span data-ttu-id="b78ee-127">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-127">Click **Save**.</span></span>
17. <span data-ttu-id="b78ee-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b78ee-128">Close the page.</span></span>
18. <span data-ttu-id="b78ee-129">Noklikšķiniet uz **Mainīt statusu**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-129">Click **Change status**.</span></span>
19. <span data-ttu-id="b78ee-130">Noklikšķiniet uz **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-130">Click **Complete**.</span></span>
20. <span data-ttu-id="b78ee-131">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="b78ee-132">Formāta izveidošana datu importēšanai</span><span class="sxs-lookup"><span data-stu-id="b78ee-132">Create a format for data import</span></span>
1.  <span data-ttu-id="b78ee-133">Noklikšķiniet uz **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b78ee-133">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="b78ee-134">Laukā **Jauns** ierakstiet “Formāts balstīts uz datu modeli Modelis XML faila importēšanai”.</span><span class="sxs-lookup"><span data-stu-id="b78ee-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.  <span data-ttu-id="b78ee-135">Laukā **Nosaukums** ierakstiet “Formāts XML faila importēšanai”.</span><span class="sxs-lookup"><span data-stu-id="b78ee-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.  <span data-ttu-id="b78ee-136">Laukā **Atbalsta datu importēšanu** atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-136">Select **Yes** in the **Supports data import** field.</span></span>
5.  <span data-ttu-id="b78ee-137">Klikšķiniet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="b78ee-138">Formāta veidošana ienākoša faila parsēšanai XML formātā</span><span class="sxs-lookup"><span data-stu-id="b78ee-138">Design a format to parse incoming file in xml format</span></span>
1.  <span data-ttu-id="b78ee-139">Noklikšķiniet uz **Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-139">Click **Designer**.</span></span>
2.  <span data-ttu-id="b78ee-140">Noklikšķiniet uz **Pievienot sakni**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b78ee-140">Click **Add root** to open the drop dialog.</span></span>
3.  <span data-ttu-id="b78ee-141">Kokā atlasiet **XML\Elements**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-141">In the tree, select **XML\Element**.</span></span>
4.  <span data-ttu-id="b78ee-142">Laukā **Nosaukums** ierakstiet “root”.</span><span class="sxs-lookup"><span data-stu-id="b78ee-142">In the **Name** field, type 'root'.</span></span>
5.  <span data-ttu-id="b78ee-143">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-143">Click **OK**.</span></span>
6.  <span data-ttu-id="b78ee-144">Noklikšķiniet uz **Pievienot**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b78ee-144">Click **Add** to open the drop dialog.</span></span>
7.  <span data-ttu-id="b78ee-145">Kokā atlasiet **XML\Elements**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-145">In the tree, select **XML\Element**.</span></span>
8.  <span data-ttu-id="b78ee-146">Laukā **Nosaukums** ierakstiet “document”.</span><span class="sxs-lookup"><span data-stu-id="b78ee-146">In the **Name** field, type 'document'.</span></span>
9.  <span data-ttu-id="b78ee-147">Laukā **Daudzkārtīgums** atlasiet **One many**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-147">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="b78ee-148">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-148">Click **OK**.</span></span>
11. <span data-ttu-id="b78ee-149">Koka struktūrā atlasiet **root\document**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-149">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="b78ee-150">Noklikšķiniet uz **Pievienot**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b78ee-150">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="b78ee-151">Kokā atlasiet **XML\Atribūts**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-151">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="b78ee-152">Laukā **Nosaukums** ierakstiet “ID”.</span><span class="sxs-lookup"><span data-stu-id="b78ee-152">In the **Name** field, type 'ID'.</span></span>
15. <span data-ttu-id="b78ee-153">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-153">Click **OK**.</span></span>
16. <span data-ttu-id="b78ee-154">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="b78ee-155">Formāta kartējuma veidošana parsētās informācijas saglabāšanai datu modelī</span><span class="sxs-lookup"><span data-stu-id="b78ee-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="b78ee-156">Noklikšķiniet uz **Kartēt formātu uz modeli**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="b78ee-157">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-157">Click **New**.</span></span>
3. <span data-ttu-id="b78ee-158">Laukā **Definīcija** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b78ee-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="b78ee-159">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b78ee-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="b78ee-160">Laukā **Nosaukums** ierakstiet “Kartēšana”.</span><span class="sxs-lookup"><span data-stu-id="b78ee-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="b78ee-161">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-161">Click **Save**.</span></span>
7. <span data-ttu-id="b78ee-162">Noklikšķiniet uz **Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-162">Click **Designer**.</span></span>
8. <span data-ttu-id="b78ee-163">Koka struktūrā izvērsiet zaru **format**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="b78ee-164">Koka struktūrā izvērsiet zaru **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10. <span data-ttu-id="b78ee-165">Koka struktūrā atlasiet \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="b78ee-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="b78ee-166">(dokuments)\*\*.</span><span class="sxs-lookup"><span data-stu-id="b78ee-166">(document)\*\*.</span></span>
11. <span data-ttu-id="b78ee-167">Noklikšķiniet uz **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-167">Click **Bind**.</span></span>
12. <span data-ttu-id="b78ee-168">Koka struktūrā izvērsiet zaru \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="b78ee-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="b78ee-169">(dokuments)\*\*.</span><span class="sxs-lookup"><span data-stu-id="b78ee-169">(document)\*\*.</span></span>
13. <span data-ttu-id="b78ee-170">Koka struktūrā atlasiet \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="b78ee-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="b78ee-171">(dokuments)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="b78ee-171">(document)\id\*\*.</span></span>
14. <span data-ttu-id="b78ee-172">Koka struktūrā izvērsiet zaru **List = format.root.document**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-172">In the tree, expand **List = format.root.document**.</span></span>
15. <span data-ttu-id="b78ee-173">Koka struktūrā atlasiet zaru **List = format.root.document\Code**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-173">In the tree, select **List = format.root.document\Code**.</span></span>
16. <span data-ttu-id="b78ee-174">Noklikšķiniet uz **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-174">Click **Bind**.</span></span>
17. <span data-ttu-id="b78ee-175">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-175">Click **Save**.</span></span>
18. <span data-ttu-id="b78ee-176">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b78ee-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="b78ee-177">Formāta kartēšanas darbināšana</span><span class="sxs-lookup"><span data-stu-id="b78ee-177">Run format mapping</span></span>
1. <span data-ttu-id="b78ee-178">Noklikšķiniet uz **Palaist**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-178">Click **Run**.</span></span>
2. <span data-ttu-id="b78ee-179">Noklikšķiniet uz **Pārlūkot** un atlasiet **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="b78ee-180">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="b78ee-181">Atlasītais fails nav importēts, jo formāta dizainā tiek pieņemts, ka elementam “document” ir atribūts “id”, bet importētajā failā tāda atribūta nav.</span><span class="sxs-lookup"><span data-stu-id="b78ee-181">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="b78ee-182">Formāta struktūras modificēšana, lai XML atribūtu apstrādātu kā neobligātu</span><span class="sxs-lookup"><span data-stu-id="b78ee-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="b78ee-183">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b78ee-183">Close the page.</span></span>
2. <span data-ttu-id="b78ee-184">Koka struktūrā izvērsiet zaru **root\document**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="b78ee-185">Koka struktūrā atlasiet zaru **root\document\id**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="b78ee-186">Laukā **Tukša virkne trūkstošam atribūtam** atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="b78ee-187">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="b78ee-188">Formāta kartējuma palaišana, lai testētu izmaiņas</span><span class="sxs-lookup"><span data-stu-id="b78ee-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="b78ee-189">Noklikšķiniet uz **Kartēt formātu uz modeli**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="b78ee-190">Noklikšķiniet uz **Palaist**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-190">Click **Run**.</span></span>
3. <span data-ttu-id="b78ee-191">Noklikšķiniet uz **Pārlūkot** un atlasiet failu **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="b78ee-192">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b78ee-192">Click **OK**.</span></span>
5. <span data-ttu-id="b78ee-193">Pārskatiet ģenerēto failu.</span><span class="sxs-lookup"><span data-stu-id="b78ee-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="b78ee-194">Tiek importēts tas pats fails, jo formāta dizainā tiek pieņemts, ka elementam “document” atribūts “id” ir neobligāts.</span><span class="sxs-lookup"><span data-stu-id="b78ee-194">The same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
