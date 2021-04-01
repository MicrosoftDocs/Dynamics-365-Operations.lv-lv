---
title: Transportēšanas ierobežojumu iestatīšana krājumam
description: Šī procedūra izveidos transportēšanas ierobežojumu, lai neļautu atlasītajam krājumam tikt transportētam caur atlasīto centrmezglu.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSConstraint, InventLocationIdLookup, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e2ff8458a9821e1aa2ae8d2dc93cc89cfc318d70
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233563"
---
# <a name="set-up-transportation-constraints-for-an-item"></a><span data-ttu-id="0ac91-103">Transportēšanas ierobežojumu iestatīšana krājumam</span><span class="sxs-lookup"><span data-stu-id="0ac91-103">Set up transportation constraints for an item</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0ac91-104">Šī procedūra izveidos transportēšanas ierobežojumu, lai neļautu atlasītajam krājumam tikt transportētam caur atlasīto centrmezglu.</span><span class="sxs-lookup"><span data-stu-id="0ac91-104">This procedure will set up a transportation constraint to prevent a selected item from being transported through a selected hub.</span></span> <span data-ttu-id="0ac91-105">Šo uzdevumu parasti veic transportēšanas koordinators.</span><span class="sxs-lookup"><span data-stu-id="0ac91-105">This task would typically be carried out by a Transportation coordinator.</span></span> <span data-ttu-id="0ac91-106">Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="0ac91-106">You can use this procedure in the USMF demo data company or on your own data.</span></span>


## <a name="create-an-item-constaint"></a><span data-ttu-id="0ac91-107">Izveidojiet krājuma ierobežojumu</span><span class="sxs-lookup"><span data-stu-id="0ac91-107">Create an item constaint</span></span>
1. <span data-ttu-id="0ac91-108">Pārejiet uz Ierobežojumiem.</span><span class="sxs-lookup"><span data-stu-id="0ac91-108">Go to Constraints.</span></span>
2. <span data-ttu-id="0ac91-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="0ac91-109">Click New.</span></span>
3. <span data-ttu-id="0ac91-110">Ierakstiet vērtību laukā ierobežojums.</span><span class="sxs-lookup"><span data-stu-id="0ac91-110">In the Item constraint field, type a value.</span></span>
4. <span data-ttu-id="0ac91-111">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0ac91-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="0ac91-112">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0ac91-112">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="0ac91-113">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0ac91-113">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="0ac91-114">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0ac91-114">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="0ac91-115">Laukā Centrmezgls ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0ac91-115">In the Hub field, enter or select a value.</span></span>
9. <span data-ttu-id="0ac91-116">Laukā Ierobežojuma darbība atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="0ac91-116">In the Constraint action field, select an option.</span></span>
10. <span data-ttu-id="0ac91-117">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="0ac91-117">Click Save.</span></span>
11. <span data-ttu-id="0ac91-118">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0ac91-118">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]