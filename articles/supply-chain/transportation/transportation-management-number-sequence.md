---
title: Transportēšanas pārvaldība skaita sērija
description: Šajā tēmā aprakstīts, kā iestatīt skaita sērijas transportēšanas pārvaldībai.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: f3da757cbf47e0e1af781b720d17a673e19aeb3b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807684"
---
# <a name="transportation-management-number-sequence"></a><span data-ttu-id="94e62-103">Transportēšanas pārvaldība skaita sērija</span><span class="sxs-lookup"><span data-stu-id="94e62-103">Transportation management number sequence</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94e62-104">Izmantojiet lapu **Skaita sērijas**, kas atrodas transportēšanas pārvaldības modulī, lai iestatītu dažādus pro numurus.</span><span class="sxs-lookup"><span data-stu-id="94e62-104">Use the **Number sequences** page in the transportation management module to set up various pro numbers.</span></span> <span data-ttu-id="94e62-105">Pro numurus izmanto pārvadātāji, lai organizētu un izsekotu katra sūtījuma norisi.</span><span class="sxs-lookup"><span data-stu-id="94e62-105">Pro numbers are used by carriers to organize and track the progress of each shipment.</span></span>

## <a name="create-a-number-sequence-for-a-pro-number"></a><span data-ttu-id="94e62-106">Izveidojiet skaita sēriju pro numuram</span><span class="sxs-lookup"><span data-stu-id="94e62-106">Create a number sequence for a pro number</span></span>

<span data-ttu-id="94e62-107">Lai izveidotu skaita sēriju pro numuram, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="94e62-107">To create a number sequence for a pro number, do the following:</span></span>

1. <span data-ttu-id="94e62-108">Dodieties uz **Transportēšanas pārvaldība \> Iestatījumi \> Pārvadātāji \> Skaita sērijas**.</span><span class="sxs-lookup"><span data-stu-id="94e62-108">Go to **Transportation management \> Setup \> Carriers \> Number sequences**.</span></span>
1. <span data-ttu-id="94e62-109">Atlasiet **Jauns**, lai izveidotu jaunu skaita sēriju.</span><span class="sxs-lookup"><span data-stu-id="94e62-109">Select **New** to create a new number sequence.</span></span>
1. <span data-ttu-id="94e62-110">Ievadiet skaita sērijai unikālu ID un aprakstošu nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="94e62-110">Enter a unique ID and descriptive name for the number sequence.</span></span>
1. <span data-ttu-id="94e62-111">Laukā **Skaita sērijas veids** *Pro numurs* ir vienīgā opcija.</span><span class="sxs-lookup"><span data-stu-id="94e62-111">In the **Number sequence type** field, *Pro number* is the only option.</span></span>
1. <span data-ttu-id="94e62-112">Laukā **Pārbaudes cipars** *Pārbaudes cipars* ir vienīgā opcija, un to iestata kā vispārīgu programmu.</span><span class="sxs-lookup"><span data-stu-id="94e62-112">In the **Check digit** field, *Check digit* is the only option and is set up as a generic engine.</span></span>
1. <span data-ttu-id="94e62-113">Kopsavilkuma cilnē **Sērija** sniedziet informāciju par sēriju.</span><span class="sxs-lookup"><span data-stu-id="94e62-113">On the **Sequence** FastTab, provide information about the sequence.</span></span>
1. <span data-ttu-id="94e62-114">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="94e62-114">Close the page.</span></span>

## <a name="link-a-number-sequence-to-a-shipping-carrier"></a><span data-ttu-id="94e62-115">Skaita sērijas saistīšana ar sūtījuma pārvadātāju</span><span class="sxs-lookup"><span data-stu-id="94e62-115">Link a number sequence to a shipping carrier</span></span>

<span data-ttu-id="94e62-116">Lai saistītu skaita sēriju ar pārvadātāju, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="94e62-116">To link a number sequence to a carrier, do the following:</span></span>

1. <span data-ttu-id="94e62-117">Dodieties uz **Transportēšanas pārvaldība \> Iestatījumi \> Pārvadātāji \> Sūtījumu pārvadātāji**.</span><span class="sxs-lookup"><span data-stu-id="94e62-117">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="94e62-118">Atlasiet nosūtījumu pārvadātāju.</span><span class="sxs-lookup"><span data-stu-id="94e62-118">Select a shipping carrier.</span></span>
1. <span data-ttu-id="94e62-119">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="94e62-119">Select **Edit**.</span></span>
1. <span data-ttu-id="94e62-120">Kopsavilkuma cilnē **Pārskats** atlasiet opciju laukā **Pro numura sērija**.</span><span class="sxs-lookup"><span data-stu-id="94e62-120">On the **Overview** FastTab, select an option in the **Pro number sequence** field.</span></span>
1. <span data-ttu-id="94e62-121">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="94e62-121">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]