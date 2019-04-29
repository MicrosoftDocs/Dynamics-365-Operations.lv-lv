---
title: Uzdevumu ceļvežu saglabāšana pakalpojumā LCS un to atkārtošana
description: Šajā tēmā ir paskaidrots, kā saglabāt uzdevumu ceļvežus pakalpojumā Microsoft Dynamics Lifecycle Services (LCS) un pēc tam tos atkārtoti skatīt.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1128a1d9b54935e44be76bf93549c0cae82e1d38
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/19/2019
ms.locfileid: "857896"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="e0b30-103">Uzdevumu ceļvežu saglabāšana pakalpojumā LCS un to atkārtošana</span><span class="sxs-lookup"><span data-stu-id="e0b30-103">Save task guides to LCS and replay them</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e0b30-104">**Informācija par vidi**</span><span class="sxs-lookup"><span data-stu-id="e0b30-104">**Environment details**</span></span> 

<span data-ttu-id="e0b30-105">Programma Microsoft Dynamics 365 for Talent, kas ir izvietota, izmantojot pakalpojumu Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="e0b30-105">Microsoft Dynamics 365 for Talent, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="e0b30-106">**Problēma**</span><span class="sxs-lookup"><span data-stu-id="e0b30-106">**Issue**</span></span>

<span data-ttu-id="e0b30-107">Debitors vēlas saglabāt jaunos uzdevumu ierakstus savā LCS projektā un tad atkārtot saglabātos uzd. ceļvežus.</span><span class="sxs-lookup"><span data-stu-id="e0b30-107">The customer wants to save new task recordings to his or her LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="e0b30-108">**Risinājums**</span><span class="sxs-lookup"><span data-stu-id="e0b30-108">**Resolution**</span></span>

<span data-ttu-id="e0b30-109">Rīkojieties šādi, lai saglabātu uzd. ierakstu LCS.</span><span class="sxs-lookup"><span data-stu-id="e0b30-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="e0b30-110">Pierakstieties LCS un atl. projektu.</span><span class="sxs-lookup"><span data-stu-id="e0b30-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="e0b30-111">Atl. elementu **Biznesa procesu modelētājs**.</span><span class="sxs-lookup"><span data-stu-id="e0b30-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="e0b30-112">Skatiet lapu atjauninātajā BPM pieredzē.</span><span class="sxs-lookup"><span data-stu-id="e0b30-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="e0b30-113">Atlasiet bibl. un tad atlasiet **Kopēt**.</span><span class="sxs-lookup"><span data-stu-id="e0b30-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="e0b30-114">Ievadiet nosauk. biznesa procesu modelētāja (BPM) modelim.</span><span class="sxs-lookup"><span data-stu-id="e0b30-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="e0b30-115">Pierakst. Talent no LCS.</span><span class="sxs-lookup"><span data-stu-id="e0b30-115">Sign in to Talent from LCS.</span></span>
7. <span data-ttu-id="e0b30-116">Laukā **Meklēt** ievadiet **palīdzība**.</span><span class="sxs-lookup"><span data-stu-id="e0b30-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="e0b30-117">Atveras Lifecycle Services palīdz.</span><span class="sxs-lookup"><span data-stu-id="e0b30-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="e0b30-118">Atl. pogu **Atsvaidzināt** Lifecycle Services palīdzības konfigurācijai.</span><span class="sxs-lookup"><span data-stu-id="e0b30-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="e0b30-119">Ir jāparādās jaunajai BPM bibliotēkai, un tai jābūt aktīvai.</span><span class="sxs-lookup"><span data-stu-id="e0b30-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="e0b30-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e0b30-120">Close the page.</span></span>
10. <span data-ttu-id="e0b30-121">Izveid. uzd. ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e0b30-121">Create a task recording.</span></span>
11. <span data-ttu-id="e0b30-122">Pēc beigām atl. **Sagl. pakalpojumā Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="e0b30-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![Saglabāt pakalpojumos Lifecycle Services](media/task-guides.png)

12. <span data-ttu-id="e0b30-124">Atlasiet BPM bibliotēku un zaru, kurā saglabāt uzd. ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e0b30-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="e0b30-125">Rīkojieties šādi, lai atkārtotu uzd. ceļv. no LCS.</span><span class="sxs-lookup"><span data-stu-id="e0b30-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="e0b30-126">Palaidiet Uzd. reģ.</span><span class="sxs-lookup"><span data-stu-id="e0b30-126">Start Task recorder.</span></span>
2. <span data-ttu-id="e0b30-127">Atl. **Atvērt no LCS**.</span><span class="sxs-lookup"><span data-stu-id="e0b30-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="e0b30-128">Atlasiet bibliotēku un BPM zaru, kurā ir saglabātais uzd. ceļvedis.</span><span class="sxs-lookup"><span data-stu-id="e0b30-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="e0b30-129">Atv. uzd. ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="e0b30-129">Open the task guide.</span></span>
