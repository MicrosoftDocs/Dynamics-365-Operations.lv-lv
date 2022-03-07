---
title: Manuālu uzdevumu konfigurēšana darbplūsmā
description: Šajā tēmā ir paskaidrots, kā konfigurēt manuāla uzdevuma rekvizītus.
author: ChrisGarty
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4be7f0ee5e487185033b7ccb9a2b0a91eb4a36c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747859"
---
# <a name="configure-manual-tasks-in-a-workflow"></a>Manuālu uzdevumu konfigurēšana darbplūsmā

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā konfigurēt manuāla uzdevuma rekvizītus.

Lai konfigurētu manuālu uzdevumu darbplūsmas redaktorā, ar peles labo taustiņu noklikšķiniet uz uzdevuma un pēc tam noklikšķiniet uz **Rekvizīti**, lai atvērtu lapu **Rekvizīti**. Pēc tam izmantojiet tālāk aprakstītās procedūras, lai konfigurētu manuālā uzdevuma rekvizītus.

## <a name="name-the-task"></a>Nosaukuma piešķiršana uzdevumam

Izpildiet tālākos norādījumus, lai ievadītu manuālā uzdevuma nosaukumu.

1. Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.
2. Laukā **Nosaukums** uzdevumam ievadiet unikālu nosaukumu.

## <a name="enter-a-subject-line-and-instructions"></a>Ievadiet tēmas rindu un instrukcijas

Jums jānorāda tēmas rinda un instrukcijas lietotājiem, kuri piešķirti šim uzdevumam. Piemēram, ja konfigurējat pirkšanas pieprasījumu uzdevumu, attiecīgajam uzdevumam piešķirtais lietotājs redz tēmas rindu un instrukcijas lapā **Pirkšanas pieprasījumi**. Tēmas rinda tiek parādīta lapā esošajā ziņojumu joslā. Lietotājs var noklikšķināt uz ziņojumu joslā redzamās ikonas, lai skatītu instrukcijas. Veiciet šīs darbības, lai ievadītu tēmas rindu un instrukcijas.

1. Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.
2. Laukā **Darbplūsmas elementa tēma** ievadiet tēmas rindu.
3. Lai personalizētu tēmas rindu, var ievadīt vietturus. Vietturi tiks aizvietoti ar atbilstošiem datiem, kad tēmas rinda tiks parādīta lietotājiem. Veiciet šīs darbības, lai ievietotu vietturi:

    1. Tekstlodziņā noklikšķiniet uz vietas, kur jāparādās vietturim.
    2. Noklikšķiniet uz **Ievietot vietturi**.
    3. Parādītajā sarakstā atlasiet vietturi, kuru ievietot.
    4. Noklikšķiniet uz **Ievietot**.

4. Lai pievienotu tēmas rindas tulkojumus, rīkojieties šādi:

    1. Noklikšķiniet uz **Tulkojumi**.
    2. Parādītajā lapā noklikšķiniet uz **Pievienot**.
    3. Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.
    4. Laukā **Tulkotais teksts** ievadiet tekstu.
    5. Lai personalizētu tekstu, var ievadīt vietturus, kā aprakstīts 3. darbībā.
    6. Noklikšķiniet uz **Aizvērt**.

5. Laukā **Darbplūsmas elementa instrukcijas** ievadiet instrukcijas.
6. Lai personalizētu instrukcijas, var ievadīt vietturus. Vietturi tiks aizvietoti ar atbilstošiem datiem, kad instrukcijas tiks parādītas lietotājiem. Veiciet šīs darbības, lai ievietotu vietturi:

    1. Tekstlodziņā noklikšķiniet uz vietas, kur jāparādās vietturim.
    2. Noklikšķiniet uz **Ievietot vietturi**.
    3. Parādītajā sarakstā atlasiet vietturi, kuru ievietot.
    4. Noklikšķiniet uz **Ievietot**.

