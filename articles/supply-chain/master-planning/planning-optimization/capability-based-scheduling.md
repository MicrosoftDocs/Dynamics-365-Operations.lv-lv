---
title: Plānošana ar iespējā balstītu resursa atlasi
description: Šajā tēmā aprakstīta resursu plānošana bezgalīgās kapacitātes plānošanas laikā, kad norādāt iespējas kā resursu prasības darbībai.
author: ChristianRytt
ms.date: 9/3/2021
ms.topic: article
ms.search.form: RouteInventProd, WrkCtrTable, WrkCtrCapability
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 382814eb3d4322ed52bd39fcb22740201335614e
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/25/2021
ms.locfileid: "7679009"
---
# <a name="scheduling-with-resource-selection-based-on-capability"></a>Plānošana ar iespējā balstītu resursa atlasi

[!include [banner](../../includes/banner.md)]

Norādot resursu prasības ražošanas maršruta darbībai, jūs definējat vajadzīgos nosacījumus darbības izpildei. Piemēram, darbībai var būt vajadzīgs konkrēts resurss vai resursu grupa vai prasmju vai iespēju apvienojums. Šajā tēmā aprakstīta resursu plānošana bezgalīgās kapacitātes plānošanas laikā, kad norādāt iespējas kā resursu prasības darbībai.

## <a name="turn-on-the-capability-based-scheduling-feature"></a>Iespējā balstīta plānošanas rīka ieslēgšana

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Vispārējā plānošana*
- **Līdzekļa nosaukums**: *Bezgalīga noslodzes plānošana plānošanas optimizācijai*

Papildinformāciju par šo līdzekli skatiet sadaļā [Plānošana ar neierobežotu noslodzi](infinite-capacity-planning.md).

## <a name="capability-based-scheduling"></a>Iespējā balstīta plānošana

Iespēja ir operācijas resursu pieejamība konkrētas aktivitātes izpildīšanai. Vienam operācijas resursam var būt piešķirta vairāk nekā viena iespēja, un vienu iespēju var piešķirt vairāk nekā vienam resursam. Iespējas var piešķirt visu veidu resursiem, piemēram, rīkiem, piegādātājiem, iekārtām, vietām, telpām un cilvēkresursiem.

Norādot iespējas kā resursu prasības, varat atlikt resursu piešķiri, līdz nav ieplānoti pasūtījumi. Tā vietā, lai maršrutēšanas darbībai piešķirtu konkrētus resursus vai resursu grupas, varat definēt iespējas, kuras ir vajadzīgas katrai maršrutēšanas darbībai. Pēc tam plānošanas laikā sistēma saskaņo vajadzīgās prasības ar prasībām, kuras definētas resursiem. Sistēma atlasa tikai tos resursus, kuri atbilst prasībām.

Lai piešķirtu iespējas darbības resursam, izmantojiet kopsavilkuma cilni **Iespējas** no lapas **Resursi**. Lai piešķirtu resursu iespējai, izmantojiet kopsavilkuma cilni **Resursi** no lapas **Resursu iespējas**. Abas lapas ir pieejamas navigācijas rūts sadaļā **Ražošanas kontrole \> Iestatījumi \>Resursi**. Abas kopsavilkuma cilnes ietver režģi, kurā uzskaitīti resursi, kuri ir saistīti ar atlasīto resursu vai iespēju. Abas kopsavilkuma cilnes ietver arī rīkjoslu, kuru varat izmantot, lai režģī noņemtu, pievienotu un rediģētu rindas. Režģī ir iekļautas tālāk minētās kolonnas.

- **Resurss** vai **Iespēja** — Atlasiet resursu vai iespēju, kuru piesķir rinda.
- **Apraksts** — Ievadiet īsu resursa vai iespējas aprakstu.
- **Stājas spēkā** — Norādiet pirmo datumu, kurā tiek piemērota resursa vai iespējas piešķire. Plānošanas laikā sistēma nelietos resursu vai iespēju, kurai ir beigusies piešķire, pat, ja šis resurss atbilst prasībām.
- **Derīguma beigas** — Norādiet pēdējo datumu, kurā tiek piemērota resursa vai iespējas piešķire. Plānošanas laikā sistēma nelietos resursu vai iespēju, kurai ir beigusies piešķire, pat, ja šis resurss atbilst prasībām.
- **Līmenis** — Norādiet kvalifikācijas līmeni, kuram resursam jābūt attiecībā uz iespēju. Ja resursa vai iespējas prasībai norādāt vērtību **Vajadzīgais minimālais līmenis**, plānošanas rīks ņem resursa atlases laikā ņem vērā kvalifikācijas līmeni. Sistēma atlasa tikai tos resursus, kuriem ir nepieciešama iespēja līmenī, kas ir vienāds ar vai pārsniedz minimālo līmeni, kas norādīts resursu prasībā.
- **Prioritāte** — Šis lauks vēl nav atbalstīts Plānošanas optimizācijā. Taču, ja lietojat iebūvēto plānošanas rīku, varat lietot **Prioritātes** lauku resursa vai iespējas piešķirē, lai definētu resursa prioritāti. Ja lapā **Parametru plānošana** ir atlasīta lauka **Primāro resursu atlase** vērtība *Prioritāte*, plānošanas laikā sistēma vispirms atlasa resursu ar augtāko prioritāti (t.i., mazāko skaitlisko lauka **Prioritāte** vērtību).

## <a name="example"></a>Paraugs

Šajā piemērā parādīts, kā plānošanas rīks atlasa resursus, pamatojoties iespējā.

Ražošanas maršrutam ir piecas darbības: *10*, *20*, *30*, *40* un *50*. Katrai maršrutēšanas darbībai ir vajadzīgs resurss ar atšķirīgām iespējām. Piemēram, maršrutēšanas darbībai *10* ir vajadzīgs resurss, kuram ir iespēja samontēt skaļruni (*0050 Spkr Assembly*) un iespēja veikt darbus ar kokmateriāliem (*1010 Wood capabilities*). Maršrutēšanais darbībai *50* or vajadzīgs resurss ar iespēju iesaiņot preci (*0070 Saiņošanas iespēja*).

![Plānošanā izmantotā iespēja.](media/capability-based-scheduling.png "Plānošanā izmantotā iespēja.")

Plānošanas laikā rīks meklē resursus, kuri atbilst darbības prasībām. Piemēram, plānošanas rīks atlasa resursu *00101*, lai izpildītu darbību *10*, jo šis resurss ir pirmais atrastais resurss ar abām vajadzīgajām iespējām. Plānošanas rīks atlasa resursu *00301*, lai izpildītu darbību *50*, jo šis resurss ir vienīgais resurss ar iesaiņošanas iespēju.

Pēc tam ņemiet vērā, kā šis piemērs tiek ietekmēt, ja tiek izmantoti kvalifikācijas līmeņi:

- Darbībai *10* ir vajadzīgs minimālais kvalifikācijas līmenis *7* attiecībā uz iespēju *0059 Montāža*.
- Resursam *00101* ir kvalifikācijas līmenis *5* attiecībā uz iespēju *0059 Montāža*.
- Resursam *00102* ir kvalifikācijas līmenis *10* attiecībā uz iespēju *0059 Montāža*.

Šajā gadījumā bezgalīgās iespēju plānošanas laikā plānošanas rīks atlasa resursu *00102*, lai izpildītu darbību *10*, jo šim resursam, atšķirībā no resursa *00101* ir iespējai vajadzīgais kvalifikācijas līmenis.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
