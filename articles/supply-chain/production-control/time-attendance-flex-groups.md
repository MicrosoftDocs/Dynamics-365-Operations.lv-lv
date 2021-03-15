---
title: Brīvā režīma grupas
description: Šajā tēmā ir aprakstīts, kā brīvā režīma grupas tiek izmantotas sadaļā Laiks un apmeklētība.
author: johanhoffmann
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgFlexGroup, JmgFlexCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 1e12874e3395ec47a6b76809b92c26e20fb14197
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980910"
---
# <a name="flex-groups"></a>Brīvā režīma grupas

[!include[banner](../includes/banner.md)]

Brīvā režīma grupas ļauj uzņēmumiem samazināt maksājumus par virsstundām, piedāvājot darbiniekiem papildu brīvo laiku tādos periodos, kad darba noslodze ir zema. Šis līdzeklis ir noderīgs, piemēram, tādos segmentos, kuros darba noslodzei ir novērojamas sezonālas izmaiņas.

Brīvā režīma grupas varat izmantot, lai darbinieku brīvā režīma darba laikam iestatītu tālāk norādītās kārtulas un principus.

- Kārtulas brīvā režīma noteikumiem
- Princips darbinieka brīvā režīma bilances aprēķināšanai

## <a name="set-up-flexible-working-hours-in-flex-groups"></a>Brīvā režīma darba laika iestatīšana brīvā režīma grupās

- Lai iestatītu brīvā režīma grupas brīvā režīma darba laikam, atlasiet **Laiks un apmeklētība** \> **Iestatīšana** \> **Grupas** \> **Brīvā režīma grupas**.

## <a name="associate-workers-with-flex-groups"></a>Darbinieku saistīšana ar brīvā režīma grupām

- Atlasiet **Laiks un apmeklētība** \> **Iestatīšana** \> **Laika reģistrācijas darbinieki**.

## <a name="rules-for-flex-regulations"></a>Kārtulas brīvā režīma noteikumiem

Brīvā režīma noteikumiem varat izmantot kārtulas, lai definētu brīvā režīma ierobežojumus, kā arī minimālo un maksimālo stundu skaitu, kas ir atļauts darbinieka brīvā režīma kontā. Brīvā režīma ierobežojumi tiek iestatīti brīvā režīma grupām. Ja brīvā režīma ierobežojumi tiek pārsniegti, darbinieka brīvā režīma bilanci un apmaksu var koriģēt.

Ja tiek pārsniegts darbiniekam atļautais brīvā režīma minimums (tas ir, ja stundu skaits brīvā režīma kontā ir mazāks par norādīto minimālo), lai koriģētu darbinieka brīvā režīma bilanci, izveidojot brīvā režīma noteikumus, varat lietot tālāk aprakstītās metodes.

- Darbinieka brīvā režīma kontu var koriģēt līdz norādītajam atļautajam minimumam, bet neatskaitot darbinieka apmaksu par darba stundu skaitu, kāds brīvā režīma kontā pietrūkst līdz atļautajam minimumam.
- Darbinieka apmaksu var atskaitīt par stundu skaitu, kāds brīvā režīma kontam pietrūkst līdz atļautajam minimumam. Šis atskaitījums tiek veikts, ģenerējot apmaksas elementus noteiktam apmaksas tipam, kam ir negatīva vai pozitīva apmaksas vienība.

Ja tiek pārsniegts darbinieka atļautais brīvā režīma maksimums, darbinieka brīvā režīma bilances koriģēšanai, izveidojot brīvā režīma noteikumus, varat izmantot tālāk aprakstītās metodes.

- Darbinieka brīvā režīma kontu var koriģēt atpakaļ uz norādīto atļauto maksimumu, bet nekompensējot darbinieka apmaksu par darba stundu skaitu, kādu darbinieks nostrādāja, pārsniedzot atļauto maksimumu.
- Stundu skaitu, par kādu darbinieks pārsniedza atļauto maksimālo darba stundu skaitu, var konvertēt uz apmaksu. Šī konvertēšana tiek veikta, ģenerējot apmaksas elementus noteiktam apmaksas tipam.

Brīvā režīma bilanci varat koriģēt tālāk norādītajos laikos.

