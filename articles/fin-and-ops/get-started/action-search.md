---
title: Darbību meklēšana
description: Šajā rakstā ir aprakstīta darbības meklēšanas funkcionalitāte programmā Microsoft Dynamics 365 for Finance and Operations. Darbību meklēšana jums palīdz lapā atrast un izpildīt darbības.
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 960c715c487fbda5d93630327f07380e6d8fbd3c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547035"
---
# <a name="action-search"></a><span data-ttu-id="5c198-104">Darbību meklēšana</span><span class="sxs-lookup"><span data-stu-id="5c198-104">Action search</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c198-105">Šajā rakstā ir aprakstīta darbības meklēšanas funkcionalitāte programmā Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5c198-105">This article describes the action search functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="5c198-106">Darbību meklēšana jums palīdz lapā atrast un izpildīt darbības.</span><span class="sxs-lookup"><span data-stu-id="5c198-106">Action search will help you find and run actions on a page.</span></span>

## <a name="introduction"></a><span data-ttu-id="5c198-107">Ievads</span><span class="sxs-lookup"><span data-stu-id="5c198-107">Introduction</span></span>

<span data-ttu-id="5c198-108">Microsoft Dynamics 365 for Finance and Operations lapās komandas galvenokārt tiek rādītas darbību rūtīs, gan standarta darbību rūtī, kas ir redzama lapas augšpusē, gan rīkjoslās, kas ir redzamas dažādās lapas sadaļās.</span><span class="sxs-lookup"><span data-stu-id="5c198-108">Pages in Microsoft Dynamics 365 for Finance and Operations primarily expose commands on Action Panes, both the standard Action Pane that appears at the top of a page and the toolbars that appear in various sections of the page.</span></span> <span data-ttu-id="5c198-109">Iepriekšējās versijās taustiņu padomu līdzeklis jums ļauj ātri piekļūt jebkurai pogai darbību rūtī, nospiežot taustiņu Alt un pēc tam burtu sēriju.</span><span class="sxs-lookup"><span data-stu-id="5c198-109">In previous versions, a Key Tips feature let you quickly access any button on an Action Pane by pressing the Alt key and then a series of letters.</span></span>

<span data-ttu-id="5c198-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)</span><span class="sxs-lookup"><span data-stu-id="5c198-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)</span></span>

<span data-ttu-id="5c198-111">Taču pašreizējā Finance and Operations versijā vairs nav pieejami taustiņu padomi. Tie ir aizstāti ar darbību meklēšanas līdzekli.</span><span class="sxs-lookup"><span data-stu-id="5c198-111">However, in the current version of Finance and Operations, Key Tips are no longer available but have been replaced by the action search feature.</span></span> <span data-ttu-id="5c198-112">Šī jaunā funkcija ļauj jums ātri meklēt un palaist pogu no jebkuras redzamas darbību rūts.</span><span class="sxs-lookup"><span data-stu-id="5c198-112">This new feature lets you quickly search for and run a button from any visible Action Pane.</span></span>

## <a name="using-action-search"></a><span data-ttu-id="5c198-113">Darbību meklēšanas izmantošana</span><span class="sxs-lookup"><span data-stu-id="5c198-113">Using action search</span></span>

<span data-ttu-id="5c198-114">Lai izmantotu darbību meklēšanas līdzekli, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="5c198-114">To use the action search feature, follow these steps.</span></span>

1. <span data-ttu-id="5c198-115">Darbību rūtī noklikšķiniet uz **darbību meklēšanas** lauka.</span><span class="sxs-lookup"><span data-stu-id="5c198-115">On the Action Pane, click in the **action search** field.</span></span> <span data-ttu-id="5c198-116">(**Darbību meklēšanas** lauks satur lupas ikonu.)</span><span class="sxs-lookup"><span data-stu-id="5c198-116">(The **action search** field contains a magnifying glass icon.)</span></span>
2. <span data-ttu-id="5c198-117">Ierakstiet pilnīgu vai daļēju nosaukumu tai pogai, kuru vēlaties palaist.</span><span class="sxs-lookup"><span data-stu-id="5c198-117">Type all or part of the name of the button that you want to run.</span></span> <span data-ttu-id="5c198-118">Meklēšanu varat arī veikt, izmantojot vārdus no pogas “ceļa”.</span><span class="sxs-lookup"><span data-stu-id="5c198-118">You can also search by using words from the button's "path."</span></span> <span data-ttu-id="5c198-119">(Plašāku informāciju skatiet šī raksta nākamajā sadaļā.) Parasti poga rezultātu saraksta augšpusē kļūst redzama, kad ir ievadītas divas līdz četras rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="5c198-119">(For more information, see the next section of this article.) Typically, a button will appear near the top of the results list after you've typed two to four characters.</span></span>
3. <span data-ttu-id="5c198-120">Atrodiet un palaidiet pogu rezultātu sarakstā (izmantojot peli vai tastatūru).</span><span class="sxs-lookup"><span data-stu-id="5c198-120">Find and run the button in the results list (by using your mouse or keyboard).</span></span>

