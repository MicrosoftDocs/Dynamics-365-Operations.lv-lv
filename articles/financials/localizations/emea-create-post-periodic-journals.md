---
title: "Sadalīt periodus periodiskajos žurnālos"
description: "Periodiskos žurnālus dažreiz sauc par cikliskiem žurnāliem, jo summa, teksts un cita informācija tiek atkārtota katru reizi, kad tiek grāmatots šis žurnāls. Veidojot žurnālu, norādiet atkārtošanās perioda intervālu, piemēram, dienas vai mēnešus. Norādiet arī to periodu skaitu, kuros jāgrāmato žurnāls."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261354
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 73ccfc906e8d7a91e7bae5ae21d9ddad9d58f109
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="split-periods-in-periodic-journals"></a><span data-ttu-id="89db0-105">Sadalīt periodus periodiskajos žurnālos</span><span class="sxs-lookup"><span data-stu-id="89db0-105">Split periods in periodic journals</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="89db0-106">Periodiskos žurnālus dažreiz sauc par cikliskiem žurnāliem, jo summa, teksts un cita informācija tiek atkārtota katru reizi, kad tiek grāmatots šis žurnāls.</span><span class="sxs-lookup"><span data-stu-id="89db0-106">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the journal is posted.</span></span> <span data-ttu-id="89db0-107">Veidojot žurnālu, norādiet atkārtošanās perioda intervālu, piemēram, dienas vai mēnešus.</span><span class="sxs-lookup"><span data-stu-id="89db0-107">When you create the journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="89db0-108">Norādiet arī to periodu skaitu, kuros jāgrāmato žurnāls.</span><span class="sxs-lookup"><span data-stu-id="89db0-108">You also specify the number of periods for which the journal will be posted.</span></span>

<span data-ttu-id="89db0-109">Lai periodiski izgūtu un grāmatotu transakciju rindas, varat lietot lapu **Periodiskie žurnāli**.</span><span class="sxs-lookup"><span data-stu-id="89db0-109">To repeatedly retrieve and post transaction lines, you can use the **Periodic journals** page.</span></span> <span data-ttu-id="89db0-110">Juridiskajām personām Čehijā, Igaunijā, Ungārijā, Latvijā, Lietuvā, Polijā un Krievijā lapa **Periodiskie žurnāli** ir paplašināta ar funkcionalitāti sadalīšanai pa periodiem.</span><span class="sxs-lookup"><span data-stu-id="89db0-110">For legal entities in Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, and Russia, the **Periodic journals** page is extended by the split for periods functionality.</span></span> <span data-ttu-id="89db0-111">Papildinformāciju skatiet rakstā [Periodiska žurnāla grāmatošana](../general-ledger/tasks/post-periodic-journals.md)</span><span class="sxs-lookup"><span data-stu-id="89db0-111">For more information, see [Post a periodic journal](../general-ledger/tasks/post-periodic-journals.md)</span></span>

### <a name="example-split-for-periods-in-periodic-journals"></a><span data-ttu-id="89db0-112">Piemērs: sadalīt pa periodiem periodiskajos žurnālos</span><span class="sxs-lookup"><span data-stu-id="89db0-112">Example: Split for periods in periodic journals</span></span>

<span data-ttu-id="89db0-113">Kāda apdrošināšanas sabiedrība jūsu uzņēmumam piedāvā atlaidi, veicot apdrošināšanas polises priekšapmaksu par visu gadu.</span><span class="sxs-lookup"><span data-stu-id="89db0-113">An insurance company offers your organization a discount for prepaying the insurance policy for an entire year.</span></span> <span data-ttu-id="89db0-114">Maksājums tiek grāmatots aktīvu kontā, piemēram, kā priekšapmaksas apdrošināšana.</span><span class="sxs-lookup"><span data-stu-id="89db0-114">The payment is posted to an asset account such as prepaid insurance.</span></span> <span data-ttu-id="89db0-115">Pēc tam jūs dzēšat ikmēneša apdrošināšanas izdevumus visa gada garumā, izveidojot periodisku žurnālu, kas ietver priekšapmaksas apdrošināšanas konta kredītu un apdrošināšanas izdevumu konta debetu.</span><span class="sxs-lookup"><span data-stu-id="89db0-115">You then amortize your monthly insurance expense throughout the year by creating a periodic journal that contains a credit to the prepaid insurance account and a debit to an insurance expense account.</span></span> <span data-ttu-id="89db0-116">Šajā gadījumā varat lietot funkcionalitāti sadalīšanai pa periodiem.</span><span class="sxs-lookup"><span data-stu-id="89db0-116">In this case, you can use the split for periods functionality.</span></span> <span data-ttu-id="89db0-117">Lapas **Periodisko žurnālu** **rindas** darbību rūtī noklikšķiniet uz pogas **Sadalīt pa periodiem**, un pēc tam norādiet tālāk uzskaitīto lauku vērtības.</span><span class="sxs-lookup"><span data-stu-id="89db0-117">Click the **Split for periods** button on the Action Pane on the **Periodic journal** **lines** page, and then specify the following fields.</span></span>

