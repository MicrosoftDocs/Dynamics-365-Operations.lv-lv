--- 
title: "Pirmdokumentu audita ierobežojumu definēšana"
description: "Šajā procedūrā ir parādīts, kā izveidot un palaist audita ierobežojuma nosacījumus."
author: ryansandness
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4b05f744120e940bfea3e92b8aac3e41fc8151d9
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="define-audit-policies-for-source-documents"></a>Pirmdokumentu audita ierobežojumu definēšana

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā izveidot un palaist audita ierobežojuma nosacījumus. Piemērā tiek izmantotas izdevumu atskaites ar viesnīcu izdevumu tipu. Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati. Auditora loma ietver šo uzdevumu veikšanai atbilstošās atļaujas.

1. Pārejiet uz sadaļu Audita rīks >; Iestatīšana > Ierobežojuma nosacījumu tips.
2. Noklikšķiniet uz Jauns.
3. Laukā Kārtulas nosaukums ierakstiet kādu vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Laukā Vaicājuma nosaukums atlasiet Izdevumu atskaites rinda
6. Vaicājuma tipa laukā atlasiet Apkopojums
7. Laukā Juridiska persona atlasiet Juridiska persona
8. Laukā Dokumenta datuma atsauce atlasiet Modificēšanas datums un laiks
9. Noklikšķiniet uz Saglabāt.
10. Pārejiet uz sadaļu Audita rīks > Iestatīšana > Audita ierobežojumi.
11. Noklikšķiniet uz Jauns.
12. Laukā Nosaukums ierakstiet kādu vērtību.
13. Izvērsiet sadaļu Politikas organizācijas.
14. Koka struktūrā atlasiet “Contoso Entertainment System USA”.
15. Noklikšķiniet uz Pievienot.
16. Koka struktūrā atlasiet “Contoso Consulting USA”.
17. Noklikšķiniet uz Pievienot.
18. Koka struktūrā atlasiet “Contoso Retail USA”.
19. Noklikšķiniet uz Pievienot.
20. Sakļaujiet sadaļu Politikas organizācijas.
21. Izvērsiet sadaļu Ierobežojuma nosacījumi.
22. Sarakstā atrodiet un atlasiet iepriekš izveidoto ierobežojuma nosacījumu.
23. Noklikšķiniet uz Izveidot ierobežojuma nosacījumu.
24. Laukā Spēkā stāšanās datums ievadiet datumu un laiku.
25. Noklikšķiniet uz Filtrēt.
26. Sarakstā atlasiet rindu vienumam Izdevumu kategorija un detalizēto informāciju iestatiet uz Viesnīca
27. Laukā Kritēriji ievadiet vai atlasiet kādu vērtību.
28. Noklikšķiniet uz cilnes Apkopot.
29. Noklikšķiniet uz Pievienot.
30. Sarakstā atlasiet vērtību laukam Transakcijas summa
31. Laukā Lauks ievadiet vai atlasiet kādu vērtību.
32. Laukā AggregateFunction atlasiet “Sum”.
33. Noklikšķiniet uz cilnes Grupēt pēc.
34. Noklikšķiniet uz Pievienot.
35. Sarakstā atlasiet kādu vērtību vienumam Darbinieks  
36. Noklikšķiniet uz Pievienot.
37. Sarakstā atlasiet kādu vērtību vienumam Izdevumu kategorija
38. Laukā Lauks ievadiet vai atlasiet kādu vērtību.
39. Noklikšķiniet uz cilnes Saturs.
40. Noklikšķiniet uz Pievienot.
41. Atlasiet Transakcijas summa
42. Laukā Lauks ievadiet vai atlasiet kādu vērtību.
43. Laukā AggregateFunction atlasiet “Sum”.
44. Laukā Kritēriji ievadiet vērtību >2000.
45. Noklikšķiniet uz OK.
46. Noklikšķiniet uz Tests.
47. Laukā Dokumentu atlases sākuma datums ievadiet kādu datumu un laiku.
48. Laukā Dokumentu atlases beigu datums ievadiet kādu datumu un laiku.
49. Noklikšķiniet uz Izpildīt testu.
50. Darbību rūtī noklikšķiniet uz Audita politika.
51. Noklikšķiniet uz Papildu opcijas.
52. Laukā Sākuma datums ievadiet kādu datumu un laiku.
53. Laukā Beigu datums ievadiet kādu datumu un laiku.
54. Noklikšķiniet uz Partija.
55. Izvērsiet sadaļu Palaist fonā.
56. Laukā Pakešapstrāde atlasiet Jā.
57. Noklikšķiniet uz OK.
58. Pārejiet uz sadaļu Audita rīks > Audita gadījumi.
59. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
60. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
61. Izvērsiet sadaļu Saistības.
62. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
63. Sarakstā noklikšķiniet uz saites atlasītajā rindā.


