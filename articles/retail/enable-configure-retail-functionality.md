---
title: "Sākumdatu inicializēšana jaunās Retail vidēs"
description: "Šajā rakstā ir aprakstīti dati, kas tiek izveidoti kā daļa no inicializēšanas procesa programmatūrai Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 52f0c52748958f0bebb6c40df01cfac10c0ed427
ms.contentlocale: lv-lv
ms.lasthandoff: 01/04/2019

---

# <a name="initialize-seed-data-in-new-retail-environments"></a><span data-ttu-id="b620f-103">Sākumdatu inicializēšana jaunās Retail vidēs</span><span class="sxs-lookup"><span data-stu-id="b620f-103">Initialize seed data in new Retail environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b620f-104">Šajā rakstā ir aprakstīti dati, kas tiek izveidoti kā daļa no inicializēšanas procesa programmatūrai Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="b620f-104">This article describes the data that's created as part of the initialization process for Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="b620f-105">Pēc mazumtirdzniecības risinājuma izvietošanas caur Microsoft Dynamics Lifecycle Services (LCS), ir jāinicializē mazumtirdzniecības konfigurācija, lai izveidotu pamata konfigurācijas datus.</span><span class="sxs-lookup"><span data-stu-id="b620f-105">After the Retail solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the retail configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b620f-106">Pirms mazumtirdzniecības konfigurācijas inicializēšanas, pārliecinieties, ka esat norādījis valodu un pasta adresi katrai juridiskajai personai, kur tiks iestatīti mazumtirdzniecības veikali.</span><span class="sxs-lookup"><span data-stu-id="b620f-106">Before you initialize the retail configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up retail stores.</span></span> <span data-ttu-id="b620f-107">Šī darbība ir jāveic katrai juridiskajai personai, kura tiks izmantota mazumtirdzniecībai.</span><span class="sxs-lookup"><span data-stu-id="b620f-107">This step must be completed for each legal entity that you use for retail.</span></span>

<span data-ttu-id="b620f-108">Lai inicializētu mazumtirdzniecības konfigurāciju, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="b620f-108">To initialize the retail configuration, follow these steps.</span></span>

1. <span data-ttu-id="b620f-109">Startējiet Dynamics 365 for Retail klientu.</span><span class="sxs-lookup"><span data-stu-id="b620f-109">Start the Dynamics 365 for Retail client.</span></span>
2. <span data-ttu-id="b620f-110">Noklikšķiniet uz **Mazumtirdzniecība** &gt; **Headquarters iestatīšana** &gt; **Parametri** &gt; **Mazumtirdzniecības parametri**.</span><span class="sxs-lookup"><span data-stu-id="b620f-110">Click **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.</span></span>
3. <span data-ttu-id="b620f-111">Noklikšķiniet uz **Inicializēt**.</span><span class="sxs-lookup"><span data-stu-id="b620f-111">Click **Initialize**.</span></span>

<span data-ttu-id="b620f-112">Inicializācija izveido šādus noklusējuma konfigurācijas datus:</span><span class="sxs-lookup"><span data-stu-id="b620f-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="b620f-113">Mazumtirdzniecības plānotāja darbi un apakšdarbi</span><span class="sxs-lookup"><span data-stu-id="b620f-113">Retail scheduler jobs and subjobs</span></span>
- <span data-ttu-id="b620f-114">Mazumtirdzniecības kanāla shēma</span><span class="sxs-lookup"><span data-stu-id="b620f-114">Retail channel schema</span></span>
- <span data-ttu-id="b620f-115">Mazumtirdzniecības sadales grafiki</span><span class="sxs-lookup"><span data-stu-id="b620f-115">Retail distribution schedules</span></span>
- <span data-ttu-id="b620f-116">Noklusējuma ekrāna izkārtojumu, kas ietver pogu rindas, attēlus un tēmas</span><span class="sxs-lookup"><span data-stu-id="b620f-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="b620f-117">Informācija par laika joslu</span><span class="sxs-lookup"><span data-stu-id="b620f-117">Time zone information</span></span>
- <span data-ttu-id="b620f-118">Pārdošanas punktu (POS) saderība</span><span class="sxs-lookup"><span data-stu-id="b620f-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="b620f-119">POS atļaujas</span><span class="sxs-lookup"><span data-stu-id="b620f-119">POS permissions</span></span>
- <span data-ttu-id="b620f-120">Kanālu pārskati</span><span class="sxs-lookup"><span data-stu-id="b620f-120">Channel reports</span></span>
- <span data-ttu-id="b620f-121">Atribūta metadati</span><span class="sxs-lookup"><span data-stu-id="b620f-121">Attribute metadata</span></span>
- <span data-ttu-id="b620f-122">Elementa validēšanas veidnes</span><span class="sxs-lookup"><span data-stu-id="b620f-122">Entity validation templates</span></span>
- <span data-ttu-id="b620f-123">Pakešuzdevums Commerce Data Exchange sesijas vēstures dzēšanai</span><span class="sxs-lookup"><span data-stu-id="b620f-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="b620f-124">Turklāt Dynamics 365 for Retail datu bāzei ir iespējota reģistrēšana, kas ir saistīta ar maksājumu karšu nozari (PCI).</span><span class="sxs-lookup"><span data-stu-id="b620f-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Dynamics 365 for Retail database.</span></span>

> [!NOTE]
> <span data-ttu-id="b620f-125">Pastāv iespēja atsevišķi konfigurēt mazumtirdzniecības plānotāju.</span><span class="sxs-lookup"><span data-stu-id="b620f-125">There is an option to separately configure the Retail scheduler.</span></span> <span data-ttu-id="b620f-126">Šī opcija ļauj atiestatīt mazumtirdzniecības plānotāja konfigurāciju uz noklusētajiem iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="b620f-126">This option lets you reset the Retail scheduler configuration to its default settings.</span></span>

<span data-ttu-id="b620f-127">Pēc inicializēšanas pabeigšanas, jums ir jākonfigurē papildu mazumtirdzniecības dati.</span><span class="sxs-lookup"><span data-stu-id="b620f-127">After initialization is completed, you must configure additional retail data.</span></span> <span data-ttu-id="b620f-128">Daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="b620f-128">Here are some examples:</span></span>

- <span data-ttu-id="b620f-129">Mazumtirdzniecības parametri</span><span class="sxs-lookup"><span data-stu-id="b620f-129">Retail parameters</span></span>
- <span data-ttu-id="b620f-130">Mazumtirdzniecības plānotāja parametri</span><span class="sxs-lookup"><span data-stu-id="b620f-130">Retail scheduler parameters</span></span>
- <span data-ttu-id="b620f-131">Mazumtirdzniecības kanāli</span><span class="sxs-lookup"><span data-stu-id="b620f-131">Retail channels</span></span>
- <span data-ttu-id="b620f-132">Reģistri un ierīces</span><span class="sxs-lookup"><span data-stu-id="b620f-132">Registers and devices</span></span>
- <span data-ttu-id="b620f-133">Preču klāsts</span><span class="sxs-lookup"><span data-stu-id="b620f-133">Assortments</span></span>

