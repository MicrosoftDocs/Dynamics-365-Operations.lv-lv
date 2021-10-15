---
title: Pārdošanas komisijas kārtulu iestatīšana
description: Šajā procedūrā parādīts, kā iestatīt un aktivizēt pārdošanas komisijas naudas aprēķināšanu un izsekošanu.
author: Henrikan
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CommissionCustomerGroup, CommissionItemGroup, CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, CommissionCalc, InventPosting, CustTable, EcoResProductDetailsExtended, CommissionEmplSalesGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f42f2fbe22124dbaaf2c4bd2f4394f734d166d5
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578900"
---
# <a name="set-up-sales-commission-rules"></a>Pārdošanas komisijas kārtulu iestatīšana

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā iestatīt un aktivizēt pārdošanas komisijas naudas aprēķināšanu un izsekošanu. Procedūrā parādīts, kā izveidot debitora un krājuma komisijas grupas un pēc tam, kā atlasīto debitoru un preci saistīt ar attiecīgo grupu. Pēc tam šīs grupas tiek lietotas komisijas aprēķina iestatīšanā, lai izveidotu debitora, krājuma un pārdošanas pārstāvja kombināciju, kam jāatbilst pārdošanas pasūtījumam, lai piešķirtu pārdevējiem tiesības uz komisiju. Izveidot debitora un krājuma komisijas grupas nav obligāti, jo komisijas naudas aprēķinu var veikt arī atsevišķam debitoram un/vai krājumam. Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.


## <a name="set-up-commission-groups-and-commission-rates"></a>Komisijas grupu un komisiju likmju iestatīšana
1. Dodieties uz **Navigācijas rūts > Moduļi > Pārdošana un mārketings > Komisijas > Komisijas debitoru grupas**.
2. Atlasiet **Jauns**.
3. Laukā **Grupa** ierakstiet vērtību.
4. Laukā **Nosaukums** ierakstiet kādu vērtību.
5. Atlasiet **Saglabāt**.
6. Aizvērt lapu.
7. Dodieties uz **Navigācijas rūts > Moduļi > Pārdošana un mārketings > Komisijas > Krājumu grupas**.
8. Atlasiet **Jauns**.
9. Laukā **Grupa** ierakstiet vērtību.
10. Laukā **Nosaukums** ierakstiet kādu vērtību.
11. Atlasiet **Saglabāt**.
12. Aizvērt lapu.
13. Pārejiet uz sadaļu **Pārdošana un mārketings > Komisijas > Pārdošanas grupas**.
    - Komisijas pārdošanas grupā norādīti darbinieki pārdošanas pārstāvja lomās, kas ir tiesīgi saņemt komisiju, kad debitors, kas saistīts ar attiecīgo pārdošanas grupu, pērk noteiktus krājumus.  
    - USMF demonstrācijas datu uzņēmumā ir pārdošanas grupa ar nosaukumu "Tirdzniecības pārstāvji ASV".  
14. **ADarbību rūtī** atlasiet **Vispārīgi**.
15. Noklikšķiniet uz **Tirdzniecības pārstāvis**. Lapā Tirdzn. pārstāvis ir redzams to uzņēmuma pārdevēju saraksts, kuri ir saistīti ar konkrēto komisijas grupu. Vairākus pārdošanas pārstāvjus var piešķirt vienai grupai un noteikt to attiecīgo daļu kopējā komisijā kā procentuālu vērtību. Visu darbinieku kopējā komisija nedrīkst pārsniegt 100. 
16. Sarakstā atzīmējiet atlasīto rindu.
17. Atlasiet **Rediģēt**.
18. Iestatiet **Komisijas daļa** uz "50".
19. Klikšķiniet **Jauns**.
20. Laukā **Nosaukums** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu pārlūku.
21. Izmantojiet līdzekli **Ātrais filtrs**, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Nosaukums, izmantojot vērtību “Susan Burk”.
22. Noklikšķiniet uz **Atlasīt**.
23. Iestatiet **Komisijas daļa** uz "50".
24. Noklikšķiniet uz **Saglabāt**.
25. Pārejiet uz sadaļu **PPārdošana un mārketings > Komisijas > Komisijas naudas aprēķins**. Lapā **Komisijas naudas aprēķins** jūs nosakāt komisijas likmi, kura darbiniekam ir jāsaņem par pārdošanas transakciju, ja tā satur iepriekš iestatīto debitora un preces kombināciju. Kā daļu no komisijas iestatīšanas jums jānorāda komisijas aprēķina pamats un vai tai vajadzētu iekļaut vai izslēgt atlaides. Varat ievadīt arī derīguma termiņu, kura laikā komisijas likme ir aktīva.  
26. Klikšķiniet **Jauns**.
27. Laukā **Krājuma kods** atlasiet Grupa.
28. Laukā **Krājumu saistība** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu pārlūku.
29. Sarakstā atrodiet un atlasiet grupu, kuru izveidojāt agrāk.
30. Laukā **Debitora kods** atlasiet "Grupa".
31. Laukā **Debitors/grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
32. Sarakstā atlasiet grupu, kuru iestatījāt agrāk.
33. Laukā **Tirdzn. pārst./grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
34. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    - Paturiet opciju "Pirms rindas atlaides".  
    - Paturiet opciju "Ieņēmumi" kā komisijas vērtības aprēķina pamatu.    
35. Laukā Komisijas nauda procentos ievadiet kādu skaitli.
36. Noklikšķiniet uz **Saglabāt**.

## <a name="setting-up-commission-posting"></a>Komisijas naudas grāmatošanas iestatīšana
1. Dodieties uz **Navigācijas rūts > Pārdošana un mārketings > Komisijas > Komisijas naudas grāmatošana**. Komisijas naudas ir jāmaksā darbiniekiem, un tāpēc tās jāiestata tā, lai nodrošinātu pareizu finanšu grāmatošanu atbilstošos **Virsgrāmatas** kontos. Tas tiek darīts lapā **Komisijas grāmatošana**. Pārskatiet iestatījumus, kas ir pieejami pašreizējam uzņēmumam. Parasti komisijas summas tiek grāmatotas speciālā izdevumu kontā un tiek nosegtas ar speciālu kreditoru kontu. Ja jums nav komisijas grāmatošanas noteikumu iestatījumu, sistēmai neizdosies veikt rēķina izrakstīšanu pārdošanas pasūtījumam, kam piemērojama komisija.  
2. Aizvērt lapu.

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a>Komisijas grupas piešķiršana debitoram un precei
1. Dodieties uz **Navigācijas rūts > Moduļi > Pārdošana un mārketings > Debitori > Visi debitori**.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
4. Noklikšķiniet uz **Rediģēt**.
5. Izvērsiet sadaļu **Pārdošanas pasūtījuma noklusējuma informācija**.
6. Laukā **Komisijas grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
7. Sarakstā atlasiet grupu, kuru izveidojāt agrāk.
8. Laukā **Pārdošanas grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
9. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
10. Noklikšķiniet uz **Saglabāt**.
11. Dodieties uz **Navigācijas rūts > Moduļi > Preču informācijas pārvaldība > Preces > Tirdzniecībā izlaistās preces**.
12. Izmantojiet līdzekli **Filtrs**, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Krājuma numurs, izmantojot vērtību "T0020".
13. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
14. Noklikšķiniet uz **Rediģēt**.
15. Izvērsiet sadaļu **Pārdot**.
16. Laukā **Komisijas grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
17. Sarakstā atlasiet komisijas grupu, kuru izveidojāt agrāk.
18. Atlasiet **Saglabāt**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]