---
title: "Pamatlīdzekļu transakciju opcijas"
description: "Šajā rakstā ir aprakstītas dažādās metodes, kas ir pieejamas pamatlīdzekļu transakciju izveidošanai."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 18352ad921c2e2d110a7535f979272685105662f
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="fixed-asset-transaction-options"></a>Pamatlīdzekļu transakciju opcijas

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstītas dažādās metodes, kas ir pieejamas pamatlīdzekļu transakciju izveidošanai.

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



Plašāku informāciju skatiet rakstā [Pamatlīdzekļu integrācija](fixed-asset-integration.md).




