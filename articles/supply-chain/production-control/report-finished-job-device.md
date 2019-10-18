---
title: Ziņot kā pabeigtu uz no numura zīmes atkarīgo novietojumu no Darba kartes ierīces
description: Šajā tēmā ir aprakstīts ražošanas pasūtījumā uz krājumu pabeigto preču pabeigšanas process, kad noliktavas numura zīme kontrolē novietojumu.
author: johanhoffmann
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: 35ad27a6b8a52bfd086fbe4fc57b1681ff88fd5b
ms.sourcegitcommit: 58db26b7edf02e7c33aaaf1c934e3263aa74b01f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/11/2019
ms.locfileid: "1995146"
---
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="9e126-103">Ziņot kā pabeigtu uz no numura zīmes atkarīgo novietojumu no Darba kartes ierīces</span><span class="sxs-lookup"><span data-stu-id="9e126-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="9e126-104">Process, ko sauc par Ziņošanu kā pabeigtu, pabeidz ražošanas pasūtījumā uz krājumu pabeigtās preces.</span><span class="sxs-lookup"><span data-stu-id="9e126-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="9e126-105">Ja pabeigtā prece ir iespējota papildu noliktavas procesiem, tad uz novietojumu, kas tiek saukts par ražošanas izvades vietu, tiek ziņots, ka prece ir pabeigta.</span><span class="sxs-lookup"><span data-stu-id="9e126-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="9e126-106">Lai iegūtu informāciju par ražošanas izvades vietas iestatīšanu, skatiet [Ražošanas izvades novietojums.](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location)</span><span class="sxs-lookup"><span data-stu-id="9e126-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="9e126-107">Lai pabeigtu šo uzdevumu, jāatlasa esošais numura zīmes numurs.</span><span class="sxs-lookup"><span data-stu-id="9e126-107">You must select an existing license plate number to complete this task.</span></span> <span data-ttu-id="9e126-108">Ja ražošanas izvades novietojums ir iestatīts izsekošanai, izmantojot numura zīmi, ir jāiekļauj numura zīmes numurs, kad ražošanas izvades vieta tiek ziņota kā pabeigta.</span><span class="sxs-lookup"><span data-stu-id="9e126-108">If the production output location is set up to be tracked by license plate, then a license plate number must be included when reporting the production output location as finished.</span></span> <span data-ttu-id="9e126-109">**Numura zīmes** lauks ir redzams **Pārskata progress** uzvednē lapā **Darba kartes ierīce** .</span><span class="sxs-lookup"><span data-stu-id="9e126-109">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="9e126-110">Lauks ir redzams tikai **pārskata progresa** uzvednē, ziņojot par ražošanas pasūtījuma pēdējo operāciju.</span><span class="sxs-lookup"><span data-stu-id="9e126-110">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order.</span></span> <span data-ttu-id="9e126-111">Lauks ir redzams tikai tad, ja krājuma ražošanas pasūtījumam ir iespējots noliktavas pārvaldības procesiem.</span><span class="sxs-lookup"><span data-stu-id="9e126-111">The field is only shown if the item for the production order is enabled for the warehouse management processes.</span></span> 
