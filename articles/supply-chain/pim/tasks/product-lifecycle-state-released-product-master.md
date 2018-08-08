--- 
title: "Preces dzīves cikla stāvokļa piešķiršana izlaistam preces šablonam"
description: "Šajā procedūrā ir parādīts, kā piešķirt preces dzīves cikla stāvokli izlaistas preces šablonam un tās variantiem."
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: dd9d40bb331b9e024617c8be55330dfce8ba1cc6
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a><span data-ttu-id="273df-103">Preces dzīves cikla stāvokļa piešķiršana izlaistam preces šablonam</span><span class="sxs-lookup"><span data-stu-id="273df-103">Assign a product lifecycle state to a released product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="273df-104">Šajā procedūrā ir parādīts, kā piešķirt preces dzīves cikla stāvokli izlaistas preces šablonam un tās variantiem.</span><span class="sxs-lookup"><span data-stu-id="273df-104">This procedure shows how to assign a product lifecycle state to a released product master and its variants.</span></span> <span data-ttu-id="273df-105">Priekšnosacījums: pirms šī uzdevuma ceļveža atskaņošanas nepieciešams atskaņot uzdevumu ceļvedi “Jauna preces dzīves cikla stāvokļa izveidošana", lai pārliecinātos, ka ir izveidots vismaz viens preces dzīves cikla stāvoklis.</span><span class="sxs-lookup"><span data-stu-id="273df-105">Prerequisite: You need to play the task guide "Create a new product lifecycle state" first to make sure that you have at least one product lifecycle state created before you can play this task guide.</span></span>


## <a name="find-a-released-product-master"></a><span data-ttu-id="273df-106">Izlaista preces šablona atrašana</span><span class="sxs-lookup"><span data-stu-id="273df-106">Find a released product master</span></span>
1. <span data-ttu-id="273df-107">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="273df-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="273df-108">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="273df-108">In the list, find and select the desired record.</span></span>

> [!NOTE]
> <span data-ttu-id="273df-109">Preces šablonam preces apakštips ir Preces šablons.</span><span class="sxs-lookup"><span data-stu-id="273df-109">A product master has the Product subtype Product master.</span></span>  

## <a name="update-the-lifecycle-state"></a><span data-ttu-id="273df-110">Dzīves cikla stāvokļa atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="273df-110">Update the lifecycle state</span></span>
1. <span data-ttu-id="273df-111">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="273df-111">Click Edit.</span></span>
2. <span data-ttu-id="273df-112">Laukā Preces dzīves cikla stāvoklis ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="273df-112">In the Product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="273df-113">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="273df-113">Click Save.</span></span>
4. <span data-ttu-id="273df-114">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="273df-114">Click Yes.</span></span>

> [!NOTE]
> <span data-ttu-id="273df-115">Atlasot Jā, visi saistītie izlaistās preces varianti, kuriem ir tāds pats sākotnējais stāvoklis kā izlaistās preces šablonam, arī tiek atjaunināti uz jauno preces dzīves cikla stāvokli.</span><span class="sxs-lookup"><span data-stu-id="273df-115">If Yes is selected, all the related released product variants that have the same original status as the released product master are also updated to the new product lifecycle state.</span></span> <span data-ttu-id="273df-116">Atlasot Nē, visiem variantiem tiek saglabāts pašreizējais stāvoklis.</span><span class="sxs-lookup"><span data-stu-id="273df-116">If No is selected, all variants keep their actual state.</span></span> <span data-ttu-id="273df-117">Varianti, kuriem ir atšķirīgs preces dzīves cikla stāvoklis no izlaistās preces šablona, netiek atjaunināti.</span><span class="sxs-lookup"><span data-stu-id="273df-117">Variants that have a different product lifecycle state from the released product master are not updated.</span></span>  

## <a name="verify-the-lifecycle-state-of-the-variants"></a><span data-ttu-id="273df-118">Variantu dzīves cikla stāvokļa pārbaude</span><span class="sxs-lookup"><span data-stu-id="273df-118">Verify the lifecycle state of the variants</span></span>
1. <span data-ttu-id="273df-119">Noklikšķiniet uz Izlaisto preču varianti.</span><span class="sxs-lookup"><span data-stu-id="273df-119">Click Released product variants.</span></span>

> [!NOTE]
> <span data-ttu-id="273df-120">Ņemiet vērā, ka visi varianti pārmanto atlasīto dzīves cikla stāvokli no izlaistās preces šablona.</span><span class="sxs-lookup"><span data-stu-id="273df-120">Note that all variants have inherited the selected lifecycle state from the released product master.</span></span>  

2. <span data-ttu-id="273df-121">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="273df-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="273df-122">Laukā Preces dzīves cikla stāvoklis ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="273df-122">In the Product lifecycle state field, enter or select a value.</span></span>


