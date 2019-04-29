---
title: Amatu iestatīšana
description: Amats ir nozīmīgs organizācijas hierarhijas zemāko līmeņu elements.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, HcmWorkforceWorkspace, HcmWorkerActivityChart, HcmAllWorkersListPart, HcmPosition, HcmPositionNewPosition, HcmJobLookup, HcmPositionReportsToDialog, HcmPositionLookup, FinancialDimensionDefaultTemplatesLookup, DimensionLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4fd355fb6c3d2742e046a616585ca349c623341d
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/19/2019
ms.locfileid: "856834"
---
# <a name="set-up-positions"></a><span data-ttu-id="b37fe-103">Amatu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="b37fe-103">Set up positions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b37fe-104">Amats ir nozīmīgs organizācijas hierarhijas zemāko līmeņu elements.</span><span class="sxs-lookup"><span data-stu-id="b37fe-104">Positions are an important element of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="b37fe-105">Pozīcija ir atsevišķa darba instance.</span><span class="sxs-lookup"><span data-stu-id="b37fe-105">A position is an individual instance of a job.</span></span> <span data-ttu-id="b37fe-106">Piemēram, amats “Pārdošanas daļas vadītājs (austrumu reģions)” ir tikai viens no amatiem, kas ir saistīti ar darbu “Pārdošanas daļas vadītājs”.</span><span class="sxs-lookup"><span data-stu-id="b37fe-106">For example, the position, “Sales manager (East),” is one of the positions that is associated with the job, “Sales manager.”</span></span> <span data-ttu-id="b37fe-107">Amats pastāv nodaļā, un ar to var būt saistīts tikai viens darbinieks.</span><span class="sxs-lookup"><span data-stu-id="b37fe-107">A position exists in a department and may have only one worker associated with it.</span></span> <span data-ttu-id="b37fe-108">Šajā uzdevumā mēs izklāstīsim darbības, kas ir jāizpilda, lai izveidotu amatu.</span><span class="sxs-lookup"><span data-stu-id="b37fe-108">In this task we will walk through the steps required to create a position.</span></span> <span data-ttu-id="b37fe-109">Šī procedūra ir paredzēta personāla vadības speciālistam.</span><span class="sxs-lookup"><span data-stu-id="b37fe-109">This procedure is intended for Human Resources Specialists.</span></span>

1. <span data-ttu-id="b37fe-110">Noklikšķiniet uz Darbaspēka pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="b37fe-110">Click Workforce management.</span></span>
2. <span data-ttu-id="b37fe-111">Noklikšķiniet uz Vakantie amati.</span><span class="sxs-lookup"><span data-stu-id="b37fe-111">Click Open positions.</span></span>
3. <span data-ttu-id="b37fe-112">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b37fe-112">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="b37fe-113">Laukā Darbs ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b37fe-113">In the Job field, enter or select a value.</span></span>
    * <span data-ttu-id="b37fe-114">Amatā no atlasītā darba automātiski tiek kopēts darba apraksts, amats un pilna darba laika ekvivalenta nodarbinātības koeficients.</span><span class="sxs-lookup"><span data-stu-id="b37fe-114">The Job description, title, and full-time equivalent employment factor are automatically copied from the selected job into the position.</span></span>  
5. <span data-ttu-id="b37fe-115">ResolveChanges vienumam Darbs.</span><span class="sxs-lookup"><span data-stu-id="b37fe-115">ResolveChanges the Job.</span></span>
6. <span data-ttu-id="b37fe-116">Noklikšķiniet uz Izveidot amatu.</span><span class="sxs-lookup"><span data-stu-id="b37fe-116">Click Create position.</span></span>
7. <span data-ttu-id="b37fe-117">Laukā Nodaļa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b37fe-117">In the Department field, enter or select a value.</span></span>
8. <span data-ttu-id="b37fe-118">Laukā Amata tips ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b37fe-118">In the Position type field, enter or select a value.</span></span>
9. <span data-ttu-id="b37fe-119">Laukā Atlīdzības reģions ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b37fe-119">In the Compensation region field, enter or select a value.</span></span>
    * <span data-ttu-id="b37fe-120">Lauks Atlīdzības reģions nosaka noteikumus par piemērotību atlīdzības saņemšanai un fiksētus pielikuma budžetus, kas attiecas uz darbinieku attiecīgajā amatā.</span><span class="sxs-lookup"><span data-stu-id="b37fe-120">The Compensation region field determines the compensation eligibility rules and fixed increase budgets that apply to an employee in that position.</span></span>  
