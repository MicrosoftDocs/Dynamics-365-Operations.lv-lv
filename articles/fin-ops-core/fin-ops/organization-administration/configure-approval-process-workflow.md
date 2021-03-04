---
title: Apstiprināšanas procesu konfigurēšana darbplūsmā
description: Izmantojiet tālāk aprakstīto procedūru, lai konfigurētu apstiprināšanas procesa rekvizītus.
author: ChrisGarty
manager: AnnBe
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6f4f6a3fdf07ae267f92eedd312c6c721f18429
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692896"
---
# <a name="configure-approval-processes-in-a-workflow"></a>Apstiprināšanas procesu konfigurēšana darbplūsmā

[!include [banner](../includes/banner.md)]

Izmantojiet tālāk aprakstīto procedūru, lai konfigurētu apstiprināšanas procesa rekvizītus.

Lai konfigurētu apstiprināšanas procesu, darbplūsmas redaktorā ar peles labo pogu noklikšķiniet uz apstiprināšanas elementa un pēc tam noklikšķiniet uz **Rekvizīti**, lai atvērtu formu **Rekvizīti**.

## <a name="name-the-approval-process"></a>Nosaukuma piešķiršana apstiprināšanas procesam

Veiciet šīs darbības, lai ievadītu apstiprināšanas procesa nosaukumu.

1. Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.
2. Laukā **Nosaukums** ievadiet unikālu apstiprināšanas procesa nosaukumu.

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a>Norādiet, kad sistēma automātiski veic darbību ar dokumentu

Varat konfigurēt, lai sistēma automātiski rīkotos ar dokumentu, ja ir izpildīti konkrēti nosacījumi. Piemēram, sistēma var apstiprināt izdevumu pārskatus, kuros kopējās summas ir mazākas par USD 100. Izpildiet šīs darbības, lai norādītu, kad sistēma veic darbības ar dokumentu.

1. Kreisajā rūtī noklikšķiniet uz **Automātiskas darbības**.
2. Atzīmējiet izvēles rūtiņu **Iespējot automātiskas darbības**.
3. Noklikšķiniet uz **Pievienot nosacījumu**.
4. Ievadīt nosacījumu.
5. Ja nepieciešams, ievadiet papildu nosacījumus.
6. Lai pārbaudītu, vai ievadītie nosacījumi ir pareizi konfigurēti, veiciet šādas darbības:

    1. Noklikšķiniet uz **Pārbaudīt**, lai atvērtu formu **Testēt darbplūsmas nosacījumu**.
    2. Formas apgabalā **Pārbaudīt nosacījumu** atlasiet ierakstu.
    3. Noklikšķiniet uz **Tests**. Sistēma novērtē ierakstu, lai noteiktu, vai tas atbilst jūsu definētajiem nosacījumiem.
    4. Noklikšķiniet uz **Labi** vai **Atcelt**, lai atgrieztos formā **Rekvizīti**.

7. Sarakstā **Automātiskās pabeigšanas darbība** atlasiet darbību, kāda sistēmai būtu jāveic ar dokumentu.

## <a name="specify-when-notifications-are-sent"></a>Norādīt, kad tiek sūtīti paziņojumi

Varat lietotājiem nosūtīt paziņojumus, kad dokuments ir apstiprināts, noraidīts, deleģēts vai eskalēts vai kad ir pieprasītas izmaiņas. Veiciet šīs darbības, lai norādītu, kad paziņojumi tiek sūtīti un kam tie tiek sūtīti.

1. Kreisajā rūtī noklikšķiniet uz **Paziņojumi**.
2. Atzīmējiet izvēles rūtiņu pie notikumiem, lai sūtītu paziņojumus par:

    - **Deleģēt** — ja dokuments ir piešķirts citam lietotājam apstiprināšanai.
    - **Eskalēt** — ja piešķirtais lietotājs nav veicis darbību ar dokumentu atvēlētajā laika.
    - **Apstiprināt** — ja dokuments ir apstiprināts.
    - **Noraidīt** — ja dokuments ir noraidīts.
    - **Pieprasīt izmaiņas** — ja piešķirtais lietotājs ir pieprasījis izmaiņas iesniegtajā dokumentā.

