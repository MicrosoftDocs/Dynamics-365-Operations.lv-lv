---
title: " Nodarbinātā konfigurēšana"
description: Šajā procedūrā ir aprakstīts, kā konfigurēt mazumtirdzniecības darbinieku kā pārdošanas pārstāvi, kurš ir tiesīgs saņemt komisiju par pārdošanu, izmantojot POS.
author: jblucher
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 797640b487884fc487582addea274007e4ba7a7d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "362537"
---
# <a name="configure-a-worker"></a> Nodarbinātā konfigurēšana

[!include[task guide banner](../includes/task-guide-banner.md)]

Šajā procedūrā ir aprakstīts, kā konfigurēt mazumtirdzniecības darbinieku kā pārdošanas pārstāvi, kurš ir tiesīgs saņemt komisiju par pārdošanu, izmantojot POS. Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.


## <a name="create-a-commission-sales-group-for-the-worker"></a>Izveidot darbinieka komisijas pārdošanas grupu
1. Pārejiet uz sadaļu Pārdošana un mārketings > Komisijas > Pārdošanas grupas.
    * Darbiniekus var piešķirt vienai vai vairākām pārdošanas grupām. Izmantojot POS, var izvēlēties jebkuru pārdošanas grupu, kas ietver darbiniekus no veikala adrešu grāmatas.  
2. Noklikšķiniet uz Jauns.
3. Laukā Grupa ierakstiet vērtību.
4. Laukā Nosaukums ierakstiet kādu vērtību.
5. Noklikšķiniet uz Saglabāt.
6. Darbību rūtī noklikšķiniet uz Vispārīgi.
7. Noklikšķiniet uz Pārdošanas pārstāvis.
    * Pārdošanas grupa var ietvert vairāk nekā vienu darbinieku. Komisijas starp darbiniekiem var sadalīt atbilstoši komisijas daļu definējumam.  
8. Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.
9. Ievadiet skaitli laukā Komisijas daļas.
10. Noklikšķiniet uz Saglabāt.
11. Aizvērt lapu.
12. Aizvērt lapu.

## <a name="assign-the-workers-default-sales-group"></a>Piešķirt darbinieku noklusējuma pārdošanas grupu
1. Pārejiet uz sadaļu Mazumtirdzniecība un komercija > Darbinieki > Darbinieki.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
4. Noklikšķiniet uz cilnes Mazumtirdzniecība.
    * Darbinieku var piešķirt noklusējuma pārdošanas grupai. Noklusējuma pārdošanas grupa tiks automātiski pievienota POS pārdošanas rindai, ja šī opcija ir iespējota veikala funkcionalitātes profilā.  
5. Noklikšķiniet uz Rediģēt.
6. Ievadiet vai atlasiet vērtību laukā Noklusējuma grupa.
7. Noklikšķiniet uz Saglabāt.

