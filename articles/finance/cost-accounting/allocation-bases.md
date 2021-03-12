---
title: Sadalījuma pamati
description: Šajā tēmā ir sniegta informācija par sadalījuma pamatiem. Sadalījuma pamati ir galvenie moduļa Izmaksu uzskaite komponenti un galvenokārt tiek izmantoti pieskaitāmo izmaksu sadalei.
author: AndersGirke
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimensionMember, CAMAllocationBaseDetail, CAMFormulaAllocationBaseDetail, CAMAllocationBasePreview, CAMAllocationBase, CAMCostAllocationRule, CAMPredefinedMemberAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.custom: 223174
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f775b09b973a4d34e77d568a5f3b2bd35a7dfdcf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976220"
---
# <a name="allocation-bases"></a>Sadalījuma pamati 

[!include [banner](../includes/banner.md)]

Sadalījuma pamati tiek izmantoti pieskaitāmu izmaksu sadalei modulī Izmaksu uzskaite. Sadalījuma pamats var būt daudzums, piemēram, izmantotās mašīnstundas, patērētās kilovatstundas (kWh) vai aizņemtā platība. Sadalījuma pamati galvenokārt tiek izmantoti pieskaitāmo izmaksu piešķiršanai saražotajam krājumam. Piemēram, IT nodaļa sadala savus izdevumus atbilstoši katrā nodaļā lietoto datoru skaitam.

Modulī Izmaksu uzskaite ir pieejami trīs sadalījuma pamatu tipi.

- Iepriekš definēti dimensijas elementu sadalījuma pamati
- Hierarhijas sadalījuma pamati
- Formulas sadalījuma pamati

## <a name="predefined-dimension-member-allocation-bases"></a>Iepriekš definēti dimensijas elementu sadalījuma pamati

Iepriekš definētie dimensijas elementu sadalījuma pamati tiek automātiski izveidoti, kad tiek izveidots tālāk norādīto tipu dimensijas elements.

- Statiski dimensiju elementi
- Izmaksu elementu dimensiju elementi

> [!NOTE]
> Iepriekš definētie dimensijas elementu sadalījuma pamatos, kas ir izveidoti, pamatojoties uz izmaksu elementa dimensijas elementu, tiek ņemtas vērā tikai vērtības no datu avota nodrošinātāja, piemēram, Virsgrāmatas vai budžeta.

### <a name="example-1-use-a-cost-element-dimension-member-as-the-allocation-base"></a>1. piemērs: izmaksu elementa dimensijas elementa izmantošana kā sadalījuma pamatu
Šajā piemērā ir parādīts, kā izveidot izmaksu sadalījuma kārtulu, lai sadalītu izmaksu elementu Nr. 10002 (Darbinieku apdrošināšana) uz bilanci, kas ir reģistrēta izmaksu elementā Nr. 10001 (Algas). Sadalījuma kārtula tiek definēta, pamatojoties uz katras nodaļas algu attiecības pret algu kopsummu. (Jāpārskata!)

Virsgrāmatā kontu plāns ir definēts tālāk norādītajā veidā.

| Kontu plāns | Galvenais konts | Apraksts        | Galvenā konta tips |
|------------------|--------------|--------------------|-------------------|
| Koplietots           | 10001        | Algas           | Izdevumi           |
| Koplietots           | 10002        | Darbinieku apdrošināšana | Izdevumi           |

Definējiet izmaksu elementa dimensiju un konfigurējiet datu savienotāju. Pēc datu importēšanas modulī Izmaksu uzskaite tiek izveidoti tālāk norādītie ieraksti.

**Izmaksu elementu dimensiju elementi**

| Izmaksu elementa dimensijas nosaukums | Izmaksu elements |  Apraksts       | Tips    |
|-----------------------------|--------------|--------------------|---------|
| Izmaksu elementi               | 10001        | Algas           | Primārs |
| Izmaksu elementi               | 10002        | Darbinieku apdrošināšana | Primārs |

**Iepriekš definēti dimensijas elementu sadalījuma pamati** 

| Nosaukums  | Apraksts        | Izmaksu elementa dimensija |
|-------|--------------------|------------------------|
| 10001 | Algas           | Izmaksu elementi          |
| 10002 | Darbinieku apdrošināšana | Izmaksu elementi          |

