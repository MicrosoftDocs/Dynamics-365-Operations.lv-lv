---
title: Atkļūdot izpildītā ER formāta datu avotus, lai analizētu datu plūsmu un transformāciju
description: Šajā tēmā izskaidrots, kā atkļūdot izpildītā ER formāta datu avotus, lai labāk saprastu konfigurēto datu plūsmu un transformāciju.
author: NickSelin
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 3a486800f37dda7829aeeaa56a30285a92a61b9d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680786"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a><span data-ttu-id="03da5-103">Atkļūdot izpildītā ER formāta datu avotus, lai analizētu datu plūsmu un transformāciju</span><span class="sxs-lookup"><span data-stu-id="03da5-103">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="03da5-104">Kad jūs [konfigurējat](tasks/er-format-configuration-2016-11.md) Elektronisko pārskatu veidošanas (ER) risinājumu, lai izveidotu izejošos dokumentus, jūs nosakat metodes, kas tiek izmantotas, lai iegūtu datus no programmas un ievadītu tos ģenerētajā izvadē.</span><span class="sxs-lookup"><span data-stu-id="03da5-104">When you [configure](tasks/er-format-configuration-2016-11.md) an Electronic reporting (ER) solution to generate outbound documents, you define the methods that are used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="03da5-105">Lai nodrošinātu efektīvāku dzīves cikla atbalstu ER risinājumam, jūsu risinājumam jāsastāv no ER [datu modeļa](general-electronic-reporting.md#DataModelComponent) un tā [kartēšanas](general-electronic-reporting.md#ModelMappingComponent) komponentiem, kā arī ER [formāta](general-electronic-reporting.md#FormatComponentOutbound), un tās kartēšanas komponentiem, lai modeļa kartēšana būtu raksturīga lietojumprogrammai, turpretī citi komponenti saglabājas agnostiski programmā.</span><span class="sxs-lookup"><span data-stu-id="03da5-105">To make the life cycle support of the ER solution more efficient, your solution should consist of an ER [data model](general-electronic-reporting.md#DataModelComponent) and its [mapping](general-electronic-reporting.md#ModelMappingComponent) components, and also an ER [format](general-electronic-reporting.md#FormatComponentOutbound) and its mapping components, so that the model mapping is application-specific, whereas other components remain application-agnostic.</span></span> <span data-ttu-id="03da5-106">Tāpēc vairāki ER komponenti var [ietekmēt](general-electronic-reporting.md#FormatComponentOutbound) datu ievades procesu ģenerētajā izvadē.</span><span class="sxs-lookup"><span data-stu-id="03da5-106">Therefore, several ER components might [affect](general-electronic-reporting.md#FormatComponentOutbound) the process of entering data in the generated output.</span></span>

<span data-ttu-id="03da5-107">Dažkārt ģenerētās izvades dati izskatās citādi nekā tie paši dati programmas datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="03da5-107">Sometimes, the data of the generated output looks different than the same data in the application database.</span></span> <span data-ttu-id="03da5-108">Šādos gadījumos jums vēlēsieties noteikt, kurš ER komponents ir atbildīgs par datu pārveidošanu.</span><span class="sxs-lookup"><span data-stu-id="03da5-108">In these cases, you will want to determine which ER component is responsible for the data transformation.</span></span> <span data-ttu-id="03da5-109">ER datu avota atkļūdotāja līdzeklis ievērojami samazina šajā izmeklēšanā iesaistīto laiku un izmaksas.</span><span class="sxs-lookup"><span data-stu-id="03da5-109">The ER data source debugger feature significantly reduces the time and cost that are involved in this investigation.</span></span> <span data-ttu-id="03da5-110">Jūs varat pārtraukt ER formāta izpildi un atvērt datu avota atkļūdotāja interfeisu.</span><span class="sxs-lookup"><span data-stu-id="03da5-110">You can interrupt the execution of an ER format and open the data source debugger interface.</span></span> <span data-ttu-id="03da5-111">Tur varat pārlūkot pieejamos datu avotus un atlasīt atsevišķu datu avotu izpildei.</span><span class="sxs-lookup"><span data-stu-id="03da5-111">There, you can browse the available data sources and select an individual data source for execution.</span></span> <span data-ttu-id="03da5-112">Šī manuālā izpilde simulē datu avota izpildi, palaižot ER formāta patieso izpildi.</span><span class="sxs-lookup"><span data-stu-id="03da5-112">This manual execution simulates the execution of the data source during the real run of an ER format.</span></span> <span data-ttu-id="03da5-113">Rezultāts ir parādīts lapā, kur varat analizēt saņemtos datus.</span><span class="sxs-lookup"><span data-stu-id="03da5-113">The result is presented on a page where you can analyze the data that is received.</span></span>

