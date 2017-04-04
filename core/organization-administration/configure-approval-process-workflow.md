---
title: "Apstiprināšanas process konfigurēt darbplūsmas"
description: "Izmantojiet tālāk aprakstīto procedūru, lai konfigurētu apstiprināšanas procesa rekvizītus."
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 579e393ef64bc5ad72d129ac08ac215c524d5c55
ms.lasthandoff: 03/31/2017


---

# <a name="configure-an-approval-process-in-a-workflow"></a>Apstiprināšanas process konfigurēt darbplūsmas

Izmantojiet tālāk aprakstīto procedūru, lai konfigurētu apstiprināšanas procesa rekvizītus.

Lai konfigurētu darbplūsmas redaktors apstiprināšanas process, ar peles labo pogu noklikšķiniet uz apstiprinājuma elementa un pēc tam noklikšķiniet uz **Properties** atvērt **Properties** formu.
Nosaukuma piešķiršana apstiprināšanas procesam
-------------------------

Veiciet šīs darbības, lai ievadītu apstiprināšanas procesa nosaukumu.
1.  Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.
2.  Laukā **Nosaukums** ievadiet unikālu apstiprināšanas procesa nosaukumu.

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a>Norādiet, kad sistēma automātiski veic darbību ar dokumentu
Varat konfigurēt, lai sistēma automātiski rīkotos ar dokumentu, ja ir izpildīti konkrēti nosacījumi. Piemēram, sistēma var apstiprināt izdevumu pārskatus, kuros kopējās summas ir mazākas par USD 100. Izpildiet šīs darbības, lai norādītu, kad sistēma veic darbības ar dokumentu.
1.  Kreisajā rūtī noklikšķiniet uz **Automātiskas darbības**.
2.  Atzīmējiet izvēles rūtiņu **Iespējot automātiskas darbības**.
3.  Click **Add condition**.
4.  Ievadīt nosacījumu.
5.  Ja nepieciešams, ievadiet papildu nosacījumus.
6.  Lai pārbaudītu, vai ievadītie nosacījumi ir pareizi konfigurēti, veiciet šādas darbības:
    1.  Noklikšķiniet uz **Pārbaudīt**, lai atvērtu formu **Testēt darbplūsmas nosacījumu**.
    2.  Formas apgabalā **Pārbaudīt nosacījumu** atlasiet ierakstu.
    3.  Noklikšķiniet uz **Tests**. Sistēma novērtē ierakstu, lai noteiktu, vai tas atbilst jūsu definētajiem nosacījumiem.
    4.  Noklikšķiniet uz **OK** vai **atcelt** atgriezties **Properties** formu.

7.  Sarakstā **Automātiskās pabeigšanas darbība** atlasiet darbību, kāda sistēmai būtu jāveic ar dokumentu.

## <a name="specify-when-notifications-are-sent"></a>Norādīt, kad tiek sūtīti paziņojumi
Varat lietotājiem nosūtīt paziņojumus, kad dokuments ir apstiprināts, noraidīts, deleģēts vai eskalēts vai kad ir pieprasītas izmaiņas. Veiciet šīs darbības, lai norādītu, kad paziņojumi tiek sūtīti un kam tie tiek sūtīti.
1.  Kreisajā rūtī noklikšķiniet uz **Paziņojumi**.
2.  Atzīmējiet izvēles rūtiņu pie notikumiem, lai sūtītu paziņojumus par:
    -   **Pārstāvis** – kad dokuments ir piešķirta cita lietotāja apstiprinājumu.
    -   **Aktualizēt** – kad piešķirtais lietotājs nav pieņēmusi lēmumu par dokumentu atvēlētais laiks.
    -   **Apstiprināt** – kad dokuments ir apstiprināts.
    -   **Noraida** – kad dokuments ir ticis noraidīts.
    -   **Pieprasīt izmaiņas** – kad piešķirtais lietotājs ir pieprasījis izmaiņas dokumentā, kas tika iesniegts.

