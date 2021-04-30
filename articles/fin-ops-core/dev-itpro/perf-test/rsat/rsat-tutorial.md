---
title: Regression Suite Automation Tool apmācība
description: Šajā tēmā ir parādīts, kā izmantot Regression Suite Automation Tool (RSAT). Tajā ir aprakstīti dažādi līdzekļi un sniegti piemēri, kuros izmantota papildu skriptēšana.
author: robinarh
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: a194e14c76827650e6752f331081ebe0c2130a13
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866160"
---
# <a name="regression-suite-automation-tool-tutorial"></a><span data-ttu-id="73a71-104">Regression Suite Automation Tool apmācība</span><span class="sxs-lookup"><span data-stu-id="73a71-104">Regression suite automation tool tutorial</span></span>

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="73a71-105">Izmantojiet interneta pārlūka rīkus, lai lejupielādētu un saglabātu šo lapu PDF formātā.</span><span class="sxs-lookup"><span data-stu-id="73a71-105">Use your internet browser tools to download and save this page in pdf format.</span></span>

<span data-ttu-id="73a71-106">Šajā apmācībā ir aprakstīti daži Regression Suite Automation Tool (RSAT) papildu līdzekļi, ietverta demonstrācijas piešķire un aprakstīta stratēģija un galvenās mācību tēmas.</span><span class="sxs-lookup"><span data-stu-id="73a71-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="notable-features-of-rsat-and-task-recorder"></a><span data-ttu-id="73a71-107">Ievērojami RSAT un uzdevumu reģistrētāja līdzekļi</span><span class="sxs-lookup"><span data-stu-id="73a71-107">Notable Features of RSAT and Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="73a71-108">Lauka vērtības validēšana</span><span class="sxs-lookup"><span data-stu-id="73a71-108">Validate a field value</span></span>

<span data-ttu-id="73a71-109">RSAT ļauj iekļaut pārbaudes soļus jūsu pārbaudes gadījumā, lai validētu paredzētās vērtības.</span><span class="sxs-lookup"><span data-stu-id="73a71-109">RSAT allows you to include validation steps within your test case to validate expected values.</span></span> <span data-ttu-id="73a71-110">Lai iegūtu vairāk informācijas par šo līdzekli, skatiet rakstu [Pārbaudīt paredzētās vērtības](rsat-validate-expected.md).</span><span class="sxs-lookup"><span data-stu-id="73a71-110">For information about this feature, see the article [Validate expected values](rsat-validate-expected.md).</span></span>

<span data-ttu-id="73a71-111">Tālāk norādītajā piemērā ir parādīts, kā varat izmantot šo līdzekli, lai pārbaudītu, vai rīcībā esošo krājumu daudzums ir vairāk nekā 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="73a71-111">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="73a71-112">Demonstrācijas datos uzņēmumā **USMF** izveidojiet uzdevuma ierakstu, kurā ir tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="73a71-112">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="73a71-113">Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="73a71-113">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="73a71-114">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="73a71-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="73a71-115">Piemēram, filtrējiet pēc lauka **Krājuma numurs**, izmantojot vērtību **1000**.</span><span class="sxs-lookup"><span data-stu-id="73a71-115">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="73a71-116">Atlasiet **Rīcībā esošie krājumi**.</span><span class="sxs-lookup"><span data-stu-id="73a71-116">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="73a71-117">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="73a71-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="73a71-118">Piemēram, filtrējiet pēc lauka **Vieta**, izmantojot vērtību **1**.</span><span class="sxs-lookup"><span data-stu-id="73a71-118">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="73a71-119">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="73a71-119">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="73a71-120">Pārbaudiet, vai lauka **Pieejamā kopsumma** vērtība ir **411.0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="73a71-120">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="73a71-121">Saglabājiet uzdevuma reģistrēšanu kā **izstrādāja ierakstu** un pievienojiet to testa gadījumam Azure Devops.</span><span class="sxs-lookup"><span data-stu-id="73a71-121">Save the task recording as a **developer recording** and attach it to your test case in Azure Devops.</span></span>
3. <span data-ttu-id="73a71-122">Pievienojiet testa gadījumu testa plānam un ielādējiet testa gadījumu RSAT.</span><span class="sxs-lookup"><span data-stu-id="73a71-122">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="73a71-123">Atveriet Excel parametra failu un dodieties uz cilni **TestCaseSteps**.</span><span class="sxs-lookup"><span data-stu-id="73a71-123">Open the Excel parameter file and go to the **TestCaseSteps** tab.</span></span>
5. <span data-ttu-id="73a71-124">Lai pārbaudītu, vai rīcībā esošie krājumi vienmēr būs vairāk par **0**, dodieties uz soli **Pārbaudīt kopējo pieejamo** un mainiet tā vērtību no **411** uz **0**.</span><span class="sxs-lookup"><span data-stu-id="73a71-124">To validate whether the inventory on-hand will always be more than **0**, go to the **Validate Total Available** step and change its value from **411** to **0**.</span></span> <span data-ttu-id="73a71-125">Mainiet **Operatora** lauka vērtību no vienādības zīmes (**=**) uz lielāku par zīmi (**\>**).</span><span class="sxs-lookup"><span data-stu-id="73a71-125">Change the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>
6. <span data-ttu-id="73a71-126">Saglabājiet un aizveriet Excel parametru failu.</span><span class="sxs-lookup"><span data-stu-id="73a71-126">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="73a71-127">Atlasiet **Augšupielādēt**, lai saglabātu izmaiņas, kuras veicāt Excel parametru failā, pakalpojumā Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="73a71-127">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="73a71-128">Ja tagad lauka **Pieejamā kopsumma** vērtība norādītajam vienumam krājumā ir lielāka par 0 (nulli), testi būs sekmīgi neatkarīgi no faktiskās rīcībā esošo krājumu vērtības.</span><span class="sxs-lookup"><span data-stu-id="73a71-128">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="saved-variables-and-chaining-of-test-cases"></a><span data-ttu-id="73a71-129">Saglabātie mainīgie un testa gadījumu ķēde</span><span class="sxs-lookup"><span data-stu-id="73a71-129">Saved variables and chaining of test cases</span></span>

