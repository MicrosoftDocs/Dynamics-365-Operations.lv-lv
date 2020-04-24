---
title: Sūtījumu pārvadātāju iestatīšana
description: Šajā tēmā parādīts, kā iestatīt nosūtījuma pārvadātāju un definēt tādu informāciju kā pakalpojums, piegādes režīms, transportēšanas norēķini, transportēšanas ierobežojumi un nosūtīšanas likme.
author: ShylaThompson
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e6a29dce877a53d125c5a151da6cfbb13d46b29
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201598"
---
# <a name="set-up-shipping-carriers"></a>Sūtījumu pārvadātāju iestatīšana

[!include [banner](../../includes/banner.md)]

Šajā tēmā parādīts, kā iestatīt nosūtījuma pārvadātāju un definēt tādu informāciju kā pakalpojums, piegādes režīms, transportēšanas norēķini, transportēšanas ierobežojumi un nosūtīšanas likme. Transportēšanas koordinators pēc tam var piešķirt nosūtījuma pārvadātāju ienākošai vai izejošai kravai.


## <a name="create-a-new-shipping-carrier"></a>Jauna nosūtījumu pārvadātāja izveide
1. Pārejiet uz **Navigācijas rūts > Moduļi > Transportēšanas pārvaldība > Iestatīšana > Pārvadātāji > Sūtījumu pārvadātāji**.
2. Darbību rūtī atlasiet **Jauns**.
3. Ierakstiet vērtību laukā **Sūtījumu pārvadātājs**.
4. Laukā **Nosaukums** ierakstiet kādu vērtību.
5. Laukā **Režīms** atlasiet opciju no nolaižamās izvēlnes.

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>Vispārējās informācijas ievade par nosūtījumu pārvadātāju
1. Pārslēdziet sadaļas **Pārskats** paplašinājumu.
2. Atzīmējiet vai noņemiet atzīmi no izvēles rūtiņas **Aktivizēt nosūtīšanas pārvadātāju**.
3. Laukā **Kreditora konts** atlasiet opciju no nolaižamās izvēlnes. Atlasiet kreditora kontu, kuram piešķirt nosūtījuma pārvadātāju.  
4. Atlasiet opciju laukā **Transportēšanas norēķinu veids**. Atlasiet **Manuāli**, lai izmantotu transportēšanas norēķinu lapu, vai atlasiet **EDI**, lai atjauninātu norēķinus, izmantojot elektronisko datu apmaiņu (EDI).  
5. Atzīmējiet vai noņemiet atzīmi no izvēles rūtiņas **Aktivizēt pārvadātāja vērtējumu**.

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>Nepieciešamo pakalpojumu izveide sūtījumu pārvadātājam
1. Pārslēdziet sadaļas **Pakalpojumi** paplašinājumu.
2. Atlasiet **Jauns**.
3. Ierakstiet vērtību laukā **Pārvadātāja pakalpojums**.
4. Laukā **Nosaukums** ierakstiet kādu vērtību.
5. Laukā **Pārvadāšanas metode** atlasiet opciju no nolaižamās izvēlnes.

## <a name="set-up-the-address-for-the-carrier-optional"></a>Iestatiet pārvadātāja adresi (nav obligāti)
1. Pārslēdziet sadaļas **Adreses** izvēršanu.
2. Atlasiet **Jauns**.
3. Laukā **Nosaukums vai apraksts** ierakstiet vērtību.
4. Laukā **Valsts/reģions** atlasiet opciju no nolaižamās izvēlnes.
5. Laukā **Pasta indekss** atlasiet opciju no nolaižamās izvēlnes.
6. Laukā **Iela** ierakstiet kādu vērtību.
7. Atlasiet **Labi**.

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>Iestatiet nosūtījumu pārvadātāja novērtēšanas profilu
1. Pārslēdziet sadaļas **Novērtējuma profili** izvēršanu.
2. Atlasiet **Jauns**.
3. Ierakstiet vērtību laukā **Novērtējuma profils**.
4. Laukā **Nosaukums** ierakstiet kādu vērtību.
5. Laukā **Vieta** atlasiet opciju no nolaižamās izvēlnes.
6. Laukā **Noliktava** atlasiet opciju no nolaižamās izvēlnes.
7. Laukā **Likmes noteikšanas programma** atlasiet opciju no nolaižamās izvēlnes. Atlasiet likmes noteikšanas programmu, kura atbilst līgumam, kas jums noslēgts ar pārvadātāju.  
8. Laukā **Likmes šablons** atlasiet opciju no nolaižamās izvēlnes.
9. Laukā **Pārvadājumu ilguma noteikšanas programma** atlasiet opciju no nolaižamās izvēlnes.
10. Atlasiet **Saglabāt**.

