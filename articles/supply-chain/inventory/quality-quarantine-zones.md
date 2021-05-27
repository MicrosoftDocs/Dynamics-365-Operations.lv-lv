---
title: Karantīnas zonas neatbilstībai
description: Šajā tēmā aprakstīts, kā izveidot un izmantot karantīnas zonas neatbilstībām.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80f4b9dfc7882af4570bf1908784b8d114396402
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021808"
---
# <a name="quarantine-zones-for-nonconformances"></a><span data-ttu-id="43a75-103">Karantīnas zonas neatbilstībai</span><span class="sxs-lookup"><span data-stu-id="43a75-103">Quarantine zones for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43a75-104">Šajā tēmā aprakstīts, kā izveidot un izmantot karantīnas zonas neatbilstībām.</span><span class="sxs-lookup"><span data-stu-id="43a75-104">This topic describes how to create and use quarantine zones for nonconformances.</span></span>

<span data-ttu-id="43a75-105">Izmantojiet lapu **Karantīnas zonas**, lai definētu zonas, ko var piešķirt neatbilstībām.</span><span class="sxs-lookup"><span data-stu-id="43a75-105">You use the **Quarantine zones** page to define zones that can be assigned to nonconformances.</span></span> <span data-ttu-id="43a75-106">Kad jūs izveidojat neatbilstību, jūs variet iestatīt laukus **Karantīnas zona** un **Karantīnas veids** cilnē **Vispārīgi** lapā **Neatbilstības**.</span><span class="sxs-lookup"><span data-stu-id="43a75-106">When you create a nonconformance, you can set the **Quarantine zone** and **Quarantine type** fields on the **General** tab of the **Non conformances** page.</span></span> <span data-ttu-id="43a75-107">Lauks **Karantīnas zona** parasti norāda apgabalu vai vietu, kur atrodas krājums.</span><span class="sxs-lookup"><span data-stu-id="43a75-107">The **Quarantine zone** field typically indicates the area or location where the item is located.</span></span> <span data-ttu-id="43a75-108">Lauks **Karantīnas veids** nosaka, vai krājums ir *Ierobežotas lietošanas* vai *Nav derīgs*.</span><span class="sxs-lookup"><span data-stu-id="43a75-108">The **Quarantine type** field defines the item as either *Restricted usage* or *Unusable*.</span></span>

<span data-ttu-id="43a75-109">Kad tiek drukāta neatbilstība vai labojumu pārskats par neatbilstību, varat apskatīt karantīnas zonu, kurā atrodas krājums.</span><span class="sxs-lookup"><span data-stu-id="43a75-109">When you print a nonconformance or corrections report for a nonconformance, you can view the quarantine zone where the item is located.</span></span>

<span data-ttu-id="43a75-110">Varat arī drukāt neatbilstības tagu neatbilstībai.</span><span class="sxs-lookup"><span data-stu-id="43a75-110">You can also print a nonconformance tag for a nonconformance.</span></span> <span data-ttu-id="43a75-111">Šis pārskats rāda piešķirto karantīnas zonu un informāciju par lietojumu, lai sniegtu norādījumus par to, kā jārīkojas ar bojātu materiālu.</span><span class="sxs-lookup"><span data-stu-id="43a75-111">This report shows the assigned quarantine zone and information about usage to provide guidance about how defective material should be handled.</span></span> <span data-ttu-id="43a75-112">Karantīnas zonas var atbilst krājumu vietām vai operāciju resursiem.</span><span class="sxs-lookup"><span data-stu-id="43a75-112">The quarantine zones might correspond to inventory locations or operations resources.</span></span>

## <a name="examples-of-quarantine-zones"></a><span data-ttu-id="43a75-113">Karantīnas zonu piemēri</span><span class="sxs-lookup"><span data-stu-id="43a75-113">Examples of quarantine zones</span></span>

### <a name="example-1"></a><span data-ttu-id="43a75-114">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="43a75-114">Example 1</span></span>

<span data-ttu-id="43a75-115">Jūs strādājat elektronikas ražošanas uzņēmumā, kas ražo un izplata televizorus, skaļruņus un multivides atskaņotājus.</span><span class="sxs-lookup"><span data-stu-id="43a75-115">You work at an electronics manufacturing company that produces and distributes televisions, speakers, and media players.</span></span> <span data-ttu-id="43a75-116">Šajā gadījumā karantīnas zonu var konfigurēt, lai attēlotu katru produkta veidu.</span><span class="sxs-lookup"><span data-stu-id="43a75-116">In this case, you can configure a quarantine zone to represent each type of product.</span></span>

### <a name="example-2"></a><span data-ttu-id="43a75-117">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="43a75-117">Example 2</span></span>

<span data-ttu-id="43a75-118">Trīs nodalījumi un divi statīvi tiek izmantoti, lai uzglabātu neatbilstošas preces.</span><span class="sxs-lookup"><span data-stu-id="43a75-118">Three bins and two racks are used to store items that are nonconforming.</span></span> <span data-ttu-id="43a75-119">Šajā gadījumā var konfigurēt piecas karantīnas zonas – pa vienai katram nodalījumam un katram statīvam.</span><span class="sxs-lookup"><span data-stu-id="43a75-119">In this case, you can configure five quarantine zones, one for each bin and each rack.</span></span>

## <a name="create-a-quarantine-zone"></a><span data-ttu-id="43a75-120">Izveidojiet karantīnas zonu</span><span class="sxs-lookup"><span data-stu-id="43a75-120">Create a quarantine zone</span></span>

1. <span data-ttu-id="43a75-121">Dodieties uz **Krājumu vadība \> Iestatīšana \> Kvalitātes pārvaldība \> Karantīnas zonas**.</span><span class="sxs-lookup"><span data-stu-id="43a75-121">Go to **Inventory management \> Setup \> Quality management \> Quarantine zones**.</span></span>
1. <span data-ttu-id="43a75-122">Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="43a75-122">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="43a75-123">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="43a75-123">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="43a75-124">**Karantīnas zona** – ievadiet karantīnas zonas unikālo ID vai nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="43a75-124">**Quarantine zone** – Enter a unique ID or name for the quarantine zone.</span></span>
    - <span data-ttu-id="43a75-125">**Apraksts** — ievadiet karantīnas zonas detālizēto aprakstu.</span><span class="sxs-lookup"><span data-stu-id="43a75-125">**Description** – Enter a detailed description of the quarantine zone.</span></span>

1. <span data-ttu-id="43a75-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="43a75-126">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="43a75-127">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="43a75-127">Additional resources</span></span>

- [<span data-ttu-id="43a75-128">Kvalitātes pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="43a75-128">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="43a75-129">Iespējot kvalitātes un neatbilstības pārvaldību</span><span class="sxs-lookup"><span data-stu-id="43a75-129">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="43a75-130">Par neatbilstību apstiprināšanu atbildīgie darbinieki</span><span class="sxs-lookup"><span data-stu-id="43a75-130">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="43a75-131">Neatbilstību problēmu tipi</span><span class="sxs-lookup"><span data-stu-id="43a75-131">Problem types for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="43a75-132">Neatbilstību diagnostikas tipi</span><span class="sxs-lookup"><span data-stu-id="43a75-132">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="43a75-133">Kvalitātes maksa par neatbilstībām</span><span class="sxs-lookup"><span data-stu-id="43a75-133">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="43a75-134">Operācijas neatbilstībai</span><span class="sxs-lookup"><span data-stu-id="43a75-134">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="43a75-135">Kvalitātes pārvaldība noliktavas procesiem</span><span class="sxs-lookup"><span data-stu-id="43a75-135">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
