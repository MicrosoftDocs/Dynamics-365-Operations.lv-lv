---
title: Numura zīmes saņemšana, izmantojot noliktavas programmu
description: Šajā tēmā skaidrots, kā iestatīt noliktavas programmu, lai atbalstītu numura zīmes saņemšanas procesa izmantošanu, lai saņemtu fizisko krājumu.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 7d5ac6598ab80ece0164d7c92f5d84e91d21b385
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346380"
---
# <a name="license-plate-receiving-via-the-warehousing-app"></a>Numura zīmes saņemšana, izmantojot noliktavas programmu

Šajā tēmā skaidrots, kā iestatīt noliktavas programmu, lai tā atbalstītu numura zīmes saņemšanas procesa izmantošanu, lai saņemtu fizisko krājumu.

Jūs varat izmantot šo funkcionalitāti, lai ātri ierakstītu ienākošo krājumu saņemšanu, kas ir saistīts ar iepriekšējo paziņojums par nosūtīšanu (ASN). Sistēma automātiski izveido ASN, kad noliktavas pārvaldības procesi tiek izmantoti, lai nosūtītu pārsūtīšanas pasūtījumu. Pirkšanas pasūtījuma procesam ASN var tikt manuāli reģistrēts, vai to var automātiski importēt, izmantojot ienākošo ASN datu elementa procesu.

ASN dati ir saistīti ar noslodzēm un kravām, izmantojot *iepakošanas struktūras*, kur paletes (standarta numura zīmes) var ietvert gadījumus (ligzdotas numura zīmes).

> [!NOTE]
> Lai samazinātu krājumu transakciju skaitu, kad tiek izmantotas iepakojuma struktūras, kurām ir ligzdotas numura zīmes, sistēma reģistrē fiziskos rīcībā esošos krājumus uz pamatnumura zīmes. Lai izraisītu fizisko rīcībā esošo krājumu pārvietošanu no pamatnumura zīmes uz ligzdotajām numura zīmēm, kas balstītas uz iepakojuma struktūras datiem, mobilajai ierīcei ir jānorāda izvēlnes elements, kas ir atkarīgs no *Ligzdotu licenču plāksnīšu iepakošanas* darba izveides procesiem.

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a>Rādīt vai izlaist saņemšanas kopsavilkuma lapu

Jūs varat izmantot līdzekli *Kontrolēt, vai mobilajās ierīcēs tiktu parādīta saņemšanas kopsavilkuma lapa*, lai izmantotu papildu detalizēto noliktavu programmu plūsmu kā daļu no numura zīmes saņemšanas procesa.

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas vadība*
- **Līdzekļa nosaukums:** *kontrolē, vai mobilajās ierīcēs tiek parādīta saņemšanas kopsavilkuma lapa*

Kad šis līdzeklis ir ieslēgts, mobilās ierīces izvēlnes vienumi numura zīmes saņemšanas vai numura zīmes saņemšanas un izvietošanas laikā nodrošinās iestatījumu **Parādīt saņemšanas kopsavilkuma lapu**. Šim iestatījumam ir šādas opcijas:

- **Rādīt detalizētu kopsavilkumu** — veicot numura zīmes saņemšanu, darbinieki redzēs papildu lapu, kas parāda pilnu ASN informāciju.
- **Izlaist kopsavilkumu** — darbinieki neredzēs pilnu ASN informāciju. Noliktavas darbinieki arī saņemšanas procesa laikā nevarēs iestatīt izvietojuma kodu vai pievienot izņēmumus.

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>Nepieļaut nodošanas pasūtījuma nosūtīto numura zīmju izmantošanu noliktavās, kas nav galamērķa noliktava

Nevar izmantot numura zīmes saņemšanas procesu, ja ASN ietver numura zīmes ID, kas jau eksistē un kam ir fiziski rīcībā esošie dati noliktavas atrašanās vietā, kas atšķiras no noliktavas atrašanās vietas, kur notiek numura zīmes reģistrācija.

Pārsūtīšanas pasūtījumu scenārijiem, kuros tranzīta noliktava neseko numura zīmēm (un tāpēc arī neseko līdzi katras numura zīmes fiziskajam inventāram uz vietas), varat izmantot līdzekli *Nepieļaut nodošanas pasūtījuma nosūtīto numura zīmju izmantošanu noliktavās, kas nav galamērķa noliktava*, lai novērstu to, ka fiziskas rīcībā esošas numura zīmes ir pieejamas tranzītā.

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas vadība*
- **Līdzekļa nosaukums:** *Nepieļaut nodošanas pasūtījuma nosūtīto numura zīmju izmantošanu citās noliktavās, kas nav galamērķa noliktava*

Lai pārvaldītu funkcionalitāti, kad šī funkcija ir pieejama, veiciet šādas darbības.

1. Doties uz **Noliktavas vadība\> Iestatīšana \> Noliktavas vadības parametri**.
1. Cilnē **Vispārīgi** kopsavilkuma cilnē **Numura zīmes**  iestatiet **Tranzīta noliktavas numura zīmes politikas** lauku uz vienu no šīm vērtībām:

    - **Atļaut nereģistrētas numura zīmes atkārtotu izmantošanu** — sistēma darbojas tādā pašā veidā, kā tas darbojas, kad līdzeklis *Nepieļaut nodošanas pasūtījuma nosūtīto numura zīmju izmantošanu citās noliktavās, kas nav galamērķa noliktava* nav pieejams. Šī vērtība ir noklusētais iestatījums, pirmoreiz aktivizējot līdzekli.
    - **Novērst nereģistrētas numura zīmju atkārtotu izmantošanu** - līdz pārsūtīšanas pasūtījuma saņemšanai mērķa noliktavā tiks atļauti tikai rīcībā esošie atjauninājumi, kas saistīti ar nosūtītajām numura zīmēm.

## <a name="more-information"></a>Papildinformācija

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

Papildinformāciju par mobilās ierīces izvēlnes elementiem skatiet [Mobilo ierīču iestatīšana noliktavas darbam](configure-mobile-devices-warehouse.md).