Virsgrāmatā ir grāmatoti tālāk norādītie ieraksti.

- Ieraksti, kas atbilst galvenajam kontam Algas, tiek iegūti no algu sistēmas un tiek grāmatoti izmaksu centros.
- Darbinieku apdrošināšanas izdevumi tiek manuāli grāmatoti noklusējuma izmaksu centrā.

| Uzskaites datums | Izmaksu centrs |  Apraksts        | Galvenais konts |  Apraksts       | Summa uzskaites valūtā |
|-----------------|-------------|---------------------|--------------|--------------------|-------------------------------|
| 03.01.2017.      | CC001       | HR                  | 10001        | Algas           | 2000,00                      |
| 03.01.2017.      | CC002       | FI                  | 10001        | Algas           | 5000,00                      |
| 03.01.2017.      | CC003       | KrP                  | 10001        | Algas           | 3000,00                      |
| 03.01.2017.      | CC099       | Noklusējuma izmaksu centrs | 10002        | Darbinieku apdrošināšana | 1000,00                      |

Pēc Virsgrāmatas avota datu apstrādes modulī Izmaksu uzskaite tiek izveidoti tālāk norādītie ieraksti.

**Izmaksu ieraksti**

| Izmaksu objekts |  Apraksts        | Izmaksu elements  |  Apraksts       | Izmaksu izturēšanās   |Summa|Uzskaites datums|
|-------------|---------------------|---------------|--------------------|-----------------|------|---------------|
| CC001       | HR                  | 10001         | Algas           | Neklasificēts    |2000,00|  03.01.2017.    |
| CC002       | FI                  | 10001         | Algas           | Neklasificēts    |5000,00|     03.01.2017.         |
| CC003       | KrP                  | 10001         | Algas           | Neklasificēts    |3000,00|      03.01.2017.        |
| CC099       | Noklusējuma izmaksu centrs | 10002         | Darbinieku apdrošināšana | Neklasificēts    |1000,00|      03.01.2017.       |

Šajā vienkāršotajā piemērā ir parādīts, kā izveidot izmaksu sadalījuma kārtulu, lai sadalītu izmaksu elementu Nr. 10002 (Darbinieku apdrošināšana) uz bilanci, kas ir reģistrēta izmaksu elementā Nr. 10001 (Algas).

**Izmaksu sadales kārtula**

| Izmaksu objektu dimensiju hierarhijas mezgls | Izmaksu elementu dimensiju hierarhijas mezgls | Izmaksu izturēšanās | Sadalījuma pamats |
|--------------------------------------|---------------------------------------|---------------|-----------------|
| CC099                                | 10002                                 | Neklasificēts  | 10001           |

**Pieskaitāmo izmaksu aprēķina veikšana**

Pēc tam, kad izmaksu elements Nr. 10001 (Algas) ir lietots kā sadalījuma pamats, tiek iegūti tālāk norādītie pieskaitāmo izmaksu aprēķina rezultāti.

| Izmaksu objekts | Apraksts | Lielums |   Sadalījuma koeficients         | Summa |
|-------------|-------------|-----------|-----------------------------|--------|
| CC001       | HR          | 2000     | (2000 ÷ 10 000) × 1000,00 | 200,00 |
| CC002       | FI          | 5000     | (5000 ÷ 10 000) × 1000,00 | 500,00 |
| CC003       | KrP          | 3000     | (3000 ÷ 10 000) × 1000,00 | 300,00 |

**Žurnāls**

| Žurnāls | Žurnāla tips                          | Kalendārais finanšu periods | Gads | Periods   | Versija                                                                 |
|---------|---------------------------------------|------------------------|------|----------|-------------------------------------------------------------------------|
| 00001   | Izmaksu sadales aprēķina žurnāls | Finanšu                 | 2017 | Periods 1 | Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods |

**Izmaksu objekta bilances žurnāla ieraksti**

| Uzskaites datums | Izmaksu objekts | Apraksts         | Izmaksu elements | Apraksts        | Izmaksu izturēšanās |  Summa  |
|-----------------|-------------|---------------------|--------------|--------------------|---------------|----------|
| 31.01.2017.      | CC099       | Noklusējuma izmaksu centrs | 10002        | Darbinieku apdrošināšana | Neklasificēts  | 1000,00 |

