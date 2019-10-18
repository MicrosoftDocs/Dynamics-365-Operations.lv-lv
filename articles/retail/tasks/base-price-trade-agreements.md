---
title: " Bāzes cena un tirdzniecības līgumi"
description: Šajā procedūrā parādīts, kā izveidot kanāla pārdošanas cenas tirdzniecības līgumus.
author: josaw1
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45d3d962958d0487c9e65910a2dce24097a83773
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017762"
---
# <a name="base-price-and-trade-agreements"></a> Bāzes cena un tirdzniecības līgumi

[!include[task guide banner](../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā izveidot kanāla pārdošanas cenas tirdzniecības līgumus. Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.

1. **Navigācijas rūtī** ejiet uz **Moduļi > Mazumtirdzniecība un komercija > Cenošanas un atlaižu pārvaldība > Cenu grupas > Visas cenu grupas**. Cenu grupas ir veids, kā tirdzniecības līgumi tiek piešķirti noteiktiem kanāliem. Izmantojot cenu grupas, lai tirdzniecības līgumus piešķirtu kanāliem, var cenas var noteikt konkrētam kanālam.  
2. Klikšķiniet **Jauns**.
3. Laukā **Cenu grupas** ievadiet vērtību.
4. Laukā **Nosaukums** ierakstiet kādu vērtību.
5. Noklikšķiniet uz **Saglabāt**.
6. Aizvērt lapu.
7. **Navigācijas rūtī** ejiet uz **Moduļi > Mazumtirdzniecība un komercija > Kanāli > Mazumtirdzniecības veikali > Visi mazumtirdzniecības veikali**.
8. Sarakstā atlasiet Ņujorka.
9. Darbību rūtī noklikšķiniet uz **Saglabāt**.
10. Noklikšķiniet uz **Cenu grupas**.
11. Klikšķiniet **Jauns**.
12. Laukā **Cenu grupas** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.
13. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
14. Noklikšķiniet uz **Saglabāt**.
15. Aizvērt lapu.
16. Aizvērt lapu.
17. **Navigācijas rūtī** ejiet uz **Moduļi > Mazumtirdzniecība un komercija > Produkti un kategorijas > Izlaistie produkti pēc kategorijas**.
18. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
19. Noklikšķiniet uz **Rediģēt**.
20. Izvērsiet kopsavilkuma cilni **Pārdot**.
21. Laukā **Cena** ievadiet skaitli. Šī cena tiek izmantota, ja netika atrasts neviens atbilstošs tirdzniecības līgums.  
22. Noklikšķiniet uz **Saglabāt**.
23. **Darbību rūtī**noklikšķiniet uz **Pārdot**.
24. Klikšķiniet uz **Izveidot tirdzniecības līgumus**.
25. Klikšķiniet **Jauns**.
26. Laukā **Nosaukums** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu pārlūku.
27. Sarakstā atlasiet **Mazumtirdzniecība**. Demonstrācijas datos žurnāla nosaukumam **Mazumtirdzniecība** ir noklusējuma relācija **Cena (pārdošanas)**. Tas nozīmē, ka visām jaunajām rindām pēc noklusējuma tiks iestatīti pārdošanas cenas tirdzniecības līgumi.  
28. **Darbību rūtī** noklikšķiniet uz **Rindas**.
29. Atlasiet „Grupa” laukā **Konta kods**.
30. Laukā **Konta atlase** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu pārlūku.
31. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu. Tādējādi tiks pabeigta piesaiste no kanāla uz cenu grupu uz tirdzniecības līgumu.  
32. Laukā **Vienuma attiecība** ierakstiet vērtību.
33. Laukā **Summa valūtā** ievadiet skaitli.
34. Kopsavilkuma cilnē **Detaļas** atzīmējiet vai noņemiet atzīmi izvēles rūtiņai **Atrast nākamo**. Kad iespēja **Atrast nākamo** iestatīta kā „Jā”, cenošanas programma turpinās meklēt piemērojamos tirdzniecības līgumus ar zemāku pārdošanas cenu. Kad iespēja **Atrast nākamo** iestatīta kā „Nē”, cenošanas programma beidz meklēt un izmanto tirdzniecības līgumu.  
35. Noklikšķiniet uz **Grāmatot**.
36. Noklikšķiniet uz **Labi**.
37. Aizvērt lapu.
38. **Darbību rūtī** noklikšķiniet uz „Pārdot”
39. Noklikšķiniet uz **Pārdošanas cena**.

