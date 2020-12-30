---
title: Līdzekļa lietošanas tiesību mazināšana
description: Šī tēma apraksta funkcionalitāti, kas reģistrē vērtības samazinājumu un koriģē uzskaites standartu kodifikācijas tēmas 842 (ASC 842) operatīvas nomas līdzekļu novecošanas grafiku.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7a017cdbcbfa01d4dba383f2b6b7c742e54014e4
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4445800"
---
# <a name="impair-right-of-use-assets"></a>Līdzekļa lietošanas tiesību mazināšana

[!include [banner](../includes/banner.md)]

Ja līdzekļa lietošanas tiesību uzskaites summa nav atgūstama, iespējams, ir jāpārbauda, vai līdzekļa tiesības ir samazinātas. Ja nosakāt, ka līdzekļa tiesības ir samazinātas, līdzekļu noma var reģistrēt vērtības samazinājumu un atbilstoši koriģēt nolietojuma plānu. Šī tēma apraksta funkcionalitāti, kas reģistrē vērtības samazinājumu un koriģē uzskaites standartu kodifikācijas tēmas 842 (ASC 842) operatīvas nomas nolietojuma plānu. To pašu metodi piemēro arī starptautisko finanšu pārskatu standarta (IFRS 16) nomām.

LLT līdzekļa atlikums tiks amortizēts atlikušajam periodu skaitam neatkarīgi no tā, vai noma tika klasificēta kā finanšu noma saskaņā ar IFRS 16 vai operatīvā noma saskaņā ar ASC 842.

## <a name="impair-an-rou-asset"></a>LLT līdzekļa tiesību samazinājums

1. Dodieties uz nomu ar vērtības samazinājumu un atlasiet **Grāmatas**.
2. Darbību rūtī atlasiet **Vērtības samazinājums**.
3. Parādītajā dialoglodziņā **Vērtības samazinājuma summa** ievadiet līdzekļu vērtības samazinājuma summu. Lai samazinātu LLT līdzekli, ievadiet pozitīvu vērtību.
4. Laukā **Darījuma datums** ievadiet datumu, kad ir jāgrāmato vērtības samazinājuma ieraksts.
5. Laukā **Atlikušie periodi** ievadiet atlikušo mēnešu skaitu, kam jāveic amortizācija.
6. Ieslēdziet parametru **Grāmatošana**, ja vēlaties, lai sistēma automātiski grāmatotu vērtības samazinājuma izdevumu žurnāla ierakstu. Ja šis parametrs tiek atstāts izslēgts, sistēma izveido ierakstu, bet to negrāmato. Tad ierakstu varat grāmatot no lapas **Līdzekļu nomas žurnāls**.
7. Iestatiet opciju **Priekšskatīt pirms grāmatošanas** uz **Jā**, lai skatītu piedāvāto ierakstu pirms tā izveides vai grāmatošanas.
8. Iestatiet opciju **Aizvērt grāmatu** uz **Jā**, lai aizvērtu nomas grāmatu. Šo darbību nevar atsaukt. Ierakstus nevar grāmatot slēgtām nomām, un slēgtās nomas nevar koriģēt.
9. Atlasiet **Labi**, lai izveidotu vai grāmatotu vērtības samazinājuma ierakstu.
10. Lai skatītu līdzekļu ar vērtības samazinājumu nolietojuma grafiku, atveriet attiecībās nomas grāmatas līdzekļu nolietojuma grafiku. Tagad līdzeklim tiks aprēķināts nolietojums pēc lineārā principa, salīdzinot ar mēnešu skaitu, ko ievadījāt laukā **Atlikušie periodi**.
11. Lai skatītu vērtības samazinājuma izdevumu žurnāla ierakstu, nomas ar vērtības samazinājumu darbību rūtī atlasiet **Līdzekļu nomāšanas žurnāls**. Sistēma izveido žurnāla ierakstu, kas debetē vērtības samazinājuma izdevumu grāmatošanas kontu un kreditē nomas līdzekļu grāmatošanas kontu.
12. Lai skatītu LLT līdzekļa jauno uzskaites vērtību, nomas grāmatas darbību rūtī atlasiet **Līdzekļu darījumi**.

## <a name="example-of-rou-asset-impairment"></a>LLT līdzekļu vērtības samazinājuma piemērs

