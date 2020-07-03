---
title: Manuālu lēmumu konfigurēšana darbplūsmā
description: Šajā tēmā ir paskaidrots, kā konfigurēt manuāla lēmuma rekvizītus.
author: sericks007
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 130cb50369c13bc3478340023c94f169ee5250cf
ms.sourcegitcommit: a5009c8958037afbaa1dd4f1469255b187ced93a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2020
ms.locfileid: "3455037"
---
# <a name="configure-manual-decisions-in-a-workflow"></a>Manuālu lēmumu konfigurēšana darbplūsmā

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā konfigurēt manuāla lēmuma rekvizītus.

Lai konfigurētu manuālu lēmumu darbplūsmas redaktorā, ar peles labo taustiņu noklikšķiniet uz manuālā lēmuma un pēc tam noklikšķiniet uz **Rekvizīti**, lai atvērtu lapu **Rekvizīti**. Pēc tam izmantojiet tālāk aprakstītās procedūras, lai konfigurētu manuālā lēmuma rekvizītus.

## <a name="name-the-decision"></a>Lēmuma nosaukums

Izpildiet tālākos norādījumus, lai ievadītu manuālā lēmuma nosaukumu.

1. Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.
2. Laukā **Nosaukums** ievadiet unikālu manuālā lēmuma nosaukumu.

## <a name="enter-a-subject-line-and-instructions"></a>Ievadiet tēmas rindu un instrukcijas

Jums jānorāda temata rinda un instrukcijas lietotājiem, kas piešķirti manuālajam lēmumam. Piemēram, ja konfigurējat pirkšanas pieprasījumu lēmumu, attiecīgajam lēmumam piešķirtais lietotājs redz tēmas rindu un instrukcijas lapā **Pirkšanas pieprasījumi**. Tēmas rinda tiek parādīta lapā esošajā ziņojumu joslā. Lietotājs var noklikšķināt uz ziņojumu joslā redzamās ikonas, lai skatītu instrukcijas. Veiciet šīs darbības, lai ievadītu tēmas rindu un instrukcijas.

1. Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.
2. Cilnes **Instrukcijas** laukā **Darbplūsmas elementa tēma** ievadiet tēmas rindu.
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

## <a name="specify-the-possible-outcomes-of-a-decision"></a>Norādiet iespējamos lēmuma iznākumus

Parasti, ja dokuments tiek piešķirts lēmumu pieņēmējam, tam tiek uzdots jautājums. Atbilde uz šo jautājumu parasti ir **Jā** vai **Nē**, vai **Patiess** vai **Aplams**. Veiciet šīs darbības, lai norādītu iespējamos manuālā lēmuma iznākumus.

1. Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.
2. Cilnes **Iznākumi** laukā **1. iznākums** ievadiet iznākuma nosaukumu vai opciju.
3. Lai pievienotu iznākuma tulkojumus, rīkojieties šādi:

    1. Noklikšķiniet uz **Tulkojumi**.
    2. Parādītajā lapā noklikšķiniet uz **Pievienot**.
    3. Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.
    4. Laukā **Tulkotais teksts** ievadiet tekstu.
    5. Noklikšķiniet uz **Aizvērt**.

4. Laukā **2. iznākums** ievadiet iznākuma nosaukumu vai opciju.
5. Lai pievienotu iznākuma tulkojumus, rīkojieties šādi:

    1. Noklikšķiniet uz **Tulkojumi**.
    2. Parādītajā lapā noklikšķiniet uz **Pievienot**.
    3. Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.
    4. Laukā **Tulkotais teksts** ievadiet tekstu.
    5. Noklikšķiniet uz **Aizvērt**.

## <a name="specify-when-notifications-are-sent"></a>Norādīt, kad tiek sūtīti paziņojumi

Varat nosūtīt lietotājiem paziņojumus, ja lēmums ir pieņemts, deleģēts vai eskalēts. Veiciet šīs darbības, lai norādītu, kad paziņojumi tiek sūtīti un kam tie tiek sūtīti.

1. Kreisajā rūtī noklikšķiniet uz **Paziņojumi**.
2. Atzīmējiet izvēles rūtiņu pie notikumiem, par kuriem tiek sūtīti paziņojumi:

    - **\[1. izvēle\]**  — piešķirtais lietotājs ir atlasījis vienumu **\[1. izvēle\]**.
    - **\[2. izvēle\]**  — piešķirtais lietotājs ir atlasījis vienumu **\[2. izvēle\]**.
    - **Deleģēt**— piešķirtais lietotājs lēmumu ir piešķīris citam lietotājam.
    - **Eskalēt** — piešķirtais lietotājs nav pieņēmis lēmumu atvēlētajā laikā.

