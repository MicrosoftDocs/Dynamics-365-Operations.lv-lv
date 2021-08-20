---
title: Maksājuma kvīts formāta iestatīšana projekta rēķiniem
description: Uzņēmumi parasti pievieno rēķiniem izdrukātas maksājuma kvītis, lai palīdzētu debitoriem un sniegtu maksājuma atsauci grāmatošanas un norēķinu nolūkiem.
author: EvgenyPopovMBS
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OMLegalEntity, CustFormletterParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb0d1d95013b3eac3131064992920da5fa9bea5a1f6d554e6be1d5006a9b21fb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732904"
---
# <a name="set-up-payment-slip-format-for-project-invoices"></a>Maksājuma kvīts formāta iestatīšana projekta rēķiniem

[!include [banner](../../includes/banner.md)]

Uzņēmumi parasti pievieno rēķiniem izdrukātas maksājuma kvītis, lai palīdzētu debitoriem un sniegtu maksājuma atsauci grāmatošanas un norēķinu nolūkiem. Maksājuma kvīts papildus pārdošanas rēķiniem vai brīva teksta rēķiniem var izmantot projektu vai pakalpojumu rēķiniem, atgādinājuma vēstulēm, procentu paziņojumiem un konta pārskatiem. Lai apstrādātu maksājuma kvītis, vispirms jāiestata kreditora identifikācijas numurs un maksājuma kvīts pielikuma formāti.

Procedūrā tiek izmantoti demonstrācijas uzņēmuma “DEMF” dati. 

Šī funkcionalitāte ir pieejama juridiskām personām, kuru primārā adrese ir Dānijā.


## <a name="set-up-a-creditor-id-number"></a>Kreditora ID numura iestatīšana
1. Pārejiet uz sadaļu Organizācijas administrēšana > Organizācijas > Juridiskās personas.
2. Izvērsiet vai sakļaujiet sadaļu Bankas konta informācija.
3. Noklikšķiniet uz Rediģēt.
4. Laukā FI kreditora ID ierakstiet vērtību.
5. Noklikšķiniet uz Saglabāt.
6. Aizvērt lapu.

## <a name="set-up-a-payment-slip-format-for-invoices-notes-letters-and-statements"></a>Maksājuma kvīts formāta iestatīšana rēķiniem, pavadzīmēm, vēstulēm un pārskatiem
1. Pārejiet uz sadaļu Debitori > Iestatījumi > Veidlapas > Veidlapu iestatīšana.
2. Noklikšķiniet uz cilnes Rēķins.
3. Laukā Saistīt maksājumu pielikumu debitora rēķinam atlasiet opciju.
    * Nav — nedrukāt maksājuma kvīti. Izvēlieties šo opciju, ja maksājuma summa ir valūtā, kas nav dāņu krona (DKK).   FIK 751 — drukāt FIK 751 maksājuma kvīti, ja maksājuma summu un izpildes datumu plānojat maksājuma kvītī ierakstīt manuāli.   FIK 752 — drukājiet FIK 752 maksājuma kvīti, ja plānojat izmantot datora ģenerētu maksājuma kvīti, kurā jau iepriekš tika ierakstīta maksājuma summa un izpildes datums.  
4. Noklikšķiniet uz Saglabāt.
5. Noklikšķiniet uz cilnes Brīva teksta rēķins.
6. Laukā Saistītā maksājuma pielikums brīvā teksta rēķinam atlasiet opciju.
    * Nav — nedrukāt maksājuma kvīti. Izvēlieties šo opciju, ja maksājuma summa ir valūtā, kas nav dāņu krona (DKK).   FIK 751 — drukājiet FIK 751 maksājuma kvīti, ja plānojat manuāli ierakstīt maksājuma summu un izpildes datumu maksājuma kvītī.   FIK 752 — drukājiet FIK 752 maksājuma kvīti, ja plānojat izmantot datora ģenerētu maksājuma kvīti, kurā jau iepriekš tika ierakstīta maksājuma summa un izpildes datums.  
7. Noklikšķiniet uz Saglabāt.
8. Noklikšķiniet uz cilnes Procentu paziņojums.
9. Laukā Saistīt maksājuma pielikumu procentu paziņojumam atlasiet opciju.
    * Nav — nedrukāt maksājuma kvīti. Izvēlieties šo opciju, ja maksājuma summa ir valūtā, kas nav dāņu krona (DKK).   FIK 751 — drukājiet FIK 751 maksājuma kvīti, ja plānojat manuāli ierakstīt maksājuma summu un izpildes datumu maksājuma kvītī.   FIK 752 — drukājiet FIK 752 maksājuma kvīti, ja plānojat izmantot datora ģenerētu maksājuma kvīti, kurā jau iepriekš tika ierakstīta maksājuma summa un izpildes datums.  
10. Noklikšķiniet uz Saglabāt.
11. Noklikšķiniet uz cilnes Atgādinājuma vēstule.
12. Laukā Saistīt maksājuma pielikumu ar atgādinājuma vēstuli atlasiet opciju.
    * Nav — nedrukāt maksājuma kvīti. Izvēlieties šo opciju, ja maksājuma summa ir valūtā, kas nav dāņu krona (DKK).   FIK 751 — drukājiet FIK 751 maksājuma kvīti, ja plānojat manuāli ierakstīt maksājuma summu un izpildes datumu maksājuma kvītī.   FIK 752 — drukājiet FIK 752 maksājuma kvīti, ja plānojat izmantot datora ģenerētu maksājuma kvīti, kurā jau iepriekš tika ierakstīta maksājuma summa un izpildes datums.  
13. Noklikšķiniet uz Saglabāt.
14. Noklikšķiniet uz cilnes Konta pārskats.
15. Laukā Starpkonta izrakstam pievienotais saistītais maksājums atlasiet opciju.
    * Nav — nedrukāt maksājuma kvīti. Izvēlieties šo opciju, ja maksājuma summa ir valūtā, kas nav dāņu krona (DKK).   FIK 751 — drukājiet FIK 751 maksājuma kvīti, ja plānojat manuāli ierakstīt maksājuma summu un izpildes datumu maksājuma kvītī.   FIK 752 — drukājiet FIK 752 maksājuma kvīti, ja plānojat izmantot datora ģenerētu maksājuma kvīti, kurā jau iepriekš tika ierakstīta maksājuma summa un izpildes datums.  
16. Noklikšķiniet uz Saglabāt.
17. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]