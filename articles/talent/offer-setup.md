---
title: Piedāvājumu pārvaldības iestatīšana programmā Attract
description: Šajā tēmā ir aprakstīts, kā iestatīt piedāvājumus programmā Microsoft Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc91a83afd5ce1627376685bcf612d6998ddbc02
ms.sourcegitcommit: 5022d63a81c3715c9a3dcf2a68217bb6b17c7805
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2019
ms.locfileid: "2890559"
---
# <a name="set-up-offer-management-in-attract"></a><span data-ttu-id="1b3e4-103">Piedāvājumu pārvaldības iestatīšana programmā Attract</span><span class="sxs-lookup"><span data-stu-id="1b3e4-103">Set up offer management in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1b3e4-104">Kad kandidāts tiek pārvietots uz piedāvājuma posmu programmā Dynamics 365 Talent: Attract, ir jānodrošina, ka var ātri izveidot kandidātam paredzētos piedāvājumus, pēc nepieciešamības tos apstiprināt un nosūtīt attiecīgajam kandidātam.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-104">When a candidate is moved to the offer stage in Dynamics 365 Talent: Attract, you need to ensure that the offers can be quickly created for the candidate, approved as necessary, and sent out to the candidate.</span></span> <span data-ttu-id="1b3e4-105">Tā kā lielākā daļa piedāvājumu ir standarta piedāvājumi, tos var izveidot no atkārtoti izmantojamām veidnēm.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-105">Because most offers are standard, they can be created from reusable templates.</span></span> <span data-ttu-id="1b3e4-106">Programmā Attract visi piedāvājumi tiek apkopoti piedāvājumu paketē, kas ir kolekcija no viena vai vairākiem piedāvājumu dokumentiem.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-106">In Attract, all offers are rolled into an offer package, which is a collection of one or more offer documents.</span></span> 

<span data-ttu-id="1b3e4-107">Šajā tēmā ir uzskaitītas visas darbības, kas Attract administratoram būtu jāizpilda, lai kā daļu no piedāvājumu pārvaldības iespējām programmā Attract iesaistītu dažādas piedāvājumu pakotņu veidnes.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-107">This topic lists all the steps that an Attract administrator would follow to set up different offer package templates as part of the offer management capability in Attract.</span></span> <span data-ttu-id="1b3e4-108">Lietotājiem, kuriem nav administratora lomas, nav piekļuves šīm iespējām.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-108">Users with non-administrator roles will not have access to these capabilities.</span></span>

>[!NOTE]
> <span data-ttu-id="1b3e4-109">Piedāvājumu pārvaldības iespējas ir pieejamas kā daļa no visaptverošās darbā pieņemšanas pievienojumprogrammas.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-109">Offer management capabilities are available as part of the Comprehensive Hiring Add-On.</span></span>

## <a name="offer-data"></a><span data-ttu-id="1b3e4-110">Piedāvājuma dati</span><span class="sxs-lookup"><span data-stu-id="1b3e4-110">Offer data</span></span> 

<span data-ttu-id="1b3e4-111">Piedāvājuma dati ir vismazākā vienība piedāvājumu pakotnes veidnē.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-111">Offer data is the smallest unit inside the offer package template.</span></span> <span data-ttu-id="1b3e4-112">Tipisks piedāvājums sastāv no standarta teksta un vērtību kopas.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-112">A typical offer consists of standard text and a set of values.</span></span> <span data-ttu-id="1b3e4-113">Vērtību kopas ir vienīgās daļas, kas dažādos piedāvājumos var mainīties.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-113">The sets of values are the only pieces that could change between offers.</span></span> <span data-ttu-id="1b3e4-114">Piedāvājuma izveidošanas laikā vissvarīgākais aspekts, uz ko piedāvājuma izveidotājs var koncentrēties, ir saraksts ar piedāvājuma datu vietturiem, kas atrodas piedāvājumu pakotnes veidnē.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-114">During the offer creation, the most important aspect that the offer creator can focus on is the list of offer data placeholders present in an offer package template.</span></span> <span data-ttu-id="1b3e4-115">Lai iestatītu piedāvājuma datus, izpildiet tālāk aprakstītos norādījumus.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-115">To set up offer data, do the following.</span></span>

