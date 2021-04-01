---
title: Preces dzīves cikla stāvokļa piešķiršana izlaistam preces šablonam
description: Šajā procedūrā ir parādīts, kā piešķirt preces dzīves cikla stāvokli izlaistas preces šablonam un tās variantiem.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a5d7f6532e3c0b61fcc5758f383257d4a9a09b5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226741"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a><span data-ttu-id="481de-103">Preces dzīves cikla stāvokļa piešķiršana izlaistam preces šablonam</span><span class="sxs-lookup"><span data-stu-id="481de-103">Assign a product lifecycle state to a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="481de-104">Šajā procedūrā ir parādīts, kā piešķirt preces dzīves cikla stāvokli izlaistas preces šablonam un tās variantiem.</span><span class="sxs-lookup"><span data-stu-id="481de-104">This procedure shows how to assign a product lifecycle state to a released product master and its variants.</span></span> <span data-ttu-id="481de-105">Priekšnosacījums: pirms šī uzdevuma ceļveža atskaņošanas nepieciešams atskaņot uzdevumu ceļvedi “Jauna preces dzīves cikla stāvokļa izveidošana", lai pārliecinātos, ka ir izveidots vismaz viens preces dzīves cikla stāvoklis.</span><span class="sxs-lookup"><span data-stu-id="481de-105">Prerequisite: You need to play the task guide "Create a new product lifecycle state" first to make sure that you have at least one product lifecycle state created before you can play this task guide.</span></span>


## <a name="find-a-released-product-master"></a><span data-ttu-id="481de-106">Izlaista preces šablona atrašana</span><span class="sxs-lookup"><span data-stu-id="481de-106">Find a released product master</span></span>
1. <span data-ttu-id="481de-107">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="481de-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="481de-108">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="481de-108">In the list, find and select the desired record.</span></span>

> [!NOTE]
> <span data-ttu-id="481de-109">Preces šablonam preces apakštips ir Preces šablons.</span><span class="sxs-lookup"><span data-stu-id="481de-109">A product master has the Product subtype Product master.</span></span>  

## <a name="update-the-lifecycle-state"></a><span data-ttu-id="481de-110">Dzīves cikla stāvokļa atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="481de-110">Update the lifecycle state</span></span>
1. <span data-ttu-id="481de-111">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="481de-111">Click Edit.</span></span>
2. <span data-ttu-id="481de-112">Laukā Preces dzīves cikla stāvoklis ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="481de-112">In the Product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="481de-113">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="481de-113">Click Save.</span></span>
4. <span data-ttu-id="481de-114">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="481de-114">Click Yes.</span></span>

> [!NOTE]
> <span data-ttu-id="481de-115">Atlasot Jā, visi saistītie izlaistās preces varianti, kuriem ir tāds pats sākotnējais stāvoklis kā izlaistās preces šablonam, arī tiek atjaunināti uz jauno preces dzīves cikla stāvokli.</span><span class="sxs-lookup"><span data-stu-id="481de-115">If Yes is selected, all the related released product variants that have the same original status as the released product master are also updated to the new product lifecycle state.</span></span> <span data-ttu-id="481de-116">Atlasot Nē, visiem variantiem tiek saglabāts pašreizējais stāvoklis.</span><span class="sxs-lookup"><span data-stu-id="481de-116">If No is selected, all variants keep their actual state.</span></span> <span data-ttu-id="481de-117">Varianti, kuriem ir atšķirīgs preces dzīves cikla stāvoklis no izlaistās preces šablona, netiek atjaunināti.</span><span class="sxs-lookup"><span data-stu-id="481de-117">Variants that have a different product lifecycle state from the released product master are not updated.</span></span>  

## <a name="verify-the-lifecycle-state-of-the-variants"></a><span data-ttu-id="481de-118">Variantu dzīves cikla stāvokļa pārbaude</span><span class="sxs-lookup"><span data-stu-id="481de-118">Verify the lifecycle state of the variants</span></span>
1. <span data-ttu-id="481de-119">Noklikšķiniet uz Izlaisto preču varianti.</span><span class="sxs-lookup"><span data-stu-id="481de-119">Click Released product variants.</span></span>

> [!NOTE]
> <span data-ttu-id="481de-120">Ņemiet vērā, ka visi varianti pārmanto atlasīto dzīves cikla stāvokli no izlaistās preces šablona.</span><span class="sxs-lookup"><span data-stu-id="481de-120">Note that all variants have inherited the selected lifecycle state from the released product master.</span></span>  

2. <span data-ttu-id="481de-121">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="481de-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="481de-122">Laukā Preces dzīves cikla stāvoklis ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="481de-122">In the Product lifecycle state field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]