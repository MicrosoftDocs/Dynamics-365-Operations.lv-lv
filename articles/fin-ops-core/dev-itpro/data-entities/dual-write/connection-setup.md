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
ms.openlocfilehash: 2d77a1458f3f4c79b231e6a6d7cc320b8ee1fad9
ms.sourcegitcommit: ee643d651d57560bccae2f99238faa39881f5c64
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088510"
---
# <a name="guidance-for-how-to-set-up-dual-write"></a><span data-ttu-id="851e1-103">Norādījumi par duālā ieraksta iestatīšanu</span><span class="sxs-lookup"><span data-stu-id="851e1-103">Guidance for how to set up dual-write</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="851e1-104">Varat iestatīt duālā ieraksta savienojumu starp Finance and Operations vidi un Common Data Service vidi.</span><span class="sxs-lookup"><span data-stu-id="851e1-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="851e1-105">**Finance and Operations vide** nodrošina **Finance and Operations programmu** (piemēram, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management un Dynamics 365 Retail) pamata platformu.</span><span class="sxs-lookup"><span data-stu-id="851e1-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, and Dynamics 365 Retail).</span></span>
+ <span data-ttu-id="851e1-106">**Common Data Service vide** nodrošina pamata platformu **klientu iesaistīšanas programmām** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing un Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="851e1-106">A **Common Data Service environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

>[!IMPORTANT]
><span data-ttu-id="851e1-107">Personāla vadība Finance and Operations atbalsta duālās rakstīšanas savienojumus, bet Dynamics 365 Human Resources programma to neizmanto.</span><span class="sxs-lookup"><span data-stu-id="851e1-107">Human Resources in Finance and Operations supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="851e1-108">Iestatīšanas mehānisms mainās atkarībā no jūsu abonementa un vides.</span><span class="sxs-lookup"><span data-stu-id="851e1-108">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="851e1-109">Jaunajām Finance and Operations programmu instancēm duālā ieraksta savienojuma iestatījums sākas portālā Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="851e1-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="851e1-110">Ja jums ir Power Platform licence, jūs saņemsit jaunu Common Data Service vidi, ja jūsu nomniekam tādas nav.</span><span class="sxs-lookup"><span data-stu-id="851e1-110">If you have a license for Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="851e1-111">Esošajām instancēm Finance and Operations programmās, duālā ieraksta savienojuma iestatīšana sākas Finance and Operations vidē.</span><span class="sxs-lookup"><span data-stu-id="851e1-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="851e1-112">Pirms sākat duālo rakstīšanu elementā, varat palaist sākotnējo sinhronizāciju, lai apstrādātu esošos datus abās programmu Finance and Operations un klientu iesaistīšanas programmu pusēs.</span><span class="sxs-lookup"><span data-stu-id="851e1-112">Before you start dual-write on an entity, you can run an initial sync to handle existing data on both sides of Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="851e1-113">Varat izlaist sākotnējo sinhronizāciju, ja nav nepieciešams sinhronizēt datus starp abām vidēm.</span><span class="sxs-lookup"><span data-stu-id="851e1-113">You can skip the initial sync if you don't need to synchronize data between the two environments.</span></span>

<span data-ttu-id="851e1-114">Veicot sākotnējo sinhronizāciju, varat kopēt esošos datus no vienas programmas uz citu divvirzienu formā.</span><span class="sxs-lookup"><span data-stu-id="851e1-114">An initial sync lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="851e1-115">Ir vairāki dažādi iestatīšanas scenāriji atkarībā no tā, kādas vides jums jau ir un kāda veida dati ir vidē.</span><span class="sxs-lookup"><span data-stu-id="851e1-115">There are several different setup scenarios depending on which environments you already have and what type of data is in the environments.</span></span>

