---
title: Microsoft Office-stila lietotāja interfeiss biznesa dokumentu pārvaldībā
description: Šajā tēmā ir paskaidrots, kā izmantot jauno lietotāja interfeisu (UI) elektroniskā pārskata (ER) struktūras biznesa dokumentu pārvaldības līdzeklī.
author: v-anamir
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e6c5081f71a18dfac83b7aea950395436b42f50e
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881040"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a><span data-ttu-id="c473d-103">Microsoft Office-stila lietotāja interfeiss biznesa dokumentu pārvaldībā</span><span class="sxs-lookup"><span data-stu-id="c473d-103">Microsoft Office-style user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c473d-104">Biznesa dokumentu pārvaldība ļauj biznesa lietotājiem rediģēt biznesa dokumentu veidnes, izmantojot pakalpojumu Microsoft 365 vai atbilstošu Microsoft Office darbvirsmas lietojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="c473d-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="c473d-105">Rediģējumi var ietvert dizaina izmaiņas vai jaunas izvietošanas, vai arī lietotāji var pievienot vietturus, lai iekļautu papildu datus, nemainot pirmkodu.</span><span class="sxs-lookup"><span data-stu-id="c473d-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="c473d-106">Papildinformāciju par to, kā strādāt ar biznesa dokumentu pārvaldību, skatiet [Biznesa dokumentu pārvaldības pārskatā](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="c473d-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="c473d-107">Jaunais lietotāja interfeiss (UI) ir saprotamāks un ērtāk lietojams.</span><span class="sxs-lookup"><span data-stu-id="c473d-107">The new user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="c473d-108">**Biznesa dokumenta** apgabals parāda tikai tās veidnes, kas ir pieejamas pašreizējam nodrošinātājam.</span><span class="sxs-lookup"><span data-stu-id="c473d-108">The **Business document** area shows only the templates that are available for the current provider.</span></span> <span data-ttu-id="c473d-109">Iepriekšējā UI cilnē **Veidne** ir uzskaitītas visas veidnes, kas bija pieejamas visiem nodrošinātājiem.</span><span class="sxs-lookup"><span data-stu-id="c473d-109">In the previous UI, the **Template** tab listed all the templates that were available for any providers.</span></span> <span data-ttu-id="c473d-110">Tas arī parāda visas veidnes, ko izveidoja un laboja jebkurš lietotājs, kuram bija vienāda loma.</span><span class="sxs-lookup"><span data-stu-id="c473d-110">It also showed all the templates that were created and edited by any user who had the same role.</span></span>

<span data-ttu-id="c473d-111">Var izmantot pogu **Jauns dokuments**, lai izveidotu un rediģētu veidni elektroniskā pārskata (ER) formāta konfigurācijā, kas pieder citam nodrošinātājam.</span><span class="sxs-lookup"><span data-stu-id="c473d-111">You can use the **New document** button to create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="c473d-112">Šīs tēmas piemērā nodrošinātājs ir Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c473d-112">In the example in this topic, the provider is Microsoft.</span></span> <span data-ttu-id="c473d-113">Alternatīvi veidni var izveidot, augšupielādējot savu veidni Excel formātā.</span><span class="sxs-lookup"><span data-stu-id="c473d-113">Alternatively, you can create a template by uploading your own template in Excel format.</span></span>


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

<span data-ttu-id="c473d-114">Video [Izveidot jaunu biznesa dokumentu, izmantojot biznesa dokumentu pārvaldību](https://youtu.be/gAIYl-mM_pw) (parādīts iepriekš) ir iekļauts [Finance and Operations atskaņošanas sarakstā](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), kas ir pieejams YouTube.</span><span class="sxs-lookup"><span data-stu-id="c473d-114">The [Create a new business document using Business document management](https://youtu.be/gAIYl-mM_pw) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="c473d-115">Nodrošināt jauno dokumentu lietotāja interfeisa pieejamību biznesa dokumentu pārvaldībā</span><span class="sxs-lookup"><span data-stu-id="c473d-115">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="c473d-116">Lai biznesa dokumentu pārvaldībā sāktu izmantot jauno dokumentu lietotāja interfeisu, jāieslēdz līdzeklis **Office līdzīgais lietotāja interfeiss biznesa dokumentu pārvaldībai** darbvietā **Līdzekļu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="c473d-116">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="c473d-117">Lai ieslēgtu šo līdzekli visām juridiskajām personām, veiciet tālak norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="c473d-117">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="c473d-118">Darbvietas **Lïdzekĺu pārvaldība** cilnē **Viss** atlasiet sarakstā līdzekli **Office līdzīgais lietotāja interfeiss biznesa dokumentu pārvaldībai**.</span><span class="sxs-lookup"><span data-stu-id="c473d-118">In the **Feature management** workspace, on the **All** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="c473d-119">Atlasiet **Iespējot tūlīt**, lai ieslēgtu atlasīto funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="c473d-119">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="c473d-120">Atsvaidziniet lapu, lai piekļūtu jaunajam līdzeklim.</span><span class="sxs-lookup"><span data-stu-id="c473d-120">Refresh the page to access the new feature.</span></span>

## <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="c473d-121">Citiem nodrošinātājiem piederošu veidņu rediģēšana</span><span class="sxs-lookup"><span data-stu-id="c473d-121">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="c473d-122">Darbvietā **Biznesa dokumentu pārvaldība** atlasiet **Jauns dokuments**.</span><span class="sxs-lookup"><span data-stu-id="c473d-122">In the **Business document management** workspace, select **New document**.</span></span>

    ![Biznesa dokumentu pārvaldības darbvieta](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="c473d-124">Cilnē **Atlasīt** atlasiet dokumentu, kas jālieto kā veidne, un pēc tam atlasiet **Izveidot dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="c473d-124">On the **Select** tab, select the document to use as a template, and then select **Create document**.</span></span>

    ![Dialoglodziņš biznesa dokumenti](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="c473d-126">Jaunā dialoglodziņa laukā **Nosaukums** mainiet nosaukumu, kā nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="c473d-126">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="c473d-127">Nosaukuma teksts tiek izmantots jaunajam automātiski izveidotās ER formāta konfigurācijas nosaukumam.</span><span class="sxs-lookup"><span data-stu-id="c473d-127">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="c473d-128">Šīs konfigurācijas (**Klientu FTI pārskats (GER) Kopija**) melnraksta versija ietvers rediģēto veidni un tiks izmantota šī ER formāta izmantošanai pašreizējam lietotājam.</span><span class="sxs-lookup"><span data-stu-id="c473d-128">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="c473d-129">Sākotnējā veidne no pamata ER formāta konfigurācijas tiks izmantota šī ER formāta lietošanai ikvienam citam lietotājam.</span><span class="sxs-lookup"><span data-stu-id="c473d-129">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="c473d-130">Laukā **Nosaukums** nomainiet nosaukumu pirmās rediģējamās veidnes pārskatīšanai, kas tiks izveidota automātiski.</span><span class="sxs-lookup"><span data-stu-id="c473d-130">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="c473d-131">Laukā **Komentārs** atjauniniet piezīmes rediģējamās veidnes, kas tiks izveidota automātiski, pārskatīšanai.</span><span class="sxs-lookup"><span data-stu-id="c473d-131">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="c473d-132">Atlasiet **Labi**, lai apstiprinātu rediģēšanas procesa sākumu.</span><span class="sxs-lookup"><span data-stu-id="c473d-132">Select **OK** to confirm the start of the editing process.</span></span>

    ![Dialoglodziņš Dokumenta izveide](./media/BDM_overview_new_template3.png)

<span data-ttu-id="c473d-134">Pogu **Jauns dokuments** lieto, lai izveidotu un rediģētu veidni ER formāta konfigurācijā, kas pieder citam nodrošinātājam.</span><span class="sxs-lookup"><span data-stu-id="c473d-134">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="c473d-135">Šajā piemērā nodrošinātājs ir Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c473d-135">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="c473d-136">Atlasot **Jauns dokuments**, jūs varat rezēt visas veidnes, kas pieder pašreizējiem un citiem nodrošinātājiem.</span><span class="sxs-lookup"><span data-stu-id="c473d-136">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="c473d-137">Pēc veidnes atlasīšanas tā ir atvērta rediģēšanai.</span><span class="sxs-lookup"><span data-stu-id="c473d-137">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="c473d-138">Rediģētā veidne būs saglabāta jaunā ER formāta konfigurācijā, kas ģenerēta automātiski.</span><span class="sxs-lookup"><span data-stu-id="c473d-138">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a><span data-ttu-id="c473d-139">Augšupielādēt veidni, kas izmanto esošu Excel formātu</span><span class="sxs-lookup"><span data-stu-id="c473d-139">Upload a template that uses an existing Excel format</span></span>
<span data-ttu-id="c473d-140">Izpildiet šīs darbības, lai pirms veidnes augšupielādes sniegtu nepieciešamo informāciju.</span><span class="sxs-lookup"><span data-stu-id="c473d-140">Follow these steps to provide required information before you upload a template.</span></span>

1. <span data-ttu-id="c473d-141">Darbvietā **Biznesa dokumentu pārvaldība** atlasiet **Jauns dokuments**.</span><span class="sxs-lookup"><span data-stu-id="c473d-141">In the **Business document management** workspace, select **New document**.</span></span>

    ![Biznesa dokumentu pārvaldības darbvieta](./media/BDM_overview_new_template1.png)
    
2. <span data-ttu-id="c473d-143">Lapā **Izveidot jaunu veidni**, cilnē **Augšupielādēt**, cilnē **Veidne** atlasiet **Pārlūkot**, lai atrastu un atlasītu Excel failu, kuru vēlaties izmantot kā veidni.</span><span class="sxs-lookup"><span data-stu-id="c473d-143">On the **Create a new template** page, on the **Upload** tab, on the **Template** tab, select **Browse** to find and select the Excel file that you want to use as a template.</span></span> <span data-ttu-id="c473d-144">Sadaļā **Veidne** automātiski tiek aizpildīti lauki **Nosaukums** un **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="c473d-144">In the **Template** section, the **Title** and **Description** fields are automatically filled in.</span></span> <span data-ttu-id="c473d-145">Tie nosaka automātiski izveidotās jaunā ER formāta konfigurācijas nosaukumu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="c473d-145">They specify the name and description of the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="c473d-146">Ja nepieciešams, jūs varat rediģēt šos laukus.</span><span class="sxs-lookup"><span data-stu-id="c473d-146">You can edit these fields as you require.</span></span>
3. <span data-ttu-id="c473d-147">Sadaļas **Dokumenta tips** laukā **Nosaukums** norādiet biznesa dokumenta tipu.</span><span class="sxs-lookup"><span data-stu-id="c473d-147">In the **Document Type** section, in the **Name** field, specify the type of business document.</span></span> <span data-ttu-id="c473d-148">Šī vērtība tiks izmantota, lai meklētu pareizo datu avotu (t.i., ER modeļa konfigurāciju).</span><span class="sxs-lookup"><span data-stu-id="c473d-148">This value will be used to search the correct data source (that is, the ER model configuration).</span></span>

    ![Cilne Veidne](./media/BDM_overview_new_UI_import_21.jpg)

4. <span data-ttu-id="c473d-150">Cilnē **Datu avots** kopsavilkuma cilnē **Filtrs** atlasiet **Lietot filtru**.</span><span class="sxs-lookup"><span data-stu-id="c473d-150">On the **Data source** tab, on the **Filter** FastTab, select **Apply filter**.</span></span> <span data-ttu-id="c473d-151">Sadaļā **Datu avots** lauks **Nosaukums** tiek aizpildīts automātiski vai varat atlasīt vērtību manuāli.</span><span class="sxs-lookup"><span data-stu-id="c473d-151">In the **Data source** section, the **Name** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="c473d-152">Filtru var izmantot, lai meklētu atbilstošu datu avota nosaukumu pēc nosaukuma, apraksta, valsts/reģiona koda un biznesa dokumenta tipa.</span><span class="sxs-lookup"><span data-stu-id="c473d-152">You can use the filter to search for the appropriate data source name by name, description, country/region code, and business document type.</span></span>

    ![Datu avota cilne](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > <span data-ttu-id="c473d-154">Kopsavilkuma cilne **Filtrs** tiek izmantota, lai meklētu pareizo datu avotu (t.i., ER modeļa konfigurāciju).</span><span class="sxs-lookup"><span data-stu-id="c473d-154">The **Filter** FastTab is used to search the correct data source (that is, the ER model configuration).</span></span> <span data-ttu-id="c473d-155">Jūs varat rediģēt visus filtra laukus, lai atrastu vispiemērotāko datu avotu dokumentam, ko augšupielādējat.</span><span class="sxs-lookup"><span data-stu-id="c473d-155">You can edit all filter fields to find the most appropriate data source for the document that you're uploading.</span></span>
    > 
    > <span data-ttu-id="c473d-156">Kopsavilkuma cilnē **Filtrs** nosacījumi tiek izmantoti kā **VAI** nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="c473d-156">The conditions on the **Filter** FastTab are used as **OR** conditions.</span></span>
    
5. <span data-ttu-id="c473d-157">Cilnē **Kartēšana** atlasiet **Automātiski noteikt**.</span><span class="sxs-lookup"><span data-stu-id="c473d-157">On the **Mapping** tab, select **Auto detect**.</span></span> <span data-ttu-id="c473d-158">Lauks **Saknes definīcija** tiek aizpildīts automātiski vai varat atlasīt vērtību manuāli.</span><span class="sxs-lookup"><span data-stu-id="c473d-158">The **Root definition** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="c473d-159">Šajā cilnē ir redzama elementu beigu kartēšana no veidnes un modeļa.</span><span class="sxs-lookup"><span data-stu-id="c473d-159">This tab shows the end mapping for the elements from the template and the model.</span></span>

    ![Cilne Kartēšana](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > <span data-ttu-id="c473d-161">Kartēšanai sadaļā **Veidņu struktūra** izmanto pilnu etiķešu vai aprakstu atbilstību datu avotā lietotāja valodā un šūnas nosaukumā veidnē.</span><span class="sxs-lookup"><span data-stu-id="c473d-161">The mapping in the **Template structure** section uses the full match of the labels or descriptions in the data source in the user's language, and in the cell name in the template.</span></span>

6. <span data-ttu-id="c473d-162">Atlasiet **Izveidot dokumentu**, lai apstiprinātu, ka vēlaties izveidot veidni un sākt rediģēšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="c473d-162">Select **Create document** to confirm that you want to create a template and start the editing process.</span></span>

<span data-ttu-id="c473d-163">Plašāku informāciju skatiet [Biznesa dokumentu pārvaldības apskatā](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="c473d-163">For more information, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="c473d-164">Ja elektronisko pārskatu nodrošinātājs nav pieejams, varat to izveidot.</span><span class="sxs-lookup"><span data-stu-id="c473d-164">If there isn't a provider in Electronic reporting, you can create one.</span></span> <span data-ttu-id="c473d-165">Ja nav aktīva nodrošinātāja, varat izvēlēties to aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="c473d-165">If there's no active provider, you can select to activate one.</span></span>

- <span data-ttu-id="c473d-166">Lai izveidotu nodrošinātāju, mainiet nodrošinātāja nosaukumu laukā **Nosaukums**, atjauniniet jaunā nodrošinātāja interneta adresi laukā **Interneta adrese** un atlasiet **Labi**, lai apstiprinātu.</span><span class="sxs-lookup"><span data-stu-id="c473d-166">To create a provider, change the name of the provider in the **Name** field, update the internet address of the new provider in the **Internet address** field, and select **OK** to confirm.</span></span>

    ![Izveidot jaunu nodrošinātāju BDM](./media/bdm_create_provider.png)
    
- <span data-ttu-id="c473d-168">Lai aktivizētu esošu nodrošinātāju, izvēlieties nodrošinātāja nosaukumu laukā **Konfigurācijas nodrošinātājs** un atlasiet **Labi**, lai iestatītu nodrošinātāju kā aktīvu.</span><span class="sxs-lookup"><span data-stu-id="c473d-168">To activate existing provider, choose the name of the provider in the **Configuration provider** field, and select **OK** to set provider as active.</span></span>

    ![Aktivizēt nodrošinātāju BDM](./media/bdm_choose_provider.png)

> [!NOTE]
> <span data-ttu-id="c473d-170">Katra BDM veidne atsaucas uz nodrošinātāju kā konfigurācijas autoru.</span><span class="sxs-lookup"><span data-stu-id="c473d-170">Each BDM template refers to the provider as the author of the configuration.</span></span> <span data-ttu-id="c473d-171">Tāpēc veidnei ir nepieciešams aktīvs nodrošinātājs.</span><span class="sxs-lookup"><span data-stu-id="c473d-171">This is why an active provider is required for the template.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
