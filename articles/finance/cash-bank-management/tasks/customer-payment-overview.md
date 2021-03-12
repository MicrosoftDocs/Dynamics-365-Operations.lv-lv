---
title: Debitoru maksājumu pārskats
description: Šis uzdevumu ceļvedis palīdzēs izprast dažādas metodes, kuras izmanto, lai ievadītu debitora maksājumus.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, CustPaymEntry, CustTableLookup, LedgerJournalTransCustPaym, CustOpenTrans, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 71e1657d738f691644b6d9cc4d34f812b853934e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978868"
---
# <a name="customer-payment-overview"></a>Debitoru maksājumu pārskats

[!include [banner](../../includes/banner.md)]

Šis uzdevumu ceļvedis palīdzēs izprast dažādas metodes, kuras izmanto, lai ievadītu debitora maksājumus. Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.

1. Pārejiet uz sadaļu **Navigācijas rūts > Moduļi > Debitori > Maksājumi > Maksājumu žurnāls**.
2. Klikšķiniet **Jauns**.
3. Atlasiet maksājumu žurnālu, kurā tiks saglabāti debitoru maksājumi.
4. Atlasiet žurnālu vai ievadiet to manuāli.
5. **Darbību rūtī** noklikšķiniet uz **Ievadīt debitora maksājumus**. Lauks Ievadīt debitora maksājumus tiek izmantots, lai vienā reizē ierakstītu vienu debitoru maksājumu. Informāciju par maksājumu ievadiet augšpusē un pēc tam atzīmējiet rēķinus, kas visi vienā lapā ar maksājumu tiek nomaksāti.  
6. Ievadiet debitoru, no kura saņēmāt maksājumu. Ja nezināt debitoru, bet zināt apmaksāto transakciju, lai ievadītu maksājumu, var izmantot lauku Transakcija. Ievadiet vai atlasiet rēķinu laukā Transakcija. Kad atlasīsiet transakciju, debitors automātiski parādīsies pēc noklusējuma.
7. Laukā **Maksājuma atsauce** ievadiet maksājuma atsauci. Maksājuma atsauce var būt debitora čeka numurs vai atsauce no klienta elektroniskā maksājuma. Maksājuma atsauce ir nepieciešama tikai tad, ja atzīmējat maksājumu iekļaušanai depozīta kvītī.  
8. Laukā **Depozīta kvīts** atlasiet, vai maksājums tiks iekļauts depozīta kvītī. 
9. Laukā **Summa** ievadiet debitora maksājuma summu. Maksājuma summa pēc noklusējuma neparādīsies. Tā jāievada manuāli. 
10. Atzīmējiet rēķinus, kurus apmaksāja debitors. Ja maksājums ir priekšapmaksa, jums nav nepieciešams atzīmēt rēķinus nosegšanai. Maksājumu joprojām var saglabāt un iegrāmatot. Rēķina segšana var notikt vēlāk.
11. Ievadiet maksājuma summu, kura jāsedz atzīmētajam rēķinam. Šo lauku var izmantot, kad maksājums ir daļējs maksājums. Ja neievadāt summu, nosedzamā summa tiks noteikta automātiski.
12. Noklikšķiniet uz **Saglabāt žurnālā**. Pirms saglabājat maksājumu žurnālā, pārliecinieties, vai ir definēts korespondējošais konts. Izmantojot funkciju **Saglabāt žurnālā**, maksājums tiks saglabāts un pārvietots uz žurnālu. Pēc tam var turpināt ievadīt nākamo maksājumu.
13. Aizvērt lapu.
14. **Darbību rūtī** noklikšķiniet uz Rindas. Atverot Rindas, ieraudzīsiet visus maksājumus, kas ierakstīti lapā **Ievadīt debitora maksājumus** un saglabāti žurnālā. Šo lapu var arī izmantot, lai ievadītu jaunos debitoru maksājumus vai rediģēt esošos debitora maksājumus pirms to grāmatošanas.
15. Noklikšķiniet uz **Jauns**, lai izveidotu citu maksājumu. 
16. Atlasiet debitoru, no kura saņēmāt maksājumu. Ja nezināt debitoru, bet zināt ar maksājumu apmaksāto rēķinu, izmantojiet lauku Rēķins, lai manuāli ievadītu vai atlasītu rēķinu. Debitors parādīsies pēc noklusējuma, kad tiks atlasīts rēķins.  
17. Noklikšķiniet **Transakciju nosegšana**, lai atzīmētu apmaksātos rēķinus. Jums nav nepieciešams segt rēķinu maksājumus. Ja tā ir priekšapmaksa vai ja nezināt, kāds rēķins tiek apmaksāts, varat ievadīt un iegrāmatot maksājumu. Ar maksājumu var nosegt rēķinu vēlāk.  
18. Atzīmējiet rēķinus, kas apmaksāti ar šo maksājumu. 
19. Laukā **Summa** ievadiet maksājuma summu, kura tiks segta šim rēķinam.
20. Noklikšķiniet uz **Labi**.
21. Laukā **Maksājuma atsauce** ievadiet maksājuma atsauci. Maksājuma atsauce ir nepieciešama tikai tad, ja atzīmējat maksājumu iekļaušanai depozīta kvītī.  
22. Lai grāmatotu starpuzņēmumu debitora rēķinu, sadaļā **Darbību rūts** noklikšķiniet uz **Grāmatot**, lai iegrāmatotu debitoru maksājumus. 

