---
title: Dimensiju hierarhija
description: "Šajā tēmā ir sniegta informācija par dimensiju hierarhijām. Izmantojot dimensiju hierarhiju, varat definēt pārskatu struktūru, izmaksu ierobežojumus un drošības iestatījumus modulī Izmaksu uzskaite."
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimensionHierarchy,
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 40a4a1d7549876b72186f30a9c0089f0d27cf3b6
ms.contentlocale: lv-lv
ms.lasthandoff: 03/26/2018

---

# <a name="dimension-hierarchy"></a>Dimensiju hierarhija

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par dimensiju hierarhijām. Izmantojot dimensiju hierarhiju, varat definēt pārskatu struktūru, izmaksu ierobežojumus un drošības iestatījumus modulī Izmaksu uzskaite.  

## <a name="overview"></a>Pārskats

Dimensiju hierarhijas tiek izmantotas dažādās moduļa Izmaksu uzskaite sadaļās. Dimensiju hierarhija sniedz iespēju definēt tālāk norādīto informāciju.

-  Pārskatu struktūru, kas atbilst organizācijas prasībām
-  Izmaksu politikas
-  Drošības iestatījumus

Tālāk ir sniegts dimensiju hierarhijas piemērs.

![Dimensiju hierarhijas piemērs](./media/dimension-hierarchy.png)

Var izveidot tālāk norādīto dimensiju veidu dimensiju hierarhiju.

-  Izmaksu elementu dimensijas
-  Izmaksu objekta dimensijas
-  Statiskās dimensijas

> [!NOTE]
> - Ja ir nepieciešamas dažādas perspektīvas, vienai dimensijai var izveidot vairākas dimensiju hierarhijas.
> - Dimensiju hierarhiju var saistīt tikai ar vienu dimensiju.
> - Dimensiju hierarhijas struktūrā var ietvert neierobežotu skaitu līmeņu. Visi līmeņi ir pieejami darbvietā **Izmaksu kontrole**. Ja pārskatu veidošanai izmantojat programmu Microsoft Excel vai Microsoft Power BI, tiek eksportēti tikai pirmie 15 dimensiju hierarhijas līmeņi. Šis ierobežojums pastāv tāpēc, ka gan Excel, gan Power BI ir nepieciešama fiksēta shēma.
> - Dimensiju hierarhija nav atkarīga no datuma. Tāpēc visas dimensiju hierarhijas izmaiņas tiek nekavējoties saglabātas ierakstā, un jūs nevarat salīdzināt stāvokli pirms noteikta datuma un pēc noteikta datuma.

## <a name="dimension-hierarchy-type"></a>Dimensiju hierarhijas tips

Kad izveidojat jaunu dimensiju hierarhiju, ir jāatlasa hierarhijas veids. Pārejiet uz sadaļu **Izmaksu uzskaite** > **Dimensijas** > **Dimensiju hierarhijas**. Noklikšķiniet uz **Jauna** un atlasiet dimensiju hierarhijas veidu. Varat atlasīt **Dimensiju kategorizācijas hierarhija** vai **Dimensiju klasifikācijas hierarhija**.

### <a name="dimension-categorization-hierarchy"></a>Dimensiju kategorizācijas hierarhija

Veids **Dimensiju kategorizācijas hierarhija** tiek izmantots pārskatu veidošanai. Tas atbalsta tikai izmaksu elementu dimensijas. Ja atlasāt šo veidu, ir spēkā tālāk norādītie nosacījumi.

-  Dimensijas elementu var vairākas reizes saistīt hierarhijas struktūras ietvaros.
-  Varat ievietot izmaksu elementa dimensijas elementu dažādos mezglos, piešķirot lapas mezglam izmaksu izturēšanos.

### <a name="dimension-classification-hierarchy"></a>Dimensiju klasifikācijas hierarhija

