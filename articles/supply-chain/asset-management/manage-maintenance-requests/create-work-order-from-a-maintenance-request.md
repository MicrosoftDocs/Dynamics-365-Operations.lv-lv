---
title: Darba pasūtījumu izveide no uzturēšanas pieprasījumiem
description: Šajā tēmā izskaidrots, kā izveidot darba pasūtījumu Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23039306bb827beb861eaacc3177f4917fabc8bf
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018100"
---
# <a name="create-work-orders-from-maintenance-requests"></a><span data-ttu-id="e5e3a-103">Darba pasūtījumu izveide no uzturēšanas pieprasījumiem</span><span class="sxs-lookup"><span data-stu-id="e5e3a-103">Create work orders from maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="e5e3a-104">Pēc uzturēšanas pieprasījumu izveides tos var viegli pārvērst par darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="e5e3a-104">After you've created maintenance requests, you can easily convert them to work orders.</span></span> <span data-ttu-id="e5e3a-105">Šajā tēmā aprakstīts ātrākais veids, kā strādāt ar uzturēšanas pieprasījumiem, vienlaicīgi atjaunināt vairākus uzturēšanas pieprasījumus un pēc tam vienlaicīgi izveidot darba pasūtījumu vairākiem uzturēšanas pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="e5e3a-105">This topic describes the quickest way to work with maintenance requests, update several maintenance requests at the same time, and then create a work order for several maintenance requests at the same time.</span></span> <span data-ttu-id="e5e3a-106">Lapā **Aktīvie uzturēšanas pieprasījumi** vai **Mania funkcionālā novietojuma uzturēšanas pieprasījumi** varat vienlaikus strādāt ar vienu uzturēšanas pieprasījumu un pārveidot vienu uzturēšanas pieprasījumu par darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e5e3a-106">On the **Active maintenance requests** or **My functional location maintenance requests** page, you can also work with one maintenance request at a time and convert one maintenance request to a work order.</span></span>

> [!NOTE]
> <span data-ttu-id="e5e3a-107">Katru uzturēšanas pieprasījumu var saistīt tikai ar vienu darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e5e3a-107">Every maintenance request can be related to only one work order.</span></span> <span data-ttu-id="e5e3a-108">Taču vienā darba pasūtījumā var iekļaut vairākus uzturēšanas pieprasījumus pat tad, ja uzturēšanas pieprasījumiem ir dažādi līdzekļi.</span><span class="sxs-lookup"><span data-stu-id="e5e3a-108">However, multiple maintenance requests can be included in one work order, even if the maintenance requests have different assets.</span></span>

1. <span data-ttu-id="e5e3a-109">Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **uzturēšanas pieprasījumi** \> **Visi uzturēšanas pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="e5e3a-109">Select **Asset management** \> **Common** \> **maintenance requests** \> **All maintenance requests**.</span></span>
2. <span data-ttu-id="e5e3a-110">Pirms jūs varat izveidot darba pasūtījumu no uzturēšanas pieprasījumiem, ir jāatlasa vismaz uzturēšanas darba veids uzturēšanas pieprasījumiem, kā arī uzturēšanas darba veida variants un tirdzniecība, ja šī informācija ir svarīga.</span><span class="sxs-lookup"><span data-stu-id="e5e3a-110">Before you can create a work order from maintenance requests, you must select, at a minimum, a maintenance job type for the maintenance requests, and also a maintenance job type variant and trade, if this information is relevant.</span></span> <span data-ttu-id="e5e3a-111">Režģa skatā varat viegli atjaunināt informāciju par uzturēšanas pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="e5e3a-111">In the grid view, you can easily update information for a maintenance request.</span></span>
3. <span data-ttu-id="e5e3a-112">Kad esat gatavs izveidot darba pasūtījumu, atlasiet uzturēšanas pieprasījumus, ko tajā iekļaut.</span><span class="sxs-lookup"><span data-stu-id="e5e3a-112">When you're ready to create a work order, select the maintenance requests to include in it.</span></span>

    - <span data-ttu-id="e5e3a-113">Ja atlasāt vairākus uzturēšanas pieprasījumus, kas ir jāpārvērš par darba pasūtījumu, tad gan lauks **Līdzeklis**, gan lauks **Uzturēšanas darba veids** ir jāiestata pirms darba pasūtījuma izveides.</span><span class="sxs-lookup"><span data-stu-id="e5e3a-113">If you select several maintenance requests to convert to a work order, both the **Asset** field and the **Maintenance job type** field must be set before you create the work order.</span></span>
    - <span data-ttu-id="e5e3a-114">Ja atlasāt vienu uzturēšanas pieprasījumu, kas jāpārvērš par darba pasūtījumu, pirms darba pasūtījuma izveides ir jāiestata tikai lauks **Līdzeklis**.</span><span class="sxs-lookup"><span data-stu-id="e5e3a-114">If you select one maintenance request to convert to a work order, only the **Asset** field must be set before you create the work order.</span></span> <span data-ttu-id="e5e3a-115">Tomēr, izveidojot darba pasūtījumu, varat atlasīt uzturēšanas darba veidu (un saistīto uzturēšanas darba veida variantu un tirdzniecību, ja šī informācija ir svarīga) dialoglodziņā **Izveidot darba pasūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="e5e3a-115">However, when you create the work order, you can select a maintenance job type (and a related maintenance job type variant and trade, if this information is relevant) in the **Create work order** dialog box.</span></span>

4. <span data-ttu-id="e5e3a-116">Atlasiet **Darba pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="e5e3a-116">Select **Work order**.</span></span>
5. <span data-ttu-id="e5e3a-117">Dialoglodziņā **Izveidot darba pasūtījumu** iestatiet laukus un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e5e3a-117">In the **Create work order** dialog box, set the fields, and then select **OK**.</span></span>

    <span data-ttu-id="e5e3a-118">Ziņojumu josla var paziņot, ka ir izveidots jauns darba pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="e5e3a-118">A message bar might notify you that a new work order has been created.</span></span>

    <span data-ttu-id="e5e3a-119">Turklāt, izveidojot darba pasūtījumu, kas ir balstīts uz uzturēšanas pieprasījumu, ja ar uzturēšanas pieprasījumu saistītais līdzeklis ir ietverts garantijas līgumā, ziņojumu josla paziņo par garantijas līgumu.</span><span class="sxs-lookup"><span data-stu-id="e5e3a-119">Additionally, when you create a work order that is based on a maintenance request, if the asset that is related to the maintenance request is included in a warranty agreement, a message bar notifies you about the warranty agreement.</span></span>

6. <span data-ttu-id="e5e3a-120">Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Darba pasūtījumi** \> **Visi darba pasūtījumi** un atveriet jauno darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e5e3a-120">Select **Asset management** \> **Common** \> **Work orders** \> **All work orders**, and open the new work order.</span></span>

    ![Atvērt jaunu darba pasūtījumu](media/05-manage-maintenance-requests.png)

