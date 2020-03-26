---
title: Statisko dimensiju elementu un statistisko mēru nodrošinātāju veidnes
description: Šajā tēmā ir sniegta informācija par statistisko dimensiju elementu un statistisko mēru nodrošinātāju veidnēm. Statistiskos dimensiju elementus var izmantot kā sadalījuma pamatu politikās, piemēram, izmaksu sadalē un izmaksu sadalījumā. Tos var izmantot arī, lai izveidotu izmaksu patēriņa pārskatu beznaudas vērtībām.
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerSourceEntryProvider, CAMStatisticalDimension, CAMAXStatisticalMeasureProviderTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c46a9e042482ad66e769383b4e81e2df85a5e97b
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124524"
---
# <a name="statistical-dimension-members-and-statistical-measure-provider-templates"></a>Statisko dimensiju elementu un statistisko mēru nodrošinātāju veidnes

[!include [banner](../includes/banner.md)]

Statistiskās dimensijas un tās elementus izmanto, lai izmaksu uzskaitē reģistrētu un kontrolētu ierakstus beznaudas vērtībām. Statistiskās dimensijas elementus var izmantot divējādi:

- Kā sadalījuma pamatu politikās, piemēram, izmaksu sadalē vai izmaksu sadalījumā
- Beznaudas patēriņa pārskatu izveidē

## <a name="statistical-dimension"></a>Statiskā dimensija

Statistiskajai dimensijai ir unikāls nosaukums un unikālu dimensiju elementu kopa. Statistiskā dimensija tiek piešķirta izmaksu uzskaites Virsgrāmatas ID. Šīs attiecības saista visus atbilstošos statistiskos dimensijas elementus ar izmaksu uzskaites virsgrāmatu. Tāpēc visi statistiskie ieraksti tiks izveidoti saistībā ar izmaksu uzskaites virsgrāmatu.

> [!NOTE]
> Statistiskā dimensija var tikt piešķirta vairākām izmaksu uzskaites virsgrāmatām.

Tālāk ir sniegts statistiskās dimensijas piemērs.

| Nosaukums                        | Dimensijas elementu datu savienotājs |
|-----------------------------|--------------------------------------|
| Koplietojami statistiskie elementi | Importētie dimensijas elementi           |

Tālāk ir sniegts statistiskās dimensijas piemērs, kas tika piešķirta izmaksu uzskaites virsgrāmatai.

| Nosaukums                  | Uzskaites valūta | Maiņas kursa veids | Finanšu kalendārs | Izmaksu elementa dimensija | Statiskā dimensija       |
|-----------------------|---------------------|--------------------|-----------------|------------------------|-----------------------------|
| Pārvaldības uzskaite | USD                 | Konstanta valūta  | Fiskālais periods   | Koplietojami izmaksu elementi   | Koplietojami statistiskie elementi |

## <a name="statistical-dimension-members"></a>Statiski dimensiju elementi

Statistiskie dimensiju elementi pārstāv elementu, kam vēlaties reģistrēt beznaudas mērījumus. Šos mērījumus var izmantot kā sadalījuma pamatu, vai arī, lai vienkārši veidotu pārskatu par beznaudas vērtībām.

Statistisko dimensiju elementus var izveidot manuāli. Tos var arī importēt no faila, izmantojot Datu pārvaldības importēšanas/eksportēšanas rīku.

Statistiskais dimensijas elements automātiski kļūst par sākotnēji definētu sadalījuma pamatu. To var izmantot kā sadalījuma pamatu politikās vai kā ievadi cita veida sadalījuma pamatos.

Tālāk ir daži parastu statistisko dimensijas elementu piemēri.

| Statistiskās dimensijas nosaukums  | Statistiskie elementi | Apraksts             | Vienība |
|-----------------------------|----------------------|-------------------------|------|
| Koplietojami statistiskie elementi | FTE                  | Pilnas slodzes darbinieki     | gab.  |
| Koplietojami statistiskie elementi | Elektrība          | Elektroenerģijas patēriņš | kWh  |
| Koplietojami statistiskie elementi | Pakotnes kopija              | Iepakojuma izmaksu centrs   | h |

## <a name="statistical-measure-provider-template"></a>Statistisko mērījumu nodrošinātāja veidne

