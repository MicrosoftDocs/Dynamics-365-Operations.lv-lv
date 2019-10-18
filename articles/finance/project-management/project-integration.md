---
title: Microsoft Project klienta integrācija
description: Projekta grafika plānošana un uzturēšana var būt sarežģīta, tādēļ projektu vadītājiem jāizmanto rīki, kas palīdz pārvaldīt šo uzdevumu. Integrācija ar Microsoft Project klientu nodrošina atbalstu projekta darba sadalījuma struktūras atvēršanai un pārvaldībai.
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 610990612d5fb38025bf39cc648d0c9572da37b6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174942"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="5ea3f-104">Microsoft Project klienta integrācija</span><span class="sxs-lookup"><span data-stu-id="5ea3f-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ea3f-105">Projekta grafika plānošana un uzturēšana var būt sarežģīta, tādēļ projektu vadītājiem jāizmanto rīki, kas palīdz pārvaldīt šo uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="5ea3f-106">Integrācija ar Microsoft Project klientu nodrošina atbalstu projekta darba sadalījuma struktūras atvēršanai un pārvaldībai.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="5ea3f-107">Projektu vadītājs var publicēt visas izmaiņas Dynamics 365 Finance projekta darba sadalījuma struktūrā.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="5ea3f-108">Ja lietojat jūlija atjauninājumu (versija 10.0.4), ir jāinstalē KB 4054797 un 4055884.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="5ea3f-109">Microsoft Project klienta pievienojumprogrammas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="5ea3f-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="5ea3f-110">Lai iespējotu integrāciju ar Microsoft Project klientu, lietotāja klienta Microsoft Project lietojumprogrammā ir jāinstalē Microsoft Dynamics 365 pievienojumprogramma.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="5ea3f-111">To var izdarīt, atverot darbvietu **Projektu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="5ea3f-112">•   Darbvietas sadaļā **Saites** > **Iestatīšana** noklikšķiniet uz **Konfigurēt projekta klienta pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="5ea3f-113">•   Noklikšķiniet uz **Atvērt**, un, kad tiek parādīta attiecīgā uzvedne, noklikšķiniet uz **Palaist**.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="5ea3f-114">Esošas melnraksta darba sadalījuma struktūras atvēršana un rediģēšana Microsoft Project klientā</span><span class="sxs-lookup"><span data-stu-id="5ea3f-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="5ea3f-115">Ja projektam programmā Dynamics 365 Finance jau ir izveidota darba sadalījuma struktūra, šo darba sadalījuma struktūru var atvērt Microsoft Project Client programmā, ja darba sadalījuma struktūrai ir melnraksta statuss.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="5ea3f-116">Lai to atvērtu lapā **Projekts**, cilnē **Plāns** noklikšķiniet uz saites **Atvērt programmā Microsoft Project**. Šo lapu var arī atvērt Microsoft Project klienta lietojumprogrammā, noklikšķinot uz **Atvērt** cilnē **Microsoft Dynamics 365**. Sarakstā atlasiet vienumus **Juridiska persona** un **Projekts**.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="5ea3f-117">Ja izmantojat pārlūkprogrammu Internet Explorer, ir jānoklikšķina uz **Saglabāt**, lai manuāli atvērtu failu vietā, kur tas ir lejupielādēts.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="5ea3f-118">Vai arī noklikšķiniet uz **Saglabāt un atvērt**, lai failu atvērtu Microsoft Project klientā.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="5ea3f-119">Saglabājot failu, nepārdēvējiet to.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="5ea3f-120">Pirms faila rediģēšanas, izmantojot Microsoft Project Client, tas ir jāpaņem. Cilnē **Microsoft Dynamics 365** noklikšķiniet uz **Paņemt**. Tādējādi citi lietotāji nevarēs vienlaikus rediģēt darba sadalījuma struktūru programmā Finance.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="5ea3f-121">Lai publicētu darba sadalījuma struktūru pēc rediģēšanas pabeigšanas, noklikšķiniet uz **Atdot** cilnē **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="5ea3f-122">Ja projekta grupa jau ir pievienota projektam programmā Finance, resursu saraksts tiks aizpildīts ar grupas dalībniekiem.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="5ea3f-123">Ja projektam vēl nav pievienota projekta grupa, varat atlasīt resursus un izveidot grupu Microsoft Project klientā, noklikšķinot uz pogas **Resursi** cilnē **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="5ea3f-124">Ar programmu Finance kā daļa no atdošanas procesa tiks sinhronizēti tālāk norādītie dati.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="5ea3f-125">•   Uzdevuma nosaukums</span><span class="sxs-lookup"><span data-stu-id="5ea3f-125">•   Task name</span></span>

