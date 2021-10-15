---
title: Starpuzņēmumu pārdošanas pasūtījumu izveide iekšējai lietošanai
description: Šajā tēmā skaidrots, kā izveidot starpuzņēmumu pārdošanas pasūtījumu iekšējai lietošanai
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0718a1560ec42df2a0a12e8b81484aa3be46d2d8
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548397"
---
# <a name="create-an-intercompany-sales-order-for-internal-use"></a>Starpuzņēmumu pārdošanas pasūtījumu izveide iekšējai lietošanai

[!include [banner](../../includes/banner.md)]

Parasti starpuzņēmuma pārdošanas pasūtījumu veido automātiski no starpuzņēmuma pirkšanas pasūtījuma. Varat arī manuāli izveidot starpuzņēmumu pārdošanas pasūtījumu, kas pēc tam ģenerē starpuzņēmumu pirkšanas pasūtījumu starpuzņēmumu debitora juridiskajā persona.

![Starpuzņēmumu iekšējās pārdošanas process](media/intercompanyinternalsalesprocess.png)

## <a name="create-an-intercompany-sales-order-manually"></a>Starpuzņēmumu pārdošanas pasūtījuma manuāla izveide

Izpildiet attēlā parādītās darbības juridiskajā personā B.

1. Doties uz **Debitoru parādi \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Lai izveidotu pārdošanas pasūtījumu, darbību rūtī atlasiet **Pārdošanas pasūtījums**.
1. Lapā **Izveidot pārdošanas** pasūtījumu atlasiet debitora kontu. Kopsavilkuma cilnē **Vispārīgi** pārliecinieties, vai ir atzīmēta izvēles rūtiņa **Starpuzņēmums**. Tas norāda, ka atlasītais debitors ir starpuzņēmuma debitors.
1. Ievadiet vai modificējiet informāciju un pēc tam noklikšķiniet uz **Labi** un pabeidziet pasūtījuma rindas, kā parasti.

    **Piegādes adreses** lauka vērtība tiek kopēta no starpuzņēmumu pārdošanas pasūtījuma galvenes uz starpuzņēmumu pirkšanas pasūtījuma galveni. **Krājuma numura** lauka vērtība, iekļaujot preču dimensijas, un **Piegādes datuma** un **Valūtas koda** lauka vērtības tiek kopētas no starpuzņēmumu pārdošanas pasūtījuma rindām uz starpuzņēmumu pirkšanas pasūtījuma rindām.

1. Pasūtījuma galvenē atlasiet **Starpuzņēmums**, lai skatītu saistīto starpuzņēmumu pirkšanas pasūtījumu.
1. Pasūtījuma rindās atlasiet **Starpuzņēmumu**, lai skatītu informāciju par rīcībā esošiem krājumiem starpuzņēmumu tirdzniecībai.

> [!TIP]
> Starpuzņēmumu pārdošanas pasūtījumus var skatīt **Starpuzņēmumu pasūtījumu** lapā.

> [!NOTE]
> Kad strādājat ar starpuzņēmumu, **Debitoru parametru** lapā ieteicams notīrīt izvēles rūtiņu **Dzēst pasūtījumu pēc rēķina izrakstīšanas**. Pretējā gadījumā saistītais pirkšanas pasūtījums tiek dzēsts. Kad strādājat ar starpuzņēmumu, **Kreditoru parametru** lapā ieteicams notīrīt izvēles rūtiņu **Dzēst pasūtījumu pēc rēķina izrakstīšanas**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
