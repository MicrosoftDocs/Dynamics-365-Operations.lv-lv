---
title: Konfigurāciju izveide atbilstoši dimensijām
description: Šajā procedūrā ir parādīts, kā definēt konfigurāciju uz dimensiju balstītai precei.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, EcoResDimensionBasedConfiguration, ConfigChooseFromRoute, ConfigChooseFromGroup, ConfigChoiceApprove
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 584bb558ee0afeaffaeb003e9f1d1b0bca42d19d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920685"
---
# <a name="create-dimension-based-configurations"></a><span data-ttu-id="b82a4-103">Konfigurāciju izveide atbilstoši dimensijām</span><span class="sxs-lookup"><span data-stu-id="b82a4-103">Create dimension-based configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b82a4-104">Šajā procedūrā ir parādīts, kā definēt konfigurāciju uz dimensiju balstītai precei.</span><span class="sxs-lookup"><span data-stu-id="b82a4-104">This procedure shows how to define a configuration for a dimension-based product.</span></span> <span data-ttu-id="b82a4-105">Šī ir pēdējā procedūra šajā sērijā, kurā ir skaidrots, kā veidot kombinācijas konfigurācijai atbilstoši dimensijām.</span><span class="sxs-lookup"><span data-stu-id="b82a4-105">This is the last procedure in the series that explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="b82a4-106">Šīs procedūras izpilde ir atkarīga no datiem, kurus izveidojāt iepriekšējos septiņos ierakstos.</span><span class="sxs-lookup"><span data-stu-id="b82a4-106">The execution of this procedure is dependent on the data created in the previous seven recordings.</span></span> <span data-ttu-id="b82a4-107">USMF ir paraugdatu uzņēmums, kas tiek izmantots šīs procedūras izveidei.</span><span class="sxs-lookup"><span data-stu-id="b82a4-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="find-the-dimension-based-product-master"></a><span data-ttu-id="b82a4-108">Atrast uz dimensiju balstīto preces šablonu</span><span class="sxs-lookup"><span data-stu-id="b82a4-108">Find the dimension-based product master</span></span>

1. <span data-ttu-id="b82a4-109">Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="b82a4-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="b82a4-110">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="b82a4-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b82a4-111">Atlasiet uz dimensijām balstīto preces šablonu, kuru izveidojāt šīs 8 ierakstu procedūras pirmajā ierakstā.</span><span class="sxs-lookup"><span data-stu-id="b82a4-111">Select the dimension-based product master that you created in the first recording in this sequence of 8 recordings.</span></span>  

## <a name="create-configurations"></a><span data-ttu-id="b82a4-112">Konfigurāciju izveide</span><span class="sxs-lookup"><span data-stu-id="b82a4-112">Create configurations</span></span>

1. <span data-ttu-id="b82a4-113">Darbību rūtī **Tehniskais** atlsiet **Uzturēt konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="b82a4-113">On the **Engineering** Action Pane, select **Maintain configurations**.</span></span>
1. <span data-ttu-id="b82a4-114">Atlasiet **Konfigurēt**.</span><span class="sxs-lookup"><span data-stu-id="b82a4-114">Select **Configure**.</span></span>
1. <span data-ttu-id="b82a4-115">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="b82a4-115">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="b82a4-116">Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b82a4-116">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="b82a4-117">Atlasiet jebkuru no elementiem pirmajā konfigurācijas grupā.</span><span class="sxs-lookup"><span data-stu-id="b82a4-117">Select any of the items in the first configuration group.</span></span>  
1. <span data-ttu-id="b82a4-118">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b82a4-118">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="b82a4-119">Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b82a4-119">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="b82a4-120">Atlasiet jebkuru elementu no otrās konfigurācijas grupas.</span><span class="sxs-lookup"><span data-stu-id="b82a4-120">Select any item from the second configuration group.</span></span>  
1. <span data-ttu-id="b82a4-121">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b82a4-121">Select **OK**.</span></span>
1. <span data-ttu-id="b82a4-122">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="b82a4-122">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="b82a4-123">Laukā **Konfigurācija** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b82a4-123">In the **Configuration** field, type a value.</span></span>
    * <span data-ttu-id="b82a4-124">Ievadiet konfigurācijas nosaukumu, kas ļaus ērti identificēt šo konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="b82a4-124">Enter a configuration name that will make it easy to identify the configuration.</span></span>  
1. <span data-ttu-id="b82a4-125">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b82a4-125">In the **Description** field, type a value.</span></span>
    * <span data-ttu-id="b82a4-126">Ievadiet konfigurācijas aprakstu, lai paskaidrotu, ko tā satur.</span><span class="sxs-lookup"><span data-stu-id="b82a4-126">Enter a description of the configuration to explain what it contains.</span></span>  
1. <span data-ttu-id="b82a4-127">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b82a4-127">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]