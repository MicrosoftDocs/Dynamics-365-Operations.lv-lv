---
title: Pamatlīdzekļu saistīšana ar nomu
description: Tēmā ir paskaidrots, kā esošu pamatlīdzekli saistīt ar jaunu nomu.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 5c4f14d38b3cfc2c4d09cfeb5854204701250757
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260857"
---
# <a name="associate-fixed-assets-with-leases"></a>Pamatlīdzekļu saistīšana ar nomu

[!include [banner](../includes/banner.md)]

Tēmā ir paskaidrots, kā esošu pamatlīdzekli saistīt ar jaunu nomu. Saistot pamatlīdzekli ar nomu, līdzekļa lietošanas tiesību (LLT) vērtība sākotnējā atzīšanā būs pamatlīdzekļa iegādes izmaksas.

Pirms varat pamatlīdzekli saistīt ar nomu, pamatlīdzeklim ir jāizveido ieraksts pie Pamatlīdzekļi. Pēc tam lapā **Nomas kopsavilkums** ir jāizveido noma un pamatlīdzeklis jāsaista ar šo nomu.

1. Nomas pievienošana, izpildot darbības [Nomas pievienošana vai kopēšana](add-lease.md). Lapas **Pievienot nomu** laukā **Pamatlīdzekļa numurs** atlasiet līdzekli, kas vēl nav iegūts.
2. Atlasiet **Grāmatas** un apstipriniet maksājuma grafiku.
3. Atlasiet **Sākotnējā atzīšana**.
4. Atlasiet **Līdzekļu nomas žurnāls**.

    Nomas sākotnējās atzīšanas žurnāla ieraksts ieraksta debetā pamatlīdzekli par summu, kas parasti tiek ierakstīts debetā LLT kontā.

    Tagad varat skatīt pamatlīdzekļa darījuma veidu un grāmatu.

5. Atlasiet **Žurnāla detalizēta informācija**.
6. Atlasiet **Rindas**, lai skatītu atsevišķas žurnāla ieraksta rindas.
7. Atlasiet žurnāla rindu, kas satur līdzekli, un pēc tam atlasiet cilni **Pamatlīdzekļi**.

    Cilnē **Pamatlīdzekļi** tiek parādīts darījuma veids un grāmata. Pēc noklusējuma lauks **Darījuma veids** ir iestatīts uz **Iegāde**, un lauks **Grāmata** ir iestatīts uz pašreizējo pamatlīdzekļu grāmatu.

Pēc sākotnējās atzīšanas žurnāla ieraksta grāmatošanas darījums tiek parādīts kā pamatlīdzekļa iegādes darījums. Lai skatītu darījuma tabulu, dodieties uz **Pamatlīdzekļi \> Pamatlīdzekļi \> Pamatlīdzekļi**, atlasiet atbilstošo līdzekli un pēc tam atlasiet **Novērtējumi**. Jums vajadzētu redzēt, ka sākotnējās atzīšanas žurnāla ieraksts ir izveidojis attiecīgā pamatlīdzekļa iegūšanas darījumu.

Tagad pamatlīdzeklim var aprēķināt nolietojumu, izmantojot standarta nolietojuma funkcionalitāti Pamatlīdzekļos. Papildinformāciju par nolietojum skatiet [Nolietojuma metodes un konvencijas](../fixed-assets/depreciation-methods-conventions.md).

> [!NOTE]
> Ja saistāt pamatlīdzekli ar nomu, Līdzekļa nomā pogas **Līdzekļa nolietojums** un **Nomas vērtības samazinājums** ir atspējotas. Varat skatīt līdzekļa nolietojumu un nomas vērtības samazinājuma darījumus no Pamatlīdzekļiem. Poga **Līdzekļu darījumi**, kas atver pieprasījuma formu, arī ir atspējota. Arī pieprasījumu **Līdzekļa darījumi** varat atvērt Pamatlīdzekļos.  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]