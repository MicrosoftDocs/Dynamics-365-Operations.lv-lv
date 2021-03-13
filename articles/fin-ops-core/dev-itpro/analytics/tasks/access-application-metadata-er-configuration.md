---
title: Piekļuve programmas metadatiem, izmantojot ER konfigurāciju
description: Šajā tēmā tiek skaidrots, kā Regulatoru configuration service (RCS) lietotājs var izveidot jaunu Elektroniskā pārskata (ER) kartēšanu, izmantojot metadatus.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58697148ecf83f4962bd64a221945b6d911e11a6
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093309"
---
# <a name="access-application-metadata-by-using-er-configuration"></a><span data-ttu-id="6287d-103">Piekļuve programmas metadatiem, izmantojot ER konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="6287d-103">Access application metadata by using ER configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6287d-104">Nākamajās darbībās ir paskaidrots, kā Regulatory Configuration Service (RCS) lietotājs ar lomu “Sistēmas administrators” vai “Elektronisko pārskatu izstrādātājs” var noformēt jauna elektronisko pārskatu (Electronic reporting — ER) modeļa kartēšanu, izmantojot programmas metadatus.</span><span class="sxs-lookup"><span data-stu-id="6287d-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using the application metadata.</span></span> <span data-ttu-id="6287d-105">Programmas metadatiem jāpiekļūst, izmantojot ER metadatu konfigurāciju, kas ietver metadatu paraugu kopu, lai piekļūtu ārējās tirdzniecības transakcijām.</span><span class="sxs-lookup"><span data-stu-id="6287d-105">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span> <span data-ttu-id="6287d-106">Lai izpildītu tālāk norādītās darbības, vispirms pakalpojumā RCS izpildiet darbības, kas ir aprakstītas procedūras tēmā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="6287d-106">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> <span data-ttu-id="6287d-107">Pēc tam izpildiet darbības, kas ir aprakstītas tēmā [Programmas metadatu sagatavošana lietošanai pakalpojumā RCS](prepare-application-metadata-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="6287d-107">Then complete the steps in the topic, [Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6287d-108">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="6287d-108">Prerequisites</span></span>
1. <span data-ttu-id="6287d-109">Dodieties uz **Visas darbvietas** > **Elektroniskie pārskati**.</span><span class="sxs-lookup"><span data-stu-id="6287d-109">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="6287d-110">Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam Litware, Inc. ir pieejams un ir atzīmēts kā **Aktīvs**.</span><span class="sxs-lookup"><span data-stu-id="6287d-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="6287d-111">Ja neredzat šo konfigurācijas nodrošinātāju, izpildiet darbības, kas ir aprakstītas procedūrā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="6287d-111">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="import-metadata-configuration"></a><span data-ttu-id="6287d-112">Metadatu konfigurācijas importēšana</span><span class="sxs-lookup"><span data-stu-id="6287d-112">Import metadata configuration</span></span> 
1. <span data-ttu-id="6287d-113">Noklikšķiniet uz **Metadatu konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="6287d-113">Click **Metadata configurations**.</span></span> 
2. <span data-ttu-id="6287d-114">Importējiet ER metadatu konfigurāciju, kas ir konfigurēta elektronisku dokumentu ģenerēšanai ārējās tirdzniecības uzņēmējdarbībai.</span><span class="sxs-lookup"><span data-stu-id="6287d-114">Import the ER metadata configuration that contains metadata that has been configured to generate electronic documents for foreign trade business.</span></span> <span data-ttu-id="6287d-115">Šī ER metadatu konfigurācija ir eksportēta kā XML fails, un procedūras [Programmas metadatu sagatavošana lietošanai pakalpojumā RCS](prepare-application-metadata-rcs.md) darbības ir izpildītas.</span><span class="sxs-lookup"><span data-stu-id="6287d-115">This ER metadata configuration has been exported as XML file while the steps in the [Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md) procedure have been completed.</span></span> 
3. <span data-ttu-id="6287d-116">Noklikšķiniet uz **Maiņa**.</span><span class="sxs-lookup"><span data-stu-id="6287d-116">Click **Exchange**.</span></span> 
4. <span data-ttu-id="6287d-117">Noklikšķiniet uz **Ielādēt no XML faila**.</span><span class="sxs-lookup"><span data-stu-id="6287d-117">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="6287d-118">Noklikšķiniet uz **Pārlūkot** un atlasiet failu 'Ārējās tirdzniecības metadati.xml'.</span><span class="sxs-lookup"><span data-stu-id="6287d-118">Click **Browse** and select the 'Foreign trade metadata.xml' file.</span></span> 
6. <span data-ttu-id="6287d-119">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6287d-119">Click **OK**.</span></span> 
7. <span data-ttu-id="6287d-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6287d-120">Close the page.</span></span> 

