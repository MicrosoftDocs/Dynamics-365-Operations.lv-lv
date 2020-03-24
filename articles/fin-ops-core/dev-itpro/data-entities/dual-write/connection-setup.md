---
title: Atbalstītie scenāriji duālā ieraksta iestatījumiem
description: Šajā tēmā aprakstīti scenāriji, kas tiek atbalstīti duālā ieraksta iestatījumiem.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 1319f1228b635e207754f7c2516cb2b5353a9edd
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112479"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="a4197-103">Atbalstītie scenāriji duālā ieraksta iestatījumiem</span><span class="sxs-lookup"><span data-stu-id="a4197-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="a4197-104">Varat iestatīt duālā ieraksta savienojumu starp Finance and Operations vidi un Common Data Service vidi.</span><span class="sxs-lookup"><span data-stu-id="a4197-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="a4197-105">**Finance and Operations vide** nodrošina **Finance and Operations programmu** (piemēram, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail un Dynamics 365 Human Resources) pamata platformu.</span><span class="sxs-lookup"><span data-stu-id="a4197-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="a4197-106">**Common Data Service vide** nodrošina pamata programmu **modeļa vadītām programmām pakalpojumā Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing un Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="a4197-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

<span data-ttu-id="a4197-107">Iestatīšanas mehānisms mainās atkarībā no jūsu abonementa un vides.</span><span class="sxs-lookup"><span data-stu-id="a4197-107">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="a4197-108">Jaunajām Finance and Operations programmu instancēm duālā ieraksta savienojuma iestatījums sākas portālā Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a4197-108">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="a4197-109">Ja jums ir Microsoft Power Platform licence, jūs saņemsit jaunu Common Data Service vidi, ja jūsu nomniekam tādas nav.</span><span class="sxs-lookup"><span data-stu-id="a4197-109">If you have a license for Microsoft Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="a4197-110">Esošajām instancēm Finance and Operations programmās, duālā ieraksta savienojuma iestatīšana sākas Finance and Operations vidē.</span><span class="sxs-lookup"><span data-stu-id="a4197-110">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="a4197-111">Tālāk ir norādīti atbalstītie iestatīšanas scenāriji:</span><span class="sxs-lookup"><span data-stu-id="a4197-111">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="a4197-112">Jauna Finance and Operations programmas instance un jauna modeļa vadītas programmas instance</span><span class="sxs-lookup"><span data-stu-id="a4197-112">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="a4197-113">Jauna Finance and Operations programmas instance un esoša modeļa vadītas programmas instance</span><span class="sxs-lookup"><span data-stu-id="a4197-113">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="a4197-114">Jauna Finance and Operations programmas instance, kurai ir demonstrācijas dati, un jauna modeļa vadītas programmas instance</span><span class="sxs-lookup"><span data-stu-id="a4197-114">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="a4197-115">Jauna Finance and Operations programmas instance, kurai ir demonstrācijas dati, un esoša modeļa vadītas programmas instance</span><span class="sxs-lookup"><span data-stu-id="a4197-115">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="a4197-116">Esoša Finance and Operations programmas instance un jauna modeļa vadītas programmas instance</span><span class="sxs-lookup"><span data-stu-id="a4197-116">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="a4197-117">Jauna Finance and Operations programmas instance un jauna modeļa vadītas programmas instance</span><span class="sxs-lookup"><span data-stu-id="a4197-117">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="a4197-118">Lai iestatītu duālā ieraksta savienojumu starp jaunu Finance and Operations programmas instanci, kurai nav datu, un jaunu modeļa vadītas programmas instanci pakalpojumā Dynamics 365, veiciet darbības, kas aprakstītas rakstā [Duālā ieraksta iestatīšana no Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="a4197-118">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="a4197-119">Kad savienojuma iestatīšana ir pabeigta, automātiski tiek veiktas šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="a4197-119">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="a4197-120">Tiek nodrošināta jauna, tukša Finance and Operations vide.</span><span class="sxs-lookup"><span data-stu-id="a4197-120">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="a4197-121">Tiek nodrošināta jauna, tukša modeļa vadītas programmas instance, kurā ir instalēts CRM galvenais risinājums.</span><span class="sxs-lookup"><span data-stu-id="a4197-121">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="a4197-122">Tiek izveidots duālā ieraksta savienojums DAT uzņēmuma datiem.</span><span class="sxs-lookup"><span data-stu-id="a4197-122">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="a4197-123">Elementa kartes ir iespējotas tiešsaistes sinhronizācijai.</span><span class="sxs-lookup"><span data-stu-id="a4197-123">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="a4197-124">Abas vides pēc tam ir gatavas tiešsaistes datu sinhronizācijai.</span><span class="sxs-lookup"><span data-stu-id="a4197-124">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a><span data-ttu-id="a4197-125">Jauna Finance and Operations programmas instance un esoša modeļa vadītas programmas instance</span><span class="sxs-lookup"><span data-stu-id="a4197-125">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="a4197-126">Lai iestatītu duālā ieraksta savienojumu starp jaunu Finance and Operations programmas instanci, kurai nav datu, un esošu modeļa vadītas programmas instanci pakalpojumā Dynamics 365, veiciet darbības, kas aprakstītas rakstā [Duālā ieraksta iestatīšana no Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="a4197-126">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="a4197-127">Kad savienojuma iestatīšana ir pabeigta, automātiski tiek veiktas šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="a4197-127">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="a4197-128">Tiek nodrošināta jauna, tukša Finance and Operations vide.</span><span class="sxs-lookup"><span data-stu-id="a4197-128">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="a4197-129">Tiek izveidots duālā ieraksta savienojums DAT uzņēmuma datiem.</span><span class="sxs-lookup"><span data-stu-id="a4197-129">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="a4197-130">Elementa kartes ir iespējotas tiešsaistes sinhronizācijai.</span><span class="sxs-lookup"><span data-stu-id="a4197-130">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="a4197-131">Abas vides pēc tam ir gatavas tiešsaistes datu sinhronizācijai.</span><span class="sxs-lookup"><span data-stu-id="a4197-131">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="a4197-132">Lai sinhronizētu esošos Common Data Service datus uz Finance and Operations programmu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="a4197-132">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="a4197-133">Izveidojiet jaunu uzņēmumu Finance and Operations programmā.</span><span class="sxs-lookup"><span data-stu-id="a4197-133">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="a4197-134">Pievienojiet uzņēmumu duālā ieraksta savienojuma iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="a4197-134">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="a4197-135">[Palaidiet](bootstrap-company-data.md)Common Data Service datus, izmantojot trīs burtu Starptautiskās Standartizācijas organizācijas (ISO) uzņēmuma kodu.</span><span class="sxs-lookup"><span data-stu-id="a4197-135">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="a4197-136">Tā kā duālais ieraksts ir tiešsaistes sinhronizācijas režīmā, dati no Common Data Service automātiski sāk plūst uz Finance and Operations programmu.</span><span class="sxs-lookup"><span data-stu-id="a4197-136">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a><span data-ttu-id="a4197-137">Jauna Finance and Operations programmas instance, kurai ir demonstrācijas dati, un jauna modeļa vadītas programmas instance</span><span class="sxs-lookup"><span data-stu-id="a4197-137">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="a4197-138">Lai iestatītu duālā ieraksta savienojumu starp jaunu Finance and Operations programmas instanci, kurā ir demonstrācijas dati, un jaunu modeļa vadītas programmas instanci pakalpojumā Dynamics 365, izpildiet darbības, kas aprakstītas sadaļā [Jauna Finance and Operations programmas instance un jauna modeļa vadītas programmas instance](#new-new) iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="a4197-138">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="a4197-139">Kad savienojuma iestatīšana ir pabeigta, ja vēlaties sinhronizēt demonstrācijas datus uz modeļa vadītu programmu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="a4197-139">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="a4197-140">LCS lapā atveriet Finance and Operations programmu, piesakieties un pēc tam atveriet **Datu pārvaldība \>Duālais ieraksts**.</span><span class="sxs-lookup"><span data-stu-id="a4197-140">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="a4197-141">Palaidiet funkciju **Sākotnējās sinhronizācijas** entītijām, kurām vēlaties sinhronizēt datus.</span><span class="sxs-lookup"><span data-stu-id="a4197-141">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a><span data-ttu-id="a4197-142">Jauna Finance and Operations programmas instance, kurai ir demonstrācijas dati, un esoša modeļa vadītas programmas instance</span><span class="sxs-lookup"><span data-stu-id="a4197-142">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="a4197-143">Lai iestatītu duālā ieraksta savienojumu starp jaunu Finance and Operations programmas instanci, kurā ir demonstrācijas dati, un esošu modeļa vadītas programmas instanci pakalpojumā Dynamics 365, izpildiet darbības, kas aprakstītas sadaļā [Jauna Finance and Operations programmas instance un esoša modeļa vadītas programmas instance](#new-existing) iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="a4197-143">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="a4197-144">Kad savienojuma iestatīšana ir pabeigta, ja vēlaties sinhronizēt demonstrācijas datus uz modeļa vadītu programmu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="a4197-144">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="a4197-145">LCS lapā atveriet Finance and Operations programmu, piesakieties un pēc tam atveriet **Datu pārvaldība \>Duālais ieraksts**.</span><span class="sxs-lookup"><span data-stu-id="a4197-145">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="a4197-146">Palaidiet funkciju **Sākotnējās sinhronizācijas** entītijām, kurām vēlaties sinhronizēt datus.</span><span class="sxs-lookup"><span data-stu-id="a4197-146">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="a4197-147">Lai sinhronizētu esošos Common Data Service datus uz Finance and Operations programmu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="a4197-147">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="a4197-148">Izveidojiet jaunu uzņēmumu Finance and Operations programmā.</span><span class="sxs-lookup"><span data-stu-id="a4197-148">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="a4197-149">Pievienojiet uzņēmumu duālā ieraksta savienojuma iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="a4197-149">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="a4197-150">[Palaidiet](bootstrap-company-data.md) Common Data Service datus, izmantojot trīs burtu Starptautiskās Standartizācijas organizācijas (ISO) uzņēmuma kodu.</span><span class="sxs-lookup"><span data-stu-id="a4197-150">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="a4197-151">Tā kā duālais ieraksts ir tiešsaistes sinhronizācijas režīmā, dati no Common Data Service automātiski sāk plūst uz Finance and Operations programmu.</span><span class="sxs-lookup"><span data-stu-id="a4197-151">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="a4197-152">Esoša Finance and Operations programmas instance un jauna modeļa vadītas programmas instance</span><span class="sxs-lookup"><span data-stu-id="a4197-152">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="a4197-153">Duālā ieraksta savienojuma iestatīšana starp esošo Finance and Operations programmas instanci un jaunu vai esošu modeļa vadītas programmas instanci pakalpojumu Dynamics 365 notiek Finance and Operation vidē.</span><span class="sxs-lookup"><span data-stu-id="a4197-153">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="a4197-154">Iestatiet savienojumu no Finance and Operations programmas.</span><span class="sxs-lookup"><span data-stu-id="a4197-154">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="a4197-155">Lai sinhronizētu esošos Common Data Service datus uz programmu Finance and Operations, [palaidiet](bootstrap-company-data.md) Common Data Service datus, izmantojot trīs burtu ISO uzņēmuma kodu.</span><span class="sxs-lookup"><span data-stu-id="a4197-155">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="a4197-156">Tā kā duālais ieraksts ir tiešsaistes sinhronizācijas režīmā, dati no Common Data Service automātiski sāk plūst uz Finance and Operations programmu.</span><span class="sxs-lookup"><span data-stu-id="a4197-156">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>
