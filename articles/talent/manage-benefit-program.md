---
title: "Atvieglojumu programmas definēšana un pārvaldība"
description: "Personāla vadība sniedz rīkus, ko var izmantot, lai iestatītu un uzturētu atvieglojumus, atvilkumus un darbinieku kompensāciju plānus, kurus uzņēmums piedāvā vai apstrādā saviem darbiniekiem. Šis raksts sniedz informāciju par to, kā iestatīt pārvaldīt atvieglojumus."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 7344fad7c4dffabd99993924604e2e497bebc5ef
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="define-and-manage-a-benefits-program"></a><span data-ttu-id="2cab1-104">Atvieglojumu programmas definēšana un pārvaldība</span><span class="sxs-lookup"><span data-stu-id="2cab1-104">Define and manage a benefits program</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="2cab1-105">Personāla vadība sniedz rīkus, ko var izmantot, lai iestatītu un uzturētu atvieglojumus, atvilkumus un darbinieku kompensāciju plānus, kurus uzņēmums piedāvā vai apstrādā saviem darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="2cab1-105">Human resources provides a set of tools that can be used to set up and maintain benefits, deductions, and workers' compensation plans that an organization offers or processes for its workers.</span></span> <span data-ttu-id="2cab1-106">Šajā tēmā ir sniegta informācija par to, kā iestatīt un pārvaldīt atvieglojumus.</span><span class="sxs-lookup"><span data-stu-id="2cab1-106">This topic provides information about how to set up and manage benefits.</span></span>

<a name="benefit-setup"></a><span data-ttu-id="2cab1-107">Atvieglojumu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="2cab1-107">Benefit setup</span></span>
-------------

<span data-ttu-id="2cab1-108">Pirms darbiniekiem var reģistrēt atvieglojumus, jāizveido katra atvieglojuma elementi.</span><span class="sxs-lookup"><span data-stu-id="2cab1-108">Before workers can be enrolled in benefits, you must create the elements of each benefit.</span></span> <span data-ttu-id="2cab1-109">Šie elementi apvienot līdzīgus atvieglojumu plānus un nosaka noklusējuma iestatījumus, piemēram, ieturējumu likmes un informāciju par uzskaiti.</span><span class="sxs-lookup"><span data-stu-id="2cab1-109">These elements combine similar benefit plans and define default settings, such as deduction rates and accounting details.</span></span> <span data-ttu-id="2cab1-110">Daudzus no šiem iestatījumiem var pielāgot, kad darbinieki tiek vēlāk reģistrēti atvieglojumiem.</span><span class="sxs-lookup"><span data-stu-id="2cab1-110">Many of these settings can be adjusted when workers are later enrolled in the benefit.</span></span> <span data-ttu-id="2cab1-111">Katram atvieglojumu plānam organizācija var piedāvāt vairākas reģistrācijas opcijas, vai darbinieks var atteikties no reģistrācijas plānā.</span><span class="sxs-lookup"><span data-stu-id="2cab1-111">For each benefit plan, an organization can offer several enrollment options, or a worker can waive enrollment in the plan.</span></span> 

