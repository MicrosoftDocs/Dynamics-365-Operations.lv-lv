--- 
title: "Numura zīmes uzlīmes drukāšanas iespējošana"
description: "Šī procedūra ļauj veikt seriālā pārvadāšanas konteinera koda (SPKK) etiķetes automātisko drukāšanu, kad pārdošanas izdošanas darba procesā pēdējais krājums ir izdots no krājumiem."
author: perlynne
manager: AnnBe
ms.date: 11/03/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6d186bf7e4aee8cfa97adbd90b9090085e842f9b
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="5ca55-103">Numura zīmes uzlīmes drukāšanas iespējošana</span><span class="sxs-lookup"><span data-stu-id="5ca55-103">Enable license plate label printing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5ca55-104">Šī procedūra ļauj veikt seriālā pārvadāšanas konteinera koda (SPKK) etiķetes automātisko drukāšanu, kad pārdošanas izdošanas darba procesā pēdējais krājums ir izdots no krājumiem.</span><span class="sxs-lookup"><span data-stu-id="5ca55-104">This procedure enables the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="5ca55-105">Šo procedūru varat palaist demonstrācijas datu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="5ca55-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="5ca55-106">Ja to palaižat, izmantojot pats savus datus, jums numura zīmei ir nepieciešama iestatīta numuru sērija.</span><span class="sxs-lookup"><span data-stu-id="5ca55-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="5ca55-107">Pirms sākat šo uzdevumu, ir jāiestata etiķešu printeris.</span><span class="sxs-lookup"><span data-stu-id="5ca55-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="5ca55-108">Dodieties uz Organizācijas administrēšana > Iestatīšana > Tīkla printeri.</span><span class="sxs-lookup"><span data-stu-id="5ca55-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="5ca55-109">Darbību rūtī noklikšķiniet uz Opcijas un pēc tam noklikšķiniet uz pogas Lejupielādēt dokumentu maršrutēšanas aģenta instalētāju.</span><span class="sxs-lookup"><span data-stu-id="5ca55-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="5ca55-110">Pirms turpiniet šīs procedūras izpildi, palaidiet instalētāju un pārliecinieties, ka strādājošs tīkla printeris ir iestatīts kā Aktīvs.</span><span class="sxs-lookup"><span data-stu-id="5ca55-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="5ca55-111">Iestatīt GS1 uzņēmuma prefiksu</span><span class="sxs-lookup"><span data-stu-id="5ca55-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="5ca55-112">Doties uz Noliktavas vadība > Iestatīšana > Noliktavas pārvaldības parametri.</span><span class="sxs-lookup"><span data-stu-id="5ca55-112">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="5ca55-113">Laukā GS1 uzņēmuma prefikss ievadiet 7 skaitļus savam GS1 uzņēmuma numuram.</span><span class="sxs-lookup"><span data-stu-id="5ca55-113">In the GS1 company prefix field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="5ca55-114">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="5ca55-114">Click Save.</span></span>
4. <span data-ttu-id="5ca55-115">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5ca55-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="5ca55-116">SPKK unikālā noliktavas vienības identifikatora virknes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5ca55-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="5ca55-117">Pārejiet uz sadaļu Organizācijas administrēšana > Numuru secība > Numuru secība.</span><span class="sxs-lookup"><span data-stu-id="5ca55-117">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="5ca55-118">Laukā Apgabals atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="5ca55-118">In the Area field, select an option.</span></span>
3. <span data-ttu-id="5ca55-119">Laukā Atsauce atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="5ca55-119">In the Reference field, select an option.</span></span>
4. <span data-ttu-id="5ca55-120">Laukā Uzņēmums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5ca55-120">In the Company field, type a value.</span></span>
5. <span data-ttu-id="5ca55-121">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="5ca55-121">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="5ca55-122">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="5ca55-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="5ca55-123">Izvērsiet sadaļu Segmenti.</span><span class="sxs-lookup"><span data-stu-id="5ca55-123">Expand the Segments section.</span></span>
8. <span data-ttu-id="5ca55-124">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="5ca55-124">Click Edit.</span></span>
9. <span data-ttu-id="5ca55-125">Tabulā Segmenti atlasiet pirmo rindu</span><span class="sxs-lookup"><span data-stu-id="5ca55-125">In the Segments table, select the first row</span></span>
10. <span data-ttu-id="5ca55-126">Noklikšķiniet uz Noņemt.</span><span class="sxs-lookup"><span data-stu-id="5ca55-126">Click Remove.</span></span>
11. <span data-ttu-id="5ca55-127">Noklikšķiniet uz Noņemt.</span><span class="sxs-lookup"><span data-stu-id="5ca55-127">Click Remove.</span></span>
12. <span data-ttu-id="5ca55-128">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="5ca55-128">Click Save.</span></span>
13. <span data-ttu-id="5ca55-129">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5ca55-129">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="5ca55-130">Izveidot dokumentu maršruta izkārtojumu</span><span class="sxs-lookup"><span data-stu-id="5ca55-130">Create the document route layout</span></span>
1. <span data-ttu-id="5ca55-131">Doties uz Noliktavas vadība > Iestatīšana > Dokumentu maršrutēšana > Dokumentu maršrutēšanas izkārtojumi.</span><span class="sxs-lookup"><span data-stu-id="5ca55-131">Go to Warehouse management > Setup > Document routing > Document routing layouts.</span></span>
    * <span data-ttu-id="5ca55-132">Iespējojiet SPKK izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="5ca55-132">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="5ca55-133">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="5ca55-133">Click New.</span></span>
