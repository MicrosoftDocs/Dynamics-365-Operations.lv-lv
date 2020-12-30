---
title: Uzlabot ER risinājumu veiktspēju, pievienojot parameterizētus APRĒĶINĀTO LAUKU datu avotus
description: Šajā tēmā ir paskaidrots, kā var palīdzēt uzlabot Elektronisko atskaišu (Electroinic reporting - ER) risinājumu veiktspēju, pievienojot parameterizētus APRĒĶINĀTO LAUKU datu avotus.
author: NickSelin
manager: AnnBe
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 940b696a06fb46bcd0557f059327cd4340448137
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681284"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a><span data-ttu-id="684ed-103">Uzlabot ER risinājumu veiktspēju, pievienojot parameterizētus APRĒĶINĀTO LAUKU datu avotus</span><span class="sxs-lookup"><span data-stu-id="684ed-103">Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="684ed-104">Šajā tēmā ir paskaidrots, kā var veikt [veiktspējas izsekošanu](trace-execution-er-troubleshoot-perf.md) attiecībā uz [Elektronisko atskaišu (ER)](general-electronic-reporting.md) formātiem, kas tiek palaisti, un tad izmantot šo izsekoto informāciju, lai palīdzētu uzlabot veiktspēju, konfigurējot parameterizētu **Aprēķinātā lauka** datu avotu.</span><span class="sxs-lookup"><span data-stu-id="684ed-104">This topic explains how you can take [performance traces](trace-execution-er-troubleshoot-perf.md) of [Electronic reporting (ER)](general-electronic-reporting.md) formats that are run, and then use the information from those traces to help improve performance by configuring a parameterized **Calculated field** data source.</span></span>

<span data-ttu-id="684ed-105">ER konfigurāciju izstrādes procesa ietvaros, lai izveidotu biznesa dokumentus, nosakiet metodi, kas tiek izmantota, lai iegūtu datus no programmas un ievadītu tos ģenerētajā izvadē.</span><span class="sxs-lookup"><span data-stu-id="684ed-105">As part of the process of designing ER configurations to generate business documents, you define the method that is used to retrieve data from the application and enter it in the generated output.</span></span> <span data-ttu-id="684ed-106">Izveidojot **Aprēķinātā lauka** veida parameterizētu ER datu avotu, varat samazināt datu bāzes izsaukumu skaitu un ievērojami samazināt laiku un izmaksas, kas ir saistītas ar ER formāta izpildes detaļu savākšanu.</span><span class="sxs-lookup"><span data-stu-id="684ed-106">By designing a parametrized ER data source of the **Calculated field** type, you can reduce the number of database calls, and significantly reduce the time and cost that are involved in collecting the details of ER format execution.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="684ed-107">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="684ed-107">Prerequisites</span></span>

- <span data-ttu-id="684ed-108">Lai izpildītu šīs tēmas piemērus, jums ir jābūt piekļuvei vienai no šādām [lomām](../sysadmin/tasks/assign-users-security-roles.md):</span><span class="sxs-lookup"><span data-stu-id="684ed-108">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="684ed-109">Elektroniskā pārskata izstrādātājs</span><span class="sxs-lookup"><span data-stu-id="684ed-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="684ed-110">Elektronisko pārskatu veidošanas funkcionālais konsultants</span><span class="sxs-lookup"><span data-stu-id="684ed-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="684ed-111">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="684ed-111">System administrator</span></span>