1.  <span data-ttu-id="1b3e4-116">Dodieties uz **Piedāvājumu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-116">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="1b3e4-117">Kreisajā navigācijas rūtī izvērsiet sadaļu **Bibliotēka** un pēc tam dodieties uz **Piedāvājuma dati**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-117">Expand the **Library** section in the left navigation pane, then go to **Offer data**.</span></span>

    >[!NOTE]
    > <span data-ttu-id="1b3e4-118">Lapā **Piedāvājuma dati** ir sadaļas **Kandidāta informācija** un **Darba informācija**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-118">On the **Offer data** page are the **Candidate details** and **Job details** sections.</span></span> <span data-ttu-id="1b3e4-119">Attract nodrošina dažus piedāvājuma datu vietturus jau standarta komplektācijā.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-119">Attract provides a few offer data placeholders out-of-the-box.</span></span>
    > 
    > <span data-ttu-id="1b3e4-120">Lapā ir sadaļas, kas ir paredzētas dažādu piedāvājuma datu vietturu sakārtošanai loģiskās grupās.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-120">There are sections on the page to organize different offer data placeholders together in logical groups.</span></span> <span data-ttu-id="1b3e4-121">Šīs sadaļas var noderēt saistībā ar piedāvājuma datu uzturēšanu un datu aizpildīšanu piedāvājuma izveidošanas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-121">These sections can help with maintenance of offer data and population of data during the offer creation process.</span></span>
    > 
    > <span data-ttu-id="1b3e4-122">Lai izveidotu viettura vērtību sarakstu, augšupielādējiet Excel izklājlapu, kurā ir viena kolonna ar vietturi kā kolonnas virsraksts un izvēļu saraksts apakšā esošajās rindās.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-122">To create a list of values for a placeholder, upload an Excel spreadsheet that has one column with the placeholder as the column title and the list of choices in the rows underneath.</span></span> <span data-ttu-id="1b3e4-123">Ja viens un tas pats vietturis ir atsauce citā datu kārtulu kopā, pārliecinieties, vai tām ir vienota vērtību kopa.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-123">If the same placeholder is referenced in another data rule set, ensure they have a common set of values.</span></span>
    
1.  <span data-ttu-id="1b3e4-124">Lai izveidotu jaunu piedāvājuma datu sadaļu, noklikšķiniet uz **Pievienot sadaļu** un ievadiet unikālu nosaukumu šai sadaļai.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-124">To create a new offer data section, click **Add a section** and enter a unique name for the section.</span></span>

1.  <span data-ttu-id="1b3e4-125">Lai jebkurai sadaļai pievienotu piedāvājuma datu vietturus, noklikšķiniet uz **Pievienot piedāvājuma datus** un ievadiet unikālu nosaukumu šim vietturim.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-125">To add offer data placeholders to any section, click **Add offer data** and enter a unique name for the placeholder.</span></span>

1.  <span data-ttu-id="1b3e4-126">Lai rediģētu jebkuras sadaļas nosaukumu, virziet peles kursoru virs sadaļas nosaukuma un atjauniniet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-126">To edit the name of any section, hover over the section name and update the name.</span></span>

1.  <span data-ttu-id="1b3e4-127">Lai rediģētu jebkuru esošu piedāvājuma datu viettura nosaukumu, vispirms pārliecinieties, vai šis vietturis vēl neveido daļu no kādas veidnes.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-127">To edit the name of any existing offer data placeholder, first make sure that the placeholder is not already part of any template.</span></span> <span data-ttu-id="1b3e4-128">Pēc tam virziet peles kursoru virs piedāvājuma datu viettura nosaukuma un pēc nepieciešamības atjauniniet šo nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-128">Then, hover over the name of the offer data placeholder and update the name as needed.</span></span>

1. <span data-ttu-id="1b3e4-129">Lai dzēstu esošu piedāvājuma datu vietturi, vispirms pārliecinieties, vai šis vietturis neveido daļu no kādas citas veidnes.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-129">To delete an existing offer data placeholder, first make sure that the placeholder is not part of any other template.</span></span> <span data-ttu-id="1b3e4-130">Pēc tam virziet peles kursoru virs viettura un, kad kļūst redzama atkritnes ikona, noklikšķiniet uz atkritnes, lai dzēstu šo piedāvājuma datu vietturi.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-130">Then, hover over the placeholder and when the trash can icon appears, click the trash can to delete the offer data placeholder.</span></span>
    >[!NOTE]
    > <span data-ttu-id="1b3e4-131">Varat redzēt, cik veidnēs ietilpst kāds piedāvājuma datu vietturis — šis skaits tiek rādīts blakus katra piedāvājuma datiem.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-131">You can see how many templates an offer data placeholder is part of by the number indicator next to each offer data.</span></span> 

