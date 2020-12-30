---
title: Prognozēšanas modeļa uzlabošana (priekšskatījums)
description: Šī tēma apraksta līdzekļus, ko varat izmantot prognozēšanas modeļu veiktspējas uzlabošanai.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 23c9062dcc13951792306c955b54cae6f656fec5
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646083"
---
# <a name="improve-the-prediction-model-preview"></a><span data-ttu-id="62d5f-103">Prognozēšanas modeļa uzlabošana (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="62d5f-103">Improve the prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="62d5f-104">Šī tēma apraksta līdzekļus, ko varat izmantot prognozēšanas modeļu veiktspējas uzlabošanai.</span><span class="sxs-lookup"><span data-stu-id="62d5f-104">This topic describes features that you can use to improve the performance of prediction models.</span></span> <span data-ttu-id="62d5f-105">Jūs sākat uzlabot savu modeli **Klientu maksājumu prognožu** darbvietā programmā Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="62d5f-105">You start to improve your model in the **Customer payment predictions** workspace in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="62d5f-106">Tad uzlabojumu darbības tiek pabeigtas AI Builder.</span><span class="sxs-lookup"><span data-stu-id="62d5f-106">The improvement steps are then completed in AI Builder.</span></span>

## <a name="select-historical-outcomes"></a><span data-ttu-id="62d5f-107">Vēsturisko iznākumu atlasīšana</span><span class="sxs-lookup"><span data-stu-id="62d5f-107">Select historical outcomes</span></span>

<span data-ttu-id="62d5f-108">Vispirms atlasiet vienu vai vairākus no trim iespējamiem iznākumiem rēķiniem: **Laicīgi**, **Novēloti** un **Ļoti novēloti**.</span><span class="sxs-lookup"><span data-stu-id="62d5f-108">You first select one or more of the three possible outcomes for invoices: **On time**, **Late**, and **Very late**.</span></span> <span data-ttu-id="62d5f-109">Jāatlasa visi trīs rezultāti.</span><span class="sxs-lookup"><span data-stu-id="62d5f-109">All three outcomes should be selected.</span></span> <span data-ttu-id="62d5f-110">Notīrot kāda rezultāta atlasi, rēķini tiks filtrēti no apmācības procesa, un prognozes precizitāte tiks samazināta.</span><span class="sxs-lookup"><span data-stu-id="62d5f-110">If you clear the selection of any of the outcomes, invoices will be filtered out of the training process and the accuracy of the prediction will be reduced.</span></span>