Statistiskos mērījumus var iegūt no dažāda veida avotiem. Dynamics 365 Finance ir lielisks statistisko mēru ieguves avots. Statistisko mērvienību nodrošinātāja veidni var izmantot, lai viegli konfigurētu statistiskos mērījumus, kurus vēlaties izgūt.

Statistisko mērījumu nodrošinātāja veidnes definīcija ir vispārīga, un to var atkārtoti izmantot vairākiem statistiskajiem dimensijas elementiem.

> [!NOTE]
> Visas tabulas, kurās ir ietvertas finanšu dimensijas, var izmantot kā statistiskos mērījumu avotus.

**Piemērs: darbinieku skaits pa izmaksu centriem**

Darbinieku skaits pa izmaksu centriem ir statistisks mērījums, ko var izmantot dažādiem nolūkiem, kas sniedz pārvaldības ieskatu:

- Statistisks pārskatu veidošanas mērījums pēc izmaksu centra
- Sadalījuma bāze dažāda veida izdevumiem
- Iekšējo izmaksu likmes pēc izmaksu centra:

    - Izmaksas pēc darbiniekiem
    - Ieņēmumi pēc darbiniekiem

Tabulā HcmEmployment ir iekļauts visu instancē esošo darbinieku saraksts. Šī ir globāla tabula. Tādēļ ieraksti nav saistīti ar specifisku datu apgabala ID.

Tālāk ir darbinieku piemērs tabulā HcmEmployment.

| Nosaukums       | Izmaksu centrs | Apraksts   | Nodarbinātā veids |
|------------|-------------|----|-------------|
| 1. darbinieks | CC001       | HR | Darbinieks    |
| 2. darbinieks | CC002       | FI | Darbinieks    |
| 3. darbinieks | CC002       | FI | Darbinieks    |
| 4. darbinieks | CC003       | KrP | Darbinieks    |
| 5. darbinieks | CC003       | KrP | Darbinieks    |
| 6. darbinieks | CC002       | FI | Līgumdarbinieks  |

Kad veidojat ierakstu **Statistisko mērījumu nodrošinātāja veidne**, ir jāizlemj, kuru funkciju izmantot:

- **Skaits** — tiek pārsūtīts ierakstu skaits pēc izmaksu objekta.
- **Summa** — tiek pārsūtīta ierakstu summa pēc izmaksu objekta. (Lauks **Summa** un **Datums** ir obligāti.)

## <a name="using-the-count-function"></a>Funkcijas Skaits lietošana

Piemēram, statistisko mērījumu nodrošinātāja veidni var iestatīt, kā parādīts tālāk.

| Nosaukums  | Funkcija | Avota tabula  | Summas lauks      | Datuma lauks     |
|-------|----------|---------------|----------------|----------------|
| FTE  | Skaits    | HcmEmployment | Nav attiecināms | Nav attiecināms |

Varat arī pievienot vienu vai vairākus diapazonus, lai sašaurinātu mērījumus no avota tabulas.

Šajā piemērā, ja vēlaties iegūt pilna laika darbinieku (FTE) skaitu, varat pievienot diapazonu laukā **Darbinieka veids**. Laukā **Kritēriji** atlasiet **Darbinieks**, lai ierobežotu izvades diapazonu, kā aprakstīts tālāk.

**Diapazoni**

| Avota tabula  | Lauks       | Kritēriji |
|---------------|-------------|----------|
| HcmEmployment | Nodarbinātā veids | Darbinieks |

Lai iegūtu statistiskos mērījumus analīzē Izmaksu uzskaite, ir jānosaka statistisko mērījumu nodrošinātāja veidnes un statistiskā dimensiju elementa relācija. Šī relācija tiek izveidota katrai izmaksu uzskaites Virsgrāmatai un versijai. Relāciju veido datu savienotājs un datu nodrošinātājs. Katram statistiskajam dimensijas elementam var būt vairāki datu savienotāji un datu nodrošinātāji.

> [!NOTE]
> Šajā piemērā mēs izveidosim relāciju tikai **faktiskajai versijai**.

