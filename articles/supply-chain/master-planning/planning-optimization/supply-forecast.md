---
title: Vispārējā plānošana ar piegādes apjoma prognozēm
description: Šajā rakstā ir aprakstīts, kā vispārējās plānošanas laikā tiek apsvērtas piegādes apjoma prognozes.
author: t-benebo
ms.date: 09/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-21
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: dc83d10851958ec67166cb7e40cfd84dceae6651
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690163"
---
# <a name="master-planning-with-supply-forecasts"></a>Vispārējā plānošana ar piegādes apjoma prognozēm

[!include [banner](../../includes/banner.md)]

Piegādes apjoma prognozes ļauj norādīt piedāvājumu, kuru prognozēsiet kāda turpmāka perioda laikā. Parasti novērtējums tiks balstīts uz iepriekšējā gada pārdošanas vēsturi un pēc tam lietojiet šo prognozi budžeta plānošanas nolūkiem. Var iestatīt arī vispārējos plānus, lai plānošanas laikā apsvērtu prognozes.

## <a name="set-up-a-master-plan-to-consider-supply-forecasts"></a>Iestatīt vispārējo plānu, lai apsvērtu piegādes apjoma prognozes

Varat norādīt, vai katram vispārējai plānam ir jāņem vērā prognozes tā izpildes laikā. Izmantojiet šo procedūru, lai katram plānam iestatītu budžeta opcijas.

1. Dodieties uz **Vispārējā plānošana \> Iestatījumi \> Plāni \> Vispārējie plāni**.
1. Atlasiet esošu vispārējo plānu saraksta rūtī vai atlasiet Jauns **darbību** rūtī, lai izveidotu jaunu.
1. Kopsavilkuma cilnē **Vispārīgi**, iestatiet tālāk minētos laukus:

    - **Budžeta modelis** – atlasiet modeli, kas ietver piedāvājuma un/vai pieprasījuma apjoma prognozes, kas būtu jāņem vērā vispārējā plānā.
    - **Iekļaut piegādes apjoma prognozi** – iestatiet šo opciju kā *Jā*, ja vispārējais plāns ņem vērā piegādes apjoma prognozes.
    - **Iekļaut pieprasījuma apjoma prognozi** – iestatiet šo opciju kā *Jā*, ja vispārējais plāns ņem vērā pieprasījuma apjoma prognozes. Kaut arī šis iestatījums nav atkarīgs **no iekļaut piegādes** apjoma prognozes iestatījuma, daži citi lapas iestatījumi attiecas gan uz piegādes apjoma prognozēm, gan uz pieprasījuma apjoma prognozēm. Papildinformāciju par plānošanu, kas ņem vērā pieprasījuma apjoma prognozes, skatiet [vispārējā plānošanā ar pieprasījuma apjoma prognozēm](demand-forecast.md).
    - **Budžeta prasību samazināšanai izmantotā metode** . Atlasiet metodi, lai vispārējās plānošanas laikā samazinātu budžeta vajadzības:

        - *Neviens* – budžeta vajadzības vispārējās plānošanas laikā netiks samazinātas.
        - *Procenti - samazināšanas princips* – budžeta vajadzības tiks samazinātas atbilstoši samazināšanas princips procentiem un laika periodiem.
        - *Darbības – samazināšanas princips* – budžeta vajadzības tiks samazinātas, izmantojot darbības, kas parādās samazināšanas princips definētos laika periodos.
        - *Darījumi – dinamiskais* periods – budžeta vajadzības tiks samazinātas, izmantojot pasūtījumu darbības, kas notiek dinamiskajā periodā. Dinamiskais periods aptver pašreizējos prognozes datumus un beidzas, kad sākas nākamā prognoze. Transakcijas *— dinamiskā perioda* metode neizmanto un pieprasa samazināšanas principu, un, ja izmantojat to, ir spēkā šādi nosacījumi:

            - Ja prognoze ir pilnībā samazināta, prognozes vajadzības pašreizējai prognozei ir 0 (nulle).
            - Ja nav nevienas turpmākas prognozes, tiek samazinātas prognozes vajadzības no pēdējās ievadītās prognozes.
            - Prognozes samazināšanas aprēķinā tiek iekļauti laika periodi.
            - Prognozes samazināšanas aprēķinā tiek iekļautas dienas(+).
            - Ja faktiskā pasūtījuma transakcijas pārsniedz prognozes vajadzības, atlikušās transakcijas netiek pārsūtītas uz nākamo prognozes periodu.

        > [!NOTE]
        > Budžeta **prasību samazināšanas metode** tiek lietota arī pieprasījuma apjoma prognozēm, ja esat tos iespējojis vispārējaim plānam, un tā ietekmē tās līdzīgi. Papildinformāciju skatiet vispārējā plānošanā [ar pieprasījuma apjoma prognozēm](demand-forecast.md).

