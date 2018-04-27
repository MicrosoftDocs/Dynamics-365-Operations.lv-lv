---
title: "Talent vides noņemšana"
description: "Šajā tēmā ir detalizēti aprakstīta Microsoft Dynamics 365 for Talent izmēģinājuma vai ražošanas vides noņemšanas procedūra."
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d1870c84d4d5e7402bae44d192ce7587c2f67fe7
ms.openlocfilehash: 0e7748b079b1cd5c069917d46e05cd281ea6aa01
ms.contentlocale: lv-lv
ms.lasthandoff: 04/05/2018

---
# <a name="remove-a-talent-environment"></a><span data-ttu-id="47619-103">Talent vides noņemšana</span><span class="sxs-lookup"><span data-stu-id="47619-103">Remove a Talent environment</span></span>

<span data-ttu-id="47619-104">Šajā tēmā ir detalizēti aprakstīta Microsoft Dynamics 365 for Talent izmēģinājuma vai ražošanas vides noņemšanas procedūra.</span><span class="sxs-lookup"><span data-stu-id="47619-104">This topic walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 for Talent.</span></span>

## <a name="removing-a-test-drive-environment"></a><span data-ttu-id="47619-105">Izmēģinājuma vides noņemšana</span><span class="sxs-lookup"><span data-stu-id="47619-105">Removing a test drive environment</span></span>

<span data-ttu-id="47619-106">Talent izmēģinājuma vides tiek nodrošinātas, izmantojot 60 dienu derīguma termiņa politiku.</span><span class="sxs-lookup"><span data-stu-id="47619-106">Talent test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="47619-107">Taču izmēģinājuma vides īpašnieki var ātrāk beigt izmēģinājumu, veicot tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="47619-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="47619-108">Pārejiet uz [PowerApps administrēšanas centru](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="47619-108">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="47619-109">Atlasiet **Vides**.</span><span class="sxs-lookup"><span data-stu-id="47619-109">Select **Environments**.</span></span>
3. <span data-ttu-id="47619-110">Atlasiet izmēģinājuma vidi, kuras nosaukuma formāts līdzinās šim: TestDrive — alias@domain.</span><span class="sxs-lookup"><span data-stu-id="47619-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="47619-111">Atlasiet **Dzēst** un apstipriniet dzēšanu.</span><span class="sxs-lookup"><span data-stu-id="47619-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="47619-112">Esošā izmēģinājuma vide tiek noņemta.</span><span class="sxs-lookup"><span data-stu-id="47619-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="47619-113">Kad tā ir noņemta, jūs varat reģistrēties jaunas izmēģinājuma vides saņemšanai.</span><span class="sxs-lookup"><span data-stu-id="47619-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="removing-a-production-environment"></a><span data-ttu-id="47619-114">Ražošanas vides noņemšana</span><span class="sxs-lookup"><span data-stu-id="47619-114">Removing a production environment</span></span>

<span data-ttu-id="47619-115">Šajā tēmā tiek pieņemts, ka esat iegādājies programmatūru Talent, noslēdzot mākoņpakalpojumu nodrošinātāja (Cloud Solution Provider — CSP) vai uzņēmuma arhitektūras (enterprise architecture — EA) līgumu.</span><span class="sxs-lookup"><span data-stu-id="47619-115">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="47619-116">Tā kā katra Talent vide ir ietverta atsevišķā PowerApps vidē, ir pieejamas divas iespējas.</span><span class="sxs-lookup"><span data-stu-id="47619-116">Since a single Talent environment is “contained” within a single PowerApps environment, there are two options to consider.</span></span> <span data-ttu-id="47619-117">Pirmā iespēja ietver visas PowerApps vides noņemšanu, bet otrā iespēja ietver tikai Talent vides noņemšanu.</span><span class="sxs-lookup"><span data-stu-id="47619-117">The first option involves removing the entire PowerApps environment; the second option involves removing only Talent.</span></span> <span data-ttu-id="47619-118">Pirmo iespēju ir ieteicams izvēlēties gadījumā, ja esat izveidojis PowerApps vidi tikai Talent nodrošināšanai un esat tikko sācis ieviešanu vai vēl nav izveidota neviena integrācija.</span><span class="sxs-lookup"><span data-stu-id="47619-118">The first option is preferred when you have created a PowerApps environment expressly for the purpose of provisioning Talent, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="47619-119">Otrā iespēja ir piemērota gadījumā, ja jums ir izveidota PowerApps vide ar bagātīgiem datiem, kas ir saistīti ar PowerApps programmām un plūsmām.</span><span class="sxs-lookup"><span data-stu-id="47619-119">The second option is appropriate when you have an established PowerApps environment populated with rich data that's leveraged in PowerApps and Flows.</span></span>

