---
title: Pieprasījuma prognozes manuāla modificēšana
description: Šajā procedūrā parādīts, kā modificēt krājuma prognozi.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ca6b881bc094b68d1bbf8c7c20b65418e42b28e3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835878"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="31e4f-103">Pieprasījuma prognozes manuāla modificēšana</span><span class="sxs-lookup"><span data-stu-id="31e4f-103">Modify a demand forecast manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="31e4f-104">Šajā procedūrā parādīts, kā modificēt krājuma prognozi.</span><span class="sxs-lookup"><span data-stu-id="31e4f-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="31e4f-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="31e4f-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="31e4f-106">Šis ieraksts ir paredzēts ražošanas plānotājam.</span><span class="sxs-lookup"><span data-stu-id="31e4f-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="31e4f-107">Krājuma prognozes modificēšana</span><span class="sxs-lookup"><span data-stu-id="31e4f-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="31e4f-108">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="31e4f-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="31e4f-109">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="31e4f-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="31e4f-110">Atlasiet krājumu, kuram vēlaties mainīt prognozi.</span><span class="sxs-lookup"><span data-stu-id="31e4f-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="31e4f-111">Piemēram, varat atlasīt krājumu D0001.</span><span class="sxs-lookup"><span data-stu-id="31e4f-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="31e4f-112">Darbību rūtī noklikšķiniet uz Plānot.</span><span class="sxs-lookup"><span data-stu-id="31e4f-112">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="31e4f-113">Noklikšķiniet uz Pieprasījuma apjoma prognoze.</span><span class="sxs-lookup"><span data-stu-id="31e4f-113">Click Demand forecast.</span></span>
5. <span data-ttu-id="31e4f-114">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="31e4f-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="31e4f-115">Ja nav budžeta rindu, izveidojiet jaunu rindu,</span><span class="sxs-lookup"><span data-stu-id="31e4f-115">If there are no forecast lines, create a new line by  .</span></span> <span data-ttu-id="31e4f-116">programmu joslā noklikšķinot uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="31e4f-116">clicking New on the app bar.</span></span>  
6. <span data-ttu-id="31e4f-117">Ierakstiet skaitli laukā Pārdošanas daudzums.</span><span class="sxs-lookup"><span data-stu-id="31e4f-117">In the Sales quantity field, enter a number.</span></span>
    * <span data-ttu-id="31e4f-118">Šis daudzums apzīmē krājuma prognozēto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="31e4f-118">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="31e4f-119">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="31e4f-119">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="31e4f-120">Prognozes modificēšana programmā Excel</span><span class="sxs-lookup"><span data-stu-id="31e4f-120">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="31e4f-121">Noklikšķiniet uz Atvērt, izmantojot Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="31e4f-121">Click Open in Microsoft Office.</span></span>
2. <span data-ttu-id="31e4f-122">Noklikšķiniet uz Pieprasījuma apjoma prognozes rediģēšana programmā Excel.</span><span class="sxs-lookup"><span data-stu-id="31e4f-122">Click Edit Demand forecast in Excel.</span></span>
    * <span data-ttu-id="31e4f-123">Programmā Excel varat pievienot, dzēst un rediģēt pieprasījuma prognozes rindas.</span><span class="sxs-lookup"><span data-stu-id="31e4f-123">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="31e4f-124">Ja nevarat redzēt datus programmā Excel, nepieciešams pierakstīties programmā Microsoft Dynamics 365 for Finance and Operations Enterprise edition ar iespējotu opciju “Neizrakstīties” un uzticēties datu savienojuma lietotnei.</span><span class="sxs-lookup"><span data-stu-id="31e4f-124">If you are not able to see the data in Excel, you need to sign in to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  

