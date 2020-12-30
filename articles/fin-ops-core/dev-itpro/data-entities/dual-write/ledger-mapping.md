---
title: Integrētā virsgrāmata
description: Šajā tēmā ir aprakstīta virsgrāmatas datu integrācija starp Finance and Operations un citām Dynamics 365 programmām, izmantojot Dataverse.
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
ms.openlocfilehash: f794d8306a3a752d811d7d84c0ed5f739f423cad
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681646"
---
# <a name="integrated-ledger"></a><span data-ttu-id="17327-103">Integrētā virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="17327-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="17327-104">Biznesa programmā virsgrāmatas dati definē pamata iestatījumus tam, kā uzņēmums darbojas.</span><span class="sxs-lookup"><span data-stu-id="17327-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="17327-105">Piemēram, virsgrāmatas datos ir aprakstīts finanšu gads, ko uzņēmums ievēro, valūtas, kurās tas veic darījumus, un konti, ko tas izmanto.</span><span class="sxs-lookup"><span data-stu-id="17327-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="17327-106">Šī tēma apraksta šo pamata finanšu datu integrēšanu.</span><span class="sxs-lookup"><span data-stu-id="17327-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="17327-107">Veidnes</span><span class="sxs-lookup"><span data-stu-id="17327-107">Templates</span></span>

<span data-ttu-id="17327-108">Virsgrāmatas dati ietver pamata finanšu tabulas vākšanu, kas darbojas kopā debitora datu mijiedarbības laikā, kā redzams nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="17327-108">Ledger data includes a collection of core financial table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="17327-109">Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="17327-109">Finance and Operations apps</span></span>      | <span data-ttu-id="17327-110">Uz modeļa balstīta lietojumprogramma Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="17327-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="17327-111">apraksts</span><span class="sxs-lookup"><span data-stu-id="17327-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="17327-112">Valūtas</span><span class="sxs-lookup"><span data-stu-id="17327-112">Currencies</span></span>                       | <span data-ttu-id="17327-113">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="17327-113">transactioncurrencies</span></span>            |
<span data-ttu-id="17327-114">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="17327-114">FiscalCalendar</span></span>                   | <span data-ttu-id="17327-115">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="17327-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="17327-116">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="17327-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="17327-117">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="17327-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="17327-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="17327-118">ExchRateType</span></span>                     | <span data-ttu-id="17327-119">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="17327-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="17327-120">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="17327-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="17327-121">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="17327-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="17327-122">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="17327-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="17327-123">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="17327-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="17327-124">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="17327-124">MainAccountCategory</span></span>              | <span data-ttu-id="17327-125">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="17327-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="17327-126">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="17327-126">MainAccount</span></span>                      | <span data-ttu-id="17327-127">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="17327-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="17327-128">Virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="17327-128">Ledger</span></span>                           | <span data-ttu-id="17327-129">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="17327-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="17327-130">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="17327-130">ExchangeRates</span></span>                    | <span data-ttu-id="17327-131">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="17327-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="17327-132">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="17327-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="17327-133">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="17327-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="17327-134">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="17327-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="17327-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="17327-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="17327-136">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="17327-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="17327-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="17327-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="17327-138">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="17327-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="17327-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="17327-139">msdyn\_chartofaccounts</span></span>        |


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




