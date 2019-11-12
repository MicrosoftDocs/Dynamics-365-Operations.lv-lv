---
title: Darba pasūtījumu kopas
description: Šajā tēmā ir aprakstīts, kā strādāt ar darba pasūtījuma kopām līdzekļu pārvaldībā.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 161244cb4451ddc7b13b579fd02e828a61adeea4
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626366"
---
# <a name="work-order-pools"></a>Darba pasūtījumu kopas

[!include [banner](../../includes/banner.md)]


Darba pasūtījumu kopas var izmantot, lai grupētu darba pasūtījumus, kuriem ir kaut kas kopīgs. Šeit ir daži piemēri lietām, kurām varat izveidot darba pasūtījumu kopas:

- Darba komandām, piemēram, Uzturēšanas komanda A vai Uzturēšanas komanda B  

- Profesionālajām prasmēm, piemēram, elektriķi vai santehniķi  

- Fiziskām atrašanās vietām  

- Laika grafikiem, piemēram, nedēļas vai citi periodi  

Pēc nepieciešamības, varat iekļaut vienu darba pasūtījumu vairākās darbu pasūtījumu kopās.


## <a name="create-a-work-order-pool"></a>Darba pasūtījumu kopas izveide

Sarakstu lapās **Visas darba pasūtījumu kopas** vai **Aktīvās darba pasūtījumu kopas** varat iegūt pārskatu par darba pasūtījuma kopām un izveidot jaunas kopas.

1. Atlasiet **Līdzekļu pārvaldība** > **Kopējs** > **Darba pasūtījumu kopas** > **Visas darba pasūtījumu kopas** vai **Aktīvās darba pasūtījuma kopas**.

2. Atlasiet **Jauns**.

3. Laukā **Kopa** ievadiet ID darba pasūtījumu kopai.

4. Laukā **Nosaukums** ievadiet nosaukumu.

5. Uzstādiet opciju **Aktīvs** uz **Jā**, lai norādītu, ka darba pasūtījumu kopa ir aktīva.

6. Uzstādiet opciju **Dzēst darba pasūtījuma attiecības** uz **Jā**, ja vēlaties, lai darba pasūtījumi tiktu automātiski noņemti no darba pasūtījumu kopas.

7. Laukā **Dzēst dzīves cikla stāvokli** atlasiet darba pasūtījuma dzīves cikla stāvokli. Piemēram, darba pasūtījuma dzīves cikla stāvoklis, lai pabeigtu darba pasūtījumu, var tikt iestatīts automātiski dzēst relācijas ar darba pasūtījuma kopām.

    Varat uzreiz sākt pievienot darba pasūtījumus darba pasūtījumu kopai.

8. Kopsavilkuma cilnē **Darba pasūtījumi** atlasiet **Pievienot rindu**.

9. Atlasiet darba pasūtījumu laukā **Darba pasūtījums**. Saistītie lauki tiek atjaunināti automātiski.

10. Atkārtojiet 8. līdz 9. soli, lai pievienotu vairāk darba pasūtījumus.

11. Ja darba pasūtījumi, ko pievienojāt, ir jāveic noteiktā kārtībā, laukā **Kārtošanas secība** varat ievadīt ciparus **1**, **2**, **3** utt., lai precizētu šo pasūtījumu.

12. Lai skatītu sarakstu ar visiem darba pasūtījumiem, kas ir iekļauti darba pasūtījumu kopā, darbības rūtī cilnē **Darba pasūtījumu kopa**, kas atrodas grupā **Skatīt saistīto darba pasūtījumu kopu**, atlasiet **Darba pasūtījumus**, lai atvērtu **Visu darbu pasūtījumu** saraksta lapa.

13. Lai aprēķinātu un skatītu noslodzi uzturēšanas grafikam, neplānotiem darba pasūtījumiem un ieplānotajiem darba pasūtījumiem, darbību rūtī cilnē **Darba pasūtījumu kopa**, kas atrodas grupā **Skatīt saistīto darba pasūtījumu kopu**, atlasiet **Noslodze**, lai atvērtu dialogu **Aprēķināt noslodzi**.

