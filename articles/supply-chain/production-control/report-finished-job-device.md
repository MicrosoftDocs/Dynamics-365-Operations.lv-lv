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

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>Ziņot kā pabeigtu uz no numura zīmes atkarīgo novietojumu no Darba kartes ierīces 

Process, ko sauc par Ziņošanu kā pabeigtu, pabeidz ražošanas pasūtījumā uz krājumu pabeigtās preces. Ja pabeigtā prece ir iespējota papildu noliktavas procesiem, tad uz novietojumu, kas tiek saukts par ražošanas izvades vietu, tiek ziņots, ka prece ir pabeigta. Lai iegūtu informāciju par ražošanas izvades vietas iestatīšanu, skatiet [Ražošanas izvades novietojums.](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location)

Ja ražošanas izvades vieta ir atkarīga no unikāla noliktavas vienības identifikatora, tad unikāls noliktavas vienības identifikators jānodrošina, ziņojot par pabeigšanu. **Numura zīmes** lauks ir redzams **Pārskata progress** uzvednē lapā **Darba kartes ierīce** . Šis lauks ir redzams tikai uzvednē **Pārskata progress**, sniedzot pārskatu par ražošanas pasūtījuma pēdējo darbību, un ražošanas pasūtījuma produkts ir iespējots noliktavas pārvaldības procesiem. 

Pastāv divas iespējas unikāla noliktavas vienības identifikatora nodrošināšanai
- Lietotājs unikāla noliktavas vienības identifikatora laukā atlasa esošu unikālu noliktavas vienības identifikatoru.
- Unikāls noliktavas vienības identifikators tiek automātiski ģenerēts no numuru sērijas un pēc noklusējuma ievietots unikāla noliktavas vienības identifikatora laukā.

Iespēja automātiski ģenerēt unikālu noliktavas vienības identifikatoru tiek konfigurēta, atlasot opciju **Ģenerēt unikālu noliktavas vienības identifikatoru** lapā **Konfigurēt darba karti ierīcēm**.