<span data-ttu-id="2cab1-112">[![Atvieglojumu procesa plūsma](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span><span class="sxs-lookup"><span data-stu-id="2cab1-112">[![Benefit process flow](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span></span>

## <a name="benefit-elements"></a><span data-ttu-id="2cab1-113">Atvieglojumu elementi</span><span class="sxs-lookup"><span data-stu-id="2cab1-113">Benefit elements</span></span>
<span data-ttu-id="2cab1-114">Pirms sākat veidot atvieglojumus un reģistrēt tajos darbiniekus, ir jādefinē elementi, kas veido atvieglojumu: tips, plāns un opcijas.</span><span class="sxs-lookup"><span data-stu-id="2cab1-114">Before you begin to create to create benefits and enroll workers in them, you must define the elements that make up a benefit: the type, plan, and options.</span></span>

-   <span data-ttu-id="2cab1-115">**Tips** — plānu kopums konkrētiem atvieglojumiem, piemēram, ārstēšanai vai auto novietošanai.</span><span class="sxs-lookup"><span data-stu-id="2cab1-115">**Type** – A collection of plans for a specific benefit, such as medical or parking.</span></span>
-   <span data-ttu-id="2cab1-116">**Plāns** — konkrēti atvieglojumi, kas saskaņā ar līgumu saņemti no nodrošinātāja.</span><span class="sxs-lookup"><span data-stu-id="2cab1-116">**Plan** – A specific benefit that is contracted from a provider.</span></span>
-   <span data-ttu-id="2cab1-117">**Opcija** — seguma līmenis, piemēram, atvieglojumi tikai darbiniekam vai darbiniekam un tā dzīvesbiedram/partnerim.</span><span class="sxs-lookup"><span data-stu-id="2cab1-117">**Option** – The coverage level, such as employee only, or employee and spouse/partner.</span></span>

<span data-ttu-id="2cab1-118">Katram atvieglojumu tipam, piemēram, redzes vai zobu, organizācija saviem darbiniekiem var piedāvāt vienu vai vairākus plānus.</span><span class="sxs-lookup"><span data-stu-id="2cab1-118">For each type of benefit, such as vision or dental, an organization can offer one or more plans to its workers.</span></span> <span data-ttu-id="2cab1-119">Katram plānam organizācija var piedāvāt dažādas opcijas.</span><span class="sxs-lookup"><span data-stu-id="2cab1-119">For each plan, the organization can offer different options.</span></span> <span data-ttu-id="2cab1-120">Piemēram, darbinieki var iegādāties papildu termiņa dzīvības apdrošināšanas segumu, kas vienu, divas vai trīs reizes pārsniedz gada algu.</span><span class="sxs-lookup"><span data-stu-id="2cab1-120">For example, workers can buy additional term life insurance coverage at one, two, or three times their yearly salary.</span></span> <span data-ttu-id="2cab1-121">Katra plānu un opciju kombinācija kļūst par atvieglojumu, kuram darbinieki var reģistrēties.</span><span class="sxs-lookup"><span data-stu-id="2cab1-121">Each combination of a plan and options becomes a benefit that workers can enroll in.</span></span> 

<span data-ttu-id="2cab1-122">[![Atvieglojumu attēls](./media/benefit-pic.png)](./media/benefit-pic.png)</span><span class="sxs-lookup"><span data-stu-id="2cab1-122">[![benefit pic](./media/benefit-pic.png)](./media/benefit-pic.png)</span></span>

## <a name="eligibility"></a><span data-ttu-id="2cab1-123">Piemērojamība</span><span class="sxs-lookup"><span data-stu-id="2cab1-123">Eligibility</span></span>
<span data-ttu-id="2cab1-124">Daudzi faktori ietekmē darbinieka atbilstību dažādiem atvieglojumu tipiem, kurus piedāvā darba devējs.</span><span class="sxs-lookup"><span data-stu-id="2cab1-124">Many factors determine worker eligibility for the various types of benefits that an employer offers.</span></span> <span data-ttu-id="2cab1-125">Kad veidojat atvieglojumu programmatūrā Microsoft Talent, varat iestatīt piemērojamības tipu, kas attiecas uz šo atvieglojumu.</span><span class="sxs-lookup"><span data-stu-id="2cab1-125">When you create a benefit in Microsoft Talent, you can set the type of eligibility that applies to that benefit.</span></span> 

<span data-ttu-id="2cab1-126">Varat padarīt atvieglojumu pieejamu visiem nodarbinātajiem.</span><span class="sxs-lookup"><span data-stu-id="2cab1-126">You can make a benefit available to all workers.</span></span> <span data-ttu-id="2cab1-127">Piemēram, daži uzņēmumi kā papildienākumu piedāvā visiem darbiniekiem stāvvietas caurlaides.</span><span class="sxs-lookup"><span data-stu-id="2cab1-127">For example, some companies offer parking passes to all employees as a fringe benefit.</span></span> <span data-ttu-id="2cab1-128">Veidojot šo atvieglojumu, iestatiet piemērojamību **Visi darbinieki ir piemēroti**.</span><span class="sxs-lookup"><span data-stu-id="2cab1-128">When you create this benefit, you set the eligibility to **All workers are eligible**.</span></span> 

<span data-ttu-id="2cab1-129">Piemērotība neattiecas uz citiem atvieglojumiem, piemēram, ieturējumiem un nodokļu maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="2cab1-129">For other benefits, such as garnishments and tax levies, eligibility doesn't apply.</span></span> <span data-ttu-id="2cab1-130">Izveidojot šo veidu atvieglojumus, ir jāiestata piemērotības opcija **Apiet piemērojamības procesu**.</span><span class="sxs-lookup"><span data-stu-id="2cab1-130">Whey you create these types of benefits, you set the eligibility to **Bypass eligibility process**.</span></span> 

<span data-ttu-id="2cab1-131">Turklāt atvieglojumu piemērotība var būt atkarīga no kārtulām.</span><span class="sxs-lookup"><span data-stu-id="2cab1-131">Finally, benefit eligibility can be rule-based.</span></span> <span data-ttu-id="2cab1-132">Piemēram, uzņēmums piedāvā darbiniekiem divu veidu dzīvības apdrošināšanas atvieglojumus.</span><span class="sxs-lookup"><span data-stu-id="2cab1-132">For example, a company offers two types of life insurance benefit to employees.</span></span> <span data-ttu-id="2cab1-133">Vadošie darbinieki var saņemt vienu dzīvības apdrošināšanas plānu, bet visi citi pilna laika darbinieki var saņemt citu dzīvības apdrošināšanas plānu.</span><span class="sxs-lookup"><span data-stu-id="2cab1-133">Executive employees are eligible for one life insurance plan, whereas all other full-time employees are eligible for the other life insurance plan.</span></span> <span data-ttu-id="2cab1-134">Programmatūrā Talent varat izveidot atvieglojumu piemērotības kārtulu, lai atrastu visus vadošos darbiniekus, un citu kārtulu, lai atrastu visus citus pilna laika darbiniekus, un pēc tam varat lietot šīs kārtulas atbilstošajiem atvieglojumiem.</span><span class="sxs-lookup"><span data-stu-id="2cab1-134">In Talent, you can create a benefit eligibility rule to find all executive employees and another rule to find all other full-time employees, and then apply those rules to the appropriate benefit.</span></span>

## <a name="enrollment"></a><span data-ttu-id="2cab1-135">Reģistrācija</span><span class="sxs-lookup"><span data-stu-id="2cab1-135">Enrollment</span></span>
<span data-ttu-id="2cab1-136">Pēc tam, kad esat izveidojis uzņēmuma piedāvātos atvieglojumus un noteicis piemērojamību, varat reģistrēt jūsu darbiniekus atvieglojumiem.</span><span class="sxs-lookup"><span data-stu-id="2cab1-136">After you've created the benefits that your organization offers and determined eligibility, you can enroll your workers in benefits.</span></span> <span data-ttu-id="2cab1-137">Varat reģistrēt atvieglojumam vienu darbinieku vai varat reģistrēt daudzus darbiniekus vienam vai vairākiem atvieglojumiem vienā procesā.</span><span class="sxs-lookup"><span data-stu-id="2cab1-137">You can enroll a single worker in benefits, or you can enroll many workers in one or more benefits during a single process.</span></span> 

<span data-ttu-id="2cab1-138">Dažreiz organizācija pārtrauc piedāvāt noteiktus atvieglojumus.</span><span class="sxs-lookup"><span data-stu-id="2cab1-138">Sometimes, an organization stops offering certain benefits.</span></span> <span data-ttu-id="2cab1-139">Šādā gadījumā ir jāatjaunina atvieglojumi un nodarbinātie, kuri ir reģistrēti to saņemšanai.</span><span class="sxs-lookup"><span data-stu-id="2cab1-139">In this case, you must update the benefit and the workers who are enrolled in.</span></span> <span data-ttu-id="2cab1-140">Opcija Masveida atvieglojuma piemērošanas beigas sniedz iespēju vienlaikus mainīt gan atvieglojumu nodrošināšanas, gan nodarbināto reģistrācijas šo atvieglojumu saņemšanai beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="2cab1-140">Mass benefit expiration lets you change the expiration date of both a benefit and the worker enrollments for that benefit at the same time.</span></span> <span data-ttu-id="2cab1-141">Varat arī izvēlēties vairākus darbiniekus, kuri ir reģistrējušies atvieglojumiem, un mainīt seguma beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="2cab1-141">You can also select multiple workers who are enrolled in a benefit and change the ending date of their coverage.</span></span> 

<span data-ttu-id="2cab1-142">Līdzīgi, masveida atvieglojumu pagarināšana ļauj pagarināt atvieglojumu un darbinieku reģistrēšanās beigu datumu šim atvieglojumam, ja nolemjat piedāvāt atvieglojumu ilgāk nekā sākotnēji plānots.</span><span class="sxs-lookup"><span data-stu-id="2cab1-142">Similarly, mass benefit extension lets you extend the expiration date of both a benefit and the worker enrollments for that benefit if you decide to offer a benefit longer than you originally planned.</span></span>

<a name="see-also"></a><span data-ttu-id="2cab1-143">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="2cab1-143">See also</span></span>
--------

[<span data-ttu-id="2cab1-144">Atvieglojumu piemērojamības ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="2cab1-144">Benefit eligibility policies</span></span>](benefit-eligibility-policies.md)




