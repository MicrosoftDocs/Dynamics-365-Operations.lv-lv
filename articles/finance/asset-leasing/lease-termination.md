---
title: Nomas izbeigšanas priekšlikums
description: Šajā tēmā izskaidrots, kā ierosināt nomas izbeigšanu.
author: moaamer
manager: Ann Beebe
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ff3795f26ab10ac19cc3a0dd00dca65095118f45
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207307"
---
# <a name="propose-a-lease-for-termination"></a>Nomas izbeigšanas ierosinājums

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Ja noma tiek izbeigta pirms termiņa, līdzekļu noma var reģistrēt žurnāla ierakstu par izbeigšanu, lai norakstītu nomas saistības, līdzekļa lietošanas tiesības (LLT) un uzkrāto nolietojumu, kā arī iegrāmatotu peļņu vai zaudējumus. Pirmstermiņa izbeigšanas process izbeidz nomu un ar to saistītās nomas grāmatas. Tas neizbeidz atsevišķas nomas grāmatas. Šajā tēmā aprakstīta funkcionalitāte, kas ļauj ierosināt nomas izbeigšanu un apstrādāt nomas izbeigšanas žurnāla ierakstu.

Ja noma netiek klasificēta kā atliktās nomas maksas noma un nav saistīta ar pamatlīdzekli, līdzekļu noma izveido šādu žurnāla ierakstu par izbeigšanu.

| Darbība                           | Debets (Dr.) | Kredīts (Kr.) |
|---------------------------------------|-------------|--------------|
| Dr. Nomas saistības                   | X           |              |
| Dr. Uzkrātais nolietojums.          | X           |              |
| Dr. Peļņa (zaudējumi) no nomas modifikācijas | X           |              |
| Kr. Nomas līdzeklis                       |             | X            |
| Kr. Peļņa (zaudējumi) no nomas modifikācijas |             | X            |

Ja nomas grāmata ir klasificēta kā atliktās nomas maksas grāmata, ieraksts noraksta atliktās nomas maksas bilanci pirms peļņas vai zaudējumu konta izbeigšanas, kā norādīts šeit.

| Darbība                           | Debets (Dr.) | Kredīts (Kr.) | 
|---------------------------------------|-------------|--------------|
| Dr. Atliktā nomas maksa                     | X           |              |
| Kr. Peļņa (zaudējumi) no nomas modifikācijas |             | X            |
| Kr. Atliktā nomas maksa                     |             | X            |
| Dr. Peļņa (zaudējumi) no nomas modifikācijas | X           |              |

Ja nomas grāmata ir saistīta ar pamatlīdzekli, LLT līdzeklis tiek ņemts vērā pamatlīdzekļos. Šādā uzskaitē ir iekļauta pirmstermiņa izbeigšanas uzskaite. Līdzekļu noma izveido šādu žurnāla ierakstu, lai norakstītu nomas saistības.

| Darbība                           | Debets (Dr.) | Kredīts (Kr.) |
|---------------------------------------|-------------|--------------|
| Dr. Nomas saistības                   | X           |              |
| Kr. Peļņa (zaudējumi) no nomas modifikācijas |             | X            |

Informāciju par pareizo veidu, kā atbrīvoties no LLT līdzekļa, skatiet sadaļā [Pamatlīdzekļu izslēgšana, atzīmējot tos kā brāķi](../fixed-assets/dispose-of-a-fixed-asset-as-scrap.md).

## <a name="propose-a-lease-for-termination"></a>Nomas izbeigšanas ierosinājums

1. Dodieties uz nomu, kura ir jāizbeidz, un pēc tam darbību rūtī atlasiet **Izbeigšanas priekšlikums**.

    > [!NOTE]
    > Poga **Izbeigšanas priekšlikums** nav pieejama, ja kādā grāmatā ir neiegrāmatoti žurnāla ieraksti. Pirms varat izbeigt nomu, jums ir jāiegrāmato vai jādzēš visi žurnāla ieraksti, kas ir izveidoti saistībā ar nomu.

