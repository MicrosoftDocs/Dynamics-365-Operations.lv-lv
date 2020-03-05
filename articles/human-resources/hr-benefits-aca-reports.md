---
title: Pieejamās aprūpes akta (ACA) pārskatu ģenerēšana
description: Ir pieejama funkcionalitāte, kura palīdz darba devējiem, kam ir nepieciešams sekot līdzi formās 1095-B un 1095-C ziņotajai informācijai, ievērojot pieejamās aprūpes akta (Affordable Care Act — ACA) prasības daļā Darba devēja mandāts. Ņemiet vērā, ka šī funkcionalitāte ir iespējota tikai juridiskajām personām Amerikas Savienotajās Valstīs.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 47532861203fedbffc49aa92d25fc99de9d25376
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009825"
---
# <a name="generate-affordable-care-act-aca-reports"></a><span data-ttu-id="36031-103">Pieejamās aprūpes akta (ACA) pārskatu ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="36031-103">Generate Affordable Care Act (ACA) reports</span></span>

<span data-ttu-id="36031-104">Ir pieejama funkcionalitāte, kura palīdz darba devējiem, kam ir nepieciešams sekot līdzi formās 1095-B un 1095-C ziņotajai informācijai, ievērojot pieejamās aprūpes akta (Affordable Care Act — ACA) prasības daļā **Darba devēja mandāts**. Ņemiet vērā, ka šī funkcionalitāte ir iespējota tikai juridiskajām personām Amerikas Savienotajās Valstīs.</span><span class="sxs-lookup"><span data-stu-id="36031-104">Functionality is available to assist employers that need to track the information reported on forms 1095-B and 1095-C in support of the **Employer Mandate** portion of the Affordable Care Act. Note this functionality is only enabled for legal entities in the United States.</span></span>

## <a name="getting-started"></a><span data-ttu-id="36031-105">Darba sākšana</span><span class="sxs-lookup"><span data-stu-id="36031-105">Getting started</span></span>
<span data-ttu-id="36031-106">Uzsākot sekot līdzi informācijai, ko ziņot formās 1095-B un 1095-C, jums vispirms ir jāizveido viena vai vairākas pieejamās aprūpes seguma grupas.</span><span class="sxs-lookup"><span data-stu-id="36031-106">When beginning to track information to report on forms 1095-B and 1095-C, you must first create one or more Affordable Care coverage groups.</span></span> <span data-ttu-id="36031-107">Šīs pieejamās aprūpes seguma grupas tiks izmantotas, lai norādītu darbiniekam nodrošināto seguma piedāvājumu, darbinieka zemāko ikmēneša iemaksu daļu (ja izmaksas pārsniedz federālās nabadzības slieksni), kā arī darba devēja izmantoto drošo patvērumu, ja piemērojams.</span><span class="sxs-lookup"><span data-stu-id="36031-107">These Affordable Care coverage groups will be used to indicate the offer of coverage that was provided to an employee, the employee’s share of the lowest cost monthly premium (if the cost is above the federal poverty line) as well as Safe Harbor used by the employer, if applicable.</span></span> <span data-ttu-id="36031-108">Izmantojot pieejamās aprūpes akta grupas, jūs varat pārvaldīt informāciju par šiem laukiem, un nav nepieciešamības aiztikt katra darbinieka ierakstu, kur nosacījumi ir vienādi.</span><span class="sxs-lookup"><span data-stu-id="36031-108">Using Affordable Care Act groups enables you to manage the information for these fields without needing to touch every employee record where the conditions are the same.</span></span> <span data-ttu-id="36031-109">Turklāt pieejamās aprūpes seguma grupas var ērti piešķirt vienam vai vairākiem darbiniekiem, izmantojot lapas funkcionalitāti Piešķirt masveidā.</span><span class="sxs-lookup"><span data-stu-id="36031-109">In addition, Affordable Care coverage groups can easily be assigned to one or more employees using the Mass assign functionality on the page.</span></span>

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a><span data-ttu-id="36031-110">Segumu grupas vairāku versiju uzturēšana</span><span class="sxs-lookup"><span data-stu-id="36031-110">Maintaining multiple versions of a coverage group</span></span>
<span data-ttu-id="36031-111">Jebkurai seguma grupai varat uzturēt vairākas versijas, tādējādi varat veikt izmaiņas, kas uztur aktuālu grupas informāciju, bez nepieciešamības izveidot jaunu grupu un atkārtoti piešķirt tai darbiniekus, ja kaut kas mainās jūsu organizācijā vai piedāvātajās priekšrocībās.</span><span class="sxs-lookup"><span data-stu-id="36031-111">You can maintain multiple versions of any coverage group, which allows you to make changes that keep the group’s information current, without having to create a new group and reassign employees to it when something changes in your organization or in the benefits that are offered.</span></span> 

