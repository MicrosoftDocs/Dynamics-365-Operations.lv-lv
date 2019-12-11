---
title: Video atskaņotāja modulis
description: Šajā tēmā tiek stāstīts par video atskaņotāja moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 32504351f712c83ba8f593c17d2e51c532374311
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785333"
---
# <a name="video-player-module"></a>Video atskaņotāja modulis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā tiek stāstīts par video atskaņotāja moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Video atskaņotāja moduļi tiek izmantoti, lai atbalstītu video atskaņošanu. Veikala sākuma komplektā ir divi video atskaņotāja moduļi: ambienta video atskaņotāja modulis un video atskaņotāja modulis. Abi atskaņotāji atbalsta .mp4 datu nesēju tipu.

## <a name="ambient-video-player-module"></a>Ambienta video atskaņotāja modulis

Ambienta video atskaņotāja modulis atbalsta īsus informatīvus videoklipus. Tas ir jālieto videoklipiem, kas ir īsāki par piecām sekundēm. Šis atskaņotājs atbalsta ierobežotas video atskaņošanas iespējas, piemēram, atskaņot un ieslēgt pauzi.

### <a name="examples-of-ambient-video-player-modules-in-e-commerce"></a>Ambienta video atskaņotāja moduļu piemēri E-komercijā

- Īsi informatīvi videoklipi, kas izceļ jaunas preces sākumlapā
- Īsi informatīvi videoklipi, kas izceļ preču funkcijas preces informācijas lapā

### <a name="ambient-video-player-module-properties"></a>Ambienta video atskaņotāja rekvizīti

| Rekvizīta nosaukums     | Vērtība                 | Apraksts |
|-------------------|-----------------------|-------------|
| Automātiskā atskaņošana          | **Patiess** vai **Nepatiess** | Ja vērtība ir iestatīta uz **Patiess**, videoklips tiek automātiski atskaņots. |
| Izslēgt skaņu              | **Patiess** vai **Nepatiess** | Ja vērtība ir iestatīta uz **Patiess**, tiek izslēgta skaņa. Šajā atskaņotājā noklusējuma vērtība ir **Patiess**. Google Chrome pārlūkā automātiskās atskaņošanas videoklipiem pēc noklusējuma tiek izslēgta skaņa, kura tiek atskaņota tikai tad, ja lietotājs manuāli atskaņo videoklipu. |
| Cilpa              | **Patiess** vai **Nepatiess** | Ja vērtība ir iestatīta uz **Patiess**, videoklipa atskaņošana tiek atkārtota. |
| Plašsaziņas līdzekļi             |  Video faila ceļš un nosaukums | Video fails, ko atskaņo video atskaņotājs. |
| Atskaņošanas vadība | **Patiess** vai **Nepatiess** | Ja vērtība ir iestatīta kā **Patiess**, videoklipā ir redzama poga atskaņot/apturēt. Ja vērtība ir iestatīta uz **Nepatiess**, poga atskaņot/apturēt netiek rādīta, bet lietotāji joprojām var apturēt un atsākt video, izmantojot tastatūru. |

## <a name="video-player-module"></a>Video atskaņotāja modulis

Video atskaņotāja moduli var izmantot, lai parādītu videoklipus E-komercijas vietnē. Tas atbalsta visas atskaņošanas iespējas, piemēram, atskaņošanu, pauzi, pilna izmēra režīmu un slēptos titrus. Video atskaņotāja modulis atbalsta arī slēpto titru pielāgošanu, lai tie atbilstu Microsoft pieejamības standartiem. Piemēram, varat pielāgot fonta izmēru un fona krāsu.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>Video atskaņotāja moduļu piemēri E-komercijā

- Pasniegšanas video preču detalizētas informācijas lapās vai mārketinga lapās
- Reklāmas videoklipi vai videoklipi par politikām jebkurā mārketinga lapā
- Mārketinga videoklipi, kas izceļ preces funkcijas preces informācijas lapās vai mārketinga lapās

### <a name="video-player-module-properties"></a>Video atskaņotāja moduļa rekvizīti

