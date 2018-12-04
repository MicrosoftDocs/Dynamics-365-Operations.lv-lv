--- 
title: "ER formāta konfigurēšana, lai veiktu uzskaiti un summēšanu (2. daļa. Aprēķinu konfigurēšana)"
description: "Tālāk aprakstītajos soļos ir izskaidrots, kā sistēmas lietotājs, kam ir piešķirta administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektronisko pārskatu sagatavošanas (ER) formātu, lai veiktu uzskaiti un summēšanu, izmantojot jau izveidotās teksta izvades datus."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 4ef657b13bc1f7f4a84676821e4175ace32c069a
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2018

---
# <a name="er-configure-format-to-do-counting-and-summing-part-2-configure-computations"></a>ER konfigurēt formātu, lai veiktu uzskaiti un summēšanu (2. daļa: Konfigurēt aprēķināšanas)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tālāk aprakstītajos soļos ir izskaidrots, kā sistēmas lietotājs, kam ir piešķirta administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektronisko pārskatu sagatavošanas (ER) formātu, lai veiktu uzskaiti un summēšanu, izmantojot jau izveidotās teksta izvades datus. Šīs darbības var veikt jebkurā uzņēmumā.

Lai veiktu šīs darbības, vispirms ir jāpabeidz procedūras “ER konfigurēt formātu, lai veiktu uzskaiti un summēšanu (1. daļa: Izveidot formātu)” darbības.

Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a>Izveidot formāta konfigurāciju, lai pievienotu uzskaites un summēšanas detalizētus datus
1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
2. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
3. Kokā struktūrā izvērsiet 'Intrastat model'.
4. Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)'.
    * Pieņemsim, ka jums ir jāpielāgo korporācijas Microsoft nodrošinātais formāts, pievienojot rindas ar kopsavilkuma datiem Intrastat pārskata beigās. Lai to izdarītu un varētu veikt izmaiņas, no Microsoft instances ir jāiegūst sava Intrastat konfigurācijas instance.  
5. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.
6. Laukā Jauns ievadiet 'Derive from Name: Intrastat (DE), Microsoft'.
7. Laukā Nosaukums ierakstiet 'Intrastat (DE) with counting & summing'.
8. Klikšķiniet Izveidot konfigurāciju.

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a>Konfigurēt šo pārskatu, lai veiktu uzskaiti un summēšana, izmantojot izejas datus
1. Noklikšķiniet uz Veidotājs.
2. Laukā Apkopot izvades datus atlasiet Jā.
    * Šis karodziņš aktivizē izpildes laikā izvades datu apkopošanas procesu, kas paredzēts Intrastat failu izveidei.  
    * Tas ir jāatkārto dažādiem Intrastat virzieniem, tāpēc pievienojiet īpašo modeļa uzskaitījumu šīs formāta konfigurācijas datu avotu sarakstam.  
3. Noklikšķiniet uz cilnes Kartēšana.
4. Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.
5. Koka struktūrā atlasiet 'Data model\Enumeration '.
6. Laukā Nosaukums ierakstiet 'Direction'.
7. Ievadiet vai atlasiet vērtību laukā Modeļa uzskaitījums.
    * Atlasiet vērtību Virziens.  
8. Noklikšķiniet uz OK.
9. Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.
10. Kokā atlasiet Funkcijas\Aprēķinātais lauks.
11. Laukā Nosaukums ierakstiet '$BlockName'.
12. Noklikšķiniet uz Rediģēt formulu.
13. Laukā Formula ievadiet '"block"'.
14. Noklikšķiniet uz Saglabāt.
15. Aizvērt lapu.
16. Noklikšķiniet uz OK.
17. Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.
18. Kokā atlasiet Funkcijas\Aprēķinātais lauks.
19. Laukā Nosaukums ierakstiet '$RecName'.
20. Noklikšķiniet uz Rediģēt formulu.
21. Laukā Formula ievadiet "record"'.
22. Noklikšķiniet uz Saglabāt.
23. Aizvērt lapu.
24. Noklikšķiniet uz OK.
25. Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.
26. Kokā atlasiet Funkcijas\Aprēķinātais lauks.
27. Laukā Nosaukums ierakstiet '$InvName'.
28. Noklikšķiniet uz Rediģēt formulu.
29. Laukā Formula ievadiet '"InvoicedAmountEUR"'.
30. Noklikšķiniet uz Saglabāt.
31. Aizvērt lapu.
32. Noklikšķiniet uz OK.
33. Koka struktūrā atlasiet 'Intrastat\Data'.
34. Noklikšķiniet uz lauka Apkopoto datu atslēgas nosaukums pogas Rediģēt
35. Noklikšķiniet uz Pievienot datu avotu.
    * $BlockName  
36. Noklikšķiniet uz Saglabāt.
37. Aizvērt lapu.
38. Noklikšķiniet uz lauka Apkopoto datu atslēgas vērtība pogas Rediģēt.
39. Laukā Formula ievadiet “IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")”.
    * IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")  
