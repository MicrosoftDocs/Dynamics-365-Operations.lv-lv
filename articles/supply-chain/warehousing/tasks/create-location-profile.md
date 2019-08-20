---
title: Novietojuma profila izveide
description: Katrai atrašanās vietai noliktavā ir jābūt ar to saistītam atrašanās vietas profilam, kas apraksta atrašanās vietas rekvizītus, piemēram, vai atrašanās vieta atļauj jauktus krājumus.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9e1217a1105e1d53fc937f927e066e392f1ef14
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847331"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="29ca0-103">Novietojuma profila izveide</span><span class="sxs-lookup"><span data-stu-id="29ca0-103">Create a location profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="29ca0-104">Katrai atrašanās vietai noliktavā ir jābūt ar to saistītam atrašanās vietas profilam, kas apraksta atrašanās vietas rekvizītus, piemēram, vai atrašanās vieta atļauj jauktus krājumus.</span><span class="sxs-lookup"><span data-stu-id="29ca0-104">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="29ca0-105">Šajā procedūrā tiks izveidots profils atrašanās vietai, kurai nav nepieciešama noliktavas vienības kontrole.</span><span class="sxs-lookup"><span data-stu-id="29ca0-105">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="29ca0-106">Tiks iespējoti jaukti krājumi un jauktu krājumu statusi, kā arī atļauta cikla inventarizācija.</span><span class="sxs-lookup"><span data-stu-id="29ca0-106">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="29ca0-107">Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="29ca0-107">You can use this procedure in the USMF demo data company.</span></span>

1. <span data-ttu-id="29ca0-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="29ca0-108">Click New.</span></span>
2. <span data-ttu-id="29ca0-109">Laukā Novietojuma profila ID ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="29ca0-109">In the Location profile ID field, type a value.</span></span>
3. <span data-ttu-id="29ca0-110">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="29ca0-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="29ca0-111">Laukā Atrašanās vietas formāts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="29ca0-111">In the Location format field, enter or select a value.</span></span>
5. <span data-ttu-id="29ca0-112">Laukā Atrašanās vietas tips ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="29ca0-112">In the Location type field, enter or select a value.</span></span>
6. <span data-ttu-id="29ca0-113">Laukā Doka pārvaldības profila ID ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="29ca0-113">In the Dock management profile ID field, enter or select a value.</span></span>
7. <span data-ttu-id="29ca0-114">Laukā Atļaut jauktus krājumus atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="29ca0-114">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="29ca0-115">Laukā Atļaut jauktus krājumu statusus atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="29ca0-115">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="29ca0-116">Atlasiet Jā laukā Atļaut cikla inventarizāciju.</span><span class="sxs-lookup"><span data-stu-id="29ca0-116">Select Yes in the Allow cycle counting field.</span></span>
10. <span data-ttu-id="29ca0-117">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="29ca0-117">Click Save.</span></span>
11. <span data-ttu-id="29ca0-118">Dodieties uz Noliktavas vadība > Iestatīšana > Noliktava > Novietojumu profili.</span><span class="sxs-lookup"><span data-stu-id="29ca0-118">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>

