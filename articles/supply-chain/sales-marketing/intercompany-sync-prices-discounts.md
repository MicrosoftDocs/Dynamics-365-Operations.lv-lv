---
title: Starpuzņēmumu cenu un atlaižu sinhronizēšana
description: Šajā tēmā skaidrota cenu un atlaižu sinhronizācija starpuzņēmumu pārdošanas un pirkšanas pasūtījumiem
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
ms.openlocfilehash: a9467e8d06a44cfaab9e3c8ea3944675c3eb8fb5
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548391"
---
# <a name="synchronize-intercompany-prices-and-discounts"></a>Starpuzņēmumu cenu un atlaižu sinhronizēšana

[!include [banner](../../includes/banner.md)]

Atlaides un cenas vienmēr tiek sinhronizētas starp starpuzņēmumu pārdošanas pasūtījumu un starpuzņēmumu pirkšanas pasūtījumu. Var arī izvēlēties sinhronizēt cenu un atlaides uz/no oriģinālā pārdošanas pasūtījuma, lai visiem pasūtījumiem būtu vienādas cenas un atlaides. To varat izdarīt no **Starpuzņēmumu** lapas, kam var piekļūt no cilnes **Vispārīgi**, kas atrodas saraksta lapā **Visi debitori** – no **Pārdošanas un mārketinga** vai **Sagādes un plānošanas**.

Lauks **Cena un atlaide** tiek sinhronizēts uz starpuzņēmumu pārdošanas pasūtījuma rindu. Tas nozīmē, ka, atlasot lauku **Aatlaut cenas rediģēšanu** un lauku **Atļaut atlaides rediģēšanu**, ir atļauta izmaiņa starp starpuzņēmumu pārdošanas un starpuzņēmumu pirkšanas pasūtījumu. Izmaiņas vienības cenā, cenas vienībā vai pārdošanas papildmaksā starpuzņēmumu pārdošanas pasūtījumā nosaka cenu starpuzņēmumu pirkšanas pasūtījuma rindā.

Ja starpuzņēmumu pārdošanas pasūtījumā vai starpuzņēmumu pirkšanas pasūtījumā ir aktivizēti lauki **Atļaut cenas rediģēšanu** un **Atļaut atlaides rediģēšanu**, cenu vai atlaidi jebkurā pasūtījumā var mainīt manuāli. Pretējā gadījumā to nevar izdarīt.

Ja starpuzņēmumu pārdošanas pasūtījumā vai starpuzņēmumu pirkšanas pasūtījumā nav aktivizēti lauki **Atļaut cenas rediģēšanu** un **Atļaut atlaides rediģēšanu**, cenu vai atlaidi jebkurā pasūtījumā var mainīt manuāli.

Ja starpuzņēmumu pārdošanas pasūtījumā vai starpuzņēmumu pirkšanas pasūtījumā nav aktivizēti lauki **Atļaut cenas rediģēšanu** un **Atļaut atlaides rediģēšanu**, cenu vai atlaidi jebkurā pasūtījumā nevar mainīt manuāli.

Ja starpuzņēmumu pārdošanas pasūtījumā vai starpuzņēmumu pirkšanas pasūtījumā ir aktivizēti lauki **Atļaut cenas rediģēšanu** un **Atļaut atlaides rediģēšanu**, cenu vai atlaidi jebkurā pasūtījumā var mainīt manuāli. Tomēr tas var radīt situāciju, kurā vienas personas veikti atjauninājumi tiek noraidīti ar atjauninājumiem, ko tajā pašā pasūtījumā veikusi cita persona citā uzņēmumā.

> [!NOTE]
> Ja lauks **Cena un atlaide** ir aktivizēts gan starpuzņēmumu, gan pirkšanas pasūtījumā, gan starpuzņēmumu pārdošanas pasūtījumā, jūs nepārvaldāt cenu noteikšanu.

Lai izvairītos no šiem konfliktu tipiem, vislabākā prakse ir ļaut mainīt cenas un atlaides tikai starpuzņēmumu pārdošanas pasūtījumā vai starpuzņēmumu pirkšanas pasūtījumā. To veic, iespējojot laukus **Atļaut cenas rediģēšanu** un **Atļaut atlaides labošanu** jebkurā no šiem pasūtījumiem.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
