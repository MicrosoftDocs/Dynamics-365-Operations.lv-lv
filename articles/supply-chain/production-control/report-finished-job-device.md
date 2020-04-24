---
title: Ziņot kā pabeigtu uz no numura zīmes atkarīgo novietojumu no Darba kartes ierīces
description: Šajā tēmā ir aprakstīts ražošanas pasūtījumā uz krājumu pabeigto preču pabeigšanas process, kad noliktavas numura zīme kontrolē novietojumu.
author: johanhoffmann
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: f5863202facc83afb91b380ba5666334783ccbcf
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211173"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="f7497-103">Ziņot kā pabeigtu uz no numura zīmes atkarīgo novietojumu no Darba kartes ierīces</span><span class="sxs-lookup"><span data-stu-id="f7497-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="f7497-104">Process, ko sauc par Ziņošanu kā pabeigtu, pabeidz ražošanas pasūtījumā uz krājumu pabeigtās preces.</span><span class="sxs-lookup"><span data-stu-id="f7497-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="f7497-105">Ja pabeigtā prece ir iespējota papildu noliktavas procesiem, tad uz novietojumu, kas tiek saukts par ražošanas izvades vietu, tiek ziņots, ka prece ir pabeigta.</span><span class="sxs-lookup"><span data-stu-id="f7497-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="f7497-106">Lai iegūtu informāciju par ražošanas izvades vietas iestatīšanu, skatiet [Ražošanas izvades novietojums.](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location)</span><span class="sxs-lookup"><span data-stu-id="f7497-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="f7497-107">Ja ražošanas izvades vieta ir atkarīga no unikāla noliktavas vienības identifikatora, tad unikāls noliktavas vienības identifikators jānodrošina, ziņojot par pabeigšanu.</span><span class="sxs-lookup"><span data-stu-id="f7497-107">If the production output location is license plate controlled, then a license plate must be provided when reporting as finished.</span></span> <span data-ttu-id="f7497-108">**Numura zīmes** lauks ir redzams **Pārskata progress** uzvednē lapā **Darba kartes ierīce** .</span><span class="sxs-lookup"><span data-stu-id="f7497-108">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="f7497-109">Šis lauks ir redzams tikai uzvednē **Pārskata progress**, sniedzot pārskatu par ražošanas pasūtījuma pēdējo darbību, un ražošanas pasūtījuma produkts ir iespējots noliktavas pārvaldības procesiem.</span><span class="sxs-lookup"><span data-stu-id="f7497-109">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order and the item for the production order is enabled for the warehouse management processes.</span></span> 

<span data-ttu-id="f7497-110">Pastāv divas iespējas unikāla noliktavas vienības identifikatora nodrošināšanai</span><span class="sxs-lookup"><span data-stu-id="f7497-110">There are two options for providing the license plate</span></span>
- <span data-ttu-id="f7497-111">Lietotājs unikāla noliktavas vienības identifikatora laukā atlasa esošu unikālu noliktavas vienības identifikatoru.</span><span class="sxs-lookup"><span data-stu-id="f7497-111">The user is selecting an existing license plate in the license plate field.</span></span>
- <span data-ttu-id="f7497-112">Unikāls noliktavas vienības identifikators tiek automātiski ģenerēts no numuru sērijas un pēc noklusējuma ievietots unikāla noliktavas vienības identifikatora laukā.</span><span class="sxs-lookup"><span data-stu-id="f7497-112">The license plate is automatically generated from a number sequence and defaulted to the license plate field.</span></span>

<span data-ttu-id="f7497-113">Iespēja automātiski ģenerēt unikālu noliktavas vienības identifikatoru tiek konfigurēta, atlasot opciju **Ģenerēt unikālu noliktavas vienības identifikatoru** lapā **Konfigurēt darba karti ierīcēm**.</span><span class="sxs-lookup"><span data-stu-id="f7497-113">The option to have the license plate generated automatically is configured by selecting the option **Generate license plate** on the **Configure job card for devices** page.</span></span>