## <a name="create-data-model-configuration"></a><span data-ttu-id="6287d-121">Datu modeļa konfigurācijas izveide</span><span class="sxs-lookup"><span data-stu-id="6287d-121">Create data model configuration</span></span>
1. <span data-ttu-id="6287d-122">Noklikšķiniet uz **Pārskatu veidošanas konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="6287d-122">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="6287d-123">Noklikšķiniet uz **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="6287d-123">Click **Create configuration** to open the drop dialog.</span></span> 
3. <span data-ttu-id="6287d-124">Laukā **Nosaukums** ierakstiet “Ārējās tirdzniecības modelis”.</span><span class="sxs-lookup"><span data-stu-id="6287d-124">In the **Name** field, type 'Foreign trade model'.</span></span> 
4. <span data-ttu-id="6287d-125">Klikšķiniet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="6287d-125">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="6287d-126">Noklikšķiniet uz **Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="6287d-126">Click **Designer**.</span></span> 
6. <span data-ttu-id="6287d-127">Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="6287d-127">Click **New** to open the drop dialog.</span></span> 
7. <span data-ttu-id="6287d-128">Laukā **Nosaukums** ierakstiet “Sakne”.</span><span class="sxs-lookup"><span data-stu-id="6287d-128">In the **Name** field, type 'Root'.</span></span> 
8. <span data-ttu-id="6287d-129">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="6287d-129">Click **Add**.</span></span> 
9. <span data-ttu-id="6287d-130">Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="6287d-130">Click **New** to open the drop dialog.</span></span> 
10.    <span data-ttu-id="6287d-131">Laukā **Nosaukums** ierakstiet “Transakcija”.</span><span class="sxs-lookup"><span data-stu-id="6287d-131">In the **Name** field, type 'Transaction'.</span></span> 
11.    <span data-ttu-id="6287d-132">Laukā **Vienuma veids** atlasiet **Ierakstu saraksts**.</span><span class="sxs-lookup"><span data-stu-id="6287d-132">In the **Item type** field, select **Record list**.</span></span> 
12.    <span data-ttu-id="6287d-133">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="6287d-133">Click **Add**.</span></span> 
13.    <span data-ttu-id="6287d-134">Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="6287d-134">Click **New** to open the drop dialog.</span></span> 
14.    <span data-ttu-id="6287d-135">Laukā **Nosaukums** ierakstiet “Preces kods”.</span><span class="sxs-lookup"><span data-stu-id="6287d-135">In the **Name** field, type 'Commodity code'.</span></span> 
15.    <span data-ttu-id="6287d-136">Laukā **Vienuma veids** atlasiet **Virkne**.</span><span class="sxs-lookup"><span data-stu-id="6287d-136">In the **Item type** field, select **String**.</span></span> 
16.    <span data-ttu-id="6287d-137">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="6287d-137">Click **Add**.</span></span> 
17.    <span data-ttu-id="6287d-138">Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="6287d-138">Click **New** to open the drop dialog.</span></span> 
18.    <span data-ttu-id="6287d-139">Laukā **Nosaukums** ierakstiet “Rēķinā iekļautā summa”.</span><span class="sxs-lookup"><span data-stu-id="6287d-139">In the **Name** field, type 'Invoiced amount'.</span></span> 
19.    <span data-ttu-id="6287d-140">Laukā **Vienuma veids** atlasiet **Reāls**.</span><span class="sxs-lookup"><span data-stu-id="6287d-140">In the **Item type** field, select **Real**.</span></span> 
20.    <span data-ttu-id="6287d-141">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="6287d-141">Click **Add**.</span></span> 
21.    <span data-ttu-id="6287d-142">Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="6287d-142">Click **New** to open the drop dialog.</span></span> 
22.    <span data-ttu-id="6287d-143">Laukā **Nosaukums** ierakstiet “Datums”.</span><span class="sxs-lookup"><span data-stu-id="6287d-143">In the **Name** field, type 'Date'.</span></span> 
23.    <span data-ttu-id="6287d-144">Laukā **Vienuma veids** atlasiet **Datums**.</span><span class="sxs-lookup"><span data-stu-id="6287d-144">In the **Item type** field, select **Date**.</span></span> 
24.    <span data-ttu-id="6287d-145">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="6287d-145">Click **Add**.</span></span> 
25.    <span data-ttu-id="6287d-146">Noklikšķiniet uz **Saknes atsauce**.</span><span class="sxs-lookup"><span data-stu-id="6287d-146">Click **Root reference**.</span></span> 
26.    <span data-ttu-id="6287d-147">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6287d-147">Click **OK**.</span></span> 
27.    <span data-ttu-id="6287d-148">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="6287d-148">Click **Save**.</span></span> 
28.    <span data-ttu-id="6287d-149">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6287d-149">Close the page.</span></span> 
29.    <span data-ttu-id="6287d-150">Noklikšķiniet uz **Mainīt statusu**.</span><span class="sxs-lookup"><span data-stu-id="6287d-150">Click **Change status**.</span></span> 
30.    <span data-ttu-id="6287d-151">Noklikšķiniet uz **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="6287d-151">Click **Complete**.</span></span> 
31.    <span data-ttu-id="6287d-152">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6287d-152">Click **OK**.</span></span> 

