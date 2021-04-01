---
title: Vēsturisko datu importēšana pieprasījuma apjoma prognozēm
description: Lai iegūtu precīzas pieprasījuma apjoma prognozes, ir nepieciešami vēsturiskie pieprasījuma dati pa krājumiem vai krājumu sadalījuma principiem. šajā tēmā ir izskaidrots, kā izmantot datu elementus, lai importētu vēsturiskos pieprasījuma datus no jebkuras sistēmas, tādējādi iegūstot vēsturiskos pieprasījuma datus par ilgāku periodu.
author: roxanadiaconu
manager: tfehr
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d415895bd05b9ab1a2311ab69cc3757047df91db
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204620"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="b6660-104">Vēsturisko datu importēšana pieprasījuma apjoma prognozēm</span><span class="sxs-lookup"><span data-stu-id="b6660-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6660-105">Lai palīdzētu nodrošināt pieprasījuma apjoma prognozes precizitāti, ir jāizmanto pēc iespējas vairāk vēsturisko pieprasījuma datu pa krājumiem vai krājumu sadalījuma principiem.</span><span class="sxs-lookup"><span data-stu-id="b6660-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="b6660-106">Ja vēsturiskie pieprasījuma dati vēl nav importēti, importējiet tos, izmantojot Dynamics 365 Supply Chain Management datu elementu **Vēsturisks ārējs pieprasījums** (ReqDemPlanHistoricalExternalDemandEntity).</span><span class="sxs-lookup"><span data-stu-id="b6660-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="b6660-107">Darbvietā **Datu pārvaldība** ir redzams pārskats par visiem entītijas laukiem.</span><span class="sxs-lookup"><span data-stu-id="b6660-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="b6660-108">Atveriet darbvietu **Datu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="b6660-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="b6660-109">Noklikšķiniet uz elementa **Datu elementi**.</span><span class="sxs-lookup"><span data-stu-id="b6660-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="b6660-110">Elementu sarakstā meklējiet elementu **Vēsturisks ārējs pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="b6660-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="b6660-111">Atlasiet **Mērķa laukus**.</span><span class="sxs-lookup"><span data-stu-id="b6660-111">Select **Target fields**.</span></span> <span data-ttu-id="b6660-112">Šie elementu lauki ir obligāti: vieta (**DeliveringSiteId**), datums (**DemandDate**), daudzums (**DemandQuantity**) un krājuma numurs (**ItemNumber**) vai krājuma sadalījuma princips (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="b6660-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="b6660-113">Lai izmantotu datu elementu, ir nepieciešams Microsoft Excel fails vai komatatdalīto vērtību (CSV) fails, kurā ir ietverti vēsturiskie pieprasījuma dati.</span><span class="sxs-lookup"><span data-stu-id="b6660-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="b6660-114">Tālāk esošajā piemērā ir aprakstīts, kā importēt datus no CSV faila.</span><span class="sxs-lookup"><span data-stu-id="b6660-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="b6660-115">Papildinformāciju par to, kā importēt datus, tostarp to, kā iztīrīt datus pēc importēšanas, skatiet [Datu importēšanas un eksportēšanas darbu pārskats](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) un ar to saistītās tēmas.</span><span class="sxs-lookup"><span data-stu-id="b6660-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

## <a name="example"></a><span data-ttu-id="b6660-116">Paraugs</span><span class="sxs-lookup"><span data-stu-id="b6660-116">Example</span></span>

<span data-ttu-id="b6660-117">Kā paraugu varat izmantot tālāk pieejamo failu.</span><span class="sxs-lookup"><span data-stu-id="b6660-117">You can use the following file as an example.</span></span> <span data-ttu-id="b6660-118">Lejupielādējiet failu [HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/).</span><span class="sxs-lookup"><span data-stu-id="b6660-118">Download the [HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/).</span></span> <span data-ttu-id="b6660-119">Šajā failā ir ietverti vēsturiskie pieprasījuma dati par krājumu D0001.</span><span class="sxs-lookup"><span data-stu-id="b6660-119">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="b6660-120">Tajā ir ietverti tikai šādi obligātie lauki: vieta, daudzums un pieprasījuma datums.</span><span class="sxs-lookup"><span data-stu-id="b6660-120">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="b6660-121">Atlasiet uzņēmumu, kurā ir jāimportē vēsturiskie pieprasījuma dati.</span><span class="sxs-lookup"><span data-stu-id="b6660-121">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="b6660-122">Atveriet darbvietu **Datu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="b6660-122">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="b6660-123">Atlasiet elementu **Imports**.</span><span class="sxs-lookup"><span data-stu-id="b6660-123">Select the **Import** tile.</span></span>
4. <span data-ttu-id="b6660-124">Ievadiet importēšanas projekta nosaukumu, piemēram, **Importētie krājuma D0001 vēsturiskie pieprasījuma dati**.</span><span class="sxs-lookup"><span data-stu-id="b6660-124">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="b6660-125">Laukā **Avota datu formāts** atlasiet importētā faila formātu.</span><span class="sxs-lookup"><span data-stu-id="b6660-125">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="b6660-126">Lai importētu šī piemēra ietveros lietoto failu HistoricalDemandData, atlasiet **CSV**.</span><span class="sxs-lookup"><span data-stu-id="b6660-126">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="b6660-127">Laukā **Elementa nosaukums** atlasiet **Vēsturisks ārējs pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="b6660-127">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="b6660-128">Saglabājiet failu datorā un pēc tam augšupielādējiet to.</span><span class="sxs-lookup"><span data-stu-id="b6660-128">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="b6660-129">Atlasiet **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="b6660-129">Select **Import**.</span></span>
9. <span data-ttu-id="b6660-130">Tiek automātiski atvērta lapa **Izpildes kopsavilkums**.</span><span class="sxs-lookup"><span data-stu-id="b6660-130">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="b6660-131">Pārbaudiet importētos datus šajā lapā.</span><span class="sxs-lookup"><span data-stu-id="b6660-131">Verify the imported data on the page.</span></span>

<span data-ttu-id="b6660-132">Pēc vēsturisko pieprasījuma datu importēšanas varat ģenerēt pieprasījuma apjoma prognozi.</span><span class="sxs-lookup"><span data-stu-id="b6660-132">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b6660-133">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="b6660-133">Additional resources</span></span>

[<span data-ttu-id="b6660-134">Statistiskās bāzlīnijas prognozes ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="b6660-134">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)  
[<span data-ttu-id="b6660-135">Datu importēšanas un eksportēšanas darbu pārskats</span><span class="sxs-lookup"><span data-stu-id="b6660-135">Data import and export jobs overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]