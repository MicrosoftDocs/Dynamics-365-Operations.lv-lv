---
title: Prognozēšanas modeļa uzlabošana (priekšskatījums)
description: Šī tēma apraksta līdzekļus, ko varat izmantot prognozēšanas modeļu veiktspējas uzlabošanai.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 184a1cb5d3851e26b41340b711c51ef38e06eb53
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186646"
---
# <a name="improve-the-prediction-model-preview"></a><span data-ttu-id="192ba-103">Prognozēšanas modeļa uzlabošana (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="192ba-103">Improve the prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="192ba-104">Šī tēma apraksta līdzekļus, ko varat izmantot prognozēšanas modeļu veiktspējas uzlabošanai.</span><span class="sxs-lookup"><span data-stu-id="192ba-104">This topic describes features that you can use to improve the performance of prediction models.</span></span> <span data-ttu-id="192ba-105">Jūs sākat uzlabot savu modeli **Klientu maksājumu prognožu** darbvietā programmā Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="192ba-105">You start to improve your model in the **Customer payment predictions** workspace in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="192ba-106">Tad uzlabojumu darbības tiek pabeigtas AI Builder.</span><span class="sxs-lookup"><span data-stu-id="192ba-106">The improvement steps are then completed in AI Builder.</span></span>

## <a name="select-historical-outcomes"></a><span data-ttu-id="192ba-107">Vēsturisko iznākumu atlasīšana</span><span class="sxs-lookup"><span data-stu-id="192ba-107">Select historical outcomes</span></span>

<span data-ttu-id="192ba-108">Vispirms atlasiet vienu vai vairākus no trim iespējamiem iznākumiem rēķiniem: **Laicīgi**, **Novēloti** un **Ļoti novēloti**.</span><span class="sxs-lookup"><span data-stu-id="192ba-108">You first select one or more of the three possible outcomes for invoices: **On time**, **Late**, and **Very late**.</span></span> <span data-ttu-id="192ba-109">Jāatlasa visi trīs rezultāti.</span><span class="sxs-lookup"><span data-stu-id="192ba-109">All three outcomes should be selected.</span></span> <span data-ttu-id="192ba-110">Notīrot kāda rezultāta atlasi, rēķini tiks filtrēti no apmācības procesa, un prognozes precizitāte tiks samazināta.</span><span class="sxs-lookup"><span data-stu-id="192ba-110">If you clear the selection of any of the outcomes, invoices will be filtered out of the training process and the accuracy of the prediction will be reduced.</span></span>

