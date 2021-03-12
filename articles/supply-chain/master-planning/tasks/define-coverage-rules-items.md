---
title: Krājumu vajadzības kārtulu definēšana
description: Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.
author: ShylaThompson
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c156ae4a8a19a428378581a0d5c7dc01d86b5ec7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999885"
---
# <a name="define-coverage-rules-for-items"></a>Krājumu vajadzības kārtulu definēšana

[!include [banner](../../includes/banner.md)]

Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Šajā procedūrā ir parādīts, kā izveidot vajadzību noteikumus un ignorēt vajadzības iestatījumus noteiktajam krājumam. Tajā ir arī parādīts, kā norādīt krājumu noklusējuma iestatījumus.


## <a name="create-a-coverage-group"></a>Vajadzības grupas izveide
1. Dodieties uz **Navigācijas rūts > Moduļi > Vispārējā plānošana > Iestatīšana > Vajadzības grupas**.
2. Klikšķiniet **Jauns**.
3. Laukā **Vajadzības grupa** ierakstiet vērtību.
4. Laukā **Nosaukums** ierakstiet kādu vērtību.
5. Laukā **Kalendārs** ierakstiet vērtību. Izvēlieties kalendāru, ko vispārējā plānošana izmanto, lai izveidotu papildināšanas ieteikumus šajā grupā iekļautajiem krājumiem.  
6. Laukā **Vajadz. aprēķ. metode** atlasiet opciju. Šai procedūrai atlasiet 'Vajadzība'.  
7. Laukā **Vajadzības periods (dienās)** ievadiet '90'. Šīs grupas krājumiem vispārējā plānošana izveidos papildināšanas ieteikumus līdz 90 dienām nākotnē.  
8. Laukā **Dienas(-)** ievadiet “1”.
9. Laukā **Dienas(+)** ievadiet “1”.
10. Izvērsiet vai sakļaujiet sadaļu **Cits**.
11. Sadaļā **Drošības rezerves dienās** laukā **Pieprasījuma datumam pieskaitītā saņemšanas rezerve** ievadiet '1'. Piemēram, ja drošības rezerve ir iestatīta uz 1 dienu un pirkšanas pasūtījuma rinda ir ieplānota saņemšanai 15. maijā, tad vispārējā plānošana pielāgoto saņemšanas datumu aprēķina kā 16. maiju.  
12. Laukā **No pieprasījuma datuma atņemtā izsniegšanas rezerve** ievadiet “1”. Piemēram, ja saņemšanas rezerve ir iestatīta uz 1 dienu un pārdošanas pasūtījuma rinda ir ieplānota piegādei 15. maijā, tad vispārējā plānošana pielāgoto piegādes datumu aprēķina kā 14. maiju.  
13. Laukā **Krājuma izpildlaikam pieskaitītā atkārtotas pasūtīšanas rezerve** ievadiet “1”.
14. Noklikšķiniet uz **Saglabāt**.

## <a name="create-a-new-product"></a>Jaunas preces izveide
1. Dodieties uz **Navigācijas rūts > Moduļi > Preču informācijas pārvaldība > Preces > Tirdzniecībā izlaistās preces**.
2. Klikšķiniet **Jauns**.
3. Laukā **Preces numurs** ierakstiet vērtību.
4. Laukā **Preces nosaukums** ierakstiet vērtību.
5. In the **Krājumu modeļu grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
8. Laukā **Krājumu grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
9. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
10. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
11. Laukā **Noliktavas dimensiju grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
12. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
13. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
14. Laukā **Izsekošanas dimensiju grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
15. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
16. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
17. Noklikšķiniet uz **Labi**.

## <a name="setup-default-order-settings"></a>Iestatīt noklusējuma pasūtījuma iestatījumus
1. **Darbību rūtī** noklikšķiniet uz **Plāns**.
2. Sadaļā **Pasūtījuma iestatījumi** noklikšķiniet uz lauka **Noklusējuma pasūtījuma iestatījumi**.
3. Sadaļā **Pirkšanas pasūtījums** laukā **Noklusējuma vieta** ierakstiet vietu, ko izmantojat kā noklusējumu, kad tiek izveidoti pirkšanas pasūtījumi.
4. Laukā **Noklusējuma noliktava** ierakstiet vietu, kur šis krājums tiek glabāts.
5. Izvērsiet vai sakļaujiet sadaļu **Krājumi**.
6. Laukā **Dalītājs** ierakstiet '10'.
7. Laukā **Minimālais pasūtījuma daudzums** ierakstiet '10'.
8. Laukā **Maksimālais pasūtījuma daudzums** ierakstiet '100'.
9. Laukā **Standarta pasūtījuma daudzums** ierakstiet '10'.
10. Laukā **Pirkšanas izpildes laiks** ievadiet kādu skaitli.
11. Atzīmējiet izvēles rūtiņu **Darba dienas** vai noņemiet tās atzīmi.
12. Noklikšķiniet uz **Saglabāt**.
13. Laukā **Noklusējuma pasūtījuma veids** atlasiet “Pirkšanas pasūtījums”.
14. Noklikšķiniet uz **Saglabāt**.
15. Aizvērt lapu. Aizveriet lapu Pasūtījuma noklusējuma iestatījumi.  

## <a name="add-an-item-to-a-coverage-group"></a>Pievienot krājumu kādai vajadzības grupai
1. Izvērsiet vai sakļaujiet sadaļu **Plāns**.
2. Laukā **Vajadzības grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
3. Šajā sarakstā atrodiet izveidoto **Vajadzības grupu**.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.

## <a name="create-item-coverage-rules"></a>Izveidot krājumu vajadzības kārtulas
1. **Darbību rūtī** noklikšķiniet uz **Plāns**.
2. Sadaļā **Vajadzība** noklikšķiniet uz **Krājumu vajadzība**.
3. Klikšķiniet **Jauns**.
4. Noklikšķiniet uz cilnes **Vispārīgi**.
5. Atzīmējiet izvēles rūtiņu iestatījumu **Ignorēt vajadzības grupu** virsrakstā.
6. Laukā **Vajadzības periods (dienās)** ievadiet '60'. Lai gan krājumi vajadzības grupā Pieprasījums tiek plānoti 90 dienas uz priekšu, šis krājums tiks plānots 60 dienas uz priekšu.  
7. Laukā **Dienas(-)** ievadiet “2”.
8. Laukā **Dienas(+)** ievadiet “2”.
9. Noklikšķiniet uz cilnes **Izpildes laiks**.
10. Atzīmējiet izvēles rūtiņu **Pirkšana** virsrakstā.
11. Laukā **Pirkšanas laiks** ievadiet “5”.
12. Noklikšķiniet uz **Saglabāt**.

