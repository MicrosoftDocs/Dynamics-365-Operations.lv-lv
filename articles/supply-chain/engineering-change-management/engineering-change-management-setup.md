---
title: Izveidot kopīgas vērtības tehnisko izmaiņu pārvaldībai
description: Šajā tēmā ir aprakstīts, kā izveidot kopīgas vērtības, kas tiek izmantotas parametriem dažādās tehnisko izmaiņu pārvaldības daļās.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductParameters, EngChgEcmSeverityTable, EngChgEcmSeverityRuleSet, EngChgEcmSeverityLookup,EngChgEcmSeverityChart,EngChgEcmRequestSeverityChart,EngChgEcmPriorityTable, EngChgEcmPriorityLookup, EngChgEcmPriorityChart, EngChgEcmMaterialDisposition, EngChgEcmEH
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: ee2be7d59f327876b92386c66433aeaf06df489c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5262361"
---
# <a name="establish-common-values-for-engineering-change-management"></a><span data-ttu-id="b490f-103">Izveidot kopīgas vērtības tehnisko izmaiņu pārvaldībai</span><span class="sxs-lookup"><span data-stu-id="b490f-103">Establish common values for engineering change management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b490f-104">Iestatot tehnisko izmaiņu pārvaldību, ir jāizveido vairākas vērtību kolekcijas, kas tiks izmantotas, lai aizpildītu nolaižamos sarakstus citās lietotāja interfeisa (UI) daļās.</span><span class="sxs-lookup"><span data-stu-id="b490f-104">When you set up engineering change management, you must establish several collections of values that will be used to fill in drop-down lists in other parts of the user interface (UI).</span></span> <span data-ttu-id="b490f-105">Šīs vērtības ir jānorāda atbilstoši ražoto produktu veidiem un konkrētajām biznesa vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="b490f-105">You should specify these values according to the types of products that you produce and your specific business needs.</span></span>

## <a name="engineering-change-categories"></a><span data-ttu-id="b490f-106">Tehnisko izmaiņu kategorijas</span><span class="sxs-lookup"><span data-stu-id="b490f-106">Engineering change categories</span></span>

<span data-ttu-id="b490f-107">Izmantojiet tehnisko izmaiņu kategorijas, lai organizētu tehnisko izmaiņu pasūtījumus, lai tos būtu vieglāk pārvaldīt un pārskatīt.</span><span class="sxs-lookup"><span data-stu-id="b490f-107">You use engineering change categories to organize your engineering change orders, so that they are easier to manage and review.</span></span> <span data-ttu-id="b490f-108">Piemēram, var būt noderīgi iestatīt darbplūsmu, kurā atkarībā no kategorijas konkrētai nodaļai ir jāpārskata piedāvātās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="b490f-108">For example, you might find it useful to set up a workflow where, depending on the category, a specific department must review the proposed changes.</span></span> <span data-ttu-id="b490f-109">Tāpēc tehnisko izmaiņu pasūtījumā ir ietverts lauks **Kategorija**.</span><span class="sxs-lookup"><span data-stu-id="b490f-109">Therefore, the engineering change order includes a **Category** field.</span></span>

<span data-ttu-id="b490f-110">Lai izveidotu to tehnisko izmaiņu kategoriju apkopojumu, kas tiek izmantotas jūsu uzņēmumā, dodieties uz **Tehnisko izmaiņu pārvaldība \> Iestatīšana \> Tehnisko izmaiņu pārvaldība \> Tehnisko izmaiņu kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="b490f-110">To establish the collection of engineering change categories that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change categories**.</span></span> <span data-ttu-id="b490f-111">Pēc tam var izmantot darbību rūts pogas, lai pievienotu, noņemtu un rediģētu vērtības un sakārtotu tās secībā, kādā tās ir redzamas nolaižamajos sarakstos, kur tās tiek rādītas.</span><span class="sxs-lookup"><span data-stu-id="b490f-111">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="engineering-change-priorities"></a><span data-ttu-id="b490f-112">Tehnisko izmaiņu prioritātes</span><span class="sxs-lookup"><span data-stu-id="b490f-112">Engineering change priorities</span></span>

