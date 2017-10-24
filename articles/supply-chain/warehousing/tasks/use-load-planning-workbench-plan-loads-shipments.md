--- 
title: "Kravu un sūtījumu plānošana, izmantojot noslodzes plānošanas rīku"
description: "Šajā procedūrā tiek parādīts, kā lietot noslodzes plānošanas rīku, lai izveidotu kravu pārdošanas pasūtījumam."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f840a4c15305af5f55451ae7f1cec2da25e685a4
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>Kravu un sūtījumu plānošana, izmantojot noslodzes plānošanas rīku

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā tiek parādīts, kā lietot noslodzes plānošanas rīku, lai izveidotu kravu pārdošanas pasūtījumam. Kā priekšnosacījumu mēs vispirms izveidosim pārdošanas pasūtījumu. Šī procedūra ir daļa no transportēšanas koordinatora ikdienas darba. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.


## <a name="create-a-sales-order"></a>Pārdošanas pasūtījuma izveidošana
1. Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Debitora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Konta US-004 atlase
5. Noklikšķiniet uz Labi.
6. Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
7. Atlasiet krājumu A0001.
    * A0001 ir iespējots transportēšanas pārvaldībai.  
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Laukā Daudzums ievadiet skaitli.
10. Laukā Noliktava ierakstiet "24".
    * Šajā piemērā atlasiet noliktavu 24. Šī noliktava ir iespējota transportēšanas pārvaldībai un papildu noliktavas vadībai.  
11. Noklikšķiniet uz Saglabāt.
12. Aizvērt lapu.

## <a name="create-a-new-load"></a>Jaunas noslodzes izveide
1. Dodieties uz Transportēšanas pārvaldība > Plānošana > Kravu plānošanas rīks.
2. Noklikšķiniet uz cilnes Pārdošanas rindas.
    * Tagad varat izveidot kravu tikko izveidotajam pārdošanas pasūtījumam. Kravas var veidot, balstoties uz piedāvājumu un pieprasījumu no pirkšanas pasūtījumiem, pārsūtīšanas pasūtījumiem un pārdošanas pasūtījumiem.  
3. Darbību rūtī noklikšķiniet uz Piedāvājums un pieprasījums.
4. Noklikšķiniet uz Jaunai noslodzei.
5. Laukā Kravas veidnes ID noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Kravas veidne nosaka maksimālos mērījumus visas kravas svaram un tilpumam. Piemēram, kravas veidne var atspoguļot konteinera vai kravas automašīnas lielumu.  
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
7. Noklikšķiniet uz OK.

## <a name="rate-and-route-the-load"></a>Noslodzes novērtēšana un maršrutēšana
1. Noklikšķiniet uz Novērtēšana un maršrutēšana.
2. Noklikšķiniet uz Likmju un maršrutu rīks.
3. Noklikšķiniet uz Likmes izvēle.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Noklikšķiniet uz Piešķirt.
6. Aizvērt lapu.
7. Aizvērt lapu.


