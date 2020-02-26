---
title: Pasūtījumu informācijas modulis
description: Šī tēma apskata pasūtījuma informācijas moduļus un apraksta, kā izmantot tos Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026021"
---
# <a name="order-details-module"></a>Pasūtījumu informācijas modulis


[!include [banner](includes/banner.md)]

Šī tēma apskata pasūtījuma informācijas moduļus un apraksta, kā izmantot tos Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Pasūtījumu informācijas moduli izmanto, lai rādītu pasūtījuma apstiprinājuma informāciju pēc pasūtījuma veikšanas. Tas parāda pasūtījuma apstiprinājuma ID, pasūtījuma kontaktinformāciju un citus pasūtījuma datus, piemēram, krājumus, kas tika iegādāti, maksājuma informāciju un nosūtīšanas metodi.

## <a name="order-confirmation-module-properties"></a>Pasūtījuma apstiprināšanas moduļa rekvizīti

| Rekvizīta nosaukums  | Vērtības | Apraksts |
|----------------|--------|-------------|
| Virsraksts        | Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**) | Pasūtījuma apstiprināšanas modulim var būt virsraksts. Pēc noklusējuma virsrakstam tiek izmantota **H2** virsraksta etiķete. Tomēr etiķeti var mainīt atbilstoši pieejamības prasībām. |
| Kontaktpersonas tālruņa numurs | Teksts | Kontaktpersonas numuru var sniegt ar pasūtījumu saistītiem jautājumiem. |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a>Moduļi, ko var izmantot pasūtījuma informācijas lapas modulī

Izveidojot pasūtījuma informācijas lapu, papildus pasūtījuma informācijas modulim varat pievienot citus atbilstošus moduļus. Daži piemēri:

- **Ieteikumu modulis** — ieteikumu moduli var pievienot pasūtījuma informācijas lapai, lai klientam ieteiktu citas preces.
- **Mārketinga moduļi** — jebkuru mārketinga moduli var pievienot pasūtījuma informācijas lapai, lai parādītu mārketinga saturu.

## <a name="create-an-order-details-page-module"></a>Pasūtījuma informācijas lapas moduļa izveide

1. Izveidojiet lapas veidni ar nosaukumu **Pasūtījuma informācijas veidne**.
1. Noklusētās lapas slotā **Galvenais** pievienojiet pasūtījuma informācijas moduli.
1. Pasūtījuma informācijas modulī pievienojiet ieteikumu moduli.
1. Saglabājiet un priekšskatiet veidni. Pasūtījuma informācijas modulis netiks atveidots, jo tas prasa pasūtījuma apstiprināšanas numura kontekstu.
1. Pabeidziet rediģēt veidni un publicējiet to.
1. Izmantojiet jūsu tikko izveidoto pasūtījuma informācijas veidni, lai izveidotu lapu ar nosaukumu **pasūtījuma informācijas lapa**.
1. Lapas strukturējumam pievienojiet noklusējuma lapu.
1. Slotā **Galvene** pievienojiet galvenes fragmentu.
1. Slotā **Kājene** pievienojiet kājenes fragmentu.
1. Slotā **Galvenais** pievienojiet pasūtījuma informācijas moduli.
1. Pasūtījuma informācijas moduļa rekvizītu rūtī pievienojiet virsrakstu **Pasūtījuma informācija**.
1. Zem pasūtījuma informācijas moduļa pievienojiet ieteikumu moduli un konfigurējiet to tā, lai tas izmantotu iestatījumus **Jauns** un **Vispirktākais**.
1. Saglabājiet un priekšskatiet lapu.
1. Pabeidziet rediģēt lapu un publicējiet to.

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Container modulis](add-container-module.md)

[Iegādes lodziņa modulis](add-buy-box.md)

[Groza modulis](add-cart-module.md)

[Izrakstīšanas modulis](add-checkout-module.md)

[Galvenes modulis](author-header-module.md)

[Kājenes modulis](author-footer-module.md)
