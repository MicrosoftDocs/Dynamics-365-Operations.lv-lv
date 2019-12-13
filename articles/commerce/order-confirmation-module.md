---
title: Pasūtījuma apstiprināšanas modulis
description: Šī tēma apskata pasūtījuma apstiprināšanas moduļus un apraksta, kā izveidot tos Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698330"
---
# <a name="order-confirmation-module"></a>Pasūtījuma apstiprināšanas modulis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šī tēma apskata pasūtījuma apstiprināšanas moduļus un apraksta, kā izveidot tos Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Pasūtījuma apstiprināšanas modulis tiek izmantots, lai pasūtījuma apstiprināšanas lapā pēc pasūtījuma veikšanas parādītu apstiprinājuma ziņojumu. Pasūtījuma apstiprināšanas modulis parāda pasūtījuma apstiprināšanas numuru un klienta e-pasta adresi, kas tika sniegta izrakstīšanas laikā.

Kad pasūtījums tiek veikts izrakstīšanas laikā, pasūtījuma apstiprināšanas numurs un klienta e-pasta adrese tiek nodoti pasūtījuma apstiprināšanas lapai kā vaicājuma virkne lapas URL. Pasūtījuma apstiprināšanas modulis saņem šo informāciju un atveido pasūtījuma statusu pasūtījuma apstiprināšanas lapā. Pasūtījuma apstiprināšanas modulim nepieciešams šis lapas konteksts, lai nodrošinātu pasūtījuma statusu.

## <a name="order-confirmation-module-properties"></a>Pasūtījuma apstiprināšanas moduļa rekvizīti

| Rekvizīta nosaukums | Vērtības | Apraksts |
|---------------|--------|-------------|
| Virsraksts       | Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**) | Pasūtījuma apstiprināšanas modulim var būt virsraksts. Pēc noklusējuma virsrakstam tiek izmantota **H2** virsraksta etiķete. Tomēr etiķeti var mainīt atbilstoši pieejamības prasībām. |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a>Moduļi, ko var izmantot pasūtījuma apstiprināšanas lapas modulī 

- **Ieteikumi** — ieteikumu moduli var ievietot pasūtījuma apstiprināšanas lapā, lai klientam ieteiktu citas preces.
- **Mārketings** — mārketinga modulis var pievienot mārketinga saturu pasūtījuma apstiprināšanas lapai.

## <a name="create-an-order-confirmation-page-module"></a>Pasūtījuma apstiprināšanas lapas moduļa izveide

1. Izveidojiet lapas veidni ar nosaukumu **pasūtījuma apstiprināšanas veidne**.
1. Noklusētās lapas slotā **Galvenais** pievienojiet pasūtījuma apstiprināšanas moduli.
1. Pasūtījuma apstiprināšanas modulī pievienojiet ieteikumu moduli.
1. Saglabājiet un priekšskatiet veidni. Pasūtījuma apstiprināšanas moduli nedrīkst atveidot, jo tas prasa pasūtījuma apstiprināšanas numura kontekstu.
1. Pārbaudiet veidni un publicējiet to.
1. Izmantojiet jūsu tikko izveidoto pasūtījuma apstiprināšanas veidni, lai izveidotu lapu ar nosaukumu **pasūtījuma apstiprināšanas lapa**.
1. Lapas strukturējumam pievienojiet noklusējuma lapu.
1. Slotā **Galvene** pievienojiet galvenes fragmentu.
1. Slotā **Kājene** pievienojiet kājenes fragmentu.
1. Slotā **Galvenais** pievienojiet pasūtījuma apstiprināšanas moduli.
1. Pasūtījuma apstiprināšanas moduļa rekvizītu rūtī pievienojiet virsrakstu **Pasūtījuma apstiprinājums**.
1. Zem pasūtījuma apstiprināšanas moduļa pievienojiet ieteikumu moduli un konfigurējiet to tā, lai tas izmantotu iestatījumus **Jauns** un **Vispirktākais**.
1. Saglabājiet un priekšskatiet lapu, reģistrējiet un publicējiet to.

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Container modulis](add-container-module.md)

[Iegādes lodziņa modulis](add-buy-box.md)

[Groza modulis](add-cart-module.md)

[Izrakstīšanas modulis](add-checkout-module.md)

[Galvenes modulis](author-header-module.md)

[Kājenes modulis](author-footer-module.md)