<span data-ttu-id="73a71-130">Viens no RSAT svarīgākajiem līdzekļiem ir testa gadījumu savienošana ķēdē, tas ir, iespēja nodot testa mainīgos citiem testiem.</span><span class="sxs-lookup"><span data-stu-id="73a71-130">One of the key features of RSAT is the chaining of test cases, that is, the ability of a test to pass variables to other tests.</span></span> <span data-ttu-id="73a71-131">Lai iegūtu papildinformāciju, skatiet rakstu [Mainīgo kopēšana uz ķēdes testa gadījumiem](rsat-chain-test-cases.md).</span><span class="sxs-lookup"><span data-stu-id="73a71-131">For more information, see the article [Copy variables to chain test cases](rsat-chain-test-cases.md).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="73a71-132">Atvasināts testa gadījums</span><span class="sxs-lookup"><span data-stu-id="73a71-132">Derived test case</span></span>

<span data-ttu-id="73a71-133">RSAT ļauj izmantot vienu un to pašu uzdevuma reģistrēšanu ar vairākiem pārbaudes gadījumiem, iespējojot uzdevumu darbināt ar atšķirīgām datu konfigurācijām.</span><span class="sxs-lookup"><span data-stu-id="73a71-133">RSAT lets you use the same task recording with multiple test cases, enabling a task to run with different data configurations.</span></span> <span data-ttu-id="73a71-134">Papildinformācijai skatiet rakstu [Iegūtie testa gadījumi](rsat-derived-test-cases.md).</span><span class="sxs-lookup"><span data-stu-id="73a71-134">See the article [Derived test cases](rsat-derived-test-cases.md) for more information.</span></span>

### <a name="validate-notifications-and-messages"></a><span data-ttu-id="73a71-135">Pārbaudīt paziņojumus un ziņas</span><span class="sxs-lookup"><span data-stu-id="73a71-135">Validate notifications and messages</span></span>

<span data-ttu-id="73a71-136">Šo funkciju var izmantot, lai pārbaudītu, vai darbība ir notikusi.</span><span class="sxs-lookup"><span data-stu-id="73a71-136">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="73a71-137">Piemēram, kad tiek izveidots un pēc tam sākts ražošanas pasūtījums, programma parāda ziņojumu “Ražošana — Sākums”, lai informētu, ka ražošanas pasūtījums ir sākts.</span><span class="sxs-lookup"><span data-stu-id="73a71-137">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Paziņojums Ražošana — Sākums](./media/use_rsa_tool_05.png)

<span data-ttu-id="73a71-139">Šo ziņojumu varat validēt ar RSAT, ievadot ziņojuma tekstu atbilstošā ieraksta Excel parametru faila cilnē **MessageValidation**.</span><span class="sxs-lookup"><span data-stu-id="73a71-139">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Ziņojuma validēšanas cilne](./media/use_rsa_tool_06.png)

<span data-ttu-id="73a71-141">Pēc testa gadījuma palaišanas ziņojums Excel parametru failā tiek salīdzināts ar ziņojumu, kas tiek parādīts programmā.</span><span class="sxs-lookup"><span data-stu-id="73a71-141">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="73a71-142">Ja ziņojumi nesakrīt, testa gadījums ir nesekmīgs.</span><span class="sxs-lookup"><span data-stu-id="73a71-142">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="73a71-143">Excel parametru faila cilnē **MessageValidation** varat ievadīt vairāk nekā vienu ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="73a71-143">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="73a71-144">Ziņojumi var būt arī kļūdu vai brīdinājuma ziņojumi, nevis informācijas ziņojumi.</span><span class="sxs-lookup"><span data-stu-id="73a71-144">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="snapshot"></a><span data-ttu-id="73a71-145">Momentuzņēmums</span><span class="sxs-lookup"><span data-stu-id="73a71-145">Snapshot</span></span>

<span data-ttu-id="73a71-146">Šis līdzeklis uzņem to darbību ekrānuzņēmumus, kas tika izpildītas uzdevuma reģistrēšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="73a71-146">This feature takes screenshots of the steps that were performed during task recording.</span></span> <span data-ttu-id="73a71-147">Tas ir noderīgs audita vai atkļūdošanas nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="73a71-147">It is useful for auditing or debugging purposes.</span></span>

- <span data-ttu-id="73a71-148">Lai izmantotu šo līdzekli, atveriet failu **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**, kas atrodas RSAT instalācijas mapē (piemēram, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), un mainiet tālāk norādītā elementa vērtību no **false** uz **true**.</span><span class="sxs-lookup"><span data-stu-id="73a71-148">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="73a71-149">Kad tiek palaists testa gadījums, RSAT ģenerēs soļu momentuzņēmumus (attēlus) pārbaudes gadījumu atskaņošanas mapē darba direktorijā.</span><span class="sxs-lookup"><span data-stu-id="73a71-149">When your run the test case, RSAT will generate snapshots (images) of the steps in the playback folder of the test cases in the working diretory.</span></span> <span data-ttu-id="73a71-150">Ja tiek izmantota vecāka RSAT versija, attēli tiek saglabāti **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, tiek izveidota atsevišķa mape katram testa gadījumam, kas tiek palaists.</span><span class="sxs-lookup"><span data-stu-id="73a71-150">If you are using an older version of RSAT, the images are saved to **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

## <a name="assignment"></a><span data-ttu-id="73a71-151">Piešķire</span><span class="sxs-lookup"><span data-stu-id="73a71-151">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="73a71-152">Scenārijs</span><span class="sxs-lookup"><span data-stu-id="73a71-152">Scenario</span></span>

