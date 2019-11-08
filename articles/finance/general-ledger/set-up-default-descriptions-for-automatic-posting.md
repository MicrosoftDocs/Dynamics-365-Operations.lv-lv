---
title: Iestatīt noklusējuma aprakstus automātiskai grāmatošanai
description: Šajā tēmā skaidrots, kā iestatīt noklusējuma tekstu, kas tiek lietots, lai aprakstītu uzskaites ierakstus, kas tiek automātiski grāmatoti Virsgrāmatā. Varat iestatīt noklusējuma apraksta tekstu, izmantojot brīvformas tekstu vai izvēloties fiksētus mainīgos.
author: aprilolson
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: eb89f50a3d227cad80226ce30f71c4f210129245
ms.sourcegitcommit: 0262a19e32b2c0c84c731d9f4fbe8ba91822afa3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622693"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a><span data-ttu-id="5e3d8-104">Iestatīt noklusējuma aprakstus automātiskai grāmatošanai</span><span class="sxs-lookup"><span data-stu-id="5e3d8-104">Set up default descriptions for automatic posting</span></span>

<span data-ttu-id="5e3d8-105">Šajā tēmā skaidrots, kā iestatīt noklusējuma tekstu, kas tiek lietots, lai aprakstītu uzskaites ierakstus, kas tiek automātiski grāmatoti Virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="5e3d8-105">This topic explains how to set up default text that is used to describe accounting entries that are posted automatically to the general ledger.</span></span> <span data-ttu-id="5e3d8-106">Varat iestatīt noklusējuma apraksta tekstu, izmantojot brīvformas tekstu vai izvēloties fiksētus mainīgos.</span><span class="sxs-lookup"><span data-stu-id="5e3d8-106">You can set up default description text by using free-form text or by selecting fixed variables.</span></span>

