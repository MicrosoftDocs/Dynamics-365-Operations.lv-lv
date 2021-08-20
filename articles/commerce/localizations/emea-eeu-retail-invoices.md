---
title: Debitoru rēķini un atgriešanas pārdošanas pasūtījumi Austrumeiropas valstīs
description: Šajā tēmā ir aprakstīts, kā iestatīt informāciju debitoru rēķiniem un pārdoto krājumu atgriešanas pasūtījumiem Austrumeiropas valstīs.
author: epopov
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 38d1708f6b113c4915b208941e1ebab70b07323f7523d742c54f3acb32b40569
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750689"
---
# <a name="customer-invoices-and-return-sales-orders-in-eastern-european-countries"></a>Debitoru rēķini un atgriešanas pārdošanas pasūtījumi Austrumeiropas valstīs


[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā iestatīt informāciju debitoru rēķiniem un pārdoto krājumu atgriešanas pasūtījumiem Austrumeiropas valstīs.

Par debitoru rēķiniem un pārdoto krājumu atgriešanas pasūtījumiem, kas tiek ģenerēti programmā Retail point of sale (POS), varat iestatīt tālāk aprakstīto informāciju.

- Varat izmantot PVN grupas, lai apstrādātu atgrieztos krājumus, izmantojot pārdoto krājumu atgriešanas pasūtījumus. Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Parametri \> Komercijas parametri**. Atveriet cilni **Grāmatošana \> Rēķins** un iestatiet vienumu **Izmantot PVN grupu atgrieztajiem krājumiem** uz **Jā**.

    * Lai norādītu PVN grupu debitoru atgrieztajiem krājumiem, lapas **Debitori** kopsavilkuma cilnē **Komercija**, laukā **PVN grupa atgrieztajiem krājumiem** atlasiet kādu PVN grupu. Kad kādam debitoram grāmatojat pārdoto krājumu atgriešanas pasūtījumu, pārdoto krājumu atgriešanas pasūtījuma rinda tiek atjaunināta ar formā **Debitori** krājumu atgriešanai norādīto PVN grupu.
    * Lai norādītu PVN grupu atgrieztajiem krājumiem, ko debitors veic pārdošanas punktā Retail POS, lapā **Veikali**, kopsavilkuma cilnē **Vispārīgi**, laukā **PVN grupa atgrieztajiem krājumiem** atlasiet kādu PVN grupu. Kad grāmatojat pārdoto krājumu atgriešanas pasūtījumu kādam veikala debitoram, pārdoto krājumu atgriešanas pasūtījuma rinda tiek atjaunināta ar lapā **Veikali** norādīto PVN grupu atgrieztajiem krājumiem.

- Ja rēķinam vai krājumu atgriešanai nav noklusējuma pārdošanas datuma, kā rēķina vai atgriešanas pārdošanas datumu varat izmantot debitora rēķina grāmatošanas datumu vai pārdoto krājumu atgriešanas pasūtījuma datumu. Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Parametri \> Komercijas parametri**. Atveriet cilni **Grāmatošana \> Rēķins** un iestatiet vienumu **Izmantot grāmatošanas datumu kā pārdošanas datumu** uz **Jā**.
- Lai numurētu Latvijas un Lietuvas debitoru rēķinus un pārdoto krājumu atgriešanas pasūtījumus, varat izmantot numuru diapazonu, ko nodrošina nodokļu iestādes.

    * Dodieties uz **Organizācijas administrēšana \> Numuru sērijas \> Skaitītāju pārvaldība**. Tur vajadzētu būt ierakstam, kur **Modulis** = **Pārdošana** un **Tips** = **Rēķins**.
    * Dodieties uz **Organizācijas administrēšana \> Numuru sērijas \> Rēķinu numerācijas iestatījumi**. Atlasiet izvēles rūtiņu **Komercija** tai numuru sērijas rindai, kas tiek izmantota, lai numurētu debitoru rēķinus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]