2. Parādītajā dialoglodziņā iestatiet izbeigšanas žurnāla ieraksta laukus **Spēkā stāšanās datums** un **Iegrāmatošanas datums**.
3. Atlasiet **Izbeigšanas priekšlikums**, lai ierosinātu nomas izbeigšanu.
4. Atlasiet **Iegrāmatot nomas izbeigšanu**, lai automātiski iegrāmatotu nomas izbeigšanas žurnāla ierakstu.
5. Lapā **Nomas izbeigšana** atlasiet tās nomas ID, kuru ierosināt izbeigt, lai skatītu izbeigšanas rindas. Izbeigšanas rindas norāda LLT līdzekļa, nomas saistību, uzkrātā nolietojuma, atliktās nomas maksas (ja piemērojams) uzskaites vērtības un peļņu vai zaudējumus, kas jāatzīst, izbeidzot nomu.

Tagad noma ir gatava izbeigšanai. Nomas grāmatas lauka **Izbeigšanas statuss** vērtība tiek mainīta uz **Gatavs izbeigšanai**. Šajā brīdī vairs nevar iegrāmatot žurnāla ierakstus attiecībā uz nomu, kā arī koriģēt vai tos mazināt. 

## <a name="process-leases-that-are-ready-for-termination"></a>Izbeigšanai gatavo nomu apstrāde

Lai apstrādātu nomas, kas ir gatavas izbeigšanai un iegrāmatotu izbeigšanas žurnāla ierakstu, veiciet tālāk norādītās darbības.

1. Lapā **Nomas izbeigšana** atlasiet nomu, ko apstrādāt, un pēc tam atlasiet **Izbeigt**.
2. Parādītajā dialoglodziņā atlasiet **Labi**.

Sistēma iegrāmato izbeigšanas žurnāla ierakstu. Nomas grāmatas lauks **Nomas statuss** tiek iestatīts uz **Izbeigts** un **Izbeigšanas priekšlikuma statusa** lauks tiek iestatīts uz **Pabeigts**.

## <a name="reverse-a-lease-termination"></a>Nomas izbeigšanas anulēšana

Lai anulētu nomas izbeigšanas žurnāla ierakstu un atvērtu izbeigto nomu, veiciet tālāk norādītās darbības.

- Lapā **Nomas izbeigšana** atlasiet izbeigto nomu, lai to anulētu, un pēc tam atlasiet **Anulēt izbeigšanu**.

Sistēma anulē izbeigšanas žurnāla ierakstu. Nomas grāmatas lauks **Nomas statuss** tiek iestatīts uz **Atvērts**. Noma vairs nav redzama lapā **Nomas izbeigšana** un to var atkārtoti ierosināt izbeigt.

## <a name="example-of-a-lease-termination"></a>Nomas izbeigšanas piemērs

Šajā piemērā noma ir saistīta ar nespecializētu līdzekli, kas nepārsūta līdzekļa īpašumtiesības un nepiešķir nomniekam iespēju iegādāties līdzekli.

### <a name="setup"></a>Iestatīšana

Tabulās ir parādītas vērtības, kas ir iestatītas cilnēs **Vispārīgi** un **Maksājumu grafika rindas** šai nomai, kas tiek izmantota šajā piemērā.

**Cilne Vispārīgi**

| Lauks                      | Vērtība            |
|----------------------------|------------------|
| Līdzekļa patiesā vērtība    | 600,000          |
| Valūta                   | USD              |
| Sākotnējās tiešās izmaksas       | 1000            |
| Salīdzināmā aizņēmuma procentu likme | 7%               |
| Pievienošanas intervāls       | Reizi gadā         |
| Līdzekļa lietderīgās lietošanas laiks (mēnešos) | 600              |
| Gada maksājuma veids               | Parastais gada maksājums |
| Sākuma datums          | 1.1.2019.         |

**Cilne Maksājumu grafika rindas**

| Lauks             | Vērtība      |
|-------------------|------------|
| Sākuma datums        | 1.1.2019.   |
| Perioda intervāls   | Mēnesis    |
| Periodi           | 120        |
| Beigu datums          | 31.12.2028. |
| Maksājumu biežums | Reizi gadā   |
| Maksājuma summa    | 10,000     |