3.  Atlasiet tāda notikuma rindu, kuru atlasījāt 2. darbībā.
4.  Noklikšķiniet uz cilnes **Paziņojuma teksts**.
5.  Tekstlodziņā ievadiet paziņojuma tekstu.
6.  Lai personalizētu tekstu, varat ievietot vietturus, kas tiks nomainīti ar attiecīgajiem datiem, kad tie tiks parādīti lietotājiem. Lai ievietotu vietturi, rīkojieties šādi:
    1.  Klikšķiniet tekstlodziņā atrašanās vietā, kur vēlaties ievietot vietturi.
    2.  Noklikšķiniet uz **Ievietot vietturi**.
    3.  Parādītajā sarakstā atlasiet vietturi, kuru ievietot.
    4.  Klikšķiniet **Ievietot**.

7.  Lai pievienotu paziņojumu tulkojumu, noklikšķiniet uz **tulkojumi**. Parādītajā formā veiciet šādas darbības:
    1.  Click **Add**.
    2.  Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.
    3.  Tekstlodziņā **Tulkotais teksts** ievadiet tekstu.
    4.  Lai personalizētu tekstu, ievietojiet vietturus.
    5.  Noklikšķiniet uz **Aizvērt**.

8.  Noklikšķiniet uz cilnes **Saņēmējs**.
9.  Norādīt, kam tiek sūtīti paziņojumi. Atlasiet vienu no tālāk redzamajā tabulā minētajām opcijām un pēc tam veiciet papildu darbības attiecīgajai opcijai, pirms pārejat uz 10. darbību.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Opcija</th>
    <th>Paziņojuma adresāti</th>
    <th>Papildu transakcijas</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><strong>Dalībnieks</strong></td>
    <td>Lietotāji, kuri ir piešķirti noteiktai grupai vai lomai</td>
    <td><ol>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Dalībnieks</strong>, noklikšķiniet uz cilnes <strong>Pēc lomas</strong>.</li>
    <li>Sarakstā <strong>Dalībnieka tips</strong> atlasiet grupas vai lomas veidu, kurai nosūtīt paziņojumus.</li>
    <li>Sarakstā <strong>Dalībnieks</strong> atlasiet grupu vai lomu, kurai nosūtīt paziņojumus.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><strong>Darbplūsmas lietotājs</strong></td>
    <td>Lietotāji, kuri piedalās pašreizējā darbplūsmā</td>
    <td><ol>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Darbplūsmas lietotājs</strong>, noklikšķiniet uz cilnes <strong>Darbplūsmas lietotājs</strong>.</li>
    <li>Sarakstā <strong>Darbplūsmas lietotājs</strong> atlasiet lietotāju, kas piedalās attiecīgajā darbplūsmā.</li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><strong>User</strong></td>
    <td>Īpaša Microsoft Dynamics 365 operācijas lietotājiem</td>
    <td><ol>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Lietotājs</strong>, noklikšķiniet uz cilnes <strong>Lietotājs</strong>.</li>
    <li><strong>Pieejams lietotājiem</strong>: saraksts ietver visus Microsoft Dynamics 365 operācijas lietotājiem. Atlasiet lietotājus, kuriem sūtīt paziņojumus, un pēc tam pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>:.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

10. Atkārtojiet 3.–9. darbību katram notikumam, ko atlasījāt 2. darbībā.

## <a name="specify-a-final-approver"></a> Norādiet pēdējo apstiprinātāju
Varat apzīmēt pēdējo apstiprinātāju scenārijiem, kuros apstiprinātājs ir persona, kas iesniegusi dokumentu apstiprināšanai. Lai norādītu galīgo apstiprinātāju, veiciet šādas darbības.
1.  Kreisajā rūtī noklikšķiniet uz **Papildu iestatījumi**.
2.  Atzīmējiet izvēles rūtiņu **Izmantot galīgo apstiprinātāju**.
3.  Sarakstā atlasiet lietotāju, kurš būs galīgais apstiprinātājs.

