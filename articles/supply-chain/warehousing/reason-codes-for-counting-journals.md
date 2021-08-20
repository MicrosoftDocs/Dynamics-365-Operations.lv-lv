---
title: Iemeslu kodi krājumu inventarizācijai
description: Šajā tēmā ir aprakstīts, kā iestatīt un lietot iemeslu kodus inventarizācijas uzdevumiem.
author: perlynne
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy, InventCountingReasonCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 4510ed7033e7c4e5187905906dcbef63f05a130bafcb7d9f19bbb360a7298119
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012095"
---
# <a name="reason-codes-for-inventory-counting"></a>Iemeslu kodi krājumu inventarizācijai

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Iemeslu kodi jums ļauj analizēt inventarizācijas procesa rezultātus un visas šajā procesā radušās neatbildības. Varat norādīt iemeslu inventarizācijas veikšanai, piemēram, bojāta palete vai krājumu korekcija, kas ir balstīta uz krājumu paraugiem. Tajā pašā laikā varat izmantot korekcijas funkcionalitāti, lai grāmatotu rīcībā esošo krājumu pielāgojumu vērtību atbilstošajā korespondējošā kontā, pamatojoties uz katras krājuma korekcijas iemeslu.

## <a name="recommendation"></a>Rekomendācija

Pirms šīs sistēmas iestatīšanas iesakām definēt stratēģiju darbam ar iemeslu kodiem. Piemēram, mēģiniet atbildēt uz tālāk norādītajiem jautājumiem.

- Vai iemeslu kodiem noliktavās ir jābūt obligātiem?
- Vai noteiktu vienumu iemeslu kodiem ir jābūt obligātiem vai neobligātiem?
- Cik iemeslu kodu jums ir nepieciešams?
- Vai jums ir iepriekš jāatlasa ierobežots korekciju iemeslu kodu saraksts?
- Kādā veidā iemeslu kodi ir jāizmanto svītrkoda skeneru lietotājiem? Vai iemeslu kodiem ir jābūt sākotnēji atlasītiem, obligātiem vai nerediģējamiem?
- Vai noliktavas darbiniekiem mobilajos skeneros ir nepieciešama citāda iemeslu kodu uzvedība? Ja atbilde ir Jā, varat izveidot vairākus izvēlnes vienumus un tos piešķirt dažādām personām.
- Vai iemeslu kodi vada finanšu korespondējošā konta grāmatošanu?

## <a name="turn-on-reason-code-features-in-your-system"></a>Ieslēdziet iemesla koda līdzekļus savā sistēmā

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Ja savā sistēmā neredzat visus līdzekļus, kas ir aprakstīti šajā tēmā, iespējams, būs jāieslēdz līdzekli *Rīcībā esošo korekciju grāmatošana, izmantojot konfigurējamus pamatojuma kodus, kas saistīti ar korespondējošo kontu*. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Rīcībā esošo korekciju grāmatošana, izmantojot konfigurējamus pamatojuma kodus, kas saistīti ar korespondējošo kontu*

## <a name="set-up-reason-codes"></a>Iestatīt cēloņa kodus

### <a name="set-up-reason-code-policies"></a>Iemeslu kodu politiku iestatīšana

Varat izveidot vairākus pamatojuma kodu politikas, lai kontrolētu, kad un kā tiek pielietoti inventarizācijas pamatojuma kodi. Katram iemesla koda ierobežojumam var būt viens no diviem inventarizācijas iemeslu kodu tipiem (*Neobligāts* vai *Obligāts*). Inventarizācijas iemeslu kodu politikas var lietot noliktavas līmenī vai krājumu līmenī.

Lai izveidotu pamatojuma koda politiku, veiciet šādas darbības.

