---
title: Aizkaves
description: Šajā tēmā ir sniegta informācija par aizkavēšanās datumiem vispārējā plānošanā. Aizkavēšanās datums ir reālistisks izpildes datums, kuru transakcija saņem, ja vispārējās plānošanas aprēķinātais drīzākais izpildes datums ir vēlāks par pieprasīto datumu.
author: roxanadiaconu
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da09d670fd952d885f013693b6362cf9002343ff
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982700"
---
# <a name="delays"></a><span data-ttu-id="35eba-104">Aizkaves</span><span class="sxs-lookup"><span data-stu-id="35eba-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35eba-105">Šajā tēmā ir sniegta informācija par aizkavēšanās datumiem vispārējā plānošanā.</span><span class="sxs-lookup"><span data-stu-id="35eba-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="35eba-106">Aizkavēšanās datums ir reālistisks izpildes datums, kuru transakcija saņem, ja vispārējās plānošanas aprēķinātais drīzākais izpildes datums ir vēlāks par pieprasīto datumu.</span><span class="sxs-lookup"><span data-stu-id="35eba-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="35eba-107">Veicot vispārējo plānošanu, var aprēķināt agrāko transakcijas izpildes datumu, pamatojoties uz izpildes laikiem, materiālu pieejamību, noslodzes pieejamību un dažādiem plānošanas parametriem.</span><span class="sxs-lookup"><span data-stu-id="35eba-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="35eba-108">Ja vispārējā plānošana aprēķina pasūtījuma datumu, kas ir pirms pašreizējā datuma, pasūtījumu nevar izpildīt savlaicīgi.</span><span class="sxs-lookup"><span data-stu-id="35eba-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="35eba-109">Tāpēc pasūtījuma izpilde aizkavējas.</span><span class="sxs-lookup"><span data-stu-id="35eba-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="35eba-110">Šajā gadījumā vispārējās plānošanas tiek veikta uz priekšu — pasūtījums tiek ieplānots ar pašreizējo datumu, un tiek iekļauti izpildes laiki.</span><span class="sxs-lookup"><span data-stu-id="35eba-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="35eba-111">Šie izpildes laikus sākas ar jebkuru zemāka līmeņa komponentu.</span><span class="sxs-lookup"><span data-stu-id="35eba-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="35eba-112">Pēc tam pasūtījums saņem aizkaves datumu.</span><span class="sxs-lookup"><span data-stu-id="35eba-112">The order then receives a delayed date.</span></span> <span data-ttu-id="35eba-113">Aizkaves datums ir faktiskais apmaksas datums, kas pamatots uz pašreizējiem datiem.</span><span class="sxs-lookup"><span data-stu-id="35eba-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="35eba-114">Vispārējā plānošana aprēķina arī aizkaves dienu skaitu.</span><span class="sxs-lookup"><span data-stu-id="35eba-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="35eba-115">Dažās situācijās varat izvēlēties neaprēķināt aizkaves, piemēram, ja lietotāji zina, ka viņi var paātrināt izpildes laikus, atlasot alternatīvu piegādes veidu.</span><span class="sxs-lookup"><span data-stu-id="35eba-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="35eba-116">Var konfigurēt, kā aizkavēšanās tiek aprēķinātas seguma grupai.</span><span class="sxs-lookup"><span data-stu-id="35eba-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="35eba-117">Seguma grupu krājumam var pievienot vēlāk.</span><span class="sxs-lookup"><span data-stu-id="35eba-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="35eba-118">Lapā **Vispārējās plānošanas parametri** var iestatīt sākuma laiku aprēķina kavējumiem.</span><span class="sxs-lookup"><span data-stu-id="35eba-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="35eba-119">Ja pasūtījums tiek izpildīts pēc šī laika, vienas dienas aizkave tiek pievienota pasūtījuma aiskaves datumam.</span><span class="sxs-lookup"><span data-stu-id="35eba-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> [!NOTE]
> <span data-ttu-id="35eba-120">Iepriekšējās versijās aprēķinātās aizkaves tika sauktas par *aizkavēšanās paziņojumiem*, aizkaves datums tika saukts par *aizkavēšanās datumu* un aizkavētā transakcija tika saukta par *transakciju, kas tika aizkavēta*.</span><span class="sxs-lookup"><span data-stu-id="35eba-120">In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a><span data-ttu-id="35eba-121">Ierobežota ražošanas iestatījuma aizkave ar vairākiem MK līmeņiem</span><span class="sxs-lookup"><span data-stu-id="35eba-121">Limited delays in production setup with multiple BOM levels</span></span>
<span data-ttu-id="35eba-122">Strādājot ar kavēšanos ražošanas iestatījumā, kam ir vairāki MK līmeņi, ir svarīgi atzīmēt, ka tikai tie krājumi, kas atrodas tieši virs krājuma (MK struktūrā), kas izraisa kavēšanos, tiks atjaunināti ar kavēšanos kā daļa no vispārējās plānošanas izpildes.</span><span class="sxs-lookup"><span data-stu-id="35eba-122">When you work with delays in a production setup that has multiple BOM levels, it is important to note that only the items directly above the item (in the BOM structure) causing the delay, will be updated with a delay as part of the master planning run.</span></span> <span data-ttu-id="35eba-123">Citi krājumi MK struktūrā netiks lietoti līdz pirmajai vispārējai plānošanai, kad plānotais pasūtījums augstākajam līmenim ir apstiprināts.</span><span class="sxs-lookup"><span data-stu-id="35eba-123">Other items in the BOM structure will not get the delay applied until the first master planning run, when the planned order for the top level is approved or firmed.</span></span> 

