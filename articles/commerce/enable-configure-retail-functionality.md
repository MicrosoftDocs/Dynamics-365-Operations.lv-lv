---
title: Sākumdatu inicializēšana jaunās Commerce vidēs
description: Šajā rakstā ir aprakstīti dati, kas tiek izveidoti Dynamics 365 Commerce inicializācijas procesa ietvaros.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9f534410b21fd97554f4e038bb14eebd5f887130
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792587"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a><span data-ttu-id="53ba7-103">Sākumdatu inicializēšana jaunās Commerce vidēs</span><span class="sxs-lookup"><span data-stu-id="53ba7-103">Initialize seed data in new Commerce environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="53ba7-104">Šajā rakstā ir aprakstīti dati, kas tiek izveidoti Dynamics 365 Commerce inicializācijas procesa ietvaros.</span><span class="sxs-lookup"><span data-stu-id="53ba7-104">This article describes the data that's created as part of the initialization process for Dynamics 365 Commerce.</span></span>

<span data-ttu-id="53ba7-105">Pēc Commerce risinājuma izvietošanas, izmantojot portālu Microsoft Dynamics Lifecycle Services (LCS), ir jāinicializē Commerce konfigurācija, lai izveidotu pamata konfigurācijas datus.</span><span class="sxs-lookup"><span data-stu-id="53ba7-105">After the Commerce solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the Commerce configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="53ba7-106">Pirms komercijas konfigurācijas inicializēšanas, pārliecinieties, ka esat norādījis valodu un pasta adresi katrai juridiskajai personai, kur tiks iestatīti veikali.</span><span class="sxs-lookup"><span data-stu-id="53ba7-106">Before you initialize the commerce configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up stores.</span></span> <span data-ttu-id="53ba7-107">Šī darbība ir jāveic katrai juridiskajai personai, kura tiks izmantota komercijai.</span><span class="sxs-lookup"><span data-stu-id="53ba7-107">This step must be completed for each legal entity that you use for commerce.</span></span>

<span data-ttu-id="53ba7-108">Lai inicializētu konfigurāciju, veiciet talāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="53ba7-108">To initialize the configuration, follow these steps.</span></span>

1. <span data-ttu-id="53ba7-109">Palaidiet Commerce klientu.</span><span class="sxs-lookup"><span data-stu-id="53ba7-109">Start the Commerce client.</span></span>
2. <span data-ttu-id="53ba7-110">Noklikšķiniet uz **Mazumtirdzniecība un komercija** &gt; **Headquarters iestatīšana** &gt; **Parametri** &gt; **Komercijas parameteri**.</span><span class="sxs-lookup"><span data-stu-id="53ba7-110">Click **Retail and Commerce** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Commerce parameters**.</span></span>
3. <span data-ttu-id="53ba7-111">Noklikšķiniet uz **Inicializēt**.</span><span class="sxs-lookup"><span data-stu-id="53ba7-111">Click **Initialize**.</span></span>

<span data-ttu-id="53ba7-112">Inicializācija izveido šādus noklusējuma konfigurācijas datus:</span><span class="sxs-lookup"><span data-stu-id="53ba7-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="53ba7-113">Commerce plānotāja darbi un apakšdarbi</span><span class="sxs-lookup"><span data-stu-id="53ba7-113">Commerce scheduler jobs and subjobs</span></span>
- <span data-ttu-id="53ba7-114">Komercijas kanāla shēma</span><span class="sxs-lookup"><span data-stu-id="53ba7-114">Commerce channel schema</span></span>
- <span data-ttu-id="53ba7-115">Commerce sadales grafiki</span><span class="sxs-lookup"><span data-stu-id="53ba7-115">Commerce distribution schedules</span></span>
- <span data-ttu-id="53ba7-116">Noklusējuma ekrāna izkārtojumu, kas ietver pogu rindas, attēlus un tēmas</span><span class="sxs-lookup"><span data-stu-id="53ba7-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="53ba7-117">Informācija par laika joslu</span><span class="sxs-lookup"><span data-stu-id="53ba7-117">Time zone information</span></span>
- <span data-ttu-id="53ba7-118">Pārdošanas punktu (POS) saderība</span><span class="sxs-lookup"><span data-stu-id="53ba7-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="53ba7-119">POS atļaujas</span><span class="sxs-lookup"><span data-stu-id="53ba7-119">POS permissions</span></span>
- <span data-ttu-id="53ba7-120">Kanālu pārskati</span><span class="sxs-lookup"><span data-stu-id="53ba7-120">Channel reports</span></span>
- <span data-ttu-id="53ba7-121">Atribūta metadati</span><span class="sxs-lookup"><span data-stu-id="53ba7-121">Attribute metadata</span></span>
- <span data-ttu-id="53ba7-122">Elementa validēšanas veidnes</span><span class="sxs-lookup"><span data-stu-id="53ba7-122">Entity validation templates</span></span>
- <span data-ttu-id="53ba7-123">Commerce Data Exchange sesijas vēstures dzēšanas pakešuzdevums</span><span class="sxs-lookup"><span data-stu-id="53ba7-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="53ba7-124">Turklāt, Commerce datu bāzei ir iespējota reģistrācija, kas ir saistīta ar maksājumu karšu nozari (PCI).</span><span class="sxs-lookup"><span data-stu-id="53ba7-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Commerce database.</span></span>

> [!NOTE]
> <span data-ttu-id="53ba7-125">Pastāv iespēja atsevišķi konfigurēt Commerce plānotāju.</span><span class="sxs-lookup"><span data-stu-id="53ba7-125">There is an option to separately configure the Commerce scheduler.</span></span> <span data-ttu-id="53ba7-126">Šī opcija ļauj atiestatīt Commerce plānotāja konfigurāciju uz noklusētajiem iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="53ba7-126">This option lets you reset the Commerce scheduler configuration to its default settings.</span></span>

<span data-ttu-id="53ba7-127">Pēc inicializēšanas pabeigšanas, jums ir jākonfigurē papildu komercijas dati.</span><span class="sxs-lookup"><span data-stu-id="53ba7-127">After initialization is completed, you must configure additional commerce data.</span></span> <span data-ttu-id="53ba7-128">Daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="53ba7-128">Here are some examples:</span></span>

- <span data-ttu-id="53ba7-129">Komercijas parametri</span><span class="sxs-lookup"><span data-stu-id="53ba7-129">Commerce parameters</span></span>
- <span data-ttu-id="53ba7-130">Komercijas plānotāja parametri</span><span class="sxs-lookup"><span data-stu-id="53ba7-130">Commerce scheduler parameters</span></span>
- <span data-ttu-id="53ba7-131">Commerce kanāli.</span><span class="sxs-lookup"><span data-stu-id="53ba7-131">Commerce channels</span></span>
- <span data-ttu-id="53ba7-132">Reģistri un ierīces</span><span class="sxs-lookup"><span data-stu-id="53ba7-132">Registers and devices</span></span>
- <span data-ttu-id="53ba7-133">Preču klāsts</span><span class="sxs-lookup"><span data-stu-id="53ba7-133">Assortments</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]