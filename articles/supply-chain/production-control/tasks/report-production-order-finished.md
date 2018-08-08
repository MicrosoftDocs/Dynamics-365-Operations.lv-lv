---
title: "Ziņojums par ražošanas pasūtījuma pabeigšanu"
description: "Šajā procedūrā parādīts, kā ziņot ražošanas pasūtījumu kā pabeigtu."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 9c523350af46ffa1516ea42aa0328d4f24f57133
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---
# <a name="report-a-production-order-as-finished"></a><span data-ttu-id="05037-103">Ziņojums par ražošanas pasūtījuma pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="05037-103">Report a production order as finished</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="05037-104">Šajā procedūrā parādīts, kā ziņot ražošanas pasūtījumu kā pabeigtu.</span><span class="sxs-lookup"><span data-stu-id="05037-104">This procedure shows how to report a production order as finished.</span></span> <span data-ttu-id="05037-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="05037-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="05037-106">Šī ir sestā procedūra no septiņām, kurā ir paskaidrots ražošanas pasūtījuma dzīves cikls.</span><span class="sxs-lookup"><span data-stu-id="05037-106">This is the sixth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="report-a-production-order-as-finished"></a><span data-ttu-id="05037-107">Ziņojums par ražošanas pasūtījuma pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="05037-107">Report a production order as finished</span></span>
1. <span data-ttu-id="05037-108">Pārejiet uz sadaļu Ražošanas kontrole > Ražošanas pasūtījumi > Visi ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="05037-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="05037-109">Atlasiet ražošanas pasūtījumu, kura statuss ir Uzsākts.</span><span class="sxs-lookup"><span data-stu-id="05037-109">Select a production order that has the Started status.</span></span>  
2. <span data-ttu-id="05037-110">Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="05037-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="05037-111">Uzklikšķiniet Reģistrēt pabeigšanu.</span><span class="sxs-lookup"><span data-stu-id="05037-111">Click Report as finished.</span></span>
    * <span data-ttu-id="05037-112">Šajā lapā varat apstiprināt pabeigto preču daudzumu, kuras jānorāda kā pabeigtas.</span><span class="sxs-lookup"><span data-stu-id="05037-112">On this page, you can confirm the quantity of the finished product to be reported as finished.</span></span>  
4. <span data-ttu-id="05037-113">Noklikšķiniet uz cilnes Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="05037-113">Click the General tab.</span></span>
5. <span data-ttu-id="05037-114">Vienumam Derīgais daudzums iestatiet vērtību "18".</span><span class="sxs-lookup"><span data-stu-id="05037-114">Set Good quantity to '18'.</span></span>
6. <span data-ttu-id="05037-115">Vienumam Brāķa daudzums iestatiet vērtību "2".</span><span class="sxs-lookup"><span data-stu-id="05037-115">Set Error quantity to '2'.</span></span>
7. <span data-ttu-id="05037-116">Laukā Brāķa iemesls atlasiet vienumu Materiāls.</span><span class="sxs-lookup"><span data-stu-id="05037-116">In the Error cause field, select 'Material'.</span></span>
8. <span data-ttu-id="05037-117">Atzīmējiet izvēles rūtiņu Pēdējais darbs vai noņemiet tās atzīmi.</span><span class="sxs-lookup"><span data-stu-id="05037-117">Select or clear the End job check box.</span></span>
9. <span data-ttu-id="05037-118">Atzīmējiet izvēles rūtiņu Pieņemt kļūdu vai noņemiet tās atzīmi.</span><span class="sxs-lookup"><span data-stu-id="05037-118">Select or clear the Accept error check box.</span></span>
10. <span data-ttu-id="05037-119">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="05037-119">Click OK.</span></span>

## <a name="verify-the-report-as-finished-journal"></a><span data-ttu-id="05037-120">Pabeigšanas žurnāla pārbaude</span><span class="sxs-lookup"><span data-stu-id="05037-120">Verify the Report as finished journal</span></span>
1. <span data-ttu-id="05037-121">Darbību rūtī noklikšķiniet uz Skatīt.</span><span class="sxs-lookup"><span data-stu-id="05037-121">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="05037-122">Noklikšķiniet uz Ziņots kā pabeigts.</span><span class="sxs-lookup"><span data-stu-id="05037-122">Click Reported as finished.</span></span>
3. <span data-ttu-id="05037-123">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="05037-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="05037-124">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="05037-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="05037-125">Pabeigtās ražošanas žurnāls ir grāmatots.</span><span class="sxs-lookup"><span data-stu-id="05037-125">The Report as finished journal is posted.</span></span> <span data-ttu-id="05037-126">Ja vēlaties veikt korekcijas žurnālā, varat manuāli izveidot jaunu žurnālu, kurā varat veikt izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="05037-126">If you want to make adjustments to the journal, you can manually create  a new journal where you can make changes.</span></span>  

