---
title: Ģenerēto ER pārskatu rezultātu izsekošanas un to salīdzināšanas ar bāzlīnijas vērtībām uzlabojumi
description: Šajā tēmā ir sniegta informācija par ER bāzlīnijas līdzekļa uzlabojumiem Microsoft Dynamics 365 for Finance and Operations versijā 10.0.3 (2019. jūnijs).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 45c0e3b569ca733ae3b70187633d2e84db5ecd87
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771170"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a><span data-ttu-id="ec18a-103">Ģenerēto ER pārskatu rezultātu izsekošanas un to salīdzināšanas ar bāzlīnijas vērtībām uzlabojumi</span><span class="sxs-lookup"><span data-stu-id="ec18a-103">Improvements in tracing the results of generated ER reports and comparing them with baseline values</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ec18a-104">Šajā tēmā ir aprakstīta pirmā uzlabojumu kopa, kas ieviesta elektronisko pārskatu veidošanas (ER) struktūras bāzlīnijas līdzeklī.</span><span class="sxs-lookup"><span data-stu-id="ec18a-104">This topic describes the first set of improvements that have been made to the baseline feature of the Electronic reporting (ER) framework.</span></span> <span data-ttu-id="ec18a-105">Šie uzlabojumi ir pieejami Microsoft Dynamics 365 for Finance and Operations versijā 10.0.3 (2019. gada jūnijs) un jaunākās versijās.</span><span class="sxs-lookup"><span data-stu-id="ec18a-105">These improvements are available in Microsoft Dynamics 365 for Finance and Operations version 10.0.3 (June 2019) and later.</span></span>

## <a name="automate-the-setting-of-baseline-rules"></a><span data-ttu-id="ec18a-106">Bāzlīnijas kārtulu iestatīšanas automatizācija</span><span class="sxs-lookup"><span data-stu-id="ec18a-106">Automate the setting of baseline rules</span></span>

