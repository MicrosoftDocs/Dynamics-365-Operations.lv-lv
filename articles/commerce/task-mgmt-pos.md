---
title: Uzdevumu pārvaldība punktā POS
description: Šajā tēmā aprakstīta uzdevumu pārvaldība Microsoft Dynamics 365 Commerce pārdošanas punkta (POS) programmā.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 18ba781795058de6228c712c6a22e59038e96368
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478366"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="2668e-103">Uzdevumu pārvaldība punktā POS</span><span class="sxs-lookup"><span data-stu-id="2668e-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2668e-104">Šajā tēmā aprakstīta uzdevumu pārvaldība Microsoft Dynamics 365 Commerce pārdošanas punkta (POS) programmā.</span><span class="sxs-lookup"><span data-stu-id="2668e-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="2668e-105">Dynamics 365 Commerce POS programmai ir uzdevumu pārvaldības līdzekļi, kas ļauj veikala vadītājiem un darbiniekiem pārvaldīt uzdevumus un atjaunināt uzdevumu statusu.</span><span class="sxs-lookup"><span data-stu-id="2668e-105">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="2668e-106">Veikala darbinieki var piekļūt uzdevumiem, atlasot elementu **Uzdevumi** POS sākumlapā vai atlasot uzdevumu paziņojumus.</span><span class="sxs-lookup"><span data-stu-id="2668e-106">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="2668e-107">Pēc noklusējuma veikala darbinieki tiek uzņemti cilnē **Mani uzdevumi**, kur tie var skatīt sev piešķirtos uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="2668e-107">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="2668e-108">Tomēr viņi var viegli pārslēgties uz cilnēm **Nokavētie uzdevumi**, **Atvērtie uzdevumi** un **Uzdevumu saraksti**.</span><span class="sxs-lookup"><span data-stu-id="2668e-108">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="2668e-109">Uzdevumu operācijas veikala pārvaldniekiem</span><span class="sxs-lookup"><span data-stu-id="2668e-109">Task operations for store managers</span></span>

<span data-ttu-id="2668e-110">Veikala pārvaldnieki var veikt šādas uzdevumu darbības POS programmā, izmantojot pogas komandjoslā:</span><span class="sxs-lookup"><span data-stu-id="2668e-110">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="2668e-111">**Piešķirt** – piešķir atlasītos uzdevumus veikala darbiniekam.</span><span class="sxs-lookup"><span data-stu-id="2668e-111">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="2668e-112">**Uzdevuma statuss** — maina atlasīto uzdevumu statusu.</span><span class="sxs-lookup"><span data-stu-id="2668e-112">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="2668e-113">**Filtrēt** – pēc noklusējuma tiek parādīti tikai aktīvie uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="2668e-113">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="2668e-114">Tomēr, lietojot filtrus, vadītāji var skatīt visus uzdevumus, pat uzdevumus, kas ir pabeigti vai atcelti.</span><span class="sxs-lookup"><span data-stu-id="2668e-114">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="2668e-115">**Jauns uzdevums** — izveidojiet uzdevumu ar esošu uzdevumu sarakstu vai izveidojiet viena mērķa uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="2668e-115">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="2668e-116">Veikala darbinieki var veikt šādas uzdevumu darbības POS programmā, izmantojot pogas komandjoslā:</span><span class="sxs-lookup"><span data-stu-id="2668e-116">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="2668e-117">**Uzdevuma statuss** — maina atlasīto uzdevumu statusu.</span><span class="sxs-lookup"><span data-stu-id="2668e-117">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="2668e-118">**Filtrēt** – pēc noklusējuma tiek parādīti tikai aktīvie uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="2668e-118">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="2668e-119">Tomēr, lietojot filtrus, darbinieki var skatīt visus uzdevumus, pat uzdevumus, kas ir pabeigti vai atcelti.</span><span class="sxs-lookup"><span data-stu-id="2668e-119">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="2668e-120">Šajā attēlā redzama cilne **Mani uzdevumi** programmā Commerce POS.</span><span class="sxs-lookup"><span data-stu-id="2668e-120">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![Manu uzdevumu cilne Commerce POS programmā](media/POS-task-management.png)

<span data-ttu-id="2668e-122">Nākamajā attēlā ir redzama cilne **Uzdevumu saraksti**.</span><span class="sxs-lookup"><span data-stu-id="2668e-122">The following illustration shows the **Task lists** tab.</span></span>

![Uzdevumu sarakstu cilne Commerce POS programmā](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="2668e-124">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="2668e-124">Additional resources</span></span>

[<span data-ttu-id="2668e-125">Uzdevumu pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="2668e-125">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="2668e-126">Uzdevumu pārvaldības konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="2668e-126">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="2668e-127">Uzdevumu sarakstu izveidošana un uzdevumu pievienošana</span><span class="sxs-lookup"><span data-stu-id="2668e-127">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="2668e-128">Uzdevumu sarakstu piešķiršana veikaliem vai darbiniekiem</span><span class="sxs-lookup"><span data-stu-id="2668e-128">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
