---
title: Preču kvalitātes pārbaude
description: Šajā tēmā ir aprakstīts, kā apstrādāt kvalitātes pārbaudes pasūtījumus.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec67e7864db12178c0f3cfe8b93d510a46e8a0d4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956138"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="7d82c-103">Preču kvalitātes pārbaude</span><span class="sxs-lookup"><span data-stu-id="7d82c-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7d82c-104">Šajā tēmā ir aprakstīts, kā apstrādāt kvalitātes pārbaudes pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="7d82c-104">This topic describes how to process quality orders.</span></span> <span data-ttu-id="7d82c-105">Kvalitātes pārbaudes parasti veic kvalitātes darbinieks.</span><span class="sxs-lookup"><span data-stu-id="7d82c-105">Quality inspections are typically done by a quality clerk.</span></span>

<span data-ttu-id="7d82c-106">Ja standarta demonstrācijas dati ir instalēti, varat izmantot tos, lai veiktu procedūras šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="7d82c-106">If the standard demo data is installed, you can use it to complete the procedures in this topic.</span></span> <span data-ttu-id="7d82c-107">Lai izmantotu demonstrācijas datus, atlasiet *USMF* juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="7d82c-107">To use the demo data, select the *USMF* legal entity before you begin.</span></span> <span data-ttu-id="7d82c-108">Pēc tam apstipriniet pirkšanas pasūtījumu *000016* un grāmatojiet produktu ieejas plūsmu.</span><span class="sxs-lookup"><span data-stu-id="7d82c-108">You must then confirm purchase order *000016* and post a product receipt.</span></span> <span data-ttu-id="7d82c-109">Kvalitātes pārbaudes pasūtījumus tiek ģenerēts automātiski.</span><span class="sxs-lookup"><span data-stu-id="7d82c-109">A quality order is automatically generated.</span></span>

## <a name="step-1-select-a-quality-order"></a><span data-ttu-id="7d82c-110">1. darbība: Atlasiet kvalitātes pārbaudes pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="7d82c-110">Step 1: Select a quality order</span></span>

<span data-ttu-id="7d82c-111">Lai atlasītu kvalitātes pārbaudes pasūtījumu, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="7d82c-111">To select a quality order, follow these steps.</span></span>

1. <span data-ttu-id="7d82c-112">Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Kvalitātes pārbaudes pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="7d82c-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="7d82c-113">Atlasiet kvalitātes pārbaudes pasūtījumu, kas tika ģenerēts pirms šīs procedūras uzsākšanas.</span><span class="sxs-lookup"><span data-stu-id="7d82c-113">Select the quality order that was generated before you started this procedure.</span></span>

## <a name="step-2-record-test-results"></a><span data-ttu-id="7d82c-114">2. darbība: Testa rezultātu reģistrēšana</span><span class="sxs-lookup"><span data-stu-id="7d82c-114">Step 2: Record test results</span></span>

<span data-ttu-id="7d82c-115">Lai ierakstītu testa rezultātus, sekojiet šiem darbībām.</span><span class="sxs-lookup"><span data-stu-id="7d82c-115">To record test results, follow these steps.</span></span>

1. <span data-ttu-id="7d82c-116">Atlasiet **Rezultāti**.</span><span class="sxs-lookup"><span data-stu-id="7d82c-116">Select **Results**.</span></span>
1. <span data-ttu-id="7d82c-117">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="7d82c-117">Select **Edit**.</span></span>
1. <span data-ttu-id="7d82c-118">Laukā **Rezultātu daudzums** ierakstiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="7d82c-118">In the **Result quantity** field, enter a number.</span></span>
1. <span data-ttu-id="7d82c-119">Laukā **Rezultāts** atlasiet vēlamo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="7d82c-119">In the **Outcome** field, select the desired record.</span></span> <span data-ttu-id="7d82c-120">Šajā piemērā rezultāta pamatā ir iepriekš definēts iznākums.</span><span class="sxs-lookup"><span data-stu-id="7d82c-120">In this example, the result is based on a predefined outcome.</span></span> <span data-ttu-id="7d82c-121">Parasti tiek ierakstīts specifiskāks testa rezultāts, piemēram, izmērs vai cita dimensija.</span><span class="sxs-lookup"><span data-stu-id="7d82c-121">Usually, you will record a more specific test result, such as a size or other dimension.</span></span>
1. <span data-ttu-id="7d82c-122">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="7d82c-122">Select **Save**.</span></span>
1. <span data-ttu-id="7d82c-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7d82c-123">Close the page.</span></span>

## <a name="step-3-validate-the-quality-order"></a><span data-ttu-id="7d82c-124">3. darbība: Pārbaudīt kvalitātes pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="7d82c-124">Step 3: Validate the quality order</span></span>

<span data-ttu-id="7d82c-125">Lai pārbaudītu kvalitātes pārbaudes pasūtījumu, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="7d82c-125">To validate the quality order, follow these steps.</span></span>

1. <span data-ttu-id="7d82c-126">Atlasiet **Pārbaudīt**.</span><span class="sxs-lookup"><span data-stu-id="7d82c-126">Select **Validate**.</span></span>
1. <span data-ttu-id="7d82c-127">Laukā **Pārbaudīts pēc** atlasiet lietotāju, kas veic pārbaudi.</span><span class="sxs-lookup"><span data-stu-id="7d82c-127">In the **Validated by** field, select the user who is doing the inspection.</span></span>
1. <span data-ttu-id="7d82c-128">Atlasiet **Atlasīt**.</span><span class="sxs-lookup"><span data-stu-id="7d82c-128">Select **Select**.</span></span>
1. <span data-ttu-id="7d82c-129">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7d82c-129">Select **OK**.</span></span>
1. <span data-ttu-id="7d82c-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7d82c-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
