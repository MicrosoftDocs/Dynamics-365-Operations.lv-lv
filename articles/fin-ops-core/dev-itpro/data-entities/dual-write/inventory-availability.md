---
title: Krājumu pieejamība duālajā ierakstā
description: Šajā tēmā ir sniegta informācija par krājumu pieejamības pārbaudi duālajā ierakstā.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426986"
---
# <a name="inventory-availability"></a>Krājumu pieejamība

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Izmantojot krājumu pieejamību, varat pārbaudīt krājumus pirms preču pievienošanas veidlapās **Piedāvājumi**, **Pasūtījumi** vai **Rēķini** no modeļa atkarīgās programmās Dynamics 365. Piemēram, krājumu pārbaude un izpildes datuma noteikšana ir galvenais uzdevums procesā [no potenciālā klienta līdz skaidrai naudai](dual-write-prospect-to-cash.md). Ja nav pietiekami daudz krājumu, varat aplēst piegādes datumu, pamatojoties uz prognozēto krājumu saņemšanas un izsniegšanas plūsmām. Varat arī pārbaudīt preces pieejams solīšanai (ATP) informāciju, kur varat atrast ATP daudzumu iepriekš definētā laika periodā.

## <a name="on-hand-inventory"></a>Rīcībā esošie krājumi 

Dynamics 365 Sales veidlapu **Piedāvājumi**, **Pasūtījumi** vai **Rēķini** galvenē ir pievienota jauna poga **Rīcībā esošie krājumi**. Noklikšķinot uz pogas, parādās dialoglodziņš, un varat norādīt uzņēmumu un preci, kurai vēlaties pārbaudīt rīcībā esošos krājumus. Tiek atgriezta informācija par krājumu no Dynamics 365 Supply Chain Management un parādīta tā pati informācija, kas sadaļā [Rīcībā esošie krājumi](../../../../supply-chain/inventory/tasks/check-availability-stock.md). Informācija ietver tālāk minētos daudzumus.

- **Rīcībā esošais daudzums**
- **Rezervētais rīcībā esošais daudzums**
- **Pieejamais rīcībā esošais daudzums**
- **Pasūtītais daudzums**
- **Pasūtījumā iekļautais daudzums**
- **Rezervētais pasūtītais daudzums**
- **Kopējais pieejamais daudzums**

## <a name="atp-information"></a>ATP informācija

Dynamics 365 Sales veidlapu **Piedāvājumi**, **Pasūtījumi** vai **Rēķini** rindas krājumos ir pievienota jauna poga **ATP informācija**. Noklikšķinot uz pogas, parādās dialoglodziņš, un varat norādīt uzņēmumu, preci, krājuma atrašanās vietu, krājuma noliktavu un krājumu daudzumu. Tiek atgriezta **ATP informācija** no Supply Chain Management un tiek parādīti iestatījumi, kas aprakstīti [Pasūtījumu solīšana](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations). Informācijā ir ietverts **ATP daudzums**, **Ieejas plūsmas daudzums**, **Izejas plūsmas daudzums** un **Rīcībā esošais daudzums**.
