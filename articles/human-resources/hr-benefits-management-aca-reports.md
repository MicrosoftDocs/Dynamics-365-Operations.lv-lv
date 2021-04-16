---
title: Ģenerēt Pieejamas aprūpes akta pārskatus Atvieglojumu pārvaldībā
description: Šajā tēmā ir aprakstīts, kā Atvieglojumu pārvaldība palīdz izsekot informāciju, kas ir norādīta Pieejamas aprūpes akta (ACA) darba devēja mandāta formā 1095-B un formā 1095-C.
author: andreabichsel
ms.date: 12/28/2020
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
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a41195ea3b52a707ce9deae38f12eb90de2ff5aa
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805806"
---
# <a name="generate-aca-reports-in-benefits-management"></a><span data-ttu-id="6087b-103">Ģenerēt ACA pārskatus Atvieglojumu pārvaldībā</span><span class="sxs-lookup"><span data-stu-id="6087b-103">Generate ACA reports in Benefits management</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6087b-104">Atvieglojumu pārvaldība palīdz izsekot informāciju, kas ir norādīta Pieejamas aprūpes akta (ACA) darba devēja mandāta formā 1095-B un formā 1095-C.</span><span class="sxs-lookup"><span data-stu-id="6087b-104">Benefits management helps you track information that is reported on Form 1095-B and Form 1095-C for the Affordable Care Act (ACA) employer mandate.</span></span> <span data-ttu-id="6087b-105">Līdzīgi ACA pārskata iespējām vecajā **Atvieglojumu** darbvietā šī funkcionalitāte attiecas tikai uz juridiskajām personām Amerikas Savienotajās Valstīs.</span><span class="sxs-lookup"><span data-stu-id="6087b-105">Like the ACA reporting capability in the old **Benefits** workspace, this functionality applies only to legal entities in the United States.</span></span>

