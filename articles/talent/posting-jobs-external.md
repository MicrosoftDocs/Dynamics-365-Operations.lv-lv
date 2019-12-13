---
title: Vakanču publicēšana Broadbean no pakalpojuma Attract
description: Šajā tēmā ir sniegta informācija par to, kā izmantot Dynamics 365 Talent - Attract, lai publicētu darbus Broadbean
author: pganapmsft
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 41fa057606887069a9ea0f1f2178eeaff59f33ca
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832663"
---
# <a name="post-jobs-to-broadbean-from-attract"></a>Vakanču publicēšana Broadbean no pakalpojuma Attract

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talent: Attract palīdz jums iegūt darbinieku, kas jums nepieciešams, ļaujot jums publicēt vakances tieši no Attract vietnē Broadbean. Kad esat [izveidojis vakanci](./creating-jobs-attract.md), viss, kas jums jādara, ir noklikšķināt uz pogas, lai jūsu vakance tiktu rādīta visiem potenciālajiem darba kandidātiem vietnē Broadbean.

Darbu publicēšanai Broadbean ir nepieciešama atbilstoša Broadbean licence. Broadbean piedāvā dažādus produktus un plānus. Lai iegūtu vairāk informācijas par Broadbean licencēšanu un cenām, [sazinieties ar Broadbean](https://www.broadbean.com/contact-us/).

Ja esat administrators, kuram ir nepieciešama plašāka informācija par to, kā konfigurēt Broadbean integrāciju ar sistēmu Attract, skatiet [Broadbean integrācijas iestatīšana programmā Microsoft Dynamics 365 Talent - Attract](./attract-admin-job-board-settings.md).

## <a name="post-jobs-to-broadbean"></a>Darbu publicēšana vietnē Broadbean

Kad vietne Broadbean ir ieslēgta, personāla atlases darbinieki un administratori var publicēt tajā darbu. Ir nepieciešams pieteikšanās uz darbu URL.

1. Pakalpojumā Attract atveriet darbu, kuru vēlaties publicēt vietnē Broadbean.
2. Sadaļā **Publikācijas** atlasiet pogu **Publicēt tagad**, kas atbilst vietnei Broadbean.
3. Izpildiet norādījumus Broadbean logā.

Pakalpojums Attract nosūta uz vietni Broadbean tālāk norādīto informāciju.

- Pieprasījuma ID
- Amata nosaukums
- Darba apraksts
- Amata atrašanās vieta
- Pieteikšanās URL
- Personāla atlases speciālista informācija

Kad publicēšana vietnē Broadbean ir sekmīgi pabeigta, pakalpojuma Attract darba sadaļā **Publikācijas** tiek parādīts Broadbean statuss **Publicēts**.

> [!NOTE]
> - Vietnē Broadbean ir obligāti jāaizpilda lauks **Nozare**. Šobrīd šis lauks pēc noklusējuma ir iestatīts ar vērtību **IT**. Tomēr šo vērtību var nomainīt ar pareizo nozares opciju Broadbean darbu publicēšanas logā.
> - Darba publicēšanas visos atlasītajos darbu sludinājumu dēļos pabeigšana vietnē Broadbean ilgst kādu laiku. Tāpēc var būt neliela aizkavēšanās, līdz pakalpojums Attract nodrošina darba statusa atjauninājumu.

### <a name="view-a-broadbean-job-posting"></a>Broadbean darba publikācijas skatīšana

Kad darbs ir publicēts vietnē Broadbean, to var skatīt, izmantojot pakalpojumu Attract.

1. Atveriet pakalpojumā Attract darbu, kuru vēlaties skatīt vietnē Broadbean.
2. Cilnē **Publikācijas** atlasiet daudzpunktes pogu (**...**), kas atbilst vietnei Broadbean, un pēc tam atlasiet **Skatīt**.

Vietnē Broadbean publicētais darbs tiek parādīts jaunā logā.

### <a name="update-a-broadbean-job-posting"></a>Broadbean darba publikācijas atjaunināšana

Darba publikāciju vietnē Broadbean var atjaunināt divējādi.

1. Atveriet pakalpojumā Attract darbu, kuru vēlaties atjaunināt.
2. Sadaļā **Publikācijas** atlasiet pogu **Atjaunināt publikāciju**, kas atbilst vietnei Broadbean.
3. Publikāciju rediģēšana Broadbean logā.

    –vai–

1. Atveriet pakalpojumā Attract darbu, kuru vēlaties skatīt vietnē Broadbean.
2. Sadaļā **Publikācijas** atlasiet daudzpunktes pogu (**...**), kas atbilst vietnei Broadbean, un pēc tam atlasiet **Skatīt**.
3. Broadbean logā rediģējiet darba datus un pēc tam vēlreiz publicējiet darbu. Darba dati pakalpojumā Attract netiek mainīti.

### <a name="remove-a-broadbean-job-posting"></a>Broadbean darba publikācijas noņemšana

Ja nepieciešamas, darba publikāciju vietnē Broadbean var noņemt.

1. Atveriet pakalpojumā Attract darbu, kuru vēlaties noņemt.
2. Sadaļā **Publikācijas** atlasiet daudzpunktes pogu (**...**), kas atbilst vietnei Broadbean, un pēc tam atlasiet **Noņemt publikāciju**.

Kad darba publikācija vietnē Broadbean ir noņemta, pakalpojumā Attract Broadbean elementam ir pieejama poga **Publicēt tagad**. Šīs pogas klātbūtne norāda, ka darbs ir noņemts un to var publicēt atkal.

### <a name="troubleshoot-job-posting-to-broadbean"></a>Problēmu novēršana darbu publicēšanā vietnē Broadbean

Ja darba publicēšana vietnē Broadbean rada problēmas, veiciet tālāk norādītās darbības.

1. Pārbaudiet, vai pakalpojumā Attract ievadītie Broadbean akreditācijas dati ir derīgi un pareizi.
2. Ja akreditācijas dati ir derīgi un pareizi, sazinieties ar [Broadbean atbalsta centru](https://www.broadbean.com/resources/support/).
3. Ja problēma joprojām pastāv, sazinieties ar [Microsoft atbalsta centru](./talent-support.md).

## <a name="see-also"></a>Skatiet arī

[Darbu izveide, apstiprināšana un grāmatošana programmā Attract](./creating-jobs-attract.md)

[Iespējot Broadbean integrāciju programmā Microsoft Dynamics 365 Talent - Attract](./attract-admin-job-board-settings.md)
