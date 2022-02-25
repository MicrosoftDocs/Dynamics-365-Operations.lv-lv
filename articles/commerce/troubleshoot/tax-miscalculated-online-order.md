---
title: Tiešsaistes pasūtījumu nodokļi nav pareizi aprēķināti
description: Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, ja tiešsaistes pasūtījumu nodokļi tiek nepareizi aprēķināti vai ja nodokļu grupa nav pareizi iestatīta pārdošanas rindā.
author: Reza-Assadi
ms.date: 02/16/2022
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 0e4361b436cc78eccaff29dfa2927d342e26072d
ms.sourcegitcommit: 4d52c67f52ad0add63cd905df61367b344389069
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/16/2022
ms.locfileid: "8312035"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a>Tiešsaistes pasūtījumu nodokļi nav pareizi aprēķināti

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, ja tiešsaistes pasūtījumu nodokļi tiek nepareizi aprēķināti vai ja nodokļu grupa nav pareizi iestatīta pārdošanas rindā.

## <a name="description"></a>Apraksts

Kad tiek veikts e-komercijas pasūtījums, nodokļi ir nepareizi aprēķināti vai nodokļu grupa ir nepareizi iestatīta pārdošanas rindā.

## <a name="resolution"></a>Novēršana

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a>Vispārīgo pārdošanas nodokļa grupu konfigurēšana programmā Commerce Headquarters

Lai konfigurētu vispārīgas pārdošanas nodokļa grupas Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Dodieties uz **Nodokļi \> Netiešie nodokļi \> Pārdošanas nodoklis \> Pārdošanas nodokļa grupa**.
1. Kreisās puses navigācijas rūtī atlasiet konfigurējamo NODOKĻU grupu.
1. Kopsavilkuma cilnē **Mazumtirdzniecības mērķis, balstoties uz nodokli**, konfigurējiet pārdošanas nodokļa grupas nodokļus.

> [!NOTE]
> Piegādei, kas neietver PVN, kas ir noteikts pēc debitora adreses, rindas piegādes adrese un mērķa nodokļi, kas ir konfigurēti nodokļu grupai, nosaka nodokļu grupu. Lai iegūtu papildu informāciju, skatiet sadaļu [Nodokļu iestatīšana tiešsaistes veikaliem, kas balstīti uz mērķi](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a>Pārdošanas nodokļa konfigurēšana mazumtirdzniecības veikalam programmā Commerce Headquarters

Lai konfigurētu pārdošanas nodokli mazumtirdzniecības veikalam programmā Commerce Headquarters, izpildiet tālāk minētās darbības.

1. Dodieties uz **Mazumtirdzniecība un komercija \> Kanāli \> Visi mazumtirdzniecības veikali**.
1. Atlasiet veikalu, kuram konfigurēt pārdošanas nodokli.
1. Kopsavilkuma cilnes **Vispārīgi** sadaļā **Pārdošanas nodoklis** konfigurējiet veikala pārdošanas nodokļa informāciju.

> [!NOTE]
> Preču savākšanai no veikala pārdošanas nodokļa grupa tiek ņemta no veikala, kas ir atlasīts savākšanai. Papildinformāciju skatiet sadaļā [Citu veikaliem pieejamo nodokļu opciju iestatīšana](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a>Pārdošanas nodokļa konfigurēšana debitora adresei programmā Commerce Headquarters

Lai konfigurētu pārdošanas nodokli debitora adresei programmā Commerce Headquarters, izpildiet tālāk minētās darbības.

1. Dodieties uz **Debitoru parādi \> Debitori \> Visi debitori**.
1. Izvēlieties debitoru, kuram konfigurēt pārdošanas nodokli.
1. Kopsavilkuma cilnē **Adreses** atlasiet adresi, kurai konfigurēt pārdošanas nodokli, atlasiet  **Papildu opcijas** un pēc tam atlasiet **Papildus**.
1. Kopsavilkuma cilnē **Vispārīgi** atlasiet **Nodokļu grupa**.
1. Laukā **Pārdošanas nodoklis** atlasiet atbilstošo vērtību.

> [!NOTE]
> Nosūtīšanai, kas ietver pārdošanas nodokli debitora adresē, rindas piegādes adrese nosaka rindas nodokļu grupu. Ja debitors veic piegādi uz esošu adresi, kam jau ir konfigurēta nodokļu grupa, tiks izmantota esošā nodokļu grupa. Pēc noklusējuma adresēm, kad tās tiek izveidotas, nav nodokļu grupas.

## <a name="additional-resources"></a>Papildu resursi

[PVN tiešsaistes pasūtījumiem konfigurēšana](../sales-tax-config.md)
