---
title: Uzdevumu pārvaldības konfigurēšana
description: Šajā tēmā ir aprakstīts, kā konfigurēt uzdevumu pārvaldības līdzekļus sistēmā Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 9a4775c2dba2b9aa8e671ab6c246000303b3a37e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414115"
---
# <a name="configure-task-management"></a><span data-ttu-id="b2b17-103">Uzdevumu pārvaldības konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="b2b17-103">Configure task management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b2b17-104">Šajā tēmā ir aprakstīts, kā konfigurēt uzdevumu pārvaldības līdzekļus sistēmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b2b17-104">This topic describes how to configure task management features in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b2b17-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="b2b17-105">Overview</span></span>

<span data-ttu-id="b2b17-106">Pirms Dynamics 365 Commerce vadītāji un nodarbinātie var lietot uzdevumu pārvaldības līdzekļus pakalpojumā Commerce, ir jākonfigurē uzdevumu pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="b2b17-106">Before Dynamics 365 Commerce managers and employees can use the task management features in Commerce, task management must be configured.</span></span> <span data-ttu-id="b2b17-107">Konfigurēšanas darbības ietver atļauju piešķiršanu vadītājiem un darbiniekiem, izplatot atļaujas pārdošanas punkta (POS) klientiem, iestatot POS paziņojumus un konfigurējot elementu **Uzdevumi** POS programmas sākumlapā.</span><span class="sxs-lookup"><span data-stu-id="b2b17-107">Configuration steps include granting permissions to managers and employees, distributing permissions to point of sale (POS) clients, setting up POS notifications, and configuring the **Tasks** tile on the home page of a POS application.</span></span>

## <a name="configure-permissions-for-store-managers"></a><span data-ttu-id="b2b17-108">Atļauju konfigurēšana veikalu vadītājiem</span><span class="sxs-lookup"><span data-stu-id="b2b17-108">Configure permissions for store managers</span></span>

<span data-ttu-id="b2b17-109">Katrs nodarbinātais konkrētajā veikalā var skatīt visus uzdevumus, kas piešķirti attiecīgajam veikalam.</span><span class="sxs-lookup"><span data-stu-id="b2b17-109">Every worker in a given store can view all tasks that are assigned to that store.</span></span> <span data-ttu-id="b2b17-110">Viņi var arī atjaunināt sev piešķirto uzdevumu statusu.</span><span class="sxs-lookup"><span data-stu-id="b2b17-110">They can also update the status of the tasks that are assigned to them.</span></span> <span data-ttu-id="b2b17-111">Tomēr personām, piemēram, veikala vadītājiem ir jābūt uzdevumu pārvaldības atļaujām, lai pārvaldītu veikalā piešķirtos uzdevumus un izveidotu viena mērķa uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="b2b17-111">However, personas such as store managers must have task management permissions to manage tasks that are assigned to the store and to create single-purpose tasks.</span></span>

<span data-ttu-id="b2b17-112">Lai konfigurētu uzdevumu pārvaldības atļaujas veikala pārvaldniekiem, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="b2b17-112">To configure task management permissions for store managers, follow these steps.</span></span>

1. <span data-ttu-id="b2b17-113">Dodieties uz **Retail un Commerce \> Nodarbinātie \> Atļauju grupas**.</span><span class="sxs-lookup"><span data-stu-id="b2b17-113">Go to **Retail and Commerce \> Employees \> Permission groups**.</span></span>
1. <span data-ttu-id="b2b17-114">Atlasiet īpašu atļauju grupu (piemēram, **Vadītājs**) un pēc tam atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="b2b17-114">Select a specific permission group (for example, **Manager**), and then select **Edit**.</span></span>
1. <span data-ttu-id="b2b17-115">Kopsavilkuma cilnē **Atļaujas** iestatiet opciju **Atļaut uzdevumu pārvaldību** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="b2b17-115">On the **Permissions** FastTab, set the **Allow task management** option to **Yes**.</span></span>
1. <span data-ttu-id="b2b17-116">Kopsavilkuma cilnē **Paziņojumi** pievienojiet operāciju **Uzdevumu pārvaldība** un ievadiet vērtību laukā **Parādīt pasūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="b2b17-116">On the **Notifications** FastTab, add the **Task management** operation, and enter a value in the **Display order** field.</span></span> <span data-ttu-id="b2b17-117">Piemēram, ievadiet **2**, ja **Pasūtījuma izpildes** operācijai jau ir **Parādīt pasūtījumu** vērtība **1**.</span><span class="sxs-lookup"><span data-stu-id="b2b17-117">For example, enter **2** if the **Order fulfillment** operation already has a **Display order** value of **1**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="b2b17-118">Ja personai, kas nav vadītāja persona, ir jābūt uzdevumu pārvaldības atļaujām POS, varat piešķirt atļauju indivīdam.</span><span class="sxs-lookup"><span data-stu-id="b2b17-118">If a non-manager persona must have task management permissions in the POS, you can grant permission to the individual.</span></span> <span data-ttu-id="b2b17-119">Varat arī izveidot jaunu atļauju grupu, kas nav pārvaldītāji, un iestatīt opciju **Atļaut uzdevumu pārvaldību** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="b2b17-119">Alternatively, you can create a new permission group for non-managers and set the **Allow task management** option to **Yes**.</span></span>