<span data-ttu-id="5c198-121">Pēc pogas palaišanas fokuss tiek atgriezts pēdējā pozīcijā lapā, tādējādi varat turpināt darbu.</span><span class="sxs-lookup"><span data-stu-id="5c198-121">After the button is run, the focus is returned to your last position on the page, so that you can continue to work.</span></span>

<span data-ttu-id="5c198-122">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span><span class="sxs-lookup"><span data-stu-id="5c198-122">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span></span>

<span data-ttu-id="5c198-123">Jūs varat arī sākt darbību meklēšanu, nospiežot Ctrl+/ vai Alt+Q.</span><span class="sxs-lookup"><span data-stu-id="5c198-123">You can also start action search by pressing Ctrl+/ or Alt+Q.</span></span> <span data-ttu-id="5c198-124">Nospiediet īsinājumtaustiņus vēlreiz, lai atgrieztu fokusu pēdējā pozīcijā lapā.</span><span class="sxs-lookup"><span data-stu-id="5c198-124">Press the keyboard shortcut again to return the focus to your last position on the page.</span></span>

## <a name="understanding-the-results-list"></a><span data-ttu-id="5c198-125">Rezultātu saraksta izprašana</span><span class="sxs-lookup"><span data-stu-id="5c198-125">Understanding the results list</span></span>

<span data-ttu-id="5c198-126">Lai pilnībā saprastu kādas pogas darbību programmatūrā Dynamics 365 for Finance and Operations, bieži vien ir jāzina šīs pogas atrašanās vieta un konteksts.</span><span class="sxs-lookup"><span data-stu-id="5c198-126">Often, in Finance and Operations, you must know both the location and the context of a button to fully understand the purpose of that button.</span></span> <span data-ttu-id="5c198-127">Tādēļ par katru sarakstā ietverto vienumu tiek radīta papildinformācija, lai jums palīdzētu saprast, kuras tieši pogas sarakstā ir redzamas.</span><span class="sxs-lookup"><span data-stu-id="5c198-127">Therefore, additional information is shown for each item in the results list, to help you understand exactly which buttons appear in the list.</span></span> <span data-ttu-id="5c198-128">Jo īpaši, tiek parādīts pogas "ceļš".</span><span class="sxs-lookup"><span data-stu-id="5c198-128">In particular, the "path" of the button is shown.</span></span> <span data-ttu-id="5c198-129">Šis ceļš var ietvert šādu UI elementu etiķetes, ja nepieciešams:</span><span class="sxs-lookup"><span data-stu-id="5c198-129">This path might include the labels of the following UI elements, as relevant:</span></span>

- <span data-ttu-id="5c198-130">Cilne Darbību rūts</span><span class="sxs-lookup"><span data-stu-id="5c198-130">Action Pane tab</span></span>
- <span data-ttu-id="5c198-131">Pogu grupa</span><span class="sxs-lookup"><span data-stu-id="5c198-131">Button group</span></span>
- <span data-ttu-id="5c198-132">Izvēlnes poga (ja poga atrodas izvēlnes pogā)</span><span class="sxs-lookup"><span data-stu-id="5c198-132">Menu button (if the button is inside a menu button)</span></span>
- <span data-ttu-id="5c198-133">Izvēlnes atdalītājs (ja šī poga ir iekļauta nosauktā grupā izvēlnes pogā)</span><span class="sxs-lookup"><span data-stu-id="5c198-133">Menu separator (if the button is inside a named group inside a menu button)</span></span>
- <span data-ttu-id="5c198-134">Grupa vai cilne lapā (piemēram, kopsavilkuma cilnes nosaukums)</span><span class="sxs-lookup"><span data-stu-id="5c198-134">Group or tab on the page (for example, the name of a FastTab)</span></span>

