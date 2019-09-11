---
title: Darba pasūtījumi un pamatlīdzekļi
description: Šajā tēmā ir paskaidroti darba pasūtījumi un pamatlīdzekļi līdzekļu pārvaldībā.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f03b7fa073c4e5338b7b5681ba7b8c9fe00a657b
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875771"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="b76dd-103">Darba pasūtījumi un pamatlīdzekļi</span><span class="sxs-lookup"><span data-stu-id="b76dd-103">Work orders and fixed assets</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="b76dd-104">Līdzekļu pārvaldībā līdzekļi var būt saistīti ar pamatlīdzekļiem, un šiem līdzekļiem varat izveidot darba pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="b76dd-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="b76dd-105">Ja izmantojat šo funkcionalitāti, varat iegūt pilnīgu pārskatu par pamatlīdzekļiem, saistītajiem investīciju projektiem un izmaksām, kas reģistrētas ieguldījumu projektiem moduļos **Projekta pārvaldība un uzskaite** un **Pamatlīdzekļi** programmā Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b76dd-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs registered on the investment projects in the **Project management and accounting** module and the **Fixed assets** module in Dynamics 365 for Finance and Operations.</span></span>

>[!NOTE]
><span data-ttu-id="b76dd-106">Lauks **Pamatlīdzekļa numurs** darba pasūtījuma uzdevuma projektā tiek aizpildīts tikai tad, ja darba pasūtījuma uzdevuma projektā kā projekta veids ir izvēlēts veids “Investīcijas”.</span><span class="sxs-lookup"><span data-stu-id="b76dd-106">The **Fixed asset number** field is only filled out on the work order job project if type "Investment" is selected as the project type on the work order job project.</span></span>

![1. attēls](media/24-work-orders.png)

<span data-ttu-id="b76dd-108">Šī procedūra apraksta relāciju starp līdzekļiem, darba pasūtījumiem, darba pasūtījuma uzdevuma projektiem un pamatlīdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="b76dd-108">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="b76dd-109">Jūs izveidojat līdzekli, kas attiecas uz pamatlīdzekli, kā parādīts attēlā zemāk.</span><span class="sxs-lookup"><span data-stu-id="b76dd-109">You create an asset that you relate to a fixed asset, as shown in the figure below.</span></span>

![2. attēls](media/25-work-orders.png)

2. <span data-ttu-id="b76dd-111">Kad iestatāt darba pasūtījuma veidus (**Līdzekļu pārvaldība** > **Iestatīšana** > **Darba pasūtījumi** > **Darba pasūtījumu veidi**), jūs izveidojat darba pasūtījuma veidu ieguldījumu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="b76dd-111">When you set up work order types (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="b76dd-112">Skatiet arī sadaļu [Darba pasūtījumu veidi](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="b76dd-112">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![3. attēls](media/26-work-orders.png)

3. <span data-ttu-id="b76dd-114">Kad iestatāt darba pasūtījuma projekta grupas (saite **Līdzekļa pārvaldība** > **Iestatīšana** > **Darba pasūtījumi** > **Projekta iestatīšana** > **Projekta gripa**), jūs izveidojat relāciju starp darba pasūtījuma veidu, kas tiek izmantots ieguldījumiem, un projekta grupu, kas izveidota ieguldījumiem modulī **Projekta pārvaldība un uzskaite** (**Projekta pārvaldība un uzskaite** > **Iestatīšana** > **Grāmatošana** > **Projekta grupas**).</span><span class="sxs-lookup"><span data-stu-id="b76dd-114">When you set up work order project groups (**Asset management** > **Setup** > **Work orders** > **Project setup** > **Project group** link), you create a relation between the work order type used for investments and the project group created for investments in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![4. attēls](media/27-work-orders.png)

4. <span data-ttu-id="b76dd-116">Veidojot darba pasūtījumu, kas attiecas uz pamatlīdzekļu objektu, jūs izvēlaties darba pasūtījuma veidu, kas tiek izmantots ieguldījumu apstrādei, piemēram, “Investīcijas”.</span><span class="sxs-lookup"><span data-stu-id="b76dd-116">When you create a work order that relates to a fixed asset object, you select the work order type used for handling investments, for example, "Investment".</span></span>

5. <span data-ttu-id="b76dd-117">Kad darba pasūtījums ir izveidots, ar to saistītais darba pasūtījuma veids tiek parādīts sadaļā **Visi darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="b76dd-117">When the work order is created, the related work order type is shown in **All work orders**.</span></span>

![5. attēls](media/28-work-orders.png)

6. <span data-ttu-id="b76dd-119">Kad darba pasūtījums ir izveidots, ar darba pasūtījumu saistīts projekts tiek izveidots sadaļā **Projekta pārvaldība un uzskaite** > **Visi projekti**.</span><span class="sxs-lookup"><span data-stu-id="b76dd-119">When the work order is created, the project related to the work order is created in **Project management and accounting** > **All projects**.</span></span> <span data-ttu-id="b76dd-120">Jūs varat apskatīt ar projektu saistīto informāciju, noklikšķinot uz darba pasūtījuma saites **Projekta ID** (sadaļā **Līdzekļu pārvaldība** atveriet darba pasūtījumu sadaļā Detalizētas informācijas skats > **Rindas informācija** kopsavilkuma cilne > **Vispārīgi** cilnes lauks > **Projekta ID**).</span><span class="sxs-lookup"><span data-stu-id="b76dd-120">You can see project-related information by clicking the **Project ID** link on the work order (in **Asset management**, open the work order in Details view > **Line details** FastTab > **General** tab > **Project ID** field).</span></span>

![6. attēls](media/29-work-orders.png)

7. <span data-ttu-id="b76dd-122">Sadaļā **Pamatlīdzekļi** jūs varat skatīt pārskatu par projektiem, kas saistīti ar pamatlīdzekli (**Pamatlīdzekļi** > **Pamatlīdzekļi** > **Pamatlīdzekļi** > noklikšķiniet uz pamatlīdzekļa laukā **Pamatlīdzekļa numurs** > skatiet saturu rūtī **Saistītā informācija** > sadaļā **Saistītie projekti**).</span><span class="sxs-lookup"><span data-stu-id="b76dd-122">In **Fixed assets**, you are able to see an overview of the projects associated with a fixed asset (**Fixed assets** > **Fixed assets** > **Fixed assets** > click on the fixed asset in the **Fixed asset number** field > view the contents in the **Related information** pane > **Associated projects** section).</span></span>