<span data-ttu-id="b2b17-120">Šajā attēlā parādīts, kā konfigurēt uzdevumu pārvaldības atļaujas veikala pārvaldniekiem.</span><span class="sxs-lookup"><span data-stu-id="b2b17-120">The following illustration shows how to configure task management permissions for store managers.</span></span>

![Uzdevumu pārvaldības atļauju konfigurēšana veikala vadītājiem](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a><span data-ttu-id="b2b17-122">Atļauju konfigurēšana nodarbinātajiem</span><span class="sxs-lookup"><span data-stu-id="b2b17-122">Configure permissions for employees</span></span>

<span data-ttu-id="b2b17-123">Darbiniekiem ir jābūt atļaujām izveidot uzdevumu sarakstus, pārvaldīt piešķires kritērijus un konfigurēt jebkuru uzdevumu saraksta periodiskumu.</span><span class="sxs-lookup"><span data-stu-id="b2b17-123">Employees must have permissions to create task lists, manage assignment criteria, and configure the recurrence of any task list.</span></span> <span data-ttu-id="b2b17-124">Lai konfigurētu šīs atļaujas, piešķiriet nodarbinātos lomai **Mazumtirdzniecības uzdevumu pārvaldnieks**.</span><span class="sxs-lookup"><span data-stu-id="b2b17-124">To configure these permissions, you assign employees to the **Retail task manager** role.</span></span>

<span data-ttu-id="b2b17-125">Lai konfigurētu atļaujas nodarbinātajam, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="b2b17-125">To configure permissions for an employee, follow these steps.</span></span>

1. <span data-ttu-id="b2b17-126">Dodieties uz **Retail un Commerce \> Nodarbinātie \> Lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="b2b17-126">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="b2b17-127">Atlasiet darbinieku.</span><span class="sxs-lookup"><span data-stu-id="b2b17-127">Select an employee.</span></span>
1. <span data-ttu-id="b2b17-128">Kopsavilkuma cilnē **Lietotāja lomas** atlasiet **Piešķirt lomas**.</span><span class="sxs-lookup"><span data-stu-id="b2b17-128">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="b2b17-129">Dialoglodziņā lomu **Piešķirt lomas lietotājam** atlasiet lomu **Mazumtirdzniecības uzdevumu vadītājs** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b2b17-129">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

## <a name="distribute-permissions-to-pos-clients"></a><span data-ttu-id="b2b17-130">Sadalīt atļaujas POS klientiem</span><span class="sxs-lookup"><span data-stu-id="b2b17-130">Distribute permissions to POS clients</span></span>

<span data-ttu-id="b2b17-131">Pirms nodarbinātie var izmantot POS klientus, atļaujas ir jāsadala un jāsinhronizē ar šiem klientiem.</span><span class="sxs-lookup"><span data-stu-id="b2b17-131">Before employees can use POS clients, permissions must be distributed and synced to those clients.</span></span>

<span data-ttu-id="b2b17-132">Lai sadalītu atļaujas POS klientiem, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="b2b17-132">To distribute permissions to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="b2b17-133">Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**.</span><span class="sxs-lookup"><span data-stu-id="b2b17-133">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="b2b17-134">Atlasiet **1060** (**Personāla**) sadales grafiku un pēc tam atlasiet **Palaist tagad**.</span><span class="sxs-lookup"><span data-stu-id="b2b17-134">Select the **1060** (**Staff**) distribution schedule, and then select **Run now**.</span></span>
1. <span data-ttu-id="b2b17-135">Atlasiet **1070** (**Kanāla konfigurācijas**) sadales grafiku un pēc tam atlasiet **Palaist tagad**.</span><span class="sxs-lookup"><span data-stu-id="b2b17-135">Select the **1070** (**Channel configuration**) distribution schedule, and then select **Run now**.</span></span>

## <a name="configure-pos-notifications-for-tasks"></a><span data-ttu-id="b2b17-136">POS paziņojumu konfigurēšana uzdevumiem</span><span class="sxs-lookup"><span data-stu-id="b2b17-136">Configure POS notifications for tasks</span></span>

<span data-ttu-id="b2b17-137">Uzdevumu pārvaldība ir jākonfigurē tā, lai paziņojumi ir pieejami POS programmā.</span><span class="sxs-lookup"><span data-stu-id="b2b17-137">Task management must be configured so that notifications are available in the POS application.</span></span>

<span data-ttu-id="b2b17-138">Lai konfigurētu POS paziņojumus uzdevumiem, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="b2b17-138">To configure POS notifications for tasks, follow these steps.</span></span>

1. <span data-ttu-id="b2b17-139">Dodieties uz **Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS \> POS operācijas**.</span><span class="sxs-lookup"><span data-stu-id="b2b17-139">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="b2b17-140">Atrodiet operāciju **1400** (**Uzdevumu pārvaldība**) un tam atlasiet izvēles rūtiņu **Iespējot paziņojumus**.</span><span class="sxs-lookup"><span data-stu-id="b2b17-140">Find operation **1400** (**Task management**), and select the **Enable notifications** check box for it.</span></span>

<span data-ttu-id="b2b17-141">Šajā attēlā redzama operācija **Uzdevumu pārvaldība** lapā **POS operācijas**.</span><span class="sxs-lookup"><span data-stu-id="b2b17-141">The following illustration shows the **Task management** operation on the **POS operations** page.</span></span>

![Uzdevumu pārvaldības operācija POS operāciju lapā](media/HQ-POS-Tasks-Notifications.png)

<span data-ttu-id="b2b17-143">Plašāku informāciju par to, kā konfigurēt POS paziņojumus, skatiet sadaļā [Pasūtījuma paziņojumu rādīšana pārdošanas punktā (POS)](notifications-pos.md).</span><span class="sxs-lookup"><span data-stu-id="b2b17-143">For more information about how to configure POS notifications, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a><span data-ttu-id="b2b17-144">Konfigurēt uzdevumu elementu POS programmas sākumlapā</span><span class="sxs-lookup"><span data-stu-id="b2b17-144">Configure the Tasks tile on a POS application home page</span></span>

<span data-ttu-id="b2b17-145">Pirms konfigurējat **Uzdevumu** elementu, kas atrodas POS programmas sākumlapā, skatiet sadaļu [Ekrāna izkārtojumi pārdošanas punktam (POS)](pos-screen-layouts.md), lai iegūtu informāciju par to, kā konfigurēt un pievienot jaunas pogas POS ekrāna izkārtojumam.</span><span class="sxs-lookup"><span data-stu-id="b2b17-145">Before you configure the **Tasks** tile on the home page of a POS application, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information about how to configure and add new buttons to a POS screen layout.</span></span>

<span data-ttu-id="b2b17-146">Lai konfigurētu elementu **Uzdevumi** POS programmas sākumlapā, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="b2b17-146">To configure the **Tasks** tile on a POS application home page, follow these steps.</span></span>

1. <span data-ttu-id="b2b17-147">Dodieties uz **Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS \> Ekrāna izkārtojumi**.</span><span class="sxs-lookup"><span data-stu-id="b2b17-147">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> Screen layouts**.</span></span>
1. <span data-ttu-id="b2b17-148">Atlasiet ekrāna izkārtojumu, izvēlieties izkārtojuma lielumu un atlasiet pogu režģi.</span><span class="sxs-lookup"><span data-stu-id="b2b17-148">Select a screen layout, select a layout size, and select a button grid.</span></span>
1. <span data-ttu-id="b2b17-149">Kopsavilkuma cilnē **Pogu režģi** atlasiet **Noformētājs**, lai rediģētu atlasīto pogu režģi.</span><span class="sxs-lookup"><span data-stu-id="b2b17-149">On the **Button grids** FastTab, select **Designer** to edit the selected button grid.</span></span>
1. <span data-ttu-id="b2b17-150">Pievienojiet elementu **Uzdevumi** atbilstošajai sākumlapas sadaļai.</span><span class="sxs-lookup"><span data-stu-id="b2b17-150">Add a **Tasks** tile to the appropriate section of the home page.</span></span>

<span data-ttu-id="b2b17-151">Šajā attēlā parādīts elementa **Uzdevumi** piemērs POS sākumlapā.</span><span class="sxs-lookup"><span data-stu-id="b2b17-151">The following illustration shows an example of a **Tasks** tile on a POS home page.</span></span>

![Uzdevumu elements POS sākumlapā](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a><span data-ttu-id="b2b17-153">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="b2b17-153">Additional resources</span></span>

[<span data-ttu-id="b2b17-154">Uzdevumu pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="b2b17-154">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="b2b17-155">Uzdevumu sarakstu izveidošana un uzdevumu pievienošana</span><span class="sxs-lookup"><span data-stu-id="b2b17-155">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="b2b17-156">Uzdevumu sarakstu piešķiršana veikaliem vai darbiniekiem</span><span class="sxs-lookup"><span data-stu-id="b2b17-156">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="b2b17-157">Uzdevumu pārvaldība punktā POS</span><span class="sxs-lookup"><span data-stu-id="b2b17-157">Task management in POS</span></span>](task-mgmt-POS.md)
