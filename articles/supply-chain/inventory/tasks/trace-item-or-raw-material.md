---
title: Krājumu vai izejmateriālu izsekošana
description: Šajā procedūra parādīts, kā lietot krājumu izsekošanu, lai identificētu, kur krājumi vai izejmateriāli ir izmantoti vai tiek izmantoti.
author: pjacobse
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria, InventTrackingItemIdLookup, InventBatchIdLookup, CustTable, SalesLine
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 897a777b3f4ce05fe995aa98a72feb99d82837ef
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561298"
---
# <a name="trace-an-item-or-raw-material"></a>Krājumu vai izejmateriālu izsekošana

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūra parādīts, kā lietot krājumu izsekošanu, lai identificētu, kur krājumi vai izejmateriāli ir izmantoti vai tiek izmantoti. Izmantojot šo procedūru, varat identificēt krājumu, izsekot to atpakaļ līdz avotam un pēc tam izsekot uz priekšu līdz ražošanai un pabeigtās preces pārdošanai. Procesu var lietot, lai izpētītu ietekmētos klientus, skartos pārdošanas pasūtījumus un citus aspektus. Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma USP2 dati.


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a>Krājuma izsekošana atpakaļ, izmantojot zināmu partijas numuru
1. Pārejiet uz sadaļu Krājumu pārvaldība > Pieprasījumi un pārskati > Izsekošanas dimensijas > Krājuma izsekošana.
2. Laukā Krājuma kods atlasiet P9100.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
4. Laukā Uz priekšu vai atpakaļ atlasiet vienumu Atpakaļ.
5. Laukā Partijas numurs atlasiet as-12-344-01.
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
7. Noklikšķiniet uz OK.

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a>Krājuma identificēšana, tā izsekošana uz priekšu un analīzes veikšana
    * Koka struktūras augšējais zars atspoguļo atlasītā krājuma un partijas rīcībā esošo daudzumu. Jums ir jāizvērš koka struktūras zari, lai atrastu krājumu, kuram ir jāveic uz priekšu vērstā izsekošanu.   
1. Koka struktūrā izvērsiet “tālāk aprakstītos zarus, un pēc tam atlasiet pēdējo zaru”.
    * Izvērsiet: “P9100 / 1 / 10 / as-12-344-01 ● 2 muciņas ● 7,00 gal. \P9100 ● Izdots ● Pārdošanas pasūtījums 000072 ● 12/22/2015 ● -1 muciņa ● -4,00 gal. ● Vieta=1, Noliktava=10, Partijas numurs=as-12-344-01 \P9100 ● Ražošana B-000050 ● 12/9/2015● 7 muciņas ● 27,00 gal. ● Vieta=1,Noliktava=10,Partijas numurs=as-12-344-01 ● Līdzprodukti: P9101” un pēc tam atlasiet šo zaru.     
2. Koka struktūrā izvērsiet “tālāk aprakstīto zaru un pēc tam atlasiet šo zaru”.
    * Sākot no jūsu atlasīta zara izvērsiet “M9103 ● Ražošanas rinda B-000050 ● 12/9/2015  ● -160,00 mārc. ● Izmērs=70, Krāsa=Labi, Vieta=1, Noliktava=10, Partijas numurs=App01'” un pēc tam atlasiet šo zaru.  
3. Noklikšķiniet uz vienuma Izsekošana no zara.
4. Noklikšķiniet uz vienuma Uz priekšu.
5. Darbību rūtī noklikšķiniet uz vienuma Izsekošana.
    * Pastāv vairākas izsekošanas opcijas, kas sniedz informāciju par debitoriem, kurus ietekmē jūsu izsekotais krājums, kā arī ar šo krājumu saistītajiem pārdošanas pasūtījumiem, kas ir un vēl nav nosūtīti.   
6. Noklikšķiniet uz vienuma Debitori.
7. Aizvērt lapu.
8. Darbību rūtī noklikšķiniet uz vienuma Izsekošana.
9. Noklikšķiniet uz vienuma Nosūtītie pārdošanas pasūtījumi.
10. Aizvērt lapu.

