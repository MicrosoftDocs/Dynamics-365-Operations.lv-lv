---
title: "Project Service Automation integrācijas parametri"
description: "Varat konfigurēt datu noklusējuma iestatījumus, veicot programmas Project Service Automation integrēšanu ar programmu Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 12/13/2017
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
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 32f7f70c5b1071cef5a3360ccc09fa2d95fbf9a9
ms.contentlocale: lv-lv
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation-integration-parameters"></a><span data-ttu-id="6da66-103">Project Service Automation integrācijas parametri</span><span class="sxs-lookup"><span data-stu-id="6da66-103">Project Service Automation integration parameters</span></span>

<span data-ttu-id="6da66-104">Lapā **Project Service Automation integrācijas parametri** varat konfigurēt datu noklusējuma iestatījumu, veicot programmas Project Service Automation integrēšanu ar programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6da66-104">On the **Project Service Automation integration parameters** page, you can configure how data should default when integrating Project Service Automation with Finance and Operations.</span></span> <span data-ttu-id="6da66-105">Lai sekmīgi sinhronizētu programmā Project Service Automation ietvertos projektus ar programmu Finance and Operations, ir jāiestata šādi elementi.</span><span class="sxs-lookup"><span data-stu-id="6da66-105">The following must be set up for projects to be successfully synchronized from Project Service Automation in Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="6da66-106">Projekta uzdevumu integrācija, izdevumu transakciju kategorijas, stundu novērtējumi, izdevumu novērtējumi un funkcionalitātes bloķēšana ir pieejama programmas Dynamics 365 for Finance and Operations versijā 8.0.</span><span class="sxs-lookup"><span data-stu-id="6da66-106">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>




