---
title: Project Service Automation
description: "Šis risinājums izmanto līdzekli Datu integrācija, lai sinhronizētu datus programmu Microsoft Dynamics 365 for Finance and Operations un Microsoft Dynamics 365 for Project Service Automation instancēs, izmantojot Common Data Service (CDS)."
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: lv-lv
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a><span data-ttu-id="5d2e2-103">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="5d2e2-103">Project Service Automation</span></span>

<span data-ttu-id="5d2e2-104">Risinājums, lai veiktu integrēšanu no programmas Project Service Automation programmā Finance and Operations, izmanto līdzekli Datu integrācija, lai sinhronizētu datus programmu Microsoft Dynamics 365 for Finance and Operations un Microsoft Dynamics 365 for Project Service Automation instancēs, izmantojot Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="5d2e2-104">The Project Service Automation to Finance and Operations integration solution uses the Data Integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via the Common Data Service (CDS).</span></span> <span data-ttu-id="5d2e2-105">Integrācijas veidnes, kas ir pieejamas līdzeklī Datu integrācija, iespējo datu plūsmu par projektiem, projekta līgumiem, projektiem, projekta līguma rindām, projekta līguma rindas atskaites punktiem, projekta uzdevumiem, izdevumu transakciju kategorijām, stundu novērtējumiem un izdevumu novērtējumiem no programmas Project Service Automation programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-105">The integration templates that are available with the Data Integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE] 
> <span data-ttu-id="5d2e2-106">Ja izmantojat Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, jums ir jāinstalē KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-106">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="5d2e2-107">Tas ļaus integrēt fiksētas cenas projektus.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-107">This will allow you to integrate fixed price projects.</span></span>
>
> <span data-ttu-id="5d2e2-108">Ja izmantojat programmas Dynamics 365 for Finance and Operations versiju 8.0, varēsit izmantot projekta uzdevumu integrāciju, izdevumu transakciju kategorijas, stundu novērtējumus, izdevumu novērtējumus un funkcionalitātes bloķēšanu.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-108">If you are using Dynamics 365 for Finance and Operations version 8.0, you will be able to use project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
>
> <span data-ttu-id="5d2e2-109">Ja izmantojat programmas Dynamics 365 for Finance and Operations versiju 8.0.1, varēsit sinhronizēt faktiskās vērtības.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-109">If you are using Dynamics 365 for Finance and Operations version 8.0.1, you will be able to synchronize actuals.</span></span>
>
> <span data-ttu-id="5d2e2-110">Ja izmantojat programmu Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, pēc KB 4132657 un KB 4132660 instalēšanas varēsit izmantot veidnes, lai integrētu projekta uzdevumus, izdevumu transakciju kategorijas, stundu novērtējumus, izdevumu novērtējumus un faktiskās vērtības, kā arī konfigurēt funkcionalitātes bloķēšanu.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-110">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="5d2e2-111">Ja ir nepieciešams atiestatīt uzskaites sadali, ieteicams arī instalēt KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-111">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

<span data-ttu-id="5d2e2-112">Pirms programmas Project Service Automation integrēšanas ar programmu Finance and Operations ir jākonfigurē Project Service Automation integrācijas parametri.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-112">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="5d2e2-113">Papildu informāciju skatiet sadaļā Project Service Automation integrācijas parametri.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-113">For more information, see Project Service Automation integration parameters.</span></span>

<span data-ttu-id="5d2e2-114">Šis integrācijas risinājums nodrošina tiešu sinhronizēšanu tālāk norādītajos scenārijos.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-114">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="5d2e2-115">Uzturiet projekta līgumus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-115">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="5d2e2-116">Izveidojiet projektus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-116">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="5d2e2-117">Uzturiet projekta līguma rindas programmā Project Service Automation un sinhronizējiet tās tieši no programmas Project Service Automation ar programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-117">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="5d2e2-118">Uzturiet projekta līguma rindas atskaites punktus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-118">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="5d2e2-119">Uzturiet projekta uzdevumus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-119">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="5d2e2-120">Uzturiet izdevumu transakciju kategorijas programmā Finance and Operations un sinhronizējiet tās tieši no programmas Finance and Operations ar programmu Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-120">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="5d2e2-121">Izveidojiet projekta stundu novērtējumus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-121">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="5d2e2-122">Izveidojiet projekta izdevumu novērtējumus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-122">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="5d2e2-123">Datu sinhronizācija</span><span class="sxs-lookup"><span data-stu-id="5d2e2-123">Data synchronization</span></span>
<span data-ttu-id="5d2e2-124">Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana integrācijas procesa ietvaros programmās Project Service Automation un Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="5d2e2-125">Šobrīd nav pieejamas visas veidnes.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-125">Not all templates are currently available.</span></span> <span data-ttu-id="5d2e2-126">Veidnes tiks izlaistas pēc to pabeigšanas.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="5d2e2-127">[![Programmas Project Service Automation integrēšana ar programmu Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="5d2e2-127">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="5d2e2-128">Sistēmas prasības programmai Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5d2e2-128">System requirements for Finance and Operations</span></span>

<span data-ttu-id="5d2e2-129">Lai izmantotu risinājumu programmas Project Service Automation integrēšanai ar programmu Finance and Operations, ir jāinstalē programma Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 ar platformas 12. atjauninājumu vai jaunāku versiju.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-129">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="5d2e2-130">Sistēmas prasības programmai Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="5d2e2-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="5d2e2-131">Lai izmantotu risinājumu programmas Project Service Automation integrēšanai ar programmu Finance and Operations, ir jāinstalē šādi komponenti.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-131">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="5d2e2-132">Microsoft Dynamics 365 for Project Service Automation, versija 9.0.0.0 vai jaunāka.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-132">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later.</span></span>
- <span data-ttu-id="5d2e2-133">Risinājums No potenciālā klienta līdz skaidrai naudai programmai Dynamics 365 for Sales, versija 1.14.0.0 (v14) vai jaunāka.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-133">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>
- <span data-ttu-id="5d2e2-134">Risinājums programmas Project Service Automation integrēšanai ar Finance and Operations programmai Dynamics 365 for Project Service Automation, versija 1.0.0.0 vai jaunāka.</span><span class="sxs-lookup"><span data-stu-id="5d2e2-134">Project Service Automation to Operations solution for Dynamics 365 for Project Service Automation version 1.0.0.0 or later.</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="5d2e2-135">Risinājuma programmas Project Service Automation integrēšanai ar programmu Finance and Operations instalēšana jūsu Project Service Automation instancē</span><span class="sxs-lookup"><span data-stu-id="5d2e2-135">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>



