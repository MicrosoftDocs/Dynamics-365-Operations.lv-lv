---
title: Ražošanas izvades vieta
description: Šajā tēmā ir aprakstīta hierarhija, ko izmanto, lai identificētu ražošanas izvades vietu.
author: johanhoffmann
manager: tfehr
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e4002bf7dddb196edf306268ecc16e1bfa5d6d1e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211311"
---
# <a name="production-output-location"></a><span data-ttu-id="1bb6d-103">Ražošanas izvades vieta</span><span class="sxs-lookup"><span data-stu-id="1bb6d-103">Production output location</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1bb6d-104">Šajā tēmā ir aprakstīta hierarhija, ko izmanto, lai identificētu ražošanas izvades vietu.</span><span class="sxs-lookup"><span data-stu-id="1bb6d-104">This topic describes the hierarchy that is used to identify the production output location.</span></span>

<span data-ttu-id="1bb6d-105">Ražošanas izvades vieta ir vieta, kurā pabeigtās preces tiek uzglabātas pēc to saražošanas.</span><span class="sxs-lookup"><span data-stu-id="1bb6d-105">The production output location is the location where a finished good is first stored after it's produced.</span></span> <span data-ttu-id="1bb6d-106">Parasti šī vieta atrodas tuvu ražošanas procesam, kas izgatavo pabeigto preci.</span><span class="sxs-lookup"><span data-stu-id="1bb6d-106">Usually, this location is close to the production process that produces the finished good.</span></span> <span data-ttu-id="1bb6d-107">Ražošanas izvades vieta tiek izmantota kā starpposms materiālu uzglabāšanai pirms to pārvietošanas nosūtīšanas zonā, uzglabāšanas vietā, ražošanas ievades vietā lejupstraumes ražošanas procesam utt.</span><span class="sxs-lookup"><span data-stu-id="1bb6d-107">The production output location is used as intermediate storage for the material before it's moved on to the shipment area, a storage location, a production input location for a downstream production process, and so on.</span></span> 

<span data-ttu-id="1bb6d-108">Noklusējuma ražošanas izvades vieta tiek iestatīta, kad par pabeigtajām precēm tiek ziņots ražošanas pasūtījumā vai partijas pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="1bb6d-108">A default production output location is set when finished goods are reported on a production order or batch order.</span></span> <span data-ttu-id="1bb6d-109">Lai identificētu šo izvades vietu, tiek izmantota tālāk norādītā hierarija.</span><span class="sxs-lookup"><span data-stu-id="1bb6d-109">The following hierarchy is used to identify this output location:</span></span>

1. <span data-ttu-id="1bb6d-110">Izmantojiet izvades vietu, kas ir definēta ražošanas pasūtījuma vai partijas pasūtījuma virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="1bb6d-110">Use the output location that is defined on the production order or batch order header.</span></span>
2. <span data-ttu-id="1bb6d-111">Ja tur vieta nav atrodama, izmantojiet izvades vietu, kas ir definēta resursā, ko izmanto ražošanas maršrutā definētā pēdējā operācija.</span><span class="sxs-lookup"><span data-stu-id="1bb6d-111">If no location is found there, use the output location that is defined on the resource that is used by the last operation that is defined in the production route.</span></span>
3. <span data-ttu-id="1bb6d-112">Ja tur vieta nav atrodama, izmantojiet izvades vietu, kas ir definēta resursu grupā, ko izmanto ražošanas maršrutā definētās pēdējās operācijas resurss.</span><span class="sxs-lookup"><span data-stu-id="1bb6d-112">If no location is found there, use the output location that is defined on the resource group that is used by the resource for the last operation that is defined in the production route.</span></span>
4. <span data-ttu-id="1bb6d-113">Ja tur vieta nav atrodama, izmantojiet izvades vietu, kas ir definēta ražošanas pasūtījumam definētajā noliktavā.</span><span class="sxs-lookup"><span data-stu-id="1bb6d-113">If no location is found there, use the output location that is defined on the warehouse that is defined for the production order.</span></span>

<span data-ttu-id="1bb6d-114">Noklusējuma ražošanas izvades vieta tiek iestatīta tikai precēm, kas ir iestatītas, izmantojot papildu noliktavas procesus.</span><span class="sxs-lookup"><span data-stu-id="1bb6d-114">A default production output location is set only for products that are set up by using advanced warehouse processes.</span></span> <span data-ttu-id="1bb6d-115">Kad šāda tipa krājums tiek norādīts kā pabeigts, tiek izveidots noliktavas darbs ar tipu **Pabeigto preču izvietošana** vai **Līdzproduktu un blakusproduktu izvietošana**.</span><span class="sxs-lookup"><span data-stu-id="1bb6d-115">When this type of item is reported as finished, warehouse work of the **Finished goods put away** or **Co-product and by-product put away** type is created.</span></span> <span data-ttu-id="1bb6d-116">Šī tipa darbs ražošanas izvades vietu izmanto kā izdošanas vietu.</span><span class="sxs-lookup"><span data-stu-id="1bb6d-116">This type of work uses the production output location as the pick location.</span></span> <span data-ttu-id="1bb6d-117">Izvietošanas vietu nosaka novietojuma direktīvas.</span><span class="sxs-lookup"><span data-stu-id="1bb6d-117">The put-away location is determined by the location directives.</span></span>
