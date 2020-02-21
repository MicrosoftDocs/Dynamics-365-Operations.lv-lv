---
title: Ieņēmumu atzīšanas pārskats
description: Šajā tēmā ir sniegta informācija par ieņēmumu atzīšanas līdzekli. Šis līdzeklis nodrošina elastīgu platformu, kas ļauj jums noteikt uzņēmuma specifiskos noteikumus, lai varētu atpazīt gan ieņēmumu cenu, gan ieņēmumu grafiku vairāku elementu pasūtījumiem.
author: kweekley
manager: aolson
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: c5a3a90b0065f8cd076117818df810cf10202d29
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030972"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="fe136-104">Ieņēmumu atzīšanas pārskats</span><span class="sxs-lookup"><span data-stu-id="fe136-104">Revenue recognition overview</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="fe136-105">Ieņēmumu atzīšanas līdzekli nav iespējams ieslēgt, izmantojot līdzekļu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="fe136-105">The Revenue recognition feature can't be turned on through Feature management.</span></span> <span data-ttu-id="fe136-106">Pašlaik jāizmanto konfigurācijas atslēgas, lai to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="fe136-106">Currently, you must use configuration keys to turn it on.</span></span>

<span data-ttu-id="fe136-107">Uzņēmumiem nozarēs, kas pārdod vairākus elementus, piemēram, preces, pakalpojumus, abonementus un tā tālāk, ir jābūt iespējai noņemt vairāku elementu pasūtījumus, lai ieņēmumus varētu atpazīt, pamatojoties uz uzņēmumam un nozarei raksturīgu vadlīniju kopu.</span><span class="sxs-lookup"><span data-stu-id="fe136-107">Companies in industries that sell multiple elements, such as products, services, subscriptions, and so on, must be able to break out multi-element orders so that revenue can be recognized based on a set of company-specific and industry-specific guidelines.</span></span>

<span data-ttu-id="fe136-108">Parasti ieņēmumu atzīšanas procesu var izmantot, lai veiktu šos uzdevumus:</span><span class="sxs-lookup"><span data-stu-id="fe136-108">In general, the revenue recognition process can be used to perform these tasks:</span></span>

* <span data-ttu-id="fe136-109">Sadalīt ieņēmumus, lai palīdzētu nodrošināt, ka tiek atzīta atbilstoša ieņēmumu cena, pamatojoties uz vairāku elementu pasūtījumos esošo komponentu vērtību.</span><span class="sxs-lookup"><span data-stu-id="fe136-109">Allocate revenue, to help guarantee that the appropriate revenue price is recognized, based on the value of the components on multi-element orders.</span></span>
* <span data-ttu-id="fe136-110">Atlikt ieņēmumus, pamatojoties uz ieņēmumu grafiku, kas atspoguļo līguma termiņu un procentus ieņēmumu atpazīšanai laika gaitā.</span><span class="sxs-lookup"><span data-stu-id="fe136-110">Defer revenue, based on a revenue schedule that represents the contractual time frame and percentages for recognizing revenue over time.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