<span data-ttu-id="b490f-113">Varat izmantot tehnisko izmaiņu prioritātes, lai norādītu tehnisko izmaiņu secības svarīgumu vai steidzamību.</span><span class="sxs-lookup"><span data-stu-id="b490f-113">You use engineering change priorities to indicate the importance or urgency of an engineering change order.</span></span> <span data-ttu-id="b490f-114">Tās palīdz izsekot tehnisko izmaiņu pasūtījuma nozīmīgumu, lai varētu viegli identificēt, kuri pasūtījumi vispirms jāapstrādā, un cik ātri.</span><span class="sxs-lookup"><span data-stu-id="b490f-114">They can help you keep track of the importance of an engineering change order, so that you can easily identify which orders should be processed first, and how quickly.</span></span>

<span data-ttu-id="b490f-115">Lai izveidotu to tehnisko izmaiņu prioritāšu apkopojumu, kas tiek izmantotas jūsu uzņēmumā, dodieties uz **Tehnisko izmaiņu pārvaldība \> Iestatīšana \> Tehnisko izmaiņu pārvaldība \> Tehnisko izmaiņu prioritātes**.</span><span class="sxs-lookup"><span data-stu-id="b490f-115">To establish the collection of engineering change priorities that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change priorities**.</span></span> <span data-ttu-id="b490f-116">Pēc tam var izmantot darbību rūts pogas, lai pievienotu, noņemtu un rediģētu vērtības un sakārtotu tās secībā, kādā tās ir redzamas nolaižamajos sarakstos, kur tās tiek rādītas.</span><span class="sxs-lookup"><span data-stu-id="b490f-116">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="engineering-change-reasons"></a><span data-ttu-id="b490f-117">Tehnisku izmaiņu iemesli</span><span class="sxs-lookup"><span data-stu-id="b490f-117">Engineering change reasons</span></span>

<span data-ttu-id="b490f-118">Tehnisko izmaiņu iemesli norāda mainītā pasūtījuma izmaiņu iemeslu vai būtību.</span><span class="sxs-lookup"><span data-stu-id="b490f-118">Engineering change reasons indicate the cause or nature of the change in the change order.</span></span>

<span data-ttu-id="b490f-119">Lai izveidotu to tehnisko izmaiņu iemeslu apkopojumu, kas tiek izmantoti jūsu uzņēmumā, dodieties uz **Tehnisko izmaiņu pārvaldība \> Iestatīšana \> Tehnisko izmaiņu pārvaldība \> Tehnisko izmaiņu iemesli**.</span><span class="sxs-lookup"><span data-stu-id="b490f-119">To establish the collection of engineering change reasons that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change reasons**.</span></span> <span data-ttu-id="b490f-120">Pēc tam var izmantot darbību rūts pogas, lai pievienotu, noņemtu un rediģētu vērtības un sakārtotu tās secībā, kādā tās ir redzamas nolaižamajos sarakstos, kur tās tiek rādītas.</span><span class="sxs-lookup"><span data-stu-id="b490f-120">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="material-disposal-codes"></a><span data-ttu-id="b490f-121">Materiālu izvietojumu kodi</span><span class="sxs-lookup"><span data-stu-id="b490f-121">Material disposal codes</span></span>

<span data-ttu-id="b490f-122">Materiālu likvidēšanas kodi tiek izmantoti, lai kategorizētu materiālus, kas tiek izmantoti pabeigtiem produktiem, vai komponentiem, kas ir jālikvidē noteiktā veidā vai, kas prasa zināmu apstrādi, pirms tos var pievienot jūsu parastajai miskastei.</span><span class="sxs-lookup"><span data-stu-id="b490f-122">You use material disposal codes to categorize materials that are used in your finished goods, or components that must be disposed of in a specific way or require some treatment before they can be added to your regular trash.</span></span> <span data-ttu-id="b490f-123">Kad pievienojat attiecīgo produktu tehnisko izmaiņu pasūtījumam, varat piešķirt likvidēšanas kodu kā daļu no izmaiņu detalizētās informācijas.</span><span class="sxs-lookup"><span data-stu-id="b490f-123">When you add a relevant product to an engineering change order, you can assign a disposal code as part of the change details.</span></span>