## <a name="set-reduction-options-for-coverage-groups"></a>Iestatīt vajadzības grupu samazināšanas opcijas

Lai iestatītu opcijas, kas kontrolē to, kā vajadzību grupa samazina tās budžeta vajadzības vispārējām sistēmām, kas izmanto uz darbībām balstītu samazināšanu, sekojiet šiem soļiem.

1. Dodieties uz sadaļu **Vispārējā plānošana \> Iestatījumi \> Plāns \> Saguma grupas**.
1. Atlasiet eksistējošu vajadzības grupu saraksta rūtī vai atlasiet Jauns **darbību** rūtī, lai izveidotu jaunu.
1. **Kopsavilkuma cilnē Cita** kopsavilkuma cilne Laukā Samazināt prognozi pēc **norādiet,** kā piegādes apjoma prognozes prasības ir jāsamazina krājumiem vajadzības grupā galvenajiem plāniem, **·** *kur lauks Budžeta vajadzību samazināšanai tiek iestatīts uz Darbības -* *samazināšanas princips vai Darbības - dinamiskais* periods. Atlasiet vienu no šīm vērtībām:

    - *Visi darījumi* – visiem darījumiem jāsamazina budžets.
    - *Pasūtījumi* – tikai viena tipa pasūtījumiem vajadzētu samazināt prognozi.

    Piemēram, pasūtījuma noklusējuma iestatījumi krājumam norāda, ka tas ražots. Daudzumam 50 ir piegādes apjoma prognozes rinda, un pastāv pirkšanas pasūtījums ar daudzumu 20. Ja lauks **Samazināt prognozi** pēc ir iestatīts *uz* Pasūtījumi, tiks izveidots plānotais ražošanas pasūtījums daudzumam 50. Ja iestatīts kā Visas *darbības*, plānotais ražošanas pasūtījums tiks samazināts līdz 30 daudzumam.

    Šis iestatījums attiecas arī uz pieprasījuma apjoma prognozēšanas samazinājumu. Papildinformāciju skatiet vispārējā plānošanā [ar pieprasījuma apjoma prognozēm](demand-forecast.md).

## <a name="enter-a-supply-forecast-for-a-product"></a>Ievadiet preces piegādes apjoma prognozi

Lai ievadītu preču piegādes apjoma prognozi, veiciet šādus soļus.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atlasiet preci, kurai vēlaties ievadīt budžetu.
1. Darbību rūtī cilnē Plāns atlasiet **Piegādes** apjoma **prognoze**.
1. Lai režģim **pievienotu** prognozi, **darbību** rūtī lapas Piegādes apjoma prognoze atlasiet Jauns.
1. Ievadiet informāciju jaunā rindā pēc vajadzības, lai norādītu budžetu.

## <a name="plan-for-an-item-with-supply-forecast-lines"></a>Plāns krājumam ar piegādes apjoma prognozes rindām

Kad palaižat vispārējo plānu, kas ietver krājumu, kam pastāv piegādes apjoma prognoze, sistēma izveidos pirkšanas pasūtījumu ievadītajām piegādes rindām. Tiek ievēroti krājuma noklusējuma pasūtījuma iestatījumi. Ja šie noklusējuma **pasūtījuma** *iestatījumi* norāda Pirkšanas pasūtījuma noklusējuma pasūtījuma tipa vērtību un piegādes apjoma prognozes rindā nav norādīts kreditora konts, sistēma krājumam izmantos noklusējuma kreditoru.

