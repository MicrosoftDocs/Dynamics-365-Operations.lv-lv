---
title: Debitoru vecumstruktūras informācijas iestatīšana un ģenerēšana
description: Šis ceļvedis jums palīdzēs iestatīt vecumstruktūras perioda definīciju, novecot debitoru bilances un skatīt bilances sarakstā Vecas bilances un lapā Iekasēšanas.
author: mikefalkner
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 77b5dd5feb16cc3bd6d64b6520cc47087c5b5224
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834371"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a><span data-ttu-id="d5088-103">Debitoru vecumstruktūras informācijas iestatīšana un ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="d5088-103">Set up and generate accounts receivable aging information</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d5088-104">Šis ceļvedis jums palīdzēs iestatīt vecumstruktūras perioda definīciju, novecot debitoru bilances un skatīt bilances sarakstā Vecas bilances un lapā Iekasēšanas.</span><span class="sxs-lookup"><span data-stu-id="d5088-104">This guide will help you set up an aging period definition, age customer balances, and view balances in the Aged balance list and the Collections page.</span></span> <span data-ttu-id="d5088-105">Šajā ierakstā tiek izmantots USMF demonstrācijas uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="d5088-105">This recording uses the USMF demo company.</span></span>


## <a name="create-an-aging-period-definition"></a><span data-ttu-id="d5088-106">Izveidot vecumstruktūras perioda definīciju</span><span class="sxs-lookup"><span data-stu-id="d5088-106">Create an aging period definition</span></span>
1. <span data-ttu-id="d5088-107">Dodieties uz **Navigācijas rūts > Moduļi > Kredīts un iekasēšana > Iestatīšana > Vecumstruktūras perioda definīcijas**.</span><span class="sxs-lookup"><span data-stu-id="d5088-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Aging period definitions**.</span></span>
2. <span data-ttu-id="d5088-108">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="d5088-108">Click **New**.</span></span>
3. <span data-ttu-id="d5088-109">Laukā **Vecumstruktūras perioda definīcija** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d5088-109">In the **Aging period definition** field, type a value.</span></span>
4. <span data-ttu-id="d5088-110">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d5088-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="d5088-111">Noklikšķiniet uz **Pievienot zemāk**, lai ievietotu jaunu vecumstruktūras periodu.</span><span class="sxs-lookup"><span data-stu-id="d5088-111">Click **Add below** to insert a new aging period.</span></span>
6. <span data-ttu-id="d5088-112">Laukā **Periods** ievadiet aprakstu, ko rādīt vecumstruktūras atskaitēs.</span><span class="sxs-lookup"><span data-stu-id="d5088-112">In the **Period** field, enter the description to show on aging reports.</span></span>
7. <span data-ttu-id="d5088-113">Laukā **Vienība** ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="d5088-113">In the **Unit** field, enter a number.</span></span>
8. <span data-ttu-id="d5088-114">Laukā **Intervāls** atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="d5088-114">In the **Interval** field, select an option.</span></span> <span data-ttu-id="d5088-115">Virsgrāmatas periods saskaņo periodu ar jūsu virsgrāmatas kalendāru.</span><span class="sxs-lookup"><span data-stu-id="d5088-115">Ledger period matches the period to your ledger calendar.</span></span> <span data-ttu-id="d5088-116">Diena, nedēļa, mēnesis, ceturksnis un gadi definē intervāla lielumu pēc datuma tipa.</span><span class="sxs-lookup"><span data-stu-id="d5088-116">Day, week, month, quarter and years define the size of the interval by date type.</span></span> <span data-ttu-id="d5088-117">Ar vērtību Neierobežots tiek atlasītas visas transakcijas pirms vai pēc iepriekšējā perioda, atkarībā no tā, vai tas ir pirmais vai pēdējais periods.</span><span class="sxs-lookup"><span data-stu-id="d5088-117">Unlimited selects all transactions before or after the previous period, depending on whether it is the first or last period.</span></span>  
9. <span data-ttu-id="d5088-118">Laukā **Vecumstruktūras indikators** atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="d5088-118">In the **Aging indicator** field, select an option.</span></span>
10. <span data-ttu-id="d5088-119">Atlasiet periodu režģa augšpusē.</span><span class="sxs-lookup"><span data-stu-id="d5088-119">Select the period at the top of the grid.</span></span> <span data-ttu-id="d5088-120">Atjaunināt aprakstu, lai aprakstītu visvecāko periodu vecumstruktūras perioda definīcijā</span><span class="sxs-lookup"><span data-stu-id="d5088-120">Update the description to describe the oldest period in the aging period definition</span></span>
11. <span data-ttu-id="d5088-121">Laukā **Periods** ievadiet jaunu vecumstruktūras perioda aprakstu.</span><span class="sxs-lookup"><span data-stu-id="d5088-121">In the **Period** field, enter the new description of the aging period.</span></span>
12. <span data-ttu-id="d5088-122">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d5088-122">Close the page.</span></span>

