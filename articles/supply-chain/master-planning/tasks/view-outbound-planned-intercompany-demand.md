---
title: Izejošo plānoto starpuzņēmumu pieprasījuma skatīšana
description: Šī procedūra parāda, kā skatīt visus plānotos pasūtījumus, kurus izpildīs starpuzņēmuma kreditors.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1bc3addb11d77a5098e80a5826bfea289d232548
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254291"
---
# <a name="view-outbound-planned-intercompany-demand"></a><span data-ttu-id="99dc8-103">Izejošo plānoto starpuzņēmumu pieprasījuma skatīšana</span><span class="sxs-lookup"><span data-stu-id="99dc8-103">View outbound planned intercompany demand</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="99dc8-104">Šī procedūra parāda, kā skatīt visus plānotos pasūtījumus, kurus izpildīs starpuzņēmuma kreditors.</span><span class="sxs-lookup"><span data-stu-id="99dc8-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="99dc8-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir DEMF.</span><span class="sxs-lookup"><span data-stu-id="99dc8-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="99dc8-106">Noklikšķiniet uz Vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="99dc8-106">Click Master planning.</span></span>
2. <span data-ttu-id="99dc8-107">Laukā Plāns ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="99dc8-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="99dc8-108">Laukā Plāns, atlasiet plānot 10.</span><span class="sxs-lookup"><span data-stu-id="99dc8-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="99dc8-109">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="99dc8-109">Click Run.</span></span>
4. <span data-ttu-id="99dc8-110">Laukā Pavedienu skaits ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="99dc8-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="99dc8-111">Tas norāda, cik paralēlu pavedienu tiks izmantots vispārējā plānošanā.</span><span class="sxs-lookup"><span data-stu-id="99dc8-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="99dc8-112">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="99dc8-112">Click OK.</span></span>
    * <span data-ttu-id="99dc8-113">Tas var aizņemt kādu laiku.</span><span class="sxs-lookup"><span data-stu-id="99dc8-113">This may take a while.</span></span>  
6. <span data-ttu-id="99dc8-114">Noklikšķiniet uz plānotais starpuzņēmumu pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="99dc8-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="99dc8-115">Noklikšķiniet uz izejošo plānoto starpuzņēmumu pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="99dc8-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="99dc8-116">Šī lapa sniedz pārskatu par visiem plānotajiem pieprasījumiem, kas izpildīs iekšējās piegādes ķēdes kreditors.</span><span class="sxs-lookup"><span data-stu-id="99dc8-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="99dc8-117">Izvērsiet sadaļu augšpus pieprasījuma detaļas.</span><span class="sxs-lookup"><span data-stu-id="99dc8-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="99dc8-118">Šajā sadaļā jūs varat skatīt detalizētu informāciju par to, kā tiks izpildīts pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="99dc8-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="99dc8-119">Iespējams, būs jāgaida, līdz piegādes uzņēmumā tiek veikta vispārējā plānošana, pirms jūs varat skatīt papildu informāciju šeit.</span><span class="sxs-lookup"><span data-stu-id="99dc8-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]