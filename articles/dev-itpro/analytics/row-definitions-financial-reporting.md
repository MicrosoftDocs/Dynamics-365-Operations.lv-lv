---
title: Rindas definīcijas finanšu atskaišu veidotājā
description: Rindas definīcija ir atskaites komponents jeb veidošanas bloks, kas norāda katras rindas saturu finanšu atskaitē. Rindas definīciju var kombinēt ar kolonnas definīcijām, atskaišu koka definīcijām un atskaites definīcijām, lai izveidotu veidošanas bloku grupu, kuru var izmantot vairāki uzņēmumi.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c829af1da1b3109f4687c9a2536dd156339d5c76
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551605"
---
# <a name="row-definitions-in-financial-report-designer"></a><span data-ttu-id="9754c-104">Rindas definīcijas finanšu atskaišu veidotājā</span><span class="sxs-lookup"><span data-stu-id="9754c-104">Row definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9754c-105">Rindas definīcija ir atskaites komponents jeb veidošanas bloks, kas norāda katras rindas saturu finanšu atskaitē.</span><span class="sxs-lookup"><span data-stu-id="9754c-105">A row definition is a report component, or building block, that specifies the contents of each row on a financial report.</span></span> <span data-ttu-id="9754c-106">Rindas definīciju var kombinēt ar kolonnas definīcijām, atskaišu koka definīcijām un atskaites definīcijām, lai izveidotu veidošanas bloku grupu, kuru var izmantot vairāki uzņēmumi.</span><span class="sxs-lookup"><span data-stu-id="9754c-106">A row definition can be combined with column definitions, reporting tree definitions, and report definitions to create a building block group that can be used by multiple companies.</span></span>

## <a name="create-a-row-definition"></a><span data-ttu-id="9754c-107">Rindu definīcijas izveide</span><span class="sxs-lookup"><span data-stu-id="9754c-107">Create a row definition</span></span>

