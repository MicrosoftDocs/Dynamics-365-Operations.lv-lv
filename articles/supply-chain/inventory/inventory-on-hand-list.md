---
title: Rīcībā esošo krājumu saraksts
description: Šajā tēmā ir aprakstīts, kā izmantot rīcībā esošo sarakstu lapu, lai pārbaudītu rīcībā esošo krājumu detaļas. Tas parāda dažus veidus, kā dažādās filtrēšanas un šķirošanas iespējas darbojas kopā, un to, kā šīs iespējas dažreiz var radīt negaidītus rezultātus, kad tās tiek apvienotas.
author: yufeihuang
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventOnhandItem, InventOnHandItemListPage, WHSOnHand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 9464240123ec2248e1b66f32dd3c9a2f974512b6
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573925"
---
# <a name="inventory-on-hand-list"></a>Rīcībā esošo krājumu saraksts

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā izmantot **rīcībā esošo sarakstu** lapu, lai pārbaudītu rīcībā esošo krājumu detaļas. Tas parāda dažus veidus, kā dažādās filtrēšanas un šķirošanas iespējas darbojas kopā, un to, kā šīs iespējas dažreiz var radīt negaidītus rezultātus, kad tās tiek apvienotas.

## <a name="query-your-on-hand-inventory"></a>Rīcībā esošo krājumu vaicājums

Lai pārbaudītu krājumu pieejamību, dodieties uz **Krājumu pārvaldība \> Vaicājumi un pārskati \> Rīcībā esošais saraksts**.

**Rīcībā esošā saraksta** lapa tiek automātiski atjaunināta, kad tiek veiktas krājumu transakcijas. Šīs transakcijas var būt prognozētas, fiziskas vai finanšu transakcijas.

Izmantojiet tālāk norādītos rīkus, lai atrastu preču kopu, ko meklējat:

- Darbību rūtī atlasiet [**Dimensijas**](#dimensions), lai atvērtu dialoglodziņu, kur varat pievienot vai noņemt kolonnas, kas tiek rādītas **Rīcībā esošajā** režģī.
- [**Filtru** rūtī](#filters-pane) ievadiet vērtības konkrētiem laukiem, lai parādītu tikai tos ierakstus, kas atbilst šīm vērtībām. Ņemiet vērā, ka šeit definētie filtri attiecas uz avota tabulām, ko var apkopot vēlāk, atbilstoši dimensijām, ko esat atlasījis rādīšanai. Informāciju par to, kā šī uzvedība var ietekmēt jūsu rezultātus, skatiet sekojošajos [piemēros](#examples) turpmāk tēmā.
- Rūtī **Filtri** atlasiet **Lietot**, lai ģenerētu rīcībā esošo krājumu salīdzināšanas sarakstu **Rīcībā esošajā** režģī.
- **Rīcībā esošajā** režģī atlasiet jebkuru kolonnas virsrakstu, lai kārtotu vai filtrētu pēc vērtībām šajā kolonnā. QuickFilter, kas atrodas režģa sākumā, piedāvā papildu filtrēšanas opcijas. Šie filtri attiecas uz rezultātiem, nevis uz avota tabulām. Informāciju par to, kā šī uzvedība var ietekmēt jūsu rezultātus, skatiet sekojošajos [piemēros](#examples) turpmāk tēmā.

Katram saskaņotajam vienumam **Rīcībā esošais** režģis sniedz šādas krājumu informācijas kolonnas.

| Kolonna | apraksts |
|---|---|
| Fizisks krājums | Krājumos pieejamais fiziskais daudzums. |
| Fiziski rezervēts | Kopējais daudzums, kas tika fiziski rezervēts. |
| Fiziski pieejams | Fiziskajos krājumos pieejamais (nav rezervēts) daudzums.<p>**Pieejamais fiziskais** ir aprēķināts lauks. Vērtība ir vienāda ar **Fizisko krājumu** vērtību mīnus **Fiziski rezervētā** vērtība.</p> |
| Pieejams fiziskais papildu dimensijās | Pieejamais fiziskais daudzums visām dimensijām, kas tiek rādītas režģī. |
| Pasūtīts kopā | Kopējais daudzums, kas ir iekļauts ienākošajos pasūtījumos vai kam ir pozitīvs daudzums dažādos krājumu žurnālos. |
| Pasūtīts | Kopējais daudzums, kas ir iekļauts izejošajos pasūtījumos vai kam ir negatīvs daudzums dažādos krājumu žurnālos. |
| Rezervēts pasūtījumos | Kopējais daudzums, kas ir rezervēts pasūtītai saņemšanai. Vērtība šajā laukā parāda kopējo krājumu daudzumu izejošajās darbībās, kurām ir statuss _Pasūtīts rezervēts_. Krājumi, kas ir rezervēti kā pasūtīti, nav fiziski pieejami krājumā. Tāpēc tās nevar tikt tieši izdotas un piegādātas. |
| Pieejams rezervācijai | Kopējais rīcībā esošo krājumu daudzums, kuru var rezervēt.<p>**Piezīme.** Ja izvēles rūtiņa **Rezervēt pasūtītos vienumus** ir atlasīta lapā **Krājumu un noliktavas pārvaldības parametri**, vērtība šajā laukā iekļauj paredzamo saņemšanu. Ja izvēles rūtiņa ir notīrīta, vērtība izslēdz paredzamo saņemšanu.</p> |
| Pieejams krājumos | Kopējais pieejamais daudzums.<p>**Kopējais pieejamais** ir aprēķināts lauks. Vērtība ir vienāda ar **Pieejamo fizisko** vērtību plus **Pasūtītā kopējā** vērtība mīnus **Pēc pasūtījuma** vērtība.</p> |

## <a name="apply-filters-to-find-the-records-that-youre-looking-for"></a><a name="filters-pane"></a>Lietot filtrus, lai atrastu meklētos ierakstus

Izmantojiet **Filtru** rūti, lai filtrētu rīcībā esošo krājumu sarakstu tā, lai tas iekļautu tikai tos ierakstus, kuros lauku vērtības atbilst filtrēšanas kritērijiem. Lai definētu filtru, izpildiet tālāk aprakstītās darbības.

1. Rūtī **Filtri** sameklējiet lauku, kuru vēlaties filtrēt.
2. Laukā zem mērķa lauka nosaukuma atlasiet loģisko operatoru (piemēram, *sākas ar*, *vienāds ar* vai *lielāks par*).
3. Ievadiet vai atlasiet meklējamo vērtību.

> [!IMPORTANT]
> **Rīcībā esošā saraksta** lapa tiek apkopota no detalizētas rīcībā esošo krājumu tabulas, kas ietver visas pieejamās dimensijas. Tomēr saraksts šajā lapā ir kopsavilkums. Tāpēc tā var apvienot rindas no avota tabulas, apkopojot vērtības atbilstoši parādītajām dimensijām.
>
> Filtri, ko nosakāt **Filtru** rūtī, attiecas uz avota tabulu, nevis uz apkopoto sarakstu. Šī uzvedība reizēm var izraisīt negaidītus rezultātus. Informāciju par to, kā šī uzvedība var ietekmēt jūsu rezultātus, skatiet sekojošajos [piemēros](#examples) turpmāk tēmā.
> 
> Tomēr [režģī sniegtie filtri](#grid-filters) *attiecas* uz apkopoto sarakstu. Šie filtri ietver gan QuickFilter režģa augšpusē, gan katra kolonnas virsraksta filtru.

Varat modificēt filtru kopu, kas ir pieejama **Filtru** rūtī, veicot šādas darbības.

- Lai noņemtu filtru no rūts, atlasiet tā **Aizvērt** pogu (**X**).
- Lai pievienotu filtru, atlasiet **Pievienot** **Filtru** rūts augšpusē. Parādās dialoglodziņš **Pievienot filtra laukus**, kas parāda pieejamo lauku sarakstu. Tas arī rāda informāciju par katra lauka datu tipu un tabulu. Izmantojiet kolonnu virsrakstus, lai filtrētu un kārtotu pēc nepieciešamības, un pēc tam atzīmējiet izvēles rūtiņu katram laukam, kuru vēlaties pievienot **Filtra** rūtij. Kad esat pabeidzis, atlasiet **Iespraust**, lai piemērotu izmaiņas.

## <a name="select-which-dimensions-to-show"></a><a name="dimensions"></a>Atlasīt rādāmās dimensijas

Dimensijas sniedz vairāk par katru rīcībā esošo vienumu, kas atrodas rīcībā esošajā krājumā, un sniedz vairāk veidu, kā kārtot un filtrēt sarakstu. Dimensijas, ko atlasāt, lai parādītu, ietekmē arī to, kā rindas tiek apkopotas **Rīcībā esošā saraksta** lapā. Šis apkopojums, savukārt, var ietekmēt to, kā avota tabulu rindas tiek apvienotas redzamajos rezultātos. Informāciju par to, kā šī uzvedība var ietekmēt jūsu rezultātus, skatiet sekojošajos [piemēros](#examples) turpmāk tēmā.

Lai pielāgotu rādāmo krājumu dimensiju atlasi, veiciet šīs darbības.

1. Darbību rūtī atlasiet **Dimensijas**.

    Parādītais dialoglodziņš **Dimensijas displejs** rāda katru dimensiju.

2. Atzīmējiet izvēles rūtiņu katrai dimensijai, ko vēlaties iekļaut režģī.
3. Ja vēlaties, lai atlase tiktu izmantota pēc noklusējuma, nākamreiz, kad atverat **Rīcībā esošo saraksta** lapu, iestatiet opciju **Saglabāt iestatījumu** uz **Jā**. Ja šī opcija ir iestatīta uz **Nē**, atlase tiks izmantota tikai pašreizējās sesijas laikā. Tāpēc nākamreiz, atverot lapu, tiks izmantota pašreizējā noklusējuma atlase.
4. Atlasiet **Labi**, lai izmaiņas piemērotu un aizvērtu dialoglodziņu.

## <a name="filter-on-the-output-of-the-inventory-on-hand-list"></a><a name="grid-filters"></a>Filtrēt rīcībā esošo krājumu saraksta izvadi

Varat atlasīt jebkuru kolonnas virsrakstu **Rīcībā esošajā** režģī, lai kārtotu vai filtrētu pēc vērtībām šajā kolonnā. QuickFilter, kas atrodas režģa sākumā, piedāvā papildu filtrēšanas opcijas. Šie filtri attiecas uz rezultātiem, nevis uz avota tabulām. Informāciju par to, kā šī uzvedība var ietekmēt jūsu rezultātus, skatiet sekojošajos [piemēros](#examples) turpmāk tēmā.

> [!NOTE]
> Nevar filtrēt un kārtot pēc visām kolonnām. Lielākajā daļā daudzuma kolonnu nav iekļautas kārtošanas un filtrēšanas vadīklas, jo tās ir aprēķinātie lauki. Kolonna **Pēc pasūtījuma** ir izņēmums.

## <a name="examples"></a><a name="examples"></a>Piemēri

Sistēmā ir ietverta detalizēta (neapkopota) krājumu tabula, kurā redzami šādi rīcībā esošie krājumi.

| Krājuma numurs | Vietne | Noliktava | Fizisks krājums | Fiziski pieejams |
|---|---|---|---|---|
| IA0001 | 1 | 1 | 1 | 1 |
| IA0001 | 1 | 2 | 2 | 2 |
| IA0001 | 1 | 3 | 1 | 1 |

### <a name="scenario-1"></a>1. scenārijs

**Rīcībā esošā saraksta** lapa ir iestatīta, lai tiktu rādītas šādas pēdējās dimensijas:

- Krājuma numurs
- Vietne
- Noliktava

**Filtru** rūtī ir iestatīti šādi filtrēšanas kritēriji:

- **Krājuma kods** \| **ir precīzi** \| _IA0001_
- **Pieejamā fiziskā** \| **vērtība ir mazāka par vai vienāda ar** \| _1_

Šeit ir iegūtā izvade.

| Krājuma numurs | Vietne | Noliktava | Fizisks krājums | Fiziski pieejams |
|---|---|---|---|---|
| IA0001 | 1 | 1 | 1 | 1 |
| IA0001 | 1 | 3 | 1 | 1 |

### <a name="scenario-2"></a>2. scenārijs

**Rīcībā esošā saraksta** lapa ir iestatīta, lai tiktu rādītas šādas pēdējās dimensijas:

- Krājuma numurs
- Vietne

**Filtru** rūtī ir iestatīti šādi filtrēšanas kritēriji:

- **Krājuma kods** \| **ir precīzi** \| _IA0001_
- **Pieejamā fiziskā** \| **vērtība ir mazāka par vai vienāda ar** \| _1_

Šeit ir iegūtā izvade.

| Krājuma numurs | Vietne | Fizisks krājums | Fiziski pieejams |
|---|---|---|---|
| IA0001 | 1 | 2 | 2 |

Ievērojiet, ka iestatījumi **Filtru** rūtī attiecas uz detalizēto (neapkopoto) krājumu tabulu, kas tiek parādīta šīs sadaļas sākumā. Tādējādi kritērijs **Pieejama fiziskā** \| **vērtība ir mazāka par vai vienāda ar** \| _1_ atrod divas rindas no šīs tabulas (pirmā un trešā rinda, no kurām katra rāda **Pieejamo fizisko** vērtību _1_). Tomēr šajā scenārijā **Rīcībā esošā saraksta** lapa nav iestatīta, lai rādītu **Noliktavas** dimensiju. Tāpēc tā apvieno divas sākotnējās rindas vienā iegūtajā rindā, jo abām rindām ir vienādas vērtības visās parādītajās dimensijās. Šī rinda tiek rādīta, lai pārkāptu filtrēšanas kritēriju, jo **Pieejamā fiziskā** vērtība tiek parādīta kā _2_. Tomēr rezultāts ir pareizs, jo iestatījumi **Filtru** rūtī attiecas uz avota tabulu, nevis uz apkopoto tabulu, kas tiek rādīta **Rīcībā esošā saraksta** lapā.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]