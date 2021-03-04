---
title: Maiņas kursa korekcijas
description: Šajā tēmā ir sniegta informācija par maiņas kursa korekciju juridiskām personām Igaunijā, Ungārijā, Čehijas Republikā, Latvijā, Lietuvā, Polijā un Krievijā.
author: ShylaThompson
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 272683
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: kfend
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 8ea7993312434a25805bd7d22ade2c7b772a5c1d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408273"
---
# <a name="exchange-rate-adjustments"></a>Maiņas kursa korekcijas

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par maiņas kursa korekciju juridiskām personām Igaunijā, Ungārijā, Čehijas Republikā, Latvijā, Lietuvā, Polijā un Krievijā.

Igaunija, Ungārija, Čehijas Republikā, Latvija, Lietuva, Polija un Krievijā maiņas kursa korekcijas funkcionalitāte ietver tālāk minētos paplašinājumus, kas ir saistīti ar debitoriem un kreditoriem.

-   Maiņas kursa korekciju grāmatojumus var atcelt kā sākotnējo korekciju labojumus (negatīvas summas).
-   Ja tiek grāmatotas secīgi nerealizētas korekcijas, neatkarīgi no tā, vai korekcijas pārstāv peļņu vai zaudējumus, tiks izmantots tas pats Virsgrāmatas grāmatošanas konts un darbības tips.
-   Aprēķinātais maiņas kursa ienākums vienmēr tiek grāmatots ienākumu kontos un aprēķinātie maiņas kursa zaudējumi vienmēr tiek grāmatoti zaudējumu kontos.

Juridiskās personas, kuru primārā adrese ir Čehijas Republikā, var izmantot speciālās maiņas kursa korekciju metodes. Šī metode tiek dēvēta par inkrementālo metodi. Ja šī metode ir iespējota, izmaiņas, ko ievieš attiecīgais līdzeklis, netiek lietota. Nerealizētā un realizētā peļņa vai zaudējumi tiek aprēķināti pret pēdējo izmantoto maiņas kursu. Koriģētā summa tiek izmantota sākotnējās summas vietā kā pamata aprēķins. Lai pārslēgtu uz inkrementālo maiņas kursa korekcijas metodi, lapas **Virsgrāmatas parametri** sadaļas **Ārvalstu valūtas pārvērtēšana** laukā **Aprēķina metode** atlasiet **Inkrementāli**. Tālāk sniegtajā piemērā ir parādīts, kā maiņas kursa korekcijas funkcionalitāte darbu Igaunijā, Ungārijā, Čehijas Republikā, Latvijā, Lietuvā, Polijā un Krievijā. Tālāk ir aprakstīts uzņēmējdarbības scenārijs, kas tiks izmantots šajā piemērā.

-   Rēķins ārvalstu valūtā tiek grāmatots 2012. gada 1. decembrī.
-   Maksājums ārvalstu valūtā tiek grāmatots 2013. gada 3. janvārī.
-   Tiek veikta segšana, lai maksājumu attiecinātu uz rēķinu.
-   Maiņas kursu korekcija tiek veikta 2012. gada 31. decembrī (metode: Standarta).
-   Maiņas kursu korekcija tiek veikta 2013. gada 1. janvārī (metode: Rēķina datums).

Tālāk ir parādīti šajā piemērā izmantotie maiņas kursi no Kanādas dolāriem (CAD) uz ASV dolāriem (USD).

-   2012. gada 1. decembris: 400,0000
-   2012. gada 31. decembris: 450,0000
-   2013. gada 3. janvāris: 420,0000

### <a name="invoice"></a>Rēķins

| Datums                             | Debets/kredīts | Summas               | Virsgrāmatas (VG) konts    | Darbības veids             | Grāmatošanas tips       | Kredītkarte | Labojums |
|----------------------------------|--------------|-----------------------|--------------------------------|------------------------------|--------------------|--------|------------|
| 1-Dec-12                         | Debetkarte        | 10 000 CAD/40 000 USD | debitoru parādi                             | Rēķins                      | Debitora bilance   |        |            |
| 1-Dec-12                         | Kredītkarte       | 10 000 CAD/40 000 USD | Korespondējošais                         | Rēķins                      | Virsgrāmatas žurnāls     | X      |

### <a name="payment"></a>Maksājums

| Datums                             | Debets/kredīts | Summas               | Virsgrāmatas (VG) konts    | Darbības veids             | Grāmatošanas tips       | Kredītkarte | Labojums |
|----------------------------------|--------------|-----------------------|--------------------------------|------------------------------|--------------------|--------|------------|
| 3-Jan-13                         | Debetkarte        | 10 000 CAD/42 000 USD | Korespondējošais                         | Maksājums                      | Virsgrāmatas žurnāls     |        |            |
| 3-Jan-13                         | Kredītkarte       | 10 000 CAD/42 000 USD | debitoru parādi                             | Maksājums                      | Debitora bilance   | X      |            |

