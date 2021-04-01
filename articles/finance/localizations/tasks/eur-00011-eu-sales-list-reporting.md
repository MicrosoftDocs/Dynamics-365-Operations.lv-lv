---
title: EUR-00011 Iestatīt ES pārdošanas saraksta atskaišu veidošanu
description: Šajā uzdevumā tiek sniegts pārskats par priekšnosacījumiem, kas nepieciešami ES pārdošanas saraksta pārskatam.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, SysQueryForm, SysQueryFieldLookUp,  TaxTable, TaxGroup, TaxItemGroup, TaxCountryRegionParameters, TaxVATNumTable, IntrastatParameters, CustTable, DirPartyQuickCreateForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0ce458697fd61aabddcbf844dd0b2afbe3aa1c0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228013"
---
# <a name="eur-00011-set-up-eu-sales-list-reporting"></a><span data-ttu-id="ae38d-103">EUR-00011 Iestatīt ES pārdošanas saraksta atskaišu veidošanu</span><span class="sxs-lookup"><span data-stu-id="ae38d-103">EUR-00011 Set up EU sales list reporting</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ae38d-104">Šajā uzdevumā tiek sniegts pārskats par priekšnosacījumiem, kas nepieciešami ES pārdošanas saraksta pārskatam.</span><span class="sxs-lookup"><span data-stu-id="ae38d-104">This task walks you through an overview of the prerequisites required for EU sales list reporting.</span></span> <span data-ttu-id="ae38d-105">Lai iegūtu plašāku informāciju par ES pārdošanas saraksta pārskatu, tai skaitā nepieciešamajiem priekšnoteikumiem, skatiet sadaļu Palīdzība.</span><span class="sxs-lookup"><span data-stu-id="ae38d-105">For more information about EU Sales list reporting, including required prerequisites, refer to Help.</span></span>

<span data-ttu-id="ae38d-106">Šis uzdevums attiecas uz visām Eiropas valstīm/reģioniem.</span><span class="sxs-lookup"><span data-stu-id="ae38d-106">This task applies to all European countries/regions.</span></span> <span data-ttu-id="ae38d-107">Šis ceļvedis tika izveidots, izmantojot demonstrācijas datu uzņēmumu DEMF un tādējādi Vācijā tiek izmantota kā iekšzemes valsts/reģiona piemērs.</span><span class="sxs-lookup"><span data-stu-id="ae38d-107">The guide was created using the demo data company DEMF and consequently Germany as an exemplar domestic country/region.</span></span> <span data-ttu-id="ae38d-108">Šajā ceļvedī kā iekšzemes valsts/reģiona piemērs tiek izmantota arī Portugāle.</span><span class="sxs-lookup"><span data-stu-id="ae38d-108">The guide also uses Portugal as an exemplar EU country/region.</span></span>

<span data-ttu-id="ae38d-109">Šie uzdevumi ir paredzēti sistēmas administratoriem.</span><span class="sxs-lookup"><span data-stu-id="ae38d-109">These tasks are intended for system administrators.</span></span>


