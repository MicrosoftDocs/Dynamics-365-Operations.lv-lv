---
title: Novietot pie sienas — novietot veikalā
description: Šajā rakstā ir sniegta informācija par funkcionalitāti Novietot pie sienas - novietot veikala funkcionalitātē. Šī funkcionalitāte ļauj apstrādāt scenārijus, kuros ir jākonsolidē prece fasēšanas sagatavošanas zonā, pamatojoties uz konfigurējamajiem kritērijiem. Tas palīdz samazināt izdošanas laiku, jo ļauj veikt izdošanu vienai mērķa noliktavas vienībai, un var izmantot vairāk izvietošanas vietu nekā klastera izdošana.
author: Mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: af6dcb6d822ab14b0b4b881ca32626ea6eae4c28
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334512"
---
# <a name="put-to-wall---put-to-store"></a>Novietot pie sienas – Novietot veikalā

[!include [banner](../includes/banner.md)]

Funkcionalitāte *Novietot pie sienas – novietot veikalā* ļauj apstrādāt scenārijus, kuros ir jākonsolidē prece fasēšanas sagatavošanas zonā, pamatojoties uz konfigurējamajiem kritērijiem. Tā kā šī funkcionalitāte ļauj veikt izdošanu vienai mērķa noliktavas vienībai, un var izmantot vairāk izvietošanas vietu nekā klastera izdošana, uzņēmumi, kas nosūta uz veikaliem vai apstrādā mazus krājumus, gūs labumu no samazināta izdošanas laika.

Šīs funkcionalitātes darbplūsma novirza izvēlēto preci uz kārtošanas vietu sadalei dažādu veidu konteineros. Parasti katra kārtošanas vieta ietver vairākas kārtošanas pozīcijas. Katra kārtošanas pozīcija tiek piešķirta atbilstoši kritērijiem, ko iestata biznesa process. Raksturīgākie kritēriji ir galamērķis, sūtījums vai krava. Pēc preces saņemšanas, tā tiek sadalīta katrai kārtošanas pozīcijai, pamatojoties uz daudzumu, kas ir saistīts ar pasūtījumu, galamērķi, sūtījumu vai kravu. Kad konteiners ir pilns vai pabeigts, tas tiek pārvietots uz sagatavošanas novietojumu vai nosūtīšanas novietojumu turpmākai apstrādei, atkarībā no biznesa procesa.

Šī noliktavas funkcionalitāte ir attiecināta arī uz citiem nosaukumiem, piemēram, novietot pie gaismas un pārtraukumos.

## <a name="turn-on-the-outbound-sorting-feature"></a>Ieslēgt līdzekli Izejošā kārtošana

Pirms varat izmantot funkcionalitāti *Novietot pie sienas -* nodot veikala funkcionalitātei, *sistēmai* ir jābūt ieslēgtai nosūtīšanas kārtošanas funkcijai. Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu. Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Izejošā kārtošana*

Līdzekli *Izejošā kārtošana* var izmantot savienojumā ar *Organizācijas līmeņa kopuma darbības kods* līdzekli, ja tas ir ieslēgts. Šis līdzeklis ir jāieslēdz arī tad, ja izmantosit iepriekš definētus kodus, kas iestatīti kopuma darbību kodos. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Organizācijas līmeņa kopuma darbības kods*

## <a name="setup"></a>Iestatīt

Šai demonstrācijai tiek izmantoti standarta Contoso dati un noliktava *62*. Tiek izmantoti arī daži papildinājumi, kas tiks minēti vēlāk.

### <a name="location-type"></a>Vietas veids

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Novietojuma veidi**.
1. Darbību rūtī atlasiet **Jauns**, lai izveidotu novietojuma veidu kārtošanai.
1. Iestatiet šādas vērtības:

    - **Novietojuma veids:** *SORT*
    - **Apraksts:** *Kārtot*

1. Atlasiet **Saglabāt**.

### <a name="warehouse-management-parameters"></a>Noliktavas pārvaldības parametri

1. Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktavas pārvaldības parametri**.
1. Cilnē **Vispārīgi**, kopsavilkuma cilnes **Novietojuma veidi** laukā **Kārtošanas novietojuma veids** ievadiet *SORT*.
1. Atlasiet **Saglabāt**.

### <a name="location-profile"></a>Novietojuma profils

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Novietojuma profili**.
1. Darbību rūtī atlasiet **Jauns**, lai izveidotu novietojuma profilu kārtošanas novietojumam.
1. Galvenē iestatiet šādas vērtības:

    - **Novietojuma profila ID:** *Kārtot*
    - **Nosaukums:** *Kārtot*

1. Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:

    - **Novietojuma formāts:** *PACK*
    - **Novietojuma veids:** *SORT*
    - **Izmantot noliktavas vienības izsekošanu:** *Jā*
    - **Atļaut jauktus krājumus:** *Jā*
    - **Atļaut jauktus krājumu statusus:** *Jā*

1. Atlasiet **Saglabāt**.

### <a name="locations"></a>Novietojumi

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Novietojums**.
1. Noņemiet atzīmi izvēles rūtiņai **Ģenerēt novietojuma kontrolciparus**.
1. Darbību rūtī atlasiet **Jauns**, un pēc tam iestatiet šādas vērtības:

    - **Noliktava:** *62*
    - **Novietojums:** *Kārtošana*
    - **Novietojuma profila ID:** *Kārtot*

1. Atlasiet **Saglabāt**.

### <a name="packing-profiles"></a>Iepakošanas profili

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Iepakošana \> Iepakošanas profili**.
1. Darbību rūtī atlasiet **Jauns**, un pēc tam iestatiet šādas vērtības:

    - **Iepakošanas profila ID:** *Sort*
    - **Apraksts:** *Kārtot*
    - **Konteineru iepakošanas politika:** atstājiet šo lauku tukšu.
    - **Konteinera ID režīms:** *Automātiski*
    - **Konteinera veids:** *PALLET 48X48*
    - **Konteinera slēgšanas laikā automātiski izveidot konteineru:** atstājiet šo lauku tukšu.

1. Atlasiet **Saglabāt**.

### <a name="wave-step-codes"></a>Kopuma darbību kodi

Ja līdzeklis *Organizācijas līmeņa kopuma darbības kods* ir ieslēgts, iestatiet tālāk norādīto kodu.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma darbību kodi**.
1. Darbību rūtī atlasiet **Jauns**, un pēc tam iestatiet šādas vērtības:

    - **Kopuma darbības kods:** *Kārtot*
    - **Kopuma darbības apraksts:** *Kārtot*
    - **Kopuma darbības veids:** *Kārtošanas veidne*

1. Atlasiet **Saglabāt**.

### <a name="outbound-sorting-template"></a>Izejošās kārtošanas veidne

Kārtošanas veidne kontrolē, vai tiek veidotas kārtošanas pozīcijas, kādi kritēriji tiek izmantoti un citus kārtošanas procesa atribūtus.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Iepakošana \> Izejošās kārtošanas veidne**.
1. Lai izveidotu kārtošanas veidni, darbību rūtī atlasiet **Jauns**.
1. Jaunās veidnes galvenē iestatiet tālāk norādītās vērtības:

    - **Izejošās kārtošanas veidnes ID:** *Wave Sort*
    - **Apraksts:** *Kopuma kārtošana*
    - **Kārtošanas veidnes veids:** *Kopuma pieprasījums*

        Šis lauks definē procesu, kam tiek izmantota kārtošanas veidne. Ir pieejamas šādas vērtības:

        - **Kopuma pieprasījums** – kārtošanas veidne tiek izmantota procesam *Novietot pie sienas*. Šis veidnes veids tiek izmantots, lai apietu iepakošanas staciju un apstrādātu krājumus tieši no kopuma. Šo veidu varat izmantot, ja **kārtošanas** kopuma procesa metode ir iekļauta kopuma veidnē.
        - **Konteiners** – kārtošanas veidne tiek izmantota procesam *Paletes izveide pēc iepakošanas*. Šis veidnes veids tiek izmantots, lai apstrādātu konteinerus, kas tika slēgti iepakošanas stacijā un ir jākārto paletēs.

    - **Noliktava:** *62*
    - **Novietojums:** *Kārtošana*

1. Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:

    - **Kārtošanas pārbaude:** *Pozīcijas skenēšana*.

        Šis lauks definē pārbaudi, kas ir nepieciešama kārtošanas laikā. Ir pieejamas šādas vērtības:

        - None
        - Numura zīmes skenēšana
        - Pozīcijas skenēšana

    - **Izveidot darbu slēgtai pozīcijai:** *Jā*

        Ja šī opcija ir iestatīta uz *Jā*, kad pozīcija tiek slēgta, tiks izveidots darbs, lai pārvietotu krājumus uz galējo nosūtīšanas vietu. Ja tā ir iestatīta uz *Nē*, krājumi tiks nekavējoties izdoti pasūtījumam, kad pozīcija tiks slēgta.

    - **Pozīcijas piešķiršana:** *Manuāli*

        Šis lauks definē pozīcijas piešķires veidu. Ir pieejamas šādas vērtības:

        - **Manuāli** – lietotājam vienmēr jānorāda, kurā pozīcijā krājums ir jākārto.
        - **Automātiski** – sistēma automātiski novirzīs krājumus uz pozīciju, kad vien iespējams, pamatojoties uz kārtošanas veidnes pārtraukumiem.

    - **Piešķirt kārtošanas pozīcijas kritērijus:** *Izmantot tikai tukšu pozīciju*

        Šis lauks kontrolē, vai krājumi, kuri jau atrodas kārtošanas pozīcijās, ir ņemti vērā, piešķirot pozīciju pieprasījumam. Ir pieejamas šādas vērtības:

        - **Izmantot tikai tukšu pozīciju** – pozīcijas, kurām jau ir ar tām saistīti krājumi, tiks ņemtas vērā.
        - **Pieņemsim, ka pozīcija ir tukša** – visi krājumi, kas jau ir pozīcijā, piešķiršanas laikā netiks ņemti vērā. Tiks izmantotas visas pieejamās pozīcijas.

    - **Kopuma darbības kods:** *Kārtot*

        Ja ir ieslēgts līdzeklis *Organizācijas līmeņa kopuma darbības kods*, tad kopuma darbību kodos ir jābūt iestatītam arī kopuma darbības kodam *Kārtot*.

    - **Automātiski slēgt kārtošanas pozīciju:** *Jā*

        Ja šī opcija ir iestatīta uz *Jā*, kārtošanas pozīcija automātiski tiks slēgta, kad visi darbi, kas tuvojas pozīcijai, būs pabeigti.

    - **Kārtošanas pozīciju skaits:** *3*

        Šis lauks definē maksimālo kārtošanas pozīciju skaitu, ko sistēma izveidos.

    - **Kārtošanas pozīcijas prefikss:** *SP-*

        Šis lauks definē prefiksu, ko sistēma piešķir pirms pozīcijas numura.

    - **Automātiski iepakot kārtošanas pozīciju:** *Jā*

        Ja šī opcija ir iestatīta uz *Jā*, krājumi kārtošanas pozīcijā tiks iepakoti konteinerā, kad pozīcija tiks slēgta.

    - **Iepakošanas profila ID:** *Sort*

        Šis lauks definē iepakošanas profilu, kas tiks izmantots, kad kārtošanas pozīcija tiks iepakota konteinerā.

1. Darbību rūtī atlasiet **Rediģēt vaicājumu**, lai norādītu kritērijus, kas tiek izmantoti šai kārtošanas veidnei.
1. Vaicājuma dialoglodziņa cilnē **Kārtošana** atlasiet **Jauns**, lai pievienotu rindu, un pēc tam iestatiet šādas vērtības:

    - **Tabula:** *Kravas informācija*
    - **Atveidotā tabula:** *Kravas informācija*
    - **Lauks:** *Sūtījuma ID*
    - **Meklēšanas virziens:** *Augošā secībā*

1. Atlasiet **Labi**.
1. Var tikt parādīts šāds ziņojums: “Grupēšana tiks atiestatīta, vai turpināt?” Atlasiet **Jā**.

    Tagad darbību rūtī ir pieejama poga **Izejošās kārtošanas veidnes pārtraukumi**.

1. Darbību rūtī atlasiet **Izejošās kārtošanas veidnes pārtraukumi**.
1. Atzīmējiet izvēles rūtiņu **Grupēt pēc lauka**, lai grupētu pēc sūtījuma ID.

    Šis iestatījums izveidos vienu kārtošanas pozīciju katram sūtījumam, kas ir kopuma konteiners.

1. Atlasiet **Labi**.

### <a name="wave-process-methods"></a>Kopuma apstrādes metodes

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma procesa metodes**.
1. Darbību rūtī atlasiet **Atkārtoti ģenerēt metodes**.

    Pieejamo metožu sarakstam tiek pievienota **kārtošanas** metode, un tai tiek atlasīts kopuma veidnes veids *Nosūtīšana*.

### <a name="wave-templates"></a>Laidiena veidnes

Rediģējiet kopuma veidni, kas tiek izmantota kopuma pieprasījuma kārtošanai.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma veidnes**.
1. Laukā **Kopuma veidnes veids** atlasiet *Nosūtīšana*.
1. Atlasiet esošo veidni **62 Sūtījums pēc noklusējuma**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Kopsavilkuma cilnē **Vispārīgi** veiciet šādas izmaiņas:

    - Iestatiet opciju **Apstrādāt kopumu, to pārvietojot uz noliktavu** uz *Nē*.
    - Iestatiet opciju **Piešķirt atvērtajiem kopumiem** uz *Jā*.

