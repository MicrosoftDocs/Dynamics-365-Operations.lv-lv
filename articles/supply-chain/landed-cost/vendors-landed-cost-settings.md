---
title: Kreditora iestatījumi pievienoti Kopējām izmaksām
description: Šajā tēmā aprakstīti jaunie lauki, kas tiek pievienoti esošai kreditoru lapai, kad iespējojat Kopējo izmaksu moduli. Izmantojiet šos laukus, lai iestatītu kreditorus, ko izmantosiet kopā ar Kopējo izmaksu funkcijām.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b4e02397f7a4cdeaa21b451268b16e4fbe773612
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690531"
---
# <a name="vendor-settings-added-for-landed-cost"></a>Kreditora iestatījumi pievienoti Kopējām izmaksām

[!include [banner](../../includes/banner.md)]

Šajā tēmā aprakstīti jaunie lauki, kas tiek pievienoti esošai **Kreditoru** lapai, kad iespējojat **Kopējo izmaksu** moduli. Izmantojiet šos laukus, lai iestatītu kreditorus, ko izmantosiet kopā ar Kopējo izmaksu funkcijām.

Lai iestatītu atbilstošos laukus, dodieties uz **Sagāde un plānošana \> Kreditori \> Visi kreditori**. Atveriet esošu kreditoru vai izveidojiet jaunu kreditoru un pēc tam atlasiet kopsavilkuma cilni **Detalizēta informācija par papildmaksu**. Visi jaunie lauki, ko **Kopējo izmaksu** modulis pievieno parādās zem **Reisu** galvenes. Tabulā ir sniegts lauku apraksts.

| Lauks | Apraksts |
|---|---|
| Nosūtīšanas veids | <p>Atlasiet kreditora lomu saistībā ar Kopīgajām izmaksām:</p><ul><li>**Neviens** – kreditoram nav specifiskas lomas, kas būtu saistīta ar Kopējām izmaksām. Šī vērtība ir noklusētais iestatījums, jo lielākajai daļai kreditoru, iespējams, nebūs noteiktas lomas.</li><li>**Piegādes uzņēmums** – kreditors ir nosūtīšanas uzņēmums. Kreditori ar šo nosūtīšanas tipu ir pieejami atlasei laukā **Nosūtīšanas uzņēmums** lapā **Reisi**.</li><li>**Muitas starpnieks** – kreditors ir muitas starpnieks. Kreditori ar šo nosūtīšanas tipu ir pieejami atlasei laukā **Muitas starpnieks** lapā **Folio**.</li><li>**Aģents** – kreditors ir aģents. Kreditori ar šo nosūtīšanas tipu ir pieejami atlasei laukā **Aģents** lapā **Kreditori** un **Pirkšanas pasūtījumi**.</li></ul> |
| Izmaksu veida grupa | Piešķiriet kreditoru izmaksu tipu grupai, lai atlasītu [automātiskās izmaksas](auto-cost-setup.md). |
| No ostas | Atlasiet reisa izcelsmes ostu. |
| Aģents | Noklusējuma aģents, ja pirkumi ir veikti no kreditora. |
| Importa izmaksu aprēķināšanas kreditors | <p>Norādiet, vai kreditors ir Kopējo izmaksu kreditors.</p><p>**Padoms:** Šo lauku var lietot kopā ar ieraksta līmeņa drošību, lai ierobežotu pirkšanas pasūtījumus, kas tiek rādīti, izveidojot reisu.</p> |
| Nosūtīšanas uzņēmums | Atlasiet noklusējuma piegādes uzņēmumu, kuru izmanto, kad kreditoram tiek izveidoti pirkšanas pasūtījumi. |
| Pakalpojumu sniedzējs | Norādiet, vai kreditors ir pakalpojumu sniedzējs. |
| Pārsniegšanas/nepārsniegšanas tolerances grupa | Atlasiet noklusēto kreditora pārsniegšanas/nepārsniegšanas tolerances grupu. |
