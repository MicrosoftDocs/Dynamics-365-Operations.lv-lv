---
title: Uzdevumu ceļvežu saglabāšana pakalpojumā LCS un to atkārtošana
description: Šajā rakstā paskaidrots, kā saglabāt uzdevumu ceļvežus pakalpojumā Microsoft Dynamics Lifecycle Services (LCS) un pēc tam tos atkārtoti skatīt.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8a18bb14ba8c3c926065c97b0ee26c38ee86ded2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053279"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="dfcde-103">Uzdevumu ceļvežu saglabāšana pakalpojumā LCS un to atkārtošana</span><span class="sxs-lookup"><span data-stu-id="dfcde-103">Save task guides to LCS and replay them</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="dfcde-104">**Informācija par vidi**</span><span class="sxs-lookup"><span data-stu-id="dfcde-104">**Environment details**</span></span> 

<span data-ttu-id="dfcde-105">Programma Microsoft Dynamics 365 Human Resources, kas ir izvietota, izmantojot pakalpojumu Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="dfcde-105">Microsoft Dynamics 365 Human Resources, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="dfcde-106">**Izsniegt**</span><span class="sxs-lookup"><span data-stu-id="dfcde-106">**Issue**</span></span>

<span data-ttu-id="dfcde-107">Debitors vēlas saglabāt jaunos uzdevumu ierakstus savā LCS projektā un tad atkārtot saglabātos uzd. ceļvežus.</span><span class="sxs-lookup"><span data-stu-id="dfcde-107">The customer wants to save new task recordings to the LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="dfcde-108">**Novēršana**</span><span class="sxs-lookup"><span data-stu-id="dfcde-108">**Resolution**</span></span>

<span data-ttu-id="dfcde-109">Rīkojieties šādi, lai saglabātu uzd. ierakstu LCS.</span><span class="sxs-lookup"><span data-stu-id="dfcde-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="dfcde-110">Pierakstieties LCS un atl. projektu.</span><span class="sxs-lookup"><span data-stu-id="dfcde-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="dfcde-111">Atl. elementu **Biznesa procesu modelētājs**.</span><span class="sxs-lookup"><span data-stu-id="dfcde-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="dfcde-112">Skatiet lapu atjauninātajā BPM pieredzē.</span><span class="sxs-lookup"><span data-stu-id="dfcde-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="dfcde-113">Atlasiet bibl. un tad atlasiet **Kopēt**.</span><span class="sxs-lookup"><span data-stu-id="dfcde-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="dfcde-114">Ievadiet nosauk. biznesa procesu modelētāja (BPM) modelim.</span><span class="sxs-lookup"><span data-stu-id="dfcde-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="dfcde-115">Pierakstieties Human Resources no LCS.</span><span class="sxs-lookup"><span data-stu-id="dfcde-115">Sign in to Human Resources from LCS.</span></span>
7. <span data-ttu-id="dfcde-116">Laukā **Meklēt** ievadiet **palīdzība**.</span><span class="sxs-lookup"><span data-stu-id="dfcde-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="dfcde-117">Atveras Lifecycle Services palīdz.</span><span class="sxs-lookup"><span data-stu-id="dfcde-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="dfcde-118">Atl. pogu **Atsvaidzināt** Lifecycle Services palīdzības konfigurācijai.</span><span class="sxs-lookup"><span data-stu-id="dfcde-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="dfcde-119">Ir jāparādās jaunajai BPM bibliotēkai, un tai jābūt aktīvai.</span><span class="sxs-lookup"><span data-stu-id="dfcde-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="dfcde-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="dfcde-120">Close the page.</span></span>
10. <span data-ttu-id="dfcde-121">Izveid. uzd. ierakstu.</span><span class="sxs-lookup"><span data-stu-id="dfcde-121">Create a task recording.</span></span>
11. <span data-ttu-id="dfcde-122">Pēc beigām atl. **Sagl. pakalpojumā Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="dfcde-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![Saglabāt pakalpojumos Lifecycle Services](media/task-guides.png)

12. <span data-ttu-id="dfcde-124">Atlasiet BPM bibliotēku un zaru, kurā saglabāt uzd. ierakstu.</span><span class="sxs-lookup"><span data-stu-id="dfcde-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="dfcde-125">Rīkojieties šādi, lai atkārtotu uzd. ceļv. no LCS.</span><span class="sxs-lookup"><span data-stu-id="dfcde-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="dfcde-126">Palaidiet Uzd. reģ.</span><span class="sxs-lookup"><span data-stu-id="dfcde-126">Start Task recorder.</span></span>
2. <span data-ttu-id="dfcde-127">Atl. **Atvērt no LCS**.</span><span class="sxs-lookup"><span data-stu-id="dfcde-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="dfcde-128">Atlasiet bibliotēku un BPM zaru, kurā ir saglabātais uzd. ceļvedis.</span><span class="sxs-lookup"><span data-stu-id="dfcde-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="dfcde-129">Atv. uzd. ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="dfcde-129">Open the task guide.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]