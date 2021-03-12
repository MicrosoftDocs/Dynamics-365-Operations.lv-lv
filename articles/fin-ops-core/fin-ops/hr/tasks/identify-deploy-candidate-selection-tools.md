---
title: Kandidātu izvēles rīku noteikšana un ieviešana
description: Var būt grūti atrast kvalificētu kandidātu kopu, lai aizpildītu vakances, it īpaši, ja amatam ir nepieciešama unikālu prasmju kopa.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmSkillMapping, HcmJobLookup, HcmSkillMappingLine, HcmPersonCertificate, CCHTMLPrintPreview
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8015d4e32da2ba80230aa0ad48576948f2fd1678
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797754"
---
# <a name="identify-and-deploy-candidate-selection-tools"></a><span data-ttu-id="ef851-103">Kandidātu izvēles rīku noteikšana un ieviešana</span><span class="sxs-lookup"><span data-stu-id="ef851-103">Identify and deploy candidate selection tools</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ef851-104">Var būt grūti atrast kvalificētu kandidātu kopu, lai aizpildītu vakances, it īpaši, ja amatam ir nepieciešama unikālu prasmju kopa.</span><span class="sxs-lookup"><span data-stu-id="ef851-104">Finding a qualified pool of candidates to fill vacancies can be difficult, especially when a position requires a unique set of skills.</span></span>  <span data-ttu-id="ef851-105">Taču iespējams, ka kandidāti ar jums nepieciešamajam prasmēm jau strādā jūsu organizācijā.</span><span class="sxs-lookup"><span data-stu-id="ef851-105">However, candidates with the skills you need might already be employed in your organization.</span></span> <span data-ttu-id="ef851-106">Noteiktu prasmju kopu varat meklēt starp esošajiem darbiniekiem vai jauniem kandidātiem.</span><span class="sxs-lookup"><span data-stu-id="ef851-106">You can search for a specific skill set among existing employees, or new applicants.</span></span> <span data-ttu-id="ef851-107">Šādi personāla atlases darbinieks var ātri apkopot un izskatīt datus par kandidātiem, kas vakantam amatam ir pieteikušies tagad vai iepriekš, vai atrastu potenciālos kandidātus starp jau esošajiem darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="ef851-107">This allows a recruiter to quickly gather and screen applicants who have applied for open position now or in the past, or to find potential candidates from their existing pool of employees.</span></span> <span data-ttu-id="ef851-108">Izmantojiet šo uzdevuma ierakstu, lai uzzinātu, kā prasmju kartēšanas funkcionalitāte jums var palīdzēt atrast vakantajam amatam vispiemērotāko personu.</span><span class="sxs-lookup"><span data-stu-id="ef851-108">Use this task recording to learn how the skill mapping functionality can help you find the right person for an open position.</span></span> <span data-ttu-id="ef851-109">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="ef851-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="ef851-110">Pārejiet uz sadaļu Personāla vadība > Zināšanas > Prasmju analīze > Prasmju kartēšanas profili.</span><span class="sxs-lookup"><span data-stu-id="ef851-110">Go to Human resources > Competencies > Skill analysis > Skill mapping profiles.</span></span>
2. <span data-ttu-id="ef851-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="ef851-111">Click New.</span></span>
3. <span data-ttu-id="ef851-112">Laukā Prasmju kartēšana ievadiet savas prasmju kartēšanas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="ef851-112">In the Skill mapping field, enter a name for your skill mapping.</span></span>  <span data-ttu-id="ef851-113">Piemērs: Grāmatvedis.</span><span class="sxs-lookup"><span data-stu-id="ef851-113">Example: Accountant.</span></span>
4. <span data-ttu-id="ef851-114">Laukā Apraksts ievadiet prasmju kartējuma aprakstu.</span><span class="sxs-lookup"><span data-stu-id="ef851-114">In the Description field, enter a description of the skill mapping..</span></span>
5. <span data-ttu-id="ef851-115">Laukā Datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="ef851-115">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="ef851-116">Noklikšķiniet uz Iegūt profilu.</span><span class="sxs-lookup"><span data-stu-id="ef851-116">Click Retrieve profile.</span></span>
    * <span data-ttu-id="ef851-117">Lietojiet vienumu Iegūt profilu, lai no atlasītās personas, darba vai kursa kā meklēšanas pamata iegūtu sertifikāta, prasmju un izglītības datus.</span><span class="sxs-lookup"><span data-stu-id="ef851-117">Use Retrieve profile to pull in the Certificate, Skill, and Education data from a selected Person, Job or Course as the basis for your search.</span></span>   <span data-ttu-id="ef851-118">Pēc tam varat pievienot vai noņemt kritērijus, norādīt, vai kritēriji ir obligāti, kā arī kārtot kritērijus pēc to svarīguma.</span><span class="sxs-lookup"><span data-stu-id="ef851-118">You can then add or remove criteria, state if the criteria is optional and rank the importance of the criteria.</span></span>  
