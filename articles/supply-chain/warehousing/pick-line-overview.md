---
title: Mobilās ierīces izvēlnes vienumu iestatīšana, lai nodrošinātu izdošanas rindas pārskatu
description: Šajā tēmā ir paskaidrots, kā definēt visu darba rindu sarakstu, kas tiks parādīts noliktavas darbiniekiem, kuri apstrādā noliktavas darbu mobilajā ierīcē. Šī iespēja var būt noderīga noliktavas darbiniekiem, kuriem bieži ir nepieciešams pārskats par izdošanas rindām darba pasūtījumā, lai varētu optimizēt izdošanas secību.
author: MarkusFogelberg
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: bec9c779399b252277c7688d4bdaf9794c050c18925eebaec0a8c0ffe2b3df28
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763895"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a>Mobilās ierīces izvēlnes vienumu iestatīšana, lai nodrošinātu izdošanas rindas pārskatu

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā konfigurēt opcijas, kas saistītas ar izdošanas rindas pārskatu mobilās ierīces izvēlnes vienumiem, kas tiek izmantoti, lai apstrādātu izdošanas darbu. Izdošanas rindas pārskats ļauj noliktavas darbiniekiem skatīt un atlasīt no saraksta visas darba rindas, kas saistītas ar viņu pašreizējo uzdevumu. Šī iespēja palīdz darbiniekiem optimizēt izdošanas secību. Līdzeklis nodrošina opcijas, kas aizvieto standarta **Izlaist** pogu, ļaujot darbiniekiem pārlūkot rindas pa vienai, fiksētā secībā. (Tomēr pogas izmantošanas opcija joprojām ir pieejama.)

Administratori var konfigurēt katru izvēlnes vienumu atsevišķi, lai kontrolētu, kā, kad un kur noliktavas programma parāda izdošanas rindas pārskatu.

## <a name="turn-on-the-work-pick-line-overview-feature"></a>Darba izdošanas rindas pārskata līdzekļa ieslēgšana

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** _Noliktavas vadība_
- **Līdzekļa nosaukums:** _Darba izdošanas rindas pārskats_

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a>Izvēlnes vienumu konfigurēšana, lai parādītu sarakstu ar visām darba rindām

Lai iestatītu mobilās ierīces izvēlnes vienumu, kas nodrošinātu izdošanas rindas pārskatu, veiciet tālāk norādītās darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Atlasiet vai izveidojiet izvēlnes vienumu, kas ir saistīts ar izdošanas darbu, un iestatiet šādas vērtības:

    - **Režīms:** *Darbs*
    - **Izmantot esošo darbu:** *Jā*
    - **Noteicējs:** *Lietotāja noteikts* vai *Sistēmas noteikts*

    Papildinformāciju par izvēlnes vienumu izveidi un izmantojumu dažādos iestatījumos, kas ir pieejami **mobilās ierīces izvēlnes vienumu** lapā, skatiet sadaļā [mobilo ierīču iestatīšana darbam noliktavā](configure-mobile-devices-warehouse.md).

1. Kopsavilkuma cilnē **Vispārīgi** konfigurējiet līdzekli, iestatot lauku **Rādīt darba rindu sarakstu** uz vienu no šīm vērtībām:

    - **Rādīt tikai pēc pieprasījuma** – darbinieki var izvēlēties skatīt izdošanas rindu sarakstu, Warehouse Management mobile programmā atlasot pogu **Pāriet uz**.
    - **Rādīt katras izdošanas sākumā** – darbinieki redz sarakstu katru reizi, kad tiek sākta vai pabeigta izdošanas rinda. Viņi var skatīt sarakstu arī atkārtoti, Warehouse Management mobile programmā atlasot pogu **Pāriet uz**.
    - **Rādīt tikai pirmās izdošanas sākumā** – darbinieki redz sarakstu katru reizi, kad tiek sākts jauns izdošanas darbs, bet ne pēc katras rindas. Viņi var skatīt sarakstu arī atkārtoti, Warehouse Management mobile programmā atlasot pogu **Pāriet uz**.
    - **Nekad nerādīt** – Warehouse Management mobile programmā tiek parādīta standarta poga **Izlaist** un tiek izslēgts darba rindu saraksta rādījums. Poga **Izlaist** ļauj darbiniekiem pārlūkot rindas pa vienai, fiksētā secībā. Viņi var arī pārlūkot sarakstu tik daudz reižu, cik nepieciešams, līdz visas rindas ir apstrādātas.

1. Darbību rūtī atlasiet **Saglabāt**.

    Ja lauku **Rādīt darba rindu sarakstu** iestatāt uz jebkādu vērtību, izņemot *Nekad nerādīt*, tad darbību rūts poga **Lauku saraksts** kļūst pieejama.

1. Darbību rūtī atlasiet **Lauku saraksts**.
1. Lapā **Lauku saraksts** konfigurējiet informāciju, ko Warehouse Management mobile programma rāda katrai rindai sarakstā.

    - Lauks **Primārā kontrole** vienmēr ir iestatīts uz *LineNum*. Tāpēc katra saraksta rinda sākas ar rindas numuru.
    - Izmantojiet atlikušos **Parādāmais lauks** laukus, lai pievienotu līdz septiņiem papildu parādāmajiem laukiem, pēc nepieciešamības. Katrā **Parādāmais lauks** laukā atlasiet darba rindas lauka nosaukumu. Katrai rindai tiks parādīta šī lauka vērtība. Vērtības tiks rādītas šeit atlasītajā pasūtījumā. Dažus no **Parādāmais lauks** laukiem var atstāt tukšus, ja nav nepieciešamas visas septiņas vērtības.

1. Darbību rūtī atlasiet **Saglabāt** un pēc tam aizveriet lapu **Lauku saraksts**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]