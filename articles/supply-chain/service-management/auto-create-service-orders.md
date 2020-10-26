---
title: Automātiski izveidot pakalpojuma pasūtījumus
description: Varat izveidot pakalpojuma pasūtījumus, kas balstīti uz pakalpojumu līgumu, tā darbības periodā.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08fb7363ab87fd6a7f3d38406e72b1f542dc2c2a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978753"
---
# <a name="automatically-create-service-orders"></a><span data-ttu-id="243ff-103">Automātiski izveidot pakalpojuma pasūtījumus</span><span class="sxs-lookup"><span data-stu-id="243ff-103">Automatically create service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="243ff-104">Varat izveidot pakalpojuma pasūtījumus, kas balstīti uz pakalpojumu līgumu, tā darbības periodā.</span><span class="sxs-lookup"><span data-stu-id="243ff-104">You can generate service orders that are based on a service agreement for the valid period of the service agreement.</span></span>

<span data-ttu-id="243ff-105">Pakalpojumu līgumam ir piesaistīti visi pakalpojuma pasūtījumi, ko izveidojāt no šī pakalpojumu līguma.</span><span class="sxs-lookup"><span data-stu-id="243ff-105">The service orders that you generate from a service agreement are all attached to the service agreement.</span></span>

<span data-ttu-id="243ff-106">Pakalpojuma pasūtījumi tiek izveidoti automātiski no šādiem iestatījumiem:</span><span class="sxs-lookup"><span data-stu-id="243ff-106">Service orders are generated automatically from the following settings:</span></span>

  - <span data-ttu-id="243ff-107">Pakalpojumu līguma rindās iestatītais pakalpojumu līguma intervāls.</span><span class="sxs-lookup"><span data-stu-id="243ff-107">The service agreement interval that is set up in the service agreement lines.</span></span> <span data-ttu-id="243ff-108">Pakalpojumu līguma intervāls norāda biežumu, kādā tiek izveidotas pakalpojuma pasūtījuma rindas.</span><span class="sxs-lookup"><span data-stu-id="243ff-108">The service agreement interval indicates the frequency that service-order lines are created.</span></span> <span data-ttu-id="243ff-109">Vairāk informācijas skatiet [Pakalpojumu intervāli](service-intervals.md).</span><span class="sxs-lookup"><span data-stu-id="243ff-109">For more information, see [Service intervals](service-intervals.md).</span></span>

  - <span data-ttu-id="243ff-110">Periods, ko norādāt, lai noteiktu pakalpojuma periodu laukos **Datums no** un **Datums līdz** veidlapā **Izveidot pakalpojuma pasūtījumus**.</span><span class="sxs-lookup"><span data-stu-id="243ff-110">The period that you specify to define the service period in the **From date** and **To date** fields in the **Create service orders** form.</span></span> <span data-ttu-id="243ff-111">Vairāk informācijas skatiet [Automātiska pakalpojuma pasūtījuma izveide](create-service-orders-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="243ff-111">For more information, see [Create service orders automatically](create-service-orders-automatically.md).</span></span>

  - <span data-ttu-id="243ff-112">**Pakalpojuma pasūtījumu kombinēšana** opcija pakalpojumu līguma galvenē.</span><span class="sxs-lookup"><span data-stu-id="243ff-112">The **Combine service orders** option on the service agreement header.</span></span> <span data-ttu-id="243ff-113">Opcija norāda, vai no pakalpojumu līguma izveidotās pakalpojuma pasūtījuma rindas kombinē pakalpojuma pasūtījumus pēc darbinieka, pakalpojumu uzdevuma, pakalpojumu objekta vai pakalpojumu līguma.</span><span class="sxs-lookup"><span data-stu-id="243ff-113">This option defines whether service order lines generated from a service agreement, combines service orders according to employee, service task, service object, or service agreement.</span></span> <span data-ttu-id="243ff-114">Vairāk informācijas skatiet tēmā [Pakalpojuma pasūtījumu kombinēšana](combine-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="243ff-114">For more information, see [Combine service orders](combine-service-orders.md).</span></span>

  - <span data-ttu-id="243ff-115">Pakalpojumu līguma rindas opcija **Laika logs**.</span><span class="sxs-lookup"><span data-stu-id="243ff-115">The **Time window** option on the service agreement line.</span></span> <span data-ttu-id="243ff-116">Laika logs nosaka, cik tālu pakalpojuma pasūtījuma rinda var pārvietoties attiecībā pret tās aprēķina datumu.</span><span class="sxs-lookup"><span data-stu-id="243ff-116">The time window defines how far a service order line can move with regard to its calculated date.</span></span> <span data-ttu-id="243ff-117">Vairāk informācijas skatiet tēmā [Laika logi](time-windows.md).</span><span class="sxs-lookup"><span data-stu-id="243ff-117">For more information, see [Time windows](time-windows.md).</span></span>


> [!NOTE]
> <P><span data-ttu-id="243ff-118">Ja pakalpojuma pasūtījumā minētā diena nav atvērta kalendārā, ko atlasījāt veidlapā <STRONG>Pakalpojuma pārvaldības parametri</STRONG>, saņemat paziņojumu, ka radies kalendāra konflikts.</span><span class="sxs-lookup"><span data-stu-id="243ff-118">If the day that is specified for a service order is not open in the calendar that you have selected in the <STRONG>Service management parameters</STRONG> form, a message will indicate that there is a calendar conflict.</span></span> <span data-ttu-id="243ff-119">Varat droši ignorēt šo paziņojumu, un pakalpojuma pasūtījums tiek izveidots, lai arī šī diena kalendārā ir slēgta.</span><span class="sxs-lookup"><span data-stu-id="243ff-119">You can safely ignore the message; the service order will be created, even though the day is closed on the calendar.</span></span></P>

## <a name="example-1"></a><span data-ttu-id="243ff-120">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="243ff-120">Example 1</span></span>

<span data-ttu-id="243ff-121">Pakalpojumu līgums ilgst no 2012. gada 1. janvāra līdz 2012. gada 31. decembrim.</span><span class="sxs-lookup"><span data-stu-id="243ff-121">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="243ff-122">Ja pakalpojuma periods, ko norādāt veidlapā **Pakalpojuma pasūtījumu izveide** ir no 2012. gada 1. novembra līdz 2013. gada 1. februārim, pakalpojuma pasūtījumi tiek veidoti no 2012. gada 1. novembra līdz 2012. gada 31. decembrim.</span><span class="sxs-lookup"><span data-stu-id="243ff-122">If the service period that you specify in the **Create service orders** form is from November 1, 2012 until February 1, 2013, service orders are created from November 1, 2012 until December 31, 2012.</span></span>

## <a name="example-2"></a><span data-ttu-id="243ff-123">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="243ff-123">Example 2</span></span>

<span data-ttu-id="243ff-124">Pakalpojumu līgums ilgst no 2012. gada 1. janvāra līdz 2012. gada 31. decembrim.</span><span class="sxs-lookup"><span data-stu-id="243ff-124">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="243ff-125">Pakalpojumu līgumam tiek pievienotas divas pakalpojumu līguma rindas.</span><span class="sxs-lookup"><span data-stu-id="243ff-125">Two service agreement lines are attached to the service agreement.</span></span> <span data-ttu-id="243ff-126">Pirmās pakalpojumu līguma rindas sākuma datums ir 2012. gada 2. janvārī un beigu datums ir 2012. gada 1. marts.</span><span class="sxs-lookup"><span data-stu-id="243ff-126">The first service agreement line has a starting date on January 2, 2012 and an ending date on March 1, 2012.</span></span> <span data-ttu-id="243ff-127">Otrās pakalpojumu līguma rindas sākuma datums ir 2012. gada 1. aprīlī un beigu datums ir 2012. gada 31. decembris.</span><span class="sxs-lookup"><span data-stu-id="243ff-127">The second service agreement line has a starting date on April 1, 2012 and an ending date on December 31, 2012.</span></span> <span data-ttu-id="243ff-128">Jūs norādāt periodu veidlapā **Pakalpojuma pasūtījumu izveide** no 2012. gada 1. oktobra līdz 2012. gada 31. decembrim.</span><span class="sxs-lookup"><span data-stu-id="243ff-128">You specify a period in the **Create service orders** form that is from October 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="243ff-129">Tāpēc pakalpojuma pasūtījumi tiek ģenerēti tikai otrai līguma rindai, jo pirmās līguma rindas sākuma un beigu datums ir pirms pakalpojuma pasūtījumam jūsu norādītā perioda.</span><span class="sxs-lookup"><span data-stu-id="243ff-129">Therefore, service orders are generated only for the second agreement line, because the starting date and ending date of the first agreement line are before the period that you specified for the service order.</span></span>

  


