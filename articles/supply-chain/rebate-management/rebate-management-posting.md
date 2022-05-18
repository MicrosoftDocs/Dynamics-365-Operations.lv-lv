---
title: Atlaižu pārvaldības grāmatošanas iestatīšana
description: Šajā tēmā ir aprakstīts, kā iestatīt grāmatošanas profilus. Grāmatošanas profili tiek izmantoti, lai noteiktu atlaižu pārvaldības aprēķina rindu grāmatošanas ierakstus.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5ed28e99e36fafa4e1275421159420a3f3380c7c
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690251"
---
# <a name="rebate-management-posting-setup"></a>Atlaižu pārvaldības grāmatošanas iestatīšana

[!include [banner](../includes/banner.md)]

Grāmatošanas profili tiek izmantoti, lai noteiktu atlaižu pārvaldības aprēķina rindu grāmatošanas ierakstus. Ja darījuma virsrakstā ir atlasīta grāmatošanas metode, tā tiek piemērota visām darījuma rindām.

Šis līdzeklis darbojas starp uzņēmumiem (juridiskajām personām). Ir iespējams noteikt uzņēmumu, kam uzkrājumi tiks uzkrāti un ka prasības tiks apmaksātas. Varat arī iestatīt dažādus uzkrājumu debeta kontus un norakstīšanas kredīta kontus katram avota grāmatošanas uzņēmumam.

Lai debitoriem un kreditoriem iestatītu atlaižu pārvaldības grāmatošanas metodes, pārejiet uz sadaļu **Atlaižu pārvaldības \> Atlaižu pārvaldības grāmatošanas iestatījums \> Atlaižu pārvaldības grāmatošanas profili**. Lapa **Atlaižu pārvaldības grāmatošanas profili** ietver saraksta rūti, kurā ir redzami visi jūsu esošie profili. Rīkjoslas pogas var izmantot, lai pievienotu režģim profilus vai noņemtu tos.

Šīs tēmas pārējās sadaļās aprakstīts, kā izmantot pieejamos laukus, veidojot vai rediģējot profilu.

## <a name="posting-profile-header"></a>Profila galvenes grāmatošana

Tabulā ir aprakstīti iestatījumi, kas ir pieejami katras Atlaižu pārvaldības grāmatošanas profila galvenes sadaļā.