3. Atlasiet tāda notikuma rindu, kuru atlasījāt 2. darbībā.
4. Cilnē **Paziņojuma teksts**, tekstlodziņā ievadiet paziņojuma tekstu.
5. Lai personalizētu paziņojumu, varat ievadīt vietturus. Vietturi tiks aizvietoti ar atbilstošiem datiem, kad paziņojums tiks parādīts lietotājiem. Veiciet šīs darbības, lai ievietotu vietturi:

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
    <li>Sarakstā <strong>Dalībnieks</strong> atlasiet grupu, kurai nosūtīt paziņojumus.</li>
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

## <a name="assign-a-decision"></a>Lēmuma piešķiršana

Veiciet šīs darbības, lai norādītu personu, kurai jāpiešķir manuālais lēmums.

1. Kreisajā rūtī noklikšķiniet uz **Piešķire**.
2. Cilnē **Piešķires tips** atlasiet vienu no tālāk redzamajā tabulā minētajām opcijām un pēc tam veiciet papildu darbības attiecīgajai opcijai, pirms pārejat uz 3. darbību.

    <table>
    <thead>
    <tr>
    <th>Opcija</th>
    <th>Lietotāji, kuriem ir piešķirts lēmums</th>
    <th>Papildu transakcijas</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Dalībnieks</td>
    <td>Lietotāji, kuri ir piešķirti noteiktai grupai vai lomai</td>
    <td>
    <ol>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Dalībnieks</strong>, cilnes <strong>Pēc lomas</strong> sarakstā <strong>Dalībnieka tips</strong> atlasiet grupas tipu vai lomu, kurai piešķirt lēmumu.</li>
    <li>Sarakstā <strong>Dalībnieks</strong> atlasiet grupu vai lomu, kurai piešķirt lēmumu.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Hierarhija</td>
    <td>Lietotāji īpašā organizācijas hierarhijā</td>
    <td>
    <ol>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Hierarhija</strong>, cilnes <strong>Hierarhijas atlase</strong> sarakstā <strong>Hierarhijas tips</strong> atlasiet hierarhijas tipu, kuram piešķirt lēmumu.</li>
    <li>Sistēmai no hierarhijas ir jāizgūst lietotāju vārdu diapazons. Šie vārdi norāda, kuriem lietotājiem var piešķirt attiecīgo lēmumu. Veiciet šīs darbības, lai norādītu sistēmas izgūto lietotāju vārdu diapazona sākumu un beigas: <ol>
    <li>Lai norādītu sākumu, atlasiet kādu personu sarakstā <strong>Sākt no</strong>.</li>
    <li>Lai norādītu beigas, noklikšķiniet uz <strong>Pievienot nosacījumu</strong>. Pēc tam ievadiet nosacījumu, kas nosaka, kurā vietā hierarhijā sistēma pārtrauc vārdu izgūšanu.</li>
    </ol>
    </li>
    <li>Cilnē <strong>Hierarhijas opcijas</strong> norādiet attiecīgajā diapazonā esošos lietotājus, kuriem lēmums jāpiešķir: <ul>
    <li><strong>Piešķirt visiem izgūtajiem lietotājiem</strong> — lēmums tiek piešķirts visiem diapazonā esošajiem lietotājiem.</li>
    <li><strong>Piešķirt tikai pēdējam izgūtajam lietotājam</strong> — lēmums tiek piešķirts tikai pēdējam lietotājam diapazonā.</li>
    <li><strong>Neiekļaut lietotājus, kuri atbilst šādiem nosacījumiem</strong> — lēmums netiek piešķirts diapazonā esošajiem lietotājiem, kuri atbilst konkrētam nosacījumam. Lai norādītu nosacījumu, noklikšķiniet uz <strong>Pievienot nosacījumu</strong>.</li>
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
    <li>Sarakstā <strong>Pieejamie lietotāji</strong> ir ietverti visi lietotāji. Atlasiet lietotājus, kuriem piešķirt lēmumu, un pēc tam pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. Cilnes **Laika limits** laukā **Ilgums** norādiet, cik ilgs laiks ir dots lietotājam, lai pieņemtu lēmumu. Izvēlieties vienu no šīm opcijām:

    - **Stundas** — ievadiet stundu skaitu, kuru laikā lietotājam ir jāpieņem lēmums. Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.
    - **Dienas** — ievadiet dienu skaitu, kuru laikā lietotājam ir jāpieņem lēmums. Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.
    - **Nedēļas** — ievadiet nedēļu skaitu, kuru laikā lietotājam ir jāpieņem lēmums.
    - **Mēneši** — izvēlieties dienu un nedēļu, līdz kurai lietotājam ir jāpieņem lēmums. Piemēram, iespējams, vēlēsities, lai lietotājs pieņemtu lēmumu līdz mēneša trešās nedēļas piektdienai.
    - **Gadi** — izvēlieties dienu, nedēļu un mēnesi līdz kuram lietotājam ir jāpieņem lēmums. Piemēram, iespējams, vēlēsities, lai lietotājs pieņemtu lēmumu līdz decembra trešās nedēļas piektdienai.

    Ja lietotājs nepieņem lēmumu atvēlētajā laikā, lēmums ir nokavēts. Nokavēts lēmums tiek eskalēts, pamatojoties uz opcijām, kas ir atlasītas lapas apgabalā **Eskalācija**.

