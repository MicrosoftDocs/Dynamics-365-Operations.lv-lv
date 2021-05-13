---
title: Preces konfigurācijas modeļa apstiprināšana
description: Šīs procedūras veikšanai ir nepieciešams, lai būtu pieejams vismaz preces konfigurācijas modelis.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductModelVersion, PCApproveProductModelVersion, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c945756997b0580ac7ffb19261f9184e53a1c10
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920511"
---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="b1dec-103">Preces konfigurācijas modeļa apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="b1dec-103">Approve a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b1dec-104">Šīs procedūras veikšanai ir nepieciešams, lai būtu pieejams vismaz preces konfigurācijas modelis.</span><span class="sxs-lookup"><span data-stu-id="b1dec-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="b1dec-105">Šajā procedūrā tiek izmantots augstas kvalitātes skaļruņu modelis demonstrācijas datu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="b1dec-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="b1dec-106">Ņemiet vērā, ka šis modelis jau ir apstiprināts, bet procedūrā ir aprakstīts viss process.</span><span class="sxs-lookup"><span data-stu-id="b1dec-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="b1dec-107">Dodieties uz **Preču informācijas pārvaldība \> Preces \> Preču konfigurācijas modeļi**.</span><span class="sxs-lookup"><span data-stu-id="b1dec-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="b1dec-108">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b1dec-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b1dec-109">Atlasiet augstas kvalitātes skaļruņa modeli šai procedūrai.</span><span class="sxs-lookup"><span data-stu-id="b1dec-109">Select the High end speaker model for this procedure.</span></span>  
1. <span data-ttu-id="b1dec-110">Atlasīt **Versijas**.</span><span class="sxs-lookup"><span data-stu-id="b1dec-110">Select **Versions**.</span></span>
1. <span data-ttu-id="b1dec-111">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="b1dec-111">Select **New**.</span></span>
1. <span data-ttu-id="b1dec-112">Laukā **Preces numurs** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="b1dec-112">In the **Product number** field, enter or select a value.</span></span>
    * <span data-ttu-id="b1dec-113">Atsauce uz preci attiecas uz preces konfigurācijas modeļa versiju.</span><span class="sxs-lookup"><span data-stu-id="b1dec-113">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="b1dec-114">Šajā sarakstā tiks parādīti tikai preču šabloni, kuriem ir konfigurācijas atbilstoši ierobežojumam tehnoloģija.</span><span class="sxs-lookup"><span data-stu-id="b1dec-114">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
1. <span data-ttu-id="b1dec-115">Ievadiet datumu laukā **No datuma**.</span><span class="sxs-lookup"><span data-stu-id="b1dec-115">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="b1dec-116">Atlasiet, kad būs pieejama preču modeļa versija.</span><span class="sxs-lookup"><span data-stu-id="b1dec-116">Select when the product model version will be available.</span></span>  
1. <span data-ttu-id="b1dec-117">Ievadiet datumu laukā **Līdz datumam**.</span><span class="sxs-lookup"><span data-stu-id="b1dec-117">In the **To date** field, enter a date.</span></span>
    * <span data-ttu-id="b1dec-118">Atlasiet beigu datumu, kad beigsies šīs preču modeļa versijas derīguma termiņš, vai atlasiet vienumu Nekad.</span><span class="sxs-lookup"><span data-stu-id="b1dec-118">Select an end date when this product model version will expire, or select Never.</span></span>  
1. <span data-ttu-id="b1dec-119">Atlasiet **Apstiprināt**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b1dec-119">Select **Approve** to open the drop dialog.</span></span>
1. <span data-ttu-id="b1dec-120">Laukā **Apstiprināt pēc** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b1dec-120">In the **Approved by** field, enter or select a value.</span></span>
    * <span data-ttu-id="b1dec-121">Atlasiet personu, kura ir atbildīga par preču modeļu apstiprināšanu izmantošanai operācijās.</span><span class="sxs-lookup"><span data-stu-id="b1dec-121">Select the person who is responsible for approving product models for use in operations.</span></span>  
1. <span data-ttu-id="b1dec-122">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b1dec-122">Select **OK**.</span></span>
1. <span data-ttu-id="b1dec-123">Laukā **Cenu noteikšanas metode** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="b1dec-123">In the **Pricing method** field, select an option.</span></span>
    * <span data-ttu-id="b1dec-124">Aktivizējiet preču modeļa versiju.</span><span class="sxs-lookup"><span data-stu-id="b1dec-124">Activate the product model version.</span></span> <span data-ttu-id="b1dec-125">Vienam preču modelim vienlaicīgi var būt aktīva tikai viena prece.</span><span class="sxs-lookup"><span data-stu-id="b1dec-125">It is only possible to have one product active for one product model at a time.</span></span>  
1. <span data-ttu-id="b1dec-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b1dec-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]