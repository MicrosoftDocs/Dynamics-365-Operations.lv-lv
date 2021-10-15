---
title: Mainīt starpuzņēmumu pasūtījumus
description: Šajā tēmā skaidrots, kā mainīt starpuzņēmumu pasūtījumu funkcionalitāti
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
ms.openlocfilehash: 1129794bf0ac6513770f8b2a0eeb7fb6154d7942
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548411"
---
# <a name="change-intercompany-orders"></a>Mainīt starpuzņēmumu pasūtījumus

[!include [banner](../../includes/banner.md)]

Ja veicat izmaiņas starpuzņēmumu pārdošanas un pirkšanas pasūtījumā, šīs izmaiņas atspoguļojas arī attiecīgajā uzņēmuma pārdošanas un pirkšanas pasūtījumā.

## <a name="adding-new-lines"></a>Jaunu rindu pievienošana

Jūs varat pievienot jaunas rindas starpuzņēmumu pārdošanas pasūtījumam un pirkšanas pasūtījumam, ja sākotnējais pārdošanas pasūtījums ir daļa no starpuzņēmumu pasūtījumu ķēdes. Jaunas rindas var pievienot arī tad, ja oriģinālā pārdošanas pasūtījuma piegāde nav tiešā piegāde. Ja sākotnējais pārdošanas pasūtījums ir tiešā piegāde, jaunas pasūtījuma rindas starpuzņēmumu pārdošanas pasūtījumam un pirkšanas pasūtījumam var pievienot tikai tad, ja sākotnējā pārdošanas pasūtījuma kopsavilkuma cilnē **Starpuzņēmumu iestatījumi** ir atlasīts lauks **Atļaut netiešu izveidi**.

## <a name="changing-prices-and-discounts"></a>Preču un atlaižu izmainīšana

Jūs varat mainīt cenas un atlaides, ja **Starpuzņēmumu** lapā ir atzīmētas izvēles rūtiņas **Atļaut cenas rediģēšanu** un **Atļaut atlaides rediģēšanu**.

Ja maināt vienības cenu kādā no esošām starpuzņēmumu pārdošanas pasūtījuma rindām, mainīsies arī vienības cena starpuzņēmumu pirkšanas pasūtījumā.

Ja maināt kādu no atlaižu laukiem starpuzņēmumu pārdošanas pasūtījuma rindā, tiek atjaunināti arī saistītie atlaižu lauki starpuzņēmumu pirkšanas pasūtījumā.

## <a name="changing-and-adding-new-charges"></a>Papildmaksu izmainīšana un pievienošana

Jūs varat mainīt cenas un atlaides, ja **Starpuzņēmumu** lapā ir atzīmētas izvēles rūtiņas **Atļaut cenas rediģēšanu** un **Atļaut atlaides rediģēšanu**.

Ja pievienojat jaunu maksu starpuzņēmumu pārdošanas pasūtījuma virsrakstam un jaunu maksu starpuzņēmumu pārdošanas rindai, abas maksas tiek kopētas starpuzņēmumu pirkšanas pasūtījumā. Šajā gadījumā dokumenti ir starpuzņēmumu pārdošanas pasūtījums un starpuzņēmumu pirkšanas pasūtījums. Papildmaksas nekad nekopē sākotnējā pārdošanas pasūtījumā.

## <a name="copying-a-fee"></a>Maksas kopēšana

Lai kopētu maksu sākotnējā pārdošanas pasūtījumā, izveidojiet to kā jaunu pārdošanas rindu; izveidojiet šo jauno pārdošanas rindu ar **Pakalpojuma** tipa krājumu.

## <a name="changing-quantities-and-deleting-intercompany-purchases-and-sales-order-lines"></a>Daudzumu izmainīšana un starpuzņēmumu pirkšanas un pārdošanas pasūtījuma rindu dzēšana

Daudzumu var mainīt vai starpuzņēmumu pirkšanas un pārdošanas pasūtījuma rindu var dzēst tikai tad, ja rinda ir tikusi izveidota tieši no veidlapas **Pārdošanas pasūtījums** vai **Pirkšanas pasūtījums**. Šīs izmaiņas izveidos vai nu starpuzņēmumu pirkšanas vai pārdošanas pasūtījuma/pasūtījuma rindu avotu.

## <a name="origins-of-orders-and-order-lines"></a>Pasūtījumu un pasūtījuma rindu izcelsme