## <a name="check-whether-a-planned-order-is-a-supply-forecast-order"></a>Pārbaudīt, vai plānotais pasūtījums ir piegādes apjoma prognozes pasūtījums

Izmantojiet šo procedūru, lai uzzinātu, vai plānotais pasūtījums ir izveidots piegādes apjoma prognozes rezultātā.

1. Doties uz **Vispārējā plānošana \> Vispārējā plānošana \> Plānotie pasūtījumi**.
1. Atveriet plānoto pasūtījumu, kurš jāpārbauda.
1. **Kopsavilkuma cilnē** Vispārējā daļa skatiet piegādes apjoma prognozes **lauka** vērtību. Ja pasūtījums tika izveidots, lai nosegtu piegādes apjoma prognozi, šis lauks tiks iestatīts uz *Jā*.

## <a name="examples-of-master-planning-with-supply-forecasts"></a>Piegādes apjoma prognozes vispārējās plānošanas piemēri

Šajā sadaļā sniegti vairāki piemēri, kas parāda, kā piegādes apjoma prognozēšana ietekmē vispārējo plānošanu.

### <a name="example-1-supply-forecast-for-an-item"></a>1. piemērs: piegādes apjoma prognoze krājumam

Jums ir krājums, kura noklusējuma pasūtījuma tips ir Pirkšanas *pasūtījums* un noklusējuma kreditors ir *US-002*. Tai ir šāda piegādes apjoma prognozes rinda.

| Modelis    | Datums     | Kreditora konts | Kreditoru grupa | Daudzums | Vienība | Vietne | Noliktava |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 |                |              | 35       | gab.   | 1    | 11        |

Izpildot vispārējo plānošanu, plānotais pirkšanas pasūtījums tiks *izveidots 35 stundas* no *kreditora US-002*.

### <a name="example-2-several-supply-forecast-lines-with-and-without-a-vendor"></a>2. piemērs: vairākas piegādes apjoma prognozes rindas ar kreditoru un bez tā

Jums ir krājums, kura noklusējuma pasūtījuma tips ir Pirkšanas *pasūtījums* un noklusējuma kreditors ir *US-002*. Tam ir šādas piegādes apjoma prognozes rindas.

| Modelis    | Datums     | Kreditora konts | Kreditoru grupa | Daudzums | Vienība | Vietne | Noliktava |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 |                |              | 35       | gab.   | 1    | 11        |
| CurrentF | 10/10/22 | US-101         |              | 25       | gab.   | 1    | 11        |

Šajā gadījumā sistēma apstrādā rindu, kas nenorāda kreditoru kā vispārēju prognozi, un tā pieņem, ka rinda, kas nenorāda kreditoru, ir jāatskaita no vispārīgās prognozes. Tādējādi vispārējais plāns krājumam izveidos šādus plānotos pirkšanas pasūtījumus:

- Plānotais pirkšanas pasūtījums *ar daudzumu 25pus* *no kreditora US-101* (tiek izmantots kreditors un budžeta rindā norādītais daudzums.)
- Plānotais *pirkšanas pasūtījums ar daudzumu 10 pēc* *kreditora US-002* (tā kā citā budžeta rindā nav norādīts kreditors, tiek izmantots noklusējuma kreditors, un šīs budžeta rindas daudzumu samazina ar kreditoram specifisku budžeta rindu daudzumu.)

### <a name="example-3-plans-that-use-the-transactions---dynamic-period-reduction-method-in-a-single-forecast-period"></a>3. piemērs: plāni, kuros vienā budžeta periodā tiek izmantota metode Darījumi — dinamiskā perioda samazināšana

Vispārējai plānošanai, kur dinamiskais *periods* tiek izmantots kā budžeta samazināšanas metode, vispārējais plāns samazina budžeta daudzumu, ja pastāv darbības, kas atbilst šīm piegādes raksturlielumiem.

