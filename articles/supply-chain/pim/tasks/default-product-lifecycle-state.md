---
title: Noklusējuma preces dzīves cikla stāvokļa izveidošana
description: Šajā procedūrā ir parādīts, kā izveidot noklusējuma preces dzīves cikla stāvokli un kā saistīt noklusējuma stāvokli ar izlaistajām precēm.
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b62d47f52da7f9e18bce401578a5e2a629ac5eb8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818137"
---
# <a name="create-a-default-product-lifecycle-state"></a><span data-ttu-id="02e09-103">Noklusējuma preces dzīves cikla stāvokļa izveidošana</span><span class="sxs-lookup"><span data-stu-id="02e09-103">Create a default product lifecycle state</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="02e09-104">Šajā procedūrā ir parādīts, kā izveidot noklusējuma preces dzīves cikla stāvokli un kā saistīt noklusējuma stāvokli ar izlaistajām precēm.</span><span class="sxs-lookup"><span data-stu-id="02e09-104">This procedure shows how to create a default product lifecycle state as well as how to associate the default state with released products.</span></span>


## <a name="create-a-default-lifecycle-state"></a><span data-ttu-id="02e09-105">Noklusējuma dzīves cikla stāvokļa izveidošana</span><span class="sxs-lookup"><span data-stu-id="02e09-105">Create a default lifecycle state</span></span>
1. <span data-ttu-id="02e09-106">Pārejiet uz sadaļu Preču informācijas pārvaldība > Iestatīšana > Preces dzīves cikla stāvoklis.</span><span class="sxs-lookup"><span data-stu-id="02e09-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="02e09-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="02e09-107">Click New.</span></span>
3. <span data-ttu-id="02e09-108">Laukā Stāvoklis ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="02e09-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="02e09-109">Atlasiet Jā laukā Noklusējums, kad izlaists juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="02e09-109">Select Yes in the Default when released to legal entity field.</span></span>
5. <span data-ttu-id="02e09-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="02e09-110">In the Description field, type a value.</span></span>
6. <span data-ttu-id="02e09-111">Laukā Ir aktīvs plānošanai atlasiet Nē.</span><span class="sxs-lookup"><span data-stu-id="02e09-111">Select No in the Is active for planning field.</span></span>

> [!NOTE]
> <span data-ttu-id="02e09-112">Ja jauna izlaistā prece nav jāiekļauj vispārējā plānošanā, atlasiet Nē.</span><span class="sxs-lookup"><span data-stu-id="02e09-112">If a new released product should not be included in Master planning, select No.</span></span> <span data-ttu-id="02e09-113">Ja tā ir jāiekļauj vispārējā plānošanā, atstājiet vadīklas noklusējuma vērtību Jā.</span><span class="sxs-lookup"><span data-stu-id="02e09-113">If it should be included in Master planning, leave the control at its default value Yes.</span></span>  

## <a name="create-a-new-released-product"></a><span data-ttu-id="02e09-114">Jaunas izlaistās preces izveide</span><span class="sxs-lookup"><span data-stu-id="02e09-114">Create a new released product</span></span>
1. <span data-ttu-id="02e09-115">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="02e09-115">Close the page.</span></span>
2. <span data-ttu-id="02e09-116">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="02e09-116">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="02e09-117">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="02e09-117">Click New.</span></span>
4. <span data-ttu-id="02e09-118">Laukā Preces numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="02e09-118">In the Product number field, type a value.</span></span>
5. <span data-ttu-id="02e09-119">Laukā Preces nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="02e09-119">In the Product name field, type a value.</span></span>
6. <span data-ttu-id="02e09-120">Laukā Meklēšanas nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="02e09-120">In the Search name field, type a value.</span></span>
7. <span data-ttu-id="02e09-121">Laukā Krājumu modeļu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="02e09-121">In the Item model group field, enter or select a value.</span></span>
8. <span data-ttu-id="02e09-122">Laukā Krājumu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="02e09-122">In the Item group field, enter or select a value.</span></span>
9. <span data-ttu-id="02e09-123">Laukā Noliktavas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="02e09-123">In the Storage dimension group field, enter or select a value.</span></span>
10. <span data-ttu-id="02e09-124">Laukā Izsekošanas dimensiju grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="02e09-124">In the Tracking dimension group field, enter or select a value.</span></span>
11. <span data-ttu-id="02e09-125">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="02e09-125">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="02e09-126">Noklusējuma preces dzīves cikla stāvoklis ir globāla definīcija.</span><span class="sxs-lookup"><span data-stu-id="02e09-126">The default product lifecycle state is a global definition.</span></span>  

## <a name="change-the-product-to-an-active-state"></a><span data-ttu-id="02e09-127">Maiņa uz aktīvu statusu precei</span><span class="sxs-lookup"><span data-stu-id="02e09-127">Change the product to an active state</span></span>
1. <span data-ttu-id="02e09-128">Laukā Preces dzīves cikla stāvoklis ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="02e09-128">In the Product lifecycle state field, enter or select a value.</span></span>

> [!NOTE]
> <span data-ttu-id="02e09-129">Pieņemot, ka esat iestatījis aktīvu stāvokli, tagad ir iespējams atlasīt aktīvo stāvokli, lai ļautu preci izmantot vispārējā plānošanā un MK līmeņa aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="02e09-129">Assume that you have set up an active state, you can now select the active state to allow the product to be used in Master planning and BOM-level calculation.</span></span> <span data-ttu-id="02e09-130">Protams, tam ir nozīme tikai tad, ja ir norādīta visa produkta detalizētā informācija, kas nepieciešama konsekventai plānošanai.</span><span class="sxs-lookup"><span data-stu-id="02e09-130">Obviously, this only makes sense if all the product details that are required for consistent planning are specified.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]