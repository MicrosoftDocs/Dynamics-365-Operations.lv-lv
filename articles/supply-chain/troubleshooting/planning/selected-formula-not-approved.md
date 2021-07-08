---
title: Atlasītais formulas numurs nav apstiprināts partijas pasūtījumam
description: Mēģinot apstiprināt plānoto pasūtījumu, tiek saņemts kļūdas ziņojums, kurā norādīts, ka atlasītais formulas numurs nav apstiprināts partijas pasūtījumam.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294124"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a><span data-ttu-id="70ee5-103">Atlasītais formulas numurs nav apstiprināts partijas pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="70ee5-103">Selected formula number isn't approved for a batch order</span></span>

<span data-ttu-id="70ee5-104">Kļūdas kods: PRO2614</span><span class="sxs-lookup"><span data-stu-id="70ee5-104">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="70ee5-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="70ee5-105">Symptoms</span></span>

<span data-ttu-id="70ee5-106">Mēģinot apstiprināt plānoto pasūtījumu saņemsit šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="70ee5-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="70ee5-107">Atlasītais formulas cipars nav apstiprināts lietošanai partijas pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="70ee5-107">The selected formula number is not approved for a batch order.</span></span>

## <a name="cause"></a><span data-ttu-id="70ee5-108">Iemesls</span><span class="sxs-lookup"><span data-stu-id="70ee5-108">Cause</span></span>

<span data-ttu-id="70ee5-109">Sistēma validē apstiprināšanas darbību, lai pārliecinātos, ka aktīvajam krājumam ir pieejama apstiprināta formula.</span><span class="sxs-lookup"><span data-stu-id="70ee5-109">The system validates the firming operation to make sure that an approved formula is available for the active item.</span></span> <span data-ttu-id="70ee5-110">Iespējams, formula ir jāapstiprina.</span><span class="sxs-lookup"><span data-stu-id="70ee5-110">You must probably approve the formula.</span></span>

## <a name="resolution"></a><span data-ttu-id="70ee5-111">Novēršana</span><span class="sxs-lookup"><span data-stu-id="70ee5-111">Resolution</span></span>

<span data-ttu-id="70ee5-112">Lai apstiprinātu formulu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="70ee5-112">To approve a formula, follow these steps.</span></span>

1. <span data-ttu-id="70ee5-113">Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Materiālu komplekti un formulas \> Formulas**.</span><span class="sxs-lookup"><span data-stu-id="70ee5-113">Go to **Product information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="70ee5-114">Atlasiet atbilstošo formulu.</span><span class="sxs-lookup"><span data-stu-id="70ee5-114">Select the relevant formula.</span></span>
1. <span data-ttu-id="70ee5-115">Darbību rūts cilnē **Formula**, grupā **Uzturēt** atlasiet **Apstiprināt formulu**.</span><span class="sxs-lookup"><span data-stu-id="70ee5-115">On the Action Pane, on the **Formula** tab, in the **Maintain** group, select **Approve formula**.</span></span>
1. <span data-ttu-id="70ee5-116">Dialoglodziņā **Apstiprināt MK vai formulu** atlasiet apstiprinātāju un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="70ee5-116">In the **Approve BOM or formula** dialog box, select an approver, and then select **OK**.</span></span>
