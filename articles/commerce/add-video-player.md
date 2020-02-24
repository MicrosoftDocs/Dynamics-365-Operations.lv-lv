---
title: Video atskaņotāja modulis
description: Šajā tēmā tiek stāstīts par video atskaņotāja moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025660"
---
# <a name="video-player-module"></a>Video atskaņotāja modulis


[!include [banner](includes/banner.md)]

Šajā tēmā tiek stāstīts par video atskaņotāja moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Video atskaņotāja modulis tiek izmantots, lai atbalstītu video atskaņošanu. To var pievienot jebkurai lapai, ar nosacījumu, ka video saturs tiek augšupielādēts un pieejams satura pārvaldības sistēmā (CMS). Video atskaņotāja modulis atbalsta .mp4 multivides veidu.

## <a name="video-player-module"></a>Video atskaņotāja modulis

Video atskaņotāja moduli var izmantot, lai parādītu videoklipus E-komercijas vietnē. Tas atbalsta visas atskaņošanas iespējas, piemēram, atskaņošanu, pauzi, pilna izmēra režīmu, audio aprakstus un slēptos titrus. Video atskaņotāja modulis atbalsta arī slēpto titru pielāgošanu, lai tie atbilstu Microsoft pieejamības standartiem. Piemēram, varat pielāgot fonta izmēru un fona krāsu.

Video atskaņotāja modulis atbalsta arī sekundāros audio celiņus. Augšupielādējot videoklipu satura pārvaldības sistēmā, var augšupielādēt arī sekundāro audio celiņu. Pēc tam video atskaņotāja modulis var atskaņot sekundāro audio celiņu, ja lietotājs to atlasījis.

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
| Atskaņot pilnekrāna režīmā       | **Patiess** vai **Nepatiess**               | Ja vērtība ir iestatīta uz **Patiess**, videoklips tiek automātiski atskaņots pilnekrāna režīmā. |
| Atskaņošanas vai pauzes trigeris    | **Patiess** vai **Nepatiess**               | Ja vērtība ir iestatīta kā **Patiess**, videoklipā ir redzama poga atskaņot/apturēt. |
| Video atskaņotāja vadīklas | **Patiess** vai **Nepatiess**               | Ja vērtība ir iestatīta uz **Patiess**, tiek rādītas visas video atskaņotāja vadīklas. Šīs vadīklas ietver atskaņošanas un pauzes pogas, progresa indikatoru un slēpts titru opcijas. |
| Paslēpt grāmatotāja attēlu     | **Patiess** vai **Nepatiess**               | Videoklipam var būt plakāta kadrs. Ja šī rekvizīta vērtība ir iestatīta uz **Patiess**, plakāta kadrs ir paslēpts. |
| Maskas līmenis            | Skaitlis no **0** līdz **100** | Maska, kas tiek lietota videoklipa stilizēšanai. |

## <a name="add-a-video-player-module-to-a-page"></a>Video atskaņotāja moduļa pievienošana lapā

> [!NOTE] 
> Pirms video atskaņotāja moduļa izveides vispirms ir jāaugšupielādē video multivides bibliotēkā.

Lai pievienotu video atskaņotāja moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Izveidojiet lapas veidni ar nosaukumu **video atskaņotāja veidne**.
1. Noklusējuma lapas **Galvenajā** slotā pievienojiet konteinera moduli.
1. Konteinera modulī pievienojiet video atskaņotāju un ambienta video atskaņotāja moduļus.
1. Pabeidziet rediģēt veidni un publicējiet to.
1. Izmantojiet jūsu izveidoto video atskaņotāja veidni, lai izveidotu lapu ar nosaukumu **video atskaņotāja lapa**.
1. Jaunās lapas **Galvenajā** slotā pievienojiet ambienta video atskaņotāja moduli.
1. Video atskaņotāja moduļa rekvizītu rūtī atlasiet **Pievienot videoklipu**.
1. Dialoglodziņā **Multivides atlasītājs** atlasiet videoklipu un pēc tam atlasiet **Augšupielādēt jaunu multivides vienumu**.
1. Saglabājiet un priekšskatiet lapu. Lapā jābūt redzamam video modulim. Varat mainīt papildu iestatījumus, lai pielāgotu moduļa darbību.
1. Pabeidziet rediģēt lapu un publicējiet to.

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Veicināšanas reklāmkarogu modulis](add-alert.md)

[Karuseļa modulis](add-carousel.md)

[Teksta bloka modulis](add-content-rich-block.md)

[Satura bloka modulis](add-hero-module.md)
