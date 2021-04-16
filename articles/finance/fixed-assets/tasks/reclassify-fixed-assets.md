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
ms.openlocfilehash: 8935213c4629de408a48df5e54a2122324e1b3e7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823936"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="1d38e-103">Pamatlīdzekļu pārklasificēšana</span><span class="sxs-lookup"><span data-stu-id="1d38e-103">Reclassify fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1d38e-104">Lai pārklasificētu pamatlīdzekli, tas ir jāpārsūta uz jaunu pamatlīdzekļu grupu vai tam ir jāpiešķir jauns pamatlīdzekļa numurs tajā pašā grupā.</span><span class="sxs-lookup"><span data-stu-id="1d38e-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="1d38e-105">Kad pamatlīdzeklis ir pārklasificētas:</span><span class="sxs-lookup"><span data-stu-id="1d38e-105">When a fixed asset is reclassified:</span></span>

* <span data-ttu-id="1d38e-106">Visas esošā pamatlīdzekļa grāmatas tiek izveidotas jaunajam pamatlīdzeklim.</span><span class="sxs-lookup"><span data-stu-id="1d38e-106">All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="1d38e-107">Visa sākotnējam pamatlīdzeklim iestatītā informācija tiek kopēta uz jauno pamatlīdzekli.</span><span class="sxs-lookup"><span data-stu-id="1d38e-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="1d38e-108">Grāmatu statuss oriģinālajam pamatlīdzeklim ir Slēgts.</span><span class="sxs-lookup"><span data-stu-id="1d38e-108">The status of the books for the original fixed asset is Closed.</span></span> 

* <span data-ttu-id="1d38e-109">Jaunā pamatlīdzekļa jaunās grāmatas satur pārklasificēšanas datumu laukā **Iegādes datums**.</span><span class="sxs-lookup"><span data-stu-id="1d38e-109">The new books of the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="1d38e-110">Datums laukā **Nolietojuma sākuma datums** tiek kopēts no sākotnējā līdzekļa informācijas.</span><span class="sxs-lookup"><span data-stu-id="1d38e-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="1d38e-111">Ja nolietojums jau ir sākts, tad laukā **Pēdējais nolietojuma aprēķināšanas datums** ir redzams pārklasificēšanas datums.</span><span class="sxs-lookup"><span data-stu-id="1d38e-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

* <span data-ttu-id="1d38e-112">Esošās pamatlīdzekļa transakcijas sākotnējam pamatlīdzeklim tiek atceltas un pārģenerētas jaunajam pamatlīdzeklim.</span><span class="sxs-lookup"><span data-stu-id="1d38e-112">The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

<span data-ttu-id="1d38e-113">Lai pārklasificētu pamatlīdzekli, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="1d38e-113">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="1d38e-114">Dodieties uz **Pamatlīdzekļi > Periodiskie uzdevumi > Pārklasificēšana.**</span><span class="sxs-lookup"><span data-stu-id="1d38e-114">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="1d38e-115">Laukā **Pamatlīdzekļu grupa** atlasiet grupu, ko vēlaties pārklasificēt.</span><span class="sxs-lookup"><span data-stu-id="1d38e-115">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="1d38e-116">Laukā **Pamatlīdzekļa numurs** atlasiet, kuru pamatlīdzekli pārklasificēt.</span><span class="sxs-lookup"><span data-stu-id="1d38e-116">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="1d38e-117">Laukā **Jauna pamatlīdzekļu grupa** atlasiet grupu, uz kuru pārsūtīt šo pamatlīdzekli.</span><span class="sxs-lookup"><span data-stu-id="1d38e-117">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="1d38e-118">Ja jaunā pamatlīdzekļu grupa ir pievienota kādai numuru sērijai, tad lauks **Jauns pamatlīdzekļa numurs** tiek atjaunināts ar numuru no jaunās pamatlīdzekļu grupas numuru sērijas.</span><span class="sxs-lookup"><span data-stu-id="1d38e-118">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="1d38e-119">Pretējā gadījumā lauks **Jauns pamatlīdzekļa numurs** tiek atjaunināts ar numuru no numuru sērijas, kas ir iestatīta lapā **Pamatlīdzekļu parametri**.</span><span class="sxs-lookup"><span data-stu-id="1d38e-119">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="1d38e-120">Ja lapā **Pamatlīdzekļu parametri** nav iestatīta numuru sērija, ievadiet kādu numuru laukā **Jauns pamatlīdzekļa numurs**.</span><span class="sxs-lookup"><span data-stu-id="1d38e-120">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="1d38e-121">Laukā **Pārklasificēšanas datums** ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="1d38e-121">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="1d38e-122">Laukā **Dokumentu sērijas** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1d38e-122">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="1d38e-123">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1d38e-123">Click **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]