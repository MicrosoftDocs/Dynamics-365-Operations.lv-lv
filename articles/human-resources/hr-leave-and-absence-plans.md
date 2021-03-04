---
title: Izveidot atvaļinājumu un prombūtnes plānu
description: Izveidojiet atvaļinājumu plānus Dynamics 365 Human Resources dažādiem atvaļinājumu veidiem.
author: andreabichsel
manager: AnnBe
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cb42860292c5e3e654917cf2f62b525993aa795a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419597"
---
# <a name="create-a-leave-and-absence-plan"></a>Izveidot atvaļinājumu un prombūtnes plānu

Definējiet atvaļinājumu un prombūtnes plānus pakalpojumā Dynamics 365 Human Resources katram atvaļinājuma veidam, ko piedāvājat. Atvaļinājumu un prombūtnes plānus var uzkrāt dažādos biežumos, piemēram, reizi gadā, mēnesī vai pusmēnesī. Plānu var definēt arī kā dotāciju, veicot vienu uzkrājumu noteiktā datumā. Piemēram, var izveidot plānu, kas ik gadu piešķir peldošās brīvdienas.

Sarindotie atvaļinājumu plāni ļauj darbiniekiem saņemt atvieglojumus, pamatojoties uz laika periodu, kuru tie ir pavadījuši organizācijā. Sarindotie plāni iespējo automātisku reģistrēšanos papildu atvieglojumu laikos.

Varat norādīt maksimālās pārnestās summas vai minimālās bilances, lai nodrošinātu, ka darbinieki izmanto tikai uzkrātās atvieglojumu stundas.

Piemēram, ar sarindotu plānu varat piešķirt atvieglojumu 80 stundām apmaksātā brīvā laika (PTO) jauniem darbiniekiem. Pēc tam varat piešķirt 120 stundas par 60 mēnešiem pakalpojumu.

Varat arī veidot amatā balstītus atvieglojumus, piemēram, vienīgi vadībai paredzētas atvieglojumu stundas.

## <a name="create-a-leave-plan"></a>Atvaļinājuma plāna izveide

1. Lapā **Atvaļinājumu un prombūtnes plāni** atlasiet **Izveidot jaunu plānu**.

2. Sadaļā **Detalizēta informācija** ievadiet **Nosaukumu**, **Sākuma datumu**, **Aprakstu** un **Atvaļinājuma veidu** savam plānam.

Ja ir iespējots līdzeklis **Vairāku atvaļinājumu veidu konfigurēšana vienam atvaļinājuma un prombūtnes plānam** atvaļinājumu veidi tiek konfigurēti **Uzkrāšanas grafikā**, nevis zem **Detalizētas informācijas**. Katram ierakstam uzkrāšanas grafika tabulā varat definēt atvaļinājuma tipu. Turklāt, ja šis līdzeklis ir aktivizēts, jums vajadzēs izmantot jaunas datu entītijas integrācijām vai citiem scenārijiem, kur jāizmanto entītijas. 

Jaunās entītijas ir:

- Atvaļinājuma un kavējuma bankas transakcija V2
- Atvaļinājuma un kavējuma reģistrācija V2
- Atvaļinājuma un kavējuma plāna pakāpe V2
- Atvaļinājuma un kavējuma plāns V2
- Atvaļinājuma pieprasījums V2

 > [!IMPORTANT]
   > Šo funkciju pēc tās iespējošanas nevar atspējot.