**Izmaksu ieraksti**

| Izmaksu objekts |  Apraksts        | Izmaksu elements |    Apraksts     | Izmaksu izturēšanās | Summa    | Uzskaites datums |
|-------------|---------------------|--------------|--------------------|---------------|-----------|-----------------|
| CC099       | Noklusējuma izmaksu centrs | 10002        | Darbinieku apdrošināšana | Neklasificēts  | -1000,00 | 31.01.2017.      |
| CC001       | HR                  | 10002        | Darbinieku apdrošināšana | Neklasificēts  | 200,00    | 31.01.2017.      |
| CC002       | FI                  | 10002        | Darbinieku apdrošināšana | Neklasificēts  | 500,00    | 31.01.2017.      |
| CC099       | KrP                  | 10002        | Darbinieku apdrošināšana | Neklasificēts  | 300,00    | 31.01.2017.      |

### <a name="example-2-use-a-statistical-dimension-member-as-the-allocation-base"></a>2. piemērs: statistikas dimensijas elementa izmantošana kā sadalījuma pamatu

Statistikas dimensiju elementus var izmantot kā sadalījuma pamatus, lai definētu politikas vai ziņotu par beznaudas patēriņu pēc izmaksu objektiem. Varat manuāli izveidot statistikas dimensiju elementus vai tos importēt no faila, izmantojot datu pārvaldības importēšanas/eksportēšanas rīku.

**Statistikas dimensiju elementi**

| Statistikas dimensijas nosaukums | Statistikas elements | Apraksts               | Vienība |
|----------------------------|---------------------|---------------------------|------|
| Statistikas elementi       | FTE                 | Pilnas slodzes darbinieki       | gab.   |
| Statistikas elementi       | Elektrība         | Elektroenerģijas patēriņš   | kWh  |

Statistikas elementu dimensija

**Iepriekš definēti dimensijas elementu sadalījuma pamati**

| Nosaukums        | Apraksts             | Statistikas elementa dimensija |
|-------------|-------------------------|-------------------------------|
| FTE         | Pilnas slodzes darbinieki     | Statistikas elementi          |
| Elektrība | Elektroenerģijas patēriņš | Statistikas elementi          |

Statistikas mēri var tikt iegūti no dažādiem avotiem.

- Elektroenerģijas patēriņu var mērīt, izmantojot mērierīces, kas ir izstādītas dažādās vietās uzņēmuma teritorijā.
- Statistikas mēri tiek glabāti tabulās. Piemēram, tabulā HcmEmployment ir ietverts visu darbinieku un attiecīgo izmaksu centru saraksts.

| Vārds, uzvārds       | Izmaksu centrs |  Apraksts  | Nodarbinātā veids |
|------------|-------------|----|-------------|
| A darbinieks | CC001       | HR | Darbinieks    |
| B darbinieks | CC002       | FI | Darbinieks    |
| C darbinieks | CC002       | FI | Darbinieks    |
| D darbinieks | CC003       | KrP | Darbinieks    |
| F darbinieks | CC003       | KrP | Darbinieks    |

> [!NOTE]
> Visas tabulas, kurās ir ietvertas finanšu dimensijas, var izmantot kā statistikas mēru avotus.

Modulis Izmaksu uzskaite atbalsta statistikas mēru apkopošanu, izmantojot tālāk norādītos datu savienojumus.

- Datu pārvaldības importēšanas/eksportēšanas rīks
- Statistiskie mēri

Lai izgūtu statistikas mērus no sistēmas, ir nepieciešama statistikas mēru nodrošinātāja veidne. Papildinformāciju skatiet tēmā “Statistikas mēru nodrošinātāja veidne.” (Kad šī tēma būs uzrakstīta, tiks pievienota saite.)

**Statistikas mēru nodrošinātāju veidnes**

| Nosaukums  | Funkcija | Avota tabula  | Summas lauks      | Datuma lauks     |
|-------|----------|---------------|----------------|----------------|
| FTE | Skaits    | HcmEmployment | Nav attiecināms | Nav attiecināms |

Pēc statistikas mēra avota datu apstrādes modulī Izmaksu uzskaite tiek izveidoti tālāk norādītie ieraksti.

**Statistikas ieraksti**

