--- 
title: "Piegādes"
description: "Šajā procedūrā parādīts, kā iestatīt nosūtījuma pārvadātāju un definēt tādu informāciju kā pakalpojums, piegādes režīms, transportēšanas norēķini, transportēšanas ierobežojumi un nosūtīšanas likme."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
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
ms.openlocfilehash: e27be049bebd63c9266029b8981874417a9f0a8c
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-shipping-carriers"></a>Piegādes

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā iestatīt nosūtījuma pārvadātāju un definēt tādu informāciju kā pakalpojums, piegādes režīms, transportēšanas norēķini, transportēšanas ierobežojumi un nosūtīšanas likme. Transportēšanas koordinators pēc tam var piešķirt nosūtījuma pārvadātāju ienākošai vai izejošai kravai.


## <a name="create-a-new-shipping-carrier"></a>Jauna nosūtījumu pārvadātāja izveide
1. Pārejiet uz sadaļu Transportēšanas pārvaldība > Iestatījumi > Pārvadātāji > Sūtījumu pārvadātāji.
2. Noklikšķiniet uz Jauns.
3. Ierakstiet vērtību laukā Sūtījumu pārvadātājs.
4. Laukā Nosaukums ierakstiet kādu vērtību.
5. Laukā Režīms noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>Vispārējās informācijas ievade par nosūtījumu pārvadātāju
1. Pārslēdziet sadaļas Pārskats paplašinājumu.
2. Atzīmējiet vai noņemiet atzīmi no izvēles rūtiņas Aktivizēt nosūtīšanas pārvadātāju.
3. Laukā Kreditors noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Atlasiet kreditora kontu, kuram piešķirt nosūtījuma pārvadātāju.  
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Atlasiet opciju laukā Transportēšanas norēķinu veids.
    * Atlasiet Manuāli, lai izmantotu transportēšanas norēķinu lapu, vai atlasiet EDI, lai atjauninātu norēķinus, izmantojot elektronisko datu apmaiņu (EDI).  
7. Atzīmējiet vai noņemiet atzīmi no izvēles rūtiņas Aktivizēt pārvadātāja vērtējumu.

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>Nepieciešamo pakalpojumu izveide sūtījumu pārvadātājam
1. Pārslēdziet sadaļas Pakalpojumi paplašinājumu.
2. Noklikšķiniet uz Jauns.
3. Sarakstā atzīmējiet atlasīto rindu.
4. Ierakstiet vērtību laukā Pārvadātāja pakalpojums.
5. Laukā Nosaukums ierakstiet kādu vērtību.
6. Laukā Transportēšanas metode noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
7. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.

## <a name="set-up-the-address-for-the-carrier-optional"></a>Iestatiet pārvadātāja adresi (nav obligāti)
1. Pārslēdziet sadaļas Adreses izvēršanu.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums vai apraksts ierakstiet kādu vērtību.
4. Laukā Valsts/reģions noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Laukā Pasta indekss noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
7. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Laukā Iela ierakstiet kādu vērtību.
10. Noklikšķiniet uz OK.

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>Iestatiet nosūtījumu pārvadātāja novērtēšanas profilu
1. Pārslēdziet sadaļas Novērtējuma profili izvēršanu.
2. Noklikšķiniet uz Jauns.
3. Sarakstā atzīmējiet atlasīto rindu.
4. Ierakstiet vērtību laukā Novērtējuma profils.
5. Laukā Nosaukums ierakstiet kādu vērtību.
6. Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
7. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
10. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
11. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
12. Laukā Likmes noteikšanas programma noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Atlasiet likmes noteikšanas programmu, kura atbilst līgumam, kas jums noslēgts ar pārvadātāju.  
13. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
14. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
15. Laukā Likmes šablons noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
16. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
17. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
18. Laukā Tranzīta laika noteikšanas programma noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
19. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
20. Noklikšķiniet uz Saglabāt.


