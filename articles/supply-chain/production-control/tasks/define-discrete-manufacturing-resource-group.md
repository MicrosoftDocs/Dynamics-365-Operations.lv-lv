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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 40a0638662cbace147aeb24bd20d3ae34a0c1670
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837672"
---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="a6e7c-103">Atsevišķu ražošanas resursu grupu definēšana</span><span class="sxs-lookup"><span data-stu-id="a6e7c-103">Define discrete manufacturing resource group</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a6e7c-104">Resursu grupa ir operācijas resursu kopa, kas parasti atbilst darba šūnu fiziskajai organizācijai, kuras ražotnē ir norādītas ar dzeltenām līnijām.</span><span class="sxs-lookup"><span data-stu-id="a6e7c-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="a6e7c-105">Šajā procedūrā ir parādīts, kā definēt resurss grupu izmantošanai atsevišķā ražošanā.</span><span class="sxs-lookup"><span data-stu-id="a6e7c-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="a6e7c-106">Šo procedūru varat izmēģināt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="a6e7c-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="a6e7c-107">Dodieties uz Resursu grupas.</span><span class="sxs-lookup"><span data-stu-id="a6e7c-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="a6e7c-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a6e7c-108">Click New.</span></span>
3. <span data-ttu-id="a6e7c-109">Laukā Resursu grupa ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a6e7c-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="a6e7c-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a6e7c-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a6e7c-111">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a6e7c-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="a6e7c-112">Laukā Ražošanas vienība ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a6e7c-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="a6e7c-113">Definēt noklusējuma operāciju parametrus</span><span class="sxs-lookup"><span data-stu-id="a6e7c-113">Define default operational parameters</span></span>
1. <span data-ttu-id="a6e7c-114">Izvērsiet sadaļu Operācija.</span><span class="sxs-lookup"><span data-stu-id="a6e7c-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="a6e7c-115">Laukā Brāķis procentos ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="a6e7c-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="a6e7c-116">Laukā Iestatīšanas kategorija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a6e7c-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="a6e7c-117">Laukā Izpildlaiks ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a6e7c-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="a6e7c-118">Laukā Operāciju plānošanas procenti ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="a6e7c-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="a6e7c-119">Definēt darba stundas</span><span class="sxs-lookup"><span data-stu-id="a6e7c-119">Define operating hours</span></span>
1. <span data-ttu-id="a6e7c-120">Izvērsiet sadaļu Kalendāri.</span><span class="sxs-lookup"><span data-stu-id="a6e7c-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="a6e7c-121">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="a6e7c-121">Click Add.</span></span>
3. <span data-ttu-id="a6e7c-122">Laukā Kalendārs ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a6e7c-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="a6e7c-123">Pievienot operāciju resursus</span><span class="sxs-lookup"><span data-stu-id="a6e7c-123">Add operations resources</span></span>
1. <span data-ttu-id="a6e7c-124">Izvērsiet sadaļu Resursi.</span><span class="sxs-lookup"><span data-stu-id="a6e7c-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="a6e7c-125">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="a6e7c-125">Click Add.</span></span>
3. <span data-ttu-id="a6e7c-126">Laukā Resursi ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a6e7c-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="a6e7c-127">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="a6e7c-127">Click Add.</span></span>
5. <span data-ttu-id="a6e7c-128">Laukā Resursi ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a6e7c-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="a6e7c-129">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a6e7c-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="a6e7c-130">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a6e7c-130">In the list, click the link in the selected row.</span></span>

