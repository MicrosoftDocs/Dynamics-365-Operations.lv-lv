---
title: Lean ražošanas procesa pārsūtīšanas aktivitāšu izveide
description: Lean ražošanas procesa pārsūtīšanas aktivitāšu izveide.
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2411dc51dc1b85499edb30d9a580f396277a5bd9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828878"
---
# <a name="create-transfer-activities-for-lean-manufacturing"></a>Lean ražošanas procesa pārsūtīšanas aktivitāšu izveide

[!include [banner](../../includes/banner.md)]

Lean manufacturing pārsūtīšanas aktivitāšu izveide. 

Priekšnosacījumi: 

1. Ir jāizveido ražošanas plūsma un versija, kas nav aktīva.

2. Ir jāizveido avota un mērķa noliktava un novietojumi. Ja nepieciešams, jāizveido uzpildīšana vai papildināta darba šūna.


## <a name="find-the-production-flow-version"></a>Ražošanas plūsmas versijas atrašana
1. Pārejiet uz sadaļu Ražošanas kontrole > Iestatījumi > Racionālās ražošanas plūsma > Ražošanas plūsmas.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Ņemiet vērā, ka ražošanas plūsmai jābūt versijai melnraksta statusā.  
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.

## <a name="create-a-new-activity"></a>Jaunas aktivitātes izveide
1. Noklikšķiniet uz Aktivitātes.
    * Nodrošiniet, lai atlasītajai ražošanas plūsmai būtu versija melnrakstā un atlasiet šo versiju.  
2. Noklikšķiniet uz Izveidojiet jaunu plāna aktivitāti.
3. Noklikšķiniet uz Tālāk.
4. Laukā Nosaukums ierakstiet kādu vērtību.
5. Laukā Aktivitātes tips atlasiet "Pārsūtīšana".
6. Laukā Apstrādes daudzums ievadiet skaitli.
7. Noklikšķiniet uz Tālāk.

## <a name="select-the-work-cells"></a>Darba šūnu atlase
1. Laukā Papildināšana noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Lai izmantotu darba šūnu izvades vietu kā avota novietojumu pārsūtīšanas aktivitātē, atlasiet darba šūnu. To pašu var izdarīt ar papildinātu darba šūnu, kas nosaka pārsūtīšanas aktivitātes mērķa novietojumu.  
2. Sarakstā noklikšķiniet uz saites atlasītajā rindā.

## <a name="define-the-inventory-updates"></a>Krājumu atjauninājumu definēšana
1. Laukā Preces tips atlasiet opciju.
    * Ņemiet vērā, ka pārsūtīšana nemaina preces tipu. Varat pārsūtīt pabeigtās preces vai daļēji pabeigtas preces (pārsūtīšana starp divām ražošanas plūsmas aktivitātēm un, iespējams, Kanban plūsmu).     Pārsūtot pabeigtās preces, varat atlasīt, vai izdošanas vai saņemšanas rezultātā tiek radīta krājuma transakcija.  

## <a name="define-the-transfer-locations"></a>Pārsūtīšanas novietojumu definēšana
1. Noklikšķiniet uz Tālāk.
2. Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
7. Lauka Kravas pārvadātājs atlasiet "Nosūtītājs".
    * Opcijas ietver: Kravas nosūtītājs — organizācija, kas darbina nosūtīšanas noliktavu, Saņēmējs — organizācija, kas darbina saņemšanas noliktavu, Pārvadātājs — trešās puses kreditors. Ja darbinoša organizācija ir kreditors, pārsūtīšanas aktivitātei nepieciešams apakšuzņēmuma līgums.  
8. Noklikšķiniet uz Tālāk.

## <a name="define-the-activity-times"></a>Aktivitātes laiku definēšana
1. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Ir nepieciešams noteikt Izpildlaiku. Izpildlaiks tiek izmantots, lai aprēķinātu izmaksas un Kanban darbu caurlaides laiku. Izpildlaiki netiek lietoti, lai aprēķinātu noslodzes grafiku un patēriņu, kuri tiek aprēķināti pēc cikla laika, atvasināti no ražošanas plūsmas versijas uzdevuma.  
2. Laukā Laiks ievadiet skaitli.
3. Laukā Mērvienība ierakstiet vērtību.
4. Atlasiet Laika vienība.
5. Laukā Uz daudzumu ierakstiet kādu skaitli.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Gaidīšanas laiki nav obligāti.  
7. Laukā Laiks ievadiet skaitli.
8. Laukā Mērvienība ierakstiet vērtību.
9. Atlasiet Laika vienība.
10. Laukā Uz daudzumu ierakstiet kādu skaitli.
11. Noklikšķiniet uz Tālāk.
12. Noklikšķiniet uz Pabeigt.
13. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]