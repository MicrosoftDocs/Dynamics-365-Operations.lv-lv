---
title: Uzdevumu sarakstu izveidošana un uzdevumu pievienošana
description: Šī tēma aprakstīts, kā izveidot uzdevumu sarakstus un tiem pievienot uzdevumus Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cca5e0efd6516d02c372e8a616b6bb0c39f3088c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006214"
---
# <a name="create-task-lists-and-add-tasks"></a><span data-ttu-id="48a11-103">Uzdevumu sarakstu izveidošana un uzdevumu pievienošana</span><span class="sxs-lookup"><span data-stu-id="48a11-103">Create task lists and add tasks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="48a11-104">Šī tēma aprakstīts, kā izveidot uzdevumu sarakstus un tiem pievienot uzdevumus Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="48a11-104">This topic describes how to create task lists and add tasks to them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="48a11-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="48a11-105">Overview</span></span>

<span data-ttu-id="48a11-106">*Uzdevums* definē noteiktu darba daļu vai darbību, ko kādam jāpabeidz noteiktā termiņā vai pirms tā.</span><span class="sxs-lookup"><span data-stu-id="48a11-106">A *task* defines a specific piece of work or an action that someone must complete on or before a specified due date.</span></span> <span data-ttu-id="48a11-107">Programmā Dynamics 365 Commerce uzdevums var iekļaut detalizētas instrukcijas un informāciju par kontaktpersonu.</span><span class="sxs-lookup"><span data-stu-id="48a11-107">In Dynamics 365 Commerce, a task can include detailed instructions and information about a contact person.</span></span> <span data-ttu-id="48a11-108">Tas var ietvert arī saites uz fona darbībām, pārdošanas punktu (POS) operācijām vai vietnes lapām, lai palīdzētu uzlabot produktivitāti un nodrošinātu kontekstu, kas ir nepieciešams uzdevuma īpašniekam efektīvai uzdevuma pabeigšanai.</span><span class="sxs-lookup"><span data-stu-id="48a11-108">It can also include links to back-office operations, point of sale (POS) operations, or site pages, to help improve productivity and provide the context that the task owner requires to complete the task efficiently.</span></span>

<span data-ttu-id="48a11-109">*Uzdevumu saraksts* ir uzdevumu apkopojums, kas ir jāpabeidz kā daļa no biznesa procesa.</span><span class="sxs-lookup"><span data-stu-id="48a11-109">A *task list* is a collection of tasks that must be completed as part of a business process.</span></span> <span data-ttu-id="48a11-110">Piemēram, var būt uzdevumu saraksts, kas jaunajam darbiniekam ir jāizpilda pievienošanās laikā, uzdevumu saraksts kasieriem, kuri strādā vakara maiņas, vai uzdevumu saraksts, kas jāaizpilda, lai sagatavotu veikalu gaidāmai atvaļinājumu sezonai.</span><span class="sxs-lookup"><span data-stu-id="48a11-110">For example, there might be a task list that a new worker must complete during onboarding, a task list for cashiers who work evening shifts, or a task list that must be completed to prepare the store for an upcoming holiday season.</span></span> <span data-ttu-id="48a11-111">Programmā Commerce katram uzdevumu sarakstam, kam ir mērķa datums, var piešķirt neierobežotu skaitu veikalu vai darbinieku, un var konfigurēt tā periodiskumu.</span><span class="sxs-lookup"><span data-stu-id="48a11-111">In Commerce, every task list that has a target date can be assigned to any number of stores or employees, and it can be configured to recur.</span></span>

<span data-ttu-id="48a11-112">Gan vadītāji, gan darbinieki var izveidot uzdevumu sarakstus Commerce atbalsta birojā, un pēc tam piešķirt tos veikalu kopai.</span><span class="sxs-lookup"><span data-stu-id="48a11-112">Both managers and workers can create task lists in Commerce back office, and then assign them to a set of stores.</span></span>

## <a name="create-a-task-list"></a><span data-ttu-id="48a11-113">Izveidot uzdevumu sarakstu</span><span class="sxs-lookup"><span data-stu-id="48a11-113">Create a task list</span></span>

<span data-ttu-id="48a11-114">Lai izveidotu uzdevumu sarakstu, izpildiet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="48a11-114">To create a task list, follow these steps.</span></span>

