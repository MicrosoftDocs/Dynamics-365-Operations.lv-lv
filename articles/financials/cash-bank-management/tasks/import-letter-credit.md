---
title: Importa akreditatīvs
description: Šajā procedūrā ir aprakstīts kredītvēstules importēšanas process.
author: kweekley
manager: AnnBe
ms.date: 02/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d5539fbd17c880d8bbadd47444c9cc53fce039c
ms.sourcegitcommit: 0c1deb100d0bf6dacd14b328968bbc7a9d92583a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/28/2019
ms.locfileid: "771235"
---
# <a name="import-letter-of-credit"></a>Importa akreditatīvs

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir aprakstīts kredītvēstules importēšanas process. Pirms šīs procedūras veikšanas ir jāiestata: bankas iestādes, grāmatošanas profili, bankas iestādes līgums un kreditora bankas dati.

Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.


## <a name="create-a-purchase-order-with-letter-of-credit"></a>Pirkšanas pasūtījuma ar kredītvēstuli izveide
1. Pārejiet uz sadaļu Kreditori > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Ievadiet vai atlasiet vērtību laukā kreditora konts.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Izvērsiet sadaļu Vispārīgi.
7. Laukā Vieta ievadiet vai atlasiet kādu vērtību.
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Laukā Noliktava ievadiet vai atlasiet kādu vērtību.
10. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
11. Laukā Uzskaites datums ievadiet datumu.
12. Laukā Piegādes datums ievadiet datumu.
    * Ņemiet vērā! Jābūt atlasītam laukam Bankas dokumenta tips un vērtībai Kredītvēstule.  
13. Noklikšķiniet uz OK.
14. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
15. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
16. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
17. Izvērsiet sadaļu Detalizēta informācija par rindu.
18. Noklikšķiniet uz cilnes Piegāde.
19. Laukā Piegādes datums ievadiet datumu.
20. Laukā Apstiprinātais piegādes datums ievadiet datumu.
21. Laukā Vienības cena ievadiet kādu skaitli.
    * Ievadiet detalizētu informāciju vienumam Kredītvēstule.  
22. Darbību rūtī noklikšķiniet uz Pārvaldīt.
23. Noklikšķiniet uz Kredītvēstule/importa inkaso.
24. Laukā Izmantošanas datums ievadiet datumu un laiku.
    * Pārbaudiet, vai lauka Bankas konts ir aktīvs noklusējuma Bankas konts, kas tiek izmantots, ņemot vērā pieteikuma datumu.  
25. Laukā Bankas dokumenta numurs ierakstiet vērtību.
26. Laukā Ieejas plūsmas datums ievadiet datumu un laiku.
27. Izvērsiet sadaļu Bankas dokuments.
28. Laukā Beigu datums ievadiet datumu un laiku.
29. Izvērsiet sadaļu Detalizēta informācija par banku.
30. Laukā Konsultatīvā banka ievadiet vai atlasiet vērtību.
31. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
32. Noklikšķiniet uz Saglabāt.
33. Noklikšķiniet uz Iegūt pirkšanas pasūtījumu kravas.
34. Aizvērt lapu.
35. Darbību rūtī noklikšķiniet uz Pirkt.
36. Noklikšķiniet uz Apstiprināt.
37. Darbību rūtī noklikšķiniet uz Pārvaldīt.
38. Noklikšķiniet uz Kredītvēstule/importa inkaso.
39. Noklikšķiniet uz Apstrādāt.
40. Noklikšķiniet uz Apstiprināt.
    * Pārbaudiet, vai lauka Kredītlīnijas bilance vērtība samazina pirkšanas pasūtījuma summu.  Šajā piemērā pirkuma summa ir 500,00; iestādes ierobežojums ir 10 000,00 un atbilstoši iestādes bilance ir 9500,00.  
41. Aizvērt lapu.
42. Laukā Vienības cena ievadiet kādu skaitli.
43. Noklikšķiniet uz Saglabāt.
44. Darbību rūtī noklikšķiniet uz Pirkt.
45. Noklikšķiniet uz Apstiprināt.
    * Vienības cenu izmaiņu dēļ jalabo lauks Kredītvēstule.  
46. Darbību rūtī noklikšķiniet uz Pārvaldīt.
47. Noklikšķiniet uz Kredītvēstule/importa inkaso.
    * Pirkšanas vienības cenas izmaiņu dēļ jalabo lauks Kredītvēstule.  
48. Noklikšķiniet uz Apstrādāt.
49. Noklikšķiniet uz Labot.
50. Noklikšķiniet uz Noņemt.
51. Noklikšķiniet uz Jā.
52. Noklikšķiniet uz Iegūt pirkšanas pasūtījumu kravas.
53. Noklikšķiniet uz Apstrādāt.
54. Noklikšķiniet uz Apstiprināt.
    * Pārbaudiet, vai lauka Kredītlīnijas bilance vērtība samazina pirkšanas pasūtījuma summu.  Šajā piemērā rediģētā pirkuma summa ir 600,00; iestādes ierobežojums ir 10 000,00; tāpēc iestādes bilance ir 9400,00.  
