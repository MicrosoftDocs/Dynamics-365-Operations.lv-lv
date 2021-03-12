---
title: Izvietošanas klasteri
description: Izvietošanas klasteri piedāvā veidu, kā vienlaicīgi izvēlēties vairākas numura zīmes un pēc tam lietot tās izvietošanai dažādās atrašanās vietās. Tie var būt ļoti noderīgi mazumtirdzniecības uzņēmumiem, kur numura zīmes parasti nav pilnas noliktavas paletes.
author: Mirzaab
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 297792e90b3d2da0d738f5cbaa14779bc17ea3c8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996202"
---
# <a name="putaway-clusters"></a>Izvietošanas klasteri

[!include [banner](../includes/banner.md)]

Izvietošanas klasteri piedāvā veidu, kā vienlaicīgi izvēlēties vairākas numura zīmes un pēc tam lietot tās izvietošanai dažādās atrašanās vietās. Šis process bieži tiek saukts par *nodošanas-saņemšanas maršrutu*. Izvietošanas klasteri var būt ļoti noderīgi mazumtirdzniecības uzņēmumiem, kur numura zīmes parasti nav pilnas noliktavas paletes. 

## <a name="turn-on-the-cluster-putaway-feature"></a>Ieslēgt līdzekli klasteru izvietošana

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu. Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Klasteru izvietošanas līdzeklis*

## <a name="setup-for-the-example-scenario"></a>Piemēra scenārija iestatījumi

### <a name="cluster-profiles"></a>Klastera profili

Izvietošanas klastera profils nosaka, kur krājums nonāks, pamatojoties uz novietojumu, kas ir piešķirts krājumam saņemšanas laikā. Ja ir nepieciešami dažādi klasteri, katram mobilās ierīces izvēlnes vienumam jāizveido cits izvietošanas klasters.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Mobilā ierīce \> Klastera profili**.
1. Darbību rūtī atlasiet **Jauns**.
1. **Galvenes** skatā iestatiet šādas vērtības:

    - **Izvietošanas klastera profila ID:** *Klasteru izvietošana*
    - **Izvietošanas klastera profila ID nosaukums:** *Klasteru izvietošana*
    - **Klastera veids:** *izvietošana*
    - **Kārtas numurs:** akceptējiet noklusējuma vērtību.

1. Atlasiet **Saglabāt**, lai padarītu pieejamus nepieciešamos laukus kopsavilkuma cilnē **Vispārīgi**.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:

    - **Klastera piešķiršanas laiks:** *Saņemšanas brīdī*

        Šis lauks nosaka, vai izvietošanas klasteris ir jāpiešķir uzreiz pēc krājuma saņemšanas vai arī tas ir jākārto vēlāk.

    - **Klastera piešķiršanas kārtula:** *Manuāla*

        Vai sistēmai ir automātiski jānosaka klastera piešķiršana, vai lietotājs to dara manuāli?

    - **Direktīvas kods:** atstājiet šo lauku tukšu.
    - **Izvietošanas klastera atrašana:** *Kvīts*

        Ir pieejamas šādas vērtības:

        - **Kvīts** - atrašanās vieta ir nekavējoties atrasta kvīts saņemšanas laikā.
        - **Klastera aizvēršana** - atrašanās vieta ir atrasta, kad klasteris ir slēgts.
        - **Lietotājs ir novirzīts** – atrašanās vieta tiek atrasta, kad numura zīme tiek saņemta no izvietošanas klastera. Šādā gadījumā vieta netiek norādīta, kad tiek izveidots izvietošanas darbs. Izvietošanas laikā lietotājam ir jāskenē numura zīme vai darba ID, lai sāktu izvietošanas darbību. Pēc tam sistēma atkal atrod izvietošanas vietu un paziņo lietotājam, kur novietot saņemto daudzumu.

    - **Izvietošanas klasteris katram lietotājam:** *Nē*

        Šis lauks nosaka, vai katram klasterim ir jābūt unikālam katram lietotājam, kad klasteri tiek piešķirti automātiski. Tas ir pieejams tikai tad, ja **Klastera piešķiršanas kārtulas** lauks ir iestatīts uz *Automātisks*.

    - **Vienības ierobežojums:** atstājiet šo lauku tukšu.

        Šis lauks nosaka vienību, kas jāsaņem, lai profils būtu derīgs. Ja tas ir atstāts tukšs, visas vienības ir derīgas.

    - **Darba vienības pārtraukums:** *Individuāls*

        Šis lauks nosaka, vai visi krājumi ir jākonsolidē (izmantojot klastera ID un numura zīmi) uz vienas numura zīmes, kad klasteris ir slēgts, un vai tas ir jānovieto atstatus kā viena numura zīme vai atsevišķi uz saņemtajām numura plāksnēm. Šis lauks nav pieejams, ja **Izvietošanas klastera atrašanas** lauks ir iestatīts uz *Kvīts*.

    - **Klasteris turpina pastāvēt kā pamata numura zīme:** *Nē*

        Ja šī opcija ir iestatīta uz *Jā*, kad izvietošanas solis ir pabeigts, klastera ID kļūs par pamata numura zīmi, un visi klastera ID vienumi tiks saistīti ar šo pamata numura zīmi.

