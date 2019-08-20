---
title: Pamatlīdzekļa pārsūtīšana
description: Šajā uzdevuma ceļvedī ir parādīts, kā pamatlīdzekļa grāmatai pārsūtīt finanšu informāciju no vienas finanšu dimensiju kopas uz jaunu finanšu dimensiju kopu.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 167591cf160916f256e2d10f122eca312ba07639
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839741"
---
# <a name="transfer-a-fixed-asset"></a>Pamatlīdzekļa pārsūtīšana

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā uzdevuma ceļvedī ir parādīts, kā pamatlīdzekļa grāmatai pārsūtīt finanšu informāciju no vienas finanšu dimensiju kopas uz jaunu finanšu dimensiju kopu.  Tas izmanto grāmatveža lomu un demonstrācijas datus USMF juridiskajai personai.

1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Pamatlīdzekļi > Pamatlīdzekļi > Pamatlīdzekļi**.
2. Sarakstā atrodiet un atlasiet pārsūtāmo pamatlīdzekli.
3. Darbību rūtī noklikšķiniet uz **Pamatlīdzeklis**.
4. Noklikšķiniet uz **Pārsūtīt pamatlīdzekļus**.
5. Ievadiet datumu laukā **Pārsūtīšanas datums**.
6. Ievadiet komentārus pārsūtīšanas aprakstam.
    
    Šajā sarakstā ir redzamas visas šī pamatlīdzekļa grāmatas.  
7. Atzīmējiet grāmatas, kuras vēlaties pārsūtīt uz jauno finanšu dimensijas kopu.
    * Šajā sarakstā ir redzamas atlasītajai grāmatai esošās finanšu dimensijas vērtības.  
    * Atlasiet finanšu dimensiju, kuru vēlaties atjaunināt atlasītā pamatlīdzekļa grāmatai.  
8. Laukā **Finanšu dimensija** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Attiecīgi iestatiet citas finanšu dimensijas vērtības.  
    * Notiekot pārsūtīšanai, tiek mainītas visas finanšu dimensiju vērtības, gan ievadītajām vērtībām, gan tukšajiem laukiem. Piemēram, ja ievadāt vērtību BusinessUnit, bet laukus CostCenter un Nodaļas finanšu dimensijas atstājat tukšus. Ja jūsu konta struktūra pieļauj tukšas vērtības CostCenter un Nodaļa laukos, tad pēc pārsūtīšanas katram vērtības modelim būtu jauna BusinessUnit vērtība un tukša vērtība laukiem CostCenter un Nodaļa.  
9. Noklikšķiniet uz **Atjaunināt**.
    * Jums ir iespēja apskatīt izmaiņas pirms pārsūtīšanas pabeigšanas.  
    * Pirms pamatlīdzekļa grāmatu pārsūtīšanas pārskatiet rezultātus.  
10. Noklikšķiniet uz **Pārsūtīt**.

