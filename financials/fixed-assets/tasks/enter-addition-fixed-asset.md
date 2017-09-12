--- 
title: "Pamatlīdzekļu papildinājuma ievadīšana"
description: "Šajā procedūrā parādīts, kā pievienot esoša pamatlīdzekļa papildinājumu."
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4c22fb105d0deedda1b7dbfdd919d1745ad0ca2f
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="enter-an-addition-to-a-fixed-asset"></a><span data-ttu-id="cf23d-103">Pamatlīdzekļu papildinājuma ievadīšana</span><span class="sxs-lookup"><span data-stu-id="cf23d-103">Enter an addition to a fixed asset</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cf23d-104">Šajā procedūrā parādīts, kā pievienot esoša pamatlīdzekļa papildinājumu.</span><span class="sxs-lookup"><span data-stu-id="cf23d-104">This procedure shows how to add an addition to an existing fixed asset.</span></span> <span data-ttu-id="cf23d-105">Pamatlīdzekļu papildinājumu mērķis ir izsekot krājumu papildinājumus, apkopi vai līdzekļa uzlabošanu, un tiem ir tikai informatīvs raksturs.</span><span class="sxs-lookup"><span data-stu-id="cf23d-105">The purpose of Fixed asset additions is to track item additions, maintenance, or improvements for an asset, and is informational only.</span></span> <span data-ttu-id="cf23d-106">Jebkuras pamatlīdzekļa vērtības vai lietošanas ilguma izmaiņas ir jāveic atsevišķi.</span><span class="sxs-lookup"><span data-stu-id="cf23d-106">Any changes to the fixed asset value or service life must be made separately.</span></span>   



<span data-ttu-id="cf23d-107">Šī procedūra izmanto grāmatveža lomu un demonstrācijas datus USMF juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="cf23d-107">The procedure uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="cf23d-108">Pārejiet uz sadaļu Pamatlīdzekļi > Pamatlīdzekļi > Pamatlīdzekļi.</span><span class="sxs-lookup"><span data-stu-id="cf23d-108">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="cf23d-109">Sarakstā atrodiet un atlasiet papildināmo pamatlīdzekli.</span><span class="sxs-lookup"><span data-stu-id="cf23d-109">In the list, find and select the fixed asset for the addition.</span></span>
3. <span data-ttu-id="cf23d-110">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="cf23d-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="cf23d-111">Darbību rūtī noklikšķiniet uz Pamatlīdzeklis.</span><span class="sxs-lookup"><span data-stu-id="cf23d-111">On the Action Pane, click Fixed asset.</span></span>
5. <span data-ttu-id="cf23d-112">Noklikšķiniet uz Pamatlīdzekļu papildinājumi.</span><span class="sxs-lookup"><span data-stu-id="cf23d-112">Click Fixed asset additions.</span></span>
6. <span data-ttu-id="cf23d-113">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="cf23d-113">Click New.</span></span>
7. <span data-ttu-id="cf23d-114">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cf23d-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="cf23d-115">Iestatiet papildinājuma pirkuma vai pakalpojuma datumu.</span><span class="sxs-lookup"><span data-stu-id="cf23d-115">Set the date of the addition purchase or service.</span></span>
9. <span data-ttu-id="cf23d-116">Ievadiet krājuma, apkopes vai cita līdzekļa uzlabojuma izmaksas.</span><span class="sxs-lookup"><span data-stu-id="cf23d-116">Enter the cost of the item, maintenance, or other improvement for the asset.</span></span>
10. <span data-ttu-id="cf23d-117">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="cf23d-117">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="cf23d-118">Kopējās izmaksas neietekmēs pamatlīdzekļa vērtību un ir paredzētas tikai izsekošanas un informatīviem nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="cf23d-118">The total cost will have no impact on the value of the fixed asset and is for tracking and informational purposes only.</span></span> <span data-ttu-id="cf23d-119">Ja izmaksas tiks kapitalizētas, vērtības palielināšanas transakcija ir jāgrāmato atsevišķi.</span><span class="sxs-lookup"><span data-stu-id="cf23d-119">If the cost will be capitalized, then a write-up adjustment transaction must be posted separately.</span></span>  
11. <span data-ttu-id="cf23d-120">Noklikšķiniet uz cilnes Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="cf23d-120">Click the General tab.</span></span>
    * <span data-ttu-id="cf23d-121">Ja papildinājums paildzina līdzekļa lietošanas ilgumu, iestatiet Palielina lietošanas ilgumu.</span><span class="sxs-lookup"><span data-stu-id="cf23d-121">Set Increases service life if the addition increases the service life of the asset.</span></span>  
    * <span data-ttu-id="cf23d-122">Šim laukam ir tikai informatīvs raksturs.</span><span class="sxs-lookup"><span data-stu-id="cf23d-122">This field is informational only.</span></span> <span data-ttu-id="cf23d-123">Lai palielinātu līdzekļa lietošanas ilgumu, mainiet lietošanas ilgumu vērtību modeļos un/vai nolietojuma grāmatās.</span><span class="sxs-lookup"><span data-stu-id="cf23d-123">To increase the service life, modify the Service life on the Value models and/or Depreciation books for the asset.</span></span>  