<span data-ttu-id="5c198-135">Piemēram, jūs ievadījāt **kop** **darbību meklēšanas** laukā un tagad izskatāt rezultātu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="5c198-135">For example, you typed **tot** in the **action search** field and are now examining the results list.</span></span> <span data-ttu-id="5c198-136">Tiek izcelts pirmais ieraksts pogai ar nosaukumu **Kopsummas**.</span><span class="sxs-lookup"><span data-stu-id="5c198-136">The first entry, for a button that is named **Totals**, is highlighted.</span></span> <span data-ttu-id="5c198-137">Tiek rādīts arī pogas ceļš **Pārdošanas pasūtījums** &gt; **Skatīt**.</span><span class="sxs-lookup"><span data-stu-id="5c198-137">A button path of **Sales order** &gt; **View** is also shown.</span></span> <span data-ttu-id="5c198-138">Ceļa daļa **Pārdošanas pasūtījums** atbilst darbību rūts cilnei **Pārdošanas pasūtījums**, un ceļa daļa **Skatīt** atbilst šīs cilnes grupai **Skatīt**. Līdzīgi arī pogas **Beigu atlaide** ceļš (**Pārdot** &gt; **Aprēķināt**) jums norāda, ka šī poga atrodas darbību rūts cilnes **Pārdot** grupā **Aprēķināt**.</span><span class="sxs-lookup"><span data-stu-id="5c198-138">The **Sales order** part of the path corresponds to the **Sales order** tab on the Action Pane, and the **View** part of the path corresponds to the **View** group on that tab. Similarly, the path of the **Total discount** button (**Sell** &gt; **Calculate**) informs you that this button is located in the **Calculate** group on the **Sell** tab of the Action Pane.</span></span> <span data-ttu-id="5c198-139">Līdz ar to šī informācija jums palīdz saprast, tieši kura poga ar darbību meklēšanu tiks aktivizēta (ja atlasāt šo pogu meklēšanas sarakstā).</span><span class="sxs-lookup"><span data-stu-id="5c198-139">Therefore, this information helps you understand exactly which button will be triggered by action search (if you select that button in the results list).</span></span>

<span data-ttu-id="5c198-140">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span><span class="sxs-lookup"><span data-stu-id="5c198-140">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span></span>

<span data-ttu-id="5c198-141">Iepriekšējā piemērā darbību meklēšana parādīja rezultātus no standarta darbību rūts lapas augšdaļā.</span><span class="sxs-lookup"><span data-stu-id="5c198-141">In the previous example, action search showed results from the standard Action Pane at the top of a page.</span></span> <span data-ttu-id="5c198-142">Tomēr, darbību meklēšana rāda rezultātus arī no redzamas rīkjoslas, kas atrodas citās vietās lapā.</span><span class="sxs-lookup"><span data-stu-id="5c198-142">However, action search also shows results from visible toolbars that are located in other places on the page.</span></span> <span data-ttu-id="5c198-143">Jūs meklējat, piemēram, pogu **Rīcībā esošie krājumi**, kura atrodas kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="5c198-143">For example, you're searching for the **On-hand inventory** button that is located on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="5c198-144">Šajā gadījumā pogas ceļš rezultātu sarakstā (**Pārdošanas pasūtījuma rindas** &gt; **Krājumi** &gt; **Skatīt**) jūs informē, ka šī poga atrodas zem kopsavilkuma cilnes **Pārdošanas pasūtījuma rindas** izvēlnes pogas **Krājumi** virsraksta **Skatīt**.</span><span class="sxs-lookup"><span data-stu-id="5c198-144">In this case, the button path in the results list (**Sales order lines** &gt; **Inventory** &gt; **View**) informs you that this button is located under the **View** heading on the **Inventory** menu button on the **Sales order lines** FastTab.</span></span>

<span data-ttu-id="5c198-145">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span><span class="sxs-lookup"><span data-stu-id="5c198-145">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span></span>

## <a name="action-search-vs-navigation-search"></a><span data-ttu-id="5c198-146">Darbību meklēšana un Navigācijas meklēšana</span><span class="sxs-lookup"><span data-stu-id="5c198-146">Action search vs. Navigation search</span></span>

<span data-ttu-id="5c198-147">Tā kā darbību meklēšana ir paredzēta darbību atrašanai un palaišanai noteiktā lapā, pastāv atsevišķa meklēšanas metode, kas ir paredzēta lapu atrašanai un pāriešanai uz tām programmatūrā Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5c198-147">Whereas action search is intended to find and run actions on a page, there is a separate search mechanism for finding and navigating to pages in Finance and Operations.</span></span> <span data-ttu-id="5c198-148">Plašāku informāciju skatiet rakstā [Navigācijas meklēšana](navigation-search.md).</span><span class="sxs-lookup"><span data-stu-id="5c198-148">For more information about that feature, see the [Navigation search](navigation-search.md) article.</span></span>