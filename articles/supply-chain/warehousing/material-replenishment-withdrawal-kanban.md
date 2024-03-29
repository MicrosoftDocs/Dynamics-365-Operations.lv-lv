---
title: Papildināšana ar atvilkumu Kanban
description: Šajā rakstā ir aprakstīts, kā atvilkuma Kanban tiek izmantots materiālu papildināšanai ražošanas aktivitātēm.
author: perlynne
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob, KanbanFlow, KanbanRules, WHSKanbanWaveTable, WHSKanbanWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 517b2eeb3b218fe0820ffa4e1d19b20841837b92
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863713"
---
# <a name="replenishment-with-withdrawal-kanbans"></a>Papildināšana ar atvilkumu Kanban

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā atvilkuma Kanban tiek izmantots materiālu papildināšanai ražošanas aktivitātēm.

## <a name="workflow-for-material-replenishment-that-uses-the-withdrawal-kanban"></a>Darbplūsma materiālu papildināšanai, kas izmanto atvilkumu Kanban

Atvilkumu Kanban darbus var izmantot, lai viena krājuma Kanban darbu pārvietotu starp noliktavām un ražošanas vietām, kur šis materiāls tiek patērēts. Atvilkumu Kanban darbi materiālu papildināšanai atbalsta no vilkšanas atkarīgu risinājumu, kur ir nepieciešams vilkšanas signāls, lai aktivizētu piegādi kādam specifiskam pieprasījumam. 

Nākamajā scenārijā ir parādīta uz vilkšanu balstīta papildināšanas sistēma, kur vilkšanas signāls aktivizē Kanban izveidošanu kāda ražošanas procesa materiālu papildināšanai. 

[![Vilkšanas signāls aktivizē Kanban izveidošanu kāda ražošanas procesa materiālu papildināšanai.](./media/material-replenishment-with-withdrawal-kanban.png)](./media/material-replenishment-with-withdrawal-kanban.png)

1.  Ieturēšanas Kanban
2.  Kanban novietojums “no” un izvietošanas novietojums noliktavas darbam
3.  Kanban novietojums “uz” un ražošanas ievades novietojums
4.  Ražošanas process
5.  Noliktavas darbs Kanban izdošanai
6.  Noliktavas novietojumi izejmateriālam
7.  Materiālu noliktava
8.  Ražošanas noliktava

Šajā scenārijā ražošanas process (4) materiālu no ražošanas ievades novietojuma (3) patērē ražošanas noliktavā (8). Kad materiālu apstrādes vienība (Kanban) tiek patērēta, tā tiek reģistrēta kā tukša. Krājuma izcelsmei tiek izveidots papildināšanas signāls, un tiek izveidots jauns Kanban (1). Šajā gadījumā krājuma izcelsme sastāv no novietojuma materiālu noliktavā (7). Kanban paredzētais materiāls tiek izdots un izvietots tās pašas noliktavas novietojumā (2). Kad šis materiāls tiek izdots, tas ir gatavs pārsūtīšanai no novietojuma 2 uz ražošanas ievades novietojumu (3) ražošanas noliktavā (8).

## <a name="configure-warehouse-work-for-kanban-picking-for-the-withdrawal-kanban"></a>Konfigurēt noliktavas darbu Kanban izdošanai attiecībā uz atvilkumu Kanban

Lai iespējotu izejmateriālu izdošanu atvilkumu Kanban darbam, konfigurējiet kopuma veidnes, darba veidnes un novietojuma direktīvas darba pasūtījuma tipam **Kanban izdošana**. Šis darba pasūtījuma tips atbalsta ne tikai izdošanas procesu atvilkumu Kanban darbam. Tas atbalsta arī izdošanas procesu ražošanas Kanban darbam. Taču katram Kanban tipam varat konfigurēt atsevišķu izdošanas procesu, atdalot kopuma veidnes, darba veidnes un novietojuma direktīvas. Lai nodalītu laidiena veidnes, darba veidnes un novietojuma direktīvas, šo elementu vaicājumos iestatiet kritēriju aktivitāšu tipam (**Process** vai **Pārsūtīšana**).

## <a name="configure-the-withdrawal-kanban"></a>Konfigurēt atvilkumu Kanban darbu

Pārsūtīšanas aktivitāte, kas tiek izmantota atvilkumu Kanban darbam, tiek konfigurēta kā daļa no aktivizētā aktivitāšu plāna racionālās ražošanas plūsmā. Kā daļu no pārsūtīšanas aktivitātes konfigurēšanas jūs norādāt pārsūtīšanas novietojumus “no” un “uz”. Kad ir konfigurēta pārsūtīšanas aktivitāte, varat to piešķirt Kanban nosacījumam ar tipu **Atvilkums**. Kanban nosacījums atvilkumu Kanban darbam iestata ierobežojumus un konfigurācijas. Kanban daudzums nosaka, cik materiālu apstrādes vienības šajā Kanban tiek ietverts pārsūtīšanas procesa laikā. Fiksētais Kanban daudzums tiek izmantots, kad ir atlasīta fiksētā papildināšanas stratēģija. Šis daudzumu nosaka, cik Kanban darbi ir nepieciešami, lai novērstu inventāra vai būvēšanas krājumu izbeigšanos pieprasījuma avotā. Fiksēto daudzumu var aprēķināt, balstoties uz faktisko pieprasījumu, vēsturisko pieprasījumu un pakalpojumu līmeņiem. Nākamajos divos scenārijos ir aprakstīts, kā pārvaldīt materiālu papildināšanu, kas izmanto atvilkumu Kanban darbu.