Lai izveidot relāciju, dodieties uz **Izmaksu uzskaites virsgrāmata** \> **Faktiskā versija** \> **Pārvaldība** \> **Statistiskie mēri**. Šajā scenārijā atlasiet datu savienotāju **Dynamics 365 Finance — statistiskie mēri**, jo vēlaties izgūt datus no programmas Finance.

**Datu avots**

| Vārds        | Datu savienotājs                                                                     | Statisko dimensiju elements |
|-------------|------------------------------------------------------------------------------------|------------------------------|
| FTEs D365FO | Dynamics 365 Finance — statistiskie mēri | FTE                         |

**Datu nodrošinātāja konfigurācija**

| Statistiskās veidnes nosaukums |
|---------------------------|
| FTE                      |

Pēc statistikas mērījumu avota datu apstrādes modulī Izmaksu uzskaite tiek izveidoti tālāk norādītie statistiskie ieraksti.

**Žurnāls**

| Žurnāls | Žurnāla tips                       | Kalendārais finanšu periods | Gads   |  Periods  |  Versija | Datu savienotāja avota ieraksti|
|---------|------------------------------------|------------------------|--------|----------|----------|------------------------------|
| 00001   | Statistikas ierakstu pārsūtīšanas žurnāls | Finanšu                 | 2017   | Periods 1 | CA virsgrāmatas USMF | FTE                   |

**Statistikas ierakstu pārsūtīšanas žurnāla ieraksti**

| Uzskaites datums | Lielums | Statistiskais elements |   Apraksts       | Izmaksu centrs |
|-----------------|-----------|---------------------|---------------------|-------------|
| 31.01.2017.      | 1,00      | FTE                | Pilnas slodzes darbinieki | CC001       |
| 31.01.2017.      | 2,00      | FTE                | Pilnas slodzes darbinieki | CC002       |
| 31.01.2017.      | 2,00      | FTE                | Pilnas slodzes darbinieki | CC003       |

**Statistiskie ieraksti**

| Izmaksu objekts |    | Uzskaites datums | Statisko dimensiju elements |  Apraksts        | Lielums |
|-------------|----|-----------------|------------------------------|---------------------|-----------|
| CC001       | HR | 31.01.2017.      | FTE                         | Pilnas slodzes darbinieki | 1,00      |
| CC002       | FI | 31.01.2017.      | FTE                         | Pilnas slodzes darbinieki | 2,00      |
| CC003       | KrP | 31.01.2017.      | FTE                         | Pilnas slodzes darbinieki | 2,00      |

Ja FTE iepriekš definēta dimensijas elementa sadalījuma pamats ir piešķirts kā sadalījuma pamats izmaksu sadales nosacījumā, izmaksas tiek sadalītas, izmantojot šādu sadalījuma koeficientu.

| Izmaksu objekts | Apraksts    | Lielums | Sadalījuma koeficients |
|-------------|----|-----------|-------------------|
| CC001       | HR | 1,00      | (1/5) × Summa    |
| CC002       | FI | 2,00      | (2/5) × Summa    |
| CC003       | KrP | 2,00      | (2/5) × Summa    |

## <a name="using-the-sum-function"></a>Funkcijas Summa lietošana

Ražošanas izmaksu centrs, CC010 (Iepakošana), ir atbildīgs par preču iepakošanu pirms to nosūtīšanas debitoriem. Tiešās darbaspēka izmaksas tiek pievienotas precēm, izmantojot materiālu komplektu (MK) un maršrutu. Netiešās izmaksas saistībā ar izmaksu centra uzturēšanu arī jāpieskaita saražotajām precēm. Bieži vien vislabākais statistiskais mērījums šādam sadalījumam ir reģistrēto ražošanas stundu skaits katrai precei konkrētā periodā.

Tabulā ProdRouteTrans ir iekļautas visi ražošanas darbaspēka darbības pēc juridiskās personas DataAreadID.

Tālāk ir sniegts tabulas ProdRouteTrans piemērs.

