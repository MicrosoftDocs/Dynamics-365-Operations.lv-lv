---
title: Atvieglojumu piemērojamības ierobežojumi
description: Šajā rakstā ir sniegta informācija par atvieglojumu piemērojamības ierobežojumiem, kas jums palīdz noteikt, kurš ir piemērots noteiktu atvieglojumu saņemšanai.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 5bd11e5dceb831968c8458ec07d2aca8fb660763
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898484"
---
# <a name="benefit-eligibility-policies"></a><span data-ttu-id="02d2f-103">Atvieglojumu piemērojamības ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="02d2f-103">Benefit eligibility policies</span></span>

<span data-ttu-id="02d2f-104">Šajā tēmā ir sniegta informācija par atvieglojumu piemērojamības ierobežojumiem, kas jums palīdz noteikt, kurš ir piemērots noteiktu atvieglojumu saņemšanai.</span><span class="sxs-lookup"><span data-stu-id="02d2f-104">This topic provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="02d2f-105">Veidojot priekšrocības, ir jāizlemj, kuriem darbiniekiem tās būs pieejamas.</span><span class="sxs-lookup"><span data-stu-id="02d2f-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="02d2f-106">Tālāk redzamajā tabulā ir parādīti piemēri priekšrocībām, kuras var iespējot konkrētiem darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="02d2f-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="02d2f-107">Atvieglojumi</span><span class="sxs-lookup"><span data-stu-id="02d2f-107">Benefit</span></span>          | <span data-ttu-id="02d2f-108">Kam šī priekšrocība ir pieejama</span><span class="sxs-lookup"><span data-stu-id="02d2f-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="02d2f-109">Veselības apdrošināšana</span><span class="sxs-lookup"><span data-stu-id="02d2f-109">Health insurance</span></span> | <span data-ttu-id="02d2f-110">Visi darbinieki</span><span class="sxs-lookup"><span data-stu-id="02d2f-110">All employees</span></span>                   |
| <span data-ttu-id="02d2f-111">Mobilais tālrunis</span><span class="sxs-lookup"><span data-stu-id="02d2f-111">Mobile phone</span></span>     | <span data-ttu-id="02d2f-112">Pārdošanas daļa, vadītāji</span><span class="sxs-lookup"><span data-stu-id="02d2f-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="02d2f-113">Stāvvietas caurlaide</span><span class="sxs-lookup"><span data-stu-id="02d2f-113">Parking passes</span></span>   | <span data-ttu-id="02d2f-114">Vadošie darbinieki</span><span class="sxs-lookup"><span data-stu-id="02d2f-114">Executives</span></span>                      |

<span data-ttu-id="02d2f-115">Lai izveidotu piemērojamības ierobežojumus, tiek izmantoti tālāk minētie komponenti.</span><span class="sxs-lookup"><span data-stu-id="02d2f-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="02d2f-116">Ierobežojuma nosacījumu veidi</span><span class="sxs-lookup"><span data-stu-id="02d2f-116">Policy rule types</span></span>
-   <span data-ttu-id="02d2f-117">Atvieglojumu piemērojamības ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="02d2f-117">Benefit eligibility policies</span></span>

<span data-ttu-id="02d2f-118">Ierobežojuma nosacījumu veidi definē vaicājuma parametrus, kas tiek izmantoti, izstrādājot noteiktus ierobežojuma nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="02d2f-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="02d2f-119">Pēc ierobežojuma nosacījumu veidu izveides, var izveidot priekšrocības piemērojamības ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="02d2f-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="02d2f-120">Politikas ļauj izveidot noteikumu kopu, kas tiek lietota vienai vai vairākām juridiskām personām.</span><span class="sxs-lookup"><span data-stu-id="02d2f-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="02d2f-121">Katras politikas ietvaros varat skatīt jebkuru priekšrocības piemērojamības ierobežojuma nosacījumu veidu, ko izveidojāt agrāk.</span><span class="sxs-lookup"><span data-stu-id="02d2f-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="02d2f-122">Definējiet nosacījumu tvērumu ierobežojumu ietvaros.</span><span class="sxs-lookup"><span data-stu-id="02d2f-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="02d2f-123">Piemēram, ja izveidojat priekšrocību piemērojamības ierobežojuma nosacījumu veidu ar nosaukumu **Vadītāji**, varat norādīt šī nosacījuma lomu saistībā ar šo politiku.</span><span class="sxs-lookup"><span data-stu-id="02d2f-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="02d2f-124">Šajā piemērā nosacījums var noteikt, ka nosacījumā jāietver visi amata nosaukumi, kas satur vārdu "vadītājs".</span><span class="sxs-lookup"><span data-stu-id="02d2f-124">In this example, the rule might state that any job title that contains the word "executive" should be included in the rule.</span></span> <span data-ttu-id="02d2f-125">Pēc tam, kad esat definējis nosacījumu parametrus vai nosacījumus, kas tiek iekļauti ierobežojumos, varat piešķirt noteikt nosacījumu priekšrocībai.</span><span class="sxs-lookup"><span data-stu-id="02d2f-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>

<a name="additional-resources"></a><span data-ttu-id="02d2f-126">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="02d2f-126">Additional resources</span></span>
--------

[<span data-ttu-id="02d2f-127">Atvieglojumu programmas definēšana un pārvaldība</span><span class="sxs-lookup"><span data-stu-id="02d2f-127">Define and manage a benefits program</span></span>](manage-benefit-program.md)