- Kad uz algu datiem balstīts maksājuma fails tiek eksportēts, izmantojot darbu **Pārsūtīt apmaksu**. Algu dati tiek ģenerēti, kad pārsūtat darbinieka reģistrāciju no lapas **Apstiprināt**.
- Kad tiek apstrādāts darbs **Koriģēt brīvā režīma bilanci**.

> [!NOTE]
> Brīvā režīma noteikumi nerodas lapas **Apstiprināt** darbinieku reģistrāciju ikdienas apstiprināšanas un pārsūtīšanas laikā.

## <a name="principle-for-calculating-a-workers-flex-balance"></a>Princips darbinieka brīvā režīma bilances aprēķināšanai

Princips, pēc kura aprēķināt stundu skaitu, par kādu tiek koriģēta darbinieka brīvā režīma bilance, ir iestatīts brīvā režīma grupai. Atlasiet **Laiks un apmeklētība** \> **Iestatīšana** \> **Grupas** \> **Brīvā režīma grupas**. 

Var lietot divus tālāk norādītos principus.

- **Laiks** — darbinieka brīvā režīma stundu skaits tiek aprēķināts tikai no darbinieka reģistrētā laika attiecīgajai dienai. Kad tiek rēķinātas darbinieka ikdienas reģistrācijas, stundu skaits “Brīvais režīms+” un “Brīvais režīms-” attiecīgajai dienai tiek aprēķināts no joslām “Brīvais režīms+” un “Brīvais režīms-”, kas ir definētas darbinieka laika profilā.
- **Apmaksas tipi** — darbinieka brīvā režīma stundu skaits tiek aprēķināts, pamatojoties uz ienākumiem ar apmaksas tipu “Brīvais režīms+” un “Brīvais režīms-”, kas ir definēti darbinieka apmaksas līgumā. Apmaksas līgums ir saistīts ar laika reģistrācijas darbinieku. Jums var būt nepieciešams izmantot apmaksas tipus, lai pārvaldītu brīvā režīma kontus, ja, piemēram, vēlaties palielināt darbinieka brīvā režīma kontu par noteiktu koeficientu vienā vai vairākās brīvā režīma joslās.

### <a name="scenario-1-adjusting-a-workers-pay-and-flex-account-because-the-allowed-flex-minimum-is-exceeded"></a>1. scenārijs. Darbinieka apmaksas un brīvā režīma konta koriģēšana, jo ir pārsniegts atļautais brīvā režīma minimums

Darbiniekam, kurš var strādāt brīvajā režīmā, ir negatīvs brīvā režīma konts.

- **Brīvā režīma konts:** -4

Darbinieks ir saistīts ar brīvā režīma grupu, kurai ir tālāk norādītā konfigurācija.

- **Brīvā režīma minimums:** -0,5
- **Minimālās apmaksas tips:** 1302
- **Apmaksas tipa koeficients:** -1,00

Kā norāda starpība starp darbinieka brīvā režīma kontu un darbiniekam atļauto brīvā režīma minimumu, darbinieks sev atļauto brīvā režīma minimumu ir pārsniedzis par 3,5 stundām.

Kad algu administrators pārsūta darbinieka apmaksas datus, izpildot darbu **Pārsūtīt uz apmaksu** vai **Brīvā režīma korekcija**, tiek veiktas tālāk norādītās korekcijas.

- Darbinieka brīvā režīma konts tiek koriģēts par 3,5 stundām. Tādēļ -4,0 stundu brīvā režīma bilance tiek koriģēta uz darbiniekam atļauto -0,5 stundu brīvā režīma minimumu.
- Tiek izveidots apmaksas elements apmaksas tipam 1302. Šim apmaksas elementam ir apmaksas vienība -3,5 stundas, kuras tiks atskaitītas no darbinieka apmaksas. Šajā gadījumā apmaksas vienība ir negatīvs skaitlis, jo 3,5 stundu pozitīvā korekcija tiek reizināta ar negatīvu apmaksas tipa koeficientu -1,0, kurš ir definēts brīvā režīma grupai. Šis apmaksas elements būs daļa no apmaksas faila, kas tiek ģenerēts ar darbu **Pārsūtīt uz apmaksu**.

### <a name="scenario-2-adjusting-a-workers-pay-and-flex-account-because-the-allowed-flex-maximum-is-exceeded"></a>2. scenārijs. Darbinieka apmaksas un brīvā režīma konta koriģēšana, jo ir pārsniegts atļautais brīvā režīma maksimums

