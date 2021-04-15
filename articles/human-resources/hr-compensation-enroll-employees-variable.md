---
title: Darbinieka reģistrēšana mainīgās atlīdzības plānā
description: Atlīdzību un atvieglojumu vadītājs var reģistrēt darbiniekus mainīgās atlīdzības plānos, lai aprēķinātu skaidras un bezskaidras naudas piemaksas darbiniekiem.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompVarEnrollEmpl, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f31790dc9389eaed125f69e4039d06a8b28bcc8b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793733"
---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a><span data-ttu-id="37732-103">Darbinieka reģistrēšana mainīgās atlīdzības plānā</span><span class="sxs-lookup"><span data-stu-id="37732-103">Enroll an employee in a variable compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="37732-104">Atlīdzību un atvieglojumu vadītājs var reģistrēt darbiniekus mainīgās atlīdzības plānos, lai aprēķinātu skaidras un bezskaidras naudas piemaksas darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="37732-104">The Compensation and Benefits manager can enroll employees in variable compensation plans to calculate cash and non-cash awards for employees.</span></span> <span data-ttu-id="37732-105">Šajā procedūrā tiek pieņemts, ka mainīgās atlīdzības plāns ir izveidots, laukā Iespējot reģistrācijas iestatot vērtību Jā, un ka mainīgās atlīdzības plānam ir izveidoti piemērotības nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="37732-105">This procedure assumes that a variable compensation plan has been created with the Enable enrolment field set to Yes, and that eligibility rules have been created for that variable compensation plan.</span></span> <span data-ttu-id="37732-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="37732-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="37732-107">Lai sāktu šo procedūru, pārejiet uz sadaļu Personāla vadība > Darbinieki > Darbinieki > Kompensācija > Reģistrācija mainīgam plānam.</span><span class="sxs-lookup"><span data-stu-id="37732-107">To begin this procedure, go to Human resources > Workers > Employees > Compensation > Variable plan enrolment</span></span>

1. <span data-ttu-id="37732-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="37732-108">Click New.</span></span>
2. <span data-ttu-id="37732-109">Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="37732-109">In the Plan field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="37732-110">Plāna meklēšana tiks filtrēta, lai parādītu tikai tos mainīgās atlīdzības plānus, uz kuriem darbinieks ir tiesīgs, pamatojoties uz iestatījumiem sadaļā Piemērotības noteikumi.</span><span class="sxs-lookup"><span data-stu-id="37732-110">The plan lookup will be filtered to only show the variable compensation plans that the employee is eligible for based on the eligibility rules.</span></span>  
3. <span data-ttu-id="37732-111">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="37732-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="37732-112">Pārslēdziet sadaļas Vispārīgi paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="37732-112">Toggle the expansion of the General section.</span></span>
5. <span data-ttu-id="37732-113">Laukā Spēkā stāšanās datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="37732-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="37732-114">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="37732-114">Click Save.</span></span>
7. <span data-ttu-id="37732-115">Pārslēdziet sadaļas Prioritātes paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="37732-115">Toggle the expansion of the Overrides section.</span></span>
    * <span data-ttu-id="37732-116">Ja nepieciešams, darbā pieņemšanas datuma kārtulai iespējams iestatīt ignorēt darbinieka darbā pieņemšanas datumu, kad darbā pieņemšanas kārtula, kas norādīta atlasītajam mainīgajam plānam, ir procenti.</span><span class="sxs-lookup"><span data-stu-id="37732-116">Optionally, a hire rule date can be set to override the hire date for an employee when the hire rule specified for the selected variable plan is Percent.</span></span>  
    * <span data-ttu-id="37732-117">Ja mainīgais plāns ir procentuālā daļa no pamata plāna, darbinieka piemaksas procentus var ignorēt.</span><span class="sxs-lookup"><span data-stu-id="37732-117">If the variable plan is a percent of basis plan, the award percentage can be overridden for the employee.</span></span> <span data-ttu-id="37732-118">Ja mainīgais atlīdzības plāns ir vienību skaita plāns, darbinieka vienību skaitu var ignorēt.</span><span class="sxs-lookup"><span data-stu-id="37732-118">If the variable compensation plan is a number of units plan, the number of units can be overridden for the employee.</span></span>  
    * <span data-ttu-id="37732-119">Ja darbiniekam piemaksā ir jāpiešķir vienota summa, šo summu var iestatīt šeit.</span><span class="sxs-lookup"><span data-stu-id="37732-119">If the employee should be given a flat amount for their award, the amount can be set here.</span></span>  
8. <span data-ttu-id="37732-120">Pārslēdziet sadaļas Organizatoriskās prioritātes paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="37732-120">Toggle the expansion of the Organizational overrides section.</span></span>
    * <span data-ttu-id="37732-121">Ja jāņem vērā darbinieka veiktspēja, kas novērtēta saistībā citu struktūrvienību vai nodaļu, kas neatbilst darbinieka amatam piešķirtajai, nodaļu var ignorēt.</span><span class="sxs-lookup"><span data-stu-id="37732-121">If the employee's performance should take into consideration, the performance of different departments, or a department other than the one assigned on the employee's position, the department can be overridden.</span></span> <span data-ttu-id="37732-122">Procentu kolonnas summai jābūt 100.</span><span class="sxs-lookup"><span data-stu-id="37732-122">The Percent column should total 100.</span></span>  



[!INCLUDE[footer-include](../includes/footer-banner.md)]