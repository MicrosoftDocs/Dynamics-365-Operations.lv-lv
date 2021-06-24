---
title: 'Ceļvedis: Pieprasījuma apjoma prognozes manuāla modificēšana'
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
ms.openlocfilehash: 1e12ccf90b9971379e8931bd48d6243a855bb795
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224014"
---
# <a name="guide-modify-a-demand-forecast-manually"></a><span data-ttu-id="c3050-103">Ceļvedis: Pieprasījuma apjoma prognozes manuāla modificēšana</span><span class="sxs-lookup"><span data-stu-id="c3050-103">Guide: Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c3050-104">Šajā procedūrā parādīts, kā modificēt krājuma prognozi.</span><span class="sxs-lookup"><span data-stu-id="c3050-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="c3050-105">Šī procedūra ir paredzēta ražošanas plānotājam.</span><span class="sxs-lookup"><span data-stu-id="c3050-105">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="c3050-106">Atlasītā krājuma prognozes modificēšana</span><span class="sxs-lookup"><span data-stu-id="c3050-106">Modify the forecast for a selected item</span></span>

<span data-ttu-id="c3050-107">Lai mainītu atlasītā krājuma prognozi:</span><span class="sxs-lookup"><span data-stu-id="c3050-107">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="c3050-108">Pārejiet uz sadaļu **Moduļi \> Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="c3050-108">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="c3050-109">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c3050-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="c3050-110">Atlasiet krājumu, kuram vēlaties mainīt prognozi.</span><span class="sxs-lookup"><span data-stu-id="c3050-110">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="c3050-111">Darbību rūtī atveriet cilni **Plāns** un atlasiet **Pieprasījuma apjoma prognoze**.</span><span class="sxs-lookup"><span data-stu-id="c3050-111">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="c3050-112">Sarakstā atlasiet rindu.</span><span class="sxs-lookup"><span data-stu-id="c3050-112">In the list, select a row.</span></span> <span data-ttu-id="c3050-113">Ja nav nevienas prognožu rindas, izveidojiet jaunu rindu, darbību rūtī atlasot **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="c3050-113">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="c3050-114">Laukā **Pārdošanas daudzums** ievadiet pozitīvu skaitli.</span><span class="sxs-lookup"><span data-stu-id="c3050-114">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="c3050-115">Šis daudzums apzīmē krājuma prognozēto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="c3050-115">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="c3050-116">Ja ievadīsiet negatīvu skaitli, tiks parādīta kļūda.</span><span class="sxs-lookup"><span data-stu-id="c3050-116">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="c3050-117">Pēc vajadzības aizpildiet parējos laukus.</span><span class="sxs-lookup"><span data-stu-id="c3050-117">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="c3050-118">Atlasiet **Saglabāt** darbību rūtī.</span><span class="sxs-lookup"><span data-stu-id="c3050-118">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a><span data-ttu-id="c3050-119">Modificējiet prognozi vienam vai vairākiem krājumiem Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="c3050-119">Modify the forecast for one or more items with Microsoft Excel</span></span>

<span data-ttu-id="c3050-120">Lai modificētu prognozi vienam vai vairākiem krājumiem Microsoft Excel:</span><span class="sxs-lookup"><span data-stu-id="c3050-120">To modify the forecast for one or more items with Microsoft Excel:</span></span>

1. <span data-ttu-id="c3050-121">Veiciet vienu no tālāk norādītajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="c3050-121">Do one of the following:</span></span>
    - <span data-ttu-id="c3050-122">Atveriet lapu **Pieprasījuma apjoma prognoze** jebkuram krājumam (nav svarīgi kuram) kā aprakstīts iepriekšējā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="c3050-122">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="c3050-123">Dodieties uz **Vispārējā plānošana \> Prognozēšana \> Manuāls prognozes ieraksts \> Pieprasījuma apjoma prognozes rindas**.</span><span class="sxs-lookup"><span data-stu-id="c3050-123">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="c3050-124">Darbību rūtī atveriet **Atvērt Microsoft Office \> Pieprasījuma apjoma prognozes ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="c3050-124">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="c3050-125">Atlasiet lejupielādes vietu, saglabājiet un pēc tam atveriet lejupielādēto failu programmā Excel.</span><span class="sxs-lookup"><span data-stu-id="c3050-125">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="c3050-126">Ja ir redzams brīdinājums, izvēlieties **Iespējot rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="c3050-126">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="c3050-127">Programmā Excel piesakieties Supply Chain Management, izmantojot Microsoft Dynamics uzdevumrūti.</span><span class="sxs-lookup"><span data-stu-id="c3050-127">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="c3050-128">Ir jāpiesakās, ja opcija **Palikt pierakstītam** ir iespējota un jums ir jāuzticas datu savienojuma programmai.</span><span class="sxs-lookup"><span data-stu-id="c3050-128">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="c3050-129">Excel izklājlapa tagad rāda visas pašreizējās pieprasījuma apjoma prognozes rindas jūsu uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="c3050-129">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="c3050-130">Pēc nepieciešamības pievienojiet, dzēsiet un labojiet pieprasījuma prognozes rindas.</span><span class="sxs-lookup"><span data-stu-id="c3050-130">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="c3050-131">Atlasiet **Publicēt** pakalpojuma Microsoft Dynamics uzdevumrūtī, lai augšupielādētu izmaiņas atpakaļ Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c3050-131">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
