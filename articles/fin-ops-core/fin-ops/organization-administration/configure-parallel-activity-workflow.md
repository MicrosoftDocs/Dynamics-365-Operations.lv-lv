---
title: Paralēlu aktivitāšu konfigurēšana darbplūsmā
description: Lai konfigurētu paralēlu aktivitāti, darbplūsmas redaktorā izpildiet tālāk aprakstītās procedūras.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dfbe78f31082ad0b1272f02e3ae9d7adbd993b1
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797730"
---
# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="aa5fb-103">Paralēlu aktivitāšu konfigurēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="aa5fb-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa5fb-104">Lai konfigurētu paralēlu aktivitāti, darbplūsmas redaktorā izpildiet tālāk aprakstītās procedūras.</span><span class="sxs-lookup"><span data-stu-id="aa5fb-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="aa5fb-105">Paralēlā aktivitāte sastāv no darbplūsmas zariem, kas darbojas vienlaicīgi.</span><span class="sxs-lookup"><span data-stu-id="aa5fb-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="aa5fb-106">Paralēlās aktivitātes nosaukums</span><span class="sxs-lookup"><span data-stu-id="aa5fb-106">Name a parallel activity</span></span>

<span data-ttu-id="aa5fb-107">Lai ievadītu paralēlās aktivitātes nosaukumu, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="aa5fb-107">Follow these steps to enter a name for a parallel activity.</span></span>

1. <span data-ttu-id="aa5fb-108">Ar peles labo pogu noklikšķiniet uz paralēlās aktivitātes un pēc tam noklikšķiniet uz **Rekvizīti**, lai atvērtu formu **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="aa5fb-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="aa5fb-109">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="aa5fb-109">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="aa5fb-110">Laukā **Nosaukums** ievadiet unikālu paralēlās aktivitātes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="aa5fb-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4. <span data-ttu-id="aa5fb-111">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="aa5fb-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="aa5fb-112">Konfigurēt paralēlās aktivitātes zarus</span><span class="sxs-lookup"><span data-stu-id="aa5fb-112">Configure the branches of a parallel activity</span></span>

<span data-ttu-id="aa5fb-113">Lai pievienotu un konfigurētu šīs paralēlās aktivitātes zarus, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="aa5fb-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>

1. <span data-ttu-id="aa5fb-114">Veiciet dubultklikšķi uz paralēlās aktivitātes, lai parādītu paralēlās aktivitātes zarus.</span><span class="sxs-lookup"><span data-stu-id="aa5fb-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="aa5fb-115">Lai pievienotu zaru, velciet elementu **Zars** no apgabala **Darbplūsmas elementi** uz ievietošanas punktu uz audekla.</span><span class="sxs-lookup"><span data-stu-id="aa5fb-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="aa5fb-116">Nākamajā attēlā ir redzams ievietošanas punkts.</span><span class="sxs-lookup"><span data-stu-id="aa5fb-116">The following figure shows an insertion point.</span></span>

    ![Ievietošanas punkts](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > <span data-ttu-id="aa5fb-118">Zaru secība nav svarīga, jo visi paralēlās aktivitātes zari darbojas vienlaicīgi.</span><span class="sxs-lookup"><span data-stu-id="aa5fb-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span>

3. <span data-ttu-id="aa5fb-119">Lai konfigurētu katru zaru, skatiet sadaļu [Konfigurēt paralēlus zarus darbplūsmā](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="aa5fb-119">To configure each branch, see [Configure parallel branches in a workflow](configure-parallel-branch-workflow.md).</span></span>
