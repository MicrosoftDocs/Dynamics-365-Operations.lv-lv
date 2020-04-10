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
ms.openlocfilehash: 01b797aa97e73cbe112c37a1efcd1e759730bc24
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149117"
---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="ac18b-103">Atsevišķu ražošanas resursu grupu definēšana</span><span class="sxs-lookup"><span data-stu-id="ac18b-103">Define discrete manufacturing resource group</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ac18b-104">Resursu grupa ir operācijas resursu kopa, kas parasti atbilst darba šūnu fiziskajai organizācijai, kuras ražotnē ir norādītas ar dzeltenām līnijām.</span><span class="sxs-lookup"><span data-stu-id="ac18b-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="ac18b-105">Šajā procedūrā ir parādīts, kā definēt resurss grupu izmantošanai atsevišķā ražošanā.</span><span class="sxs-lookup"><span data-stu-id="ac18b-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="ac18b-106">Šo procedūru varat izmēģināt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="ac18b-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="ac18b-107">Dodieties uz Resursu grupas.</span><span class="sxs-lookup"><span data-stu-id="ac18b-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="ac18b-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="ac18b-108">Click New.</span></span>
3. <span data-ttu-id="ac18b-109">Laukā Resursu grupa ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ac18b-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="ac18b-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ac18b-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ac18b-111">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ac18b-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="ac18b-112">Laukā Ražošanas vienība ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ac18b-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="ac18b-113">Definēt noklusējuma operāciju parametrus</span><span class="sxs-lookup"><span data-stu-id="ac18b-113">Define default operational parameters</span></span>
1. <span data-ttu-id="ac18b-114">Izvērsiet sadaļu Operācija.</span><span class="sxs-lookup"><span data-stu-id="ac18b-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="ac18b-115">Laukā Brāķis procentos ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="ac18b-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="ac18b-116">Laukā Iestatīšanas kategorija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ac18b-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="ac18b-117">Laukā Izpildlaiks ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ac18b-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="ac18b-118">Laukā Operāciju plānošanas procenti ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="ac18b-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="ac18b-119">Definēt darba stundas</span><span class="sxs-lookup"><span data-stu-id="ac18b-119">Define operating hours</span></span>
1. <span data-ttu-id="ac18b-120">Izvērsiet sadaļu Kalendāri.</span><span class="sxs-lookup"><span data-stu-id="ac18b-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="ac18b-121">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="ac18b-121">Click Add.</span></span>
3. <span data-ttu-id="ac18b-122">Laukā Kalendārs ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ac18b-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="ac18b-123">Pievienot operāciju resursus</span><span class="sxs-lookup"><span data-stu-id="ac18b-123">Add operations resources</span></span>
1. <span data-ttu-id="ac18b-124">Izvērsiet sadaļu Resursi.</span><span class="sxs-lookup"><span data-stu-id="ac18b-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="ac18b-125">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="ac18b-125">Click Add.</span></span>
3. <span data-ttu-id="ac18b-126">Laukā Resursi ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ac18b-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="ac18b-127">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="ac18b-127">Click Add.</span></span>
5. <span data-ttu-id="ac18b-128">Laukā Resursi ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ac18b-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="ac18b-129">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="ac18b-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ac18b-130">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="ac18b-130">In the list, click the link in the selected row.</span></span>

