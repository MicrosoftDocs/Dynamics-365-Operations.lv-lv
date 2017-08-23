--- 
title: "Krājumu izsekošanas informācijas labošana"
description: "Šajā procedūrā parādīts, kā izveidot un grāmatot krājumu pārsūtīšanas žurnālu, lai labotu krājumu izsekošanas informāciju."
author: MarkusFogelberg
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: caf8c67d315666edfffe86e459bc7a4478697f07
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="correct-inventory-tracking-information"></a>Krājumu izsekošanas informācijas labošana

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā izveidot un grāmatot krājumu pārsūtīšanas žurnālu, lai labotu krājumu izsekošanas informāciju. Šajā piemērā tiks atjaunināta informācija par krājumu, kas ir atkarīgs no partijas, mainot nepareizi reģistrēto partiju uz citu partiju. Šo procedūru var izmēģināt, izmantojot demonstrācijas datu uzņēmumu USPI vai izmantojot savus datus. Ja izmantojat savus datus, jums ir jābūt krājumam, kuram ir iespējota partija, un tas nedrīkst būt atkarīgs no novietojuma. Ir jābūt izveidotam arī krājumu žurnāla nosaukumam krājumu pārsūtīšanām. Šos uzdevumus parasti veic noliktavas darbinieks.


## <a name="create-an-inventory-transfer-journal"></a>Krājumu pārsūtīšanas žurnāla izveide
1. Dodieties uz sadaļu Pārsūtīšana.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.
4. Noklikšķiniet uz OK.

## <a name="create-journal-lines"></a>Žurnāla rindu izveide
1. Noklikšķiniet uz Jauns.
2. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
    * Ja izmantojat USPI, atlasiet krājumu "M5003".  
3. Laukā Daudzums ievadiet skaitli.
4. Noklikšķiniet uz cilnes Krājumu dimensijas.
5. Laukā Partijas numurs ievadiet vai atlasiet kādu vērtību.
6. Laukā Vieta ievadiet vai atlasiet kādu vērtību.
7. Laukā Noliktava ievadiet vai atlasiet kādu vērtību.
8. Laukā Partijas numurs ievadiet vai atlasiet kādu vērtību.

## <a name="post-the-journal"></a>Grāmatot žurnālu
1. Noklikšķiniet uz Grāmatot.
2. Noklikšķiniet uz OK.

## <a name="check-tracing-information"></a>Izsekošanas informācijas pārbaude
1. Noklikšķiniet uz Krājumi.
2. Noklikšķiniet uz Izsekot.
3. Noklikšķiniet uz OK.
    * Izmantojot šo izsekošanas informāciju var izsekot, no kuras partijas tika veikts krājuma labojums.  Lai skatītu šo informāciju, var izmantot arī lapu Krājumu izsekošana.  
4. Aizvērt lapu.

## <a name="check-inventory-transactions"></a>Krājumu darbību pārbaude
1. Noklikšķiniet uz Krājumi.
2. Noklikšķiniet uz Transakcijas.
    * Šeit varat redzēt darbības, kas tika izveidotas, grāmatojot žurnālu.   