1. Pārejiet uz sadaļu **Krājumu pārvaldība** \> **Iestatījums** \> **Krājumi** \> **Inventarizācijas iemesla koda politika**.
1. Lai režģim pievienotu politiku, darbību rūtī atlasiet **Jauns**.
1. Iestatiet lauku **Nosaukums** jaunajai politikai.
1. Laukā **Inventarizācijas iemesla koda tips** atlasiet vienumu *Obligāts* vai *Neobligāts*, lai norādītu, vai iemeslu koda atlasīšanai ir jābūt neobligātai vai obligātai vienā no tālāk norādītajiem krājumu pielāgošanas procesiem:

    - Cikla inventarizācija (mobilā ierīce)
    - Skaits uz vietas (mobilā ierīce)
    - Sliekšņa skaits (mobilā ierīce)
    - Ienākošās korekcijas (mobilā ierīce)
    - Izejošās korekcijas (mobilā ierīce)
    - Inventarizācijas žurnāls (bagātināts klients)
    - Daudzuma korekcija/tiešsaistes inventarizācija (bagāts klients)

Iemeslu kodu politikas varat iestatīt gan atsevišķām noliktavām, gan precēm. Preces iemesla koda iestatījumi var noraidīt preces noliktavas iestatījumus.

> [!NOTE]
> Ja noliktavām vai krājumiem lauks **Inventarizācijas iemeslu koda politika** ir iestatīts kā *Obligāts*, uzskaites inventarizācijas nevar pabeigt un noslēgt, kamēr nav norādīts iemesla kods. Papildinformāciju skatiet sadaļā tālāk.

### <a name="assign-counting-reason-code-policies-to-warehouses"></a>Piešķiriet noliktavām inventarizācijas iemeslu koda politikas

Lai noliktavai piešķirtu inventarizācijas iemesla koda politiku, veiciet šādas darbības.

1. Doties uz **Krājumu vadība** \> **Iestatījumi** \> **Noliktavu sadalījums** \> **Noliktavas**.
1. SarakSaraksta rūtī atlasiet noliktavu.
1. Darbību rūtī cilnes **Noliktava** grupā **Iestātīšana** atlasiet **Inventarizācijas iemeslu koda politika**. Pēc tam nolaižamajā dialoglodziņā **Piešķirt inventarizācijas iemesla koda politiku** izpildiet vienu no tālāk minētajām darbībām.

    - Lai katram krājumam izmantotu politikas iestatījumus, lai noteiktu, vai inventarizācijas žurnāli tam ir obligāti, ievadiet vērtību (vai dzēsiet esošo vērtību).
    - Lai noliktavai pieprasītu iemesla kodu inventarizācijas žurnālos, atlasiet iemesla politiku, kur lauks **Inventarizācijas iemesla koda tips** ir iestatīts uz *Obligāts*.
    - Ja iemesla kods nav obligāts inventarizācijas žurnālos, atlasiet iemesla politiku, kur lauks **Inventarizācijas iemesla koda tips** ir iestatīts uz *Neobligāts*.

### <a name="assign-counting-reason-code-policies-to-products"></a>Piešķiriet precēm inventarizācijas iemeslu koda politikas

Lai precei piešķirtu inventarizācijas iemesla koda politiku, veiciet šādas darbības.

1. DOdieties uz **Preču informācijas pārvaldība** \> **Preces** \> **Nodotās preces**.
1. Režģī atlasiet preci.
1. Darbību rūtī cilnes **Prece** grupā **Iestātīšana** atlasiet **Inventarizācijas iemeslu koda politika**. Pēc tam nolaižamajā dialoglodziņā **Piešķirt inventarizācijas iemesla koda politiku** izpildiet vienu no tālāk minētajām darbībām.

    - Lai noliktavai izmantotu politikas iestatījumus, lai noteiktu, vai inventarizācijas žurnāli precei ir obligāti, ievadiet vērtību (vai dzēsiet esošo vērtību).
    - Lai precei pieprasītu iemesla kodu inventarizācijas žurnālos, atlasiet iemesla politiku, kur lauks **Inventarizācijas iemesla koda tips** ir iestatīts uz *Obligāts*. Šis iestatījums ignorē visus iemeslu kodu iestatījumus noliktavas līmenī.
    - Ja iemesla kods nav obligāts precei inventarizācijas žurnālos, atlasiet iemesla politiku, kur lauks **Inventarizācijas iemesla koda tips** ir iestatīts uz *Neobligāts*. Šis iestatījums ignorē visus iemeslu kodu iestatījumus noliktavas līmenī.

### <a name="set-up-counting-reason-codes"></a>Inventarizācijas iemeslu kodu iestatīšana