Veids **Dimensiju klasifikācijas hierarhija** tiek izmantots kārtulu definēšanai un pārskatu veidošanai. Tas atbalsta visas dimensijas, piemēram, izmaksu objektu, izmaksu elementu un statistiskās dimensijas. Ja atlasāt šo veidu, dimensijas elementu var saistīt tikai vienu reizi hierarhijas struktūras ietvaros.

## <a name="create-and-maintain-a-dimension-hierarchy"></a>Dimensiju hierarhijas izveide un uzturēšana

Dimensiju hierarhija tiek veidota kā koka struktūra, kurā pastāv mezglu un lapu mezglu relācijas.

-  Katram mezglam var būt 1:_n_ apakšmezgli.
-  Mezglam nevar piešķirt gan apakšmezglus, gan lapu mezglus.
-  Lapas mezglu var piešķirt tikai zemākajā hierarhijas līmenī.

### <a name="example"></a>Paraugs

Mazam uzņēmumam ir tālāk norādītā organizācijas struktūra, kurā finanšu un personāla vadības nodaļas ir pakļautas administrācijai, bet montāžas un iepakošanas nodaļas ir pakļautas ražošanas nodaļai.

![Organizācijas struktūras piemērs](./media/dimension-hierarchy-org.png)

Izmaksu objekta dimensija atbilst viesiem izmaksu centriem organizācijā.

- Izmaksu objekta dimensija
    - Izmaksu centri

Izmaksu objekta dimensiju, kas atbilst visiem izmaksu centriem, var iestatīt tālāk norādītajā veidā.

| Izmaksu centri | Apraksts |
|--------------|-------------|
| CC001        | HR          |
| CC002        | Finansēt     |
| CC003        | Nodokļi         |
| CC007        | Debitoru parādi/parādi kreditoriem       |
| CC005        | Montāža    |
| CC006        | Iepakošana   |

Izmaksu elementa dimensija atbilst viesiem izmaksu elementiem organizācijā.

- Izmaksu elementa dimensija
    - Izmaksu elementi

Izmaksu elementa dimensiju, kas atbilst visiem izmaksu elementiem, var iestatīt tālāk norādītajā veidā.

| Izmaksu elementi | Apraksts |
|---------------|-------------|
| 10001         | Elektrība |
| 10010         | Tīrīšana    |
| 10011         | Apsilde     |
| 40001         | PPPI        |

Organizācijas pārskatu prasībām atbilstošu dimensiju hierarhiju var iestatīt tālāk norādītajā veidā.

**Detalizēta informācija par dimensiju hierarhiju**

| Dimensiju hierarhijas nosaukums | Dimensija    | Dimensiju hierarhijas veida nosaukums      | Piekļuves sarakstu hierarhija |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organizācija             | Izmaksu centri | Dimensiju klasifikācijas hierarhija | Nav                    |

Pārskatu dimensiju hierarhiju var iestatīt tālāk norādītajā veidā.

|                   | Dimensijas elementu diapazons   |                         |
|-------------------|---------------------------|-------------------------|
| **Mezgli**         | **Avota dimensijas elements** | **Mērķa dimensijas elements** |
| Organizācija      |                           |                         |
| &nbsp;&nbsp;Administrators         |                           |                         |
|&nbsp;&nbsp;&nbsp;&nbsp;Finansēt   | CC002                     | CC003                   |
|                   | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;HR        | CC001                     | CC001                   |
| &nbsp;&nbsp;Ražošana    |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Iepakošana | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Montāža  | CC006                     | CC006                   |

Ierobežojuma prasībām atbilstošu dimensiju hierarhiju var iestatīt tālāk norādītajā veidā.

**Detalizēta informācija par dimensiju hierarhiju**

| Dimensiju hierarhijas nosaukums | Dimensija     | Dimensiju hierarhijas veida nosaukums      |
|--------------------------|---------------|------------------------------------|
| Izmaksu izturēšanās            | Izmaksu elementi | Dimensiju klasifikācijas hierarhija |

Ierobežojuma dimensiju hierarhiju var iestatīt tālāk norādītajā veidā.

