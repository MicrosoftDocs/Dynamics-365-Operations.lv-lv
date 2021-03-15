---
title: Krājumu izsekošanas informācijas labošana
description: Šajā procedūrā parādīts, kā izveidot un grāmatot krājumu pārsūtīšanas žurnālu, lai labotu krājumu izsekošanas informāciju.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c70dba7d21eab372cec235efa5a4be19587a409
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000138"
---
# <a name="correct-inventory-tracking-information"></a>Krājumu izsekošanas informācijas labošana

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]