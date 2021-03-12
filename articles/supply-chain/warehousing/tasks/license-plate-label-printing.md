---
title: Numura zīmes uzlīmes drukāšanas iespējošana
description: Šajā tēmā parādīts, kā iespējot seriālā pārvadāšanas konteinera koda (SSCC) marķējuma drukāšanu pēc tam, kad pēdējais vienums ir izņemts no inventāra pārdošanas pavadzīmju darba procesā.
author: perlynne
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d5580edb3324f76f04140bd6793bddaace5fadcf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977117"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="0e93e-103">Numura zīmes uzlīmes drukāšanas iespējošana</span><span class="sxs-lookup"><span data-stu-id="0e93e-103">Enable license plate label printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0e93e-104">Šajā tēmā parādīts, kā iespējot seriālā pārvadāšanas konteinera koda (SSCC) marķējuma drukāšanu pēc tam, kad pēdējais vienums ir izņemts no inventāra pārdošanas pavadzīmju darba procesā.</span><span class="sxs-lookup"><span data-stu-id="0e93e-104">This topic shows how to enable the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="0e93e-105">Šo procedūru varat palaist demonstrācijas datu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="0e93e-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="0e93e-106">Ja to palaižat, izmantojot pats savus datus, jums numura zīmei ir nepieciešama iestatīta numuru sērija.</span><span class="sxs-lookup"><span data-stu-id="0e93e-106">If you're run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="0e93e-107">Pirms sākat šo uzdevumu, ir jāiestata etiķešu printeris.</span><span class="sxs-lookup"><span data-stu-id="0e93e-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="0e93e-108">Dodieties uz Organizācijas administrēšana > Iestatīšana > Tīkla printeri.</span><span class="sxs-lookup"><span data-stu-id="0e93e-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="0e93e-109">Darbību rūtī noklikšķiniet uz Opcijas un pēc tam noklikšķiniet uz pogas Lejupielādēt dokumentu maršrutēšanas aģenta instalētāju.</span><span class="sxs-lookup"><span data-stu-id="0e93e-109">On the Action Pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="0e93e-110">Pirms turpiniet šīs procedūras izpildi, palaidiet instalētāju un pārliecinieties, ka strādājošs tīkla printeris ir iestatīts kā Aktīvs.</span><span class="sxs-lookup"><span data-stu-id="0e93e-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="0e93e-111">Iestatīt GS1 uzņēmuma prefiksu</span><span class="sxs-lookup"><span data-stu-id="0e93e-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="0e93e-112">Dodieties uz **Navigācijas rūts > Moduļi > Noliktavas vadība > Iestatīšana> Noliktavas vadības parametri**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-112">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="0e93e-113">Laukā **GS1 uzņēmuma prefikss** ievadiet sava GS1 uzņēmuma numura 7 ciparus.</span><span class="sxs-lookup"><span data-stu-id="0e93e-113">In the **GS1 company prefix** field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="0e93e-114">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-114">Select **Save**.</span></span>
4. <span data-ttu-id="0e93e-115">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0e93e-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="0e93e-116">SPKK unikālā noliktavas vienības identifikatora virknes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="0e93e-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="0e93e-117">Pārejiet uz **Navigācijas rūts > Moduļi > Organizācijas administrēšana > Numuru sērijas > Numuru sērijas**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-117">Go to **Navigation pane > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="0e93e-118">Laukā **Apgabals** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="0e93e-118">In the **Area** field, select an option.</span></span>
3. <span data-ttu-id="0e93e-119">Laukā **Atsauce** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="0e93e-119">In the **Reference** field, select an option.</span></span>
4. <span data-ttu-id="0e93e-120">Laukā **Uzņēmums** ievadiet vērtību. </span><span class="sxs-lookup"><span data-stu-id="0e93e-120">In the **Company** field, type a value.</span></span>
5. <span data-ttu-id="0e93e-121">Izvērsiet sadaļu **Segmenti**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-121">Expand the **Segments** section.</span></span>
6. <span data-ttu-id="0e93e-122">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-122">Select **Edit**.</span></span>
7. <span data-ttu-id="0e93e-123">Tabulā **Segmenti** atlasiet pirmo rindu</span><span class="sxs-lookup"><span data-stu-id="0e93e-123">In the **Segments** table, select the first row</span></span>
8. <span data-ttu-id="0e93e-124">Atlasiet **Noņemt**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-124">Select **Remove**.</span></span>
9. <span data-ttu-id="0e93e-125">Atlasiet **Noņemt**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-125">Select **Remove**.</span></span>
10. <span data-ttu-id="0e93e-126">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-126">Select **Save**.</span></span>
11. <span data-ttu-id="0e93e-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0e93e-127">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="0e93e-128">Izveidot dokumentu maršruta izkārtojumu</span><span class="sxs-lookup"><span data-stu-id="0e93e-128">Create the document route layout</span></span>
1. <span data-ttu-id="0e93e-129">Dodieties uz **Navigācijas rūts > Moduļi > Noliktavas vadība > Iestatīšana> Dokumentu maršrutēšana > Dokumentu maršrutēšanas izkārtojumi**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-129">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing layouts**.</span></span> <span data-ttu-id="0e93e-130">Iespējojiet SPKK izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="0e93e-130">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="0e93e-131">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-131">Select **New**.</span></span>
3. <span data-ttu-id="0e93e-132">Laukā **Izkārtojuma ID** ievadiet vērtību. </span><span class="sxs-lookup"><span data-stu-id="0e93e-132">In the **Layout ID** field, type a value.</span></span>
4. <span data-ttu-id="0e93e-133">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0e93e-133">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="0e93e-134">Atlasiet **Ievadīt teksta beigās**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-134">Select **Insert at end of text**.</span></span>
6. <span data-ttu-id="0e93e-135">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-135">Select **Save**.</span></span>
7. <span data-ttu-id="0e93e-136">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0e93e-136">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="0e93e-137">Iestatīt dokumentu maršrutēšanu</span><span class="sxs-lookup"><span data-stu-id="0e93e-137">Set up the document routing</span></span>
1. <span data-ttu-id="0e93e-138">Dodieties uz **Navigācijas rūts > Moduļi > Noliktavas vadība > Iestatīšana> Dokumentu maršrutēšana > Dokumentu maršrutēšana**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-138">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing**.</span></span>
2. <span data-ttu-id="0e93e-139">Laukā **Darba pasūtījuma tips** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="0e93e-139">In the **Work order type** field, select an option.</span></span>
3. <span data-ttu-id="0e93e-140">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-140">Select **New**.</span></span>
4. <span data-ttu-id="0e93e-141">Laukā **Noliktava** atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="0e93e-141">In the **Warehouse** field, type a value.</span></span>
5. <span data-ttu-id="0e93e-142">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0e93e-142">In the **Name** field, type a value.</span></span>
6. <span data-ttu-id="0e93e-143">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-143">Select **New**.</span></span>
7. <span data-ttu-id="0e93e-144">Laukā **Izkārtojuma ID** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="0e93e-144">In the **Layout ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="0e93e-145">Laukā **Nosaukums** ievadiet tā printera nosaukumu, kuru vēlaties lietot.</span><span class="sxs-lookup"><span data-stu-id="0e93e-145">In the **Name** field, enter the printer name that you want to use.</span></span>
9. <span data-ttu-id="0e93e-146">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-146">Select **Save**.</span></span>
10. <span data-ttu-id="0e93e-147">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0e93e-147">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="0e93e-148">Izveidot mobilās ierīces izvēlni</span><span class="sxs-lookup"><span data-stu-id="0e93e-148">Create mobile device menu</span></span>
1. <span data-ttu-id="0e93e-149">Dodieties uz **Navigācijas rūts > Moduļi > Noliktavas vadība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlne**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-149">Go to **Navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="0e93e-150">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-150">Select **New**.</span></span>
3. <span data-ttu-id="0e93e-151">Laukā **Izvēlnes vienuma nosaukums** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="0e93e-151">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="0e93e-152">Laukā **Nosaukums** ievadiet vērtību. </span><span class="sxs-lookup"><span data-stu-id="0e93e-152">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="0e93e-153">Laukā **Režīms** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="0e93e-153">In the **Mode** field, select an option.</span></span>
6. <span data-ttu-id="0e93e-154">Atlasiet **Jā** laukā **Izmantot esošo darbu**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-154">Select **Yes** in the **Use existing work** field.</span></span>
7. <span data-ttu-id="0e93e-155">Atlasiet **Jā** laukā **Ģenerēt licences numura zīmi**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-155">Select **Yes** in the **Generate license plate** field.</span></span>
8. <span data-ttu-id="0e93e-156">Izvērtiet sadaļu **Darba klases**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-156">Expand the **Work classes** section.</span></span>
9. <span data-ttu-id="0e93e-157">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-157">Select **New**.</span></span>
10. <span data-ttu-id="0e93e-158">Laukā **Darba klases ID** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="0e93e-158">In the **Work class ID** field, type a value.</span></span>
11. <span data-ttu-id="0e93e-159">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-159">Select **Save**.</span></span>
12. <span data-ttu-id="0e93e-160">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0e93e-160">Close the page.</span></span>
13. <span data-ttu-id="0e93e-161">Dodieties uz **Navigācijas rūts > Moduļi > Noliktavas vadība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlne**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-161">Go to **navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
14. <span data-ttu-id="0e93e-162">Kokā atlasiet to izvēlnes vienumu, kuru izveidojāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="0e93e-162">In the tree, select the menu item that you created before.</span></span>
15. <span data-ttu-id="0e93e-163">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-163">Select **Edit**.</span></span>
16. <span data-ttu-id="0e93e-164">Atlasiet bultu, lai izvēlnei pievienotu izvēlnes vienumu.</span><span class="sxs-lookup"><span data-stu-id="0e93e-164">Select the arrow to add the menu item to the menu.</span></span>
17. <span data-ttu-id="0e93e-165">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-165">Select **Save**.</span></span>
18. <span data-ttu-id="0e93e-166">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0e93e-166">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="0e93e-167">Atjaunināt darba veidni</span><span class="sxs-lookup"><span data-stu-id="0e93e-167">Update a work template</span></span>
1. <span data-ttu-id="0e93e-168">Dodieties uz **Navigācijas rūts > Moduļi > Noliktavas vadība > Iestatīšana> Darbs > Darba veidnes**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-168">Go to **Navigation pane > Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="0e93e-169">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-169">Select **Edit**.</span></span>
3. <span data-ttu-id="0e93e-170">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-170">Select **New**.</span></span>
4. <span data-ttu-id="0e93e-171">Laukā **Darba tips** atlasiet **Drukāt**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-171">In the **Work type** field, select **Print**.</span></span>
5. <span data-ttu-id="0e93e-172">Laukā **Darba klases ID** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="0e93e-172">In the **Work class ID** field, enter or select a value.</span></span>
6. <span data-ttu-id="0e93e-173">Atlasiet **Pārvietot uz augšu**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-173">Select **Move up**.</span></span>
7. <span data-ttu-id="0e93e-174">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0e93e-174">Select **Save**.</span></span>
8. <span data-ttu-id="0e93e-175">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0e93e-175">Close the page.</span></span>

