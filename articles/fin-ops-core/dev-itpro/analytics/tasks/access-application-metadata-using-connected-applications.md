---
title: Piekļuve programmas metadatiem, izmantojot saistītās programmas
description: Šajā tēmā tiek skaidrots, kā Regulatory configuration service (RCS) lietotājs var izveidot jaunu Elektroniskā pārskata (ER) kartēšanu, izmantojot metadatus.
author: NickSelin
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0b113f0db1d44dc5fbda30e10d62ff939550f299
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748697"
---
# <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="17abc-103">Piekļuve programmas metadatiem, izmantojot saistītās programmas</span><span class="sxs-lookup"><span data-stu-id="17abc-103">Access application metadata by using connected applications</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="17abc-104">Nākamajās darbībās ir paskaidrots, kā Regulatory Configuration Service (RCS) lietotājs ar lomu “Sistēmas administrators” vai “Elektronisko pārskatu izstrādātājs” var noformēt jauna elektronisko pārskatu (Electronic reporting — ER) modeļa kartēšanu, izmantojot Finance and Operations metadatus.</span><span class="sxs-lookup"><span data-stu-id="17abc-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using metadata in Finance and Operations.</span></span> <span data-ttu-id="17abc-105">Programmas metadatiem jāpiekļūst tiešsaistē, izmantojot ar RCS saistīto programmu.</span><span class="sxs-lookup"><span data-stu-id="17abc-105">Application metadata will be accessed online by using the RCS connected application.</span></span> <span data-ttu-id="17abc-106">Parauga ER modeļa kartēšana jākonfigurē piekļuvei ārējās tirdzniecības transakcijām.</span><span class="sxs-lookup"><span data-stu-id="17abc-106">Sample ER model mapping will be configured to access foreign trade transactions.</span></span> <span data-ttu-id="17abc-107">Lai izpildītu tālāk norādītās darbības, pakalpojumā RCS vispirms izpildiet darbības, kas ir aprakstītas tēmā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="17abc-107">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="17abc-108">Ja neesat izpildījis tēmā [Piekļuve programmas metadatiem, izmantojot ER konfigurāciju](access-application-metadata-er-configuration.md) norādītās darbības, dodieties uz [Elektronisko pārskatu piemēru lapu](https://go.microsoft.com/fwlink/?linkid=862266), lai lejupielādētu un saglabātu šādas ER konfigurācijas: Ārējās tirdzniecības metadati.xml; Ārējās tirdzniecības modelis.xml; Ārējās tirdzniecības kartēšana.xml. Pēc tam izpildiet procedūras darbības.</span><span class="sxs-lookup"><span data-stu-id="17abc-108">If you have not completed the steps in the topic, [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md), go to the [Electronic reporting examples page](https://go.microsoft.com/fwlink/?linkid=862266) to download and save the following ER configurations: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml, and then complete the steps in the procedure.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="17abc-109">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="17abc-109">Prerequisites</span></span>
1. <span data-ttu-id="17abc-110">Dodieties uz **Visas darbvietas** > **Elektroniskie pārskati**.</span><span class="sxs-lookup"><span data-stu-id="17abc-110">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="17abc-111">Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam Litware, Inc. ir pieejams un ir atzīmēts kā **Aktīvs**.</span><span class="sxs-lookup"><span data-stu-id="17abc-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="17abc-112">Ja neredzat šo konfigurācijas nodrošinātāju, izpildiet darbības, kas ir aprakstītas procedūrā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="17abc-112">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="get-required-er-configurations"></a><span data-ttu-id="17abc-113">Nepieciešamo ER konfigurāciju iegūšana</span><span class="sxs-lookup"><span data-stu-id="17abc-113">Get required ER configurations</span></span>
1. <span data-ttu-id="17abc-114">Noklikšķiniet uz **Pārskatu veidošanas konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="17abc-114">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="17abc-115">Ja esat jau izpildījis darbības, kas ir aprakstītas procedūrā [Piekļuve programmas metadatiem, izmantojot ER konfigurāciju](access-application-metadata-er-configuration.md), jums jau ir visas nepieciešamās ER konfigurācijas (ārējās tirdzniecības metadatu, modeļa un kartēšanas konfigurācijas) pašreizējā RCS instancē.</span><span class="sxs-lookup"><span data-stu-id="17abc-115">If you already completed the steps in the [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md) procedure, you already have all necessary ER configurations (foreign trade metadata, model and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="17abc-116">Visas atlikušās šī apakšuzdevuma darbības varat izlaist.</span><span class="sxs-lookup"><span data-stu-id="17abc-116">You can skip all the remaining steps of this sub-task.</span></span> 
3. <span data-ttu-id="17abc-117">Noklikšķiniet uz **Maiņa**.</span><span class="sxs-lookup"><span data-stu-id="17abc-117">Click **Exchange**.</span></span> 
4. <span data-ttu-id="17abc-118">Noklikšķiniet uz **Ielādēt no XML faila**.</span><span class="sxs-lookup"><span data-stu-id="17abc-118">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="17abc-119">Noklikšķiniet uz **Pārlūkot** un atlasiet failu **Ārējās tirdzniecības metadati.xml**.</span><span class="sxs-lookup"><span data-stu-id="17abc-119">Click **Browse** and select the **Foreign trade metadata.xml** file.</span></span> 
6. <span data-ttu-id="17abc-120">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="17abc-120">Click **OK**.</span></span> 
7. <span data-ttu-id="17abc-121">Noklikšķiniet uz **Maiņa**.</span><span class="sxs-lookup"><span data-stu-id="17abc-121">Click **Exchange**.</span></span> 
8. <span data-ttu-id="17abc-122">Noklikšķiniet uz **Ielādēt no XML faila**.</span><span class="sxs-lookup"><span data-stu-id="17abc-122">Click **Load from XML file**.</span></span> 
9. <span data-ttu-id="17abc-123">Noklikšķiniet uz **Pārlūkot** un atlasiet failu **Ārējās tirdzniecības modelis.xml**.</span><span class="sxs-lookup"><span data-stu-id="17abc-123">Click **Browse** and select the **Foreign trade model.xml** file.</span></span> 
10. <span data-ttu-id="17abc-124">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="17abc-124">Click **OK**.</span></span> 
11. <span data-ttu-id="17abc-125">Noklikšķiniet uz **Maiņa**.</span><span class="sxs-lookup"><span data-stu-id="17abc-125">Click **Exchange**.</span></span> 
12. <span data-ttu-id="17abc-126">Noklikšķiniet uz **Ielādēt no XML faila**.</span><span class="sxs-lookup"><span data-stu-id="17abc-126">Click **Load from XML file**.</span></span> 
13. <span data-ttu-id="17abc-127">Noklikšķiniet uz **Pārlūkot** un atlasiet failu **Ārējās tirdzniecības kartēšana.xml**.</span><span class="sxs-lookup"><span data-stu-id="17abc-127">Click **Browse** and select the **Foreign trade mapping.xml** file.</span></span> 
14. <span data-ttu-id="17abc-128">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="17abc-128">Click **OK**.</span></span> 

## <a name="register-a-connected-application"></a><span data-ttu-id="17abc-129">Savienotas programmas reģistrēšana</span><span class="sxs-lookup"><span data-stu-id="17abc-129">Register a connected application</span></span>
1. <span data-ttu-id="17abc-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="17abc-130">Close the page.</span></span> 
2. <span data-ttu-id="17abc-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="17abc-131">Close the page.</span></span> 
3. <span data-ttu-id="17abc-132">Dodieties uz **Visas darbvietas** > **Elektroniskie pārskati**.</span><span class="sxs-lookup"><span data-stu-id="17abc-132">Go to **All workspaces** > **Electronic reporting**.</span></span> 
4. <span data-ttu-id="17abc-133">Noklikšķiniet uz **Savienotās programmas**.</span><span class="sxs-lookup"><span data-stu-id="17abc-133">Click **Connected applications**.</span></span> 
5. <span data-ttu-id="17abc-134">Pārliecinieties, vai konfigurētā programma ir Azure programma un ir pieejama pašreizējam RCS lietotājam.</span><span class="sxs-lookup"><span data-stu-id="17abc-134">Make sure that the configured application is Azure based and accessible for the current RCS user.</span></span> <span data-ttu-id="17abc-135">Turklāt pašreizējam RCS lietotājam ir arī jābūt piekļuvei atlasītājai programmai un ir jābūt reģistrētam kā šīs programmas lietotājam ar lomu, kas dod tam privilēģijas piekļūt programmas metadatiem.</span><span class="sxs-lookup"><span data-stu-id="17abc-135">It is also required that the current RCS user has access to the selected application and has been registered as a user of this application playing a role giving them privileges to access application's metadata.</span></span> 
6. <span data-ttu-id="17abc-136">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="17abc-136">Click **New**.</span></span> 
7. <span data-ttu-id="17abc-137">Laukā **Nosaukums** ierakstiet “MyConnectedApp”.</span><span class="sxs-lookup"><span data-stu-id="17abc-137">In the **Name** field, type 'MyConnectedApp'.</span></span> 
8. <span data-ttu-id="17abc-138">Laukā **Programma** ievadiet “https:// mycompany.operations.dynamics.com”.</span><span class="sxs-lookup"><span data-stu-id="17abc-138">In the **Application** field, type 'https:// mycompany.operations.dynamics.com'.</span></span> 
9. <span data-ttu-id="17abc-139">Laukā **Nomnieks** ievadiet 'mycompany.onmicrosoft.com'.</span><span class="sxs-lookup"><span data-stu-id="17abc-139">In the **Tenant** field, type 'mycompany.onmicrosoft.com'.</span></span> 
10. <span data-ttu-id="17abc-140">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="17abc-140">Click **Save**.</span></span> 
11. <span data-ttu-id="17abc-141">Kad tiek pārbaudīts savienojums ar konfigurēto programmu, lapā **Savienojuma izveide ar attālo programmu** noklikšķiniet uz saites **Noklikšķināt šeit, lai izveidotu savienojumu ar atlasīto attālo programmu**.</span><span class="sxs-lookup"><span data-stu-id="17abc-141">When you check connection to configured application, on the **Connect to remote application** page click **Click here to connect to selected remote application** link.</span></span> 
12. <span data-ttu-id="17abc-142">Noklikšķiniet uz **Pārbaudīt savienojumu**.</span><span class="sxs-lookup"><span data-stu-id="17abc-142">Click **Check connection**.</span></span> 
13. <span data-ttu-id="17abc-143">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="17abc-143">Click **Close**.</span></span> 
14. <span data-ttu-id="17abc-144">Ja savienojuma validācija ir izdevusies, pašreizējā režģī konfigurētajai programmai tiks atjaunināta versija un nomnieka informācija.</span><span class="sxs-lookup"><span data-stu-id="17abc-144">When the connection validation succeeded, version and tenant details will be updated for the configured application in the current grid.</span></span> 

## <a name="review-existing-model-mapping-configuration"></a><span data-ttu-id="17abc-145">Esošas ER modeļa kartēšanas konfigurācijas pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="17abc-145">Review existing model mapping configuration</span></span>
1. <span data-ttu-id="17abc-146">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="17abc-146">Close the page.</span></span> 
2. <span data-ttu-id="17abc-147">Noklikšķiniet uz **Pārskatu veidošanas konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="17abc-147">Click **Reporting configurations**.</span></span> 
3. <span data-ttu-id="17abc-148">Kokā izvērsiet sadaļu **Ārējās tirdzniecības modelis**.</span><span class="sxs-lookup"><span data-stu-id="17abc-148">In the tree, expand **Foreign trade model**.</span></span> 
4. <span data-ttu-id="17abc-149">Kokā atlasiet **Ārējās tirdzniecības modelis\Ārējās tirdzniecības kartēšana**.</span><span class="sxs-lookup"><span data-stu-id="17abc-149">In the tree, select **Foreign trade model\Foreign trade mapping**.</span></span> 
5. <span data-ttu-id="17abc-150">Izvērsiet sadaļu **Priekšnosacījumi**.</span><span class="sxs-lookup"><span data-stu-id="17abc-150">Expand the **Prerequisites** section.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="17abc-151">Pašlaik šī kartēšana attiecas uz metadatu konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="17abc-151">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="17abc-152">Izstrādājot šī modeļa kartēšanu, tiks piedāvāti šīs konfigurācijas programmas metadati.</span><span class="sxs-lookup"><span data-stu-id="17abc-152">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

6. <span data-ttu-id="17abc-153">Noklikšķiniet uz **Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="17abc-153">Click **Designer**.</span></span> 
7. <span data-ttu-id="17abc-154">Noklikšķiniet uz **Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="17abc-154">Click **Designer**.</span></span> 
8. <span data-ttu-id="17abc-155">Kokā atlasiet **Dynamics 365 for Operations\Tabulas ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="17abc-155">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
9. <span data-ttu-id="17abc-156">Noklikšķiniet uz **Pievienot sakni**.</span><span class="sxs-lookup"><span data-stu-id="17abc-156">Click **Add root**.</span></span> 
10. <span data-ttu-id="17abc-157">Laukā **Tabula** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="17abc-157">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="17abc-158">Pašlaik šī kartēšana attiecas uz metadatu konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="17abc-158">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="17abc-159">Izstrādājot šī modeļa kartēšanu, tiks piedāvāti šīs konfigurācijas programmas metadati.</span><span class="sxs-lookup"><span data-stu-id="17abc-159">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

11. <span data-ttu-id="17abc-160">Noklikšķiniet uz **Atcelt**.</span><span class="sxs-lookup"><span data-stu-id="17abc-160">Click **Cancel**.</span></span> 
12. <span data-ttu-id="17abc-161">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="17abc-161">Close the page.</span></span> 
13. <span data-ttu-id="17abc-162">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="17abc-162">Close the page.</span></span> 

## <a name="assign-connected-application-to-model-mapping"></a><span data-ttu-id="17abc-163">Savienotās programmas piešķiršana modeļa kartēšanai</span><span class="sxs-lookup"><span data-stu-id="17abc-163">Assign connected application to model mapping</span></span> 
1. <span data-ttu-id="17abc-164">Noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="17abc-164">Click **Edit**.</span></span> 
2. <span data-ttu-id="17abc-165">Atlasiet programmu **MyConnectedApp**.</span><span class="sxs-lookup"><span data-stu-id="17abc-165">Select **MyConnectedApp** application.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="17abc-166">Pašlaik šī kartēšana attiecas uz atlasītās savienotās programmas metadatiem.</span><span class="sxs-lookup"><span data-stu-id="17abc-166">Currently, this mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="17abc-167">Ja tā pati kartēšana attiecas vienlaikus uz metadatu konfigurāciju un uz savienoto programmu, tiks izmantoti savienotās programmas metadati.</span><span class="sxs-lookup"><span data-stu-id="17abc-167">When the same mapping refers to metadata configuration and connected application at the same time, metadata of the connected application will be used.</span></span> 

3. <span data-ttu-id="17abc-168">Noklikšķiniet uz **Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="17abc-168">Click **Designer**.</span></span> 
4. <span data-ttu-id="17abc-169">Noklikšķiniet uz **Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="17abc-169">Click **Designer**.</span></span> 
5. <span data-ttu-id="17abc-170">Kokā atlasiet **Dynamics 365 for Operations\Tabulas ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="17abc-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
6. <span data-ttu-id="17abc-171">Noklikšķiniet uz **Pievienot sakni**.</span><span class="sxs-lookup"><span data-stu-id="17abc-171">Click **Add root**.</span></span> 
7. <span data-ttu-id="17abc-172">Laukā **Tabula** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="17abc-172">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="17abc-173">Tiek piedāvātas vairāk nekā divas programmas tabulas, jo šī kartēšana izmanto visus tai piešķirtās savienotās programmas metadatus.</span><span class="sxs-lookup"><span data-stu-id="17abc-173">More than two application tables were offered now as this mapping uses all the metadata of the connected application that has been assigned for it.</span></span> 

8. <span data-ttu-id="17abc-174">Noklikšķiniet uz **Atcelt**.</span><span class="sxs-lookup"><span data-stu-id="17abc-174">Click **Cancel**.</span></span> 
9. <span data-ttu-id="17abc-175">Noklikšķiniet uz **Validēt**.</span><span class="sxs-lookup"><span data-stu-id="17abc-175">Click **Validate**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="17abc-176">Datu modeļa elementi ir veiksmīgi saistīti ar datu avotu vienībām, kas aprakstītas, lietojot detalizētu informāciju par kartēšanai piešķirtās savienotās programmas metadatiem.</span><span class="sxs-lookup"><span data-stu-id="17abc-176">We successfully bound elements of data model with items of data sources that are described by using details of metadata of the connected application that has been assigned for this mapping.</span></span> 

10. <span data-ttu-id="17abc-177">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="17abc-177">Close the page.</span></span> 
11. <span data-ttu-id="17abc-178">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="17abc-178">Close the page.</span></span> 

<span data-ttu-id="17abc-179">Ja ir jānovērtē šī modeļa kartēšana, izmantojot citas versijas programmas metadatus, reģistrējiet citu savienoto programmu, piešķiriet to šai modeļa kartēšanai un validējiet to ar jauniem metadatiem.</span><span class="sxs-lookup"><span data-stu-id="17abc-179">When you need to evaluate this model mapping by using metadata of a different version application, register another connected application, assign it to this model mapping and validate it against new metadata.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]