## <a name="create-model-mapping-configuration"></a><span data-ttu-id="6287d-153">Modeļa kartēšanas konfigurācijas izveide</span><span class="sxs-lookup"><span data-stu-id="6287d-153">Create model mapping configuration</span></span> 
1. <span data-ttu-id="6287d-154">Noklikšķiniet uz **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="6287d-154">Click **Create configuration** to open the drop dialog.</span></span> 
2. <span data-ttu-id="6287d-155">Laukā **Jauns** ievadiet “Uz datu modeli Ārējās tirdzniecības modelis balstīta modeļa kartēšana”.</span><span class="sxs-lookup"><span data-stu-id="6287d-155">In the **New** field, enter 'Model Mapping based on data model Foreign trade model'.</span></span> 
3. <span data-ttu-id="6287d-156">Laukā **Nosaukums** ierakstiet “Ārējās tirdzniecības kartēšana”.</span><span class="sxs-lookup"><span data-stu-id="6287d-156">In the **Name** field, type 'Foreign trade mapping'.</span></span> 
4. <span data-ttu-id="6287d-157">Klikšķiniet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="6287d-157">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="6287d-158">Izvērsiet sadaļu **Priekšnosacījumi**.</span><span class="sxs-lookup"><span data-stu-id="6287d-158">Expand the **Prerequisites** section.</span></span> 
6. <span data-ttu-id="6287d-159">Noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="6287d-159">Click **Edit**.</span></span> 
7. <span data-ttu-id="6287d-160">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="6287d-160">Click **New**.</span></span> 
8. <span data-ttu-id="6287d-161">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="6287d-161">In the list, mark the selected row.</span></span> 
9. <span data-ttu-id="6287d-162">Laukā **Priekšnosacījuma komponenta veids** atlasiet **Konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="6287d-162">In the **Prerequisite component type** field, select **Configuration**.</span></span> 
10.    <span data-ttu-id="6287d-163">Atlasiet konfigurāciju **Ārējās tirdzniecības metadati**.</span><span class="sxs-lookup"><span data-stu-id="6287d-163">Select **Foreign trade metadata** configuration.</span></span> 
11.    <span data-ttu-id="6287d-164">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="6287d-164">Click **Save**.</span></span> 
12.    <span data-ttu-id="6287d-165">Tika pievienota atsauce uz konfigurācijas 'Ārējās tirdzniecības metadati' 1. versiju.</span><span class="sxs-lookup"><span data-stu-id="6287d-165">We added the reference to the version 1 of the 'Foreign trade metadata' configuration.</span></span> <span data-ttu-id="6287d-166">Izstrādājot šī modeļa kartēšanu, tiks piedāvāti šīs konfigurācijas programmas metadati.</span><span class="sxs-lookup"><span data-stu-id="6287d-166">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 
13.    <span data-ttu-id="6287d-167">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6287d-167">Close the page.</span></span> 
14.    <span data-ttu-id="6287d-168">Noklikšķiniet uz **Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="6287d-168">Click **Designer**.</span></span> 
15.    <span data-ttu-id="6287d-169">Noklikšķiniet uz **Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="6287d-169">Click **Designer**.</span></span> 
16.    <span data-ttu-id="6287d-170">Kokā atlasiet **Dynamics 365 for Operations\Tabulas ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="6287d-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
17.    <span data-ttu-id="6287d-171">Noklikšķiniet uz **Pievienot sakni**.</span><span class="sxs-lookup"><span data-stu-id="6287d-171">Click **Add root**.</span></span> 
18.    <span data-ttu-id="6287d-172">Laukā **Nosaukums** ierakstiet “Intrastat”.</span><span class="sxs-lookup"><span data-stu-id="6287d-172">In the **Name** field, type 'Intrastat'.</span></span> 
19.    <span data-ttu-id="6287d-173">Atlasiet **Intrastat** tabulas ierakstus.</span><span class="sxs-lookup"><span data-stu-id="6287d-173">Select **Intrastat** table records.</span></span> 
20.    <span data-ttu-id="6287d-174">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6287d-174">Click **OK**.</span></span> 