1. Kopsavilkuma cilnē **Metodes** iestatiet **kārtošanas** metodi:

    1. Režģī **Atlikušās metodes** atlasiet **Kārtošana**.
    2. Atlasiet bultiņas pa labi pogu, lai pārvietotu **Kārtošana** uz režģi **Atlasītās metodes**.
    3. Režģī **Atlasītās metodes** atlasiet **Kārtošana**.
    4. Iestatiet lauku **Kopuma darbības kods** uz *Kārtot*.

1. Atlasiet **Saglabāt**.

### <a name="mobile-device-menu-items"></a>Mobilās ierīces izvēlnes vienumi

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Galvenē iestatiet šādas vērtības:

    - **Izvēlnes vienuma nosaukums:** *Kārtot*
    - **Nosaukums:** *Kārtot*
    - **Režīms:** *Netiešs*
    - **Izmantot esošo darbu:** *Nē*

1. Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:

    - **Aktivitātes kods:** *Izejošā kārtošana*
    - **Izmantot procesa ceļvedi:** *Jā* (noklusējuma vērtība)
    - **Izejošās kārtošanas veidnes ID:** *Wave Sort*

1. Atlasiet **Saglabāt**.

### <a name="mobile-device-menu"></a>Mobilās ierīces izvēlne

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlne**.
1. Izvēlņu sarakstā atlasiet **Izejošs**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Režģī **Pieejamās izvēlnes un izvēļņu elementi** meklējiet un atlasiet tikko izveidoto izvēlnes elementu **Kārtot**.
1. Atlasiet bultiņas pa labi pogu, lai pārvietotu **Kārtot** uz režģi **Izvēlnes struktūra**. Šādā veidā jūs pievienojat izvēlnes elementu izvēlnei **Izejošs**.
1. Atlasiet **Saglabāt**.

### <a name="location-directives"></a>Vietas direktīvas

Ir jāizveido novietojuma direktīvas, lai vadītu darbu, kas tiek izveidots pēc kārtošanas pabeigšanas.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Novietojuma direktīvas**.
1. Laukā **Darba pasūtījuma veids** atlasiet *Kārtotu krājumu izdošana*.
1. Darbību rūtī atlasiet **Jauns**.
1. Galvenē iestatiet šādas vērtības:

    - **Secība:** *1*
    - **Nosaukums:** *Novietot pie angāra durvīm*

1. Kopsavilkuma cilnē **Novietojuma direktīvas** iestatiet tālāk norādītās vērtības:

    - **Darba veids:** *Izvietošana*
    - **Vieta:** *6*
    - **Noliktava:** *62*
    - **Direktīvas kods:** atstājiet šo lauku tukšu.
    - **Vairākas SKU:** *Nē*

1. Atlasiet **Saglabāt**, lai padarītu pieejamu kopsavilkuma cilni **Rindas**.
1. Kopsavilkuma cilnē **Rindas** atlasiet **Jauns**, un pēc tam iestatiet šādas vērtības. Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.

    - **Secības numurs:** *1*
    - **No daudzuma:** *0*
    - **Līdz daudzumam:** *1 000 000*

1. Atlasiet **Saglabāt**, lai padarītu pieejamu kopsavilkuma cilni **Novietojuma direktīvu darbības**.
1. Kopsavilkuma cilnē **Novietojuma direktīvu darbības** atlasiet **Jauns**, un pēc tam iestatiet šādas vērtības. Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.

    - **Secības numurs:** *1*
    - **Nosaukums:** *Baydoor*

1. Atlasiet **Saglabāt**, lai padarītu pogu **Rediģēt vaicājumu** pieejamu **Novietojuma direktīvu darbības** kopsavilkuma cilnē.
1. Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Rediģēt vaicājumu**.
1. Vaicājuma dialoglodziņā cilnē **Diapazons** sameklējiet rindu, kurā lauks **Lauks** ir iestatīts uz *Novietojums*. Iestatiet lauku **Kritēriji** šai rindai uz *Angāra durvis*.
1. Lai apstiprinātu rediģēšanu, atlasiet **Labi**.

### <a name="work-classes"></a>Darba klases

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba klases**.
1. Darbību rūtī atlasiet **Jauns**.
1. Galvenē iestatiet šādas vērtības:

    - **Darba klases ID:** *Kārtošana*
    - **Apraksts:** *Kārtošana*
    - **Darba pasūtījuma veids:** *Kārtotu krājumu izdošana*