<span data-ttu-id="62d5f-111">[![Iznāķumu apstiprināšana](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span><span class="sxs-lookup"><span data-stu-id="62d5f-111">[![Confirming outcomes](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span></span>

<span data-ttu-id="62d5f-112">Ja jūsu organizācijai nepieciešami tikai divi iznākumi, mainiet **Novēloti** un **Ļoti novēloti** slieksni uz 0 (nulle) dienām.</span><span class="sxs-lookup"><span data-stu-id="62d5f-112">If your organization requires only two outcomes, change the **Late** and **Very late** thresholds to 0 (zero) days.</span></span> <span data-ttu-id="62d5f-113">Šādā veidā jūs efektīvi sakļaujat prognozes binārajā stāvoklī ar **Laicīgi** vai **Novēloti**.</span><span class="sxs-lookup"><span data-stu-id="62d5f-113">In this way, you effectively collapse the prediction to a binary state of **On time** or **Late**.</span></span>

## <a name="select-fields"></a><span data-ttu-id="62d5f-114">Atlasiet pārskata laukus</span><span class="sxs-lookup"><span data-stu-id="62d5f-114">Select fields</span></span>

<span data-ttu-id="62d5f-115">Kad atlasāt laukus iekļaušanai modelī, ņemiet vērā, ka sarakstā ir iekļauti visi pieejamie lauki elementā Common Data Service, kas ir kartēts Azure datu ezera datos.</span><span class="sxs-lookup"><span data-stu-id="62d5f-115">When you're selecting fields to include in the model, be aware that the list includes all available fields in the Common Data Service entity that is mapped to the data in the Azure data lake.</span></span> <span data-ttu-id="62d5f-116">Dažus no šiem laukiem **nedrīkst** atlasīt.</span><span class="sxs-lookup"><span data-stu-id="62d5f-116">Some of these fields should **not** be selected.</span></span> <span data-ttu-id="62d5f-117">Lauki, kas nav jāatlasa, ietilpst vienā no trijām kategorijām:</span><span class="sxs-lookup"><span data-stu-id="62d5f-117">The fields that should not be selected fall into one of three categories:</span></span>

- <span data-ttu-id="62d5f-118">Šis lauks ir nepieciešams Common Data Service elementam, bet datu ezerā tam nav datu dublēšanas datu.</span><span class="sxs-lookup"><span data-stu-id="62d5f-118">The field is required for the Common Data Service entity, but there is no backing data for it in the data lake.</span></span>
- <span data-ttu-id="62d5f-119">Lauks ir ID un tādēļ nav jēgas izmantot algoritmiskās mācīšanās līdzekli.</span><span class="sxs-lookup"><span data-stu-id="62d5f-119">The field is an ID and therefore doesn't make sense for a machine learning feature.</span></span>
- <span data-ttu-id="62d5f-120">Lauks ataino informāciju, kas nebūs pieejama prognozēšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="62d5f-120">The field represents information that won't be available during prediction.</span></span>

<span data-ttu-id="62d5f-121">Šajās sadaļās ir redzami lauki, kas ir pieejami rēķina un klienta elementiem, un uzskaitīti lauki, kas **nav** jāatlasa apmācībai.</span><span class="sxs-lookup"><span data-stu-id="62d5f-121">The following sections show the fields that are available for the invoice and customer entities, and list the fields that should **not** be selected for training.</span></span> <span data-ttu-id="62d5f-122">Kategorija, kas norādīta katram no šiem laukiem, attiecas uz kategorijām iepriekšējā sarakstā.</span><span class="sxs-lookup"><span data-stu-id="62d5f-122">The category that is specified for each of those fields refers to the categories in the preceding list.</span></span>
 
### <a name="invoice-common-data-model-entity"></a><span data-ttu-id="62d5f-123">Rēķina Common Data Model elements</span><span class="sxs-lookup"><span data-stu-id="62d5f-123">Invoice Common Data Model entity</span></span>

<span data-ttu-id="62d5f-124">Nākamajā attēlā ir parādīti avoti, kas ir pieejami rēķina elementam.</span><span class="sxs-lookup"><span data-stu-id="62d5f-124">The following illustration shows the fields that are available for the invoice entity.</span></span>

<span data-ttu-id="62d5f-125">[![Rēķina elementam pieejamie lauki](./media/available-fields.png)](./media/available-fields.png)</span><span class="sxs-lookup"><span data-stu-id="62d5f-125">[![Available fields for the invoice entity](./media/available-fields.png)](./media/available-fields.png)</span></span>

<span data-ttu-id="62d5f-126">Apmācībām nav jāatlasa tālāk minētie lauki.</span><span class="sxs-lookup"><span data-stu-id="62d5f-126">The following fields should not be selected for training:</span></span>

- <span data-ttu-id="62d5f-127">**Rēķina konts** (2. kategorija)</span><span class="sxs-lookup"><span data-stu-id="62d5f-127">**Invoice Account** (category 2)</span></span>
- <span data-ttu-id="62d5f-128">**Ir slēgts** (3. kategorija) — šis lauks tiek izmantots, lai filtrētu rēķinus apmācībām (slēgts) un prognozēšanai (nav slēgts).</span><span class="sxs-lookup"><span data-stu-id="62d5f-128">**Is closed** (category 3) – This field is used to filter invoices for training (closed) and prediction (not closed).</span></span>
- <span data-ttu-id="62d5f-129">**Nosaukums** (1. kategorija)</span><span class="sxs-lookup"><span data-stu-id="62d5f-129">**Name** (category 1)</span></span>
- <span data-ttu-id="62d5f-130">**Avota ID** (2. kategorija)</span><span class="sxs-lookup"><span data-stu-id="62d5f-130">**Source Id** (category 2)</span></span>
- <span data-ttu-id="62d5f-131">**Avota ieraksts** (2. kategorija)</span><span class="sxs-lookup"><span data-stu-id="62d5f-131">**Source record** (category 2)</span></span>
- <span data-ttu-id="62d5f-132">**Avota tabula** (2. kategorija)</span><span class="sxs-lookup"><span data-stu-id="62d5f-132">**Source table** (category 2)</span></span>

### <a name="customer-common-data-model-entity"></a><span data-ttu-id="62d5f-133">Debitora Common Data Model elements</span><span class="sxs-lookup"><span data-stu-id="62d5f-133">Customer Common Data Model entity</span></span>

<span data-ttu-id="62d5f-134">Nākamajā attēlā ir parādīti avoti, kas ir pieejami debitora elementam.</span><span class="sxs-lookup"><span data-stu-id="62d5f-134">The following illustration shows the fields that are available for the customer entity.</span></span>

<span data-ttu-id="62d5f-135">[![Debitora elementam pieejamie lauki](./media/related-entities.png)](./media/related-entities.png)</span><span class="sxs-lookup"><span data-stu-id="62d5f-135">[![Available fields for the customer entity](./media/related-entities.png)](./media/related-entities.png)</span></span>

<span data-ttu-id="62d5f-136">Apmācībām nav jāatlasa tālāk minētais lauks.</span><span class="sxs-lookup"><span data-stu-id="62d5f-136">The following field should not be selected for training:</span></span>

- <span data-ttu-id="62d5f-137">**Unikālā rindas atslēga** (2. kategorija)</span><span class="sxs-lookup"><span data-stu-id="62d5f-137">**Row Unique Key** (category 2)</span></span>

## <a name="filters"></a><span data-ttu-id="62d5f-138">Filtri</span><span class="sxs-lookup"><span data-stu-id="62d5f-138">Filters</span></span>

<span data-ttu-id="62d5f-139">Filtri pašlaik neatbalsta debitoru maksājumu prognozēšanas scenāriju.</span><span class="sxs-lookup"><span data-stu-id="62d5f-139">The filters don't currently support the Customer payment predictor scenario.</span></span> <span data-ttu-id="62d5f-140">Tāpēc atlasiet **Izlaist šo darbību** un pārejiet uz kopsavilkuma lapu.</span><span class="sxs-lookup"><span data-stu-id="62d5f-140">Therefore, select **Skip this step**, and continue to the summary page.</span></span>

<span data-ttu-id="62d5f-141">[![Fokusa režīms ar filtriem](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span><span class="sxs-lookup"><span data-stu-id="62d5f-141">[![Focus model with filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="62d5f-142">Paziņojums par konfidencialitāti</span><span class="sxs-lookup"><span data-stu-id="62d5f-142">Privacy notice</span></span>
<span data-ttu-id="62d5f-143">Priekšskatījumiem (1) var tikt izmantots mazāk konfidencialitātes un drošības pasākumu nekā pakalpojumam Dynamics 365 Finance and Operations, (2) tie nav ietverti pakalpojuma līmeņa līgumā par šo pakalpojumu, (3) tos nedrīkst izmantot personas datu vai citu tādu datu apstrādei, uz kuriem attiecas juridiskās vai normatīvās prasības, un (4) tiem tiek nodrošināts ierobežots atbalsts.</span><span class="sxs-lookup"><span data-stu-id="62d5f-143">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
