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
ms.openlocfilehash: 0987ae1e9cfbb1e2d2a957a5fd1ad82257292c0a
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804106"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>Bankas iestāžu iestatīšana un garantijas vēstuļu grāmatošanas profili

[!include [banner](../../includes/banner.md)]

Šis uzdevums izveido bankas iestādes un grāmatošanas profilu, kas ir vajadzīgs, lai apstrādātu garantijas vēstuli.



Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF. 




## <a name="general-ledger-parameter"></a>Virsgrāmatas parametrs
1. Pārejiet uz **sadaļu Kases un bankas > un > kases un bankas pārvaldības parametrus**.
2. Izvērsiet sadaļu **Bankas** dokuments.
3. Atlasiet opciju **Iespējot garantijas vēstuli** .
4. Laukā **Darbību** žurnāls noklikšķiniet uz nolaižamās izvēlnes pogas, lai atvērtu uzmeklēšanu.
5. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
7. Noklikšķiniet uz **cilnes Numuru sērijas** .
    * Numuru sērijas koda definēšana garantijas vēstules numuram un garantijas vēstuļu transakciju atsaucēm  
8. Noklikšķiniet uz **Saglabāt**.
9. Aizvērt lapu.

## <a name="create-bank-facility"></a>Bankas iestādes izveide
1. Dodieties uz **sadaļu Skaidras naudas > bankas > bankas iestādes**.
2. Klikšķiniet **Jauns**.
3. Laukā **Iestādes grupa** ievadiet bankas iestādes grupas nosaukumu garantijas vēstules darbībai.
4. Laukā **Apraksts** ierakstiet kādu vērtību.
5. Noklikšķiniet uz **Saglabāt**.
6. Noklikšķiniet uz **cilnes Iestādes** tipi.
7. Klikšķiniet **Jauns**.
8. Laukā **Kredīta tips** ievadiet bankas iestādes tipa nosaukumu, kas saistīts ar bankas iestādes līgumu.
9. Laukā **Apraksts** ierakstiet kādu vērtību.
10. Laukā **Iestādes grupa** noklikšķiniet uz nolaižamās izvēlnes pogas, lai atvērtu uzmeklēšanu.
11. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
12. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
13. Laukā **Kredīta raksturs** atlasiet opciju.
14. Noklikšķiniet uz **Saglabāt**.
15. Aizvērt lapu.

## <a name="bank-posting-profile"></a>Bankas grāmatošanas profils
1. Dodieties uz **sadaļu Kases un bankas > un > bankas dokumentu grāmatošanas metodi**.
2. Klikšķiniet **Jauns**.
3. Laukā **Konta/grupas** numurs noklikšķiniet uz nolaižamās izvēlnes pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Laukā **Nosegšanas** konts atlasiet galveno nosegšanas kontu.
7. Laukā **Izmaksu** konts atlasiet kontu izdevumu darbībām.
8. Laukā Uzcenojuma **konts** atlasiet kontu uzcenojuma darbībai.
9. Laukā **Likvidācijas** konts atlasiet likvidācijas kontu garantijas vēstules darbībai. 
10. Noklikšķiniet uz **Saglabāt**.
11. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
