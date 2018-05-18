--- 
title: "Bankas iestāžu iestatīšana un kredītvēstuļu grāmatošanas profili"
description: "Šajā procedūrā ir aprakstīts, kā izveidot bankas iestādi un grāmatošanas profilu, lai apstrādātu akreditīvus."
author: kweekley
manager: AnnBe
ms.date: 10/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 18ad27eb673745d09569f6a49c8bc66132550f35
ms.openlocfilehash: 9ad19534091bdbd8924f90174b720d818b9ed778
ms.contentlocale: lv-lv
ms.lasthandoff: 10/27/2017

---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a>Bankas iestāžu iestatīšana un kredītvēstuļu grāmatošanas profili

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir aprakstīts, kā izveidot bankas iestādi un grāmatošanas profilu, lai apstrādātu akreditīvus. 

Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums “USMF”.






## <a name="general-ledger-parameter"></a>Virsgrāmatas parametrs
1. Pārejiet uz sadaļu Kases un bankas pārvaldība > Iestatījumi > Kases un bankas pārvaldības parametri.
2. Izvērsiet sadaļu Bankas dokuments.
3. Atlasiet opciju Iespējot akreditīva importu.
4. Atlasiet opciju Iespējot akreditīva eksportu.
5. Noklikšķiniet uz Saglabāt.
6. Aizvērt lapu.

## <a name="create-bank-facility"></a>Bankas iestādes izveide
1. Pārejiet uz sadaļu Kases un bankas pārvaldība > Iestatījumi > Bankas iestādes.
2. Noklikšķiniet uz Jauns.
3. Laukā Iestādes grupa ievadiet bankas iestāžu grupas nosaukumu.
4. Laukā Apraksts ievadiet bankas iestāžu grupas aprakstu.
5. Noklikšķiniet uz Saglabāt.
6. Noklikšķiniet uz cilnes Iestādes tipi.
7. Noklikšķiniet uz Jauns.
8. Laukā Iestādes tips ierakstiet unikālu kodu.
9. Apraksta laukā ierakstiet vērtību.
10. Laukā Iestādes grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
11. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
12. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
13. Laukā Iestādes būtība atlasiet bankas iestādes būtību.
14. Noklikšķiniet uz Saglabāt.
15. Aizvērt lapu.

## <a name="bank-posting-profile"></a>Bankas grāmatošanas profils
1. Pārejiet uz sadaļu Kases un bankas pārvaldība > Iestatījumi > Bankas dokumentu grāmatošanas metode.
2. Noklikšķiniet uz Jauns.
3. Laukā Konta/grupas numurs noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Atlasiet galveno norēķinu kontu.
    * Šis konts tiek izmantots, aprēķinot naudas plūsmas prognozi.  
7. Laukā Maksājumu konts atlasiet kontu izdevumu transakcijām.
8. Laukā Uzcenojuma konts atlasiet kontu uzcenojuma transakcijām.
    * Šis konts tiek debetēts, ja atvēršanas rezerve ir grāmatota un kreditēta, grāmatojot maksājumu.  
9. Noklikšķiniet uz Saglabāt.


