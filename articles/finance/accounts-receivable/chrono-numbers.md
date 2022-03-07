---
title: Dokumentu un kvīšu hronoloģiska numerācija
description: Šajā tēmā skaidrots, kā iestatīt un izmantot hronoloģiskus numurus piemērojamiem dokumentiem un saistītajām kvītīm.
author: ikond
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ced09fb4be49dbfd10dac9f9ece86372d38e854460c7ca6cd72922c64ac7cce4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724139"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a>Dokumentu un kvīšu hronoloģiska numerācija

[!include [banner](../includes/banner.md)]


Dažās valstīs pastāv juridiska prasība numurēt dokumentus un saistītās kvītis hronoloģiskā secībā. Hronoloģija ir jāatbalsta ar periodiem. Visiem skaitļiem, kas attiecas uz agrākiem periodiem, jābūt mazākiem par skaitļiem, kas pieder vēlākiem periodiem. Lai atbilstu šai prasībai, ir ieviesta hronoloģiska numerācijas funkcionalitāte. Šajā tēmā skaidrots, kā konfigurēt un izmantot hronoloģiskus numurus piemērojamiem dokumentiem un saistītajām kvītīm.

## <a name="prerequisites"></a>Priekšnosacījumi

Līdzekļu pārvaldības darbvietā aktivizējiet **Hronoloģiskās numerācijas** līdzekli. Papildinformāciju skatiet [Līdzekļu pārvaldības pārskatā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="configure-chronological-numbering"></a>Konfigurēt hronoloģisku numerāciju

Hronoloģiska numerācija ietekmē tālāk norādītos dokumentus.

**Debitori**
- Rēķins debitoram
- Debitora rēķina dokuments
- Pārdošanas kredīta nota
- Pārdošanas kredīta notas dokuments
- Brīva teksta rēķins
- Rēķina dokuments brīvā tekstā
- Brīva teksta kredīta nota
- Kredīta notas dokuments brīvā tekstā
- Pavadzīme
- Pavadzīme
- Pavadzīmes storno dokuments
- Procentu paziņojums
- Atgādinājuma vēstule

**Kreditori**
- Rēķinu dokuments
- Kredīta nota
- Produktu ieejas plūsmas dokuments

**Projektu pārvaldība**
- Rēķins
- Rēķinu dokuments
- Kredīta piezīme
- Kredīta nota 

### <a name="define-number-sequences"></a>Numuru secību definēšana

Lai definētu numuru secības, dodieties uz **Organizācijas administrēšana** > **Numuru secības** > **Numuru secības**. Varat definēt tik daudz numuru secības, cik nepieciešams, lai segtu ietekmētos periodus nepieciešamajiem dokumentiem. 

Norādiet uzņēmumu katrai numuru secībai. Numuru secību segmentiem jābūt definētiem tā, lai tie periodiem nodrošinātu hronoloģiski secību. Piemēram, segmentu nosaukumi var ietvert īpašu prefiksu, kas identificē noteiktu periodu.

![Numuru secību iestatīšana.](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a>Konfigurēt numuru secību grupas

Lai konfigurētu numuru secību grupas, dodieties uz **Debitori** > **Iestatīšana** > **Debitoru parametri**. Cilnē **Numuru secības** definējiet tik daudz numuru secību grupu, cik nepieciešams, lai ietvertu ietekmētos periodus. 

Katrai grupai sadaļā **Atsauce** atlasiet vienu no atbalstītajām dokumenta atsaucēm un **Numuru secības koda** laukā skatiet numuru secību, kas iepriekš izveidota saistītajam periodam.

![Numuru sēriju grupas iestatījumi.](media/chrono-num-sequence-group.jpg)

Līdzīgi konfigurējiet numuru secību grupas moduļos **Kreditori** un **Projektu pārvaldība un uzskaite**.

### <a name="configure-number-sequence-groups-chronology"></a>Konfigurēt numuru secību grupu hronoloģiju

Lai konfigurētu numuru secību grupu hronoloģiju, dodieties uz **Organizācijas administrēšana** > **Numuru secības** > **Hronoloģiskas numuru secību grupas**. Definējiet numuru secību grupu piemērojamības nosacījumus.

![Hronoloģiska numuru iestatīšana.](media/chrono-num-sequence-group-period.jpg)

| Lauks            | Apraksts                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ir spēkā  | Numuru secību grupas piemērojamības sākuma datums. |
| Termiņa beigas      | Numuru secību grupas piemērojamības beigu datums. Ja netiek lietots beigu datums, atlasiet **Nekad**. |
| Numuru sēriju grupa | Numuru secību grupa, kas tiks izmantota dokumentu numuru ģenerēšanai periodā. |
| Oriģinālā numuru secību grupa | Šis numuru secības grupas kods tiek izmantots papildu filtrēšanai gadījumos, kad dokumentiem jau ir piešķirta noteikta *pastāvīga* numuru secību grupa. Tukša vērtība tiek uzskatīta par noteiktu vērtību. Ja ir jāignorē iepriekšējā piešķirtā grupa, šim iestatījumam izmantojiet opciju **Noklusējuma**. |
| Noklusētā vērtība | Ja ieslēgts, sistēma ignorē iepriekšējo piešķirto dokumenta numuru secību grupu un piemērojamības analīzei izmanto tikai periodu sākuma un beigu datumus. Ja izslēgts, atlasei sistēma izmanto pilnu kombināciju **Stājies spēkā** + **Derīguma termiņš** + **Sākotnējā numuru secību grupa**. |

## <a name="document-posting"></a>Dokumentu grāmatošana
Grāmatojot dokumentu, dokumentam tiek piešķirta atbilstoša numuru secību grupa, pamatojoties uz dokumenta grāmatošanas datumu, un pēc tam izmantota, lai ģenerētu dokumenta numuru, kas balstīts uz konstatēto numuru secību. Sistēma sniedz ziņojumu par numuru secību grupas piešķiri.

![Dokumenta numurs](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> Dažām valstīm jau ir noteikta loģika dokumentu numerācijai. Šajā gadījumā valstij noteiktā loģika pārrakstīs **Hronoloģiskās numerācijas** funkciju.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
