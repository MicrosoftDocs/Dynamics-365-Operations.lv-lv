--- 
title: "EK iekšējās transakcijas iekraušanas adreses norādīšana"
description: "Šajā procedūrā parādīts kā norādīt iekraušanas adresi EK tirdzniecības darbībai."
author: v-oloski
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fc54b59f6cf8aec8d489955c57cbcf34c4e6be0a
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="specify-a-lading-address-for-an-intra-community-transaction"></a>EK iekšējās transakcijas iekraušanas adreses norādīšana

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts kā norādīt iekraušanas adresi EK tirdzniecības darbībai. Piemēram, Vācijas uzņēmums pasūta krājumus no kreditora ar vācu uzņēmuma adresi. Šim kreditoram ir noliktava Itālijā, un krājumi tiek piegādāti no turienes. Pārskats par šo piegādi jāsaglabā Intrastat. Tāda pati situācija ir derīga debitora atgrieztajiem krājumiem.
Šī procedūra attiecas uz visām Eiropas valstīm/reģioniem. Šis uzdevums ir izveidots, izmantojot demonstrācijas uzņēmuma DEMF datus, norādot Vāciju kā primārās adreses valsti. Lai varētu veikt šo procedūru, ir jākonfigurē Intrastat pārskatu veidošana. Šī procedūra ir paredzēta grāmatvežiem. Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.

1. Pārejiet uz sadaļu Kreditori > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Ievadiet vai atlasiet kādu vērtību
    * Piemēram, atlasiet DE-001. Šis kreditoram ir Vācijas uzņēmuma adrese.  
4. Noklikšķiniet uz OK.
5. Sarakstā atzīmējiet atlasīto rindu.
6. Laukā Krājuma kods ievadiet vai atlasiet vērtību D0001.
7. Klikšķiniet Saglabāt.
8. Darbību rūtī noklikšķiniet uz Saņemt.
9. Noklikšķiniet uz Transportēšanas dati.
10. Laukā Iekraušanas datums un laiks ievadiet kādu datumu un laiku.
11. Noklikšķiniet uz Pievienot adresi.
12. Noklikšķiniet uz Jauns un izveidojiet jaunu adresi ar nolūku Iekraušana.
13. Laukā Nosaukums vai apraksts ierakstiet 'Itālijas'.
14. Atlasiet Iekraušana kā vērtību.
    * Ņemiet vērā, ka adreses nolūkam ir jābūt Iekraušana.  
15. Laukā Valsts/reģions ievadiet vai atlasiet vērtību ITA.
16. Noklikšķiniet uz Saglabāt.
17. Aizvērt lapu.
18. Noklikšķiniet uz Saglabāt.
    * Pārbaudiet vai iekraušanas adrese ir pareiza.  
19. Aizvērt lapu.
20. Darbību rūtī noklikšķiniet uz Pirkt.
21. Noklikšķiniet uz Apstiprināt.
22. Darbību rūtī noklikšķiniet uz Rēķins.
23. Noklikšķiniet uz Rēķins.
24. Laukā Numurs ierakstiet kādu vērtību.
25. Laukā Rēķina datums ievadiet datumu.
26. Noklikšķiniet uz Noklusējums no: Produktu ieejas plūsmu daudzums, lai atvērtu nolaižamo dialoglodziņu.
27. Laukā Noklusējuma daudzums rindām atlasiet opciju 'Pasūtītais daudzums'.
28. Noklikšķiniet uz OK.
29. Noklikšķiniet uz Transportēšanas dati.
    * Pārbaudiet vai preces tika nosūtītas no Itālijas. Ja nepieciešams, varat rediģēt iekraušanas informāciju.  
30. Aizvērt lapu.
31. Noklikšķiniet uz Grāmatot.
32. Aizvērt lapu.
33. Dodieties uz Nodokļi > Deklarācijas > Ārējā tirdzniecība > Intrastat.
34. Noklikšķiniet uz Pārvest.
35. Atlasiet Jā laukā Kreditora rēķins.
36. Noklikšķiniet uz OK.
37. Noklikšķiniet uz cilnes Vispārīgi.
    * Atrodiet jaunizveidoto rindu un pārbaudiet, vai sūtītājs nosūtīja preces no Itālijas.  


