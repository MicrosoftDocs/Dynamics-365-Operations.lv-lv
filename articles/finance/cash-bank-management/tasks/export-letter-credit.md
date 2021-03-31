---
title: Kredītvēstules eksportēšana
description: Šajā procedūrā ir aprakstīts kredītvēstules eksportēšanas process.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 127f38e7db0a8c0703fd95274f45ff4ca49c131e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225445"
---
# <a name="export-letter-of-credit"></a>Kredītvēstules eksportēšana

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir aprakstīts kredītvēstules eksportēšanas process.

Kredītvēstule ir līgums, ko izsniedz banka un kurā banka piekrīt veikt maksājumu pircēja vārdā, ja tiek izpildīti starp pircēju un pārdevēju noslēgtā līguma nosacījumi.



Pirms šīs procedūras izpildiet procedūru Bankas iestāžu iestatīšana un metožu grāmatošana un Kredītvēstule_Bankas iestādes līguma izveide. Lai sekmīgi izpildītu šo procedūru, jāatlasa demonstrācijas uzņēmums “USMF”.




## <a name="create-sales-order-for-export-letter-of-credit"></a>Pārdošanas pasūtījuma izveide kredītvēstules eksportēšanai
1. Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Debitora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Izvērsiet vai sakļaujiet sadaļu Vispārīgi.
7. Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Atlasiet vietu, kur krājums ir jāuzkrāj.  
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Atlasiet noliktavu, kur izsniedzamais krājums ir jāuzkrāj.  
10. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Ņemiet vērā! Jābūt atlasītam laukam Bankas dokumenta tips un vērtībai Kredītvēstule.  
11. Laukā Bankas dokumenta veids atlasiet Kredītvēstule.
12. Izvērsiet vai sakļaujiet sadaļu Piegāde.
    * Atlasiet Piegādes datuma kontrole = Nav.  
13. Laukā Pieprasītais saņemšanas datums ievadiet datumu.
14. Noklikšķiniet uz OK.
15. Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Atlasiet vajadzīgo krājumu, jas ir jāizdod/jāpārdod.  
16. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
17. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
18. Laukā Vienības cena ievadiet kādu skaitli.
19. Izvērsiet vai sakļaujiet sadaļu Detalizēta rindas informācija.
20. Noklikšķiniet uz cilnes Piegāde.
21. Laukā Pieprasītais nosūtīšanas datums ievadiet datumu.
22. Laukā Apstiprinātais nosūtīšanas datums ievadiet datumu.
23. Darbību rūtī noklikšķiniet uz Pārvaldīt.
24. Noklikšķiniet uz Kredītvēstule.
25. Laukā Bankas dokumenta numurs ierakstiet vērtību.
26. Laukā Beigu datums ievadiet datumu un laiku.
27. Izvērsiet vai sakļaujiet sadaļu Detalizēta informācija par banku.
28. Laukā Izdevēja banka noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.
29. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
30. Laukā Konsultatīvā banka noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.
31. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
32. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
33. Noklikšķiniet uz Iegūt pārdošanas pasūtījumu kravas.
34. Noklikšķiniet uz Izsniegt bankas dokumentu.
35. Aizvērt lapu.

## <a name="post-packing-slip"></a>Pavadzīmes grāmatošana
1. Darbību rūtī noklikšķiniet uz Izdot un iepakot.
2. Noklikšķiniet uz Grāmatot pavadzīmi.
3. Izvērsiet vai sakļaujiet sadaļu Parametri.
4. Laukā Daudzums atlasiet vērtību “Visi”.
5. Izvērsiet vai sakļaujiet sadaļu Iestatīšana.
6. Laukā Pavadzīmes datums ievadiet datumu.
7. Atlasiet Sūtīšanas numurs.
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Noklikšķiniet uz OK.
10. Noklikšķiniet uz OK.

## <a name="post-sales-invoice"></a>Pārdošanas rēķina grāmatošana
1. Darbību rūtī noklikšķiniet uz Rēķins.
2. Noklikšķiniet uz Rēķins.
3. Izvērsiet vai sakļaujiet sadaļu Pārskats.
4. Atlasiet Sūtīšanas numurs.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Izvērsiet vai sakļaujiet sadaļu Iestatīšana.
7. Laukā Rēķina datums ievadiet datumu.
8. Noklikšķiniet uz OK.
9. Noklikšķiniet uz OK.

## <a name="shipment-document-submitted-status"></a>Iesniegtā sūtījuma dokumenta statuss
1. Darbību rūtī noklikšķiniet uz Pārvaldīt.
2. Noklikšķiniet uz Kredītvēstule.
3. Izvērsiet vai sakļaujiet sadaļu Rindas.
    * Piezīme. Laukam Iesniegtais dokuments jāiestata Jā.  

## <a name="verify-export-letter-of-credit"></a>Kredītvēstules eksportēšanas pārbaude
1. Dodieties uz Kases un bankas vadība > Akreditīvi > Eksporta akreditatīva un importa iekasēšana.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Pārbaudiet, vai lauka Kredītvēstule vienuma Sūtījums statuss ir Iekļauts rēķinā.  

## <a name="customer-payment"></a>Debitora maksājums
1. Pārejiet uz sadaļu Debitori > Maksājumi > Maksājumu žurnāls.
2. Noklikšķiniet uz Jauns.
3. Sarakstā atzīmējiet atlasīto rindu.
4. Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Noklikšķiniet uz Rindas.
7. Laukā Datums ievadiet kādu datumu.
8. Laukā Konts norādiet vēlamās vērtības.
9. Noklikšķiniet uz Nosegšana.
10. Atzīmējiet izvēles rūtiņu, kura atrodas lauka Kopsummas galvenē.
    * Piezīme. Laukam Rādīt iestatiet Kredītvēstule.  
11. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
12. Atzīmējiet vai notīriet izvēles rūtiņu Atzīmēt.
13. Noklikšķiniet uz OK.
14. Noklikšķiniet uz cilnes Maksājums.
    * Bankas dokumenta numura un sūtījuma numura detalizētas informācijas pārbaude  
15. Noklikšķiniet uz Grāmatot.

## <a name="verify-export-letter-of-credit-after-payment"></a>Kredītvēstules eksportēšanas pārbaude pēc maksājuma izpildes
1. Dodieties uz Kases un bankas vadība > Akreditīvi > Eksporta akreditatīva un importa iekasēšana.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Pārbaudiet: Sūtījuma statuss = Maksājums saņemts un bilances summa = 0,00.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]