---
title: Atvaļinājumu un kavējumu jēdzieni
description: Šajā tēmā ir aprakstīti atvaļinājumu un kavējumu jēdzieni un brīvā laika bilanču noteikšanas principi.
author: jcart
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 563593d6c93b0488c681f5b43004f5c0d22cc004
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "305383"
---
# <a name="leave-and-absence-concepts"></a>Atvaļinājumu un kavējumu jēdzieni

[!include[banner](../includes/banner.md)]

Jēdzieni un noteikumi, kas ir aprakstīti šajā tēmā, var palīdzēt noteikt, kā darbiniekam tiek piešķirts brīvais laiks un kā tiek aprēķinātas šī darbinieka laika bilances. Papildinformāciju par atvaļinājumu un kavējumu pārvaldību skatiet tēmā [Atvaļinājumu un kavējumu pārvaldība](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).

## <a name="leave-plan-details"></a>Detalizēta informācija par atvaļinājuma plānu

### <a name="start-date"></a>Sākuma datums

Sākuma datums ir datums, kurā sākas uzkrājumu apstrāde. Sākuma datums ir arī gadadienas datums, ko izmanto, lai aprēķinātu pārnestās summas.

## <a name="accruals"></a>Uzkrājumi

Uzkrājumi nosaka, kad un cik bieži darbiniekam tiek piešķirts brīvais laiks. Uzkrājumu piešķiršanas politika un proporcionalitātes politika tiek definēta sadaļā **Uzkrājumi**, kad iestatāt atvaļinājuma un kavējuma plānu.

### <a name="accrual-frequency"></a>Uzkrāšanas biežums

Uzkrāšanas biežums nosaka, cik bieži atvaļinājums tiek uzkrāts vai piešķirts. Ir pieejamas tālāk minētās opcijas.

- Ikdienas
- Iknedēļas
- Katru otro nedēļu
- Pusmēneša
- Mēnesis
- Ceturkšņa
- Divreiz gadā
- Reizi gadā
- Neviens

### <a name="accrual-period-basis"></a>Uzkrāšanas perioda kritērijs

Uzkrāšanas perioda kritērijs nosaka datumu, kas tiek izmantots, lai aprēķinātu uzkrāšanas periodu. Ir pieejamas tālāk minētās opcijas.

- **Plāna sākuma datums**
- **Darbiniekam noteikts datums** — ja ir atlasīta šī opcija, vērtība nosaka sākotnējā datuma vērtības avotu, kas tiek izmantots, lai aprēķinātu uzkrāšanas periodus. Ir pieejamas tālāk minētās opcijas.

    - Pielāgot
    - Gadadienas datums
    - Sākotnējais darbā pieņemšanas datums
    - Darba stāža datums
    - Nodarbinātā koriģētais pieņemšanas datums
    - Nodarbinātā pieņemšanas datums

### <a name="accrual-award-date"></a>Uzkrājuma piešķiršanas datums

Uzkrājuma piešķiršanas datums nosaka, kad darbiniekam tiek piešķirts brīvais laiks. Ir pieejamas tālāk minētās opcijas.

- **Uzkrāšanas perioda beigu datums** — darbiniekam brīvais laiks tiks piešķirts piešķiršanas perioda pēdējā dienā.

    Lai uzkrātu pareizu summu, uzkrāšanas procesā ir jāiekļauj viss periods. Piemēram, uzkrāšanas periods ir no 2018. gada 1. janvāra līdz 2018. gada 31. janvārim. Šajā gadījumā, lai janvāris tiktu iekļauts periodā, uzkrāšanas beigu datumam ir jābūt 2018. gada 1. februārī.

- **Uzkrāšanas perioda sākuma datums** — darbiniekam brīvais laiks tiks piešķirts piešķiršanas perioda pirmajā dienā.

### <a name="accrual-policy-on-enrollment"></a>Uzkrājuma politika reģistrācijas gadījumā

Uzkrājuma politika reģistrācijas gadījumā nosaka, kā tiek aprēķināts uzkrājums, kad darbinieks ir reģistrēts uzkrāšanas perioda vidū. Ir pieejamas tālāk minētās opcijas.

