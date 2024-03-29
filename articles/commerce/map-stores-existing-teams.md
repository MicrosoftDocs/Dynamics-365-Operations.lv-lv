---
title: Kartējiet veikalus un grupas, ja programmā Microsoft Teams ir iepriekšējas darba grupas
description: Šajā rakstā ir aprakstīts, kā kartēt veikalus un attiecīgās komandas galvenajā Dynamics 365 Commerce birojā, ja jūsu organizācija jau ir izveidojusi grupas Microsoft Teams pirms Commerce integrācijas.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 67a1a79dd74d411aa7e21000c8baaa8a069cede7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279124"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a>Kartējiet veikalus un grupas, ja programmā Microsoft Teams ir iepriekšējas darba grupas

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā kartēt veikalus un attiecīgās komandas galvenajā Dynamics 365 Commerce birojā, ja jūsu organizācija jau ir izveidojusi grupas Microsoft Teams pirms Commerce integrācijas.

Iespējams, jūsu organizācijai ir izveidotas grupas dažiem vai visiem veikaliem pirms integrēšanas Dynamics 365 Commerce un Microsoft Teams. Ja tā ir, lai izveidotu uzdevumu sinhronizāciju starp Commerce POS un Microsoft Teams ir jānodrošina veikalu un atbilstošo grupu kartēšana Commerce Headquarters.

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a>Kartēt veikalus un atbilstošās grupas programmā Commerce headquarters 

Lai kartētu veikalus un attiecīgās komandas Commerce Headquarters, rīkojieties šādi.

1. Dodieties uz **Sistēmas administrēšana \> Darbvieta \> Datu pārvaldība**.
1. Atlasiet **Eksportēt**. 
1. Darbību rūtī atlasiet **Jauns**.
1. Sadaļā **Grupas nosaukums** ievadiet "Eksportēt Teams kartēšanu".
1. Kopsavilkuma cilnē **Atlasītās entītijas** atlasiet **Pievienot entītiju**. Tiek parādīts dialoglodziņš **Pievienot entītiju**.  
1. Nolaižamajā sarakstā **Entītijas nosaukums** atlasiet **Teams kartēšana starp avotu un grupu**.
1. Nolaižamajā sarakstā **Mērķa datu formāts** atlasiet **CSV**.
1. Atlasiet **Pievienot** un pēc tam atlasiet **Aizvērt**.
1. Augšējā kreisajā stūrī zem Darbību rūts atlasiet **Eksportēt tūlīt**.
1. Sadaļā **Elementa apstrādes statuss** atlasiet **Lejupielādēt failu**.
1. Eksportētā CSV failā ievadiet šādas **SOURCETYPE**, **SOURCEID** un **TEAMID** vērtības:
    - **SOURCETYPE** vērtībā ievadiet "RetailStore". 
    - Ievadiet **SOURCEID** veikala numuru (piemēram, "000135", kas paredzēts Sanfrancisko veikalam). Veikalu numurus var atrast **Mazumtirdzniecība un komercija \> Kanāli \> Veikali**.
    - Ja tiek lietots **TEAMID**, ievadiet atbilstošo grupas ID no Microsoft Teams (piemēram, "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c"). Grupas ID informāciju varat atrast [admin.teams.microsoft.com](https://admin.teams.microsoft.com).
1. Saglabājiet CSV failu lokālajā datorā.
1. Dodieties uz **Sistēmas administrēšana \> Darbvieta \> Datu pārvaldība** un atlasiet **Importēt**.
1. Kopsavilkuma cilnē **Atlasītās entītijas** atlasiet **Pievienot failu**. Tiek parādīts dialoglodziņš **Pievienot failu**.
1. Nolaižamajā sarakstā **Entītijas nosaukums** atlasiet **Teams kartēšana starp avotu un grupu**.
1. Nolaižamajā sarakstā **Avota datu formāts** atlasiet **CSV**.
1. Atlasiet **Augšupielādēt un pievienot**, atlasiet iepriekš saglabāto CSV failu un pēc tam atlasiet **Atvērt**.
1. Dialoglodziņā **Pievienot** atlasiet **Aizvērt**.
1. Darbības rūtī atlasiet **Saglabāt** un pēc tam atlasiet **Importēt**.

Nākamajā piemēra attēlā ir parādīta **Eksporta darba grupu kartēšanas** grupa programmā Commerce ar elementiem **Pievienot entītiju** un izceltas eksportēto CSV failu galvenes.

![Eksporta darba grupu kartēšanas grupa programmā Commerce ar entītijas pievienošanas elementiem un izceltām eksportēto CSV failu galvenēm.](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> Pēc tam, kad esiet pabeidzis (-usi) precei pa solim, sekojiet soļiem [Sinhronizēt uzdevumu pārvaldību starp Microsoft Teams un POS](synchronize-tasks-teams-pos.md), lai sinhronizētu uzdevumu pārvaldību. 

## <a name="additional-resources"></a>Papildu resursi

[Dynamics 365 Commerce un Microsoft Teams integrācijas pārskats](commerce-teams-integration.md)

[Iespējot Dynamics 365 Commerce un Microsoft Teams integrāciju](enable-teams-integration.md)

[Nodrošināt Microsoft Teams no Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Sinhronizēt uzdevumu pārvaldību starp Microsoft Teams un Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Lietotāju lomu pārvaldība Microsoft Teams](manage-user-roles-teams.md)

[Dynamics 365 Commerce un Microsoft Teams integrācijas BUJ](teams-integration-faq.md)