1. Kopsavilkuma cilnē **Klastera šķirošana** varat definēt izvietošanas šķirošanas kritērijus. Rīkjoslā atlasiet **Jauns**, lai pievienotu rindu, un tad iestatiet šādas vērtības:

    - **Kārtas numurs:** akceptējiet noklusējuma vērtību.
    - **Lauka nosaukums:** *WMSLocationId*

        Šis lauks nosaka lauku, kas šai rindai jāizmanto kā kārtošanas kritērijs.

    - **Kārtošana:** *Augošā secībā*

        Šis lauks nosaka, vai kārtošanai vajadzētu tikt veiktai augošā vai dilstošā secībā.

1. Kopsavilkuma cilnē **Klastera darba veidne** rīkjoslā atlasiet **Jauns**, lai pievienotu rindu, un pēc tam iestatiet šādas vērtības:

    - **Darba pasūtījuma tips:** *Pirkšanas pasūtījumi*
    - **Darba veidne:** *61 PP Direct*

1. Darbības rūtī atlasiet **Saglabāt** un pēc tam atlasiet **Rediģēt vaicājumu**.
1. **Klastera izvietošanas** dialoglodziņā cilnē **Diapazons** atlasiet **Pievienot**, lai pievienotu otru rindu vaicājumam. Pēc tam atjauniniet vaicājumu rindas, kā tas ir norādīts tabulā.

    | Tabula | Atveidotā tabula | Lauks | Kritēriji |
    |---|---|---|---|
    | Ir spēkā | Ir spēkā | Noliktava | *61* |
    | Ir spēkā | Ir spēkā | Darba ID | Atstājiet šo lauku tukšu. |

1. Atlasiet **Labi**, lai saglabātu vaicājumu un aizvērtu dialoglodziņu.
1. Darbības rūtī atlasiet **Saglabāt** un aizveriet lapu.

> [!IMPORTANT]
> Klastera profila lauki, kas parādās pelēkoti, kad opcija **Ģenerēt klastera ID** ir iestatīta uz *Jā*, nav pieejami, un netiks ņemti vērā, ja tiek izmantots šis līdzeklis.

### <a name="mobile-device-menu-items"></a>Mobilās ierīces izvēlnes vienumi

Šim līdzeklim ir pieejamas divas jaunas mobilās ierīces izvēlnes vienības. Izvēlnes elements **Saņemt un kārtot klasteri** tiek lietots, lai sakārtotu saņemto krājumu izvietošanas klasterī pēc saņemšanas. Izvēlnes vienums **Klastera izvietošana** tiek izmantots, lai pēc piešķiršanas izvietotu klasteri.

#### <a name="receive-and-sort-cluster"></a>Saņemt un kārtot klasteri

Izveidot jaunu mobilās ierīces izvēlnes elementu krājumu un šķirošanas saņemšanai klasterī. Šis izvēlnes elements izveidos ienākošo darbu pēc krājumu saņemšanas, kas norāda, ka saņemšanas izvēlnes elements tiks izmantots izvietošanas klasteriem.

> [!NOTE]
> Izvēlnes elementu **Saņemt un kārtot klasteri** var izmantot ar šādiem saņemšanas izvēlnes elementiem:
>
> - Pirkšanas pasūtījuma rindas saņemšana
> - Pirkšanas pasūtījuma krājuma saņemšana
> - Kravas krājuma saņemšana

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Darbību rūtī atlasiet **Jauns**.
1. **Galvenes** skatā iestatiet šādas vērtības:

    - **Izvēlnes elementa nosaukums:** *Saņemt un kārtot klasteri*
    - **Virsraksts:** *Saņemt un kārtot klasteri*
    - **Režīms:** *Darbs*
    - **Izmantot esošo darbu:** *Nē*

1. Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:

    - **Darba izveides process:** *Pirkšanas pasūtījuma krājuma saņemšana*
    - **Ģenerēt numura zīmi:** *Jā*
    - **Piešķirt izvietošanas klasteri:** *Jā*

        > [!NOTE]
        > Opcija **Piešķirt izvietošanas klasteri** ir pieejama tikai vienas darbības *Darba izveides procesa* aktivitātes saņemšanai.

    Pieņemiet noklusējuma vērtības atlikušajiem laukiem.