| Izmaksu objekts | Apraksts      | Uzskaites datums | Statisko dimensiju elements | Apraksts         | Lielums |
|-------------|------------------|-----------------|------------------------------|---------------------|-----------|
| CC001       | HR               | 31.01.2017.      | FTE                        | Pilnas slodzes darbinieki | 1,00      |
| CC002       | FI               | 31.01.2017.      | FTE                        | Pilnas slodzes darbinieki | 2,00      |
| CC003       | KrP               | 31.01.2017.      | FTE                        | Pilnas slodzes darbinieki | 2,00      |

Tālāk esošajā piemērā ir parādīta izmaksu sadales kārtula, kurā kā sadalījuma pamats ir piešķirts iepriekš definētais dimensijas elementa sadalījuma pamats FTE.

| Izmaksu objekts | Apraksts  | Lielums | Sadalījuma koeficients |
|-------------|------|-----------|-------------------|
| CC001       | HR   | 1,00      | (1/5) × Summa    |
| CC002       | FI   | 2,00      | (2/5) × Summa    |
| CC003       | KrP   | 2,00      | (2/5) × Summa    |

Varat izmantot importēto statistikas ēru datu ierakstu, lai importētu statistikas mērus modulī Izmaksu uzskaite. Varat arī izmantot datu pārvaldības importēšanas/eksportēšanas rīku. Programmā Excel elektroenerģijas patēriņš tiek reģistrēts tālāk norādītajā veidā.

| Uzskaites datums | Dimensijas elements | Lielums | Avota identifikators |
|-----------------|------------------|-----------|-------------------|
| 31.01.2017.      | CC001            | 2,450.00  | Elektrība       |
| 31.01.2017.      | CC002            | 4,100.00  | Elektrība       |
| 31.01.2017.      | CC003            | 15,000.00 | Elektrība       |

Pēc statistikas mēra avota datu apstrādes modulī Izmaksu uzskaite tiek izveidoti tālāk norādītie ieraksti.

**Statistikas ieraksti**

| Izmaksu objekts |    | Uzskaites datums | Statisko dimensiju elements |    Apraksts          | Lielums |
|-------------|----|-----------------|------------------------------|-------------------------|-----------|
| CC001       | HR | 31.01.2017.      | Elektrība                  | Elektroenerģijas patēriņš | 2,450.00  |
| CC002       | FI | 31.01.2017.      | Elektrība                  | Elektroenerģijas patēriņš | 4,100.00  |
| CC003       | KrP | 31.01.2017.      | Elektrība                  | Elektroenerģijas patēriņš | 15,000.00 |

Tālāk esošajā piemērā ir parādīta izmaksu sadales kārtula, kurā kā sadalījuma pamats ir piešķirts iepriekš definētais dimensijas elementa sadalījuma pamats Elektrība.

| Izmaksu objekts | Apraksts  | Lielums | Sadalījuma koeficients          |
|-------------|------|-----------|----------------------------|
| CC001       | HR   | 2,450.00  | (2450 ÷ 21 550) × Summa  |
| CC002       | FI   | 4,100.00  | (4100 ÷ 21 550) × Summa  |
| CC003       | KrP   | 15,000.00 | (15 000 ÷ 21 550) × Summa |

## <a name="hierarchy-allocation-bases"></a>Hierarhijas sadalījuma pamati

Izmaksu grāmatveži var manuāli izveidot hierarhijas sadalījuma pamatus, lietojot izmaksu objektu dimensiju hierarhijas mezglu esošam sadalījuma pamatam. Šādā veidā varat ierobežot sākotnējā iepriekš definētā dimensijas elementa sadalījuma pamata diapazonu. Vienu iepriekš definēto dimensijas elementa sadalījuma pamatu var izmantot, lai izveidotu vairākus hierarhijas sadalījuma pamatus. Izmaksu objektu dimensiju hierarhijā, kas ir saistīta ar hierarhijas sadalījuma pamatiem, var saglabāt diapazonus.

### <a name="example-hierarchy-allocation-bases-that-are-based-on-full-time-employees-in-the-organization"></a>Piemērs: hierarhijas sadalījuma pamati, kas ir izveidoti, pamatojoties uz organizācijas pilnas slodzes darbinieku skaitu
Tālāk esošajā piemērā ir parādīta izmaksu objektu dimensiju hierarhija, ko var izveidot, lai raksturotu vienkāršotu organizāciju.