1. <span data-ttu-id="1b3e4-132">Lai dzēstu jebkuru sadaļu, virziet peles kursoru virs tās nosaukuma.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-132">To delete any section, hover over the name.</span></span> <span data-ttu-id="1b3e4-133">Ja neviens no sadaļā esošajiem piedāvājuma datu vietturiem nav redzams nevienā veidnē, varat noklikšķināt uz atkritnes ikonas, lai to dzēstu.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-133">If none of the offer data placeholders inside the section appear in any template, you can click the trash can icon to delete it.</span></span> 
    >[!NOTE]
    > <span data-ttu-id="1b3e4-134">Dzēšot sadaļu, tiek dzēsti arī visi piedāvājuma datu vietturi šajā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-134">Deleting the section will also delete all the offer data placeholders inside that section.</span></span>

<span data-ttu-id="1b3e4-135">Pēc piedāvājuma datu vietturu iestatīšanas tos varat izmantot jebkurā dokumenta veidnē.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-135">After the offer data placeholders have been set up, you can use them across any document template.</span></span> <span data-ttu-id="1b3e4-136">Piedāvājuma datu vietturi nav ierobežoti tikai noteiktā veidnē — to pašu kopu var izmantot visās veidnēs.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-136">Offer data placeholders are not restricted to a specific template -- the same set can be used across all templates.</span></span>

## <a name="offer-data-rules"></a><span data-ttu-id="1b3e4-137">Piedāvājuma datu kārtulas</span><span class="sxs-lookup"><span data-stu-id="1b3e4-137">Offer data rules</span></span>

<span data-ttu-id="1b3e4-138">Vairumam organizāciju ir kārtulas, kas nosaka piedāvājumu izveidošanu.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-138">Most organization have rules for how offers must be created.</span></span> <span data-ttu-id="1b3e4-139">Piemēram, organizācija var vēlēties pieprasīt, lai maksimālās gada algas piedāvājums noteiktai atrašanās vietas un darba stāža līmeņa kombinācijai būtu noteiktā diapazonā vai lai būtu iespējamas tikai dažas konkrētas vērtības piedāvājuma līmenim attiecībā uz nesen nolīgtu darbinieku.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-139">For example, an organization may want to require that the maximum annual salary offer for a specific location and seniority level combination has to be within a certain range, or that there are only a few specific values possible for the offer level for the new hire.</span></span> <span data-ttu-id="1b3e4-140">Pašlaik Attract atbalsta visas šādas datu kārtulas, izmantojot CSV failu.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-140">Attract currently supports all such data rules using a CSV file.</span></span>

<span data-ttu-id="1b3e4-141">Lai sagatavotu datu kārtulu CSV failu, izpildiet tālāk aprakstītos norādījumus.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-141">To prepare the data rules CSV file, do the following.</span></span>

1.  <span data-ttu-id="1b3e4-142">Nosakiet piedāvājuma datu vietturi kārtulu kopai.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-142">Determine the offer data placeholder for the rule set.</span></span> <span data-ttu-id="1b3e4-143">Piemēram, **Gada alga**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-143">For example, **Annual Salary**.</span></span>

1.  <span data-ttu-id="1b3e4-144">Identificējiet pakārtoto piedāvājuma datu vietturu vērtības.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-144">Identify the dependent offer data placeholder values.</span></span> <span data-ttu-id="1b3e4-145">Piemēram, **Darba atrašanās vieta** un **Līmenis**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-145">For example, **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="1b3e4-146">Norādiet 1. un 2. kolonnu kā **Darba atrašanās vieta** un **Līmenis**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-146">Specify columns 1 and 2 as **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="1b3e4-147">Lai augšupielādētu diapazona vērtību, nosaukumu **Gada alga** piešķiriet gan 3., gan 4. kolonnai.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-147">To upload a range value, make columns 3 and 4 **Annual Salary**.</span></span> <span data-ttu-id="1b3e4-148">Lai augšupielādētu konkrētu vērtību, nevis diapazonu, nosaukumu **Gada alga** piešķiriet tikai 3. kolonnai.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-148">To upload a specific value instead of a range, only make column 3 **Annual Salary**.</span></span>

