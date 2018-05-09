---
title: "Microsoft Project klienta integrācija"
description: "Projekta grafika plānošana un uzturēšana var būt sarežģīta, tādēļ projektu vadītājiem jāizmanto rīki, kas palīdz pārvaldīt šo uzdevumu. Integrācija ar Microsoft Project klientu nodrošina atbalstu projekta darba sadalījuma struktūras atvēršanai un pārvaldībai."
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a54e1281dc54e1656298ea86c0724ad18ceff9a2
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="microsoft-project-client-integration"></a><span data-ttu-id="f0e1e-104">Microsoft Project klienta integrācija</span><span class="sxs-lookup"><span data-stu-id="f0e1e-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0e1e-105">Projekta grafika plānošana un uzturēšana var būt sarežģīta, tādēļ projektu vadītājiem jāizmanto rīki, kas palīdz pārvaldīt šo uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="f0e1e-106">Integrācija ar Microsoft Project klientu nodrošina atbalstu projekta darba sadalījuma struktūras atvēršanai un pārvaldībai.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="f0e1e-107">Projektu vadītājs var publicēt visas izmaiņas Finance and Operations projekta darba sadalījuma struktūrā.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-107">The project manager can publish any changes back to the Finance and Operations project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="f0e1e-108">Ja izmantojat Microsoft Dynamics 365 for Finance and Operations jūlija atjauninājumu, jums ir jāinstalē KB 4054797 un 4055884.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-108">If you are using Microsoft Dynamics 365 for Finance and Operations, July update, you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="f0e1e-109">Microsoft Project klienta pievienojumprogrammas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="f0e1e-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="f0e1e-110">Lai iespējotu integrāciju ar Microsoft Project klientu, lietotāja klienta Microsoft Project programmā ir jāinstalē Microsoft Dynamics 365 pievienojumprogramma.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="f0e1e-111">To var izdarīt, atverot darbvietu **Projektu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="f0e1e-112">•   Darbvietas sadaļā **Saites** > **Iestatīšana** noklikšķiniet uz **Konfigurēt projekta klienta pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="f0e1e-113">•   Noklikšķiniet uz **Atvērt**, un, kad tiek parādīta attiecīgā uzvedne, noklikšķiniet uz **Palaist**.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="f0e1e-114">Esošas melnraksta darba sadalījuma struktūras atvēršana un rediģēšana Microsoft Project klientā</span><span class="sxs-lookup"><span data-stu-id="f0e1e-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="f0e1e-115">Ja projektam programmā Finance and Operations jau ir izveidota darba sadalījuma struktūra, šo darba sadalījuma struktūru var atvērt Microsoft Project klienta lietojumprogrammā, ja darba sadalījuma struktūrai ir melnraksta statuss.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-115">If a project in Finance and Operations already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="f0e1e-116">Lai atvērtu no lapas **Projekts**, cilnē **Plāns** noklikšķiniet uz saites **Atvērt programmā Microsoft Project**. Šo lapu var arī atvērt no Microsoft Project klienta lietojumprogrammas, cilnē **Microsoft Dynamics 365** noklikšķinot uz **Atvērt**. Sarakstā atlasiet vienumus **Juridiska persona** un **Projekts**.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="f0e1e-117">Ja izmantojat pārlūkprogrammu Internet Explorer, jums jānoklikšķina uz **Saglabāt**, lai manuāli atvērtu no vietas, kurā fails ir lejupielādēts.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="f0e1e-118">Vai arī noklikšķiniet uz **Saglabāt un atvērt**, lai failu atvērtu Microsoft Project klientā.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="f0e1e-119">Saglabājot failu, nepārdēvējiet to.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="f0e1e-120">Pirms veicat jebkādu rediģēšanu failā, izmantojot Microsoft Project klientu, jums tas ir jāpaņem. Cilnē **Microsoft Dynamics 365** noklikšķiniet uz **Paņemt**. Tādējādi citi lietotāji nevarēs vienlaikus rediģēt darba sadalījuma struktūru no programmas Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance and Operations at the same time.</span></span> <span data-ttu-id="f0e1e-121">Lai darba sadalījuma struktūru publicētu pēc rediģēšanas pabeigšanas, cilnē **Microsoft Dynamics 365** noklikšķiniet uz **Atdot**.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="f0e1e-122">Ja projekta grupa jau ir pievienota projektam programmā Finance and Operations, resursu saraksts tiks aizpildīts ar grupas dalībniekiem.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-122">If a project team has already been added to the project in Finance and Operations, the resource list will be populated with the team members.</span></span> <span data-ttu-id="f0e1e-123">Ja projekta grupa vēl nav pievienota projektam, varat atlasīt resursus un izveidot grupu Microsoft Project klientā, cilnē **Microsoft Dynamics 365** noklikšķinot uz pogas **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="f0e1e-124">Ar programmu Finance and Operations kā daļa no atdošanas procesa tiks sinhronizēti tālāk norādītie dati.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-124">The following data will be synced back to Finance and Operations as part of the check in process:</span></span>