3. Atlasiet tāda notikuma rindu, kuru atlasījāt 2. darbībā.
4. Noklikšķiniet uz cilnes **Paziņojuma teksts**.
5. Tekstlodziņā ievadiet paziņojuma tekstu.
6. Lai personalizētu tekstu, varat ievietot vietturus, kas tiks nomainīti ar attiecīgajiem datiem, kad tie tiks parādīti lietotājiem. Lai ievietotu vietturi, rīkojieties šādi:

    1. Noklikšķiniet tekstlodziņā tajā atrašanās vietā, kur vēlaties ievietot vietturi.
    2. Noklikšķiniet uz **Ievietot vietturi**.
    3. Parādītajā sarakstā atlasiet vietturi, kuru ievietot.
    4. Noklikšķiniet uz **Ievietot**.

7. Lai pievienotu paziņojuma tulkojumus, noklikšķiniet uz **Tulkojumi**. Parādītajā formā veiciet šādas darbības:

    1. Noklikšķiniet uz **Pievienot**.
    2. Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.
    3. Tekstlodziņā **Tulkotais teksts** ievadiet tekstu.
    4. Lai personalizētu tekstu, ievietojiet vietturus.
    5. Noklikšķiniet uz **Aizvērt**.

8. Noklikšķiniet uz cilnes **Saņēmējs**.
9. Norādīt, kam tiek sūtīti paziņojumi. Atlasiet vienu no tālāk redzamajā tabulā minētajām opcijām un pēc tam veiciet papildu darbības attiecīgajai opcijai, pirms pārejat uz 10. darbību.

    <table>
    <thead>
    <tr>
    <th>Opcija</th>
    <th>Paziņojuma adresāti</th>
    <th>Papildu transakcijas</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><strong>Dalībnieks</strong></td>
    <td>Lietotāji, kuri ir piešķirti noteiktai grupai vai lomai</td>
    <td>
    <ol>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Dalībnieks</strong>, noklikšķiniet uz cilnes <strong>Pēc lomas</strong>.</li>
    <li>Sarakstā <strong>Dalībnieka tips</strong> atlasiet grupas vai lomas veidu, kurai nosūtīt paziņojumus.</li>
    <li>Sarakstā <strong>Dalībnieks</strong> atlasiet grupu vai lomu, kurai nosūtīt paziņojumus.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><strong>Darbplūsmas lietotājs</strong></td>
    <td>Lietotāji, kuri piedalās pašreizējā darbplūsmā</td>
    <td>
    <ol>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Darbplūsmas lietotājs</strong>, noklikšķiniet uz cilnes <strong>Darbplūsmas lietotājs</strong>.</li>
    <li>Sarakstā <strong>Darbplūsmas lietotājs</strong> atlasiet lietotāju, kas piedalās attiecīgajā darbplūsmā.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><strong>Lietotājs</strong></td>
    <td>Īpaši lietotāji</td>
    <td>
    <ol>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Lietotājs</strong>, noklikšķiniet uz cilnes <strong>Lietotājs</strong>.</li>
    <li>Atlasiet lietotājus, kuriem sūtīt paziņojumus, un pēc tam pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. Atkārtojiet 3.–9. darbību katram notikumam, ko atlasījāt 2. darbībā.

## <a name="specify-a-final-approver"></a> Norādiet pēdējo apstiprinātāju

Varat norādīt galīgo apstiprinātāju scenārijiem, kuros apstiprinātājs ir persona, kas iesniegusi dokumentu apstiprināšanai, un tiek izmantota “neatļauta apstiprināšana, ko veic iesniedzējs”. Lai norādītu galīgo apstiprinātāju, veiciet šādas darbības.

1. Darbplūsmas redaktorā ar peles labo pogu noklikšķiniet uz apstiprināšanas elementa un pēc tam atlasiet **Rekvizīti**, lai atvērtu formu **Rekvizīti**.
2. Kreisajā rūtī noklikšķiniet uz **Papildu iestatījumi**.
3. Atzīmējiet izvēles rūtiņu **Izmantot galīgo apstiprinātāju**.
4. Sarakstā atlasiet lietotāju, kurš būs galīgais apstiprinātājs.