<span data-ttu-id="b490f-124">Lai izveidotu to materiālu likvidēšanas kodu apkopojumu, kas tiek izmantoti jūsu uzņēmumā, dodieties uz **Tehnisko izmaiņu pārvaldība \> Iestatīšana \> Tehnisko izmaiņu pārvaldība \> Materiālu likvidēšanas kodi**.</span><span class="sxs-lookup"><span data-stu-id="b490f-124">To establish the collection of material disposal codes that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Material disposal codes**.</span></span> <span data-ttu-id="b490f-125">Pēc tam var izmantot darbību rūts pogas, lai pievienotu, noņemtu un rediģētu vērtības un sakārtotu tās secībā, kādā tās ir redzamas nolaižamajos sarakstos, kur tās tiek rādītas.</span><span class="sxs-lookup"><span data-stu-id="b490f-125">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="received-customer-approval"></a><span data-ttu-id="b490f-126">Saņemts klienta apstiprinājums</span><span class="sxs-lookup"><span data-stu-id="b490f-126">Received customer approval</span></span>

<span data-ttu-id="b490f-127">Projektējot produktus konkrētam klientam, dizains un specifikācijas bieži ir jāapstiprina, pirms produktu var iestatīt kā gatavu.</span><span class="sxs-lookup"><span data-stu-id="b490f-127">When you design products for a specific customer, the design and specifications often must be validated before the product can be set as ready.</span></span> <span data-ttu-id="b490f-128">Lauks **Saņemtais klienta apstiprinājums** ļauj norādīt, cik tālu klientu apstiprināšanas procesā produkts ir un/vai apstiprinājums ir saņemts.</span><span class="sxs-lookup"><span data-stu-id="b490f-128">The **Received customer approval** field lets you indicate how far in the customer approval process the product is and/or whether the approval has been received.</span></span>

<span data-ttu-id="b490f-129">Lai izveidotu to saņemto klientu apstiprinājumu vērtību apkopojumu, kas tiek izmantoti jūsu uzņēmumā, dodieties uz **Tehnisko izmaiņu pārvaldība \> Iestatīšana \> Tehnisko izmaiņu pārvaldība \> Saņemtais klientu apstiprinājums**.</span><span class="sxs-lookup"><span data-stu-id="b490f-129">To establish the collection of received customer approval values that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Received customer approval**.</span></span> <span data-ttu-id="b490f-130">Pēc tam var izmantot darbību rūts pogas, lai pievienotu, noņemtu un rediģētu vērtības un sakārtotu tās secībā, kādā tās ir redzamas nolaižamajos sarakstos, kur tās tiek rādītas.</span><span class="sxs-lookup"><span data-stu-id="b490f-130">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="engineering-change--environmental-health-and-safety-codes"></a><span data-ttu-id="b490f-131">Tehniskā izmaiņa — vides veselības un drošības kodi</span><span class="sxs-lookup"><span data-stu-id="b490f-131">Engineering change – Environmental health and safety codes</span></span>

<span data-ttu-id="b490f-132">Ja, ražojot produktus, ir jāņem vērā kādi standarta vides veselības un drošības noteikumi, vai uzņēmumam raksturīgi noteikumi vai procedūras, varat izmantot vides veselības un drošības kodus, lai tos definētu.</span><span class="sxs-lookup"><span data-stu-id="b490f-132">If any standard environmental health and safety regulations, or company-specific regulations or procedures, must be considered in the manufacture of a product, you can use the environmental health and safety codes to define them.</span></span> <span data-ttu-id="b490f-133">Tehnsko izmaiņu pasūtījumā varat norādīt, kurus kodus piemērot produkta ražošanai, rediģējot ietekmētā produkta informāciju.</span><span class="sxs-lookup"><span data-stu-id="b490f-133">In the engineering change order, you can indicate which codes apply to the manufacture of a product while you edit the details of the affected product.</span></span>

<span data-ttu-id="b490f-134">Lai izveidotu to veselības un drošības vērtību apkopojumu, kas tiek izmantotas jūsu uzņēmumā, dodieties uz **Tehnisko izmaiņu pārvaldība \> Iestatīšana \> Tehnisko izmaiņu pārvaldība \> Vides veselības un drošības kodi**.</span><span class="sxs-lookup"><span data-stu-id="b490f-134">To establish the collection of health and safety values that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change - Environmental health and safety codes**.</span></span> <span data-ttu-id="b490f-135">Pēc tam var izmantot darbību rūts pogas, lai pievienotu, noņemtu un rediģētu vērtības un sakārtotu tās secībā, kādā tās ir redzamas nolaižamajos sarakstos, kur tās tiek rādītas.</span><span class="sxs-lookup"><span data-stu-id="b490f-135">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="engineering-change-severities"></a><span data-ttu-id="b490f-136">Tehnisko izmaiņu nozīmīgums</span><span class="sxs-lookup"><span data-stu-id="b490f-136">Engineering change severities</span></span>

<span data-ttu-id="b490f-137">Tiek izmantotas tehnisko izmaiņu pakāpes, lai norādītu ietekmes līmeni, kas attiecas uz produktiem tehnisko izmaiņu pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="b490f-137">You use engineering change severities to indicate the level of impact that applies to the products in an engineering change order.</span></span>

<span data-ttu-id="b490f-138">Lai izveidotu to tehnisko izmaiņu stingrības apkopojumu, kas tiek izmantotas jūsu uzņēmumā, dodieties uz **Tehnisko izmaiņu pārvaldība \> Iestatīšana \> Tehnisko izmaiņu pārvaldība \> Tehnisko izmaiņu stingrība**.</span><span class="sxs-lookup"><span data-stu-id="b490f-138">To establish the collection of engineering change severities that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change severities**.</span></span> <span data-ttu-id="b490f-139">Pēc tam var izmantot darbību rūts pogas, lai pievienotu, noņemtu un rediģētu vērtības un sakārtotu tās secībā, kādā tās ir redzamas nolaižamajos sarakstos, kur tās tiek rādītas.</span><span class="sxs-lookup"><span data-stu-id="b490f-139">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

<span data-ttu-id="b490f-140">Varat izveidot noteikumus, kas attiecas uz katru izveidoto stingrības līmeni.</span><span class="sxs-lookup"><span data-stu-id="b490f-140">You can establish rules that apply to each severity level that you create.</span></span> <span data-ttu-id="b490f-141">Plašāku informāciju par šo noteikumu piešķiršanu skatiet nākamajā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="b490f-141">For more information about how to assign these rules, see the next section.</span></span>

## <a name="engineering-change-severity-rule-sets"></a><span data-ttu-id="b490f-142">Tehnisko izmaiņu nozīmīguma kārtulu kopas</span><span class="sxs-lookup"><span data-stu-id="b490f-142">Engineering change severity rule sets</span></span>

<span data-ttu-id="b490f-143">Lai izveidotu noteikumu grupu, ko varat izmantot, lai automātiski aprēķinātu izmaiņu pasūtījuma smagumu, pamatojoties uz ietekmēto produktu izmaiņu veidu, izmantojiet tehnisko izmaiņu stingrības noteikumu kopas.</span><span class="sxs-lookup"><span data-stu-id="b490f-143">You use engineering change severity rule sets to establish a group of rules that you can use to automatically calculate the severity of the change order, based on the type of changes in the affected products.</span></span> <span data-ttu-id="b490f-144">Lai izmantotu stingrības nosacījumus, atveriet lapu **Tehnisko izmaiņu pārvaldības parametri** un iestatiet lauku **Stingrības noteikums** uz *Aprēķināt* vai *Automātiski aprēķināt*.</span><span class="sxs-lookup"><span data-stu-id="b490f-144">To use the severity rules, open the **Engineering change management parameters** page, and set the **Severity rule** field to *Calculate* or *Calculate automatically*.</span></span>

<span data-ttu-id="b490f-145">Kad sistēma novērtē stingrību, tā apstrādā kārtulas tādā secībā, kādā tās parādās lapā, no sākuma līdz beigām.</span><span class="sxs-lookup"><span data-stu-id="b490f-145">When the system evaluates severity, it processes the rules in the order in which they appear on the page, from top to bottom.</span></span> <span data-ttu-id="b490f-146">Lai kārtula tiktu atlasīta un tās prioritāte tiktu noteikta, ir jāizpilda visas noteikumu kopas kārtulas.</span><span class="sxs-lookup"><span data-stu-id="b490f-146">For a rule to be selected and have its priority established, all the rules in a rule set must be met.</span></span>

<span data-ttu-id="b490f-147">Lai iestatītu noteikumus, kas attiecas uz katru norādītās izmaiņas stingrības līmeni, dodieties uz **Tehnisko izmaiņu pārvaldība \> Iestatīšana \> Tehnisko izmaiņu pārvaldība \> Tehnisko izmaiņu stingrības noteikumu kopas**.</span><span class="sxs-lookup"><span data-stu-id="b490f-147">To set up the rules that apply to each change severity level that you've defined, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change severity rule sets**.</span></span> <span data-ttu-id="b490f-148">Pēc tam izpildiet kādu no norādītajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="b490f-148">Then follow one of these steps.</span></span>

- <span data-ttu-id="b490f-149">Lai izveidotu noteikumu kopu, darbības rūtī atlasiet **Jauns** un pēc tam iestatiet laukus, kā aprakstīts tālāk šajā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="b490f-149">To create a new rule set, select **New** on the Action Pane, and then set the fields as described later in this section.</span></span>
- <span data-ttu-id="b490f-150">Lai rediģētu esošu noteikumu kopu, atlasiet to saraksta rūtī, atlasiet **Rediģēt** darbību rūtī un pēc tam iestatiet laukus, kā aprakstīts tālāk šajā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="b490f-150">To edit an existing rule set, select it in the list pane, select **Edit** on the Action Pane, and then set the fields as described later in this section.</span></span>
- <span data-ttu-id="b490f-151">Lai dzēstu esošu noteikumu kopu, atlasiet to saraksta rūtī un pēc tam darbības rūtī atlasiet vienumu **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="b490f-151">To delete an existing rule set, select it in the list pane, and then select **Delete** on the Action Pane.</span></span>
- <span data-ttu-id="b490f-152">Lai pārkārtotu noteikumu kopu sarakstu, atlasiet noteikumu kopu saraksta rūtī un pēc tam izmantojiet pogas **Uz augšu** un **Uz leju** darbības rūtī, lai mainītu tās novietojumu.</span><span class="sxs-lookup"><span data-stu-id="b490f-152">To rearrange the list of rule sets, select a rule set in the list pane, and then use the **Up** and **Down** buttons on the Action Pane to reposition it.</span></span>

<span data-ttu-id="b490f-153">Katrai noteikumu kopai iestatiet tālāk norādīto lauku.</span><span class="sxs-lookup"><span data-stu-id="b490f-153">For each rule set, set the following field:</span></span>

- <span data-ttu-id="b490f-154">**Stingrība** – Atlasiet stingrības līmeni, lai izveidotu noteikumus.</span><span class="sxs-lookup"><span data-stu-id="b490f-154">**Severity** – Select the severity level to establish rules for.</span></span> <span data-ttu-id="b490f-155">Lai izveidotu un nosauktu līmeņus, izmantojiet lapu **Tehnisko izmaiņu stingrība**.</span><span class="sxs-lookup"><span data-stu-id="b490f-155">You use the **Engineering change severities** page to create and name the levels.</span></span> <span data-ttu-id="b490f-156">(Papildinformāciju skatiet iepriekšējā sadaļā.)</span><span class="sxs-lookup"><span data-stu-id="b490f-156">(For more information, see the previous section.)</span></span>

<span data-ttu-id="b490f-157">Izmantojiet pogas kopsavilkuma cilnē **Kārtulas**, lai pievienotu vai noņemtu kārtulu pašreizējam stingrības iestatījumam.</span><span class="sxs-lookup"><span data-stu-id="b490f-157">Use the buttons on the **Rules** FastTab to add or remove a rule for the current severity setting.</span></span> <span data-ttu-id="b490f-158">Katrai kārtulai ir lauks **Kārtula** un lauks **Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="b490f-158">Each rule has a **Rule** field and a **Name** field.</span></span> <span data-ttu-id="b490f-159">Šos noteikumus nosaka sistēma, un tajos ir norādīti produkta iespējamo izmaiņu veidi.</span><span class="sxs-lookup"><span data-stu-id="b490f-159">The rules are established by the system and indicate the types of changes that a product can have.</span></span> <span data-ttu-id="b490f-160">Nosaukums norāda izmaiņu veidu.</span><span class="sxs-lookup"><span data-stu-id="b490f-160">The name indicates the type of change.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]