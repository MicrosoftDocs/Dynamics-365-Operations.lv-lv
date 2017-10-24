--- 
title: "Izveidot formāta konfigurāciju elektronisko pārskatu veidošanai (ER)"
description: "Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izveidot formāta konfigurāciju Elektroniskajos pārskatos (ER)."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 04817d1f1851e43679995641e8b0ff99edaa83ad
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-format-configuration-for-electronic-reporting-er"></a>Izveidot formāta konfigurāciju elektronisko pārskatu veidošanai (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izveidot formāta konfigurāciju Elektroniskajos pārskatos (ER). Šī formāta konfigurāciju noteiks to elektronisko dokumentu formātu, kas tiek izmantoti maksājumu apstrādei. Šajā piemērā jāuzveido parauga uzņēmuma Litware, Inc. formāta konfigurācija. Lai varētu veikt šīs darbības, vispirms jāizpilda procedūrā “Modeļa kartēšana izvēlētajos datu avotos” aprakstītās darbības.


## <a name="create-a-new-format-configuration"></a>Jaunas formāta konfigurācijas izveide
1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
2. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
3. Kokā atlasiet “Maksājumi (vienkāršotais modelis)”.
4. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.
5. Laukā Jauns ievadiet "Formāts pamatojoties uz datu modeli PaymentModel".
6. Laukā Nosaukums ierakstiet "BAKS (UK fiktīvs)".
    * BAKS (UK fiktīvs)  
7. Laukā Apraksts ierakstiet "BAKS kreditora maksājuma formāts (UK fiktīvs)".
    * BAKS kreditora maksājuma formāts (UK fiktīvs)  
    * Šeit tiek automātiski ievadīts aktīvais konfigurācijas nodrošinātājs. Šis nodrošinātājs varēs uzturēt šo konfigurāciju. Citi nodrošinātāji var izmantot šo konfigurāciju, bet nevar uzturēt to.  
    * Var definēt noteiktu elektroniskā dokumenta formātu. Atstājiet šo lauku tukšu, ja vēlaties atlasīt formātu izpildes laikā.  
8. Ievadiet vai atlasiet kādu vērtību laukā Datu modelis.
9. Klikšķiniet Izveidot konfigurāciju.
    * Tika izveidota jauna konfigurācija. Melnraksta versiju var izmantot, lai saglabātu dizaina formātu elektronisko dokumentu pārvaldībai.  

## <a name="design-format-of-electronic-document"></a>Elektronisko dokumentu formāta noformēšana
1. Noklikšķiniet uz Veidotājs.
2. Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.
3. Kokā atlasiet "Vispārīgi\Fails".
4. Laukā Nosaukums ierakstiet "Xml".
    * Xml  
5. Laukā Kodēšana ierakstiet "UTF-8".
    * UTF-8  
6. Noklikšķiniet uz OK.
7. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
8. Kokā atlasiet "XML\Elements".
9. Laukā Nosaukums ierakstiet "Ziņojums".
    * Paziņojums  
10. Noklikšķiniet uz OK.
11. Koka struktūrā atlasiet zaru “Xml\Ziņojums”.
12. Noklikšķiniet uz Pievienot elementu.
13. Laukā Nosaukums ievadiet "ProcessingDate".
    * ProcessingDate  
14. Noklikšķiniet uz OK.
15. Noklikšķiniet uz Pievienot elementu.
16. Laukā Nosaukums ierakstiet "MessageId".
    * MessageId  
17. Noklikšķiniet uz OK.
18. Noklikšķiniet uz Pievienot elementu.
19. Laukā Nosaukums ierakstiet "Maksājumi".
    * Maksājumi  
20. Noklikšķiniet uz OK.
21. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi”.
22. Noklikšķiniet uz Pievienot elementu.
23. Laukā Nosaukums ierakstiet "Krājums".
    * Objekts  
24. Noklikšķiniet uz OK.
25. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums”.
26. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
27. Kokā atlasiet "XML\Atribūts".
28. Laukā Nosaukums ierakstiet "Id".
    * ID  
29. Noklikšķiniet uz OK.
30. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
31. Kokā atlasiet "XML\Elements".
32. Laukā Nosaukums ierakstiet "Kreditors".
    * Kreditors  
