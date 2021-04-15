---
title: Pieejamās aprūpes akta (ACA) pārskatu ģenerēšana
description: Pieejamās aprūpes akta (ACA) pārskatu sniegšana ģenerē formas 1095-B un 1095-C, atbalstot Pieejamās aprūpes akta daļu **Darba devēja mandāts**.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 055de1f0ff3f8fd4fadba0a685fd703b9d19d918
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805998"
---
# <a name="generate-aca-reports"></a><span data-ttu-id="2e521-103">ACA pārskatu ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="2e521-103">Generate ACA reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="2e521-104">Pieejamās aprūpes akta (ACA) pārskatu sniegšana ģenerē formas 1095-B un 1095-C, atbalstot Pieejamās aprūpes akta daļu **Darba devēja mandāts**.</span><span class="sxs-lookup"><span data-stu-id="2e521-104">Affordable Care Act (ACA) reporting generates forms 1095-B and 1095-C in support of the **Employer Mandate** portion of the Affordable Care Act.</span></span>

> [!NOTE]
> <span data-ttu-id="2e521-105">ACA pārskatu sniegšana ir iespējota tikai juridiskajām personām Amerikas Savienotajās Valstīs.</span><span class="sxs-lookup"><span data-stu-id="2e521-105">ACA reporting is only enabled for legal entities in the United States.</span></span>

## <a name="getting-started"></a><span data-ttu-id="2e521-106">Darba sākšana</span><span class="sxs-lookup"><span data-stu-id="2e521-106">Getting started</span></span>

<span data-ttu-id="2e521-107">Lai sekotu līdzi informācijai formām 1095-B un 1095-C, jums vispirms ir jāizveido viena vai vairākas pieejamās aprūpes seguma grupas.</span><span class="sxs-lookup"><span data-stu-id="2e521-107">To track information for forms 1095-B and 1095-C, you must first create one or more Affordable care coverage groups.</span></span> <span data-ttu-id="2e521-108">Pieejamās aprūpes seguma grupas norāda:</span><span class="sxs-lookup"><span data-stu-id="2e521-108">Affordable Care coverage groups indicate:</span></span>

- <span data-ttu-id="2e521-109">Darbinieka seguma piedāvājumu</span><span class="sxs-lookup"><span data-stu-id="2e521-109">The offer of coverage for an employee</span></span>
- <span data-ttu-id="2e521-110">Darbinieka daļa no zemāko mēneša prēmiju izmaksām, ja izmaksas pārsniedz federālo nabadzības slieksni</span><span class="sxs-lookup"><span data-stu-id="2e521-110">The employee’s share of the lowest cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="2e521-111">Darba devēja izmantoto drošo patvērumu, ja piemērojams</span><span class="sxs-lookup"><span data-stu-id="2e521-111">Safe Harbor used by the employer, if applicable</span></span>

<span data-ttu-id="2e521-112">Pieejamās aprūpes seguma grupas ļauj pārvaldīt informāciju par šiem laukiem, un nav nepieciešamības mainīt katra darbinieka ierakstu, kur nosacījumi ir vienādi.</span><span class="sxs-lookup"><span data-stu-id="2e521-112">Affordable Care coverage groups allow you to manage the information for these fields without changing every employee record where the conditions are the same.</span></span> <span data-ttu-id="2e521-113">Varat viegli piešķirt pieejamās aprūpes seguma grupas vienam vai vairākiem darbiniekiem, izmantojot lapas funkcionalitāti **Piešķirt masveidā**.</span><span class="sxs-lookup"><span data-stu-id="2e521-113">You can easily assign Affordable Care coverage groups to one or more employees by using the **Mass assign** option on the page.</span></span>

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a><span data-ttu-id="2e521-114">Segumu grupas vairāku versiju uzturēšana</span><span class="sxs-lookup"><span data-stu-id="2e521-114">Maintaining multiple versions of a coverage group</span></span>

<span data-ttu-id="2e521-115">Varat uzturēt jebkuras segumu grupas vairākas versijas.</span><span class="sxs-lookup"><span data-stu-id="2e521-115">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="2e521-116">Šī funkcionalitāte ļauj veikt izmaiņas, neveidojiet jaunu grupu un atkārtoti nepiešķirot tai darbiniekus.</span><span class="sxs-lookup"><span data-stu-id="2e521-116">This functionality allows you to make changes without having to create a new group and reassign employees to it.</span></span> 