1. <span data-ttu-id="73a71-153">Preču noformētājs izveido jaunu izlaisto preci.</span><span class="sxs-lookup"><span data-stu-id="73a71-153">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="73a71-154">Ražošanas pārvaldnieks uzsāk ražošanas pasūtījumu, lai palielinātu krājumu līmeni līdz diviem gabaliem.</span><span class="sxs-lookup"><span data-stu-id="73a71-154">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="73a71-155">Ražošana sāk un beidz ražošanas pasūtījumu un pārbauda, vai rīcībā esošais daudzums ir divi gabali.</span><span class="sxs-lookup"><span data-stu-id="73a71-155">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="73a71-156">Pārdošanas grupa saņem četru jaunās preces gabalu pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="73a71-156">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="73a71-157">Tāpēc pārdošanas grupa atjaunina neto vajadzības, izmantojot dinamisko plānu.</span><span class="sxs-lookup"><span data-stu-id="73a71-157">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="73a71-158">Papildu noslodze nav pieejama, tādēļ noklusētā pasūtījuma politika ir iestatīta uz “pirkt, nevis izgatavot”.</span><span class="sxs-lookup"><span data-stu-id="73a71-158">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="73a71-159">Tādēļ tiek izveidots plānotais pirkšanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="73a71-159">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="73a71-160">Pircējs pievieno kreditoru, apstiprina plānoto pirkšanas pasūtījumu un pēc tam apstiprina pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="73a71-160">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="73a71-161">Kad nopirktās preces nonāk veikalā, veikala operators meklē saistīto pirkšanas pasūtījumu un saņem preces.</span><span class="sxs-lookup"><span data-stu-id="73a71-161">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="73a71-162">Tagad pasūtījums ir pabeigts, tādēļ preces var tikt izdotas un iepakotas, salīdzinot ar pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="73a71-162">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="73a71-163">Finance iegrāmato pirkšanas rēķinu un pārdošanas rēķinu.</span><span class="sxs-lookup"><span data-stu-id="73a71-163">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="73a71-164">Tālāk redzamajā attēlā ir parādīta šī scenārija plūsma.</span><span class="sxs-lookup"><span data-stu-id="73a71-164">The following illustration shows the flow for this scenario.</span></span>

![Demonstrācijas scenārija plūsma](./media/use_rsa_tool_14.png)

<span data-ttu-id="73a71-166">Sekojošajā attēlā redzama biznesa procesu hierarhija šim scenārijam LCS biznesa procesu modelētājā.</span><span class="sxs-lookup"><span data-stu-id="73a71-166">The following illustration shows the business processes hierarchy for this scenario in the LCS Business Process Modeler.</span></span>