Piemēram, jums ir krājums, kura noklusējuma pasūtījuma tips ir Pirkšanas *pasūtījums*. Tai ir šāda piegādes apjoma prognozes rinda.

| Modelis    | Datums     | Kreditora konts | Kreditoru grupa | Daudzums | Vienība | Vietne | Noliktava |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 | US-101         |              | 25       | gab.   | 1    | 11        |

Tā kā ir tikai viena piegādes apjoma prognozes rinda, ir tikai viens prognozes periods.

Palaižot vispārējo plānu, kas iestatīts *izmantot darbības -* dinamiskais periods kā samazināšanas metode, var rasties viens no šiem rezultātiem:

- *Ja kreditoram US-101* *pastāv pirkšanas pasūtījums ar daudzumu 10 s*, un lauks Piegādes apjoma prognoze ir iestatīts uz Jā, **·** *·* *vispārējā plānošana izveido jaunu plānoto pirkšanas pasūtījumu atlikušajam daudzumam 10 e.* Budžeta rinda tiek samazināta, jo kreditors atbilst esošajam pirkšanas pasūtījumam.
- *Ja kreditoram US-102*, vietai 1, *·* *noliktavai 11* *un daudzumam 10 p* **·** *·*. un piegādes apjoma prognozes laukam ir iestatīts iestatījums Jā, *vispārējais plāns izveido jaunu plānoto pirkšanas pasūtījumu ar pilnu daudzumu 25 elektron.* Budžeta rindu nevar samazināt, jo tai ir citāds kreditors nekā esošajam pirkšanas pasūtījumam.

> [!NOTE]
> Šāda situācija var rasties plānotiem pirkšanas pasūtījumiem, jo ar tiem ir saistīts kreditors. Tomēr pārsūtīšanas pasūtījumiem un ražošanas pasūtījumiem piegādes apjoma prognozes summas vienmēr tiks samazinātas ar esošajiem pasūtījumiem, jo šiem pasūtījumu tipiem nav norādīts kreditors.

### <a name="example-4-plans-that-use-the-transactions---dynamic-period-reduction-method-over-several-forecast-periods"></a>4. piemērs: plāni, kuros tiek izmantota metode Darījumi — dinamiskā perioda samazināšana vairāku budžeta periodu laikā

Jums ir krājums, kura noklusējuma pasūtījuma tips ir Pirkšanas *pasūtījums*. Tam ir šādas piegādes apjoma prognozes rindas.

| Modelis    | Datums     | Kreditora konts | Kreditoru grupa | Daudzums | Vienība | Vietne | Noliktava |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 | US-101         |              | 25       | gab.   | 1    | 11        |
| CurrentF | 10/15/22 | US-101         |              | 25       | gab.   | 1    | 11        |

Šajā piemērā ir divas prognozes rindas, no kurām katrai ir citāds datums. Tāpēc datumi izveido budžeta periodu robežas. Pirmais periods ir no 2022. gada 10. oktobris līdz 2022. gada 14. oktobris (10/10/22–10/14/22). Otrais ir no 2022. gada 15. oktobris (10/15/22) uz priekšu.

Pastāv pirkšanas *pasūtījums kreditoram US-101*, *daudzums 10 pēc datuma* *10/12/22* (2022. gada 12. oktobris). Palaižot vispārējo plānu, kas iestatīts *izmantot darbības -* dinamiskais periods kā samazināšanas metode, tas izveidos šādus pasūtījumus:

- Plānotais pasūtījums ar *daudzumu 15 līdz* *10/10/22* (daudzumu samazina esošais pirkšanas pasūtījums, kas datēts tajā pašā budžeta periodā.)
- Plānotais pasūtījums ar *daudzumu 25pus* *un 15.01.22* . (Daudzums ir pilns prognozes daudzums.)

### <a name="example-5-plans-that-use-no-reduction"></a>5. piemērs: Plāni, kuros netiek izmantots samazinājums

Kad tiek palaists plāns, kur prognozes samazināšanas metode ir *Nav*, vispārējā plānošana vienmēr izveidos plānoto piegādi visām piegādes apjoma prognozes rindām. Kad plānotā piegāde ir apstiprināta, tiks samazināti turpmākie plānotie pasūtījumi. Tomēr pirkšanas pasūtījumi samazinās piegādes apjoma prognozes rindas.

