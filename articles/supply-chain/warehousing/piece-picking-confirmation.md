---
title: Vienības izdošanas apstiprinājums
description: Vienības izdošana ļauj apstiprināt katru krājuma vienību, izmantojot izdošanas vai inventarizācijas darbu mobilajā ierīcē.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a925685b80c635cf036f19748e16d415953ed5fdda7b81498baeade35ccbfcab
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766006"
---
# <a name="piece-picking-confirmation"></a>Vienības izdošanas apstiprinājums

[!include [banner](../includes/banner.md)]

Vienības izdošana ļauj apstiprināt katru krājuma vienību, izmantojot izdošanas vai inventarizācijas darbu mobilajā ierīcē. Attiecībā uz izdodamo vienību varat pārbaudīt apstrādājamo darba daudzumu vai izdodamo daudzumu, kas norādīts darbā. Attiecībā uz inventarizācijas darbu varat skenēt krājumu, kas tiek uzskaitīts, un izsekot kopsummu.

Iespējojot vienības izdošanu, preču apstiprinājums tiek automātiski atlasīts. Attiecībā uz darba veida izdošanu varat iestatīt maksimālo vienību skaitu. Tādējādi var iestatīt maksimālo vienību skaitu, kas ir jāapstiprina darba procesa laikā. Maksimālais daudzums ir atkarīgs no pašreizējās darba vienības, kas tiek apstrādāta. Inventarizācijas darba veidā nav atļauts maksimālais daudzums.

Var izmantot arī daudzumu un mērvienību (UOM), kas saistīta ar skenēto svītrkodu. Tas darbosies ienākošo plūsmu saņemšanā, tostarp saņemot jauktas noliktavas vienības, pirkšanas pasūtījuma krājumiem, pārsūtīšanas pasūtījuma krājumiem un noslodzes krājumiem. To var izmantot arī vienības izdošanai, ja skenējot svītrkodu, apstiprināto vienību kopskaitam tiks pievienos daudzums, kas tiks pārveidots starp svītrkoda UOM un darba vienību. Ja uzskaitot svītrkoda UOM, tiek apstiprināts, ka daudzums ir atļauts inventarizācijai secību grupā, daudzums tiks pievienots kopējam daudzumam.

## <a name="where-it-applies"></a>Darbības tvērums

Vienības izdošana darbojas visos inventarizācijas darbos un jebkura veida darba sākotnējā izdošanā. Vienības izdošana nedarbojas, ja krājums tiek kontrolēts, izmantojot sērijas numurus, vai, ja tas ir ražošanas vai Kanban izdošana no noliktavas vienības (LP) atrašanās vietas, un krājumam ir iestatīti sagatavošanas posmi.

## <a name="set-up-piece-picking"></a>Vienības izdošanas iestatīšana

1.  Mobilās ierīces izvēlnes vienumā atveriet iestatīšanas formu darba apstiprināšanai: Noliktavas pārvaldība > **Noliktavas pārvaldība** > **Iestatījumi** > **Mobilā ierīce** > **Mobilās ierīces izvēlnes vienumi**. 
2. No mobilās ierīces izvēlnes vienuma atveriet sadaļu Darba apstiprinājuma iestatīšana.

Tālāk minētās opcijas ir pieejamas atlasei, ja darbs ir izdošanas vai inventarizācijas darbs.


|           Opcija           |                                                                            Apraksts                                                                            |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vienības izdošanas apstiprinājums | Izdošanai un inventarizācijai pieejamie darba veidi. Preču apstiprināšana tiek automātiski atlasīta. Ļauj apstiprināt katru krājuma vienību no mobilās ierīces. |
|  Maksimālais vienību skaits  |                   Darbs, kas pieejams izdošanai, ja vienības izdošanas apstiprināšana ir iespējota. Iestata vienību skaita ierobežojumu, kas ir jāapstiprina.                   |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]