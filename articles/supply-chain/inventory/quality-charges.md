---
title: Maksa par neatbilstības operācijam
description: Šajā tēmā ir aprakstīts, kā izveidot kvalitātes maksas, ko var izmantot operācijām neatbilstībai.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfa424e94048aa9eb1ce4da9aa69e8d4df71cefb
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956742"
---
# <a name="charges-for-nonconformance-operations"></a><span data-ttu-id="afeaa-103">Maksa par neatbilstības operācijam</span><span class="sxs-lookup"><span data-stu-id="afeaa-103">Charges for nonconformance operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="afeaa-104">Šajā tēmā ir aprakstīts, kā izveidot kvalitātes maksas, ko var izmantot operācijām neatbilstībai.</span><span class="sxs-lookup"><span data-stu-id="afeaa-104">This topic describes how to create quality charges that can be used with operations for a nonconformance.</span></span>

<span data-ttu-id="afeaa-105">Izmantojiet lapu **Kvalitātes maksas**, lai definētu maksu veidus, kas var pievienot operācijām neatbilstībām.</span><span class="sxs-lookup"><span data-stu-id="afeaa-105">You use the **Quality charges** page to define the types of charges that can be added to operations for a nonconformance.</span></span> <span data-ttu-id="afeaa-106">Maksas ļauj izsekot detalizētu informāciju par maksām, ko esat parādā debitoram par neatbilstošiem produktiem, vai ko kreditors ir parādā jums par saņemtajiem neatbilstošiem produktiem.</span><span class="sxs-lookup"><span data-stu-id="afeaa-106">Charges let you track details about fees or charges that you owe to a customer for nonconforming products, or that a vendor owes to you for nonconforming products that you received.</span></span> <span data-ttu-id="afeaa-107">Maksas var izmantot arī, lai izsekotu izmaksas, kas nepieciešamas ārējiem kreditoriem vai pakalpojumiem operācijas veikšanai.</span><span class="sxs-lookup"><span data-stu-id="afeaa-107">You might also use charges to track costs that are required for external vendors or services to perform an operation.</span></span>

## <a name="examples-of-quality-charges"></a><span data-ttu-id="afeaa-108">Kvalitātes maksu piemēri</span><span class="sxs-lookup"><span data-stu-id="afeaa-108">Examples of quality charges</span></span>

<span data-ttu-id="afeaa-109">Jūs strādājat ražošanas uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="afeaa-109">You work for a manufacturing company.</span></span> <span data-ttu-id="afeaa-110">Jūsu uzņēmumam ir līgumi ar vairākiem kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="afeaa-110">Your company has contracts with several vendors.</span></span> <span data-ttu-id="afeaa-111">Šie līgumi ieskicē krājumu nosūtīšanas laikā, bojājuma un preču kvalitātes standartus.</span><span class="sxs-lookup"><span data-stu-id="afeaa-111">Those contracts outline standards for on-time shipment, damages, and product quality for items.</span></span> <span data-ttu-id="afeaa-112">Tāpat arī vairākiem debitoriem ir līgumi ar jūsu uzņēmumu par atgriešanu, zaudējumiem un produktu kvalitāti.</span><span class="sxs-lookup"><span data-stu-id="afeaa-112">Likewise, several of your customers have agreements with your company about returns, damages, and product quality.</span></span>

<span data-ttu-id="afeaa-113">Maksas struktūra ir definēta katram pārskaitījumam un norādīta līgumā.</span><span class="sxs-lookup"><span data-stu-id="afeaa-113">A fee structure is defined for each circumstance and specified in the contract.</span></span> <span data-ttu-id="afeaa-114">Jūs varat konfigurēt kvalitātes maksas, lai ieskicētu dažādus maksu veidus, piemēram, *Bojājumus*, *Nokavētus sūtījumus* un *Kvalitāti*.</span><span class="sxs-lookup"><span data-stu-id="afeaa-114">You can configure quality charges to outline the various types of charges, such as *Damages*, *Late shipment*, and *Quality*.</span></span> <span data-ttu-id="afeaa-115">Pēc tam, veidojot neatbilstību, pievienojiet vienu vai vairākas operācijas.</span><span class="sxs-lookup"><span data-stu-id="afeaa-115">Then, when you create a nonconformance, you add one or more operations.</span></span> <span data-ttu-id="afeaa-116">Katrai operācijai atlasiet **Maksas**, lai definētu detalizētu informāciju par komisijas maksām.</span><span class="sxs-lookup"><span data-stu-id="afeaa-116">For each operation, you select **Charges** to define the details about the fees.</span></span>

## <a name="create-a-quality-charge"></a><span data-ttu-id="afeaa-117">Kvalitātes maksas izveide</span><span class="sxs-lookup"><span data-stu-id="afeaa-117">Create a quality charge</span></span>

1. <span data-ttu-id="afeaa-118">Dodieties uz **Krājumu vadība \> Iestatīšana \> Kvalitātes pārvaldība \> Kvalitātes maksas**.</span><span class="sxs-lookup"><span data-stu-id="afeaa-118">Go to **Inventory management \> Setup \> Quality management \> Quality charges**.</span></span>
1. <span data-ttu-id="afeaa-119">Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="afeaa-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="afeaa-120">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="afeaa-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="afeaa-121">**Maksas kods** - ievadiet unikālu ID vai nosaukumu kvalitātes maksai.</span><span class="sxs-lookup"><span data-stu-id="afeaa-121">**Charges code** – Enter a unique ID or name for the quality charge.</span></span>
    - <span data-ttu-id="afeaa-122">**Apraksts** — ievadiet kvalitātes maksas detālizēto aprakstu.</span><span class="sxs-lookup"><span data-stu-id="afeaa-122">**Description** – Enter a detailed description of the quality charge.</span></span>

1. <span data-ttu-id="afeaa-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="afeaa-123">Close the page.</span></span>

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a><span data-ttu-id="afeaa-124">Pievienot kvalitātes maksu neatbilstības operācijai</span><span class="sxs-lookup"><span data-stu-id="afeaa-124">Add a quality charge to an operation for a nonconformance</span></span>

<span data-ttu-id="afeaa-125">Detalizētu informāciju par to, kā pievienot operācijas neatbilstībai un pielietot tām maksas, skatiet sadaļā [Neatbilstības operācijas](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="afeaa-125">For details about how to add operations to a nonconformance and apply charges to them, see [Operations for nonconformances](quality-operations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="afeaa-126">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="afeaa-126">Additional resources</span></span>

- [<span data-ttu-id="afeaa-127">Kvalitātes pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="afeaa-127">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="afeaa-128">Iespējot kvalitātes un neatbilstības pārvaldību</span><span class="sxs-lookup"><span data-stu-id="afeaa-128">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="afeaa-129">Par neatbilstību apstiprināšanu atbildīgie darbinieki</span><span class="sxs-lookup"><span data-stu-id="afeaa-129">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="afeaa-130">Karantīnas zonas neatbilstībai</span><span class="sxs-lookup"><span data-stu-id="afeaa-130">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="afeaa-131">Neatbilstību diagnostikas tipi</span><span class="sxs-lookup"><span data-stu-id="afeaa-131">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="afeaa-132">Kvalitātes maksa par neatbilstībām</span><span class="sxs-lookup"><span data-stu-id="afeaa-132">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="afeaa-133">Operācijas neatbilstībai</span><span class="sxs-lookup"><span data-stu-id="afeaa-133">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="afeaa-134">Kvalitātes pārvaldība noliktavas procesiem</span><span class="sxs-lookup"><span data-stu-id="afeaa-134">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
