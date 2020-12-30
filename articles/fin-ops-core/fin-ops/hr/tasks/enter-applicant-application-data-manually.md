---
title: Kandidāta un pieteikuma datu manuāla ievade
description: Šajā procedūrā parādīts, kā manuāli uzturēt informāciju par kandidātiem un viņu pieteikumiem.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmApplicant, LogisticsContactInfoGrid, HRMApplication,  DirPartyTable
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ea39e86ace40cd8e3ad2733b7f7f7a873a963e7
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693044"
---
# <a name="enter-applicant-and-application-data-manually"></a><span data-ttu-id="e7d0a-103">Kandidāta un pieteikuma datu manuāla ievade</span><span class="sxs-lookup"><span data-stu-id="e7d0a-103">Enter applicant and application data manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e7d0a-104">Šajā procedūrā parādīts, kā manuāli uzturēt informāciju par kandidātiem un viņu pieteikumiem.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-104">This procedure shows how to manually maintain information about applicants and their application.</span></span>   <span data-ttu-id="e7d0a-105">Varat ievadīt un uzturēt kandidātu personisko informāciju, interviju datumus un laikus, atsauksmes, zināšanas un naktsmītnes pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-105">You can enter and maintain personal information, interview dates and times, references, competencies, and accommodation requests for applicants.</span></span> <span data-ttu-id="e7d0a-106">Varat arī atjaunināt kandidātu darba pieteikumu statusu un izveidot vēstules vai e-pasta ziņojumus, lai sazinātos ar kandidātiem.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-106">You can also update the status of applicants' applications for employment and create letters or email messages to communicate with applicants.</span></span> <span data-ttu-id="e7d0a-107">Kad izveidojat kandidāta ierakstu, globālajā adrešu grāmatā tiek izveidots šī kandidāta personas ieraksts.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-107">When you create an applicant record, a person record for that applicant is created in the global address book.</span></span>       <span data-ttu-id="e7d0a-108">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-new-applicant-record"></a><span data-ttu-id="e7d0a-109">Jaunu pieteikuma ieraksta izveide</span><span class="sxs-lookup"><span data-stu-id="e7d0a-109">Create a new applicant record</span></span>
1. <span data-ttu-id="e7d0a-110">Pārejiet uz sadaļu Personāla vadība > Personāla atlase > Kandidāti > Kandidāti.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-110">Go to Human resources > Recruitment > Applicants > Applicants.</span></span>
2. <span data-ttu-id="e7d0a-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-111">Click New.</span></span>
3. <span data-ttu-id="e7d0a-112">Laukā Vārds ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-112">In the First name field, type a value.</span></span>
4. <span data-ttu-id="e7d0a-113">Laukā Uzvārds ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-113">In the Last name field, type a value.</span></span>
    * <span data-ttu-id="e7d0a-114">Varat ievadīt papildu informāciju par kandidātu, ja tā ir pieejama.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-114">You can enter additional applicant information if it's available.</span></span> <span data-ttu-id="e7d0a-115">Informāciju var iekļaut, piemēram, kandidāta specializācijas pakāpi, pašreizējo darba amatu vai iepriekšējo darba devēju.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-115">For example, information can include the applicant's highest degree, current job title, or previous employer.</span></span>  
5. <span data-ttu-id="e7d0a-116">Pārslēdziet sadaļas Kontaktinformācija paplašināšanu.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-116">Toggle the expansion of the Contact information section.</span></span>
6. <span data-ttu-id="e7d0a-117">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-117">Click Add.</span></span>
7. <span data-ttu-id="e7d0a-118">Laukā Apraksts ierakstiet Saziņas e-pasta adrese.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-118">In the Description field, type 'Communications email'.</span></span>
8. <span data-ttu-id="e7d0a-119">Atlasiet opciju laukā Tips.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-119">In the Type field, select an option.</span></span>
9. <span data-ttu-id="e7d0a-120">Ierakstiet vērtību laukā Kontaktpersonas tālrunis/adrese.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-120">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="e7d0a-121">Šī e-pasta adrese tiks lietota, lai ģenerētu e-pasta ziņojumus saziņai ar kandidātu.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-121">This email address will be used to generate email communication with the applicant.</span></span>  
10. <span data-ttu-id="e7d0a-122">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-122">Click Add.</span></span>
11. <span data-ttu-id="e7d0a-123">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-123">In the Description field, type a value.</span></span>
12. <span data-ttu-id="e7d0a-124">Ierakstiet vērtību laukā Kontaktpersonas tālrunis/adrese.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-124">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="e7d0a-125">Kandidāta personiskā informācija.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-125">Applicant personal information.</span></span>  
    * <span data-ttu-id="e7d0a-126">Ja nepieciešams, varat ievadīt papildu personisko informāciju par kandidātu.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-126">You can enter additional personal information for the applicant, if needed.</span></span> <span data-ttu-id="e7d0a-127">Tas var iekļaut, piemēram, dzimšanas datumu, etnisko izcelsmi, dzimumu vai ģimenes stāvokli.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-127">For example, this can include birth date, ethnic origin, gender, or marital status.</span></span>  
13. <span data-ttu-id="e7d0a-128">Darbību rūtī noklikšķiniet uz Zināšanas.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-128">On the Action Pane, click Competencies.</span></span>
    * <span data-ttu-id="e7d0a-129">Varat ievadīt kandidāta kompetences profilu, norādot prasmes, profesionālo pieredzi, izglītību, testus vai sertifikātus.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-129">You can enter the applicant's competency profile, including their skills, professional experiences, education, tests, or certificates.</span></span>  
    * <span data-ttu-id="e7d0a-130">Šo informāciju varat izmantot, lai kartētu kandidāta prasmes attiecībā uz prasmēm, kas saistītas ar jūsu uzņēmuma datos definētajiem darbiem.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-130">This information can be used to map the applicant's skills to the skills associated with the jobs defined in your company's data.</span></span>   

## <a name="create-an-application-for-the-applicant"></a><span data-ttu-id="e7d0a-131">Kandidāta pieteikuma izveide</span><span class="sxs-lookup"><span data-stu-id="e7d0a-131">Create an application for the applicant</span></span>
1. <span data-ttu-id="e7d0a-132">Noklikšķiniet uz Pieteikumi.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-132">Click Applications.</span></span>
2. <span data-ttu-id="e7d0a-133">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-133">Click New.</span></span>
3. <span data-ttu-id="e7d0a-134">Laukā Personāla atlases projekts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-134">In the Recruitment project field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e7d0a-135">Atlasot personāla atlases projektu, kandidāts tiks sasaistīts ar noteiktu atvērtu amatu, kas iekļauts personāla atlases projektā.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-135">By selecting a recruitment project, the applicant will be associated with a specific opening included in that recruitment project.</span></span>  
4. <span data-ttu-id="e7d0a-136">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-136">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="e7d0a-137">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e7d0a-138">Pēc noklusējuma darbs un nodaļa tiek iegūti no atlasītā personāla atlases projekta.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-138">By default, the job and department are based on the selected recruitment project.</span></span>  
6. <span data-ttu-id="e7d0a-139">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-139">Click Save.</span></span>
    * <span data-ttu-id="e7d0a-140">Pēc pieteikuma saglabāšanas varat tam pievienot dokumentus, tai skaitā kandidāta pieredzi un apbalvojumus apliecinošus dokumentus un pavadvēstuli.</span><span class="sxs-lookup"><span data-stu-id="e7d0a-140">After saving the application, you can attach documents to it, including the applicant's experience, awards, and cover letter.</span></span>  

