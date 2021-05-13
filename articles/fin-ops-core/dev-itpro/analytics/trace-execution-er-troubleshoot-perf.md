---
title: Elektronisko atskaišu veidošanas (ER) formāta failu izpildes uzraudzīšana, lai novērstu veiktspējas problēmas
description: Šajā tēmā ir sniegta informācija par to, kā izmantot veiktspējas izsekošanas līdzekli elektronisko pārskatu veidošanā (ER), lai novērstu veiktspējas problēmas.
author: NickSelin
ms.date: 04/23/2021
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
ms.openlocfilehash: 13e631d3330eefed09111eca70a5aa111e88274f
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944657"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="80cf3-103">ER formātu izpildes izsekošana, lai novērstu veiktspējas problēmas</span><span class="sxs-lookup"><span data-stu-id="80cf3-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="80cf3-104">Elektronisko pārskatu veidošanas (ER) konfigurāciju izstrādes procesa ietvaros, lai izveidotu elektroniskus dokumentus, nosakiet metodi, kas tiek izmantota, lai iegūtu datus no programmas un ievadītu tos ģenerētajā izvadē.</span><span class="sxs-lookup"><span data-stu-id="80cf3-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="80cf3-105">ER veiktspējas izsekošanas līdzeklis palīdz ievērojami samazināt laiku un izmaksas, kas saistītas ar ER formāta izpildes informācijas vākšanu un tās izmantošanu, lai novērstu veiktspējas problēmas.</span><span class="sxs-lookup"><span data-stu-id="80cf3-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="80cf3-106">Šajā apmācībā ir sniegti norādījumi par to, kā informāciju par izpildīto ER formātu veiktspējas izsekošanu var izmantot, lai palīdzētu uzlabot veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="80cf3-106">This tutorial provides guidelines about how to take performance traces for executed ER formats, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="80cf3-107">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="80cf3-107">Prerequisites</span></span>

<span data-ttu-id="80cf3-108">Lai izpildītu šajā apmācībā aprakstītos piemērus, jums ir nepieciešama tālāk norādītā piekļuve.</span><span class="sxs-lookup"><span data-stu-id="80cf3-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="80cf3-109">Piekļuve vienai no sekojošajām lomām:</span><span class="sxs-lookup"><span data-stu-id="80cf3-109">Access to one of the following roles:</span></span>

    - <span data-ttu-id="80cf3-110">Elektroniskā pārskata izstrādātājs</span><span class="sxs-lookup"><span data-stu-id="80cf3-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="80cf3-111">Elektronisko pārskatu veidošanas funkcionālais konsultants</span><span class="sxs-lookup"><span data-stu-id="80cf3-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="80cf3-112">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="80cf3-112">System administrator</span></span>

- <span data-ttu-id="80cf3-113">Piekļuve Regulatory Configuration Services (RCS) instancei, kas ir nodrošināta tam pašam nomniekam, kuram nodrošināta programmas instance, vienai no šādām lomām:</span><span class="sxs-lookup"><span data-stu-id="80cf3-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as the application, for one of the following roles:</span></span>

    - <span data-ttu-id="80cf3-114">Elektroniskā pārskata izstrādātājs</span><span class="sxs-lookup"><span data-stu-id="80cf3-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="80cf3-115">Elektronisko pārskatu veidošanas funkcionālais konsultants</span><span class="sxs-lookup"><span data-stu-id="80cf3-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="80cf3-116">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="80cf3-116">System administrator</span></span>

<span data-ttu-id="80cf3-117">Nepieciešams arī lejupielādēt un lokāli saglabāt tālāk norādītos failus.</span><span class="sxs-lookup"><span data-stu-id="80cf3-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="80cf3-118">Fails</span><span class="sxs-lookup"><span data-stu-id="80cf3-118">File</span></span>                                  | <span data-ttu-id="80cf3-119">Saturs</span><span class="sxs-lookup"><span data-stu-id="80cf3-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="80cf3-120">Veiktspējas izsekošanas modelis.versija.1</span><span class="sxs-lookup"><span data-stu-id="80cf3-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="80cf3-121">Parauga ER datu modeļa konfigurācija</span><span class="sxs-lookup"><span data-stu-id="80cf3-121">Sample ER data model configuration</span></span>](https://download.microsoft.com/download/0/a/a/0aa84e48-8040-4c46-b542-e3bf15c9b2ad/Performancetracemodelversion.1.xml)    |
| <span data-ttu-id="80cf3-122">Veiktspējas izsekošanas metadati.versija.1</span><span class="sxs-lookup"><span data-stu-id="80cf3-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="80cf3-123">Parauga ER metadatu konfigurācija</span><span class="sxs-lookup"><span data-stu-id="80cf3-123">Sample ER metadata configuration</span></span>](https://download.microsoft.com/download/a/9/3/a937e8c4-1f8a-43e4-83ee-7d599cf7d983/Performancetracemetadataversion.1.xml)      |
| <span data-ttu-id="80cf3-124">Veiktspējas izsekošanas kartējums.versija.1.1</span><span class="sxs-lookup"><span data-stu-id="80cf3-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="80cf3-125">Parauga ER modeļa kartējuma konfigurācija</span><span class="sxs-lookup"><span data-stu-id="80cf3-125">Sample ER model mapping configuration</span></span>](https://download.microsoft.com/download/7/7/3/77379bdc-7b22-4cfc-9b64-a9147599f931/Performancetracemappingversion1.1.xml) |
| <span data-ttu-id="80cf3-126">Veiktspējas izsekošanas formāts.versija.1.1</span><span class="sxs-lookup"><span data-stu-id="80cf3-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="80cf3-127">Parauga ER formāta konfigurācija</span><span class="sxs-lookup"><span data-stu-id="80cf3-127">Sample ER format configuration</span></span>](https://download.microsoft.com/download/8/6/8/868ba581-5a06-459e-b173-fb00f038b37f/Performancetraceformatversion1.1.xml)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="80cf3-128">Konfigurēt ER parametrus</span><span class="sxs-lookup"><span data-stu-id="80cf3-128">Configure ER parameters</span></span>

