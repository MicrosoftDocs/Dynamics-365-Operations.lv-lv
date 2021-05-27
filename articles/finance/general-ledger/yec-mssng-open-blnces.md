---
title: Gada beigu slēgšanas trūkstošās sākuma bilances
description: Šajā tēmā skaidrots, kādēļ, slēdzot gadu, var būt trūkstošas sākuma bilances, un kā atjaunot šīs bilances, ja tās iztrūkst.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 045d0bf11b11c9a353858ce3ca82c698dbceea7c
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028575"
---
# <a name="year-end-close-missing-opening-balances"></a><span data-ttu-id="357d8-103">Gada beigu slēgšanas trūkstošās sākuma bilances</span><span class="sxs-lookup"><span data-stu-id="357d8-103">Year-end close missing opening balances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="357d8-104">Šajā tēmā skaidrots, kādēļ, slēdzot gadu, var būt trūkstošas sākuma bilances, un kā atjaunot šīs bilances, ja tās iztrūkst.</span><span class="sxs-lookup"><span data-stu-id="357d8-104">This topic explains why opening balances might be missing when you close a year, and how to rebuild those balances if they are missing.</span></span>

### <a name="symptom"></a><span data-ttu-id="357d8-105">Simptoms</span><span class="sxs-lookup"><span data-stu-id="357d8-105">Symptom</span></span>

<span data-ttu-id="357d8-106">Kādēļ pēc virsgrāmatas gada beigu slēgšanas nav sākuma bilanču?</span><span class="sxs-lookup"><span data-stu-id="357d8-106">Why are there no beginning balances after running the General ledger year-end close?</span></span> 

### <a name="resolution"></a><span data-ttu-id="357d8-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="357d8-107">Resolution</span></span>

<span data-ttu-id="357d8-108">Ja virsgrāmatā gads ir slēgts un pēc tam ģenerēta apgrozījuma bilance, kas nerāda sākuma bilances nākamajam finanšu gadam, ir jāveic pārbaudes.</span><span class="sxs-lookup"><span data-stu-id="357d8-108">Here are things to check if you've closed a year in General ledger, and then generated a trial balance that doesn't display opening balances for the next fiscal year.</span></span>

<span data-ttu-id="357d8-109">Ja laukā **Atsaukt iepriekšējo slēgšanu** ir norādīta vērtība **Jā**, tiek stornēta iepriekšējā gada beigu slēgšana tam pašam finanšu gadam.</span><span class="sxs-lookup"><span data-stu-id="357d8-109">If the **Undo previous close** field is set to **Yes**, the previous year-end close for the same fiscal year is being reversed.</span></span> <span data-ttu-id="357d8-110">Ja tiek izpildīta gada beigu slēgšanas stornēšanas darbība, visi beigu bilances un sākuma bilances ieraksti tiks dzēsti, it kā gads nebūtu ticis slēgts.</span><span class="sxs-lookup"><span data-stu-id="357d8-110">When running a process to reverse the year-end close, all entries for both closing and opening balances will be deleted, as if the year had never been closed.</span></span> <span data-ttu-id="357d8-111">Arī dokumenti tiks dzēsti.</span><span class="sxs-lookup"><span data-stu-id="357d8-111">The vouchers are also deleted.</span></span> <span data-ttu-id="357d8-112">Gada beigu slēgšanas process vairs netiks automātiski atkārtoti izpildīts.</span><span class="sxs-lookup"><span data-stu-id="357d8-112">The year-end close process will not run again automatically.</span></span> <span data-ttu-id="357d8-113">Šis process ir jāsāk vēlreiz, šoreiz atjauninot opcijas **Atsaukt iepriekšējo slēgšanu** vērtību uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="357d8-113">You must start the process again, this time updating the **Undo previous close** option to **No**.</span></span>

<span data-ttu-id="357d8-114">Šis scenārijs ir iekļauts gada beigu bieži uzdoto jautājumu tēmā.</span><span class="sxs-lookup"><span data-stu-id="357d8-114">This scenario is covered in the year-end close FAQ topic.</span></span> <span data-ttu-id="357d8-115">Papildinformāciju skatiet dokumentā [Bieži uzdotie jautājumi par darbībām gada beigās](faq-year-end-activities.md).</span><span class="sxs-lookup"><span data-stu-id="357d8-115">For more information, see [Year-end activities FAQ](faq-year-end-activities.md).</span></span>

