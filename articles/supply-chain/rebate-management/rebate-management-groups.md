---
title: Atlaižu pārvaldības grupas
description: Šajā rakstā ir aprakstīts, kā iestatīt atlaižu pārvaldības grupas. Atlaižu pārvaldības grupas var izmantot atlaižu aprēķinos, un tās var pievienot šablona ierakstam.
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
ms.openlocfilehash: 2b948e994783d6ec6f00b77d12bd2594a29f6512
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851541"
---
# <a name="rebate-management-groups"></a>Atlaižu pārvaldības grupas

[!include [banner](../includes/banner.md)]

Atlaižu pārvaldības aprēķinus var vadīt pa grupām. Atlaižu pārvaldības grupas var izveidot debitoriem, kreditoriem un krājumiem. Tos var pievienot šablona ierakstam.

## <a name="rebate-management-customer-groups"></a>Atlaižu pārvaldības debitoru grupas

Aprēķins klientu grupai bieži tiek izveidots uzņēmumu ķēdei, piemēram, lielveikalu ķēdei vai franšīzes uzņēmumam. Šis aprēķina veids parasti ir saistīts ar atlaidi.

Ieturējums bieži tiek aprēķināts, neņemot vērā, kam tika pārdots kvalificētais pasūtījums. Taču ir izņēmumi. Piemēram, licenciāts var izveidot ieturējumu shēmu, kurā debitoru grupa A saņems 4 procentus, bet debitoru grupa B saņems tikai 3 procentus.

### <a name="set-up-customer-groups"></a>Iestatīt debitoru grupas

Lai strādātu ar Atlaižu pārvaldības klientu grupām, dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatīšana \> Debitoru grupas**. Jūs varat izmantot pogas Darbību rūtī, lai pievienotu un noņemtu grupas. Katrai grupai iestatiet šādus laukus:

- **Atlaižu pārvaldības grupa** - ievadiet unikālu grupas nosaukumu.
- **Apraksts** — ievadiet grupas aprakstu, lai sniegtu papildinformāciju par tās lietošanu.

### <a name="manage-customer-group-assignments"></a>Pārvaldīt debitoru grupu piešķires

Katrs klients var piederēt jebkuram Atlaižu pārvaldības grupu skaitam. Lai skatītu un piešķirtu grupas dalībniekus, varat sākt no grupu saraksta vai klientu saraksta.

Lai skatītu, pievienotu vai noņemtu atlasītās grupas debitorus, rīkojieties šādi.

1. Dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatījumi \> Klientu grupas**.
1. Atlasiet pārvaldāmo grupu.
1. Darbību rūtī atlasiet **Debitori**. Tiek parādīta lapa **Atlaižu pārvaldības grupas**, kurā redzams to debitoru saraksts, kuri jau ir atlasītās grupas dalībnieki.
1. Darbību rūtī atlasiet **Jauns**, lai pievienotu grupai jaunu debitoru, lai pievienotu režģim rindu. Jaunajā rindā iestatiet šādu lauku:

    - **Debitora konts** - atlasiet debitora konta ID.

1. Lai noņemtu debitoru no grupas, atlasiet klientu un pēc tam darbību rūtī atlasiet **Dzēst**.

Lai skatītu, pievienotu vai noņemtu atlasītās grupas piešķires atlasītajam debitoram, rīkojieties šādi.

1. Dodieties uz **Debitoru parādi \> Debitori \> Visi debitori**.
1. Atlasiet debitoru, ar kuru jāstrādā.
1. Darbību rūtī cilnē **Debitori** grupā **Atlaižu pārvaldība** atlasiet **Atlaižu pārvaldības grupas**. Tiek parādīta lapa **Atlaižu pārvaldības grupas**, kurā redzams to debitoru saraksts, kuri jau ir atlasītās grupas dalībnieki.
1. Darbību rūtī atlasiet **Jauns**, lai pievienotu grupai jaunu debitoru, lai pievienotu režģim rindu. Jaunajā rindā iestatiet šādu lauku:

    - **Atlaižu pārvaldības grupa** – atlasiet grupu, kurā pievienot debitoru.

