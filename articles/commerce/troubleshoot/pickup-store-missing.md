---
title: Mazumtirdzniecības veikals netiek parādīts to veikalu sarakstā, no kuriem saņemt
description: Šajā rakstā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt, kad mazumtirdzniecības veikals nav pieejams to veikalu sarakstā, kuros var saņemt preces.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: b6cec3d9d598be221516506388e4797ad579a610
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286757"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a>Mazumtirdzniecības veikals netiek parādīts to veikalu sarakstā, no kuriem saņemt

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt, kad mazumtirdzniecības veikals nav pieejams to veikalu sarakstā, kuros var saņemt preces.

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
