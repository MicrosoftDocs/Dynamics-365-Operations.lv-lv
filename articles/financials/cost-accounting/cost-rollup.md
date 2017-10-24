---
title: "Izmaksu apkopojuma politika un pieskaitāmo izmaksu aprēķināšana"
description: "Šajā tēmā ir sniegta informācija par to, kā noteikt pareizo sekundāro izmaksu elementu līmeni un izveidot izmaksu apkopojuma kārtulas, kas atbilst organizācijas pārskatu un izmaksu izsekojamības prasībām."
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostRollupRule, CAMDimensionHierarchy
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: YuyuScheller
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 088883f35fe73c933c1d8558297bee0e3ccc3cb2
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="cost-rollup-policy-and-overhead-calculation"></a>Izmaksu apkopojuma politika un pieskaitāmo izmaksu aprēķināšana 

[!include[banner](../includes/banner.md)]

Izmaksu uzskaite sniedz iespēju gūt ieskatu par to, kā izmaksu plūsma ir saistīta ar organizācijas nodrošinātajām precēm un pakalpojumiem. Lai nodrošinātu izmaksu pārskatāmību, ir svarīgi sadalīt izmaksas pa izmaksu objektiem, pamatojoties uz atbilstošu sadalījuma pamatu. Pēc noklusējuma tiek nodrošināts primāro izmaksu elementa sadalījums, kas ir vajadzīgs dažos gadījumos, taču rada maz vērā ņemamu seku.

-   Pēc pieskaitāmo izmaksu aprēķināšanas primārā izmaksu elementa papildu izmaksu objektu bilance būs vienāda ar nulli.

-   Pieskaitāmo izmaksu aprēķināšanas laikā var tikt ģenerēts ļoti daudz izmaksu ierakstu.

-   Izmaksu plūsmu starp izmaksu objektiem nevar izsekot.

Lai nepieļautu šādus sarežģījumus, modulis Izmaksu uzskaite sniedz iespēju konfigurēt izmaksu sadalījumu atbilstoši jūsu organizācijas vadības pārskatu prasībām. Šajā tēmā ir aprakstīts, kā noteikt pareizo sekundāro izmaksu elementu līmeni un izveidot izmaksu apkopojuma kārtulas, kas ir piemērotas organizācijas pārskatu un izmaksu izsekojamības metodēm.

> [!NOTE]
> Pārskatu prasību izmaiņu gadījumā varat mainīt konfigurācijas.

## <a name="example-of-cost-rollup-policy-setup"></a>Izmaksu apkopojuma politikas iestatījumu piemērs

Pieņemsim, ka organizācijai ir tālāk norādītā struktūra, kurā ir ietverti 4 izmaksu centri.

![Organizācijas struktūras piemērs](./media/dimension-hierarchy-org.png)

**Izmaksu objekta dimensija**

| Izmaksu centri | Apraksts          |
|--------------|-----------|
| CC001        | HR        |
| CC002        | Finansēt   |
| CC003        | Montāža  |
| CC004        | Iepakošana |

**Izmaksu elementa dimensija**

| Izmaksu elementi | Apraksts | Tips    |
|---------------|-------------|---------|
| 1001          | Elektrība | Primārs |
| 1002          | Algas    | Primārs |
| 1003          | Reklāma | Primārs |

Organizācijas pārskatu prasībām atbilstošu dimensiju hierarhiju var iestatīt tālāk norādītajā veidā.

**Detalizēta informācija par dimensiju hierarhiju**

| Dimensiju hierarhijas nosaukums | Dimensija    | Dimensiju hierarhijas veida nosaukums      | Piekļuves sarakstu hierarhija |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organizācija             | Izmaksu centri | Dimensiju klasifikācijas hierarhija | Nav                    |

**Dimensiju hierarhija**

