---
title: Vidējās vērtības pārvietošanas regresa izmaksu secība
description: Šajā tēmā ir sniegta informācija par regresa izmaksu secību vidējā vērtības pārrēķiniem programmā Microsoft Dynamics 365 Supply Chain Management.
author: AndersGirke
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: d91b3b4b8d49e59aa03d62f4dd101b5a1ec18c41
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568211"
---
# <a name="moving-average-fallback-cost-sequence"></a>Vidējās vērtības pārvietošanas regresa izmaksu secība

[!include [banner](../includes/banner.md)]

Viens no veidiem, kā aprēķināt krājumu izmaksas, ir izmantot _vidējo mainīgo_. Ar katru krājuma vienību var saistīt līdz trim izmaksu vērtībām:

- **Pēdējā izejas plūsma** - pēdējās izejas plūsmas izmaksas, kas tika piešķirtas pirms krājuma, bija negatīvas
- **Aktīvās izmaksas** — jaunākās izmaksas, kas tika aktivizētas izmaksu aprēķināšanas versijā
- **Preces cena** — izlaistajai precei norādītā cena

Lai noteiktu, kuras no šīm izmaksu vērtībām ir jāizmanto vidējo aprēķinu pārvietošanā, sistēma izmanto _regresa izmaksu secību_, lai izveidotu preferenču secību vērtībām. Ja vēlamā izmaksu vērtība nav pieejama, sistēma izmanto nākamo vēlamo vērtību, un tā tālāk.

Iepriekšējās Microsoft Dynamics 365 Supply Chain Management versijās sistēma izmantoja fiksētu regresa izmaksu secību (_Pēdējā izejas plūsma – Aktīvās izmaksas – Krājuma cena_). Versijā 10.0.11 šī secība joprojām ir noklusējuma secība. Tomēr jūs varat arī ieslēgt līdzekli, kas ļauj atlasīt starp trim pieejamām alternatīvo izmaksu secībām. Šis līdzeklis var būt īpaši noderīgs uzņēmumiem, kas regulāri izmanto negatīvās krājumu vērtības.

Lai būtu pieejams regresa izmaksu secības selektors, jums (vai administratoram) ir jāizmanto [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai ieslēgtu līdzekli ar nosaukumu _Vidējās vērtības pārvietošanas regresa izmaksu secība_.

Lai izvēlētos regresa izmaksu secību vidējās vērtības pārvietošanas aprēķinam, veiciet šīs darbības.

1. Atveriet lapu **Parametri**.
2. Cilnē **Krājumu uzskaite** sadaļā **Mainīgais vidējais** iestatiet **Regresa izmaksu secības** lauku uz vienu no šīm vērtībām:

    - **Pēdējā izejas plūsma – Aktīvās izmaksas — Krājuma cena** — šī secība ir noklusētā secība. Tā ir tā pati secība, kas tiek izmantota, ja _Mainīgās vidējās vērtības regresa izmaksu secība_ līdzeklis nav ieslēgts.
    - **Aktīvās izmaksas — Pēdējā izejas plūsma**
    - **Aktīvās izmaksas — Krājuma cena** — organizācijām var rasties veiktspējas problēmas, ja tās izmanto biznesa procesus, kuros krājumi regulāri ir negatīvi, un tajā pašā laikā transakciju apjoms ir augsts. Šis iestatījums var palīdzēt mazināt šīs veiktspējas problēmas.

![Krājumu uzskaites parametri.](media/inventory-accounting-parameters.png "Krājumu uzskaites parametri")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]