7. Lai pievienotu instrukciju tulkojumus, rīkojieties šādi:

    1. Noklikšķiniet uz **Tulkojumi**.
    2. Parādītajā lapā noklikšķiniet uz **Pievienot**.
    3. Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.
    4. Laukā **Tulkotais teksts** ievadiet tekstu.
    5. Lai personalizētu tekstu, var ievadīt vietturus, kā aprakstīts 6. darbībā.
    6. Noklikšķiniet uz **Aizvērt**.

## <a name="assign-the-task"></a>Uzdevuma piešķiršana

Veiciet šīs darbības, lai norādītu personu, kurai jāpiešķir manuālais uzdevums.

1. Kreisajā rūtī noklikšķiniet uz **Piešķire**.
2. Cilnē **Piešķires tips** atlasiet vienu no tālāk redzamajā tabulā minētajām opcijām un pēc tam veiciet papildu darbības attiecīgajai opcijai, pirms pārejat uz 3. darbību.

    <table>
    <thead>
    <tr>
    <th>Opcija</th>
    <th>Lietotāji, kuriem ir piešķirts uzdevums</th>
    <th>Papildu transakcijas</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Dalībnieks</td>
    <td>Lietotāji, kuri ir piešķirti noteiktai grupai vai lomai</td>
    <td>
    <ol>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Dalībnieks</strong>, cilnes <strong>Pēc lomas</strong> sarakstā <strong>Dalībnieka tips</strong> atlasiet grupas tipu vai lomu, kurai piešķirt uzdevumu.</li>
    <li>Sarakstā <strong>Dalībnieks</strong> atlasiet grupu vai lomu, kurai piešķirt uzdevumu.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Hierarhija</td>
    <td>Lietotāji īpašā organizācijas hierarhijā</td>
    <td>
    <ol>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Hierarhija</strong>, cilnes <strong>Hierarhijas atlase</strong> sarakstā <strong>Hierarhijas tips</strong> atlasiet hierarhijas tipu, kuram piešķirt uzdevumu.</li>
    <li>Sistēmai no hierarhijas ir jāizgūst lietotāju vārdu diapazons. Šie vārdi norāda, kuriem lietotājiem var piešķirt attiecīgo uzdevumu. Veiciet šīs darbības, lai norādītu sistēmas izgūto lietotāju vārdu diapazona sākumu un beigas: <ol>
    <li>Lai norādītu sākumu, atlasiet kādu personu sarakstā <strong>Sākt no</strong>.</li>
    <li>Lai norādītu beigas, noklikšķiniet uz <strong>Pievienot nosacījumu</strong>. Pēc tam ievadiet nosacījumu, kas nosaka, kurā vietā hierarhijā sistēma pārtrauc vārdu izgūšanu.</li>
    </ol>
    </li>
    <li>Cilnē <strong>Hierarhijas opcijas</strong> norādiet attiecīgajā diapazonā esošos lietotājus, kuriem uzdevums jāpiešķir: <ul>
    <li><strong>Piešķirt visiem izgūtajiem lietotājiem</strong> — uzdevums tiek piešķirts visiem diapazonā esošajiem lietotājiem.</li>
    <li><strong>Piešķirt tikai pēdējam izgūtajam lietotājam</strong> — uzdevums tiek piešķirts tikai pēdējam lietotājam diapazonā.</li>
    <li><strong>Neiekļaut lietotājus, kuri atbilst šādiem nosacījumiem</strong> — uzdevums netiek piešķirts diapazonā esošajiem lietotājiem, kuri atbilst konkrētam nosacījumam. Lai norādītu nosacījumu, noklikšķiniet uz <strong>Pievienot nosacījumu</strong>.</li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Darbplūsmas lietotājs</td>
    <td>Lietotāji pašreizējā darbplūsmā</td>
    <td>
    <ul>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Darbplūsmas lietotājs</strong>, cilnes <strong>Darbplūsmas lietotājs</strong> sarakstā <strong>Darbplūsmas lietotājs</strong> atlasiet lietotāju, kas piedalās attiecīgajā darbplūsmā.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Lietotājs</td>
    <td>Īpaši lietotāji</td>
    <td>
    <ol>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Lietotājs</strong>, noklikšķiniet uz cilnes <strong>Lietotājs</strong>.</li>
    <li>Sarakstā <strong>Pieejamie lietotāji</strong> ir ietverti visi lietotāji. Atlasiet lietotājus, kuriem piešķirt uzdevumu, un pēc tam pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Rinda</td>
    <td>Darba vienumu rinda</td>
    <td>
    <ol>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Rinda</strong>, noklikšķiniet uz cilnes <strong>Balstīts uz rindu</strong>.</li>
    <li>Lai uzdevumu piešķirtu noteiktai rindai, rīkojieties šādi: <ol>
    <li>Sarakstā <strong>Rindas tips</strong> atlasiet <strong>Darba vienumu rindas</strong>.</li>
    <li>Sarakstā <strong>Rindas nosaukums</strong> atlasiet rindu.</li>
    </ol>
    </li>
    <li>Ja konkrētam nosacījumam jānosaka, kurai rindai uzdevums tiek piešķirts, rīkojieties šādi: <ol>
    <li>Sarakstā <strong>Rindas tips</strong> atlasiet <strong>Nosacījuma darba vienumu rindas</strong>.</li>
    <li>Sarakstā <strong>Rindas nosaukums</strong> atlasiet <strong>Nosacījumu rinda</strong>.</li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] Šī opcija tiek izmantota tikai dažām darbplūsmām, piemēram, Pieteikumu pārvaldība.</blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. Cilnes **Laika limits** laukā **Ilgums** norādiet, cik ilgs laiks ir dots lietotājam, lai pabeigtu uzdevumu. Izvēlieties vienu no šīm opcijām:

    - **Stundas** — ievadiet stundu skaitu, kuru laikā lietotājam ir jāpabeidz uzdevums. Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.
    - **Dienas** — ievadiet dienu skaitu, kuru laikā lietotājam ir jāpabeidz uzdevums. Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.
    - **Nedēļas** — ievadiet nedēļu skaitu, kuru laikā lietotājam ir jāpabeidz uzdevums.
    - **Mēneši** — izvēlieties dienu un nedēļu, līdz kurai lietotājam ir jāpabeidz uzdevums. Piemēram, iespējams, vēlēsities, lai lietotājs pabeigtu uzdevumu līdz mēneša trešās nedēļas piektdienai.
    - **Gadi** — izvēlieties dienu, nedēļu un mēnesi, līdz kuram lietotājam ir jāpabeidz uzdevums. Piemēram, iespējams, vēlēsities, lai lietotājs pabeigt uzdevumu līdz decembra trešās nedēļas piektdienai.

    Ja lietotājs nepabeidz uzdevumu atvēlētajā laikā, uzdevums ir nokavēts. Nokavētu uzdevumu var eskalēt, pamatojoties uz opcijām, kas ir atlasītas lapas apgabalā **Eskalācija**.

