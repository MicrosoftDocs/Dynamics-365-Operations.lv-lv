---
title: Aprēķināt MK, izmantojot viena līmeņa struktūru (2016. gada februāris)
description: Šajā procedūrā ir parādīts, kā aprēķināt pabeigtas preces izmaksas, izmantojot viena līmeņa izvēršanu, kura ir balstīta uz izmaksu aprēķināšanas lapu.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22ed277d6f4dca3ab0a5be4ddba8982350c7e05ccbb6ade7313ac22b45fbecb1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772548"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a>Aprēķināt MK, izmantojot viena līmeņa struktūru (2016. gada februāris)

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir parādīts, kā aprēķināt pabeigtas preces izmaksas, izmantojot viena līmeņa izvēršanu, kura ir balstīta uz izmaksu aprēķināšanas lapu. Tas ir MK aprēķina sērijas sestais uzdevums. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.

1. Dodieties uz Izlaistās preces.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlasiet preci BOM_1.  
3. Darbību rūtī noklikšķiniet uz Pārvaldīt izmaksas.
4. Noklikšķiniet uz Krājuma cena.
5. Noklikšķiniet uz Aprēķināt krājuma izmaksas.
    * Lai augšējā izvēlnē redzētu šo opciju, iespējams, ir jānoklikšķina uz daudzpunktes (...).  
6. Laukā Izmaksu aprēķināšanas versija noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Šajā demonstrācijā atlasiet vērtību 10. Tā ir tā pati izmaksu aprēķināšanas versija, kas tika izmantota izmaksu cenas pievienošanai komponentiem.  
7. Noklikšķiniet uz OK.
8. Noklikšķiniet uz Skatīt detalizētu informāciju par aprēķinu.
    * Lai augšējā izvēlnē redzētu šo opciju, iespējams, ir jānoklikšķina uz daudzpunktes (...).    Izmaksu sastāvs: * 10 — atvasināts no ITEM_A, 10 — no ITEM_B, 10 — no BOM_2. Šajā gadījumā nav informācijas par BOM_2, jo tas tika ievadīts kā standarta izmaksas 10, bet nav iegūts, veicot aprēķinu.  * 7 tiek atvasināts no uzstādīšanas laika, kuram ir konstantas izmaksas, un papildu 7 tiek atvasināts no izpildlaika darbības (Process).  * Pastāv arī citas summas, kas atbilst netiešajām izmaksām.  
9. @SysTaskRecorder:_RequestClose



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]