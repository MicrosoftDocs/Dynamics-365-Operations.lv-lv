---
title: Ieņēmumu atzīšanas pārskats
description: Šajā tēmā ir sniegta informācija par ieņēmumu atzīšanas līdzekli. Šis līdzeklis nodrošina elastīgu platformu, kas ļauj jums noteikt uzņēmuma specifiskos noteikumus, lai varētu atpazīt gan ieņēmumu cenu, gan ieņēmumu grafiku vairāku elementu pasūtījumiem.
author: kweekley
manager: aolson
ms.date: 08/24/2018
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
ms.openlocfilehash: d1aeb0cf556582ff53ca00c6bb8d863a088950b9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184121"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="93e3b-104">Ieņēmumu atzīšanas pārskats</span><span class="sxs-lookup"><span data-stu-id="93e3b-104">Revenue recognition overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!NOTE]
> <span data-ttu-id="93e3b-105">Ieņēmumu atzīšanas līdzekli vēl nav iespējams ieslēgt, izmantojot līdzekļu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="93e3b-105">The Revenue recognition feature can't yet be turned on through Feature management.</span></span> <span data-ttu-id="93e3b-106">Pašlaik jāizmanto konfigurācijas atslēgas, lai to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="93e3b-106">Currently, you must use configuration keys to turn it on.</span></span>

<span data-ttu-id="93e3b-107">Uzņēmumiem nozarēs, kas pārdod vairākus elementus, piemēram, preces, pakalpojumus, abonementus un tā tālāk, ir jābūt iespējai noņemt vairāku elementu pasūtījumus, lai ieņēmumus varētu atpazīt, pamatojoties uz uzņēmumam un nozarei raksturīgu vadlīniju kopu.</span><span class="sxs-lookup"><span data-stu-id="93e3b-107">Companies in industries that sell multiple elements, such as products, services, subscriptions, and so on, must be able to break out multi-element orders so that revenue can be recognized based on a set of company-specific and industry-specific guidelines.</span></span>

<span data-ttu-id="93e3b-108">Parasti ieņēmumu atzīšanas procesu var izmantot, lai veiktu šos uzdevumus:</span><span class="sxs-lookup"><span data-stu-id="93e3b-108">In general, the revenue recognition process can be used to perform these tasks:</span></span>

* <span data-ttu-id="93e3b-109">Sadalīt ieņēmumus, lai palīdzētu nodrošināt, ka tiek atzīta atbilstoša ieņēmumu cena, pamatojoties uz vairāku elementu pasūtījumos esošo komponentu vērtību.</span><span class="sxs-lookup"><span data-stu-id="93e3b-109">Allocate revenue, to help guarantee that the appropriate revenue price is recognized, based on the value of the components on multi-element orders.</span></span>
* <span data-ttu-id="93e3b-110">Atlikt ieņēmumus, pamatojoties uz ieņēmumu grafiku, kas atspoguļo līguma termiņu un procentus ieņēmumu atpazīšanai laika gaitā.</span><span class="sxs-lookup"><span data-stu-id="93e3b-110">Defer revenue, based on a revenue schedule that represents the contractual time frame and percentages for recognizing revenue over time.</span></span>

<span data-ttu-id="93e3b-111">Ieņēmumu atzīšanas līdzeklis nodrošina elastīgu platformu, kas ļauj jums noteikt uzņēmuma specifiskos noteikumus, lai varētu atpazīt gan ieņēmumu cenu, gan ieņēmumu grafiku.</span><span class="sxs-lookup"><span data-stu-id="93e3b-111">The Revenue recognition feature provides a flexible framework that lets you define company-specific rules for recognizing both the revenue price and the revenue schedule.</span></span>

<span data-ttu-id="93e3b-112">Izlaistie produkti tiek izmantoti, lai atbalstītu ieņēmumu atzīšanu pārdošanas pasūtījuma dokumentos.</span><span class="sxs-lookup"><span data-stu-id="93e3b-112">Released products are used to support revenue recognition on sales order documents.</span></span> <span data-ttu-id="93e3b-113">Izlaistās preces ietver iestatījumus, kas nepieciešami, lai noteiktu ieņēmumu cenu un ieņēmumu grafiku.</span><span class="sxs-lookup"><span data-stu-id="93e3b-113">The released products contain the setup that is required to determine the revenue price and the revenue schedule.</span></span> <span data-ttu-id="93e3b-114">Pārdošanas pasūtījumu var izveidot no laika un materiālu projekta.</span><span class="sxs-lookup"><span data-stu-id="93e3b-114">The sales order can originate from a Time and materials project.</span></span>