> [!NOTE]
> <span data-ttu-id="6287d-175">Tika piedāvātas tikai 2 tabulas, jo tikai 2 tabulas bija pievienotas pašlaik izmantotajai metadatu kopai.</span><span class="sxs-lookup"><span data-stu-id="6287d-175">The only 2 tables were offered as the only 2 tables were added into the set of metadata which is currently in use.</span></span> 

21.    <span data-ttu-id="6287d-176">Noklikšķiniet uz **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="6287d-176">Click **Bind**.</span></span> 
22.    <span data-ttu-id="6287d-177">Kokā izvērsiet sadaļu **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="6287d-177">In the tree, expand **Intrastat**.</span></span> 
23.    <span data-ttu-id="6287d-178">Kokā atlasiet **Intrastat\AmountMST**.</span><span class="sxs-lookup"><span data-stu-id="6287d-178">In the tree, select **Intrastat\AmountMST**.</span></span> 
24.    <span data-ttu-id="6287d-179">Kokā izvērsiet sadaļu **Transakcija = Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="6287d-179">In the tree, expand **Transaction = Intrastat**.</span></span> 
25.    <span data-ttu-id="6287d-180">Kokā atlasiet **Transakcija = Intrastat\Rēķinā iekļautā summa**.</span><span class="sxs-lookup"><span data-stu-id="6287d-180">In the tree, select **Transaction = Intrastat\Invoiced amount**.</span></span> 
26.    <span data-ttu-id="6287d-181">Noklikšķiniet uz **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="6287d-181">Click **Bind**.</span></span> 
27.    <span data-ttu-id="6287d-182">Kokā atlasiet **Intrastat\TransDate**.</span><span class="sxs-lookup"><span data-stu-id="6287d-182">In the tree, select **Intrastat\TransDate**.</span></span> 
28.    <span data-ttu-id="6287d-183">Kokā atlasiet **Transakcija = Intrastat\Datums**.</span><span class="sxs-lookup"><span data-stu-id="6287d-183">In the tree, select **Transaction = Intrastat\Date**.</span></span> 
29.    <span data-ttu-id="6287d-184">Noklikšķiniet uz **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="6287d-184">Click **Bind**.</span></span> 
30.    <span data-ttu-id="6287d-185">Kokā izvērsiet sadaļu **Intrastat\>Relācijas**.</span><span class="sxs-lookup"><span data-stu-id="6287d-185">In the tree, expand **Intrastat\>Relations**.</span></span> 
31.    <span data-ttu-id="6287d-186">Kokā izvērsiet sadaļu **Intrastat\>Relācijas\IntrastatCommodity**.</span><span class="sxs-lookup"><span data-stu-id="6287d-186">In the tree, expand **Intrastat\>Relations\IntrastatCommodity**.</span></span> 
32.    <span data-ttu-id="6287d-187">Kokā atlasiet **Intrastat\>Relācijas\IntrastatCommodity\Kods**.</span><span class="sxs-lookup"><span data-stu-id="6287d-187">In the tree, select **Intrastat\>Relations\IntrastatCommodity\Code**.</span></span> 
33.    <span data-ttu-id="6287d-188">Kokā atlasiet **Transakcija = Intrastat\Preces kods**.</span><span class="sxs-lookup"><span data-stu-id="6287d-188">In the tree, select **Transaction = Intrastat\Commodity code**.</span></span> 
34.    <span data-ttu-id="6287d-189">Noklikšķiniet uz **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="6287d-189">Click **Bind**.</span></span> 
35.    <span data-ttu-id="6287d-190">Noklikšķiniet uz **Validēt**.</span><span class="sxs-lookup"><span data-stu-id="6287d-190">Click **Validate**.</span></span> 