## <a name="import-electronic-reporting-configurations-for-eu-sales-list-reporting"></a><span data-ttu-id="ae38d-110">Elektroniskā pārskata konfigurāciju importēšana ES pārdošanas saraksta pārskatos</span><span class="sxs-lookup"><span data-stu-id="ae38d-110">Import electronic reporting configurations for EU sales list reporting</span></span>
1. <span data-ttu-id="ae38d-111">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="ae38d-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="ae38d-112">Noklikšķiniet uz Iestatīt aktīvu.</span><span class="sxs-lookup"><span data-stu-id="ae38d-112">Click Set active.</span></span>
3. <span data-ttu-id="ae38d-113">Noklikšķiniet uz Repozitoriji.</span><span class="sxs-lookup"><span data-stu-id="ae38d-113">Click Repositories.</span></span>
4. <span data-ttu-id="ae38d-114">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="ae38d-114">Click Open.</span></span>
5. <span data-ttu-id="ae38d-115">Darbību rūtī noklikšķiniet uz Opcijas.</span><span class="sxs-lookup"><span data-stu-id="ae38d-115">On the Action Pane, click Options.</span></span>
6. <span data-ttu-id="ae38d-116">Noklikšķiniet uz Detalizēts filtrs/kārtošana.</span><span class="sxs-lookup"><span data-stu-id="ae38d-116">Click Advanced Filter/Sort.</span></span>
7. <span data-ttu-id="ae38d-117">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="ae38d-117">Click Add.</span></span>
8. <span data-ttu-id="ae38d-118">Laukā Lauks atlasiet "Konfigurācijas nosaukums".</span><span class="sxs-lookup"><span data-stu-id="ae38d-118">In the Field field, select 'Configuration name'.</span></span>
9. <span data-ttu-id="ae38d-119">Laukā Kritēriji ierakstiet "ES pārdošanas saraksts (DE)".</span><span class="sxs-lookup"><span data-stu-id="ae38d-119">In the Criteria field, type 'EU Sales list (DE)'.</span></span>
10. <span data-ttu-id="ae38d-120">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ae38d-120">Click OK.</span></span>
11. <span data-ttu-id="ae38d-121">Noklikšķiniet uz Importēt.</span><span class="sxs-lookup"><span data-stu-id="ae38d-121">Click Import.</span></span>
12. <span data-ttu-id="ae38d-122">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="ae38d-122">Click Yes.</span></span>
13. <span data-ttu-id="ae38d-123">Darbību rūtī noklikšķiniet uz Opcijas.</span><span class="sxs-lookup"><span data-stu-id="ae38d-123">On the Action Pane, click Options.</span></span>
14. <span data-ttu-id="ae38d-124">Noklikšķiniet uz Detalizēts filtrs/kārtošana.</span><span class="sxs-lookup"><span data-stu-id="ae38d-124">Click Advanced Filter/Sort.</span></span>
15. <span data-ttu-id="ae38d-125">Noklikšķiniet uz Atiestatīt.</span><span class="sxs-lookup"><span data-stu-id="ae38d-125">Click Reset.</span></span>
16. <span data-ttu-id="ae38d-126">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="ae38d-126">Click Add.</span></span>
17. <span data-ttu-id="ae38d-127">Laukā Lauks atlasiet "Konfigurācijas nosaukums".</span><span class="sxs-lookup"><span data-stu-id="ae38d-127">In the Field field, select 'Configuration name'.</span></span>
18. <span data-ttu-id="ae38d-128">Laukā Kritēriji ierakstiet "Pārskats par ES pārdošanas sarakstu pa rindām".</span><span class="sxs-lookup"><span data-stu-id="ae38d-128">In the Criteria field, type 'EU Sales list by rows report'.</span></span>
19. <span data-ttu-id="ae38d-129">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ae38d-129">Click OK.</span></span>
20. <span data-ttu-id="ae38d-130">Noklikšķiniet uz Importēt.</span><span class="sxs-lookup"><span data-stu-id="ae38d-130">Click Import.</span></span>
21. <span data-ttu-id="ae38d-131">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="ae38d-131">Click Yes.</span></span>

## <a name="set-up-sales-tax-codes-for-eu-sales-list-reporting"></a><span data-ttu-id="ae38d-132">PVN kodu iestatīšana ES pārdošanas saraksta pārskatiem</span><span class="sxs-lookup"><span data-stu-id="ae38d-132">Set up sales tax codes for EU sales list reporting</span></span>
1. <span data-ttu-id="ae38d-133">Pārejiet uz sadaļu Nodokļi > Netiešie nodokļi > PVN > PVN kodi.</span><span class="sxs-lookup"><span data-stu-id="ae38d-133">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="ae38d-134">Izmantojiet ātro filtru, lai filtrētu pēc lauka PVN kods, izmantojot vērtību “VAT19”.</span><span class="sxs-lookup"><span data-stu-id="ae38d-134">Use the Quick Filter to filter on the Sales tax code field with a value of 'VAT19'.</span></span>
3. <span data-ttu-id="ae38d-135">Izvērsiet sadaļu Pārskata iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="ae38d-135">Expand the Report setup section.</span></span>
    * <span data-ttu-id="ae38d-136">Pārbaudiet, vai opcija Nav iekļauts ir iestatīta uz Nē.</span><span class="sxs-lookup"><span data-stu-id="ae38d-136">Verify that the Excluded selection is set to No.</span></span>  
    * <span data-ttu-id="ae38d-137">Jums var būt nepieciešams atbloķēt šo uzdevumu ceļvedi, lai mainītu šo iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="ae38d-137">You may need to unlock the task guide to change this setting.</span></span>  