1. Atlasiet **Saglabāt**.

### <a name="work-templates"></a>Darbu veidnes

1. Dodieties uz **Noliktavas pārvaldība \> Darbs \> Darbu veidnes**.
1. Laukā **Darba pasūtījuma veids** atlasiet *Pārdošanas pasūtījumi*.
1. Režģī atlasiet darba veidni **62 izdot iepakošanai**.
1. Darbību rūtī atlasiet **Darba galvenes pārtraukumi**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Rindā, kur lauks **Lauka nosaukums** ir iestatīts uz *Sūtījuma ID*, noņemiet atzīmi izvēles rūtiņā **Grupēt pēc šī lauka**.
1. Atlasiet **Saglabāt** un pēc tam aizveriet dialoglodziņu **Darba galvenes pārtraukumi**.
1. Laukā **Darba pasūtījuma veids** atlasiet *Kārtotu krājumu izdošana*.
1. Atlasiet **Jauns**, lai izveidotu darba veidni.
1. Sadaļā **Pārskats** iestatiet šādas vērtības. Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.

    - **Darba veidne:** *Kārtota izdošana*
    - **Darba veidnes apraksts:** *Kārtota izdošana*

1. Atlasiet **Saglabāt**, lai padarītu pieejamu sadaļu **Darba veidnes informācija**.
1. Sadaļā **Darba veidnes informācija** tiks izveidotas divas rindas. Atlasiet **Jauns** un pēc tam 1. rindai iestatiet šādas vērtības:

    - **Darba veids:** *Izdošana*
    - **Obligāts:** atlasīts (= *Jā*)
    - **Darba klases ID:** *Kārtošana*

1. Vēlreiz atlasiet **Jauns** un pēc tam 2. rindai iestatiet šādas vērtības:

    - **Darba veids:** *Izvietošana*
    - **Obligāts:** atlasīts (= *Jā*)
    - **Darba klases ID:** *Kārtošana*

1. Atlasiet **Saglabāt**.

## <a name="example-scenario"></a>Piemēra situācija

Šis scenārijs simulē situāciju, kad noliktavas novietojumos tiek uzglabāti mazi krājumi un tie pirms nosūtīšanas ir jāiepako kastēs, bet iepakošanas stacijas funkcionalitāte nav īsti piemērota. Darbinieki vienlaicīgi izdot pasūtījumus vairākiem klientiem un atšķirīgās adresēs, lai palielinātu izdošanas ātrumu. Kad izdošana ir pabeigta, darbinieki ierodas kārtošanas vietā, kur izdotos krājumus var kārtot pareizajā kastē, pamatojoties uz nepieciešamajiem kritērijiem. Šajā piemērā sūtījuma ID tiks izmantots, lai noteiktu pareizo kasti, jo katram sūtījumam ir cita adrese. Kad visi noslodzes krājumi ir iepakoti un sakārtoti pēc sūtījuma, kastes tiks pārvietotas uz sagatavošanas zonu, un visbeidzot ielādētas kravas automašīnā.

Pirms sākat scenāriju, pārliecinieties, vai noliktavai ir pareizi iestatīta visa standarta noliktavas funkcionalitāte. Šim nolūkam tiek izmantota standarta Contoso noliktava *62*. Standarta konfigurācijas nav mainītas papildus tam, kas aprakstīts iestatījumā.

### <a name="create-demand"></a>Pieprasījuma izveide

Lai funkcionalitāti varētu demonstrēt, ir jāizveido daži pieprasījumi. Šim scenārijam tiks izveidoti trīs pārdošanas pasūtījumi trīs dažādiem klientiem, lai simulētu dažādas piegādes adreses. Šādā veidā tiks izveidoti trīs atsevišķi sūtījumi.

Pirms pārdošanas pasūtījumu un sūtījumu izveides, ir jāpārliecinās, vai izdošanas vietās ir pietiekami daudz krājumu visiem krājumiem pasūtījumos. Pārskatiet novietojuma direktīvas iestatījumus, lai apstiprinātu izdošanas vietas, kas tiek izmantotas pārdošanas pasūtījuma izdošanai. Pielāgojot krājumus, varat izveidot manuālo kustību, izmantot papildināšanu vai jebkuru citu plūsmu. Pēc tam rezervējiet krājumus.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atlasiet **Jauns**, lai 1. pasūtījumam izveidotu pārdošanas pasūtījumu.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - **Klients:** *US-001*
    - **Noliktava:** *62*

