---
title: Pamatlīdzekļa pārsūtīšana
description: Šajā uzdevuma ceļvedī ir parādīts, kā pamatlīdzekļa grāmatai pārsūtīt finanšu informāciju no vienas finanšu dimensiju kopas uz jaunu finanšu dimensiju kopu.
author: saraschi2
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c307568ab1cc064c27fa8d3e24756f564947e4716aaed1c280019c1283da1c93
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765696"
---
# <a name="transfer-a-fixed-asset"></a>Pamatlīdzekļa pārsūtīšana

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]