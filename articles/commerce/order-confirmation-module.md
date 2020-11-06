---
title: Pasūtījumu informācijas modulis
description: Šī tēma apskata pasūtījuma informācijas moduļus un apraksta, kā izmantot tos Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 06/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6610d2abe0a1b03ddd763f9a65fc1dab42f1da1b
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015184"
---
# <a name="order-details-module"></a>Pasūtījumu informācijas modulis

[!include [banner](includes/banner.md)]

Šī tēma apskata pasūtījuma informācijas moduļus un apraksta, kā izmantot tos Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Pasūtījumu informācijas moduli izmanto, lai rādītu pasūtījuma apstiprinājuma informāciju pēc pasūtījuma veikšanas. Tas parāda pasūtījuma apstiprinājuma ID, pasūtījuma kontaktinformāciju un citus pasūtījuma datus, piemēram, krājumus, kas tika iegādāti, maksājuma informāciju un nosūtīšanas metodi.

## <a name="order-details-module-properties"></a>Pasūtījumu informācijas moduļa rekvizīti

| Rekvizīta nosaukums  | Vērtības | apraksts |
|----------------|--------|-------------|
| Virsraksts        | Virsraksta teksts un virsraksta etiķete ( **H1** , **H2** , **H3** , **H4** , **H5** vai **H6** ) | Pasūtījuma informācijas modulim var būt virsraksts. Pēc noklusējuma virsrakstam tiek izmantota **H2** virsraksta etiķete. Tomēr etiķeti var mainīt atbilstoši pieejamības prasībām. |
| Kontaktpersonas tālruņa numurs | Teksts | Kontaktpersonas numuru var sniegt ar pasūtījumu saistītiem jautājumiem. |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a>Moduļi, ko var izmantot pasūtījuma informācijas lapas modulī

Izveidojot pasūtījuma informācijas lapu, papildus pasūtījuma informācijas modulim varat pievienot citus atbilstošus moduļus. Daži piemēri:

- **Ieteikumu modulis** — ieteikumu moduli var pievienot pasūtījuma informācijas lapai, lai klientam ieteiktu citas preces.
- **Mārketinga moduļi** — jebkuru mārketinga moduli var pievienot pasūtījuma informācijas lapai, lai parādītu mārketinga saturu.

## <a name="add-an-order-details-module-to-a-page"></a>Pasūtījuma informācijas moduļa pievienošana lapā

Lai pievienotu pasūtījuma informācijas moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns** , lai izveidotu jaunu veidni.
1. Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukuma** ievadiet **Pasūtījuma informācijas veidnes** nosaukumu un pēc tam atlasiet **Labi**.
1. Slotā **Pamatteksts** atlasiet daudzpunkti ( **...** ) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Noklusējuma lapa** un pēc tam atlasiet **Labi**.
1. Moduļa **Noklusējuma lapa** slotā **Galvenais** atlasiet daudzpunkti ( **...** ) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Pasūtījuma informācija** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums** , lai priekšskatītu veidni. Pasūtījuma informācijas modulis netiks atveidots, jo tas prasa pasūtījuma apstiprināšanas numura kontekstu.
1. Atlasiet **Pabeigt rediģēšanu** , lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt** , lai publicētu to.
1. Dodieties uz **Lapas** un atlasiet **Jauns** , lai izveidotu jaunu lapu.
1. Dialoglodziņā **Izvēlēties veidni** atlasiet **Pasūtījuma informācijas veidne**. Sadaļā **Lapas nosaukums** ievadiet **Pasūtījuma informācijas lapa** pēc tam atlasiet **Labi**.
1. Moduļa **Noklusējuma lapa** slotā **Galvenais** atlasiet daudzpunkti ( **...** ) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Pasūtījuma informācija** un pēc tam atlasiet **Labi**.
1. Pasūtījuma informācijas moduļa rekvizītu rūtī atlasiet blakus zīmuļa simbolam **Virsraksts**.
1. Dialoglodziņa **Virsraksts** laukā **Virsraksta teksts** ievadiet virsraksta teksta **Pasūtījuma informāciju** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums** , lai priekšskatītu lapu.
1. Atlasiet **Pabeigt rediģēšanu** , lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt** , lai publicētu to.

## <a name="additional-resources"></a>Papildu resursi

[Groza modulis](add-cart-module.md)

[Groza ikonas modulis](cart-icon-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Maksājuma modulis](payment-module.md)

[Piegādes adreses modulis](ship-address-module.md)

[Piegādes opciju modulis](delivery-options-module.md)

[Dāvanu kartes modulis](add-giftcard.md)
