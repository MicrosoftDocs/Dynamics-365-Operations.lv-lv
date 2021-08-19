---
title: Globālo krājumu uzskaites virsgrāmata
description: Šajā tēmā aprakstītas Globālās krājumu uzskaites Virsgrāmatas, kas definētas, izmantojot valūtas kombināciju, kalendāru, konvenciju un saistību ar juridisku personu.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e956bac61df4b694ef347b804fed139e9e22e6f95d1bac7ea483a07946cb110f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722443"
---
# <a name="global-inventory-accounting-ledger"></a>Globālo krājumu uzskaites virsgrāmata

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

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
