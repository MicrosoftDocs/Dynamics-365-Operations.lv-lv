---
title: Preces partijas atribūtu izveide
description: Šajā procedūrā tiek parādīts, kā izveidot partijas atribūtu, piešķirt noklusējuma vērtību diapazonus un iekļaut atribūtu grupā.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8924eedfbb635ca04aa167d7f6c44872fef496fd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432785"
---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="ea97c-103">Preces partijas atribūtu izveide</span><span class="sxs-lookup"><span data-stu-id="ea97c-103">Create batch attributes for a product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ea97c-104">Šajā procedūrā tiek parādīts, kā izveidot partijas atribūtu, piešķirt noklusējuma vērtību diapazonus un iekļaut atribūtu grupā.</span><span class="sxs-lookup"><span data-stu-id="ea97c-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="ea97c-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USP2 uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="ea97c-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="ea97c-106">Pārejiet uz sadaļu Krājumu pārvaldība > Iestatījumi > Partija > Partijas atribūti.</span><span class="sxs-lookup"><span data-stu-id="ea97c-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="ea97c-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="ea97c-107">Click New.</span></span>
3. <span data-ttu-id="ea97c-108">Laukā Atribūts ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ea97c-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="ea97c-109">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ea97c-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ea97c-110">Laukā Atribūta tips atlasiet "Daļskaitlis".</span><span class="sxs-lookup"><span data-stu-id="ea97c-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="ea97c-111">Daļskaitļa veids šajā procedūrā tiek izmantots, lai iespējotu decimāldaļskaitļu vērtības.</span><span class="sxs-lookup"><span data-stu-id="ea97c-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="ea97c-112">Var atlasīt citus atribūtu tipus.</span><span class="sxs-lookup"><span data-stu-id="ea97c-112">You can select other attribute types.</span></span> <span data-ttu-id="ea97c-113">Ja atlasāt tipu Uzskaitījums, vērtības uzskaitījuma sarakstā ir jāievada pirms laukā Mērķis var ievadīt vērtību.</span><span class="sxs-lookup"><span data-stu-id="ea97c-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="ea97c-114">Laukā Minimums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="ea97c-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="ea97c-115">Laukā Maksimums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="ea97c-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="ea97c-116">Laukā Solis ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="ea97c-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="ea97c-117">Laukā Mērķis ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ea97c-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="ea97c-118">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ea97c-118">Click Save.</span></span>
11. <span data-ttu-id="ea97c-119">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ea97c-119">Close the page.</span></span>
12. <span data-ttu-id="ea97c-120">Pārejiet uz sadaļu Krājumu pārvaldība > Iestatījumi > Partija > Partijas atribūta grupas.</span><span class="sxs-lookup"><span data-stu-id="ea97c-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="ea97c-121">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="ea97c-121">Click New.</span></span>
14. <span data-ttu-id="ea97c-122">Laukā Atribūtu grupa ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ea97c-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="ea97c-123">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ea97c-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="ea97c-124">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ea97c-124">Click Save.</span></span>
17. <span data-ttu-id="ea97c-125">Noklikšķiniet uz Grupas atribūti.</span><span class="sxs-lookup"><span data-stu-id="ea97c-125">Click Group attributes.</span></span>
18. <span data-ttu-id="ea97c-126">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="ea97c-126">Click New.</span></span>
19. <span data-ttu-id="ea97c-127">Laukā Atribūts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="ea97c-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="ea97c-128">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="ea97c-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="ea97c-129">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="ea97c-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ea97c-130">Atribūtu var iekļaut jebkurā no grupām.</span><span class="sxs-lookup"><span data-stu-id="ea97c-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="ea97c-131">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ea97c-131">Click Save.</span></span>
23. <span data-ttu-id="ea97c-132">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ea97c-132">Close the page.</span></span>

