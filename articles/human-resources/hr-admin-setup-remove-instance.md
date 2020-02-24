---
title: Instances noņemšana
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5c5f875ad9361c31af4fbe863488b881cdd97a6e
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009759"
---
# <a name="remove-an-instance"></a><span data-ttu-id="343a6-102">Instances noņemšana</span><span class="sxs-lookup"><span data-stu-id="343a6-102">Remove an instance</span></span>

<span data-ttu-id="343a6-103">Šajā rakstā ir detalizēti aprakstīts, kā noņemt izmēģinājuma vai ražošanas vidi Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="343a6-103">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="343a6-104">Izmēģinājuma vides noņemšana</span><span class="sxs-lookup"><span data-stu-id="343a6-104">Remove a test drive environment</span></span>

<span data-ttu-id="343a6-105">Human Resources izmēģinājuma vides tiek nodrošinātas, izmantojot 60 dienu derīguma termiņa politiku.</span><span class="sxs-lookup"><span data-stu-id="343a6-105">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="343a6-106">Taču izmēģinājuma vides īpašnieki var ātrāk beigt izmēģinājumu, veicot tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="343a6-106">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="343a6-107">Pāriet uz [Power Apps Administrēšanas centru](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="343a6-107">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="343a6-108">Atlasiet **Vides**.</span><span class="sxs-lookup"><span data-stu-id="343a6-108">Select **Environments**.</span></span>
3. <span data-ttu-id="343a6-109">Atlasiet izmēģinājuma vidi, kuras nosaukuma formāts līdzinās šim: TestDrive — aizstājvārds@domēns.</span><span class="sxs-lookup"><span data-stu-id="343a6-109">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="343a6-110">Atlasiet **Dzēst** un apstipriniet dzēšanu.</span><span class="sxs-lookup"><span data-stu-id="343a6-110">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="343a6-111">Esošā izmēģinājuma vide tiek noņemta.</span><span class="sxs-lookup"><span data-stu-id="343a6-111">The existing test drive environment will be removed.</span></span> <span data-ttu-id="343a6-112">Kad tā ir noņemta, jūs varat reģistrēties jaunas izmēģinājuma vides saņemšanai.</span><span class="sxs-lookup"><span data-stu-id="343a6-112">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="343a6-113">Ražošanas vides noņemšana</span><span class="sxs-lookup"><span data-stu-id="343a6-113">Remove a production environment</span></span>

<span data-ttu-id="343a6-114">Šajā rakstā tiek pieņemts, ka esat iegādājies Human Resources, noslēdzot mākoņpakalpojumu nodrošinātāja (Cloud Solution Provider — CSP) vai uzņēmuma arhitektūras (enterprise architecture — EA) līgumu.</span><span class="sxs-lookup"><span data-stu-id="343a6-114">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="343a6-115">Tā kā katra Human Resources vide ir ietverta atsevišķā Power Apps vidē, ir pieejamas divas iespējas.</span><span class="sxs-lookup"><span data-stu-id="343a6-115">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="343a6-116">Pirmā iespēja ietver visas Power Apps vides noņemšanu, bet otrā iespēja ietver tikai Human Resources vides noņemšanu.</span><span class="sxs-lookup"><span data-stu-id="343a6-116">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="343a6-117">Pirmo iespēju ir ieteicams izvēlēties gadījumā, ja esat izveidojis Power Apps vidi tikai Human Resources nodrošināšanai un esat tikko sācis ieviešanu vai vēl nav izveidota neviena integrācija.</span><span class="sxs-lookup"><span data-stu-id="343a6-117">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="343a6-118">Otrā iespēja ir piemērota gadījumā, ja jums ir izveidota Power Apps vide ar bagātīgiem datiem, kas ir saistīti ar Power Apps un Power Automate.</span><span class="sxs-lookup"><span data-stu-id="343a6-118">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="343a6-119">Pirms Power Apps vides noņemšanas pārliecinieties, vai tā netiek izmantota vērtīgu datu integrācijai ārpus Human Resources tvēruma.</span><span class="sxs-lookup"><span data-stu-id="343a6-119">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="343a6-120">Ņemiet arī vērā, ka noklusējuma Power Apps vides nevar noņemt.</span><span class="sxs-lookup"><span data-stu-id="343a6-120">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="343a6-121">Lai noņemtu visu Power Apps vidi, tostarp Human Resources vidi un saistītās programmas un plūsmas, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="343a6-121">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="343a6-122">Pāriet uz [Power Apps Administrēšanas centru](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="343a6-122">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="343a6-123">Atlasiet **Vides**.</span><span class="sxs-lookup"><span data-stu-id="343a6-123">Select **Environments**.</span></span>
3. <span data-ttu-id="343a6-124">Atlasiet noņemamo vidi.</span><span class="sxs-lookup"><span data-stu-id="343a6-124">Select the environment to be removed.</span></span>
4. <span data-ttu-id="343a6-125">Atlasiet **Dzēst** un apstipriniet dzēšanu.</span><span class="sxs-lookup"><span data-stu-id="343a6-125">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="343a6-126">Uzgaidiet, līdz ir pabeigta dzēšana.</span><span class="sxs-lookup"><span data-stu-id="343a6-126">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="343a6-127">Pierakstieties [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS), izmantojot kontu, ko izmantojāt, lai abonētu Human Resources.</span><span class="sxs-lookup"><span data-stu-id="343a6-127">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="343a6-128">Atlasiet Human Resources projektu, kurā ir ietverta vide.</span><span class="sxs-lookup"><span data-stu-id="343a6-128">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="343a6-129">Savā LCS projektā atlasiet elementu **Human Resources programmas pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="343a6-129">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="343a6-130">Atlasiet noņemamo instanci.</span><span class="sxs-lookup"><span data-stu-id="343a6-130">Select the instance to remove.</span></span> 
10. <span data-ttu-id="343a6-131">Atlasiet **Noņemt instanci** un apstipriniet savu lēmumu.</span><span class="sxs-lookup"><span data-stu-id="343a6-131">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="343a6-132">Lai noņemtu Human Resources vidi no esošas Power Apps vides, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="343a6-132">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="343a6-133">Ņemiet vērā, ka nepieciešamība sazināties ar atbalsta dienestu un Human Resources DevOps grupu ir pagaidu prasība, kas ir jāizpilda, līdz šis līdzeklis tiks tiešā veidā iespējots LCS.</span><span class="sxs-lookup"><span data-stu-id="343a6-133">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="343a6-134">Sazinieties ar atbalsta dienestu, lai iesniegtu noņemšanas pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="343a6-134">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="343a6-135">Atbalsta dienesta grupa iesniedz noņemšanas pieprasījumu Human Resources DevOps grupai.</span><span class="sxs-lookup"><span data-stu-id="343a6-135">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="343a6-136">Turpiniet darbu, kad saņemat paziņojumu par vides noņemšanu.</span><span class="sxs-lookup"><span data-stu-id="343a6-136">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="343a6-137">Pierakstieties LCS, izmantojot to pašu kontu, ko lietojat Human Resources abonēšanai.</span><span class="sxs-lookup"><span data-stu-id="343a6-137">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="343a6-138">Atlasiet Human Resources projektu, kurā ir ietverta vide.</span><span class="sxs-lookup"><span data-stu-id="343a6-138">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="343a6-139">Savā LCS projektā atlasiet elementu **Human Resources programmas pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="343a6-139">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="343a6-140">Atlasiet noņemamo instanci, kam ir jānorāda izvietošanas statuss **Neizdevās**.</span><span class="sxs-lookup"><span data-stu-id="343a6-140">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="343a6-141">Atlasiet **Noņemt instanci** un apstipriniet savu lēmumu.</span><span class="sxs-lookup"><span data-stu-id="343a6-141">Select **Remove instance** and confirm your decision.</span></span> 