> [!Important]
> <span data-ttu-id="47619-120">Pirms PowerApps vides noņemšanas pārliecinieties, vai tā netiek izmantota bagātīgu datu integrācijai ārpus Talent tvēruma.</span><span class="sxs-lookup"><span data-stu-id="47619-120">Before removing the PowerApps environment, ensure it is not being used for rich data integrations outside the scope of Talent.</span></span> <span data-ttu-id="47619-121">Ņemiet arī vērā, ka noklusējuma PowerApps vides nevar noņemt.</span><span class="sxs-lookup"><span data-stu-id="47619-121">Also note that the default PowerApps environments cannot be removed.</span></span> 

<span data-ttu-id="47619-122">Lai noņemtu visu PowerApps vidi, tostarp Talent vidi un saistītās programmas un plūsmas, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="47619-122">To remove the entire PowerApps environment, including Talent and the associated Apps and Flows:</span></span>

1. <span data-ttu-id="47619-123">Pārejiet uz [PowerApps administrēšanas centru](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="47619-123">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="47619-124">Atlasiet **Vides**.</span><span class="sxs-lookup"><span data-stu-id="47619-124">Select **Environments**.</span></span>
3. <span data-ttu-id="47619-125">Atlasiet noņemamo vidi.</span><span class="sxs-lookup"><span data-stu-id="47619-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="47619-126">Atlasiet **Dzēst** un apstipriniet dzēšanu.</span><span class="sxs-lookup"><span data-stu-id="47619-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="47619-127">Uzgaidiet, līdz ir pabeigta dzēšana.</span><span class="sxs-lookup"><span data-stu-id="47619-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="47619-128">Pierakstieties pakalpojumā [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS), izmantojot kontu, ko izmantojāt, lai abonētu programmatūru Talent.</span><span class="sxs-lookup"><span data-stu-id="47619-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Talent.</span></span> 
7. <span data-ttu-id="47619-129">Atlasiet Talent projektu, kurā ir ietverta vide.</span><span class="sxs-lookup"><span data-stu-id="47619-129">Select the Talent Project that contains the environment.</span></span> 
8. <span data-ttu-id="47619-130">LCS projektā atlasiet elementu **Talent programmas pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="47619-130">In your LCS project, select the **Talent App Management** tile.</span></span> 
9. <span data-ttu-id="47619-131">Atlasiet noņemamo instanci.</span><span class="sxs-lookup"><span data-stu-id="47619-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="47619-132">Atlasiet **Noņemt instanci** un apstipriniet savu lēmumu.</span><span class="sxs-lookup"><span data-stu-id="47619-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="47619-133">Lai noņemtu Talent vidi no esošas PowerApps vides, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="47619-133">To remove a Talent environment from an existing PowerApps environment, complete the following steps.</span></span> <span data-ttu-id="47619-134">Ņemiet vērā, ka nepieciešamība sazināties ar atbalsta dienestu un Talent DevOps darba grupu ir pagaidu prasība, kas ir jāizpilda, līdz šis līdzeklis tiks tiešā veidā iespējots LCS.</span><span class="sxs-lookup"><span data-stu-id="47619-134">Note that the need to involve support and contact the Talent DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="47619-135">Sazinieties ar atbalsta dienestu, lai iesniegtu noņemšanas pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="47619-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="47619-136">Atbalsta dienesta darba grupa iesniedz noņemšanas pieprasījumu Talent DevOps darba grupai.</span><span class="sxs-lookup"><span data-stu-id="47619-136">The Support team will initiate a removal request with the Talent DevOps team.</span></span> 
3. <span data-ttu-id="47619-137">Turpiniet darbu, kad saņemat paziņojumu par vides noņemšanu.</span><span class="sxs-lookup"><span data-stu-id="47619-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="47619-138">Pierakstieties pakalpojumā LCS, izmantojot to pašu kontu, ko izmantojāt, lai abonētu Talent.</span><span class="sxs-lookup"><span data-stu-id="47619-138">Sign in to LCS using the account that you used to subscribe to Talent.</span></span> 
5. <span data-ttu-id="47619-139">Atlasiet Talent projektu, kurā ir ietverta vide.</span><span class="sxs-lookup"><span data-stu-id="47619-139">Select the Talent project that contains the environment.</span></span> 
6. <span data-ttu-id="47619-140">LCS projektā atlasiet elementu **Talent programmas pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="47619-140">In your LCS project, select the **Talent App Management** tile.</span></span> 
7. <span data-ttu-id="47619-141">Atlasiet noņemamo instanci, kam ir jānorāda izvietošanas statuss **Neizdevās**.</span><span class="sxs-lookup"><span data-stu-id="47619-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="47619-142">Atlasiet **Noņemt instanci** un apstipriniet savu lēmumu.</span><span class="sxs-lookup"><span data-stu-id="47619-142">Select **Remove instance** and confirm your decision.</span></span> 


