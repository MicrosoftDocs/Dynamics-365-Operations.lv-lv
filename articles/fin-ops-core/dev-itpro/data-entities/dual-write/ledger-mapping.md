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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 7f5435a97776b817a4b99887cbab8283de25b692
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4014862"
---
# <a name="integrated-ledger"></a><span data-ttu-id="f2aee-103">Integrētā virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="f2aee-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="f2aee-104">Biznesa programmā virsgrāmatas dati definē pamata iestatījumus tam, kā uzņēmums darbojas.</span><span class="sxs-lookup"><span data-stu-id="f2aee-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="f2aee-105">Piemēram, virsgrāmatas datos ir aprakstīts finanšu gads, ko uzņēmums ievēro, valūtas, kurās tas veic darījumus, un konti, ko tas izmanto.</span><span class="sxs-lookup"><span data-stu-id="f2aee-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="f2aee-106">Šī tēma apraksta šo pamata finanšu datu integrēšanu.</span><span class="sxs-lookup"><span data-stu-id="f2aee-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="f2aee-107">Veidnes</span><span class="sxs-lookup"><span data-stu-id="f2aee-107">Templates</span></span>

<span data-ttu-id="f2aee-108">Virsgrāmatas dati ietver pamata finanšu elementa karšu vākšanu, kas darbojas kopā debitora datu mijiedarbības laikā, kā redzams nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="f2aee-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="f2aee-109">Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="f2aee-109">Finance and Operations apps</span></span>      | <span data-ttu-id="f2aee-110">Uz modeļa balstīta lietojumprogramma Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="f2aee-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="f2aee-111">apraksts</span><span class="sxs-lookup"><span data-stu-id="f2aee-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="f2aee-112">Valūtas</span><span class="sxs-lookup"><span data-stu-id="f2aee-112">Currencies</span></span>                       | <span data-ttu-id="f2aee-113">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="f2aee-113">transactioncurrencies</span></span>            |
<span data-ttu-id="f2aee-114">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="f2aee-114">FiscalCalendar</span></span>                   | <span data-ttu-id="f2aee-115">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="f2aee-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="f2aee-116">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="f2aee-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="f2aee-117">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="f2aee-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="f2aee-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="f2aee-118">ExchRateType</span></span>                     | <span data-ttu-id="f2aee-119">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="f2aee-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="f2aee-120">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="f2aee-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="f2aee-121">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="f2aee-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="f2aee-122">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="f2aee-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="f2aee-123">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="f2aee-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="f2aee-124">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="f2aee-124">MainAccountCategory</span></span>              | <span data-ttu-id="f2aee-125">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="f2aee-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="f2aee-126">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="f2aee-126">MainAccount</span></span>                      | <span data-ttu-id="f2aee-127">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="f2aee-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="f2aee-128">Virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="f2aee-128">Ledger</span></span>                           | <span data-ttu-id="f2aee-129">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="f2aee-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="f2aee-130">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="f2aee-130">ExchangeRates</span></span>                    | <span data-ttu-id="f2aee-131">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="f2aee-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="f2aee-132">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="f2aee-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="f2aee-133">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="f2aee-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="f2aee-134">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="f2aee-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="f2aee-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="f2aee-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="f2aee-136">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="f2aee-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="f2aee-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="f2aee-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="f2aee-138">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="f2aee-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="f2aee-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="f2aee-139">msdyn\_chartofaccounts</span></span>        |


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](includes/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](includes/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](includes/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](includes/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Main account category](includes/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](includes/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](includes/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](includes/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](includes/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](includes/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](includes/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]




