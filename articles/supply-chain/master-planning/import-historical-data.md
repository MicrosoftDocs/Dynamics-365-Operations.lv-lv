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
ms.search.scope: Core, Operations
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97e84b478b8fd65313d8c3be5c9a50756d8b4924
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213848"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="f2d9a-104">Vēsturisko datu importēšana pieprasījuma apjoma prognozēm</span><span class="sxs-lookup"><span data-stu-id="f2d9a-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2d9a-105">Lai palīdzētu nodrošināt pieprasījuma apjoma prognozes precizitāti, ir jāizmanto pēc iespējas vairāk vēsturisko pieprasījuma datu pa krājumiem vai krājumu sadalījuma principiem.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="f2d9a-106">Ja vēsturiskie pieprasījuma dati vēl nav importēti, importējiet tos, izmantojot Dynamics 365 Supply Chain Management datu elementu **Vēsturisks ārējs pieprasījums** (ReqDemPlanHistoricalExternalDemandEntity).</span><span class="sxs-lookup"><span data-stu-id="f2d9a-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="f2d9a-107">Darbvietā **Datu pārvaldība** ir redzams pārskats par visiem entītijas laukiem.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="f2d9a-108">Atveriet darbvietu **Datu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="f2d9a-109">Noklikšķiniet uz elementa **Datu elementi**.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-109">Click the **Data entities** tile.</span></span>
3. <span data-ttu-id="f2d9a-110">Elementu sarakstā meklējiet elementu **Vēsturisks ārējs pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="f2d9a-111">Noklikšķiniet uz **Mērķa lauki**.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-111">Click **Target fields**.</span></span> <span data-ttu-id="f2d9a-112">Šie elementu lauki ir obligāti: vieta (**DeliveringSiteId**), datums (**DemandDate**), daudzums (**DemandQuantity**) un krājuma numurs (**ItemNumber**) vai krājuma sadalījuma princips (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="f2d9a-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="f2d9a-113">Lai izmantotu datu elementu, ir nepieciešams Microsoft Excel fails vai komatatdalīto vērtību (CSV) fails, kurā ir ietverti vēsturiskie pieprasījuma dati.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="f2d9a-114">Tālāk esošajā piemērā ir aprakstīts, kā importēt datus no CSV faila.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-114">The following example shows how to import the data from a CSV file.</span></span>

## <a name="example"></a><span data-ttu-id="f2d9a-115">Piemērs</span><span class="sxs-lookup"><span data-stu-id="f2d9a-115">Example</span></span>

<span data-ttu-id="f2d9a-116">Kā paraugu varat izmantot tālāk pieejamo failu.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-116">You can use the following file as an example.</span></span> <span data-ttu-id="f2d9a-117">Lejupielādējiet failu [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span><span class="sxs-lookup"><span data-stu-id="f2d9a-117">Download the [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span></span> <span data-ttu-id="f2d9a-118">Šajā failā ir ietverti vēsturiskie pieprasījuma dati par krājumu D0001.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-118">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="f2d9a-119">Tajā ir ietverti tikai šādi obligātie lauki: vieta, daudzums un pieprasījuma datums.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-119">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="f2d9a-120">Atlasiet uzņēmumu, kurā ir jāimportē vēsturiskie pieprasījuma dati.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-120">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="f2d9a-121">Atveriet darbvietu **Datu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-121">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="f2d9a-122">Noklikšķiniet uz elementa **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-122">Click the **Import** tile.</span></span>
4. <span data-ttu-id="f2d9a-123">Ievadiet importēšanas projekta nosaukumu, piemēram, **Importētie krājuma D0001 vēsturiskie pieprasījuma dati**.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-123">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="f2d9a-124">Laukā **Avota datu formāts** atlasiet importētā faila formātu.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-124">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="f2d9a-125">Lai importētu šī piemēra ietveros lietoto failu HistoricalDemandData, atlasiet **CSV**.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-125">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="f2d9a-126">Laukā **Elementa nosaukums** atlasiet **Vēsturisks ārējs pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-126">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="f2d9a-127">Saglabājiet failu datorā un pēc tam augšupielādējiet to.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-127">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="f2d9a-128">Noklikšķiniet uz **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-128">Click **Import**.</span></span>
9. <span data-ttu-id="f2d9a-129">Tiek automātiski atvērta lapa **Izpildes kopsavilkums**.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-129">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="f2d9a-130">Pārbaudiet importētos datus šajā lapā.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-130">Verify the imported data on the page.</span></span>

<span data-ttu-id="f2d9a-131">Pēc vēsturisko pieprasījuma datu importēšanas varat ģenerēt pieprasījuma apjoma prognozi.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-131">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2d9a-132">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="f2d9a-132">Additional resources</span></span>

[<span data-ttu-id="f2d9a-133">Ģenerēt statistiskās bāzlīnijas prognozi</span><span class="sxs-lookup"><span data-stu-id="f2d9a-133">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)
