---
title: Sistēmas administratori nevar dzēst pasūtījumu aizturēšanu, jo tie nav autorizēti
description: Sistēmas administratori nevar dzēst pasūtījumu aizturēšanu, jo tie nav autorizēti.
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acabd6409d9b2860535335bc648bcc34304e0cb0
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026728"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a>Sistēmas administratori nevar dzēst pasūtījumu aizturēšanu, jo tie nav autorizēti

KB numurs: 4614642

## <a name="symptoms"></a>Simptomi

Sistēmas administratori nevar dzēst pārdošanas pasūtījumu aizturēšanas gadījumus, ja tiem nav noteikta loma, kas piešķirta pasūtījuma aizturēšanas kodā.

## <a name="resolution"></a>Novēršana

Piekļuvi dažām operācijām, piemēram, pārdošanas pasūtījumu aizturēšanas dzēšanai, nosaka biznesa politikas iestatījumi. Sistēmas administratoriem parasti nav atļauts veikt šī tipa operācijas. 

Piekļuve noteikta uzdevuma veikšanai bieži tiek pārvaldīta ar uzņēmējdarbības politiku, un tikai noteiktas personas organizācijā tiek akceptētas veikt šo uzdevumu. Piemēri iekļauj apstiprinājumus, kas ir darbplūsmas apstiprinājumu rezultāts, un konkrētus uzdevumus, kas ir darbplūsmas konfigurācijas rezultāts.

Lai gan neviena darbplūsma nav saistīta ar pasūtījumu aizturēšanu, princips ir līdzīgs. Atbilstoša loma norāda noteiktu personu grupu organizācijā, kurai ir tiesības dzēst pasūtījumu aizturēšanu. Šīs tiesības nav jāpiešķir visiem administratoriem, jo šī pieeja pārkāpj noteikto uzņēmējdarbības politiku.
