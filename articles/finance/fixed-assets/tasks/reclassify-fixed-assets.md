---
title: Pamatlīdzekļu pārklasificēšana
description: Lai pārklasificētu pamatlīdzekli, tas ir jāpārsūta uz jaunu pamatlīdzekļu grupu vai tam ir jāpiešķir jauns pamatlīdzekļa numurs tajā pašā grupā.
author: saraschi2
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fbfb754459fad1f3b1509f4f9c65c20e0385b013
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944717"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="d74d9-103">Pamatlīdzekļu pārklasificēšana</span><span class="sxs-lookup"><span data-stu-id="d74d9-103">Reclassify fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d74d9-104">Lai pārklasificētu pamatlīdzekli, tas ir jāpārsūta uz jaunu pamatlīdzekļu grupu vai tam ir jāpiešķir jauns pamatlīdzekļa numurs tajā pašā grupā.</span><span class="sxs-lookup"><span data-stu-id="d74d9-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="d74d9-105">Kad pamatlīdzeklis ir pārklasificētas:</span><span class="sxs-lookup"><span data-stu-id="d74d9-105">When a fixed asset is reclassified:</span></span>

- <span data-ttu-id="d74d9-106">Visas esošā pamatlīdzekļa grāmatas tiek izveidotas jaunajam pamatlīdzeklim.</span><span class="sxs-lookup"><span data-stu-id="d74d9-106">All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="d74d9-107">Visa sākotnējam pamatlīdzeklim iestatītā informācija tiek kopēta uz jauno pamatlīdzekli.</span><span class="sxs-lookup"><span data-stu-id="d74d9-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="d74d9-108">Grāmatu statuss oriģinālajam pamatlīdzeklim ir Slēgts.</span><span class="sxs-lookup"><span data-stu-id="d74d9-108">The status of the books for the original fixed asset is Closed.</span></span> 

- <span data-ttu-id="d74d9-109">Jaunā pamatlīdzekļa jaunās grāmatas satur pārklasificēšanas datumu laukā **Iegādes datums**.</span><span class="sxs-lookup"><span data-stu-id="d74d9-109">The new books for the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="d74d9-110">Datums laukā **Nolietojuma sākuma datums** tiek kopēts no sākotnējā līdzekļa informācijas.</span><span class="sxs-lookup"><span data-stu-id="d74d9-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="d74d9-111">Ja nolietojums jau ir sākts, tad laukā **Pēdējais nolietojuma aprēķināšanas datums** ir redzams pārklasificēšanas datums.</span><span class="sxs-lookup"><span data-stu-id="d74d9-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

- <span data-ttu-id="d74d9-112">Esošās pamatlīdzekļa transakcijas sākotnējam pamatlīdzeklim tiek atceltas un pārģenerētas jaunajam pamatlīdzeklim.</span><span class="sxs-lookup"><span data-stu-id="d74d9-112">The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

