---
title: Problēmu novēršana saistībā ar daļēju izlaidi un daļēju nosūtīšanu
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar daļēju izlaidi un daļēju nosūtīšanu programmā Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e89a430f90374733b23fadaf53f5bab598d67d62
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645952"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a>Problēmu novēršana saistībā ar daļēju izlaidi un daļēju nosūtīšanu

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar daļēju izlaidi un daļēju nosūtīšanu programmā Microsoft Dynamics 365 Supply Chain Management.

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>Pārdošanas pasūtījuma izlaišanas statuss paliek Daļēji izlaists pat pēc tam, kad pārdošanas pasūtījums ir iekļauts rēķinā.

### <a name="issue-description"></a>Problēmas apraksts

Pārdošanas pasūtījums ir piegādes pasūtījums, bet vienam vai vairākiem krājumiem tajā ir cits piegādes veids. Pēc tam, kad pasūtījums ir iekļauts rēķinā, tam joprojām ir laidiena statuss *Daļēji izlaists*.

Piemēram, pārdošanas pasūtījumam ir divi krājumi: viens piegādāšanai un viens saņemšanai. Ir veikta gan nogādāšana, gan saņemšana. Tāpēc abām rindām ir izrakstīts rēķins. Tomēr izdošanas statuss joprojām tiek norādīts kā *Daļēji izlaists*, un tas ir maldinošs.

### <a name="issue-resolution"></a>Problēmas risinājums

Izdošanas statuss attiecas tikai uz pasūtījuma rindām, kur krājumi ir iespējoti noliktavas pārvaldībai. Tāpēc nodošanas statuss šajā scenārijā paliek *Daļēji izlaists*. Korporācija Microsoft ir izvērtējusi šo problēmu un ir noteikusi, ka tas ir līdzekļa ierobežojums. Paplašinājumu var pievienot kā daļu no pavadzīmes un rēķinu izrakstīšanas procesa, lai atjauninātu izlaides statusu.
