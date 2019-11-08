---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent — Core HR (2018. gada 16. oktobris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent — Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
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
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0d7c6562ca8b5e7cfa0071ec408955e13a46cb6e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551707"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-16-2018"></a>Jaunumi un izmaiņas programmā Dynamics 365 Talent — Core HR (2018. gada 16. oktobris)

[!include[banner](includes/banner.md)]

**8.1.1067 būvējums**

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Core HR.

## <a name="allow-managers-to-update-time-off-requests"></a>Ļaušana vadītājiem atjaunināt brīvā laika pieprasījumus

Darbinieku brīvā laika pieprasījumus var būt nepieciešams atjaunināt pēc tam, kad tie ir apstiprināti, izmantojot darbplūsmu. Daudzos gadījumos vadītājs šos atjauninājumus veic darbinieka vārdā. Šis jaunais līdzeklis nodrošina iespēju vadītājiem atjaunināt brīvo laiku vai atcelt brīvā laika pieprasījumus savu darbinieku vārdā. Šo iespēju kontrolē parametrs **Darbs kāda vārdā**, un šo parametru var iestatīt lapā **Personāla vadības parametri**. 
 
## <a name="allow-hr-to-update-time-off-requests"></a>Ļaušana personāla vadībai (HR) atjaunināt brīvā laika pieprasījumus

Līdzīgi iepriekš aprakstītajam līdzeklim, arī personāla vadībai (HR) var būt nepieciešams atjaunināt darbinieku brīvā laika pieprasījumus pēc tam, kad tie ir apstiprināti, izmantojot darbplūsmu. Šis līdzeklis nodrošina HR lietotājiem iespēju atjaunināt brīvā laika pieprasījumus. Šī iespēja tiek aktivizēta darbvietā **Personas** un lapā **Nodarbinātais**, izmantojot jaunu opciju ar nosaukumu **Skatīt brīvo laiku**. Šajās lapās HR lietotāji var skatīt pieprasījumus un atjaunināt brīvā laika transakcijas, līdzīgi kā šīs darbības var veikt vadītāji.

Drošības pienākums, kas kontrolē piekļuvi šai funkcionalitātei, ir šāds:
- Pienākums: Uzturēt nodarbinātajam raksturīgus atvaļinājumu un prombūtnes procesus.
- Privilēģija: Uzturēt visu nodarbināto atvaļinājuma un prombūtnes pieprasījumus.

## <a name="other-changes"></a>Cita izmaiņas
Šajā laidienā ir ieviesti tālāk aprakstītie atjauninājumi.
- Izmaiņas nodarbināto darbā pieņemšanas darbībās, lai nodarbinātie vairs “neiestrēgtu” stāvoklī **Darbplūsma izpildīta**.
- Nodarbinātības ierakstu tagad var izveidot bez nodarbinātības sākuma datuma.
- Dynamics 365 Talent reģistrācijas datums kursam, kas tiek rādīts darbinieku pašapkalpošanās sadaļā, tagad datumam lieto laika joslas nobīdi.
- Excel failus var importēt vairākas reizes bez kļūdām, izmantojot **elementu Darbinieks**.

## <a name="known-issue"></a>Zināma problēma

- **Problēma**: kad nodarbinātajam tiek pievienots jauns pielikums, poga **Jauns** un **Rediģēt** ir pelēkotas. 
- **Risinājums:** pirms pielikuma lapas atvēršanas ir jāpārliecinās, vai papildinformācijas lodziņi lapā **Nodarbinātais** ir aizvērti. Ja, ielādējot lapu **Nodarbinātais**, papildinformācija ir aizvērta, pielikumu pogas tiek iespējotas. (Šī problēma tiks novērsta nākamajā platformas atjauninājumā.)
