--- 
title: " Lojalitātes programmu definēšana"
description: "Šajā procedūrā parādīts, kā lojalitātes programmai iestatīt divus lojalitātes programmas līmeņus."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7a949d5cb4f01518b46bc4b1769de34196109050
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="define-loyalty-programs"></a> Lojalitātes programmu definēšana

[!include[task guide banner](../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā lojalitātes programmai iestatīt divus lojalitātes programmas līmeņus. Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.

1. Dodieties uz Mazumtirdzniecība un komercija > .. > Lojalitātes programmas.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums ierakstiet kādu vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Noklikšķiniet uz Pievienot rindu.
6. Laukā Līmenis ievadiet kādu skaitli.
7. Laukā Līmenis ievadiet lojalitātes programmas līmeņa nosaukumu.
8. Laukā Apraksts ierakstiet kādu vērtību.
9. Laukā Datumu intervāls noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Šo datumu intervālu ir jāpagarina tā, lai tas beigtos nākotnē. Piemēram, ja datumu intervāls, kas ir atlasīts zelta līmenim, ir viena gada periods, klients, kurš kvalificējas zelta līmenim, var saņemt zelta līmenim piešķirto atlīdzību uz vienu gadu. Ja klients atkārtoti kvalificējas zelta līmenim, kamēr viņam jau ir šis līmenis, līmeņa derīguma datums tiek pagarināts par vēl vienu gadu, sākot no dienas, kad klients atkārtoti iegūst zelta līmeņa statusu.  
10. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
11. Noklikšķiniet uz Pievienot rindu.
12. Laukā Līmenis ievadiet kādu skaitli.
13. Laukā Līmenis ievadiet lojalitātes programmas līmeņa nosaukumu.
14. Laukā Apraksts ierakstiet kādu vērtību.
15. Laukā Datumu intervāls noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
16. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
17. Noklikšķiniet uz Saglabāt.
18. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Līmeņu kārtulās tiek definēts minimālais atlīdzības punktu skaits, kas laika gaitā jāsakrāj, lai kvalificētos līmenim.  
19. Pārslēdziet sadaļas Līmeņu kārtulas paplašinājumu.
20. Noklikšķiniet uz Jauns.
    * Vienam līmenim var būt vairākas kārtulas. Piemēram, lai kvalificētos līmenim, var būt iestatīti trīs atšķirīgi kritēriji; iztērēt 500 ASV dolārus viena mēneša laikā, iztērēt 1000 ASV dolārus viena gada laikā un veikt 20 transakcijas viena gada laikā. Lai to paveiktu, ir jāizveido trīs limeņa kārtulas.  
21. Laukā Atlīdzības punkts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.
    * Tiem ir jābūt neizpērkamiem lojalitātes programmas atlīdzības punktiem.  
22. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
23. Laukā Minimālais izsniegto punktu skaits ievadiet skaitli.
    * Attiecībā uz viszemāko līmeni: ja visi debitori kvalificējas, tikai piedaloties programmā, ievadiet vērtību 0.  
24. Laukā Novērtēšanas datums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.
    * Šo datumu intervālu ir jāpagarina tā, lai tas beigtos pagātnē. Lai iegūtu minimālo izsniegto punktu vērtību, skaitīti tiks tikai šajā datumu intervālā iegūtie punkti.  
25. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
26. Noklikšķiniet uz Saglabāt.
27. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
28. Klikšķiniet Jauns.
29. Laukā Atlīdzības punkts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.
30. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
31. Laukā Minimālais izsniegto punktu skaits ievadiet skaitli.
32. Laukā Novērtēšanas datums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.
    * Šo datumu intervālu ir jāpagarina tā, lai tas beigtos pagātnē.  
33. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
34. Noklikšķiniet uz Saglabāt.
35. Noklikšķiniet uz Cenu grupas.
    * Ja saviem lojalitātes programmas debitoriem vēlaties piešķirt atlaides. Piešķiriet lojalitātes programmai un atlaidēm vienu vai vairākas cenu grupas. Tas ir vislabākais veids, kā nesajaukt cenu grupas dažāda veida atlaižu elementiem.  Piemēram, nelietojiet vienu cenu grupu lojalitātes programmas atlaidēm un kanāla atlaidēm.  
36. Laukā Cenu grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.
    * Lapas augšdaļā esošā cenu grupas saite ir paredzēta lojalitātes programmai. Programmas līmeņu kopsavilkuma cilnēs esošās cenu grupas saites ir paredzētas tikai noteiktam lojalitātes programmas līmenim.  
37. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
38. Noklikšķiniet uz Saglabāt.
39. Aizvērt lapu.
40. Noklikšķiniet uz Saglabāt.