<span data-ttu-id="2e521-117">Kad esat izveidojis ACA seguma grupas, varat masveidā piešķirt grupas darbiniekiem ar opciju **Piešķirt masveidā**.</span><span class="sxs-lookup"><span data-stu-id="2e521-117">After you’ve created ACA coverage groups, you can mass assign the groups to employees with the **Mass assignment** option.</span></span> <span data-ttu-id="2e521-118">Varat arī atsevišķi norādīt, vai izsekot un ziņot ACA informāciju, un piešķirt darbinieku pieejamās aprūpes grupai.</span><span class="sxs-lookup"><span data-stu-id="2e521-118">You can also individually indicate whether to track and report ACA information, and assign an employee to an Affordable Care coverage group.</span></span>

<span data-ttu-id="2e521-119">Jums nav jāizseko noteikta ACA seguma informācija, piemēram, nepilna laika darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="2e521-119">You don't need to track some ACA coverage information, such as for part-time employees.</span></span> <span data-ttu-id="2e521-120">Šajā gadījumā iestatiet lauku **Pārskata segums** uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="2e521-120">In this case, set the **Report coverage** field to **No**.</span></span> <span data-ttu-id="2e521-121">Lai gan katram darbiniekam ir jāpiešķir izsekošanas ACA informācija pieejamās aprūpes seguma grupai, tomēr mēnešiem varat mainīt tālāk norādītās opcijas ar dažādām vērtībām:</span><span class="sxs-lookup"><span data-stu-id="2e521-121">Although you must assign each employee with trackable ACA information to an Affordable Care coverage group, you can still change the following options for months with different values:</span></span>

- <span data-ttu-id="2e521-122">**Vajadzību piedāvājums**</span><span class="sxs-lookup"><span data-stu-id="2e521-122">**Offer of coverage**</span></span>
- <span data-ttu-id="2e521-123">**Darbinieka izmaksu daļa**</span><span class="sxs-lookup"><span data-stu-id="2e521-123">**Employee share of cost**</span></span>
- <span data-ttu-id="2e521-124">**Drošais patvērums**</span><span class="sxs-lookup"><span data-stu-id="2e521-124">**Safe Harbor**</span></span>

<span data-ttu-id="2e521-125">Lai jebkurai no pieejamās aprūpes seguma grupas vērtībām ievadītu izņēmumus, atlasiet saiti **Pieejamās aprūpes segums** lapā **Detalizēta informācija par nodarbināto**, kas atrodas cilnes **Nodarbinātība** sadaļā **Papildinformācija**.</span><span class="sxs-lookup"><span data-stu-id="2e521-125">To enter exceptions for Affordable Care coverage group values, select the **Affordable Care Coverage** link on the **Worker detail** page under the **Additional information** section on the **Employment tab**.</span></span>

## <a name="reporting-health-care-coverage"></a><span data-ttu-id="2e521-126">Veselības aprūpes seguma ziņošana</span><span class="sxs-lookup"><span data-stu-id="2e521-126">Reporting health care coverage</span></span>

<span data-ttu-id="2e521-127">Papildus iespējai sekot līdzi tam, vai pilnas slodzes darbiniekiem tika piedāvāts jebkāds veselības apdrošināšanas segums, ja darba devējs piedāvā darba devēja sponsorētu paša apdrošināšanu veselības segumu, kuram darbinieks ir reģistrējies (neatkarīgi no tā, vai tas ir pilna laika vai nepilna laika darbinieks), tad ir jāziņo papildu informācija formā 1095-C.</span><span class="sxs-lookup"><span data-stu-id="2e521-127">In addition to tracking health insurance coverage offered to full-time employees, if the employer offers employer-sponsored self-insured health coverage for which the employee is enrolled (regardless of whether their employment status is full-time or part-time), additional information needs to be reported on the 1095-C.</span></span> <span data-ttu-id="2e521-128">Katrs darbinieks (tostarp apgādājamie), uz ko attiecas darba devēja sponsorētie atvieglojumu plāni, ir jāietver pārskatā par tiem mēnešiem, kuros viņiem bija spēkā šis segums.</span><span class="sxs-lookup"><span data-stu-id="2e521-128">Each employee (including dependents) covered by the employer-sponsored benefit plans needs to be included on the report for the months they were covered.</span></span> 