<span data-ttu-id="80cf3-129">Katra ER veiktspējas izsekošana, kas tiek ģenerēta programmā, tiek saglabāta kā izpildes žurnāla ieraksta pielikums.</span><span class="sxs-lookup"><span data-stu-id="80cf3-129">Each ER performance trace that is generated in the application is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="80cf3-130">Šo pielikumu pārvaldībai tiek izmantota dokumentu pārvaldības (Document Management — DM) struktūras.</span><span class="sxs-lookup"><span data-stu-id="80cf3-130">The Document management (DM) framework is used to manage these attachments.</span></span> <span data-ttu-id="80cf3-131">Vispirms ir jākonfigurē ER parametri, lai norādītu DM dokumenta tipu, kas jāizmanto veiktspējas izsekošanas pievienošanai.</span><span class="sxs-lookup"><span data-stu-id="80cf3-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="80cf3-132">Darbvietā **Elektronisko pārskatu veidošana** atlasiet saiti **Elektronisko pārskatu veidošanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-132">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="80cf3-133">Pēc tam lapas **Elektronisko pārskatu veidošanas parametri** cilnes **Pielikumi** laukā **Citi** atlasiet DM dokumenta tipu, kas tiks izmantots veiktspējas izsekošanai.</span><span class="sxs-lookup"><span data-stu-id="80cf3-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Elektronisko pārskatu veidošanas parametru lapa](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="80cf3-135">Lai DM dokumenta tips būtu pieejams uzmeklēšanas laukā **Citi**, tas ir jākonfigurē lapā **Dokumentu tipi** (**Organizācijas administrēšana \> Dokumentu pārvaldība \> Dokumentu tipi**) šādā veidā:</span><span class="sxs-lookup"><span data-stu-id="80cf3-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="80cf3-136">**Klase:** Pievienot failu</span><span class="sxs-lookup"><span data-stu-id="80cf3-136">**Class:** Attach file</span></span>
- <span data-ttu-id="80cf3-137">**Grupa:** Fails</span><span class="sxs-lookup"><span data-stu-id="80cf3-137">**Group:** File</span></span>

