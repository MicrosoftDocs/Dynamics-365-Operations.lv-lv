---
title: Ziņojums par ražošanas pasūtījuma pabeigšanu
description: Šajā procedūrā parādīts, kā ziņot ražošanas pasūtījumu kā pabeigtu.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd, ProdSetupReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 93193e6365bcf82fbbf93af81e2581a358899fa1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432471"
---
# <a name="report-a-production-order-as-finished"></a><span data-ttu-id="043ed-103">Ziņojums par ražošanas pasūtījuma pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="043ed-103">Report a production order as finished</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="043ed-104">Šajā procedūrā parādīts, kā ziņot ražošanas pasūtījumu kā pabeigtu.</span><span class="sxs-lookup"><span data-stu-id="043ed-104">This procedure shows how to report a production order as finished.</span></span> <span data-ttu-id="043ed-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="043ed-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="043ed-106">Šī ir sestā procedūra no septiņām, kurā ir paskaidrots ražošanas pasūtījuma dzīves cikls.</span><span class="sxs-lookup"><span data-stu-id="043ed-106">This is the sixth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="report-a-production-order-as-finished"></a><span data-ttu-id="043ed-107">Ziņojums par ražošanas pasūtījuma pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="043ed-107">Report a production order as finished</span></span>
1. <span data-ttu-id="043ed-108">Pārejiet uz sadaļu Ražošanas kontrole > Ražošanas pasūtījumi > Visi ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="043ed-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="043ed-109">Atlasiet ražošanas pasūtījumu, kura statuss ir Uzsākts.</span><span class="sxs-lookup"><span data-stu-id="043ed-109">Select a production order that has the Started status.</span></span>  
2. <span data-ttu-id="043ed-110">Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="043ed-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="043ed-111">Uzklikšķiniet Reģistrēt pabeigšanu.</span><span class="sxs-lookup"><span data-stu-id="043ed-111">Click Report as finished.</span></span>
    * <span data-ttu-id="043ed-112">Šajā lapā varat apstiprināt pabeigto preču daudzumu, kuras jānorāda kā pabeigtas.</span><span class="sxs-lookup"><span data-stu-id="043ed-112">On this page, you can confirm the quantity of the finished product to be reported as finished.</span></span>  
4. <span data-ttu-id="043ed-113">Noklikšķiniet uz cilnes Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="043ed-113">Click the General tab.</span></span>
5. <span data-ttu-id="043ed-114">Vienumam Derīgais daudzums iestatiet vērtību "18".</span><span class="sxs-lookup"><span data-stu-id="043ed-114">Set Good quantity to '18'.</span></span>
6. <span data-ttu-id="043ed-115">Vienumam Brāķa daudzums iestatiet vērtību "2".</span><span class="sxs-lookup"><span data-stu-id="043ed-115">Set Error quantity to '2'.</span></span>
7. <span data-ttu-id="043ed-116">Laukā Brāķa iemesls atlasiet vienumu Materiāls.</span><span class="sxs-lookup"><span data-stu-id="043ed-116">In the Error cause field, select 'Material'.</span></span>
8. <span data-ttu-id="043ed-117">Atzīmējiet izvēles rūtiņu Pēdējais darbs vai noņemiet tās atzīmi.</span><span class="sxs-lookup"><span data-stu-id="043ed-117">Select or clear the End job check box.</span></span>
9. <span data-ttu-id="043ed-118">Atzīmējiet izvēles rūtiņu Pieņemt kļūdu vai noņemiet tās atzīmi.</span><span class="sxs-lookup"><span data-stu-id="043ed-118">Select or clear the Accept error check box.</span></span>
10. <span data-ttu-id="043ed-119">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="043ed-119">Click OK.</span></span>

## <a name="verify-the-report-as-finished-journal"></a><span data-ttu-id="043ed-120">Pabeigšanas žurnāla pārbaude</span><span class="sxs-lookup"><span data-stu-id="043ed-120">Verify the Report as finished journal</span></span>
1. <span data-ttu-id="043ed-121">Darbību rūtī noklikšķiniet uz Skatīt.</span><span class="sxs-lookup"><span data-stu-id="043ed-121">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="043ed-122">Noklikšķiniet uz Ziņots kā pabeigts.</span><span class="sxs-lookup"><span data-stu-id="043ed-122">Click Reported as finished.</span></span>
3. <span data-ttu-id="043ed-123">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="043ed-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="043ed-124">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="043ed-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="043ed-125">Pabeigtās ražošanas žurnāls ir grāmatots.</span><span class="sxs-lookup"><span data-stu-id="043ed-125">The Report as finished journal is posted.</span></span> <span data-ttu-id="043ed-126">Ja vēlaties veikt korekcijas žurnālā, varat manuāli izveidot jaunu žurnālu, kurā varat veikt izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="043ed-126">If you want to make adjustments to the journal, you can manually create  a new journal where you can make changes.</span></span>  

