---
title: Redzamība materiālu izņēmumos
description: Šajā tēmā ir aprakstīts, kā varat iegūt labāku redzamību par izņēmumiem attiecībā uz izejmateriāliem ražošanas pasūtījumos un partijas pasūtījumos.
author: johanhoffmann
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgShopSupervisorWorkspace, WHSProdWaveTableListPage, WHSProdWaveTableManageBOMPool
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: d3ea260535e76d7ac3d73d4bca930b7b4b2d22b2b2c076d4d1346785eaed85b8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726805"
---
# <a name="visibility-into-material-exceptions"></a>Redzamība materiālu izņēmumos

[!include [banner](../includes/banner.md)]

Darbvietā **Ražošanas pārvaldība** labāku redzamību par izņēmumiem attiecībā uz izejmateriāliem ražošanas pasūtījumos un partijas pasūtījumos jums nodrošina trīs elementi.

- Neizlaistās materiālu rindas, kam jāpievērš uzmanība
- Neapstrādātie kopumi, kuriem jāpievērš uzmanība
- Atvērtais noliktavas darbs, kam jāpievērš uzmanība

Visos trīs elementos materiālu komplekta (MK) rindu un formulas rindu izejmateriālu datums tiek salīdzināts ar darbvietas datumu, kā arī ar filtriem, kas iestatīti vienumiem **Ražošanas vienība**, **Resursu grupa** un **Resurss** — šie vienumi ir iestatīti izvēlnē **Konfigurēt manu darbvietu**. Darbvietas datums pēc noklusējuma ir iestatīts uz pašreizējo datumu, bet varat to regulēt.

Neizlaistai MK rindai vai formulas rindai ir jāpievērš uzmanība, ja rindas izejmateriālu datums ir vienāds ar vai agrāks par darbvietas datumu, kā arī gadījumos, ja tas atbilst darbvietas filtru noteiktajiem kritērijiem.

Nākamajā attēlā zilā josla norāda ražošanas darbu, kurš ir plānots kādam resursam. Šim darbam ir plānots sākties 2017. gada 1. maijā (01.05.2017.). Šis datums ir izejmateriālu datums. Citiem vārdiem sakot — šajā datumā ir jābūt gataviem materiāliem, kas šim darbam ir piešķirti MK un formulas rindās. Otrs attēlā redzamais datums, 2017. gada 6. maijs (06.05.2017.), apzīmē darbvietas datumu. Šajā piemērā izejmateriālu datums ir agrāks par darbvietas datumu. Tādēļ datums, kad izejmateriālu patēriņam bija plānots sākties, ir pagājis, un MK un formulas rindas atbilst kritērijiem par nepieciešamību pievērst uzmanību.

![Ražošanas darba piemērs, kur izejmateriālu datums ir agrāks par darbvietas datumu.](./media/improved-visibility.png)

## <a name="unreleased-material-lines-needing-attention"></a>Neizlaistās materiālu rindas, kam nepieciešama uzraudzība

MK vai formulas rindu var izlaist nosūtīšanai uz noliktavu trīs tālāk norādītajos veidos.

- Kā daļu no ražošanas pasūtījuma vai partijas pasūtījuma izlaišanas
- Kā manuālu izlaišanu
- Automātiski, izmantojot pakešuzdevumu

Papildinformāciju skatiet šeit: [MK un formulas rindu izlaišana nosūtīšanai uz noliktavu](releasing-bom-and-formula-lines-to-warehouse.md). 

Ja kāda MK vai formulas rinda nav izlaista vai ir izlaista tikai daļēji, kā arī, ja ir izpildīti darbvietas datuma un filtra kritēriji, šī rinda tiek ietverta elementā **Neizlaistās materiālu rindas, kam jāpievērš uzmanība** rādītā skaitļa aprēķinā.

Kad atlasāt šo elementu, tiek atvērta lapa **Pārvietot uz noliktavu**. Šajā lapā tiek rādīts neizlaisto MK un formulas rindu skaits, kas tiek norādīts ar skaitli šajā elementā. Neizlaistās rindas ir redzamas augšējā režģī. Šajā režģī tiek radīts daudzums, kas rindai bija sākotnēji prognozēts, daudzums, kas jau ir izlaists, un atlikušais daudzums, kas joprojām ir jālaiž. Varat pievienot rindas no augšējā režģa uz apakšējo režģi. Pēc tam no apakšējā režģa atlasītās rindas varat izlaist pārvietošanai uz noliktavu. No apakšējā režģa varat arī pielāgot izlaižamo daudzumu, lai tiktu izlaists tikai daļējs daudzums.

## <a name="unprocessed-waves-needing-attention"></a>Neapstrādātie kopumi, kuriem jāpievērš uzmanība

Kad MK vai formulas rinda tiek izlaista, atkarībā no ražošanas kopuma veidnes konfigurācijas tā tiek pievienota jaunam ražošanas kopumam vai jau pastāvošam atvērtam kopumam. Izmantojot laidiena veidnes konfigurāciju, kopumu varat arī iestatīt tā, lai tas tiktu apstrādāts automātiski, kad tiek izlaista MK vai formulas rinda. Kad kopums ir apstrādāts, tiek ģenerēts noliktavas darbs izejmateriālu izdošanai. Ja laidiena veidne ir konfigurēta tā, ka kopumi netiek apstrādāti izlaišanas laikā, šis kopums saglabājas neapstrādātā stāvoklī. Elementā **Neapstrādātie kopumi, kuriem jāpievērš uzmanība** tiek rādīts skaits ar MK un formulas rindām, kas ir izlaistas pārvietošanai uz noliktavu neapstrādātos laidienos un kam izejmateriālu datums ir agrāks par vai vienāds ar darbvietas datumu. Šis rindas ir nepieciešams arī patērēt ar operācijas resursu, kas attiecas uz darbvietas filtru.

Kad šis elements tiek atlasīts, tiek atvērta lapa **Visi ražošanas kopumi**. Šī lapa tiek filtrēta pēc tādu atvērto kopumu skaita, kuros ir kopuma rindas no izlaistajām MK un formulas rindām, kas atbilst šī elementa kritērijiem.

### <a name="manually-maintain-production-waves"></a>Manuāli uzturēt ražošanas kopumus

Lapā **Visi ražošanas kopumi** varat izmantot pogas darbības rūts cilnē **Kopums**, lai manuāli **Apstrādātu** un **Izlaistu** laidienu. Varat izmantot arī opciju **Uzturēt ražošanas**, lai skatītu un uzturētu **Ražošanas MK kopas datus**, kas tiek lietoti, lai apstrādātu sakārtošanas procesu.

## <a name="open-warehouse-work-needing-attention"></a>Atvērtais noliktavas darbs, kam nepieciešama uzraudzība

Elementā **Atvērtais noliktavas darbs, kam jāpievērš uzmanība** tiek rādīts skaits ar MK un formulas rindām, kuras ir izlaistas pārvietošanai uz noliktavu, kurās ir neapstrādāts darbs un kurās izejmateriālu datums ir agrāks par vai vienāds ar darbvietas datumu. Šis rindas ir nepieciešams arī patērēt ar operācijas resursu, kas attiecas uz darbvietas filtru.

Kad šis elements tiek atlasīts, tiek atvērta lapa **Viss darbs**. Šī lapa tiek filtrēta pēc tādu atvērto darba virsrakstu skaita, kuros ir darba rindas no izlaistajām MK un formulas rindām, kas atbilst šī elementa kritērijiem. No lapas **Viss darbs** šo darbu varat apstrādāt manuāli.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]