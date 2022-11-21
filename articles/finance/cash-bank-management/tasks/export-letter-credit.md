---
title: Kredītvēstules eksportēšana
description: Šajā procedūrā ir aprakstīts kredītvēstules eksportēšanas process.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf06a73bf7665059658c7884a0b9f973929d647c
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779559"
---
# <a name="export-letter-of-credit"></a>Kredītvēstules eksportēšana

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir aprakstīts kredītvēstules eksportēšanas process.

Kredītvēstule ir līgums, ko izsniedz banka un kurā banka piekrīt veikt maksājumu pircēja vārdā, ja tiek izpildīti starp pircēju un pārdevēju noslēgtā līguma nosacījumi.



Pirms šīs procedūras palaidiet **procedūru Izveidot bankas mehānismus un grāmatot profilus**, **kā arī Credit_Create bankas mehānisma līguma** procedūru. Lai sekmīgi izpildītu šo procedūru, jāatlasa demonstrācijas uzņēmums “USMF”.


## <a name="create-sales-order-for-export-letter-of-credit"></a>Pārdošanas pasūtījuma izveide kredītvēstules eksportēšanai
1. Pārejiet uz sadaļu **Debitoru parādi > Pasūtījumi > Visi pārdošanas pasūtījumi**.
2. Klikšķiniet **Jauns**.
3. Laukā **Debitora konts** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Izvērsiet vai sakļaujiet **sadaļu Vispārīgi**.
7. Laukā **Vieta** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.
    * Atlasiet vietni **,** kurā tiek glabāts emitējamais krājums.  
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Laukā **Noliktava** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.
    * Atlasiet noliktavu **,** kurā tiek glabāts izsniedzamais krājums.  
10. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Piezīme: **Bankas dokumenta veida** lauks jāizvēlas ar **akreditīvu**.  
11. Laukā **Bankas dokumenta veids** atlasiet **Kredītvēstule**.
12. Izvērsiet **vai sakļaujiet sadaļu Piegāde**.
    * Atlasiet **Piegādes datuma vadīkla** = **Nav**.  
13. **Laukā Pieprasītais saņemšanas datums** ievadiet datumu.
14. Noklikšķiniet uz **Labi**.
15. Laukā **Krājuma kods** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Atlasiet vajadzīgo krājumu, jas ir jāizdod/jāpārdod.  
16. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
17. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
18. Laukā **Vienības cena** ievadiet kādu skaitli.
19. Izvērsiet vai sakļaujiet sadaļu **Detalizēta rindas informācija**.
20. Noklikšķiniet uz **cilnes Piegāde**.
21. **Laukā Pieprasītais nosūtīšanas datums** ievadiet datumu.
22. **Laukā Apstiprināts nosūtīšanas datums** ievadiet datumu.
23. Darbību rūtī noklikšķiniet uz **Pārvaldīt**.
24. Noklikšķiniet uz **Kredītvēstule**.
25. Laukā **Bankas dokumenta numurs** ierakstiet vērtību.
26. **Laukā Derīguma termiņš** ievadiet datumu un laiku.
27. Izvērsiet **vai sakļaujiet sadaļu Bankas informācija**.
28. **Laukā Izdevējbanka** noklikšķiniet uz nolaižamās izvēlnes pogas, lai atvērtu uzmeklēšanu.
29. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
30. **Laukā Konsultatīvā banka** noklikšķiniet uz nolaižamās izvēlnes pogas, lai atvērtu uzmeklēšanu.
31. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
32. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
33. Noklikšķiniet uz **Ienest pārdošanas pasūtījumu sūtījumus**.
34. Noklikšķiniet uz **Izsniegt bankas dokumentu**.
35. Aizvērt lapu.

## <a name="post-packing-slip"></a>Pavadzīmes grāmatošana
1. Darbību rūtī noklikšķiniet uz **Izdot un iepakot**.
2. Noklikšķiniet uz **Izlikt pavadzīmi**.
3. Izvērsiet vai sakļaujiet sadaļu **Parametri**.
4. Laukā **Daudzums** atlasiet vērtību **Visi**.
5. Izvērsiet **vai sakļaujiet sadaļu Iestatīšana**.
6. **Laukā Lapiņas datums (Packing slip date**) ievadiet datumu.
7. Atlasiet Sūtīšanas numurs.
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Noklikšķiniet uz **Labi**.
10. Noklikšķiniet uz **Labi**.

## <a name="post-sales-invoice"></a>Pārdošanas rēķina grāmatošana
1. Darbību rūtī noklikšķiniet uz **Rēķins**.
2. Noklikšķiniet uz **Rēķins**.
3. Izvērsiet **vai sakļaujiet sadaļu Pārskats**.
4. **Atlasiet sūtījuma numuru**.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Izvērsiet **vai sakļaujiet sadaļu Iestatīšana**.
7. Ievadiet datumu laukā **Rēķina datums**.
8. Noklikšķiniet uz **Labi**.
9. Noklikšķiniet uz **Labi**.

## <a name="shipment-document-submitted-status"></a>Iesniegtā sūtījuma dokumenta statuss
1. Darbību rūtī noklikšķiniet uz **Pārvaldīt**.
2. Noklikšķiniet uz **Kredītvēstule**.
3. Izvērsiet **vai sakļaujiet sadaļu Līnijas**.
    * Piezīme: **laukam Iesniegtais** dokuments jābūt iestatītam uz **Jā**.  

## <a name="verify-export-letter-of-credit"></a>Kredītvēstules eksportēšanas pārbaude
1. Dodieties uz **Skaidrā nauda un bankas vadība > Akreditīvi > Eksporta akreditīvs un importa savākšana**.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Pārbaudiet, vai **eksporta akreditīvam** ir **rēķina sūtījuma** statuss **·**.  

## <a name="customer-payment"></a>Debitora maksājums
1. Pārejiet uz žurnālu **Debitoru parādi > Maksājumi > Maksājumi**.
2. Klikšķiniet **Jauns**.
3. Sarakstā atzīmējiet atlasīto rindu.
4. Laukā **Nosaukums** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu pārlūku.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Noklikšķiniet uz **Rindas**.
7. Laukā **Datums** ievadiet datumu.
8. Laukā **Konts** norādiet vēlamās vērtības.
9. Noklikšķiniet uz **Norēķini**.
10. Atzīmējiet izvēles rūtiņu, kura atrodas lauka Kopsummas galvenē.
    * Piezīmes: Iestatiet **lauku Rādīt** uz **Akreditīvs**.  
11. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
12. Atzīmējiet vai notīriet izvēles rūtiņu **Atzīmēt**.
13. Noklikšķiniet uz **Labi**.
14. Noklikšķiniet uz cilnes **Maksājums**.
    * Pārbaudiet bankas dokumenta numuru un sūtījuma numura informāciju  
15. Noklikšķiniet uz **Grāmatot**.

## <a name="verify-export-letter-of-credit-after-payment"></a>Kredītvēstules eksportēšanas pārbaude pēc maksājuma izpildes
1. Dodieties uz **Skaidrā nauda un bankas vadība > Akreditīvi > Eksporta akreditīvs un importa savākšana**.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Pārbaudiet, **vai sūtījuma statuss** = **Maksājums saņemts** un **Atlikuma summa** = **0,00**.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
