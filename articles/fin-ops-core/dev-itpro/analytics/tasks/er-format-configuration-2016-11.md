---
title: ER Izveidot formāta konfigurāciju (2016. gada novembris)
description: Šajā tēmā skaidrots, kā izveidot formāta konfigurāciju elektroniskajiem pārskatiem (ER).
author: NickSelin
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9404d1e242c83d2103d1f24c42589c33b9f57f02
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092254"
---
# <a name="er-create-a-format-configuration-november-2016"></a>ER Izveidot formāta konfigurāciju (2016. gada novembris)

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā lietotājs Sistēmas administratora vai Elektronisko pārskatu izstrādātāja lomā var izveidot Elektroniskā pārskata (EK) formāta konfigurāciju. Šī formāta konfigurāciju noteiks to elektronisko dokumentu formātu, kas tiek izmantoti maksājumu apstrādei. Šajā piemērā jāuzveido parauga uzņēmuma Litware, Inc. formāta konfigurācija. Lai varētu veikt šīs darbības, vispirms jāizpilda procedūrā "Modeļa kartēšana izvēlētajos datu avotos" aprakstītās darbības.


## <a name="create-a-new-format-configuration"></a>Jaunas formāta konfigurācijas izveide
1. Pārejiet uz sadaļu **Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana**.
2. Noklikšķiniet uz **Pārskatu veidošanas konfigurācijas**.
3. Kokā atlasiet **Maksājumi (vienkāršotais modelis)**.
4. Noklikšķiniet uz **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu.

 > [!NOTE]
 > Ja neredzat opciju **Izveidot konfigurāciju**, ir jāiespējo noformēšanas režīms lapā **Elektronisko pārskatu veidošanas parametri**. 
 
5. Laukā **Jauns** ievadiet **Format based on data model PaymentModel**.
6. Laukā **Nosaukums** ierakstiet **BAKS (UK fiktīvs)**.
7. Laukā **Apraksts** ierakstiet **BAKS kreditora maksājuma formāts (UK fiktīvs)**.
    * Šeit tiek automātiski ievadīts aktīvais konfigurācijas nodrošinātājs. Šis nodrošinātājs varēs uzturēt šo konfigurāciju. Citi nodrošinātāji var izmantot šo konfigurāciju, bet nevar uzturēt to.  
    * Var definēt noteiktu elektroniskā dokumenta formātu. Atstājiet šo lauku tukšu, ja vēlaties atlasīt formātu izpildes laikā.  
8. Ievadiet vai atlasiet kādu vērtību laukā **Datu modeļa definīcija**.
9. Klikšķiniet **Izveidot konfigurāciju**. Tika izveidota jauna konfigurācija. Melnraksta versiju var izmantot, lai saglabātu dizaina formātu elektronisko dokumentu pārvaldībai.  

