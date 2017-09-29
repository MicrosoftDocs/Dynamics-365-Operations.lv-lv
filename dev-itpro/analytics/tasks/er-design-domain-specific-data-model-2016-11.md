--- 
title: "Noformēt domēnam specifisku datu modeli elektronisko pārskatu veidošanai (ER)"
description: "Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izveidot jaunu Elektronisko pārskatu (ER) konfigurāciju, kas saturēs datu modeli elektronisko maksājumu dokumentiem."
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: bf727b63ed86e7cc26d4fca630d97af88abb1804
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="design-a-domain-specific-data-model-for-electronic-reporting-er"></a>Noformēt domēnam specifisku datu modeli elektronisko pārskatu veidošanai (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izveidot jaunu Elektronisko pārskatu (ER) konfigurāciju, kas saturēs datu modeli elektronisko maksājumu dokumentiem. Šis datu modelis vēlāk tiek izmantots kā datu avots, kad veidojat maksājumu dokumentu formātu.



Šajā piemērā tiek izveidota parauga uzņēmuma Litware, Inc. konfigurācija. Šīs darbības var veikt jebkurā uzņēmumā, jo ER konfigurācijas ir kopīgas visiem uzņēmumiem. Lai veiktu šīs darbības, vispirms veiciet "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu" procedūras darbības.

1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
    * Atlasiet konfigurācijas nodrošinātāju parauga uzņēmumam Litware, Inc. Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas aprakstītas procedūrā “Izveidot konfigurācijas nodrošinātāju un atzīmēt to ka aktīvu”.  
2. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
    * Jūs izveidosit konfigurāciju, kas satur datu modeli elektronisko maksājumu dokumentiem. Šis datu modelis tiks vēlāk izmantots par datu avotu, veidojot maksājumu dokumentu formātu.  

## <a name="create-a-new-data-model-configuration"></a>Jaunas datu modeļa konfigurācijas izveide
1. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.
2. Laukā Nosaukums ierakstiet "Maksājumi (vienkāršots modelis)".
    * Maksājumi (vienkāršots modelis)  
3. Laukā Apraksts ierakstiet "Maksājumu modeļa konfigurācija".
    * Maksājuma modeļa konfigurācija  
    * Šeit tiek automātiski ievadīts aktīvais konfigurācijas nodrošinātājs. Šis nodrošinātājs varēs uzturēt šo konfigurāciju. Citi nodrošinātāji var izmantot šo konfigurāciju, bet nevar uzturēt to.  
4. Noklikšķiniet uz pogas Izveidot konfigurāciju, lai pabeigtu konfigurācijas izveides uzdevumu

## <a name="create-a-data-model"></a>Datu modeļa izveide
    * Jūs veidojat jaunu datu modeli atlasītajai konfigurācijai. Šīs konfigurācijas versijas statuss būs Melnraksts.  
1. Noklikšķiniet uz Veidotājs.

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a>Definēt struktūru pusei, kas piedalās maksājuma procesā
1. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
2. Laukā Nosaukums ierakstiet “Puse”.
    * Puse  
3. Noklikšķiniet uz Pievienot.
4. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
5. Laukā Nosaukums ierakstiet "Nosaukums".
    * Vārds, uzvārds  
6. Laukā Vienuma tips atlasiet "String".
7. Noklikšķiniet uz Pievienot.
8. Laukā Atrast ierakstiet “Puse”.
    * Puse  
9. Noklikšķiniet uz Atrast iepriekšējo.

## <a name="define-the-bank-structure-for-this-model"></a>Šī modeļa bankas struktūras definēšana
1. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
2. Laukā Nosaukums ierakstiet "Aģents".
    * Aģents  
3. Laukā Vienuma tips atlasiet "Record".
4. Noklikšķiniet uz Pievienot.
5. Laukā Apraksts ierakstiet “Finanšu iestāde (piemēram, banka), kas apkalpo puses (debitora/kreditora) kontu.”.
    * Finanšu iestāde (piemēram, banka), kas apkalpo puses (debitora/kreditora) kontu.  
6. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
7. Laukā Nosaukums ierakstiet "Nosaukums".
    * Vārds, uzvārds  
8. Laukā Vienuma tips atlasiet "String".
9. Noklikšķiniet uz Pievienot.
10. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
11. Laukā Nosaukums ierakstiet "SWIFT".
    * SWIFT  
12. Noklikšķiniet uz Pievienot.
13. Laukā Apraksts ievadiet “Bankas identifikācijas kods”.
    * Bankas identifikācijas kods  
14. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
15. Laukā Nosaukums ierakstiet "RoutingNumber".
    * RoutingNumber  
16. Noklikšķiniet uz Pievienot.
17. Laukā Apraksts ievadiet “Reģistrācijas numurs”.
    * Reģistrācijas numurs  
18. Noklikšķiniet uz Atrast iepriekšējo.

## <a name="define-the-bank-account-structure-for-this-model"></a>Šī modeļa bankas konta struktūras definēšana
1. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
2. Laukā Nosaukums ierakstiet "Konts".
    * Konts  
3. Laukā Vienuma tips atlasiet "Record".
4. Noklikšķiniet uz Pievienot.
5. Laukā Apraksts ierakstiet “Identifikācija puses kontam kādā finanšu iestādē (piemēram, bankā).”.
    * Identifikācija puses kontam kādā finanšu iestādē (piemēram, bankā).  
6. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
7. Laukā Nosaukums ierakstiet "Valūta".
    * Valūta  
8. Laukā Vienuma tips atlasiet "String".
9. Noklikšķiniet uz Pievienot.
10. Laukā Apraksts ievadiet “Valūtas kods”.
    * Valūtas kods  
11. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
12. Laukā Nosaukums ierakstiet "Number".
    * Skaits  
13. Noklikšķiniet uz Pievienot.
14. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
15. Laukā Nosaukums ierakstiet "IBAN".
    * IBAN  
16. Noklikšķiniet uz Pievienot.
17. Laukā Apraksts ievadiet “Starptautiskais bankas konta numurs ”.
    * Starptautiskais bankas konta numurs  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a>Definēt maksājuma ziņojuma struktūru kredīta pārsūtīšanas maksājuma veidam
1. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
2. Laukā Jauns zars ievadiet “Modeļa sakne”.
3. Laukā Nosaukums ierakstiet "CustomerCreditTransferInitiation".
    * CustomerCreditTransferInitiation  
4. Noklikšķiniet uz Pievienot.
5. Laukā Atrast ierakstiet “CustomerCreditTransferInitiation”.
    * CustomerCreditTransferInitiation  
6. Noklikšķiniet uz Atrast iepriekšējo.
7. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
8. Laukā Nosaukums ievadiet "MessageIdentification".
    * MessageIdentification  
9. Noklikšķiniet uz Pievienot.
10. Laukā Apraksts ievadiet “Atsauce no punkta uz punktu, kuru norādījusi instruējošā puse ziņojuma identificēšanai (tā tiek nosūtīta nākamajai pusei).”.
    * Atsauce no punkta uz punktu, kuru piešķīrusi instruējošā puse, ziņojuma identificēšanai (tā tiek nosūtīta nākamajai pusei).  
11. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
12. Laukā Nosaukums ievadiet "ProcessingDateTime".
    * ProcessingDateTime  
13. Laukā Vienuma tips atlasiet "DateTime".
14. Noklikšķiniet uz Pievienot.
15. Laukā Apraksts ievadiet “Maksājuma ziņojuma izveides datums un laiks.”.
    * Datums un laiks, kad maksājuma ziņojums tika izveidots.  
16. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
    * Definējiet maksāšanas transakcijas struktūras šim modelim.  
17. Laukā Nosaukums ierakstiet "Maksājumi".
    * Maksājumi  
18. Laukā Vienuma tips atlasiet "Record list".
19. Noklikšķiniet uz Pievienot.
20. Laukā Apraksts ievadiet "Aktīvā ziņojuma maksājuma rindas".
    * Pašreizējā ziņojuma maksājuma rindas  
21. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
22. Laukā Nosaukums ierakstiet "Kreditors".
    * Kreditors  
23. Laukā Vienuma tips atlasiet "Record".
24. Noklikšķiniet uz Pievienot.
25. Laukā Apraksts ierakstiet “Puse, kurai ir jāsaņem kāda naudas summa.”.
    * Puse, kurai ir jāsaņem kāda naudas summa.  
26. Noklikšķiniet uz Pārslēgt vienuma atsauci.
27. Laukā Atrast ierakstiet “Puse”.
    * Puse  
28. Noklikšķiniet uz Atrast nākamo.
29. Noklikšķiniet uz OK.
30. Laukā Atrast ierakstiet “Maksājumi”.
    * Maksājumi  
31. Noklikšķiniet uz Atrast nākamo.
32. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
33. Laukā Nosaukums ierakstiet "Debitors".
    * Debitors  
34. Noklikšķiniet uz Pievienot.
35. Laukā Apraksts ierakstiet “Puse, kurai ir pienākums maksāt naudas summu (galīgajam) kreditoram.”.
    * Puse, kurai ir pienākums maksāt naudas summu (galīgajam) kreditoram.  
36. Noklikšķiniet uz Pārslēgt vienuma atsauci.
37. Laukā Atrast ierakstiet “Puse”.
    * Puse  
38. Noklikšķiniet uz Atrast nākamo.
39. Noklikšķiniet uz OK.
40. Noklikšķiniet uz Atrast nākamo.
41. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
42. Laukā Nosaukums ierakstiet "Apraksts".
    * apraksts  
43. Laukā Vienuma tips atlasiet "String".
44. Noklikšķiniet uz Pievienot.
45. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
46. Laukā Nosaukums ierakstiet "Valūta".
    * Valūta  
47. Noklikšķiniet uz Pievienot.
48. Laukā Apraksts ievadiet “Valūtas kods”.
    * Valūtas kods  
49. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
50. Laukā Nosaukums ierakstiet "TransactionDate".
    * TransactionDate  
51. Laukā Vienuma tips atlasiet "Date".
52. Noklikšķiniet uz Pievienot.
53. Laukā Apraksts ievadiet “Darījuma datums”.
    * Darījuma datums  
54. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
55. Laukā Nosaukums ierakstiet "'InstructedAmount".
    * InstructedAmount  
56. Laukā Vienuma tips atlasiet "Real".
57. Noklikšķiniet uz Pievienot.
58. Laukā Apraksts ievadiet “Naudas summa, ko paredzēts pārvietot starp debitoru un kreditoru, pirms ir ieturētas maksas. Summa jāizsaka tajā valūtā, kuru norādījusi iniciējošā puse.".
    * Naudas summa, ko paredzēts pārvietot starp debitoru un kreditoru pirms maksu ieturēšanas. Summa jāizsaka tajā valūtā, kuru norādījusi iniciējošā puse.  
59. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
60. Laukā Nosaukums ierakstiet "End2EndID".
    * End2EndID  
61. Laukā Vienuma tips atlasiet "String".
62. Noklikšķiniet uz Pievienot.
63. Laukā Apraksts ievadiet “Unikālais identifikators, kuru piešķīrusi iniciējošā puse. Šis identifikators tiek nodots tālāk neizmainītā veidā visā ķēdes garumā."
    * Unikāls identifikators, kuru piešķīrusi iniciējošā puse. Šis identifikators tiek nodots tālāk neizmainītā veidā visā ķēdes garumā.  
64. Laukā Nosaukums ierakstiet "PaymentModel".
    * PaymentModel nosaukums sakrīt ar iepriekš definētiem maksājumu veidlapu interfeisiem.  
65. Noklikšķiniet uz Saglabāt.
66. Aizvērt lapu.

