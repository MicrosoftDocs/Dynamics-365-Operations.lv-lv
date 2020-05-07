---
title: Sveiciena ziņojuma pievienošana
description: Šajā tēmā ir aprakstīts, kā pievienot sveiciena ziņojumu savai Microsoft Dynamics 365 Commerce tīmekļa vietnei.
author: psimolin
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d2a125b4e71016ad620f128af2e3c9f29aa04f4c
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269618"
---
# <a name="add-a-welcome-message"></a>Sveiciena ziņojuma pievienošana


[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā pievienot sveiciena ziņojumu savai Microsoft Dynamics 365 Commerce tīmekļa vietnei.

## <a name="overview"></a>Pārskats

Sveiciena ziņojums jūsu E-komercijas tīmekļa vietnē var informēt apmeklētājus par notiekošo pārdošanu, vietnes atjauninājumiem vai sezonālo kolekciju pieejamību. Sveiciena ziņojums tiek iestatīts, izmantojot brīdinājuma moduli.

Brīdinājuma modulis ir jāpievieno galvenes fragmenta slotam **Kļūdas/informācijas ziņojumi**. Brīdinājuma modulis ļauj norādīt parādāmo tekstu, teksta krāsu un līdzinājumu. Tas arī ļauj norādīt, vai vietnes apmeklētāji var noraidīt šo ziņojumu.

Kad koplietojamam galvenes fragmentam tiek pievienots sveiciena ziņojums, tas tiks parādīts katrā lapā, kas lieto veidni, kurā tiek izmantots šis koplietojamais galvenes fragments.

Lai vietnei pievienotu sveiciena ziņojumu, veiciet tālāk norādītās darbības.

1. Dodieties uz savu vietni Commerce vietņu veidotājā.
1. Atlasiet **Fragmenti**.
1. Atlasiet galvenes fragmentu, kam pievienot ziņojumu.
1. Strukturējuma kokā izvērsiet **Kļūdas/informācijas ziņojumus**.
1. Atlasiet brīdinājuma moduli un pēc tam atlasiet **Labi**. Ja brīdinājuma modulis vēl nav izveidots, vispirms atlasiet daudzpunktes pogu (**...**) blakus **Kļūdas/informācijas ziņojumi** un pēc tam atlasiet **Pievienot moduli**.
1. Rekvizītu rūtī labajā pusē cilnē **Dati** atlasiet **Pievienot datu avotu** un pēc tam atlasiet **Saturs**.
1. Laukā **Ievades teksts** norādiet sveiciena ziņojuma tekstu.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu galvenes fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to. 

Tagad sveiciena ziņojums tiks parādīts katras vietnes lapas, kura izmanto atlasīto galvenes fragmentu, augšdaļā.

## <a name="additional-resources"></a>Papildu resursi

[Logotipa pievienošana](add-logo.md)

[Vietnes dizaina atlase](select-site-theme.md)

[Darbs ar CSS ignorēšanas failiem](css-override-files.md)

[Izlases ikonas pievienošana](add-favicon.md)

[Autortiesību paziņojuma pievienošana](add-copyright-notice.md)

[Valodu pievienošana vietnei](add-languages-to-site.md)

[Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju](add-telemetry.md)