1. <span data-ttu-id="48a11-115">Dodieties uz **Retail un Commerce \>Uzdevumu pārvaldība \>Uzdevumu pārvaldības administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="48a11-115">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="48a11-116">Atlasiet **Jauns** un pēc tam ievadiet vērtības laukos **Nosaukums**, **Apraksts** un **Īpašnieks**.</span><span class="sxs-lookup"><span data-stu-id="48a11-116">Select **New**, and then enter values in the **Name**, **Description**, and **Owner** fields.</span></span>
1. <span data-ttu-id="48a11-117">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="48a11-117">Select **Save**.</span></span>

## <a name="add-tasks-to-a-task-list"></a><span data-ttu-id="48a11-118">Uzdevumu pievienošana uzdevumu sarakstam</span><span class="sxs-lookup"><span data-stu-id="48a11-118">Add tasks to a task list</span></span>

<span data-ttu-id="48a11-119">Lai uzdevumu sarakstam pievienotu uzdevumus, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="48a11-119">To add tasks to a task list, follow these steps.</span></span>
 
1. <span data-ttu-id="48a11-120">Esoša uzdevuma kopsavilkuma cilnē **Uzdevumi** atlasiet **Jauns**, lai pievienotu uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="48a11-120">On the **Tasks** FastTab of an existing task list, select **New** to add a task.</span></span>
1. <span data-ttu-id="48a11-121">Dialoglodziņā **Izveidot jaunu uzdevumu**, laukā **Nosaukums** ievadiet uzdevuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="48a11-121">In the **Create a new task** dialog box, in the **Name** field, enter a name for the task.</span></span>
1. <span data-ttu-id="48a11-122">Laukā **Izpildes datuma nobīde no mērķa datuma** ievadiet pozitīvu vai negatīvu veselu skaitli.</span><span class="sxs-lookup"><span data-stu-id="48a11-122">In the **Due data offset from target date** field, enter a positive or negative integer value.</span></span> <span data-ttu-id="48a11-123">Piemēram, ievadiet **-2**, ja uzdevums jāpabeidz divas dienas pirms uzdevumu saraksta izpildes datuma.</span><span class="sxs-lookup"><span data-stu-id="48a11-123">For example, enter **-2** if the task should be completed two days before the task list's due date.</span></span>
1. <span data-ttu-id="48a11-124">Laukā **Piezīmes** Ievadiet detalizētus norādījumus.</span><span class="sxs-lookup"><span data-stu-id="48a11-124">In the **Notes** field, enter detailed instructions.</span></span>
1. <span data-ttu-id="48a11-125">Laukā **Kontaktpersona** ievadiet tēmas eksperta vārdu, ar kuru uzdevuma īpašnieks var sazināties, ja viņam ir nepieciešama palīdzība.</span><span class="sxs-lookup"><span data-stu-id="48a11-125">In the **Contact person** field, enter the name of a subject matter expert that the task owner can contact if he or she needs help.</span></span>
1. <span data-ttu-id="48a11-126">Laukā **Uzdevuma saite** ievadiet saiti, pamatojoties uz uzdevuma iedabu.</span><span class="sxs-lookup"><span data-stu-id="48a11-126">In the **Task link** field, enter a link, based on the nature of the task.</span></span>

> [!TIP]
> <span data-ttu-id="48a11-127">Lai gan varat izmantot lauku **Piešķirts**, lai piešķirtu uzdevumus kādam, kamēr veidojat uzdevumu sarakstu, mēs iesakām izvairīties no uzdevumu piešķiršanas uzdevumu saraksta izveides laikā.</span><span class="sxs-lookup"><span data-stu-id="48a11-127">Although you can use the **Assigned to** field to assign tasks to someone while you're creating a task list, we recommend that you avoid assigning tasks during task list creation.</span></span> <span data-ttu-id="48a11-128">Tā vietā piešķiriet uzdevumus pēc tam, kas atsevišķu veikalu sarakstam ir izveidota instance.</span><span class="sxs-lookup"><span data-stu-id="48a11-128">Instead, assign the tasks after the list is instantiated for individual stores.</span></span>

## <a name="use-task-links-to-help-improve-worker-productivity"></a><span data-ttu-id="48a11-129">Izmantojiet uzdevumu saites, lai uzlabotu darbinieku produktivitāti</span><span class="sxs-lookup"><span data-stu-id="48a11-129">Use task links to help improve worker productivity</span></span>

