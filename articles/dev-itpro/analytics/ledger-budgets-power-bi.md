---
title: "Power BI saturs Faktiski pret budžetu"
description: "Šajā tēmā ir aprakstīts Power BI saturs Faktiski pret budžetu. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti saturā, un ir sniegta informācija par satura izveidei izmantoto datu modeli un elementiem."
author: ryansandness
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: 2a0ad5af4e4d7da09690331dc9d1a51d2e97a664
ms.contentlocale: lv-lv
ms.lasthandoff: 12/01/2017

---

# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="22323-104">Power BI saturs Faktiski pret budžetu</span><span class="sxs-lookup"><span data-stu-id="22323-104">Actual vs budget Power BI content</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="22323-105">Šajā tēmā ir aprakstīts Microsoft Power BI saturs **Faktiski pret budžetu**.</span><span class="sxs-lookup"><span data-stu-id="22323-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="22323-106">Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.</span><span class="sxs-lookup"><span data-stu-id="22323-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span> 

# <a name="overview"></a><span data-ttu-id="22323-107">Pārskats</span><span class="sxs-lookup"><span data-stu-id="22323-107">Overview</span></span>

<span data-ttu-id="22323-108">Power BI saturs **Faktiski pret budžetu** tika izveidots personām, kas savā organizācijā atbild par faktiskās izpildes uzraudzīšanu salīdzinājumā ar budžetā paredzēto izpildi.</span><span class="sxs-lookup"><span data-stu-id="22323-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="22323-109">Power BI saturs **Faktiski pret budžetu** nodrošina ieskatu jūsu budžeta novirzēs.</span><span class="sxs-lookup"><span data-stu-id="22323-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="22323-110">Lai gūtu lielāku izpratni par noviržu iemeslu, budžetu pašreizējam gadam var analizēt pēc konta kategorijas, budžeta koda, galvenā konta, galvenā konta aprakstiem vai finanšu perioda.</span><span class="sxs-lookup"><span data-stu-id="22323-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span> 

# <a name="accessing-the-power-bi-content"></a><span data-ttu-id="22323-111">Piekļūšana Power BI saturam</span><span class="sxs-lookup"><span data-stu-id="22323-111">Accessing the Power BI content</span></span>
<span data-ttu-id="22323-112">Pārskati no Power BI satura pakotnes **Faktiski pret budžetu** tiek rādīti darbvietās **Virsgrāmatas budžeti un prognozes** un **CFO**.</span><span class="sxs-lookup"><span data-stu-id="22323-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

