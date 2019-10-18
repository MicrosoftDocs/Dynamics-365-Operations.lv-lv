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
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184397"
---
# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="ceeae-104">Power BI satura pakotne Faktiski pret budžetu</span><span class="sxs-lookup"><span data-stu-id="ceeae-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ceeae-105">Šajā tēmā ir aprakstīta Microsoft Power BI satura pakotne **Faktiski pret budžetu**.</span><span class="sxs-lookup"><span data-stu-id="ceeae-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="ceeae-106">Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī ir sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.</span><span class="sxs-lookup"><span data-stu-id="ceeae-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="ceeae-107">Pārskats</span><span class="sxs-lookup"><span data-stu-id="ceeae-107">Overview</span></span>

<span data-ttu-id="ceeae-108">Power BI satura pakotne **Faktiski pret budžetu** ir izveidota personām, kas savā organizācijā atbild par faktiskās un budžetā paredzētās veiktspējas salīdzinājuma uzraudzību.</span><span class="sxs-lookup"><span data-stu-id="ceeae-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="ceeae-109">Power BI satura pakotne **Faktiski pret budžetu** nodrošina ieskatu budžeta novirzēs.</span><span class="sxs-lookup"><span data-stu-id="ceeae-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="ceeae-110">Lai gūtu lielāku izpratni par noviržu iemeslu, budžetu pašreizējam gadam var analizēt pēc konta kategorijas, budžeta koda, galvenā konta, galvenā konta aprakstiem vai finanšu perioda.</span><span class="sxs-lookup"><span data-stu-id="ceeae-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="ceeae-111">Piekļuve Power BI satura pakotnei</span><span class="sxs-lookup"><span data-stu-id="ceeae-111">Accessing the Power BI content</span></span>
<span data-ttu-id="ceeae-112">Power BI satura pakotnes **Faktiski pret budžetu** pārskati tiek rādīti darbvietās **Virsgrāmatas budžeti un prognozes** un **CFO**.</span><span class="sxs-lookup"><span data-stu-id="ceeae-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="ceeae-113">Power BI satura pakotnē iekļautie pārskati</span><span class="sxs-lookup"><span data-stu-id="ceeae-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="ceeae-114">Tālāk esošajā tabulā ir sniegta detalizēta informācija par rādītājiem, kas ir iekļauti katrā Power BI satura pakotnes **Faktiski pret budžetu** pārskata lapā.</span><span class="sxs-lookup"><span data-stu-id="ceeae-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="ceeae-115">Pārskats</span><span class="sxs-lookup"><span data-stu-id="ceeae-115">Report</span></span>                      | <span data-ttu-id="ceeae-116">Metrika</span><span class="sxs-lookup"><span data-stu-id="ceeae-116">Metrics</span></span>                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ceeae-117">Izdevumi — faktisko un budžeta salīdzinājums</span><span class="sxs-lookup"><span data-stu-id="ceeae-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="ceeae-118">Kopējie izdevumi šajā gadā</span><span class="sxs-lookup"><span data-stu-id="ceeae-118">Total expenses this year</span></span></li><li><span data-ttu-id="ceeae-119">Budžeta kopējie izdevumi šajā gadā</span><span class="sxs-lookup"><span data-stu-id="ceeae-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="ceeae-120">Ieņēmumi — faktisko un budžeta salīdzinājums</span><span class="sxs-lookup"><span data-stu-id="ceeae-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="ceeae-121">Kopējie ieņēmumi šajā gadā</span><span class="sxs-lookup"><span data-stu-id="ceeae-121">Total revenue this year</span></span></li><li><span data-ttu-id="ceeae-122">Budžeta kopējie ieņēmumi šajā gadā</span><span class="sxs-lookup"><span data-stu-id="ceeae-122">Budget total revenue this year</span></span></li><ul>     |
| <span data-ttu-id="ceeae-123">Izdevumi</span><span class="sxs-lookup"><span data-stu-id="ceeae-123">Expense</span></span>                     | <ul><li><span data-ttu-id="ceeae-124">Kopējie izdevumi šajā gadā</span><span class="sxs-lookup"><span data-stu-id="ceeae-124">Total expenses this year</span></span></li><li><span data-ttu-id="ceeae-125">Izdevumu mērķis, pamatojoties uz budžetu</span><span class="sxs-lookup"><span data-stu-id="ceeae-125">Goal for expenses based on budget</span></span></li><ul> |
| <span data-ttu-id="ceeae-126">Ieņēmumi</span><span class="sxs-lookup"><span data-stu-id="ceeae-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="ceeae-127">Kopējie ieņēmumi šajā gadā</span><span class="sxs-lookup"><span data-stu-id="ceeae-127">Total revenue this year</span></span></li><li><span data-ttu-id="ceeae-128">Ieņēmumu mērķis, pamatojoties uz budžetu</span><span class="sxs-lookup"><span data-stu-id="ceeae-128">Goal for revenue based on budget</span></span></li><ul>   |
| <span data-ttu-id="ceeae-129">Neto ieņēmumi</span><span class="sxs-lookup"><span data-stu-id="ceeae-129">Net income</span></span>                  | <ul><li><span data-ttu-id="ceeae-130">Neto ieņēmumi šajā gadā</span><span class="sxs-lookup"><span data-stu-id="ceeae-130">Net income this year</span></span></li><li><span data-ttu-id="ceeae-131">Neto ieņēmumu mērķis, pamatojoties uz budžetu</span><span class="sxs-lookup"><span data-stu-id="ceeae-131">Goal for net income based on budget</span></span></li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="ceeae-132">Datu modeļa un elementu izprašana</span><span class="sxs-lookup"><span data-stu-id="ceeae-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="ceeae-133">Elements</span><span class="sxs-lookup"><span data-stu-id="ceeae-133">Entity</span></span>                    | <span data-ttu-id="ceeae-134">Saturs</span><span class="sxs-lookup"><span data-stu-id="ceeae-134">Contents</span></span>                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ceeae-135">Virsgrāmatas aktivitātes</span><span class="sxs-lookup"><span data-stu-id="ceeae-135">General Ledger Activities</span></span> | <span data-ttu-id="ceeae-136">Transakciju summas virsgrāmatai</span><span class="sxs-lookup"><span data-stu-id="ceeae-136">Transaction amounts for the general ledger</span></span>                                       |
| <span data-ttu-id="ceeae-137">Budžeta aktivitātes</span><span class="sxs-lookup"><span data-stu-id="ceeae-137">Budget Activities</span></span>         | <span data-ttu-id="ceeae-138">Transakciju summas budžeta reģistram</span><span class="sxs-lookup"><span data-stu-id="ceeae-138">Transaction amounts for the budget register</span></span>                                      |
| <span data-ttu-id="ceeae-139">Galvenie konti</span><span class="sxs-lookup"><span data-stu-id="ceeae-139">Main Accounts</span></span>             | <span data-ttu-id="ceeae-140">Galvenie konti, pēc kuriem filtrēt pārskatus</span><span class="sxs-lookup"><span data-stu-id="ceeae-140">Main accounts to filter reports by</span></span>                                               |
| <span data-ttu-id="ceeae-141">Finanšu kalendāri</span><span class="sxs-lookup"><span data-stu-id="ceeae-141">Fiscal Calendars</span></span>          | <span data-ttu-id="ceeae-142">Finanšu kalendāri, pēc kuriem filtrēt pārskatus</span><span class="sxs-lookup"><span data-stu-id="ceeae-142">Fiscal calendars to filter reports by</span></span>                                            |
| <span data-ttu-id="ceeae-143">Virsgrāmatas</span><span class="sxs-lookup"><span data-stu-id="ceeae-143">Ledgers</span></span>                   | <span data-ttu-id="ceeae-144">Virsgrāmatas, ko var izmantot, lai pārskatu filtrētu pašreizējai virsgrāmatai</span><span class="sxs-lookup"><span data-stu-id="ceeae-144">Ledgers that can be used to filter the report to the current ledger</span></span>              |
| <span data-ttu-id="ceeae-145">Budžetu kodi</span><span class="sxs-lookup"><span data-stu-id="ceeae-145">Budget Codes</span></span>              | <span data-ttu-id="ceeae-146">Budžetu kodi, pēc kuriem filtrēt pārskatus</span><span class="sxs-lookup"><span data-stu-id="ceeae-146">Budget codes to filter reports by</span></span>                                                |
| <span data-ttu-id="ceeae-147">Juridiskās personas</span><span class="sxs-lookup"><span data-stu-id="ceeae-147">Legal Entities</span></span>            | <span data-ttu-id="ceeae-148">Juridiskās personas, ko var izmantot, lai pārskatu filtrētu pašreizējai juridiskajai personai</span><span class="sxs-lookup"><span data-stu-id="ceeae-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |
