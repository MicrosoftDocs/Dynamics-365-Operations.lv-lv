---
title: Izmantojot nepārtrauktības programmu
description: Šajā procedūrā ir aprakstīts, kā pārdot nepārtrauktības programmu, un apstrādāt saistītos pārdošanas pasūtījumus.
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.industry: Retail
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
ms.openlocfilehash: 3736984a336b35b23b7060b2d98770912cc9ec6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267409"
---
# <a name="using-continuity-program"></a>Izmantojot nepārtrauktības programmu

[!include [banner](../includes/banner.md)]

Šajā procedūrā ir aprakstīts, kā pārdot nepārtrauktības programmu, un apstrādāt saistītos pārdošanas pasūtījumus. Lai pabeigtu šo procedūru, lietotājam ir jābūt iestatītam kā zvanu centra lietotājam. Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.

1. Dodieties uz Retail un Commerce > Debitori > Debitoru apkalpošana.
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
15. Dodieties uz Retail un Commerce > Nepārtrauktība > Nepārtrauktības maksājumu apstrāde.
16. Laukā Nepārtrauktības krājums ierakstiet '88000', un pēc tam nospiediet taustiņu Tab.
17. Noklikšķiniet uz Labi.
18. Dodieties uz Retail un Commerce > Nepārtrauktība > Izveidot nepārtrauktības apakšpasūtījumus.
    * Šī procesa laikā tiks izveidoti jauni pārdošanas pasūtījumi, pamatojoties uz nepārtrauktības programmas iestatījumiem.  
19. Laukā Nepārtrauktības krājums ierakstiet '88000', un pēc tam nospiediet taustiņu Tab.
    * Krājums '88000' ir nepārtrauktības krājums USRT demonstrācijas datos.  
20. Laukā Pārdošanas pasūtījums ievadiet vai atlasiet kādu vērtību.
    * Ievadiet pārdošanas pasūtījuma numuru, kas atzīmējāt iepriekš šajā procedūrā. Tas saglabās apstrādes laiku minimālu šai procedūrai. Lauks pārdošanas pasūtījums ir neobligāts--jūs varat apstrādāt visus pasūtījumus jebkurai programmai.  
21. Noklikšķiniet uz OK.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
