---
title: Problēmu novēršana naudas plūsmas prognozēšanas iestatīšanā
description: Šajā tēmā ir sniegtas atbildes uz jautājumiem, kas var rasties skaidras naudas plūsmas prognozēšanas konfigurēšanas gaitā. Tā apraksta biežāk uzdotos jautājumus (BUJ) par naudas plūsmas iestatīšanu, naudas plūsmas atjauninājumiem un naudas plūsmas Power BI.
author: panolte
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7b4760d7a0d0c14e2df8df20c2f81ec41e077cc0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827318"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="c6ba4-104">Problēmu novēršana naudas plūsmas prognozēšanas iestatīšanā</span><span class="sxs-lookup"><span data-stu-id="c6ba4-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6ba4-105">Šajā tēmā ir sniegtas atbildes uz jautājumiem, kas var rasties skaidras naudas plūsmas prognozēšanas konfigurēšanas gaitā.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="c6ba4-106">Tā apraksta biežāk uzdotos jautājumus (BUJ) par naudas plūsmas iestatīšanu, naudas plūsmas atjauninājumiem un naudas plūsmas Power BI.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="c6ba4-107">Kādēļ naudas plūsma tiek rādīta tikai vienai juridiskajai personai?</span><span class="sxs-lookup"><span data-stu-id="c6ba4-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="c6ba4-108">Naudas plūsmas prognozēšana tiek konfigurēta un aprēķināta katrai juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="c6ba4-109">Power BI pārskati un naudas plūsmas prognožu spēja rāda rezultātus sadaļā Finance insights.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="c6ba4-110">Naudas plūsmas prognozēšana jāiestata katrai juridiskajai personai, kurai vēlaties skatīt prognozi.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="c6ba4-111">Pārskatiet naudas plūsmas prognozes konfigurāciju visās juridiskajās personas.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="c6ba4-112">Alternatīvi pārskatiet visu juridisko personu konfigurāciju naudas plūsmas prognozēšanai un pārliecinieties, ka tās ir iestatītas tā, kā paredzēts.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="c6ba4-113">Kādēļ Power BI netiek rādīti visi naudas plūsmas dati?</span><span class="sxs-lookup"><span data-stu-id="c6ba4-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="c6ba4-114">Pirms naudas plūsmas prognozes var parādīties Power BI skatījumos, ir jāveic vairāki soļi.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="c6ba4-115">Pārskatiet sekojošo kontrolsarakstu un pārliecinieties, ka katrs solis ir pabeigts:</span><span class="sxs-lookup"><span data-stu-id="c6ba4-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="c6ba4-116">Iestatiet naudas plūsmu katrai juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="c6ba4-117">Virsgrāmatas parametros iestatiet sistēmas valūtu un sistēmas maiņas kursa tipu.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="c6ba4-118">Iestatiet Virsgrāmatas uzskaites valūtu un maiņas kursa tipu.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="c6ba4-119">Ievadiet maiņas kursus no darījuma valūtas uz uzskaites valūtu.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="c6ba4-120">Ievadiet maiņas kursus starp uzskaites valūtu un sistēmas valūtu.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="c6ba4-121">Ievadiet maiņas kursus starp uzskaites valūtu un katras bankas valūtu.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="c6ba4-122">Kādēļ naudas plūsma Power BI darbojas iepriekšējās versijās, bet tagad ir tukša?</span><span class="sxs-lookup"><span data-stu-id="c6ba4-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="c6ba4-123">Pārbaudiet, vai Elementu krātuves mērījumi "Naudas plūsmas mērījums V2" un "LedgerCovLiquidityMeasurement" ir konfigurēti.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="c6ba4-124">Lai iegūtu papildinformāciju par to, kā strādāt ar datiem entītiju krātuvē, skatiet sadaļu [Power BI integrācija ar Elementu krātuvi](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="c6ba4-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="c6ba4-125">Pārbaudiet, vai ir pabeigtas visas darbības, kas nepieciešamas Power BI satura skatīšanai.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-125">Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="c6ba4-126">Plašāku informāciju skatiet sadaļā [Skaidras naudas pārskata Power BI saturs](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="c6ba4-126">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="c6ba4-127">Vai Elementu krātuves elementi ir atsvaidzināti?</span><span class="sxs-lookup"><span data-stu-id="c6ba4-127">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="c6ba4-128">Periodiski jāatsvaidzina elementi, lai nodrošinātu, ka dati ir pašreizējie un precīzi.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-128">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="c6ba4-129">Lai manuāli atsvaidzinātu noteiktu elementu, pārejiet uz sadaļu **Sistēmas administrēšana \> Iestatīšanas \> Elementu krātuve** atlasiet elementu un pēc tam atlasiet **Atsvaidzināt**.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-129">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="c6ba4-130">Datus var atjaunināt arī automātiski.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-130">The data can also be updated automatically.</span></span> <span data-ttu-id="c6ba4-131">Lapā **Elementu krātuve** iestatiet opciju **Automātiskā atsvaidzināšana iespējota** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-131">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a><span data-ttu-id="c6ba4-132">Kuru aprēķinu metodi lietot, aprēķinot naudas plūsmas prognozes?</span><span class="sxs-lookup"><span data-stu-id="c6ba4-132">Which calculation method should be used when calculating cash flow forecasts?</span></span>

