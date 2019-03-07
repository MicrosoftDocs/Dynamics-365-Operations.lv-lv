---
title: Ieturētā nodokļa iestatīšana
description: Ieturētais nodoklis ir nodoklis, kas tiek piemērots kreditoram, kuri neveido PVN darījumus.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 382b6332665af2491563960a75d498a4f007aba8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "337237"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="5c08b-103">Ieturētā nodokļa iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5c08b-103">Set up withholding tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5c08b-104">Ieturētais nodoklis ir nodoklis, kas tiek piemērots kreditoram, kuri neveido PVN darījumus.</span><span class="sxs-lookup"><span data-stu-id="5c08b-104">Withholding tax is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="5c08b-105">Ieturētais nodoklis, kas tiek aprēķināts kreditora maksājumiem, ir pasīvs.</span><span class="sxs-lookup"><span data-stu-id="5c08b-105">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="5c08b-106">Tāpēc ieturētā nodokļa grāmatošanai ir derīgi tikai bilances konti vai pasīvu konti.</span><span class="sxs-lookup"><span data-stu-id="5c08b-106">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="5c08b-107">Šis uzdevuma ceļvedis parāda, kā iestatīt ieturēto nodokli.</span><span class="sxs-lookup"><span data-stu-id="5c08b-107">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="5c08b-108">Pārejiet uz sadaļu Nodokļi > Netiešie nodokļi > Ieturētais nodoklis > Ieturētā nodokļa kodi.</span><span class="sxs-lookup"><span data-stu-id="5c08b-108">Go to Tax > Indirect taxes > Withholding tax > Withholding tax codes.</span></span>
2. <span data-ttu-id="5c08b-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="5c08b-109">Click New.</span></span>
3. <span data-ttu-id="5c08b-110">Ierakstiet vērtību laukā Ieturētā nodokļa kods.</span><span class="sxs-lookup"><span data-stu-id="5c08b-110">In the Withholding tax code field, type a value.</span></span>
4. <span data-ttu-id="5c08b-111">Laukā Ieturētā nodokļa nosaukums ievadiet ieturētā nodokļa koda nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="5c08b-111">In the Withholding tax name field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="5c08b-112">Laukā Galvenais konts atlasiet galveno kontu ieturētā nodokļa parādu grāmatošanai.</span><span class="sxs-lookup"><span data-stu-id="5c08b-112">In the Main account field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="5c08b-113">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="5c08b-113">Click Save.</span></span>
7. <span data-ttu-id="5c08b-114">Noklikšķiniet uz vienuma Vērtības.</span><span class="sxs-lookup"><span data-stu-id="5c08b-114">Click Values.</span></span>
8. <span data-ttu-id="5c08b-115">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="5c08b-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="5c08b-116">Laukā Vērtība ievadiet ieturētā nodokļa aprēķinam izmantojamo procentuālo vērtību.</span><span class="sxs-lookup"><span data-stu-id="5c08b-116">In the Value field, enter a percentage used for the calculation of the withholding tax.</span></span>
10. <span data-ttu-id="5c08b-117">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="5c08b-117">Click Save.</span></span>
11. <span data-ttu-id="5c08b-118">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5c08b-118">Close the page.</span></span>
12. <span data-ttu-id="5c08b-119">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="5c08b-119">Click Save.</span></span>
13. <span data-ttu-id="5c08b-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5c08b-120">Close the page.</span></span>
14. <span data-ttu-id="5c08b-121">Pārejiet uz sadaļu Nodokļi > Netiešie nodokļi > Ieturētais nodoklis > Ieturētā nodokļa grupas.</span><span class="sxs-lookup"><span data-stu-id="5c08b-121">Go to Tax > Indirect taxes > Withholding tax > Withholding tax groups.</span></span>
15. <span data-ttu-id="5c08b-122">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="5c08b-122">Click New.</span></span>
16. <span data-ttu-id="5c08b-123">Laukā Ieturētā nodokļa grupa ievadiet ieturētā nodokļa grupas identifikatoru.</span><span class="sxs-lookup"><span data-stu-id="5c08b-123">In the Withholding tax group field, enter the identifier of the withholding tax group.</span></span>
17. <span data-ttu-id="5c08b-124">Laukā Apraksts ievadiet krājumu ieturētā nodokļa grupas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="5c08b-124">In the Description field, enter the name of the withholding tax group.</span></span>
18. <span data-ttu-id="5c08b-125">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="5c08b-125">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="5c08b-126">Laukā Ieturētā nodokļa kods atlasiet ieturētā nodokļa kodu.</span><span class="sxs-lookup"><span data-stu-id="5c08b-126">In the Withholding tax code field, select the withholding tax code.</span></span>
20. <span data-ttu-id="5c08b-127">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="5c08b-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="5c08b-128">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="5c08b-128">Click Save.</span></span>