1. Atlasiet **Labi**.
1. Kopsavilkuma cilnei **Pārdošanas pasūtījuma rindas** tiek pievienota jauna rinda. Iestatiet šādas vērtības:

    - **Krājuma numurs:** *A0001*
    - **Daudzums:** *5*

1. Atlasiet **Pievienot rindu**, lai pievienotu otro rindu, un iestatiet šādas vērtības:

    - **Krājuma numurs:** *A0002*
    - **Daudzums:** *10*

1. Atkārtojiet šīs darbības katrai pasūtījuma pārdošanas rindai, lai rezervētu tai krājumus:

    1. Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** izvēlnē **Krājumi** atlasiet **Rezervācija**.
    1. Lapā **Rezervācija** atlasiet **Rezervēt laidienu**, un pēc tam aizveriet lapu.
    1. Atlasiet **Saglabāt**.

1. Atlasiet **Jauns**, lai 2. pasūtījumam izveidotu pārdošanas pasūtījumu.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - **Klients:** *US-004*
    - **Noliktava:** *62*

1. Atlasiet **Labi**.
1. Kopsavilkuma cilnei **Pārdošanas pasūtījuma rindas** tiek pievienota jauna rinda. Iestatiet šādas vērtības:

    - **Krājuma numurs:** *A0001*
    - **Daudzums:** *7*

1. Atlasiet **Pievienot rindu**, lai pievienotu otro rindu, un iestatiet šādas vērtības:

    - **Krājuma numurs:** *A0002*
    - **Daudzums:** *3*

1. Atkārtojiet šīs darbības katrai pasūtījuma pārdošanas rindai, lai rezervētu tai krājumus:

    1. Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** izvēlnē **Krājumi** atlasiet **Rezervācija**.
    1. Lapā **Rezervācija** atlasiet **Rezervēt laidienu**, un pēc tam aizveriet lapu.
    1. Atlasiet **Saglabāt**.

1. Atlasiet **Jauns**, lai 3. pasūtījumam izveidotu pārdošanas pasūtījumu.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - **Klients:** *US-007*
    - **Noliktava:** *62*

1. Atlasiet **Labi**.
1. Kopsavilkuma cilnei **Pārdošanas pasūtījuma rindas** tiek pievienota jauna rinda. Iestatiet šādas vērtības:

    - **Krājuma numurs:** *A0001*
    - **Daudzums:** *8*

1. Veiciet tālāk norādītās darbības, lai rezervētu krājumus pārdošanas rindām:

    1. Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** izvēlnē **Krājumi** atlasiet **Rezervācija**.
    1. Lapā **Rezervācija** atlasiet **Rezervēt laidienu**, un pēc tam aizveriet lapu.
    1. Atlasiet **Saglabāt**.

Izpildiet šo procedūru, lai katru pārdošanas pasūtījumu izlaistu noliktavā. Tiks izveidoti trīs dažādi sūtījumi. Pēc tam visi trīs sūtījumi ir jāpievieno vienam jaunam kopumam.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Režģī atlasiet pirmo izveidoto pārdošanas pasūtījumu.
1. Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.

    Tiks saņemts informatīvs ziņojums, kurā norādīts izveidotais kopuma ID un sūtījuma ID.

1. Atkārtojiet iepriekšējās darbības, lai izlaistu noliktavā 2. un 3. pārdošanas pasūtījumu. Ievērojiet, ka saņemtais informatīvais ziņojums norāda, ka sūtījums ir pievienots kopumam, kas tika izveidots, izlaižot 1. pārdošanas pasūtījumu.
1. Dodieties uz **Noliktavas pārvaldība \> Izejošie kopumi \> Sūtījuma kopumi \> Visi kopumi**.
1. Atlasiet kopuma ID, kas tika izveidots no pārdošanas pasūtījuma izlaides, lai atvērtu lapu **Kopumi**. Šajā lapā tiek rādīta kopuma informācija. Kopsavilkuma cilne **Kopuma rindas** rāda izveidotos sūtījumus.

    Tagad ir jāizveido darbs, lai krājumus no izdošanas vietām pārnestu uz kārtošanas vietām.

1. Darbību rūtī atlasiet **Apstrādāt**.

    Kopuma apstrādes laikā kārtošanas metode izmanto kārtošanas veidni, lai piešķirtu krājumus kārtošanas pozīcijām. Kad kopuma apstrāde ir pabeigta, tiks saņemts informatīvs ziņojums, ka kopums ir iegrāmatots un darbs ir izveidots.