55. Aizvērt lapu.

## <a name="post-packing-slip"></a>Pavadzīmes grāmatošana
1. Darbību rūtī noklikšķiniet uz Saņemt.
2. Noklikšķiniet uz Produktu ieejas plūsma.
3. Laukā PurchParmTable_Num ierakstiet vērtību.
    * Atlasiet kopā ar kredītvēstules atsauci izveidoto lauku Sūtīšanas numurs.  
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Laukā Produktu ieejas plūsmas datums ievadiet datumu.
6. Noklikšķiniet uz OK.
7. Aizvērt lapu.
8. Aizvērt lapu.

## <a name="verify-import-letter-of-credit-status"></a>Darbības Kredītvēstules importēšana statusa pārbaude
1. Dodieties uz Kases un bankas vadība > Akreditatīvi > Importa akreditatīvs un importa iekasēšana.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Pārbaudiet darbības Kredītvēstules importēšana statusu.     
4. Aizvērt lapu.
5. Aizvērt lapu.

## <a name="post-purchase-invoice"></a>Pirkšanas rēķina grāmatošana
1. Pārejiet uz sadaļu Kreditori > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.
    * Atlasiet pirkšanas pasūtījumu, kas tika izveidots kopā ar kredītvēstuli.  
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
4. Darbību rūtī noklikšķiniet uz Rēķins.
5. Noklikšķiniet uz Rēķins.
6. Laukā Numurs ierakstiet kādu vērtību.
7. Laukā Sūtīšanas numurs ievadiet vai atlasiet vērtību.
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Laukā Rēķina datums ievadiet datumu.
10. Noklikšķiniet uz Atjaunināt atbilstības statusu.
11. Noklikšķiniet uz Grāmatot.
12. Aizvērt lapu.
13. Aizvērt lapu.

## <a name="verify-import-letter-of-credit-status"></a>Darbības Kredītvēstules importēšana statusa pārbaude
1. Dodieties uz Kases un bankas vadība > Akreditatīvi > Importa akreditatīvs un importa iekasēšana.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Pārbaudiet darbību Importēt kredītvēstuli 2.  
    * Pārbaudiet: Sūtījuma statuss = rēķinos iekļautie bankas dati  
4. Noklikšķiniet uz Skatīt.
5. Noklikšķiniet uz Drukāt pieteikumu.
6. Noklikšķiniet uz OK.
    * Pārbaudiet, vai kredītvēstules pieteikums tiek izdrukāts.  
7. Aizvērt lapu.
8. Aizvērt lapu.
9. Aizvērt lapu.

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a>Kreditoru maksājumu žurnāla grāmatošana izveidotajam pirkšanas rēķinam ar kredītvēstuli
1. Pārejiet uz sadaļu Kreditori > Maksājumi > Maksājumu žurnāls.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Noklikšķiniet uz Rindas.
6. Laukā Datums ievadiet kādu datumu.
7. Laukā Konts norādiet vēlamās vērtības.
8. Noklikšķiniet uz Transakciju nosegšana.
9. Izvērsiet sadaļu Kopsummas.
10. Laukā Rādīt atlasiet kādu opciju.
    * Pārbaudiet, vai lauks Bankas dokumenta numurs un Sūtījuma numurs tika atjaunināts.  
11. Atzīmējiet izvēles rūtiņu Atzīmēt.
12. Noklikšķiniet uz OK.
13. Noklikšķiniet uz cilnes Maksājums.
    * Pārbaudiet, vai lauks Bankas dokumenta numurs un Sūtījuma numurs tika atjaunināts.  
14. Noklikšķiniet uz Grāmatot.
15. Aizvērt lapu.
16. Aizvērt lapu.

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a>Darbības Kredītvēstules importēšana statusa pārbaude pēc rēķina apmaksas
1. Dodieties uz Kases un bankas vadība > Akreditatīvi > Importa akreditatīvs un importa iekasēšana.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Pārbaudiet darbības Kredītvēstules importēšana statusu.   
4. Aizvērt lapu.

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a>Bankas iestādes ierobežojuma un lietojuma pārskata pārbaude
1. Dodieties uz Kases un bankas vadība > Uzziņas un atskaites > Akreditatīvi vai garantijas vēstules > Bankas pakalpojumu un lietojuma atskaite.
2. Izvērsiet sadaļu Iekļaujamie ieraksti.
3. Noklikšķiniet uz Filtrēt.
    * Definējiet lauka Kritēriji vērtību, izmantojot nepieciešamo bankas kontu.  
4. Laukā Kritēriji ievadiet vai atlasiet kādu vērtību.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Noklikšķiniet uz OK.
7. Noklikšķiniet uz OK.
    * Pārbaudiet pārskatu, kurā ir norādītas transakcijas.  
    * Pārbaudiet, vai pārskatā ir ietvertas transakcijas ar šādiem elementiem Bankas dokumenta numurs, Iestādes ierobežojums, Izmantotā summa un Iestādes bilances summa.  
8. Aizvērt lapu.

