---
title: MK uzturēšana preces konfigurācijas modelim
description: Šīs procedūras veikšanai ir nepieciešams esošs preces konfigurācijas modelis.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4ad73265e321b6339c061a7866b55cb2769954b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921321"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>MK uzturēšana preces konfigurācijas modelim

[!include [banner](../../includes/banner.md)]

Šīs procedūras veikšanai ir nepieciešams esošs preces konfigurācijas modelis. Augstas kvalitātes skaļruņu modelis demonstrācijas uzņēmumā USMF tiek izmantots, lai izveidotu šo procedūru.

## <a name="add-a-bom-line"></a>MK rindas pievienošana

1. Dodieties uz **Preču informācijas pārvaldība \> Preces \> Preču konfigurācijas modeļi**.
1. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlasiet augstas kvalitātes skaļruni šai procedūrai.  
1. Sarakstā atlasiet saiti atlasītajā rindā.
1. Izvērsiet sadaļu **MK rindas**.
1. Atlasiet **Pievienot**.
1. Laukā **Nosaukums** ierakstiet kādu vērtību.
1. Laukā **Apraksts** ierakstiet kādu vērtību.
1. Atlasiet **Saglabāt**.

## <a name="add-bom-line-details"></a>MK rindas informācijas pievienošana

1. Atlasiet **Detalizēta MK rindas informācija**.
2. Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību.
    * Piemēram, varat atlasīt krājumu M0055.  
    * Katram MK rindas rekvizītam varat atlasīt, vai tam tiek piešķirta fiksēta vērtība vai arī tas tiek kartēts uz atribūtu.  
3. Atzīmējiet izvēles rūtiņu **Iestatīt**.
4. Laukā **Aprēķins** atlasiet *Jā*.
    * Iestatot rekvizītam **Aprēķins** vienumu *Jā*, tiek nodrošināta MK rindas iekļaušana izmaksu aprēķinos.  
5. Atlasiet cilni **Iestatījums**.
6. Atzīmējiet izvēles rūtiņu **Iestatīt**.
7. Laukā **Daudzums** ierakstiet kādu skaitli.
    * Daudzuma lauks nosaka, kāds krājumu daudzums tiks iekļauts MK. Tas varētu būt piemērots atribūtu kartēšanai.  
8. Atlasiet cilni **Dimensija**.
    * Pārbaudiet, vai kāda no preču dimensijām ir aktīva un tādējādi tai jābūt piešķirtai vērtībai vai atribūtam.  
9. Atlasiet **Labi**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]