1.  <span data-ttu-id="1b3e4-149">Aizpildiet Microsoft Excel failu, pamatojoties uz nepieciešamajām lomām.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-149">Populate the Microsoft Excel file based on your required roles.</span></span>

1.  <span data-ttu-id="1b3e4-150">Pārliecinieties, vai katrā rindā ir unikāla kombinācija no visām vērtībām kopā.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-150">Ensure that each row is a unique combination of all the values put together.</span></span>

1.  <span data-ttu-id="1b3e4-151">Saglabājiet failu kā CSV formāta failu.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-151">Save the file as a CSV format.</span></span>

<span data-ttu-id="1b3e4-152">Lai augšupielādētu piedāvājuma datu kārtulu failu, izpildiet tālāk aprakstītos norādījumus.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-152">To upload the offer data rules file, do the following.</span></span>

1.  <span data-ttu-id="1b3e4-153">Dodieties uz **Piedāvājumu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-153">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="1b3e4-154">Kreisajā navigācijas panelī izvērsiet sadaļu **Bibliotēka** un pēc tam dodieties uz **Piedāvājuma dati kārtulas**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-154">Expand the **Library** section in the left navigation panel, then go to **Offer data rules**.</span></span>

1.  <span data-ttu-id="1b3e4-155">Noklikšķiniet uz **Jauna datu kopa**, lai parādītu dialoglodziņu **Augšupielādēt**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-155">Click **New data set** to display the **Upload** dialog box.</span></span>

1.  <span data-ttu-id="1b3e4-156">Norādiet unikālu nosaukumu šai kārtulu kopai un pēc tam augšupielādējiet saglabāto CSV failu.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-156">Specify a unique name for the rule set and then upload the saved CSV file.</span></span>

1.  <span data-ttu-id="1b3e4-157">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-157">Click **Add**.</span></span>
    <span data-ttu-id="1b3e4-158">Kārtulu kopa tiks apstrādāta fonā, un pēc apstrādes pabeigšanas jums tiks paziņots programmā un pa e-pastu.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-158">The rule set will be processed in the background and you will be notified in-app and via email once it completes.</span></span>

    <span data-ttu-id="1b3e4-159">Jums tiks paziņots, ja augšupielādes apstrādāšanas laikā būs radušās kļūdas.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-159">You will be notified if there are errors while processing the upload.</span></span> <span data-ttu-id="1b3e4-160">Pēc tam varat lejupielādējiet kļūdu žurnālfailu, izlabot failu un augšupielādēt to vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-160">You can then download the error log, fix the file, and upload it again.</span></span>

1.  <span data-ttu-id="1b3e4-161">Izmantojiet daudzpunktes pogas (**...**) opciju, ja vēlaties lejupielādēt kārtulu kopu un atjaunināt šo vērtību kopu.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-161">Use the ellipses button (**…**) option if you want to download the rule set and update the set of values.</span></span> <span data-ttu-id="1b3e4-162">Pēc atjaunināšanas varat šo failu augšupielādēt vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-162">After updating, you can upload the file again.</span></span>

1.  <span data-ttu-id="1b3e4-163">Esošu kārtulu kopas augšupielādi varat dzēst, ja definētais vietturis netiek izmantots nevienā citā dokumenta veidnē.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-163">You can delete an existing rule set upload if the placeholder being defined is not being used in another document template.</span></span>

>[!NOTE]
> - <span data-ttu-id="1b3e4-164">Katram vietturim var būt tikai viena unikāla kolonnu kopa, no kuras tas ir atkarīgs.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-164">Each placeholder can only have one unique set of columns that it is dependent on.</span></span> <span data-ttu-id="1b3e4-165">Piemēram, ja vietturis **Gada alga** ir atkarīgs no vērtības kolonnā **Darba atrašanās vieta** un kolonnā **Līmenis**, jūs nevarat augšupielādēt citu kārtulu kopu, kur vietturis **Gada alga** ir atkarīgs no citas kolonnu kopas.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-165">For example, if **Annual Salary** is dependent on **Job Location** and **Level**, you can't upload another rule set where **Annual Salary** is dependent on a different set of columns.</span></span>

> - <span data-ttu-id="1b3e4-166">Lapas **Piedāvājuma datu kārtulas** cilnē **Paraugi** varat lejupielādēt piedāvājuma datu kārtulu kopu paraugus.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-166">You can download sample offer data rule sets on the **Samples** tab on the **Offer data rules** page.</span></span>

