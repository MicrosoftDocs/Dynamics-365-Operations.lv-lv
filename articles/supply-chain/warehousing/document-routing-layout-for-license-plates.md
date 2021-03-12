---
title: Dokumenta maršrutēšanas izkārtojums numura zīmes etiķetēm
description: Šajā tēmā ir aprakstīts, kā lietot formatēšanas metodes etiķešu vērtību drukāšanai.
author: perlynne
manager: tfehr
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 66ba73ab5c790aa4a67419842f63f6f741bf0d3a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973764"
---
# <a name="document-routing-layout-for-license-plate-labels"></a>Dokumenta maršrutēšanas izkārtojums numura zīmes etiķetēm

[!include [banner](../includes/banner.md)]

Dokumenta maršrutēšanas izkārtojums nosaka numura zīmes etiķešu izskatu un uz tām izdrukātos datus. Konfigurējiet drukāšanas trigera punktus, iestatot mobilās ierīces izvēlnes elementus un darba veidnes.

Tipiskā scenārijā noliktavas saņemšanas darbinieki drukā numura zīmju etiķetes uzreiz pēc tam, kad tie reģistrē paletes saturu, kas tiek saņemti saņemšanas zonā. Fiziskās etiķetes tiek lietotas paletēm. Tos var izmantot validācijai kā daļu no izvietošanas procesa, kas seko turpmākajām nosūtīšanas izdošanas operācijām.

Jūs varat drukāt augstas sarežģītības etiķetes, ar nosacījumu, ka drukas ierīce spēj interpretēt tai sūtīto tekstu. Piemēram, Zebra programmēšanas valodas (ZPL) izkārtojums, kas ietver svītrkodu, var izskatīties līdzīgi šim piemēram.

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

Kā daļa no etiķešu drukāšanas procesa teksts `$LicensePlateId$` šajā piemērā tiks aizstāts ar datu vērtību.

Lai apskatītu vērtības, kas tiks drukātas, dodieties uz **Noliktavas pārvaldība \> Vaicājumi un pārskati \> Numura zīmes etiķetes**.

Vairāki plaši pieejami etiķešu ģenerēšanas rīki var jums palīdzēt formatēt etiķetes izkārtojuma tekstu. Daudzi no šiem rīkiem atbalsta `$FieldName$` formātu. Turklāt Microsoft Dynamics 365 Supply Chain Management izmanto īpašu formatēšanas loģiku kā daļu no lauka kartējuma dokumenta maršrutēšanas izkārtojumam.

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

Pilnīgu pieejamo skaitļu formāta virkņu sarakstu skatiet [Pielāgotās skaitļu formāta virknes](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).

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

Pilnīgu pieejamo datuma/laika formātu sarakstu skatiet [Pielāgotās datuma un laika formāta virknes](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).

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

Jūs varat kombinēt šo formātu ar citiem tipiem, kas tika aprakstīti iepriekš šajā tēmā. Piemēram, jums ir ekrāna metode, kas ir nosaukta `DisplayListOfItemsNumbers()`, un jūs vēlaties izdrukāt šīs metodes pirmo preces numuru. Šajā gadījumā, var izmantot sekojošo kodu.

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a>Papildinformācija par etiķešu drukāšanu

Papildinformāciju par to, kā iestatīt un drukāt etiķetes, skatiet [Iespējot numura zīmes etiķetes drukāšanu](tasks/license-plate-label-printing.md).
