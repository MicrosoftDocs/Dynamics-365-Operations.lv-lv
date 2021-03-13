---
title: ER domēnam specifiska datu modeļa izveide
description: Tematā aprakstīts, kā izveidot jaunu elektronisko pārskatu (ER) konfigurāciju, kas satur datu modeli elektroniskajiem maksājumu dokumentiem.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1eb2c6e5b5f186fb6db7c32a9982807274e5ea1b
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092695"
---
# <a name="er-design-domain-specific-data-model"></a>ER domēnam specifiska datu modeļa izveide

[!include [banner](../../includes/banner.md)]

Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izveidot jaunu Elektronisko pārskatu (ER) konfigurāciju, kas saturēs datu modeli elektronisko maksājumu dokumentiem. Šis datu modelis vēlāk tiek izmantots kā datu avots, kad veidojat maksājumu dokumentu formātu.

Šajā piemērā tiek izveidota parauga uzņēmuma Litware, Inc. konfigurācija. Šīs darbības var veikt jebkurā uzņēmumā, jo ER konfigurācijas ir kopīgas visiem uzņēmumiem. Lai izpildītu tālāk norādītās darbības, vispirms izpildiet darbības, kas aprakstītas procedūrā "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu".

1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.

    Atlasiet konfigurācijas nodrošinātāju parauga uzņēmumam 'Litware, Inc.' Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas aprakstītas procedūrā "Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu".  
    
2. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.

    Jūs izveidosit konfigurāciju, kas satur datu modeli elektronisko maksājumu dokumentiem. Šis datu modelis tiks vēlāk izmantots par datu avotu, veidojot maksājumu dokumentu formātu.  

## <a name="create-a-new-data-model-configuration"></a>Jaunas datu modeļa konfigurācijas izveide
1. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.
2. Laukā Nosaukums ierakstiet "Maksājumi (vienkāršots modelis)".
3. Laukā Apraksts ierakstiet "Maksājumu modeļa konfigurācija".

    Šeit tiek automātiski ievadīts aktīvais konfigurācijas nodrošinātājs. Šis nodrošinātājs varēs uzturēt šo konfigurāciju. Citi nodrošinātāji var izmantot šo konfigurāciju, bet nevar uzturēt to.  

4. Noklikšķiniet uz pogas 'Izveidot konfigurāciju', lai pabeigtu konfigurācijas izveides uzdevumu

## <a name="create-a-data-model"></a>Datu modeļa izveide
Jūs veidojat jaunu datu modeli atlasītajai konfigurācijai. Šīs konfigurācijas versijas statuss būs Melnraksts.  
1. Noklikšķiniet uz Veidotājs.

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a>Definēt struktūru pusei, kas piedalās maksājuma procesā
1. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
2. Laukā Nosaukums ierakstiet “Puse”.
3. Noklikšķiniet uz Pievienot.
4. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
5. Laukā Nosaukums ierakstiet "Nosaukums".
6. Laukā Vienuma tips atlasiet "String".
7. Noklikšķiniet uz Pievienot.
8. Laukā Atrast ierakstiet “Puse”.
9. Noklikšķiniet uz Atrast iepriekšējo.

## <a name="define-the-bank-structure-for-this-model"></a>Šī modeļa bankas struktūras definēšana
1. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
2. Laukā Nosaukums ierakstiet "Aģents".
3. Laukā Vienuma tips atlasiet "Record".
4. Noklikšķiniet uz Pievienot.
5. Laukā Apraksts ierakstiet “Finanšu iestāde (piemēram, banka), kas apkalpo puses (debitora/kreditora) kontu.”.

    Finanšu iestāde (piemēram, banka), kas apkalpo puses (debitora/kreditora) kontu.  

6. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
7. Laukā Nosaukums ierakstiet "Nosaukums". 
8. Laukā Vienuma tips atlasiet "String".
9. Noklikšķiniet uz Pievienot.
10. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
11. Laukā Nosaukums ierakstiet "SWIFT".
12. Noklikšķiniet uz Pievienot.
13. Laukā Apraksts ievadiet “Bankas identifikācijas kods”. 
14. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
15. Laukā Nosaukums ierakstiet "RoutingNumber".
16. Noklikšķiniet uz Pievienot.
17. Laukā Apraksts ievadiet “Reģistrācijas numurs”.
18. Noklikšķiniet uz Atrast iepriekšējo.

## <a name="define-the-bank-account-structure-for-this-model"></a>Šī modeļa bankas konta struktūras definēšana
1. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
2. Laukā Nosaukums ierakstiet "Konts". 
3. Laukā Vienuma tips atlasiet "Record".
4. Noklikšķiniet uz Pievienot.
5. Laukā Apraksts ierakstiet “Identifikācija puses kontam kādā finanšu iestādē (piemēram, bankā).”.

    Identifikācija puses kontam kādā finanšu iestādē (piemēram, bankā).  

6. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
7. Laukā Nosaukums ierakstiet "Valūta". 
8. Laukā Vienuma tips atlasiet "String".
9. Noklikšķiniet uz Pievienot.
10. Laukā Apraksts ievadiet “Valūtas kods”.
11. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
12. Laukā Nosaukums ierakstiet "Number". 
13. Noklikšķiniet uz Pievienot.
14. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
15. Laukā Nosaukums ierakstiet "IBAN". 
16. Noklikšķiniet uz Pievienot.
17. Laukā Apraksts ievadiet “Starptautiskais bankas konta numurs ”.

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a>Definēt maksājuma ziņojuma struktūru kredīta pārsūtīšanas maksājuma veidam
1. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
2. Laukā Jauns zars ievadiet “Modeļa sakne”.
3. Laukā Nosaukums ierakstiet "CustomerCreditTransferInitiation".
4. Noklikšķiniet uz Pievienot.
5. Laukā Atrast ierakstiet “CustomerCreditTransferInitiation”. 
6. Noklikšķiniet uz Atrast iepriekšējo.
7. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
8. Laukā Nosaukums ievadiet "MessageIdentification". 
9. Noklikšķiniet uz Pievienot.
10. Laukā Apraksts ievadiet “Atsauce no punkta uz punktu, kuru norādījusi instruējošā puse ziņojuma identificēšanai (tā tiek nosūtīta nākamajai pusei).”.

    Atsauce no punkta uz punktu, kuru piešķīrusi instruējošā puse, ziņojuma identificēšanai (tā tiek nosūtīta nākamajai pusei).  

11. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
12. Laukā Nosaukums ievadiet "ProcessingDateTime".
13. Laukā Vienuma tips atlasiet "DateTime".
14. Noklikšķiniet uz Pievienot.
15. Laukā Apraksts ievadiet “Maksājuma ziņojuma izveides datums un laiks.”. 
16. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.

    Definējiet maksāšanas transakcijas struktūras šim modelim.  

17. Laukā Nosaukums ierakstiet "Maksājumi".
18. Laukā Vienuma tips atlasiet "Record list".
19. Noklikšķiniet uz Pievienot.
20. Laukā Apraksts ievadiet "Aktīvā ziņojuma maksājuma rindas".
21. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
22. Laukā Nosaukums ierakstiet "Kreditors". 
23. Laukā Vienuma tips atlasiet "Record".
24. Noklikšķiniet uz Pievienot.
25. Laukā Apraksts ierakstiet “Puse, kurai ir jāsaņem kāda naudas summa.”. 
26. Noklikšķiniet uz Pārslēgt vienuma atsauci.
27. Laukā Atrast ierakstiet “Puse”.
28. Noklikšķiniet uz Atrast nākamo.
29. Noklikšķiniet uz Labi.
30. Laukā Atrast ierakstiet “Maksājumi”.
31. Noklikšķiniet uz Atrast nākamo.
32. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
33. Laukā Nosaukums ierakstiet "Debitors". 
34. Noklikšķiniet uz Pievienot.
35. Laukā Apraksts ierakstiet “Puse, kurai ir pienākums maksāt naudas summu (galīgajam) kreditoram.”.
36. Noklikšķiniet uz Pārslēgt vienuma atsauci.
37. Laukā Atrast ierakstiet “Puse”.
38. Noklikšķiniet uz Atrast nākamo.
39. Noklikšķiniet uz Labi.
40. Noklikšķiniet uz Atrast nākamo.
41. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
42. Laukā Nosaukums ierakstiet "Apraksts".
43. Laukā Vienuma tips atlasiet "String".
44. Noklikšķiniet uz Pievienot.
45. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
46. Laukā Nosaukums ierakstiet "Valūta".
47. Noklikšķiniet uz Pievienot.
48. Laukā Apraksts ievadiet “Valūtas kods”.
49. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
50. Laukā Nosaukums ierakstiet "TransactionDate". 
51. Laukā Vienuma tips atlasiet "Date".
52. Noklikšķiniet uz Pievienot.
53. Laukā Apraksts ievadiet “Darījuma datums”. 
54. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
55. Laukā Nosaukums ierakstiet "'InstructedAmount".  
56. Laukā Vienuma tips atlasiet "Real".
57. Noklikšķiniet uz Pievienot.
58. Laukā Apraksts ievadiet “Naudas summa, ko paredzēts pārvietot starp debitoru un kreditoru, pirms ir ieturētas maksas. Summa jāizsaka tajā valūtā, kuru norādījusi iniciējošā puse.".

    Naudas summa, ko paredzēts pārvietot starp debitoru un kreditoru pirms maksu ieturēšanas. Summa jāizsaka tajā valūtā, kuru norādījusi iniciējošā puse.  

59. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
60. Laukā Nosaukums ierakstiet "End2EndID". 
61. Laukā Vienuma tips atlasiet "String".
62. Noklikšķiniet uz Pievienot.
63. Laukā Apraksts ievadiet “Unikālais identifikators, kuru piešķīrusi iniciējošā puse. Šis identifikators tiek nodots tālāk neizmainītā veidā visā ķēdes garumā." 
64. Laukā Nosaukums ierakstiet "PaymentModel".

    PaymentModel nosaukums sakrīt ar iepriekš definētiem maksājumu veidlapu interfeisiem.  

65. Noklikšķiniet uz Saglabāt.
66. Aizvērt lapu.

