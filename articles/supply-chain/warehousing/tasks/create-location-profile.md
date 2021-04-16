---
title: Vietas profila izveide
description: Šajā tēmā ir paskaidrots, kā izveidot atrašanās vietas profilu pakalpojumā Dynamics 365 Supply Chain Management.
author: ShylaThompson
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 101d80216f786eb8edb687031e4deac8cc3033ff
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831030"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="5447c-103">Vietas profila izveide</span><span class="sxs-lookup"><span data-stu-id="5447c-103">Create a location profile</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5447c-104">Šajā tēmā ir paskaidrots, kā izveidot atrašanās vietas profilu pakalpojumā Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5447c-104">This topic explains how to create a location profile in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="5447c-105">Katrai atrašanās vietai noliktavā ir jābūt ar to saistītam atrašanās vietas profilam, kas apraksta atrašanās vietas rekvizītus, piemēram, vai atrašanās vieta atļauj jauktus krājumus.</span><span class="sxs-lookup"><span data-stu-id="5447c-105">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="5447c-106">Šajā procedūrā tiks izveidots profils atrašanās vietai, kurai nav nepieciešama noliktavas vienības kontrole.</span><span class="sxs-lookup"><span data-stu-id="5447c-106">In this procedure we'll create a profile for a location that doesn't require license plate control.</span></span> <span data-ttu-id="5447c-107">Tiks iespējoti jaukti krājumi un jauktu krājumu statusi, kā arī atļauta cikla inventarizācija.</span><span class="sxs-lookup"><span data-stu-id="5447c-107">We'll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="5447c-108">Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="5447c-108">You can use this procedure in the USMF demo data company.</span></span>


1. <span data-ttu-id="5447c-109">Navigācijas rūtī ejiet uz **Moduļi > Noliktavas pārvaldība > Iestatīšana> Noliktava > Atrašanās vietas profili**.</span><span class="sxs-lookup"><span data-stu-id="5447c-109">In the navigation pane, go to **Modules > Warehouse management > Setup > Warehouse > Location profiles**.</span></span>
2. <span data-ttu-id="5447c-110">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5447c-110">Select **New**.</span></span>
3. <span data-ttu-id="5447c-111">Laukā **Atrašanās vietas ID** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="5447c-111">In the **Location profile ID** field, type a value.</span></span>
4. <span data-ttu-id="5447c-112">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5447c-112">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="5447c-113">Ievadiet vai atlasiet vērtību laukā **Atrašanās vietas formāts**.</span><span class="sxs-lookup"><span data-stu-id="5447c-113">In the **Location format** field, enter or select a value.</span></span>
6. <span data-ttu-id="5447c-114">Ievadiet vai atlasiet vērtību laukā **Atrašanās vietas veids**.</span><span class="sxs-lookup"><span data-stu-id="5447c-114">In the **Location type** field, enter or select a value.</span></span>
7. <span data-ttu-id="5447c-115">Ievadiet vai atlasiet vērtību laukā **Dokot pārvaldības profila ID**.</span><span class="sxs-lookup"><span data-stu-id="5447c-115">In the **Dock management profile ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="5447c-116">Atlasiet **Jā** laukā **Atļaut jauktus vienumus**.</span><span class="sxs-lookup"><span data-stu-id="5447c-116">Select **Yes** in the **Allow mixed items** field.</span></span>
9. <span data-ttu-id="5447c-117">Atlasiet **Jā** laukā **Atļaut jauktus krājumu statusus**.</span><span class="sxs-lookup"><span data-stu-id="5447c-117">Select **Yes** in the **Allow mixed inventory statuses** field.</span></span>
10. <span data-ttu-id="5447c-118">Atlasiet **Jā** laukā **Atļaut ciklu skaitīšanu**.</span><span class="sxs-lookup"><span data-stu-id="5447c-118">Select **Yes** in the **Allow cycle counting** field.</span></span>
11. <span data-ttu-id="5447c-119">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5447c-119">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]