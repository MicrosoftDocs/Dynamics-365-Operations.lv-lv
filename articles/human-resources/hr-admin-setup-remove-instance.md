---
title: Noņemt instanci
description: Šajā rakstā ir detalizēti aprakstīts, kā noņemt izmēģinājuma vai ražošanas vidi Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 17f299f81d1326dfb06c11a6125acc54b8ef2a6e
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431203"
---
# <a name="remove-an-instance"></a><span data-ttu-id="c3719-103">Noņemt instanci</span><span class="sxs-lookup"><span data-stu-id="c3719-103">Remove an instance</span></span>

<span data-ttu-id="c3719-104">Šajā rakstā ir detalizēti aprakstīts, kā noņemt izmēģinājuma vai ražošanas vidi Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c3719-104">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="c3719-105">Izmēģinājuma vides noņemšana</span><span class="sxs-lookup"><span data-stu-id="c3719-105">Remove a test drive environment</span></span>

<span data-ttu-id="c3719-106">Human Resources izmēģinājuma vides tiek nodrošinātas, izmantojot 60 dienu derīguma termiņa politiku.</span><span class="sxs-lookup"><span data-stu-id="c3719-106">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="c3719-107">Taču izmēģinājuma vides īpašnieki var ātrāk beigt izmēģinājumu, veicot tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="c3719-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="c3719-108">Pāriet uz [Power Apps Administrēšanas centru](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="c3719-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="c3719-109">Atlasiet **Vides**.</span><span class="sxs-lookup"><span data-stu-id="c3719-109">Select **Environments**.</span></span>
3. <span data-ttu-id="c3719-110">Atlasiet izmēģinājuma vidi, kuras nosaukuma formāts līdzinās šim: TestDrive — aizstājvārds@domēns.</span><span class="sxs-lookup"><span data-stu-id="c3719-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="c3719-111">Atlasiet **Dzēst** un apstipriniet dzēšanu.</span><span class="sxs-lookup"><span data-stu-id="c3719-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="c3719-112">Esošā izmēģinājuma vide tiek noņemta.</span><span class="sxs-lookup"><span data-stu-id="c3719-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="c3719-113">Kad tā ir noņemta, jūs varat reģistrēties jaunas izmēģinājuma vides saņemšanai.</span><span class="sxs-lookup"><span data-stu-id="c3719-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="c3719-114">Ražošanas vides noņemšana</span><span class="sxs-lookup"><span data-stu-id="c3719-114">Remove a production environment</span></span>

<span data-ttu-id="c3719-115">Šajā rakstā tiek pieņemts, ka esat iegādājies Human Resources, noslēdzot mākoņpakalpojumu nodrošinātāja (Cloud Solution Provider — CSP) vai uzņēmuma arhitektūras (enterprise architecture — EA) līgumu.</span><span class="sxs-lookup"><span data-stu-id="c3719-115">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="c3719-116">Tā kā katra Human Resources vide ir ietverta atsevišķā Power Apps vidē, ir pieejamas divas iespējas.</span><span class="sxs-lookup"><span data-stu-id="c3719-116">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="c3719-117">Pirmā iespēja ietver visas Power Apps vides noņemšanu, bet otrā iespēja ietver tikai Human Resources vides noņemšanu.</span><span class="sxs-lookup"><span data-stu-id="c3719-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="c3719-118">Pirmo iespēju ir ieteicams izvēlēties gadījumā, ja esat izveidojis Power Apps vidi tikai Human Resources nodrošināšanai un esat tikko sācis ieviešanu vai vēl nav izveidota neviena integrācija.</span><span class="sxs-lookup"><span data-stu-id="c3719-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="c3719-119">Otrā iespēja ir piemērota gadījumā, ja jums ir izveidota Power Apps vide ar bagātīgiem datiem, kas ir saistīti ar Power Apps un Power Automate.</span><span class="sxs-lookup"><span data-stu-id="c3719-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="c3719-120">Pirms Power Apps vides noņemšanas pārliecinieties, vai tā netiek izmantota vērtīgu datu integrācijai ārpus Human Resources tvēruma.</span><span class="sxs-lookup"><span data-stu-id="c3719-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="c3719-121">Ņemiet arī vērā, ka noklusējuma Power Apps vides nevar noņemt.</span><span class="sxs-lookup"><span data-stu-id="c3719-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="c3719-122">Lai noņemtu visu Power Apps vidi, tostarp Human Resources vidi un saistītās programmas un plūsmas, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="c3719-122">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="c3719-123">Pāriet uz [Power Apps Administrēšanas centru](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="c3719-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="c3719-124">Atlasiet **Vides**.</span><span class="sxs-lookup"><span data-stu-id="c3719-124">Select **Environments**.</span></span>
3. <span data-ttu-id="c3719-125">Atlasiet noņemamo vidi.</span><span class="sxs-lookup"><span data-stu-id="c3719-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="c3719-126">Atlasiet **Dzēst** un apstipriniet dzēšanu.</span><span class="sxs-lookup"><span data-stu-id="c3719-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="c3719-127">Uzgaidiet, līdz ir pabeigta dzēšana.</span><span class="sxs-lookup"><span data-stu-id="c3719-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="c3719-128">Pierakstieties [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS), izmantojot kontu, ko izmantojāt, lai abonētu Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c3719-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="c3719-129">Atlasiet Human Resources projektu, kurā ir ietverta vide.</span><span class="sxs-lookup"><span data-stu-id="c3719-129">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="c3719-130">Savā LCS projektā atlasiet elementu **Human Resources programmas pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="c3719-130">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="c3719-131">Atlasiet noņemamo instanci.</span><span class="sxs-lookup"><span data-stu-id="c3719-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="c3719-132">Atlasiet **Noņemt instanci** un apstipriniet savu lēmumu.</span><span class="sxs-lookup"><span data-stu-id="c3719-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="c3719-133">Lai noņemtu Human Resources vidi no esošas Power Apps vides, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="c3719-133">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="c3719-134">Ņemiet vērā, ka nepieciešamība sazināties ar atbalsta dienestu un Human Resources DevOps grupu ir pagaidu prasība, kas ir jāizpilda, līdz šis līdzeklis tiks tiešā veidā iespējots LCS.</span><span class="sxs-lookup"><span data-stu-id="c3719-134">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="c3719-135">Sazinieties ar atbalsta dienestu, lai iesniegtu noņemšanas pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="c3719-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="c3719-136">Atbalsta dienesta grupa iesniedz noņemšanas pieprasījumu Human Resources DevOps grupai.</span><span class="sxs-lookup"><span data-stu-id="c3719-136">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="c3719-137">Turpiniet darbu, kad saņemat paziņojumu par vides noņemšanu.</span><span class="sxs-lookup"><span data-stu-id="c3719-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="c3719-138">Pierakstieties LCS, izmantojot to pašu kontu, ko lietojat Human Resources abonēšanai.</span><span class="sxs-lookup"><span data-stu-id="c3719-138">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="c3719-139">Atlasiet Human Resources projektu, kurā ir ietverta vide.</span><span class="sxs-lookup"><span data-stu-id="c3719-139">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="c3719-140">Savā LCS projektā atlasiet elementu **Human Resources programmas pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="c3719-140">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="c3719-141">Atlasiet noņemamo instanci, kam ir jānorāda izvietošanas statuss **Neizdevās**.</span><span class="sxs-lookup"><span data-stu-id="c3719-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="c3719-142">Atlasiet **Noņemt instanci** un apstipriniet savu lēmumu.</span><span class="sxs-lookup"><span data-stu-id="c3719-142">Select **Remove instance** and confirm your decision.</span></span> 