<span data-ttu-id="36031-112">Kad esat izveidojis nepieciešamās pieejamās aprūpes seguma grupas, varat izlemt šim grupām masveidā piešķirt darbiniekus, izmantojot lapas funkcionalitāti **Masveida piešķiršana**, vai varat doties uz katra darbinieka ierakstu un norādīt, vai ir jāseko līdzi ACA informācijai un vai tā ir jāziņo par attiecīgo darbinieku, kā arī piešķirt šo darbinieku kādai pieejamās aprūpes seguma grupai.</span><span class="sxs-lookup"><span data-stu-id="36031-112">After you’ve created the Affordable Care coverage groups that you need, you can choose to mass assign the groups to employees using the **Mass assignment** functionality on the page, or you can go to each employee and indicate whether ACA information needs to tracked and reported for that employee as well as assigning the employee to an Affordable Care coverage group.</span></span>

<span data-ttu-id="36031-113">Ja kādam darbiniekam informācija par pieejamās aprūpes segumu nav jāizseko vai jāziņo, piemēram, ja tas ir nepilnas slodzes darbinieks, tad lauka **Pārskata segums** vērtība ir jāiestata uz Nē.</span><span class="sxs-lookup"><span data-stu-id="36031-113">If affordable care coverage information doesn’t need to be tracked or reported for an employee, for example if they are a part-time employee, the **Report coverage** field could be set to No.</span></span> <span data-ttu-id="36031-114">Lai gan katrs darbinieks, kura ACA informācija ir jāizseko, ir jāpiešķir kādai pieejamās aprūpes seguma grupai, opcijas **Seguma piedāvājums**, **Darbinieka izmaksu daļa** un **Drošais patvērums** joprojām varat mainīt jebkuram mēnesim — vai mēnešiem —, kuriem varētu būt nepieciešamas atšķirīgas vērtības nekā pieejamās aprūpes seguma grupā ierakstītās.</span><span class="sxs-lookup"><span data-stu-id="36031-114">Although each employee for which ACA information needs to be tracked needs to be assigned to an Affordable Care coverage group, you can still change the **Offer of coverage**, **Employee share of cost** and **Safe Harbor** options for any month – or months – that may need different values than those entered in the Affordable Care coverage group.</span></span>

<span data-ttu-id="36031-115">Lai jebkurai no pieejamās aprūpes seguma grupas vērtībām ievadītu izņēmumus, noklikšķiniet uz pieejamās aprūpes seguma saites lapā Detalizēta informācija par nodarbināto, kas atrodas cilnes Nodarbinātība sadaļā Papildinformācija.</span><span class="sxs-lookup"><span data-stu-id="36031-115">To enter exceptions to any of the Affordable Care coverage group values, click on the Affordable Care Coverage link found on the Worker detail page, which is under the Additional information section on the Employment tab.</span></span>

## <a name="reporting-health-care-coverage"></a><span data-ttu-id="36031-116">Veselības aprūpes seguma ziņošana</span><span class="sxs-lookup"><span data-stu-id="36031-116">Reporting health care coverage</span></span>
<span data-ttu-id="36031-117">Papildus iespējai sekot līdzi tam, vai pilnas slodzes darbiniekam tika piedāvāts jebkāds veselības apdrošināšanas segums, ja darba devējs piedāvā darba devēja sponsorētu paša apdrošināšanu veselības segumu, kuram darbinieks ir reģistrējies (neatkarīgi no tā, vai tas ir pilna laika vai nepilna laika darbinieks), tad ir jāziņo papildu informācija formā 1095-C.</span><span class="sxs-lookup"><span data-stu-id="36031-117">In addition to tracking what if any health insurance coverage was offered to a full-time employee, if the employer offers employer-sponsored self-insured health coverage for which the employee is enrolled (regardless of whether their employment status is full-time or part-time), additional information needs to be reported on the 1095-C.</span></span> <span data-ttu-id="36031-118">Katrs darbinieks (tostarp apgādājamie), uz ko attiecas darba devēja sponsorētie atvieglojumu plāni, ir jāietver pārskatā par tiem mēnešiem, kuros viņiem bija spēkā šis segums.</span><span class="sxs-lookup"><span data-stu-id="36031-118">Each employee (including dependents) covered by the employer-sponsored benefit plans needs to be included on the report for the months they were covered.</span></span> 