## <a name="specify-what-happens-when-the-task-is-overdue"></a>Norādiet, kas notiek, ja uzdevums nokavēts

Ja lietotājs nepabeidz manuālo uzdevumu atvēlētajā laikā, uzdevums ir nokavēts. Uzdevumu, kas ir nokavēts, var eskalēt vai automātiski piešķirt citam lietotājam. Veiciet šīs darbības, lai eskalētu uzdevumu, ja tas ir nokavēts.

1. Kreisajā rūtī noklikšķiniet uz **Eskalācija**.
2. Atzīmējiet izvēles rūtiņu **Izmantot eskalācijas ceļu**, lai izveidotu eskalācijas ceļu. Sistēma automātiski piešķirs uzdevumu lietotājiem, kuri ir norādīti eskalācijas ceļā. Piemēram, šajā tabulā ir attēlots eskalācijas ceļš.

    | Secība | Eskalācijas ceļš      |
    |----------|----------------------|
    | 1        | Piešķirt: Lindai     |
    | 2        | Piešķirt: Zanei      |
    | 3        | Pēdējā darbība: noraidīt |

    Šajā piemērā sistēma piešķir nokavēto uzdevumu Lindai. Ja Linda nepabeidz uzdevumu atvēlētajā laikā, sistēma piešķir uzdevumu Zanei. Ja Zane nepabeidz uzdevumu atvēlētajā laikā, sistēma noraida dokumentu, kas tika iesniegts apstrādei.