| Atsauce        | Skaits | Operācija | Tips | Laiks  | Fiziskais datums | Preču grupa (finanšu dimensija) | Juridiska persona |
|------------------|--------|-----------|------|-------|---------------|-------------------------------------|--------------|
| Ražošanas pasūtījums | P0001  | Iepakošana | Laiks | 8,00  | 01 – 01 = 2017    | Apelsīnu sula B2B                    | USMF         |
| Ražošanas pasūtījums | P0001  | Iepakošana | Laiks | 8,00  | 02 – 01 = 2017    | Apelsīnu sula B2B                    | USMF         |
| Ražošanas pasūtījums | P0002  | Iepakošana | Laiks | 4,00  | 03.01.2017.    | Apelsīnu sulas patērētājs               | USMF         |
| Ražošanas pasūtījums | P0003  | Iepakošana | Laiks | 4,00  | 03.01.2017.    | Apelsīnu sulas patērētājs               | USMF         |
| Ražošanas pasūtījums | P0004  | Rekonst.  | Laiks | 10,00 | 03.01.2017.    | Apelsīnu sulas patērētājs               | USMF         |

Kad veidojat ierakstu **Statistisko mērījumu nodrošinātāja veidne**, ir jāizlemj, kuru funkciju izmantot:

- **Skaits** — tiek pārsūtīts ierakstu skaits pēc izmaksu objekta.
- **Summa** — tiek pārsūtīta ierakstu summa pēc izmaksu objekta. (Lauks **Summa** un **Datums** ir obligāti.)

Statistisko mērījumu nodrošinātāja veidni var iestatīt, kā parādīts tālāk.

| Nosaukums    | Funkcija | Avota tabula   | Summas lauks | Datuma lauks    |
|---------|----------|----------------|-----------|---------------|
| Pakotnes kopija | Summa      | ProdRouteTrans | Stundas     | Fiziskais datums |

Varat arī pievienot diapazonus, lai sašaurinātu mērījumus no avota tabulas.

Šajā piemērā, ja vēlaties tikai iegūtu to stundu summu, kas ir saistīta ar CC010 iepakošanas izmaksu centru, varat pievienot diapazonu laukā **Operācija**. Laukā **Kritēriji** atlasiet **Iepakošana**, lai ierobežotu izvades diapazonu.

**Diapazoni**

| Avota tabula   | Lauks     | Kritēriji  |
|----------------|-----------|-----------|
| ProdRouteTrans | Operācija | Iepakošana |

Lai iegūtu statistiskos mērījumus analīzē Izmaksu uzskaite, ir jānosaka statistisko mērījumu nodrošinātāja veidnes un statistiskā dimensiju elementa relācija. Šī relācija tiek izveidota katrai izmaksu uzskaites Virsgrāmatai un versijai. Relāciju veido datu savienotājs un datu nodrošinātājs. Katram statistiskajam dimensijas elementam var būt vairāki datu savienotāji un datu nodrošinātāji.

> [!NOTE]
> Šajā piemērā mēs izveidosim relāciju tikai **faktiskajai versijai**.

Lai izveidot relāciju, dodieties uz **Izmaksu uzskaites virsgrāmata** \> **Faktiskā versija** \> **Pārvaldība** \> **Statistiskie mēri**. Šajā scenārijā atlasiet datu savienotāju **Dynamics 365 Finance — statistiskie mēri**, jo vēlaties izgūt datus no programmas Finance.

**Datu avots**

| Vārds           | Datu savienotājs                                                                     | Statisko dimensiju elements |
|----------------|------------------------------------------------------------------------------------|------------------------------|
| Pakotne CC D365FO | Dynamics 365 Finance — statistiskie mēri | Pakotnes kopija                      |

Sistēma atpazīst, ka ProdRouteTrans ir tabula, kur katrs ieraksts pieder atsevišķai juridiskai personai. Tāpēc jums būs jāizvēlas juridiskā persona, no kuras jāimportē darbības.

**Datu nodrošinātāja konfigurācija**

| Statistiskās veidnes nosaukums | Juridiska persona |
|---------------------------|--------------|
| Pakotnes kopija                   | USMF         |

Pēc statistikas mērījumu avota datu apstrādes modulī Izmaksu uzskaite tiek izveidoti tālāk norādītie statistiskie ieraksti.

**Žurnāls**

