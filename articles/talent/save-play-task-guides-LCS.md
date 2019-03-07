---
title: Uzdevumu ceļvežu saglabāšana pakalpojumā LCS un to atkārtošana
description: Šajā tēmā ir paskaidrots, kā saglabāt uzdevumu ceļvežus pakalpojumā Microsoft Dynamics Lifecycle Services (LCS) un pēc tam tos atkārtoti skatīt.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 40b4c3154a04a557b8a670e1f1ae3722c71122fe
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "305334"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="bb0d1-103">Uzdevumu ceļvežu saglabāšana pakalpojumā LCS un to atkārtošana</span><span class="sxs-lookup"><span data-stu-id="bb0d1-103">Save task guides to LCS and replay them</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bb0d1-104">**Informācija par vidi**</span><span class="sxs-lookup"><span data-stu-id="bb0d1-104">**Environment details**</span></span> 

<span data-ttu-id="bb0d1-105">Programma Microsoft Dynamics 365 for Talent, kas ir izvietota, izmantojot pakalpojumu Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="bb0d1-105">Microsoft Dynamics 365 for Talent, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="bb0d1-106">**Izejas plūsma**</span><span class="sxs-lookup"><span data-stu-id="bb0d1-106">**Issue**</span></span>

<span data-ttu-id="bb0d1-107">Debitors vēlas saglabāt jaunos uzdevumu ierakstus savā LCS projektā un tad atkārtot saglabātos uzd. ceļvežus.</span><span class="sxs-lookup"><span data-stu-id="bb0d1-107">The customer wants to save new task recordings to his or her LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="bb0d1-108">**Izšķirtspēja**</span><span class="sxs-lookup"><span data-stu-id="bb0d1-108">**Resolution**</span></span>

<span data-ttu-id="bb0d1-109">Rīkojieties šādi, lai saglabātu uzd. ierakstu LCS.</span><span class="sxs-lookup"><span data-stu-id="bb0d1-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="bb0d1-110">Pierakstieties LCS un atl. projektu.</span><span class="sxs-lookup"><span data-stu-id="bb0d1-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="bb0d1-111">Atl. elementu **Biznesa procesu modelētājs**.</span><span class="sxs-lookup"><span data-stu-id="bb0d1-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="bb0d1-112">Skatiet lapu atjauninātajā BPM pieredzē.</span><span class="sxs-lookup"><span data-stu-id="bb0d1-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="bb0d1-113">Atlasiet bibl. un tad atlasiet **Kopēt**.</span><span class="sxs-lookup"><span data-stu-id="bb0d1-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="bb0d1-114">Ievadiet nosauk. biznesa procesu modelētāja (BPM) modelim.</span><span class="sxs-lookup"><span data-stu-id="bb0d1-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="bb0d1-115">Pierakst. Talent no LCS.</span><span class="sxs-lookup"><span data-stu-id="bb0d1-115">Sign in to Talent from LCS.</span></span>
7. <span data-ttu-id="bb0d1-116">Laukā **Meklēt** ievadiet **palīdzība**.</span><span class="sxs-lookup"><span data-stu-id="bb0d1-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="bb0d1-117">Atveras Lifecycle Services palīdz.</span><span class="sxs-lookup"><span data-stu-id="bb0d1-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="bb0d1-118">Atl. pogu **Atsvaidzināt** Lifecycle Services palīdzības konfigurācijai.</span><span class="sxs-lookup"><span data-stu-id="bb0d1-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="bb0d1-119">Ir jāparādās jaunajai BPM bibliotēkai, un tai jābūt aktīvai.</span><span class="sxs-lookup"><span data-stu-id="bb0d1-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="bb0d1-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="bb0d1-120">Close the page.</span></span>
10. <span data-ttu-id="bb0d1-121">Izveid. uzd. ierakstu.</span><span class="sxs-lookup"><span data-stu-id="bb0d1-121">Create a task recording.</span></span>
11. <span data-ttu-id="bb0d1-122">Pēc beigām atl. **Sagl. pakalpojumā Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="bb0d1-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![Saglabāt pakalpojumos Lifecycle Services](media/task-guides.png)

12. <span data-ttu-id="bb0d1-124">Atlasiet BPM bibliotēku un zaru, kurā saglabāt uzd. ierakstu.</span><span class="sxs-lookup"><span data-stu-id="bb0d1-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="bb0d1-125">Rīkojieties šādi, lai atkārtotu uzd. ceļv. no LCS.</span><span class="sxs-lookup"><span data-stu-id="bb0d1-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="bb0d1-126">Palaidiet Uzd. reģ.</span><span class="sxs-lookup"><span data-stu-id="bb0d1-126">Start Task recorder.</span></span>
2. <span data-ttu-id="bb0d1-127">Atl. **Atvērt no LCS**.</span><span class="sxs-lookup"><span data-stu-id="bb0d1-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="bb0d1-128">Atlasiet bibliotēku un BPM zaru, kurā ir saglabātais uzd. ceļvedis.</span><span class="sxs-lookup"><span data-stu-id="bb0d1-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="bb0d1-129">Atv. uzd. ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="bb0d1-129">Open the task guide.</span></span>