| Rekvizīta nosaukums         | Vērtība                               | Apraksts |
|-----------------------|-------------------------------------|-------------|
| Automātiskā atskaņošana             | **Patiess** vai **Nepatiess**               | Ja vērtība ir iestatīta uz **Patiess**, videoklips tiek automātiski atskaņots. |
| Izslēgt skaņu                  | **Patiess** vai **Nepatiess**               | Ja vērtība ir iestatīta uz **Patiess**, tiek izslēgta skaņa. Šajā atskaņotājā noklusējuma vērtība ir **Nepatiess**. Google Chrome pārlūkā automātiskās atskaņošanas videoklipiem pēc noklusējuma tiek izslēgta skaņa, kura tiek atskaņota tikai tad, ja lietotājs manuāli atskaņo videoklipu. |
| Cilpa                  | **Patiess** vai **Nepatiess**               | Ja vērtība ir iestatīta uz **Patiess**, videoklipa atskaņošana tiek atkārtota. |
| Plašsaziņas līdzekļi                 | Video faila ceļš un nosaukums | Video fails, ko atskaņo video atskaņotājā. |
| Atskaņošanas vadība     | **Patiess** vai **Nepatiess**               | Ja vērtība ir iestatīta kā **Patiess**, videoklipā ir redzama poga atskaņot/apturēt. Ja vērtība ir iestatīta uz **Nepatiess**, poga atskaņot/apturēt netiek rādīta, bet lietotāji joprojām var apturēt un atsākt video, izmantojot tastatūru. |
| Atskaņot pilnekrāna režīmā       | **Patiess** vai **Nepatiess**               | Ja vērtība ir iestatīta uz **Patiess**, videoklips tiek automātiski atskaņots pilnekrāna režīmā. |
| Vadīklas              | **Patiess** vai **Nepatiess**               | Ja vērtība ir iestatīta uz **Patiess**, tiek rādītas visas vadīklas. Šīs vadīklas ietver atskaņošanas un pauzes pogas, progresa indikatoru un slēptos titrus. |
| Plakāta kadra slēpšana     | **Patiess** vai **Nepatiess**               | Videoklipam var būt plakāta kadrs. Ja šī rekvizīta vērtība ir iestatīta uz **Patiess**, plakāta kadrs ir paslēpts. |
| Maskas līmenis            | Skaitlis no **0** līdz **100** | Maska, kas tiek lietota videoklipa stilizēšanai. |
| Pilnekrāna ikonas stils | **Kvadrāts** vai **Bultiņa**             | Pilnekrāna ikonas stils, kas ir redzams video atskaņotājā. |

## <a name="add-a-video-player-module-to-a-page"></a>Video atskaņotāja moduļa pievienošana lapā

Lai pievienotu video atskaņotāja moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Izveidojiet lapas veidni ar nosaukumu **video atskaņotāja veidne**.
1. Noklusējuma lapas **Galvenajā** slotā pievienojiet konteinera moduli.
1. Konteinera modulī pievienojiet video atskaņotāju un ambienta video atskaņotāja moduļus.
1. Pārbaudiet veidni un publicējiet to.
1. Izmantojiet jūsu tikko izveidoto video atskaņotāja veidni, lai izveidotu lapu ar nosaukumu **video atskaņotāja lapa**.
1. Jaunās lapas **Galvenajā** slotā pievienojiet ambienta video atskaņotāja moduli.
1. Ambienta video atskaņotāja moduļa iestatījumos dodieties uz **Multivide**un augšupielādējiet video failu. Varat mainīt **Automātiskā atskaņošana**, **Cikls**un citus rekvizītus pēc nepieciešamības.
1. Saglabājiet un priekšskatiet lapu.
1. Jaunās lapas **Galvenajā** slotā pievienojiet ambienta video atskaņotāja moduli.
1. Video atskaņotāja moduļa iestatījumos dodieties uz **Multivide**un augšupielādējiet video failu.
1. Saglabājiet un priekšskatiet lapu. Lapā jābūt redzamiem abiem video moduļiem. Varat mainīt papildu iestatījumus, lai pielāgotu katra moduļa darbību.
1. Pārbaudiet lapu un publicējiet to.

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Brīdinājuma modulis](add-alert.md)

[Karuseļa modulis](add-carousel.md)

[Bagātinātā satura bloka modulis](add-content-rich-block.md)

[Satura izvietojuma modulis](add-content-placement-modules.md)

[Funkcijas modulis](add-feature-module.md)

[Centrālais modulis](add-hero-module.md)