## <a name="set-up-sales-tax-groups-for-eu-sales-list-reporting"></a><span data-ttu-id="ae38d-138">PVN grupu iestatīšana ES pārdošanas saraksta pārskatiem</span><span class="sxs-lookup"><span data-stu-id="ae38d-138">Set up sales tax groups for EU sales list reporting</span></span>
1. <span data-ttu-id="ae38d-139">Dodieties uz Nodokļi > Netiešie nodokļi > Pārdošanas nodoklis > Pārdošanas nodokļa grupas.</span><span class="sxs-lookup"><span data-stu-id="ae38d-139">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="ae38d-140">Izmantojiet ātro filtru, lai filtrētu pēc lauka PVN grupa, izmantojot vērtību “AR-DOM”.</span><span class="sxs-lookup"><span data-stu-id="ae38d-140">Use the Quick Filter to filter on the Sales tax group field with a value of 'AR-DOM'.</span></span>
3. <span data-ttu-id="ae38d-141">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="ae38d-141">Click Edit.</span></span>
4. <span data-ttu-id="ae38d-142">Izvērsiet sadaļu Iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="ae38d-142">Expand the Setup section.</span></span>
5. <span data-ttu-id="ae38d-143">Sarakstā atlasiet pirmo rindu.</span><span class="sxs-lookup"><span data-stu-id="ae38d-143">In the list, select the first row.</span></span>
6. <span data-ttu-id="ae38d-144">Atzīmējiet izvēles rūtiņu Neapliekams.</span><span class="sxs-lookup"><span data-stu-id="ae38d-144">Select the Exempt check box.</span></span>
7. <span data-ttu-id="ae38d-145">Sarakstā atlasiet otro rindu.</span><span class="sxs-lookup"><span data-stu-id="ae38d-145">In the list, select the second row.</span></span>
8. <span data-ttu-id="ae38d-146">Atzīmējiet izvēles rūtiņu Neapliekams.</span><span class="sxs-lookup"><span data-stu-id="ae38d-146">Select the Exempt check box.</span></span>
9. <span data-ttu-id="ae38d-147">Sarakstā atlasiet trešo rindu.</span><span class="sxs-lookup"><span data-stu-id="ae38d-147">In the list, select the third row.</span></span>
10. <span data-ttu-id="ae38d-148">Atzīmējiet izvēles rūtiņu Neapliekams.</span><span class="sxs-lookup"><span data-stu-id="ae38d-148">Select the Exempt check box.</span></span>

## <a name="set-up-item-sales-tax-groups-for-eu-sales-list-reporting"></a><span data-ttu-id="ae38d-149">Krājumu PVN grupu iestatīšana ES pārdošanas saraksta pārskatiem</span><span class="sxs-lookup"><span data-stu-id="ae38d-149">Set up item sales tax groups for EU sales list reporting</span></span>
1. <span data-ttu-id="ae38d-150">Dodieties uz Nodokļi > Netiešie nodokļi > Pārdošanas nodoklis > Krājumu pārdošanas nodokļa grupas.</span><span class="sxs-lookup"><span data-stu-id="ae38d-150">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
2. <span data-ttu-id="ae38d-151">Izmantojiet ātro filtru, lai filtrētu pēc lauka Krājuma PVN grupa, izmantojot vērtību “PILNS”.</span><span class="sxs-lookup"><span data-stu-id="ae38d-151">Use the Quick Filter to filter on the Item sales tax group field with a value of 'FULL '.</span></span>
    * <span data-ttu-id="ae38d-152">Pārbaudiet, vai opcija Pārskata veids ir iestatīta uz "Krājums".</span><span class="sxs-lookup"><span data-stu-id="ae38d-152">Verify that the Reporting type selection is set to 'Item'.</span></span>  
    * <span data-ttu-id="ae38d-153">Jums var būt nepieciešams atbloķēt šo uzdevumu ceļvedi, lai mainītu vērtību šajā laukā.</span><span class="sxs-lookup"><span data-stu-id="ae38d-153">You may need to unlock the task guide to change the value in this field.</span></span>  
3. <span data-ttu-id="ae38d-154">Izmantojiet ātro filtru, lai filtrētu pēc lauka Krājuma PVN grupa, izmantojot vērtību “SARKANS”.</span><span class="sxs-lookup"><span data-stu-id="ae38d-154">Use the Quick Filter to filter on the Item sales tax group field with a value of 'RED '.</span></span>
    * <span data-ttu-id="ae38d-155">Pārbaudiet, vai opcija Pārskata veids ir iestatīta uz "Pakalpojums".</span><span class="sxs-lookup"><span data-stu-id="ae38d-155">Verify that the Reporting type selection is set to 'Service'.</span></span>  
    * <span data-ttu-id="ae38d-156">Jums var būt nepieciešams atbloķēt šo uzdevumu ceļvedi, lai mainītu vērtību šajā laukā.</span><span class="sxs-lookup"><span data-stu-id="ae38d-156">You may need to unlock the task guide to change the value in this field.</span></span>  