1. Darbību rūtī cilnes **Kopums** grupā **Saistītā informācija**, atlasiet **Darbs**, lai skatītu izveidoto darbu. Pierakstiet darba ID.
1. Dodieties uz **Noliktavas pārvaldība \> Iepakošana un konteinerizēšana \> Izejošās kārtošanas pozīciju piešķires**.
1. Kreisajā kolonnā varat skatīt izejošo kārtošanas pozīciju, kas tika izveidota katram sūtījumam.
1. Kopsavilkuma cilnē **Kārtošanas pozīcijas kritēriji** varat skatīt šīs pozīcijas sūtījuma ID.

Viens darba ID ir izveidots, lai krājumus no izdošanas vietām pārnestu uz kārtošanas vietām. Lai pabeigtu darbu, ir nepieciešams darba ID, kas tika izveidots kopuma apstrādes laikā.

### <a name="sales-order-picking-to-the-sorting-location"></a>Pārdošanas pasūtījuma izdošana kārtošanas vietai

1. Piesakieties mobilajā programmā kā darbinieks noliktavā *62*.
1. Galvenajā izvēlnē atlasiet **Izejošs**.
1. Izvēlnē **Izejošs** atlasiet **Pārdošanas izdošana**.
1. Atlasiet lauku **ID** un pēc tam ievadiet darba ID no kopuma apstrādes.
1. Apstipriniet ievadīto.

    Pēc tam tiek parādīta uzvedne ievadīt mērķa noliktavas vienību (LP). Ievērojiet, ka 1. pārdošanas pasūtījuma 1. rinda ir jāizdod un jāpievieno mērķa noliktavas vienībai. Tiek parādīts krājuma kods, daudzums, krājuma apraksts un izdošanas vieta.

1. Laukā **Mērķa LP** ievadiet unikālu noliktavas vienības identifikatoru.

    Visas izveidotās rindas no apstrādātā kopuma tiks izdotas tai pašai mērķa noliktavas vienībai.

1. Apstipriniet ievadīto.

    Mobilā programma tagad piedāvā lapu sēriju **Izdošana**, kas norāda uz izdošanas vietu, krājumu un daudzumu, kas ir jāizdod. Pēc tam, kad izdotais krājums ir pievienots noliktavas vienībai, tiks apstiprināts izdošanas darbs. Pēdējā lapa būs darbs, lai izdotos krājumus izvietotu kārtošanas vietā.

1. Apstipriniet pirmo izdošanas darbu.
1. Tiek parādīts nākamais izdošanas darbs. Apstipriniet izdošanu.
1. Turpiniet apstiprināt atlikušo izdošanas darbu.
1. Pēdējā darbība ir pabeigt izvietošanas darbu. Apstipriniet izvietošanu kārtošanas vietā.

    Tiek saņemts ziņojums “Darbs pabeigts”.

1. Izejiet no mobilās programmas **Pārdošanas izdošana**.

### <a name="sortingput-to-wall"></a>Kārtošana/novietot pie sienas

Tagad, kad visi krājumi ir novietoti kārtošanas vietā, tie ir jākārto pareizajā kārtošanas pozīcijā.

1. Piesakieties mobilajā programmā.
1. Galvenajā izvēlnē atlasiet **Izejošs**.
1. Izvēlnē **Izejošs** atlasiet **Kārtot**, lai sāktu kārtot krājumus.
1. Laukā **LP/CON** ievadiet mērķa noliktavas vienību izdotajam pārdošanas pasūtījuma darbam.
1. Apstipriniet ievadīto.
1. Ievadiet krājuma kodu, kas jākārto kā pirmais.
1. Sistēma nosaka pirmo kārtošanas pozīciju, kas ir jāparāda. Apstipriniet kārtošanas pozīciju.
1. Tiek pieprasīts piešķirt noliktavas vienību kārtošanas pozīcijai. Atlasiet lauku **LP**, ievadiet unikālo noliktavas vienības identifikatoru un pēc tam apstipriniet ierakstu.

    Tā kā kārtošanas pozīcija ir saistīta ar sūtījuma ID, izdotie krājumi tiks kārtoti noliktavas vienībā, kas ir raksturīga izejošajam sūtījumam un pārdošanas pasūtījumam.

    Nākamā lapa parāda krājuma ID, daudzumu, kārtošanas pozīcijas ID un “no” (izdošana) un “uz” (kārtošana) noliktavas vienības ID. Šajā lapā sniegtā informācija sniedz norādījumus, kārtot norādīto krājumu un daudzumus no izdošanas noliktavas vienības uz kārtošanas noliktavas vienību.