1. Darbību rūtī atlasiet **Saglabāt**.

#### <a name="cluster-putaway"></a>Klastera izvietošana

Izveidot jaunu mobilās ierīces izvēlnes elementu klastera izvietošanai pēc tā piešķiršanas.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Darbību rūtī atlasiet **Jauns**.
1. **Galvenes** skatā iestatiet šādas vērtības:

    - **Izvēlnes vienuma nosaukums:** *Klastera izvietošana*
    - **Virsraksts:** *Klastera izvietošana*
    - **Režīms:** *Darbs*
    - **Izmantot esošo darbu:** *Jā*

1. Kopsavilkuma cilnē **Vispārīgi** iestatiet lauku **Noteicējs:** uz *Klastera izvietošana*. Pieņemiet noklusējuma vērtības atlikušajiem laukiem.
1. Kopsavilkuma cilnē **Darba klases** iestatiet šīs mobilās ierīces izvēlnes vienumam derīgo darba klasi:

    - **Darba klases ID:** *Pirkums*
    - **Darba pasūtījuma tips:** *Pirkšanas pasūtījumi*

1. Darbību rūtī atlasiet **Saglabāt**.

### <a name="mobile-device-menu"></a>Mobilās ierīces izvēlne

Pievienojiet izvēlnes elementus, ko tikko izveidojāt mobilās programmas saņemšanas izvēlnei.

1. Dodieties uz **Noliktavas vadība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlne**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Izvēlnes sarakstā atlasiet **Ienākošie**.
1. Sarakstā **Pieejamās izvēlnes un izvēļņu elementi** atrodiet un atlasiet izvēlnes elementu **Saņemt un kārtot klasteru**.
1. Atlasiet labo bultiņu, lai pārvietotu atlasītās izvēlnes elementu **Izvēlņu struktūras** sarakstā.
1. Izmantojiet pogu uz augšu vai uz leju, lai pārvietotu izvēlnes elementu vēlamajā pozīcijā izvēlnē.
1. Darbību rūtī atlasiet **Saglabāt**.
1. Atkārtojiet soļus no 4. līdz 7., lai pievienotu atlikušos izvēlnes elementus:

    - Piešķirt klasteri
    - Klastera izvietošana

## <a name="example-scenario"></a>Piemērs

Šis scenārijs simulē izvietošanas klastera apstrādi.

### <a name="create-a-purchase-order"></a>Pirkšanas pasūtījuma izveide

1. Dodieties uz **Kreditori \> Pirkšanas pasūtījumi \> Visi pirkšanas pasūtījumi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Izveidot pirkuma pasūtījumu** iestatiet sekojošas vērtības:

    - **Tirgotāja konts:** *1001*
    - **Noliktava:** *61*

1. Atlasiet **Labi**.

    Atveras lapa **Visi pirkšanas pasūtījumi**.

1. Lapā **Visi pirkšanas pasūtījumi**, kas atrodas kopsavilkuma cilnē **Pirkšanas pasūtījuma rindas**, izmantojiet pogu **Pievienot rindu**, lai pievienotu šādas rindas:

    - Pirkšanas pasūtījuma 1. rinda:

        - **Krājuma numurs:** *A0001*
        - **Daudzums:** *10*

    - Pirkšanas pasūtījuma 2. rinda:

        - **Krājuma numurs:** *A0002*
        - **Daudzums:** *20*

    - Pirkšanas pasūtījuma 3. rinda:

        - **Krājuma numurs:** *M9215*
        - **Daudzums:** *30*

1. Darbību rūtī atlasiet **Saglabāt**.
1. Pierakstiet pirkuma pasūtījuma numuru.

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a>Saņemt krājumu un nodot to tālāk prom no mobilās ierīces

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a>Saņemt un kārtot krājumus klasterī

