---
title: Projekta resursu iestatīšana
description: Šajā tēmā sniegta informācija par projekta resursu iestatīšanu vai pieprasīšanu.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760608"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="a4447-103">Projekta resursu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a4447-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4447-104">Ir jāiestata kalendārs un jāsaista tas ar darbinieku vai nodarbināto.</span><span class="sxs-lookup"><span data-stu-id="a4447-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="a4447-105">Kalendārs tiek izmantots, lai plānotu projektu un projektam rezervēto resursu darba laiku.</span><span class="sxs-lookup"><span data-stu-id="a4447-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="a4447-106">Kalendāra iestatīšanas laikā projektu vadītāji resursu optimizēšanas ietvaros var veikt resursu izlīdzināšanu.</span><span class="sxs-lookup"><span data-stu-id="a4447-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="a4447-107">Pamatojoties uz kalendāra grafiku, resursiem var noteikt ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="a4447-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="a4447-108">Kalendāru varat iestatīt lapā **Kalendāri**.</span><span class="sxs-lookup"><span data-stu-id="a4447-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="a4447-109">Kad kādu nodarbināto iestatāt kā projekta resursu, varat atlasīt no nodarbinātajiem, kuri strādā uzņēmumā, kam iestatāt resursus.</span><span class="sxs-lookup"><span data-stu-id="a4447-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="a4447-110">Varat arī atlasīt nodarbinātos no citiem uzņēmumiem jūsu organizācijā.</span><span class="sxs-lookup"><span data-stu-id="a4447-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="a4447-111">Šie nodarbinātie tiek saukti par starpuzņēmumu resursiem.</span><span class="sxs-lookup"><span data-stu-id="a4447-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="a4447-112">Tālāk sniegtajos procedūru aprakstos ir paskaidrots, kā nodarbināto iestatīt kā projekta resursu jūsu uzņēmumā un kā iestatīt starpuzņēmumu projekta resursu.</span><span class="sxs-lookup"><span data-stu-id="a4447-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="a4447-113">Nodarbinātā kā projekta resursa iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a4447-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="a4447-114">Lapas **Darbinieki** sarakstā **Nodarbinātie** atlasiet nodarbināto, kuru pievienojat kā projekta resursu, un atveriet nodarbinātā ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a4447-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="a4447-115">Darbību rūtī atlasiet **Projekts** &gt; **Iestatījumi** &gt; **Projektu iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="a4447-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="a4447-116">Atlasiet kalendāru un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="a4447-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="a4447-117">Jūs varat arī norādīt resursam noklusējuma projektus kā iepriekšēju piešķiri.</span><span class="sxs-lookup"><span data-stu-id="a4447-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="a4447-118">Iepriekšējas piešķires var izmantot, ja resursu pārvaldnieks vai projektu vadītājs iepriekš zina, kurā projektā resurss veiks darbu.</span><span class="sxs-lookup"><span data-stu-id="a4447-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="a4447-119">Iepriekšējas piešķires arī var balstīties uz projekta sponsora vai debitora pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="a4447-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="a4447-120">Lai veiktu projekta iepriekšēju piešķiri, lapas **Piešķirt projektus** cilnes **Projekti** sarakstā **Atlikušie projekti** atlasiet attiecīgo projektu.</span><span class="sxs-lookup"><span data-stu-id="a4447-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="a4447-121">Starpuzņēmumu resursa iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a4447-121">Set up an intercompany resource</span></span>

<span data-ttu-id="a4447-122">Kad nodarbināto iestatāt kā starpuzņēmumu resursu, iestatīšana ir jāveic gan patapināšanas uzņēmumā, gan piesaistīšanas uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="a4447-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="a4447-123">Patapināšanas uzņēmumā</span><span class="sxs-lookup"><span data-stu-id="a4447-123">In the lending company</span></span>

