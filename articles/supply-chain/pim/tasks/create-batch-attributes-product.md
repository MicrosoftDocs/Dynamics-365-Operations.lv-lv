---
title: Preces partijas atribūtu izveide
description: Šajā procedūrā tiek parādīts, kā izveidot partijas atribūtu, piešķirt noklusējuma vērtību diapazonus un iekļaut atribūtu grupā.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d874b6b6e53164c00d9b4656d27b1060f4e3ba06
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934939"
---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="8103a-103">Preces partijas atribūtu izveide</span><span class="sxs-lookup"><span data-stu-id="8103a-103">Create batch attributes for a product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8103a-104">Šajā procedūrā tiek parādīts, kā izveidot partijas atribūtu, piešķirt noklusējuma vērtību diapazonus un iekļaut atribūtu grupā.</span><span class="sxs-lookup"><span data-stu-id="8103a-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="8103a-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USP2 uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="8103a-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="8103a-106">Pārejiet uz sadaļu Krājumu pārvaldība > Iestatījumi > Partija > Partijas atribūti.</span><span class="sxs-lookup"><span data-stu-id="8103a-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="8103a-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="8103a-107">Click New.</span></span>
3. <span data-ttu-id="8103a-108">Laukā Atribūts ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8103a-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="8103a-109">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8103a-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8103a-110">Laukā Atribūta tips atlasiet "Daļskaitlis".</span><span class="sxs-lookup"><span data-stu-id="8103a-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="8103a-111">Daļskaitļa veids šajā procedūrā tiek izmantots, lai iespējotu decimāldaļskaitļu vērtības.</span><span class="sxs-lookup"><span data-stu-id="8103a-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="8103a-112">Var atlasīt citus atribūtu tipus.</span><span class="sxs-lookup"><span data-stu-id="8103a-112">You can select other attribute types.</span></span> <span data-ttu-id="8103a-113">Ja atlasāt tipu Uzskaitījums, vērtības uzskaitījuma sarakstā ir jāievada pirms laukā Mērķis var ievadīt vērtību.</span><span class="sxs-lookup"><span data-stu-id="8103a-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="8103a-114">Laukā Minimums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="8103a-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="8103a-115">Laukā Maksimums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="8103a-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="8103a-116">Laukā Solis ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="8103a-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="8103a-117">Laukā Mērķis ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8103a-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="8103a-118">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8103a-118">Click Save.</span></span>
11. <span data-ttu-id="8103a-119">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="8103a-119">Close the page.</span></span>
12. <span data-ttu-id="8103a-120">Pārejiet uz sadaļu Krājumu pārvaldība > Iestatījumi > Partija > Partijas atribūta grupas.</span><span class="sxs-lookup"><span data-stu-id="8103a-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="8103a-121">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="8103a-121">Click New.</span></span>
14. <span data-ttu-id="8103a-122">Laukā Atribūtu grupa ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8103a-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="8103a-123">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8103a-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="8103a-124">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8103a-124">Click Save.</span></span>
17. <span data-ttu-id="8103a-125">Noklikšķiniet uz Grupas atribūti.</span><span class="sxs-lookup"><span data-stu-id="8103a-125">Click Group attributes.</span></span>
18. <span data-ttu-id="8103a-126">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="8103a-126">Click New.</span></span>
19. <span data-ttu-id="8103a-127">Laukā Atribūts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="8103a-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="8103a-128">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="8103a-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="8103a-129">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="8103a-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8103a-130">Atribūtu var iekļaut jebkurā no grupām.</span><span class="sxs-lookup"><span data-stu-id="8103a-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="8103a-131">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8103a-131">Click Save.</span></span>
23. <span data-ttu-id="8103a-132">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="8103a-132">Close the page.</span></span>

