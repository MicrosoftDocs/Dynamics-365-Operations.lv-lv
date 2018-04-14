--- 
title: "ES Intrastat deklarācijas ģenerēšana"
description: "Šajā procedūrā ir aprakstīti soļi, kas nepieciešami, lai eksportētu Intrastat deklarāciju elektroniskā faila formātā un priekšskatītu deklarācijas datus Excel formātā."
author: Anasyash
manager: AnnBe
ms.date: 06/09/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: be094425de50e3919e97e9f2baf636c498768a47
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---
# <a name="generate-an-eu-intrastat-declaration"></a><span data-ttu-id="ef36c-103">ES Intrastat deklarācijas ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="ef36c-103">Generate an EU Intrastat declaration</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ef36c-104">Šajā procedūrā ir aprakstīti soļi, kas nepieciešami, lai eksportētu Intrastat deklarāciju elektroniskā faila formātā un priekšskatītu deklarācijas datus Excel formātā.</span><span class="sxs-lookup"><span data-stu-id="ef36c-104">This procedure walks you through the steps required to export the Intrastat declaration in the electronic file format and preview the declaration data in an Excel format.</span></span> 

<span data-ttu-id="ef36c-105">Lai varētu veikt šo procedūru, ir jāveic transakciju pārsūtīšana uz Intrastat.</span><span class="sxs-lookup"><span data-stu-id="ef36c-105">Before you can complete this procedure, you must transfer transactions to the Intrastat.</span></span> 

<span data-ttu-id="ef36c-106">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma DEMF dati.</span><span class="sxs-lookup"><span data-stu-id="ef36c-106">This procedure was created using the demo data company DEMF.</span></span>


## <a name="import-configurations-with-settings"></a><span data-ttu-id="ef36c-107">Importēt konfigurācijas ar iestatījumiem</span><span class="sxs-lookup"><span data-stu-id="ef36c-107">Import configurations with settings</span></span>
1. <span data-ttu-id="ef36c-108">Dodieties uz Darbvietas > Elektronisko atskaišu veidošana</span><span class="sxs-lookup"><span data-stu-id="ef36c-108">Go to Workspaces > Electronic reporting</span></span>
2. <span data-ttu-id="ef36c-109">Noklikšķiniet uz Iestatīt aktīvu.</span><span class="sxs-lookup"><span data-stu-id="ef36c-109">Click Set active.</span></span>
3. <span data-ttu-id="ef36c-110">Noklikšķiniet uz Repozitoriji.</span><span class="sxs-lookup"><span data-stu-id="ef36c-110">Click Repositories.</span></span>
4. <span data-ttu-id="ef36c-111">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="ef36c-111">Click Open.</span></span>
5. <span data-ttu-id="ef36c-112">Atveriet kolonnas Konfigurācijas nosaukums filtru.</span><span class="sxs-lookup"><span data-stu-id="ef36c-112">Open Configuration name column filter.</span></span>
6. <span data-ttu-id="ef36c-113">Lietojiet filtru laukam “Konfigurācijas nosaukums” ar vērtību “Intrastat (DE)”, izmantojot filtra operatoru “sākas ar”.</span><span class="sxs-lookup"><span data-stu-id="ef36c-113">Apply a filter on the "Configuration name" field, with a value of "Intrastat (DE)", using the "begins with" filter operator.</span></span>
    * <span data-ttu-id="ef36c-114">Atlasiet konfigurācijas nosaukumu, kas attiecas uz jūsu juridiskās personas valsti.</span><span class="sxs-lookup"><span data-stu-id="ef36c-114">You should select the configuration name applicable for the country of your legal entity.</span></span> <span data-ttu-id="ef36c-115">Šai procedūrai kā piemērs tiek izmantota Vācijas juridiskā persona (DEMF), līdz ar to ir jāizvēlas “Intrastat (DE)”.</span><span class="sxs-lookup"><span data-stu-id="ef36c-115">This procedure uses the German legal entity (DEMF) as an example, therefore "Intrastat (DE)" should be chosen.</span></span>  
    * <span data-ttu-id="ef36c-116">Noklikšķiniet uz Importēt un pēc tam uz Jā.</span><span class="sxs-lookup"><span data-stu-id="ef36c-116">Click Import and then click Yes.</span></span>  
