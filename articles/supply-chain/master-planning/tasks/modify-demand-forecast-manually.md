---
title: Pieprasījuma prognozes manuāla modificēšana
description: Šajā procedūrā parādīts, kā modificēt krājuma prognozi.
author: ShylaThompson
manager: AnnBe
ms.date: 08/12/2019
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
ms.openlocfilehash: 1ec1edb861619bae2ae3c211720b55e170b83ec9
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916626"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="18102-103">Pieprasījuma prognozes manuāla modificēšana</span><span class="sxs-lookup"><span data-stu-id="18102-103">Modify a demand forecast manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="18102-104">Šajā procedūrā parādīts, kā modificēt krājuma prognozi.</span><span class="sxs-lookup"><span data-stu-id="18102-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="18102-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="18102-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="18102-106">Šis ieraksts ir paredzēts ražošanas plānotājam.</span><span class="sxs-lookup"><span data-stu-id="18102-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="18102-107">Krājuma prognozes modificēšana</span><span class="sxs-lookup"><span data-stu-id="18102-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="18102-108">**Navigācijas rūtī** pārejiet uz sadaļu **Moduļi > Preču informācijas pārvaldība > Preces > Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="18102-108">In the **Navigation pane**, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="18102-109">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="18102-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="18102-110">Atlasiet krājumu, kuram vēlaties mainīt prognozi.</span><span class="sxs-lookup"><span data-stu-id="18102-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="18102-111">Piemēram, varat atlasīt krājumu D0001.</span><span class="sxs-lookup"><span data-stu-id="18102-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="18102-112">**Darbību rūtī** noklikšķiniet uz **Plāns**.</span><span class="sxs-lookup"><span data-stu-id="18102-112">On the **Action Pane**, click **Plan**.</span></span>
4. <span data-ttu-id="18102-113">Noklikšķiniet uz **Pieprasīt prognozi**.</span><span class="sxs-lookup"><span data-stu-id="18102-113">Click **Demand forecast**.</span></span>
5. <span data-ttu-id="18102-114">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="18102-114">In the list, mark the selected row.</span></span> <span data-ttu-id="18102-115">Ja nav nevienas prognožu rindas, izveidojiet jaunu rindu, lietojumprogrammas joslā noklikšķinot uz Jauna.</span><span class="sxs-lookup"><span data-stu-id="18102-115">If there are no forecast lines, create a new line by clicking New on the app bar.</span></span>  
6. <span data-ttu-id="18102-116">Laukā **Pārdošanas daudzums** ievadiet skaitu.</span><span class="sxs-lookup"><span data-stu-id="18102-116">In the **Sales quantity** field, enter a number.</span></span> <span data-ttu-id="18102-117">Šis daudzums apzīmē krājuma prognozēto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="18102-117">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="18102-118">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="18102-118">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="18102-119">Prognozes modificēšana programmā Excel</span><span class="sxs-lookup"><span data-stu-id="18102-119">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="18102-120">Programmā Microsoft Office noklikšķiniet uz **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="18102-120">Click **Open** in Microsoft Office.</span></span>
2. <span data-ttu-id="18102-121">Programmā Excel noklikšķiniet uz **Rediģēt pieprasījuma prognozi**.</span><span class="sxs-lookup"><span data-stu-id="18102-121">Click **Edit Demand forecast** in Excel.</span></span> <span data-ttu-id="18102-122">Programmā Excel varat pievienot, dzēst un rediģēt pieprasījuma prognozes rindas.</span><span class="sxs-lookup"><span data-stu-id="18102-122">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="18102-123">Ja nevarat redzēt datus programmā Excel, nepieciešams pierakstīties programmā Microsoft Dynamics 365 for Finance and Operations Enterprise edition ar iespējotu opciju “Neizrakstīties” un uzticēties datu savienojuma lietotnei.</span><span class="sxs-lookup"><span data-stu-id="18102-123">If you are not able to see the data in Excel, you need to sign in to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  