1. <span data-ttu-id="a4447-124">Programmā Finance pārbaudiet, vai ir atlasīts patapināšanas uzņēmums, un pēc tam veiciet iepriekšējā sadaļā “Nodarbinātā kā projekta resursa iestatīšana” aprakstīto procedūru.</span><span class="sxs-lookup"><span data-stu-id="a4447-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="a4447-125">Lapā **Starpuzņēmumu uzskaite** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="a4447-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="a4447-126">Laukā **Juridiskās personas ID** atlasiet patapināšanas uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="a4447-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="a4447-127">Aizpildiet pārējos laukus ar atbilstošu informāciju un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="a4447-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="a4447-128">Lapā **Transfertcena** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="a4447-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="a4447-129">Laukā **Piesaistīšanas juridiskā persona** atlasiet atbilstošo uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="a4447-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="a4447-130">Lai piesaistīšanas uzņēmumam aizdotu tikai to resursu, kuru izveidojāt šīs sadaļas sākumā, laukā **Resurss** atlasiet izveidotā resursa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="a4447-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="a4447-131">Lai piesaistīšanas uzņēmumam būtu pieejami visi patapināšanas uzņēmuma resursi, lauks **Resurss** ir jāatstāj tukšs.</span><span class="sxs-lookup"><span data-stu-id="a4447-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="a4447-132">Lapā **Projektu vadības un uzskaites parametri**, cilnē **Starpuzņēmumu** opciju **Aktivizēt starpuzņēmumu resursu plānošanu un laika grafikus** iestatiet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="a4447-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="a4447-133">Piesaistīšanas uzņēmumā</span><span class="sxs-lookup"><span data-stu-id="a4447-133">In the borrowing company</span></span>

- <span data-ttu-id="a4447-134">Lapā **Resursu saraksts**, meklēšanas filtrā ievadiet tā resursu nosaukumu, kuru izveidojāt patapināšanas uzņēmumam, lai pārbaudītu, vai šis nosaukums ir ietverts piesaistīšanas uzņēmuma resursu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="a4447-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="a4447-135">Projekta resursu pieprasīšana</span><span class="sxs-lookup"><span data-stu-id="a4447-135">Request project resources</span></span>
<span data-ttu-id="a4447-136">Projekta resursu plānošanas funkcionalitāte resursu pārvaldniekiem pa piesaistēm vai projektiem ļauj sadalīt tikai nokomplektētos resursus.</span><span class="sxs-lookup"><span data-stu-id="a4447-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="a4447-137">Lai iespējoto šo funkcionalitāti, izpildiet tālāk norādītos uzdevumus vai pārliecinieties, ka tie jau ir izpildīti.</span><span class="sxs-lookup"><span data-stu-id="a4447-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="a4447-138">Iestatiet numuru sērijas.</span><span class="sxs-lookup"><span data-stu-id="a4447-138">Set up number sequences.</span></span>
- <span data-ttu-id="a4447-139">Iestatiet projektu vadības un uzskaites darbplūsmas.</span><span class="sxs-lookup"><span data-stu-id="a4447-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="a4447-140">Iespējojiet resursu pieprasījumu darbplūsmas.</span><span class="sxs-lookup"><span data-stu-id="a4447-140">Enable resource request workflows.</span></span>

<span data-ttu-id="a4447-141">Kad iepriekš norādītie uzdevumi ir izpildīti, pēc nepieciešamības varat izpildīt tālāk norādītos uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="a4447-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="a4447-142">Izveidojiet resursa pieprasījumu, izmantojot viegli rezervētu personāla resursu.</span><span class="sxs-lookup"><span data-stu-id="a4447-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="a4447-143">Pārraugiet resursu pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="a4447-143">Monitor resource requests.</span></span>
- <span data-ttu-id="a4447-144">Izpildiet resursu pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="a4447-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="a4447-145">Pieprasiet nokomplektētu resursu no WBS.</span><span class="sxs-lookup"><span data-stu-id="a4447-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="a4447-146">Rezervējiet projektam resursus bez nepieciešamības pieprasīt nokomplektētu resursu.</span><span class="sxs-lookup"><span data-stu-id="a4447-146">Book resources to a project without having a request for a staffed resource.</span></span>