Šajā piemērā noma ir nespecializēts līdzeklis, kas nepārsūta īpašumtiesības un nepiešķir nomniekam iespēju veikt pirkumu.

### <a name="setup"></a>Iestatīt

Tabulās ir parādītas vērtības, kas ir iestatītas cilnēs **Vispārīgi** un **Maksājumu grafika rindas** šai nomai, kas tiek izmantota šajā piemērā.

**Cilne Vispārīgi**

| Lauks                      | Vērtība            |
|----------------------------|------------------|
| Līdzekļa patiesā vērtība    | 600,000          |
| Salīdzināmā aizņēmuma procentu likme | 7%               |
| Pievienošanas intervāls       | Reizi gadā         |
| Līdzekļa lietderīgās lietošanas laiks (mēnešos) | 600              |
| Gada maksājuma veids               | Parastais gada maksājums |
| Sākuma datums          | 01.01.2019.       |

**Cilne Maksājumu grafika rindas**

| Lauks             | Vērtība      |
|-------------------|------------|
| Sākuma datums        | 1.1.2019.   |
| Perioda intervāls   | Mēnesis    |
| Periodi           | 120        |
| Beigu datums          | 31.12.2028. |
| Maksājumu biežums | Reizi gadā   |
| Maksājuma summa    | 10,000     |

### <a name="steps"></a>Soļi

1. Pēc nomas izveides, kā aprakstīts iepriekš šajā tēmā, dodieties uz nomas grāmatu un apstipriniet maksājumu grafiku. Pēc tam iegrāmatojiet sākotnējās atpazīšanas žurnāla ierakstu. Sākotnējam LLT aktīvam un nomas saistībām ir jābūt $ 70 235,81. Šajā piemērā noma tika klasificēta kā operatīvā noma saskaņā ar ASC 842.
2. Palaidiet partijas žurnāla apstrādi trīs reizes, lai simulētu trīs gadu paiešanu nomas maksājumiem, procentu izdevumiem un nolietojuma izdevumiem.
3. Kad esat pabeidzis visu trīs pakešuzdevumu izpildi, atgriezieties pie nomas grāmatas un atveriet saistību un līdzekļu darījumu tabulas, lai skatītu LLT un nomas saistītu pašreizējo uzskaites vērtību. Pēc trīs gadiem, saistību vērtībai ir jābūt aptuveni $ -53 893,00, un līdzekļa vērtībai jābūt aptuveni $ 53 893,00. 

    Pēc trīs gadiem uzņēmums veic vērtības samazināšanās testus un nosaka, ka LLT ir $ 35 000 vērtības samazinājums. Jums ir jāreģistrē šis vērtības samazinājums.
    
4. Dodieties uz nomas grāmatu un pēc tam darbību rūtī atlasiet **Vērtības samazinājums**.
5. Lapā **Vērtības samazinājuma parametrs** ievadiet tālāk norādīto informāciju.

    | Lauks                  | Vērtība    |
    |------------------------|----------|
    | Vērtības samazinājuma summa      | 35,000   |
    | Darījuma datums       | 1.1.2022. |
    | Atlikušie periodi      | 84       |
    | Amats                   | Jā      |
    | Priekšskatīt pirms grāmatošanas | Nr.       |
    | Slēgt grāmatu             | Nr.       |

6. Ir izveidots un grāmatots vērtības samazinājuma izdevumu žurnāla ieraksts. Lai to skatītu, dodieties uz līdzekļa nomas žurnālu nomas grāmatā. Ievērojiet, ka vērtības samazinājuma summa tika debetēta vērtības samazināšanās izdevumu grāmatošanas kontā, un LLT grāmatošanas konts tika kreditēts.
7. Lai skatītu vērtības samazinājuma tīro ietekmi, dodieties uz saistību un līdzekļu darījumu tabulām. Ievērojiet, ka vērtības samazināšanās izdevumi ir samazinājuši LLT, bet nomas saistības uzskaites summa nav mainījusies.

Vērtības samazinājumam ir viens cits efekts, kas jāņem vērā. Tā kā LLT summa tagad ir daudz mazāka par nomas saistībām, summai jābūt izlietotai citādi nekā pirms tam. Proti, līdzeklis tagad tiek nolietots lineārā veidā visu atlikušo nomas 84 mēnešu laikā, sākot no darījuma datuma.
