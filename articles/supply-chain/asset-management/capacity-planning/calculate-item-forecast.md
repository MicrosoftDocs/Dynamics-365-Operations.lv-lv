---
title: Aprēķināt krājumu prognozi
description: Šajā tēmā paskaidrots, kā aprēķināt vienuma prognozi programmā Asset Management.
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetItemForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 155dc720804196ccc44fad5eaf71e3563a9c68cf
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022562"
---
# <a name="calculate-item-forecast"></a>Aprēķināt krājumu prognozi

[!include [banner](../../includes/banner.md)]

 

Tāpat kā veikt noslodzes aprēķinus, kas aprakstīti iepriekšējā sadaļā, varat veikt arī vienuma prognozes aprēķinus.

- uzturēšanas grafika rindām,  
- darba pasūtījumiem, kas vēl nav ieplānoti,  
- ieplānotajiem darba pasūtījumiem.

Tas ir noderīgi, ja vēlaties iegūt pārskatu par paredzamo vienuma patēriņu (rezerves daļas un citi vienumi, kas vajadzīgi darba pasūtījuma pabeigšanai) noteiktam periodam. Vienuma prognozes aprēķinu var veikt visiem līdzekļiem vai atlasītiem līdzekļiem. Varat veikt arī dīkstāves uzturēšanas dēļ aprēķinu (**Visas dīkstāves uzturēšanas dēļ darbības** vai **Aktīvās dīkstāves uzturēšanas dēļ darbības**) vai darba pasūtījumu kopai (**Visas darba pasūtījumu kopas** vai **Aktīvās darba pasūtījumu kopas**).

1. Klikšķiniet uz pogas **Aktīvu pārvaldība** > **Pieprasījumi** > **Vienuma prognoze** vai **Līdzekļu pārvaldība** > **Kopīgi** > **Darbu pasūtījuma kopas** > **Visas darbu pasūtījumu kopas** / **Aktīvās darba pasūtījumu kopas** > atlasiet darba pasūtījumu kopu sarakstā > **Vienuma prognoze** vai **Aktīvu pārvaldība** > **Vispārīgi** > **Dīkstāve uzturēšanas dēļ** > **Visas dīkstāves uzturēšanas dēļ darbības** / **Aktīvās dīkstāves uzturēšanas dēļ darbības** > atlasiet uzturēšanas darbību sarakstā > **Vienuma prognoze**.

2. Dialogā **Aprēķināt vienuma prognozi** atlasiet periodu, kuram vēlaties veikt aprēķinu, laukos **Sākuma datums/laiks** un **Beigu datums/laiks**.

3. Pārslēgšanas pogā **Iekļaut uzturēšanas grafiku**. atlasiet "Jā", ja vēlaties iekļaut prognozes aprēķinā uzturēšanas grafika rindas.

4. Pārslēgšanas pogā **Iekļaut darba pasūtījumu**. atlasiet "Jā", ja vēlaties iekļaut prognozes aprēķinā darba pasūtījuma uzdevumus.

5. Jūs varat izmantot lauku **Līmenis**, lai noteiktu, cik detalizētas vēlaties vienuma prognozes rindas attiecībā uz funkcionālo novietojumu. 

      Piemēram, ja laukā ievadāt ciparu „1” un jums ir vairāklīmeņu funkcionālā novietojuma struktūra, visas uzturēšanas grafika rindas un darba pasūtījumus funkcionālajam novietojumam tiks uzrādītas augstākajā līmenī, tāpēc stundas rindā var tikt pievienotas no funkcionāliem novietojumiem, kas atrodas zemākā līmenī. 
  
      Ja laukā **Līmenis** ievadāt ciparu „0”, jūs redzēsit detalizētu rezultātu, kas uzrādīs visas uzturēšanas grafika rindas un darba pasūtījumus visos funkcionālā novietojuma līmeņos, ar kuriem tie ir saistīti.

6. Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu.

7. Grupās **Grupēt pēc...** noklikšķiniet uz attiecīgās pogas, lai uzrādītu nepieciešamo aprēķina informācijas detalizācijas līmeni. Attēlā tālāk atlasītās pogas **Grupēt pēc** ir izceltas zilā krāsā. Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.

8. Ja vēlaties rādīt produkta, glabāšanas vai izsekošanas īpašības, kas saistītas ar vienumu, noklikšķiniet uz **Rādīt izmērus**. Atzīmējiet attiecīgās izvēles rūtiņas un noklikšķiniet uz **Labi**.

![1. attēls](media/02-capacity-planning.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]