# <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="22323-113">Power BI satura pakotnē iekļautie pārskati</span><span class="sxs-lookup"><span data-stu-id="22323-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="22323-114">Nākamajā tabulā ir sniegta detalizēta informācija par rādītājiem, kas ir atrodami katrā Power BI satura **Faktiski pret budžetu** pārskata lapā.</span><span class="sxs-lookup"><span data-stu-id="22323-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="22323-115">Pārskats</span><span class="sxs-lookup"><span data-stu-id="22323-115">Report</span></span>                      | <span data-ttu-id="22323-116">Metrika</span><span class="sxs-lookup"><span data-stu-id="22323-116">Metrics</span></span> |
|-----------------------------|---------|
| <span data-ttu-id="22323-117">Izdevumi — faktisko un budžeta salīdzinājums</span><span class="sxs-lookup"><span data-stu-id="22323-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="22323-118">Kopējie izdevumi šajā gadā</span><span class="sxs-lookup"><span data-stu-id="22323-118">Total expenses this year</span></span></li><li><span data-ttu-id="22323-119">Budžeta kopējie izdevumi šajā gadā</span><span class="sxs-lookup"><span data-stu-id="22323-119">Budget total expenses this year</span></span></li></ul> |
| <span data-ttu-id="22323-120">Ieņēmumi — faktisko un budžeta salīdzinājums</span><span class="sxs-lookup"><span data-stu-id="22323-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="22323-121">Kopējie ieņēmumi šajā gadā</span><span class="sxs-lookup"><span data-stu-id="22323-121">Total revenue this year</span></span></li><li><span data-ttu-id="22323-122">Budžeta kopējie ieņēmumi šajā gadā</span><span class="sxs-lookup"><span data-stu-id="22323-122">Budget total revenue this year</span></span></li><ul> |
| <span data-ttu-id="22323-123">Izdevumi</span><span class="sxs-lookup"><span data-stu-id="22323-123">Expense</span></span>                     | <ul><li><span data-ttu-id="22323-124">Kopējie izdevumi šajā gadā</span><span class="sxs-lookup"><span data-stu-id="22323-124">Total expenses this year</span></span></li><li><span data-ttu-id="22323-125">Izdevumu mērķis, pamatojoties uz budžetu</span><span class="sxs-lookup"><span data-stu-id="22323-125">Goal for expenses based on budget</span></span> </li><ul> |
| <span data-ttu-id="22323-126">Ieņēmumi</span><span class="sxs-lookup"><span data-stu-id="22323-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="22323-127">Kopējie ieņēmumi šajā gadā</span><span class="sxs-lookup"><span data-stu-id="22323-127">Total revenue this year</span></span></li><li><span data-ttu-id="22323-128">Ieņēmumu mērķis, pamatojoties uz budžetu</span><span class="sxs-lookup"><span data-stu-id="22323-128">Goal for revenue based on budget</span></span> </li><ul> |
| <span data-ttu-id="22323-129">Neto ieņēmumi</span><span class="sxs-lookup"><span data-stu-id="22323-129">Net income</span></span>                  | <ul><li><span data-ttu-id="22323-130">Neto ieņēmumi šajā gadā</span><span class="sxs-lookup"><span data-stu-id="22323-130">Net income this year</span></span></li><li><span data-ttu-id="22323-131">Neto ieņēmumu mērķis, pamatojoties uz budžetu</span><span class="sxs-lookup"><span data-stu-id="22323-131">Goal for net income based on budget</span></span> </li><ul> |

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="22323-132">Power BI satura paplašināšana</span><span class="sxs-lookup"><span data-stu-id="22323-132">Extending the Power BI content</span></span>
<span data-ttu-id="22323-133">Izmantojot pakalpojumā Microsoft Dynamics Lifecycle Services (LCS) pieejamās satura pakotnes, varat nodrošināt lielisku analīzes funkcionalitāti personām, kuras nepierakstās programmatūrā Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="22323-133">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="22323-134">Varat izmainīt šīs satura pakotnes, tajās ietverot citus pārskatus vai vizualizācijas, un pēc tam publicēt tās savā Power BI.com nomniekā analīzes veikšanai.</span><span class="sxs-lookup"><span data-stu-id="22323-134">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="22323-135">Power BI saturs **Faktiski pret budžetu** ir atrodams LCS koplietojamo līdzekļu bibliotēkā.</span><span class="sxs-lookup"><span data-stu-id="22323-135">You can find the **Actual vs budget** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="22323-136">Papildinformāciju par to, kā lejupielādēt satura pakotni un ieviest to savā organizācijā, skatiet tēmā [Power BI saturs pakalpojumā LCS no Microsoft un jūsu partneriem](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="22323-136">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="22323-137">Power BI satura pakotnes implementēšanas demonstrāciju skatiet tēmā [Power BI saturs pakalpojumā Dynamics Lifecycle Services no Microsoft un jūsu partneriem](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).</span><span class="sxs-lookup"><span data-stu-id="22323-137">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

# <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="22323-138">Datu modeļa un elementu izprašana</span><span class="sxs-lookup"><span data-stu-id="22323-138">Understanding the data model and entities</span></span>

| <span data-ttu-id="22323-139">Elements</span><span class="sxs-lookup"><span data-stu-id="22323-139">Entity</span></span>                    | <span data-ttu-id="22323-140">Saturs</span><span class="sxs-lookup"><span data-stu-id="22323-140">Contents</span></span> |
|---------------------------|----------|
| <span data-ttu-id="22323-141">Virsgrāmatas aktivitātes</span><span class="sxs-lookup"><span data-stu-id="22323-141">General Ledger Activities</span></span> | <span data-ttu-id="22323-142">Transakciju summas virsgrāmatai</span><span class="sxs-lookup"><span data-stu-id="22323-142">Transaction amounts for the general ledger</span></span> |
| <span data-ttu-id="22323-143">Budžeta aktivitātes</span><span class="sxs-lookup"><span data-stu-id="22323-143">Budget Activities</span></span>         | <span data-ttu-id="22323-144">Transakciju summas budžeta reģistram</span><span class="sxs-lookup"><span data-stu-id="22323-144">Transaction amounts for the budget register</span></span> |
| <span data-ttu-id="22323-145">Galvenie konti</span><span class="sxs-lookup"><span data-stu-id="22323-145">Main Accounts</span></span>             | <span data-ttu-id="22323-146">Galvenie konti, pēc kuriem filtrēt pārskatus</span><span class="sxs-lookup"><span data-stu-id="22323-146">Main accounts to filter reports by</span></span> |
| <span data-ttu-id="22323-147">Finanšu kalendāri</span><span class="sxs-lookup"><span data-stu-id="22323-147">Fiscal Calendars</span></span>          | <span data-ttu-id="22323-148">Finanšu kalendāri, pēc kuriem filtrēt pārskatus</span><span class="sxs-lookup"><span data-stu-id="22323-148">Fiscal calendars to filter reports by</span></span> |
| <span data-ttu-id="22323-149">Virsgrāmatas</span><span class="sxs-lookup"><span data-stu-id="22323-149">Ledgers</span></span>                   | <span data-ttu-id="22323-150">Virsgrāmatas, ko var izmantot, lai pārskatu filtrētu pašreizējai virsgrāmatai</span><span class="sxs-lookup"><span data-stu-id="22323-150">Ledgers that can be used to filter the report to the current ledger</span></span> |
| <span data-ttu-id="22323-151">Budžetu kodi</span><span class="sxs-lookup"><span data-stu-id="22323-151">Budget Codes</span></span>              | <span data-ttu-id="22323-152">Budžetu kodi, pēc kuriem filtrēt pārskatus</span><span class="sxs-lookup"><span data-stu-id="22323-152">Budget codes to filter reports by</span></span> |
| <span data-ttu-id="22323-153">Juridiskās personas</span><span class="sxs-lookup"><span data-stu-id="22323-153">Legal Entities</span></span>            | <span data-ttu-id="22323-154">Juridiskās personas, ko var izmantot, lai pārskatu filtrētu pašreizējai juridiskajai personai</span><span class="sxs-lookup"><span data-stu-id="22323-154">Legal entities that can be used to filter the report to the current legal entity</span></span> |

