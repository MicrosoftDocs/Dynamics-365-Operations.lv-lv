---
title: Apstiprināšanas darbību konfigurēšana darbplūsmā
description: Šajā rakstā skaidrots, kā konfigurēt apstiprināšanas soļa rekvizītus.
author: ChrisGarty
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d7491c690cce7014f1aca0fb30ff6c3f21f45f9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848698"
---
# <a name="configure-approval-steps-in-a-workflow"></a>Apstiprināšanas darbību konfigurēšana darbplūsmā

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Šajā rakstā skaidrots, kā konfigurēt apstiprināšanas soļa rekvizītus.

Lai konfigurētu apstiprināšanas darbību darbplūsmas redaktorā, ar peles labo taustiņu noklikšķiniet uz apstiprināšanas darbības un pēc tam noklikšķiniet uz **Rekvizīti**, lai atvērtu lapu **Rekvizīti**. Pēc tam izmantojiet tālāk aprakstītās procedūras, lai konfigurētu apstiprināšanas darbības rekvizītus.

## <a name="name-the-step"></a>Nosaukuma piešķiršana solim
Izpildiet tālākos norādījumus, lai ievadītu apstiprināšanas darbības nosaukumu.

1. Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.
2. Laukā **Nosaukums** ievadiet unikālu nosaukumu apstiprināšanas solim.

## <a name="enter-a-subject-line-and-instructions"></a>Ievadiet tēmas rindu un instrukcijas

Jums jānorāda temata rinda un instrukcijas lietotājiem, kas piešķirti apstiprināšanas darbībai. Piemēram, ja konfigurējat pirkšanas pieprasījumu apstiprināšanas darbību, attiecīgajai darbībai piešķirtais lietotājs redz tēmas rindu un instrukcijas lapā **Pirkšanas pieprasījumi**. Tēmas rinda tiek parādīta lapā esošajā ziņojumu joslā. Lietotājs var noklikšķināt uz ziņojumu joslā redzamās ikonas, lai skatītu instrukcijas. Veiciet šīs darbības, lai ievadītu tēmas rindu un instrukcijas.

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

## <a name="assign-the-approval-step"></a>Piešķiriet apstiprināšanas soli

Veiciet šīs darbības, lai norādītu personu, kurai jāpiešķir apstiprināšanas darbība.