| Hierarhijas nosaukums | 0 mezgla līmenis | 1. mezgla līmenis | 2. mezgla līmenis | Dimensijas elementi |
|----------------|--------------|--------------|--------------|-------------------|
| Organizācija   | Izpilddirektore          | CFO          | FICO         | CC001             |
| Organizācija   | Izpilddirektore          | CFO          | HR           | CC002             |
| Organizācija   | Izpilddirektore          | CIO          | KrP           | CC003             |

Iepriekšēja sadaļā izveidotajā iepriekš definētajā dimensijas elementa sadalījuma pamatā FTE ir ietverti tālāk norādītie ieraksti.

**Statistikas ieraksti**

| Izmaksu objekts | Apraksts  | Uzskaites datums | Statisko dimensiju elements | Apraksts | Lielums |
|-------------|------|-----------------|------------------------------|---------------------|-----------|
| CC001       | HR   | 31.01.2017.      | FTE                        | Pilnas slodzes darbinieki | 1,00      |
| CC002       | FI   | 31.01.2017.      | FTE                        | Pilnas slodzes darbinieki | 2,00      |
| CC003       | KrP   | 31.01.2017.      | FTE                        | Pilnas slodzes darbinieki | 2,00      |

Izmaksas ir jāsadala starp izmaksu centriem, kas ir pakļauti organizācijas finanšu direktoram (CFO). Ir atzīts, ka pareizā sadalījuma attiecība atbilst pilnas slodzes darbinieku (FTE) skaitam katrā izmaksu centrā.

**Hierarhijas sadalījuma pamati**

| Nosaukums                  | Sadalījuma pamats | Izmaksu objektu dimensiju hierarhija | Izmaksu objektu dimensiju hierarhijas mezgls |
|-----------------------|-----------------|---------------------------------|--------------------------------------|
| FTE skaits katram CFO | FTE           | Organizācija                    | CFO                                  |

Priekšskatījuma funkcija sniedz iespēju pārbaudīt hierarhijas sadalījuma pamatus, kas ir izveidoti, pamatojoties uz statistikas ierakstiem sistēmā.

**Detalizēta informācija par sadalījuma pamatu**

| Izmaksu objekts | Apraksts  |  Lielums |
|-------------|------|------------|
| CC001       | HR   | 1,00       |
| CC002       | FI   | 2,00       |

Tālāk esošajā piemērā ir parādīta izmaksu sadales kārtula, kurā kā sadalījuma pamats ir piešķirts sadalījuma pamats FTE skaits katram CFO.

| Izmaksu objekts | Apraksts  | Lielums | Sadalījuma koeficients |
|-------------|------|-----------|-------------------|
| CC001       | HR   | 1,00      | (1/3) × Summa    |
| CC002       | FI   | 2,00      | (2/3) × Summa    |

## <a name="formula-allocation-bases"></a>Formulas sadalījuma pamati

Formulas sadalījuma pamati sniedz iespēju definēt uzlabotas formulas, lai iegūtu vajadzīgos sadalījuma pamatus. Formulas sadalījuma pamatus varat izveidot manuāli.

Izveidojot formulas sadalījuma pamatu, ir jāatlasa statistikas dimensija un izmaksu elementa dimensija, kas tiks izmantota formulas izveidei. Formulas sadalījuma pamata ietvaros var izmantot visus sadalījuma pamatus, kas ir saistīti ar iepriekš atlasītajām dimensijām.

> [!NOTE]
> Iepriekš definētos formulas sadalījuma pamatus var izmantot, lai definētu jaunu formulas sadalījuma pamatu.

Izveidojot formulas sadalījuma pamata koeficientus ir jāizveido aizstājvārds, kas ir jāsaista ar sadalījuma pamatu vai konstanti. Pēc tam aizstājvārdi tiek izmantoti, lai definētu formulu.

Lai definētu formulu, varat izmantot tālāk norādītos operatorus.

| Simboli | Teksts           |
|---------|----------------|
| ( )     | Iekavas    |
| \<      | Mazāks nekā   |
| \>      | Lielāks nekā    |
| +       | Saskaitīšana       |
| –       | Atņemšana    |
| \*      | Reizināšana |