<span data-ttu-id="48a11-130">Commerce ļauj saistīt uzdevumus ar konkrētām POS operācijām, piemēram, palaižot pārdošanas pārskatu, apskatot tiešsaistes mācību videoklipu jaunai darbinieka orientācijai vai veicot darbību operāciju uzskaites daļā.</span><span class="sxs-lookup"><span data-stu-id="48a11-130">Commerce lets you link tasks to specific POS operations, such as running a sales report, viewing an online training video for new employee orientation, or performing a back-office operation.</span></span> <span data-ttu-id="48a11-131">Šis līdzeklis palīdz uzdevumu īpašniekiem iegūt informāciju, kas nepieciešama efektīvai uzdevuma izpildei.</span><span class="sxs-lookup"><span data-stu-id="48a11-131">This feature helps task owners get the information that they need to complete a task efficiently.</span></span>

<span data-ttu-id="48a11-132">Lai, veidojot uzdevumu, pievienotu uzdevumu saites, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="48a11-132">To add task links while you create a task, follow these steps.</span></span>

1. <span data-ttu-id="48a11-133">Esoša uzdevuma kopsavilkuma cilnē **Uzdevumi** atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="48a11-133">On the **Tasks** FastTab of an existing task list, select **Edit**.</span></span>
1. <span data-ttu-id="48a11-134">Dialoglodziņā **Rediģēt uzdevumu** laukā **Uzdevuma saite** atlasiet vienu vai vairākas no šīm opcijām:</span><span class="sxs-lookup"><span data-stu-id="48a11-134">In the **Edit task** dialog box, in the **Task link** field, select one or more of the following options:</span></span>

    - <span data-ttu-id="48a11-135">Atlasiet **Izvēlnes elements**, lai konfigurētu operāciju uzskaites daļas darbību, piemēram "Preču komplekti."</span><span class="sxs-lookup"><span data-stu-id="48a11-135">Select **Menu item** to configure a back-office operation, such as "Product kits."</span></span>
    - <span data-ttu-id="48a11-136">Atlasiet **POS operācija**, lai konfigurētu POS operāciju, piemēram, "Pārdošanas pārskati."</span><span class="sxs-lookup"><span data-stu-id="48a11-136">Select **POS Operation** to configure a POS operation, such as "Sales reports."</span></span>
    - <span data-ttu-id="48a11-137">Atlasiet **URL**, lai konfigurētu absolūto vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="48a11-137">Select **URL** to configure an absolute URL.</span></span>

<span data-ttu-id="48a11-138">Šajā ilustrācijā redzama uzdevumu saišu atlase dialoglodziņā **Rediģēt uzdevumu**.</span><span class="sxs-lookup"><span data-stu-id="48a11-138">The following illustration shows the selection of task links in the **Edit task** dialog box.</span></span>

![Uzdevumu saišu atlasīšana dialoglodziņā Rediģēt uzdevumu](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a><span data-ttu-id="48a11-140">Konfigurējiet POS operāciju, lai to varētu saistīt ar uzdevumu</span><span class="sxs-lookup"><span data-stu-id="48a11-140">Configure a POS operation so that it can be linked to a task</span></span>

<span data-ttu-id="48a11-141">Lai konfigurētu POS operāciju, lai to varētu saistīt ar uzdevumu, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="48a11-141">To configure a POS operation so that it can be linked to a task, follow these steps.</span></span>

1. <span data-ttu-id="48a11-142">Dodieties uz **Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS \> POS operācijas**.</span><span class="sxs-lookup"><span data-stu-id="48a11-142">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="48a11-143">Atlasiet **Rediģēt**, atrodiet POS operāciju un pēc tam atzīmējiet izvēles rūtiņu **Iespējot Task Management**.</span><span class="sxs-lookup"><span data-stu-id="48a11-143">Select **Edit**, find the POS operation, and then select the **Enable Task Management** check box for it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="48a11-144">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="48a11-144">Additional resources</span></span>

[<span data-ttu-id="48a11-145">Uzdevumu pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="48a11-145">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="48a11-146">Uzdevumu pārvaldības konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="48a11-146">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="48a11-147">Uzdevumu sarakstu piešķiršana veikaliem vai darbiniekiem</span><span class="sxs-lookup"><span data-stu-id="48a11-147">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="48a11-148">Uzdevumu pārvaldība punktā POS</span><span class="sxs-lookup"><span data-stu-id="48a11-148">Task management in POS</span></span>](task-mgmt-POS.md)
