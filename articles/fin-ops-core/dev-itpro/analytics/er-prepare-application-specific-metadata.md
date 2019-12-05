---
title: Programmai atbilstošo metadatu sagatavošana izmantošanai RCS un ER
description: Šajā tēmā ir paskaidrots, kā sagatavot programmai atbilstošus metadatus izmantošanai pakalpojumā Regulatory Configuration Service (RCS) un elektroniskajos pārskatos ( Electronic Reporting — ER).
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 89d36c305bc9210f7906cd4288e33e5028baecdb
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771264"
---
# <a name="prepare-application-specific-metadata-for-rcs-and-er"></a><span data-ttu-id="3d192-103">Programmai atbilstošo metadatu sagatavošana izmantošanai RCS un ER</span><span class="sxs-lookup"><span data-stu-id="3d192-103">Prepare application-specific metadata for RCS and ER</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3d192-104">Šajā tēmā ir sniegti šādi uzdevumu piemēri:</span><span class="sxs-lookup"><span data-stu-id="3d192-104">This topic walks you through examples of the following tasks:</span></span>

- [<span data-ttu-id="3d192-105">RCS izmantojamo programmas metadatu sagatavošana</span><span class="sxs-lookup"><span data-stu-id="3d192-105">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)
- [<span data-ttu-id="3d192-106">Piekļuve programmas metadatiem, izmantojot ER konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="3d192-106">Access application metadata by using an ER configuration</span></span>](#access-application-metadata-by-using-an-er-configuration)
- [<span data-ttu-id="3d192-107">Piekļuve programmas metadatiem, izmantojot saistītās programmas</span><span class="sxs-lookup"><span data-stu-id="3d192-107">Access application metadata by using connected applications</span></span>](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a><span data-ttu-id="3d192-108">RCS izmantojamo programmas metadatu sagatavošana</span><span class="sxs-lookup"><span data-stu-id="3d192-108">Prepare application metadata that can be used in RCS</span></span>

<span data-ttu-id="3d192-109">Nākamajā procedūrā ir parādīts, kā lietotājs, kas ir **Sistēmas administrators** vai **Elektronisko pārskatu izstrādātājs** var izveidot jaunu elektronisko pārskatu (Electronic reporting — ER) konfigurāciju, kurā ir programmas metadati un ko izmanto ER modeļa kartēšanas konfigurāciju veidošanai pakalpojumā Regulatory configuration service (RCS).</span><span class="sxs-lookup"><span data-stu-id="3d192-109">The following procedure shows how a user who has the **System Administrator** or **Electronic Reporting Developer** role can create an Electronic reporting (ER) configuration that contains metadata for the application, and that is used to design ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="3d192-110">Parauga ER modeļa kartēšanas konfigurācija, ko izveido šajā piemērā, tiks izmantota piekļūšanai ārējās tirdzniecības transakcijām.</span><span class="sxs-lookup"><span data-stu-id="3d192-110">The sample ER model mapping configuration that is created in this example will be used to access foreign trade transactions.</span></span>

<span data-ttu-id="3d192-111">Šajā piemērā izmantosim pakalpojumu RCS, lai izveidotu ER risinājumu programmai, kas tiks izmantota, lai ģenerētu elektroniskus dokumentus, kuros ir informācija no ārējās tirdzniecības uzņēmējdarbības jomas.</span><span class="sxs-lookup"><span data-stu-id="3d192-111">For this example, you want to use RCS to design an ER solution for the application that will be used to generate electronic documents that contain information from the foreign trade business domain.</span></span> <span data-ttu-id="3d192-112">Lai norādītu noteiktu kartēšanu starp ER datu modeli un nepieciešamo datu avotiem, pakalpojumā RCS jums ir nepieciešama piekļuve programmas metadatiem.</span><span class="sxs-lookup"><span data-stu-id="3d192-112">To specify the mapping between the ER data model and the sources of required data, you must have access to application metadata in RCS.</span></span> <span data-ttu-id="3d192-113">Tādēļ ER risinājuma veidošanas procesā jums ir jākonfigurē jauna ER metadatu konfigurācija, kas ietver visus metadatus, kuri pašlaik ir nepieciešami ER pārskatu veidošanai atlasītajai uzņēmējdarbības jomai.</span><span class="sxs-lookup"><span data-stu-id="3d192-113">Therefore, as part of the process of designing the ER solution, you must configure a new ER metadata configuration that contains all the metadata that is currently required in order to generate ER reports for the selected business domain.</span></span>

> [!NOTE]
> <span data-ttu-id="3d192-114">Šajā piemērā jūs izveidosit konfigurāciju parauga uzņēmumam Litware, Inc. Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="3d192-114">In this example, you will create a configuration for the sample company, Litware, Inc. These steps can be performed in any company.</span></span>

1. <span data-ttu-id="3d192-115">Dodieties uz **Organizācijas administrēšana \> Darbvietas \> Elektronisko atskaišu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="3d192-115">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="3d192-116">Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam Litware, Inc. ir pieejams un ir atzīmēts kā **Aktīvs**.</span><span class="sxs-lookup"><span data-stu-id="3d192-116">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="3d192-117">Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda procedūra [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="3d192-117">If you don't see this configuration provider, complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="3d192-118">Atlasiet **Metadatu konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="3d192-118">Select **Metadata configurations**.</span></span>
4. <span data-ttu-id="3d192-119">Atlasiet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="3d192-119">Select **Create configuration**.</span></span>
5. <span data-ttu-id="3d192-120">Nolaižamā dialoglodziņa laukā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="3d192-120">In the drop-down dialog box, in the **Name** field, enter a name.</span></span> <span data-ttu-id="3d192-121">Šim piemēram ievadiet **Ārējās tirdzniecības metadati**.</span><span class="sxs-lookup"><span data-stu-id="3d192-121">For this example, enter **Foreign trade metadata**.</span></span>
6. <span data-ttu-id="3d192-122">Atlasiet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="3d192-122">Select **Create configuration**.</span></span>
7. <span data-ttu-id="3d192-123">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="3d192-123">Select **Designer**.</span></span>
8. <span data-ttu-id="3d192-124">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="3d192-124">Select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3d192-125">Varat atlasīt visus metadatus vai nu visai programmai, vai atlasītajiem modeļiem vai moduļiem.</span><span class="sxs-lookup"><span data-stu-id="3d192-125">You can select all metadata either for the whole application, or for selected models or modules.</span></span> <span data-ttu-id="3d192-126">Abos gadījumos ņemiet vērā, ka automātiski tiks pievienoti šādi metadati: ierakstu tabulas, uzskaitījumi un paplašinātie datu tipi (EDT).</span><span class="sxs-lookup"><span data-stu-id="3d192-126">In both cases, be aware that the following metadata will be automatically added: tables of records, enumerations, and extended data types (EDTs).</span></span> <span data-ttu-id="3d192-127">Ja ir nepieciešami papildu metadatu tipi, tie ir jāpievieno manuāli.</span><span class="sxs-lookup"><span data-stu-id="3d192-127">When additional types of metadata are required, they must be manually added.</span></span>

    <span data-ttu-id="3d192-128">Jums ir jāpievieno daži ar ārējās tirdzniecības transakcijām saistīti metadati un manuāli jāatlasa metadatu vienumi.</span><span class="sxs-lookup"><span data-stu-id="3d192-128">You must add some metadata that is related to foreign trade transactions and manually select metadata items.</span></span>

9. <span data-ttu-id="3d192-129">Atlasiet **Pievienot datu avotu \> Tabulas ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="3d192-129">Select **Add data source \> Table records**.</span></span>
10. <span data-ttu-id="3d192-130">Filtrējiet **Intrastat** vērtību laukā **Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="3d192-130">Filter on a value of **Intrastat** in the **Name** field.</span></span>
11. <span data-ttu-id="3d192-131">Atlasiet **Intrastat** tabulas ierakstu.</span><span class="sxs-lookup"><span data-stu-id="3d192-131">Select the **Intrastat** table record.</span></span>
12. <span data-ttu-id="3d192-132">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3d192-132">Select **OK**.</span></span>

    <span data-ttu-id="3d192-133">Jums ir jāpievieno metadatu informācija par Intrastat ierakstu tabulu.</span><span class="sxs-lookup"><span data-stu-id="3d192-133">You must add metadata information about the Intrastat table of records.</span></span>

13. <span data-ttu-id="3d192-134">Koka struktūrā atlasiet **Tabulas ieraksti Intrastat \> \>Relācijas \> IntrastatCommodity (Tabulas ieraksti EcoResCategory)**.</span><span class="sxs-lookup"><span data-stu-id="3d192-134">In the tree, select **Table records Intrastat \> \>Relations \> IntrastatCommodity (Table records EcoResCategory)**.</span></span>
14. <span data-ttu-id="3d192-135">Atlasiet **Pievienot metadatus**.</span><span class="sxs-lookup"><span data-stu-id="3d192-135">Select **Add metadata**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3d192-136">Metadati par nepieciešamajām relācijām atlasītajai ierakstu tabulai ir jāpievieno manuāli.</span><span class="sxs-lookup"><span data-stu-id="3d192-136">Metadata about required relations for the selected table of records must be added manually.</span></span>

15. <span data-ttu-id="3d192-137">Atlasiet **Pievienot datu avotu**.</span><span class="sxs-lookup"><span data-stu-id="3d192-137">Select **Add data source**.</span></span>
16. <span data-ttu-id="3d192-138">Atlasiet **Uzskaitījums**.</span><span class="sxs-lookup"><span data-stu-id="3d192-138">Select **Enumeration**.</span></span>
17. <span data-ttu-id="3d192-139">Filtrējiet **IntrastatDirection** vērtību laukā **Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="3d192-139">Filter on a value of **IntrastatDirection** in the **Name** field.</span></span>
18. <span data-ttu-id="3d192-140">Atlasiet uzskaitījuma ierakstu **IntrastatDirection**.</span><span class="sxs-lookup"><span data-stu-id="3d192-140">Select the **IntrastatDirection** enumeration record.</span></span>
19. <span data-ttu-id="3d192-141">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3d192-141">Select **OK**.</span></span>
20. <span data-ttu-id="3d192-142">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="3d192-142">Select **Save**.</span></span>
21. <span data-ttu-id="3d192-143">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3d192-143">Close the page.</span></span>
22. <span data-ttu-id="3d192-144">Pabeidziet metadatu konfigurācijas melnraksta versiju, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="3d192-144">Complete the draft version of the metadata configuration:</span></span>

    1. <span data-ttu-id="3d192-145">Atlasiet **Mainīt statusu \> Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="3d192-145">Select **Change status \> Complete**.</span></span>
    2. <span data-ttu-id="3d192-146">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3d192-146">Select **OK**.</span></span>
    3. <span data-ttu-id="3d192-147">Atlasiet 1. pabeigto versiju.</span><span class="sxs-lookup"><span data-stu-id="3d192-147">Select the completed version 1.</span></span>

23. <span data-ttu-id="3d192-148">Eksportējiet pabeigtās metadatu konfigurācijas versiju no programmas XML faila veidā, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="3d192-148">Export the completed version of the metadata configuration from the application as an XML file:</span></span>

    1. <span data-ttu-id="3d192-149">Atlasiet **Maiņa \> Eksportēt kā XML failu**.</span><span class="sxs-lookup"><span data-stu-id="3d192-149">Select **Exchange \> Export as XML file**.</span></span>
    2. <span data-ttu-id="3d192-150">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3d192-150">Select **OK**.</span></span>

<span data-ttu-id="3d192-151">Izveidotā ER metadatu konfigurācija tiek saglabāta kā fails **Ārējās tirdzniecības metadati.xml**.</span><span class="sxs-lookup"><span data-stu-id="3d192-151">The ER metadata configuration that you created is saved as the **Foreign trade metadata.xml** file.</span></span> <span data-ttu-id="3d192-152">Tagad varat importēt to pakalpojumā RCS, lai to varētu izmantot kā metadatu avotu ārējās tirdzniecības biznesa domēnam.</span><span class="sxs-lookup"><span data-stu-id="3d192-152">You can now import it into RCS, so that it can be used as the source of metadata for the foreign trade business domain.</span></span> <span data-ttu-id="3d192-153">Balstoties uz šo informāciju, varat norādīt kartēšanu starp programmas metadatiem un ER datu modeli.</span><span class="sxs-lookup"><span data-stu-id="3d192-153">Based on this information, you can specify the mapping between application metadata and the ER data model.</span></span>

## <a name="access-application-metadata-by-using-an-er-configuration"></a><span data-ttu-id="3d192-154">Piekļuve programmas metadatiem, izmantojot ER konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="3d192-154">Access application metadata by using an ER configuration</span></span>

<span data-ttu-id="3d192-155">Šī procedūra parāda, kā RCS lietotājs, kuram ir loma **Sistēmas administrators** vai **Elektronisko pārskatu izstrādātājs**, var izveidot jaunu ER modeļa kartēšanu, izmantojot programmas metadatus.</span><span class="sxs-lookup"><span data-stu-id="3d192-155">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata from the application.</span></span> <span data-ttu-id="3d192-156">Programmas metadatiem jāpiekļūst, izmantojot ER metadatu konfigurāciju, kas ietver metadatu paraugu kopu, lai piekļūtu ārējās tirdzniecības transakcijām.</span><span class="sxs-lookup"><span data-stu-id="3d192-156">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span>

<span data-ttu-id="3d192-157">Lai varētu izpildīt šo procedūru, vispirms ir jāveic tālāk norādītās procedūras.</span><span class="sxs-lookup"><span data-stu-id="3d192-157">Before you can complete this procedure, you must first complete the following procedures:</span></span>

- [<span data-ttu-id="3d192-158">Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus</span><span class="sxs-lookup"><span data-stu-id="3d192-158">Create configuration providers and mark them as active</span></span>](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [<span data-ttu-id="3d192-159">RCS izmantojamo programmas metadatu sagatavošana</span><span class="sxs-lookup"><span data-stu-id="3d192-159">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)

1. <span data-ttu-id="3d192-160">Dodieties uz **Visas darbvietas \> Elektroniskie pārskati**.</span><span class="sxs-lookup"><span data-stu-id="3d192-160">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="3d192-161">Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam Litware, Inc. ir pieejams un ir atzīmēts kā **Aktīvs**.</span><span class="sxs-lookup"><span data-stu-id="3d192-161">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="3d192-162">Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda procedūra [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="3d192-162">If you don't see this configuration provider, complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="3d192-163">Importējiet ER metadatu konfigurāciju, kas satur programmas metadatus un kas ir konfigurēta elektronisko dokumentu ģenerēšanai ārējās tirdzniecības uzņēmējdarbībai.</span><span class="sxs-lookup"><span data-stu-id="3d192-163">Import the ER metadata configuration that contains metadata for the application, and that is configured to generate electronic documents for the foreign trade business domain.</span></span> <span data-ttu-id="3d192-164">Jūs izveidojāt šo ER metadatu konfigurāciju un eksportējāt to kā XML failu procedūrā [RCS izmantojamo programmas metadatu sagatavošana](#prepare-application-metadata-that-can-be-used-in-rcs), kas norādīta iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="3d192-164">You created this ER metadata configuration and exported it as an XML file in the [Prepare application metadata that can be used in RCS](#prepare-application-metadata-that-can-be-used-in-rcs) procedure earlier in this topic.</span></span>

    1. <span data-ttu-id="3d192-165">Atlasiet **Metadatu konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="3d192-165">Select **Metadata configurations**.</span></span>
    2. <span data-ttu-id="3d192-166">Atlasiet **Maiņa**.</span><span class="sxs-lookup"><span data-stu-id="3d192-166">Select **Exchange**.</span></span>
    3. <span data-ttu-id="3d192-167">Atlasiet **Ielādēt no XML faila**.</span><span class="sxs-lookup"><span data-stu-id="3d192-167">Select **Load from XML file**.</span></span>
    4. <span data-ttu-id="3d192-168">Pārlūkojiet un atlasiet failu **Ārējās tirdzniecības metadati.xml**.</span><span class="sxs-lookup"><span data-stu-id="3d192-168">Browse to select the **Foreign trade metadata.xml** file.</span></span>
    5. <span data-ttu-id="3d192-169">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3d192-169">Select **OK**.</span></span>
    6. <span data-ttu-id="3d192-170">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3d192-170">Close the page.</span></span>

4. <span data-ttu-id="3d192-171">Izveidojiet datu modeļa konfigurāciju, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="3d192-171">Create a data model configuration:</span></span>

    1. <span data-ttu-id="3d192-172">Atlasiet **Pārskatu konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="3d192-172">Select **Reporting configurations**.</span></span>
    2. <span data-ttu-id="3d192-173">Atlasiet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="3d192-173">Select **Create configuration**.</span></span>
    3. <span data-ttu-id="3d192-174">Nolaižamā dialoglodziņa laukā **Nosaukums** ievadiet **Ārējās tirdzniecības modelis**.</span><span class="sxs-lookup"><span data-stu-id="3d192-174">In the drop-down dialog box, in the **Name** field, enter **Foreign trade model**.</span></span>
    4. <span data-ttu-id="3d192-175">Atlasiet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="3d192-175">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="3d192-176">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="3d192-176">Select **Designer**.</span></span>
    6. <span data-ttu-id="3d192-177">Atalsiet **Jauns**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="3d192-177">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="3d192-178">Laukā **Nosaukums** ierakstiet **Sakne**.</span><span class="sxs-lookup"><span data-stu-id="3d192-178">In the **Name** field, type **Root**.</span></span>
        2. <span data-ttu-id="3d192-179">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="3d192-179">Select **Add**.</span></span>
    
    7. <span data-ttu-id="3d192-180">Atalsiet **Jauns**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="3d192-180">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="3d192-181">Laukā **Nosaukums** ierakstiet **Transakcija**.</span><span class="sxs-lookup"><span data-stu-id="3d192-181">In the **Name** field, type **Transaction**.</span></span>
        2. <span data-ttu-id="3d192-182">Laukā **Vienuma veids** atlasiet **Ierakstu saraksts**.</span><span class="sxs-lookup"><span data-stu-id="3d192-182">In the **Item type** field, select **Record list**.</span></span>
        3. <span data-ttu-id="3d192-183">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="3d192-183">Select **Add**.</span></span>
 
    8. <span data-ttu-id="3d192-184">Atalsiet **Jauns**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="3d192-184">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="3d192-185">Laukā **Nosaukums** ierakstiet **Preces kods**.</span><span class="sxs-lookup"><span data-stu-id="3d192-185">In the **Name** field, type **Commodity code**.</span></span>
        2. <span data-ttu-id="3d192-186">Laukā **Vienuma veids** atlasiet **Virkne**.</span><span class="sxs-lookup"><span data-stu-id="3d192-186">In the **Item type** field, select **String**.</span></span>
        3. <span data-ttu-id="3d192-187">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="3d192-187">Select **Add**.</span></span>

    9. <span data-ttu-id="3d192-188">Atalsiet **Jauns**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="3d192-188">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="3d192-189">Laukā Nosaukums ierakstiet **Rēķinā iekļautā summa**.</span><span class="sxs-lookup"><span data-stu-id="3d192-189">In the Name field, type **Invoiced amount**.</span></span>
        2. <span data-ttu-id="3d192-190">Laukā **Vienuma veids** atlasiet **Reāls**.</span><span class="sxs-lookup"><span data-stu-id="3d192-190">In the **Item type** field, select **Real**.</span></span>
        3. <span data-ttu-id="3d192-191">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="3d192-191">Select **Add**.</span></span>

    10. <span data-ttu-id="3d192-192">Atalsiet **Jauns**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="3d192-192">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="3d192-193">Laukā **Nosaukums** ierakstiet **Datums**.</span><span class="sxs-lookup"><span data-stu-id="3d192-193">In the **Name** field, type **Date**.</span></span>
        2. <span data-ttu-id="3d192-194">Laukā **Vienuma veids** atlasiet **Datums**.</span><span class="sxs-lookup"><span data-stu-id="3d192-194">In the **Item type** field, select **Date**.</span></span>
        3. <span data-ttu-id="3d192-195">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="3d192-195">Select **Add**.</span></span>
 
    11. <span data-ttu-id="3d192-196">Atlasiet **Pievienot \> Saknes atsauce**.</span><span class="sxs-lookup"><span data-stu-id="3d192-196">Select **Add \> Root reference**.</span></span>
    12. <span data-ttu-id="3d192-197">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3d192-197">Select **OK**.</span></span>
    13. <span data-ttu-id="3d192-198">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="3d192-198">Select **Save**.</span></span>
    14. <span data-ttu-id="3d192-199">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3d192-199">Close the page.</span></span>
    15. <span data-ttu-id="3d192-200">Atlasiet **Mainīt statusu \> Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="3d192-200">Select **Change status \> Complete**.</span></span>
    16. <span data-ttu-id="3d192-201">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3d192-201">Select **OK**.</span></span>

5. <span data-ttu-id="3d192-202">Izveidojiet modeļa kartēšanas konfigurāciju, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="3d192-202">Create a model mapping configuration:</span></span>

    1. <span data-ttu-id="3d192-203">Atlasiet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="3d192-203">Select **Create configuration**.</span></span>
    2. <span data-ttu-id="3d192-204">Nolaižamā dialoglodziņa laukā **Jauns** ievadiet **Uz datu modeli “Ārējās tirdzniecības modelis” balstīta modeļa kartēšana**.</span><span class="sxs-lookup"><span data-stu-id="3d192-204">In the drop-down dialog box, in the **New** field, enter **Model Mapping based on data model Foreign trade model**.</span></span>
    3. <span data-ttu-id="3d192-205">Laukā **Nosaukums** ievadiet **Ārējās tirdzniecības kartēšana**.</span><span class="sxs-lookup"><span data-stu-id="3d192-205">In the **Name** field, enter **Foreign trade mapping**.</span></span>
    4. <span data-ttu-id="3d192-206">Atlasiet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="3d192-206">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="3d192-207">Kopsavilkuma cilnē **Priekšnosacījumi** atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="3d192-207">On the **Prerequisites** FastTab, select **Edit**.</span></span>
    6. <span data-ttu-id="3d192-208">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="3d192-208">Select **New**.</span></span>
    7. <span data-ttu-id="3d192-209">Laukā **Priekšnosacījuma komponenta veids** atlasiet **Konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="3d192-209">In the **Prerequisite component type** field, select **Configuration**.</span></span>
    8. <span data-ttu-id="3d192-210">Atlasiet konfigurāciju **Ārējās tirdzniecības metadati**.</span><span class="sxs-lookup"><span data-stu-id="3d192-210">Select the **Foreign trade metadata** configuration.</span></span>
    9. <span data-ttu-id="3d192-211">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="3d192-211">Select **Save**.</span></span> <span data-ttu-id="3d192-212">Ņemiet vērā, ka konfigurācijas **Ārējās tirdzniecības metadati** 1. versijai ir pievienota atsauce.</span><span class="sxs-lookup"><span data-stu-id="3d192-212">Notice that the reference is added to version 1 of the **Foreign trade metadata** configuration.</span></span> <span data-ttu-id="3d192-213">Izstrādājot šī modeļa kartēšanu, tiks piedāvāti šīs konfigurācijas programmas metadati.</span><span class="sxs-lookup"><span data-stu-id="3d192-213">Application metadata from this configuration will be offered while the model mapping is designed.</span></span>
    10. <span data-ttu-id="3d192-214">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3d192-214">Close the page.</span></span>
    11. <span data-ttu-id="3d192-215">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="3d192-215">Select **Designer**.</span></span>
    12. <span data-ttu-id="3d192-216">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="3d192-216">Select **Designer**.</span></span>
    13. <span data-ttu-id="3d192-217">Kokā atlasiet **Dynamics 365 for Operations \> Tabulas ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="3d192-217">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
    14. <span data-ttu-id="3d192-218">Atlasiet **Pievienot sakni**.</span><span class="sxs-lookup"><span data-stu-id="3d192-218">Select **Add root**.</span></span>
    15. <span data-ttu-id="3d192-219">Laukā **Nosaukums** ievadiet **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="3d192-219">In the **Name** field, enter **Intrastat**.</span></span>
    16. <span data-ttu-id="3d192-220">Atlasiet **Intrastat** tabulas ierakstus.</span><span class="sxs-lookup"><span data-stu-id="3d192-220">Select **Intrastat** table records.</span></span>
    17. <span data-ttu-id="3d192-221">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3d192-221">Select **OK**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="3d192-222">Tika piedāvātas tikai 2 tabulas, jo tikai 2 tabulas bija pievienotas pašlaik izmantotajai metadatu kopai.</span><span class="sxs-lookup"><span data-stu-id="3d192-222">Only two tables are offered, because only two tables were added to the set of metadata that is currently used.</span></span>

    18. <span data-ttu-id="3d192-223">Atlasiet **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="3d192-223">Select **Bind**.</span></span>
    19. <span data-ttu-id="3d192-224">Kokā atlasiet **Intrastat \> AmountMST**.</span><span class="sxs-lookup"><span data-stu-id="3d192-224">In the tree, select **Intrastat \> AmountMST**.</span></span>
    20. <span data-ttu-id="3d192-225">Kokā atlasiet **Transakcija = Intrastat \> Rēķinā iekļautā summa**.</span><span class="sxs-lookup"><span data-stu-id="3d192-225">In the tree, select **Transaction = Intrastat \> Invoiced amount**.</span></span>
    21. <span data-ttu-id="3d192-226">Atlasiet **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="3d192-226">Select **Bind**.</span></span>
    22. <span data-ttu-id="3d192-227">Kokā atlasiet **Intrastat \> TransDate**.</span><span class="sxs-lookup"><span data-stu-id="3d192-227">In the tree, select **Intrastat \> TransDate**.</span></span>
    23. <span data-ttu-id="3d192-228">Kokā atlasiet **Transakcija = Intrastat \> Datums**.</span><span class="sxs-lookup"><span data-stu-id="3d192-228">In the tree, select **Transaction = Intrastat \> Date**.</span></span>
    24. <span data-ttu-id="3d192-229">Atlasiet **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="3d192-229">Select **Bind**.</span></span>
    25. <span data-ttu-id="3d192-230">Kokā atlasiet **Intrastat \> \>Relācijas \> IntrastatCommodity \> Kods**.</span><span class="sxs-lookup"><span data-stu-id="3d192-230">In the tree, select **Intrastat \> \>Relations \> IntrastatCommodity \> Code**.</span></span>
    26. <span data-ttu-id="3d192-231">Kokā atlasiet **Transakcija = Intrastat \> Preces kods**.</span><span class="sxs-lookup"><span data-stu-id="3d192-231">In the tree, select **Transaction = Intrastat \> Commodity code**.</span></span>
    27. <span data-ttu-id="3d192-232">Atlasiet **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="3d192-232">Select **Bind**.</span></span>
    28. <span data-ttu-id="3d192-233">Atlasiet **Validēt**.</span><span class="sxs-lookup"><span data-stu-id="3d192-233">Select **Validate**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="3d192-234">Pēc validācijas pabeigšanas, esat veiksmīgi saistījis datu modeļa elementus ar datu avotu vienībām, kas aprakstītas, lietojot detalizētu informāciju par programmas metadatiem no atsauces ER metadatu konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="3d192-234">After validation is completed, you've successfully bound elements of the data model to items of the data sources that are described by using details of the application metadata from the referenced ER metadata configuration.</span></span>

    29. <span data-ttu-id="3d192-235">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="3d192-235">Select **Save**.</span></span>

<span data-ttu-id="3d192-236">Ja vēlaties, varat paplašināt esošo metadatu kopu programmā.</span><span class="sxs-lookup"><span data-stu-id="3d192-236">As you require, you can extend the existing set of metadata in the application.</span></span> <span data-ttu-id="3d192-237">Pēc tam jūs varat eksportēt ER metadatu konfigurācijas jauno pabeigto versiju, importēt to pakalpojumā RCS un atjaunināt konfigurācijas priekšnosacījumus konfigurētā modeļa kartēšanas konfigurācijai, lai tie attiektos uz importēto metadatu konfigurācijas jauno versiju.</span><span class="sxs-lookup"><span data-stu-id="3d192-237">You can then export the new completed version of the ER metadata configuration, import it into RCS, and update the prerequisites of the configured model mapping configuration to refer to a new version of the imported metadata configuration.</span></span>

> [!NOTE]
> <span data-ttu-id="3d192-238">Šī metode, kā iegūt informāciju par programmas metadatiem, ir vienīgā pieejamā metode programmām, kas ir izvietotas lokāli (proti, kad ir izmantots lokālas biznesa datu \[LBD\] vai vietējais izvietošanas modelis programmai).</span><span class="sxs-lookup"><span data-stu-id="3d192-238">This method for getting information about application metadata is the only available method for applications that are locally deployed (that is, when a local business data \[LBD\], or on-premises, deployment model is used for the application).</span></span>

## <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="3d192-239">Piekļuve programmas metadatiem, izmantojot saistītās programmas</span><span class="sxs-lookup"><span data-stu-id="3d192-239">Access application metadata by using connected applications</span></span>

<span data-ttu-id="3d192-240">Šī procedūra parāda, kā RCS lietotājs, kuram ir loma **Sistēmas administrators** vai **Elektronisko pārskatu izstrādātājs**, var izveidot jaunu ER modeļa kartēšanu, izmantojot programmas metadatus.</span><span class="sxs-lookup"><span data-stu-id="3d192-240">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata of the application.</span></span> <span data-ttu-id="3d192-241">Programmas metadatiem jāpiekļūst tiešsaistē, izmantojot ar RCS saistīto programmu.</span><span class="sxs-lookup"><span data-stu-id="3d192-241">Application metadata will be accessed online by using RCS connected application.</span></span> <span data-ttu-id="3d192-242">Parauga ER modeļa kartēšana jākonfigurē piekļuvei ārējās tirdzniecības transakcijām.</span><span class="sxs-lookup"><span data-stu-id="3d192-242">A sample ER model mapping will be configured to access foreign trade transactions.</span></span>

<span data-ttu-id="3d192-243">Lai izpildītu šo procedūru, vispirms rīkā RCS izpildiet procedūru [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="3d192-243">To complete this procedure, you must first complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure in RCS.</span></span> <span data-ttu-id="3d192-244">Ja vēl neesat izpildījis iepriekš šajā tēmā aprakstīto procedūru [Piekļuve programmas metadatiem, izmantojot ER konfigurāciju](#access-application-metadata-by-using-an-er-configuration) dodieties uz lapu [Elektronisko pārskatu uzdevumu ceļvedis izmantošanai Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739), lai jau laikus lejupielādētu un lokāli saglabātu šādas ER konfigurācijas: **Ārējās tirdzniecības metadati.xml**, **Ārējās tirdzniecības modelis.xml** un **Ārējās tirdzniecības kartēšana.xml**.</span><span class="sxs-lookup"><span data-stu-id="3d192-244">If you haven't yet completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, go to [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page to download the following ER configuration files in advance and save them locally: **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml**.</span></span>


### <a name="get-required-er-configurations"></a><span data-ttu-id="3d192-245">Nepieciešamo ER konfigurāciju iegūšana</span><span class="sxs-lookup"><span data-stu-id="3d192-245">Get required ER configurations</span></span>

<span data-ttu-id="3d192-246">Ja esat jau izpildījis darbības, kas ir aprakstītas iepriekš šājā tēmā norādītajā procedūrā [Piekļuve programmas metadatiem, izmantojot ER konfigurāciju](#access-application-metadata-by-using-an-er-configuration), jums jau ir visas nepieciešamās ER konfigurācijas (ārējās tirdzniecības metadatu, modeļa un kartēšanas konfigurācijas) pašreizējā RCS instancē.</span><span class="sxs-lookup"><span data-stu-id="3d192-246">If you've already completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, you already have all the required ER configurations (the foreign trade metadata, model, and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="3d192-247">Šādā gadījumā šo procedūru varat izlaist.</span><span class="sxs-lookup"><span data-stu-id="3d192-247">In that case, you can skip this procedure.</span></span>

1. <span data-ttu-id="3d192-248">Dodieties uz **Visas darbvietas \> Elektroniskie pārskati**.</span><span class="sxs-lookup"><span data-stu-id="3d192-248">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="3d192-249">Atlasiet **Pārskatu konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="3d192-249">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="3d192-250">Ielādējiet konfigurācijas failus **Ārējās tirdzniecības metadati.xml** **Ārējās tirdzniecības modelis.xml** un **Ārējās tirdzniecības kartēšana.xml**, kas katra atkārto tālāk norādīto darbību ķēdi.</span><span class="sxs-lookup"><span data-stu-id="3d192-250">Load the **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml** configuration files repeating the following chain of steps for each of them:</span></span>

    1. <span data-ttu-id="3d192-251">Atlasiet **Maiņa**.</span><span class="sxs-lookup"><span data-stu-id="3d192-251">Select **Exchange**.</span></span>
    2. <span data-ttu-id="3d192-252">Atlasiet **Ielādēt no XML faila**.</span><span class="sxs-lookup"><span data-stu-id="3d192-252">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="3d192-253">Atlasiet **Pārlūkot** un atlasiet failu.</span><span class="sxs-lookup"><span data-stu-id="3d192-253">Select **Browse**, and select a file.</span></span>
    4. <span data-ttu-id="3d192-254">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3d192-254">Select **OK**.</span></span>

### <a name="register-the-connection-with-the-application"></a><span data-ttu-id="3d192-255">Reģistrējiet savienojumu ar programmu</span><span class="sxs-lookup"><span data-stu-id="3d192-255">Register the connection with the application</span></span>

1. <span data-ttu-id="3d192-256">Dodieties uz **Visas darbvietas \> Elektroniskie pārskati**.</span><span class="sxs-lookup"><span data-stu-id="3d192-256">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="3d192-257">Atlasiet **Savienotās programmas**.</span><span class="sxs-lookup"><span data-stu-id="3d192-257">Select **Connected applications**.</span></span>
3. <span data-ttu-id="3d192-258">Pārliecinieties, ka konfigurētā programma ir balstīta uz Microsoft Azure un ka tā ir pieejama RCS lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="3d192-258">Make sure that the configured application is based on Microsoft Azure, and that it is accessible in general to RCS users.</span></span> <span data-ttu-id="3d192-259">Pašreizējam RCS lietotājam ir arī jābūt piekļuvei konfigurētajai programmai un ir jābūt reģistrētam kā šīs programmas lietotājam ar lomu, kas dod viņam privilēģijas piekļūt programmas metadatiem.</span><span class="sxs-lookup"><span data-stu-id="3d192-259">The current RCS user must have access to the configured application being registered as a user of this application in a role that gives him or her privileges to access the application's metadata.</span></span>
4. <span data-ttu-id="3d192-260">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="3d192-260">Select **New**.</span></span>
5. <span data-ttu-id="3d192-261">Laukā **Nosaukums** ievadiet **MyConnectedApp** kā savienotās programmas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="3d192-261">In the **Name** field, enter **MyConnectedApp** as the name of the connected application.</span></span>
6. <span data-ttu-id="3d192-262">Laukā **Programma** norādiet programmas vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="3d192-262">In the **Application** field, specify the URL of the application.</span></span>
7. <span data-ttu-id="3d192-263">Laukā **Nomnieks** norādiet programmas nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="3d192-263">In the **Tenant** field, specify the provider of the application.</span></span>
8. <span data-ttu-id="3d192-264">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="3d192-264">Select **Save**.</span></span> 
9. <span data-ttu-id="3d192-265">Kad pārbaudāt savienojums ar konfigurēto programmu, lapā **Savienojuma izveide ar attālo programmu** atlasiet saiti **Atlasīt šeit, lai izveidotu savienojumu ar atlasīto attālo programmu**.</span><span class="sxs-lookup"><span data-stu-id="3d192-265">When you check the connection to the configured application, on the **Connect to remote application** page, select the **Select here to connect to selected remote application** link.</span></span> 
10. <span data-ttu-id="3d192-266">Atlasiet **Pārbaudīt savienojumu**, lai validētu piekļuvi konfigurētajai programmai.</span><span class="sxs-lookup"><span data-stu-id="3d192-266">Select **Check connection** to validate access to the configured application.</span></span>
11. <span data-ttu-id="3d192-267">Atlasiet **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="3d192-267">Select **Close**.</span></span>

<span data-ttu-id="3d192-268">Kad šī procedūra ir pabeigta un savienojuma validācija ir izdevusies, pašreizējā režģī konfigurētajai programmai tiks atjaunināta versija un nomnieka informācija.</span><span class="sxs-lookup"><span data-stu-id="3d192-268">After you complete this procedure and validation of the connection succeeds, the version and tenant details for the configured application will be updated in the current grid.</span></span>

### <a name="review-the-existing-model-mapping-configuration"></a><span data-ttu-id="3d192-269">Esošās modeļa kartēšanas konfigurācijas pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="3d192-269">Review the existing model mapping configuration</span></span>

1. <span data-ttu-id="3d192-270">Dodieties uz **Visas darbvietas \> Elektroniskie pārskati**.</span><span class="sxs-lookup"><span data-stu-id="3d192-270">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="3d192-271">Atlasiet **Pārskatu konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="3d192-271">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="3d192-272">Kokā atlasiet **Ārējās tirdzniecības modelis \> Ārējās tirdzniecības kartēšana**.</span><span class="sxs-lookup"><span data-stu-id="3d192-272">In the tree, select **Foreign trade model \> Foreign trade mapping**.</span></span>
4. <span data-ttu-id="3d192-273">Atlasiet kopsavilkuma cilni **Priekšnosacījumi**.</span><span class="sxs-lookup"><span data-stu-id="3d192-273">Select the **Prerequisites** FasTab.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3d192-274">Pašlaik šī kartēšana attiecas uz metadatu konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="3d192-274">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="3d192-275">Izstrādājot šī modeļa kartēšanu, tiks piedāvāti šīs konfigurācijas programmas metadati.</span><span class="sxs-lookup"><span data-stu-id="3d192-275">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

4. <span data-ttu-id="3d192-276">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="3d192-276">Select **Designer**.</span></span>
5. <span data-ttu-id="3d192-277">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="3d192-277">Select **Designer**.</span></span>
6. <span data-ttu-id="3d192-278">Kokā atlasiet **Dynamics 365 for Operations \> Tabulas ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="3d192-278">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
7. <span data-ttu-id="3d192-279">Atlasiet **Pievienot sakni**.</span><span class="sxs-lookup"><span data-stu-id="3d192-279">Select **Add root**.</span></span>
8. <span data-ttu-id="3d192-280">Laukā **Tabula** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3d192-280">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3d192-281">Pašlaik šī kartēšana attiecas uz metadatu konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="3d192-281">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="3d192-282">Izstrādājot šī modeļa kartēšanu, tiks piedāvāti šīs konfigurācijas programmas metadati.</span><span class="sxs-lookup"><span data-stu-id="3d192-282">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

9. <span data-ttu-id="3d192-283">Atlasiet **Atcelt**.</span><span class="sxs-lookup"><span data-stu-id="3d192-283">Select **Cancel**.</span></span>

### <a name="assign-the-connected-application-to-a-model-mapping"></a><span data-ttu-id="3d192-284">Savienotās programmas piešķiršana modeļa kartēšanai</span><span class="sxs-lookup"><span data-stu-id="3d192-284">Assign the connected application to a model mapping</span></span>

1. <span data-ttu-id="3d192-285">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="3d192-285">Select **Edit**.</span></span>
2. <span data-ttu-id="3d192-286">Laukā **Savienotā programma** atlasiet programmu **MyConnectedApp.**</span><span class="sxs-lookup"><span data-stu-id="3d192-286">In the **Connected application field**, select the **MyConnectedApp** application.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3d192-287">Šī kartēšana attiecas uz atlasītās savienotās programmas metadatiem.</span><span class="sxs-lookup"><span data-stu-id="3d192-287">This mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="3d192-288">Ja kartēšana attiecas vienlaikus uz metadatu konfigurāciju un uz savienoto programmu, tiks izmantoti savienotās programmas metadati.</span><span class="sxs-lookup"><span data-stu-id="3d192-288">If a mapping refers to the metadata configuration and the connected application at the same time, the metadata of the connected application will be used.</span></span>

3. <span data-ttu-id="3d192-289">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="3d192-289">Select **Designer**.</span></span>
4. <span data-ttu-id="3d192-290">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="3d192-290">Select **Designer**.</span></span>
5. <span data-ttu-id="3d192-291">Kokā atlasiet **Dynamics 365 for Operations \> Tabulas ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="3d192-291">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
6. <span data-ttu-id="3d192-292">Atlasiet **Pievienot sakni**.</span><span class="sxs-lookup"><span data-stu-id="3d192-292">Select **Add root**.</span></span>
7. <span data-ttu-id="3d192-293">Laukā **Tabula** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3d192-293">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3d192-294">Šobrīd tiek piedāvātas vairāk nekā divas programmas tabulas, jo šī kartēšana izmanto visus tai piešķirtās savienotās programmas metadatus.</span><span class="sxs-lookup"><span data-stu-id="3d192-294">At this point, more than two application tables are offered, because this mapping uses all the metadata of the connected application that has been assigned to it.</span></span>

8. <span data-ttu-id="3d192-295">Atlasiet **Atcelt**.</span><span class="sxs-lookup"><span data-stu-id="3d192-295">Select **Cancel**.</span></span>
9. <span data-ttu-id="3d192-296">Atlasiet **Validēt**.</span><span class="sxs-lookup"><span data-stu-id="3d192-296">Select **Validate**.</span></span>

<span data-ttu-id="3d192-297">Datu modeļa elementus tagad esat veiksmīgi saistījis ar datu avotu vienībām, kas aprakstītas, lietojot detalizētu informāciju par kartēšanai piešķirtās savienotās programmas metadatiem.</span><span class="sxs-lookup"><span data-stu-id="3d192-297">You've now bound elements of the data model to items of the data sources that are described by using details of the metadata of the connected application that has been assigned to this mapping.</span></span>

<span data-ttu-id="3d192-298">Ja ir jānovērtē šī modeļa kartēšana, izmantojot citas versijas programmas metadatus, reģistrējiet citu savienoto programmu, piešķiriet to šai modeļa kartēšanai un validējiet to ar jauniem metadatiem.</span><span class="sxs-lookup"><span data-stu-id="3d192-298">When you must evaluate this model mapping by using the metadata of a different version of the application, register another connected application, assign it to this model mapping, and validate it against the new metadata.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3d192-299">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="3d192-299">Additional resources</span></span>

<span data-ttu-id="3d192-300">Vai arī varat atskaņot uzdevuma ceļvedi **RCS izmantojamo programmas metadatu sagatavošana** programmā, kā arī uzdevuma ceļvežus **Piekļuve programmas metadatiem, izmantojot ER konfigurāciju** un **Piekļuve programmas metadatiem, izmantojot saistītas programmas** rīkā RCS.</span><span class="sxs-lookup"><span data-stu-id="3d192-300">Alternatively, you can play the **Prepare application metadata that can be used in RCS** task guide in the application as as well as the **Access application metadata by using an ER configuration** and **Access application metadata by using connected applications** task guides in RCS.</span></span> <span data-ttu-id="3d192-301">Šos uzdevumu ceļvežus var lejupielādēt lapā [Elektronisko pārskatu uzdevumu ceļvedis izmantošanai Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739).</span><span class="sxs-lookup"><span data-stu-id="3d192-301">These task guides can be downloaded from the [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page.</span></span>
