---
title: Noklusējuma finanšu dimensijas finanšu žurnālos
description: Šajā rakstā ir aprakstīti noteikumi, kas nosaka, kā finanšu dimensijas vērtības tiek iestatītas transakcijām, kas ievadītas, izmantojot finanšu žurnālus. Tajā ir iekļauta arī detalizēta informācija par scenārijiem, kuros tiek izmantotas fiksētas dimensijas.
author: kweekley
ms.date: 09/04/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransDaily, LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8d0fcf836e22207baae562801fb082d735df0f96
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907933"
---
# <a name="default-financial-dimensions-on-financial-journals"></a>Noklusējuma finanšu dimensijas finanšu žurnālos

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīti noteikumi, kas nosaka, kā finanšu dimensijas vērtības tiek iestatītas transakcijām, kas ievadītas, izmantojot finanšu žurnālus (bet ne izmantojot krājumu žurnālus vai projektu žurnālus). Tajā ir iekļauta arī detalizēta informācija par scenārijiem, kuros tiek izmantotas fiksētas dimensijas.

## <a name="symptom"></a>Simptoms

Finanšu dimensiju vērtības netiek iestatītas, kā paredzēts kontā vai korespondējošajā kontā finanšu žurnālā. Tālāk izklāstītie scenāriji ir divi piemēri.

Dokuments tiek ievadīts žurnālā kā virsgrāmatas žurnālā. Konts ir kreditora konts, un korespondējošais konts ir bankas konts. Kreditora finanšu dimensijas pēc noklusējuma tiek ievadītas kontā, bet bankas finanšu dimensijas pēc noklusējuma netiek ievadītas korespondējošajā kontā. Tā vietā dimensiju vērtības no konta pēc noklusējuma tiek ievadītas korespondējošajā kontā.

Debitoram ir piešķirtas noklusējuma finanšu dimensijas vērtības, un ieņēmumu galvenajam kontam ir piešķirta fiksēta dimensijas vērtība nodaļas finanšu dimensijai. Dokuments tiek ievadīts virsgrāmatas žurnālā.  Konts ir debitors, un korespondējošais konts ir virsgrāmatas konts, konkrēti ieņēmumu konts ar fiksēto dimensijas vērtību. Fiksētā dimensija nav iestatīta ieņēmumu galvenā konta korespondējošajā kontā. Tā vietā tas ir iestatīts uz nodaļas dimensijas vērtību no konta, kas tika ņemts no debitora.  Pēc dokumenta grāmatošanas fiksētās dimensijas vērtība tiek izmantota grāmatotajā uzskaites ierakstā, bet dokuments joprojām rāda debitora nodaļas vērtību ieņēmumu kontā. 

Kādi noteikumi tiek ievēroti finanšu dimensiju vērtībām, kas iestatītas dokumentiem žurnālā?

## <a name="resolution"></a>Novēršana

Tālāk norādītie noteikumi ir jāievēro, lai finanšu dimensijas vērtības ievadītu pēc noklusējuma dokumenta rindās finanšu žurnālos, piemēram, virsgrāmatas žurnālā vai kreditoru rēķinu žurnālā. 

1. **Žurnāla virsraksts**

   - Žurnāla virsraksta dimensijas pēc noklusējuma tiek ievadītas no žurnāla nosaukuma dimensijām.

2. **Žurnāla rindas konts**

   - Žurnāla rindas konta dimensijas pēc noklusējuma tiek ievadītas no žurnāla virsraksta dimensijām.
   - Ja kāda no finanšu dimensijām ir tukša, tās vērtības tiek pēc noklusējuma ievadītas no debitora, kreditora, bankas, pamatlīdzekļa, projekta vai virsgrāmatas dimensijām.

     - Ja konta tips ir **Virsgrāmata**, fiksēta dimensija virsgrāmatas kontā transakcijas ieraksta laikā tiek apstrādāta kā noklusējuma dimensija.
     - Ja konta tips ir **Debitors**, **Kreditors**, **Banka**, **Pamatlīdzekļi** vai **Projekts**, galveno kontu vēl nevar noteikt. Tāpēc fiksēta dimensija kontam nekad netiks ievadīta pēc noklusējuma.

