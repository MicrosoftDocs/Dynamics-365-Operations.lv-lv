---
title: Starpuzņēmumu pārdošanas pasūtījuma mainīšana vai dzēšana
description: Šajā tēmā skaidrots oriģinālā pārdošanas pasūtījuma funkcionalitātes mainīšana un dzēšana
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 7bd6bdbf65499e9f18bf6bb5e160a5634bc37fba
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548398"
---
# <a name="change-or-delete-an-original-intercompany-sales-order"></a>Starpuzņēmumu pārdošanas pasūtījuma mainīšana vai dzēšana

[!include [banner](../../includes/banner.md)]

Var izdarīt izmaiņas pārdošanas pasūtījumā, un šīs izmaiņas tiek automātiski sinhronizētas uz atbilstīgu starpuzņēmumu pirkšanas pasūtījumu un starpuzņēmumu pārdošanas pasūtījumu.

> [!NOTE]
> Nekādas jūsu veiktās izmaiņas neietekmē pirkšanas pasūtījumus ārējiem kreditoriem, ne arī oriģinālās pārdošanas rindas, kas saistītas pie pirkšanas pasūtījuma rindām ārējiem kreditoriem.

Tabulā ir apkopotas izmaiņas, ko varat veikt, un paredzamie rezultāti.

| Operācija | Rezultāts |
|---|---|
| Dzēst&nbsp;&nbsp;oriģinālo&nbsp;pārdošanas&nbsp;pasūtījumu. | Tiek dzēsts arī starpuzņēmumu pirkšanas pasūtījums un starpuzņēmumu pārdošanas pasūtījums. Ja pasūtījums ir ar statusu **Izdošanas sarakstā** vai tālākā procesā, pārdošanas pasūtījumu nav iespējams dzēst. |
| Dzēst oriģinālo pārdošanas pasūtījuma rindu. | Tiek dzēsta starpuzņēmumu pirkšanas pasūtījuma rinda un starpuzņēmumu pārdošanas pasūtījuma rinda. Ja pasūtījums ir ar statusu **Izdošanas sarakstā** vai tālākā procesā, pārdošanas pasūtījumu nav iespējams dzēst. |
| Pievienojiet jaunu pārdošanas rindu oriģinālajam pārdošanas pasūtījumam. | Jauna pārdošanas rinda tiek izveidota gan starpuzņēmumu pirkšanas pasūtījumā, gan starpuzņēmumu pārdošanas pasūtījumā. |
| Mainiet daudzumu oriģinālajā pārdošanas pasūtījuma rindā. | Daudzums tiek sinhronizēts starpuzņēmumu pirkšanas pasūtījuma rindā un starpuzņēmumu pārdošanas pasūtījuma rindā. Neto daudzums tiek pārrēķināts visos pasūtījumos. |
| Deaktivizējiet tiešo piegādi oriģinālajā pārdošanas pasūtījumā. | Oriģinālā pārdošanas pasūtījuma lauku **Tiešā piegāde** nevar mainīt, ja starpuzņēmumu pārdošanas pasūtījuma rinda ir sasniegusi **Izdošanas saraksta**, **Izdošanas pasūtījuma** vai **Izdošanas saraksta žurnāla** minimālo statusu. Piegādes adrese starpuzņēmumu pirkšanas pasūtījumā tiek mainīta uz standarta piegādes adresi (standarta pirkšanas pasūtījuma piegādes adrese). Arī starpuzņēmuma pirkšanas pasūtījuma rindas tiek mainītas uz rindu standarta piegādes adresi. Abas tiek sinhronizētas starpuzņēmumu pārdošanas pasūtījumā un rindās. Piegādes tips visās rindās oriģinālajā pārdošanas pasūtījumā tiek mainīts uz **Nav**, un lauks tiek sinhronizēts ar starpuzņēmumu pirkšanas pasūtījuma rindām. Pirkšanas pasūtījumi ārējiem kreditoriem nav ietekmēti, un oriģinālās pārdošanas rindas nav pievienotas ārējo kreditoru pirkšanas pasūtījuma rindām. Starpuzņēmumu pirkšanas pasūtījumu un rindu piegādes datums un pieprasīto starpuzņēmumu pārdošanas pasūtījumu un rindu saņemšanas/nosūtīšanas datumi tiek atjaunināti. |
| Aktivizējiet tiešo piegādi oriģinālajā pārdošanas pasūtījumā. | Oriģinālā pārdošanas pasūtījuma lauku **Tiešā piegāde** nevar mainīt, ja starpuzņēmumu pārdošanas pasūtījuma rinda ir sasniegusi **Izdošanas saraksta**, **Izdošanas pasūtījuma** vai **Izdošanas saraksta žurnāla** minimālo statusu. Piegādes adrese starpuzņēmumu pirkšanas pasūtījumā tiek mainīta uz piegādes adresi no oriģinālā pārdošanas pasūtījuma un sinhronizēta ar starpuzņēmumu pārdošanas pasūtījumu. Piegādes tips visās rindās oriģinālajā pārdošanas pasūtījumā tiek mainīts uz **Tiešā piegāde**, un lauks tiek sinhronizēts ar starpuzņēmumu pirkšanas pasūtījuma rindām. Piegādes adrese katrā oriģinālā pārdošanas pasūtījuma rindā tiek sinhronizēta starpuzņēmumu pirkšanas pasūtījuma rindās un starpuzņēmumu pārdošanas pasūtījuma rindās. Starpuzņēmumu pirkšanas pasūtījumu un rindu piegādes datums un pieprasīto starpuzņēmumu pārdošanas pasūtījumu un rindu saņemšanas/nosūtīšanas datumi tiek atjaunināti. |
| Pievienojiet piezīmi oriģinālā pārdošanas pasūtījuma virsrakstam un rindām. | Piezīme tiek kopēta uz starpuzņēmumu pirkšanas pasūtījumu un starpuzņēmumu pārdošanas pasūtījumu. |
| Mainiet vai dzēsiet piezīmi. | Mainot vai dzēšot piezīmi, atbilstoši tiek mainīta vai dzēsta attiecīgā piezīme starpuzņēmumu pirkšanas pasūtījumā un starpuzņēmumu pārdošanas pasūtījumā. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
