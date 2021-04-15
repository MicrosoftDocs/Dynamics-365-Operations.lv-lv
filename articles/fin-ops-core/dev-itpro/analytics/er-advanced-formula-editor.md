---
title: Elektronisko pārskatu uzlabotās formulas redaktors
description: Šajā tēmā aprakstīts, kā uzlabotās formulas redaktoru var izmantot, lai konfigurētu elektronisko pārskatu (ER) modeļu kartēšanas izteiksmes un formāta komponentus.
author: NickSelin
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: d18aeedb2f21176ffe964b926168d4bf088a093b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751212"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="e4ca2-103">Elektronisko pārskatu uzlabotās formulas redaktors</span><span class="sxs-lookup"><span data-stu-id="e4ca2-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4ca2-104">Papildus [Elektronisko pārskatu](general-electronic-reporting.md) [formulas redaktoram](general-electronic-reporting-formula-designer.md) varat izmantot uzlaboto elektronisko pārskatu formulas redaktoru, lai uzlabotu elektronisko pārskatu (ER) izteiksmju konfigurēšanas pieredzi.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="e4ca2-105">Uzlabotais redaktors ir pieejams pārlūkprogrammā, un to nodrošina [Monako redaktors](https://microsoft.github.io/monaco-editor).</span><span class="sxs-lookup"><span data-stu-id="e4ca2-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="e4ca2-106">Tālāk apskatītajā tēmā ir aprakstītas visbiežāk izmantotās uzlabota redaktora funkcijas.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="e4ca2-107">Kodu autoformatējums</span><span class="sxs-lookup"><span data-stu-id="e4ca2-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="e4ca2-108">IntelliSense</span><span class="sxs-lookup"><span data-stu-id="e4ca2-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="e4ca2-109">Kodu pabeigšana</span><span class="sxs-lookup"><span data-stu-id="e4ca2-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="e4ca2-110">Kodu navigācija</span><span class="sxs-lookup"><span data-stu-id="e4ca2-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="e4ca2-111">Kodu strukturēšana</span><span class="sxs-lookup"><span data-stu-id="e4ca2-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="e4ca2-112">Meklēt un aizvietot</span><span class="sxs-lookup"><span data-stu-id="e4ca2-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="e4ca2-113">Datu ielīmēšana</span><span class="sxs-lookup"><span data-stu-id="e4ca2-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="e4ca2-114">Sintakses iekrāsošana</span><span class="sxs-lookup"><span data-stu-id="e4ca2-114">Syntax colorization</span></span>](#SyntaxColorization)

## <a name=""></a><span data-ttu-id="e4ca2-115"><a name="ActivateAdvEditor">Uzlabotās formulas redaktora aktivizēšana</a></span><span class="sxs-lookup"><span data-stu-id="e4ca2-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="e4ca2-116">Veiciet tālāk norādītās darbības, lai sāktu izmantot uzlabotās formulas redaktoru savā Microsoft Dynamics 365 Finance instancē.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="e4ca2-117">Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="e4ca2-118">Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="e4ca2-119">Dialoglodziņā **Lietotāja parametri** sadaļā **Izpildes izsekošana** iestatiet parametru **Iespējot uzlabotās formulas redaktoru** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="e4ca2-120">[![ER konfigurāciju lapa](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="e4ca2-120">[![ER configurations page](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="e4ca2-121">Ņemiet vērā, ka šis parametrs ir lietotājam raksturīgs un uzņēmumam raksturīgs.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-121">Be aware that this parameter is user specific and company specific.</span></span>

