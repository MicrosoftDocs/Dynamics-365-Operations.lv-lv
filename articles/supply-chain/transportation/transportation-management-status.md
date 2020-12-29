---
title: Transportēšanas pārvaldības statusi
description: Šajā tēmā skaidrots, kā izveidot transportēšanas statusu un kartēt šo statusu uz pārvadātāja statusu.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 3f7d471771ec2b4703d878fbf395cd90902b6669
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/29/2020
ms.locfileid: "4433241"
---
# <a name="transportation-management-statuses"></a><span data-ttu-id="315e1-103">Transportēšanas pārvaldības statusi</span><span class="sxs-lookup"><span data-stu-id="315e1-103">Transportation management statuses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="315e1-104">Iestatiet transportēšanas statusu šablona kodus, lai interpretētu jūsu sūtījumu pārvadātāju kodus.</span><span class="sxs-lookup"><span data-stu-id="315e1-104">Set up master codes for transportation statuses to interpret codes that are provided by your shipping carriers.</span></span> <span data-ttu-id="315e1-105">Tas ļauj integrēt sūtījuma pārvadātājus, lai nodrošinātu statusu.</span><span class="sxs-lookup"><span data-stu-id="315e1-105">This lets you integrate with shipping carriers to provide a status.</span></span> <span data-ttu-id="315e1-106">Transportēšanas statuss, ko norādāt transportēšanas šablona statusa kodam, var palīdzēt izsekot kravas, sūtījuma vai konteinera statusam.</span><span class="sxs-lookup"><span data-stu-id="315e1-106">The transportation status that you provide for a transportation master status code can help you track the status of a load, shipment, or container.</span></span> <span data-ttu-id="315e1-107">Noslodzes, kravas vai konteinera konkrēto transportēšanas statusu var atjaunināt tikai ar datu integrēšanu, nevis manuāli, izmantojot lietotāja interfeisu.</span><span class="sxs-lookup"><span data-stu-id="315e1-107">The specific transportation status for a load, shipment, or container can only be updated through data integration and not manually through the user interface.</span></span>

## <a name="create-a-transportation-status"></a><span data-ttu-id="315e1-108">Transportēšanas statusa izveide</span><span class="sxs-lookup"><span data-stu-id="315e1-108">Create a transportation status</span></span>

<span data-ttu-id="315e1-109">Lai izveidotu transportēšanas statusu, veiciet tālāk norādītās darbības:</span><span class="sxs-lookup"><span data-stu-id="315e1-109">To create a transportation status, follow these steps:</span></span>

1. <span data-ttu-id="315e1-110">Dodieties uz **Transportēšanas pārvaldība \> Iestatījumi \> Transportēšanas statusa šabloni**.</span><span class="sxs-lookup"><span data-stu-id="315e1-110">Go to **Transportation management \> Setup \> Transportation status masters**.</span></span>
1. <span data-ttu-id="315e1-111">Atlasiet **Jauns**, lai izveidotu transportēšanas statusa šablonu.</span><span class="sxs-lookup"><span data-stu-id="315e1-111">Select **New** to create a transportation status master.</span></span>
1. <span data-ttu-id="315e1-112">Laukā **Transportēšanas statusa šablons** ievadiet transportēšanas statusa kodu.</span><span class="sxs-lookup"><span data-stu-id="315e1-112">In the **Transportation status master** field, enter a unique code for the transportation status.</span></span>
1. <span data-ttu-id="315e1-113">Laukā **Transportēšanas veids** atlasiet vai nu *Nosūtīšanas pārvadātāju*, vai *Centrmezglu* kā transportēšanas veidu.</span><span class="sxs-lookup"><span data-stu-id="315e1-113">In the **Transportation type** field, select either *Shipping carrier* or *Hub* as the type of transportation.</span></span>
1. <span data-ttu-id="315e1-114">Ievadiet nosaukumu un transportēšanas statusu.</span><span class="sxs-lookup"><span data-stu-id="315e1-114">Enter a name and transportation status.</span></span>
1. <span data-ttu-id="315e1-115">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="315e1-115">Close the page.</span></span>

## <a name="map-a-transportation-status-to-a-carrier-status"></a><span data-ttu-id="315e1-116">Kartēt transportēšanas statusu uz pārvadātāja statusu</span><span class="sxs-lookup"><span data-stu-id="315e1-116">Map a transportation status to a carrier status</span></span>

<span data-ttu-id="315e1-117">Lai kartētu transportēšanas statusu uz pārvadātāja statusu, veiciet sekojošās darbības:</span><span class="sxs-lookup"><span data-stu-id="315e1-117">To map a transportation status to a carrier status, follow these steps:</span></span>

1. <span data-ttu-id="315e1-118">Dodieties uz **Transportēšanas pārvaldība \> Iestatījumi \> Pārvadātāji \> Pārvadātāja transportēšanas statuss**.</span><span class="sxs-lookup"><span data-stu-id="315e1-118">Go to **Transportation management \> Setup \> Carriers \> Carrier transportation status**.</span></span>
1. <span data-ttu-id="315e1-119">Atlasiet **Jauns**, lai sūtījumu pārvadātāja kodu kartētu uz transportēšanas statusa šablona kodu.</span><span class="sxs-lookup"><span data-stu-id="315e1-119">Select **New** to map a code from a shipping carrier to a transportation status master code.</span></span>
1. <span data-ttu-id="315e1-120">Atlasiet sūtījumu pārvadātāja un pārvadātāja pakalpojuma unikālo ID.</span><span class="sxs-lookup"><span data-stu-id="315e1-120">Select the unique ID for the shipping carrier and the carrier service.</span></span>
1. <span data-ttu-id="315e1-121">Atlasiet transportēšanas statusa kodu, ko vēlaties kartēt uz atlasīto sūtījumu pārvadātāja kodu.</span><span class="sxs-lookup"><span data-stu-id="315e1-121">Select the transportation status code that you want to map to the selected shipping carrier's code.</span></span>
1. <span data-ttu-id="315e1-122">Ievadiet ārējo kodu, ko izmanto sūtījumu pārvadātājs.</span><span class="sxs-lookup"><span data-stu-id="315e1-122">Enter the external code that is used by the shipping carrier.</span></span>
1. <span data-ttu-id="315e1-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="315e1-123">Close the page.</span></span>
