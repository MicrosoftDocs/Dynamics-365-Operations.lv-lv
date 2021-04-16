---
title: Transportēšanas pārvaldības statusi
description: Šajā tēmā skaidrots, kā izveidot transportēšanas statusu un kartēt šo statusu uz pārvadātāja statusu.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: f3a2b9e50dddf0f015cdd3f16d6d93fcc03d464d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807612"
---
# <a name="transportation-management-statuses"></a><span data-ttu-id="cf8a5-103">Transportēšanas pārvaldības statusi</span><span class="sxs-lookup"><span data-stu-id="cf8a5-103">Transportation management statuses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf8a5-104">Iestatiet transportēšanas statusu šablona kodus, lai interpretētu jūsu sūtījumu pārvadātāju kodus.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-104">Set up master codes for transportation statuses to interpret codes that are provided by your shipping carriers.</span></span> <span data-ttu-id="cf8a5-105">Tas ļauj integrēt sūtījuma pārvadātājus, lai nodrošinātu statusu.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-105">This lets you integrate with shipping carriers to provide a status.</span></span> <span data-ttu-id="cf8a5-106">Transportēšanas statuss, ko norādāt transportēšanas šablona statusa kodam, var palīdzēt izsekot kravas, sūtījuma vai konteinera statusam.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-106">The transportation status that you provide for a transportation master status code can help you track the status of a load, shipment, or container.</span></span> <span data-ttu-id="cf8a5-107">Noslodzes, kravas vai konteinera konkrēto transportēšanas statusu var atjaunināt tikai ar datu integrēšanu, nevis manuāli, izmantojot lietotāja interfeisu.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-107">The specific transportation status for a load, shipment, or container can only be updated through data integration and not manually through the user interface.</span></span>

## <a name="create-a-transportation-status"></a><span data-ttu-id="cf8a5-108">Transportēšanas statusa izveide</span><span class="sxs-lookup"><span data-stu-id="cf8a5-108">Create a transportation status</span></span>

<span data-ttu-id="cf8a5-109">Lai izveidotu transportēšanas statusu, veiciet tālāk norādītās darbības:</span><span class="sxs-lookup"><span data-stu-id="cf8a5-109">To create a transportation status, follow these steps:</span></span>

1. <span data-ttu-id="cf8a5-110">Dodieties uz **Transportēšanas pārvaldība \> Iestatījumi \> Transportēšanas statusa šabloni**.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-110">Go to **Transportation management \> Setup \> Transportation status masters**.</span></span>
1. <span data-ttu-id="cf8a5-111">Atlasiet **Jauns**, lai izveidotu transportēšanas statusa šablonu.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-111">Select **New** to create a transportation status master.</span></span>
1. <span data-ttu-id="cf8a5-112">Laukā **Transportēšanas statusa šablons** ievadiet transportēšanas statusa kodu.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-112">In the **Transportation status master** field, enter a unique code for the transportation status.</span></span>
1. <span data-ttu-id="cf8a5-113">Laukā **Transportēšanas veids** atlasiet vai nu *Nosūtīšanas pārvadātāju*, vai *Centrmezglu* kā transportēšanas veidu.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-113">In the **Transportation type** field, select either *Shipping carrier* or *Hub* as the type of transportation.</span></span>
1. <span data-ttu-id="cf8a5-114">Ievadiet nosaukumu un transportēšanas statusu.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-114">Enter a name and transportation status.</span></span>
1. <span data-ttu-id="cf8a5-115">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-115">Close the page.</span></span>

## <a name="map-a-transportation-status-to-a-carrier-status"></a><span data-ttu-id="cf8a5-116">Kartēt transportēšanas statusu uz pārvadātāja statusu</span><span class="sxs-lookup"><span data-stu-id="cf8a5-116">Map a transportation status to a carrier status</span></span>

<span data-ttu-id="cf8a5-117">Lai kartētu transportēšanas statusu uz pārvadātāja statusu, veiciet sekojošās darbības:</span><span class="sxs-lookup"><span data-stu-id="cf8a5-117">To map a transportation status to a carrier status, follow these steps:</span></span>

1. <span data-ttu-id="cf8a5-118">Dodieties uz **Transportēšanas pārvaldība \> Iestatījumi \> Pārvadātāji \> Pārvadātāja transportēšanas statuss**.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-118">Go to **Transportation management \> Setup \> Carriers \> Carrier transportation status**.</span></span>
1. <span data-ttu-id="cf8a5-119">Atlasiet **Jauns**, lai sūtījumu pārvadātāja kodu kartētu uz transportēšanas statusa šablona kodu.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-119">Select **New** to map a code from a shipping carrier to a transportation status master code.</span></span>
1. <span data-ttu-id="cf8a5-120">Atlasiet sūtījumu pārvadātāja un pārvadātāja pakalpojuma unikālo ID.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-120">Select the unique ID for the shipping carrier and the carrier service.</span></span>
1. <span data-ttu-id="cf8a5-121">Atlasiet transportēšanas statusa kodu, ko vēlaties kartēt uz atlasīto sūtījumu pārvadātāja kodu.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-121">Select the transportation status code that you want to map to the selected shipping carrier's code.</span></span>
1. <span data-ttu-id="cf8a5-122">Ievadiet ārējo kodu, ko izmanto sūtījumu pārvadātājs.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-122">Enter the external code that is used by the shipping carrier.</span></span>
1. <span data-ttu-id="cf8a5-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-123">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]