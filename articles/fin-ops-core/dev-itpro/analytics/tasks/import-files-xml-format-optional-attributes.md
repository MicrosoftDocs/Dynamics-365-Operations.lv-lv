---
title: (RCS) Failu importēšana XML formātā ar neobligātiem atribūtiem
description: Šajā tēmā ir sniegta informācija par to, kā lietotājs var izveidot ER formāta konfigurāciju, lai importētu failus XML formātā ar neobligātiem atribūtiem.
author: NickSelin
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 25ced72bc1bb1b18996c8bab986270fde0557ed3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744871"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="95d35-103">(RCS) Failu importēšana XML formātā ar neobligātiem atribūtiem</span><span class="sxs-lookup"><span data-stu-id="95d35-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="95d35-104">Nākamajās darbībās ir paskaidrots, kā lietotājs ar lomu “Sistēmas administrators” vai “Elektronisko pārskatu izstrādātājs” var izveidot ER formāta konfigurāciju, lai importētu XML formātā tādus failus, kuros ir neobligāti atribūti.</span><span class="sxs-lookup"><span data-stu-id="95d35-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="95d35-105">Lai izpildītu tālāk norādītās darbības, vispirms izpildiet darbības, kas aprakstītas procedūrā "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu".</span><span class="sxs-lookup"><span data-stu-id="95d35-105">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span> <span data-ttu-id="95d35-106">Pirms sākšanas lejupielādējiet un lokāli saglabājiet failu IncomingDocumentToLearnHowToHandleOptionalAttributes.xml no [Microsoft lejupielādes centra](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="95d35-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.    <span data-ttu-id="95d35-107">Dodieties uz **Visas darbvietas** > **Elektroniskie pārskati**.</span><span class="sxs-lookup"><span data-stu-id="95d35-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.    <span data-ttu-id="95d35-108">Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam Litware, Inc. ir pieejams un ir atzīmēts kā **Aktīvs**.</span><span class="sxs-lookup"><span data-stu-id="95d35-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="95d35-109">Ja neredzat šo konfigurācijas nodrošinātāju, izpildiet darbības, kas ir aprakstītas procedūrā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="95d35-109">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.    <span data-ttu-id="95d35-110">Noklikšķiniet uz **Pārskatu veidošanas konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="95d35-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="95d35-111">Jaunas datu modeļa konfigurācijas izveide</span><span class="sxs-lookup"><span data-stu-id="95d35-111">Create a new data model configuration</span></span>
1.    <span data-ttu-id="95d35-112">Noklikšķiniet uz **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="95d35-112">Click **Create configuration** to open the drop dialog.</span></span>
2.    <span data-ttu-id="95d35-113">Laukā **Nosaukums** ierakstiet “Modelis XML faila importēšanai”.</span><span class="sxs-lookup"><span data-stu-id="95d35-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.    <span data-ttu-id="95d35-114">Klikšķiniet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="95d35-114">Click **Create configuration**.</span></span>
4.    <span data-ttu-id="95d35-115">Noklikšķiniet uz **Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="95d35-115">Click **Designer**.</span></span>
5.    <span data-ttu-id="95d35-116">Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="95d35-116">Click **New** to open the drop dialog.</span></span>
6.    <span data-ttu-id="95d35-117">Laukā **Nosaukums** ierakstiet “Sakne”.</span><span class="sxs-lookup"><span data-stu-id="95d35-117">In the **Name** field, type 'Root'.</span></span>
7.    <span data-ttu-id="95d35-118">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="95d35-118">Click **Add**.</span></span>
8.    <span data-ttu-id="95d35-119">Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="95d35-119">Click **New** to open the drop dialog.</span></span>
9.    <span data-ttu-id="95d35-120">Laukā **Nosaukums** ierakstiet “Saraksts”.</span><span class="sxs-lookup"><span data-stu-id="95d35-120">In the **Name** field, type 'List'.</span></span>
10.    <span data-ttu-id="95d35-121">Laukā **Vienuma veids** atlasiet **Ierakstu saraksts**.</span><span class="sxs-lookup"><span data-stu-id="95d35-121">In the **Item type** field, select **Record list**.</span></span>
11.    <span data-ttu-id="95d35-122">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="95d35-122">Click **Add**.</span></span>
12.    <span data-ttu-id="95d35-123">Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="95d35-123">Click **New** to open the drop dialog.</span></span>
13.    <span data-ttu-id="95d35-124">Laukā **Nosaukums** ierakstiet “Kods”.</span><span class="sxs-lookup"><span data-stu-id="95d35-124">In the **Name** field, type 'Code'.</span></span>
14.    <span data-ttu-id="95d35-125">Laukā **Vienuma veids** atlasiet **Virkne**.</span><span class="sxs-lookup"><span data-stu-id="95d35-125">In the **Item type** field, select **String**.</span></span>
15.    <span data-ttu-id="95d35-126">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="95d35-126">Click **Add**.</span></span>
16.    <span data-ttu-id="95d35-127">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="95d35-127">Click **Save**.</span></span>
17.    <span data-ttu-id="95d35-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="95d35-128">Close the page.</span></span>
18.    <span data-ttu-id="95d35-129">Noklikšķiniet uz **Mainīt statusu**.</span><span class="sxs-lookup"><span data-stu-id="95d35-129">Click **Change status**.</span></span>
19.    <span data-ttu-id="95d35-130">Noklikšķiniet uz **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="95d35-130">Click **Complete**.</span></span>
20.    <span data-ttu-id="95d35-131">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="95d35-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="95d35-132">Formāta izveidošana datu importēšanai</span><span class="sxs-lookup"><span data-stu-id="95d35-132">Create a format for data import</span></span>
1.    <span data-ttu-id="95d35-133">Noklikšķiniet uz **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="95d35-133">Click **Create configuration** to open the drop dialog.</span></span>
2.    <span data-ttu-id="95d35-134">Laukā **Jauns** ierakstiet “Formāts balstīts uz datu modeli Modelis XML faila importēšanai”.</span><span class="sxs-lookup"><span data-stu-id="95d35-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.    <span data-ttu-id="95d35-135">Laukā **Nosaukums** ierakstiet “Formāts XML faila importēšanai”.</span><span class="sxs-lookup"><span data-stu-id="95d35-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.    <span data-ttu-id="95d35-136">Laukā **Atbalsta datu importēšanu** atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="95d35-136">Select **Yes** in the **Supports data import** field.</span></span>
5.    <span data-ttu-id="95d35-137">Klikšķiniet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="95d35-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="95d35-138">Formāta veidošana ienākoša faila parsēšanai XML formātā</span><span class="sxs-lookup"><span data-stu-id="95d35-138">Design a format to parse incoming file in xml format</span></span>
1.    <span data-ttu-id="95d35-139">Noklikšķiniet uz **Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="95d35-139">Click **Designer**.</span></span>
2.    <span data-ttu-id="95d35-140">Noklikšķiniet uz **Pievienot sakni**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="95d35-140">Click **Add root** to open the drop dialog.</span></span>
3.    <span data-ttu-id="95d35-141">Kokā atlasiet **XML\Elements**.</span><span class="sxs-lookup"><span data-stu-id="95d35-141">In the tree, select **XML\Element**.</span></span>
4.    <span data-ttu-id="95d35-142">Laukā **Nosaukums** ierakstiet “root”.</span><span class="sxs-lookup"><span data-stu-id="95d35-142">In the **Name** field, type 'root'.</span></span>
5.    <span data-ttu-id="95d35-143">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="95d35-143">Click **OK**.</span></span>
6.    <span data-ttu-id="95d35-144">Noklikšķiniet uz **Pievienot**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="95d35-144">Click **Add** to open the drop dialog.</span></span>
7.    <span data-ttu-id="95d35-145">Kokā atlasiet **XML\Elements**.</span><span class="sxs-lookup"><span data-stu-id="95d35-145">In the tree, select **XML\Element**.</span></span>
8.    <span data-ttu-id="95d35-146">Laukā **Nosaukums** ierakstiet “document”.</span><span class="sxs-lookup"><span data-stu-id="95d35-146">In the **Name** field, type 'document'.</span></span>
9.    <span data-ttu-id="95d35-147">Laukā **Daudzkārtīgums** atlasiet **One many**.</span><span class="sxs-lookup"><span data-stu-id="95d35-147">In the **Multiplicity** field, select **One many**.</span></span>
10.    <span data-ttu-id="95d35-148">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="95d35-148">Click **OK**.</span></span>
11.    <span data-ttu-id="95d35-149">Koka struktūrā atlasiet **root\document**.</span><span class="sxs-lookup"><span data-stu-id="95d35-149">In the tree, select **root\document**.</span></span>
12.    <span data-ttu-id="95d35-150">Noklikšķiniet uz **Pievienot**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="95d35-150">Click **Add** to open the drop dialog.</span></span>
13.    <span data-ttu-id="95d35-151">Kokā atlasiet **XML\Atribūts**.</span><span class="sxs-lookup"><span data-stu-id="95d35-151">In the tree, select **XML\Attribute**.</span></span>
14.    <span data-ttu-id="95d35-152">Laukā **Nosaukums** ierakstiet “ID”.</span><span class="sxs-lookup"><span data-stu-id="95d35-152">In the **Name** field, type 'ID'.</span></span>
15.    <span data-ttu-id="95d35-153">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="95d35-153">Click **OK**.</span></span>
16.    <span data-ttu-id="95d35-154">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="95d35-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="95d35-155">Formāta kartējuma veidošana parsētās informācijas saglabāšanai datu modelī</span><span class="sxs-lookup"><span data-stu-id="95d35-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="95d35-156">Noklikšķiniet uz **Kartēt formātu uz modeli**.</span><span class="sxs-lookup"><span data-stu-id="95d35-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="95d35-157">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="95d35-157">Click **New**.</span></span>
3. <span data-ttu-id="95d35-158">Laukā **Definīcija** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="95d35-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="95d35-159">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="95d35-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="95d35-160">Laukā **Nosaukums** ierakstiet “Kartēšana”.</span><span class="sxs-lookup"><span data-stu-id="95d35-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="95d35-161">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="95d35-161">Click **Save**.</span></span>
7. <span data-ttu-id="95d35-162">Noklikšķiniet uz **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="95d35-162">Click **Designer**.</span></span>
8. <span data-ttu-id="95d35-163">Koka struktūrā izvērsiet zaru **format**.</span><span class="sxs-lookup"><span data-stu-id="95d35-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="95d35-164">Koka struktūrā izvērsiet zaru **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="95d35-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10.    <span data-ttu-id="95d35-165">Koka struktūrā atlasiet \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="95d35-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="95d35-166">(dokuments)\*\*.</span><span class="sxs-lookup"><span data-stu-id="95d35-166">(document)\*\*.</span></span>
11.    <span data-ttu-id="95d35-167">Noklikšķiniet uz **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="95d35-167">Click **Bind**.</span></span>
12.    <span data-ttu-id="95d35-168">Koka struktūrā izvērsiet zaru \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="95d35-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="95d35-169">(dokuments)\*\*.</span><span class="sxs-lookup"><span data-stu-id="95d35-169">(document)\*\*.</span></span>
13.    <span data-ttu-id="95d35-170">Koka struktūrā atlasiet \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="95d35-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="95d35-171">(dokuments)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="95d35-171">(document)\id\*\*.</span></span>
14.    <span data-ttu-id="95d35-172">Koka struktūrā izvērsiet zaru **List = format.root.document**.</span><span class="sxs-lookup"><span data-stu-id="95d35-172">In the tree, expand **List = format.root.document**.</span></span>
15.    <span data-ttu-id="95d35-173">Koka struktūrā atlasiet zaru **List = format.root.document\Code**.</span><span class="sxs-lookup"><span data-stu-id="95d35-173">In the tree, select **List = format.root.document\Code**.</span></span>
16.    <span data-ttu-id="95d35-174">Noklikšķiniet uz **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="95d35-174">Click **Bind**.</span></span>
17.    <span data-ttu-id="95d35-175">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="95d35-175">Click **Save**.</span></span>
18.    <span data-ttu-id="95d35-176">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="95d35-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="95d35-177">Formāta kartēšanas darbināšana</span><span class="sxs-lookup"><span data-stu-id="95d35-177">Run format mapping</span></span>
1. <span data-ttu-id="95d35-178">Noklikšķiniet uz **Palaist**.</span><span class="sxs-lookup"><span data-stu-id="95d35-178">Click **Run**.</span></span>
2. <span data-ttu-id="95d35-179">Noklikšķiniet uz **Pārlūkot** un atlasiet **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="95d35-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="95d35-180">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="95d35-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="95d35-181">Atlasītais fails nav importēts, jo formāta dizainā tiek pieņemts, ka elementam “document” ir atribūts “id”, bet importētajā failā tāda atribūta nav.</span><span class="sxs-lookup"><span data-stu-id="95d35-181">The selected file has not been imported as the format design assumes the existence of 'id' attribute for the 'document' element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="95d35-182">Formāta struktūras modificēšana, lai XML atribūtu apstrādātu kā neobligātu</span><span class="sxs-lookup"><span data-stu-id="95d35-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="95d35-183">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="95d35-183">Close the page.</span></span>
2. <span data-ttu-id="95d35-184">Koka struktūrā izvērsiet zaru **root\document**.</span><span class="sxs-lookup"><span data-stu-id="95d35-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="95d35-185">Koka struktūrā atlasiet zaru **root\document\id**.</span><span class="sxs-lookup"><span data-stu-id="95d35-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="95d35-186">Laukā **Tukša virkne trūkstošam atribūtam** atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="95d35-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="95d35-187">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="95d35-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="95d35-188">Formāta kartējuma palaišana, lai testētu izmaiņas</span><span class="sxs-lookup"><span data-stu-id="95d35-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="95d35-189">Noklikšķiniet uz **Kartēt formātu uz modeli**.</span><span class="sxs-lookup"><span data-stu-id="95d35-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="95d35-190">Noklikšķiniet uz **Palaist**.</span><span class="sxs-lookup"><span data-stu-id="95d35-190">Click **Run**.</span></span>
3. <span data-ttu-id="95d35-191">Noklikšķiniet uz **Pārlūkot** un atlasiet failu **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="95d35-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="95d35-192">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="95d35-192">Click **OK**.</span></span>
5. <span data-ttu-id="95d35-193">Pārskatiet ģenerēto failu.</span><span class="sxs-lookup"><span data-stu-id="95d35-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="95d35-194">Tiek importēts tas pats fails, jo formāta dizainā tiek pieņemts, ka elementam 'document' atribūts 'id' ir neobligāts.</span><span class="sxs-lookup"><span data-stu-id="95d35-194">The same file has been imported as the format design now consider the 'id' attribute for the 'document' element as optional.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]