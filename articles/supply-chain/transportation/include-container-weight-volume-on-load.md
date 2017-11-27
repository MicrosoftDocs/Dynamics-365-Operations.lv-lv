---
title: "Konteinera svara un tilpuma ietveršana kravā"
description: "Šajā tēmā ir aprakstīts, kā iestatīt un lietot funkcionalitāti konteinera svara un tilpuma ietveršanai kravās."
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4190b5cb05cccc3d762d8ad153ecbd467fa0a332
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="include-container-weight-and-volume-on-load"></a><span data-ttu-id="681c4-103">Konteinera svara un tilpuma ietveršana kravā</span><span class="sxs-lookup"><span data-stu-id="681c4-103">Include container weight and volume on load</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="681c4-104">Funkcionalitāte konteinera svara un tilpuma ietveršanai kravā skaidri parāda kravu veidojošo konteineru un krājumu kopējo svaru un tilpumu.</span><span class="sxs-lookup"><span data-stu-id="681c4-104">The functionality for including the container weight and volume on a load gives a clear representation of the total weight and volume of containers and items that are going on a load.</span></span>

<span data-ttu-id="681c4-105">Krava ietver atsevišķu sūtījumu vai vairākus sūtījumus, un šie sūtījumi ietver atsevišķus krājumus, kas pieder vienam pārdošanas pasūtījumam vai vairākiem pārdošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="681c4-105">A load contains a single shipment or multiple shipments, and these shipments contain distinct items that belong to a single sales order or multiple sales orders.</span></span> <span data-ttu-id="681c4-106">Šie krājumi tiek ievietoti konteinerā, un konteineri tiek ievietoti kravā.</span><span class="sxs-lookup"><span data-stu-id="681c4-106">The items are stored inside a container, and containers are loaded on a load.</span></span> <span data-ttu-id="681c4-107">Arī krājumi, kas atrodas ārpus konteinera, var veidot daļu no kravas.</span><span class="sxs-lookup"><span data-stu-id="681c4-107">Items that are outside a container can also be part of a load.</span></span> <span data-ttu-id="681c4-108">Pamatojoties uz šiem nosacījumiem, sistēma aprēķina vērtības attiecībā uz kravas svaru un tilpumu, ņemot vērā gan konteineru, gan krājumu svaru un tilpumu.</span><span class="sxs-lookup"><span data-stu-id="681c4-108">Based on these conditions, the system calculates values for the weight and volume on the load by considering the weight and volume of both containers and items.</span></span>

<span data-ttu-id="681c4-109">Ja aprēķinātās vērtības nav precīzs, varat tās pielāgot, ievadot faktiskās vērtības attiecībā uz kravas svaru un tilpumu.</span><span class="sxs-lookup"><span data-stu-id="681c4-109">If the calculated values aren’t precise, you can adjust them by entering the actual values for the weight and volume on the load.</span></span> <span data-ttu-id="681c4-110">Svara un tilpuma vērtības tiek izmantotas transportēšanas pārvaldības procesos.</span><span class="sxs-lookup"><span data-stu-id="681c4-110">The values for the weight and volume are used in transportation management processes.</span></span> <span data-ttu-id="681c4-111">Šis vērtības tiek izmantotas, piemēram, likmju un maršrutu rīkā, kur tās palīdz definēt kravu likmi un maršrutu, un tās tiek izmantotas arī transportēšanas norēķinos un transportlīdzekļu vadītāju reģistrēšanai norīkojuma izpildei.</span><span class="sxs-lookup"><span data-stu-id="681c4-111">For example, the values are used in the rate route workbench, where they help define the rate and route for loads, and they are also used for transportation tenders and driver check-in.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="681c4-112">Darbības tvērums</span><span class="sxs-lookup"><span data-stu-id="681c4-112">Where it applies</span></span>

<span data-ttu-id="681c4-113">Funkcionalitāte konteinera svara un tilpuma ietveršanai kravā attiecas uz transportēšanas pārvaldības procesiem, piemēram, uz likmju un maršrutu rīku, transportēšanas norēķiniem un transportlīdzekļu vadītāju reģistrēšanu norīkojuma izpildei.</span><span class="sxs-lookup"><span data-stu-id="681c4-113">The functionality for including the container weight and volume on a load applies in transportation management processes, such as the rate route workbench, transportation tenders, and driver check-in.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="681c4-114">Kā to iestatīt</span><span class="sxs-lookup"><span data-stu-id="681c4-114">How it is set up</span></span>

<span data-ttu-id="681c4-115">Par kravu uzskatāmo konteineru skaits tiek aprēķināts, pamatojoties uz konteinera svaru un tilpumu, kā arī uz konteinera izmantojuma procentuālo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="681c4-115">The number of containers that should be considered for a load is calculated based on the weight and volume of the container, and on the percentage of the container is used.</span></span>

-   <span data-ttu-id="681c4-116">Lai konteineram iestatītu svaru un tilpumu, noklikšķiniet uz **Noliktavas vadība** \> **Iestatījumi** \> **Konteineri** \> **Konteineru tipi**.</span><span class="sxs-lookup"><span data-stu-id="681c4-116">To set the weight and volume for a container, click **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>

-   <span data-ttu-id="681c4-117">Lai iestatītu konteinera izmantojuma procentuālo vērtību, noklikšķiniet uz **Noliktavas vadība** \> **Iestatījumi** \> **Konteineri** \> **Konteineru grupas** un ievadiet vērtību laukā **Konteinera izmantojuma procentuālā vērtība**.</span><span class="sxs-lookup"><span data-stu-id="681c4-117">To set the container utilization percentage, click **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**, and then enter a value in the **Container utilization percentage** field.</span></span>