- **Proporcionāli sadalīts** — lai noteiktu starpību dienās, tiek izmantots datumu diapazons starp reģistrācijas datumu un sākuma datumu. Šī starpība tiek piemērota, kad uzkrājumi tiek apstrādāti.
- **Pilns uzkrājums** — pirmās uzkrājumu apstrādes laikā tiek piešķirta pilna uzkrājuma summa atbilstoši pakāpei.
- **Nav uzkrājuma** — līdz nākamajam uzkrāšanas periodam netiek piešķirts uzkrājums.

### <a name="accrual-policy-on-unenrollment"></a>Uzkrājuma politika reģistrācijas pārtraukšanas gadījumā

Uzkrājuma politika reģistrācijas pārtraukšanas gadījumā nosaka, kā tiek aprēķināts uzkrājums, kad darbinieka reģistrācija tiek pārtraukta uzkrāšanas perioda vidū. Ir pieejamas tālāk minētās opcijas.

- **Proporcionāli sadalīts** — lai noteiktu starpību dienās, tiek izmantots datumu diapazons starp reģistrācijas datumu un sākuma datumu. Šī starpība tiek piemērota, kad uzkrājumi tiek apstrādāti.
- **Pilns uzkrājums** — pirmās uzkrājumu apstrādes laikā tiek piešķirta pilna uzkrājuma summa atbilstoši pakāpei.
- **Nav uzkrājuma** — līdz nākamajam uzkrāšanas periodam netiek piešķirts uzkrājums.

## <a name="accrual-schedule"></a>Uzkrāšanas grafiks

Uzkrāšanas grafiks nosaka, kā darbinieks uzkrās brīvo laiku un kādas summas šis darbinieks varēs uzkrāt un pārnest. Pakāpes var izveidot tā, lai brīvais laiks tiktu piešķirts, pamatojoties uz dažādiem līmeņiem.

### <a name="months-of-service"></a>Nodarbinātības mēnešu skaits

**Nodarbinātības mēnešu skaits** vērtība nosaka minimālo mēnešu skaitu, kas darbiniekiem jānostrādā, lai viņiem pienāktos uzkrājumi. Ja minimālais skaits nav nepieciešams, iestatiet vērtību **0**.

### <a name="hours-worked"></a>Nostrādātās stundas

**Nostrādātās stundas** vērtība nosaka minimālo stundu skaitu, kas darbiniekiem jānostrādā uzkrāšanas periodā, lai viņiem pienāktos uzkrājumi. Ja minimālais skaits nav nepieciešams, iestatiet vērtību **0**.

### <a name="accrual-amount"></a>Uzkrājuma summa

Uzkrājumu summa ir stundu vai dienu skaits, ko darbinieki periodā uzkrāj. Periodu nosaka uzkrāšanas biežums.

### <a name="minimum-balance"></a>Minimālā bilance

Negatīvu vērtību var izmantot minimālajai bilancei, ja darbinieki var pieprasīt vairāk atvaļinājumu, nekā viņiem ir pieejams.

### <a name="maximum-carry-forward"></a>Maksimālā pārnesamā summa

Uzkrāšanas procesā atvaļinājumu bilances, kas pārsniedz maksimālo pārnešanas bilanci, tiks pielāgotas sākuma datuma gadadienā.

### <a name="grant-amount"></a>Garantētā summa

Garantētā summa ir sākotnējais stundu vai dienu skaits, kas darbiniekiem tiek piešķirts, kad viņi pirmo reizi reģistrējas atvaļinājuma plānā. Summa netiek uzkrāta katram uzkrāšanas periodam.

## <a name="enrollments-and-balances"></a>Registrācijas un bilances

### <a name="enrollment-date"></a>Reģistrācijas datums

Reģistrācijas datums nosaka, kad darbinieks var sākt uzkrāt brīvo laiku. Piemēram, ja darbiniece tiek reģistrēta atvaļinājuma plānā 2018. gada 15. jūnijā, viņa nevar uzkrāt brīvo laiku pirms 2018. gada 15. jūnija.

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

### <a name="forecasted-balance"></a>Prognozētā bilance

*Prognozētā bilance* ir atvaļinājuma laiks, kas ir pieejams tālākā datumā. Uzkrājumu un pārnešanas korekcijas tiek prognozētas līdz attiecīgajam datumam.

Tiek izmantota šāda formula:

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
| Žanete Nikolsone | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Džejs Normans          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 2,00    |