> - <span data-ttu-id="1b3e4-167">Ja piedāvājuma izveidotājs pārraksta piedāvājuma datu kārtulu ieteiktās vērtības, šis piedāvājums tiek atzīmēts ar karodziņu kā nestandarta un tiek atļauta piedāvājuma apstiprināšanas darbplūsma.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-167">When an offer creator overrides the values that are recommended by the offer data rules, the offer is flagged as non-standard and offer approval workflow will be mandated.</span></span>

## <a name="document-templates"></a><span data-ttu-id="1b3e4-168">Dokumentu veidnes</span><span class="sxs-lookup"><span data-stu-id="1b3e4-168">Document templates</span></span>

<span data-ttu-id="1b3e4-169">Piedāvājuma dokumenta veidne administratoriem var noderēt piedāvājumu vēstuļu izveidošanai.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-169">An offer document template can help administrators create offer letters.</span></span> <span data-ttu-id="1b3e4-170">Piedāvājuma dokumenta veidne sastāv no teksta, kas būs daļa no piedāvājuma, un no definētajiem piedāvājuma datu vietturiem.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-170">The offer document template is a combination of the text that will be part of the offer as well as the defined offer data placeholders.</span></span> 

<span data-ttu-id="1b3e4-171">Lai izveidotu piedāvājuma dokumenta veidni, izpildiet tālāk aprakstītos norādījumus.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-171">To create an offer document template, do the following.</span></span>

1.  <span data-ttu-id="1b3e4-172">Dodieties uz **Piedāvājumu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-172">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="1b3e4-173">Kreisajā navigācijas rūtī izvērsiet sadaļu **Bibliotēka** un dodieties uz **Veidnes**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-173">Expand the **Library** section in the left navigation pane and go to **Templates**.</span></span>

    <span data-ttu-id="1b3e4-174">Lapā **Veidnes** tiek rādīts saraksts ar jau definētajām dokumentu veidnēm.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-174">The **Templates** page will display a list of document templates that have already been defined.</span></span>

1.  <span data-ttu-id="1b3e4-175">Lai izveidotu jaunu dokumenta veidni, noklikšķiniet uz **Jauna veidne**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-175">To create a new document template, click **New Template**.</span></span>

1.  <span data-ttu-id="1b3e4-176">Ievadiet unikālu nosaukumu šai veidnei un noklikšķiniet uz **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-176">Enter a unique name for the template and click **Create**.</span></span>

1.  <span data-ttu-id="1b3e4-177">Izmantojiet bagātinātā teksta redaktoru, lai ievietotu vai rediģētu piedāvājuma dokumenta saturu.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-177">Use the rich text editor to insert or edit the offer document content.</span></span> <span data-ttu-id="1b3e4-178">Varat ievietot tabulas, attēlus un hipersaites, izmantojot teksta redaktora augšpusē pieejamās opcijas.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-178">You can insert tables, images, and hyperlinks using the options available at the top of the text editor.</span></span>