> [!NOTE]
> <span data-ttu-id="6287d-191">Datu modeļa elementi ir veiksmīgi saistīti ar datu avotu vienībām, kas aprakstītas, lietojot detalizētu informāciju par programmas metadatiem no atsauces ER metadatu konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="6287d-191">We have successfully bound elements of data model with items of data sources that are described by using details of application metadata from the referred ER metadata configuration.</span></span> 
36.    <span data-ttu-id="6287d-192">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="6287d-192">Click **Save**.</span></span> 
37.    <span data-ttu-id="6287d-193">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6287d-193">Close the page.</span></span> 
38.    <span data-ttu-id="6287d-194">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6287d-194">Close the page.</span></span> 
39.    <span data-ttu-id="6287d-195">Ja nepieciešams, varat paplašināt esošo metadatu kopu un pēc tam eksportēt jauno ER metadatu konfigurācijas versiju.</span><span class="sxs-lookup"><span data-stu-id="6287d-195">When needed, you can extend the existing set of metadata and then export the new completed version of ER metadata configuration.</span></span> <span data-ttu-id="6287d-196">Pēc tam varat importēt to uz RCS un atjaunināt konfigurētā modeļa kartēšanas konfigurācijas priekšnosacījumus, kas attiecas uz jaunu importēto metadatu konfigurācijas versiju.</span><span class="sxs-lookup"><span data-stu-id="6287d-196">You can then import it to RCS, and update the prerequisites of the configured model mapping configuration referring to a new version of imported metadata configuration.</span></span> 

> [!NOTE]
> <span data-ttu-id="6287d-197">Šāds veids, kā iegūt informāciju par programmas metadatiem, ir vienīgais pieejamais lokāli izvietotajām programmām (kad risinājumā tiek izmantots vietējas biznesa datu (LBD) izvietošanas vai lokālas izvietošanas modelis).</span><span class="sxs-lookup"><span data-stu-id="6287d-197">This way of getting information about application metadata is the only one available for locally deployed applications (when local business data (LBD), or on-premises, deployment model is used).</span></span>
        
