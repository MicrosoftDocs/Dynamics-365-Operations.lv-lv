---
title: Ražošanas pasūtījuma novērtējums
description: Šo procedūru var izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savu datu kopu.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8274e390a177f51649f5cad70ef7ad5bd50a8830
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558483"
---
# <a name="estimate-a-production-order"></a><span data-ttu-id="52ee2-103">Ražošanas pasūtījuma novērtējums</span><span class="sxs-lookup"><span data-stu-id="52ee2-103">Estimate a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="52ee2-104">Šo procedūru var izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savu datu kopu.</span><span class="sxs-lookup"><span data-stu-id="52ee2-104">You can run this procedure by using the USMF demo data company or your own data set.</span></span> <span data-ttu-id="52ee2-105">Abos gadījumos jums ir jābūt atvērtam ražošanas pasūtījumam, kam ir statuss Izveidots.</span><span class="sxs-lookup"><span data-stu-id="52ee2-105">In both cases, you need to have an open production order that has the Created status.</span></span> <span data-ttu-id="52ee2-106">Šī ir otrā procedūra no septiņām, kurā ir paskaidrots ražošanas pasūtījuma dzīves cikls.</span><span class="sxs-lookup"><span data-stu-id="52ee2-106">This is the second procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="estimate-a-production-order"></a><span data-ttu-id="52ee2-107">Ražošanas pasūtījuma novērtējums</span><span class="sxs-lookup"><span data-stu-id="52ee2-107">Estimate a production order</span></span>
1. <span data-ttu-id="52ee2-108">Pārejiet uz sadaļu Ražošanas kontrole > Ražošanas pasūtījumi > Visi ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="52ee2-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="52ee2-109">Atlasiet pasūtījumu, kura statuss režģī ir Izveidots.</span><span class="sxs-lookup"><span data-stu-id="52ee2-109">Select an order that has the Created status in the grid.</span></span>
3. <span data-ttu-id="52ee2-110">Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="52ee2-110">On the Action Pane, click Production order.</span></span>
4. <span data-ttu-id="52ee2-111">Noklikšķiniet uz Novērtējums.</span><span class="sxs-lookup"><span data-stu-id="52ee2-111">Click Estimate.</span></span>
    * <span data-ttu-id="52ee2-112">Šajā darbībā tiek aprēķinātas viena ražošanas pasūtījuma novērtētās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="52ee2-112">In this step, the estimated costs of a single production order is calculated.</span></span>   
5. <span data-ttu-id="52ee2-113">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="52ee2-113">Click OK.</span></span>

## <a name="view-the-calculation-details"></a><span data-ttu-id="52ee2-114">Detalizētas informācijas par aprēķinu skatīšana</span><span class="sxs-lookup"><span data-stu-id="52ee2-114">View the calculation details</span></span>
1. <span data-ttu-id="52ee2-115">Darbību rūtī noklikšķiniet uz Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="52ee2-115">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="52ee2-116">Noklikšķiniet uz Skatīt detalizētu informāciju par aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="52ee2-116">Click View calculation details.</span></span>
    * <span data-ttu-id="52ee2-117">Šajā lapā parādīts izmaksu sadalījums.</span><span class="sxs-lookup"><span data-stu-id="52ee2-117">This page displays the cost breakdown.</span></span> <span data-ttu-id="52ee2-118">Piemēram, pirmajā rindā var apskatīt pabeigtās preces vienības kopējo izmaksu cenu.</span><span class="sxs-lookup"><span data-stu-id="52ee2-118">For example, you can view the total cost price per unit for the finished product in the first row.</span></span> <span data-ttu-id="52ee2-119">Sekojošās rindās ir izmaksas atbilstoši materiālu komplektam, ražošanas maršrutam un netiešām izmaksām.</span><span class="sxs-lookup"><span data-stu-id="52ee2-119">The subsequent rows contain costs according to the bill of materials, production route, and indirect costs.</span></span>  
