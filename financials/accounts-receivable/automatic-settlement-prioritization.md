---
title: "Automātisko nosegšanu un prioritāšu noteikšana"
description: "Šajā rakstā ir sniegta informācija par to, kā tiek segtas transakcijas, atlasot vienumu Automātiska nosegšana lapā Kreditoru parametri. Šeit ir arī izskaidrots, kā automātisko nosegšanu var izmantot kopā ar maksājuma prioritātes statusu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14531
ms.assetid: e7837cf6-ec69-44b4-8d47-eba38d5c7b1f
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: a751973b49febd6925267d00fb1d2c72114f86b0
ms.lasthandoff: 03/31/2017


---

# <a name="automatic-settlement-and-prioritization"></a>Automātisko nosegšanu un prioritāšu noteikšana

Šajā rakstā ir sniegta informācija par to, kā tiek segtas transakcijas, atlasot vienumu Automātiska nosegšana lapā Kreditoru parametri. Šeit ir arī izskaidrots, kā automātisko nosegšanu var izmantot kopā ar maksājuma prioritātes statusu.

Jums ir divas iespējas, apmaksājot maksājumus ar rēķiniem un citām transakcijām. Varat atlasīt manuāli nokārtot darījumu vai Microsoft Dynamics 365 darbībām var atlasīt darbības automātiski, izmantojot automātisko nosegšanu funkcionalitāti. Varat arī pielāgot automātiskās segšanas apstrādi, izmantojot opciju **Noteikt segšanai prioritāti**. Visas šīs iespējas ir daļa no nosegšanas parametrus, kas ir definētas **Accounts receivable parameters** lapā. Veida, kā transakcijas tiek automātiski nosegtas, var atšķirties atkarībā no metodes, ko izmantojat automātiskajai nosegšanai. Pieejamas šādas metodes.

-   Lietotāja definētas nosegšanas prioritātes
-   Automātiskā nosegšana pēc noklusējuma

Turpmākajās sadaļās ir aprakstīts, kā transakcijas tiek nosegtas katrai metodei.

## <a name="example-transactions"></a>Transakciju piemēri
Šī raksta turpinājumā sniegto segšanas piemēru pamatā ir tālāk norādītās transakcijas. Visas transakcijas ir klientam 2050.

| Transakcija   | Datums        | Summa | Nosacījumi atlaidei skaidrā naudā | Termiņatlaides datums | Komentāri                                                                                                                                                                                      |
|---------------|-------------|--------|---------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rēķins 1     | 15.augusts   | 100,00 | 2%14, neto 30        | 29.augusts          |                                                                                                                                                                                               |
| Rēķins 2     | 1.septembris | 250,00 | 2%14, neto 30        | 15.septembris       |                                                                                                                                                                                               |
| Rēķins 3     | 15.oktobris  | 500,00 | 2% 14/neto 30        | 29.oktobris         |                                                                                                                                                                                               |
| Procentu paziņojums | 15.oktobris  | 7,00   |                     |                    | Šo procentu paziņojums ir pavadzīmes 1. un 2. rēķina. Summa tiek aprēķināta kā 2 procenti procentu summām, kas ir 30 vai vairāk dienas kavēts. Piemēram, 0,02 × (100,00 + 250,00) = 7,00. |

## <a name="userdefined-settlement-priority"></a>Userdefined izšķiršanas prioritāte
Ja norādāt opcijas **Izmantot prioritāti automātiskai segšanai** iestatījumu **Jā** lapā **Debitoru parādu parametri**, tad, atlasot transakcijas automātiskai segšanai, tiek izmantota lapā **Norēķinu prioritāte** definētā segšanas prioritāte. Šajā piemērā ir definēta tālāk norādītā segšanas prioritāte.

1.  Darījuma veids
    -   Komisijas maksas
    -   Atgādinājuma vēstules
    -   Procentu paziņojumi
    -   Rēķini

2.  Transakcijas datums, dilstošā secībā
3.  Dokuments

Ja 25. oktobrī grāmatojat maksājumu ar summu 700,00, šis maksājums tiek segts ar transakcijām tālāk norādītajā secībā.

| Dokuments       | Datums       | Rēķins | Summa darījuma valūtā | Nosedzamā summa | Bilance | Valūta |
|---------------|------------|---------|--------------------------------|------------------|---------|----------|
| Procentu paziņojums | 15.10.2015. |         | 7,00                           | 7,00             | 0,00    | USD      |
| Rēķins 1     | 15.08.2015.  | 10001   | 100,00                         | 100,00           | 0,00    | USD      |
| Rēķins 2     | 01.09.2015.   | 10002   | 250,00                         | 250,00           | 0,00    | USD      |
| Rēķins 3     | 15.10.2015. |         | 500,00                         | 343,00           | 157,00  | USD      |

## <a name="default-automatic-settlement"></a>Automātiskā nosegšana pēc noklusējuma
Ja nav nevienas lietotāja definētas nosegšanas prioritātes, transakcijas tiek atlasītas automātiski nosegšanai, pamatojoties uz izpildes datumu. Nosegtajām transakcijām ir jābūt tādā pašā valūtā, kā tām transakcijām, kas tiek nosegtas kopā ar tām. Ja 25.oktobrī grāmatojat 700,00 maksājumu, šādas transakcijas tiek atzīmētas nosegšanai.

| Dokuments       | Datums       | Rēķins | Summa darījuma valūtā | Nosedzamā summa | Bilance | Valūta |
|---------------|------------|---------|--------------------------------|------------------|---------|----------|
| Rēķins 1     | 15.08.2015.  | 10001   | 100,00                         | 100,00           | 0,00    | USD      |
| Rēķins 2     | 01.09.2015.   | 10002   | 250,00                         | 250,00           | 0,00    | USD      |
| Rēķins 3     | 15.10.2015. |         | 500,00                         | 350,00           | 150,00  | USD      |
| Procentu paziņojums | 15.10.2015. |         | 7,00                           | 0,00             | 0,00    | USD      |




