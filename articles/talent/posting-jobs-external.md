---
title: Darbu publicēšana ārējās karjeras vietnēs no pakalpojuma Attract
description: Šajā tēmā ir sniegta informācija par to, kā izmantot Dynamics 365 for Talent - Attract, lai publicētu darbus ārējās personāla atlases vietnēs
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
ms.openlocfilehash: 9c27d1810a89ed7d7a7745e41c5f118dbdfe5dda
ms.sourcegitcommit: cadce85ca3004d53caf6bc49147a524c1bfd421f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/16/2019
ms.locfileid: "1590486"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a>Darbu publicēšana ārējās karjeras vietnēs no pakalpojuma Attract

[!include [banner](../includes/banner.md)]

Jūs vēlaties, lai jūsu atvērtās pozīcijas redz iespējami daudz kvalificētu kandidātu. Personāla atlases vietnes, piemēram, Broadbean, palīdz jums sasniegt šo mērķi. Microsoft Dynamics 365 Talent: pakalpojums Attract tagad ļauj jums publicēt vietnē Broadbean, un Microsoft pastāvīgi nodrošina jaunu piedāvājumu šajā jomā.

## <a name="post-jobs-to-broadbean"></a>Darbu publicēšana vietnē Broadbean

Lai varētu publicēt darbus vietnē Broadbean, vispirms ir jākonfigurē Broadbean integrācija.

> [!NOTE]
> - Lai publicētu darbus ārējās vietnēs, ir nepieciešama [visaptveroša nolīgšanas pievienojumprogramma](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).
> - Lai grāmatotu darbus programmatūrā Broadbean, izmantojot Attract, jums ir nepieciešams Broadbean abonements.
> - Šis līdzeklis pašreiz ir priekšskatījumā. Ja vēlaties to izmēģināt, jums [tā ir jāieslēdz pakalpojuma Attract administratora iestatījumos](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).

### <a name="configure-broadbean-integration"></a>Broadbean integrācijas konfigurēšana

1. Piesakieties pakalpojumā Attract kā administrators.
2. Atlasiet pogu **Iestatījumi** (zobrata simbols) lapas labās puses augšējā stūrī un pēc tam atlasiet **Administrēšanas centrs**.
3. Sadaļas **Iespējot Broadbean integrāciju** cilnē **Darbu sludinājuma dēļa iestatījumi** ieslēdziet integrāciju.
4. Sazinieties ar Broadbean un ievadiet informāciju laukā **Lietotājvārds, Klienta ID, Šifrēšanas pilnvara**.

> [!WARNING]
> Jūsu Broadbean akreditācijas dati ir jutīgi un konfidenciāli. Tāpēc glabājiet un koplietojiet tos atbildīgi. Ikviena persona, kurai administratora loma pakalpojumā Attract, var skatīt šos akreditācijas datus.

> [!NOTE]
> Microsoft un Attract nav iesaistīti šo vērtību izveidē un saglabāšanā. Jūsu pienākums ir tos atjaunināt pakalpojumā Attract un sadarboties ar Broadbean, lai atrisinātu jebkādas problēmas, kas ir saistītas ar jūsu akreditācijas datiem.

### <a name="post-a-job-to-broadbean"></a>Darba publicēšana vietnē Broadbean

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
2. Sadaļā **Publikācijas** atlasiet daudzpunktes pogu (**...**), kas atbilst vietnei Broadbean, un pēc tam atlasiet **Skatīt**.

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

### <a name="troubleshoot-the-broadbean-integration"></a>Ar Broadbean integrāciju saistīto problēmu novēršana

Ja darba publicēšana vietnē Broadbean rada problēmas, veiciet tālāk norādītās darbības.

1. Pārbaudiet, vai pakalpojumā Attract ievadītie Broadbean akreditācijas dati ir derīgi un pareizi.
2. Ja akreditācijas dati ir derīgi un pareizi, sazinieties ar [Broadbean atbalsta centru](https://www.broadbean.com/resources/support/).
3. Ja problēma joprojām pastāv, sazinieties ar [Microsoft atbalsta centru](./talent-support.md).