| Lauks | Apraksts |
|---|---|
| Grāmatošanas metode | Ievadiet unikālu profila nosaukumu. |
| Apraksts | Ievadiet profila aprakstu. |
| Modulis | Atlasiet moduli, ar kuru saistītas profila atlaides un patentmaksas (*Debitors* vai *Kreditors*). |
| tips | Atlasiet profila tipu (*Atlaide* vai *Patentmaksa*). |
| Maksājuma veids | <p>Šis lauks nosaka grāmatotās atlaides izvades formātu.<p><p>Kad **Veids** ir iestatīts uz *Atlaide*, ir pieejamas šādas vērtības:</p><ul><li>*Maksāt, izmantojot kreditorus* - iegrāmatojot debitora atlaidi, tiek izveidots kreditora rēķins pārskaitījuma kreditoram, kas iestatīts atlaides debitoram. Iegrāmatojot kreditora atlaidi, tiek izveidots kreditora rēķins atlaides kreditora kontam.</li><li>*Debitoru ieturējumi* - kad grāmatojat atlaidi, tiek izveidots debitora ieturējumu žurnāls šim atlaides debitoram.</li><li>*Nodokļu rēķina debitoru ieturējumi* - kad grāmatojat atlaidi, tiek izveidots atlaides debitora brīvā teksta rēķins.</li><li>*Kreditoru izdevumi* - kad grāmatojat atlaidi, tiek izveidots debitora ieturējumu žurnāls šim atlaides debitoram.</li><li>*Pārskata=i* - kad grāmatojat atlaidi, tiek izveidots debitora ieturējumu žurnāls šim atlaides debitoram.</li></ul><p>Kad **Veids** ir iestatīts uz *Patentmaka*, ir pieejamas šādas vērtības:</p><ul><li>*Maksāt, izmantojot kreditorus* - Kad grāmatojat atlaidi, tiek izveidots kreditora rēķins pārskaitījuma kreditoram, kas iestatīts atlaides kreditoram.</li><li>*Pārskati* - Kad grāmatojat atlaidi, tiek izveidots kreditora rēķins pārskaitījuma kreditoram, kas iestatīts atlaides kreditoram.</li></ul><p>Lai iegūtu vairāk informācijas, skatiet nākamajā sadaļā [Maksājumu veidi](#payment-types). |
| Uzņēmums | Atlasiet uzņēmumu (juridisku personu), kam uzkrājumi tiks uzkrāti un ka prasības tiks apmaksātas. |

### <a name="payment-types"></a>Maksājumu tipi

Tabulā ir apkopots, kā dažādie lauka **Maksājumu veidi** iestatījumi ietekmē maksājumu grāmatošanas vietu. Maksājumus var grāmatot debitora kontā, kreditora kontā vai pārskaitījuma kontā atkarībā no mērķa darbības un atlaides veida.

| Maksājuma veids | Mērķa darījuma veids | Atlaides veids | Maksājums līdz (rēķina konts) |
|---|---|---|---|
| Maksāt, izmantojot kreditoru parādu | Kreditoru rēķinu žurnāls | Debitora atlaide | Debitora pārskaitījuma kreditora konts |
| Maksāt, izmantojot kreditoru parādu | Kreditoru rēķinu žurnāls | Debitora patentmaksa | Kreditora konts |
| Maksāt, izmantojot kreditoru parādu | Kreditoru rēķinu žurnāls | Kreditora atlaide | Kreditora konts |
| Ieturējumi debitoriem | Ikdienas žurnāls | Debitora atlaide | Debitora konts |
| Debitoru nodokļu rēķina ieturējumi | Brīva teksta rēķins | Debitora atlaide | Debitora konts |
| Tirdzniecības izdevumi | Ikdienas žurnāls | Debitora atlaide | Debitora konts |
| Pārskatu veidošana | Ikdienas žurnāls | Debitora atlaide | Debitora konts |
| Pārskatu veidošana | Kreditoru rēķinu žurnāls | Debitora patentmaksa | Kreditora konts |
| Pārskatu veidošana | Kreditoru rēķinu žurnāls | Kreditora atlaide | Kreditora konts |

> [!NOTE]
> Ņemiet vērā šādus punktus, iestatot [Atlaižu pārvaldības darījumus](rebate-management-deals.md):
>
> - Darījumos, kur lauks **Saskaņot pēc** ir iestatīts uz *Darījums*, grāmatošanas laikā dinamisko darījuma kontu nevar izmantot. Ir jāizmanto norādītais debitora vai kreditora konts.
> - Darījumiem, kur lauks **Saskaņot pēc** ir iestatīts uz *Rinda*, jūs varat izmantot grāmatošanas metodi, kas nobīdi uz dinamiska darījuma kontu darījuma rindā, jo debitors vai kreditors ir iestatīts uz vienu darījuma rindu.

## <a name="posting-fasttab"></a>Grāmatošanas kopsavilkuma cilne

Tabulā ir aprakstīti lauki, kas ir pieejami katras Atlaižu pārvaldības profila kopsavilkuma cilnes **Grāmatošana** galvenes sadaļā.

| Lauks | Apraksts |
|---|---|
| Kredīta tips | Izvēlieties, vai kreditēt Virsgrāmatas kontu vai debitoru. Ja virsraksta lauks **Maksājuma tips** ir iestatīts kā *Debitora ieturējumi nodokļa rēķinā*, šis lauks ir iestatīts kā *Virsgrāmatas konts*. Kreditora atlaidēm šis lauks ir iestatīts uz *Virsgrāmatas kontu*. |
| Kredīta konts | Atlasiet kontu, kurā grāmato kredīta summas, veicot atlaižu uzkrājumus. Šis konts tiks izmantots arī kā korespondējošais konts, kad atlaide tiek grāmatota debitora kreditēšanai vai kreditora beditēšanai. |
| Žurnāla nosaukums<br>(Sadaļā **Nodrošināšana** ) | Atlasiet žurnāla nosaukumu, ko lietot grāmatoto uzkrājumu ierakstīšanai. |
| tips | Izvēlieties, vai grāmatot atlaidi Virsgrāmatas kontam, debitoram vai kreditoram. Ja virsraksta lauks **Maksājuma tips** ir iestatīts kā *Debitora ieturējumi nodokļa rēķinā*, šis lauks ir iestatīts kā *Debitors/Kreditors*. |
| Izmantot konta avotu | <p>Atlasiet vienu no šīm vērtībām:</p><ul><li>*Fiksētais konts* - ja atlasīsiet šo vērtību, jums jānorāda konts laukā **Atlaides konts**.</li><li>*Darījuma rindas konts* - izmantojiet atlaides rindā norādīto debitora vai kreditora kontu. Šo vērtību var atlasīt tikai darījumiem, kur lauks **Saskaņot pēc** ir iestatīts uz *Rinda* un darījuma rindas, kur **Konta koda** lauks ir iestatīts uz *Tabula*. Tas neattiecas uz debitora patentmaksas grāmatošanas profiliem vai kreditora atlaidēm, kuru pamatā ir pārdošanas pasūtījumi.</li></ul> |
| Atlaižu konts | Konts, kurā tiks grāmatoti faktiskie atlaižu izdevumi. |
| Žurnāla nosaukums<br>(Lauku grupā **Atlaižu pārvaldība** ) | Atlasiet žurnāla nosaukumu, ko izmantot, lai grāmatotu debitora atlaides summas kredīta vai debitora notu. Ja virsraksta lauks **Maksājuma tips** ir iestatīts kā *Debitora ieturējumi nodokļa rēķinā*. Debitoru atlaidēm ir pieejami žurnāla nosaukumi, kuru tips ir *Ikdienas* žurnāls. Debitoru un kreditoru atlaidēm ir pieejami žurnāla nosaukumi, kuru tips ir *Kreditoru rēķinu reģistrēšanas* žurnāls. |
| Krājumu PVN grupa | Norādiet, vai atlaide ir apliekama ar nodokli. |
| Žurnāla nosaukums<br>(Lauku grupā **Norakstīt** ) | Ja grāmatotā atlaide nav vienāda ar uzkrājumiem, starpību var norakstīt. Atlasiet žurnāla nosaukumu, ko lietot grāmatoto uzkrājumu norakstīšanai. |

## <a name="posting-by-company-fasttab"></a>Grāmatošana pēc uzņēmuma kopsavilkuma cilne

Katras atlaižu pārvaldības grāmatošanas metodes kopsavilkuma cilne **Grāmatošana pēc uzņēmuma** ļauj norādīt grāmatošanas kontu, ko režģī izmanto katrs uzņēmums (juridiskā persona).

Rīkjoslas pogas var izmantot, lai pievienotu režģim uzņēmumus vai noņemtu tos. Katru reizi, kad režģim pievienojat rindu, izmantojiet lauku **Uzņēmums**, lai norādītu juridisko personu tai rindai. Lauks **Nosaukums** tiek iestatīts automātiski.

Atlasiet rindu katram uzņēmumam un pēc tam ievadiet šādu informāciju, izmantojot laukus zem režģa:

- **Debeta veids** – Izvēlieties, vai debitēt Virsgrāmatas kontu vai kreditoru. Debitora atlaidēm un patentmaksām šis lauks ir iestatīts uz *Virsgrāmatas kontu*.
- **Debeta konts** - ievadiet kontu, kurā tiek grāmatota debeta summa, veicot atlaižu uzkrājumus.
- **Galvenais konts** – atlasiet norakstīšanas galveno kontu.
