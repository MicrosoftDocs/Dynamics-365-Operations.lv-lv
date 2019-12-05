---
title: Piekļuve programmas metadatiem, izmantojot saistītās programmas
description: Šajā tēmā ietvertajās darbībās ir paskaidrots, kā Regulatory Configuration Service (RCS) lietotājs var noformēt jauna elektronisko pārskatu (Electronic Reporting — ER) modeļa kartēšanu, izmantojot Finance and Operations metadatus.
author: NickSelin
manager: AnnBe
ms.date: 06/29/2019
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
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5020b523ca5d76d36f7436a8f43e8629c029e3e8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769882"
---
# <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="fbdf7-103">Piekļuve programmas metadatiem, izmantojot saistītās programmas</span><span class="sxs-lookup"><span data-stu-id="fbdf7-103">Access application metadata by using connected applications</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fbdf7-104">Nākamajās darbībās ir paskaidrots, kā Regulatory Configuration Service (RCS) lietotājs ar lomu “Sistēmas administrators” vai “Elektronisko pārskatu izstrādātājs” var noformēt jauna elektronisko pārskatu (Electronic reporting — ER) modeļa kartēšanu, izmantojot metadatus programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using metadata in Finance and Operations.</span></span> <span data-ttu-id="fbdf7-105">Programmas metadatiem jāpiekļūst tiešsaistē, izmantojot ar RCS saistīto programmu.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-105">Application metadata will be accessed online by using the RCS connected application.</span></span> <span data-ttu-id="fbdf7-106">Parauga ER modeļa kartēšana jākonfigurē piekļuvei ārējās tirdzniecības transakcijām.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-106">Sample ER model mapping will be configured to access foreign trade transactions.</span></span> <span data-ttu-id="fbdf7-107">Lai izpildītu tālāk norādītās darbības, pakalpojumā RCS vispirms izpildiet darbības, kas ir aprakstītas tēmā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="fbdf7-107">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="fbdf7-108">Ja neesat izpildījis tēmā [Piekļuve programmas metadatiem, izmantojot ER konfigurāciju](access-application-metadata-er-configuration.md) norādītās darbības, dodieties uz [Elektronisko pārskatu piemēru lapu](https://go.microsoft.com/fwlink/?linkid=862266), lai lejupielādētu un saglabātu šādas ER konfigurācijas: Ārējās tirdzniecības metadati.xml; Ārējās tirdzniecības modelis.xml; Ārējās tirdzniecības kartēšana.xml. Pēc tam izpildiet procedūras darbības.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-108">If you have not completed the steps in the topic, [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md), go to the [Electronic reporting examples page](https://go.microsoft.com/fwlink/?linkid=862266) to download and save the following ER configurations: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml, and then complete the steps in the procedure.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fbdf7-109">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="fbdf7-109">Prerequisites</span></span>
1. <span data-ttu-id="fbdf7-110">Dodieties uz **Visas darbvietas** > **Elektroniskie pārskati**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-110">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="fbdf7-111">Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam Litware, Inc. ir pieejams un ir atzīmēts kā **Aktīvs**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="fbdf7-112">Ja neredzat šo konfigurācijas nodrošinātāju, izpildiet darbības, kas ir aprakstītas procedūrā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="fbdf7-112">If you don’t see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="get-required-er-configurations"></a><span data-ttu-id="fbdf7-113">Nepieciešamo ER konfigurāciju iegūšana</span><span class="sxs-lookup"><span data-stu-id="fbdf7-113">Get required ER configurations</span></span>
1. <span data-ttu-id="fbdf7-114">Noklikšķiniet uz **Pārskatu veidošanas konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-114">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="fbdf7-115">Ja esat jau izpildījis darbības, kas ir aprakstītas procedūrā [Piekļuve programmas metadatiem, izmantojot ER konfigurāciju](access-application-metadata-er-configuration.md), jums jau ir visas nepieciešamās ER konfigurācijas (ārējās tirdzniecības metadatu, modeļa un kartēšanas konfigurācijas) pašreizējā RCS instancē.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-115">If you already completed the steps in the [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md) procedure, you already have all necessary ER configurations (foreign trade metadata, model and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="fbdf7-116">Visas atlikušās šī apakšuzdevuma darbības varat izlaist.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-116">You can skip all the remaining steps of this sub-task.</span></span> 
3. <span data-ttu-id="fbdf7-117">Noklikšķiniet uz **Maiņa**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-117">Click **Exchange**.</span></span> 
4. <span data-ttu-id="fbdf7-118">Noklikšķiniet uz **Ielādēt no XML faila**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-118">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="fbdf7-119">Noklikšķiniet uz **Pārlūkot** un atlasiet failu **Ārējās tirdzniecības metadati.xml**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-119">Click **Browse** and select the **Foreign trade metadata.xml** file.</span></span> 
6. <span data-ttu-id="fbdf7-120">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-120">Click **OK**.</span></span> 
7. <span data-ttu-id="fbdf7-121">Noklikšķiniet uz **Maiņa**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-121">Click **Exchange**.</span></span> 
8. <span data-ttu-id="fbdf7-122">Noklikšķiniet uz **Ielādēt no XML faila**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-122">Click **Load from XML file**.</span></span> 
9. <span data-ttu-id="fbdf7-123">Noklikšķiniet uz **Pārlūkot** un atlasiet failu **Ārējās tirdzniecības modelis.xml**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-123">Click **Browse** and select the **Foreign trade model.xml** file.</span></span> 
10. <span data-ttu-id="fbdf7-124">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-124">Click **OK**.</span></span> 
11. <span data-ttu-id="fbdf7-125">Noklikšķiniet uz **Maiņa**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-125">Click **Exchange**.</span></span> 
12. <span data-ttu-id="fbdf7-126">Noklikšķiniet uz **Ielādēt no XML faila**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-126">Click **Load from XML file**.</span></span> 
13. <span data-ttu-id="fbdf7-127">Noklikšķiniet uz **Pārlūkot** un atlasiet failu **Ārējās tirdzniecības kartēšana.xml**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-127">Click **Browse** and select the **Foreign trade mapping.xml** file.</span></span> 
14. <span data-ttu-id="fbdf7-128">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-128">Click **OK**.</span></span> 

## <a name="register-a-connected-application"></a><span data-ttu-id="fbdf7-129">Savienotas programmas reģistrēšana</span><span class="sxs-lookup"><span data-stu-id="fbdf7-129">Register a connected application</span></span>
1. <span data-ttu-id="fbdf7-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-130">Close the page.</span></span> 
2. <span data-ttu-id="fbdf7-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-131">Close the page.</span></span> 
3. <span data-ttu-id="fbdf7-132">Dodieties uz **Visas darbvietas** > **Elektroniskie pārskati**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-132">Go to **All workspaces** > **Electronic reporting**.</span></span> 
4. <span data-ttu-id="fbdf7-133">Noklikšķiniet uz **Savienotās programmas**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-133">Click **Connected applications**.</span></span> 
5. <span data-ttu-id="fbdf7-134">Pārliecinieties, vai konfigurētā programma ir Azure programma un ir pieejama pašreizējam RCS lietotājam.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-134">Make sure that the configured application is Azura based and accessible for the current RCS user.</span></span> <span data-ttu-id="fbdf7-135">Turklāt pašreizējam RCS lietotājam ir arī jābūt piekļuvei atlasītajai programmai un ir jābūt reģistrētam kā šīs programmas lietotājam ar lomu, kas dod viņam privilēģijas piekļūt programmas metadatiem.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-135">It is also required that the current RCS user has access to the selected application and has been registered as a user of this application playing a role giving him privileges to access application’s metadata.</span></span> 
6. <span data-ttu-id="fbdf7-136">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-136">Click **New**.</span></span> 
7. <span data-ttu-id="fbdf7-137">Laukā **Nosaukums** ierakstiet “MyConnectedApp”.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-137">In the **Name** field, type 'MyConnectedApp'.</span></span> 
8. <span data-ttu-id="fbdf7-138">Laukā **Programma** ievadiet “https:// mycompany.operations.dynamics.com”.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-138">In the **Application** field, type 'https:// mycompany.operations.dynamics.com'.</span></span> 
9. <span data-ttu-id="fbdf7-139">Laukā **Nomnieks** ievadiet “mycompany.onmicrosoft.com”.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-139">In the **Tenant** field, type ‘mycompany.onmicrosoft.com’.</span></span> 
10. <span data-ttu-id="fbdf7-140">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-140">Click **Save**.</span></span> 
11. <span data-ttu-id="fbdf7-141">Kad tiek pārbaudīts savienojums ar konfigurēto programmu, lapā **Savienojuma izveide ar attālo programmu** noklikšķiniet uz saites **Noklikšķināt šeit, lai izveidotu savienojumu ar atlasīto attālo programmu**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-141">When you check connection to configured application, on the **Connect to remote application** page click **Click here to connect to selected remote application** link.</span></span> 
12. <span data-ttu-id="fbdf7-142">Noklikšķiniet uz **Pārbaudīt savienojumu**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-142">Click **Check connection**.</span></span> 
13. <span data-ttu-id="fbdf7-143">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-143">Click **Close**.</span></span> 
14. <span data-ttu-id="fbdf7-144">Ja savienojuma validācija ir izdevusies, pašreizējā režģī konfigurētajai programmai tiks atjaunināta versija un nomnieka informācija.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-144">When the connection validation succeeded, version and tenant details will be updated for the configured application in the current grid.</span></span> 

## <a name="review-existing-model-mapping-configuration"></a><span data-ttu-id="fbdf7-145">Esošas ER modeļa kartēšanas konfigurācijas pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="fbdf7-145">Review existing model mapping configuration</span></span>
1. <span data-ttu-id="fbdf7-146">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-146">Close the page.</span></span> 
2. <span data-ttu-id="fbdf7-147">Noklikšķiniet uz **Pārskatu veidošanas konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-147">Click **Reporting configurations**.</span></span> 
3. <span data-ttu-id="fbdf7-148">Kokā izvērsiet sadaļu **Ārējās tirdzniecības modelis**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-148">In the tree, expand **Foreign trade model**.</span></span> 
4. <span data-ttu-id="fbdf7-149">Kokā atlasiet **Ārējās tirdzniecības modelis\Ārējās tirdzniecības kartēšana**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-149">In the tree, select **Foreign trade model\Foreign trade mapping**.</span></span> 
5. <span data-ttu-id="fbdf7-150">Izvērsiet sadaļu **Priekšnosacījumi**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-150">Expand the **Prerequisites** section.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="fbdf7-151">Pašlaik šī kartēšana attiecas uz metadatu konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-151">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="fbdf7-152">Izstrādājot šī modeļa kartēšanu, tiks piedāvāti šīs konfigurācijas programmas metadati.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-152">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

6. <span data-ttu-id="fbdf7-153">Noklikšķiniet uz **Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-153">Click **Designer**.</span></span> 
7. <span data-ttu-id="fbdf7-154">Noklikšķiniet uz **Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-154">Click **Designer**.</span></span> 
8. <span data-ttu-id="fbdf7-155">Kokā atlasiet **Dynamics 365 for Operations\Tabulas ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-155">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
9. <span data-ttu-id="fbdf7-156">Noklikšķiniet uz **Pievienot sakni**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-156">Click **Add root**.</span></span> 
10. <span data-ttu-id="fbdf7-157">Laukā **Tabula** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-157">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="fbdf7-158">Pašlaik šī kartēšana attiecas uz metadatu konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-158">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="fbdf7-159">Izstrādājot šī modeļa kartēšanu, tiks piedāvāti šīs konfigurācijas programmas metadati.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-159">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

11. <span data-ttu-id="fbdf7-160">Noklikšķiniet uz **Atcelt**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-160">Click **Cancel**.</span></span> 
12. <span data-ttu-id="fbdf7-161">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-161">Close the page.</span></span> 
13. <span data-ttu-id="fbdf7-162">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-162">Close the page.</span></span> 

## <a name="assign-connected-application-to-model-mapping"></a><span data-ttu-id="fbdf7-163">Savienotās programmas piešķiršana modeļa kartēšanai</span><span class="sxs-lookup"><span data-stu-id="fbdf7-163">Assign connected application to model mapping</span></span> 
1. <span data-ttu-id="fbdf7-164">Noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-164">Click **Edit**.</span></span> 
2. <span data-ttu-id="fbdf7-165">Atlasiet programmu **MyConnectedApp**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-165">Select **MyConnectedApp** application.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="fbdf7-166">Pašlaik šī kartēšana attiecas uz atlasītās savienotās programmas metadatiem.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-166">Currently, this mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="fbdf7-167">Ja tā pati kartēšana attiecas vienlaikus uz metadatu konfigurāciju un uz savienoto programmu, tiks izmantoti savienotās programmas metadati.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-167">When the same mapping refers to metadata configuration and connected application at the same time, metadata of the connected application will be used.</span></span> 

3. <span data-ttu-id="fbdf7-168">Noklikšķiniet uz **Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-168">Click **Designer**.</span></span> 
4. <span data-ttu-id="fbdf7-169">Noklikšķiniet uz **Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-169">Click **Designer**.</span></span> 
5. <span data-ttu-id="fbdf7-170">Kokā atlasiet **Dynamics 365 for Operations\Tabulas ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
6. <span data-ttu-id="fbdf7-171">Noklikšķiniet uz **Pievienot sakni**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-171">Click **Add root**.</span></span> 
7. <span data-ttu-id="fbdf7-172">Laukā **Tabula** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-172">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="fbdf7-173">Tiek piedāvātas vairāk nekā divas programmas tabulas, jo šī kartēšana izmanto visus tai piešķirtās savienotās programmas metadatus.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-173">More than two application tables were offered now as this mapping uses all the metadata of the connected application that has been assigned for it.</span></span> 

8. <span data-ttu-id="fbdf7-174">Noklikšķiniet uz **Atcelt**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-174">Click **Cancel**.</span></span> 
9. <span data-ttu-id="fbdf7-175">Noklikšķiniet uz **Validēt**.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-175">Click **Validate**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="fbdf7-176">Datu modeļa elementi ir veiksmīgi saistīti ar datu avotu vienībām, kas aprakstītas, lietojot detalizētu informāciju par kartēšanai piešķirtās savienotās programmas metadatiem.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-176">We successfully bound elements of data model with items of data sources that are described by using details of metadata of the connected application that has been assigned for this mapping.</span></span> 

10. <span data-ttu-id="fbdf7-177">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-177">Close the page.</span></span> 
11. <span data-ttu-id="fbdf7-178">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-178">Close the page.</span></span> 

<span data-ttu-id="fbdf7-179">Ja ir jānovērtē šī modeļa kartēšana, izmantojot citas versijas programmas metadatus, reģistrējiet citu savienoto programmu, piešķiriet to šai modeļa kartēšanai un validējiet to ar jauniem metadatiem.</span><span class="sxs-lookup"><span data-stu-id="fbdf7-179">When you need to evaluate this model mapping by using metadata of a different version application, register another connected application, assign it to this model mapping and validate it against new metadata.</span></span>
