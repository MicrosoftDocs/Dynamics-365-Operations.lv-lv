---
title: Video atskaņotāja modulis
description: Šajā rakstā ir apskatīti video player moduļi un aprakstīts, kā pievienot tos vietnes lapām Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 919446981f7439d61b01deb57b206cd457eed919
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269299"
---
# <a name="video-player-module"></a>Video atskaņotāja modulis

[!include [banner](includes/banner.md)]

Šajā rakstā ir apskatīti video player moduļi un aprakstīts, kā pievienot tos vietnes lapām Microsoft Dynamics 365 Commerce.

Video atskaņotāja modulis tiek izmantots, lai atbalstītu video atskaņošanu. To var pievienot jebkurai lapai, ar nosacījumu, ka video saturs tiek augšupielādēts un pieejams satura pārvaldības sistēmā (CMS). Video atskaņotāja modulis atbalsta .mp4 multivides veidu.

## <a name="video-player-module"></a>Video atskaņotāja modulis

Video atskaņotāja moduli var izmantot, lai parādītu videoklipus E-komercijas vietnē. Tas atbalsta visas atskaņošanas iespējas, piemēram, atskaņošanu, pauzi, pilna izmēra režīmu, audio aprakstus un slēptos titrus. Video atskaņotāja modulis atbalsta arī slēpto titru pielāgošanu, lai tie atbilstu Microsoft pieejamības standartiem. Piemēram, varat pielāgot fonta izmēru un fona krāsu.

Video atskaņotāja modulis atbalsta arī sekundāros audio celiņus. Augšupielādējot videoklipu satura pārvaldības sistēmā, var augšupielādēt arī sekundāro audio celiņu. Pēc tam video atskaņotāja modulis var atskaņot sekundāro audio celiņu, ja lietotājs to atlasījis.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>Video atskaņotāja moduļu piemēri E-komercijā

- Pasniegšanas video preču detalizētas informācijas lapās vai mārketinga lapās
- Reklāmas videoklipi vai videoklipi par politikām jebkurā mārketinga lapā
- Mārketinga videoklipi, kas izceļ preces funkcijas preces informācijas lapās vai mārketinga lapās

Attēlā zemāk redzams video atskaņotāja moduļa piemērs sākumlapā.

![Video atskaņotāja moduļa piemērs.](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a>Video atskaņotāja moduļa rekvizīti

| Rekvizīta nosaukums         | Vērtība                               | Apraksts |
|-----------------------|-------------------------------------|-------------|
| Virsraksts               | Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**) | Pēc noklusējuma virsrakstam tiek izmantots virsraksta tags **H2**, bet tagu var mainīt atbilstoši pieejamības prasībām. |
| Bagātināts teksts             | Rindkopas teksts | Modulis atbalsta rindkopu tekstu bagātinātā teksta formātā. Tiek atbalstītas dažas pamata bagātinātā teksta iespējas, piemēram, hipersaites, treknraksts, pasvītrots un slīpraksta teksts. Modulim piemērots lapas dizains var ignorēt dažas no šīm iespējām. |
| Saistīt                  | Saites teksts, saites vietrādis URL, pieejamās bagātinātās interneta lietojumprogrammas (ARIA) etiķete un **Atvērt saiti jaunā cilnē** atlasītājs | Modulis atbalsta vienu vai vairākas saites “aicinājums uz darbību”. Ja ir pievienota saite, ir nepieciešams saites teksts, vietrādis URL un ARIA etiķete. ARIA etiķetēm jābūt aprakstošām, lai tās atbilstu pieejamības prasībām. Saites var konfigurēt tā, lai tās tiktu atvērtas jaunā cilnē. |
| Apakštekts              | Virsraksts, teksts vai saites | Var pievienot papildu kontekstu video atskaņotāja modulim, piemēram, autora vai veidotāja vārdu, vai saites uz personīgajām papildmaksām. |
| Automātiskā atskaņošana             | **Patiess** vai **Nepatiess**               | Ja vērtība ir iestatīta uz **Patiess**, videoklips tiek automātiski atskaņots. |
| Izslēgt skaņu                  | **Patiess** vai **Nepatiess**               | Ja vērtība ir iestatīta uz **Patiess**, tiek izslēgta skaņa. Šajā atskaņotājā noklusējuma vērtība ir **Nepatiess**. Google Chrome pārlūkā automātiskās atskaņošanas videoklipiem pēc noklusējuma tiek izslēgta skaņa, kura tiek atskaņota tikai tad, ja lietotājs manuāli atskaņo videoklipu. |
| Cilpa                  | **Patiess** vai **Nepatiess**               | Ja vērtība ir iestatīta uz **Patiess**, videoklipa atskaņošana tiek atkārtota. |
| Plašsaziņas līdzekļi                 | Video faila ceļš un nosaukums | Video fails, ko atskaņo video atskaņotājā. |
| Atskaņot pilnekrāna režīmā       | **Patiess** vai **Nepatiess**               | Ja vērtība ir iestatīta uz **Patiess**, videoklips tiek automātiski atskaņots pilnekrāna režīmā. |
| Atskaņošanas vai pauzes trigeris    | **Patiess** vai **Nepatiess**               | Ja vērtība ir iestatīta kā **Patiess**, videoklipā ir redzama poga atskaņot/apturēt. |
| Video atskaņotāja vadīklas | **Patiess** vai **Nepatiess**               | Ja vērtība ir iestatīta uz **Patiess**, tiek rādītas visas video atskaņotāja vadīklas. Šīs vadīklas ietver atskaņošanas un pauzes pogas, progresa indikatoru un slēpts titru opcijas. |
| Paslēpt grāmatotāja attēlu     | **Patiess** vai **Nepatiess**               | Videoklipam var būt plakāta kadrs. Ja šī rekvizīta vērtība ir iestatīta uz **Patiess**, plakāta kadrs ir paslēpts. |
| Maskas līmenis            | Skaitlis no **0** līdz **100** | Maska, kas tiek lietota videoklipa stilizēšanai. |

