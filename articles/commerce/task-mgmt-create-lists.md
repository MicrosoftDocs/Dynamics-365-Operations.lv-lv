---
title: Uzdevumu sarakstu izveidošana un uzdevumu pievienošana
description: Šī tēma aprakstīts, kā izveidot uzdevumu sarakstus un tiem pievienot uzdevumus programmā Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: a0e49d1eced3bb62e78c630b137a5b86121682f3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795241"
---
# <a name="create-task-lists-and-add-tasks"></a><span data-ttu-id="c834d-103">Uzdevumu sarakstu izveidošana un uzdevumu pievienošana</span><span class="sxs-lookup"><span data-stu-id="c834d-103">Create task lists and add tasks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c834d-104">Šī tēma aprakstīts, kā izveidot uzdevumu sarakstus un tiem pievienot uzdevumus programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c834d-104">This topic describes how to create task lists and add tasks to them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c834d-105">*Uzdevums* definē noteiktu darba daļu vai darbību, ko kādam jāpabeidz noteiktā termiņā vai pirms tā.</span><span class="sxs-lookup"><span data-stu-id="c834d-105">A *task* defines a specific piece of work or an action that someone must complete on or before a specified due date.</span></span> <span data-ttu-id="c834d-106">Programmā Dynamics 365 Commerce uzdevums var iekļaut detalizētas instrukcijas un informāciju par kontaktpersonu.</span><span class="sxs-lookup"><span data-stu-id="c834d-106">In Dynamics 365 Commerce, a task can include detailed instructions and information about a contact person.</span></span> <span data-ttu-id="c834d-107">Tas var ietvert arī saites uz fona darbībām, pārdošanas punktu (POS) operācijām vai vietnes lapām, lai palīdzētu uzlabot produktivitāti un nodrošinātu kontekstu, kas ir nepieciešams uzdevuma īpašniekam efektīvai uzdevuma pabeigšanai.</span><span class="sxs-lookup"><span data-stu-id="c834d-107">It can also include links to back-office operations, point of sale (POS) operations, or site pages, to help improve productivity and provide the context that the task owner requires to complete the task efficiently.</span></span>

<span data-ttu-id="c834d-108">*Uzdevumu saraksts* ir uzdevumu apkopojums, kas ir jāpabeidz kā daļa no biznesa procesa.</span><span class="sxs-lookup"><span data-stu-id="c834d-108">A *task list* is a collection of tasks that must be completed as part of a business process.</span></span> <span data-ttu-id="c834d-109">Piemēram, var būt uzdevumu saraksts, kas jaunajam darbiniekam ir jāizpilda pievienošanās laikā, uzdevumu saraksts kasieriem, kuri strādā vakara maiņas, vai uzdevumu saraksts, kas jāaizpilda, lai sagatavotu veikalu gaidāmai atvaļinājumu sezonai.</span><span class="sxs-lookup"><span data-stu-id="c834d-109">For example, there might be a task list that a new worker must complete during onboarding, a task list for cashiers who work evening shifts, or a task list that must be completed to prepare the store for an upcoming holiday season.</span></span> <span data-ttu-id="c834d-110">Programmā Commerce katram uzdevumu sarakstam, kam ir mērķa datums, var piešķirt neierobežotu skaitu veikalu vai darbinieku, un var konfigurēt tā periodiskumu.</span><span class="sxs-lookup"><span data-stu-id="c834d-110">In Commerce, every task list that has a target date can be assigned to any number of stores or employees, and it can be configured to recur.</span></span>

<span data-ttu-id="c834d-111">Gan vadītāji, gan darbinieki var izveidot uzdevumu sarakstus Commerce atbalsta birojā, un pēc tam piešķirt tos veikalu kopai.</span><span class="sxs-lookup"><span data-stu-id="c834d-111">Both managers and workers can create task lists in Commerce back office, and then assign them to a set of stores.</span></span>

## <a name="create-a-task-list"></a><span data-ttu-id="c834d-112">Izveidot uzdevumu sarakstu</span><span class="sxs-lookup"><span data-stu-id="c834d-112">Create a task list</span></span>

<span data-ttu-id="c834d-113">Lai izveidotu uzdevumu sarakstu, izpildiet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="c834d-113">To create a task list, follow these steps.</span></span>