<span data-ttu-id="2e521-129">Katram atvieglojumu plānam varat norādīt, vai tas ir jāziņo, atzīmējot izvēles rūtiņu **Norādāms ACA pārskatā**.</span><span class="sxs-lookup"><span data-stu-id="2e521-129">You can indicate whether or not each benefit plan must be reported by selecting the **ACA reportable** check box.</span></span>

<span data-ttu-id="2e521-130">Turklāt, ja darbinieks ir izvēlējies atvieglojumu plānā ietvert kādus no saviem apgādājamiem, tad jūs katram darbiniekam lapā **Atvieglojumu uzturēšana** varat norādīt datumus, kad apgādājamais bija ietverts.</span><span class="sxs-lookup"><span data-stu-id="2e521-130">In addition, if employees have chosen to have any of their dependents covered under a benefit, you can indicate the dates the dependent was covered for each employee on the **Maintain benefits** page.</span></span> <span data-ttu-id="2e521-131">Lai norādītu, ka atvieglojumu plānā ir ietverts apgādājamais, kopsavilkuma cilnes **Apgādājamie** darbību rūtī izvēlieties pogu **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="2e521-131">To indicate that the dependent is covered under the benefit, select the **Edit** button in the action pane of the **Dependents** fast tab.</span></span>

<span data-ttu-id="2e521-132">Lapā **Apgādājamā seguma datumu pārvaldnieks** varat norādīt datumus, kad apgādājamais bija ietverts atvieglojumu plānā.</span><span class="sxs-lookup"><span data-stu-id="2e521-132">On the **Dependent coverage date manager** page, you can indicate the dates the dependent was covered by the benefit.</span></span> <span data-ttu-id="2e521-133">Ievadot datumus šajā lapā, lapā **Atvieglojumu uzturēšana** tiek automātiski atzīmēta izvēles rūtiņa **Segts**.</span><span class="sxs-lookup"><span data-stu-id="2e521-133">Entering dates on this page will automatically select the **Covered** checkbox on the **Maintain benefits** page.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="2e521-134">Formu 1095-B un 1095-C ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="2e521-134">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="2e521-135">Šī produkta ietvaros varat arī ģenerēt formas 1095-B un 1095-C un tās izdalīt katram no saviem darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="2e521-135">You can also generate 1095-B and 1095-C forms from within the product, and distribute them to each of your employees.</span></span> <span data-ttu-id="2e521-136">Sistēma var arī elektroniski ģenerēt 1095-C formas un 1094-C IRS pārsūtāmos failus.</span><span class="sxs-lookup"><span data-stu-id="2e521-136">The system can also electronically generate 1095-C forms and the 1094-C IRS transmittal files.</span></span>  

<span data-ttu-id="2e521-137">Ģenerējot formu 1095-C, ievadiet attiecīgo taksācijas gadu un norādiet, vai ir jāaizklāj sociālās apdrošināšanas numurs.</span><span class="sxs-lookup"><span data-stu-id="2e521-137">When generating the 1095-C form, enter the appropriate tax year and indicate if social security numbers should be masked.</span></span> <span data-ttu-id="2e521-138">Ja drukājat formas 1095-C vairāk nekā 500 darbiniekiem, jūs saņemsiet vairāk nekā vienu PDF failu.</span><span class="sxs-lookup"><span data-stu-id="2e521-138">If you're printing 1095-C forms for more than 500 employees, you'll receive more than one PDF file.</span></span> <span data-ttu-id="2e521-139">Ir ieteicams palielināt loga **Dokumentu pārvaldības parametri** iestatījuma **Maksimālais faila lielums** vērtību līdz 150 MB.</span><span class="sxs-lookup"><span data-stu-id="2e521-139">It’s recommended that you increase the **Maximum file size** in the **Document management parameters** window to 150 MB.</span></span>

## <a name="viewing-information"></a><span data-ttu-id="2e521-140">Informācijas skatīšana</span><span class="sxs-lookup"><span data-stu-id="2e521-140">Viewing information</span></span>