3. Definējiet uzkrājumus cilnē **Uzkrājumi**. Uzkrājumi nosaka, kad un cik bieži darbiniekam tiek piešķirts brīvais laiks. Šajā darbībā ir jādefinē politika par to, kad ir jāpiešķir uzkrājumi, un politika par atvaļinājumu atvieglojumu likmēm.

   1. Nolaižamajā lodziņā **Uzkrāšanas biežums** atlasiet vērtību:

      - Ikdienas
      - Iknedēļas
      - Katru otro nedēļu
      - Divreiz mēnesī
      - Mēnesis
      - Reizi ceturksnī
      - Divreiz gadā
      - Reizi gadā
      - Nav

   2. Atlasiet opciju no nolaižamā lodziņa **Uzkrāšanas perioda pamats**, lai noteiktu uzkrājumu periodu aprēķinam izmantoto sākuma datumu:

      | Uzkrāšanas perioda kritērijs | Apraksts |
      | --- | --- |
      | **Plāna sākuma datums** | Uzkrāšanas perioda sākuma datums ir datums, kad plāns ir pieejams. |
      | **Darbiniekam individuāls datums** | Uzkrājumu perioda sākuma datums ir atkarīgs no darbinieka notikuma:</br><ul><li>Pielāgots (ir jānorāda uzkrāšanas datums katrai atsevišķai reģistrācijai)</li><li>Gadadienas datums</li><li>Sākotnējais darbā pieņemšanas datums</li><li>Darba stāža datums</li><li>Nodarbinātā koriģētais pieņemšanas datums</li><li>Nodarbinātā pieņemšanas datums</li></ul> |

   3. Atlasiet opciju nolaižamajā lodziņā **Uzkrājumu piešķiršanas datums**:

      - **Uzkrāšanas perioda beigu datums** - darbiniekam brīvais laiks tiek piešķirts piešķiršanas perioda pēdējā dienā. Lai uzkrātu pareizu summu, uzkrāšanas procesā ir jāiekļauj viss periods. Piemēram, ja uzkrājumu periods ir no 2020. gada 1. janvāra līdz 2020. gada 31. janvārim, ir jāpalaiž uzkrājums 2020. gada 1. februārim, lai tas iekļautu janvāri.

      - **Uzkrāšanas perioda sākuma datums** - darbiniekam brīvais laiks tiek piešķirts piešķiršanas perioda pirmajā dienā.

   4. Atlasiet opciju nolaižamajā lodziņā **Uzkrājumu reģistrēšanas politika**. Šī vērtība nosaka, kā aprēķināt uzkrāšanu, kad darbinieks piesakās uzkrāšanas perioda vidū.

      - **Proporcionāli sadalīts** - lai noteiktu starpību dienās, tiek izmantots datumu diapazons starp reģistrācijas datumu un sākuma datumu. Šī starpība tiek piemērota, kad uzkrājumi tiek apstrādāti.

      - **Pilns uzkrājums** - pirmās uzkrājumu apstrādes laikā tiek piešķirta pilna uzkrājuma summa atbilstoši pakāpei.

      - **Nav uzkrājuma** - līdz nākamajam uzkrāšanas periodam netiek piešķirts uzkrājums.

   5. Atlasiet opciju nolaižamajā lodziņā **Uzkrājumu reģistrēšanas atsaukšanas politika**. Šī vērtība nosaka, kā aprēķināt uzkrāšanu, kad darbinieks atsakās uzkrāšanas perioda vidū.

      - **Proporcionāli sadalīts** - lai noteiktu starpību dienās, tiek izmantots datumu diapazons starp reģistrācijas datumu un sākuma datumu. Šī starpība tiek piemērota, kad uzkrājumi tiek apstrādāti.

      - **Pilns uzkrājums** - pirmās uzkrājumu apstrādes laikā tiek piešķirta pilna uzkrājuma summa atbilstoši pakāpei.

      - **Nav uzkrājuma** - līdz nākamajam uzkrāšanas periodam netiek piešķirts uzkrājums.

