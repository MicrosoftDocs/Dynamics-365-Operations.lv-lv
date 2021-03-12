---
title: Organizācijas hierarhija Dataverse
description: Šajā tēmā ir aprakstīta organizācijas datu integrācija starp programmām Finance and Operations un Dataverse
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 5132fd85fdf2c08ccded9db590328c394a2f984e
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744697"
---
# <a name="organization-hierarchy-in-dataverse"></a><span data-ttu-id="a42e1-103">Organizācijas hierarhija Dataverse</span><span class="sxs-lookup"><span data-stu-id="a42e1-103">Organization hierarchy in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a42e1-104">Tā kā Dynamics 365 Finance ir finanšu sistēma *organizācija* ir pamatkoncepts un sistēmas iestatīšana sākas ar organizācijas hierarhijas konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="a42e1-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="a42e1-105">Pēc tam biznesa finanses var izsekot organizācijas līmenī, kā arī jebkurā līmenī organizācijas hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="a42e1-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="a42e1-106">Lai gan Dataverse nav organizācijas hierarhijas koncepta, tai ir daži brīvāki koncepti, piemēram, kopējie pārdošanas ieņēmumi.</span><span class="sxs-lookup"><span data-stu-id="a42e1-106">Although Dataverse doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="a42e1-107">Kā daļa no Dataverse integrācijas organizācijas hierarhijas datu struktūra tiek pievienota Dataverse.</span><span class="sxs-lookup"><span data-stu-id="a42e1-107">As part of Dataverse integration, the organization hierarchy data structure is added to Dataverse.</span></span>

## <a name="data-flow"></a><span data-ttu-id="a42e1-108">Datu plūsmas</span><span class="sxs-lookup"><span data-stu-id="a42e1-108">Data flow</span></span>

<span data-ttu-id="a42e1-109">Biznesa ekosistēmai, kas sastāv no programmām Finance and Operations un Dataverse arī turpmāk būs organizācijas hierarhija.</span><span class="sxs-lookup"><span data-stu-id="a42e1-109">A business ecosystem that consists of Finance and Operations apps and Dataverse will continue to have an organization hierarchy.</span></span> <span data-ttu-id="a42e1-110">Šī organizācijas hierarhija ir veidota, pamatojoties uz Finance and Operations programmām, bet tā ir pakļauta Dataverse informatīviem un paplašināmības mērķiem.</span><span class="sxs-lookup"><span data-stu-id="a42e1-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Dataverse for informational and extensibility purposes.</span></span> <span data-ttu-id="a42e1-111">Nākamajā attēlā ir parādīta organizācijas hierarhijas informācija, kas ir atklāta Dataverse kā vienvirziena datu plūsma no Finance and Operations programmām uz Dataverse.</span><span class="sxs-lookup"><span data-stu-id="a42e1-111">The following illustration shows the organization hierarchy information that is exposed in Dataverse as a one-way data flow from Finance and Operations apps to Dataverse.</span></span>

![Arhitektūras attēls](media/dual-write-data-flow.png)

<span data-ttu-id="a42e1-113">Organizācijas hierarhijas tabulu kartes ir pieejamas datu vienvirziena sinhronizācijai no programmas Finance and Operations programmām uz Dataverse.</span><span class="sxs-lookup"><span data-stu-id="a42e1-113">Organization hierarchy table maps are available for one-way synchronization of data from Finance and Operations apps to Dataverse.</span></span>

## <a name="templates"></a><span data-ttu-id="a42e1-114">Veidnes</span><span class="sxs-lookup"><span data-stu-id="a42e1-114">Templates</span></span>

<span data-ttu-id="a42e1-115">Preces informācijā ir ietverts viss nepieciešamais, kas saistīts ar preci un tās definīciju, piemēram, preces dimensijas vai izsekošana un noliktavas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="a42e1-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="a42e1-116">Kā redzams šajā tabulā, tiek izveidota tabulas karšu kolekcija, lai sinhronizētu preces un saistīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="a42e1-116">As the following table shows, a collection of table maps is created to sync products and related information.</span></span>

<span data-ttu-id="a42e1-117">Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="a42e1-117">Finance and Operations apps</span></span> | <span data-ttu-id="a42e1-118">Citas Dynamics 365 programmas</span><span class="sxs-lookup"><span data-stu-id="a42e1-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="a42e1-119">apraksts</span><span class="sxs-lookup"><span data-stu-id="a42e1-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="a42e1-120">Organizācijas hierarhijas nolūki</span><span class="sxs-lookup"><span data-stu-id="a42e1-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="a42e1-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="a42e1-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="a42e1-122">Šī veidne nodrošina organizācijas hierarhijas mērķa tabulas vienvirziena sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="a42e1-122">This template provides one-way synchronization of the Organization Hierarchy Purpose table.</span></span>
<span data-ttu-id="a42e1-123">Organizācijas hierarhijas tips</span><span class="sxs-lookup"><span data-stu-id="a42e1-123">Organization hierarchy type</span></span> | <span data-ttu-id="a42e1-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="a42e1-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="a42e1-125">Šī veidne nodrošina organizācijas hierarhijas veida tabulas vienvirziena sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="a42e1-125">This template provides one-way synchronization of the Organization Hierarchy Type table.</span></span>
<span data-ttu-id="a42e1-126">Organizācijas hierarhija — publicēta</span><span class="sxs-lookup"><span data-stu-id="a42e1-126">Organization hierarchy - published</span></span> | <span data-ttu-id="a42e1-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="a42e1-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="a42e1-128">Šī veidne nodrošina organizācijas hierarhijas publicētās tabulas vienvirziena sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="a42e1-128">This template provides one-way synchronization of the Organization Hierarchy Published table.</span></span>
<span data-ttu-id="a42e1-129">Pārvaldības struktūrvienība</span><span class="sxs-lookup"><span data-stu-id="a42e1-129">Operating unit</span></span> | <span data-ttu-id="a42e1-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="a42e1-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="a42e1-131">Juridiskas personas</span><span class="sxs-lookup"><span data-stu-id="a42e1-131">Legal entities</span></span> | <span data-ttu-id="a42e1-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="a42e1-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="a42e1-133">Juridiskas personas</span><span class="sxs-lookup"><span data-stu-id="a42e1-133">Legal entities</span></span> | <span data-ttu-id="a42e1-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="a42e1-134">cdm_companies</span></span> | <span data-ttu-id="a42e1-135">Nodrošina juridiskas personas (uzņēmuma) informācijas divvirzienu sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="a42e1-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="a42e1-136">Iekšējā organizācija</span><span class="sxs-lookup"><span data-stu-id="a42e1-136">Internal Organization</span></span>

<span data-ttu-id="a42e1-137">Iekšējās organizācijas informācija Dataverse tiek iegūta no divām tabulām — **pārvaldības struktūrvienība** un **juridiska persona**.</span><span class="sxs-lookup"><span data-stu-id="a42e1-137">Internal organization information in Dataverse comes from two tables, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
