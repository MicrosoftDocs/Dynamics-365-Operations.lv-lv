---
title: Automātisko darījumu konti
description: Šajā tēmā skaidrots, kā kontus automātiskajām darbībām izmanto grāmatošanai Microsoft Dynamics ar 365. gadu, un sniedz galveno kontu piemērus automātiskajām darbībām.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cecbeb769235e525390cc7a66800a9b0d55d78a9
ms.sourcegitcommit: 5bfd6511d710deb539b4030eb0e9c48d25513595
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/19/2022
ms.locfileid: "8014109"
---
# <a name="accounts-for-automatic-transactions"></a>Automātisko darījumu konti

Automātisko darbību kontu lapa (Virsgrāmatas automātisko darbību grāmatošanas iestatījumu konti) tiek izmantota, lai definētu noklusēto galveno kontu, ko izmanto katram grāmatošanas **tipam** **&gt;&gt;** sistēmā. Lai gan lielāko daļu grāmatošanas tipu var konfigurēt moduļa raksturīgajā vai funkcionalitātes lapā, dažus grāmatošanas tipus var konfigurēt tikai lapā Automātisko **darbību** konti.

Piemēram, var norādīt galveno kontu, kas tiek izmantots Klienta bilances grāmatošanas tipam lauku Kopsavilkums lapā Debitora grāmatošanas metode, un izmantot atšķirīgu galveno kontu **katram** debitora **·** **profilam**. Šādā veidā ir granulētāka grāmatojumu kontrole. No otras puses, jūs varat norādīt kļūdu kontu tikai automātisko **darbību konta** lapā.

Atverot lapu **Konti automātiskajām darbībām** jaunā juridiskajā persona, kontu saraksts būs tukšs. Varat pievienot visbiežāk lietotos grāmatošanas tipus, kas jākonfigurē lapā, atlasot pogu **Izveidot noklusētos** tipus. Pēc tam katrai rindai varat atlasīt galveno kontu **laukā Galvenais** konts. Ja grāmatošanas tipam atstājat tukšu galvenā konta lauku un neesat konfigurējis galveno kontu modulim raksturīgā vai raksturīgajā lapā, grāmatojot darbību, kas izmanto grāmatošanas tipu, saņemsit kļūdas **ziņojumu**. Parasti ziņojums būs "Grāmatošanas tipa \[konts nav \] atrodams".

## <a name="default-posting-types"></a>Noklusējuma grāmatošanas tipi

Tālāk sniegtajā tabulā sniegti noklusējuma grāmatošanas tipu piemēri, kas izveidoti, kad lapā Automātisko darbību konti atlasāt **Izveidot** **noklusētos** tipus. Tajā ir norādīti galveno kontu paraugs un apraksti. "Debets/kredīts?" Kolonna norāda, vai darbība parasti grāmato debetu vai kredītu. Dažos gadījumos darbība var grāmatot debetu vai kredītu. Kolonna Tīrīšanas konts norāda, vai grāmatošanas tips ir tīrīšanas konts. Ja grāmatošanas tips ir tīrīšanas konts, tad kontā grāmatotā summa tiek automātiski apgriezta, grāmatojot vēlāku darbību.

| Grāmatošanas tips | Galvenā konta piemērs | Galvenā konta nosaukuma piemērs | Konta veids | Vai debets/kredīts? | Dzēšanas konts | Apraksts |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Sīknaudas starpība pārskata valūtā | 618160 | Dažādi izdevumi | Izdevumi | Abi | Nē | Šis grāmatošanas tips tiek izmantots, kad sīknaudas starpība rodas, kad darbības summa ārzemju valūtā tiek tulkota pārskata valūtā. |
| Sīknaudas starpība uzskaites valūtā | 618160 | Dažādi izdevumi | Izdevumi | Abi | Nē | Šis grāmatošanas tips tiek izmantots, ja sīknaudas starpība rodas, kad darbības summa ārzemju valūtā tiek tulkota uzskaites valūtā. |
| Kļūdu konts | 999999 | Kļūdu konts | Izdevumi | Abi | Nē | Šis grāmatošanas tips tiek izmantots, ja sistēmā rodas kļūda. Konts ir jāpārbauda katru periodu, un visas kļūdas ir jāatrisina. |
| Rezultāts gada beigās | 300160 | Nesadalītā peļņa | Kapitāls | Abi | Nē | Šis grāmatošanas tips tiek lietots, kad tiek palaists gada beigu slēgšanas process, lai pārvietotu peļņas un zaudējumu tipa kontu bilanci uz galveno kontu, kas atlasīts gada **beigu** rezultātam. |
| Debitora termiņatlaide | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nē | Netiek izmantots grāmatošanas tips, **kas ir definēts lapu Automātisko darbību** konti. Galvenais konts ir nepieciešams, ja termiņatlaides ir konfigurētas debitoru parādos.|
| Kreditora termiņatlaide | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nav attiecināms | Nē | Netiek izmantots grāmatošanas tips, **kas ir definēts lapu Automātisko darbību** konti. Galvenais konts ir nepieciešams, ja termiņatlaides ir konfigurētas pie Kreditoriem. |

## <a name="additional-posting-types"></a>Papildu grāmatošanas tipi

Tabulā parādīti papildu grāmatošanas tipu piemēri, kas jākonfigurē, ja plānojat izmantot saistītās funkcijas. Šiem grāmatošanas tipiem grāmatošanas metodes konfigurācija nav pieejama citā modulī. "Debets/kredīts?" Kolonna norāda, vai darbība parasti grāmato debetu vai kredītu. Dažos gadījumos darbība var grāmatot debetu vai kredītu. Kolonna Tīrīšanas konts norāda, vai grāmatošanas tips ir tīrīšanas konts. Ja grāmatošanas tips ir tīrīšanas konts, tad kontā grāmatotā summa tiek automātiski apgriezta, grāmatojot vēlāku darbību.

| Grāmatošanas tips | Galvenā konta piemērs | Galvenā konta nosaukuma piemērs | Konta veids | Vai debets/kredīts? | Dzēšanas konts | Apraksts |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Bilances konts konsolidācijas starpībai | 801200 | Peļņa un zaudējumi — pārvērtēšana | Izdevumi | Abi | Nē | Šis grāmatošanas tips tiek lietots, veicot konsolidāciju, kas ietver valūtas pārvērtēšanu, un sīknaudas starpības rodas pārvērtēšanas laikā. |
| Peļņas un zaudējumu konts konsolidācijas starpībai | 801200 | Peļņa un zaudējumi — pārvērtēšana | Izdevumi | Abi | Nē | Šis grāmatošanas tips tiek lietots, veicot konsolidāciju, kas ietver valūtas pārvērtēšanu, un sīknaudas starpības rodas pārvērtēšanas laikā. |
| Starpvienumu uzskaite - debets | 133500 | Starpvienumu debitori | Līdzeklis | Debetkarte | Nē | Šis grāmatošanas tips tiek izmantots, atlasot līdzsvarošanas dimensiju Virsgrāmatas lapā un dimensija nelīdzsvaro **darbību**, kas tiek grāmatota. |
| Starpvienumu uzskaite - kredīts | 233500 | Starpvienumu kreditors | Saistības | Kredītkarte | Nē | Šis grāmatošanas tips tiek izmantots, atlasot līdzsvarošanas dimensiju Virsgrāmatas lapā un dimensija nelīdzsvaro **darbību**, kas tiek grāmatota. |
