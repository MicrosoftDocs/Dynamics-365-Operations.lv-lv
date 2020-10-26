---
title: Jauktas realitātes ceļvežu nodrošināšana ražošanas darbiniekiem
description: Šajā tēmā skaidrots, kā integrēt ražošanas pārvaldības moduli programmā Microsoft Dynamics 365 Supply Chain Management ar Dynamics 365 Guides.
author: cabeln
manager: tfehr
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: d8c2da17d4e3df37c55844f0aad00f883725f741
ms.sourcegitcommit: c55fecae96b4bb27bc313ba10a97eddb9c91350a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989284"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a><span data-ttu-id="9ed71-103">Jauktas realitātes ceļvežu nodrošināšana ražošanas darbiniekiem</span><span class="sxs-lookup"><span data-stu-id="9ed71-103">Provide mixed-reality Guides for workers in production</span></span>

<span data-ttu-id="9ed71-104">Darbinieki ražošanas procesos gūs labumu no atbilstošām instrukcijām, kas tiek sniegtas īstajā laikā, ņemot vērā darba kontekstu.</span><span class="sxs-lookup"><span data-stu-id="9ed71-104">Workers in production processes will benefit from relevant instructions that are provided at the right time in the context of their work.</span></span> <span data-ttu-id="9ed71-105">*Instrukcijas* attiecas uz vairākiem darbu domēniem, tai skaitā: montāžu, pakalpojumiem, operācijām, sertificēšanu un drošību.</span><span class="sxs-lookup"><span data-stu-id="9ed71-105">*Instructions* apply in several domains of work, including: assembly, service, operations, certification, and safety.</span></span> <span data-ttu-id="9ed71-106">Visās šajās pamata biznesa funkcijās pastāvīgas apmācību instrukcijas var palīdzēt darbiniekiem sasniegt vairāk un strādāt labāk.</span><span class="sxs-lookup"><span data-stu-id="9ed71-106">Across all of these core business functions, ongoing training instructions can help empower workers to achieve more and work better.</span></span>

## <a name="introduction"></a><span data-ttu-id="9ed71-107">Ievads</span><span class="sxs-lookup"><span data-stu-id="9ed71-107">Introduction</span></span>

<span data-ttu-id="9ed71-108">Instrukcijas var sniegt dažādos veidos.</span><span class="sxs-lookup"><span data-stu-id="9ed71-108">You can provide instructions in different ways.</span></span> <span data-ttu-id="9ed71-109">Viena efektīva sistēma, kas piegādā nestandarta pielietojuma veidus [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).</span><span class="sxs-lookup"><span data-stu-id="9ed71-109">One efficient system that ships out of the box uses [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).</span></span>

<span data-ttu-id="9ed71-110">Dynamics 365 Guides var sniegt darbiniekiem iespējas, izmantojot praktiskas apmācības.</span><span class="sxs-lookup"><span data-stu-id="9ed71-110">Dynamics 365 Guides can help empower your employees with hands-on learning.</span></span> <span data-ttu-id="9ed71-111">Jūs varat definēt standartizētus procesus, izmantojot detalizētus norādījumus, kas iepazīstinās jūsu darbiniekus ar nepieciešamajiem rīkiem un daļām un parādīs darbiniekiem, kā izmantot šos rīkus reālās darba situācijās.</span><span class="sxs-lookup"><span data-stu-id="9ed71-111">You can define standardized processes with step-by-step instructions that guide your employees to the tools and parts they need and show employees how to use these tools in real work situations.</span></span>

<span data-ttu-id="9ed71-112">Varat pievienot ceļvežus dažādiem ražošanas kontroles aspektiem, tostarp:</span><span class="sxs-lookup"><span data-stu-id="9ed71-112">You can attach guides to various aspects of production control including:</span></span>

