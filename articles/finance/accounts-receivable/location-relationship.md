---
title: Atrašanās vietas un pušu attiecību tipu pievienošana
description: Šajā rakstā skaidrots, kā pievienot jaunu atrašanās vietas un puses attiecību veidu.
author: ShivamPandey-msft
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2aaf16fac658d26dc2d2a389fd5c1dbb9cbb7649
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874759"
---
# <a name="add-location-and-party-relationship-types"></a>Atrašanās vietas un pušu attiecību tipu pievienošana 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a>Vietu lomu pievienošana

Pastāv divi tālāk aprakstītie veidi, kā pievienot jaunas atrašanās vietas lomas adresei un kontaktinformācijai.

-  Pievienojiet šo informāciju lapā **Adreses un kontaktinformācijas nolūks**. Jaunā loma tiks saglabāta tabulā **LogisticsLocationRole** ar iestatījumu type = 0, kas norāda, ka šī loma nav sistēmas loma, kas tiek definēta uzskaitījumā **LogisticsLocationRoleType** un tā paplašinājumos. Lietotājs šo lomu varēs izmantot, veidojot adresi vai kontaktinformāciju.

    ![Adreses un kontaktinformācijas nolūks.](media/Address-Contact.PNG)

-  Pievienojiet šo vienumu uzskaitījuma **LogisticsLocationRoleType** paplašinājumam un ļaujiet tam aizpildīties, izmantojot datubāzes sinhronizēšanas procesu.

    1.  Izveidojiet paplašinājumu uzskaitījumam **LogisticsLocationRoleType** un pievienojiet jaunu lomu šajā paplašinājumā. 
  
        ![LogisticsLocationRoleType uzskaitījuma paplašinājums.](media/Logistics.PNG)

    2. Izveidojiet jaunu resursu failu jaunajai lomai un pēc tam piešķiriet kādu vērtību tā rekvizītiem.
     
     ![Jauns resursu fails.](media/Resource.PNG)
        
    3.  Izveidojiet datu aizpildīšanas klasi un nodrošiniet apdarinātāja metodi, lai aizpildītu jauno lomu. 

        ![Datu aizpildīšana.](media/Dirdata.PNG)

    4.  Lai pārbaudītu jaunās vietas lomas aizpildīšanu, varat izveidot izpildāmu klasi un izsaukt DirDataPopulation::insertLogisticsLocationRoles() funkcijā Main(). Pēc šī procesa izpildīšanas jums vajadzētu redzēt, ka jaunā loma ir aizpildīta tabulā **LogisticsLocationRole** ar tipu \> 0. Jaunā loma tiks rādīta lapā **Adreses un kontaktinformācijas nolūks**.

        ![Jaunas atrašanās vietas ievietošana.](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a>Pušu attiecību veidu pievienošana 

Pastāv divi tālāk aprakstītie veidi, kā pievienot jaunu attiecību tipu.

-   Pievienojiet to, izmantojot lapu **Attiecību tipu**. Jaunās attiecības tiks saglabātas tabulā **DirRelationshipTypeTable** ar iestatījumu systemtype = 0.

    ![Attiecību veidi.](media/Relationship.PNG)

-  Pievienojiet šo vienumu uzskaitījuma **DirSystemRelationshipType** paplašinājumam un ļaujiet tam aizpildīties, izmantojot datubāzes sinhronizēšanas procesu.

    1.  Izveidojiet uzskaitījuma **DirSystemRelationshipType** paplašinājumu un pievienojiet jauno attiecību tipu.

    2. Izveidojiet inicializētāju šim jaunajam tipam. Kodola kodā ir atrodami vairāki piemēri, viens no tiem ir  **DirRelationshipTypeChildInitialize**. Šī ir inicializētāja klase pušu attiecību tipam “Bērnelements”. Varat sākt darbu ar savu inicializētāju, nokopējot un ielīmējot šo kodu, un pēc tam atjaunināt iezīmētos apgabalus.
    
    ![DirRelationshipChild inicializēšana.](media/DirRelationship.PNG)

    3.  Lai pārbaudītu jaunā attiecību tipa aizpildīšanu, varat izveidot izpildāmu klasi un izsaukt DirDataPopulation::insertDirRelationshipTypes() funkcijā Main(). Jums vajadzētu redzēt jauno attiecību tipu tabulā **DirRelationshipTypeTable**, un jaunais attiecību tips būs pieejams lapā **Attiecību tipi**.

        ![Izpildāma klase.](media/Runnable.PNG)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
