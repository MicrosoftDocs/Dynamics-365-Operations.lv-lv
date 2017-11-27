---
title: "Nepārtrauktības programmas iestatīšana zvanu centram"
description: "Šajā rakstā ir aprakstīts, kā zvanu centrā iestatīt nepārtrauktības programmu."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0fa2c5aaf6953eed75729017cca8cf3c2220e80d
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-a-continuity-program-for-a-call-center"></a><span data-ttu-id="665ca-103">Nepārtrauktības programmas iestatīšana zvanu centram</span><span class="sxs-lookup"><span data-stu-id="665ca-103">Set up a continuity program for a call center</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="665ca-104">Šajā rakstā ir aprakstīts, kā zvanu centrā iestatīt nepārtrauktības programmu.</span><span class="sxs-lookup"><span data-stu-id="665ca-104">This article describes how to set up a continuity program for a call center.</span></span>

<span data-ttu-id="665ca-105">Nepārtrauktības programmā, kas ir pazīstama arī kā periodisku pasūtījumu programma, klienti saņem regulārus preču sūtījumus saskaņā ar iepriekš noteiktu grafiku.</span><span class="sxs-lookup"><span data-stu-id="665ca-105">In a continuity program, which is also known as a recurring order program, customers receive regular product shipments according to a predefined schedule.</span></span> <span data-ttu-id="665ca-106">Katrā sūtījumā var būt atšķirīgas preces, kā tas ir ar klubu, kas katru mēnesi saņem jaunu grāmatu, vai arī vienu preci var sūtīt atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="665ca-106">Each shipment can contain a different product, as in the case of a book-of-the-month club, or the same product can be sent repeatedly.</span></span> <span data-ttu-id="665ca-107">Lai iestatītu nepārtrauktības programmu, ir jāizpilda tālāk minētie uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="665ca-107">To set up a continuity program, you must complete the following tasks.</span></span>

1.  <span data-ttu-id="665ca-108">Iestatiet nepārtrauktības parametrus lapā **Zvanu centra parametri**.</span><span class="sxs-lookup"><span data-stu-id="665ca-108">Set the continuity parameters on the **Call center parameters** page.</span></span>
2.  <span data-ttu-id="665ca-109">Izveidojiet nepārtrauktības programmu, kas norāda detalizētu informāciju, piemēram, maksājumu grafiku, sūtījumu laiku un vai maksājums tiek veikts uzreiz.</span><span class="sxs-lookup"><span data-stu-id="665ca-109">Create a continuity program that specifies details such as the payment schedule, the timing of the shipments, and whether billing is up front.</span></span> <span data-ttu-id="665ca-110">Jums jāpievieno arī to preču saraksts, kas ir iekļautas nepārtrauktības programmā.</span><span class="sxs-lookup"><span data-stu-id="665ca-110">You must also add a list of products that are included in the continuity program.</span></span> <span data-ttu-id="665ca-111">Katra prece saņem notikuma ID numuru, kas tiek piešķirts secīgi, sākot ar 1.</span><span class="sxs-lookup"><span data-stu-id="665ca-111">Each product receives an event ID number that is assigned sequentially, beginning with 1.</span></span> <span data-ttu-id="665ca-112">Notikuma ID nosaka secību, kādā preces tiek nosūtītas.</span><span class="sxs-lookup"><span data-stu-id="665ca-112">The event IDs determine the order that products are sent in.</span></span>
    -   <span data-ttu-id="665ca-113">Ja katrā sūtījumā debitori saņem atšķirīgu preci, tās tiek nosūtītas secīgi saskaņā ar to notikuma ID, sākot no pašreizējā notikuma.</span><span class="sxs-lookup"><span data-stu-id="665ca-113">If customers receive a different product in each shipment, the products are sent in sequential order, based on their event IDs and beginning with the current event.</span></span>
    -   <span data-ttu-id="665ca-114">Ja debitori katrā sūtījumā saņem vienu un to pašu preci, sarakstā ir tikai viena prece, kam ir viens notikuma ID.</span><span class="sxs-lookup"><span data-stu-id="665ca-114">If customers receive the same product in each shipment, the list contains only one product that has one event ID.</span></span> <span data-ttu-id="665ca-115">Viens un tas pats notikums notiek atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="665ca-115">The same event occurs repeatedly.</span></span> <span data-ttu-id="665ca-116">Varat norādīt, cik reizes atkārtot katru notikumu.</span><span class="sxs-lookup"><span data-stu-id="665ca-116">You can specify how many times each event is repeated.</span></span>

