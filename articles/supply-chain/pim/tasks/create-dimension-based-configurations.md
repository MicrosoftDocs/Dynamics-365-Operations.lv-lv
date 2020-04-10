---
title: Konfigurāciju izveide atbilstoši dimensijām
description: Šajā procedūrā ir parādīts, kā definēt konfigurāciju uz dimensiju balstītai precei.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, EcoResDimensionBasedConfiguration, ConfigChooseFromRoute, ConfigChooseFromGroup, ConfigChoiceApprove
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e612e3cd0343d386da4755f13eca6bf1443816d5
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150160"
---
# <a name="create-dimension-based-configurations"></a><span data-ttu-id="7d92e-103">Konfigurāciju izveide atbilstoši dimensijām</span><span class="sxs-lookup"><span data-stu-id="7d92e-103">Create dimension-based configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7d92e-104">Šajā procedūrā ir parādīts, kā definēt konfigurāciju uz dimensiju balstītai precei.</span><span class="sxs-lookup"><span data-stu-id="7d92e-104">This procedure shows how to define a configuration for a dimension-based product.</span></span> <span data-ttu-id="7d92e-105">Šī ir pēdējā procedūra šajā sērijā, kurā ir skaidrots, kā veidot kombinācijas konfigurācijai atbilstoši dimensijām.</span><span class="sxs-lookup"><span data-stu-id="7d92e-105">This is the last procedure in the series that explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="7d92e-106">Šīs procedūras izpilde ir atkarīga no datiem, kurus izveidojāt iepriekšējos septiņos ierakstos.</span><span class="sxs-lookup"><span data-stu-id="7d92e-106">The execution of this procedure is dependent on the data created in the previous seven recordings.</span></span> <span data-ttu-id="7d92e-107">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="7d92e-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-dimension-based-product-master"></a><span data-ttu-id="7d92e-108">Atrast uz dimensiju balstīto preces šablonu</span><span class="sxs-lookup"><span data-stu-id="7d92e-108">Find the dimension-based product master</span></span>
1. <span data-ttu-id="7d92e-109">Noklikšķiniet uz Izlaisto preču uzturēšana.</span><span class="sxs-lookup"><span data-stu-id="7d92e-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="7d92e-110">Noklikšķiniet uz Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="7d92e-110">Click Released products.</span></span>
3. <span data-ttu-id="7d92e-111">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="7d92e-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7d92e-112">Atlasiet uz dimensijām balstīto preces šablonu, kuru izveidojāt šīs 8 ierakstu procedūras pirmajā ierakstā.</span><span class="sxs-lookup"><span data-stu-id="7d92e-112">Select the dimension-based product master that you created in the first recording in this sequence of 8 recordings.</span></span>  

## <a name="create-configurations"></a><span data-ttu-id="7d92e-113">Izveidot konfigurācijas</span><span class="sxs-lookup"><span data-stu-id="7d92e-113">Create configurations</span></span>
1. <span data-ttu-id="7d92e-114">Tehnikas darbību rūtī noklikšķiniet uz Uzturēt konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="7d92e-114">On the Engineering Action Pane, click Maintain configurations.</span></span>
2. <span data-ttu-id="7d92e-115">Noklikšķiniet uz Konfigurēt.</span><span class="sxs-lookup"><span data-stu-id="7d92e-115">Click Configure.</span></span>
3. <span data-ttu-id="7d92e-116">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="7d92e-116">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="7d92e-117">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7d92e-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="7d92e-118">Atlasiet jebkuru no elementiem pirmajā konfigurācijas grupā.</span><span class="sxs-lookup"><span data-stu-id="7d92e-118">Select any of the items in the first configuration group.</span></span>  
5. <span data-ttu-id="7d92e-119">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="7d92e-119">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="7d92e-120">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7d92e-120">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="7d92e-121">Atlasiet jebkuru elementu no otrās konfigurācijas grupas.</span><span class="sxs-lookup"><span data-stu-id="7d92e-121">Select any item from the second configuration group.</span></span>  
7. <span data-ttu-id="7d92e-122">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="7d92e-122">Click OK.</span></span>
8. <span data-ttu-id="7d92e-123">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="7d92e-123">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="7d92e-124">Laukā Konfigurācija ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7d92e-124">In the Configuration field, type a value.</span></span>
    * <span data-ttu-id="7d92e-125">Ievadiet konfigurācijas nosaukumu, kas ļaus ērti identificēt šo konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="7d92e-125">Enter a configuration name that will make it easy to identify the configuration.</span></span>  
10. <span data-ttu-id="7d92e-126">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="7d92e-126">In the Description field, type a value.</span></span>
    * <span data-ttu-id="7d92e-127">Ievadiet konfigurācijas aprakstu, lai paskaidrotu, ko tā satur.</span><span class="sxs-lookup"><span data-stu-id="7d92e-127">Enter a description of the configuration to explain what it contains.</span></span>  
11. <span data-ttu-id="7d92e-128">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="7d92e-128">Click OK.</span></span>

