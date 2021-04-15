---
title: Atvieglojumu piemērojamības apstrāde
description: Šīs procedūras aprakstā ir paskaidrots, kā darbojas atvieglojumu piemērojamības noteikšanas process.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 55137cfa62f40713b2aed740f08ab5ead53b46d8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805878"
---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="f0cef-103">Atvieglojumu piemērojamības apstrāde</span><span class="sxs-lookup"><span data-stu-id="f0cef-103">Benefit eligibility process</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f0cef-104">Šīs procedūras aprakstā ir paskaidrots, kā darbojas atvieglojumu piemērojamības noteikšanas process.</span><span class="sxs-lookup"><span data-stu-id="f0cef-104">This procedure shows how the benefit eligibility process works.</span></span> <span data-ttu-id="f0cef-105">Kad process ir pabeigts, varat skatīt rezultātus.</span><span class="sxs-lookup"><span data-stu-id="f0cef-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="f0cef-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="f0cef-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="f0cef-107">Pārejiet uz sadaļu Personāla vadība > Atvieglojumi > Atvieglojumi.</span><span class="sxs-lookup"><span data-stu-id="f0cef-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="f0cef-108">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f0cef-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f0cef-109">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f0cef-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f0cef-110">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="f0cef-110">Click Edit.</span></span>
5. <span data-ttu-id="f0cef-111">Laukā Piemērojamība atlasiet vienumu Atbilstoši nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="f0cef-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="f0cef-112">Laukā Nosacījuma tips atlasiet atvieglojumu ierobežojuma nosacījumu, kuru vēlaties lietot atvieglojumam.</span><span class="sxs-lookup"><span data-stu-id="f0cef-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="f0cef-113">Darbību rūtī noklikšķiniet uz Atvieglojums.</span><span class="sxs-lookup"><span data-stu-id="f0cef-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="f0cef-114">Noklikšķiniet uz Izveidot piemērojamības notikumu, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="f0cef-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="f0cef-115">Laukā Noteikums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="f0cef-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="f0cef-116">Laukā Apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f0cef-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="f0cef-117">Laukā Notikuma veids atlasiet Atvērt reģistrāciju.</span><span class="sxs-lookup"><span data-stu-id="f0cef-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="f0cef-118">Laukā Vajadzības sākuma datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="f0cef-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="f0cef-119">Laukā Reģistrācijas perioda sākuma datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="f0cef-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="f0cef-120">Laukā Reģistrācijas dienas ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="f0cef-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="f0cef-121">Noklikšķiniet uz Izveidot notikumu.</span><span class="sxs-lookup"><span data-stu-id="f0cef-121">Click Create event.</span></span>
16. <span data-ttu-id="f0cef-122">Kopsavilkuma cilnē Darbinieki noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="f0cef-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="f0cef-123">Laukā Parādīt pēc tipa atlasiet Darbinieki.</span><span class="sxs-lookup"><span data-stu-id="f0cef-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="f0cef-124">Laukā Parādīt pa juridiskajām personām atlasiet Pašreizējā juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="f0cef-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="f0cef-125">Sarakstā atzīmējiet visas rindas vai noņemiet tām atzīmi.</span><span class="sxs-lookup"><span data-stu-id="f0cef-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="f0cef-126">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f0cef-126">Click OK.</span></span>
21. <span data-ttu-id="f0cef-127">Noklikšķiniet uz Apstrādāt.</span><span class="sxs-lookup"><span data-stu-id="f0cef-127">Click Process.</span></span>
22. <span data-ttu-id="f0cef-128">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f0cef-128">Click OK.</span></span>
23. <span data-ttu-id="f0cef-129">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="f0cef-129">Refresh the page.</span></span>
24. <span data-ttu-id="f0cef-130">Noklikšķiniet uz Rādīt rezultātus.</span><span class="sxs-lookup"><span data-stu-id="f0cef-130">Click Show results.</span></span>
25. <span data-ttu-id="f0cef-131">Atveriet kolonnas filtru Statuss.</span><span class="sxs-lookup"><span data-stu-id="f0cef-131">Open Status column filter.</span></span>
26. <span data-ttu-id="f0cef-132">Kārtot no A uz Z</span><span class="sxs-lookup"><span data-stu-id="f0cef-132">Sort A to Z</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]