Piemēram, jums ir krājums, kura noklusējuma pasūtījuma tips ir Pirkšanas *pasūtījums*. Tai ir šāda piegādes apjoma prognozes rinda.

| Modelis    | Datums     | Kreditora konts | Kreditoru grupa | Daudzums | Vienība | Vietne | Noliktava |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 | US-101         |              | 25       | gab.   | 1    | 11        |

Pastāv pirkšanas *pasūtījums kreditoram US-101*, *vietai 1*, *noliktavai 11*, *daudzumam 25 p* *. un datumam 10/10/22*. 

Palaižot *vispārējo* plānu, kas iestatīts izmantot Nav kā samazināšanas metodi, *tiks izveidots plānotais pirkšanas pasūtījums kreditoram US-101*, *1*. vieta, *11*. noliktava *,* daudzums 25pus *un datums 10/10/22*. Citiem vārdiem sakot, esošais pirkšanas pasūtījums netiks samazināts, jo prognozes samazināšanas metode ir *Nav*.

Tagad rediģējiet plānoto pirkšanas pasūtījumu, kas tika izveidots pēc pēdējās plānošanas izpildes, un mainiet daudzumu uz *15.* Pēc tam jūs apstipriniet pasūtījumu. *Nākamajā vispārējā plāna palaišanas reizē tiks izveidots plānotais pirkšanas pasūtījums kreditoram US-101*, *1*. vieta, *11*. noliktava, *daudzums 10 us* un *datums 10/10/22*. Šoreiz daudzums tiks samazināts, lai atspoguļotu esošā apstiprinātā pasūtījuma daudzumu no iepriekšējās plānošanas izpildes.

## <a name="differences-between-planning-optimization-and-the-built-in-planning-engine"></a>Atšķirības starp plānošanas optimizāciju un iebūvēto plānošanas programmu

Piegādes apjoma prognozes nedaudz atšķiras atkarībā no izmantotās plānošanas programmas (iebūvēta vispārējā plānošana vai plānošanas optimizācija). Šajā sadaļā ir aprakstītas atšķirības.

### <a name="vendor-groups"></a>Kreditoru grupas

Kad pievienojat budžeta rindu, varat norādīt kreditoru un kreditoru grupu. Iebūvētajā plānošanas programmā izveidotie plānotie pasūtījumi tiek grupēti pēc kreditoru un kreditoru grupu vērtību kombinācijām. Plānošanas optimizācijā plānotie pasūtījumi tiek grupēti pēc kreditoriem.

Tabulā sniegti daži piegādes apjoma prognozes rindu piemēri krājumam.

| Modelis    | Datums     | Kreditora konts | Kreditoru grupa | Daudzums | Vienība | Vietne | Noliktava |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 |                | VendorGroupA | 5        | gab.   | 1    | 11        |
| CurrentF | 10/10/22 |                | VendorGroupA | 6        | gab.   | 1    | 11        |
| CurrentF | 10/10/22 |                |              | 7        | gab.   | 1    | 11        |

Kreditoru *grupa VendorGroupA* *ir noklusējuma kreditors*. Tas ir arī krājuma noklusētais kreditors.

Iebūvētā plānošanas programma izveidos šādus pasūtījumus:

- Plānotais pirkšanas pasūtījums kreditoram *VendorA*, kreditoru *grupai VendorGroupA* un daudzumam *11*
- Plānotais pirkšanas pasūtījums *kreditoram VendorA* un daudzums *7*

Plānošanas optimizēšana izveidos tikai vienu pasūtījumu:

- Plānotais pirkšanas pasūtījums kreditoram *VendorA*, kreditoru *grupai VendorGroupA* un daudzumam *18*

### <a name="reduction-of-general-forecasts-by-more-specific-forecasts"></a>Vispārējo prognožu samazināšana par specifiskākām prognozēm