Starpuzņēmumu pasūtījumiem un pasūtījumu rindām var būt viens no diviem izcelsmes veidiem:

- **Atvasināts** - Pasūtījums ticis izveidots automātiski starpuzņēmumu pasūtījumu ķēdes rezultātā.
- **Avota** - Pasūtījumu manuāli izveidojis lietotājs.

Statusu nosaka starpuzņēmumu pirkšanas pasūtījumu un pārdošanas pasūtījumu virsrakstā laukā **Izcelsme**. Šis lauks atrodas pārdošanas pasūtījuma **Starpuzņēmumu iestatījumu** kopsavilkuma cilnē un pirkšanas pasūtījuma kopsavilkuma cilnē **Iestatījumi**.

**Atvasinātās** un **Avota** izcelsmes attiecas tikai uz starpuzņēmumu pasūtījumiem. Tādēļ lauks **Izcelsme** būs tukšs visiem pārējiem pārdošanas pasūtījumiem, pirkšanas pasūtījumiem un pasūtījumu rindām. Šis lauks būs tukšs arī sākotnējam pārdošanas pasūtījumam.

## <a name="example-derived-origin"></a>Piemērs: atvasinātā izcelsme

Jūs izveidojat sākotnējo pārdošanas pasūtījumu ārējam debitoram. Šim pārdošanas pasūtījumam ir viena rinda. Šis sākotnējais pārdošanas pasūtījums izveido starpuzņēmumu pirkšanas pasūtījumu, kurā ir viena pasūtījuma rinda, kas izveido starpuzņēmumu pārdošanas pasūtījumu, kurā ir viena pasūtījuma rinda. Starpuzņēmumu pirkšanas pasūtījuma virsraksts un pasūtījuma rinda tiek izveidota automātiski no sākotnējā pārdošanas pasūtījuma.

**Izcelsmes** lauka vērtība starpuzņēmumu pirkšanas pasūtījuma kopsavilkuma cilnē **Iestatījumi** un starpuzņēmumu pārdošanas pasūtījumu virsrakstu kopsavilkuma cilnē **Starpuzņēmumu iestatījumi** ir **Atvasināts**. Lauka **Izcelsme** vērtība arī ir **Atvasināta** pirkšanas pasūtījuma un pārdošanas pasūtījuma rindu cilnē **Detalizēta informācija par rindu**.

Ja pasūtījuma rindas izcelsme ir **Atvasināts**, pasūtījuma rindu nevar izdzēst tieši. Tāpat arī pasūtīto daudzumu jūs varat mainīt tikai no tā avota, kurā pasūtījuma rinda veidota. Tāpat arī pasūtīto daudzumu jūs varat mainīt tikai no tā avota, kurā pasūtījuma rinda veidota.

Ja sākotnējais pārdošanas pasūtījums un sākotnējā pārdošanas pasūtījuma rinda ir daļa no starpuzņēmumu pasūtījumu ķēdes, jūs varat izmainīt pasūtīto daudzumu no sākotnējā pārdošanas pasūtījuma un jūs varat izdzēst pasūtījuma rindu no sākotnējā pārdošanas pasūtījuma.

## <a name="example-source-origin"></a>Piemērs: avota izcelsme

Jūs izveidojat pirkšanas pasūtījumu starpuzņēmumu kreditoram. Gan starpuzņēmumu pirkšanas pasūtījumam, gan pasūtījuma rindai būs **Avota** izcelsme. Tādēļ šis starpuzņēmumu pirkšanas pasūtījums būs regulators un automātiski izveidotā starpuzņēmumu pārdošanas pasūtījuma kreditora uzņēmumā būs **Atvasināta** izcelsme.

Papildus tam, pasūtīto daudzumu pasūtījuma rindā, kas izveidota starpuzņēmumu pirkšanas pasūtījumā, nevar mainīt starpuzņēmumu pārdošanas pasūtījumā. Pasūtījuma rindu var dzēst tikai no starpuzņēmuma pirkšanas pasūtījuma. Ja starpuzņēmumu pārdošanas pasūtījumā tiek pievienota jauna rinda, starpuzņēmumu pārdošanas pasūtījuma rindai būs **Avota** izcelsme .

Ja sākotnējais pārdošanas pasūtījums ir daļa no starpuzņēmumu pasūtījumu ķēdes, vienmēr ir iespējams kontrolēt starpuzņēmumu pasūtījumus un starpuzņēmumu pasūtījumu rindas no sākotnējā pārdošanas pasūtījuma.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
