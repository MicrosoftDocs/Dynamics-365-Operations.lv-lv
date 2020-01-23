---
title: Integrētā virsgrāmata
description: Šajā tēmā ir aprakstīta virsgrāmatas datu integrācija starp Finance and Operations un citām Dynamics 365 programmām, izmantojot Common Data Service.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 4a0a8f2f52cf9a73efc3557b63793201a7a3f8b8
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853886"
---
# <a name="integrated-ledger"></a><span data-ttu-id="2da3c-103">Integrētā virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="2da3c-103">Integrated ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2da3c-104">Biznesa programmā virsgrāmatas dati definē pamata iestatījumus tam, kā uzņēmums darbojas.</span><span class="sxs-lookup"><span data-stu-id="2da3c-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="2da3c-105">Piemēram, virsgrāmatas datos ir aprakstīts finanšu gads, ko uzņēmums ievēro, valūtas, kurās tas veic darījumus, un konti, ko tas izmanto.</span><span class="sxs-lookup"><span data-stu-id="2da3c-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="2da3c-106">Šī tēma apraksta šo pamata finanšu datu integrēšanu.</span><span class="sxs-lookup"><span data-stu-id="2da3c-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="2da3c-107">Veidnes</span><span class="sxs-lookup"><span data-stu-id="2da3c-107">Templates</span></span>

<span data-ttu-id="2da3c-108">Virsgrāmatas dati ietver pamata finanšu elementa karšu vākšanu, kas darbojas kopā debitora datu mijiedarbības laikā, kā redzams nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="2da3c-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="2da3c-109">Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="2da3c-109">Finance and Operations apps</span></span>      | <span data-ttu-id="2da3c-110">Citas Dynamics 365 programmas</span><span class="sxs-lookup"><span data-stu-id="2da3c-110">Other Dynamics 365 apps</span></span>
---------------------------------|---------------------------------
<span data-ttu-id="2da3c-111">Valūtas</span><span class="sxs-lookup"><span data-stu-id="2da3c-111">Currencies</span></span>                       | <span data-ttu-id="2da3c-112">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="2da3c-112">transactioncurrencies</span></span>
<span data-ttu-id="2da3c-113">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="2da3c-113">FiscalCalendar</span></span>                   | <span data-ttu-id="2da3c-114">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="2da3c-114">msdyn\_fiscalcalendars</span></span>
<span data-ttu-id="2da3c-115">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="2da3c-115">FiscalCalendarYear</span></span>               | <span data-ttu-id="2da3c-116">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="2da3c-116">msdyn\_fiscalcalendaryears</span></span>
<span data-ttu-id="2da3c-117">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="2da3c-117">ExchRateType</span></span>                     | <span data-ttu-id="2da3c-118">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="2da3c-118">msdyn\_exchangeratetypes</span></span>
<span data-ttu-id="2da3c-119">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="2da3c-119">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="2da3c-120">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="2da3c-120">msdyn\_currencyexchangeratepairs</span></span>
<span data-ttu-id="2da3c-121">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="2da3c-121">FiscalPeriodEntity</span></span>               | <span data-ttu-id="2da3c-122">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="2da3c-122">msdyn\_fiscalcalendarperiods</span></span>
<span data-ttu-id="2da3c-123">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="2da3c-123">MainAccountCategory</span></span>              | <span data-ttu-id="2da3c-124">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="2da3c-124">msdyn\_mainaccountcategory</span></span>
<span data-ttu-id="2da3c-125">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="2da3c-125">MainAccount</span></span>                      | <span data-ttu-id="2da3c-126">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="2da3c-126">msdyn\_mainaccounts</span></span>
<span data-ttu-id="2da3c-127">Virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="2da3c-127">Ledger</span></span>                           | <span data-ttu-id="2da3c-128">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="2da3c-128">msdyn\_ledgers</span></span>
<span data-ttu-id="2da3c-129">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="2da3c-129">ExchangeRates</span></span>                    | <span data-ttu-id="2da3c-130">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="2da3c-130">msdyn\_currencyexchangerates</span></span>
<span data-ttu-id="2da3c-131">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="2da3c-131">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="2da3c-132">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="2da3c-132">msdyn\_fiscalcalendarperiods</span></span>
<span data-ttu-id="2da3c-133">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="2da3c-133">DimensionAttributeEntity</span></span>         | <span data-ttu-id="2da3c-134">msdyn\_dimensionattributes.md</span><span class="sxs-lookup"><span data-stu-id="2da3c-134">msdyn\_dimensionattributes.md</span></span>
<span data-ttu-id="2da3c-135">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="2da3c-135">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="2da3c-136">msdyn\_financialdimensionformats.md</span><span class="sxs-lookup"><span data-stu-id="2da3c-136">msdyn\_financialdimensionformats.md</span></span>
<span data-ttu-id="2da3c-137">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="2da3c-137">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="2da3c-138">msdyn\_chartofaccounts.md</span><span class="sxs-lookup"><span data-stu-id="2da3c-138">msdyn\_chartofaccounts.md</span></span>


[!include [banner](../includes/dual-write-symbols.md)]

[!include [Currency](dual-write/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](dual-write/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](dual-write/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](dual-write/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](dual-write/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Ledger fiscal periods](dual-write/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Main account category](dual-write/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](dual-write/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](dual-write/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](dual-write/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](dual-write/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](dual-write/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](dual-write/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](dual-write/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]




