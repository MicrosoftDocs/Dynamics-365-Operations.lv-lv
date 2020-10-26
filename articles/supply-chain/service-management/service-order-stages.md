---
title: Pakalpojuma pasūtījuma stadijas
description: Definējot pakalpojuma pasūtījuma stadijas un piešķirot tās darbiniekiem, varat kontrolēt pakalpojuma pasūtījuma plūsmu caur uzdevumiem, ko pakalpojumu organizācijā veic dažādi cilvēki.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52bcb72e8222b378198fcd044428fa1a4a0e8944
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978439"
---
# <a name="service-order-stages"></a><span data-ttu-id="19d03-103">Pakalpojuma pasūtījuma stadijas</span><span class="sxs-lookup"><span data-stu-id="19d03-103">Service order stages</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="19d03-104">Varat iestatīt stadijas pakalpojuma pasūtījumam, lai definētu veicamos uzdevumus, to veikšanas secību un darbiniekus, kuri ir atbildīgi par to izpildīšanu.</span><span class="sxs-lookup"><span data-stu-id="19d03-104">You can set up stages for a service order to define the tasks that must be completed, the order in which they are completed, and the workers who are responsible for completing them.</span></span> <span data-ttu-id="19d03-105">Definējot pakalpojuma pasūtījuma stadijas un piešķirot tās darbiniekiem, jūs kontrolējat pakalpojuma pasūtījuma plūsmu caur uzdevumiem, ko pakalpojumu organizācijā veic dažādi cilvēki.</span><span class="sxs-lookup"><span data-stu-id="19d03-105">By defining the stages for a service order and assigning them to workers, you can control the flow of a service order through the tasks that various people perform in the service organization.</span></span> <span data-ttu-id="19d03-106">Stadiju secībā ir jābūt ietvertai sākotnējai stadijai.</span><span class="sxs-lookup"><span data-stu-id="19d03-106">The sequence of stages must include an initial stage.</span></span>

<span data-ttu-id="19d03-107">Varat arī noteikt darbības, kuras ir atļautas katrā stadijā.</span><span class="sxs-lookup"><span data-stu-id="19d03-107">You can also define the actions that are permitted at each stage.</span></span> <span data-ttu-id="19d03-108">Piemēram, ja noņemat atzīmi izvēles rūtiņai **Publicēt** visām stadijām, izņemot pēdējo, jūs novēršat iespēju, ka kāds no pakalpojuma pasūtījumiem tiks grāmatots pirms tam, kad šim pakalpojuma pasūtījumam ir izpildīta visa stadiju secība.</span><span class="sxs-lookup"><span data-stu-id="19d03-108">For example, if you clear the **Post** check box for all stages except the final stage, you prevent any service orders from being posted before the service orders are processed through the complete sequence of stages.</span></span>

## <a name="branching-in-service-order-stages"></a><span data-ttu-id="19d03-109">Zarošana pakalpojuma pasūtījuma stadijās</span><span class="sxs-lookup"><span data-stu-id="19d03-109">Branching in service order stages</span></span>

<span data-ttu-id="19d03-110">Iestatot pakalpojuma posmu, var izveidot vairākas opcijas vai zarus, lai tos atlasītu nākamajā pakalpojuma posmā.</span><span class="sxs-lookup"><span data-stu-id="19d03-110">When you set up a service stage, you can create multiple options, or branches, to select from for the next service stage.</span></span> <span data-ttu-id="19d03-111">Visus zarus, ko izveidojat, var atlasīt, kad ir pabeigts sākotnējais posms.</span><span class="sxs-lookup"><span data-stu-id="19d03-111">All the branches that you create are available to select from when the initial stage is completed.</span></span> <span data-ttu-id="19d03-112">Piemēram, kā sākotnējo posmu varat iestatīt **Plānošanu**.</span><span class="sxs-lookup"><span data-stu-id="19d03-112">For example, you set up **Planning** as an initial stage.</span></span> <span data-ttu-id="19d03-113">Izveidojiet divus posmus ar nosaukumu **Procesā** un **Atcelt** un pēc tam atlasiet tiem **Plānošanu** kā pamatposmu.</span><span class="sxs-lookup"><span data-stu-id="19d03-113">You create two stages named **In process** and **Cancel**, and then select **Planning** as the parent for them.</span></span> <span data-ttu-id="19d03-114">Piešķiriet **Plānošanas** posmu pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="19d03-114">You assign the **Planning** stage to sales order.</span></span> <span data-ttu-id="19d03-115">Ja plānošanas stadija pārdošanas pasūtījumam ir pabeigta, varat atlasīt posmu **Procesā**, ja pārdošanas pasūtījums ir gatavs darbam, vai atlasīt posmu **Atcelt**, ja pārdošanas pasūtījums ir atcelts.</span><span class="sxs-lookup"><span data-stu-id="19d03-115">When the planning stage for the sales order is completed, you can select the **In process** stage if the sales order is ready to work on, or you can select the **Cancel** stage if the sales order is canceled.</span></span>

## <a name="see-also"></a><span data-ttu-id="19d03-116">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="19d03-116">See also</span></span>

[<span data-ttu-id="19d03-117">Pakalpojuma pasūtījuma stadiju iestatīšana</span><span class="sxs-lookup"><span data-stu-id="19d03-117">Set up service order stages</span></span>](set-up-service-order-stages.md)

[<span data-ttu-id="19d03-118">Pakalpojuma pasūtījuma stadijas maiņa</span><span class="sxs-lookup"><span data-stu-id="19d03-118">Change the service order stage</span></span>](change-service-order-stage.md)

  