4. Definējiet uzkrāšanas grafiku cilnē **Uzkrājumu grafiks**. Uzkrājumu grafiks nosaka:

   - Kā darbinieks uzkrāj brīvo laiku
   - Kādas summas darbinieks uzkrās
   - Kādas summas tiks pārnēsātas

   Varat izveidot pakāpes, lai piešķirtu brīvo laiku, pamatojoties uz dažādiem līmeņiem.

   Ja jums ir darbinieki ar stundu likmi, jūs varat piešķirt laika uzkrāšanu pēc jūsu organizācijā nostrādātajam stundām, nevis pēc darba stāža. Dati par nostrādātajām stundām tiek glabāti laika un apmeklētības sistēmā. Varat importēt regulārās un virsstundas, kas nostrādātas no laika un apmeklētības sistēmas un izmantot tās kā pamatu darbinieka piešķīrumam.
   
    1. Atlasiet opciju nolaižamajā lodziņā **Uzkrājuma veids**:

      - **Pakalpojumu mēneši** mēneši – Uzkrāšanas grafiks balstās pakalpojumu sniegšanas mēnešos.

      - **Nostrādātās stundas** – Uzkrājumu grafiks ir balstīts nostrādātajās stundās. Lai iegūtu vairāk informācijas par uzkrājumiem par nostrādātajām stundām, skatiet [Uzkrāšanas brīvais laiks, balstīts nostrādātajās stundās](hr-leave-and-absence-plans.md?accrue-time-off-based-on-hours-worked).

      Lai iegūtu vairāk informācijas par uzkrājumu bilancēm par nostrādātajām stundām, skatiet [Uzkrāšanas brīvais laiks, balstīts nostrādātajās stundās](hr-leave-and-absence-plans.md?enrollments-and-balances).

    2. Ievadiet vērtības uzkrāšanas grafika tabulā:

      - **Nodarbinātības mēnešu skaits** – minimālais mēnešu skaits, kas darbiniekiem jānostrādā, lai viņiem pienāktos uzkrājumi. Ja nav nepieciešams minimums, iestatiet vērtību 0.

      - **Nostrādātās stundas** – Minimālais stundu skaits, kas darbiniekiem jānostrādā uzkrāšanas periodā, lai viņiem pienāktos uzkrājumi. Ja nav nepieciešams minimums, iestatiet vērtību 0.

      - **Uzkrājumu summa** – stundu vai dienu skaits, ko darbinieki periodā uzkrāj. Periodu nosaka uzkrāšanas biežums.

      - **Minimālā bilance** – Varat izmantot negatīvu vērtību minimālajai bilancei, ja darbinieki var pieprasīt vairāk atvaļinājumu, nekā viņiem ir pieejams.

      - **Maksimālā pārnešana** - uzkrājumu process pielāgo atvaļinājumu bilanci, kas pārsniedz maksimālo pārnešanas bilanci sākuma datuma gadadienā.

      - **Garantētā summa** – Sākotnējais stundu vai dienu skaits, kas darbiniekiem tiek piešķirts, kad viņi pirmo reizi reģistrējas atvaļinājuma plānā. Summa netiek uzkrāta katram uzkrāšanas periodam.
      
Ja līdzeklis **Konfigurēt vairāku atvaļinājumu veidus vienam atvaļinājumam un prombūtnes plānam** ir iespējots, atlasiet opciju no **Atvaļinājuma veida**. 

   > [!IMPORTANT]
   > Šo funkciju pēc tās iespējošanas nevar atspējot.

Ja līdzeklis **Izmantojiet pilna laika ekvivalenci** ir iespējots, Personāla vadība izmanto pilna laika ekvivalentu (FTE), kas noteikts amatam, lai proporcionāli noteiktu darbinieka uzkrājumu. Piemēram, ja FTE ir 0,5 un uzkrājumu summa ir10, darbiniekam tiks uzkrāti 5. Šo funkciju var izmantot tikai tad, ja iespējosit vairākus atvaļinājumu veidus.  

5. Atlasiet **Saglabāt**.

## <a name="accrue-time-off-based-on-hours-worked"></a>Brīvā laika uzkrāšana, pamatojoties uz nostrādātajām stundām

Ja jums ir darbinieki ar stundu likmi, jūs varat piešķirt laika uzkrāšanu pēc jūsu organizācijā nostrādātajam stundām, nevis pēc darba stāža. Dati par nostrādātajām stundām tiek glabāti laika un apmeklētības sistēmā. Varat importēt regulārās un virsstundas, kas nostrādātas no sava laika un apmeklētības sistēmas un izmantot tās kā pamatu darbinieka piešķīrumam.

Ja atlasāt nostrādātās stundas kā uzkrāšanas veidu, varat izmantot divus stundu veidus uzkrāšanai: regulārās un virsstundas. Lai noteiktu uzkrājamo stundu skaitu, nostrādāto stundu plānu uzkrājuma apstrādē izmanto uzkrāšanas biežumu kopā ar uzkrājuma perioda kritēriju.

### <a name="annual-accrual-frequency"></a>Uzkrāšana reizi gadā

| Uzkrājuma prēmijas datums    | Nostrādāto stundu pakāpe    | Uzkrājuma summa        | Darba stundu datumi   | Faktiski nostrādāto stundu skaits| Piemaksa               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 12/31/2018            | 2080                 | 144                   | 1/1/2018-12/31/2018  | 2085                | 144                 |        
| 12/31/2018            | 2080                 | 144                   | 1/1/2018-12/31/2018  | 2000                | 0                 |