<span data-ttu-id="ec18a-107">Tēmā [Ģenerēto pārskatu rezultātu izsekošana un to salīdzināšana ar bāzlīnijas vērtībām](er-trace-reports-compare-baseline.md) ir paskaidrots, kā konfigurēt ER struktūru, lai apkopotu informāciju par ER formāta izpildēm un novērtētu šo izpilžu rezultātus.</span><span class="sxs-lookup"><span data-stu-id="ec18a-107">The [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic explains how to configure the ER framework to collect information about ER format executions and evaluate the results of those executions.</span></span> <span data-ttu-id="ec18a-108">Šajā tēmā sniegtajā piemērā ir parādītas veicamās darbības.</span><span class="sxs-lookup"><span data-stu-id="ec18a-108">The example in this topic shows the steps that must be completed.</span></span>

<span data-ttu-id="ec18a-109">Tālāk ir norādītas dažas darbības.</span><span class="sxs-lookup"><span data-stu-id="ec18a-109">Here are some of the steps:</span></span>

- <span data-ttu-id="ec18a-110">Izpildiet ER formātu, lai ģenerētu izejošo failu, un saglabājiet failu lokāli.</span><span class="sxs-lookup"><span data-stu-id="ec18a-110">Run an ER format to generate an outbound file, and store the file locally.</span></span>
- <span data-ttu-id="ec18a-111">Pievienojiet lokāli saglabāto failu kā ER formātam pievienotās bāzlīnijas pielikumu.</span><span class="sxs-lookup"><span data-stu-id="ec18a-111">Add the locally stored file as an attachment of the baseline that was added for an ER format.</span></span>
- <span data-ttu-id="ec18a-112">Konfigurējiet pievienotās bāzlīnijas kārtulu.</span><span class="sxs-lookup"><span data-stu-id="ec18a-112">Configure the baseline rule for the added baseline.</span></span> <span data-ttu-id="ec18a-113">Šajā konfigurācijā ir ietvertas šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="ec18a-113">This configuration includes the following steps:</span></span>

    - <span data-ttu-id="ec18a-114">norādīt ER formāta elementu, kas tiek izmantots, lai ģenerētu izejošo failu;</span><span class="sxs-lookup"><span data-stu-id="ec18a-114">Specify an ER format element that is used to generate an outbound file.</span></span>
    - <span data-ttu-id="ec18a-115">atlasīt pielikumu, kas attiecas uz ģenerēto izejošo failu.</span><span class="sxs-lookup"><span data-stu-id="ec18a-115">Select the attachment that refers to the generated outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="ec18a-116">Šīs darbības ir jāveic manuāli, kaut arī jaunās ER iespējas ļauj tās automatizēt.</span><span class="sxs-lookup"><span data-stu-id="ec18a-116">These steps must be done manually, even though the new ER capabilities enable them to be automated.</span></span> <span data-ttu-id="ec18a-117">Lai uzzinātu vairāk par šo līdzekli, izpildiet šo piemēru.</span><span class="sxs-lookup"><span data-stu-id="ec18a-117">To learn more about this feature, complete the following example.</span></span>

## <a name="example-automate-the-setting-of-baseline-rules"></a><span data-ttu-id="ec18a-118">Piemērs: bāzlīnijas kārtulu iestatīšanas automatizācija</span><span class="sxs-lookup"><span data-stu-id="ec18a-118">Example: Automate the setting of baseline rules</span></span>

<span data-ttu-id="ec18a-119">Lai izpildītu šajā piemērā norādītās darbības, vispirms ir jāizpilda darbības, kas aprakstītas tēmā [Ģenerēto pārskatu rezultātu izsekošana un to salīdzināšana ar bāzlīnijas vērtībām](er-trace-reports-compare-baseline.md) sniegtajā piemērā, līdz sadaļai “Jaunas bāzlīnijas pievienošana izveidotam ER formātam”.</span><span class="sxs-lookup"><span data-stu-id="ec18a-119">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, up through the "Add a new baseline for a designed ER format" section.</span></span>

### <a name="review-added-baseline"></a><span data-ttu-id="ec18a-120">Pievienotas bāzlīnijas pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="ec18a-120">Review added baseline</span></span>

1. <span data-ttu-id="ec18a-121">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-121">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="ec18a-122">Atlasiet **Bāzlīnijas**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-122">Select **Baselines**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ec18a-123">Poga **Bāzlīnijas** ir pieejama tikai tad, kad ER lietotāja parametrs **Palaist atkļūdošanas režīmā** ir ieslēgts pašreizējam uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="ec18a-123">The **Baselines** button on the Action Pane is available only when the **Run in debug mode** ER user parameter is turned on for the current company.</span></span>

<span data-ttu-id="ec18a-124">Bāzlīnija tika pievienota atlasītajam formātam **Formāts ER bāzlīniju apgūšanai**, bet šai bāzlīnijai vēl nav pievienotas bāzlīnijas kārtulas.</span><span class="sxs-lookup"><span data-stu-id="ec18a-124">The baseline has been added for the selected **Format to learn ER baselines** format, but the baseline rules haven't yet been added for this baseline.</span></span>

<span data-ttu-id="ec18a-125">![Elektroniskā pārskata formāta bāzlīniju lapa](media/GER-BaselineSample-AddBaseline2.PNG "Elektronisko pārskatu formāta bāzlīniju lapu konfigurāciju ekrānuzņēmums")</span><span class="sxs-lookup"><span data-stu-id="ec18a-125">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline2.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="ec18a-126">Jaunas bāzlīnijas kārtulas izveide</span><span class="sxs-lookup"><span data-stu-id="ec18a-126">Make a new baseline rule</span></span>

1. <span data-ttu-id="ec18a-127">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-127">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="ec18a-128">Kokā izvērsiet vienumu **Modelis ER bāzlīniju apgūšanai**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-128">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="ec18a-129">Kokā atlasiet **Modelis ER bāzlīniju apgūšanai\\Formāts ER bāzlīniju apgūšanai**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-129">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="ec18a-130">Kopsavilkuma cilnē **Versijas** atlasiet **Palaist**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-130">On the **Versions** FastTab, select **Run**.</span></span>
5. <span data-ttu-id="ec18a-131">Laukā **Ievadīt ID** ievadiet **1**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-131">In the **Enter Id** field, enter **1**.</span></span>
6. <span data-ttu-id="ec18a-132">Atlasiet opcijas **Izveidot bāzlīnijas failus** iestatījumu **Jā**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-132">Set the **Make baseline files** option to **Yes**.</span></span>
7. <span data-ttu-id="ec18a-133">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-133">Select **OK**.</span></span>
8. <span data-ttu-id="ec18a-134">Atlasiet **Bāzlīnijas**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-134">Select **Baselines**.</span></span>

    <span data-ttu-id="ec18a-135">![Elektroniskā pārskata formāta bāzlīniju lapa](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Elektronisko pārskatu formāta bāzlīniju lapu konfigurāciju ekrānuzņēmums")</span><span class="sxs-lookup"><span data-stu-id="ec18a-135">![Electronic reporting format baselines page](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

    <span data-ttu-id="ec18a-136">Ģenerētais izejošais fails tiek automātiski pievienots izpildītā ER formāta bāzlīnijai.</span><span class="sxs-lookup"><span data-stu-id="ec18a-136">The generated outbound file has been automatically attached to the baseline of the executed ER format.</span></span> <span data-ttu-id="ec18a-137">Bāzlīnijas kārtula tiek automātiski pievienota šai bāzlīnijai un arī satur atsauci uz pievienoto failu.</span><span class="sxs-lookup"><span data-stu-id="ec18a-137">The baseline rule has been automatically added to this baseline and also contains the reference to the attached file.</span></span>

9. <span data-ttu-id="ec18a-138">Laukā **Nosaukums** ievadiet **1. bāzlīnija**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-138">In the **Name** field, enter **Baseline 1**.</span></span>
10. <span data-ttu-id="ec18a-139">Laukā **Faila nosaukuma maska** ievadiet **.xml**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-139">In the **File name mask** field, enter **.xml**.</span></span>
11. <span data-ttu-id="ec18a-140">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-140">Select **Save**.</span></span>

### <a name="run-the-format"></a><span data-ttu-id="ec18a-141">Formāta palaišana</span><span class="sxs-lookup"><span data-stu-id="ec18a-141">Run the format</span></span>

<span data-ttu-id="ec18a-142">Tagad varat pabeigt atlikušās piemēra darbības tēmā [Ģenerēto pārskatu rezultātu izsekošana un to salīdzināšana ar bāzlīnijas vērtībām](er-trace-reports-compare-baseline.md), sākot no sadaļas “Paredzētā ER formāta palaišana un žurnāla pārskatīšana, lai analizētu rezultātus”.</span><span class="sxs-lookup"><span data-stu-id="ec18a-142">You're now ready to complete the remaining steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, starting from the "Run the designed ER format and review the log to analyze the results" section.</span></span>

> [!NOTE]
> <span data-ttu-id="ec18a-143">Dzēšot automātiski pievienoto bāzlīnijas kārtulu kopsavilkuma cilnē **Bāzlīnijas**, pielikums ar atsauci netiek automātiski dzēsts.</span><span class="sxs-lookup"><span data-stu-id="ec18a-143">When you delete the automatically added baseline rule on the **Baselines** FastTab, the referenced attachment isn't automatically deleted.</span></span>

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="ec18a-144">Bāzlīnijas konfigurēšana, lai tā ignorētu pastāvīgi mainītās ER izvades daļas</span><span class="sxs-lookup"><span data-stu-id="ec18a-144">Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="ec18a-145">Ja ER formāts ir izstrādāts, lai ietvertu informāciju, kas, palaižot formātu, tiek mainīta, formātam ir nepieciešams izmantot ER bāzlīnijas funkciju, lai salīdzinātu ģenerētos rezultātus ar bāzlīnijas vērtībām.</span><span class="sxs-lookup"><span data-stu-id="ec18a-145">When an ER format has been designed to contain information that is changed when the format is run, the format must be required to use the ER baseline feature to compare the generated results with baseline values.</span></span> <span data-ttu-id="ec18a-146">Informācija var būt, piemēram, apstrādes datums un laiks vai ģenerēta dokumenta unikālais identifikators dažādos formātos (globāli unikālais identifikators \[GUID\] utt.).</span><span class="sxs-lookup"><span data-stu-id="ec18a-146">For example, the information might be the processing date and time or the unique identifier of a generated document in different formats (globally unique identifier \[GUID\], and so on).</span></span> <span data-ttu-id="ec18a-147">Jaunās ER iespējas ļauj konfigurēt bāzlīnijas kārtulu tā, lai tā ignorētu ER formāta maināmos elementus, kad formāts tiek palaists ar mērķi salīdzināt bāzlīnijas vērtības ar formāta izpildes rezultātiem.</span><span class="sxs-lookup"><span data-stu-id="ec18a-147">The new ER capabilities let you configure the baseline rule so that it ignores changeable elements of an ER format when the format is run with the purpose of comparing baseline values with the results of the format's execution.</span></span> <span data-ttu-id="ec18a-148">Lai uzzinātu vairāk par šo līdzekli, izpildiet šo piemēru.</span><span class="sxs-lookup"><span data-stu-id="ec18a-148">To learn more about this feature, complete the following example.</span></span>

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="ec18a-149">Piemērs: bāzlīnijas konfigurēšana, lai tā ignorētu pastāvīgi mainītās ER izvades daļas</span><span class="sxs-lookup"><span data-stu-id="ec18a-149">Example: Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="ec18a-150">Lai izpildītu šajā piemērā norādītās darbības, vispirms ir jāizpilda darbības, kas aprakstītas tēmā [Ģenerēto pārskatu rezultātu izsekošana un to salīdzināšana ar bāzlīnijas vērtībām](er-trace-reports-compare-baseline.md) sniegtajā piemērā.</span><span class="sxs-lookup"><span data-stu-id="ec18a-150">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic.</span></span>

### <a name="modify-a-configured-er-format"></a><span data-ttu-id="ec18a-151">Konfigurēta ER formāta modificēšana</span><span class="sxs-lookup"><span data-stu-id="ec18a-151">Modify a configured ER format</span></span>

1. <span data-ttu-id="ec18a-152">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-152">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="ec18a-153">Kokā izvērsiet vienumu **Modelis ER bāzlīniju apgūšanai**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-153">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="ec18a-154">Kokā atlasiet **Modelis ER bāzlīniju apgūšanai\\Formāts ER bāzlīniju apgūšanai**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-154">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="ec18a-155">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-155">Select **Designer**.</span></span>
5. <span data-ttu-id="ec18a-156">Kokā atlasiet **Izvade\\Dokuments**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-156">In the tree, select **Output\\Document**.</span></span>
6. <span data-ttu-id="ec18a-157">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-157">Select **Add**.</span></span>
7. <span data-ttu-id="ec18a-158">Nolaižamajā dialoglodziņā, kas atrodas kokā, atlasiet **XML\\Atribūts**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-158">In the drop-down dialog box, in the tree, select **XML\\Attribute**.</span></span>
8. <span data-ttu-id="ec18a-159">Laukā **Nosaukums** ievadiet **ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-159">In the **Name** field, enter **ProcessingDateTime**.</span></span>
9. <span data-ttu-id="ec18a-160">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-160">Select **OK**.</span></span>
10. <span data-ttu-id="ec18a-161">Cilnes **Kartēšana** kokā atlasiet **Izvade\\Dokuments\\ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-161">On the **Mapping** tab, in the tree, select **Output\\Document\\ProcessingDateTime**.</span></span>
11. <span data-ttu-id="ec18a-162">Atlasiet **Rediģēt formulu**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-162">Select **Edit formula**.</span></span>
12. <span data-ttu-id="ec18a-163">Laukā **Formula** ievadiet šo izteiksmi: **DATETIMEFORMAT(NOW(), "O")**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-163">In the **Formula** field, enter the following expression: **DATETIMEFORMAT(NOW(), "O")**</span></span>
13. <span data-ttu-id="ec18a-164">Atlasiet **Saglabāt** un pēc tam **Testēt**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-164">Select **Save**, and then select **Test**.</span></span>
14. <span data-ttu-id="ec18a-165">Lai testētu konfigurēto izteiksmi atkārtoti, vēlreiz atlasiet **Testēt**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-165">Select **Test** again to retest the configured expression.</span></span>

    <span data-ttu-id="ec18a-166">![Formulas veidotāja lapa](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Formulas veidotāja lapas ekrānuzņēmums")</span><span class="sxs-lookup"><span data-stu-id="ec18a-166">![Formula designer page](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Screenshot of the Formula designer page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="ec18a-167">Cilnē **Testa rezultāts** tiek parādīts, ka katru reizi, kad konfigurētā izteiksme tiek izsaukta, tā atgriež citu datuma un laika vērtību.</span><span class="sxs-lookup"><span data-stu-id="ec18a-167">The **Test result** tab shows that the configured expression returns a different date and time value whenever it's called.</span></span>

15. <span data-ttu-id="ec18a-168">Atlasiet lapu **Formulas veidotājs** un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-168">Close the **Formula designer** page, and then select **Save**.</span></span>

    <span data-ttu-id="ec18a-169">![Formāta veidotāja lapa](media/GER-BaselineSample-FormatMappingDesign2.PNG "Formāta veidotāja lapas ekrānuzņēmums")</span><span class="sxs-lookup"><span data-stu-id="ec18a-169">![Format designer page](media/GER-BaselineSample-FormatMappingDesign2.PNG "Screenshot of the Format designer page")</span></span>

16. <span data-ttu-id="ec18a-170">Aizveriet lapu **Formāta veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-170">Close the **Format designer** page.</span></span>

### <a name="remove-an-existing-baseline-rule"></a><span data-ttu-id="ec18a-171">Esošas bāzlīnijas kārtulas noņemšana</span><span class="sxs-lookup"><span data-stu-id="ec18a-171">Remove an existing baseline rule</span></span>

1. <span data-ttu-id="ec18a-172">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-172">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="ec18a-173">Atlasiet **Bāzlīnijas**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-173">Select **Baselines**.</span></span>
3. <span data-ttu-id="ec18a-174">Bāzlīniju sarakstā atlasiet bāzlīniju, kas konfigurēta formātam **Formāts ER bāzlīniju apgūšanai**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-174">In the list of baselines, select the baseline that is configured for the **Format to learn ER baselines** format.</span></span>
4. <span data-ttu-id="ec18a-175">Kopsavilkuma cilnē **Bāzlīnijas** atlasiet **Dzēst**, lai noņemtu iepriekš konfigurēto bāzlīnijas kārtulu.</span><span class="sxs-lookup"><span data-stu-id="ec18a-175">On the **Baselines** FastTab, select **Delete** to remove the baseline rule that you configured earlier.</span></span>

<span data-ttu-id="ec18a-176">![Elektroniskā pārskata formāta bāzlīniju lapa](media/GER-BaselineSample-AddBaseline3.PNG "Elektronisko pārskatu formāta bāzlīniju lapu konfigurāciju ekrānuzņēmums")</span><span class="sxs-lookup"><span data-stu-id="ec18a-176">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline3.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="define-replacements-for-bindings-of-designed-er-format"></a><span data-ttu-id="ec18a-177">Izveidotā ER formāta saistījumu aizstājēju definēšana</span><span class="sxs-lookup"><span data-stu-id="ec18a-177">Define replacements for bindings of designed ER format</span></span>

1. <span data-ttu-id="ec18a-178">Lapas **Konfigurācijas** kopsavilkuma cilnē **Aizstājēji** atlasiet **Atlasīt komponentus**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-178">On the **Configurations** page, on the **Replacements** FastTab, select **Select components**.</span></span>
2. <span data-ttu-id="ec18a-179">Formāta komponentu kokā izvērsiet **Izvade**, izvērsiet **Izvade\\Dokuments** un pēc tam atlasiet vienuma **Izvade\\Dokuments\\ProcessingDateTime** izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="ec18a-179">In the format components tree, expand **Output**, expand **Output\\Document**, and then select the check box for **Output\\Document\\ProcessingDateTime**.</span></span>
3. <span data-ttu-id="ec18a-180">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-180">Select **OK**.</span></span>

<span data-ttu-id="ec18a-181">![Elektroniskā pārskata formāta bāzlīniju lapa](media/GER-BaselineSample-AddBaseline4.PNG "Elektronisko pārskatu formāta bāzlīniju lapu konfigurāciju ekrānuzņēmums")</span><span class="sxs-lookup"><span data-stu-id="ec18a-181">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline4.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

<span data-ttu-id="ec18a-182">Atlasītais ER formāta komponents ir pievienots komponentu sarakstam kopsavilkuma cilnē **Aizstājēji**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-182">The selected ER format component has been added to the list of components on the **Replacements** FastTab.</span></span> <span data-ttu-id="ec18a-183">Kad pamata ER formāts tiek palaists atkļūdošanas režīmā, katra komponenta saistījums formātā tiek aizstāts ar saistījumu, kas redzams kolonnā **Saistīšana**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-183">When the base ER format is run in debug mode, the format's binding for each component will be replaced by the binding that is shown in the **Binding** column.</span></span> <span data-ttu-id="ec18a-184">Lai mainītu komponenta noklusējuma saistījumu, kas uzskaitīts kopsavilkuma cilnē **Aizstājēji**, atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-184">To change the default binding for a component that is listed on the **Replacements** FastTab, select **Edit**.</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="ec18a-185">Jaunas bāzlīnijas kārtulas izveide</span><span class="sxs-lookup"><span data-stu-id="ec18a-185">Make a new baseline rule</span></span>

<span data-ttu-id="ec18a-186">Izpildiet darbības, kas aprakstītas šīs tēmas sadaļā “Piemērs: bāzlīnijas kārtulu iestatīšanas automatizācija”.</span><span class="sxs-lookup"><span data-stu-id="ec18a-186">Follow the steps in the "Example: Automate the setting of baseline rules" section earlier in this topic.</span></span> <span data-ttu-id="ec18a-187">Paziņojums brīdina, ka izejošais fails ir ģenerēts, izmantojot bāzlīnijas iestatījumus, un ir notikusi formāta saistījumu piespiedu aizstāšana.</span><span class="sxs-lookup"><span data-stu-id="ec18a-187">A notification warns you that the outbound file has been generated by using baseline settings, and that a forced replacement of the format bindings has occurred.</span></span>

<span data-ttu-id="ec18a-188">![Paziņojums lapā Konfigurācijas](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Lapas Konfigurācijas paziņojuma ekrānuzņēmums")</span><span class="sxs-lookup"><span data-stu-id="ec18a-188">![Notification on the Configurations page](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Screenshot of the notification on the Configurations page")</span></span>

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a><span data-ttu-id="ec18a-189">Brīdinājumu par formāta saistījumu aizstāšanu izlaišana</span><span class="sxs-lookup"><span data-stu-id="ec18a-189">Suppress warnings about the replacement of format bindings</span></span>

<span data-ttu-id="ec18a-190">Iestatot konkrētus ER parametrus, varat izlaist paziņojumus, kas brīdina par formāta saistījumu aizstāšanu.</span><span class="sxs-lookup"><span data-stu-id="ec18a-190">By setting specific ER parameters, you can suppress notifications that warn about the replacement of format bindings.</span></span> <span data-ttu-id="ec18a-191">Šī izlaišana var noderēt, kad formāta saistījumi tiek aizstāti neuzraudzītā režīmā, izmantojot Regression Suite Automation Tool.</span><span class="sxs-lookup"><span data-stu-id="ec18a-191">This suppression can be useful when format bindings are replaced in an unattended mode by using the Regression Suite Automation Tool.</span></span> <span data-ttu-id="ec18a-192">Šajā gadījumā brīdinājumu var uzskatīt par palaista testa gadījuma kļūmi.</span><span class="sxs-lookup"><span data-stu-id="ec18a-192">In this case, the warning can be considered a failure of the test case that is running.</span></span>

1. <span data-ttu-id="ec18a-193">Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas** atlasiet vienumu **Lietotāja parametri**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-193">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
2. <span data-ttu-id="ec18a-194">Atlasiet opcijai **Izlaist bāzlīnijas brīdinājumus** iestatījumu **Jā** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-194">Set the **Suppress baseline warnings** option to **Yes**, and then select **OK**.</span></span>

### <a name="review-the-generated-baseline-file"></a><span data-ttu-id="ec18a-195">Ģenerētā bāzlīnijas faila pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="ec18a-195">Review the generated baseline file</span></span>

1. <span data-ttu-id="ec18a-196">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="ec18a-197">Atlasiet **Bāzlīnijas**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-197">Select **Baselines**.</span></span>
3. <span data-ttu-id="ec18a-198">Atlasiet **Pielikumi**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-198">Select **Attachments**.</span></span>
    > [!NOTE]
    > <span data-ttu-id="ec18a-199">Ģenerētajā failā ir ietverts apstrādes datuma un laika teksts (**"#"**) no saistījuma, kas tika konfigurēts pievienotajā bāzlīnijas kārtulā, nevis no formāta saistījuma.</span><span class="sxs-lookup"><span data-stu-id="ec18a-199">The generated file contains the processing date and time text (**"#"**) from the binding that was configured in the added baseline rule, not from the format's binding.</span></span>
    
4. <span data-ttu-id="ec18a-200">Aizveriet lapu **Pielikumi**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-200">Close the **Attachments** page.</span></span>

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a><span data-ttu-id="ec18a-201">Paredzētā ER formāta palaišana un žurnāla pārskatīšana, lai analizētu rezultātus</span><span class="sxs-lookup"><span data-stu-id="ec18a-201">Run the designed ER format and review the log to analyze the results</span></span>

1. <span data-ttu-id="ec18a-202">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-202">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="ec18a-203">Kokā izvērsiet vienumu **Modelis ER bāzlīniju apgūšanai**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-203">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="ec18a-204">Kokā atlasiet **Modelis ER bāzlīniju apgūšanai\\Formāts ER bāzlīniju apgūšanai**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-204">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="ec18a-205">Kopsavilkuma cilnē **Versijas** atlasiet **Palaist**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-205">On the **Versions** FastTab select **Run**.</span></span>
5. <span data-ttu-id="ec18a-206">Laukā **Ievadīt ID** ierakstiet **1**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-206">In the **Enter Id** field, type **1**.</span></span>
6. <span data-ttu-id="ec18a-207">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-207">Select **OK**.</span></span>
7. <span data-ttu-id="ec18a-208">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas atkļūdošanas žurnāli**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-208">Go to **Organization administration** \> **Electronic reporting** \> **Configuration debug logs**.</span></span>

<span data-ttu-id="ec18a-209">Izpildes žurnālā ir ietverta informācija par ģenerētā faila salīdzinājuma rezultātiem ar konfigurēto bāzlīniju.</span><span class="sxs-lookup"><span data-stu-id="ec18a-209">The execution log contains information about the results of the comparison of the generated file with the configured baseline.</span></span> <span data-ttu-id="ec18a-210">Žurnālā ir norādīts, ka ģenerētais fails un bāzlīnija ir vienādas, kaut arī izpildītais formāts ietver saistījumu pastāvīgi mainīgas datuma un laika vērtības ievadīšanai izejošajā failā.</span><span class="sxs-lookup"><span data-stu-id="ec18a-210">The log indicates that the generated file and the baseline are equal, even though the executed format contains the binding to enter a constantly changing date and time value in the outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="ec18a-211">Lai gan izejošais fails ir ģenerēts, izmantojot bāzlīnijas iestatījumus, kas iespējo formāta saistījumu piespiedu aizstāšanu, brīdinājumi par aizstāšanu netiek rādīti.</span><span class="sxs-lookup"><span data-stu-id="ec18a-211">Although the outbound file has been generated by using baseline settings that force the replacement of the format's bindings, you don't receive any warnings about the replacement.</span></span>

## <a name="exchange-baseline-settings-between-environments"></a><span data-ttu-id="ec18a-212">Bāzlīnijas iestatījumu apmaiņa starp vidēm</span><span class="sxs-lookup"><span data-stu-id="ec18a-212">Exchange baseline settings between environments</span></span>

### <a name="export-baseline-settings"></a><span data-ttu-id="ec18a-213">Bāzlīnijas iestatījumu eksportēšana</span><span class="sxs-lookup"><span data-stu-id="ec18a-213">Export baseline settings</span></span>

<span data-ttu-id="ec18a-214">Jaunās ER iespējas ļauj eksportēt bāzlīnijas iestatījumus atlasītajam ER formātam no pašreizējās vides un saglabāt tos kā XML failus.</span><span class="sxs-lookup"><span data-stu-id="ec18a-214">The new ER capabilities let you export baseline settings for the selected ER format from the current environment and store them as XML files.</span></span> 

<span data-ttu-id="ec18a-215">Lai eksportētu bāzlīnijas iestatījumus, lapā **Elektronisko pārskatu veidošanas formāta bāzlīnijas** atlasiet **Eksportēt**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-215">To export baseline settings, on the **Electronic reporting format baselines** page, select **Export**.</span></span>

### <a name="import-baseline-settings"></a><span data-ttu-id="ec18a-216">Importēt bāzlīnijas iestatījumus</span><span class="sxs-lookup"><span data-stu-id="ec18a-216">Import baseline settings</span></span>

<span data-ttu-id="ec18a-217">Eksportētos bāzlīnijas iestatījumus var importēt citā vidē.</span><span class="sxs-lookup"><span data-stu-id="ec18a-217">Exported baseline settings can be imported into a different environment.</span></span> <span data-ttu-id="ec18a-218">Vide vispirms ir jāimportē kā ER formāts.</span><span class="sxs-lookup"><span data-stu-id="ec18a-218">The environment must first be imported as an ER format.</span></span> <span data-ttu-id="ec18a-219">Pēc tam varat importēt bāzlīnijas iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="ec18a-219">You can then import the baseline settings.</span></span>

<span data-ttu-id="ec18a-220">Lai importētu bāzlīnijas iestatījumus no lokāli saglabāta XML faila, lapā **Elektronisko pārskatu veidošanas formāta bāzlīnijas** atlasiet **Importēt** un pēc tam atlasiet **Pārlūkot**, lai atlasītu XML failu.</span><span class="sxs-lookup"><span data-stu-id="ec18a-220">To import baseline settings from a locally stored XML file, on the **Electronic reporting format baselines** page, select **Import**, and then select **Browse** to select the XML file.</span></span>

<span data-ttu-id="ec18a-221">![Importēt bāzlīnijas iestatījumu dialoglodziņu](media/GER-BaselineSample-ImportBaseline1.PNG "Dialoglodziņa Importēt bāzlīnijas iestatījumus ekrānuzņēmums")</span><span class="sxs-lookup"><span data-stu-id="ec18a-221">![Import baseline settings dialog box](media/GER-BaselineSample-ImportBaseline1.PNG "Screenshot of the Import baseline settings dialog box")</span></span>

<span data-ttu-id="ec18a-222">Lai importētu bāzlīnijas iestatījumus no XML faila, kas saglabāts Microsoft SharePoint serverī, balstoties uz pašreizējiem dokumentu pārvaldības iestatījumiem un atlasītā dokumenta veida, lapā **Elektronisko pārskatu veidošanas formāta bāzlīnijas** atlasiet **Importēt no avota**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-222">To import baseline settings from an XML file that is stored on the Microsoft SharePoint Server, based on the current Document management settings and the selected document type, on the **Electronic reporting format baselines** page, select **Import from source**.</span></span> <span data-ttu-id="ec18a-223">Pēc tam atlasiet dokumenta veidu un XML failu.</span><span class="sxs-lookup"><span data-stu-id="ec18a-223">Then select the document type and the XML file.</span></span> <span data-ttu-id="ec18a-224">Dokumenta tips, kas nepieciešams, lai piekļūtu SharePoint mapei, ir jākonfigurē iepriekš.</span><span class="sxs-lookup"><span data-stu-id="ec18a-224">The required document type to access the SharePoint folder must be configured in advance.</span></span>

<span data-ttu-id="ec18a-225">![Dialoglodziņš Importēt no avota](media/GER-BaselineSample-ImportBaseline2.PNG "Dialoglodziņa Importēt no avota ekrānuzņēmums")</span><span class="sxs-lookup"><span data-stu-id="ec18a-225">![Import from source dialog box](media/GER-BaselineSample-ImportBaseline2.PNG "Screenshot of the Import from source dialog box")</span></span>

> [!NOTE]
> <span data-ttu-id="ec18a-226">Varat izmantot uzdevumu ierakstītāju, lai reģistrētu darbības, kas jāveic nepieciešamā dokumenta veida un faila nosaukuma atlasīšanai dialoglodziņā **Importēt no avota**.</span><span class="sxs-lookup"><span data-stu-id="ec18a-226">You can use Task recorder to record the steps for selecting the required document type and the file name in the **Import from source** dialog box.</span></span> <span data-ttu-id="ec18a-227">Šādā veidā varat saglabāt nepieciešamos bāzlīnijas iestatījumus SharePoint serverī un pēc tam automātiski importēt tos, atskaņojot uzdevuma ierakstu, kad palaižat automātiskos testus ar Regression Suite Automation Tool.</span><span class="sxs-lookup"><span data-stu-id="ec18a-227">In this way, you can keep required baseline settings on SharePoint Server and then automatically import them by playing a task recording when you run automated tests by using the Regression Suite Automation Tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ec18a-228">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ec18a-228">Additional resources</span></span>

- [<span data-ttu-id="ec18a-229">Ģenerēto pārskatu rezultātu izsekošana un to salīdzināšana ar bāzlīnijas vērtībām</span><span class="sxs-lookup"><span data-stu-id="ec18a-229">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="ec18a-230">Uzdevuma reģistrētāja resursi</span><span class="sxs-lookup"><span data-stu-id="ec18a-230">Task recorder resources</span></span>](../user-interface/task-recorder.md)
