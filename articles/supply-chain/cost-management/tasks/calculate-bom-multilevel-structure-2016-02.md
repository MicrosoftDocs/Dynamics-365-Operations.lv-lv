---
title: Aprēķināt MK, izmantojot vairāklīmeņu struktūru (2016. gada februāris)
description: Šajā procedūrā ir parādīts, kā aprēķināt pabeigtas preces izmaksas, izmantojot vairāklīmeņu izvēršanu, kura ir balstīta uz izmaksu aprēķināšanas lapu.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 24f40f1505f39889cf03b0a062cd254b10384374ab51e8b4aab59a7c0f92271c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746236"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a>Aprēķināt MK, izmantojot vairāklīmeņu struktūru (2016. gada februāris)

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]