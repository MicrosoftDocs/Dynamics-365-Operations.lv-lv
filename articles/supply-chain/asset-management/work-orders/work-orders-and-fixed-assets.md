---
title: Darba pasūtījumi un pamatlīdzekļi
description: Šajā tēmā ir paskaidroti darba pasūtījumi un pamatlīdzekļi Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4eadbdc452a5b7d28adfa0f102a9a727faad3c07
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016707"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="03c9e-103">Darba pasūtījumi un pamatlīdzekļi</span><span class="sxs-lookup"><span data-stu-id="03c9e-103">Work orders and fixed assets</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="03c9e-104">Līdzekļu pārvaldībā līdzekļi var būt saistīti ar pamatlīdzekļiem, un šiem līdzekļiem varat izveidot darba pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="03c9e-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="03c9e-105">Ja izmantojat šo funkcionalitāti, varat iegūt pilnīgu pārskatu par pamatlīdzekļiem, saistītajiem investīciju projektiem un izmaksām, kas reģistrētas ieguldījumu projektiem moduļos **Projekta pārvaldība un uzskaite** un **Pamatlīdzekļi** programmā Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="03c9e-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs that are registered on the investment projects in the **Project management and accounting** and **Fixed assets** modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

>[!NOTE]
><span data-ttu-id="03c9e-106">Lauks **Pamatlīdzekļa numurs** darba pasūtījuma uzdevuma projektā tiek aizpildīts tikai tad, ja darba pasūtījuma uzdevuma projektā kā projekta veids ir izvēlēts veids **Investīcijas**.</span><span class="sxs-lookup"><span data-stu-id="03c9e-106">The **Fixed asset number** field on the work order job project is set only if **Investment** is selected as the project type on the work order job project.</span></span>

<span data-ttu-id="03c9e-107">Attēlā ir parādīta saite starp investīciju projektu **projekta vadības un uzskaites** modulī un darba pasūtījuma darba projektu.</span><span class="sxs-lookup"><span data-stu-id="03c9e-107">The illustration below shows the relation between an investment project in the **Project management and accounting** module and a work order job project.</span></span>

![1. attēls](media/24-work-orders.png)

<span data-ttu-id="03c9e-109">Šī procedūra apraksta relāciju starp līdzekļiem, darba pasūtījumiem, darba pasūtījuma uzdevuma projektiem un pamatlīdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="03c9e-109">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="03c9e-110">Jūs izveidojat pamatlīdzeklim piesaistītu pamatlīdzekli.</span><span class="sxs-lookup"><span data-stu-id="03c9e-110">You create an asset that you relate to a fixed asset.</span></span>

![2. attēls](media/25-work-orders.png)

2. <span data-ttu-id="03c9e-112">Kad iestatāt darba pasūtījuma veidus **Darba pasūtījumu veidi** lapā (**Līdzekļu pārvaldība** > **Iestatīšana** > **Darba pasūtījumi** > **Darba pasūtījumu veidi**), jūs izveidojat darba pasūtījuma veidu ieguldījumu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="03c9e-112">When you set up work order types on the **Work order types** page (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="03c9e-113">Skatiet arī sadaļu [Darba pasūtījumu veidi](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="03c9e-113">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![3. attēls](media/26-work-orders.png)

3. <span data-ttu-id="03c9e-115">Kad iestatāt darba pasūtījuma projekta grupas cilnē **Projektu grupa** lapā **Darba pasūtījumu projektu iestatīšana** (**Līdzekļu pārvaldība** > **Iestatīšana** > **Darba pasūtījumi** > **Projekta iestatīšana**), jūs izveidojat relāciju starp darba pasūtījuma veidu, kas tiek izmantots ieguldījumiem, un projekta grupu, kas izveidota ieguldījumiem **Projektu grupu** lapā modulī **Projekta pārvaldība un uzskaite** (**Projekta pārvaldība un uzskaite** > **Iestatīšana** > **Grāmatošana** > **Projekta grupas**).</span><span class="sxs-lookup"><span data-stu-id="03c9e-115">When you set up work order project groups on the **Project group** tab of the **Work order project setup** page (**Asset management** > **Setup** > **Work orders** > **Project setup**), you create a relation between the work order type that is used for investments and the project group that was created for investments on the **Project groups** page in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![4. attēls](media/27-work-orders.png)

4. <span data-ttu-id="03c9e-117">Veidojot darba pasūtījumu, kas attiecas uz pamatlīdzekļu objektu, jūs izvēlaties darba pasūtījuma veidu, kas tiek izmantots ieguldījumu apstrādei, piemēram, **Investīcijas**.</span><span class="sxs-lookup"><span data-stu-id="03c9e-117">When you create a work order that is related to a fixed asset, you select the work order type that is used to handle investments, such as **Investment**.</span></span>

5. <span data-ttu-id="03c9e-118">Kad darba pasūtījums ir izveidots, ar to saistītais darba pasūtījuma veids tiek parādīts lapā **Visi darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="03c9e-118">When the work order is created, the related work order type is shown on the **All work orders** page.</span></span>

![5. attēls](media/28-work-orders.png)

6. <span data-ttu-id="03c9e-120">Kad darba pasūtījums ir izveidots, projekts, kas saistīts ar darba pasūtījumu, tiek izveidots lapā **Visi projekti** modulī **Projekta vadība un uzskaite** (**Projektu vadība un uzskaite** > **Projekti** > **Visi projekti**).</span><span class="sxs-lookup"><span data-stu-id="03c9e-120">When the work order is created, the project that is related to the work order is created on the **All projects** page in the **Project management and accounting** module (**Project management and accounting** > **Projects** > **All projects**).</span></span> <span data-ttu-id="03c9e-121">Lai skatītu informāciju, kas saistīta ar projektu, atlasiet saiti laukā **Projekta ID** cilnē **Vispārīgi** kopsavilkuma cilnē **Rindas detaļas** detalizētajā skatā **Visi darba pasūtījumi** lapā **Līdzekļu pārvaldības** modulī (**Līdzekļu pārvaldība** > **Kopējais** > **Darba pasūtījumi** > **Visiem darba pasūtījumi**).</span><span class="sxs-lookup"><span data-stu-id="03c9e-121">To view project-related information, select the link in the **Project ID** field on the **General** tab on the **Line details** FastTab in the details view of the **All work orders** page in the **Asset management** module (**Asset management** > **Commom** > **Work orders** > **All work orders**).</span></span>

![6. attēls](media/29-work-orders.png)

7. <span data-ttu-id="03c9e-123">Lai skatītu pārskatu par projektiem, kas saistīti ar pamatlīdzekļiem, atlasiet **Pamatlīdzekļi** > **Pamatlīdzekļi** > **Pamatlīdzekļi** un pēc tam laukā **Pamatlīdzekļa numurs** atlasiet saiti pamatlīdzeklim, lai atvērtu detaļu skatu.</span><span class="sxs-lookup"><span data-stu-id="03c9e-123">To see an overview of the projects associated with a fixed asset, select **Fixed assets** > **Fixed assets** > **Fixed assets**, and then, in the **Fixed asset number** field, select the link for the fixed asset to open the details view.</span></span> <span data-ttu-id="03c9e-124">Paplašiniet **Saistīto informācijas** rūti lapas labajā pusē un atlasiet **Saistītie projekti** kopsavilkuma cilni.</span><span class="sxs-lookup"><span data-stu-id="03c9e-124">Expand the **Related information** pane on the right side of the page, and select the **Associated projects** FastTab.</span></span>

