---
title: Pārsūtīšanas pasūtījumu izveide no noliktavas programmas
description: Šajā rakstā ir aprakstīts, kā izveidot un apstrādāt pārsūtīšanas pasūtījumus no mobilās programmas Noliktavas pārvaldība
author: perlynne
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: b9edc2d94aa1f4850d2e7fe2b4bdd1b092be944f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877455"
---
# <a name="create-transfer-orders-from-the-warehouse-app"></a>Pārsūtīšanas pasūtījumu izveide no noliktavas programmas

[!include [banner](../includes/banner.md)]

Šis līdzeklis ļauj noliktavas darbiniekiem izveidot un apstrādāt pārsūtīšanas pasūtījumus tieši no Warehouse Management mobile programmas. Vispirms darbinieks atlasa mērķa noliktavu un pēc tam viņi var skenēt vienu vai vairākas noliktavas vienības, izmantojot programmu, lai pievienotu noliktavas vienības pārsūtīšanas pasūtījumam. Kad noliktavas darbinieks atlasa **Pabeigt pasūtījumu**, pakešuzdevums izveido nepieciešamo pārsūtīšanas pasūtījumu un pasūtījuma rindas, pamatojoties uz rīcībā esošajiem krājumiem, kas reģistrēti šīm noliktavas vienībām.

## <a name="turn-this-feature-on-or-off"></a><a name="enable-create-transfer-order-from-warehouse-app"></a> Ieslēgt vai izslēgt šo līdzekli

Lai varētu izmantot šo līdzekli, sistēmā vispirms ir jāiespējo gan pats līdzeklis, gan tā priekšnosacījumi. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lapu, lai pārbaudītu līdzekļa statusu un iespējotu to pēc nepieciešamības.

1. Iespējojiet tālāk norādītās divas funkcijas (šādā secībā), kas atrodas līdzekļu [pārvaldības darbvietā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). No Piegādes ķēdes pārvaldības versijas 10.0.25 abi šie līdzekļi ir ieslēgti pēc noklusējuma.
    1. *Apstrādāt noliktavas programmas notikumus*
    1. *Izveidot un apstrādāt pārsūtīšanas pasūtījumus no noliktavas programmas*
1. Lai automatizētu izejošo sūtījumu apstrādi, [ir jāiespējo arī funkcija Apstiprināt nosūtīšanas kravas no pakešuzdevumiem](confirm-outbound-shipments-from-batch-jobs.md).

## <a name="set-up-a-mobile-device-menu-item-to-create-transfer-orders"></a><a name="setup-warehouse-app-menu"></a>Iestatīt mobilās ierīces izvēlnes vienumu, lai veidotu pārsūtīšanas pasūtījumus

Šeit atrodamas vispārīgās vadlīnijas mobilās ierīces izvēlnes vienuma iestatīšanai, lai veidotu pārsūtīšanas pasūtījumu. Atkarībā no jūsu uzņēmējdarbības prasībām automatizēšanas līmeņa iestatīšanai, kad lietotāji izveido pārsūtīšanas pasūtījumus no ražotnes, tiks iespējotas dažādas konfigurācijas. Šī dokumenta scenārijā tiks aprakstīta viena šāda konfigurācija.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Atlasiet **Jauns**, lai pievienotu jaunu izvēlnes vienumu. Pēc tam veiciet šādus iestatījumus, lai sāktu darbu:

    - **Izvēlnes vienuma nosaukums** – piešķiriet nosaukumu, kas tiks parādīts Supply Chain Management.
    - **Nosaukums** – piešķiriet izvēlnes nosaukumu, kas jāuzrāda darbiniekiem Warehouse Management mobile programmā.
    - **Režīms** – iestatīts uz *Netiešs* (šis izvēlnes elements neveidos darbu).
    - **Aktivitātes kods** – iestatīts uz *Izveidot pārsūtīšanas pasūtījumu no noliktavas vienībām*, lai ļautu noliktavas darbiniekiem veidot pārsūtīšanas pasūtījumu, pamatojoties uz vienu vai vairākām skenētām noliktavas vienībām.

1. Izmantojiet iestatījumu **Pārsūtīšanas pasūtījuma rindas izveides politika**, lai kontrolētu, kā pārsūtīšanas pasūtījuma rindas tiks veidotas ar šo izvēlnes vienumu. Rindas tiks veidotas/atjauninātas, pamatojoties uz rīcībā esošajiem krājumiem, kas reģistrēti skenētajām noliktavas vienībām. Izvēlieties vienu no šīm vērtībām:

    - **Bez rezervēšanas** – pārsūtīšanas pasūtījuma rindas netiks rezervētas.
    - **Noliktavas vienību vadība ar rindas rezervāciju** – pārsūtīšanas pasūtījuma rindas tiks rezervētas un izmantos noliktavas vienību vadības stratēģijas opciju, kas glabā ar pasūtījuma rindām attiecīgi saistītos noliktavas vienību ID. Tāpēc novietoto noliktavas vienību ID vērtības var izmantot kā pārsūtīšanas pasūtījuma rindu darba izveides procesa daļu.

