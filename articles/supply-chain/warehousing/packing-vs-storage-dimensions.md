---
title: Iestatīt dažādas iepakošanas un glabāšanas dimensijas
description: Šajā tēmā ir parādīts, kā norādīt, kurai procesam (iepakošanai, uzglabāšanai vai ligzdotam iepakojumam) tiek izmantota katra noteiktā dimensija.
author: mirzaab
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResPhysicalProductDimensions, WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: e997f8bccde7856303d8b3c6407143598ccc6030
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818924"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a>Iestatīt dažādas iepakošanas un glabāšanas dimensijas

[!include [banner](../../includes/banner.md)]

Daži krājumi tiek iepakoti vai uzglabāti tā, ka katram no vairākiem dažādiem procesiem fiziskās dimensijas var būt atšķirīgas. Funkcija *Iepakojuma preces dimensijas* ļauj iestatīt katram produktam vienu vai vairākus dimensiju tipus. Katrs dimensiju tips sniedz fizisko mērījumu kopu (svars, platums, dziļums un augstums) un nosaka procesu, kur tiek pielietotas šīs fiziskās mērījumu vērtības. Kad šī funkcija ir aktivizēta, sistēma atbalsta šādus dimensiju tipus:

- *Noliktava* - noliktavas dimensijas tiek izmantotas kopā ar atrašanās vietas tilpums, lai noteiktu, cik no katra krājuma var uzglabāt dažādās noliktavas vietās.
- *Iepakošana* - iepakošanas dimensijas tiek izmantotas konteinerinēšanas un manuālās iepakošanas procesa laikā, lai noteiktu, cik daudz katra krājuma iederēsies dažādos konteinera tipos.
- *Ligzdots iepakojums* - ligzdotas iepakojuma dimensijas tiek izmantotas, kad iepakošanas procesā ir vairāki līmeņi.

*Noliktavas dimensijas* tiek atbalstītas pat tad, ja nav iespējota funkcija *Iepakojuma preces dimensijas*. Jūs tos iestatāt, izmantojot **Fizisko dimensiju** lapu programmā Supply Chain Management. Šīs dimensijas tiek izmantotas visos procesos, kuros nav norādītas iepakošanas un ligzdotās iepakojuma dimensijas.

*Iepakošanas* un *ligzdotā iepakojuma* dimensijas tiek iestatītas, izmantojot lapu **Fizisko preču dimensijas**, kas tiek pievienotas, iespējojot iespēju *Iepakojuma preces dimensijas*.
Šajā tēmā sniegts scenārijs, kas parāda, kā izmantot šo funkciju.

## <a name="turn-on-the-packaging-product-dimensions-feature"></a>Ieslēgt iepakojuma preču dimensiju līdzekli

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu. Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Produkta iepakojuma dimensijas*

## <a name="example-scenario"></a>Piemērs

### <a name="set-up-the-scenario"></a>Scenārija iestatīšana

Pirms jūs varat palaist piemēra scenāriju, jums ir jāsagatavo sistēma, kā aprakstīts šajā sadaļā.

#### <a name="enable-demo-data"></a>Iespējot paraugdatus

