---
title: Pārsūtīšanas dokumentu ģenerēšana iekšējo krājumu pārsūtīšanai
description: Šajā procedūrā ir aprakstīts, kā izveidot preču kustības uzņēmuma robežās pārsūtīšanas dokumentus.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e945dca9f0014489a0c0713ef412b281357a276e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830383"
---
# <a name="generate-a-transfer-document-for-an-internal-inventory-transfer"></a>Pārsūtīšanas dokumentu ģenerēšana iekšējo krājumu pārsūtīšanai

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir aprakstīts, kā izveidot preču kustības uzņēmuma robežās pārsūtīšanas dokumentus. Šī procedūra ir pieejama tikai juridiskām personām, kuru primārā adrese ir Lietuvā. Šī procedūra ir izveidota, izmantojot demonstrācijas datu uzņēmumu DEMF, kura primārā adrese ir Lietuvā. Lai varētu pabeigt šo procedūru, ir jāizpilda procedūra "Iestatīt preču kustības uzņēmuma robežās pārsūtīšanas dokumentus". Šī procedūra ir paredzēta krājumu grāmatvežiem. Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.


## <a name="create-a-transfer-order"></a>Izveidot pārsūtīšanas pasūtījumu
1. Dodieties uz sadaļu Krājumu pārvaldība > Ienākošie pasūtījumi > Pārsūtīšanas pasūtījums.
2. Noklikšķiniet uz Jauns.
3. Laukā No noliktavas ievadiet vai atlasiet kādu vērtību.
4. Laukā Uz noliktavu ievadiet vai atlasiet kādu vērtību.
5. Noklikšķiniet uz Pievienot.
6. Sarakstā atzīmējiet atlasīto rindu.
7. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.

## <a name="enter-transportation-details-for-the-transfer-order"></a>Ievadīt pārsūtīšanas pasūtījuma transportēšanas datus
1. Noklikšķiniet uz Saglabāt.
2. Darbību rūtī noklikšķiniet uz Sūtīt.
3. Noklikšķiniet uz Transportēšanas dati.
4. Laukā Drukāt transportēšanas datus atlasiet Jā.
5. Laukā Preces izsniedza ievadiet vai atlasiet vērtību.
6. Laukā Iepakojums ievadiet vērtību.
7. Ievadiet vērtību laukā Noslodzes riska līmenis.
8. Ievadiet vai atlasiet vērtību laukā Pārvadātājs.
9. Ievadiet vai atlasiet vērtību laukā Modelis.
10. Laukā Reģistrācijas numurs ierakstiet vērtību.
11. Ievadiet vērtību laukā Piekabes reģistrācijas numurs.
12. Ievadiet vai atlasiet vērtību laukā Transportlīdzekļa vadītājs.
13. Laukā Autovadītāja vārds ierakstiet vērtību.
14. Noklikšķiniet uz Saglabāt.
15. Aizvērt lapu.

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a>Skatīt negrāmatotā pārsūtīšanas pasūtījuma pavadzīmi
1. Noklikšķiniet uz Pavadzīme.
2. Noklikšķiniet uz OK.
3. Aizvērt lapu.

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a>Skatīt grāmatotā pārsūtīšanas pasūtījuma pavadzīmi
1. Darbību rūtī noklikšķiniet uz Pārsūtīšanas pasūtījums.
2. Darbību rūtī noklikšķiniet uz Sūtīt.
3. Noklikšķiniet uz Nosūtīt pārsūtīšanas pasūtījumu.
4. Noklikšķiniet uz cilnes Vispārīgi.
5. Atlasiet opciju laukā Atjaunināt.
6. Noklikšķiniet uz cilnes Apskats.
7. Ierakstiet vērtību laukā Pavadzīme.
8. Noklikšķiniet uz OK.
9. Darbību rūtī noklikšķiniet uz Sūtīt.
10. Noklikšķiniet uz Pavadzīme.
11. Noklikšķiniet uz OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]