1. Izmantojiet iestatījumu **Izejošā sūtījuma politika**, lai pēc nepieciešamības pievienotu papildu automatizēšanu izejošā pārsūtīšanas pasūtījuma nosūtīšanas procesam. Kad darbinieks atlasa pogu **Pabeigt pasūtījumu**, programma izveido *Pabeigt pasūtījumu* noliktavas programmas notikumu, kas saglabā lauka **Izejošā sūtījuma politika** šeit izvēlēto vērtību katrai rindai pašreizējā pārsūtīšanas pasūtījumā. Vēlāk, kad notikumu rinda tiek apstrādāta, izmantojot pakešuzdevumu, lai izveidotu pārsūtīšanas pasūtījumu, pakešuzdevums var nolasīt šajā laukā saglabāto vērtību un tādējādi kontrolēt, kā šis darbs apstrādā katru rindu. Izvēlieties vienu no šīm:

    - **Nav** — automatizēta apstrāde netiek veikta.
    - **Izdot noliktavai** – automatizē izdošanu noliktavā.
    - **Nosūtīšanas apstiprinājums** – automatizē nosūtīšanas apstiprināšanu.
    - **Izdošanas un nosūtīšanas apstiprinājums** — automatizē gan izdošanu noliktavā, gan nosūtīšanas apstiprināšanu.

## <a name="add-the-mobile-device-menu-item-to-a-menu"></a>Mobilās ierīces izvēlnes vienuma pievienošana izvēlnei

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlne**
1. Atlasiet **Rediģēt**.
1. Atlasiet esošu izvēlni, izvēloties jauno izvēlnes vienumu sadaļā **Pieejamās izvēlnes un izvēļņu vienumi**. Pievienojiet izvēlnes vienumu, atlasot bultiņas pa labi pogu.

## <a name="create-a-transfer-order-based-on-license-plates"></a>Pārsūtīšanas pasūtījuma izveide, pamatojoties uz noliktavas vienībām

Warehouse Management mobile programmā ir vienkāršs pārsūtīšanas pasūtījumu izveides process, kas pamatots uz noliktavas vienībām. Lai to paveiktu, darbinieks veic šādas darbības, izmantojot Warehouse Management mobile programmu:

1. Izveidojiet pārsūtīšanas pasūtījumu un norādiet mērķa noliktavu.
1. Norādiet katru nosūtāmo noliktavas vienību.
1. Atlasiet **Pabeigt pasūtījumu**.

