---
title: Degvielas rādītāja saistīšana ar pārvadātāju kā papildobjekta maksu
description: Šajā ceļvedī parādīts, kā izveidot papildobjekta piešķiri, pārvadātāja papildobjekta maksu, papildobjekta šablonu degvielas piemaksai un saistīt pārvadātāja degvielas rādītāju ar pārvadātāju.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1f69a6350a5a84ed19dcb37e174c25b112c16bd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974139"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a>Degvielas rādītāja saistīšana ar pārvadātāju kā papildobjekta maksu

[!include [banner](../../includes/banner.md)]

Šajā ceļvedī parādīts, kā izveidot papildobjekta piešķiri, pārvadātāja papildobjekta maksu, papildobjekta šablonu degvielas piemaksai un saistīt pārvadātāja degvielas rādītāju ar pārvadātāju. Pirms izpildīt šo ceļvedi ir jāiestata degvielas rādītājs. To var izdarīt, izmantojot ceļvedi "Pārvadātāja degvielas rādītāja iestatīšana". Šos iestatīšanas uzdevumus parasti veic loģistikas vadītājs. Demonstrācijas dati, kas tiek izmantoti, lai izveidotu šo procedūru, ir USMF.


## <a name="create-an-accessorial-master"></a>Papildobjekta šablona izveide
1. Dodieties uz Transportēšanas pārvaldība > Iestatīšana > Vērtējums > Papildobjekta šabloni.
2. Noklikšķiniet uz Jauns.
3. Laukā Papildobjekta šablons ierakstiet vērtību.
4. Laukā Nosaukums ierakstiet vērtību.
5. Noklikšķiniet uz Saglabāt.

## <a name="create-a-carrier-accessorial-charge"></a>Pārvadātāja papildobjekta maksas izveide
1. Dodieties uz Transportēšanas pārvaldība > Iestatīšana > Vērtējums > Pārvadātāja papildobjekta maksas.
2. Noklikšķiniet uz Jauns.
3. Laukā Pārvadātāja papildobjekta ID ierakstiet vērtību.
4. Laukā Sūtījumu pārvadātājs noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
5. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Šajā piemērā izvēlieties Kravas pārvadātājs.  
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
7. Laukā Pārvadātāja pakalpojums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Laukā Papildobjekta šablons noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
10. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Šajā piemērā izvēlieties jaunizveidoto Papildobjekta šablonu.  
11. Noklikšķiniet uz Saglabāt.

## <a name="create-an-accessorial-assignment"></a>Papildobjekta piešķires izveide
1. Noklikšķiniet uz Papildobjekta piešķires.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums ierakstiet kādu vērtību.
4. Pārslēdziet sadaļas Kritēriji paplašinājumu.
    * Kritērijos var izvēlēties vienmēr lietot degvielas piemaksu vai šim piemēram izvēlēties, ka tā piemērojama tikai noteiktā reģionā.  
5. Laukā Pasta indekss no ierakstiet vērtību.
6. Laukā Pasta indekss līdz ierakstiet vērtību.
7. Pārslēdziet sadaļas Aprēķins paplašinājumu.
    * Aprēķina sadaļā var norādīt, kā aprēķināt degvielas piemaksu. Šis aprēķins ir atkarīgs no Papildobjekta vienības, kuru izvēlējāties kā bāzi aprēķinam.  
8. Laukā Papildobjekta maksas tips atlasiet "Degvielas piemaksa".
9. Laukā Papildobjekta vienība atlasiet "Nobraukums".
10. Laukā Reģions noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
11. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
12. Noklikšķiniet uz Saglabāt.

## <a name="update-the-carrier-rating-profile"></a>Pārvadātāju novērtēšanas profila atjaunināšana
1. Pārejiet uz sadaļu Transportēšanas pārvaldība > Iestatījumi > Pārvadātāji > Sūtījumu pārvadātāji.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Pārslēdziet sadaļas Novērtējuma profili izvēršanu.
4. Noklikšķiniet uz Rediģēt.
5. Laukā Pārvadātāja degvielas rādītājs noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
7. Noklikšķiniet uz Saglabāt.