### <a name="symptom"></a><span data-ttu-id="357d8-116">Simptoms</span><span class="sxs-lookup"><span data-stu-id="357d8-116">Symptom</span></span>

<span data-ttu-id="357d8-117">Es izpildīju gada beigu slēgšanu, opcijai **Atsaukt iepriekšējo slēgšanu** norādot vērtību **Nē**, un joprojām nav sākuma bilanču manam finanšu gadam.</span><span class="sxs-lookup"><span data-stu-id="357d8-117">I ran year-end close with the **Undo previous close** option set to **No**, and I still do not have opening balances for my fiscal year.</span></span>

### <a name="resolution"></a><span data-ttu-id="357d8-118">Novēršana</span><span class="sxs-lookup"><span data-stu-id="357d8-118">Resolution</span></span>

<span data-ttu-id="357d8-119">Vispirms pārbaudiet pakešuzdevuma statusu.</span><span class="sxs-lookup"><span data-stu-id="357d8-119">First check the status of the batch job.</span></span> <span data-ttu-id="357d8-120">Gada slēgšana ietver vairākus atsevišķus uzdevumus, bet vissvarīgākā darbība ir pakešuzdevums ar uzdevuma aprakstu **Darbība 5.0.0**.</span><span class="sxs-lookup"><span data-stu-id="357d8-120">Closing a year includes a number of separate tasks, but the most critical step is the batch task with the task description **Step 5.0.0**.</span></span> <span data-ttu-id="357d8-121">Šīs darbības laikā tiek veikta sākuma transakciju grāmatošana un pēc izvēles arī slēgšanas transakciju grāmatošana virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="357d8-121">Posting the opening transactions, and optionally the closing transactions, to General ledger takes place during this step.</span></span> 

