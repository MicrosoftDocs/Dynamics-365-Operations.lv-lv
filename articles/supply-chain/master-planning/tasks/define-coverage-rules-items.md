---
title: Krājumu vajadzības kārtulu definēšana
description: Šajā procedūrā ir parādīts, kā izveidot vajadzību noteikumus un ignorēt vajadzības iestatījumus noteiktajam krājumam. Tajā ir arī parādīts, kā norādīt krājumu noklusējuma iestatījumus.
author: ChristianRytt
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3947c8a51facfb02012cc8e9a3ffd5887073bd9
ms.sourcegitcommit: 8c17717b800c2649af573851ab640368af299981
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/23/2021
ms.locfileid: "7860617"
---
# <a name="define-coverage-rules-for-items"></a>Krājumu vajadzības kārtulu definēšana

[!include [banner](../../includes/banner.md)]

USMF ir paraugdatu uzņēmums, kas tiek izmantots šīs procedūras izveidei. Šajā procedūrā ir parādīts, kā izveidot vajadzību noteikumus un ignorēt vajadzības iestatījumus noteiktajam krājumam. Tajā ir arī parādīts, kā norādīt krājumu noklusējuma iestatījumus.

## <a name="create-a-coverage-group"></a>Vajadzības grupas izveide

Izveidojiet vajadzības grupu, rīkojoties šādi:

1. Dodieties uz **Navigācijas rūts > Moduļi > Vispārējā plānošana > Iestatīšana > Vajadzības grupas**.
1. Atlasiet **Jauns**.
1. Laukā **Vajadzības grupa** ierakstiet vērtību.
1. Laukā **Nosaukums** ierakstiet kādu vērtību.
1. Laukā **Kalendārs** ierakstiet vērtību. Izvēlieties kalendāru, ko vispārējā plānošana izmanto, lai izveidotu papildināšanas ieteikumus šajā grupā iekļautajiem krājumiem.  
1. Laukā **Vajadzības kods** atlasiet opciju. Šai procedūrai atlasiet 'Prasība'.  
1. Laukā **Vajadzības periods (dienās)** ievadiet '90'. Šīs grupas krājumiem vispārējā plānošana izveidos papildināšanas ieteikumus līdz 90 dienām nākotnē.  
1. Laukā **Dienas(-)** ievadiet “1”.
1. Laukā **Dienas(+)** ievadiet “1”.
1. Izvērsiet vai sakļaujiet sadaļu **Cits**.
1. Sadaļā **Drošības rezerves dienās** laukā **Pieprasījuma datumam pieskaitītā saņemšanas rezerve** ievadiet '1'. Piemēram, ja drošības rezerve ir iestatīta uz 1 dienu un pirkšanas pasūtījuma rinda ir ieplānota saņemšanai 15. maijā, tad vispārējā plānošana pielāgoto saņemšanas datumu aprēķina kā 16. maiju.
1. Laukā **No pieprasījuma datuma atņemtā izsniegšanas rezerve** ievadiet “1”. Piemēram, ja saņemšanas rezerve ir iestatīta uz 1 dienu un pārdošanas pasūtījuma rinda ir ieplānota piegādei 15. maijā, tad vispārējā plānošana pielāgoto piegādes datumu aprēķina kā 14. maiju.  
1. Laukā **Krājuma izpildlaikam pieskaitītā atkārtotas pasūtīšanas rezerve** ievadiet “1”.
1. Atlasiet **Saglabāt**.

## <a name="create-a-new-product"></a>Izveidot jaunu preci

Izveidojiet vajadzības grupu, rīkojoties šādi:

1. Dodieties uz **Navigācijas rūts > Moduļi > Preču informācijas pārvaldība > Preces > Tirdzniecībā izlaistās preces**.
1. Atlasiet **Jauns**.
1. Laukā **Preces numurs** ierakstiet vērtību.
1. Laukā **Preces nosaukums** ierakstiet vērtību.
1. Laukā **Krājumu modeļu grupa** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu.
1. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
1. Sarakstā atlasiet saiti atlasītajā rindā.
1. Laukā **Krājumu grupa** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu.
1. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
1. Sarakstā atlasiet saiti atlasītajā rindā.
1. Laukā **Noliktavas dimensiju grupa** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu.
1. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
1. Sarakstā atlasiet saiti atlasītajā rindā.
1. Laukā **Izsekošanas dimensiju grupa** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu.
1. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
1. Sarakstā atlasiet saiti atlasītajā rindā.
1. Atlasiet **Labi**.

