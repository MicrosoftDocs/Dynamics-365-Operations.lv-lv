---
title: Papildu līgumu izveide norēķiniem, pamatojoties uz progresu
description: Šajā tēmā skaidrots, kā izveidot projektu līgumus, lai varētu ģenerēt debitoru rēķinus, pamatojoties uz pabeigto darbu procentuālo attiecību.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282837"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="f1d9b-103">Papildu līgumu izveide norēķiniem, pamatojoties uz progresu</span><span class="sxs-lookup"><span data-stu-id="f1d9b-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1d9b-104">Šajā tēmā skaidrots, kā izveidot projektu līgumus, lai varētu izveidot debitoru rēķinus, pamatojoties uz pabeigto darbu procentuālo attiecību.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="f1d9b-105">Rēķina summas tiek aprēķinātas automātiski darba budžeta kategorijām, ko iestatījāt projektam.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="f1d9b-106">Rēķinu izrakstīšanas grafiks tiek iestatīts, kad ar debitoru vienojaties par projekta līgumu.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="f1d9b-107">Izmantojiet procedūras šajā tēmā, lai uzstādītu līgumu, saistītu projektu un norēķinu nosacījumus, ko izmantot, lai aprēķinātu rēķinu summas darba budžeta kategorijām, ko esat uzstādījis projektam.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="f1d9b-108">Pēc tam, kad esat izveidojis līgumu un projektu, varat iestatīt projekta detaļas.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="f1d9b-109">Piemēram, varat definēt projekta aktivitātes un piešķirt projektam darbiniekus.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="f1d9b-110">Paraugs</span><span class="sxs-lookup"><span data-stu-id="f1d9b-110">Example</span></span>

<span data-ttu-id="f1d9b-111">Jūsu organizācija ir programmatūras izstrādes firma.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-111">Your organization is a software development firm.</span></span> <span data-ttu-id="f1d9b-112">Jūs piekrītat debitoram izstrādāt algu uzskaites pakotni par 20 000 ASV dolāru (USD) kopējo samaksu.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="f1d9b-113">Jūsu organizācija piekrīt nosūtīt debitoram rēķinu, kad pabeidzat noteiktu procentuālu daudzumu projekta darba.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="f1d9b-114">Jūs varat iestatīt šādas projekta kategorijas darbam, lai tās varētu izmantot norēķinu procesā:</span><span class="sxs-lookup"><span data-stu-id="f1d9b-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="f1d9b-115">Konsultācijas</span><span class="sxs-lookup"><span data-stu-id="f1d9b-115">Consulting</span></span>
- <span data-ttu-id="f1d9b-116">Dizains</span><span class="sxs-lookup"><span data-stu-id="f1d9b-116">Design</span></span>
- <span data-ttu-id="f1d9b-117">Instalēšana</span><span class="sxs-lookup"><span data-stu-id="f1d9b-117">Installation</span></span>

<span data-ttu-id="f1d9b-118">Iestatiet arī norēķinu nosacījumus, kas automātiski aprēķina rēķina summas procentuālajam daudzumam projekta darba, kas ir pabeigts katrā kategorijā.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="f1d9b-119">Budžeta pārvaldītājs izveido budžetu projekta kategorijām.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="f1d9b-120">Pabeigtā darba apjoms tiek automātiski aprēķināts kā faktiskā darba procentuālais apjoms salīdzinājumā ar budžetā paredzēto apjomu.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f1d9b-121">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="f1d9b-121">Prerequisites</span></span>

<span data-ttu-id="f1d9b-122">Pirms izveidojat projektu, kas izmanto norēķinu kārtulas, ir jāiestata numuru sērijas norēķinu kārtulām un papildmaksu žurnālam, ko izmanto progresa rēķinu grāmatošanai.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="f1d9b-123">Dodieties uz **Projektu vadība un uzskaite** \> **Iestatīšana** \> **Projektu vadības un uzskaites parametri**.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="f1d9b-124">Lapā **Projekta pārvaldības un uzskaites parametri** cilnē **Numuru sērijas** iestatiet numuru sēriju, ko vēlaties izmantot, izveidojot norēķinu kārtulas.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="f1d9b-125">Dodieties uz **Projekta vadība un uzskaite** \> **Žurnāli** \> **Maksa**.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="f1d9b-126">Lapā **Maksas žurnāls** atlasiet **Jauns** un ievadiet žurnāla nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="f1d9b-127">Izveidot līgumu apmaksai atbilstoši progresam</span><span class="sxs-lookup"><span data-stu-id="f1d9b-127">Create a contract for progress billings</span></span>

