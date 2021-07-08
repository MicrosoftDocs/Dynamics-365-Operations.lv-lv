---
title: Elektronisko atskaišu veidošanas (ER) formāta failu izpildes uzraudzīšana, lai novērstu veiktspējas problēmas
description: Šajā tēmā ir sniegta informācija par to, kā izmantot veiktspējas izsekošanas līdzekli elektronisko pārskatu veidošanā (ER), lai novērstu veiktspējas problēmas.
author: NickSelin
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7fbec962fea374afdbabaad48a42dad380708678
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295577"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="d618e-103">ER formātu izpildes izsekošana, lai novērstu veiktspējas problēmas</span><span class="sxs-lookup"><span data-stu-id="d618e-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d618e-104">Elektronisko pārskatu veidošanas (ER) konfigurāciju izstrādes procesa ietvaros, lai izveidotu elektroniskus dokumentus, nosakiet metodi, kas tiek izmantota, lai iegūtu datus no programmas un ievadītu tos ģenerētajā izvadē.</span><span class="sxs-lookup"><span data-stu-id="d618e-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="d618e-105">ER veiktspējas izsekošanas līdzeklis palīdz ievērojami samazināt laiku un izmaksas, kas saistītas ar ER formāta izpildes informācijas vākšanu un tās izmantošanu, lai novērstu veiktspējas problēmas.</span><span class="sxs-lookup"><span data-stu-id="d618e-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="d618e-106">Šajā apmācībā ir sniegti norādījumi par to, kā informāciju par izpildīto ER formātu veiktspējas izsekošanu var izmantot, lai palīdzētu uzlabot veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="d618e-106">This tutorial provides guidelines about how to take performance traces for executed ER formats, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d618e-107">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="d618e-107">Prerequisites</span></span>

<span data-ttu-id="d618e-108">Lai izpildītu šajā apmācībā aprakstītos piemērus, jums ir nepieciešama tālāk norādītā piekļuve.</span><span class="sxs-lookup"><span data-stu-id="d618e-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="d618e-109">Piekļuve vienai no sekojošajām lomām:</span><span class="sxs-lookup"><span data-stu-id="d618e-109">Access to one of the following roles:</span></span>

    - <span data-ttu-id="d618e-110">Elektroniskā pārskata izstrādātājs</span><span class="sxs-lookup"><span data-stu-id="d618e-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="d618e-111">Elektronisko pārskatu veidošanas funkcionālais konsultants</span><span class="sxs-lookup"><span data-stu-id="d618e-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="d618e-112">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="d618e-112">System administrator</span></span>

- <span data-ttu-id="d618e-113">Piekļuve Regulatory Configuration Services (RCS) instancei, kas ir nodrošināta tam pašam nomniekam, kuram nodrošināta programmas instance, vienai no šādām lomām:</span><span class="sxs-lookup"><span data-stu-id="d618e-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as the application, for one of the following roles:</span></span>

    - <span data-ttu-id="d618e-114">Elektroniskā pārskata izstrādātājs</span><span class="sxs-lookup"><span data-stu-id="d618e-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="d618e-115">Elektronisko pārskatu veidošanas funkcionālais konsultants</span><span class="sxs-lookup"><span data-stu-id="d618e-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="d618e-116">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="d618e-116">System administrator</span></span>

<span data-ttu-id="d618e-117">Nepieciešams arī lejupielādēt un lokāli saglabāt tālāk norādītos failus.</span><span class="sxs-lookup"><span data-stu-id="d618e-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="d618e-118">Fails</span><span class="sxs-lookup"><span data-stu-id="d618e-118">File</span></span>                                  | <span data-ttu-id="d618e-119">Saturs</span><span class="sxs-lookup"><span data-stu-id="d618e-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="d618e-120">Veiktspējas izsekošanas modelis.versija.1</span><span class="sxs-lookup"><span data-stu-id="d618e-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="d618e-121">Parauga ER datu modeļa konfigurācija</span><span class="sxs-lookup"><span data-stu-id="d618e-121">Sample ER data model configuration</span></span>](https://download.microsoft.com/download/0/a/a/0aa84e48-8040-4c46-b542-e3bf15c9b2ad/Performancetracemodelversion.1.xml)    |
| <span data-ttu-id="d618e-122">Veiktspējas izsekošanas metadati.versija.1</span><span class="sxs-lookup"><span data-stu-id="d618e-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="d618e-123">Parauga ER metadatu konfigurācija</span><span class="sxs-lookup"><span data-stu-id="d618e-123">Sample ER metadata configuration</span></span>](https://download.microsoft.com/download/a/9/3/a937e8c4-1f8a-43e4-83ee-7d599cf7d983/Performancetracemetadataversion.1.xml)      |
| <span data-ttu-id="d618e-124">Veiktspējas izsekošanas kartējums.versija.1.1</span><span class="sxs-lookup"><span data-stu-id="d618e-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="d618e-125">Parauga ER modeļa kartējuma konfigurācija</span><span class="sxs-lookup"><span data-stu-id="d618e-125">Sample ER model mapping configuration</span></span>](https://download.microsoft.com/download/7/7/3/77379bdc-7b22-4cfc-9b64-a9147599f931/Performancetracemappingversion1.1.xml) |
| <span data-ttu-id="d618e-126">Veiktspējas izsekošanas formāts.versija.1.1</span><span class="sxs-lookup"><span data-stu-id="d618e-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="d618e-127">Parauga ER formāta konfigurācija</span><span class="sxs-lookup"><span data-stu-id="d618e-127">Sample ER format configuration</span></span>](https://download.microsoft.com/download/8/6/8/868ba581-5a06-459e-b173-fb00f038b37f/Performancetraceformatversion1.1.xml)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="d618e-128">Konfigurēt ER parametrus</span><span class="sxs-lookup"><span data-stu-id="d618e-128">Configure ER parameters</span></span>

