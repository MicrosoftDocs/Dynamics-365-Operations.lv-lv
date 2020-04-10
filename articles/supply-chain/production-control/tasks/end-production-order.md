---
title: Ražošanas pasūtījuma pārtraukšana
description: Šajā procedūrā ir parādīts, kā pabeigt ražošanas pasūtījumu.
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
ms.openlocfilehash: cb84d3b1908d6be889a49f7386de876cb52141ab
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149048"
---
# <a name="end-a-production-order"></a><span data-ttu-id="01d3b-103">Ražošanas pasūtījuma pārtraukšana</span><span class="sxs-lookup"><span data-stu-id="01d3b-103">End a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="01d3b-104">Šajā procedūrā ir parādīts, kā pabeigt ražošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="01d3b-104">This procedure shows how to end a production order.</span></span> <span data-ttu-id="01d3b-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="01d3b-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="01d3b-106">Šī ir pēdējā procedūra no septiņām, kurā ir paskaidrots ražošanas pasūtījuma dzīves cikls.</span><span class="sxs-lookup"><span data-stu-id="01d3b-106">This is the final procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="end-a-production-order"></a><span data-ttu-id="01d3b-107">Ražošanas pasūtījuma pārtraukšana</span><span class="sxs-lookup"><span data-stu-id="01d3b-107">End a production order</span></span>
1. <span data-ttu-id="01d3b-108">Pārejiet uz sadaļu Ražošanas kontrole > Ražošanas pasūtījumi > Visi ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="01d3b-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="01d3b-109">Atlasiet ražošanas pasūtījumu, kuram ir statuss Ziņots kā pabeigts.</span><span class="sxs-lookup"><span data-stu-id="01d3b-109">Select a production order that has the status Reported as finished.</span></span>  
2. <span data-ttu-id="01d3b-110">Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="01d3b-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="01d3b-111">Noklikšķiniet uz Beigt.</span><span class="sxs-lookup"><span data-stu-id="01d3b-111">Click End.</span></span>
    * <span data-ttu-id="01d3b-112">Šajā lapā var apstiprināt, ka vēlaties pabeigt ražošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="01d3b-112">On this page, you can confirm that you want to end the production order.</span></span>  
4. <span data-ttu-id="01d3b-113">Noklikšķiniet uz cilnes Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="01d3b-113">Click the General tab.</span></span>
5. <span data-ttu-id="01d3b-114">Laukā Datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="01d3b-114">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="01d3b-115">Laukā Brāķa metode atlasiet "Sadalījums".</span><span class="sxs-lookup"><span data-stu-id="01d3b-115">In the Scrap method field, select 'Allocation'.</span></span>
    * <span data-ttu-id="01d3b-116">Atlasot Sadalījuma metodi, izmaksas no norakstītajiem materiāliem tiek pievienotas pabeigtām precēm.</span><span class="sxs-lookup"><span data-stu-id="01d3b-116">When you select the Allocation method, costs from the scrapped materials are added to the finished goods.</span></span>  
7. <span data-ttu-id="01d3b-117">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="01d3b-117">Click OK.</span></span>

## <a name="validate-calculation-results"></a><span data-ttu-id="01d3b-118">Aprēķina rezultātu pārbaude</span><span class="sxs-lookup"><span data-stu-id="01d3b-118">Validate calculation results</span></span>
1. <span data-ttu-id="01d3b-119">Darbību rūtī noklikšķiniet uz Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="01d3b-119">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="01d3b-120">Noklikšķiniet uz Skatīt izmaksu salīdzinājumu.</span><span class="sxs-lookup"><span data-stu-id="01d3b-120">Click View cost comparison.</span></span>
    * <span data-ttu-id="01d3b-121">Pēc ražošanas pasūtījuma pabeigšanas var salīdzināt novērtēto izmaksu cenu ar realizēto izmaksu cenu, lai iegūtu pārskatu par ražošanas novirzēm.</span><span class="sxs-lookup"><span data-stu-id="01d3b-121">After you have ended the production order, you can compare the estimated cost price against the realized cost price to get an overview of the production variances.</span></span>  
