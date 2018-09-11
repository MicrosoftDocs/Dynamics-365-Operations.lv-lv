--- 
title: "Atvieglojumu piemērojamības apstrāde"
description: "Ar šo procedūru tiek parādīts, kā darbojas atvieglojumu piemērojamības process."
author: kherr75
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: b4de57495696fdfa6b7d138a3668fb387ae5e5be
ms.contentlocale: lv-lv
ms.lasthandoff: 09/11/2018

---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="033e5-103">Atvieglojumu piemērojamības apstrāde</span><span class="sxs-lookup"><span data-stu-id="033e5-103">Benefit eligibility process</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="033e5-104">Ar šo procedūru tiek parādīts, kā darbojas atvieglojumu piemērojamības process.</span><span class="sxs-lookup"><span data-stu-id="033e5-104">This procedure hows the benefit eligibility process works.</span></span> <span data-ttu-id="033e5-105">Kad process ir pabeigts, varat skatīt rezultātus.</span><span class="sxs-lookup"><span data-stu-id="033e5-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="033e5-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="033e5-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="033e5-107">Pārejiet uz sadaļu Personāla vadība > Atvieglojumi > Atvieglojumi.</span><span class="sxs-lookup"><span data-stu-id="033e5-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="033e5-108">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="033e5-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="033e5-109">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="033e5-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="033e5-110">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="033e5-110">Click Edit.</span></span>
5. <span data-ttu-id="033e5-111">Laukā Piemērojamība atlasiet vienumu Atbilstoši nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="033e5-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="033e5-112">Laukā Nosacījuma tips atlasiet atvieglojumu ierobežojuma nosacījumu, kuru vēlaties lietot atvieglojumam.</span><span class="sxs-lookup"><span data-stu-id="033e5-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="033e5-113">Darbību rūtī noklikšķiniet uz Atvieglojums.</span><span class="sxs-lookup"><span data-stu-id="033e5-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="033e5-114">Noklikšķiniet uz Izveidot piemērojamības notikumu, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="033e5-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="033e5-115">Laukā Noteikums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="033e5-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="033e5-116">Laukā Apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="033e5-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="033e5-117">Laukā Notikuma veids atlasiet Atvērt reģistrāciju.</span><span class="sxs-lookup"><span data-stu-id="033e5-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="033e5-118">Laukā Vajadzības sākuma datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="033e5-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="033e5-119">Laukā Reģistrācijas perioda sākuma datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="033e5-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="033e5-120">Laukā Reģistrācijas dienas ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="033e5-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="033e5-121">Noklikšķiniet uz Izveidot notikumu.</span><span class="sxs-lookup"><span data-stu-id="033e5-121">Click Create event.</span></span>
16. <span data-ttu-id="033e5-122">Kopsavilkuma cilnē Darbinieki noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="033e5-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="033e5-123">Laukā Parādīt pēc tipa atlasiet Darbinieki.</span><span class="sxs-lookup"><span data-stu-id="033e5-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="033e5-124">Laukā Parādīt pa juridiskajām personām atlasiet Pašreizējā juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="033e5-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="033e5-125">Sarakstā atzīmējiet visas rindas vai noņemiet tām atzīmi.</span><span class="sxs-lookup"><span data-stu-id="033e5-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="033e5-126">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="033e5-126">Click OK.</span></span>
21. <span data-ttu-id="033e5-127">Noklikšķiniet uz Apstrādāt.</span><span class="sxs-lookup"><span data-stu-id="033e5-127">Click Process.</span></span>
22. <span data-ttu-id="033e5-128">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="033e5-128">Click OK.</span></span>
23. <span data-ttu-id="033e5-129">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="033e5-129">Refresh the page.</span></span>
24. <span data-ttu-id="033e5-130">Noklikšķiniet uz Rādīt rezultātus.</span><span class="sxs-lookup"><span data-stu-id="033e5-130">Click Show results.</span></span>
25. <span data-ttu-id="033e5-131">Atveriet kolonnas filtru Statuss.</span><span class="sxs-lookup"><span data-stu-id="033e5-131">Open Status column filter.</span></span>
26. <span data-ttu-id="033e5-132">Kārtot no A uz Z</span><span class="sxs-lookup"><span data-stu-id="033e5-132">Sort A to Z</span></span>