1.  <span data-ttu-id="1b3e4-179">Piedāvājuma veidnes dokumentā varat ievietot piedāvājuma datu vietturus, izmantojot tālāk aprakstītās metodes.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-179">You can insert offer data placeholders in the offer template document by:</span></span>

    - <span data-ttu-id="1b3e4-180">Velkot un nometot no labās rūts.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-180">Dragging and dropping from the right pane.</span></span>

    - <span data-ttu-id="1b3e4-181">Ievietojot piedāvājuma datu viettura atsauces tagu tieši nepieciešamajā pozīcijā.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-181">Hashtag the offer data placeholder directly into position.</span></span> <span data-ttu-id="1b3e4-182">Ierakstiet **\#** un pēc tam sāciet rakstīt piedāvājuma datu viettura nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-182">Type **\#** and then start typing the name of the offer data placeholder.</span></span> <span data-ttu-id="1b3e4-183">Tiks parādīts nolaižamais saraksts ar opcijām.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-183">Options will appear in the drop-down list.</span></span> <span data-ttu-id="1b3e4-184">Noklikšķiniet vai nospiediet taustiņu **Enter**, lai ievietotu piedāvājuma datu vietturi.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-184">Click or press **Enter** to insert the offer data placeholder.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="1b3e4-185">Lai vietturi saistītu ar piedāvājuma dokumenta veidni, neizpaužot tā vērtību kandidātam, virziet peles kursoru virs piedāvājuma datu viettura un noklikšķiniet uz ikonas **Piespraust**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-185">To associate a placeholder to the offer document template without exposing its value to the candidate, hover over the offer data placeholder and click the **Pin** icon.</span></span> <span data-ttu-id="1b3e4-186">Šādi vietturis tiks pārbīdīts uz piedāvājuma dokumenta veidnes sadaļu **Piespraustie piedāvājuma dati**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-186">This will push the placeholder to the **Pinned offer data** section of the offer document template.</span></span> <span data-ttu-id="1b3e4-187">Lai atspraustu, izpildiet tās pašas darbības, bet piedāvājuma datu vietturu sarakstā noklikšķiniet uz **Atspraust**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-187">To unpin, follow the same steps but click **Unpin** in the list of offer data placeholders.</span></span>

    > - <span data-ttu-id="1b3e4-188">Lai skatītu sarakstu ar aktīvajiem piedāvājuma datu vietturiem, labajā rūtī pārslēdziet uz cilni **Aktīvs**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-188">To view the list of active offer data placeholders, switch to the **Active** tab in the right pane.</span></span>

    > - <span data-ttu-id="1b3e4-189">Ja ievietojat vietturi, kas ir atvasināts no kādas piedāvājuma datu kārtulu kopas, varat redzēt šī piedāvājuma datu viettura atkarību no citām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-189">If you insert a placeholder that is driven by an offer data rule set, you can see the dependency of that offer data placeholder on other values.</span></span>

    > - <span data-ttu-id="1b3e4-190">Ja vēlaties, saturu no .docx faila varat **Importēt** savā lokālajā mašīnā un pēc nepieciešamības to rediģēt.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-190">Alternatively, you can **Import** the content from a .docx file on your local machine and edit as required.</span></span> <span data-ttu-id="1b3e4-191">Tādējādi jums redaktorā nav jāieraksta viss saturs.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-191">That way, you don’t have to type in all the content in the editor.</span></span>

1. <span data-ttu-id="1b3e4-192">Lai priekšskatītu piedāvājuma dokumentu, izmantojiet opciju **Priekšskatīt** lapas augšpusē.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-192">To preview the offer document, use the **Preview** option at the top of the page.</span></span>

1. <span data-ttu-id="1b3e4-193">Lai kontrolētu, vai piedāvājuma veidotājs var rediģēt piedāvājuma dokumenta saturu, izmantojiet opciju **Pārvaldīt atļauju** lapas augšdaļā.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-193">To control whether an offer creator can edit the offer document content, use the **Manage permission** option at the top of the page.</span></span> <span data-ttu-id="1b3e4-194">Ja piedāvājuma izveidotājam vēlaties ļaut tikai ievietot vietturu vērtības, nevis rediģēt tekstu, atļaujas vērtība ir jāiestata uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-194">If you want the offer creator to only insert placeholder values and not edit text, set the permission value to **No**.</span></span>

1. <span data-ttu-id="1b3e4-195">Noklikšķiniet uz **Saglabāt**, lai saglabātu savu progresu.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-195">Click **Save** to save your progress.</span></span> <span data-ttu-id="1b3e4-196">Veidne tiks saglabāta melnraksta stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-196">The template will be saved in a draft state.</span></span>

1. <span data-ttu-id="1b3e4-197">Lai finalizētu un atzīmētu dokumentu kā publicētu, noklikšķiniet uz **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-197">To finalize and mark the document as published, click **Finish**.</span></span>

1. <span data-ttu-id="1b3e4-198">Varat redzēt, kuras dokumentu veidnes pašlaik ir aktīvas, kuras atrodas melnraksta režīmā, un kuras ir arhivētas un vairs netiek izmantotas dokumentu veidņu bibliotēkas izvietošanas funkcionalitātē.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-198">You can see which document templates are currently active, in draft mode, and have been archived and are no longer in use on the document templates library landing experience.</span></span>

>[!NOTE]
> <span data-ttu-id="1b3e4-199">Varat dzēst jebkuru piedāvājuma dokumenta veidni, kas neveido daļu no esošas piedāvājuma pakotnes veidnes.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-199">You can delete any offer document template that is not part of an existing offer package template.</span></span>


## <a name="offer-package-templates"></a><span data-ttu-id="1b3e4-200">Piedāvājuma pakotņu veidnes</span><span class="sxs-lookup"><span data-stu-id="1b3e4-200">Offer package templates</span></span>

