---
title: Atvieglojumu piemērotības kārtulu un ierobežojumu definēšana
description: Šajā rakstā parādīts, kā izveidot atvieglojumu piemērotības kārtulas un ierobežojumus un pēc tam piešķirt kārtulas atvieglojumiem.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 046b045fbdda125c5a2259783c0347f687453528
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053157"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="3ffd7-103">Atvieglojumu piemērotības kārtulu un ierobežojumu definēšana</span><span class="sxs-lookup"><span data-stu-id="3ffd7-103">Define benefit eligibility rules and policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3ffd7-104">Šajā tēmā parādīts, kā izveidot atvieglojumu piemērotības kārtulas un ierobežojumus un pēc tam piešķirt kārtulas atvieglojumiem.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-104">This topic shows you how you can create benefit eligibility rules and policies and then assign rules to benefits.</span></span>  

## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="3ffd7-105">Atvieglojumu piemērojamības ierobežojuma nosacījumu tipa izveide</span><span class="sxs-lookup"><span data-stu-id="3ffd7-105">Create benefit eligibility policy rule type</span></span>

1. <span data-ttu-id="3ffd7-106">Dodieties uz **Personāla vadība > Atvieglojumi > Piemērojamība > Atvieglojumu piemērojamības ierobežojumu nosacījumu tipi**.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-106">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policy rule types**.</span></span>
2. <span data-ttu-id="3ffd7-107">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-107">Select **New**.</span></span>
3. <span data-ttu-id="3ffd7-108">Ievadiet vērtību laukā **Nosacījuma nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-108">In the **Rule name** field, enter a value.</span></span>
4. <span data-ttu-id="3ffd7-109">Laukā **Apraksts** ievadiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-109">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="3ffd7-110">Laukā **Vaicājuma nosaukums** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-110">In the **Query name** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="3ffd7-111">Sarakstā atlasiet saiti atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-111">In the list, select the link in the selected row.</span></span>
7. <span data-ttu-id="3ffd7-112">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-112">Select **Save**.</span></span>
8. <span data-ttu-id="3ffd7-113">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-113">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="3ffd7-114">Atvieglojumu piemērojamības ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="3ffd7-114">Benefit eligibility policy</span></span>

1. <span data-ttu-id="3ffd7-115">Dodieties uz **Personāla vadība > Atvieglojumi > Piemērojamība > Atvieglojumu piemērojamības ierobežojumi**.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-115">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policies**.</span></span>
2. <span data-ttu-id="3ffd7-116">Atlasiet esošu atvieglojumu ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-116">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="3ffd7-117">Sarakstā atlasiet saiti atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-117">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="3ffd7-118">Pārslēdziet sadaļas **Politikas organizācijas** paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-118">Toggle the expansion of the **Policy organizations** sections.</span></span> <span data-ttu-id="3ffd7-119">Varat pievienot vai noņemt jebkuras organizācijas, kuras vēlaties iekļaut politikā.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-119">You can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="3ffd7-120">Izvērsiet vai sakļaujiet sadaļu **Ierobežojuma nosacījumi**.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-120">Expand or collapse the **Policy rules** section.</span></span>
6. <span data-ttu-id="3ffd7-121">Sarakstā atrodiet iepriekš izveidoto ierobežojuma nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-121">In the list, find the policy rule previously created.</span></span>
7. <span data-ttu-id="3ffd7-122">Atlasiet **Izveidot ierobežojuma nosacījumu**.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-122">Select **Create policy rule**.</span></span>
8. <span data-ttu-id="3ffd7-123">Laukā **Spēkā stāšanās datums** ievadiet datumu, kurā politikai vajadzētu stāties spēkā.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-123">In the **Effective date** field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="3ffd7-124">Iestatot spēkā stāšanās beigu datumus, ir iespējams veikt turpmākas ierobežojuma nosacījumu izmaiņas, tādēļ nebūs jāatgriežas pie politikas, lai šīs izmaiņas aktivizētu.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-124">Setting effective end dates allows you to make future changes to policy rules so you don't need to come back to the policy when you want those changes to take effect.</span></span>  
9. <span data-ttu-id="3ffd7-125">Ja nepieciešams, pievienojiet klauzulu laukā **Pievienot nosacījumu**.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-125">If needed, add a where clause to the **Add condition** field.</span></span>
    * <span data-ttu-id="3ffd7-126">Piemēram, ja jūs vēlaties, lai kārtula attiecas tikai uz pārdošanas daļu vadītājiem, izveidojiet ¨kur¨ klauzulu ar loģiku: kur amata apraksts ir vienāds ar pārdošanas daļas vadītājs.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-126">For example if you wanted the rule to only apply to Sales Managers you could create the where clause to say: Where position description equals Sales Manager.</span></span> <span data-ttu-id="3ffd7-127">Vienā kārtulā varat pievienot vairākus ¨kur¨ nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-127">You can add multiple where statements together in the rule.</span></span>  
10. <span data-ttu-id="3ffd7-128">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-128">Select **OK**.</span></span>
11. <span data-ttu-id="3ffd7-129">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-129">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="3ffd7-130">Nosacījuma piešķiršana atvieglojumam</span><span class="sxs-lookup"><span data-stu-id="3ffd7-130">Assign rule to benefit</span></span>

1. <span data-ttu-id="3ffd7-131">Pārejiet uz sadaļu **Personāla vadība > Atvieglojumi > Atvieglojumi**.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-131">Go to **Human resources > Benefits > Benefits**.</span></span>
2. <span data-ttu-id="3ffd7-132">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-132">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3ffd7-133">Sarakstā atlasiet saiti atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-133">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="3ffd7-134">Izvērsiet vai sakļaujiet sadaļu **Piemērotības noteikumi**.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-134">Expand or collapse the **Eligibility rules** section.</span></span>
5. <span data-ttu-id="3ffd7-135">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-135">Select **Edit**.</span></span>
6. <span data-ttu-id="3ffd7-136">Laukā **Piemērojamība** atlasiet kārtulu.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-136">In the **Eligibility** field, select the rule.</span></span>
7. <span data-ttu-id="3ffd7-137">Laukā **Kārtulas veids** atlasiet iepriekš izveidoto nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-137">In the **Rule type** field, select the rule you previously created.</span></span>
9. <span data-ttu-id="3ffd7-138">Sarakstā atlasiet saiti atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-138">In the list, select the link in the selected row.</span></span>
10. <span data-ttu-id="3ffd7-139">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-139">Select **Save**.</span></span>
11. <span data-ttu-id="3ffd7-140">Aizveriet formu.</span><span class="sxs-lookup"><span data-stu-id="3ffd7-140">Close the form.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]