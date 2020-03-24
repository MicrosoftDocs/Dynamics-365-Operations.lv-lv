---
title: Iestatīt organizāciju hierarhijas
description: Šajā tēmā ir aprakstīts, kā iestatīt organizācijas hierarhijas programmā Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 29d4b686cbb66715196fca06e4642fbb8a337ace
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113855"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="2b4f3-103">Iestatīt organizāciju hierarhijas</span><span class="sxs-lookup"><span data-stu-id="2b4f3-103">Set up organization hierarchies</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2b4f3-104">Šajā tēmā ir aprakstīts, kā iestatīt organizācijas hierarhijas programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2b4f3-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="2b4f3-105">Overview</span></span>

<span data-ttu-id="2b4f3-106">Pirms kanālu izveides ir jāapstiprina, ka jūs vēlaties iestatīt organizācijas hierarhijas.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-106">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="2b4f3-107">Varat izmantot organizācijas hierarhijas, lai apskatītu jūsu uzņēmējtransakciju no dažādām perspektīvām un veidotu pārskatus.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-107">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="2b4f3-108">Piemēram, varat iestatīt vienu hierarhiju nodokļu, juridiskajai vai ar likumu noteikto pārskatu veidošanai.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-108">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="2b4f3-109">Pēc tam varat iestatīt citu hierarhiju, lai veidotu pārskatu par finanšu informāciju, kas saskaņā ar likumu nav obligāta, bet tiek izmantota iekšējos pārskatos.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-109">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="2b4f3-110">Pirms organizācijas hierarhijas izveides jāizveido organizācijas.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-110">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="2b4f3-111">Papildinformāciju skatiet sadaļā [Izveidot juridisku personu](channels-legal-entities.md) vai [izveidot struktūrvienības](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="2b4f3-111">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="2b4f3-112">Papildinformāciju skatiet tālāk norādītajās tēmās.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-112">For more information, see the following topics.</span></span>
- [<span data-ttu-id="2b4f3-113">Organizācijas un organizāciju hierarhiju pārskats</span><span class="sxs-lookup"><span data-stu-id="2b4f3-113">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="2b4f3-114">Organizācijas hierarhijas plānošana</span><span class="sxs-lookup"><span data-stu-id="2b4f3-114">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="2b4f3-115">Organizācijas hierarhijas izveide</span><span class="sxs-lookup"><span data-stu-id="2b4f3-115">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="2b4f3-116">Organizāciju hierarhijas izveide</span><span class="sxs-lookup"><span data-stu-id="2b4f3-116">Create an organizational hierarchy</span></span>

<span data-ttu-id="2b4f3-117">Lai izveidotu organizācijas hierarhijas, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-117">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="2b4f3-118">Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Organizācijas hierarhijas**.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-118">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="2b4f3-119">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="2b4f3-120">Laukā **Nosaukums** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-120">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="2b4f3-121">Sadaļā **Nolūks** atlasiet **Piešķirt nolūku**.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-121">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="2b4f3-122">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-122">In the list, find and select the desired record.</span></span> <span data-ttu-id="2b4f3-123">Atlasiet nolūku, kas tiks piešķirts jūsu organizācijas hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-123">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="2b4f3-124">Sadaļā **Piešķirtās hierarhijas** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-124">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="2b4f3-125">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-125">In the list, mark the selected row.</span></span> <span data-ttu-id="2b4f3-126">Atrodiet tikko izveidoto hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-126">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="2b4f3-127">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-127">Select **OK**.</span></span>

<span data-ttu-id="2b4f3-128">Tālāk esošajā attēlā redzama parauga organizācijas hierarhija, kas izveidota fiktīvai “Adventure Works” veikalu kopai.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-128">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![Organizācijas hierarhijas piemēri](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="2b4f3-130">Pievienot organizācijas hierarhijai</span><span class="sxs-lookup"><span data-stu-id="2b4f3-130">Add organizations to a hierarchy</span></span>

<span data-ttu-id="2b4f3-131">Lai pievienotu organizāciju hierarhijai, veiciet tālāk norādīto.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-131">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="2b4f3-132">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-132">In the list, find and select the desired record.</span></span> <span data-ttu-id="2b4f3-133">Atlasiet hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-133">Select your hierarchy.</span></span>
1. <span data-ttu-id="2b4f3-134">Darbību rūtī atlasiet **Skatīt**.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-134">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="2b4f3-135">Nepieciešamības gadījumā pievienojiet papildu organizācijas.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-135">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="2b4f3-136">Lai pievienotu organizāciju, atlasiet **Rediģēt** un pēc tam atlasiet **Ievietot**.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-136">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="2b4f3-137">Kad esat pabeidzis izmaiņu veikšanu, varat saglabāt melnrakstu un publicēt izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-137">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="2b4f3-138">Tālāk esošajā attēlā redzama juridiska persona, kas pievienota hierarhijas saknē ar četriem izmaksu centriem, kas pievienoti kanāliem “Mall”, “Outlet”, “Online” un “Call Center”.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-138">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="2b4f3-139">Katram no tiem var pievienot dažādus mazumtirdzniecības, zvanu centru un tiešsaistes kanālus.</span><span class="sxs-lookup"><span data-stu-id="2b4f3-139">Various retail, call center and online channels can then be added to each.</span></span>

![Hierarhijas dizainera piemērs](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="2b4f3-141">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="2b4f3-141">Additional resources</span></span>

[<span data-ttu-id="2b4f3-142">Organizācijas un organizāciju hierarhiju pārskats</span><span class="sxs-lookup"><span data-stu-id="2b4f3-142">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="2b4f3-143">Organizācijas hierarhijas plānošana</span><span class="sxs-lookup"><span data-stu-id="2b4f3-143">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="2b4f3-144">Izveidot juridiskās personas</span><span class="sxs-lookup"><span data-stu-id="2b4f3-144">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="2b4f3-145">Pārvaldības struktūrvienību izveide</span><span class="sxs-lookup"><span data-stu-id="2b4f3-145">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="2b4f3-146">Kanālu apskats</span><span class="sxs-lookup"><span data-stu-id="2b4f3-146">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="2b4f3-147">Kanālu iestatīšanas priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="2b4f3-147">Channel setup prerequisites</span></span>](channels-prerequisites.md)
