---
title: "Projektu līgumi"
description: "Šajā rakstā aprakstīti projektu līgumi, ko var izveidot dažādu veidu projektiem un finansējuma avotiem, kā arī sniegti to piemēri, un aprakstīts, kā var pārvaldīt līgumus un izrakstīt projekta rēķinus debitoriem programmatūras Microsoft Dynamics 365 for Finance and Operations izdevumā Enterprise."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: 0d7d3b64b0d6a662246074b12e3a3fe105dfae47
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2017

---

# <a name="project-contracts"></a><span data-ttu-id="e3531-103">Projekta līgumi</span><span class="sxs-lookup"><span data-stu-id="e3531-103">Project contracts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e3531-104">Šajā rakstā aprakstīti projektu līgumi, ko var izveidot dažādu veidu projektiem un finansējuma avotiem, kā arī sniegti to piemēri, un aprakstīts, kā var pārvaldīt līgumus un izrakstīt projekta rēķinus debitoriem programmatūras Microsoft Dynamics 365 for Finance and Operations izdevumā Enterprise.</span><span class="sxs-lookup"><span data-stu-id="e3531-104">This article describes and provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

<span data-ttu-id="e3531-105">Projekta tips, ko izveidojat projekta līgumam, nosaka metodi, kas tiek izmantota projekta debitoru rēķinu izrakstīšanai.</span><span class="sxs-lookup"><span data-stu-id="e3531-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="e3531-106">Varat mainīt projekta līgumu un saistīto projektu, bet projekta tipu nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="e3531-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="e3531-107">Izmantojot projekta līgumu, vienlaicīgi varat izrakstīt rēķinu vienam vai vairākiem projektiem.</span><span class="sxs-lookup"><span data-stu-id="e3531-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="e3531-108">Projekta līgums palīdz arī garantēt konsekventu rēķinu izrakstīšanas procedūru katram projekta struktūrā iekļautajam apakšprojektam.</span><span class="sxs-lookup"><span data-stu-id="e3531-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="e3531-109">Katram projektam, kam tiks izrakstīts rēķins, ir jābūt saistītam ar projekta līgumu.</span><span class="sxs-lookup"><span data-stu-id="e3531-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="e3531-110">Projekta līguma iestatījumi attiecas uz visiem projektiem un apakšprojektiem, kas ir saistīti ar attiecīgo projekta līgumu.</span><span class="sxs-lookup"><span data-stu-id="e3531-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="e3531-111">Projekta līgumā var norādīt vienu vai vairākus finansējuma avotus.</span><span class="sxs-lookup"><span data-stu-id="e3531-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="e3531-112">Līdz ar to norēķinus varat sadalīt starp vairākiem finansētājiem, iestatīt finansējuma ierobežojumus, lai no finansējuma avotiem netiktu iekasēts vairāk par noteikto summu, un konfigurēt iekasējamo izdevumu finansējuma nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="e3531-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="e3531-113">Projekta līgumu finansējums</span><span class="sxs-lookup"><span data-stu-id="e3531-113">Funding for project contracts</span></span>
<span data-ttu-id="e3531-114">Noteiktos projektu līgumos ir norādīts, ka par projekta izmaksu finansēšanu kopīgi atbild vairākas puses.</span><span class="sxs-lookup"><span data-stu-id="e3531-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="e3531-115">Daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="e3531-115">Here are some examples:</span></span>