|              | Dimensijas elementu diapazons |                     |
|--------------|-------------------------|---------------------|
| **Mezgli**        | **Avota dimensijas elements**   | **Mērķa dimensijas elements** |
| Organizācija |                         |                     |
| &nbsp;&nbsp;Administrators             |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Finansēt              | CC001                   | CC001               |
| &nbsp;&nbsp;&nbsp;&nbsp;HR               | CC002                   | CC002               |
| &nbsp;&nbsp;Ražošana               |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Iepakošana              | CC003                   | CC003               |
| &nbsp;&nbsp;&nbsp;&nbsp;Montāža             | CC004                   | CC004               |

Politikas prasībām atbilstošu dimensiju hierarhiju var iestatīt tālāk norādītajā veidā.

**Detalizēta informācija par dimensiju hierarhiju**

| Dimensiju hierarhijas nosaukums | Dimensija     | Dimensiju hierarhijas veida nosaukums      |
|--------------------------|---------------|------------------------------------|
| Peļņas un zaudējumu aprēķins  | Izmaksu elementi | Dimensiju klasifikācijas hierarhija |

**Dimensiju hierarhija**

|                         | Dimensijas elementu diapazons |                     |
|-------------------------|-------------------------|---------------------|
| Zari                   | Avota dimensijas elements   | Mērķa dimensijas elements |
| Peļņas un zaudējumu aprēķins |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Primārās izmaksas                    | 10001                   | 10003               |

Tālāk ir redzams, kā pēc virsgrāmatas ierakstu apstrādes izskatās izmaksu ierakstu bilance pēc izmaksu objekta.

|                      | **Izmaksu objekts** |           |           |           | **Kopsumma**     |
|----------------------|-----------------|-----------|-----------|-----------|---------------|
| **Izmaksu elements**     | **CC001**       | **CC002** | **CC003** | **CC004** |               |
| **1001 Elektrība** | 100,00          | 200,00    | 6.000,00  | 2.000,00  | **8.300,00**  |
| **1002 Algas**    | 10.000,00       | 10.000,00 | 8.000,00  | 6.500,00  | **34.500,00** |
| **1003 Reklāma** | 0,00            | 4.000,00  | 0,00      | 0,00      | **4.000,00**  |
|                      | 10.100,00       | 14.200,00 | 14.000,00 | 8.500,00  | **46.800,00** |

**Statiskā dimensija**

| Statistikas elementi |    Apraksts   |
|----------------------|------------------|
| SE-1                 | HR pakalpojumi      |
| SE-2                 | Finanšu pakalpojumi |

Izmaksu objekts CC001 HR nodrošina HR pakalpojumus vairākiem izmaksu objektiem.

HR pakalpojumi tiek patērēti atbilstoši tālāk norādītajam lielumu sadalījumam.

| Izmaksu objekts | Apraksts |   HR pakalpojumi |
|-------------|-------------|----|
| CC002       | Finansēt     | 35 |
| CC003       | Montāža    | 55 |
| CC004       | Iepakošana   | 10. |

Izmaksu objekts CC002 Finanses nodrošina finanšu pakalpojumus vairākiem izmaksu objektiem.

Finanšu pakalpojumi tiek patērēti atbilstoši tālāk norādītajam lielumu sadalījumam.

| Izmaksu objekts |   Apraksts    |  Finanšu pakalpojumi   |
|-------------|------------------|----|
| CC003       | Montāža         | 65 |
| CC004       | Iepakošana        | 35 |

Izmaksu sadalījuma politikas var iestatīt tālāk norādītajā veidā.

| Ierobežojuma nosaukums | Apraksts     | Izmaksu objektu dimensiju hierarhija | Statiskā dimensija | Izmaksu elementa dimensija |
|-------------|-----------------|---------------------------------|-----------------------|------------------------|
| 2017        | Izmaksu sadalījums | Organizācija                    | Statistikas elementi  | Izmaksu elementi          |

Izmaksu sadalījuma kārtulas var iestatīt tālāk norādītajā veidā.

| Izmaksu objektu dimensiju hierarhijas mezgls | Izmaksu izturēšanās | Sadalījuma pamats        |
|--------------------------------------|---------------|------------------------|
| CC001                                | Summa         | **HR pakalpojumi**        |
| CC002                                | Summa         | **Finanšu pakalpojumi** |

