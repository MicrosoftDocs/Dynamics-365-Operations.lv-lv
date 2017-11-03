---
title: "Piegādes grafiki"
description: "Piegādes grafiki ļauj izsekot pasūtījuma rindu daudzumam, ja vienam pārdošanas pasūtījumam, pārdošanas piedāvājumam vai pirkšanas pasūtījumam tiek izmantotas vairākas piegādes."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ceb568cc223a631f704caf2417f1a3bd56b56288
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="delivery-schedules"></a><span data-ttu-id="b69a1-103">Piegādes grafiki</span><span class="sxs-lookup"><span data-stu-id="b69a1-103">Delivery schedules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b69a1-104">Piegādes grafiki ļauj izsekot pasūtījuma rindu daudzumam, ja vienam pārdošanas pasūtījumam, pārdošanas piedāvājumam vai pirkšanas pasūtījumam tiek izmantotas vairākas piegādes.</span><span class="sxs-lookup"><span data-stu-id="b69a1-104">Delivery schedules allow you to track order line quantity when you are using multiple deliveries for a single sales order, sales quotation, or purchase order.</span></span>

<span data-ttu-id="b69a1-105">Izmantojiet piegādes grafikus, kad kopējais daudzums pasūtījuma vai piedāvājuma rindā ir jāpiegādā vairākos sūtījumos.</span><span class="sxs-lookup"><span data-stu-id="b69a1-105">Use a delivery schedule when the total quantity on an order or quotation line must be delivered in multiple shipments.</span></span> <span data-ttu-id="b69a1-106">Atsevišķi sūtījumi tiek norādīti ar piegādes rindām.</span><span class="sxs-lookup"><span data-stu-id="b69a1-106">Individual shipments are represented by delivery lines.</span></span> <span data-ttu-id="b69a1-107">Divas vai vairākas piegādes rindas veido vienu piegādes grafiku.</span><span class="sxs-lookup"><span data-stu-id="b69a1-107">Two or more delivery lines make up one delivery schedule.</span></span> <span data-ttu-id="b69a1-108">Piegādes rindām var būt atšķirīgi piegādes datumi, daudzumi, piegādes režīmi un noliktavas dimensijas, piemēram, vieta un noliktava.</span><span class="sxs-lookup"><span data-stu-id="b69a1-108">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span>  

<span data-ttu-id="b69a1-109">**Piegādes grafika piemērs**</span><span class="sxs-lookup"><span data-stu-id="b69a1-109">**Example of a delivery schedule**</span></span>

|                                   |                                          |
|-----------------------------------|------------------------------------------|
| <span data-ttu-id="b69a1-110">Kopējais pasūtījums (sākotnējā pasūtījuma rinda)</span><span class="sxs-lookup"><span data-stu-id="b69a1-110">Total order (original order line)</span></span> | <span data-ttu-id="b69a1-111">600 krēsli</span><span class="sxs-lookup"><span data-stu-id="b69a1-111">600 chairs</span></span>                               |
| <span data-ttu-id="b69a1-112">Pieprasītais piegādes grafiks</span><span class="sxs-lookup"><span data-stu-id="b69a1-112">Requested delivery schedule</span></span>       | <span data-ttu-id="b69a1-113">100 krēslu mēnesī</span><span class="sxs-lookup"><span data-stu-id="b69a1-113">100 chairs per month</span></span>                     |
| <span data-ttu-id="b69a1-114">Pieprasītais piegādes laiks</span><span class="sxs-lookup"><span data-stu-id="b69a1-114">Requested time frame for delivery</span></span> | <span data-ttu-id="b69a1-115">6 mēneši, katra mēneša pirmajā dienā</span><span class="sxs-lookup"><span data-stu-id="b69a1-115">6 months, on the first day of each month</span></span> |

<span data-ttu-id="b69a1-116">Šādā gadījumā klients pieprasa piegādāt 600 krēslus paketēs pa 100 krēsliem sešu mēnešu laikā.</span><span class="sxs-lookup"><span data-stu-id="b69a1-116">In this scenario, the customer requests delivery of 600 chairs in batches of 100 chairs over a period of six months.</span></span> <span data-ttu-id="b69a1-117">Lai izsekotu piegādes prasības, izveidojiet piegādes grafiku.</span><span class="sxs-lookup"><span data-stu-id="b69a1-117">To keep track of the delivery requirements, you create a delivery schedule.</span></span> <span data-ttu-id="b69a1-118">Piegādes grafika lapā izveidojiet sešas atsevišķas piegādes rindas.</span><span class="sxs-lookup"><span data-stu-id="b69a1-118">On the delivery schedule page, you create six separate delivery lines.</span></span> <span data-ttu-id="b69a1-119">Katrā piegādes rindā ir 100 krēsli; tā norāda šo 100 krēslu piegādes datumu.</span><span class="sxs-lookup"><span data-stu-id="b69a1-119">Each delivery line contains 100 chairs and indicates the delivery date for those 100 chairs.</span></span> <span data-ttu-id="b69a1-120">Šajā gadījumā katra rinda ir korespondējoša pirmajā mēneša dienā sešus mēnešus pēc kārtas.</span><span class="sxs-lookup"><span data-stu-id="b69a1-120">In this case, each line is offset on the first of the month for six consecutive months.</span></span>  