|                   | Dimensijas elementu diapazons   |                         |
|-------------------|---------------------------|-------------------------|
| **Mezgli**         | **Avota dimensijas elements** | **Mērķa dimensijas elements** |
| Izmaksu izturēšanās     |                           |                         |
| &nbsp;&nbsp;Fiksētas izmaksas    | 10001                     | 10011                   |
|&nbsp;&nbsp;Mainīgas izmaksas | 40001                     | 40010                   |

> [!NOTE]
> Sadaļā **Dimensijas elementu diapazons** mezgls var ietvert 1:_n_ dimensiju elementu diapazonus. Varat ievietot vēl neesošu dimensiju elementu ID. Tādējādi hierarhija tiek padarīta viegli pielāgojama.  

### <a name="copy-a-hierarchy"></a>Hierarhijas kopēšana

Varat kopēt pašreizējo dimensiju hierarhiju, lai to izmantotu kā sākumpunktu jaunas dimensiju hierarhijas izveidei. Šī pieeja var būt noderīga, ja vēlaties salīdzināt iepriekšējo dimensiju hierarhiju ar jauno dimensiju hierarhiju.

### <a name="rearrange-nodes-in-a-hierarchy"></a>Hierarhijas mezglu pārkārtošana

Varat pārvietot mezglu hierarhijā uz augšu un uz leju tā pašreizējā līmeņa ietvaros. Tādējādi varat pārkārtot mezglus pārskaut izveidei darbvietā **Izmaksu kontrole**.

Lai pārvietotu mezglu uz jaunu vietu hierarhijā, ir jāatlasa mērķa mezgls. Mezglu var pārvietot divos tālāk norādītajos veidos.

- **Pārvietot zem** — pārvietojiet atlasīto mezglu no tā pašreizējās pozīcijas hierarhijā un ievietojiet to **zem** atlasītā mērķa mezgla.
- **Pārvietot pēc** — pārvietojiet atlasīto mezglu no tā pašreizējās pozīcijas hierarhijā un ievietojiet to **pēc** atlasītā mērķa mezgla tā hierarhijas līmeņa ietvaros.

> [!NOTE] 
> Eksportējot datus uz programmu Excel vai Power BI, netiek saglabāta mezglu secība, jo šajos rīkos pēc noklusējuma tiek izmantota burtciparu kārtošanas secība. Secība ir jāmaina manuāli.

## <a name="define-dimension-hierarchies-for-reporting"></a>Dimensiju hierarhiju definēšana pārskatu izveidei

Dimensiju hierarhijas ir svarīgas pārskatu izveidi. Tās sniedz iespēju definēt konkrēto struktūru, kas atbilst noteiktas organizācijas prasībām. Dimensiju hierarhijas mezgla līmenī veiktās apkopošanas sniedz ieinteresētajām pusēm jebkurā organizācijas līmenī skatīt jebkura līmeņa datus.

Dimensiju hierarhijas ir pieejamas tālāk norādītajos pārskatu rīkos. Šī pieeja palīdz nodrošināt konsekvenci pārskata struktūras ietvaros.

- Darbvieta **Izmaksu kontrole** (klients):

    - tiek kontrolēta, izmantojot konfigurāciju.

- Darbvieta **Izmaksu kontrole** (mobilā lietojumprogramma):

    - tiek kontrolēta, izmantojot konfigurāciju.

- Excel

    - Sniedz iespēju katrai eksportēšanas definīcijai atlasīt noteiktu dimensiju hierarhiju.

        - Viena izmaksu elementu dimensiju hierarhija (obligāti)
        - Viena izmaksu objektu dimensiju hierarhija (pēc izvēles)
        - Viena statistisko dimensiju hierarhija (pēc izvēles)

- Power BI:

    - ir pieejamas visas dimensiju hierarhijas.
    
