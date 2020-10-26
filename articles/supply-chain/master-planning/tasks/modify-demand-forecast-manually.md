---
title: Pieprasījuma prognozes manuāla modificēšana
description: Šajā procedūrā parādīts, kā modificēt krājuma prognozi.
author: ShylaThompson
manager: tfehr
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 105cf50698889e81804155cdac3a8b484cbf87d7
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3987170"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="802ce-103">Pieprasījuma prognozes manuāla modificēšana</span><span class="sxs-lookup"><span data-stu-id="802ce-103">Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="802ce-104">Šajā procedūrā parādīts, kā modificēt krājuma prognozi.</span><span class="sxs-lookup"><span data-stu-id="802ce-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="802ce-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="802ce-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="802ce-106">Šis ieraksts ir paredzēts ražošanas plānotājam.</span><span class="sxs-lookup"><span data-stu-id="802ce-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="802ce-107">Krājuma prognozes modificēšana</span><span class="sxs-lookup"><span data-stu-id="802ce-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="802ce-108">**Navigācijas rūtī** pārejiet uz sadaļu **Moduļi > Preču informācijas pārvaldība > Preces > Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="802ce-108">In the **Navigation pane**, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="802ce-109">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="802ce-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="802ce-110">Atlasiet krājumu, kuram vēlaties mainīt prognozi.</span><span class="sxs-lookup"><span data-stu-id="802ce-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="802ce-111">Piemēram, varat atlasīt krājumu D0001.</span><span class="sxs-lookup"><span data-stu-id="802ce-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="802ce-112">**Darbību rūtī** noklikšķiniet uz **Plāns**.</span><span class="sxs-lookup"><span data-stu-id="802ce-112">On the **Action Pane**, click **Plan**.</span></span>
4. <span data-ttu-id="802ce-113">Noklikšķiniet uz **Pieprasīt prognozi**.</span><span class="sxs-lookup"><span data-stu-id="802ce-113">Click **Demand forecast**.</span></span>
5. <span data-ttu-id="802ce-114">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="802ce-114">In the list, mark the selected row.</span></span> <span data-ttu-id="802ce-115">Ja nav nevienas prognožu rindas, izveidojiet jaunu rindu, lietojumprogrammas joslā noklikšķinot uz Jauna.</span><span class="sxs-lookup"><span data-stu-id="802ce-115">If there are no forecast lines, create a new line by clicking New on the app bar.</span></span>  
6. <span data-ttu-id="802ce-116">Laukā **Pārdošanas daudzums** ievadiet skaitu.</span><span class="sxs-lookup"><span data-stu-id="802ce-116">In the **Sales quantity** field, enter a number.</span></span> <span data-ttu-id="802ce-117">Šis daudzums apzīmē krājuma prognozēto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="802ce-117">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="802ce-118">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="802ce-118">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="802ce-119">Prognozes modificēšana programmā Excel</span><span class="sxs-lookup"><span data-stu-id="802ce-119">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="802ce-120">Programmā Microsoft Office noklikšķiniet uz **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="802ce-120">Click **Open** in Microsoft Office.</span></span>
2. <span data-ttu-id="802ce-121">Programmā Excel noklikšķiniet uz **Rediģēt pieprasījuma prognozi**.</span><span class="sxs-lookup"><span data-stu-id="802ce-121">Click **Edit Demand forecast** in Excel.</span></span> <span data-ttu-id="802ce-122">Programmā Excel varat pievienot, dzēst un rediģēt pieprasījuma prognozes rindas.</span><span class="sxs-lookup"><span data-stu-id="802ce-122">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="802ce-123">Ja nevarat redzēt datus programmā Excel, nepieciešams pierakstīties ar iespējotu opciju "Neizrakstīties" un uzticēties datu savienojuma lietotnei.</span><span class="sxs-lookup"><span data-stu-id="802ce-123">If you are not able to see the data in Excel, you need to sign in with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  

