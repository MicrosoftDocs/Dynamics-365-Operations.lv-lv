---
title: Maksa par neatbilstības operācijam
description: Šajā tēmā ir aprakstīts, kā izveidot kvalitātes maksas, ko var izmantot operācijām neatbilstībai.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 382890232bff47a885840af1eb7e91d27bb46cae
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022304"
---
# <a name="charges-for-nonconformance-operations"></a><span data-ttu-id="30200-103">Maksa par neatbilstības operācijam</span><span class="sxs-lookup"><span data-stu-id="30200-103">Charges for nonconformance operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30200-104">Šajā tēmā ir aprakstīts, kā izveidot kvalitātes maksas, ko var izmantot operācijām neatbilstībai.</span><span class="sxs-lookup"><span data-stu-id="30200-104">This topic describes how to create quality charges that can be used with operations for a nonconformance.</span></span>

<span data-ttu-id="30200-105">Izmantojiet lapu **Kvalitātes maksas**, lai definētu maksu veidus, kas var pievienot operācijām neatbilstībām.</span><span class="sxs-lookup"><span data-stu-id="30200-105">You use the **Quality charges** page to define the types of charges that can be added to operations for a nonconformance.</span></span> <span data-ttu-id="30200-106">Maksas ļauj izsekot detalizētu informāciju par maksām, ko esat parādā debitoram par neatbilstošiem produktiem, vai ko kreditors ir parādā jums par saņemtajiem neatbilstošiem produktiem.</span><span class="sxs-lookup"><span data-stu-id="30200-106">Charges let you track details about fees or charges that you owe to a customer for nonconforming products, or that a vendor owes to you for nonconforming products that you received.</span></span> <span data-ttu-id="30200-107">Maksas var izmantot arī, lai izsekotu izmaksas, kas nepieciešamas ārējiem kreditoriem vai pakalpojumiem operācijas veikšanai.</span><span class="sxs-lookup"><span data-stu-id="30200-107">You might also use charges to track costs that are required for external vendors or services to perform an operation.</span></span>

## <a name="examples-of-quality-charges"></a><span data-ttu-id="30200-108">Kvalitātes maksu piemēri</span><span class="sxs-lookup"><span data-stu-id="30200-108">Examples of quality charges</span></span>

<span data-ttu-id="30200-109">Jūs strādājat ražošanas uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="30200-109">You work for a manufacturing company.</span></span> <span data-ttu-id="30200-110">Jūsu uzņēmumam ir līgumi ar vairākiem kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="30200-110">Your company has contracts with several vendors.</span></span> <span data-ttu-id="30200-111">Šie līgumi ieskicē krājumu nosūtīšanas laikā, bojājuma un preču kvalitātes standartus.</span><span class="sxs-lookup"><span data-stu-id="30200-111">Those contracts outline standards for on-time shipment, damages, and product quality for items.</span></span> <span data-ttu-id="30200-112">Tāpat arī vairākiem debitoriem ir līgumi ar jūsu uzņēmumu par atgriešanu, zaudējumiem un produktu kvalitāti.</span><span class="sxs-lookup"><span data-stu-id="30200-112">Likewise, several of your customers have agreements with your company about returns, damages, and product quality.</span></span>

<span data-ttu-id="30200-113">Maksas struktūra ir definēta katram pārskaitījumam un norādīta līgumā.</span><span class="sxs-lookup"><span data-stu-id="30200-113">A fee structure is defined for each circumstance and specified in the contract.</span></span> <span data-ttu-id="30200-114">Jūs varat konfigurēt kvalitātes maksas, lai ieskicētu dažādus maksu veidus, piemēram, *Bojājumus*, *Nokavētus sūtījumus* un *Kvalitāti*.</span><span class="sxs-lookup"><span data-stu-id="30200-114">You can configure quality charges to outline the various types of charges, such as *Damages*, *Late shipment*, and *Quality*.</span></span> <span data-ttu-id="30200-115">Pēc tam, veidojot neatbilstību, pievienojiet vienu vai vairākas operācijas.</span><span class="sxs-lookup"><span data-stu-id="30200-115">Then, when you create a nonconformance, you add one or more operations.</span></span> <span data-ttu-id="30200-116">Katrai operācijai atlasiet **Maksas**, lai definētu detalizētu informāciju par komisijas maksām.</span><span class="sxs-lookup"><span data-stu-id="30200-116">For each operation, you select **Charges** to define the details about the fees.</span></span>

## <a name="create-a-quality-charge"></a><span data-ttu-id="30200-117">Kvalitātes maksas izveide</span><span class="sxs-lookup"><span data-stu-id="30200-117">Create a quality charge</span></span>

1. <span data-ttu-id="30200-118">Dodieties uz **Krājumu vadība \> Iestatīšana \> Kvalitātes pārvaldība \> Kvalitātes maksas**.</span><span class="sxs-lookup"><span data-stu-id="30200-118">Go to **Inventory management \> Setup \> Quality management \> Quality charges**.</span></span>
1. <span data-ttu-id="30200-119">Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="30200-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="30200-120">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="30200-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="30200-121">**Maksas kods** - ievadiet unikālu ID vai nosaukumu kvalitātes maksai.</span><span class="sxs-lookup"><span data-stu-id="30200-121">**Charges code** – Enter a unique ID or name for the quality charge.</span></span>
    - <span data-ttu-id="30200-122">**Apraksts** — ievadiet kvalitātes maksas detālizēto aprakstu.</span><span class="sxs-lookup"><span data-stu-id="30200-122">**Description** – Enter a detailed description of the quality charge.</span></span>

1. <span data-ttu-id="30200-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="30200-123">Close the page.</span></span>

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a><span data-ttu-id="30200-124">Pievienot kvalitātes maksu neatbilstības operācijai</span><span class="sxs-lookup"><span data-stu-id="30200-124">Add a quality charge to an operation for a nonconformance</span></span>

<span data-ttu-id="30200-125">Detalizētu informāciju par to, kā pievienot operācijas neatbilstībai un pielietot tām maksas, skatiet sadaļā [Neatbilstības operācijas](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="30200-125">For details about how to add operations to a nonconformance and apply charges to them, see [Operations for nonconformances](quality-operations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="30200-126">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="30200-126">Additional resources</span></span>

- [<span data-ttu-id="30200-127">Kvalitātes pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="30200-127">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="30200-128">Iespējot kvalitātes un neatbilstības pārvaldību</span><span class="sxs-lookup"><span data-stu-id="30200-128">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="30200-129">Par neatbilstību apstiprināšanu atbildīgie darbinieki</span><span class="sxs-lookup"><span data-stu-id="30200-129">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="30200-130">Karantīnas zonas neatbilstībai</span><span class="sxs-lookup"><span data-stu-id="30200-130">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="30200-131">Neatbilstību diagnostikas tipi</span><span class="sxs-lookup"><span data-stu-id="30200-131">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="30200-132">Kvalitātes maksa par neatbilstībām</span><span class="sxs-lookup"><span data-stu-id="30200-132">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="30200-133">Operācijas neatbilstībai</span><span class="sxs-lookup"><span data-stu-id="30200-133">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="30200-134">Kvalitātes pārvaldība noliktavas procesiem</span><span class="sxs-lookup"><span data-stu-id="30200-134">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
