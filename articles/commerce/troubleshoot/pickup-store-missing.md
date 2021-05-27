---
title: Mazumtirdzniecības veikals netiek parādīts to veikalu sarakstā, no kuriem saņemt
description: Šajā tēmā ir sniegti problēmu novēršanas norādes, kas var palīdzēt, kad mazumtirdzniecības veikals netiek parādīts to veikalu sarakstā, kuros var saņemt preces.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ad7ddf8a17640471a2344c45eef76f682d29ef2b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020831"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a>Mazumtirdzniecības veikals netiek parādīts to veikalu sarakstā, no kuriem saņemt

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir sniegti problēmu novēršanas norādes, kas var palīdzēt, kad mazumtirdzniecības veikals netiek parādīts to veikalu sarakstā, kuros var saņemt preces.

## <a name="description"></a>Apraksts

Mazumtirdzniecības veikals netiek parādīts to veikalu sarakstā, kuros var saņemt preces.

## <a name="resolution"></a>Novēršana

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a>Veikala adreses garuma un platuma konfigurēšana programmā Commerce Headquarters

Lai konfigurētu veikala adreses garumu un platumu programmā Commerce Headquarters, veiciet tālāk minētās darbības.

1. Parejiet uz **Mazumtirdzniecība un komercija \> Kanāli \> Veikali \> Visi veikali**.
1. Atrodiet veikalu, kuru vēlaties redzēt saņemšanas opcijās e-komercijas vietnē. Atzīmējiet tās vērtību **Pārvaldības struktūrvienības numurs**.
1. Pārejiet uz sadaļu **Organizācijas administrēšana \> Organizācijas \> Pārvaldības struktūrvienības**.
1. Meklējiet pārvaldības struktūrvienības numuru, ko iepriekš atzīmējāt, un pēc tam meklēšanas rezultātos atlasiet pārvaldības struktūrvienību.
1. Kopsavilkuma cilnē **Adreses** atlasiet **Papildu opcijas** un pēc tam atlasiet **Papildu**.
1. Kopsavilkuma cilnē **Vispārīgi** pārliecinieties, vai lauki **Garums** un **Platums** ir pareizi iestatīti. Šīs darbības ietvaros pārliecinieties, vai vērtības ir pareizi norādītas kā pozitīvi vai negatīvi skaitļi.

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a>Izpildes grupu konfigurēšana programmā Commerce Headquarters

Lai konfigurētu izpildes grupas Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Kanāli \> Tiešsaistes veikali**.
1. Atlasiet konfigurējamo tiešsaistes veikalu.
1. Darbību rūtī atlasiet cilni **Iestatīšana** un pēc tam atlasiet **Izpilde/grupas piešķire**.
1. Lapā **Izpilde/s grupas piešķire** atlasiet tiešsaistes veikala izpildes grupu.
1. Sadaļā **Iestatījumi** pārliecinieties, vai mazumtirdzniecības veikals ir pareizi konfigurēts izpildes grupai.

## <a name="additional-resources"></a>Papildu resursi 

[Pārvaldības struktūrvienības izveide](../../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md)

[Tiešsaistes kanāla iestatīšana](../channel-setup-online.md)