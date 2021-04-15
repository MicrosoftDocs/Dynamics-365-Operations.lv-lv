---
title: Ieturētā nodokļa iestatīšana
description: Šajā tēmā ir paskaidrots, kā iestatīt ieturēto nodokli.
author: twheeloc
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 592afb7542fa44dcb1bf3f7354937d3c21fb1a87
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813472"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="f7f0d-103">Ieturētā nodokļa iestatīšana</span><span class="sxs-lookup"><span data-stu-id="f7f0d-103">Set up withholding tax</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f7f0d-104">Šajā tēmā ir paskaidrots, kā iestatīt ieturēto nodokli.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="f7f0d-105">*Ieturētais nodoklis* ir nodoklis, kas tiek piemērots kreditoram, kuri neveido PVN darījumus.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="f7f0d-106">Ieturētais nodoklis, kas tiek aprēķināts kreditora maksājumiem, ir pasīvs.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="f7f0d-107">Tāpēc ieturētā nodokļa grāmatošanai ir derīgi tikai bilances konti vai pasīvu konti.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="f7f0d-108">Šis uzdevuma ceļvedis parāda, kā iestatīt ieturēto nodokli.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="f7f0d-109">Pārejiet uz **Navigācijas rūts > Moduļi > Nodokļi > Netiešie nodokļi > Ieturētais nodoklis > Ieturētā nodokļa kodi**.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="f7f0d-110">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-110">Select **New**.</span></span>
3. <span data-ttu-id="f7f0d-111">Ierakstiet vērtību laukā **Ieturētā nodokļa kods**.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="f7f0d-112">Laukā **Ieturētā nodokļa nosaukums** ievadiet ieturētā nodokļa koda nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="f7f0d-113">Laukā **Galvenais konts** atlasiet galveno kontu ieturētā nodokļa parādu grāmatošanai.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="f7f0d-114">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-114">Select **Save**.</span></span>
7. <span data-ttu-id="f7f0d-115">Atlasiet **Vērtības** un atzīmējiet vēlamo ierakstu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="f7f0d-116">Laukā **Vērtība** ievadiet ieturētā nodokļa aprēķinam izmantojamo procentuālo vērtību.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="f7f0d-117">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-117">Select **Save**.</span></span>
10. <span data-ttu-id="f7f0d-118">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-118">Close the page.</span></span>
11. <span data-ttu-id="f7f0d-119">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-119">Select **Save**.</span></span>
12. <span data-ttu-id="f7f0d-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-120">Close the page.</span></span>
13. <span data-ttu-id="f7f0d-121">Pārejiet uz **Navigācijas rūts > Moduļi > Nodokļi > Netiešie nodokļi > Ieturētais nodoklis > Ieturētā nodokļa grupas**.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="f7f0d-122">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-122">Select **New**.</span></span>
15. <span data-ttu-id="f7f0d-123">Laukā **Ieturētā nodokļa grupa** ievadiet ieturētā nodokļa grupas identifikatoru.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="f7f0d-124">Laukā **Apraksts** ievadiet krājumu ieturētā nodokļa grupas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="f7f0d-125">Laukā **Ieturētā nodokļa kods** atlasiet ieturētā nodokļa kodu.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="f7f0d-126">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-126">Select **Save**.</span></span>
19. <span data-ttu-id="f7f0d-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-127">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]