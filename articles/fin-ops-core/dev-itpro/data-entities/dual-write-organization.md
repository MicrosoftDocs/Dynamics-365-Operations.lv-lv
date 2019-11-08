---
title: Organizācijas hierarhija Common Data Service
description: Šajā tēmā ir aprakstīta organizācijas datu integrācija starp programmām Finance and Operations un Common Data Service.
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
ms.openlocfilehash: 9a12ab249129dce24cdca5e29d737fa9f68c0eac
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572453"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="659d0-103">Organizācijas hierarhija Common Data Service</span><span class="sxs-lookup"><span data-stu-id="659d0-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="659d0-104">Tā kā Dynamics 365 Finance ir finanšu sistēma *organizācija* ir pamatkoncepts un sistēmas iestatīšana sākas ar organizācijas hierarhijas konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="659d0-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="659d0-105">Pēc tam biznesa finanses var izsekot organizācijas līmenī, kā arī jebkurā līmenī organizācijas hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="659d0-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="659d0-106">Lai gan Common Data Service nav organizācijas hierarhijas koncepta, tai ir daži brīvāki koncepti, piemēram, kopējie pārdošanas ieņēmumi.</span><span class="sxs-lookup"><span data-stu-id="659d0-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="659d0-107">Kā daļa no Common Data Service integrācijas organizācijas hierarhijas datu struktūra tiek pievienota Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="659d0-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="659d0-108">Datu plūsmas</span><span class="sxs-lookup"><span data-stu-id="659d0-108">Data flow</span></span>

<span data-ttu-id="659d0-109">Biznesa ekosistēmai, kas sastāv no programmām Finance and Operations un Common Data Service arī turpmāk būs organizācijas hierarhija.</span><span class="sxs-lookup"><span data-stu-id="659d0-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="659d0-110">Šī organizācijas hierarhija ir veidota, pamatojoties uz Finance and Operations programmām, bet tā ir pakļauta Common Data Service informatīviem un paplašināmības mērķiem.</span><span class="sxs-lookup"><span data-stu-id="659d0-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="659d0-111">Nākamajā attēlā ir parādīta organizācijas hierarhijas informācija, kas ir atklāta Common Data Service kā vienvirziena datu plūsma no Finance and Operations programmām uz Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="659d0-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Arhitektūras attēls](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="659d0-113">Veidnes</span><span class="sxs-lookup"><span data-stu-id="659d0-113">Templates</span></span>

<span data-ttu-id="659d0-114">Organizācijas hierarhijas elementu kartes ir pieejamas datu vienvirziena sinhronizācijai no programmas Finance and Operations programmām uz Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="659d0-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="659d0-115">Iekšējais organizācijas hierarhijas nolūks</span><span class="sxs-lookup"><span data-stu-id="659d0-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="659d0-116">Šī veidne nodrošina organizācijas hierarhijas nolūka elementa vienvirziena sinhronizāciju no Finance and Operations uz citām Dynamics 365 programmām.</span><span class="sxs-lookup"><span data-stu-id="659d0-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="659d0-117">Avota lauks</span><span class="sxs-lookup"><span data-stu-id="659d0-117">Source field</span></span> | <span data-ttu-id="659d0-118">Kartes veids</span><span class="sxs-lookup"><span data-stu-id="659d0-118">Map type</span></span> | <span data-ttu-id="659d0-119">Mērķa lauks</span><span class="sxs-lookup"><span data-stu-id="659d0-119">Destination field</span></span>
---|---|---
<span data-ttu-id="659d0-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="659d0-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="659d0-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="659d0-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="659d0-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="659d0-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="659d0-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="659d0-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="659d0-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="659d0-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="659d0-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="659d0-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="659d0-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="659d0-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="659d0-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="659d0-127">msdyn\_immutable</span></span>
<span data-ttu-id="659d0-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="659d0-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="659d0-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="659d0-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="659d0-130">Iekšējais organizācijas hierarhijas veids</span><span class="sxs-lookup"><span data-stu-id="659d0-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="659d0-131">Šī veidne nodrošina organizācijas hierarhijas veida elementa vienvirziena sinhronizāciju no Finance and Operations uz citām Dynamics 365 programmām.</span><span class="sxs-lookup"><span data-stu-id="659d0-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="659d0-132">Avota lauks</span><span class="sxs-lookup"><span data-stu-id="659d0-132">Source field</span></span> | <span data-ttu-id="659d0-133">Kartes veids</span><span class="sxs-lookup"><span data-stu-id="659d0-133">Map type</span></span> | <span data-ttu-id="659d0-134">Mērķa lauks</span><span class="sxs-lookup"><span data-stu-id="659d0-134">Destination field</span></span>
---|---|---
<span data-ttu-id="659d0-135">NOSAUKUMS</span><span class="sxs-lookup"><span data-stu-id="659d0-135">NAME</span></span> | \> | <span data-ttu-id="659d0-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="659d0-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="659d0-137">Iekšējā organizācijas hierarhija</span><span class="sxs-lookup"><span data-stu-id="659d0-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="659d0-138">Šī veidne nodrošina organizācijas hierarhijas publicētā elementa vienvirziena sinhronizāciju no Finance and Operations uz citām Dynamics 365 programmām.</span><span class="sxs-lookup"><span data-stu-id="659d0-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="659d0-139">Avota lauks</span><span class="sxs-lookup"><span data-stu-id="659d0-139">Source field</span></span> | <span data-ttu-id="659d0-140">Kartes veids</span><span class="sxs-lookup"><span data-stu-id="659d0-140">Map type</span></span> | <span data-ttu-id="659d0-141">Mērķa lauks</span><span class="sxs-lookup"><span data-stu-id="659d0-141">Destination field</span></span>
---|---|---
<span data-ttu-id="659d0-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="659d0-142">VALIDTO</span></span> | \> | <span data-ttu-id="659d0-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="659d0-143">msdyn\_validto</span></span>
<span data-ttu-id="659d0-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="659d0-144">VALIDFROM</span></span> | \> | <span data-ttu-id="659d0-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="659d0-145">msdyn\_validfrom</span></span>
<span data-ttu-id="659d0-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="659d0-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="659d0-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="659d0-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="659d0-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="659d0-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="659d0-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="659d0-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="659d0-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="659d0-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="659d0-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="659d0-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="659d0-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="659d0-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="659d0-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="659d0-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="659d0-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="659d0-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="659d0-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="659d0-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="659d0-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="659d0-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="659d0-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="659d0-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="659d0-158">Iekšējā organizācija</span><span class="sxs-lookup"><span data-stu-id="659d0-158">Internal Organization</span></span>

