--- 
title: "Pamatlīdzekļu pārklasificēšana"
description: "Lai pārklasificētu pamatlīdzekli, tas ir jāpārsūta uz jaunu pamatlīdzekļu grupu vai tam ir jāpiešķir jauns pamatlīdzekļa numurs tajā pašā grupā."
author: saraschi2
manager: AnnBe
ms.date: 06/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: fda4d71b050edde2752536985b18ebcad203d078
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="748c8-103">Pamatlīdzekļu pārklasificēšana</span><span class="sxs-lookup"><span data-stu-id="748c8-103">Reclassify fixed assets</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="748c8-104">Lai pārklasificētu pamatlīdzekli, tas ir jāpārsūta uz jaunu pamatlīdzekļu grupu vai tam ir jāpiešķir jauns pamatlīdzekļa numurs tajā pašā grupā.</span><span class="sxs-lookup"><span data-stu-id="748c8-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="748c8-105">Kad pamatlīdzeklis ir pārklasificētas:</span><span class="sxs-lookup"><span data-stu-id="748c8-105">When a fixed asset is reclassified:</span></span>

<span data-ttu-id="748c8-106">• Visi esošā pamatlīdzekļa vērtības modeļi tiek izveidoti jaunajam pamatlīdzeklim.</span><span class="sxs-lookup"><span data-stu-id="748c8-106">• All value models for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="748c8-107">Visa sākotnējam pamatlīdzeklim iestatītā informācija tiek kopēta uz jauno pamatlīdzekli.</span><span class="sxs-lookup"><span data-stu-id="748c8-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="748c8-108">Vērtības modeļu statuss oriģinālajam pamatlīdzeklim ir Slēgts.</span><span class="sxs-lookup"><span data-stu-id="748c8-108">The status of the value models for the original fixed asset is Closed.</span></span> 

<span data-ttu-id="748c8-109">• Jaunā pamatlīdzekļa jaunie vērtības modeļi satur pārklasificēšanas datumu laukā Iegādes datums.</span><span class="sxs-lookup"><span data-stu-id="748c8-109">• The new value models of the new fixed asset contain the date of the reclassification in the Acquisition date field.</span></span> <span data-ttu-id="748c8-110">Datums laukā Nolietojuma sākuma datums tiek kopēts no sākotnējā līdzekļa informācijas.</span><span class="sxs-lookup"><span data-stu-id="748c8-110">The date in the Depreciation run date field is copied from the original asset information.</span></span> <span data-ttu-id="748c8-111">Ja nolietojums jau ir sākts, tad laukā Pēdējais nolietojuma aprēķināšanas datums ir redzams pārklasificēšanas datums.</span><span class="sxs-lookup"><span data-stu-id="748c8-111">If the depreciation has already started, the Date when depreciation was last run field displays the date of the reclassification.</span></span> 

<span data-ttu-id="748c8-112">• Esošās pamatlīdzekļa transakcijas sākotnējam pamatlīdzeklim tiek atceltas un pārģenerētas jaunajam pamatlīdzeklim.</span><span class="sxs-lookup"><span data-stu-id="748c8-112">• The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

1. <span data-ttu-id="748c8-113">Dodieties uz Pamatlīdzekļi > Periodiskie uzdevumi > Pārklasificēšana.</span><span class="sxs-lookup"><span data-stu-id="748c8-113">Go to Fixed assets > Periodic tasks > Reclassification.</span></span>
2. <span data-ttu-id="748c8-114">Laukā Pamatlīdzekļu grupa atlasiet grupu, kuru vēlaties pārklasificēt.</span><span class="sxs-lookup"><span data-stu-id="748c8-114">In the Fixed asset group field, selet the group to reclassify.</span></span>
3. <span data-ttu-id="748c8-115">Laukā Pamatlīdzekļa numurs atlasiet, kuru pamatlīdzekli pārklasificēt.</span><span class="sxs-lookup"><span data-stu-id="748c8-115">In the Fixed asset number field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="748c8-116">Laukā Jauna pamatlīdzekļu grupa atlasiet grupu, uz kuru pārsūtīt šo pamatlīdzekli.</span><span class="sxs-lookup"><span data-stu-id="748c8-116">In the New fixed asset group field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="748c8-117">Ja jaunā pamatlīdzekļu grupa ir pievienota kādai numuru sērijai, tad lauks Jauns pamatlīdzekļa numurs tiek atjaunināts ar numuru no jaunās pamatlīdzekļu grupas numuru sērijas.</span><span class="sxs-lookup"><span data-stu-id="748c8-117">If the new fixed asset group is attached to a number sequence, the New fixed asset number field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="748c8-118">Pretējā gadījumā lauks Jauns pamatlīdzekļa numurs tiek atjaunināts ar numuru no numuru sērijas, kas ir iestatīta lapā Pamatlīdzekļu parametri.</span><span class="sxs-lookup"><span data-stu-id="748c8-118">Otherwise, the New fixed asset number field is updated with the number from the number sequence that is set up in the Fixed asset parameters page.</span></span> <span data-ttu-id="748c8-119">Ja lapā Pamatlīdzekļu parametri nav iestatīta numuru sērija, ievadiet kādu numuru laukā Jauns pamatlīdzekļa numurs.</span><span class="sxs-lookup"><span data-stu-id="748c8-119">If a number sequence is not set up in the Fixed asset parameters page, enter a number in the New fixed asset number field.</span></span>  
5. <span data-ttu-id="748c8-120">Laukā Pārklasificēšanas datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="748c8-120">In the Reclassification date field, enter a date.</span></span>
6. <span data-ttu-id="748c8-121">Laukā Dokumentu sērijas ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="748c8-121">In the Voucher series field, enter or select a value.</span></span>
7. <span data-ttu-id="748c8-122">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="748c8-122">Click OK.</span></span>