>[!NOTE]
> Vairākiem darbiniekiem ir iespējams piešķirt noliktavas vienības, kas paredzētas vienam pārsūtīšanas pasūtījumam, izmantojot pogu **Atlasīt pārsūtīšanas pasūtījumu**, lai atlasītu esošu, neapstrādātu, pārsūtīšanas pasūtījuma numuru no noliktavas programmas notikumu rindas. Informāciju par to, kā atrast pārsūtīšanas pasūtījuma numura vērtības, skatiet sadaļā [Uzziņas par noliktavas programmas notikumiem](#inquire-the-warehouse-app-events).

## <a name="example-scenario"></a>Piemērs

Šis scenārijs sniedz pārskatu par pārsūtīšanas pasūtījumu izveides un automātiskas apstrādes procesu, pamatojoties uz rīcībā esošajiem krājumiem, kas reģistrēti atlasītajās noliktavas vienībās.

Lai ar šo scenāriju strādātu, izmantojot ieteiktās vērtības, ir jāstrādā ar sistēmu, kurā ir instalēti demonstrācijas dati, un pirms sākat, atlasiet *USMF* juridisko personu.

Šajā scenārijā tiek pieņemts, ka jau esat iespējojis gan [izveidot un apstrādāt pārsūtīšanas pasūtījumus no noliktavas programmas līdzekļa](#enable-create-transfer-order-from-warehouse-app), gan [noliktavas programmas notikumu apstrādes](warehouse-app-events.md) iespēju.

Papildus pārsūtīšanas pasūtījuma izveidei mobilās ierīces izvēlnes vienumos ir jāiestata un jāiespējo arī papildu veidnes, novietojuma direktīvas un pakešuzdevumi.

### <a name="example-scenario-blueprint"></a>Piemēra plāns

Jūs esat mazumtirgotājs un jums ir vairākas noliktavas vienības, katra no tām satur krājumu kopumu, kas novietots noteiktā vietā vienā no jūsu noliktavām (*Noliktava 51*). Jūs vēlaties iespējot procesu, kas ļauj darbiniekiem izveidot pārsūtīšanas pasūtījumu uz citu noliktavu (*Noliktava 61*), jau skenētajam noliktavas vienību kopumam. Pārsūtīšanas pasūtījums tiks automātiski nosūtīts–atjaunināts, tiklīdz būs norādīta pasūtījuma pēdējā noliktavas vienība.

![Automātiska pārsūtīšanas pasūtījuma procesa piemērs.](media/create-transfer-order-from-app-example.png "Automātiska pārsūtīšanas pasūtījuma procesa piemērs")

### <a name="create-a-mobile-device-menu-item-for-creating-transfer-orders"></a>Izveidot mobilās ierīces izvēlnes vienumu, lai veidotu pārsūtīšanas pasūtījumus

Šajā sadaļā ir paskaidrots, kā izveidot jaunu mobilās ierīces izvēlnes vienumu pārsūtīšanas pasūtījumu izveidei. Iestatiet **Režīms** uz *Netiešs* un **Aktivitātes kods** uz *Izveidot pārsūtīšanas pasūtījumu no noliktavas vienībām*.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Atlasiet **Jauns**.
1. Laukā **Izvēlnes vienuma nosaukums** ievadiet nosaukumu *Izveidot*.
1. Laukā **Nosaukums** ievadiet aprakstu *Izveidot*.
1. Laukā **Režīms** atlasiet *Netiešs*.
1. Laukā **Aktivitātes kods** atlasiet *Izveidot pārsūtīšanas pasūtījumu no noliktavas vienībām*.
1. Laukā **Pasūtījuma rindas izveides politika** atlasiet *Noliktavas vienību vadība ar rindas rezervāciju*.
1. Laukā **Izejošā sūtījuma politika** atlasiet *Izdošanas un nosūtīšanas apstiprinājums*.
1. Dodieties uz **Noliktavas vadība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlne**.
1. Atlasiet **Rediģēt**.
1. Atlasiet esošu izvēlni **Krājumi**, un pēc tam atlasiet jauno izvēlnes vienumu sadaļā **Pieejamās izvēlnes un izvēļņu vienumi**. Pievienojiet izvēlnes vienumu izvēlnei **Krājumi**, atlasot bultiņas pa labi pogu.

### <a name="set-up-work-templates-to-auto-process-and-break-work-by-located-license-plate"></a>Darba veidņu iestatīšana automātiskai apstrādei un darba sadalei, izmantojot novietoto noliktavas vienību

Šajā sadaļā ir paskaidrots, kā iespējot darba veidni automātiskai darba apstrādei, kas izveidots kopuma izdošanas laikā, izmantojot veidni.

1. Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba veidnes**.
1. Laukā **Darba pasūtījuma veids** atlasiet *Pārsūtīt izejas plūsmu*.
1. Atlasiet **Jauns**, lai izveidotu jaunu darba veidni.
1. Laukā **Darba veidne** ievadiet *LP automātiska apstrāde 51. noliktavā*.
1. Laukā **Darba veidnes apraksts** ievadiet *LP automātiska apstrāde 51. noliktavā*.
1. Atzīmējiet izvēles rūtiņu **Automātiski apstrādāt**. Tā ir jāatlasa, lai varētu apstrādāt visas automatizēšanas darbības.
1. Demonstrācijas datos jau pastāv darba veidne *51 pārsūtīšana*, rediģējiet lauku **Secības numurs**, lai jaunajai darba veidnei būtu zemāks secības numurs nekā esošajai darba veidnei *51 pārsūtīšana*.
1. Atlasiet **Saglabāt**, lai rīkjoslā iespējotu kopsavilkuma cilni **Darba veidnes informācija**.
1. Kopsavilkuma cilnē **Darba veidnes informācija** rīkjoslā atlasiet **Jauns**. Tiks pievienotas divas rindas.
1. Laukā **Darba tips atlasiet** vienumu *Izdošana*.
1. Laukā **Darba klases ID** atlasiet *TransfOut*.
1. Rīkjoslā **Darba veidnes informācija** atlasiet **Jauns**.
1. Laukā **Darba veids** atlasiet *Izvietot*.
1. Laukā **Darba klases ID** atlasiet *TransfOut*.
1. Atlasiet **Saglabāt**, lai iespējotu lauku **Direktīvas kods**.
1. Lauka **Darba veids** rindā *Izvietot*, atlasiet **Direktīvas kods** *Angāra durvis*. Pārliecinieties, vai šī jaunā darba veidne ir ar viszemāko **Secības numuru**.
1. Rīkjoslā atlasiet **Rediģēt vaicājumu**, lai atvērtu vaicājumu redaktoru.
1. Cilnē **Diapazons** atlasiet **Pievienot**.
1. Pievienotās rindas laukā **Lauks** atlasiet *Noliktava*.
1. Laukā **Kritēriji** atlasiet *51*.
1. Atlasiet cilni **Kārtošana**.
1. Atlasiet **Pievienot** un iestatiet **Lauks** uz *Novietoto noliktavas vienību ID*. Atlasot šo lauku, tiks iespējota rīkjoslas poga **Darba galvenes pārtraukumi**.
1. Atlasiet **Labi**, pēc tam **Jā**, lai atiestatītu grupēšanu un atgrieztos lapā **Darba veidnes**.
1. Atlasiet **Darba galvenes pārtraukumi** un iespējojiet **Grupēt pēc šī lauka**, lai izmantotu **Novietoto noliktavas vienību ID** un aizveriet.

> [!NOTE]
> Ne visus iestatījumus var apstrādāt automātiski, piemēram, krājumu pieļaujamais svars un jauktu izsekošanas dimensiju izmantošana.

### <a name="set-up-location-directives-for-the-license-plate-guided-strategy"></a>Iestatīt novietojuma direktīvas noliktavas vienību vadības stratēģijai

Šajā sadaļā ir paskaidrots, kā iestatīt novietojuma direktīvas izdošanas procesu, lai izmantotu stratēģiju **Noliktavas vienību vadība**.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Novietojuma direktīvas**.
1. Atlasiet **Rediģēt**.
1. Navigācijas saraksta galvenē atlasiet **Darba pasūtījuma veids** *Pārsūtīt izejas plūsmu*.
1. Navigācijas sarakstā atlasiet esošo novietojuma direktīvu **51 izdot**.
1. Kopsavilkuma cilnē **Rindas** atzīmējiet izvēles rūtiņu **Atļaut sadali**.
1. Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Jauns**, lai pievienotu darbības rindu.
1. Laukā **Nosaukums** ievadiet *LP vadība*.
1. Laukā **Stratēģija** atlasiet *Noliktavas vienību vadība*. Šai darbībai ir nepieciešams zemākais secības numurs.
1. Rīkjoslā atlasiet **Saglabāt**.
1. Rīkjoslā atlasiet ikonu **Atsvaidzināt** lapu.
1. Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet rindu *TOPick*.
1. Rīkjoslā **Novietojuma direktīvas darbības** atlasiet **Pārvietot uz leju**, lai mainītu secības numuru uz lielāku par tikko izveidotās darbības *LP vadība* secības numuru.

> [!NOTE]
> Noliktavas vienību vadības stratēģija mēģinās rezervēt un izveidot izdošanas darbu novietojumos, kur tiek glabātas pieprasītās noliktavas vienības, kas ir saistītas ar pārsūtīšanas pasūtījuma rindām. Bet, ja tas nav iespējams, un jūs joprojām vēlaties izveidot izdošanas darbu, jums vajadzētu atgriezties pie citas novietojuma direktīvas darbības stratēģijas un, iespējams, arī meklēt krājumus citā noliktavas zonā, atkarībā no jūsu biznesa procesa vajadzībām.

### <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Iestatiet pakešuzdevumu, lai apstrādātu noliktavas programmas notikumus

Šajā sadaļā ir paskaidrots, kā iestatīt ieplānotu pakešuzdevumu, lai apstrādātu noliktavas programmas notikumus.

1. Dodieties uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Apstrādāt noliktavas programmas notikumus**.
2. Dialoglodziņā iespējojiet **Pakešapstrāde**, kas atrodas zem sadaļas **Palaist fonā**.
3. Atlasiet **Periodiskums** un iestatiet pakešuzdevumu apstrādei, pamatojoties uz jūsu biznesam nepieciešamo intervālu.
4. Atlasiet **Labi**, lai atgrieztos galvenajā dialoglodziņā.
5. Galvenajā dialoglodziņā atlasiet **Labi**, lai pievienotu darbu pakešuzdevumu rindai.

### <a name="set-up-a-batch-job-to-release-transfer-orders-automatically"></a>Pakešuzdevuma iestatīšana pārsūtīšanas pasūtījumu automātiskai izdošanai

Šajā sadaļā ir paskaidrots, kā iestatīt ieplānotu pakešuzdevumu, lai izdotu pārsūtīšanas pasūtījumus, kas ir atzīmēti kā “gatavi izdošanai”.

1. Doties uz **Noliktavas pārvaldība \> Izdot noliktavai \> Automātiska pārsūtīšanas pasūtījumu izdošana**.
1. Dialoglodziņā izvērsiet sadaļu **Iekļaujamie ieraksti**.
1. Atlasiet **Filtrs**, kas atrodas zem sadaļas **Iekļaujamie ieraksti**.
1. Vaicājumu lapas **WHSTransferAutoRTWQuery** cilnē **Diapazons** atlasiet **Pievienot**, lai vaicājumam pievienotu jaunu rindu.
1. Jaunās rindas laukā **Tabula** atlasiet nolaižamo izvēlni un atlasiet tabulu **Pārsūtīšanas rindas izdošana noliktavai**.
1. Nolaižamās izvēlnes laukā **Lauks** atlasiet **Izejošā sūtījuma politika**.
1. Laukā **Kritēriji** atlasiet **Izdošanas un nosūtīšanas apstiprinājums**.
1. Rindā, kur **Lauks** ir iestatīts uz *No noliktavas*, laukā **Kritēriji** atlasiet *51*.
1. Atlasiet **Labi**, lai atgrieztos galvenajā dialoglodziņā.
1. Izvērsiet sadaļu **Palaist fonā**, lai iestatītu pakešapstrādi.
1. Iespējojiet **Pakešapstrāde**, kas atrodas zem sadaļas **Palaist fonā**.
1. Atlasiet **Periodiskums** un iestatiet pakešuzdevumu apstrādei, pamatojoties uz jūsu biznesam nepieciešamo intervālu.
1. Atlasiet **Labi**, lai atgrieztos galvenajā dialoglodziņā.
1. Galvenajā dialoglodziņā atlasiet **Labi**, lai pakešuzdevumu pievienotu pakešuzdevumu rindai.

### <a name="set-up-the-process-outbound-shipment-batch-job"></a>Iestatīt pakešuzdevumu “Apstrādāt izejošos sūtījumus”

Šajā sadaļā ir paskaidrots, kā iestatīt ieplānotu pakešuzdevumu, lai izpildītu izejošo sūtījuma apstiprinājumu nosūtīšanai gatavām kravām, kas saistītas ar pārsūtīšanas pasūtījuma rindām, kas ir “gatavas nosūtīšanai”.

1. Dodieties uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Apstrādāt izejošos sūtījumus**.
1. Izvērsiet sadaļu **Iekļaujamie ieraksti**.
1. Atlasiet **Filtrēt**.
1. Vaicājumā **WHSLoadShipConfirm** atlasiet cilni **Savienojumi**.
1. Izvērsiet tabulas hierarhiju, lai tiktu izvērstas **Kravas** un **Kravas informācija**.
1. Atlasiet tabulu **Kravas informācija**.
1. Atlasiet pogu **Pievienot tabulas savienojumu**.
1. Tabulas relāciju sarakstā, kolonnā **Relācija** filtrējiet vai meklējiet *Pārsūtīšanas pasūtījuma rindas (Atsauce)*.
1. Koncentrējieties uz tabulas relāciju sarakstā, pēc tam nospiediet pogu **Atlasīt**.
1. Atlasiet tabulu **Pārsūtīšanas pasūtījuma rindas**.
1. Atlasiet pogu **Pievienot tabulas savienojumu**.
1. Tabulas relāciju sarakstā, kolonnā **Relācija** filtrējiet vai meklējiet *Krājumu pārsūtīšanas papildu lauki (Ieraksta ID)*.
1. Koncentrējieties uz tabulas relāciju sarakstā, pēc tam nospiediet pogu **Atlasīt**.
1. Atlasiet cilni **Diapazons**.
1. Trīs vaicājumu kritēriju diapazoni tiks iestatīti **Diapazona** vaicājumu tabulās. Lai pievienotu rindu, atlasiet pogu **Pievienot**.
1. Pievienojiet diapazonu tabulai **Kravas**. Iestatiet **Lauks** uz *Kravas statuss* un iestatiet **Kritēriji** uz *Iekrauts*.
1. Pievienojiet citu diapazonu tabulai **Krājumu pārsūtīšanas papildu lauki**. Iestatiet **Lauks** uz *Izejošā sūtījuma politika* un iestatiet **Kritēriji** uz *Izdošanas un nosūtīšanas apstiprinājums*.
1. Pievienojiet citu diapazonu tabulai **Kravas informācija**. Iestatiet **Lauks** uz *Atsauce* un iestatiet **Kritēriji** uz *Pārsūtīšanas pasūtījuma nosūtīšana*.
1. Atlasiet **Labi**, lai atgrieztos galvenajā dialoglodziņā.
1. Izvērsiet sadaļu **Palaist fonā**.
1. Iespējojiet **Pakešapstrāde**.
1. Atlasiet **Periodiskums** un iestatiet pakešuzdevumu apstrādei, pamatojoties uz jūsu biznesam nepieciešamo intervālu.
1. Atlasiet **Labi**, lai atgrieztos galvenajā dialoglodziņā.
1. Galvenajā dialoglodziņā atlasiet **Labi**, lai pakešuzdevumu pievienotu pakešuzdevumu rindai.

> [!NOTE]
> Papildinformāciju skatiet sadaļā [Apstiprināt izejošos sūtījumus no pakešuzdevumiem](confirm-outbound-shipments-from-batch-jobs.md).

## <a name="processing-the-example-for-create-transfer-order-from-the-warehouse-app"></a>“Izveidot pārsūtīšanas pasūtījumus no noliktavas programmas” piemēra apstrāde

### <a name="add-on-hand-on-a-license-plate"></a>Pievienot rīcībā esošo noliktavas vienībai

Kā sākumpunkts šim scenārijam ir nepieciešama noliktavas vienība ar fiziski pieejamiem rīcībā esošiem krājumiem.

| Krājums | Noliktava | Krājumu statuss | Novietojums | Noliktavas vienība | Daudzums |
| --- | --- | --- | --- | --- | --- |
| A0001 | 51 | Pieejama | LP-010 | LP10 | 1 |
| A0002 | 51 | Pieejama | LP-010 | LP10 | 2 |

Pievienojiet fiziski pieejamos krājumus rīcībā esošajiem daudzumiem, izmantojot šādas vērtības:

> [!NOTE]
> Jums vajadzēs izveidot noliktavas vienību un izmantot novietojumus, kas ļauj pārvadāt jauktus krājumus, piemēram, LP-010.

### <a name="create-and-process-transfer-orders-from-the-warehouse-app"></a>Izveidot un apstrādāt pārsūtīšanas pasūtījumus no noliktavas programmas

1. Atveriet programmu un piesakieties kā lietotājs *51*. Pašreizējā lietotāja noliktava būs 51.
1. Atlasiet izvēlnes vienumu **Izveidot** no izvēlnes novietojuma, kuru pievienojāt iestatīšanas laikā.
1. Sāciet pārsūtīšanas pasūtījuma izveidi, ievadot mērķa noliktavu (Uz noliktavu) laukā **Noliktava**, ievadot *61*. Jaunais pārsūtīšanas pasūtījums no pašreizējās noliktavas 51 (No noliktavas) tiks nogādāts uz mērķa noliktavu *61*.
1. Atlasiet **Labi**.
1. Skenējiet noliktavas vienības ID laukā **Noliktavas vienība**. Ievadiet krājuma noliktavas vienību, kas tika pievienota iepriekšējā darbībā, *LP10*.
1. Atlasiet **Labi**.
1. Atlasiet izvēlnes pogu un pēc tam atlasiet **Pabeigt pasūtījumu**, lai pabeigtu noliktavas programmas pārsūtīšanas pasūtījuma izveidi.

Minētajā piemērā tiek izmantoti divi **Noliktavas programmas notikumi** (*Izveidot pārsūtīšanas pasūtījumu* un *Pabeigt pārsūtīšanas pasūtījumu*).

### <a name="inquire-the-warehouse-app-events"></a><a name="#inquire-the-warehouse-app-events"></a>Uzziņas par noliktavas programmas notikumiem

Varat skatīt notikumu rindu un notikumu ziņojumus, ko ģenerējusi Warehouse Management mobile programma, dodoties uz **Noliktavas pārvaldība \> Pieprasījumi un pārskati \> Mobilās ierīces žurnāli \> Noliktavas programmas notikumi**.

Notikumu ziņojumi *Izveidot pārsūtīšanas pasūtījumu* saņems statusu *Gaida*, kas nozīmē, ka pakešuzdevums **Apstrādāt noliktavas programmas notikumus** nesaņems un neapstrādās notikumu ziņojumus. Tiklīdz notikuma ziņojuma statuss tiek atjaunināts uz *Rindā*, pakešuzdevums apstrādās notikumus. Tas notiks vienlaicīgi ar notikuma *Pabeigt pārsūtīšanas pasūtījumu* izveidi (kad darbinieks atlasa Warehouse Management mobile programmas pogu **Pabeigt pasūtījumu** ). Kad *Izveidot pārsūtīšanas pasūtījumu* notikuma ziņojumi ir apstrādāti, statuss tiek atjaunināts uz *Pabeigts* vai *Neizdevās*. Kad *Izveidot pārsūtīšanas pasūtījumu* statuss ir atjaunināts uz *Pabeigts*, visi saistītie notikumi tiek dzēsti no rindas.

Pakešuzdevums neapstrādā **Noliktavas programmas notikumus** pārsūtīšanas pasūtījuma datu izveidei, pirms ziņojums tiek atjaunināts uz statusu *Rindā*, tāpēc pieprasītie pārsūtīšanas pasūtījumu numuri ir jāmeklē laukā **Identifikators**. Lauks **Identifikators** ir lapas **Noliktavas programmas notikumi** galvenē.

Kā daļa no noliktavas notikuma apstrādes, pārsūtīšanas pasūtījuma rindas izveide var neizdoties. Šādā gadījumā notikuma ziņojuma stāvoklis tiek atjaunināts uz *Neizdevās*, un varat izmantot **Pakešuzdevumu žurnāls** informāciju, lai uzzinātu, kāpēc un rīkoties, lai labotu problēmas.

Tipiskas problēmas var būt saistītas ar trūkstošiem procesa iestatījumiem, piemēram, trūkst tranzīta noliktava *Izveidot pārsūtīšanas pasūtījumu* notikumam. Šādā gadījumā nosūtīšanas noliktavai jāpievieno tranzīta noliktava un jāizmanto opcija **Atiestatīt**, lai mainītu visu noliktavas programmas notikumu statusu no *Neizdevies* un *Rindā*, kas nozīmē, ka pakešuzdevums apstrādās notikumu ziņojumus pēc iestatījumu datu labošanas.

Ražošanas vidēs izņēmumi varētu būt saistīti ar procesu, piemēram, pieprasītā noliktavas vienība, kas pakešuzdevumu apstrādes laikā ir tukša un tādējādi netiek izveidota neviena pārsūtīšanas pasūtījuma rinda. Šo neizdevušos notikuma ziņojumu var noņemt, izmantojot opciju **Dzēst**, vai arī varat pievienot nepieciešamo fiziski rīcībā esošo noliktavas vienībai un izmantot opciju **Atiestatīt** visiem saistītajiem notikumu ziņojumiem.

Papildinformāciju skatiet sadaļā [Noliktavas programmas notikumu apstrāde](warehouse-app-events.md).

### <a name="follow-up-on-the-example-scenario-processing"></a>Papildinformācija par piemēra procesu

Piemēra izpildes laikā tika veiktas šādas darbības:

1. Izmantojot Warehouse Management mobile programmu, tika atlasīts izvēlnes vienums, kas izmanto aktivitātes kodu **Izveidot pārsūtīšanas pasūtījumu no noliktavas vienībām**.
1. Programma piedāvā atlasīt mērķa noliktavu pārsūtīšanas pasūtījumam. Avota noliktava vienmēr ir tā, kurā pašlaik esat pieteicies kā darbinieks.
1. Atlasot mērķa noliktavu, sistēma rezervēja ID numuru nākamajam pārsūtīšanas pasūtījumam (pamatojoties uz sistēmā definēto pārsūtīšanas pasūtījumu numuru secību), bet pārsūtīšanas pasūtījumu vēl neizveidoja.
1. Skenējot noliktavas vienību *LP10*, kurā ir rīcība esošs krājums, kas jāpārvieto uz jauno noliktavu, notikumu rindai tika pievienots **Noliktavas programmas notikums**, kas tiks apstrādāts vēlāk. Noliktavas notikums ietvēra ziņojuma informāciju par skenēšanu, tostarp paredzēto pārsūtīšanas pasūtījuma numuru.
1. Kad noliktavas programmā ir atlasīta poga **Pabeigt pasūtījumu**, tiek izveidots jauns noliktavas programmas notikums **Pabeigt pārsūtīšanas pasūtījumu** un saistītā esošā notikuma **Izveidot pārsūtīšanas pasūtījumu** statuss tiek mainīts uz **Rindā**.
1. Tikmēr aizmugursistēmā pakešuzdevums **Apstrādāt noliktavas programmas notikumus** saņēma notikumu **Rindā** un apkopoja rīcībā esošos, kas saistīti ar skenēto noliktavas vienību. Pamatojoties uz rīcībā esošo, tika izveidots faktiskais pārsūtīšanas pasūtījuma ieraksts un saistītās rindas. Darbs aizpildīja arī pārsūtīšanas pasūtījuma lauku **Izejošā sūtījuma politika** ar vērtību, kuras pamatā ir konfigurēts *Izdošanas un nosūtīšanas apstiprinājums*, un saistīja noliktavas vienību ar stratēģijas **Noliktavas vienību vadība** rindām.
1. Pamatojoties uz pārsūtīšanas pasūtījuma rindas **Izejošā sūtījuma politika** lauka vērtību, vaicājums **Automātiska pārsūtīšanas pasūtījumu izdošana pakešuzdevumam** tika pabeigts pārsūtīšanas pasūtījumu izdodot nosūtīšanas noliktavai. Un iestatot **Kopuma veidne**, **Darba veidne** un **Novietojuma direktīvas**, darbs tika automātiski apstrādāts, kā rezultātā **Kravas statuss** tika atjaunināts uz *Iekrauts*.
1. Kravai tiek izpildīts **Apstrādāt izejošo sūtījumu pakešuzdevumu**, kā rezultātā tiek nosūtīts pārsūtīšanas pasūtījums un tiek izveidots iepriekšējs paziņojums par nosūtīšanu (IPPN).
1. Visu šo notikumu laiks ir atkarīgs no izveidoto pakešuzdevumu iestatījumiem **Periodiskums**.

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

### <a name="mobile-device-menu-item-setup"></a>Mobilās ierīces izvēlnes vienuma iestatīšana

#### <a name="why-cant-i-see-create-transfer-order-from-license-plate-in-the-menu-item-work-activity-drop-down-list"></a>Kāpēc izvēlnes vienuma darba aktivitāšu nolaižamajā sarakstā nevar redzēt “Izveidot pārsūtīšanas pasūtījumu no noliktavas vienības”?

Ir jābūt iespējotam līdzeklim *Izveidot un apstrādāt pārsūtīšanas pasūtījumus no noliktavas programmas*. Papildinformāciju skatiet sadaļā [Iespējot pārsūtīšanas pasūtījumu izveidi no noliktavas programmas](#enable-create-transfer-order-from-warehouse-app).

### <a name="warehouse-management-mobile-app-processes"></a>Warehouse Management mobile programmas procesi

#### <a name="why-cant-i-see-the-menu-button-complete-order"></a>Kāpēc nevar redzēt izvēlnes pogu “Pabeigt pasūtījumu”?

Pārsūtīšanas pasūtījumam ir jāpiešķir vismaz viena noliktavas vienība.

#### <a name="can-several-warehouse-management-mobile-app-users-add-license-plates-to-the-same-transfer-order-at-the-same-time"></a>Vai vairāki Warehouse Management mobile programmas lietotāji var vienlaikus pievienot noliktavas vienības vienam pārsūtīšanas pasūtījumam?

Jā, vairāki noliktavas darbinieki var skenēt noliktavas vienības tajā pašā pārsūtīšanas pasūtījumā.

#### <a name="can-the-same-license-plate-be-added-to-different-transfer-orders"></a>Vai vienu noliktavas vienību var pievienot dažādiem pārsūtīšanas pasūtījumiem?

Nē, noliktavas vienību vienlaikus var pievienot tikai vienam pārsūtīšanas pasūtījumam.

#### <a name="after-having-selected-the-complete-order-button-can-i-then-add-more-license-plates-for-that-transfer-order"></a>Vai ir iespējams pievienot papildu noliktavas vienības pārsūtīšanas pasūtījumam, pēc pogas “Pabeigt pasūtījumu” atlasīšanas?

Nē, nav iespējams pievienot papildu noliktavas vienības pārsūtīšanas pasūtījumam ar noliktavas programmas notikumu **Pabeigt pārsūtīšanas pasūtījumu**.

#### <a name="how-can-i-find-existing-transfer-orders-to-be-used-via-the-select-transfer-order-button-in-the-warehouse-management-mobile-app-if-the-order-has-not-yet-been-created-in-the-backend-system"></a>Kā Warehouse Management mobile programmā var atrast izmantojamos pārsūtīšanas pasūtījumus, izmantojot pogu “Atlasīt pārsūtīšanas pasūtījumu”, ja pasūtījums vēl nav izveidots aizmugursistēmā?

Pašlaik programmā nav iespējams meklēt pārsūtīšanas pasūtījumus, bet pārsūtīšanas pasūtījumu numurus var atrast lapā **Noliktavas programmas notikumi**. Papildinformāciju skatiet sadaļā [Uzziņas par noliktavas programmas notikumiem](#inquire-the-warehouse-app-events).

#### <a name="can-i-manually-select-the-transfer-order-number-to-be-used-from-the-warehouse-management-mobile-app"></a>Vai no Warehouse Management mobile programmas var manuāli atlasīt izmantojamo pārsūtīšanas pasūtījuma numuru?

Tiek atbalstīti tikai automātiski ģenerētie pārsūtīšanas pasūtījumu numuri, izmantojot numuru secības.

### <a name="background-processing"></a>Fona apstrāde

#### <a name="how-should-i-clean-up-records-in-my-warehouse-app-events-queue-message-tables"></a>Kā dzēst noliktavas programmas notikumu rindas ziņojumu tabulu ierakstus?

Varat skatīt un to uzturēt lapā **Noliktavas programmas notikumi**. Papildinformāciju skatiet sadaļā [Uzziņas par noliktavas programmas notikumiem](#inquire-the-warehouse-app-events).

#### <a name="why-is-the-transfer-order-receipt-date-not-updated-according-to-my-delivery-date-control-setup"></a>Kāpēc pārsūtīšanas pasūtījuma “Saņemšanas datums” nav atjaunināts atbilstoši “Piegādes datuma kontroles” iestatījumam?

Pārsūtīšanas pasūtījumi tiek izveidoti, neizmantojot **Piegādes datuma kontroles** iespējas.

#### <a name="can-i-use-a-license-plate-having-physical-negative-inventory-on-hand"></a>Vai var izmantot noliktavas vienību ar fiziski negatīviem rīcībā esošiem krājumiem?

Šis līdzeklis atbalsta tikai pozitīvus fiziskos rīcībā esošos daudzumus unikālās noliktavas vienības līmenī, bet, piešķirot noliktavas vienības pārsūtīšanas pasūtījumiem, jūs varat izmantot fiziskus negatīvus rīcībā esošos daudzumus augstākā noliktavas un krājuma statusa līmenī.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]