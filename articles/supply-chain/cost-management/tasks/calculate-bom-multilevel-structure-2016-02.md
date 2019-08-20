---
title: Aprēķināt MK, izmantojot vairāklīmeņu struktūru (2016. gada februāris)
description: Šajā procedūrā ir parādīts, kā aprēķināt pabeigtas preces izmaksas, izmantojot vairāklīmeņu izvēršanu, kura ir balstīta uz izmaksu aprēķināšanas lapu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0834baf42ed6aa10acec6529513e44ff52ab754
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845646"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a>Aprēķināt MK, izmantojot vairāklīmeņu struktūru (2016. gada februāris)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā aprēķināt pabeigtas preces izmaksas, izmantojot vairāklīmeņu izvēršanu, kura ir balstīta uz izmaksu aprēķināšanas lapu. Tas ir MK aprēķina sērijas septītais uzdevums. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.

1. Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlasiet preci BOM_1.  
3. Darbību rūtī noklikšķiniet uz Pārvaldīt izmaksas.
4. Noklikšķiniet uz Krājuma cena.
5. Noklikšķiniet uz Aprēķināt krājuma izmaksas.
    * Lai augšējā izvēlnē redzētu šo opciju, iespējams, ir jānoklikšķina uz daudzpunktes (...).  
6. Laukā Izmaksu aprēķināšanas versija ievadiet vai atlasiet vērtību.
    * Atlasiet 20. izmaksu aprēķināšanas versiju, jo tās plānoto izmaksu tips un izvēršanas režīms ir Vairāklīmeņu.   Vairāklīmeņu izvēršanas režīms ir paredzēts plānotajām izmaksām un simulācijām. Tas netiek izmantots standarta izmaksām.  
7. Noklikšķiniet uz OK.
8. Noklikšķiniet uz Skatīt detalizētu informāciju par aprēķinu.
    * Lai augšējā izvēlnē redzētu šo opciju, iespējams, ir jānoklikšķina uz daudzpunktes (...).  Šajā gadījumā ievērojiet, kā BOM_2 tika aprēķināts, ņemot vērā izejmateriālu, procesu un pieskaitāmās izmaksas ar kopējo summu 29,40, nevis standarta izmaksu summu 10, kas tika aktivizēta šīs sērijas sākotnējā uzdevuma ceļvedī.  
9. Noklikšķiniet uz cilnes Izmaksu aprēķināšanas lapa.
    * Pārejot uz cilni Izmaksu aprēķināšanas lapa, izmaksu grupu kopsummas atšķiras, salīdzinājumā ar iepriekšējā uzdevuma ceļvedī veiktajiem aprēķiniem.  
10. Laukā Līmenis atlasiet “Multi”.
    * Atlasot vienumu Multi, izmaksas tiek klasificētas atbilstoši BOM_2 sastāvam, kur 10 tiek atvasināts no M1 izmaksu grupas (ITEM_C) un 15,60 tiek atvasināts no tās ražošanas, kur izmaksu grupa ir L2. Arī netiešās izmaksas atšķiras.  
11. Aizvērt lapu.
12. Aizvērt lapu.

