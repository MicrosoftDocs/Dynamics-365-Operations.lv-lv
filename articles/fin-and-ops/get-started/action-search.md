---
title: "Darbību meklēšana"
description: "Šajā rakstā ir aprakstīta darbību meklēšanas funkcionalitāte programmā Microsoft Dynamics 365 for Finance and Operations. Darbību meklēšana jums palīdz lapā atrast un izpildīt darbības."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 80beefe142eb46d7c330a472ffa594a8a35a296b
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="action-search"></a><span data-ttu-id="ebf6e-104">Darbību meklēšana</span><span class="sxs-lookup"><span data-stu-id="ebf6e-104">Action search</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="ebf6e-105">Šajā rakstā ir aprakstīta darbību meklēšanas funkcionalitāte programmā Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-105">This article describes the action search functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="ebf6e-106">Darbību meklēšana jums palīdz lapā atrast un izpildīt darbības.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-106">Action search will help you find and run actions on a page.</span></span>

<a name="introduction"></a><span data-ttu-id="ebf6e-107">Ievads</span><span class="sxs-lookup"><span data-stu-id="ebf6e-107">Introduction</span></span>
------------

<span data-ttu-id="ebf6e-108">Programmatūras Microsoft Dynamics 365 for Finance and Operations lapās galvenokārt tiek rādītas komandas darbību rūtīs, gan standarta darbību rūtī, kas ir redzama lapas augšdaļā, gan rīkjoslās, kas ir redzamas dažādās lapas sadaļās.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-108">Pages in Microsoft Dynamics 365 for Finance and Operations primarily expose commands on Action Panes, both the standard Action Pane that appears at the top of a page and the toolbars that appear in various sections of the page.</span></span> <span data-ttu-id="ebf6e-109">Iepriekšējās versijās taustiņu padomu līdzeklis jums ļauj ātri piekļūt jebkurai pogai darbību rūtī, nospiežot taustiņu Alt un pēc tam burtu sēriju.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-109">In previous versions, a Key Tips feature let you quickly access any button on an Action Pane by pressing the Alt key and then a series of letters.</span></span> 

<span data-ttu-id="ebf6e-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) Taču pašreizējā Dynamics 365 for Finance and Operations versijā vairs nav pieejami taustiņu padomi. Tie ir aizstāti ar darbību meklēšanas līdzekli.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) However, in the current version of Finance and Operations, Key Tips are no longer available but have been replaced by the action search feature.</span></span> <span data-ttu-id="ebf6e-111">Šī jaunā funkcija ļauj jums ātri meklēt un palaist pogu no jebkuras redzamas darbību rūts.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-111">This new feature lets you quickly search for and run a button from any visible Action Pane.</span></span>

## <a name="using-action-search"></a><span data-ttu-id="ebf6e-112">Darbību meklēšanas izmantošana</span><span class="sxs-lookup"><span data-stu-id="ebf6e-112">Using action search</span></span>
<span data-ttu-id="ebf6e-113">Lai izmantotu darbību meklēšanas līdzekli, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-113">To use the action search feature, follow these steps.</span></span>

1.  <span data-ttu-id="ebf6e-114">Darbību rūtī noklikšķiniet uz **darbību meklēšanas** lauka.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-114">On the Action Pane, click in the **action search** field.</span></span> <span data-ttu-id="ebf6e-115">(**Darbību meklēšanas** lauks satur lupas ikonu.)</span><span class="sxs-lookup"><span data-stu-id="ebf6e-115">(The **action search** field contains a magnifying glass icon.)</span></span>
2.  <span data-ttu-id="ebf6e-116">Ierakstiet pilnīgu vai daļēju nosaukumu tai pogai, kuru vēlaties palaist.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-116">Type all or part of the name of the button that you want to run.</span></span> <span data-ttu-id="ebf6e-117">Meklēšanu varat arī veikt, izmantojot vārdus no pogas “ceļa”.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-117">You can also search by using words from the button's "path."</span></span> <span data-ttu-id="ebf6e-118">(Plašāku informāciju skatiet šī raksta nākamajā sadaļā.) Parasti poga rezultātu saraksta augšpusē kļūst redzama, kad ir ievadītas divas līdz četras rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-118">(For more information, see the next section of this article.) Typically, a button will appear near the top of the results list after you've typed two to four characters.</span></span>
3.  <span data-ttu-id="ebf6e-119">Atrodiet un palaidiet pogu rezultātu sarakstā (izmantojot peli vai tastatūru).</span><span class="sxs-lookup"><span data-stu-id="ebf6e-119">Find and run the button in the results list (by using your mouse or keyboard).</span></span>