3. Lai pievienotu lietotāju eskalācijas ceļam, noklikšķiniet uz **Pievienot eskalāciju**. Cilnē **Piešķires tips** atlasiet vienu no tālāk redzamajā tabulā minētajām opcijām un pēc tam veiciet papildu darbības attiecīgajai opcijai, pirms pārejat uz 4. darbību.

    <table>
    <thead>
    <tr>
    <th>Opcija</th>
    <th>Lietotāji, kuriem tiek eskalēts uzdevums</th>
    <th>Papildu transakcijas</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Hierarhija</td>
    <td>Lietotāji īpašā organizācijas hierarhijā</td>
    <td>
    <ol>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Hierarhija</strong>, cilnes <strong>Hierarhijas atlase</strong> sarakstā <strong>Hierarhijas tips</strong> atlasiet hierarhijas tipu, kuram eskalēt uzdevumu.</li>
    <li>Sistēmai no hierarhijas ir jāizgūst lietotāju vārdu diapazons. Šie vārdi norāda, kuriem lietotājiem var eskalēt attiecīgo uzdevumu. Veiciet šīs darbības, lai norādītu sistēmas izgūto lietotāju vārdu diapazona sākumu un beigas: <ol>
    <li>Lai norādītu sākumu, atlasiet kādu personu sarakstā <strong>Sākt no</strong>.</li>
    <li>Lai norādītu beigas, noklikšķiniet uz <strong>Pievienot nosacījumu</strong>. Pēc tam ievadiet nosacījumu, kas nosaka, kurā vietā hierarhijā sistēma pārtrauc vārdu izgūšanu.</li>
    </ol>
    </li>
    <li>Cilnē <strong>Hierarhijas opcijas</strong> norādiet attiecīgajā diapazonā esošos lietotājus, kuriem uzdevums jāeskalē: <ul>
    <li><strong>Piešķirt visiem izgūtajiem lietotājiem</strong> — uzdevums tiek eskalēts visiem diapazonā esošajiem lietotājiem.</li>
    <li><strong>Piešķirt tikai pēdējam izgūtajam lietotājam</strong> — uzdevums tiek eskalēts tikai pēdējam lietotājam diapazonā.</li>
    <li><strong>Neiekļaut lietotājus, kuri atbilst šādiem nosacījumiem</strong> — šis uzdevums netiek eskalēts diapazonā esošajiem lietotājiem, kuri atbilst konkrētam nosacījumam. Lai norādītu nosacījumu, noklikšķiniet uz <strong>Pievienot nosacījumu</strong>.</li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Darbplūsmas lietotājs</td>
    <td>Lietotāji pašreizējā darbplūsmā</td>
    <td>
    <ul>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Darbplūsmas lietotājs</strong>, cilnes <strong>Darbplūsmas lietotājs</strong> sarakstā <strong>Darbplūsmas lietotājs</strong> atlasiet lietotāju, kas piedalās attiecīgajā darbplūsmā.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Lietotājs</td>
    <td>Īpaši lietotāji</td>
    <td>
    <ol>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Lietotājs</strong>, noklikšķiniet uz cilnes <strong>Lietotājs</strong>.</li>
    <li>Sarakstā <strong>Pieejamie lietotāji</strong> ir ietverti visi lietotāji. Atlasiet lietotājus, kuriem eskalēt uzdevumu, un pēc tam pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. Cilnes **Laika limits** laukā **Ilgums** norādiet, cik ilgs laiks ir dots lietotājam, lai pabeigtu uzdevumu. Izvēlieties vienu no šīm opcijām:

    - **Stundas** — ievadiet stundu skaitu, kuru laikā lietotājam ir jāpabeidz uzdevums. Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.
    - **Dienas** — ievadiet dienu skaitu, kuru laikā lietotājam ir jāpabeidz uzdevums. Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.
    - **Nedēļas** — ievadiet nedēļu skaitu, kuru laikā lietotājam ir jāpabeidz uzdevums.
    - **Mēneši** — izvēlieties dienu un nedēļu, līdz kurai lietotājam ir jāpabeidz uzdevums. Piemēram, iespējams, vēlēsities, lai lietotājs pabeigtu uzdevumu līdz mēneša trešās nedēļas piektdienai.
    - **Gadi** — izvēlieties dienu, nedēļu un mēnesi, līdz kuram lietotājam ir jāpabeidz uzdevums. Piemēram, iespējams, vēlēsities, lai lietotājs pabeigt uzdevumu līdz decembra trešās nedēļas piektdienai.

