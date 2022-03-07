---
title: Pašlaik tiek lietoti noliktavas pārvaldības procesi
description: Rezervējot vai izlaižot darbu, varat saņemt ziņojumu, ka pašlaik tiek izmantoti noliktavas pārvaldības procesi. Izlabojiet problēmu, izmantojot vienu no šīm darbībām.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bfda2fae824cdc64d722310d20cf16e6306d766c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476936"
---
# <a name="cant-reserve-or-release-work-because-processes-are-currently-being-used"></a>Nevar rezervēt vai izlaist darbu, jo pašlaik tiek izmantoti procesi

## <a name="symptoms"></a>Simptomi

Strādājot ar diskrētu ražošanu, jūs saņemat šādu kļūdu:

> Pašlaik tiek lietoti noliktavas pārvaldības procesi. Ja darba rindas vēl nav reģistrētas, varat atcelt izveidoto darbu un jebkuras noslodzes vai sūtījuma rindas un pēc tam turpināt izdošanas vai nosūtīšanas procesu.

## <a name="cause"></a>Iemesls

Šī problēma rodas, ja mēģināt rezervēt vai izlaist darbu rindai, bet krājuma darbības statuss ir *Izdots*, kas norāda, ka materiāls ir izdots.

## <a name="resolution"></a>Novēršana

Lai novērstu šo problēmu, izpildiet vienu no sekojošajām darbībām.

- Mainīt ražošanas pasūtījuma statusu atpakaļ uz *Prognozētu* vai *Izlaistu*.
- Atveriet lapu ar detalizētu informāciju par attiecīgās ražošanas pasūtījumu. Darbības rūtī cilnē **Noliktava**, kas atrodas grupā **Apturēt**, atlasiet opciju **Apturēt un neizdot**, lai atceltu visu izdoto darbību izdošanu. Pēc tam atlasiet **Noņemt apturēšanu**, lai apstrādātu ražošanas pasūtījumu.

Piedāvājam paskaidrojumu par funkcijām *Neizdot* un *Apturēt*:
  
- **Neizdot** – šī funkcija anulē krājumu darbību statusu materiālu komplekta (MK) rindās un formulas rindās, kuru statuss ir no *Izdots* *Pēc pasūtījuma*. Kad darbs ar izejmateriālu izdošanu ir pabeigts, rindu statuss ir iestatīts uz *Izdots*. Šis statuss neļauj atiestatīt ražošanas pasūtījumu uz statusu *Izveidots* . Šādā gadījumā varat izmantot funkciju *Neizdot*, lai atgrieztu darbības no statusa *Izdots* un pēc tam atiestatītu ražošanas pasūtījumu uz statusu *Izveidots*.
- **Apturēt** – šī funkcija iestata **Apturēts** karodziņu ražošanas pasūtījumā, lai nepieļautu statusa atjaunināšanu pasūtījumā. **Apturēts** karodziņu varat atrast kopsavilkuma cilnē **Noliktava** ražošanas pasūtījuma informācijas lapā.

> [!NOTE]
>
> - Pogas ir redzamas tikai tad, kad ražošanas pasūtījums tiek izveidots krājumiem, kas ir iespējoti noliktavas procesiem.
> - Grupa **Apturēt** ir redzama tikai cilnē **Noliktava**, kas atrodas ražošanas pasūtījuma informācijas lapas darbības rūtī. Tā nav redzama kopsavilkuma cilnē **Noliktava**, kas atrodas **Ražošanas pasūtījumu** saraksta lapā.
