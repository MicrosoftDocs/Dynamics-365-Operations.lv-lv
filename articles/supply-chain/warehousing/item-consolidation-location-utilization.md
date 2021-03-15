---
title: Krājuma konsolidācija – novietojuma izmantojums
description: Šajā tēmā ir sniegta informācija par funkcionalitāti, kas noliktavu pārvaldniekiem atvieglo iespēju skatīt un filtrēt noliktavas novietojumu tilpuma izmantojumu. Pārvaldnieki var atlasīt novietojumus un izveidot krājumu pārvietošanas darbu tieši no lapas Krājuma konsolidācija, lai konsolidētu krājumus, un tādējādi labāk izmantotu noliktavas telpu.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6edabc51981d8935672b44e53b453cfbaca9031b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004656"
---
# <a name="item-consolidation---location-utilization"></a>Krājuma konsolidācija – novietojuma izmantojums

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par funkcionalitāti, kas noliktavu pārvaldniekiem atvieglo iespēju skatīt un filtrēt noliktavas novietojumu tilpuma izmantojumu. Pārvaldnieki var atlasīt novietojumus un izveidot krājumu pārvietošanas darbu tieši no lapas **Krājuma konsolidācija**, lai konsolidētu krājumus, un tādējādi labāk izmantotu noliktavas telpu.

## <a name="turn-on-the-features"></a>Līdzekļu ieslēgšana