<span data-ttu-id="1b3e4-201">Piedāvājuma pakotnes ir piedāvājuma artefakti, kas tiek koplietoti ar kandidātu un sastāv no vienas piedāvājuma veidnes vai vairāku piedāvājuma veidņu kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-201">Offer packages are the offer artifacts that are shared with the candidate and consist of a combination of one or more offer document templates.</span></span> <span data-ttu-id="1b3e4-202">Lai izveidotu piedāvājuma pakotni, izpildiet tālāk aprakstītos norādījumus.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-202">To create an offer package, do the following.</span></span>

1.  <span data-ttu-id="1b3e4-203">Dodieties uz **Piedāvājumu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-203">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="1b3e4-204">No kreisās navigācijas rūts dodieties uz **Pakotnes**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-204">Go to **Packages** from the left navigation pane.</span></span>

    <span data-ttu-id="1b3e4-205">Tiek parādīts saraksts ar aktīvajām pakotnes veidnēm, kas piedāvājumu veidotājiem ir pieejamas lietošanai.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-205">A list of active package templates that are available for offer creators to use is displayed.</span></span>

1.  <span data-ttu-id="1b3e4-206">Lai izveidotu jaunu piedāvājuma pakotni, noklikšķiniet uz **Jauna pakotne**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-206">To create a new offer package, click **New Package**.</span></span>

1.  <span data-ttu-id="1b3e4-207">Ievadiet unikālu nosaukumu un noklikšķiniet uz **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-207">Enter a unique name and click **Create**.</span></span>

1.  <span data-ttu-id="1b3e4-208">Noklikšķiniet uz **Pievienot veidni**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-208">Click **Add template**.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="1b3e4-209">Varat izvēlēties izveidot jaunu veidni vai izvēlēties kādu no esošajām.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-209">You can choose to create a new template or choose from an existing one.</span></span>

    > - <span data-ttu-id="1b3e4-210">Ja izvēlaties pievienot esošu veidni, jums ir jāpārliecinās, vai piedāvājuma dokumenta veidne bija saglabāta, finalizēta un atzīmēta kā aktīva.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-210">If you choose to add an existing template, you need to make sure that the   offer document template was saved, finalized, and marked as   active.</span></span>
    
    > - <span data-ttu-id="1b3e4-211">Varat izvēlēties jebkādu skaitu dokumenta veidņu.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-211">You can choose as many document templates as you want.</span></span> 
    
1.  <span data-ttu-id="1b3e4-212">Noklikšķiniet uz **Gatavs**, lai atgrieztos sadaļā **Pakotņu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-212">Click **Done** to return to **Package management**.</span></span>

    <span data-ttu-id="1b3e4-213">Varat konfigurēt dokumentu sēriju un varat arī atzīmēt, vai konkrētais piedāvājuma dokuments ir nepieciešams piedāvājuma izveidošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-213">You can configure the sequence of the documents and also mark whether the specific offer document is required during offer creation.</span></span> <span data-ttu-id="1b3e4-214">Piedāvājumu veidotājam būs opcija dzēst dokumentus, kas ir atzīmēti kā **Nav nepieciešams**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-214">The offer creator will have an option to delete the documents marked as **Not required**.</span></span>

1. <span data-ttu-id="1b3e4-215">Lai saglabātu piedāvājuma pakotnes veidni tā, ka to var izmantot visi piedāvājumu veidotāji, noklikšķiniet uz **Saglabāt un publicēt**.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-215">To save the offer package template so that it's usable by all offer creators, click **Save and publish**.</span></span>

   <span data-ttu-id="1b3e4-216">Lai skatītu melnraksta piedāvājuma pakotņu veidnes, dodieties uz cilni **Melnraksti**. Ja piedāvājuma pakotnes veidnē tiek veiktas kādas izmaiņas, tā ir jāsaglabā un jāpublicē atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-216">To view draft offer package templates, go to the **Drafts** tab. If a change is made to the offer package template, it must be  saved and republished.</span></span>

## <a name="configure-an-offer-process"></a><span data-ttu-id="1b3e4-217">Piedāvājuma procesa konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="1b3e4-217">Configure an offer process</span></span>

<span data-ttu-id="1b3e4-218">Piedāvājuma veidošanas procesā ir vairākas daļas, kuras var konfigurēt Attract administrators.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-218">There are several parts of the offer creation process that can be configured by an Attract administrator.</span></span>

