---
title: Izmaksu uzskaites virsgrāmatas datu avota pārvaldība
description: Izmantojiet šo procedūru, lai pārvaldītu izmaksu uzskaites virsgrāmatas datu avotu.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMAXGeneralLedgerEntryProviderConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 48d92a634a08f686e29260a71782bbacf7215f2f
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759164"
---
# <a name="manage-a-data-source-for-the-cost-accounting-ledger"></a><span data-ttu-id="46c3d-103">Izmaksu uzskaites virsgrāmatas datu avota pārvaldība</span><span class="sxs-lookup"><span data-stu-id="46c3d-103">Manage a data source for the cost accounting ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="46c3d-104">Izmantojiet šo procedūru, lai pārvaldītu izmaksu uzskaites virsgrāmatas datu avotu.</span><span class="sxs-lookup"><span data-stu-id="46c3d-104">Use this procedure to manage the general ledger data source for a cost accounting ledger.</span></span> <span data-ttu-id="46c3d-105">Pirms varat pabeigt šo uzdevumu, atskaņojiet uzdevuma ceļvežus "Izmaksu uzskaites virsgrāmatas izveide" un "Izmaksu vadības ierīču definēšana".</span><span class="sxs-lookup"><span data-stu-id="46c3d-105">Before you complete this task, make sure that you play the "Create a cost accounting ledger" and "Define cost control units" task guides.</span></span> <span data-ttu-id="46c3d-106">Šajā ierakstā tiek izmantots USP2 demonstrācijas datu uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="46c3d-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="46c3d-107">Dodieties uz Izmaksu uzskaite > Virsgrāmatas iestatīšana > Izmaksu uzskaites virsgrāmatas.</span><span class="sxs-lookup"><span data-stu-id="46c3d-107">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="46c3d-108">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="46c3d-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="46c3d-109">Noklikšķiniet uz Faktiskās versijas.</span><span class="sxs-lookup"><span data-stu-id="46c3d-109">Click Actual versions.</span></span>
4. <span data-ttu-id="46c3d-110">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="46c3d-110">On the Action Pane, click Manage.</span></span>
5. <span data-ttu-id="46c3d-111">Noklikšķiniet uz Virsgrāmata.</span><span class="sxs-lookup"><span data-stu-id="46c3d-111">Click General ledger.</span></span>
6. <span data-ttu-id="46c3d-112">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="46c3d-112">Click New.</span></span>
7. <span data-ttu-id="46c3d-113">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="46c3d-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="46c3d-114">Laukā Datu nodrošinātājs ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="46c3d-114">In the Data provider field, enter or select a value.</span></span>
    * <span data-ttu-id="46c3d-115">Šim piemēram atlasiet Dynamics 365 Finance - Virsgrāmatas ieraksti.</span><span class="sxs-lookup"><span data-stu-id="46c3d-115">For this example, select Dynamics 365 Finance - General ledger entries.</span></span>  
9. <span data-ttu-id="46c3d-116">Laukā Izmaksu elementa dimensija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="46c3d-116">In the Cost element dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="46c3d-117">Šim piemēram atlasiet Izmaksu elementi.</span><span class="sxs-lookup"><span data-stu-id="46c3d-117">For this example, select Cost elements.</span></span>  
10. <span data-ttu-id="46c3d-118">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="46c3d-118">Click Save.</span></span>
11. <span data-ttu-id="46c3d-119">Noklikšķiniet uz Konfigurēt datu nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="46c3d-119">Click Configure data provider.</span></span>
12. <span data-ttu-id="46c3d-120">Laukā Juridiska persona ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="46c3d-120">In the Legal entity field, enter or select a value.</span></span>
    * <span data-ttu-id="46c3d-121">Šim piemēram atlasiet vienumu USP2.</span><span class="sxs-lookup"><span data-stu-id="46c3d-121">For this example, select USP2.</span></span>  
13. <span data-ttu-id="46c3d-122">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="46c3d-122">Click New.</span></span>
14. <span data-ttu-id="46c3d-123">Laukā Grāmatošanas līmenis atlasiet Pašreizējais.</span><span class="sxs-lookup"><span data-stu-id="46c3d-123">In the Posting layer field, select Current.</span></span>
15. <span data-ttu-id="46c3d-124">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="46c3d-124">Click OK.</span></span>

