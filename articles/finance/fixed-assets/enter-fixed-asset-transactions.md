---
title: Pamatlīdzekļu transakciju opcijas
description: Šajā tēmā ir aprakstītas dažādās pieejamās pamatlīdzekļu transakciju izveides metodes.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: roschlom
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 494087bc7a1247999d3f63dcdc0a0f403dcfdb2d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978693"
---
# <a name="fixed-asset-transaction-options"></a>Pamatlīdzekļu transakciju opcijas

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas dažādās pieejamās pamatlīdzekļu transakciju izveides metodes.

Varat iestatīt pamatlīdzekļus, lai integrētu ar kreditoriem, debitoriem, sagādi un izcelsmi un Virsgrāmatu. Ja vēlaties, varat arī pārsūtīt noliktavas krājumu pārvaldību uz pamatlīdzekļiem iekšējai izmantošanai.

## <a name="accounts-payable"></a>Parādi kreditoriem
Pamatlīdzekļu transakcijas varat ievadīt lapā Žurnāla dokuments. Šo lapu var atvērt tikai no lapas Rēķinu žurnāls. Lapu Žurnāla dokuments varat atvērt arī no lapas Rēķinu apstiprināšanas žurnāls. Laukā Korespondējošā konta tips atlasiet Pamatlīdzekļi. Pēc tam laukā Korespondējošais konts atlasiet pamatlīdzekļa numuru. Cilnē Pamatlīdzekļi ievadiet vērtības laukos Transakcijas tips un Grāmata.

## <a name="accounts-receivable"></a>Debitoru parādi
Pamatlīdzekļu transakcijas varat ievadīt lapā Brīva teksta rēķins.  Lapā Brīva teksta rēķins, režģī Rēķina rindas atlasiet kādu rindas krājumu. Noklikšķiniet uz kopsavilkuma cilnes Detalizēta informācija par rindu. Ievadiet norakstīšanas transakcijas pamatlīdzekļa numuru un grāmatu. Brīvā teksta rēķiniem pamatlīdzekļa transakcijas tips vienmēr ir Norakstīšana - pārdošana.

## <a name="procurement-and-sourcing"></a>Sagāde un avoti
Pamatlīdzekļu transakcijas varat ievadīt lapā Pirkšanas pasūtījums. Ievadiet nepieciešamo informāciju, lai izveidotu pirkšanas pasūtījumu, un pēc tam noklikšķiniet uz Labi. Lapā Pirkšanas pasūtījums noklikšķiniet uz kopsavilkuma cilnes Detalizēta informācija par rindu. Pēc tam cilnē Pamatlīdzekļi ievadiet informāciju par pamatlīdzekli. 

Lai grāmatotu iegādes transakciju esošam pamatlīdzeklim, norādiet šī pamatlīdzekļa numuru, grāmatu un transakcijas tipu. Pamatlīdzekli nevar grāmatot, ja kāda informācija nav norādīta. Lai grāmatotu iegādes transakciju jaunam pamatlīdzeklim, atzīmējiet opciju Vai jauns pamatlīdzeklis? un pēc tam atlasiet pamatlīdzekļu grupu, kurai piešķirt šo jauno pamatlīdzekli. Tomēr nav pieejams neviens no pamatlīdzekļu laukiem, ja krājums ir krājumu modeļu grupā, kas izmanto standarta izmaksu krājumu modeli. Turklāt opcijas, kas ir noteiktas lapā Pamatlīdzekļu parametri, nosaka, vai iegādes transakcijas varat grāmatot no pirkšanas moduļiem. 

Ja pamatlīdzekļu iegādei tiek izmantots pirkšanas pasūtījums vai žurnāls Krājumi pamatlīdzekļiem, tiek ietekmēta krājumu vērtība.

## <a name="general-ledger"></a>Virsgrāmata
Jebkuru pamatlīdzekļa transakcijas tipu var grāmatot lapā Virsgrāmatas žurnāls. Varat arī izmantot žurnālus sadaļā Pamatlīdzekļi, lai grāmatotu pamatlīdzekļu darbības.

## <a name="options-for-entering-fixed-asset-transaction-types"></a>Pamatlīdzekļu darbības tipu ievadīšanas opcijas


| Darījuma veids                    | Modulis                   | Opcijas                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| Iegāde, Iegādes korekcija | Pamatlīdzekļi             | Pamatlīdzekļi, Krājumi pamatlīdzekļiem   |
|                                     | Virsgrāmata           | Virsgrāmatas žurnāls                           |
|                                     | Parādi kreditoriem         | Rēķinu žurnāls, Rēķinu apstiprināšanas žurnāls |
|                                     | Sagāde un avoti | Pirkšanas pasūtījums                            |
| Nolietojums                        | Pamatlīdzekļi             | Pamatlīdzekļi                              |
|                                     | Virsgrāmata           | Virsgrāmatas žurnāls                           |
| Izslēgšana                            | Pamatlīdzekļi             | Pamatlīdzekļi                              |
| ** **                               | Virsgrāmata           | Virsgrāmatas žurnāls                           |
| ** **                               | Debitoru parādi      | Brīva teksta rēķins                         |


Pamatlīdzekļa nolietojuma periodu atlikusī vērtība netiek atjaunināta, ja nolietojuma transakcijas veida žurnāla rinda tiek ievadīta manuāli vai importēta, izmantojot datu elementu. Šī vērtība tiek atjaunināta, kad žurnāla rinda tiek izveidota, izmantojot nolietojuma priekšlikuma procesu.

Plašāku informāciju skatiet rakstā [Pamatlīdzekļu integrācija](fixed-asset-integration.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]