## <a name="set-up-countryregion-parameters-for-eu-sales-list-reporting"></a><span data-ttu-id="ae38d-157">Valsts/reģiona parametru iestatīšana ES pārdošanas saraksta pārskatiem</span><span class="sxs-lookup"><span data-stu-id="ae38d-157">Set up country/region parameters for EU sales list reporting</span></span>
1. <span data-ttu-id="ae38d-158">Dodieties uz Nodokļi > Iestatīšana > Pārdošanas nodoklis > Valsts/reģiona parametri.</span><span class="sxs-lookup"><span data-stu-id="ae38d-158">Go to Tax > Setup > Sales tax > Country/region parameters.</span></span>
2. <span data-ttu-id="ae38d-159">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="ae38d-159">Click New.</span></span>
3. <span data-ttu-id="ae38d-160">Laukā Valsts/reģions ierakstiet "PRT".</span><span class="sxs-lookup"><span data-stu-id="ae38d-160">In the Country/region field, type 'PRT'.</span></span>
4. <span data-ttu-id="ae38d-161">Laukā PVN ierakstiet "PT".</span><span class="sxs-lookup"><span data-stu-id="ae38d-161">In the Sales tax field, type 'PT'.</span></span>

## <a name="create-tax-exempt-numbers"></a><span data-ttu-id="ae38d-162">PVN reģistrācijas numuru izveide</span><span class="sxs-lookup"><span data-stu-id="ae38d-162">Create tax exempt numbers</span></span>
1. <span data-ttu-id="ae38d-163">Dodieties uz Nodokļi > Iestatīšana > Pārdošanas nodoklis > PVN reģ. numuri.</span><span class="sxs-lookup"><span data-stu-id="ae38d-163">Go to Tax > Setup > Sales tax > Tax exempt numbers.</span></span>
2. <span data-ttu-id="ae38d-164">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="ae38d-164">Click New.</span></span>
3. <span data-ttu-id="ae38d-165">Laukā Valsts/reģions ierakstiet "PRT".</span><span class="sxs-lookup"><span data-stu-id="ae38d-165">In the Country/region field, type 'PRT'.</span></span>
4. <span data-ttu-id="ae38d-166">Laukā PVN reģ. numurs ierakstiet “PT12345”.</span><span class="sxs-lookup"><span data-stu-id="ae38d-166">In the Tax exempt number field, type 'PT12345'.</span></span>

## <a name="set-up-eu-sales-list-reporting-parameters"></a><span data-ttu-id="ae38d-167">ES pārdošanas saraksta pārskatu parametru iestatīšana</span><span class="sxs-lookup"><span data-stu-id="ae38d-167">Set up EU sales list reporting parameters</span></span>
1. <span data-ttu-id="ae38d-168">Dodieties uz Nodokļi > Iestatīšana > Ārējā tirdzniecība > Ārējās tirdzniecības parametri.</span><span class="sxs-lookup"><span data-stu-id="ae38d-168">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="ae38d-169">Noklikšķiniet uz cilnes ES pārdošanas saraksts.</span><span class="sxs-lookup"><span data-stu-id="ae38d-169">Click the EU sales list tab.</span></span>
3. <span data-ttu-id="ae38d-170">Atlasiet Jā laukā Pārsūtīšanas pirkumi.</span><span class="sxs-lookup"><span data-stu-id="ae38d-170">Select Yes in the Transfer purchases field.</span></span>
4. <span data-ttu-id="ae38d-171">Izvērsiet sadaļu Noapaļošanas nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="ae38d-171">Expand the Rounding rules section.</span></span>
5. <span data-ttu-id="ae38d-172">Iestatiet Noapaļošanas nosacījumu uz "0,1".</span><span class="sxs-lookup"><span data-stu-id="ae38d-172">Set Rounding rule to '0.1'.</span></span>
6. <span data-ttu-id="ae38d-173">Laukā Lietot minimālo vērtību atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="ae38d-173">Select Yes in the Use minimum value field.</span></span>
7. <span data-ttu-id="ae38d-174">Laukā Decimālciparu skaits ievadiet "2".</span><span class="sxs-lookup"><span data-stu-id="ae38d-174">In the Number of decimals field, enter '2'.</span></span>
8. <span data-ttu-id="ae38d-175">Izvērsiet sadaļu Elektroniskie pārskati.</span><span class="sxs-lookup"><span data-stu-id="ae38d-175">Expand the Electronic reporting section.</span></span>
9. <span data-ttu-id="ae38d-176">Laukā Faila formāta kartēšana atlasiet "ES pārdošanas saraksts (DE)".</span><span class="sxs-lookup"><span data-stu-id="ae38d-176">In the File format mapping field, select 'EU Sales list (DE)'.</span></span>
10. <span data-ttu-id="ae38d-177">Laukā Pārskata formāta kartēšana atlasiet "Pārskats par ES pārdošanas sarakstu pa rindām".</span><span class="sxs-lookup"><span data-stu-id="ae38d-177">In the Report format mapping field, select 'EU Sales list by rows report'.</span></span>
11. <span data-ttu-id="ae38d-178">Noklikšķiniet uz cilnes Valsts/reģiona rekvizīti.</span><span class="sxs-lookup"><span data-stu-id="ae38d-178">Click the Country/region properties tab.</span></span>
    * <span data-ttu-id="ae38d-179">Pārbaudiet, vai lauks Valsts/reģiona tips valstij/reģionam DEU ir iestatīts uz "Iekšzemes".</span><span class="sxs-lookup"><span data-stu-id="ae38d-179">Verify that the Country/region type field is set to 'Domestic' for Country/region DEU.</span></span>  
    * <span data-ttu-id="ae38d-180">Jums var būt nepieciešams atbloķēt šo uzdevumu ceļvedi, lai mainītu vērtību šajā laukā.</span><span class="sxs-lookup"><span data-stu-id="ae38d-180">You may need to unlock the task guide to change the value in this field.</span></span>  
