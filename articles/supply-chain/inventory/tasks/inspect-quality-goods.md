---
title: Preču kvalitātes pārbaude
description: Šajā tēmā ir paskaidrots, kā apstrādāt kvalitātes pārbaudes pasūtījumu.
author: perlynne
manager: tfehr
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dbfb3733cc52f0f8f54ab4388764429387358ee7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011526"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="52cd8-103">Preču kvalitātes pārbaude</span><span class="sxs-lookup"><span data-stu-id="52cd8-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="52cd8-104">Šajā tēmā ir paskaidrots, kā apstrādāt kvalitātes pārbaudes pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="52cd8-104">This topic explains how to process a quality order.</span></span> <span data-ttu-id="52cd8-105">Šo ceļvedi varat izpildīt demonstrācijas datu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="52cd8-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="52cd8-106">Pirms sākat šo piemēra procedūru, jums ir jāapstiprina pirkšanas pasūtījums "000016" un jāiegrāmato produktu ieejas plūsma.</span><span class="sxs-lookup"><span data-stu-id="52cd8-106">Before you start this example procedure, you need to confirm purchase order "000016" and post a product receipt.</span></span> <span data-ttu-id="52cd8-107">Šādi automātiski tiks izveidots kvalitātes pārbaudes pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="52cd8-107">This will automatically create a quality order.</span></span> <span data-ttu-id="52cd8-108">Kvalitātes pārbaudes parasti veic kvalitātes darbinieks.</span><span class="sxs-lookup"><span data-stu-id="52cd8-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="52cd8-109">Atlasiet kvalitātes pārbaudes pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="52cd8-109">Select a quality order</span></span>
1. <span data-ttu-id="52cd8-110">Navigācijas rūtī dodieties uz **Moduļi > Krājumu vadība > Periodiskie uzdevumi > Kvalitātes vadība > Kvalitātes pārbaudes pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="52cd8-110">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="52cd8-111">Atlasiet kvalitātes pārbaudes pasūtījumu, kas tika izveidots pirms šīs procedūras uzsākšanas.</span><span class="sxs-lookup"><span data-stu-id="52cd8-111">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="52cd8-112">Testa rezultātu reģistrēšana</span><span class="sxs-lookup"><span data-stu-id="52cd8-112">Record test results</span></span>
1. <span data-ttu-id="52cd8-113">Atlasiet **Rezultāti**.</span><span class="sxs-lookup"><span data-stu-id="52cd8-113">Select **Results**.</span></span>
2. <span data-ttu-id="52cd8-114">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="52cd8-114">Select **Edit**.</span></span>
3. <span data-ttu-id="52cd8-115">Laukā **Rezultātu daudzums** ierakstiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="52cd8-115">In the **Result quantity** field, enter a number.</span></span>
4. <span data-ttu-id="52cd8-116">Laukā **Iznākums** nolaižamamajā izvēlnē atlasiet vēlamo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="52cd8-116">In the **Outcome** field, select the desired record in the drop-down menu.</span></span>  
- <span data-ttu-id="52cd8-117">Šajā piemērā rezultāta pamatā ir iepriekš definēts iznākums.</span><span class="sxs-lookup"><span data-stu-id="52cd8-117">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="52cd8-118">Parasti tiek ierakstīts specifiskāks testa rezultāts, piemēram, izmērs vai cita dimensija.</span><span class="sxs-lookup"><span data-stu-id="52cd8-118">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
5. <span data-ttu-id="52cd8-119">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="52cd8-119">Select **Save**.</span></span>
6. <span data-ttu-id="52cd8-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="52cd8-120">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="52cd8-121">Pārbaudīt kvalitātes pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="52cd8-121">Validate the quality order</span></span>
1. <span data-ttu-id="52cd8-122">Atlasiet **Validēt**.</span><span class="sxs-lookup"><span data-stu-id="52cd8-122">Select **Validate**.</span></span>
2. <span data-ttu-id="52cd8-123">Laukā **Validējis** atlasiet lietotāju, kurš veic pārbaudi no nolaižamās izvēlnes.</span><span class="sxs-lookup"><span data-stu-id="52cd8-123">In the **Validated by** field, select the user performing the inspection from the drop-down menu.</span></span>  
3. <span data-ttu-id="52cd8-124">Noklikšķiniet uz **Atlasīt**.</span><span class="sxs-lookup"><span data-stu-id="52cd8-124">Click **Select**.</span></span>
4. <span data-ttu-id="52cd8-125">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="52cd8-125">Select **OK**.</span></span>
5. <span data-ttu-id="52cd8-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="52cd8-126">Close the page.</span></span>

