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
ms.openlocfilehash: f97cccc0d27d1154d8f8cb5018cf5040efcf190a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001778"
---
# <a name="view-outbound-planned-intercompany-demand"></a><span data-ttu-id="93e4b-103">Izejošo plānoto starpuzņēmumu pieprasījuma skatīšana</span><span class="sxs-lookup"><span data-stu-id="93e4b-103">View outbound planned intercompany demand</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="93e4b-104">Šī procedūra parāda, kā skatīt visus plānotos pasūtījumus, kurus izpildīs starpuzņēmuma kreditors.</span><span class="sxs-lookup"><span data-stu-id="93e4b-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="93e4b-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir DEMF.</span><span class="sxs-lookup"><span data-stu-id="93e4b-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="93e4b-106">Noklikšķiniet uz Vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="93e4b-106">Click Master planning.</span></span>
2. <span data-ttu-id="93e4b-107">Laukā Plāns ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="93e4b-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="93e4b-108">Laukā Plāns, atlasiet plānot 10.</span><span class="sxs-lookup"><span data-stu-id="93e4b-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="93e4b-109">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="93e4b-109">Click Run.</span></span>
4. <span data-ttu-id="93e4b-110">Laukā Pavedienu skaits ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="93e4b-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="93e4b-111">Tas norāda, cik paralēlu pavedienu tiks izmantots vispārējā plānošanā.</span><span class="sxs-lookup"><span data-stu-id="93e4b-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="93e4b-112">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="93e4b-112">Click OK.</span></span>
    * <span data-ttu-id="93e4b-113">Tas var aizņemt kādu laiku.</span><span class="sxs-lookup"><span data-stu-id="93e4b-113">This may take a while.</span></span>  
6. <span data-ttu-id="93e4b-114">Noklikšķiniet uz plānotais starpuzņēmumu pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="93e4b-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="93e4b-115">Noklikšķiniet uz izejošo plānoto starpuzņēmumu pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="93e4b-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="93e4b-116">Šī lapa sniedz pārskatu par visiem plānotajiem pieprasījumiem, kas izpildīs iekšējās piegādes ķēdes kreditors.</span><span class="sxs-lookup"><span data-stu-id="93e4b-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="93e4b-117">Izvērsiet sadaļu augšpus pieprasījuma detaļas.</span><span class="sxs-lookup"><span data-stu-id="93e4b-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="93e4b-118">Šajā sadaļā jūs varat skatīt detalizētu informāciju par to, kā tiks izpildīts pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="93e4b-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="93e4b-119">Iespējams, būs jāgaida, līdz piegādes uzņēmumā tiek veikta vispārējā plānošana, pirms jūs varat skatīt papildu informāciju šeit.</span><span class="sxs-lookup"><span data-stu-id="93e4b-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