<span data-ttu-id="03da5-114">Lai ieslēgtu datu avota atkļūdošanas līdzekli, iestatiet opciju **Iespējot datu atkļūdošanu, kad formāts tiek palaists** uz **Jā** ER lietotāja parametros.</span><span class="sxs-lookup"><span data-stu-id="03da5-114">To turn on the data source debugging feature, set the **Enable data debugging at format run** option to **Yes** in the ER user parameters.</span></span> <span data-ttu-id="03da5-115">Pēc tam varat sākt datu avota atkļūdošanu, kamēr tiek palaists ER formāts, lai izveidotu izejošos dokumentus.</span><span class="sxs-lookup"><span data-stu-id="03da5-115">You can then start data source debugging while you run an ER format to generate outbound documents.</span></span> <span data-ttu-id="03da5-116">Jūs varat arī izmantot opciju **Sākt atkļūdošanu**, lai iniciētu datu avota atkļūdošanu ER formātā, kas ir konfigurēts [ER operāciju veidotājā](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span><span class="sxs-lookup"><span data-stu-id="03da5-116">You can also use the **Start debugging** option to initiate data source debugging for an ER format that is configured in the [ER Operation designer](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span></span>

<span data-ttu-id="03da5-117">Šī tēma sniedz vadlīnijas datu avota atkļūdošanas uzsākšanai izpildītiem ER formātiem.</span><span class="sxs-lookup"><span data-stu-id="03da5-117">This topic provides guidelines for initiating data source debugging for executed ER formats.</span></span> <span data-ttu-id="03da5-118">Tajā ir paskaidrots, kā informācija var palīdzēt saprast datu plūsmu un datu transformācijas.</span><span class="sxs-lookup"><span data-stu-id="03da5-118">It explains how the information can help you understand the data flow and data transformations.</span></span> <span data-ttu-id="03da5-119">Šīs tēmas piemēri izmanto biznesa procesu kreditoru maksājumu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="03da5-119">The examples in this topic use the business process for vendor payments processing.</span></span>

## <a name="limitations"></a><span data-ttu-id="03da5-120">Ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="03da5-120">Limitations</span></span>

<span data-ttu-id="03da5-121">Datu avota atkļūdotāju var izmantot, lai piekļūtu datu avotu datiem, kas tiek izmantoti ER formātos, kas tiek palaisti, lai ģenerētu izejošos dokumentus.</span><span class="sxs-lookup"><span data-stu-id="03da5-121">The data source debugger can be used to access the data of data sources that are used in ER formats that are run to generate outbound documents.</span></span> <span data-ttu-id="03da5-122">To nevar izmantot, lai atkļūdotu datu avotus no ER formātiem, kas ir paredzēti, lai analizētu ienākošos dokumentus.</span><span class="sxs-lookup"><span data-stu-id="03da5-122">It can't be used to debug data sources of ER formats that are designed to parse inbound documents.</span></span>

<span data-ttu-id="03da5-123">Šādi ER formātu iestatījumi pašlaik nav pieejami datu avota atkļūdošanai:</span><span class="sxs-lookup"><span data-stu-id="03da5-123">The following settings of ER formats aren't currently accessible for data source debugging:</span></span>

- <span data-ttu-id="03da5-124">Formātu pārveidošanas</span><span class="sxs-lookup"><span data-stu-id="03da5-124">Format transformations</span></span>
- <span data-ttu-id="03da5-125">Apstiprināšanas noteikumu formatēšana un kartēšana</span><span class="sxs-lookup"><span data-stu-id="03da5-125">Format and mapping validation rules</span></span>
- <span data-ttu-id="03da5-126">Izteiksmju iespējošana</span><span class="sxs-lookup"><span data-stu-id="03da5-126">Enabling expressions</span></span>
- <span data-ttu-id="03da5-127">Detalizēta informācija par atmiņas datu apkopošanu</span><span class="sxs-lookup"><span data-stu-id="03da5-127">Details of in-memory data collection</span></span>

## <a name="prerequisites"></a><span data-ttu-id="03da5-128">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="03da5-128">Prerequisites</span></span>

- <span data-ttu-id="03da5-129">Lai izpildītu šīs tēmas piemērus, jums ir jābūt piekļuvei vienai no šādām [lomām](../sysadmin/tasks/assign-users-security-roles.md):</span><span class="sxs-lookup"><span data-stu-id="03da5-129">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="03da5-130">Elektroniskā pārskata izstrādātājs</span><span class="sxs-lookup"><span data-stu-id="03da5-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="03da5-131">Elektronisko pārskatu veidošanas funkcionālais konsultants</span><span class="sxs-lookup"><span data-stu-id="03da5-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="03da5-132">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="03da5-132">System administrator</span></span>

- <span data-ttu-id="03da5-133">Uzņēmumam jābūt iestatītam uz **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="03da5-133">The company must be set to **DEMF**.</span></span>

- <span data-ttu-id="03da5-134">Izpildiet šīs tēmas [1. papildinājumā](#appendix1) norādītās darbības, lai lejupielādētu Microsoft ER risinājuma komponentus, kas nepieciešami, lai apstrādātu kreditoru maksājumus.</span><span class="sxs-lookup"><span data-stu-id="03da5-134">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the Microsoft ER solution that are required to process vendor payments.</span></span>
- <span data-ttu-id="03da5-135">Izpildiet šīs tēmas [2. papildinājumā](#appendix2) norādītās darbības, lai sagatavotu kreditoru maksājumu parādu apstrādi, izmantojot ER risinājumu, ko lejupielādēsit.</span><span class="sxs-lookup"><span data-stu-id="03da5-135">Follow the steps in [Appendix 2](#appendix2) of this topic to prepare Accounts payable for vendor payment processing by using the ER solution that you will download.</span></span>

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a><span data-ttu-id="03da5-136">Apstrādāt kreditora maksājumu, lai iegūtu maksājuma failu</span><span class="sxs-lookup"><span data-stu-id="03da5-136">Process a vendor payment to get a payment file</span></span>

1. <span data-ttu-id="03da5-137">Izpildiet šīs tēmas [3. papildinājumā](#appendix3) norādītās darbības, lai apstrādātu kreditoru maksājumus.</span><span class="sxs-lookup"><span data-stu-id="03da5-137">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>

    ![Kreditora maksājumu apstrāde notiek](./media/er-data-debugger-process-payment.png)

2. <span data-ttu-id="03da5-139">Lejupielādējiet un saglabājiet zip failu vietējā datorā.</span><span class="sxs-lookup"><span data-stu-id="03da5-139">Download and save the zip file to your local computer.</span></span>
3. <span data-ttu-id="03da5-140">Izvelciet **ISO20022 Credit transfer.xml** maksājuma failu no zip faila.</span><span class="sxs-lookup"><span data-stu-id="03da5-140">Extract the **ISO20022 Credit transfer.xml** payment file from the zip file.</span></span>
4. <span data-ttu-id="03da5-141">Atveriet izgūto maksājuma failu, izmantojot XML failu skatītāju.</span><span class="sxs-lookup"><span data-stu-id="03da5-141">Open the extracted payment file by using the XML file viewer.</span></span>

    <span data-ttu-id="03da5-142">Maksājuma failā bankas konta starptautiskais bankas konta numurs (IBAN) nesatur atstarpes.</span><span class="sxs-lookup"><span data-stu-id="03da5-142">In the payment file, the International Bank Account Number (IBAN) code of the vendor bank account contains no spaces.</span></span> <span data-ttu-id="03da5-143">Tāpēc tas atšķiras no vērtības, kas tika [ievadīta](#enteredIBANcode) lapā **Bankas konti**.</span><span class="sxs-lookup"><span data-stu-id="03da5-143">Therefore, it differs from the value that was [entered](#enteredIBANcode) on the **Bank accounts** page.</span></span>

    ![IBAN kods bez atstarpēm](./media/er-data-debugger-payment-file.png)

    <span data-ttu-id="03da5-145">Jūs varat izmantot ER datu avota atkļūdotāju, lai uzzinātu, kurš ER risinājuma komponents tiek izmantots, lai saīsinātu atstarpes IBAN kodā.</span><span class="sxs-lookup"><span data-stu-id="03da5-145">You can use the ER data source debugger to learn which component of the ER solution is used to truncate spaces in the IBAN code.</span></span>

## <a name="turn-on-data-source-debugging"></a><span data-ttu-id="03da5-146">Ieslēgt datu avota atkļūdošanu</span><span class="sxs-lookup"><span data-stu-id="03da5-146">Turn on data source debugging</span></span>

1. <span data-ttu-id="03da5-147">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="03da5-147">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="03da5-148">Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.</span><span class="sxs-lookup"><span data-stu-id="03da5-148">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="03da5-149">Iestatiet opciju **Iespējot datu atkļūdošanu, kad formāts tiek palaists** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="03da5-149">Set the **Enable data debugging at format run** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="03da5-150">Šis parametrs ir lietotājam raksturīgs un uzņēmumam raksturīgs.</span><span class="sxs-lookup"><span data-stu-id="03da5-150">This parameter is user-specific and company-specific.</span></span>

    ![Lietotāja parametru dialoglodziņš](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a><span data-ttu-id="03da5-152">Apstrādāt kreditora maksājumu atkļūdošanai</span><span class="sxs-lookup"><span data-stu-id="03da5-152">Process a vendor payment for debugging</span></span>

1. <span data-ttu-id="03da5-153">Izpildiet šīs tēmas [3. papildinājumā](#appendix3) norādītās darbības, lai apstrādātu kreditoru maksājumus.</span><span class="sxs-lookup"><span data-stu-id="03da5-153">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>
2. <span data-ttu-id="03da5-154">Ziņojuma lodziņā atlasiet **Jā**, lai apstiprinātu, ka vēlaties pārtraukt kreditora maksājumu apstrādi, un tā vietā startējiet datu avota atkļūdošanu lapā **Atkļūdot datu avotus**.</span><span class="sxs-lookup"><span data-stu-id="03da5-154">In the message box, select **Yes** to confirm that you want to interrupt vendor payment processing and instead start data source debugging on the **Debug Datasources** page.</span></span>

    ![Apstiprinājuma ziņojuma lodziņš](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a><span data-ttu-id="03da5-156">Atkļūdot datu avotus, kas tiek izmantoti maksājuma apstrādei</span><span class="sxs-lookup"><span data-stu-id="03da5-156">Debug data sources that are used in payment processing</span></span>

### <a name="debug-the-model-mapping"></a><span data-ttu-id="03da5-157">Atkļūdot modeļa kartējumu</span><span class="sxs-lookup"><span data-stu-id="03da5-157">Debug the model mapping</span></span>

1. <span data-ttu-id="03da5-158">Lapā **Atkļūdošanas datu avoti**, kas atrodas darbības rūtī, atlasiet **Modeļa kartēšanu**, lai sāktu atkļūdot no šī ER komponenta.</span><span class="sxs-lookup"><span data-stu-id="03da5-158">On the **Debug Datasources** page, on the Action Pane, select **Model mapping** to start to debug from this ER component.</span></span>
2. <span data-ttu-id="03da5-159">Kreisajā pusē esošajā datu avota rūtī atlasiet **\$notSentTransactions** datu avotu un pēc tam atlasiet **Lasīt visus ierakstus**.</span><span class="sxs-lookup"><span data-stu-id="03da5-159">In the data source pane on the left, select the **\$notSentTransactions** data source, and then select **Read all records**.</span></span>

    <span data-ttu-id="03da5-160">Jūs varat izvēlēties **Lasīt 1 ierakstu**, **Lasīt 10 ierakstus**, **Lasīt 100 ierakstus** vai **Lasīt visus ierakstus**, lai piespiestu atbilstošo ierakstu skaitu, kas jālasa no atlasītā datu avota.</span><span class="sxs-lookup"><span data-stu-id="03da5-160">You can select **Read 1 record**, **Read 10 records**, **Read 100 records**, or **Read all records** to force the appropriate number of records to be read from the selected data source.</span></span> <span data-ttu-id="03da5-161">Šādā veidā jūs varat simulēt piekļuvi datu avotam no "Running ER" formāta.</span><span class="sxs-lookup"><span data-stu-id="03da5-161">In this way, you can simulate access to the data source from the running ER format.</span></span>

3. <span data-ttu-id="03da5-162">Datu rūts labajā pusē atlasiet rekvizītu **Izvērst visus**.</span><span class="sxs-lookup"><span data-stu-id="03da5-162">In the data pane on the right, select **Expand all**.</span></span>

    <span data-ttu-id="03da5-163">Jūs varat redzēt, ka **Ierakstu saraksta** veida atlasītais datu avots satur vienu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="03da5-163">You can see that the selected data source of the **Record list** type contains a single record.</span></span>

4. <span data-ttu-id="03da5-164">Paplašiniet **\$notSentTransactions** datu avotu un atlasiet ligzdoto **vendBankAccountInTransactionCompany()** metodi.</span><span class="sxs-lookup"><span data-stu-id="03da5-164">Expand the **\$notSentTransactions** data source, and select the nested **vendBankAccountInTransactionCompany()** method.</span></span>
5. <span data-ttu-id="03da5-165">Paplašiniet **vendBankAccountInTransactionCompany()** metodi un atlasiet ligzdoto **IBAN** lauku.</span><span class="sxs-lookup"><span data-stu-id="03da5-165">Expand the **vendBankAccountInTransactionCompany()** method, and select the nested **IBAN** field.</span></span>
6. <span data-ttu-id="03da5-166">Atlasiet **Iegūt vērtību**.</span><span class="sxs-lookup"><span data-stu-id="03da5-166">Select **Get value**.</span></span>

    <span data-ttu-id="03da5-167">Jūs varat izvēlēties **Iegūt vērtību**, lai piespiestu atlasītā datu avota atlasītā lauka vērtību lasīšanai.</span><span class="sxs-lookup"><span data-stu-id="03da5-167">You can select **Get value** to force the value of a selected field of the selected data source to be read.</span></span> <span data-ttu-id="03da5-168">Šādā veidā jūs varat simulēt piekļuvi laukam no "Running ER" formāta.</span><span class="sxs-lookup"><span data-stu-id="03da5-168">In this way, you can simulate access to this field from the running ER format.</span></span>

7. <span data-ttu-id="03da5-169">Atlasiet **Izvērst visas**.</span><span class="sxs-lookup"><span data-stu-id="03da5-169">Select **Expand all**.</span></span>

    ![IBAN lauka vērtība modeļa kartēšanā](./media/er-data-debugger-debugging-model-mapping.png)

    <span data-ttu-id="03da5-171">Kā redzat, modeļa kartēšana nav atbildīga par saīsinātajām atstarpēm, jo IBAN kods, ko tā atgriež kreditora bankas kontam, ietver atstarpes.</span><span class="sxs-lookup"><span data-stu-id="03da5-171">As you can see, the model mapping isn't responsible for the truncated spaces, because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="03da5-172">Tāpēc ir jāturpina datu avota atkļūdošana.</span><span class="sxs-lookup"><span data-stu-id="03da5-172">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format-mapping"></a><span data-ttu-id="03da5-173">Formāta kartēšanas atkļūdošana</span><span class="sxs-lookup"><span data-stu-id="03da5-173">Debug the format mapping</span></span>

1. <span data-ttu-id="03da5-174">Lapā **Atkļūdošanas datu avoti**, kas atrodas darbības rūtī, atlasiet **Formāta kartēšanu**, lai turpinātu atkļūdot no šī ER komponenta.</span><span class="sxs-lookup"><span data-stu-id="03da5-174">On the **Debug Datasources** page, on the Action Pane, select **Format mapping** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="03da5-175">Atlasiet **\$PaymentByDebtor** datu avotu un pēc tam atlasiet **Lasīt visus ierakstus**.</span><span class="sxs-lookup"><span data-stu-id="03da5-175">Select the **\$PaymentByDebtor** data source, and then select **Read all records**.</span></span>
3. <span data-ttu-id="03da5-176">Izvērsiet **\$PaymentByDebtor**.</span><span class="sxs-lookup"><span data-stu-id="03da5-176">Expand **\$PaymentByDebtor**.</span></span>
4. <span data-ttu-id="03da5-177">Izvērsiet **\$PaymentByDebtor.Lines** un pēc tam atlasiet **Lasīt visus ierakstus**.</span><span class="sxs-lookup"><span data-stu-id="03da5-177">Expand **\$PaymentByDebtor.Lines**, and then select **Read all records**.</span></span>
5. <span data-ttu-id="03da5-178">Izvērsiet **\$PaymentByDebtor.Lines.CreditorAccount**.</span><span class="sxs-lookup"><span data-stu-id="03da5-178">Expand **\$PaymentByDebtor.Lines.CreditorAccount**.</span></span>
6. <span data-ttu-id="03da5-179">Izvērsiet **\$PaymentByDebtor.Lines.CreditorAccount.Identification** un tad atlasiet **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span><span class="sxs-lookup"><span data-stu-id="03da5-179">Expand **\$PaymentByDebtor.Lines.CreditorAccount.Identification**, and then select **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span></span>
7. <span data-ttu-id="03da5-180">Atlasiet **Iegūt vērtību**.</span><span class="sxs-lookup"><span data-stu-id="03da5-180">Select **Get value**.</span></span>
8. <span data-ttu-id="03da5-181">Atlasiet **Izvērst visas**.</span><span class="sxs-lookup"><span data-stu-id="03da5-181">Select **Expand all**.</span></span>

    ![IBAN lauka vērtība formāta kartēšanā](./media/er-data-debugger-debugging-format-mapping.png)

    <span data-ttu-id="03da5-183">Kā redzat, formāta kartēšanas datu avoti nav atbildīgi par saīsinātajām atstarpēm, jo IBAN kods, ko tie atgriež kreditora bankas kontam, ietver atstarpes.</span><span class="sxs-lookup"><span data-stu-id="03da5-183">As you can see, the data sources of the format mapping aren't responsible for the truncated spaces, because the IBAN code that they return for the vendor bank account includes spaces.</span></span> <span data-ttu-id="03da5-184">Tāpēc ir jāturpina datu avota atkļūdošana.</span><span class="sxs-lookup"><span data-stu-id="03da5-184">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format"></a><span data-ttu-id="03da5-185">Formāta atkļūdošana</span><span class="sxs-lookup"><span data-stu-id="03da5-185">Debug the format</span></span>

1. <span data-ttu-id="03da5-186">Lapā **Atkļūdošanas datu avoti**, kas atrodas darbības rūtī, atlasiet **Formāts**, lai turpinātu atkļūdot no šī ER komponenta.</span><span class="sxs-lookup"><span data-stu-id="03da5-186">On the **Debug Datasources** page, on the Action Pane, select **Format** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="03da5-187">Izvērsiet formāta elementus, lai atlasītu **ISO20022CTReports**\> **XMLHeader**\> **Dokuments**\>**CstmrCdtTrfInitn**\> **PmtInf** un pēc tam atlasiet **Lasīt visus ierakstus**.</span><span class="sxs-lookup"><span data-stu-id="03da5-187">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf**, and then select **Read all records**.</span></span>
3. <span data-ttu-id="03da5-188">Izvērsiet formāta elementus, lai atlasītu **ISO20022CTReports** \> **XMLHeader** \> **Dokuments** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** un tad atlasiet **Lasīt visus ierakstus**.</span><span class="sxs-lookup"><span data-stu-id="03da5-188">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, and then select **Read all records**.</span></span>
4. <span data-ttu-id="03da5-189">Izvērsiet formāta elementus, lai atlasītu **ISO20022CTReports** \> **XMLHeader** \> **Dokuments** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** un tad atlasiet **Iegūt vērtību**.</span><span class="sxs-lookup"><span data-stu-id="03da5-189">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, and then select **Get value**.</span></span>
5. <span data-ttu-id="03da5-190">Atlasiet **Izvērst visas**.</span><span class="sxs-lookup"><span data-stu-id="03da5-190">Select **Expand all**.</span></span>

    ![IBAN lauka vērtība formātā](./media/er-data-debugger-debugging-format.png)

   <span data-ttu-id="03da5-192">Kā redzat, formāta saistīšana nav atbildīga par saīsinātajām atstarpēm, jo IBAN kods, ko tā atgriež kreditora bankas kontam, ietver atstarpes.</span><span class="sxs-lookup"><span data-stu-id="03da5-192">As you can see, the format binding isn't responsible for the truncated spaces because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="03da5-193">Tāpēc **BankIBAN** elements ir konfigurēts tā, lai izmantotu formāta transformāciju, kas saīsina atstarpes.</span><span class="sxs-lookup"><span data-stu-id="03da5-193">Therefore, the **BankIBAN** element is configured to use a format transformation that truncates spaces.</span></span>

6. <span data-ttu-id="03da5-194">Aizveriet datu avota atkļūdotāju.</span><span class="sxs-lookup"><span data-stu-id="03da5-194">Close the data source debugger.</span></span>

### <a name="review-the-format-transformations"></a><span data-ttu-id="03da5-195">Pārskatiet formāta transformācijas</span><span class="sxs-lookup"><span data-stu-id="03da5-195">Review the format transformations</span></span>

1. <span data-ttu-id="03da5-196">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="03da5-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="03da5-197">Lapā **Konfigurācijas** atlasiet **Maksājuma modelis** \> **ISO20022 kredīta pārskaitījums**.</span><span class="sxs-lookup"><span data-stu-id="03da5-197">On the **Configurations** page, select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="03da5-198">Atlasiet **Noformētājs** un tad izvērsiet elementus, lai atlasītu **Dokuments** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.</span><span class="sxs-lookup"><span data-stu-id="03da5-198">Select **Designer**, and then expand the elements to select **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.</span></span>

    ![BankIBAN elements lapā Formāta veidotājs](./media/er-data-debugger-referred-transformation.png)

    <span data-ttu-id="03da5-200">Kā redzat, **BankIBAN** elements ir konfigurēts, lai izmantotu **noņemt, kas nav burtcipari** transformāciju.</span><span class="sxs-lookup"><span data-stu-id="03da5-200">As you can see, the **BankIBAN** element is configured to use the **remove not alphanumeric** transformation.</span></span>

4. <span data-ttu-id="03da5-201">Atlasiet cilni **Transformācijas**.</span><span class="sxs-lookup"><span data-stu-id="03da5-201">Select the **Transformations** tab.</span></span>

    ![BankIBAN elementa transformāciju cilne](./media/er-data-debugger-transformation.png)

    <span data-ttu-id="03da5-203">Kā redzat, **noņemt, kas nav burtcipari** transformācija ir konfigurēta, lai izmantotu izteiksmi, kas saīsina atstarpes no nodrošinātās teksta virknes.</span><span class="sxs-lookup"><span data-stu-id="03da5-203">As you can see, the **remove not alphanumeric** transformation is configured to use an expression that truncates spaces from the text string that is provided.</span></span>

## <a name="start-to-debug-in-the-operation-designer"></a><span data-ttu-id="03da5-204">Sākt atkļūdot Operāciju noformētājā</span><span class="sxs-lookup"><span data-stu-id="03da5-204">Start to debug in the Operation designer</span></span>

<span data-ttu-id="03da5-205">Konfigurējot ER formāta melnraksta versiju, ko var palaist tieši no Operāciju noformētāja, varat piekļūt datu avota atkļūdotājam, darbības rūtī atlasot **Sākt atkļūdošanu**.</span><span class="sxs-lookup"><span data-stu-id="03da5-205">When you configure a draft version of the ER format that can be run directly from the Operation designer, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![Sākt atkļūdošanu poga lapā Formāta veidotājs](./media/er-data-debugger-run-from-designer.png)

<span data-ttu-id="03da5-207">Atkļūdošanai ir pieejami rediģējamā ER formāta kartēšanas un formāta komponenti.</span><span class="sxs-lookup"><span data-stu-id="03da5-207">The format mapping and format components of the ER format that is being edited are available for debugging.</span></span>

## <a name="start-to-debug-in-the-model-mapping-designer"></a><span data-ttu-id="03da5-208">Sākt atkļūdot Modeļa kartēšanas noformētājā</span><span class="sxs-lookup"><span data-stu-id="03da5-208">Start to debug in the Model mapping designer</span></span>

<span data-ttu-id="03da5-209">Konfigurējot ER modeļa kartēšanu, ko var palaist tieši no **Modeļa kartēšanas** lapas, varat piekļūt datu avota atkļūdotājam, darbības rūtī atlasot **Sākt atkļūdošanu**.</span><span class="sxs-lookup"><span data-stu-id="03da5-209">When you configure an ER model mapping that can be run from the **Model mapping** page, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![Sākt atkļūdošanu poga noformētāja lapā Modeļa kartēšana](./media/er-data-debugger-run-from-designer-mapping.png)

<span data-ttu-id="03da5-211">Rediģējamā ER kartēšanas komponenta modeļa komponents ir pieejams atkļūdošanai.</span><span class="sxs-lookup"><span data-stu-id="03da5-211">The model mapping component of the ER mapping that is being edited is available for debugging.</span></span>

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a><span data-ttu-id="03da5-212">1. papildinājums: Saņemiet ER risinājumu</span><span class="sxs-lookup"><span data-stu-id="03da5-212">Appendix 1: Get an ER solution</span></span>

### <a name="download-an-er-solution"></a><span data-ttu-id="03da5-213">ER risinājuma lejupielāde</span><span class="sxs-lookup"><span data-stu-id="03da5-213">Download an ER solution</span></span>

<span data-ttu-id="03da5-214">Ja vēlaties izmantot ER risinājumu, lai ģenerētu elektronisko maksājumu failu kreditora maksājumam, kas tiek apstrādāts, jūs varat [lejupielādēt](download-electronic-reporting-configuration-lcs.md) **ISO20022 kredīta pārvedumu** ER maksājuma formātu, kas ir pieejams no koplietojamo līdzekļu bibliotēkas Microsoft Dynamics Lifecycle Services (LCS) pakalpojumos vai no Globālās krātuves.</span><span class="sxs-lookup"><span data-stu-id="03da5-214">If you want to use an ER solution to generate an electronic payment file for a vendor payment that is processed, you can [download](download-electronic-reporting-configuration-lcs.md) the **ISO20022 Credit transfer** ER payment format that is available from the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) or from the Global repository.</span></span>

![ER maksājuma formātu importēšana lapā Konfigurācijas krātuve](./media/er-data-debugger-import-from-repo.png)

<span data-ttu-id="03da5-216">Papildus atlasītajam ER formātam sekojošajām [konfigurācijām](general-electronic-reporting.md#Configuration) ir jābūt automātiski importētām jūsu Microsoft Dynamics 365 Finance instancē kā daļai no **ISO20022 kredīta pārveduma** ER risinājuma:</span><span class="sxs-lookup"><span data-stu-id="03da5-216">In addition to the selected ER format, the following [configurations](general-electronic-reporting.md#Configuration) must be automatically imported into your Microsoft Dynamics 365 Finance instance as part of the **ISO20022 Credit transfer** ER solution:</span></span>

- <span data-ttu-id="03da5-217">**Maksājuma modelis** [ER datu modeļa konfigurācija](general-electronic-reporting.md#DataModelComponent)</span><span class="sxs-lookup"><span data-stu-id="03da5-217">**Payment model** [ER data model configuration](general-electronic-reporting.md#DataModelComponent)</span></span>
- <span data-ttu-id="03da5-218">**ISO20022 kredīta pārvedums** [ER formāta konfigurācija](general-electronic-reporting.md#FormatComponentOutbound)</span><span class="sxs-lookup"><span data-stu-id="03da5-218">**ISO20022 Credit transfer** [ER format configuration](general-electronic-reporting.md#FormatComponentOutbound)</span></span>
- <span data-ttu-id="03da5-219">**Maksājuma modeļa kartēšana 1611** [ER modeļa kartēšanas konfigurācija](general-electronic-reporting.md#ModelMappingComponent)</span><span class="sxs-lookup"><span data-stu-id="03da5-219">**Payment model mapping 1611** [ER model mapping configuration](general-electronic-reporting.md#ModelMappingComponent)</span></span>
- <span data-ttu-id="03da5-220">**Maksājumu modeļa kartēšana uz ISO20022 galapunktu** ER modeļa kartēšanas konfigurācija</span><span class="sxs-lookup"><span data-stu-id="03da5-220">**Payment model mapping to destination ISO20022** ER model mapping configuration</span></span>

<span data-ttu-id="03da5-221">Šīs konfigurācijas ir iespējams atrast ER struktūras lapā **Konfigurācijas** (**Organizācijas administrēšana** \> **Elektroniskā ziņošana** \> **Konfigurācijas**).</span><span class="sxs-lookup"><span data-stu-id="03da5-221">You can find these configurations on the **Configurations** page of the ER framework (**Organization administration** \> **Electronic reporting** \> **Configurations**).</span></span>

![Importētās konfigurācijas Konfigurāciju lapā](./media/er-data-debugger-configurations.png)

<span data-ttu-id="03da5-223">Ja konfigurācijas kokā trūkst kādas no iepriekš uzskaitītajām konfigurācijām, tās ir manuāli jālejupielādē no koplietojamā līdzekļa bibliotēkas tādā pašā veidā, kā lejupielādējat ER maksājuma formātu **ISO20022 kredīta pārvedums**.</span><span class="sxs-lookup"><span data-stu-id="03da5-223">If any of the previously listed configurations are missing in the configuration tree, you must manually download them from the LCS Shared asset library in the same way that you downloaded the **ISO20022 Credit transfer** ER payment format.</span></span>

### <a name="analyze-the-downloaded-er-solution"></a><span data-ttu-id="03da5-224">Analizēt lejupielādējamo ER risinājumu</span><span class="sxs-lookup"><span data-stu-id="03da5-224">Analyze the downloaded ER solution</span></span>

#### <a name="review-the-model-mapping"></a><span data-ttu-id="03da5-225">Pārskatīt modeļa kartēšanu</span><span class="sxs-lookup"><span data-stu-id="03da5-225">Review the model mapping</span></span>

1. <span data-ttu-id="03da5-226">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="03da5-226">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="03da5-227">Atlasiet **Maksājuma modelis** \> **Maksājuma modeļa kartēšana 1611**.</span><span class="sxs-lookup"><span data-stu-id="03da5-227">Select **Payment model** \> **Payment model mapping 1611**.</span></span>
3. <span data-ttu-id="03da5-228">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="03da5-228">Select **Designer**.</span></span>
4. <span data-ttu-id="03da5-229">Atlasiet **Maksājuma modeļa kartēšana ISO20022 CT** kartēšanas ierakstu.</span><span class="sxs-lookup"><span data-stu-id="03da5-229">Select the **Payment model mapping ISO20022 CT** mapping record.</span></span>
5. <span data-ttu-id="03da5-230">Atlasiet **Noformētāju** un pēc tam pārskatiet atvērto modeļa kartējumu.</span><span class="sxs-lookup"><span data-stu-id="03da5-230">Select **Designer**, and then review the model mapping that is opened.</span></span>

    <span data-ttu-id="03da5-231">Ievērojiet, ka datu modeļa **Maksājumu** lauks ir saistīts ar **\$notSentTransactions** datu avotu, kas atgriež to kreditoru maksājumu rindu sarakstu, kuras tiek apstrādātas.</span><span class="sxs-lookup"><span data-stu-id="03da5-231">Notice that the **Payments** field of the data model is bound to the **\$notSentTransactions** data source that returns the list of vendor payment lines that are being processed.</span></span>

    ![Maksājumu lauks Modeļa kartēšanas noformētāja lapā](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a><span data-ttu-id="03da5-233">Pārskatīt formāta kartēšanu</span><span class="sxs-lookup"><span data-stu-id="03da5-233">Review the format mapping</span></span>

1. <span data-ttu-id="03da5-234">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="03da5-234">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="03da5-235">Atlasiet **Maksājuma modelis** \> **ISO20022 kredīta pārvedums**.</span><span class="sxs-lookup"><span data-stu-id="03da5-235">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="03da5-236">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="03da5-236">Select **Designer**.</span></span>
4. <span data-ttu-id="03da5-237">Cilnē **Kartēšana** pārskatiet atvērto formāta kartēšanu.</span><span class="sxs-lookup"><span data-stu-id="03da5-237">On the **Mapping** tab, review the format mapping that is opened.</span></span>

    <span data-ttu-id="03da5-238">Ievērojiet, ka **Dokuments** \> **CstmrCdtTrfInitn** \> **PmtInf** elements failam **ISO20022CTReports** \> **XMLHeader** ir piesaistīts  **\$PaymentByDebtor** datu avotam, kas ir konfigurēts datu modeļa **Maksājumu** lauka ierakstu grupēšanai.</span><span class="sxs-lookup"><span data-stu-id="03da5-238">Notice that the **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** element of the **ISO20022CTReports** \> **XMLHeader** file is bound to the **\$PaymentByDebtor** data source that is configured to group records of the data model's **Payments** field.</span></span>

    ![PmtInf elements lapā Formāta veidotājs](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a><span data-ttu-id="03da5-240">Pārskatīt formātu</span><span class="sxs-lookup"><span data-stu-id="03da5-240">Review the format</span></span>

1. <span data-ttu-id="03da5-241">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="03da5-241">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="03da5-242">Atlasiet **Maksājuma modelis** \> **ISO20022 kredīta pārvedums**.</span><span class="sxs-lookup"><span data-stu-id="03da5-242">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="03da5-243">Atlasiet **Noformētāju** un pēc tam pārskatiet atvērto formātu.</span><span class="sxs-lookup"><span data-stu-id="03da5-243">Select **Designer**, and then review the format that is opened.</span></span>

    <span data-ttu-id="03da5-244">Ievērojiet, ka formāta elements sadaļā **Dokuments** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** ir konfigurēts, lai maksājuma failā ievadītu kreditora konta IBAN kodu.</span><span class="sxs-lookup"><span data-stu-id="03da5-244">Notice that the format element under **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** is configured to enter the IBAN code of the vendor account in the payment file.</span></span>

    ![BankIBAN elements lapā Formāta veidotājs](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a><span data-ttu-id="03da5-246">2.papildinājums: Konfigurēt kreditorus</span><span class="sxs-lookup"><span data-stu-id="03da5-246">Appendix 2: Configure Accounts payable</span></span>

### <a name="modify-a-vendor-property"></a><span data-ttu-id="03da5-247">Pārveidot kreditora rekvizītu</span><span class="sxs-lookup"><span data-stu-id="03da5-247">Modify a vendor property</span></span>

1. <span data-ttu-id="03da5-248">Dodieties uz **Kreditori** \> **Kreditori** \> **Visi kreditori**.</span><span class="sxs-lookup"><span data-stu-id="03da5-248">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="03da5-249">Atlasiet kreditoru **DE-01002** un pēc tam darbību rūts cilnē **Kreditors** grupā **Uzstādīt** atlasiet **Banku konti**.</span><span class="sxs-lookup"><span data-stu-id="03da5-249">Select vendor **DE-01002**, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="03da5-250">Kopsavilkuma cilnē **Identifikācija** laukā **IBAN** <a name="enteredIBANcode"></a>ievadiet **GB33 BUKB 2020 1555 5555 55**.</span><span class="sxs-lookup"><span data-stu-id="03da5-250">On the **Identification** FastTab, in the **IBAN** field, <a name="enteredIBANcode"></a>enter **GB33 BUKB 2020 1555 5555 55**.</span></span>
4. <span data-ttu-id="03da5-251">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="03da5-251">Select **Save**.</span></span>

![IBAN lauks uzstādīts lapā Kreditora bankas konti](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a><span data-ttu-id="03da5-253">Maksāšanas metodes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="03da5-253">Set up a method of payment</span></span>

1. <span data-ttu-id="03da5-254">Dodieties uz **Kreditori** \> **Maksājuma iestatīšana** \> **Maksājuma metodes**.</span><span class="sxs-lookup"><span data-stu-id="03da5-254">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="03da5-255">Atlasiet **SEPA CT** maksāšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="03da5-255">Select the **SEPA CT** payment method.</span></span>
3. <span data-ttu-id="03da5-256">Kopsavilkuma cilnē **Failu formāti** sadaļā **Failu formāti** iestatiet opciju **Vispārīgs elektroniskās eksportēšanas formāts** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="03da5-256">On the **File formats** FastTab, in the **File formats** section, set the **Generic electronic Export format** option to **Yes**.</span></span>
4. <span data-ttu-id="03da5-257">Laukā **Eksporta formāta konfigurācija** atlasiet **ISO20022 kredīta pārveduma** ER formātu.</span><span class="sxs-lookup"><span data-stu-id="03da5-257">In the **Export format configuration** field, select the **ISO20022 Credit transfer** ER format.</span></span>
5. <span data-ttu-id="03da5-258">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="03da5-258">Select **Save**.</span></span>

![Faila formāta iestatījumi lapā Maksājuma metodes](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a><span data-ttu-id="03da5-260">Kreditora maksājuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="03da5-260">Add a vendor payment</span></span>

1. <span data-ttu-id="03da5-261">Dodieties uz **Kreditori** \> **Maksājumi** \> **Kreditora maksājumu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="03da5-261">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="03da5-262">Pievienot jaunu maksājumu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="03da5-262">Add a new payment journal.</span></span>
3. <span data-ttu-id="03da5-263">Atlasiet **Rindas** un pievienojiet jaunu maksājuma rindu.</span><span class="sxs-lookup"><span data-stu-id="03da5-263">Select **Lines**, and add a new payment line.</span></span>
4. <span data-ttu-id="03da5-264">Laukā **Konts** atlasiet kreditoru **DE-01002**.</span><span class="sxs-lookup"><span data-stu-id="03da5-264">In the **Account** field, select vendor **DE-01002**.</span></span>
5. <span data-ttu-id="03da5-265">Laukā **Debets** ievadiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="03da5-265">In the **Debit** field, enter a value.</span></span>
6. <span data-ttu-id="03da5-266">Laukā **Maksājuma metode** atlasiet **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="03da5-266">In the **Method of payment** field, select **SEPA CT**.</span></span>
7. <span data-ttu-id="03da5-267">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="03da5-267">Select **Save**.</span></span>

![Kreditora maksājums ir pievienots lapā Kreditora maksājumi](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a><span data-ttu-id="03da5-269">3. papildinājums: Kreditora maksājumu apstrāde</span><span class="sxs-lookup"><span data-stu-id="03da5-269">Appendix 3: Process a vendor payment</span></span>

1. <span data-ttu-id="03da5-270">Dodieties uz **Kreditori** \> **Maksājumi** \> **Kreditora maksājumu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="03da5-270">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="03da5-271">Lapā **Kreditora maksājumu žurnāls** atlasiet iepriekš izveidoto maksājumu žurnālu un pēc tam atlasiet **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="03da5-271">On the **Vendor payment journal** page, select the payment journal that you previously created, and then select **Lines**.</span></span>
3. <span data-ttu-id="03da5-272">Atlasiet maksājuma rindu un pēc tam atlasiet **Maksājuma statuss** \> **Nav**.</span><span class="sxs-lookup"><span data-stu-id="03da5-272">Select the payment line, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="03da5-273">Atlasiet **Ģenerēt maksājumus**.</span><span class="sxs-lookup"><span data-stu-id="03da5-273">Select **Generate payments**.</span></span>
5. <span data-ttu-id="03da5-274">Laukā **Maksājuma metode** atlasiet **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="03da5-274">In the **Method of payment** field, select **SEPA CT**.</span></span>
6. <span data-ttu-id="03da5-275">Laukā **Bankas konts** atlasiet **DEMF OPER**.</span><span class="sxs-lookup"><span data-stu-id="03da5-275">In the **Bank account** field, select **DEMF OPER**.</span></span>
7. <span data-ttu-id="03da5-276">Dialoglodziņā **Ģenerēt maksājumus** atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="03da5-276">In the **Generate payments** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="03da5-277">Dialoglodziņā **Elektroniskā pārskata parametri** atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="03da5-277">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
