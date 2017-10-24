---
title: "Konfigurēt paralēlu aktivitāti darbplūsmā"
description: "Lai konfigurētu paralēlu aktivitāti, darbplūsmas redaktorā izpildiet tālāk aprakstītās procedūras."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5473327c0665c9183746eb8125c7a368fbedc21e
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="configure-a-parallel-activity-in-a-workflow"></a><span data-ttu-id="137c1-103">Konfigurēt paralēlu aktivitāti darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="137c1-103">Configure a parallel activity in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="137c1-104">Lai konfigurētu paralēlu aktivitāti, darbplūsmas redaktorā izpildiet tālāk aprakstītās procedūras.</span><span class="sxs-lookup"><span data-stu-id="137c1-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="137c1-105">Paralēlā aktivitāte sastāv no darbplūsmas zariem, kas darbojas vienlaicīgi.</span><span class="sxs-lookup"><span data-stu-id="137c1-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="137c1-106">Paralēlās aktivitātes nosaukums</span><span class="sxs-lookup"><span data-stu-id="137c1-106">Name a parallel activity</span></span>
<span data-ttu-id="137c1-107">Lai ievadītu paralēlās aktivitātes nosaukumu, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="137c1-107">Follow these steps to enter a name for a parallel activity.</span></span>
1.  <span data-ttu-id="137c1-108">Ar peles labo pogu noklikšķiniet uz paralēlās aktivitātes un pēc tam noklikšķiniet uz **Rekvizīti**, lai atvērtu formu **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="137c1-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2.  <span data-ttu-id="137c1-109">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="137c1-109">In the left pane, click **Basic Settings**.</span></span>
3.  <span data-ttu-id="137c1-110">Laukā **Nosaukums** ievadiet unikālu paralēlās aktivitātes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="137c1-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4.  <span data-ttu-id="137c1-111">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="137c1-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="137c1-112">Konfigurēt paralēlās aktivitātes zarus</span><span class="sxs-lookup"><span data-stu-id="137c1-112">Configure the branches of a parallel activity</span></span>
<span data-ttu-id="137c1-113">Lai pievienotu un konfigurētu šīs paralēlās aktivitātes zarus, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="137c1-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>
1.  <span data-ttu-id="137c1-114">Veiciet dubultklikšķi uz paralēlās aktivitātes, lai parādītu paralēlās aktivitātes zarus.</span><span class="sxs-lookup"><span data-stu-id="137c1-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2.  <span data-ttu-id="137c1-115">Lai pievienotu zaru, velciet elementu **Zars** no apgabala **Darbplūsmas elementi** uz ievietošanas punktu uz audekla.</span><span class="sxs-lookup"><span data-stu-id="137c1-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="137c1-116">Šajā attēlā redzams ievietošanas punkts.![Ievietošanas punkts](./media/workflow_insertionpoint.gif)</span><span class="sxs-lookup"><span data-stu-id="137c1-116">The following figure shows an insertion point.![Insertion point](./media/workflow_insertionpoint.gif)</span></span>
    | <span data-ttu-id="137c1-117">**Piezīme**</span><span class="sxs-lookup"><span data-stu-id="137c1-117">**Note**</span></span>                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="137c1-118">Zaru secība nav svarīga, jo visi paralēlās aktivitātes zari darbojas vienlaicīgi.</span><span class="sxs-lookup"><span data-stu-id="137c1-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span> |

3.  <span data-ttu-id="137c1-119">Lai konfigurētu katru zaru, skatiet sadaļu [Konfigurēt paralēlu zaru](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="137c1-119">To configure each branch, see [Configure a parallel branch](configure-parallel-branch-workflow.md).</span></span>






