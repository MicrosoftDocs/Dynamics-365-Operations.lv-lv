---
title: Problēmu novēršana saistībā ar daļēju izlaidi un daļēju nosūtīšanu
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar daļēju izlaidi un daļēju nosūtīšanu programmā Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7b8cb887a4acd6fc1a691614dc666bbdbe4a34b1ff874c5d80cf492f2984d299
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742564"
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]