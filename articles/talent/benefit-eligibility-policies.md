---
title: "Atvieglojumu piemērojamības ierobežojumi"
description: "Šajā rakstā ir sniegta informācija par atvieglojumu piemērojamības ierobežojumiem, kas jums palīdz noteikt, kurš ir piemērots noteiktu atvieglojumu saņemšanai."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 682100881d6ea8c1e02db50629208c765600c49a
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="benefit-eligibility-policies"></a><span data-ttu-id="a8ab1-103">Atvieglojumu piemērojamības ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="a8ab1-103">Benefit eligibility policies</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="a8ab1-104">Šajā tēmā ir sniegta informācija par atvieglojumu piemērojamības ierobežojumiem, kas jums palīdz noteikt, kurš ir piemērots noteiktu atvieglojumu saņemšanai.</span><span class="sxs-lookup"><span data-stu-id="a8ab1-104">This topic provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="a8ab1-105">Veidojot priekšrocības, ir jāizlemj, kuriem darbiniekiem tās būs pieejamas.</span><span class="sxs-lookup"><span data-stu-id="a8ab1-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="a8ab1-106">Tālāk redzamajā tabulā ir parādīti piemēri priekšrocībām, kuras var iespējot konkrētiem darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="a8ab1-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="a8ab1-107">Atvieglojumi</span><span class="sxs-lookup"><span data-stu-id="a8ab1-107">Benefit</span></span>          | <span data-ttu-id="a8ab1-108">Kam šī priekšrocība ir pieejama</span><span class="sxs-lookup"><span data-stu-id="a8ab1-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="a8ab1-109">Veselības apdrošināšana</span><span class="sxs-lookup"><span data-stu-id="a8ab1-109">Health insurance</span></span> | <span data-ttu-id="a8ab1-110">Visi darbinieki</span><span class="sxs-lookup"><span data-stu-id="a8ab1-110">All employees</span></span>                   |
| <span data-ttu-id="a8ab1-111">Mobilais tālrunis</span><span class="sxs-lookup"><span data-stu-id="a8ab1-111">Mobile phone</span></span>     | <span data-ttu-id="a8ab1-112">Pārdošanas daļa, vadītāji</span><span class="sxs-lookup"><span data-stu-id="a8ab1-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="a8ab1-113">Stāvvietas caurlaide</span><span class="sxs-lookup"><span data-stu-id="a8ab1-113">Parking passes</span></span>   | <span data-ttu-id="a8ab1-114">Vadošie darbinieki</span><span class="sxs-lookup"><span data-stu-id="a8ab1-114">Executives</span></span>                      |

<span data-ttu-id="a8ab1-115">Lai izveidotu piemērojamības ierobežojumus, tiek izmantoti tālāk minētie komponenti.</span><span class="sxs-lookup"><span data-stu-id="a8ab1-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="a8ab1-116">Ierobežojuma nosacījumu veidi</span><span class="sxs-lookup"><span data-stu-id="a8ab1-116">Policy rule types</span></span>
-   <span data-ttu-id="a8ab1-117">Atvieglojumu piemērojamības ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="a8ab1-117">Benefit eligibility policies</span></span>

<span data-ttu-id="a8ab1-118">Ierobežojuma nosacījumu veidi definē vaicājuma parametrus, kas tiek izmantoti, izstrādājot noteiktus ierobežojuma nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="a8ab1-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="a8ab1-119">Pēc ierobežojuma nosacījumu veidu izveides, var izveidot priekšrocības piemērojamības ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="a8ab1-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="a8ab1-120">Politikas ļauj izveidot noteikumu kopu, kas tiek lietota vienai vai vairākām juridiskām personām.</span><span class="sxs-lookup"><span data-stu-id="a8ab1-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="a8ab1-121">Katras politikas ietvaros varat skatīt jebkuru priekšrocības piemērojamības ierobežojuma nosacījumu veidu, ko izveidojāt agrāk.</span><span class="sxs-lookup"><span data-stu-id="a8ab1-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="a8ab1-122">Definējiet nosacījumu tvērumu ierobežojumu ietvaros.</span><span class="sxs-lookup"><span data-stu-id="a8ab1-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="a8ab1-123">Piemēram, ja izveidojat priekšrocību piemērojamības ierobežojuma nosacījumu veidu ar nosaukumu **Vadītāji**, varat norādīt šī nosacījuma lomu saistībā ar šo politiku.</span><span class="sxs-lookup"><span data-stu-id="a8ab1-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="a8ab1-124">Šajā piemērā nosacījums var noteikt, ka nosacījumā jāietver visi amata nosaukumi, kas satur vārdu “vadītājs”.</span><span class="sxs-lookup"><span data-stu-id="a8ab1-124">In this example, the rule might state that any job title that contains the word “executive” should be included in the rule.</span></span> <span data-ttu-id="a8ab1-125">Pēc tam, kad esat definējis nosacījumu parametrus vai nosacījumus, kas tiek iekļauti ierobežojumos, varat piešķirt noteikt nosacījumu priekšrocībai.</span><span class="sxs-lookup"><span data-stu-id="a8ab1-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>

<a name="see-also"></a><span data-ttu-id="a8ab1-126">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="a8ab1-126">See also</span></span>
--------

[<span data-ttu-id="a8ab1-127">Atvieglojumu programmas definēšana un pārvaldīšana</span><span class="sxs-lookup"><span data-stu-id="a8ab1-127">Defining and managing a benefit program</span></span>](manage-benefit-program.md)




