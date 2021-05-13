---
title: Operācijas neatbilstībai
description: Šajā tēmā aprakstīts, kā izveidot un izmantot neatbilstības operācijas.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6454a56323ea66369696dd6e3310a41b4eb9ee58
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956750"
---
# <a name="operations-for-nonconformances"></a><span data-ttu-id="5e1eb-103">Operācijas neatbilstībai</span><span class="sxs-lookup"><span data-stu-id="5e1eb-103">Operations for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e1eb-104">Šajā tēmā aprakstīts, kā izveidot un izmantot neatbilstības operācijas.</span><span class="sxs-lookup"><span data-stu-id="5e1eb-104">This topic describes how to create and use operations for nonconformances.</span></span>

<span data-ttu-id="5e1eb-105">Var izmantot lapu **Operācijas**, lai definētu klasifikācijas darbam, ko var veikt apstiprinātajai neatbilstībai.</span><span class="sxs-lookup"><span data-stu-id="5e1eb-105">You can use the **Operations** page to define classifications of the work that can be performed for an approved nonconformance.</span></span> <span data-ttu-id="5e1eb-106">Ja neatbilstībai piešķirat saistīto operāciju, varat nodrošināt detalizētu informāciju, piemēram, par saistīto materiālu, darba stundām un maksām, kas nepieciešamas operācijas izpildē.</span><span class="sxs-lookup"><span data-stu-id="5e1eb-106">When you assign a related operation to a nonconformance, you can provide details such as the associated material, labor hours, and charges that are required to do the operation.</span></span> <span data-ttu-id="5e1eb-107">Sistēma izmanto šo informāciju, lai operācijai aprēķinātu novērtētās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="5e1eb-107">The system uses this information to calculate an estimated cost for the operation.</span></span> <span data-ttu-id="5e1eb-108">Detalizētā informācija un novērtētās izmaksas tiek nodrošinātas tikai atsauces nolūkā.</span><span class="sxs-lookup"><span data-stu-id="5e1eb-108">The detailed information and estimated costs are for reference.</span></span> <span data-ttu-id="5e1eb-109">Kvalitātes saistītās operācijas ir atšķirīgas no operācijām, ko var definēt ražošanas maršrutā.</span><span class="sxs-lookup"><span data-stu-id="5e1eb-109">The related operations for quality differ from the operations that can be defined for a production route.</span></span>

> [!NOTE]
> <span data-ttu-id="5e1eb-110">Lai gan jūs varat izsekot izmaksas, laiku un krājumus, kas tiek izmantoti operācijā, kas saistīta ar neatbilstību, jūsu ievadītie dati ir tikai informatīvi.</span><span class="sxs-lookup"><span data-stu-id="5e1eb-110">Although you can track costs, time, and the items that are used in an operation that is related to a nonconformance, the data that you enter is only informational.</span></span> <span data-ttu-id="5e1eb-111">Tas nav automātiski integrēts ar Virsgrāmatu, krājumu apakšgrāmatu vai moduli **Laiks un apmeklētība**.</span><span class="sxs-lookup"><span data-stu-id="5e1eb-111">It isn't automatically integrated with the general ledger, inventory subledger, or the **Time and attendance** module.</span></span>

## <a name="examples-of-operations"></a><span data-ttu-id="5e1eb-112">Operāciju piemēri</span><span class="sxs-lookup"><span data-stu-id="5e1eb-112">Examples of operations</span></span>

<span data-ttu-id="5e1eb-113">Jūs strādājat ražošanas uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="5e1eb-113">You work for a manufacturing company.</span></span> <span data-ttu-id="5e1eb-114">Krājumiem, kam neizdevās kvalitātes tests, tika izveidota un apstiprināta neatbilstība.</span><span class="sxs-lookup"><span data-stu-id="5e1eb-114">A nonconformance was created and approved for items that failed a quality test.</span></span> <span data-ttu-id="5e1eb-115">Labojums tika izveidots, lai norādītu, ka problēma tika saistīta ar slikto gultni iekārtā.</span><span class="sxs-lookup"><span data-stu-id="5e1eb-115">A correction was created to indicate that the problem was related to a bad bearing on a machine.</span></span> <span data-ttu-id="5e1eb-116">Lai nomainītu gultni, nepieciešamas vairākas darbības, un tiek izsekota atbildība par katru operāciju.</span><span class="sxs-lookup"><span data-stu-id="5e1eb-116">Several steps are required to replace the bearing, and the responsibility for each operation is tracked.</span></span> <span data-ttu-id="5e1eb-117">Piemēram, var būt nepieciešamas šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="5e1eb-117">For example, the following steps might be required:</span></span>

