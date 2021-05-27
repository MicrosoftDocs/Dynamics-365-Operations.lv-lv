---
title: Uzdevumu ceļvežu saglabāšana pakalpojumā LCS un to atkārtošana
description: Šajā rakstā paskaidrots, kā saglabāt uzdevumu ceļvežus pakalpojumā Microsoft Dynamics Lifecycle Services (LCS) un pēc tam tos atkārtoti skatīt.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 40377ece3685c50a448bf48e1d001fb1ecbbff3e
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6028063"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="e3ed4-103">Uzdevumu ceļvežu saglabāšana pakalpojumā LCS un to atkārtošana</span><span class="sxs-lookup"><span data-stu-id="e3ed4-103">Save task guides to LCS and replay them</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e3ed4-104">**Informācija par vidi**</span><span class="sxs-lookup"><span data-stu-id="e3ed4-104">**Environment details**</span></span> 

<span data-ttu-id="e3ed4-105">Programma Microsoft Dynamics 365 Human Resources, kas ir izvietota, izmantojot pakalpojumu Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="e3ed4-105">Microsoft Dynamics 365 Human Resources, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="e3ed4-106">**Izsniegt**</span><span class="sxs-lookup"><span data-stu-id="e3ed4-106">**Issue**</span></span>

<span data-ttu-id="e3ed4-107">Debitors vēlas saglabāt jaunos uzdevumu ierakstus savā LCS projektā un tad atkārtot saglabātos uzd. ceļvežus.</span><span class="sxs-lookup"><span data-stu-id="e3ed4-107">The customer wants to save new task recordings to the LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="e3ed4-108">**Novēršana**</span><span class="sxs-lookup"><span data-stu-id="e3ed4-108">**Resolution**</span></span>

<span data-ttu-id="e3ed4-109">Rīkojieties šādi, lai saglabātu uzd. ierakstu LCS.</span><span class="sxs-lookup"><span data-stu-id="e3ed4-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="e3ed4-110">Pierakstieties LCS un atl. projektu.</span><span class="sxs-lookup"><span data-stu-id="e3ed4-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="e3ed4-111">Atl. elementu **Biznesa procesu modelētājs**.</span><span class="sxs-lookup"><span data-stu-id="e3ed4-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="e3ed4-112">Skatiet lapu atjauninātajā BPM pieredzē.</span><span class="sxs-lookup"><span data-stu-id="e3ed4-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="e3ed4-113">Atlasiet bibl. un tad atlasiet **Kopēt**.</span><span class="sxs-lookup"><span data-stu-id="e3ed4-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="e3ed4-114">Ievadiet nosauk. biznesa procesu modelētāja (BPM) modelim.</span><span class="sxs-lookup"><span data-stu-id="e3ed4-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="e3ed4-115">Pierakstieties Human Resources no LCS.</span><span class="sxs-lookup"><span data-stu-id="e3ed4-115">Sign in to Human Resources from LCS.</span></span>
7. <span data-ttu-id="e3ed4-116">Laukā **Meklēt** ievadiet **palīdzība**.</span><span class="sxs-lookup"><span data-stu-id="e3ed4-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="e3ed4-117">Atveras Lifecycle Services palīdz.</span><span class="sxs-lookup"><span data-stu-id="e3ed4-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="e3ed4-118">Atl. pogu **Atsvaidzināt** Lifecycle Services palīdzības konfigurācijai.</span><span class="sxs-lookup"><span data-stu-id="e3ed4-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="e3ed4-119">Ir jāparādās jaunajai BPM bibliotēkai, un tai jābūt aktīvai.</span><span class="sxs-lookup"><span data-stu-id="e3ed4-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="e3ed4-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e3ed4-120">Close the page.</span></span>
10. <span data-ttu-id="e3ed4-121">Izveid. uzd. ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e3ed4-121">Create a task recording.</span></span>
11. <span data-ttu-id="e3ed4-122">Pēc beigām atl. **Sagl. pakalpojumā Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="e3ed4-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![Saglabāt pakalpojumos Lifecycle Services](media/task-guides.png)

12. <span data-ttu-id="e3ed4-124">Atlasiet BPM bibliotēku un zaru, kurā saglabāt uzd. ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e3ed4-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="e3ed4-125">Rīkojieties šādi, lai atkārtotu uzd. ceļv. no LCS.</span><span class="sxs-lookup"><span data-stu-id="e3ed4-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="e3ed4-126">Palaidiet Uzd. reģ.</span><span class="sxs-lookup"><span data-stu-id="e3ed4-126">Start Task recorder.</span></span>
2. <span data-ttu-id="e3ed4-127">Atl. **Atvērt no LCS**.</span><span class="sxs-lookup"><span data-stu-id="e3ed4-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="e3ed4-128">Atlasiet bibliotēku un BPM zaru, kurā ir saglabātais uzd. ceļvedis.</span><span class="sxs-lookup"><span data-stu-id="e3ed4-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="e3ed4-129">Atv. uzd. ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="e3ed4-129">Open the task guide.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]