7. <span data-ttu-id="ef36c-117">Atveriet kolonnas Konfigurācijas nosaukums filtru.</span><span class="sxs-lookup"><span data-stu-id="ef36c-117">Open Configuration name column filter.</span></span>
8. <span data-ttu-id="ef36c-118">Lietojiet filtru laukam “Konfigurācijas nosaukums” ar vērtību “Intrastat pārskats”, izmantojot filtra operatoru “sākas ar”.</span><span class="sxs-lookup"><span data-stu-id="ef36c-118">Apply a filter on the "Configuration name" field, with a value of "intrastat report", using the "begins with" filter operator.</span></span>
    * <span data-ttu-id="ef36c-119">Noklikšķiniet uz Importēt un pēc tam uz Jā.</span><span class="sxs-lookup"><span data-stu-id="ef36c-119">Click Import and then click Yes.</span></span>  

## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="ef36c-120">Iestatīt ārējās tirdzniecības parametrus</span><span class="sxs-lookup"><span data-stu-id="ef36c-120">Set up Foreign trade parameters</span></span>
1. <span data-ttu-id="ef36c-121">Dodieties uz Nodokļi > Iestatīšana > Ārējā tirdzniecība > Ārējās tirdzniecības parametri</span><span class="sxs-lookup"><span data-stu-id="ef36c-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters</span></span>
2. <span data-ttu-id="ef36c-122">Izvērsiet sadaļu Elektroniskie pārskati.</span><span class="sxs-lookup"><span data-stu-id="ef36c-122">Expand the Electronic reporting section.</span></span>
3. <span data-ttu-id="ef36c-123">Laukā Faila formāta kartēšana ievadiet vai atlasiet vērtību Intrastat (DE)</span><span class="sxs-lookup"><span data-stu-id="ef36c-123">In the File format mapping field, enter or select a value Intrastat (DE)</span></span>
4. <span data-ttu-id="ef36c-124">Laukā Pārskata formāta kartēšana ievadiet vai atlasiet vērtību Intrastat pārskats</span><span class="sxs-lookup"><span data-stu-id="ef36c-124">In the Report format mapping field, enter or select a value Intrastat report</span></span>
5. <span data-ttu-id="ef36c-125">Izvērsiet sadaļu Noapaļošanas nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="ef36c-125">Expand the Rounding rules section.</span></span>
    * <span data-ttu-id="ef36c-126">Jums ir jāiestata noapaļošanas nosacījumi, kas ir spēkā jūsu valstī/reģionā Intrastat pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="ef36c-126">You should set up rounding rules that are applicable in your country/region for Intrastat reporting.</span></span>  
6. <span data-ttu-id="ef36c-127">Ievadiet skaitli laukā Noapaļošanas nosacījums.</span><span class="sxs-lookup"><span data-stu-id="ef36c-127">In the Rounding rule field, enter a number.</span></span>
    * <span data-ttu-id="ef36c-128">Ievadiet noapaļošanas precizitāti, piemēram, ievadiet “0,01”.</span><span class="sxs-lookup"><span data-stu-id="ef36c-128">Enter rounding precision, for example, enter '0.01'.</span></span>  
7. <span data-ttu-id="ef36c-129">Ievadiet skaitli laukā Aiz komata esošo ciparu skaits summai.</span><span class="sxs-lookup"><span data-stu-id="ef36c-129">In the Number of decimals for amount field, enter a number.</span></span>
    * <span data-ttu-id="ef36c-130">Piemēram, ievadiet “2”.</span><span class="sxs-lookup"><span data-stu-id="ef36c-130">For example, enter '2'.</span></span>  
8. <span data-ttu-id="ef36c-131">Atlasiet opciju laukā Noapaļošana zem 1 kg.</span><span class="sxs-lookup"><span data-stu-id="ef36c-131">In the Rounding below 1 kg field, select an option.</span></span>
    * <span data-ttu-id="ef36c-132">Piemēram, atlasiet “Noapaļošana uz augšu līdz 1 kg”.</span><span class="sxs-lookup"><span data-stu-id="ef36c-132">For example, select 'Rounding up to 1 kg'.</span></span>  
9. <span data-ttu-id="ef36c-133">Ievadiet skaitli laukā Noapaļošanas nosacījums.</span><span class="sxs-lookup"><span data-stu-id="ef36c-133">In the Rounding rule field, enter a number.</span></span>
    * <span data-ttu-id="ef36c-134">Piemēram, ievadiet “1”, lai noapaļotu svaru līdz veselam skaitlim.</span><span class="sxs-lookup"><span data-stu-id="ef36c-134">For example, enter '1' for rounding weight to the integer.</span></span>  