| <span data-ttu-id="6da66-107">**Cilne**</span><span class="sxs-lookup"><span data-stu-id="6da66-107">**Tab**</span></span>                      | <span data-ttu-id="6da66-108">**Lauks**</span><span class="sxs-lookup"><span data-stu-id="6da66-108">**Field**</span></span>                          | <span data-ttu-id="6da66-109">**Apraksts**</span><span class="sxs-lookup"><span data-stu-id="6da66-109">**Description**</span></span>                    |
|------------------------------|------------------------------------|--------------------------------|
| <span data-ttu-id="6da66-110">**Vispārīgie iestatījumi**</span><span class="sxs-lookup"><span data-stu-id="6da66-110">**General**</span></span>                  | <span data-ttu-id="6da66-111">**Noklusējuma projekta veids**</span><span class="sxs-lookup"><span data-stu-id="6da66-111">**Default project type**</span></span>               | <span data-ttu-id="6da66-112">Atlasiet noklusējuma vērtību vienumam **Projekta veids** gadījumos, kad tiek sinhronizēti programmā Project Service Automation ietvertie projekti, ja neesat norādījis noklusējuma vērtību integrācijas veidnē.</span><span class="sxs-lookup"><span data-stu-id="6da66-112">Select the default for **Project type**, which is when projects are synchronized from Project Service Automation if you have not provided a default value in the integration template.</span></span> <span data-ttu-id="6da66-113">Sinhronizēšanas laikā jauniem projektiem vienumam **Projekta veids** tiks iestatīta šī vērtība, un to var atjaunināt, veicot programmā Project Service Automation ietverto projekta līguma rindu sinhronizēšanu.</span><span class="sxs-lookup"><span data-stu-id="6da66-113">During synchronization, new projects will have the **Project type** set to this value and may be updated when the project contract lines are synchronized from Project Service Automation.</span></span>               |
| <span data-ttu-id="6da66-114">**Vispārīgie iestatījumi**</span><span class="sxs-lookup"><span data-stu-id="6da66-114">**General**</span></span>                  | <span data-ttu-id="6da66-115">**Laika kategorija**</span><span class="sxs-lookup"><span data-stu-id="6da66-115">**Time category**</span></span>                      | <span data-ttu-id="6da66-116">Atlasiet noklusējuma vērtību vienumam **Laika kategorija** gadījumos, kad tiek sinhronizēti programmā Project Service Automation ietvertie stundu novērtējumi.</span><span class="sxs-lookup"><span data-stu-id="6da66-116">Select the default for **Time category**, which is when hour estimates are synchronized from Project Service Automation.</span></span> <span data-ttu-id="6da66-117">Sinhronizēšanas laikā jaunām projekta stundu prognozēm programmā Finance and Operations vienumam **Kategorija** tiks iestatīta šī vērtība, veicot programmā Project Service Automation ietverto stundu novērtējumu un stundu faktisko vērtību sinhronizēšanu.</span><span class="sxs-lookup"><span data-stu-id="6da66-117">During synchronization, new project hour forecasts in Finance and Operations will have the **Category** set to this value when the hour estimates and hour actuals are synchronized from Project Service Automation.</span></span>   |
| <span data-ttu-id="6da66-118">**Vispārīgie iestatījumi**</span><span class="sxs-lookup"><span data-stu-id="6da66-118">**General**</span></span>                  | <span data-ttu-id="6da66-119">**Maksas kategorija**</span><span class="sxs-lookup"><span data-stu-id="6da66-119">**Fee category**</span></span>                       | <span data-ttu-id="6da66-120">Atlasiet noklusējuma vērtību vienumam **Maksas kategorija** gadījumos, kad tiek sinhronizētas programmā Project Service Automation ietvertās maksas faktiskās vērtības.</span><span class="sxs-lookup"><span data-stu-id="6da66-120">Select the default for **Fee category**, which is when fee actuals are synchronized from Project Service Automation.</span></span> <span data-ttu-id="6da66-121">Sinhronizēšanas laikā jaunām maksas transakcijām programmā Finance and Operations vienumam **Kategorija** tiks iestatīta šī vērtība, veicot programmā Project Service Automation ietverto maksas faktisko vērtību sinhronizēšanu.</span><span class="sxs-lookup"><span data-stu-id="6da66-121">During synchronization, new fee transactions in Finance and Operations will have the **Category** set to this value when the fee actuals are synchronized from Project Service Automation.</span></span>          |
| <span data-ttu-id="6da66-122">**Projektu grupas noklusējuma vērtības**</span><span class="sxs-lookup"><span data-stu-id="6da66-122">**Project group defaults**</span></span>   | <span data-ttu-id="6da66-123">**Projekta veids**</span><span class="sxs-lookup"><span data-stu-id="6da66-123">**Project type**</span></span> | <span data-ttu-id="6da66-124">Noklikšķiniet uz **Jauns**, lai pievienotu rindu, kurā var izvēlēties projekta veidu, kuram iestatīt noklusējuma projekta grupu.</span><span class="sxs-lookup"><span data-stu-id="6da66-124">Click **New** to add a row where you can select the project type for which to set the default project group.</span></span> <span data-ttu-id="6da66-125">Noteiktu projekta veidu var atlasīt tikai vienu reizi konfigurācijā.</span><span class="sxs-lookup"><span data-stu-id="6da66-125">A specific project type can be selected only once in the configuration.</span></span>              
|                              | <span data-ttu-id="6da66-126">**Projektu grupa**</span><span class="sxs-lookup"><span data-stu-id="6da66-126">**Project group**</span></span>          | <span data-ttu-id="6da66-127">Atlasiet norādītajam projekta veidam noklusējuma projekta grupu.</span><span class="sxs-lookup"><span data-stu-id="6da66-127">Select the default project group for the specified project type.</span></span> <span data-ttu-id="6da66-128">Kad tiek sinhronizēti programmā Project Service Automation ietvertie projekti, **Projekta grupa** būs noklusējuma iestatījums, kas balstīts uz projekta veidu, ja neesat norādījis noklusējuma vērtību integrācijas veidnē.</span><span class="sxs-lookup"><span data-stu-id="6da66-128">When new projects are synced from Project Service Automation, the **Project group** will be the default based on the project type if you have not provided a default value in the integration template.</span></span>  |
| <span data-ttu-id="6da66-129">**Norēķinu veida noklusējuma vērtības**</span><span class="sxs-lookup"><span data-stu-id="6da66-129">**Billing type defaults**</span></span>    | <span data-ttu-id="6da66-130">**Norēķinu veids**</span><span class="sxs-lookup"><span data-stu-id="6da66-130">**Billing type**</span></span> | <span data-ttu-id="6da66-131">Noklikšķiniet uz **Jauns**, lai pievienotu rindu, kurā var izvēlēties norēķinu veidu, kuram iestatīt noklusējuma rindas rekvizītu.</span><span class="sxs-lookup"><span data-stu-id="6da66-131">Click **New** to add a row where you can select the billing type for which to set the default line property.</span></span> <span data-ttu-id="6da66-132">Noteiktu norēķinu veidu var atlasīt tikai vienu reizi konfigurācijā.</span><span class="sxs-lookup"><span data-stu-id="6da66-132">A specific billing type can be selected only once in the configuration.</span></span>          |
|                              | <span data-ttu-id="6da66-133">**Rindas statuss**</span><span class="sxs-lookup"><span data-stu-id="6da66-133">**Line property**</span></span>| <span data-ttu-id="6da66-134">Atlasiet norādītajam norēķinu veidam noklusējuma rindas rekvizītu.</span><span class="sxs-lookup"><span data-stu-id="6da66-134">Select the default line property for the specified billing type.</span></span> <span data-ttu-id="6da66-135">Sinhronizējot programmā Project Service Automation ietvertos jaunos stundu novērtējumus, jaunos izdevumu novērtējumus vai jaunas faktiskās vērtības, vienums **Rindas rekvizīts** būs noklusējuma iestatījums, kas balstīts uz norēķinu veidu.</span><span class="sxs-lookup"><span data-stu-id="6da66-135">When new hour estimates, new expense estimates, or new actuals are synced from Project Service Automation, the **Line property** will be the default based on the billing type.</span></span>          |
| <span data-ttu-id="6da66-136">**Funkcionalitātes bloķēšana**</span><span class="sxs-lookup"><span data-stu-id="6da66-136">**Functionality locking**</span></span>    |                   | <span data-ttu-id="6da66-137">Atlasiet funkcionalitāti, kas tiks atspējota programmā Finance and Operations projektiem un līgumiem, kuru izcelsme ir Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="6da66-137">Select the functionality to disable in Finance and Operations for projects and contracts that originated from Project Service Automation.</span></span> <span data-ttu-id="6da66-138">Piemēram, varat izvēlēties izslēgt iespēju rediģēt līgumus un projektus, veidot darba sadalījuma struktūras un ievadīt darba laiku grafikus programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6da66-138">For example, you can choose to turn off the ability to edit contracts and projects, create work breakdown structures, and enter timesheets in Finance and Operations.</span></span> <span data-ttu-id="6da66-139">Ar uzskaiti saistītie lauki joprojām būs iespējoti pat tad, ja tie ir atzīmēti kā nepieejami parametru iestatījumos.</span><span class="sxs-lookup"><span data-stu-id="6da66-139">Accounting-related fields will continue to be enabled, even if they are made unavailable by the parameter setting.</span></span> <span data-ttu-id="6da66-140">Pēc noklusējuma tiks iespējotas visas funkcijas.</span><span class="sxs-lookup"><span data-stu-id="6da66-140">By default, all functionality will be enabled.</span></span>           |
