---
title: Uzdevumu sarakstu piešķiršana veikaliem vai darbiniekiem
description: Šajā tēmā aprakstīts, kā piešķirt uzdevumu sarakstus veikaliem vai darbiniekiem programmā Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0c4f028367c894c54392963ffc4f6a0f0c04c03a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795265"
---
# <a name="assign-task-lists-to-stores-or-employees"></a><span data-ttu-id="6136d-103">Uzdevumu sarakstu piešķiršana veikaliem vai darbiniekiem</span><span class="sxs-lookup"><span data-stu-id="6136d-103">Assign task lists to stores or employees</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6136d-104">Šajā tēmā aprakstīts, kā piešķirt uzdevumu sarakstus veikaliem vai darbiniekiem programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6136d-104">This topic describes how to assign task lists to stores or employees in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6136d-105">Uzdevumu pārvaldība programmā Dynamics 365 Commerce ļauj piešķirt uzdevumu sarakstu vairākiem veikaliem vai darbiniekiem vai arī veikalu un darbinieku kombinācijai.</span><span class="sxs-lookup"><span data-stu-id="6136d-105">Task management in Dynamics 365 Commerce lets you assign a task list to multiple stores or employees, or to a combination of stores and employees.</span></span> <span data-ttu-id="6136d-106">Piemēram, reģionālais vadītājs 20 veikaliem varētu vēlēties piešķirt uzdevumu sarakstu **Gatavošanās atvaļinājumu sezonai** visiem 20 veikaliem.</span><span class="sxs-lookup"><span data-stu-id="6136d-106">For example, a regional manager for 20 stores might want to assign the **Holiday season preparation** task list to all 20 stores.</span></span>

## <a name="start-the-task-list-assignment-process"></a><span data-ttu-id="6136d-107">Sākt uzdevumu saraksta piešķires procesu</span><span class="sxs-lookup"><span data-stu-id="6136d-107">Start the task list assignment process</span></span>

<span data-ttu-id="6136d-108">Lai sāktu uzdevumu saraksta piešķiršanu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="6136d-108">To start the process of assigning a task list, follow these steps.</span></span>

1. <span data-ttu-id="6136d-109">Dodieties uz **Mazumtirdzniecība un komercija \> Uzdevumu pārvaldība \> Uzdevumu pārvaldības administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="6136d-109">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="6136d-110">Atlasiet uzdevumu sarakstu, ko piešķirt.</span><span class="sxs-lookup"><span data-stu-id="6136d-110">Select the task list to assign.</span></span>
1. <span data-ttu-id="6136d-111">Atlasiet **Uzsākt procesu**.</span><span class="sxs-lookup"><span data-stu-id="6136d-111">Select **Start process**.</span></span>
1. <span data-ttu-id="6136d-112">Dialoglodziņa **Uzsākt procesu** cilnē **Vispārīgi**, laukā **Procesa nosaukums** ievadiet nosaukumu (piemēram, **Austrumu apgabala veikali**).</span><span class="sxs-lookup"><span data-stu-id="6136d-112">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name (for example, **East region stores**).</span></span>
1. <span data-ttu-id="6136d-113">Laukā **Mērķa datums** konkretizējiet datumu.</span><span class="sxs-lookup"><span data-stu-id="6136d-113">In the **Target date** field, specify a date.</span></span>
1. <span data-ttu-id="6136d-114">Lai uzdevumu sarakstu piešķirtu veikaliem, cilnē **Veikali** izmantojiet **Organizācijas hierarhijas** filtru, lai atrastu un atlasītu veikalus.</span><span class="sxs-lookup"><span data-stu-id="6136d-114">To assign the task list to stores, on the **Stores** tab, use the **Organization hierarchy** filter to find and select the stores.</span></span>

    <span data-ttu-id="6136d-115">Lai piešķirtu uzdevumu sarakstu darbiniekiem, cilnē **Darbinieki** meklējiet un atlasiet darbiniekus.</span><span class="sxs-lookup"><span data-stu-id="6136d-115">To assign the task list to employees, on the **Workers** tab, find and select the employees.</span></span>