<span data-ttu-id="5ea3f-126">•   Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="5ea3f-126">•   Start date</span></span>

<span data-ttu-id="5ea3f-127">•   Beigu datums</span><span class="sxs-lookup"><span data-stu-id="5ea3f-127">•   Finish date</span></span>

<span data-ttu-id="5ea3f-128">•   Pirmstecīgas aktivitātes</span><span class="sxs-lookup"><span data-stu-id="5ea3f-128">•   Predecessors</span></span>

<span data-ttu-id="5ea3f-129">•   Resursu nosaukumi</span><span class="sxs-lookup"><span data-stu-id="5ea3f-129">•   Resource names</span></span>

<span data-ttu-id="5ea3f-130">•   Kategorija</span><span class="sxs-lookup"><span data-stu-id="5ea3f-130">•   Category</span></span>

<span data-ttu-id="5ea3f-131">•   Resursu kategorija</span><span class="sxs-lookup"><span data-stu-id="5ea3f-131">•   Resource category</span></span>

<span data-ttu-id="5ea3f-132">•   Darba stundas</span><span class="sxs-lookup"><span data-stu-id="5ea3f-132">•   Work hours</span></span>

<span data-ttu-id="5ea3f-133">•   Piezīmes</span><span class="sxs-lookup"><span data-stu-id="5ea3f-133">•   Notes</span></span>

<span data-ttu-id="5ea3f-134">•   Prioritāte</span><span class="sxs-lookup"><span data-stu-id="5ea3f-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="5ea3f-135">Ja savam Microsoft Project klienta failam pievienosit jebkuras citas kolonnas, tās netiks saglabātas failā un netiks parādītas pēc atkārtotas faila atvēršanas.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="5ea3f-136">Darba sadalījuma struktūras izveide esošam projektam, izmantojot Microsoft Project klientu</span><span class="sxs-lookup"><span data-stu-id="5ea3f-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="5ea3f-137">Lai izveidotu jaunu darba sadalījuma struktūru, izmantojot Microsoft Project klientu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="5ea3f-138">Atveriet Microsoft Project klientu.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="5ea3f-139">Cilnē **Microsoft Dynamics 365** noklikšķiniet uz **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="5ea3f-140">Projektam atlasiet vienumu **Juridiska persona**.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="5ea3f-141">Atlasiet vienumu **Projekts**.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="5ea3f-142">Noklikšķiniet uz **Paņemt** cilnē **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="5ea3f-143">Kad fails ir gatavs publicēšanai programmā Finance, noklikšķiniet uz **Atdot** cilnē **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="5ea3f-144">Esošas darba sadalījuma struktūras aizstāšana esošam projektam, izmantojot Microsoft Project klientu</span><span class="sxs-lookup"><span data-stu-id="5ea3f-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="5ea3f-145">Lai izveidotu jaunu darba sadalījuma struktūru, izmantojot Microsoft Project klientu, un aizstātu esošu darba sadalījuma struktūru esošam projektam, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="5ea3f-146">Atveriet Microsoft Project klientu.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="5ea3f-147">Izveidojiet grafiku Microsoft Project klientā.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="5ea3f-148">Cilnē **Microsoft Dynamics 365** noklikšķiniet uz vienumiem **Saglabāt izmaiņas** > **Aizstāt esošu projektu**.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="5ea3f-149">Projektam atlasiet vienumu **Juridiska persona**.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="5ea3f-150">Atlasiet vienumu **Projekts**.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="5ea3f-151">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="5ea3f-152">Jauna projekta izveide no Microsoft Project klienta</span><span class="sxs-lookup"><span data-stu-id="5ea3f-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="5ea3f-153">Atveriet Microsoft Project klientu.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="5ea3f-154">Izveidojiet grafiku Microsoft Project klientā.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="5ea3f-155">Cilnē **Microsoft Dynamics 365** noklikšķiniet uz vienumiem **Saglabāt izmaiņas** > **Saglabāt jaunā projektā**.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="5ea3f-156">Projektam atlasiet vienumu **Juridiska persona**.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="5ea3f-157">Ievadiet **Projekta ID**, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="5ea3f-158">Ievadiet vienumu **Projekta nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="5ea3f-159">Atlasiet vienumus **Projekta tips**, **Projektu grupa** un **Projekta līguma ID**.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="5ea3f-160">Vai arī varat izveidot jaunu projekta līgumu, noklikšķinot uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="5ea3f-161">Atlasiet vienumu **Kalendārs**, ko izmantot resursiem.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="5ea3f-162">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5ea3f-162">Click **OK**.</span></span>