<span data-ttu-id="2e521-141">Lapu **Pieejamās aprūpes segums nodarbinātajam** varat izmantot, lai redzētu, kuri darbinieki ir piešķirti kurai seguma grupai, kuri darbinieki nav jāietver pārskatā, un kuri darbinieki nav piešķirti.</span><span class="sxs-lookup"><span data-stu-id="2e521-141">You can use the **Worker Affordable Care coverage** page to see which employees have been assigned to each coverage group, which employees don’t need to be included on a report, and which employees are unassigned.</span></span>

<span data-ttu-id="2e521-142">Ja kāda no pieejamās aprūpes seguma grupas noklusējuma vērtībām ir pārrakstīta, pie mainītās vērtības tiek rādīta zvaigznīte.</span><span class="sxs-lookup"><span data-stu-id="2e521-142">If any of the default values from the Affordable Care coverage group have been overridden, an asterisk will appear next to the value that was changed.</span></span> <span data-ttu-id="2e521-143">Ja vērtības visiem 12 mēnešiem ir vienādas un nav tikušas pārrakstītas, tad vērtība tiks drukāta kolonnā **Visi 12 mēneši**.</span><span class="sxs-lookup"><span data-stu-id="2e521-143">If the values for all 12 months are the same and haven’t been overridden, the value will print in the **All 12 months** column.</span></span>

<span data-ttu-id="2e521-144">Varat izmantot arī uzziņu logu, lai saprastu, kuri darbinieki ir atzīmēti kā tādi, kas nav jānorāda ACA pārskatā.</span><span class="sxs-lookup"><span data-stu-id="2e521-144">You can also use the inquiry window to understand which employees have been flagged as not ACA reportable.</span></span> <span data-ttu-id="2e521-145">Nav nepieciešams izsekot, vai tiem tika piedāvāts segums, un gada beigās tiem nebūs jāizsniedz 1095-C.</span><span class="sxs-lookup"><span data-stu-id="2e521-145">You don’t need to track whether coverage was offered to them and won't need to issue a 1095-C to them at the end of the year.</span></span> <span data-ttu-id="2e521-146">Lai ģenerētu sarakstu ar visiem darbiniekiem, kuri nesaņems 1095-C, laukā **Filtrēt pēc** atlasiet **Nav norādāms ACA pārskatā**.</span><span class="sxs-lookup"><span data-stu-id="2e521-146">Select **Not ACA reportable** in the **Filter by** field to generate a list of all employees who won't receive a 1095-C.</span></span>

<span data-ttu-id="2e521-147">Papildus tam varat apskatīt jebkuru darbinieku, kuri nav piešķirti (lauks **ACA pārskata segums** ir tukšs) vai kuri ir piešķirti kādai pieejamās aprūpes seguma grupai, kuras darbība ir beigusies tajā gadā, kas ir atlasīts laukā **Gads**.</span><span class="sxs-lookup"><span data-stu-id="2e521-147">In addition, you can view any employees who are unassigned (the **ACA Report coverage** field is empty) or who have been assigned to an Affordable Care coverage group that is expired for the year selected in the **Year** field.</span></span>

<span data-ttu-id="2e521-148">Sarakstus ar darbiniekiem, kas tika ģenerēti, izmantojot filtrēšanas opcijas, varat eksportēt uz programmu Excel.</span><span class="sxs-lookup"><span data-stu-id="2e521-148">You can export lists of employees that were generated using any of the filtering options to Excel.</span></span>

<span data-ttu-id="2e521-149">Ja jums ir jāsniedz pārskats par iekļautajām personām, jo jūs nodrošināt paša apdrošinātu segumu, varat apskatīt visus apgādājamos, kas ietverti atvieglojumu plānos, kuri atzīmēti kā **Norādāmi ACA pārskā**.</span><span class="sxs-lookup"><span data-stu-id="2e521-149">If you need to report covered individuals because you provide self-insured coverage, you can view any dependents covered under benefit plans marked as **ACA reportable**.</span></span> <span data-ttu-id="2e521-150">Darbību rūtī atlasiet **Skatīt apgādājamā segumu**.</span><span class="sxs-lookup"><span data-stu-id="2e521-150">Select **View Dependent coverage** on the action pane.</span></span>

> [!NOTE]
> <span data-ttu-id="2e521-151">Pieprasījuma logā tiek rādīti tikai atvieglojumu plāni, kas atzīmēti kā **Norādāms ACA pārskatā**.</span><span class="sxs-lookup"><span data-stu-id="2e521-151">Only benefit plans marked as **ACA reportable** display in the inquiry window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]