---
title: Regression Suite Automation Tool lietošanas apmācība
description: Šajā tēmā ir parādīts, kā izmantot Regression Suite Automation Tool (RSAT). Tajā ir aprakstīti dažādi līdzekļi un sniegti piemēri, kuros izmantota papildu skriptēšana.
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: cf3ca501efb4e540994b01e651eee5b8aab4ddbc
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191090"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="167cb-104">Regression Suite Automation Tool lietošanas apmācība</span><span class="sxs-lookup"><span data-stu-id="167cb-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="167cb-105">Izmantojiet interneta pārlūka rīkus, lai lejupielādētu un saglabātu šo lapu PDF formātā.</span><span class="sxs-lookup"><span data-stu-id="167cb-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="167cb-106">Šajā apmācībā ir aprakstīti daži Regression Suite Automation Tool (RSAT) papildu līdzekļi, ietverta demonstrācijas piešķire un aprakstīta stratēģija un galvenās mācību tēmas.</span><span class="sxs-lookup"><span data-stu-id="167cb-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="features-of-rsattask-recorder"></a><span data-ttu-id="167cb-107">RSAT/uzdevumu reģistrētāja līdzekļi</span><span class="sxs-lookup"><span data-stu-id="167cb-107">Features of RSAT/Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="167cb-108">Lauka vērtības validēšana</span><span class="sxs-lookup"><span data-stu-id="167cb-108">Validate a field value</span></span>

