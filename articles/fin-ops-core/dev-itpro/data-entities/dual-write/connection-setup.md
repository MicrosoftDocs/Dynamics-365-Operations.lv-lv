---
title: Norādījumi par duālā ieraksta iestatīšanu
description: Šajā tēmā aprakstīti scenāriji, kas tiek atbalstīti duālā ieraksta iestatījumiem.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 78a7cdc18476a1c523c83c92ca6f354c3ba806dc
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744857"
---
# <a name="guidance-for-dual-write-setup"></a><span data-ttu-id="5f84f-103">Norādījumi par duālā ieraksta iestatīšanu</span><span class="sxs-lookup"><span data-stu-id="5f84f-103">Guidance for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5f84f-104">Varat iestatīt duālā ieraksta savienojumu starp Finance and Operations vidi un Dataverse vidi.</span><span class="sxs-lookup"><span data-stu-id="5f84f-104">You can set up a dual-write connection between a Finance and Operations environment and a Dataverse environment.</span></span>

+ <span data-ttu-id="5f84f-105">**Finance and Operations vide** nodrošina **Finance and Operations programmu** (piemēram, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce un Dynamics 365 Human Resources) pamata platformu.</span><span class="sxs-lookup"><span data-stu-id="5f84f-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="5f84f-106">**Dataverse vide** nodrošina pamata platformu **Customer Engagement programmās** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing un Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="5f84f-106">A **Dataverse environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5f84f-107">Personāla vadības modulis Dynamics 365 Finance atbalsta duālās rakstīšanas savienojumus, bet Dynamics 365 Human Resources programma to neizmanto.</span><span class="sxs-lookup"><span data-stu-id="5f84f-107">The Human Resources module in Dynamics 365 Finance supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="5f84f-108">Iestatīšanas mehānisms mainās atkarībā no jūsu abonementa un vides.</span><span class="sxs-lookup"><span data-stu-id="5f84f-108">The setup mechanism varies, depending on your subscription and the environment:</span></span>

+ <span data-ttu-id="5f84f-109">Jaunajām Finance and Operations programmu instancēm duālā ieraksta savienojuma iestatījums sākas portālā Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="5f84f-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="5f84f-110">Ja jums ir Microsoft Power Platform licence, jūs saņemsit jaunu Dataverse vidi, ja jūsu nomniekam tādas nav.</span><span class="sxs-lookup"><span data-stu-id="5f84f-110">If you have a license for Microsoft Power Platform, you will get a new Dataverse environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="5f84f-111">Esošajām instancēm Finance and Operations programmās, duālā ieraksta savienojuma iestatīšana sākas Finance and Operations vidē.</span><span class="sxs-lookup"><span data-stu-id="5f84f-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="5f84f-112">Pirms sākat duālo rakstīšanu elementā, varat palaist sākotnējo sinhronizāciju, lai apstrādātu esošos datus abās pusēs: Finance and Operations programmas un klientu iesaistīšanas programmās.</span><span class="sxs-lookup"><span data-stu-id="5f84f-112">Before you start dual-write on an entity, you can run an initial synchronization to handle existing data on both sides: Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="5f84f-113">Varat izlaist sākotnējo sinhronizāciju, ja nav vajadzības sinhronizēt datus starp abām vidēm.</span><span class="sxs-lookup"><span data-stu-id="5f84f-113">You can skip the initial synchronization if you don't have to sync data between the two environments.</span></span>

<span data-ttu-id="5f84f-114">Veicot sākotnējo sinhronizāciju, varat kopēt esošos datus no vienas programmas uz citu divvirzienu formā.</span><span class="sxs-lookup"><span data-stu-id="5f84f-114">An initial synchronization lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="5f84f-115">Ir vairāki dažādi iestatīšanas scenāriji atkarībā no tā, kādas vides jums jau ir un kāda veida dati tajās ir.</span><span class="sxs-lookup"><span data-stu-id="5f84f-115">There are several setup scenarios, depending on the environments that you already have and the type of data in them.</span></span>

