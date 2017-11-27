---
title: Aizkaves
description: "Šajā rakstā ir sniegta informācija par aizkavēšanās datumiem vispārējā plānošanā. Aizkavēšanās datums ir reālistisks izpildes datums, kuru transakcija saņem, ja vispārējās plānošanas aprēķinātais drīzākais izpildes datums ir vēlāks par pieprasīto datumu."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ed0df1abbf4f70ea70046eff7b91a25fdd59016c
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="delays"></a><span data-ttu-id="93bc4-104">Aizkaves</span><span class="sxs-lookup"><span data-stu-id="93bc4-104">Delays</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="93bc4-105">Šajā rakstā ir sniegta informācija par aizkavēšanās datumiem vispārējā plānošanā.</span><span class="sxs-lookup"><span data-stu-id="93bc4-105">This article provides information about delayed dates in master planning.</span></span> <span data-ttu-id="93bc4-106">Aizkavēšanās datums ir reālistisks izpildes datums, kuru transakcija saņem, ja vispārējās plānošanas aprēķinātais drīzākais izpildes datums ir vēlāks par pieprasīto datumu.</span><span class="sxs-lookup"><span data-stu-id="93bc4-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="93bc4-107">Veicot vispārējo plānošanu, var aprēķināt agrāko transakcijas izpildes datumu, pamatojoties uz izpildes laikiem, materiālu pieejamību, noslodzes pieejamību un dažādiem plānošanas parametriem.</span><span class="sxs-lookup"><span data-stu-id="93bc4-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="93bc4-108">Ja vispārējā plānošana aprēķina pasūtījuma datumu, kas ir pirms pašreizējā datuma, pasūtījumu nevar izpildīt savlaicīgi.</span><span class="sxs-lookup"><span data-stu-id="93bc4-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="93bc4-109">Tāpēc pasūtījuma izpilde aizkavējas.</span><span class="sxs-lookup"><span data-stu-id="93bc4-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="93bc4-110">Šajā gadījumā vispārējās plānošanas tiek veikta uz priekšu — pasūtījums tiek ieplānots ar pašreizējo datumu, un tiek iekļauti izpildes laiki.</span><span class="sxs-lookup"><span data-stu-id="93bc4-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="93bc4-111">Šie izpildes laikus sākas ar jebkuru zemāka līmeņa komponentu.</span><span class="sxs-lookup"><span data-stu-id="93bc4-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="93bc4-112">Pēc tam pasūtījums saņem aizkaves datumu.</span><span class="sxs-lookup"><span data-stu-id="93bc4-112">The order then receives a delayed date.</span></span> <span data-ttu-id="93bc4-113">Aizkaves datums ir faktiskais apmaksas datums, kas pamatots uz pašreizējiem datiem.</span><span class="sxs-lookup"><span data-stu-id="93bc4-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="93bc4-114">Vispārējā plānošana aprēķina arī aizkaves dienu skaitu.</span><span class="sxs-lookup"><span data-stu-id="93bc4-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="93bc4-115">Dažās situācijās varat izvēlēties neaprēķināt aizkaves, piemēram, ja lietotāji zina, ka viņi var paātrināt izpildes laikus, atlasot alternatīvu piegādes veidu.</span><span class="sxs-lookup"><span data-stu-id="93bc4-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="93bc4-116">Var konfigurēt, kā aizkavēšanās tiek aprēķinātas seguma grupai.</span><span class="sxs-lookup"><span data-stu-id="93bc4-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="93bc4-117">Seguma grupu krājumam var pievienot vēlāk.</span><span class="sxs-lookup"><span data-stu-id="93bc4-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="93bc4-118">Lapā **Vispārējās plānošanas parametri** var iestatīt sākuma laiku aprēķina kavējumiem.</span><span class="sxs-lookup"><span data-stu-id="93bc4-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="93bc4-119">Ja pasūtījums tiek izpildīts pēc šī laika, vienas dienas aizkave tiek pievienota pasūtījuma aiskaves datumam.</span><span class="sxs-lookup"><span data-stu-id="93bc4-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

<span data-ttu-id="93bc4-120">**Piezīme.** Iepriekšējās versijās aprēķinātās aizkaves tika sauktas par *aizkavēšanās paziņojumiem*, aizkaves datums tika saukts par *aizkavēšanās datumu* un aizkavētā transakcija tika saukta par *transakciju, kas tika aizkavēta*.</span><span class="sxs-lookup"><span data-stu-id="93bc4-120">**Note:** In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

<a name="see-also"></a><span data-ttu-id="93bc4-121">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="93bc4-121">See also</span></span>
--------

[<span data-ttu-id="93bc4-122">Vajadzības iestatījumi</span><span class="sxs-lookup"><span data-stu-id="93bc4-122">Coverage settings</span></span>](coverage-settings.md)