Lai, izmantojot šo scenāriju, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [paraugdati](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Turklāt pirms sākšanas ir jāatlasa *USMF* juridiskā persona.

#### <a name="add-a-new-physical-dimension-to-a-product"></a>Pievienot precei jaunu fizisko dimensiju

Pievienojiet precei jaunu fizisko dimensiju, rīkojoties šādi:

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atlasiet preci ar **Krājuma numuru** *A0001*.
1. Darbību rūtī cilnes **Pārvaldīt krājumus** grupā **Noliktava** atlasiet **Preces fiziskās dimensijas**.
1. Atveras lapa **Preces fiziskās dimensijas**. Darbību rūtī atlasiet **Jauns**, lai pievienotu rindu režģim, un pēc tam atlasiet šos iestatījumus:
    - **Fiziskās dimensijas tips** - *Iepakojums*
    - **Fiziska vienība** - *gab*
    - **Svars** - *4*
    - **Svara mērvienība** - *kg*
    - **Dziļums** - *3*
    - **Augstums** - *4*
    - **Platums** - *3*
    - **Garums** - *cm*
    - **Tilpuma mērvienība** - *cm3*

Lauks **Tilpums** tiek aprēķināts automātiski, pamatojoties uz **Dziļuma**, **Augstuma** un **Platuma** iestatījumiem.

#### <a name="create-a-new-container-type"></a>Izveidot jaunu konteinera tipu

Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Konteineri \> Konteinera tipi** un izveidojiet jaunu ierakstu ar šādiem iestatījumiem:

- **Konteinera tipa kods** - *maza kaste*
- **Apraksts** - *maza kaste*
- **Maksimālais neto svars** - *50*
- **Tilpums** - *144*
- **Garums** - *6*
- **Platums** - *6*
- **Augstums** - *4*

#### <a name="create-a-container-group"></a>Konteineru grupas izveide

Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Konteineri \> Konteinera tipi** un izveidojiet jaunu ierakstu ar šādiem iestatījumiem:

- **Konteineru grupas ID** - *maza kaste*
- **Apraksts** - *maza kaste*

Pievienojiet jauu rindu sadaļā **Detalizēta informācija**. Iestatiet **Konteinera veidu** uz *maza kaste*.

#### <a name="set-up-a-container-build-template"></a>Konteinera būvējuma veidnes iestatīšana

Dodieties uz **Noliktavas vadība \> Iestatījumi \> Konteineris \> Konteinera būvējuma veidnes** un atlasiet **Kastes**. Mainīt **Konteineru grupas ID** uz *maza kaste*.

### <a name="run-the-scenario"></a>Palaist scenāriju

Kad esat sagatavojis sistēmu tā, kā aprakstīts iepriekšējā sadaļā, esat gatavs palaist scenāriju tā, kā aprakstīts nākamajā sadaļā.

#### <a name="create-a-sales-order-and-create-a-shipment"></a>Izveidot pārdošanas pasūtījumu un izveidot kravu

Šajā procesā tiks izveidots sūtījums, balstoties uz krājuma *iepakojuma* dimensijām, kurām augstums ir mazāks par 3.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - **Debitora konts:** *US-001*
    - **Noliktava:** *63*

1. Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu un aizvērtu dialoglodziņu.
1. Jaunais pārdošanas pasūtījums ir atvērts. Tam ir jāietver jauna, tukša rinda režģī kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**. Iestatiet šādas vērtības šai rindai:

    - **Krājuma numurs:** *A0001*
    - **Daudzums:** *5*

1. Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet **Krājumi \> Rezervācija**.
1. Lapas **Rezervācija** darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu krājumus.
1. Aizvērt lapu.
1. Darbību rūts cilnē **Noliktava** atlasiet **Pārvietot uz noliktavu**, lai noliktavai izveidotu darbu.
1. Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet **Noliktava \> Detalizēta informācija par sūtījumu**.
1. Darbības rūtī atveriet cilni **Transports** un atlasiet **Skatīt konteinerus**. Apstipriniet, ka krājums ir salikts divos *mazo kastu* konteineros.

#### <a name="place-an-item-into-storage"></a>Preces novietošana noliktavā

1. Atveriet mobilo ierīci, piesakieties noliktavā 63 un dodieties uz sadaļu **Krājums \> Pielāgošana**.
1. Ievadiet **Loc** = *SHORT-01*. Izveidojiet jaunu numura zīmi ar **Krājumu** = *A0001* un **Daudzumu** = *1 gab.*.
1. Atlasiet **Labi**. Tiks saņemts kļūdas ziņojums "Atrašanās vieta SHORT-01 neizdevās, jo krājums A0001 neatbilst novietojumā norādītajām dimensijām." Tas tādēļ, ka preces *Noliktavas* tipa dimensijas ir lielākas par noliktavas profilā norādītajām dimensijām.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]