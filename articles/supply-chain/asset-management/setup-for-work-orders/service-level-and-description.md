---
title: Pakalpojuma līmenis un apraksts
description: Šajā tēmā ir paskaidrots pakalpojuma līmenis un tā apraksts Līdzekļu pārvaldībā.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7dd577c930c6cc17da6baee30d3558656de01a09
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569827"
---
# <a name="service-level-and-description"></a><span data-ttu-id="d5d84-103">Pakalpojuma līmenis un apraksts</span><span class="sxs-lookup"><span data-stu-id="d5d84-103">Service level and description</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d5d84-104">Kad izveidojat darba pasūtījumu, iespējams, vēlaties tam definēt pakalpojumu līmeņus un pievienot vispārīgu aprakstu.</span><span class="sxs-lookup"><span data-stu-id="d5d84-104">When you create a work order, you might want to define the service levels for it and add a general description to it.</span></span> <span data-ttu-id="d5d84-105">Varat izveidot darba pasūtījuma pakalpojumu līmeņus lapā **Darba pasūtījuma pakalpojumu līmeņi** un aprakstus lapā **Darba pasūtījuma apraksts**.</span><span class="sxs-lookup"><span data-stu-id="d5d84-105">You can create work order service levels on the **Work order service levels** page and descriptions on the **Work order description** page.</span></span>

## <a name="create-a-service-level"></a><span data-ttu-id="d5d84-106">Pakalpojuma līmeņa izveide</span><span class="sxs-lookup"><span data-stu-id="d5d84-106">Create a service level</span></span>

1. <span data-ttu-id="d5d84-107">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Darba pasūtījumi** \> **Pakalpojuma līmenis**.</span><span class="sxs-lookup"><span data-stu-id="d5d84-107">Select **Asset management** \> **Setup** \> **Work orders** \> **Service level**.</span></span>
2. <span data-ttu-id="d5d84-108">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="d5d84-108">Select **New**.</span></span>
3. <span data-ttu-id="d5d84-109">Laukā **Pakalpojuma līmenis** ievadiet pakalpojuma līmeni (piemēram, numuru).</span><span class="sxs-lookup"><span data-stu-id="d5d84-109">In the **Service level** field, enter the service level (for example, a number).</span></span>
4. <span data-ttu-id="d5d84-110">Laukā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="d5d84-110">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="d5d84-111">Kopsavilkuma cilnē **Darba pasūtījumi** varat definēt paredzamo sākuma un beigu datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="d5d84-111">On the **Work orders** FastTab, you can define expected start and end dates and times.</span></span> <span data-ttu-id="d5d84-112">Šīs kopsavilkuma cilnes lauki definē periodu, kad darba pasūtījumi ir jāsāk un kad tiem ir jābeidzas.</span><span class="sxs-lookup"><span data-stu-id="d5d84-112">The fields on this FastTab define the period that work orders should be started and ended during.</span></span> <span data-ttu-id="d5d84-113">Tie tiek izmantoti manuāli izveidotiem darba pasūtījumiem un darba pasūtījumiem, kas tiek izveidoti, pamatojoties uz uzturēšanas pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="d5d84-113">They are used for work orders that are manually created and work orders that are created based on maintenance requests.</span></span> 

