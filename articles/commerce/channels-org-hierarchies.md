---
title: Iestatīt organizāciju hierarhijas
description: Šajā tēmā aprakstīts, kā iestatīt organizāciju hierarhijas risinājumā Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4238d1aa277bf2f1df30825ef20dbf3095d13ebc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800571"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="5d60c-103">Iestatīt organizāciju hierarhijas</span><span class="sxs-lookup"><span data-stu-id="5d60c-103">Set up organization hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5d60c-104">Šajā tēmā aprakstīts, kā iestatīt organizāciju hierarhijas risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5d60c-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5d60c-105">Pirms kanālu izveides ir jāapstiprina, ka jūs vēlaties iestatīt organizācijas hierarhijas.</span><span class="sxs-lookup"><span data-stu-id="5d60c-105">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="5d60c-106">Varat izmantot organizācijas hierarhijas, lai apskatītu jūsu uzņēmējtransakciju no dažādām perspektīvām un veidotu pārskatus.</span><span class="sxs-lookup"><span data-stu-id="5d60c-106">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="5d60c-107">Piemēram, varat iestatīt vienu hierarhiju nodokļu, juridiskajai vai ar likumu noteikto pārskatu veidošanai.</span><span class="sxs-lookup"><span data-stu-id="5d60c-107">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="5d60c-108">Pēc tam varat iestatīt citu hierarhiju, lai veidotu pārskatu par finanšu informāciju, kas saskaņā ar likumu nav obligāta, bet tiek izmantota iekšējos pārskatos.</span><span class="sxs-lookup"><span data-stu-id="5d60c-108">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="5d60c-109">Pirms organizācijas hierarhijas izveides jāizveido organizācijas.</span><span class="sxs-lookup"><span data-stu-id="5d60c-109">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="5d60c-110">Papildinformāciju skatiet sadaļā [Izveidot juridisku personu](channels-legal-entities.md) vai [izveidot struktūrvienības](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="5d60c-110">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="5d60c-111">Papildinformāciju skatiet tālāk norādītajās tēmās.</span><span class="sxs-lookup"><span data-stu-id="5d60c-111">For more information, see the following topics.</span></span>
- [<span data-ttu-id="5d60c-112">Organizācijas un organizāciju hierarhiju pārskats</span><span class="sxs-lookup"><span data-stu-id="5d60c-112">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="5d60c-113">Organizācijas hierarhijas plānošana</span><span class="sxs-lookup"><span data-stu-id="5d60c-113">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="5d60c-114">Organizācijas hierarhijas izveide</span><span class="sxs-lookup"><span data-stu-id="5d60c-114">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="5d60c-115">Organizāciju hierarhijas izveide</span><span class="sxs-lookup"><span data-stu-id="5d60c-115">Create an organizational hierarchy</span></span>

<span data-ttu-id="5d60c-116">Lai izveidotu organizācijas hierarhijas, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="5d60c-116">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="5d60c-117">Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Organizācijas hierarhijas**.</span><span class="sxs-lookup"><span data-stu-id="5d60c-117">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="5d60c-118">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5d60c-118">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="5d60c-119">Laukā **Nosaukums** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="5d60c-119">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="5d60c-120">Sadaļā **Nolūks** atlasiet **Piešķirt nolūku**.</span><span class="sxs-lookup"><span data-stu-id="5d60c-120">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="5d60c-121">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="5d60c-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="5d60c-122">Atlasiet nolūku, kas tiks piešķirts jūsu organizācijas hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="5d60c-122">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="5d60c-123">Sadaļā **Piešķirtās hierarhijas** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="5d60c-123">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="5d60c-124">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="5d60c-124">In the list, mark the selected row.</span></span> <span data-ttu-id="5d60c-125">Atrodiet tikko izveidoto hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="5d60c-125">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="5d60c-126">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5d60c-126">Select **OK**.</span></span>

<span data-ttu-id="5d60c-127">Tālāk esošajā attēlā redzama parauga organizācijas hierarhija, kas izveidota fiktīvai “Adventure Works” veikalu kopai.</span><span class="sxs-lookup"><span data-stu-id="5d60c-127">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![Organizācijas hierarhijas piemēri](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="5d60c-129">Pievienot organizācijas hierarhijai</span><span class="sxs-lookup"><span data-stu-id="5d60c-129">Add organizations to a hierarchy</span></span>

<span data-ttu-id="5d60c-130">Lai pievienotu organizāciju hierarhijai, veiciet tālāk norādīto.</span><span class="sxs-lookup"><span data-stu-id="5d60c-130">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="5d60c-131">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="5d60c-131">In the list, find and select the desired record.</span></span> <span data-ttu-id="5d60c-132">Atlasiet hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="5d60c-132">Select your hierarchy.</span></span>
1. <span data-ttu-id="5d60c-133">Darbību rūtī atlasiet **Skatīt**.</span><span class="sxs-lookup"><span data-stu-id="5d60c-133">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="5d60c-134">Nepieciešamības gadījumā pievienojiet papildu organizācijas.</span><span class="sxs-lookup"><span data-stu-id="5d60c-134">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="5d60c-135">Lai pievienotu organizāciju, atlasiet **Rediģēt** un pēc tam atlasiet **Ievietot**.</span><span class="sxs-lookup"><span data-stu-id="5d60c-135">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="5d60c-136">Kad esat pabeidzis izmaiņu veikšanu, varat saglabāt melnrakstu un publicēt izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="5d60c-136">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="5d60c-137">Tālāk esošajā attēlā redzama juridiska persona, kas pievienota hierarhijas saknē ar četriem izmaksu centriem, kas pievienoti kanāliem “Mall”, “Outlet”, “Online” un “Call Center”.</span><span class="sxs-lookup"><span data-stu-id="5d60c-137">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="5d60c-138">Katram no tiem var pievienot dažādus mazumtirdzniecības, zvanu centru un tiešsaistes kanālus.</span><span class="sxs-lookup"><span data-stu-id="5d60c-138">Various retail, call center and online channels can then be added to each.</span></span>

![Hierarhijas dizainera piemērs](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="5d60c-140">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="5d60c-140">Additional resources</span></span>

[<span data-ttu-id="5d60c-141">Organizācijas un organizāciju hierarhiju pārskats</span><span class="sxs-lookup"><span data-stu-id="5d60c-141">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="5d60c-142">Organizācijas hierarhijas plānošana</span><span class="sxs-lookup"><span data-stu-id="5d60c-142">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="5d60c-143">Izveidot juridiskās personas</span><span class="sxs-lookup"><span data-stu-id="5d60c-143">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="5d60c-144">Pārvaldības struktūrvienību izveide</span><span class="sxs-lookup"><span data-stu-id="5d60c-144">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="5d60c-145">Kanālu apskats</span><span class="sxs-lookup"><span data-stu-id="5d60c-145">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="5d60c-146">Kanālu iestatīšanas priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="5d60c-146">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