10. <span data-ttu-id="b37fe-121">Laukā Pieejams piešķirei ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="b37fe-121">In the Available for assignment field, enter a date and time.</span></span>
11. <span data-ttu-id="b37fe-122">Izvērsiet sadaļu Amata ieņemšanas ilgums.</span><span class="sxs-lookup"><span data-stu-id="b37fe-122">Expand the Position duration section.</span></span>
    * <span data-ttu-id="b37fe-123">Amata ieņemšanas ilgums tiek ievadīts pēc noklusējuma, pamatojoties uz iepriekš ievadītajiem aktivizēšanas un pensionēšanās datumiem</span><span class="sxs-lookup"><span data-stu-id="b37fe-123">Position duration is entered by default based on activation and retirement dates entered earlier</span></span>  
12. <span data-ttu-id="b37fe-124">Izvērsiet sadaļu Pakļautās personas amats.</span><span class="sxs-lookup"><span data-stu-id="b37fe-124">Expand the Reports to position section.</span></span>
    * <span data-ttu-id="b37fe-125">Kad darbinieku piešķirat kādam amatam, kas ir pakļauts citam amatam, jūs izveidojat tiešas pakļautības attiecības starp darbiniekiem, kuri ir piešķirti šiem abiem amatiem.</span><span class="sxs-lookup"><span data-stu-id="b37fe-125">When you assign a worker to a position that reports to another position, you create a direct reporting relationship between the workers who are assigned to the two positions.</span></span>  
13. <span data-ttu-id="b37fe-126">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b37fe-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="b37fe-127">Laukā Pakļautība ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="b37fe-127">In the Reports to field, enter or select a value.</span></span>
15. <span data-ttu-id="b37fe-128">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="b37fe-128">Click Create.</span></span>
16. <span data-ttu-id="b37fe-129">Izvērsiet sadaļu Darbinieka piešķire.</span><span class="sxs-lookup"><span data-stu-id="b37fe-129">Expand the Worker assignment section.</span></span>
17. <span data-ttu-id="b37fe-130">Izvērsiet sadaļu Attiecības.</span><span class="sxs-lookup"><span data-stu-id="b37fe-130">Expand the Relationships section.</span></span>
    * <span data-ttu-id="b37fe-131">Ja jūsu organizācija izmanto matricas hierarhiju vai citu pielāgotu hierarhiju, varat iestatīt amatu hierarhijas tipus un pēc tam pievienot katra iestatītā hierarhijas tipa matiem pakļautības attiecības.</span><span class="sxs-lookup"><span data-stu-id="b37fe-131">If your organization uses a matrix hierarchy or another custom hierarchy, you can set up position hierarchy types and then add reporting relationships to positions for each hierarchy type that you set up.</span></span>  
18. <span data-ttu-id="b37fe-132">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b37fe-132">Click Add.</span></span>
19. <span data-ttu-id="b37fe-133">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="b37fe-133">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="b37fe-134">Laukā Hierarhijas nosaukums ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="b37fe-134">In the Hierarchy name field, enter or select a value.</span></span>
21. <span data-ttu-id="b37fe-135">Laukā Pakļautās personas amats ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="b37fe-135">In the Reports to position field, enter or select a value.</span></span>
22. <span data-ttu-id="b37fe-136">Izvērsiet sadaļu Alga.</span><span class="sxs-lookup"><span data-stu-id="b37fe-136">Expand the Payroll section.</span></span>
23. <span data-ttu-id="b37fe-137">Laukā Apmaksas cikls ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b37fe-137">In the Pay cycle field, enter or select a value.</span></span>
24. <span data-ttu-id="b37fe-138">Laukā Apmaksa pēc ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b37fe-138">In the Paid by field, enter or select a value.</span></span>
25. <span data-ttu-id="b37fe-139">Laukā Gada parasto stundu skaits ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="b37fe-139">In the Annual regular hours field, enter a number.</span></span>
    * <span data-ttu-id="b37fe-140">Šis ir parasti apmaksāto stundu skaits, kādu šo amatu ieņemošam darbiniekam ir plānots nostrādāt katru gadu.</span><span class="sxs-lookup"><span data-stu-id="b37fe-140">This is the number of regularly paid hours that the worker in this position is expected to work each year.</span></span>  
26. <span data-ttu-id="b37fe-141">Izvērsiet sadaļu Arodbiedrība.</span><span class="sxs-lookup"><span data-stu-id="b37fe-141">Expand the Labor union section.</span></span>
27. <span data-ttu-id="b37fe-142">Sakļaujiet sadaļu Arodbiedrība.</span><span class="sxs-lookup"><span data-stu-id="b37fe-142">Collapse the Labor union section.</span></span>
28. <span data-ttu-id="b37fe-143">Izvērsiet sadaļu Finanšu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="b37fe-143">Expand the Financial dimensions section.</span></span>
29. <span data-ttu-id="b37fe-144">Laukā Sadales veidne ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b37fe-144">In the Distribution template field, enter or select a value.</span></span>
30. <span data-ttu-id="b37fe-145">Laukā Nodaļa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b37fe-145">In the Department field, enter or select a value.</span></span>
31. <span data-ttu-id="b37fe-146">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b37fe-146">Click Save.</span></span>

