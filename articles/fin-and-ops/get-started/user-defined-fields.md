---
title: "Pielāgoti lauki"
description: "Šajā tēmā parādīts, kā Microsoft Dynamics 365 for Finance and Operations noteiktiem lietotājiem ļauj izveidot pielāgotus laukus un pielāgot programmu sava uzņēmuma vajadzībām."
author: jasongre
manager: AnnBe
ms.date: 01/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: ad59346f88b7a5984e16418e2aade7ccaedf180b
ms.openlocfilehash: 142c66c189d6401cfb3db128e45fea6c071e99bf
ms.contentlocale: lv-lv
ms.lasthandoff: 02/28/2018

---

# <a name="custom-fields"></a><span data-ttu-id="7d48f-103">Pielāgoti lauki</span><span class="sxs-lookup"><span data-stu-id="7d48f-103">Custom fields</span></span>

[!include[banner](../includes/banner.md)] 

[!include[banner](../includes/pre-release.md)] 

<span data-ttu-id="7d48f-104">Lai gan Microsoft Dynamics 365 for Finance and Operations Enterprise Edition nodrošina lietošanai gatavu plašu lauku kopu dažādu veidu biznesa procesu pārvaldībai, dažkārt uzņēmumā ir nepieciešams sistēmā izsekot papildu informāciju.</span><span class="sxs-lookup"><span data-stu-id="7d48f-104">While Microsoft Dynamics 365 for Finance and Operations, Enterprise edition provides an extensive set of fields out-of-the-box for managing a broad range of business processes, sometimes there is a need for a company to track additional information in the system.</span></span> <span data-ttu-id="7d48f-105">Tādēļ programmā Finance and Operations varat izveidot pielāgotus laukus un programmu pielāgot sava uzņēmuma vajadzībām (ja jums ir nepieciešamās atļaujas, lai piekļūtu šim līdzeklim).</span><span class="sxs-lookup"><span data-stu-id="7d48f-105">To accommodate this need, Finance and Operations allows you to create custom fields to tailor the application to fit your business, provided you have permissions to the feature.</span></span>

<span data-ttu-id="7d48f-106">Šajā video parādīts, cik viegli ir lapai pievienot pielāgotu lauku.</span><span class="sxs-lookup"><span data-stu-id="7d48f-106">This video shows how easy it is to add a custom field to a page.</span></span>