- <span data-ttu-id="684ed-112">Uzņēmumam jābūt iestatītam uz **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="684ed-112">The company must be set to **DEMF**.</span></span>
- <span data-ttu-id="684ed-113">Izpildiet šīs tēmas [1. papildinājumā](#appendix1) norādītās darbības, lai lejupielādētu parauga Microsoft ER risinājuma komponentus, kas nepieciešami, lai aizpildītu piemērus šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="684ed-113">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the sample Microsoft ER solution that is required to complete the examples in this topic.</span></span>
- <span data-ttu-id="684ed-114">Izpildiet šīs tēmas [2. papildinājumā](#appendix2) norādītās darbības, lai konfigurētu minimālu ER parametru kopumu, kas nepieciešams, lai izmantotu ER struktūru, lai palīdzētu uzlabot parauga Microsoft ER risinājuma veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="684ed-114">Follow the steps in [Appendix 2](#appendix2) of this topic to configure the minimal set of ER parameters that is required to use the ER framework to help improve the performance of the sample Microsoft ER solution.</span></span>

## <a name="import-the-sample-er-solution"></a><span data-ttu-id="684ed-115">Parauga ER risinājuma failu importēšana</span><span class="sxs-lookup"><span data-stu-id="684ed-115">Import the sample ER solution</span></span>

<span data-ttu-id="684ed-116">Iedomājieties, ka jums ir jāizstrādā ER risinājums, lai ģenerētu jaunu pārskatu, kurā parādītas kreditoru darbības.</span><span class="sxs-lookup"><span data-stu-id="684ed-116">Imagine that you must design an ER solution to generate a new report that shows vendor transactions.</span></span> <span data-ttu-id="684ed-117">Pašlaik varat atrast atlasītā kreditora transakcijas lapā **Kreditoru transakcijas** (pārejiet uz **Parādi kreditoriem** \> **Kreditori** \> **Visi kreditori**, atlasiet kreditoru un pēc tam darbību rūtī, cilnē **Kreditors**, grupā **Transakcijas** atlasiet vienumu **Transakcijas**).</span><span class="sxs-lookup"><span data-stu-id="684ed-117">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable** \> **Vendors** \> **All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="684ed-118">Tomēr ir nepieciešams, lai visas kreditoru transakcijas kopā būtu vienā elektroniskajā dokumentā XML formātā.</span><span class="sxs-lookup"><span data-stu-id="684ed-118">However, you want to have all vendor transactions together in one electronic document in XML format.</span></span> <span data-ttu-id="684ed-119">Šis risinājums sastāv no vairākām ER konfigurācijām, kas ietver nepieciešamo datu modeli, modeļa kartējumu un formāta komponentus.</span><span class="sxs-lookup"><span data-stu-id="684ed-119">This solution will consist of several ER configurations that contain the required data model, model mapping, and format components.</span></span>

<span data-ttu-id="684ed-120">Pirmais solis ir importēt parauga ER risinājumu, lai ģenerētu kreditora darbību pārskatu.</span><span class="sxs-lookup"><span data-stu-id="684ed-120">The first step is to import the sample ER solution to generate a vendor transactions report.</span></span>

1. <span data-ttu-id="684ed-121">Piesakieties Microsoft Dynamics 365 Finance instancē, kas nodrošināta jūsu uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="684ed-121">Sign in to the instance of Microsoft Dynamics 365 Finance that is provisioned for your company.</span></span>
2. <span data-ttu-id="684ed-122">Šajā tēmā jūs izveidosit un modificēsit nepieciešamās konfigurācijas parauga uzņēmumam **Litware, Inc.** .</span><span class="sxs-lookup"><span data-stu-id="684ed-122">In this topic, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="684ed-123">Pārliecinieties, ka šis konfigurācijas nodrošinātājs ir pievienots jūsu Finance instancei un atzīmēts kā aktīvs.</span><span class="sxs-lookup"><span data-stu-id="684ed-123">Make sure that this configuration provider has been added to your Finance instance and is marked as active.</span></span> <span data-ttu-id="684ed-124">Papildinformāciju skatiet [Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="684ed-124">For more information, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="684ed-125">Darbvietā **Elektroniskie pārskati** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="684ed-125">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="684ed-126">Lapā **Konfigurācijas** importējiet ER konfigurācijas, kuras lejupielādējāt kā priekšnosacījumu pakalpojumā Finance, šādā secībā: datu modelis, modeļa kartējums, formāts.</span><span class="sxs-lookup"><span data-stu-id="684ed-126">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into Finance, in the following order: data model, model mapping, format.</span></span> <span data-ttu-id="684ed-127">Katrai konfigurācijai rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="684ed-127">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="684ed-128">Darbību rūtī atlasiet **Mainīt** \> **Ielādēt no XML faila**.</span><span class="sxs-lookup"><span data-stu-id="684ed-128">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
    2. <span data-ttu-id="684ed-129">Atlasiet **Pārlūkot** un atlasiet atbilstošu failu ER konfigurācijai XML formātā.</span><span class="sxs-lookup"><span data-stu-id="684ed-129">Select **Browse**, and select the appropriate file for the ER configuration in XML format.</span></span>
    3. <span data-ttu-id="684ed-130">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="684ed-130">Select **OK**.</span></span>

![Importētās konfigurācijas Konfigurāciju lapā](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a><span data-ttu-id="684ed-132">Parauga ER risinājuma failu priekšskatījums</span><span class="sxs-lookup"><span data-stu-id="684ed-132">Review the sample ER solution</span></span>

### <a name="review-the-model-mapping"></a><span data-ttu-id="684ed-133">Pārskatīt modeļa kartēšanu</span><span class="sxs-lookup"><span data-stu-id="684ed-133">Review the model mapping</span></span>

1. <span data-ttu-id="684ed-134">Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Veiktspējas uzlabošanas modelis** un pēc tam atlasiet **Veiktspējas uzlabošanas kartēšana**.</span><span class="sxs-lookup"><span data-stu-id="684ed-134">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="684ed-135">Darbību rūtī atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="684ed-135">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="684ed-136">Lapā **Datu avota kartējuma modelis** darbību rūtī atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="684ed-136">On the **Model to datasource mapping** page, on the Action Pane, select **Designer**.</span></span>

    <span data-ttu-id="684ed-137">Šī ER modeļa kartēšana ir veidota, lai veiktu šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="684ed-137">This ER model mapping is designed to perform the following actions:</span></span>

    - <span data-ttu-id="684ed-138">Ielādēt tabulā VendTrans saglabāto kreditoru darbību sarakstu (**Trans** datu avots).</span><span class="sxs-lookup"><span data-stu-id="684ed-138">Fetch the list of vendor transactions that are stored in the VendTrans table (**Trans** data source).</span></span>
    - <span data-ttu-id="684ed-139">Katrai darbībai, ielādējiet no tabulas VendTable tā kreditora ierakstu, kuram ir grāmatota darbība (**\#Vend** datu avots).</span><span class="sxs-lookup"><span data-stu-id="684ed-139">For every transaction, fetch, from the VendTable table, the record of a vendor that the transaction has been posted for (**\#Vend** data source).</span></span>

    > [!NOTE]
    > <span data-ttu-id="684ed-140">Datu avots **\#Vend** ir konfigurēts, lai varētu ielādēt atbilstošo kreditora ierakstu, izmantojot esošo daudzkārtējo relāciju **\@.'\>Relācijas'.VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="684ed-140">The **\#Vend** data source is configured to fetch the corresponding vendor record by using the existing many-to-one relation **\@.'\>Relations'.VendTable\_AccountNum**.</span></span>

    <span data-ttu-id="684ed-141">Modeļa kartēšana šajā konfigurācijā implementē pamatdatu modeli jebkuram no šajā modelī kas ir izveidoti šim modelim un tiek palaisti risinājumā Finance.</span><span class="sxs-lookup"><span data-stu-id="684ed-141">The model mapping in this configuration implements the base data model for any ER formats that are created for this model and run in Finance.</span></span> <span data-ttu-id="684ed-142">Tādējādi **Trans** datu avotu saturs ir pakļauts ER formātiem, piemēram, abstraktiem **modelis** datu avotiem.</span><span class="sxs-lookup"><span data-stu-id="684ed-142">Therefore, the content of the **Trans** data source is exposed for ER formats such as abstract **model** data sources.</span></span>

    ![Trans datu avots Modeļu kartēšanas veidotāja lapā](media/er-calculated-field-ds-performance-mapping-1.png)

4. <span data-ttu-id="684ed-144">Aizveriet lapu **Modeļa kartējuma noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="684ed-144">Close the **Model mapping designer** page.</span></span>
5. <span data-ttu-id="684ed-145">Aizveriet lapu **Datu avota kartējuma modelis**.</span><span class="sxs-lookup"><span data-stu-id="684ed-145">Close the **Model to datasource mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="684ed-146">Pārskata formāts</span><span class="sxs-lookup"><span data-stu-id="684ed-146">Review format</span></span>

1. <span data-ttu-id="684ed-147">Lapā **Konfigurācijas**, konfigurācijas kokā izvērsiet **Veiktspējas uzlabošanas modelis** un pēc tam atlasiet **Veiktspējas uzlabošanas formats**.</span><span class="sxs-lookup"><span data-stu-id="684ed-147">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement format**.</span></span>
2. <span data-ttu-id="684ed-148">Darbību rūtī atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="684ed-148">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="684ed-149">Lapā **Formāta veidotājs** cilnē **Kartēšana** atlasiet **Izvērst/Sakļaut**.</span><span class="sxs-lookup"><span data-stu-id="684ed-149">On the **Format designer** page, on the **Mapping** tab, select **Expand/Collapse**.</span></span>
4. <span data-ttu-id="684ed-150">Izvērst elementus **Modelis**, **Dati** un **Transakcija** .</span><span class="sxs-lookup"><span data-stu-id="684ed-150">Expand the **Model**, **Data,** and **Transaction** items.</span></span>

    <span data-ttu-id="684ed-151">Šis ER formāts ir izveidots, lai ģenerētu kreditoru transakciju pārskatu XML formātā.</span><span class="sxs-lookup"><span data-stu-id="684ed-151">This ER format is designed to generate a vendor transactions report in XML format.</span></span>

    ![Formātu datu avoti un konfigurētie formāta elementu saistījumi Formāta veidotāja lapā](media/er-calculated-field-ds-performance-format.png)

5. <span data-ttu-id="684ed-153">Aizveriet lapu **Formāta veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="684ed-153">Close the **Format designer** page.</span></span>

## <a name="run-the-sample-er-solution-to-trace-execution"></a><span data-ttu-id="684ed-154">Parauga ER risinājuma palaišana, lai izsekotu izpildi</span><span class="sxs-lookup"><span data-stu-id="684ed-154">Run the sample ER solution to trace execution</span></span>

<span data-ttu-id="684ed-155">Iedomājieties, ka esat pabeidzis izstrādāt ER risinājuma pirmo versiju.</span><span class="sxs-lookup"><span data-stu-id="684ed-155">Imagine that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="684ed-156">Tagad vēlaties pārbaudīt risinājumu savā FInance instancē un analizēt izpildes veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="684ed-156">You now want to test the solution in your Finance instance and analyze the execution performance.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="684ed-157">ER veiktspējas izsekošanas ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="684ed-157">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="684ed-158">Atlasiet **DEMF** uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="684ed-158">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="684ed-159">Izpildiet darbības, kas aprakstītas [Ieslēgt ER veiktspējas izsekošanu](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) , lai izveidotu veiktspējas izsekošanu, kamēr tiek palaists ER formāts.</span><span class="sxs-lookup"><span data-stu-id="684ed-159">Follow the steps in [Turn on the ER performance trace](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) to generate a performance trace while an ER format is run.</span></span>

    ![Lietotāja parametru dialoglodziņš](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a><span data-ttu-id="684ed-161">ER formāta palaišana</span><span class="sxs-lookup"><span data-stu-id="684ed-161">Run the ER format</span></span>

1. <span data-ttu-id="684ed-162">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="684ed-162">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="684ed-163">Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Veiktspējas uzlabošanas formāts**.</span><span class="sxs-lookup"><span data-stu-id="684ed-163">On the **Configurations** page, in the configuration tree, select **Performance improvement format**.</span></span>
3. <span data-ttu-id="684ed-164">Darbību rūtī atlasiet **Palaist**.</span><span class="sxs-lookup"><span data-stu-id="684ed-164">On the Action Pane, select **Run**.</span></span>

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a><span data-ttu-id="684ed-165">Izmantot veiktspējas izsekošanu, lai analizētu modeļa kartēšanas veiktspēju</span><span class="sxs-lookup"><span data-stu-id="684ed-165">Use the performance trace to analyze model mapping performance</span></span>

1. <span data-ttu-id="684ed-166">Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Veiktspējas uzlabošanas kartēšana**.</span><span class="sxs-lookup"><span data-stu-id="684ed-166">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="684ed-167">Darbību rūtī atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="684ed-167">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="684ed-168">Lapā **Modeļa kartēšana** darbību rūtī atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="684ed-168">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="684ed-169">Lapā **Modeļa kartējuma noformētājs**, darbību rūtī atlasiet **Veiktspējas izsekošana**.</span><span class="sxs-lookup"><span data-stu-id="684ed-169">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="684ed-170">Atlasiet pēdējo ģenerēto izsekošanu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="684ed-170">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="684ed-171">Tagad ir pieejama jauna informācija par dažiem pašreizējā modeļa kartējuma datu avota vienumiem:</span><span class="sxs-lookup"><span data-stu-id="684ed-171">New information is now available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="684ed-172">Faktiskais laiks, kas patērēts, iegūstot datus, izmantojot datu avotu</span><span class="sxs-lookup"><span data-stu-id="684ed-172">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="684ed-173">Tas pats laiks, kas izteikts procentos no kopējā laika, kurš patērēts, palaižot visu modeļa kartējumu</span><span class="sxs-lookup"><span data-stu-id="684ed-173">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

![Izpildes laika informācija Modeļa kartēšanas veidotāja lapā](./media/er-calculated-field-ds-performance-mapping-2.png)

<span data-ttu-id="684ed-175">Režģis **Veiktspējas statistika** rāda, ka **Trans** datu avots izsauc VendTrans tabulu vienu reizi.</span><span class="sxs-lookup"><span data-stu-id="684ed-175">The **Performance statistics** grid shows that the **Trans** data source calls the VendTrans table one time.</span></span> <span data-ttu-id="684ed-176">Vērtība **\[265\]\[Q:265\]** no **Trans** datu avota norāda, ka 265 kreditoru darbības ir paņemtas no programmas tabulas un atgrieztas datu modelī.</span><span class="sxs-lookup"><span data-stu-id="684ed-176">The value **\[265\]\[Q:265\]** of the **Trans** data source indicates that 265 vendor transactions have been fetched from the application table and returned to the data model.</span></span>

<span data-ttu-id="684ed-177">Režģis **Veiktspējas statistika** arī rāda, ka pašreizējā modeļa kartēšana dublē datu bāzes pieprasījumus, kamēr tiek palaists **\#Vend** datu avots.</span><span class="sxs-lookup"><span data-stu-id="684ed-177">The **Performance statistics** grid also shows that the current model mapping duplicates database requests while the **\#Vend** data source is run.</span></span> <span data-ttu-id="684ed-178">Šī dublēšana notiek tālāk norādīto iemeslu dēļ.</span><span class="sxs-lookup"><span data-stu-id="684ed-178">This duplication occurs for the following reasons:</span></span>

- <span data-ttu-id="684ed-179">Kreditoru tabula tiek izsaukta divas reizes katrai no 265 atkārtotajām kreditora transakcijam, kopā 530 izsaukumi:</span><span class="sxs-lookup"><span data-stu-id="684ed-179">The vendor table is called two times for each of the 265 iterated vendor transactions, for a total of 530 calls:</span></span>

    - <span data-ttu-id="684ed-180">Viens izsaukums tiek veikts, lai ievadītu kreditora konta numuru.</span><span class="sxs-lookup"><span data-stu-id="684ed-180">One call is made to enter the vendor account number.</span></span>
    - <span data-ttu-id="684ed-181">Viens izsaukums tiek veikts, lai ievadītu kreditora vārdu.</span><span class="sxs-lookup"><span data-stu-id="684ed-181">One call is made to enter the vendor name.</span></span>

- <span data-ttu-id="684ed-182">Kreditoru tabula tiek izsaukta katrai no atkārtotajām kreditora transakcijam, pat ja iesniegtās transakcijas ir grāmatotas tikai pieciem kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="684ed-182">The vendor table is called for each iterated vendor transaction, even though the fetched transactions have been posted for only five vendors.</span></span> <span data-ttu-id="684ed-183">No 530 izsaukumiem 525 ir dublikāti.</span><span class="sxs-lookup"><span data-stu-id="684ed-183">Of the 530 calls, 525 are duplicates.</span></span> <span data-ttu-id="684ed-184">Sekojošajā attēlā parādīts ziņojums, ko saņemat par dubultajiem izsaukumiem (datu bāzes pieprasījumi).</span><span class="sxs-lookup"><span data-stu-id="684ed-184">The following illustration shows the message that you receive about duplicate calls (database requests).</span></span>

![Ziņojums par datu bāzes pieprasījumu dublikātiem lapā Modeļa kartējuma noformētājs](./media/er-calculated-field-ds-performance-mapping-2a.png)

<span data-ttu-id="684ed-186">Ievērojiet, ka no kopējā modeļa kartēšanas izpildes laika (aptuveni astoņas sekundes) vairāk nekā 80 procenti (aptuveni sešas sekundes) ir izlietoti, izgūstot vērtības no VendTable pieteikumu tabulas.</span><span class="sxs-lookup"><span data-stu-id="684ed-186">Of the total model mapping execution time (approximately eight seconds), notice that more than 80 percent (approximately six seconds) has been spent retrieving values from the VendTable application table.</span></span> <span data-ttu-id="684ed-187">Šis procentuālais daudzums ir pārāk liels diviem piecu kreditoru atribūtiem, salīdzinot ar informācijas apjomu no VendTrans pieteikumu tabulas.</span><span class="sxs-lookup"><span data-stu-id="684ed-187">That percentage is too large for two attributes of five vendors, compared with the volume of information from the VendTrans application table.</span></span>

<span data-ttu-id="684ed-188">Lai samazinātu to izsaukumu skaitu, kas ir veikti, lai iegūtu detalizētu informāciju par katru transakciju, un lai uzlabotu modeļa kartēšanas veiktspēju, varat izmantot kešošanu **\#Vend** datu avotam.</span><span class="sxs-lookup"><span data-stu-id="684ed-188">To reduce the number of calls that are made to get the vendor details for every transaction, and to improve the performance of the model mapping, you can use caching for the **\#Vend** data source.</span></span>

> [!NOTE]
> <span data-ttu-id="684ed-189">Datu avots **Trans\\\#Vend** tiks kešots pašreizējās **Trans** datu avota transakcijas darbības sfēras izpildlaikā.</span><span class="sxs-lookup"><span data-stu-id="684ed-189">The **Trans\\\#Vend** data source will be cached in the scope of the current transaction of the **Trans** data source at runtime.</span></span>

<span data-ttu-id="684ed-190">Kad tiek kešots **\#Vend** datu avots, dublēto izsaukumu skaits tiek samazināts no 525 uz 260, bet dublēšana netiek pilnībā likvidēta.</span><span class="sxs-lookup"><span data-stu-id="684ed-190">By caching the **\#Vend** data source, you reduce the number of duplicated calls from 525 to 260, but you don't completely eliminate the duplication.</span></span> <span data-ttu-id="684ed-191">Lai pilnībā izvairītos no dublēšanās, varat konfigurēt jaunu parameterizētu datu avotu veidam **Aprēķinātais lauks** .</span><span class="sxs-lookup"><span data-stu-id="684ed-191">To completely eliminate duplication, you can configure a new parameterized data source of the **Calculated field** type.</span></span>

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="684ed-192">Modeļa kartējuma uzlabošana, pamatojoties uz informāciju no izpildes izsekošanas</span><span class="sxs-lookup"><span data-stu-id="684ed-192">Improve the model mapping based on information from the execution trace</span></span>

### <a name="change-the-logic-of-the-model-mapping"></a><span data-ttu-id="684ed-193">Modeļa kartējuma loģikas mainīšana</span><span class="sxs-lookup"><span data-stu-id="684ed-193">Change the logic of the model mapping</span></span>

<span data-ttu-id="684ed-194">Veiciet šīs darbības, lai izmantotu kešatmiņu un **Aprēķinātais lauks** veida datu avotu , lai palīdzētu novērst dubultus izsaukumus uz datu bāzi.</span><span class="sxs-lookup"><span data-stu-id="684ed-194">Follow these steps to use caching and a data source of the **Calculated field** type, to help prevent duplicate calls to the database.</span></span>

1. <span data-ttu-id="684ed-195">Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Veiktspējas uzlabošanas kartēšana**.</span><span class="sxs-lookup"><span data-stu-id="684ed-195">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="684ed-196">Darbību rūtī atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="684ed-196">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="684ed-197">Lapā **Modeļa kartēšana** darbību rūtī atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="684ed-197">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="684ed-198">Lapā **Modeļa kartēšanas veidotājs** veiciet tālāk norādītās darbības, lai pievienotu datu avotu veidam **Tabulas ieraksts** , lai piekļūtu ierakstiem VendTable pieteikumu tabulā:</span><span class="sxs-lookup"><span data-stu-id="684ed-198">On the **Model mapping designer** page, follow these steps to add a data source of the **Table records** type to access records in the VendTable application table:</span></span>

    1. <span data-ttu-id="684ed-199">Rūtī **Datu avota veidi** izvērsiet **Dynamics 365 for Operations** un atlasiet **Tabulas ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="684ed-199">In the **Data source types** pane, expand **Dynamics 365 for Operations**, and select **Table records**.</span></span>
    2. <span data-ttu-id="684ed-200">Atlasiet **Pievienot sakni**.</span><span class="sxs-lookup"><span data-stu-id="684ed-200">Select **Add root**.</span></span>
    3. <span data-ttu-id="684ed-201">Dialoglodziņa laukā **Nosaukums** ievadiet **Vend**.</span><span class="sxs-lookup"><span data-stu-id="684ed-201">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    4. <span data-ttu-id="684ed-202">Laukā **Tabula** ievadiet **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="684ed-202">In the **Table** field, enter **VendTable**.</span></span>
    5. <span data-ttu-id="684ed-203">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="684ed-203">Select **OK**.</span></span>

5. <span data-ttu-id="684ed-204">Varat parameterizēt izsaukumus uz **Aprēķinātais lauks** veidu datu avotiem tikai tad, ja šie datu avoti atrodas konteinerā.</span><span class="sxs-lookup"><span data-stu-id="684ed-204">You can parameterize calls to data sources of the **Calculated field** type only if those data sources reside in a container.</span></span> <span data-ttu-id="684ed-205">Tāpēc veiciet šīs darbības, lai pievienotu **Tukšs konteineris** veida datu avotu, lai uzglabātu jaunu **Aprēķinātais lauks** veida parameterizētu datu avotu:</span><span class="sxs-lookup"><span data-stu-id="684ed-205">Therefore, follow these steps to add a data source of the **Empty container** type to hold a new parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="684ed-206">Rūtī **Datu avota veidi** izvērsiet **Vispārīgi** un atlasiet **Tukšs konteineris**.</span><span class="sxs-lookup"><span data-stu-id="684ed-206">In the **Data source types** pane, expand **General**, and select **Empty container**.</span></span>
    2. <span data-ttu-id="684ed-207">Atlasiet **Pievienot sakni**.</span><span class="sxs-lookup"><span data-stu-id="684ed-207">Select **Add root**.</span></span>
    3. <span data-ttu-id="684ed-208">Dialoglodziņa laukā **Nosaukums** ievadiet **Box**.</span><span class="sxs-lookup"><span data-stu-id="684ed-208">In the dialog box, in the **Name** field, enter **Box**.</span></span>
    3. <span data-ttu-id="684ed-209">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="684ed-209">Select **OK**.</span></span>

    ![Lodziņa datu avots Modeļu kartēšanas veidotāja lapā](./media/er-calculated-field-ds-performance-mapping-3.png)

6. <span data-ttu-id="684ed-211">Veiciet šīs darbības, lai pievienotu **Aprēķinātais lauks** veida parameterizētu datu avotu:</span><span class="sxs-lookup"><span data-stu-id="684ed-211">Follow these steps to add a parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="684ed-212">Rūtī **Datu avoti** atlasiet **Box**.</span><span class="sxs-lookup"><span data-stu-id="684ed-212">In the **Data sources** pane, select **Box**.</span></span>
    2. <span data-ttu-id="684ed-213">Rūtī **Datu avota veidi** izvērsiet **Funkcijas** un atlasiet **Aprēķinātais lauks**.</span><span class="sxs-lookup"><span data-stu-id="684ed-213">In the **Data source types** pane, expand **Functions**, and select **Calculated field**.</span></span>
    3. <span data-ttu-id="684ed-214">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="684ed-214">Select **Add**.</span></span>
    4. <span data-ttu-id="684ed-215">Dialoglodziņa laukā **Nosaukums** ievadiet **Vend**.</span><span class="sxs-lookup"><span data-stu-id="684ed-215">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    5. <span data-ttu-id="684ed-216">Atlasiet **Rediģēt formulu**.</span><span class="sxs-lookup"><span data-stu-id="684ed-216">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="684ed-217">Lapā **Formulas veidotājs** atlasiet **Parametri** , lai norādītu parametrus, kas ir jāsniedz, kad tiek izsaukts šis datu avots.</span><span class="sxs-lookup"><span data-stu-id="684ed-217">On the **Formula designer** page, select **Parameters** to specify the parameters that must be provided when this data source is called.</span></span>
    7. <span data-ttu-id="684ed-218">Dialoglodziņā **Parametri** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="684ed-218">In the **Parameters** dialog box, select **New**.</span></span>
    8. <span data-ttu-id="684ed-219">Laukā **Nosaukums** ievadiet **parmVendAccNumber**.</span><span class="sxs-lookup"><span data-stu-id="684ed-219">In the **Name** field, enter **parmVendAccNumber**.</span></span>
    9. <span data-ttu-id="684ed-220">Laukā **Tips** atlasiet **Virkne**.</span><span class="sxs-lookup"><span data-stu-id="684ed-220">In the **Type** field, select **String**.</span></span>
    10. <span data-ttu-id="684ed-221">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="684ed-221">Select **OK**.</span></span>
    11. <span data-ttu-id="684ed-222">Laukā **Formula** ievadiet **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span><span class="sxs-lookup"><span data-stu-id="684ed-222">In the **Formula** field, enter **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span></span>
    12. <span data-ttu-id="684ed-223">Atlasiet **Saglabāt** un aizvēriet lapu **Formulas veidotājs** .</span><span class="sxs-lookup"><span data-stu-id="684ed-223">Select **Save**, and close the **Formula designer** page.</span></span>
    13. <span data-ttu-id="684ed-224">Atlasiet **Labi**, lai pievienotu jaunu datu avotu.</span><span class="sxs-lookup"><span data-stu-id="684ed-224">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="684ed-225">Veiciet šīs darbības, lai iezīmētu pievienoto datu avotu kā kešoto izpildes laikā:</span><span class="sxs-lookup"><span data-stu-id="684ed-225">Follow these steps to mark the added data source as cached during the execution:</span></span>

    1. <span data-ttu-id="684ed-226">Rūtī **Datu avoti** atlasiet **Box\\Vend**.</span><span class="sxs-lookup"><span data-stu-id="684ed-226">In the **Data sources** pane, select **Box\\Vend**.</span></span>
    2. <span data-ttu-id="684ed-227">Atlasiet **Kešatmiņa**.</span><span class="sxs-lookup"><span data-stu-id="684ed-227">Select **Cache**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="684ed-228">Datu avots **Box\\Vend** tiks kešots visās **Trans** datu avota transakcijas darbības sfēras izpildlaikā.</span><span class="sxs-lookup"><span data-stu-id="684ed-228">The **Box\\Vend** data source will be cached in the scope of all vendor transactions of the **Trans** data source at runtime.</span></span>

8. <span data-ttu-id="684ed-229">Veiciet šīs darbības, lai atjauninātu ligzdoto **Trans\\\#Vend** datu avotu, lai tas izmantotu **Box\\Vend** datu avotu:</span><span class="sxs-lookup"><span data-stu-id="684ed-229">Follow these steps to update the nested **Trans\\\#Vend** data source so that it uses the **Box\\Vend** data source:</span></span>

    1. <span data-ttu-id="684ed-230">Rūtī **Datu avoti** izvērsiet **Trans**.</span><span class="sxs-lookup"><span data-stu-id="684ed-230">In the **Data sources** pane, expand **Trans**.</span></span>
    2. <span data-ttu-id="684ed-231">Atlasiet **Trans\\\#Vend** datu avotu un pēc tam atlasiet **Rediģēt** \> **Rediģēt formulu**.</span><span class="sxs-lookup"><span data-stu-id="684ed-231">Select the **Trans\\\#Vend** data source, and then select **Edit** \> **Edit formula**.</span></span>
    3. <span data-ttu-id="684ed-232">Lapā **Formulas veidotājs** laukā **Formula** ievadiet **Box.Vend(\@.AccountNum)**.</span><span class="sxs-lookup"><span data-stu-id="684ed-232">On the **Formula designer** page, in the **Formula** field, enter **Box.Vend(\@.AccountNum)**.</span></span>
    4. <span data-ttu-id="684ed-233">Atlasiet **Saglabāt** un pēc tam aizvēriet lapu **Formulas veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="684ed-233">Select **Save**, and then close the **Formula designer** page.</span></span>
    5. <span data-ttu-id="684ed-234">Atlasiet **Labi** , lai pabeigtu izmaiņas atlasītajā datu avotā.</span><span class="sxs-lookup"><span data-stu-id="684ed-234">Select **OK** to complete your changes to the selected data source.</span></span>

9. <span data-ttu-id="684ed-235">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="684ed-235">Select **Save**.</span></span>

    ![Vend datu avots Modeļu kartēšanas veidotāja lapā](./media/er-calculated-field-ds-performance-mapping-4.png)

10. <span data-ttu-id="684ed-237">Aizveriet lapu **Modeļa kartējuma noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="684ed-237">Close the **Model mapping designer** page.</span></span>
11. <span data-ttu-id="684ed-238">Aizveriet lapu **Modeļa kartējumi**.</span><span class="sxs-lookup"><span data-stu-id="684ed-238">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="684ed-239">ER modeļa kartējuma modificētās versijas pabeigšana</span><span class="sxs-lookup"><span data-stu-id="684ed-239">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="684ed-240">Lapā **Konfigurācijas**, kopsavilkuma cilnē **Versijas** atlasiet konfigurācijas **Veiktspējas uzlabošanas kartējums** versiju **1.2.**.</span><span class="sxs-lookup"><span data-stu-id="684ed-240">On the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance improvement mapping** configuration.</span></span>
2. <span data-ttu-id="684ed-241">Atlasiet **Mainīt statusu** \> **Pabeigt**, un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="684ed-241">Select **Change status** \> **Complete**, and then select **OK**.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="684ed-242">Modificētā ER risinājuma palaišana, lai izsekotu izpildi</span><span class="sxs-lookup"><span data-stu-id="684ed-242">Run the modified ER solution to trace execution</span></span>

<span data-ttu-id="684ed-243">Atkārtojiet šīs tēmas iepriekšējā sadaļā [ER formāta palaišana](#run-format) minētās darbības, lai ģenerētu jaunu veiktspējas izsekošanu.</span><span class="sxs-lookup"><span data-stu-id="684ed-243">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a><span data-ttu-id="684ed-244">Izmantot veiktspējas izsekošanu, lai analizētu modeļa kartēšanas pielāgojumus</span><span class="sxs-lookup"><span data-stu-id="684ed-244">Use the performance trace to analyze adjustments to the model mapping</span></span> 

1. <span data-ttu-id="684ed-245">Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Veiktspējas uzlabošanas kartēšana**.</span><span class="sxs-lookup"><span data-stu-id="684ed-245">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="684ed-246">Darbību rūtī atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="684ed-246">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="684ed-247">Lapā **Modeļa kartēšana** darbību rūtī atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="684ed-247">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="684ed-248">Lapā **Modeļa kartējuma noformētājs**, darbību rūtī atlasiet **Veiktspējas izsekošana**.</span><span class="sxs-lookup"><span data-stu-id="684ed-248">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="684ed-249">Atlasiet pēdējo ģenerēto izsekošanu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="684ed-249">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="684ed-250">Ņemiet vērā, ka korekcijas, kuras veicāt modeļa kartējumam, likvidēja datu bāzes vaicājumu dublikātus.</span><span class="sxs-lookup"><span data-stu-id="684ed-250">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="684ed-251">Datu bāzu tabulu un datu avotu izsaukumu skaits šim modeļa kartējumam arī ir samazināts.</span><span class="sxs-lookup"><span data-stu-id="684ed-251">The number of calls to database tables and data sources for this model mapping has also been reduced.</span></span>

![Izsekošanas informācija Modeļu kartēšanas veidotāja lapā 1](./media/er-calculated-field-ds-performance-mapping-5.png)

<span data-ttu-id="684ed-253">Kopējais izpildes laiks ir samazināts aptuveni 20 reizes (no aptuveni 8 sekundēm līdz aptuveni 400 milisekundēm).</span><span class="sxs-lookup"><span data-stu-id="684ed-253">The total execution time has been reduced about 20 times (from about 8 seconds to about 400 milliseconds).</span></span> <span data-ttu-id="684ed-254">Tādēļ tika uzlabota ER risinājuma kopējā veiktspēja.</span><span class="sxs-lookup"><span data-stu-id="684ed-254">Therefore, the performance of the whole ER solution has been improved.</span></span>

![Izsekošanas informācija Modeļu kartēšanas veidotāja lapā 2](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a><span data-ttu-id="684ed-256">1. papildinājums: lejupielādēt parauga Microsoft ER risinājuma komponentus</span><span class="sxs-lookup"><span data-stu-id="684ed-256">Appendix 1: Download the components of the sample Microsoft ER solution</span></span>

<span data-ttu-id="684ed-257">Nepieciešams lejupielādēt tālāk norādītos failus un saglabāt tos lokāli.</span><span class="sxs-lookup"><span data-stu-id="684ed-257">You must download the following files and store them locally.</span></span>

| <span data-ttu-id="684ed-258">Fails</span><span class="sxs-lookup"><span data-stu-id="684ed-258">File</span></span>                                        | <span data-ttu-id="684ed-259">Saturs</span><span class="sxs-lookup"><span data-stu-id="684ed-259">Content</span></span> |
|---------------------------------------------|---------|
| <span data-ttu-id="684ed-260">Veiktspējas uzlabošanas modelis.versija.1</span><span class="sxs-lookup"><span data-stu-id="684ed-260">Performance improvement model.version.1</span></span>     | [<span data-ttu-id="684ed-261">Parauga ER datu modeļa konfigurācija</span><span class="sxs-lookup"><span data-stu-id="684ed-261">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="684ed-262">Veiktspējas uzlabošanas kartējums.versija.1.1</span><span class="sxs-lookup"><span data-stu-id="684ed-262">Performance improvement mapping.version.1.1</span></span> | [<span data-ttu-id="684ed-263">Parauga ER modeļa kartējuma konfigurācija</span><span class="sxs-lookup"><span data-stu-id="684ed-263">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="684ed-264">Veiktspējas uzlabošanas formats.versija.1.1</span><span class="sxs-lookup"><span data-stu-id="684ed-264">Performance improvement format.version.1.1</span></span>  | [<span data-ttu-id="684ed-265">Parauga ER formāta konfigurācija</span><span class="sxs-lookup"><span data-stu-id="684ed-265">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a><span data-ttu-id="684ed-266">2. papildinājums: ER struktūras konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="684ed-266">Appendix 2: Configure the ER framework</span></span>

<span data-ttu-id="684ed-267">Pirms sākat lietot ER struktūru, lai uzlabotu parauga Microsoft ER risinājuma veiktspēju, ir jākonfigurē minimāls ER parametru kopums.</span><span class="sxs-lookup"><span data-stu-id="684ed-267">Before you can start to use the ER framework to improve the performance of the sample Microsoft ER solution, you must configure the minimal set of ER parameters.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="684ed-268">Konfigurējiet ER parametrus</span><span class="sxs-lookup"><span data-stu-id="684ed-268">Configure ER parameters</span></span>

1. <span data-ttu-id="684ed-269">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="684ed-269">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="684ed-270">Lapas **Lokalizācijas konfigurācijas** sadaļā **Saistītās saites** atlasiet **Elektronisko pārskatu veidošanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="684ed-270">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="684ed-271">Lapas **Elektronisko pārskatu veidošanas parametri** cilnē **Vispārīgi** iestatiet opciju **Iespējot noformēšanas režīmu** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="684ed-271">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="684ed-272">Cilnē **Pielikumi** iestatiet šādus parametrus:</span><span class="sxs-lookup"><span data-stu-id="684ed-272">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="684ed-273">Laukā **Konfigurācijas** atlasiet veidu **Fails** uzņēmumam **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="684ed-273">In the **Configurations** field, select the **File** type for the **DEMF** company.</span></span>
    - <span data-ttu-id="684ed-274">Laukos **Darbu arhīvs**, **Pagaidu**, **Bāzlīnija** un **Citi** atlasiet veidu **Fails**.</span><span class="sxs-lookup"><span data-stu-id="684ed-274">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="684ed-275">Papildinformāciju par ER parametriem skatiet sadaļā [ER struktūras konfigurēšana](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="684ed-275">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="684ed-276">ER konfigurācijas nodrošinātāja aktivizēšana</span><span class="sxs-lookup"><span data-stu-id="684ed-276">Activate an ER configuration provider</span></span>

<span data-ttu-id="684ed-277">Katra pievienotā ER konfigurācija tiek atzīmēta kā piederoša ER konfigurācijas nodrošinātājam.</span><span class="sxs-lookup"><span data-stu-id="684ed-277">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="684ed-278">Šim nolūkam tiek izmantots ER konfigurācijas nodrošinātājs, kas ir aktivizēts **Elektroniskie pārskati** darbvietā.</span><span class="sxs-lookup"><span data-stu-id="684ed-278">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="684ed-279">Tāpēc, pirms sākat pievienot vai rediģēt ER konfigurācijas, jums ir jāaktivizē ER konfigurācijas nodrošinātājs **Elektroniskie pārskati** darbvietā.</span><span class="sxs-lookup"><span data-stu-id="684ed-279">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="684ed-280">Tikai ER konfigurācijas īpašnieks var rediģēt konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="684ed-280">Only the owner of an ER configuration can edit the configuration.</span></span> <span data-ttu-id="684ed-281">Tāpēc, pirms ER konfigurācija var tikt rediģēta, darbvietā **Elektroniskie pārskati** ir jāaktivizē atbilstošais ER konfigurācijas nodrošinātājs.</span><span class="sxs-lookup"><span data-stu-id="684ed-281">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="684ed-282">ER konfigurācijas nodrošinātāju saraksta pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="684ed-282">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="684ed-283">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="684ed-283">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="684ed-284">Lapas **Lokalizācijas konfigurācijas** sadaļā **Saistītās saites** atlasiet **Konfigurācijas nodrošinātāji**.</span><span class="sxs-lookup"><span data-stu-id="684ed-284">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="684ed-285">Lapā **Konfigurācijas nodrošinātāju tabula** katram nodrošinātāja ierakstam ir unikāls nosaukums un URL.</span><span class="sxs-lookup"><span data-stu-id="684ed-285">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="684ed-286">Pārskatiet šīs lapas saturu.</span><span class="sxs-lookup"><span data-stu-id="684ed-286">Review the contents of this page.</span></span> <span data-ttu-id="684ed-287">Ja ieraksts **Litware, Inc.** jau pastāv, izlaidiet nākamo procedūru, [Jauna ER konfigurācijas nodrošinātāja pievienošana](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="684ed-287">If a record for **Litware, Inc.** already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="684ed-288">Jauna ER konfigurācijas nodrošinātāja pievienošana</span><span class="sxs-lookup"><span data-stu-id="684ed-288">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="684ed-289">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="684ed-289">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="684ed-290">Lapas **Lokalizācijas konfigurācijas** sadaļā **Saistītās saites** atlasiet **Konfigurācijas nodrošinātāji**.</span><span class="sxs-lookup"><span data-stu-id="684ed-290">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="684ed-291">Lapā **Konfigurācijas nodrošinātāji** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="684ed-291">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="684ed-292">Laukā **Nosaukums** ievadiet **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="684ed-292">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="684ed-293">Laukā **Interneta adrese** ievadiet `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="684ed-293">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="684ed-294">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="684ed-294">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="684ed-295">ER konfigurācijas nodrošinātāja aktivizēšana</span><span class="sxs-lookup"><span data-stu-id="684ed-295">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="684ed-296">Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="684ed-296">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="684ed-297">Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Litware, Inc.** un pēc tam atlasiet **Iestatīt kā aktīvu**.</span><span class="sxs-lookup"><span data-stu-id="684ed-297">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="684ed-298">Papildinformāciju par ER konfigurācijas nodrošinātājiem skatiet sadaļā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="684ed-298">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="684ed-299">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="684ed-299">Additional resources</span></span>

- [<span data-ttu-id="684ed-300">Elektronisko pārskatu veidošanas apskats</span><span class="sxs-lookup"><span data-stu-id="684ed-300">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="684ed-301">Elektronisko atskaišu veidošanas (ER) formāta failu izpildes uzraudzīšana, lai novērstu veiktspējas problēmas</span><span class="sxs-lookup"><span data-stu-id="684ed-301">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)
- [<span data-ttu-id="684ed-302">Atbalsta Aprēķināto lauka tipa ER datu avotu parametru izsaukumus.</span><span class="sxs-lookup"><span data-stu-id="684ed-302">Support parameterized calls of ER data sources of the Calculated field type</span></span>](er-calculated-field-type.md)