1. <span data-ttu-id="9754c-108">Atskaišu veidotāja navigācijas rūtī noklikšķiniet uz **Rindas definīcijas**.</span><span class="sxs-lookup"><span data-stu-id="9754c-108">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="9754c-109">Izvēlnē **Fails** noklikšķiniet uz **Jauns** un pēc tam noklikšķiniet uz **Rindas definīcija**.</span><span class="sxs-lookup"><span data-stu-id="9754c-109">On the **File** menu, click **New**, and then click **Row Definition**.</span></span> <span data-ttu-id="9754c-110">Lai iegūtu papildu informāciju par katras šūnas saturu, skatiet [Rindu definīciju šūnu modificēšana](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="9754c-110">For more information about the content of each cell, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="open-a-row-definition"></a><span data-ttu-id="9754c-111">Rindas definīcijas atvēršana</span><span class="sxs-lookup"><span data-stu-id="9754c-111">Open a row definition</span></span>
1. <span data-ttu-id="9754c-112">Atskaišu veidotāja navigācijas rūtī noklikšķiniet uz **Rindas definīcijas**.</span><span class="sxs-lookup"><span data-stu-id="9754c-112">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="9754c-113">Veiciet dubultklikšķi uz tās rindas definīcijas, kuru vēlaties atvērt.</span><span class="sxs-lookup"><span data-stu-id="9754c-113">Double-click the name of the row definition to open.</span></span>
3. <span data-ttu-id="9754c-114">Lai apskatītu veidošanas blokus, kas ir saistīti ar rindas definīciju, ar peles labo pogu noklikšķiniet uz rindas definīcijas un tad atlasiet **Asociācijas**.</span><span class="sxs-lookup"><span data-stu-id="9754c-114">To view any building blocks that are associated with the row definition, right-click the row definition, and then select **Associations**.</span></span>

## <a name="contents-of-a-row-definition"></a><span data-ttu-id="9754c-115">Rindas definīcijas saturs</span><span class="sxs-lookup"><span data-stu-id="9754c-115">Contents of a row definition</span></span>
<span data-ttu-id="9754c-116">Rindas definīcijas var ietvert līdz 20 000 finanšu dimensiju rindu, kā arī tālāk minēto informāciju.</span><span class="sxs-lookup"><span data-stu-id="9754c-116">A row definition can contain up to 20,000 financial dimension rows and can include the following information:</span></span>

- <span data-ttu-id="9754c-117">Aprakstošs teksts, kas piešķir atskaitei jēgu, izveidojot sadaļu virsrakstus, rindas un atstarpes, piemēram, **Skaidra nauda** vai **Kopējie ieņēmumi**.</span><span class="sxs-lookup"><span data-stu-id="9754c-117">Descriptive text that adds meaning to the report by creating section headings, lines, and spaces, such as **Cash** or **Total Revenue**</span></span>
- <span data-ttu-id="9754c-118">Saites uz finanšu datiem, kuros var būt ietvertas dimensiju vērtības programmā Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9754c-118">Links to financial data, which can include dimension values in the Microsoft Dynamics 365 for Finance and Operations</span></span>

    > [!NOTE]
    > <span data-ttu-id="9754c-119">Varat iestatīt, lai katru reizi, kad tiek ģenerēts pārskats, rindu definīcijai tiktu iegūti dati no finanšu dimensiju sistēmas.</span><span class="sxs-lookup"><span data-stu-id="9754c-119">You can set up a row definition to pull data from the financial dimensions system every time that the report is generated.</span></span>

- <span data-ttu-id="9754c-120">Rindu kopsummas un formulas, kuru pamatā ir saistītie finanšu dati</span><span class="sxs-lookup"><span data-stu-id="9754c-120">Row totals and formulas that are based on the linked financial data</span></span>

<span data-ttu-id="9754c-121">Parasti katra rinda rindas definīcijā satur vienu no šiem informācijas tipiem:</span><span class="sxs-lookup"><span data-stu-id="9754c-121">Usually, each row in a row definition contains one of the following types of information:</span></span>

- <span data-ttu-id="9754c-122">Atsauces uz finanšu dimensiju sistēmu</span><span class="sxs-lookup"><span data-stu-id="9754c-122">References to the financial dimensions system</span></span>
- <span data-ttu-id="9754c-123">Kopsummas vai uz datiem balstīti aprēķini</span><span class="sxs-lookup"><span data-stu-id="9754c-123">Totals or calculations that are based on the data</span></span>
- <span data-ttu-id="9754c-124">Formatēšana</span><span class="sxs-lookup"><span data-stu-id="9754c-124">Formatting</span></span>

<span data-ttu-id="9754c-125">Rindas definīcijā informāciju var ievadīt divos veidos:</span><span class="sxs-lookup"><span data-stu-id="9754c-125">There are two methods for entering information in a row definition:</span></span>

- <span data-ttu-id="9754c-126">Informāciju manuāli ievadīt jaunā rindas definīcijā.</span><span class="sxs-lookup"><span data-stu-id="9754c-126">Manually enter row information in a new row definition.</span></span> <span data-ttu-id="9754c-127">Plašāku informāciju skatiet sadaļā [Rindu definīciju šūnu modificēšana](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="9754c-127">For more information, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>
- <span data-ttu-id="9754c-128">Izmantot atskaišu veidotāju, lai rindas informāciju izgūtu tieši no finanšu dimensijām.</span><span class="sxs-lookup"><span data-stu-id="9754c-128">Use report designer to pull row information directly from the financial dimensions.</span></span> <span data-ttu-id="9754c-129">Plašāku informāciju skatiet sadaļā “Saistītās formulas/rindas/vienības”, rakstā [Modificēt rindu definīcijas šūnas](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="9754c-129">For more information, see the "Related formulas/rows/units" section in [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="add-dimensions-in-a-row-definition"></a><span data-ttu-id="9754c-130">Dimensiju pievienošana rindas definīcijai</span><span class="sxs-lookup"><span data-stu-id="9754c-130">Add dimensions in a row definition</span></span>
<span data-ttu-id="9754c-131">Dimensija ir datu un vērtību krustpunkts.</span><span class="sxs-lookup"><span data-stu-id="9754c-131">A dimension is an intersection of data and values.</span></span> <span data-ttu-id="9754c-132">Atskaišu veidotājā datus un vērtības varat grupēt.</span><span class="sxs-lookup"><span data-stu-id="9754c-132">You can group data and values in report designer.</span></span> <span data-ttu-id="9754c-133">Pēc tam transakcijas varat detalizētāk klasificēt un analizēt.</span><span class="sxs-lookup"><span data-stu-id="9754c-133">You can then classify and analyze transactions in more detail.</span></span> <span data-ttu-id="9754c-134">Varat izmantot dialoglodziņu **Ievietot rindas no dimensijām**, lai vienlaicīgi rindas definīcijai pievienotu vairākas rindas.</span><span class="sxs-lookup"><span data-stu-id="9754c-134">You can use the **Insert Rows from Dimensions** dialog box to add multiple rows to a row definition at the same time.</span></span> <span data-ttu-id="9754c-135">Dialoglodziņā katrai dimensijai attēlo vienu kolonnu.</span><span class="sxs-lookup"><span data-stu-id="9754c-135">The dialog box displays one column for each dimension.</span></span> <span data-ttu-id="9754c-136">Nākamajā tabulā ir aprakstīta informācija, ko varat norādīt katrai dimensijai.</span><span class="sxs-lookup"><span data-stu-id="9754c-136">The following table describes the information that you can specify for each dimension.</span></span>

| <span data-ttu-id="9754c-137">Opcija</span><span class="sxs-lookup"><span data-stu-id="9754c-137">Option</span></span>                | <span data-ttu-id="9754c-138">Apraksts</span><span class="sxs-lookup"><span data-stu-id="9754c-138">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="9754c-139">Dimensija</span><span class="sxs-lookup"><span data-stu-id="9754c-139">Dimension</span></span>             | <span data-ttu-id="9754c-140">Modelis, kas identificē dimensiju, kura jāpievieno rindas definīcijai.</span><span class="sxs-lookup"><span data-stu-id="9754c-140">The pattern that identifies the dimension to add to the row definition.</span></span> <span data-ttu-id="9754c-141">Šajā modelī ir ietverta viena zīme & un viena restītes zīme (\#) atbilstoši katrai dimensiju pozīcijai.</span><span class="sxs-lookup"><span data-stu-id="9754c-141">This pattern contains one ampersand (&) or number sign (\#) for each position in the dimensions.</span></span> <span data-ttu-id="9754c-142">Parasti visas (&) zīmes tiek izmantotas galvenā konta dimensijai, un visas numura zīmes tiek izmantotas citām dimensijām.</span><span class="sxs-lookup"><span data-stu-id="9754c-142">Generally, use all ampersands for the Main Account dimension and all number signs for other dimensions.</span></span> |
| <span data-ttu-id="9754c-143">Dimensiju diapazona sākums</span><span class="sxs-lookup"><span data-stu-id="9754c-143">Dimension Range Start</span></span> | <span data-ttu-id="9754c-144">Pirmā šīs dimensijas vērtība, kas jāpievieno rindas definīcijai.</span><span class="sxs-lookup"><span data-stu-id="9754c-144">The first value for this dimension to add to the row definition.</span></span> |
| <span data-ttu-id="9754c-145">Dimensiju diapazona beigas</span><span class="sxs-lookup"><span data-stu-id="9754c-145">Dimension Range End</span></span>   | <span data-ttu-id="9754c-146">Pēdējā vērtība šai dimensijai, kuru pievienot rindas definīcijai.</span><span class="sxs-lookup"><span data-stu-id="9754c-146">The last value for this dimension to add to the row definition.</span></span> |

<span data-ttu-id="9754c-147">Lai rindas definīcijai pievienotu dimensijas, izpildiet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="9754c-147">To add dimensions to a row definition, follow these steps.</span></span>

1. <span data-ttu-id="9754c-148">Atskaišu veidotājā noklikšķiniet uz **Rindas definīcijas** un atveriet modificējamo rindas definīciju.</span><span class="sxs-lookup"><span data-stu-id="9754c-148">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="9754c-149">Izvēlnē **Rediģēšana** noklikšķiniet uz **Ievietot rindas no dimensijām**.</span><span class="sxs-lookup"><span data-stu-id="9754c-149">On the **Edit** menu, click **Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="9754c-150">Dialoglodziņa **Ievietot rindas no dimensijām** rindā **Dimensijas** atlasiet šūnu dimensijai, kuru pārsūtīt uz rindas definīciju, un pēc tam noklikšķiniet uz **Visas &&&**.</span><span class="sxs-lookup"><span data-stu-id="9754c-150">In the **Insert Rows from Dimensions** dialog box, in the **Dimensions** row, select the cell for the dimension to transfer to the row definition, and then click **All &&&**.</span></span>
4. <span data-ttu-id="9754c-151">Lai rindas definīcijai ļautu izmantot tikai noteiktu dimensijas vērtību diapazonu, dimensijas sākuma vērtību ievadiet šūnā **Dimensijas diapazona sākums** un pēc tam dimensijas beigu vērtību ievadiet šūnā **Dimensijas diapazona beigas**.</span><span class="sxs-lookup"><span data-stu-id="9754c-151">To limit the row definition to a specific range of dimension values, enter the starting dimension value in the **Dimension Range Start** cell, and then enter the ending dimension value in the **Dimension Range End** cell.</span></span> <span data-ttu-id="9754c-152">Lai iekļautu visas atlasītās dimensijas vērtības, atstājiet šīs šūnas tukšas.</span><span class="sxs-lookup"><span data-stu-id="9754c-152">To include all values for the selected dimension, leave these cells empty.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9754c-153">Ja dimensiju diapazonos tiek izmantotas aizstājējzīmes (\* vai ?), atkarībā no tā, kā dati tiek šķiroti ERP datu bāzē, var netikt uzrādīti visi vēlamie rezultāti.</span><span class="sxs-lookup"><span data-stu-id="9754c-153">Wildcard characters (\* or ?) in dimension ranges might not return all the results that you want, depending on how the ERP database collates data.</span></span>

5. <span data-ttu-id="9754c-154">Laukā **Sākuma rindas kods** norādiet rindas kodu pirmajai dimensijas vērtībai, kas jāpievieno rindas definīcijai.</span><span class="sxs-lookup"><span data-stu-id="9754c-154">In the **Starting row code** field, specify the row code for the first dimension value to add to the row definition.</span></span>
6. <span data-ttu-id="9754c-155">Laukā **Pieauguma solis katrā rindā** norādiet atstarpi starp secīgiem rindu kodiem.</span><span class="sxs-lookup"><span data-stu-id="9754c-155">In the **Increment each row by** field, specify the gap between consecutive row codes.</span></span> <span data-ttu-id="9754c-156">Piemēram, ja pirmās rindas kods ir 100 un pieauguma vērtība ir 30, pirmo jauno rindu kodi ir 100, 130, 160, 190 un 220.</span><span class="sxs-lookup"><span data-stu-id="9754c-156">For example, if the first row code is 100, and the increment value is 30, the first new rows have the codes 100, 130, 160, 190, and 220.</span></span> <span data-ttu-id="9754c-157">Izmantojiet pieauguma vērtību, kas nodrošina pietiekami daudz vietas jaunu formāta un formulas rindu ievietošanai.</span><span class="sxs-lookup"><span data-stu-id="9754c-157">Use an increment value that provides enough space to insert new format and formula rows.</span></span>
7. <span data-ttu-id="9754c-158">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="9754c-158">Click **OK**.</span></span> <span data-ttu-id="9754c-159">Katrai no atlasītajām dimensijas vērtībām rindas definīcijai tiek pievienota viena rinda.</span><span class="sxs-lookup"><span data-stu-id="9754c-159">For each of the selected dimension values, one line is added to the row definition.</span></span>

## <a name="adjust-rounding-in-a-row-definition"></a><span data-ttu-id="9754c-160">Noapaļošanas koriģēšana rindas definīcijā</span><span class="sxs-lookup"><span data-stu-id="9754c-160">Adjust rounding in a row definition</span></span>
<span data-ttu-id="9754c-161">Ja jums ir bilance, kur summas tiek noapaļotas, tad kopsummas var nesakrist.</span><span class="sxs-lookup"><span data-stu-id="9754c-161">If you have a balance sheet where the amounts are rounded, the totals might not balance.</span></span> <span data-ttu-id="9754c-162">Šāda problēma var rasties, ja, piemēram, jūs bilances atskaitē izmantojat noapaļošanas opciju un arī atskaites definīcijai ir norādīta noapaļošana.</span><span class="sxs-lookup"><span data-stu-id="9754c-162">This issue can occur if, for example, you use the rounding option on a balance sheet report and the report definition also specifies rounding.</span></span> <span data-ttu-id="9754c-163">Varat rindas definīcijā izmantot opciju **Noapaļošanas korekcija**, lai sabalansētu bilanču summas.</span><span class="sxs-lookup"><span data-stu-id="9754c-163">You can use the **Rounding adjustment** option in the row definition to balance the amounts in the balance sheets.</span></span> <span data-ttu-id="9754c-164">Varat noapaļošanu izslēgt vai to modificēt atskaites definīcijas cilnē **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="9754c-164">You can turn rounding off or modify it on the **Settings** tab of the report definition.</span></span> <span data-ttu-id="9754c-165">Sekojošajā tabulā redzams, kā šīs summas tiek noapaļotas.</span><span class="sxs-lookup"><span data-stu-id="9754c-165">The following table shows how amounts are rounded.</span></span> <span data-ttu-id="9754c-166">Ja noapaļošana ir ieslēgta, šīs tabulas 100. un 200. rindas kopsummas atšķiras.</span><span class="sxs-lookup"><span data-stu-id="9754c-166">In this table, the totals of rows 100 and 200 differ when rounding is turned on.</span></span>

| <span data-ttu-id="9754c-167">Rindas kods</span><span class="sxs-lookup"><span data-stu-id="9754c-167">Row code</span></span> | <span data-ttu-id="9754c-168">Summas bez noapaļošanas</span><span class="sxs-lookup"><span data-stu-id="9754c-168">Amounts without rounding</span></span> | <span data-ttu-id="9754c-169">Summa ar noapaļošanu līdz pilniem tūkstošiem</span><span class="sxs-lookup"><span data-stu-id="9754c-169">Amount with rounding to whole thousands</span></span> |
|----------|--------------------------|-----------------------------------------|
| <span data-ttu-id="9754c-170">100</span><span class="sxs-lookup"><span data-stu-id="9754c-170">100</span></span>      | <span data-ttu-id="9754c-171">3600</span><span class="sxs-lookup"><span data-stu-id="9754c-171">3,600</span></span>                    | <span data-ttu-id="9754c-172">4.</span><span class="sxs-lookup"><span data-stu-id="9754c-172">4</span></span>                                       |
| <span data-ttu-id="9754c-173">200</span><span class="sxs-lookup"><span data-stu-id="9754c-173">200</span></span>      | <span data-ttu-id="9754c-174">3700</span><span class="sxs-lookup"><span data-stu-id="9754c-174">3,700</span></span>                    | <span data-ttu-id="9754c-175">4.</span><span class="sxs-lookup"><span data-stu-id="9754c-175">4</span></span>                                       |
| <span data-ttu-id="9754c-176">KOPĀ</span><span class="sxs-lookup"><span data-stu-id="9754c-176">Total</span></span>    | <span data-ttu-id="9754c-177">7300</span><span class="sxs-lookup"><span data-stu-id="9754c-177">7,300</span></span>                    | <span data-ttu-id="9754c-178">8.</span><span class="sxs-lookup"><span data-stu-id="9754c-178">8</span></span>                                       |

<span data-ttu-id="9754c-179">Lai koriģētu bilances noapaļošanu, izpildiet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="9754c-179">To adjust rounding in a balance sheet, follow these steps.</span></span>

1. <span data-ttu-id="9754c-180">Pārskatu veidotājā noklikšķiniet uz **Rindu definīcijas** un atveriet modificējamo rindas definīciju.</span><span class="sxs-lookup"><span data-stu-id="9754c-180">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="9754c-181">Izvēlnē **Rediģēt** noklikšķiniet uz **Noapaļošanas korekcija**.</span><span class="sxs-lookup"><span data-stu-id="9754c-181">On the **Edit** menu, click **Rounding Adjustment**.</span></span>
3. <span data-ttu-id="9754c-182">Dialoglodziņā **Noapaļošanas korekcijas** ievadiet tālāk minētās vērtības.</span><span class="sxs-lookup"><span data-stu-id="9754c-182">In the **Rounding Adjustments** dialog box, enter the following values:</span></span>

    - <span data-ttu-id="9754c-183">**Noapaļošanas korekcijas rinda** — rindas kods tai rindai, kura ir jāpielāgo bilances izlīdzināšanai.</span><span class="sxs-lookup"><span data-stu-id="9754c-183">**Rounding adjustment row** – The row code for the row that should be adjusted to balance the balance sheet.</span></span>
    - <span data-ttu-id="9754c-184">**Kopējo aktīvu rinda** — rindas kods rindai bilancē, kas satur kopējo aktīvu summu.</span><span class="sxs-lookup"><span data-stu-id="9754c-184">**Total assets row** – The row code for the row in the balance sheet that contains the total assets.</span></span>
    - <span data-ttu-id="9754c-185">**Saistību un kapitāla kopsummas rinda** — rindas kods rindai bilancē, kas satur kopējo saistību un kapitāla summu.</span><span class="sxs-lookup"><span data-stu-id="9754c-185">**Total liabilities and equity row** – The row code for the row in the balance sheet that contains the total liabilities and equity.</span></span>
    - <span data-ttu-id="9754c-186">**Korekcijas summas ierobežojums** — pozitīvs vesels skaitlis, kas norāda automātisko korekciju ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="9754c-186">**Adjustment amount limit** – A positive whole number that specifies the limit on automatic adjustments.</span></span> <span data-ttu-id="9754c-187">Šī summa tiek salīdzināta ar faktiskās noapaļošanas starpības absolūto vērtību.</span><span class="sxs-lookup"><span data-stu-id="9754c-187">This amount is compared with the absolute value of the actual rounding difference.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9754c-188">Šie rindu kodi ir jāsaista ar finanšu datiem.</span><span class="sxs-lookup"><span data-stu-id="9754c-188">These row codes must be linked to your financial data.</span></span> <span data-ttu-id="9754c-189">Tas nozīmē, ka rindai šūnā **Saite uz finanšu dimensijām** ir nepieciešama dimensijas vērtība.</span><span class="sxs-lookup"><span data-stu-id="9754c-189">In other words, the row must have a dimension value in its **Link to Financial Dimensions** cell.</span></span> <span data-ttu-id="9754c-190">**Neatsaucieties** uz apraksta (**DESC**), aprēķina (**CALC**) vai kopsavilkuma (**TOT**) rindu.</span><span class="sxs-lookup"><span data-stu-id="9754c-190">Do **not** reference a description (**DESC**), calculated (**CALC**), or totaled (**TOT**) row.</span></span>

<span data-ttu-id="9754c-191">Kad noapaļošana ir ieslēgta, jūsu bilances summas tagad tiks izlīdzinātas.</span><span class="sxs-lookup"><span data-stu-id="9754c-191">The amounts in your balance sheet will now balance evenly when rounding is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="9754c-192">Korekcijas ierobežojums tiek piemērots, ņemot vērā šī pārskata definīcijai noteikto opciju **Noapaļošanas precizitāte**.</span><span class="sxs-lookup"><span data-stu-id="9754c-192">The adjustment limit is applied based on the **Rounding precision** option that is specified for the report definition.</span></span> <span data-ttu-id="9754c-193">Piemēram, ja atskaites summas noapaļojat līdz tūkstošiem un laukā **Korekcijas summas ierobežojums** ievadāt **2**, tad brīdinājuma ziņojums tiek parādīts, kad laukā **Noapaļošanas korekcijas rinda** esošā vērtība tiek palielināta vai samazināta par vairāk nekā 2000.</span><span class="sxs-lookup"><span data-stu-id="9754c-193">For example, if you round your report to thousands and enter **2** in the **Adjustment amount limit** field, you receive a warning message when the value in the **Rounding adjustment row** field increases or decreases by more than 2,000.</span></span>

## <a name="format-row-and-column-text"></a><span data-ttu-id="9754c-194">Rindu un kolonnu teksta formatēšana</span><span class="sxs-lookup"><span data-stu-id="9754c-194">Format row and column text</span></span>
<span data-ttu-id="9754c-195">Savu pārskatu izskatu varat pielāgot, mainot fontus un izmantojot teksta formatēšanu.</span><span class="sxs-lookup"><span data-stu-id="9754c-195">You can customize the appearance of your reports by changing fonts and formatting text.</span></span> <span data-ttu-id="9754c-196">Nākamajās sadaļās ir paskaidrots, kā formatēt atskaišu rindu un kolonnu izskatu.</span><span class="sxs-lookup"><span data-stu-id="9754c-196">The following sections explain how to format the appearance of rows and columns on reports.</span></span>

### <a name="manage-font-styles"></a><span data-ttu-id="9754c-197">Fontu stilu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="9754c-197">Manage font styles</span></span>

<span data-ttu-id="9754c-198">Savai atskaitei varat veidot un modificēt fontu stilus.</span><span class="sxs-lookup"><span data-stu-id="9754c-198">You can create and modify font styles for your report.</span></span> <span data-ttu-id="9754c-199">Pēc tam šos stilus varat lietot dokumentam vai konkrētai atskaites rindai vai kolonnai.</span><span class="sxs-lookup"><span data-stu-id="9754c-199">You can then apply those styles to the document, or to a specific row or column on a report.</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="9754c-200"><strong>Fonta stila izveide</strong></span><span class="sxs-lookup"><span data-stu-id="9754c-200"><strong>Create a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="9754c-201">Pārskatu veidotāja izvēlnē <strong>Formāts</strong> noklikšķiniet uz <strong>Stili un formatējums</strong>.</span><span class="sxs-lookup"><span data-stu-id="9754c-201">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="9754c-202">Dialoglodziņā <strong>Stili un formatējums</strong> noklikšķiniet uz <strong>Jauns</strong> un pēc tam ievadiet jaunā stila unikālu nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="9754c-202">In the <strong>Styles and Formatting</strong> dialog box, click <strong>New</strong>, and then enter a unique name for the new style.</span></span></li>
<li><span data-ttu-id="9754c-203">Atlasiet fontu un noklikšķiniet uz <strong>Labi</strong>.</span><span class="sxs-lookup"><span data-stu-id="9754c-203">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="9754c-204"><strong>Fonta stila modificēšana</strong></span><span class="sxs-lookup"><span data-stu-id="9754c-204"><strong>Modify a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="9754c-205">Pārskatu veidotāja izvēlnē <strong>Formāts</strong> noklikšķiniet uz <strong>Stili un formatējums</strong>.</span><span class="sxs-lookup"><span data-stu-id="9754c-205">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="9754c-206">Dialoglodziņā <strong>Stili un formatējums</strong> atlasiet modificējamo stilu un pēc tam noklikšķiniet uz <strong>Modificēt</strong>.</span><span class="sxs-lookup"><span data-stu-id="9754c-206">In the <strong>Styles and Formatting</strong> dialog box, select a style to modify, and then click <strong>Modify</strong>.</span></span></li>
<li><span data-ttu-id="9754c-207">Atlasiet fontu un noklikšķiniet uz <strong>Labi</strong>.</span><span class="sxs-lookup"><span data-stu-id="9754c-207">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="9754c-208"><strong>Fonta stila pielietošana</strong></span><span class="sxs-lookup"><span data-stu-id="9754c-208"><strong>Apply a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="9754c-209">Atskaišu veidotājā, definīcijā vai kolonnas definīcijā, vai galvenēs un kājenēs atlasiet vienu vai vairākas šūnas.</span><span class="sxs-lookup"><span data-stu-id="9754c-209">In Report Designer, in a definition or column definition, or in headers and footers, select one or more cells.</span></span></li>
<li><span data-ttu-id="9754c-210">Rīkjoslas sarakstā <strong>Stils</strong> atlasiet fonta stilu.</span><span class="sxs-lookup"><span data-stu-id="9754c-210">In the <strong>Style</strong> list on the toolbar, select a font style.</span></span></li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a><span data-ttu-id="9754c-211">Rindas teksta formatēšana</span><span class="sxs-lookup"><span data-stu-id="9754c-211">Format row text</span></span>

<span data-ttu-id="9754c-212">Rindas definīcijā norādītais formatējums ignorē visu formatējumu, kas ir norādīts kolonnas definīcijā un atskaites definīcijā.</span><span class="sxs-lookup"><span data-stu-id="9754c-212">The formatting that is specified in the row definition overrides any formatting that is specified in the column definition and the report definition.</span></span> <span data-ttu-id="9754c-213">Teksta formātu varat modificēt, izmantojot formatēšanas rīkjoslas vadīklas.</span><span class="sxs-lookup"><span data-stu-id="9754c-213">You can modify the text format by using the controls on the formatting toolbar.</span></span> <span data-ttu-id="9754c-214">Tās ir Microsoft Windows standarta vadīklas.</span><span class="sxs-lookup"><span data-stu-id="9754c-214">These controls are standard Microsoft Windows controls.</span></span>

1. <span data-ttu-id="9754c-215">Pārskatu veidotājā atveriet modificējamo rindas definīciju.</span><span class="sxs-lookup"><span data-stu-id="9754c-215">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="9754c-216">Atlasiet formatējamās šūnas.</span><span class="sxs-lookup"><span data-stu-id="9754c-216">Select the cells to format.</span></span> <span data-ttu-id="9754c-217">Lai atlasītu vairākas šūnas, atlasīšanas laikā turiet taustiņu Ctrl.</span><span class="sxs-lookup"><span data-stu-id="9754c-217">To select multiple cells, hold down the Ctrl key while you select the cell.</span></span>
3. <span data-ttu-id="9754c-218">Rīkjoslā noklikšķiniet uz nepieciešamā formāta pogas.</span><span class="sxs-lookup"><span data-stu-id="9754c-218">Click the toolbar button of the format to apply.</span></span> <span data-ttu-id="9754c-219">Piemēram, lai izveidotu rindas atkāpi, atlasiet rindu un pēc tam rīkjoslā noklikšķiniet uz **Palielināt atkāpi** ![Palielināt atkāpi](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Palielināt atkāpi").</span><span class="sxs-lookup"><span data-stu-id="9754c-219">For example, to indent a row, select the row, and then click **Increase Indent** ![Increase Indent](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Increase Indent") on the toolbar.</span></span>

### <a name="adjust-columns-while-you-design-reports"></a><span data-ttu-id="9754c-220">Kolonnu pielāgošana pārskatu veidošanas laikā</span><span class="sxs-lookup"><span data-stu-id="9754c-220">Adjust columns while you design reports</span></span>

<span data-ttu-id="9754c-221">Lai atvieglotu iespēju apskatīt kolonnas, ar kurām strādājat rindas definīcijā, varat pielāgot kolonnas platumu, ka arī paslēpt (minimizēt) vai parādīt kolonnas apskates rūtī.</span><span class="sxs-lookup"><span data-stu-id="9754c-221">To make it easier to view the columns that you're working on in the row definition, you can adjust the width of a column, and can also hide (minimize) or show columns in the view pane.</span></span> <span data-ttu-id="9754c-222">Jūsu veiktās modifikācijas ietekmē tikai kolonnu izskatu ekrānā.</span><span class="sxs-lookup"><span data-stu-id="9754c-222">The modifications that you make affect only the on-screen appearance of the columns.</span></span> <span data-ttu-id="9754c-223">Tās neietekmē šo kolonnu formatējumu atskaitēs.</span><span class="sxs-lookup"><span data-stu-id="9754c-223">They don't affect the column formatting on reports.</span></span>

### <a name="change-the-width-of-a-column-in-the-view-pane"></a><span data-ttu-id="9754c-224">Kolonnas platuma maiņa apskates rūtī</span><span class="sxs-lookup"><span data-stu-id="9754c-224">Change the width of a column in the view pane</span></span>

1. <span data-ttu-id="9754c-225">Pārskatu veidotājā atveriet modificējamo rindas definīciju.</span><span class="sxs-lookup"><span data-stu-id="9754c-225">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="9754c-226">Izvēlnē **Formāts** atlasiet **Kolonnas platums**.</span><span class="sxs-lookup"><span data-stu-id="9754c-226">On the **Format** menu, select **Column Width**.</span></span>
3. <span data-ttu-id="9754c-227">Dialoglodziņā **Kolonnas platums** ievadiet kādu vērtību un pēc tam noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="9754c-227">In the **Column Width** dialog box, enter a value, and then click **OK**.</span></span> <span data-ttu-id="9754c-228">Lai mainītu kolonnas platumu, varat arī vilkt kolonnas virsraksta šūnas labo malu.</span><span class="sxs-lookup"><span data-stu-id="9754c-228">Alternatively, you can drag the right boundary of a column heading cell to change the width of the column.</span></span>

### <a name="hide-columns-in-the-view-pane"></a><span data-ttu-id="9754c-229">Kolonnu paslēpšana apskates rūtī</span><span class="sxs-lookup"><span data-stu-id="9754c-229">Hide columns in the view pane</span></span>

1. <span data-ttu-id="9754c-230">Pārskatu veidotājā atveriet modificējamo rindas definīciju.</span><span class="sxs-lookup"><span data-stu-id="9754c-230">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="9754c-231">Atlasiet vienu vai vairākas kolonnas, ko samazināt.</span><span class="sxs-lookup"><span data-stu-id="9754c-231">Select the column or columns to minimize.</span></span>
3. <span data-ttu-id="9754c-232">Veiciet klikšķi ar peles labo pogu un tad noklikšķiniet uz **Paslēpt**.</span><span class="sxs-lookup"><span data-stu-id="9754c-232">Right-click, and then click **Hide**.</span></span>

### <a name="show-all-hidden-columns-in-the-view-pane"></a><span data-ttu-id="9754c-233">Visu paslēpto kolonnu rādīšana apskates rūtī</span><span class="sxs-lookup"><span data-stu-id="9754c-233">Show all hidden columns in the view pane</span></span>

1. <span data-ttu-id="9754c-234">Pārskatu veidotājā atveriet modificējamo rindas definīciju.</span><span class="sxs-lookup"><span data-stu-id="9754c-234">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="9754c-235">Ar peles labo pogu noklikšķiniet uz minimizētās kolonnas, kuru vēlaties parādīt, un pēc tam noklikšķiniet uz **Parādīt**.</span><span class="sxs-lookup"><span data-stu-id="9754c-235">Right-click the minimized column to display, and then click **Unhide**.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="9754c-236">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="9754c-236">Additional resources</span></span>

[<span data-ttu-id="9754c-237">Finanšu pārskati</span><span class="sxs-lookup"><span data-stu-id="9754c-237">Financial reporting</span></span>](financial-reporting-intro.md)