5. Atkārtojiet 3.–4. darbību katram lietotājam, kurš jāpievieno eskalācijas ceļam. Jūs varat mainīt lietotāju secību.
6. Ja eskalācijas ceļā norādītie lietotāji nepabeidz uzdevumu atvēlētajā laikā, sistēma veic darbību ar uzdevumu. Lai norādītu darbību, ko sistēma veic, atlasiet rindu **Darbība** un pēc tam cilnē **Beigu darbība** atlasiet darbību.

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a>Norādiet, kad sistēma automātiski veic darbību ar uzdevumu

Varat konfigurēt sistēmu, lai tā veiktu darbību ar manuālu uzdevumu, ja tiek izpildīti konkrēti nosacījumi. Piemēram, uzdevumam ir nepieciešams, lai nodaļas Izdevumu atskaites dalībnieks pārskatītu čekus, kas ir iesniegti kopā ar izdevumu pārskatu. Saskaņā ar uzņēmuma politiku, šis uzdevums ir jāveic, ja izdevumu pārskata kopsumma ir lielāka par 100 USD. Šādā scenārijā varat konfigurēt sistēmu, lai tā automātiski atzīmētu uzdevumu kā **Pabeigts**, ja kopsumma ir mazāka par 100. Izpildiet šīs darbības, lai norādītu, kad sistēma veic darbības ar manuālo uzdevumu.

1. Kreisajā rūtī noklikšķiniet uz **Automātiskas darbības**.
2. Atzīmējiet izvēles rūtiņu **Iespējot automātiskas darbības**.
3. Noklikšķiniet uz **Pievienot nosacījumu**.
4. Ievadīt nosacījumu.
5. Ievadiet visus nepieciešamos papildu nosacījumus.
6. Lai pārbaudītu, vai ievadītie nosacījumi ir pareizi konfigurēti, rīkojieties šādi:

    1. Noklikšķiniet uz **Tests**.
    2. Lapas **Testēt darbplūsmas nosacījumu** apgabalā **Pārbaudīt nosacījumu** atlasiet ierakstu.
    3. Noklikšķiniet uz **Tests**. Sistēma novērtē ierakstu, lai noteiktu, vai tas atbilst jūsu definētajiem nosacījumiem.
    4. Noklikšķiniet uz **Labi** vai **Atcelt**, lai atgrieztos lapā **Rekvizīti**.

7. Sarakstā **Automātiskās pabeigšanas darbība** atlasiet darbību, kāda sistēmai būtu jāveic ar uzdevumu.

