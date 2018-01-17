---
title: "Preču kvalitātes pārbaude"
description: "Šajā procedūrā parādīts, kā apstrādāt kvalitātes pārbaudes pasūtījumu."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 3a4ace658b8a3a20d613b7a251eb85c32c7f1c09
ms.contentlocale: lv-lv
ms.lasthandoff: 01/17/2018

---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="9c2e9-103">Preču kvalitātes pārbaude</span><span class="sxs-lookup"><span data-stu-id="9c2e9-103">Inspect the quality of goods</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9c2e9-104">Šajā procedūrā parādīts, kā apstrādāt kvalitātes pārbaudes pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-104">This procedure shows you how to process a quality order.</span></span> <span data-ttu-id="9c2e9-105">Šo ceļvedi varat izpildīt demonstrācijas datu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="9c2e9-106">Pirms sākat šo piemēra procedūru, jums ir jāapstiprina pirkšanas pasūtījums 000016 un jāiegrāmato produktu ieejas plūsma.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-106">Before you start this example procedure, you need to confirm purchase order “000016” and post a product receipt.</span></span> <span data-ttu-id="9c2e9-107">Šādi automātiski tiks izveidots kvalitātes pārbaudes pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-107">This will automatically create a quality order.</span></span> <span data-ttu-id="9c2e9-108">Kvalitātes pārbaudes parasti veic kvalitātes darbinieks.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="9c2e9-109">Atlasiet kvalitātes pārbaudes pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-109">Select a quality order</span></span>
1. <span data-ttu-id="9c2e9-110">Dodieties uz Krājumu vadība > Periodiskie uzdevumi > Kvalitātes vadība > Kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-110">Go to Inventory management > Periodic tasks > Quality management > Quality orders.</span></span>
2. <span data-ttu-id="9c2e9-111">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9c2e9-112">Atlasiet kvalitātes pārbaudes pasūtījumu, kas tika izveidots pirms šīs procedūras uzsākšanas.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-112">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="9c2e9-113">Testa rezultātu reģistrēšana</span><span class="sxs-lookup"><span data-stu-id="9c2e9-113">Record test results</span></span>
1. <span data-ttu-id="9c2e9-114">Noklikšķiniet uz Rezultāti.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-114">Click Results.</span></span>
2. <span data-ttu-id="9c2e9-115">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-115">Click Edit.</span></span>
3. <span data-ttu-id="9c2e9-116">Ierakstiet skaitli laukā Rezultātu daudzums.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-116">In the Result quantity field, enter a number.</span></span>
4. <span data-ttu-id="9c2e9-117">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-117">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="9c2e9-118">Laukā Iznākums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-118">In the Outcome field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9c2e9-119">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9c2e9-120">Šajā piemērā rezultāta pamatā ir iepriekš definēts iznākums.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-120">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="9c2e9-121">Parasti tiek ierakstīts specifiskāks testa rezultāts, piemēram, izmērs vai cita dimensija.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-121">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
7. <span data-ttu-id="9c2e9-122">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9c2e9-123">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-123">Click Save.</span></span>
9. <span data-ttu-id="9c2e9-124">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-124">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="9c2e9-125">Pārbaudīt kvalitātes pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="9c2e9-125">Validate the quality order</span></span>
1. <span data-ttu-id="9c2e9-126">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-126">Click Validate.</span></span>
2. <span data-ttu-id="9c2e9-127">Laukā Pārbaudīja noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-127">In the Validated by field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9c2e9-128">Atlasiet lietotāju, kas veic pārbaudi.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-128">Select the user performing the inspection.</span></span>  
3. <span data-ttu-id="9c2e9-129">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-129">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9c2e9-130">Noklikšķiniet uz Atlasīt.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-130">Click Select.</span></span>
5. <span data-ttu-id="9c2e9-131">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-131">Click OK.</span></span>
6. <span data-ttu-id="9c2e9-132">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-132">Close the page.</span></span>

