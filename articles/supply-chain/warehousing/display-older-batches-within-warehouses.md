---
title: "Vecāko partiju rādīšanas noliktavā konfigurēšana, izmantojot mobilo ierīci"
description: "Šajā tēmā aprakstīts, kā iestatīt mobilo ierīci tā, lai parādītu sarakstu ar novietojumiem, kuru partijas ir vecākas par pašreizējo darba rindas novietojumu."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations, Core
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 68477589ee43dcd7d6258ad259d2f0b8cf0050ca
ms.contentlocale: lv-lv
ms.lasthandoff: 01/17/2018

---

# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a><span data-ttu-id="f118f-103">Vecāko partiju rādīšanas noliktavā konfigurēšana, izmantojot mobilo ierīci</span><span class="sxs-lookup"><span data-stu-id="f118f-103">Configure Display older batches within warehouse on a mobile device</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f118f-104">Konfigurācija **Rādīt vecākās partijas noliktavā** ļauj parādīt sarakstu ar novietojumiem, kuru partijas ir vecākas par pašreizējo darba rindas novietojumu.</span><span class="sxs-lookup"><span data-stu-id="f118f-104">The **Display older batches within warehouse** configuration lets you display a list of locations with batches older than the current location of the work line.</span></span> <span data-ttu-id="f118f-105">Parādītajā novietojumu sarakstā ir iekļauta informācija par vecākajām partijām novietojumā, katrai partijai norādot beigu datumu un fiziskos krājumus.</span><span class="sxs-lookup"><span data-stu-id="f118f-105">The list of locations that are displayed includes information about the older batches in the location with the expiration date and the physical inventory of each batch.</span></span> <span data-ttu-id="f118f-106">Varat izvēlēties izdot no jauna novietojuma vai turpināt izdot no pašreizējā novietojuma.</span><span class="sxs-lookup"><span data-stu-id="f118f-106">You can choose to pick from a new location or to continue picking from the current location.</span></span> 
- <span data-ttu-id="f118f-107">Izdot no jauna novietojuma — ja atlasāt jaunu novietojumu, no kura izdot, pašreizējā darba rinda tiks atjaunināta jaunā novietojuma izmantošanai un darbs turpināsies jaunajā novietojumā, kā parasti.</span><span class="sxs-lookup"><span data-stu-id="f118f-107">Pick from a new location - If you select a new location to pick from, the  current work line will be updated to use the new location and work will continue as usual with the new location.</span></span> <span data-ttu-id="f118f-108">Lai jaunais novietojums būtu derīgs, tajā ir jābūt pietiekamam pieejamajam daudzumam visai darba rindai.</span><span class="sxs-lookup"><span data-stu-id="f118f-108">For the new location to be valid, it must have enough available quantity for the whole work line.</span></span> <span data-ttu-id="f118f-109">Ja nepieciešamais daudzums nebūs pieejams, darba rinda netiks atjaunināta un tiks parādīts saraksts.</span><span class="sxs-lookup"><span data-stu-id="f118f-109">If the required quantity is not available, the work line will not be updated, and the list will display.</span></span> 
- <span data-ttu-id="f118f-110">Turpināt izdot no pašreizējā novietojuma — ja turpināsit izmantot pašreizējo darba rindas novietojumu, darba rindas daudzumus turpinās izdot no sākotnējā novietojuma.</span><span class="sxs-lookup"><span data-stu-id="f118f-110">Continue picking from the current location - If you continue with the current work line location, the quantities for the work line will continue to be picked from the original location.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="f118f-111">Darbības tvērums</span><span class="sxs-lookup"><span data-stu-id="f118f-111">Where it applies</span></span>
<span data-ttu-id="f118f-112">Vecāko partiju rādīšana noliktavā tiek konfigurēta mobilās ierīces izvēlnes vienumos, un tā ietekmē izdošanu partijā iekļautajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="f118f-112">Display older batches within warehouse is configured on mobile device menu items and affects the pick for batch below items.</span></span>

## <a name="set-up-display-older-batches-within-warehouse"></a><span data-ttu-id="f118f-113">Vecāko partiju rādīšanas noliktavā iestatīšana</span><span class="sxs-lookup"><span data-stu-id="f118f-113">Set up Display older batches within warehouse</span></span>
<span data-ttu-id="f118f-114">Konfigurācija **Rādīt vecākās partijas noliktavā** ir pieejama mobilās ierīces izvēlnes vienumiem, ja opcija **Izdot vecāko partiju** ir iestatīta uz **Brīdināt**.</span><span class="sxs-lookup"><span data-stu-id="f118f-114">The **Display older batches within warehouse** configuration is available on mobile device menu items when the **Pick oldest batch** option is set to **Warn**.</span></span>

- <span data-ttu-id="f118f-115">Sadaļā **Noliktavas pārvaldība** > **Iestatīšana** > **Mobilā ierīce** > **Mobilās ierīces izvēlnes vienumi** iestatiet opciju **Izmantot esošo darbu** uz **Jā** izvēlnes vienumam un laukā **Izdot vecāko partiju** atlasiet **Brīdināt**.</span><span class="sxs-lookup"><span data-stu-id="f118f-115">Under **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**, set **Use existing work** to **Yes** for the menu item, and select **Warn** in the **Pick oldest batch** field.</span></span> 


