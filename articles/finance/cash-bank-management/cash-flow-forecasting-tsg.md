---
title: Problēmu novēršana naudas plūsmas prognozēšanas iestatīšanā
description: Šajā tēmā ir sniegtas atbildes uz jautājumiem, kas var rasties skaidras naudas plūsmas prognozēšanas konfigurēšanas gaitā. Tā apraksta biežāk uzdotos jautājumus (BUJ) par naudas plūsmas iestatīšanu, naudas plūsmas atjauninājumiem un naudas plūsmas Power BI.
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d1cde9321259753bd0cacab3706c7f8455598ff3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232493"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="6bdea-104">Problēmu novēršana naudas plūsmas prognozēšanas iestatīšanā</span><span class="sxs-lookup"><span data-stu-id="6bdea-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6bdea-105">Šajā tēmā ir sniegtas atbildes uz jautājumiem, kas var rasties skaidras naudas plūsmas prognozēšanas konfigurēšanas gaitā.</span><span class="sxs-lookup"><span data-stu-id="6bdea-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="6bdea-106">Tā apraksta biežāk uzdotos jautājumus (BUJ) par naudas plūsmas iestatīšanu, naudas plūsmas atjauninājumiem un naudas plūsmas Power BI.</span><span class="sxs-lookup"><span data-stu-id="6bdea-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="6bdea-107">Kādēļ naudas plūsma tiek rādīta tikai vienai juridiskajai personai?</span><span class="sxs-lookup"><span data-stu-id="6bdea-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="6bdea-108">Naudas plūsmas prognozēšana tiek konfigurēta un aprēķināta katrai juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="6bdea-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="6bdea-109">Power BI pārskati un naudas plūsmas prognožu spēja rāda rezultātus sadaļā Finance insights.</span><span class="sxs-lookup"><span data-stu-id="6bdea-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="6bdea-110">Naudas plūsmas prognozēšana jāiestata katrai juridiskajai personai, kurai vēlaties skatīt prognozi.</span><span class="sxs-lookup"><span data-stu-id="6bdea-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="6bdea-111">Pārskatiet naudas plūsmas prognozes konfigurāciju visās juridiskajās personas.</span><span class="sxs-lookup"><span data-stu-id="6bdea-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="6bdea-112">Alternatīvi pārskatiet visu juridisko personu konfigurāciju naudas plūsmas prognozēšanai un pārliecinieties, ka tās ir iestatītas tā, kā paredzēts.</span><span class="sxs-lookup"><span data-stu-id="6bdea-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="6bdea-113">Kādēļ Power BI netiek rādīti visi naudas plūsmas dati?</span><span class="sxs-lookup"><span data-stu-id="6bdea-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="6bdea-114">Pirms naudas plūsmas prognozes var parādīties Power BI skatījumos, ir jāveic vairāki soļi.</span><span class="sxs-lookup"><span data-stu-id="6bdea-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="6bdea-115">Pārskatiet sekojošo kontrolsarakstu un pārliecinieties, ka katrs solis ir pabeigts:</span><span class="sxs-lookup"><span data-stu-id="6bdea-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="6bdea-116">Iestatiet naudas plūsmu katrai juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="6bdea-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="6bdea-117">Virsgrāmatas parametros iestatiet sistēmas valūtu un sistēmas maiņas kursa tipu.</span><span class="sxs-lookup"><span data-stu-id="6bdea-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="6bdea-118">Iestatiet Virsgrāmatas uzskaites valūtu un maiņas kursa tipu.</span><span class="sxs-lookup"><span data-stu-id="6bdea-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="6bdea-119">Ievadiet maiņas kursus no darījuma valūtas uz uzskaites valūtu.</span><span class="sxs-lookup"><span data-stu-id="6bdea-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="6bdea-120">Ievadiet maiņas kursus starp uzskaites valūtu un sistēmas valūtu.</span><span class="sxs-lookup"><span data-stu-id="6bdea-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="6bdea-121">Ievadiet maiņas kursus starp uzskaites valūtu un katras bankas valūtu.</span><span class="sxs-lookup"><span data-stu-id="6bdea-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="6bdea-122">Kādēļ naudas plūsma Power BI darbojas iepriekšējās versijās, bet tagad ir tukša?</span><span class="sxs-lookup"><span data-stu-id="6bdea-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="6bdea-123">Pārbaudiet, vai Elementu krātuves mērījumi "Naudas plūsmas mērījums V2" un "LedgerCovLiquidityMeasurement" ir konfigurēti.</span><span class="sxs-lookup"><span data-stu-id="6bdea-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="6bdea-124">Papildinformāciju par to, kā strādāt ar datiem Elementa krātuvē, skatiet [Power BI integrācija ar elementu krātuvi](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) Pārbaudiet, vai ir izpildītas visas darbības, kas jāveic, lai skatītu Power BI saturu.</span><span class="sxs-lookup"><span data-stu-id="6bdea-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="6bdea-125">Plašāku informāciju skatiet sadaļā [Skaidras naudas pārskata Power BI saturs](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="6bdea-125">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="6bdea-126">Vai Elementu krātuves elementi ir atsvaidzināti?</span><span class="sxs-lookup"><span data-stu-id="6bdea-126">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="6bdea-127">Periodiski jāatsvaidzina elementi, lai nodrošinātu, ka dati ir pašreizējie un precīzi.</span><span class="sxs-lookup"><span data-stu-id="6bdea-127">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="6bdea-128">Lai manuāli atsvaidzinātu noteiktu elementu, pārejiet uz sadaļu **Sistēmas administrēšana \> Iestatīšanas \> Elementu krātuve** atlasiet elementu un pēc tam atlasiet **Atsvaidzināt**.</span><span class="sxs-lookup"><span data-stu-id="6bdea-128">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="6bdea-129">Datus var atjaunināt arī automātiski.</span><span class="sxs-lookup"><span data-stu-id="6bdea-129">The data can also be updated automatically.</span></span> <span data-ttu-id="6bdea-130">Lapā **Elementu krātuve** iestatiet opciju **Automātiskā atsvaidzināšana iespējota** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="6bdea-130">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]