1. <span data-ttu-id="c834d-114">Dodieties uz **Retail un Commerce \>Uzdevumu pārvaldība \>Uzdevumu pārvaldības administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="c834d-114">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="c834d-115">Atlasiet **Jauns** un pēc tam ievadiet vērtības laukos **Nosaukums**, **Apraksts** un **Īpašnieks**.</span><span class="sxs-lookup"><span data-stu-id="c834d-115">Select **New**, and then enter values in the **Name**, **Description**, and **Owner** fields.</span></span>
1. <span data-ttu-id="c834d-116">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c834d-116">Select **Save**.</span></span>

## <a name="add-tasks-to-a-task-list"></a><span data-ttu-id="c834d-117">Uzdevumu pievienošana uzdevumu sarakstam</span><span class="sxs-lookup"><span data-stu-id="c834d-117">Add tasks to a task list</span></span>

<span data-ttu-id="c834d-118">Lai uzdevumu sarakstam pievienotu uzdevumus, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="c834d-118">To add tasks to a task list, follow these steps.</span></span>
 
1. <span data-ttu-id="c834d-119">Esoša uzdevuma kopsavilkuma cilnē **Uzdevumi** atlasiet **Jauns**, lai pievienotu uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="c834d-119">On the **Tasks** FastTab of an existing task list, select **New** to add a task.</span></span>
1. <span data-ttu-id="c834d-120">Dialoglodziņā **Izveidot jaunu uzdevumu**, laukā **Nosaukums** ievadiet uzdevuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="c834d-120">In the **Create a new task** dialog box, in the **Name** field, enter a name for the task.</span></span>
1. <span data-ttu-id="c834d-121">Laukā **Izpildes datuma nobīde no mērķa datuma** ievadiet pozitīvu vai negatīvu veselu skaitli.</span><span class="sxs-lookup"><span data-stu-id="c834d-121">In the **Due data offset from target date** field, enter a positive or negative integer value.</span></span> <span data-ttu-id="c834d-122">Piemēram, ievadiet **-2**, ja uzdevums jāpabeidz divas dienas pirms uzdevumu saraksta izpildes datuma.</span><span class="sxs-lookup"><span data-stu-id="c834d-122">For example, enter **-2** if the task should be completed two days before the task list's due date.</span></span>
1. <span data-ttu-id="c834d-123">Laukā **Piezīmes** Ievadiet detalizētus norādījumus.</span><span class="sxs-lookup"><span data-stu-id="c834d-123">In the **Notes** field, enter detailed instructions.</span></span>
1. <span data-ttu-id="c834d-124">Laukā **Kontaktpersona** ievadiet tēmas eksperta vārdu, ar kuru uzdevuma īpašnieks var sazināties, ja viņam ir nepieciešama palīdzība.</span><span class="sxs-lookup"><span data-stu-id="c834d-124">In the **Contact person** field, enter the name of a subject matter expert that the task owner can contact if he or she needs help.</span></span>
1. <span data-ttu-id="c834d-125">Laukā **Uzdevuma saite** ievadiet saiti, pamatojoties uz uzdevuma iedabu.</span><span class="sxs-lookup"><span data-stu-id="c834d-125">In the **Task link** field, enter a link, based on the nature of the task.</span></span>

> [!TIP]
> <span data-ttu-id="c834d-126">Lai gan varat izmantot lauku **Piešķirts**, lai piešķirtu uzdevumus kādam, kamēr veidojat uzdevumu sarakstu, mēs iesakām izvairīties no uzdevumu piešķiršanas uzdevumu saraksta izveides laikā.</span><span class="sxs-lookup"><span data-stu-id="c834d-126">Although you can use the **Assigned to** field to assign tasks to someone while you're creating a task list, we recommend that you avoid assigning tasks during task list creation.</span></span> <span data-ttu-id="c834d-127">Tā vietā piešķiriet uzdevumus pēc tam, kas atsevišķu veikalu sarakstam ir izveidota instance.</span><span class="sxs-lookup"><span data-stu-id="c834d-127">Instead, assign the tasks after the list is instantiated for individual stores.</span></span>

## <a name="use-task-links-to-help-improve-worker-productivity"></a><span data-ttu-id="c834d-128">Izmantojiet uzdevumu saites, lai uzlabotu darbinieku produktivitāti</span><span class="sxs-lookup"><span data-stu-id="c834d-128">Use task links to help improve worker productivity</span></span>