<span data-ttu-id="5f84f-116">Tālāk ir norādīti atbalstītie iestatīšanas scenāriji:</span><span class="sxs-lookup"><span data-stu-id="5f84f-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="5f84f-117">Jauna Finance and Operations programmas instance un jauna klientu iesaistīšanas programmas instance</span><span class="sxs-lookup"><span data-stu-id="5f84f-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="5f84f-118">Jauna Finance and Operations programmas instance un esoša klientu iesaistīšanas programmas instance</span><span class="sxs-lookup"><span data-stu-id="5f84f-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="5f84f-119">Jauna Finance and Operations programmas instance, kurai ir dati, un jauna klientu iesaistīšanas programmas instance</span><span class="sxs-lookup"><span data-stu-id="5f84f-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="5f84f-120">Jauna Finance and Operations programmas instance, kurai ir dati, un esoša klientu iesaistīšanas programmas instance</span><span class="sxs-lookup"><span data-stu-id="5f84f-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="5f84f-121">Esoša Finance and Operations programmas instance un jauna klientu iesaistīšanas programmas instance</span><span class="sxs-lookup"><span data-stu-id="5f84f-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="5f84f-122">Esoša Finance and Operations programmas instance un esoša klientu iesaistīšanas programmas instance</span><span class="sxs-lookup"><span data-stu-id="5f84f-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="5f84f-123">Jauna Finance and Operations programmas instance un jauna klientu iesaistīšanas programmas instance</span><span class="sxs-lookup"><span data-stu-id="5f84f-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="5f84f-124">Lai iestatītu duālā ieraksta savienojumu starp jaunu Finance and Operations programmas instanci, kurai nav datu, un jaunu klientu iesaistīšanas programmas instanci, veiciet darbības, kas aprakstītas rakstā [Duālā ieraksta iestatīšana no Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="5f84f-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="5f84f-125">Kad savienojuma iestatīšana ir pabeigta, automātiski tiek veiktas tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="5f84f-125">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="5f84f-126">Tiek nodrošināta jauna, tukša Finance and Operations vide.</span><span class="sxs-lookup"><span data-stu-id="5f84f-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="5f84f-127">Tiek nodrošināta jauna, tukša klientu iesaistīšanas programmas instance, kurā ir instalēts CRM galvenais risinājums.</span><span class="sxs-lookup"><span data-stu-id="5f84f-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="5f84f-128">Tiek izveidots duālā ieraksta savienojums DAT uzņēmuma datiem.</span><span class="sxs-lookup"><span data-stu-id="5f84f-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="5f84f-129">Tabulas kartes ir iespējotas tiešsaistes sinhronizācijai.</span><span class="sxs-lookup"><span data-stu-id="5f84f-129">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="5f84f-130">Abas vides pēc tam ir gatavas tiešsaistes datu sinhronizācijai.</span><span class="sxs-lookup"><span data-stu-id="5f84f-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="5f84f-131">Jauna Finance and Operations programmas instance un esoša klientu iesaistīšanas programmas instance</span><span class="sxs-lookup"><span data-stu-id="5f84f-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="5f84f-132">Lai iestatītu duālā ieraksta savienojumu starp jaunu Finance and Operations programmas instanci, kurai nav datu, un esošu klientu iesaistīšanas programmas instanci pakalpojumā Dynamics 365, veiciet darbības, kas aprakstītas rakstā [Duālā ieraksta iestatīšana no Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="5f84f-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="5f84f-133">Kad savienojuma iestatīšana ir pabeigta, automātiski tiek veiktas tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="5f84f-133">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="5f84f-134">Tiek nodrošināta jauna, tukša Finance and Operations vide.</span><span class="sxs-lookup"><span data-stu-id="5f84f-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="5f84f-135">Tiek izveidots duālā ieraksta savienojums DAT uzņēmuma datiem.</span><span class="sxs-lookup"><span data-stu-id="5f84f-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="5f84f-136">Tabulas kartes ir iespējotas tiešsaistes sinhronizācijai.</span><span class="sxs-lookup"><span data-stu-id="5f84f-136">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="5f84f-137">Abas vides pēc tam ir gatavas tiešsaistes datu sinhronizācijai.</span><span class="sxs-lookup"><span data-stu-id="5f84f-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="5f84f-138">Lai sinhronizētu esošos Dataverse datus uz Finance and Operations programmu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="5f84f-138">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="5f84f-139">Izveidojiet jaunu uzņēmumu Finance and Operations programmā.</span><span class="sxs-lookup"><span data-stu-id="5f84f-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="5f84f-140">Pievienojiet uzņēmumu duālā ieraksta savienojuma iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="5f84f-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="5f84f-141">[Palaidiet](bootstrap-company-data.md) datus Dataverse, izmantojot trīs burtu Starptautiskās Standartizācijas organizācijas (ISO) uzņēmuma kodu.</span><span class="sxs-lookup"><span data-stu-id="5f84f-141">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="5f84f-142">Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.</span><span class="sxs-lookup"><span data-stu-id="5f84f-142">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="5f84f-143">Lai skatītu saites uz piemēru un alternatīvu pieeju, skatiet sadaļu [Piemērs](#example) tālāk šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="5f84f-143">For links to an example and an alternative approach, see the [Example](#example) section later in this topic.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="5f84f-144">Jauna Finance and Operations programmas instance, kurai ir dati, un jauna klientu iesaistīšanas programmas instance</span><span class="sxs-lookup"><span data-stu-id="5f84f-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="5f84f-145">Lai iestatītu duālā ieraksta savienojumu starp jaunu Finance and Operations programmas instanci, kurā ir demonstrācijas dati, un jaunu klientu iesaistīšanas programmas instanci pakalpojumā Dynamics 365, izpildiet darbības, kas aprakstītas sadaļā [Jauna Finance and Operations programmas instance un jauna klientu iesaistīšanas programmas instance](#new-new) iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="5f84f-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="5f84f-146">Kad savienojuma iestatīšana ir pabeigta, ja vēlaties sinhronizēt demonstrācijas datus uz klientu iesaistīšanas programmu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="5f84f-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="5f84f-147">LCS lapā atveriet Finance and Operations programmu, piesakieties un pēc tam atveriet **Datu pārvaldība \> Duālais ieraksts**.</span><span class="sxs-lookup"><span data-stu-id="5f84f-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="5f84f-148">Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.</span><span class="sxs-lookup"><span data-stu-id="5f84f-148">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="5f84f-149">Lai skatītu saites uz piemēru un alternatīvu pieeju, skatiet sadaļu [Piemērs](#example).</span><span class="sxs-lookup"><span data-stu-id="5f84f-149">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="5f84f-150">Jauna Finance and Operations programmas instance, kurai ir dati, un esoša klientu iesaistīšanas programmas instance</span><span class="sxs-lookup"><span data-stu-id="5f84f-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="5f84f-151">Lai iestatītu duālā ieraksta savienojumu starp jaunu Finance and Operations programmas instanci, kurā ir demonstrācijas dati, un esošu klientu iesaistīšanas programmas instanci pakalpojumā Dynamics 365, izpildiet darbības, kas aprakstītas sadaļā [Jauna Finance and Operations programmas instance un esoša klientu iesaistīšanas programmas instance](#new-existing) iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="5f84f-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="5f84f-152">Kad savienojuma iestatīšana ir pabeigta, ja vēlaties sinhronizēt demonstrācijas datus uz klientu iesaistīšanas programmu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="5f84f-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="5f84f-153">LCS lapā atveriet Finance and Operations programmu, piesakieties un pēc tam atveriet **Datu pārvaldība \> Duālais ieraksts**.</span><span class="sxs-lookup"><span data-stu-id="5f84f-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="5f84f-154">Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.</span><span class="sxs-lookup"><span data-stu-id="5f84f-154">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="5f84f-155">Lai sinhronizētu esošos Dataverse datus uz Finance and Operations programmu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="5f84f-155">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="5f84f-156">Izveidojiet jaunu uzņēmumu Finance and Operations programmā.</span><span class="sxs-lookup"><span data-stu-id="5f84f-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="5f84f-157">Pievienojiet uzņēmumu duālā ieraksta savienojuma iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="5f84f-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="5f84f-158">[Palaidiet](bootstrap-company-data.md) Dataverse datus, izmantojot trīs burtu Starptautiskās Standartizācijas organizācijas (ISO) uzņēmuma kodu.</span><span class="sxs-lookup"><span data-stu-id="5f84f-158">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="5f84f-159">Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.</span><span class="sxs-lookup"><span data-stu-id="5f84f-159">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="5f84f-160">Lai skatītu saites uz piemēru un alternatīvu pieeju, skatiet sadaļu [Piemērs](#example).</span><span class="sxs-lookup"><span data-stu-id="5f84f-160">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="5f84f-161">Esoša Finance and Operations programmas instance un jauna klientu iesaistīšanas programmas instance</span><span class="sxs-lookup"><span data-stu-id="5f84f-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="5f84f-162">Duālā ieraksta savienojuma iestatīšana starp esošo Finance and Operations programmas instanci un jaunu vai esošu klientu iesaistīšanās programmas instanci notiek Finance and Operation vidē.</span><span class="sxs-lookup"><span data-stu-id="5f84f-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="5f84f-163">[Iestatiet savienojumu no Finance and Operations programmas](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="5f84f-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="5f84f-164">Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.</span><span class="sxs-lookup"><span data-stu-id="5f84f-164">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="5f84f-165">Lai skatītu saites uz piemēru un alternatīvu pieeju, skatiet sadaļu [Piemērs](#example).</span><span class="sxs-lookup"><span data-stu-id="5f84f-165">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="5f84f-166">Esoša Finance and Operations programmas instance un esoša klientu iesaistīšanas programmas instance</span><span class="sxs-lookup"><span data-stu-id="5f84f-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="5f84f-167">Duālā ieraksta savienojuma iestatīšana starp esošo Finance and Operations programmas instanci un esošu klientu iesaistīšanās programmas instanci pakalpojumu notiek Finance and Operation vidē.</span><span class="sxs-lookup"><span data-stu-id="5f84f-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="5f84f-168">[Iestatiet savienojumu no Finance and Operations programmas](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="5f84f-168">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="5f84f-169">Lai sinhronizētu esošos Dataverse datus uz programmu Finance and Operations, [palaidiet](bootstrap-company-data.md) Dataverse datus, izmantojot trīs burtu ISO uzņēmuma kodu.</span><span class="sxs-lookup"><span data-stu-id="5f84f-169">To sync the existing Dataverse data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="5f84f-170">Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.</span><span class="sxs-lookup"><span data-stu-id="5f84f-170">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="5f84f-171">Lai skatītu saites uz piemēru un alternatīvu pieeju, skatiet sadaļu [Piemērs](#example).</span><span class="sxs-lookup"><span data-stu-id="5f84f-171">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="example"></a><span data-ttu-id="5f84f-172">Paraugs</span><span class="sxs-lookup"><span data-stu-id="5f84f-172">Example</span></span>

<span data-ttu-id="5f84f-173">Piemēru skatiet [V3 klientu iespējošana — kontaktpersonu tabulas karte](enable-entity-map.md#enable-table-map)</span><span class="sxs-lookup"><span data-stu-id="5f84f-173">For an example, see [Enabling the Customers V3—Contacts table map](enable-entity-map.md#enable-table-map)</span></span>

<span data-ttu-id="5f84f-174">Lai varētu izmantot alternatīvu pieeju, kas balstās uz datu apjomu katrā elementā, kam jāpalaiž sākotnējā sinhronizāciju, skatiet [Apsvērumi par sākotnējo sinhronizāciju](initial-sync-guidance.md).</span><span class="sxs-lookup"><span data-stu-id="5f84f-174">For an alternative approach that is based on data volumes in each entity that must run an initial synchronization, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>