## <a name="specify-what-happens-when-a-decision-is-overdue"></a>Norādiet, kas notiek, ja lēmums nokavēts

Ja lietotājs nepieņem lēmumu atvēlētajā laikā, lēmums ir nokavēts. Lēmumu, kas ir nokavēts, var eskalēt vai automātiski piešķirt citam lietotājam. Veiciet šīs darbības, lai eskalētu lēmumu, ja tas ir nokavēts.

1. Kreisajā rūtī noklikšķiniet uz **Eskalācija**.
2. Atzīmējiet izvēles rūtiņu **Izmantot eskalācijas ceļu**, lai izveidotu eskalācijas ceļu. Sistēma automātiski piešķirs lēmumu lietotājiem, kuri ir norādīti eskalācijas ceļā. Piemēram, šajā tabulā ir attēlots eskalācijas ceļš.

    | Secība | Eskalācijas ceļš            |
    |----------|----------------------------|
    | 1.        | Piešķirt: Lindai           |
    | 2.        | Piešķirt: Zanei            |
    | 3.        | Gala darbība: \[1. izvēle\] |

    Šajā piemērā sistēma piešķir nokavēto lēmumu Lindai. Ja Linda nepieņem lēmumu atvēlētajā laikā, sistēma piešķir lēmumu Zanei. Ja Zane nepieņem lēmumu atvēlētajā laikā, sistēma kā lēmumu atlasa vienumu **\[1. izvēle\]**.

