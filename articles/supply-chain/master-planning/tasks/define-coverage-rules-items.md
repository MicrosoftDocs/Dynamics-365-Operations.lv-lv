---
title: Krājumu vajadzības kārtulu definēšana
description: Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 02aa3b2b7924cdf6317225bfce23f182aa390b8c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "320631"
---
# <a name="define-coverage-rules-for-items"></a>Krājumu vajadzības kārtulu definēšana

[!include [task guide banner](../../includes/task-guide-banner.md)]

Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Šajā procedūrā ir parādīts, kā izveidot vajadzību noteikumus un ignorēt vajadzības iestatījumus noteiktajam krājumam. Tajā ir arī parādīts, kā norādīt krājumu noklusējuma iestatījumus.


## <a name="create-a-coverage-group"></a>Vajadzības grupas izveide
1. Dodieties uz Vajadzības grupas.
2. Noklikšķiniet uz Jauns.
3. Laukā Vajadzības grupa ierakstiet vērtību.
4. Laukā Nosaukums ierakstiet kādu vērtību.
5. Laukā Kalendārs ierakstiet vērtību.
    * Izvēlieties kalendāru, ko vispārējā plānošana izmanto, lai izveidotu papildināšanas ieteikumus šajā grupā iekļautajiem krājumiem.  
6. Laukā Vajadz. aprēķ. metode atlasiet opciju.
    * Šai procedūrai atlasiet Vajadzība.  
7. Laukā Vajadzības periods (dienās) ievadiet “90”.
    * Šīs grupas krājumiem vispārējā plānošana izveidos papildināšanas ieteikumus līdz 90 dienām nākotnē.  
8. Laukā Dienas(-) ievadiet “1”.
9. Laukā Dienas(+) ievadiet “1”.
10. Izvērsiet vai sakļaujiet sadaļu Cits.
11. Laukā Pieprasījuma datumam pieskaitītā saņemšanas rezerve ievadiet “1”.
    * Piemēram, ja drošības rezerve ir iestatīta uz 1 dienu un pirkšanas pasūtījuma rinda ir ieplānota saņemšanai 15. maijā, tad vispārējā plānošana pielāgoto saņemšanas datumu aprēķina kā 16. maiju.  
12. Laukā No pieprasījuma datuma atņemtā izsniegšanas rezerve ievadiet “1”.
    * Piemēram, ja saņemšanas rezerve ir iestatīta uz 1 dienu un pārdošanas pasūtījuma rinda ir ieplānota piegādei 15. maijā, tad vispārējā plānošana pielāgoto piegādes datumu aprēķina kā 14. maiju.  
13. Laukā Krājuma izpildlaikam pieskaitītā atkārtotas pasūtīšanas rezerve ievadiet “1”.
14. Noklikšķiniet uz Saglabāt.

## <a name="create-a-new-product"></a>Izveidot jaunu preci
1. Dodieties uz Izlaistās preces.
2. Noklikšķiniet uz Jauns.
3. Laukā Preces numurs ierakstiet vērtību.
4. Laukā Preces nosaukums ierakstiet kādu vērtību.
5. Laukā Krājumu modeļu grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
8. Laukā Krājumu grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
9. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
10. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
11. Laukā Noliktavas dimensiju grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
12. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
13. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
14. Laukā Izsekošanas dimensiju grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
15. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
16. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
17. Noklikšķiniet uz OK.

## <a name="setup-default-order-settings"></a>Iestatīt noklusējuma pasūtījuma iestatījumus
1. Darbību rūtī noklikšķiniet uz Plānot.
2. Noklikšķiniet uz Pasūtījuma noklusējuma iestatījumi.
3. Laukā Pirkšanas vieta ierakstiet vietu, ko izmantojat kā noklusējumu, kad tiek izveidoti pirkšanas pasūtījumi.
4. Laukā Krājumu atrašanās vieta ierakstiet vietu, kur šis krājums tiek glabāts.
5. Izvērsiet vai sakļaujiet sadaļu Krājumi.
6. Vienumam Vairāki iestatiet vērtību “10”.
7. Vienumam Min. pasūtījuma daudzums iestatiet vērtību “10”.
8. Vienumam Maks. pasūtījuma daudzums iestatiet vērtību “100”.
9. Vienumam Standarta pasūtījuma daudzums iestatiet vērtību “10”.
10. Laukā Pirkšanas izpildes laiks ievadiet kādu skaitli.
11. Atzīmējiet izvēles rūtiņu Darba dienas vai noņemiet tās atzīmi.
12. Noklikšķiniet uz Saglabāt.
13. Laukā Noklusējuma pasūtījuma tips atlasiet “Pirkšanas pasūtījums”.
14. Noklikšķiniet uz Saglabāt.
15. Aizvērt lapu.
    * Aizveriet lapu Pasūtījuma noklusējuma iestatījumi.  

## <a name="add-an-item-to-a-coverage-group"></a>Pievienot krājumu kādai vajadzības grupai
1. Izvērsiet vai sakļaujiet sadaļu Plāns.
2. Laukā Vajadzības grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
3. Šajā sarakstā atrodiet izveidoto vajadzības grupu.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.

## <a name="create-item-coverage-rules"></a>Izveidot krājumu vajadzības kārtulas
1. Darbību rūtī noklikšķiniet uz Plānot.
2. Noklikšķiniet uz Krājumu vajadzība.
3. Noklikšķiniet uz Jauns.
4. Noklikšķiniet uz cilnes Vispārīgi.
5. Atzīmējiet izvēles rūtiņu lauka Ignorēt seguma grupas iestatījumus virsrakstā.
6. Laukā Vajadzības periods (dienās) ievadiet “60”.
    * Lai gan krājumi vajadzības grupā Pieprasījums tiek plānoti 90 dienas uz priekšu, šis krājums tiks plānots 60 dienas uz priekšu.  
7. Laukā Dienas(-) ievadiet “2”.
8. Laukā Dienas(+) ievadiet “2”.
9. Noklikšķiniet uz cilnes Izpildes laiks.
10. Atzīmējiet izvēles rūtiņu lauka Pirkšana virsrakstā.
11. Laukā Pirkšanas laiks ievadiet “5”.
12. Noklikšķiniet uz Saglabāt.

