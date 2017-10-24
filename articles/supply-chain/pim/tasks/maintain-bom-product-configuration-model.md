--- 
title: "MK uzturēšana preces konfigurācijas modelim"
description: "Šīs procedūras veikšanai ir nepieciešams esošs preces konfigurācijas modelis."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c017d7719ac6af43b0c8a162080bb753587df030
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="maintain-bom-for-a-product-configuration-model"></a>MK uzturēšana preces konfigurācijas modelim

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šīs procedūras veikšanai ir nepieciešams esošs preces konfigurācijas modelis. Augstas kvalitātes skaļruņu modelis demonstrācijas uzņēmumā USMF tiek izmantots, lai izveidotu šo procedūru.


## <a name="add-a-bom-line"></a>MK rindas pievienošana
1. Noklikšķiniet uz Preces varianta modeļa definīcija.
2. Noklikšķiniet uz Preču konfigurācijas modeļi.
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlasiet augstas kvalitātes skaļruni šai procedūrai.  
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Izvērsiet sadaļu MK rindas.
6. Noklikšķiniet uz Pievienot.
7. Laukā Nosaukums ierakstiet kādu vērtību.
8. Apraksta laukā ierakstiet vērtību.
9. Noklikšķiniet uz Saglabāt.

## <a name="add-bom-line-details"></a>MK rindas informācijas pievienošana
1. Noklikšķiniet uz Detalizēta informācija par MK rindu.
2. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
    * Piemēram, varat atlasīt krājumu M0055.  
    * Katram MK rindas rekvizītam varat atlasīt, vai tam tiek piešķirta fiksēta vērtība vai arī tas tiek kartēts uz atribūtu.  
3. Atzīmējiet izvēles rūtiņu Iestatīt.
4. Laukā Aprēķins atlasiet Jā.
    * Iestatot rekvizītam Aprēķins vienumu Jā, tiek nodrošināta MK rindas iekļaušana izmaksu aprēķinos.  
5. Noklikšķiniet uz cilnes Iestatījumi.
6. Atzīmējiet izvēles rūtiņu Iestatīt.
7. Laukā Daudzums ievadiet skaitli.
    * Daudzuma lauks nosaka, kāds krājumu daudzums tiks iekļauts MK. Tas varētu būt piemērots atribūtu kartēšanai.  
8. Noklikšķiniet uz cilnes Dimensija.
    * Pārbaudiet, vai kāda no preču dimensijām ir aktīva un tādējādi tai jābūt piešķirtai vērtībai vai atribūtam.  
9. Noklikšķiniet uz OK.