<span data-ttu-id="c834d-129">Commerce ļauj saistīt uzdevumus ar konkrētām POS operācijām, piemēram, palaižot pārdošanas pārskatu, apskatot tiešsaistes mācību videoklipu jaunai darbinieka orientācijai vai veicot darbību operāciju uzskaites daļā.</span><span class="sxs-lookup"><span data-stu-id="c834d-129">Commerce lets you link tasks to specific POS operations, such as running a sales report, viewing an online training video for new employee orientation, or performing a back-office operation.</span></span> <span data-ttu-id="c834d-130">Šis līdzeklis palīdz uzdevumu īpašniekiem iegūt informāciju, kas nepieciešama efektīvai uzdevuma izpildei.</span><span class="sxs-lookup"><span data-stu-id="c834d-130">This feature helps task owners get the information that they need to complete a task efficiently.</span></span>

<span data-ttu-id="c834d-131">Lai, veidojot uzdevumu, pievienotu uzdevumu saites, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="c834d-131">To add task links while you create a task, follow these steps.</span></span>

1. <span data-ttu-id="c834d-132">Esoša uzdevuma kopsavilkuma cilnē **Uzdevumi** atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="c834d-132">On the **Tasks** FastTab of an existing task list, select **Edit**.</span></span>
1. <span data-ttu-id="c834d-133">Dialoglodziņā **Rediģēt uzdevumu** laukā **Uzdevuma saite** atlasiet vienu vai vairākas no šīm opcijām:</span><span class="sxs-lookup"><span data-stu-id="c834d-133">In the **Edit task** dialog box, in the **Task link** field, select one or more of the following options:</span></span>

    - <span data-ttu-id="c834d-134">Atlasiet **Izvēlnes elements**, lai konfigurētu operāciju uzskaites daļas darbību, piemēram "Preču komplekti."</span><span class="sxs-lookup"><span data-stu-id="c834d-134">Select **Menu item** to configure a back-office operation, such as "Product kits."</span></span>
    - <span data-ttu-id="c834d-135">Atlasiet **POS operācija**, lai konfigurētu POS operāciju, piemēram, "Pārdošanas pārskati."</span><span class="sxs-lookup"><span data-stu-id="c834d-135">Select **POS Operation** to configure a POS operation, such as "Sales reports."</span></span>
    - <span data-ttu-id="c834d-136">Atlasiet **URL**, lai konfigurētu absolūto vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="c834d-136">Select **URL** to configure an absolute URL.</span></span>

<span data-ttu-id="c834d-137">Šajā ilustrācijā redzama uzdevumu saišu atlase dialoglodziņā **Rediģēt uzdevumu**.</span><span class="sxs-lookup"><span data-stu-id="c834d-137">The following illustration shows the selection of task links in the **Edit task** dialog box.</span></span>

![Uzdevumu saišu atlasīšana dialoglodziņā Rediģēt uzdevumu](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a><span data-ttu-id="c834d-139">Konfigurējiet POS operāciju, lai to varētu saistīt ar uzdevumu</span><span class="sxs-lookup"><span data-stu-id="c834d-139">Configure a POS operation so that it can be linked to a task</span></span>

<span data-ttu-id="c834d-140">Lai konfigurētu POS operāciju, lai to varētu saistīt ar uzdevumu, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="c834d-140">To configure a POS operation so that it can be linked to a task, follow these steps.</span></span>

1. <span data-ttu-id="c834d-141">Dodieties uz **Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS \> POS operācijas**.</span><span class="sxs-lookup"><span data-stu-id="c834d-141">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="c834d-142">Atlasiet **Rediģēt**, atrodiet POS operāciju un pēc tam atzīmējiet izvēles rūtiņu **Iespējot Task Management**.</span><span class="sxs-lookup"><span data-stu-id="c834d-142">Select **Edit**, find the POS operation, and then select the **Enable Task Management** check box for it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c834d-143">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="c834d-143">Additional resources</span></span>

[<span data-ttu-id="c834d-144">Uzdevumu pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="c834d-144">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="c834d-145">Uzdevumu pārvaldības konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="c834d-145">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="c834d-146">Uzdevumu sarakstu piešķiršana veikaliem vai darbiniekiem</span><span class="sxs-lookup"><span data-stu-id="c834d-146">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="c834d-147">Uzdevumu pārvaldība punktā POS</span><span class="sxs-lookup"><span data-stu-id="c834d-147">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
