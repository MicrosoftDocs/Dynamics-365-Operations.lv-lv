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
ms.openlocfilehash: 244cf7337ec856f7517a3c0c3e055a90ab65b13f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973939"
---
# <a name="set-up-transportation-constraints-for-an-item"></a><span data-ttu-id="1f047-103">Transportēšanas ierobežojumu iestatīšana krājumam</span><span class="sxs-lookup"><span data-stu-id="1f047-103">Set up transportation constraints for an item</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1f047-104">Šī procedūra izveidos transportēšanas ierobežojumu, lai neļautu atlasītajam krājumam tikt transportētam caur atlasīto centrmezglu.</span><span class="sxs-lookup"><span data-stu-id="1f047-104">This procedure will set up a transportation constraint to prevent a selected item from being transported through a selected hub.</span></span> <span data-ttu-id="1f047-105">Šo uzdevumu parasti veic transportēšanas koordinators.</span><span class="sxs-lookup"><span data-stu-id="1f047-105">This task would typically be carried out by a Transportation coordinator.</span></span> <span data-ttu-id="1f047-106">Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="1f047-106">You can use this procedure in the USMF demo data company or on your own data.</span></span>


## <a name="create-an-item-constaint"></a><span data-ttu-id="1f047-107">Izveidojiet krājuma ierobežojumu</span><span class="sxs-lookup"><span data-stu-id="1f047-107">Create an item constaint</span></span>
1. <span data-ttu-id="1f047-108">Pārejiet uz Ierobežojumiem.</span><span class="sxs-lookup"><span data-stu-id="1f047-108">Go to Constraints.</span></span>
2. <span data-ttu-id="1f047-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1f047-109">Click New.</span></span>
3. <span data-ttu-id="1f047-110">Ierakstiet vērtību laukā ierobežojums.</span><span class="sxs-lookup"><span data-stu-id="1f047-110">In the Item constraint field, type a value.</span></span>
4. <span data-ttu-id="1f047-111">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1f047-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="1f047-112">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1f047-112">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="1f047-113">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1f047-113">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="1f047-114">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1f047-114">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="1f047-115">Laukā Centrmezgls ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1f047-115">In the Hub field, enter or select a value.</span></span>
9. <span data-ttu-id="1f047-116">Laukā Ierobežojuma darbība atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="1f047-116">In the Constraint action field, select an option.</span></span>
10. <span data-ttu-id="1f047-117">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="1f047-117">Click Save.</span></span>
11. <span data-ttu-id="1f047-118">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1f047-118">Close the page.</span></span>