1. <span data-ttu-id="5e1eb-118">Ražošanas rinda tiek apturēta, un tiek veikta tīrīšanas rutīna.</span><span class="sxs-lookup"><span data-stu-id="5e1eb-118">The production line is stopped, and the clean-out routine is performed.</span></span>
1. <span data-ttu-id="5e1eb-119">Uzturēšanas personāls nomaina gultni.</span><span class="sxs-lookup"><span data-stu-id="5e1eb-119">Maintenance personnel replace the bearing.</span></span>
1. <span data-ttu-id="5e1eb-120">Kvalitātes nodrošināšanas personāls pārbauda iekārtu, pirms tā tiek atkal ieslēgta.</span><span class="sxs-lookup"><span data-stu-id="5e1eb-120">Quality assurance personnel inspect the machine before it's turned back on.</span></span>

<span data-ttu-id="5e1eb-121">Šajā piemērā var veidot šādas operācijas, lai attēlotu darbu, kas jāveic:</span><span class="sxs-lookup"><span data-stu-id="5e1eb-121">For this example, the following operations can be created to represent the work that must be done:</span></span>

- <span data-ttu-id="5e1eb-122">Apturēt ražošanas rindu.</span><span class="sxs-lookup"><span data-stu-id="5e1eb-122">Stop the production line.</span></span>
- <span data-ttu-id="5e1eb-123">Iztīrīt ražošanas rindu.</span><span class="sxs-lookup"><span data-stu-id="5e1eb-123">Clean out the production line.</span></span>
- <span data-ttu-id="5e1eb-124">Veikt iekārtas uzturēšanu.</span><span class="sxs-lookup"><span data-stu-id="5e1eb-124">Perform machine maintenance.</span></span>
- <span data-ttu-id="5e1eb-125">Pārbaudīt iekārtu.</span><span class="sxs-lookup"><span data-stu-id="5e1eb-125">Inspect the machine.</span></span>

## <a name="create-an-operation"></a><span data-ttu-id="5e1eb-126">Operācijas izveide</span><span class="sxs-lookup"><span data-stu-id="5e1eb-126">Create an operation</span></span>

1. <span data-ttu-id="5e1eb-127">Dodieties uz **Krājumu vadība \> Iestatīšana \> Kvalitātes pārvaldība \> Operācijas**.</span><span class="sxs-lookup"><span data-stu-id="5e1eb-127">Go to **Inventory management \> Setup \> Quality management \> Operations**.</span></span>
1. <span data-ttu-id="5e1eb-128">Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5e1eb-128">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="5e1eb-129">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="5e1eb-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5e1eb-130">**Operācija** - ievadiet operācijas unikālo ID vai nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="5e1eb-130">**Operation** – Enter a unique ID or name for the operation.</span></span>
    - <span data-ttu-id="5e1eb-131">**Apraksts** — ievadiet operācijas detālizēto aprakstu.</span><span class="sxs-lookup"><span data-stu-id="5e1eb-131">**Description** – Enter a detailed description of the operation.</span></span>
    - <span data-ttu-id="5e1eb-132">**Tips**– Ja operāciju var izmantot tikai ar neatbilstībām, kas attiecas uz noteiktu pasūtījuma tipu, atlasiet pasūtījuma tipu (*Pirkšanas pasūtījums* vai *Pārdošanas pasūtījums*).</span><span class="sxs-lookup"><span data-stu-id="5e1eb-132">**Type** – If the operation can be used only with nonconformances that are related to a specific type of order, select the order type (*Purchase order* or *Sales order*).</span></span>

1. <span data-ttu-id="5e1eb-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5e1eb-133">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5e1eb-134">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="5e1eb-134">Additional resources</span></span>

- [<span data-ttu-id="5e1eb-135">Kvalitātes pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="5e1eb-135">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="5e1eb-136">Iespējot kvalitātes un neatbilstības pārvaldību</span><span class="sxs-lookup"><span data-stu-id="5e1eb-136">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="5e1eb-137">Neatbilstības izveide un apstrāde</span><span class="sxs-lookup"><span data-stu-id="5e1eb-137">Create and process nonconformances</span></span>](tasks/create-process-non-conformance.md)
- [<span data-ttu-id="5e1eb-138">Par neatbilstību apstiprināšanu atbildīgie darbinieki</span><span class="sxs-lookup"><span data-stu-id="5e1eb-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="5e1eb-139">Karantīnas zonas neatbilstībai</span><span class="sxs-lookup"><span data-stu-id="5e1eb-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="5e1eb-140">Neatbilstību diagnostikas tipi</span><span class="sxs-lookup"><span data-stu-id="5e1eb-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="5e1eb-141">Kvalitātes maksa par neatbilstībām</span><span class="sxs-lookup"><span data-stu-id="5e1eb-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="5e1eb-142">Neatbilstību problēmu tipi</span><span class="sxs-lookup"><span data-stu-id="5e1eb-142">Problem types for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="5e1eb-143">Kvalitātes pārvaldība noliktavas procesiem</span><span class="sxs-lookup"><span data-stu-id="5e1eb-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