10. <span data-ttu-id="ef36c-135">Izvērsiet sadaļu Minimālā robeža.</span><span class="sxs-lookup"><span data-stu-id="ef36c-135">Expand the Minimum limit section.</span></span>
11. <span data-ttu-id="ef36c-136">Laukā Svars ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="ef36c-136">In the Weight field, enter a number.</span></span>
    * <span data-ttu-id="ef36c-137">Piemēram, ievadiet “10” kā minimālo svaru.</span><span class="sxs-lookup"><span data-stu-id="ef36c-137">For example, enter '10' as the minimum weight.</span></span>  
12. <span data-ttu-id="ef36c-138">Laukā Summa ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="ef36c-138">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="ef36c-139">Piemēram, ievadiet “200” kā minimālo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="ef36c-139">For example, enter '200' as the minimum amount.</span></span>  
13. <span data-ttu-id="ef36c-140">Laukā Prece ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ef36c-140">In the Commodity field, enter or select a value.</span></span>

## <a name="set-up-compression-of-intrastat"></a><span data-ttu-id="ef36c-141">Iestatīt Intrastat arhivēšanu</span><span class="sxs-lookup"><span data-stu-id="ef36c-141">Set up Compression of Intrastat</span></span>
1. <span data-ttu-id="ef36c-142">Dodieties uz Nodokļi > Iestatīšana > Ārējā tirdzniecība > Intrastat arhivēšana.</span><span class="sxs-lookup"><span data-stu-id="ef36c-142">Go to Tax > Setup > Foreign trade > Compression of Intrastat.</span></span>
2. <span data-ttu-id="ef36c-143">Noklikšķiniet uz Noņemt.</span><span class="sxs-lookup"><span data-stu-id="ef36c-143">Click Remove.</span></span>
3. <span data-ttu-id="ef36c-144">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="ef36c-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ef36c-145">Piemēram, sadaļā Pieejams atlasiet vienumu Prece.</span><span class="sxs-lookup"><span data-stu-id="ef36c-145">For example, select Commodity in the Available section.</span></span>  
4. <span data-ttu-id="ef36c-146">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="ef36c-146">Click Add.</span></span>

## <a name="generate-intrastat-declaration"></a><span data-ttu-id="ef36c-147">Ģenerēt Intrastat deklarāciju</span><span class="sxs-lookup"><span data-stu-id="ef36c-147">Generate Intrastat declaration</span></span>
1. <span data-ttu-id="ef36c-148">Dodieties uz Nodokļi > Deklarācijas > Ārējā tirdzniecība > Intrastat</span><span class="sxs-lookup"><span data-stu-id="ef36c-148">Go to Tax > Declarations > Foreign trade > Intrastat</span></span>
2. <span data-ttu-id="ef36c-149">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="ef36c-149">Click Validate.</span></span>
    * <span data-ttu-id="ef36c-150">Pārbaude tiek veikta saskaņā ar lauku Iestatījumu pārbaude lapā Ārējās tirdzniecības parametri.</span><span class="sxs-lookup"><span data-stu-id="ef36c-150">The validation is done according to the Check setup field on the Foreign trade parameters page.</span></span>  
3. <span data-ttu-id="ef36c-151">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ef36c-151">Click OK.</span></span>
4. <span data-ttu-id="ef36c-152">Noklikšķiniet uz Atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="ef36c-152">Click Update.</span></span>
5. <span data-ttu-id="ef36c-153">Noklikšķiniet uz Minimālā robeža.</span><span class="sxs-lookup"><span data-stu-id="ef36c-153">Click Minimum limit.</span></span>
6. <span data-ttu-id="ef36c-154">Laukā Sākuma datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="ef36c-154">In the Start date field, enter a date.</span></span>
    * <span data-ttu-id="ef36c-155">Piemēram, ievadiet 2015. gada 1. janvāris.</span><span class="sxs-lookup"><span data-stu-id="ef36c-155">For example, enter January 1, 2015.</span></span>  
7. <span data-ttu-id="ef36c-156">Laukā Arhivēt atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="ef36c-156">Select Yes in the Compress field.</span></span>
8. <span data-ttu-id="ef36c-157">Laukā Beigu datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="ef36c-157">In the End date field, enter a date.</span></span>
    * <span data-ttu-id="ef36c-158">Piemēram, ievadiet 2015. gada 31. janvāris.</span><span class="sxs-lookup"><span data-stu-id="ef36c-158">For example, enter January 31, 2015.</span></span>  