Lai iestatītu inventarizācijas iemesla kodus, veiciet tālāk norādītās darbības.

1. Pārejiet uz sadaļu **Krājumu pārvaldība** \> **Iestatījums** \> **Krājumi** \> **Inventarizācijas iemesla kodi**.
1. Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**.
1. Iestatiet laukus **Inventarizācijas iemesla kods** un **Apraksts** jaunajai rindai.
1. Lai piešķirtu korespondējošo kontu, ievadiet vai atlasiet vērtību laukā **Korespondējošais konts**.

    > [!NOTE]
    > Ja korespondējošais konts ir piešķirts inventarizācijas iemesla kodam, grāmatojot inventarizācijas žurnālu, tam ir inventarizācijas pamatojuma kods, vērtība tiek grāmatota attiecībā pret piešķirto korespondējošo kontu, nevis noklusējuma krājumu grāmatošanas metodes kontu.

### <a name="set-up-counting-reason-code-groups"></a><a name="reason-groups"></a>Iestatiet inventarizācijas iemeslu kodu grupas

*Uzskaites iemeslu kodu grupas* var izmantot kā daļu no mobilās programmas Warehouse Management izvēlnes vienumiem *Pielāgojums* un *Korekcija*, lai ierobežotu inventarizācijas iemeslu kodu sarakstu. (Papildinformāciju par inventarizācijas iemesla kodu grupām skatiet tālāk šīs tēmas sadaļā [Iestatiet mobilās ierīces izvēlnes vienumus pielāgošanai un koriģēšanai](#setup-adjustment-in-out).)

1. Pārejiet uz sadaļu **Krājumu pārvaldība** \> **Iestatījums** \> **Krājumi** \> **Inventarizācijas iemesla koda grupas**.
1. Lai pievienotu grupu, darbību rūtī atlasiet **Jauns**.
1. Iestatiet laukus **Inventarizācijas iemesla grupa** un **Grupas apraksts** jaunajai grupai.
1. Darbību rūtī atlasiet **Saglabāt**.
1. Sadaļā **Detālizētā informācija** un rīkjoslā atlasiet **Jauns**, lai režģim pievienotu rindu. Pēc tam iestatiet lauku **Inventarizācijas iemesla kods** jaunajai rindai. 
1. Pēc vajadzības atkārtojiet iepriekšējo darbību, lai piešķirtu papildu kodus. Ja no grupas ir jānoņem kods, atlasiet to un pēc tam rīkjoslā atlasiet **Dzēst**.

### <a name="set-up-reason-codes-for-mobile-device-menu-items"></a>Iemeslu kodu iestatīšana mobilās ierīces izvēlnes vienumiem

Varat konfigurēt pamatojuma kodus šādiem rīcībā esošo krājumu korekcijas tipiem:

- Cikla inventarizācija
- Inventarizācija uz vietas
- Sliekšņa inventarizācija
- Ienākošā korekcija
- Izejošā korekcija

Vairumā gadījumu varat definēt šādu informāciju par katru atbilstīgo mobilās ierīces izvēlnes elementu:

- Vai iemesla kods tiek rādīts mobilās ierīces darbiniekam inventarizācijas laikā.
- Noklusējuma iemesla kods, kas tiek rādīts mobilās ierīces izvēlnes vienumā.
- Vai lietotājs var rediģēt šo iemesla kodu.

#### <a name="set-up-mobile-device-menu-items-for-a-counting-process"></a>Iestatiet mobilās ierīces izvēlnes vienumus inventarizācijas procesam

Lai iestatītu mobilās ierīces izvēlnes vienumu inventarizācijas procesam, veiciet tālāk norādītās darbības.

1. Dodieties uz **Noliktavas pārvaldība** \> **Iestatījumi** \> **Mobilā ierīce** \> **Mobilās ierīces izvēlnes vienumi**.
1. Atlasiet atbilstīgo izvēlnes elementu saraksta rūtī vai izveidojiet jaunu izvēlnes elementu.
1. Darbību rūtī atlasiet **Cikla inventarizācija**.
1. Laukā **Noklusējuma inventarizācijas iemesla kods** iestatiet noklusējuma iemesla kodu, kas ir jāieraksta, kad šīs mobilās ierīces izvēlnes vienums tiek izmantots, lai veiktu inventarizāciju.
1. Laukā **Parādīt inventarizācijas iemesla kodu** atlasiet vienu no šīm vērtībām:

    - *Rinda* – parāda iemesla kodu pēc katras novirzes ierakstīšanas.
    - *Slēpt* – nerādīt iemesla kodu.

1. Iestatiet **Rediģēt inventarizācijas iemesla kodu** uz *Jā*, lai darbinieks iemesla kodu varētu rediģēt, kad inventarizācijas laikā tas tiek rādīts mobilajā ierīcē. Iestatiet to uz *Nē*, lai neļautu darbiniekam labot kodu.

> [!NOTE]
> Poga **Cikla inventarizācija** var būt iespējota jebkuram mobilās ierīces izvēlnes vienumam, kur var veikt inventarizāciju. Piemēri tostarp ir izvēlnes vienumi inventarizācijai uz vietas, lietotāja noteiktam darbam un sistēmas noteiktam darbam.

#### <a name="set-up-mobile-device-menu-items-for-adjustment-in-and-adjustment-out"></a><a name="setup-adjustment-in-out"></a>Mobilās ierīces izvēlnes vienumu iestatīšana ienākošajai korekcijai un izejošajai korekcijai

Lai iestatītu mobilās ierīces izvēlnes vienumu ienākošajai korekcijai un izejošajai korekcijai, veiciet tālāk norādītās darbības.

1. Dodieties uz **Noliktavas pārvaldība** \> **Iestatījumi** \> **Mobilā ierīce** \> **Mobilās ierīces izvēlnes vienumi**.
1. Lai izveidotu izvēlnes vienumu, darbību rūtī atlasiet **Jauns**.
1. Iestatiet laukus **Mobilās preces nosaukums** un **Nosaukums** jaunajam izvēlnes vienumam.
1. Iestatiet lauku **Režīms** uz *Darbs*.
1. Opciju **Izmantot esošo darbu** iestatiet uz *Nē*.
1. Laukā **Darba izveides process** atlasiet *Ienākošā korekcija* vai *Izējošā korekcija*.
1. Kopsavilkuma cilnē **Vispārīgi**, iestatiet tālāk minētos laukus. (Atlasot šos laukus, tiek pievienoti visi šie lauki *Ienākošā korekcija* vai *Izējošā korekcija* laukā **Darba izveides process**.)

    - **Izmantojiet procesa rokasgrāmatu** - ja veidojat procesu *Izējošā korekcija*, noteikti iestatiet šo opciju uz *Jā*. Ja veidojat procesu *Izējošā korekcija*, šī opcija vienmēr ir iestatīta uz *Jā*.
    - **Noklusējuma inventarizācijas iemesla kods** – iestatiet noklusējuma iemesla kodu, kas ir jāieraksta, kad šīs mobilās ierīces izvēlnes vienums tiek izmantots, lai veiktu inventarizāciju.
    - **Parādīt inventarizācijas iemesla kodu** – atlasiet vienu no šīm vērtībām:

        - *Rinda* – parāda iemesla kodu pēc katras novirzes ierakstīšanas.
        - *Slēpt* – nerādīt iemesla kodu.

    - **Rediģēt inventarizācijas iemesla kodu** – iestatiet šo opciju uz *Jā*, lai darbinieks iemesla kodu varētu rediģēt, kad inventarizācijas laikā tas tiek rādīts mobilajā ierīcē. Iestatiet to uz *Nē*, lai neļautu darbiniekam labot kodu.
    - **Inventarizācijas iemesla koda grupa** – atlasiet iemesla koda grupu, ja vēlaties ierobežot darbiniekiem piedāvāto opciju sarakstu. Informāciju par to, kā iestatīt iemesla koda grupas, skatiet iepriekš šajā tēmā sadaļā [Iestatīt inventarizācijas iemeslu kodu grupas](#reason-groups). 

> [!NOTE]
> Kad piešķirat inventarizācijas iemesla kodu grupu izvēlnes vienumiem *Ienākošā korekcija* un *Izējošā korekcija*, kur opcija **Izmantot procesa rokasgrāmatu** ir iestatīta uz *Jā*, varat iegūt ierobežotu inventarizācijas iemeslu kodu sarakstu kā daļu no apstrādes mobilajā programmā Warehouse Management.
>
> Opcija **Izmantot procesa rokasgrāmatu** var arī palīdzēt novērst lielu koriģējamu daudzumu atkārtošanos kļūdas dēļ. (Piemēram, darbinieks var nejauši skenēt krājuma numura svītrkodu, nevis daudzuma vērtību.) Lai iestatītu šo funkcionalitāti, katram atbilstošajam izvēlnes elementam iestatiet opciju **Izmantot procesa rokasgrāmatu** uz *Jā*. Pēc tam dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Darbinieks** un iestatiet lauku **Pielāgojuma daudzuma ierobežojums** katram atbilstošajam noliktavas darbiniekam, lai norādītu maksimālo korekcijas daudzumu, ko darbinieks var reģistrēt.

## <a name="processing-that-uses-counting-reason-codes"></a>Apstrāde, kas izmanto inventarizācijas iemeslu kodus

Ja darbinieki izmanto mobilo programmu Warehouse Management, pamatojumu kodi tiek ierakstīti. Ja inventarizācijas apstiprināšanas process nav definēts, ierakstītie pamatojuma kodi tiek nekavējoties izmantoti kā daļa no tālāk minētā inventarizācijas žurnāla grāmatošanas.

### <a name="cycle-count-approvals"></a>Cikla inventarizācijas apstiprinājumi

Pirms inventarizācijas apstiprināšanas darbinieks var mainīt ar attiecīgo inventarizāciju saistīto iemesla kodu. Kad inventarizācija ir apstiprināta, iemesla kods tiek ievadīts inventarizācijas žurnāla rindās.

#### <a name="modify-reason-codes-for-cycle-count-approvals"></a>Modificēt cikla inventarizācijas apstiprinājumu iemeslu kodus

Lai modificētu cikla inventarizācijas apstiprinājumu, veiciet šīs darbības.

1. Atlasiet **Noliktavas pārvaldība** \> **Cikla inventarizācija** \> **Izskatīšanu gaidošais cikla inventarizācijas darbs**.
1. Režģī atlasiet cikla inventarizāciju.
1. Darbību rūts cilnē **Darbs** atlasiet **Cikla inventarizācija**. Pēc tam, laukā **Iemeslu kods** atlasiet jaunu iemesla kodu.

Iemeslu kodi tiek pievienoti žurnāla rindām inventarizācijas žurnālos ar tipu *Inventarizācijas žurnāls*.

1. Pārejiet uz sadaļu **Krājumu pārvaldība** \> **Žurnāla ieraksti** \> **Krājumu inventarizācija** \> **Inventarizācija**.
2. Inventarizācijas žurnāla rindas detaļas laukā **Inventarizācijas iemesla kods** atlasiet pamatojuma kodu, kas atbilst pašreizējai situācijai.

### <a name="view-the-reason-codes-recorded-in-the-counting-history"></a>Skatiet inventarizācijas vēsturē ierakstītos iemeslu kodus

Lai skatītu inventarizācijas vēsturē ierakstītos iemeslu kodus, veiciet šīs darbības.

1. Dodieties uz **Krājumu vadība** \> **Uzziņas un atskaites** \> **Inventarizācijas vēsture**.
1. Atlasiet krājumu skaita ierakstu saraksta rūtī.
1. Laukā **Inventarizācijas iemesla kods** skatiet inventarizācijas vēsturi, kas ierakstīta, izmantojot iemesla kodu.

### <a name="use-reason-codes-for-quantity-adjustment-or-online-counting"></a>Izmantot iemeslu kodus daudzuma korekcijai vai tiešsaistes inventarizācijai

Lai daudzuma korekcijai vai tiešsaistes inventarizācijai izmantotu pamatojuma kodu, veiciet šīs darbības.

1. Dodieties uz **Krājumu vadība \> Uzziņas un atskaites \> Rīcībā esošie krājumu saraksts**.
1. Darbību rūtī atlasiet **Daudzuma korekcija**.
1. Atlasiet **Daudzuma korekcija** un pēc tam laukā **Inventarizācijas iemesla kods** atlasiet kādu iemesla kodu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