5. <span data-ttu-id="d5d84-114">Laukā **Sākuma diena** ievadiet dienu skaitu, lai definētu periodu, kurā jāsākas darba pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="d5d84-114">In the **Start day** field, enter a number of days to define the period that the work order should start during.</span></span> <span data-ttu-id="d5d84-115">Dienu skaits tiek aprēķināts no darba pasūtījuma izveides datuma.</span><span class="sxs-lookup"><span data-stu-id="d5d84-115">The number of days is calculated from the creation date of the work order.</span></span> <span data-ttu-id="d5d84-116">Piemēram, ja darba pasūtījums jāsāk uzreiz pēc tā izveides, ievadiet **0**.</span><span class="sxs-lookup"><span data-stu-id="d5d84-116">For example, if the work order should start when it's created, enter **0**.</span></span> <span data-ttu-id="d5d84-117">Ja darba pasūtījums jāsāk vienas nedēļas laikā pēc tā izveides, ievadiet **7**.</span><span class="sxs-lookup"><span data-stu-id="d5d84-117">If the work order should start within one week after it's created, enter **7**.</span></span>
6. <span data-ttu-id="d5d84-118">Lai darba pasūtījumam iestatītu sākuma laiku, papildus sākuma datumam iestatiet opciju **Iestatīt sākuma laiku** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="d5d84-118">To set a start time for the work order, in addition to a start date, set the **Set start time** option to **Yes**.</span></span> <span data-ttu-id="d5d84-119">Pēc tam laukā **Sākuma laiks** ievadiet sākuma laiku.</span><span class="sxs-lookup"><span data-stu-id="d5d84-119">Then enter the start time in the **Start time** field.</span></span> <span data-ttu-id="d5d84-120">Ja opcija ir iestatīta uz **Nē**, tiek izmantots pašreizējās dienas laiks.</span><span class="sxs-lookup"><span data-stu-id="d5d84-120">If you set the option to **No**, the current time of day is used.</span></span>
7. <span data-ttu-id="d5d84-121">Laukā **Beigu diena** ievadiet dienu skaitu, lai definētu periodu, kurā jāpabeidz darba pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="d5d84-121">In the **End day** field, enter a number of days to define the period that the work order should end during.</span></span> <span data-ttu-id="d5d84-122">Dienu skaits tiek aprēķināts no darba pasūtījuma sākšanas datuma.</span><span class="sxs-lookup"><span data-stu-id="d5d84-122">The number of days is calculated from the start date of the work order.</span></span> <span data-ttu-id="d5d84-123">Piemēram, ja darba pasūtījums ir jāpabeidz vienas nedēļas laikā kopš tā sākuma datuma, ievadiet **7**.</span><span class="sxs-lookup"><span data-stu-id="d5d84-123">For example, if the work order should end within one week of its start date, enter **7**.</span></span>
8. <span data-ttu-id="d5d84-124">Lai darba pasūtījumam iestatītu beigu, laiku papildus beigu datumam iestatiet opciju **Iestatīt beigu laiku** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="d5d84-124">To set an end time for the work order, in addition to an end date, set the **Set end time** option to **Yes**.</span></span> <span data-ttu-id="d5d84-125">Pēc tam laukā **Beigu laiks** ievadiet beigu laiku.</span><span class="sxs-lookup"><span data-stu-id="d5d84-125">Then enter the end time in the **End time** field.</span></span> <span data-ttu-id="d5d84-126">Ja opcija ir iestatīta uz **Nē**, tiek izmantots pašreizējās dienas laiks.</span><span class="sxs-lookup"><span data-stu-id="d5d84-126">If you set the option to **No**, the current time of day is used.</span></span>
9. <span data-ttu-id="d5d84-127">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d5d84-127">Select **Save**.</span></span>

![Darba pasūtījumu pakalpojuma līmeņa lapa](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a><span data-ttu-id="d5d84-129">Izveidot aprakstu</span><span class="sxs-lookup"><span data-stu-id="d5d84-129">Create a description</span></span>

1. <span data-ttu-id="d5d84-130">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Darba pasūtījumi** \> **Apraksti**.</span><span class="sxs-lookup"><span data-stu-id="d5d84-130">Select **Asset management** \> **Setup** \> **Work orders** \> **Descriptions**.</span></span>
2. <span data-ttu-id="d5d84-131">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="d5d84-131">Select **New**.</span></span>
3. <span data-ttu-id="d5d84-132">Laukā **Apraksts** ievadiet aprakstu.</span><span class="sxs-lookup"><span data-stu-id="d5d84-132">In the **Description** field, enter the description.</span></span>
4. <span data-ttu-id="d5d84-133">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d5d84-133">Select **Save**.</span></span>