<span data-ttu-id="ebf6e-120">Pēc pogas palaišanas fokuss tiek atgriezts pēdējā pozīcijā lapā, tādējādi varat turpināt darbu.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-120">After the button is run, the focus is returned to your last position on the page, so that you can continue to work.</span></span> 

<span data-ttu-id="ebf6e-121">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span><span class="sxs-lookup"><span data-stu-id="ebf6e-121">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span></span>

<span data-ttu-id="ebf6e-122">Jūs varat arī sākt darbību meklēšanu, nospiežot Ctrl+/ vai Alt+Q.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-122">You can also start action search by pressing Ctrl+/ or Alt+Q.</span></span> <span data-ttu-id="ebf6e-123">Nospiediet īsinājumtaustiņus vēlreiz, lai atgrieztu fokusu pēdējā pozīcijā lapā.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-123">Press the keyboard shortcut again to return the focus to your last position on the page.</span></span>

## <a name="understanding-the-results-list"></a><span data-ttu-id="ebf6e-124">Rezultātu saraksta izprašana</span><span class="sxs-lookup"><span data-stu-id="ebf6e-124">Understanding the results list</span></span>
<span data-ttu-id="ebf6e-125">Lai pilnībā saprastu kādas pogas darbību programmatūrā Dynamics 365 for Finance and Operations, bieži vien ir jāzina šīs pogas atrašanās vieta un konteksts.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-125">Often, in Finance and Operations, you must know both the location and the context of a button to fully understand the purpose of that button.</span></span> <span data-ttu-id="ebf6e-126">Tādēļ par katru sarakstā ietverto vienumu tiek radīta papildinformācija, lai jums palīdzētu saprast, kuras tieši pogas sarakstā ir redzamas.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-126">Therefore, additional information is shown for each item in the results list, to help you understand exactly which buttons appear in the list.</span></span> <span data-ttu-id="ebf6e-127">Jo īpaši, tiek parādīts pogas "ceļš".</span><span class="sxs-lookup"><span data-stu-id="ebf6e-127">In particular, the "path" of the button is shown.</span></span> <span data-ttu-id="ebf6e-128">Šis ceļš var ietvert šādu UI elementu etiķetes, ja nepieciešams:</span><span class="sxs-lookup"><span data-stu-id="ebf6e-128">This path might include the labels of the following UI elements, as relevant:</span></span>

-   <span data-ttu-id="ebf6e-129">Cilne Darbību rūts</span><span class="sxs-lookup"><span data-stu-id="ebf6e-129">Action Pane tab</span></span>
-   <span data-ttu-id="ebf6e-130">Pogu grupa</span><span class="sxs-lookup"><span data-stu-id="ebf6e-130">Button group</span></span>
-   <span data-ttu-id="ebf6e-131">Izvēlnes poga (ja poga atrodas izvēlnes pogā)</span><span class="sxs-lookup"><span data-stu-id="ebf6e-131">Menu button (if the button is inside a menu button)</span></span>
-   <span data-ttu-id="ebf6e-132">Izvēlnes atdalītājs (ja šī poga ir iekļauta nosauktā grupā izvēlnes pogā)</span><span class="sxs-lookup"><span data-stu-id="ebf6e-132">Menu separator (if the button is inside a named group inside a menu button)</span></span>
-   <span data-ttu-id="ebf6e-133">Grupa vai cilne lapā (piemēram, kopsavilkuma cilnes nosaukums)</span><span class="sxs-lookup"><span data-stu-id="ebf6e-133">Group or tab on the page (for example, the name of a FastTab)</span></span>