> [!Video https://www.youtube.com/embed/gWSGZI9Vtnc]

## <a name="creating-custom-fields"></a><span data-ttu-id="7d48f-107">Pielāgoto lauku izveide</span><span class="sxs-lookup"><span data-stu-id="7d48f-107">Creating custom fields</span></span>
<span data-ttu-id="7d48f-108">Kad esat noteicis, kādu papildu informāciju vēlaties izsekot programmā, attiecīgajā tabulā varat izveidot pielāgoto laiku un sniegt šo jauno lauku lapā.</span><span class="sxs-lookup"><span data-stu-id="7d48f-108">After you’ve identified additional information that you would like to track in the application, you can create the custom field on the appropriate table and expose that new field on a page.</span></span>   

<span data-ttu-id="7d48f-109">Tālākajās darbībās aprakstīts process pielāgota lauka izveidei un šī lauka ievietošanai formā.</span><span class="sxs-lookup"><span data-stu-id="7d48f-109">The following steps describe the process for creating a custom field and placing that field on a form.</span></span>  

1.   <span data-ttu-id="7d48f-110">Atveriet formu, kurā nepieciešams pievienot jauno lauku.</span><span class="sxs-lookup"><span data-stu-id="7d48f-110">Navigate to the form where the new field is needed.</span></span> 
2.   <span data-ttu-id="7d48f-111">Tā kā mērķis ir pielāgoto lauku sniegt formā, pielāgoto lauku ieejas punkts ir personalizēšanas pieredzē.</span><span class="sxs-lookup"><span data-stu-id="7d48f-111">Because the end goal is to expose the custom field on a form, the entry point for creating custom fields exists inside the personalization experience.</span></span> <span data-ttu-id="7d48f-112">Atveriet personalizēšanas rīkjoslu, atlasot vienumu **Opcijas** un pēc tam atlasot vienumu **Personalizēt šo formu**.</span><span class="sxs-lookup"><span data-stu-id="7d48f-112">Open the personalization toolbar by selecting **Options**, and then **Personalize this form**.</span></span> 
3.   <span data-ttu-id="7d48f-113">Noklikšķiniet uz vienuma **Ievietot** un pēc tam uz **Lauks**.</span><span class="sxs-lookup"><span data-stu-id="7d48f-113">Click **Insert** and then **Field**.</span></span>  
4.   <span data-ttu-id="7d48f-114">Atlasiet to formas reģionu, kurā vēlaties parādīt jauno lauku.</span><span class="sxs-lookup"><span data-stu-id="7d48f-114">Select the region of the form where you want to expose the new field.</span></span> <span data-ttu-id="7d48f-115">Pēc atlases dialoglodziņā **Ievietot laukus** tiks parādīts saraksts ar esošiem laukiem, ko var ievietot atlasītajā formas reģionā.</span><span class="sxs-lookup"><span data-stu-id="7d48f-115">After selection, the **Insert fields** dialog box will display a list of existing fields that can be inserted into the selected region of the form.</span></span>  
5.   <span data-ttu-id="7d48f-116">Pārliecinieties, vai interesējošais lauks jau nav sarakstā.</span><span class="sxs-lookup"><span data-stu-id="7d48f-116">Ensure that the field you are interested in does not already exist in the list.</span></span> <span data-ttu-id="7d48f-117">Ja tas ir sarakstā, atlasiet šo lauku un noklikšķiniet uz **Ievietot**.</span><span class="sxs-lookup"><span data-stu-id="7d48f-117">If it does, you can simply select that field in the list and click **Insert**.</span></span>   
6.   <span data-ttu-id="7d48f-118">Noklikšķiniet uz pogas **Izveidot jaunu lauku** virs saraksta, lai uzsāktu pielāgota lauka izveides procesu.</span><span class="sxs-lookup"><span data-stu-id="7d48f-118">Click the **Create new field** button above the list to initiate the process of creating a custom field.</span></span> <span data-ttu-id="7d48f-119">Tiks atvērts dialoglodziņš **Izveidot jaunu lauku**.</span><span class="sxs-lookup"><span data-stu-id="7d48f-119">This will open the **Create new field** dialog box.</span></span> 

     <span data-ttu-id="7d48f-120">Ja neredzat pogu **Izveidot jaunu lauku**, jums nav nepieciešamo atļauju šī līdzekļa lietošanai.</span><span class="sxs-lookup"><span data-stu-id="7d48f-120">If you do not see the **Create new field** button, you do not have the necessary permissions to use this feature.</span></span>  
     
7.   <span data-ttu-id="7d48f-121">Dialoglodziņā **Izveidot jaunu lauku** ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="7d48f-121">In the **Create new field** dialog box, enter the following information.</span></span>
     1.   <span data-ttu-id="7d48f-122">Atlasiet datu bāzes tabulu, kurai jāpievieno šis lauks.</span><span class="sxs-lookup"><span data-stu-id="7d48f-122">Select the database table where this field should be added.</span></span> <span data-ttu-id="7d48f-123">Ņemiet vērā, ka nolaižamajā sarakstā tiks parādītas tikai tabulas, kas atbalsta pielāgotos laukus.</span><span class="sxs-lookup"><span data-stu-id="7d48f-123">Note that only tables that support custom fields will appear in the drop-down list.</span></span> <span data-ttu-id="7d48f-124">Tehnisko informāciju par atbalstītajām tabulām skatiet tālāk esošajā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="7d48f-124">See the section below for technical details on supported tables.</span></span>  
     2.   <span data-ttu-id="7d48f-125">Atlasiet jaunā lauka datu tipu.</span><span class="sxs-lookup"><span data-stu-id="7d48f-125">Select the data type for the new field.</span></span> <span data-ttu-id="7d48f-126">Pieejamie datu tipi ir izvēles rūtiņa, datums, datums un laiks, decimāldaļskaitlis, skaitlis, salasīšanas saraksts un teksts.</span><span class="sxs-lookup"><span data-stu-id="7d48f-126">The available data types are checkbox, date, date time, decimal, number, picklist, and text.</span></span>   
          - <span data-ttu-id="7d48f-127">Ja izvēlaties teksta datu tipu, var arī norādīt maksimālo šajā laukā ievadāmā teksta garumu.</span><span class="sxs-lookup"><span data-stu-id="7d48f-127">If you choose the text data type, you can also specify the maximum length of the text that can be entered in this field.</span></span> 
          - <span data-ttu-id="7d48f-128">Ja izvēlaties salasīšanas saraksta datu tipu, varat arī atlasīt laukam derīgo vērtību kopu.</span><span class="sxs-lookup"><span data-stu-id="7d48f-128">If you choose the picklist data type, you can also select the set of valid values for the field.</span></span>  
     3.   <span data-ttu-id="7d48f-129">Norādiet lauka nosaukumu, etiķeti un palīdzības tekstu.</span><span class="sxs-lookup"><span data-stu-id="7d48f-129">Provide a name, label, and help text for the field.</span></span> <span data-ttu-id="7d48f-130">Nosaukums atbilst fiziskajam lauka nosaukumam datu bāzē, savukārt etiķete un palīdzības teksts ir teksts, kas šo lauku attēlo lietotāja interfeisā.</span><span class="sxs-lookup"><span data-stu-id="7d48f-130">The name corresponds to the physical field name in the database, whereas the label and help text are the text used to represent this field in the user interface.</span></span>  
8.   <span data-ttu-id="7d48f-131">Ja tas ir vienīgais lauks, kas jums jāizveido šai formai, noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="7d48f-131">If this is the only field that you need to create for this form, click **Save**.</span></span> <span data-ttu-id="7d48f-132">Ja nepieciešams izveidot papildu laukus, noklikšķiniet uz **Saglabāt un izveidot jaunu** un pārejiet uz 7. darbību.</span><span class="sxs-lookup"><span data-stu-id="7d48f-132">If you need to create additional fields, click **Save and new** and go back to step 7.</span></span> <span data-ttu-id="7d48f-133">Ņemiet vērā, ka pašlaik ir noteikts ierobežojums **20 pielāgoto lauku vienā tabulā**.</span><span class="sxs-lookup"><span data-stu-id="7d48f-133">Note that there is currently a limit of **20 custom fields per table**.</span></span>
9.   <span data-ttu-id="7d48f-134">Ja iziesit no dialoglodziņa **Izveidot jaunu lauku**, tiksit novirzīts uz dialoglodziņu **Ievietot laukus**.</span><span class="sxs-lookup"><span data-stu-id="7d48f-134">Leaving the **Create new field** dialog box will return you to the **Insert fields** dialog box.</span></span> <span data-ttu-id="7d48f-135">Visi tikko pievienotie pielāgotie lauki tiks automātiski atzīmēti lauku sarakstā ievietošanai formā.</span><span class="sxs-lookup"><span data-stu-id="7d48f-135">Any custom fields that were just added will be automatically marked in the field list to be inserted into the form.</span></span>  
10.   <span data-ttu-id="7d48f-136">Lai atzīmētos laukus ievietotu atlasītajā formas reģionā, noklikšķiniet uz **Ievietot**.</span><span class="sxs-lookup"><span data-stu-id="7d48f-136">Click **Insert** to insert the marked fields into the selected region of the form.</span></span> 
11.   <span data-ttu-id="7d48f-137">**Neobligāti:** iespējojiet personalizēšanas rīkjoslā režīmu **Pārvietot**, lai jaunos laukus pārvietotu uz vajadzīgo vietu atlasītajā reģionā.</span><span class="sxs-lookup"><span data-stu-id="7d48f-137">**Optional:** Enable **Move** mode from the personalization toolbar to move the new fields to their desired location in the selected region.</span></span> <span data-ttu-id="7d48f-138">Papildinformāciju par to, kā izmantot dažādās personalizēšanas iespējas, lai formu optimāli pielāgotu personīgajam lietojumam, skatiet tēmā [Lietotāja pieredzes personalizēšana](personalize-user-experience.md).</span><span class="sxs-lookup"><span data-stu-id="7d48f-138">See [Personalize the user experience](personalize-user-experience.md) for more information about how to use the various personalization capabilities to optimize a form for your personal usage.</span></span>  

## <a name="sharing-custom-fields-with-other-users"></a><span data-ttu-id="7d48f-139">Pielāgoto lauku koplietošana ar citiem lietotājiem</span><span class="sxs-lookup"><span data-stu-id="7d48f-139">Sharing custom fields with other users</span></span>
<span data-ttu-id="7d48f-140">Kad esat izveidojis pielāgotu laiku un sniedzis to formā, iespējams, šo atjaunināto lapas skatu, kurā ietverts jaunais lauks, vēlaties nodrošināt citiem sistēmas lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="7d48f-140">After you have created a custom field and exposed it on a form, you might want to provide this updated page view that includes the new field to other users in the system.</span></span> <span data-ttu-id="7d48f-141">To var izdarīt divos dažādos veidos, izmantojot produkta personalizēšanas iespējas.</span><span class="sxs-lookup"><span data-stu-id="7d48f-141">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

-   <span data-ttu-id="7d48f-142">Ieteicamais veids ir caur sistēmas administratoru, kurš personalizāciju var aizgādāt visiem lietotajiem vai lietotāju apakškopai.</span><span class="sxs-lookup"><span data-stu-id="7d48f-142">The recommended route is through the system administrator, who can push a personalization to all users or a subset of users.</span></span> <span data-ttu-id="7d48f-143">Papildinformāciju skatiet tēmā [Lietotāja pieredzes personalizēšana](personalize-user-experience.md).</span><span class="sxs-lookup"><span data-stu-id="7d48f-143">See [Personalize the user experience](personalize-user-experience.md) for more details.</span></span> 

-   <span data-ttu-id="7d48f-144">Vai arī varat eksportēt veiktās izmaiņas (dēvētas par *personalizācijām*), nosūtīt tās vienam vai vairākiem lietotājiem un likt katram no šiem lietotājiem importēt izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="7d48f-144">Alternatively, you can export your changes (called *personalizations*), send them to one or more users, and have each of those users import your changes.</span></span> <span data-ttu-id="7d48f-145">Izmantojot personalizēšanas rīkjoslā esošo opciju **Pārvaldīt**, varat eksportēt un importēt personalizācijas.</span><span class="sxs-lookup"><span data-stu-id="7d48f-145">The **Manage** option on the personalization toolbar enables you to export and import personalizations.</span></span>

## <a name="managing-custom-fields"></a><span data-ttu-id="7d48f-146">Pielāgoto lauku pārvaldība</span><span class="sxs-lookup"><span data-stu-id="7d48f-146">Managing custom fields</span></span>

<span data-ttu-id="7d48f-147">Visus sistēmā esošos pielāgotos laukus var pārvaldīt, izmantojot lapu **Pielāgoti lauki** sistēmas administrēšanas modulī.</span><span class="sxs-lookup"><span data-stu-id="7d48f-147">Management of all the custom fields in the system can be accomplished through the **Custom fields** page in the System administration module.</span></span>  <span data-ttu-id="7d48f-148">Izmantojot šo lapu, lietotāji var piekļūt daudzām iespējām, tostarp tālāk norādītajām.</span><span class="sxs-lookup"><span data-stu-id="7d48f-148">This page allows users access to many capabilities, including:</span></span> 
-   <span data-ttu-id="7d48f-149">Visu sistēmā esošo pielāgoto lauku saraksta skatīšana.</span><span class="sxs-lookup"><span data-stu-id="7d48f-149">Viewing a list of all custom fields in the system.</span></span>
-   <span data-ttu-id="7d48f-150">Ierobežota esošo pielāgoto lauku rediģēšana.</span><span class="sxs-lookup"><span data-stu-id="7d48f-150">Limited editing of existing custom fields.</span></span>
-   <span data-ttu-id="7d48f-151">Pielāgoto lauku dzēšana.</span><span class="sxs-lookup"><span data-stu-id="7d48f-151">Deleting custom fields.</span></span>
-   <span data-ttu-id="7d48f-152">Pielāgoto lauku sniegšana datu elementos.</span><span class="sxs-lookup"><span data-stu-id="7d48f-152">Exposing custom fields on data entities.</span></span>
-   <span data-ttu-id="7d48f-153">Pielāgoto lauku etiķešu un palīdzības teksta tulkojumu nodrošināšana.</span><span class="sxs-lookup"><span data-stu-id="7d48f-153">Providing translations of custom field labels and help text.</span></span>

### <a name="viewing-all-custom-fields"></a><span data-ttu-id="7d48f-154">Visu pielāgoto lauku skatīšana</span><span class="sxs-lookup"><span data-stu-id="7d48f-154">Viewing all custom fields</span></span>
<span data-ttu-id="7d48f-155">Lapa **Pielāgoti lauki** nodrošina visu sistēmā definēto pielāgoto lauku redzamību.</span><span class="sxs-lookup"><span data-stu-id="7d48f-155">The **Custom fields** page provides visibility to all the custom fields that have been defined in the system.</span></span> <span data-ttu-id="7d48f-156">Atlasiet interesējošo tabulu, un lapa tiks atjaunināta, lai parādītu ar šo tabulu saistītos pielāgotos laukus.</span><span class="sxs-lookup"><span data-stu-id="7d48f-156">Simply select the table that you are interested in, and the page will update to show a list of the custom fields associated with that table.</span></span> <span data-ttu-id="7d48f-157">Izvēloties pielāgotu lauku no saraksta, varēsit skatīt visu informāciju par lauku.</span><span class="sxs-lookup"><span data-stu-id="7d48f-157">Choosing a custom field from the list will allow you to view all the details about the field.</span></span>

### <a name="editing-custom-fields"></a><span data-ttu-id="7d48f-158">Pielāgoto lauku rediģēšana</span><span class="sxs-lookup"><span data-stu-id="7d48f-158">Editing custom fields</span></span>
<span data-ttu-id="7d48f-159">Pēc pielāgotā lauka izveides lapā **Pielāgoti lauki** var modificēt tikai noteiktu informāciju par šo pielāgoto lauku.</span><span class="sxs-lookup"><span data-stu-id="7d48f-159">After a custom field has been created, only certain pieces of information about the custom field can be modified on the **Custom fields** page.</span></span>   

<span data-ttu-id="7d48f-160">*Var* modificēt tālāk norādītos atribūtus.</span><span class="sxs-lookup"><span data-stu-id="7d48f-160">You *can* modify these attributes:</span></span> 
-   <span data-ttu-id="7d48f-161">Iezīme</span><span class="sxs-lookup"><span data-stu-id="7d48f-161">Label</span></span> 
-   <span data-ttu-id="7d48f-162">Palīdzības teksts</span><span class="sxs-lookup"><span data-stu-id="7d48f-162">Help text</span></span>
-   <span data-ttu-id="7d48f-163">Garums (teksta laukiem)</span><span class="sxs-lookup"><span data-stu-id="7d48f-163">Length, for Text fields</span></span>

<span data-ttu-id="7d48f-164">*Nevar* rediģēt tālāk norādītos atribūtus.</span><span class="sxs-lookup"><span data-stu-id="7d48f-164">You *cannot* edit the following attributes:</span></span> 
-   <span data-ttu-id="7d48f-165">Lauka nosaukums</span><span class="sxs-lookup"><span data-stu-id="7d48f-165">Field name</span></span>
-   <span data-ttu-id="7d48f-166">Datu tips</span><span class="sxs-lookup"><span data-stu-id="7d48f-166">Data type</span></span>

<span data-ttu-id="7d48f-167">Turklāt salasīšanas sarakstiem var pārkārtot pielāgotā lauka derīgo vērtību kopu un pievienot jaunas vērtības. Tomēr esošās salasīšanas saraksta lauka vērtības nevar noņemt.</span><span class="sxs-lookup"><span data-stu-id="7d48f-167">Additionally, for picklist fields, the set of valid values for the custom field can be reordered, and new values can be added; however, existing values for the picklist field cannot be removed.</span></span> <span data-ttu-id="7d48f-168">Kad esat pabeidzis rediģēt noteiktas tabulas laukus, noteikti noklikšķiniet uz vienuma **Lietot izmaiņas**, lai izmaiņas tiktu saglabātas.</span><span class="sxs-lookup"><span data-stu-id="7d48f-168">Remember to click **Apply changes** when you are done editing fields for a particular table so the changes are saved.</span></span> 

### <a name="exposing-custom-fields-on-data-entities"></a><span data-ttu-id="7d48f-169">Pielāgoto lauku sniegšana datu elementos</span><span class="sxs-lookup"><span data-stu-id="7d48f-169">Exposing custom fields on data entities</span></span>
<span data-ttu-id="7d48f-170">Var būt svarīgi arī atļaut pielāgotajiem laukiem būt redzamiem datu elementos.</span><span class="sxs-lookup"><span data-stu-id="7d48f-170">It may also be important to allow custom fields to be visible on data entities.</span></span> <span data-ttu-id="7d48f-171">Datu elementi tiek izmantoti līdzeklī [Atvērt programmu komplektā Office](../../dev-itpro/office-integration/office-integration.md), kā arī datu importēšanas/eksportēšanas scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="7d48f-171">Data entities are utilized in the [Open in Office](../../dev-itpro/office-integration/office-integration.md) feature, as well as for data import/export scenarios.</span></span>  

<span data-ttu-id="7d48f-172">Lai pielāgoto lauku sniegtu datu elementam, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="7d48f-172">Follow these steps to expose a custom field on a data entity:</span></span> 
1.   <span data-ttu-id="7d48f-173">Atlasiet pielāgoto lauku formā **Pielāgoti lauki**.</span><span class="sxs-lookup"><span data-stu-id="7d48f-173">Select the custom field on the **Custom fields** form.</span></span> 
2.   <span data-ttu-id="7d48f-174">Izvērsiet sadaļu **Elementi**, lai skatītu attiecīgo elementu kopu.</span><span class="sxs-lookup"><span data-stu-id="7d48f-174">Expand the **Entities** section to view the set of relevant entities.</span></span>  
3.   <span data-ttu-id="7d48f-175">Noklikšķiniet uz pogas **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="7d48f-175">Click the **Edit** button.</span></span>
4.   <span data-ttu-id="7d48f-176">Modificējiet lauku **Iespējot** atlasīšanai katram elementam, kam ir jāsniedz šis lauks.</span><span class="sxs-lookup"><span data-stu-id="7d48f-176">Modify the **Enabled** field to be selected for each entity that should expose this field.</span></span>  
5.   <span data-ttu-id="7d48f-177">Noklikšķiniet uz **Lietot izmaiņas**, lai saglabātu veiktās atlases.</span><span class="sxs-lookup"><span data-stu-id="7d48f-177">Click **Apply changes** to save your selections.</span></span>  

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a><span data-ttu-id="7d48f-178">Atļauja pielāgotos laukus parādīt citās valodās</span><span class="sxs-lookup"><span data-stu-id="7d48f-178">Allowing custom fields to be displayed in other languages</span></span>
<span data-ttu-id="7d48f-179">Tā kā pielāgotajiem laukiem, iespējams, vajadzēs piekļūt lietotājiem, kuri pārzina dažādas valodas, lapā **Pielāgoti lauki** nodrošināts mehānisms, kas pielāgotā lauka etiķeti un palīdzības tekstu ļauj iztulkot citās valodās.</span><span class="sxs-lookup"><span data-stu-id="7d48f-179">Because custom fields may need to be accessed by users in a variety of languages, the **Custom fields** page provides a mechanism to allow the label and help text for a custom field to be translated into other languages.</span></span>  

<span data-ttu-id="7d48f-180">Tālāk esošajās darbībās aprakstīts pielāgoto lauku tulkošanas process citās valodās.</span><span class="sxs-lookup"><span data-stu-id="7d48f-180">The following steps describe the process for translating custom fields in other languages:</span></span> 
1.   <span data-ttu-id="7d48f-181">Lapā **Pielāgoti lauki** atlasiet pielāgoto lauku.</span><span class="sxs-lookup"><span data-stu-id="7d48f-181">Select the custom field on the **Custom fields** page.</span></span> 
2.   <span data-ttu-id="7d48f-182">Darbību rūtī atlasiet pogu **Tulkojumi**.</span><span class="sxs-lookup"><span data-stu-id="7d48f-182">Select the **Translations** button in the Action Pane.</span></span> <span data-ttu-id="7d48f-183">Tiks atvērta nolaižamā izvēlne ar esošajiem šī lauka tulkojumiem.</span><span class="sxs-lookup"><span data-stu-id="7d48f-183">This will open a drop-down menu with existing translations for this field.</span></span>
3.   <span data-ttu-id="7d48f-184">Nolaižamajā izvēlnē **Valoda** parādīta to valodu kopa, kam jau ir nodrošināti tulkojumi.</span><span class="sxs-lookup"><span data-stu-id="7d48f-184">The **Language** drop-down menu shows the set of languages for which translations have already been provided.</span></span> 
     1.   <span data-ttu-id="7d48f-185">Ja vēlaties rediģēt esošu tulkojumu, izvēlnē atlasiet vajadzīgo valodu un modificējiet etiķetes un palīdzības teksta vērtības.</span><span class="sxs-lookup"><span data-stu-id="7d48f-185">If you want to edit an existing translation, select the desired language from the menu and modify the values for the label and help text.</span></span>  
     2.   <span data-ttu-id="7d48f-186">Ja to nevēlaties darīt, noklikšķiniet uz pogas **Pievienot valodu**, izvēlnē atlasiet vajadzīgo valodu un nodrošiniet tulkotās etiķetes un palīdzības teksta vērtības.</span><span class="sxs-lookup"><span data-stu-id="7d48f-186">Otherwise, click the **Add language** button, select the desired language from the menu, and then provide translated values for the label and help text.</span></span>  
4.   <span data-ttu-id="7d48f-187">Kad esat pabeidzis, noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7d48f-187">Click **OK** when you are finished.</span></span>  

### <a name="deleting-custom-fields"></a><span data-ttu-id="7d48f-188">Pielāgoto lauku dzēšana</span><span class="sxs-lookup"><span data-stu-id="7d48f-188">Deleting custom fields</span></span>
<span data-ttu-id="7d48f-189">Dažos retos gadījumos varat izlemt, ka pielāgotais lauks vairs nav vajadzīgs.</span><span class="sxs-lookup"><span data-stu-id="7d48f-189">In some rare cases, you may decide that a custom field is no longer needed.</span></span> <span data-ttu-id="7d48f-190">Ja tā notiek, sistēmas administrators var izvēlēties dzēst šo lauku no lapas **Pielāgoti lauki**.</span><span class="sxs-lookup"><span data-stu-id="7d48f-190">When this occurs, a system administrator can choose to delete the field from the **Custom fields** page.</span></span> <span data-ttu-id="7d48f-191">Lai to izdarītu, pārliecinieties, vai ir atlasīts pareizais lauks, noklikšķiniet uz **Dzēst**, noklikšķiniet uz **Jā**, lai apstiprinātu dzēšanu, pēc tam noklikšķiniet uz **Lietot izmaiņas**.</span><span class="sxs-lookup"><span data-stu-id="7d48f-191">To do this, ensure the correct field is selected, click **Delete**, click **Yes** to confirm the deletion, and finally click **Apply changes**.</span></span> 

> [!Note]
> <span data-ttu-id="7d48f-192">Šo darbību nevar atsaukt, un tās rezultātā ar lauku saistītie dati tiks neatgriezeniski izdzēsti no datu bāzes.</span><span class="sxs-lookup"><span data-stu-id="7d48f-192">This action cannot be undone, and will result in the data associated with the field being permanently deleted from the database.</span></span> 

## <a name="appendix"></a><span data-ttu-id="7d48f-193">Pielikums</span><span class="sxs-lookup"><span data-stu-id="7d48f-193">Appendix</span></span> 
### <a name="who-can-create-custom-fields"></a><span data-ttu-id="7d48f-194">Kas var izveidot pielāgotos laukus?</span><span class="sxs-lookup"><span data-stu-id="7d48f-194">Who can create custom fields?</span></span>
<span data-ttu-id="7d48f-195">Drošības apsvērumu dēļ pielāgotos laukus pēc noklusējuma var izveidot tikai sistēmas administratori.</span><span class="sxs-lookup"><span data-stu-id="7d48f-195">As a safeguard to the system, only system administrators are able to create custom fields by default.</span></span> <span data-ttu-id="7d48f-196">Taču prasmīgiem lietotājiem, kuriem pēc organizācijas ieskatiem tas ir nepieciešams, sistēmas administrators var piešķirt tiesības izveidot pielāgotos laukus, izmantojot drošības lomu **Prasmīgs izpildlaika pielāgošanas lietotājs**.</span><span class="sxs-lookup"><span data-stu-id="7d48f-196">However, those power users whom the organization deems necessary can be given rights to create custom fields by a system administrator using the **Runtime customization power user** security role.</span></span> <span data-ttu-id="7d48f-197">Lietotāji bez šīs drošības lomas nevarēs izveidot pielāgotos laukus, taču joprojām varēs skatīt citu lietotāju sistēmā pievienotos pielāgotos laukus un mijiedarboties ar tiem.</span><span class="sxs-lookup"><span data-stu-id="7d48f-197">Users without this security role will not be able to create custom fields, but will still be able to see and interact with custom fields added by other users in the system.</span></span>    

### <a name="what-tables-support-custom-fields"></a><span data-ttu-id="7d48f-198">Kādas tabulas atbalsta pielāgotos laukus?</span><span class="sxs-lookup"><span data-stu-id="7d48f-198">What tables support custom fields?</span></span>
<span data-ttu-id="7d48f-199">Veiktspējas un tehnisku iemeslu dēļ pielāgotos laukus pašlaik var pievienot tikai tabulām, kas atbilst tālāk norādītajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="7d48f-199">For performance and technical reasons, only tables that meet the following conditions currently allow custom fields to be added.</span></span>

- <span data-ttu-id="7d48f-200">Tabulai ir jābūt atzīmētai kā vienai no tālāk norādītajām grupām.</span><span class="sxs-lookup"><span data-stu-id="7d48f-200">The table must be tagged as one of these groups:</span></span> 
     -   <span data-ttu-id="7d48f-201">Grupa</span><span class="sxs-lookup"><span data-stu-id="7d48f-201">Group</span></span>
     -   <span data-ttu-id="7d48f-202">WorksheetHeader</span><span class="sxs-lookup"><span data-stu-id="7d48f-202">WorksheetHeader</span></span>
     -   <span data-ttu-id="7d48f-203">Galvenā</span><span class="sxs-lookup"><span data-stu-id="7d48f-203">Main</span></span>
     -   <span data-ttu-id="7d48f-204">Dažādi</span><span class="sxs-lookup"><span data-stu-id="7d48f-204">Miscellaneous</span></span>
     -   <span data-ttu-id="7d48f-205">Parametrs</span><span class="sxs-lookup"><span data-stu-id="7d48f-205">Parameter</span></span>
     -   <span data-ttu-id="7d48f-206">Atsauce</span><span class="sxs-lookup"><span data-stu-id="7d48f-206">Reference</span></span>
     -   <span data-ttu-id="7d48f-207">TransactionHeader</span><span class="sxs-lookup"><span data-stu-id="7d48f-207">TransactionHeader</span></span>
- <span data-ttu-id="7d48f-208">Tabula nedrīkst paplašināt citu tabulu.</span><span class="sxs-lookup"><span data-stu-id="7d48f-208">The table cannot not extend another table.</span></span>
- <span data-ttu-id="7d48f-209">Tabula nedrīkst būt atzīmēta kā sistēmas tabula.</span><span class="sxs-lookup"><span data-stu-id="7d48f-209">The table cannot be marked as a system table.</span></span>
- <span data-ttu-id="7d48f-210">Tabula nedrīkst būt pagaidu tabula.</span><span class="sxs-lookup"><span data-stu-id="7d48f-210">The table cannot be a temporary table.</span></span>
