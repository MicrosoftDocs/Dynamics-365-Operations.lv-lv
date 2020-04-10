---
title: Mobilās ierīces izvēlnes vienuma izveide, lai saņemtu numura zīmes konsolidāciju
description: Šajā procedūrā parādīts kā izveidot mobilās ierīces izvēlnes vienumu, lai saņemtu noliktavas vienības konsolidāciju.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13d08de62129698f85e0a30f870ba680e3bb0532
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148404"
---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="d84de-103">Mobilās ierīces izvēlnes vienuma izveide, lai saņemtu numura zīmes konsolidāciju</span><span class="sxs-lookup"><span data-stu-id="d84de-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d84de-104">Šajā procedūrā parādīts kā izveidot mobilās ierīces izvēlnes vienumu, lai saņemtu noliktavas vienības konsolidāciju.</span><span class="sxs-lookup"><span data-stu-id="d84de-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="d84de-105">Tas ļauj noliktavas darbiniekiem konsolidēt vienumus vienā noliktavas vienībā ar krājumiem, citā noliktavas vienībā tajā pašā atrašanās vietā.</span><span class="sxs-lookup"><span data-stu-id="d84de-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="d84de-106">Piemēram, to varētu izmantot, ja turpmākās sagatavošanas darbības būtu vienādas abiem darba pasūtījumiem, tāpēc, tādējādi sapludinātajiem vienumiem darbs ir jāpaveic tikai vienreiz.</span><span class="sxs-lookup"><span data-stu-id="d84de-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="d84de-107">Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="d84de-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="d84de-108">Šo uzdevumu parasti veic noliktavas pārvaldnieks.</span><span class="sxs-lookup"><span data-stu-id="d84de-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="d84de-109">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="d84de-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="d84de-110">Dodieties uz Noliktavas vadība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlnes vienumi.</span><span class="sxs-lookup"><span data-stu-id="d84de-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="d84de-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d84de-111">Click New.</span></span>
3. <span data-ttu-id="d84de-112">Laukā Izvēlnes vienuma nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d84de-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="d84de-113">Laukā Virsraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d84de-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="d84de-114">Laukā Režīms atlasiet 'Netiešs'.</span><span class="sxs-lookup"><span data-stu-id="d84de-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="d84de-115">Laukā Aktivitātes kods atlasiet 'Konsolidēt noliktavas vienības.</span><span class="sxs-lookup"><span data-stu-id="d84de-115">In the Activity code field, select 'Consolidate license plates'.</span></span>