Darbiniekam, kurš var strādāt brīvajā režīmā, ir pozitīvs brīvā režīma konts.

- **Brīvā režīma konts:** 6

Darbinieks ir saistīts ar brīvā režīma grupu, kurai ir tālāk norādītā konfigurācija.

- **Brīvā režīma maksimums:** 2,0
- **Minimālās apmaksas tips:** 1302
- **Apmaksas tipa koeficients:** -1,0

Kā norāda starpība starp darbinieka brīvā režīma kontu un darbiniekam atļauto brīvā režīma maksimumu, darbinieks sev atļauto brīvā režīma maksimumu ir pārsniedzis par 4,0 stundām.

Kad algu administrators pārsūta darbinieka apmaksas datus, izpildot darbu **Pārsūtīt uz apmaksu** vai **Brīvā režīma korekcija**, tiek veiktas tālāk norādītās korekcijas.

- Darbinieka brīvā režīma konts tiek koriģēts par -4,0 stundām. Tādēļ 6,0 stundu brīvā režīma bilance tiek koriģēta uz darbiniekam atļauto 2,0 stundu brīvā režīma maksimumu.
- Tiek izveidots apmaksas elements apmaksas tipam 1302. Šim apmaksas elementam ir apmaksas vienība 4,0 stundas, kuras tiks pieskaitītas darbinieka apmaksai. Šajā gadījumā apmaksas vienība ir pozitīvs skaitlis, jo 4,0 stundu negatīvā korekcija tiek reizināta ar negatīvu apmaksas tipa koeficientu -1,0, kurš ir definēts brīvā režīma grupai. Šis apmaksas elements būs daļa no apmaksas faila, kas tiek ģenerēts ar darbu **Pārsūtīt uz apmaksu**.

### <a name="scenario-3-managing-a-workers-flex-balance-based-on-pay-types"></a>3. scenārijs. Darbinieku brīvā režīma bilances pārvaldīšana, pamatojoties uz apmaksas tipiem

Kā jau paskaidrojām iepriekš, brīvā režīma kontus var pārvaldīt, pamatojoties uz laiku, kas ir reģistrēts joslās “Brīvais režīms+” un “Brīvais režīms-”, kuras ir definētas darbinieka laika profilā, vai pamatojoties uz apmaksas tipiem, kuri ir definēti darbinieka apmaksas līgumos. Ja tiek lietoti apmaksas tipi, darbinieka brīvā režīma konts tiek koriģēts par apmaksas elementiem, kuri tiek ģenerēti, kad pārsūtat darbinieka reģistrāciju no lapas **Apstiprināt**. Jums var būt nepieciešams izmantot apmaksas tipus, lai pārvaldītu brīvā režīma kontus, ja, piemēram, vēlaties palielināt darbinieka brīvā režīma kontu par noteiktu koeficientu vienā vai vairākās brīvā režīma joslās.

Šajā scenārijā tiek izmantots tālāk norādītais brīvā režīma profils, kas atbilst darbdienai.

| Profila tips  | Sākums    | Beigas      |
|---------------|----------|----------|
| Brīvais režīms+         | 12:00 | 08:00 |
| Ierašanās laiks      | 08:00 | 08:00 |
| Brīvais režīms-         | 08:00 | 09:00 |
| Standarta laiks | 09:00 | 11:30 |
| Apmaksāts pārtraukums    | 11:30 | 12:00 |
| Brīvais režīms-         | 12:00 | 04:00 |
| Aiziešanas laiks     | 04:00 | 04:00 |
| Brīvais režīms+         | 04:00 | 12:00 |

Šajā gadījumā jūs vēlaties spēt pārvaldīt darbinieka brīvā režīma bilanci, pamatojoties uz apmaksas tipiem. Tāpēc darbinieka brīvā režīma grupā opcija **Pamatojas uz apmaksas tipiem** jums ir jāiestata uz **Jā**.

Lai ņemtu vērā brīvā režīma stundas, jums ir jādefinē arī jauns apmaksas tips. Šim scenārijam apmaksas tips tiek nosaukts par **FlexCnt**.

| Apmaksas tips | Apraksts  |
|----------|--------------|
| FlexCnt  | Brīvā režīma skaitītājs |