## <a name="design-the-format-of-an-electronic-document"></a>Elektroniskā dokumenta formāta noformēšana
1. Noklikšķiniet uz **Veidotājs**.
2. Noklikšķiniet uz **Pievienot sakni**, lai atvērtu nolaižamo dialoglodziņu.
3. Kokā atlasiet **Vispārīgi\Fails**.
4. Laukā **Nosaukums** ierakstiet **Xml**.
5. Laukā **Kodēšana** ierakstiet **UTF-8**.
6. Noklikšķiniet uz **Labi**.
7. Noklikšķiniet uz **Pievienot**.
8. Kokā atlasiet **XML\Elements**.
9. Laukā **Nosaukums** ierakstiet **Ziņojums**.
10. Noklikšķiniet uz **Labi**.
11. Kokā atlasiet **Xml\Ziņojums**.
12. Noklikšķiniet uz **Pievienot elementu**.
13. Laukā **Nosaukums** ievadiet **ProcessingDate**.
14. Noklikšķiniet uz **Labi**.
15. Noklikšķiniet uz **Pievienot elementu**.
16. Laukā Nosaukums ierakstiet **MessageId**.
17. Noklikšķiniet uz **Labi**.
18. Noklikšķiniet uz **Pievienot elementu**.
19. Laukā **Nosaukums** ierakstiet **Maksājumi**.
20. Noklikšķiniet uz **Labi**.
21. Kokā atlasiet **Xml\Ziņojums\Maksājumi**.
22. Noklikšķiniet uz **Pievienot elementu**.
23. Laukā **Nosaukums** ierakstiet **Krājums**.
24. Noklikšķiniet uz **Labi**.
25. Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums**.
26. Noklikšķiniet uz **Pievienot**.
27. Kokā atlasiet **XML\Atribūts**.
28. Laukā Nosaukums ierakstiet **Id**.
29. Noklikšķiniet uz **Labi**.
30. Noklikšķiniet uz **Pievienot**.
31. Kokā atlasiet **XML\Elements**.
32. Laukā Nosaukums ierakstiet **Kreditors**.
33. Noklikšķiniet uz **Labi**.
34. Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Kreditors**.
35. Noklikšķiniet uz **Pievienot elementu**.
36. Laukā Nosaukums ierakstiet **Nosaukums**.
37. Noklikšķiniet uz **Labi**.
38. Noklikšķiniet uz **Pievienot elementu**.
39. Laukā **Nosaukums** ierakstiet **Banka**.
40. Noklikšķiniet uz **Labi**.
41. Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka**.
42. Noklikšķiniet uz **Pievienot elementu**.
43. Laukā **Nosaukums** ierakstiet **RoutingNumber**.
44. Noklikšķiniet uz **Labi**.
45. Noklikšķiniet uz **Pievienot elementu**.
46. Laukā **Nosaukums** ierakstiet **AccountNumber**.
47. Noklikšķiniet uz **Labi**.
48. Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Kreditors**.
49. Noklikšķiniet uz **Kopēt**.
50. Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums**.
51. Noklikšķiniet uz **Ielīmēt**.
52. Laukā **Nosaukums** ierakstiet **Maksātājs**.
53. Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums**.
54. Noklikšķiniet uz **Pievienot elementu**.
55. Laukā **Nosaukums** ierakstiet **Valūta**.
56. Noklikšķiniet uz **Labi**.
57. Noklikšķiniet uz **Pievienot elementu**.
58. Laukā **Nosaukums** ierakstiet **Apraksts**.
59. Noklikšķiniet uz **Labi**.
60. Noklikšķiniet uz **Pievienot elementu**.
61. Laukā Nosaukums ierakstiet **TransDate**.
62. Noklikšķiniet uz **Labi**.
63. Noklikšķiniet uz **Pievienot elementu**.
64. Laukā Nosaukums ierakstiet **Summa**.
65. Noklikšķiniet uz **Labi**.

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>Formātā komponentu sagatavošana kartēšanai datu modeļa elementos
1. Kokā atlasiet **Xml\Ziņojums\ProcessingDate**.
2. Noklikšķiniet uz **Pievienot**, lai atvērtu nolaižamo dialoglodziņu.
3. Kokā atlasiet **Teksts\DateTime**.
4. Laukā **Formāts** ierakstiet **gggg-MM-dd**.
5. Noklikšķiniet uz **Labi**.
6. Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\TransDate**.
7. Noklikšķiniet uz **Pievienot DateTime**.
8. Laukā **Formāts** ierakstiet **gggg-MM-dd**.
9. Tipa **DateTime** laukā atlasiet **Datums**.
10. Noklikšķiniet uz **Labi**.
11. Kokā atlasiet **Xml\Ziņojums\MessageId**.
12. Noklikšķiniet uz **Pievienot**, lai atvērtu nolaižamo dialoglodziņu.
13. Kokā atlasiet **Teksts\Virkne**.
14. Noklikšķiniet uz **Labi**.
15. Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Nosaukums**.
16. Noklikšķiniet uz **Pievienot virkni**.
17. Noklikšķiniet uz **Labi**.
18. Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka\RoutingNumber**.
19. Noklikšķiniet uz **Pievienot virkni**.
20. Noklikšķiniet uz **Labi**.
21. Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka\AccountNumber**.
22. Noklikšķiniet uz **Pievienot virkni**.
23. Noklikšķiniet uz **Labi**.
24. Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Nosaukums**.
25. Noklikšķiniet uz **Pievienot virkni**.
26. Noklikšķiniet uz **Labi**.
27. Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Banka\RoutingNumber**.
28. Noklikšķiniet uz **Pievienot virkni**.
29. Noklikšķiniet uz **Labi**.
30. Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Banka\AccountNumber**.
31. Noklikšķiniet uz **Pievienot virkni**.
32. Noklikšķiniet uz **Labi**.
33. Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Valūta**.
34. Noklikšķiniet uz **Pievienot virkni**.
35. Noklikšķiniet uz **Labi**.
36. Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Apraksts**.
37. Noklikšķiniet uz **Pievienot virkni**.
38. Noklikšķiniet uz **Labi**.
39. Kokā atlasiet **Xml\Ziņojums\Maksājumi\Krājums\Summa**.
40. Noklikšķiniet uz **Pievienot virkni**.
41. Noklikšķiniet uz **Labi**.
42. Noklikšķiniet uz **Saglabāt**.
43. Aizvērt lapu.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]