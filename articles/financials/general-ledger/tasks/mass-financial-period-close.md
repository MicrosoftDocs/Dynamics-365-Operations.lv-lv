---
title: Masveida finanšu periodu slēgšana
description: Šī procedūra parāda, kā aizturēt vai neatgriezeniski slēgt periodu, vai vienlaicīgi vairāk nekā vienu juridisku personu.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2988b7ab0837cc9a3e4f1c4eaf3fe6e219fa721
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "311385"
---
# <a name="mass-financial-period-close"></a>Masveida finanšu periodu slēgšana

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šī procedūra parāda, kā aizturēt vai neatgriezeniski slēgt periodu, vai vienlaicīgi vairāk nekā vienu juridisku personu. Turklāt, šis uzdevums parāda, kā ierobežot lietotāju grupu grāmatošanu noteiktiem moduļiem.

1. Dodieties uz Virsgrāmata > Perioda noslēgšana > Virsgrāmatas kalendāri.
    * Ievērojiet, ka parādītais juridisko personu saraksts ir atkarīgs no finanšu kalendāra, kas ir atlasīts lapā. Tiks parādītas tikai juridiskās personas, kas izmanto atlasīto finanšu kalendāru.  
2. Noklikšķiniet uz Rediģēt.
3. Atlasiet periodu, kuram vēlaties mainīt statusu.
4. Atlasiet juridiskās personas, kurām vēlaties atjaunināt statusu.
    * Jūs varat ātri atlasīt visas juridiskās personas, atzīmējot izvēles rūtiņu, kas atrodas režģa augšējā kreisajā pusē.  
5. Atlasiet Atjaunināt moduļa piekļuvi, lai definētu grāmatošanas piekļuvi atlasītajam modulim.
    * Moduļa statusi var tikt atjaunināti viens pēc viena, rediģējot ierakstus režģī. Poga ir noderīgas ja vēlaties ātri atjaunināt vairākus juridisko personu ierakstus.  
6. Laukā Programmas modulis, atlasiet moduli, kura statusu vēlaties atjaunināt. Noklikšķiniet uz Atlasīt.
7. Piekļuves līmenī, atlasiet Visi, Neviens vai ir konkrēta lietotāju grupa. Noklikšķiniet uz Atlasīt.
    * Visi nozīmē, ka visi lietotāji ar rediģēšanas piekļuvi moduļiem var veikt grāmatošanu, ja periods ir atvērts. Neviens nozīmē, ka neviens lietotājs nevar veikt grāmatošanu modulī, ja periods ir atvērts. Specifiska lietotāju grupa nozīmē, ka tikai grupas lietotāji var veikt grāmatošanu modulī, ja periods ir atvērts.  
8. Noklikšķiniet uz Atjaunināt.
9. Atlasīt citu periodu, lai atjauninātu statusu.
10. Atlasiet juridiskās personas, kurām vēlaties atjaunināt perioda statusu.
11. Atlasiet Perioda statusu, un iestatiet statusu Aizturēts, Atvērts vai Neatgriezeniski slēgts.
    * Atvērts norāda uz periodu, kurā var grāmatot, pie nosacījuma, ka lietotājam ir piekļuve. Aizturēts nozīmē, ka periods nevar būt grāmatots, bet periodu var atvērt atkārtoti. Neatgriezeniski slēgts nozīmē, ka periods ir slēgts un to nevar atvērt. Korekcijas nevar grāmatot. Nav ieteicams iestatīt periodu uz Neatgriezeniski slēgts, kamēr visas korekcijas un auditi nav pabeigti.  
12. Noklikšķiniet uz Atjaunināt.