<span data-ttu-id="f1d9b-128">Izmantojiet šo procedūru, lai izveidotu projekta līgumu fiksētas cenas projektam.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="f1d9b-129">Jāizveido projekta rēķins, kad projektā pabeigtais darbs sasniedz norādīto procentuālo vērtību.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="f1d9b-130">Dodieties uz **Projektu vadība un uzskaite** \> **Projekti** \> **Projekta līgumi**.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="f1d9b-131">Lapā **Projekta līgumi** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="f1d9b-132">Dialoglodziņā **Jauns projekta līgums** iestatiet sekojošus laukus:</span><span class="sxs-lookup"><span data-stu-id="f1d9b-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="f1d9b-133">**Vārds/nosaukums**</span><span class="sxs-lookup"><span data-stu-id="f1d9b-133">**Name**</span></span>
    - <span data-ttu-id="f1d9b-134">**Finansējuma veids**</span><span class="sxs-lookup"><span data-stu-id="f1d9b-134">**Funding type**</span></span>
    - <span data-ttu-id="f1d9b-135">**Finansējuma avots**</span><span class="sxs-lookup"><span data-stu-id="f1d9b-135">**Funding source**</span></span>
    - <span data-ttu-id="f1d9b-136">**Pārdošanas valūta** — pēc noklusējuma šo valūtu lieto debitoru rēķiniem, kas saistīti ar projekta līgumu.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="f1d9b-137">Tomēr varat mainīt noteikta debitora rēķina pārdošanas valūtu.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="f1d9b-138">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-138">Select **OK**.</span></span> <span data-ttu-id="f1d9b-139">Informācija tiek kopēta uz lapas **Projekta līgumi** galveni.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="f1d9b-140">Lapā **Projekta līgumi** aizpildiet visu nepieciešamo projekta informāciju.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="f1d9b-141">Izveidot projektu apmaksai atbilstoši progresam</span><span class="sxs-lookup"><span data-stu-id="f1d9b-141">Create a project for progress billings</span></span>

<span data-ttu-id="f1d9b-142">Sekojiet šiem soļiem, lai izveidotu projektu un apakšprojektus, kas ir saistīti ar projekta līgumu.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="f1d9b-143">Dodieties uz **Projektu vadība un uzskaite** \> **Projekti** \> **Visi projekti**.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="f1d9b-144">Lapā **Visi projekti** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="f1d9b-145">Dialoglodziņā **Jauns projekts** laukā **Projekta veids** atlasiet **Laiks un materiāli**.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="f1d9b-146">Atlasiet projektu grupu.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-146">Select a project group.</span></span> <span data-ttu-id="f1d9b-147">Projektu grupa nosaka grupai piešķirto projektu grāmatošanas informāciju.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="f1d9b-148">Atlasiet **Izveidot projektu**.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-148">Select **Create project**.</span></span>
6. <span data-ttu-id="f1d9b-149">Kad esat izveidojis projektu, iestatiet projekta posmu kā **Notiek**.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="f1d9b-150">Izveidot budžetu projektam</span><span class="sxs-lookup"><span data-stu-id="f1d9b-150">Create a budget for a project</span></span>

<span data-ttu-id="f1d9b-151">Budžeta kategorijas tiek izmantotas, lai automātiski aprēķinātu summas par katrā kategorijā pabeigtā darba procentuālo apjomu.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="f1d9b-152">Sekojiet šiem soļiem, lai izveidotu budžeta kategorijas prognozētajām izmaksām.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="f1d9b-153">Dodieties uz **Projektu vadība un uzskaite** \> **Projekti** \> **Visi projekti**.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="f1d9b-154">Lapā **Visi projekti** atlasiet un atveriet vēlamo projektu.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="f1d9b-155">Lapā **Projekti**, kas atrodas darbības rūtī, cilnē **Plāns**, grupā **Budžets** atlasiet **Projekta budžets**.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="f1d9b-156">Lapā **Projekta budžets** ievadiet novērtētās izmaksas katrai projekta kategorijai.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="f1d9b-157">Izveidot norēķinu nosacījumus apmaksai atbilstoši progresam</span><span class="sxs-lookup"><span data-stu-id="f1d9b-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="f1d9b-158">Dodieties uz **Projektu vadība un uzskaite** \> **Projekti** \> **Projekta līgumi**.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="f1d9b-159">Lapā **Projekta līgumi** atlasiet un atveriet projekta līgumu.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="f1d9b-160">Projekta līguma lapā, kas atrodas **Norēķinu kārtulas** kopsavilkuma cilnē atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="f1d9b-161">Lapā **Norēķinu kārtula** laukā **Rindas veids** atlasiet **Progress**.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="f1d9b-162">**Norēķinu kārtulu līnijas informācija** kopsavilkuma cilnē laukā **Līguma vērtība** ievadiet līguma kopējo vērtību.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="f1d9b-163">Laukā **Kategorija** atlasiet kategoriju, uz kuru grāmatot apmaksas transakciju.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="f1d9b-164">Laukā **Projekts** atlasiet projektu, kas izmanto šo norēķinu kārtulu.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="f1d9b-165">Neobligāti: piešķirt norēķinu kārtulu papildu projektiem.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="f1d9b-166">Kopsavilkuma cilnē **Projekts** sadaļā **Pieejamie projekti** atlasiet projektu un pēc tam atlasiet labo bultiņu, lai pievienotu projektu sadaļai **Atlasītie projekti**.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="f1d9b-167">Neobligāti: aprēķiniet procentuālu vērtību, ko klients ietur no rēķina maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="f1d9b-168">Kopsavilkuma cilnē **Maksājuma ieturēšanas noteikumi** atlasiet finansējuma avotu un pēc tam laukā **Ieturēšanas procents** ievadiet ieturēšanas procentu.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="f1d9b-169">Atkārtojiet šos soļus, lai izveidotu papildu norēķinu kārtulas projekta līgumam.</span><span class="sxs-lookup"><span data-stu-id="f1d9b-169">Repeat these steps to create additional billing rules for the project contract.</span></span>
