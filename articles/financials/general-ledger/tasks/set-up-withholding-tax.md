--- 
title: "Ieturētā nodokļa iestatīšana"
description: "Ieturētais nodoklis ir nodoklis, kas tiek piemērots kreditoram, kuri neveido PVN darījumus."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ccaccd7b5b32431ac463925c887324a7607ae7dc
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="f6c66-103">Ieturētā nodokļa iestatīšana</span><span class="sxs-lookup"><span data-stu-id="f6c66-103">Set up withholding tax</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f6c66-104">Ieturētais nodoklis ir nodoklis, kas tiek piemērots kreditoram, kuri neveido PVN darījumus.</span><span class="sxs-lookup"><span data-stu-id="f6c66-104">Withholding tax is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="f6c66-105">Ieturētais nodoklis, kas tiek aprēķināts kreditora maksājumiem, ir pasīvs.</span><span class="sxs-lookup"><span data-stu-id="f6c66-105">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="f6c66-106">Tāpēc ieturētā nodokļa grāmatošanai ir derīgi tikai bilances konti vai pasīvu konti.</span><span class="sxs-lookup"><span data-stu-id="f6c66-106">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="f6c66-107">Šis uzdevuma ceļvedis parāda, kā iestatīt ieturēto nodokli.</span><span class="sxs-lookup"><span data-stu-id="f6c66-107">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="f6c66-108">Pārejiet uz sadaļu Nodokļi > Netiešie nodokļi > Ieturētais nodoklis > Ieturētā nodokļa kodi.</span><span class="sxs-lookup"><span data-stu-id="f6c66-108">Go to Tax > Indirect taxes > Withholding tax > Withholding tax codes.</span></span>
2. <span data-ttu-id="f6c66-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="f6c66-109">Click New.</span></span>
3. <span data-ttu-id="f6c66-110">Ierakstiet vērtību laukā Ieturētā nodokļa kods.</span><span class="sxs-lookup"><span data-stu-id="f6c66-110">In the Withholding tax code field, type a value.</span></span>
4. <span data-ttu-id="f6c66-111">Laukā Ieturētā nodokļa nosaukums ievadiet ieturētā nodokļa koda nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="f6c66-111">In the Withholding tax name field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="f6c66-112">Laukā Galvenais konts atlasiet galveno kontu ieturētā nodokļa parādu grāmatošanai.</span><span class="sxs-lookup"><span data-stu-id="f6c66-112">In the Main account field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="f6c66-113">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f6c66-113">Click Save.</span></span>
7. <span data-ttu-id="f6c66-114">Noklikšķiniet uz vienuma Vērtības.</span><span class="sxs-lookup"><span data-stu-id="f6c66-114">Click Values.</span></span>
8. <span data-ttu-id="f6c66-115">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="f6c66-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="f6c66-116">Laukā Vērtība ievadiet ieturētā nodokļa aprēķinam izmantojamo procentuālo vērtību.</span><span class="sxs-lookup"><span data-stu-id="f6c66-116">In the Value field, enter a percentage used for the calculation of the withholding tax.</span></span>
10. <span data-ttu-id="f6c66-117">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f6c66-117">Click Save.</span></span>
11. <span data-ttu-id="f6c66-118">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f6c66-118">Close the page.</span></span>
12. <span data-ttu-id="f6c66-119">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f6c66-119">Click Save.</span></span>
13. <span data-ttu-id="f6c66-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f6c66-120">Close the page.</span></span>
14. <span data-ttu-id="f6c66-121">Pārejiet uz sadaļu Nodokļi > Netiešie nodokļi > Ieturētais nodoklis > Ieturētā nodokļa grupas.</span><span class="sxs-lookup"><span data-stu-id="f6c66-121">Go to Tax > Indirect taxes > Withholding tax > Withholding tax groups.</span></span>
15. <span data-ttu-id="f6c66-122">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="f6c66-122">Click New.</span></span>
16. <span data-ttu-id="f6c66-123">Laukā Ieturētā nodokļa grupa ievadiet ieturētā nodokļa grupas identifikatoru.</span><span class="sxs-lookup"><span data-stu-id="f6c66-123">In the Withholding tax group field, enter the identifier of the withholding tax group.</span></span>
17. <span data-ttu-id="f6c66-124">Laukā Apraksts ievadiet krājumu ieturētā nodokļa grupas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="f6c66-124">In the Description field, enter the name of the withholding tax group.</span></span>
18. <span data-ttu-id="f6c66-125">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="f6c66-125">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="f6c66-126">Laukā Ieturētā nodokļa kods atlasiet ieturētā nodokļa kodu.</span><span class="sxs-lookup"><span data-stu-id="f6c66-126">In the Withholding tax code field, select the withholding tax code.</span></span>
20. <span data-ttu-id="f6c66-127">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f6c66-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="f6c66-128">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f6c66-128">Click Save.</span></span>