## <a name="set-up-default-order-settings"></a>Iestatīt noklusējuma pasūtījuma iestatījumus

Iestatiet pasūtījuma noklusētos iestatījumus, rīkojoties šādi:

1. **Darbību rūtī** atlasiet **Plāns**.
1. Sadaļā **Pasūtījuma iestatījumi** atlasiet **Noklusējuma pasūtījuma iestatījumi**.
1. Sadaļā **Pirkšanas pasūtījums** laukā **Noklusējuma vieta** ierakstiet vietu, ko izmantojat kā noklusējumu, kad tiek izveidoti pirkšanas pasūtījumi.
1. Laukā **Noklusējuma noliktava** ierakstiet vietu, kur šis krājums tiek glabāts.
1. Izvērsiet vai sakļaujiet sadaļu **Krājumi**.
1. Laukā **Dalītājs** ierakstiet '10'.
1. Laukā **Minimālais pasūtījuma daudzums** ierakstiet '10'.
1. Laukā **Maksimālais pasūtījuma daudzums** ierakstiet '100'.
1. Laukā **Standarta pasūtījuma daudzums** ierakstiet '10'.
1. Laukā **Pirkšanas izpildes laiks** ievadiet kādu skaitli.
1. Atzīmējiet izvēles rūtiņu **Darba dienas** vai noņemiet tās atzīmi.
1. Atlasiet **Saglabāt**.
1. Laukā **Noklusējuma pasūtījuma veids** atlasiet “Pirkšanas pasūtījums”.
1. Atlasiet **Saglabāt**.
1. Aizvērt lapu. Aizveriet lapu Pasūtījuma noklusējuma iestatījumi.  

## <a name="add-an-item-to-a-coverage-group"></a>Pievienot krājumu kādai vajadzības grupai

Pievienojiet vajadzības grupai krājumu, rīkojoties šādi:

1. Izvērsiet vai sakļaujiet sadaļu **Plāns**.
1. Laukā **Vajadzības grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
1. Šajā sarakstā atrodiet izveidoto **Vajadzības grupu**.
1. Sarakstā atlasiet saiti atlasītajā rindā.

## <a name="create-item-coverage-rules"></a>Izveidot krājumu vajadzības kārtulas

Izveidojiet krājuma vajadzības kārtulas, rīkojoties šādi:

1. **Darbību rūtī** atlasiet **Plāns**.
1. Sadaļā **Vajadzība** noklikšķiniet uz **Krājumu vajadzība**.
1. Atlasiet **Jauns**.
1. Atlasiet cilni **Vispārēji**.
1. Atzīmējiet izvēles rūtiņu iestatījumu **Ignorēt vajadzības grupu** virsrakstā.
1. Laukā **Vajadzības periods (dienās)** ievadiet '60'. Lai gan krājumi vajadzības grupā Pieprasījums tiek plānoti 90 dienas uz priekšu, šis krājums tiks plānots 60 dienas uz priekšu.  
1. Laukā **Dienas(-)** ievadiet “2”.
1. Laukā **Dienas(+)** ievadiet “2”.
1. Atlasiet cilni **Izpildes laiks**.
1. Atzīmējiet izvēles rūtiņu **Pirkšana** virsrakstā.
1. Laukā **Pirkšanas laiks** ievadiet “5”.
1. Atlasiet **Saglabāt**.

> [!NOTE]
> Ražotajiem krājumiem tiek **izmantots ražošanas** izpildes laiks, ja krājumam nav maršruta. Ja aktīvs maršruts ir saistīts ar krājumu, tad vispārējais plāns plāno pasūtījumu un aprēķina tā datumus, ņemot vērā maršruta laikus un resursu noslodzi (ja piemērojams).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
