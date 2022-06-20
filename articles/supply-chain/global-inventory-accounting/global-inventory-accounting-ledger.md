---
title: Globālo krājumu uzskaites virsgrāmata
description: Šajā rakstā ir aprakstītas globālās krājumu uzskaites virsgrāmatas, kas definētas, izmantojot valūtas kombināciju, kalendāru, konvenciju un saistību ar juridisku personu.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4d3779d7d335a903d7eabfadfed79e47652c6835
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897666"
---
# <a name="global-inventory-accounting-ledger"></a>Globālo krājumu uzskaites virsgrāmata

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

Globālajai krājumu uzskaitei ir sava Virsgrāmatu kopa. Katru reizi, kad ar krājumu saistīta transakcija tiek apstrādāta saistītai juridiskajai personai, sistēma var šo transakciju ņemt vērā jebkurā Globālās krājumu uzskaites Virsgrāmatā, ja nepieciešams.

Virsgrāmata ir debeta un kredīta pasākumu reģistrs. Šie pasākumi tiek klasificēti, izmantojot izmaksu elementus un apakšgrāmatas kontus. Globālās krājumu uzskaites Virsgrāmata, kas definēta, izmantojot valūtas kombināciju, kalendāru, konvenciju un saistību ar juridisku personu.

Lai iestatītu Globālās krājumu uzskaites Virsgrāmatas, dodieties uz sadaļu **Globālā krājumu uzskaite \> Iestatīšana \> Virsgrāmatas**. Katrai Virsgrāmatai iestatiet šādus laukus:

- **Nosaukums** — ievadiet Virsgrāmatas nosaukumu.
- **Apraksts** — ievadiet Virsgrāmatas aprakstu.
- **Finanšu kalendārs** – norādiet Virsgrāmatas finanšu kalendāru.
- **Valūta un maiņas kursa tips** – izmantojiet šīs kopsavilkuma cilnes laukus, lai izvēlētos uzskaites valūtu, ko izmanto Virsgrāmata, un maiņas kursa tipu. Atlasītā valūta var atšķirties no juridiskās personas lietotās valūtas. Globālajā krājumu uzskaitē lietotāji var definēt tik daudz Virsgrāmatas izmaksu, cik nepieciešams. Globālā krājumu uzskaite atbalsta krājumu uzskaiti vairākās valūtās un vairākos novērtējumos. Iestatiet tālāk minētos laukus:

    - **Valūta** – atlasiet izmaksu valūtu, kurā tiek uzturētas ar krājumiem saistītās vērtības. Šīs vērtības ietver krājumu vērtību, pārdoto preču izmaksas, krājumu tranzītā un visus noviržu veidus.
    - **Maiņas kursa tips** — atlasiet maiņas kursu, kas sistēmai jāizmanto, lai konvertētu darbības summu darbības valūtā un krājumu standarta izmaksas izmaksu valūtā.

- **Konvencijas nosaukums** – norādiet konvenciju. Konvencija ir politiku apkopojums, kas nosaka, kā izmaksas šajā Virsgrāmatā tiks ņemtas vērā.
- **Juridiska persona** – Virsgrāmata grāmatos dokumentus, kas grāmatoti atlasītajai juridiskajai personai.
- **Primings** - atlasiet, vai krājumu darbības, kas tika izveidotas pirms Virsgrāmatas izveidošanas, ir jāapstrādā saskaņā ar valūtu un konvenciju Virsgrāmatā. Atlasiet vienu no šīm vērtībām:

    - **Aktivizēts** – Virsgrāmatai jāapstrādā darbības, kas tika izveidotas pirms Virsgrāmatas izveides.
    - **Deaktivizēts** – Virsgrāmatai jāapstrādā tikai tās darbības, kas ir izveidotas pēc Virsgrāmatas izveides.

    > [!IMPORTANT]
    > Pēc jaunu dokumentu ievadīšanas **nevarēsit** atgriezties un iestatīt šo lauku.

- **Statuss** – sistēma automātiski iestata jauno izveidoto Virsgrāmatu statusu uz *Sagatavot*.
