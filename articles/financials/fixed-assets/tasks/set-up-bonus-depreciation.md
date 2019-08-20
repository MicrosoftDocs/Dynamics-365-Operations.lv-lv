---
title: Prēmijas nolietojuma iestatīšana
description: Šajā procedūrā parādīts, kā izveidot speciālā nolietojuma atļauto daudzumu, un sasaistīt to ar pamatlīdzekļu grāmatu.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 788cddf4d822fe3d3d6a33e83d7b30f32f4b6b9c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839885"
---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="0dfeb-103">Prēmijas nolietojuma iestatīšana</span><span class="sxs-lookup"><span data-stu-id="0dfeb-103">Set up bonus depreciation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0dfeb-104">Šajā procedūrā parādīts, kā izveidot speciālā nolietojuma atļauto daudzumu, un sasaistīt to ar pamatlīdzekļu grāmatu.</span><span class="sxs-lookup"><span data-stu-id="0dfeb-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="0dfeb-105">Tas izmanto grāmatveža lomu un demonstrācijas datus USMF juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="0dfeb-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="0dfeb-106">Speciālā nolietojuma atļautā daudzuma izveide</span><span class="sxs-lookup"><span data-stu-id="0dfeb-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="0dfeb-107">Pārejiet uz sadaļu Pamatlīdzekļi > Iestatījumi > Speciālā nolietojuma atļautais daudzums.</span><span class="sxs-lookup"><span data-stu-id="0dfeb-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="0dfeb-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="0dfeb-108">Click New.</span></span>
3. <span data-ttu-id="0dfeb-109">Ievadiet vērtību laukā Speciālā nolietojuma atļautais daudzums.</span><span class="sxs-lookup"><span data-stu-id="0dfeb-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="0dfeb-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="0dfeb-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0dfeb-111">Ievadiet skaitli laukā Procenti.</span><span class="sxs-lookup"><span data-stu-id="0dfeb-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="0dfeb-112">Ja procentuālā daļa nav norādīta, norādiet summu.</span><span class="sxs-lookup"><span data-stu-id="0dfeb-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="0dfeb-113">Speciālā nolietojuma atļautā daudzuma sasaiste ar pamatlīdzekļu grupas grāmatu</span><span class="sxs-lookup"><span data-stu-id="0dfeb-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="0dfeb-114">Pārejiet uz sadaļu Pamatlīdzekļi > Iestatījumi > Pamatlīdzekļu grupas.</span><span class="sxs-lookup"><span data-stu-id="0dfeb-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="0dfeb-115">Sarakstā atlasiet pamatlīdzekļu grupu, kura saistīta ar speciālā nolietojuma atļauto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="0dfeb-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="0dfeb-116">Noklikšķiniet uz Grāmatas.</span><span class="sxs-lookup"><span data-stu-id="0dfeb-116">Click Books.</span></span>
4. <span data-ttu-id="0dfeb-117">Sarakstā atlasiet grāmatu, kas ir saistīta ar speciālā nolietojuma atļauto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="0dfeb-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="0dfeb-118">Noklikšķiniet uz Speciālā nolietojuma atļautais daudzums.</span><span class="sxs-lookup"><span data-stu-id="0dfeb-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="0dfeb-119">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="0dfeb-119">Click New.</span></span>
7. <span data-ttu-id="0dfeb-120">Laukā Speciālā nolietojuma atļautais daudzums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0dfeb-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="0dfeb-121">Procentuālā daļa vai summa pēc noklusējuma tiek ņemta no speciālā nolietojuma atļautā daudzuma iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="0dfeb-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="0dfeb-122">Laukā Prioritāte ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="0dfeb-122">In the Priority field, enter a number.</span></span>

