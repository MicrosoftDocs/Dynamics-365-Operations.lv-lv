---
title: Pirmdokumentu audita politiku definēšana
description: Šajā rakstā skaidrots, kā iestatīt un palaist audita ierobežojumu nosacījumus.
author: panolte
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b8aa106cd5a5596f6b9a6663390e03ebc3f91a7b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872533"
---
# <a name="define-audit-policies-for-source-documents"></a>Pirmdokumentu audita politiku definēšana

[!include [banner](../../includes/banner.md)]

Šajā rakstā skaidrots, kā iestatīt un palaist audita ierobežojumu nosacījumus. Piemērā tiek izmantotas izdevumu atskaites ar viesnīcu izdevumu tipu. Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati. Auditora loma ietver šo uzdevumu veikšanai atbilstošās atļaujas.

1. Navigācijas rūtī ejiet uz **Moduļi > Audita darbvieta > Iestatīšana > Politikas noteikuma veids**.
2. Atlasiet **Jauns**.
3. Laukā **Noteikuma nosaukums** ierakstiet vērtību.
4. Laukā **Apraksts** ierakstiet kādu vērtību.
5. Laukā **Vaicājuma nosaukums** atlasiet **Izdevumu atskaites rinda**
6. Laukā **Vaicājuma veids** atlasiet **Apkopot**
7. Laukā **Juridiskā persona** atlasiet **Juridiskā persona**
8. Laukā **Dokumenta datuma atsauce** atlasiet **Izmaiņu datums un laiks**.
9. Atlasiet **Saglabāt**.
10. Navigācijas rūtī ejiet uz **Moduļi > Audita darbvieta > Iestatīšana > Audita politikas**.
11. Atlasiet **Jauns**.
12. Laukā **Nosaukums** ierakstiet kādu vērtību.
13. Izvērsiet sadaļu **Politikas organizācijas**.
14. Kokā atlasiet **Contoso Entertainment System USA**, tad atlasiet **Pievienot**.
15. Kokā atlasiet **Contoso Consulting USA**, tad atlasiet **Pievienot**.
16. Kokā atlasiet **Contoso Retail USA**, tad atlasiet **Pievienot**.
17. Sakļaujiet sadaļu **Politikas organizācijas**.
18. Izvērsiet sadaļu **Politikas noteikumi**.
19. Sarakstā atrodiet un atlasiet iepriekš izveidoto ierobežojuma nosacījumu.
20. Atlasiet **Izveidot ierobežojuma nosacījumu**.
21. Laukā **Spēkā stāšanās datums** ievadiet datumu un laiku.
22. Atlasiet **Filtrēt**.
23. Sarakstā atlasiet **Izdevumu kategorijas** rindu un iestatiet detalizēto informāciju kā **Viesnīca**.
24. Ievadiet vai atlasiet vērtību laukā **Kritēriji**.
25. Atlasiet cilni **Apkopot**.
26. Atlasiet **Pievienot**.
27. Sarakstā atlasiet vērtību laukam **Darījuma summa**.
28. Laukā **Lauks** ievadiet vai atlasiet vērtību.
29. Laukā **ApkopošanasFunkcija** atlasiet **Summa**.
30. Atlasiet cilni **Grupēt pēc**.
31. Atlasiet **Pievienot**.
32. Sarakstā atlasiet vērtību laukam **Darbinieks**.
33. Atlasiet **Pievienot**.
34. Sarakstā atlasiet vērtību laukam **Izdevumu kategorija**.
35. Laukā **Lauks** ievadiet vai atlasiet vērtību.
36. Atlasiet cilni **Ir rīcībā**.
37. Atlasiet **Pievienot**.
38. Atlasiet **Darījuma summa**.
39. Laukā **Lauks** ievadiet vai atlasiet vērtību.
40. Laukā **ApkopošanasFunkcija** atlasiet **Summa**.
41. Laukā **Kritēriji** ievadiet `>2000`.
42. Atlasiet **Labi**.
43. Atlasiet **Pārbaudīt**.
44. Laukā **Dokumenta atlases sākuma datums** ievadiet datumu un laiku.
45. Laukā **Dokumenta atlases beigu datums** ievadiet datumu un laiku.
46. Atlasiet **Veikt pārbaudi**.
47. Darbību rūtī atlasiet **Audita politika**.
48. Atlasiet **Papildu opcijas**.
49. Laukā **Sākuma datums** ievadiet datumu un laiku.
50. Laukā **Beigu datums** ievadiet datumu un laiku.
51. Atlasiet **Partija**.
52. Izvērsiet sadaļu **Darbināt fonā**.
53. Laukā **Partijas apstrāde** atlasiet **Jā**.
54. Atlasiet **Labi**.
55. Navigācijas rūtī ejiet uz **Moduļi > Audita darbvieta > Audita lietas**.
56. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
57. Izvērsiet sadaļu **Saistības**.
58. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