<span data-ttu-id="36031-119">Katram atvieglojumu plānam varat norādīt, vai tas ir jāziņo, atzīmējot izvēles rūtiņu **Norādāms ACA pārskatā**.</span><span class="sxs-lookup"><span data-stu-id="36031-119">You can indicate whether or not each Benefit plan must be reported by selecting the **ACA reportable** check box.</span></span>

<span data-ttu-id="36031-120">Turklāt, ja darbinieks ir izvēlējies atvieglojumu plānā ietvert kādus no saviem apgādājamiem, tad jūs katram darbiniekam lapā Atvieglojumu uzturēšana varat norādīt datumus, kad apgādājamais bija ietverts.</span><span class="sxs-lookup"><span data-stu-id="36031-120">In addition, if employees have chosen to have any of their dependents covered under a benefit you can indicate the dates the dependent was covered for each employee on the Maintain benefits page.</span></span> <span data-ttu-id="36031-121">Lai norādītu, ka atvieglojumu plānā ir ietverts apgādājamais, kopsavilkuma cilnes Apgādājamie darbību rūtī izvēlieties pogu Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="36031-121">To indicate that the dependent is covered under the benefit, choose the Edit button in the action pane of the Dependents FastTab.</span></span>

<span data-ttu-id="36031-122">Lapā **Apgādājamā seguma datumu pārvaldnieks** varat norādīt datumus, kad apgādājamais bija ietverts atvieglojumu plānā.</span><span class="sxs-lookup"><span data-stu-id="36031-122">On the **Dependent coverage date manager** page, you can indicate the dates the dependent was covered by the benefit.</span></span> <span data-ttu-id="36031-123">Ievadot datumus šajā lapā, lapā **Atvieglojumu uzturēšana** tiek automātiski atzīmēta izvēles rūtiņa **Segts**.</span><span class="sxs-lookup"><span data-stu-id="36031-123">Entering dates on this page will automatically select the **Covered** checkbox on the **Maintain benefits** page.</span></span>

## <a name="generate-1095b-and-1095c-forms"></a><span data-ttu-id="36031-124">Ģenerēt formas 1095B un 1095C</span><span class="sxs-lookup"><span data-stu-id="36031-124">Generate 1095B and 1095C forms</span></span>
<span data-ttu-id="36031-125">Šī produkta ietvaros varat arī ģenerēt formas 109-B un 1095-C un tās izdalīt katram no saviem darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="36031-125">You can also generate 109-B and 1095-C forms from with in the product, and distribute them to each of your employees.</span></span> <span data-ttu-id="36031-126">No sistēmas var arī elektroniski ģenerēt 1095-C un atbilstošos 1094-C pārsūtīšanas failus, kurus var izmantot, lai sūtītu uz IRS.</span><span class="sxs-lookup"><span data-stu-id="36031-126">Electronically generating 1095-C and the corresponding 1094-C transmittal files which can be used to send to the IRS, can also be generated from the system.</span></span>  

<span data-ttu-id="36031-127">Ģenerējot formu 1095-C, ievadiet attiecīgo taksācijas gadu un norādiet, vai ir jāaizklāj sociālās apdrošināšanas numurs.</span><span class="sxs-lookup"><span data-stu-id="36031-127">When generating the 1095-C form, enter in the appropriate tax year and indicate if social security numbers should be masked.</span></span> <span data-ttu-id="36031-128">Ja drukājat formas 1095-C vairāk nekā 500 darbiniekiem, jūs saņemsiet vairāk nekā vienu PDF failu.</span><span class="sxs-lookup"><span data-stu-id="36031-128">If you are printing 1095-C forms for more than 500 employees, you will receive more than one PDF file.</span></span> <span data-ttu-id="36031-129">Ir ieteicams palielināt loga **Dokumentu pārvaldības parametri** iestatījuma **Maksimālais faila lielums** vērtību līdz 150 MB.</span><span class="sxs-lookup"><span data-stu-id="36031-129">It’s recommended that you increase the **Maximum file size** in the **Document management parameters** window to 150 MB.</span></span>

