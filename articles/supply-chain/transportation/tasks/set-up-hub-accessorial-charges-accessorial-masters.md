--- 
title: "Pārkraušanas punkta papildobjekta maksas un papildobjekta šablonu iestatīšana"
description: "Šajā procedūrā parādīts, kā izveidot papildobjekta šablonu pārkraušanas punktam un izmantot šo šablonu, lai izveidotu pārkraušanas punkta papildobjekta maksu."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 61a506b3824fa220d052ca667199edac526c1cbc
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="d7214-103">Pārkraušanas punkta papildobjekta maksas un papildobjekta šablonu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d7214-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d7214-104">Šajā procedūrā parādīts, kā izveidot papildobjekta šablonu pārkraušanas punktam un izmantot šo šablonu, lai izveidotu pārkraušanas punkta papildobjekta maksu.</span><span class="sxs-lookup"><span data-stu-id="d7214-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="d7214-105">Procedūrā tiek izmantota USMF datu kopa.</span><span class="sxs-lookup"><span data-stu-id="d7214-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="d7214-106">Šo iestatīšanu parasti veic transportēšanas koordinators.</span><span class="sxs-lookup"><span data-stu-id="d7214-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="d7214-107">Pārkraušanas punkta šablona iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d7214-107">Set up a hub master</span></span>
1. <span data-ttu-id="d7214-108">Dodieties uz Transportēšanas pārvaldība > Iestatīšana > Vērtējums > Papildobjekta šabloni.</span><span class="sxs-lookup"><span data-stu-id="d7214-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="d7214-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d7214-109">Click New.</span></span>
3. <span data-ttu-id="d7214-110">Laukā Papildobjekta šablons ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d7214-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="d7214-111">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d7214-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d7214-112">Laukā Papildobjekta tips atlasiet "Pārkraušanas punkts".</span><span class="sxs-lookup"><span data-stu-id="d7214-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="d7214-113">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d7214-113">Click Save.</span></span>
7. <span data-ttu-id="d7214-114">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d7214-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="d7214-115">Pārkraušanas punkta papildobjekta maksas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d7214-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="d7214-116">Dodieties uz Transportēšanas pārvaldība > Iestatīšana > Vērtējums > Pārkraušanas punkta papildobjekta maksas.</span><span class="sxs-lookup"><span data-stu-id="d7214-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="d7214-117">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d7214-117">Click New.</span></span>
3. <span data-ttu-id="d7214-118">Laukā Pārkraušanas punkta papildobjekta ID ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d7214-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="d7214-119">Laukā Pārkraušanas punkts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d7214-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d7214-120">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d7214-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="d7214-121">Laukā Pārkraušanas punkta pozīcija atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="d7214-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="d7214-122">Varat izveidot maksu kā saņemšanas vai nodošanas maksu.</span><span class="sxs-lookup"><span data-stu-id="d7214-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="d7214-123">Atkarībā no veiktās atlases maksa tiks piemērota atbilstošam transportēšanas segmentam jūsu maršrutā.</span><span class="sxs-lookup"><span data-stu-id="d7214-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="d7214-124">Laukā Papildobjekta šablons noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d7214-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="d7214-125">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d7214-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d7214-126">Atlasiet tikko izveidoto šablonu.</span><span class="sxs-lookup"><span data-stu-id="d7214-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="d7214-127">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d7214-127">Click Save.</span></span>
10. <span data-ttu-id="d7214-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d7214-128">Close the page.</span></span>


