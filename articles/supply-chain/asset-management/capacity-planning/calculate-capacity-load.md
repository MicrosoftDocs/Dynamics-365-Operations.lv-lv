---
title: Noslodzes grafika aprēķināšana
description: Šajā rakstā ir izskaidrots, kā aprēķināt noslodzes grafiku Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCapacityLoad, EntAssetWorkOrderCapacityLoadCalculate, EntAssetWorkOrderCapacityLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 95d1e38db8e4658a57f36139836264b87d525e61
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016135"
---
# <a name="calculate-capacity-load"></a>Aprēķināt noslodzes grafiku

[!include [banner](../../includes/banner.md)]


Līdzekļu pārvaldībā varat aprēķināt noslodzi

- uzturēšanas grafika rindām,  
- darba pasūtījumiem, kas vēl nav ieplānoti,  
- ieplānotajiem darba pasūtījumiem.

Tas ir noderīgi, ja vēlaties iegūt pārskatu par paredzamo noslodzi konkrētam periodam. Noslodzes aprēķinu var veikt visiem līdzekļiem vai atlasītiem līdzekļiem. Jūs varat izveidot aprēķinu arī dīkstāves uzturēšanas dēļ darbībām vai darba pasūtījumu apkopojumiem.

1. **·** > **·** > **·** **·** > **·** > **·** / **Noklikšķiniet** uz Līdzekļu pārvaldības uzziņas Noslodzes noslodzes noslodze vai Līdzekļu pārvaldības darba pasūtījumu kopas Visas darba pasūtījumu kopas Aktīvās darba pasūtījumu kopas > atlasiet darbu pasūtījumu kopu sarakstā > **·** **·** > **·** > **·** / **Noslodzes** noslodzes poga vai Līdzekļu pārvaldības dīkstāves uzturēšanas dīkstāves aktivitātes Visas uzturēšanas dīkstāves aktivitātes > atlasiet uzturēšanas aktivitāti sarakstā > **Noslodzes** noslodze.

2. Dialogā **Aprēķināt noslodzi** atlasiet periodu, kuram vēlaties veikt aprēķinu, laukos **Sākuma datums/laiks** un **Beigu datums/laiks**.

3. Pārslēgšanas pogā **Iekļaut uzturēšanas grafiku** atlasiet "Jā", ja vēlaties iekļaut aprēķinā uzturēšanas grafika rindas.

4. Pārslēgšanas pogā **Iekļaut darba pasūtījumu**. atlasiet "Jā", ja vēlaties iekļaut aprēķinā darba pasūtījuma uzdevumus.

5. Jūs varat izmantot lauku **Līmenis**, lai noteiktu, cik detalizētu vēlaties noslodzes rindu aprēķinu attiecībā uz funkcionālo novietojumu. 

    Piemēram, ja laukā ievadāt ciparu „1” un jums ir vairāklīmeņu funkcionālā novietojuma struktūra, visas uzturēšanas grafika rindas un darba pasūtījumus funkcionālajam novietojumam tiks uzrādītas augstākajā līmenī, tāpēc stundas rindā var tikt pievienotas no funkcionāliem novietojumiem, kas atrodas zemākā līmenī. 
    
    Ja laukā **Līmenis** ievadāt ciparu „0”, jūs redzēsit detalizētu rezultātu, kas uzrādīs visas uzturēšanas grafika rindas un darba pasūtījumus visos funkcionālā novietojuma līmeņos, ar kuriem tie ir saistīti.

6. Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu.

7. Grupās **Grupēt pēc...** noklikšķiniet uz attiecīgās pogas, lai uzrādītu nepieciešamo aprēķina informācijas detalizācijas līmeni. Attēlā tālāk atlasītās pogas **Grupēt pēc** ir izceltas zilā krāsā. Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.

    ![1. attēls.](media/01-capacity-planning.png)

>[!NOTE]
>Ja vēlaties koncentrēties tikai uz noslodzes plānošanu attiecībā uz ieplānotiem darba pasūtījumiem, skatiet [Aprēķināt noslodzi ieplānotiem darba pasūtījumiem](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]