Ja veidojat pārskatus, izmantojot programmu Excel vai Power BI, tiek eksportēti tikai pirmie 15 dimensiju hierarhijas līmeņi. Šis ierobežojums pastāv tāpēc, ka programmā Excel un Power BI ir nepieciešama fiksēta shēma. Ja hierarhijā ir vairāk nekā 15 līmeņi, papildu līmeņi netiek eksportēti. Normalizētajā tabulā ir ietverts katra hierarhijas dimensijas elementa ierakts. Tāpēc notiek automatizēta apkopošana. Tas palīdz nodrošināt, ka jebkurā no 15 pieejamajiem hierarhijas līmeņiem joprojām ir pareiza bilance.

Tālāk ir sniegts pārskatu struktūrā ietvertas dimensiju hierarhijas piemērs.

| Izmaksu objektu dimensiju hierarhija — 1. līmenis | Izmaksu objektu dimensiju hierarhija — 2. līmenis | Izmaksu objektu dimensiju hierarhija — 3. līmenis | Izmaksu objektu dimensiju hierarhija — 4. līmenis | Izmaksu objektu dimensiju hierarhija — 15. līmenis |
|-------------------------------------------|-------------------------------------------|-------------------------------------------|-------------------------------------------|--------------------------------------------|
| Organizācija                              | Administrators                                     | Finansēt                                   | CC002                                     |                                            |
| Organizācija                              | Administrators                                     | Finansēt                                   | CC003                                     |                                            |
| Organizācija                              | Administrators                                     | Finansēt                                   | CC007                                     |                                            |
| Organizācija                              | Administrators                                     | HR                                        | CC001                                     |                                            |
| Organizācija                              | Ražošana                                | Iepakošana                                 | CC005                                     |                                            |
| Organizācija                              | Ražošana                                | Montāža                                  | CC006                                     |                                            |

### <a name="update-the-dimension-hierarchies-that-are-used-for-reporting"></a>Pārskatiem izmantoto dimensiju hierarhiju atjaunināšana 

Pēc kāda laika ir jāatjaunina iepriekš minētajos pārskatu rīkos izmantotās dimensiju hierarhijas. Dimensiju hierarhijas var atjaunināt, atsvaidzinot klientu.

- Darbvieta **Izmaksu kontrole** (klients)
- Darbvieta **Izmaksu kontrole** (mobilā lietojumprogramma)

Dimensiju hierarhiju atjauninājumi tiek fiksēti ik pēc 24 stundām, un to nodrošina kešatmiņa iepriekš saglabāts darbs. Pēc eksportēto datu atjaunināšanas izmainītās dimensiju hierarhijas ir pieejamas tālāk norādītajos rīkos.

- Excel
- Power BI

> [!NOTE] 
> Lai manuāli aktivizētu dimensiju hierarhijas kešatmiņas atjaunināšanu, varat no jauna eksportēt uz programmu Excel vienu vai vairākas dimensiju hierarhijas, kas ir jāatjaunina.

## <a name="define-dimension-hierarchies-for-cost-policies"></a>Izmaksu ierobežojumu dimensiju hierarhiju definēšana

Izmaksu uzskaites ietvaros tiek izmantoti vairāki ierobežojumi, kam tiek definētas detalizētas kārtulas. Tālāk norādītajiem ierobežojumiem ir jādefinē viena vai vairākas dimensiju hierarhijas.

- Izmaksu izturēšanās
- Izmaksu sadale
- Izmaksu sadalījums
- Izmaksu apkopojums

Dimensiju hierarhijas atvieglo kārtulu izveidi. Lai nevajadzētu izveidot kārtulas katram dimensijas elementam, varat izmantot dimensiju elementu apkopojumus, ko nodrošina dimensiju hierarhijas līmeņi. Ja kārtulas pārklājas, ir jādefinē konkrētas kārtulas, kas sistēmā tiks ņemtas vērā, veidot pieskaitāmo izmaksu aprēķinu.

### <a name="example-define-a-cost-behavior-policy"></a>Piemērs: izmaksu izturēšanās ierobežojuma definēšana

Tiek izveidots jauns izmaksu izturēšanās ierobežojums, un tam tiek piešķirtas atbilstošās dimensiju hierarhijas, kā tas ir parādīts tālāk.

**Izmaksu izturēšanās ierobežojums**

