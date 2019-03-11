---
title: Kreditora darbību saraksta lapa
description: Šajā tēmā ir sniegta informācija par saraksta lapu Kreditora transakcijas programmā Microsoft Dynamics 365 for Finance and Operations.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 99a169bd51e14f15c085f7547ec240b2787258cc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "341745"
---
# <a name="vendor-transactions-list-page"></a>Kreditora darbību saraksta lapa

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Skatīt nosegšanas darbības

Darbību rūts poga **Skatīt nosegšanas darbības** nodrošina ātru piekļuvi nosegšanas darbību vēsturei un detalizētai informācijai par nosegšanas transakciju. Varat arī parādīt papildu transakcijas, kas ir saistītas ar atlasīto transakciju, vai nu tāpēc, ka tās ir šīs segšanas daļa, vai arī tie ir maksājumi, kas izveidoti tajā pašā maksājumu žurnālā.

1. Atlasiet cilni **Kreditori \> Visi kreditori**.
2. Atlasiet kreditoru, kuram ir transakcijas, un pēc tam darbību rūts cilnē **Kreditors** atlasiet **Transakcija**.
3. Atlasiet transakciju, lai veiktu meklēšanu, un pēc tam darbību rūtī atlasiet **Skatīt nosegšanas darbības**.

    Tiek parādīts dialoglodziņš **Skatīt nosegšanas darbības**, kurā ir redzama atlasītā transakcija un visi dokumenti, kas ir nosegti saistībā ar to. Šis dialoglodziņš līdzinās segšanas vēstures skatam, bet tas ietver visus saistītos dokumentus.

4. Dialoglodziņā var izpildīt dažādus uzdevumus. Atlasiet vienu vai vairākus dokumentus un pēc tam atlasiet vienu no tālāk norādītajām pogām.

    - **Skatīt saistīto** — parādīt visas konkrētā kreditora maksājumu žurnāla transakcijas un Virsgrāmatas žurnāla transakcijas, kas ir izveidotas žurnālos, kuros ir izveidoti sarakstā redzamie dokumenti. Piemēram, ja tiek rādīts maksājums, tad tiek parādīti visi maksājumi tajā maksājumu žurnālā, kurā ir izveidots šis maksājums. Ja tiek rādīts rēķins vai maksājums, kas ir izveidots Virsgrāmatas žurnālā, tad tiek parādīti visi dokumenti tajā Virsgrāmatas žurnālā, kurā ir izveidots šis rēķins vai maksājums. Tiek parādītas arī visas ar dokumentu sarakstu saistītas nosegšanas darbības. Skatot saistītos maksājumus, šīs pogas apzīmējums mainās uz **Skatīt nosegšanas darbības**. Atlasiet **Skatīt nosegšanas darbības**, lai skatītu tikai tās transakcijas, kuras tika parādītas, pirmo reizi atvērot dialoglodziņu **Skatīt nosegšanas darbības**.
    - **Skatīt vēsturi** — ļauj skatīt ar dokumentiem saistīto nosegšanas vēsturi. Atlasiet **Aizvērt**, lai aizvērtu dialoglodziņu.
    - **Skatīt uzskaiti** — ļauj skatīt visus ar atlasītajiem dokumentiem saistītos dokumentus. Atlasiet **Aizvērt**, lai aizvērtu dialoglodziņu.
    - **Eksportēt** — eksportēt atlasītos dokumentus uz programmu Microsoft Excel.
    - **Nosegšanas transakcijas** — šī poga tiek parādīta tikai tad, ja oriģinālais atlasītais dokuments nav pilnībā nosegts. Atlasot šo pogu, tiek parādīts dialoglodziņš **Nosegšanas transakcijas**, kurā var atlasīt nosegšanas transakcijas.
    - **Nosegšanas darbību atsaukšana** — šī poga tiek parādīta tikai tad, ja oriģinālais atlasītais dokuments, ir pilnībā nosegts. Atlasot šo pogu, tiek parādīts dialoglodziņš **Nosegšanas darbību atsaukšana**, kurā var atsaukt nosegšanas darbības, kuras ir veiktas šim dokumentam.

## <a name="global-transactions"></a>Globālās transakcijas

Poga **Globālās transakcijas** tiek rādīta arī sarakstu lapā **Kreditoru transakcijas**. Izmantojot šo pogu, var skatīt visas ar kreditoru saistītās transakcijas, ko veikušas visas juridiskās personas. Sarakstu lapā **Kreditora transakcijas** ir redzamas tikai to juridisko personu transakcijas, kurām lietotājam ir piekļuve saskaņā ar viņa vai viņas drošības iestatījumiem.

Sarakstu lapā tiek parādītas to kreditoru transakcijas, kuriem ir tāds pats puses ID kā atlasītajam kreditoram. Piemēram, ja juridiskas personas kreditoram US-001 ir tāds pats puses ID kā citas juridiskas personas kreditoram DE-001, tiek parādītas visas abu kreditoru ID transakcijas.

Izvēlnes sarakstu lapā **Kreditoru transakcijas** atšķiras atkarībā no juridiskās personas, kas veikusi transakciju. Piemēram, ja funkcija ir pieejama tikai Šveices juridiskajām personām, šīs funkcijas izvēlnes opcijas tiek parādītas tikai tad, ja ir atlasīta Šveices transakcija.

Lai piekļūtu funkcijai, veiciet tālāk norādītās darbības.