## <a name=""></a><span data-ttu-id="e4ca2-122"><a name="Autoformatting">Kodu autoformatējums</a></span><span class="sxs-lookup"><span data-stu-id="e4ca2-122"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="e4ca2-123">Kad rakstāt kompleksu izteiksmi, kas sastāv no vairākām koda rindām, jaunas ievadītas rindas atkāpe būs atbilstoša iepriekšējās rindas atkāpei.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-123">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="e4ca2-124">Varat atlasīt rindas un mainīt to atkāpes, ierakstot **Cilne** vai **Shift+Tab**.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-124">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="e4ca2-125">[![ER formulas redaktors](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="e4ca2-125">[![ER formula editor](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="e4ca2-126">Izmantojot autoformatēšanu, varat saglabāt visu izteiksmi labi formatētu, kas atvieglos turpmāku uzturēšanu un vienkāršos konfigurētās loģikas izpratni.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-126">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <a name=""></a><span data-ttu-id="e4ca2-127"><a name="IntelliSense">IntelliSense</a></span><span class="sxs-lookup"><span data-stu-id="e4ca2-127"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="e4ca2-128">Redaktors nodrošina vārdu pabeigšanu, kas palīdz ātrāk uzrakstīt izteiksmi un izvairīties no iespiedkļūdām.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-128">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="e4ca2-129">Kad sākat pievienot jaunu tekstu, redaktors automātiski piedāvā to funkciju sarakstu, kas tiek atbalstītas ER funkcijās, kuras satur ievadītās rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-129">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="e4ca2-130">Varat arī jebkurā konfigurētās izteiksmes vietā aktivizēt IntelliSense, ievadot **Ctrl+Atstarpe**.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-130">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="e4ca2-131">[![ER formulas redaktors](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="e4ca2-131">[![ER formula editor](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <a name=""></a><span data-ttu-id="e4ca2-132"><a name="CodeCompletion">Kodu pabeigšana</a></span><span class="sxs-lookup"><span data-stu-id="e4ca2-132"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="e4ca2-133">Redaktors automātiski nodrošina koda pabeigšanu, veicot tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-133">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="e4ca2-134">Ievietojot aizverošo iekavu, kad tiek ievadīta atverošā iekava, noturot kursoru iekavās.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-134">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="e4ca2-135">Ievietojot otro pēdiņu simbolu, kad tiek ierakstīts pirmais, paturot kursoru pēdiņās.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-135">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="e4ca2-136">Ievietojot otro dubultpēdiņu simbolu, kad tiek ierakstīts pirmais, paturot kursoru pēdiņās.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-136">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="e4ca2-137">[![ER formulas redaktors](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="e4ca2-137">[![ER formula editor](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="e4ca2-138">Kad norādāt uz ierakstītajam pēdiņām, šī pāra otrā iekava tiek automātiski iezīmēta, lai parādītu konstrukciju, ko tās atbalsta.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-138">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <a name=""></a><span data-ttu-id="e4ca2-139"><a name="CodeNavigation">Kodu navigācija</a></span><span class="sxs-lookup"><span data-stu-id="e4ca2-139"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="e4ca2-140">Izteiksmē nepieciešmos simbolus vai rindas var sameklēt, ievadot komandu **Doties uz**, izmantojot komandu paleti vai konteksta izvēlni.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-140">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="e4ca2-141">Piemēram, lai pārlēktu uz **8**. rindu, veiciet tālak norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-141">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="e4ca2-142">Piespiediet taustiņu kombināciju **Ctrl+G**, ievadiet vēŗtību **8** un pēc tam piespiediet taustiņu **Enter**.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-142">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="e4ca2-143">- vai -</span><span class="sxs-lookup"><span data-stu-id="e4ca2-143">-or-</span></span>

- <span data-ttu-id="e4ca2-144">Piespiediet **F1**, ierakstiet **G**, atlasiet **Doties uz rindu**, ievadiet vērtību **8** un piespiediet **Enter**.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-144">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="e4ca2-145">[![ER formulas redaktors](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="e4ca2-145">[![ER formula editor](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <a name=""></a><span data-ttu-id="e4ca2-146"><a name="CodeStructuring">Kodu strukturēšana</a></span><span class="sxs-lookup"><span data-stu-id="e4ca2-146"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="e4ca2-147">Dažu funkciju kods, piemēram [IF](er-functions-logical-if.md) vai [CASE](er-functions-logical-case.md), ir automātiski strukturēts.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-147">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="e4ca2-148">Varat izvērst un sakļaut jebkuru vai visus šī koda saliekamos reģionus, lai samazinātu izteiksmes rediģējamo daļu un koncentrētos tikai uz to koda daļu, kam jāpievērš uzmanība.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-148">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="e4ca2-149">Šim nolūkam var izmantot pārslēgšanas komandas salocīt/atlocīt.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-149">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="e4ca2-150">Piemēram, lai salocītu visus reģionus, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-150">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="e4ca2-151">Piepiediet **Ctrl+K**</span><span class="sxs-lookup"><span data-stu-id="e4ca2-151">Press **Ctrl+K**</span></span>

  <span data-ttu-id="e4ca2-152">- vai -</span><span class="sxs-lookup"><span data-stu-id="e4ca2-152">-or-</span></span>

