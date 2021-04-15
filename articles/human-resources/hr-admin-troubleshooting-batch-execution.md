---
title: Atiestatīt iestrēgušus pakešuzdevumus
description: Šajā tēmā ir paskaidrots, kā atrisināt problēmas, kas saistītas ar iestrēgušajiem pakešuzdevumiem.
author: andreabichsel
ms.date: 03/19/2021
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
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: 01ef0bf8ccc486614eec42d3fb6f0b2941fc47c0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794953"
---
# <a name="reset-stuck-batch-jobs"></a><span data-ttu-id="75a14-103">Atiestatīt iestrēgušus pakešuzdevumus</span><span class="sxs-lookup"><span data-stu-id="75a14-103">Reset stuck batch jobs</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a><span data-ttu-id="75a14-104">Izsniegt</span><span class="sxs-lookup"><span data-stu-id="75a14-104">Issue</span></span>

<span data-ttu-id="75a14-105">Microsoft Dynamics 365 Human Resources var rasties problēmas ar pakešuzdevumiem, kas ir iestrēguši stāvoklī **Izpilde** vai **Atcelšana** un nav pabeigti.</span><span class="sxs-lookup"><span data-stu-id="75a14-105">Microsoft Dynamics 365 Human Resources can experience issues with batch jobs that are stuck in either an **Executing** or **Canceling** state and don't complete.</span></span>

## <a name="resolution"></a><span data-ttu-id="75a14-106">Novēršana</span><span class="sxs-lookup"><span data-stu-id="75a14-106">Resolution</span></span>

<span data-ttu-id="75a14-107">Ja pakešuzdevums ir iestrēdzis stāvoklī **Izpilde** vai **Atcelšana**, varat atiestatīt statusu, liekot atcelt darbu.</span><span class="sxs-lookup"><span data-stu-id="75a14-107">When a batch job is stuck in an **Executing** or **Canceling** state, you can reset the status by forcing the cancellation of the job.</span></span> <span data-ttu-id="75a14-108">Pēc pakešuzdevuma atcelšanas to var atiestatīt, iestatot statusu **Gaida**.</span><span class="sxs-lookup"><span data-stu-id="75a14-108">After you cancel it, you can reset the batch job by setting it to a **Waiting** status.</span></span> <span data-ttu-id="75a14-109">Pēc tam tas tiks atkal paņemts izpildei nākamajā plānotajā pakešizpildes reizē.</span><span class="sxs-lookup"><span data-stu-id="75a14-109">It will then be picked up again for execution in the next scheduled batch run.</span></span>

1. <span data-ttu-id="75a14-110">Darbvietā **Sistēmas administrēšana** atlasiet lapu **Saites** un atlasiet **Pakešuzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="75a14-110">In the **System administration** workspace, select the **Links** page, and select **Batch jobs**.</span></span>

2. <span data-ttu-id="75a14-111">Saraksta lapā **Pakešuzdevumi** atlasiet darbu, kas ir jāatiestata.</span><span class="sxs-lookup"><span data-stu-id="75a14-111">On the **Batch job** list page, select the job that needs to be reset.</span></span>

3. <span data-ttu-id="75a14-112">Darbību lentē atlasiet **Piespiedu atcelšana** un apstipriniet darbību.</span><span class="sxs-lookup"><span data-stu-id="75a14-112">On the action ribbon, select **Force cancel**, and confirm the action.</span></span>

   > [!NOTE]
   > <span data-ttu-id="75a14-113">Darbība **Piespiedu atcelšana** ir pieejama tikai tad, ja atlasītajam pakešuzdevumam ir statuss **Izpilde** vai **Atcelšana** un šim darbam netiek palaisti pakešveida izpildes vai atcelšanas procesi.</span><span class="sxs-lookup"><span data-stu-id="75a14-113">The **Force cancel** action is only available when the selected batch job has a status of either **Executing** or **Canceling**, and no batch execution or cancellation processes are running for the job.</span></span>

4. <span data-ttu-id="75a14-114">Uz darbības lentesatlasiet **Mainīt statusu**.</span><span class="sxs-lookup"><span data-stu-id="75a14-114">On the action ribbon, select **Change status**.</span></span>

5. <span data-ttu-id="75a14-115">Lapā **Atlasīt jaunu statusu** atlasiet **Gaida** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="75a14-115">On the **Select new status** page, select **Waiting**, and then select **OK**.</span></span>

   ![Atlasīt jaunu pakešuzdevuma statusu](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a><span data-ttu-id="75a14-117">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="75a14-117">See also</span></span>

[<span data-ttu-id="75a14-118">Veiktspējas optimizēšana, plānojot pakešuzdevumus pēc darba laika</span><span class="sxs-lookup"><span data-stu-id="75a14-118">Optimize performance by scheduling batch jobs after hours</span></span>](hr-admin-troubleshooting-batch-jobs.md)<br>
[<span data-ttu-id="75a14-119">Veiktspējas optimizēšana, izmantojot automātiskās tīrīšanas uzdevumus</span><span class="sxs-lookup"><span data-stu-id="75a14-119">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
