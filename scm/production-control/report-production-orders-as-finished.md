---
title: "Ziņošana par ražošanas pasūtījumu pabeigšanu"
description: "“Ziņot kā pabeigtu” ir ražošanas posms. Šī posma ietvaros tiek ziņots par preces pabeigšanu un tā tiek pārvietota no ražošanas pasūtījuma uz krājumiem."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 52607d645c6eaf4ff97d2c4bf8abc6ec1374fd7e
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="report-production-orders-as-finished"></a>Ziņošana par ražošanas pasūtījumu pabeigšanu

[!include[banner](../includes/banner.md)]


“Ziņot kā pabeigtu” ir ražošanas posms. Šī posma ietvaros tiek ziņots par preces pabeigšanu un tā tiek pārvietota no ražošanas pasūtījuma uz krājumiem.

Kad pabeigto preču daudzumu ražošanas pasūtījumā reģistrē kā pabeigtu, tiek atjaunināts rīcībā esošo krājumu daudzums. Daļējos daudzumus sākotnēji plānotajā pasūtījuma daudzumā var reģistrēt kā pabeigtus. Reģistrējot daudzumus kā pabeigtus, ir iespējams arī ziņot par kļūdainiem daudzumiem, norādot saistīto kļūdu pamatojumu. Kad ražošanas pasūtījums sasniedz stadiju Fiziski pabeigts, tas nozīmē, ka par pārējiem daudzumiem ražošanas pasūtījumā netiks ziņots.
Šīs īpašības arī saistītas ar procesu **Reģistrēt pabeigšanu**:
-   Ir iespējams iestatīt izejmateriālu patēriņu un laiku, kas ir proporcionāls paziņotajam daudzumam (reversā norakstīšana)
-   Izvietošanas darbu var izveidot krājumiem, kas ir iespējoti noliktavas procesiem.
-   Pabeigto preču plānoto vai standarta izmaksu vērtību var iestatīt tā, lai tā tiktu ziņota Virsgrāmatas kontiem.
-   Kvalitātes pārbaudes pasūtījumu var izveidot paziņotajam daudzumam, pamatojoties uz kvalitātes piesaistes iestatījumu.

Daudzums tiek ziņots ražojuma novietojumam. Pēc tam tiek ģenerēts noliktavas darbs, lai pārvietotu daudzumu no ražojuma novietojuma uz galamērķi, ko nosaka izvietošanas darba novietojuma direktīva.

-   Kvalitātes pārbaudes pasūtījumu var izveidot, kad ražošanas pasūtījums ir reģistrēts kā pabeigts, ja ir iestatīta kvalitātes piesaiste.

## <a name="set-a-production-order-to-reporting-as-finished"></a>Ražošanas pasūtījuma iestatīšana uz Fiziski pabeigts
Ražošanas pasūtījumu var iestatīt uz statusu **Fiziski pabeigts**, izmantojot standarta ražošanas pasūtījuma atjaunināšanas funkciju, vai maršrutu un darba karšu žurnālus, vai žurnālu **Fiziski pabeigts**. Jūs varat arī atjaunināt stadiju uz **Fiziski pabeigts**, izmantojot darbu karšu terminālu un darbu karšu ierīces lapas, sniedzot pārskatu par pēdējo ražošanas pasūtījuma darbu. Visbeidzot, jūs varat iespējot opciju **Fiziski pabeigts** kā rokas noliktavas ierīces risinājuma procesu.  




