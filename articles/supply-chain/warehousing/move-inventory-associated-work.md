---
title: Krājumu kustība, ja ar tiem noliktavas pārvaldībā ir saistīts darbs
description: Izmantojot krājumu kustību, varat izlemt, kuriem noliktavas darbiniekiem ir atļauts pārvietot rezervētos krājumus.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d996886a90037f288e839c54c8c9d932cabb21f19f2aef1552ca82b192c96a51
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736555"
---
# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a>Krājumu kustība, ja ar tiem noliktavas pārvaldībā ir saistīts darbs

[!include [banner](../includes/banner.md)]

Izmantojot krājumu kustību, varat izlemt, kuriem noliktavas darbiniekiem ir atļauts pārvietot rezervētos krājumus. Tas nodrošina elastību regulētās noliktavās, kur varat izlemt, ka kādam darbiniekam netiek ļauts izvēlēties jaunu izdošanas novietojumu jau izveidotam izdošanas darbam. Turklāt noliktavas pārvaldniekam tā ļauj kontrolēt to, kuras iespējas ir jāpiešķir dažiem mazāk pieredzējušiem darbiniekiem.

Noliktavas darbinieku ikdienas operāciju pārvaldīšanas elastība var noderēt tālāk norādītajos scenārijos.

## <a name="scenario-1"></a>1. scenārijs

Uzņēmumam ir relatīvi maza saņemšanas zona, un tā ir pārslogota ar paletēm un kastēm, kas gaida izvietošanu. Pašreizējā dienā ir paredzēts piegādāt lielu sūtījumu, tādēļ saņemšanas darbinieks izlemj atbrīvot saņemšanas zonu, dažas paletes pārvietojot uz sekundāru ienākošo sagatavošanas zonu.

## <a name="scenario-2"></a>2. scenārijs

Pieredzējis noliktavas darbinieks pamana iespēju noliktavā krājumus konsolidēt vienā novietojumā, nevis tos sadalīt 3 netālu esošos novietojumos ar nelielu daudzumu katrā. Šis darbinieks vēlas konsolidēt daudzumu, katra šī novietojuma krājumus pārvietojot uz to pašu novietojumu un tajā pašā noliktavas vienībā.

## <a name="scenario-3"></a>3. scenārijs

Palete gaida sūtījumu sagatavošanas novietojumā, piemēram, STAGE01, kas atrodas netālu no BAYDOOR01. Taču sakarā ar plānu izmaiņām kravas auto pienākšana tiek plānota novietojumā BAYDOOR04. Nosūtīšanas darbinieks ir informēts par to, un viņam ir jānodrošina, ka kravas automašīnai nav jāgaida iekraušana no STAGE01. Nosūtīšanas darbinieks izlemj krājumus šajā sūtījumā no STAGE01 pārvietot uz STAGE04, kas ir tuvāk jaunajam mērķim.

### <a name="current-limitations"></a>Pašreizējie ierobežojumi

Pārvietot varat tikai tādas darba rezervācijas, kas ir Pārdošanas pasūtījums, Pārsūtīšanas pasūtījuma izejas plūsma, Pārsūtīšanas pasūtījuma ieejas plūsma, Pirkšanas pasūtījums un Papildināšanas darbs.

Krājumu pārvietošana ir ierobežota, lai novērstu darba rindu dalīšanu. Tas nozīmē, ka gadījumā, ja jums ir darba rinda 100 gab. krājumiem A no novietojuma Loc1, tad nevarat no turienes uz citu novietojumu pārvietot tikai 30 gab. šī krājuma A. Tas izraisītu esošās darba rindas dalīšanu uz 30 un 70, jo novietojumi tagad ir dažādi.

Sagatavošanas posmu scenārijiem, kur noliktavas vienība, no kuras jūs pārvietojat preces vai uz kuru jūs pārvietojat preces, darba pasūtījumam tiek iestatīta kā Mērķa LP, un ir atļauta tikai visas LP kustība, lai nesadalītu mērķa LP.

Pašlaik tiek atbalstītas tikai ekspromta kustības. Tas nozīmē, ka nevar pārvietot rezervētus krājumus, izmantojot kustību ar veidnes mobilās ierīces izvēlnes vienumiem.

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a>Rezervēto krājumu pārvietošanas atļaujas iestatīšana atsevišķiem darbiniekiem

Darbiniekam, kuram vēlaties atļaut pārvietot rezervētus krājumus, sadaļā **Noliktavas pārvaldība \> Iestatījumi \> Nodarbinātais** atzīmējiet izvēles rūtiņu **Atļaut krājumu kustību, ja ar tiem ir saistīts darbs**.  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
