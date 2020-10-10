---
title: Kalendāra izveide un darba laiku ģenerēšana
description: Kalendāros ir norādīta operāciju resursu noslodze un darba laiki. Šajā rakstā ir paskaidrots, kā izveidot darba kalendāru, pamatojoties uz darba laika veidni.
author: andreabichsel
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate, HcmPersonnelManagementWorkspace, WrkCtrGroupDateCalendar, WrkCtrDateCalendar
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f5c630297a8962d1bb383110881b2acdc872b9cd
ms.sourcegitcommit: 175f9394021322c685c5b37317c2f649c81a731a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826101"
---
# <a name="create-calendars-and-generate-working-times"></a><span data-ttu-id="12c8a-104">Kalendāra izveide un darba laiku ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="12c8a-104">Create calendars and generate working times</span></span>



<span data-ttu-id="12c8a-105">Kalendāros ir norādīta operāciju resursu noslodze un darba laiki.</span><span class="sxs-lookup"><span data-stu-id="12c8a-105">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="12c8a-106">Šajā rakstā ir paskaidrots, kā izveidot darba kalendāru, pamatojoties uz darba laika veidni.</span><span class="sxs-lookup"><span data-stu-id="12c8a-106">This article explains how to define a work calendar based on a working time template.</span></span> <span data-ttu-id="12c8a-107">Šo procedūru var izmēģināt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="12c8a-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="12c8a-108">Sākumlapā atlasiet **Resursu dzīves cikla pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="12c8a-108">On the home page, select **Resource lifecycle management**.</span></span>
2. <span data-ttu-id="12c8a-109">Atlasiet **Kalendāri**.</span><span class="sxs-lookup"><span data-stu-id="12c8a-109">Select **Calendars**.</span></span>
3. <span data-ttu-id="12c8a-110">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="12c8a-110">Select **New**.</span></span>
4. <span data-ttu-id="12c8a-111">Laukā **Kalendārs** klasificējiet kalendāru.</span><span class="sxs-lookup"><span data-stu-id="12c8a-111">In the **Calendar** field, classify your calendar.</span></span> <span data-ttu-id="12c8a-112">Tas ir kalendāra ID, kas tiek izmantots kā atsauce, piešķirot kalendārus, piemēram, operācijas resursiem vai resursu grupai.</span><span class="sxs-lookup"><span data-stu-id="12c8a-112">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="12c8a-113">Laukā **Nosaukums** ievadiet savu kalendāru.</span><span class="sxs-lookup"><span data-stu-id="12c8a-113">In the **Name** field, name your calendar.</span></span>
6. <span data-ttu-id="12c8a-114">Ievadiet skaitli laukā **Standarta darba dienas ilgums stundās**.</span><span class="sxs-lookup"><span data-stu-id="12c8a-114">In the **Standard work day in hours** field, enter a number.</span></span>
7. <span data-ttu-id="12c8a-115">Pārliecinieties, ka ir atlasīta rinda, pēc tam Darbību rūtī atlasiet **Darba laiki**.</span><span class="sxs-lookup"><span data-stu-id="12c8a-115">Make sure the row is selected, then select **Working times** from the Action Pane.</span></span>
8. <span data-ttu-id="12c8a-116">Atlasiet **Darba laiku definēšana**.</span><span class="sxs-lookup"><span data-stu-id="12c8a-116">Select **Compose working times**.</span></span> <span data-ttu-id="12c8a-117">Ģenerējiet darba stundas katrai dienai periodā, kurā vēlaties plānot darbu.</span><span class="sxs-lookup"><span data-stu-id="12c8a-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="12c8a-118">Laika gaitā jūs varat ģenerēt darba laikus papildu periodiem.</span><span class="sxs-lookup"><span data-stu-id="12c8a-118">As time goes by, you can generate working times for additional periods.</span></span>  
9. <span data-ttu-id="12c8a-119">Ievadiet datumu laukā **No datuma**.</span><span class="sxs-lookup"><span data-stu-id="12c8a-119">In the **From date** field, enter a date.</span></span> <span data-ttu-id="12c8a-120">Tā ir pirmā diena, kad šim kalendāram ir jābūt atvērtam.</span><span class="sxs-lookup"><span data-stu-id="12c8a-120">This is the first day that this calendar must be open.</span></span>  
10. <span data-ttu-id="12c8a-121">Ievadiet datumu laukā **Līdz datumam**.</span><span class="sxs-lookup"><span data-stu-id="12c8a-121">In the **To date field**, enter a date.</span></span> <span data-ttu-id="12c8a-122">Tā ir pēdējā diena, kad šis kalendārs ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="12c8a-122">This is the last day that this calendar is open.</span></span>  
11. <span data-ttu-id="12c8a-123">Laukā **Darba laika veidne** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="12c8a-123">In the **Working time template** field, enter or select a value.</span></span> <span data-ttu-id="12c8a-124">Darba laika veidne nosaka darba stundas katrai nedēļas dienai.</span><span class="sxs-lookup"><span data-stu-id="12c8a-124">The working time template defines the working hours for each day of the week.</span></span>  
12. <span data-ttu-id="12c8a-125">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="12c8a-125">Select **OK**.</span></span>
13. <span data-ttu-id="12c8a-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="12c8a-126">Close the page.</span></span>

