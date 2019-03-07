---
title: Retail Modern POS (MPOS) un Cloud POS uzdevumu ierakstītājs un palīdzība
description: Šajā tēmā ir aprakstīts, kā lietot uzdevuma reģistrētāju programmās Retail Modern POS un Cloud POS
author: mugunthanm
manager: AnnBe
ms.date: 06/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTerminalTable, SystemParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a74a1275f08e3dba60a1002a102e143eb37fcd9a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "346000"
---
# <a name="task-recorder-and-help-for-retail-modern-pos-mpos-and-cloud-pos"></a><span data-ttu-id="c4fa4-103">Retail Modern POS (MPOS) un Cloud POS uzdevumu ierakstītājs un palīdzība</span><span class="sxs-lookup"><span data-stu-id="c4fa4-103">Task recorder and Help for Retail Modern POS (MPOS) and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c4fa4-104">Šajā tēmā ir aprakstīts, kā lietot uzdevuma reģistrētāju programmās Retail Modern POS un Cloud POS</span><span class="sxs-lookup"><span data-stu-id="c4fa4-104">This topic describes how to use Task recorder in Retail Modern POS and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="c4fa4-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="c4fa4-105">Overview</span></span>

<span data-ttu-id="c4fa4-106">Programmās Retail Modern POS un Cloud POS ietvertais uzdevuma reģistrētājs ir jauns risinājums, kas ir izstrādāts tā, lai nodrošinātu augstu reaģētspēju.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-106">Task recorder in Retail Modern POS or Cloud POS is a new solution that was built with a focus on high responsiveness.</span></span> <span data-ttu-id="c4fa4-107">Tas nodrošina pielāgojamu lietojumprogrammu programmēšanas saskarni (API), kura nodrošina paplašināšanas iespējas un vienkāršu integrāciju ar biznesa procesu ierakstus izmantojošajām sistēmām.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-107">It provides a flexible application programming interface (API) for extensibility and seamless integration with consumers of business process recordings.</span></span> <span data-ttu-id="c4fa4-108">Turklāt ir progresējusi Uzdevumu ierakstītāja integrācija portāla Microsoft Dynamics Lifecycle Services rīkā Biznesa procesu modelētājs (BPM) ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)).</span><span class="sxs-lookup"><span data-stu-id="c4fa4-108">Additionally, Task recorder integration with the Business process modeler (BPM) tool on Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) has been brought forward.</span></span> <span data-ttu-id="c4fa4-109">Tāpēc lietotāji joprojām var no ierakstiem veidot ar datiem piesātinātas biznesa procesu diagrammas, lai analizētu un izstrādātu lietojumprogrammas.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-109">Therefore, users can continue to produce rich business process diagrams from recordings to analyze and design their applications.</span></span>

## <a name="architecture"></a><span data-ttu-id="c4fa4-110">Arhitektūra</span><span class="sxs-lookup"><span data-stu-id="c4fa4-110">Architecture</span></span>

