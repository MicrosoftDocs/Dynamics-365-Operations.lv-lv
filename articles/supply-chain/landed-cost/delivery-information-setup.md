---
title: Informācijas par piegādi iestatīšana
description: Šajā tēmā ir aprakstīts, kā iestatīt piegādes informāciju Kopīgo izmaksu modulim.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMPortTable, ITMLeadTimeTable, ITMLegTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 5d20f732f02140204d67e5602acaf42f9d9df424
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021592"
---
# <a name="delivery-information-setup"></a>Informācijas par piegādi iestatīšana

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā iestatīt piegādes informāciju **Kopīgo izmaksu** modulim.

## <a name="shipping-ports"></a>Nosūtīšanas ostas

Nosūtīšanas ostas norāda, no kurienes un uz kurieni tiek sūtītas preces. Katram reisam tiek definēta osta "uz" un osta "no", pamatojoties uz kuģošanas laikā izvēlētu reisa kuģim. Nosūtīšanas ostas tiek izmantotas, lai būvētu ceļojuma kravas un arī reisu darbības. Tās parasti tiek definētas, izmantojot pilsētas nosaukumu un valsti vai reģionu, kur atrodas fiziskas nosūtīšanas osta.

Lai strādātu ar nosūtīšanas ostām, dodieties uz sadaļu **Kopīgās izmaksas \> Piegādes informācijas iestatīšana \> Nosūtīšanas ostas**. Tur varat skatīt, pievienot un noņemt ierakstus saviem nosūtīšanas ostām. Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram ierakstam.

| Lauks | Apraksts |
|---|---|
| Nosūtīšanas osta | Ievadiet nosūtīšanas ostai unikālu ID nosaukumu/numuru. |
| Apraksts | Ievadiet nosūtīšanas ostas aprakstu. |

## <a name="tracking-control-center"></a><a name="tracking-control-center"></a>Izsekošanas vadības centrs

Jūs izmantojat Izsekošanas kontroles centru, lai iestatītu izpildes laikus, statusa atjauninājumus un informācijas plūsmu, kas saistīta ar reisu, kā nosūtīšanas konteineri pārvietojas no vienas kravas uz nākamo. Kad izveidojat izsekošanas kontroles ierakstu, tas ir saistīts ar noteiktu reisa ceļojuma kājai. Kad reiss atjaunina kāju, saistītais ieraksts tiks atjaunināts un aizpildīts, kā norādīts. Izsekošanas informāciju par atsevišķiem reisiem varat atjaunināt no lapas **Visi reisi**.

Lai atvērtu izsekošanas kontroles centru, dodieties uz sadaļu **Kopīgās izmaksas \> Piegādes informācijas iestatīšanas \> Izsekošanas kontroles centrs**.

Izsekošanas kontroles centrs rāda vienu no trim lapas skatiem atkarībā no vērtības, kas atlasīta laukā **Izveidot tipu** saraksta rūtī: *Tukšs*, *Izpildes laiks* vai *Statusa atjauninājums*. Katra tipa izveides darbības atjaunina atšķirīgu informācijas kopu, kas ir saistīta ar reisa progresu no izcelsmes vietas līdz gala adresātam.

### <a name="common-rule-settings"></a>Vispārējo kārtulu iestatījumi

Tālāk redzamajā tabulā ir parādīti lauki, kas ir pieejami visiem trim Izsekošanas kontroles centra izveides tipiem.

| Lauks | Apraksts |
|---|---|
| Avota tabula, Avota lauks | Šie lauki identificē avota tabulu un lauku datu bāzē. Kārtula ielādēs vērtību laukā un pēc tam izmantos to tādā veidā, kā noteikts ar citiem kārtulas iestatījumiem. |
| Mērķa tabula, Mērķa lauks | Šie lauki identificē galamērķa tabulu un lauku datu bāzē. Kārtula ielādēs vērtību laukā un pēc tam izmantos to (vai pārrakstīs) tādā veidā, kā noteikts ar citiem kārtulas iestatījumiem. |
| Aktivitāte | Šajā laukā ir norādīts aktivitātes veids, kas jālieto saskaņā ar kārtulu atbilstošam nosūtīšanas konteineram. |
| Atbilstības kritēriji | Šis lauks nosaka, kā sistēma identificē kārtulas atbilstību. Katrā gadījumā sistēma pārskata datus avota un galamērķa tabulās, lai noteiktu, vai un kad lauks jāatjaunina mērķa tabulā.<p>Piemēram, avota tabula ir *Reisi*, un mērķa tabula ir *Pirkšanas virsraksts* vai *Pirkšanas rindas*. *Reisu* tabulai ir lauka **No ostas** vērtība *Honkonga*, un tabulas *Pirkšanas virsraksts* vērtība **No ostas** *Šanhaja*. Pēc tam tiek izveidota kārtula, kuras ostas vērtība "No" ir *Honkonga*. Šajā gadījumā **Atbilstības kritēriju** lauka vērtības darbosies šādi:</p><ul><li>**Abi** — mērķa lauks netiks atjaunināts, jo viena no divām ostām neatbilst.</li><li>**Avots** — mērķa lauks tiks atjaunināts, jo avota tabulas "No" ostas vērtība ir *Honkonga*.</li><li>**Mērķis** — mērķa lauks netiks atjaunināts, jo mērķa tabulas "no" osta ir *Šanhaja* (nevis *Honkonga*).</li></ul> |
| Kopēt darbību | Pieejamās vērtības ir *Kopēt* un *Noklusējums*. Atlasiet *Kopēt*, lai avota lauka vērtību iekopētu galamērķa laukā. Atlasiet *Noklusējums*, lai galamērķa laukam iestatītu statisku vērtību. |
| Noklusētā vērtība | Kad lauks **Kopēt darbību** ir iestatīts uz *Noklusējums*, lauks **Noklusējums** nosaka mērķa lauka noklusējuma vērtību. Piemēram, ja darbība ir saistīta ar porta atjaunināšanu un lauks **Kopēt darbību** ir iestatīts uz *Noklusējums*, lauks **Noklusējums** nosaka ostu. |
| Fāze | Šajā laukā ir norādīta ceļojuma posms, kurā noteikta darbība, piemēram, iekraušana vai muita. |
| Pakalpojuma sniedzējs | Ja konkrēta pakalpojumu sniedzējs tiek izmantots pašreizējā statusa atjaunināšanai/ceļojuma kājai, šis lauks identificē pakalpojuma sniedzēju. Pakalpojumu nodrošinātāji tiek definēti kreditora kontā. |

