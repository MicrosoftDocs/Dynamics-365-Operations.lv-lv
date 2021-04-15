---
title: Darbinieka reģistrēšana fiksētās atlīdzības plānā
description: Lai pārvaldītu darbinieku pamata algas, atlīdzību un atvieglojumu vadītājs var piešķirt darbiniekus fiksētu atlīdzību plāniem.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0eeb52bf39160bd89e2164c0dd0413f2781e7a5b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805614"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a><span data-ttu-id="0430a-103">Darbinieka reģistrēšana fiksētās atlīdzības plānā</span><span class="sxs-lookup"><span data-stu-id="0430a-103">Enroll an employee in a fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0430a-104">Lai pārvaldītu darbinieku pamata algas, atlīdzību un atvieglojumu vadītājs var piešķirt darbiniekus fiksētu atlīdzību plāniem.</span><span class="sxs-lookup"><span data-stu-id="0430a-104">The compensation and benefits manager can assign employees to fixed compensation plans to manage their base pay.</span></span> <span data-ttu-id="0430a-105">Šajā procedūrā pieņemts, ka fiksētais plāns ir izveidots un ir aktīvs, un ka plānam ir iestatīti piemērotības nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="0430a-105">This procedure assumes that a fixed plan has been created and is active, and that eligibility rules have been set for the plan.</span></span> <span data-ttu-id="0430a-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="0430a-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0430a-107">Lai sāktu procedūru, dodieties uz Personāla vadība > Darbinieki > Darbinieki > Atlīdzība > Fiksēts plāns</span><span class="sxs-lookup"><span data-stu-id="0430a-107">To begin the procedure, go to Human resources > Workers > Employees > Compensation > Fixed plan</span></span>

1. <span data-ttu-id="0430a-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="0430a-108">Click New.</span></span>
2. <span data-ttu-id="0430a-109">Lai aprakstītu darbinieka atlīdzības izmaiņas, laukā Darbība atlasiet Fiksētās kompensācijas darbība ar tipu Pieņemt darbā/atkārtoti pieņemt darbā.</span><span class="sxs-lookup"><span data-stu-id="0430a-109">In the Action field, select a Fixed compensation action of type Hire/Rehire to describe the change in the employee's compensation.</span></span>
3. <span data-ttu-id="0430a-110">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0430a-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0430a-111">Laukā Amats noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0430a-111">In the Position field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="0430a-112">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0430a-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0430a-113">Līmenis, kas tiek parādīts, ir nolasīts no mainīgā Atlīdzības līmenis, kas atbilst pozīcijas darbam.</span><span class="sxs-lookup"><span data-stu-id="0430a-113">The level that's displayed is from the Compensation Level of the Job on the Position.</span></span> <span data-ttu-id="0430a-114">Pirms darbiniekam būs iespējams piešķirt atlīdzību, ir jāiestata uz darbu attiecināmais līmenis.</span><span class="sxs-lookup"><span data-stu-id="0430a-114">The level must be set on the Job before compensation can be assigned to the employee.</span></span>  
6. <span data-ttu-id="0430a-115">Laukā Plāns atlasiet darbinieka fiksēto atlīdzības plānu.</span><span class="sxs-lookup"><span data-stu-id="0430a-115">In the Plan field, select the fixed compensation plan for the employee.</span></span> <span data-ttu-id="0430a-116">Plāna meklēšana tiek filtrēta, lai parādītu tikai tos plānus, uz kuriem darbinieks ir tiesīgs, pamatojoties uz iestatījumiem sadaļā Piemērotības noteikumi.</span><span class="sxs-lookup"><span data-stu-id="0430a-116">The Plan lookup is filtered to show only the plans that the employee is eligible for based on the Eligibility rules.</span></span>
7. <span data-ttu-id="0430a-117">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0430a-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0430a-118">Atlīdzības efektīvais un termiņa beigu datumi pēc noklusējuma tiek ņemti no darbinieka amata piešķiršanas sākuma un beigu datumiem.</span><span class="sxs-lookup"><span data-stu-id="0430a-118">The Effective and Expiration dates for the compensation default from the start and end dates for the worker's position assignment.</span></span> <span data-ttu-id="0430a-119">Šos datumus varat mainīt pēc vajadzības.</span><span class="sxs-lookup"><span data-stu-id="0430a-119">You can adjust these dates as needed.</span></span>  
    * <span data-ttu-id="0430a-120">Ja mainīgā Fiksētās atlīdzības plāns vērtība ir soļu plāns, atlasiet soli, kas satur darbiniekam atbilstošu algas likmi.</span><span class="sxs-lookup"><span data-stu-id="0430a-120">If the Fixed compensation plan is a step plan, select the step containing the correct pay rate for the employee.</span></span> <span data-ttu-id="0430a-121">Ja mainīgā Fiksētās atlīdzības plāns vērtība ir pakāpenisks vai indeksēts plāns, atlasiet darbiniekam atbilstošu algas likmi.</span><span class="sxs-lookup"><span data-stu-id="0430a-121">If the fixed compensation plan is a grade or a band plan, enter the pay rate for the employee.</span></span> <span data-ttu-id="0430a-122">Algas likme tiks validēta pēc plāna tolerances iestatījumiem, kā arī darba atlīdzības līmeņa minimālo un maksimālo atsauces punktu.</span><span class="sxs-lookup"><span data-stu-id="0430a-122">The pay rate will be validated against the tolerance settings for the plan, and the minimum and maximum reference points for the job's compensation level.</span></span>  
8. <span data-ttu-id="0430a-123">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0430a-123">Click OK.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]