| Ierobežojuma nosaukums   | Izmaksu elementu dimensiju hierarhija | Izmaksu objektu dimensiju hierarhija | Uzskaites valūta |
|---------------|----------------------------------|---------------------------------|---------------------|
| Izmaksu izturēšanās | Izmaksu izturēšanās                    | Organizācija                    | USD                 |

**Kārtulas**

| Izmaksu elementu dimensiju hierarhijas mezgls | Izmaksu objektu dimensiju hierarhijas mezgls | Fiksēta procentuālā vērtība | Fiksēta summa | Derīgs no | Derīgs līdz |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|----------|
| Fiksētas izmaksas                            | Organizācija                         | 100,00           | 0,00         | 01.01.2017.   | Nekad    |
| 10001                                 | Organizācija                         | 0,00             | 150,00       | 01.01.2017.   | Nekad    |
| 10001 (\*)                             | Finansēt                              |                  | 50,00        | 01.01.2017.   | Nekad    |
| Izmaksu izturēšanās vai Mainīgās izmaksas (\*\*)   | Organizācija                         | 0,00             | 0,00         | 01.01.2017.   | Nekad    |

\* Mainīgo izmaksu mezgls nav nepieciešams. Ja izmaksas nav klasificētas kā fiksētas izmaksas, tām ir jābūt mainīgajām izmaksām.

\*\* Tiek izveidota detalizēta kārtula, apvienojot izmaksu elementu 10001 un visus izmaksu objektu elementus, kas ir apkopoti hierarhijas līmenī Finanses (CC002, CC003, CC007).

Iepriekšējās kārtulas liecina par pielāgojamību, ko nodrošina dimensiju hierarhijas. Definējot augsta līmeņa kārtulas, varat samazināt uzturēšanai vajadzīgo laiku. Pēc tam varat definēt detalizētas kārtulas, kas atbilst noteiktiem uzņēmējdarbības mērķiem.

Ja tiek atjauninātas kārtulās izmantotās dimensiju hierarhijas, sistēma automātiski izceļ atjauninājumus.

Ja vairs nav nepieciešams kāds kārtulu granularitātes līmenis, attiecīgo kārtulu var anulēt.

Piemēram, vairs nav nepieciešama noteikta izmaksu objektu dimensiju hierarhijas Finanses izmaksu izturēšanās kārtula. Šādā gadījumā noklikšķiniet uz **Derīguma kārtula**, lai anulētu šo kārtulu.

| Izmaksu elementu dimensiju hierarhijas mezgls | Izmaksu objektu dimensiju hierarhijas mezgls | Fiksēta procentuālā vērtība | Fiksēta summa | Derīgs no | Derīgs līdz  |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|-----------|
| Fiksētas izmaksas                            | Organizācija                         | 100,00           | 0,00         | 01.01.2017.   | Nekad     |
| 10001                                 | Organizācija                         | 0,00             | 150,00       | 01.01.2017.   | Nekad     |
| 10001                                 | Finansēt                              |                  | 50,00        | 01.01.2017.   | 20.01.2017. |
| Izmaksu izturēšanās vai Mainīgās izmaksas        | Organizācija                         | 0,00             | 0,00         | 01.01.2017.   | Nekad     |

Šī kārtula netiek ņemta vērā nevienā pieskaitāmo izmaksu aprēķinā, kas tiek veikts pēc 2017. gada 20. janvāra.

> [!NOTE] 
> Lauki **Derīgs no** un **Derīgs līdz** ir atkarīgi no datuma un laika. Varat anulēt kārtulu un tajā pašā dienā palaist jaunu pieskaitāmo izmaksu aprēķinu.

## <a name="define-dimension-hierarchies-for-security-setup"></a>Dimensiju hierarhiju definēšana drošības iestatīšanai

Izmaksu uzskaites dati ir jāpadara pieejami visiem vadītājiem, kuri ir atbildīgi par kādu pārskata vienību. Saskaņā ar izmaksu uzskaites terminoloģiju pārskata vienībai atbilst izmaksu objekts vai izmaksu objektu kopa.

