---
title: Izdevumu veidu iestatīšana
description: Šajā tēmā ir paskaidrots, kā līdzekļu pārvaldībā iestatīt izdevumu veidus.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseExpenseTypeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a1d6667a7c6fe1cd44196f2e753ca72b2ca97649
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880988"
---
# <a name="set-up-expense-types"></a>Izdevumu veidu iestatīšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā līdzekļu pārvaldībā iestatīt izdevumu veidus. Izmaksas, kas nav atainotas maksājumu grafikā, ir zināmas kā *Izdevumu izmaksas*. Šo izmaksu piemēri ietver īpašuma nodokļus, kopējās platības uzturēšanas izmaksas un apdrošināšanas izdevumus.

## <a name="add-an-administrative-expense-type"></a>Administratīvo izmaksu tipa pievienošana

1. Dodieties uz **Līdzekļu noma \> Iestatījumi \> Izdevumu tipi**.
2. Atlasiet **Jauns**.
3. Atbilstošajos laukos ievadiet jauno izdevumu tipu un aprakstu.

## <a name="assign-accounts-to-administrative-costs"></a>Piešķirt kontus administratīvajām izmaksām

Pēc tam saistiet kontus ar izdevumu tipiem. Šie konti tiks debetēti, kad tiks grāmatoti izdevumu grafika ieraksti. Korespondējošais konts ir norādīts **izpildes izmaksu maksājuma grafika** rindās katrai nomai.

1. Dodieties uz **Līdzekļu noma \> Iestatījumi \> Līdzekļu nomas parametri**.
2. Cilnes **Konti**, kas atrodas kopsavilkuma cilnē **Izpildes izmaksas**, laukā **Izdevumu tips** atlasiet izdevumu tipu.
3. Atlasiet **Pievienot**.
4. Laukā **Grāmatas tips** atlasiet grāmatas tipu, ko saistīt ar administratīvajām izmaksām.

    > [!NOTE]
    > Vairākus grāmatu tipus var saistīt ar vienu izdevumu kontu.

5. Laukā **Konta kods** norādiet, kurām nomām jālieto grāmata.

    - **Visi** — lietot grāmatu visām nomām.
    - **Grupa** — lietot grāmatu konkrētai nomu grupai.
    - **Tabula** — lietot grāmatu noteiktām nomām.

6. Ja laukā **Konta kods** atlasījāt **Tabula** vai **Grupa**, laukā **Konta/grupas numurs** atlasiet konta numuru vai grupas numuru.
7. Atbilstošajos laukos atlasiet finanšu nomas galveno kontu un operatīvas nomas galveno kontu.

Kad šīs darbības ir pabeigtas, varat pievienot izdevumus, izmantojot **izpildes izmaksu maksājuma grafika** rindas atlasītās nomas lapā **Līguma informācija**. Varat arī pievienot izdevumus, izveidojot jaunu nomu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
