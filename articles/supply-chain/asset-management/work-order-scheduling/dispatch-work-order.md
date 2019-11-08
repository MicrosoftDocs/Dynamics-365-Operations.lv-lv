---
title: Darba pasūtījuma nosūtīšana
description: Šajā tēmā ir paskaidrots, kā nosūtīt darba pasūtījumu, izmantojot Līdzekļu pārvaldību.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 026b34934d6527416a4632d8e1aee76a8836dcb0
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652015"
---
# <a name="dispatch-work-order"></a><span data-ttu-id="de43e-103">Darba pasūtījuma nosūtīšana</span><span class="sxs-lookup"><span data-stu-id="de43e-103">Dispatch work order</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="de43e-104">Varat plānot vienu vai vairākus darba pasūtījumus vienam darbiniekam, izmantojot funkcionalitāti **Nosūtīt**.</span><span class="sxs-lookup"><span data-stu-id="de43e-104">You can schedule one work order or work order jobs to one worker using the **Dispatch** functionality.</span></span>

1. <span data-ttu-id="de43e-105">Klikšķiniet uz **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="de43e-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="de43e-106">Sarakstā atlasiet darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="de43e-106">Select the work order in the list.</span></span>

3. <span data-ttu-id="de43e-107">Cilnē **Vispārīgi** noklikšķiniet uz **Nosūtīt**.</span><span class="sxs-lookup"><span data-stu-id="de43e-107">On the **General** tab, click **Dispatch**.</span></span>

4. <span data-ttu-id="de43e-108">Dialoglodziņā **Plānot darba pasūtījumu** atlasiet darbinieku laukā **Darbinieks**.</span><span class="sxs-lookup"><span data-stu-id="de43e-108">In the **Schedule work order** dialog, select the worker in the **Worker** field.</span></span>

5. <span data-ttu-id="de43e-109">Laukā **Plānot stundas** varat ievietot paredzētās darba stundas, ja paredzētās darba stundas atšķiras no prognozētajām stundām.</span><span class="sxs-lookup"><span data-stu-id="de43e-109">In the **Schedule hours** field, you can insert expected work hours in case expected work hours differ from forecast hours.</span></span>

6. <span data-ttu-id="de43e-110">Laukā **Plānotais sākums** varat rediģēt sākuma datumu un laiku, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="de43e-110">In the **Scheduled start** field, you can edit start date and time, if required.</span></span>

7. <span data-ttu-id="de43e-111">Ja plānošanas procesam ir piemērojami noslodzes ierobežojumi saistībā ar resursiem, kas jau ieplānoti citiem darbiem, nodrošiniet, lai pārslēgšanas pogas **Līdzeklis**, **Rīks** un **Darbinieks** ir iestatītas uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="de43e-111">If the scheduling process should observe capacity limitations regarding resources already scheduled on other jobs, make sure that the **Asset**, **Tool**, and **Worker** toggle buttons are set to **Yes**.</span></span> <span data-ttu-id="de43e-112">Lai skatītu sīkāku informāciju par plānošanas procesu, atlasiet **Jā**, nospiežot pārslēgšanas pogu **Izvērsti**.</span><span class="sxs-lookup"><span data-stu-id="de43e-112">If you want to see detailed information about the scheduling process, select **Yes** on the **Verbose** toggle button.</span></span> <span data-ttu-id="de43e-113">Tas nozīmē, ka detalizēta informācija par aprēķinātajiem rezultātiem attiecībā uz darba rezultātiem ir parādīta Informācijas žurnālā.</span><span class="sxs-lookup"><span data-stu-id="de43e-113">This means detailed information about the calculated scores on the work order is shown in the Infolog.</span></span>

8. <span data-ttu-id="de43e-114">Atlasiet **Jā**, nospiežot pārslēgšanas pogu **Ignorēt grafiku**, lai ignorētu slēgtās dienas kalendārā (piemērojams līdzeklim, darbiniekam un rīkiem).</span><span class="sxs-lookup"><span data-stu-id="de43e-114">Select **Yes** on the **Ignore schedule** toggle button to ignore closed days in the calendar (applies to asset, worker, and tools).</span></span> <span data-ttu-id="de43e-115">Atlasiet **Jā**, nospiežot pārslēgšanas pogu **Ignorēt ieplānoto izpildi** ierobežojumu ignorēšanai, kuri, iespējams, tika atlasīti darba pasūtījumā attiecībā uz plānošanu.</span><span class="sxs-lookup"><span data-stu-id="de43e-115">Select **Yes** on the **Ignore scheduled execution** toggle button to ignore limitations that may have been selected on the work order regarding scheduling.</span></span> 

    <span data-ttu-id="de43e-116">Informāciju par ieplānotas izpildes iestatīšanu skatiet sadaļā [SIeplānota izpilde](../setup-for-work-orders/scheduled-execution.md).</span><span class="sxs-lookup"><span data-stu-id="de43e-116">For information on the setup of scheduled execution, see the [Scheduled execution](../setup-for-work-orders/scheduled-execution.md) section.</span></span>

9. <span data-ttu-id="de43e-117">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="de43e-117">Click **OK**.</span></span> <span data-ttu-id="de43e-118">Darba pasūtījuma dzīves cikla stāvoklis tiek automātiski atjaunināts uz **Ieplānotu** dzīves cikla stāvokli, kas norādīts sadaļā **Līdzekļu pārvaldība** > **Iestatīšana** > **Darba pasūtījumi** > **Dzīves cikla modeļi**.</span><span class="sxs-lookup"><span data-stu-id="de43e-118">The work order lifecycle state is automatically updated to the **Scheduled** lifecycle state specified **Asset management** > **Setup** > **Work orders** > **Lifecycle models**.</span></span>

<span data-ttu-id="de43e-119">Tālāk redzamais attēls parāda nosūtīšanas atlašu piemēru dialoglodziņā **Plānot darba pasūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="de43e-119">The figure below shows an example of dispatch selections in the **Schedule work order** dialog.</span></span>

![1. attēls](media/04-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="de43e-121">Ja vēlaties dzēst darba pasūtījuma grafiku, atlasiet darba pasūtījumu sadaļā **Visi darba pasūtījumi** un pēc tam noklikšķiniet uz **Dzēst grafiku** cilnē **Vispārīgi**. Izdzēšot grafiku, neaizmirstiet manuāli atjaunināt darba pasūtījuma dzīves cikla stāvokli.</span><span class="sxs-lookup"><span data-stu-id="de43e-121">If you want to delete the schedule on a work order, select the work order in **All work orders**, and then click **Delete schedule** on the **General** tab. Remember to manually update the work order lifecycle state if you delete the schedule.</span></span>

