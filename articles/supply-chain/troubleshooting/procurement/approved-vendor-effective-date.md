---
title: Nevar mainīt apstiprināta piegādātāja spēkā stāšanās datumu
description: Apstiprināto piegādātāju sarakstā pēc produktu entitījas nevar mainīt spēkā stāšanās datumu
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: cb6dbd134d63daa163261cabdbd7eceb978877ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476940"
---
# <a name="cant-change-the-effective-date-for-an-approved-vendor"></a>Nevar mainīt apstiprināta piegādātāja spēkā stāšanās datumu


## <a name="symptoms"></a>Simptomi

Precei ir apstiprināts piegādātājs, kura spēkā stāšanās datums ir, piemēram, 2018. gada 11. janvāris (*01/11/2018*) un beigu datums ir *Nekad*. Ja mēģināsit mainīt spēkā stāšanās datumu uz 2018. gada 10. janvāri (*01/10/2018*) vai 2018. gada 12. janvāri (*01/12/2018*), tiks parādīta šāda kļūda:

> Nevar izveidot ierakstu apstiprinātā piegādātāja sarakstā (PdsApproveVendorList). Vērtībai “Termiņa beigas” ir jābūt lielākai vai vienādai ar vērtību “Spēkā esošs”.

## <a name="resolution"></a>Novēršana

Varat pagarināt tikai periodu, kurā piegādātājs ir apstiprināts. Ir spēkā šādi nosacījumi:

- Lai mainītu spēkā stāšanās datumu tā, ka tas ir agrāks par krājuma kreditora esošajiem ierakstiem (periodiem), jaunā perioda beigu datumam ir jābūt pirms visu esošo ierakstu beigu datumiem.
- Lai mainītu beigu datumu tā, lai tas būtu vēlāks par jebkuru no esošajiem periodiem, spēkā stāšanās datumam jābūt pēc vēlākā beigu datuma jebkurā esošajā ierakstā.
- Lai samazinātu kopējo periodu, kurā kreditors ir apstiprināts, ir jādzēš vai jāmodificē esošie ieraksti. Vai arī importēšanas laikā varat izmantot slēdzi **Saīsināt**. Šis slēdzis dzēš visus esošos ierakstus tabulā apstiprinātajiem piegādātājiem pēc krājuma.

Piemēra scenārijam, kas ir aprakstīts problēmas aprakstā, kur ierakstam ir spēkā stāšanās datums *01/11/2018* un beigu datums *Nekad*, jūs varat importēt jaunu ierakstu, kam ir spēkā stāšanās datums *01/10/2018* un beigu datums *Nekad*. Tomēr jūs nevarat samazināt periodu tā, lai spēkā stāšanās datums tiktu atjaunināts uz *01/12/2018*, izmantojot datu pārvaldību. Šīs izmaiņas jāveic, izmantojot lietotāja interfeisu.
