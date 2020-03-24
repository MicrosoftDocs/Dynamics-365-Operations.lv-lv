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
ms.openlocfilehash: d9bcec1d4bb0207a2c3e0d46f7661b666fea3736
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112218"
---
# <a name="integrated-ledger"></a><span data-ttu-id="f0909-103">Integrētā virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="f0909-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="f0909-104">Biznesa programmā virsgrāmatas dati definē pamata iestatījumus tam, kā uzņēmums darbojas.</span><span class="sxs-lookup"><span data-stu-id="f0909-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="f0909-105">Piemēram, virsgrāmatas datos ir aprakstīts finanšu gads, ko uzņēmums ievēro, valūtas, kurās tas veic darījumus, un konti, ko tas izmanto.</span><span class="sxs-lookup"><span data-stu-id="f0909-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="f0909-106">Šī tēma apraksta šo pamata finanšu datu integrēšanu.</span><span class="sxs-lookup"><span data-stu-id="f0909-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="f0909-107">Veidnes</span><span class="sxs-lookup"><span data-stu-id="f0909-107">Templates</span></span>

<span data-ttu-id="f0909-108">Virsgrāmatas dati ietver pamata finanšu elementa karšu vākšanu, kas darbojas kopā debitora datu mijiedarbības laikā, kā redzams nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="f0909-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="f0909-109">Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="f0909-109">Finance and Operations apps</span></span>      | <span data-ttu-id="f0909-110">Uz modeļa balstīta lietojumprogramma Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="f0909-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="f0909-111">apraksts</span><span class="sxs-lookup"><span data-stu-id="f0909-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="f0909-112">Valūtas</span><span class="sxs-lookup"><span data-stu-id="f0909-112">Currencies</span></span>                       | <span data-ttu-id="f0909-113">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="f0909-113">transactioncurrencies</span></span>            |
<span data-ttu-id="f0909-114">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="f0909-114">FiscalCalendar</span></span>                   | <span data-ttu-id="f0909-115">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="f0909-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="f0909-116">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="f0909-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="f0909-117">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="f0909-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="f0909-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="f0909-118">ExchRateType</span></span>                     | <span data-ttu-id="f0909-119">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="f0909-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="f0909-120">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="f0909-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="f0909-121">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="f0909-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="f0909-122">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="f0909-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="f0909-123">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="f0909-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="f0909-124">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="f0909-124">MainAccountCategory</span></span>              | <span data-ttu-id="f0909-125">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="f0909-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="f0909-126">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="f0909-126">MainAccount</span></span>                      | <span data-ttu-id="f0909-127">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="f0909-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="f0909-128">Virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="f0909-128">Ledger</span></span>                           | <span data-ttu-id="f0909-129">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="f0909-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="f0909-130">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="f0909-130">ExchangeRates</span></span>                    | <span data-ttu-id="f0909-131">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="f0909-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="f0909-132">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="f0909-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="f0909-133">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="f0909-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="f0909-134">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="f0909-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="f0909-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="f0909-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="f0909-136">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="f0909-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="f0909-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="f0909-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="f0909-138">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="f0909-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="f0909-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="f0909-139">msdyn\_chartofaccounts</span></span>        |


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](includes/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](includes/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](includes/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](includes/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Ledger fiscal periods](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Main account category](includes/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](includes/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](includes/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](includes/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](includes/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](includes/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](includes/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]




