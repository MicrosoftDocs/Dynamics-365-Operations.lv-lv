---
title: Rezervācijas nevar noņemt, atceļot pasūtījumu
description: Nav iespējams atcelt pārdošanas pasūtījumu, līdz darbs, kas saistīts ar šo pasūtījumu, nav atcelts un atsaukts. Lai to izdarītu, veiciet tālāk norādītās trīs darbības.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a8d947e64568246dba5eff3c21fd3920b6494b73
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476995"
---
# <a name="reservations-cannot-be-removed-when-canceling-an-order"></a>Rezervācijas nevar noņemt, atceļot pasūtījumu

## <a name="symptoms"></a>Simptomi

Ja darbs tiek saistīts ar pārdošanas pasūtījumu un jūs mēģināt atcelt pasūtījumu, iespējams, saņemsit šādu kļūdas ziņojumu:

> Nevar noņemt rezervācijas, jo ir izveidots darbs, kuram šīs rezervācijas ir nepieciešamas.

Nav iespējams atcelt pārdošanas pasūtījumu, līdz darbs nav atcelts un atsaukts. Šī prasība ir spēkā pat tad, ja ar pārdošanas pasūtījumu saistītais darbs ir slēgts.

## <a name="resolution"></a>Novēršana

Lai novērstu šo problēmu, veiciet tālāk minētās darbības.

1. Atceliet darbu un atgrieziet krājumu vēlamajā atrašanās vietā. Dodieties uz atbilstošo pārdošanas pasūtījuma noslodzi un atlasiet **Samazināt izdoto daudzumu** kravas rindā vai **Atsaukt darbu** darbību rūtī.

    Darbs tagad ir ar statusu *Atcelts* un jauns krājumu pārvietošanas darbs tiek automātiski izveidots un apstrādāts, lai ievietotu krājumus atpakaļ novietojumā, kas tika aprakstīts atsaukšanas laikā.

2. Dzēsiet noslodzi. Tiek dzēsts arī sūtījums.

3. Tagad varēsit doties uz pārdošanas pasūtījumu un to atcelt.