- [<span data-ttu-id="9ed71-113">Resursi</span><span class="sxs-lookup"><span data-stu-id="9ed71-113">Resources</span></span>](#resources)
- [<span data-ttu-id="9ed71-114">Resursu grupas</span><span class="sxs-lookup"><span data-stu-id="9ed71-114">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="9ed71-115">Izlaistās preces</span><span class="sxs-lookup"><span data-stu-id="9ed71-115">Released products</span></span>](#released-products)
- [<span data-ttu-id="9ed71-116">Formulas</span><span class="sxs-lookup"><span data-stu-id="9ed71-116">Formulas</span></span>](#formulas)
- [<span data-ttu-id="9ed71-117">Formulas versijas</span><span class="sxs-lookup"><span data-stu-id="9ed71-117">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="9ed71-118">Materiālu komplekti (MK)</span><span class="sxs-lookup"><span data-stu-id="9ed71-118">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="9ed71-119">MK versijas</span><span class="sxs-lookup"><span data-stu-id="9ed71-119">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="9ed71-120">Maršruti</span><span class="sxs-lookup"><span data-stu-id="9ed71-120">Routes</span></span>](#routes)
- [<span data-ttu-id="9ed71-121">Maršruta versijas</span><span class="sxs-lookup"><span data-stu-id="9ed71-121">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="9ed71-122">Maršruta operāciju relācijas</span><span class="sxs-lookup"><span data-stu-id="9ed71-122">Route operation relations</span></span>](#route-operation-relations)

> [!NOTE]
> <span data-ttu-id="9ed71-123">Varat arī pievienot ceļvežus, izmantojot līdzekļu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="9ed71-123">You can also attach Guides with Asset Management.</span></span> <span data-ttu-id="9ed71-124">Papildu informāciju par šo opciju skatiet šeit: [Integrējiet Dynamics 365 Supply Chain Management (līdzekļu pārvaldība) ar Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).</span><span class="sxs-lookup"><span data-stu-id="9ed71-124">For more information about that option, see [Integrate Dynamics 365 Supply Chain Management (Asset Management) with Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).</span></span>

<span data-ttu-id="9ed71-125">Kad zemākā līmeņa nodarbinātais izvēlas darbu ražotnē, izmantojot Supply Chain Management, nodarbinātais var redzēt [atbilstošos ceļvežus](#logic) darba kartē.</span><span class="sxs-lookup"><span data-stu-id="9ed71-125">When a first-line worker chooses a job on the shop floor through Supply Chain Management, the worker can see [the relevant guides](#logic) on the job card.</span></span> <span data-ttu-id="9ed71-126">Kad nodarbinātais izvēlas noteiktu ceļvedi, ekrānā tiek parādīts šī ceļveža QR kods.</span><span class="sxs-lookup"><span data-stu-id="9ed71-126">When the worker chooses a specific guide, a QR code for that guide is shown on the screen.</span></span> <span data-ttu-id="9ed71-127">Pēc tam nodarbinātais izmanto savu HoloLens, lai skenētu QR kodu, kas palaiž ceļvežus un parāda nepieciešamās instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="9ed71-127">The worker then uses their HoloLens to scan the QR code, which launches Guides and shows the required instructions.</span></span>

<span data-ttu-id="9ed71-128">Tālāk minētās apakšsadaļas apraksta dažus atlasītus scenārijus, kuros uzņēmumi dažādās nozarēs var redzēt vislielākos ieguvumus, izmantojot ceļvežus ražošanas instrukciju prezentēšanā.</span><span class="sxs-lookup"><span data-stu-id="9ed71-128">The following subsections describe a few selected scenarios where companies across industries can see the biggest value when using Guides to present instructions for manufacturing.</span></span>

### <a name="assembly"></a><span data-ttu-id="9ed71-129">Montāža</span><span class="sxs-lookup"><span data-stu-id="9ed71-129">Assembly</span></span>

<span data-ttu-id="9ed71-130">![Ceļvežu izmantošana montāžas uzdevumos](media/instruction-guides-hero-assembly.png "Ceļvežu izmantošana pakalpojumu uzdevumos")</span><span class="sxs-lookup"><span data-stu-id="9ed71-130">![Use Guides in assembly tasks](media/instruction-guides-hero-assembly.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="9ed71-131">Montāžas operāciju instrukcijas parāda nodarbinātajiem nepieciešamos rīkus un daļas un kā tos izmantot reālās darba situācijās.</span><span class="sxs-lookup"><span data-stu-id="9ed71-131">Instructions in assembly operations show workers the tools and parts they need and how to use them in real work situations.</span></span>

<span data-ttu-id="9ed71-132">Ražošanas vadītāji var izveidot un piešķirt ceļvežus, piemēram, [ražošanas maršrutiem](routes-operations.md), [operāciju relācijām](routes-operations.md#operation-relations) vai [materiālu komplektiem](bill-of-material-bom.md).</span><span class="sxs-lookup"><span data-stu-id="9ed71-132">Production managers can create and assign Guides, for example, for [production routes](routes-operations.md), [operation relations](routes-operations.md#operation-relations), or [bills of material](bill-of-material-bom.md).</span></span> <span data-ttu-id="9ed71-133">Nodarbinātie atradīs atbilstošās instrukcijas par attiecīgo operācijas pieredzi ražotnē.</span><span class="sxs-lookup"><span data-stu-id="9ed71-133">Workers will find the relevant instructions on the respective operation experience on the shop floor.</span></span>

### <a name="service"></a><span data-ttu-id="9ed71-134">Pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="9ed71-134">Service</span></span>

<span data-ttu-id="9ed71-135">![Ceļvežu izmantošana pakalpojumu uzdevumos](media/instruction-guides-hero-service.png "Ceļvežu izmantošana pakalpojumu uzdevumos")</span><span class="sxs-lookup"><span data-stu-id="9ed71-135">![Use Guides in service tasks](media/instruction-guides-hero-service.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="9ed71-136">Aprīkojiet tehniskos darbiniekus ar vadītām instrukcijām darba vietā, novēršot nepieciešamību ieplānot papildu apmeklējumus.</span><span class="sxs-lookup"><span data-stu-id="9ed71-136">Equip technicians with guided instructions at the job site, eliminating the need to schedule additional visits.</span></span>

<span data-ttu-id="9ed71-137">Pakalpojumu pārvaldnieki var piešķirt ceļvežus, piemēram, noteiktiem [produktiem](../../commerce/product.md), kas iepazīstina ar kvalitātes novērtējuma rutīnām.</span><span class="sxs-lookup"><span data-stu-id="9ed71-137">Service managers can assign Guides, for example, to specific [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="quality"></a><span data-ttu-id="9ed71-138">Kvalitāte</span><span class="sxs-lookup"><span data-stu-id="9ed71-138">Quality</span></span>

<span data-ttu-id="9ed71-139">![Ceļvežu izmantošana kvalitātes nodrošināšanas uzdevumos](media/instruction-guides-hero-quality.png "Ceļvežu izmantošana kvalitātes nodrošināšanas uzdevumos")</span><span class="sxs-lookup"><span data-stu-id="9ed71-139">![Use Guides in quality assurance tasks](media/instruction-guides-hero-quality.png "Use Guides in quality assurance tasks")</span></span>

<span data-ttu-id="9ed71-140">Ieviesiet jaunus procesus un nodrošiniet lielāku konsekvenci, pārvēršot nodarbināto zināšanas par atkārtoti izmantojamu rīku.</span><span class="sxs-lookup"><span data-stu-id="9ed71-140">Rollout new processes and ensure increased consistency by turning employee knowledge into a repeatable tool.</span></span>

<span data-ttu-id="9ed71-141">Kvalitātes nodrošināšanas pārvaldnieki var piešķirt ceļvežus, piemēram, noteiktiem [produktiem](../../commerce/product.md), kas iepazīstina ar kvalitātes novērtējuma rutīnām.</span><span class="sxs-lookup"><span data-stu-id="9ed71-141">Quality assurance managers can assign guides, for example, to [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="certifications"></a><span data-ttu-id="9ed71-142">Sertifikācijas</span><span class="sxs-lookup"><span data-stu-id="9ed71-142">Certifications</span></span>

<span data-ttu-id="9ed71-143">![Ceļvežu izmantošana ar sertifikāciju saistītos uzdevumos](media/instruction-guides-hero-certification.png "Ceļvežu izmantošana ar sertifikāciju saistītos uzdevumos")</span><span class="sxs-lookup"><span data-stu-id="9ed71-143">![Use Guides for certification related tasks](media/instruction-guides-hero-certification.png "Use Guides for certification related tasks")</span></span>

<span data-ttu-id="9ed71-144">Pārliecinieties, ka katrs nodarbinātais atbilst augstiem standartiem, ātri identificējot, kam un kur nepieciešama palīdzība.</span><span class="sxs-lookup"><span data-stu-id="9ed71-144">Ensure every employee meets high standards by quickly identifying who needs help and where.</span></span>

### <a name="safety"></a><span data-ttu-id="9ed71-145">Drošība</span><span class="sxs-lookup"><span data-stu-id="9ed71-145">Safety</span></span>

<span data-ttu-id="9ed71-146">![Ceļvežu izmantošana darba drošības instrukcijās](media/instruction-guides-hero-safety.png "Ceļvežu izmantošana darba drošības instrukcijās")</span><span class="sxs-lookup"><span data-stu-id="9ed71-146">![Use Guides in work safety instructions](media/instruction-guides-hero-safety.png "Use Guides in work safety instructions")</span></span>

<span data-ttu-id="9ed71-147">Sniedziet norādījumus, kas virtuāli iepazīstina ar bīstamām procedūrām pirms mēģinājuma tās veikt fiziskajā vidē.</span><span class="sxs-lookup"><span data-stu-id="9ed71-147">Provide instructions that walk through dangerous procedures virtually before attempting in the physical environment.</span></span> <span data-ttu-id="9ed71-148">Ar jaukas realitātes pieeju nodarbinātie var virtuāli gūt pieredzi ar bīstamām procedūrām.</span><span class="sxs-lookup"><span data-stu-id="9ed71-148">With a mixed reality approach, workers can experience dangerous procedures virtually.</span></span>

<span data-ttu-id="9ed71-149">Ražošanas vadītāji var nodrošināt īpašus norādījumus par rīkošanos ar bīstamiem materiāliem vai maigas apiešanās procedūrām, piešķirot instrukcijas [produkta krājumiem](../../commerce/product.md), [maršrutiem](routes-operations.md) un [operācijām](routes-operations.md#operation-relations).</span><span class="sxs-lookup"><span data-stu-id="9ed71-149">Production managers can provide dedicated handling instructions for hazardous material handling or delicate handling procedures by assigning instructions to [product items](../../commerce/product.md), [routes](routes-operations.md), and [operations](routes-operations.md#operation-relations).</span></span>

## <a name="get-started-with-instructions-and-guides"></a><span data-ttu-id="9ed71-150">Sāciet darbu ar instrukcijām un ceļvežiem</span><span class="sxs-lookup"><span data-stu-id="9ed71-150">Get started with instructions and Guides</span></span>

<span data-ttu-id="9ed71-151">Lai iespējotu instrukcijas ražošanas procesos, Supply Chain Management nodrošina gatavu integrāciju ar Dynamics 365 Guides.</span><span class="sxs-lookup"><span data-stu-id="9ed71-151">To enable instructions in production processes, Supply Chain Management provides an out-of-the-box integration with Dynamics 365 Guides.</span></span> <span data-ttu-id="9ed71-152">Lai izveidotu, uzturētu un piešķirtu jauktās realitātes instrukcijas ražošanas pamatlīdzekļiem un darbam, nepieciešama licencēta un instalēta Guides programmas instance.</span><span class="sxs-lookup"><span data-stu-id="9ed71-152">A licensed and installed application instance of Guides is required to build, maintain, and assign mixed reality instructions to production assets and work.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="9ed71-153">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="9ed71-153">Prerequisites</span></span>

<span data-ttu-id="9ed71-154">Lai izmantotu šo līdzekli, jūsu sistēmā jābūt iekļautam tālāk minētajam:</span><span class="sxs-lookup"><span data-stu-id="9ed71-154">To use this feature, your system must include the following:</span></span>

- <span data-ttu-id="9ed71-155">Dynamics 365 Supply Chain Management versija 10.0.15 vai jaunāka versija</span><span class="sxs-lookup"><span data-stu-id="9ed71-155">Dynamics 365 Supply Chain Management version 10.0.15 or later</span></span>
- <span data-ttu-id="9ed71-156">[Duālā rakstīšana](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) Supply Chain Management lietojumprogrammām.</span><span class="sxs-lookup"><span data-stu-id="9ed71-156">[Dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) for Supply Chain Management apps.</span></span>
- <span data-ttu-id="9ed71-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) versija 400.0.1.48 vai jaunāka versija</span><span class="sxs-lookup"><span data-stu-id="9ed71-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 400.0.1.48 or later</span></span>

### <a name="turn-on-the-feature"></a><span data-ttu-id="9ed71-158">Līdzekļa iespējošana</span><span class="sxs-lookup"><span data-stu-id="9ed71-158">Turn on the feature</span></span>

<span data-ttu-id="9ed71-159">Lai līdzeklis būtu pieejams jūsu sistēmā, ir jāiespējo tā konfigurācijas atslēgas.</span><span class="sxs-lookup"><span data-stu-id="9ed71-159">To make the feature available on your system, you must enable its configuration keys.</span></span> <span data-ttu-id="9ed71-160">Tas jādara tikai vienreiz.</span><span class="sxs-lookup"><span data-stu-id="9ed71-160">You only need to do this once.</span></span> <span data-ttu-id="9ed71-161">Lai to izdarītu, administratoram jāveic šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="9ed71-161">To do this, an administrator must do the following:</span></span>

1. <span data-ttu-id="9ed71-162">Ielieciet savu sistēmu uzturēšanas režīmā, kā aprakstīts sadaļā [Uzturēšanas režīms](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="9ed71-162">Place your system into maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="9ed71-163">Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Licences konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-163">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="9ed71-164">Izvērsiet sadaļu **Jauktā realitāte** un tad atzīmējiet izvēles rūtiņu **Jauktās realitātes ceļvedis**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-164">Expand the **Mixed reality** section and then select the **Mixed reality guide** check box.</span></span>
1. <span data-ttu-id="9ed71-165">Izvērsiet sadaļu **Produktu pārvaldība** un tad atzīmējiet izvēles rūtiņu **Produktu instrukcijas**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-165">Expand the **Production management** section and then select the **Production instructions** check box.</span></span>
1. <span data-ttu-id="9ed71-166">Izslēdziet uzturēšanas režīmu, kā aprakstīts sadaļā [Uzturēšanas režīms](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="9ed71-166">Turn off maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a><span data-ttu-id="9ed71-167">Ceļvežu ražotnē parādīšanās veida konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="9ed71-167">Configure how Guides appear on the shop floor</span></span>

<span data-ttu-id="9ed71-168">Lai konfigurētu, kā ceļveži parādās ražotnē, dodieties uz **Jauktā realitāte \> Dynamics 365 Guides \> Konfigurēt ceļvežu integrāciju**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-168">To configure how Guides appear on the shop floor, go to **Mixed Reality \> Dynamics 365 Guides \> Configure Guides integration**.</span></span>

<span data-ttu-id="9ed71-169">![Konfigurējiet ceļvežu integrāciju ražošanai](media/instruction-guides-configure-integration.png "Konfigurējiet ceļvežu integrāciju ražošanai")</span><span class="sxs-lookup"><span data-stu-id="9ed71-169">![Configure Guide integration for manufacturing](media/instruction-guides-configure-integration.png "Configure Guide integration for manufacturing")</span></span>

<span data-ttu-id="9ed71-170">Iestatiet tālāk minētos laukus:</span><span class="sxs-lookup"><span data-stu-id="9ed71-170">Set the following fields:</span></span>

- <span data-ttu-id="9ed71-171">**CDS vides apakšdomēns** — šim laukam jau vajadzētu parādīt vērtību.</span><span class="sxs-lookup"><span data-stu-id="9ed71-171">**CDS environment subdomain** - This field should already show a value.</span></span> <span data-ttu-id="9ed71-172">Šajā laukā ir ietverts Common Data Service vides, kurā tiek veidoti jūsu ceļveži, apakšdomēns.</span><span class="sxs-lookup"><span data-stu-id="9ed71-172">This field holds the subdomain for the Common Data Service environment where you create your Guides.</span></span> <span data-ttu-id="9ed71-173">Apakšdomēns ir pirmā URL daļa un parasti tiek nosaukts līdzīgi organizācijas nosaukumam.</span><span class="sxs-lookup"><span data-stu-id="9ed71-173">The subdomain is the first part of the URL and is typically named after your organization.</span></span> <span data-ttu-id="9ed71-174">Piemēram, ja jūsu Common Data Service URL ir "contoso.crm4.dynamics.com", šeit jāievada *contoso*.</span><span class="sxs-lookup"><span data-stu-id="9ed71-174">For example, if your Common Data Service URL is "contoso.crm4.dynamics.com", you should enter *contoso* here.</span></span> <span data-ttu-id="9ed71-175">Šī vērtība tiek izmantota, lai sastādītu jūsu ceļvežu adreses, un tā tiks iekodēta QR kodos.</span><span class="sxs-lookup"><span data-stu-id="9ed71-175">This value is used to compose addresses for your guides and will be encoded into the QR codes.</span></span>
- <span data-ttu-id="9ed71-176">**QR koda izmērs** — iestatiet atveidotā QR koda izmēru.</span><span class="sxs-lookup"><span data-stu-id="9ed71-176">**QR code size** - Set the size of the rendered QR code.</span></span> <span data-ttu-id="9ed71-177">Ieteicams izvēlēties izmēru, kas aizpildīs lielāko daļu displeja ekrāna, bet ne lielāku.</span><span class="sxs-lookup"><span data-stu-id="9ed71-177">We recommend choosing a size that will fill most of your display screen, but not more.</span></span> <span data-ttu-id="9ed71-178">Parasti *15* ir laba vērtība.</span><span class="sxs-lookup"><span data-stu-id="9ed71-178">Typically, *15* is a good value.</span></span>
- <span data-ttu-id="9ed71-179">**QR koda kļūdu labošanas līmenis** — iestatiet QR koda granularitāti.</span><span class="sxs-lookup"><span data-stu-id="9ed71-179">**QR code error correction level** - Set the granularity of the QR code.</span></span> <span data-ttu-id="9ed71-180">Lielāka granularitāte var paaugstināt koda uzticamību, bet jūsu **QR koda izmēram** ir jābūt pietiekami lielam, lai varētu atbalstīt detalizācijas līmeni, kāds nepieciešams jūsu atlasītajam labošanas līmenim.</span><span class="sxs-lookup"><span data-stu-id="9ed71-180">Higher granularity can help increase the code's reliability, but your **QR code size** must be large enough to support the level of detail required by your selected correction level.</span></span>


> [!TIP]
> - <span data-ttu-id="9ed71-181">QR kodu izmēri, kas ir pārāk lieli displejam, aizņems mazliet ilgāku laiku, lai tos atveidotu un pēc tam mērogotu, lai tas atbilstu jūsu displeja izmēram.</span><span class="sxs-lookup"><span data-stu-id="9ed71-181">QR codes sizes that are too large for your display will take a bit longer to render and then be scaled down to fit your display.</span></span> <span data-ttu-id="9ed71-182">Tie nenodrošina priekšrocības.</span><span class="sxs-lookup"><span data-stu-id="9ed71-182">These do not provide a benefit.</span></span>
> - <span data-ttu-id="9ed71-183">QR koda izmēri, kas ir pārāk mazi, var samazināt HoloLens spēju dažās vidēs pareizi nolasīt kodu.</span><span class="sxs-lookup"><span data-stu-id="9ed71-183">QR code sizes that are too small may decrease the ability of HoloLens to read the code properly in some environments.</span></span>
> - <span data-ttu-id="9ed71-184">Mēs iesakām pārbaudīt iestatījumus katrai ierīcei, kas parādīs QR kodus HoloLens lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="9ed71-184">We recommend that you test the settings for each device that will display QR codes for HoloLens users.</span></span> <span data-ttu-id="9ed71-185">Izvēlieties iestatījumus, kas nodrošina pietiekamu lasāmību jūsu ražotnes vidē.</span><span class="sxs-lookup"><span data-stu-id="9ed71-185">Choose settings that provide sufficient readability in your shop floor environment.</span></span>  

## <a name="get-an-overview-of-all-guide-assignments"></a><span data-ttu-id="9ed71-186">Visu ceļvežu norīkojumu pārskata iegūšana</span><span class="sxs-lookup"><span data-stu-id="9ed71-186">Get an overview of all Guide assignments</span></span>

<span data-ttu-id="9ed71-187">Izmantojiet lapu **Visi ceļveži**, lai redzētu sarakstu ar visiem jūsu organizācijā pieejamajiem ceļvežiem un visiem norīkojumiem, kas piešķirti jūsu ražošanas procesiem un resursiem.</span><span class="sxs-lookup"><span data-stu-id="9ed71-187">Use the **All Guides** page to see the list of all available Guides in your organization and all assignments to your production processes and resources.</span></span> <span data-ttu-id="9ed71-188">Lai to atvērtu, dodieties uz **Jauktā realitāte \> Ceļveži \> Visi ceļveži**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-188">To open it, go to **Mixed reality \> Guides \> All Guides**.</span></span> <span data-ttu-id="9ed71-189">Saraksta augšpusē parādīti visi pieejamie ceļveži, un jūs varat izmantot šeit pieejamo lauku, lai filtrētu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="9ed71-189">The list at the top shows all the available Guides and you can use the field here to filter the list.</span></span> <span data-ttu-id="9ed71-190">Saraksta apakšpusē parādīti visi ceļvežu norīkojumi un ir nodrošināta rīkjosla to pārvaldībai.</span><span class="sxs-lookup"><span data-stu-id="9ed71-190">The list at the bottom shows all Guide assignments and provides a toolbar for managing them.</span></span>

<span data-ttu-id="9ed71-191">![Ceļvežu pārvaldība](media/instruction-guides-allguides.png "Ceļvežu pārvaldība")</span><span class="sxs-lookup"><span data-stu-id="9ed71-191">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

<span data-ttu-id="9ed71-192">Turpmākajās sadaļās ir aprakstīti objektu tipi, kam var piešķirt ceļvežus.</span><span class="sxs-lookup"><span data-stu-id="9ed71-192">The following sections describe the types of objects that you can assign Guides to.</span></span> <span data-ttu-id="9ed71-193">Katrs piešķirtais ceļvedis sniedz instrukcijas, kas tiek automātiski pievienotas attiecīgajiem ražošanas darbiem un būs pieejamas ražotnē.</span><span class="sxs-lookup"><span data-stu-id="9ed71-193">Each assigned guide provides instructions that are automatically attached to the respective production jobs and will be available on the shop floor.</span></span>

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a><span data-ttu-id="9ed71-194">Saistīt ceļvedi ar resursu</span><span class="sxs-lookup"><span data-stu-id="9ed71-194">Associate a Guide to a resource</span></span>

<span data-ttu-id="9ed71-195">Pievienojiet ceļvedi [resursam](operations-resources.md), lai piedāvātu ceļvedi attiecīgo ražošanas darbu kontekstā.</span><span class="sxs-lookup"><span data-stu-id="9ed71-195">Add a Guide to a [resource](operations-resources.md) to offer the Guide in the context of relevant production jobs.</span></span>

### <a name="typical-scenario-using-resources"></a><span data-ttu-id="9ed71-196">Tipisks scenārijs, izmantojot resursus</span><span class="sxs-lookup"><span data-stu-id="9ed71-196">Typical scenario using resources</span></span>

<span data-ttu-id="9ed71-197">Piemēram, jūs varētu pievienot ceļvedi ar vispārējām iekārtas drošības instrukcijām vai norādījumiem par rīkošanos resursam vai iekārtas veidam.</span><span class="sxs-lookup"><span data-stu-id="9ed71-197">For example, you could attach a Guide with general machine security or handling instructions to a resource of type machine.</span></span> <span data-ttu-id="9ed71-198">Pēc tam ceļvedis būs pieejams katrā darbā, kas veikts pie attiecīgās iekārtas.</span><span class="sxs-lookup"><span data-stu-id="9ed71-198">Then, the Guide will be available on every job that is performed on the machine.</span></span>

### <a name="add-a-guide-to-a-resource"></a><span data-ttu-id="9ed71-199">Ceļveža pievienošana resursam</span><span class="sxs-lookup"><span data-stu-id="9ed71-199">Add a Guide to a resource</span></span>

<span data-ttu-id="9ed71-200">Lai pievienotu ceļvedi resursam:</span><span class="sxs-lookup"><span data-stu-id="9ed71-200">To add a Guide to a resource:</span></span>

1. <span data-ttu-id="9ed71-201">Dodieties uz **Ražošanas kontrole \> Uzstādīšana \> Resursi \> Resursi**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-201">Go to **Production control \> Setup \> Resources \> Resources**.</span></span>
1. <span data-ttu-id="9ed71-202">No saraksta rūts atlasiet resursu, kuram vēlaties piešķirt ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="9ed71-202">From the list pane, select the resource you want to assign a Guide to.</span></span>
1. <span data-ttu-id="9ed71-203">Paplašiniet kopsavilkuma cilni **Saistītie ceļveži**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-203">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="9ed71-204">Atlasiet **Pievienot** rīkjoslā **Saistītie ceļveži**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-204">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="9ed71-205">Režģim tiek pievienota jauna rinda.</span><span class="sxs-lookup"><span data-stu-id="9ed71-205">A new line is added to the grid.</span></span>
1. <span data-ttu-id="9ed71-206">Jaunajai rindai lietojiet nolaižamo sarakstu kolonnā **Nosaukums**, lai izvēlētos ceļvedi, ko vēlaties piešķirt.</span><span class="sxs-lookup"><span data-stu-id="9ed71-206">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="9ed71-207">Ja jums ir daudz ceļvežu, tad varat filtrēt sarakstu, lai atrastu meklēto.</span><span class="sxs-lookup"><span data-stu-id="9ed71-207">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="9ed71-208">![Ceļvežu pārvaldība](media/instruction-guides-allguides.png "Ceļvežu pārvaldība")</span><span class="sxs-lookup"><span data-stu-id="9ed71-208">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a><span data-ttu-id="9ed71-209">Saistīt ceļvedi ar resursu grupu</span><span class="sxs-lookup"><span data-stu-id="9ed71-209">Associate a Guide to a resource group</span></span>

<span data-ttu-id="9ed71-210">Varat pievienot ceļvedi [resursu grupām](tasks/define-discrete-manufacturing-resource-group.md), ja izmantojat tos, lai pārvaldītu iekārtu grupas, ražošanas rindas vai darba šūnas.</span><span class="sxs-lookup"><span data-stu-id="9ed71-210">You can add a guide to [resource groups](tasks/define-discrete-manufacturing-resource-group.md) if you use them to manage groups of machines, production lines, or work cells.</span></span>

### <a name="typical-scenarios-using-resource-groups"></a><span data-ttu-id="9ed71-211">Tipiski scenāriji, izmantojot resursu grupas</span><span class="sxs-lookup"><span data-stu-id="9ed71-211">Typical scenarios using resource groups</span></span>

<span data-ttu-id="9ed71-212">**1. piemērs:** ir definēta resursu grupa vairākām viena modeļa iekārtām.</span><span class="sxs-lookup"><span data-stu-id="9ed71-212">**Example 1:** You have defined a resource group for several machines of the same model.</span></span> <span data-ttu-id="9ed71-213">Tā vietā, lai piešķirtu iekārtas modelim atbilstošos norādījumus par rīkošanos katram atbilstošajam resursam, jūs varat piešķirt ceļvedi resursu grupai, kas atspoguļo iekārtas modeli.</span><span class="sxs-lookup"><span data-stu-id="9ed71-213">Instead of assigning the relevant handling instruction guide for the machine model to every relevant resource, you could instead assign the Guide to the resource group that reflects that machine model.</span></span>

<span data-ttu-id="9ed71-214">**2. piemērs:** ir definēta resursu grupa darba šūnai, kas satur dažādas iekārtas, un jums ir ceļvedis, kas sniedz vispārīgus norādījumus par to, kā uzturēt darba šūnu.</span><span class="sxs-lookup"><span data-stu-id="9ed71-214">**Example 2:** You have defined a resource group for a work cell that contains different machines and you have a Guide that provides general instructions for how to maintain the work cell.</span></span> <span data-ttu-id="9ed71-215">Ceļvedis attiecas uz visām ražošanas aktivitātēm šajā darba šūnā.</span><span class="sxs-lookup"><span data-stu-id="9ed71-215">The Guide applies to any production activity in this work cell.</span></span>

### <a name="add-a-guide-to-a-resource-group"></a><span data-ttu-id="9ed71-216">Ceļveža pievienošana resursu grupai</span><span class="sxs-lookup"><span data-stu-id="9ed71-216">Add a Guide to a resource group</span></span>

<span data-ttu-id="9ed71-217">Lai pievienotu ceļvedi resursu grupai:</span><span class="sxs-lookup"><span data-stu-id="9ed71-217">To add a Guide to a resource group:</span></span>

1. <span data-ttu-id="9ed71-218">Dodieties uz **Ražošanas kontrole \> Uzstādīšana \> Resursi \> Resursu grupas**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-218">Go to **Production control \> Setup \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="9ed71-219">No saraksta rūts atlasiet resursu grupu, kam vēlaties piešķirt ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="9ed71-219">From the list pane, select the resource group you want to assign a Guide to.</span></span>
1. <span data-ttu-id="9ed71-220">Paplašiniet kopsavilkuma cilni **Saistītie ceļveži**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-220">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="9ed71-221">Atlasiet **Pievienot** rīkjoslā **Saistītie ceļveži**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-221">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="9ed71-222">Režģim tiek pievienota jauna rinda.</span><span class="sxs-lookup"><span data-stu-id="9ed71-222">A new line is added to the grid.</span></span>
1. <span data-ttu-id="9ed71-223">Jaunajai rindai lietojiet nolaižamo sarakstu kolonnā **Nosaukums**, lai izvēlētos ceļvedi, ko vēlaties piešķirt.</span><span class="sxs-lookup"><span data-stu-id="9ed71-223">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="9ed71-224">Ja jums ir daudz ceļvežu, tad varat filtrēt sarakstu, lai atrastu meklēto.</span><span class="sxs-lookup"><span data-stu-id="9ed71-224">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="9ed71-225">![Ceļveža pievienošana resursu grupai](media/instruction-guides-resourcegroup.png "Ceļveža pievienošana resursu grupai")</span><span class="sxs-lookup"><span data-stu-id="9ed71-225">![Adding a Guide to a resource group](media/instruction-guides-resourcegroup.png "Adding a Guide to a resource group")</span></span>

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a><span data-ttu-id="9ed71-226">Ceļveža saistīšana ar izlaistu preci</span><span class="sxs-lookup"><span data-stu-id="9ed71-226">Associate a Guide to a released product</span></span>

<span data-ttu-id="9ed71-227">Varat pievienot ceļvedi jebkurai [izlaistai precei](../pim/tasks/create-released-product-single-company.md).</span><span class="sxs-lookup"><span data-stu-id="9ed71-227">You can add a guide to any [released product](../pim/tasks/create-released-product-single-company.md).</span></span>

### <a name="typical-scenario-using-released-products"></a><span data-ttu-id="9ed71-228">Tipisks scenārijs, izmantojot izlaistas preces</span><span class="sxs-lookup"><span data-stu-id="9ed71-228">Typical scenario using released products</span></span>

<span data-ttu-id="9ed71-229">Preču līmeņa ceļveži palīdz ražotnes darbiniekiem ar instrukcijām, kas attiecas uz specifisku izlaistu preču vai krājumu pārvaldību vai apstrādi.</span><span class="sxs-lookup"><span data-stu-id="9ed71-229">Product-level Guides help shop floor workers with instructions relevant to operating or handling a specific released product or item.</span></span>

### <a name="add-a-guide-to-a-released-product"></a><span data-ttu-id="9ed71-230">Ceļveža pievienošana izlaistai precei</span><span class="sxs-lookup"><span data-stu-id="9ed71-230">Add a Guide to a released product</span></span>

<span data-ttu-id="9ed71-231">Lai pievienotu ceļvedi izlaistai precei:</span><span class="sxs-lookup"><span data-stu-id="9ed71-231">To add a Guide to a released product:</span></span>

1. <span data-ttu-id="9ed71-232">Dodieties uz **Ražošanas informācijas pārvaldība \> Preces \> Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-232">Go to **Production information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="9ed71-233">Atveriet preci, kurai vēlaties piešķirt ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="9ed71-233">Open the product you want to assign a Guide to.</span></span>
1. <span data-ttu-id="9ed71-234">Darbības rūtī atveriet cilni **Inženieris** un grupā **Skats** atlasiet **Saistītie ceļveži**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-234">On the Action Pane, open the **Engineer** tab and from the **View** group, select **Associated Guides**.</span></span>
1. <span data-ttu-id="9ed71-235">Jūsu atlasītajai precei tiek atvērta lapa **Saistītie ceļveži**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-235">The **Associated Guides** page opens for your selected product.</span></span>
1. <span data-ttu-id="9ed71-236">Lai režģim pievienotu jaunu rindu, darbības rūtī atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-236">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="9ed71-237">Jaunajai rindai lietojiet nolaižamo sarakstu kolonnā **Nosaukums**, lai izvēlētos ceļvedi, ko vēlaties piešķirt.</span><span class="sxs-lookup"><span data-stu-id="9ed71-237">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="9ed71-238">![Ceļveža pievienošana izlaistai precei:](media/instruction-guides-ReleasedProduct-AddGuides.png "Ceļveža pievienošana izlaistai precei")</span><span class="sxs-lookup"><span data-stu-id="9ed71-238">![Adding a Guide to a released product](media/instruction-guides-ReleasedProduct-AddGuides.png "Adding a Guide to a released product")</span></span>

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a><span data-ttu-id="9ed71-239">Saistīt ceļvedi ar formulu</span><span class="sxs-lookup"><span data-stu-id="9ed71-239">Associate a Guide to a formula</span></span>

<span data-ttu-id="9ed71-240">Varat pievienot ceļvedi jebkurai [formulai](bill-of-material-bom.md#formulas-co-products-and-by-products).</span><span class="sxs-lookup"><span data-stu-id="9ed71-240">You can add a guide to any [formula](bill-of-material-bom.md#formulas-co-products-and-by-products).</span></span>

### <a name="typical-scenario-using-formulas"></a><span data-ttu-id="9ed71-241">Tipisks scenārijs, izmantojot formulas</span><span class="sxs-lookup"><span data-stu-id="9ed71-241">Typical scenario using formulas</span></span>
  
<span data-ttu-id="9ed71-242">Formulas līmeņa ceļveži sniedz ražotnes darbiniekiem vadītus norādījumus par rīkošanos formulas vai receptes kontekstā.</span><span class="sxs-lookup"><span data-stu-id="9ed71-242">Formula-level Guides provide shop floor workers with guided handling instructions in the context of a formula or recipe.</span></span> <span data-ttu-id="9ed71-243">Ceļvežus var piešķirt arī formulas versijām.</span><span class="sxs-lookup"><span data-stu-id="9ed71-243">Guides can also be assigned to versions of a formula.</span></span>

> [!NOTE]
> <span data-ttu-id="9ed71-244">Varat piešķirt norādījumus, kas attiecas uz ražošanas procesiem, pamatojoties uz formulu maršrutam, maršruta versijai vai maršruta operāciju relācijām.</span><span class="sxs-lookup"><span data-stu-id="9ed71-244">You can assign guidance relevant for production processes based on a formula to a route, route version, or route operation relations.</span></span>  

> <span data-ttu-id="9ed71-245">Pašlaik ceļvežus nevar pievienot atsevišķām formulas rindām.</span><span class="sxs-lookup"><span data-stu-id="9ed71-245">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula"></a><span data-ttu-id="9ed71-246">Ceļveža pievienošana formulai</span><span class="sxs-lookup"><span data-stu-id="9ed71-246">Add a Guide to a formula</span></span>

<span data-ttu-id="9ed71-247">Lai ceļvedi pievienotu formulai:</span><span class="sxs-lookup"><span data-stu-id="9ed71-247">To add a Guide to a formula:</span></span>

1. <span data-ttu-id="9ed71-248">Dodieties uz **Ražošanas informācijas pārvaldība \> Materiālu komplekti un formulas \> Formulas**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-248">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="9ed71-249">Atveriet formulu, kurai vēlaties piešķirt ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="9ed71-249">Open the formula you want to assign a Guide to.</span></span>
1. <span data-ttu-id="9ed71-250">Atveriet cilni **Galvene** virs augšējās kopsavilkuma cilnes.</span><span class="sxs-lookup"><span data-stu-id="9ed71-250">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="9ed71-251">Paplašiniet kopsavilkuma cilni **Saistītie ceļveži**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-251">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="9ed71-252">Atlasiet **Pievienot** rīkjoslā **Saistītie ceļveži**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-252">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="9ed71-253">Režģim tiek pievienota jauna rinda.</span><span class="sxs-lookup"><span data-stu-id="9ed71-253">A new line is added to the grid.</span></span>
1. <span data-ttu-id="9ed71-254">Jaunajai rindai lietojiet nolaižamo sarakstu kolonnā **Nosaukums**, lai izvēlētos ceļvedi, ko vēlaties piešķirt.</span><span class="sxs-lookup"><span data-stu-id="9ed71-254">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="9ed71-255">![Ceļveža pievienošana formulai:](media/instruction-guides-Formula.png "Ceļveža pievienošana formulai")</span><span class="sxs-lookup"><span data-stu-id="9ed71-255">![Adding a Guide to a formula](media/instruction-guides-Formula.png "Adding a Guide to a formula")</span></span>

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a><span data-ttu-id="9ed71-256">Saistīt ceļvedi ar formulas versiju</span><span class="sxs-lookup"><span data-stu-id="9ed71-256">Associate a Guide to a formula version</span></span>

<span data-ttu-id="9ed71-257">Varat pievienot ceļvedi jebkurai [formulas versijai](bill-of-material-bom.md#bom-and-formula-versions).</span><span class="sxs-lookup"><span data-stu-id="9ed71-257">You can add a guide to any [formula version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-formula-versions"></a><span data-ttu-id="9ed71-258">Tipisks scenārijs, izmantojot formulas versijas</span><span class="sxs-lookup"><span data-stu-id="9ed71-258">Typical scenario using formula versions</span></span>

<span data-ttu-id="9ed71-259">Ceļveži, kas pievienoti atsevišķai formulas versijai sniedz ražotnes darbiniekiem instrukcijas, kas iepazīstina ar formulas receptes attiecīgās versijas ražošanu.</span><span class="sxs-lookup"><span data-stu-id="9ed71-259">Guides attached to an individual version of a formula provide shop floor workers with instructions that walk through the production of that version of the formula recipe.</span></span>

> [!TIP]
> <span data-ttu-id="9ed71-260">Varat piešķirt norādījumus, kas attiecas uz ražošanas procesiem, pamatojoties uz šīs formulas versiju maršrutam, maršruta versijai vai maršruta operāciju relācijām.</span><span class="sxs-lookup"><span data-stu-id="9ed71-260">You can assign guidance relevant for production processes based on this formula version to a route, route version, or route operation relations.</span></span>  

> [!NOTE]
> <span data-ttu-id="9ed71-261">Pašlaik ceļvežus nevar pievienot atsevišķām formulas rindām.</span><span class="sxs-lookup"><span data-stu-id="9ed71-261">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula-version"></a><span data-ttu-id="9ed71-262">Ceļveža pievienošana formulas versijai</span><span class="sxs-lookup"><span data-stu-id="9ed71-262">Add a Guide to a formula version</span></span>

<span data-ttu-id="9ed71-263">Lai ceļvedi pievienotu formulas versijai:</span><span class="sxs-lookup"><span data-stu-id="9ed71-263">To add a Guide to a formula version:</span></span>

1. <span data-ttu-id="9ed71-264">Dodieties uz **Ražošanas informācijas pārvaldība \> Materiālu komplekti un formulas \> Formulas**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-264">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="9ed71-265">Atveriet formulu, kas ietver versiju, kurai vēlaties piešķirt ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="9ed71-265">Open the formula that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="9ed71-266">Atveriet cilni **Galvene** virs augšējās kopsavilkuma cilnes.</span><span class="sxs-lookup"><span data-stu-id="9ed71-266">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="9ed71-267">Kopsavilkuma cilnē **Formulas versijas**, atlasiet versiju, kurai vēlaties piešķirt ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="9ed71-267">On the **Formula versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="9ed71-268">Rīkjoslā **Formulas versijas** atlasiet **Saistītie ceļveži**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-268">On the **Formula versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="9ed71-269">![Ar atlasīto formulas versiju saistīto ceļvežu atvēršana](media/instruction-guides-FormulaVersion.png "Ar atlasīto formulas versiju saistīto ceļvežu atvēršana")</span><span class="sxs-lookup"><span data-stu-id="9ed71-269">![Open the Guides associated with a selected formula version](media/instruction-guides-FormulaVersion.png "Open the Guides associated with a selected formula version")</span></span>
1. <span data-ttu-id="9ed71-270">Jūsu formulas versijai tiek atvērta lapa **Saistītie ceļveži**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-270">The **Associated Guides** page opens for your formula version.</span></span>
1. <span data-ttu-id="9ed71-271">Lai režģim pievienotu jaunu rindu, darbības rūtī atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-271">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="9ed71-272">Jaunajai rindai lietojiet nolaižamo sarakstu kolonnā **Nosaukums**, lai izvēlētos ceļvedi, ko vēlaties piešķirt.</span><span class="sxs-lookup"><span data-stu-id="9ed71-272">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="9ed71-273">![Ceļveža pievienošana formulas versijai](media/instruction-guides-FormulaVersionAddGuide.png "Ceļveža pievienošana formulas versijai")</span><span class="sxs-lookup"><span data-stu-id="9ed71-273">![Adding a Guide to a formula version](media/instruction-guides-FormulaVersionAddGuide.png "Adding a Guide to a formula version")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a><span data-ttu-id="9ed71-274">Saistiet ceļvedi ar materiālu komplektu</span><span class="sxs-lookup"><span data-stu-id="9ed71-274">Associate a Guide to a bill of materials</span></span>

<span data-ttu-id="9ed71-275">Varat pievienot ceļvedi jebkuram [materiālu komplektam](bill-of-material-bom.md) (MK).</span><span class="sxs-lookup"><span data-stu-id="9ed71-275">You can add a guide to any [bill of materials](bill-of-material-bom.md) (BOM).</span></span>

### <a name="typical-scenario-using-bills-of-materials"></a><span data-ttu-id="9ed71-276">Tipisks scenārijs, izmantojot materiālu komplektus</span><span class="sxs-lookup"><span data-stu-id="9ed71-276">Typical scenario using bills of materials</span></span>

<span data-ttu-id="9ed71-277">Ceļveži, kas pievienoti MK sniedz ražotnes darbiniekiem instrukcijas, kas paskaidro, kā sagatavot un apstrādāt materiālu no MK.</span><span class="sxs-lookup"><span data-stu-id="9ed71-277">Guides attached to a BOM provide shop floor workers with instructions that explain how to prepare and handle material from a BOM.</span></span> <span data-ttu-id="9ed71-278">Ceļvežus var piešķirt arī MK versijām.</span><span class="sxs-lookup"><span data-stu-id="9ed71-278">Guides can also be assigned to versions of a BOM.</span></span>

> [!NOTE]
> <span data-ttu-id="9ed71-279">Pašlaik ceļvežus nevar pievienot atsevišķām MK rindām.</span><span class="sxs-lookup"><span data-stu-id="9ed71-279">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials"></a><span data-ttu-id="9ed71-280">Ceļveža pievienošana materiālu komplektam</span><span class="sxs-lookup"><span data-stu-id="9ed71-280">Add a Guide to a bill of materials</span></span>

<span data-ttu-id="9ed71-281">Lai ceļvedi pievienotu materiālu komplektam:</span><span class="sxs-lookup"><span data-stu-id="9ed71-281">To add a Guide to a bill of material:</span></span>

1. <span data-ttu-id="9ed71-282">Dodieties uz **Ražošanas informācijas pārvaldība \> Materiālu komplekti un formulas \> Materiālu komplekti**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-282">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="9ed71-283">Atveriet materiālu komplektu, kuram vēlaties piešķirt ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="9ed71-283">Open the bill of materials that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="9ed71-284">Atveriet cilni **Galvene** virs augšējās kopsavilkuma cilnes.</span><span class="sxs-lookup"><span data-stu-id="9ed71-284">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="9ed71-285">Paplašiniet kopsavilkuma cilni **Saistītie ceļveži**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-285">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="9ed71-286">Atlasiet **Pievienot** rīkjoslā **Saistītie ceļveži**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-286">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="9ed71-287">Režģim tiek pievienota jauna rinda.</span><span class="sxs-lookup"><span data-stu-id="9ed71-287">A new line is added to the grid.</span></span>
1. <span data-ttu-id="9ed71-288">Jaunajai rindai lietojiet nolaižamo sarakstu kolonnā **Nosaukums**, lai izvēlētos ceļvedi, ko vēlaties piešķirt.</span><span class="sxs-lookup"><span data-stu-id="9ed71-288">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="9ed71-289">![Ceļveža pievienošana MK:](media/instruction-guides-BOM.png "Ceļveža pievienošana MK")</span><span class="sxs-lookup"><span data-stu-id="9ed71-289">![Adding a Guide to a BOM](media/instruction-guides-BOM.png "Adding a Guide to a BOM")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a><span data-ttu-id="9ed71-290">Saistiet ceļvedi ar materiālu komplekta versiju</span><span class="sxs-lookup"><span data-stu-id="9ed71-290">Associate a Guide to a bill of materials version</span></span>

<span data-ttu-id="9ed71-291">Varat pievienot ceļvedi jebkurai [materiālu komplekta versijai](bill-of-material-bom.md#bom-and-formula-versions).</span><span class="sxs-lookup"><span data-stu-id="9ed71-291">You can add a guide to any [bill of materials version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-bill-of-materials-versions"></a><span data-ttu-id="9ed71-292">Tipisks scenārijs, izmantojot materiālu komplekta versijas</span><span class="sxs-lookup"><span data-stu-id="9ed71-292">Typical scenario using bill of materials versions</span></span>

<span data-ttu-id="9ed71-293">Atsevišķai MK versijai piesaistītie ceļveži nodrošina ražotnes darbiniekus ar instrukcijām, kas paskaidro, kā sagatavot un apstrādāt materiālu MK versijai, kas atšķiras no vispārējā MK vai citām tā versijām.</span><span class="sxs-lookup"><span data-stu-id="9ed71-293">Guides attached to an individual BOM version provide shop floor workers with instructions that explain how to prepare and handle material for a version of a BOM that is different from the generic BOM or other versions of it.</span></span>

> [!NOTE]
> <span data-ttu-id="9ed71-294">Pašlaik ceļvežus nevar pievienot atsevišķām MK rindām.</span><span class="sxs-lookup"><span data-stu-id="9ed71-294">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials-version"></a><span data-ttu-id="9ed71-295">Ceļveža pievienošana materiālu komplekta versijai</span><span class="sxs-lookup"><span data-stu-id="9ed71-295">Add a Guide to a bill of materials version</span></span>

<span data-ttu-id="9ed71-296">Lai ceļvedi pievienotu materiālu komplekta versijai:</span><span class="sxs-lookup"><span data-stu-id="9ed71-296">To add a Guide to a bill of materials version:</span></span>

1. <span data-ttu-id="9ed71-297">Dodieties uz **Ražošanas informācijas pārvaldība \> Materiālu komplekti un formulas \> Materiālu komplekti**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-297">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="9ed71-298">Atveriet MK, kas ietver versiju, kurai vēlaties piešķirt ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="9ed71-298">Open the BOM that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="9ed71-299">Atveriet cilni **Galvene** virs augšējās kopsavilkuma cilnes.</span><span class="sxs-lookup"><span data-stu-id="9ed71-299">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="9ed71-300">Kopsavilkuma cilnē **MK versijas**, atlasiet versiju, kurai vēlaties piešķirt ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="9ed71-300">On the **BOM versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="9ed71-301">Rīkjoslā **MK versijas** atlasiet **Saistītie ceļveži**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-301">On the **BOM versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="9ed71-302">![Ar atlasīto MK versiju saistīto ceļvežu atvēršana](media/instruction-guides-BOMVersion.png "Ar atlasīto MK versiju saistīto ceļvežu atvēršana")</span><span class="sxs-lookup"><span data-stu-id="9ed71-302">![Open the Guides associated with a selected BOM version](media/instruction-guides-BOMVersion.png "Open the Guides associated with a selected BOM version")</span></span>
1. <span data-ttu-id="9ed71-303">Jūsu MK versijai tiek atvērta lapa **Saistītie ceļveži**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-303">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="9ed71-304">Lai režģim pievienotu jaunu rindu, darbības rūtī atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-304">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="9ed71-305">Jaunajai rindai lietojiet nolaižamo sarakstu kolonnā **Nosaukums**, lai izvēlētos ceļvedi, ko vēlaties piešķirt.</span><span class="sxs-lookup"><span data-stu-id="9ed71-305">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="9ed71-306">![Ceļveža pievienošana MK versijai](media/instruction-guides-BOMVersionAddGuide.png "Ceļveža pievienošana MK versijai")</span><span class="sxs-lookup"><span data-stu-id="9ed71-306">![Adding a Guide to a BOM version](media/instruction-guides-BOMVersionAddGuide.png "Adding a Guide to a BOM version")</span></span>

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a><span data-ttu-id="9ed71-307">Saistīt ceļvedi ar maršrutu</span><span class="sxs-lookup"><span data-stu-id="9ed71-307">Associate a Guide to a route</span></span>

<span data-ttu-id="9ed71-308">Varat pievienot ceļvedi jebkuram [maršrutam](routes-operations.md).</span><span class="sxs-lookup"><span data-stu-id="9ed71-308">You can add a guide to any [route](routes-operations.md).</span></span>

### <a name="typical-scenario-using-routes"></a><span data-ttu-id="9ed71-309">Tipisks scenārijs, izmantojot maršrutus</span><span class="sxs-lookup"><span data-stu-id="9ed71-309">Typical scenario using routes</span></span>

<span data-ttu-id="9ed71-310">Maršruti parasti tiek izmantoti, lai norādītu, kā noteikta izlaistā prece jāražo, pamatojoties uz MK vai MK versiju un ar resursu vai resursu grupu kopu.</span><span class="sxs-lookup"><span data-stu-id="9ed71-310">Routes are typically used to specify how a certain released product shall be produced based on a BOM or BOM version and with a set of resources or resource groups.</span></span>

<span data-ttu-id="9ed71-311">Piešķiriet ceļvedi maršrutam, lai nodrošinātu detalizētas instrukcijas attiecīgajam ražošanas procesam.</span><span class="sxs-lookup"><span data-stu-id="9ed71-311">Assign a Guide to a route to provide step-by-step instructions for the respective production process.</span></span>

### <a name="add-a-guide-to-a-route"></a><span data-ttu-id="9ed71-312">Ceļveža pievienošana maršrutam</span><span class="sxs-lookup"><span data-stu-id="9ed71-312">Add a Guide to a route</span></span>

<span data-ttu-id="9ed71-313">Lai ceļvedi pievienotu maršrutam:</span><span class="sxs-lookup"><span data-stu-id="9ed71-313">To add a Guide to a route:</span></span>

1. <span data-ttu-id="9ed71-314">Doties uz **Ražošanas kontrole \> Visi maršruti**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-314">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="9ed71-315">Atveriet maršrutu, kuram vēlaties piešķirt ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="9ed71-315">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="9ed71-316">Paplašiniet kopsavilkuma cilni **Saistītie ceļveži**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-316">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="9ed71-317">Atlasiet **Pievienot** rīkjoslā **Saistītie ceļveži**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-317">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="9ed71-318">Režģim tiek pievienota jauna rinda.</span><span class="sxs-lookup"><span data-stu-id="9ed71-318">A new line is added to the grid.</span></span>
1. <span data-ttu-id="9ed71-319">Jaunajai rindai lietojiet nolaižamo sarakstu kolonnā **Nosaukums**, lai izvēlētos ceļvedi, ko vēlaties piešķirt.</span><span class="sxs-lookup"><span data-stu-id="9ed71-319">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="9ed71-320">![Ceļveža pievienošana maršrutam](media/instruction-guides-Route.png "Ceļveža pievienošana maršrutam")</span><span class="sxs-lookup"><span data-stu-id="9ed71-320">![Adding a Guide to a route](media/instruction-guides-Route.png "Adding a Guide to a route")</span></span>

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a><span data-ttu-id="9ed71-321">Saistīt ceļvedi ar maršruta versiju</span><span class="sxs-lookup"><span data-stu-id="9ed71-321">Associate a Guide to a route version</span></span>

<span data-ttu-id="9ed71-322">Varat pievienot ceļvedi jebkurai [maršruta versijai](routes-operations.md#route-versions).</span><span class="sxs-lookup"><span data-stu-id="9ed71-322">You can add a guide to any [route version](routes-operations.md#route-versions).</span></span>

### <a name="typical-scenario-using-route-versions"></a><span data-ttu-id="9ed71-323">Tipisks scenārijs, izmantojot maršruta versijas</span><span class="sxs-lookup"><span data-stu-id="9ed71-323">Typical scenario using route versions</span></span>

<span data-ttu-id="9ed71-324">Maršrutu versijas parasti tiek izmantotas, lai noteiktu ražošanas procesu variantus, pamatojoties uz esošu maršrutu.</span><span class="sxs-lookup"><span data-stu-id="9ed71-324">Routes versions are typically used to specify variants of production processes based on an existing route.</span></span> <span data-ttu-id="9ed71-325">Katrai maršruta versijai varat piešķirt dažādus ceļvežus.</span><span class="sxs-lookup"><span data-stu-id="9ed71-325">You can assign different Guides to each route version.</span></span>

### <a name="add-a-guide-to-a-route-version"></a><span data-ttu-id="9ed71-326">Ceļveža pievienošana maršruta versijai</span><span class="sxs-lookup"><span data-stu-id="9ed71-326">Add a Guide to a route version</span></span>

<span data-ttu-id="9ed71-327">Lai pievienotu ceļvedi maršruta versijai:</span><span class="sxs-lookup"><span data-stu-id="9ed71-327">To add a Guide to a route version:</span></span>

1. <span data-ttu-id="9ed71-328">Doties uz **Ražošanas kontrole \> Visi maršruti**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-328">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="9ed71-329">Atveriet maršrutu, kuram vēlaties piešķirt ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="9ed71-329">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="9ed71-330">Kopsavilkuma cilnē **Versijas** atlasiet versiju, kurai vēlaties piešķirt ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="9ed71-330">On the **Versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="9ed71-331">Rīkjoslā **Versijas** atlasiet **Saistītie ceļveži**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-331">On the **Versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="9ed71-332">![Ar atlasīto maršruta versiju saistīto ceļvežu atvēršana](media/instruction-guides-RouteVersion.png "Ar atlasīto maršruta versiju saistīto ceļvežu atvēršana")</span><span class="sxs-lookup"><span data-stu-id="9ed71-332">![Open the Guides associated with a selected route version](media/instruction-guides-RouteVersion.png "Open the Guides associated with a selected route version")</span></span>
1. <span data-ttu-id="9ed71-333">Jūsu MK versijai tiek atvērta lapa **Saistītie ceļveži**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-333">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="9ed71-334">Lai režģim pievienotu jaunu rindu, darbības rūtī atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-334">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="9ed71-335">Jaunajai rindai lietojiet nolaižamo sarakstu kolonnā **Nosaukums**, lai izvēlētos ceļvedi, ko vēlaties piešķirt.</span><span class="sxs-lookup"><span data-stu-id="9ed71-335">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="9ed71-336">![Ceļveža pievienošana maršruta versijai](media/instruction-guides-RouteVersionAddGuide.png "Ceļveža pievienošana maršruta versijai")</span><span class="sxs-lookup"><span data-stu-id="9ed71-336">![Adding a Guide to a route version](media/instruction-guides-RouteVersionAddGuide.png "Adding a Guide to a route version")</span></span>

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a><span data-ttu-id="9ed71-337">Saistīt ceļvedi ar maršruta operācijas saiti</span><span class="sxs-lookup"><span data-stu-id="9ed71-337">Associate a Guide to a route operation relation</span></span>

<span data-ttu-id="9ed71-338">Varat pievienot ceļvedi jebkurai [maršruta operācijas saitei](routes-operations.md#operation-relations).</span><span class="sxs-lookup"><span data-stu-id="9ed71-338">You can add a guide to any [route operation relation](routes-operations.md#operation-relations).</span></span>

### <a name="typical-scenario-using-route-operation-relations"></a><span data-ttu-id="9ed71-339">Tipisks scenārijs, izmantojot maršruta operāciju saites</span><span class="sxs-lookup"><span data-stu-id="9ed71-339">Typical scenario using route operation relations</span></span>

<span data-ttu-id="9ed71-340">Operāciju saites ir vispiemērotākais veids, kā pievienot norādījumus preces procesam un ar to saistītajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="9ed71-340">Operation relations are the most specific way to add guidance to a product process and its related operations.</span></span> <span data-ttu-id="9ed71-341">Varat atzīmēt norādījumus katrai operācijai maršrutā un atzīmēt dažādus norādījumus jebkāda veida relāciju kontekstam, kas noteikts maršrutam, piemēram, noteiktiem krājumiem, konfigurācijām un daudz kam citam.</span><span class="sxs-lookup"><span data-stu-id="9ed71-341">You can specify guidance for each operation in a route and specify different guidance for any type of relation context specified for a route, such as for specific items, configurations, and more.</span></span> <span data-ttu-id="9ed71-342">Var arī norādīt, uz kuriem operācijas posmiem norādījumi attiecas (piemēram, iestatīšanu, rindošanu, procesu vai transportu).</span><span class="sxs-lookup"><span data-stu-id="9ed71-342">You can also specify to which stages in the operation the guidance applies (such as setup, queueing, process, or transport).</span></span>

> [!NOTE]
> <span data-ttu-id="9ed71-343">Ja jūs norādāt ceļvežus vairākām maršruta operāciju saitēm, no šiem ceļvežiem ražotnē ģenerētajam darbam tiks parādīts tikai ceļvedis, kas saistīts ar viskonkrētāko saiti.</span><span class="sxs-lookup"><span data-stu-id="9ed71-343">If you specify guides for several operation relations of a route, among those guides, only the guide from the most specific relation will be show on the shop floor for the generated job.</span></span>

### <a name="add-a-guide-to-a-route-operation-relation"></a><span data-ttu-id="9ed71-344">Ceļveža pievienošana maršruta operācijas saitei</span><span class="sxs-lookup"><span data-stu-id="9ed71-344">Add a Guide to a route operation relation</span></span>

<span data-ttu-id="9ed71-345">Lai pievienotu ceļvedi maršruta operācijas saitei:</span><span class="sxs-lookup"><span data-stu-id="9ed71-345">To add a Guide to a route operation relation:</span></span>

1. <span data-ttu-id="9ed71-346">Doties uz **Ražošanas kontrole \> Visi maršruti**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-346">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="9ed71-347">Atveriet maršrutu, kuram vēlaties piešķirt ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="9ed71-347">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="9ed71-348">Darbības rūtī atveriet cilni **Maršruts** un grupā **Uzturēt** atlasiet **Maršruta informācija**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-348">On the Action Pane, open the **Route** tab and from the **Maintain** group, select **Route details**.</span></span>
1. <span data-ttu-id="9ed71-349">Atlasītajam maršrutam tiek atvērta lapa **Maršruta informācija**.</span><span class="sxs-lookup"><span data-stu-id="9ed71-349">The **Route details** page opens for your selected rout.</span></span>
1. <span data-ttu-id="9ed71-350">Augšējā režģī atlasiet operāciju, kurai vēlaties sniegt norādījumus.</span><span class="sxs-lookup"><span data-stu-id="9ed71-350">In the top grid, select the operation you want to provide guidance for.</span></span>
1. <span data-ttu-id="9ed71-351">Apakšējā režģī atlasiet specifisku saiti (vai vispārējo saiti **Viss**).</span><span class="sxs-lookup"><span data-stu-id="9ed71-351">In the bottom grid, select a specific relation (or the generic **All** relation).</span></span>
    <span data-ttu-id="9ed71-352">![Atlasiet operāciju un pēc tam saiti](media/instruction-guides-RouteOperationRelation.png "Atlasiet operāciju un pēc tam saiti")</span><span class="sxs-lookup"><span data-stu-id="9ed71-352">![Select an operation and then a relation](media/instruction-guides-RouteOperationRelation.png "Select an operation and then a relation")</span></span>
1. <span data-ttu-id="9ed71-353">Virs apakšējā režģa atveriet cilni **Saistītie ceļveži**.  ![Cilne Saistītie ceļveži](media/instruction-guides-RouteOperationRelation-AddGuide.png "Cilne Saistītie ceļveži")</span><span class="sxs-lookup"><span data-stu-id="9ed71-353">Above the bottom gird, open the **Associated Guides** tab.  ![The Associated Guides tab](media/instruction-guides-RouteOperationRelation-AddGuide.png "The Associated Guides tab")</span></span>
1. <span data-ttu-id="9ed71-354">Atlasiet **Pievienot** rīkjoslā, kas atrodas apakšējā režģa augšdaļā, lai režģim pievienotu jaunu rindu.</span><span class="sxs-lookup"><span data-stu-id="9ed71-354">Select **Add** from the toolbar at the top of the bottom grid to add a new line to the grid.</span></span>
1. <span data-ttu-id="9ed71-355">Jaunajai rindai lietojiet nolaižamo sarakstu kolonnā **Nosaukums**, lai izvēlētos ceļvedi, ko jūs vēlaties piešķirt.</span><span class="sxs-lookup"><span data-stu-id="9ed71-355">For the new row, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="9ed71-356">Pārējā rindā atzīmējiet izvēles rūtiņu katram kontekstam, kurā atlasītajam ceļvedim jābūt pieejamam.</span><span class="sxs-lookup"><span data-stu-id="9ed71-356">In the rest of the row, select the check box for each context where the selected Guide should be available.</span></span>

> [!NOTE]
> <span data-ttu-id="9ed71-357">Katram operācijas posmam var pievienot vienu vai vairākus ceļvežus.</span><span class="sxs-lookup"><span data-stu-id="9ed71-357">You can add one or more guides for each stage of each operation.</span></span>

## <a name="select-guides-from-the-shop-floor-execution-interface"></a><span data-ttu-id="9ed71-358">Atlasiet ceļvežus no ražotnes izpildes interfeisa</span><span class="sxs-lookup"><span data-stu-id="9ed71-358">Select guides from the shop floor execution interface</span></span>

<span data-ttu-id="9ed71-359">Kad nodarbinātais atver darbu sarakstu ražotnes izpildes interfeisā, Supply Chain Management atrod atbilstošos ceļvežus parādītajiem darbiem.</span><span class="sxs-lookup"><span data-stu-id="9ed71-359">When a worker opens a job list on the shop floor execution interface, Supply Chain Management finds the relevant guides for the jobs shown.</span></span> <span data-ttu-id="9ed71-360">Izmantojiet pogu **Ceļveži**, lai skatītu atbilstošos ceļvežus.</span><span class="sxs-lookup"><span data-stu-id="9ed71-360">Use the **Guides** button to view the relevant guides.</span></span>

<span data-ttu-id="9ed71-361">![Ceļvežu poga ražotnes izpildes interfeisā](media/instruction-guides-Shopfloor1.png "Ceļvežu poga ražotnes izpildes interfeisā")</span><span class="sxs-lookup"><span data-stu-id="9ed71-361">![Guides button in the shop floor execution interface](media/instruction-guides-Shopfloor1.png "Guides button in the shop floor execution interface")</span></span>

<span data-ttu-id="9ed71-362">Pēc tam uzvelciet HoloLens un piekļūstiet attiecīgajam ceļvedim, paskatoties uz QR kodu un aktivizējot atbilstošo ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="9ed71-362">Then put on a HoloLens and access the respective guide by glancing at the QR code and activating the respective Guide.</span></span>

<span data-ttu-id="9ed71-363">![QR kods, lai piekļūtu ceļvežiem, izmantojot HoloLens](media/instruction-guides-Shopfloor2.png "QR kods, lai piekļūtu ceļvežiem, izmantojot HoloLens")</span><span class="sxs-lookup"><span data-stu-id="9ed71-363">![QR code to access guides using a HoloLens](media/instruction-guides-Shopfloor2.png "QR code to access guides using a HoloLens")</span></span>

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a><span data-ttu-id="9ed71-364">Ceļvežu atlases loģikas risināšana</span><span class="sxs-lookup"><span data-stu-id="9ed71-364">Resolving the logic for selecting Guides</span></span>

<span data-ttu-id="9ed71-365">Varat pievienot ceļvežus šādiem ražošanas datiem:</span><span class="sxs-lookup"><span data-stu-id="9ed71-365">You can add Guides to the following production data:</span></span>

- [<span data-ttu-id="9ed71-366">Resursi</span><span class="sxs-lookup"><span data-stu-id="9ed71-366">Resources</span></span>](#resources)
- [<span data-ttu-id="9ed71-367">Resursu grupas</span><span class="sxs-lookup"><span data-stu-id="9ed71-367">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="9ed71-368">Izlaistās preces</span><span class="sxs-lookup"><span data-stu-id="9ed71-368">Released products</span></span>](#released-products)
- [<span data-ttu-id="9ed71-369">Formulas</span><span class="sxs-lookup"><span data-stu-id="9ed71-369">Formulas</span></span>](#formulas)
- [<span data-ttu-id="9ed71-370">Formulas versijas</span><span class="sxs-lookup"><span data-stu-id="9ed71-370">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="9ed71-371">Materiālu komplekti (MK)</span><span class="sxs-lookup"><span data-stu-id="9ed71-371">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="9ed71-372">MK versijas</span><span class="sxs-lookup"><span data-stu-id="9ed71-372">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="9ed71-373">Maršruti</span><span class="sxs-lookup"><span data-stu-id="9ed71-373">Routes</span></span>](#routes)
- [<span data-ttu-id="9ed71-374">Maršruta versijas</span><span class="sxs-lookup"><span data-stu-id="9ed71-374">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="9ed71-375">Maršruta operāciju relācijas</span><span class="sxs-lookup"><span data-stu-id="9ed71-375">Route operation relations</span></span>](#route-operation-relations)

<span data-ttu-id="9ed71-376">Kad Supply Chain Management ģenerē darbus ražotnei, tas apkopos atbilstošos ceļvežus no šiem avotiem.</span><span class="sxs-lookup"><span data-stu-id="9ed71-376">When Supply Chain Management generates the jobs for the production floor, it will collect the relevant Guides from those sources.</span></span> <span data-ttu-id="9ed71-377">Ņemiet vērā šos svarīgos noteikumus.</span><span class="sxs-lookup"><span data-stu-id="9ed71-377">Take note of the following important rules.</span></span>

- <span data-ttu-id="9ed71-378">Ja maršrutam vai ražošanas pasūtījumam tiek pievienota MK versija vai formulas versija, darbam tiks rādītas visi šai versijai piesaistītie ceļveži, kā arī ceļveži, kas piesaistīti pamata MK vai tā versijas formulai.</span><span class="sxs-lookup"><span data-stu-id="9ed71-378">If you attach a BOM version or formula version to a route or production order, then any Guides attached to this version, and also the Guides attached to the parent BOM or formula of that version, will be shown on the job.</span></span>
- <span data-ttu-id="9ed71-379">Ja ražošanas pasūtījumam tiek pievienota maršruta versija, darbam tiks rādīti visi šai versijai piesaistītie ceļveži, kā arī ceļveži, kas piesaistīti šīs versijas pamata maršrutam.</span><span class="sxs-lookup"><span data-stu-id="9ed71-379">If you attach a route version to a production order, then any Guides attached to this version, and also the Guides attached to the parent route of that version, will be shown on the job.</span></span>
- <span data-ttu-id="9ed71-380">Ja definējat vairākas maršruta operāciju saites, kas ietver *Visas* saites un piešķir tām ceļvežus, darbam tiks parādīts tikai ceļveži, kas saistīti ar viskonkrētāko saiti.</span><span class="sxs-lookup"><span data-stu-id="9ed71-380">If you define several route operation relations that include the *All* relation and assign Guides to those, only the Guides from the most specific relation will be shown for the job.</span></span>  

<span data-ttu-id="9ed71-381">![Shēma, kā atrisināt atbilstošos ceļvežus](media/instruction-guides-Resolve.png "Shēma, kā atrisināt atbilstošos ceļvežus")</span><span class="sxs-lookup"><span data-stu-id="9ed71-381">![Diagram on resolving the relevant Guides](media/instruction-guides-Resolve.png "Diagram on resolving the relevant Guides")</span></span>
