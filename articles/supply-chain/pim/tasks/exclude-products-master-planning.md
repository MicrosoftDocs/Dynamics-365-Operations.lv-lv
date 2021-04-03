---
title: Preces dzīves cikla stāvokļa izveidošana, lai izslēgtu preces no vispārējās plānošanas
description: Šajā procedūrā ir parādīts, kā izveidot jaunu preces dzīves cikla stāvokli, kas izslēdz preces no vispārējās plānošanas un MK līmeņa aprēķina.
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
ms.openlocfilehash: fc24aad05499adf9bfb2db3613c7f134c3a70770
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264702"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a><span data-ttu-id="88d4a-103">Preces dzīves cikla stāvokļa izveidošana, lai izslēgtu preces no vispārējās plānošanas</span><span class="sxs-lookup"><span data-stu-id="88d4a-103">Create a product lifecycle state to exclude products from Master planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="88d4a-104">Šajā procedūrā ir parādīts, kā izveidot jaunu preces dzīves cikla stāvokli, kas izslēdz preces no vispārējās plānošanas un MK līmeņa aprēķina.</span><span class="sxs-lookup"><span data-stu-id="88d4a-104">This procedure shows how to create a new product lifecycle state that excludes the products from Master planning and BOM-level calculation.</span></span>


## <a name="create-an-obsolete-state"></a><span data-ttu-id="88d4a-105">Novecojuša stāvokļa izveide</span><span class="sxs-lookup"><span data-stu-id="88d4a-105">Create an obsolete state</span></span>
1. <span data-ttu-id="88d4a-106">Pārejiet uz sadaļu Preču informācijas pārvaldība > Iestatīšana > Preces dzīves cikla stāvoklis.</span><span class="sxs-lookup"><span data-stu-id="88d4a-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="88d4a-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="88d4a-107">Click New.</span></span>
3. <span data-ttu-id="88d4a-108">Laukā Stāvoklis ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="88d4a-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="88d4a-109">Atlasiet Nē laukā Ir aktīvs plānošanai.</span><span class="sxs-lookup"><span data-stu-id="88d4a-109">Select No in the Is active for planning field.</span></span>
5. <span data-ttu-id="88d4a-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="88d4a-110">In the Description field, type a value.</span></span>

## <a name="associate-the-obsolete-state-to-a-released-product"></a><span data-ttu-id="88d4a-111">Novecojuša stāvokļa saistīšana ar izlaistu preci</span><span class="sxs-lookup"><span data-stu-id="88d4a-111">Associate the obsolete state to a released product</span></span>
1. <span data-ttu-id="88d4a-112">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="88d4a-112">Close the page.</span></span>
2. <span data-ttu-id="88d4a-113">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="88d4a-113">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="88d4a-114">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="88d4a-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="88d4a-115">Piemēram, filtrējiet pēc lauka Saīsināts nosaukums, izmantojot vērtību “M00”.</span><span class="sxs-lookup"><span data-stu-id="88d4a-115">For example, filter on the Search name field with a value of 'M00'.</span></span>
4. <span data-ttu-id="88d4a-116">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="88d4a-116">Click Edit.</span></span>
5. <span data-ttu-id="88d4a-117">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="88d4a-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="88d4a-118">Laukā Preces dzīves cikla stāvoklis ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="88d4a-118">In the Product lifecycle state field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]