Pēc tam izpildiet tālāk aprakstītās darbības, lai iestatītu apmaksas tipu un apmaksas profilam pievienotu jaunā tipa rindas.

1. Atlasiet **Laiks un apmeklētība** \> **Iestatīšana** \> **Grupas** \> **Brīvā režīma grupas** un pēc tam atlasiet **Jauns**.
2. Gan laukā **Brīvais režīms+**, gan laukā **Brīvais režīms-** norādiet jauno apmaksas tipu — **FlexCnt**.
3. Atlasiet **Laiks un apmeklētība** \> **Iestatīšana** \> **Apmaksas līgumi** un pēc tam atlasiet **Līguma rindas**.
4. Vienumam **Pirmdiena**, profila tipam **Brīvais režīms+** pievienojiet trīs tālāk norādītās rindas.

    | Apmaksas tips | Apraksts  | No plkst. | Līdz plkst.  | Minimums | Maksimums | Koeficients |
    |----------|--------------|-----------|----------|---------|---------|--------|
    | FlexCnt  | Brīvā režīma skaitītājs | 12:00  | 18:00 | 00,00   | 00,00   | 1,00   |
    | FlexCnt  | Brīvā režīma skaitītājs | 18:00  | 24:00 | 00,00   | 02,00   | 1,50   |
    | FlexCnt  | Brīvā režīma skaitītājs | 18:00  | 24:00 | 02,00   | 06,00   | 2,00   |

    > [!NOTE]
    > Katra rinda tiek izmantota atšķirīgam laika intervālam, un tai ir atšķirīgs koeficients. Brīvā režīma stundu skaits, ko darbinieks strādā kādā laika intervālā, tiek reizināts ar attiecīgās rindas koeficientu. Piemēram, nostrādāto stundu skaits periodā no 18:00 līdz 20:00 tiek reizināts ar 1,50. Koeficients ir norādīts lapas **Apmaksas līguma rindas** cilnes **Vispārīgi** laukā **Koeficients**.

Darbinieks par šo dienu ievada tālāk norādītās reģistrācijas.

| Žurnāla reģistrācijas tips | Sākums    | Beigas      |
|---------------------------|----------|----------|
| Ierašanās laiks                  | 07:00 | 07:00 |
| Ražošanas darbs            | 07:00 | 21:00 |
| Aiziešanas laiks                 | 21:00 | 21:00 |

Maksājamā summa tiek aprēķināta lapā **Apstiprināt**, pamatojoties uz darbinieka reģistrāciju. Kad reģistrācija ir aprēķināta, rezultātu varat apskatīt cilnē **Laiki**. Šajā scenārijā jūs interesē tālāk norādītie lauki.

| Brīvais režīms+ | Brīvais režīms- | Laiks  | Apmaksājamais laiks |
|--------|--------|-------|----------|
| 6,00   | 0.00   | 13,50 | 08,00    |

Laika “Brīvais režīms+” daudzums ir sešas stundas, un aprēķins ir balstīts ir brīvā režīma joslām laika profilā. Šis daudzums sastāv no vienas stundas laika “Brīvais režīms+” no 07:00 līdz 08:00, un no piecām stundām laika “Brīvais režīms-” no 16:00 līdz 21:00.

Pārsūtot reģistrācijas, jūs ievērosiet, ka laiks “Brīvais režīms+” no 6,0 stundām tiek mainīts uz 8,0 stundām.

| Brīvais režīms+ | Brīvais režīms- | Laiks  | Apmaksājamais laiks |
|--------|--------|-------|----------|
| 8,00   | 0,00   | 13,50 | 08,00    |

Šīs izmaiņas pēc pārsūtīšanas rodas tāpēc, ka brīvā režīma stundu skaits ir aprēķināts, pamatojoties uz apmaksas tipiem, nevis uz laiku. Nākamajā tabulā ir redzams, kā tiek aprēķinātas šīs astoņas stundas.

| No     | Līdz       | Laiks | Koeficients    | Brīvā režīma konts |
|----------|----------|------|-----------|--------------|
| 07:00 | 08:00 | 1    | 1         | 1            |
| 16:00 | 18:00 | 2    | 1         | 2            |
| 18:00 | 20:00 | 2    | 1,5       | 3            |
| 20:00 | 21:00 | 1    | 2         | 2            |
|          |          |      | **Kopā** | **8**        |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]