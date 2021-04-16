---
title: Ieturētā nodokļa deklarācija Ēģiptei
description: Šajā tēmā paskaidrots, kā konfigurēt un ģenerēt ieturētā nodokļa deklarācijas Ēģiptei.
author: sndray
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4e3d68ac003fabaa504ffe81b8bf2f7ff8d7538d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839796"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a><span data-ttu-id="13b52-103">Ieturētā nodokļa deklarācija Ēģiptei (EG-00005)</span><span class="sxs-lookup"><span data-stu-id="13b52-103">Withholding tax declaration for Egypt (EG-00005)</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a><span data-ttu-id="13b52-104">Pārskats</span><span class="sxs-lookup"><span data-stu-id="13b52-104">Overview</span></span>
<span data-ttu-id="13b52-105">Šajā tēmā ir paskaidrots, kā iestatīt un ģenerēt ieturētā nodokļa deklarāciju un ieturētā nodokļa deklarācijas veidlapas Nr. 41 un 11 juridiskajām personām Ēģiptē</span><span class="sxs-lookup"><span data-stu-id="13b52-105">This topic explains how to set up and generate the withholding tax declaration and the withholding tax declaration forms 41 and 11 for legal entities in Egypt</span></span> 

<span data-ttu-id="13b52-106">Visiem Ēģiptes uzņēmumiem ir jāsagatavo veidlapa Nr. 41, kurā apkopoti visi nodokļi, kas tiek paturēti no vietējiem piegādātājiem un pakalpojumu sniedzējiem.</span><span class="sxs-lookup"><span data-stu-id="13b52-106">All Egyptian entities must prepare the form  41 which summarizes all taxes that are retained from local suppliers and service providers.</span></span> <span data-ttu-id="13b52-107">Papildus veidlapai Nr. 41 ir jāizveido veidlapa Nr. 11, lai detalizētu visus ieturētos nodokļus no ārvalstu pakalpojumu sniedzējiem.</span><span class="sxs-lookup"><span data-stu-id="13b52-107">In addition to form 41, form 11 must be generated to detail all of the retained taxed from foreign providers.</span></span> 

<span data-ttu-id="13b52-108">**Ieturētā nodokļa deklarācijas** pārskatā programmā Dynamics 365 Finance ir iekļauti tālāk minētie pārskati.</span><span class="sxs-lookup"><span data-stu-id="13b52-108">The **Withholding tax declaration** report in Dynamics 365 Finance includes the following reports:</span></span>

- <span data-ttu-id="13b52-109">Deklarācijas veidlapa Nr.</span><span class="sxs-lookup"><span data-stu-id="13b52-109">Declaration form No.</span></span> <span data-ttu-id="13b52-110">41</span><span class="sxs-lookup"><span data-stu-id="13b52-110">41</span></span>
- <span data-ttu-id="13b52-111">Deklarācijas veidlapa Nr.</span><span class="sxs-lookup"><span data-stu-id="13b52-111">Declaration form No.</span></span> <span data-ttu-id="13b52-112">11.</span><span class="sxs-lookup"><span data-stu-id="13b52-112">11</span></span>
    
    
## <a name="prerequisites"></a><span data-ttu-id="13b52-113">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="13b52-113">Prerequisites</span></span>
<span data-ttu-id="13b52-114">Juridiskās personas primārajai adresei ir jāatrodas Ēģiptē.</span><span class="sxs-lookup"><span data-stu-id="13b52-114">The primary address of the legal entity must be in Egypt.</span></span>
<span data-ttu-id="13b52-115">Darbvietā **Līdzekļu pārvaldība** ir jāiespējo tālāk norādītais līdzeklis.</span><span class="sxs-lookup"><span data-stu-id="13b52-115">In the **Feature management** workspace, the following feature must be enabled:</span></span>

   - <span data-ttu-id="13b52-116">**Globālais ieturētais nodoklis**</span><span class="sxs-lookup"><span data-stu-id="13b52-116">**Global withholding tax**</span></span>

