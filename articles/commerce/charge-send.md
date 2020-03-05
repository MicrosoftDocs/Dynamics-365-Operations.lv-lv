---
title: Pasūtījumu piegāde no cita veikala, izmantojot līdzekli Maksas nosūtīšana
description: Šajā tēmā ir aprakstīts līdzeklis Maksas nosūtīšana.
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 0bbebcc7b2ab89bf2f5db7294acfca1d8a5ad96e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023250"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a><span data-ttu-id="eee3c-103">Pasūtījumu piegāde no cita veikala, izmantojot līdzekli Maksas nosūtīšana</span><span class="sxs-lookup"><span data-stu-id="eee3c-103">Ship orders from another store by using the Charge send feature</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="eee3c-104">Izmantojot programmas Commerce līdzekli Maksas nosūtīšana, vienā veikalā veiktos debitoru pasūtījumus var nosūtīt no cita veikala.</span><span class="sxs-lookup"><span data-stu-id="eee3c-104">With the Charge send feature in Commerce, customer orders can be placed in one store and shipped from another store.</span></span>

<span data-ttu-id="eee3c-105">Debitoru pasūtījumiem pārdošanas punkta (POS) klientā tiek atbalstītas vairākas izpildes opcijas.</span><span class="sxs-lookup"><span data-stu-id="eee3c-105">Customer orders in the point of sale (POS) client support multiple fulfillment options.</span></span> <span data-ttu-id="eee3c-106">Tālāk ir norādīti daži izpildes opciju piemēri.</span><span class="sxs-lookup"><span data-stu-id="eee3c-106">Some examples of fulfillment options include:</span></span>

- <span data-ttu-id="eee3c-107">Izdot tajā pašā veikalā citā datumā.</span><span class="sxs-lookup"><span data-stu-id="eee3c-107">Pick up from the same store on a different date.</span></span>
- <span data-ttu-id="eee3c-108">Izdot citā veikalā tajā pašā vai citā datumā.</span><span class="sxs-lookup"><span data-stu-id="eee3c-108">Pick up from a different store on the same date or a different date.</span></span>
- <span data-ttu-id="eee3c-109">Izdot no citas veikalam piešķirtās nosūtīšanas noliktavas un piegādāt noteiktā datumā.</span><span class="sxs-lookup"><span data-stu-id="eee3c-109">Ship from the default shipping warehouse that is assigned to the store, and deliver on a specific date.</span></span>

<span data-ttu-id="eee3c-110">Līdzeklim Maksas sūtīšana tiek izmantotas šādas POS operācijas: Nosūtīt visas preces un Nosūtīt atlasītās preces.</span><span class="sxs-lookup"><span data-stu-id="eee3c-110">The Charge send feature uses the following POS operations: Ship all products and Ship selected products.</span></span> <span data-ttu-id="eee3c-111">Tas sniedz veikala darbiniekam iespēju atlasīt nosūtīšanas vietu, no kuras ir jāizpilda pasūtījums vai pasūtījuma rinda.</span><span class="sxs-lookup"><span data-stu-id="eee3c-111">This allows the store clerk to select the "ship from" location that the order or order line can be fulfilled from.</span></span> <span data-ttu-id="eee3c-112">Pēc noklusējuma kā nosūtīšanas vieta ir iestatīta ar veikalu saistītā nosūtīšanas noliktava.</span><span class="sxs-lookup"><span data-stu-id="eee3c-112">By default, the "ship from" location is the shipping warehouse that is associated with the store.</span></span> <span data-ttu-id="eee3c-113">Taču veikala darbinieks var mainīt šo vietu un atlasīt jebkuru attiecīgajam veikalam piešķirtajā veikalu vietrāžu grupā definēto veikalu.</span><span class="sxs-lookup"><span data-stu-id="eee3c-113">However, the store clerk can change this location and select any store that is defined in the store locator group that is assigned to the store.</span></span>

<span data-ttu-id="eee3c-114">Tas neietekmē iespēju atlasīt piegādes adresi.</span><span class="sxs-lookup"><span data-stu-id="eee3c-114">The ability to select "ship to" addresses remains unchanged.</span></span>

<span data-ttu-id="eee3c-115">Pasūtījuma rindas izpildei izmantojamās piegādes metodes ir atkarīgas no precēm un adresēm konfigurētajiem derīgajiem piegādes veidiem.</span><span class="sxs-lookup"><span data-stu-id="eee3c-115">The shipping methods that can be used to fulfill the order line are based on the configuration of valid modes of delivery for products and addresses.</span></span> <span data-ttu-id="eee3c-116">Tā kā piegādes veidu derīguma kārtulas tiek glabātas tikai modulī Headquarters (HQ), POS klientā tiek veikts reāllaika izsaukums, lai iegūtu informāciju par sūtīšanas rindai derīgajiem piegādes veidiem.</span><span class="sxs-lookup"><span data-stu-id="eee3c-116">Because the rules about valid of modes of delivery are maintained only in the Headquarters (HQ), the POS client makes a real-time call to fetch the valid modes of delivery for a ship line.</span></span>