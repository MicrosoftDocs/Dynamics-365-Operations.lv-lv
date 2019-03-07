---
title: Atsevišķu ražošanas resursu grupu definēšana
description: Resursu grupa ir operācijas resursu kopa, kas parasti atbilst darba šūnu fiziskajai organizācijai, kuras ražotnē ir norādītas ar dzeltenām līnijām.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 50733e34bbf14ae2cade6822105da4d8c2120d7d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "353245"
---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="b3f32-103">Atsevišķu ražošanas resursu grupu definēšana</span><span class="sxs-lookup"><span data-stu-id="b3f32-103">Define discrete manufacturing resource group</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b3f32-104">Resursu grupa ir operācijas resursu kopa, kas parasti atbilst darba šūnu fiziskajai organizācijai, kuras ražotnē ir norādītas ar dzeltenām līnijām.</span><span class="sxs-lookup"><span data-stu-id="b3f32-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="b3f32-105">Šajā procedūrā ir parādīts, kā definēt resurss grupu izmantošanai atsevišķā ražošanā.</span><span class="sxs-lookup"><span data-stu-id="b3f32-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="b3f32-106">Šo procedūru varat izmēģināt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="b3f32-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="b3f32-107">Dodieties uz Resursu grupas.</span><span class="sxs-lookup"><span data-stu-id="b3f32-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="b3f32-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b3f32-108">Click New.</span></span>
3. <span data-ttu-id="b3f32-109">Laukā Resursu grupa ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b3f32-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="b3f32-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="b3f32-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b3f32-111">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b3f32-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="b3f32-112">Laukā Ražošanas vienība ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b3f32-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="b3f32-113">Definēt noklusējuma operāciju parametrus</span><span class="sxs-lookup"><span data-stu-id="b3f32-113">Define default operational parameters</span></span>
1. <span data-ttu-id="b3f32-114">Izvērsiet sadaļu Operācija.</span><span class="sxs-lookup"><span data-stu-id="b3f32-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="b3f32-115">Laukā Brāķis procentos ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="b3f32-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="b3f32-116">Laukā Iestatīšanas kategorija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b3f32-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="b3f32-117">Laukā Izpildlaiks ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b3f32-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="b3f32-118">Laukā Operāciju plānošanas procenti ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="b3f32-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="b3f32-119">Definēt darba stundas</span><span class="sxs-lookup"><span data-stu-id="b3f32-119">Define operating hours</span></span>
1. <span data-ttu-id="b3f32-120">Izvērsiet sadaļu Kalendāri.</span><span class="sxs-lookup"><span data-stu-id="b3f32-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="b3f32-121">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b3f32-121">Click Add.</span></span>
3. <span data-ttu-id="b3f32-122">Laukā Kalendārs ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b3f32-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="b3f32-123">Pievienot operāciju resursus</span><span class="sxs-lookup"><span data-stu-id="b3f32-123">Add operations resources</span></span>
1. <span data-ttu-id="b3f32-124">Izvērsiet sadaļu Resursi.</span><span class="sxs-lookup"><span data-stu-id="b3f32-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="b3f32-125">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b3f32-125">Click Add.</span></span>
3. <span data-ttu-id="b3f32-126">Laukā Resursi ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b3f32-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="b3f32-127">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b3f32-127">Click Add.</span></span>
5. <span data-ttu-id="b3f32-128">Laukā Resursi ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b3f32-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="b3f32-129">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b3f32-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="b3f32-130">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b3f32-130">In the list, click the link in the selected row.</span></span>

