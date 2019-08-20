---
title: Ieturētā nodokļa iestatīšana
description: Šajā tēmā ir paskaidrots, kā iestatīt ieturēto nodokli.
author: twheeloc
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10e7018c79e54841d0729636b08ad475a94d20d5
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834738"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="cc67c-103">Ieturētā nodokļa iestatīšana</span><span class="sxs-lookup"><span data-stu-id="cc67c-103">Set up withholding tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cc67c-104">Šajā tēmā ir paskaidrots, kā iestatīt ieturēto nodokli.</span><span class="sxs-lookup"><span data-stu-id="cc67c-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="cc67c-105">*Ieturētais nodoklis* ir nodoklis, kas tiek piemērots kreditoram, kuri neveido PVN darījumus.</span><span class="sxs-lookup"><span data-stu-id="cc67c-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="cc67c-106">Ieturētais nodoklis, kas tiek aprēķināts kreditora maksājumiem, ir pasīvs.</span><span class="sxs-lookup"><span data-stu-id="cc67c-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="cc67c-107">Tāpēc ieturētā nodokļa grāmatošanai ir derīgi tikai bilances konti vai pasīvu konti.</span><span class="sxs-lookup"><span data-stu-id="cc67c-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="cc67c-108">Šis uzdevuma ceļvedis parāda, kā iestatīt ieturēto nodokli.</span><span class="sxs-lookup"><span data-stu-id="cc67c-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="cc67c-109">Pārejiet uz **Navigācijas rūts > Moduļi > Nodokļi > Netiešie nodokļi > Ieturētais nodoklis > Ieturētā nodokļa kodi**.</span><span class="sxs-lookup"><span data-stu-id="cc67c-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="cc67c-110">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="cc67c-110">Select **New**.</span></span>
3. <span data-ttu-id="cc67c-111">Ierakstiet vērtību laukā **Ieturētā nodokļa kods**.</span><span class="sxs-lookup"><span data-stu-id="cc67c-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="cc67c-112">Laukā **Ieturētā nodokļa nosaukums** ievadiet ieturētā nodokļa koda nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="cc67c-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="cc67c-113">Laukā **Galvenais konts** atlasiet galveno kontu ieturētā nodokļa parādu grāmatošanai.</span><span class="sxs-lookup"><span data-stu-id="cc67c-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="cc67c-114">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="cc67c-114">Select **Save**.</span></span>
7. <span data-ttu-id="cc67c-115">Atlasiet **Vērtības** un atzīmējiet vēlamo ierakstu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="cc67c-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="cc67c-116">Laukā **Vērtība** ievadiet ieturētā nodokļa aprēķinam izmantojamo procentuālo vērtību.</span><span class="sxs-lookup"><span data-stu-id="cc67c-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="cc67c-117">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="cc67c-117">Select **Save**.</span></span>
10. <span data-ttu-id="cc67c-118">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cc67c-118">Close the page.</span></span>
11. <span data-ttu-id="cc67c-119">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="cc67c-119">Select **Save**.</span></span>
12. <span data-ttu-id="cc67c-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cc67c-120">Close the page.</span></span>
13. <span data-ttu-id="cc67c-121">Pārejiet uz **Navigācijas rūts > Moduļi > Nodokļi > Netiešie nodokļi > Ieturētais nodoklis > Ieturētā nodokļa grupas**.</span><span class="sxs-lookup"><span data-stu-id="cc67c-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="cc67c-122">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="cc67c-122">Select **New**.</span></span>
15. <span data-ttu-id="cc67c-123">Laukā **Ieturētā nodokļa grupa** ievadiet ieturētā nodokļa grupas identifikatoru.</span><span class="sxs-lookup"><span data-stu-id="cc67c-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="cc67c-124">Laukā **Apraksts** ievadiet krājumu ieturētā nodokļa grupas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="cc67c-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="cc67c-125">Laukā **Ieturētā nodokļa kods** atlasiet ieturētā nodokļa kodu.</span><span class="sxs-lookup"><span data-stu-id="cc67c-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="cc67c-126">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="cc67c-126">Select **Save**.</span></span>
19. <span data-ttu-id="cc67c-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cc67c-127">Close the page.</span></span>