<span data-ttu-id="192ba-111">[![Iznāķumu apstiprināšana](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span><span class="sxs-lookup"><span data-stu-id="192ba-111">[![Confirming outcomes](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span></span>

<span data-ttu-id="192ba-112">Ja jūsu organizācijai nepieciešami tikai divi iznākumi, mainiet **Novēloti** un **Ļoti novēloti** slieksni uz 0 (nulle) dienām.</span><span class="sxs-lookup"><span data-stu-id="192ba-112">If your organization requires only two outcomes, change the **Late** and **Very late** thresholds to 0 (zero) days.</span></span> <span data-ttu-id="192ba-113">Šādā veidā jūs efektīvi sakļaujat prognozes binārajā stāvoklī ar **Laicīgi** vai **Novēloti**.</span><span class="sxs-lookup"><span data-stu-id="192ba-113">In this way, you effectively collapse the prediction to a binary state of **On time** or **Late**.</span></span>

## <a name="select-fields"></a><span data-ttu-id="192ba-114">Atlasiet pārskata laukus</span><span class="sxs-lookup"><span data-stu-id="192ba-114">Select fields</span></span>

<span data-ttu-id="192ba-115">Kad atlasāt laukus iekļaušanai modelī, ņemiet vērā, ka sarakstā ir iekļauti visi pieejamie lauki Microsoft Dataverse tabulā, kas ir kartēts Azure datu ezera datos.</span><span class="sxs-lookup"><span data-stu-id="192ba-115">When you're selecting fields to include in the model, be aware that the list includes all available fields in the Microsoft Dataverse table that is mapped to the data in the Azure data lake.</span></span> <span data-ttu-id="192ba-116">Dažus no šiem laukiem **nedrīkst** atlasīt.</span><span class="sxs-lookup"><span data-stu-id="192ba-116">Some of these fields should **not** be selected.</span></span> <span data-ttu-id="192ba-117">Lauki, kas nav jāatlasa, ietilpst vienā no trijām kategorijām:</span><span class="sxs-lookup"><span data-stu-id="192ba-117">The fields that should not be selected fall into one of three categories:</span></span>

- <span data-ttu-id="192ba-118">Šis lauks ir nepieciešams Dataverse tabulai, bet datu ezerā tam nav datu dublēšanas datu.</span><span class="sxs-lookup"><span data-stu-id="192ba-118">The field is required for the Dataverse table, but there is no backing data for it in the data lake.</span></span>
- <span data-ttu-id="192ba-119">Lauks ir ID un tādēļ nav jēgas izmantot algoritmiskās mācīšanās līdzekli.</span><span class="sxs-lookup"><span data-stu-id="192ba-119">The field is an ID and therefore doesn't make sense for a machine learning feature.</span></span>
- <span data-ttu-id="192ba-120">Lauks ataino informāciju, kas nebūs pieejama prognozēšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="192ba-120">The field represents information that won't be available during prediction.</span></span>

<span data-ttu-id="192ba-121">Šajās sadaļās ir redzami lauki, kas ir pieejami rēķina un klienta elementiem, un uzskaitīti lauki, kas **nav** jāatlasa apmācībai.</span><span class="sxs-lookup"><span data-stu-id="192ba-121">The following sections show the fields that are available for the invoice and customer entities, and list the fields that should **not** be selected for training.</span></span> <span data-ttu-id="192ba-122">Kategorija, kas norādīta katram no šiem laukiem, attiecas uz kategorijām iepriekšējā sarakstā.</span><span class="sxs-lookup"><span data-stu-id="192ba-122">The category that is specified for each of those fields refers to the categories in the preceding list.</span></span>
 
### <a name="invoice-dataverse-table"></a><span data-ttu-id="192ba-123">Rēķinu Dataverse tabula</span><span class="sxs-lookup"><span data-stu-id="192ba-123">Invoice Dataverse table</span></span>

<span data-ttu-id="192ba-124">Nākamajā attēlā ir parādīti avoti, kas ir pieejami rēķina tabulai.</span><span class="sxs-lookup"><span data-stu-id="192ba-124">The following illustration shows the fields that are available for the invoice table.</span></span>

<span data-ttu-id="192ba-125">[![Rēķina tabulai pieejamie lauki](./media/available-fields.png)](./media/available-fields.png)</span><span class="sxs-lookup"><span data-stu-id="192ba-125">[![Available fields for the invoice table](./media/available-fields.png)](./media/available-fields.png)</span></span>

<span data-ttu-id="192ba-126">Apmācībām nav jāatlasa tālāk minētie lauki.</span><span class="sxs-lookup"><span data-stu-id="192ba-126">The following fields should not be selected for training:</span></span>

- <span data-ttu-id="192ba-127">**Rēķina konts** (2. kategorija)</span><span class="sxs-lookup"><span data-stu-id="192ba-127">**Invoice Account** (category 2)</span></span>
- <span data-ttu-id="192ba-128">**Ir slēgts** (3. kategorija) — šis lauks tiek izmantots, lai filtrētu rēķinus apmācībām (slēgts) un prognozēšanai (nav slēgts).</span><span class="sxs-lookup"><span data-stu-id="192ba-128">**Is closed** (category 3) – This field is used to filter invoices for training (closed) and prediction (not closed).</span></span>
- <span data-ttu-id="192ba-129">**Nosaukums** (1. kategorija)</span><span class="sxs-lookup"><span data-stu-id="192ba-129">**Name** (category 1)</span></span>
- <span data-ttu-id="192ba-130">**Avota ID** (2. kategorija)</span><span class="sxs-lookup"><span data-stu-id="192ba-130">**Source Id** (category 2)</span></span>
- <span data-ttu-id="192ba-131">**Avota ieraksts** (2. kategorija)</span><span class="sxs-lookup"><span data-stu-id="192ba-131">**Source record** (category 2)</span></span>
- <span data-ttu-id="192ba-132">**Avota tabula** (2. kategorija)</span><span class="sxs-lookup"><span data-stu-id="192ba-132">**Source table** (category 2)</span></span>

### <a name="customer-dataverse-table"></a><span data-ttu-id="192ba-133">Debitoru Dataverse tabula</span><span class="sxs-lookup"><span data-stu-id="192ba-133">Customer Dataverse table</span></span>

<span data-ttu-id="192ba-134">Nākamajā attēlā ir parādīti avoti, kas ir pieejami debitora tabulai.</span><span class="sxs-lookup"><span data-stu-id="192ba-134">The following illustration shows the fields that are available for the customer table.</span></span>

<span data-ttu-id="192ba-135">[![Debitora tabulai pieejamie lauki](./media/related-entities.png)](./media/related-entities.png)</span><span class="sxs-lookup"><span data-stu-id="192ba-135">[![Available fields for the customer table](./media/related-entities.png)](./media/related-entities.png)</span></span>

<span data-ttu-id="192ba-136">Apmācībām nav jāatlasa tālāk minētais lauks.</span><span class="sxs-lookup"><span data-stu-id="192ba-136">The following field should not be selected for training:</span></span>

- <span data-ttu-id="192ba-137">**Unikālā rindas atslēga** (2. kategorija)</span><span class="sxs-lookup"><span data-stu-id="192ba-137">**Row Unique Key** (category 2)</span></span>

## <a name="filters"></a><span data-ttu-id="192ba-138">Filtri</span><span class="sxs-lookup"><span data-stu-id="192ba-138">Filters</span></span>

<span data-ttu-id="192ba-139">Filtri pašlaik neatbalsta debitoru maksājumu prognozēšanas scenāriju.</span><span class="sxs-lookup"><span data-stu-id="192ba-139">The filters don't currently support the Customer payment predictor scenario.</span></span> <span data-ttu-id="192ba-140">Tāpēc atlasiet **Izlaist šo darbību** un pārejiet uz kopsavilkuma lapu.</span><span class="sxs-lookup"><span data-stu-id="192ba-140">Therefore, select **Skip this step**, and continue to the summary page.</span></span>

<span data-ttu-id="192ba-141">[![Fokusa režīms ar filtriem](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span><span class="sxs-lookup"><span data-stu-id="192ba-141">[![Focus model with filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