Iebūvētajā vispārējās plānošanas programmā rezultāts ir neprognozējams, ja dažām prognozēm ir kreditors, bet citiem tā nav.

Optimizācijas plānošanā vispārīgās prognozes vienmēr tiek samazinātas ar specifiskām prognozēm, kā redzams šajā piemērā.

Tabulā sniegti daži piegādes apjoma prognozes rindu piemēri krājumam.

| Datums       | Daudzums | Kreditors   | Kreditoru grupa  |
|------------|----------|----------|---------------|
| 02/11/2022 | 5.00     | Kreditors-A | VendorGroup-A |
| 02/11/2022 | 6,00     | Kreditors-A | VendorGroup-A |
| 02/11/2022 | 15.00    |          |               |

Vispārējo prognozi (15,00 gabaliem) samazina par specifiskākām prognozēm (par 5,00 + 6,00 = 11,00 gabaliem). Atlikums tiek piešķirts noklusētajam kreditoram. Tabulā redzami plānotie pasūtījumi.

| Datums       | Daudzums | Kreditors   | Kreditoru grupa  |
|------------|----------|----------|---------------|
| 02/11/2022 | 11.00    | Kreditors-A | VendorGroup-A |
| 02/11/2022 | 4.00     | Kreditors-A | VendorGroup-A |

### <a name="respect-for-default-order-settings-when-planned-orders-are-generated"></a>Jāņem vērā noklusējuma pasūtījuma iestatījumi, kad tiek ģenerēti plānotie pasūtījumi

Katram krājumam var būt noklusējuma pasūtījuma iestatījumi, piemēram, minimālais pirkšanas pasūtījuma daudzums. Iebūvētā plānošanas programma ignorē šos iestatījumus, un tādēļ pārveido prognozes par plānotajiem pasūtījumiem, kam ir vienāds daudzums. Optimizācijas plānošanā tiek ievēroti šie iestatījumi, kad plānotie pasūtījumi tiek ģenerēti no piegādes apjoma prognozēm. 

### <a name="aggregation-of-planned-orders-as-a-result-of-reduction-by-approved-orders"></a>Plānoto pasūtījumu apkopojums apstiprināto pasūtījumu samazināšanas rezultātā

Iebūvētā vispārējās plānošanas programma pieņem, ka tikai viens pasūtījums samazinās esošo piegādes apjoma prognozi. Tādēļ, ja vairāki pasūtījumi atbilst piegādes apjoma prognozes rindai, tikai pirmais pasūtījums to samazina. Optimizācijas plānošanā visi pasūtījumi, kas atbilst piegādes apjoma prognozes rindai, to samazinās.

### <a name="reduction-of-forecasts-by-matching-vendors-only"></a>Prognožu samazināšana, izmantojot tikai atbilstošus kreditorus

Kad iebūvētā vispārējās plānošanas programma samazina prognozi, izmantojot jau izlaistos pirkšanas pasūtījumus, netiek nodrošināts, ka pirkšanas pasūtījumā esošais kreditors atbilst kreditoram prognozē. Optimizācijas plānošana samazina prognozes tikai par pirkšanas pasūtījumiem, kuriem kreditora laukā ir atbilstoša vērtība.

Pārsūtīšanas un ražošanas pasūtījumos kreditora lauks vienmēr tiek ignorēts, jo tas nav derīgs šiem pasūtījuma tipiem.

### <a name="reduction-of-forecasts-by-transfer-orders"></a>Prognožu samazināšana pēc pārsūtīšanas pasūtījumiem

Ja krājuma noklusētais pasūtījuma tips ir *Pārsūtīšana*, prognozes var samazināt tikai par esošajiem plānotajiem pārsūtīšanas pasūtījumiem. Tomēr ražošanas pasūtījumiem un pirkšanas pasūtījumiem tikai izlaistie pasūtījumi samazina piegādes apjoma prognozi.

Iebūvētā plānošanas programma samazina visu pārsūtīšanas pasūtījumu administratīvos apgabalos, bet plānošanas optimizācija samazina prognozes tikai par pārsūtīšanas pasūtījumiem, kas ir atbrīvotā *stāvoklī*.
