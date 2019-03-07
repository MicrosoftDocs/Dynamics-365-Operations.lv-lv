---
title: Numura zīmes uzlīmes drukāšanas iespējošana
description: Šī procedūra ļauj veikt seriālā pārvadāšanas konteinera koda (SPKK) etiķetes automātisko drukāšanu, kad pārdošanas izdošanas darba procesā pēdējais krājums ir izdots no krājumiem.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d906ca9f5a6536870fa0c322a0792ed5672c25e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "324035"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="45959-103">Numura zīmes uzlīmes drukāšanas iespējošana</span><span class="sxs-lookup"><span data-stu-id="45959-103">Enable license plate label printing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="45959-104">Šī procedūra ļauj veikt seriālā pārvadāšanas konteinera koda (SPKK) etiķetes automātisko drukāšanu, kad pārdošanas izdošanas darba procesā pēdējais krājums ir izdots no krājumiem.</span><span class="sxs-lookup"><span data-stu-id="45959-104">This procedure enables the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="45959-105">Šo procedūru varat palaist demonstrācijas datu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="45959-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="45959-106">Ja to palaižat, izmantojot pats savus datus, jums numura zīmei ir nepieciešama iestatīta numuru sērija.</span><span class="sxs-lookup"><span data-stu-id="45959-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="45959-107">Pirms sākat šo uzdevumu, ir jāiestata etiķešu printeris.</span><span class="sxs-lookup"><span data-stu-id="45959-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="45959-108">Dodieties uz Organizācijas administrēšana > Iestatīšana > Tīkla printeri.</span><span class="sxs-lookup"><span data-stu-id="45959-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="45959-109">Darbību rūtī noklikšķiniet uz Opcijas un pēc tam noklikšķiniet uz pogas Lejupielādēt dokumentu maršrutēšanas aģenta instalētāju.</span><span class="sxs-lookup"><span data-stu-id="45959-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="45959-110">Pirms turpiniet šīs procedūras izpildi, palaidiet instalētāju un pārliecinieties, ka strādājošs tīkla printeris ir iestatīts kā Aktīvs.</span><span class="sxs-lookup"><span data-stu-id="45959-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="45959-111">Iestatīt GS1 uzņēmuma prefiksu</span><span class="sxs-lookup"><span data-stu-id="45959-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="45959-112">Doties uz Noliktavas vadība > Iestatīšana > Noliktavas pārvaldības parametri.</span><span class="sxs-lookup"><span data-stu-id="45959-112">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="45959-113">Laukā GS1 uzņēmuma prefikss ievadiet 7 skaitļus savam GS1 uzņēmuma numuram.</span><span class="sxs-lookup"><span data-stu-id="45959-113">In the GS1 company prefix field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="45959-114">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="45959-114">Click Save.</span></span>
4. <span data-ttu-id="45959-115">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="45959-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="45959-116">SPKK unikālā noliktavas vienības identifikatora virknes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="45959-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="45959-117">Pārejiet uz sadaļu Organizācijas administrēšana > Numuru secība > Numuru secība.</span><span class="sxs-lookup"><span data-stu-id="45959-117">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="45959-118">Laukā Apgabals atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="45959-118">In the Area field, select an option.</span></span>
3. <span data-ttu-id="45959-119">Laukā Atsauce atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="45959-119">In the Reference field, select an option.</span></span>
4. <span data-ttu-id="45959-120">Laukā Uzņēmums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="45959-120">In the Company field, type a value.</span></span>
5. <span data-ttu-id="45959-121">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="45959-121">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="45959-122">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="45959-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="45959-123">Izvērsiet sadaļu Segmenti.</span><span class="sxs-lookup"><span data-stu-id="45959-123">Expand the Segments section.</span></span>
8. <span data-ttu-id="45959-124">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="45959-124">Click Edit.</span></span>
9. <span data-ttu-id="45959-125">Tabulā Segmenti atlasiet pirmo rindu</span><span class="sxs-lookup"><span data-stu-id="45959-125">In the Segments table, select the first row</span></span>
10. <span data-ttu-id="45959-126">Noklikšķiniet uz Noņemt.</span><span class="sxs-lookup"><span data-stu-id="45959-126">Click Remove.</span></span>
11. <span data-ttu-id="45959-127">Noklikšķiniet uz Noņemt.</span><span class="sxs-lookup"><span data-stu-id="45959-127">Click Remove.</span></span>
12. <span data-ttu-id="45959-128">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="45959-128">Click Save.</span></span>
13. <span data-ttu-id="45959-129">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="45959-129">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="45959-130">Izveidot dokumentu maršruta izkārtojumu</span><span class="sxs-lookup"><span data-stu-id="45959-130">Create the document route layout</span></span>
1. <span data-ttu-id="45959-131">Doties uz Noliktavas vadība > Iestatīšana > Dokumentu maršrutēšana > Dokumentu maršrutēšanas izkārtojumi.</span><span class="sxs-lookup"><span data-stu-id="45959-131">Go to Warehouse management > Setup > Document routing > Document routing layouts.</span></span>
    * <span data-ttu-id="45959-132">Iespējojiet SPKK izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="45959-132">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="45959-133">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="45959-133">Click New.</span></span>
