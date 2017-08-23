--- 
title: "Finanšu gada slēgšana"
description: "Šajā procedūrā tiek aprakstīts gada beigu slēgšanas process, kas pārsūta bilances uz jaunu finanšu gadu."
author: aprilolson
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 83ea19e11596374c3e3ceb051db0b483f4b58583
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="close-the-fiscal-year"></a>Finanšu gada slēgšana

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā tiek aprakstīts gada beigu slēgšanas process, kas pārsūta bilances uz jaunu finanšu gadu.


## <a name="validate-year-end-close-parameters"></a>Apstiprināt gada beigu slēgšanas parametrus
1. Dodieties uz Virsgrāmata > Virsgrāmatas iestatīšana > Virsgrāmatas parametri.
2. Izvērsiet sadaļu Finanšu gada slēgšana.
3. Atlasiet Jā vai Nē opcijai gada slēgšanas darbību dzēšana pārsūtīšanas laikā.
    * Ja finanšu gads jau ir slēgts, un gada beigu slēgšana tiek palaista vēlreiz, šis iestatījums ir svarīgs. Ja iestatīts uz Jā, dokuments par iepriekšējā gada beigu slēgšanu tiks dzēsts, un tiks izveidots jauns dokuments visu kontu sākuma bilancēm. Ja iestatīts uz Nē, iepriekšējais dokuments tiks saglabāts un tiks izveidots jauns dokuments tikai ierakstu pielāgošanai, kas tika grāmatoti pēc iepriekšējā gada beigu slēgšanas.  
4. Atlasiet Jā vai Nē, vai veidot slēgšanas darbības pārsūtīšanas laikā.
    * Ja iestatīts uz Jā, tiek izveidotas divas darbības. Viens dokuments ir izveidots finanšu gadā, kas tiek slēgts, lai pārnestu bilances uz PL virsgrāmatas kontiem, līdz nullei, un nākamajā finanšu gada tiek izveidots otrs dokuments sākuma bilancēm. Ja iestatīts uz Nē, tiek izveidots viens dokuments nākamā finanšu gada sākuma bilancēm.  
5. Atlasiet Jā vai Nē, vai iestatīt finanšu gada statusu kā neatgriezeniski slēgtu.
    * Ja iestatīts uz Jā, finanšu gada statuss tiek iestatīts uz Neatgriezeniski slēgts.  Tā kā neatgriezeniski slēgtu gadu nevar atvērt atkārtoti, vislabāk ir iestatīt šo opciju uz Nē.  
6. Atlasiet Jā vai Nē, vai dokumenta numurs ir jānorāda gada beigu slēgšanas laikā.
    * Ja iestatīts uz Jā, Gada beigu slēgšanas procesa laikā, dokumenta numurs ir jāievada manuāli. Numuru sērija netiek izmantota, lai ģenerētu šo dokumenta numuru. Vislabāk ir iestatīt to uz Jā.  
7. Aizvērt lapu.
8. Pārejiet uz sadaļu Virsgrāmata > Perioda noslēgšana > Gada beigu slēgšana.
9. Noklikšķiniet uz Jauns, lai izveidotu gada beigu slēgšanas veidni.
    * Veidni var izveidot juridisku personu grupai, kurai vēlaties palaist gada beigu slēgšanu. Šo veidni var izmantot atkārtoti katru gadu.  
10. Grupas nosaukuma laukā, ievadiet gada beigu slēgšanas veidnes nosaukumu..
11. Atlasiet finanšu gadu, kuram tiks izveidota veidne.
    * Tikai juridiskas personas, kas izmanto vienā finanšu gadu, var sagrupēt gada beigu slēgšanas veidnē. Tas ir tāpēc, ka gada beigu slēgšana tiek veikta, izvēloties finanšu gadu, nevis datumu.  
12. Lietojiet šo saīsni ieraksta saglabāšanai.
13. Noklikšķiniet uz Pievienot, lai atlasītu juridiskas personas šo veidnei.
    * Juridiskās personas var pievienot, atlasot juridiskās personas vai atlasot organizācijas hierarhiju.  Tiks pievienotas tikai juridiskās personas ar organizācijas hierarhiju, ar atlasītu to pašu finanšu kalendāru.  
14. Atlasiet juridiskās personas vai organizācijas hierarhiju.
15. Noklikšķiniet uz OK.
16. Atlasiet vai finanšu dimensijas tiks pārnestas uz nākamo finanšu gadu.
    * Vislabākais ir iestatīt šo opciju Bilances kontiem uz Jā.  Tas saglabās grāmatoto darbību finanšu dimensijas, veidojot bilances kontu sākuma atlikumus.  Peļņas un zaudējumu kontos jūs varat uzturēt finanšu dimensijas (Slēgt visu), kad bilances tiek pārvietotas uz Nesadalīto peļņu, vai jūs varat aizstāt finanšu dimensijas ar citu dimensijas vērtību (Slēgt vienu). Atlasot opciju Slēgt vienu, jūs varat definēt konkrētu dimensijas vērtību katrai dimensijai vai pat atstāt to tukšu.  
17. Noklikšķiniet uz Saglabāt.
18. Sāciet gada beigu slēgšanu, Darbību rūtī, atlasot palaist finanšu slēgšanu.
    * Gada beigu slēgšana tiks veikta atlasītajai veidnei.  
19. Atlasiet visas vai juridisko personu apakškopu no veidnes, kurā vēlaties palaist gada beigu slēgšanu.
    * Pirmo reizi palaižot gada beigu slēgšanu, lai iegūtu sākuma bilances daļa organizāciju var izvēlēties veikt gada beigu slēgšanas visām juridiskajām personām veidnē. Ja pēc tam tiek veikti pielāgošanas ieraksti, jūs varat palaist gada beigu slēgšanu tikai juridiskām personām, kurām ir korekcijas.  
20. Noklikšķiniet uz OK.
21. Atlasiet finanšu gadu, kuram vēlaties palaist gada beigu slēgšanu.
22. Laukā Dokuments ievadiet vērtību.
    * Tas ir vislabākais veids, lai iekļautu finanšu gada dokumenta numuru, lai būtu vieglāk atrast gada beigu slēgšanas dokumentu, kas tiek izveidots.  
23. Gada beigu slēgšanas noklusējumi, kas jāpalaiž paketē.
    * Tas ir vislabākais veids kā ilgstošus procesus palaist pakešveida režīmā. Tas parasti ir viens no šiem procesiem, tāpēc pēc noklusējuma nepieciešams izmantot pakešveida režīmu.  
24. Noklikšķiniet uz OK.


