---
title: Darba pasūtījumu kopas
description: Šajā tēmā ir aprakstīts, kā strādāt ar darba pasūtījuma kopām līdzekļu pārvaldībā.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875778"
---
# <a name="work-order-pools"></a>Darba pasūtījumu kopas


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Darba pasūtījumu kopas var izmantot, lai grupētu darba pasūtījumus, kuriem ir kaut kas kopīgs. Piemēram, varat izveidot darba pasūtījumu kopas

- darba komandām, piemēram, uzturēšanas komanda A, uzturēšanas komanda B  

- profesionālajām prasmēm, piemēram, elektriķi vai santehniķi  

- fiziskām atrašanās vietām  

- laika grafikiem, piemēram, nedēļas vai citi periodi  


Ja nepieciešams, vienu darba pasūtījumu var ievietot daudzās darba pasūtījuma kopās.


## <a name="create-work-order-pool"></a>Darba pasūtījumu kopas izveide

Sadaļās **Visas darba pasūtījumu kopas** vai **Aktīvās darba pasūtījumu kopas** varat iegūt pārskatu par darba pasūtījuma kopām un izveidot jaunas kopas.

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Kopējs** > **Darba pasūtījumu kopas** > **Visas darba pasūtījumu kopas** vai **Aktīvās darba pasūtījuma kopas**.

2. Klikšķiniet **Jauns**.

3. Ievadiet darba pasūtījumu kopas ID laukā **Kopa** un ievadiet tās nosaukumu laukā **Nosaukums**.

4. Atlasiet “Jā” pie pārslēgšanas pogas **Aktīva**, lai norādītu, ka darba pasūtījumu kopa ir aktīva.

5. Atlasiet “Jā” pie pārslēgšanas pogas **Dzēst visas darba pasūtījuma relācijas**, ja vēlaties, lai darba pasūtījumi tiktu automātiski noņemti no darba pasūtījumu kopas.

6. Laukā **Dzēst dzīves cikla stāvokli** atlasiet darba pasūtījuma dzīves cikla stāvokli. Piemēram, darba pasūtījuma dzīves cikla stāvoklis, lai pabeigtu darba pasūtījumu, var tikt iestatīts automātiski dzēst relācijas ar darba pasūtījuma kopām.

7. Varat uzreiz sākt pievienot darba pasūtījumus darba pasūtījumu kopai. Kopsavilkuma cilnē **Darba pasūtījumi** noklikšķiniet uz **Pievienot rindu**.

8. Atlasiet darba pasūtījumu laukā **Darba pasūtījums**. Saistītie lauki tiek atjaunināti automātiski.

9. Atkārtojiet 7.–8. darbību, ja vēlaties pievienot papildu darba pasūtījumus.

10. Laukā **Kārtošanas secība** varat norādīt, vai darba pasūtījumi ir jāveic noteiktā secībā. Ievietojiet skaitļus 1, 2, 3 un tā tālāk, lai norādītu noteiktu secību atlasītajiem darba pasūtījumiem.

11. Noklikšķiniet uz pogas **Darba pasūtījumi**, lai skatītu sarakstu ar visiem darba pasūtījumiem, kas iekļauti darba pasūtījumu kopā.

12. Noklikšķiniet uz pogas **Noslodze**, lai atvērtu sadaļu **Noslodze**, lai aprēķinātu un skatītu noslodzi uzturēšanas grafikam, neplānotajiem darba pasūtījumiem un plānotajiem darba pasūtījumiem.

13. Noklikšķiniet uz pogas **Krājumu prognoze**, lai atvērtu sadaļu **Krājumu prognoze**, lai aprēķinātu un skatītu krājumu (rezerves daļu un citu nepieciešamo krājumu) prognozes saistībā ar uzturēšanas grafiku, neplānotajiem darba pasūtījumiem un plānotajiem darba pasūtījumiem.

14. Noklikšķiniet uz pogas **Darba pasūtījuma pirkšanas pieprasījums**, lai atvērtu sarakstu **Darba pasūtījuma pirkšanas pieprasījumi** un skatītu pirkšanas pieprasījumu sarakstu, kas saistīts ar darba pasūtījumiem darba pasūtījumu kopā.

15. Noklikšķiniet uz pogas **Darba pasūtījuma pirkšana**, lai atvērtu sarakstu **Darba pasūtījuma pirkšana** un skatītu pirkšanas pieprasījumus, kas saistīti ar darba pasūtījumiem darba pasūtījumu kopā.

>[!NOTE]
>Kad darba pasūtījumu kopa jūsu darba plānošanai vairs nav atbilstoša, iestatiet izvēles rūtiņu **Aktīva** uz “Nē” saraksta skatā **Darba pasūtījumu kopas**.

Ja vēlaties dzēst visas darba pasūtījumu rindas, atzīmējiet izvēles rūtiņu **Dzēst darba pasūtījumu relācijas**, piemēram, lai izveidotu tukšu kopu, ko vēlāk var izmantot citiem darba pasūtījumiem. Atcerieties noņemt izvēles rūtiņu **Dzēst darba pasūtījuma attiecības**, ja vēlaties izmantot darba pasūtījuma kopu, lai vēlāk izveidotu jaunas darba pasūtījuma attiecības.


![1. attēls](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a>Darba pasūtījuma pievienošana darba pasūtījumu kopai

Kā iepriekš aprakstīts šajā sadaļā, varat pievienot darba pasūtījumus darba pasūtījumu kopai, kad veidojat kopu. Darba pasūtījumu varat pievienot darba pasūtījumu kopai arī no kāda saraksta **Visi darba pasūtījumi**.

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Kopējs** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.

2. Sarakstā atlasiet darba pasūtījumu un noklikšķiniet uz **Darba pasūtījumu kopa**.

3. Laukā **Pievienot/noņemt** atlasiet “Pievienot”.

4. Atlasiet darba pasūtījumu kopu laukā **Kopa**.

5. Noklikšķiniet uz **Labi**.

6. Pēc tam, kad darba pasūtījums ir pievienots darba pasūtījumu kopai, ja vēlaties ievietot darba pasūtījumu kopā noteiktā secībā, atveriet vienu no darba pasūtījumu kopu saraksta lapām, atlasiet kopu un noklikšķiniet uz **Rediģēt** un pielāgojiet darba pasūtījumu, kas ietverti kopā, kārtošanas secību, atverot veidlapu **Darba pasūtījumu kopas** > kopsavilkuma cilni **Darba pasūtījumi** > lauku **Kārtošanas secība**.

Ja vēlaties noņemt atlasīto darba pasūtījumu no darba pasūtījumu kopas, 3. darbībā atlasiet “Noņemt”.

