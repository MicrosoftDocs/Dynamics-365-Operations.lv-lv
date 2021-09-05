---
title: Pamatlīdzekļu saistīšana ar nomu
description: Tēmā ir paskaidrots, kā esošu pamatlīdzekli saistīt ar jaunu nomu.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: bd55d433b0961b8b210b9c28d7340ff880635a85
ms.sourcegitcommit: 3af457fc216bd0020843291ca57fd379acb53c96
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/17/2021
ms.locfileid: "7392478"
---
# <a name="associate-fixed-assets-with-leases"></a>Pamatlīdzekļu saistīšana ar nomu

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

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

Kad noma ir saistīta ar pamatlīdzekli, lauks **Lietošanas ilgums** pamatlīdzekļu grāmatā tiks atjaunināts, lai saskaņotu ar mazāko vērtību no šādiem kritērijiem: 

 - Līdzekļa lietderīgās lietošanas laiks
 - Nomas termiņš no saistītās nomas grāmatas

Ja nomas grāmatas **Īpašumtiesību pārsūtīšanas lauks** ir iestatīts uz **Jā**, vērtība laukā **Lietošanas ilgums** vienmēr būs pamatlīdzekļa lietošanas ilgums. 
 
Lietošanas ilgums tiks atjaunināts katru reizi, kad tiek koriģēta noma, lai nodrošinātu, ka līdzekļa lietošanas tiesības tiek noņemtas pēc nomas perioda tāpat kā tās tiek noņemtas līdzekļu nomā.

> [!NOTE]
> Ja saistāt pamatlīdzekli ar nomu, Līdzekļa nomā pogas **Līdzekļa nolietojums** un **Nomas vērtības samazinājums** ir atspējotas. Varat skatīt līdzekļa nolietojumu un nomas vērtības samazinājuma darījumus no Pamatlīdzekļiem. Poga **Līdzekļu darījumi**, kas atver pieprasījuma formu, arī ir atspējota. Arī pieprasījumu **Līdzekļa darījumi** varat atvērt Pamatlīdzekļos.  

Lapas **Pamatlīdzekļi** un **Pamatlīdzekļu grāmata** attelos nomas ID, kas ir saistīts ar pamatlīdzekli. Ja pamatlīdzeklis ir saistīts ar nomu, nomas ID un nomas apraksts tiks parādīts kopsavilkuma cilnē **Informācija par nomu** lapā **Pamatlīdzekļi**. amatlīdzekļu grāmatām, kas ir saistītas ar nomas grāmatām, lauki **Nomas ID**, **Nomas apraksts** un **Grāmatas veids** parādīs informāciju par atlasīto pamatlīdzekļu grāmatu kopsavilkuma cilnē **Nomas informācija**, lai norādītu, ka tā ir saistīta ar nomas grāmatu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