<span data-ttu-id="851e1-116">Tālāk ir norādīti atbalstītie iestatīšanas scenāriji:</span><span class="sxs-lookup"><span data-stu-id="851e1-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="851e1-117">Jauna Finance and Operations programmas instance un jauna klientu iesaistīšanas programmas instance</span><span class="sxs-lookup"><span data-stu-id="851e1-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="851e1-118">Jauna Finance and Operations programmas instance un esoša klientu iesaistīšanas programmas instance</span><span class="sxs-lookup"><span data-stu-id="851e1-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="851e1-119">Jauna Finance and Operations programmas instance, kurai ir dati, un jauna klientu iesaistīšanas programmas instance</span><span class="sxs-lookup"><span data-stu-id="851e1-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="851e1-120">Jauna Finance and Operations programmas instance, kurai ir dati, un esoša klientu iesaistīšanas programmas instance</span><span class="sxs-lookup"><span data-stu-id="851e1-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="851e1-121">Esoša Finance and Operations programmas instance un jauna klientu iesaistīšanas programmas instance</span><span class="sxs-lookup"><span data-stu-id="851e1-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="851e1-122">Esoša Finance and Operations programmas instance un esoša klientu iesaistīšanas programmas instance</span><span class="sxs-lookup"><span data-stu-id="851e1-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="851e1-123">Jauna Finance and Operations programmas instance un jauna klientu iesaistīšanas programmas instance</span><span class="sxs-lookup"><span data-stu-id="851e1-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="851e1-124">Lai iestatītu duālā ieraksta savienojumu starp jaunu Finance and Operations programmas instanci, kurai nav datu, un jaunu klientu iesaistīšanas programmas instanci, veiciet darbības, kas aprakstītas rakstā [Duālā ieraksta iestatīšana no Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="851e1-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="851e1-125">Kad savienojuma iestatīšana ir pabeigta, automātiski tiek veiktas šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="851e1-125">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="851e1-126">Tiek nodrošināta jauna, tukša Finance and Operations vide.</span><span class="sxs-lookup"><span data-stu-id="851e1-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="851e1-127">Tiek nodrošināta jauna, tukša klientu iesaistīšanas programmas instance, kurā ir instalēts CRM galvenais risinājums.</span><span class="sxs-lookup"><span data-stu-id="851e1-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="851e1-128">Tiek izveidots duālā ieraksta savienojums DAT uzņēmuma datiem.</span><span class="sxs-lookup"><span data-stu-id="851e1-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="851e1-129">Elementa kartes ir iespējotas tiešsaistes sinhronizācijai.</span><span class="sxs-lookup"><span data-stu-id="851e1-129">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="851e1-130">Abas vides pēc tam ir gatavas tiešsaistes datu sinhronizācijai.</span><span class="sxs-lookup"><span data-stu-id="851e1-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="851e1-131">Jauna Finance and Operations programmas instance un esoša klientu iesaistīšanas programmas instance</span><span class="sxs-lookup"><span data-stu-id="851e1-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="851e1-132">Lai iestatītu duālā ieraksta savienojumu starp jaunu Finance and Operations programmas instanci, kurai nav datu, un esošu klientu iesaistīšanas programmas instanci pakalpojumā Dynamics 365, veiciet darbības, kas aprakstītas rakstā [Duālā ieraksta iestatīšana no Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="851e1-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="851e1-133">Kad savienojuma iestatīšana ir pabeigta, automātiski tiek veiktas šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="851e1-133">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="851e1-134">Tiek nodrošināta jauna, tukša Finance and Operations vide.</span><span class="sxs-lookup"><span data-stu-id="851e1-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="851e1-135">Tiek izveidots duālā ieraksta savienojums DAT uzņēmuma datiem.</span><span class="sxs-lookup"><span data-stu-id="851e1-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="851e1-136">Elementa kartes ir iespējotas tiešsaistes sinhronizācijai.</span><span class="sxs-lookup"><span data-stu-id="851e1-136">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="851e1-137">Abas vides pēc tam ir gatavas tiešsaistes datu sinhronizācijai.</span><span class="sxs-lookup"><span data-stu-id="851e1-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="851e1-138">Lai sinhronizētu esošos Common Data Service datus uz Finance and Operations programmu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="851e1-138">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="851e1-139">Izveidojiet jaunu uzņēmumu Finance and Operations programmā.</span><span class="sxs-lookup"><span data-stu-id="851e1-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="851e1-140">Pievienojiet uzņēmumu duālā ieraksta savienojuma iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="851e1-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="851e1-141">[Palaidiet](bootstrap-company-data.md) datus Common Data Service, izmantojot trīs burtu Starptautiskās Standartizācijas organizācijas (ISO) uzņēmuma kodu.</span><span class="sxs-lookup"><span data-stu-id="851e1-141">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="851e1-142">Palaidiet funkciju **Sākotnējās sinhronizācijas** entītijām, kurām vēlaties sinhronizēt datus.</span><span class="sxs-lookup"><span data-stu-id="851e1-142">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="851e1-143">Piemēru un alternatīvu pieeju skatiet sadaļā [Piemērs](#example).</span><span class="sxs-lookup"><span data-stu-id="851e1-143">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="851e1-144">Jauna Finance and Operations programmas instance, kurai ir dati, un jauna klientu iesaistīšanas programmas instance</span><span class="sxs-lookup"><span data-stu-id="851e1-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="851e1-145">Lai iestatītu duālā ieraksta savienojumu starp jaunu Finance and Operations programmas instanci, kurā ir demonstrācijas dati, un jaunu klientu iesaistīšanas programmas instanci pakalpojumā Dynamics 365, izpildiet darbības, kas aprakstītas sadaļā [Jauna Finance and Operations programmas instance un jauna klientu iesaistīšanas programmas instance](#new-new) iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="851e1-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="851e1-146">Kad savienojuma iestatīšana ir pabeigta, ja vēlaties sinhronizēt demonstrācijas datus uz klientu iesaistīšanas programmu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="851e1-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="851e1-147">LCS lapā atveriet Finance and Operations programmu, piesakieties un pēc tam atveriet **Datu pārvaldība \> Duālais ieraksts**.</span><span class="sxs-lookup"><span data-stu-id="851e1-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="851e1-148">Palaidiet funkciju **Sākotnējās sinhronizācijas** entītijām, kurām vēlaties sinhronizēt datus.</span><span class="sxs-lookup"><span data-stu-id="851e1-148">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="851e1-149">Piemēru un alternatīvu pieeju skatiet sadaļā [Piemērs](#example).</span><span class="sxs-lookup"><span data-stu-id="851e1-149">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="851e1-150">Jauna Finance and Operations programmas instance, kurai ir dati, un esoša klientu iesaistīšanas programmas instance</span><span class="sxs-lookup"><span data-stu-id="851e1-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="851e1-151">Lai iestatītu duālā ieraksta savienojumu starp jaunu Finance and Operations programmas instanci, kurā ir demonstrācijas dati, un esošu klientu iesaistīšanas programmas instanci pakalpojumā Dynamics 365, izpildiet darbības, kas aprakstītas sadaļā [Jauna Finance and Operations programmas instance un esoša klientu iesaistīšanas programmas instance](#new-existing) iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="851e1-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="851e1-152">Kad savienojuma iestatīšana ir pabeigta, ja vēlaties sinhronizēt demonstrācijas datus uz klientu iesaistīšanas programmu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="851e1-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="851e1-153">LCS lapā atveriet Finance and Operations programmu, piesakieties un pēc tam atveriet **Datu pārvaldība \> Duālais ieraksts**.</span><span class="sxs-lookup"><span data-stu-id="851e1-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="851e1-154">Palaidiet funkciju **Sākotnējās sinhronizācijas** entītijām, kurām vēlaties sinhronizēt datus.</span><span class="sxs-lookup"><span data-stu-id="851e1-154">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="851e1-155">Lai sinhronizētu esošos Common Data Service datus uz Finance and Operations programmu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="851e1-155">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="851e1-156">Izveidojiet jaunu uzņēmumu Finance and Operations programmā.</span><span class="sxs-lookup"><span data-stu-id="851e1-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="851e1-157">Pievienojiet uzņēmumu duālā ieraksta savienojuma iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="851e1-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="851e1-158">[Palaidiet](bootstrap-company-data.md) Common Data Service datus, izmantojot trīs burtu Starptautiskās Standartizācijas organizācijas (ISO) uzņēmuma kodu.</span><span class="sxs-lookup"><span data-stu-id="851e1-158">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="851e1-159">Palaidiet funkciju **Sākotnējās sinhronizācijas** entītijām, kurām vēlaties sinhronizēt datus.</span><span class="sxs-lookup"><span data-stu-id="851e1-159">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="851e1-160">Piemēru un alternatīvu pieeju skatiet sadaļā [Piemērs](#example).</span><span class="sxs-lookup"><span data-stu-id="851e1-160">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="851e1-161">Esoša Finance and Operations programmas instance un jauna klientu iesaistīšanas programmas instance</span><span class="sxs-lookup"><span data-stu-id="851e1-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="851e1-162">Duālā ieraksta savienojuma iestatīšana starp esošo Finance and Operations programmas instanci un jaunu vai esošu klientu iesaistīšanās programmas instanci notiek Finance and Operation vidē.</span><span class="sxs-lookup"><span data-stu-id="851e1-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="851e1-163">[Iestatiet savienojumu no Finance and Operations programmas](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="851e1-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="851e1-164">Palaidiet funkciju **Sākotnējās sinhronizācijas** entītijām, kurām vēlaties sinhronizēt datus.</span><span class="sxs-lookup"><span data-stu-id="851e1-164">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="851e1-165">Piemēru un alternatīvu pieeju skatiet sadaļā [Piemērs](#example).</span><span class="sxs-lookup"><span data-stu-id="851e1-165">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="851e1-166">Esoša Finance and Operations programmas instance un esoša klientu iesaistīšanas programmas instance</span><span class="sxs-lookup"><span data-stu-id="851e1-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="851e1-167">Duālā ieraksta savienojuma iestatīšana starp esošo Finance and Operations programmas instanci un esošu klientu iesaistīšanās programmas instanci pakalpojumu notiek Finance and Operation vidē.</span><span class="sxs-lookup"><span data-stu-id="851e1-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app  occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="851e1-168">Iestatiet savienojumu no Finance and Operations programmas.</span><span class="sxs-lookup"><span data-stu-id="851e1-168">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="851e1-169">Lai sinhronizētu esošos Common Data Service datus uz programmu Finance and Operations, [palaidiet](bootstrap-company-data.md) Common Data Service datus, izmantojot trīs burtu ISO uzņēmuma kodu.</span><span class="sxs-lookup"><span data-stu-id="851e1-169">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="851e1-170">Palaidiet funkciju **Sākotnējās sinhronizācijas** entītijām, kurām vēlaties sinhronizēt datus.</span><span class="sxs-lookup"><span data-stu-id="851e1-170">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="851e1-171">Piemēru un alternatīvu pieeju skatiet sadaļā [Piemērs](#example).</span><span class="sxs-lookup"><span data-stu-id="851e1-171">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="example"></a><span data-ttu-id="851e1-172">Paraugs</span><span class="sxs-lookup"><span data-stu-id="851e1-172">Example</span></span>

<span data-ttu-id="851e1-173">Piemēru skatiet sadaļā [V3 klientu iespējošana — kontaktpersonu elementa karte](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)</span><span class="sxs-lookup"><span data-stu-id="851e1-173">For an example, see [Enabling the Customers V3—Contacts entity map](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)</span></span>

<span data-ttu-id="851e1-174">Lai varētu izmantot alternatīvu pieeju, pamatojoties uz katra elementa datu apjomu, kas nepieciešams, lai veiktu sākotnējo sinhronizāciju, skatiet sadaļu [Apsvērumi par sākotnējo sinhronizāciju](initial-sync-guidance.md).</span><span class="sxs-lookup"><span data-stu-id="851e1-174">For an alternative approach based on data volumes in each entity that need to run initial sync, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>