## <a name="set-a-time-limit"></a>Laika robežas iestatīšana

Veiciet šīs darbības, ja apstiprināšanas process ir jāpabeidz noteiktā laikā.

> [!NOTE]
> Šajās darbībās izvēlētās opcijas tiks lietotas neatkarīgi no opcijām, kas atlasītas katra apstiprināšanas soļa apgabalā **Piešķire** un **Eskalācija**.

1. Kreisajā rūtī noklikšķiniet uz **Papildu iestatījumi**.
2. Atzīmējiet izvēles rūtiņu **Iestatīt darbplūsmas** **elementa** laika ierobežojumu.
3. Laukā **Ilgums** norādiet, kad apstiprināšanas process ir jāpabeidz. Izvēlieties vienu no šīm opcijām:

    - **Stundas** — ievadiet stundu skaitu, pēc kurām apstiprināšanas procesam jābūt pabeigtam. Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.
    - **Dienas** — ievadiet dienu skaitu, pēc kurām apstiprināšanas procesam jābūt pabeigtam. Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.
    - **Nedēļas** — ievadiet nedēļu skaitu, pēc kurām apstiprināšanas procesam jābūt pabeigtam.
    - **Mēneši** — izvēlieties dienu un nedēļu, līdz kurai ir jāpabeidz apstiprināšanas process. Piemēram, iespējams, vēlēsieties, lai apstiprināšanas process būtu pabeigts līdz mēneša trešās nedēļas piektdienai.
    - **Gadi** — izvēlieties dienu, nedēļu un mēnesi, līdz kuram ir jāpabeidz apstiprināšanas process. Piemēram, iespējams, vēlēsieties, lai apstiprināšanas process būtu pabeigts līdz decembra trešās nedēļas piektdienai.

4. Ja laika ierobežojums ir pārsniegts, sistēma veiks darbību ar dokumentu. Sarakstā **Darbība** atlasiet darbību, kāda sistēmai būtu jāveic.

## <a name="specify-which-actions-are-available-to-the-user"></a>Norādiet, kuras darbības ir pieejamas lietotājam

Kad dokuments ir piešķirts lietotājam apstiprināšanai, lietotājam ar šo dokumentu jārīkojas. Izpildiet šīs darbības, lai norādītu, kuras darbības lietotājs var veikt ar iesniegto dokumentu.

1. Kreisajā rūtī noklikšķiniet uz **Papildu iestatījumi**.
2. Atzīmējiet izvēles rūtiņu **Apstiprināt**, ja lietotājs var apstiprināt dokumentu.
3. Atzīmējiet izvēles rūtiņu **Noraidīt**, ja lietotājs var noraidīt dokumentu.
4. Atzīmējiet izvēles rūtiņu **Pieprasīt izmaiņas**, ja lietotājs var pieprasīt izmaiņas dokumentā.
5. Atzīmējiet izvēles rūtiņu **Deleģēt**, ja lietotājs var piešķirt dokumentu citam lietotājam apstiprināšanai.

> [!NOTE]
> Izvēles rūtiņa **Iespējot darbības no darbu saraksta uzņēmuma portālā** ir novecojusi.

## <a name="configure-the-approval-steps"></a> Apstiprinājuma darbību konfigurēšana

Apstiprināšanas process sastāv no apstiprināšanas darbībām. Veiciet šādu procedūru, lai pievienotu darbības apstiprināšanas procesam un konfigurētu darbības.

1. Darbplūsmas redaktorā veiciet dubultklikšķi uz apstiprināšanas procesa. Darbplūsmas redaktorā tiek parādītas apstiprināšanas procesa darbības.
2. Lai pievienotu apstiprināšanas darbību, velciet darbību no apgabala **Darbplūsmas elementi** uz audekla.
3. Lai konfigurētu apstiprināšanas darbību, skatiet sadaļu [Apstiprinājuma darbību konfigurēšana darbplūsmā](configure-approval-step-workflow.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]