## <a name="viewing-information"></a><span data-ttu-id="36031-130">Informācijas skatīšana</span><span class="sxs-lookup"><span data-stu-id="36031-130">Viewing information</span></span>
<span data-ttu-id="36031-131">Lapu **Pieejamās aprūpes segums nodarbinātajam** varat izmantot, lai redzētu, kuri darbinieki ir piešķirti kurai seguma grupai, kuri darbinieki nav jāietver pārskatā, un kuri darbinieki nav piešķirti.</span><span class="sxs-lookup"><span data-stu-id="36031-131">You can use the **Worker Affordable Care coverage** page to see which employees have been assigned to each coverage group, which employees don’t need to be included on a report, and which employees are unassigned.</span></span>

<span data-ttu-id="36031-132">Ja kāda no pieejamās aprūpes seguma grupas noklusējuma vērtībām ir pārrakstīta, pie mainītās vērtības tiek rādīta zvaigznīte.</span><span class="sxs-lookup"><span data-stu-id="36031-132">If any of the default values from the Affordable Care coverage group have been overridden an asterisk will appear next to the value that was changed.</span></span> <span data-ttu-id="36031-133">Ja vērtības visiem 12 mēnešiem ir vienādas un nav tikušas pārrakstītas, tad vērtība tiks drukāta kolonnā **Visi 12 mēneši**.</span><span class="sxs-lookup"><span data-stu-id="36031-133">If the values for all 12 months are the same and haven’t been overridden, the value will print in the **All 12 months** column.</span></span>

<span data-ttu-id="36031-134">Varat arī izmantot uzziņu logu, lai saprastu, kuri darbinieki ir atzīmēti kā ACA pārskatos nenorādāmi — tas nozīmē, ka jums nav nepieciešams sekot līdzi tam, vai šiem darbiniekiem ir piedāvāts segums, un viņiem nav nepieciešams izsniegt 1095-C formas gada beigās.</span><span class="sxs-lookup"><span data-stu-id="36031-134">You can also use the inquiry window to understand which employees have been flagged as not ACA reportable, meaning you don’t need to track whether coverage was offered to them and will not need to issue a 1095-C to them at the end of the year.</span></span> <span data-ttu-id="36031-135">Laukā **Filtrēt pēc** atlasot vērtību **Nav norādāms ACA pārskatā**, varat ģenerēt sarakstu ar visiem darbiniekiem, kas ir atzīmēti kā tādi, kuriem nav jāsaņem 1095-C forma.</span><span class="sxs-lookup"><span data-stu-id="36031-135">By selecting **Not ACA reportable** in the **Filter by** field, you can generate a list of all employees that have been flagged to not receive a 1095-C.</span></span>

<span data-ttu-id="36031-136">Papildus tam, ka varat apskatīt sarakstu ar darbiniekiem, kas nav norādāmi ACA pārskatā, varat arī skatīt darbiniekus, kuri nav piešķirti (lauks **ACA pārskata segums** ir tukšs) vai kuri ir piešķirti kādai pieejamās aprūpes seguma grupai, kuras darbība ir beigusies tajā gadā, kas ir atlasīts laukā **Gads**.</span><span class="sxs-lookup"><span data-stu-id="36031-136">In addition to viewing a list of employees that are not ACA reportable, you can also view any employees who are unassigned (the **ACA Report coverage** field is empty) or that have been assigned to an Affordable Care coverage group that is expired for the year selected in the **Year** field.</span></span>

<span data-ttu-id="36031-137">Sarakstus ar darbiniekiem, kas tika ģenerēti, izmantojot filtrēšanas opcijas, varat eksportēt uz programmu Excel.</span><span class="sxs-lookup"><span data-stu-id="36031-137">You can export lists of employees that were generated using any of the filtering options to Excel.</span></span>

<span data-ttu-id="36031-138">Ja nepieciešams ziņot par ietvertajām personām, jo kā darba devējs jūsu nodrošināt paša apdrošinātu segumu, tad varat skatīt arī jebkurus apgādājamos, kuri ir iekļauti atvieglojumu plānos, kas ir atzīmēti kā **Norādāms ACA pārskatā**, darbību rūts joslā atlasot darbību Skatīt apgādājamo segumu.</span><span class="sxs-lookup"><span data-stu-id="36031-138">If you need to report covered individuals because as an employer you provide self-insured coverage you can also view any dependents covered under benefit plans that have been marked as **ACA reportable** by selecting the View Dependent coverage action on the action pane strip.</span></span>

<span data-ttu-id="36031-139">**Piezīme.** Uzziņu lokā tiek rādīti tikai atvieglojumi, kuru plāns ir atzīmēts kā **Norādāms ACA pārskatā**.</span><span class="sxs-lookup"><span data-stu-id="36031-139">**Note:** Only benefits whose plan has been marked as **ACA reportable** will display in the inquiry window.</span></span>