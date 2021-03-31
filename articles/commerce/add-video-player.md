---
title: Video atskaņotāja modulis
description: Šajā tēmā aplūkoti video atskaņotāja moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 13072c8d6839fef1ab0dd55d626c23a2a1084d4d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209183"
---
# <a name="video-player-module"></a>Video atskaņotāja modulis

[!include [banner](includes/banner.md)]

Šajā tēmā aplūkoti video atskaņotāja moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.

Video atskaņotāja modulis tiek izmantots, lai atbalstītu video atskaņošanu. To var pievienot jebkurai lapai, ar nosacījumu, ka video saturs tiek augšupielādēts un pieejams satura pārvaldības sistēmā (CMS). Video atskaņotāja modulis atbalsta .mp4 multivides veidu.

## <a name="video-player-module"></a>Video atskaņotāja modulis

Video atskaņotāja moduli var izmantot, lai parādītu videoklipus E-komercijas vietnē. Tas atbalsta visas atskaņošanas iespējas, piemēram, atskaņošanu, pauzi, pilna izmēra režīmu, audio aprakstus un slēptos titrus. Video atskaņotāja modulis atbalsta arī slēpto titru pielāgošanu, lai tie atbilstu Microsoft pieejamības standartiem. Piemēram, varat pielāgot fonta izmēru un fona krāsu.

Video atskaņotāja modulis atbalsta arī sekundāros audio celiņus. Augšupielādējot videoklipu satura pārvaldības sistēmā, var augšupielādēt arī sekundāro audio celiņu. Pēc tam video atskaņotāja modulis var atskaņot sekundāro audio celiņu, ja lietotājs to atlasījis.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>Video atskaņotāja moduļu piemēri E-komercijā

- Pasniegšanas video preču detalizētas informācijas lapās vai mārketinga lapās
- Reklāmas videoklipi vai videoklipi par politikām jebkurā mārketinga lapā
- Mārketinga videoklipi, kas izceļ preces funkcijas preces informācijas lapās vai mārketinga lapās

Attēlā zemāk redzams video atskaņotāja moduļa piemērs sākumlapā.

![Video atskaņotāja moduļa piemērs](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a>Video atskaņotāja moduļa rekvizīti

| Rekvizīta nosaukums         | Vērtība                               | apraksts |
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

1. Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.
1. Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukums** ievadiet **Video atskaņotāja veidne** un pēc tam atlasiet **Labi**.
1. Slotā **Pamatteksts** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Noklusējuma lapa** un pēc tam atlasiet **Labi**.
1. Moduļa **Noklusējuma lapa** slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.
1. Slotā **Konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Video atskaņotājs** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to. 
1. Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.
1. Dialoglodziņā **Izvēlēties veidni** atlasiet video atskaņotāja veidni, kuru izveidojāt. Sadaļā **Lapas nosaukums** ievadiet **Video atskaņotāja lapa** pēc tam atlasiet **Labi**.
1. Jaunās lapas slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.
1. Slotā **Konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Video atskaņotājs** un pēc tam atlasiet **Labi**.
1. Video atskaņotāja moduļa rekvizītu rūtī atlasiet **Pievienot videoklipu**.
1. Dialoglodziņā **Multivides atlasītājs** atlasiet videoklipu un pēc tam atlasiet **Augšupielādēt jaunu multivides vienumu**.
1. Failu pārlūkā atlasiet video failus un pēc tam atlasiet **Atvērt**.
1. Dialoglodziņā **Augšupielādēt multivides vienumu** ievadiet nosaukumu un citu informāciju pēc vajadzības un pēc tam atlasiet **Labi**.
1. Dialoglodziņā **Mediju atlasītājs** atlasiet **Aizvērt**.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu. Lapā jābūt redzamam video modulim. Varat mainīt papildu iestatījumus, lai pielāgotu moduļa darbību.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to. 

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Akcijas reklāmkaroga modulis](add-alert.md)

[Karuseļa modulis](add-carousel.md)

[Teksta bloka modulis](add-content-rich-block.md)

[Satura bloka modulis](add-hero-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]