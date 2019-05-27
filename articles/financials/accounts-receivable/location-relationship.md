---
title: Atrašanās vietas un pušu attiecību tipu pievienošana
description: Šajā tēmā ir paskaidrots, kā pievienot jaunu atrašanās vietas un pušu attiecību tipu.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 543784e8072f88c10f63e1b44921b9f2d37308c3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549702"
---
# <a name="add-location-roles-and-party-relationship-types"></a>Vietu lomu un pušu attiecību veidu pievienošana 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a>Vietu lomu pievienošana

Pastāv divi tālāk aprakstītie veidi, kā pievienot jaunas atrašanās vietas lomas adresei un kontaktinformācijai.

-  Pievienojiet šo informāciju lapā **Adreses un kontaktinformācijas nolūks**. Jaunā loma tiks saglabāta tabulā **LogisticsLocationRole** ar iestatījumu type = 0, kas norāda, ka šī loma nav sistēmas loma, kas tiek definēta uzskaitījumā **LogisticsLocationRoleType** un tā paplašinājumos. Lietotājs šo lomu varēs izmantot, veidojot adresi vai kontaktinformāciju.

    ![Adreses un kontaktinformācijas nolūks](media/Address-Contact.PNG)

-  Pievienojiet šo vienumu uzskaitījuma **LogisticsLocationRoleType** paplašinājumam un ļaujiet tam aizpildīties, izmantojot datubāzes sinhronizēšanas procesu.

    1.  Izveidojiet paplašinājumu uzskaitījumam **LogisticsLocationRoleType** un pievienojiet jaunu lomu šajā paplašinājumā. 
  
        ![LogisticsLocationRoleType](media/Logistics.PNG)

    2. Izveidojiet jaunu resursu failu jaunajai lomai un pēc tam piešķiriet kādu vērtību tā rekvizītiem.
     
     ![Jauns resursu fails](media/Resource.PNG)
        
    3.  Izveidojiet datu aizpildīšanas klasi un nodrošiniet apdarinātāja metodi, lai aizpildītu jauno lomu. 

        ![Datu aizpildīšana](media/Dirdata.PNG)

    4.  Lai pārbaudītu jaunās vietas lomas aizpildīšanu, varat izveidot izpildāmu klasi un izsaukt DirDataPopulation::insertLogisticsLocationRoles() funkcijā Main(). Pēc šī procesa izpildīšanas jums vajadzētu redzēt, ka jaunā loma ir aizpildīta tabulā **LogisticsLocationRole** ar tipu \> 0. Jaunā loma tiks rādīta lapā **Adreses un kontaktinformācijas nolūks**.

        ![Jaunas atrašanās vietas ievietošana](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a>Pušu attiecību veidu pievienošana 

Pastāv divi tālāk aprakstītie veidi, kā pievienot jaunu attiecību tipu.

-   Pievienojiet to, izmantojot lapu **Attiecību tipu**. Jaunās attiecības tiks saglabātas tabulā **DirRelationshipTypeTable** ar iestatījumu systemtype = 0.

    ![Attiecību tipi](media/Relationship.PNG)

-  Pievienojiet šo vienumu uzskaitījuma **DirSystemRelationshipType** paplašinājumam un ļaujiet tam aizpildīties, izmantojot datubāzes sinhronizēšanas procesu.

    1.  Izveidojiet uzskaitījuma **DirSystemRelationshipType** paplašinājumu un pievienojiet jauno attiecību tipu.

    2. Izveidojiet inicializētāju šim jaunajam tipam. Kodola kodā ir atrodami vairāki piemēri, viens no tiem ir  **DirRelationshipTypeChildInitialize**. Šī ir inicializētāja klase pušu attiecību tipam “Bērnelements”. Varat sākt darbu ar savu inicializētāju, nokopējot un ielīmējot šo kodu, un pēc tam atjaunināt iezīmētos apgabalus.
    
    ![DirRelationshipChild](media/DirRelationship.PNG)

    3.  Lai pārbaudītu jaunā attiecību tipa aizpildīšanu, varat izveidot izpildāmu klasi un izsaukt DirDataPopulation::insertDirRelationshipTypes() funkcijā Main(). Jums vajadzētu redzēt jauno attiecību tipu tabulā **DirRelationshipTypeTable**, un jaunais attiecību tips būs pieejams lapā **Attiecību tipi**.

        ![Izpildāma klase](media/Runnable.PNG)