3. **Žurnāla rindas korespondējošais konts**

 - Pirmkārt, žurnāla rindas korespondējošā konta dimensijas pēc noklusējuma tiek ievadītas no žurnāla rindas konta dimensijām.

 - Ja kāda no finanšu dimensijām ir tukša, nākamais noklusējuma ieraksts būs no noklusējuma dimensijām no tipa Debitors, Kreditors, Banka, Pamatlīdzekļi, Projekts vai Virsgrāmata.
   1. Ja korespondējošā konta tips ir **Virsgrāmata**, fiksēta dimensija virsgrāmatas kontā transakcijas ieraksta laikā tiek apstrādāta kā noklusējuma dimensija. Ja dimensijas vērtība pēc noklusējuma jau tika ievadīta no konta, galvenā konta noklusējuma vai fiksētās dimensijas vērtība neignorēs esošo vērtību.
   2. Ja korespondējošā konta tips ir **Debitors**, **Kreditors**, **Banka**, **Pamatlīdzekļi** vai **Projekts**, galvenais konts vēl nav zināms, tāpēc korespondējošajam kontam pēc noklusējuma nekad nebūs fiksētās dimensijas.

4. **Grāmatošana**

    1. Grāmatošanas laikā galvenais konts katrai uzskaites ieraksta rindai (gan kontam, gan korespondējošajam kontam) tiek novērtēts, lai noteiktu, vai pastāv fiksētas dimensijas vērtība. Ja ir definēta fiksēta dimensija, visas esošās vai tukšās vērtības tiek aizstātas ar šo fiksētās dimensijas vērtību.

        Fiksētās dimensijas vērtība žurnāla rindās pēc grāmatošanas **netiek** rādīta. Tā vietā tā tiek parādīta uzskaites ierakstā, kad skatāt dokumentu pēc tā grāmatošanas.

    2. Grāmatošanas laikā pēc noklusējuma netiek ievadītas citas dimensijas vērtības, ieskaitot papildu virsgrāmatas kontus, kurus var tikt pievienoti grāmatošanas laikā, piemēram, noapaļošanas kontus un starpuzņēmumu parādus vai parādus no kontiem. Noklusējuma dimensiju ieraksti papildu virsgrāmatas kontiem tiek ņemti no konta vai korespondējošajiem kontiem.

Lai pēc noklusējuma ievadītu dimensiju vērtības, žurnāla noklusējuma process nevar noteikt, vai tukša dimensijas vērtība tika ar nolūku atstāta tukša vai arī netika veikts noklusējuma ieraksts. Ja dimensijas vērtība ar nolūku atstāta tukša, vērtība joprojām var tikt ievadīta pēc noklusējuma, izmantojot iepriekš aprakstīto noklusējuma pasūtījumu. Ja nepieciešams, lai dimensijai būtu tukša vērtība, iespējams, jāizveido dimensija, kuras vērtība ir **0** (nulle) vai **Tukšs**, tā, lai to varētu izmantot tukšas dimensijas vietā.

Pārskatiet tālāk norādītos scenārijus, kuros sniegti finanšu dimensijas noklusējuma pasūtījuma piemēri.

### <a name="scenario-1"></a>1. scenārijs

Dodieties uz **Virsgrāmata \> Žurnāla izveidošana \> Žurnālu nosaukumi** un atlasiet žurnāla nosaukumu **GenJrn**. Pēc tam kopsavilkuma cilnē **Finanšu dimensijas** definējiet šādas noklusējuma finanšu dimensiju vērtības:

- **BUSINESSUNIT:** 001
- **DEPARTMENT:** 024

[![Žurnālu nosaukumu lapa](./media/financial-dimension-defaulting-jrnl-names-01.png)](./media/financial-dimension-defaulting-jrnl-names-01.png)

Dodieties uz **Virsgrāmata \> Žurnāla ieraksti \> Virsgrāmatas žurnāls** un izveidojiet jaunu virsgrāmatas žurnālu, kurā tiek izmantots žurnāla nosaukums **GenJrn**. Dimensijas pēc noklusējuma tiek ievadītas no žurnāla nosaukuma (tabulas LedgerJournalName) līdz žurnāla virsrakstam (tabulai LedgerJournalTable), kā norādīts cilnē **Finanšu dimensijas**.

[![Cilne Finanšu dimensijas lapā Virsgrāmatas žurnāli](./media/financial-dimension-defaulting-genrl-jrnl-02.png)](./media/financial-dimension-defaulting-genrl-jrnl-02.png)