Lai varētu izmantot šajā tēmā aprakstītos līdzekļus, tie ir jāieslēdz jūsu sistēmā. Administratori var izmantot darbvietu [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai pārbaudītu līdzekļu statusu un tos ieslēgtu, ja tas nepieciešams. Ieslēdziet abus šos līdzekļus, tādā secībā, kādā tie ir norādīti. (Abi līdzekļi ir paredzēti modulim **Noliktavas pārvaldība**.)

1. Noliktavas vietas statuss
2. Krājumu konsolidācijas novietojuma utilizācija

## <a name="warehouse-location-status"></a>Noliktavas vietas statuss

Līdzeklis *Noliktavas novietojuma statuss* pievieno četrus jaunus laukus lapai **Novietojumi**, lai izsekotu papildu informācijai par pašreizējo novietojuma stāvokli:

- **Krājuma numurs** — pašlaik novietojumā esošais krājums. Ja novietojumā ir vairāki krājumi, šis lauks būs tukšs.
- **Pēdējās aktivitātes datums un laiks** — pēdējā noliktavas darījuma laikspiedols, kas tika veikts saistībā ar novietojumu.
- **Vecumstruktūras datums** — datums, kad noliktavā tika ievietots krājums novietojumā. Datums tiek aprēķināts, pamatojoties uz noliktavas vienības vecumstruktūras datumu. Lai arī šis datums ir precīzs novietojumiem, kurus var izsekot pēc noliktavas vienības, tas var nebūt precīzs novietojumiem, kurus nevar izsekot pēc noliktavas vienības.
- **Novietojuma statuss** — novietojuma statuss. Ir pieejamas četras vērtības:

    - **Nav noteikts** – novietojuma profils neizseko statusu. Tāpēc pašreizējais statuss ir nezināms.
    - **Tukšs**– novietojumā pašlaik nav neviena krājuma.
    - **Izdošana** – izejošās darbības ir veiktas attiecībā pret novietojumu, kopš tas pēdējoreiz bija tukšs.
    - **Glabāšana** – ir veiktas tikai ienākošās transakcijas, jo pēdējoreiz novietojums bija tukšs.

Šie lauki sniedz noliktavas pārvaldniekiem iespēju iegūt labāku pārskatu par noliktavas novietojumu statusu. Tāpat tie ļauj veikt detalizētāku pārskatu veidošanu un filtrēšanu.

## <a name="set-up-item-consolidation-and-location-utilization"></a>Krājuma konsolidācijas un novietojuma izmantojuma iestatīšana

Šajā sadaļā ir aprakstīts, kā sagatavot sistēmu, lai izmantotu krājuma konsolidāciju un novietojuma izmantojumu. Procedūrās tiek izmantoti vērtību paraugi no standarta demonstrācijas datiem. Ja plānojat strādāt ar scenārija piemēru, kas ir sniegts tālāk šajā tēmā, atlasiet **USMF** juridisko personu (kurā ir standarta demonstrācijas dati) un izveidojiet katru šajā sadaļā aprakstīto ierakstu. Ja neplānojat strādāt ar scenārija piemēru, šeit sniegtās vērtības var uzskatīt par tādu iestatīšanas veidu piemēriem, kas ir jāpabeidz, lai izmantotu līdzekļus.

### <a name="released-product"></a>Izlaistā prece

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Laukā **Krājuma kods** atlasiet *M9201* un atveriet informācijas lapu.
1. Darbību rūtī cilnes **Pārvaldīt krājumus** grupā **Noliktava** atlasiet **Fiziskās dimensijas**.
1. Lapā **Fiziskās dimensijas** darbību rūtī atlasiet **Jauns**.

    Režģim tiek pievienota jauna rinda. Lauks **Krājuma kods** ir priekšiestatīts.

1. Laukā **Vienība** atlasiet *katra*. Atlikušie rindas lauki tiek iestatīti automātiski.
1. Atlasiet **Saglabāt** un aizveriet lapu.

### <a name="location-profile"></a>Novietojuma profils

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Novietojuma profili**.
1. Novietojuma profilu sarakstā atlasiet **FLOOR-05**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Kopsavilkuma cilnē **Vispārīgi** pārliecinieties, vai abas šīs opcijas ir iestatītas uz *Jā*:

    - Iespējot krājumu vietā
    - Iespējot vietas statusu

1. Atlasiet **Saglabāt**.

    > [!IMPORTANT]
    > Ja opcijas **Iespējot krājumu novietojumā** un **Iespējot novietojuma statusu** jau ir iestatītas uz *Jā*, pārejiet pie instrukciju 10. darbības, lai iestatītu kopsavilkuma cilni **Dimensijas**. Ja opcijas jau nav iestatītas uz *Jā*, tad pēc to manuālas iestatīšanas, palaidiet konsekvences pārbaudi modulim **Noliktavas pārvaldība**. Šādā gadījumā turpiniet ar nākamo darbību.

1. Lai palaistu konsekvences pārbaudi, dodieties uz **Sistēmas administrēšana \> Periodiskie uzdevumi \> Datu bāze \> Konsekvences pārbaude**.
1. Dialoglodziņā **Konsekvences pārbaude** iestatiet šādas vērtības:

    - **Modulis:** *Noliktavas pārvaldība*
    - **Pārbaudīt/Labot:** *Pārbaudīt*
    - **No datuma:** atstājiet šo lauku tukšu.
    - **Noliktavas novietojuma statusa konsekvences pārbaude:** atzīmējiet šo izvēles rūtiņu.

1. Atlasiet **Labi**.

    > [!TIP]
    > Kad konsekvences pārbaude ir pabeigta, tiek saņemts paziņojums. Atveriet [darbību centru](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications), lai skatītu ziņojumu. Atlasiet **Ziņojuma informācija**, lai skatītu informāciju.
    >
    > Ja konsekvences pārbaudes ziņojums norāda, “Novietojumam XXXX konstatēta nepareiza novietojuma statusa informācija noliktavā XX”, konsekvences pārbaude ir jāpalaiž vēlreiz. Šoreiz lauku **Pārbaudīt/Labot** iestatiet uz *Labot kļūdu*. Skatiet ziņojumus, lai pārliecinātos, vai nav atrastas kļūdas.

1. Pabeidziet novietojuma profila iestatīšanu. Atgriezieties sadaļā **Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Novietojuma profili**, atlasiet novietojuma profilu **FLOOR-05**, un pēc tam darbību rūtī atlasiet **Rediģēt**.
1. Kopsavilkuma cilnē **Dimensijas** iestatiet šādas vērtības:

    - **Tilpuma izmantojuma procentuālā vērtība:** *100*
    - **Krājumu novietojumam izmantotā tilpuma metode:** *izmantot novietojumu tilpumu*
    - **Faktiskais novietojuma augstums:** *10*
    - **Faktiskais novietojuma platums:** *10*
    - **Faktiskais novietojuma dziļums:** *10*
    - **Maksimālais svars:** *100*

1. Atlasiet **Saglabāt**.

### <a name="mobile-device-menu-items"></a>Mobilās ierīces izvēlnes vienumi

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Darbību rūtī atlasiet **Jauns**, lai izveidotu kārtošanas izvēlnes elementu.
1. Galvenē iestatiet šādas vērtības:

    - **Izvēlnes elementa nosaukums:** *Koriģēt ienākošo*
    - **Nosaukums:** *Koriģēt ienākošo*
    - **Režīms:** *Darbs*
    - **Izmantot esošo darbu:** *Nē*

1. Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:

    - **Darba izveides process:** *Ienākošā korekcija*
    - **Krājumu korekciju veidi:** *Koriģēt ienākošo*

1. Atlasiet **Saglabāt**.

### <a name="mobile-device-menu"></a>Mobilās ierīces izvēlne

1. Dodieties uz **Noliktavas vadība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlne**.
1. Izvēļņu sarakstā atlasiet **Krājumi**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Sarakstā **Pieejamās izvēlnes un izvēļņu elementi** atrodiet un atlasiet izvēlnes elementu **Koriģēt ienākošo**.
1. Atlasiet bultiņas pa labi pogu, lai pārvietotu **Koriģēt ienākošo** uz sarakstu **Izvēlnes struktūra**. Šādā veidā jūs pievienojat jauno izvēlnes elementu atlasītajai izvēlnei.
1. Atlasiet **Saglabāt**.

### <a name="movement-types"></a>Kustības veidi

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Krājumi \> Kustības veidi**.
1. Darbību rūtī atlasiet **Jauns**, un pēc tam iestatiet šādas vērtības:

    - **Kustības veida kods:** *CONSOLIDATE*
    - **Apraksts:** *Novietojumu konsolidēšana*
    - **Darba klases ID:** *InvMov*

1. Atlasiet **Saglabāt**.

## <a name="example-scenario"></a>Piemēra situācija

Šajā scenārijā tiek izmantota noliktavas programma mobilajā ierīcē, lai veiktu krājumu *ienākošo korekciju* diviem noliktavas novietojumiem.

### <a name="add-inventory-to-locations"></a>Krājumu pievienošana novietojumiem

1. Piesakieties mobilajā ierīcē kā lietotājs, kurš ir iestatīts noliktavai *51*.
1. Dodieties uz **Krājumi \> Koriģēt ienākošo**.

    Tagad ievadiet pirmā novietojuma korekciju.

1. Uzdevumā **Ienākošā korekcija** atlasiet novietojumu, kuram veikt krājumu korekciju. Laukā **LOC** atlasiet *LP-001*.
1. Apstipriniet novietojumu.
1. Izveidojiet noliktavas vienības ID krājumam, kas tiks pievienots novietojumam. Laukā **LP** ievadiet *LP00101*.
1. Apstipriniet noliktavas vienību.
1. Ievadiet krājumu, kas tiks pievienots noliktavas vienībai. Laukā **ITEM** ievadiet *M9201*.
1. Apstipriniet krājumu.
1. Ievadiet krājuma daudzumu, kas tiks pievienots. Laukā **QTY** ievadiet *10*.
1. Apstipriniet daudzumu.

    Tiek saņemts ziņojums "Darbība pabeigta". Tagad ievadiet otrā novietojuma korekciju.

1. Uzdevumā **Ienākošā korekcija** atlasiet novietojumu, kuram veikt krājumu korekciju. Laukā **LOC** atlasiet *LP-002*.
1. Apstipriniet novietojumu.
1. Izveidojiet noliktavas vienības ID krājumam, kas tiks pievienots novietojumam. Laukā **LP** ievadiet *LP00201*.
1. Apstipriniet noliktavas vienību.
1. Ievadiet krājumu, kas tiks pievienots noliktavas vienībai. Laukā **ITEM** ievadiet *M9201*.
1. Apstipriniet krājumu.
1. Ievadiet krājuma daudzumu, kas tiks pievienots. Laukā **QTY** ievadiet *15*.
1. Apstipriniet daudzumu.

    Tiek saņemts ziņojums "Darbība pabeigta".

1. Atlasiet pogu Izvēlne (dažreiz saukta par hamburgeru vai hamburgera pogu) un pēc tam atlasiet **Atcelt**, lai izietu no uzdevuma **Ienākošā korekcija**.

### <a name="consolidate-locations"></a>Novietojumu konsolidēšana

1. Dodieties uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Krājuma konsolidācija**.
1. Galvenē atlasiet noliktavu, kurai veikt konsolidēšanu. Laukā **Noliktava** ievadiet *51*.

    Katram novietojumam, kurā tika koriģēts krājums *M9201*, tiek parādīts ieraksts. Kolonna **Izmantojuma procentuālā vērtība** rāda tilpuma izmantojumu katram novietojumam.

1. Lai konsolidētu krājumus, atlasiet visus konsolidējamos novietojumus, un pēc tam darbību rūtī atlasiet **Krājumu konsolidēšana**.
1. Dialoglodziņā **Krājumu konsolidēšana** norādiet novietojumu un kustības veidu, kas jāizmanto, lai izveidotu krājumu pārvietošanas darbu. Iestatiet šādas vērtības:

    - **Novietojums:** *LP-001*
    - **Kustības veida kods:** *CONSOLIDATE*

1. Atlasiet **Labi**.
1. Tiks saņemts informatīvs ziņojums, kurā norādīts izveidotais pārvietošanas darbs. Pierakstiet pārvietošanas darba ID.

### <a name="view-movement-work"></a>Pārvietošanas darba skatīšana

1. Dodieties uz **Noliktavas pārvaldība \> Darbs \> Darba informācija**.
1. Skatiet izveidoto darbu. Izmantojiet pārvietošanas darba ID no krājumu konsolidācijas, lai filtrētu vai meklētu darbu režģī.

    Šajā scenārijā esošs novietojums, kurā bija krājumi, tika izmantots kā krājumu konsolidācijas novietojums. Tādēļ tika izveidots tikai viens darba ID.

    > [!NOTE]
   > Sistēma izveido vienu darba ID katrai kustībai, kas ir jāpabeidz. Ja norādāt novietojumu, kurā jau ir krājumi, tiek izveidots tikai viens darba ID. Ja norādāt jaunu novietojumu, tiek izveidoti divi darba ID.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]