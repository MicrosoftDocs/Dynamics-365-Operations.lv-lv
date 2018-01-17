--- 
title: Izveidot jaunu preci
description: "Šajā uzdevumā ir aprakstīts, kā izveidot jaunu koplietojamu preci."
author: YuyuScheller
manager: AnnBe
ms.date: 06/08/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 0ea85775e7be86eead716e88ef9d51cae9c007f3
ms.contentlocale: lv-lv
ms.lasthandoff: 01/17/2018

---
# <a name="create-a-new-product"></a><span data-ttu-id="2342b-103">Izveidot jaunu preci</span><span class="sxs-lookup"><span data-stu-id="2342b-103">Create a new product</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2342b-104">Šajā uzdevumā ir aprakstīts, kā izveidot jaunu koplietojamu preci.</span><span class="sxs-lookup"><span data-stu-id="2342b-104">This task shows how to create a new shared product.</span></span> <span data-ttu-id="2342b-105">To parasti veic preču noformētājs.</span><span class="sxs-lookup"><span data-stu-id="2342b-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="2342b-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="2342b-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="2342b-107">Dodieties uz Preču informācijas pārvaldība > Preces > Preces.</span><span class="sxs-lookup"><span data-stu-id="2342b-107">Go to Product information management > Products > Products.</span></span>

## <a name="create-a-product"></a><span data-ttu-id="2342b-108">Preces izveide</span><span class="sxs-lookup"><span data-stu-id="2342b-108">Create a product</span></span>
1. <span data-ttu-id="2342b-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="2342b-109">Click New.</span></span>
2. <span data-ttu-id="2342b-110">Laukā Preces numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="2342b-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="2342b-111">Ja nav iestatīta numuru sērija preces numuram, tas ir jāievada manuāli.</span><span class="sxs-lookup"><span data-stu-id="2342b-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
3. <span data-ttu-id="2342b-112">Laukā Preces nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2342b-112">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="2342b-113">Preces nosaukuma noklusējuma vērtība ir meklēšanas nosaukums.</span><span class="sxs-lookup"><span data-stu-id="2342b-113">The product name defaults to the search name.</span></span> <span data-ttu-id="2342b-114">Ja nepieciešams, varat to izmainīt.</span><span class="sxs-lookup"><span data-stu-id="2342b-114">You can change this if needed.</span></span>  
4. <span data-ttu-id="2342b-115">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2342b-115">Click OK.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="2342b-116">Iestatīt dimensiju grupas</span><span class="sxs-lookup"><span data-stu-id="2342b-116">Set up dimension groups</span></span>
1. <span data-ttu-id="2342b-117">Noklikšķiniet uz Dimensiju grupas, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2342b-117">Click Dimension groups to open the drop dialog.</span></span>
2. <span data-ttu-id="2342b-118">Laukā Noliktavas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2342b-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="2342b-119">Noliktavas dimensijas grupa nosaka, kuras noliktavas dimensijas ir jāievada katrai transakcijai attiecīgajai precei un kā tā tiks izsekota krājumos.</span><span class="sxs-lookup"><span data-stu-id="2342b-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="2342b-120">Laukā Izsekošanas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2342b-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="2342b-121">Izsekošanas dimensijas grupa nosaka, kuras izsekošanas dimensijas ir jāievada katrai transakcijai attiecīgajai precei un kā tā tiks apstrādāta krājumos.</span><span class="sxs-lookup"><span data-stu-id="2342b-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="2342b-122">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2342b-122">Click OK.</span></span>


