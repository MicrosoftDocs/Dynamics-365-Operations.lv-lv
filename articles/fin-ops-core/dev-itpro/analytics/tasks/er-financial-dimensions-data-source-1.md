---
title: ER finanšu dimensijas, kuras izmanto kā datu avotu (1. daļa. Datu modeļa noformēšana)
description: Šajā rakstā ir aprakstīts, kā konfigurēt elektronisko pārskatu (ER) modeli, lai finanšu dimensijas izmantotu kā datu avotu ER pārskatiem. (1. daļa)
author: kfend
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
ms.openlocfilehash: 053b9cf9ea6b2845bef5d95e901c1c90fac964be
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290850"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a>ER finanšu dimensijas, kuras izmanto kā datu avotu (1. daļa. Datu modeļa noformēšana)

[!include [banner](../../includes/banner.md)]

Tālāk ir paskaidrots kā sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem. Šīs darbības var veikt jebkurā uzņēmumā.

Lai izpildītu tālāk norādītās darbības, vispirms izpildiet procedūras darbības "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu".


## <a name="create-a-new-data-model"></a>Izveidot jaunu datu modeli
1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
    * Pārliecinieties, vai "Litware, Inc." ir pieejams un atzīmēts kā aktīvs.  
2. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
3. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.
4. Laukā Nosaukums ierakstiet 'Finanšu dimensiju parauga modelis'.
5. Klikšķiniet Izveidot konfigurāciju.
6. Noklikšķiniet uz Veidotājs.
7. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
8. Laukā Nosaukums ierakstiet 'Ieraksts'.
9. Noklikšķiniet uz Pievienot.
10. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
11. Laukā Nosaukums ierakstiet "Uzņēmums".
12. Noklikšķiniet uz Pievienot.
    * Pievienosim mūsu modelim jaunu ierakstu sarakstu. Šajā sarakstā tiks atklāti (visiem ER pārskatiem, kas izmanto šo modeli kā datu avotu) atlasīto finanšu dimensiju iestatījumi. Katra finanšu dimensija tiks parādīta šajā sarakstā kā ieraksts ar atbilstošiem laukiem, kas norāda dimensijas iestatījumu.  
13. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
14. Laukā Nosaukums ierakstiet 'Dimensiju iestatīšana'.
15. Laukā Vienuma tips atlasiet "Record list".
16. Noklikšķiniet uz Pievienot.
17. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
18. Laukā Nosaukums ierakstiet 'Kods'.
19. Laukā Vienuma tips atlasiet "String".
20. Noklikšķiniet uz Pievienot.
21. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
22. Laukā Nosaukums ierakstiet "Nosaukums".
23. Noklikšķiniet uz Pievienot.
24. Kokā atlasiet 'Ieraksts'.
25. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
26. Laukā Nosaukums ierakstiet 'Žurnāls'.
27. Laukā Vienuma tips atlasiet "Record list".
28. Noklikšķiniet uz Pievienot.
29. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
30. Laukā Nosaukums ierakstiet 'Partija'.
31. Laukā Vienuma tips atlasiet "String".
32. Noklikšķiniet uz Pievienot.
33. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
34. Laukā Nosaukums ierakstiet 'Darbība'.
35. Laukā Vienuma tips atlasiet "Record list".
36. Noklikšķiniet uz Pievienot.
37. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
38. Laukā Nosaukums ierakstiet 'Datums'.
39. Laukā Vienuma tips atlasiet "Date".
40. Noklikšķiniet uz Pievienot.
41. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
42. Laukā Nosaukums ierakstiet 'Debets'.
43. Laukā Vienuma tips atlasiet "Real".
44. Noklikšķiniet uz Pievienot.
45. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
46. Laukā Nosaukums ierakstiet 'Kredīts'.
47. Noklikšķiniet uz Pievienot.
48. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
49. Laukā Nosaukums ierakstiet "Valūta".
50. Laukā Vienuma tips atlasiet "String".
51. Noklikšķiniet uz Pievienot.
52. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
53. Laukā Nosaukums ierakstiet 'Dokuments'.
54. Noklikšķiniet uz Pievienot.
55. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
56. Laukā Nosaukums ierakstiet 'Dimensiju dati.
57. Laukā Vienuma tips atlasiet "Record list".
58. Noklikšķiniet uz Pievienot.
    * Pievienojām mūsu modelim jaunu ierakstu sarakstu. Šajā sarakstā tiks atklāti (visiem ER pārskatiem, kas izmanto šo modeli kā datu avotu) atlasīto finanšu dimensiju vērtības. Katra finanšu dimensija tiks parādīta šajā sarakstā kā ieraksts ar atbilstošiem laukiem, kas norāda dimensijas vērtības. Dimensijas nosaukums arī tiks iesniegts šajā ierakstā kā lauks, kas jāizmanto atlases nolūkiem, ja nepieciešams.  
59. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
60. Laukā Nosaukums ierakstiet 'Kods'.
61. Laukā Vienuma tips atlasiet "String".
62. Noklikšķiniet uz Pievienot.
63. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
64. Laukā Nosaukums ierakstiet "Apraksts".
65. Noklikšķiniet uz Pievienot.
66. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
67. Laukā Nosaukums ierakstiet "Nosaukums".
68. Noklikšķiniet uz Pievienot.
69. Noklikšķiniet uz Saglabāt.
70. Aizvērt lapu.

![EP datu modeļa veidotāja lapa.](../media/er-financial-dimensions-guides-data-model.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
