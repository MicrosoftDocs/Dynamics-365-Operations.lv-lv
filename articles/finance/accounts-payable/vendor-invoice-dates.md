---
title: Kreditora rēķinu datumi
description: Šajā tēmā aprakstīti datumi, kas parādās kreditoru rēķinos. Tajā skaidrots arī, kā iestatīt sistēmu, lai tā automātiski koriģētu grāmatošanas datumu.
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
ms.openlocfilehash: 064a125d448ebb3511db2d9b1f4228380805dc44
ms.sourcegitcommit: f2a78e0d7d461ca843ac2f9abff7690275db9196
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/09/2022
ms.locfileid: "8105468"
---
# <a name="vendor-invoice-dates"></a>Kreditora rēķinu datumi

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstīti datumi, kas parādās kreditoru rēķinos. Tajā skaidrots arī, kā iestatīt sistēmu, lai tā automātiski koriģētu grāmatošanas datumu.

Lapā **Detalizētā informācija par nenokārtoto kreditora rēķinu** rēķina virsraksts rāda četrus datumus: rēķina saņemšanas datumu, rēķina datumu, grāmatošanas datumu un apmaksas datumu. Pēc kreditora rēķina izveidošanas pēc noklusējuma tiek ievadīti šādi datumi:

- **Rēķina saņemšanas datums** – šis lauks ir iestatīts uz pašreizējo sistēmas datumu.
- **Grāmatošanas datums** – šis lauks ir iestatīts uz pašreizējo sistēmas datumu. 
- **Apmaksas datums** – datums šajā laukā tiek aprēķināts, pamatojoties uz grāmatošanas datumu un maksājuma nosacījumiem.
- **Rēķina datums** – pēc noklusējuma šis lauks ir tukšs. Tomēr, jūs varat ievadīt vērtību pēc nepieciešamības. Šajā gadījumā, datums laukā **Apmaksas datums** tiek pārrēķināts, pamatojoties uz rēķina datumu un maksājuma nosacījumiem.

Dažreiz kreditora rēķins var būt gaidīšanas stāvoklī ilgu laiku pēc perioda slēgšanas. Kad tas ir gatavs grāmatošanai, iepriekšējā grāmatošanas perioda vecais grāmatošanas datums joprojām tiek izmantots. Tomēr šis periods tagad ir slēgts. Tādēļ kreditora (AP) darbiniekam manuāli jāmaina visus grāmatošanas datumus uz jaunu grāmatošanas periodu visiem iepriekš izveidotajiem neapmaksātajiem rēķiniem.

Šajā tēmā aprakstītais līdzeklis ļauj iestatīt sistēmu tā, lai tā automātiski koriģētu grāmatošanas datumu atbilstoši biznesa prasībām.

## <a name="parameter-for-automatically-adjusting-the-vendor-invoice-posting-date"></a>Parametrs kreditora rēķina grāmatošanas datuma automātiskai pielāgošanai

Izpildiet šīs darbības, lai ļautu sistēmai automātiski koriģēt grāmatošanas datumu kreditora rēķiniem.

1.  Dodieties uz **Parāds kreditoriem \> Iestatīšana \> Kreditora moduļa parametri**.
2.  Laukā **Koriģēt grāmatošanas datumu automātiski** cilnē **Virsgrāmata un PVN** atlasiet vienu no šīm vērtībām:

    - **Bez izmaiņām** – grāmatošanas laikā sistēma automātiski nemaina grāmatošanas datumu. Šī vērtība ir atlasīta pēc noklusējuma.
    - **Vienmēr mainīt grāmatošanas datumu uz sistēmas datumu** – sistēma grāmatošanas laikā automātiski maina grāmatošanas datumu uz sistēmas datumu.
    - **Mainīt grāmatošanas datumu uz sistēmas datumu, kad grāmatošanas datuma periods ir slēgts vai aizturēts** – sistēma grāmatošanas laikā maina grāmatošanas datumu uz sistēmas datumu, bet tikai tad, ja atbilstošajam grāmatošanas datuma periodam ir statuss **Slēgts** vai **Aizturēts**.
    - **Mainīt grāmatošanas datumu uz pirmo jaunā perioda dienu, kad grāmatošanas datuma periods ir slēgts vai aizturēts** – sistēma grāmatošanas laikā maina grāmatošanas datumu uz pirmo jaunā atvērtā perioda datumu, bet tikai tad, ja atbilstošajam grāmatošanas datuma periodam ir statuss **Slēgts** vai **Aizturēts**.

> [!NOTE]
> Ja jaunais automātiski koriģētais grāmatošanas datums ir jaunajā finanšu gadā, rēķina grāmatošanas datums netiks atjaunināts. Lietotājs saņems kļūdu "Finanšu gads ir mainījies. Lūdzu, pārbaudiet un atkārtoti ievadiet grāmatošanas datumu." Lai varētu veikt grāmatošanu, rēķina grāmatošanas datums ir jāatjaunina uz jauno finanšu gada datumu.

## <a name="impact-of-posting-date-changes"></a>Grāmatošanas datuma izmaiņu ietekme

Ja neapmaksātā kreditora rēķinā grāmatošanas datums ir mainīts, izmaiņām ir šādi efekti:

- **Izpildes termiņš**

    - Ja lauks **Rēķina datums** ir tukšs, apmaksas datums tiek aprēķināts, pamatojoties uz jaunu grāmatošanas datumu un maksājuma nosacījumiem.
    - Ja lauks **Rēķina datums** tika iestatīts iepriekš, grāmatošanas datuma maiņa neietekmē apmaksas datumu.

- **Termiņatlaides datums**

    - Ja lauks **Rēķina datums** ir tukšs, lai aprēķinātu termiņatlaidi, izmanto jauno grāmatošanas datumu.
    - Ja lauks **Rēķina datums** tika iestatīts iepriekš, termiņatlaide netiek mainīta.

- **Maiņas kurss** - valūtas maiņas kursu nosaka opcijas **Kreditoru grāmatvedības atjaunināšana, izmantojot rēķina datuma** iestatījums lapas **Kreditoru parametri** cilnē **Rēķins** (**Parādi kreditoriem \> Iestatījums \> Kreditora moduļa parametri**).

    - Ja šī opcija ir iestatīta uz **Jā** , tiek izmantots rēķina datums un grāmatošanas datuma maiņa neietekmē maiņas kursu.
    - Ja šī opcija ir iestatīta uz **Nē**, grāmatošanas datums tiek izmantots, lai aprēķinātu maiņas kursu. Kad grāmatošanas datums ir atjaunināts, uzskaites un pārskata summas tiek pārrēķinātas. Tāpēc vēlreiz jāveic atbilstības pārbaude.

## <a name="validation"></a>Validācija

Divi citi lauki **Kreditoru parametru** lapas cilnē **Rēķins** (**Parādi kreditoriem \> Iestatīšana \> Kreditora moduļa parametri**) ietekmē rēķina apstrādi:

- Ja lauks **Pārbaudīt izmantoto rēķina numuru** ir iestatīts uz **Noraidīt dublikātus finanšu gada laikā**, sistēma izmanto grāmatošanas datumu, lai rēķina grāmatošanas laikā pārbaudītu rēķinu dublikātus.
- Ja opcija **Pieprasīt dokumenta datumu kreditora rēķinā** ir iestatīta uz **Kļūdas opciju**, ir nepieciešams lauks **Neapmaksātā rēķina virsraksta rēķina datums**. Ja rēķina datums ir vēlāks par grāmatošanas datumu, sistēma rāda kļūdas ziņojumu.
