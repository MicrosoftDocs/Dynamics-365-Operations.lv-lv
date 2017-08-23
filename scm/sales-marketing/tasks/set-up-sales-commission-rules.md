--- 
title: "Pārdošanas komisijas kārtulu iestatīšana"
description: "Šajā procedūrā parādīts, kā iestatīt un aktivizēt pārdošanas komisijas naudas aprēķināšanu un izsekošanu."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 0ab5b3b5447e56eb8ed012a67454400cb2357af4
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-sales-commission-rules"></a>Pārdošanas komisijas kārtulu iestatīšana

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā iestatīt un aktivizēt pārdošanas komisijas naudas aprēķināšanu un izsekošanu. Procedūrā parādīts, kā izveidot debitora un krājuma komisijas grupas un pēc tam, kā atlasīto debitoru un preci saistīt ar attiecīgo grupu. Pēc tam šīs grupas tiek lietotas komisijas aprēķina iestatīšanā, lai izveidotu debitora, krājuma un pārdošanas pārstāvja kombināciju, kam jāatbilst pārdošanas pasūtījumam, lai piešķirtu pārdevējiem tiesības uz komisiju. Izveidot debitora un krājuma komisijas grupas nav obligāti, jo komisijas naudas aprēķinu var veikt arī atsevišķam debitoram un/vai krājumam. Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.


## <a name="set-up-commission-groups-and-commission-rates"></a>Komisijas grupu un komisiju likmju iestatīšana
1. Pārejiet uz sadaļu Pārdošana un mārketings > Komisijas > Komisijas debitoru grupas.
2. Noklikšķiniet uz Jauns.
3. Laukā Grupa ierakstiet vērtību.
4. Laukā Nosaukums ierakstiet kādu vērtību.
5. Noklikšķiniet uz Saglabāt.
6. Aizvērt lapu.
7. Pārejiet uz sadaļu Pārdošana un mārketings > Komisijas > Krājumu grupas.
8. Noklikšķiniet uz Jauns.
9. Laukā Grupa ierakstiet vērtību.
10. Laukā Nosaukums ierakstiet kādu vērtību.
11. Aizvērt lapu.
12. Pārejiet uz sadaļu Pārdošana un mārketings > Komisijas > Pārdošanas grupas.
    * Komisijas pārdošanas grupā norādīti darbinieki pārdošanas pārstāvja lomās, kas ir tiesīgi saņemt komisiju, kad debitors, kas saistīts ar attiecīgo pārdošanas grupu, pērk noteiktus krājumus.  
    * USMF demonstrācijas datu uzņēmumā ir pārdošanas grupa ar nosaukumu "Tirdzniecības pārstāvji ASV".  
13. Darbību rūtī noklikšķiniet uz Vispārīgi.
14. Noklikšķiniet uz Tirdzn. pārstāvis.
    * Lapā Tirdzn. pārstāvis ir parādīts uzņēmuma pārdevēju saraksts, kuri ir saistīti ar specifisku komisijas grupu. Vairākus pārdošanas pārstāvjus var piešķirt vienai grupai un noteikt to attiecīgo daļu kopējā komisijā kā procentuālu vērtību. Visu darbinieku kopējā komisija nedrīkst pārsniegt 100.  
15. Sarakstā atzīmējiet atlasīto rindu.
16. Noklikšķiniet uz Rediģēt.
17. Iestatiet Komisijas daļa uz "50".
18. Noklikšķiniet uz Jauns.
19. Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
20. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Nosaukums, izmantojot vērtību “Susan Burk”.
21. Noklikšķiniet uz Atlasīt.
22. Iestatiet Komisijas daļa uz "50".
23. Noklikšķiniet uz Saglabāt.
24. Pārejiet uz sadaļu Pārdošana un mārketings > Komisijas > Komisijas naudas aprēķins.
    * Laukā Komisijas naudas aprēķins jūs nosakāt komisijas likmi, kura darbiniekam ir jāsaņem par pārdošanas transakciju, ja tā satur iepriekš iestatīto debitora un preces kombināciju. Kā daļu no komisijas iestatīšanas jums jānorāda komisijas aprēķina pamats un vai tai vajadzētu iekļaut vai izslēgt atlaides. Varat ievadīt arī derīguma termiņu, kura laikā komisijas likme ir aktīva.  
25. Noklikšķiniet uz Jauns.
26. Laukā Krājuma kods atlasiet Grupa.
27. Laukā Krājumu saistība noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
28. Sarakstā atrodiet un atlasiet grupu, kuru izveidojāt agrāk.
29. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
30. Laukā Debitora kods atlasiet "Grupa".
31. Laukā Debitors/grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
32. Sarakstā atlasiet grupu, kuru iestatījāt agrāk.
33. Relācijas laukā Tirdzn. noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
34. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Paturiet opciju "Pirms rindas atlaides".  
    * Paturiet opciju "Ieņēmumi" kā komisijas vērtības aprēķina pamatu.    
35. Laukā Komisijas nauda procentos ievadiet kādu skaitli.
36. Noklikšķiniet uz Saglabāt.

## <a name="setting-up-commission-posting"></a>Komisijas naudas grāmatošanas iestatīšana
1. Pārejiet uz sadaļu Pārdošana un mārketings > Komisijas > Komisijas naudas grāmatošana.
    * Komisijas naudas ir jāmaksā darbiniekiem, un tāpēc tās jāiestata tā, lai nodrošinātu pareizu finanšu grāmatošanu atbilstošos Virsgrāmatas kontos. Tas tiek darīts lapā Komisijas grāmatošana. Pārskatiet iestatījumus, kas ir pieejami pašreizējam uzņēmumam. Parasti komisijas summas tiek grāmatotas speciālā izdevumu kontā un tiek nosegtas ar speciālu kreditoru kontu. Ja jums nav komisijas grāmatošanas noteikumu iestatījumu, sistēmai neizdosies veikt rēķina izrakstīšanu pārdošanas pasūtījumam, kam piemērojama komisija.  
2. Aizvērt lapu.

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a>Komisijas grupas piešķiršana debitoram un precei
1. Pārejiet uz sadaļu Pārdošana un mārketings > Debitori > Visi debitori.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
4. Noklikšķiniet uz Rediģēt.
5. Izvērsiet sadaļu Pārdošanas pasūtījuma noklusējuma informācija.
6. Laukā Komisijas grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
7. Sarakstā atlasiet grupu, kuru izveidojāt agrāk.
8. Laukā Pārdošanas grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
9. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
10. Noklikšķiniet uz Saglabāt.
11. Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.
12. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Krājuma numurs, izmantojot vērtību "T0020".
13. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
14. Noklikšķiniet uz Rediģēt.
15. Izvērsiet sadaļu Pārdot.
16. Laukā Komisijas grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
17. Sarakstā atlasiet komisijas grupu, kuru izveidojāt agrāk.