| Žurnāls | Žurnāla tips                     | Kalendārais finanšu periods | Gads   | Periods | Versija   |   Datu savienotāja avota ieraksti  |
|---------|----------------------------------|------------------------|--------|---------|----------------|---------|
| 00002   | Statistikas ierakstu pārsūtīšanas žurnāls | Finanšu               | 2017    | Periods 1  | CA virsgrāmatas USMF | Pakotnes kopija |

**Statistikas ierakstu pārsūtīšanas žurnāla ieraksti**

| Uzskaites datums | Lielums | Statistiskais elements |  Apraksts          | Preču grupa         |
|-----------------|-----------|---------------------|-----------------------|-----------------------|
| 31.01.2017.      | 16,00     | Pakotnes kopija             | Iepakojuma izmaksu centrs | Apelsīnu sula B2B      |
| 31.01.2017.      | 8,00      | Pakotnes kopija             | Iepakojuma izmaksu centrs | Apelsīnu sulas patērētājs |

**Statistikas ieraksti**

| Izmaksu objekts           | Uzskaites datums | Statisko dimensiju elements |    Apraksts        | Lielums |
|-----------------------|-----------------|------------------------------|-----------------------|-----------|
| Apelsīnu sula B2B      | 31.01.2017.      | Pakotnes kopija                      | Iepakojuma izmaksu centrs | 16,00     |
| Apelsīnu sulas patērētājs | 31.01.2017.      | Pakotnes kopija                      | Iepakojuma izmaksu centrs | 8,00      |

Ja Pakotnes kopija iepriekš definēta dimensijas elementa sadalījuma pamats ir piešķirts kā sadalījuma pamats izmaksu sadales nosacījumā, izmaksas tiek sadalītas, izmantojot šādu sadalījuma koeficientu.

| Izmaksu objekts           | Lielums | Sadalījuma koeficients  |
|-----------------------|-----------|--------------------|
| Apelsīnu sula B2B      | 16,00     | (16 ÷ 24) × Summa |
| Apelsīnu sulas patērētājs | 8,00      | (8 ÷ 24) × Summa  |

## <a name="imported-statistical-measures"></a>Importētie statistiskie mēri

Statistiskos mērījumus var importēt izmaksu uzskaitē, izmantojot Datu pārvaldības importēšanas/eksportēšanas rīku.

Datu elementa, kas tiek izmantots importēšanā, nosaukums ir Importētie statistiskie mēri.

> [!NOTE]
> Šis datu elements ir izveidots, lai katram ierakstam atļautu ne vairāk par piecām unikālām dimensiju vērtībām.

Elektroenerģijas patēriņš tiek reģistrēts programmā Microsoft Excel, izmantojot iepriekš definētu datu elementa formātu. Tālāk ir minēts piemērs.

| Uzskaites datums | 1. Dimensiju elementa nosaukums | 2. dimensiju elementa nosaukums | 5. dimensiju elementa nosaukums | Lielums  | Avota identifikators |
|-----------------|------------------------|------------------------|------------------------|------------|-------------------|
| 31.01.2017.      | CC001                  |                        |                        | 2,450.00   | Elektrība       |
| 31.01.2017.      | CC002                  |                        |                        | 4,100.00   | Elektrība       |
| 31.01.2017.      | CC003                  |                        |                        | 15,000.00  | Elektrība       |

Kad dati ir importēti, izmantojot datu pārvaldības darbību, tie tiek saglabāti tabulā Izmaksu uzskaites sagatavošanas posmi. Tāpēc importētos datus var izmantot vairākās izmaksu uzskaites virsgrāmatās. Nav nepieciešams pārlādēt datus.

Lai importētu datus, dodieties uz **Importētie dati** \> **Datu elements** \> **Importētie statistiskie mēri**.

| Avota identifikators | Uzskaites datums | Lielums  | 1. Dimensiju elementa nosaukums | 2. dimensiju elementa nosaukums | 5. dimensiju elementa nosaukums |
|-------------------|-----------------|------------|------------------------|------------------------|------------------------|
| Elektrība       | 31.01.2017.      | 2,450.00   | CC001                  |                        |                        |
| Elektrība       | 31.01.2017.      | 4,100.00   | CC002                  |                        |                        |
| Elektrība       | 31.01.2017.      | 15,000.00  | CC003                  |                        |                        |

