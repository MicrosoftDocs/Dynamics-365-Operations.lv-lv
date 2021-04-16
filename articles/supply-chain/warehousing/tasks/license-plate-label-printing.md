---
title: Numura zīmes uzlīmes drukāšanas iespējošana
description: Šajā tēmā parādīts, kā iespējot seriālā pārvadāšanas konteinera koda (SSCC) marķējuma drukāšanu pēc tam, kad pēdējais vienums ir izņemts no inventāra pārdošanas pavadzīmju darba procesā.
author: perlynne
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a608e9a2356f9dd49bbec1bcbe5489af5931d44
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830886"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="2390d-103">Numura zīmes uzlīmes drukāšanas iespējošana</span><span class="sxs-lookup"><span data-stu-id="2390d-103">Enable license plate label printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2390d-104">Šajā tēmā parādīts, kā iespējot seriālā pārvadāšanas konteinera koda (SSCC) marķējuma drukāšanu pēc tam, kad pēdējais vienums ir izņemts no inventāra pārdošanas pavadzīmju darba procesā.</span><span class="sxs-lookup"><span data-stu-id="2390d-104">This topic shows how to enable the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="2390d-105">Šo procedūru varat palaist demonstrācijas datu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="2390d-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="2390d-106">Ja to palaižat, izmantojot pats savus datus, jums numura zīmei ir nepieciešama iestatīta numuru sērija.</span><span class="sxs-lookup"><span data-stu-id="2390d-106">If you're run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="2390d-107">Pirms sākat šo uzdevumu, ir jāiestata etiķešu printeris.</span><span class="sxs-lookup"><span data-stu-id="2390d-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="2390d-108">Dodieties uz Organizācijas administrēšana > Iestatīšana > Tīkla printeri.</span><span class="sxs-lookup"><span data-stu-id="2390d-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="2390d-109">Darbību rūtī noklikšķiniet uz Opcijas un pēc tam noklikšķiniet uz pogas Lejupielādēt dokumentu maršrutēšanas aģenta instalētāju.</span><span class="sxs-lookup"><span data-stu-id="2390d-109">On the Action Pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="2390d-110">Pirms turpiniet šīs procedūras izpildi, palaidiet instalētāju un pārliecinieties, ka strādājošs tīkla printeris ir iestatīts kā Aktīvs.</span><span class="sxs-lookup"><span data-stu-id="2390d-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="2390d-111">Iestatīt GS1 uzņēmuma prefiksu</span><span class="sxs-lookup"><span data-stu-id="2390d-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="2390d-112">Dodieties uz **Navigācijas rūts > Moduļi > Noliktavas pārvaldība > Iestatīšana> Noliktavas vadības parametri**.</span><span class="sxs-lookup"><span data-stu-id="2390d-112">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="2390d-113">Laukā **GS1 uzņēmuma prefikss** ievadiet sava GS1 uzņēmuma numura 7 ciparus.</span><span class="sxs-lookup"><span data-stu-id="2390d-113">In the **GS1 company prefix** field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="2390d-114">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="2390d-114">Select **Save**.</span></span>
4. <span data-ttu-id="2390d-115">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2390d-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="2390d-116">SPKK unikālā noliktavas vienības identifikatora virknes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="2390d-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="2390d-117">Pārejiet uz **Navigācijas rūts > Moduļi > Organizācijas administrēšana > Numuru sērijas > Numuru sērijas**.</span><span class="sxs-lookup"><span data-stu-id="2390d-117">Go to **Navigation pane > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="2390d-118">Laukā **Apgabals** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="2390d-118">In the **Area** field, select an option.</span></span>
3. <span data-ttu-id="2390d-119">Laukā **Atsauce** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="2390d-119">In the **Reference** field, select an option.</span></span>
4. <span data-ttu-id="2390d-120">Laukā **Uzņēmums** ievadiet vērtību. </span><span class="sxs-lookup"><span data-stu-id="2390d-120">In the **Company** field, type a value.</span></span>
5. <span data-ttu-id="2390d-121">Izvērsiet sadaļu **Segmenti**.</span><span class="sxs-lookup"><span data-stu-id="2390d-121">Expand the **Segments** section.</span></span>
6. <span data-ttu-id="2390d-122">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="2390d-122">Select **Edit**.</span></span>
7. <span data-ttu-id="2390d-123">Tabulā **Segmenti** atlasiet pirmo rindu</span><span class="sxs-lookup"><span data-stu-id="2390d-123">In the **Segments** table, select the first row</span></span>
8. <span data-ttu-id="2390d-124">Atlasiet **Noņemt**.</span><span class="sxs-lookup"><span data-stu-id="2390d-124">Select **Remove**.</span></span>
9. <span data-ttu-id="2390d-125">Atlasiet **Noņemt**.</span><span class="sxs-lookup"><span data-stu-id="2390d-125">Select **Remove**.</span></span>
10. <span data-ttu-id="2390d-126">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="2390d-126">Select **Save**.</span></span>
11. <span data-ttu-id="2390d-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2390d-127">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="2390d-128">Izveidot dokumentu maršruta izkārtojumu</span><span class="sxs-lookup"><span data-stu-id="2390d-128">Create the document route layout</span></span>
1. <span data-ttu-id="2390d-129">Dodieties uz **Navigācijas rūts > Moduļi > Noliktavas pārvaldība > Iestatīšana> Dokumentu maršrutēšana > Dokumentu maršrutēšanas izkārtojumi**.</span><span class="sxs-lookup"><span data-stu-id="2390d-129">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing layouts**.</span></span> <span data-ttu-id="2390d-130">Iespējojiet SPKK izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="2390d-130">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="2390d-131">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="2390d-131">Select **New**.</span></span>
3. <span data-ttu-id="2390d-132">Laukā **Izkārtojuma ID** ievadiet vērtību. </span><span class="sxs-lookup"><span data-stu-id="2390d-132">In the **Layout ID** field, type a value.</span></span>
4. <span data-ttu-id="2390d-133">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2390d-133">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="2390d-134">Atlasiet **Ievadīt teksta beigās**.</span><span class="sxs-lookup"><span data-stu-id="2390d-134">Select **Insert at end of text**.</span></span>
6. <span data-ttu-id="2390d-135">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="2390d-135">Select **Save**.</span></span>
7. <span data-ttu-id="2390d-136">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2390d-136">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="2390d-137">Iestatīt dokumentu maršrutēšanu</span><span class="sxs-lookup"><span data-stu-id="2390d-137">Set up the document routing</span></span>
1. <span data-ttu-id="2390d-138">Dodieties uz **Navigācijas rūts > Moduļi > Noliktavas pārvaldība > Iestatīšana> Dokumentu maršrutēšana > Dokumentu maršrutēšana**.</span><span class="sxs-lookup"><span data-stu-id="2390d-138">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing**.</span></span>
2. <span data-ttu-id="2390d-139">Laukā **Darba pasūtījuma tips** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="2390d-139">In the **Work order type** field, select an option.</span></span>
3. <span data-ttu-id="2390d-140">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="2390d-140">Select **New**.</span></span>
4. <span data-ttu-id="2390d-141">Laukā **Noliktava** atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="2390d-141">In the **Warehouse** field, type a value.</span></span>
5. <span data-ttu-id="2390d-142">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2390d-142">In the **Name** field, type a value.</span></span>
6. <span data-ttu-id="2390d-143">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="2390d-143">Select **New**.</span></span>
7. <span data-ttu-id="2390d-144">Laukā **Izkārtojuma ID** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="2390d-144">In the **Layout ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="2390d-145">Laukā **Nosaukums** ievadiet tā printera nosaukumu, kuru vēlaties lietot.</span><span class="sxs-lookup"><span data-stu-id="2390d-145">In the **Name** field, enter the printer name that you want to use.</span></span>
9. <span data-ttu-id="2390d-146">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="2390d-146">Select **Save**.</span></span>
10. <span data-ttu-id="2390d-147">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2390d-147">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="2390d-148">Izveidot mobilās ierīces izvēlni</span><span class="sxs-lookup"><span data-stu-id="2390d-148">Create mobile device menu</span></span>
1. <span data-ttu-id="2390d-149">Dodieties uz **Navigācijas rūts > Moduļi > Noliktavas pārvaldība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlne**.</span><span class="sxs-lookup"><span data-stu-id="2390d-149">Go to **Navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="2390d-150">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="2390d-150">Select **New**.</span></span>
3. <span data-ttu-id="2390d-151">Laukā **Izvēlnes vienuma nosaukums** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="2390d-151">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="2390d-152">Laukā **Nosaukums** ievadiet vērtību. </span><span class="sxs-lookup"><span data-stu-id="2390d-152">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="2390d-153">Laukā **Režīms** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="2390d-153">In the **Mode** field, select an option.</span></span>
6. <span data-ttu-id="2390d-154">Atlasiet **Jā** laukā **Izmantot esošo darbu**.</span><span class="sxs-lookup"><span data-stu-id="2390d-154">Select **Yes** in the **Use existing work** field.</span></span>
7. <span data-ttu-id="2390d-155">Atlasiet **Jā** laukā **Ģenerēt licences numura zīmi**.</span><span class="sxs-lookup"><span data-stu-id="2390d-155">Select **Yes** in the **Generate license plate** field.</span></span>
8. <span data-ttu-id="2390d-156">Izvērtiet sadaļu **Darba klases**.</span><span class="sxs-lookup"><span data-stu-id="2390d-156">Expand the **Work classes** section.</span></span>
9. <span data-ttu-id="2390d-157">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="2390d-157">Select **New**.</span></span>
10. <span data-ttu-id="2390d-158">Laukā **Darba klases ID** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="2390d-158">In the **Work class ID** field, type a value.</span></span>
11. <span data-ttu-id="2390d-159">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="2390d-159">Select **Save**.</span></span>
12. <span data-ttu-id="2390d-160">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2390d-160">Close the page.</span></span>
13. <span data-ttu-id="2390d-161">Dodieties uz **Navigācijas rūts > Moduļi > Noliktavas pārvaldība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlne**.</span><span class="sxs-lookup"><span data-stu-id="2390d-161">Go to **navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
14. <span data-ttu-id="2390d-162">Kokā atlasiet to izvēlnes vienumu, kuru izveidojāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="2390d-162">In the tree, select the menu item that you created before.</span></span>
15. <span data-ttu-id="2390d-163">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="2390d-163">Select **Edit**.</span></span>
16. <span data-ttu-id="2390d-164">Atlasiet bultu, lai izvēlnei pievienotu izvēlnes vienumu.</span><span class="sxs-lookup"><span data-stu-id="2390d-164">Select the arrow to add the menu item to the menu.</span></span>
17. <span data-ttu-id="2390d-165">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="2390d-165">Select **Save**.</span></span>
18. <span data-ttu-id="2390d-166">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2390d-166">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="2390d-167">Atjaunināt darba veidni</span><span class="sxs-lookup"><span data-stu-id="2390d-167">Update a work template</span></span>
1. <span data-ttu-id="2390d-168">Dodieties uz **Navigācijas rūts > Moduļi > Noliktavas pārvaldība > Iestatīšana> Darbs > Darba veidnes**.</span><span class="sxs-lookup"><span data-stu-id="2390d-168">Go to **Navigation pane > Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="2390d-169">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="2390d-169">Select **Edit**.</span></span>
3. <span data-ttu-id="2390d-170">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="2390d-170">Select **New**.</span></span>
4. <span data-ttu-id="2390d-171">Laukā **Darba tips** atlasiet **Drukāt**.</span><span class="sxs-lookup"><span data-stu-id="2390d-171">In the **Work type** field, select **Print**.</span></span>
5. <span data-ttu-id="2390d-172">Laukā **Darba klases ID** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="2390d-172">In the **Work class ID** field, enter or select a value.</span></span>
6. <span data-ttu-id="2390d-173">Atlasiet **Pārvietot uz augšu**.</span><span class="sxs-lookup"><span data-stu-id="2390d-173">Select **Move up**.</span></span>
7. <span data-ttu-id="2390d-174">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="2390d-174">Select **Save**.</span></span>
8. <span data-ttu-id="2390d-175">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2390d-175">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]