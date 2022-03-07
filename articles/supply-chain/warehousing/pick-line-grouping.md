---
title: Izdošanas rindu grupēšana
description: Šajā tēmā ir sniegts pārskats par izdošanas rindu grupēšanu.
author: Mirzaab
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 076a4dfdc49525eef616d1008073371be1dd4a248cd6f16d395b544ae70e7531
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757498"
---
# <a name="pick-line-grouping"></a>Izdošanas rindu grupēšana

[!include [banner](../includes/banner.md)]

Izdošanas rindu grupēšanā vairākas darba rindas, kurām ir viens un tas pats vienums un novietojums, var apvienot vienā savākšanas programmā, kas lietotājam tiek uzrādīta mobilajā ierīcē. Tādējādi noliktavas darbinieki var saņemt visefektīvākos iespējamos norādījumus, bet tiek uzturēta arī nepieciešamā darba līniju nodalīšana sistēmā (piemēram, dažādiem konteineriem un pasūtījumiem).

## <a name="turn-on-the-pick-line-grouping-feature"></a>Darba izdošanas rindas pārskata līdzekļa ieslēgšana

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [Funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams. Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Izvēles rindu grupēšana*

## <a name="set-up-pick-line-grouping"></a>Izdošanas rindu grupēšanas iestatīšana

### <a name="create-a-mobile-device-menu-item"></a>Mobilās ierīces izvēlnes elementa izveide

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Laukā **Izvēlnes elementa nosaukums** ievadiet *Pārdošanas grupas rindu izdošana*.
1. Laukā **Nosaukums** ievadiet *Pārdošanas grupas rindas izdošana*. Šis nosaukums tiks rādīts mobilās ierīces izvēlnē.
1. Laukā **Režīms** atlasiet *Darbs*.
1. Iestatiet opciju **Izmantot esošo darbu** uz *Jā*.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:

    - Laukā **Noteica** atlasiet *Noteica lietotājs*.
    - Iestatiet opciju **Ģenerēt pozīcijas unikālo noliktavas vienības identifikatoru** uz *Jā*.
    - Atlasiet opcijas **Grupas izdošana** iestatījumu *Jā*.
    - Pieņemiet noklusējuma vērtības atlikušajām funkcijām.

1. Kopsavilkuma cilnē Darba klases veiciet šīs darbības, lai konfigurētu mobilās ierīces izvēlnes vienumam derīgās darba klases:

    1. Kopsavilkuma cilnē **Darba klases** atlasiet **Jauns**.
    2. Laukā **Darba klases ID** atlasiet *Pārdošana* vai *SO izdošana* atkarībā no noliktavas, kuru izmantosiet. Šim scenārijam atlasiet *SO izdošana*.

        Galvenē iestatiet lauku **Darba pasūtījuma veids** uz *Pirkšanas pasūtījumi*.

### <a name="set-up-a-mobile-device-menu"></a>Mobilās ierīces izvēlnes iestatīšana

Sekojiet šiem soļiem, lai pievienotu tikko izveidoto izvēlnes elementu **Nosūtīšanas** izvēlnei.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlne**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Saraksta rūtī ir redzamas visas esošās mobilās ierīces izvēlnes. Sarakstā atlasiet *Izejošie*.
1. Režģī **Pieejamās izvēlnes un izvēļņu elementi** meklējiet un atlasiet tikko izveidoto izvēlnes elementu *Pārdošanas grupas rindu izdošana*.
1. Atlasiet labo bultiņu, lai pārvietotu *PO rindas saņemšanas* izvēlnes elementu **Izvēlņu struktūras** sarakstā.
1. Izmantojiet pogu uz augšu vai uz leju, lai pārvietotu izvēlnes elementu vēlamajā pozīcijā izvēlnē.
1. Darbību rūtī atlasiet **Saglabāt**.

### <a name="set-up-a-work-template"></a>Darba veidnes iestatīšana

1. Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba veidnes**.
1. Laukā **Darba pasūtījuma veids** atlasiet *Pārdošanas pasūtījumi*.
1. Režģī **Pārskats** atrodiet un atlasiet darba veidni, kas jāizmanto ar šo funkciju. Šim scenārijam atlasiet *51 izdot stadijai* veidni.
1. Darbību rūtī atlasiet **Rediģēt vaicājumu**.
1. Vaicājuma dialoglodziņa cilnē **Kārtošana** atlasiet **Pievienot**, lai pievienotu rindu, un pēc tam iestatiet šādas vērtības:

    - Kolonnā **Tabula** atlasiet *Pagaidu darba transakcijas*.
    - Laukā **Atveidotā tabula** atlasiet *Pagaidu darba transakcijas*.
    - Kolonnā **Lauks** atlasiet *Vienuma numurs*.
    - Laukā **Meklēšanas virziens** atlasiet *Augošā secībā*.

1. Atlasiet **Labi**, lai iestatījumus saglabātu un aizvērtu dialoglodziņu.
1. Var tikt parādīts šāds ziņojums: “Grupēšana tiks atiestatīta, vai turpināt?” Lai turpinātu, atlasiet **Jā**.

> [!IMPORTANT]
> Lai izdošanas rindu grupēšanas funkcionalitāte darbotos, darba rindas ir jākārto pēc vienuma ID. Ja rindas, kurām ir vienādi vienumi, netiek kārtotas viena pēc otras, tās netiks grupētas.

## <a name="example"></a>Paraugs

### <a name="create-picking-work"></a>Izveidot izdošanas darbu

Pirms varēsiet iestatīt izdošanas rindas grupēšanu, ir jāizveido daži piemēroti izejošie darbi.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atlasiet **Jauns**, lai izveidotu pārdošanas pasūtījumu.
1. Laukā **Debitora konts** atlasiet *US-004*.
1. Kopsavilkuma cilnes **Vispārīgi** laukā **Noliktava** atlasiet *51*.
1. Atlasiet **Labi**.
1. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** pievienojiet šādas sešas rindas:

    - **1. rinda:** laukā **Krājuma numurs**, atlasiet *M9200*. Laukā **Daudzums** ievadiet *3*.
    - **2. rinda:** laukā **Krājuma numurs**, atlasiet *M9201*. Laukā **Daudzums** ievadiet *3*.
    - **3. rinda:** laukā **Krājuma numurs**, atlasiet *M9202*. Laukā **Daudzums** ievadiet *2*.
    - **4. rinda:** laukā **Krājuma numurs**, atlasiet *M9200*. Laukā **Daudzums** ievadiet *1*.
    - **5. rinda:** laukā **Krājuma numurs**, atlasiet *M9200*. Laukā **Daudzums** ievadiet *3*.
    - **6. rinda:** laukā **Krājuma numurs**, atlasiet *M9202*. Laukā **Daudzums** ievadiet *7*.

    Šeit ir kopsavilkums par kopējiem daudzumiem katram krājumam:

    - **Krājums M9200:** *7* katram
    - **Krājums M9201:** *3* katram
    - **Krājums M9202:** *9* katram

1. Pirms pasūtījumu izdošanas noliktavā jāpārliecinās, vai savākšanas vietās ir pietiekami daudz krājumu visām precēm visos pasūtījumos. Pārskatiet **Atrašanās vietas direktīvas** iestatījumu, lai noteiktu, kuras izdošanas vietas tiek izmantotas pārdošanas pasūtījuma izdošanai. Ja izmantojat Contoso demonstrācijas datu vidi noliktavai *51*, apstipriniet, ka ir pieejami krājumi.

    Tagad krājums ir jārezervē katrai rindai.

1. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** atlasiet vienu no rezervējamajām rindām.
1. Izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.
1. Lapas **Rezervācija** darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu krājumus. Tad aizveriet lapu.
1. Atlikušajām rindām, kas ir jārezervē, atkārtojiet 8. - 10. soli.

    Atlasiet pārdošanas pasūtījumu, kuru tikko izlaidāt noliktavā.

1. Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.

    Jūs saņemat ziņojumu, ka sūtījums un kopums ir izveidoti un ka kopums ir iesniegts palaišanai partijā.

    Kad kopums un visi lejupstraumes darbi ir pabeigti, darbam ar sešām rindām tiek izveidots darba ID. Rindas tiek kārtotas pēc krājuma koda.

1. Dodieties uz **Noliktavas pārvaldība \> Darbs \> Visi darbi**, lai skatītu izveidoto darbu. Atzīmējiet **Noslodzes ID** vērtību, lai to varētu izmantot nākamajā procedūrā.

### <a name="initiate-picking-from-the-mobile-device"></a>Sākt izdošanu no mobilās ierīces

1. Piesakieties mobilajā ierīcē kā lietotājs, kurš ir iestatīts noliktavai *51*.
1. Mobilajā ierīcē atlasiet izvēlni, kurā ir iekļauts jaunais mobilās ierīces izvēlnes vienums. Šim scenārijam atlasiet **Izejošie**.
1. Atlasiet izvēlnes vienumu **Pārdošanas grupas rindas izdošana** un iniciējiet izdošanu.
1. Ievadiet **Darba ID** vērtību, par kuru izdarījāt piezīmi iepriekšējā procedūrā.

    Vajadzētu redzēt izdošanas soli, kur visas krājuma *M9200* izdošanas rindas ir grupētas, un jums jāsaņem instrukcija izdot katrus *7* no *M9200* krājumiem.

    > [!IMPORTANT]
    > Mobilajā ierīcē izdošanas darbs trīs izdošanas darba rindām ir apkopots lietotāja vienā izdošanas solī.

1. Apstipriniet izdošanas darbību.
1. Pārejiet uz darba procesa klienta ekrānu un ievērojiet, ka visas trīs savākšanas rindas krājumam *M9200* tika slēgtas vienlaicīgi.
1. Atgriezieties mobilajā ierīcē un turpiniet izdot. Ir jānorāda krājuma *M9201* 4. darba rinda. Pasūtījumā bija tikai viena darba rinda, tāpēc nav ko uzkrāt.
1. Apstipriniet izdošanas darbību.
1. Pēdējā izdošanas darbība mobilajā ierīcē apkopo pēdējās divas izdošanas rindas no darba pasūtījuma.
1. Pabeidziet izdošanas darbību pa *9* no katra krājuma *M9202*.
1. Apstipriniet nolikšanas darbību un visus papildu izdošanas/nolikšanas pārus, lai pabeigtu darbu.

> [!IMPORTANT]
>
> - Darba rindas var grupēt tikai tad, ja tās ir secīgas.
> - Šī funkcionalitāte netiek atbalstīta:
>
>   - Pieļaujamā svara krājumi
>
>    Ja darbā ir kādi pieļaujamā svara krājumi, jūs pirms izdošanas uzsākšanas saņemsit kļūdas ziņojumu.
>
>   - Vienību izdošana
>   - Darba rindas, kurām ir nepabeigti papildināšanas darbi
>   - Pārizidošana
>   - Saīsināta izdošana ar krājuma atkārtotu sadali


[!INCLUDE[footer-include](../../includes/footer-banner.md)]