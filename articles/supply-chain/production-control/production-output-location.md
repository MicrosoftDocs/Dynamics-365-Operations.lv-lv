---
title: Ražošanas izvades vieta
description: Šajā rakstā aprakstīta hierarhija, kas tiek izmantota ražošanas izvades vietas identificēšanai.
author: johanhoffmann
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 130db343c4d09f2b8d31bf8acad3dcceec2be32e
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067947"
---
# <a name="production-output-location"></a>Ražošanas izvades vieta

[!include [banner](../includes/banner.md)]

Šajā rakstā aprakstīta hierarhija, kas tiek izmantota ražošanas izvades vietas identificēšanai.

Ražošanas izvades vieta ir vieta, kurā pabeigtās preces tiek uzglabātas pēc to saražošanas. Parasti šī vieta atrodas tuvu ražošanas procesam, kas izgatavo pabeigto preci. Ražošanas izvades vieta tiek izmantota kā starpposms materiālu uzglabāšanai pirms to pārvietošanas nosūtīšanas zonā, uzglabāšanas vietā, ražošanas ievades vietā lejupstraumes ražošanas procesam utt. 

Noklusējuma ražošanas izvades vieta tiek iestatīta, kad par pabeigtajām precēm tiek ziņots ražošanas pasūtījumā vai partijas pasūtījumā. Lai identificētu šo izvades vietu, tiek izmantota tālāk norādītā hierarija.

1. Izmantojiet izvades vietu, kas ir definēta ražošanas pasūtījuma vai partijas pasūtījuma virsrakstā.
2. Ja tur vieta nav atrodama, izmantojiet izvades vietu, kas ir definēta resursā, ko izmanto ražošanas maršrutā definētā pēdējā operācija.
3. Ja tur vieta nav atrodama, izmantojiet izvades vietu, kas ir definēta resursu grupā, ko izmanto ražošanas maršrutā definētās pēdējās operācijas resurss.
4. Ja tur vieta nav atrodama, izmantojiet izvades vietu, kas ir definēta ražošanas pasūtījumam definētajā noliktavā.

Noklusējuma ražošanas izvades vieta ir iestatīta tikai precēm, kas iestatītas, izmantojot noliktavas vadības procesus (WMS). Kad šāda tipa krājums tiek norādīts kā pabeigts, tiek izveidots noliktavas darbs ar tipu **Pabeigto preču izvietošana** vai **Līdzproduktu un blakusproduktu izvietošana**. Šī tipa darbs ražošanas izvades vietu izmanto kā izdošanas vietu. Izvietošanas vietu nosaka novietojuma direktīvas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]