1. Kreisajā rūtī noklikšķiniet uz **Piešķire**.
2. Cilnē **Piešķires tips** atlasiet vienu no tālāk redzamajā tabulā minētajām opcijām un pēc tam veiciet papildu darbības attiecīgajai opcijai, pirms pārejat uz 3. darbību.

    <table>
    <thead>
    <tr>
    <th>Opcija</th>
    <th>Lietotāji, kuriem ir piešķirta apstiprināšanas darbība</th>
    <th>Papildu transakcijas</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Dalībnieks</td>
    <td>Lietotāji, kuri ir piešķirti noteiktai grupai vai lomai</td>
    <td>
    <ol>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Dalībnieks</strong>, cilnes <strong>Pēc lomas</strong> sarakstā <strong>Dalībnieka tips</strong> atlasiet grupas tipu vai lomu, kurai piešķirt darbību.</li>
    <li>Sarakstā <strong>Dalībnieks</strong> atlasiet grupu vai lomu, kurai piešķirt darbību.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Hierarhija</td>
    <td>Lietotāji īpašā organizācijas hierarhijā</td>
    <td>
    <ol>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Hierarhija</strong>, cilnes <strong>Hierarhijas atlase</strong> sarakstā <strong>Hierarhijas tips</strong> atlasiet hierarhijas tipu, kurai piešķirt darbību.</li>
    <li>Sistēmai no hierarhijas ir jāizgūst lietotāju vārdu diapazons. Šie vārdi norāda, kuriem lietotājiem var piešķirt attiecīgo darbību. Veiciet šīs darbības, lai norādītu sistēmas izgūto lietotāju vārdu diapazona sākumu un beigas: <ol>
    <li>Lai norādītu sākumu, atlasiet kādu personu sarakstā <strong>Sākt no</strong>.</li>
    <li>Lai norādītu beigas, noklikšķiniet uz <strong>Pievienot nosacījumu</strong>. Pēc tam ievadiet nosacījumu, kas nosaka, kurā vietā hierarhijā sistēma pārtrauc vārdu izgūšanu.</li>
    </ol>
    </li>
    <li>Cilnē <strong>Hierarhijas opcijas</strong> norādiet attiecīgajā diapazonā esošos lietotājus, kuriem darbība jāpiešķir: <ul>
    <li><strong>Piešķirt visiem izgūtajiem lietotājiem</strong> — darbība tiek piešķirta visiem diapazonā esošajiem lietotājiem.</li>
    <li><strong>Piešķirt tikai pēdējam izgūtajam lietotājam</strong> — darbība tiek piešķirta tikai pēdējam lietotājam diapazonā.</li>
    <li><strong>Neiekļaut lietotājus, kuri atbilst šādiem nosacījumiem</strong> — darbība netiek piešķirta diapazonā esošajiem lietotājiem, kuri atbilst konkrētam nosacījumam. Lai norādītu nosacījumu, noklikšķiniet uz <strong>Pievienot nosacījumu</strong>.</li>
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
    <li>Sarakstā <strong>Pieejamie lietotāji</strong> ir ietverti visi sistēmas lietotāji. Atlasiet lietotājus, kuriem piešķirt darbību, un pēc tam pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. Cilnes **Laika limits** laukā **Ilgums** norādiet, cik ilgs laiks ir dots lietotājam, lai veiktu darbību saistībā ar vai atbildētu uz dokumentiem, kas sasniedz apstiprināšanas darbību. Izvēlieties vienu no šīm opcijām:

    - **Stundas** — ievadiet stundu skaitu, kuru laikā lietotājam ir jāatbild. Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.
    - **Dienas** — ievadiet dienu skaitu, kuru laikā lietotājam ir jāatbild. Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.
    - **Nedēļas** — ievadiet nedēļu skaitu, kuru laikā lietotājam ir jāatbild.
    - **Mēneši** — izvēlieties dienu un nedēļu, līdz kurai lietotājam ir jāatbild. Piemēram, varat norādīt, lai lietotājs atbild līdz mēneša trešās nedēļas piektdienai.
    - **Gadi** — izvēlieties dienu, nedēļu un mēnesi, līdz kuram lietotājam ir jāatbild. Piemēram, varat norādīt, lai lietotājs atbildētu līdz decembra trešās nedēļas piektdienai.

    Ja lietotājs neveic darbības ar dokumentu atvēlētajā laikā, dokuments ir nokavēts. Nokavēts dokuments tiek eskalēts, pamatojoties uz opcijām, kas ir atlasītas lapas apgabalā **Eskalācija**.

4. Ja apstiprināšanas darbība ir piešķirta vairākiem lietotājiem vai lietotāju grupai, cilnē **Pabeigšanas ierobežojums** atlasiet vienu no šīm opcijām:

    - **Viens apstiprinātājs** — ar dokumentu veicamo darbību nosaka pirmā persona, kas atbild. Piemēram, Sems iesniedzis izdevumu pārskatu par USD 15 000. Izdevumu pārskats pašlaik ir piešķirts Sjū, Džo un Bilam. Ja Sjū ir pirmā uz dokumentu atbildējusī persona, dokumentam tiek veikta viņas izpildītā darbība. Ja Sjū noraida dokumentu, tas tiek noraidīts un nosūtīts atpakaļ Semam. Ja Sjū apstiprina šo dokumentu, tas tiek nosūtīts Annai apstiprināšanai.

        ![Darbplūsma, kurai ir apstiprināšanas process.](./media/workflow_multipleusersinstep.gif)

    - **Apstiprinātāju vairākums** — ar dokumentu veicamā darbība tiek noteikta, kad atbild apstiprinātāju vairākums. Piemēram, Sems iesniedzis izdevumu pārskatu par USD 15 000. Izdevumu pārskats pašlaik ir piešķirts Sjū, Džo un Bilam. Ja Sjū un Džo ir pirmie divi apstiprinātāji, kas atbild, viņu izpildītā darbība nosaka ar dokumentu veicamo darbību.

        - Ja Sjū apstiprina dokumentu, bet Džo to noraida, dokuments tiek noraidīts un atgriežas pie Sema.
        - Ja gan Sjū, gan Džo apstiprina dokumentu, tas nonāk apstiprināšanai pie Annas.

    - **Apstiprinātāju procenti** — ar dokumentu veicamā darbība tiek noteikta, kad atbild noteikts apstiprinātāju procentuālais daudzums. Piemēram, Sems iesniedzis izdevumu pārskatu par USD 15 000. Izdevumu pārskats pašlaik ir piešķirts Sjū, Džo un Bilam, un jūs ievadījāt **50** kā procentuālo daudzumu. Ja Sjū un Džo ir pirmie divi apstiprinātāji, kas atbild, viņu izpildītā darbība nosaka ar dokumentu veicamo darbību, jo tiek izpildīta prasība attiecībā uz 50 procentiem no apstiprinātājiem.

        - Ja Sjū apstiprina dokumentu, bet Džo to noraida, dokuments tiek noraidīts un atgriežas pie Sema.
        - Ja gan Sjū, gan Džo apstiprina dokumentu, tas nonāk apstiprināšanai pie Annas.

    - **Visi apstiprinātāji** — visiem apstiprinātājiem dokuments jāapstiprina. Pretējā gadījumā nevar turpināt darbplūsmu. Piemēram, Sems iesniedzis izdevumu pārskatu par USD 15 000. Izdevumu pārskats pašlaik ir piešķirts Sjū, Džo un Bilam. Ja Sjū un Džo apstiprina dokumentu, bet Bils to noraida, dokuments tiek noraidīts un nosūtīts atpakaļ Semam. Ja Sjū, Džo un Bils apstiprina dokumentu, tas nonāk apstiprināšanai pie Annas.

