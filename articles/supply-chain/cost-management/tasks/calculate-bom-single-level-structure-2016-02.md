--- 
title: "Aprēķināt MK, izmantojot viena līmeņa struktūru (2016. gada februāris)"
description: "Šajā procedūrā ir parādīts, kā aprēķināt pabeigtas preces izmaksas, izmantojot viena līmeņa izvēršanu, kura ir balstīta uz izmaksu aprēķināšanas lapu."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: f74f8e4efc4474693f0a5b543c1300c3b64ecda0
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2018

---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a>Aprēķināt MK, izmantojot viena līmeņa struktūru (2016. gada februāris)

[!include [task guide banner](../../includes/task-guide-banner.md)]

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
    * Lai augšējā izvēlnē redzētu šo opciju, iespējams, ir jānoklikšķina uz daudzpunktes (...).    Izmaksu sastāvs: • 10 — atvasināts no ITEM_A, 10 — no ITEM_B, 10 — no BOM_2. Šajā gadījumā nav informācijas par BOM_2, jo tas tika ievadīts kā standarta izmaksas 10, bet nav iegūts, veicot aprēķinu.  • 7 tiek atvasināts no uzstādīšanas laika, kuram ir konstantas izmaksas, un papildu 7 tiek atvasināts no izpildlaika darbības (Process).  • Pastāv arī citas summas, kas atbilst netiešajām izmaksām.  
9. @SysTaskRecorder:_RequestClose


