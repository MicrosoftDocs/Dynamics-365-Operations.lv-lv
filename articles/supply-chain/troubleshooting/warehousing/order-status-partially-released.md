---
title: Pasūtījuma statuss pēc rēķina izrakstīšanas joprojām ir "Daļēji izlaists"
description: Dažos gadījumos pārdošanas pasūtījuma statuss joprojām ir "Daļēji izlaists" pat pēc tam, kad pasūtījumam ir izrakstīts rēķins. Šajā lapā paskaidrots, kāpēc tā notiek un kā šo problēmu risināt.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8bfe7ecfd4beb6e77e8dd1e23ccd896d067bdb51
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476994"
---
# <a name="order-status-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>Pasūtījuma statuss pat pēc pārdošanas pasūtījuma rēķina izrakstīšanas joprojām ir "Daļēji izlaists"

## <a name="symptoms"></a>Simptomi

Pārdošanas pasūtījums ir piegādes pasūtījums, bet vienam vai vairākiem krājumiem tajā ir cits piegādes veids. Pēc tam, kad pasūtījums ir iekļauts rēķinā, tam joprojām ir laidiena statuss *Daļēji izlaists*.

Piemēram, pārdošanas pasūtījumam ir divi krājumi: viens piegādāšanai un viens saņemšanai. Ir veikta gan nogādāšana, gan saņemšana. Tāpēc abām rindām ir izrakstīts rēķins. Tomēr izdošanas statuss joprojām tiek norādīts kā *Daļēji izlaists*, un tas ir maldinošs.

## <a name="workaround"></a>Kļūdas apiešanas risinājums

Izdošanas statuss attiecas tikai uz pasūtījuma rindām, kur krājumi ir iespējoti noliktavas pārvaldībai. Tāpēc nodošanas statuss šajā scenārijā paliek *Daļēji izlaists*. Korporācija Microsoft ir izvērtējusi šo problēmu un ir noteikusi, ka tas ir līdzekļa ierobežojums. Paplašinājumu var pievienot kā daļu no pavadzīmes un rēķinu izrakstīšanas procesa, lai atjauninātu izlaides statusu.
