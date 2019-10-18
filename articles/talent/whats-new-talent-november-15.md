---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent — Core HR (2018. gada 15. novembris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent — Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ab3758506679db5032e3dffc1664fe1ac7f622c8
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009674"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-november-15-2018"></a>Jaunumi un izmaiņas programmā Dynamics 365 Talent: Core HR (2018. gada 15. novembris)

[!include [banner](includes/banner.md)]

**8.1.2045 būvējums**

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Core HR.

## <a name="other-changesfixes"></a>Citas izmaiņas/labojumi

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a>Nevar mainīt darbinieka pašreizējo amatu uz turpmāko atvērto amatu

Ir veiktas izmaiņas, lai iespējotu amatu pārnešanu, ja amats ir pieejams tikai nākotnē. 

### <a name="position-does-not-display-when-creating-a-new-employee"></a>Amats netiek rādīts, veidojot jaunu darbinieku

Ir veiktas izm., lai rādītu visus atvērtos amatus, kas pieejami piešķiršanai, pieņemot darbā jaunu darb. programmā Talent. Tas ietver vēsturiskos amatus vai gadījumus, ja amatiem ir nākotnes datums. Tagad amati tiks rādīti pareizi, balstoties uz nodarbin. sākuma datumu. 

### <a name="termination-date-is-displaying-based-on-user-settings"></a>Izbeigš. datumu rāda, balstoties uz lietot. iestat.

Ir veiktas izm. bijušo darbinieku sarakstā, lai ņemtu vērā laika joslu nobīdes darbiniekiem vēlamajai laika joslai, skatot darba attiec. pārtraukšanas datumu.

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a>Darba vienumu, kas saistīti ar mani, saites neparāda pareizo inform.

Ar šīm izmaiņām navigācija uz atsevišķu darba vienumu informāciju sarakstā parādīs pareizu informāciju atlasītajam krājumam. Šī problēma rodas tikai ar papildu drošības opcijām.


## <a name="known-issue"></a>Zināma problēma

- **Problēma**: kad nodarbinātajam tiek pievienots jauns pielikums, poga **Jauns** un **Rediģēt** ir pelēkotas. 
- **Risinājums:** pirms pielikuma lapas atvēršanas ir jāpārliecinās, vai papildinformācijas lodziņi lapā **Nodarbinātais** ir aizvērti. Ja, ielādējot lapu **Nodarbinātais**, papildinformācija ir aizvērta, pielikumu pogas tiek iespējotas. (Šī problēma tiks novērsta nākamajā platformas atjauninājumā.)
