---
title: PVN specifikācija pēc virsgrāmatas darbības pārskata
description: Šajā tēmā tiek skaidrots, kā izmantot PVN specifikāciju pēc virsgrāmatas darbību pārskata, lai skatītu un drukātu informāciju par virsgrāmatas darbībām, kas tiek aprēķinātas ar PVN.
author: ericwang
manager: Ann Beebe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 438a640124e778b839c660f5e161efa22c319af0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445441"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a>PVN specifikācija pēc virsgrāmatas darbības pārskata
[!include [banner](../includes/banner.md)]

Šajā tēmā tiek skaidrots, kā izmantot **PVN specifikācija pēc virsgrāmatas darbības** pārskatu, lai skatītu un drukātu informāciju par virsgrāmatas darbībām, kas tiek aprēķinātas ar PVN.

## <a name="tax-accounts-vs-non-tax-accounts"></a>Nodokļu kinti vs. ar nodokļiem neapliekamie konti

**PVN specifikācija pēc virsgrāmatas darbības** pārskats parāda nodokļu darbības gan nodokļu kontos, gan ar nodokļiem neapliekamajos kontos. Šie konti tiek iedalīti kategorijās šādā veidā:

- **Nodokļu konts** — tiek uzskatīts, ka konts ir nodokļu konts, kad tiek grāmatota nodokļu darbība, un galvenais konts **PVN** žurnāla rindā ir nodokļu konts, piemēram, PVN maksājuma konts vai PVN saņemēja konts.
- **Ar nodokļiem neapliekamais konts**— tiek uzskatīts, ka konts ir ar nodokļiem neapliekamais konts, kad tiek grāmatota nodokļu darbība, un galvenais konts sākotnējā darbībā ir ar nodokļiem neapliekamais konts, piemēram, ieņēmumu konts vai izdevumu konts.

Nodokļu kontiem, **Izcelsme**, **PVN ienākumi** un **PVN maksājami** pārskata kolonnas rāda **0** (nulle). Ar nodokļiem neapliekamajiem kontiem, šīs kolonnas rāda summas.

## <a name="filtering-the-data-on-the-report"></a>Filtrējot pārskatā parādītos datus.

Veidojot pārskatu, ie pieejami tālāk norādītie noklusējuma lauki. Izmantojot šos laukus, jūs varat filtrēt pārskatā ietvertos datus.

| Lauks                      | Apraksts |
|----------------------------|-------------|
| Datums                       | Izmantojiet laukus sadaļās **No** un **Līdz** , lai noteiktu datumu diapazonu nodokļu darbībām. |
| Galvenais konts               | Izmantojiet laukus sadaļās **No** un **Līdz** , lai noteiktu datumu diapazonu galvēniem kontiem. |
| PVN kods             | Izmantojiet laukus sadaļās **No** un **Līdz** , lai noteiktu datumu diapazonu PVN kodiem. |
| Grupēšana                   | Atlasiet, vai pārskats ir jāsagrupē pēc virsgrāmatas konta vai PVN koda. |
| Apakšsumma pēc PVN koda | Iestatiet šo opciju uz **Jā**, lai parādītu starpsummas pēc PVN koda. |
| Tikai kopsummas                | Iestatiet šo opciju uz **Jā**, lai rādītu tikai kopsummas. |
| Tikai galvenie konti         | Iestatiet šo opciju uz **Jā**, lai pārskatā iekļautu tikai galvenos kontus. |

## <a name="showing-only-non-tax-accounts-on-the-report"></a>Rādīt pārskatā tikai ar nodokļiem neapliekamos kontus

Lai pārskatā rādītu tikai ar nodokļiem neapliekamos kontus, iestatiet filtra nosacījumu, piemēram, zvaigznīti (\*), kā parādīts sekojošajā ilustrācijā.

![Pārskats, kas parāda ar nodokļiem neapliekamos kontus](media/taxspecperledgertrans.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]