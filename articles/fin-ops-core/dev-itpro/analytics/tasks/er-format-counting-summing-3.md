---
title: ER formāta konfigurēšana, lai veiktu uzskaiti un summēšanu (3. daļa. Aprēķinu izmantošana izvades datu izveidei)
description: Šajā tēmā ir aprakstīts, kā konfigurēt elektronisko pārskatu formātu, lai to skaitītu un summētu, pamatojoties uz jau ģenerētā teksta izvades datiem. (3. daļa)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a69dd28051d8e98643eb95c663525075bed8dec
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092976"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a>ER formāta konfigurēšana, lai veiktu uzskaiti un summēšanu (3. daļa. Aprēķinu izmantošana izvades datu izveidei)

[!include [banner](../../includes/banner.md)]

Tālāk aprakstītajos soļos ir izskaidrots, kā sistēmas lietotājs, kam ir piešķirta administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektronisko pārskatu sagatavošanas (ER) formātu, lai veiktu uzskaiti un summēšanu, izmantojot jau izveidotās teksta izvades datus. Šīs darbības var veikt jebkurā uzņēmumā.

Lai veiktu šīs darbības, vispirms ir jāpabeidz procedūras "ER konfigurēt formātu, lai veiktu uzskaiti un summēšanu (2. daļa: Konfigurēt aprēķinus)" darbības.

Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.


## <a name="configure-this-report-to-use-counting-and-summing-info"></a>Konfigurēt šo pārskatu, lai varētu izmantot uzskaites un summēšanas datus
1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
2. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
3. Kokā struktūrā izvērsiet 'Intrastat model'.
4. Koka struktūrā izvērsiet 'Intrastat model\Intrastat (DE)'.
5. Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.
6. Noklikšķiniet uz Veidotājs.
7. Noklikšķiniet uz cilnes Kartēšana.
8. Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.
    * Pievienojiet jaunu datu avotu, lai iegūtu atmiņā saglabāto bloku sarakstu.  
9. Kokā atlasiet Funkcijas\Aprēķinātais lauks.
10. Laukā Nosaukums ierakstiet '$BlocksList'.
    * $BlocksList  
11. Noklikšķiniet uz Rediģēt formulu.
12. Koka struktūrā atlasiet 'Data collection functions\COLLECTEDLIST'.
13. Noklikšķiniet uz Pievienot funkciju.
14. Noklikšķiniet uz Pievienot datu avotu.
15. Laukā Formula ievadiet 'COLLECTEDLIST('$BlockName', '.
    * COLLECTEDLIST('$BlockName',  
16. Laukā Formula ievadiet 'COLLECTEDLIST('$BlockName', "*")'.
    * COLLECTEDLIST('$BlockName', "*")  
17. Klikšķiniet Saglabāt.
    * Simbols "*" norāda, ka visi bloki tiks iekļauti šī ieraksta sarakstā.  
18. Aizvērt lapu.
19. Noklikšķiniet uz OK.
20. Noklikšķiniet uz cilnes Formāts.
21. Koka struktūrā atlasiet 'Intrastat\Data'.
22. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
23. Koka struktūrā atlasiet 'Text\Sequence'.
24. Laukā Nosaukums ierakstiet 'Totals by blocks'.
    * Kopsummas pēc blokiem  
25. Laukā Īpašas rakstzīmes atlasiet 'New line - Windows (CR LF)'.
26. Noklikšķiniet uz Labi.
27. Koka struktūrā atlasiet 'Intrastat\Data\Totals by blocks'.
28. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
29. Kokā atlasiet elementu “Teksts\Virkne”.
30. Laukā Nosaukums ierakstiet 'Block code'.
    * Bloka kods  
31. Noklikšķiniet uz OK.
32. Noklikšķiniet uz Pievienot virkni.
33. Laukā Nosaukums ierakstiet 'Lines counting'.
    * Uzskaites rindas  
34. Noklikšķiniet uz OK.
35. Noklikšķiniet uz Pievienot virkni.
36. Laukā Nosaukums ierakstiet 'Total amount'.
    * Kopējā summa  
37. Noklikšķiniet uz OK.
38. Noklikšķiniet uz cilnes Kartēšana.
39. Koka struktūrā atlasiet '$BlocksList'.
40. Noklikšķiniet uz Saistīt.
    * Izveidojiet kopsavilkuma rindu katram atmiņā saglabātajam blokam.  
41. Noklikšķiniet uz cilnes Formāts.
42. Koka struktūrā atlasiet 'Intrastat\Data\Totals by blocks\Block code'.
43. Noklikšķiniet uz cilnes Kartēšana.
44. Noklikšķiniet uz Rediģēt formulu.
45. Laukā Formula ievadiet '"Block id: " & '.
    * "Block id: " &  
46. Koka struktūrā izvērsiet sadaļu '$BlocksList'.
47. Koka struktūrā atlasiet '$BlocksList\Value'.
48. Noklikšķiniet uz Pievienot datu avotu.
49. Noklikšķiniet uz Saglabāt.
50. Aizvērt lapu.
51. Noklikšķiniet uz cilnes Formāts.
52. Koka struktūrā atlasiet 'Intrastat\Data\Totals by blocks\Lines counting'.
53. Noklikšķiniet uz cilnes Kartēšana.
54. Noklikšķiniet uz Rediģēt formulu.
    * Izveidojiet rindu skaita izvadi katram pārskatā esošajam blokam.  
55. Laukā Formula ievadiet '"Number of lines in this block: " & '.
    * "Number of lines in this block: " &  
56. Laukā Formula ievadiet '"Number of lines in this block: " & TEXT('.
    * "Number of lines in this block: " & TEXT(  
57. Koka struktūrā atlasiet 'Data collection functions\COUNTIFS'.
58. Noklikšķiniet uz Pievienot funkciju.
59. Noklikšķiniet uz Pievienot datu avotu.
60. Laukā Formula ievadiet '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.
    * "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',  
61. Koka struktūrā izvērsiet sadaļu '$BlocksList'.
62. Koka struktūrā atlasiet '$BlocksList\Value'.
63. Noklikšķiniet uz Pievienot datu avotu.
64. Laukā Formula ievadiet '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.
    * "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,  
65. Koka struktūrā atlasiet '$RecName'.
66. Noklikšķiniet uz Pievienot datu avotu.
67. Laukā Formula ievadiet '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))'.
    * "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))  
68. Noklikšķiniet uz Saglabāt.
69. Aizvērt lapu.
70. Noklikšķiniet uz cilnes Formāts.
71. Koka struktūrā atlasiet 'Intrastat\Data\Totals by blocks\Total amount'.
72. Noklikšķiniet uz cilnes Kartēšana.
73. Noklikšķiniet uz Rediģēt formulu.
    * Izveidojiet izvadi, kas būs visu šajā pārskatā esošo bloku rēķinā iekļauto summu kopsumma.  
74. Laukā Formula ievadiet '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))'.
    * "Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))  
75. Noklikšķiniet uz Saglabāt.
76. Aizvērt lapu.
77. Noklikšķiniet uz Saglabāt.
78. Aizvērt lapu.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]