## <a name="specify-when-notifications-are-sent"></a>Norādīt, kad tiek sūtīti paziņojumi

Varat lietotājiem nosūtīt paziņojumus, kad manuālais uzdevums ir deleģēts, eskalēts, pabeigts vai noraidīts vai kad ir pieprasītas izmaiņas. Veiciet šīs darbības, lai norādītu, kad paziņojumi tiek sūtīti un kam tie tiek sūtīti.

1. Kreisajā rūtī noklikšķiniet uz **Paziņojumi**.
2. Atzīmējiet izvēles rūtiņu pie notikumiem, par kuriem tiek sūtīti paziņojumi:

    - **Deleģēt** — uzdevums ir piešķirts citam lietotājam.
    - **Eskalēt** — piešķirtais lietotājs nav pabeidzis uzdevumu atvēlētajā laikā.
    - **Pabeigt** — piešķirtais lietotājs ir pabeidzis uzdevumu.
    - **Noraidīt** — piešķirtais lietotājs ir noraidījis iesniegto dokumentu.
    - **Pieprasīt izmaiņas** — piešķirtais lietotājs ir pieprasījis izmaiņas iesniegtajā dokumentā.

3. Atlasiet tāda notikuma rindu, kuru atlasījāt 2. darbībā.
4. Cilnē **Paziņojuma teksts**, tekstlodziņā ievadiet paziņojuma tekstu.
5. Lai personalizētu paziņojumu, varat ievadīt vietturus. Vietturi tiks aizvietoti ar atbilstošu informāciju, kad paziņojums tiks parādīts lietotājiem. Veiciet šīs darbības, lai ievietotu vietturi:

    1. Tekstlodziņā noklikšķiniet uz vietas, kur jāparādās vietturim.
    2. Noklikšķiniet uz **Ievietot vietturi**.
    3. Parādītajā sarakstā atlasiet vietturi, kuru ievietot.
    4. Noklikšķiniet uz **Ievietot**.

6. Lai pievienotu paziņojuma tulkojumus, rīkojieties šādi:

    1. Noklikšķiniet uz **Tulkojumi**.
    2. Parādītajā lapā noklikšķiniet uz **Pievienot**.
    3. Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.
    4. Laukā **Tulkotais teksts** ievadiet tekstu.
    5. Lai personalizētu tekstu, var ievadīt vietturus, kā aprakstīts 5. darbībā.
    6. Noklikšķiniet uz **Aizvērt**.

7. Cilnē **Adresāts** norādiet personu, kurai paziņojumi tiek nosūtīti. Atlasiet vienu no tālāk redzamajā tabulā minētajām opcijām un pēc tam veiciet papildu darbības attiecīgajai opcijai, pirms pārejat uz 8. darbību.

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
    <td>Dalībnieks</td>
    <td>Lietotāji, kuri ir piešķirti noteiktai grupai vai lomai</td>
    <td>
    <ol>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Dalībnieks</strong>, cilnes <strong>Pēc lomas</strong> sarakstā <strong>Dalībnieka tips</strong> atlasiet grupas tipu vai lomu, kurai nosūtīt paziņojumu.</li>
    <li>Sarakstā <strong>Dalībnieks</strong> atlasiet grupu vai lomu, kurai nosūtīt paziņojumus.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Darbplūsmas lietotājs</td>
    <td>Lietotāji pašreizējā darbplūsmā</td>
    <td>
    <ul>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Darbplūsmas lietotājs</strong>, cilnes <strong>Darbplūsmas lietotājs</strong> sarakstā <strong>Darbplūsmas lietotājs</strong> atlasiet lietotāju, kas piedalās attiecīgajā darbplūsmā.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Lietotājs</td>
    <td>Īpaši lietotāji</td>
    <td>
    <ol>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Lietotājs</strong>, noklikšķiniet uz cilnes <strong>Lietotājs</strong>.</li>
    <li>Sarakstā <strong>Pieejamie lietotāji</strong> ir ietverti visi lietotāji. Atlasiet lietotājus, kuriem sūtīt paziņojumus, un pēc tam pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. Atkārtojiet 3.–7. darbību katram notikumam, ko atlasījāt 2. darbībā.