<span data-ttu-id="c4fa4-111">Uzdevuma reģistrētājs var nodrošināt klientā veikto lietotāja darbību precīzu reģistrāciju.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-111">Task recorder can record user actions in the client with exact fidelity.</span></span> <span data-ttu-id="c4fa4-112">Katra vadīkla ir konfigurēta tām, lai uz uzdevuma reģistrētāju tiktu sūtīta informācija par lietotāja darbību izpildi.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-112">Each control is instrumented to notify Task recorder about the execution of a user action.</span></span> <span data-ttu-id="c4fa4-113">No vadīklas uz uzdevuma reģistrētāju tiek reāllaikā nosūtīta informācija par notikuma norisi, kā arī visa vajadzīgā informācija par attiecīgo lietotāja darbību.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-113">The control notifies Task recorder that an event occurred and passes along all pertinent information about the corresponding user action in real time.</span></span> <span data-ttu-id="c4fa4-114">No šīs informācijas uzdevuma reģistrētajā tiek izgūts lietotāja darbības veids (piemēram, pogas klikšķis, vērtības ievade vai navigācija) un visi ar lietotāja darbību saistītie dati (piemēram, ievadīto datu vērtība un veids, veidlapas konteksts vai ieraksta konteksts).</span><span class="sxs-lookup"><span data-stu-id="c4fa4-114">From this information, Task recorder can capture the type of user action (such as a button click, value entry, or navigation) and any data that is related to the user action (such as the input data value and type, form context, or record context).</span></span> <span data-ttu-id="c4fa4-115">Uzdevuma reģistrētājā informācija tiek reģistrēta pietiekami detalizēti, lai nodrošinātu, ka ieraksta demonstrēšanas laikā reģistrētās darbības var veikt tieši tā, kā to darīja lietotājs.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-115">Task recorder persists the information with enough detail to help guarantee that a playback of the recording can perform the recorded actions exactly as the user performed them.</span></span> <span data-ttu-id="c4fa4-116">(Demonstrēšanas līdzeklis vēl nav ieviests programmās Retail Modern POS un Cloud POS.)</span><span class="sxs-lookup"><span data-stu-id="c4fa4-116">(The playback feature isn't yet implemented at Retail modern POS or Cloud POS.)</span></span>

## <a name="basic-configuration"></a><span data-ttu-id="c4fa4-117">Pamata konfigurācija</span><span class="sxs-lookup"><span data-stu-id="c4fa4-117">Basic configuration</span></span>

<span data-ttu-id="c4fa4-118">Lai POS iespējotu uzdevuma reģistrēšanu, veiciet tālāk norādītas darbības.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-118">To enable task recording in POS, follow these steps.</span></span>

1. <span data-ttu-id="c4fa4-119">Noklikšķiniet uz **Mazumtirdzniecība** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **Reģistri**.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-119">Click **Retail** &gt; **Channel Setup** &gt; **POS Setup** &gt; **Registers**.</span></span>
2. <span data-ttu-id="c4fa4-120">Noklikšķiniet uz kases sistēmas, kurā vēlaties iespējot uzdevuma reģistrēšanu.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-120">Click the register to enable task recording on.</span></span>
3. <span data-ttu-id="c4fa4-121">Cilnes **Reģistrs** kopsavilkuma cilnē **Vispārīgi** iestatiet opcijas **Iespējot uzdevumu ierakstīšanu** vērtību **Jā**.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-121">On the **Register** tab, on the **General** FastTab, set the **Enable task recording** option to **Yes**.</span></span>
4. <span data-ttu-id="c4fa4-122">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-122">Click **Save**.</span></span>
5. <span data-ttu-id="c4fa4-123">Dodieties uz **Mazumtirdzniecība** &gt; **Mazumtirdzniecības IT** &gt; **Sadales grafiks**.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-123">Go to **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
6. <span data-ttu-id="c4fa4-124">Atlasiet uzdevumu **Reģistri (1090)** un pēc tam noklikšķiniet uz **Izpildīt tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-124">Select the **Registers (1090)** job, and then click **Run now**.</span></span>

## <a name="create-a-recording"></a><span data-ttu-id="c4fa4-125">Ieraksta izveide</span><span class="sxs-lookup"><span data-stu-id="c4fa4-125">Create a recording</span></span>

<span data-ttu-id="c4fa4-126">Lai izveidotu jaunu ierakstu, izmantojot uzdevuma reģistrētāju, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-126">Follow these steps to create a new recording using Task recorder.</span></span>

1. <span data-ttu-id="c4fa4-127">Palaidiet programmu Retail Modern POS vai Cloud POS un pierakstieties.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-127">Start Retail Modern POS or Cloud POS, and sign in.</span></span>
2. <span data-ttu-id="c4fa4-128">Lapas **Iestatījumi** sadaļā **Uzdevuma reģistrētājs** noklikšķiniet uz **Atvērt uzdevuma reģistrētāju**.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-128">On the **Settings** page, in the **Task Recorder** section, click **Open task recorder**.</span></span> <span data-ttu-id="c4fa4-129">Tiek parādīta rūts **Uzdevuma reģistrētājs**.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-129">The **Task recorder** pane appears.</span></span> <span data-ttu-id="c4fa4-130">Varat noklikšķināt uz pogas **Aizvērt** (**X**) augšējā labajā stūrī, lai aizvērtu rūti **Uzdevuma reģistrētājs** pirms jaunas reģistrēšanas sesijas sākšanas.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-130">You can click the **Close** button (**X**) in the upper-right corner to close the **Task recorder** pane before you begin a new recording.</span></span> <span data-ttu-id="c4fa4-131">Lai atkārtoti atvērtu rūti, atkārtojiet 2. darbību.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-131">To reopen the pane, repeat step 2.</span></span>

    <span data-ttu-id="c4fa4-132">[![Rūts Uzdevuma reģistrētājs](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span><span class="sxs-lookup"><span data-stu-id="c4fa4-132">[![Task recorder pane](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span></span>

3. <span data-ttu-id="c4fa4-133">Ievadiet ieraksta nosaukumu un aprakstu un pēc tam noklikšķiniet uz **Sākt**.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-133">Enter a name and description for the recording, and then click **Start**.</span></span> <span data-ttu-id="c4fa4-134">Reģistrēšanas sesija sākas, tiklīdz noklikšķināt uz **Sākt**.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-134">The recording session begins as soon as you click **Start**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c4fa4-135">Ja ierakstīšanas laikā noklikšķināt uz pogas **Aizvērt** (**X**) augšējā labajā stūrī, tiek aizvērta rūts **Uzdevuma reģistrētājs**, taču reģistrēšanas sesija netiek beigta.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-135">If you click the **Close** button (**X**) in the upper-right corner while recording is in progress, the **Task recorder** pane is closed, but the recording session isn't ended.</span></span> <span data-ttu-id="c4fa4-136">Lai atkāroti atvērtu uzdevuma reģistrētāju, noklikšķiniet uz pogas **Palīdzība** (jautājuma zīmes ikonas) ekrāna augšpusē.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-136">To reopen the Task recorder pane, click the **Help** button (question mark) at the top of the screen.</span></span>
    >
    > <span data-ttu-id="c4fa4-137">[![Jautājuma zīme](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="c4fa4-137">[![Question mark](./media/help.jpg)](./media/help.jpg)</span></span>

4. <span data-ttu-id="c4fa4-138">Pēc noklikšķināšanas uz **Sākt** uzdevuma reģistrētājs tiek pārslēgts reģistrēšanas režīmā.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-138">After you click **Start**, Task recorder enters recording mode.</span></span> <span data-ttu-id="c4fa4-139">Rūtī **Uzdevuma reģistrētājs** tiek rādīta ar reģistrēšanas procesu saistītā informācija un vadīklas.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-139">The **Task recorder** pane shows information and controls that are related to the recording process.</span></span>
5. <span data-ttu-id="c4fa4-140">Veiciet vajadzīgās darbības programmas Retail Modern POS vai Cloud POS lietotāja interfeisā (UI).</span><span class="sxs-lookup"><span data-stu-id="c4fa4-140">Perform the actions that you want to perform in the Retail Modern POS or Cloud POS user interface (UI).</span></span>
6. <span data-ttu-id="c4fa4-141">Lai beigtu reģistrēšanas sesiju, noklikšķiniet uz **Apturēt**.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-141">To end the recording session, click **Stop**.</span></span>

## <a name="download-options"></a><span data-ttu-id="c4fa4-142">Lejupielādes opcijas</span><span class="sxs-lookup"><span data-stu-id="c4fa4-142">Download options</span></span>

<span data-ttu-id="c4fa4-143">Kad beidzat reģistrēšanas sesiju, tiek parādītas vairākas ierakstu lejupielādes opcijas.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-143">After you end the recording session, several options are shown, so that you can download your recording.</span></span>

<span data-ttu-id="c4fa4-144">[![Lejupielādes opcijas](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span><span class="sxs-lookup"><span data-stu-id="c4fa4-144">[![Download options](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span></span>

### <a name="save-to-this-pc"></a><span data-ttu-id="c4fa4-145">Saglabāt šajā datorā</span><span class="sxs-lookup"><span data-stu-id="c4fa4-145">Save to this PC</span></span>

<span data-ttu-id="c4fa4-146">Varat izmantot ieraksta pakotni, lai demonstrētu uzdevuma ceļvedi, uzturētu ierakstu vai rediģētu ierakstā esošās anotācijas.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-146">You can use the recording package to play a Task guide, maintain the recording, or edit the annotations in the recording.</span></span> <span data-ttu-id="c4fa4-147">(Šis līdzeklis vēl nav ieviests programmās Retail Modern POS un Cloud POS.)</span><span class="sxs-lookup"><span data-stu-id="c4fa4-147">(This feature isn't yet implemented in Retail Modern POS and Cloud POS.)</span></span>

### <a name="export-as-word-document"></a><span data-ttu-id="c4fa4-148">Eksportēt kā Word dokumentu</span><span class="sxs-lookup"><span data-stu-id="c4fa4-148">Export as Word document</span></span>

<span data-ttu-id="c4fa4-149">Varat saglabāt ierakstu Microsoft Word dokumenta formātā.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-149">You can save the recording as a Microsoft Word document.</span></span> <span data-ttu-id="c4fa4-150">Dokumentā ir ietvertas reģistrētās darbības un iegūtie ekrānuzņēmumi.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-150">The document will contain the recorded steps and the screenshots that were captured.</span></span>

### <a name="save-as-developer-recording"></a><span data-ttu-id="c4fa4-151">Saglabāt kā izstrādātāja ierakstu</span><span class="sxs-lookup"><span data-stu-id="c4fa4-151">Save as developer recording</span></span>

<span data-ttu-id="c4fa4-152">Neapstrādātais ieraksta fails ir noderīgs izstrādātājiem, piemēram, testa koda ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-152">The raw recording file will be useful for developer scenarios such as test code generation.</span></span> <span data-ttu-id="c4fa4-153">(Šis līdzeklis vēl nav ieviests.)</span><span class="sxs-lookup"><span data-stu-id="c4fa4-153">(This feature isn't yet implemented.)</span></span>

## <a name="recording-controls"></a><span data-ttu-id="c4fa4-154">Ierakstīšanas vadīklas</span><span class="sxs-lookup"><span data-stu-id="c4fa4-154">Recording controls</span></span>

<span data-ttu-id="c4fa4-155">[![Reģistrēšanas vadīklas](./media/controls.jpg)](./media/controls.jpg)</span><span class="sxs-lookup"><span data-stu-id="c4fa4-155">[![Recording controls](./media/controls.jpg)](./media/controls.jpg)</span></span>

### <a name="stop"></a><span data-ttu-id="c4fa4-156">Apturēt</span><span class="sxs-lookup"><span data-stu-id="c4fa4-156">Stop</span></span>

<span data-ttu-id="c4fa4-157">Noklikšķiniet uz **Apturēt**, lai beigtu reģistrēšanas sesiju.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-157">Click **Stop** to end the recording session.</span></span> <span data-ttu-id="c4fa4-158">Ņemiet vērā, ka pēc sesijas beigšanas to vairs nevar atsākt.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-158">Note that you can't restart a session after you end it.</span></span> <span data-ttu-id="c4fa4-159">Tāpēc pirms reģistrēšanas sesijas beigšanas pārliecinieties, ka reģistrēšana ir pabeigta.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-159">Therefore, make sure that the recording is completed before you end it.</span></span>

### <a name="pause"></a><span data-ttu-id="c4fa4-160">Pauze</span><span class="sxs-lookup"><span data-stu-id="c4fa4-160">Pause</span></span>

<span data-ttu-id="c4fa4-161">Noklikšķiniet uz **Pauze**, lai īslaicīgi apturētu (pārtrauktu) reģistrēšanas sesiju un turpinātu darbību.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-161">Click **Pause** to temporarily stop (pause) the recording session and continue with the operation.</span></span> <span data-ttu-id="c4fa4-162">Darbības, ko veicat pēc noklikšķināšanas uz **Pauze**, netiek reģistrētas.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-162">Steps that you perform after you click **Pause** aren't recorded.</span></span>

### <a name="continue"></a><span data-ttu-id="c4fa4-163">Turpināt</span><span class="sxs-lookup"><span data-stu-id="c4fa4-163">Continue</span></span>

<span data-ttu-id="c4fa4-164">Lai atsāktu reģistrēšanas sesiju pēc tās pārtraukšanas noklikšķiniet uz **Turpināt**.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-164">To resume the recording session after you've paused it, click **Continue**.</span></span>

### <a name="capture-screenshots"></a><span data-ttu-id="c4fa4-165">Veikt ekrānuzņēmumus</span><span class="sxs-lookup"><span data-stu-id="c4fa4-165">Capture screenshots</span></span>

<span data-ttu-id="c4fa4-166">Uzdevuma reģistrētājs var nodrošināt Retail Modern POS lietotāja interfeisa ekrānuzņēmumu veikšanu biznesa procesa reģistrēšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-166">Task recorder can capture screenshots of the Retail Modern POS UI as you record a business process.</span></span> <span data-ttu-id="c4fa4-167">Lai ieslēgtu ekrānuzņēmumu veikšanas līdzekli, opcijai **Veikt ekrānuzņēmumu** iestatiet vērtību **Jā** un pēc tam uzņemiet ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-167">To turn on the screenshot capture feature, set the **Capture screenshot** option to **Yes** and then make the recording.</span></span> <span data-ttu-id="c4fa4-168">Kad ierakstīšana ir pabeigta, noklikšķiniet uz **Apturēt** un lejupielādējiet Word dokumentu.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-168">Once the recording is completed, click **Stop** and download the Word document.</span></span> <span data-ttu-id="c4fa4-169">Dokumentā būs ietvertas darbības ar attiecīgajiem ekrānuzņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-169">The document will contain the steps with relevant screenshots.</span></span>

> [!NOTE]
> <span data-ttu-id="c4fa4-170">Funkcija Veikt ekrānuzņēmumu netiek atbalstīta programmā Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-170">Capture screenshot functionality is not supported in Cloud POS.</span></span>

### <a name="start-task-and-end-task"></a><span data-ttu-id="c4fa4-171">Uzdevuma sākšana un beigšana</span><span class="sxs-lookup"><span data-stu-id="c4fa4-171">Start task and End task</span></span>

<span data-ttu-id="c4fa4-172">Varat norādīt grupētu darbību kopas sākumu un beigas, izmantojot pogas **Sākt uzdevumu** un **Beigt** **uzdevumu**.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-172">You can specify the beginning and end of a set of grouped steps by using the **Start task** and **End** **task** buttons.</span></span> <span data-ttu-id="c4fa4-173">Noklikšķiniet uz **Sākt uzdevumu**, lai pievienotu darbību "Sākt uzdevumu", un pēc tam veiciet darbības, kas ir jāietver grupā.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-173">Click **Start task** to add a "Start Task" step, and then perform the steps that should be included in the group.</span></span> <span data-ttu-id="c4fa4-174">Kad esat pabeidzis grupā ietveramo darbību izpildi, noklikšķiniet uz **Beigt uzdevumu**.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-174">After you've finished performing the steps for the group, click **End task**.</span></span> <span data-ttu-id="c4fa4-175">Uzdevumi palīdz strukturēt procedūras.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-175">Tasks help you organize your procedures.</span></span> <span data-ttu-id="c4fa4-176">Uzdevumus var ligzdot citos uzdevumos.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-176">Tasks can be nested within other tasks.</span></span> <span data-ttu-id="c4fa4-177">Šādā veidā varat labāk strukturēt ļoti garus un sarežģītu biznesa procesus.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-177">In this way, you can better organize very long and complex business processes.</span></span>

## <a name="adding-annotations"></a><span data-ttu-id="c4fa4-178">Anotāciju pievienošana</span><span class="sxs-lookup"><span data-stu-id="c4fa4-178">Adding annotations</span></span>

<span data-ttu-id="c4fa4-179">Piezīme ir papildu teksts, ko pievienojat ieraksta darbībai.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-179">An annotation is additional text that you add to a step in a recording.</span></span> <span data-ttu-id="c4fa4-180">Piemēram, varat izmantot piezīmes, lai sniegtu lietotājam papildu informāciju vai kontekstu.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-180">For example, you can use annotations to give the user more context or instructions.</span></span> <span data-ttu-id="c4fa4-181">Anotācijas var pievienot pirms vai pēc darbības.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-181">You can add annotations before or after a step.</span></span> <span data-ttu-id="c4fa4-182">Varat pievienot anotāciju jebkurai darbībai, noklikšķinot uz pogas **Rediģēt** (zīmuļa simbola) pa labi no darbības.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-182">You can add an annotation to any step by clicking the **Edit** button (pencil symbol) to the right of the step.</span></span>

<span data-ttu-id="c4fa4-183">[![Darbības rediģēšanas poga](./media/annotate.jpg)](./media/annotate.jpg)</span><span class="sxs-lookup"><span data-stu-id="c4fa4-183">[![Edit button for a step](./media/annotate.jpg)](./media/annotate.jpg)</span></span>

### <a name="texts-and-notes"></a><span data-ttu-id="c4fa4-184">Teksts un piezīmes</span><span class="sxs-lookup"><span data-stu-id="c4fa4-184">Texts and notes</span></span>

<span data-ttu-id="c4fa4-185">Varat izmantot laukus **Teksts** un **Piezīmes**, lai pievienotu tekstu, kas ir jāsaista ar darbību uzdevuma reģistrētājā.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-185">You can use the **Texts** and **Notes** fields to add text that should be associated with a step in a Task guide.</span></span>

<span data-ttu-id="c4fa4-186">[![Lauki Teksts un Piezīmes](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span><span class="sxs-lookup"><span data-stu-id="c4fa4-186">[![Text and Notes fields](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span></span>

#### <a name="text"></a><span data-ttu-id="c4fa4-187">Teksts</span><span class="sxs-lookup"><span data-stu-id="c4fa4-187">Text</span></span>

<span data-ttu-id="c4fa4-188">Laukā **Teksts** ievadītais teksts tiek rādīts *virs* darbības teksta uzdevuma reģistrētājā.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-188">Text that you enter in the **Text** field appears *above* the step text in the Task guide.</span></span> <span data-ttu-id="c4fa4-189">Šī atrašanās vieta ir piemērota tekstam, kas lietotājam ir jāizlasa pirms darbības veikšanas.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-189">This location is appropriate for text that you want the user to read before he or she completes the step.</span></span>

#### <a name="notes"></a><span data-ttu-id="c4fa4-190">Piezīmes</span><span class="sxs-lookup"><span data-stu-id="c4fa4-190">Notes</span></span>

<span data-ttu-id="c4fa4-191">Laukā **Piezīmes** ievadītais teksts tiek rādīts *zem* darbības teksta uzdevuma reģistrētājā.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-191">Text that you enter in the **Notes** field appears *below* the step text in the Task guide.</span></span> <span data-ttu-id="c4fa4-192">Lai izlasītu piezīmes tekstu, lietotājam ir jāizvērš darbības teksts uznirstošajā logā.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-192">To read the note text, the user must expand the step text in the pop-up window.</span></span> <span data-ttu-id="c4fa4-193">Šī atrašanās vieta ir piemērota papildinformācijai vai citai informācijai, kas lietotājam var noderēt lietotājam, taču nav nepieciešama, lai veiktu darbību.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-193">This location is appropriate for optional reading material or other information that might be useful to the user, but that the user doesn't require in order to complete the action.</span></span>

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a><span data-ttu-id="c4fa4-194">Palīdzība programmās Retail Modern POS un Cloud POS</span><span class="sxs-lookup"><span data-stu-id="c4fa4-194">Help in Retail Modern POS and Cloud POS</span></span>

<span data-ttu-id="c4fa4-195">Lai jūsu pielāgotie uzdevumu ieraksti tiktu rādīti programmu Retail Modern POS un Cloud POS rūtī Palīdzība teksta formātā, jums ir jāsaglabā ieraksti savā BPM bibliotēkā un pēc tam ir jāatjaunina palīdzības sistēmas parametri tā, lai tie norādītu uz jūsu BPM bibliotēku.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-195">To show your own custom task recordings in the Help pane of Retail Modern POS and Cloud POS so that they can be viewed as text, you must save your task recordings to your own BPM library, and then update your Help system parameters to point to your BPM library.</span></span> <span data-ttu-id="c4fa4-196">Plašāku informāciju skatiet rakstā [Savienojuma izveidošana ar palīdzības sistēmu](../fin-and-ops/get-started/help-connect.md).</span><span class="sxs-lookup"><span data-stu-id="c4fa4-196">For more information, see [Connecting the Help system](../fin-and-ops/get-started/help-connect.md).</span></span> <span data-ttu-id="c4fa4-197">Retail Modern POS un Cloud POS palīdzības sistēma nodrošina reāllaika meklēšanu pakalpojumā LCS.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-197">Retail Modern POS and Cloud POS Help searches LCS in real time.</span></span> <span data-ttu-id="c4fa4-198">Sistēma nodrošina meklēšanu visās BPM bibliotēkās, kas ir atlasītas Microsoft Dynamics 365 for Retail palīdzības sistēmas parametros, un atbilstošo rezultātu parādīšanu.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-198">It searches across all the BPM libraries that are selected in the Microsoft Dynamics 365 for Retail Help system parameters and shows the relevant results.</span></span> <span data-ttu-id="c4fa4-199">Lai piekļūtu izvēlnei **Palīdzība**, noklikšķiniet uz pogas **Palīdzīga** (jautājuma zīme) ekrāna augšdaļā, meklēšanas lodziņā ievadiet procesa nosaukumu un nospiediet meklēšanas pogu.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-199">To access the **Help** menu, click the **Help** button (question mark) at the top of the screen and then in the search box type your process name and hit the search button.</span></span>

<span data-ttu-id="c4fa4-200">[![Poga Palīdzība](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="c4fa4-200">[![Help button](./media/help.jpg)](./media/help.jpg)</span></span>

<span data-ttu-id="c4fa4-201">Kad meklēšanas rezultātu sarakstā noklikšķināt uz uzdevuma ceļveža, varat skatīt darbības palīdzības tēmas formātā vai eksportēt darbības Word dokumenta formātā.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-201">When you click a Task guide in the search results, you can either view the steps as a Help topic or export the steps to a Word document.</span></span>

> [!NOTE]
> <span data-ttu-id="c4fa4-202">Palīdzība programmās Retail Modern POS un Cloud POS nevar parādīt uzdevumu ceļvežus, ņemot vērā, kuru veidlapu pašlaik atvērāt vai kuru darbību izpildāt.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-202">Help in Retail Modern POS and Cloud POS will not bring up task guides according to what form you're on or operation you're doing.</span></span> <span data-ttu-id="c4fa4-203">Meklēšanas lodziņā ierakstiet procesa nosaukumu un pēc tam noklikšķiniet uz **Meklēt**.</span><span class="sxs-lookup"><span data-stu-id="c4fa4-203">You have to type the process name in the search box and then click **Search**.</span></span>
