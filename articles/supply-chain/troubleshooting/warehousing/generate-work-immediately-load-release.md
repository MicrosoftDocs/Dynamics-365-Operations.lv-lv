---
title: Ģenerējiet izdoto darbu nekavējoties pēc noslodzes izlaišanas
description: Ja, izlaižot noslodzi, darbs ir jāveido nekavējoties, ir attiecīgi jākonfigurē laidiena veidne. Šajā lapā ir sniegtas pakāpeniskas norādes.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fdeb0b27f4d2c1a2cc9f8e0c4ba537cdce604bd2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477002"
---
# <a name="picking-work-isnt-generated-immediately-when-outbound-load-is-released"></a>Izdotais darbs netiek ģenerēts nekavējoties pēc izejošās noslodzes izlaišanas

## <a name="symptoms"></a>Simptomi

Izejošā noslodze tiek izveidota, izmantojot pārdošanas vai pārsūtīšanas pasūtījumu un izlaižot noslodzi uz noliktavu. Taču nav vēl ģenerēts neviens izdotais darbs.

## <a name="resolution"></a>Novēršana

Ja, izlaižot noslodzi, darbs ir jāveido nekavējoties, ir attiecīgi jākonfigurē laidiena veidne. Laidiena veidnē iestatiet šādas opcijas uz *Jā*:

- Automatizēt kopuma izveidi
- Apstrādāt kopumu, to pārvietojot uz noliktavu
- Automatizēt kopuma izlaidi
