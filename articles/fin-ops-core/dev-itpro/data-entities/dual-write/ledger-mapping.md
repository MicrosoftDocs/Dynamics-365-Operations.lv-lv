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
ms.openlocfilehash: 6bf1c554f56c1424da9fde98f67f80a6b7c95461
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019899"
---
# <a name="integrated-ledger"></a><span data-ttu-id="3b26e-103">Integrētā virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="3b26e-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="3b26e-104">Biznesa programmā virsgrāmatas dati definē pamata iestatījumus tam, kā uzņēmums darbojas.</span><span class="sxs-lookup"><span data-stu-id="3b26e-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="3b26e-105">Piemēram, virsgrāmatas datos ir aprakstīts finanšu gads, ko uzņēmums ievēro, valūtas, kurās tas veic darījumus, un konti, ko tas izmanto.</span><span class="sxs-lookup"><span data-stu-id="3b26e-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="3b26e-106">Šī tēma apraksta šo pamata finanšu datu integrēšanu.</span><span class="sxs-lookup"><span data-stu-id="3b26e-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="3b26e-107">Veidnes</span><span class="sxs-lookup"><span data-stu-id="3b26e-107">Templates</span></span>

<span data-ttu-id="3b26e-108">Virsgrāmatas dati ietver pamata finanšu elementa karšu vākšanu, kas darbojas kopā debitora datu mijiedarbības laikā, kā redzams nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="3b26e-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="3b26e-109">Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="3b26e-109">Finance and Operations apps</span></span>      | <span data-ttu-id="3b26e-110">Citas Dynamics 365 programmas</span><span class="sxs-lookup"><span data-stu-id="3b26e-110">Other Dynamics 365 apps</span></span>
---------------------------------|---------------------------------
<span data-ttu-id="3b26e-111">Valūtas</span><span class="sxs-lookup"><span data-stu-id="3b26e-111">Currencies</span></span>                       | <span data-ttu-id="3b26e-112">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="3b26e-112">transactioncurrencies</span></span>
<span data-ttu-id="3b26e-113">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="3b26e-113">FiscalCalendar</span></span>                   | <span data-ttu-id="3b26e-114">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="3b26e-114">msdyn\_fiscalcalendars</span></span>
<span data-ttu-id="3b26e-115">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="3b26e-115">FiscalCalendarYear</span></span>               | <span data-ttu-id="3b26e-116">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="3b26e-116">msdyn\_fiscalcalendaryears</span></span>
<span data-ttu-id="3b26e-117">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="3b26e-117">ExchRateType</span></span>                     | <span data-ttu-id="3b26e-118">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="3b26e-118">msdyn\_exchangeratetypes</span></span>
<span data-ttu-id="3b26e-119">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="3b26e-119">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="3b26e-120">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="3b26e-120">msdyn\_currencyexchangeratepairs</span></span>
<span data-ttu-id="3b26e-121">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="3b26e-121">FiscalPeriodEntity</span></span>               | <span data-ttu-id="3b26e-122">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="3b26e-122">msdyn\_fiscalcalendarperiods</span></span>
<span data-ttu-id="3b26e-123">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="3b26e-123">MainAccountCategory</span></span>              | <span data-ttu-id="3b26e-124">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="3b26e-124">msdyn\_mainaccountcategory</span></span>
<span data-ttu-id="3b26e-125">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="3b26e-125">MainAccount</span></span>                      | <span data-ttu-id="3b26e-126">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="3b26e-126">msdyn\_mainaccounts</span></span>
<span data-ttu-id="3b26e-127">Virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="3b26e-127">Ledger</span></span>                           | <span data-ttu-id="3b26e-128">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="3b26e-128">msdyn\_ledgers</span></span>
<span data-ttu-id="3b26e-129">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="3b26e-129">ExchangeRates</span></span>                    | <span data-ttu-id="3b26e-130">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="3b26e-130">msdyn\_currencyexchangerates</span></span>
<span data-ttu-id="3b26e-131">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="3b26e-131">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="3b26e-132">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="3b26e-132">msdyn\_fiscalcalendarperiods</span></span>
<span data-ttu-id="3b26e-133">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="3b26e-133">DimensionAttributeEntity</span></span>         | <span data-ttu-id="3b26e-134">msdyn\_dimensionattributes.md</span><span class="sxs-lookup"><span data-stu-id="3b26e-134">msdyn\_dimensionattributes.md</span></span>
<span data-ttu-id="3b26e-135">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="3b26e-135">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="3b26e-136">msdyn\_financialdimensionformats.md</span><span class="sxs-lookup"><span data-stu-id="3b26e-136">msdyn\_financialdimensionformats.md</span></span>
<span data-ttu-id="3b26e-137">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="3b26e-137">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="3b26e-138">msdyn\_chartofaccounts.md</span><span class="sxs-lookup"><span data-stu-id="3b26e-138">msdyn\_chartofaccounts.md</span></span>


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




