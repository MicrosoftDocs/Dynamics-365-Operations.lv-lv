---
title: Lean manufacturing procesa aktivitāšu izveide
description: Izveidojiet lean manufacturing procesa aktivitāti.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup, PlanActivityDetails, KanbanJobPickingListPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3cb096eb25fa449b521c370bcb1677e38e399658
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983402"
---
# <a name="create-process-activities-for-lean-manufacturing"></a>Lean manufacturing procesa aktivitāšu izveide

[!include [banner](../../includes/banner.md)]

Izveidojiet lean manufacturing procesa aktivitāti. 

Priekšnosacījumi: 

1. Ir jāizveido ražošanas plūsma un versija, kas nav aktīva.

2. Ir jāizveido darba šūna.


## <a name="find-the-production-flow-version"></a>Ražošanas plūsmas versijas atrašana
1. Pārejiet uz sadaļu Ražošanas kontrole > Iestatījumi > Racionālās ražošanas plūsma > Ražošanas plūsmas.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.

## <a name="create-a-new-activity"></a>Jaunas aktivitātes izveide
1. Noklikšķiniet uz Aktivitātes.
    * Nodrošiniet, lai atlasītajai ražošanas plūsmai būtu versija melnrakstā un atlasiet šo versiju.  
2. Noklikšķiniet uz Izveidojiet jaunu plāna aktivitāti.
3. Noklikšķiniet uz Tālāk.
4. Laukā Nosaukums ierakstiet kādu vērtību.
5. Laukā Nosaukums ierakstiet kādu vērtību.
    * Ņemiet vērā, ka dotās ražošanas plūsmas nosaukumam jābūt unikālam visās versijās.  
6. Laukā Apstrādes daudzums ievadiet skaitli.
    * Ņemiet vērā, ka neatkarīgi no tā, kāds darba apjoms tiks apstrādāts, tas ir minimālais daudzums uz darbu, lai aprēķinātu darbaspēka izmaksas. Ja darbu daudzumi atšķiras no šī daudzuma, tiks izveidota darbaspēka izmaksu novirze.  
7. Noklikšķiniet uz Tālāk.

## <a name="select-the-work-cell"></a>Darba šūnas atlase
1. Laukā Darba šūna noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
2. Sarakstā noklikšķiniet uz saites atlasītajā rindā.

## <a name="define-the-inventory-updates"></a>Krājumu atjauninājumu definēšana
1. Atzīmējiet vai notīriet izvēles rūtiņu Atjauniniet rīcībā esošo krājumu saņemšanu.
    * Ja Atjauniniet rīcībā esošos krājumus = Nē, varat definēt aktivitāti, lai saņemtu daļēji pabeigtu preci (aktivitāte nesasniedz nākamo MK līmeni).    Varat arī atlasīt patērēt daļēji pabeigtās preces.  

## <a name="define-the-picking-activities"></a>Izdošanas aktivitāšu definēšana
1. Noklikšķiniet uz Tālāk.
2. Sarakstā atzīmējiet atlasīto rindu.
    * Atlasītās darba šūnas ievades vietai tiek izveidota noklusējuma izdošanas aktivitāte.  
3. Noklikšķiniet uz Pievienot.
    * Varat izveidot papildu izdošanas aktivitātes īpašām precēm, kas nav izveidotas darba šūnu ievades aktivitātē.  
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Laukā Krājuma kods ierakstiet kādu vērtību.
6. Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Ar šo definīciju, visi aktivitātes patērētie materiāli tiek izdoti no noklusējuma ievades noliktavas un novietojuma, izņemot krājumu, kas ir definēts otrajā izdošanas aktivitātē. Šis krājums tiks izdots no citas noliktavas un novietojuma.  
7. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Atzīmējiet vai notīriet izvēles rūtiņu Reģistrēt brāķi.
10. Noklikšķiniet uz Tālāk.

## <a name="define-the-activity-times"></a>Aktivitātes laiku definēšana
1. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Ir nepieciešams noteikt Izpildlaiku. Izpildlaiks tiek izmantots, lai aprēķinātu izmaksas un Kanban darbu caurlaides laiku. Izpildlaiki netiek lietoti, lai aprēķinātu noslodzes grafiku un patēriņu, tie tiek aprēķināti pēc cikla laika, atvasināti no ražošanas plūsmas versijas uzdevuma.  
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