9. <span data-ttu-id="ef36c-159">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ef36c-159">Click OK.</span></span>
10. <span data-ttu-id="ef36c-160">Noklikšķiniet uz Atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="ef36c-160">Click Update.</span></span>
11. <span data-ttu-id="ef36c-161">Noklikšķiniet uz Arhivēt.</span><span class="sxs-lookup"><span data-stu-id="ef36c-161">Click Compress.</span></span>
    * <span data-ttu-id="ef36c-162">Šī arhivēšana tiek veikta atbilstoši tam, kā ir iestatīti Instrastat arhivēšanas iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="ef36c-162">This compression happens according to how you set the Compression of intrastate settings.</span></span>  
12. <span data-ttu-id="ef36c-163">Laukā Sākuma datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="ef36c-163">In the Start date field, enter a date.</span></span>
    * <span data-ttu-id="ef36c-164">Piemēram, ievadiet 2015. gada 1. janvāris.</span><span class="sxs-lookup"><span data-stu-id="ef36c-164">For example, enter January 1, 2015.</span></span>  
13. <span data-ttu-id="ef36c-165">Laukā Beigu datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="ef36c-165">In the End date field, enter a date.</span></span>
    * <span data-ttu-id="ef36c-166">Piemēram, ievadiet 2015. gada 31. janvāris.</span><span class="sxs-lookup"><span data-stu-id="ef36c-166">For example, enter 31st January 2015.</span></span>  
14. <span data-ttu-id="ef36c-167">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ef36c-167">Click OK.</span></span>
15. <span data-ttu-id="ef36c-168">Noklikšķiniet uz Atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="ef36c-168">Click Update.</span></span>
16. <span data-ttu-id="ef36c-169">Noklikšķiniet uz Atjaunot sērijas numurus.</span><span class="sxs-lookup"><span data-stu-id="ef36c-169">Click Regenerate sequence numbers.</span></span>
17. <span data-ttu-id="ef36c-170">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ef36c-170">Click OK.</span></span>
18. <span data-ttu-id="ef36c-171">Noklikšķiniet uz Izvade.</span><span class="sxs-lookup"><span data-stu-id="ef36c-171">Click Output.</span></span>
19. <span data-ttu-id="ef36c-172">Noklikšķiniet uz Atskaite.</span><span class="sxs-lookup"><span data-stu-id="ef36c-172">Click Report.</span></span>
20. <span data-ttu-id="ef36c-173">Laukā No datuma ievadiet pārskata perioda pirmo datumu.</span><span class="sxs-lookup"><span data-stu-id="ef36c-173">In the From date field, enter the first date of the reporting period.</span></span>
    * <span data-ttu-id="ef36c-174">Piemēram, iestatiet datumu “2015. gada 1. janvāris”.</span><span class="sxs-lookup"><span data-stu-id="ef36c-174">For example, set the date to January 1, 2015.</span></span>  
21. <span data-ttu-id="ef36c-175">Laukā Līdz datumam ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="ef36c-175">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="ef36c-176">Piemēram, ievadiet 2015. gada 31. janvāris.</span><span class="sxs-lookup"><span data-stu-id="ef36c-176">For example, enter January 31, 2015.</span></span>  
22. <span data-ttu-id="ef36c-177">Laukā Ģenerēt failu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="ef36c-177">Select Yes in the Generate file field.</span></span>
23. <span data-ttu-id="ef36c-178">Ierakstiet vērtību laukā Faila nosaukums.</span><span class="sxs-lookup"><span data-stu-id="ef36c-178">In the File name field, type a value.</span></span>
24. <span data-ttu-id="ef36c-179">Laukā Ģenerēt pārskatu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="ef36c-179">Select Yes in the Generate report field.</span></span>
25. <span data-ttu-id="ef36c-180">Ierakstiet vērtību laukā Pārskata faila nosaukums.</span><span class="sxs-lookup"><span data-stu-id="ef36c-180">In the Report file name field, type a value.</span></span>
26. <span data-ttu-id="ef36c-181">Laukā Virziens atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="ef36c-181">In the Direction field, select an option.</span></span>
    * <span data-ttu-id="ef36c-182">Piemēram atlasiet “Izejošie krājumi”.</span><span class="sxs-lookup"><span data-stu-id="ef36c-182">For example, select 'Dispatches'.</span></span>  
27. <span data-ttu-id="ef36c-183">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ef36c-183">Click OK.</span></span>


