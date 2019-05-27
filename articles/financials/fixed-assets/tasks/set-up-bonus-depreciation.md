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
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6bbd6b78d05fcc9d95f6e6409db2619a210ad760
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571717"
---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="dfe83-103">Prēmijas nolietojuma iestatīšana</span><span class="sxs-lookup"><span data-stu-id="dfe83-103">Set up bonus depreciation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dfe83-104">Šajā procedūrā parādīts, kā izveidot speciālā nolietojuma atļauto daudzumu, un sasaistīt to ar pamatlīdzekļu grāmatu.</span><span class="sxs-lookup"><span data-stu-id="dfe83-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="dfe83-105">Tas izmanto grāmatveža lomu un demonstrācijas datus USMF juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="dfe83-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="dfe83-106">Speciālā nolietojuma atļautā daudzuma izveide</span><span class="sxs-lookup"><span data-stu-id="dfe83-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="dfe83-107">Pārejiet uz sadaļu Pamatlīdzekļi > Iestatījumi > Speciālā nolietojuma atļautais daudzums.</span><span class="sxs-lookup"><span data-stu-id="dfe83-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="dfe83-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="dfe83-108">Click New.</span></span>
3. <span data-ttu-id="dfe83-109">Ievadiet vērtību laukā Speciālā nolietojuma atļautais daudzums.</span><span class="sxs-lookup"><span data-stu-id="dfe83-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="dfe83-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="dfe83-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="dfe83-111">Ievadiet skaitli laukā Procenti.</span><span class="sxs-lookup"><span data-stu-id="dfe83-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="dfe83-112">Ja procentuālā daļa nav norādīta, norādiet summu.</span><span class="sxs-lookup"><span data-stu-id="dfe83-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="dfe83-113">Speciālā nolietojuma atļautā daudzuma sasaiste ar pamatlīdzekļu grupas grāmatu</span><span class="sxs-lookup"><span data-stu-id="dfe83-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="dfe83-114">Pārejiet uz sadaļu Pamatlīdzekļi > Iestatījumi > Pamatlīdzekļu grupas.</span><span class="sxs-lookup"><span data-stu-id="dfe83-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="dfe83-115">Sarakstā atlasiet pamatlīdzekļu grupu, kura saistīta ar speciālā nolietojuma atļauto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="dfe83-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="dfe83-116">Noklikšķiniet uz Grāmatas.</span><span class="sxs-lookup"><span data-stu-id="dfe83-116">Click Books.</span></span>
4. <span data-ttu-id="dfe83-117">Sarakstā atlasiet grāmatu, kas ir saistīta ar speciālā nolietojuma atļauto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="dfe83-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="dfe83-118">Noklikšķiniet uz Speciālā nolietojuma atļautais daudzums.</span><span class="sxs-lookup"><span data-stu-id="dfe83-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="dfe83-119">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="dfe83-119">Click New.</span></span>
7. <span data-ttu-id="dfe83-120">Laukā Speciālā nolietojuma atļautais daudzums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="dfe83-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="dfe83-121">Procentuālā daļa vai summa pēc noklusējuma tiek ņemta no speciālā nolietojuma atļautā daudzuma iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="dfe83-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="dfe83-122">Laukā Prioritāte ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="dfe83-122">In the Priority field, enter a number.</span></span>