3. <span data-ttu-id="45959-134">Laukā Izkārtojuma ID ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="45959-134">In the Layout ID field, type a value.</span></span>
4. <span data-ttu-id="45959-135">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="45959-135">In the Description field, type a value.</span></span>
5. <span data-ttu-id="45959-136">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="45959-136">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="45959-137">Noklikšķiniet uz Ievietot teksta beigās.</span><span class="sxs-lookup"><span data-stu-id="45959-137">Click Insert at end of text.</span></span>
7. <span data-ttu-id="45959-138">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="45959-138">Click Save.</span></span>
8. <span data-ttu-id="45959-139">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="45959-139">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="45959-140">Iestatīt dokumentu maršrutēšanu</span><span class="sxs-lookup"><span data-stu-id="45959-140">Set up the document routing</span></span>
1. <span data-ttu-id="45959-141">Doties uz Noliktavas vadība > Iestatīšana > Dokumentu maršrutēšana > Dokumentu maršrutēšana.</span><span class="sxs-lookup"><span data-stu-id="45959-141">Go to Warehouse management > Setup > Document routing > Document routing.</span></span>
2. <span data-ttu-id="45959-142">Laukā Darba pasūtījuma tips atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="45959-142">In the Work order type field, select an option.</span></span>
3. <span data-ttu-id="45959-143">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="45959-143">Click New.</span></span>
4. <span data-ttu-id="45959-144">Laukā Noliktava ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="45959-144">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="45959-145">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="45959-145">In the Name field, type a value.</span></span>
6. <span data-ttu-id="45959-146">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="45959-146">Click New.</span></span>
7. <span data-ttu-id="45959-147">Laukā Izkārtojuma ID ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="45959-147">In the Layout ID field, enter or select a value.</span></span>
8. <span data-ttu-id="45959-148">Laukā Nosaukums ievadiet tā printera nosaukumu, kuru vēlaties izmantot.</span><span class="sxs-lookup"><span data-stu-id="45959-148">In the Name field, enter the printer name that you want to use..</span></span>
9. <span data-ttu-id="45959-149">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="45959-149">Click Save.</span></span>
10. <span data-ttu-id="45959-150">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="45959-150">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="45959-151">Izveidot mobilās ierīces izvēlni</span><span class="sxs-lookup"><span data-stu-id="45959-151">Create mobile device menu</span></span>
1. <span data-ttu-id="45959-152">Dodieties uz Noliktavas vadība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlnes vienumi.</span><span class="sxs-lookup"><span data-stu-id="45959-152">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="45959-153">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="45959-153">Click New.</span></span>
3. <span data-ttu-id="45959-154">Laukā Izvēlnes vienuma nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="45959-154">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="45959-155">Laukā Virsraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="45959-155">In the Title field, type a value.</span></span>
5. <span data-ttu-id="45959-156">Laukā Režīms atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="45959-156">In the Mode field, select an option.</span></span>
6. <span data-ttu-id="45959-157">Laukā Izmantot esošo darbu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="45959-157">Select Yes in the Use existing work field.</span></span>
7. <span data-ttu-id="45959-158">Laukā Ģenerēt numura zīmi atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="45959-158">Select Yes in the Generate license plate field.</span></span>
8. <span data-ttu-id="45959-159">Izvērsiet sadaļu Darba klases.</span><span class="sxs-lookup"><span data-stu-id="45959-159">Expand the Work classes section.</span></span>
9. <span data-ttu-id="45959-160">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="45959-160">Click New.</span></span>
10. <span data-ttu-id="45959-161">Laukā Darba klases ID ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="45959-161">In the Work class ID field, type a value.</span></span>
11. <span data-ttu-id="45959-162">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="45959-162">Click Save.</span></span>
12. <span data-ttu-id="45959-163">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="45959-163">Close the page.</span></span>
13. <span data-ttu-id="45959-164">Dodieties uz Noliktavas vadība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlne.</span><span class="sxs-lookup"><span data-stu-id="45959-164">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
14. <span data-ttu-id="45959-165">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="45959-165">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="45959-166">Koka struktūrā atlasiet “Koka struktūrā atlasiet iepriekš izveidoto izvēlnes vienumu.”.</span><span class="sxs-lookup"><span data-stu-id="45959-166">In the tree, select 'In the tree, select the menu item that you created before.'.</span></span>
16. <span data-ttu-id="45959-167">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="45959-167">Click Edit.</span></span>
17. <span data-ttu-id="45959-168">Noklikšķiniet uz bultiņas, lai šo izvēlnes vienumu pievienotu izvēlnei.</span><span class="sxs-lookup"><span data-stu-id="45959-168">Click on the arrow to add the menu item to the menu.</span></span>
18. <span data-ttu-id="45959-169">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="45959-169">Click Save.</span></span>
19. <span data-ttu-id="45959-170">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="45959-170">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="45959-171">Atjaunināt darba veidni</span><span class="sxs-lookup"><span data-stu-id="45959-171">Update a work template</span></span>
1. <span data-ttu-id="45959-172">Doties uz Noliktavas vadība > Iestatīšana > Darbs > Darbu veidnes.</span><span class="sxs-lookup"><span data-stu-id="45959-172">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="45959-173">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="45959-173">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="45959-174">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="45959-174">Click Edit.</span></span>
4. <span data-ttu-id="45959-175">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="45959-175">Click New.</span></span>
5. <span data-ttu-id="45959-176">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="45959-176">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="45959-177">Laukā Darba tips atlasiet vienumu “Drukāt”.</span><span class="sxs-lookup"><span data-stu-id="45959-177">In the Work type field, select 'Print'.</span></span>
7. <span data-ttu-id="45959-178">Laukā Darba klases ID ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="45959-178">In the Work class ID field, enter or select a value.</span></span>
8. <span data-ttu-id="45959-179">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="45959-179">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="45959-180">Noklikšķiniet uz Pārvietot uz augšu.</span><span class="sxs-lookup"><span data-stu-id="45959-180">Click Move up.</span></span>
10. <span data-ttu-id="45959-181">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="45959-181">Click Save.</span></span>
11. <span data-ttu-id="45959-182">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="45959-182">Close the page.</span></span>

