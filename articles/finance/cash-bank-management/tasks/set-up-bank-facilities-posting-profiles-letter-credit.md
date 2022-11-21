---
title: Bankas iestāžu iestatīšana un kredītvēstuļu grāmatošanas profili
description: Šajā procedūrā ir aprakstīts, kā izveidot bankas iestādi un grāmatošanas profilu, lai apstrādātu akreditīvus.
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
ms.openlocfilehash: 7fe5b2ba43c4fcb4855c742bdb6f8209ebd92d68
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779467"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a>Bankas iestāžu iestatīšana un kredītvēstuļu grāmatošanas profili

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir aprakstīts, kā izveidot bankas iestādi un grāmatošanas profilu, lai apstrādātu akreditīvus. 

Šajos uzdevumos tiek izmantots demonstrācijas uzņēmums "USMF".


## <a name="general-ledger-parameter"></a>Virsgrāmatas parametrs
1. Pārejiet uz sadaļu **Skaidras naudas un bankas pārvaldība > Iestatīšana > Skaidras naudas un bankas pārvaldības parametri**.
2. Izvērsiet sadaļu Bankas **dokumenti**.
3. **Atlasiet opciju Iespējot importēšanas akreditīvu**.
4. **Atlasiet opciju Iespējot eksporta akreditīvu**.
5. Noklikšķiniet uz **Saglabāt**.
6. Aizvērt lapu.

## <a name="create-bank-facility"></a>Bankas iestādes izveide
1. Pārejiet uz sadaļu **Skaidras naudas un bankas pārvaldība > Iestatīšana > Bankas iespējas**.
2. Klikšķiniet **Jauns**.
3. **Laukā Iespēju grupa** ievadiet bankas aizdevumu grupas nosaukumu.
4. **Laukā Apraksts** ievadiet bankas iespējas grupas aprakstu.
5. Noklikšķiniet uz **Saglabāt**.
6. Noklikšķiniet uz **cilnes Objektu tipi**.
7. Klikšķiniet **Jauns**.
8. **Laukā Objekta tips** ievadiet unikālu kodu.
9. Laukā **Apraksts** ierakstiet kādu vērtību.
10. **Laukā Objekta grupa** noklikšķiniet uz nolaižamās izvēlnes pogas, lai atvērtu uzmeklēšanu.
11. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
12. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
13. **Laukā Facility nature (Mehānisma daba**) atlasiet bankas mehānisma veidu.
14. Noklikšķiniet uz **Saglabāt**.
15. Aizvērt lapu.

## <a name="bank-posting-profile"></a>Bankas grāmatošanas profils
1. Pārejiet uz sadaļu **Skaidras naudas un bankas pārvaldība > Iestatīšana > Bankas dokumentu publicēšanas profils**.
2. Klikšķiniet **Jauns**.
3. **Laukā Account/Group number (Konts/grupas numurs**) noklikšķiniet uz nolaižamās izvēlnes pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Atlasiet galveno norēķinu kontu.
    * Šis konts tiek izmantots, aprēķinot naudas plūsmas prognozi.  
7. Laukā **Maksas konts** atlasiet kontu izdevumu transakcijām.
8. **Laukā Maržas konts** atlasiet maržas transakciju kontu.
    * Šis konts tiek debetēts, ja atvēršanas rezerve ir grāmatota un kreditēta, grāmatojot maksājumu.  
9. Noklikšķiniet uz **Saglabāt**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