![Demonstrācijas scenārija biznesa procesi](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="73a71-168">Stratēģija — galvenās mācību tēmas</span><span class="sxs-lookup"><span data-stu-id="73a71-168">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="73a71-169">Dati</span><span class="sxs-lookup"><span data-stu-id="73a71-169">Data</span></span>

- <span data-ttu-id="73a71-170">Pārliecinieties, ka jums ir reprezentatīvi datu apjomi (ražošanas/zelta konfigurācijas datu kopija un migrētie dati).</span><span class="sxs-lookup"><span data-stu-id="73a71-170">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="73a71-171">Kad ģenerējat jaunus datus, izmantojot uzdevuma reģistrētāju, izveidojiet testa nosaukumus, kas nekonfliktē ar esošiem nosaukumiem (piemēram, izmantojiet prefiksu **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="73a71-171">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="73a71-172">Izmantojiet Azure punkta laikā atjaunošanu, lai atkārtoti palaistu testus vidēs, kas nav 1. līmeņa vides.</span><span class="sxs-lookup"><span data-stu-id="73a71-172">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="73a71-173">Lai ģenerētu unikālu kombināciju, varat izmantot Excel funkcijas **RANDOM** un **NOW**, tomēr būs jāiegulda ievērojamas pūles.</span><span class="sxs-lookup"><span data-stu-id="73a71-173">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="73a71-174">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="73a71-174">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="73a71-175">Uzdevumu reģistrētājs</span><span class="sxs-lookup"><span data-stu-id="73a71-175">Task recorder</span></span>

- <span data-ttu-id="73a71-176">Pirms ierakstīšanas sākšanas definējiet scenārijus.</span><span class="sxs-lookup"><span data-stu-id="73a71-176">Define scenarios before you start recording.</span></span> <span data-ttu-id="73a71-177">Labi pārvaldītam projektam ir iepriekš definēti testa scenāriji.</span><span class="sxs-lookup"><span data-stu-id="73a71-177">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="73a71-178">Lai izveidotu testa gadījumu, apsveriet, cik prognozējams ir šo testa scenāriju rezultāts.</span><span class="sxs-lookup"><span data-stu-id="73a71-178">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="73a71-179">Sadaliet ierakstus, ja tos izpilda dažādas lomas vai ja pirms nākamās darbības ir gaidīšanas laiks vai ārējs notikums.</span><span class="sxs-lookup"><span data-stu-id="73a71-179">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="73a71-180">Neatlasiet vērtības sarakstos.</span><span class="sxs-lookup"><span data-stu-id="73a71-180">Avoid selecting values in lists.</span></span> <span data-ttu-id="73a71-181">Tā vietā izmantojiet teksta formātus, piemēram, **FIFO**, **AudioRM** un **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="73a71-181">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="73a71-182">Atlasot sarakstā, tiek ierakstīta vērtības pozīcija sarakstā, nevis pati vērtība.</span><span class="sxs-lookup"><span data-stu-id="73a71-182">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="73a71-183">Ja šim sarakstam tiek pievienoti krājumi, vērtības pozīcija var mainīties.</span><span class="sxs-lookup"><span data-stu-id="73a71-183">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="73a71-184">Tādēļ ierakstam tiks izmantots cits parametrs, un var tikt ietekmēta pārējā scenārija daļa.</span><span class="sxs-lookup"><span data-stu-id="73a71-184">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="73a71-185">Ņemiet vērā, ka var būt vairāki lietotāji.</span><span class="sxs-lookup"><span data-stu-id="73a71-185">Think about multi-user behavior.</span></span> <span data-ttu-id="73a71-186">Piemēram, nepieņemiet, ka jaunizveidotais pārdošanas pasūtījums vienmēr tiks atlasīts automātiski.</span><span class="sxs-lookup"><span data-stu-id="73a71-186">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="73a71-187">Tā vietā vienmēr izmantojiet filtru, lai atrastu pareizo pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="73a71-187">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="73a71-188">Tikko izveidotas preces nosaukuma saglabāšanai izmantojiet uzdevumu ierakstītāja kopēšanas funkciju, lai varētu to izmantot savienotos testa gadījumos.</span><span class="sxs-lookup"><span data-stu-id="73a71-188">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="73a71-189">Lietojiet uzdevumu ierakstītāja funkciju Validēt, lai iestatītu kontrolpunktus, kas pārbauda, vai darbības ir pareizi izpildītas.</span><span class="sxs-lookup"><span data-stu-id="73a71-189">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="73a71-190">RSAT</span><span class="sxs-lookup"><span data-stu-id="73a71-190">RSAT</span></span>

- <span data-ttu-id="73a71-191">Lai palaistu testu citā uzņēmumā, varat nomainīt uzņēmumu Excel parametru faila cilnē **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="73a71-191">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="73a71-192">Pārliecinieties, ka iestatījumi un dati nesen atlasītajā uzņēmumā ir pieejami.</span><span class="sxs-lookup"><span data-stu-id="73a71-192">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="73a71-193">Varat mainīt testa lietotāju Excel parametru faila cilnē **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="73a71-193">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="73a71-194">Norādiet tā lietotāja e-pasta ID, kurš izpildīs testa gadījumu.</span><span class="sxs-lookup"><span data-stu-id="73a71-194">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="73a71-195">Šādā veidā testu var izpildīt, izmantojot norādītā lietotāja drošības atļaujas.</span><span class="sxs-lookup"><span data-stu-id="73a71-195">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="73a71-196">Lai nogaidītu pirms testa sākšanas, varat noteikt pauzi Excel parametru faila cilnē **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="73a71-196">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="73a71-197">Šo pauzi var izmantot pakešuzdevumā (piemēram, ja darbplūsma ir jāizpilda, pirms var izpildīt nākamo darbību.)</span><span class="sxs-lookup"><span data-stu-id="73a71-197">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="73a71-198">Papildu skriptēšana</span><span class="sxs-lookup"><span data-stu-id="73a71-198">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="73a71-199">CLI</span><span class="sxs-lookup"><span data-stu-id="73a71-199">CLI</span></span>

<span data-ttu-id="73a71-200">RSAT var izsaukt no **Komandu uzvednes** vai **PowerShell** loga.</span><span class="sxs-lookup"><span data-stu-id="73a71-200">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="73a71-201">Pārbaudiet, vai vides mainīgajam **TestRoot** ir iestatīts RSAT instalācijas ceļš.</span><span class="sxs-lookup"><span data-stu-id="73a71-201">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="73a71-202">(Operētājsistēmā Microsoft Windows atveriet **Vadības panelis**, atlasiet **Sistēma un drošība \> Sistēma \> Sistēmas papildiestatījumi** un pēc tam atlasiet **Vides mainīgie**.)</span><span class="sxs-lookup"><span data-stu-id="73a71-202">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="73a71-203">Atveriet **Komandu uzvednes** vai **PowerShell** logu kā administrators.</span><span class="sxs-lookup"><span data-stu-id="73a71-203">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="73a71-204">Dodieties uz RSAT instalācijas direktoriju.</span><span class="sxs-lookup"><span data-stu-id="73a71-204">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="73a71-205">Attēlojiet visas komandas saraksta veidā.</span><span class="sxs-lookup"><span data-stu-id="73a71-205">List all commands.</span></span>

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a><span data-ttu-id="73a71-206">?</span><span class="sxs-lookup"><span data-stu-id="73a71-206">?</span></span>

<span data-ttu-id="73a71-207">Rāda palīdzību par visām pieejamām komandām un to parametriem.</span><span class="sxs-lookup"><span data-stu-id="73a71-207">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a><span data-ttu-id="73a71-208">?: Neobligāti parametri</span><span class="sxs-lookup"><span data-stu-id="73a71-208">?: Optional parameters</span></span>

<span data-ttu-id="73a71-209">`command`: Kur ``[command]`` ir viena no tālāk norādītajām komandām.</span><span class="sxs-lookup"><span data-stu-id="73a71-209">`command`: Where ``[command]`` is one of the commands specified below.</span></span>

#### <a name="about"></a><span data-ttu-id="73a71-210">par programmu</span><span class="sxs-lookup"><span data-stu-id="73a71-210">about</span></span>

<span data-ttu-id="73a71-211">Rāda pašreizējo versiju.</span><span class="sxs-lookup"><span data-stu-id="73a71-211">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="73a71-212">cls</span><span class="sxs-lookup"><span data-stu-id="73a71-212">cls</span></span>

<span data-ttu-id="73a71-213">Notīra ekrānu.</span><span class="sxs-lookup"><span data-stu-id="73a71-213">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a><span data-ttu-id="73a71-214">lejupielādēt</span><span class="sxs-lookup"><span data-stu-id="73a71-214">download</span></span>

<span data-ttu-id="73a71-215">Lejupielādē pielikumus norādītajam testa gadījumam izvades direktorijā.</span><span class="sxs-lookup"><span data-stu-id="73a71-215">Downloads attachments for the specified test case to the output directory.</span></span>
<span data-ttu-id="73a71-216">Varat izmantot ``list`` komandu, lai iegūtu visus pieejamos pārbaudes gadījumus.</span><span class="sxs-lookup"><span data-stu-id="73a71-216">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="73a71-217">Izmantojiet jebkuru vērtību no pirmās kolonnas kā **test_case_id** parametru.</span><span class="sxs-lookup"><span data-stu-id="73a71-217">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="download-required-parameters"></a><span data-ttu-id="73a71-218">lejupielāde: obligātie parametri</span><span class="sxs-lookup"><span data-stu-id="73a71-218">download: required parameters</span></span>

+ <span data-ttu-id="73a71-219">`test_case_id`: Parāda testa gadījuma ID.</span><span class="sxs-lookup"><span data-stu-id="73a71-219">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="73a71-220">`output_dir`: Attēlo izvades direktoriju.</span><span class="sxs-lookup"><span data-stu-id="73a71-220">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="73a71-221">Direktorijam ir jāpastāv.</span><span class="sxs-lookup"><span data-stu-id="73a71-221">The directory must exist.</span></span>

##### <a name="download-examples"></a><span data-ttu-id="73a71-222">lejupielāde: piemēri</span><span class="sxs-lookup"><span data-stu-id="73a71-222">download: examples</span></span>

`download 123 c:\temp\rsat`

`download 765 c:\rsat\last`

#### <a name="edit"></a><span data-ttu-id="73a71-223">rediģēt</span><span class="sxs-lookup"><span data-stu-id="73a71-223">edit</span></span>

<span data-ttu-id="73a71-224">Ļauj atvērt parametru failu Excel programmā un to rediģēt.</span><span class="sxs-lookup"><span data-stu-id="73a71-224">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a><span data-ttu-id="73a71-225">rediģēt: obligātie parametri</span><span class="sxs-lookup"><span data-stu-id="73a71-225">edit: required parameters</span></span>

+ <span data-ttu-id="73a71-226">`excel_file`: Ir jāietver pilns ceļš uz esošu Excel failu.</span><span class="sxs-lookup"><span data-stu-id="73a71-226">`excel_file`: Must contain a full path to an existing Excel file.</span></span>

##### <a name="edit-examples"></a><span data-ttu-id="73a71-227">rediģēt: piemēri</span><span class="sxs-lookup"><span data-stu-id="73a71-227">edit: examples</span></span>

`edit c:\RSAT\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a><span data-ttu-id="73a71-228">ģenerēt</span><span class="sxs-lookup"><span data-stu-id="73a71-228">generate</span></span>

<span data-ttu-id="73a71-229">Ģenerē pārbaudes izpildi un parametru failus norādītajam testa gadījumam izvades direktorijā.</span><span class="sxs-lookup"><span data-stu-id="73a71-229">Generates test execution and parameter files for the specified test case in the output directory.</span></span> <span data-ttu-id="73a71-230">Varat izmantot ``list`` komandu, lai iegūtu visus pieejamos pārbaudes gadījumus.</span><span class="sxs-lookup"><span data-stu-id="73a71-230">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="73a71-231">Izmantojiet jebkuru vērtību no pirmās kolonnas kā **test_case_id** parametru.</span><span class="sxs-lookup"><span data-stu-id="73a71-231">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="generate-required-parameters"></a><span data-ttu-id="73a71-232">ģenerēt: nepieciešamos parametrus</span><span class="sxs-lookup"><span data-stu-id="73a71-232">generate: required parameters</span></span>

+ <span data-ttu-id="73a71-233">`test_case_id`: Parāda testa gadījuma ID.</span><span class="sxs-lookup"><span data-stu-id="73a71-233">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="73a71-234">`output_dir`: Attēlo izvades direktoriju.</span><span class="sxs-lookup"><span data-stu-id="73a71-234">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="73a71-235">Direktorijam ir jāpastāv.</span><span class="sxs-lookup"><span data-stu-id="73a71-235">The directory must exist.</span></span>

##### <a name="generate-examples"></a><span data-ttu-id="73a71-236">ģenerēt: piemēri</span><span class="sxs-lookup"><span data-stu-id="73a71-236">generate: examples</span></span>

`generate 123 c:\temp\rsat`

`generate 765 c:\rsat\last`

#### <a name="generatederived"></a><span data-ttu-id="73a71-237">generatederived</span><span class="sxs-lookup"><span data-stu-id="73a71-237">generatederived</span></span>

<span data-ttu-id="73a71-238">Ģenerē jaunu testa gadījumu, kas iegūts no norādītā testa gadījuma.</span><span class="sxs-lookup"><span data-stu-id="73a71-238">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="73a71-239">Varat izmantot ``list`` komandu, lai iegūtu visus pieejamos pārbaudes gadījumus.</span><span class="sxs-lookup"><span data-stu-id="73a71-239">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="73a71-240">Izmantojiet jebkuru vērtību no pirmās kolonnas kā **test_case_id** parametru.</span><span class="sxs-lookup"><span data-stu-id="73a71-240">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-required-parameters"></a><span data-ttu-id="73a71-241">generatederived: nepieciešamos parametrus</span><span class="sxs-lookup"><span data-stu-id="73a71-241">generatederived: required parameters</span></span>

+ <span data-ttu-id="73a71-242">`parent_test_case_id`: Parāda vecāka pārbaudes gadījuma ID.</span><span class="sxs-lookup"><span data-stu-id="73a71-242">`parent_test_case_id`: Represents the parent test case ID.</span></span>
+ <span data-ttu-id="73a71-243">`test_plan_id`: Parāda testa plāna ID.</span><span class="sxs-lookup"><span data-stu-id="73a71-243">`test_plan_id`: Represents the test plan ID.</span></span>
+ <span data-ttu-id="73a71-244">`test_suite_id`: Parāda testa komplekta ID.</span><span class="sxs-lookup"><span data-stu-id="73a71-244">`test_suite_id`: Represents the test suite ID.</span></span>

##### <a name="generatederived-examples"></a><span data-ttu-id="73a71-245">generatederived: piemēri</span><span class="sxs-lookup"><span data-stu-id="73a71-245">generatederived: examples</span></span>

`generatederived 123 8901 678`

#### <a name="generatetestonly"></a><span data-ttu-id="73a71-246">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="73a71-246">generatetestonly</span></span>

<span data-ttu-id="73a71-247">Ģenerē tikai pārbaudes izpildes failu norādītajam testa gadījumam izvades direktorijā.</span><span class="sxs-lookup"><span data-stu-id="73a71-247">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="73a71-248">Varat izmantot ``list`` komandu, lai iegūtu visus pieejamos pārbaudes gadījumus.</span><span class="sxs-lookup"><span data-stu-id="73a71-248">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="73a71-249">Izmantojiet jebkuru vērtību no pirmās kolonnas kā **test_case_id** parametru.</span><span class="sxs-lookup"><span data-stu-id="73a71-249">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="generatetestonly-required-parameters"></a><span data-ttu-id="73a71-250">generatesonly: nepieciešamos parametrus</span><span class="sxs-lookup"><span data-stu-id="73a71-250">generatetestonly: required parameters</span></span>

+ <span data-ttu-id="73a71-251">`test_case_id`: Parāda testa gadījuma ID.</span><span class="sxs-lookup"><span data-stu-id="73a71-251">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="73a71-252">`output_dir`: Attēlo izvades direktoriju.</span><span class="sxs-lookup"><span data-stu-id="73a71-252">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="73a71-253">Direktorijam ir jāpastāv.</span><span class="sxs-lookup"><span data-stu-id="73a71-253">The directory must exist.</span></span>

##### <a name="generatetestonly-examples"></a><span data-ttu-id="73a71-254">generatesonly: piemēri</span><span class="sxs-lookup"><span data-stu-id="73a71-254">generatetestonly: examples</span></span>

`generatetestonly 123 c:\temp\rsat`

`generatetestonly 765 c:\rsat\last`

#### <a name="generatetestsuite"></a><span data-ttu-id="73a71-255">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="73a71-255">generatetestsuite</span></span>

<span data-ttu-id="73a71-256">Ģenerē visus testa gadījumus norādītajam komplektam izvades direktorijā.</span><span class="sxs-lookup"><span data-stu-id="73a71-256">Generates all test cases for the specified suite in the output directory.</span></span> <span data-ttu-id="73a71-257">Varat izmantot ``listtestsuitenames`` komandu, lai iegūtu visus pieejamos pārbaudes komplektus.</span><span class="sxs-lookup"><span data-stu-id="73a71-257">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="73a71-258">Izmantojiet jebkuru vērtību no pirmās kolonnas kā **test_suite_name** parametru.</span><span class="sxs-lookup"><span data-stu-id="73a71-258">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="generatetestsuite-required-parameters"></a><span data-ttu-id="73a71-259">generatetestsuite: nepieciešamos parametrus</span><span class="sxs-lookup"><span data-stu-id="73a71-259">generatetestsuite: required parameters</span></span>

+ <span data-ttu-id="73a71-260">`test_suite_name`: Parāda testa komplekta nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="73a71-260">`test_suite_name`: Represents the test suite name.</span></span>
+ <span data-ttu-id="73a71-261">`output_dir`: Attēlo izvades direktoriju.</span><span class="sxs-lookup"><span data-stu-id="73a71-261">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="73a71-262">Direktorijam ir jāpastāv.</span><span class="sxs-lookup"><span data-stu-id="73a71-262">The directory must exist.</span></span>

##### <a name="generatetestsuite-examples"></a><span data-ttu-id="73a71-263">generatetestsuite: piemēri</span><span class="sxs-lookup"><span data-stu-id="73a71-263">generatetestsuite: examples</span></span>

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite Purchase c:\rsat\last`

#### <a name="help"></a><span data-ttu-id="73a71-264">palīdzība</span><span class="sxs-lookup"><span data-stu-id="73a71-264">help</span></span>

<span data-ttu-id="73a71-265">Identisks ar [?](#section)</span><span class="sxs-lookup"><span data-stu-id="73a71-265">Identical to the [?](#section)</span></span> <span data-ttu-id="73a71-266">komanda.</span><span class="sxs-lookup"><span data-stu-id="73a71-266">command.</span></span>

#### <a name="list"></a><span data-ttu-id="73a71-267">sarakstā</span><span class="sxs-lookup"><span data-stu-id="73a71-267">list</span></span>

<span data-ttu-id="73a71-268">Uzskaita visus pieejamos pārbaudes gadījumus.</span><span class="sxs-lookup"><span data-stu-id="73a71-268">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a><span data-ttu-id="73a71-269">listtestplans</span><span class="sxs-lookup"><span data-stu-id="73a71-269">listtestplans</span></span>

<span data-ttu-id="73a71-270">Uzskaita visus pieejamos pārbaudes plānus.</span><span class="sxs-lookup"><span data-stu-id="73a71-270">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a><span data-ttu-id="73a71-271">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="73a71-271">listtestsuite</span></span>

<span data-ttu-id="73a71-272">Uzskaita testa gadījumus norādītajam testu komplektam.</span><span class="sxs-lookup"><span data-stu-id="73a71-272">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="73a71-273">Varat izmantot ``listtestsuitenames`` komandu, lai iegūtu visus pieejamos pārbaudes komplektus.</span><span class="sxs-lookup"><span data-stu-id="73a71-273">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="73a71-274">Izmantojiet jebkuru vērtību no pirmās kolonnas kā **suite_name** parametru.</span><span class="sxs-lookup"><span data-stu-id="73a71-274">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="listtestsuite-required-parameters"></a><span data-ttu-id="73a71-275">listtestsuite: nepieciešamie parametrus</span><span class="sxs-lookup"><span data-stu-id="73a71-275">listtestsuite: required parameters</span></span>

+ <span data-ttu-id="73a71-276">`suite_name`: Nepieciešamā komplekta nosaukums.</span><span class="sxs-lookup"><span data-stu-id="73a71-276">`suite_name`: Name of the desired suite.</span></span>

##### <a name="listtestsuite-examples"></a><span data-ttu-id="73a71-277">listtestsuite: piemēri</span><span class="sxs-lookup"><span data-stu-id="73a71-277">listtestsuite: examples</span></span>

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitenames"></a><span data-ttu-id="73a71-278">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="73a71-278">listtestsuitenames</span></span>

<span data-ttu-id="73a71-279">Uzskaita visus pieejamos pārbaudes komplektus.</span><span class="sxs-lookup"><span data-stu-id="73a71-279">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a><span data-ttu-id="73a71-280">atskaņošana</span><span class="sxs-lookup"><span data-stu-id="73a71-280">playback</span></span>

<span data-ttu-id="73a71-281">Atskaņo pārbaudes gadījumu, izmantojot Excel failu.</span><span class="sxs-lookup"><span data-stu-id="73a71-281">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="playback-required-parameters"></a><span data-ttu-id="73a71-282">atskaņošana: obligātie parametri</span><span class="sxs-lookup"><span data-stu-id="73a71-282">playback: required parameters</span></span>

+ <span data-ttu-id="73a71-283">`excel_file`: Pilns ceļš uz Excel failu.</span><span class="sxs-lookup"><span data-stu-id="73a71-283">`excel_file`: A full path to the Excel file.</span></span> <span data-ttu-id="73a71-284">Failam ir jāpastāv.</span><span class="sxs-lookup"><span data-stu-id="73a71-284">File must exist.</span></span>

##### <a name="playback-examples"></a><span data-ttu-id="73a71-285">atskaņošana: piemēri</span><span class="sxs-lookup"><span data-stu-id="73a71-285">playback: examples</span></span>

`playback c:\RSAT\TestCaseParameters\sample1.xlsx`

`playback e:\temp\test.xlsx`

#### <a name="playbackbyid"></a><span data-ttu-id="73a71-286">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="73a71-286">playbackbyid</span></span>

<span data-ttu-id="73a71-287">Vienlaicīgi atskaņo vairākus pārbaudes gadījumus.</span><span class="sxs-lookup"><span data-stu-id="73a71-287">Plays back multiple test cases at once.</span></span> <span data-ttu-id="73a71-288">Varat izmantot ``list`` komandu, lai iegūtu visus pieejamos pārbaudes gadījumus.</span><span class="sxs-lookup"><span data-stu-id="73a71-288">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="73a71-289">Izmantojiet jebkuru vērtību no pirmās kolonnas kā **test_case_id** parametru.</span><span class="sxs-lookup"><span data-stu-id="73a71-289">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-required-parameters"></a><span data-ttu-id="73a71-290">playbackbyid: obligātie parametri</span><span class="sxs-lookup"><span data-stu-id="73a71-290">playbackbyid: required parameters</span></span>

+ <span data-ttu-id="73a71-291">`test_case_id1`: Esošā testa gadījuma ID.</span><span class="sxs-lookup"><span data-stu-id="73a71-291">`test_case_id1`: ID of exisiting test case.</span></span>
+ <span data-ttu-id="73a71-292">`test_case_id2`: Esošā testa gadījuma ID.</span><span class="sxs-lookup"><span data-stu-id="73a71-292">`test_case_id2`: ID of exisiting test case.</span></span>
+ <span data-ttu-id="73a71-293">`test_case_idN`: Esošā testa gadījuma ID.</span><span class="sxs-lookup"><span data-stu-id="73a71-293">`test_case_idN`: ID of exisiting test case.</span></span>

##### <a name="playbackbyid-examples"></a><span data-ttu-id="73a71-294">playbackbyid: piemēri</span><span class="sxs-lookup"><span data-stu-id="73a71-294">playbackbyid: examples</span></span>

`playbackbyid 878`

`playbackbyid 2345 667 135`

#### <a name="playbackmany"></a><span data-ttu-id="73a71-295">playbackmany</span><span class="sxs-lookup"><span data-stu-id="73a71-295">playbackmany</span></span>

<span data-ttu-id="73a71-296">Vienlaicīgi atskaņo daudzus pārbaudes gadījumus, izmantojot Excel failus.</span><span class="sxs-lookup"><span data-stu-id="73a71-296">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="playbackmany-required-parameters"></a><span data-ttu-id="73a71-297">playbackbymany: obligātie parametri</span><span class="sxs-lookup"><span data-stu-id="73a71-297">playbackmany: required parameters</span></span>

+ <span data-ttu-id="73a71-298">`excel_file1`: Pilns ceļš uz Excel failu.</span><span class="sxs-lookup"><span data-stu-id="73a71-298">`excel_file1`: Full path to the Excel file.</span></span> <span data-ttu-id="73a71-299">Failam ir jāpastāv.</span><span class="sxs-lookup"><span data-stu-id="73a71-299">File must exist.</span></span>
+ <span data-ttu-id="73a71-300">`excel_file2`: Pilns ceļš uz Excel failu.</span><span class="sxs-lookup"><span data-stu-id="73a71-300">`excel_file2`: Full path to the Excel file.</span></span> <span data-ttu-id="73a71-301">Failam ir jāpastāv.</span><span class="sxs-lookup"><span data-stu-id="73a71-301">File must exist.</span></span>
+ <span data-ttu-id="73a71-302">`excel_fileN`: Pilns ceļš uz Excel failu.</span><span class="sxs-lookup"><span data-stu-id="73a71-302">`excel_fileN`: Full path to the Excel file.</span></span> <span data-ttu-id="73a71-303">Failam ir jāpastāv.</span><span class="sxs-lookup"><span data-stu-id="73a71-303">File must exist.</span></span>

##### <a name="playbackmany-examples"></a><span data-ttu-id="73a71-304">playbackmany: piemēri</span><span class="sxs-lookup"><span data-stu-id="73a71-304">playbackmany: examples</span></span>

`playbackmany c:\RSAT\TestCaseParameters\param1.xlsx`

`playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a><span data-ttu-id="73a71-305">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="73a71-305">playbacksuite</span></span>

<span data-ttu-id="73a71-306">Atskaņo visus testa gadījumus no norādītā testu komplekta.</span><span class="sxs-lookup"><span data-stu-id="73a71-306">Plays back all test cases from the specified test suite.</span></span>
<span data-ttu-id="73a71-307">Varat izmantot ``listtestsuitenames`` komandu, lai iegūtu visus pieejamos pārbaudes komplektus.</span><span class="sxs-lookup"><span data-stu-id="73a71-307">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="73a71-308">Izmantojiet jebkuru vērtību no pirmās kolonnas kā **suite_name** parametru.</span><span class="sxs-lookup"><span data-stu-id="73a71-308">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="playbacksuite-required-parameters"></a><span data-ttu-id="73a71-309">playbacksuite: obligātie parametri</span><span class="sxs-lookup"><span data-stu-id="73a71-309">playbacksuite: required parameters</span></span>

+ <span data-ttu-id="73a71-310">`suite_name`: Nepieciešamā komplekta nosaukums.</span><span class="sxs-lookup"><span data-stu-id="73a71-310">`suite_name`: Name of the desired suite.</span></span>

##### <a name="playbacksuite-examples"></a><span data-ttu-id="73a71-311">playbacksuite: piemēri</span><span class="sxs-lookup"><span data-stu-id="73a71-311">playbacksuite: examples</span></span>

`playbacksuite suiteName`

`playbacksuite sample_suite`

#### <a name="quit"></a><span data-ttu-id="73a71-312">iziet</span><span class="sxs-lookup"><span data-stu-id="73a71-312">quit</span></span>

<span data-ttu-id="73a71-313">Aizver programmu.</span><span class="sxs-lookup"><span data-stu-id="73a71-313">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

#### <a name="upload"></a><span data-ttu-id="73a71-314">augšupielādēt</span><span class="sxs-lookup"><span data-stu-id="73a71-314">upload</span></span>

<span data-ttu-id="73a71-315">Augšupielādē visus failus, kas pieder norādītajam pārbaudes komplektam vai pārbaudes gadījumiem.</span><span class="sxs-lookup"><span data-stu-id="73a71-315">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="upload-required-parameters"></a><span data-ttu-id="73a71-316">augšupielāde: obligātie parametri</span><span class="sxs-lookup"><span data-stu-id="73a71-316">upload: required parameters</span></span>

+ <span data-ttu-id="73a71-317">`suite_name`: Augšupielādēs visus failus, kas pieder norādītajam pārbaudes komplektam.</span><span class="sxs-lookup"><span data-stu-id="73a71-317">`suite_name`: All files belonging to the specified test suite will be uploaded.</span></span>
+ <span data-ttu-id="73a71-318">`testcase_id`: Augšupielādēs visus failus, kas pieder norādītajam pārbaudes gadījumam(-iem).</span><span class="sxs-lookup"><span data-stu-id="73a71-318">`testcase_id`: All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="upload-examples"></a><span data-ttu-id="73a71-319">augšupielāde: piemēri</span><span class="sxs-lookup"><span data-stu-id="73a71-319">upload: examples</span></span>

`upload sample_suite`

`upload 123`

`upload 123 456`

#### <a name="uploadrecording"></a><span data-ttu-id="73a71-320">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="73a71-320">uploadrecording</span></span>

<span data-ttu-id="73a71-321">Augšupielādē vienīgi to ieraksta failu, kas pieder norādītajiem pārbaudes gadījumiem.</span><span class="sxs-lookup"><span data-stu-id="73a71-321">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="uploadrecording-required-parameters"></a><span data-ttu-id="73a71-322">uploadrecording: obligātie parametri</span><span class="sxs-lookup"><span data-stu-id="73a71-322">uploadrecording: required parameters</span></span>

+ <span data-ttu-id="73a71-323">`testcase_id`: Augšupielādē ieraksta failu, kas pieder norādītajiem pārbaudes gadījumiem.</span><span class="sxs-lookup"><span data-stu-id="73a71-323">`testcase_id`: Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="uploadrecording-examples"></a><span data-ttu-id="73a71-324">uploadrecording: piemēri</span><span class="sxs-lookup"><span data-stu-id="73a71-324">uploadrecording: examples</span></span>

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a><span data-ttu-id="73a71-325">lietojums</span><span class="sxs-lookup"><span data-stu-id="73a71-325">usage</span></span>

<span data-ttu-id="73a71-326">Tiek rādīti divi veidi, kā izsaukt šo programmu: viens izmanto noklusējuma iestatījumu failu, otrs nodrošina iestatījumu failu.</span><span class="sxs-lookup"><span data-stu-id="73a71-326">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

### <a name="windows-powershell-examples"></a><span data-ttu-id="73a71-327">Windows PowerShell piemēri</span><span class="sxs-lookup"><span data-stu-id="73a71-327">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="73a71-328">Testa gadījuma palaišana ciklā</span><span class="sxs-lookup"><span data-stu-id="73a71-328">Run a test case in a loop</span></span>

<span data-ttu-id="73a71-329">Jums ir testa skripts, ar kuru tiek izveidots jauns debitors.</span><span class="sxs-lookup"><span data-stu-id="73a71-329">You have a test script that creates a new customer.</span></span> <span data-ttu-id="73a71-330">Izmantojot skriptēšanu, šo testa gadījumu var palaist ciklā, pirms katra atkārtojuma izpildes randomizējot tālāk norādītos datus.</span><span class="sxs-lookup"><span data-stu-id="73a71-330">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="73a71-331">Debitora ID</span><span class="sxs-lookup"><span data-stu-id="73a71-331">Customer ID</span></span>
- <span data-ttu-id="73a71-332">Debitora nosaukums</span><span class="sxs-lookup"><span data-stu-id="73a71-332">Customer name</span></span>
- <span data-ttu-id="73a71-333">Debitora adrese</span><span class="sxs-lookup"><span data-stu-id="73a71-333">Customer address</span></span>

<span data-ttu-id="73a71-334">Klienta ID formāts vienmēr būs formātā *ATCUS\<number\>*, kur \<number\> ir vērtība no **000000001** līdz **999999999**.</span><span class="sxs-lookup"><span data-stu-id="73a71-334">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="73a71-335">Šajā piemērā izmantots viens parametrs **start**, lai definētu pirmo izmantoto numuru.</span><span class="sxs-lookup"><span data-stu-id="73a71-335">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="73a71-336">Tiek izmantots otrs parametrs **nr**, lai definētu izveidojamo debitoru skaitu.</span><span class="sxs-lookup"><span data-stu-id="73a71-336">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="73a71-337">Katram atkārtojumam parametri Excel parametru failā tiek mainīti, izmantojot funkciju UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="73a71-337">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="73a71-338">Pēc tam RSAT komandrinda tiek izsaukta funkcijā RunTestCase.</span><span class="sxs-lookup"><span data-stu-id="73a71-338">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="73a71-339">Atveriet Microsoft Windows PowerShell integrētās skriptēšanas vidi (ISE) administratora režīmā un ielīmējiet tālāk norādīto kodu logā ar nosaukumu **Untitled1.ps1**.</span><span class="sxs-lookup"><span data-stu-id="73a71-339">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

```powershell
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
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="73a71-340">No Microsoft Dynamics 365 datiem atkarīga skripta palaišana</span><span class="sxs-lookup"><span data-stu-id="73a71-340">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="73a71-341">Tālāk norādītajā piemērā izmantots atvērta datu protokola (OData) izsaukums, lai atrastu pirkšanas pasūtījuma statusu.</span><span class="sxs-lookup"><span data-stu-id="73a71-341">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="73a71-342">Ja statuss nav **iekļauts rēķinā**, varat, piemēram, izsaukt RSAT testa gadījumu, kas iegrāmato rēķinu.</span><span class="sxs-lookup"><span data-stu-id="73a71-342">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

```xpp
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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]