1. Pierakstieties noliktavas lietotnē kā lietotājs, kurš ir iespējots noliktavā *61*.
1. Galvenajā izvēlnē atlasiet **Ienākošs**.
1. Izvēlnē **Ienākošie** atlasiet **Saņemt un kārtot klasteri**.
1. Laukā **Ponum** ievadiet savu pirkuma pasūtījuma numuru.
1. Atlasiet pogu **Labi** (atzīmes poga).
1. Atlasiet lauku **Krājums**, ievadiet krājuma numuru *A0001* un atlasiet **Labi**.
1. Atlasiet lauku **Daudzums**, ievadiet *10*, izmantojot ciparu tastatūru, un pēc tam atlasiet izvēles rūtiņas pogu.
1. Uzdevumu lapā **Daudzums** atlasiet **Labi** (izvēles rūtiņas poga), lai apstiprinātu ievadīto daudzumu.
1. Uzdevumu lapā **Krājums** atlasiet **Labi**, lai apstiprinātu, ka krājums *A0001* tika ievadīts .
1. Atlasiet lauku **Klastera ID** un ievadiet vērtību, lai piešķirtu izveidoto klastera ID.

    Šeit ievadītais ID tiks izmantots, kad tiek saņemti divi atlikušie pirkšanas pasūtījuma krājumi.

1. Atlasiet **Labi**.

    Parādās uzdevumu lapa **Ponum** un parādīts ziņojums "Darbs pabeigts".

    Krājums *A0001* tagad ir saņemts *RECV* atrašanās vietā un piešķirts klastera ID, ko ievadījāt 10. solī.

1. Atkārtojiet 4. – 11. soli, lai saņemtu atlikušos divus krājumus no pirkšanas pasūtījuma, un piešķiriet tiem klastera ID:

    - Preces *A0002* daudzums *20*
    - Preces *M9215* daudzums *30*

#### <a name="close-the-cluster"></a>Aizvērt klasteri

Pirms krājumu var izvietot klasterī, klasteris ir jāslēdz.

1. Supply Chain Management dodieties uz **Noliktavas pārvaldība \> Darbs \> Izejošie \> Darba klasteri**.
1. Lapā **Darba klasteri** sadaļā **Darba klasteris** meklējiet lauku **Klastera ID**, ko ievadījāt iepriekš.
1. Ja klasteris netiek norādīts, iespējams, tas jau ir slēgts. Lai noteiktu, vai klasteris tika slēgts, atzīmējiet izvēles rūtiņu **Rādīt slēgto darbu** un meklējiet klastera ID, ko ievadījāt iepriekš. Pēc tam izpildiet kādu no norādītajām darbībām.

    - Ja klasteris ir slēgts, izlaidiet atlikušos šīs procedūras soļus un pārejiet uz nākamo procedūru [Novietot klasteri tālāk](#put-the-cluster-away).
    - Ja klasteris nav slēgts, izpildiet atlikušos šīs procedūras soļus, lai manuāli aizvērtu klasteri. Tad pārejiet uz nākamo darbību.

1. Sadaļā **Darba klasteris** atlasiet klastera ID, ko ievadījāt iepriekš.
1. Darbību rūtī atlasiet **Slēgt klasteri**.

    Pēc klastera slēgšanas tas vairs netiek parādīts sadaļā **Darba klasteris** (ja vien nav atzīmētā izvēles rūtiņa **Parādīt slēgto darbu**).

#### <a name="put-the-cluster-away"></a>Klastera izvietošana

1. Pierakstieties noliktavas lietotnē kā lietotājs, kurš ir iespējots noliktavā *61*.
1. Galvenajā izvēlnē atlasiet **Ienākošs**.
1. Izvēlnē **Ienākošie** atlasiet **Klastera izvietošana**.
1. Atlasiet **Klastera ID** un ievadiet klastera ID, ko iepriekš ievadījāt slēgtajam klasterim.
1. Atlasiet **Labi**.

    Tiek parādīta lapa **Klastera izvietošana: Izdot**. Tas rāda klastera ID, izdošanas vietu, krājumus (tiks rādītas *Vairākas* vērtības) un kopējo daudzumu klasterī, kas ir jāizdod.

1. Atlasiet **Labi**.

    Tiek parādīta lapa **Klastera izvietošana: Izvietot**. **Izvietot** instrukcijās tiek identificēts klastera ID, novietojums, krājumi, kopējais daudzums un numura zīmes ID krājumiem, kas saņemti klasterī.

    Ir standarta opcijas, lai ignorētu vai izpildītu šo darbību.

    ![Klastera izvietošana: izvietot lapu](media/Cluster_putaway-Put.png "Klastera izvietošana: izvietot lapu")

1. Atlasiet **Labi**, lai apstiprinātu klastera izvietošanu.

    Tiek parādīts ziņojums "Klasteris pabeigts".

## <a name="notes-and-tips"></a>Piezīmes un padomi

Gadījumos, kad klastera ID ir kļuvis par pamatnumura zīmi ligzdotai paletei, novietošanas pozīcija tiek norādīta automātiski, kad tiek skenēts klastera ID. Neviena papildu numura zīme nedrīkst tikt skenēta, pat ja numura zīmes ģenerēšana ir iestatīta uz manuālu.