1. Lai noņemtu debitoru no grupas, atlasiet grupu un pēc tam darbību rūtī atlasiet **Dzēst**.

## <a name="rebate-management-vendor-groups"></a>Atlaižu pārvaldības kreditoru grupas

Aprēķins kreditoru grupai bieži tiek izveidots piegādes punktu grupai. Šis aprēķina veids parasti ir saistīts ar atlaidi.

### <a name="set-up-vendor-groups"></a>Kreditoru grupu iestatīšana

Lai strādātu ar Atlaižu pārvaldības kreditoru grupām, dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatījumi \> Kreditoru grupas**. Jūs varat izmantot pogas Darbību rūtī, lai pievienotu un noņemtu grupas. Katrai grupai iestatiet šādus laukus:

- **Atlaižu pārvaldības grupa** - ievadiet unikālu grupas nosaukumu.
- **Apraksts** — ievadiet grupas aprakstu, lai sniegtu papildinformāciju par tās lietošanu.

### <a name="manage-vendor-group-assignments"></a>Pārvaldīt kreditoru grupu piešķires

Katrs kreditors var piederēt jebkuram Atlaižu pārvaldības grupu skaitam. Lai skatītu un piešķirtu grupas dalībniekus, varat sākt no grupu saraksta vai kreditoru saraksta.

Lai skatītu, pievienotu vai noņemtu atlasītās grupas kreditorus, rīkojieties šādi.

1. Dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatījumi \> Kreditoru grupas**.
1. Atlasiet pārvaldāmo grupu.
1. Darbību rūtī atlasiet **Kreditori**. Tiek parādīta lapa **Atlaižu pārvaldības grupas**, kurā redzams to kreditoru saraksts, kuri jau ir atlasītās grupas dalībnieki.
1. Darbību rūtī atlasiet **Jauns**, lai pievienotu grupai jaunu kreditoru, lai pievienotu režģim rindu. Jaunajā rindā iestatiet šādu lauku:

    - **Kreditora konts** - atlasiet kreditora konta ID.

1. Lai noņemtu kreditoru no grupas, atlasiet klientu un pēc tam darbību rūtī atlasiet **Dzēst**.

Lai skatītu, pievienotu vai noņemtu atlasītās grupas piešķires atlasītajam kreditoram, rīkojieties šādi.

1. Dodieties uz **Kreditori \> Kreditori \> Visi kreditori**.
1. Atlasiet kreditoru, ar kuru jāstrādā.
1. Darbību rūtī cilnē **Kreditori** grupā **Atlaižu pārvaldība** atlasiet **Atlaižu pārvaldības grupas**. Tiek parādīta lapa **Atlaižu pārvaldības grupas**, kurā redzams to kreditoru saraksts, kuri jau ir atlasītās grupas dalībnieki.
1. Darbību rūtī atlasiet **Jauns**, lai pievienotu grupai jaunu kreditoru, lai pievienotu režģim rindu. Jaunajā rindā iestatiet šādu lauku:

    - **Atlaižu pārvaldības grupa** – atlasiet grupu, kurā pievienot kreditoru.

1. Lai noņemtu kreditoru no grupas, atlasiet grupu un pēc tam darbību rūtī atlasiet **Dzēst**.

## <a name="item-rebate-groups"></a>Krājumu atlaižu grupas

Grupējot krājumus, jums ir lielāka elastība, aprēķinot atlaides un ieturējumus. Šī pieeja bieži vien ir efektīvāks veids, kā iestatīt atlaides un atskaitījumus debitoriem un kreditoriem.

### <a name="set-up-item-groups"></a>Iestatīt krājumu grupas

Lai strādātu ar Atlaižu pārvaldības krājumu grupām, dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatījumi \> Krājumu grupas**. Jūs varat izmantot pogas Darbību rūtī, lai pievienotu un noņemtu grupas. Katrai grupai iestatiet šādus laukus:

