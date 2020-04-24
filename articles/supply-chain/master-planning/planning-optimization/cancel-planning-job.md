---
title: Atcelt plānošanas darbu
description: Šajā tēmā izskaidrots, kā atcelt aktīvu plānošanas darbu, kas izmanto funkcionalitāti Plānošanas optimizācija.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: b731aa4573b438e594ede702e6556c1be2daa549
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213475"
---
# <a name="cancel-a-planning-job"></a>Plānošanas darba atcelšana

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Programmā Microsoft Dynamics 365 Supply Chain Management varat atcelt aktīvu plānošanas darbu, kas izmanto funkcionalitāti Plānošanas optimizācija. Atlasot opciju **Atcelt** dialoglodziņā, kad plānošanas optimizācijas darbs tiek parādīts tieši no lietotāja interfeisa (nevis fonā), tas neatcels plānošanas optimizācijas darbu. Pat ja saņemat brīdinājumu, piemēram, "Operācija atcelta", jums joprojām būs jāveic šīs darbības, lai atceltu plānošanas darbu ar plānošanas optimizāciju.


Lai atceltu aktīvu plānošanas darbu, veiciet tālāk norādītās darbības. 

> [!NOTE]
> Atcelt var tikai aktīvus darbus.

1. Pārejiet uz **Vispārējā plānošana \> Iestatīšana \> Plāni**.
2. Atlasiet atbilstošu plānu izpildes plānošanai.
3. Atlasiet **Vēsture**.
4. Atlasīt plānošanas darbu, kuru atcelt.
5. Atlasiet **Atcelt**.

Darba statuss būs **Atcelšana**, līdz pakalpojums Plānošanas optimizācija apstiprinās, ka darbs ir atcelts. Pēc tam statuss tiks mainīts uz **Atcelts**.

> [!NOTE]
> Lai skatītu statusa izmaiņas, ir jāatsvaidzina lapa, atlasot pogu **Atsvaidzināt**.

## <a name="additional-resources"></a>Papildu resursi

[Plānošanas optimizācijas apskats](planning-optimization-overview.md)

[Darba sākšana ar plānošanas optimizāciju](get-started.md)

[Plānošanas optimizācijas atbilstības analīze](planning-optimization-fit-analysis.md)

[Plāna vēstures un plānošanas žurnālu skatīšana](plan-history-logs.md)

[Filtru lietošana plānam](plan-filters.md)
