--- 
title: "Pārdošanas nepārtrauktības programmas un saistīto pārdošanas pasūtījumu apstrādāšana"
description: "Šajā procedūrā ir aprakstīts, kā pārdot nepārtrauktības programmu, un apstrādāt saistītos pārdošanas pasūtījumus."
author: scott-tucker
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 5fe1823c9b684bbc5ac5bd0871cc5c0a0e6ce678
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---
# <a name="selling-continuity-programs-and-processing-related-sales-orders"></a>Pārdošanas nepārtrauktības programmas un saistīto pārdošanas pasūtījumu apstrādāšana

[!include [task guide banner](../includes/task-guide-banner.md)]

Šajā procedūrā ir aprakstīts, kā pārdot nepārtrauktības programmu, un apstrādāt saistītos pārdošanas pasūtījumus. Lai pabeigtu šo procedūru, lietotājam ir jābūt iestatītam kā zvanu centra lietotājam. Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.

1. Dodieties uz Mazumtirdzniecība un komercija > Debitori > Debitoru apkalpošana.
2. Laukā SearchText ierakstiet 'Zane', un pēc tam nospiediet taustiņu Tab.
    * Parādīsies detalizētās meklēšanas uznirstošais dialoglodziņš. Ja tas neparādās, noklikšķiniet uz Meklēt, pa labi no šī lauka.  
3. Sarakstā atzīmējiet atlasīto rindu.
    * Jābūt tikai vienai rindai, kurā redzams Zane Siliņa. Atlasiet rindu, noklikšķinot uz atzīmes kolonnu, kas atrodas pa kreisi no režģa.  
4. Noklikšķiniet uz Atlasīt.
5. Noklikšķiniet uz Jauns pārdošanas pasūtījums.
    * Ir ieteicams atzīmēt pārdošanas pasūtījuma numuru. Tas būs nepieciešams vēlāk šajā procedūrā.  
6. Laukā Krājuma kods ierakstiet '88000', un pēc tam nospiediet taustiņu Tab.
    * Tas ir nepārtrauktības krājums USRT demonstrācijas datos.  
7. Noklikšķiniet uz Pabeigt.
8. Laukā Maksājuma metode ievadiet 'Visa'.
9. Noklikšķiniet uz Pievienot kredītkarti.
    * Ievadiet nepieciešamo kredītkartes informāciju šajā lapā.  
10. Noklikšķiniet uz OK.
11. Izvērsiet sadaļu Maksājums.
    * Lai iesniegtu zvanu centra pasūtījumu, pasūtījumam ir jāievada maksājumi.  
12. Noklikšķiniet uz OK.
13. Klikšķiniet Iesniegt.
    * Jūs esat pabeidzis jauna nepārtrauktību pasūtījuma izveidi. Pēc tam izpildiet divas pakešuzdevumu apstrādes, kas tiek izmantotas, lai apstrādātu nepārtrauktības pasūtījumus.  
14. Aizvērt lapu.
15. Dodieties uz Mazumtirdzniecība un komercija > Nepārtrauktība > Nepārtrauktības maksājumu apstrāde.
16. Laukā Nepārtrauktības krājums ierakstiet '88000', un pēc tam nospiediet taustiņu Tab.
17. Noklikšķiniet uz OK.
18. Dodieties uz Mazumtirdzniecība un komercija > Nepārtrauktība > Izveidot nepārtrauktības apakšpasūtījumus.
    * Šī procesa laikā tiks izveidoti jauni pārdošanas pasūtījumi, pamatojoties uz nepārtrauktības programmas iestatījumiem.  
19. Laukā Nepārtrauktības krājums ierakstiet '88000', un pēc tam nospiediet taustiņu Tab.
    * Krājums '88000' ir nepārtrauktības krājums USRT demonstrācijas datos.  
20. Laukā Pārdošanas pasūtījums ievadiet vai atlasiet kādu vērtību.
    * Ievadiet pārdošanas pasūtījuma numuru, kas atzīmējāt iepriekš šajā procedūrā. Tas saglabās apstrādes laiku minimālu šai procedūrai. Lauks Pārdošanas pasūtījums nav obligāts — varat apstrādāt visus pasūtījumus jebkurai programmai.  
21. Noklikšķiniet uz OK.