7. <span data-ttu-id="ef851-119">Noklikšķiniet uz Darbs.</span><span class="sxs-lookup"><span data-stu-id="ef851-119">Click Job.</span></span>
8. <span data-ttu-id="ef851-120">Laukā Darbs ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ef851-120">In the Job field, enter or select a value.</span></span>
9. <span data-ttu-id="ef851-121">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="ef851-121">Click OK.</span></span>
10. <span data-ttu-id="ef851-122">Izvērsiet diapazona kopsavilkuma cilni un pievienojiet visu nepieciešamo papildinformāciju, piemēram, nodaļu.</span><span class="sxs-lookup"><span data-stu-id="ef851-122">Expand the Range FastTab, and add any additional information, such as department.</span></span>
11. <span data-ttu-id="ef851-123">Izvērst sertifikātu kopsavilkuma cilni, lai apskatītu vai rediģētu sertifikātus.</span><span class="sxs-lookup"><span data-stu-id="ef851-123">Expand the Certificates FastTab to view or edit the certificates.</span></span>
12. <span data-ttu-id="ef851-124">Izvērst kopsavilkuma cilni Prasmes, lai apskatītu vai rediģētu prasmes.</span><span class="sxs-lookup"><span data-stu-id="ef851-124">Expand the Skills FastTab to view or edit the skills.</span></span>
13. <span data-ttu-id="ef851-125">Izvērst kopsavilkuma cilni Izglītība, lai apskatītu vai rediģētu izglītības kritērijus.</span><span class="sxs-lookup"><span data-stu-id="ef851-125">Expand the Education FastTab to view or edit the education criteria.</span></span>
14. <span data-ttu-id="ef851-126">Noklikšķiniet uz Izpildīt.</span><span class="sxs-lookup"><span data-stu-id="ef851-126">Click Execute.</span></span>
15. <span data-ttu-id="ef851-127">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="ef851-127">Click OK.</span></span>
16. <span data-ttu-id="ef851-128">Klikšķiniet Rezultāts.</span><span class="sxs-lookup"><span data-stu-id="ef851-128">Click Result.</span></span>
17. <span data-ttu-id="ef851-129">Klikšķiniet Rezultāts.</span><span class="sxs-lookup"><span data-stu-id="ef851-129">Click Result.</span></span>
18. <span data-ttu-id="ef851-130">Klikšķiniet Atsākt.</span><span class="sxs-lookup"><span data-stu-id="ef851-130">Click Resume.</span></span>
19. <span data-ttu-id="ef851-131">Noklikšķiniet uz Sertifikāti.</span><span class="sxs-lookup"><span data-stu-id="ef851-131">Click Certificates.</span></span>
    * <span data-ttu-id="ef851-132">Varat rakties detalizētākos datos par katru uzskaitīto personu un skatīt sīkāku informāciju par šo personu izglītību, prasmēm, profesionālo pieredzi un citiem datiem.</span><span class="sxs-lookup"><span data-stu-id="ef851-132">You can drill further into each person listed and see details regarding their education, skills, and professional experience.</span></span>  
20. <span data-ttu-id="ef851-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ef851-133">Close the page.</span></span>
21. <span data-ttu-id="ef851-134">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ef851-134">Close the page.</span></span>
22. <span data-ttu-id="ef851-135">Vēlreiz atlasiet rezultātu.</span><span class="sxs-lookup"><span data-stu-id="ef851-135">Select result again.</span></span>
23. <span data-ttu-id="ef851-136">Noklikšķiniet uz Atskaite.</span><span class="sxs-lookup"><span data-stu-id="ef851-136">Click Report.</span></span>
    * <span data-ttu-id="ef851-137">Atskaitē vislabākās atbilstības ir uzskaitītas atskaites augšpusē.</span><span class="sxs-lookup"><span data-stu-id="ef851-137">The report will list the best matches at the top of the report.</span></span>  <span data-ttu-id="ef851-138">Varat redzēt, ka ir uzskaitīts starpības elements.</span><span class="sxs-lookup"><span data-stu-id="ef851-138">You can see that a gap element is listed.</span></span>  <span data-ttu-id="ef851-139">Šis vienums apzīmē atšķirību starp prasmju kartējumā uzskaitīto līmeni un attiecīgajai personai piešķirto prasmju līmeni.</span><span class="sxs-lookup"><span data-stu-id="ef851-139">This is the difference between the level that was listed on the skill mapping, and the level of the skill that is assigned to the person.</span></span>  
24. <span data-ttu-id="ef851-140">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ef851-140">Close the page.</span></span>
25. <span data-ttu-id="ef851-141">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ef851-141">Click Save.</span></span>

