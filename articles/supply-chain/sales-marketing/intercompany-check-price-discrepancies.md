---
title: Pārbaudīt starpuzņēmuma pasūtījumu cenu atšķirības
description: Šajā tēmā skaidrots, kā pārbaudīt starpuzņēmuma pasūtījumu cenu atšķirības
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f9a0ba4980f8acf56d84dc865094b405b7402ad5
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548392"
---
# <a name="check-intercompany-order-price-discrepancies"></a>Pārbaudīt starpuzņēmuma pasūtījumu cenu atšķirības

[!include [banner](../../includes/banner.md)]

Varat izmantot šo procedūru, lai pārbaudītu cenu neatbilstības starpuzņēmumu pasūtījumos.

1. Dodieties uz **Iepirkumi un sagāde \> Periodiskie \> Tīrīšana \> Pārbaudīt starpuzņēmuma pasūtījumu cenu atšķirības**.
1. Iestatiet pakešuzdevumu, ja nepieciešams, un pēc tam noklikšķiniet uz **Labi**, lai pārbaudītu cenas un atlaides starpuzņēmumu pārdošanas pasūtījumiem un pirkšanas pasūtījumiem. Pretējā gadījumā noklikšķiniet uz **Atcelt**, lai aizvērtu lapu bez pārbaudes veikšanas.

    > [!TIP]
    > Ja ir jebkādas sinhronizācijas problēmas vai problēmas ar cenām, tās tiks uzskaitītas informatīvā ziņojumā, kas tiks parādīts. Informācijas žurnālu varat drukāt atsaucei.

1. Informatīvajā ziņojumā veiciet dubultklikšķi uz atbilstošās rindas, lai atvērtu pasūtījumu šajā juridiskajā personā. Atveriet pasūtījumu saistītajā juridiskajā darbībā, atlasot **Starpuzņēmumu** un pēc tam **Starpuzņēmumu pirkšanas pasūtījumu** vai **Starpuzņēmumu pārdošanas pasūtījumu**.

    > [!NOTE]
    > Lai atļautu atjaunināt starpuzņēmumu pasūtījumu:
    >
    > 1. Dodieties uz **Debitoru parādi \> Debitori \> Visi debitori**.
    > 1. Darbību rūtī atlasiet cilni **Vispārīgi** un pēc tam atlasiet **Starpuzņēmums**.
    > 1. **Starpuzņēmumu** lapā atlasiet **Pirkšanas pasūtījumu politikas** vai **Pārdošanas pasūtījumu politikas**.
    > 1. Atlasiet **Atļaut cenas rediģēšanu** un **Atļaut labot atlaidi** abos apgabalos.

1. Atveriet attiecīgo starpuzņēmumu pasūtījumu, kur jāsaglabā cena.
1. Katrai pasūtījuma rindai mainiet rindas lauku **Vienības cena** un pēc tam mainiet to atpakaļ uz sākotnējo vērtību. Mainiet rindas lauku **Atlaide** uz priekšu un atpakaļ un mainiet attiecīgos laukus **Pirkumu izmaksas** vai **Pārdošanas izmaksas** uz priekšu un atpakaļ. Vērtību mainīšana uz priekšu un atpakaļ aktivizēs cenu, atlaižu un maksu sinhronizāciju no šīs starpuzņēmumu pasūtījumu rindas uz atsaucē norādīto starpuzņēmumu pasūtījumu rindu, lai tās tiktu automātiski saskaņotas.

    > [!NOTE]
    > Šī sinhronizācija ir derīga tikai tad, ja starpuzņēmumu pārdošanas pasūtījumam nav izrakstīts rēķins. Ja starpuzņēmumu pārdošanas pasūtījumam ir izrakstīts rēķins un tas ir grāmatots, un ir izveidots debitora rēķina žurnāls, izmaiņas jāveic tieši starpuzņēmumu pirkšanas pasūtījuma rindās, iestatot cenas, atlaides un maksas, kas līdzvērtīgas cenām, atlaidēm un maksām starpuzņēmumu debitora rēķina žurnālā. Ja tas netiek veikts, starpuzņēmuma pirkšanas pasūtījumam nevar izrakstīt rēķinu un to nevar grāmatot, jo neatbilst pasūtījumu kopsummas.

1. Atkārtojiet procedūru, līdz ir sinhronizēti visi starpuzņēmumu pirkšanas un pārdošanas pasūtījumi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