<span data-ttu-id="357d8-122">[![Pakešuzdevumu vēstures saraksts](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span><span class="sxs-lookup"><span data-stu-id="357d8-122">[![Batch history list](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span></span>

<span data-ttu-id="357d8-123">Ja šī darbība ir sekmīgi pabeigta, bet jūs neredzat sākuma bilances lapā **Apgrozījuma bilances vaicājums** (**Virsgrāmata > Vaicājumi un pārskati > Apgrozījuma bilance**), pārskatiet gada beigu slēgšanas pakešuzdevuma rezultātus, lai redzētu, vai bilances atjaunošanas darbība ir sekmīgi pabeigta.</span><span class="sxs-lookup"><span data-stu-id="357d8-123">If this step ended successfully but you don’t see opening balances on the **Trial balance inquiry** page (**General ledger > Inquires and reports > Trial balance**), review the results of the year-end close batch job to see if the Rebuild balances step completed successfully.</span></span>

<span data-ttu-id="357d8-124">[![Gada beigu slēgšanas pakešuzdevuma rezultāti](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span><span class="sxs-lookup"><span data-stu-id="357d8-124">[![Results of year-end close batch job](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span></span>

<span data-ttu-id="357d8-125">Ja šī darbība kāda iemesla dēļ nav izdevusies, sākuma (un pēc izvēles arī slēgšanas) transakcijas, visticamāk, ir sekmīgi iegrāmatotas.</span><span class="sxs-lookup"><span data-stu-id="357d8-125">If this step has failed for any reason, the opening (and optionally closing) transactions were likely posted successfully.</span></span> <span data-ttu-id="357d8-126">Varat pārbaudīt, vai virsgrāmatas darbības ir sekmīgi grāmatotas, izmantojot lapu **Dokumentu transakciju vaicājums** un norādot dokumenta numuru un datumu, kas norādīts noslēgtā gada beigu slēgšanas dialogā (**Virsgrāmata > Vaicājumi un pārskati > Dokumentu transakcijas**).</span><span class="sxs-lookup"><span data-stu-id="357d8-126">You can verify that the General ledger transactions were posted successfully using the **Voucher transactions inquiry** page by specifying the voucher number and date provided on the year-end close dialog for the year that you closed, (**General Ledger > Inquiries and reports > Voucher transactions**).</span></span>

<span data-ttu-id="357d8-127">[![Dokumentu transakciju vaicājums](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span><span class="sxs-lookup"><span data-stu-id="357d8-127">[![Voucher transactions inquiry](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span></span>

<span data-ttu-id="357d8-128">Ja ir sākuma (un pēc izvēles arī slēgšanas) dokumenti ir klātesoši, gada beigu slēgšana nav jāizpilda vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="357d8-128">If the opening (and optionally closing) vouchers are present, you don’t need to run the year-end close again.</span></span> <span data-ttu-id="357d8-129">Tā vietā skatiet nākamo sadaļu, lai uzzinātu, kā turpināt darbu.</span><span class="sxs-lookup"><span data-stu-id="357d8-129">Instead refer to the next section for information about how to move forward.</span></span>

### <a name="symptom"></a><span data-ttu-id="357d8-130">Simptoms</span><span class="sxs-lookup"><span data-stu-id="357d8-130">Symptom</span></span>

<span data-ttu-id="357d8-131">Gada beigu slēgšanas darbība “Atjaunot bilances” neizdevās — vai vēlreiz jāizpilda viss gada beigu slēgšanas process?</span><span class="sxs-lookup"><span data-stu-id="357d8-131">The “Rebuild balances” step in the year-end close failed, do I need to re-run the entire year-end close process?</span></span>

### <a name="resolution"></a><span data-ttu-id="357d8-132">Novēršana</span><span class="sxs-lookup"><span data-stu-id="357d8-132">Resolution</span></span>

<span data-ttu-id="357d8-133">Veicot bilanču atjaunošanas darbību, tiek atjauninātas virsgrāmatas bilances, kas tiek izmantotas, ģenerējot apgrozījuma bilances vaicājumu.</span><span class="sxs-lookup"><span data-stu-id="357d8-133">The Rebuild balances step updates the General ledger balances that are used when the Trial balance inquiry is generated.</span></span>  <span data-ttu-id="357d8-134">Tā ir pēdējā darbība gada beigu slēgšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="357d8-134">It is the final step in the year-end close process.</span></span>  <span data-ttu-id="357d8-135">Ja šī darbība ir vienīgā nesekmīgā darbība, virsgrāmatas transakcijas ir sekmīgi iegrāmatotas.</span><span class="sxs-lookup"><span data-stu-id="357d8-135">If this step is the only step that failed, the General ledger transactions have posted successfully.</span></span>  <span data-ttu-id="357d8-136">Gada beigu slēgšana nav jāizpilda atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="357d8-136">You do not need to run the year-end close again.</span></span> <span data-ttu-id="357d8-137">Varat izpildīt procesu bilanču manuālai atjaunošanai, izmantojot lapu **Finanšu dimensiju kopas** (**Virsgrāmata > Kontu plāns > Dimensijas > Finanšu dimensiju kopas**).</span><span class="sxs-lookup"><span data-stu-id="357d8-137">You can run the process to rebuild the balances manually using the **Financial dimension sets** page (**General ledger > Chart of accounts > Dimensions > Financial dimension sets**).</span></span>

<span data-ttu-id="357d8-138">[![Bilanču atjaunošanas poga lapā Finanšu dimensiju kopas](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span><span class="sxs-lookup"><span data-stu-id="357d8-138">[![Rebuild balances button on Financial dimension sets page](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span></span>

<span data-ttu-id="357d8-139">Ja šī darbība prasa ilgāku laiku, ieteicams pārskatīt finanšu dimensiju kopu paraugpraksi, kā aprakstīts dokumentā [Finanšu dimensiju kopu atjaunināšanas paraugprakse](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span><span class="sxs-lookup"><span data-stu-id="357d8-139">If this step takes a long time to process, we recommend reviewing the best practices for financial dimension sets as described in [Best practices for updating Financial dimension sets](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span></span> 