<span data-ttu-id="13b52-117">Papildinformāciju par līdzekļu iespējošanu skatiet rakstā [Pārskats par līdzekļu pārvaldību.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span><span class="sxs-lookup"><span data-stu-id="13b52-117">For more information about how to enable features, see [Feature management overview.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span></span>

1. <span data-ttu-id="13b52-118">Atveriet **Nodoklis** > **Iestatīšana** > **Parametri** > **Virsgrāmatas parametri** un cilnē **Ieturētais nodoklis** iestatiet **Iespējot globālo ieturēto nodokli** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="13b52-118">Go to **Tax** > **Setup** > **Parameters** > **General ledger parameters**, and on the **Withholding tax** tab, set **Enable global withholding tax** to **Yes**.</span></span>
2. <span data-ttu-id="13b52-119">Darbvietā **Elektronisko pārskatu sniegšana** no repozitorija importējiet elektronisko pārskatu formātus:</span><span class="sxs-lookup"><span data-stu-id="13b52-119">In the **Electronic reporting** workspace, import the following Electronic reporting formats from the repository:</span></span>

    - <span data-ttu-id="13b52-120">WHT deklarācija Excel (EG)</span><span class="sxs-lookup"><span data-stu-id="13b52-120">WHT Declaration Excel (EG)</span></span>

    > [!NOTE]
    > <span data-ttu-id="13b52-121">Iepriekš minētais formāts ir balstīts uz **Nodokļu deklarēšanas modeli** un tas izmanto **Nodokļu deklarācijas modeļa kartējumu**.</span><span class="sxs-lookup"><span data-stu-id="13b52-121">The format above is based on the **Tax declaration model** and uses the **Tax declaration model mapping**.</span></span> <span data-ttu-id="13b52-122">Šī papildu konfigurācija tiek importēta automātiski.</span><span class="sxs-lookup"><span data-stu-id="13b52-122">This additional configuration is automatically imported.</span></span>

<span data-ttu-id="13b52-123">Papildinformāciju par elektronisko pārskatu konfigurāciju importēšanu skatiet sadaļā [Elektronisko pārskatu konfigurāciju lejupielāde no Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="13b52-123">For more information about how to import Electronic reporting configurations, see [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

## <a name="download-electronic-reporting-configurations"></a><span data-ttu-id="13b52-124">Elektronisko atskaišu veidošanas konfigurāciju lejupielāde</span><span class="sxs-lookup"><span data-stu-id="13b52-124">Download Electronic reporting configurations</span></span>

<span data-ttu-id="13b52-125">WHT deklarācijas veidlapu no Ēģiptes īstenošana ir balstīta uz elektronisko pārskatu (ER) konfigurācijām.</span><span class="sxs-lookup"><span data-stu-id="13b52-125">The implementation of the WHT declaration forms for Egypt is based on Electronic reporting (ER) configurations.</span></span> <span data-ttu-id="13b52-126">Papildinformāciju par konfigurējamām pārskata iespējām un koncepcijām skatiet sadaļā [Elektronisko pārskatu sniegšana](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="13b52-126">For more information about the capabilities and concepts of configurable reporting, see [Electronic reporting](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span></span>

<span data-ttu-id="13b52-127">Informācijai par ražošanas un lietotāju pieņemšanas testēšanas (UAT) vidēm skatiet instrukcijas tēmā [Elektronisko pārskatu konfigurāciju lejupielāde no Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="13b52-127">For production and user acceptance testing (UAT) environments, follow the instructions in the topic, [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

<span data-ttu-id="13b52-128">Lai ģenerētu ieturētās deklarācijas Ēģiptes juridiskajā personām, jāielādē šādas konfigurācijas:</span><span class="sxs-lookup"><span data-stu-id="13b52-128">To generate the Withholding declarations in an Egyptian legal entity, you need to upload the following configurations:</span></span>

- <span data-ttu-id="13b52-129">Nodokļu deklarācijas model.version.82.xml vai jaunāka versija</span><span class="sxs-lookup"><span data-stu-id="13b52-129">Tax declaration model.version.82.xml or later version</span></span>
- <span data-ttu-id="13b52-130">Nodokļu deklarācijas modeļa mapping.version.82.133.xml vai jaunāka versija</span><span class="sxs-lookup"><span data-stu-id="13b52-130">Tax declaration model mapping.version.82.133.xml or a later version</span></span>
- <span data-ttu-id="13b52-131">WHT deklarācijas Excel (EG).version.82.21 vai jaunāka versija</span><span class="sxs-lookup"><span data-stu-id="13b52-131">WHT Declaration Excel (EG).version.82.21  or a later version</span></span>

<span data-ttu-id="13b52-132">Pēc ER konfigurāciju lejupielādes no Lifecycle Services (LCS) vai globālā repozitorija pabeigšanas veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="13b52-132">After you finish downloading the ER configurations from Lifecycle Services (LCS) or the global repository, complete the following steps.</span></span>

1. <span data-ttu-id="13b52-133">Pārejiet uz darbvietu **Elektroniskie pārskati** un atlasiet elementu **Pārskatu veidošanas konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="13b52-133">Go to the **Electronic reporting** workspace and select the **Reporting configurations** tile.</span></span>
1. <span data-ttu-id="13b52-134">Lapas **Konfigurācijas** darbību rūtī atlasiet **Valūta > Ielādēt no XML faila**.</span><span class="sxs-lookup"><span data-stu-id="13b52-134">On the **Configurations** page, on the Action Pane, select **Exchange > Load from XML file**.</span></span>
1. <span data-ttu-id="13b52-135">Augšupielādējiet visus failus tādā secībā, kādā tie ir uzskaitīti iepriekšējās biļetenos.</span><span class="sxs-lookup"><span data-stu-id="13b52-135">Upload all the files in the order in which they are listed in the previous bullets.</span></span> <span data-ttu-id="13b52-136">Kad visas konfigurācijas ir augšupielādētas, konfigurācijas kokam ir jābūt redzamam programmā Finance.</span><span class="sxs-lookup"><span data-stu-id="13b52-136">After all of the configurations are uploaded, the configuration tree should be present in Finance.</span></span>

## <a name="set-up-application-specific-parameters"></a><span data-ttu-id="13b52-137">Programmai raksturīgu parametru iestatīšana</span><span class="sxs-lookup"><span data-stu-id="13b52-137">Set up application-specific parameters</span></span>

<span data-ttu-id="13b52-138">Programmai raksturīgo parametru opcija ļauj lietotājiem izveidot kritērijus, kā nodokļu darījumi tiek klasificēti un aprēķināti katrā ģenerētā pārskata rindā atkarībā no **ieturētā nodokļa krājumu grupas** konfigurācijas vai citiem kritērijiem, kas noteikti uzmeklēšanas definīcijā.</span><span class="sxs-lookup"><span data-stu-id="13b52-138">The application-specific parameters option lets users establish the criteria of how the tax transactions will be classified and calculated in each line of a generated report depending on the configuration of **withholding tax item group** or other criteria established in the definition of lookup.</span></span>

<span data-ttu-id="13b52-139">Ieturētās deklarācijas veidlapā Nr. 41 ir iekļauta noteikta kolonna, kur ieturētā nodokļa darījums ir jāklasificē saskaņā ar nodokļu iestādes klasifikāciju ar nosaukumu **Atlaides koda veids**.</span><span class="sxs-lookup"><span data-stu-id="13b52-139">Withholding declaration form 41 includes a specific column where the withholding tax transaction must be classified in accordance with the tax authority classification named **Discount code type**.</span></span> <span data-ttu-id="13b52-140">Tā vietā, lai šīs jaunās klasifikācijas iekļautu kā jaunus ierakstu datus, grāmatojot darbības, klasifikācijas tiks noteiktas, pamatojoties uz dažādām uzmeklēšanām, kas ieviestas **Konfigurācijas** > **Programmai specifisku parametru iestatīšana** > **Iestatīšana**, lai izpildītu ieturēšanas pārskatu prasības Ēģiptei.</span><span class="sxs-lookup"><span data-stu-id="13b52-140">Instead of including these new classifications as new entry data when the transactions are posted, the classifications will be determined based on the different lookups introduced in **Configurations** > **Set up application-specific parameters** > **Setup** to meet the requirements of withholding reports for Egypt.</span></span> 

<span data-ttu-id="13b52-141">Šī konfigurācija tiek izmantota, lai klasificētu darījumus Ieturētās deklarācijas veidlapas Nr. 41 pārskatā:</span><span class="sxs-lookup"><span data-stu-id="13b52-141">The following configuration is used to classify the transactions in the Withholding declaration form 41 report:</span></span>

- <span data-ttu-id="13b52-142">**DiscountTaxTypeLookup** -> kolonna Nr. 18</span><span class="sxs-lookup"><span data-stu-id="13b52-142">**DiscountTaxTypeLookup**-> Column No 18</span></span> 

<span data-ttu-id="13b52-143">Veiciet tālāk norādītās darbības, lai iestatītu dažādās uzmeklēšanas, kas tiek izmantotas WHT deklarācijas un saistīto grāmatu pārskatu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="13b52-143">Complete the following steps to set up the different lookups used to generate the WHT declaration and related books reports.</span></span> 

1. <span data-ttu-id="13b52-144">Darbvietā **Elektronisko pārskatu sniegšana** atlasiet **Konfigurācijas** > **Iestatījumi**, lai iestatītu kārtulas, kas nosaka, kā identificēt to, kā darījumi tiek klasificēti WHT deklarācijas pārskatā.</span><span class="sxs-lookup"><span data-stu-id="13b52-144">In the **Electronic reporting** workspace, select **Configurations** > **Setup** to set up the rules to identify how transactions are classified in the WHT declaration report.</span></span> 
2. <span data-ttu-id="13b52-145">Atlasiet pašreizējo versiju un kopsavilkuma cilnē **Uzmeklēšanas** atlasiet uzmeklēšanas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="13b52-145">Select the current version, and on the **Lookups** FastTab, select the lookup name.</span></span> <span data-ttu-id="13b52-146">Piemēram, **DiscountTaxTypeLookup**.</span><span class="sxs-lookup"><span data-stu-id="13b52-146">For example, **DiscountTaxTypeLookup**.</span></span> <span data-ttu-id="13b52-147">Šī uzmeklēšana identificē nodokļu iestādes pieprasīto atlaižu veidu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="13b52-147">This lookup identifies the list of discount types required by the tax authority.</span></span>
3. <span data-ttu-id="13b52-148">Kopsavilkuma cilnē **Nosacījumi** atlasiet **Pievienot** un jaunajā rindā kolonnā **Uzmeklēšanas rezultāti** atlasiet saistīto rindu, kas apzīmē klasifikāciju **18. kolonnā**.</span><span class="sxs-lookup"><span data-stu-id="13b52-148">On the **Conditions** FastTab, select **Add** and in the new line in the **Lookup result** column, select the related line that represents the classification in the **Column 18**.</span></span>
4. <span data-ttu-id="13b52-149">Kolonnā **Ieturētā nodokļa krājumu grupa** atlasiet saistīto kodu, kas tiek izmantots klasifikācijas identificēšanai.</span><span class="sxs-lookup"><span data-stu-id="13b52-149">In the **Withholding tax item group** column, select the related code that's used to identify the classification.</span></span> <span data-ttu-id="13b52-150">Piemēram, **Atļautā atlaide**.</span><span class="sxs-lookup"><span data-stu-id="13b52-150">For example, **Allowed discount**.</span></span>  
5. <span data-ttu-id="13b52-151">Atkārtojiet 3. un 4. darbību visām pieejamajām uzmeklēšanām.</span><span class="sxs-lookup"><span data-stu-id="13b52-151">Repeat steps 3 and 4 for all available lookups.</span></span>
6. <span data-ttu-id="13b52-152">Vēlreiz atlasiet **Pievienot**, lai ietvertu galīgo ieraksta rindu, un kolonnā **Uzmeklēšanas rezultāti** atlasiet **Nav attiecināms**.</span><span class="sxs-lookup"><span data-stu-id="13b52-152">Select **Add** again to include the final record line, and in the **Lookup result** column, select **Not applicable**.</span></span> 
7. <span data-ttu-id="13b52-153">Atlikušajās kolonnās atlasiet **Nav tukšs**.</span><span class="sxs-lookup"><span data-stu-id="13b52-153">In the remaining columns, select **Not blank**.</span></span> 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a><span data-ttu-id="13b52-154">Virsgrāmatas parametru iestatīšana</span><span class="sxs-lookup"><span data-stu-id="13b52-154">Set up General ledger parameters</span></span>

<span data-ttu-id="13b52-155">Lai izveidotu WHT deklarācijas veidlapas pārskatus Microsoft Excel, definējiet ER formātu lapā **Virsgrāmatas parametri**.</span><span class="sxs-lookup"><span data-stu-id="13b52-155">To generate the WHT declaration form reports in Microsoft Excel, define an ER format on the **General ledger parameters** page.</span></span>

1. <span data-ttu-id="13b52-156">Atveriet **Nodoklis** > **Iestatīšana** > **Virsgrāmatas parametri**.</span><span class="sxs-lookup"><span data-stu-id="13b52-156">Go to **Tax** > **Setup** > **General ledger parameters**.</span></span>
2. <span data-ttu-id="13b52-157">Cilnes **Ieturētais nodoklis** laukā **WHT deklarācijas formāta kartēšana** atlasiet **WHT deklarācija Excel (EG)**.</span><span class="sxs-lookup"><span data-stu-id="13b52-157">On the **Withholding tax** tab, in the **WHT declaration format mapping** field, select **WHT Declaration Excel (EG)**.</span></span> <span data-ttu-id="13b52-158">Ja šo lauku atstājat tukšu, standarta PVN pārskats tiks ģenerēts SSRS formātā.</span><span class="sxs-lookup"><span data-stu-id="13b52-158">If you leave the field blank, the standard sales tax report will be generated in SSRS format.</span></span>


![Deklarācijas veidlapa](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a><span data-ttu-id="13b52-160">Ģenerēt ieturētās deklarācijas veidlapas</span><span class="sxs-lookup"><span data-stu-id="13b52-160">Generate the Withholding declaration forms</span></span>
<span data-ttu-id="13b52-161">Ieturētā nodokļa deklarācijas veidlapas sagatavošanas un iesniegšanas process noteiktam periodam ir balstīts uz ieturētā nodokļa darījumiem, kas grāmatoti apmaksas un iegrāmatošanas maksājuma nodokļa darba laikā.</span><span class="sxs-lookup"><span data-stu-id="13b52-161">The process of preparing and submitting a Withholding declaration form for a specific period is based on the withholding tax transactions posted during the settle and post payment tax job.</span></span> <span data-ttu-id="13b52-162">Plašāku informāciju par globālo ieturēto nodokli skatiet sadaļā [Globālais ieturētais nodoklis](../general-ledger/global-withholding-tax-overview.md).</span><span class="sxs-lookup"><span data-stu-id="13b52-162">For more information about global withholding tax, see [Global withholding tax](../general-ledger/global-withholding-tax-overview.md).</span></span>

<span data-ttu-id="13b52-163">Lai ģenerētu nodokļu deklarācijas pārskatu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="13b52-163">Complete the following steps to generate the tax declaration report.</span></span>

1. <span data-ttu-id="13b52-164">Atveriet **Nodoklis** > **Deklarācijas** > **Ieturētais nodoklis** > \**Ieturētā nodokļa maksājums*.</span><span class="sxs-lookup"><span data-stu-id="13b52-164">Go to **Tax** > **Declarations** > **Withholding tax** > \**Withholding tax payment*.</span></span>
2. <span data-ttu-id="13b52-165">Atlasiet apmaksas periodu un pēc tam atlasiet pārskata sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="13b52-165">Select the settlement period and then select the from date for the report.</span></span> 
3. <span data-ttu-id="13b52-166">Ievadiet darījuma datumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="13b52-166">Enter the transaction date and then select **OK**.</span></span>
4. <span data-ttu-id="13b52-167">Atvērtajā dialoglodziņā atlasiet vienu vai vairākus veidlapu veidus **Veidlapa Nr. 41**, **Veidlapa Nr. 11** vai **Neviens**.</span><span class="sxs-lookup"><span data-stu-id="13b52-167">In the dialog box that opens, select one or more of the form types \*\*Form No 41 \*\*, **Form No 11**, or **None**.</span></span> <span data-ttu-id="13b52-168">Ja atlasāt **Neviens**, tiek ģenerēts standarta pārskats.</span><span class="sxs-lookup"><span data-stu-id="13b52-168">If you select **None**, the standard report is generated.</span></span> 
5. <span data-ttu-id="13b52-169">Atlasiet valodu.</span><span class="sxs-lookup"><span data-stu-id="13b52-169">Select the language.</span></span> <span data-ttu-id="13b52-170">Visi pārskati tiek tulkoti **en-us** un **ar-eg**.</span><span class="sxs-lookup"><span data-stu-id="13b52-170">All reports are translated in **en-us** and **ar-eg**.</span></span>
6. <span data-ttu-id="13b52-171">Ievadiet bankas filiāli un nosaukumu, kur tiks veikts nodokļu maksājums.</span><span class="sxs-lookup"><span data-stu-id="13b52-171">Enter the branch and name of the bank where the tax payment will be paid.</span></span>
7. <span data-ttu-id="13b52-172">Atlasiet biznesa veidu un tad ievadiet čeka un dokumenta numurus.</span><span class="sxs-lookup"><span data-stu-id="13b52-172">Select the business type and then enter the check and document numbers.</span></span> 
8. <span data-ttu-id="13b52-173">Ievadiet entītijas veidu.</span><span class="sxs-lookup"><span data-stu-id="13b52-173">Enter the entity type.</span></span> 
9. <span data-ttu-id="13b52-174">Ievadiet tās personas vārdu, kas reģistrēta, lai piešķirtu formu, un atlasiet **Labi**, lai apstiprinātu pārskata ģenerēšanu.</span><span class="sxs-lookup"><span data-stu-id="13b52-174">Enter the name of person registered to assign the form and select **OK** to confirm the report generation.</span></span> 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