3. <span data-ttu-id="5ca55-134">Laukā Izkārtojuma ID ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5ca55-134">In the Layout ID field, type a value.</span></span>
4. <span data-ttu-id="5ca55-135">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="5ca55-135">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5ca55-136">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="5ca55-136">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="5ca55-137">Noklikšķiniet uz Ievietot teksta beigās.</span><span class="sxs-lookup"><span data-stu-id="5ca55-137">Click Insert at end of text.</span></span>
7. <span data-ttu-id="5ca55-138">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="5ca55-138">Click Save.</span></span>
8. <span data-ttu-id="5ca55-139">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5ca55-139">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="5ca55-140">Iestatīt dokumentu maršrutēšanu</span><span class="sxs-lookup"><span data-stu-id="5ca55-140">Set up the document routing</span></span>
1. <span data-ttu-id="5ca55-141">Doties uz Noliktavas vadība > Iestatīšana > Dokumentu maršrutēšana > Dokumentu maršrutēšana.</span><span class="sxs-lookup"><span data-stu-id="5ca55-141">Go to Warehouse management > Setup > Document routing > Document routing.</span></span>
2. <span data-ttu-id="5ca55-142">Laukā Darba pasūtījuma tips atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="5ca55-142">In the Work order type field, select an option.</span></span>
3. <span data-ttu-id="5ca55-143">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="5ca55-143">Click New.</span></span>
4. <span data-ttu-id="5ca55-144">Laukā Noliktava ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5ca55-144">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="5ca55-145">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5ca55-145">In the Name field, type a value.</span></span>
6. <span data-ttu-id="5ca55-146">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="5ca55-146">Click New.</span></span>
7. <span data-ttu-id="5ca55-147">Laukā Izkārtojuma ID ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5ca55-147">In the Layout ID field, enter or select a value.</span></span>
8. <span data-ttu-id="5ca55-148">Laukā Nosaukums ievadiet tā printera nosaukumu, kuru vēlaties izmantot.</span><span class="sxs-lookup"><span data-stu-id="5ca55-148">In the Name field, enter the printer name that you want to use..</span></span>
9. <span data-ttu-id="5ca55-149">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="5ca55-149">Click Save.</span></span>
10. <span data-ttu-id="5ca55-150">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5ca55-150">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="5ca55-151">Izveidot mobilās ierīces izvēlni</span><span class="sxs-lookup"><span data-stu-id="5ca55-151">Create mobile device menu</span></span>
1. <span data-ttu-id="5ca55-152">Dodieties uz Noliktavas vadība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlnes vienumi.</span><span class="sxs-lookup"><span data-stu-id="5ca55-152">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="5ca55-153">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="5ca55-153">Click New.</span></span>
3. <span data-ttu-id="5ca55-154">Laukā Izvēlnes vienuma nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5ca55-154">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="5ca55-155">Laukā Virsraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5ca55-155">In the Title field, type a value.</span></span>
5. <span data-ttu-id="5ca55-156">Laukā Režīms atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="5ca55-156">In the Mode field, select an option.</span></span>
6. <span data-ttu-id="5ca55-157">Laukā Izmantot esošo darbu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="5ca55-157">Select Yes in the Use existing work field.</span></span>
7. <span data-ttu-id="5ca55-158">Laukā Ģenerēt numura zīmi atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="5ca55-158">Select Yes in the Generate license plate field.</span></span>
8. <span data-ttu-id="5ca55-159">Izvērsiet sadaļu Darba klases.</span><span class="sxs-lookup"><span data-stu-id="5ca55-159">Expand the Work classes section.</span></span>
9. <span data-ttu-id="5ca55-160">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="5ca55-160">Click New.</span></span>
10. <span data-ttu-id="5ca55-161">Laukā Darba klases ID ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5ca55-161">In the Work class ID field, type a value.</span></span>
11. <span data-ttu-id="5ca55-162">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="5ca55-162">Click Save.</span></span>
12. <span data-ttu-id="5ca55-163">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5ca55-163">Close the page.</span></span>
13. <span data-ttu-id="5ca55-164">Dodieties uz Noliktavas vadība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlne.</span><span class="sxs-lookup"><span data-stu-id="5ca55-164">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
14. <span data-ttu-id="5ca55-165">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="5ca55-165">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="5ca55-166">Koka struktūrā atlasiet “Koka struktūrā atlasiet iepriekš izveidoto izvēlnes vienumu.”.</span><span class="sxs-lookup"><span data-stu-id="5ca55-166">In the tree, select 'In the tree, select the menu item that you created before.'.</span></span>
16. <span data-ttu-id="5ca55-167">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="5ca55-167">Click Edit.</span></span>
17. <span data-ttu-id="5ca55-168">Noklikšķiniet uz bultiņas, lai šo izvēlnes vienumu pievienotu izvēlnei.</span><span class="sxs-lookup"><span data-stu-id="5ca55-168">Click on the arrow to add the menu item to the menu.</span></span>
18. <span data-ttu-id="5ca55-169">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="5ca55-169">Click Save.</span></span>
19. <span data-ttu-id="5ca55-170">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5ca55-170">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="5ca55-171">Atjaunināt darba veidni</span><span class="sxs-lookup"><span data-stu-id="5ca55-171">Update a work template</span></span>
1. <span data-ttu-id="5ca55-172">Doties uz Noliktavas vadība > Iestatīšana > Darbs > Darbu veidnes.</span><span class="sxs-lookup"><span data-stu-id="5ca55-172">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="5ca55-173">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="5ca55-173">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="5ca55-174">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="5ca55-174">Click Edit.</span></span>
4. <span data-ttu-id="5ca55-175">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="5ca55-175">Click New.</span></span>
5. <span data-ttu-id="5ca55-176">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="5ca55-176">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="5ca55-177">Laukā Darba tips atlasiet vienumu “Drukāt”.</span><span class="sxs-lookup"><span data-stu-id="5ca55-177">In the Work type field, select 'Print'.</span></span>
7. <span data-ttu-id="5ca55-178">Laukā Darba klases ID ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5ca55-178">In the Work class ID field, enter or select a value.</span></span>
8. <span data-ttu-id="5ca55-179">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="5ca55-179">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="5ca55-180">Noklikšķiniet uz Pārvietot uz augšu.</span><span class="sxs-lookup"><span data-stu-id="5ca55-180">Click Move up.</span></span>
10. <span data-ttu-id="5ca55-181">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="5ca55-181">Click Save.</span></span>
11. <span data-ttu-id="5ca55-182">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5ca55-182">Close the page.</span></span>


