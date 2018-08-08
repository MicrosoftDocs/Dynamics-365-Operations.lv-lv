--- 
title: "Atsevišķu ražošanas resursu grupu definēšana"
description: "Resursu grupa ir operācijas resursu kopa, kas parasti atbilst darba šūnu fiziskajai organizācijai, kuras ražotnē ir norādītas ar dzeltenām līnijām."
author: sorenva
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e1be950a7d1d7548aced041a189222b472d767cf
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="de272-103">Atsevišķu ražošanas resursu grupu definēšana</span><span class="sxs-lookup"><span data-stu-id="de272-103">Define discrete manufacturing resource group</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="de272-104">Resursu grupa ir operācijas resursu kopa, kas parasti atbilst darba šūnu fiziskajai organizācijai, kuras ražotnē ir norādītas ar dzeltenām līnijām.</span><span class="sxs-lookup"><span data-stu-id="de272-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="de272-105">Šajā procedūrā ir parādīts, kā definēt resursu grupu izmantošanai atsevišķā ražošanā.</span><span class="sxs-lookup"><span data-stu-id="de272-105">This procedure shows you how to define a resource group for use in discrete production.</span></span> <span data-ttu-id="de272-106">Šo procedūru varat izmēģināt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="de272-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="de272-107">Dodieties uz Resursu grupas.</span><span class="sxs-lookup"><span data-stu-id="de272-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="de272-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="de272-108">Click New.</span></span>
3. <span data-ttu-id="de272-109">Laukā Resursu grupa ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="de272-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="de272-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="de272-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="de272-111">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="de272-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="de272-112">Laukā Ražošanas vienība ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="de272-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="de272-113">Definēt noklusējuma operāciju parametrus</span><span class="sxs-lookup"><span data-stu-id="de272-113">Define default operational parameters</span></span>
1. <span data-ttu-id="de272-114">Izvērsiet sadaļu Operācija.</span><span class="sxs-lookup"><span data-stu-id="de272-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="de272-115">Laukā Brāķis procentos ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="de272-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="de272-116">Laukā Iestatīšanas kategorija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="de272-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="de272-117">Laukā Izpildlaiks ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="de272-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="de272-118">Laukā Operāciju plānošanas procenti ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="de272-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="de272-119">Definēt darba stundas</span><span class="sxs-lookup"><span data-stu-id="de272-119">Define operating hours</span></span>
1. <span data-ttu-id="de272-120">Izvērsiet sadaļu Kalendāri.</span><span class="sxs-lookup"><span data-stu-id="de272-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="de272-121">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="de272-121">Click Add.</span></span>
3. <span data-ttu-id="de272-122">Laukā Kalendārs ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="de272-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="de272-123">Pievienot operāciju resursus</span><span class="sxs-lookup"><span data-stu-id="de272-123">Add operations resources</span></span>
1. <span data-ttu-id="de272-124">Izvērsiet sadaļu Resursi.</span><span class="sxs-lookup"><span data-stu-id="de272-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="de272-125">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="de272-125">Click Add.</span></span>
3. <span data-ttu-id="de272-126">Laukā Resursi ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="de272-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="de272-127">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="de272-127">Click Add.</span></span>
5. <span data-ttu-id="de272-128">Laukā Resursi ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="de272-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="de272-129">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="de272-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="de272-130">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="de272-130">In the list, click the link in the selected row.</span></span>