1. Apstipriniet kārtošanas pozīciju.
1. Kārtojiet krājumus pirmajā kārtošanas pozīcijā. Kad esat beidzis, sistēma novirza jūs uz nākamo kārtošanas pozīciju.
1. Atkārtojiet šo procesu visām izdošanas rindām darba pasūtījumā. Šo procesu ir jāizmanto arī tad, ja ir vairākas izdošanas rindas ar vienādu krājuma kodu.

    Atkārtojot šo procesu visiem krājumiem, sistēma novērtē nākamā skenētā krājuma (darba rinda) kritērijus un nosaka, kurā kārtošanas pozīcijā tie ir jānovieto. Jūs automātiski tiekat novirzīts novietot krājumu pareizā kārtošanas pozīcijā. Atkarībā no apstiprinājuma iestatījumiem, jūs tiekat novirzīts apstiprināt šo darbību, ievadot pozīcijas numuru vai noliktavas vienības ID.

    > [!NOTE]
    > Ja automātiskā kārtošana ir ieslēgta, manuālā ignorēšana nav pieejama.

1. Kad esat pabeidzis, programmā Microsoft Dynamics 365 Supply Chain Management atveriet lapu **Izejošās kārtošanas pozīciju piešķires**, lai pārskatītu pozīciju statusu.

    - Ja pozīcijas tiek slēgtas automātiski, atlasiet **Rādīt slēgto**, lai parādītu slēgtās pozīcijas.
    - Ievērojiet, ka tiek parādītas kārtošanas pozīcijas transakcijas. Tiek parādīts krājums un daudzums, kas tika apstrādāts, izmantojot pozīciju.

    Iestatot izejošās kārtošanas veidni, opcija **Automātiski slēgt kārtošanas pozīciju** ir jāiestata uz *Jā*. Tādēļ pozīcija tiek automātiski slēgta pēc tam, kad tajā tiek novietots pēdējais paredzētais krājums. Kārtošanas pozīcijas statuss ir **Slēgts** un ir izveidots darbs, lai pārvietotu kārtotos krājumus uz novietojumu *Angāra durvis*.

1. Pabeidziet kārtoto krājumu izdošanas darbu, lai pārvietotu krājumus uz nosūtīšanas vietu. Kad krājumi ir gatavi, apstipriniet tos nosūtīšanai.

> [!NOTE]
> Lai kārtoto krājumu izdošanas darbs tiktu apstrādāts pareizi, pārvietošanas un iekraušanas procesam ir jāizmanto mobilās ierīces izvēlnes elements, kam ir darba klases ID, kur lauks **Darba pasūtījuma veids** ir iestatīts uz *Kārtotu krājumu izdošana*.

### <a name="manually-close-a-position-optional"></a>Pozīcijas manuāla slēgšana (neobligāts)

Ja kārtošanas pozīcijas jāslēdz manuāli, izejošās kārtošanas veidnes opcijai **Automātiski slēgt kārtošanas pozīciju** jābūt iestatītai uz *Nē*, un slēgšana jāveic pirms krājumus var pārvietot uz angāra durvis zonu. Pozīcijas var slēgt dažādos veidos:

- Ar lietotni Warehouse Management mobile:

    - Lietotājs var skenēt vienu no krājumiem, kas jau ir pozīcijā, un pēc tam atlasīt **Slēgt**, lai slēgtu pozīciju.
    - Ja lietotājs skenē konteineru, kas jau ir sakārtots, tiek parādīts kļūdas ziņojums. Tomēr lietotājs joprojām var turpināt pozīcijas slēgšanu.

- Izmantojot lapu Microsoft Dynamics 365 Supply Chain Management **Izejošās kārtošanas pozīcijas piešķires**:

    - Lietotājs var atlasīt izejošās kārtošanas pozīcijas ierakstu un pēc tam darbību rūtī atlasīt **Slēgt pozīciju**.

## <a name="tips"></a>Padomi

- Krājumus nevar pārvietot starp pozīcijām pēc to piešķiršanas. Sistēma novērtē, cik daudz no katra krājuma ir jāpārvieto uz noteiktu pozīciju.
- Kārtošanas veidni var konfigurēt, lai automātiski izveidotu konteinerus, kad pozīcijas ir slēgtas. Šī pieeja veidos standarta konteinera ID struktūru, kas balstīta uz norādīto iepakošanas profilu.

> [!IMPORTANT]
> Pēc tam, kad no kārtošanas vietas ir izveidots pārvietošanas darbs, darbu nedrīkst atcelt. Pretējā gadījumā pozīcija un tajā esošie konteineri tiks dzēsti no sistēmas un nebūs pieejami turpmākai apstrādei. Tiks noņemti arī krājumi.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]