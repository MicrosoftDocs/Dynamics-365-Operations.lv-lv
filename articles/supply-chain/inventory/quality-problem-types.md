---
title: Neatbilstību problēmu veidi
description: Šajā tēmā aprakstīts, kā izveidot un izmantot problēmu veidus neatbilstībām.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 742edec8570610efe41a2c627efd1df586e0733e
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022160"
---
# <a name="problem-types-for-nonconformances"></a><span data-ttu-id="2dd8f-103">Neatbilstību problēmu veidi</span><span class="sxs-lookup"><span data-stu-id="2dd8f-103">Problem types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2dd8f-104">Šajā tēmā aprakstīts, kā izveidot un izmantot problēmu veidus neatbilstībām.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-104">This topic describes how to create and use problem types for nonconformances.</span></span>

<span data-ttu-id="2dd8f-105">Izmantojiet lapu **Problēmveidi**, lai definētu to kvalitātes problēmu klasifikāciju, kas var rasties dažādiem neatbilstības veidiem.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-105">You use the **Problem types** page to define a classification of the quality problems that might occur for the various nonconformance types.</span></span> <span data-ttu-id="2dd8f-106">Katram jūsu izveidotajiem problēmas veidam ir jānorāda neatbilstību veidi, ar kuriem var izmantot problēmas veidu.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-106">For each problem type that you create, you must specify the types of nonconformances that the problem type can be used with.</span></span> <span data-ttu-id="2dd8f-107">Jūs varat iestatīt tālāk minētos neatbilstību veidus.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-107">You can set up the following nonconformance types:</span></span>

- <span data-ttu-id="2dd8f-108">**Iekšējs** – šī veida neatbilstības ir saistītas ar rīcībā esošiem krājumiem (piemēram, kvalitātes pārbaudes pasūtījumiem vai karantīnas pasūtījumiem).</span><span class="sxs-lookup"><span data-stu-id="2dd8f-108">**Internal** – Nonconformances of this type are related to on-hand inventory (for example, quality orders or quarantine orders).</span></span>
- <span data-ttu-id="2dd8f-109">**Debitors** – šī veida neatbilstības ir saistītas ar pārdošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-109">**Customer** – Nonconformances of this type are related to sales orders.</span></span>
- <span data-ttu-id="2dd8f-110">**Kreditors** – šī veida neatbilstības ir saistītas ar pirkšanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-110">**Vendor** – Nonconformances of this type are related to purchase orders.</span></span>
- <span data-ttu-id="2dd8f-111">**Pakalpojuma pieprasījums** – šī veida neatbilstības ir saistītas ar pakalpojuma pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-111">**Service request** – Nonconformances of this type are related to service orders.</span></span>
- <span data-ttu-id="2dd8f-112">**Ražošana** - šī veida neatbilstības ir saistītas ar partijas pasūtījumiem vai ražošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-112">**Production** – Nonconformances of this type are related to batch orders or production orders.</span></span>
- <span data-ttu-id="2dd8f-113">**Līdzprodukta ražošana** - šī veida neatbilstības ir saistītas ar partijas pasūtījumiem vai līdzproduktiem.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-113">**Co-product production** – Nonconformances of this type are related to batch orders for co-products.</span></span>

<span data-ttu-id="2dd8f-114">Izveidojot jaunu problēmas veidu, atlasiet **Neatbilstības veidus** darbību rūtī, lai izveidotu sarakstu ar vienu vai vairākiem neatbilstības veidiem, kas ir autorizēti problēmas veidam.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-114">When you create a new problem type, select **Non conformance types** on the Action Pane to create a list of one or more nonconformance types that are authorized for the problem type.</span></span> <span data-ttu-id="2dd8f-115">Piemēram, problēmas veids, kas saistīts ar defekta kodu, var attiekties uz viesiem neatbilstības veidiem.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-115">For example, a problem type that is related to a defect code might apply to all nonconformance types.</span></span> <span data-ttu-id="2dd8f-116">Tomēr problēmas veidu, kas ir saistīts ar debitora sūdzībām, var pielietot tikai neatbilstības veidiem **Debitors** un **Pakalpojuma pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-116">However, a problem type that is related to customer complaints might apply only to the **Customer** and **Service request** nonconformance types.</span></span>

## <a name="examples-of-problem-types"></a><span data-ttu-id="2dd8f-117">Problēmu veidu paraugi</span><span class="sxs-lookup"><span data-stu-id="2dd8f-117">Examples of problem types</span></span>

<span data-ttu-id="2dd8f-118">Šeit sniegti daži scenāriju piemēri problēmu veidiem, kurus var izmantot ar dažādiem neatbilstības veidiem:</span><span class="sxs-lookup"><span data-stu-id="2dd8f-118">Here are some examples of scenarios for problem types that can be used with the different nonconformance types:</span></span>

