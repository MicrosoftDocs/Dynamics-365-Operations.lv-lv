---
title: Integrētā virsgrāmata
description: Šajā tēmā ir aprakstīta virsgrāmatas datu integrācija starp Finance and Operations un citām Dynamics 365 programmām, izmantojot Dataverse.
author: robinarh
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5fedcbcd8db2692214ea66b2fbab9f7381e0a622
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748521"
---
# <a name="integrated-ledger"></a><span data-ttu-id="2fca2-103">Integrētā virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="2fca2-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="2fca2-104">Biznesa programmā virsgrāmatas dati definē pamata iestatījumus tam, kā uzņēmums darbojas.</span><span class="sxs-lookup"><span data-stu-id="2fca2-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="2fca2-105">Piemēram, virsgrāmatas datos ir aprakstīts finanšu gads, ko uzņēmums ievēro, valūtas, kurās tas veic darījumus, un konti, ko tas izmanto.</span><span class="sxs-lookup"><span data-stu-id="2fca2-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="2fca2-106">Šī tēma apraksta šo pamata finanšu datu integrēšanu.</span><span class="sxs-lookup"><span data-stu-id="2fca2-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="2fca2-107">Veidnes</span><span class="sxs-lookup"><span data-stu-id="2fca2-107">Templates</span></span>

<span data-ttu-id="2fca2-108">Virsgrāmatas dati ietver pamata finanšu tabulas vākšanu, kas darbojas kopā debitora datu mijiedarbības laikā, kā redzams nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="2fca2-108">Ledger data includes a collection of core financial table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="2fca2-109">Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="2fca2-109">Finance and Operations apps</span></span>      | <span data-ttu-id="2fca2-110">Uz modeļa balstīta lietojumprogramma Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="2fca2-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="2fca2-111">apraksts</span><span class="sxs-lookup"><span data-stu-id="2fca2-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="2fca2-112">Valūtas</span><span class="sxs-lookup"><span data-stu-id="2fca2-112">Currencies</span></span>                       | <span data-ttu-id="2fca2-113">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="2fca2-113">transactioncurrencies</span></span>            |
<span data-ttu-id="2fca2-114">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="2fca2-114">FiscalCalendar</span></span>                   | <span data-ttu-id="2fca2-115">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="2fca2-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="2fca2-116">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="2fca2-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="2fca2-117">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="2fca2-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="2fca2-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="2fca2-118">ExchRateType</span></span>                     | <span data-ttu-id="2fca2-119">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="2fca2-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="2fca2-120">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="2fca2-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="2fca2-121">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="2fca2-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="2fca2-122">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="2fca2-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="2fca2-123">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="2fca2-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="2fca2-124">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="2fca2-124">MainAccountCategory</span></span>              | <span data-ttu-id="2fca2-125">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="2fca2-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="2fca2-126">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="2fca2-126">MainAccount</span></span>                      | <span data-ttu-id="2fca2-127">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="2fca2-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="2fca2-128">Virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="2fca2-128">Ledger</span></span>                           | <span data-ttu-id="2fca2-129">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="2fca2-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="2fca2-130">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="2fca2-130">ExchangeRates</span></span>                    | <span data-ttu-id="2fca2-131">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="2fca2-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="2fca2-132">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="2fca2-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="2fca2-133">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="2fca2-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="2fca2-134">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="2fca2-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="2fca2-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="2fca2-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="2fca2-136">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="2fca2-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="2fca2-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="2fca2-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="2fca2-138">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="2fca2-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="2fca2-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="2fca2-139">msdyn\_chartofaccounts</span></span>        |


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






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]