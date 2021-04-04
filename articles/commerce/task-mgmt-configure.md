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
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: ba2283bbfa2fdce75d3fbef6fcff47dd872c7998
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478048"
---
# <a name="configure-task-management"></a><span data-ttu-id="70867-103">Uzdevumu pārvaldības konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="70867-103">Configure task management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="70867-104">Šajā tēmā ir aprakstīts, kā konfigurēt uzdevumu pārvaldības līdzekļus sistēmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="70867-104">This topic describes how to configure task management features in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="70867-105">Pirms Dynamics 365 Commerce vadītāji un nodarbinātie var lietot uzdevumu pārvaldības līdzekļus pakalpojumā Commerce, ir jākonfigurē uzdevumu pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="70867-105">Before Dynamics 365 Commerce managers and employees can use the task management features in Commerce, task management must be configured.</span></span> <span data-ttu-id="70867-106">Konfigurēšanas darbības ietver atļauju piešķiršanu vadītājiem un darbiniekiem, izplatot atļaujas pārdošanas punkta (POS) klientiem, iestatot POS paziņojumus un konfigurējot elementu **Uzdevumi** POS programmas sākumlapā.</span><span class="sxs-lookup"><span data-stu-id="70867-106">Configuration steps include granting permissions to managers and employees, distributing permissions to point of sale (POS) clients, setting up POS notifications, and configuring the **Tasks** tile on the home page of a POS application.</span></span>

## <a name="configure-permissions-for-store-managers"></a><span data-ttu-id="70867-107">Atļauju konfigurēšana veikalu vadītājiem</span><span class="sxs-lookup"><span data-stu-id="70867-107">Configure permissions for store managers</span></span>

<span data-ttu-id="70867-108">Katrs nodarbinātais konkrētajā veikalā var skatīt visus uzdevumus, kas piešķirti attiecīgajam veikalam.</span><span class="sxs-lookup"><span data-stu-id="70867-108">Every worker in a given store can view all tasks that are assigned to that store.</span></span> <span data-ttu-id="70867-109">Viņi var arī atjaunināt sev piešķirto uzdevumu statusu.</span><span class="sxs-lookup"><span data-stu-id="70867-109">They can also update the status of the tasks that are assigned to them.</span></span> <span data-ttu-id="70867-110">Tomēr personām, piemēram, veikala vadītājiem ir jābūt uzdevumu pārvaldības atļaujām, lai pārvaldītu veikalā piešķirtos uzdevumus un izveidotu viena mērķa uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="70867-110">However, personas such as store managers must have task management permissions to manage tasks that are assigned to the store and to create single-purpose tasks.</span></span>

<span data-ttu-id="70867-111">Lai konfigurētu uzdevumu pārvaldības atļaujas veikala pārvaldniekiem, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="70867-111">To configure task management permissions for store managers, follow these steps.</span></span>

1. <span data-ttu-id="70867-112">Dodieties uz **Retail un Commerce \> Nodarbinātie \> Atļauju grupas**.</span><span class="sxs-lookup"><span data-stu-id="70867-112">Go to **Retail and Commerce \> Employees \> Permission groups**.</span></span>
1. <span data-ttu-id="70867-113">Atlasiet īpašu atļauju grupu (piemēram, **Vadītājs**) un pēc tam atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="70867-113">Select a specific permission group (for example, **Manager**), and then select **Edit**.</span></span>
1. <span data-ttu-id="70867-114">Kopsavilkuma cilnē **Atļaujas** iestatiet opciju **Atļaut uzdevumu pārvaldību** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="70867-114">On the **Permissions** FastTab, set the **Allow task management** option to **Yes**.</span></span>
1. <span data-ttu-id="70867-115">Kopsavilkuma cilnē **Paziņojumi** pievienojiet operāciju **Uzdevumu pārvaldība** un ievadiet vērtību laukā **Parādīt pasūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="70867-115">On the **Notifications** FastTab, add the **Task management** operation, and enter a value in the **Display order** field.</span></span> <span data-ttu-id="70867-116">Piemēram, ievadiet **2**, ja **Pasūtījuma izpildes** operācijai jau ir **Parādīt pasūtījumu** vērtība **1**.</span><span class="sxs-lookup"><span data-stu-id="70867-116">For example, enter **2** if the **Order fulfillment** operation already has a **Display order** value of **1**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="70867-117">Ja personai, kas nav vadītāja persona, ir jābūt uzdevumu pārvaldības atļaujām POS, varat piešķirt atļauju indivīdam.</span><span class="sxs-lookup"><span data-stu-id="70867-117">If a non-manager persona must have task management permissions in the POS, you can grant permission to the individual.</span></span> <span data-ttu-id="70867-118">Varat arī izveidot jaunu atļauju grupu, kas nav pārvaldītāji, un iestatīt opciju **Atļaut uzdevumu pārvaldību** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="70867-118">Alternatively, you can create a new permission group for non-managers and set the **Allow task management** option to **Yes**.</span></span>