<span data-ttu-id="ebf6e-134">Piemēram, jūs ievadījāt **kop** **darbību meklēšanas** laukā un tagad izskatāt rezultātu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-134">For example, you typed **tot** in the **action search** field and are now examining the results list.</span></span> <span data-ttu-id="ebf6e-135">Tiek izcelts pirmais ieraksts pogai ar nosaukumu **Kopsummas**.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-135">The first entry, for a button that is named **Totals**, is highlighted.</span></span> <span data-ttu-id="ebf6e-136">Tiek rādīts arī pogas ceļš **Pārdošanas pasūtījums** &gt; **Skatīt**.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-136">A button path of **Sales order** &gt; **View** is also shown.</span></span> <span data-ttu-id="ebf6e-137">Ceļa daļa **Pārdošanas pasūtījums** atbilst darbību rūts cilnei **Pārdošanas pasūtījums**, un ceļa daļa **Skatīt** atbilst šīs cilnes grupai **Skatīt**. Līdzīgi arī pogas **Beigu atlaide** ceļš (**Pārdot** &gt; **Aprēķināt**) jums norāda, ka šī poga atrodas darbību rūts cilnes **Pārdot** grupā **Aprēķināt**.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-137">The **Sales order** part of the path corresponds to the **Sales order** tab on the Action Pane, and the **View** part of the path corresponds to the **View** group on that tab. Similarly, the path of the **Total discount** button (**Sell** &gt; **Calculate**) informs you that this button is located in the **Calculate** group on the **Sell** tab of the Action Pane.</span></span> <span data-ttu-id="ebf6e-138">Līdz ar to šī informācija jums palīdz saprast, tieši kura poga ar darbību meklēšanu tiks aktivizēta (ja atlasāt šo pogu meklēšanas sarakstā).</span><span class="sxs-lookup"><span data-stu-id="ebf6e-138">Therefore, this information helps you understand exactly which button will be triggered by action search (if you select that button in the results list).</span></span> 

<span data-ttu-id="ebf6e-139">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span><span class="sxs-lookup"><span data-stu-id="ebf6e-139">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span></span> 

<span data-ttu-id="ebf6e-140">Iepriekšējā piemērā darbību meklēšana parādīja rezultātus no standarta darbību rūts lapas augšdaļā.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-140">In the previous example, action search showed results from the standard Action Pane at the top of a page.</span></span> <span data-ttu-id="ebf6e-141">Tomēr, darbību meklēšana rāda rezultātus arī no redzamas rīkjoslas, kas atrodas citās vietās lapā.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-141">However, action search also shows results from visible toolbars that are located in other places on the page.</span></span> <span data-ttu-id="ebf6e-142">Jūs meklējat, piemēram, pogu **Rīcībā esošie krājumi**, kura atrodas kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-142">For example, you're searching for the **On-hand inventory** button that is located on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="ebf6e-143">Šajā gadījumā pogas ceļš rezultātu sarakstā (**Pārdošanas pasūtījuma rindas** &gt; **Krājumi** &gt; **Skatīt**) jūs informē, ka šī poga atrodas zem kopsavilkuma cilnes **Pārdošanas pasūtījuma rindas** izvēlnes pogas **Krājumi** virsraksta **Skatīt**.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-143">In this case, the button path in the results list (**Sales order lines** &gt; **Inventory** &gt; **View**) informs you that this button is located under the **View** heading on the **Inventory** menu button on the **Sales order lines** FastTab.</span></span> 

<span data-ttu-id="ebf6e-144">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span><span class="sxs-lookup"><span data-stu-id="ebf6e-144">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span></span>

## <a name="action-search-vs-navigation-search"></a><span data-ttu-id="ebf6e-145">Darbību meklēšana un Navigācijas meklēšana</span><span class="sxs-lookup"><span data-stu-id="ebf6e-145">Action search vs. Navigation search</span></span>
<span data-ttu-id="ebf6e-146">Tā kā darbību meklēšana ir paredzēta darbību atrašanai un palaišanai noteiktā lapā, pastāv atsevišķa meklēšanas metode, kas ir paredzēta lapu atrašanai un pāriešanai uz tām programmatūrā Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ebf6e-146">Whereas action search is intended to find and run actions on a page, there is a separate search mechanism for finding and navigating to pages in Finance and Operations.</span></span> <span data-ttu-id="ebf6e-147">Plašāku informāciju skatiet rakstā [Navigācijas meklēšana](navigation-search.md).</span><span class="sxs-lookup"><span data-stu-id="ebf6e-147">For more information about that feature, see the [Navigation search](navigation-search.md) article.</span></span>




