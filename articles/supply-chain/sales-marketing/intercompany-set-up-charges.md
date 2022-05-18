---
title: Maksu iestatīšana starpuzņēmumu pasūtījumos
description: Šajā rakstā ir paskaidrots, kā iestatīt maksu starpuzņēmumu pasūtījumiem
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 27633e09bfcf41fbbe5449b0d3b5f283eaf7ee13
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673667"
---
# <a name="set-up-charges-on-intercompany-orders"></a>Maksu iestatīšana starpuzņēmumu pasūtījumos

[!include [banner](../../includes/banner.md)]

Varat iestatīt maksas, ko pievienot starpuzņēmumu pasūtījumiem. Kad starpuzņēmumu pārdošanas pasūtījumam tiek pievienota maksa, tas tiek automātiski sinhronizēts ar starpuzņēmumu pirkšanas pasūtījumu. Tas darbojas abos veidos — no starpuzņēmumu pārdošanas pasūtījuma uz pirkšanas pasūtījumu un otrādi.

Maksas var arī izmantot, lai pievienotu peļņu starpuzņēmumu pārdošanas pasūtījumam, definējot maksu kā starpuzņēmumu procentus.

Iestatot starpuzņēmumu pasūtījumiem lietojamās maksas, tiek iespējots iekšējās peļņas aprēķins starpuzņēmumu pārdošanas pasūtījumam no sākotnējā pārdošanas pasūtījuma neto summas. Iespējams, vēlaties to izmantot, ja jūsu starpuzņēmumu kreditors jums pārdod par izmaksu cenu. Tālāk esošajā procedūrā aprakstīts, kā to izpildīt starpuzņēmumu debitoriem. To pašu procedūru var izmantot kreditoriem.

1. Dodieties uz **Debitori \> Iestatījumi \> Maksas \> Debitora maksu grupas**.
1. Izveidojiet maksu grupu.
1. Dodieties uz **Debitoru parādi \> Debitori \> Visi debitori**. Atlasīt debitora konta saiti. Atlasiet cilni **Debitori** Darbību rūtī, un tad atlasiet kopsavilkuma cilni **Pārdošanas pasūtījums**.
1. Darbību rūtī atlasiet **Rediģēt**, lai iespējotu labojumu veikšanu laukā. Laukā **Maksu grupa** atlasiet 2. darbībā iestatīto starpuzņēmumu maksu grupu.
1. Pārejiet uz sadaļu **Debitori \> Iestatījumi \> Maksas \> Automātiskās izmaksas**.
1. Iestatiet maksas, aizpildot atbilstošos laukus.
1. Laukā **Debitoru relācijas** atlasiet 2. darbībā iestatīto starpuzņēmumu maksu grupu.
1. Kopsavilkuma cilnes **Rindas** laukā **Kategorija** atlasiet **Starpuzņēmumu procenti**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
