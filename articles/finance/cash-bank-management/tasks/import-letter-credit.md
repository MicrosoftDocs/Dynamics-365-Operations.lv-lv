---
title: Importa akreditatīvs
description: Šajā procedūrā ir aprakstīts kredītvēstules importēšanas process.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f07748c2dc41f6411add1d54589652baa7fc3fbb
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779443"
---
# <a name="import-letter-of-credit"></a>Importa akreditatīvs

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir aprakstīts kredītvēstules importēšanas process. Pirms šīs procedūras veikšanas ir jāiestata: bankas iestādes, grāmatošanas profili, bankas iestādes līgums un kreditora bankas dati.

Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.


## <a name="create-a-purchase-order-with-letter-of-credit"></a>Pirkšanas pasūtījuma ar kredītvēstuli izveide
1. Pārejiet uz sadaļu **Kreditoru parādi > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi**.
2. Klikšķiniet **Jauns**.
3. Laukā **Kreditora konts** ievadiet vai atlasiet vērtību.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Izvērsiet sadaļu **Vispārīgi**.
7. Laukā **Vieta** ievadiet vai atlasiet kādu vērtību.
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Laukā **Noliktava** ievadiet vai atlasiet kādu vērtību.
10. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
11. Laukā **Uzskaites datums** ievadiet datumu.
12. Laukā **Piegādes datums** ievadiet datumu.
    * Piezīme **: Bankas dokumenta veida** laukam jābūt **Akreditīvs**.  
13. Noklikšķiniet uz **Labi**.
14. Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību.
15. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
16. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
17. Izvērsiet sadaļu **Detalizēta informācija par rindu**.
18. Noklikšķiniet uz **cilnes Piegāde**.
19. Laukā **Piegādes datums** ievadiet datumu.
20. Laukā **Apstiprinātais piegādes datums** ievadiet datumu.
21. Laukā **Vienības cena** ievadiet kādu skaitli.
    * Ievadiet detalizētu informāciju vienumam Kredītvēstule.  
22. Darbību rūtī noklikšķiniet uz **Pārvaldīt**.
23. Noklikšķiniet uz **Kredītvēstules/importa iekasēšana**.
24. **Laukā Pieteikšanās datums** ievadiet datumu un laiku.
    * Pārbaudiet, **vai laukā Bankas konts ir noklusējuma aktīvais bankas konts**, kura pamatā ir pieteikšanās datums.  
25. Laukā **Bankas dokumenta numurs** ierakstiet vērtību.
26. **Laukā Saņemšanas** datums ievadiet datumu un laiku.
27. Izvērsiet sadaļu Bankas **dokumenti**.
28. **Laukā Derīguma termiņš** ievadiet datumu un laiku.
29. Izvērsiet sadaļu Bankas **rekvizīti**.
30. **Laukā Konsultatīvā banka** ievadiet vai atlasiet vērtību.
31. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
32. Noklikšķiniet uz **Saglabāt**.
33. Noklikšķiniet uz **Ienest pirkšanas pasūtījuma sūtījumus**.
34. Aizvērt lapu.
35. Darbību rūtī noklikšķiniet uz **Pirkšana**.
36. Noklikšķiniet uz **Apstiprināt**.
37. Darbību rūtī noklikšķiniet uz **Pārvaldīt**.
38. Noklikšķiniet uz **Kredītvēstule / importa iekasēšana**.
39. Noklikšķiniet uz **Apstrādāt**.
40. Noklikšķiniet uz **Apstiprināt**.
    * Pārbaudiet, vai lauka Kredītlīnijas bilance vērtība samazina pirkšanas pasūtījuma summu. Šajā piemērā pirkuma summa ir 500,00; iestādes ierobežojums ir 10 000,00 un atbilstoši iestādes bilance ir 9500,00.  
41. Aizvērt lapu.
42. Laukā **Vienības cena** ievadiet kādu skaitli.
43. Noklikšķiniet uz **Saglabāt**.
44. Darbību rūtī noklikšķiniet uz **Pirkšana**.
45. Noklikšķiniet uz **Apstiprināt**.
    * Vienības cenu izmaiņu dēļ jalabo lauks Kredītvēstule.  
46. Darbību rūtī noklikšķiniet uz **Pārvaldīt**.
47. Noklikšķiniet uz **Kredītvēstule / importa iekasēšana**.
    * Pirkšanas vienības cenas izmaiņu dēļ jalabo lauks Kredītvēstule.  
48. Noklikšķiniet uz **Apstrādāt**.
49. Noklikšķiniet uz **Grozīt**.
50. Noklikšķiniet uz **Noņemt**.
51. Noklikšķiniet uz pogas **Jā**.
52. Noklikšķiniet uz **Ienest pirkšanas pasūtījuma sūtījumus**.
53. Noklikšķiniet uz **Apstrādāt**.
54. Noklikšķiniet uz **Apstiprināt**.
    * Pārbaudiet, vai lauka Kredītlīnijas bilance vērtība samazina pirkšanas pasūtījuma summu. Šajā piemērā rediģētā pirkuma summa ir 600,00; iestādes ierobežojums ir 10 000,00; tāpēc iestādes bilance ir 9400,00.  
55. Aizvērt lapu.

