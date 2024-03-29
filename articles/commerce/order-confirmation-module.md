---
title: Pasūtījuma apstiprinājuma modulis
description: Šis raksts aptver pasūtījuma apstiprinājuma moduļus un apraksta, kā tos lietot Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 6011c7e4713813a02fa8f812ea8981fd6fa0253f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269140"
---
# <a name="order-confirmation-module"></a>Pasūtījuma apstiprinājuma modulis

[!include [banner](includes/banner.md)]

Šis raksts aptver pasūtījuma apstiprinājuma moduļus un apraksta, kā tos lietot Microsoft Dynamics 365 Commerce.

Pasūtījumu apstiprinājuma moduli izmanto, lai rādītu pasūtījuma apstiprinājuma informāciju pēc pasūtījuma veikšanas. Tas parāda pasūtījuma apstiprinājuma ID, pasūtījuma kontaktinformāciju un citus pasūtījuma datus, piemēram, krājumus, kas tika iegādāti, maksājuma informāciju, saņemšanas iespējas un nosūtīšanas metodi.

## <a name="order-confirmation-module-properties"></a>Pasūtījuma apstiprināšanas moduļa rekvizīti

| Rekvizīta nosaukums  | Vērtības | Apraksts |
|----------------|--------|-------------|
| Virsraksts        | Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**) | Pasūtījuma apstiprināšanas modulim var būt virsraksts. Pēc noklusējuma virsrakstam tiek izmantota **H2** virsraksta etiķete. Tomēr etiķeti var mainīt atbilstoši pieejamības prasībām. |
| Kontaktpersonas tālruņa numurs | Teksts | Kontaktpersonas numuru var sniegt ar pasūtījumu saistītiem jautājumiem. |
| Rādīt saņemšanas laika loga informācija | Patiess vai aplams | Šis rekvizīts ir pieejams risinājumā Dynamics 365 Commerce 10.0.15 un jaunākos. Kad patiess, tas rāda saņemšanas laika loga informāciju, ja tas ir paredzēts saņemšanas krājumam|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a>Moduļi, ko var izmantot pasūtījuma konfigurācijas lapas modulī

Izveidojot pasūtījuma konfigurācijas lapu, papildus pasūtījuma konfigurācijas modulim varat pievienot citus atbilstošus moduļus. Daži piemēri:

- **Ieteikumu modulis** — ieteikumu moduli var pievienot pasūtījuma konfigurācijas lapai, lai klientam ieteiktu citas preces.
- **Mārketinga moduļi** — jebkuru mārketinga moduli var pievienot pasūtījuma konfigurācijas lapai, lai parādītu mārketinga saturu.

## <a name="add-an-order-confirmation-module-to-a-page"></a>Pasūtījuma konfigurācijas moduļa pievienošana lapā

Lai pievienotu pasūtījuma konfigurācijas moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.
1. Dialoglodziņā Jauna **veidne ar** veidnes nosaukumu ievadiet **pasūtījuma** apstiprinājuma veidnes nosaukumu **un** pēc tam atlasiet **Labi**.
1. Pamatteksta **slotā** atlasiet daudzpunkti (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet noklusējuma lapas **moduli** un pēc tam atlasiet **Labi**.
1. Noklusējuma lapas **moduļa** galvenajā **slotā** atlasiet daudzpunkti (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet pasūtījuma apstiprināšanas **moduli un** pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu veidni. Pasūtījuma apstiprināšanas modulis netiks atveidots, jo tas prasa pasūtījuma apstiprināšanas numura kontekstu.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.
1. Dialoglodziņa Izveidot **jaunu lapu sadaļā** Lapas nosaukums ievadiet **pasūtījuma** apstiprināšanas lapu **un pēc** tam atlasiet **Tālāk**.
1. Sadaļā **Izvēlēties veidni atlasiet** pasūtījuma apstiprinājuma **veidni un** pēc tam atlasiet **Tālāk**.
1. Sadaļā **Izvēlēties izkārtojumu atlasiet** lapas izkārtojumu (piemēram, Elastīgs **izkārtojums**) un pēc tam atlasiet **Tālāk**.
1. Sadaļā **Pārskatīt un pabeigt** pārskatiet lapas konfigurāciju. Ja jums ir jārediģē lapas informācija, atlasiet **Atpakaļ**. Ja lapas informācija ir pareiza, atlasiet Izveidot **lapu**. 
1. Noklusējuma lapas **moduļa** galvenajā **slotā** atlasiet daudzpunkti (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet pasūtījuma apstiprināšanas **moduli un** pēc tam atlasiet **Labi**.
1. Pasūtījuma konfigurācijas moduļa rekvizītu rūtī atlasiet blakus zīmuļa simbolam **Virsraksts**.
1. Dialoglodziņa **Virsraksts** laukā **Virsraksta teksts** ievadiet virsraksta teksta **Pasūtījuma konfigurāciju** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="additional-resources"></a>Papildu resursi

[Groza modulis](add-cart-module.md)

[Groza ikonas modulis](cart-icon-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Maksājumu modulis](payment-module.md)

[Piegādes adreses modulis](ship-address-module.md)

[Piegādes opciju modulis](delivery-options-module.md)

[Saņemšanas informācijas modulis](pickup-info-module.md)

[Dāvanu kartes modulis](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