## <a name="specify-when-the-approval-step-is-required"></a>Norādiet, kad ir nepieciešama apstiprināšanas darbība

Varat norādīt, kad ir nepieciešama apstiprināšanas darbība. Apstiprināšanas darbība var būt nepieciešama vienmēr, vai arī tā var būt nepieciešama tikai tad, ja ir izpildīti konkrēti nosacījumi.

### <a name="the-approval-step-is-always-required"></a>Apstiprināšanas darbība ir nepieciešama vienmēr

Veiciet šīs darbības, ja apstiprināšanas darbība ir nepieciešama vienmēr.

1. Kreisajā rūtī noklikšķiniet uz **Nosacījums**.
2. Atlasiet opciju **Vienmēr izpildīt šo soli**.

### <a name="the-approval-step-is-required-in-specific-conditions"></a>Apstiprināšanas darbība ir nepieciešama, ja ir konkrēti nosacījumi

Apstiprināšanas darbība, kura tiek konfigurēta, var būt nepieciešama tikai tad, ja ir izpildīti konkrēti nosacījumi. Piemēram, ja konfigurējat pirkšanas pieprasījuma darbplūsmas apstiprināšanas darbību, varat to lietot tikai tad, ja pirkšanas pieprasījuma summa ir lielāka par USD 10 000. Veiciet šīs darbības, lai norādītu, kad ir nepieciešama apstiprināšanas darbība.

1. Kreisajā rūtī noklikšķiniet uz **Nosacījums**.
2. Atlasiet opciju **Izpildīt šo soli, ja ir spēkā šāds nosacījums**.
3. Ievadīt nosacījumu.
4. Ievadiet visus nepieciešamos papildu nosacījumus.
5. Lai pārbaudītu, vai ievadītie nosacījumi ir pareizi konfigurēti, rīkojieties šādi:

    1. Noklikšķiniet uz **Tests**.
    2. Lapas **Testēt darbplūsmas nosacījumu** apgabalā **Pārbaudīt nosacījumu** atlasiet ierakstu.
    3. Noklikšķiniet uz **Tests**. Sistēma novērtē ierakstu, lai noteiktu, vai tas atbilst jūsu definētajiem nosacījumiem.
    4. Noklikšķiniet uz **Labi** vai **Atcelt**, lai atgrieztos lapā **Rekvizīti**.

## <a name="specify-what-happens-when-the-document-is-overdue"></a>Norādiet, kas notiek, ja dokuments ir nokavēts

Ja lietotājs neveic darbības ar dokumentu atvēlētajā laikā, dokuments ir nokavēts. Dokumentu, kas ir nokavēts, var eskalēt vai automātiski piešķirt citam lietotājam apstiprināšanai. Veiciet šīs darbības, lai eskalētu dokumentu, ja tas ir nokavēts.

1. Kreisajā rūtī noklikšķiniet uz **Eskalācija**.
2. Atzīmējiet izvēles rūtiņu **Izmantot eskalācijas ceļu**, lai izveidotu eskalācijas ceļu. Sistēma automātiski piešķirs dokumentu lietotājiem, kuri ir norādīti eskalācijas ceļā. Piemēram, šajā tabulā ir attēlots eskalācijas ceļš.

    | Secība | Eskalācijas ceļš      |
    |----------|----------------------|
    | 1        | Piešķirt: Lindai     |
    | 2        | Piešķirt: Zanei      |
    | 3        | Pēdējā darbība: noraidīt |

    Šajā piemērā sistēma piešķir nokavēto dokumentu Lindai. Ja Linda neatbild atvēlētajā laikā, sistēma piešķir dokumentu Zanei. Ja Zane neatbild atvēlētajā laikā, sistēma noraida dokumentu.