3.  <span data-ttu-id="665ca-117">Izveidojiet pamata preci, kas apzīmē nepārtrauktības programmu, kuru izveidojāt 2. uzdevuma izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="665ca-117">Create a parent product that represents the continuity program that you created in task 2.</span></span> <span data-ttu-id="665ca-118">Ja šo preci pievienojat pārdošanas pasūtījumam, tiek atvērta lapa **Nepārtrauktība**.</span><span class="sxs-lookup"><span data-stu-id="665ca-118">If you add this product to a sales order, the **Continuity** page opens.</span></span> <span data-ttu-id="665ca-119">Pēc tam šo lapu varat izmantot, lai izveidotu faktisko nepārtrauktības pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="665ca-119">You can then use that page to create the actual continuity order.</span></span> <span data-ttu-id="665ca-120">Pamata prece nenorāda atsevišķas preces, ko debitors saņem katrā sūtījumā.</span><span class="sxs-lookup"><span data-stu-id="665ca-120">The parent product doesn't specify the individual products that the customer receives in each shipment.</span></span>

<span data-ttu-id="665ca-121">Kad esat iestatījis nepārtrauktības programmu, kā aprakstīts iepriekš, varat debitoram izveidot nepārtrauktības pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="665ca-121">After you've set up a continuity program as described above, you can create a continuity order for a customer.</span></span> <span data-ttu-id="665ca-122">Iespējams, būs jāizpilda arī tālāk minētie papildu uzturēšanas uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="665ca-122">You might also have to perform the following additional maintenance tasks.</span></span>

-   <span data-ttu-id="665ca-123">**Pašreizējā notikuma perioda nepārtrauktības atjaunināšana** — iestatiet pakešuzdevumu, kas sistēmai paziņo, kāds ir pašreizējais notikuma periods.</span><span class="sxs-lookup"><span data-stu-id="665ca-123">**Update the current continuity event period** – Set up a batch job that tells the system what the current event period is.</span></span>
-   <span data-ttu-id="665ca-124">**Izveidot nepārtrauktos apakšpasūtījumus** — izveidojiet apakšpasūtījumus no pamata nepārtrauktības pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="665ca-124">**Create continuity child orders** – Create child orders from the parent continuity order.</span></span>
-   <span data-ttu-id="665ca-125">**Nepārtrauktības maksājumu apstrāde** — apstrādājiet to maksājumu norēķinus un paziņojumus, kas ir saistīti ar nepārtrauktības pārdošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="665ca-125">**Process continuity payments** – Process billing and notifications for payments that are associated with continuity sales orders.</span></span>
-   <span data-ttu-id="665ca-126">**Nepārtrauktības rindu paplašināšana** (ja nepieciešams) — palieliniet reižu skaitu, cik nepārtrauktības notikumu var atkārtot.</span><span class="sxs-lookup"><span data-stu-id="665ca-126">**Extend continuity lines** (if required) – Extend the number of times that a continuity event can be repeated.</span></span> <span data-ttu-id="665ca-127">Sūtījumu atkārtošana var pārsniegt ierobežojumus, kas ir iestatīti zvanu centra parametru laukā **Nepārtrauktības atkārtošanas robežvērtība**.</span><span class="sxs-lookup"><span data-stu-id="665ca-127">The repetition of shipments can then extend beyond the limit that was set in the **Continuity repeat threshold** field in the call center parameters.</span></span>
-   <span data-ttu-id="665ca-128">**Nepārtrauktības atjauninājuma veikšana** (ja nepieciešams) — sinhronizējiet izmaiņas starp nepārtrauktības programmu un nepārtrauktība pamata pārdošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="665ca-128">**Perform a continuity update** (if required) – Synchronize changes between the continuity program and the continuity parent sales orders.</span></span>
-   <span data-ttu-id="665ca-129">**Galveno nepārtrauktības rindu un pasūtījumu aizvēršana** — aizveriet nepārtrauktības pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="665ca-129">**Close continuity parent lines and orders** – Close continuity orders.</span></span>