- <span data-ttu-id="2dd8f-119">**Debitors:** debitors iesniedza sūdzību, debitors veica atgriešanu vai arī netika ievērotas kvalitātes specifikācijas.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-119">**Customer:** A customer filed a complaint, a customer made a return, or quality specifications weren't met.</span></span>
- <span data-ttu-id="2dd8f-120">**Kreditors:** prece tika bojāta, kvalitātes specifikācijas netika ievērotas vai tika saņemta nepareiza prece.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-120">**Vendor:** The product was damaged, quality specifications weren't met, or the wrong product was received.</span></span>
- <span data-ttu-id="2dd8f-121">**Pakalpojuma pieprasījums:** netika ievērotas kvalitātes specifikācijas, debitors bija iesniedzis sūdzību vai ir nepieciešama iekārtas uzturēšana.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-121">**Service request:** Quality specifications weren't met, a customer filed a complaint, or machine maintenance is required.</span></span>
- <span data-ttu-id="2dd8f-122">**Ražošana:** netika izpildītas kvalitātes specifikācijas, ir nepieciešama iekārtas uzturēšana vai prece tika bojāta.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-122">**Production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>
- <span data-ttu-id="2dd8f-123">**Līdzprodukta ažošana:** netika izpildītas kvalitātes specifikācijas, ir nepieciešama iekārtas uzturēšana vai prece tika bojāta.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-123">**Co-product production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a><span data-ttu-id="2dd8f-124">Izveidojiet problēmas veidu un piešķiriet to neatbilstības veidiem</span><span class="sxs-lookup"><span data-stu-id="2dd8f-124">Create a problem type and assign it to nonconformance types</span></span>

1. <span data-ttu-id="2dd8f-125">Dodieties uz **Krājumu vadība \> Iestatīšana \> Kvalitātes pārvaldība \> Problēmu veidi**.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-125">Go to **Inventory management \> Setup \> Quality management \> Problem types**.</span></span>
1. <span data-ttu-id="2dd8f-126">Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-126">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="2dd8f-127">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="2dd8f-127">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="2dd8f-128">**Problēmu veidi** - Ievadiet unikālu problēmas veida ID vai nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-128">**Problem type** – Enter a unique ID or name for the problem type.</span></span>
    - <span data-ttu-id="2dd8f-129">**Apraksts** — ievadiet problēmas veida detālizēto aprakstu.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-129">**Description** – Enter a detailed description of the problem type.</span></span>

1. <span data-ttu-id="2dd8f-130">Kamēr jaunā rinda joprojām ir atlasīta, darbību rūtī atlasiet **Neatbilstības veidus**.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-130">While the new row is still selected, select **Non conformance types** on the Action Pane.</span></span>
1. <span data-ttu-id="2dd8f-131">Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-131">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="2dd8f-132">Tad jaunajai rindai iestatiet lauku **Neatbilstības veids** neatbilstības veidam, kuru vēlaties atļaut problēmas veidam.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-132">Then, for the new row, set the **Non conformance type** field to the nonconformance type that you want to allow for the problem type.</span></span>
1. <span data-ttu-id="2dd8f-133">Atkārtojiet iepriekšējo darbību katram papildu neatbilstības veidam, kuru vēlaties autorizēt problēmas veidam.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-133">Repeat the previous step for each additional nonconformance type that you want to authorize for the problem type.</span></span>
1. <span data-ttu-id="2dd8f-134">Aizveriet lapas.</span><span class="sxs-lookup"><span data-stu-id="2dd8f-134">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2dd8f-135">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="2dd8f-135">Additional resources</span></span>

- [<span data-ttu-id="2dd8f-136">Kvalitātes pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="2dd8f-136">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="2dd8f-137">Iespējot kvalitātes un neatbilstības pārvaldību</span><span class="sxs-lookup"><span data-stu-id="2dd8f-137">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="2dd8f-138">Par neatbilstību apstiprināšanu atbildīgie darbinieki</span><span class="sxs-lookup"><span data-stu-id="2dd8f-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="2dd8f-139">Karantīnas zonas neatbilstībai</span><span class="sxs-lookup"><span data-stu-id="2dd8f-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="2dd8f-140">Neatbilstību diagnostikas tipi</span><span class="sxs-lookup"><span data-stu-id="2dd8f-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="2dd8f-141">Kvalitātes maksa par neatbilstībām</span><span class="sxs-lookup"><span data-stu-id="2dd8f-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="2dd8f-142">Operācijas neatbilstībai</span><span class="sxs-lookup"><span data-stu-id="2dd8f-142">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="2dd8f-143">Kvalitātes pārvaldība noliktavas procesiem</span><span class="sxs-lookup"><span data-stu-id="2dd8f-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
