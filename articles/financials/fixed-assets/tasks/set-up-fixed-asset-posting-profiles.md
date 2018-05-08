--- 
title: "Pamatlīdzekļa grāmatošanas profilu iestatīšana"
description: "Šajā uzdevuma ceļvedī tiks iestatītas pamatlīdzekļu grāmatošanas metodes."
author: saraschi2
manager: AnnBe
ms.date: 02/24/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b9766d96d16429d0ce0864695a3157f54cad4054
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-fixed-asset-posting-profiles"></a>Pamatlīdzekļa grāmatošanas profilu iestatīšana

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā uzdevuma ceļvedī tiks iestatītas pamatlīdzekļu grāmatošanas metodes.  Tas izmanto grāmatveža lomu un demonstrācijas datus USMF juridiskajai personai.  Uzdevuma ceļvedī sniegti piemēri pamata grāmatošanas metodei, lai gan grāmatošanas metodes ir jāizveido jūsu konkrētajam kontu plānam un finanšu atskaišu prasībām.

1. Pārejiet uz sadaļu Pamatlīdzekļi > Iestatījumi > Pamatlīdzekļu grāmatošanas metodes.
2. Noklikšķiniet uz Jauns.
3. Ievadiet vērtību laukā Grāmatošanas metode.
4. Apraksta laukā ierakstiet vērtību.
    * Jums vajadzēs izveidot grāmatošanas metodi katram pamatlīdzekļu transakciju tipam, kuru izmantosit darbā ar pamatlīdzekļiem.  Šī uzdevuma ceļveža sākumā tiks apskatīts Iegādes transakcijas tips.  
5. Noklikšķiniet uz Pievienot.
6. Laukā Grāmata ievadiet vai atlasiet kādu vērtību.
    * Grupējumu lauks ļauj definēt grāmatošanas metodi tabulai (viens konts iestatīts katram pamatlīdzeklim) vai grupai (viens konts iestatīts katrai pamatlīdzekļu grupai).  Šajā uzdevuma ceļvedī vērtība būs iestatīta uz “Visi”, lai norādīto grāmatu lietotu visiem pamatlīdzekļiem.  
7. Laukā Galvenais konts norādiet vēlamās vērtības.
    * Iegādēm varat ievadīt korespondējošo kontu vai atstāt to tukšu, aizpildot to specifiskām transakcijām.    
8. Laukā Transakcijas veids atlasiet „Iegādes korekcija”.
    * Iegādes korekcijas transakcijām izmantosim tos pašus kontus, kas izmantoti iegādes transakcijām.  
9. Noklikšķiniet uz Pievienot.
10. Laukā Grāmata ievadiet vai atlasiet kādu vērtību.
11. Laukā Galvenais konts norādiet vēlamās vērtības.
    * Iegāžu korekcijām varat ievadīt korespondējošo kontu vai atstāt to tukšu, aizpildot to specifiskām transakcijām.    
12. Laukā Transakcijas veids atlasiet „Nolietojums”.
13. Noklikšķiniet uz Pievienot.
14. Laukā Grāmata ievadiet vai atlasiet kādu vērtību.
15. Laukā Galvenais konts norādiet vēlamās vērtības.
16. Laukā Korespondējošais konts norādiet vēlamās vērtības.
17. Laukā Transakcijas veids atlasiet „Nolietojuma korekcija”.
    * Nolietojuma korekcijas transakcijām izmantosim tos pašus kontus, kas izmantoti nolietojuma transakcijām.  
18. Noklikšķiniet uz Pievienot.
19. Laukā Grāmata ievadiet vai atlasiet kādu vērtību.
20. Laukā Galvenais konts norādiet vēlamās vērtības.
21. Laukā Korespondējošais konts norādiet vēlamās vērtības.
22. Laukā Transakcijas veids atlasiet „Izslēgšana — pārdošana”.
23. Noklikšķiniet uz Pievienot.
24. Laukā Grāmata ievadiet vai atlasiet kādu vērtību.
25. Laukā Galvenais konts norādiet vēlamās vērtības.
    * Izslēgšanām varat ievadīt korespondējošo kontu vai atstāt to tukšu, aizpildot to specifiskām transakcijām.  
26. Laukā Transakcijas veids atlasiet „Izslēgšana — brāķis”.
    * Izmantosim tos pašus kontus Izslēgšanas pārdošanai un Izslēgšanas brāķim.  
27. Noklikšķiniet uz Pievienot.
28. Laukā Grāmata ievadiet vai atlasiet kādu vērtību.
29. Laukā Galvenais konts norādiet vēlamās vērtības.
    * Izslēgšanām varat ievadīt korespondējošo kontu vai atstāt to tukšu, aizpildot to specifiskām transakcijām.  
30. Izvērsiet sadaļu Izslēgšana.
    * Jums ir jāiestata izslēgšanas grāmatošanas metodes gan pārdošanai, gan brāķim.  Sāksim ar izslēgšanas pārdošanas transakcijām.  
