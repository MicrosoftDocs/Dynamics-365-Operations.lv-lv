---
title: Failu importēšana XML formātā ar neobligātiem atribūtiem
description: Šajā tēmā ir sniegta informācija par tādu ER formātu veidošanu, kuri nosaka XML atribūtus ienākošo elektronisko dokumentu parsēšanai XML formātā.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5e2989906c5aa3ead9e46b8ed5333e880e5cf1c6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769951"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="35c2c-103">Failu importēšana XML formātā ar neobligātiem atribūtiem</span><span class="sxs-lookup"><span data-stu-id="35c2c-103">Import files in XML format with optional attributes</span></span>

<span data-ttu-id="35c2c-104">Varat veidot elektronisko pārskatu (Electronic Reporting — ER) formātus ienākošo dokumentu parsēšanai XML formātā.</span><span class="sxs-lookup"><span data-stu-id="35c2c-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents in XML format.</span></span> <span data-ttu-id="35c2c-105">Izveidotajā ER formātā noteiktus XML elementu atribūtus var norādīts kā neobligātus.</span><span class="sxs-lookup"><span data-stu-id="35c2c-105">Certain attributes of XML elements can be specified in designed ER format as optional.</span></span> <span data-ttu-id="35c2c-106">Tādējādi jūs varat pareizi apstrādāt ienākošos failus gan ar šādiem XML atribūtiem, gan bez tiem.</span><span class="sxs-lookup"><span data-stu-id="35c2c-106">It will allow you to handle incoming files with and without such XML attributes properly.</span></span> <span data-ttu-id="35c2c-107">Pēc tam saturu no šiem failiem varat izmantot, lai atjauninātu programmas datus.</span><span class="sxs-lookup"><span data-stu-id="35c2c-107">You can then use the content from these files to update application data.</span></span>