<span data-ttu-id="93e3b-115">Uzņēmumi var izmantot ieņēmumu grafika funkcionalitāti, neizmantojot ieņēmumu cenas funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="93e3b-115">Companies can use the revenue schedule functionality without using the revenue price functionality.</span></span> <span data-ttu-id="93e3b-116">Tāpēc pārdošanas pasūtījuma rindu cena tiks izmantota kā ieņēmumi vai atliktie ieņēmumi.</span><span class="sxs-lookup"><span data-stu-id="93e3b-116">Therefore, the price on the sales order lines will be used as either revenue or deferred revenue.</span></span> <span data-ttu-id="93e3b-117">Ja pārdošanas pasūtījuma rindā pastāv ieņēmumu grafiks, pārdošanas pasūtījuma rindā norādītā cena tiks atlikta.</span><span class="sxs-lookup"><span data-stu-id="93e3b-117">If a revenue schedule exists on the sales order line, the price on the sales order line will be deferred.</span></span> <span data-ttu-id="93e3b-118">Ja pārdošanas pasūtījuma rindā nav ieņēmumu grafika, pārdošanas pasūtījuma rindā norādītā cena tiks grāmatota ieņēmumu kontā, kad tiek izrakstīts rēķins.</span><span class="sxs-lookup"><span data-stu-id="93e3b-118">If a revenue schedule doesn't exist on the sales order line, the price on the sales order line will be posted to a revenue account when it's invoiced.</span></span>

<span data-ttu-id="93e3b-119">Ieņēmumu cena tiek aprēķināta vai nu pēc pārdošanas pasūtījuma apstiprināšanas, vai tad, kad rēķins ir iegrāmatots.</span><span class="sxs-lookup"><span data-stu-id="93e3b-119">The revenue price is calculated either when the sales order is confirmed or when the invoice is posted.</span></span> <span data-ttu-id="93e3b-120">Lai priekšskatītu ieņēmumu cenu pirms rēķina grāmatošanas, ir jāapstiprina pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="93e3b-120">To preview the revenue price before the invoice is posted, you must confirm the sales order.</span></span>

<span data-ttu-id="93e3b-121">Kad pārdošanas pasūtījums tiek apstiprināts, tiek izveidots arī prognozētais ieņēmumu grafiks, ja pārdošanas pasūtījuma rindai ir ieņēmumu grafiks.</span><span class="sxs-lookup"><span data-stu-id="93e3b-121">When the sales order is confirmed, an expected revenue schedule is also created if any sales order line has a revenue schedule.</span></span> <span data-ttu-id="93e3b-122">Kad pārdošanas pasūtījums ir iekļauts rēķinā, paredzamais ieņēmumu grafiks tiek dzēsts un paredzamais ieņēmumu grafiks tiek aizstāts ar faktisko ieņēmumu atzīšanas grafiku.</span><span class="sxs-lookup"><span data-stu-id="93e3b-122">When the sales order is invoiced, the expected revenue schedule is deleted, and the expected revenue schedule is replaced with the actual revenue recognition schedule.</span></span>

<span data-ttu-id="93e3b-123">Detalizēta informācija par ieņēmumu atzīšanas grafiku tiek uzturēta katrai pārdošanas pasūtījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="93e3b-123">The details of the revenue recognition schedule are maintained for each sales order line.</span></span> <span data-ttu-id="93e3b-124">Tāpēc ieņēmumu atzīšanas vadītājs var skatīt detalizētu informāciju un var nodot rindas ieņēmumiem, kad līgumsaistības ir pabeigtas.</span><span class="sxs-lookup"><span data-stu-id="93e3b-124">Therefore, the revenue recognition manager can view the details and can release lines to revenue when the contractual obligation has been completed.</span></span> <span data-ttu-id="93e3b-125">Katra perioda beigās ieņēmumu atzīšanas vadītājs var izveidot ieņēmumu žurnālu, lai izlaistu visas grafika rindas, kas maksājamas tieši tajā datumā vai pirms datuma, ko viņš vai viņa definē.</span><span class="sxs-lookup"><span data-stu-id="93e3b-125">At the end of each period, the revenue recognition manager can create a revenue journal to release any schedule lines that are due on or before a date that he or she defines.</span></span> <span data-ttu-id="93e3b-126">Šis ieņēmumu žurnāls netiek grāmatots nekavējoties.</span><span class="sxs-lookup"><span data-stu-id="93e3b-126">This revenue journal isn't posted immediately.</span></span> <span data-ttu-id="93e3b-127">Tāpēc ieņēmumu atzīšanas vadītājs var pārbaudīt, vai pareizās summas tiek atbrīvotas no atliktajiem ieņēmumiem uz faktiskajiem ieņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="93e3b-127">Therefore, the revenue recognition manager can verify that the correct amounts are being released from deferred revenue to actual revenue.</span></span>

<span data-ttu-id="93e3b-128">Ja līguma izmaiņa rada jaunu pārdošanas pasūtījuma rindu, kas jāpievieno esošajam pārdošanas pasūtījumam vai jaunam pārdošanas pasūtījumam, var tikt palaists pārdales process, lai labotu ieņēmumu cenu visās rindās pārdošanas pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="93e3b-128">If a contractual change causes a new sales order line to be added either to the existing sales order or a new sales order, a reallocation process can be run to correct the revenue price across all lines on the sales orders.</span></span>