![Dokumentu veidu lapa](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="80cf3-139">Atlasītajam dokumenta tipam jābūt pieejamam ikvienā pašreizējās instances uzņēmumā, jo DM pielikumi attiecas tikai uz konkrētu uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="80cf3-139">The selected document type must be available in every company of the current instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="80cf3-140">RCS parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="80cf3-140">Configure RCS parameters</span></span>

<span data-ttu-id="80cf3-141">ER veiktspējas izsekošana, kas tiek ģenerēta, tiks importēta RCS analīzes veikšanai, izmantojot ER formāta noformētāju un ER kartēšanas noformētāju.</span><span class="sxs-lookup"><span data-stu-id="80cf3-141">ER performance traces that are generated will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="80cf3-142">Tā kā ER veiktspējas izsekošana tiek uzglabāta kā izpildes žurnāla ieraksta pielikums, kas ir saistīts ar ER formātu, RCS parametri ir jākonfigurē iepriekš, lai norādītu DM dokumenta tipu, kas jāizmanto veiktspējas izsekošanas pievienošanai.</span><span class="sxs-lookup"><span data-stu-id="80cf3-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="80cf3-143">Tādā RCS instancē, kas nodrošināta jūsu uzņēmumam, darbvietā **Elektronisko pārskatu veidošana** atlasiet **Elektronisko pārskatu veidošanas parametri.**</span><span class="sxs-lookup"><span data-stu-id="80cf3-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="80cf3-144">Pēc tam lapas **Elektronisko pārskatu veidošanas parametri** cilnes **Pielikumi** laukā **Citi** atlasiet DM dokumenta tipu, kas tiks izmantots veiktspējas izsekošanai.</span><span class="sxs-lookup"><span data-stu-id="80cf3-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Lapa Elektronisko pārskatu veidošanas parametri pakalpojumā RCS](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="80cf3-146">Lai DM dokumenta tips būtu pieejams uzmeklēšanas laukā **Citi**, tas ir jākonfigurē lapā **Dokumentu tipi** (**Organizācijas administrēšana \> Dokumentu pārvaldība \> Dokumentu tipi**) šādā veidā:</span><span class="sxs-lookup"><span data-stu-id="80cf3-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="80cf3-147">**Klase:** Pievienot failu</span><span class="sxs-lookup"><span data-stu-id="80cf3-147">**Class:** Attach file</span></span>
- <span data-ttu-id="80cf3-148">**Grupa:** Fails</span><span class="sxs-lookup"><span data-stu-id="80cf3-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="80cf3-149">ER risinājuma izstrāde</span><span class="sxs-lookup"><span data-stu-id="80cf3-149">Design an ER solution</span></span>

<span data-ttu-id="80cf3-150">Pieņemsim, ka esat sācis izstrādāt jaunu ER risinājumu, lai ģenerētu jaunu pārskatu, kurā parādītas kreditoru darbības.</span><span class="sxs-lookup"><span data-stu-id="80cf3-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="80cf3-151">Pašlaik varat atrast atlasītā kreditora transakcijas lapā **Kreditoru transakcijas** (pārejiet uz **Parādi kreditoriem \> Kreditori \> Visi kreditori**, atlasiet kreditoru un pēc tam darbību rūtī, cilnē **Kreditors**, grupā **Transakcijas** atlasiet vienumu **Transakcijas**).</span><span class="sxs-lookup"><span data-stu-id="80cf3-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="80cf3-152">Tomēr ir nepieciešams, lai visas kreditoru transakcijas vienlaicīgi būtu vienā elektroniskajā dokumentā XML formātā.</span><span class="sxs-lookup"><span data-stu-id="80cf3-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="80cf3-153">Šis risinājums sastāv no vairākām ER konfigurācijām, kas ietver nepieciešamo datu modeli, metadatus, modeļa kartējumu un formāta komponentus.</span><span class="sxs-lookup"><span data-stu-id="80cf3-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="80cf3-154">Piesakieties RCS instancē, kas nodrošināta jūsu uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="80cf3-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="80cf3-155">Šajā apmācībā jūs izveidosit un modificēsit nepieciešamās konfigurācijas parauga uzņēmumam **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="80cf3-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="80cf3-156">Tādēļ pārliecinieties, ka šis konfigurācijas nodrošinātājs ir pievienots RCS un atlasīts kā aktīvs.</span><span class="sxs-lookup"><span data-stu-id="80cf3-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="80cf3-157">Norādījumus skatiet procedūrā [Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="80cf3-157">For instructions, see the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>
3. <span data-ttu-id="80cf3-158">Darbvietā **Elektroniskie pārskati** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="80cf3-159">Lapā **Konfigurācijas** importējiet ER konfigurācijas, kuras lejupielādējāt kā priekšnosacījumu pakalpojumā RCS, šādā secībā: datu modelis, metadati, modeļa kartējums, formāts.</span><span class="sxs-lookup"><span data-stu-id="80cf3-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="80cf3-160">Katrai konfigurācijai rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="80cf3-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="80cf3-161">Darbību rūtī atlasiet **Mainīt \> Ielādēt no XML faila**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="80cf3-162">Atlasiet **Pārlūkot**, lai atlasītu atbilstošu failu nepieciešamajai ER konfigurācijai XML formātā.</span><span class="sxs-lookup"><span data-stu-id="80cf3-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="80cf3-163">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-163">Select **OK**.</span></span>

    ![Lapa Konfigurācijas pakalpojumā RCS](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="80cf3-165">Palaidiet ER risinājumu, lai izsekotu izpildi</span><span class="sxs-lookup"><span data-stu-id="80cf3-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="80cf3-166">Pieņemsim, ka esat pabeidzis izstrādāt ER risinājuma pirmo versiju.</span><span class="sxs-lookup"><span data-stu-id="80cf3-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="80cf3-167">Tagad vēlaties to pārbaudīt savā instancē un analizēt izpildes veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="80cf3-167">You now want to test it in your instance and analyze execution performance.</span></span>

### <a name="import-an-er-configuration-from-rcs-into-finance-and-operations"></a><a id='import-configuration'></a><span data-ttu-id="80cf3-168">ER konfigurācijas importēšana no RCS uz Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="80cf3-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="80cf3-169">Piesakieties savā programmas instancē.</span><span class="sxs-lookup"><span data-stu-id="80cf3-169">Sign in to your application instance.</span></span>
2. <span data-ttu-id="80cf3-170">Šīs apmācības ietvaros importēsit konfigurācijas no savas RCS instances (kur izstrādājat ER komponentus) savā instancē (kur tos testējat un izmantojat).</span><span class="sxs-lookup"><span data-stu-id="80cf3-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your instance (where you test and finally use them).</span></span> <span data-ttu-id="80cf3-171">Tāpēc ir jāpārliecinās, ka ir sagatavoti visi vajadzīgie artefakti.</span><span class="sxs-lookup"><span data-stu-id="80cf3-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="80cf3-172">Norādījumus skatiet procedūrā [Importēt elektronisko pārskatu (ER) konfigurācijas no Regulatory Configuration Services (RCS)](rcs-download-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="80cf3-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md) procedure.</span></span>
3. <span data-ttu-id="80cf3-173">Veiciet šādas darbības, lai importētu konfigurācijas no RCS programmā.</span><span class="sxs-lookup"><span data-stu-id="80cf3-173">Follow these steps to import the configurations from RCS into the application:</span></span>

    1. <span data-ttu-id="80cf3-174">Darbvietā **Elektronisko pārskatu veidošana**, **Litware, Inc.** konfigurācijas nodrošinātāja elementā atlasiet **Repozitoriji**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="80cf3-175">Lapā **Konfigurācijas repozitorijs** atlasiet repozitoriju ar tipu **RCS** un pēc tam atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="80cf3-176">Kopsavilkuma cilnē **Konfigurācijas** atlasiet konfigurāciju **Veiktspējas izsekošanas formāts**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="80cf3-177">Kopsavilkuma cilnē **Versijas** atlasiet atlasītās konfigurācijas versiju **1.1** un pēc tam atlasiet **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![Konfigurācijas repozitorijas lapa.](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="80cf3-179">Datu modeļa un modeļa kartējuma konfigurāciju atbilstošās versijas automātiski tiek importētas kā priekšnosacījumi importētajai ER formāta konfigurācijai.</span><span class="sxs-lookup"><span data-stu-id="80cf3-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="80cf3-180">ER veiktspējas izsekošanas ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="80cf3-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="80cf3-181">Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-181">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="80cf3-182">Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="80cf3-183">Dialoglodziņa **Lietotāja parametri** sadaļā **Izpildes izsekošana** rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="80cf3-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="80cf3-184">Laukā **Izpildes izsekošanas formāts** atlasiet vienumu **Atkļūdot izsekošanas formātu**, lai sāktu apkopot informāciju par ER formāta izpildi.</span><span class="sxs-lookup"><span data-stu-id="80cf3-184">In the **Execution trace format** field, select **Debug trace format** to start to collect the details of ER format execution.</span></span> <span data-ttu-id="80cf3-185">Atlasot šo vērtību, veiktspējas izsekošana apkopos informāciju par laiku, kas tiek patērēts šādām darbībām:</span><span class="sxs-lookup"><span data-stu-id="80cf3-185">When this value is selected, the performance trace will collect information about the time that is spent on the following actions:</span></span>

        - <span data-ttu-id="80cf3-186">Katra datu avota palaišana modeļa kartējumā, kas tiek izsaukts datu iegūšanai</span><span class="sxs-lookup"><span data-stu-id="80cf3-186">Running each data source in the model mapping that is called to get data</span></span>
        - <span data-ttu-id="80cf3-187">Katra formāta vienuma apstrāde, lai ievadītu datus ģenerētajā izvadē</span><span class="sxs-lookup"><span data-stu-id="80cf3-187">Processing each format item to enter data in the output that is generated</span></span>

        <span data-ttu-id="80cf3-188">Lauku **Izpildes izsekošanas formāts** izmanto, lai norādītu ģenerētās veiktspējas izsekošanas formātu, kurā tiek uzglabāta izpildes informācijas ER formāta un kartēšanas elementiem.</span><span class="sxs-lookup"><span data-stu-id="80cf3-188">You use the **Execution trace format** field to specify the format of the generated performance trace that the execution details are stored in for ER format and mapping elements.</span></span> <span data-ttu-id="80cf3-189">Atlasot kā vērtību **Atkļūdot izsekošanas formātu**, varēsit analizēt izsekošanas saturu ER operāciju noformētājā un skatīt ER formāta vai kartēšanas elementus, kas minēti izsekošanā.</span><span class="sxs-lookup"><span data-stu-id="80cf3-189">By selecting **Debug trace format** as the value, you will be able to analyze the content of the trace in ER Operation designer, and see the ER format or mapping elements that are mentioned in the trace.</span></span>

    2. <span data-ttu-id="80cf3-190">Iestatiet tālāk minētajām opcijām vienumu **Jā**, lai apkopotu noteiktu informāciju par ER modeļa kartējuma un ER formāta komponentu izpildi:</span><span class="sxs-lookup"><span data-stu-id="80cf3-190">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="80cf3-191">**Apkopot vaicājumu statistiku** — ja šī opcija ir ieslēgta, veiktspējas izsekošanā tiks apkopota šāda informācija:</span><span class="sxs-lookup"><span data-stu-id="80cf3-191">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="80cf3-192">Datu avotu veikto datu bāzes izsaukumu skaits</span><span class="sxs-lookup"><span data-stu-id="80cf3-192">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="80cf3-193">Datu bāzes dublētu izsaukumu skaits</span><span class="sxs-lookup"><span data-stu-id="80cf3-193">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="80cf3-194">Informācija par SQL priekšrakstiem, kas izmantoti datu bāzes izsaukumu veikšanai</span><span class="sxs-lookup"><span data-stu-id="80cf3-194">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="80cf3-195">**Izsekot kešdarbes piekļuvi** — ja šī opcija ir ieslēgta, veiktspējas izsekošanā tiks apkopota informācija par ER modeļa kartējuma kešatmiņas izmantošanu.</span><span class="sxs-lookup"><span data-stu-id="80cf3-195">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="80cf3-196">**Izsekot datu piekļuvi** — ja šī opcija ir ieslēgta, veiktspējas izsekošanā tiks apkopota informācija par datu bāzes izsaukumu skaitu izpildītajiem datu avotiem, kas atbilst tipam “ierakstu saraksts”.</span><span class="sxs-lookup"><span data-stu-id="80cf3-196">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="80cf3-197">**Izsekot saraksta uzskaitījumu** — ja šī opcija ir ieslēgta, veiktspējas izsekošanā tiks apkopota informācija par ierakstu skaitu, kas pieprasīti no datu avotiem, kuri atbilst tipam “ierakstu saraksts”.</span><span class="sxs-lookup"><span data-stu-id="80cf3-197">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="80cf3-198">Parametri dialoglodziņā **Lietotāja parametri** dialoglodziņā ir raksturīgi lietotājam un pašreizējam uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="80cf3-198">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![Lietotāja parametru dialoglodziņš](./media/GER-PerfTrace-GER-UserParameters.png)

### <a name="run-the-er-format"></a><a id='run-format'></a><span data-ttu-id="80cf3-200">ER formāta palaišana</span><span class="sxs-lookup"><span data-stu-id="80cf3-200">Run the ER format</span></span>

1. <span data-ttu-id="80cf3-201">Atlasiet **DEMF** uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="80cf3-201">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="80cf3-202">Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-202">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="80cf3-203">Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Veiktspējas izsekošanas formāts**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-203">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="80cf3-204">Darbību rūtī atlasiet **Palaist**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-204">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="80cf3-205">Ņemiet vērā, ka ģenerētajā failā ir ietverta informācija par 265 transakcijām sešiem kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="80cf3-205">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="80cf3-206">Izpildes izsekošanas pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="80cf3-206">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><a id='export-trace'></a><span data-ttu-id="80cf3-207">Eksportēt ģenerēto izsekošanu no programmas</span><span class="sxs-lookup"><span data-stu-id="80cf3-207">Export the generated trace from the application</span></span>

<span data-ttu-id="80cf3-208">Veiktspējas izsekošana ir atdalīta no avota ER formāta, un to var serializēt ārējā zip failā.</span><span class="sxs-lookup"><span data-stu-id="80cf3-208">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="80cf3-209">Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas atkļūdošanas žurnāli**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-209">Go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="80cf3-210">Lapā **Elektronisko pārskatu palaišanas žurnāli**, kreisajā rūtī, laukā **Konfigurācijas nosaukums** atlasiet **Veiktspējas izsekošanas formāts**, lai atrastu žurnāla ierakstus, kas ģenerēti, izpildot konfigurāciju **Veiktspējas izsekošanas formāts**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-210">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="80cf3-211">Atlasiet pogu **Pielikumi** (papīra saspraudes simbols) lapas augšējā labajā stūrī vai nospiediet **Ctrl+Shift+A**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-211">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![Poga Pielikumi lapā Elektronisko pārskatu palaišanas žurnāli](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="80cf3-213">Lapas **Elektronisko pārskatu palaišanas žurnālu pielikumi** darbību rūtī atlasiet **Atvērt**, lai iegūtu veiktspējas izsekošanu kā zip failu un saglabātu to lokāli.</span><span class="sxs-lookup"><span data-stu-id="80cf3-213">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![Elektronisko pārskatu palaisanas žurnālu pielikumi](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="80cf3-215">Ģenerētajai izsekošanai ir atsauce uz avota ER pārskatu, izmantojot unikālu pārskata identifikatoru tikai **GUID** formātā.</span><span class="sxs-lookup"><span data-stu-id="80cf3-215">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="80cf3-216">Formāta versijas numerācija netiek ņemta vērā.</span><span class="sxs-lookup"><span data-stu-id="80cf3-216">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="80cf3-217">Ņemiet vērā, ka saistība starp veiktspējas izsekošanu, kas ir ģenerēta izpildītajam ER formātam, un ER modeļa kartējumu ir balstīta uz izmantoto saknes deskriptoru un kopējo datu modeli.</span><span class="sxs-lookup"><span data-stu-id="80cf3-217">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="80cf3-218">Formāta un modeļa kartējuma versijas numerācija netiek ņemta vērā.</span><span class="sxs-lookup"><span data-stu-id="80cf3-218">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="80cf3-219">Modeļa kartējuma karodziņa **Modeļa kartējuma noklusējums** iestatījums arī netiek ņemts vērā.</span><span class="sxs-lookup"><span data-stu-id="80cf3-219">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><a id='import-trace'></a><span data-ttu-id="80cf3-220">Importēt ģenerēto izsekošanu RCS</span><span class="sxs-lookup"><span data-stu-id="80cf3-220">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="80cf3-221">Pakalpojuma RCS darbvietā **Elektroniskie pārskati** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-221">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="80cf3-222">Lapā **Konfigurācijas**, konfigurāciju kokā izvērsiet vienumu **Veiktspējas izsekošanas modelis** un atlasiet vienumu **Veiktspējas izsekošanas formāts**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-222">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="80cf3-223">Darbību rūtī atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-223">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="80cf3-224">Lapā **Formāta noformētājs**, darbību rūtī atlasiet **Veiktspējas izsekošana**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-224">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="80cf3-225">Dialoglodziņā **Veiktspējas izsekošanas rezultātu iestatījumi** atlasiet **Importēt veiktspējas izsekošanu**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-225">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="80cf3-226">Lai atlasītu iepriekš eksportētu .axtr failu, atlasiet **Pārlūkot** .</span><span class="sxs-lookup"><span data-stu-id="80cf3-226">Select **Browse** to select the zip file that you exported earlier.</span></span>
7. <span data-ttu-id="80cf3-227">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-227">Select **OK**.</span></span>

    ![Dialoglodziņš Veiktspējas izsekošanas rezultātu iestatījumi pakalpojumā RCS](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="80cf3-229">Veiktspējas izsekošanas izmantošana analīzes veikšanai pakalpojumā RCS — formāta izpilde</span><span class="sxs-lookup"><span data-stu-id="80cf3-229">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="80cf3-230">Pakalpojumā RCS, lapā **Formāta noformētājs** atlasiet **Izvērst/sakļaut**, lai izvērstu visu formāta vienumu saturu.</span><span class="sxs-lookup"><span data-stu-id="80cf3-230">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="80cf3-231">Ņemiet vērā, ka dažiem pašreizējā formāta vienumiem tiek rādīta papildu informācija:</span><span class="sxs-lookup"><span data-stu-id="80cf3-231">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="80cf3-232">Faktiskais laiks, kas patērēts, ievadot datus ģenerētajā izvadē, izmantojot formāta vienumu</span><span class="sxs-lookup"><span data-stu-id="80cf3-232">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="80cf3-233">Tas pats laiks, kas izteikts procentos no kopējā laika, kurš patērēts, ģenerējot visu izvadi</span><span class="sxs-lookup"><span data-stu-id="80cf3-233">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![Formāta noformētāja lapa pakalpojumā RCS](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="80cf3-235">Aizveriet lapu **Formāta noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-235">Close **Format designer** page.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><a id='use-trace'></a><span data-ttu-id="80cf3-236">Veiktspējas izsekošanas izmantošana analīzes veikšanai pakalpojumā RCS — modeļa kartējums</span><span class="sxs-lookup"><span data-stu-id="80cf3-236">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="80cf3-237">Pakalpojuma RCS lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Veiktspējas izsekošanas kartējums**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-237">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="80cf3-238">Darbību rūtī atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-238">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="80cf3-239">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-239">Select **Designer**.</span></span>
4. <span data-ttu-id="80cf3-240">Lapā **Modeļa kartējuma noformētājs**, darbību rūtī atlasiet **Veiktspējas izsekošana**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-240">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="80cf3-241">Atlasiet iepriekš importēto izsekošanu.</span><span class="sxs-lookup"><span data-stu-id="80cf3-241">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="80cf3-242">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-242">Select **OK**.</span></span>

<span data-ttu-id="80cf3-243">Ņemiet vērā, ka kļūst pieejama jauna informācija par dažiem pašreizējā modeļa kartējuma datu avota vienumiem:</span><span class="sxs-lookup"><span data-stu-id="80cf3-243">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="80cf3-244">Faktiskais laiks, kas patērēts, iegūstot datus, izmantojot datu avotu</span><span class="sxs-lookup"><span data-stu-id="80cf3-244">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="80cf3-245">Tas pats laiks, kas izteikts procentos no kopējā laika, kurš patērēts, palaižot visu modeļa kartējumu</span><span class="sxs-lookup"><span data-stu-id="80cf3-245">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="80cf3-246">Ņemiet vērā, ka ER jūs informē par to, ka pašreizējais modeļa kartējums dublē datu bāzes pieprasījumus, kamēr tiek izpildīts VendTable/\<Relations/VendTrans.VendTable\_AccountNum datu avots.</span><span class="sxs-lookup"><span data-stu-id="80cf3-246">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="80cf3-247">Šāda dublēšana notiek tāpēc, ka kreditoru transakciju saraksts tiek izsaukts divas reizes katram atkārtotajam kreditora ierakstam:</span><span class="sxs-lookup"><span data-stu-id="80cf3-247">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="80cf3-248">Viens izsaukums tiek veikts, lai ievadītu informāciju par katru transakciju datu modelī, pamatojoties uz konfigurētajiem saistījumiem.</span><span class="sxs-lookup"><span data-stu-id="80cf3-248">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="80cf3-249">Viens izsaukums tiek veikts, lai ievadītu aprēķināto transakciju skaitu katram kreditoram datu modelī.</span><span class="sxs-lookup"><span data-stu-id="80cf3-249">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![Ziņojums par datu bāzes pieprasījumu dublikātiem lapā Modeļa kartējuma noformētājs pakalpojumā RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="80cf3-251">Vērtība **\[Q:530\]** norāda, ka VendTrans tabula tika izsaukta 530 reizes, lai atgrieztu ierakstu no šīs tabulas uz VendTable/\<Relations/VendTrans.VendTable\_AccountNum datu avotu.</span><span class="sxs-lookup"><span data-stu-id="80cf3-251">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="80cf3-252">Vērtība **\[530\]** norāda, ka VendTable/\<Relations/VendTrans.VendTable\_AccountNum datu avots tika izsaukts 530 reizes, lai atgrieztu ierakstu no šī datu avota un ievadītu tā informāciju datu modelī.</span><span class="sxs-lookup"><span data-stu-id="80cf3-252">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="80cf3-253">Ieteicams izmantot kešdarbi VendTable/\<Relations/VendTrans.VendTable\_AccountNum datu avotam, lai samazinātu izsaukumu skaitu, kas veikti, lai iegūtu informāciju par 265 transakcijām un palīdzētu uzlabot modeļa kartējuma veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="80cf3-253">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="80cf3-254">Tas arī var būt noderīgi, lai samazinātu LedgerTransTypeList datu avotam veikto izsaukumu skaitu.</span><span class="sxs-lookup"><span data-stu-id="80cf3-254">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="80cf3-255">Šis datu avots tiek izmantots, lai katru **LedgerTransType** uzskaitījuma vērtību saistītu ar tā etiķeti.</span><span class="sxs-lookup"><span data-stu-id="80cf3-255">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="80cf3-256">Izmantojot šo datu avotu, varat atrast atbilstošu etiķeti un ievadīt to katras kreditora transakcijas datu modelī.</span><span class="sxs-lookup"><span data-stu-id="80cf3-256">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="80cf3-257">Pašreizējais izsaukumu skaits šim datu avotam (9027) ir diezgan liels 265 transakcijām.</span><span class="sxs-lookup"><span data-stu-id="80cf3-257">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![Lapa Modeļa kartējuma noformētājs pakalpojumā RCS, kurā norādīti 9027 izsaukumi uz datu avotu](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="80cf3-259">Modeļa kartējuma uzlabošana, pamatojoties uz informāciju no izpildes izsekošanas</span><span class="sxs-lookup"><span data-stu-id="80cf3-259">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="80cf3-260">Modeļa kartējuma loģikas modificēšana</span><span class="sxs-lookup"><span data-stu-id="80cf3-260">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="80cf3-261">Veiciet šīs darbības, lai izmantotu kešdarbi, lai palīdzētu novērst dublētus izsaukumus datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="80cf3-261">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="80cf3-262">Pakalpojuma RCS lapā **Modeļa kartējuma noformētājs**, rūtī **Datu avoti** atlasiet vienumu **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-262">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="80cf3-263">Atlasiet **Kešatmiņa**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-263">Select **Cache**.</span></span>
    3. <span data-ttu-id="80cf3-264">Izvērsiet vienumu **VendTable**, izvērsiet “viens pret daudziem” relāciju sarakstu VendTable datu avotam (vienums **\<Relācijas** ) un atlasiet vienumu **VendTrans.VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-264">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="80cf3-265">Atlasiet **Kešatmiņa**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-265">Select **Cache**.</span></span>

    ![Kešdarbes iestatīšana, lai palīdzētu novērst dublētus izsaukumus](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="80cf3-267">Veiciet šīs darbības, lai LedgerTransTypeList datu avotu iekļautu VendTable datu avota tvērumā.</span><span class="sxs-lookup"><span data-stu-id="80cf3-267">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="80cf3-268">Rūtī **Datu avota tipi** izvērsiet vienumu **Funkcijas** un atlasiet vienumu **Aprēķinātais lauks**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-268">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="80cf3-269">Rūtī **Datu avoti** atlasiet vienumu **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-269">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="80cf3-270">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-270">Select **Add**.</span></span>
    4. <span data-ttu-id="80cf3-271">Laukā **Nosaukums** ievadiet **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-271">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="80cf3-272">Atlasiet **Rediģēt formulu**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-272">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="80cf3-273">Laukā **Formula** ievadiet **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-273">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="80cf3-274">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-274">Select **Save**.</span></span>
    8. <span data-ttu-id="80cf3-275">Aizveriet lapu **Formulas redaktors**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-275">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="80cf3-276">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-276">Click **OK**.</span></span>

3. <span data-ttu-id="80cf3-277">Veiciet šīs darbības, lai veiktu lauka **\$TransType** kešdarbi.</span><span class="sxs-lookup"><span data-stu-id="80cf3-277">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="80cf3-278">Atlasiet vienumu **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-278">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="80cf3-279">Atlasiet **Kešatmiņa**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-279">Select **Cache**.</span></span>
    3. <span data-ttu-id="80cf3-280">Atlasiet vienumu **VendTable.\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-280">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="80cf3-281">Atlasiet **Kešatmiņa**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-281">Select **Cache**.</span></span>

    ![Kešdarbes iestatīšana laukam $TransType](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="80cf3-283">Veiciet šīs darbības, lai mainītu lauku **\$TransTypeRecord**, lai tas sāktu izmantot kešoto lauku **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-283">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="80cf3-284">Rūtī **Datu avoti** izvērsiet vienumu **VendTable**, izvērsiet vienumu **\<Relācijas**, izvērsiet vienumu **VendTrans.VendTable\_AccountNum** un atlasiet vienumu **VendTable.VendTrans.VendTable\_AccountNum.\$TransTypeRecord**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-284">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="80cf3-285">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-285">Select **Edit**.</span></span>
    3. <span data-ttu-id="80cf3-286">Atlasiet **Rediģēt formulu**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-286">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="80cf3-287">Laukā **Formula** atrodiet šādu izteiksmi:</span><span class="sxs-lookup"><span data-stu-id="80cf3-287">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="80cf3-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="80cf3-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="80cf3-289">Laukā **Formula** ievadiet šādu izteiksmi:</span><span class="sxs-lookup"><span data-stu-id="80cf3-289">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="80cf3-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span><span class="sxs-lookup"><span data-stu-id="80cf3-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="80cf3-291">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-291">Select **Save**.</span></span>
    7. <span data-ttu-id="80cf3-292">Aizveriet lapu **Formulas redaktors**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-292">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="80cf3-293">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-293">Select **OK**.</span></span>

5. <span data-ttu-id="80cf3-294">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-294">Select **Save**.</span></span>
6. <span data-ttu-id="80cf3-295">Aizveriet lapu **Modeļa kartējuma noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-295">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="80cf3-296">Aizveriet lapu **Modeļa kartējumi**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-296">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="80cf3-297">ER modeļa kartējuma modificētās versijas pabeigšana</span><span class="sxs-lookup"><span data-stu-id="80cf3-297">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="80cf3-298">Pakalpojuma RCS lapā **Konfigurācijas**, kopsavilkuma cilnē **Versijas** atlasiet konfigurācijas **Veiktspējas izsekošanas kartējums** versiju **1.2**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-298">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="80cf3-299">Atlasiet **Mainīt statusu**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-299">Select **Change status**.</span></span>
3. <span data-ttu-id="80cf3-300">Atlasiet **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-300">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a><span data-ttu-id="80cf3-301">Modificētās ER modeļa kartējuma konfigurācijas importēšana no RCS programmā</span><span class="sxs-lookup"><span data-stu-id="80cf3-301">Import the modified ER model mapping configuration from RCS into the application</span></span>

<span data-ttu-id="80cf3-302">Atkārtojiet šīs tēmas iepriekšējā sadaļā [ER konfigurācijas importēšana no pakalpojuma RCS programmā Finance and Operations](#import-configuration) minētās darbības, lai importētu konfigurācijas **Veiktspējas izsekošanas kartējums** versiju 1.2.</span><span class="sxs-lookup"><span data-stu-id="80cf3-302">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="80cf3-303">Modificētā ER risinājuma palaišana, lai izsekotu izpildi</span><span class="sxs-lookup"><span data-stu-id="80cf3-303">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="80cf3-304">ER formāta palaišana</span><span class="sxs-lookup"><span data-stu-id="80cf3-304">Run the ER format</span></span>

<span data-ttu-id="80cf3-305">Atkārtojiet šīs tēmas iepriekšējā sadaļā [ER formāta palaišana](#run-format) minētās darbības, lai ģenerētu jaunu veiktspējas izsekošanu.</span><span class="sxs-lookup"><span data-stu-id="80cf3-305">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="work-with-the-execution-trace"></a><span data-ttu-id="80cf3-306">Darbs ar izpildes izsekošanu</span><span class="sxs-lookup"><span data-stu-id="80cf3-306">Work with the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><span data-ttu-id="80cf3-307">Eksportēt ģenerēto izsekošanu no programmas</span><span class="sxs-lookup"><span data-stu-id="80cf3-307">Export the generated trace from the application</span></span>

<span data-ttu-id="80cf3-308">Atkārtojiet šīs tēmas iepriekšējā sadaļā [Eksportēt ģenerēto izsekošanu no programmas](#export-trace) minētās darbības, lai saglabātu jaunu veiktspējas izsekošanu lokāli.</span><span class="sxs-lookup"><span data-stu-id="80cf3-308">Repeat the steps in the [Export the generated trace from the application](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="80cf3-309">Importēt ģenerēto izsekošanu RCS</span><span class="sxs-lookup"><span data-stu-id="80cf3-309">Import the generated trace into RCS</span></span>

<span data-ttu-id="80cf3-310">Atkārtojiet šīs tēmas iepriekšējā sadaļā [Importēt ģenerēto izsekošanu RCS](#import-trace) minētās darbības, lai importētu jauno veiktspējas izsekošanu pakalpojumā RCS.</span><span class="sxs-lookup"><span data-stu-id="80cf3-310">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="80cf3-311">Veiktspējas izsekošanas izmantošana analīzes veikšanai pakalpojumā RCS — modeļa kartējums</span><span class="sxs-lookup"><span data-stu-id="80cf3-311">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="80cf3-312">Atkārtojiet šīs tēmas iepriekšējā sadaļā [Veiktspējas izsekošanas izmantošana analīzes veikšanai pakalpojumā RCS — modeļa kartējums](#use-trace) minētās darbības, lai analizētu jaunāko veiktspējas izsekošanu.</span><span class="sxs-lookup"><span data-stu-id="80cf3-312">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="80cf3-313">Ņemiet vērā, ka korekcijas, kuras veicāt modeļa kartējumam, likvidēja datu bāzes vaicājumu dublikātus.</span><span class="sxs-lookup"><span data-stu-id="80cf3-313">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="80cf3-314">Datu bāzu tabulu un datu avotu izsaukumu skaits šim modeļa kartējumam arī ir samazināts.</span><span class="sxs-lookup"><span data-stu-id="80cf3-314">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="80cf3-315">Tādēļ ir uzlabojusies ER risinājuma kopējā veiktspēja.</span><span class="sxs-lookup"><span data-stu-id="80cf3-315">Therefore, the performance of the whole ER solution has improved.</span></span>

![Izsekot informāciju par VendTable datu avotu lapā Modeļa kartējuma noformētājs pakalpojumā RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="80cf3-317">Izsekošanas informācijā VendTable datu avota vērtība **\[12\]** norāda, ka šis datu avots tika izsaukts 12 reizes.</span><span class="sxs-lookup"><span data-stu-id="80cf3-317">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="80cf3-318">Vērtība **\[Q:6\]** norāda, ka seši izsaukumi tika pārveidoti par datu bāzes izsaukumiem uz VendTable tabulu.</span><span class="sxs-lookup"><span data-stu-id="80cf3-318">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="80cf3-319">Vērtība **\[C:6\]** norāda, ka ieraksti, kas tika ienesti no datu bāzes, tika kešoti, un seši citi izsaukumi tika apstrādāti, izmantojot kešatmiņu.</span><span class="sxs-lookup"><span data-stu-id="80cf3-319">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="80cf3-320">Ņemiet vērā, ka LedgerTransTypeList datu avota izsaukumu skaits ir samazināts no 9027 līdz 240.</span><span class="sxs-lookup"><span data-stu-id="80cf3-320">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![Izsekot informāciju par LedgerTransTypeList datu avotu lapā Modeļa kartējuma noformētājs pakalpojumā RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a><span data-ttu-id="80cf3-322">Pārskatiet izpildes izsekošanu lietojumprogrammā</span><span class="sxs-lookup"><span data-stu-id="80cf3-322">Review the execution trace in the application</span></span>

<span data-ttu-id="80cf3-323">Papildus pakalpojumam RCS dažas versijas var nodrošināt ER struktūras noformētāja iespējas.</span><span class="sxs-lookup"><span data-stu-id="80cf3-323">In addition to RCS, some versions might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="80cf3-324">Šīm versijām ir opcija **Iespējot noformēšanas režīmu**, ko var ieslēgt.</span><span class="sxs-lookup"><span data-stu-id="80cf3-324">These versions have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="80cf3-325">Šo opciju var atrast lapas **Elektronisko pārskatu veidošanas parametri** cilnē **Vispārīgi**, kuru varat atvērt, izmantojot darbvietu **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-325">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![Opcija Iespējot noformēšanas režīmu lapā Elektronisko pārskatu veidošanas parametri](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="80cf3-327">Ja izmantojat vienu no šīm versijām, varat analizēt ģenerēto veiktspējas izsekošanu informāciju tieši programmā.</span><span class="sxs-lookup"><span data-stu-id="80cf3-327">If you use one of these versions, you can analyze the details of generated performance traces directly in the application.</span></span> <span data-ttu-id="80cf3-328">Tās nav jāeksportē no programmas un jāimportē pakalpojumā RCS.</span><span class="sxs-lookup"><span data-stu-id="80cf3-328">You don't have to export them from the application and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="80cf3-329">Pārskatīt izpildes izsekošanu, izmantojot ārējos rīkus</span><span class="sxs-lookup"><span data-stu-id="80cf3-329">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="80cf3-330">Lietotāja parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="80cf3-330">Configure user parameters</span></span>

1. <span data-ttu-id="80cf3-331">Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-331">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="80cf3-332">Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-332">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="80cf3-333">Dialoglodziņā **Lietotāja parametri**, sadaļā **Izpildes izsekošana**, laukā **Izpildes izsekošanas formāts** atlasiet **PerfView XML.**</span><span class="sxs-lookup"><span data-stu-id="80cf3-333">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="80cf3-334">ER formāta palaišana</span><span class="sxs-lookup"><span data-stu-id="80cf3-334">Run the ER format</span></span>

<span data-ttu-id="80cf3-335">Atkārtojiet šīs tēmas iepriekšējā sadaļā [ER formāta palaišana](#run-format) minētās darbības, lai ģenerētu jaunu veiktspējas izsekošanu.</span><span class="sxs-lookup"><span data-stu-id="80cf3-335">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="80cf3-336">Ņemiet vērā, ka tīmekļa pārlūkprogramma piedāvā lejupielādēt zip failu.</span><span class="sxs-lookup"><span data-stu-id="80cf3-336">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="80cf3-337">Šis fails satur veiktspējas izsekošanu PerfView formātā.</span><span class="sxs-lookup"><span data-stu-id="80cf3-337">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="80cf3-338">Pēc tam varat izmantot PerfView veiktspējas analīzes rīku, lai analizētu ER formāta izpildes informāciju.</span><span class="sxs-lookup"><span data-stu-id="80cf3-338">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>

![Veiktspējas izsekošanas informācija PerfView formātā](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a><span data-ttu-id="80cf3-340">Ārēju rīku izmantošana, lai pārskatītu izpildes izsekošanu, kas ietver datu bāzes vaicājumus</span><span class="sxs-lookup"><span data-stu-id="80cf3-340">Use external tools to review an execution trace that includes database queries</span></span>

<span data-ttu-id="80cf3-341">Tā kā ER struktūrā ir veikti uzlabojumi, PerfView formātā ģenerētā veiktspējas izsekošana tagad piedāvā plašāku informāciju par ER formāta izpildi.</span><span class="sxs-lookup"><span data-stu-id="80cf3-341">Because of improvements that have been made to the ER framework, the performance trace that is generated in PerfView format now offers more details about ER format execution.</span></span> <span data-ttu-id="80cf3-342">Microsoft Dynamics 365 for Finance and Operations versijā 10.0.4 (2019. gada jūlijs) šī izsekošana var ietvert arī informāciju par izpildītajiem SQL vaicājumiem uz programmas datu bāzi.</span><span class="sxs-lookup"><span data-stu-id="80cf3-342">In Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019), this trace can also include details of executed SQL queries to the application database.</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="80cf3-343">Lietotāja parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="80cf3-343">Configure user parameters</span></span>

1. <span data-ttu-id="80cf3-344">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-344">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="80cf3-345">Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-345">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="80cf3-346">Dialoglodziņa **Lietotāja parametri** sadaļā **Izpildes izsekošana** iestatiet tālāk norādītos parametrus.</span><span class="sxs-lookup"><span data-stu-id="80cf3-346">In the **User parameters** dialog box, in the **Execution tracing** section, set the following parameters:</span></span>

    - <span data-ttu-id="80cf3-347">Laukā **Izpildes izsekošanas formāts** atlasiet vienumu **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-347">In the **Execution trace format** field, select **PerfView XML**.</span></span>
    - <span data-ttu-id="80cf3-348">Opciju **Vākt vaicājumu statistiku** iestatiet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-348">Set the **Collect query statistics** option to **Yes**.</span></span>
    - <span data-ttu-id="80cf3-349">Opciju **Izsekot vaicājumu** iestatiet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="80cf3-349">Set the **Trace query** option to **Yes**.</span></span>

    ![Izpildes izsekošanas sadaļa, lietotāja parametru dialoglodziņš](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a><span data-ttu-id="80cf3-351">ER formāta palaišana</span><span class="sxs-lookup"><span data-stu-id="80cf3-351">Run the ER format</span></span>

<span data-ttu-id="80cf3-352">Atkārtojiet šīs tēmas iepriekšējā sadaļā [ER formāta palaišana](#run-format) minētās darbības, lai ģenerētu jaunu veiktspējas izsekošanu.</span><span class="sxs-lookup"><span data-stu-id="80cf3-352">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="80cf3-353">Ņemiet vērā, ka tīmekļa pārlūkprogramma piedāvā lejupielādēt zip failu.</span><span class="sxs-lookup"><span data-stu-id="80cf3-353">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="80cf3-354">Šis fails satur veiktspējas izsekošanu PerfView formātā.</span><span class="sxs-lookup"><span data-stu-id="80cf3-354">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="80cf3-355">Pēc tam varat izmantot PerfView veiktspējas analīzes rīku, lai analizētu ER formāta izpildes informāciju.</span><span class="sxs-lookup"><span data-stu-id="80cf3-355">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span> <span data-ttu-id="80cf3-356">Šajā izsekošanā tagad ir informācija par piekļuvi SQL datu bāzei ER formāta izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="80cf3-356">This trace now includes the details of SQL database access during the execution of the ER format.</span></span>

![Izpildītā ER formāta informācijas izsekošana rīkā PerfView](./media/GER-PerfTrace2-PerfViewTrace2.PNG)

## <a name="additional-resources"></a><span data-ttu-id="80cf3-358">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="80cf3-358">Additional resources</span></span>

- [<span data-ttu-id="80cf3-359">Elektronisko pārskatu veidošanas apskats</span><span class="sxs-lookup"><span data-stu-id="80cf3-359">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="80cf3-360">Uzlabot ER risinājumu veiktspēju, pievienojot parameterizētus APRĒĶINĀTO LAUKU datu avotus</span><span class="sxs-lookup"><span data-stu-id="80cf3-360">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
