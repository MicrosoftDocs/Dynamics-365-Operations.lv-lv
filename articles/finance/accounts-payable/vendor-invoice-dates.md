---
title: Kreditora rēķinu datumi
description: Šajā rakstā ir aprakstīti kreditoru rēķinos redzamie datumi. Tajā ir arī paskaidrots, kā automātiski pielāgot publicēšanas datumu.
author: sunfzam
ms.date: 2/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 022fd0ce07fbb4c54afcf7334c1c9411e01dcf26
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775277"
---
# <a name="vendor-invoice-dates"></a>Kreditora rēķinu datumi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīti kreditoru rēķinos redzamie datumi. Tajā ir arī paskaidrots, kā automātiski pielāgot publicēšanas datumu.

Lapā Neapstiprinātā **kreditora rēķina detalizēta informācija** rēķina galvenē tiek rādīti četri datumi: **rēķina saņemšanas datums,** rēķina **datums,** grāmatošanas datums un **apmaksas datums** **·**. Pēc kreditora rēķina izveidošanas pēc noklusējuma tiek ievadīti šādi datumi:

- **Rēķina saņemšanas datums** – šis lauks ir iestatīts uz pašreizējo sistēmas datumu.
- **Grāmatošanas datums** – šis lauks ir iestatīts uz pašreizējo sistēmas datumu. 
- **Apmaksas datums** – datums šajā laukā tiek aprēķināts, pamatojoties uz grāmatošanas datumu un maksājuma nosacījumiem.
- **Rēķina datums** – pēc noklusējuma šis lauks ir tukšs. Tomēr, jūs varat ievadīt vērtību pēc nepieciešamības. Šajā gadījumā, datums laukā **Apmaksas datums** tiek pārrēķināts, pamatojoties uz rēķina datumu un maksājuma nosacījumiem.

Dažreiz kreditora rēķins var būt gaidīšanas stāvoklī ilgu laiku pēc perioda slēgšanas. Kad tas ir gatavs grāmatošanai, iepriekšējā grāmatošanas perioda vecais grāmatošanas datums joprojām tiek izmantots. Tomēr šis periods tagad ir slēgts. Tādēļ kreditora (AP) darbiniekam manuāli jāmaina visus grāmatošanas datumus uz jaunu grāmatošanas periodu visiem iepriekš izveidotajiem neapmaksātajiem rēķiniem.

Šajā rakstā aprakstītais līdzeklis ļauj automātiski pielāgot publicēšanas datumu atbilstoši uzņēmuma prasībām.

## <a name="parameter-for-automatically-adjusting-the-vendor-invoice-posting-date"></a>Parametrs kreditora rēķina grāmatošanas datuma automātiskai pielāgošanai

Veiciet šīs darbības, lai automātiski pielāgotu kreditoru rēķinu grāmatošanas datumu.

1.  Dodieties uz **Parāds kreditoriem \> Iestatīšana \> Kreditora moduļa parametri**.
2.  Laukā **Koriģēt grāmatošanas datumu automātiski** cilnē **Virsgrāmata un PVN** atlasiet vienu no šīm vērtībām:

    - **Bez izmaiņām** – grāmatošanas laikā sistēma automātiski nemaina grāmatošanas datumu. Šī vērtība ir atlasīta pēc noklusējuma.
    - **Vienmēr mainiet publicēšanas datumu uz sistēmas datumu — grāmatošanas datums publicēšanas laikā tiek automātiski mainīts uz sistēmas datumu**.
    - **Mainīt grāmatošanas datumu uz sistēmas datumu, kad grāmatošanas datuma periods ir slēgts vai aizturēts** — grāmatošanas datums publicēšanas laikā tiek automātiski mainīts uz sistēmas datumu, bet tikai tad, ja attiecīgajam grāmatošanas datuma periodam ir statuss **Slēgts** vai **Aizturēts**.
    - **Mainiet grāmatošanas datumu uz jaunā perioda pirmo dienu, ja grāmatošanas datuma periods ir slēgts vai aizturēts** — grāmatošanas datums tiek mainīts uz jaunā atvērtā perioda pirmo dienu, bet tikai tad, ja attiecīgajam grāmatošanas datuma periodam ir statuss **Slēgts** vai **Aizturēts**.

> [!NOTE]
> Ja jaunais grāmatošanas datums, kas tika automātiski pielāgots, ir jauns finanšu gads, rēķina grāmatošanas datums netiks atjaunināts. Lietotājs saņems kļūdu "Finanšu gads ir mainījies. Lūdzu, pārbaudiet un atkārtoti ievadiet publicēšanas datumu." Lai rēķinu grāmatošanas datums tiktu grāmatots, tas ir jāatjaunina uz jauno finanšu gada datumu.

## <a name="impact-of-posting-date-changes"></a>Grāmatošanas datuma izmaiņu ietekme

Ja neapmaksātā kreditora rēķinā grāmatošanas datums ir mainīts, izmaiņām ir šādi efekti:

- **Izpildes termiņš**

    - Ja lauks **Rēķina datums** ir tukšs, apmaksas datums tiek aprēķināts, pamatojoties uz jaunu grāmatošanas datumu un maksājuma nosacījumiem.
    - Ja lauks **Rēķina datums** tika iestatīts iepriekš, grāmatošanas datuma maiņa neietekmē apmaksas datumu.

- **Termiņatlaides datums**

    - Ja lauks **Rēķina datums** ir tukšs, lai aprēķinātu termiņatlaidi, izmanto jauno grāmatošanas datumu.
    - Ja lauks **Rēķina datums** tika iestatīts iepriekš, termiņatlaide netiek mainīta.

- **Maiņas kurss** - valūtas maiņas kursu nosaka opcijas **Kreditoru grāmatvedības atjaunināšana, izmantojot rēķina datuma** iestatījums lapas **Kreditoru parametri** cilnē **Rēķins** (**Parādi kreditoriem \> Iestatījums \> Kreditora moduļa parametri**).

    - Ja šī opcija ir iestatīta uz **Jā**, tiek izmantots rēķina datums **un** grāmatošanas datuma **izmaiņas** neietekmē valūtas kursu.
    - Ja šī opcija ir iestatīta uz **Nē**, grāmatošanas datums tiek izmantots, lai aprēķinātu maiņas kursu. Kad grāmatošanas datums ir atjaunināts, uzskaites un pārskata summas tiek pārrēķinātas. Tāpēc vēlreiz jāveic atbilstības pārbaude.

## <a name="validation"></a>Validācija

Divi citi lauki **Kreditoru parametru** lapas cilnē **Rēķins** (**Parādi kreditoriem \> Iestatīšana \> Kreditora moduļa parametri**) ietekmē rēķina apstrādi:

- Ja lauks Pārbaudīt izmantoto **rēķina numuru ir iestatīts** uz **Noraidīt dublikātus finanšu gada** laikā, grāmatošanas datums tiks izmantots, lai pārbaudītu rēķinu dublikātus rēķina grāmatošanas laikā.
- Ja opcija **Pieprasīt dokumenta datumu kreditora rēķinā** ir iestatīta uz **Kļūdas opciju**, ir nepieciešams lauks **Neapmaksātā rēķina virsraksta rēķina datums**. Ja rēķina datums ir vēlāks par grāmatošanas datumu, tiks parādīts kļūdas ziņojums.
