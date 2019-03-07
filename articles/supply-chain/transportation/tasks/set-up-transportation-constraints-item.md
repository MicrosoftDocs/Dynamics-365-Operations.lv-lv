---
title: Transportēšanas ierobežojumu iestatīšana krājumam
description: Šī procedūra izveidos transportēšanas ierobežojumu, lai neļautu atlasītajam krājumam tikt transportētam caur atlasīto centrmezglu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSConstraint, InventLocationIdLookup, InventItemIdLookupSimple
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 900ea1476c95d295a151125afe46aebd9642630e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "338134"
---
# <a name="set-up-transportation-constraints-for-an-item"></a><span data-ttu-id="53cc1-103">Transportēšanas ierobežojumu iestatīšana krājumam</span><span class="sxs-lookup"><span data-stu-id="53cc1-103">Set up transportation constraints for an item</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="53cc1-104">Šī procedūra izveidos transportēšanas ierobežojumu, lai neļautu atlasītajam krājumam tikt transportētam caur atlasīto centrmezglu.</span><span class="sxs-lookup"><span data-stu-id="53cc1-104">This procedure will set up a transportation constraint to prevent a selected item from being transported through a selected hub.</span></span> <span data-ttu-id="53cc1-105">Šo uzdevumu parasti veic transportēšanas koordinators.</span><span class="sxs-lookup"><span data-stu-id="53cc1-105">This task would typically be carried out by a Transportation coordinator.</span></span> <span data-ttu-id="53cc1-106">Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="53cc1-106">You can use this procedure in the USMF demo data company or on your own data.</span></span>


## <a name="create-an-item-constaint"></a><span data-ttu-id="53cc1-107">Izveidojiet krājuma ierobežojumu</span><span class="sxs-lookup"><span data-stu-id="53cc1-107">Create an item constaint</span></span>
1. <span data-ttu-id="53cc1-108">Pārejiet uz Ierobežojumiem.</span><span class="sxs-lookup"><span data-stu-id="53cc1-108">Go to Constraints.</span></span>
2. <span data-ttu-id="53cc1-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="53cc1-109">Click New.</span></span>
3. <span data-ttu-id="53cc1-110">Ierakstiet vērtību laukā ierobežojums.</span><span class="sxs-lookup"><span data-stu-id="53cc1-110">In the Item constraint field, type a value.</span></span>
4. <span data-ttu-id="53cc1-111">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53cc1-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="53cc1-112">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53cc1-112">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="53cc1-113">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53cc1-113">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="53cc1-114">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53cc1-114">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="53cc1-115">Laukā Centrmezgls ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="53cc1-115">In the Hub field, enter or select a value.</span></span>
9. <span data-ttu-id="53cc1-116">Laukā Ierobežojuma darbība atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="53cc1-116">In the Constraint action field, select an option.</span></span>
10. <span data-ttu-id="53cc1-117">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="53cc1-117">Click Save.</span></span>
11. <span data-ttu-id="53cc1-118">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="53cc1-118">Close the page.</span></span>