33. Noklikšķiniet uz OK.
34. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors”.
35. Noklikšķiniet uz Pievienot elementu.
36. Laukā Nosaukums ierakstiet "Nosaukums".
    * Nosaukums  
37. Noklikšķiniet uz OK.
38. Noklikšķiniet uz Pievienot elementu.
39. Laukā Nosaukums ierakstiet "Banka".
    * Banka  
40. Noklikšķiniet uz OK.
41. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka”.
42. Noklikšķiniet uz Pievienot elementu.
43. Laukā Nosaukums ierakstiet "RoutingNumber".
    * RoutingNumber  
44. Noklikšķiniet uz OK.
45. Noklikšķiniet uz Pievienot elementu.
46. Laukā Nosaukums ierakstiet "AccountNumber".
    * Konta numurs  
47. Noklikšķiniet uz OK.
48. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors”.
49. Noklikšķiniet uz Kopēt.
50. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums”.
51. Noklikšķiniet uz Ielīmēt.
52. Laukā Nosaukums ierakstiet "Maksātājs".
    * Maksātājs  
53. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums”.
54. Noklikšķiniet uz Pievienot elementu.
55. Laukā Nosaukums ierakstiet "Valūta".
    * Valūta  
56. Noklikšķiniet uz Labi.
57. Noklikšķiniet uz Pievienot elementu.
58. Laukā Nosaukums ierakstiet "Apraksts".
    * Apraksts  
59. Noklikšķiniet uz Labi.
60. Noklikšķiniet uz Pievienot elementu.
61. Laukā Nosaukums ierakstiet "TransDate".
    * Darbības datums  
62. Noklikšķiniet uz Labi.
63. Noklikšķiniet uz Pievienot elementu.
64. Laukā Nosaukums ierakstiet "Summa".
    * Summa  
65. Noklikšķiniet uz Labi.

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>Formātā komponentu sagatavošana kartēšanai datu modeļa elementos
1. Koka struktūrā atlasiet zaru “Xml\Ziņojums\ProcessingDate”.
2. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
3. Koka struktūrā atlasiet zaru “Teksts\DateTime”.
4. Laukā Formāts ierakstiet "gggg-MM-dd".
    * gggg-MM-dd  
5. Noklikšķiniet uz OK.
6. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\TransDate”.
7. Noklikšķiniet uz Pievienot DateTime.
8. Laukā Formāts ierakstiet "gggg-MM-dd".
    * gggg-MM-dd  
9. Laukā DateTime tips atlasiet “Datums”.
10. Noklikšķiniet uz OK.
11. Koka struktūrā atlasiet zaru “Xml\Ziņojums\MessageId”.
12. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
13. Kokā atlasiet elementu “Teksts\Virkne”.
14. Noklikšķiniet uz Labi.
15. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Nosaukums”.
16. Noklikšķiniet uz Pievienot virkni.
17. Noklikšķiniet uz Labi.
18. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka\RoutingNumber”.
19. Noklikšķiniet uz Pievienot virkni.
20. Noklikšķiniet uz Labi.
21. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka\AccountNumber”.
22. Noklikšķiniet uz Pievienot virkni.
23. Noklikšķiniet uz Labi.
24. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Nosaukums”.
25. Noklikšķiniet uz Pievienot virkni.
26. Noklikšķiniet uz Labi.
27. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Banka\RoutingNumber”.
28. Noklikšķiniet uz Pievienot virkni.
29. Noklikšķiniet uz Labi.
30. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Banka\AccountNumber”.
31. Noklikšķiniet uz Pievienot virkni.
32. Noklikšķiniet uz Labi.
33. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Valūta”.
34. Noklikšķiniet uz Pievienot virkni.
35. Noklikšķiniet uz Labi.
36. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Apraksts”.
37. Noklikšķiniet uz Pievienot virkni.
38. Noklikšķiniet uz Labi.
39. Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Summa”.
40. Noklikšķiniet uz Pievienot virkni.
41. Noklikšķiniet uz Labi.
42. Noklikšķiniet uz Saglabāt.
43. Aizvērt lapu.


