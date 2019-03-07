---
title: Atvieglojumu piemērotības kārtulu un ierobežojumu definēšana
description: Šajā ierakstā parādīts, kā izveidot atvieglojumu piemērojamības noteikumus un ierobežojumus un pēc tam piešķirt noteikumus atvieglojumiem.
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d346c3277e8f19020d6aa96cf6961c4c52ac28fb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "341676"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="7b066-103">Atvieglojumu piemērotības kārtulu un ierobežojumu definēšana</span><span class="sxs-lookup"><span data-stu-id="7b066-103">Define benefit eligibility rules and policies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7b066-104">Šajā ierakstā parādīts, kā izveidot atvieglojumu piemērojamības noteikumus un ierobežojumus un pēc tam piešķirt noteikumus atvieglojumiem.</span><span class="sxs-lookup"><span data-stu-id="7b066-104">This recording will show you how you can create benefit eligibility rules and policies and then assign rules to Benefits.</span></span>  

<span data-ttu-id="7b066-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo ierakstu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="7b066-105">The demo data company used to create this recording is USMF.</span></span>


## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="7b066-106">Atvieglojumu piemērojamības ierobežojuma nosacījumu tipa izveide</span><span class="sxs-lookup"><span data-stu-id="7b066-106">Create benefit eligibility policy rule type</span></span>
1. <span data-ttu-id="7b066-107">Dodieties uz Personāla vadība > Atvieglojumi > Piemērojamība > Atvieglojumu piemērojamības ierobežojumu nosacījumu tipi.</span><span class="sxs-lookup"><span data-stu-id="7b066-107">Go to Human resources > Benefits > Eligibility > Benefit eligibility policy rule types.</span></span>
2. <span data-ttu-id="7b066-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="7b066-108">Click New.</span></span>
3. <span data-ttu-id="7b066-109">Laukā Kārtulas nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7b066-109">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="7b066-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="7b066-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7b066-111">Laukā Vaicājuma nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="7b066-111">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="7b066-112">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="7b066-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="7b066-113">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="7b066-113">Click Save.</span></span>
8. <span data-ttu-id="7b066-114">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7b066-114">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="7b066-115">Atvieglojumu piemērojamības ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="7b066-115">Benefit eligibility policy</span></span>
1. <span data-ttu-id="7b066-116">Dodieties uz Personāla vadība > Atvieglojumi > Piemērojamība > Atvieglojumu piemērojamības ierobežojumi.</span><span class="sxs-lookup"><span data-stu-id="7b066-116">Go to Human resources > Benefits > Eligibility > Benefit eligibility policies.</span></span>
2. <span data-ttu-id="7b066-117">Atlasiet esošu atvieglojumu ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="7b066-117">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="7b066-118">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="7b066-118">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="7b066-119">Pārslēdziet sadaļas Politikas organizācijas paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="7b066-119">Toggle the expansion of the Policy organizations sections.</span></span>  <span data-ttu-id="7b066-120">Šeit varat pievienot vai noņemt jebkuras organizācijas, kuras vēlaties iekļaut politikā.</span><span class="sxs-lookup"><span data-stu-id="7b066-120">Here you can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="7b066-121">Izvērsiet vai sakļaujiet sadaļu Ierobežojuma nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="7b066-121">Expand or collapse the Policy rules section.</span></span>
6. <span data-ttu-id="7b066-122">Sarakstā atrodiet iepriekš izveidoto ierobežojuma nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="7b066-122">In the list find the policy rule previously created.</span></span>
7. <span data-ttu-id="7b066-123">Noklikšķiniet uz Izveidot ierobežojuma nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="7b066-123">Click Create policy rule.</span></span>
8. <span data-ttu-id="7b066-124">Laukā Spēkā stāšanās datums ievadiet datumu, kurā politikai vajadzētu stāties spēkā.</span><span class="sxs-lookup"><span data-stu-id="7b066-124">In the Effective date field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="7b066-125">Iestatot spēkā stāšanās un beigu datumus, ir iespējams veikt turpmākas ierobežojuma nosacījumu izmaiņas un novērst vajadzību atgriezties pie politikas, lai šīs izmaiņas aktivizētu.</span><span class="sxs-lookup"><span data-stu-id="7b066-125">Setting effective and end dates allows you to make future changes to policy rules and removing the need to come back to the policy when you want those changes to take effect.</span></span>  
9. 
    * <span data-ttu-id="7b066-126">Piemēram, ja jūs vēlaties, lai kārtula attiecas tikai uz pārdošanas daļu vadītājiem, izveidojiet WHERE klauzulu ar loģiku: kur amata apraksts ir vienāds ar pārdošanas daļas vadītājs.</span><span class="sxs-lookup"><span data-stu-id="7b066-126">For example if you wanted the rule to only apply to Sales Managers you could create the Where clause to say: Where position description equals Sales Manager.</span></span>  <span data-ttu-id="7b066-127">Vienā kārtulā varat savienot vairākus WHERE nosacījumus, izmantojot AND vai OR.</span><span class="sxs-lookup"><span data-stu-id="7b066-127">You can And or Or multiple Where statements together in the rule.</span></span>  
10. <span data-ttu-id="7b066-128">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="7b066-128">Click OK.</span></span>
11. <span data-ttu-id="7b066-129">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7b066-129">Close the page.</span></span>
12. <span data-ttu-id="7b066-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7b066-130">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="7b066-131">Nosacījuma piešķiršana atvieglojumam</span><span class="sxs-lookup"><span data-stu-id="7b066-131">Assign rule to benefit</span></span>
1. <span data-ttu-id="7b066-132">Pārejiet uz sadaļu Personāla vadība > Atvieglojumi > Atvieglojumi.</span><span class="sxs-lookup"><span data-stu-id="7b066-132">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="7b066-133">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="7b066-133">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7b066-134">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="7b066-134">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="7b066-135">Izvērsiet vai sakļaujiet sadaļu Piemērotības noteikumi.</span><span class="sxs-lookup"><span data-stu-id="7b066-135">Expand or collapse the Eligibility rules section.</span></span>
5. <span data-ttu-id="7b066-136">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="7b066-136">Click Edit.</span></span>
6. <span data-ttu-id="7b066-137">Laukā Piemērojamība atlasiet no saraksta Atbilstoši nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="7b066-137">In the Eligibility field, select Rule based from the list.</span></span>
7. <span data-ttu-id="7b066-138">Laukā Nosacījuma tips noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="7b066-138">In the Rule type field, click the drop down button to open the lookup.</span></span>
8. <span data-ttu-id="7b066-139">Sarakstā atrodiet un atlasiet iepriekš izveidoto nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="7b066-139">In the list find and select the rule you previously created.</span></span>
9. <span data-ttu-id="7b066-140">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="7b066-140">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="7b066-141">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="7b066-141">Click Save.</span></span>
11. <span data-ttu-id="7b066-142">Aizveriet formu.</span><span class="sxs-lookup"><span data-stu-id="7b066-142">Close the form.</span></span>