<span data-ttu-id="f0e1e-125">•   Uzdevuma nosaukums</span><span class="sxs-lookup"><span data-stu-id="f0e1e-125">•   Task name</span></span>

<span data-ttu-id="f0e1e-126">•   Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="f0e1e-126">•   Start date</span></span>

<span data-ttu-id="f0e1e-127">•   Beigu datums</span><span class="sxs-lookup"><span data-stu-id="f0e1e-127">•   Finish date</span></span>

<span data-ttu-id="f0e1e-128">•   Pirmstecīgas aktivitātes</span><span class="sxs-lookup"><span data-stu-id="f0e1e-128">•   Predecessors</span></span>

<span data-ttu-id="f0e1e-129">•   Resursu nosaukumi</span><span class="sxs-lookup"><span data-stu-id="f0e1e-129">•   Resource names</span></span>

<span data-ttu-id="f0e1e-130">•   Kategorija</span><span class="sxs-lookup"><span data-stu-id="f0e1e-130">•   Category</span></span>

<span data-ttu-id="f0e1e-131">•   Resursu kategorija</span><span class="sxs-lookup"><span data-stu-id="f0e1e-131">•   Resource category</span></span>

<span data-ttu-id="f0e1e-132">•   Darba stundas</span><span class="sxs-lookup"><span data-stu-id="f0e1e-132">•   Work hours</span></span>

<span data-ttu-id="f0e1e-133">•   Piezīmes</span><span class="sxs-lookup"><span data-stu-id="f0e1e-133">•   Notes</span></span>

<span data-ttu-id="f0e1e-134">•   Prioritāte</span><span class="sxs-lookup"><span data-stu-id="f0e1e-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="f0e1e-135">Ja savam Microsoft Project klienta failam pievienosit jebkuras citas kolonnas, tās netiks saglabātas failā un netiks parādītas pēc atkārtotas faila atvēršanas.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="f0e1e-136">Darba sadalījuma struktūras izveide esošam projektam, izmantojot Microsoft Project klientu</span><span class="sxs-lookup"><span data-stu-id="f0e1e-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="f0e1e-137">Lai izveidotu jaunu darba sadalījuma struktūru, izmantojot Microsoft Project klientu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="f0e1e-138">Atveriet Microsoft Project klientu.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="f0e1e-139">Cilnē **Microsoft Dynamics 365** noklikšķiniet uz **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="f0e1e-140">Projektam atlasiet vienumu **Juridiska persona**.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="f0e1e-141">Atlasiet vienumu **Projekts**.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="f0e1e-142">Cilnē **Microsoft Dynamics 365** noklikšķiniet uz **Paņemt**.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="f0e1e-143">Kad fails ir gatavs publicēšanai programmā Finance and Operations, cilnē **Microsoft Dynamics 365** noklikšķiniet uz **Atdot**.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-143">When ready to publish to Finance and Operations, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="f0e1e-144">Esošas darba sadalījuma struktūras aizstāšana esošam projektam, izmantojot Microsoft Project klientu</span><span class="sxs-lookup"><span data-stu-id="f0e1e-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="f0e1e-145">Lai izveidotu jaunu darba sadalījuma struktūru, izmantojot Microsoft Project klientu, un aizstātu esošu darba sadalījuma struktūru esošam projektam, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="f0e1e-146">Atveriet Microsoft Project klientu.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="f0e1e-147">Izveidojiet grafiku Microsoft Project klientā.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="f0e1e-148">Cilnē **Microsoft Dynamics 365** noklikšķiniet uz vienumiem **Saglabāt izmaiņas** > **Aizstāt esošu projektu**.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="f0e1e-149">Projektam atlasiet vienumu **Juridiska persona**.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="f0e1e-150">Atlasiet vienumu **Projekts**.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="f0e1e-151">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="f0e1e-152">Jauna projekta izveide no Microsoft Project klienta</span><span class="sxs-lookup"><span data-stu-id="f0e1e-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="f0e1e-153">Atveriet Microsoft Project klientu.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="f0e1e-154">Izveidojiet grafiku Microsoft Project klientā.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="f0e1e-155">Cilnē **Microsoft Dynamics 365** noklikšķiniet uz vienumiem **Saglabāt izmaiņas** > **Saglabāt jaunā projektā**.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="f0e1e-156">Projektam atlasiet vienumu **Juridiska persona**.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="f0e1e-157">Ievadiet **Projekta ID**, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="f0e1e-158">Ievadiet vienumu **Projekta nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="f0e1e-159">Atlasiet vienumus **Projekta tips**, **Projektu grupa** un **Projekta līguma ID**.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="f0e1e-160">Vai arī varat izveidot jaunu projekta līgumu, noklikšķinot uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="f0e1e-161">Atlasiet vienumu **Kalendārs**, ko izmantot resursiem.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="f0e1e-162">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="f0e1e-162">Click **OK**.</span></span>