Parastie **IF** priekšraksti netiek atbalstīti. Taču varat izveidot priekšrakstus un pārbaudīt, vai tie ir patiesi.

| Pārskats | Validācija | Rezultāts |
|-----------|------------|--------|
| a \> b    | Patiess       | 1.      |
| a \> b    | Aplams      | 0      |

### <a name="example-1-a-simple-formula"></a>1. piemērs: vienkārša formula

Elektroenerģijas rēķinā bieži ir ietvertas divas tālāk norādītās daļas.

- Fiksēta maksa par tīkla ekspluatāciju
- Izmaksas par patērēto elektroenerģiju (kWh)

Iepriekš definētais dimensijas elementa sadalījuma pamats Elektrība jau ir definēts, un tajā ir ietvertas šīs vērtības.

**Statistikas ieraksti**

| Izmaksu objekts | Nosaukums | Uzskaites datums | Statisko dimensiju elements | Apraksts             | Lielums |
|-------------|------|-----------------|------------------------------|-------------------------|-----------|
| CC001       | HR   | 31.01.2017.      | Elektrība                  | Elektroenerģijas patēriņš | 2,450.00  |
| CC002       | FI   | 31.01.2017.      | Elektrība                  | Elektroenerģijas patēriņš | 4,100.00  |
| CC003       | KrP   | 31.01.2017.      | Elektrība                  | Elektroenerģijas patēriņš | 15,000.00 |

Ja fiksētā maksa tagad ir vienmērīgi jāsadala starp izmaksu objektiem, kas rada elektroenerģijas patēriņu, izmaksas var sadalīt divos tālāk norādītajos veidos.

- Izveidojiet jaunu iepriekš definētu sadalījuma pamatu Fiksētā maksa par elektroenerģiju un pēc tam lietojiet statistikas mēru 1,00 katram izmaksu objektam, kas ir radījis elektrības patēriņu.
- Izveidojiet formulas sadalījuma pamatu Fiksēta maksa par elektroenerģiju, kas izmanto iepriekš definēto sadalījuma pamatu Elektrība, kurš jau ir definēts sistēmā. Šī veida priekšrocība ir tas, ka modulī Izmaksu uzskaite ir jāielādē dati tikai par vienu statistikas dimensijas elementu Elektrība.

**Formulas sadalījuma pamats** 

| Nosaukums              | Izmaksu elementa dimensija | Statiskā dimensija | Formula |
|-------------------|------------------------|-----------------------|---------|
| Fiksētā maksa par elektroenerģiju |                        | Statistikas elementi  |         |

Pirms lauka **Formula** aizpildīšanas ir jānorāda aizstājvārds, kas ir jāizmanto formulā.

**Formulas sadalījuma pamata koeficienti**

| Aizstājvārds | Konstants | Sadalījuma pamats |
|-------|----------|-----------------|
| a     |          | Elektrība     |
| b     | 0,01     |                 |

Ņemiet vērā, ka 0 (nulle) netiek atbalstīta kā konstante.

**Formulas sadalījuma pamats**

| Nosaukums              | Izmaksu elementa dimensija | Statiskā dimensija | Formula |
|-------------------|------------------------|-----------------------|---------|
| Fiksētā maksa par elektroenerģiju |                        | Statistikas elementi  | a \> b  |

Priekšskatījuma funkcija sniedz iespēju pārbaudīt formulas sadalījuma pamatu, kas ir izveidots, pamatojoties uz statistikas ierakstiem sistēmā.

**Detalizēta informācija par sadalījuma pamatu**

| Izmaksu objekts | Apraksts  | Formula           | Lielums |
|-------------|------|-------------------|-----------|
| CC001       | HR   | 2.450,00 \> 0,01  | 1,00      |
| CC002       | FI   | 4.100,00 \> 0,01  | 1,00      |
| CC003       | KrP   | 15.000,00 \> 0,01 | 1,00      |

Tālāk esošajā piemērā ir parādīta izmaksu sadales kārtula, kurā kā sadalījuma pamats ir piešķirts formulas sadalījuma pamats Elektrība.

**Izmaksu objekta lieluma sadalījuma koeficients**

| Izmaksu objekts | Nosaukums | Lielums |  Sadalījuma koeficients |
|-------------|------|-----------|--------------------|
| CC001       | HR   | 1,00      | (1/3) × Summa     |
| CC002       | FI   | 1,00      | (1/3) × Summa     |
| CC003       | KrP   | 1,00      | (1/3) × Summa     |