<span data-ttu-id="fe136-111">Video [Kā izmantot ieņēmumu atzīšanu programmā Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) (parādīts iepriekš) ir iekļauts [Finance and Operations atskaņošanas sarakstā](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), kas ir pieejams vietnē YouTube.</span><span class="sxs-lookup"><span data-stu-id="fe136-111">The [How to use revenue recognition in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

<span data-ttu-id="fe136-112">Ieņēmumu atzīšanas līdzeklis nodrošina elastīgu platformu, kas ļauj jums noteikt uzņēmuma specifiskos noteikumus, lai varētu atpazīt gan ieņēmumu cenu, gan ieņēmumu grafiku.</span><span class="sxs-lookup"><span data-stu-id="fe136-112">The Revenue recognition feature provides a flexible framework that lets you define company-specific rules for recognizing both the revenue price and the revenue schedule.</span></span>

<span data-ttu-id="fe136-113">Izlaistie produkti tiek izmantoti, lai atbalstītu ieņēmumu atzīšanu pārdošanas pasūtījuma dokumentos.</span><span class="sxs-lookup"><span data-stu-id="fe136-113">Released products are used to support revenue recognition on sales order documents.</span></span> <span data-ttu-id="fe136-114">Izlaistās preces ietver iestatījumus, kas nepieciešami, lai noteiktu ieņēmumu cenu un ieņēmumu grafiku.</span><span class="sxs-lookup"><span data-stu-id="fe136-114">The released products contain the setup that is required to determine the revenue price and the revenue schedule.</span></span> <span data-ttu-id="fe136-115">Pārdošanas pasūtījumu var izveidot no laika un materiālu projekta.</span><span class="sxs-lookup"><span data-stu-id="fe136-115">The sales order can originate from a Time and materials project.</span></span>

<span data-ttu-id="fe136-116">Uzņēmumi var izmantot ieņēmumu grafika funkcionalitāti, neizmantojot ieņēmumu cenas funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="fe136-116">Companies can use the revenue schedule functionality without using the revenue price functionality.</span></span> <span data-ttu-id="fe136-117">Tāpēc pārdošanas pasūtījuma rindu cena tiks izmantota kā ieņēmumi vai atliktie ieņēmumi.</span><span class="sxs-lookup"><span data-stu-id="fe136-117">Therefore, the price on the sales order lines will be used as either revenue or deferred revenue.</span></span> <span data-ttu-id="fe136-118">Ja pārdošanas pasūtījuma rindā pastāv ieņēmumu grafiks, pārdošanas pasūtījuma rindā norādītā cena tiks atlikta.</span><span class="sxs-lookup"><span data-stu-id="fe136-118">If a revenue schedule exists on the sales order line, the price on the sales order line will be deferred.</span></span> <span data-ttu-id="fe136-119">Ja pārdošanas pasūtījuma rindā nav ieņēmumu grafika, pārdošanas pasūtījuma rindā norādītā cena tiks grāmatota ieņēmumu kontā, kad tiek izrakstīts rēķins.</span><span class="sxs-lookup"><span data-stu-id="fe136-119">If a revenue schedule doesn't exist on the sales order line, the price on the sales order line will be posted to a revenue account when it's invoiced.</span></span>

<span data-ttu-id="fe136-120">Ieņēmumu cena tiek aprēķināta vai nu pēc pārdošanas pasūtījuma apstiprināšanas, vai tad, kad rēķins ir iegrāmatots.</span><span class="sxs-lookup"><span data-stu-id="fe136-120">The revenue price is calculated either when the sales order is confirmed or when the invoice is posted.</span></span> <span data-ttu-id="fe136-121">Lai priekšskatītu ieņēmumu cenu pirms rēķina grāmatošanas, ir jāapstiprina pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="fe136-121">To preview the revenue price before the invoice is posted, you must confirm the sales order.</span></span>

<span data-ttu-id="fe136-122">Kad pārdošanas pasūtījums tiek apstiprināts, tiek izveidots arī prognozētais ieņēmumu grafiks, ja pārdošanas pasūtījuma rindai ir ieņēmumu grafiks.</span><span class="sxs-lookup"><span data-stu-id="fe136-122">When the sales order is confirmed, an expected revenue schedule is also created if any sales order line has a revenue schedule.</span></span> <span data-ttu-id="fe136-123">Kad pārdošanas pasūtījums ir iekļauts rēķinā, paredzamais ieņēmumu grafiks tiek dzēsts un paredzamais ieņēmumu grafiks tiek aizstāts ar faktisko ieņēmumu atzīšanas grafiku.</span><span class="sxs-lookup"><span data-stu-id="fe136-123">When the sales order is invoiced, the expected revenue schedule is deleted, and the expected revenue schedule is replaced with the actual revenue recognition schedule.</span></span>

<span data-ttu-id="fe136-124">Detalizēta informācija par ieņēmumu atzīšanas grafiku tiek uzturēta katrai pārdošanas pasūtījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="fe136-124">The details of the revenue recognition schedule are maintained for each sales order line.</span></span> <span data-ttu-id="fe136-125">Tāpēc ieņēmumu atzīšanas vadītājs var skatīt detalizētu informāciju un var nodot rindas ieņēmumiem, kad līgumsaistības ir pabeigtas.</span><span class="sxs-lookup"><span data-stu-id="fe136-125">Therefore, the revenue recognition manager can view the details and can release lines to revenue when the contractual obligation has been completed.</span></span> <span data-ttu-id="fe136-126">Katra perioda beigās ieņēmumu atzīšanas vadītājs var izveidot ieņēmumu žurnālu, lai izlaistu visas grafika rindas, kas maksājamas tieši tajā datumā vai pirms datuma, ko viņš vai viņa definē.</span><span class="sxs-lookup"><span data-stu-id="fe136-126">At the end of each period, the revenue recognition manager can create a revenue journal to release any schedule lines that are due on or before a date that he or she defines.</span></span> <span data-ttu-id="fe136-127">Šis ieņēmumu žurnāls netiek grāmatots nekavējoties.</span><span class="sxs-lookup"><span data-stu-id="fe136-127">This revenue journal isn't posted immediately.</span></span> <span data-ttu-id="fe136-128">Tāpēc ieņēmumu atzīšanas vadītājs var pārbaudīt, vai pareizās summas tiek atbrīvotas no atliktajiem ieņēmumiem uz faktiskajiem ieņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="fe136-128">Therefore, the revenue recognition manager can verify that the correct amounts are being released from deferred revenue to actual revenue.</span></span>

<span data-ttu-id="fe136-129">Ja līguma izmaiņa rada jaunu pārdošanas pasūtījuma rindu, kas jāpievieno esošajam pārdošanas pasūtījumam vai jaunam pārdošanas pasūtījumam, var tikt palaists pārdales process, lai labotu ieņēmumu cenu visās rindās pārdošanas pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="fe136-129">If a contractual change causes a new sales order line to be added either to the existing sales order or a new sales order, a reallocation process can be run to correct the revenue price across all lines on the sales orders.</span></span>
