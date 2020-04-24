---
title: MK uzturēšana preces konfigurācijas modelim
description: Šīs procedūras veikšanai ir nepieciešams esošs preces konfigurācijas modelis.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1aa2a22056ff4435d4c66f13c170aeadc02fbe03
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203576"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>MK uzturēšana preces konfigurācijas modelim

[!include [banner](../../includes/banner.md)]

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