<span data-ttu-id="b69a1-121">Izveidojot piegādes grafiku, sākotnējās pasūtījuma rindas tips automātiski mainās uz **Pasūtījuma rinda ar vairākām piegādēm**.</span><span class="sxs-lookup"><span data-stu-id="b69a1-121">When you create a delivery schedule, the type of the original order line is automatically changed to **Order line with multiple deliveries**.</span></span> <span data-ttu-id="b69a1-122">Šī tipa rindu dēvē par tirdzniecības rindu, un tā tiek apzīmēta ar ikonu.</span><span class="sxs-lookup"><span data-stu-id="b69a1-122">A line of this type is referred to as a commercial line and is marked by an icon.</span></span> <span data-ttu-id="b69a1-123">Piegādes rinda tiek atzīmēta ar citu ikonu.</span><span class="sxs-lookup"><span data-stu-id="b69a1-123">The delivery line is marked by a different icon.</span></span> <span data-ttu-id="b69a1-124">Ja piegādes rindā maināt daudzumu, tad tirdzniecības rinda tiek atjaunināta uz piegādes grafika kopējo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="b69a1-124">If you change a quantity on a delivery line, the commercial line is updated to the total quantity of the delivery schedule.</span></span> <span data-ttu-id="b69a1-125">Ja tirdzniecības līgums ir definējis pasūtījuma kopējo atlaidi, tad piegādes grafiks nodrošina, ka jūsu pasūtījumam piešķir kopējo pasūtījuma atlaidi pat tad, ja pasūtījums ir sadalīts atsevišķās piegādēs.</span><span class="sxs-lookup"><span data-stu-id="b69a1-125">If a trade agreement has defined a total discount for the order, the delivery schedule ensures that your order is eligible for the total order discount, even when the order is split into separate deliveries.</span></span>  

<span data-ttu-id="b69a1-126">Pasūtījumi, kuriem ir piegādes grafiks, tiek apstrādāti pret piegādes rindām.</span><span class="sxs-lookup"><span data-stu-id="b69a1-126">Orders that have a delivery schedule are processed against the delivery lines.</span></span> <span data-ttu-id="b69a1-127">Apstrāde ietver pavadzīmju grāmatošanu, produktu ieejas plūsmas un rēķina izrakstīšanu.</span><span class="sxs-lookup"><span data-stu-id="b69a1-127">Processing includes the posting of packing slips, product receipts, and invoicing.</span></span>  

<span data-ttu-id="b69a1-128">Dokumenta izdrukas pasūtījumiem un piedāvājumiem, kam ir piegādes grafiks, uzrāda tikai piegādes rindas.</span><span class="sxs-lookup"><span data-stu-id="b69a1-128">Document printouts of orders and quotations that have a delivery schedule show only the delivery lines.</span></span> <span data-ttu-id="b69a1-129">Tajās nebūs redzamas sākotnējas rindas (tirdzniecības rindas).</span><span class="sxs-lookup"><span data-stu-id="b69a1-129">They don't show the original lines (commercial lines).</span></span> <span data-ttu-id="b69a1-130">**Piezīme.** Turklāt ir redzamas tikai piegādes rindas, kad veicat tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="b69a1-130">**Note:** In addition, only the delivery lines are shown when you perform these actions:</span></span>

-   <span data-ttu-id="b69a1-131">Amats</span><span class="sxs-lookup"><span data-stu-id="b69a1-131">Post</span></span>
-   <span data-ttu-id="b69a1-132">Kopēt lapas</span><span class="sxs-lookup"><span data-stu-id="b69a1-132">Copy pages</span></span>
-   <span data-ttu-id="b69a1-133">Pārlūkot saraksta lapas un pārskatus</span><span class="sxs-lookup"><span data-stu-id="b69a1-133">Browse list pages and reports</span></span>

<span data-ttu-id="b69a1-134">Apstiprinot pārdošanas piedāvājumu, iegūtie pārdošanas pasūtījumi uzradīs visu piegādes grafiku pat tad, ja pasūtījuma rindās ir vairākas piegādes.</span><span class="sxs-lookup"><span data-stu-id="b69a1-134">When you confirm sales quotations, the resulting sales orders show the whole delivery schedule, even the order lines that have multiple deliveries.</span></span> <span data-ttu-id="b69a1-135">Turklāt viss piegādes grafiks būs redzams visās galvenajās lapās, piemēram, pārdošanas pasūtījumos, pārdošanas piedāvājumos un pirkšanas pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="b69a1-135">In addition, the whole delivery schedule is shown on all the major pages, such as sales orders, sales quotations, and purchase orders.</span></span>