40. Noklikšķiniet uz Saglabāt.
41. Aizvērt lapu.
    * Saskaitiet šīs secības līnijas. Rezultāti tiks izmantoti ar nosaukumu “bloķēt” atsevišķi dažādiem virzieniem. Vērtība “Importēt” tiks izmantota visām ienākošajām Intrastat transakcijām. Vērtība “Eksportēt” tiks izmantota visām Intrastat nosūtītajām transakcijām. Uzskatiet to par virtuālu Excel izklājlapu. Katra transakcijas rindas, kur pirmā kolonna ir “bloķēt”, tiek aizpildīta ar attiecīgi ar vērtību “Importēt” un “Eksportēt”.  
42. Kokā struktūrā izvērsiet Intrastat\Data: Sequence'.
43. Koka struktūrā atlasiet 'Intrastat\Data: Sequence\Arrivals?'.
44. Noklikšķiniet uz lauka Apkopoto datu atslēgas nosaukums pogas Rediģēt.
    * Saskaitiet šīs secības līnijas. Rezultāti tiks saglabāti atmiņā ar vārdu “ierakstīt”.  
45. Koka struktūrā atlasiet '$RecName'.
46. Noklikšķiniet uz Pievienot datu avotu.
47. Noklikšķiniet uz Saglabāt.
48. Aizvērt lapu.
49. Noklikšķiniet uz lauka Apkopoto datu atslēgas vērtība pogas Rediģēt.
50. Laukā Formula ievadiet “Intrastat.CommodityRecord.CommodityCode”.
51. Noklikšķiniet uz Saglabāt.
52. Aizvērt lapu.
    * Saskaitiet šīs secības līnijas. Rezultāti tiks izmantoti ar nosaukumu “ierakstīt” atsevišķi dažādiem preces kodiem. Uzskatiet to par virtuālu Excel izklājlapu. Katra transakcijas rinda, kur pirmā kolonna ir “bloķēt”, tiek aizpildīta ar attiecīgi ar vērtību “Importēt” un “Eksportēt” un otrais bloks “ierakstīt” tiek aizpildīts ar preces koda vērtību.  
53. Koka struktūrā atlasiet 'Intrastat\Data: Sequence\Dispatches?'.
54. Noklikšķiniet uz lauka Apkopoto datu atslēgas nosaukums pogas Rediģēt
55. Koka struktūrā atlasiet '$RecName'.
56. Noklikšķiniet uz Pievienot datu avotu.
57. Noklikšķiniet uz Saglabāt.
58. Aizvērt lapu.
59. Noklikšķiniet uz lauka Apkopoto datu atslēgas vērtība pogas Rediģēt.
60. Laukā Formula ievadiet “Intrastat.CommodityRecord.CommodityCode”.
61. Klikšķiniet Saglabāt.
62. Aizvērt lapu.
63. Kokā struktūrā izvērsiet 'Intrastat\Data: Sequence\Dispatches: Sequence?'.
64. Kokā struktūrā izvērsiet 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.
65. Noklikšķiniet uz cilnes Formāts.
66. Koka struktūrā atlasiet 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.
67. Noklikšķiniet uz cilnes Kartēšana.
68. Noklikšķiniet uz lauka Apkopoto datu atslēgas nosaukums pogas Rediģēt.
69. Koka struktūrā atlasiet '$InvName'.
70. Noklikšķiniet uz Pievienot datu avotu.
71. Noklikšķiniet uz Saglabāt.
72. Aizvērt lapu.
    * Aprēķiniet šīs secības rindas rēķinā iekļauto summu vērtību. Rezultāti tiks izmantoti ar nosaukumu “InvoicedAmountEUR” atsevišķi dažādiem Intrastat virzieniem un preces kodiem. Uzskatiet to par virtuālu Excel izklājlapas izveidi. Katra transakcijas rindas, kur pirmā kolonna ir “bloķēt”, tiek aizpildīta ar attiecīgi ar vērtību “Importēt” un “Eksportēt”. Otrs bloks “ierakstīt” tiek aizpildīts ar preces koda vērtību un trešā kolonna “InvoicedAmountEUR” tiek aizpildīta ar rēķina summas vērtību.  
73. Kokā struktūrā izvērsiet 'Intrastat\Data\Arrivals?'.
74. Koka struktūrā izvērsiet 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.
75. Noklikšķiniet uz cilnes Formāts.
76. Koka struktūrā atlasiet 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.
77. Noklikšķiniet uz cilnes Kartēšana.
78. Noklikšķiniet uz lauka Apkopoto datu atslēgas nosaukums pogas Rediģēt.
79. Koka struktūrā atlasiet '$InvName'.
80. Noklikšķiniet uz Pievienot datu avotu.
81. Noklikšķiniet uz Saglabāt.
82. Aizvērt lapu.
83. Noklikšķiniet uz Saglabāt.
84. Aizvērt lapu.