-   <span data-ttu-id="e3531-116">Liels debitors ar vairākām nodaļām pieprasa, lai projekta finansējums tiktu sadalīts pēc nodaļas.</span><span class="sxs-lookup"><span data-stu-id="e3531-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="e3531-117">Jūsu uzņēmumam un kādai ārējai organizācijai ir kopējas izmaksas par lielu projektu.</span><span class="sxs-lookup"><span data-stu-id="e3531-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="e3531-118">Divas pašvaldības kopīgi finansē ceļubūves projektu.</span><span class="sxs-lookup"><span data-stu-id="e3531-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="e3531-119">Tilta projektu finansē valsts dotācijas un privāta korporācija.</span><span class="sxs-lookup"><span data-stu-id="e3531-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="e3531-120">Programmatūrā Finance and Operations norēķinus par vienu transakciju vai visu projektu varat sadalīt starp vairākiem debitoriem, dotācijām vai organizācijām.</span><span class="sxs-lookup"><span data-stu-id="e3531-120">In Finance and Operations, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="e3531-121">Projektos, kuriem ir vairāki finansētāji, visas puses, kas sniedz līdzekļus projekta papildu finansēšanai, tiek saukti par finansējuma avotiem.</span><span class="sxs-lookup"><span data-stu-id="e3531-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="e3531-122">Kad debitors, organizācija vai dotācija ir definēti kā finansējuma avots, to var piešķirt vienam vai vairākiem finansējuma nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="e3531-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="e3531-123">Finansējuma nosacījumi ietver kritērijus, kas nosaka, kā izmaksas tiek sadalītas starp projekta dažādajiem finansējuma avotiem.</span><span class="sxs-lookup"><span data-stu-id="e3531-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="e3531-124">Tā kā uzkrātos krājumus, piemēram, tādus, kas ir minēti pirkšanas pieprasījumos un pirkšanas pasūtījumos, nevar sadalīt, sadales laikā šo izmaksu summu nevar sadalīt starp vairākiem finansējuma avotiem.</span><span class="sxs-lookup"><span data-stu-id="e3531-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="e3531-125">Tāpēc finansējuma avota vērtība paliek 0 (nulle), līdz tiek iegrāmatota krājumu izejas plūsma.</span><span class="sxs-lookup"><span data-stu-id="e3531-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="e3531-126">Kad tiek grāmatota krājumu izejas plūsma, izmaksu summa tiek sadalīta saskaņā ar projekta konta sadales nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="e3531-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="e3531-127">Tālāk ir aprakstītas dažas darbības, kas varētu atvieglot norēķinu sadali starp vairākiem finansējuma avotiem.</span><span class="sxs-lookup"><span data-stu-id="e3531-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="e3531-128">Norādiet, ka visās projektam ievadītajās transakcijās ir jāizmanto tā pati pārdošanas valūta kā projekta līgumā.</span><span class="sxs-lookup"><span data-stu-id="e3531-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="e3531-129">Iestatiet finansējuma ierobežojumus, lai finansējuma avotam netiktu izrakstīts rēķins, kas pārsniedz noteiktu summu saistībā ar projektu.</span><span class="sxs-lookup"><span data-stu-id="e3531-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="e3531-130">Konfigurējiet finansējuma nosacījumus un finansējuma ierobežojumus katram darbiniekam, krājumam, kategorijai, kategoriju grupai un transakcijas tipam (vai visiem transakciju tipiem).</span><span class="sxs-lookup"><span data-stu-id="e3531-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="e3531-131">Atlasiet papildu sākuma un beigu datumus, lai definētu periodu, kad ir spēkā katrs finansējuma nosacījums.</span><span class="sxs-lookup"><span data-stu-id="e3531-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="e3531-132">Norādiet procentus, par ko ir atbildīgs katrs finansējuma avots.</span><span class="sxs-lookup"><span data-stu-id="e3531-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="e3531-133">Norādiet, kurš finansējuma avots ir atbildīgs par noapaļošanas atšķirībām, ko izraisa finansējuma sadalījuma aprēķini.</span><span class="sxs-lookup"><span data-stu-id="e3531-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="e3531-134">Iestatiet kārtulas, kas nosaka veidu, kādā par projekta izmaksām tiek izrakstīti rēķini ārējiem debitoriem un kā projekta izmaksas tiek iekasētas iekšējām organizācijām.</span><span class="sxs-lookup"><span data-stu-id="e3531-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="e3531-135">Reģistrējiet transakcijas aizturēšanas finansējuma kontā, līdz var iegūt papildu finansējumu vai līdz izlemjat šīs izmaksas segt iekšēji.</span><span class="sxs-lookup"><span data-stu-id="e3531-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="e3531-136">Lai noteiktu, kuru nodokļu grupu saistīt ar kādu transakciju, projektā tiek meklēta nodokļu grupas piešķire.</span><span class="sxs-lookup"><span data-stu-id="e3531-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="e3531-137">Ja nodokļu grupas piešķire nav veikta projekta līmenī, tiek meklēts projekta līgumā.</span><span class="sxs-lookup"><span data-stu-id="e3531-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="e3531-138">Piemērs. Vairāki finansējuma avoti (vienkārši)</span><span class="sxs-lookup"><span data-stu-id="e3531-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="e3531-139">Nākamajā tabulā ir sniegti scenāriji finansējuma sadalījuma pārvaldīšanai starp vairākiem finansējuma avotiem.</span><span class="sxs-lookup"><span data-stu-id="e3531-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="e3531-140">Šie scenāriji ir balstīti uz šādiem pieņēmumiem:</span><span class="sxs-lookup"><span data-stu-id="e3531-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="e3531-141">Prioritātes iestatījumi ir iestrādāti līdzekļu sadalījumā, pirms tiek lietoti citi finansējuma nosacījumu kritēriji.</span><span class="sxs-lookup"><span data-stu-id="e3531-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="e3531-142">Nav norādīts datumu diapazons, lai definētu periodu d, kad ir spēkā šie finansējuma nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="e3531-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e3531-143"><strong>Scenārijs</strong></span><span class="sxs-lookup"><span data-stu-id="e3531-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="e3531-144"><strong>Finansējuma avots </strong></span><span class="sxs-lookup"><span data-stu-id="e3531-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="e3531-145"><strong>Sadalījuma procenti </strong></span><span class="sxs-lookup"><span data-stu-id="e3531-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="e3531-146"><strong>Sadalījuma prioritāte </strong></span><span class="sxs-lookup"><span data-stu-id="e3531-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3531-147">Jūs vēlaties piešķirt izmaksas vienam finansējuma avotam, līdz tā līdzekļi ir beigušies, piešķirt izmaksas otram finansējuma avotam, līdz tā līdzekļi ir beigušies, un visbeidzot atlikušās izmaksas piešķirt trešajam finansējuma avotam.</span><span class="sxs-lookup"><span data-stu-id="e3531-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="e3531-148">1.　finansējuma　avots</span><span class="sxs-lookup"><span data-stu-id="e3531-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="e3531-149">2.　finansējuma　avots</span><span class="sxs-lookup"><span data-stu-id="e3531-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="e3531-150">3.　finansējuma　avots</span><span class="sxs-lookup"><span data-stu-id="e3531-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e3531-151">100%</span><span class="sxs-lookup"><span data-stu-id="e3531-151">100%</span></span></li>
<li><span data-ttu-id="e3531-152">100%</span><span class="sxs-lookup"><span data-stu-id="e3531-152">100%</span></span></li>
<li><span data-ttu-id="e3531-153">100%</span><span class="sxs-lookup"><span data-stu-id="e3531-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e3531-154">1</span><span class="sxs-lookup"><span data-stu-id="e3531-154">1</span></span></li>
<li><span data-ttu-id="e3531-155">2</span><span class="sxs-lookup"><span data-stu-id="e3531-155">2</span></span></li>
<li><span data-ttu-id="e3531-156">3</span><span class="sxs-lookup"><span data-stu-id="e3531-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3531-157">Jūs vēlaties 75 procentus izmaksu piešķirt vienam finansējuma avotam un 25 procentus piešķirt otram finansējuma avotam.</span><span class="sxs-lookup"><span data-stu-id="e3531-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="e3531-158">Kad kādam no šiem finansējuma avotiem ir beigušies līdzekļi, jūs vēlaties atlikušās izmaksas samaksāt no trešā finansējuma avota.</span><span class="sxs-lookup"><span data-stu-id="e3531-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="e3531-159">1.　finansējuma　avots</span><span class="sxs-lookup"><span data-stu-id="e3531-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="e3531-160">2.　finansējuma　avots</span><span class="sxs-lookup"><span data-stu-id="e3531-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="e3531-161">3.　finansējuma　avots</span><span class="sxs-lookup"><span data-stu-id="e3531-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e3531-162">75%</span><span class="sxs-lookup"><span data-stu-id="e3531-162">75%</span></span></li>
<li><span data-ttu-id="e3531-163">25%</span><span class="sxs-lookup"><span data-stu-id="e3531-163">25%</span></span></li>
<li><span data-ttu-id="e3531-164">100%</span><span class="sxs-lookup"><span data-stu-id="e3531-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e3531-165">1</span><span class="sxs-lookup"><span data-stu-id="e3531-165">1</span></span></li>
<li><span data-ttu-id="e3531-166">1</span><span class="sxs-lookup"><span data-stu-id="e3531-166">1</span></span></li>
<li><span data-ttu-id="e3531-167">2</span><span class="sxs-lookup"><span data-stu-id="e3531-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3531-168">Jūs vēlaties 75 procentus izmaksu piešķirt vienam finansējuma avotam un 25 procentus piešķirt otram finansējuma avotam.</span><span class="sxs-lookup"><span data-stu-id="e3531-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="e3531-169">Kad kādam no šiem finansējuma avotiem ir beigušies līdzekļi, jūs vēlaties atlikušās izmaksas sadalīt starp trešo finansējuma avotu un ceturto finansējuma avotu.</span><span class="sxs-lookup"><span data-stu-id="e3531-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="e3531-170">1.　finansējuma　avots</span><span class="sxs-lookup"><span data-stu-id="e3531-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="e3531-171">2.　finansējuma　avots</span><span class="sxs-lookup"><span data-stu-id="e3531-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="e3531-172">3.　finansējuma　avots</span><span class="sxs-lookup"><span data-stu-id="e3531-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="e3531-173">4.　finansējuma　avots</span><span class="sxs-lookup"><span data-stu-id="e3531-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e3531-174">75%</span><span class="sxs-lookup"><span data-stu-id="e3531-174">75%</span></span></li>
<li><span data-ttu-id="e3531-175">25%</span><span class="sxs-lookup"><span data-stu-id="e3531-175">25%</span></span></li>
<li><span data-ttu-id="e3531-176">50%</span><span class="sxs-lookup"><span data-stu-id="e3531-176">50%</span></span></li>
<li><span data-ttu-id="e3531-177">50%</span><span class="sxs-lookup"><span data-stu-id="e3531-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e3531-178">1</span><span class="sxs-lookup"><span data-stu-id="e3531-178">1</span></span></li>
<li><span data-ttu-id="e3531-179">1</span><span class="sxs-lookup"><span data-stu-id="e3531-179">1</span></span></li>
<li><span data-ttu-id="e3531-180">2</span><span class="sxs-lookup"><span data-stu-id="e3531-180">2</span></span></li>
<li><span data-ttu-id="e3531-181">2</span><span class="sxs-lookup"><span data-stu-id="e3531-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3531-182">Jūs vēlaties pirmos 25 procentus izmaksu piešķirt vienam finansējuma avotam, un pārējo piešķirt otram finansējuma avotam.</span><span class="sxs-lookup"><span data-stu-id="e3531-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="e3531-183">1.　finansējuma　avots</span><span class="sxs-lookup"><span data-stu-id="e3531-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="e3531-184">2.　finansējuma　avots</span><span class="sxs-lookup"><span data-stu-id="e3531-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e3531-185">25%</span><span class="sxs-lookup"><span data-stu-id="e3531-185">25%</span></span></li>
<li><span data-ttu-id="e3531-186">100%</span><span class="sxs-lookup"><span data-stu-id="e3531-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e3531-187">1</span><span class="sxs-lookup"><span data-stu-id="e3531-187">1</span></span></li>
<li><span data-ttu-id="e3531-188">2</span><span class="sxs-lookup"><span data-stu-id="e3531-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="e3531-189">Piemērs. Vairāki finansējuma avoti (kompleksi)</span><span class="sxs-lookup"><span data-stu-id="e3531-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="e3531-190">Jums ir trīs finansējuma avoti, kurus vēlaties izmantot šādā secībā:</span><span class="sxs-lookup"><span data-stu-id="e3531-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="e3531-191">Izmantot 2. finansējuma avotu 3. finansējuma avotu vienādi, līdz 2. finansējuma avota līdzekļi ir beigušies.</span><span class="sxs-lookup"><span data-stu-id="e3531-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="e3531-192">Turpināt lietot 3. finansējuma avotu, līdz tā līdzekļi ir beigušies.</span><span class="sxs-lookup"><span data-stu-id="e3531-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="e3531-193">Lietot 1. finansējuma avotu pēc tam, kad 3. finansējuma avota līdzekļi ir beigušies.</span><span class="sxs-lookup"><span data-stu-id="e3531-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="e3531-194">Lai sasniegtu šo mērķi, jums ir jārīkojas tālāk aprakstītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="e3531-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="e3531-195">Iestatiet finansējuma ierobežojumus 2. finansējuma avotam un 3. finansējuma avotam to attiecīgajām summām.</span><span class="sxs-lookup"><span data-stu-id="e3531-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="e3531-196">Izveidojiet šādus finansējuma nosacījumus:</span><span class="sxs-lookup"><span data-stu-id="e3531-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="e3531-197">1. nosacījums (1. prioritāte): 50 procentus no transakcijām piešķirt 2. finansējuma avotam un 50 procentus piešķirt 3. finansējuma avotam.</span><span class="sxs-lookup"><span data-stu-id="e3531-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="e3531-198">2. nosacījums (2. prioritāte): 100 procentus no transakcijām piešķirt 3. finansējuma avotam.</span><span class="sxs-lookup"><span data-stu-id="e3531-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="e3531-199">3. nosacījums (3. prioritāte): 100 procentus no transakcijām piešķirt 1. finansējuma avotam.</span><span class="sxs-lookup"><span data-stu-id="e3531-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="e3531-200">Šāds iestatījums darbojas, jo transakcijas tiek pārbaudītas attiecībā pret nosacījumiem un ierobežojumiem, lai noteiktu, vai kāds no tiem attiecas uz šo transakciju.</span><span class="sxs-lookup"><span data-stu-id="e3531-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="e3531-201">Ja uz transakciju neattiecas kādi īpaši nosacījumi vai ierobežojumi, tiek lietots nosacījums Visas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="e3531-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="e3531-202">Nosacījums Visas transakcijas salīdzina visas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="e3531-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="e3531-203">Ja tiek atrasts nosacījums, kas atbilst transakcijai, tad vispirms tiek lietots procentuālais daudzums, kurš ir piešķirts šajā nosacījumā, bet tikai pēc tam, kad atbilstības ir pārbaudītas pret visiem iestatītajiem ierobežojumiem.</span><span class="sxs-lookup"><span data-stu-id="e3531-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="e3531-204">Ja ir sasniegts ierobežojums un finansējuma avota līdzekļi ir beigušies, ar šo finansējuma ierobežojumu saistītie finansējuma nosacījumi tiek ignorēti, un programma pārbauda nākamos piemērojamos nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="e3531-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="e3531-205">Noteiktos gadījumos saskaņā ar nosacījumiem sadali var izpildīt tikai daļai no transakcijas.</span><span class="sxs-lookup"><span data-stu-id="e3531-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="e3531-206">Tā var notikt, jo transakcijas sadales laikā tiek sasniegts ierobežojums.</span><span class="sxs-lookup"><span data-stu-id="e3531-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="e3531-207">Šajā gadījumā saskaņā ar šo nosacījumu tiek sadalīta tikai noteikta summa, piemēram, 50 procenti katram finansējuma avotam.</span><span class="sxs-lookup"><span data-stu-id="e3531-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="e3531-208">Tā notiek 1. nosacījumā, kas šajā sadaļā tika aprakstīts iepriekš.</span><span class="sxs-lookup"><span data-stu-id="e3531-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="e3531-209">Atlikums tiek sadalīts saskaņā ar nākamo piemērojamo nosacījumu attiecīgajā secībā.</span><span class="sxs-lookup"><span data-stu-id="e3531-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="e3531-210">Nākamajā tabulā šis scenārijs ir izpētīts detalizētāk.</span><span class="sxs-lookup"><span data-stu-id="e3531-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e3531-211"><strong>Fokuss </strong></span><span class="sxs-lookup"><span data-stu-id="e3531-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="e3531-212"><strong>Detalizēta informācija</strong></span><span class="sxs-lookup"><span data-stu-id="e3531-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3531-213">Finansējuma nosacījumi</span><span class="sxs-lookup"><span data-stu-id="e3531-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="e3531-214">1. nosacījums (1. prioritāte): Visas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="e3531-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="e3531-215">Piešķirt 2. finansējuma avotam 50% un 3. finansējuma avotam 50%.</span><span class="sxs-lookup"><span data-stu-id="e3531-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="e3531-216">2. nosacījums (2. prioritāte): Visas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="e3531-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="e3531-217">Piešķirt 3. finansējuma avotam 100%.</span><span class="sxs-lookup"><span data-stu-id="e3531-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="e3531-218">3. nosacījums (2. prioritāte): Visas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="e3531-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="e3531-219">Piešķirt 1. finansējuma avotam 100%.</span><span class="sxs-lookup"><span data-stu-id="e3531-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3531-220">Finansējuma ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="e3531-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="e3531-221">1. finansējuma avota ierobežojums = 10 000,00</span><span class="sxs-lookup"><span data-stu-id="e3531-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="e3531-222">2. finansējuma avota ierobežojums = 500,00</span><span class="sxs-lookup"><span data-stu-id="e3531-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="e3531-223">3. finansējuma avota ierobežojums = 750,00</span><span class="sxs-lookup"><span data-stu-id="e3531-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3531-224">1. transakcija</span><span class="sxs-lookup"><span data-stu-id="e3531-224">Transaction 1</span></span></td>
<td><span data-ttu-id="e3531-225"><strong>Transakcijas summa:</strong> 100,00<strong>Finansējums:</strong> transakcija tiek apmaksāta tikai saskaņā ar 1. nosacījumu, jo pēc 1. nosacījuma piemērošanas transakcija ir apmaksāta pilnībā.</span><span class="sxs-lookup"><span data-stu-id="e3531-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="e3531-226">Transakcijas finansēšana tiek vienādi sadalīta starp 2. finansējuma avotu un 3. finansējuma avotu.</span><span class="sxs-lookup"><span data-stu-id="e3531-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="e3531-227">2. finansējuma avots: 50,00</span><span class="sxs-lookup"><span data-stu-id="e3531-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="e3531-228">3. finansējuma avots: 50,00</span><span class="sxs-lookup"><span data-stu-id="e3531-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3531-229">2. transakcija</span><span class="sxs-lookup"><span data-stu-id="e3531-229">Transaction 2</span></span></td>
<td><span data-ttu-id="e3531-230"><strong>Transakcijas summa:</strong> 5000,00<strong>Finansējums:</strong> transakcija tiek apmaksāta saskaņā ar visiem trim nosacījumiem.<strong>1. nosacījums</strong>
</span><span class="sxs-lookup"><span data-stu-id="e3531-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.<strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="e3531-231">2. finansējuma avots: 450,00</span><span class="sxs-lookup"><span data-stu-id="e3531-231">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="e3531-232">3. finansējuma avots: 450,00</span><span class="sxs-lookup"><span data-stu-id="e3531-232">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="e3531-233">
<strong>2. nosacījums</strong>
</span><span class="sxs-lookup"><span data-stu-id="e3531-233">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="e3531-234">3. finansējuma avots: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="e3531-234">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="e3531-235">
<strong>3. nosacījums</strong>
</span><span class="sxs-lookup"><span data-stu-id="e3531-235">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="e3531-236">1. finansējuma avots: 3850,00 (= 5000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="e3531-236">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3531-237">Kopējie līdzekļi, kas tiek sadalīti katram finansējuma avotam</span><span class="sxs-lookup"><span data-stu-id="e3531-237">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="e3531-238">1. finansējuma avots: 3850,00</span><span class="sxs-lookup"><span data-stu-id="e3531-238">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="e3531-239">2. finansējuma avots: 500,00</span><span class="sxs-lookup"><span data-stu-id="e3531-239">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="e3531-240">3. finansējuma avots: 750,00</span><span class="sxs-lookup"><span data-stu-id="e3531-240">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="e3531-241">Norēķinu noteikumi</span><span class="sxs-lookup"><span data-stu-id="e3531-241">Billing rules</span></span>
<span data-ttu-id="e3531-242">Veicot pārrunas ar debitoru par projekta līgumu, jums jānorāda, kā un kad jūs varat debitoram izrakstīt rēķinu par darbu pie projekta.</span><span class="sxs-lookup"><span data-stu-id="e3531-242">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="e3531-243">Kad esat iestatījis projekta līgumu un projektu, varat projektam iestatīt norēķinu kārtulas.</span><span class="sxs-lookup"><span data-stu-id="e3531-243">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="e3531-244">Norēķinu kārtulu pamatā ir projekta nosacījumi, kas norādīti projekta līgumā.</span><span class="sxs-lookup"><span data-stu-id="e3531-244">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="e3531-245">Norēķinu kārtulas, ko varat izveidot, ir atkarīgas no projekta līguma nosacījumiem un projekta veida, piemēram, laika un materiālu vai fiksētas cenas projekta, ko saistāt ar norēķinu kārtulu.</span><span class="sxs-lookup"><span data-stu-id="e3531-245">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="e3531-246">Varat izveidot vairāk nekā vienu norēķinu kārtulu projekta līgumam.</span><span class="sxs-lookup"><span data-stu-id="e3531-246">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="e3531-247">Norēķinu kārtulu varat piešķirt arī vairākiem projektiem, kas ir saistīti ar vienu projekta līgumu un kuriem ir līdzīgi norēķinu nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="e3531-247">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="e3531-248">Varat iestatīt tālāk norādīto veidu norēķinu kārtulas.</span><span class="sxs-lookup"><span data-stu-id="e3531-248">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="e3531-249">**Piegādes vienība** — rēķins debitoram tiek izrakstīts pēc piegādes vienības pabeigšanas.</span><span class="sxs-lookup"><span data-stu-id="e3531-249">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="e3531-250">Piegādes vienības tiek definētas līgumā.</span><span class="sxs-lookup"><span data-stu-id="e3531-250">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="e3531-251">**Norise** — rēķins debitoram tiek izrakstīts, kad ir pabeigta noteikta procentuālā daļa no projekta.</span><span class="sxs-lookup"><span data-stu-id="e3531-251">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="e3531-252">Varat iestatīt norēķinu kārtulas, lai automātiski aprēķinātu pabeigtā darba procentuālo daļu, vai arī varat manuāli aprēķināt pabeigtā darba procentuālo daļu un debitora rēķina summu.</span><span class="sxs-lookup"><span data-stu-id="e3531-252">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="e3531-253">**Atskaites punkts** — rēķins debitoram tiek izrakstīts par pilnu projekta atskaites punkta summu, kad ir sasniegts šis atskaites punkts.</span><span class="sxs-lookup"><span data-stu-id="e3531-253">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="e3531-254">**Papildmaksa** — rēķins debitoram tiek izrakstīts par jūsu pakalpojumiem, kā arī par pārvaldības maksu, kas parasti ir procentuāls daudzums no pakalpojumu izmaksām.</span><span class="sxs-lookup"><span data-stu-id="e3531-254">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="e3531-255">**Laiks un materiāli** — rēķins debitoram tiek izrakstīts par projektam patērēto laiku un materiāliem.</span><span class="sxs-lookup"><span data-stu-id="e3531-255">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="e3531-256">Visu veidu norēķinu kārtulām varat norādīt ieturamo procentuālo daļu, kas tiek atņemta no debitora rēķiniem, līdz projekts sasniedz iepriekš noteikto stadiju.</span><span class="sxs-lookup"><span data-stu-id="e3531-256">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="e3531-257">Maksājumu ieturējuma procentuālā daļa ir norādīta projekta līgumā.</span><span class="sxs-lookup"><span data-stu-id="e3531-257">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="e3531-258">Summa tiek aprēķināta, pamatojoties uz debitora rēķina rindu kopējās vērtības, un atņemta no tās.</span><span class="sxs-lookup"><span data-stu-id="e3531-258">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="e3531-259">Norēķinu kārtulām **Laiks un materiāli** un **Norise** varat piešķirt rēķinā iekļaujamas kategorijas.</span><span class="sxs-lookup"><span data-stu-id="e3531-259">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="e3531-260">Rēķinā iekļaujamās kategorijas norāda transakcijas, kas būtu jāiekļauj debitoru rēķinos.</span><span class="sxs-lookup"><span data-stu-id="e3531-260">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="e3531-261">Kad esat gatavs izrakstīt debitoram rēķinu, projekta rēķinā iekļaujamā summa tiek aprēķināta, pamatojoties uz norēķinu kārtulām, un tiek izveidots projekta rēķina priekšlikums.</span><span class="sxs-lookup"><span data-stu-id="e3531-261">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="e3531-262">Nākamajās sadaļās ir sniegti piemēri, kuros parādīts, kā iestatīt un pārvaldīt projekta norēķinu kārtulas.</span><span class="sxs-lookup"><span data-stu-id="e3531-262">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="e3531-263">Piemērs. Uz piegādāto vienību skaitu balstītas norēķinu kārtulas izveide</span><span class="sxs-lookup"><span data-stu-id="e3531-263">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="e3531-264">Jūsu organizācijai noslēdz līgumu par kopā piecu apmācību sesiju nodrošināšanu debitora darbiniekiem un katras apmācības sesijas maksu 10 000.</span><span class="sxs-lookup"><span data-stu-id="e3531-264">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="e3531-265">Pēc katras apmācību sesijas jūs izrakstāt debitoram rēķinu.</span><span class="sxs-lookup"><span data-stu-id="e3531-265">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="e3531-266">Kad iestatāt norēķinu kārtulas šim līgumam, jūs izmantojat tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="e3531-266">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="e3531-267">Piegādes vienība ir viena apmācību sesija.</span><span class="sxs-lookup"><span data-stu-id="e3531-267">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="e3531-268">Vienības cena ir 10 000 par vienu apmācības sesiju.</span><span class="sxs-lookup"><span data-stu-id="e3531-268">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="e3531-269">Kopējais vienību skaits ir piecas apmācības sesijas.</span><span class="sxs-lookup"><span data-stu-id="e3531-269">The total number of units is five training sessions.</span></span>

<span data-ttu-id="e3531-270">Kad esat pabeidzis vienu apmācības sesiju, varat izveidot rēķinu 10 000 apmērā par pirmo vienību, kas ir piegādāta, un nosūtīt šo rēķinu debitoram.</span><span class="sxs-lookup"><span data-stu-id="e3531-270">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="e3531-271">Piemērs. Uz noteiktu projekta pabeigtības procentuālo daļu balstītas norēķinu kārtulas izveide (manuāls aprēķins)</span><span class="sxs-lookup"><span data-stu-id="e3531-271">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="e3531-272">Jūsu organizācija, programmatūras konsultāciju uzņēmums, noslēdz līgumu ar klientu par izstrādes procesā esoša klienta produkta daļas izstrādāšanu.</span><span class="sxs-lookup"><span data-stu-id="e3531-272">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="e3531-273">Jūsu organizācija apņemas piegādāt programmatūras kodu sešu mēnešu periodā.</span><span class="sxs-lookup"><span data-stu-id="e3531-273">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="e3531-274">Klients piekrīt maksāt jūsu organizācijai par darbu kopumā 100 000.</span><span class="sxs-lookup"><span data-stu-id="e3531-274">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="e3531-275">Jūs izveidojat norēķinu kārtulu, lai izrakstītu rēķinu debitoram, pamatojoties uz projekta ietvaros pabeigtā darba procentuālo daļu, kā norādīts līgumā.</span><span class="sxs-lookup"><span data-stu-id="e3531-275">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="e3531-276">Pirmā mēneša beigās jūs tiekaties ar klientu, lai noteiktu pabeigtā darba procentuālo daļu.</span><span class="sxs-lookup"><span data-stu-id="e3531-276">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="e3531-277">Pēc projekta pārskatīšanas jūs un debitors izlemjat, ka projekta pabeigtības līmenis ir 15 procenti.</span><span class="sxs-lookup"><span data-stu-id="e3531-277">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="e3531-278">Jūs izveidojat rēķinu par 15 000 (15 procenti no 100 000) un nosūtāt to debitoram.</span><span class="sxs-lookup"><span data-stu-id="e3531-278">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="e3531-279">Piemērs. Uz noteiktu projekta pabeigtības procentuālo daļu balstītas norēķinu kārtulas izveide (automātisks aprēķins)</span><span class="sxs-lookup"><span data-stu-id="e3531-279">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="e3531-280">Jūsu organizācija, programmatūras izstrādes firma, piekrīt debitoram izstrādāt algu uzskaites pakotni par 30 000.</span><span class="sxs-lookup"><span data-stu-id="e3531-280">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="e3531-281">Klients piekrīt maksāt jūsu organizācijai, pamatojoties uz pabeigtā darba procentuālo daļu.</span><span class="sxs-lookup"><span data-stu-id="e3531-281">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="e3531-282">Jūs novērtējat, ka projekta izmaksas ir 20 000.</span><span class="sxs-lookup"><span data-stu-id="e3531-282">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="e3531-283">Projekta līgumā ir norādītas darba kategorijas, ko jūs izmantojat norēķinu procesā.</span><span class="sxs-lookup"><span data-stu-id="e3531-283">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="e3531-284">Iestatiet norēķinu nosacījumus, kas automātiski aprēķina rēķina summas procentuālajam daudzumam darba, kas ir pabeigts katrai kategorijai.</span><span class="sxs-lookup"><span data-stu-id="e3531-284">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="e3531-285">Katrai kategorijai jāiestata budžets.</span><span class="sxs-lookup"><span data-stu-id="e3531-285">You set up a budget for each category:</span></span>

-   <span data-ttu-id="e3531-286">**Izstrāde** — izmaksas 15 000 un ieņēmumi 20 000</span><span class="sxs-lookup"><span data-stu-id="e3531-286">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="e3531-287">**Uzstādīšana** — izmaksas 5000 un ieņēmumi 10 000</span><span class="sxs-lookup"><span data-stu-id="e3531-287">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="e3531-288">Pirmo reizi izveidojot debitora rēķinu, rēķina summa tiek automātiski aprēķināta, pamatojoties uz tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="e3531-288">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="e3531-289">Pēc mēneša projekta darbinieks iesniedz projekta darba laika uzskaites tabulu.</span><span class="sxs-lookup"><span data-stu-id="e3531-289">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="e3531-290">Darbinieka darba stundu izmaksas ir 5000 par izstrādi un 1000 par uzstādīšanu.</span><span class="sxs-lookup"><span data-stu-id="e3531-290">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="e3531-291">Izstrādes darba pabeigtība ir 33 procenti (5000 faktiskās izmaksas/15 000 budžeta izmaksas), un uzstādīšanas darba pabeigtība ir 20 procenti (1000 faktiskās izmaksas/5000 budžeta izmaksas).</span><span class="sxs-lookup"><span data-stu-id="e3531-291">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="e3531-292">Rēķina summa 8667 tiek aprēķināta automātiski (33 procenti no 20 000 + 20 procenti no 10 000).</span><span class="sxs-lookup"><span data-stu-id="e3531-292">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="e3531-293">Jūs izveidojat rēķinu par 8667 un nosūtāt to debitoram.</span><span class="sxs-lookup"><span data-stu-id="e3531-293">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="e3531-294">Piemērs. Uz saskaņotiem atskaites punktiem balstītas norēķinu kārtulas izveide</span><span class="sxs-lookup"><span data-stu-id="e3531-294">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="e3531-295">Jūsu organizācija, vadības konsultāciju uzņēmums, piekrīt veikt tirgus izpēti par patēriņa preci, ko debitors plāno pārdot.</span><span class="sxs-lookup"><span data-stu-id="e3531-295">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="e3531-296">Klients piekrīt izmantot jūsu pakalpojumus trīs mēnešus — sākot no marta — un piekrīt maksāt jūsu organizācijai 50 000.</span><span class="sxs-lookup"><span data-stu-id="e3531-296">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="e3531-297">Projektam ir trīs atskaites punkti:</span><span class="sxs-lookup"><span data-stu-id="e3531-297">The project has three milestones:</span></span>

-   <span data-ttu-id="e3531-298">1. atskaites punkts: patērētāju datu apkopošana — 31. marts</span><span class="sxs-lookup"><span data-stu-id="e3531-298">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="e3531-299">2. atskaites punkts: patēriņa datu analīze — 30. aprīlis</span><span class="sxs-lookup"><span data-stu-id="e3531-299">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="e3531-300">3. atskaites punkts: priekšlikuma iesniegšana par preču dzīvotspēju — 31. maijs</span><span class="sxs-lookup"><span data-stu-id="e3531-300">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="e3531-301">Debitors piekrīt maksāt jūsu organizācijai 10 000 par pirmo atskaites punktu, 20 000 par otro atskaites punktu, un 20 000 par trešo atskaites punktu.</span><span class="sxs-lookup"><span data-stu-id="e3531-301">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="e3531-302">Kad iestatāt projekta līgumu, jūs piekrītat debitoram izrakstīt rēķinu, pamatojoties uz izpildīto atskaites punktu.</span><span class="sxs-lookup"><span data-stu-id="e3531-302">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="e3531-303">Norēķinu kārtulas iestatīšanā ietvertas tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e3531-303">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="e3531-304">Definējiet projekta atskaites punktus.</span><span class="sxs-lookup"><span data-stu-id="e3531-304">Define the project milestones.</span></span>
-   <span data-ttu-id="e3531-305">Nosakiet debitora rēķinā iekļaujamo summu, kad tiek pabeigts katrs atskaites punkts.</span><span class="sxs-lookup"><span data-stu-id="e3531-305">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="e3531-306">Kad 31. martā tiek pabeigts pirmais atskaites punkts, jūs atzīmējat šo atskaites punktu kā pabeigtu, un pēc tam izveidojat rēķinu par 10 000 un nosūtāt to debitoram.</span><span class="sxs-lookup"><span data-stu-id="e3531-306">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="e3531-307">Rēķinu par atskaites punktu nevar izveidot, kamēr šo atskaites punktu neesat atzīmējis kā pabeigtu.</span><span class="sxs-lookup"><span data-stu-id="e3531-307">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="e3531-308">Piemērs. Uz pakalpojumiem un pārvaldības maksu pamatotas norēķinu kārtulas izveide</span><span class="sxs-lookup"><span data-stu-id="e3531-308">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="e3531-309">Jūsu organizācija, vadības konsultāciju firma, piekrīt veikt tirgus izpēti, lai novērtētu dzīvotspēju kādam produktam, ko izstrādā debitors — kāds mazumtirdzniecības uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="e3531-309">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="e3531-310">Līguma nosacījumos ir norādīts, ka jūs nodrošināsiet trīs labāko vadības konsultantu pakalpojumus, kuri veikts izpēti, pamatojoties uz patērēto laiku un materiāliem.</span><span class="sxs-lookup"><span data-stu-id="e3531-310">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="e3531-311">Debitors piekrīt maksāt summu 100/stundā, kā arī pārvaldības maksu 10 procentu apmērā par konsultāciju stundām, kuras tiek apmaksātas projekta ietvaros.</span><span class="sxs-lookup"><span data-stu-id="e3531-311">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="e3531-312">Iestatot projekta līgumu, izveidojiet norēķinu kārtulu, kas pievieno 10 procentu pārvaldības maksu konsultāciju stundām, kuras tiek apmaksātas projekta ietvaros.</span><span class="sxs-lookup"><span data-stu-id="e3531-312">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="e3531-313">Izveidojot rēķinu klientam, tajā iekļauta 10 procentu pārvaldības maksa, kā arī konsultāciju stundu izmaksas.</span><span class="sxs-lookup"><span data-stu-id="e3531-313">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="e3531-314">Piemēram, ja trīs konsultanti projekta ietvaros kopā ir strādājuši 200 stundas, rēķins par summu 22 000 tiek izveidots, pamatojoties uz tālāk norādīto aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="e3531-314">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="e3531-315">200 stundas par likmi 100 stundā = 20 000</span><span class="sxs-lookup"><span data-stu-id="e3531-315">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="e3531-316">10 procentu pārvaldības maksa = 2000</span><span class="sxs-lookup"><span data-stu-id="e3531-316">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="e3531-317">Rēķina kopsumma = 22 000</span><span class="sxs-lookup"><span data-stu-id="e3531-317">Total invoice amount = 22,000</span></span>

<span data-ttu-id="e3531-318">Ja klientam piemērojamās maksas ir ar apliekamas ar nodokli un projekta līgumā tiek atlasīta PVN grupa, maksu norēķinu kārtulā tiek automātiski ievadīta PVN grupa.</span><span class="sxs-lookup"><span data-stu-id="e3531-318">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="e3531-319">Piemērs. Norēķinu kārtulas izveidošana par patērēto laiku un izmantotajiem materiāliem</span><span class="sxs-lookup"><span data-stu-id="e3531-319">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="e3531-320">Jūsu organizācija, programmatūras konsultāciju uzņēmums, piekrīt nodrošināt piecus tehniskos konsultantus, kas nākamo sešu mēnešu laikā debitoram strādās pie programmatūras izstrādes projekta.</span><span class="sxs-lookup"><span data-stu-id="e3531-320">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="e3531-321">Debitors piekrīt maksāt summu 150 par katru konsultācijas stundu, kā arī segt kancelejas piederumu izmaksas.</span><span class="sxs-lookup"><span data-stu-id="e3531-321">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="e3531-322">Jūsu organizācija nosūta rēķinu klientam katra mēneša beigās.</span><span class="sxs-lookup"><span data-stu-id="e3531-322">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="e3531-323">Kad iestatāt projekta līgumu, jūs piekrītat debitoram katru mēnesi izrakstīt rēķinu par projektā patērēto laiku un izmantotajiem materiāliem.</span><span class="sxs-lookup"><span data-stu-id="e3531-323">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="e3531-324">Jāizveido norēķinu kārtula ar tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="e3531-324">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="e3531-325">Līguma periods ir seši mēneši.</span><span class="sxs-lookup"><span data-stu-id="e3531-325">The contract period is six months.</span></span>
-   <span data-ttu-id="e3531-326">Konsultāciju laiks tiek aprēķināts atbilstoši likmei 150/stundā.</span><span class="sxs-lookup"><span data-stu-id="e3531-326">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="e3531-327">Kancelejas preču izmaksas tiek iekļautas rēķinā, un projekta kopējās izmaksas nedrīkst pārsniegt 10 000.</span><span class="sxs-lookup"><span data-stu-id="e3531-327">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="e3531-328">Debitora rēķins projekta laikā tiek izveidots katra kalendārā mēneša beigās.</span><span class="sxs-lookup"><span data-stu-id="e3531-328">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="e3531-329">Pirmajā mēnesī projekta konsultanti ieraksta kopumā 800 stundas.</span><span class="sxs-lookup"><span data-stu-id="e3531-329">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="e3531-330">Kancelejas preču izmaksas, kuras tiek iekļautas projekta rēķinā, ir 2000.</span><span class="sxs-lookup"><span data-stu-id="e3531-330">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="e3531-331">Līdz ar to mēneša beigās jūs izveidojat rēķinu par summu 122 000, kura tiek aprēķināta kā 800 stundas par likmi 150/stundā, kā arī 2000 par kancelejas precēm.</span><span class="sxs-lookup"><span data-stu-id="e3531-331">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>