14. Lai aprēķinātu un skatītu prognozes precēm (rezerves daļas un cita nepieciešamās preces), kas ir saistītas ar uzturēšanas grafiku, neplānotiem darba pasūtījumiem un ieplānotajiem darba pasūtījumiem, darbību rūtī cilnē **Darba pasūtījumu kopa**, kas atrodas grupā **Skatīt saistīto darba pasūtījumu kopu**, atlasiet **Preču prognoze**, lai atvērtu dialogu **Aprēķināt preču prognozi**.

15. Lai skatītu sarakstu ar visiem pirkšanas pieprasījumiem, kas ir saistīti ar darba pasūtījumiem to kopā, darbības rūtī cilnē **Darba pasūtījumu kopa**, kas atrodas grupā **Sagāde**, atlasiet **Darba pasūtījumu pirkšanas pieprasījumu**, lai atvērtu **Darba pasūtījumu pirkšanas pieprasījumu** saraksta lapa.

16. Lai skatītu sarakstu ar visiem pirkšanas pasūtījumiem, kas ir saistīti ar darba pasūtījumiem to kopā, darbības rūtī cilnē **Darba pasūtījumu kopa**, kas atrodas grupā **Sagāde**, atlasiet **Darba pasūtījumu pirkšana**, lai atvērtu **Darba pasūtījumu pirkšanas** saraksta lapu.

>[!NOTE]
>Kad darba pasūtījumu kopa jūsu darba plānošanai vairs nav atbilstoša, iestatiet opciju **Aktīvs** attiecīgajai kopai uz **Nē** saraksta skatā **Darba pasūtījumu kopas** lapā.

Lai dzēstu visas darbinieka pasūtījuma rindas, iestatiet opciju **Dzēst darba pasūtījumu attiecības** uz **Jā**. Šī opcija noder, piemēram, ja vēlaties izveidot tukšu kopu, ko vēlāk var izmantot citiem darba pasūtījumiem. Atcerieties iestatīt opciju **Dzēst darba pasūtījuma attiecības** uz **Nē**, kad esat gatavi izmantot darba pasūtījuma kopu, lai vēlāk izveidotu jaunas darba pasūtījuma attiecības.

Attēlā tālāk ir parādīts sarakstu lapas **Darba pasūtījumu kopa** piemērs.

![1. attēls](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a>Darba pasūtījuma pievienošana darba pasūtījumu kopai

Kā aprakstīts iepriekšējā sadaļā, varat pievienot darba pasūtījumus darba pasūtījumu kopai, kad veidojat kopu. Darba pasūtījumus var pievienot arī darba pasūtījumu kopai **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi** saraksta lapā.

1. Atlasiet darba pasūtījumu un pēc tam darbības rūtī, cilnē **Darba pasūtījums** grupā **Uzturēt** atlasiet **Darba pasūtījumu kopa**.

2. Sarakstā atlasiet darba pasūtījumu un noklikšķiniet uz **Darba pasūtījumu kopa**.

3. Dialogā **Uzturēt darba uzdevumu kopu**, laukā **Pievienot/noņemt** atlasiet **Pievienot**.

4. Atlasiet darba pasūtījumu kopu laukā **Kopa**.

5. Atlasiet **Labi**.

6. Lai noliktu darba pasūtījumu, ko pievienojāt noteiktam pasūtījumam darba pasūtījumu kopā, **Visas darba pasūtījumu kopas** vai **Aktīvo darbu pasūtījumu kopas** saraksta lapā, atlasiet kopu un pēc tam atlasiet **Rediģēt**. Pēc tam lapā **Darba pasūtījumu kopa** kopsavilkuma cilnē **Darba pasūtījumi** lietojiet lauku **Kārtot secību**, lai koriģētu kārtošanas secību darba pasūtījumiem, kas iekļauti kopā.

Lai noņemtu darba pasūtījumu no darba pasūtījumu kopas, atkārtojiet šīs darbības, bet atlasiet opciju **Noņemt** 3. solī.

