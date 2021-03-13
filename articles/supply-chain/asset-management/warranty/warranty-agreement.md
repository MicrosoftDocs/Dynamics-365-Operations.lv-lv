---
title: Garantijas līgumi
description: Šajā tēmā ir aprakstīti garantijas līgumi līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7080af2059c9c9bcdd11ca0ee9c5e339cef69302
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021508"
---
# <a name="warranty-agreements"></a><span data-ttu-id="37a1a-103">Garantijas līgumi</span><span class="sxs-lookup"><span data-stu-id="37a1a-103">Warranty agreements</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="37a1a-104">Līdzekļu pārvaldībā varat iestatīt garantijas nosacījumus, ko var pievienot līdzeklim vai līdzekļu tipam.</span><span class="sxs-lookup"><span data-stu-id="37a1a-104">In Asset Management, you can set up warranty terms that can be connected to an asset or an asset type.</span></span> <span data-ttu-id="37a1a-105">Garantijas nosacījumi tiek veidoti noteiktam periodam.</span><span class="sxs-lookup"><span data-stu-id="37a1a-105">Warranty terms are created for a specific period.</span></span> <span data-ttu-id="37a1a-106">Garantiju var iestatīt, lai nodrošinātu pilnīgu nodrošinājumu vai daļēju nodrošinājumu, un varat iestatīt nosacījumus, kas ir saistīti ar stundām, izdevumiem un krājumiem.</span><span class="sxs-lookup"><span data-stu-id="37a1a-106">Warranty can be set up to provide full coverage or partial coverage, and you can set up terms that are related to hours, expenses, and items.</span></span>

<span data-ttu-id="37a1a-107">Pirmā darbība ir izveidot kreditora garantijas līgumus, kas ir jūsu aprīkojumam.</span><span class="sxs-lookup"><span data-stu-id="37a1a-107">The first step is to create any vendor warranty agreements that you have for your equipment.</span></span> <span data-ttu-id="37a1a-108">Pēc tam varat pievienot garantijas līgumus līdzekļiem vai līdzekļu veidiem.</span><span class="sxs-lookup"><span data-stu-id="37a1a-108">You then attach warranty agreements to assets or asset types.</span></span> <span data-ttu-id="37a1a-109">Kreditora garantijas līgumus izmanto tikai informatīviem nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="37a1a-109">Vendor warranty agreements are used only for informational purposes.</span></span> <span data-ttu-id="37a1a-110">Ja līdzeklim ir iestatīta kreditora garantija, varat apskatīt līdzekļa garantijas nodrošinājuma periodu.</span><span class="sxs-lookup"><span data-stu-id="37a1a-110">If vendor warranty is set up on an asset, you can see the warranty coverage period on the asset.</span></span>

## <a name="create-a-warranty-agreement"></a><span data-ttu-id="37a1a-111">Garantijas līguma izveide</span><span class="sxs-lookup"><span data-stu-id="37a1a-111">Create a warranty agreement</span></span>

<span data-ttu-id="37a1a-112">Garantijas līgumā var iekļaut vairākas līguma rindas, lai segtu darba stundu, izdevumu un krājumu garantijas.</span><span class="sxs-lookup"><span data-stu-id="37a1a-112">A warranty agreement can include several agreement lines to cover the warranty for work hours, expenses, and items.</span></span>

1. <span data-ttu-id="37a1a-113">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļi** \> **Garantija**.</span><span class="sxs-lookup"><span data-stu-id="37a1a-113">Select **Asset management** \> **Setup** \> **Assets** \> **Warranty**.</span></span>
2. <span data-ttu-id="37a1a-114">Atlasiet **Jauns**, lai izveidotu preci.</span><span class="sxs-lookup"><span data-stu-id="37a1a-114">Select **New** to create a product.</span></span>
3. <span data-ttu-id="37a1a-115">Ievadiet garantijas ID laukā **Garantija**.</span><span class="sxs-lookup"><span data-stu-id="37a1a-115">In the **Warranty** field, enter a warranty ID.</span></span> 
4. <span data-ttu-id="37a1a-116">Laukā **Nosaukums** ievadiet aprakstu.</span><span class="sxs-lookup"><span data-stu-id="37a1a-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="37a1a-117">Kopsavilkuma cilnes **Detalizēta informācija** lauks **Līdzekļi** parāda aktīvo līdzekļu skaitu, kas izmanto garantijas līgumu.</span><span class="sxs-lookup"><span data-stu-id="37a1a-117">On the **Details** FastTab, the **Assets** field shows the number of active assets that use the warranty agreement.</span></span>

5. <span data-ttu-id="37a1a-118">Kopsavilkuma cilnē **Garantijas rindas** veiciet šīs darbības, lai pievienotu rindas, kas jāiekļauj garantijas līgumā:</span><span class="sxs-lookup"><span data-stu-id="37a1a-118">On the **Warranty lines** FastTab, follow these steps to add lines that should be included in a warranty agreement:</span></span>

    1. <span data-ttu-id="37a1a-119">Atlasiet **Pievienot rindu**, lai pievienotu jaunu nosacījumu garantijai.</span><span class="sxs-lookup"><span data-stu-id="37a1a-119">Select **Add line** to add a new condition to the warranty.</span></span> <span data-ttu-id="37a1a-120">Laukā **Rinda** automātiski tiek ievadīts kārtas numurs.</span><span class="sxs-lookup"><span data-stu-id="37a1a-120">A sequential line number is automatically entered in the **Line** field.</span></span>
    2. <span data-ttu-id="37a1a-121">Laukā **Periods** atlasiet garantijas perioda veidu.</span><span class="sxs-lookup"><span data-stu-id="37a1a-121">In the **Period** field, select the type of warranty period.</span></span>
    3. <span data-ttu-id="37a1a-122">Ievadiet skaitli laukā **Intervāls**.</span><span class="sxs-lookup"><span data-stu-id="37a1a-122">In the **Interval** field, enter a number.</span></span> <span data-ttu-id="37a1a-123">Šis lauks nosaka periodu skaitu, kuru laikā garantija ir spēkā.</span><span class="sxs-lookup"><span data-stu-id="37a1a-123">This field defines the number of periods that the warranty should be valid for.</span></span>
    4. <span data-ttu-id="37a1a-124">Laukā **Procenti** ievadiet nodrošinājuma procentuālo vērtību garantijas rindai.</span><span class="sxs-lookup"><span data-stu-id="37a1a-124">In the **Percent** field, enter the coverage percentage for the warranty line.</span></span> <span data-ttu-id="37a1a-125">Procenti norāda, cik daudz jūsu uzņēmums sedz.</span><span class="sxs-lookup"><span data-stu-id="37a1a-125">The percentage indicates how much is covered by your company.</span></span>

![Garantijas lapa](media/01-warranty.png)
