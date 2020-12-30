---
title: Krājumu pieejamība duālajā ierakstā
description: Šajā tēmā ir sniegta informācija par to, kā pārbaudīt krājumu pieejamību duālajā ierakstā.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 4d1022eec633bf0a9edb4d5b26982853cec836d7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4455019"
---
# <a name="inventory-availability-in-dual-write"></a>Krājumu pieejamība duālajā ierakstā

[!include [banner](../../includes/banner.md)]

Izmantojot krājumu pieejamību, varat pārbaudīt krājumus pirms preču pievienošanas lapā **Piedāvājumi**, **Pasūtījumi** vai **Rēķini** programmā Microsoft Dynamics 365 Sales. Piemēram, krājumu pārbaude un izpildes datuma noteikšana ir galvenais uzdevums procesā [no potenciālā klienta līdz skaidrai naudai](dual-write-prospect-to-cash.md).

Ja nav pietiekami daudz krājumu, varat aplēst piegādes datumu, pamatojoties uz prognozēto krājumu saņemšanas un izsniegšanas plūsmām. Varat arī pārbaudīt preces pieejams solīšanai (ATP) informāciju, kur varat atrast ATP daudzumu iepriekš definētā laika periodā.

## <a name="on-hand-inventory"></a>Rīcībā esošie krājumi

Dynamics 365 Sales **Piedāvājumi**, **Pasūtījumi** vai **Rēķini** lapu galvenē ir pievienota jauna poga **Rīcībā esošie krājumi**. Atlasot šo pogu, parādās dialoglodziņš, kur varat norādīt uzņēmumu un preci, kurai vēlaties pārbaudīt rīcībā esošos krājumus. Šis dialoglodziņš parāda to pašu informāciju, ko [rīcībā esošie krājumi](../../../../supply-chain/inventory/tasks/check-availability-stock.md).

Dialoglodziņā tiek atgriezta informācija par krājumiem no Dynamics 365 Supply Chain Management. Šajā informācijā ir iekļauti tālāk norādītie daudzumi:

- Rīcībā esošais daudzums
- Rezervētais rīcībā esošais daudzums
- Pieejamais rīcībā esošais daudzums
- Pasūtītais daudzums
- Pasūtījumā iekļautais daudzums
- Rezervētais pasūtītais daudzums
- Kopējais pieejamais daudzums

## <a name="atp-information"></a>ATP informācija

Programmā Sales ir pievienota jauna **ATP informācija**, kas ir pievienota rindas precēm **Piedāvājumu**, **Pasūtījumu** un **Rēķinu** lapās. Atlasot šo pogu, parādās dialoglodziņš, kur varat norādīt uzņēmumu, preci, krājuma atrašanās vietu, krājuma noliktavu un krājumu daudzumu. Šim dialoglodziņam ir tie paši iestatījumi, kas aprakstīti [Pasūtījumu solīšanā](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).

Dialoglodziņā tiek atgriezta ATP informācija no Supply Chain Management. Šajā informācijā ir iekļauti tālāk norādītie daudzumi:

- ATP daudzums
- Ieejas plūsmas daudzums
- Izejas plūsmas daudzums
- Rīcībā esošais daudzums