3. Lai pievienotu lietotāju eskalācijas ceļam, noklikšķiniet uz **Pievienot eskalāciju**. Atlasiet vienu no tālāk redzamajā tabulā minētajām opcijām un pēc tam veiciet papildu darbības attiecīgajai opcijai, pirms pārejat uz 4. darbību.

    <table>
    <thead>
    <tr>
    <th>Opcija</th>
    <th>Lietotāji, kuriem tiek eskalēts lēmums</th>
    <th>Papildu transakcijas</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Hierarhija</td>
    <td>Lietotāji īpašā organizācijas hierarhijā</td>
    <td>
    <ol>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Hierarhija</strong>, cilnes <strong>Hierarhijas atlase</strong> sarakstā <strong>Hierarhijas tips</strong> atlasiet hierarhijas tipu, uz kuru eskalēt lēmumu.</li>
    <li>Sistēmai no hierarhijas ir jāizgūst lietotāju vārdu diapazons. Šie vārdi norāda, kuriem lietotājiem var eskalēt lēmumu. Veiciet šīs darbības, lai norādītu sistēmas izgūto lietotāju vārdu diapazona sākumu un beigas: <ol>
    <li>Lai norādītu sākumu, atlasiet kādu personu sarakstā <strong>Sākt no</strong>.</li>
    <li>Lai norādītu beigas, noklikšķiniet uz <strong>Pievienot nosacījumu</strong>. Pēc tam ievadiet nosacījumu, kas nosaka, kurā vietā hierarhijā sistēma pārtrauc vārdu izgūšanu.</li>
    </ol>
    </li>
    <li>Cilnē <strong>Hierarhijas opcijas</strong> norādiet attiecīgajā diapazonā esošos lietotājus, kuriem jāveic lēmuma eskalācija: <ul>
    <li><strong>Piešķirt visiem izgūtajiem lietotājiem</strong> — lēmums tiek eskalēts visiem diapazonā esošajiem lietotājiem.</li>
    <li><strong>Piešķirt tikai pēdējam izgūtajam lietotājam</strong> — lēmums tiek eskalēts tikai pēdējam lietotājam diapazonā.</li>
    <li><strong>Neiekļaut lietotājus, kuri atbilst šādiem nosacījumiem</strong> — lēmums netiek eskalēts diapazonā esošajiem lietotājiem, kuri atbilst konkrētam nosacījumam. Lai norādītu nosacījumu, noklikšķiniet uz <strong>Pievienot nosacījumu</strong>.</li>
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
    <li>Sarakstā <strong>Pieejamie lietotāji</strong> ir ietverti visi lietotāji. Atlasiet lietotājus, kuriem eskalēt lēmumu, un pēc tam pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. Cilnes **Laika limits** laukā **Ilgums** norādiet, cik ilgs laiks ir dots lietotājam, lai pieņemtu lēmumu. Izvēlieties vienu no šīm opcijām:

    - **Stundas** — ievadiet stundu skaitu, kuru laikā lietotājam ir jāpieņem lēmums. Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.
    - **Dienas** — ievadiet dienu skaitu, kuru laikā lietotājam ir jāpieņem lēmums. Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.
    - **Nedēļas** — ievadiet nedēļu skaitu, kuru laikā lietotājam ir jāpieņem lēmums.
    - **Mēneši** — izvēlieties dienu un nedēļu, līdz kurai lietotājam ir jāpieņem lēmums. Piemēram, iespējams, vēlēsities, lai lietotājs pieņemtu lēmumu līdz mēneša trešās nedēļas piektdienai.
    - **Gadi** — izvēlieties dienu, nedēļu un mēnesi līdz kuram lietotājam ir jāpieņem lēmums. Piemēram, iespējams, vēlēsities, lai lietotājs pieņemtu lēmumu līdz decembra trešās nedēļas piektdienai.

5. Atkārtojiet 3.–4. darbību katram lietotājam, kurš jāpievieno eskalācijas ceļam. Jūs varat mainīt lietotāju secību.
6. Ja eskalācijas ceļā norādītie lietotāji nepieņem lēmumu atvēlētajā laikā, sistēma pieņem lēmumu. Lai norādītu opciju, ko sistēma izvēlas, atlasiet rindu **Darbība** un pēc tam cilnē **Beigu darbība** atlasiet opciju.

## <a name="set-a-time-limit"></a>Laika robežas iestatīšana

Veiciet šīs darbības, ja lēmums ir jāpieņem noteiktā laikā.

> [!NOTE]
> Šajā procedūrā izvēlētās opcijas tiks lietotas neatkarīgi no opcijām, kas atlasītas lapas apgabalos **Piešķire** un **Eskalācija**.

1. Kreisajā rūtī noklikšķiniet uz **Papildu iestatījumi**.
2. Atzīmējiet izvēles rūtiņu **Iestatīt darbplūsmas elementa laika ierobežojumu**.
3. Laukā **Ilgums** norādiet, kad lēmums ir jāpieņem. Izvēlieties vienu no šīm opcijām:

    - **Stundas** — ievadiet stundu skaitu. Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.
    - **Dienas** — ievadiet dienu skaitu. Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.
    - **Nedēļas** — ievadiet nedēļu skaitu.
    - **Mēneši** — izvēlieties dienu un nedēļu, līdz kurai ir jāpieņem lēmums. Piemēram, iespējams, vēlēsities, lai lēmums tiktu pieņemts līdz mēneša trešās nedēļas piektdienai.
    - **Gadi** — izvēlieties dienu, nedēļu un mēnesi, līdz kuram ir jāpieņem lēmums. Piemēram, iespējams, vēlēsities, lai lēmums tiktu pieņemts līdz decembra trešās nedēļas piektdienai.

4. Ja laika ierobežojums ir pārsniegts, sistēma pieņems lēmumu. Sarakstā **Darbība** atlasiet opciju, kura sistēmai būtu jāizvēlas.
