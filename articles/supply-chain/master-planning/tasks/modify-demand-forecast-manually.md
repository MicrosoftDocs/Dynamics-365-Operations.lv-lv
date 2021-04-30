---
title: Pieprasījuma apjoma prognozes manuāla modificēšana
description: Šajā tēmā aprakstīts, kā modificēt krājuma prognozi
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5da1d5b1fbd91964e695a704681b1c9ee513a2f1
ms.sourcegitcommit: 4016c223a985c46e33f9941bf91ba5e1583e1cfd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889028"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="8fa59-103">Pieprasījuma apjoma prognozes manuāla modificēšana</span><span class="sxs-lookup"><span data-stu-id="8fa59-103">Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8fa59-104">Šajā procedūrā parādīts, kā modificēt krājuma prognozi.</span><span class="sxs-lookup"><span data-stu-id="8fa59-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="8fa59-105">USMF ir paraugdatu uzņēmums, kas tiek izmantots šīs procedūras izveidei.</span><span class="sxs-lookup"><span data-stu-id="8fa59-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8fa59-106">Šī procedūra ir paredzēta ražošanas plānotājam.</span><span class="sxs-lookup"><span data-stu-id="8fa59-106">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="8fa59-107">Atlasītā krājuma prognozes modificēšana</span><span class="sxs-lookup"><span data-stu-id="8fa59-107">Modify the forecast for a selected item</span></span>

<span data-ttu-id="8fa59-108">Lai mainītu atlasītā krājuma prognozi:</span><span class="sxs-lookup"><span data-stu-id="8fa59-108">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="8fa59-109">Pārejiet uz sadaļu **Moduļi \> Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="8fa59-109">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="8fa59-110">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="8fa59-110">In the list, find and select the desired record.</span></span> <span data-ttu-id="8fa59-111">Atlasiet krājumu, kuram vēlaties mainīt prognozi.</span><span class="sxs-lookup"><span data-stu-id="8fa59-111">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="8fa59-112">Darbību rūtī atveriet cilni **Plāns** un atlasiet **Pieprasījuma apjoma prognoze**.</span><span class="sxs-lookup"><span data-stu-id="8fa59-112">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="8fa59-113">Sarakstā atlasiet rindu.</span><span class="sxs-lookup"><span data-stu-id="8fa59-113">In the list, select a row.</span></span> <span data-ttu-id="8fa59-114">Ja nav nevienas prognožu rindas, izveidojiet jaunu rindu, darbību rūtī atlasot **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="8fa59-114">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="8fa59-115">Laukā **Pārdošanas daudzums** ievadiet pozitīvu skaitli.</span><span class="sxs-lookup"><span data-stu-id="8fa59-115">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="8fa59-116">Šis daudzums apzīmē krājuma prognozēto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="8fa59-116">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="8fa59-117">Ja ievadīsiet negatīvu skaitli, tiks parādīta kļūda.</span><span class="sxs-lookup"><span data-stu-id="8fa59-117">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="8fa59-118">Pēc vajadzības aizpildiet parējos laukus.</span><span class="sxs-lookup"><span data-stu-id="8fa59-118">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="8fa59-119">Atlasiet **Saglabāt** darbību rūtī.</span><span class="sxs-lookup"><span data-stu-id="8fa59-119">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-microsoft-excel"></a><span data-ttu-id="8fa59-120">Modificēt prognozi vienam vai vairākiem krājumiem Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="8fa59-120">Modify the forecast for one or more items Microsoft Excel</span></span>

<span data-ttu-id="8fa59-121">Lai modificētu prognozi vienam vai vairākiem krājumiem Microsoft Excel:</span><span class="sxs-lookup"><span data-stu-id="8fa59-121">To modify the forecast for one or more items Microsoft Excel:</span></span>

1. <span data-ttu-id="8fa59-122">Veiciet vienu no tālāk norādītajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="8fa59-122">Do one of the following:</span></span>
    - <span data-ttu-id="8fa59-123">Atveriet lapu **Pieprasījuma apjoma prognoze** jebkuram krājumam (nav svarīgi kuram) kā aprakstīts iepriekšējā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="8fa59-123">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="8fa59-124">Dodieties uz **Vispārējā plānošana \> Prognozēšana \> Manuāls prognozes ieraksts \> Pieprasījuma apjoma prognozes rindas**.</span><span class="sxs-lookup"><span data-stu-id="8fa59-124">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="8fa59-125">Darbību rūtī atveriet **Atvērt Microsoft Office \> Pieprasījuma apjoma prognozes ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="8fa59-125">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="8fa59-126">Atlasiet lejupielādes vietu, saglabājiet un pēc tam atveriet lejupielādēto failu programmā Excel.</span><span class="sxs-lookup"><span data-stu-id="8fa59-126">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="8fa59-127">Ja ir redzams brīdinājums, izvēlieties **Iespējot rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="8fa59-127">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="8fa59-128">Programmā Excel piesakieties Supply Chain Management, izmantojot Microsoft Dynamics uzdevumrūti.</span><span class="sxs-lookup"><span data-stu-id="8fa59-128">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="8fa59-129">Ir jāpiesakās, ja opcija **Palikt pierakstītam** ir iespējota un jums ir jāuzticas datu savienojuma programmai.</span><span class="sxs-lookup"><span data-stu-id="8fa59-129">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="8fa59-130">Excel izklājlapa tagad rāda visas pašreizējās pieprasījuma apjoma prognozes rindas jūsu uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="8fa59-130">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="8fa59-131">Pēc nepieciešamības pievienojiet, dzēsiet un labojiet pieprasījuma prognozes rindas.</span><span class="sxs-lookup"><span data-stu-id="8fa59-131">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="8fa59-132">Atlasiet **Publicēt** pakalpojuma Microsoft Dynamics uzdevumrūtī, lai augšupielādētu izmaiņas atpakaļ Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8fa59-132">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