1. <span data-ttu-id="6136d-116">Atlasiet **Labi**, lai sāktu procesu.</span><span class="sxs-lookup"><span data-stu-id="6136d-116">Select **OK** to start the process.</span></span> <span data-ttu-id="6136d-117">Uzdevumu saraksts ir piešķirts atlasītajiem veikaliem vai darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="6136d-117">The tasks list is assigned to the selected stores or employees.</span></span>

<span data-ttu-id="6136d-118">Šajā attēlā parādīts piemērs, kā atrast un atlasīt veikalus dialoglodziņā **Uzsākt procesu**.</span><span class="sxs-lookup"><span data-stu-id="6136d-118">The following illustration shows an example of how to find and select stores in the **Start process** dialog box.</span></span>

![Veikalu atrašana un atlasīšana procesa uzsākšanas dialoglodziņā](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a><span data-ttu-id="6136d-120">Uzdevumu sarakstu periodiska piešķiršana</span><span class="sxs-lookup"><span data-stu-id="6136d-120">Assign task lists on a recurring basis</span></span>

<span data-ttu-id="6136d-121">Mazumtirgotājam reizēm ir periodiski uzdevumi, piemēram, "Ceturtdienas slēgšanas kontrolsaraksts" vai "Mēneša pirmā dienas kontrolsaraksts".</span><span class="sxs-lookup"><span data-stu-id="6136d-121">Retailer sometimes have recurrent tasks, such as "Thursday closure checklist" or "First day of the month checklist."</span></span> <span data-ttu-id="6136d-122">Tāpēc viņi var vēlēties uzdevumu sarakstu piešķirt periodiski.</span><span class="sxs-lookup"><span data-stu-id="6136d-122">Therefore, they might want to assign the task list on a recurring basis.</span></span>

1. <span data-ttu-id="6136d-123">Dodieties uz **Retail un Commerce \>Uzdevumu pārvaldība \>Uzdevumu pārvaldības administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="6136d-123">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="6136d-124">Atlasiet uzdevumu sarakstu, ko piešķirt.</span><span class="sxs-lookup"><span data-stu-id="6136d-124">Select the task list to assign.</span></span>
1. <span data-ttu-id="6136d-125">Atlasiet **Uzsākt procesu**.</span><span class="sxs-lookup"><span data-stu-id="6136d-125">Select **Start process**.</span></span>
1. <span data-ttu-id="6136d-126">Dialoglodziņa **Uzsākt procesu** cilnē **Vispārīgi**, laukā **Procesa nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="6136d-126">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name.</span></span>
1. <span data-ttu-id="6136d-127">Iestatiet opciju **Periodiskums** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="6136d-127">Set the **Recurrence** option to **Yes**.</span></span>
1. <span data-ttu-id="6136d-128">Laukā **Atkārtošanās mērķa datuma nobīde dienās** ievadiet dienu skaitu.</span><span class="sxs-lookup"><span data-stu-id="6136d-128">In the **Recurrence target date offset in days** field, enter a number of days.</span></span> <span data-ttu-id="6136d-129">Piemēram, ja ievadāt **4**, mērķa datums ir atkārtošanās datums plus četras dienas.</span><span class="sxs-lookup"><span data-stu-id="6136d-129">For example, if you enter **4**, the target date is the recurrence date plus four days.</span></span>
1. <span data-ttu-id="6136d-130">Cilnē **Palaist fonā** atlasiet **Periodiskums**.</span><span class="sxs-lookup"><span data-stu-id="6136d-130">On the **Run in the background** tab, select **Recurrence**.</span></span>
1. <span data-ttu-id="6136d-131">Dialoglodziņā **Definēt periodiskumu** ievadiet biežuma kritērijus un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6136d-131">In the **Define recurrence** dialog box, enter the frequency criteria, and then select **OK**.</span></span>

<span data-ttu-id="6136d-132">Šajā attēlā parādīts piemērs, kā ievadīt biežuma kritērijus dialoglodziņā **Definēt periodiskumu**.</span><span class="sxs-lookup"><span data-stu-id="6136d-132">The following illustration shows an example of how to enter frequency criteria in the **Define recurrence** dialog box.</span></span>

![Biežuma kritēriju ievade dialoglodziņā Definēt periodiskumu](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a><span data-ttu-id="6136d-134">Izsekot uzdevumu saraksta statusam</span><span class="sxs-lookup"><span data-stu-id="6136d-134">Track task list status</span></span>

<span data-ttu-id="6136d-135">Ja esat reģionālais vadītājs vai veikala vadītājs, iespējams, vēlēsities izsekot to uzdevumu sarakstu statusam, kas ir piešķirti vairākiem veikaliem vai nodarbinātajiem.</span><span class="sxs-lookup"><span data-stu-id="6136d-135">If you're a regional manager or store manager, you might want to track the status of task lists that have been assigned to multiple stores or employees.</span></span> <span data-ttu-id="6136d-136">Pēc tam varat sekot līdzi veikaliem vai darbiniekiem, kas nav laicīgi izpildījuši tiem piešķirtos uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="6136d-136">You can then follow up with stores or workers that didn't complete their assigned tasks on time.</span></span> <span data-ttu-id="6136d-137">Commerce operāciju uzskaites daļa ļauj skatīt uzdevumu sarakstu statusu, atkārtoti piešķirt uzdevumus vai mainīt uzdevuma statusu.</span><span class="sxs-lookup"><span data-stu-id="6136d-137">Commerce back office lets you view the status of task lists, reassign tasks, or change the status of a task.</span></span>

<span data-ttu-id="6136d-138">Lai izsekotu uzdevumu saraksta statusam visiem uzdevumiem, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="6136d-138">To track the task list status for all tasks, follow these steps.</span></span>

1. <span data-ttu-id="6136d-139">Dodieties uz **Retail un Commerce \>Uzdevumu pārvaldība \>Uzdevumu pārvaldības procesi**.</span><span class="sxs-lookup"><span data-stu-id="6136d-139">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="6136d-140">Atlasiet cilni **Visi uzdevumu saraksti**, lai skatītu visu to uzdevumu sarakstu statusu, kas ir piešķirti dažādiem veikaliem.</span><span class="sxs-lookup"><span data-stu-id="6136d-140">Select the **All task lists** tab to view the status of all task lists that are assigned to various stores.</span></span>

<span data-ttu-id="6136d-141">Lai izsekotu uzdevumu saraksta statusam visiem uzdevumiem, kas piešķirti jums, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="6136d-141">To track the task list status for all tasks that are assigned to you, follow these steps.</span></span>

1. <span data-ttu-id="6136d-142">Dodieties uz **Retail un Commerce \>Uzdevumu pārvaldība \>Uzdevumu pārvaldības procesi**.</span><span class="sxs-lookup"><span data-stu-id="6136d-142">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="6136d-143">Atlasiet cilni **Mani uzdevumi** vai **Visi uzdevumi**, lai skatītu vai atjauninātu jums piešķirto uzdevumu statusu.</span><span class="sxs-lookup"><span data-stu-id="6136d-143">Select the **My tasks** or **All tasks** tab to view or update the status of tasks that are assigned to you.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6136d-144">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="6136d-144">Additional resources</span></span>

[<span data-ttu-id="6136d-145">Uzdevumu pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="6136d-145">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="6136d-146">Uzdevumu pārvaldības konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="6136d-146">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="6136d-147">Uzdevumu sarakstu izveidošana un uzdevumu pievienošana</span><span class="sxs-lookup"><span data-stu-id="6136d-147">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="6136d-148">Uzdevumu pārvaldība punktā POS</span><span class="sxs-lookup"><span data-stu-id="6136d-148">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