- <span data-ttu-id="1b3e4-219">**Piedāvājumu apstiprinājumi** — izvēlieties, vai piedāvājumi ir jāapstiprina, pirms tie tiek nosūtīti kandidātam.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-219">**Offer approvals** - Choose whether offer approvals are required before the offer can be sent to the candidate.</span></span> <span data-ttu-id="1b3e4-220">Kā administrators jūs varat arī izlemt, vai visiem piedāvājumu apstiprinājumiem ir jānotiek secīgā vai paralēlā apstiprināšanas darbplūsmā.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-220">As an administrator, you can also decide whether all offer approvals will happen in a sequential manner or parallel approval workflow.</span></span> <span data-ttu-id="1b3e4-221">Varat arī norādīt, vai piedāvājumu apstiprinātājiem kopā ar savu piedāvājuma apstiprinājumu ir jāpievieno arī komentārs.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-221">You can also mandate whether offer approvers must add a comment along with their offer approval.</span></span> <span data-ttu-id="1b3e4-222">Piedāvājumu apstiprinājumi ir obligāti visiem nestandarta piedāvājumiem.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-222">Offer approvals are mandatory for all non-standard offers.</span></span>

- <span data-ttu-id="1b3e4-223">**Kandidāta piedāvājuma pieredze** — kā administrators varat izvēlēties iestatīt, vai visiem piedāvājumiem ir beigu datums un — ja tāds ir — kādai ir jābūt beigu datuma noklusējuma nobīdei.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-223">**Candidate’s offer experience** - As administrator, you can choose to set whether all offers have an expiration date, and if so, what the default offset for the expiration date should be.</span></span> <span data-ttu-id="1b3e4-224">Varat arī konfigurēt to, vai kandidāti var noraidīt kādu piedāvājumu.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-224">You can also configure whether candidates can decline an offer.</span></span>

- <span data-ttu-id="1b3e4-225">**Elektroniskie paraksti** — kā administrators varat arī izvēlēties metodi, kuru kandidātiem izmantot, lai parakstītu piedāvājumus.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-225">**e-Signatures** - As an administrator, you can also choose the method that candidates can use to sign offers.</span></span>
    - <span data-ttu-id="1b3e4-226">Adobe Sign — visas piedāvājumu pakotnes tiks nosūtītas un parakstītas, izmantojot Adobe Sign.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-226">Adobe Sign - All offer packages will be sent and signed via Adobe Sign.</span></span> <span data-ttu-id="1b3e4-227">Katram piedāvājumu izveidotājam, kurš publicē piedāvājumu, ir nepieciešams programmai Attract piesaistīts Adobe Sign konts.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-227">Each offer creator publishing the offer needs to have their Adobe Sign account connected to Attract.</span></span> <span data-ttu-id="1b3e4-228">Lai iegūtu Adobe Sign licenci bezmaksas izmēģinājumversiju, noklikšķiniet uz šīs [saites](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span><span class="sxs-lookup"><span data-stu-id="1b3e4-228">For Adobe Sign licenses and a free Trial, please visit this [link](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span></span>

    - <span data-ttu-id="1b3e4-229">DocuSign — visas piedāvājumu pakotnes tiks nosūtītas un parakstītas, izmantojot DocuSign.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-229">DocuSign - All offer packages will be sent and signed via DocuSign.</span></span> <span data-ttu-id="1b3e4-230">Katram piedāvājumu izveidotājam, kurš publicē piedāvājumu, ir nepieciešams programmai Attract piesaistīts DocuSign konts.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-230">Each offer creator publishing the offer needs to have their DocuSign account connected to Attract.</span></span> 
    
    - <span data-ttu-id="1b3e4-231">ESign — šī ir standarta komplektācijā iekļautā noklusējuma opcija, ar kuru lietotājs var parakstīt piedāvājumu, ievadot savu vārdu un iniciāļus.</span><span class="sxs-lookup"><span data-stu-id="1b3e4-231">ESign - This is the default option, provided out of the box, where the user can sign an offer by typing their name and initials.</span></span>


<span data-ttu-id="1b3e4-232">Plašāku informāciju par piedāvājuma izveidošanas procesu skatiet [Piedāvājumu izveide, apstiprināšana un parakstīšana](./creating-offers.md).</span><span class="sxs-lookup"><span data-stu-id="1b3e4-232">To learn more about the offer creation process, see [Create, approve, and sign offers](./creating-offers.md).</span></span>
