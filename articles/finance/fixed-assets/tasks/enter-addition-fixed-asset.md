---
title: Pamatlīdzekļu papildinājuma ievadīšana
description: Šajā procedūrā parādīts, kā pievienot esoša pamatlīdzekļa papildinājumu.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc1e13863ae13daaa641f52f7a55e01fc1353dc1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445603"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a><span data-ttu-id="41326-103">Pamatlīdzekļu papildinājuma ievadīšana</span><span class="sxs-lookup"><span data-stu-id="41326-103">Enter an addition to a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="41326-104">Šajā procedūrā parādīts, kā pievienot esoša pamatlīdzekļa papildinājumu.</span><span class="sxs-lookup"><span data-stu-id="41326-104">This procedure shows how to add an addition to an existing fixed asset.</span></span> <span data-ttu-id="41326-105">Pamatlīdzekļu papildinājumu mērķis ir izsekot krājumu papildinājumus, apkopi vai līdzekļa uzlabošanu, un tiem ir tikai informatīvs raksturs.</span><span class="sxs-lookup"><span data-stu-id="41326-105">The purpose of Fixed asset additions is to track item additions, maintenance, or improvements for an asset, and is informational only.</span></span> <span data-ttu-id="41326-106">Jebkuras pamatlīdzekļa vērtības vai lietošanas ilguma izmaiņas ir jāveic atsevišķi.</span><span class="sxs-lookup"><span data-stu-id="41326-106">Any changes to the fixed asset value or service life must be made separately.</span></span>   

<span data-ttu-id="41326-107">Šī procedūra izmanto grāmatveža lomu un demonstrācijas datus USMF juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="41326-107">The procedure uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="41326-108">Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Pamatlīdzekļi > Pamatlīdzekļi > Pamatlīdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="41326-108">In the Navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="41326-109">Sarakstā atrodiet un atlasiet papildināmo pamatlīdzekli.</span><span class="sxs-lookup"><span data-stu-id="41326-109">In the list, find and select the fixed asset for the addition.</span></span>
3. <span data-ttu-id="41326-110">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="41326-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="41326-111">Darbību rūtī noklikšķiniet uz **Pamatlīdzeklis**.</span><span class="sxs-lookup"><span data-stu-id="41326-111">On the Action Pane, click **Fixed asset**.</span></span>
5. <span data-ttu-id="41326-112">Noklikšķiniet uz **Pamatlīdzekļu papildinājumi**.</span><span class="sxs-lookup"><span data-stu-id="41326-112">Click **Fixed asset additions**.</span></span>
6. <span data-ttu-id="41326-113">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="41326-113">Click **New**.</span></span>
7. <span data-ttu-id="41326-114">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="41326-114">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="41326-115">Laukā **Iegādes datums** iestatiet papildu pirkuma vai pakalpojuma datumu.</span><span class="sxs-lookup"><span data-stu-id="41326-115">In the **Acquisition date** field, set the date of the addition purchase or service.</span></span>
9. <span data-ttu-id="41326-116">Laukā **Vienības izmaksas** ievadiet krājuma, apkopes vai cita līdzekļa uzlabojuma izmaksas.</span><span class="sxs-lookup"><span data-stu-id="41326-116">In the **Unit cost** field, enter the cost of the item, maintenance, or other improvement for the asset.</span></span>
10. <span data-ttu-id="41326-117">Laukā **Daudzums** ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="41326-117">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="41326-118">Kopējās izmaksas neietekmēs pamatlīdzekļa vērtību un ir paredzētas tikai izsekošanas un informatīviem nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="41326-118">The total cost will have no impact on the value of the fixed asset and is for tracking and informational purposes only.</span></span> <span data-ttu-id="41326-119">Ja izmaksas tiks kapitalizētas, vērtības palielināšanas transakcija ir jāgrāmato atsevišķi.</span><span class="sxs-lookup"><span data-stu-id="41326-119">If the cost will be capitalized, then a write-up adjustment transaction must be posted separately.</span></span>  
11. <span data-ttu-id="41326-120">Noklikšķiniet uz cilnes **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="41326-120">Click the **General** tab.</span></span>

    * <span data-ttu-id="41326-121">Ja papildinājums paildzina līdzekļa lietošanas ilgumu, iestatiet **Palielina lietošanas ilgumu** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="41326-121">Set **Increases service life** to **Yes** if the addition increases the service life of the asset.</span></span>  
    * <span data-ttu-id="41326-122">Šim laukam ir tikai informatīvs raksturs.</span><span class="sxs-lookup"><span data-stu-id="41326-122">This field is informational only.</span></span> <span data-ttu-id="41326-123">Lai palielinātu līdzekļa lietošanas ilgumu, mainiet lietošanas ilgumu vērtību modeļos un/vai nolietojuma grāmatās.</span><span class="sxs-lookup"><span data-stu-id="41326-123">To increase the service life, modify the Service life on the Value models and/or Depreciation books for the asset.</span></span>  

