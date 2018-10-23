---
title: "Kreditora darbību saraksta lapa"
description: "Šajā tēmā ir sniegta informācija par kreditora transakciju saraksta lapu sistēmai Microsoft Dynamics 365 for Finance and Operations."
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: c5d4fb53939d88fcb1bd83d70bc361ed9879f298
ms.openlocfilehash: 53740f6ed0d463de5ba962f1ba15b208634a0739
ms.contentlocale: lv-lv
ms.lasthandoff: 10/01/2018

---

# <a name="vendor-transactions-list-page"></a>Kreditora darbību saraksta lapa

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Skatīt nosegšanas darbības

Darbību rūts poga **Skatīt nosegšanas darbības** nodrošina ātru piekļuvi nosegšanas darbību vēsturei un papildu informācijai par visu nosegšanas transakciju. Varat arī parādīt papildu transakcijas, kas ir saistītas ar atlasīto transakciju, vai nu tāpēc, ka tās ir šīs segšanas daļa, vai arī tie ir maksājumi, kas izveidoti tajā pašā maksājumu žurnālā.

1. Atlasiet cilni **Kreditori \> Visi kreditori**.
2. Atlasiet kreditoru, kuram ir transakcijas, un pēc tam darbību rūts cilnē **Kreditors** atlasiet **Transakcija**.
3. Atlasiet transakciju, lai veiktu meklēšanu, un pēc tam darbību rūtī atlasiet **Skatīt nosegšanas darbības**.

    Tiek parādīts dialoglodziņš **Skatīt nosegšanas darbības**, kurā ir redzama atlasītā transakcija un visi dokumenti, kas ir nosegti saistībā ar to. Šis dialoglodziņš līdzinās segšanas vēstures skatam, bet tas ietver visus saistītos dokumentus.

4. Dialoglodziņā var izpildīt dažādus uzdevumus. Atlasiet vienu vai vairākus dokumentus un pēc tam atlasiet vienu no tālāk norādītajām pogām.

    - **Skatīt saistītos maksājumus** – ļauj skatīt visas maksājumu žurnālā izveidotās maksājumu žurnāla transakcijas, kas ir saistīts ar atlasīto dokumentu. Tiek parādītas arī visas nosegšanas darbības, kas ir saistītas ar šiem maksājumiem. Skatot saistītos maksājumus, šīs pogas apzīmējums mainās uz **Skatīt nosegšanas darbības**. Atlasiet **Skatīt nosegšanas darbības**, lai skatītu tikai tās transakcijas, kuras tika parādītas, pirmo reizi atvērot dialoglodziņu **Skatīt nosegšanas darbības**.
    - **Skatīt vēsturi** — ļauj skatīt ar dokumentiem saistīto nosegšanas vēsturi. Atlasiet **Aizvērt**, lai aizvērtu dialoglodziņu.
    - **Skatīt uzskaiti** — ļauj skatīt visus ar atlasītajiem dokumentiem saistītos dokumentus. Atlasiet **Aizvērt**, lai aizvērtu dialoglodziņu.
    - **Eksportēt** – eksportēt atlasītos vaučerus uz programmu Microsoft Excel.
    - **Nosegšanas transakcijas** — šī poga tiek parādīta tikai tad, ja oriģinālais atlasītais dokuments nav pilnībā nosegts. Atlasot šo pogu, tiek parādīts dialoglodziņš **Nosegšanas transakcijas**, kurā var atlasīt nosegšanas transakcijas.
    - **Nosegšanas darbību atsaukšana** — šī poga tiek parādīta tikai tad, ja oriģinālais atlasītais dokuments, ir pilnībā nosegts. Atlasot šo pogu, tiek parādīts dialoglodziņš **Nosegšanas darbību atsaukšana**, kurā var atsaukt nosegšanas darbības, kuras ir veiktas šim dokumentam.

## <a name="global-transactions"></a>Globālās transakcijas

