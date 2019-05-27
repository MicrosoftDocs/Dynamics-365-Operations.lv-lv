---
title: Sadarbība ar iekšējās piegādes ķēdes debitoriem
description: Šī procedūra parāda, kā skatīt visus plānotos pasūtījumus, kurus izpildīs starpuzņēmuma kreditors.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44b9f516835acc792ec1edba0b5efdcbd2823422
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561229"
---
# <a name="collaborate-with-internal-supply-chain-customers"></a><span data-ttu-id="ba2fe-103">Sadarbība ar iekšējās piegādes ķēdes debitoriem</span><span class="sxs-lookup"><span data-stu-id="ba2fe-103">Collaborate with internal supply chain customers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ba2fe-104">Šī procedūra parāda, kā skatīt visus plānotos pasūtījumus, kurus izpildīs starpuzņēmuma kreditors.</span><span class="sxs-lookup"><span data-stu-id="ba2fe-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="ba2fe-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir DEMF.</span><span class="sxs-lookup"><span data-stu-id="ba2fe-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="ba2fe-106">Noklikšķiniet uz Vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="ba2fe-106">Click Master planning.</span></span>
2. <span data-ttu-id="ba2fe-107">Laukā Plāns ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ba2fe-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="ba2fe-108">Laukā Plāns, atlasiet plānot 10.</span><span class="sxs-lookup"><span data-stu-id="ba2fe-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="ba2fe-109">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="ba2fe-109">Click Run.</span></span>
4. <span data-ttu-id="ba2fe-110">Laukā Pavedienu skaits ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="ba2fe-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="ba2fe-111">Tas norāda, cik paralēlu pavedienu tiks izmantots vispārējā plānošanā.</span><span class="sxs-lookup"><span data-stu-id="ba2fe-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="ba2fe-112">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ba2fe-112">Click OK.</span></span>
    * <span data-ttu-id="ba2fe-113">Tas var aizņemt kādu laiku.</span><span class="sxs-lookup"><span data-stu-id="ba2fe-113">This may take a while.</span></span>  
6. <span data-ttu-id="ba2fe-114">Noklikšķiniet uz plānotais starpuzņēmumu pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="ba2fe-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="ba2fe-115">Noklikšķiniet uz izejošo plānoto starpuzņēmumu pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="ba2fe-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="ba2fe-116">Šī lapa sniedz pārskatu par visiem plānotajiem pieprasījumiem, kas izpildīs iekšējās piegādes ķēdes kreditors.</span><span class="sxs-lookup"><span data-stu-id="ba2fe-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="ba2fe-117">Izvērsiet sadaļu augšpus pieprasījuma detaļas.</span><span class="sxs-lookup"><span data-stu-id="ba2fe-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="ba2fe-118">Šajā sadaļā jūs varat skatīt detalizētu informāciju par to, kā tiks izpildīts pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="ba2fe-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="ba2fe-119">Iespējams, būs jāgaida, līdz piegādes uzņēmumā tiek veikta vispārējā plānošana, pirms jūs varat skatīt papildu informāciju šeit.</span><span class="sxs-lookup"><span data-stu-id="ba2fe-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