### <a name="settlement"></a>Segšana

| Datums                             | Debets/kredīts | Summas               | Virsgrāmatas (VG) konts    | Darbības veids             | Grāmatošanas tips       | Kredītkarte | Labojums |
|----------------------------------|--------------|-----------------------|--------------------------------|------------------------------|--------------------|--------|------------|
|2013. gada 3. janvāris (maksājuma datums) | Debetkarte        | 0 CAD/2000 USD       | debitoru parādi                             | Debitors                     | Peļņa no maiņas kursa |        |            |
2013. gada 3. janvāris (maksājuma datums) | Kredītkarte       | 0 CAD/2000 USD       | Realizētā valūtas korekcijas peļņa   | Debitors                     | Peļņa no maiņas kursa | X      |            |


### <a name="revaluation--standard-method-date--december-31-2012"></a>Pārvērtēšana (standarta metode; datums = 2012. gada 31. decembris)
Saistībā ar šo pārvērtēšanu piemēru ievērojiet, ka 2013. gada 3. janvāra ieraksts tieši anulē 2012. gada 31. decembra ierakstu. Pat Virsgrāmatas kontus un grāmatošanas tipi ir vienādi. Turklāt ievērojiet, ka tika iestatīts karodziņš **Labojums**.

| Datums                             | Debets/kredīts | Summas               | Virsgrāmatas (VG) konts    | Darbības veids             | Grāmatošanas tips       | Kredītkarte | Labojums |
|----------------------------------|--------------|-----------------------|--------------------------------|------------------------------|--------------------|--------|------------|
| 31-Dec-12           | Debetkarte        | 0 CAD/5000 USD       | debitoru parādi                             | Ārvalstu valūtas pārvērtēšana | Peļņa no maiņas kursa |        |            |
| 31-Dec-12           | Kredītkarte       | 0 CAD/5000 USD       | Nerealizētā valūtas korekcijas peļņa | Ārvalstu valūtas pārvērtēšana | Peļņa no maiņas kursa | X      |            |
| 3-Jan-13            | Debetkarte        | 0 CAD/5000 USD       | debitoru parādi                             | Ārvalstu valūtas pārvērtēšana | Peļņa no maiņas kursa |        | X          |
 3-Jan-13            | Kredītkarte       | 0 CAD/5000 USD       | Nerealizētā valūtas korekcijas peļņa | Ārvalstu valūtas pārvērtēšana | Peļņa no maiņas kursa | X      | X          |


### <a name="revaluation-invoice-date-method-date--january-1-2013"></a>Pārvērtēšana (rēķina datuma metode, datums = 2013. gada 1. janvāris)
Saistībā ar šo pārvērtēšanu ievērojiet, ka 2013. gada 1. janvāra ieraksts tieši anulē 2013. gada 3. janvāra ierakstu. Pat Virsgrāmatas kontus un grāmatošanas tipi ir vienādi. Turklāt ievērojiet, ka tika iestatīts karodziņš **Labojums**.

| Datums   | Debets/kredīts | Summas | Virsgrāmatas (VG) konts| Darbības veids| Grāmatošanas tips| Kredītkarte | Labojums |
|--------|--------------|---------|----------------------------|----------------|--------|------------|--------------|
|1-Jan-13 | Debetkarte  | 0 CAD/5000 USD | debitoru parādi                             | Ārvalstu valūtas pārvērtēšana | Peļņa no maiņas kursa |   | X |
|1-Jan-13 | Kredītkarte | 0 CAD/5000 USD | Nerealizētā valūtas korekcijas peļņa | Ārvalstu valūtas pārvērtēšana | Peļņa no maiņas kursa | X | X |
|3-Jan-13 | Debetkarte  | 0 CAD/5000 USD | debitoru parādi                             | Ārvalstu valūtas pārvērtēšana | Peļņa no maiņas kursa |   |   |
|3-Jan-13 | Kredītkarte | 0 CAD/5000 USD | Nerealizētā valūtas korekcijas peļņa | Ārvalstu valūtas pārvērtēšana | Peļņa no maiņas kursa | X |   |

Sistēmas darbība ir vienāda neatkarīgi no tā, vai lapas **Virsgrāmatas parametri** sadaļas **Darbības anulēšana** opcija **Labojums** ir iestatīta uz **Jā** vai **Nē**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]