## <a name="scenario-1-replenish-a-production-input-location-by-using-a-fixed-withdrawal-kanban"></a>1. scenārijs. Papildināt ražošanas ievades novietojumu, izmantojot fiksētu atvilkumu Kanban darbu

Ražošanas process iegādāto izejmateriālu patērē no ražošanas ievades novietojuma, kas ir ražošanas noliktava. Kad šis izejmateriāls tiek saņemts no kreditora, tas tiek glabāts materiālu noliktavas novietojumos. Tā kā materiālu pieprasījums periodā tiek uzskatīts par stabilu, tam ir iestatīta piegāde ražošanai fiksēta daudzuma Kanban plūsmā. Kad Kanban tiek patērēts ražošanas ievades novietojumā, tiek reģistrēts tukšs signāls un plūsmai tiek pievienots jauns Kanban ar tādu pašu tipu. 

Tukšo signālu var konfigurēt tā, lai tas automātiski rastos, kad Kanban ir izpildīts. Ja vēlaties, tukšo signālu var iestatīt kā manuālu mijiedarbību, kas tiek dota vai nu no Kanban pārsūtīšanas paneļa, vai no izvēlnes pārnēsājamajā ierīcē. Kanban pārsūtīšanas panelis ir darbvieta, kur tiek pārvaldītas visas Kanban dzīves ciklā ietvertās aktivitātes. 

Kad tiek izveidots Kanban darbs, materiālu noliktavas Kanban kopumam tiek pievienota izejmateriālu kopuma rinda. Kanban pārsūtīšanas paneļa izdošanas sarakstā materiālu un saistīto noliktavas procesu statusu var pārraudzīt no kopuma izveidošanas līdz darba izveidošanai, līdz šis materiāls ir rīcībā esošs novietojumā “pārsūtīt no” un ir gatavs pārsūtīšanai uz ražošanas ievades novietojumiem. Kanban darbu var izpildīt vai nu no Kanban pārsūtīšanas paneļa, vai no izvēlnes pārnēsājamajā ierīcē. 

Šādā gadījumā izdošanas darbs materiālu noliktavā tiek apstrādāts kā viena aktivitāte. Pārsūtīšanas aktivitāte starp materiālu noliktavu un ražošanas noliktavu tiek apstrādāta kā atsevišķa aktivitāte. Šī metode var noderēt, ja, piemēram, starp abām noliktavām ir liels fiziskais attālums. Tādā gadījumā Kanban pārsūtīšanas aktivitāte var apzīmēt kravas automašīnas kravu. 

Ja attālums starp noliktavu novietojumiem un ražošanas ievades novietojumu ir mazs, iespējams, efektīvāk būtu pārsūtīšanas aktivitāti ietvert izdošanas procesā. Tad pēc materiāla izdošanas to var tieši novietot ražošanas ievades novietojumā. Lai atbalstītu šo procesu, jums pārsūtīšanas aktivitāte ir jākonfigurē tā, lai tā tiek izpildīta automātiski, kad tiek apstrādāts atvilkumu Kanban izdošanas darbs.

## <a name="scenario-2-automatically-complete-the-transfer-activity-when-kanban-picking-work-is-processed"></a>2. scenārijs. Automātiski izpildīt pārsūtīšanas aktivitāti, kad ir apstrādāts Kanban izdošanas darbs

Nākamajā scenārijā atvilkumu Kanban pārsūtīšanas aktivitāte ir konfigurēta tā, lai pārsūtītu starp diviem novietojumiem vienā un tajā pašā noliktavā. Atvilkumu Kanban pārsūtīšanas aktivitāte ir iestatīta tā, lai tā tiktu izpildīta automātiski. 

[![Pārsūtīšanas aktivitāte tiek automātiski izpildīta, kad tiek apstrādāts Kanban izdošanas darbs.](./media/transfer-activities-when-processing-kanban-picking.png)](./media/transfer-activities-when-processing-kanban-picking.png)

1.  Kopīga noliktavu izejmateriāliem un ražošanai
2.  Noliktavas novietojumi izejmateriāliem
3.  Kanban novietojums “no” un izvietošanas novietojums noliktavas darbam
4.  Atvilkumu Kanban
5.  Ražošanas ievades vieta
6.  Ražošanas process

Kad Kanban ir patērēts ražošanas ievades novietojumā, šis Kanban tiek ziņots kā tukšs un plūsmai tiek pievienots jauns Kanban. Kad tiek izveidots Kanban darbs, tad Kanban kopumam tiek pievienota kopuma rinda. Kad Kanban kopums tiek apstrādāts, tiek izveidots noliktavas darbs Kanban izdošanai. Noliktavas darbinieks apstrādā darbu Kanban izdošanai, un darbs viņu instruē izdot šo materiālu Kanban darbam noliktavas novietojumā. Kad šis noliktavas darbinieks apstiprina izdošanu, Kanban tiek automātiski izpildīts, un noliktavas darbinieks tiek instruēts izvietot materiālu ražošanas ievades novietojumā.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]