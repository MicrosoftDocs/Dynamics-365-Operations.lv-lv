---
title: Preces partijas atribūtu izveide
description: Šajā procedūrā tiek parādīts, kā izveidot partijas atribūtu, piešķirt noklusējuma vērtību diapazonus un iekļaut atribūtu grupā.
author: ShylaThompson
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PdsBatchAttrib
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5deb35028ee499633fb6b0bb5155df2fd91e643a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820110"
---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="96eef-103">Preces partijas atribūtu izveide</span><span class="sxs-lookup"><span data-stu-id="96eef-103">Create batch attributes for a product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="96eef-104">Šajā procedūrā tiek parādīts, kā izveidot partijas atribūtu, piešķirt noklusējuma vērtību diapazonus un iekļaut atribūtu grupā.</span><span class="sxs-lookup"><span data-stu-id="96eef-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="96eef-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USP2 uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="96eef-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="96eef-106">Pārejiet uz sadaļu Krājumu pārvaldība > Iestatījumi > Partija > Partijas atribūti.</span><span class="sxs-lookup"><span data-stu-id="96eef-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="96eef-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="96eef-107">Click New.</span></span>
3. <span data-ttu-id="96eef-108">Laukā Atribūts ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="96eef-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="96eef-109">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="96eef-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="96eef-110">Laukā Atribūta tips atlasiet "Daļskaitlis".</span><span class="sxs-lookup"><span data-stu-id="96eef-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="96eef-111">Daļskaitļa veids šajā procedūrā tiek izmantots, lai iespējotu decimāldaļskaitļu vērtības.</span><span class="sxs-lookup"><span data-stu-id="96eef-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="96eef-112">Var atlasīt citus atribūtu tipus.</span><span class="sxs-lookup"><span data-stu-id="96eef-112">You can select other attribute types.</span></span> <span data-ttu-id="96eef-113">Ja atlasāt tipu Uzskaitījums, vērtības uzskaitījuma sarakstā ir jāievada pirms laukā Mērķis var ievadīt vērtību.</span><span class="sxs-lookup"><span data-stu-id="96eef-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="96eef-114">Laukā Minimums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="96eef-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="96eef-115">Laukā Maksimums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="96eef-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="96eef-116">Laukā Solis ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="96eef-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="96eef-117">Laukā Mērķis ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="96eef-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="96eef-118">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="96eef-118">Click Save.</span></span>
11. <span data-ttu-id="96eef-119">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="96eef-119">Close the page.</span></span>
12. <span data-ttu-id="96eef-120">Pārejiet uz sadaļu Krājumu pārvaldība > Iestatījumi > Partija > Partijas atribūta grupas.</span><span class="sxs-lookup"><span data-stu-id="96eef-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="96eef-121">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="96eef-121">Click New.</span></span>
14. <span data-ttu-id="96eef-122">Laukā Atribūtu grupa ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="96eef-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="96eef-123">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="96eef-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="96eef-124">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="96eef-124">Click Save.</span></span>
17. <span data-ttu-id="96eef-125">Noklikšķiniet uz Grupas atribūti.</span><span class="sxs-lookup"><span data-stu-id="96eef-125">Click Group attributes.</span></span>
18. <span data-ttu-id="96eef-126">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="96eef-126">Click New.</span></span>
19. <span data-ttu-id="96eef-127">Laukā Atribūts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="96eef-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="96eef-128">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="96eef-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="96eef-129">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="96eef-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="96eef-130">Atribūtu var iekļaut jebkurā no grupām.</span><span class="sxs-lookup"><span data-stu-id="96eef-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="96eef-131">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="96eef-131">Click Save.</span></span>
23. <span data-ttu-id="96eef-132">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="96eef-132">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]