---
title: Preces konfigurācijas modeļa apstiprināšana
description: Šīs procedūras veikšanai ir nepieciešams, lai būtu pieejams vismaz preces konfigurācijas modelis.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductModelVersion, PCApproveProductModelVersion, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aa0027382e08a23c4dc1e782773a20db441d4f27
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208367"
---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="65e39-103">Preces konfigurācijas modeļa apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="65e39-103">Approve a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="65e39-104">Šīs procedūras veikšanai ir nepieciešams, lai būtu pieejams vismaz preces konfigurācijas modelis.</span><span class="sxs-lookup"><span data-stu-id="65e39-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="65e39-105">Šajā procedūrā tiek izmantots augstas kvalitātes skaļruņu modelis demonstrācijas datu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="65e39-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="65e39-106">Ņemiet vērā, ka šis modelis jau ir apstiprināts, bet procedūrā ir aprakstīts viss process.</span><span class="sxs-lookup"><span data-stu-id="65e39-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="65e39-107">Noklikšķiniet uz Preces varianta modeļa definīcija.</span><span class="sxs-lookup"><span data-stu-id="65e39-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="65e39-108">Noklikšķiniet uz Preču konfigurācijas modeļi.</span><span class="sxs-lookup"><span data-stu-id="65e39-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="65e39-109">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="65e39-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="65e39-110">Atlasiet augstas kvalitātes skaļruņa modeli šai procedūrai.</span><span class="sxs-lookup"><span data-stu-id="65e39-110">Select the High end speaker model for this procedure.</span></span>  
4. <span data-ttu-id="65e39-111">Noklikšķiniet uz Versijas.</span><span class="sxs-lookup"><span data-stu-id="65e39-111">Click Versions.</span></span>
5. <span data-ttu-id="65e39-112">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="65e39-112">Click New.</span></span>
6. <span data-ttu-id="65e39-113">Laukā Preces numurs ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="65e39-113">In the Product number field, enter or select a value.</span></span>
    * <span data-ttu-id="65e39-114">Atsauce uz preci attiecas uz preces konfigurācijas modeļa versiju.</span><span class="sxs-lookup"><span data-stu-id="65e39-114">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="65e39-115">Šajā sarakstā tiks parādīti tikai preču šabloni, kuriem ir konfigurācijas atbilstoši ierobežojumam tehnoloģija.</span><span class="sxs-lookup"><span data-stu-id="65e39-115">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
7. <span data-ttu-id="65e39-116">Ievadiet datumu laukā No datuma.</span><span class="sxs-lookup"><span data-stu-id="65e39-116">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="65e39-117">Atlasiet, kad būs pieejama preču modeļa versija.</span><span class="sxs-lookup"><span data-stu-id="65e39-117">Select when the product model version will be available.</span></span>  
8. <span data-ttu-id="65e39-118">Laukā Līdz datumam ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="65e39-118">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="65e39-119">Atlasiet beigu datumu, kad beigsies šīs preču modeļa versijas derīguma termiņš, vai atlasiet vienumu Nekad.</span><span class="sxs-lookup"><span data-stu-id="65e39-119">Select an end date when this product model version will expire, or select Never.</span></span>  
9. <span data-ttu-id="65e39-120">Noklikšķiniet uz Apstiprināt, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="65e39-120">Click Approve to open the drop dialog.</span></span>
10. <span data-ttu-id="65e39-121">Laukā Apstiprināja ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="65e39-121">In the Approved by field, enter or select a value.</span></span>
    * <span data-ttu-id="65e39-122">Atlasiet personu, kura ir atbildīga par preču modeļu apstiprināšanu izmantošanai operācijās.</span><span class="sxs-lookup"><span data-stu-id="65e39-122">Select the person who is responsible for approving product models for use in operations.</span></span>  
11. <span data-ttu-id="65e39-123">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="65e39-123">Click OK.</span></span>
12. <span data-ttu-id="65e39-124">Laukā Cenu noteikšanas metode atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="65e39-124">In the Pricing method field, select an option.</span></span>
    * <span data-ttu-id="65e39-125">Aktivizējiet preču modeļa versiju.</span><span class="sxs-lookup"><span data-stu-id="65e39-125">Activate the product model version.</span></span> <span data-ttu-id="65e39-126">Vienam preču modelim vienlaicīgi var būt aktīva tikai viena prece.</span><span class="sxs-lookup"><span data-stu-id="65e39-126">It is only possible to have one product active for one product model at a time.</span></span>  
13. <span data-ttu-id="65e39-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="65e39-127">Close the page.</span></span>