3. Lai pievienotu lietotāju eskalācijas ceļam, noklikšķiniet uz **Pievienot eskalāciju**. Cilnē **Piešķires tips** atlasiet vienu no tālāk redzamajā tabulā minētajām opcijām un pēc tam veiciet papildu darbības attiecīgajai opcijai, pirms pārejat uz 4. darbību.

    <table>
    <thead>
    <tr>
    <th>Opcija</th>
    <th>Lietotāji, kuriem tiek eskalēts dokuments</th>
    <th>Papildu transakcijas</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Hierarhija</td>
    <td>Lietotāji īpašā organizācijas hierarhijā</td>
    <td>
    <ol>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Hierarhija</strong>, cilnes <strong>Hierarhijas atlase</strong> sarakstā <strong>Hierarhijas tips</strong> atlasiet hierarhijas tipu, uz kuru eskalēt dokumentu.</li>
    <li>Sistēmai no hierarhijas ir jāizgūst lietotāju vārdu diapazons. Šie vārdi norāda, kuriem lietotājiem var eskalēt dokumentu. Veiciet šīs darbības, lai norādītu sistēmas izgūto lietotāju vārdu diapazona sākumu un beigas: <ol>
    <li>Lai norādītu sākumu, atlasiet kādu personu sarakstā <strong>Sākt no</strong>.</li>
    <li>Lai norādītu beigas, noklikšķiniet uz <strong>Pievienot nosacījumu</strong>. Pēc tam ievadiet nosacījumu, kas nosaka, kurā vietā hierarhijā sistēma pārtrauc vārdu izgūšanu.</li>
    </ol>
    </li>
    <li>Cilnē <strong>Hierarhijas opcijas</strong> norādiet attiecīgajā diapazonā esošos lietotājus, kuriem jāveic dokumenta eskalācija: <ul>
    <li><strong>Piešķirt visiem izgūtajiem lietotājiem</strong> — dokuments tiek eskalēts visiem diapazonā esošajiem lietotājiem.</li>
    <li><strong>Piešķirt tikai pēdējam izgūtajam lietotājam</strong> — dokuments tiek eskalēts tikai pēdējam lietotājam diapazonā.</li>
    <li><strong>Neiekļaut lietotājus, kuri atbilst šādiem nosacījumiem</strong> — dokuments netiek eskalēts diapazonā esošajiem lietotājiem, kuri atbilst konkrētam nosacījumam. Lai norādītu nosacījumu, noklikšķiniet uz <strong>Pievienot nosacījumu</strong>.</li>
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
    <li>Sarakstā <strong>Pieejamie lietotāji</strong> ir ietverti visi lietotāji. Atlasiet lietotājus, kuriem eskalēt dokumentu, un pēc tam pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. Cilnes **Laika limits** laukā **Ilgums** norādiet, cik ilgs laiks ir dots lietotājam, lai veiktu darbību saistībā ar vai atbildētu uz dokumentiem. Izvēlieties vienu no šīm opcijām:

    - **Stundas** — ievadiet stundu skaitu, kuru laikā lietotājam ir jāatbild. Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.
    - **Dienas** — ievadiet dienu skaitu, kuru laikā lietotājam ir jāatbild. Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.
    - **Nedēļas** — ievadiet nedēļu skaitu, kuru laikā lietotājam ir jāatbild.
    - **Mēneši** — izvēlieties dienu un nedēļu, līdz kurai lietotājam ir jāatbild. Piemēram, varat norādīt, lai lietotājs atbild līdz mēneša trešās nedēļas piektdienai.
    - **Gadi** — izvēlieties dienu, nedēļu un mēnesi, līdz kuram lietotājam ir jāatbild. Piemēram, varat norādīt, lai lietotājs atbildētu līdz decembra trešās nedēļas piektdienai.

5. Atkārtojiet 3.–4. darbību katram lietotājam, kurš jāpievieno eskalācijas ceļam. Jūs varat mainīt lietotāju secību.
6. Ja eskalācijas ceļā norādītie lietotāji neatbild atvēlētajā laikā, sistēma automātiski veiks darbību ar dokumentu. Lai norādītu darbību, ko sistēma veic, atlasiet rindu **Darbība** un pēc tam cilnē **Beigu darbība** atlasiet darbību.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]