### <a name="lead-time-rules"></a>Izpildes laika kārtulas

Izpildes laiks ir plānotais laiks, kas reisam būs nepieciešams, lai veiktu reisam noteikto ceļojuma kājai kāsi. Lai aprēķinātu reisa prognozēto piegādes datumu, tiek izmantots katras ceļojuma kravas izpildes laiks. Pēc tam šis datums tiek ievadīts laukā **Apstiprinātais piegādes datums** katrā reisa pirkšanas rindā.

Lai pārvaldītu datumu atjaunināšanu, izmantojiet izpildes laika kārtulas. Aktivitātes tiek automātiski ģenerētas, kad ceļojuma veidne tiek izmantota reisam.

Lai izsekošanas kontroles centram pievienotu izpildes laika noteikumu, sekojiet šiem soļiem.

1. Izpildiet kādu no šīm darbībām:

    - Dodieties uz sadaļu **Kopīgās izmaksas \> Vairākpušu ceļojuma izmaksas iestatījumi \> Kājas**. Izvēlieties, kam vēlaties iestatīt izpildes laikus, un pēc tam Darbību rūtī izvēlieties **Izsekošanas kontroles centrs**. Izsekošanas kontroles centram tiek iepriekšēja ielādēta informācija par izvēlēto kāju.
    - Dodieties uz **Kopīgās izmaksas \> Piegādes informācijas iestatījumi \> Izsekošanas kontroles centrs**. Ir manuāli jāiestata kāja šīs procedūras 4. solī.

1. Saraksta rūtī iestatiet lauku **Izveidot tipu** uz *Izpildes laiks*.
1. Darbību rūtī atlasiet **Jauns**.
1. Ja jūs sākāt no Izsekošanas kontroles centra 1. solī, iestatiet lauku **Kāja** līdz kājai, kurai vēlaties izveidot izpildes laika kārtulu. Ja sākāt no lapas **Kājas**, laukam **Kāja** ir iestatīta priekštece, ko atlasījāt pirms Izsekošanas vadības centra atvēršanas.

    Pamatojoties uz lauka **Kāja** vērtību, automātiski tiek iestatīti vairāki lauki, kā parādīts šeit:

    - **Avota tabula:** *Konteinera aktivitātes*
    - **Avota lauks:** *Sākuma datums*
    - **Mērķa tabula:** *Konteinera aktivitātes*
    - **Mērķa lauks:** *Plānotais beigu datums*

1. Laukā **Darbība** atlasiet aktivitāti, uz kuru attiecas pašreizējā kārtula.
1. Laukā **Izpildes laiks** ievadiet izpildes laiku (dienās), kas jālieto, ja tiek izraisīta pašreizējā kārtula.

### <a name="status-update-rules"></a>Statusa atjaunināšanas kārtulas

Ieraksti, kuru lauks **Izveidot tipu** ir iestatīts uz *Statusa atjaunināšana*, atjauninās pirkšanas pasūtījuma rindu statusu vai statusu reisa, nosūtīšanas konteinera vai folio līmenī. Statusi var būt neatkarīgi iestatīti. Izmantojiet tos, lai informētu lietotāju vai nodaļu par reisa pakāpi (piemēram, saņemtos dokumentus vai tranzīta kravu).

Kad lauka **Izveidot tipu** iestatījums ir *Statusa atjaunināšana*, izsekošanas kontroles centrs ietver kopsavilkuma cilni **Rindas**, kur varat definēt izmaksu apgabalu un reisa atjaunināto statusu. Piemēram, jums ir rinda, kur **Izmaksu apgabala** lauks ir iestatīts uz *Konteiners*, un **Reisa statusa** lauks ir iestatīts uz *Tranzīta krava*. Šajā gadījumā, kad pasūtījums ir pabeigts norādītajā transportēšanas laikā, nosūtīšanas konteinera lauks **Reisa statuss** tiks atjaunināts uz *Tranzīta kravas*.