### <a name="monthly-accrual-frequency"></a>Uzkrāšana reizi mēnesī

| Uzkrājuma prēmijas datums    | Nostrādāto stundu pakāpe    | Uzkrājuma summa        | Darba stundu datumi   | Faktiski nostrādāto stundu skaits| Piemaksa               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 160                  | 12                    | 8/1/2018-8/31/2018   | 184                 | 12                  |        
| 8/31/2018             | 160                  | 3                     | 8/1/2018-8/31/2018   | 184                 | 3                   |

### <a name="semi-monthly-accrual-frequency"></a>Uzkrāšana divas reizes mēnesī

| Uzkrājuma prēmijas datums    | Nostrādāto stundu pakāpe    | Uzkrājuma summa        | Darba stundu datumi   | Faktiski nostrādāto stundu skaits| Piemaksa               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 80                   | 6.                     | 8/16/2018-8/31/2018  | 81                  | 6.                  |        
| 8/31/2018             | 80                   | 6.                     | 8/16/2018-8/31/2018  | 75                  | 0                   |

### <a name="weekly-accrual-frequency"></a>Uzkrāšana reizi nedēļā

| Uzkrājuma prēmijas datums    | Nostrādāto stundu pakāpe    | Uzkrājuma summa        | Darba stundu datumi   | Faktiski nostrādāto stundu skaits| Piemaksa               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 40                   | 3                     | 8/27/2018-8/31/2018  | 42                  | 3                  |        
| 8/31/2018             | 40                   | 3                     | 8/27/2018-8/31/2018  | 35                  | 0                   |

### <a name="employee-assigned-leave-plans"></a>Darbiniekam piešķirtie atvaļinājumu plāni

Darbiniekam piešķirtajos atvaļinājumu plānos pakāpju bāze un stundu veids uzrāda nostrādāto stundu plānus. Aktīvajos plānos tiek parādīts uzkrājuma periodos faktiski nostrādāto stundu skaits, sākot no pašreizējā datuma.

### <a name="loading-data"></a>Datu ielāde

Varat importēt faktisko stundu skaitu, izmantojot **Nostrādāto atvaļinājuma un prombūtnes stundu** elementu datu pārvaldībā. Ja tiek izmantoti darba laika kalendāri, importēšanas funkcija pārbauda, vai pastāvīgi nostrādāto stundu skaists nepārsniedz ieplānoto stundu skaitu dienā, ko nosaka kalendārs. Importēšanas funkcija arī pārbauda, vai konkrētajā dienā nostrādāto stundu skaits nepārsniedz 24 stundas. 

Tālāk sniegtā informācija ir nepieciešama, lai importētu faktisko stundu skaitu, kas jāizmanto atvaļinājuma uzkrāšanas procesā.

- Darbinieku skaits 
- Darbdienas datums
- tips
- Stundas

Uz vienu datumu var attiekties tikai viens ar to saistītais veids.

| Darbinieku skaits       | Darbdienas datums           | Tips                  | Stundas                |
| --------------------- | -------------------- | --------------------- | -------------------- |
| 000337                | 8/6/2018             | Regulārs               | 8                    |       
| 000337                | 8/7/2018             | Regulārs               | 8                    |
| 000337                | 8/7/2018             | Virsstundas              | 3                    |
| 000337                | 8/8/2018             | Regulārs               | 8                    |
| 000337                | 8/7/2018             | Regulārs               | 8                    |
| 000337                | 8/9/2018             | Regulārs               | 8                    |

## <a name="enrollments-and-balances"></a>Registrācijas un bilances

### <a name="enrollment-date"></a>Reģistrācijas datums

Reģistrācijas datums nosaka, kad darbinieks var sākt uzkrāt brīvo laiku. Piemēram, ja darbinieks tiek reģistrēts atvaļinājuma plānā 2018. gada 15. jūnijā, viņš nevar uzkrāt brīvo laiku pirms 2018. gada 15. jūnija.

### <a name="current-balance"></a>Pašreizējā bilance