### <a name="example-2-an-advanced-formula"></a>2. piemērs: uzlabota formula
Šajā piemērā elektroenerģijas izmaksas nedrīkst vienkārši tikt noteiktas, pamatojoties uz faktisko elektroenerģijas patēriņu (kWh). Vadība vēlas ietvert pamudinājumu samazināt elektroenerģijas patēriņu. 

| Noteikums              | Norma | 
|-------------------|------|
| a <= 10000,00 kWh | 0.75 |
| a > 10000,00 kWh  | 1.15 |

Tiek izveidots jauns formulas sadalījuma pamats Elektroenerģijas patēriņš.

**Formulas sadalījuma pamats**

| Nosaukums              | Izmaksu elementa dimensija | Statiskā dimensija | Formula |
|-------------------|------------------------|-----------------------|---------|
| Elektroenerģijas patēriņš |                        | Statistikas elementi  |         |

Pirms lauka **Formula** aizpildīšanas ir jānorāda aizstājvārds, kas ir jāizmanto formulā.

**Formulas sadalījuma pamata koeficienti**

| Aizstājvārds | Konstants  | Sadalījuma pamats |
|-------|-----------|-----------------|
| a     |           | Elektrība     |
| b     | 10 000,00 |                 |
| c     | 0.75      |                 |
| d     | 1.15      |                 |

**Formulas sadalījuma pamats**

| Nosaukums              | Izmaksu elementa dimensija | Statiskā dimensija | Formula                                                    |
|-------------------|------------------------|-----------------------|------------------------------------------------------------|
| Fiksētā maksa par elektroenerģiju |                        | Statistikas elementi  | ((a \> b) × ((b × c) + (a – b) × d)) + ((a \<= b] × a × c) |

Priekšskatījuma funkcija sniedz iespēju pārbaudīt formulas sadalījuma pamatu, kas ir izveidots, pamatojoties uz statistikas ierakstiem sistēmā.

**Detalizēta informācija par sadalījuma pamatu**

| Izmaksu objekts |    | Formula                                                                                                                             | Lielums |
|-------------|----|-------------------------------------------------------------------------------------------------------------------------------------|-----------|
| CC001       | HR | ((2450,00 \> 10 000,00) × ((10 000,00 × 0,75) + (2450,00 – 10 000,00) × 1,15)) + ((2450,00 \<= 10 000,00) × 2450,00 × 0,75)     | 1,837.50  |
| CC002       | FI | ((4100,00 \> 10 000,00) × ((10 000,00 × 0,75) + (4100,00 – 10 000,00) × 1,15)) + ((4100,00 \<= 10,000,00) × 4100,00 × 0,75)     | 3,075.00  |
| CC003       | KrP | ((15 000,00 \> 10 000,00) × ((10 000,00 × 0,75) + (15 000,00 – 10 000,00) × 1,15)) + ((15 000,00 \<= 10,000,00) × 15 000,00 × 0,75) | 1,3250.00 |

Tālāk ir sniegta detalizēta informācija par objekta CC003 (IT) formulu.

((15 000,00 \> 10 000,00) × ((10 000,00 × 0,75) + (15 000,00 – 10 000,00) × 1,15)) + ((15 000,00 \<= 10 000,00) × 15 000,00 × 0,75) = 13 250,00

(1 × (7500,00 + 5000,00 × 1,15)) + (0 × 15 000,00 × 0,75)            

1 × 7500,00 + 5750,00 + 0 

Tālāk esošajā piemērā ir parādīta izmaksu sadales kārtula, kurā kā sadalījuma pamats ir piešķirts formulas sadalījuma pamats Fiksētā maksa par elektroenerģiju.


| Izmaksu objekts | Apraksts | Lielums |        Sadalījuma koeficients         |
|-------------|-------------|-----------|----------------------------------|
|    CC001    |     HR      | 1,837.50  | (1837,50 ÷ 18 162,50) × Summa  |
|    CC002    |     FI      | 3,075.00  | (3075,00 ÷ 18 162,50) × Summa  |
|    CC003    |     KrP      | 13,250.00 | (13 250,00 ÷ 18 162,50) × Summa |

