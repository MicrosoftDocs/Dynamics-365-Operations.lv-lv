---
title: Vēsturisko datu importēšana pieprasījuma apjoma prognozēm
description: Lai iegūtu precīzas pieprasījuma apjoma prognozes, ir nepieciešami vēsturiskie pieprasījuma dati pa krājumiem vai krājumu sadalījuma principiem. šajā tēmā ir izskaidrots, kā izmantot datu elementus, lai importētu vēsturiskos pieprasījuma datus no jebkuras sistēmas, tādējādi iegūstot vēsturiskos pieprasījuma datus par ilgāku periodu.
author: roxanadiaconu
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0b04ee246d4c28e934407ccb92d792692cc4347d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301654"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="472ef-104">Vēsturisko datu importēšana pieprasījuma apjoma prognozēm</span><span class="sxs-lookup"><span data-stu-id="472ef-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="472ef-105">Lai palīdzētu nodrošināt pieprasījuma apjoma prognozes precizitāti, ir jāizmanto pēc iespējas vairāk vēsturisko pieprasījuma datu pa krājumiem vai krājumu sadalījuma principiem.</span><span class="sxs-lookup"><span data-stu-id="472ef-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="472ef-106">Ja vēsturiskie pieprasījuma dati vēl nav importēti, importējiet tos, izmantojot Dynamics 365 Supply Chain Management datu elementu **Vēsturisks ārējs pieprasījums** (ReqDemPlanHistoricalExternalDemandEntity).</span><span class="sxs-lookup"><span data-stu-id="472ef-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="472ef-107">Darbvietā **Datu pārvaldība** ir redzams pārskats par visiem entītijas laukiem.</span><span class="sxs-lookup"><span data-stu-id="472ef-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="472ef-108">Atveriet darbvietu **Datu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="472ef-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="472ef-109">Noklikšķiniet uz elementa **Datu elementi**.</span><span class="sxs-lookup"><span data-stu-id="472ef-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="472ef-110">Elementu sarakstā meklējiet elementu **Vēsturisks ārējs pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="472ef-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="472ef-111">Atlasiet **Mērķa laukus**.</span><span class="sxs-lookup"><span data-stu-id="472ef-111">Select **Target fields**.</span></span> <span data-ttu-id="472ef-112">Šie elementu lauki ir obligāti: vieta (**DeliveringSiteId**), datums (**DemandDate**), daudzums (**DemandQuantity**) un krājuma numurs (**ItemNumber**) vai krājuma sadalījuma princips (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="472ef-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="472ef-113">Lai izmantotu datu elementu, ir nepieciešams Microsoft Excel fails vai komatatdalīto vērtību (CSV) fails, kurā ir ietverti vēsturiskie pieprasījuma dati.</span><span class="sxs-lookup"><span data-stu-id="472ef-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="472ef-114">Tālāk esošajā piemērā ir aprakstīts, kā importēt datus no CSV faila.</span><span class="sxs-lookup"><span data-stu-id="472ef-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="472ef-115">Papildinformāciju par to, kā importēt datus, tostarp to, kā iztīrīt datus pēc importēšanas, skatiet [Datu importēšanas un eksportēšanas darbu pārskats](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) un ar to saistītās tēmas.</span><span class="sxs-lookup"><span data-stu-id="472ef-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

<span data-ttu-id="472ef-116">Skatiet arī [Statistiskās bāzlīnijas prognozes ģenerēšana](generate-statistical-baseline-forecast.md).</span><span class="sxs-lookup"><span data-stu-id="472ef-116">See also [Generate a statistical baseline forecast](generate-statistical-baseline-forecast.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]