<span data-ttu-id="167cb-109">Informāciju par šo līdzekli skatiet tēmā [Jauna uzdevuma ieraksta izveide ar validēšanas funkciju](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span><span class="sxs-lookup"><span data-stu-id="167cb-109">For information about this feature, see the [Create a new task recording that has a Validate function](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span></span>

### <a name="saved-variable"></a><span data-ttu-id="167cb-110">Saglabāts mainīgais</span><span class="sxs-lookup"><span data-stu-id="167cb-110">Saved variable</span></span>

<span data-ttu-id="167cb-111">Informāciju par šo līdzekli skatiet tēmā [Esoša uzdevuma ieraksta modificēšana, lai izveidotu saglabātu mainīgo](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span><span class="sxs-lookup"><span data-stu-id="167cb-111">For information about this feature, see the [Modify an existing task recording to create a saved variable](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="167cb-112">Atvasināts testa gadījums</span><span class="sxs-lookup"><span data-stu-id="167cb-112">Derived test case</span></span>

1. <span data-ttu-id="167cb-113">Atveriet Regression Suite Automation Tool (RSAT) un atlasiet abus testa gadījumus, ko izveidojāt, izpildot tēmā [Regression Suite Automation Tool iestatīšana un instalēšana](./hol-set-up-regression-suite-automation-tool.md) norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="167cb-113">Open Regression suite automation tool (RSAT), and select both the test cases that you created in [Set up and install Regression suite automation tool](./hol-set-up-regression-suite-automation-tool.md).</span></span>
2. <span data-ttu-id="167cb-114">Atlasiet **Jauns \> Izveidot atvasināto testa gadījumu**.</span><span class="sxs-lookup"><span data-stu-id="167cb-114">Select **New \> Create derived test case**.</span></span>

    ![Jauna atvasinātā testa gadījuma komandas izveide izvēlnē Jauns](./media/use_rsa_tool_01.png)

3. <span data-ttu-id="167cb-116">Tiek parādīts ziņojums, ka atvasinātais testa gadījums tiks izveidots katram pašreizējā testu kopā atlasītajam testa gadījumam un ka katram atvasinātajam testa gadījumam tiks izveidota sava Excel parametru faila kopija.</span><span class="sxs-lookup"><span data-stu-id="167cb-116">You receive a message that states that a derived test case will be created for each selected test case in the current test suite, and that each derived test case will have its own copy of the Excel parameter file.</span></span> <span data-ttu-id="167cb-117">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="167cb-117">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="167cb-118">Palaižot atvasināto testa gadījumu, tiek izmantots tā pamata testa gadījuma uzdevuma ieraksts un atvasinātā testa gadījuma Excel parametru faila kopija.</span><span class="sxs-lookup"><span data-stu-id="167cb-118">When you run a derived test case, it uses the task recording of its parent test case and its own copy of the Excel parameter file.</span></span> <span data-ttu-id="167cb-119">Šādā veidā varat palaist vienu un to pašu testu ar dažādiem parametriem bez nepieciešamības uzturēt vairāk par vienu uzdevuma ierakstu.</span><span class="sxs-lookup"><span data-stu-id="167cb-119">In this way, you can run the same test with different parameters, without having to maintain more than one task recording.</span></span> <span data-ttu-id="167cb-120">Atvasinātajam testa gadījumam nav jāietilpst tajā pašā testu kopā, kurā ietilpst tā pamata testa gadījums.</span><span class="sxs-lookup"><span data-stu-id="167cb-120">A derived test case doesn't have to be part of the same test suite as its parent test case.</span></span>

    ![Ziņojuma lodziņš](./media/use_rsa_tool_02.png)

    <span data-ttu-id="167cb-122">Tiek izveidoti divi papildu atvasinātie testa gadījumi, un tiek atlasīta šo atvasināto testa gadījumu izvēles rūtiņa **Atvasināts?**.</span><span class="sxs-lookup"><span data-stu-id="167cb-122">Two additional derived test cases are created, and the **Derived?** check box is selected for them.</span></span>

    ![Izveidotie atvasinātie testa gadījumi](./media/use_rsa_tool_03.png)

    <span data-ttu-id="167cb-124">Pakalpojumā Azure DevOps tiek automātiski izveidots atvasinātais testa gadījums.</span><span class="sxs-lookup"><span data-stu-id="167cb-124">A derived test case is automatically created in Azure DevOps.</span></span> <span data-ttu-id="167cb-125">Tas ir testa gadījuma **Izveidot jaunu preci** pakārtotais vienums un ir atzīmēts ar īpašu atslēgvārdu: **RSAT:DerivedTestSteps**.</span><span class="sxs-lookup"><span data-stu-id="167cb-125">It's a child item of the **Create a new product** test case and is tagged with a special keyword: **RSAT:DerivedTestSteps**.</span></span> <span data-ttu-id="167cb-126">Šie testa gadījumi arī tiek automātiski pievienoti testa plānam pakalpojumā Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="167cb-126">These test cases are also automatically added to the test plan in Azure DevOps.</span></span>

    ![RSAT:DerivedTestSteps atslēgvārds](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > <span data-ttu-id="167cb-128">Ja kāda iemesla dēļ izveidotie atvasinātie testa gadījumi nav pareizā secībā, dodieties uz Azure DevOps un pārkārtojiet testa gadījumus testu komplektā, lai RSAT varētu tos palaist pareizā secībā.</span><span class="sxs-lookup"><span data-stu-id="167cb-128">If, for any reason, the derived test cases that are created aren't in the correct order, go to Azure DevOps, and reorder the test cases in the test suite, so that RSAT can run them in the correct order.</span></span>

4. <span data-ttu-id="167cb-129">Atlasiet atvasinātos testa gadījumus un pēc tam atlasiet **Rediģēt**, lai atvērtu atbilstošos Excel parametru failus.</span><span class="sxs-lookup"><span data-stu-id="167cb-129">Select the derived test cases, and then select **Edit** to open the corresponding Excel parameter files.</span></span>
5. <span data-ttu-id="167cb-130">Rediģējiet šos Excel parametru failus tādā pašā veidā, kā rediģējāt pamata failus.</span><span class="sxs-lookup"><span data-stu-id="167cb-130">Edit these Excel parameter files in the same way that you edited the parent files.</span></span> <span data-ttu-id="167cb-131">Citiem vārdiem sakot, pārliecinieties, ka preces ID ir iestatīts tā, lai tas tiktu ģenerēts automātiski.</span><span class="sxs-lookup"><span data-stu-id="167cb-131">In other words, make sure that the product ID is set so that it's automatically generated.</span></span> <span data-ttu-id="167cb-132">Turklāt pārliecinieties, ka saglabātais mainīgais tiek kopēts atbilstošajos laukos.</span><span class="sxs-lookup"><span data-stu-id="167cb-132">Also make sure that the saved variable is copied to the relevant fields.</span></span>
6. <span data-ttu-id="167cb-133">Abu Excel parametru failu cilnē **Vispārīgi** atjauniniet lauka **Uzņēmums** vērtību uz **USSI**, lai atvasinātie testa gadījumi tiktu izpildīti attiecībā pret citu juridisko personu, nevis to, kas norādīta pamata testa gadījumam.</span><span class="sxs-lookup"><span data-stu-id="167cb-133">On the **General** tab of both Excel parameter files, update the value of the **Company** field to **USSI**, so that the derived test cases will be run against a different legal entity than the parent test case.</span></span> <span data-ttu-id="167cb-134">Lai palaistu testa gadījumus attiecībā pret noteiktu lietotāju (vai lomu, kas saistīta ar noteiktu lietotāju), varat atjaunināt lauka **Testa lietotājs** vērtību.</span><span class="sxs-lookup"><span data-stu-id="167cb-134">To run the test cases against a specific user (or the role that is associated with a specific user), you can update the value of the **Test User** field.</span></span>
7. <span data-ttu-id="167cb-135">Atlasiet **Palaist**un pārliecinieties, ka prece ir izveidota gan USMF juridiskajai personai, gan USSI juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="167cb-135">Select **Run**, and validate that the product is created in both the USMF legal entity and the USSI legal entity.</span></span>

### <a name="validate-notifications"></a><span data-ttu-id="167cb-136">Paziņojumu validēšana</span><span class="sxs-lookup"><span data-stu-id="167cb-136">Validate notifications</span></span>

<span data-ttu-id="167cb-137">Šo funkciju var izmantot, lai pārbaudītu, vai darbība ir notikusi.</span><span class="sxs-lookup"><span data-stu-id="167cb-137">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="167cb-138">Piemēram, kad tiek izveidots un pēc tam sākts ražošanas pasūtījums, programma parāda ziņojumu “Ražošana — Sākums”, lai informētu, ka ražošanas pasūtījums ir sākts.</span><span class="sxs-lookup"><span data-stu-id="167cb-138">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Paziņojums Ražošana — Sākums](./media/use_rsa_tool_05.png)

<span data-ttu-id="167cb-140">Šo ziņojumu varat validēt ar RSAT, ievadot ziņojuma tekstu atbilstošā ieraksta Excel parametru faila cilnē **MessageValidation**.</span><span class="sxs-lookup"><span data-stu-id="167cb-140">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Ziņojuma validēšanas cilne](./media/use_rsa_tool_06.png)

<span data-ttu-id="167cb-142">Pēc testa gadījuma palaišanas ziņojums Excel parametru failā tiek salīdzināts ar ziņojumu, kas tiek parādīts programmā.</span><span class="sxs-lookup"><span data-stu-id="167cb-142">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="167cb-143">Ja ziņojumi nesakrīt, testa gadījums ir nesekmīgs.</span><span class="sxs-lookup"><span data-stu-id="167cb-143">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="167cb-144">Excel parametru faila cilnē **MessageValidation** varat ievadīt vairāk nekā vienu ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="167cb-144">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="167cb-145">Ziņojumi var būt arī kļūdu vai brīdinājuma ziņojumi, nevis informācijas ziņojumi.</span><span class="sxs-lookup"><span data-stu-id="167cb-145">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="validate-values-by-using-operators"></a><span data-ttu-id="167cb-146">Vērtību validēšana, izmantojot operatorus</span><span class="sxs-lookup"><span data-stu-id="167cb-146">Validate values by using operators</span></span>

<span data-ttu-id="167cb-147">Iepriekšējās RSAT versijās bija iespējams validēt vērtības tikai tad, ja kontroles vērtība bija vienāda ar paredzēto vērtību.</span><span class="sxs-lookup"><span data-stu-id="167cb-147">In previous versions of RSAT, you could validate values only if a control value equaled an expected value.</span></span> <span data-ttu-id="167cb-148">Jaunais līdzeklis ļauj validēt mainīgo, kas nav vienāds ar, ir mazāks par vai ir lielāks par norādīto vērtību.</span><span class="sxs-lookup"><span data-stu-id="167cb-148">The new feature lets you validate that a variable isn't equal to, is less than, or is more than a specified value.</span></span>

- <span data-ttu-id="167cb-149">Lai izmantotu šo līdzekli, atveriet failu **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**, kas atrodas RSAT instalācijas mapē (piemēram, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), un mainiet tālāk norādītā elementa vērtību no **false** uz **true**.</span><span class="sxs-lookup"><span data-stu-id="167cb-149">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    <span data-ttu-id="167cb-150">Excel parametru failā tiek parādīts jauns laiks **Operators**.</span><span class="sxs-lookup"><span data-stu-id="167cb-150">In the Excel parameter file, a new **Operator** field appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="167cb-151">Ja izmantojat vecāku RSAT versiju, ir jāģenerē jauni Excel parametru faili.</span><span class="sxs-lookup"><span data-stu-id="167cb-151">If you've been using an older version of RSAT, you must generate new Excel parameter files.</span></span>

    ![Lauks Operators](./media/use_rsa_tool_07.png)

<span data-ttu-id="167cb-153">Tālāk norādītajā piemērā ir parādīts, kā varat izmantot šo līdzekli, lai pārbaudītu, vai rīcībā esošo krājumu daudzums ir vairāk nekā 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="167cb-153">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="167cb-154">Demonstrācijas datos uzņēmumā **USMF** izveidojiet uzdevuma ierakstu, kurā ir tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="167cb-154">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="167cb-155">Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="167cb-155">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="167cb-156">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="167cb-156">Use the Quick Filter to find records.</span></span> <span data-ttu-id="167cb-157">Piemēram, filtrējiet pēc lauka **Krājuma numurs**, izmantojot vērtību **1000**.</span><span class="sxs-lookup"><span data-stu-id="167cb-157">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="167cb-158">Atlasiet **Rīcībā esošie krājumi**.</span><span class="sxs-lookup"><span data-stu-id="167cb-158">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="167cb-159">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="167cb-159">Use the Quick Filter to find records.</span></span> <span data-ttu-id="167cb-160">Piemēram, filtrējiet pēc lauka **Vieta**, izmantojot vērtību **1**.</span><span class="sxs-lookup"><span data-stu-id="167cb-160">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="167cb-161">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="167cb-161">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="167cb-162">Pārbaudiet, vai lauka **Pieejamā kopsumma** vērtība ir **411.0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="167cb-162">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="167cb-163">Saglabājiet uzdevuma ierakstu BPM bibliotēkā pakalpojumā LCS un sinhronizējiet ar Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="167cb-163">Save the task recording to the BPM library in LCS, and sync it to Azure DevOps.</span></span>
3. <span data-ttu-id="167cb-164">Pievienojiet testa gadījumu testa plānam un ielādējiet testa gadījumu RSAT.</span><span class="sxs-lookup"><span data-stu-id="167cb-164">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="167cb-165">Atveriet Excel parametru failu.</span><span class="sxs-lookup"><span data-stu-id="167cb-165">Open the Excel parameter file.</span></span> <span data-ttu-id="167cb-166">Cilnē **InventOnhandItem** ir redzama sadaļa **Validēt InventOnhandItem**, kurā ietverts lauks **Operators**.</span><span class="sxs-lookup"><span data-stu-id="167cb-166">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![Lauks Operators](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="167cb-168">Lai pārbaudītu, vai rīcībā esošie krājumi vienmēr būs lielāki par 0, mainiet lauka **Vērtība** vērtību no **411** uz **0** un lauka **Operators** vērtību no vienādības zīmes (**=**) uz zīmi “lielāks par” (**\>**).</span><span class="sxs-lookup"><span data-stu-id="167cb-168">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![Nomainītas lauku Vērtība un Operators vērtības](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="167cb-170">Saglabājiet un aizveriet Excel parametru failu.</span><span class="sxs-lookup"><span data-stu-id="167cb-170">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="167cb-171">Atlasiet **Augšupielādēt**, lai saglabātu izmaiņas, kuras veicāt Excel parametru failā, pakalpojumā Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="167cb-171">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="167cb-172">Ja tagad lauka **Pieejamā kopsumma** vērtība norādītajam vienumam krājumā ir lielāka par 0 (nulli), testi būs sekmīgi neatkarīgi no faktiskās rīcībā esošo krājumu vērtības.</span><span class="sxs-lookup"><span data-stu-id="167cb-172">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="generator-logs"></a><span data-ttu-id="167cb-173">Ģeneratora žurnāli</span><span class="sxs-lookup"><span data-stu-id="167cb-173">Generator logs</span></span>

<span data-ttu-id="167cb-174">Šis līdzeklis izveido mapi, kurā atrodas palaisto testa gadījumu žurnāli.</span><span class="sxs-lookup"><span data-stu-id="167cb-174">This feature creates a folder that contains the logs of the test cases that have been run.</span></span>

- <span data-ttu-id="167cb-175">Lai izmantotu šo līdzekli, atveriet failu **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**, kas atrodas RSAT instalācijas mapē (piemēram, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), un mainiet tālāk norādītā elementa vērtību no **false** uz **true**.</span><span class="sxs-lookup"><span data-stu-id="167cb-175">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```
    <add key="LogGeneration" value="false" />
    ```

<span data-ttu-id="167cb-176">Kad testa gadījumi ir izpildīti, žurnāla failus varat atrast sadaļā **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span><span class="sxs-lookup"><span data-stu-id="167cb-176">After the test cases are run, you can find the log files under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span></span>

![Mape GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> <span data-ttu-id="167cb-178">Ja testa gadījumi pastāvēja, pirms mainījāt vērtību failā .config, šiem testa gadījumiem žurnāli netiks ģenerēti, kamēr netiks ģenerēti jauni testa izpildes faili.</span><span class="sxs-lookup"><span data-stu-id="167cb-178">If there were existing test cases before you changed the value in the .config file, logs won't be generated for those test cases until you generate new test execution files.</span></span>
> 
> ![Komanda Izveidot tikai teksta izpildes failus izvēlnē Jauns](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a><span data-ttu-id="167cb-180">Momentuzņēmums</span><span class="sxs-lookup"><span data-stu-id="167cb-180">Snapshot</span></span>

<span data-ttu-id="167cb-181">Šis līdzeklis uzņem to darbību ekrānuzņēmumus, kas tika izpildītas uzdevuma reģistrēšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="167cb-181">This feature takes screenshots of the steps that were performed during task recording.</span></span>

- <span data-ttu-id="167cb-182">Lai izmantotu šo līdzekli, atveriet failu **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**, kas atrodas RSAT instalācijas mapē (piemēram, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), un mainiet tālāk norādītā elementa vērtību no **false** uz **true**.</span><span class="sxs-lookup"><span data-stu-id="167cb-182">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="167cb-183">Sadaļā **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback** tiek izveidota atsevišķa mape katram izpildītajam testa gadījumam.</span><span class="sxs-lookup"><span data-stu-id="167cb-183">Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

![Testa gadījuma momentuzņēmuma mape](./media/use_rsa_tool_12.png)

<span data-ttu-id="167cb-185">Katrā no šīm mapēm varat atrast to darbību momentuzņēmumus, kas tika veiktas, kamēr tika izpildīti testa gadījumi.</span><span class="sxs-lookup"><span data-stu-id="167cb-185">In each of these folders, you can find snapshots of the steps that were performed while the test cases were run.</span></span>

![Momentuzņēmumu faili](./media/use_rsa_tool_13.png)

## <a name="assignment"></a><span data-ttu-id="167cb-187">Piešķire</span><span class="sxs-lookup"><span data-stu-id="167cb-187">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="167cb-188">Scenārijs</span><span class="sxs-lookup"><span data-stu-id="167cb-188">Scenario</span></span>

1. <span data-ttu-id="167cb-189">Preču noformētājs izveido jaunu izlaisto preci.</span><span class="sxs-lookup"><span data-stu-id="167cb-189">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="167cb-190">Ražošanas pārvaldnieks uzsāk ražošanas pasūtījumu, lai palielinātu krājumu līmeni līdz diviem gabaliem.</span><span class="sxs-lookup"><span data-stu-id="167cb-190">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="167cb-191">Ražošana sāk un beidz ražošanas pasūtījumu un pārbauda, vai rīcībā esošais daudzums ir divi gabali.</span><span class="sxs-lookup"><span data-stu-id="167cb-191">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="167cb-192">Pārdošanas grupa saņem četru jaunās preces gabalu pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="167cb-192">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="167cb-193">Tāpēc pārdošanas grupa atjaunina neto vajadzības, izmantojot dinamisko plānu.</span><span class="sxs-lookup"><span data-stu-id="167cb-193">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="167cb-194">Papildu noslodze nav pieejama, tādēļ noklusētā pasūtījuma politika ir iestatīta uz “pirkt, nevis izgatavot”.</span><span class="sxs-lookup"><span data-stu-id="167cb-194">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="167cb-195">Tādēļ tiek izveidots plānotais pirkšanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="167cb-195">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="167cb-196">Pircējs pievieno kreditoru, apstiprina plānoto pirkšanas pasūtījumu un pēc tam apstiprina pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="167cb-196">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="167cb-197">Kad nopirktās preces nonāk veikalā, veikala operators meklē saistīto pirkšanas pasūtījumu un saņem preces.</span><span class="sxs-lookup"><span data-stu-id="167cb-197">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="167cb-198">Tagad pasūtījums ir pabeigts, tādēļ preces var tikt izdotas un iepakotas, salīdzinot ar pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="167cb-198">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="167cb-199">Finance iegrāmato pirkšanas rēķinu un pārdošanas rēķinu.</span><span class="sxs-lookup"><span data-stu-id="167cb-199">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="167cb-200">Tālāk redzamajā attēlā ir parādīta šī scenārija plūsma.</span><span class="sxs-lookup"><span data-stu-id="167cb-200">The following illustration shows the flow for this scenario.</span></span>

![Demonstrācijas scenārija plūsma](./media/use_rsa_tool_14.png)

<span data-ttu-id="167cb-202">Tālāk redzamajā attēlā ir parādīti šī scenārija biznesa procesi RSAT.</span><span class="sxs-lookup"><span data-stu-id="167cb-202">The following illustration shows the business processes for this scenario in RSAT.</span></span>

![Demonstrācijas scenārija biznesa procesi](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="167cb-204">Stratēģija — galvenās mācību tēmas</span><span class="sxs-lookup"><span data-stu-id="167cb-204">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="167cb-205">Dati</span><span class="sxs-lookup"><span data-stu-id="167cb-205">Data</span></span>

- <span data-ttu-id="167cb-206">Pārliecinieties, ka jums ir reprezentatīvi datu apjomi (ražošanas/zelta konfigurācijas datu kopija un migrētie dati).</span><span class="sxs-lookup"><span data-stu-id="167cb-206">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="167cb-207">Kad ģenerējat jaunus datus, izmantojot uzdevuma reģistrētāju, izveidojiet testa nosaukumus, kas nekonfliktē ar esošiem nosaukumiem (piemēram, izmantojiet prefiksu **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="167cb-207">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="167cb-208">Izmantojiet Azure punkta laikā atjaunošanu, lai atkārtoti palaistu testus vidēs, kas nav 1. līmeņa vides.</span><span class="sxs-lookup"><span data-stu-id="167cb-208">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="167cb-209">Lai ģenerētu unikālu kombināciju, varat izmantot Excel funkcijas **RANDOM** un **NOW**, tomēr būs jāiegulda ievērojamas pūles.</span><span class="sxs-lookup"><span data-stu-id="167cb-209">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="167cb-210">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="167cb-210">Here is an example.</span></span>

    ```
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="167cb-211">Uzdevumu reģistrētājs</span><span class="sxs-lookup"><span data-stu-id="167cb-211">Task recorder</span></span>

- <span data-ttu-id="167cb-212">Pirms ierakstīšanas sākšanas definējiet scenārijus.</span><span class="sxs-lookup"><span data-stu-id="167cb-212">Define scenarios before you start recording.</span></span> <span data-ttu-id="167cb-213">Labi pārvaldītam projektam ir iepriekš definēti testa scenāriji.</span><span class="sxs-lookup"><span data-stu-id="167cb-213">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="167cb-214">Lai izveidotu testa gadījumu, apsveriet, cik prognozējams ir šo testa scenāriju rezultāts.</span><span class="sxs-lookup"><span data-stu-id="167cb-214">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="167cb-215">Sadaliet ierakstus, ja tos izpilda dažādas lomas vai ja pirms nākamās darbības ir gaidīšanas laiks vai ārējs notikums.</span><span class="sxs-lookup"><span data-stu-id="167cb-215">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="167cb-216">Neatlasiet vērtības sarakstos.</span><span class="sxs-lookup"><span data-stu-id="167cb-216">Avoid selecting values in lists.</span></span> <span data-ttu-id="167cb-217">Tā vietā izmantojiet teksta formātus, piemēram, **FIFO**, **AudioRM** un **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="167cb-217">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="167cb-218">Atlasot sarakstā, tiek ierakstīta vērtības pozīcija sarakstā, nevis pati vērtība.</span><span class="sxs-lookup"><span data-stu-id="167cb-218">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="167cb-219">Ja šim sarakstam tiek pievienoti krājumi, vērtības pozīcija var mainīties.</span><span class="sxs-lookup"><span data-stu-id="167cb-219">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="167cb-220">Tādēļ ierakstam tiks izmantots cits parametrs, un var tikt ietekmēta pārējā scenārija daļa.</span><span class="sxs-lookup"><span data-stu-id="167cb-220">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="167cb-221">Ņemiet vērā, ka var būt vairāki lietotāji.</span><span class="sxs-lookup"><span data-stu-id="167cb-221">Think about multi-user behavior.</span></span> <span data-ttu-id="167cb-222">Piemēram, nepieņemiet, ka jaunizveidotais pārdošanas pasūtījums vienmēr tiks atlasīts automātiski.</span><span class="sxs-lookup"><span data-stu-id="167cb-222">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="167cb-223">Tā vietā vienmēr izmantojiet filtru, lai atrastu pareizo pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="167cb-223">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="167cb-224">Tikko izveidotas preces nosaukuma saglabāšanai izmantojiet uzdevumu ierakstītāja kopēšanas funkciju, lai varētu to izmantot savienotos testa gadījumos.</span><span class="sxs-lookup"><span data-stu-id="167cb-224">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="167cb-225">Lietojiet uzdevumu ierakstītāja funkciju Validēt, lai iestatītu kontrolpunktus, kas pārbauda, vai darbības ir pareizi izpildītas.</span><span class="sxs-lookup"><span data-stu-id="167cb-225">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="167cb-226">RSAT</span><span class="sxs-lookup"><span data-stu-id="167cb-226">RSAT</span></span>

- <span data-ttu-id="167cb-227">Lai palaistu testu citā uzņēmumā, varat nomainīt uzņēmumu Excel parametru faila cilnē **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="167cb-227">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="167cb-228">Pārliecinieties, ka iestatījumi un dati nesen atlasītajā uzņēmumā ir pieejami.</span><span class="sxs-lookup"><span data-stu-id="167cb-228">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="167cb-229">Varat mainīt testa lietotāju Excel parametru faila cilnē **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="167cb-229">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="167cb-230">Norādiet tā lietotāja e-pasta ID, kurš izpildīs testa gadījumu.</span><span class="sxs-lookup"><span data-stu-id="167cb-230">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="167cb-231">Šādā veidā testu var izpildīt, izmantojot norādītā lietotāja drošības atļaujas.</span><span class="sxs-lookup"><span data-stu-id="167cb-231">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="167cb-232">Lai nogaidītu pirms testa sākšanas, varat noteikt pauzi Excel parametru faila cilnē **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="167cb-232">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="167cb-233">Šo pauzi var izmantot pakešuzdevumā (piemēram, ja darbplūsma ir jāizpilda, pirms var izpildīt nākamo darbību.)</span><span class="sxs-lookup"><span data-stu-id="167cb-233">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="167cb-234">Papildu skriptēšana</span><span class="sxs-lookup"><span data-stu-id="167cb-234">Advanced scripting</span></span>

### <a name="command-line"></a><span data-ttu-id="167cb-235">Komandrinda</span><span class="sxs-lookup"><span data-stu-id="167cb-235">Command line</span></span>

<span data-ttu-id="167cb-236">RSAT var izsaukt no **komandu uzvednes** loga.</span><span class="sxs-lookup"><span data-stu-id="167cb-236">RSAT can be called from a **Command Prompt** window.</span></span>

> [!NOTE]
> <span data-ttu-id="167cb-237">Pārbaudiet, vai vides mainīgajam **TestRoot** ir iestatīts RSAT instalācijas ceļš.</span><span class="sxs-lookup"><span data-stu-id="167cb-237">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="167cb-238">(Operētājsistēmā Microsoft Windows atveriet **Vadības panelis**, atlasiet **Sistēma un drošība \> Sistēma \> Sistēmas papildiestatījumi** un pēc tam atlasiet **Vides mainīgie**.)</span><span class="sxs-lookup"><span data-stu-id="167cb-238">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="167cb-239">Atveriet **komandu uzvednes** logu kā administrators.</span><span class="sxs-lookup"><span data-stu-id="167cb-239">Open a **Command Prompt** window as an admin.</span></span>
2. <span data-ttu-id="167cb-240">Palaidiet rīku no instalācijas direktorija.</span><span class="sxs-lookup"><span data-stu-id="167cb-240">Run the tool from the installation directory.</span></span>

    ```
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="167cb-241">Attēlojiet visas komandas saraksta veidā.</span><span class="sxs-lookup"><span data-stu-id="167cb-241">List all commands.</span></span>

    ```
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        list
        listtestsuite suite_name
        download test_case_id output_dir
        generate test_case_id output_dir
        generatederived parent_test_case_id test_plan_id test_suite_id
        generatetestonly test_case_id output_dir
        edit excel_file
        playback excel_file
        playbackmany excel_file1 [excel_file2 [.. excel_fileN]]
        playbackbyid test_case_id1 [test_case_id2 [.. test_case_idN]]
        playbacksuite suite_name
        clear
        help
        about
        quit
    ```

### <a name="windows-powershell-examples"></a><span data-ttu-id="167cb-242">Windows PowerShell piemēri</span><span class="sxs-lookup"><span data-stu-id="167cb-242">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="167cb-243">Testa gadījuma palaišana ciklā</span><span class="sxs-lookup"><span data-stu-id="167cb-243">Run a test case in a loop</span></span>

<span data-ttu-id="167cb-244">Jums ir testa skripts, ar kuru tiek izveidots jauns debitors.</span><span class="sxs-lookup"><span data-stu-id="167cb-244">You have a test script that creates a new customer.</span></span> <span data-ttu-id="167cb-245">Izmantojot skriptēšanu, šo testa gadījumu var palaist ciklā, pirms katra atkārtojuma izpildes randomizējot tālāk norādītos datus.</span><span class="sxs-lookup"><span data-stu-id="167cb-245">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="167cb-246">Debitora ID</span><span class="sxs-lookup"><span data-stu-id="167cb-246">Customer ID</span></span>
- <span data-ttu-id="167cb-247">Debitora nosaukums</span><span class="sxs-lookup"><span data-stu-id="167cb-247">Customer name</span></span>
- <span data-ttu-id="167cb-248">Debitora adrese</span><span class="sxs-lookup"><span data-stu-id="167cb-248">Customer address</span></span>

<span data-ttu-id="167cb-249">Klienta ID formāts vienmēr būs *ATCUS\<numurs\>*, kur \<numurs\> ir vērtība no **000000001** līdz **999999999**.</span><span class="sxs-lookup"><span data-stu-id="167cb-249">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="167cb-250">Šajā piemērā izmantots viens parametrs **start**, lai definētu pirmo izmantoto numuru.</span><span class="sxs-lookup"><span data-stu-id="167cb-250">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="167cb-251">Tiek izmantots otrs parametrs **nr**, lai definētu izveidojamo debitoru skaitu.</span><span class="sxs-lookup"><span data-stu-id="167cb-251">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="167cb-252">Katram atkārtojumam parametri Excel parametru failā tiek mainīti, izmantojot funkciju UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="167cb-252">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="167cb-253">Pēc tam RSAT komandrinda tiek izsaukta funkcijā RunTestCase.</span><span class="sxs-lookup"><span data-stu-id="167cb-253">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="167cb-254">Atveriet Microsoft Windows PowerShell integrētās skriptēšanas vidi (ISE) administratora režīmā un ielīmējiet tālāk norādīto kodu logā ar nosaukumu **Untitled1.ps1**.</span><span class="sxs-lookup"><span data-stu-id="167cb-254">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

```
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to excel file parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="167cb-255">No Microsoft Dynamics 365 datiem atkarīga skripta palaišana</span><span class="sxs-lookup"><span data-stu-id="167cb-255">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="167cb-256">Tālāk norādītajā piemērā izmantots atvērta datu protokola (OData) izsaukums, lai atrastu pirkšanas pasūtījuma statusu.</span><span class="sxs-lookup"><span data-stu-id="167cb-256">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="167cb-257">Ja statuss nav **iekļauts rēķinā**, varat, piemēram, izsaukt RSAT testa gadījumu, kas iegrāmato rēķinu.</span><span class="sxs-lookup"><span data-stu-id="167cb-257">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

```
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```