> [!NOTE]
> <span data-ttu-id="5e3d8-107">Dažiem transakciju veidiem dažās valstīs vai reģionos varat iekļaut arī tekstu no laukiem sistēmas Microsoft Dynamics AX datu bāzē, kas ir saistīti ar šiem transakciju veidiem.</span><span class="sxs-lookup"><span data-stu-id="5e3d8-107">For some transaction types in some countries or regions, you can also include text from fields in the Microsoft Dynamics AX database that are related to those transaction types.</span></span> <span data-ttu-id="5e3d8-108">Sarakstu ar darbību tipiem, kā arī valstīm un reģioniem, skatiet sadaļu [Papildus: pievienot citu tekstu noklusējuma aprakstiem](#optional-add-other-text-to-default-descriptions) tālāk šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="5e3d8-108">For a list of the transaction types, and the countries and regions, see the [Optional: Add other text to default descriptions](#optional-add-other-text-to-default-descriptions) section later in this topic.</span></span>

## <a name="set-up-default-descriptions"></a><span data-ttu-id="5e3d8-109">Noklusējuma aprakstu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5e3d8-109">Set up default descriptions</span></span>

1. <span data-ttu-id="5e3d8-110">Dodieties uz **Organizācijas administrēšana** \> **Iestatīšana** \> **Noklusējuma apraksti**.</span><span class="sxs-lookup"><span data-stu-id="5e3d8-110">Go to **Organization administration** \> **Setup** \> **Default descriptions**.</span></span>
2. <span data-ttu-id="5e3d8-111">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5e3d8-111">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="5e3d8-112">Laukā **Apraksts** izvēlieties transakcijas veidu, kam izveidot noklusējuma aprakstu.</span><span class="sxs-lookup"><span data-stu-id="5e3d8-112">In the **Description** field, select the type of transaction to create a default description for.</span></span>
4. <span data-ttu-id="5e3d8-113">Laukā **Valoda** atlasiet valodu, uz ko šis apraksts attiecas.</span><span class="sxs-lookup"><span data-stu-id="5e3d8-113">In the **Language** field, select the language that the description applies to.</span></span>
5. <span data-ttu-id="5e3d8-114">Laukā **Teksts** ievadiet noklusējuma aprakstu.</span><span class="sxs-lookup"><span data-stu-id="5e3d8-114">In the **Text** field, enter the default description.</span></span> <span data-ttu-id="5e3d8-115">Šajā laukā varat ievadīt tekstu vai varat izmantot vienu vai vairākus no tālāk minētajiem brīva teksta mainīgajiem:</span><span class="sxs-lookup"><span data-stu-id="5e3d8-115">You can type text in the field, or you can use one or more of the following free-text variables:</span></span>

    - <span data-ttu-id="5e3d8-116">**%1** – Pievienojiet transakcijas datumu.</span><span class="sxs-lookup"><span data-stu-id="5e3d8-116">**%1** – Add the transaction date.</span></span>
    - <span data-ttu-id="5e3d8-117">**%2** – Pievienojiet identifikatoru, kas atbilst dokumenta veidam, no kura tiek veikta grāmatošana Virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="5e3d8-117">**%2** – Add an identifier that corresponds to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="5e3d8-118">Piemēram, transakciju veidiem, kas saistīti ar rēķiniem, mainīgais **%2** pievieno rēķina numuru.</span><span class="sxs-lookup"><span data-stu-id="5e3d8-118">For example, for transaction types that are related to invoices, the **%2** variable adds the invoice number.</span></span>
    - <span data-ttu-id="5e3d8-119">**%3** – Pievienojiet identifikatoru, kas ir saistīts ar dokumenta veidu, no kura tiek veikta grāmatošana Virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="5e3d8-119">**%3** – Add an identifier that is related to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="5e3d8-120">Piemēram, transakciju veidiem, kas saistīti ar rēķiniem, mainīgais **%3** pievieno debitora konta numuru.</span><span class="sxs-lookup"><span data-stu-id="5e3d8-120">For example, for transaction types that are related to invoices, the **%3** variable adds the customer account number.</span></span>

## <a name="optional-add-other-text-to-default-descriptions"></a><span data-ttu-id="5e3d8-121">Nav obligāti: pievienot citu tekstu noklusējuma aprakstiem</span><span class="sxs-lookup"><span data-stu-id="5e3d8-121">Optional: Add other text to default descriptions</span></span>

<span data-ttu-id="5e3d8-122">Dažiem transakciju veidiem dažās valstīs vai reģionos noklusējuma aprakstos varat iekļaut tekstu no laukiem sistēmas jūsu datu bāzē, kas ir saistīti ar šiem transakciju veidiem.</span><span class="sxs-lookup"><span data-stu-id="5e3d8-122">For some transaction types in some countries or regions, default descriptions can include text that comes from fields in your data that are related to those transaction types.</span></span> <span data-ttu-id="5e3d8-123">Tālāk esošajos sarakstos parādīti transakciju veidi, kā arī valstis un reģioni, kuros šī iespēja ir pieejama.</span><span class="sxs-lookup"><span data-stu-id="5e3d8-123">The following lists show the transaction types, and the countries and regions, that this option is available for.</span></span>

<span data-ttu-id="5e3d8-124">**Darbību tipi**</span><span class="sxs-lookup"><span data-stu-id="5e3d8-124">**Transaction types**</span></span>

<span data-ttu-id="5e3d8-125">Varat pievienot citu tekstu transakciju veidu noklusējuma aprakstiem, kas saistīti ar šādiem dokumentu veidiem:</span><span class="sxs-lookup"><span data-stu-id="5e3d8-125">You can add other text to default descriptions for transaction types that are related to the following document types:</span></span>

- <span data-ttu-id="5e3d8-126">Debitora rēķini</span><span class="sxs-lookup"><span data-stu-id="5e3d8-126">Customer invoices</span></span>
- <span data-ttu-id="5e3d8-127">Debitora kredīta notas</span><span class="sxs-lookup"><span data-stu-id="5e3d8-127">Customer credit notes</span></span>
- <span data-ttu-id="5e3d8-128">Debitoru skaidras naudas maksājumi</span><span class="sxs-lookup"><span data-stu-id="5e3d8-128">Customer cash payments</span></span>
- <span data-ttu-id="5e3d8-129">Kreditoru maksājumi</span><span class="sxs-lookup"><span data-stu-id="5e3d8-129">Vendor payments</span></span>
- <span data-ttu-id="5e3d8-130">Pārdošanas pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="5e3d8-130">Sales orders</span></span>
- <span data-ttu-id="5e3d8-131">Pirkšanas pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="5e3d8-131">Purchase orders</span></span>
- <span data-ttu-id="5e3d8-132">Krājumu žurnāli</span><span class="sxs-lookup"><span data-stu-id="5e3d8-132">Inventory journals</span></span>
- <span data-ttu-id="5e3d8-133">Vispārējā plānošana (MRP)</span><span class="sxs-lookup"><span data-stu-id="5e3d8-133">Master planning (MRP)</span></span>
- <span data-ttu-id="5e3d8-134">Pamatlīdzekļi</span><span class="sxs-lookup"><span data-stu-id="5e3d8-134">Fixed assets</span></span>

<span data-ttu-id="5e3d8-135">**Valstis un reģioni**</span><span class="sxs-lookup"><span data-stu-id="5e3d8-135">**Countries and regions**</span></span>

<span data-ttu-id="5e3d8-136">Šī iespēja ir pieejama šādām valstīm un reģioniem:</span><span class="sxs-lookup"><span data-stu-id="5e3d8-136">This option is available for the following countries and regions:</span></span>

- <span data-ttu-id="5e3d8-137">Brazīlija</span><span class="sxs-lookup"><span data-stu-id="5e3d8-137">Brazil</span></span>
- <span data-ttu-id="5e3d8-138">Ķīna</span><span class="sxs-lookup"><span data-stu-id="5e3d8-138">China</span></span>
- <span data-ttu-id="5e3d8-139">Čehijas Republika</span><span class="sxs-lookup"><span data-stu-id="5e3d8-139">Czech Republic</span></span>
- <span data-ttu-id="5e3d8-140">Austrumeiropa</span><span class="sxs-lookup"><span data-stu-id="5e3d8-140">Eastern Europe</span></span>
- <span data-ttu-id="5e3d8-141">Ungārija</span><span class="sxs-lookup"><span data-stu-id="5e3d8-141">Hungary</span></span>
- <span data-ttu-id="5e3d8-142">Indija</span><span class="sxs-lookup"><span data-stu-id="5e3d8-142">India</span></span>
- <span data-ttu-id="5e3d8-143">Japāna</span><span class="sxs-lookup"><span data-stu-id="5e3d8-143">Japan</span></span>
- <span data-ttu-id="5e3d8-144">Lietuva</span><span class="sxs-lookup"><span data-stu-id="5e3d8-144">Lithuania</span></span>
- <span data-ttu-id="5e3d8-145">Latvija</span><span class="sxs-lookup"><span data-stu-id="5e3d8-145">Latvia</span></span>
- <span data-ttu-id="5e3d8-146">Polija</span><span class="sxs-lookup"><span data-stu-id="5e3d8-146">Poland</span></span>
- <span data-ttu-id="5e3d8-147">Krievija</span><span class="sxs-lookup"><span data-stu-id="5e3d8-147">Russia</span></span>

### <a name="add-text-to-default-descriptions"></a><span data-ttu-id="5e3d8-148">Pievienot tekstu noklusējuma aprakstiem</span><span class="sxs-lookup"><span data-stu-id="5e3d8-148">Add text to default descriptions</span></span>

<span data-ttu-id="5e3d8-149">Kad pabeidzat iepriekš šajā tēmā aprakstītos soļus sadaļā [Noklusējuma aprakstu iestatīšana](#set-up-default-descriptions), rīkojieties šādi, lai pievienotu citu tekstu noklusējuma aprakstiem.</span><span class="sxs-lookup"><span data-stu-id="5e3d8-149">After you complete the steps in the [Set up default descriptions](#set-up-default-descriptions) section earlier in this topic, follow these steps to add other text to the default descriptions.</span></span>

1. <span data-ttu-id="5e3d8-150">Kopsavilkuma cilnē **Parametri** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="5e3d8-150">On the **Parameters** FastTab, select **Add**.</span></span>
2. <span data-ttu-id="5e3d8-151">Laukā **Atsauču tabula** atlasiet datu bāzes tabulu, no kuras pievienot parametru datu aprakstam.</span><span class="sxs-lookup"><span data-stu-id="5e3d8-151">In the **Reference table** field, select the database table from which to add parameter data to the description.</span></span>
3. <span data-ttu-id="5e3d8-152">Laukā **Atsauču lauks** atlasiet datu bāzes lauku, no kuras pievienot parametru datu aprakstam.</span><span class="sxs-lookup"><span data-stu-id="5e3d8-152">In the **Reference field** field, select the field from which to add parameter data to the description.</span></span>
4. <span data-ttu-id="5e3d8-153">Atkārtojiet 1. līdz 3. soli, lai pievienotu vairāk parametru.</span><span class="sxs-lookup"><span data-stu-id="5e3d8-153">Repeat steps 1 through 3 to add more parameters.</span></span>