Pašreizējā bilance ir atvaļinājuma apjoms, kas ir pieejams brīvā laika pieprasījumiem. Šis apjoms iekļauj uzkrājumus, apstiprinātos pieprasījumus un korekcijas līdz pašreizējam datumam.

### <a name="current-balance-examples"></a>Pašreizējās bilances piemēri

#### <a name="annual-plan"></a>Gada plāns

**Plāna iestatījumi**

| Plāna sākuma datums | Reģistrācijas datums | Uzkrāšanas biežums | Uzkrāšanas perioda kritērijs | Uzkrājuma piešķiršanas datums    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Ikgadējs            | Plāna sākuma datums      | Uzkrāšanas perioda beigu datums |

Uzkrājumi tiek apstrādāti 2019. gada 1. janvārī (1/1/2019), lai tiktu iekļauts viss periods.

**Rezultāti**

| Uzkrājuma summa | Minimālā bilance | Maksimālā pārnesamā summa | Pieprasījumu summa | Pašreizējā bilance (uz 1/1/2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 200            | 0               | 120                   | 40             | 160                              |

Pašreizējā bilance (160) = uzkrājumu summa (200) – pieprasījumu summa (40)

#### <a name="semimonthly-plan"></a>Pusmēneša plāns

**Plāna iestatījumi**

| Plāna sākuma datums | Reģistrācijas datums | Uzkrāšanas biežums | Uzkrāšanas perioda kritērijs | Uzkrājuma piešķiršanas datums    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Pusmēneša       | Plāna sākuma datums      | Uzkrāšanas perioda beigu datums |

Uzkrājumi tiek apstrādāti 2018. gada 1. maijā (5/1/2018), lai tiktu iekļauts viss periods.

**Rezultāti**

| Uzkrājuma summa | Minimālā bilance | Maksimālā pārnesamā summa | Pieprasījumu summa | Pašreizējā bilance (uz 1/1/2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5.              | 0               | 120                   | 8              | 22                               |

Pašreizējā bilance (22) = uzkrājumu summa (5 x 6) – pieprasījumu summa (8)

#### <a name="monthly-plan"></a>Mēneša plāns

**Plāna iestatījumi**

| Plāna sākuma datums | Reģistrācijas datums | Uzkrāšanas biežums | Uzkrāšanas perioda kritērijs | Uzkrājuma piešķiršanas datums    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Pusmēneša       | Plāna sākuma datums      | Uzkrāšanas perioda beigu datums |

Uzkrājumi tiek apstrādāti 2018. gada 1. maijā (5/1/2018), lai tiktu iekļauts viss periods.

**Rezultāti**

| Uzkrājuma summa | Minimālā bilance | Maksimālā pārnesamā summa | Pieprasījumu summa | Pašreizējā bilance (uz 1/1/2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5.              | 0               | 120                   | 8              | 7.                                |

Pašreizējā bilance (7) = uzkrājumu summa (5 x 3) – pieprasījumu summa (8)

### <a name="forecasted-balance"></a>Budžeta bilance

*Prognozētā bilance* ir atvaļinājuma laiks, kas ir pieejams tālākā datumā. Uzkrājumu un pārnešanas korekcijas tiek prognozētas līdz attiecīgajam datumam.

Human Resources izmanto šādu formulu:

Pirmdienai prognozētā bilance = pašreizējā bilance – pieprasījumi + uzkrājumi – pārnešanas korekcija

### <a name="forecasted-balance-examples"></a>Prognozētās bilances piemēri

#### <a name="annual-plan"></a>Gada plāns

**Plāna iestatījumi**

| Plāna sākuma datums | Reģistrācijas datums | Uzkrāšanas biežums | Uzkrāšanas perioda kritērijs | Uzkrājuma piešķiršanas datums    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Ikgadējs            | Plāna sākuma datums      | Uzkrāšanas perioda beigu datums |

Uzkrājumi tiek apstrādāti 2019. gada 15. februārī (2/15/2019), lai tiktu iekļauts viss periods.

**Rezultāti**

| Uzkrājuma summa | Minimālā bilance | Maksimālā pārnesamā summa | Pašreizējā bilance | Prognozētā bilance (uz 2/15/2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 20.             | 0               | 20.                    | 40              | 40                                   |

Prognozētā bilance (40) = uzkrājumu summa (20) + pašreizējā bilance (40) – pārnešanas korekcija (20)

#### <a name="semimonthly-plan"></a>Pusmēneša plāns

**Plāna iestatījumi**

| Plāna sākuma datums | Reģistrācijas datums | Uzkrāšanas biežums | Uzkrāšanas perioda kritērijs | Uzkrājuma piešķiršanas datums    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Pusmēneša       | Plāna sākuma datums      | Uzkrāšanas perioda beigu datums |

Uzkrājumi tiek apstrādāti 2019. gada 15. februārī (2/15/2019), lai tiktu iekļauts viss periods.

**Rezultāti**

| Uzkrājuma summa | Minimālā bilance | Maksimālā pārnesamā summa | Pašreizējā bilance | Prognozētā bilance (uz 2/15/2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 5.              | 0               | 20.                    | 40              | 35                                   |

Prognozētā bilance (35) = uzkrājumu summa (5 x 3) + pašreizējā bilance (40) – pārnešanas korekcija (20)

#### <a name="monthly-plan"></a>Mēneša plāns

**Plāna iestatījumi**

| Plāna sākuma datums | Reģistrācijas datums | Uzkrāšanas biežums | Uzkrāšanas perioda kritērijs | Uzkrājuma piešķiršanas datums    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Pusmēneša       | Plāna sākuma datums      | Uzkrāšanas perioda beigu datums |

Uzkrājumi tiek apstrādāti 2019. gada 15. februārī (2/15/2019), lai tiktu iekļauts viss periods.

**Rezultāti**

| Uzkrājuma summa | Minimālā bilance | Maksimālā pārnesamā summa | Pašreizējā bilance | Prognozētā bilance (uz 2/15/2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 10.             | 0               | 20.                    | 40              | 30                                   |

Prognozētā bilance (30) = uzkrājumu summa (10 x 1) + pašreizējā bilance (40) – pārnešanas korekcija (20)

### <a name="proration-balance-examples"></a>Proporcionālā sadalījuma bilances piemēri

#### <a name="prorated-monthly-plan"></a>Proporcionāli sadalītais mēneša plāns

**Plāna iestatījumi**

| Plāna sākuma datums | Uzkrāšanas biežums | Uzkrāšanas perioda kritērijs |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Mēnesis           | Plāna sākuma datums      |

**Rezultāti**

| Darbinieks            | Nodarbinātības mēnešu skaits | Reģistrācijas datums | Sākuma datums | Uzkrājuma summa | Apstrādātais uzkrājums | Bilance |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Žanete Nikolsone | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Džejs Normans          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 2,53    |

#### <a name="full-accrual-monthly-plan"></a>Pilna uzkrājuma mēneša plāns

**Plāna iestatījumi**

| Plāna sākuma datums | Uzkrāšanas biežums | Uzkrāšanas perioda kritērijs |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Mēnesis           | Plāna sākuma datums      |

**Rezultāti**

| Darbinieks            | Nodarbinātības mēnešu skaits | Reģistrācijas datums | Sākuma datums | Uzkrājuma summa | Apstrādātais uzkrājums | Bilance |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Žanete Nikolsone | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Džejs Normans          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 3,00    |

#### <a name="no-accrual-monthly-plan"></a>Mēneša bez uzkrājuma plāns

**Plāna iestatījumi**

| Plāna sākuma datums | Uzkrāšanas biežums | Uzkrāšanas perioda kritērijs |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Mēnesis           | Plāna sākuma datums      |

**Rezultāti**

| Darbinieks            | Nodarbinātības mēnešu skaits | Reģistrācijas datums | Sākuma datums | Uzkrājuma summa | Apstrādātais uzkrājums | Bilance |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Žanete Nikolsone | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3.00    |
| Džejs Normans          | 0.00              | 6/15/2018       | 6/15/2018  | 1.00           | 9/1/2018        | 2.00    |

## <a name="see-also"></a>Skatiet arī

- [Atvaļinājumu un kavējumu apskats](hr-leave-and-absence-overview.md)
- [Konfigurēt atvaļinājumu un kavējumu veidus](hr-leave-and-absence-types.md)
- [Atvaļinājumu un prombūtnes plānu uzkrāšana](hr-leave-and-absence-accrue.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]