12. <span data-ttu-id="ae38d-181">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="ae38d-181">Click New.</span></span>
13. <span data-ttu-id="ae38d-182">Laukā Valsts/reģions ierakstiet "PRT".</span><span class="sxs-lookup"><span data-stu-id="ae38d-182">In the Country/region field, type 'PRT'.</span></span>
14. <span data-ttu-id="ae38d-183">Laukā Intrastat kods ierakstiet "PT".</span><span class="sxs-lookup"><span data-stu-id="ae38d-183">In the Intrastat code field, type 'PT'.</span></span>
15. <span data-ttu-id="ae38d-184">Laukā Valsts/reģiona tips atlasiet "ES".</span><span class="sxs-lookup"><span data-stu-id="ae38d-184">In the Country/region type field, select 'EU'.</span></span>
16. <span data-ttu-id="ae38d-185">Noklikšķiniet uz cilnes Numuru sērijas.</span><span class="sxs-lookup"><span data-stu-id="ae38d-185">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="ae38d-186">Pārbaudiet, vai Atsaucei "ES pārdošanas saraksts" ir norādīts Numuru sērijas kods.</span><span class="sxs-lookup"><span data-stu-id="ae38d-186">Verify that a Number sequence code is specified for the Reference 'EU sales list'.</span></span>  

## <a name="create-a-customer-for-eu-sales-list-reporting-demo-purposes"></a><span data-ttu-id="ae38d-187">Debitora izveide ES pārdošanas saraksta pārskatu demonstrācijas nolūkiem</span><span class="sxs-lookup"><span data-stu-id="ae38d-187">Create a customer for EU sales list reporting demo purposes</span></span>
1. <span data-ttu-id="ae38d-188">Pārejiet uz sadaļu Debitori > Debitori > Visi debitori.</span><span class="sxs-lookup"><span data-stu-id="ae38d-188">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="ae38d-189">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="ae38d-189">Click New.</span></span>
3. <span data-ttu-id="ae38d-190">Laukā Debitora konts ierakstiet "PRT-001".</span><span class="sxs-lookup"><span data-stu-id="ae38d-190">In the Customer account field, type 'PRT-001'.</span></span>
4. <span data-ttu-id="ae38d-191">Laukā Nosaukums ierakstiet "Debitors no Portugāles".</span><span class="sxs-lookup"><span data-stu-id="ae38d-191">In the Name field, type 'A customer from Portugal'.</span></span>
5. <span data-ttu-id="ae38d-192">Laukā Debitoru grupa atlasiet "10".</span><span class="sxs-lookup"><span data-stu-id="ae38d-192">In the Customer group field, select '10'.</span></span>
6. <span data-ttu-id="ae38d-193">Laukā PVN grupa atlasiet "AR-DOM".</span><span class="sxs-lookup"><span data-stu-id="ae38d-193">In the Sales tax group field, select 'AR-DOM'.</span></span>
7. <span data-ttu-id="ae38d-194">Laukā PVN reģ. numurs atlasiet “PT12345”.</span><span class="sxs-lookup"><span data-stu-id="ae38d-194">In the Tax exempt number field, select 'PT12345'.</span></span>
8. <span data-ttu-id="ae38d-195">Laukā Valsts/reģions ierakstiet "PRT".</span><span class="sxs-lookup"><span data-stu-id="ae38d-195">In the Country/region field, type 'PRT'.</span></span>
9. <span data-ttu-id="ae38d-196">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ae38d-196">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]