<span data-ttu-id="659d0-159">Iekšējās organizācijas informācija Common Data Service tiek iegūta no diviem — **pārvaldības struktūrvienība** un **juridiska persona**.</span><span class="sxs-lookup"><span data-stu-id="659d0-159">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="659d0-160">Pārvaldības struktūrvienība</span><span class="sxs-lookup"><span data-stu-id="659d0-160">Operating unit</span></span>

<span data-ttu-id="659d0-161">Avota lauks</span><span class="sxs-lookup"><span data-stu-id="659d0-161">Source field</span></span> | <span data-ttu-id="659d0-162">Kartes veids</span><span class="sxs-lookup"><span data-stu-id="659d0-162">Map type</span></span> | <span data-ttu-id="659d0-163">Mērķa lauks</span><span class="sxs-lookup"><span data-stu-id="659d0-163">Destination field</span></span>
---|---|---
<span data-ttu-id="659d0-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="659d0-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="659d0-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="659d0-165">msdyn\_languageid</span></span>
<span data-ttu-id="659d0-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="659d0-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="659d0-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="659d0-167">msdyn\_namealias</span></span>
<span data-ttu-id="659d0-168">NOSAUKUMS</span><span class="sxs-lookup"><span data-stu-id="659d0-168">NAME</span></span> | \> | <span data-ttu-id="659d0-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="659d0-169">msdyn\_name</span></span>
<span data-ttu-id="659d0-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="659d0-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="659d0-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="659d0-171">msdyn\_partynumber</span></span>
<span data-ttu-id="659d0-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="659d0-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="659d0-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="659d0-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="659d0-174">Juridiska persona</span><span class="sxs-lookup"><span data-stu-id="659d0-174">Legal entity</span></span>

<span data-ttu-id="659d0-175">Avota lauks</span><span class="sxs-lookup"><span data-stu-id="659d0-175">Source field</span></span> | <span data-ttu-id="659d0-176">Kartes veids</span><span class="sxs-lookup"><span data-stu-id="659d0-176">Map type</span></span> | <span data-ttu-id="659d0-177">Mērķa lauks</span><span class="sxs-lookup"><span data-stu-id="659d0-177">Destination field</span></span>
---|---|---
<span data-ttu-id="659d0-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="659d0-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="659d0-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="659d0-179">msdyn\_namealias</span></span>
<span data-ttu-id="659d0-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="659d0-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="659d0-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="659d0-181">msdyn\_languageid</span></span>
<span data-ttu-id="659d0-182">NOSAUKUMS</span><span class="sxs-lookup"><span data-stu-id="659d0-182">NAME</span></span> | \> | <span data-ttu-id="659d0-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="659d0-183">msdyn\_name</span></span>
<span data-ttu-id="659d0-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="659d0-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="659d0-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="659d0-185">msdyn\_partynumber</span></span>
<span data-ttu-id="659d0-186">nav</span><span class="sxs-lookup"><span data-stu-id="659d0-186">none</span></span> | \>\> | <span data-ttu-id="659d0-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="659d0-187">msdyn\_type</span></span>
<span data-ttu-id="659d0-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="659d0-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="659d0-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="659d0-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="659d0-190">Uzņēmums</span><span class="sxs-lookup"><span data-stu-id="659d0-190">Company</span></span>

<span data-ttu-id="659d0-191">Nodrošina juridiskas personas (uzņēmuma) informācijas divvirzienu sinhronizāciju starp Finance and Operations un citām Dynamics 365 programmām.</span><span class="sxs-lookup"><span data-stu-id="659d0-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="659d0-192">Avota lauks</span><span class="sxs-lookup"><span data-stu-id="659d0-192">Source field</span></span> | <span data-ttu-id="659d0-193">Kartes veids</span><span class="sxs-lookup"><span data-stu-id="659d0-193">Map type</span></span> | <span data-ttu-id="659d0-194">Mērķa lauks</span><span class="sxs-lookup"><span data-stu-id="659d0-194">Destination field</span></span>
---|---|---
<span data-ttu-id="659d0-195">NOSAUKUMS</span><span class="sxs-lookup"><span data-stu-id="659d0-195">NAME</span></span> | = | <span data-ttu-id="659d0-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="659d0-196">cdm\_name</span></span>
<span data-ttu-id="659d0-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="659d0-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="659d0-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="659d0-198">cdm\_companycode</span></span>