> [!IMPORTANT]
> Rekvizīti **Virsraksts**, **Bagātinātais teksts**, **Saite** un **Apakšteksts** ir pieejami Dynamics 365 Commerce versijas 10.0.20 izlaidumā.

## <a name="add-a-video-player-module-to-a-page"></a>Video atskaņotāja moduļa pievienošana lapā

> [!NOTE] 
> Pirms video atskaņotāja moduļa izveides vispirms ir jāaugšupielādē video multivides bibliotēkā.

Lai pievienotu video atskaņotāja moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.
1. Dialoglodziņā Jauna **veidne ar** veidnes nosaukumu **ievadiet** **Video player veidni un** pēc tam atlasiet **Labi**.
1. Pamatteksta **slotā** atlasiet daudzpunkti (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet noklusējuma lapas **moduli** un pēc tam atlasiet **Labi**.
1. Noklusējuma lapas **moduļa** galvenajā **slotā** atlasiet daudzpunkti (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Moduļu **atlase** atlasiet moduli Konteiners **un** pēc tam atlasiet **Labi**.
1. Konteinera slotā **atlasiet** daudzpunkti (**...) un** pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet moduli **Video player un** pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to. 
1. Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.
1. Dialoglodziņa Izveidot **jaunu lapu sadaļā** Lapas nosaukums **ievadiet** **Video player** lapu un pēc tam atlasiet **Tālāk.**
1. Sadaļā **Izvēlēties veidni atlasiet** izveidoto **Video player veidni** un pēc tam atlasiet **Tālāk**.
1. Sadaļā **Izvēlēties izkārtojumu atlasiet** lapas izkārtojumu (piemēram, Elastīgs **izkārtojums**) un pēc tam atlasiet **Tālāk**.
1. Sadaļā **Pārskatīt un pabeigt** pārskatiet lapas konfigurāciju. Ja jums ir jārediģē lapas informācija, atlasiet **Atpakaļ**. Ja lapas informācija ir pareiza, atlasiet Izveidot **lapu**.
1. Jaunās lapas **galvenajā** slotā atlasiet daudzpunkti (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Moduļu **atlase** atlasiet moduli Konteiners **un** pēc tam atlasiet **Labi**.
1. Konteinera slotā **atlasiet** daudzpunkti (**...) un** pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet moduli **Video player un** pēc tam atlasiet **Labi**.
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