## <a name="post-packing-slip"></a>Pavadzīmes grāmatošana
1. Darbību rūtī noklikšķ. uz **Saņemt**.
2. Nokl. **Pr. ieejas pl**.
3. **Laukā PurchParmTable_Num** ierakstiet vērtību.
    * Atlasiet kopā ar kredītvēstules atsauci izveidoto lauku Sūtīšanas numurs.  
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Laukā **Produkta ieejas plūsmas datums** ievadiet datumu.
6. Noklikšķiniet uz **Labi**.
7. Aizvērt lapu.
8. Aizvērt lapu.

## <a name="verify-import-letter-of-credit-status"></a>Darbības Kredītvēstules importēšana statusa pārbaude
1. Dodieties uz Skaidras **naudas un bankas pārvaldības > Akreditīvi > Importa akreditīvs un importa savākšana**.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Pārbaudiet darbības Kredītvēstules importēšana statusu.     
4. Aizvērt lapu.
5. Aizvērt lapu.

## <a name="post-purchase-invoice"></a>Pirkšanas rēķina grāmatošana
1. Pārejiet uz sadaļu **Kreditoru parādi > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi**.
    * Atlasiet pirkšanas pasūtījumu, kas tika izveidots kopā ar kredītvēstuli.  
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
4. Darbību rūtī noklikšķiniet uz **Rēķins**.
5. Noklikšķiniet uz **Rēķins**.
6. Laukā **Numurs** ierakstiet vērtību.
7. **Laukā Sūtījuma numurs** ievadiet vai atlasiet vērtību.
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Ievadiet datumu laukā **Rēķina datums**.
10. Noklikšķiniet uz **Atjaunināt atbilstības statusu**.
11. Noklikšķiniet uz **Grāmatot**.
12. Aizvērt lapu.
13. Aizvērt lapu.

## <a name="verify-import-letter-of-credit-status-and-printing"></a>Pārbaudiet Kredītvēstules importēšanas statusu un drukāšanu

1. Dodieties uz Skaidras **naudas un bankas pārvaldības > Akreditīvi > Importa akreditīvs un importa savākšana**.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Pārbaudiet darbību Importēt kredītvēstuli 2.  
    * Validēt: sūtījuma statuss **Bankas iestādes informācija,** = **par kuru izrakstīts** rēķins  
4. Noklikšķiniet uz **Skatīt**.
5. Noklikšķiniet uz **Drukāt lietojumprogrammu**.
6. Noklikšķiniet uz **Labi**.
    * Pārbaudiet, vai kredītvēstules pieteikums tiek izdrukāts.  
7. Aizvērt lapu.
8. Aizvērt lapu.
9. Aizvērt lapu.

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a>Kreditoru maksājumu žurnāla grāmatošana izveidotajam pirkšanas rēķinam ar kredītvēstuli
1. Pārejiet uz sadaļu **Kreditori > Maksājumi > Maksājumu žurnāls**.
2. Klikšķiniet **Jauns**.
3. Ievadiet vai atlasiet vērtību laukā **Nosaukums**.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Noklikšķiniet uz **Rindas**.
6. Laukā **Datums** ievadiet datumu.
7. Laukā **Konts** norādiet vēlamās vērtības.
8. Noklikšķiniet uz **Nokārtot transakcijas**.
9. Izvērsiet sadaļu Kopsummas.
10. Laukā **Rādīt** atlasiet opciju.
    * Pārbaudiet, **vai lauki Bankas dokumenta numurs un** Sūtījuma numurs **ir** atjaunināti.  
11. Atzīmējiet izvēles rūtiņu **Atzīmēt**.
12. Noklikšķiniet uz **Labi**.
13. Noklikšķiniet uz cilnes Maksājums.
    * Pārbaudiet, **vai lauki Bankas dokumenta numurs un** Sūtījuma numurs **ir** atjaunināti.  
14. Noklikšķiniet uz **Grāmatot**.
15. Aizvērt lapu.
16. Aizvērt lapu.

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a>Darbības Kredītvēstules importēšana statusa pārbaude pēc rēķina apmaksas
1. Dodieties uz Skaidras **naudas un bankas pārvaldības > Akreditīvi > Importa akreditīvs un importa savākšana**.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Pārbaudiet darbības Kredītvēstules importēšana statusu.   
4. Aizvērt lapu.

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a>Bankas iestādes ierobežojuma un lietojuma pārskata pārbaude
1. Dodieties uz Skaidrā **nauda un bankas vadība > Pieprasījumi un ziņojumi > Akreditīvi vai garantijas > Bankas iespējas un izmantošanas pārskats**.
2. Izvērsiet sadaļu Iekļaujamie ieraksti.
3. Noklikšķiniet uz **Filtrēt**.
    * Definējiet **lauku Kritēriji** ar nepieciešamo bankas kontu.  
4. Ievadiet vai atlasiet vērtību laukā **Kritēriji**.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Noklikšķiniet uz **Labi**.
7. Noklikšķiniet uz **Labi**.
    * Pārbaudiet pārskatu, kurā ir norādītas transakcijas.  
    * Pārbaudiet, vai pārskatā ir ietvertas transakcijas ar šādiem elementiem Bankas dokumenta numurs, Iestādes ierobežojums, Izmantotā summa un Iestādes bilances summa.  
8. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
