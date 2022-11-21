---
title: Bankas iestāžu iestatīšana un garantijas vēstuļu grāmatošanas profili
description: Šis uzdevums izveido bankas iestādes un grāmatošanas profilu, kas ir vajadzīgs, lai apstrādātu garantijas vēstuli.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1bfdef0cd535f47bb1df9fb7494043d3dd519c5b
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779885"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>Bankas iestāžu iestatīšana un garantijas vēstuļu grāmatošanas profili

[!include [banner](../../includes/banner.md)]

Šis uzdevums izveido bankas iestādes un grāmatošanas profilu, kas ir vajadzīgs, lai apstrādātu garantijas vēstuli.



Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF. 




## <a name="general-ledger-parameter"></a>Virsgrāmatas parametrs
1. Pārejiet uz sadaļu **Skaidras naudas un bankas pārvaldība > Iestatīšana > Skaidras naudas un bankas pārvaldības parametri**.
2. Izvērsiet sadaļu Bankas **dokumenti**.
3. **Atlasiet opciju Iespējot garantijas** vēstuli.
4. **Laukā Transakciju žurnāls** noklikšķiniet uz nolaižamās izvēlnes pogas, lai atvērtu uzmeklēšanu.
5. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
7. Noklikšķiniet uz **cilnes Numuru sērijas**.
    * Numuru sērijas koda definēšana garantijas vēstules numuram un garantijas vēstuļu transakciju atsaucēm  
8. Noklikšķiniet uz **Saglabāt**.
9. Aizvērt lapu.

## <a name="create-bank-facility"></a>Bankas iestādes izveide
1. Pārejiet uz sadaļu **Skaidras naudas un bankas pārvaldība > Iestatīšana > Bankas iespējas**.
2. Klikšķiniet **Jauns**.
3. **Laukā Mehānisma grupa** ievadiet bankas aizdevumu grupas nosaukumu garantijas darījuma vēstulei.
4. Laukā **Apraksts** ierakstiet kādu vērtību.
5. Noklikšķiniet uz **Saglabāt**.
6. Noklikšķiniet uz **cilnes Objektu tipi**.
7. Klikšķiniet **Jauns**.
8. **Laukā Darījuma veids** ievadiet tā bankas iespējas veida nosaukumu, kas ir saistīts ar bankas iespējas līgumu.
9. Laukā **Apraksts** ierakstiet kādu vērtību.
10. **Laukā Objekta grupa** noklikšķiniet uz nolaižamās izvēlnes pogas, lai atvērtu uzmeklēšanu.
11. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
12. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
13. Laukā **Objekta daba atlasiet opciju.
14. Noklikšķiniet uz **Saglabāt**.
15. Aizvērt lapu.

## <a name="bank-posting-profile"></a>Bankas grāmatošanas profils
1. Pārejiet uz sadaļu **Skaidras naudas un bankas pārvaldība > Iestatīšana > Bankas dokumentu publicēšanas profils**.
2. Klikšķiniet **Jauns**.
3. **Laukā Account/Group number (Konts/grupas numurs**) noklikšķiniet uz nolaižamās izvēlnes pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Laukā **Nosegt kontu atlasiet norēķinu galveno kontu**.
7. Laukā **Maksas konts** atlasiet kontu izdevumu transakcijām.
8. **Laukā Maržas konts** atlasiet maržas transakcijas kontu.
9. Laukā **Likvidācijas konts** atlasiet garantijas vēstules darījuma likvidācijas kontu. 
10. Noklikšķiniet uz **Saglabāt**.
11. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
