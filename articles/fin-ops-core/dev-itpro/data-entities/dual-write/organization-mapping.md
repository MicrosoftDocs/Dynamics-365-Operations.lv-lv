---
title: Organizācijas hierarhija Common Data Service
description: Šajā tēmā ir aprakstīta organizācijas datu integrācija starp programmām Finance and Operations un Common Data Service
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: fbf7cc33d12fb54d2ff02acc46ba2e284b2a2b3f
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019898"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="7f553-103">Organizācijas hierarhija Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7f553-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="7f553-104">Tā kā Dynamics 365 Finance ir finanšu sistēma *organizācija* ir pamatkoncepts un sistēmas iestatīšana sākas ar organizācijas hierarhijas konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="7f553-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="7f553-105">Pēc tam biznesa finanses var izsekot organizācijas līmenī, kā arī jebkurā līmenī organizācijas hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="7f553-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="7f553-106">Lai gan Common Data Service nav organizācijas hierarhijas koncepta, tai ir daži brīvāki koncepti, piemēram, kopējie pārdošanas ieņēmumi.</span><span class="sxs-lookup"><span data-stu-id="7f553-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="7f553-107">Kā daļa no Common Data Service integrācijas organizācijas hierarhijas datu struktūra tiek pievienota Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="7f553-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="7f553-108">Datu plūsmas</span><span class="sxs-lookup"><span data-stu-id="7f553-108">Data flow</span></span>

<span data-ttu-id="7f553-109">Biznesa ekosistēmai, kas sastāv no programmām Finance and Operations un Common Data Service arī turpmāk būs organizācijas hierarhija.</span><span class="sxs-lookup"><span data-stu-id="7f553-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="7f553-110">Šī organizācijas hierarhija ir veidota, pamatojoties uz Finance and Operations programmām, bet tā ir pakļauta Common Data Service informatīviem un paplašināmības mērķiem.</span><span class="sxs-lookup"><span data-stu-id="7f553-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="7f553-111">Nākamajā attēlā ir parādīta organizācijas hierarhijas informācija, kas ir atklāta Common Data Service kā vienvirziena datu plūsma no Finance and Operations programmām uz Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="7f553-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Arhitektūras attēls](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="7f553-113">Veidnes</span><span class="sxs-lookup"><span data-stu-id="7f553-113">Templates</span></span>

<span data-ttu-id="7f553-114">Organizācijas hierarhijas elementu kartes ir pieejamas datu vienvirziena sinhronizācijai no programmas Finance and Operations programmām uz Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="7f553-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="7f553-115">Veidnes</span><span class="sxs-lookup"><span data-stu-id="7f553-115">Templates</span></span>

<span data-ttu-id="7f553-116">Preces informācijā ir ietverts viss nepieciešamais, kas saistīts ar preci un tās definīciju, piemēram, preces dimensijas vai izsekošana un noliktavas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="7f553-116">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="7f553-117">Kā redzams šajā tabulā, tiek izveidota elementa karšu kolekcija, lai sinhronizētu preces un saistīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="7f553-117">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="7f553-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7f553-118">Finance and Operations</span></span> | <span data-ttu-id="7f553-119">Citas Dynamics 365 programmas</span><span class="sxs-lookup"><span data-stu-id="7f553-119">Other Dynamics 365 apps</span></span> | <span data-ttu-id="7f553-120">Apraksts</span><span class="sxs-lookup"><span data-stu-id="7f553-120">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="7f553-121">Organizācijas hierarhijas nolūki</span><span class="sxs-lookup"><span data-stu-id="7f553-121">Organization hierarchy purposes</span></span> | <span data-ttu-id="7f553-122">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="7f553-122">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="7f553-123">Šī veidne nodrošina organizācijas hierarhijas mērķa elementa vienvirziena sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="7f553-123">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="7f553-124">Organizācijas hierarhijas tips</span><span class="sxs-lookup"><span data-stu-id="7f553-124">Organization hierarchy type</span></span> | <span data-ttu-id="7f553-125">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="7f553-125">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="7f553-126">Šī veidne nodrošina organizācijas hierarhijas veida elementa vienvirziena sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="7f553-126">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="7f553-127">Organizācijas hierarhija — publicētā</span><span class="sxs-lookup"><span data-stu-id="7f553-127">Organization hierarchy - published</span></span> | <span data-ttu-id="7f553-128">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="7f553-128">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="7f553-129">Šī veidne nodrošina organizācijas hierarhijas publicētā elementa vienvirziena sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="7f553-129">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="7f553-130">Pārvaldības struktūrvienība</span><span class="sxs-lookup"><span data-stu-id="7f553-130">Operating unit</span></span> | <span data-ttu-id="7f553-131">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="7f553-131">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="7f553-132">Juridiskas personas</span><span class="sxs-lookup"><span data-stu-id="7f553-132">Legal entities</span></span> | <span data-ttu-id="7f553-133">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="7f553-133">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="7f553-134">Juridiskas personas</span><span class="sxs-lookup"><span data-stu-id="7f553-134">Legal entities</span></span> | <span data-ttu-id="7f553-135">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="7f553-135">cdm_companies</span></span> | <span data-ttu-id="7f553-136">Nodrošina juridiskas personas (uzņēmuma) informācijas divvirzienu sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="7f553-136">Provides bidirectional synchronization of legal entity (company) information.</span></span>


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="7f553-137">Iekšējā organizācija</span><span class="sxs-lookup"><span data-stu-id="7f553-137">Internal Organization</span></span>

<span data-ttu-id="7f553-138">Iekšējās organizācijas informācija Common Data Service tiek iegūta no diviem — **pārvaldības struktūrvienība** un **juridiska persona**.</span><span class="sxs-lookup"><span data-stu-id="7f553-138">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
