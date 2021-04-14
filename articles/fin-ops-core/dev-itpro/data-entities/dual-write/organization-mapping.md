---
title: Organizācijas hierarhija Dataverse
description: Šajā tēmā ir aprakstīta organizācijas datu integrācija starp programmām Finance and Operations un Dataverse
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8b147c27b9309b1b3597f1194c415fbb2e2b7ad2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750816"
---
# <a name="organization-hierarchy-in-dataverse"></a><span data-ttu-id="92b2e-103">Organizācijas hierarhija Dataverse</span><span class="sxs-lookup"><span data-stu-id="92b2e-103">Organization hierarchy in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="92b2e-104">Tā kā Dynamics 365 Finance ir finanšu sistēma *organizācija* ir pamatkoncepts un sistēmas iestatīšana sākas ar organizācijas hierarhijas konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="92b2e-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="92b2e-105">Pēc tam biznesa finanses var izsekot organizācijas līmenī, kā arī jebkurā līmenī organizācijas hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="92b2e-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="92b2e-106">Lai gan Dataverse nav organizācijas hierarhijas koncepta, tai ir daži brīvāki koncepti, piemēram, kopējie pārdošanas ieņēmumi.</span><span class="sxs-lookup"><span data-stu-id="92b2e-106">Although Dataverse doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="92b2e-107">Kā daļa no Dataverse integrācijas organizācijas hierarhijas datu struktūra tiek pievienota Dataverse.</span><span class="sxs-lookup"><span data-stu-id="92b2e-107">As part of Dataverse integration, the organization hierarchy data structure is added to Dataverse.</span></span>

## <a name="data-flow"></a><span data-ttu-id="92b2e-108">Datu plūsmas</span><span class="sxs-lookup"><span data-stu-id="92b2e-108">Data flow</span></span>

<span data-ttu-id="92b2e-109">Biznesa ekosistēmai, kas sastāv no programmām Finance and Operations un Dataverse arī turpmāk būs organizācijas hierarhija.</span><span class="sxs-lookup"><span data-stu-id="92b2e-109">A business ecosystem that consists of Finance and Operations apps and Dataverse will continue to have an organization hierarchy.</span></span> <span data-ttu-id="92b2e-110">Šī organizācijas hierarhija ir veidota, pamatojoties uz Finance and Operations programmām, bet tā ir pakļauta Dataverse informatīviem un paplašināmības mērķiem.</span><span class="sxs-lookup"><span data-stu-id="92b2e-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Dataverse for informational and extensibility purposes.</span></span> <span data-ttu-id="92b2e-111">Nākamajā attēlā ir parādīta organizācijas hierarhijas informācija, kas ir atklāta Dataverse kā vienvirziena datu plūsma no Finance and Operations programmām uz Dataverse.</span><span class="sxs-lookup"><span data-stu-id="92b2e-111">The following illustration shows the organization hierarchy information that is exposed in Dataverse as a one-way data flow from Finance and Operations apps to Dataverse.</span></span>

![Arhitektūras attēls](media/dual-write-data-flow.png)

<span data-ttu-id="92b2e-113">Organizācijas hierarhijas tabulu kartes ir pieejamas datu vienvirziena sinhronizācijai no programmas Finance and Operations programmām uz Dataverse.</span><span class="sxs-lookup"><span data-stu-id="92b2e-113">Organization hierarchy table maps are available for one-way synchronization of data from Finance and Operations apps to Dataverse.</span></span>

## <a name="templates"></a><span data-ttu-id="92b2e-114">Veidnes</span><span class="sxs-lookup"><span data-stu-id="92b2e-114">Templates</span></span>

<span data-ttu-id="92b2e-115">Preces informācijā ir ietverts viss nepieciešamais, kas saistīts ar preci un tās definīciju, piemēram, preces dimensijas vai izsekošana un noliktavas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="92b2e-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="92b2e-116">Kā redzams šajā tabulā, tiek izveidota tabulas karšu kolekcija, lai sinhronizētu preces un saistīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="92b2e-116">As the following table shows, a collection of table maps is created to sync products and related information.</span></span>

<span data-ttu-id="92b2e-117">Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="92b2e-117">Finance and Operations apps</span></span> | <span data-ttu-id="92b2e-118">Citas Dynamics 365 programmas</span><span class="sxs-lookup"><span data-stu-id="92b2e-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="92b2e-119">apraksts</span><span class="sxs-lookup"><span data-stu-id="92b2e-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="92b2e-120">Organizācijas hierarhijas nolūki</span><span class="sxs-lookup"><span data-stu-id="92b2e-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="92b2e-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="92b2e-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="92b2e-122">Šī veidne nodrošina organizācijas hierarhijas mērķa tabulas vienvirziena sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="92b2e-122">This template provides one-way synchronization of the Organization Hierarchy Purpose table.</span></span>
<span data-ttu-id="92b2e-123">Organizācijas hierarhijas tips</span><span class="sxs-lookup"><span data-stu-id="92b2e-123">Organization hierarchy type</span></span> | <span data-ttu-id="92b2e-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="92b2e-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="92b2e-125">Šī veidne nodrošina organizācijas hierarhijas veida tabulas vienvirziena sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="92b2e-125">This template provides one-way synchronization of the Organization Hierarchy Type table.</span></span>
<span data-ttu-id="92b2e-126">Organizācijas hierarhija — publicēta</span><span class="sxs-lookup"><span data-stu-id="92b2e-126">Organization hierarchy - published</span></span> | <span data-ttu-id="92b2e-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="92b2e-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="92b2e-128">Šī veidne nodrošina organizācijas hierarhijas publicētās tabulas vienvirziena sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="92b2e-128">This template provides one-way synchronization of the Organization Hierarchy Published table.</span></span>
<span data-ttu-id="92b2e-129">Pārvaldības struktūrvienība</span><span class="sxs-lookup"><span data-stu-id="92b2e-129">Operating unit</span></span> | <span data-ttu-id="92b2e-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="92b2e-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="92b2e-131">Juridiskas personas</span><span class="sxs-lookup"><span data-stu-id="92b2e-131">Legal entities</span></span> | <span data-ttu-id="92b2e-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="92b2e-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="92b2e-133">Juridiskas personas</span><span class="sxs-lookup"><span data-stu-id="92b2e-133">Legal entities</span></span> | <span data-ttu-id="92b2e-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="92b2e-134">cdm_companies</span></span> | <span data-ttu-id="92b2e-135">Nodrošina juridiskas personas (uzņēmuma) informācijas divvirzienu sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="92b2e-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="92b2e-136">Iekšējā organizācija</span><span class="sxs-lookup"><span data-stu-id="92b2e-136">Internal Organization</span></span>

<span data-ttu-id="92b2e-137">Iekšējās organizācijas informācija Dataverse tiek iegūta no divām tabulām — **pārvaldības struktūrvienība** un **juridiska persona**.</span><span class="sxs-lookup"><span data-stu-id="92b2e-137">Internal organization information in Dataverse comes from two tables, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]