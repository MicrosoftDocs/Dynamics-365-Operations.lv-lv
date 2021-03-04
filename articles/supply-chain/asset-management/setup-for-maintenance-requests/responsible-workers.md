---
title: Atbildīgie uzturēšanas speciālisti
description: Šajā tēmā izskaidrots, kā iestatīt uzturēšanas pieprasījumu veidus Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkerResponsible
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 113ee2b45c569c7dae3609f1027e31c4e5e5c54a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432888"
---
# <a name="responsible-maintenance-workers"></a>Atbildīgie uzturēšanas speciālisti

[!include [banner](../../includes/banner.md)]

 

Atbildīgi uzturēšanas speciālisti var būt saistīti ar līdzekļu veidiem, līdzekļiem, funkcionālajiem novietojumiem, uzturēšanas darbu veidu kategorijām, uzturēšanas darbu veidiem, uzturēšanas darbu veida variantiem un tirdzniecību. Tos var izmantot darba pasūtījumos un uzturēšanas pieprasījumos, lai norādītu prioritāti uzturēšanas speciālistiem, kuriem jābūt atbildīgiem par darba pasūtījumu. (Tomēr šie uzturēšanas speciālisti ne vienmēr ir tie paši darbinieki, kuri ir ieplānoti darba pasūtījuma veikšanai.) Šīs funkcionalitātes izmantošana nav obligāta. Piemēram, to var izmantot, lai atlasītu atbildīgos darbiniekus vai darbinieku grupas konkrētiem darba veidiem vai darba apgabaliem.

Darba pasūtījuma dzīves cikla vai uzturēšanas pieprasījuma dzīves ciklā laikā atbildīgos uzturēšanas speciālistus var mainīt vai atjaunināt. Šī maiņa vai atjaunināšana var būt saistīta, piemēram, ar izmaiņām uzturēšanas pieprasījuma dzīves cikla stāvoklī vai darba pasūtījuma dzīves cikla stāvoklī.

Darba pasūtījuma plānošanas laikā iestatīšana lapā **Atbildīgie uzturēšanas speciālisti** *netiek* izmantota.

> [!NOTE]
> Līdzekļu pārvaldībā var arī iestatīt *vēlamus* uzturēšanas speciālistus, kuri var tikt piešķirti darba pasūtījumiem darba pasūtījumu plānošanas laikā.

Pirms varat iestatīt atbildīgos uzturēšanas speciālistus, ir jāiestata darbinieki un uzturēšanas speciālistu grupas, kam jābūt pieejamiem atlasei. Informāciju par to, kā iestatīt darbiniekus un uzturēšanas speciālistu grupas, skatiet nodaļā [Uzturēšanas speciālisti un speciālistu grupas](../setup-for-objects/workers-and-worker-groups.md).

## <a name="set-up-responsible-maintenance-workers"></a>Iestatīt atbildīgos uzturēšanas speciālistus

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Speciālisti** \> **Atbildīgie uzturēšanas speciālisti**.
2. Atlasiet **Jauns**, lai izveidotu ierakstu.
3. Vispirms izveidojiet noklusējuma atbildīgo uzturēšanas speciālistu vai atbildīgo uzturēšanas speciālistu grupas iestatījumu, kur iestatāt tikai lauku **Atbildīgo uzturēšanas speciālistu grupa** un/vai lauku **Atbildīgais darbinieks**. Atlikušos laukus atstājiet tukšus. Šis noklusējuma iestatījums tiks izmantots darba pasūtījuma plānošanā, ja neviena cita specifiska kombinācija neatbilst darba pasūtījuma saturam.

    > [!NOTE]
    > Uzturēšanas pieprasījuma izveides laikā, kad atbildīgais uzturēšanas speciālists vai atbildīgo uzturēšanas speciālistu grupa tiek darīta pieejama atlasei lapā **Visi uzturēšanas pieprasījumi**, Līdzekļu pārvaldība iziet cauri visiem atbildīgo uzturēšanas speciālistu ierakstiem, lai pārbaudītu iespējamu atbilstību. Tā vienmēr vispirms pārbauda visraksturīgāko kombināciju. Citiem vārdiem sakot, Līdzekļu pārvaldība vispirms pārbauda atbilstību laukam **Tirdzniecība**. Ja atbilstība netiek atrasta, tā meklē atbilstību laukam **Uzturēšanas darba veida variants**. Ja atbilstība netiek atrasta, tā meklē atbilstību laukam **Uzturēšanas darba veids** un tā tālāk. Kā varat redzēt lapas izkārtojumā, šī uzvedība nozīmē, ka, lai atrastu visspecifiskāko kombināciju, Līdzekļu pārvaldība pārbauda katru ierakstu no labās puses uz kreiso, meklējot atbilstību (vispirms **Tirdzniecība**, tad **Uzturēšana darba veida variants**, tad **Uzturēšanas darba veids**, tad **uzturēšanas darba veidu kategorija**, tad **Funkcionālais novietojums**, tad **Līdzeklis** un visbeidzot **Līdzekļu veids**). Ja atbilstība netiek atrasta, tiek izmantots "noklusējuma" ieraksts, kam nav atlases iespēju šajos septiņos laukos.

Nākamajā attēlā ir parādīts sarakstu lapas **Atbildīgie uzturēšanas speciālisti** piemērs.

![Atbildīgas uzturēšanas nodarbināto lapa](media/08-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]