### <a name="steps-for-terminating-the-lease"></a>Nomas izbeigšanas darbības

1. Pēc nomas izveides, kā aprakstīts iepriekš šajā tēmā, dodieties uz nomas grāmatu un apstipriniet maksājumu grafiku. Pēc tam iegrāmatojiet sākotnējās atpazīšanas žurnāla ierakstu. Sākotnējais LLT līdzeklis ir 71 235,81 $ un nomas saistībām ir jābūt 70 235,81 $. Šajā piemērā noma tika klasificēta kā operatīvā noma saskaņā ar Uzskaites standartu kodifikācijas tēmu 842 (ASC 842).
2. Palaidiet žurnāla pakešuzdevuma apstrādi trīs reizes, lai simulētu trīs gadu paiešanu nomas maksājumiem, procentu izdevumiem un nolietojuma izdevumiem.
3. Kad esat pabeidzis visu trīs pakešuzdevumu izpildi, atgriezieties pie nomas grāmatas un atveriet saistību un līdzekļu darījumu tabulas, lai skatītu LLT līdzekļu un nomas saistību pašreizējo uzskaites vērtību. Pēc trīs gadiem, saistību vērtībai ir jābūt aptuveni -53 893,00 $ un līdzekļa vērtībai jābūt aptuveni 54 593,00 $.

    Pēc trīs gadiem uzņēmums un iznomātājs savstarpēji vienojas izbeigt nomu. Tādēļ jums tagad noma ir jāizbeidz.

4. Dodieties uz nomu, kura ir jāizbeidz, un pēc tam darbību rūtī atlasiet **Izbeigšanas priekšlikums**. 
5. Parādītā dialoglodziņa laukos **Spēkā stāšanās datums** un **Iegrāmatošanas datums** ievadiet **1.1.2021**.
6. Atlasiet **Izbeigšanas priekšlikums**, lai ierosinātu nomas izbeigšanu.

    Tiek parādīta lapa **Nomas izbeigšana** un noma, kas tiks izbeigta.

7. Lai skatītu izbeigšanas rindas, atlasiet tās nomas ID, kuru ierosināt izbeigt. Izbeigšanas rindas parāda nomas uzskaites vērtības. Tālāk esošajā tabulā ir parādīts, kādas vērtības paredzēts šim piemēram. 

    | Lauks                                                 | Vērtība      |
    |-------------------------------------------------------|------------|
    | Saistību uzskaites bilance darījuma valūtā | 53 892,89 $ |
    | Līdzekļa lietošanas tiesības darījuma valūtā            | 71 235,81 $ |
    | Uzkrātais nolietojums darījuma valūtā      | 16 642,92 $ |
    | Peļņa (zaudējumi) darījuma valūtā                   | -700,00 $   |

8. Lai iegrāmatotu izbeigšanas žurnāla ierakstu, atlasiet nomu lapā **Nomas izbeigšana** un pēc tam atlasiet **Izbeigt**.
9. Parādītajā dialoglodziņā atlasiet **Labi**.
10. Lai skatītu izveidoto un iegrāmatoto izbeigšanas žurnāla ierakstu, dodieties uz līdzekļa nomas žurnālu nomas grāmatā. Tālāk esošajā tabulā ir parādīts, kā šim ierakstam paredzēts izskatīties šajā piemērā.

    | Darbība                           | Debets (Dr.) | Kredīts (Kr.) |
    |---------------------------------------|-------------|--------------|
    | Dr. Nomas saistības                   | 53 892,89   |              |
    | Dr. Uzkrātais nolietojums.          | 16 642,92   |              |
    | Dr. Peļņa (zaudējumi) no nomas modifikācijas | 700,00      |              |
    | Kr. Nomas līdzeklis                       |             | 71 235,81    |

11. Lai skatītu izbeigšanas neto ietekmi, kur LLT līdzekļa un nomas saistību vērtība būs 0 (nulle), atveriet saistību un līdzekļu darījumu tabulu.

Tagad nomas statusam ir jābūt **Izbeigts**. Šai nomai netiks iegrāmatoti papildu žurnāla ieraksti, izņemot gadījumus, kad izbeigšana tiek anulēta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]