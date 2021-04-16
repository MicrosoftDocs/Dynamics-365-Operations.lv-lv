---
title: Plānot darba pasūtījumu noteiktā datumā un laikā
description: Šajā tēmā ir aprakstīts, kā plānot darba pasūtījumu noteiktā datumā un laikā Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 827f4ca16341d29413f1b1d928965aa1919abf59
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822519"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a><span data-ttu-id="3ac78-103">Plānot darba pasūtījumu noteiktā datumā un laikā</span><span class="sxs-lookup"><span data-stu-id="3ac78-103">Schedule work order on specific date and time</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="3ac78-104">Ja darba pasūtījums ir jāplāno noteiktā datumā *un* laikā, varat ignorēt standarta plānošanas procesu Līdzekļu pārvaldībā un izveidot konkrētu grafiku darba pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="3ac78-104">If a work order must be scheduled on a specific date *and* time, you can override the standard scheduling process in Asset Management and create a specific schedule for a work order.</span></span>

1. <span data-ttu-id="3ac78-105">Klikšķiniet uz **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="3ac78-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="3ac78-106">Darba pasūtījuma sarakstā noklikšķiniet uz darba pasūtījuma ID kolonnā **Darba pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="3ac78-106">In the work order list, click on the Work order ID in the **Work order** column.</span></span>

3. <span data-ttu-id="3ac78-107">Noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="3ac78-107">Click **Edit**.</span></span>

4. <span data-ttu-id="3ac78-108">Kopsavilkuma cilnē **Darba pasūtījuma virsraksts** ievadiet sākuma un beigu datumu un laiku laukos **Paredzētais sākums** un **Paredzētās beigas**.</span><span class="sxs-lookup"><span data-stu-id="3ac78-108">On the **Work order header** FastTab, insert start and end dates and times in the **Expected start** and **Expected end** fields.</span></span>

    ![1. attēls](media/05-work-order-scheduling.png)

5. <span data-ttu-id="3ac78-110">Cilnē **Vispārīgi** noklikšķiniet uz **Grafiks**, lai izmantotu standarta plānošanas procesu, vai noklikšķiniet uz **Nosūtīt**, ja vēlaties piešķirt darba pasūtījumu konkrētam darbiniekam.</span><span class="sxs-lookup"><span data-stu-id="3ac78-110">On the **General** tab, click **Schedule** to use the standard scheduling process, or click **Dispatch** if you want to assign the work order to a specific worker.</span></span>

6. <span data-ttu-id="3ac78-111">Lai ignorētu esošās noslodzes rezervācija un lai nodrošinātu, ka darba pasūtījums tiek ieplānots paredzētajā periodā, veiciet atlasi, kā parādīts attēlā tālāk, dialoglodziņā **Ieplānot darba pasūtījumu** > sadaļā **Ierobežota noslodze**.</span><span class="sxs-lookup"><span data-stu-id="3ac78-111">In order to override any existing capacity reservations to ensure that the work order is scheduled in the expected period, make the selections as shown in the figure below in the **Schedule work order** dialog > **Finite capacity** section.</span></span> <span data-ttu-id="3ac78-112">Tas nozīmē, ka plānošanas process ignorēs esošās noslodzes rezervācijas, jo darba pasūtījumam ir jāsākas ar paredzēto sākuma laiku.</span><span class="sxs-lookup"><span data-stu-id="3ac78-112">This means that the scheduling process will ignore existing capacity reservations because the work order must start on the expected start time.</span></span>

    ![2. attēls](media/06-work-order-scheduling.png)

7. <span data-ttu-id="3ac78-114">Lai sāktu plānošanu, noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3ac78-114">Click **OK** to start scheduling.</span></span>

8. <span data-ttu-id="3ac78-115">Ja plānošanas procesa rezultātā izveidojas divas rezervācijas, ekrānā tiek parādīts ziņojums, un jūs varat pielāgot saistītos darba pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="3ac78-115">If the scheduling process results in double bookings, you will see a message on the screen, and you can adjust the related work orders.</span></span>

>[!NOTE]
><span data-ttu-id="3ac78-116">Lai darba pasūtījumam ieplānotu uzturēšanas speciālistu, šim uzturēšanas speciālistam ir jābūt pieejamam paredzētajā sākuma datumā un laikā.</span><span class="sxs-lookup"><span data-stu-id="3ac78-116">In order to schedule a maintenance worker for the work order, that maintenance worker must be available at the expected start date and time.</span></span> <span data-ttu-id="3ac78-117">Darbinieku pieejamība tiek iestatīta [Nodarbināto kalendārā](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md).</span><span class="sxs-lookup"><span data-stu-id="3ac78-117">Worker availability is set up in the [worker calendar](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md).</span></span> 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]