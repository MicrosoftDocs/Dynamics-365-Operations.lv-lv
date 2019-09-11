---
title: Aprēķināt noslodzes grafiku
description: Šajā tēmā paskaidrots, kā aprēķināt noslodzi programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c6d15861492a46ddb1222db2210f8c751ed38cb3
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886797"
---
# <a name="calculate-capacity-load"></a>Aprēķināt noslodzes grafiku

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Līdzekļu pārvaldniekā varat aprēķināt noslodzi

- uzturēšanas grafika rindām,  
- darba pasūtījumiem, kas vēl nav ieplānoti,  
- ieplānotajiem darba pasūtījumiem.

Tas ir noderīgi, ja vēlaties iegūt pārskatu par paredzamo noslodzi konkrētam periodam. Noslodzes aprēķinu var veikt visiem līdzekļiem vai atlasītiem līdzekļiem. Jūs varat izveidot aprēķinu arī dīkstāves uzturēšanas dēļ darbībām vai darba pasūtījumu apkopojumiem.

1. Klikšķiniet uz pogas **Līdzekļu pārvaldība** > **Pieprasījumi** > **Noslodze** vai **Līdzekļu pārvaldība** > **Vispārīgi** > **Darbu pasūtījuma kopas** > **Visas darbu pasūtījumu kopas** / **Aktīvās darba pasūtījumu kopas** >, atlasiet darba pasūtījumu kopu sarakstā > **Noslodze** vai **Līdzekļu pārvaldība** > **Vispārīgi** > **Dīkstāve uzturēšanas dēļ** > **Visas dīkstāves uzturēšanas dēļ darbības** / **Aktīvās dīkstāves uzturēšanas dēļ darbības** >, atlasīt uzturēšanas darbību sarakstā > **Noslodze**.

2. Dialogā **Aprēķināt noslodzi** atlasiet periodu, kuram vēlaties veikt aprēķinu, laukos **Sākuma datums/laiks** un **Beigu datums/laiks**.

3. Pārslēgšanas pogā **Iekļaut uzturēšanas grafiku** atlasiet "Jā", ja vēlaties iekļaut aprēķinā uzturēšanas grafika rindas.

4. Pārslēgšanas pogā **Iekļaut darba pasūtījumu**. atlasiet "Jā", ja vēlaties iekļaut aprēķinā darba pasūtījuma uzdevumus.

5. Jūs varat izmantot lauku **Līmenis**, lai noteiktu, cik detalizētu vēlaties noslodzes rindu aprēķinu attiecībā uz funkcionālo novietojumu. Piemēram, ja laukā ievadāt ciparu „1” un jums ir vairāklīmeņu funkcionālā novietojuma struktūra, visas uzturēšanas grafika rindas un darba pasūtījumus funkcionālajam novietojumam tiks uzrādītas augstākajā līmenī, tāpēc stundas rindā var tikt pievienotas no funkcionāliem novietojumiem, kas atrodas zemākā līmenī. Ja laukā **Līmenis** ievadāt ciparu „0”, jūs redzēsit detalizētu rezultātu, kas uzrādīs visas uzturēšanas grafika rindas un darba pasūtījumus visos funkcionālā novietojuma līmeņos, ar kuriem tie ir saistīti.

6. Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu.

7. Darbības rūšu grupās **Grupēt pēc...** klikšķiniet uz attiecīgās pogas, lai uzrādītu nepieciešamo aprēķina informācijas detalizācijas līmeni. Atlasītās darbības rūts grupēšanas pogas ir izceltas zilā krāsā. Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.

Zemāk esošajā attēlā ir parādīts saskarnes piemērs.

![1. attēls](media/01-capacity-planning.png)

>[!NOTE]
>Ja vēlaties koncentrēties tikai uz noslodzes plānošanu attiecībā uz ieplānotiem darba pasūtījumiem, skatiet [Aprēķināt noslodzi ieplānotiem darba pasūtījumiem](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).

