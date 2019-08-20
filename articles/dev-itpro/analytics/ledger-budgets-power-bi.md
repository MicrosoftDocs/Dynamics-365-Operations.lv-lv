---
title: Power BI satura pakotne Faktiski pret budžetu
description: Šajā tēmā ir aprakstīta Power BI satura pakotne Faktiski pret budžetu. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti saturā, un ir sniegta informācija par satura izveidei izmantoto datu modeli un elementiem.
author: ryansandness
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a577ab24aaf86c1f7a22953e03f397a2e8213c78
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/02/2019
ms.locfileid: "1849435"
---
# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="07396-104">Power BI satura pakotne Faktiski pret budžetu</span><span class="sxs-lookup"><span data-stu-id="07396-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07396-105">Šajā tēmā ir aprakstīta Microsoft Power BI satura pakotne **Faktiski pret budžetu**.</span><span class="sxs-lookup"><span data-stu-id="07396-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="07396-106">Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī ir sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.</span><span class="sxs-lookup"><span data-stu-id="07396-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="07396-107">Pārskats</span><span class="sxs-lookup"><span data-stu-id="07396-107">Overview</span></span>

<span data-ttu-id="07396-108">Power BI satura pakotne **Faktiski pret budžetu** ir izveidota personām, kas savā organizācijā atbild par faktiskās un budžetā paredzētās veiktspējas salīdzinājuma uzraudzību.</span><span class="sxs-lookup"><span data-stu-id="07396-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="07396-109">Power BI satura pakotne **Faktiski pret budžetu** nodrošina ieskatu budžeta novirzēs.</span><span class="sxs-lookup"><span data-stu-id="07396-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="07396-110">Lai gūtu lielāku izpratni par noviržu iemeslu, budžetu pašreizējam gadam var analizēt pēc konta kategorijas, budžeta koda, galvenā konta, galvenā konta aprakstiem vai finanšu perioda.</span><span class="sxs-lookup"><span data-stu-id="07396-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="07396-111">Piekļuve Power BI satura pakotnei</span><span class="sxs-lookup"><span data-stu-id="07396-111">Accessing the Power BI content</span></span>
<span data-ttu-id="07396-112">Power BI satura pakotnes **Faktiski pret budžetu** pārskati tiek rādīti darbvietās **Virsgrāmatas budžeti un prognozes** un **CFO**.</span><span class="sxs-lookup"><span data-stu-id="07396-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="07396-113">Power BI satura pakotnē iekļautie pārskati</span><span class="sxs-lookup"><span data-stu-id="07396-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="07396-114">Tālāk esošajā tabulā ir sniegta detalizēta informācija par rādītājiem, kas ir iekļauti katrā Power BI satura pakotnes **Faktiski pret budžetu** pārskata lapā.</span><span class="sxs-lookup"><span data-stu-id="07396-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="07396-115">Pārskats</span><span class="sxs-lookup"><span data-stu-id="07396-115">Report</span></span>                      | <span data-ttu-id="07396-116">Metrika</span><span class="sxs-lookup"><span data-stu-id="07396-116">Metrics</span></span>                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="07396-117">Izdevumi — faktisko un budžeta salīdzinājums</span><span class="sxs-lookup"><span data-stu-id="07396-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="07396-118">Kopējie izdevumi šajā gadā</span><span class="sxs-lookup"><span data-stu-id="07396-118">Total expenses this year</span></span></li><li><span data-ttu-id="07396-119">Budžeta kopējie izdevumi šajā gadā</span><span class="sxs-lookup"><span data-stu-id="07396-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="07396-120">Ieņēmumi — faktisko un budžeta salīdzinājums</span><span class="sxs-lookup"><span data-stu-id="07396-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="07396-121">Kopējie ieņēmumi šajā gadā</span><span class="sxs-lookup"><span data-stu-id="07396-121">Total revenue this year</span></span></li><li><span data-ttu-id="07396-122">Budžeta kopējie ieņēmumi šajā gadā</span><span class="sxs-lookup"><span data-stu-id="07396-122">Budget total revenue this year</span></span></li><ul>     |
| <span data-ttu-id="07396-123">Izdevumi</span><span class="sxs-lookup"><span data-stu-id="07396-123">Expense</span></span>                     | <ul><li><span data-ttu-id="07396-124">Kopējie izdevumi šajā gadā</span><span class="sxs-lookup"><span data-stu-id="07396-124">Total expenses this year</span></span></li><li><span data-ttu-id="07396-125">Izdevumu mērķis, pamatojoties uz budžetu</span><span class="sxs-lookup"><span data-stu-id="07396-125">Goal for expenses based on budget</span></span></li><ul> |
| <span data-ttu-id="07396-126">Ieņēmumi</span><span class="sxs-lookup"><span data-stu-id="07396-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="07396-127">Kopējie ieņēmumi šajā gadā</span><span class="sxs-lookup"><span data-stu-id="07396-127">Total revenue this year</span></span></li><li><span data-ttu-id="07396-128">Ieņēmumu mērķis, pamatojoties uz budžetu</span><span class="sxs-lookup"><span data-stu-id="07396-128">Goal for revenue based on budget</span></span></li><ul>   |
| <span data-ttu-id="07396-129">Neto ieņēmumi</span><span class="sxs-lookup"><span data-stu-id="07396-129">Net income</span></span>                  | <ul><li><span data-ttu-id="07396-130">Neto ieņēmumi šajā gadā</span><span class="sxs-lookup"><span data-stu-id="07396-130">Net income this year</span></span></li><li><span data-ttu-id="07396-131">Neto ieņēmumu mērķis, pamatojoties uz budžetu</span><span class="sxs-lookup"><span data-stu-id="07396-131">Goal for net income based on budget</span></span></li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="07396-132">Datu modeļa un elementu izprašana</span><span class="sxs-lookup"><span data-stu-id="07396-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="07396-133">Elements</span><span class="sxs-lookup"><span data-stu-id="07396-133">Entity</span></span>                    | <span data-ttu-id="07396-134">Saturs</span><span class="sxs-lookup"><span data-stu-id="07396-134">Contents</span></span>                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="07396-135">Virsgrāmatas aktivitātes</span><span class="sxs-lookup"><span data-stu-id="07396-135">General Ledger Activities</span></span> | <span data-ttu-id="07396-136">Transakciju summas virsgrāmatai</span><span class="sxs-lookup"><span data-stu-id="07396-136">Transaction amounts for the general ledger</span></span>                                       |
| <span data-ttu-id="07396-137">Budžeta aktivitātes</span><span class="sxs-lookup"><span data-stu-id="07396-137">Budget Activities</span></span>         | <span data-ttu-id="07396-138">Transakciju summas budžeta reģistram</span><span class="sxs-lookup"><span data-stu-id="07396-138">Transaction amounts for the budget register</span></span>                                      |
| <span data-ttu-id="07396-139">Galvenie konti</span><span class="sxs-lookup"><span data-stu-id="07396-139">Main Accounts</span></span>             | <span data-ttu-id="07396-140">Galvenie konti, pēc kuriem filtrēt pārskatus</span><span class="sxs-lookup"><span data-stu-id="07396-140">Main accounts to filter reports by</span></span>                                               |
| <span data-ttu-id="07396-141">Finanšu kalendāri</span><span class="sxs-lookup"><span data-stu-id="07396-141">Fiscal Calendars</span></span>          | <span data-ttu-id="07396-142">Finanšu kalendāri, pēc kuriem filtrēt pārskatus</span><span class="sxs-lookup"><span data-stu-id="07396-142">Fiscal calendars to filter reports by</span></span>                                            |
| <span data-ttu-id="07396-143">Virsgrāmatas</span><span class="sxs-lookup"><span data-stu-id="07396-143">Ledgers</span></span>                   | <span data-ttu-id="07396-144">Virsgrāmatas, ko var izmantot, lai pārskatu filtrētu pašreizējai virsgrāmatai</span><span class="sxs-lookup"><span data-stu-id="07396-144">Ledgers that can be used to filter the report to the current ledger</span></span>              |
| <span data-ttu-id="07396-145">Budžetu kodi</span><span class="sxs-lookup"><span data-stu-id="07396-145">Budget Codes</span></span>              | <span data-ttu-id="07396-146">Budžetu kodi, pēc kuriem filtrēt pārskatus</span><span class="sxs-lookup"><span data-stu-id="07396-146">Budget codes to filter reports by</span></span>                                                |
| <span data-ttu-id="07396-147">Juridiskās personas</span><span class="sxs-lookup"><span data-stu-id="07396-147">Legal Entities</span></span>            | <span data-ttu-id="07396-148">Juridiskās personas, ko var izmantot, lai pārskatu filtrētu pašreizējai juridiskajai personai</span><span class="sxs-lookup"><span data-stu-id="07396-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |
