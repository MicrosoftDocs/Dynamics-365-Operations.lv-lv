---
title: Budžeta plānošanas attaisnojuma dokumenti
description: Attaisnojuma dokumenti sniedz skaidrojumu tiem, kas budžetam pieprasa paskaidrot, kādēļ ir nepieciešams kāds noteikts budžets.
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 321da6643b421070ddd9f32bddd3e8d72f0adb86
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445713"
---
# <a name="budget-planning-justification-documents"></a><span data-ttu-id="6d73b-103">Budžeta plānošanas attaisnojuma dokumenti</span><span class="sxs-lookup"><span data-stu-id="6d73b-103">Budget planning justification documents</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d73b-104">Attaisnojuma dokumenti sniedz skaidrojumu tiem, kas budžetam pieprasa paskaidrot, kādēļ ir nepieciešams kāds noteikts budžets.</span><span class="sxs-lookup"><span data-stu-id="6d73b-104">Justification documents provide a narrative for those requesting a budget to explain why a specific budget is necessary.</span></span> 

<span data-ttu-id="6d73b-105">Budžeta pārvaldnieks izveido budžeta plāna veidni programmā Microsoft Word, un tā tiek piešķirta pašreizējam budžeta plānošanas procesam.</span><span class="sxs-lookup"><span data-stu-id="6d73b-105">A budget plan template is created by the budget manager in Microsoft Word and assigned to the current budget planning process.</span></span> <span data-ttu-id="6d73b-106">Pēc tam budžeta īpašnieki šo veidni var atvērt un likt datus automātiski aizpildīt programmā Word, pamatojoties uz to budžeta pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="6d73b-106">Budget owners can then open the template and have data automatically populated in Word based on their budget request.</span></span> <span data-ttu-id="6d73b-107">Pēc tam viņi var pievienot papildu tekstu vai datus, pirms savu personalizēto attaisnojuma dokumentu saglabā un pievieno budžeta plānam.</span><span class="sxs-lookup"><span data-stu-id="6d73b-107">They can then add additional text or data prior to saving and attaching their personalized justification document to their budget plan.</span></span>

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a><span data-ttu-id="6d73b-108">Microsoft Dynamics Office pievienojumprogrammas iestatīšana programmai Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="6d73b-108">Set up Microsoft Dynamics Office Add-in for Microsoft Word</span></span>

1.  <span data-ttu-id="6d73b-109">Atveriet jaunu Microsoft Word dokumentu.</span><span class="sxs-lookup"><span data-stu-id="6d73b-109">Open a new Microsoft Word document.</span></span>
2.  <span data-ttu-id="6d73b-110">Lentē noklikšķiniet uz **Ievietot** un noklikšķiniet uz **Veikals**.</span><span class="sxs-lookup"><span data-stu-id="6d73b-110">Click **Insert** on the ribbon, and click **Store**.</span></span>
3.  <span data-ttu-id="6d73b-111">Meklējiet Microsoft Dynamics Office pievienojumprogrammu un noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="6d73b-111">Search for Microsoft Dynamics Office Add-in and click **Add**.</span></span>
4.  <span data-ttu-id="6d73b-112">Programmā Word, labajā rūtī noklikšķiniet uz **Pievienot servera informāciju**.</span><span class="sxs-lookup"><span data-stu-id="6d73b-112">In Word, in the right pane, click **Add server information**.</span></span>
5.  <span data-ttu-id="6d73b-113">Ierakstiet vai ielīmējiet servera vietrādi URL un noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d73b-113">Type or paste the server URL and click **OK**.</span></span>

##### <a name="define-the-justification-template-in-microsoft-word"></a><span data-ttu-id="6d73b-114">Līdzināšanas veidnes definēšana programmā Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="6d73b-114">Define the Justification template in Microsoft Word</span></span>

1.  <span data-ttu-id="6d73b-115">Pēc pierakstīšanās Microsoft Dynamics Office pievienojumprogrammā noklikšķiniet uz **Dizains**.</span><span class="sxs-lookup"><span data-stu-id="6d73b-115">Click **Design** in the Microsoft Dynamics Office Add-in after you’ve logged in.</span></span>
2.  <span data-ttu-id="6d73b-116">Galvenes informācijai izmantojiet pogu **Pievienot laukus**.</span><span class="sxs-lookup"><span data-stu-id="6d73b-116">For header information, use the **Add fields** button.</span></span>
3.  <span data-ttu-id="6d73b-117">Atlasiet BudgetPlanJustification elementa datu avotu un noklikšķiniet uz **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="6d73b-117">Select the entity data source of BudgetPlanJustification, and click **Next**.</span></span> <span data-ttu-id="6d73b-118">**Piezīme.** Šis elements ir nepieciešams visiem attaisnojuma dokumentiem.</span><span class="sxs-lookup"><span data-stu-id="6d73b-118">**Note:** This entity is required for any justification document.</span></span> <span data-ttu-id="6d73b-119">Var izmantot citus elementus, taču, ja nav ietverts šis elements, neizdodas augšupielāde atpakaļ programmā Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="6d73b-119">Other entities can be used but the upload back to Microsoft Dynamics 365 Finance will fail if this entity isn’t included.</span></span>
4.  <span data-ttu-id="6d73b-120">Word dokumentā pievienojiet etiķetes un vērtības BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter un DocumentNumber.</span><span class="sxs-lookup"><span data-stu-id="6d73b-120">Add the BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter, and DocumentNumber labels and values in the Word document.</span></span> <span data-ttu-id="6d73b-121">**Piezīme.** Ja nepieciešams, varat izmantot pats savas pielāgotās etiķetes, nevis standarta etiķetes.</span><span class="sxs-lookup"><span data-stu-id="6d73b-121">**Note:** You can use your own custom labels, rather than the standard labels, if needed.</span></span>
5.  <span data-ttu-id="6d73b-122">Lai pabeigtu galvenes atlasi, noklikšķiniet uz **Gatavs**.</span><span class="sxs-lookup"><span data-stu-id="6d73b-122">Click **Done** to complete the header section.</span></span>
6.  <span data-ttu-id="6d73b-123">Rindas līmeņa informācijai par budžeta plāna summām noklikšķiniet uz **Pievienot tabulu**.</span><span class="sxs-lookup"><span data-stu-id="6d73b-123">For line level detail of budget plan amounts, click **Add table**.</span></span>
7.  <span data-ttu-id="6d73b-124">Atkal atlasiet BudgetPlanJustification elementa datu avotu un noklikšķiniet uz **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="6d73b-124">Again, select the entity data source of BudgetPlanJustification, and click **Next**.</span></span>
8.  <span data-ttu-id="6d73b-125">Pievienojiet laukus vērtībām EffectiveDate, ScenarioName, AccountDisplayValue un AccountingCurrencyExpenseAmount.</span><span class="sxs-lookup"><span data-stu-id="6d73b-125">Add fields for EffectiveDate, ScenarioName, AccountDisplayValue, and AccountingCurrencyExpenseAmount.</span></span> <span data-ttu-id="6d73b-126">**Piezīme.** Ja atsevišķās budžeta plāna rindās pievienošanai ir pieejami komentāri, šeit tos varat pievienot tabulai.</span><span class="sxs-lookup"><span data-stu-id="6d73b-126">**Note:** If comments are available to add within individual budget plan lines, those can be added to the table here.</span></span>
9.  <span data-ttu-id="6d73b-127">Pievienojiet visus papildu norādījumus, ko sniegt lietotājam, un veiciet dokumentam visu nepieciešamo formatēšanu vai stila mainīšanu.</span><span class="sxs-lookup"><span data-stu-id="6d73b-127">Add any additional instructions to provide to the end user, and perform any necessary formatting or styling to the document.</span></span>
10. <span data-ttu-id="6d73b-128">Saglabājiet dokumentu lokālajā datorā un aizveriet failu, pirms turpināt.</span><span class="sxs-lookup"><span data-stu-id="6d73b-128">Save the document to your local computer and close the file before continuing.</span></span>

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a><span data-ttu-id="6d73b-129">Iestatīt budžeta plānošanas procesu attaisnojuma veidnes lietošanai</span><span class="sxs-lookup"><span data-stu-id="6d73b-129">Set up the Budget planning process to use the Justification template</span></span>

1.  <span data-ttu-id="6d73b-130">Pārejiet uz sadaļu **Budžeta veidošana** &gt; **Iestatīšana** &gt; **Budžeta plānošana** &gt; **Attaisnojuma dokumenta veidnes**.</span><span class="sxs-lookup"><span data-stu-id="6d73b-130">Go to **Budgeting** &gt; **Setup** &gt; **Budget planning** &gt; **Justification document templates**.</span></span>
2.  <span data-ttu-id="6d73b-131">Noklikšķiniet uz **Jauns** un pārlūkojiet līdz jaunizveidotajam Microsoft Word dokumentam.</span><span class="sxs-lookup"><span data-stu-id="6d73b-131">Click **New** and browse to your newly created Microsoft Word document.</span></span>
3.  <span data-ttu-id="6d73b-132">Ievadiet veidnes parādāmo nosaukumu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="6d73b-132">Enter a template display name and description.</span></span> <span data-ttu-id="6d73b-133">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6d73b-133">Click **OK**.</span></span>
4.  <span data-ttu-id="6d73b-134">Dodieties uz **Budžeta veidošana** &gt; **Iestatīšana** &gt; **Budžeta** **plānošana** &gt; **Budžeta plānošanas process**.</span><span class="sxs-lookup"><span data-stu-id="6d73b-134">Go to **Budgeting** &gt; **Setup** &gt; **Budget** **planning** &gt; **Budget planning process**.</span></span>
5.  <span data-ttu-id="6d73b-135">Atlasiet procesu, kurā ir jālieto attaisnojuma veidne, un noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="6d73b-135">Select the process where the justification template should be used, and click **Edit**.</span></span>
6.  <span data-ttu-id="6d73b-136">Laukā **Attaisnojuma dokumenta veidne** atlasiet atbilstošo veidni un saglabājiet.</span><span class="sxs-lookup"><span data-stu-id="6d73b-136">In the **Justification document template** field, select the appropriate template and save.</span></span>

##### <a name="edit-and-save-personalized-justification-documents"></a><span data-ttu-id="6d73b-137">Rediģēt un saglabāt personalizētus attaisnojuma dokumentus</span><span class="sxs-lookup"><span data-stu-id="6d73b-137">Edit and save personalized justification documents</span></span>

1.  <span data-ttu-id="6d73b-138">Izveidot jaunu budžeta plānu vai atveriet esošu budžeta plānu.</span><span class="sxs-lookup"><span data-stu-id="6d73b-138">Create a new budget plan or open an existing budget plan.</span></span>
2.  <span data-ttu-id="6d73b-139">Nolaižamajā izvēlnē **Attaisnojums** atlasiet vienumu **Izveidot jaunu attaisnojumu**.</span><span class="sxs-lookup"><span data-stu-id="6d73b-139">In the **Justification** drop-down menu, select **Create new justification**.</span></span>
3.  <span data-ttu-id="6d73b-140">Pēc informācijas aizpildīšanas izvēlieties augšupielādēt personalizēto dokumentu no nolaižamās izvēlnes **Attaisnojums**.</span><span class="sxs-lookup"><span data-stu-id="6d73b-140">After filling in the details, select to upload the personalized document from the **Justification** drop-down menu.</span></span>