<a name="brhow-cost-flows-between-cost-centers"></a><br>Izmaksu plūsma starp izmaksu centriem 
---------------------------------------------------

Ja vēlaties uzzināt par izmaksu plūsmu starp izmaksu centriem organizācijas ietvaros, varat katram izmaksu centram izveidot tipa **Sekundārs** izmaksu elementus. Pēc tam šie izmaksu elementi tiks izmantoti bilanču pārsūtīšanai starp izmaksu centriem pieskaitāmo izmaksu aprēķināšanas laikā.

Izmaksu elementu dimensiju elementus var iestatīt tālāk norādītajā veidā.

| Izmaksu elementi | Tips          |               |
|---------------|---------------|---------------|
| 1001          | Elektrība   | Primārs       |
| 1002          | Algas      | Primārs       |
| 1003          | Reklāma   | Primārs       |
| **SC-CC001**  | **HR**        | **Sekundārs** |
| **SC-CC002**  | **Finanses**   | **Sekundārs** |
| **SC-CC003**  | **Montāžā**  | **Sekundārs** |
| **SC-CC004**  | **Iepakošana** | **Sekundārs** |

Dimensiju hierarhija **Peļņas un zaudējumu aprēķins** ir jāatjaunina, to papildinot ar jaunajiem dimensijas elementiem, lai dimensiju hierarhijā būtu ietverti pareizie dati, ko var izmantot pārskatu un politiku definēšanai.

**Detalizēta informācija par dimensiju hierarhiju**

| Dimensiju hierarhijas nosaukums | Dimensija     | Dimensiju hierarhijas veida nosaukums      |
|--------------------------|---------------|------------------------------------|
| Peļņas un zaudējumu aprēķins  | Izmaksu elementi | Dimensiju klasifikācijas hierarhija |

**Dimensiju hierarhija**

|                         | Dimensijas elementu diapazons |                     |
|-------------------------|-------------------------|---------------------|
| Zari                   | Avota dimensijas elements   | Mērķa dimensijas elements |
| Peļņas un zaudējumu aprēķins |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Primārās izmaksas                        | 10001                   | 10003               |
| &nbsp;&nbsp;&nbsp;&nbsp;Sekundārās izmaksas                         | **SC-CC001**            | **SC-CC004**        |

Izveidojiet **izmaksu apkopojuma politiku**, kurā katrs izmaksu centrs ir kartēts ar atbilstošu tipa **Sekundārs** izmaksu elementu.

**Izmaksu apkopojuma politikas**

| Ierobežojuma nosaukums | Apraksts | Izmaksu objektu dimensiju hierarhija | Izmaksu elementu dimensiju hierarhija |
|-------------|-------------|---------------------------------|----------------------------------|
| 2017        | Izmaksu plūsma   | Organizācija                    | Peļņas un zaudējumu aprēķins          |

**Izmaksu apkopojuma kārtulas**

| Izmaksu objektu dimensiju hierarhijas mezgls | Izmaksu elementu dimensiju hierarhijas mezgls | Sekundāro izmaksu elements |
|--------------------------------------|---------------------------------------|------------------------|
| CC001                                | Peļņas un zaudējumu aprēķins               | **SC-CC001**           |
| CC002                                | Peļņas un zaudējumu aprēķins               | **SC-CC002**           |
| CC003                                | Peļņas un zaudējumu aprēķins               | **SC-CC003**           |
| CC004                                | Peļņas un zaudējumu aprēķins               | **SC-CC004**           |

## <a name="perform-overhead-calculation"></a>Pieskaitāmo izmaksu aprēķina veikšana

**Žurnāls**

| Žurnāls | Žurnāla tips            | Kalendārais finanšu periods | Gads | Periods | Versija       |
|---------|-------------------------|------------------------|------|--------|---------------|
| 00002   | Izmaksu sadalījuma žurnāls | Finanšu                 | 2017    | Periods 1 | Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods |

Tagad, veidojot **izmaksu objekta bilances žurnāla ierakstus**, sistēmā tiks lietota **izmaksu apkopojuma politika**.

**Izmaksu objekta bilances žurnāla ieraksti**

| Uzskaites datums | Izmaksu objekts | Apraksts  | Izmaksu elements | Apraksts |  Summa |
|-----------------|-------------|--------------|----------|-----------|-----------|
| 31.01.2017.      | CC001       | HR           | SC-CC001 | HR        | 10.100,00 |
| 31.01.2017.      | CC002       | Finansēt      | SC-CC002 | Finansēt   | 17.735,00 |
| 31.01.2017.      | CC003       | Montāža     | SC-CC003 | Montāža  | 31.082,75 |
| 31.01.2017.      | CC004       | Iepakošana    | SC-CC004 | Iepakošana | 15.717,25 |

> [!NOTE]
> Ja pastāv **izmaksu apkopojuma politika**, žurnāla ieraksti tiek izveidoti, pamatojoties uz politikā ietvertajām kārtulām. Parādītā bilance ir pieskaitāmo izmaksu aprēķina bilance.

Lapā **Detalizēta izmaksu objekta izmaksu bilances žurnāla ieraksta informācija**, kam var piekļūt no žurnāla ierakstiem, tiek rādīta informācija par to, kā tiek iegūta bilance.

**Piemērs: izmaksu objekta CC002 Finanses žurnāla ieraksts**

**Detalizēta izmaksu objekta izmaksu bilances žurnāla ieraksta informācija**

| Izmaksu elementu dimensiju elements | Apraksts |  Summa   |
|-------------------------------|-------------|-----------|
| 1001                          | Elektrība | 200,00    |
| 1002                          | Algas    | 10.000,00 |
| 1003                          | Reklāma | 4.000,00  |
| SC-CC001                      | HR          | 3.535,00  |

**Izmantojot pieskaitāmo izmaksu aprēķinu ģenerētie izmaksu ieraksti**

| Izmaksu objekts | Apraksts  | Izmaksu elements   | Apraksts  |        Summa     |       Uzskaites datums     |
|-------------|--------------|----------|-----------------|-------------|------------|
| CC001       | HR           | SC-CC001 | HR              | \-10 100,00 | 31.01.2017. |
| CC002       | Finansēt      | SC-CC001 | HR              | 3.535,00    | 31.01.2017. |
| CC003       | Montāža     | SC-CC001 | HR              | 5.555,00    | 31.01.2017. |
| CC004       | Iepakošana    | SC-CC001 | HR              | 1.010,00    | 31.01.2017. |
| CC002       | Finansēt      | SC-CC002 | Finansēt         | \-17 735,00 | 31.01.2017. |
| CC003       | Montāža     | SC-CC002 | Finansēt         | 11.527,75   | 31.01.2017. |
| CC004       | Iepakošana    | SC-CC002 | Finansēt         | 6.207,25    | 31.01.2017. |

Pēc **pieskaitāmo izmaksu aprēķina** pabeigšanas varat izveidot rezultātu pārskatus, izmantojot tādus rīkus kā Microsoft SharePoint Workspace, Excel vai Power BI.

## <a name="view-reporting-in-excel"></a>Pārskatu skatīšana programmā Excel 

Dimensiju hierarhijas sniedz iespēju skatīt datus dažādos apkopojuma līmeņos.

Tālāk esošajā piemērā ir parādīta Power Pivot pārskata skatīšana programmā Excel.

