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
ms.openlocfilehash: 889cc90b534de33ccd0e2bea367b2da42b5d72e0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006189"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="670e7-103">Uzdevumu pārvaldība punktā POS</span><span class="sxs-lookup"><span data-stu-id="670e7-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="670e7-104">Šajā tēmā aprakstīta uzdevumu pārvaldība Microsoft Dynamics 365 Commerce pārdošanas punkta (POS) programmā.</span><span class="sxs-lookup"><span data-stu-id="670e7-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

## <a name="overview"></a><span data-ttu-id="670e7-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="670e7-105">Overview</span></span>

<span data-ttu-id="670e7-106">Dynamics 365 Commerce POS programmai ir uzdevumu pārvaldības līdzekļi, kas ļauj veikala vadītājiem un darbiniekiem pārvaldīt uzdevumus un atjaunināt uzdevumu statusu.</span><span class="sxs-lookup"><span data-stu-id="670e7-106">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="670e7-107">Veikala darbinieki var piekļūt uzdevumiem, atlasot elementu **Uzdevumi** POS sākumlapā vai atlasot uzdevumu paziņojumus.</span><span class="sxs-lookup"><span data-stu-id="670e7-107">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="670e7-108">Pēc noklusējuma veikala darbinieki tiek uzņemti cilnē **Mani uzdevumi**, kur tie var skatīt sev piešķirtos uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="670e7-108">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="670e7-109">Tomēr viņi var viegli pārslēgties uz cilnēm **Nokavētie uzdevumi**, **Atvērtie uzdevumi** un **Uzdevumu saraksti**.</span><span class="sxs-lookup"><span data-stu-id="670e7-109">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="670e7-110">Uzdevumu operācijas veikala pārvaldniekiem</span><span class="sxs-lookup"><span data-stu-id="670e7-110">Task operations for store managers</span></span>

<span data-ttu-id="670e7-111">Veikala pārvaldnieki var veikt šādas uzdevumu darbības POS programmā, izmantojot pogas komandjoslā:</span><span class="sxs-lookup"><span data-stu-id="670e7-111">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="670e7-112">**Piešķirt** – piešķir atlasītos uzdevumus veikala darbiniekam.</span><span class="sxs-lookup"><span data-stu-id="670e7-112">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="670e7-113">**Uzdevuma statuss** — maina atlasīto uzdevumu statusu.</span><span class="sxs-lookup"><span data-stu-id="670e7-113">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="670e7-114">**Filtrēt** – pēc noklusējuma tiek parādīti tikai aktīvie uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="670e7-114">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="670e7-115">Tomēr, lietojot filtrus, vadītāji var skatīt visus uzdevumus, pat uzdevumus, kas ir pabeigti vai atcelti.</span><span class="sxs-lookup"><span data-stu-id="670e7-115">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="670e7-116">**Jauns uzdevums** — izveidojiet uzdevumu ar esošu uzdevumu sarakstu vai izveidojiet viena mērķa uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="670e7-116">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="670e7-117">Veikala darbinieki var veikt šādas uzdevumu darbības POS programmā, izmantojot pogas komandjoslā:</span><span class="sxs-lookup"><span data-stu-id="670e7-117">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="670e7-118">**Uzdevuma statuss** — maina atlasīto uzdevumu statusu.</span><span class="sxs-lookup"><span data-stu-id="670e7-118">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="670e7-119">**Filtrēt** – pēc noklusējuma tiek parādīti tikai aktīvie uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="670e7-119">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="670e7-120">Tomēr, lietojot filtrus, darbinieki var skatīt visus uzdevumus, pat uzdevumus, kas ir pabeigti vai atcelti.</span><span class="sxs-lookup"><span data-stu-id="670e7-120">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="670e7-121">Šajā attēlā redzama cilne **Mani uzdevumi** programmā Commerce POS.</span><span class="sxs-lookup"><span data-stu-id="670e7-121">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![Manu uzdevumu cilne Commerce POS programmā](media/POS-task-management.png)

<span data-ttu-id="670e7-123">Nākamajā attēlā ir redzama cilne **Uzdevumu saraksti**.</span><span class="sxs-lookup"><span data-stu-id="670e7-123">The following illustration shows the **Task lists** tab.</span></span>

![Uzdevumu sarakstu cilne Commerce POS programmā](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="670e7-125">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="670e7-125">Additional resources</span></span>

[<span data-ttu-id="670e7-126">Uzdevumu pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="670e7-126">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="670e7-127">Uzdevumu pārvaldības konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="670e7-127">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="670e7-128">Uzdevumu sarakstu izveidošana un uzdevumu pievienošana</span><span class="sxs-lookup"><span data-stu-id="670e7-128">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="670e7-129">Uzdevumu sarakstu piešķiršana veikaliem vai darbiniekiem</span><span class="sxs-lookup"><span data-stu-id="670e7-129">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)
