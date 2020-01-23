---
title: Sveiciena ziņojuma pievienošana
description: Šajā tēmā ir aprakstīts, kā pievienot sveiciena ziņojumu savai Microsoft Dynamics 365 Commerce tīmekļa vietnei.
author: psimolin
manager: annbe
ms.date: 12/12/2019
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
ms.openlocfilehash: 4e9deeeaf491b77700ba0833e429f05d376a4392
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914520"
---
# <a name="add-a-welcome-message"></a>Sveiciena ziņojuma pievienošana

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā pievienot sveiciena ziņojumu savai Microsoft Dynamics 365 Commerce tīmekļa vietnei.

## <a name="overview"></a>Pārskats

Sveiciena ziņojums jūsu E-komercijas tīmekļa vietnē var informēt apmeklētājus par notiekošo pārdošanu, vietnes atjauninājumiem vai sezonālo kolekciju pieejamību. Sveiciena ziņojums tiek iestatīts, izmantojot brīdinājuma moduli.

Brīdinājuma modulis ir jāpievieno galvenes fragmenta slotam **Kļūdas/informācijas ziņojumi**. Brīdinājuma modulis ļauj norādīt parādāmo tekstu, teksta krāsu un līdzinājumu. Tas arī ļauj norādīt, vai vietnes apmeklētāji var noraidīt šo ziņojumu.

Kad koplietojamam galvenes fragmentam tiek pievienots sveiciena ziņojums, tas tiks parādīts katrā lapā, kas lieto veidni, kurā tiek izmantots šis koplietojamais galvenes fragments.

Lai vietnei pievienotu sveiciena ziņojumu, veiciet tālāk norādītās darbības.

1. Programmā Dynamics 365 Commerce dodieties uz savu vietni.
1. Atlasiet **Fragmenti**.
1. Atlasiet galvenes fragmentu, kam pievienot ziņojumu.
1. Strukturējuma kokā izvērsiet **Kļūdas/informācijas ziņojumus**.
1. Atlasiet brīdinājuma moduli.

    Ja brīdinājuma modulis vēl nav izveidots, atlasiet daudzpunktes pogu (**...**) blakus **Kļūdas/informācijas ziņojumi** un pēc tam atlasiet **Pievienot moduli**. Atlasiet brīdinājuma moduli un pēc tam atlasiet **Labi**.

1. Rekvizītu rūtī labajā pusē cilnē **Dati** atlasiet **Pievienot datu avotu** un pēc tam atlasiet **Saturs**.
1. Laukā **Ievades teksts** norādiet sveiciena ziņojuma tekstu.
1. Saglabājiet galvenes fragmentu, pārbaudiet un publicējiet to.

Tagad sveiciena ziņojums tiks parādīts katras vietnes lapas, kura izmanto atlasīto galvenes fragmentu, augšdaļā.

## <a name="additional-resources"></a>Papildu resursi

[Logotipa pievienošana](add-logo.md)

[Vietnes dizaina atlase](select-site-theme.md)

[Darbs ar CSS ignorēšanas failiem](css-override-files.md)

[Izlases ikonas pievienošana](add-favicon.md)

[Autortiesību paziņojuma pievienošana](add-copyright-notice.md)

[Valodu pievienošana vietnei](add-languages-to-site.md)

[Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju](add-telemetry.md)