<span data-ttu-id="35eba-124">Lai apietu šo zināmo ierobežojumu, ražošanas pasūtījumus MK struktūras virspusē ar kavējumiem var apstiprināt pirms nākamās vispārējās plānošanas izpildes.</span><span class="sxs-lookup"><span data-stu-id="35eba-124">To work around this known limitation, the production orders on the top of the BOM structure with delays can be approved (or firmed) prior to the next master planning run.</span></span> <span data-ttu-id="35eba-125">Šādā veidā aizkave no aizkavētā, apstiprinātā, plānotā ražošanas pasūtījuma tiks paturēta, un visi pakārtotie komponenti tiks attiecīgi atjaunināti.</span><span class="sxs-lookup"><span data-stu-id="35eba-125">This way the delay from the delayed approved planned production order will be kept and all underlying components will be updated accordingly.</span></span>
<span data-ttu-id="35eba-126">Darbības ziņojumus var arī izmantot, lai noteiktu plānotos pasūtījumus, ko var pārlikt uz vēlāku datumu citu kavējumu MK struktūrā dēļ.</span><span class="sxs-lookup"><span data-stu-id="35eba-126">Action messages can also be used to identify planned orders that can be moved to a later date, due to other delays in the BOM structure.</span></span>

## <a name="desired-date"></a><span data-ttu-id="35eba-127">Vēlamais datums</span><span class="sxs-lookup"><span data-stu-id="35eba-127">Desired date</span></span>

<span data-ttu-id="35eba-128">Lapas **Plānotais pasūtījums** cilnē **Aizkaves** ir pieejams plānotā pasūtījuma **Vēlamais datums**.</span><span class="sxs-lookup"><span data-stu-id="35eba-128">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="35eba-129">Plānotā pasūtījuma vēlamais datums ir aizkavju bāzes datums, un tas ir aprēķināts datums, kas ir vienāds ar vērtību **Pieprasītais datums**, kura aprēķināta, balstoties uz parametriem **Neto prasības**.</span><span class="sxs-lookup"><span data-stu-id="35eba-129">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement**.</span></span> <span data-ttu-id="35eba-130">Ja plānotais pasūtījums ir MK rinda, ražošanas rinda vai Kanban rinda, vēlamais datums balstās uz vērtību **Vajadzības datums**, un vēlamais datums netiks rādīts lapā **Plānotais pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="35eba-130">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

<a name="additional-resources"></a><span data-ttu-id="35eba-131">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="35eba-131">Additional resources</span></span>
--------

[<span data-ttu-id="35eba-132">Seguma iestatījumi</span><span class="sxs-lookup"><span data-stu-id="35eba-132">Coverage settings</span></span>](coverage-settings.md)