- <span data-ttu-id="d74d9-113">Kad pamatlīdzeklis, kam ir pārsūtīšanas transakcija, tiek pārklasificēts, sistēma **Darbību centrā** parādīs ziņojumu, lai norādītu, ka pārklasificēšanas procesa laikā pārsūtīšanas transakcija netika pabeigta.</span><span class="sxs-lookup"><span data-stu-id="d74d9-113">When an asset that has a transfer transaction has been reclassified, the system will display a message in the **Action center** to indicate that a transfer transaction wasn't completed during the reclassification process.</span></span> <span data-ttu-id="d74d9-114">Jāpabeidz pārsūtīšanas transakcija, lai pārvietotu esošās pārklasificēšanas transakcijas uz atbilstošām finanšu dimensijām.</span><span class="sxs-lookup"><span data-stu-id="d74d9-114">It's necessary to complete a transfer transaction to move the existing reclassification transactions to the appropriate financial dimensions.</span></span> 

   <span data-ttu-id="d74d9-115">Pārklasificēšanas procesa laikā sistēma palaiž šādas darbības, lai pārklasificētu līdzekļu bilanci no sākotnējā pamatlīdzekļa uz jaunu līdzekli.</span><span class="sxs-lookup"><span data-stu-id="d74d9-115">During the reclassification process, the system runs the following actions to reclassify the asset balance from the original asset to the new asset.</span></span> 
   
   - <span data-ttu-id="d74d9-116">Pārklasificēšanas process kopē datus no sākotnējās pamatlīdzekļu grāmatas uz jauno pamatlīdzekļu grāmatu.</span><span class="sxs-lookup"><span data-stu-id="d74d9-116">The reclassification process copies the data from the original fixed asset book to the new fixed asset book.</span></span>

   - <span data-ttu-id="d74d9-117">Pārklasificēšanas transakcija izmanto informāciju no oriģinālās iegrāmatotās iegādes, kas ietver finanšu dimensijas informāciju, kas ir iekļauta iegādes transakcijā.</span><span class="sxs-lookup"><span data-stu-id="d74d9-117">The reclassification transaction uses information from the original posted acquisition that includes financial dimension information that is included in the acquisition transaction.</span></span>  
   
   - <span data-ttu-id="d74d9-118">Tajā pašā laikā pārklasificēšanas process atceļ sākotnējo līdzekļa iegādes un līdzekļa pārsūtīšanas transakciju.</span><span class="sxs-lookup"><span data-stu-id="d74d9-118">At the same time, the reclassification process reverses the original asset acquisition and asset transfer transaction.</span></span> 

<span data-ttu-id="d74d9-119">Šajā diagrammā un procedūrā dots pārklasificēšanas procesa piemērs.</span><span class="sxs-lookup"><span data-stu-id="d74d9-119">The following diagram and procedure provide an example of the reclassification process.</span></span> 

<span data-ttu-id="d74d9-120">[![Diagramma, kas parāda pārklasifikācijas procesu](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)</span><span class="sxs-lookup"><span data-stu-id="d74d9-120">[![Diagram showing the reclassicification process](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)</span></span>

<span data-ttu-id="d74d9-121">Lai pārklasificētu pamatlīdzekli, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="d74d9-121">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="d74d9-122">Dodieties uz **Pamatlīdzekļi > Periodiskie uzdevumi > Pārklasificēšana.**</span><span class="sxs-lookup"><span data-stu-id="d74d9-122">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="d74d9-123">Laukā **Pamatlīdzekļu grupa** atlasiet grupu, ko vēlaties pārklasificēt.</span><span class="sxs-lookup"><span data-stu-id="d74d9-123">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="d74d9-124">Laukā **Pamatlīdzekļa numurs** atlasiet, kuru pamatlīdzekli pārklasificēt.</span><span class="sxs-lookup"><span data-stu-id="d74d9-124">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="d74d9-125">Laukā **Jauna pamatlīdzekļu grupa** atlasiet grupu, uz kuru pārsūtīt šo pamatlīdzekli.</span><span class="sxs-lookup"><span data-stu-id="d74d9-125">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="d74d9-126">Ja jaunā pamatlīdzekļu grupa ir pievienota kādai numuru sērijai, tad lauks **Jauns pamatlīdzekļa numurs** tiek atjaunināts ar numuru no jaunās pamatlīdzekļu grupas numuru sērijas.</span><span class="sxs-lookup"><span data-stu-id="d74d9-126">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="d74d9-127">Pretējā gadījumā lauks **Jauns pamatlīdzekļa numurs** tiek atjaunināts ar numuru no numuru sērijas, kas ir iestatīta lapā **Pamatlīdzekļu parametri**.</span><span class="sxs-lookup"><span data-stu-id="d74d9-127">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="d74d9-128">Ja lapā **Pamatlīdzekļu parametri** nav iestatīta numuru sērija, ievadiet kādu numuru laukā **Jauns pamatlīdzekļa numurs**.</span><span class="sxs-lookup"><span data-stu-id="d74d9-128">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="d74d9-129">Laukā **Pārklasificēšanas datums** ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="d74d9-129">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="d74d9-130">Laukā **Dokumentu sērijas** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d74d9-130">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="d74d9-131">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d74d9-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