<span data-ttu-id="6087b-106">Lai lietotu šo funkcionalitāti, vispirms ir jāslēdz **Papildu atvieglojumu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="6087b-106">To use this functionality, you must first turn on **Advanced Benefits Management**.</span></span> <span data-ttu-id="6087b-107">Papildinformāciju, tostarp svarīgus atvieglojumu pārvaldības procesus, skatiet sadaļā [Atvieglojumu pārvaldības iespējošana vai deaktivizēšana](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span><span class="sxs-lookup"><span data-stu-id="6087b-107">For more information, including important caveats about Benefits management, see [Enable or disable Benefits management](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6087b-108">Varat izmantot ACA pārskatus tikai no darbvietas **Atvieglojumu pārvaldība** vai no vecās darbvietas **Atvieglojumi**, taču ne no abām.</span><span class="sxs-lookup"><span data-stu-id="6087b-108">You can use ACA reporting only from either the **Benefits management** workspace or the old **Benefits** workspace, not from both.</span></span> <span data-ttu-id="6087b-109">Piemēram, ja esat pārslēdzies uz Atvieglojumu pārvaldību, ACA pārskati ir pieejami tikai no **Atvieglojumu pārvaldības** darbvietas, nevis no vecās darbvietas **Atvieglojumi**.</span><span class="sxs-lookup"><span data-stu-id="6087b-109">For example, if you switched to Benefits management, ACA reporting is available only from the **Benefits management** workspace, not from the old **Benefits** workspace.</span></span>
>
> <span data-ttu-id="6087b-110">Ja pārslēdzaties uz Atvieglojumu pārvaldību reģistrācijas gada vidū, Atvieglojumu pārvaldībā pareizi jākonfigurē darbinieka dati par visu gadu.</span><span class="sxs-lookup"><span data-stu-id="6087b-110">If you switch to Benefits management in the middle of an enrollment year, you must correctly configure employee data for the whole year in Benefits management.</span></span> <span data-ttu-id="6087b-111">Šādā veidā jūs nodrošināt, ka saņemsiet precīzu pārskatu informāciju par visu gadu.</span><span class="sxs-lookup"><span data-stu-id="6087b-111">In this way, you ensure that you will receive accurate reporting information for the whole year.</span></span>

## <a name="getting-started"></a><span data-ttu-id="6087b-112">Darba sākšana</span><span class="sxs-lookup"><span data-stu-id="6087b-112">Getting started</span></span>

<span data-ttu-id="6087b-113">Lai sekotu līdzi informācijai formām 1095, vispirms izveidojiet vienu vai vairākas Pieejamās aprūpes seguma grupas.</span><span class="sxs-lookup"><span data-stu-id="6087b-113">To track information for 1095 forms, first create one or more Affordable Care coverage groups.</span></span> <span data-ttu-id="6087b-114">Šīs grupas norāda šādu informāciju:</span><span class="sxs-lookup"><span data-stu-id="6087b-114">These groups indicate the following information:</span></span>

- <span data-ttu-id="6087b-115">Darbiniekam nodrošinātais seguma piedāvājums</span><span class="sxs-lookup"><span data-stu-id="6087b-115">The offer of coverage that was provided to an employee</span></span>
- <span data-ttu-id="6087b-116">Darbinieka daļa no zemāko mēneša prēmiju izmaksām, ja izmaksas pārsniedz federālo nabadzības slieksni</span><span class="sxs-lookup"><span data-stu-id="6087b-116">The employee's share of the lowest-cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="6087b-117">Darba devēja izmantoto drošo patvērumu, ja piemērojams</span><span class="sxs-lookup"><span data-stu-id="6087b-117">The safe harbor that is used by the employer, if applicable</span></span>

<span data-ttu-id="6087b-118">Pieejamās aprūpes seguma grupas palīdz pārvaldīt šo informāciju vairākiem darbinieku ierakstiem, kuriem ir vienādi nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="6087b-118">Affordable Care coverage groups help you manage this information for multiple employee records that have the same conditions.</span></span> <span data-ttu-id="6087b-119">Grupas var viegli piešķirt vienam vai vairākiem darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="6087b-119">You can easily assign groups to one or more employees.</span></span>

### <a name="create-or-edit-an-affordable-care-coverage-group"></a><span data-ttu-id="6087b-120">Izveidot vai rediģēt Pieejamās aprūpes seguma grupu</span><span class="sxs-lookup"><span data-stu-id="6087b-120">Create or edit an Affordable Care coverage group</span></span>

1. <span data-ttu-id="6087b-121">Darbvietā **Atvieglojumu pārvaldība** atlasiet **Pieejamās aprūpes seguma grupa**.</span><span class="sxs-lookup"><span data-stu-id="6087b-121">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>

    ![Pieejamās aprūpes seguma grupas atlasīšana](./media/hr-benefits-management-aca-coverage-group.png)

2. <span data-ttu-id="6087b-123">Atlasiet **Jauns**, lai izveidotu jaunu Pieejamās aprūpes seguma grupu, vai **Rediģēt**, lai mainītu esošo grupu.</span><span class="sxs-lookup"><span data-stu-id="6087b-123">Select **New** to create a new Affordable Care coverage group or **Edit** to change an existing group.</span></span>

    ![Jauns vai Rediģēt atlasīšana](./media/hr-benefits-management-aca-new.png)

3. <span data-ttu-id="6087b-125">Iestatiet tālāk minētos laukus.</span><span class="sxs-lookup"><span data-stu-id="6087b-125">Set the following fields.</span></span>

    | <span data-ttu-id="6087b-126">Lauks</span><span class="sxs-lookup"><span data-stu-id="6087b-126">Field</span></span> | <span data-ttu-id="6087b-127">Apraksts</span><span class="sxs-lookup"><span data-stu-id="6087b-127">Description</span></span> |
    |---|---|
    | <span data-ttu-id="6087b-128">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="6087b-128">Name</span></span> | <span data-ttu-id="6087b-129">Ievadiet grupas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="6087b-129">Enter a name for the group.</span></span> |
    | <span data-ttu-id="6087b-130">Apraksts</span><span class="sxs-lookup"><span data-stu-id="6087b-130">Description</span></span> | <span data-ttu-id="6087b-131">Ievadiet grupas aprakstu.</span><span class="sxs-lookup"><span data-stu-id="6087b-131">Enter a description of the group.</span></span> |
    | <span data-ttu-id="6087b-132">Vajadzību piedāvājums</span><span class="sxs-lookup"><span data-stu-id="6087b-132">Offer of coverage</span></span> | <span data-ttu-id="6087b-133">Segums, kas tiek piedāvāts darbiniekiem, viņu dzīvesbiedram vai partnerim un viņu apgādājamajiem.</span><span class="sxs-lookup"><span data-stu-id="6087b-133">The coverage that is offered to employees, their spouse or partner, and their dependents.</span></span> |
    | <span data-ttu-id="6087b-134">Darbinieka izmaksu daļa</span><span class="sxs-lookup"><span data-stu-id="6087b-134">Employee share of cost</span></span> | <span data-ttu-id="6087b-135">Summa, par kuru darbinieks atbildīgs.</span><span class="sxs-lookup"><span data-stu-id="6087b-135">The amount that the employee is responsible for.</span></span> |
    | <span data-ttu-id="6087b-136">Piemērojamā drošā patvēruma platformas 4980H daļa</span><span class="sxs-lookup"><span data-stu-id="6087b-136">Applicable section 4980H safe harbor</span></span> | <span data-ttu-id="6087b-137">4980H drošā patvēruma vai pārejas atvieglojumu kods.</span><span class="sxs-lookup"><span data-stu-id="6087b-137">The 4980H safe harbor or transition relief code.</span></span> |
    | <span data-ttu-id="6087b-138">Plāna sākuma mēnesis</span><span class="sxs-lookup"><span data-stu-id="6087b-138">Plan start month</span></span> | <span data-ttu-id="6087b-139">Atlasiet kalendāro mēnesi, kad sākas atvieglojumu plāna gads.</span><span class="sxs-lookup"><span data-stu-id="6087b-139">Select the calendar month when your benefit plan year begins.</span></span> |
    | <span data-ttu-id="6087b-140">Grupa derīga no</span><span class="sxs-lookup"><span data-stu-id="6087b-140">Group valid from</span></span> | <span data-ttu-id="6087b-141">Pirmais datums, kad šis ieraksts ir derīgs.</span><span class="sxs-lookup"><span data-stu-id="6087b-141">The first date when this record is valid.</span></span> |
    | <span data-ttu-id="6087b-142">Grupa derīga līdz</span><span class="sxs-lookup"><span data-stu-id="6087b-142">Group valid through</span></span> | <span data-ttu-id="6087b-143">Pēdējais datums, kad šis ieraksts ir derīgs.</span><span class="sxs-lookup"><span data-stu-id="6087b-143">The last date when this record is valid.</span></span> <span data-ttu-id="6087b-144">Ja nav beigu datuma, ievadiet **Nekad**.</span><span class="sxs-lookup"><span data-stu-id="6087b-144">If there is no expiration date, enter **Never**.</span></span> |

    ![Seguma grupas izveide](./media/hr-benefits-management-aca-new-group.png)

4. <span data-ttu-id="6087b-146">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="6087b-146">Select **Save**.</span></span>

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a><span data-ttu-id="6087b-147">Vairāku darbinieku piešķiršana Pieejamās aprūpes seguma grupai</span><span class="sxs-lookup"><span data-stu-id="6087b-147">Assign multiple employees to an Affordable Care coverage group</span></span>

1. <span data-ttu-id="6087b-148">Darbvietā **Atvieglojumu pārvaldība** atlasiet **Pieejamās aprūpes seguma grupa**.</span><span class="sxs-lookup"><span data-stu-id="6087b-148">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>
2. <span data-ttu-id="6087b-149">Atlasiet grupu, kam piešķirt darbiniekus.</span><span class="sxs-lookup"><span data-stu-id="6087b-149">Select the group to assign employees to.</span></span>
3. <span data-ttu-id="6087b-150">Atlasiet **Masveida piešķire**.</span><span class="sxs-lookup"><span data-stu-id="6087b-150">Select **Mass assignment**.</span></span>

    ![Masveida piešķires atlasīšana](./media/hr-benefits-management-aca-mass-assignment.png)

4. <span data-ttu-id="6087b-152">Atlasiet sarakstā darbiniekus un pēc tam atlasiet **Piešķirt**.</span><span class="sxs-lookup"><span data-stu-id="6087b-152">Select employees in the list, and then select **Assign**.</span></span>

    ![Atlasīto darbinieku piešķiršana grupai](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a><span data-ttu-id="6087b-154">Segumu opciju vairāku versiju uzturēšana</span><span class="sxs-lookup"><span data-stu-id="6087b-154">Maintain multiple versions of coverage options</span></span>

<span data-ttu-id="6087b-155">Varat uzturēt jebkuras segumu grupas vairākas versijas.</span><span class="sxs-lookup"><span data-stu-id="6087b-155">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="6087b-156">Kad jūsu organizācijā vai sniegtajos atvieglojumos notiek kādas izmaiņas, varat saglabāt grupas informāciju vienmēr atjauninātu, neveidojiet jaunu grupu un atkārtoti nepiešķirot tai darbiniekus.</span><span class="sxs-lookup"><span data-stu-id="6087b-156">When something changes in your organization or the benefits that are offered, you can keep the group's information up to date without having to create a new group and reassign employees to it.</span></span>

<span data-ttu-id="6087b-157">Kad esat izveidojis Pieejamās aprūpes seguma grupas, varat tām piešķirt darbiniekus masveidā.</span><span class="sxs-lookup"><span data-stu-id="6087b-157">After you've created Affordable Care coverage groups, you can mass-assign employees to them.</span></span> <span data-ttu-id="6087b-158">Varat arī atsevišķi piešķirt darbiniekus grupām, kā arī norādīt, vai ACA informācija tiek izsekota un norādīta pārskatā.</span><span class="sxs-lookup"><span data-stu-id="6087b-158">You can also individually assign employees to groups, and indicate whether ACA information is tracked and reported.</span></span>

<span data-ttu-id="6087b-159">Ja nav nepieciešams izsekot darbinieka ACA informāciju un norādīt to, varat iestatīt opciju **Norādīt segumu** uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="6087b-159">If you don't have to track and report ACA information for an employee, you can set the **Report coverage** option to **No**.</span></span> <span data-ttu-id="6087b-160">Piemēram, jums ir nepilna laika darbinieki, kuri nav jānorāda ACA pārskatos.</span><span class="sxs-lookup"><span data-stu-id="6087b-160">For example, you might have part-time employees who don't require ACA reporting.</span></span>

### <a name="override-default-values-for-an-employee"></a><span data-ttu-id="6087b-161">Ignorējiet darbinieka noklusētās vērtības</span><span class="sxs-lookup"><span data-stu-id="6087b-161">Override default values for an employee</span></span>

<span data-ttu-id="6087b-162">Darbiniekiem, kas piešķirti Pieejamās aprūpes seguma grupai, jūs varat mainīt šādas opcijas par mēnešiem, kam nepieciešamas citas vērtības:</span><span class="sxs-lookup"><span data-stu-id="6087b-162">For employees who are assigned to an Affordable Care coverage group, you can change the following options for any months that require different values:</span></span>

- <span data-ttu-id="6087b-163">Vajadzību piedāvājums</span><span class="sxs-lookup"><span data-stu-id="6087b-163">Offer of coverage</span></span>
- <span data-ttu-id="6087b-164">Darbinieka izmaksu daļa</span><span class="sxs-lookup"><span data-stu-id="6087b-164">Employee share of cost</span></span>
- <span data-ttu-id="6087b-165">Piemērojamā drošā patvēruma platformas 4980H daļa</span><span class="sxs-lookup"><span data-stu-id="6087b-165">Applicable section 4980H safe harbor</span></span>

> [!NOTE]
> <span data-ttu-id="6087b-166">2020. gada ACA pārskatiem formā 1095-C jānorāda gan darba, gan mājas pasta indeksi.</span><span class="sxs-lookup"><span data-stu-id="6087b-166">For 2020 ACA reports, you must report both work and home ZIP Codes on Form 1095-C.</span></span> <span data-ttu-id="6087b-167">Vērtības tiek aizpildītas automātiski, pamatojoties uz pašreizējām aktīvām atrašanās vietām.</span><span class="sxs-lookup"><span data-stu-id="6087b-167">Values are automatically filled in, based on current active locations.</span></span> <span data-ttu-id="6087b-168">Ja kādā gada daļā kāda no atrašanās vietām bija atšķirīga, vērtība ir jāignorē.</span><span class="sxs-lookup"><span data-stu-id="6087b-168">If either location was different during any part of the year, you must override the value.</span></span> <span data-ttu-id="6087b-169">Lauks **Pasta indekss** (17. rinda) pārskatā 1095-C tiek aizpildīts tikai tad, ja kods **Seguma piedāvājums** ietver **1L** līdz **1Q**, kā redzams zemāk:</span><span class="sxs-lookup"><span data-stu-id="6087b-169">The **ZIP Code** field (line 17) of the 1095-C report is filled in only if the **Offer of coverage** code contains **1L** through **1Q**, as follows:</span></span>
>
> - <span data-ttu-id="6087b-170">**1L, 1M vai 1N:** primārās dzīvesvietas pasta indekss</span><span class="sxs-lookup"><span data-stu-id="6087b-170">**1L, 1M, or 1N:** The primary residence ZIP Code</span></span>
> - <span data-ttu-id="6087b-171">**1O, 1P, 1Q:** primārās darba vietas pasta indekss</span><span class="sxs-lookup"><span data-stu-id="6087b-171">**1O, 1P, 1Q:** The primary work ZIP Code</span></span>

<span data-ttu-id="6087b-172">Lai ievadītu izņēmumus jebkādām seguma grupas vērtībām, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="6087b-172">To enter exceptions for any values of an Affordable Care coverage group, follow these steps.</span></span>

1. <span data-ttu-id="6087b-173">**Personāla vadības** darbvietā atlasiet **Saites** un pēc tam atlasiet **Darbinieki**.</span><span class="sxs-lookup"><span data-stu-id="6087b-173">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>
2. <span data-ttu-id="6087b-174">Sarakstā atlasiet darbinieku.</span><span class="sxs-lookup"><span data-stu-id="6087b-174">Select the employee in the list.</span></span>
3. <span data-ttu-id="6087b-175">Cilnes **Nodarbinātība** sadaļā **Papildinformācija** atlasiet **Pieejamās aprūpes segums**.</span><span class="sxs-lookup"><span data-stu-id="6087b-175">On the **Employment** tab, in the **More information** section, select **Affordable Care coverage**.</span></span>

    ![Darbinieka opciju maiņa](./media/hr-benefits-management-aca-change-single-employee.png)

4. <span data-ttu-id="6087b-177">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="6087b-177">Select **Edit**.</span></span>
5. <span data-ttu-id="6087b-178">Katram mēnesim, kam nepieciešamas izmaiņas, atzīmējiet izvēles rūtiņu **Ignorēt noklusējumu** un pēc tam mainiet pārējās vērtības pēc vajadzības.</span><span class="sxs-lookup"><span data-stu-id="6087b-178">For each month that requires changes, select the **Override default** check box, and then change the other values as required.</span></span>

    ![Noklusēto vērtību ignorēšana](./media/hr-benefits-management-aca-override-default.png)

6. <span data-ttu-id="6087b-180">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="6087b-180">Select **Save**.</span></span>

## <a name="report-health-care-coverage"></a><span data-ttu-id="6087b-181">Veselības aprūpes seguma pārskats</span><span class="sxs-lookup"><span data-stu-id="6087b-181">Report health care coverage</span></span>

<span data-ttu-id="6087b-182">Ir jāizseko jebkāds darba devēja sponsorēts paša apdrošināts veselības aprūpes segums pilna laika un nepilna laika darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="6087b-182">You must track any employer-sponsored, self-insured health care coverage for full-time and part-time employees.</span></span> <span data-ttu-id="6087b-183">Ietveriet katru darbinieku kopā ar viņu apgādājamiem 1095-C pārskatā par mēnešiem, kad viņi tika segti.</span><span class="sxs-lookup"><span data-stu-id="6087b-183">Include each employee, together with their dependents, on the 1095-C report for the months when they were covered.</span></span>

<span data-ttu-id="6087b-184">Lai norādītu, vai jāsniedz pārskats par atvieglojumu plānu, izpildiet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="6087b-184">To indicate whether a benefit plan must be reported, follow these steps.</span></span>

1. <span data-ttu-id="6087b-185">Darbvietā **Atvieglojumu pārvaldība** atlasiet **Atvieglojumu plāni**.</span><span class="sxs-lookup"><span data-stu-id="6087b-185">In the **Benefits management** workspace, select **Benefit plans**.</span></span>
2. <span data-ttu-id="6087b-186">Atlasiet atvieglojumu plānu pārskatam.</span><span class="sxs-lookup"><span data-stu-id="6087b-186">Select the benefit plan to report.</span></span>
3. <span data-ttu-id="6087b-187">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="6087b-187">Select **Edit**.</span></span>
4. <span data-ttu-id="6087b-188">Iestatiet opciju **Norādīts pārskatā saskaņā ar Pieejamās aprūpes aktu** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="6087b-188">Set the **Reported under the Affordable Care Act** option to **Yes**.</span></span>

    ![Veselības aprūpes seguma ziņošana](./media/hr-benefits-management-aca-report-coverage.png)

5. <span data-ttu-id="6087b-190">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="6087b-190">Select **Save**.</span></span>

<span data-ttu-id="6087b-191">Ja darbinieks izvēlas apgādājamā veselības aprūpes segumu, apgādājamā seguma periodu nosaka datums, kad apgādājamais tika reģistrēts vai noņemts.</span><span class="sxs-lookup"><span data-stu-id="6087b-191">If an employee chooses health care coverage for a dependent, the dependent's coverage period is determined by the date when the dependent was enrolled or removed.</span></span> <span data-ttu-id="6087b-192">Seguma datumi apgādājamajiem tiek automātiski aprēķināti, pamatojoties uz periodu, kad apgādājamais bija tiesīgs un aktīvs plānā reģistrācijas gada laikā.</span><span class="sxs-lookup"><span data-stu-id="6087b-192">Coverage dates for dependents are automatically calculated based on the period when the dependent was eligible and active in a plan during the enrollment year.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="6087b-193">Formu 1095-B un 1095-C ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="6087b-193">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="6087b-194">Šī produkta ietvaros varat ģenerēt ACA formas 1095-B un 1095-C un pēc tam tās izdalīt katram no saviem darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="6087b-194">You can generate ACA 1095-B and 1095-C forms, and then distribute them to each of your employees.</span></span> <span data-ttu-id="6087b-195">Varat arī elektroniski ģenerēt formu 1095-C un atbilstošos 1094-C pārsūtāmos failus, lai nosūtītu Iekšējam ieņēmumu dienestam (IRS).</span><span class="sxs-lookup"><span data-stu-id="6087b-195">You can also electronically generate Form 1095-C and the corresponding 1094-C transmittal files to send to the Internal Revenue Service (IRS).</span></span>

1. <span data-ttu-id="6087b-196">Darbvietā **Atvieglojumu pārvaldība** atlasiet **ACA 1095-B forma** vai **ACA 1095-C forma**.</span><span class="sxs-lookup"><span data-stu-id="6087b-196">In the **Benefits management** workspace, select **ACA 1095-B form** or **ACA 1095-C form**.</span></span>
2. <span data-ttu-id="6087b-197">Pēc vajadzības mainiet parametrus un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6087b-197">Change the parameters as required, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6087b-198">Ja drukājat formas 1095-C vairāk nekā 500 darbiniekiem, jūs saņemsiet vairāk nekā vienu PDF failu.</span><span class="sxs-lookup"><span data-stu-id="6087b-198">If you're printing 1095-C forms for more than 500 employees, you will receive more than one PDF file.</span></span> <span data-ttu-id="6087b-199">Iesakām palielināt lauka **Maksimālais faila lielums megabaitos** vērtību lapā **Dokumentu pārvaldības parametri** uz **150**.</span><span class="sxs-lookup"><span data-stu-id="6087b-199">We recommend that you increase the value of the **Maximum file size in megabytes** field on the **Document management parameters** page to **150**.</span></span> <span data-ttu-id="6087b-200">(Lai ātri atvērtu šo lapu, varat izmantot meklēšanas lauku navigācijas joslā.)</span><span class="sxs-lookup"><span data-stu-id="6087b-200">(To quickly open that page, you can use the search field on the navigation bar.)</span></span>
    >
    > ![Maksimālā faila lieluma maiņa](./media/hr-benefits-management-aca-maximum-file-size.png)

3. <span data-ttu-id="6087b-202">Lai pārbaudītu pārskatu statusu un tos skatītu, izmantojiet meklēšanas lauku navigācijas joslā, lai atvērtu lapu **Elektronisko pārskatu izveides darbi**.</span><span class="sxs-lookup"><span data-stu-id="6087b-202">To check the status of your reports and view them, use the search field on the navigation bar to open the **Electronic reporting jobs** page.</span></span>

    ![Elektronisko pārskatu izveides darbu lapas meklēšana](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. <span data-ttu-id="6087b-204">Atlasiet skatāmo pārskatu un pēc tam atlasiet **Rādīt failus**.</span><span class="sxs-lookup"><span data-stu-id="6087b-204">Select the report to view, and then select **Show files**.</span></span>

    ![Failu rādīšana](./media/hr-benefits-management-aca-show-files.png)

5. <span data-ttu-id="6087b-206">Atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="6087b-206">Select **Open**.</span></span>

    ![Faila atvēršana](./media/hr-benefits-management-aca-open-file.png)

6. <span data-ttu-id="6087b-208">No paziņojumu joslas, kas tiek parādīta pārlūkprogrammas loga apakšā, atveriet tilpsaspiesto failu un pēc tam atlasiet pārskatu.</span><span class="sxs-lookup"><span data-stu-id="6087b-208">From the Notification bar that appears at the bottom of the browser window, open the zip file, and then select the report.</span></span> <span data-ttu-id="6087b-209">Varat apskatīt vai drukāt PDF failu.</span><span class="sxs-lookup"><span data-stu-id="6087b-209">You can view or print the PDF file.</span></span>

    ![Parauga forma 1095-C](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a><span data-ttu-id="6087b-211">ACA seguma informācijas skatīšana</span><span class="sxs-lookup"><span data-stu-id="6087b-211">View ACA coverage information</span></span>

<span data-ttu-id="6087b-212">Lapā **Darbinieka Pieejamās aprūpes segums** tiek rādīta šāda informācija:</span><span class="sxs-lookup"><span data-stu-id="6087b-212">The **Worker Affordable Care coverage** page shows the following information:</span></span>

- <span data-ttu-id="6087b-213">Darbinieki, kuri piešķirti katrai seguma grupai</span><span class="sxs-lookup"><span data-stu-id="6087b-213">Employees who are assigned to each coverage group</span></span>
- <span data-ttu-id="6087b-214">Darbinieki, kuri nav jāiekļauj pārskatā</span><span class="sxs-lookup"><span data-stu-id="6087b-214">Employees who don't have to be included on a report</span></span>
- <span data-ttu-id="6087b-215">Nepiešķirtie darbinieki</span><span class="sxs-lookup"><span data-stu-id="6087b-215">Unassigned employees</span></span>

<span data-ttu-id="6087b-216">Lai apskatītu šo informāciju, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="6087b-216">To view this information, follow these steps.</span></span>

1. <span data-ttu-id="6087b-217">Darbvietā **Atvieglojumu pārvaldība** atlasiet **Darbinieka Pieejamās aprūpes segums**.</span><span class="sxs-lookup"><span data-stu-id="6087b-217">In the **Benefits management** workspace, select **Worker Affordable Care coverage**.</span></span>
2. <span data-ttu-id="6087b-218">Laukā **Grupas nosaukums** atlasiet grupu.</span><span class="sxs-lookup"><span data-stu-id="6087b-218">In the **Group name** field, select a group.</span></span>

    ![ACA seguma skatīšana](./media/hr-benefits-management-aca-view-coverage.png)

<span data-ttu-id="6087b-220">Ja kāda no pieejamās aprūpes seguma grupas noklusējuma vērtībām ir pārrakstīta, pie mainītās vērtības tiek rādīta zvaigznīte.</span><span class="sxs-lookup"><span data-stu-id="6087b-220">If any default values from the Affordable Care coverage group have been overridden, an asterisk appears next to the value that was changed.</span></span> <span data-ttu-id="6087b-221">Ja vērtības visiem 12 mēnešiem ir vienādas un nav tikušas pārrakstītas, tad vērtība tiek rādīta kolonnā **Visi 12 mēneši**.</span><span class="sxs-lookup"><span data-stu-id="6087b-221">If the values for all 12 months are the same and haven't been overridden, the value appears in the **All 12 months** column.</span></span>

<span data-ttu-id="6087b-222">Varat skatīt darbiniekus, kuri ir atzīmēti kā tādi, kuri ACA pārskatā nav jānorāda, un kuriem nebūs nepieciešama forma 1095-C.</span><span class="sxs-lookup"><span data-stu-id="6087b-222">You can view employees who are marked as not ACA-reportable, and who won't require a Form 1095-C.</span></span> <span data-ttu-id="6087b-223">Laukā **Filtrēt pēc** atlasiet **Nav jānorāda ACA pārskatā**.</span><span class="sxs-lookup"><span data-stu-id="6087b-223">In the **Filter by** field, select **Not ACA reportable**.</span></span>

<span data-ttu-id="6087b-224">Varat skatīt darbiniekus, kuri nav piešķirti grupai vai kuri ir piešķirti grupai, kurai beidzies derīguma termiņš.</span><span class="sxs-lookup"><span data-stu-id="6087b-224">You can view employees who aren't assigned to a group, or who are assigned to an expired group.</span></span> <span data-ttu-id="6087b-225">Laukā **Filtrēt pēc** atlasiet **Nepiešķirts vai grupai beidzies derīguma termiņš**.</span><span class="sxs-lookup"><span data-stu-id="6087b-225">In the **Filter by** field, select **Unassigned or expired group**.</span></span>

### <a name="export-to-excel"></a><span data-ttu-id="6087b-226">Eksportēt programmā Excel</span><span class="sxs-lookup"><span data-stu-id="6087b-226">Export to Excel</span></span>

<span data-ttu-id="6087b-227">Lai eksportētu kādu no sarakstiem uz Microsoft Excel, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="6087b-227">To export any of the lists to Microsoft Excel, follow these steps.</span></span>

1. <span data-ttu-id="6087b-228">Atlasiet pogu **Atvērt programmā Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="6087b-228">Select the **Open in Microsoft Office** button.</span></span>
2. <span data-ttu-id="6087b-229">Atlasiet **HCM Human Resources pagaidu tabula iekšējai lietošanai**.</span><span class="sxs-lookup"><span data-stu-id="6087b-229">Select **HCM Human Resources temporary table for internal use**.</span></span>
3. <span data-ttu-id="6087b-230">Atlasiet **Lejupielādēt**.</span><span class="sxs-lookup"><span data-stu-id="6087b-230">Select **Download**.</span></span>

### <a name="view-aca-reportable-dependents"></a><span data-ttu-id="6087b-231">Skatīt ACA pārskatā norādāmos apgādājamos</span><span class="sxs-lookup"><span data-stu-id="6087b-231">View ACA-reportable dependents</span></span>

<span data-ttu-id="6087b-232">Ja jums ir jāsniedz pārskats par iekļautajām personām, jo jūs nodrošināt paša apdrošinātu segumu, varat apskatīt visus apgādājamos, kas ietverti atvieglojumu plānos, kuri atzīmēti kā **Norādāmi ACA pārskā**.</span><span class="sxs-lookup"><span data-stu-id="6087b-232">If you must report covered individuals because you provide self-insured coverage, you can view dependents who are covered under benefit plans that are marked as **ACA reportable**.</span></span> <span data-ttu-id="6087b-233">Darbību rūtī atlasiet **Skatīt apgādājamā segumu**.</span><span class="sxs-lookup"><span data-stu-id="6087b-233">On the Action Pane, select **View Dependent coverage**.</span></span>

![Apgādājamā seguma skatīšana](./media/hr-benefits-management-aca-view-dependent-coverage.png)

<span data-ttu-id="6087b-235">Tiek rādīta seguma informācija par darbinieka apgādājamiem.</span><span class="sxs-lookup"><span data-stu-id="6087b-235">Coverage information for the employee's dependents is shown.</span></span>

![Apgādājamo segums](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> <span data-ttu-id="6087b-237">Lapā tiek rādīti tikai tie atvieglojumu plāni, kas ir atzīmēti kā **Norādāmi ACA pārskatā**.</span><span class="sxs-lookup"><span data-stu-id="6087b-237">The page shows only benefits plans that are marked as **ACA reportable**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]