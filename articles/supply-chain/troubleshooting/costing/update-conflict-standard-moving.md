---
title: Atjauniniet konfliktu, ja krājumu novērtēšanas metode ir standarta izmaksas vai slīdošais vidējais
description: Atjaunināšanas konflikts rodas, kad krājumu novērtēšanas metode ir standarta izmaksas vai slīdošais vidējais
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 920d20d19843ce0cac678c5426c00ec99aa61c61
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477014"
---
# <a name="an-update-conflict-occurs-when-the-inventory-valuation-method-is-either-standard-cost-or-moving-average"></a>Atjaunināšanas konflikts rodas, kad krājumu novērtēšanas metode ir standarta izmaksas vai slīdošais vidējais

## <a name="symptoms"></a>Simptomi

Ja grāmatojat dokumentus, piemēram, krājumu žurnālus, pirkšanas pasūtījuma rēķinus vai pārdošanas pasūtījuma rēķinus paralēli mērogošanai un veiktspējai, var tikt parādīts kļūdas ziņojums par atjauninājumu konfliktu un daži dokumenti, iespējams, netiks grāmatoti. Šī problēma rodas, kad krājumu novērtēšanas metode ir *Standarta izmaksas* vai *Pārvieto vidējo vērtību*. Abas šīs metodes ir pastāvīgas izmaksu aprēķināšanas metodes. Citiem vārdiem sakot, gala izmaksas tiek noteiktas iegrāmatošanas laikā.

Ja izmantojat metodi *Pārvieto vidējo*, kļūdas ziņojums ir līdzīgs šim piemēram:

> Krājumu vērtība xx.xx nav paredzama pēc proporcionālo izdevumu aprēķina

Ja izmantojat metodi *Standarta izmaksas*, kļūdas ziņojums ir līdzīgs šim piemēram:

> Standarta izmaksas nesakrīt ar finanšu krājumu vērtību pēc atjaunināšanas. Vērtība = xx.xx, Daudzums = yy.yy, Standarta izmaksas = zz.zz

## <a name="workaround"></a>Kļūdas apiešanas risinājums

Kamēr Microsoft nav izlaidis risinājumu problēmas atrisināšanai, apsveriet iespēju izmantot šādus risinājumus, lai palīdzētu izvairīties no šīm kļūdām vai tās samazināt:

- Neizdevušos dokumentu atkārtota grāmatošana.
- Izveidojiet dokumentus, kam ir mazāk rindu.
- Izvairieties no decimālvērtībām standarta izmaksās. Mēģiniet definēt standarta izmaksas tā, lai lauks **Cenas daudzums** būtu iestatīts uz *1*. Ja ir jānorāda **Cenas daudzuma** vērtība, kas pārsniedz *1*, mēģiniet samazināt decimāldaļu skaitu vienības standarta izmaksās. (Ideālā gadījumā jābūt mazāk nekā diviem decimāldaļskaitļiem.) Piemēram, izvairieties no standarta izmaksu iestatījumu definēšanas, piemēram, **Cena** = *10* un **Cenas daudzums** = *3* cenas, jo tie ražos vienības standarta izmaksas 3.333333 (kur decimālskaitļa vērtība atkārtojas).
- Lielākajā daļā dokumentu izvairīties no vairākām rindām, kurās ir viena un tā pati preču un finanšu krājumu dimensiju kombinācija.
- Samaziniet paralēlošanas pakāpi. (Šādā gadījumā sistēma var kļūt ātrāka, jo notiek mazāk atjauninājumu konfliktu un mēģinājumu.)
