---
title: "Kreditora daļējas summas maksājumi"
description: "Reizēm jūs veicat kreditoram maksājumu, kas ir mazāks par rēķinā norādīto summu. Šajā rakstā ir aprakstītas dažādās opcijas, ko darīt šādās situācijās. Jums pieejamās opcijas ir atkarīgas no jūsu biznesa prasībām un konfigurācijas."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 4d243e6a9a68b69a6b32748344fc606ff3f2d965
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-payments-for-a-partial-amount"></a>Kreditora daļējas summas maksājumi

Reizēm jūs veicat kreditoram maksājumu, kas ir mazāks par rēķinā norādīto summu. Šajā rakstā ir aprakstītas dažādās opcijas, ko darīt šādās situācijās. Jums pieejamās opcijas ir atkarīgas no jūsu biznesa prasībām un konfigurācijas. 

<a name="cash-discount-amounts"></a>Termiņatlaides summas
---------------------

Varat piedāvāt kreditoram termiņatlaidi, ja rēķins tiek apmaksāts pirms apmaksas datuma. Piemēram, ja rēķins tiek apmaksāts 10 dienu laikā, jūs ievadiet rēķinu par summu 100,00, kurā norādīta 2 procentu termiņatlaide. Apmaksas termiņš ir 30 dienas. Ja maksājuma piedāvājums izmanto termiņatlaides kā kritēriju, atlasot rēķinu un priekšlikums darbojas tieši vai pirms termiņatlaides datumu, rēķinu atlasītajam maksājumu un maksājumu izveidojas 98,00. Termiņatlaides var ņemt arī vienreizējs maksājums, kas tika izveidots manuāli.

## <a name="partial-payments-with-cash-discounts"></a>Daļēji maksājumi ar termiņatlaidēm
Ja tiek veikts daļējs maksājums, var ieplānot veikt papildu daļēju maksājumu, lai pilnībā segtu rēķinu. Jāiestata termiņatlaides daļēju samaksu veikt * * aprēķināt termiņatlaides daļējiem maksājumiem * * iespēju **Jā** par **konts kreditoru parametrus** lapu. 

Piemēram, ja rēķins tiek apmaksāts 10 dienu laikā pēc tā izrakstīšanas, jums tiek piedāvāta 2 procentu termiņatlaide. Rēķins ir iegrāmatots par summu 100,00. Ja veicat maksājumu 49.00 10 dienu laikā, ievadiet 49.00 debeta maksājumu žurnālā. Kad iestatāt daļējs maksājums **nokārtot atvērtās darbības** lapu, **1.00** parādās **termiņatlaides summa jāņem** lauks. 

> [!NOTE] 
> Ja ievadāt daļēju maksājumu un atstāt pilna rēķina summa **apjoms, lai nokārtotu** jomā, **termiņatlaides summa jāņem** laukā tiek automātiski pārrēķināta, lai, veicot transakciju grāmatošanu.

## <a name="credit-notes-with-cash-discounts"></a>Kredīta notas ar temiņatlaidēm
Jūs varat atgriezt dažas rēķinā iekļautās preces un saņemt kredīta notu. Ja termiņatlaide ir piemērota sākotnējam rēķinam, varat atņemt atlaides vērtību un saņemt pareizās summas atmaksu. Ja * aprēķināt kredīta notām termiņatlaides * * opcija ir iestatīta uz **Jā** par **debitoru kreditoru parametrus** lapu, atlaides aprēķina automātiski kredīta notu. 

Piemēram, ja rēķins tiek apmaksāts 10 dienu laikā pēc tā izrakstīšanas, jums tiek piedāvāta 2 procentu termiņatlaide. Rēķins tiek iegrāmatots par summu 100,00. Ja preču atgriešana un saņemt kredīta notu, kredīta notu var ievadīt rēķina oriģinālu 100,00, kopā ar 2 procentu termiņatlaide, kas arī norādīts kredītrēķinam pilnā apmērā.  Skatot kredīta notas **norēķiniem par darījumiem** lapu, **98,00** parādās **apjoms, lai nokārtotu** jomā, un **-2.00** parādās **termiņatlaides summa** lauks. Atlaides summa tiek grāmatota uz termiņatlaides kontu.

## <a name="overpaymentunderpayment-amounts"></a>Pārmaksas/nepilnas samaksas summas
Ja vēl atlikusī nosedzamā summa ir ļoti neliela, varat veikt daļējo maksājumu. Piemēram, kreditora rēķins summa ir 1000,00, bet jūs veicat maksājumu par summu 999.90. Ja atlikusī summa ir mazāka par summu, kas norādīta pārmaksām vai nepilnām samaksām lapā **Kreditoru moduļa parametri**, starpība tiek automātiski grāmatota uz pārmaksas/nepilnas samaksas virsgrāmatas kontu.


