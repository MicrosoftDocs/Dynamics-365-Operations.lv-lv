---
title: MK līniju skalošanas principa iestatījumi netiek ievēroti
description: Materiālu komplekta (MK) līniju skalošanas principa iestatījumi netiek ievēroti.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 84a84728016119a2a02f59f6903171afbceb48e7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026713"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a>MK līniju skalošanas principa iestatījumi netiek ievēroti

KB numurs: 4612725

## <a name="symptoms"></a>Simptomi

Šī problēma rodas, ja **Automātiskā MK patēriņa** lauks cilnē **Automātiska atjaunināšana**, lapā **Ražošanas kontroles parametri** ir iestatīts uz *Tīrīšanas principu*. Šis iestatījums norāda, ka visas materiālu komplekta (MK) rindas ir automātiski jāpatērē, kad ir saņemts pirkšanas pasūtījums. Ja **Tīrīšanas principa** lauks MK rindās ir skaidri iestatīts uz *Manuāli*, var būt paredzams, ka MK rindas netiks automātiski patērētas. Tomēr, kad rodas šī problēma, MK rindas, kur **Tīrīšanas principa** lauks ir iestatīts uz *Manuāli*, vienalga tiek automātiski patērētas.

## <a name="resolution"></a>Novēršana

Ja rodas šī problēma, iespējams, ražošanas kontroles parametri ir iestatīti, lai ignorētu **Tīrīšanas principa** iestatījumu MK rindās. Lapā **Ražošanas kontroles parametri**, cilnē **Automātiskā atjaunināšana** pārbaudiet lauku **Automātiskais MK patēriņš**. Ja tas ir iestatīts uz *Vienmēr*, sistēma ignorēs **Tīrīšanas principa** iestatījumu visās MK rindās un vienmēr iztukšos rindas. Lai sistēmā būtu atbilstība MK rindu **Tīrīšanas principa** iestatījumam, mainiet lauka **Automātisks MK patēriņš** vērtību uz *Tīrīšanas princips*.