- <span data-ttu-id="e4ca2-153">Piespiediet **F1**, piespiediet **FO**, atlasiet **Salocīt visu** un pēc tam piespiediet **Enter**</span><span class="sxs-lookup"><span data-stu-id="e4ca2-153">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="e4ca2-154">Lai salocītu visus reģionus, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-154">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="e4ca2-155">Piepiediet **Ctrl+J**</span><span class="sxs-lookup"><span data-stu-id="e4ca2-155">Press **Ctrl+J**</span></span>

  <span data-ttu-id="e4ca2-156">- vai -</span><span class="sxs-lookup"><span data-stu-id="e4ca2-156">-or-</span></span>
  
- <span data-ttu-id="e4ca2-157">Piespiediet **F1**, ierakstiet **UN**, atlasiet **Atlocīt visu** un pēc tam piespiediet **Enter**</span><span class="sxs-lookup"><span data-stu-id="e4ca2-157">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="e4ca2-158">[![ER formulas redaktors](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="e4ca2-158">[![ER formula editor](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <a name=""></a><span data-ttu-id="e4ca2-159"><a name="FindAndReplace">Meklēt un aizvietot</a></span><span class="sxs-lookup"><span data-stu-id="e4ca2-159"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="e4ca2-160">Lai atrastu konkrēta teksta gadījumus, atlasiet izteiksmē tekstu un veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-160">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="e4ca2-161">Piespiediet **Ctrl+F** un pēc tam piespiediet **F3**, lai atrastu nākamo atlasītā teksta gadījumu, vai piespiediet **Shift+F3**, lai atrastu iepriekšējo gadījumu.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-161">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="e4ca2-162">- vai -</span><span class="sxs-lookup"><span data-stu-id="e4ca2-162">-or-</span></span>
  
- <span data-ttu-id="e4ca2-163">Piespiediet **F1**, ievadiet **F** un pēc tam atlasiet nepieciešamo opciju, lai atrastu atlasīto tekstu.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-163">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="e4ca2-164">Lai aizvietotu konkrēta teksta gadījumus, atlasiet izteiksmē tekstu un veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-164">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="e4ca2-165">Piepiediet **Ctrl+H**.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-165">Press **Ctrl+H**.</span></span> <span data-ttu-id="e4ca2-166">Ievadiet alternatīvo tekstu un atlasiet aizstāšanas opciju, lai pašreizējā izteiksmē aizstātu atlasīto tekstu vai visus šī teksta gadījumus.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-166">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="e4ca2-167">- vai -</span><span class="sxs-lookup"><span data-stu-id="e4ca2-167">-or-</span></span>
  
- <span data-ttu-id="e4ca2-168">Piespiediet **F1**, ievadiet **R** un pēc tam atlasiet nepieciešamo opciju, lai aizstātu atlasīto tekstu.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-168">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="e4ca2-169">Ievadiet alternatīvo tekstu un atlasiet aizstāšanas opciju, lai pašreizējā izteiksmē aizstātu atlasīto tekstu vai visus šī teksta gadījumus.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-169">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="e4ca2-170">Lai izmainītu visus konkrēta teksta gadījumus, atlasiet izteiksmē tekstu un veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-170">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="e4ca2-171">Piespiediet **Ctrl+F2** un pēc tam ievadiet alternatīvo tekstu.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-171">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="e4ca2-172">- vai -</span><span class="sxs-lookup"><span data-stu-id="e4ca2-172">-or-</span></span>
  
- <span data-ttu-id="e4ca2-173">Piespiediet **F1**, ievadiet **C** un pēc tam atlasiet nepieciešamo opciju, lai izmainītu atlasīto tekstu.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-173">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="e4ca2-174">Ievadiet alternatīvo tekstu.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-174">Enter the alternative text.</span></span>

<span data-ttu-id="e4ca2-175">[![ER formulas redaktors](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="e4ca2-175">[![ER formula editor](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <a name=""></a><span data-ttu-id="e4ca2-176"><a name="DataPasting">Datu avoti un funkciju ielīmēšana</a></span><span class="sxs-lookup"><span data-stu-id="e4ca2-176"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="e4ca2-177">Varat atlasīt **Pievienot datu avotu**, kas Ielīmē pašreizējā izteiksmē datu avotu, kas pašlaik ir atlasīts **Datu avota** kreisajā panelī.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-177">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="e4ca2-178">Līdzīgi varat atlasīt **Pievienot funkciju**, kas ielīmē pašreizējā izteiksmē funkciju, kura pašlaik ir atlasīta **Funkciju** labajā panelī.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-178">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="e4ca2-179">Ja izmantojat ER formulas redaktoru, atlasītā funkcija vai atlasītais datu avots vienmēr tiks ielīmēts konfigurētās izteiksmes beigās.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-179">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="e4ca2-180">Ja izmantojat uzlabotās ER formulas redaktoru, atlasītā funkcija vai atlasītais datu avots var tikt ielīmēts jebkurā konfigurētās izteiksmes daļā.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-180">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="e4ca2-181">Lai norādītu, kur vēlaties ielīmēt datus, būs jāizmanto kursors.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-181">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="e4ca2-182">[![ER formulas redaktors](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="e4ca2-182">[![ER formula editor](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <a name=""></a><span data-ttu-id="e4ca2-183"><a name="SyntaxColorization">Sintakses iekrāsošana</a></span><span class="sxs-lookup"><span data-stu-id="e4ca2-183"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="e4ca2-184">Pašlaik tiek lietotas dažādas krāsas, lai iezīmētu tālāk norādītās izteiksmes daļas.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-184">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="e4ca2-185">Teksts dubultiekavās, kas var apzīmēt teksta konstantes etiķetes ID.</span><span class="sxs-lookup"><span data-stu-id="e4ca2-185">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="e4ca2-186">[![ER formulas redaktors](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="e4ca2-186">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="limitations"></a><span data-ttu-id="e4ca2-187">Ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="e4ca2-187">Limitations</span></span>

<span data-ttu-id="e4ca2-188">Redaktors pašlaik tiek atbalstīts šādās tīmekļa pārlūkprogrammās:</span><span class="sxs-lookup"><span data-stu-id="e4ca2-188">The editor is currently supported in the following web browsers:</span></span>

- <span data-ttu-id="e4ca2-189">Chrome</span><span class="sxs-lookup"><span data-stu-id="e4ca2-189">Chrome</span></span>
- <span data-ttu-id="e4ca2-190">Edge</span><span class="sxs-lookup"><span data-stu-id="e4ca2-190">Edge</span></span>
- <span data-ttu-id="e4ca2-191">Firefox</span><span class="sxs-lookup"><span data-stu-id="e4ca2-191">Firefox</span></span>
- <span data-ttu-id="e4ca2-192">Opera</span><span class="sxs-lookup"><span data-stu-id="e4ca2-192">Opera</span></span>
- <span data-ttu-id="e4ca2-193">Safari</span><span class="sxs-lookup"><span data-stu-id="e4ca2-193">Safari</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e4ca2-194">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e4ca2-194">Additional resources</span></span>

- [<span data-ttu-id="e4ca2-195">Elektronisko pārskatu veidošanas (ER) apskats</span><span class="sxs-lookup"><span data-stu-id="e4ca2-195">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="e4ca2-196">Formulu veidotājs elektronisko atskaišu veidošanā</span><span class="sxs-lookup"><span data-stu-id="e4ca2-196">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="e4ca2-197">Monako redaktors</span><span class="sxs-lookup"><span data-stu-id="e4ca2-197">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]