31. Noklikšķiniet uz Pievienot.
32. Laukā Grāmata ievadiet vai atlasiet kādu vērtību.
33. Laukā Grāmatot vērtību atlasiet „Iegādes vērtība”.
    * Iegādes vērtība attieksies uz iegādes un iegādes korekcijas vērtībām visus gadus.  Šiem transakciju tipiem varat definēt arī atsevišķus kontus.  
    * Varat iestatīt izslēgšanas procesu, kuru izmantot dažādiem kontiem, atkarībā no tā, vai izslēgšanas rezultātā rodas peļņa vai zaudējumi.  Šajā piemērā pārdošanas vērtības tips tiks iestatīts uz "Visi", lai izmantotu vienādus kontus visu veidu izslēgšanām.  
34. Laukā Galvenais konts norādiet vēlamās vērtības.
35. Laukā Korespondējošais konts norādiet vēlamās vērtības.
36. Noklikšķiniet uz Pievienot.
37. Laukā Grāmata ievadiet vai atlasiet kādu vērtību.
    * Laukā Grāmatot vērtību atlasiet „Nolietojums (iepriekšējie gadi)”.  
38. Laukā Galvenais konts norādiet vēlamās vērtības.
39. Laukā Korespondējošais konts norādiet vēlamās vērtības.
40. Noklikšķiniet uz Pievienot.
41. Laukā Grāmata ievadiet vai atlasiet kādu vērtību.
42. Laukā Grāmatot vērtību atlasiet „Nolietojums (šis gads)”.
43. Laukā Galvenais konts norādiet vēlamās vērtības.
44. Laukā Korespondējošais konts norādiet vēlamās vērtības.
45. Noklikšķiniet uz Pievienot.
46. Laukā Grāmata ievadiet vai atlasiet kādu vērtību.
47. Laukā Grāmatot vērtību atlasiet „Nolietojuma korekcijas (iepriekšējie gadi)”.
48. Laukā Galvenais konts norādiet vēlamās vērtības.
49. Laukā Korespondējošais konts norādiet vēlamās vērtības.
50. Noklikšķiniet uz Pievienot.
51. Laukā Grāmata ievadiet vai atlasiet kādu vērtību.
52. Laukā Grāmatot vērtību atlasiet „Nolietojuma korekcijas (šis gads)”.
53. Laukā Galvenais konts norādiet vēlamās vērtības.
54. Laukā Korespondējošais konts norādiet vēlamās vērtības.
55. Noklikšķiniet uz Pievienot.
56. Laukā Grāmata ievadiet vai atlasiet kādu vērtību.
57. Laukā Grāmatot vērtību atlasiet „Atlikusī vērtība”.
58. Laukā Galvenais konts norādiet vēlamās vērtības.
59. Laukā Korespondējošais konts norādiet vēlamās vērtības.
60. Laukā Pārdošana vai brāķis atlasiet „Brāķis”.
61. Noklikšķiniet uz Pievienot.
62. Laukā Grāmata ievadiet vai atlasiet kādu vērtību.
63. Laukā Grāmatot vērtību atlasiet „Iegādes vērtība”.
64. Laukā Galvenais konts norādiet vēlamās vērtības.
65. Laukā Korespondējošais konts norādiet vēlamās vērtības.
66. Noklikšķiniet uz Pievienot.
67. Laukā Grāmata ievadiet vai atlasiet kādu vērtību.
    * Laukā Grāmatot vērtību atlasiet „Nolietojums (iepriekšējie gadi)”.  
68. Laukā Galvenais konts norādiet vēlamās vērtības.
69. Laukā Korespondējošais konts norādiet vēlamās vērtības.
70. Noklikšķiniet uz Pievienot.
71. Laukā Grāmata ievadiet vai atlasiet kādu vērtību.
72. Laukā Grāmatot vērtību atlasiet „Nolietojums (šis gads)”.
73. Laukā Galvenais konts norādiet vēlamās vērtības.
74. Laukā Korespondējošais konts norādiet vēlamās vērtības.
75. Noklikšķiniet uz Pievienot.
76. Laukā Grāmata ievadiet vai atlasiet kādu vērtību.
77. Laukā Grāmatot vērtību atlasiet „Nolietojuma korekcijas (iepriekšējie gadi)”.
78. Laukā Galvenais konts norādiet vēlamās vērtības.
79. Laukā Korespondējošais konts norādiet vēlamās vērtības.
80. Noklikšķiniet uz Pievienot.
81. Laukā Grāmata ievadiet vai atlasiet kādu vērtību.
82. Laukā Grāmatot vērtību atlasiet „Nolietojuma korekcijas (šis gads)”.
83. Laukā Galvenais konts norādiet vēlamās vērtības.
84. Laukā Korespondējošais konts norādiet vēlamās vērtības.
85. Noklikšķiniet uz Pievienot.
86. Laukā Grāmata ievadiet vai atlasiet kādu vērtību.
87. Laukā Grāmatot vērtību atlasiet „Atlikusī vērtība”.
88. Laukā Galvenais konts norādiet vēlamās vērtības.
89. Laukā Korespondējošais konts norādiet vēlamās vērtības.


