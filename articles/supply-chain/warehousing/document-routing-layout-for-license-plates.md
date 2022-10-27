---
title: Dokumentu maršrutēšanas etiķešu izkārtojumi
description: Šajā rakstā ir aprakstīts, kā izmantot formatēšanas metodes vērtību drukāšanai uz etiķetēm.
author: perlynne
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: a4e0c16b71c257cae832870ca58679884047ea16
ms.sourcegitcommit: 9e6a9d644a34158390c6e209e80053ccbdb7d974
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708650"
---
# <a name="document-routing-label-layout"></a>Dokumentu maršrutēšanas uzlīmes izkārtojums

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā izveidot noliktavas vienības, konteinera un kopuma etiķešu izkārtojumus. Tā arī sniedz vadlīnijas par To, kā lietot Papildmaksas programmēšanas valodu (ZPL), kas tiek lietota izkārtojumu izveidošanai.

Dokumentu maršrutēšanas etiķešu izkārtojumi nosaka veidu, kādā etiķetes tiek noteiktas un uz tiem izdrukātie dati. Konfigurējiet drukāšanas trigera punktus, iestatot mobilās ierīces izvēlnes elementus un darba veidnes.

Informācija šajā dokumentā attiecas uz visiem dokumentu maršrutēšanas etiķešu izkārtojumiem, [tostarp](tasks/license-plate-label-printing.md) numura zīmes etiķešu, [konteinera](print-container-labels.md) etiķešu un kopuma etiķešu [izkārtojumiem](configure-wave-label-printing.md).

Jūs varat drukāt augstas sarežģītības etiķetes, ar nosacījumu, ka drukas ierīce spēj interpretēt tai sūtīto tekstu. Piemēram, ZPL izkārtojums, kas ietver svītrkodu, var būt līdzīgs šim piemēram.

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

Kā daļa no etiķešu drukāšanas procesa teksts `$LicensePlateId$` šajā piemērā tiks aizstāts ar datu vērtību. Vairāki plaši pieejami etiķešu ģenerēšanas rīki var jums palīdzēt formatēt etiķetes izkārtojuma tekstu. Daudzi no šiem rīkiem atbalsta `$FieldName$` formātu. Turklāt Microsoft Dynamics 365 Supply Chain Management izmanto īpašu formatēšanas loģiku kā daļu no lauka kartējuma dokumenta maršrutēšanas izkārtojumam.

Lai apskatītu vērtības, kas tiks drukātas, dodieties uz **Noliktavas pārvaldība \> Vaicājumi un pārskati \> Numura zīmes etiķetes**.

## <a name="turn-on-this-feature-for-your-system"></a>Līdzekļa ieslēgšana sistēmā

Ja sistēmā vēl nav ietverti šajā rakstā aprakstītie līdzekļi, [...](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)*pārejiet uz sadaļu Līdzekļu pārvaldība un slēdziet līdzekli Uzlabotie numura zīmes etiķešu izkārtojumi.* (No Piegādes ķēdes pārvaldības versijas 10.0.21, šī funkcija ir ieslēgta pēc noklusējuma. Attiecībā uz Piegādes ķēdes pārvaldību 10.0.25 šī funkcija ir obligāta un to nevar izslēgt.)

## <a name="custom-number-formats"></a>Pielāgoti skaitļu formāti

Jūs varat pielāgot formatējumu skaitliskām lauka vērtībām, kas tiek drukātas, izmantojot kodus, kuriem ir šāds formāts.

```dos
$FieldName:FormatString$
```

Tālāk minēts šī formāta paskaidrojums:

- `FieldName` ir datu lauka nosaukums (piemēram, **Daudzums**).
- `FormatString` nosaka, kā jādrukā dati.

Sekojošie piemēri parāda, kā varat pielāgot darba daudzuma (**Daudzums**) lauku:

- Lai vienmēr parādītu četrus ciparus (izmantojot nulles kā vietturus), lietojiet `$Qty:0000$`. Piemēram, ja daudzums ir 10, etiķetē tiks parādīts "0010".
- Lai vienmēr parādītu divas decimāldaļas vietas, izmantojiet `$Qty:0.00$`. Piemēram, ja daudzums ir 10, etiķetē tiks parādīts "10.00".

Pilnīgu pieejamo skaitļu formāta virkņu sarakstu skatiet [Pielāgotās skaitļu formāta virknes](/dotnet/standard/base-types/custom-numeric-format-strings).

## <a name="custom-string-formats"></a>Pielāgotu virkņu formāti

Jūs varat noņemt virknes pirmās rakstzīmes, izmantojot šādu lauku un formāta kodu.

```dos
$FieldName:#..$
```

Šeit `#` norāda izlaisto rakstzīmju skaitu. Piemēram, lai drukātu Sērijas pārvadāšanas konteinera koda (SSCC) numura zīmes numuru, kurā nav iekļautas pirmās divas rakstzīmes, izmantojiet `$LicensePlateId:2..$`. Šādā gadījumā numura zīmes numurs 0011111111111222221 tiks drukāts kā "11111111111222221".

## <a name="custom-datetime-formats"></a>Pielāgotie datuma/laika formāti

Šajā piemērā ir parādīts, kā varat kontrolēt formātu, kas tiek izmantots, lai drukātu datumus.

```dos
$PrintedDate:dd-MM-yyyy$
```

Šajā piemērā datums 2020. gada 30. aprīlis tiks drukāts kā "30-04-2020".

Pilnīgu pieejamo datuma/laika formātu sarakstu skatiet [Pielāgotās datuma un laika formāta virknes](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="print-individual-lines-from-multiline-data"></a>Drukāt atsevišķas rindas no vairākrindu datiem

Ja datu lauks satur vairākas rindas (t.i., rindas, kas atdalītas ar rindu pārtraukumiem), varat izdrukāt atsevišķu rindu, lietojot šādu formātu.

```dos
$FieldName[#]$
```

Šeit `#` ir rindas numurs, ko vēlaties drukāt. (Pirmajai rindai izmantojiet 1.)

Piemēram, sistēmai ir `AdditionalAddress` lauks, kurā tiek uzglabāta šāda daudzrindu adrese:

Contoso Inc.  
Ielas nosaukums 123  
Kāda pilsēta, kāds štats

Šo adresi var drukāt pa vienai rindai, izmantojot tālāk norādītos kodus.

| Kods | Drukātais teksts |
|---|---|
| `$AdditionalAddress[1]$` | Contoso Inc. |
| `$AdditionalAddress[2]$` | Ielas nosaukums 123 |
| `$AdditionalAddress[3]$` | Kāda pilsēta, kāds štats |

## <a name="print-and-format-from-a-display-method"></a>Drukāt un formatēt no ekrāna metodes

Jūs varat drukāt no ekrāna metodes, izmantojot sekojošo formātu.

```dos
$DisplayMethod()$
```

Šo formātu var kombinēt ar citiem veidiem, kas tika aprakstīti iepriekš šajā rakstā. Piemēram, jums ir ekrāna metode, kas ir nosaukta `DisplayListOfItemsNumbers()`, un jūs vēlaties izdrukāt šīs metodes pirmo preces numuru. Šajā gadījumā, var izmantot sekojošo kodu.

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a>Papildinformācija par etiķešu drukāšanu

Papildinformāciju par etiķešu iestatīšanas un drukāšanas veidu skatiet šādos rakstos:

- [Numura zīmes iezīmes drukāšana](tasks/license-plate-label-printing.md)
- [Drukāt konteinera etiķetes](print-container-labels.md)
- [Kopuma etiķešu drukāšana](configure-wave-label-printing.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
