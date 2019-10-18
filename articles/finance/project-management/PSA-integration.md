---
title: Project Service Automation pārskats
description: Šajā tēmā ir sniegta informācija par integrācijas risinājumu no Dynamics 365 Project Service Automation uz Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250557"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="e28bb-103">Project Service Automation pārskats</span><span class="sxs-lookup"><span data-stu-id="e28bb-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e28bb-104">Risinājums Project Service Automation integrēšanai programmā Finance, izmanto līdzekli Datu integrācija, lai sinhronizētu datus Dynamics 365 Finance un Dynamics 365 Project Service Automation instancēs, izmantojot pakalpojumu Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e28bb-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="e28bb-105">Integrācijas veidnes, kas ir pieejamas līdzeklī Datu integrācija, iespējo projektu, projekta līgumu, projekta līgumu rindu, projekta līgumu rindu atskaites punktu, projekta uzdevumu, izdevumu transakciju kategoriju, stundu novērtējumu un izdevumu novērtējumu datu plūsmu no programmas Project Service Automation uz programmu Finance.</span><span class="sxs-lookup"><span data-stu-id="e28bb-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="e28bb-106">Ja lietojat versiju 7.3.0, ir jāinstalē KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="e28bb-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="e28bb-107">Pēc tam jūs varēsit integrēt fiksētas cenas projektus.</span><span class="sxs-lookup"><span data-stu-id="e28bb-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="e28bb-108">Ja izmantojat versiju 7.3.0 un pārceļat maksu transakcijas no programmas Project Service Automation, ir jāinstalē KB 4345320, lai šīs maksas ietvertu projekta rēķinā.</span><span class="sxs-lookup"><span data-stu-id="e28bb-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="e28bb-109">Ja lietojat versiju 8.0, varat izmantot projekta uzdevumu integrāciju, izdevumu transakciju kategorijas, stundu novērtējumus, izdevumu novērtējumus un funkcionalitātes bloķēšanu.</span><span class="sxs-lookup"><span data-stu-id="e28bb-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="e28bb-110">Ja lietojat versiju 8.0.1 vai jaunāku versiju, varat sinhronizēt faktiskās vērtības.</span><span class="sxs-lookup"><span data-stu-id="e28bb-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="e28bb-111">Pirms programmas Project Service Automation Finance integrēšanas ir jākonfigurē Project Service Automation integrācijas parametri.</span><span class="sxs-lookup"><span data-stu-id="e28bb-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="e28bb-112">Papildinformāciju skatiet tēmā [Project Service Automation integrācijas parametri](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e28bb-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="e28bb-113">Šis integrācijas risinājums nodrošina tiešu sinhronizēšanu tālāk norādītajos scenārijos.</span><span class="sxs-lookup"><span data-stu-id="e28bb-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="e28bb-114">Uzturiet projekta līgumus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance.</span><span class="sxs-lookup"><span data-stu-id="e28bb-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="e28bb-115">Izveidojiet projektus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance.</span><span class="sxs-lookup"><span data-stu-id="e28bb-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="e28bb-116">Uzturiet projekta līgumu rindas programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance.</span><span class="sxs-lookup"><span data-stu-id="e28bb-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="e28bb-117">Uzturiet projekta līgumu rindu atskaites punktus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance.</span><span class="sxs-lookup"><span data-stu-id="e28bb-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="e28bb-118">Uzturiet projekta uzdevumus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance.</span><span class="sxs-lookup"><span data-stu-id="e28bb-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="e28bb-119">Uzturiet izdevumu transakciju kategorijas programmā Finance un sinhronizējiet tās tieši no programmas Finance ar programmu Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e28bb-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="e28bb-120">Izveidojiet projekta stundu novērtējumus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance.</span><span class="sxs-lookup"><span data-stu-id="e28bb-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="e28bb-121">Izveidojiet projekta izdevumu novērtējumus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance.</span><span class="sxs-lookup"><span data-stu-id="e28bb-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="e28bb-122">Izveidojiet projekta laiku, izdevumus un faktiskās vērtības programmā Project Service Automation un izveidojiet projekta transakcijas programmas Project Service Automation integrācijas žurnālā, lai tos varētu grāmatot programmā Finance.</span><span class="sxs-lookup"><span data-stu-id="e28bb-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="e28bb-123">Datu sinhronizācija</span><span class="sxs-lookup"><span data-stu-id="e28bb-123">Data synchronization</span></span>

<span data-ttu-id="e28bb-124">Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana integrācijas procesa ietvaros programmās Project Service Automation un Finance.</span><span class="sxs-lookup"><span data-stu-id="e28bb-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="e28bb-125">Šobrīd nav pieejamas visas veidnes.</span><span class="sxs-lookup"><span data-stu-id="e28bb-125">Not all templates are currently available.</span></span> <span data-ttu-id="e28bb-126">Veidnes tiks izlaistas pēc to pabeigšanas.</span><span class="sxs-lookup"><span data-stu-id="e28bb-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="e28bb-127">[![Project Service Automation integrācija ar programmu Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="e28bb-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="e28bb-128">Sistēmas prasības programmai Finance</span><span class="sxs-lookup"><span data-stu-id="e28bb-128">System requirements for Finance</span></span>

<span data-ttu-id="e28bb-129">Lai izmantotu risinājumu Project Service Automation integrēšanai programmā Finance, ir jāinstalē Enterprise Edition versija 7.3 ar 12. Platformas atjauninājumu vai jaunāka versija.</span><span class="sxs-lookup"><span data-stu-id="e28bb-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="e28bb-130">Sistēmas prasības programmai Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e28bb-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="e28bb-131">Lai izmantotu risinājumu programmas Project Service Automation integrēšanai ar programmu Finance, ir jāinstalē šādi komponenti.</span><span class="sxs-lookup"><span data-stu-id="e28bb-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="e28bb-132">Dynamics 365 Project Service Automation versija 9.0.0.0 vai jaunāka versija</span><span class="sxs-lookup"><span data-stu-id="e28bb-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="e28bb-133">Risinājums No potenciālā klienta līdz skaidrai naudai programmai Dynamics 365 Sales, versija 1.14.0.0 (v14) vai jaunāka</span><span class="sxs-lookup"><span data-stu-id="e28bb-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="e28bb-134">Risinājuma Project Service Automation integrēšanai programmā Finance programmai Dynamics 365 Project Service Automation versija 1.0.0.0 vai jaunāka versija</span><span class="sxs-lookup"><span data-stu-id="e28bb-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="e28bb-135">Risinājuma programmas Project Service Automation integrēšanai ar programmu Finance instalēšana jūsu Project Service Automation instancē</span><span class="sxs-lookup"><span data-stu-id="e28bb-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="e28bb-136">Lejupielādējiet Integrēšanas risinājumu programmas Project Service Automation integrēšanai programmā Finance no [Microsoft lejupielādes centra](https://www.microsoft.com/download/details.aspx?id=57016) un izpildiet šajā risinājumā ietvertos norādījumus.</span><span class="sxs-lookup"><span data-stu-id="e28bb-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
