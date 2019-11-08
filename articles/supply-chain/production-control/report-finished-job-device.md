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
ms.openlocfilehash: cb809e596fd6bf3030bcee460838798435512b95
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572133"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>Ziņot kā pabeigtu uz no numura zīmes atkarīgo novietojumu no Darba kartes ierīces 

Process, ko sauc par Ziņošanu kā pabeigtu, pabeidz ražošanas pasūtījumā uz krājumu pabeigtās preces. Ja pabeigtā prece ir iespējota papildu noliktavas procesiem, tad uz novietojumu, kas tiek saukts par ražošanas izvades vietu, tiek ziņots, ka prece ir pabeigta. Lai iegūtu informāciju par ražošanas izvades vietas iestatīšanu, skatiet [Ražošanas izvades novietojums.](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location)

Lai pabeigtu šo uzdevumu, jāatlasa esošais numura zīmes numurs. Ja ražošanas izvades novietojums ir iestatīts izsekošanai, izmantojot numura zīmi, ir jāiekļauj numura zīmes numurs, kad ražošanas izvades vieta tiek ziņota kā pabeigta. **Numura zīmes** lauks ir redzams **Pārskata progress** uzvednē lapā **Darba kartes ierīce** . Lauks ir redzams tikai **pārskata progresa** uzvednē, ziņojot par ražošanas pasūtījuma pēdējo operāciju. Lauks ir redzams tikai tad, ja krājuma ražošanas pasūtījumam ir iespējots noliktavas pārvaldības procesiem. 