<span data-ttu-id="35c2c-108">Lai par šo līdzekli uzzinātu vairāk, izpildiet darbības, kas ir aprakstītas tēmā [(RCS) Failu importēšana XML formātā ar neobligātiem atribūtiem](tasks/import-files-xml-format-optional-attributes.md), kura veido daļu no biznesa procesa 7.5.4.3 IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677).</span><span class="sxs-lookup"><span data-stu-id="35c2c-108">To learn more about this feature, complete the steps in the topic, [(RCS) Import files in XML format with optional attributes](tasks/import-files-xml-format-optional-attributes.md), which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process.</span></span> <span data-ttu-id="35c2c-109">Šo uzdevuma ceļvedi un saistītos parauga failus varat lejupielādēt no [Microsoft lejupielādes centra](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="35c2c-109">You can download this task guide and associated sample files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>


| <span data-ttu-id="35c2c-110">Satura apraksts</span><span class="sxs-lookup"><span data-stu-id="35c2c-110">Content description</span></span>       | <span data-ttu-id="35c2c-111">Fails</span><span class="sxs-lookup"><span data-stu-id="35c2c-111">File</span></span>                                                         |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="35c2c-112">Parauga fails XML formātā</span><span class="sxs-lookup"><span data-stu-id="35c2c-112">Sample file in XML format</span></span> | <span data-ttu-id="35c2c-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span><span class="sxs-lookup"><span data-stu-id="35c2c-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span></span>     |
| <span data-ttu-id="35c2c-114">Uzdevuma ceļvedis</span><span class="sxs-lookup"><span data-stu-id="35c2c-114">Task guide</span></span>                | <span data-ttu-id="35c2c-115">RCS failu importēšana XML formātā ar neobligātiem atribūtiem.axtr</span><span class="sxs-lookup"><span data-stu-id="35c2c-115">RCS Import files in XML format with optional attributes.axtr</span></span> |


<span data-ttu-id="35c2c-116">Nākamajās darbībās ir paskaidrots, kā lietotājs ar lomu “Sistēmas administrators” vai “Elektronisko pārskatu izstrādātājs” var izveidot ER formāta konfigurāciju, lai importētu XML formātā tādus failus, kuros ir neobligāti atribūti.</span><span class="sxs-lookup"><span data-stu-id="35c2c-116">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="35c2c-117">Lai izpildītu tālāk norādītās darbības, vispirms izpildiet darbības procedūrā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="35c2c-117">To complete these steps, you must first complete the steps in the procedure, [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="35c2c-118">Pirms sākšanas lejupielādējiet un lokāli saglabājiet failu IncomingDocumentToLearnHowToHandleOptionalAttributes.xml no Microsoft lejupielādes centra (https://go.microsoft.com/fwlink/?linkid=874684 ).</span><span class="sxs-lookup"><span data-stu-id="35c2c-118">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span></span>

1. <span data-ttu-id="35c2c-119">Dodieties uz **Organizācijas administrēšana** > **Darbvietas** > **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-119">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="35c2c-120">Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam Litware, Inc. ir pieejams un ir atzīmēts kā **Aktīvs**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-120">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="35c2c-121">Ja neredzat šo konfigurācijas nodrošinātāju, izpildiet darbības tēmā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="35c2c-121">If you don’t see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="35c2c-122">Noklikšķiniet uz **Pārskatu veidošanas konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-122">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="35c2c-123">Jaunas datu modeļa konfigurācijas izveide</span><span class="sxs-lookup"><span data-stu-id="35c2c-123">Create a new data model configuration</span></span>
1. <span data-ttu-id="35c2c-124">Noklikšķiniet uz **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="35c2c-124">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="35c2c-125">Laukā **Nosaukums** ierakstiet “Modelis XML faila importēšanai”.</span><span class="sxs-lookup"><span data-stu-id="35c2c-125">In the **Name** field, type 'Model to import xml file'.</span></span>
3. <span data-ttu-id="35c2c-126">Klikšķiniet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-126">Click **Create configuration**.</span></span>
4. <span data-ttu-id="35c2c-127">Noklikšķiniet uz **Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-127">Click **Designer**.</span></span>
5. <span data-ttu-id="35c2c-128">Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="35c2c-128">Click **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="35c2c-129">Laukā **Nosaukums** ierakstiet “Sakne”.</span><span class="sxs-lookup"><span data-stu-id="35c2c-129">In the **Name** field, type 'Root'.</span></span>
7. <span data-ttu-id="35c2c-130">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-130">Click **Add**.</span></span>
8. <span data-ttu-id="35c2c-131">Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="35c2c-131">Click **New** to open the drop dialog.</span></span>
9. <span data-ttu-id="35c2c-132">Laukā **Nosaukums** ierakstiet “Saraksts”.</span><span class="sxs-lookup"><span data-stu-id="35c2c-132">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="35c2c-133">Laukā **Vienuma veids** atlasiet **Ierakstu saraksts**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-133">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="35c2c-134">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-134">Click **Add**.</span></span>
12. <span data-ttu-id="35c2c-135">Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="35c2c-135">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="35c2c-136">Laukā **Nosaukums** ierakstiet “Kods”.</span><span class="sxs-lookup"><span data-stu-id="35c2c-136">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="35c2c-137">Laukā **Vienuma veids** atlasiet **Virkne**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-137">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="35c2c-138">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-138">Click **Add**.</span></span>
16. <span data-ttu-id="35c2c-139">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-139">Click **Save**.</span></span>
17. <span data-ttu-id="35c2c-140">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="35c2c-140">Close the page.</span></span>
18. <span data-ttu-id="35c2c-141">Noklikšķiniet uz **Mainīt statusu**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-141">Click **Change status**.</span></span>
19. <span data-ttu-id="35c2c-142">Noklikšķiniet uz **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-142">Click **Complete**.</span></span>
20. <span data-ttu-id="35c2c-143">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-143">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="35c2c-144">Formāta izveidošana datu importēšanai</span><span class="sxs-lookup"><span data-stu-id="35c2c-144">Create a format for data import</span></span>
1. <span data-ttu-id="35c2c-145">Noklikšķiniet uz **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="35c2c-145">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="35c2c-146">Laukā **Jauns** ierakstiet “Formāts balstīts uz datu modeli Modelis XML faila importēšanai”.</span><span class="sxs-lookup"><span data-stu-id="35c2c-146">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3. <span data-ttu-id="35c2c-147">Laukā **Nosaukums** ierakstiet “Formāts XML faila importēšanai”.</span><span class="sxs-lookup"><span data-stu-id="35c2c-147">In the **Nam**e field, type 'Format to import xml file'.</span></span> 
4. <span data-ttu-id="35c2c-148">Laukā **Atbalsta datu importēšanu** atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-148">Select **Yes** in the **Supports data import** field.</span></span>
5. <span data-ttu-id="35c2c-149">Klikšķiniet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-149">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="35c2c-150">Formāta veidošana ienākoša faila parsēšanai XML formātā</span><span class="sxs-lookup"><span data-stu-id="35c2c-150">Design a format to parse incoming file in xml format</span></span>
1. <span data-ttu-id="35c2c-151">Noklikšķiniet uz **Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-151">Click **Designer**.</span></span>
2. <span data-ttu-id="35c2c-152">Noklikšķiniet uz **Pievienot sakni**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="35c2c-152">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="35c2c-153">Kokā atlasiet **XML\Elements**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-153">In the tree, select **XML\Element**.</span></span>
4. <span data-ttu-id="35c2c-154">Laukā **Nosaukums** ierakstiet “root”.</span><span class="sxs-lookup"><span data-stu-id="35c2c-154">In the **Name** field, type 'root'.</span></span>
5. <span data-ttu-id="35c2c-155">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-155">Click **OK**.</span></span>
6. <span data-ttu-id="35c2c-156">Noklikšķiniet uz **Pievienot**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="35c2c-156">Click **Add** to open the drop dialog.</span></span>
7. <span data-ttu-id="35c2c-157">Kokā atlasiet **XML\Elements**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-157">In the tree, select **XML\Element**.</span></span>
8. <span data-ttu-id="35c2c-158">Laukā **Nosaukums** ierakstiet “document”.</span><span class="sxs-lookup"><span data-stu-id="35c2c-158">In the **Name** field, type 'document'.</span></span>
9. <span data-ttu-id="35c2c-159">Laukā **Daudzkārtīgums** atlasiet **One many**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-159">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="35c2c-160">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-160">Click **OK**.</span></span>
11. <span data-ttu-id="35c2c-161">Koka struktūrā atlasiet **root\document**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-161">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="35c2c-162">Noklikšķiniet uz **Pievienot**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="35c2c-162">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="35c2c-163">Kokā atlasiet **XML\Atribūts**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-163">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="35c2c-164">Laukā **Nosaukums** ierakstiet “id”.</span><span class="sxs-lookup"><span data-stu-id="35c2c-164">In the **Name** field, type 'id'.</span></span>
15. <span data-ttu-id="35c2c-165">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-165">Click **OK**.</span></span>
16. <span data-ttu-id="35c2c-166">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-166">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="35c2c-167">Formāta kartējuma veidošana parsētās informācijas saglabāšanai datu modelī</span><span class="sxs-lookup"><span data-stu-id="35c2c-167">Design a format mapping to save parsed information to data model</span></span>
1.  <span data-ttu-id="35c2c-168">Noklikšķiniet uz **Kartēt formātu uz modeli**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-168">Click **Map format to model**.</span></span>
2.  <span data-ttu-id="35c2c-169">Noklikšķiniet uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-169">Click **New**.</span></span>
3.  <span data-ttu-id="35c2c-170">Laukā **Definīcija** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="35c2c-170">In the **Definition** field, enter or select a value.</span></span>
4.  <span data-ttu-id="35c2c-171">Laukā **Nosaukums** ierakstiet “Kartēšana”.</span><span class="sxs-lookup"><span data-stu-id="35c2c-171">In the **Name** field, type 'Mapping'.</span></span>
5.  <span data-ttu-id="35c2c-172">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-172">Click **Save**.</span></span>
6.  <span data-ttu-id="35c2c-173">Noklikšķiniet uz **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-173">Click **Designer**.</span></span>
7.  <span data-ttu-id="35c2c-174">Koka struktūrā izvērsiet zaru **format**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-174">In the tree, expand **format**.</span></span>
8.  <span data-ttu-id="35c2c-175">Koka struktūrā izvērsiet zaru **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-175">In the tree, expand **format\root: XML Element(root)**.</span></span>
9.  <span data-ttu-id="35c2c-176">Koka struktūrā atlasiet \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="35c2c-176">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="35c2c-177">(dokuments)\*\*.</span><span class="sxs-lookup"><span data-stu-id="35c2c-177">(document)\*\*.</span></span>
10. <span data-ttu-id="35c2c-178">Noklikšķiniet uz **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-178">Click **Bind**.</span></span>
11. <span data-ttu-id="35c2c-179">Koka struktūrā izvērsiet zaru \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="35c2c-179">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="35c2c-180">(dokuments)\*\*.</span><span class="sxs-lookup"><span data-stu-id="35c2c-180">(document)\*\*.</span></span>
12. <span data-ttu-id="35c2c-181">Koka struktūrā atlasiet \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="35c2c-181">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="35c2c-182">(dokuments)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="35c2c-182">(document)\id\*\*.</span></span>
13. <span data-ttu-id="35c2c-183">Koka struktūrā izvērsiet zaru **List = format.root.document**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-183">In the tree, expand **List = format.root.document**.</span></span>
14. <span data-ttu-id="35c2c-184">Koka struktūrā atlasiet zaru **List = format.root.document\Code**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-184">In the tree, select **List = format.root.document\Code**.</span></span>
15. <span data-ttu-id="35c2c-185">Noklikšķiniet uz **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-185">Click **Bind**.</span></span>
16. <span data-ttu-id="35c2c-186">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-186">Click **Save**.</span></span>
17. <span data-ttu-id="35c2c-187">Aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="35c2c-187">Close the page.</span></span>

## <a name="run-format-mapping"></a><span data-ttu-id="35c2c-188">Formāta kartēšanas darbināšana</span><span class="sxs-lookup"><span data-stu-id="35c2c-188">Run format mapping</span></span>
1. <span data-ttu-id="35c2c-189">Noklikšķiniet uz **Palaist**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-189">Click **Run**.</span></span>
2. <span data-ttu-id="35c2c-190">Noklikšķiniet uz **Pārlūkot** un atlasiet failu **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-190">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="35c2c-191">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-191">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="35c2c-192">Atlasītais fails nav importēts, jo formāta dizainā tiek pieņemts, ka elementam “document” ir atribūts “id”, bet importētajā failā tāda atribūta nav.</span><span class="sxs-lookup"><span data-stu-id="35c2c-192">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="35c2c-193">Formāta struktūras modificēšana, lai XML atribūtu apstrādātu kā neobligātu</span><span class="sxs-lookup"><span data-stu-id="35c2c-193">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="35c2c-194">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="35c2c-194">Close the page.</span></span>
2. <span data-ttu-id="35c2c-195">Koka struktūrā izvērsiet zaru **root\document**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-195">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="35c2c-196">Koka struktūrā atlasiet zaru **root\document\id**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-196">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="35c2c-197">Laukā **Tukša virkne trūkstošam atribūtam** atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-197">In the **Empty string for missing attribute** field, select **Yes**.</span></span>
5. <span data-ttu-id="35c2c-198">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-198">Click **Save**.</span></span>

## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="35c2c-199">Formāta kartējuma palaišana, lai testētu izmaiņas</span><span class="sxs-lookup"><span data-stu-id="35c2c-199">Run format mapping to test changes</span></span>
1. <span data-ttu-id="35c2c-200">Noklikšķiniet uz **Kartēt formātu uz modeli**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-200">Click **Map format to model**.</span></span>
2. <span data-ttu-id="35c2c-201">Noklikšķiniet uz **Palaist**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-201">Click **Run**.</span></span>
3. <span data-ttu-id="35c2c-202">Noklikšķiniet uz **Pārlūkot** un atlasiet failu **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-202">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
4. <span data-ttu-id="35c2c-203">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="35c2c-203">Click **OK**.</span></span>
5. <span data-ttu-id="35c2c-204">Pārskatiet ģenerēto failu.</span><span class="sxs-lookup"><span data-stu-id="35c2c-204">Review the generated file.</span></span> <span data-ttu-id="35c2c-205">Ievērojiet, ka tas pats fails ir importēts, jo formāta dizainā tiek pieņemts, ka elementam “document” atribūts “id” ir neobligāts.</span><span class="sxs-lookup"><span data-stu-id="35c2c-205">Note that same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