- **Atlaižu pārvaldības grupa** - ievadiet unikālu grupas nosaukumu.
- **Apraksts** — ievadiet grupas aprakstu, lai sniegtu papildinformāciju par tās lietošanu.

### <a name="manage-item-group-assignments"></a>Pārvaldīt krājumu grupu piešķires

Katrs krājums var piederēt jebkuram Atlaižu pārvaldības grupu skaitam. Lai skatītu un piešķirtu grupas dalībniekus, varat sākt no grupu saraksta vai krājumu saraksta. Varat arī pievienot krājumus, pamatojoties uz kategoriju hierarhiju.

Lai skatītu, pievienotu vai noņemtu atlasītās grupas krājumus, rīkojieties šādi.

1. Dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatījumi \> Krājumu grupas**.
1. Atlasiet pārvaldāmo grupu.
1. Darbību rūtī atlasiet **Krājumi**. Tiek parādīta lapa **Atlaižu pārvaldības grupas**, kurā redzams to krājumu saraksts, kuri jau ir atlasītās grupas dalībnieki.
1. Darbību rūtī atlasiet **Jauns**, lai pievienotu grupai jaunu krājumu, lai pievienotu režģim rindu. Jaunajā rindā iestatiet šādu lauku:

    - **Kreditora konts** - atlasiet krājuma konta ID.

1. Lai noņemtu krājumu no grupas, atlasiet krājumu un pēc tam darbību rūtī atlasiet **Dzēst**.

Lai skatītu, pievienotu vai noņemtu atlasītās grupas piešķires atlasītajam krājumam, rīkojieties šādi.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atlasiet krājumu, ar kuru jāstrādā.
1. Darbību rūtī cilnē **Preces** grupā **Atlaižu pārvaldība** atlasiet **Atlaižu pārvaldības grupas**. Tiek parādīta lapa **Atlaižu pārvaldības grupas**, kurā redzams to grupu saraksts, kuriem jau pieder atlasītais krājums.
1. Darbību rūtī atlasiet **Jauns**, lai pievienotu grupai jaunu krājumu, lai pievienotu režģim rindu. Jaunajā rindā iestatiet šādu lauku:

    - **Atlaižu pārvaldības grupa** – atlasiet grupu, kurā pievienot krājumu.

1. Lai noņemtu krājumu no grupas, atlasiet grupu un pēc tam darbību rūtī atlasiet **Dzēst**.

Lai grupai pievienotu krājumus, pamatojoties uz kategoriju hierarhiju, rīkojieties šādi.

1. Dodieties uz **Atlaižu pārvaldība \> Atlaižu pārvaldības grupu iestatījumi \> Krājumu grupas**.
1. Atlasiet pārvaldāmo grupu.
1. Darbību rūtī atlasiet **Pievienot krājumus**.
1. Dialoglodziņa **Pievienot krājumus** laukā **Kategoriju hierarhija** atlasiet augstākā līmeņa kategoriju.
1. Krājumu hierarhija tiek atvērta kreisajā rūtī. Atlasiet meklējamo hierarhijas līmeni. 
1. Krājumi no atlasītā hierarhijas un hierarhijas līmeņa tagad ir uzskaitīti labajā rūtī. Lai strādātu ar rūti, rīkojieties šādi:

    - Atzīmējiet katra pievienojamā krājuma izvēles rūtiņu.
    - Atzīmējiet izvēles rūtiņu režģa galvenē, lai atlasītu visus uzskaitītos krājumus.
    - Atlasiet pogu **Rādīt atlasīto**, lai filtrētu režģi tā, lai tajā būtu redzami tikai līdz šim atlasītie krājumi. Lai atgrieztos pilnajā sarakstā, vēlreiz atlasiet pogu.

1. Atlasiet **Labi**, lai atlasītajai grupai lietotu vienumu atlasi.