Statusa atjauninājumi nodrošina reisa statusu reisa rindās un pirkšanas pasūtījuma rindās, kas ir saistītas ar šo reisu. Kad reiss pārvietojas cauri tā ceļojumam no ostas, kuģošanas un muitas uz mērķa noliktavu, reisa ieraksta lauks **Reisa statuss** nodrošina ātru krājumu atrašanās vietas skatu.

Lai Izsekošanas kontroles centram pievienotu izpildes laika kārtul, sekojiet šiem soļiem.

1. Izpildiet kādu no šīm darbībām:

    - Dodieties uz sadaļu **Kopīgās izmaksas \> Vairākpušu ceļojuma izmaksas iestatījumi \> Kājas**. Izvēlieties kāju, kurai vēlas iestatīt statusa atjauninājumu, un pēc tam Darbību rūtī izvēlieties **Izsekošanas kontroles centrs**. Izsekošanas kontroles centram tiek iepriekšēja ielādēta informācija par izvēlēto kāju.
    - Dodieties uz **Kopīgās izmaksas \> Piegādes informācijas iestatījumi \> Izsekošanas kontroles centrs**. Ir manuāli jāiestata kāja šīs procedūras 4. solī.

1. Saraksta rūtī iestatiet lauku **Izveidot tipu** uz *Statusa atjaunināšana*.
1. Darbību rūtī atlasiet **Jauns**.
1. Ja jūs sākāt no Izsekošanas kontroles centra 1. solī, iestatiet lauku **Kāja** līdz kājai, kurai vēlaties izveidot statusa atjaunināšanas kārtulu. Ja sākāt no lapas **Kājas**, laukam **Kāja** ir iestatīta priekštece, ko atlasījāt pirms Izsekošanas vadības centra atvēršanas.

    Pamatojoties uz lauka **Kāja** vērtību, automātiski tiek iestatīti vairāki lauki, kā parādīts šeit:

    - **Avota tabula:** *Konteinera aktivitātes*
    - **Avota lauks:** *Faktiskais beigu datums*
    - **Mērķa tabula:** Šis lauks ir atstāts tukšs.
    - **Mērķa lauks:** Šis lauks ir atstāts tukšs.

1. Laukā **Darbība** atlasiet aktivitāti, uz kuru attiecas jūsu kārtula.
1. Kopsavilkuma cilnē **Rindas** ievadiet statusa atjauninājumus katrai izmaksu jomai.

### <a name="blank-type-rules"></a>Tukša tipa kārtulas

Izmantojiet ierakstus, kuru vērtība **Izveidot tipu** ir *Tukšs*, lai ignorētu vai ievadītu lauka vērtību, pamatojoties uz cita lauka datiem. Lauks no Kopīgajām izmaksām pārrakstīs datus citos Microsoft Dynamics 365 Supply Chain Management apgabalos, balstoties uz izsekošanas kontroles centrā iestatītajiem noteikumiem.

1. Dodieties uz **Kopīgās izmaksas \> Piegādes informācijas iestatījumi \> Izsekošanas kontroles centrs**.
1. Saraksta rūtī iestatiet lauku **Izveidot tipu** uz *Tukšs*.
1. Darbību rūtī atlasiet **Jauns**.
1. Definējiet avota un mērķa vērtības, atbilstības kritērijus, kopēšanas darbību un citus būtiskus parametrus, kā tas nepieciešams kārtulā.

### <a name="required-tracking-control-setup"></a>Nepieciešamais izsekošanas kontroles iestatījums

Katrai ceļojuma veidnei Izsekošanas kontroles centrā ir jāiestata divi ieraksti. Abiem šiem ierakstiem ir vērtība **Izveidot tipu** *Tukšs* un tie tiek izmantoti visās ieviestajās Kopīgajās izmaksās. Tie palīdz nodrošināt, ka ar pirkumu apstiprinātais datums un tranzītā paredzamie datumi tiek atjaunināti reisiem un ar tām saistītajām pirkšanas pasūtījuma rindām prognozētajā veidā.

Pirmais ieraksts ir nepieciešams, lai atjauninātu pirkšanas rindas. Tajā ir jābūt šādiem iestatījumiem:

- **Avota tabula:** *Konteinera aktivitātes*
- **Avota lauks:** *Plānotais beigu datums*
- **Mērķa tabula:** *Pirkšanas rindas*
- **Mērķa lauks:** *Apstiprinātais vai piegādes datums*

Otrais ieraksts ir nepieciešams, lai atjauninātu tranzīta kravu darbības. Tajā ir jābūt šādiem iestatījumiem:

- **Avota tabula:** *Konteinera aktivitātes*
- **Avota lauks:** *Plānotais beigu datums*
- **Mērķa tabula:** *Tranzīta preču pasūtījums*
- **Mērķa lauks:** *Plānotais datums*