1. Atlasiet **Kreditori** \> **Visi kreditori**.
2. Atlasiet kreditoru un pēc tam darbību rūts cilnes **Kreditors** grupā **Transakcijas** atlasiet **Globālās transakcijas**.

## <a name="more-transaction-filters"></a>Papildu transakciju filtri

Filtrs atvērto transakciju parādīšanai ir aizstāts ar jaunu filtru, kas ļauj skatīt transakciju papildu kombinācijas. Laukā **Rādīt** ir pieejamas tālāk norādītās opcijas.

- **Visi** — ļauj skatīt visas atlasīto kreditoru transakcijas (atvērtas un slēgtas).
- **Slēgts** — ļauj skatīt tikai tās transakcijas, kuras ir pilnībā nosegtas un aizvērtas.
- **Atvērts** — ļauj skatīt tikai tās transakcijas, kuras nav pilnībā nosegtas.
- **Atvērt, ieskaitot tās, kas slēgtas datumā vai pēc datuma** — rādīt tikai tās transakcijas, kas vēl nav pilnībā nosegtas jūsu norādītajā datumā vai pēc tā. Atlasot šo opciju, var mainīt datumu, kas ir redzams blakus šim filtram. Sarakstā transakcijas, kurām laukā **Pēdējais nosegšanas datums** vērtība ir norādītajā datumā vai pēc tā, tiek parādītas arī tad, ja šīs transakcijas pašreizējā datumā ir pilnībā nosegtas. Tomēr bilance norāda bilances uz pašreizējo datumu, nevis uz atlasīto datumu.

Atzīmējiet izvēles rūtiņu **Slēpt valūtas konvertēšanas transakcijas**, lai slēptu valūtu pārrēķināšanas transakcijas.

## <a name="modify-due-dates-and-discount-dates"></a>Apmaksas un atlaides datumu mainīšana

Var atjaunināt debitora atvērtu transakciju apmaksas un atlaides datumu. Laidienā 8.1 tagad sarakstu lapā **Kreditoru transakcijas** varat pievienot paredzētos apmaksas datumus. Noklikšķinot dialoglodziņā **Atjaunināt apmaksas un termiņatlaides datumu** uz apmaksas datuma sarakstu lapā **Kreditora transakcijas**, jūs varat arī mainīt apmaksas un atlaides datumu, apmaksas nosacījumus un termiņatlaides nosacījumus.

### <a name="activate-the-feature"></a>Funkcijas aktivizēšana

Lai sarakstu lapā **Kreditora transakcijas** pievienotu apmaksas datumu un mainītu transakcijas maksājuma iestatījumus, izmantojot dialoglodziņu **Atjaunināt apmaksas un termiņatlaides datumu**, veiciet tālāk aprakstītās darbības.

1. Atlasiet **Kreditori \> Iestatīšana \> Kreditoru parametri**.
2. Cilnē **Nosegšanas darbības** iestatiet opcijas **Rādīt apmaksas datumu un ļaut rediģēt** vērtību **Jā**.
3. Lai iespējotu šo funkciju, kreditora transakcijām ir pievienoti jauni lauki. Šie lauki tiek aizpildīti, kad tiek pabeigta jauna transakcija. Tie tiek aizpildīti arī tad, ja tiek atvērts dialoglodziņš **Atjaunināt apmaksas un termiņatlaides datumu**. Ja ir iestatīta opcijas **Rādīt apmaksas datumu un ļaut rediģēt** vērtība **Jā**, tiek parādīts dialoglodziņš **Atjaunināt maksājuma informāciju**.  Lai tūlītēji atjauninātu esošās transakcijas, atlasiet **Atjaunināt visas esošās transakcijas**. Vai arī atlasiet **Turpināt bez atjaunināšanas**, lai aizpildītu tikai jauno transakciju laukus.

Tagad sarakstu lapā **Kreditoru transakcijas** ir pievienots paredzētais apmaksas datums, tādēļ varat ērtāk mainīt transakciju apmaksas un termiņatlaides datumus.

### <a name="modify-the-payment-settings"></a>Maksājuma iestatījumu mainīšana

Sarakstu lapā **Kreditora transakcijas** tiek parādītas visas kreditora transakcijas. Atlasot transakcijas apmaksas datumu, tiek parādīts dialoglodziņš. Šajā dialoglodziņā ir redzams apmaksas datuma un atlaides aprēķinu bāzes datums, apmaksas datums, maksājuma nosacījumi, kā arī termiņatlaides nosacījumi un datums.

Katra lauka izmaiņas citādi ietekmē transakciju.

- **Rediģēt bāzes datumu** — apmaksas un atlaides datums tiek mainīts tā, lai bāzes datums ir dokumenta datums.
- **Rediģēt apmaksas datumu** — tiek mainīts tikai paredzētais apmaksas datums
- **Rediģēt atlaides datumu** — mainīts tiek tikai atlaides datums.
- **Rediģēt maksājuma nosacījumus** — apmaksas datums tiek mainīts atbilstoši bāzes datumam un apmaksas nosacījumiem.
- **Rediģēt termiņatlaides nosacījumus** — termiņatlaides tiek mainītas atbilstoši bāzes datumam un termiņatlaides nosacījumiem.

Kad maksājuma iestatījumu rediģēšana ir pabeigta, atlasiet **Aizvērt**, lai saglabātu izmaiņas.