## <a name="age-the-balances"></a><span data-ttu-id="d5088-123">Novecot bilances</span><span class="sxs-lookup"><span data-stu-id="d5088-123">Age the balances</span></span>
1. <span data-ttu-id="d5088-124">Pārejiet uz sadaļu **Kredīts un iekasēšana > Periodiskie uzdevumi > Vecas debitoru bilances**.</span><span class="sxs-lookup"><span data-stu-id="d5088-124">Go to **Credit and collections > Periodic tasks > Age customer balances**.</span></span>
2. <span data-ttu-id="d5088-125">Laukā **Vecumstruktūras perioda definīcija** atlasiet savu izveidoto vecumstruktūras perioda definīciju.</span><span class="sxs-lookup"><span data-stu-id="d5088-125">In the **Aging period definition** field, select the aging period definition that you created.</span></span>
    + <span data-ttu-id="d5088-126">Katrai vecumstruktūras perioda definīcijai jums var būt viens aktīvs momentuzņēmums.</span><span class="sxs-lookup"><span data-stu-id="d5088-126">You can have one active snapshot for each aging period definition.</span></span>  
    + <span data-ttu-id="d5088-127">Visi debitori tiek apstrādāti pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="d5088-127">All customers are processed by default.</span></span> <span data-ttu-id="d5088-128">Šo atlasi varat izmantot, lai aprēķinātu vienu debitoru iekasēšanas pūlu.</span><span class="sxs-lookup"><span data-stu-id="d5088-128">You can use this selection to calculate a single collections pool of customers.</span></span>  
    + <span data-ttu-id="d5088-129">Atlasiet datumu no transakcijas, kas tiks izmantots vecumstruktūrai.</span><span class="sxs-lookup"><span data-stu-id="d5088-129">Select the date from the transaction that you will use for the aging.</span></span>  
    + <span data-ttu-id="d5088-130">Vecumstruktūrai atlasiet datumu “kopš”.</span><span class="sxs-lookup"><span data-stu-id="d5088-130">Select an "as of" date for aging.</span></span> <span data-ttu-id="d5088-131">Noklusējuma vērtība ir šodiena, bet, ja šo lauku maināt uz Atlasītais datums, varēsiet izvēlēties nepieciešamo datumu.</span><span class="sxs-lookup"><span data-stu-id="d5088-131">The default is today but, if you change this field to Selected date, you will be able to pick the date that you want.</span></span> <span data-ttu-id="d5088-132">Pakešapstrādei lietojiet Šodienas datums.</span><span class="sxs-lookup"><span data-stu-id="d5088-132">For batch processing, use Today's date.</span></span>  
3. <span data-ttu-id="d5088-133">Izvērsiet diapazonu **Uzņēmums**.</span><span class="sxs-lookup"><span data-stu-id="d5088-133">Expand the **Company** range.</span></span> <span data-ttu-id="d5088-134">Varat atlasīt uzņēmumus, kas tiks iekļauti momentuzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="d5088-134">You can select the companies that will be included in the snapshot.</span></span> <span data-ttu-id="d5088-135">Pašreizējais uzņēmums tiek atlasīts pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="d5088-135">The current company is selected by default.</span></span>
4. <span data-ttu-id="d5088-136">Noklikšķiniet uz **Labi**, lai apstrādātu šo momentuzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="d5088-136">Click **Ok** to process the snapshot.</span></span> <span data-ttu-id="d5088-137">Tas aizņems kādu laiku, tāpēc pagaidiet, līdz slīdnis izzūd, un pārbaudiet, vai ziņojumu centrā ir kāds ziņojums.</span><span class="sxs-lookup"><span data-stu-id="d5088-137">It will take some time so wait for the slider to disappear and check the message center for a message.</span></span>

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a><span data-ttu-id="d5088-138">Skatīt bilances sarakstā Vecas bilances un lapā Iekasēšana</span><span class="sxs-lookup"><span data-stu-id="d5088-138">View the balances on the Aged balances list and on the Collection page</span></span>
1. <span data-ttu-id="d5088-139">Pārejiet uz sadaļu **Kredīts un iekasēšana > Iekasēšana > Vecas bilances**.</span><span class="sxs-lookup"><span data-stu-id="d5088-139">Go to **Credit and collections > Collections > Aged balances**.</span></span> <span data-ttu-id="d5088-140">Saraksta lapā tiek rādītas bilances šim debitoram.</span><span class="sxs-lookup"><span data-stu-id="d5088-140">The list page shows the balances for the customer.</span></span> <span data-ttu-id="d5088-141">Vecumstruktūras ikona rāda vecumstruktūras periodu vecākajai transakcijai.</span><span class="sxs-lookup"><span data-stu-id="d5088-141">The aging icon shows the aging period for the oldest transaction.</span></span>  
2. <span data-ttu-id="d5088-142">Atlasiet debitoru ar bilanci.</span><span class="sxs-lookup"><span data-stu-id="d5088-142">Select a customer with a balance.</span></span>
3. <span data-ttu-id="d5088-143">Izvērsiet apgabala lodziņu **Vecumstruktūras fakts**, lai skatītu vecās bilances.</span><span class="sxs-lookup"><span data-stu-id="d5088-143">Expand the **Aging fact** box area to view the aged balances.</span></span> <span data-ttu-id="d5088-144">Vecumstruktūras perioda definīcija šai papildinformācijai tiek ņemta no parametros norādītās noklusējuma vecumstruktūras perioda definīcijas.</span><span class="sxs-lookup"><span data-stu-id="d5088-144">The aging period definition for the fact box is taken from the default aging period definition specified in the parameters.</span></span> <span data-ttu-id="d5088-145">Varat to mainīt, izmantojot izvēlni Iekasēt.</span><span class="sxs-lookup"><span data-stu-id="d5088-145">You can change it using the Collect menu.</span></span>  

