---
title: Izveidot pabeigtu preci (2016. gada februāris)
description: Šajā uzdevumā uzmanība ir vērsta uz pabeigtas preces izveidošanu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44b3bf17c69f37e7a96c75345a3e4f27ba9eab50
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "349726"
---
# <a name="create-a-finished-product-february-2016"></a><span data-ttu-id="e53eb-103">Izveidot pabeigtu preci (2016. gada februāris)</span><span class="sxs-lookup"><span data-stu-id="e53eb-103">Create a finished product (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e53eb-104">Šajā uzdevumā uzmanība ir vērsta uz pabeigtas preces izveidošanu.</span><span class="sxs-lookup"><span data-stu-id="e53eb-104">This task focuses on creating a finished product.</span></span> <span data-ttu-id="e53eb-105">Tas ir MK aprēķina sērijas pirmais uzdevums.</span><span class="sxs-lookup"><span data-stu-id="e53eb-105">It is the first task in the BOM calculation series.</span></span> <span data-ttu-id="e53eb-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="e53eb-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="e53eb-107">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="e53eb-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="e53eb-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e53eb-108">Click New.</span></span>
3. <span data-ttu-id="e53eb-109">Laukā Preces numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="e53eb-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="e53eb-110">Demonstrācijas nolūkos ierakstiet BOM_1.</span><span class="sxs-lookup"><span data-stu-id="e53eb-110">For the demonstration, type BOM_1.</span></span>  
4. <span data-ttu-id="e53eb-111">Laukā Krājumu modeļu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e53eb-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="e53eb-112">Atlasiet STD.</span><span class="sxs-lookup"><span data-stu-id="e53eb-112">Select STD.</span></span> <span data-ttu-id="e53eb-113">STD nozīmē standarta izmaksas, un tas ir visplašāk izmantotais modelis, strādājot ar izmaksu aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="e53eb-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="e53eb-114">Laukā Krājumu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e53eb-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="e53eb-115">Atlasiet, piemēram, Audio.</span><span class="sxs-lookup"><span data-stu-id="e53eb-115">For example, select Audio.</span></span> <span data-ttu-id="e53eb-116">Tas neietekmē izmaksu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="e53eb-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="e53eb-117">Laukā Noliktavas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e53eb-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e53eb-118">Atlasiet SiteWH.</span><span class="sxs-lookup"><span data-stu-id="e53eb-118">Select SiteWH.</span></span> <span data-ttu-id="e53eb-119">Demonstrācijai tiks izmantota tikai Vieta un Noliktava.</span><span class="sxs-lookup"><span data-stu-id="e53eb-119">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="e53eb-120">Laukā Izsekošanas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e53eb-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e53eb-121">Šajā piemērā izsekošanas dimensijas netiks lietotas, atlasiet Nav.</span><span class="sxs-lookup"><span data-stu-id="e53eb-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="e53eb-122">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="e53eb-122">Click OK.</span></span>
9. <span data-ttu-id="e53eb-123">Darbību rūtī noklikšķiniet uz Pārvaldīt krājumus.</span><span class="sxs-lookup"><span data-stu-id="e53eb-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="e53eb-124">Noklikšķiniet uz Pasūtījuma noklusējuma iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="e53eb-124">Click Default order settings.</span></span>
11. <span data-ttu-id="e53eb-125">Laukā Noklusējuma pasūtījuma tips atlasiet vērtību “Ražošana”.</span><span class="sxs-lookup"><span data-stu-id="e53eb-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="e53eb-126">Tā kā šī ir pabeigta prece, kas tiks ražota, atlasiet Ražošana.</span><span class="sxs-lookup"><span data-stu-id="e53eb-126">Because this is a finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="e53eb-127">Laukā Pirkšanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e53eb-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="e53eb-128">Demonstrācijas nolūkos atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="e53eb-128">For the demonstration, select Site 1.</span></span>  
13. <span data-ttu-id="e53eb-129">Laukā Krājumu vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e53eb-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="e53eb-130">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="e53eb-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="e53eb-131">Laukā Pārdošanas vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e53eb-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="e53eb-132">Šajā piemērā atlasiet vērtību 1. vieta.</span><span class="sxs-lookup"><span data-stu-id="e53eb-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="e53eb-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e53eb-133">Close the page.</span></span>

