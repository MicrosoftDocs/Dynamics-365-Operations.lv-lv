---
title: Vispārējās plānošanas darba atcelšana
description: Šajā tēmā izskaidrots, kā atcelt aktīvu plānošanas darbu, kas izmanto iebūvētās plānošanas funkcionalitāti.
author: ChristianRytt
manager: tfehr
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1e38b1bb84414dde603dbf5bcda0e8253a12e40b
ms.sourcegitcommit: 78a1aa37f9a1565135b139e36501b759e7b2f849
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/14/2020
ms.locfileid: "3374800"
---
# <a name="cancel-a-master-planning-job"></a><span data-ttu-id="324ea-103">Vispārējās plānošanas darba atcelšana</span><span class="sxs-lookup"><span data-stu-id="324ea-103">Cancel a master planning job</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="324ea-104">Pakalpojumā Microsoft Dynamics 365 Supply Chain Management ir vairākas opcijas, kā atcelt vispārējās plānošanas darbu.</span><span class="sxs-lookup"><span data-stu-id="324ea-104">In Microsoft Dynamics 365 Supply Chain Management, there are multiple options for canceling a master planning job.</span></span> <span data-ttu-id="324ea-105">Piemēram, iespējams, jūs vēlēsities atcelt vispārējās plānošanas darbu, ja tas tika sākts kļūdas dēļ vai darbojas ilgāk, nekā paredzēts, un jūs vēlaties to beigt.</span><span class="sxs-lookup"><span data-stu-id="324ea-105">For example, you may want to cancel a master planning job if it was started by mistake or is running longer than expected and you want to end it.</span></span> <span data-ttu-id="324ea-106">Labākais veids, kā atcelt plānošanas darbu, ir no lapas **Nepabeigtie plānošanas procesi**.</span><span class="sxs-lookup"><span data-stu-id="324ea-106">The best way to cancel a planning job is from  the **Unfinished planning processes** page.</span></span> <span data-ttu-id="324ea-107">Alternatīvās opcijas no lapām **Pakešuzdevumi** un **Uzlabotie pakešuzdevumi** var izmantot tikai tad, ja, atceļot vispārējās plānošanas darbu no lapas **Nepabeigtie plānošanas procesi**, tas dažu minūšu laikā netika izpildīts.</span><span class="sxs-lookup"><span data-stu-id="324ea-107">Alternative options from the **Batch jobs** and **Batch jobs enhanced** pages should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

## <a name="preferred-cancel-option"></a><span data-ttu-id="324ea-108">Vēlamā atcelšanas opcija</span><span class="sxs-lookup"><span data-stu-id="324ea-108">Preferred cancel option</span></span>
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a><span data-ttu-id="324ea-109">Atcelt vispārējās plānošanas darbu no lapas **Nepabeigtie plānošanas procesi**</span><span class="sxs-lookup"><span data-stu-id="324ea-109">Cancel master planning job from **Unfinished planning processes** page</span></span>
1. <span data-ttu-id="324ea-110">Dodieties uz **Vispārējā plānošana > Uzziņas un atskaites > Vispārējā plānošana > Nepabeigtie plānošanas procesi**.</span><span class="sxs-lookup"><span data-stu-id="324ea-110">Go to **Master planning > Inquiries and reports > Master planning > Unfinished planning processes**.</span></span>
2. <span data-ttu-id="324ea-111">Atlasiet līniju ar plānošanas procesu, kuru vēlaties atcelt.</span><span class="sxs-lookup"><span data-stu-id="324ea-111">Select the line with the planning process that you want to cancel.</span></span>
3. <span data-ttu-id="324ea-112">Noklikšķiniet uz **Atcelt**.</span><span class="sxs-lookup"><span data-stu-id="324ea-112">Click **Cancel**.</span></span>

## <a name="additional-cancel-options"></a><span data-ttu-id="324ea-113">Papildu atcelšanas opcijas</span><span class="sxs-lookup"><span data-stu-id="324ea-113">Additional cancel options</span></span>
<span data-ttu-id="324ea-114">Tās var izmantot tikai tad, ja, atceļot vispārējās plānošanas darbu no lapas **Nepabeigtie plānošanas procesi**, tas dažu minūšu laikā netika izpildīts.</span><span class="sxs-lookup"><span data-stu-id="324ea-114">These should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a><span data-ttu-id="324ea-115">Vispārējās plānošanas darba dzēšana no lapas **Pakešuzdevumi**</span><span class="sxs-lookup"><span data-stu-id="324ea-115">Delete master planning job from the **Batch jobs** page</span></span>
1. <span data-ttu-id="324ea-116">Dodieties uz **Sistēmas administrēšana > Pieprasījumi > Pakešuzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="324ea-116">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="324ea-117">Atlasiet līniju ar plānošanas darbu, kuru vēlaties dzēst.</span><span class="sxs-lookup"><span data-stu-id="324ea-117">Select the line with the planning job that you want to delete.</span></span>
3. <span data-ttu-id="324ea-118">Noklikšķiniet uz **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="324ea-118">Click **Delete**.</span></span>

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a><span data-ttu-id="324ea-119">Pārtraukt vispārējās plānošanas darbu no lapas **Uzlabotie pakešuzdevumi**</span><span class="sxs-lookup"><span data-stu-id="324ea-119">Abort master planning job task from the **Batch jobs enhanced** page</span></span>
1. <span data-ttu-id="324ea-120">Dodieties uz **Sistēmas administrēšana > Pieprasījumi > Pakešuzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="324ea-120">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="324ea-121">Ja darba ID sarakstā nav redzams, noklikšķiniet uz **Pārslēgties uz uzlaboto formu**, pretējā gadījumā pārejiet pie nākamās darbības.</span><span class="sxs-lookup"><span data-stu-id="324ea-121">If the job ID is not shown in the list, click **Switch to enhanced form**, otherwise proceed with the next step.</span></span>
3. <span data-ttu-id="324ea-122">Atvērt pakešuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="324ea-122">Open the batch job.</span></span> <span data-ttu-id="324ea-123">Noklikšķiniet uz **Darba ID** pakešuzdevumam ar uzdevumiem, kurus vēlaties beigt.</span><span class="sxs-lookup"><span data-stu-id="324ea-123">Click the **Job ID** for the batch job with tasks that you want to end.</span></span>
4. <span data-ttu-id="324ea-124">Sadaļā **Pakešuzdevumi** atlasiet uzdevumus, kurus nepieciešams beigt.</span><span class="sxs-lookup"><span data-stu-id="324ea-124">In **Batch tasks**, select the tasks to end.</span></span>
5. <span data-ttu-id="324ea-125">Noklikšķiniet uz **Mainīt statusu**, izvēlieties **Atcelt** un noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="324ea-125">Click **Change status**, choose **Canceling** and click **OK**.</span></span>
6. <span data-ttu-id="324ea-126">Kopsavilkuma cilnē **Pakešuzdevumi** noklikšķiniet uz **Pārtraukt**.</span><span class="sxs-lookup"><span data-stu-id="324ea-126">On the **Batch tasks** FastTab, click **Abort**.</span></span>
