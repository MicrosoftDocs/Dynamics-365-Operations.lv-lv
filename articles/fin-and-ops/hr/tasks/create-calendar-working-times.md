--- 
title: "Kalendāra izveide un darba laiku ģenerēšana"
description: "Kalendāros ir norādīta operāciju resursu noslodze un darba laiki."
author: kherr75
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a8dcef8d8ba6f6d41a997b5b0623cb9577ce00d3
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-calendar-and-generate-working-times"></a><span data-ttu-id="b3d43-103">Kalendāra izveide un darba laiku ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="b3d43-103">Create a calendar and generate working times</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b3d43-104">Kalendāros ir norādīta operāciju resursu noslodze un darba laiki.</span><span class="sxs-lookup"><span data-stu-id="b3d43-104">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="b3d43-105">Šī procedūra palīdzēs jums izveidot darba kalendāru, pamatojoties uz darba laika veidni.</span><span class="sxs-lookup"><span data-stu-id="b3d43-105">This procedure will help you define a work calendar based on a working time template.</span></span> <span data-ttu-id="b3d43-106">Šo procedūru var izmēģināt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="b3d43-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="b3d43-107">Pārejiet uz sadaļu Visas darbvietas > Resursu darbmūža pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="b3d43-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="b3d43-108">Noklikšķiniet uz Kalendāri.</span><span class="sxs-lookup"><span data-stu-id="b3d43-108">Click Calendars.</span></span>
3. <span data-ttu-id="b3d43-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b3d43-109">Click New.</span></span>
4. <span data-ttu-id="b3d43-110">Laukā Kalendārs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="b3d43-110">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="b3d43-111">Tas ir kalendāra ID, kas tiek izmantots kā atsauce, piešķirot kalendārus, piemēram, operācijas resursiem vai resursu grupai.</span><span class="sxs-lookup"><span data-stu-id="b3d43-111">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="b3d43-112">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b3d43-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="b3d43-113">Ievadiet skaitli laukā Standarta darba dienas ilgums stundās.</span><span class="sxs-lookup"><span data-stu-id="b3d43-113">In the Standard work day in hours field, enter a number.</span></span>
7. <span data-ttu-id="b3d43-114">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="b3d43-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="b3d43-115">Noklikšķiniet uz Darba laiki.</span><span class="sxs-lookup"><span data-stu-id="b3d43-115">Click Working times.</span></span>
9. <span data-ttu-id="b3d43-116">Noklikšķiniet uz Darba laiku definēšana.</span><span class="sxs-lookup"><span data-stu-id="b3d43-116">Click Compose working times.</span></span>
    * <span data-ttu-id="b3d43-117">Ģenerējiet darba stundas katrai dienai periodā, kurā vēlaties plānot darbu.</span><span class="sxs-lookup"><span data-stu-id="b3d43-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="b3d43-118">Laika gaitā jūs varat ģenerēt darba laikus papildu periodiem.</span><span class="sxs-lookup"><span data-stu-id="b3d43-118">As time goes by, you can generate working times for additional periods.</span></span>  
10. <span data-ttu-id="b3d43-119">Ievadiet datumu laukā No datuma.</span><span class="sxs-lookup"><span data-stu-id="b3d43-119">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="b3d43-120">Tā ir pirmā diena, kad šim kalendāram ir jābūt atvērtam.</span><span class="sxs-lookup"><span data-stu-id="b3d43-120">This is the first day that this calendar must be open.</span></span>  
11. <span data-ttu-id="b3d43-121">Laukā Līdz datumam ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="b3d43-121">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="b3d43-122">Tā ir pēdējā diena, kad šis kalendārs ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="b3d43-122">This is the last day that this calendar is open.</span></span>  
12. <span data-ttu-id="b3d43-123">Laukā Darba laika veidne ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b3d43-123">In the Working time template field, enter or select a value.</span></span>
    * <span data-ttu-id="b3d43-124">Darba laika veidne nosaka darba stundas katrai nedēļas dienai.</span><span class="sxs-lookup"><span data-stu-id="b3d43-124">The working time template defines the working hours for each day of the week.</span></span>  
13. <span data-ttu-id="b3d43-125">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="b3d43-125">Click OK.</span></span>
14. <span data-ttu-id="b3d43-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b3d43-126">Close the page.</span></span>


