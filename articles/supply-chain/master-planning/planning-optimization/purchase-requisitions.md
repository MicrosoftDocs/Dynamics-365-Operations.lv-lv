---
title: Pirkšanas pieprasījumi
description: Šajā rakstā ir aprakstīti pirkšanas pieprasījumi.
author: t-benebo
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: d9d55186307b18f4c3be78ae0828b08d3c987aad
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740689"
---
# <a name="purchase-requisitions"></a>Pirkšanas pieprasījumi

[!include [banner](../../includes/banner.md)]

Vispārējā plānošana var papildināt apstiprinātos pirkšanas pieprasījumus. Tādēļ, lai segtu pirkšanas pieprasījumus, lietotājiem nav jāizmanto darbplūsma pirkšanas pasūtījumu izveidei. Tā vietā pirkšanas pieprasījumus var segt vispārējā plānošana. Šīs funkcionalitātes dēļ pirkšanas pieprasījums var izveidot pirkšanas pasūtījumu, pārsūtīšanas pasūtījumu vai ražošanas pasūtījumu atkarībā no **Plānotā pasūtījuma tipa** vērtības, kas iestatīta saistītajam produktam.

## <a name="enable-master-plans-to-include-requisitions"></a>Iestatīt vispārējos plānus, lai iekļautu pieprasījumus

Lai vispārējā plāna seguma aprēķina laikā iekļautu pieprasījumus, sekojiet šiem soļiem.

1. Dodieties uz **Vispārējā plānošana** \> **Iestatījumi** \> **Plāni** \> **Vispārējie plāni**.
1. Izveidojiet vai atlasiet vispārējo plānu.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Izmantot noklusējuma datus** uz *Jā*.
1. Atkārtojiet 2. un 3. soli katram papildu vispārējam plānam, kurā vēlaties iekļaut pieprasījumus.

## <a name="approved-requisitions-time-fence"></a>Apstiprināto pieprasījumu periods

*Apstiprināto pieprasījumu laika periods* izveido, cik tālu (dienās) vispārējais plāns ietvers pieprasījumu no apstiprinātiem papildināšanas pieprasījumiem. Varat iestatīt apstiprināto pieprasījumu laika periodu gan vajadzību grupas līmenī, gan vispārējā plāna līmenī.

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a>Vajadzības perioda iestatīšana vajadzību grupai

1. Dodieties uz **Vispārējā plānošana** \> **Iestatījumi** \> **Vajadzība** \> **Vajadzību grupas**.
1. Izveidojiet vai atlasiet vajadzību grupu.
1. Kopsavilkuma cilnē **Citi** iestatiet lauku **Apstiprināts pieprasījumu periods (dienas)** uz dienu skaitu, ko iekļaut laika periodā.
1. Atkārtojiet 2. un 3. soli katrai papildu vajadzību grupai, kur vēlaties iestatīt apstiprināto pieprasījumu periodu.

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a>Apstiprināto pieprasījumu laika perioda iestatīšana atsevišķiem vispārējiem plāniem

Kad iestatāt apstiprinātu pieprasījumu periodu atsevišķam vispārējai plānam, iestatījums ignorē laika perioda iestatījumu jebkurai piemērojamai vajadzību grupai.

1. Dodieties uz **Vispārējā plānošana** \> **Iestatījumi** \> **Plāni** \> **Vispārējie plāni**.
1. Izveidojiet vai atlasiet vispārējo plānu.
1. Kopsavilkuma cilnē **Citi** iestatiet lauku **Apstiprināto pieprasījumu periods (dienas)** uz dienu skaitu, ko iekļaut laika periodā.
1. Atkārtojiet 2. un 3. soli katrai papildu vajadzību grupai, kur vēlaties iestatīt apstiprināto pieprasījumu periodu.

> [!IMPORTANT]
> Plānošanas optimizēšanai nav atbalstīti apstiprināti pieprasījumu laika periodi. Kamēr tās netiek atbalstītas, visas laukā **Apstiprināto pieprasījumu periods (dienas)** ievadītās vērtības tiks ignorētas.

## <a name="independent-supply-regardless-of-coverage-code"></a>Neatkarīga piegāde, neņemot vērā vajadzības kodu

Pirkšanas pieprasījumus vienmēr sedz neatkarīgi plānotie pasūtījumi, neatkarīgi no vajadzību koda. Šī darbība nodrošina skaidru izsekošanu un darbplūsmas starp pirkšanas pieprasījumiem un papildināšanas pasūtījumiem.

### <a name="example-1"></a>1. piemērs

Prece ir iestatīta tā, lai tai būtu **Vajadzību koda** vērtība *Min./maks.* Tai ir šādi krājumu un pieprasījumu statusi:

- Rīcībā esošo krājumu saraksts = 10.
- Minimālais krājumu daudzums = 15.
- Maksimālais krājumu daudzums = 20.
- Eksistē pirkšanas pieprasījums vienam gabalam. Tā pieprasītais datums ir šodien.

Kad tiek palaista vispārējā plānošana, tiek izveidoti divi plānotie pasūtījumi: viens 10 gabaliem, lai papildinātu krājumus līdz maksimālajam daudzumam, un viens vienam gabalam, lai papildinātu pirkšanas pieprasījumu.

### <a name="example-2"></a>2. piemērs

Prece ir iestatīta tā, lai tai būtu **Vajadzību koda** vērtība *Min./maks.* Tai ir šādi krājumu un pieprasījumu statusi:

- Rīcībā esošo krājumu saraksts = 17.
- Minimālais krājumu daudzums = 15.
- Maksimālais krājumu daudzums = 20.
- Eksistē pirkšanas pieprasījums vienam gabalam. Tā pieprasītais datums ir šodien.

Kad tiek palaista vispārējā plānošana, pirkšanas pieprasījuma papildināšanai tiek izveidots viens plānotais pasūtījums vienam gabalam.

### <a name="example-3"></a>3. piemērs

Prece ir iestatīta tā, lai tās *Periods* ir **Vajadzību koda** vērtība un septiņu dienu perioda ilgums. Tai ir šādi krājumi, pārdošanas pasūtījumi un pieprasījumu statusi:

- Rīcībā esošo krājumu saraksts = 0.
- Pastāv pārdošanas pasūtījums pieciem gabaliem. Tam paredzamais nosūtīšanas datums ir šodiena, plus viena diena.
- Eksistē pirkšanas pieprasījums trim gabaliem. Tā pieprasītais datums ir šodiena un vēl trīs dienas.

Kad tiek palaista vispārējā plānošana, tiek izveidoti divi plānotie pasūtījumi: viens trim gabaliem, lai papildinātu krājumus līdz maksimālajam daudzumam, un viens pieciem gabalam, lai papildinātu pirkšanas pieprasījumu.

> [!NOTE]
> Kad plānotais pasūtījums, kas ir piesaistīts pirkšanas pieprasījumam, ir apstiprināts, plānošanas programma uztur piesaisti pirkšanas pieprasījumam. Ja pēc tam apstiprinātajam pasūtījumam trūkst daudzuma, kas ir nepieciešams pirkšanas pieprasījuma izpildei, sistēma izveidos jaunu plānoto pasūtījumu starpībai.

Vispārīgāku informāciju par pirkšanas pasūtījumiem skatiet rakstā [Pirkšanas pasūtījuma pārskats](../../procurement/purchase-requisitions-overview.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]