<span data-ttu-id="70867-119">Šajā attēlā parādīts, kā konfigurēt uzdevumu pārvaldības atļaujas veikala pārvaldniekiem.</span><span class="sxs-lookup"><span data-stu-id="70867-119">The following illustration shows how to configure task management permissions for store managers.</span></span>

![Uzdevumu pārvaldības atļauju konfigurēšana veikala vadītājiem](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a><span data-ttu-id="70867-121">Atļauju konfigurēšana nodarbinātajiem</span><span class="sxs-lookup"><span data-stu-id="70867-121">Configure permissions for employees</span></span>

<span data-ttu-id="70867-122">Darbiniekiem ir jābūt atļaujām izveidot uzdevumu sarakstus, pārvaldīt piešķires kritērijus un konfigurēt jebkuru uzdevumu saraksta periodiskumu.</span><span class="sxs-lookup"><span data-stu-id="70867-122">Employees must have permissions to create task lists, manage assignment criteria, and configure the recurrence of any task list.</span></span> <span data-ttu-id="70867-123">Lai konfigurētu šīs atļaujas, piešķiriet nodarbinātos lomai **Mazumtirdzniecības uzdevumu pārvaldnieks**.</span><span class="sxs-lookup"><span data-stu-id="70867-123">To configure these permissions, you assign employees to the **Retail task manager** role.</span></span>

<span data-ttu-id="70867-124">Lai konfigurētu atļaujas nodarbinātajam, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="70867-124">To configure permissions for an employee, follow these steps.</span></span>

1. <span data-ttu-id="70867-125">Dodieties uz **Retail un Commerce \> Nodarbinātie \> Lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="70867-125">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="70867-126">Atlasiet darbinieku.</span><span class="sxs-lookup"><span data-stu-id="70867-126">Select an employee.</span></span>
1. <span data-ttu-id="70867-127">Kopsavilkuma cilnē **Lietotāja lomas** atlasiet **Piešķirt lomas**.</span><span class="sxs-lookup"><span data-stu-id="70867-127">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="70867-128">Dialoglodziņā lomu **Piešķirt lomas lietotājam** atlasiet lomu **Mazumtirdzniecības uzdevumu vadītājs** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="70867-128">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

## <a name="distribute-permissions-to-pos-clients"></a><span data-ttu-id="70867-129">Sadalīt atļaujas POS klientiem</span><span class="sxs-lookup"><span data-stu-id="70867-129">Distribute permissions to POS clients</span></span>

<span data-ttu-id="70867-130">Pirms nodarbinātie var izmantot POS klientus, atļaujas ir jāsadala un jāsinhronizē ar šiem klientiem.</span><span class="sxs-lookup"><span data-stu-id="70867-130">Before employees can use POS clients, permissions must be distributed and synced to those clients.</span></span>

<span data-ttu-id="70867-131">Lai sadalītu atļaujas POS klientiem, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="70867-131">To distribute permissions to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="70867-132">Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**.</span><span class="sxs-lookup"><span data-stu-id="70867-132">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="70867-133">Atlasiet **1060** (**Personāla**) sadales grafiku un pēc tam atlasiet **Palaist tagad**.</span><span class="sxs-lookup"><span data-stu-id="70867-133">Select the **1060** (**Staff**) distribution schedule, and then select **Run now**.</span></span>
1. <span data-ttu-id="70867-134">Atlasiet **1070** (**Kanāla konfigurācijas**) sadales grafiku un pēc tam atlasiet **Palaist tagad**.</span><span class="sxs-lookup"><span data-stu-id="70867-134">Select the **1070** (**Channel configuration**) distribution schedule, and then select **Run now**.</span></span>

## <a name="configure-pos-notifications-for-tasks"></a><span data-ttu-id="70867-135">POS paziņojumu konfigurēšana uzdevumiem</span><span class="sxs-lookup"><span data-stu-id="70867-135">Configure POS notifications for tasks</span></span>

<span data-ttu-id="70867-136">Uzdevumu pārvaldība ir jākonfigurē tā, lai paziņojumi ir pieejami POS programmā.</span><span class="sxs-lookup"><span data-stu-id="70867-136">Task management must be configured so that notifications are available in the POS application.</span></span>

<span data-ttu-id="70867-137">Lai konfigurētu POS paziņojumus uzdevumiem, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="70867-137">To configure POS notifications for tasks, follow these steps.</span></span>

1. <span data-ttu-id="70867-138">Dodieties uz **Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS \> POS operācijas**.</span><span class="sxs-lookup"><span data-stu-id="70867-138">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="70867-139">Atrodiet operāciju **1400** (**Uzdevumu pārvaldība**) un tam atlasiet izvēles rūtiņu **Iespējot paziņojumus**.</span><span class="sxs-lookup"><span data-stu-id="70867-139">Find operation **1400** (**Task management**), and select the **Enable notifications** check box for it.</span></span>

<span data-ttu-id="70867-140">Šajā attēlā redzama operācija **Uzdevumu pārvaldība** lapā **POS operācijas**.</span><span class="sxs-lookup"><span data-stu-id="70867-140">The following illustration shows the **Task management** operation on the **POS operations** page.</span></span>

![Uzdevumu pārvaldības operācija POS operāciju lapā](media/HQ-POS-Tasks-Notifications.png)

<span data-ttu-id="70867-142">Plašāku informāciju par to, kā konfigurēt POS paziņojumus, skatiet sadaļā [Pasūtījuma paziņojumu rādīšana pārdošanas punktā (POS)](notifications-pos.md).</span><span class="sxs-lookup"><span data-stu-id="70867-142">For more information about how to configure POS notifications, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a><span data-ttu-id="70867-143">Konfigurēt uzdevumu elementu POS programmas sākumlapā</span><span class="sxs-lookup"><span data-stu-id="70867-143">Configure the Tasks tile on a POS application home page</span></span>

<span data-ttu-id="70867-144">Pirms konfigurējat **Uzdevumu** elementu, kas atrodas POS programmas sākumlapā, skatiet sadaļu [Ekrāna izkārtojumi pārdošanas punktam (POS)](pos-screen-layouts.md), lai iegūtu informāciju par to, kā konfigurēt un pievienot jaunas pogas POS ekrāna izkārtojumam.</span><span class="sxs-lookup"><span data-stu-id="70867-144">Before you configure the **Tasks** tile on the home page of a POS application, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information about how to configure and add new buttons to a POS screen layout.</span></span>

<span data-ttu-id="70867-145">Lai konfigurētu elementu **Uzdevumi** POS programmas sākumlapā, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="70867-145">To configure the **Tasks** tile on a POS application home page, follow these steps.</span></span>

1. <span data-ttu-id="70867-146">Dodieties uz **Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS \> Ekrāna izkārtojumi**.</span><span class="sxs-lookup"><span data-stu-id="70867-146">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> Screen layouts**.</span></span>
1. <span data-ttu-id="70867-147">Atlasiet ekrāna izkārtojumu, izvēlieties izkārtojuma lielumu un atlasiet pogu režģi.</span><span class="sxs-lookup"><span data-stu-id="70867-147">Select a screen layout, select a layout size, and select a button grid.</span></span>
1. <span data-ttu-id="70867-148">Kopsavilkuma cilnē **Pogu režģi** atlasiet **Noformētājs**, lai rediģētu atlasīto pogu režģi.</span><span class="sxs-lookup"><span data-stu-id="70867-148">On the **Button grids** FastTab, select **Designer** to edit the selected button grid.</span></span>
1. <span data-ttu-id="70867-149">Pievienojiet elementu **Uzdevumi** atbilstošajai sākumlapas sadaļai.</span><span class="sxs-lookup"><span data-stu-id="70867-149">Add a **Tasks** tile to the appropriate section of the home page.</span></span>

<span data-ttu-id="70867-150">Šajā attēlā parādīts elementa **Uzdevumi** piemērs POS sākumlapā.</span><span class="sxs-lookup"><span data-stu-id="70867-150">The following illustration shows an example of a **Tasks** tile on a POS home page.</span></span>

![Uzdevumu elements POS sākumlapā](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a><span data-ttu-id="70867-152">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="70867-152">Additional resources</span></span>

[<span data-ttu-id="70867-153">Uzdevumu pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="70867-153">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="70867-154">Uzdevumu sarakstu izveidošana un uzdevumu pievienošana</span><span class="sxs-lookup"><span data-stu-id="70867-154">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="70867-155">Uzdevumu sarakstu piešķiršana veikaliem vai darbiniekiem</span><span class="sxs-lookup"><span data-stu-id="70867-155">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="70867-156">Uzdevumu pārvaldība punktā POS</span><span class="sxs-lookup"><span data-stu-id="70867-156">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