<span data-ttu-id="d618e-129">Katra ER veiktspējas izsekošana, kas tiek ģenerēta programmā, tiek saglabāta kā izpildes žurnāla ieraksta pielikums.</span><span class="sxs-lookup"><span data-stu-id="d618e-129">Each ER performance trace that is generated in the application is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="d618e-130">Šo pielikumu pārvaldībai tiek izmantota dokumentu pārvaldības (Document Management — DM) struktūras.</span><span class="sxs-lookup"><span data-stu-id="d618e-130">The Document management (DM) framework is used to manage these attachments.</span></span> <span data-ttu-id="d618e-131">Vispirms ir jākonfigurē ER parametri, lai norādītu DM dokumenta tipu, kas jāizmanto veiktspējas izsekošanas pievienošanai.</span><span class="sxs-lookup"><span data-stu-id="d618e-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="d618e-132">Darbvietā **Elektronisko pārskatu veidošana** atlasiet saiti **Elektronisko pārskatu veidošanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="d618e-132">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="d618e-133">Pēc tam lapas **Elektronisko pārskatu veidošanas parametri** cilnes **Pielikumi** laukā **Citi** atlasiet DM dokumenta tipu, kas tiks izmantots veiktspējas izsekošanai.</span><span class="sxs-lookup"><span data-stu-id="d618e-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Elektronisko pārskatu veidošanas parametru lapa](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="d618e-135">Lai DM dokumenta tips būtu pieejams uzmeklēšanas laukā **Citi**, tas ir jākonfigurē lapā **Dokumentu tipi** (**Organizācijas administrēšana \> Dokumentu pārvaldība \> Dokumentu tipi**) šādā veidā:</span><span class="sxs-lookup"><span data-stu-id="d618e-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="d618e-136">**Klase:** Pievienot failu</span><span class="sxs-lookup"><span data-stu-id="d618e-136">**Class:** Attach file</span></span>
- <span data-ttu-id="d618e-137">**Grupa:** Fails</span><span class="sxs-lookup"><span data-stu-id="d618e-137">**Group:** File</span></span>

![Dokumentu veidu lapa](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="d618e-139">Atlasītajam dokumenta tipam jābūt pieejamam ikvienā pašreizējās instances uzņēmumā, jo DM pielikumi attiecas tikai uz konkrētu uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="d618e-139">The selected document type must be available in every company of the current instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="d618e-140">RCS parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="d618e-140">Configure RCS parameters</span></span>

<span data-ttu-id="d618e-141">ER veiktspējas izsekošana, kas tiek ģenerēta, tiks importēta RCS analīzes veikšanai, izmantojot ER formāta noformētāju un ER kartēšanas noformētāju.</span><span class="sxs-lookup"><span data-stu-id="d618e-141">ER performance traces that are generated will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="d618e-142">Tā kā ER veiktspējas izsekošana tiek uzglabāta kā izpildes žurnāla ieraksta pielikums, kas ir saistīts ar ER formātu, RCS parametri ir jākonfigurē iepriekš, lai norādītu DM dokumenta tipu, kas jāizmanto veiktspējas izsekošanas pievienošanai.</span><span class="sxs-lookup"><span data-stu-id="d618e-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="d618e-143">Tādā RCS instancē, kas nodrošināta jūsu uzņēmumam, darbvietā **Elektronisko pārskatu veidošana** atlasiet **Elektronisko pārskatu veidošanas parametri.**</span><span class="sxs-lookup"><span data-stu-id="d618e-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="d618e-144">Pēc tam lapas **Elektronisko pārskatu veidošanas parametri** cilnes **Pielikumi** laukā **Citi** atlasiet DM dokumenta tipu, kas tiks izmantots veiktspējas izsekošanai.</span><span class="sxs-lookup"><span data-stu-id="d618e-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Lapa Elektronisko pārskatu veidošanas parametri pakalpojumā RCS](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="d618e-146">Lai DM dokumenta tips būtu pieejams uzmeklēšanas laukā **Citi**, tas ir jākonfigurē lapā **Dokumentu tipi** (**Organizācijas administrēšana \> Dokumentu pārvaldība \> Dokumentu tipi**) šādā veidā:</span><span class="sxs-lookup"><span data-stu-id="d618e-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="d618e-147">**Klase:** Pievienot failu</span><span class="sxs-lookup"><span data-stu-id="d618e-147">**Class:** Attach file</span></span>
- <span data-ttu-id="d618e-148">**Grupa:** Fails</span><span class="sxs-lookup"><span data-stu-id="d618e-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="d618e-149">ER risinājuma izstrāde</span><span class="sxs-lookup"><span data-stu-id="d618e-149">Design an ER solution</span></span>

<span data-ttu-id="d618e-150">Pieņemsim, ka esat sācis izstrādāt jaunu ER risinājumu, lai ģenerētu jaunu pārskatu, kurā parādītas kreditoru darbības.</span><span class="sxs-lookup"><span data-stu-id="d618e-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="d618e-151">Pašlaik varat atrast atlasītā kreditora transakcijas lapā **Kreditoru transakcijas** (pārejiet uz **Parādi kreditoriem \> Kreditori \> Visi kreditori**, atlasiet kreditoru un pēc tam darbību rūtī, cilnē **Kreditors**, grupā **Transakcijas** atlasiet vienumu **Transakcijas**).</span><span class="sxs-lookup"><span data-stu-id="d618e-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="d618e-152">Tomēr ir nepieciešams, lai visas kreditoru transakcijas vienlaicīgi būtu vienā elektroniskajā dokumentā XML formātā.</span><span class="sxs-lookup"><span data-stu-id="d618e-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="d618e-153">Šis risinājums sastāv no vairākām ER konfigurācijām, kas ietver nepieciešamo datu modeli, metadatus, modeļa kartējumu un formāta komponentus.</span><span class="sxs-lookup"><span data-stu-id="d618e-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="d618e-154">Piesakieties RCS instancē, kas nodrošināta jūsu uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="d618e-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="d618e-155">Šajā apmācībā jūs izveidosit un modificēsit nepieciešamās konfigurācijas parauga uzņēmumam **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="d618e-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="d618e-156">Tādēļ pārliecinieties, ka šis konfigurācijas nodrošinātājs ir pievienots RCS un atlasīts kā aktīvs.</span><span class="sxs-lookup"><span data-stu-id="d618e-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="d618e-157">Norādījumus skatiet procedūrā [Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="d618e-157">For instructions, see the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>
3. <span data-ttu-id="d618e-158">Darbvietā **Elektroniskie pārskati** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="d618e-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="d618e-159">Lapā **Konfigurācijas** importējiet ER konfigurācijas, kuras lejupielādējāt kā priekšnosacījumu pakalpojumā RCS, šādā secībā: datu modelis, metadati, modeļa kartējums, formāts.</span><span class="sxs-lookup"><span data-stu-id="d618e-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="d618e-160">Katrai konfigurācijai rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="d618e-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="d618e-161">Darbību rūtī atlasiet **Mainīt \> Ielādēt no XML faila**.</span><span class="sxs-lookup"><span data-stu-id="d618e-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="d618e-162">Atlasiet **Pārlūkot**, lai atlasītu atbilstošu failu nepieciešamajai ER konfigurācijai XML formātā.</span><span class="sxs-lookup"><span data-stu-id="d618e-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="d618e-163">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d618e-163">Select **OK**.</span></span>

    ![Lapa Konfigurācijas pakalpojumā RCS](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="d618e-165">Palaidiet ER risinājumu, lai izsekotu izpildi</span><span class="sxs-lookup"><span data-stu-id="d618e-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="d618e-166">Pieņemsim, ka esat pabeidzis izstrādāt ER risinājuma pirmo versiju.</span><span class="sxs-lookup"><span data-stu-id="d618e-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="d618e-167">Tagad vēlaties to pārbaudīt savā instancē un analizēt izpildes veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="d618e-167">You now want to test it in your instance and analyze execution performance.</span></span>

### <a name="import-an-er-configuration-from-rcs-into-finance-and-operations"></a><a id='import-configuration'></a><span data-ttu-id="d618e-168">ER konfigurācijas importēšana no RCS uz Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d618e-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="d618e-169">Piesakieties savā programmas instancē.</span><span class="sxs-lookup"><span data-stu-id="d618e-169">Sign in to your application instance.</span></span>
2. <span data-ttu-id="d618e-170">Šīs apmācības ietvaros importēsit konfigurācijas no savas RCS instances (kur izstrādājat ER komponentus) savā instancē (kur tos testējat un izmantojat).</span><span class="sxs-lookup"><span data-stu-id="d618e-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your instance (where you test and finally use them).</span></span> <span data-ttu-id="d618e-171">Tāpēc ir jāpārliecinās, ka ir sagatavoti visi vajadzīgie artefakti.</span><span class="sxs-lookup"><span data-stu-id="d618e-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="d618e-172">Norādījumus skatiet procedūrā [Importēt elektronisko pārskatu (ER) konfigurācijas no Regulatory Configuration Services (RCS)](rcs-download-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="d618e-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md) procedure.</span></span>
3. <span data-ttu-id="d618e-173">Veiciet šādas darbības, lai importētu konfigurācijas no RCS programmā.</span><span class="sxs-lookup"><span data-stu-id="d618e-173">Follow these steps to import the configurations from RCS into the application:</span></span>

    1. <span data-ttu-id="d618e-174">Darbvietā **Elektronisko pārskatu veidošana**, **Litware, Inc.** konfigurācijas nodrošinātāja elementā atlasiet **Repozitoriji**.</span><span class="sxs-lookup"><span data-stu-id="d618e-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="d618e-175">Lapā **Konfigurācijas repozitorijs** atlasiet repozitoriju ar tipu **RCS** un pēc tam atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="d618e-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="d618e-176">Kopsavilkuma cilnē **Konfigurācijas** atlasiet konfigurāciju **Veiktspējas izsekošanas formāts**.</span><span class="sxs-lookup"><span data-stu-id="d618e-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="d618e-177">Kopsavilkuma cilnē **Versijas** atlasiet atlasītās konfigurācijas versiju **1.1** un pēc tam atlasiet **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="d618e-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![Konfigurācijas repozitorijas lapa.](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="d618e-179">Datu modeļa un modeļa kartējuma konfigurāciju atbilstošās versijas automātiski tiek importētas kā priekšnosacījumi importētajai ER formāta konfigurācijai.</span><span class="sxs-lookup"><span data-stu-id="d618e-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="d618e-180">ER veiktspējas izsekošanas ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="d618e-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="d618e-181">Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="d618e-181">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="d618e-182">Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.</span><span class="sxs-lookup"><span data-stu-id="d618e-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="d618e-183">Dialoglodziņa **Lietotāja parametri** sadaļā **Izpildes izsekošana** rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="d618e-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="d618e-184">Laukā **Izpildes izsekošanas formāts** norādiet ģenerētās veiktspējas izsekošanas formātu, kurā ir jāuzglabā izpildes informācija ER formāta un kartēšanas elementiem:</span><span class="sxs-lookup"><span data-stu-id="d618e-184">In the **Execution trace format** field, specify the format of the generated performance trace that the execution details should be stored in for ER format and mapping elements:</span></span>

        - <span data-ttu-id="d618e-185">**Atkļūdošanas izsekošanas formāts** – atlasiet šo vērtību, ja plānojat interaktīvi palaist ER formātu, kam ir īss izpildes laiks.</span><span class="sxs-lookup"><span data-stu-id="d618e-185">**Debug trace format** – Select this value if you plan to interactively run an ER format that has a short execution time.</span></span> <span data-ttu-id="d618e-186">Pēc tam tiek sākta datu kolekcija par ER formāta izpildi.</span><span class="sxs-lookup"><span data-stu-id="d618e-186">The collection of details about ER format execution is then started.</span></span> <span data-ttu-id="d618e-187">Atlasot šo vērtību, veiktspējas izsekošana apkopo informāciju par laiku, kas tiek patērēts šādām darbībām:</span><span class="sxs-lookup"><span data-stu-id="d618e-187">When this value is selected, the performance trace collects information about the time that is spent on the following actions:</span></span>

            - <span data-ttu-id="d618e-188">Katra datu avota palaišana modeļa kartējumā, kas tiek izsaukts datu iegūšanai</span><span class="sxs-lookup"><span data-stu-id="d618e-188">Running each data source in the model mapping that is called to get data</span></span>
            - <span data-ttu-id="d618e-189">Katra formāta vienuma apstrāde, lai ievadītu datus ģenerētajā izvadē</span><span class="sxs-lookup"><span data-stu-id="d618e-189">Processing each format item to enter data in the output that is generated</span></span>

            <span data-ttu-id="d618e-190">Ja atlasāt vērtību **Atkļūdošanas izsekošanas formāts**, varat analizēt izsekošanas saturu ER operāciju veidotājā.</span><span class="sxs-lookup"><span data-stu-id="d618e-190">If you select the **Debug trace format** value, you can analyze the content of the trace in the ER Operation designer.</span></span> <span data-ttu-id="d618e-191">Tur varat skatīt ER formātu vai kartēšanas elementus, kas ir iepriekš minēti izsekošanā.</span><span class="sxs-lookup"><span data-stu-id="d618e-191">There, you can view the ER format or mapping elements that are mentioned in the trace.</span></span>

        - <span data-ttu-id="d618e-192">**Apkopotais izsekošanas formāts** – atlasiet šo vērtību, ja plānojat palaist ER formātu, kam ir ilgs izpildes laiks partijas režīmā.</span><span class="sxs-lookup"><span data-stu-id="d618e-192">**Aggregated trace format** – Select this value if you plan to run an ER format that has a long execution time in batch mode.</span></span> <span data-ttu-id="d618e-193">Pēc tam tiek sākta apkopoto datu kolekcija par ER formāta izpildi.</span><span class="sxs-lookup"><span data-stu-id="d618e-193">The collection of the aggregated details about ER format execution is then started.</span></span> <span data-ttu-id="d618e-194">Atlasot šo vērtību, veiktspējas izsekošana apkopo informāciju par laiku, kas tiek patērēts šādām darbībām:</span><span class="sxs-lookup"><span data-stu-id="d618e-194">When this value is selected, the performance trace collects information about the time that is spent on the following actions:</span></span>

            - <span data-ttu-id="d618e-195">Katra datu avota palaišana modeļa kartējumā, kas tiek izsaukts datu iegūšanai</span><span class="sxs-lookup"><span data-stu-id="d618e-195">Running each data source in the model mapping that is called to get data</span></span>
            - <span data-ttu-id="d618e-196">Katra datu avota palaišana formata kartējumā, kas tiek izsaukts datu iegūšanai</span><span class="sxs-lookup"><span data-stu-id="d618e-196">Running each data source in the format mapping that is called to get data</span></span>
            - <span data-ttu-id="d618e-197">Katra formāta vienuma apstrāde, lai ievadītu datus ģenerētajā izvadē</span><span class="sxs-lookup"><span data-stu-id="d618e-197">Processing each format item to enter data in the output that is generated</span></span>

            <span data-ttu-id="d618e-198">Vērtība **Apkopotās izsekošanas formāts** ir pieejama Microsoft Dynamics 365 Finance versijā 10.0.20 vai jaunākā versijā.</span><span class="sxs-lookup"><span data-stu-id="d618e-198">The **Aggregated trace format** value is available in Microsoft Dynamics 365 Finance version 10.0.20 and later.</span></span>

            <span data-ttu-id="d618e-199">ER formāta veidotājā un ER modeļu kartēšanas veidotājā varat apskatīt kopējo viena komponenta izpildes laiku.</span><span class="sxs-lookup"><span data-stu-id="d618e-199">In the ER format designer and ER model mapping designer, you can view the total execution time for a single component.</span></span> <span data-ttu-id="d618e-200">Papildus tam, izsekošana satur detaļas par izpildi, piemēram, izpildes skaitu un minimālo un maksimālo vienas izpildes laiku.</span><span class="sxs-lookup"><span data-stu-id="d618e-200">Additionally, the trace contains details about the execution, such as the number of executions, and the minimum and maximum time of a single execution.</span></span>

            > [!NOTE]
            > <span data-ttu-id="d618e-201">Šī izsekošana tiek apkopota, balstoties uz izsekoto komponentu ceļu.</span><span class="sxs-lookup"><span data-stu-id="d618e-201">This trace is collected based on the traced components path.</span></span> <span data-ttu-id="d618e-202">Tāpēc statistika var būt nepareiza, ja vienam pamatkomponentam ir vairāki nenosaukti pakārtotie komponenti vai ja vairākiem pakārtotajiem komponentiem ir vienāds nosaukums.</span><span class="sxs-lookup"><span data-stu-id="d618e-202">Therefore, the statistics might be incorrect when a single parent component contains several unnamed child components, or when several child components have the same name.</span></span>

    2. <span data-ttu-id="d618e-203">Iestatiet tālāk minētajām opcijām vienumu **Jā**, lai apkopotu noteiktu informāciju par ER modeļa kartējuma un ER formāta komponentu izpildi:</span><span class="sxs-lookup"><span data-stu-id="d618e-203">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="d618e-204">**Apkopot vaicājumu statistiku** — ja šī opcija ir ieslēgta, veiktspējas izsekošanā tiks apkopota šāda informācija:</span><span class="sxs-lookup"><span data-stu-id="d618e-204">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="d618e-205">Datu avotu veikto datu bāzes izsaukumu skaits</span><span class="sxs-lookup"><span data-stu-id="d618e-205">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="d618e-206">Datu bāzes dublētu izsaukumu skaits</span><span class="sxs-lookup"><span data-stu-id="d618e-206">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="d618e-207">Informācija par SQL priekšrakstiem, kas izmantoti datu bāzes izsaukumu veikšanai</span><span class="sxs-lookup"><span data-stu-id="d618e-207">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="d618e-208">**Izsekot kešdarbes piekļuvi** — ja šī opcija ir ieslēgta, veiktspējas izsekošanā tiks apkopota informācija par ER modeļa kartējuma kešatmiņas izmantošanu.</span><span class="sxs-lookup"><span data-stu-id="d618e-208">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="d618e-209">**Izsekot datu piekļuvi** — ja šī opcija ir ieslēgta, veiktspējas izsekošanā tiks apkopota informācija par datu bāzes izsaukumu skaitu izpildītajiem datu avotiem, kas atbilst tipam “ierakstu saraksts”.</span><span class="sxs-lookup"><span data-stu-id="d618e-209">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="d618e-210">**Izsekot saraksta uzskaitījumu** — ja šī opcija ir ieslēgta, veiktspējas izsekošanā tiks apkopota informācija par ierakstu skaitu, kas pieprasīti no datu avotiem, kuri atbilst tipam “ierakstu saraksts”.</span><span class="sxs-lookup"><span data-stu-id="d618e-210">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d618e-211">Parametri dialoglodziņā **Lietotāja parametri** dialoglodziņā ir raksturīgi lietotājam un pašreizējam uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="d618e-211">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![Lietotāja parametru dialoglodziņš](./media/GER-PerfTrace-GER-UserParameters.png)

### <a name="run-the-er-format"></a><a id='run-format'></a><span data-ttu-id="d618e-213">ER formāta palaišana</span><span class="sxs-lookup"><span data-stu-id="d618e-213">Run the ER format</span></span>

1. <span data-ttu-id="d618e-214">Atlasiet **DEMF** uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="d618e-214">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="d618e-215">Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="d618e-215">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="d618e-216">Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Veiktspējas izsekošanas formāts**.</span><span class="sxs-lookup"><span data-stu-id="d618e-216">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="d618e-217">Darbību rūtī atlasiet **Palaist**.</span><span class="sxs-lookup"><span data-stu-id="d618e-217">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="d618e-218">Ņemiet vērā, ka ģenerētajā failā ir ietverta informācija par 265 transakcijām sešiem kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="d618e-218">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="d618e-219">Izpildes izsekošanas pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="d618e-219">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><a id='export-trace'></a><span data-ttu-id="d618e-220">Eksportēt ģenerēto izsekošanu no programmas</span><span class="sxs-lookup"><span data-stu-id="d618e-220">Export the generated trace from the application</span></span>

<span data-ttu-id="d618e-221">Veiktspējas izsekošana ir atdalīta no avota ER formāta, un to var serializēt ārējā zip failā.</span><span class="sxs-lookup"><span data-stu-id="d618e-221">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="d618e-222">Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas atkļūdošanas žurnāli**.</span><span class="sxs-lookup"><span data-stu-id="d618e-222">Go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="d618e-223">Lapā **Elektronisko pārskatu palaišanas žurnāli**, kreisajā rūtī, laukā **Konfigurācijas nosaukums** atlasiet **Veiktspējas izsekošanas formāts**, lai atrastu žurnāla ierakstus, kas ģenerēti, izpildot konfigurāciju **Veiktspējas izsekošanas formāts**.</span><span class="sxs-lookup"><span data-stu-id="d618e-223">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="d618e-224">Atlasiet pogu **Pielikumi** (papīra saspraudes simbols) lapas augšējā labajā stūrī vai nospiediet **Ctrl+Shift+A**.</span><span class="sxs-lookup"><span data-stu-id="d618e-224">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![Poga Pielikumi lapā Elektronisko pārskatu palaišanas žurnāli](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="d618e-226">Lapas **Elektronisko pārskatu palaišanas žurnālu pielikumi** darbību rūtī atlasiet **Atvērt**, lai iegūtu veiktspējas izsekošanu kā zip failu un saglabātu to lokāli.</span><span class="sxs-lookup"><span data-stu-id="d618e-226">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![Elektronisko pārskatu palaisanas žurnālu pielikumi](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="d618e-228">Ģenerētajai izsekošanai ir atsauce uz avota ER pārskatu, izmantojot unikālu pārskata identifikatoru tikai **GUID** formātā.</span><span class="sxs-lookup"><span data-stu-id="d618e-228">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="d618e-229">Formāta versijas numerācija netiek ņemta vērā.</span><span class="sxs-lookup"><span data-stu-id="d618e-229">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="d618e-230">Ņemiet vērā, ka saistība starp veiktspējas izsekošanu, kas ir ģenerēta izpildītajam ER formātam, un ER modeļa kartējumu ir balstīta uz izmantoto saknes deskriptoru un kopējo datu modeli.</span><span class="sxs-lookup"><span data-stu-id="d618e-230">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="d618e-231">Formāta un modeļa kartējuma versijas numerācija netiek ņemta vērā.</span><span class="sxs-lookup"><span data-stu-id="d618e-231">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="d618e-232">Modeļa kartējuma karodziņa **Modeļa kartējuma noklusējums** iestatījums arī netiek ņemts vērā.</span><span class="sxs-lookup"><span data-stu-id="d618e-232">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><a id='import-trace'></a><span data-ttu-id="d618e-233">Importēt ģenerēto izsekošanu RCS</span><span class="sxs-lookup"><span data-stu-id="d618e-233">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="d618e-234">Pakalpojuma RCS darbvietā **Elektroniskie pārskati** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="d618e-234">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="d618e-235">Lapā **Konfigurācijas**, konfigurāciju kokā izvērsiet vienumu **Veiktspējas izsekošanas modelis** un atlasiet vienumu **Veiktspējas izsekošanas formāts**.</span><span class="sxs-lookup"><span data-stu-id="d618e-235">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="d618e-236">Darbību rūtī atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="d618e-236">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="d618e-237">Lapā **Formāta noformētājs**, darbību rūtī atlasiet **Veiktspējas izsekošana**.</span><span class="sxs-lookup"><span data-stu-id="d618e-237">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="d618e-238">Dialoglodziņā **Veiktspējas izsekošanas rezultātu iestatījumi** atlasiet **Importēt veiktspējas izsekošanu**.</span><span class="sxs-lookup"><span data-stu-id="d618e-238">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="d618e-239">Lai atlasītu iepriekš eksportētu .axtr failu, atlasiet **Pārlūkot** .</span><span class="sxs-lookup"><span data-stu-id="d618e-239">Select **Browse** to select the zip file that you exported earlier.</span></span>
7. <span data-ttu-id="d618e-240">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d618e-240">Select **OK**.</span></span>

    ![Dialoglodziņš Veiktspējas izsekošanas rezultātu iestatījumi pakalpojumā RCS](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="d618e-242">Veiktspējas izsekošanas izmantošana analīzes veikšanai pakalpojumā RCS — formāta izpilde</span><span class="sxs-lookup"><span data-stu-id="d618e-242">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="d618e-243">Pakalpojumā RCS, lapā **Formāta noformētājs** atlasiet **Izvērst/sakļaut**, lai izvērstu visu formāta vienumu saturu.</span><span class="sxs-lookup"><span data-stu-id="d618e-243">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="d618e-244">Ņemiet vērā, ka dažiem pašreizējā formāta vienumiem tiek rādīta papildu informācija:</span><span class="sxs-lookup"><span data-stu-id="d618e-244">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="d618e-245">Faktiskais laiks, kas patērēts, ievadot datus ģenerētajā izvadē, izmantojot formāta vienumu</span><span class="sxs-lookup"><span data-stu-id="d618e-245">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="d618e-246">Tas pats laiks, kas izteikts procentos no kopējā laika, kurš patērēts, ģenerējot visu izvadi</span><span class="sxs-lookup"><span data-stu-id="d618e-246">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![Formāta noformētāja lapa pakalpojumā RCS](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="d618e-248">Aizveriet lapu **Formāta noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="d618e-248">Close **Format designer** page.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><a id='use-trace'></a><span data-ttu-id="d618e-249">Veiktspējas izsekošanas izmantošana analīzes veikšanai pakalpojumā RCS — modeļa kartējums</span><span class="sxs-lookup"><span data-stu-id="d618e-249">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="d618e-250">Pakalpojuma RCS lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Veiktspējas izsekošanas kartējums**.</span><span class="sxs-lookup"><span data-stu-id="d618e-250">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="d618e-251">Darbību rūtī atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="d618e-251">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="d618e-252">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="d618e-252">Select **Designer**.</span></span>
4. <span data-ttu-id="d618e-253">Lapā **Modeļa kartējuma noformētājs**, darbību rūtī atlasiet **Veiktspējas izsekošana**.</span><span class="sxs-lookup"><span data-stu-id="d618e-253">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="d618e-254">Atlasiet iepriekš importēto izsekošanu.</span><span class="sxs-lookup"><span data-stu-id="d618e-254">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="d618e-255">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d618e-255">Select **OK**.</span></span>

<span data-ttu-id="d618e-256">Ņemiet vērā, ka kļūst pieejama jauna informācija par dažiem pašreizējā modeļa kartējuma datu avota vienumiem:</span><span class="sxs-lookup"><span data-stu-id="d618e-256">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="d618e-257">Faktiskais laiks, kas patērēts, iegūstot datus, izmantojot datu avotu</span><span class="sxs-lookup"><span data-stu-id="d618e-257">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="d618e-258">Tas pats laiks, kas izteikts procentos no kopējā laika, kurš patērēts, palaižot visu modeļa kartējumu</span><span class="sxs-lookup"><span data-stu-id="d618e-258">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="d618e-259">Ņemiet vērā, ka ER jūs informē par to, ka pašreizējais modeļa kartējums dublē datu bāzes pieprasījumus, kamēr tiek izpildīts VendTable/\<Relations/VendTrans.VendTable\_AccountNum datu avots.</span><span class="sxs-lookup"><span data-stu-id="d618e-259">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="d618e-260">Šāda dublēšana notiek tāpēc, ka kreditoru transakciju saraksts tiek izsaukts divas reizes katram atkārtotajam kreditora ierakstam:</span><span class="sxs-lookup"><span data-stu-id="d618e-260">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="d618e-261">Viens izsaukums tiek veikts, lai ievadītu informāciju par katru transakciju datu modelī, pamatojoties uz konfigurētajiem saistījumiem.</span><span class="sxs-lookup"><span data-stu-id="d618e-261">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="d618e-262">Viens izsaukums tiek veikts, lai ievadītu aprēķināto transakciju skaitu katram kreditoram datu modelī.</span><span class="sxs-lookup"><span data-stu-id="d618e-262">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![Ziņojums par datu bāzes pieprasījumu dublikātiem lapā Modeļa kartējuma noformētājs pakalpojumā RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="d618e-264">Vērtība **\[Q:530\]** norāda, ka VendTrans tabula tika izsaukta 530 reizes, lai atgrieztu ierakstu no šīs tabulas uz VendTable/\<Relations/VendTrans.VendTable\_AccountNum datu avotu.</span><span class="sxs-lookup"><span data-stu-id="d618e-264">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="d618e-265">Vērtība **\[530\]** norāda, ka VendTable/\<Relations/VendTrans.VendTable\_AccountNum datu avots tika izsaukts 530 reizes, lai atgrieztu ierakstu no šī datu avota un ievadītu tā informāciju datu modelī.</span><span class="sxs-lookup"><span data-stu-id="d618e-265">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="d618e-266">Ieteicams izmantot kešdarbi VendTable/\<Relations/VendTrans.VendTable\_AccountNum datu avotam, lai samazinātu izsaukumu skaitu, kas veikti, lai iegūtu informāciju par 265 transakcijām un palīdzētu uzlabot modeļa kartējuma veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="d618e-266">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="d618e-267">Tas arī var būt noderīgi, lai samazinātu LedgerTransTypeList datu avotam veikto izsaukumu skaitu.</span><span class="sxs-lookup"><span data-stu-id="d618e-267">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="d618e-268">Šis datu avots tiek izmantots, lai katru **LedgerTransType** uzskaitījuma vērtību saistītu ar tā etiķeti.</span><span class="sxs-lookup"><span data-stu-id="d618e-268">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="d618e-269">Izmantojot šo datu avotu, varat atrast atbilstošu etiķeti un ievadīt to katras kreditora transakcijas datu modelī.</span><span class="sxs-lookup"><span data-stu-id="d618e-269">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="d618e-270">Pašreizējais izsaukumu skaits šim datu avotam (9027) ir diezgan liels 265 transakcijām.</span><span class="sxs-lookup"><span data-stu-id="d618e-270">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![Lapa Modeļa kartējuma noformētājs pakalpojumā RCS, kurā norādīti 9027 izsaukumi uz datu avotu](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="d618e-272">Modeļa kartējuma uzlabošana, pamatojoties uz informāciju no izpildes izsekošanas</span><span class="sxs-lookup"><span data-stu-id="d618e-272">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="d618e-273">Modeļa kartējuma loģikas modificēšana</span><span class="sxs-lookup"><span data-stu-id="d618e-273">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="d618e-274">Veiciet šīs darbības, lai izmantotu kešdarbi, lai palīdzētu novērst dublētus izsaukumus datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="d618e-274">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="d618e-275">Pakalpojuma RCS lapā **Modeļa kartējuma noformētājs**, rūtī **Datu avoti** atlasiet vienumu **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="d618e-275">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="d618e-276">Atlasiet **Kešatmiņa**.</span><span class="sxs-lookup"><span data-stu-id="d618e-276">Select **Cache**.</span></span>
    3. <span data-ttu-id="d618e-277">Izvērsiet vienumu **VendTable**, izvērsiet “viens pret daudziem” relāciju sarakstu VendTable datu avotam (vienums **\<Relācijas** ) un atlasiet vienumu **VendTrans.VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="d618e-277">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="d618e-278">Atlasiet **Kešatmiņa**.</span><span class="sxs-lookup"><span data-stu-id="d618e-278">Select **Cache**.</span></span>

    ![Kešdarbes iestatīšana, lai palīdzētu novērst dublētus izsaukumus](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="d618e-280">Veiciet šīs darbības, lai LedgerTransTypeList datu avotu iekļautu VendTable datu avota tvērumā.</span><span class="sxs-lookup"><span data-stu-id="d618e-280">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="d618e-281">Rūtī **Datu avota tipi** izvērsiet vienumu **Funkcijas** un atlasiet vienumu **Aprēķinātais lauks**.</span><span class="sxs-lookup"><span data-stu-id="d618e-281">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="d618e-282">Rūtī **Datu avoti** atlasiet vienumu **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="d618e-282">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="d618e-283">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="d618e-283">Select **Add**.</span></span>
    4. <span data-ttu-id="d618e-284">Laukā **Nosaukums** ievadiet **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="d618e-284">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="d618e-285">Atlasiet **Rediģēt formulu**.</span><span class="sxs-lookup"><span data-stu-id="d618e-285">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="d618e-286">Laukā **Formula** ievadiet **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="d618e-286">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="d618e-287">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d618e-287">Select **Save**.</span></span>
    8. <span data-ttu-id="d618e-288">Aizveriet lapu **Formulas redaktors**.</span><span class="sxs-lookup"><span data-stu-id="d618e-288">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="d618e-289">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d618e-289">Click **OK**.</span></span>

3. <span data-ttu-id="d618e-290">Veiciet šīs darbības, lai veiktu lauka **\$TransType** kešdarbi.</span><span class="sxs-lookup"><span data-stu-id="d618e-290">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="d618e-291">Atlasiet vienumu **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="d618e-291">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="d618e-292">Atlasiet **Kešatmiņa**.</span><span class="sxs-lookup"><span data-stu-id="d618e-292">Select **Cache**.</span></span>
    3. <span data-ttu-id="d618e-293">Atlasiet vienumu **VendTable.\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="d618e-293">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="d618e-294">Atlasiet **Kešatmiņa**.</span><span class="sxs-lookup"><span data-stu-id="d618e-294">Select **Cache**.</span></span>

    ![Kešdarbes iestatīšana laukam $TransType](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="d618e-296">Veiciet šīs darbības, lai mainītu lauku **\$TransTypeRecord**, lai tas sāktu izmantot kešoto lauku **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="d618e-296">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="d618e-297">Rūtī **Datu avoti** izvērsiet vienumu **VendTable**, izvērsiet vienumu **\<Relācijas**, izvērsiet vienumu **VendTrans.VendTable\_AccountNum** un atlasiet vienumu **VendTable.VendTrans.VendTable\_AccountNum.\$TransTypeRecord**.</span><span class="sxs-lookup"><span data-stu-id="d618e-297">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="d618e-298">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="d618e-298">Select **Edit**.</span></span>
    3. <span data-ttu-id="d618e-299">Atlasiet **Rediģēt formulu**.</span><span class="sxs-lookup"><span data-stu-id="d618e-299">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="d618e-300">Laukā **Formula** atrodiet šādu izteiksmi:</span><span class="sxs-lookup"><span data-stu-id="d618e-300">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="d618e-301">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="d618e-301">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="d618e-302">Laukā **Formula** ievadiet šādu izteiksmi:</span><span class="sxs-lookup"><span data-stu-id="d618e-302">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="d618e-303">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span><span class="sxs-lookup"><span data-stu-id="d618e-303">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="d618e-304">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d618e-304">Select **Save**.</span></span>
    7. <span data-ttu-id="d618e-305">Aizveriet lapu **Formulas redaktors**.</span><span class="sxs-lookup"><span data-stu-id="d618e-305">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="d618e-306">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d618e-306">Select **OK**.</span></span>

5. <span data-ttu-id="d618e-307">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d618e-307">Select **Save**.</span></span>
6. <span data-ttu-id="d618e-308">Aizveriet lapu **Modeļa kartējuma noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="d618e-308">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="d618e-309">Aizveriet lapu **Modeļa kartējumi**.</span><span class="sxs-lookup"><span data-stu-id="d618e-309">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="d618e-310">ER modeļa kartējuma modificētās versijas pabeigšana</span><span class="sxs-lookup"><span data-stu-id="d618e-310">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="d618e-311">Pakalpojuma RCS lapā **Konfigurācijas**, kopsavilkuma cilnē **Versijas** atlasiet konfigurācijas **Veiktspējas izsekošanas kartējums** versiju **1.2**.</span><span class="sxs-lookup"><span data-stu-id="d618e-311">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="d618e-312">Atlasiet **Mainīt statusu**.</span><span class="sxs-lookup"><span data-stu-id="d618e-312">Select **Change status**.</span></span>
3. <span data-ttu-id="d618e-313">Atlasiet **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="d618e-313">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a><span data-ttu-id="d618e-314">Modificētās ER modeļa kartējuma konfigurācijas importēšana no RCS programmā</span><span class="sxs-lookup"><span data-stu-id="d618e-314">Import the modified ER model mapping configuration from RCS into the application</span></span>

<span data-ttu-id="d618e-315">Atkārtojiet šīs tēmas iepriekšējā sadaļā [ER konfigurācijas importēšana no pakalpojuma RCS programmā Finance and Operations](#import-configuration) minētās darbības, lai importētu konfigurācijas **Veiktspējas izsekošanas kartējums** versiju 1.2.</span><span class="sxs-lookup"><span data-stu-id="d618e-315">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="d618e-316">Modificētā ER risinājuma palaišana, lai izsekotu izpildi</span><span class="sxs-lookup"><span data-stu-id="d618e-316">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="d618e-317">ER formāta palaišana</span><span class="sxs-lookup"><span data-stu-id="d618e-317">Run the ER format</span></span>

<span data-ttu-id="d618e-318">Atkārtojiet šīs tēmas iepriekšējā sadaļā [ER formāta palaišana](#run-format) minētās darbības, lai ģenerētu jaunu veiktspējas izsekošanu.</span><span class="sxs-lookup"><span data-stu-id="d618e-318">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="work-with-the-execution-trace"></a><span data-ttu-id="d618e-319">Darbs ar izpildes izsekošanu</span><span class="sxs-lookup"><span data-stu-id="d618e-319">Work with the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><span data-ttu-id="d618e-320">Eksportēt ģenerēto izsekošanu no programmas</span><span class="sxs-lookup"><span data-stu-id="d618e-320">Export the generated trace from the application</span></span>

<span data-ttu-id="d618e-321">Atkārtojiet šīs tēmas iepriekšējā sadaļā [Eksportēt ģenerēto izsekošanu no programmas](#export-trace) minētās darbības, lai saglabātu jaunu veiktspējas izsekošanu lokāli.</span><span class="sxs-lookup"><span data-stu-id="d618e-321">Repeat the steps in the [Export the generated trace from the application](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="d618e-322">Importēt ģenerēto izsekošanu RCS</span><span class="sxs-lookup"><span data-stu-id="d618e-322">Import the generated trace into RCS</span></span>

<span data-ttu-id="d618e-323">Atkārtojiet šīs tēmas iepriekšējā sadaļā [Importēt ģenerēto izsekošanu RCS](#import-trace) minētās darbības, lai importētu jauno veiktspējas izsekošanu pakalpojumā RCS.</span><span class="sxs-lookup"><span data-stu-id="d618e-323">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="d618e-324">Veiktspējas izsekošanas izmantošana analīzes veikšanai pakalpojumā RCS — modeļa kartējums</span><span class="sxs-lookup"><span data-stu-id="d618e-324">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="d618e-325">Atkārtojiet šīs tēmas iepriekšējā sadaļā [Veiktspējas izsekošanas izmantošana analīzes veikšanai pakalpojumā RCS — modeļa kartējums](#use-trace) minētās darbības, lai analizētu jaunāko veiktspējas izsekošanu.</span><span class="sxs-lookup"><span data-stu-id="d618e-325">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="d618e-326">Ņemiet vērā, ka korekcijas, kuras veicāt modeļa kartējumam, likvidēja datu bāzes vaicājumu dublikātus.</span><span class="sxs-lookup"><span data-stu-id="d618e-326">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="d618e-327">Datu bāzu tabulu un datu avotu izsaukumu skaits šim modeļa kartējumam arī ir samazināts.</span><span class="sxs-lookup"><span data-stu-id="d618e-327">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="d618e-328">Tādēļ ir uzlabojusies ER risinājuma kopējā veiktspēja.</span><span class="sxs-lookup"><span data-stu-id="d618e-328">Therefore, the performance of the whole ER solution has improved.</span></span>

![Izsekot informāciju par VendTable datu avotu lapā Modeļa kartējuma noformētājs pakalpojumā RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="d618e-330">Izsekošanas informācijā VendTable datu avota vērtība **\[12\]** norāda, ka šis datu avots tika izsaukts 12 reizes.</span><span class="sxs-lookup"><span data-stu-id="d618e-330">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="d618e-331">Vērtība **\[Q:6\]** norāda, ka seši izsaukumi tika pārveidoti par datu bāzes izsaukumiem uz VendTable tabulu.</span><span class="sxs-lookup"><span data-stu-id="d618e-331">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="d618e-332">Vērtība **\[C:6\]** norāda, ka ieraksti, kas tika ienesti no datu bāzes, tika kešoti, un seši citi izsaukumi tika apstrādāti, izmantojot kešatmiņu.</span><span class="sxs-lookup"><span data-stu-id="d618e-332">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="d618e-333">Ņemiet vērā, ka LedgerTransTypeList datu avota izsaukumu skaits ir samazināts no 9027 līdz 240.</span><span class="sxs-lookup"><span data-stu-id="d618e-333">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![Izsekot informāciju par LedgerTransTypeList datu avotu lapā Modeļa kartējuma noformētājs pakalpojumā RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a><span data-ttu-id="d618e-335">Pārskatiet izpildes izsekošanu lietojumprogrammā</span><span class="sxs-lookup"><span data-stu-id="d618e-335">Review the execution trace in the application</span></span>

<span data-ttu-id="d618e-336">Papildus pakalpojumam RCS dažas versijas var nodrošināt ER struktūras noformētāja iespējas.</span><span class="sxs-lookup"><span data-stu-id="d618e-336">In addition to RCS, some versions might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="d618e-337">Šīm versijām ir opcija **Iespējot noformēšanas režīmu**, ko var ieslēgt.</span><span class="sxs-lookup"><span data-stu-id="d618e-337">These versions have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="d618e-338">Šo opciju var atrast lapas **Elektronisko pārskatu veidošanas parametri** cilnē **Vispārīgi**, kuru varat atvērt, izmantojot darbvietu **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="d618e-338">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![Opcija Iespējot noformēšanas režīmu lapā Elektronisko pārskatu veidošanas parametri](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="d618e-340">Ja izmantojat vienu no šīm versijām, varat analizēt ģenerēto veiktspējas izsekošanu informāciju tieši programmā.</span><span class="sxs-lookup"><span data-stu-id="d618e-340">If you use one of these versions, you can analyze the details of generated performance traces directly in the application.</span></span> <span data-ttu-id="d618e-341">Tās nav jāeksportē no programmas un jāimportē pakalpojumā RCS.</span><span class="sxs-lookup"><span data-stu-id="d618e-341">You don't have to export them from the application and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="d618e-342">Pārskatīt izpildes izsekošanu, izmantojot ārējos rīkus</span><span class="sxs-lookup"><span data-stu-id="d618e-342">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="d618e-343">Lietotāja parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="d618e-343">Configure user parameters</span></span>

1. <span data-ttu-id="d618e-344">Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="d618e-344">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="d618e-345">Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.</span><span class="sxs-lookup"><span data-stu-id="d618e-345">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="d618e-346">Dialoglodziņā **Lietotāja parametri**, sadaļā **Izpildes izsekošana**, laukā **Izpildes izsekošanas formāts** atlasiet **PerfView XML.**</span><span class="sxs-lookup"><span data-stu-id="d618e-346">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="d618e-347">ER formāta palaišana</span><span class="sxs-lookup"><span data-stu-id="d618e-347">Run the ER format</span></span>

<span data-ttu-id="d618e-348">Atkārtojiet šīs tēmas iepriekšējā sadaļā [ER formāta palaišana](#run-format) minētās darbības, lai ģenerētu jaunu veiktspējas izsekošanu.</span><span class="sxs-lookup"><span data-stu-id="d618e-348">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="d618e-349">Ņemiet vērā, ka tīmekļa pārlūkprogramma piedāvā lejupielādēt zip failu.</span><span class="sxs-lookup"><span data-stu-id="d618e-349">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="d618e-350">Šis fails satur veiktspējas izsekošanu PerfView formātā.</span><span class="sxs-lookup"><span data-stu-id="d618e-350">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="d618e-351">Pēc tam varat izmantot PerfView veiktspējas analīzes rīku, lai analizētu ER formāta izpildes informāciju.</span><span class="sxs-lookup"><span data-stu-id="d618e-351">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>

![Veiktspējas izsekošanas informācija PerfView formātā](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a><span data-ttu-id="d618e-353">Ārēju rīku izmantošana, lai pārskatītu izpildes izsekošanu, kas ietver datu bāzes vaicājumus</span><span class="sxs-lookup"><span data-stu-id="d618e-353">Use external tools to review an execution trace that includes database queries</span></span>

<span data-ttu-id="d618e-354">Tā kā ER struktūrā ir veikti uzlabojumi, PerfView formātā ģenerētā veiktspējas izsekošana tagad piedāvā plašāku informāciju par ER formāta izpildi.</span><span class="sxs-lookup"><span data-stu-id="d618e-354">Because of improvements that have been made to the ER framework, the performance trace that is generated in PerfView format now offers more details about ER format execution.</span></span> <span data-ttu-id="d618e-355">Microsoft Dynamics 365 for Finance and Operations versijā 10.0.4 (2019. gada jūlijs) šī izsekošana var ietvert arī informāciju par izpildītajiem SQL vaicājumiem uz programmas datu bāzi.</span><span class="sxs-lookup"><span data-stu-id="d618e-355">In Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019), this trace can also include details of executed SQL queries to the application database.</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="d618e-356">Lietotāja parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="d618e-356">Configure user parameters</span></span>

1. <span data-ttu-id="d618e-357">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="d618e-357">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="d618e-358">Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.</span><span class="sxs-lookup"><span data-stu-id="d618e-358">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="d618e-359">Dialoglodziņa **Lietotāja parametri** sadaļā **Izpildes izsekošana** iestatiet tālāk norādītos parametrus.</span><span class="sxs-lookup"><span data-stu-id="d618e-359">In the **User parameters** dialog box, in the **Execution tracing** section, set the following parameters:</span></span>

    - <span data-ttu-id="d618e-360">Laukā **Izpildes izsekošanas formāts** atlasiet vienumu **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="d618e-360">In the **Execution trace format** field, select **PerfView XML**.</span></span>
    - <span data-ttu-id="d618e-361">Opciju **Vākt vaicājumu statistiku** iestatiet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="d618e-361">Set the **Collect query statistics** option to **Yes**.</span></span>
    - <span data-ttu-id="d618e-362">Opciju **Izsekot vaicājumu** iestatiet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="d618e-362">Set the **Trace query** option to **Yes**.</span></span>

    ![Izpildes izsekošanas sadaļa, lietotāja parametru dialoglodziņš](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a><span data-ttu-id="d618e-364">ER formāta palaišana</span><span class="sxs-lookup"><span data-stu-id="d618e-364">Run the ER format</span></span>

<span data-ttu-id="d618e-365">Atkārtojiet šīs tēmas iepriekšējā sadaļā [ER formāta palaišana](#run-format) minētās darbības, lai ģenerētu jaunu veiktspējas izsekošanu.</span><span class="sxs-lookup"><span data-stu-id="d618e-365">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="d618e-366">Ņemiet vērā, ka tīmekļa pārlūkprogramma piedāvā lejupielādēt zip failu.</span><span class="sxs-lookup"><span data-stu-id="d618e-366">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="d618e-367">Šis fails satur veiktspējas izsekošanu PerfView formātā.</span><span class="sxs-lookup"><span data-stu-id="d618e-367">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="d618e-368">Pēc tam varat izmantot PerfView veiktspējas analīzes rīku, lai analizētu ER formāta izpildes informāciju.</span><span class="sxs-lookup"><span data-stu-id="d618e-368">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span> <span data-ttu-id="d618e-369">Šajā izsekošanā tagad ir informācija par piekļuvi SQL datu bāzei ER formāta izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="d618e-369">This trace now includes the details of SQL database access during the execution of the ER format.</span></span>

![Izpildītā ER formāta informācijas izsekošana rīkā PerfView](./media/GER-PerfTrace2-PerfViewTrace2.PNG)

## <a name="additional-resources"></a><span data-ttu-id="d618e-371">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d618e-371">Additional resources</span></span>

- [<span data-ttu-id="d618e-372">Elektronisko pārskatu veidošanas apskats</span><span class="sxs-lookup"><span data-stu-id="d618e-372">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="d618e-373">Uzlabot ER risinājumu veiktspēju, pievienojot parameterizētus APRĒĶINĀTO LAUKU datu avotus</span><span class="sxs-lookup"><span data-stu-id="d618e-373">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