| **Peļņas un zaudējumu aprēķins** | **Izmaksu objekts** |                |               |               |  **Kopsumma**    |
|-----------------------------|-----------------|----------------|---------------|---------------|---------------|
|                             | **CC001**       | **CC002**      | **CC003**     | **CC004**     |               |
| **Primārās izmaksas**            | **10.100,00**   | **14.200,00**  | **14.000,00** | **8.500,00**  | **46.800,00** |
| &nbsp;&nbsp;&nbsp;&nbsp;1001                            | 100,00          | 200,00         | 6.000,00      | 2.000,00      | **8.300,00**  |
| &nbsp;&nbsp;&nbsp;&nbsp;1002                            | 10.000,00       | 10.000,00      | 8.000,00      | 6.500,00      | **34.500,00** |
|&nbsp;&nbsp;&nbsp;&nbsp;1003                             | 0,00            | 4.000,00       | 0,00          | 0,00          | **4.000,00**  |
|**Sekundārās izmaksas**                            | **–10 100,00**  | **–14 200,00** | **17,082,75** | **7.217,25**  | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC001                            | \-10 100,00     | 3.535,00       | 5.555,00      | 1.010,00      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC002                             | 0,00            | \-17 735,00    | 11.527,75     | 6.207,25      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC003                            | 0,00            | 0,00           | 0,00          | 0,00          | 0,00          |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC004                             | 0,00            | 0,00           | 0,00          | 0,00          | 0,00          |
| **Kopsumma**                   | **0,00**        | **0,00**       | **31.082,75** | **15.717,25** | **46.800,00** |

Izmantojot **izmaksu apkopojuma politiku** un **sekundāro izmaksu elementus**, varat izmantot primārās izmaksas pēc izmaksu objekta iekšējiem pārskatiem kā primārās izmaksas, kas paliek pēc **pieskaitāmo izmaksu aprēķināšanas**.

Ja šī piemēra ietvaros netiktu izveidota **izmaksu apkopojuma politika**, tiktu iegūts tālāk norādītais pārskata rezultāts. Izmaksu plūsma ir pareiza, taču ir zaudēti ieskati par izmaksu plūsmu starp izmaksu centriem un šīs plūsmas izsekojamība.

| **Peļņas un zaudējumu aprēķins** | **Izmaksu objekts** |           |               |               |          **Kopsumma**  |
|-----------------------------|-----------------|-----------|---------------|---------------|---------------|
|                             | **CC001**       | **CC002** | **CC003**     | **CC004**     |               |
| **Primārās izmaksas**            | **0,00**        | **0,00**  | **31.082,75** | **15.717,25** | **46.800,00** |
|&nbsp;&nbsp;&nbsp;&nbsp;1001                              | 0,00            | 0,00      | 6.207,75      | 2.092,25      | **8.300,00**  |
| &nbsp;&nbsp;&nbsp;&nbsp;1002                             | 0,00            | 0,00      | 22.275,00     | 12.225,00     | **34.500,00** |
|&nbsp;&nbsp;&nbsp;&nbsp;1003                              | 0,00            | 0,00      | 2600,00       | 1.400,00      | **4.000,00**  |
|**Sekundārās izmaksas**                            | **0,00**        | **0,00**  | **0,00**      | **0,00**      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC001                             | 0,00            | 0,00      | 0,00          | 0,00          | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC002                             | 0,00            | 0,00      | 0,00          | 0,00          | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC003                             | 0,00            | 0,00      | 0,00          | 0,00          | 0,00          |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC004                             | 0,00            | 0,00      | 0,00          | 0,00          | 0,00          |
| **Kopsumma**                   | **0,00**        | **0,00**  | **31.082,75** | **15.717,25** | **46.800,00** |

Atkarībā no organizācijas pārskatu un izsekojamības prasībām varat noteikt pareizo sekundāro izmaksu elementu līmeni un izveidot izmaksu apkopojuma kārtulas, kas atbilst jūsu vajadzībām.

Skaidrais **izmaksu sadalījuma** un **izmaksu apkopošanas politiku** nošķīrums sniedz iespēju nepārtraukti veikt atjauninājumus, neradot savstarpēju ietekmi.



## <a name="see-also"></a>Skatiet arī
-  [Izmaksu objekta dimensijas](cost-objects.md)
-  [Izmaksu elementu dimensijas](cost-elements.md)
-  [Dimensiju hierarhijas](dimension-hierarchy.md)
-  [Pieskaitāmo izmaksu aprēķināšana](overhead-calculation.md)