<span data-ttu-id="c6ba4-133">Naudas plūsmas prognozes aprēķina metodei ir divas svarīgas atlases opcijas.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-133">The Cash flow forecast calculation method has two important selection options.</span></span> <span data-ttu-id="c6ba4-134">Opcija **Jauns** aprēķinās naudas plūsmas prognozes jaunajiem dokumentiem un dokumentiem, kas ir mainījušies kopš pēdējā pakešuzdevuma izpildes.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-134">The **New** option will calculate cash flow forecasts for new documents and documents that have changed since the last batch job ran.</span></span> <span data-ttu-id="c6ba4-135">Šī opcija darbojas ātrāk, jo apstrādā mazāku dokumentu apakškopu.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-135">This option tends to run faster because it processes a smaller subset of documents.</span></span> <span data-ttu-id="c6ba4-136">Opcija **Kopsumma** pārrēķinās naudas plūsmas prognozes katram dokumentam sistēmā.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-136">The **Total** option will recalculate cash flow forecasts for every document in the system.</span></span> <span data-ttu-id="c6ba4-137">Šīs opcijas pabeigšanai nepieciešams vairāk laika, jo tai ir vairāk darba.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-137">This option takes more time because it has more work to complete.</span></span>

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a><span data-ttu-id="c6ba4-138">Kā uzlabot naudas plūsmas prognozēšanas periodiskā pakešuzdevuma veiktspēju?</span><span class="sxs-lookup"><span data-stu-id="c6ba4-138">How do I improve the performance of the cash flow forecasting recurring batch job?</span></span>

<span data-ttu-id="c6ba4-139">veikt naudas plūsmas prognozi vienu reizi dienā ārpusslodzes stundu laikā, izmantojot aprēķina metodi **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-139">We recommend running your cash flow forecast once each day during the off-peak hours using the **New** calculation method.</span></span> <span data-ttu-id="c6ba4-140">Ieteicams izmantot šo pieeju sešas dienas nedēļā.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-140">We recommend using this approach six days per week.</span></span> <span data-ttu-id="c6ba4-141">Pēc tam vienu reizi nedēļā palaidiet naudas plūsmas prognozi, izmantojot aprēķina metodi **Kopējais** dienā ar vismazāko aktivitātes daudzumu.</span><span class="sxs-lookup"><span data-stu-id="c6ba4-141">Then run a cash flow forecast once each week using the **Total** calculation method on the day with the least amount of activity.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

