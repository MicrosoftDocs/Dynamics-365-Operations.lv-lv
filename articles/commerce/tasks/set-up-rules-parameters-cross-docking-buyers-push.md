---
title: " Kārtulu un parametru iestatīšana pārkraušanai sadales centrā un sagādes sadalē"
description: Šī procedūra parāda, kā izveidot papildināšanas kārtulas.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailReplenishmentRuleTable, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ecc3e1ce842e8d3b693b5e81ed665e9f3c00bfb5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023265"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a><span data-ttu-id="d735a-103"> Kārtulu un parametru iestatīšana pārkraušanai sadales centrā un sagādes sadalē</span><span class="sxs-lookup"><span data-stu-id="d735a-103">Set up rules and parameters for cross docking and buyer's push</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="d735a-104">Šī procedūra parāda, kā izveidot papildināšanas kārtulas.</span><span class="sxs-lookup"><span data-stu-id="d735a-104">This procedure demonstrates the steps to create Replenishment rules.</span></span> <span data-ttu-id="d735a-105">Papildināšanas kārtulas var lietot, lai kontrolētu to, kā preces tiek sadalītas veikalos, izmantojot pārkraušanu sadales centrā un sagādes sadali.</span><span class="sxs-lookup"><span data-stu-id="d735a-105">Replenishment rules can be used to control how products are distributed to stores when using Cross-docking and Buyer´s push.</span></span> <span data-ttu-id="d735a-106">Papildināšanas kārtulas var iestatīt veikaliem vai veikalu grupām.</span><span class="sxs-lookup"><span data-stu-id="d735a-106">Replenishment rules can be set up for stores or store groups.</span></span> <span data-ttu-id="d735a-107">Katrā kārtulas rindā definētā svara vērtība kontrolēs to, kā preču daudzumi tiks sadalīti starp veikaliem, ja pārkraušanai sadales centrā vai sagādes sadalēm kā sadales metode tiks izmantotas papildināšanas kārtulas.</span><span class="sxs-lookup"><span data-stu-id="d735a-107">The weight defined for each line in a rule will control how the quantities of products will get distributed between the stores when using Replenishment rules as the distribution method in Cross-docking or Buyer´s push.</span></span> <span data-ttu-id="d735a-108">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="d735a-108">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="d735a-109">Dodieties uz cilni Papildināšanas kārtulas.</span><span class="sxs-lookup"><span data-stu-id="d735a-109">Go to Replenishment rules.</span></span>
2. <span data-ttu-id="d735a-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d735a-110">Click New.</span></span>
3. <span data-ttu-id="d735a-111">Laukā Papildināšanas kārtula ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d735a-111">In the Replenishment rule field, type a value.</span></span>
4. <span data-ttu-id="d735a-112">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d735a-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d735a-113">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d735a-113">Click Save.</span></span>
6. <span data-ttu-id="d735a-114">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d735a-114">Click Add.</span></span>
7. <span data-ttu-id="d735a-115">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="d735a-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d735a-116">Varat izvēlēties veidu Papildināšanas hierarhiju vai Kanāls.</span><span class="sxs-lookup"><span data-stu-id="d735a-116">You can choose Replenishment hierarchy or Channel for the type.</span></span> <span data-ttu-id="d735a-117">Vērtība kontrolē, vai atlase laukā Nosaukums būs kanālu vai noteikta kanāla hierarhija.</span><span class="sxs-lookup"><span data-stu-id="d735a-117">The value controls whether the selection in Name will be a hierarchy of channels or a specific channel.</span></span>  <span data-ttu-id="d735a-118">Šajā piemērā atstājiet to iestatītu kā Papildināšanas hierarhija.</span><span class="sxs-lookup"><span data-stu-id="d735a-118">For this example, leave it set as Replenishment hierarchy.</span></span>  
8. <span data-ttu-id="d735a-119">Laukā Nosaukums atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d735a-119">In the Name field, select a value.</span></span>
    * <span data-ttu-id="d735a-120">Noklusējuma svara vērtība tiek aizpildīta, izmantojot noliktavā definēto svaru.</span><span class="sxs-lookup"><span data-stu-id="d735a-120">The default weight value is populated from the weight defined on the warehouse.</span></span>  <span data-ttu-id="d735a-121">Šo svara vērtību var izmantot kārtulai Papildināšana, vai arī laukā Svars var ievadīt jaunu svara vērtību.</span><span class="sxs-lookup"><span data-stu-id="d735a-121">This weight can be used for the Replenishment rule or you can enter a new weight in the Weight field.</span></span>  
9. <span data-ttu-id="d735a-122">Laukā Svars ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="d735a-122">In the Weight field, enter a number.</span></span>
10. <span data-ttu-id="d735a-123">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d735a-123">Click Add.</span></span>
11. <span data-ttu-id="d735a-124">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="d735a-124">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="d735a-125">Laukā Veids atlasiet Kanāls.</span><span class="sxs-lookup"><span data-stu-id="d735a-125">In the Type field, select 'Channel'.</span></span>
13. <span data-ttu-id="d735a-126">Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d735a-126">In the Name field, enter or select a value.</span></span>
14. <span data-ttu-id="d735a-127">Laukā Svars ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="d735a-127">In the Weight field, enter a number.</span></span>
15. <span data-ttu-id="d735a-128">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d735a-128">Click Save.</span></span>
