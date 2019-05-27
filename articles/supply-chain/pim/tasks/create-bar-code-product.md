---
title: Preces svītrkoda izveide
description: Šajā procedūrā parādīts, kā manuāli izveidot svītrkodu, kā piemēru izmantojot krājuma kodu M0001.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, InventItemBarcode, InventItemBarcodeLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ae2765a125045d60566267d01e380069d5d527c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568608"
---
# <a name="create-a-bar-code-for-a-product"></a><span data-ttu-id="f12b9-103">Preces svītrkoda izveide</span><span class="sxs-lookup"><span data-stu-id="f12b9-103">Create a bar code for a product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f12b9-104">Šajā procedūrā parādīts, kā manuāli izveidot svītrkodu, kā piemēru izmantojot krājuma kodu M0001.</span><span class="sxs-lookup"><span data-stu-id="f12b9-104">This procedure shows how to manually create a bar code using the item number M0001 as an example.</span></span> <span data-ttu-id="f12b9-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="f12b9-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="f12b9-106">Noklikšķiniet uz Izlaisto preču uzturēšana.</span><span class="sxs-lookup"><span data-stu-id="f12b9-106">Click Released product maintenance.</span></span>
2. <span data-ttu-id="f12b9-107">Noklikšķiniet uz Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="f12b9-107">Click Released products.</span></span>
3. <span data-ttu-id="f12b9-108">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f12b9-108">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="f12b9-109">Darbību rūtī noklikšķiniet uz Pārvaldīt krājumus.</span><span class="sxs-lookup"><span data-stu-id="f12b9-109">On the Action Pane, click Manage inventory.</span></span>
5. <span data-ttu-id="f12b9-110">Noklikšķiniet uz Svītrkodi.</span><span class="sxs-lookup"><span data-stu-id="f12b9-110">Click Bar codes.</span></span>
6. <span data-ttu-id="f12b9-111">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="f12b9-111">Click New.</span></span>
7. <span data-ttu-id="f12b9-112">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="f12b9-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="f12b9-113">Ievadiet vai atlasiet vērtību laukā Svītrkodu iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="f12b9-113">In the Barcode setup field, enter or select a value.</span></span>
9. <span data-ttu-id="f12b9-114">Laukā Svītrkods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f12b9-114">In the Bar code field, enter or select a value.</span></span>
10. <span data-ttu-id="f12b9-115">Laukā Svītrkods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f12b9-115">In the Bar code field, type a value.</span></span>
    * <span data-ttu-id="f12b9-116">Nospiediet taustiņu Tab.</span><span class="sxs-lookup"><span data-stu-id="f12b9-116">Press the Tab key.</span></span>  
11. <span data-ttu-id="f12b9-117">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f12b9-117">Close the page.</span></span>
12. <span data-ttu-id="f12b9-118">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="f12b9-118">In the Quantity field, enter a number.</span></span>
13. <span data-ttu-id="f12b9-119">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f12b9-119">Click Save.</span></span>
    * <span data-ttu-id="f12b9-120">Noklikšķinot uz Saglabāt, tiek veikta svītrkoda pārbaude, un šajā gadījumā tiks parādīta kļūda, norādot, ka paredzētais kontrolcipars ir 8, bet tika atrasts 3.</span><span class="sxs-lookup"><span data-stu-id="f12b9-120">When you click Save, the barcode check is run, and in this case it will display an error stating that the expected check digit is 8, but that 3 was found.</span></span> <span data-ttu-id="f12b9-121">Manuāli atjauniniet svītrkoda numuru, lai beigās ir 8.</span><span class="sxs-lookup"><span data-stu-id="f12b9-121">Manually update the barcode number so that 8 is at the end.</span></span>  
14. <span data-ttu-id="f12b9-122">Laukā Svītrkods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f12b9-122">In the Bar code field, enter or select a value.</span></span>
15. <span data-ttu-id="f12b9-123">Laukā Svītrkods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f12b9-123">In the Bar code field, type a value.</span></span>
    * <span data-ttu-id="f12b9-124">Nospiediet taustiņu Tab.</span><span class="sxs-lookup"><span data-stu-id="f12b9-124">Press the Tab key.</span></span>  
16. <span data-ttu-id="f12b9-125">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f12b9-125">Close the page.</span></span>
17. <span data-ttu-id="f12b9-126">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f12b9-126">Click Save.</span></span>
18. <span data-ttu-id="f12b9-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f12b9-127">Close the page.</span></span>

