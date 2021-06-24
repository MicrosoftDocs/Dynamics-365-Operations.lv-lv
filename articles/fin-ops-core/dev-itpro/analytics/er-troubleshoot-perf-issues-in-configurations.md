---
title: Veiktspējas problēmu novēršana ER konfigurācijās
description: Šajā tēmā skaidrots, kā atrast un labot veiktspējas problēmas Elektronisko pārskatu (ER) konfigurācijās.
author: NickSelin
ms.date: 06/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: d77c2aad904ba911ac19009d6a981ea4153aaa48
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216869"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a><span data-ttu-id="f145c-103">Veiktspējas problēmu novēršana ER konfigurācijās</span><span class="sxs-lookup"><span data-stu-id="f145c-103">Troubleshooting performance issues in ER configurations</span></span>

<span data-ttu-id="f145c-104">Šajā tēmā skaidrots, kā atrast un atrisināt veiktspējas problēmas [Elektronisko pārskatu](general-electronic-reporting.md) (ER) [konfigurācijās](general-electronic-reporting.md#Configuration).</span><span class="sxs-lookup"><span data-stu-id="f145c-104">This topic explains how to find and solve performance issues in [Electronic reporting](general-electronic-reporting.md) (ER) [configurations](general-electronic-reporting.md#Configuration).</span></span>

<span data-ttu-id="f145c-105">Parasti veiktspējas izpēte sastāv no vairākām darbībām.</span><span class="sxs-lookup"><span data-stu-id="f145c-105">Typically, performance investigation consists of several steps.</span></span>

1. <span data-ttu-id="f145c-106">[Apkopot](#collecting-data) datus.</span><span class="sxs-lookup"><span data-stu-id="f145c-106">[Collect](#collecting-data) data.</span></span>
2. <span data-ttu-id="f145c-107">Analizēt apkopotos datus.</span><span class="sxs-lookup"><span data-stu-id="f145c-107">Analyze the collected data.</span></span>
3. <span data-ttu-id="f145c-108">Pamatojoties uz analīzes rezultātiem, izmantojiet ER konfigurācijas, lai [veiktu izmaiņas](#making-changes), vai arī izlemtu apkopot vairāk datu.</span><span class="sxs-lookup"><span data-stu-id="f145c-108">Based on the results of the analysis, use ER configurations to [make changes](#making-changes), or decide to collect more data.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="f145c-109">Problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="f145c-109">Troubleshooting</span></span>

### <a name="analyze-execution-time"></a><span data-ttu-id="f145c-110">Analizēt izpildes laiku</span><span class="sxs-lookup"><span data-stu-id="f145c-110">Analyze execution time</span></span>

<span data-ttu-id="f145c-111">Izpildes laiks var būt atkarīgs no neprognozējamiem faktoriem, piemēram, citiem uzdevumiem, kas darbojas tajā pašā vidē, un kešdarbes, kas izmanto datus, kad tie tiek izsaukti pirmo reizi.</span><span class="sxs-lookup"><span data-stu-id="f145c-111">Execution time can depend on unpredictable factors, such as other tasks that are running in the same environment and caching that uses data when it's called for the first time.</span></span> <span data-ttu-id="f145c-112">Tādēļ izpilde un mērījums ir jāatkārto vairākas reizes.</span><span class="sxs-lookup"><span data-stu-id="f145c-112">Therefore, you should repeat the execution and measurement several times.</span></span>

<span data-ttu-id="f145c-113">Dažreiz veiktspējas problēmas nav saistītas ar ER formāta konfigurāciju, kas tiek izmantota pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="f145c-113">Sometimes, performance issues aren't caused by an ER format configuration that is used for reporting.</span></span> <span data-ttu-id="f145c-114">Tā vietā tās izraisa X++ kods, kas tiek izmantots, lai atvērtu šī ER formāta konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="f145c-114">Instead, they are caused by the X++ code that is used to open that ER format configuration.</span></span>

1. <span data-ttu-id="f145c-115">Vai nu [darbību centrā](#infolog-time) vai [notikumu žurnālā](#event-log-time) skatiet pārskata izpildes laiku.</span><span class="sxs-lookup"><span data-stu-id="f145c-115">In either the [Action center](#infolog-time) or the [event log](#event-log-time), look at the execution time of the report.</span></span>
2. <span data-ttu-id="f145c-116">Salīdziniet pārskata izpildes laiku ar kopējo izpildes laiku scenārijā.</span><span class="sxs-lookup"><span data-stu-id="f145c-116">Compare the execution time of the report with the total execution time in the scenario.</span></span>
3. <span data-ttu-id="f145c-117">Ja pārskata izpildes laiks ir daudz mazāks nekā kopējais izpildes laiks, apsveriet datu apjomu, ko pārskats apstrādā:</span><span class="sxs-lookup"><span data-stu-id="f145c-117">If the execution time of the report is much less than the total execution time, consider the amount of data that the report processes:</span></span>

    - <span data-ttu-id="f145c-118">Ja pārskats apstrādā mazu datu apjomu, problēma var ietvert konfigurācijas ielādes laiku.</span><span class="sxs-lookup"><span data-stu-id="f145c-118">If the report processes a small amount of data, the issue might involve the loading time of the configuration.</span></span>
    - <span data-ttu-id="f145c-119">Ja pārskats apstrādā lielu datu apjomu, problēma var ietvert koda X++ pirmapstrādi.</span><span class="sxs-lookup"><span data-stu-id="f145c-119">If the report processes a large amount of data, the issue might involve preprocessing X++.</span></span> <span data-ttu-id="f145c-120">Izmantojiet [Trace parsētāju](#analyze-trace-parser-trace), lai analizētu šo gadījumu.</span><span class="sxs-lookup"><span data-stu-id="f145c-120">Use [Trace parser](#analyze-trace-parser-trace) to analyze this case.</span></span>

    <span data-ttu-id="f145c-121">Pārējos gadījumos skatiet nākamās sadaļas.</span><span class="sxs-lookup"><span data-stu-id="f145c-121">For other cases, see the next sections.</span></span>

4. <span data-ttu-id="f145c-122">Veiciet vairākus testus, kas ietver dažādus datu apjomus, lai noteiktu, kā izpildes laiks ir atkarīgs no datu apjoma.</span><span class="sxs-lookup"><span data-stu-id="f145c-122">Run multiple tests that involve different amounts of data to determine how the execution time depends on the amount of data.</span></span>

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a><span data-ttu-id="f145c-123">Trace parsētāja darbību izsekošanas analīze</span><span class="sxs-lookup"><span data-stu-id="f145c-123">Analyze Trace parser traces</span></span>

<span data-ttu-id="f145c-124">Sagatavojiet nelielu piemēru vai savāciet vairākas izsekotās darbības no pārskata ģenerēšanas nejaušām daļām.</span><span class="sxs-lookup"><span data-stu-id="f145c-124">Prepare a small example, or collect several traces during random parts of the report generation.</span></span>

<span data-ttu-id="f145c-125">Pēc tam [Trace parsētājā](#trace-parser) veiciet pilnu standarta analīzi un atbildiet uz šādiem jautājumiem:</span><span class="sxs-lookup"><span data-stu-id="f145c-125">Then, in [Trace parser](#trace-parser), do a standard bottom-to-up analysis, and answer the following questions:</span></span>

- <span data-ttu-id="f145c-126">Kādas ir galvenās metodes attiecībā uz laika patēriņu?</span><span class="sxs-lookup"><span data-stu-id="f145c-126">What are the top methods in terms of time consumption?</span></span>
- <span data-ttu-id="f145c-127">Kādu daļu no kopējā laika šīs metodes izmanto?</span><span class="sxs-lookup"><span data-stu-id="f145c-127">What part of the overall time do those methods use?</span></span>

<span data-ttu-id="f145c-128">Atbildiet uz tiem pašiem jautājumiem arī par vaicājumiem.</span><span class="sxs-lookup"><span data-stu-id="f145c-128">Answer the same questions for queries.</span></span>

<span data-ttu-id="f145c-129">Ja redzat, ka metodes prefiksā ir “ER”, pārejiet uz nākamo sadaļu.</span><span class="sxs-lookup"><span data-stu-id="f145c-129">If you see that methods are prefixed with "ER," move on to the next section.</span></span>

<span data-ttu-id="f145c-130">Ja redzat, ka metodes vai vaicājumi tiek veidoti programmas komplektā, apsveriet vispārēju optimizāciju (piemēram, izveidojot indeksus).</span><span class="sxs-lookup"><span data-stu-id="f145c-130">If you see that methods or queries originated in the application suite, consider generic optimizations (for example, create indexes).</span></span>

<span data-ttu-id="f145c-131">Analizējiet izsaukumu skaitu.</span><span class="sxs-lookup"><span data-stu-id="f145c-131">Analyze the number of calls.</span></span> <span data-ttu-id="f145c-132">Ja to skaits ir ievērojami augstāks nekā paredzēts, apsveriet atbilstošo konfigurācijas mezglu kešdarbi.</span><span class="sxs-lookup"><span data-stu-id="f145c-132">If the number is significantly higher than expected, consider caching the corresponding nodes of the configuration.</span></span>

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a><span data-ttu-id="f145c-133">Datu bāzes izsaukumu analīze</span><span class="sxs-lookup"><span data-stu-id="f145c-133">Analyze database calls</span></span>

<span data-ttu-id="f145c-134">Sagatavojiet piemēru, kas satur nelielu datu apjomu, lai varētu apkopot [ER izsekotās darbības](#electronic-reporting-traces).</span><span class="sxs-lookup"><span data-stu-id="f145c-134">Prepare an example that has a small amount of data, so that you can collect an [ER trace](#electronic-reporting-traces).</span></span>

<span data-ttu-id="f145c-135">Pēc tam atveriet izsekotās darbības ER modeļa kartēšanas noformētājā un apskatiet lapas apakšpusi.</span><span class="sxs-lookup"><span data-stu-id="f145c-135">Then open the trace in the ER model mapping designer, and look at the bottom of the page.</span></span> <span data-ttu-id="f145c-136">Atbildiet uz šādiem jautājumiem:</span><span class="sxs-lookup"><span data-stu-id="f145c-136">Answer the following questions:</span></span>

- <span data-ttu-id="f145c-137">Vai tiek veikta vaicājumu dublēšana?</span><span class="sxs-lookup"><span data-stu-id="f145c-137">Is there any query duplication?</span></span> <span data-ttu-id="f145c-138">Ja tā ir, apsveriet vienu no šiem labojumiem:</span><span class="sxs-lookup"><span data-stu-id="f145c-138">If there is, consider one of the following fixes:</span></span>

    - <span data-ttu-id="f145c-139">[Izmantojiet kešdarbi](#use-caching), ja domājat, ka vienā pamatierakstā ir vairāki izsaukumi.</span><span class="sxs-lookup"><span data-stu-id="f145c-139">[Use caching](#use-caching) if you think that there are several calls inside one parent record.</span></span>
    - <span data-ttu-id="f145c-140">[Izmantojiet kešdarbes parametru aprēķinātu lauku](#cached-parameterized), ja domājat, ka dažādos ierakstos ir izsaukumi uz vienu un to pašu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f145c-140">[Use a cached, parameterized calculated field](#cached-parameterized) if you think that there are calls to the same record inside different records.</span></span>
    - <span data-ttu-id="f145c-141">[Izmantojiet **JOIN** datu avotu](#use-join-datasource), ja jums ir jālasa ļoti daudz dažādu datu bāzu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f145c-141">[Use a **JOIN** data source](#use-join-datasource) if you have to read to a substantial number of different records from a database.</span></span>

- <span data-ttu-id="f145c-142">Vai vaicājumu un ienesto ierakstu skaits atbilst vispārējam datu apjomam?</span><span class="sxs-lookup"><span data-stu-id="f145c-142">Does the number of queries and fetched records correspond to the overall amount of data?</span></span> <span data-ttu-id="f145c-143">Piemēram, ja dokumentam ir 10 rindas, vai statistika rāda, ka pārskats izgūs 10 rindas vai 1000 rindas?</span><span class="sxs-lookup"><span data-stu-id="f145c-143">For example, if a document has 10 lines, do the statistics show that the report extracts 10 lines or 1,000 lines?</span></span> <span data-ttu-id="f145c-144">Ja jums ir liels skaits ienesto ierakstu, apsveriet vienu no šiem labojumiem:</span><span class="sxs-lookup"><span data-stu-id="f145c-144">If you have a substantial number of fetched records, consider one of the following fixes:</span></span>

    - <span data-ttu-id="f145c-145">[Izmantojiet funkciju **FILTER**, nevis **WHERE** funkciju](#filter), lai apstrādātu datus SQL Server pusē.</span><span class="sxs-lookup"><span data-stu-id="f145c-145">[Use the **FILTER** function instead of the **WHERE** function](#filter) to process data on the SQL Server side.</span></span>
    - <span data-ttu-id="f145c-146">Izmantojiet kešdarbi, lai izvairītos no to pašu datu ieneses.</span><span class="sxs-lookup"><span data-stu-id="f145c-146">Use caching to avoid fetching the same data.</span></span>
    - <span data-ttu-id="f145c-147">[Izmantojiet apkopoto datu funkcijas](#collected-data), lai izvairītos no to pašu ienesto datu apkopošanas.</span><span class="sxs-lookup"><span data-stu-id="f145c-147">[Use collected data functions](#collected-data) to avoid fetching the same data for summarization.</span></span>

### <a name="analyze-perfview-traces"></a><span data-ttu-id="f145c-148">PerfView darbību izsekošanas analīze</span><span class="sxs-lookup"><span data-stu-id="f145c-148">Analyze PerfView traces</span></span>

<span data-ttu-id="f145c-149">[PerfView](#perfview) ir pieredzējušu izstrādātāju rīks.</span><span class="sxs-lookup"><span data-stu-id="f145c-149">[PerfView](#perfview) is a tool for experienced developers.</span></span> <span data-ttu-id="f145c-150">Papildinformāciju par tālāk minētajām darbībām skatiet sadaļā [Pulksteņa laika izpētes pamati](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span><span class="sxs-lookup"><span data-stu-id="f145c-150">For more detailed information about the following steps, see [Wall Clock Time Investigation Basics](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span></span>

1. <span data-ttu-id="f145c-151">Apkopojiet izsekotās darbības, izmantojot pavediena laiku.</span><span class="sxs-lookup"><span data-stu-id="f145c-151">Collect a trace by using thread time.</span></span>
2. <span data-ttu-id="f145c-152">Ietveriet tikai stekus, kas izmanto **runUnattended**, lai filtrētu tikai pavedienu, kam ir konfigurācijas izpilde.</span><span class="sxs-lookup"><span data-stu-id="f145c-152">Include only stacks that use **runUnattended**, to filter only the thread that has configuration execution.</span></span> <span data-ttu-id="f145c-153">(Pievienojiet **runUnattended** pie **IncPats** ievades lodziņa.)</span><span class="sxs-lookup"><span data-stu-id="f145c-153">(Add **runUnattended** to the **IncPats** input box.)</span></span>
3. <span data-ttu-id="f145c-154">Saīsiniet visu CPU, tīklu un bloķēto laiku.</span><span class="sxs-lookup"><span data-stu-id="f145c-154">Fold all CPU, network, and blocked time.</span></span>
4. <span data-ttu-id="f145c-155">Ielādējiet [ER priekšiestatījumus rīkam PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span><span class="sxs-lookup"><span data-stu-id="f145c-155">Load [ER presets for PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span></span>
5. <span data-ttu-id="f145c-156">Atlasiet **ER** \> **Citi priekšiestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="f145c-156">Select **ER** \> **Other preset**.</span></span>
6. <span data-ttu-id="f145c-157">Apskatiet nosaukumus:</span><span class="sxs-lookup"><span data-stu-id="f145c-157">Look at the names:</span></span>

    - <span data-ttu-id="f145c-158">Iespējams, redzēsit platformas kodu, kas aizņem visvairāk laika.</span><span class="sxs-lookup"><span data-stu-id="f145c-158">You will probably see the platform code that consumes the most time.</span></span>
    - <span data-ttu-id="f145c-159">Varat veikt dubultskārienu (vai dubultklikšķi) un doties uz **izsaukumiem**.</span><span class="sxs-lookup"><span data-stu-id="f145c-159">You can double-tap (or double-click) and go up through **callees**.</span></span>

        <span data-ttu-id="f145c-160">Ja atradīsit klases ar prefiksu “ERExpression”, un ja tās ir funkcijas, kas saistītas ar formulām, tad funkciju nosaukumu iespējams atrast, balstoties uz klases nosaukuma, un varat apskatīt ER repositoriju, lai skatītu atribūtus.</span><span class="sxs-lookup"><span data-stu-id="f145c-160">If you find classes that have the prefix "ERExpression," and if they are functions that are related to formulas, you can guess the function name based on the class name, and you can look at the ER repo to view the attributes.</span></span>

### <a name="fixes"></a><span data-ttu-id="f145c-161">Labojumi</span><span class="sxs-lookup"><span data-stu-id="f145c-161">Fixes</span></span>

- <span data-ttu-id="f145c-162">Ja redzams, ka vaicājumi patērē lielāko daļu no CPU laika, mēģiniet samazināt vaicājumu apjomu:</span><span class="sxs-lookup"><span data-stu-id="f145c-162">If you see that most of the CPU time is consumed by queries, try to reduce the number of queries:</span></span>

    - <span data-ttu-id="f145c-163">[Pārskatiet ER izsekotās darbības](#analyze-database-calls), meklējot vaicājumu dublējumus.</span><span class="sxs-lookup"><span data-stu-id="f145c-163">[Review the ER trace](#analyze-database-calls) for duplicated queries.</span></span>
    - <span data-ttu-id="f145c-164">Apskatiet, cik ierakstu tiek ienesti, un novērtējiet, cik daudz datu teorētiski būtu jāienes.</span><span class="sxs-lookup"><span data-stu-id="f145c-164">See how many records are fetched, and evaluate how much data should theoretically be fetched.</span></span>

- <span data-ttu-id="f145c-165">Ja redzat, ka lielāko daļu no CPU laika patērē funkcijas, mēģiniet atrast vietu konfigurācijā, kas patērē visvairāk resursu.</span><span class="sxs-lookup"><span data-stu-id="f145c-165">If you see that most of the CPU time is consumed by the functions that are used, try to find the place in the configuration that consumes the most resources.</span></span>
- <span data-ttu-id="f145c-166">Ja redzat, ka lielāko daļu no CPU laika patērē datu apkopošanas funkcijas, apsveriet iespēju tās aizstāt ar *SQL grupēšanu pēc* modeļa kartēšanas puses.</span><span class="sxs-lookup"><span data-stu-id="f145c-166">If you see that most of the CPU time is consumed by data collection functions, consider replacing them with *SQL group by* on the model mapping side.</span></span>

### <a name="collecting-data"></a><a name="collecting-data"></a><span data-ttu-id="f145c-167">Datu apkopošana</span><span class="sxs-lookup"><span data-stu-id="f145c-167">Collecting data</span></span>

<span data-ttu-id="f145c-168">Atkarībā no vides ir vairāki veidi, kā apkopot pieejamos datus:</span><span class="sxs-lookup"><span data-stu-id="f145c-168">Depending on your environment, there are several ways to collect available data:</span></span>

- <span data-ttu-id="f145c-169">Iegūt kopējo palaišanas laiku no:</span><span class="sxs-lookup"><span data-stu-id="f145c-169">Get the total running time:</span></span>

    - <span data-ttu-id="f145c-170">Darbību centra</span><span class="sxs-lookup"><span data-stu-id="f145c-170">From the Action center</span></span>
    - <span data-ttu-id="f145c-171">Notikumu žurnāla</span><span class="sxs-lookup"><span data-stu-id="f145c-171">From the event log</span></span>

- <span data-ttu-id="f145c-172">Izpildes profilēšana izmantojot:</span><span class="sxs-lookup"><span data-stu-id="f145c-172">Profile the execution:</span></span>

    - <span data-ttu-id="f145c-173">ER rīkus</span><span class="sxs-lookup"><span data-stu-id="f145c-173">By using ER tools</span></span>
    - <span data-ttu-id="f145c-174">Trace parsētāju</span><span class="sxs-lookup"><span data-stu-id="f145c-174">By using Trace parser</span></span>
    - <span data-ttu-id="f145c-175">PerfView</span><span class="sxs-lookup"><span data-stu-id="f145c-175">By using PerfView</span></span>

#### <a name="collecting-data-in-a-production-environment"></a><span data-ttu-id="f145c-176">Datu apkopošana ražošanas vidē</span><span class="sxs-lookup"><span data-stu-id="f145c-176">Collecting data in a production environment</span></span>

<span data-ttu-id="f145c-177">Dažreiz problēmas var pavairot tikai ražošanas vidē.</span><span class="sxs-lookup"><span data-stu-id="f145c-177">Sometimes, issues can be reproduced only in a production environment.</span></span> <span data-ttu-id="f145c-178">Datus var apkopot, šādos veidos:</span><span class="sxs-lookup"><span data-stu-id="f145c-178">Data can be collected in the following ways:</span></span>

- <span data-ttu-id="f145c-179">Izmantojot [Trace parsētāja](../perf-test/trace-trace-tutorial.md) darbību izsekošanu</span><span class="sxs-lookup"><span data-stu-id="f145c-179">By using [Trace parser](../perf-test/trace-trace-tutorial.md) traces</span></span>
- <span data-ttu-id="f145c-180">Izmantojot [ER izpildes](trace-execution-er-troubleshoot-perf.md) darbību izsekošanu</span><span class="sxs-lookup"><span data-stu-id="f145c-180">By using [ER execution](trace-execution-er-troubleshoot-perf.md) traces</span></span>
- <span data-ttu-id="f145c-181">Izmantojot kopējo izpildes laiku</span><span class="sxs-lookup"><span data-stu-id="f145c-181">By using the total execution time</span></span>

#### <a name="collecting-data-in-a-development-environment"></a><span data-ttu-id="f145c-182">Datu apkopošana izstrādes vidē</span><span class="sxs-lookup"><span data-stu-id="f145c-182">Collecting data in a development environment</span></span>

<span data-ttu-id="f145c-183">Papildus tiem rīkiem, kurus var izmantot ražošanas vidē, ir vairāki rīki, ko var izmantot izstrādes vidē:</span><span class="sxs-lookup"><span data-stu-id="f145c-183">In addition to the tools that can be used in a production environment, there are several tools that you can use in a development environment:</span></span>

- <span data-ttu-id="f145c-184">Notikumu žurnāls (Microsoft-Dynamics-ElectronicReporting).</span><span class="sxs-lookup"><span data-stu-id="f145c-184">Event log (Microsoft-Dynamics-ElectronicReporting).</span></span> <span data-ttu-id="f145c-185">Šis žurnāls var sniegt kopējo izpildes laiku.</span><span class="sxs-lookup"><span data-stu-id="f145c-185">This log can give you the total execution time.</span></span>
- <span data-ttu-id="f145c-186">Vispārīgie .NET rīki, piemēram, PerfView.</span><span class="sxs-lookup"><span data-stu-id="f145c-186">Common .NET tools, such as PerfView.</span></span>

<span data-ttu-id="f145c-187">Turklāt izstrādes vide sniedz lielāku elastību attiecībā uz eksperimentiem.</span><span class="sxs-lookup"><span data-stu-id="f145c-187">Additionally, a development environment gives you more flexibility to experiment.</span></span> <span data-ttu-id="f145c-188">Piemēram, varat izslēgt daļu pārskatu, lai redzētu, kā tiek ietekmēts izpildes laiks.</span><span class="sxs-lookup"><span data-stu-id="f145c-188">For example, you can turn off parts of reports to see how the execution time is affected.</span></span>

### <a name="tools"></a><a name="tools"></a><span data-ttu-id="f145c-189">Rīki</span><span class="sxs-lookup"><span data-stu-id="f145c-189">Tools</span></span>

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a><span data-ttu-id="f145c-190">Izpildes laiks darbību centrā</span><span class="sxs-lookup"><span data-stu-id="f145c-190">Execution time in the Action center</span></span>

<span data-ttu-id="f145c-191">ER var parādīt konfigurācijas izpildes laiku darbību centrā.</span><span class="sxs-lookup"><span data-stu-id="f145c-191">ER can show the execution time of the configuration in the Action center.</span></span> <span data-ttu-id="f145c-192">Šī opcija darbojas tikai noteiktam lietotājam un noteiktam uzņēmumam, kā arī tikai interaktīvām sesijām.</span><span class="sxs-lookup"><span data-stu-id="f145c-192">This option works only for a specific user and a specific company, and only for interactive sessions.</span></span> <span data-ttu-id="f145c-193">Lai padarītu šo līdzekli pieejamu, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="f145c-193">To make this feature available, follow these steps.</span></span>

1. <span data-ttu-id="f145c-194">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="f145c-194">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="f145c-195">Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.</span><span class="sxs-lookup"><span data-stu-id="f145c-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="f145c-196">Dialoglodziņā **Lietotāja parametri** iestatiet opciju **Rādīt failu ģenerēšanas laiku** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="f145c-196">In the **User parameters** dialog box, set the **Show file generation time** option to **Yes**.</span></span>

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a><span data-ttu-id="f145c-197">Izpildes laiks notikumu žurnālā</span><span class="sxs-lookup"><span data-stu-id="f145c-197">Execution time in the event log</span></span>

1. <span data-ttu-id="f145c-198">Atvērt Windows Notikumu skatītāju.</span><span class="sxs-lookup"><span data-stu-id="f145c-198">Open Windows Event Viewer.</span></span>
2. <span data-ttu-id="f145c-199">Sadaļā **Programmu un pakalpojumu žurnāli** atveriet **Microsoft-Dynamics-ElectronicReporting/Operational**.</span><span class="sxs-lookup"><span data-stu-id="f145c-199">Under **Applications and Services logs**, open **Microsoft-Dynamics-ElectronicReporting/Operational**.</span></span>
3. <span data-ttu-id="f145c-200">Meklējiet **FormatMapingRun** notikumus, kur **EventID=2**, jo šie notikumi ietver informāciju par patērēto laiku.</span><span class="sxs-lookup"><span data-stu-id="f145c-200">Look for **FormatMapingRun** events where **EventID=2**, because these events contain the information about elapsed time.</span></span>

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a><span data-ttu-id="f145c-201">Trace parsētāja darbību izsekošana</span><span class="sxs-lookup"><span data-stu-id="f145c-201">Trace parser traces</span></span> 

<span data-ttu-id="f145c-202">Tā kā ER ir ieviests kodā X++, varat izmantot vispārējos X++ rīkus, veiktspējas analizēšanai.</span><span class="sxs-lookup"><span data-stu-id="f145c-202">Because ER is implemented in X++, you can use common X++ tools to analyze performance.</span></span> <span data-ttu-id="f145c-203">Papildinformāciju skatiet sadaļā [Darbību izsekošana, izmantojot Trace parsētāju](../perf-test/trace-trace-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="f145c-203">For more information, see [Take traces by using Trace parser](../perf-test/trace-trace-tutorial.md).</span></span>

<span data-ttu-id="f145c-204">Šai pieejai ir daži ierobežojumi.</span><span class="sxs-lookup"><span data-stu-id="f145c-204">There are a few limitations to this approach.</span></span> <span data-ttu-id="f145c-205">Tā kā daļa no ER ir ieviesta C#, ne visa informācija būs pieejama.</span><span class="sxs-lookup"><span data-stu-id="f145c-205">Because part of ER is implemented in C#, not all the details will be available.</span></span> <span data-ttu-id="f145c-206">Tomēr, varat skatīt datu izmantošanas informāciju.</span><span class="sxs-lookup"><span data-stu-id="f145c-206">However, you can view the data usage details.</span></span> <span data-ttu-id="f145c-207">Turklāt pārskata ilga izpilde var pārsniegt darbību izsekošanas krātuves ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="f145c-207">Additionally, long report runs can exceed trace storage limitations.</span></span>

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a><span data-ttu-id="f145c-208">ER darbību izsekošana</span><span class="sxs-lookup"><span data-stu-id="f145c-208">ER traces</span></span>

<span data-ttu-id="f145c-209">ER var apkopot savu darbību izsekošanas informāciju, un tam ir vizualizācijas un analīzes rīki, kas paredzēti šīm izsekotajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="f145c-209">ER can collect its own traces, and it has visualization and analysis tools for those traces.</span></span> <span data-ttu-id="f145c-210">Papildinformāciju skatiet [Elektronisko atskaišu veidošanas (ER) formāta failu izpildes uzraudzīšana, lai novērstu veiktspējas problēmas](trace-execution-er-troubleshoot-perf.md).</span><span class="sxs-lookup"><span data-stu-id="f145c-210">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

#### <a name="perfview"></a><a name="perfview"></a><span data-ttu-id="f145c-211">PerfView</span><span class="sxs-lookup"><span data-stu-id="f145c-211">PerfView</span></span>

<span data-ttu-id="f145c-212">Tā kā gan X++, gan ER ir ieviesti papildus .NET platformai, varat izmantot vispārējos .NET rīkus.</span><span class="sxs-lookup"><span data-stu-id="f145c-212">Because both X++ and ER are implemented on top of the .NET platform, you can use common .NET tools.</span></span> <span data-ttu-id="f145c-213">Piemēram, varat izmantot bezmaksas [PerfView](https://github.com/Microsoft/perfview) rīku.</span><span class="sxs-lookup"><span data-stu-id="f145c-213">For example, you can use the free [PerfView](https://github.com/Microsoft/perfview) tool.</span></span>

<span data-ttu-id="f145c-214">Varat arī apkopot datus no komandrindas.</span><span class="sxs-lookup"><span data-stu-id="f145c-214">You can also collect data from the command line.</span></span> <span data-ttu-id="f145c-215">Piemēram, tālāk redzamais Windows PowerShell skripts apkopo izpildes laiku, līdz datorā tiek apturēta jebkāda formāta izpilde.</span><span class="sxs-lookup"><span data-stu-id="f145c-215">For example, the following Windows PowerShell script collects the execution time until any format execution is stopped on the machine.</span></span>

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

<span data-ttu-id="f145c-216">Šai pieejai ir daži ierobežojumi.</span><span class="sxs-lookup"><span data-stu-id="f145c-216">There are a few limitations to this approach.</span></span> <span data-ttu-id="f145c-217">Jums ir nepieciešama administratora piekļuve šim datoram.</span><span class="sxs-lookup"><span data-stu-id="f145c-217">You must have administrative access to the machine.</span></span> <span data-ttu-id="f145c-218">Turklāt jums ir jābūt pieredzējušiem izstrādātājiem, jo eksistē grūtības apgūt šo pieredzi.</span><span class="sxs-lookup"><span data-stu-id="f145c-218">Additionally, you must be an experienced developer, because there is a steep learning curve.</span></span>

### <a name="making-changes"></a><a name="making-changes"></a><span data-ttu-id="f145c-219">Izmaiņu veikšana</span><span class="sxs-lookup"><span data-stu-id="f145c-219">Making changes</span></span>

#### <a name="use-caching"></a><a name="use-caching"></a><span data-ttu-id="f145c-220">Kešdarbes izmantošana</span><span class="sxs-lookup"><span data-stu-id="f145c-220">Use caching</span></span>

<span data-ttu-id="f145c-221">Lai gan kešdarbe samazina laiku, kas nepieciešams atkārtotai datu ienesei, tā aizņem lielu atmiņas krātuves vietu.</span><span class="sxs-lookup"><span data-stu-id="f145c-221">Although caching reduces the amount of time that is required to fetch data again, it costs memory.</span></span> <span data-ttu-id="f145c-222">Izmantojiet kešdarbi gadījumos, kad ienesto datu apjoms nav pārāk liels.</span><span class="sxs-lookup"><span data-stu-id="f145c-222">Use caching in cases where the amount of fetched data isn't very large.</span></span> <span data-ttu-id="f145c-223">Papildinformāciju un piemēru, kas parāda, kā izmantot kešdarbi, skatiet sadaļā [Modeļa kartēšanas uzlabošana, pamatojoties uz izpildes darbību izsekošanas informāciju](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span><span class="sxs-lookup"><span data-stu-id="f145c-223">For more information and an example that shows how to use caching, see [Improve the model mapping based on information from the execution trace](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span></span>

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a><span data-ttu-id="f145c-224">Izmantot kešdarbes parametru aprēķināto lauku</span><span class="sxs-lookup"><span data-stu-id="f145c-224">Use a cached, parameterized calculated field</span></span>

<span data-ttu-id="f145c-225">Dažreiz vērtības ir nepieciešams izmantot atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="f145c-225">Sometimes, values must be looked up repeatedly.</span></span> <span data-ttu-id="f145c-226">Piemēri ietver kontu nosaukumus un kontu numurus.</span><span class="sxs-lookup"><span data-stu-id="f145c-226">Examples include account names and account numbers.</span></span> <span data-ttu-id="f145c-227">Lai ietaupītu laiku, varat izveidot aprēķinātu lauku, kura parametri atrodas augstākajā līmenī, un pēc tam pievienot šo lauku kešatmiņai.</span><span class="sxs-lookup"><span data-stu-id="f145c-227">To help save time, you can create a calculated field that has parameters on the top level, and then add the field to the cache.</span></span>

<span data-ttu-id="f145c-228">Šo pieeju ieteicams lietot tikai tad, ja kešatmiņā saglabāto datu lielums ir mazs.</span><span class="sxs-lookup"><span data-stu-id="f145c-228">We recommend that you use this approach only when the size of the cached data is small.</span></span> <span data-ttu-id="f145c-229">Papildinformāciju skatiet sadaļā [ER risinājumu veiktspējas uzlabošana, pievienojot APRĒĶINĀTĀ LAUKA datu avotu parametrus](er-calculated-field-ds-performance.md).</span><span class="sxs-lookup"><span data-stu-id="f145c-229">For more information, see [Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources](er-calculated-field-ds-performance.md).</span></span>

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a><span data-ttu-id="f145c-230">SAVIENOJUMA datu avota izmantošana</span><span class="sxs-lookup"><span data-stu-id="f145c-230">Use a JOIN data source</span></span>

<span data-ttu-id="f145c-231">Datu avots **SAVIENOJUMS** iespējo vairāku savienotu ierakstu ienešanu, izmantojot vienu vaicājumu.</span><span class="sxs-lookup"><span data-stu-id="f145c-231">A **JOIN** data source enables several connected records to be fetched by one query.</span></span> <span data-ttu-id="f145c-232">Nav nepieciešams izmantot atsevišķu vaicājumu, lai ienestu katru savienoto ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f145c-232">A separate query doesn't have to be used to fetch each connected record.</span></span> <span data-ttu-id="f145c-233">Piemēram, ja ir 1000 rindas un katras rindas krājumu dati tiek ienesti, izmantojot relāciju, tad sanāks 1001 vaicājums (= 1000 + 1).</span><span class="sxs-lookup"><span data-stu-id="f145c-233">For example, if you have 1,000 lines, and you fetch item data for each line by relation, you will have 1,001 queries (= 1,000 + 1).</span></span> <span data-ttu-id="f145c-234">Izmantojot **SAVIENOJUMA** datu avotu, jūs izmantosit tikai vienu vaicājumu, lai ienestu tos pašus datus.</span><span class="sxs-lookup"><span data-stu-id="f145c-234">If you use a **JOIN** data source, you will use only one query to fetch the same data.</span></span> <span data-ttu-id="f145c-235">Papildinformāciju skatiet sadaļā [Izmantojiet SAVIENOJUMA datu avotus ER modeļu kartējumos, lai iegūtu datus no vairākām programmas tabulām](er-join-data-sources.md).</span><span class="sxs-lookup"><span data-stu-id="f145c-235">For more information, see [Use JOIN data sources in ER model mappings to get data from multiple application tables](er-join-data-sources.md).</span></span>

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a><span data-ttu-id="f145c-236">Funkcijas WHERE vietā izmantot funkciju FILTER</span><span class="sxs-lookup"><span data-stu-id="f145c-236">Use the FILTER function instead of the WHERE function</span></span>

<span data-ttu-id="f145c-237">Funkcija **[FILTER](er-functions-list-filter.md)** platformā SQL Server izpilda nosacījumus, savukārt **WHERE** funkcija ienes visus datus no saraksta pa vienam ierakstam un piemēro nosacījumus katram ierakstam.</span><span class="sxs-lookup"><span data-stu-id="f145c-237">The **[FILTER](er-functions-list-filter.md)** function runs conditions on SQL Server, whereas the **WHERE** function fetches all data from the list, one record at a time, and applies the condition for each record.</span></span> <span data-ttu-id="f145c-238">Piemēram, jūs vēlaties atlasīt vienu ierakstu no 1000 ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="f145c-238">For example, you want to select one record out of 1,000 records.</span></span> <span data-ttu-id="f145c-239">Ja izmantosit **WHERE**, tiks ienesti visi 1000 ieraksti.</span><span class="sxs-lookup"><span data-stu-id="f145c-239">If you use **WHERE**, all 1,000 records will be fetched.</span></span> <span data-ttu-id="f145c-240">Tomēr, ja izmantosit **FILTER**, tiks ienests tieši viens ieraksts.</span><span class="sxs-lookup"><span data-stu-id="f145c-240">However, if you use **FILTER**, exactly one record will be fetched.</span></span> <span data-ttu-id="f145c-241">**FILTER** var izmantot arī indeksus datu bāzes pusē.</span><span class="sxs-lookup"><span data-stu-id="f145c-241">**FILTER** can also use indexes on the database side.</span></span>

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a><span data-ttu-id="f145c-242">Apkopoto datu funkciju vai uzkrāto datu avota izmantošana</span><span class="sxs-lookup"><span data-stu-id="f145c-242">Using collected data functions or an accumulated data data source</span></span>

<span data-ttu-id="f145c-243">Ja konfigurācijai ir *grupēt pēc* komponents, kas apkopo iepriekš ienestos datus pēc pārskata, tad komponents visus datus ienesīs atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="f145c-243">If your configuration has a *group by* component that summarizes previously fetched data by report, the component will fetch all the data again.</span></span> <span data-ttu-id="f145c-244">Izmantojot apkopotās datu funkcijas, jūs iespējojat ER uzkrāt datus pirmās ieneses laikā.</span><span class="sxs-lookup"><span data-stu-id="f145c-244">By using collected data functions, you enable ER to accumulate data during the first fetch.</span></span> <span data-ttu-id="f145c-245">Plašāku informāciju skatiet [ER formātu konfigurēšana, lai veiktu uzskaiti un summēšanu](tasks/er-format-counting-summing-2.md).</span><span class="sxs-lookup"><span data-stu-id="f145c-245">For more information, see [ER Configure format to do counting and summing](tasks/er-format-counting-summing-2.md).</span></span>

#### <a name="rewrite-parts-of-the-configuration-in-x"></a><span data-ttu-id="f145c-246">Konfigurācijas daļu pārrakstīšana kompilatorā X++</span><span class="sxs-lookup"><span data-stu-id="f145c-246">Rewrite parts of the configuration in X++</span></span>

<span data-ttu-id="f145c-247">ER atbalsta tabulu un klašu izsaukšanas metodes, ieskaitot paplašinājumus.</span><span class="sxs-lookup"><span data-stu-id="f145c-247">ER supports calling methods of tables and classes, including extensions.</span></span> <span data-ttu-id="f145c-248">Apsveriet iespēju pārrakstīt modeļa kartēšanas daļas kompilatorā X++, lai palīdzētu uzlabot veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="f145c-248">Consider rewriting parts of the model mapping in X++ to help improve performance.</span></span>

<span data-ttu-id="f145c-249">ER var patērēt datus no šādiem avotiem:</span><span class="sxs-lookup"><span data-stu-id="f145c-249">ER can consume data from the following sources:</span></span>

- <span data-ttu-id="f145c-250">Klases (**objekta** un **klases** datu avoti)</span><span class="sxs-lookup"><span data-stu-id="f145c-250">Classes (**object** and **class** data sources)</span></span>
- <span data-ttu-id="f145c-251">Tabulas (**tabulas** un **tabulas ierakstu** datu avoti)</span><span class="sxs-lookup"><span data-stu-id="f145c-251">Tables (**table** and **table records** data sources)</span></span>

<span data-ttu-id="f145c-252">Vēl [ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) nodrošina arī veidu, kā nosūtīt iepriekš aprēķinātos datus no izsaukšanas koda.</span><span class="sxs-lookup"><span data-stu-id="f145c-252">The [ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) also provides a way to send precalculated data from the calling code.</span></span> <span data-ttu-id="f145c-253">Programmas komplekts satur daudzus šādas pieejas piemērus.</span><span class="sxs-lookup"><span data-stu-id="f145c-253">The application suite contains numerous examples of this approach.</span></span>