## <a name="set-a-time-limit"></a>Laika robežas iestatīšana

Veiciet šīs darbības, ja manuālais uzdevums ir jāpabeidz noteiktā laikā.

> [!NOTE]
> Šajā procedūrā izvēlētās opcijas tiks lietotas neatkarīgi no opcijām, kas atlasītas lapas apgabalos **Piešķire** un **Eskalācija**.

1. Kreisajā rūtī noklikšķiniet uz **Papildu iestatījumi**.
2. Atzīmējiet izvēles rūtiņu **Iestatīt darbplūsmas elementa laika ierobežojumu**.
3. Laukā **Ilgums** norādiet, kad uzdevums ir jāpabeidz. Izvēlieties vienu no šīm opcijām:

    - **Stundas** — ievadiet stundu skaitu, kuru laikā uzdevums ir jāpabeidz. Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.
    - **Dienas** — ievadiet dienu skaitu, kuru laikā uzdevums ir jāpabeidz. Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.
    - **Nedēļas** — ievadiet nedēļu skaitu, kuru laikā uzdevums ir jāpabeidz.
    - **Mēneši** — izvēlieties dienu un nedēļu, līdz kurai ir jāpabeidz uzdevums. Piemēram, iespējams, vēlēsieties, lai uzdevums tiktu pabeigts līdz mēneša trešās nedēļas piektdienai.
    - **Gadi** — izvēlieties dienu, nedēļu un mēnesi, līdz kuram ir jāpabeidz uzdevums. Piemēram, iespējams, vēlēsieties, lai uzdevums tiktu pabeigts līdz decembra trešās nedēļas piektdienai.

4. Ja laika ierobežojums ir pārsniegts, sistēma veiks darbību ar uzdevumu. Sarakstā **Darbība** atlasiet darbību, kāda sistēmai būtu jāveic.

## <a name="specify-which-actions-are-available-to-the-user"></a>Norādiet, kuras darbības ir pieejamas lietotājam

Kad manuālais uzdevums ir piešķirts lietotājam, lietotājam ir jāveic darbība ar šo uzdevumu. Izpildiet šīs darbības, lai norādītu, kuras darbības lietotājs var veikt ar uzdevumu.

> [!NOTE]
> Pieejamās darbības var atšķirties atkarībā no tā, kā uzdevums ir projektēts.

1. Kreisajā rūtī noklikšķiniet uz **Papildu iestatījumi**.
2. Atzīmējiet izvēles rūtiņu **Pabeigts**, lai lietotājs varētu atzīmēt šo uzdevumu, izmantojot vienumu **Pabeigts**.
3. Atzīmējiet izvēles rūtiņu **Noraidīt**, lai lietotājs varētu noraidīt iesniegto dokumentu.
4. Atzīmējiet izvēles rūtiņu **Pieprasīt izmaiņas**, lai lietotājs varētu pieprasīt izmaiņu veikšanu iesniegtajā dokumentā.
5. Atzīmējiet izvēles rūtiņu **Deleģēt**, lai lietotājs varētu piešķirt uzdevumu citam lietotājam.
6. Atzīmējiet izvēles rūtiņu **Piešķirt no jauna**, lai lietotājs varētu piešķirt no jauna uzdevumu citam lietotājam darba vienumu rindā.
7. Atzīmējiet izvēles rūtiņu **Nodot izpildei**, lai lietotājs varētu piešķirt no jauna uzdevumu darba vienumu rindā. Pēc tam uzdevumu var pabeigt cits lietotājs.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]