Dodieties uz **Rindas**. Laukā **Konta tips** atlasiet **Virsgrāmata** un pēc tam laukā **Konts** ievadiet **170150**. Pēc tam atlasiet **tabulēšanas** taustiņu, lai pārvietotos ārpus lauka. Dimensijas pēc noklusējuma tiek ievadītas no žurnāla virsraksta. Tāpēc vērtība **Konts** tiek rādīta kā **170150-001-024**.

[![Žurnāla rindas virsgrāmatas žurnālam lapā Žurnāla dokuments](./media/financial-dimension-defaulting-jrnl-vchr-03.png)](./media/financial-dimension-defaulting-jrnl-vchr-03.png)

Mainiet vērtību **Konts** uz **170150-001-023**. Ievadiet debeta summu vai kredīta summu. Laukā **Korespondējošā konta tips** atlasiet **Virsgrāmata** un pēc tam laukā **Korespondējošais konts** ievadiet **600150**. Dimensiju vērtības pēc noklusējuma tiek ievadītas no konta. Tāpēc vērtība **Korespondējošais konts** tiek rādīta kā **600150-001-023**.

### <a name="scenario-2"></a>2. scenārijs

Izmantojiet tās pašas finanšu dimensijas, kas 1. scenārijā definētas žurnāla nosaukumam. Pēc tam dodieties uz **Debitori \> Debitori \> Visi debitori** un definējiet noklusējuma finanšu dimensiju vērtības debitoram US-001. Atlasiet debitoru, lai atvērtu detalizēto informāciju par debitoru. Cilnē **Finanšu dimensijas** saglabājiet noklusējuma vērtību dimensijai **BUSINESSUNIT** (**001**). Pievienojiet dimensiju **COSTCENTER** un ievadiet kā vērtību **007**.

Izveidojiet jaunu virsgrāmatas žurnālu, kas izmanto žurnāla nosaukumu **GenJrn**. Cilnē **Finanšu dimensijas** mainiet noklusējuma **BUSINESSUNIT** vērtību no **001** uz **002**.

Dodieties uz **Rindas**. Laukā **Konta tips** atlasiet **Debitors** un pēc tam laukā **Konts** ievadiet **US-001**. Lai skatītu finanšu dimensijas kontu tipiem, kas nav virsgrāmatas kontu tipi, atlasiet **Finanšu dimensijas \> Konts**. Tiek ievadīti šādi noklusējuma ieraksti finanšu dimensiju vērtībām:

- **BUSINESSUNIT:** 002 — noklusējuma ieraksts tiek ņemts no žurnāla virsraksta. Vērtība **001** netiek ievadīta pēc noklusējuma no debitora US-001, jo noklusējuma vērtība jau tika ievadīta.
- **COSTCENTER:** 007 — noklusējuma ieraksts tiek ņemts no debitora US-001 iestatījumiem.
- **DEPARTMENT:** 024 — noklusējuma ieraksts tiek ņemts no žurnāla virsraksta.

Atpakaļ rindā laukā **Korespondējošā konta tips** atlasiet **Virsgrāmata** un pēc tam laukā **Korespondējošais konts** ievadiet **600150**. Rindā tiek ievadītas šādas noklusējuma finanšu dimensiju vērtības:

- **BUSINESSUNIT:** 002 — noklusējuma ieraksts tiek ņemts no konta finanšu dimensijām. (Sākotnēji tas pēc noklusējuma tika ievadīts no žurnāla virsraksta.)
- **DEPARTMENT:** 024 — noklusējuma ieraksts tiek ņemts no konta finanšu dimensijām. (Sākotnēji tas pēc noklusējuma tika ievadīts no žurnāla virsraksta.)
- **COSTCENTER:** 007 — noklusējuma ieraksts tiek ņemts no konta finanšu dimensijām. (Sākotnēji tas pēc noklusējuma tika ievadīts no debitora.)

### <a name="scenario-3"></a>3. scenārijs

Tajā pašā žurnālā, kuru izmantojāt 2. scenārijam, pievienojiet jaunu rindu. Laukā **Konta tips** atlasiet **Virsgrāmata** un pēc tam laukā **Konts** ievadiet **170150**. Notīriet noklusējuma dimensiju vērtības tā, lai paliek tikai galvenais konts 170150. Laukā **Korespondējošā konta tips** atlasiet **Debitors** un pēc tam laukā **Korespondējošais konts** ievadiet **US-001**. Tiek ievadīti šādi noklusējuma ieraksti finanšu dimensiju vērtībām:

- **BUSINESSUNIT:** 002 — noklusējuma ieraksts tiek ņemts no žurnāla virsraksta, jo konta dimensijas vērtība ir tukša. Vērtība **001** netiek ievadīta pēc noklusējuma no debitora US-001, jo noklusējuma vērtība jau tika ņemta no žurnāla virsraksta. Ja **BUSINESSUNIT** vērtība ar nolūku atstāta tukša, jums jānoņem arī finanšu dimensija korespondējošajā kontā.
- **COSTCENTER:** 007 — noklusējuma ieraksts tiek ņemts no debitora US-001, jo konta dimensijas vērtība un žurnāla virsraksta dimensijas vērtība ir tukšas. Ja **COSTCENTER** vērtība ar nolūku atstāta tukša, jums jānoņem arī finanšu dimensija korespondējošajā kontā.
- **DEPARTMENT:** 024 — noklusējuma ieraksts tiek ņemts no žurnāla virsraksta, jo konta dimensijas vērtība ir tukša. Ja **DEPARTMENT** vērtība ar nolūku atstāta tukša, jums jānoņem arī finanšu dimensija korespondējošajā kontā.

### <a name="scenario-4"></a>4. scenārijs

Izmantojiet tās pašas noklusējuma finanšu dimensiju vērtības, kas tika definētas žurnāla nosaukumam un debitoram 1. un 2. scenārijā. Pēc tam definējiet fiksētu dimensijas vērtību dimensijai **BUSINESSUNIT** galvenajā kontā 170150. Dodieties uz **Virsgrāmata \> Kontu plāns \> Konti \> Galvenie konti**. Laukā **Galvenais konts** atlasiet **170150** un pēc tam cilnē **Juridiskas personas prioritātes** atlasiet **Pievienot**. Atlasiet **USMF** kā juridisko personu un pēc tam atlasiet **Pievienot**. Atlasiet šo ierakstu un pēc tam atlasiet **Noklusējuma dimensijas**. Mainiet dimensiju **BUSINESSUNIT** uz **Fiksēta vērtība** un kā vērtību ievadiet **003**.

Izveidojiet jaunu virsgrāmatas žurnālu, kas izmanto žurnāla nosaukumu **GenJrn**. Cilnē **Finanšu dimensijas** noņemiet visas noklusējuma dimensiju vērtības.

Dodieties uz **Rindas**. Laukā **Konta tips** atlasiet **Virsgrāmata** un pēc tam laukā **Konts** ievadiet **170150**. Pēc tam atlasiet **tabulēšanas** taustiņu, lai pārvietotos ārpus lauka. Dimensiju vērtības pēc noklusējuma tiek ievadītas no galvenā konta iestatījumiem kontam 170150. Tāpēc vērtība **Konts** tiek rādīta kā **170150-003-**.

Mainiet vērtību **Konts** uz **170150-004-**. **Žurnāla funkcionalitāte neliedz mainīt fiksētas dimensijas vērtību.** Ievadiet debeta summu vai kredīta summu. Laukā **Korespondējošā konta tips** atlasiet **Virsgrāmata** un pēc tam laukā **Korespondējošais konts** ievadiet **170250**. Finanšu dimensijas vērtība 004 tiek ievadīta kā noklusējums no konta. Pēc tam grāmatojiet dokumentu. Žurnālā atlasiet **Dokuments**. Grāmatošanas laikā ņemiet vērā, ka **BUSINESSUNIT** vērtība tika atgriezta uz fiksēto dimensijas vērtību **003**.

Atgriežot pie dokumenta žurnālā, dimensija **BUSINESSUNIT** **neatspoguļo** fiksēto dimensijas vērtību. Tai vienmēr ir vērtība, kas pirms grāmatošanas tiek parādīta ekrānā. Grāmatošanas process nemaina neko, kas ir ievadīts dokumentā. Grāmatošanas laikā tiek mainīts tikai uzskaites ieraksts.

## <a name="developer-notes"></a>Izstrādātāja piezīmes

Ja esat izstrādātājs un vēlaties apskatīt noklusējuma procesa kodu, pārskatiet šādas metodes:

- **LedgerJournalEngine.accountModified()**  — šī metode ir galvenais ievades punkts primārā konta dimensijas noklusējuma procesam, kas ir standarts visiem žurnāliem (un to ignorē daži žurnālu tipi).
- **LedgerJournalEngine.offsetAccountModified()**  — šī metode ir galvenais korespondējošā konta dimensiju noklusējuma procesa ievades punkts.