Lai iegūtu statistiskos mērījumus analīzē Izmaksu uzskaite, ir jānosaka avota identifikatora un statistiskā dimensiju elementa relācija. Šī relācija tiek izveidota katrai izmaksu uzskaites Virsgrāmatai un versijai. Relāciju veido datu savienotājs un datu nodrošinātājs. Katram statistiskajam dimensijas elementam var būt vairāki datu savienotāji un datu nodrošinātāji.

> [!NOTE]
> Šajā piemērā mēs izveidosim relāciju tikai **faktiskajai versijai**.

Lai izveidot relāciju, dodieties uz **Izmaksu uzskaites virsgrāmata** \> **Faktiskā versija** \> **Pārvaldība** \> **Statistiskie mēri**. Šajā scenārijā atlasiet datu savienotāju **Importētie statistiskie mēri**, jo dati tika importēti no trešās personas sistēmas izmaksu uzskaites, izmantojot Excel.

**Datu avots**

| Nosaukums        | Datu savienotājs                | Statisko dimensiju elements |
|-------------|-------------------------------|------------------------------|
| Elektrība | Importētie statistiskie mēri | Elektrība                  |

**Datu nodrošinātāja konfigurācija**

| Importa avota identifikators | Funkcija | 1. dimensija   | 2. dimensija | 5. dimensija |
|--------------------------|----------|--------------|------------|------------|
| Elektrība              | Summa      | Izmaksu centri |            |            |

> [!NOTE]
> Definējot datu nodrošinātāju konfigurāciju, ir jānorāda, kuru izmaksu objektu dimensijas jāskaņo ar darbībām, kas importētas. Pēc statistikas mērījumu avota datu apstrādes modulī Izmaksu uzskaite tiek izveidoti tālāk norādītie statistiskie ieraksti.

**Žurnāls**

| Žurnāls | Žurnāla tips                       | Kalendārais finanšu periods | Gads  | Periods  |Versija      |Datu savienotāja avota ieraksti |
|---------|------------------------------------|------------------------|-------|--------|---------------|-------------|
| 00002   | Statistikas ierakstu pārsūtīšanas žurnāls | Finanšu                 | 2017  | Periods 1 | CA virsgrāmatas USMF | Elektrība |

**Statistikas ierakstu pārsūtīšanas žurnāla ieraksti**

| Uzskaites datums | Lielums  | Izmaksu elements |   Apraksts           | Izmaksu centrs |
|-----------------|------------|--------------|-------------------------|-------------|
| 31.01.2017.      | 2,450.00   | Elektrība  | Elektroenerģijas patēriņš | CC001       |
| 31.01.2017.      | 4,100.00   | Elektrība  | Elektroenerģijas patēriņš | CC002       |
| 31.01.2017.      | 15,000.00  | Elektrība  | Elektroenerģijas patēriņš | CC003       |

**Statistikas ieraksti**

| Izmaksu objekts |    | Uzskaites datums | Statisko dimensiju elements |      Apraksts                   | Lielums  |
|-------------|----|-----------------|------------------------------|-------------------------|------------|
| CC001       | HR | 31.01.2017.      | Elektrība                  | Elektroenerģijas patēriņš | 2,450.00   |
| CC002       | FI | 31.01.2017.      | Elektrība                  | Elektroenerģijas patēriņš | 4,100.00   |
| CC003       | KrP | 31.01.2017.      | Elektrība                  | Elektroenerģijas patēriņš | 15,000.00  |

Ja iepriekš definētais dimensijas elementa sadalījuma pamats Elektrība ir piešķirts kā sadalījuma pamats izmaksu sadales nosacījumā, izmaksas tiek sadalītas, izmantojot šādu sadalījuma koeficientu.

| Izmaksu objekts |    | Lielums | Sadalījuma koeficients          |
|-------------|----|-----------|----------------------------|
| CC001       | HR | 2,450.00  | (2450 ÷ 21 550) × Summa  |
| CC002       | FI | 4,100.00  | (4100 ÷ 21 550) × Summa  |
| CC003       | KrP | 15,000.00 | (15 000 ÷ 21 550) × Summa |

## <a name="additional-resources"></a>Papildu resursi

[Sadalījuma pamati](allocation-bases.md)