Kreditoru lapā ir pievienota poga **Globālās transakcijas**. Izmantojot šo pogu, var skatīt visas ar kreditoru saistītās transakcijas, ko veikušas visas juridiskās personas. Sarakstu lapā **Kreditora transakcijas** ir redzamas tikai to juridisko personu transakcijas, kurām lietotājam ir piekļuve saskaņā ar viņa vai viņas drošības iestatījumiem.

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
- **Atvērts no konkrētā datuma** — ļauj skatīt tikai tās transakcijas, kas vēl nav pilnībā nosegtas uz norādīto datumu. Atlasot šo opciju, var mainīt datumu, kas ir redzams blakus šim filtram. Sarakstā transakcijas, kurām laukā **Pēdējais nosegšanas datums** vērtība ir pēc norādītā datuma, tiek parādītas arī tad, ja šīs transakcijas pašreizējā datumā ir pilnībā nosegtas. Tomēr bilance norāda bilances uz pašreizējo datumu, nevis uz atlasīto datumu.

Ir pievienots arī filtrs, kas ļauj slēpt valūtas konvertēšanas transakcijas. Atlasiet tikai izvēles rūtiņu **Slēpt valūtas konvertēšanas transakcijas**.

## <a name="more-easily-modify-due-dates-and-discount-dates"></a>Ērtāka apmaksas un atlaides datumu mainīšana

Var atjaunināt debitora atvērtu transakciju apmaksas un atlaides datumu. Versijā 8.1 ir uzlabota izmantošanas pieredze. Tagad sarakstu lapā **Kreditora transakcijas** varat pievienot apmaksas datumu. Noklikšķinot dialoglodziņā **Atjaunināt apmaksas un termiņatlaides datumu** uz apmaksas datuma sarakstu lapā **Kreditora transakcijas**, jūs varat arī mainīt apmaksas un atlaides datumu, apmaksas nosacījumus un termiņatlaides nosacījumus.

### <a name="activate-the-feature"></a>Funkcijas aktivizēšana

Lai sarakstu lapā **Kreditora transakcijas** pievienotu apmaksas datumu un mainītu transakcijas maksājuma iestatījumus, izmantojot dialoglodziņu **Atjaunināt apmaksas un termiņatlaides datumu**, veiciet tālāk aprakstītās darbības.

1. Atlasiet **Kreditori \> Iestatīšana \> Kreditoru parametri**.
2. Cilnē **Nosegšanas darbības** iestatiet opcijas **Rādīt apmaksas datumu un ļaut rediģēt** vērtību **Jā**.
3. Lai iespējotu šo funkciju, kreditora transakcijām ir pievienoti jauni lauki. Šie lauki tiek aizpildīti, kad tiek pabeigta jauna transakcija. Tie tiek aizpildīti arī tad, ja tiek atvērts dialoglodziņš **Atjaunināt apmaksas un termiņatlaides datumu**. Ja ir iestatīta opcijas **Rādīt apmaksas datumu un ļaut rediģēt** vērtība **Jā**, tiek parādīts dialoglodziņš **Atjaunināt maksājuma informāciju**.  Lai tūlītēji atjauninātu esošās transakcijas, atlasiet **Atjaunināt visas esošās transakcijas**. Vai arī atlasiet **Turpināt bez atjaunināšanas**, lai aizpildītu tikai jauno transakciju laukus.

Tagad sarakstu lapā **Kreditora transakcijas** ir pievienots apmaksas datums, un var ērtāk mainīt transakcijas apmaksas un termiņatlaides datumu.

### <a name="modify-the-payment-settings"></a>Maksājuma iestatījumu mainīšana

Sarakstu lapā **Kreditora transakcijas** tiek parādītas visas kreditora transakcijas. Atlasot transakcijas apmaksas datumu, tiek parādīts dialoglodziņš. Šajā dialoglodziņā ir redzams apmaksas datuma un atlaides aprēķinu bāzes datums, apmaksas datums, maksājuma nosacījumi, kā arī termiņatlaides nosacījumi un datums.

Katra lauka izmaiņas citādi ietekmē transakciju.

- **Rediģēt bāzes datumu:** apmaksas un atlaidies datums tiek mainīts tā, lai bāzes datums ir dokumenta datums.
- **Rediģēt apmaksas datumu:** mainīts tiek tikai apmaksas datums
- **Rediģēt atlaides datumu:** mainīts tiek tikai atlaides datums.
- **Rediģēt maksājuma nosacījumus:** apmaksas datums tiek mainīts atbilstoši bāzes datumam un apmaksas nosacījumiem.
- **Rediģēt termiņatlaides nosacījumus:** termiņatlaides tiek mainītas atbilstoši bāzes datumam un termiņatlaides nosacījumiem.

Kad maksājuma iestatījumu rediģēšana ir pabeigta, atlasiet **Aizvērt**, lai saglabātu izmaiņas.