Pastāv iespēja, ka visi vadītāji varēs piekļūt ļoti sensitīviem uzņēmējdarbības datiem, piemēram, informācijai par ieņēmumiem un peļņu. Tāpēc ir svarīgi iestatīt drošības līdzekļus, lai vadītāji varētu skatīt tikai tos datus, kas attiecas uz viņiem. Lai palīdzētu kontrolēt datu drošību, varat definēt dimensiju hierarhijas.

- Dimensiju hierarhijas var izmantot tikai tad, ja atsaucē uz dimensiju hierarhiju atlasītā dimensijas vērtība ir izmaksu objekta dimensija.
- Katrai izmaksu objekta dimensijai piekļuves saraksta hierarhijā var iespējot tikai vienu dimensiju hierarhiju.

**Detalizēta informācija par dimensiju hierarhiju**

| Dimensiju hierarhijas nosaukums | Dimensija    | Dimensiju hierarhijas veida nosaukums      | Piekļuves sarakstu hierarhija |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organizācija             | Izmaksu centri | Dimensiju klasifikācijas hierarhija | **Jā**               |

Hierarhiju veidotājā ir pieejama jauna kopsavilkuma cilne **Lietotāji**. Tajā varat ievietot vienu vai vairākus lietotāju ID katrā hierarhijas mezglā.

|                 | Lietotāji            | Dimensijas elementu diapazons   |                         |
|-----------------|------------------|---------------------------|-------------------------|
| **Mezgli**       | **Lietotāja ID**      | **Avota dimensijas elements** | **Mērķa dimensijas elements** |
| Organizācija    | Bendžamins, Klēra |                           |                         |
| &nbsp;&nbsp;Administrators         | Aprīlī            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Finansēt   | Alīsija           | CC002                     | CC003                   |
|                 |                  | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;HR        | Ārnijs            | CC001                     | CC001                   |
| &nbsp;&nbsp;Ražošana    | Deivids            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Iepakošana | Elēna            | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Montāža  | Kriss            | CC006                     | CC006                   |

> [!NOTE] 
> Izmaksu grāmatveži ir jāpiešķir augstākajam hierarhijas līmenim, lai viņi varētu skatīt visus ierakstus darbvietā Izmaksu uzskaite.

Lai iespējotu piekļuves saraksta hierarhiju un tās drošības iestatījumus, pārejiet uz sadaļu **Izmaksu uzskaite** > **Iestatīšana** > **Parametri** > **Vispārīgi**. Atlasiet parametru **Iespējot skatīšanas piekļuvi izmaksu objekta dimensijas elementiem**.

Piekļuves saraksta hierarhijas iestatījumi tiek izmantoti, lai kontrolētu to, kādi dati tiek rādīti tālāk norādītajos apgabalos.

- Darbvieta **Izmaksu kontrole** (klients):

    - Dati formātos, kas tiek izmantoti detalizētas informācijas skatīšanai par noteiktiem gadījumiem

- Darbvieta **Izmaksu kontrole** (mobilā lietojumprogramma):

    - Kartēs norādītās bilances

- Power BI:

    - Power Bi vizualizācijās attēlotie dati
    - Programmas Microsoft Dynamics 365 for Finance and Operations klientā iegultās datu Power BI vizualizācijas

> [!NOTE] 
> - Lai piekļuves saraksta hierarhija varētu ietekmēt datus pakalpojumā Power BI, piekļuves saraksta hierarhija ir jāsavieno pārī ar rindas līmeņa drošību pakalpojumā Power BI. Papildinformāciju skatiet rakstā [Drošības iestatīšana satura pakotnei Izmaksu uzskaite](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).
> - Piekļuves saraksta hierarhija nepalīdz aizsargāt datu eksportēšanu uz programmu Excel. Tāpēc pārskatu rīku drīkst izmantot tikai izmaksu grāmatveži un vadītāji, kuriem ir nepieciešama pilna piekļuve datu skatīšanai.