## <a name="set-a-time-limit"></a>Laika robežas iestatīšana
Veiciet šīs darbības, ja apstiprināšanas process ir jāpabeidz noteiktā laikā.
| **Piezīme **                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Šajās darbībās izvēlētās opcijas tiks lietotas neatkarīgi no opcijām, kas atlasītas katra apstiprināšanas soļa apgabalā **Piešķire** un **Eskalācija**. |

1.  Kreisajā rūtī noklikšķiniet uz **Papildu iestatījumi**.
2.  Atzīmējiet izvēles rūtiņu **Iestatīt darbplūsmas **elementa** laika ierobežojumu**.
3.  Laukā **Ilgums** norādiet, kad apstiprināšanas process ir jāpabeidz. Izvēlieties vienu no šīm opcijām:
    -   **Stundas** — ievadiet stundu skaitu, pēc kurām apstiprināšanas procesam jābūt pabeigtam. Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.
    -   **Dienas** — ievadiet dienu skaitu, pēc kurām apstiprināšanas procesam jābūt pabeigtam. Pēc tam atlasiet kalendāru, ko izmanto jūsu organizācija, un ievadiet informāciju par jūsu organizācijas darba nedēļu.
    -   **Nedēļas** — ievadiet nedēļu skaitu, pēc kurām apstiprināšanas procesam jābūt pabeigtam.
    -   **Mēneši** — izvēlieties dienu un nedēļu, līdz kurai ir jāpabeidz apstiprināšanas process. Piemēram, iespējams, vēlēsieties, lai apstiprināšanas process būtu pabeigts līdz mēneša trešās nedēļas piektdienai.
    -   **Gadi** — izvēlieties dienu, nedēļu un mēnesi, līdz kuram ir jāpabeidz apstiprināšanas process. Piemēram, iespējams, vēlēsieties, lai apstiprināšanas process būtu pabeigts līdz decembra trešās nedēļas piektdienai.

4.  Ja laika ierobežojums ir pārsniegts, sistēma veiks darbību ar dokumentu. Sarakstā **Darbība** atlasiet darbību, kāda sistēmai būtu jāveic.

## <a name="specify-which-actions-are-available-to-the-user"></a>Norādiet, kuras darbības ir pieejamas lietotājam
Kad dokuments ir piešķirts lietotājam apstiprināšanai, lietotājam ar šo dokumentu jārīkojas. Izpildiet šīs darbības, lai norādītu, kuras darbības lietotājs var veikt ar iesniegto dokumentu.
1.  Kreisajā rūtī noklikšķiniet uz **Papildu iestatījumi**.
2.  Atlasiet **apstiprināt** izvēles rūtiņu, ja lietotājs var apstiprināt šo dokumentu.
3.  Atlasiet **noraidīt** izvēles rūtiņu lietotājs var noraidīt dokumentu.
4.  Atlasiet **pieprasītu izmaiņas** izvēles rūtiņu lietotājs var pieprasīt veikt dokumentā izmaiņas.
5.  Atlasiet **pārstāvis** izvēles rūtiņu, ja lietotājs var piešķirt dokumentu apstiprināšanai citam lietotājam.

**Piezīme**. Izvēles rūtiņa **Iespējot darbības no darbu saraksta uzņēmuma portālā ** ir novecojusi.

## <a name="configure-the-approval-steps"></a> Apstiprinājuma darbību konfigurēšana
Apstiprināšanas process sastāv no apstiprināšanas darbībām. Veiciet šādu procedūru, lai pievienotu darbības apstiprināšanas procesam un konfigurētu darbības.
1.  Darbplūsmas redaktorā veiciet dubultklikšķi uz apstiprināšanas procesa. Darbplūsmas redaktorā tiek parādītas apstiprināšanas procesa darbības.
2.  Lai pievienotu apstiprināšanas darbību, velciet darbību no apgabala **Darbplūsmas elementi** uz audekla.
3.  Lai konfigurētu apstiprināšanas darbību, skatiet sadaļu [Apstiprinājuma darbības konfigurēšana](http://axhelp.dynamics.com/en/wiki/configure-an-approval-step/).




