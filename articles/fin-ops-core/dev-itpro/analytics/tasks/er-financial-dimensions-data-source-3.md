---
title: ER finanšu dimensijas, ko izmanto kā datu avotu (3. daļa. Pārskata izkārtošana)
description: Šajā tēmā ir aprakstīts, kā konfigurēt elektronisko pārskatu (ER) modeli, lai finanšu dimensijas izmantotu kā datu avotu ER pārskatiem. (3. daļa)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a3b9a8b5775d2001f3384480e2f9593f2dfa8b1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752416"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a>ER finanšu dimensijas, ko izmanto kā datu avotu (3. daļa. Pārskata izkārtošana)

[!include [banner](../../includes/banner.md)]

Tālāk ir paskaidrots kā lietotājs, kam piešķirta loma sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem. Šīs darbības var veikt jebkurā uzņēmumā.

Lai izpildītu šos soļus, vispirms ir jāpabeidz soļi, kas aprakstīti procedūrā "ER Finanšu dimensijas, ko izmanto kā datu avotu" (2. daļa: Modeļa kartēšana).


## <a name="design-a-report-to-present-financial-dimensions"></a>Izveidojiet pārskatu, lai parādītu finanšu dimensijas
1. Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.
2. Koka struktūrā atlasiet 'Finanšu dimensiju parauga modelis'.
3. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.
4. Laukā Jauns ievadiet "Formāts pamatojoties uz datu modeli 'Finanšu dimensiju parauga modelis'.
    * Izmantojiet iepriekš izveidoto modeli kā jaunā pārskata datu avotu.  
5. Laukā Nosaukums ierakstiet 'Virsgrāmatas žurnāla pārskats'.
6. Laukā Datu modeļa definīcija atlasiet Ieraksts.
7. Klikšķiniet Izveidot konfigurāciju.
8. Noklikšķiniet uz Veidotājs.
9. Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.
10. Kokā atlasiet "XML\Elements".
11. Laukā Nosaukums ierakstiet 'Sakne'.
12. Noklikšķiniet uz Labi.
13. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
14. Kokā atlasiet "XML\Atribūts".
15. Laukā Nosaukums ierakstiet "Uzņēmums".
16. Noklikšķiniet uz Labi.
17. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
18. Kokā atlasiet "XML\Elements".
19. Laukā Nosaukums ierakstiet 'Žurnāls'.
20. Noklikšķiniet uz Labi.
21. Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements'.
22. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
23. Kokā atlasiet "XML\Atribūts".
24. Laukā Nosaukums ierakstiet 'Partija'.
25. Noklikšķiniet uz Labi.
26. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
27. Kokā atlasiet "XML\Elements".
28. Laukā Nosaukums ierakstiet 'Darbība'.
29. Noklikšķiniet uz Labi.
30. Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements'.
31. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
32. Kokā atlasiet "XML\Atribūts".
33. Laukā Nosaukums ierakstiet 'Dokuments'.
34. Noklikšķiniet uz OK.
35. Noklikšķiniet uz Pievienot atribūtu.
36. Laukā Nosaukums ierakstiet 'Datums'.
37. Noklikšķiniet uz OK.
38. Noklikšķiniet uz Pievienot atribūtu.
39. Laukā Nosaukums ierakstiet "Valūta".
40. Noklikšķiniet uz OK.
41. Noklikšķiniet uz Pievienot atribūtu.
42. Laukā Nosaukums ierakstiet 'Dt'.
43. Noklikšķiniet uz OK.
44. Noklikšķiniet uz Pievienot atribūtu.
45. Laukā Nosaukums ierakstiet 'Ct'.
46. Noklikšķiniet uz OK.
47. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
48. Kokā atlasiet "XML\Elements".
49. Laukā Nosaukums ierakstiet 'Dimensijas'.
50. Noklikšķiniet uz Labi.
51. Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dimensija: XML elements'.
52. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
53. Kokā atlasiet "XML\Atribūts".
54. Laukā Nosaukums ierakstiet 'Kods'.
55. Noklikšķiniet uz OK.
56. Noklikšķiniet uz Pievienot atribūtu.
57. Laukā Nosaukums ierakstiet 'Vērtība'.
58. Noklikšķiniet uz OK.
59. Noklikšķiniet uz Pievienot atribūtu.
60. Laukā Nosaukums ierakstiet 'Desc'.
61. Noklikšķiniet uz Labi.
![ER operāciju veidotāja lapa](../media/er-financial-dimensions-guides-format1.png)

## <a name="map-report-elements-to-data-sources"></a>Kartējiet pārskata elementus datu avotiem
1. Noklikšķiniet uz cilnes Kartēšana.
2. Kokā izvērsiet 'modelis: datu modelis Finanšu dimensiju parauga modelis'.
3. Kokā izvērsiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts'.
4. Kokā izvērsiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Darbība: Ierakstu saraksts'.
5. Kokā izvērsiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Darbība: Ierakstu saraksts\Dimensiju dati: Ierakstu saraksts'.
6. Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dimensijas: XML elements\Desc: XML atribūts'.
7. Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Darbība: Ierakstu saraksts\Dimensiju dati: Ierakstu saraksts\Apraksts: Virkne'.
8. Noklikšķiniet uz Saistīt.
9. Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dimensijas: XML elements\Vērtība: XML atribūts'.
10. Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Darbība: Ierakstu saraksts\Dimensiju dati: Ierakstu saraksts\Kods: Virkne'.
11. Noklikšķiniet uz Saistīt.
12. Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dimensijas: XML elements\Kods: XML atribūts'.
13. Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Darbība: Ierakstu saraksts\Dimensiju dati: Ierakstu saraksts\Nosaukums: Virkne'.
14. Noklikšķiniet uz Saistīt.
15. Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Darbība: Ierakstu saraksts\Dimensiju dati: Ierakstu saraksts'.
16. Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dimensija: XML elements'.
17. Noklikšķiniet uz Saistīt.
18. Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Ct: XML atribūts'.
19. Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Kredīts: Reāls'.
20. Noklikšķiniet uz Saistīt.
21. Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dt: XML atribūts'.
22. Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Debets: Reāls'.
23. Noklikšķiniet uz Saistīt.
24. Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Valūta: XML atribūts'.
25. Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Valūta: Virkne'.
26. Noklikšķiniet uz Saistīt.
27. Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Datums: XML atribūts'.
28. Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Datums: Datums'.
29. Noklikšķiniet uz Saistīt.
30. Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dokuments: XML atribūts'.
31. Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Dokuments: Virkne'.
32. Noklikšķiniet uz Saistīt.
33. Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements'.
34. Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Darbība: Ierakstu saraksts'.
35. Noklikšķiniet uz Saistīt.
36. Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Partija: XML atribūts'.
37. Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Partija: Virkne'.
38. Noklikšķiniet uz Saistīt.
39. Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements'.
40. Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts'.
41. Noklikšķiniet uz Saistīt.
42. Kokā atlasiet 'Sakne: XML elements\Uzņēmums: XML atribūts'.
43. Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Uzņēmums: Virkne'.
44. Noklikšķiniet uz Saistīt.
45. Klikšķiniet Saglabāt.
46. Aizvērt lapu.
![ER operāciju veidotāja lapa](../media/er-financial-dimensions-guides-format2.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]