|                       |                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89db0-118">**Lauks**</span><span class="sxs-lookup"><span data-stu-id="89db0-118">**Field**</span></span>             | <span data-ttu-id="89db0-119">**Apraksts**</span><span class="sxs-lookup"><span data-stu-id="89db0-119">**Description**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="89db0-120">**Sākuma datums**</span><span class="sxs-lookup"><span data-stu-id="89db0-120">**Start date**</span></span>        | <span data-ttu-id="89db0-121">Atlasiet datumu pirmajai periodiskā žurnāla rindai.</span><span class="sxs-lookup"><span data-stu-id="89db0-121">Select the date for the first periodic journal line.</span></span>                                                                                                                                                        |
| <span data-ttu-id="89db0-122">**Periodu skaits**</span><span class="sxs-lookup"><span data-stu-id="89db0-122">**Number of periods**</span></span> | <span data-ttu-id="89db0-123">Ievadiet skaitu, cik periodos sadalīt šo žurnāla rindu.</span><span class="sxs-lookup"><span data-stu-id="89db0-123">Enter the number of periods across which to split the journal line.</span></span> <span data-ttu-id="89db0-124">Šī vērtība nosaka, cik daudz jaunu darījumu tiek ģenerēts.</span><span class="sxs-lookup"><span data-stu-id="89db0-124">This value determines how many new transactions are generated.</span></span> <span data-ttu-id="89db0-125">Darījuma summa ir vienmērīgi sadalīta pa jaunajiem darījumiem.</span><span class="sxs-lookup"><span data-stu-id="89db0-125">The transaction amount is distributed evenly among the new transactions.</span></span> |
| <span data-ttu-id="89db0-126">**Vienība**</span><span class="sxs-lookup"><span data-stu-id="89db0-126">**Unit**</span></span>              | <span data-ttu-id="89db0-127">Atlasiet perioda mērvienību.</span><span class="sxs-lookup"><span data-stu-id="89db0-127">Select the unit of measure for the period.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="89db0-128">**Perioda intervāls**</span><span class="sxs-lookup"><span data-stu-id="89db0-128">**Period interval**</span></span>   | <span data-ttu-id="89db0-129">Nosakiet intervālu starp grāmatošanas periodiem.</span><span class="sxs-lookup"><span data-stu-id="89db0-129">Determine an interval between posting periods.</span></span>                                                                                                                                                              |

<span data-ttu-id="89db0-130">Piemēram, lai ģenerētu ceturkšņa grāmatojumus, laukā **Periodu skaits** ievadiet **4**, laukā **Vienība** atlasiet vērtību **Mēneši** un laukā **Periodu intervāls** ievadiet **3**.</span><span class="sxs-lookup"><span data-stu-id="89db0-130">For example, to generate quarterly postings, enter **4** in the **Number of periods** field, select **Months** in the **Unit** field, and enter **3** in the **Period interval** field.</span></span> <span data-ttu-id="89db0-131">Sistēma ģenerē četras žurnāla rindas ar 3 mēnešu intervāliem, un katra no tām ietver vienu ceturto daļu no jūsu ievadītās žurnāla rindas summas.</span><span class="sxs-lookup"><span data-stu-id="89db0-131">The system generates four journal lines, each for one fourth of the journal line amount that you entered, at 3-month intervals.</span></span> <span data-ttu-id="89db0-132">Līdzīga funkcionalitāte ir pieejama arī virsgrāmatas žurnālam.</span><span class="sxs-lookup"><span data-stu-id="89db0-132">Similar functionality is also available for the general journal.</span></span> <span data-ttu-id="89db0-133">Kad apskatāt virsgrāmatas žurnāla rindas, atlasiet **Periodiskais žurnāls** &gt; **Saglabāt žurnālu**.</span><span class="sxs-lookup"><span data-stu-id="89db0-133">When viewing general journal lines, select **Period journal** &gt; **Save journal**.</span></span>




