---
title: Masveida finanšu periodu slēgšana
description: Šajā rakstā ir paskaidrots, kā periodu aizturēt vai neatgriezeniski slēgt periodu vai vairākas juridiskās personas vienlaikus.
author: aprilolson
ms.date: 11/16/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a85d512842b27f2d74507be16a8f2819f483e0d
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779831"
---
# <a name="mass-financial-period-close"></a>Masveida finanšu periodu slēgšana

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir paskaidrots, kā periodu aizturēt vai neatgriezeniski slēgt periodu vai vairākas juridiskās personas vienlaikus. Turklāt, šis uzdevums parāda, kā ierobežot lietotāju grupu grāmatošanu noteiktiem moduļiem.

1. Navigācijas rūtī dodieties uz Virsgrāmata **> Perioda aizvēršana > Virsgrāmatas kalendāri**. 

>[!NOTE]
> Parādītais juridisko personu saraksts ir atkarīgs no lapā atlasītā finanšu kalendāra. Tiks parādītas tikai juridiskās personas, kas izmanto atlasīto finanšu kalendāru.

2. Atlasiet **Rediģēt**.
3. Atlasiet periodu, kuram vēlaties mainīt statusu.
4. Atlasiet juridiskās personas, kurām vēlaties atjaunināt statusu. Jūs varat ātri atlasīt visas juridiskās personas, atlasot atzīmi režģa augšējā kreisajā pusē.  
5. Atlasiet **Atjaunināt moduļa piekļuvi**, lai definētu grāmatošanas piekļuvi atlasītajam modulim. Moduļa statusi var tikt atjaunināti viens pēc viena, rediģējot ierakstus režģī. Poga ir noderīgas ja vēlaties ātri atjaunināt vairākus juridisko personu ierakstus.  
6. Modulī **Lietojumprogramma** atlasiet moduli, kuram vēlaties atjaunināt statusu. Noklikšķiniet uz **Atlasīt**.
7. Līmenī **Piekļuve** atlasiet **Visi**, **Neviens** vai konkrētu lietotāju grupu. Noklikšķiniet uz **Atlasīt**.  
- **Visi** - visi lietotāji ar rediģēšanas piekļuvi modulim var publicēt, ja periods ir atvērts. 
- **Nav** — lietotāji nevar izlikt ziņas modulī, ja periods ir atvērts. Specifiska lietotāju grupa nozīmē, ka tikai grupas lietotāji var veikt grāmatošanu modulī, ja periods ir atvērts.  
8. Atlasiet **Atjaunināt**, 
9. Atlasīt citu periodu, lai atjauninātu statusu.
10. Atlasiet juridiskās personas, kurām vēlaties atjaunināt perioda statusu.
11. Atlasiet **Atjaunināt perioda statusu** un iestatiet statusu uz **Apturēts**, **Atvērts** vai **Pastāvīgi slēgts**. **Atvērts** norāda uz to, ka periodu var grāmatot, ja lietotājam ir piekļuve. **Apturēts** nozīmē, ka periodu nevar grāmatot, taču periodu var atvērt no jauna. **Pastāvīgi slēgts** nozīmē, ka periods ir slēgts un nevar tikt atvērts. Korekcijas nevar grāmatot. Nav ieteicams iestatīt periodu uz **Pastāvīgi slēgts**, kamēr nav pabeigtas visas korekcijas un auditi.  
12. Atlasiet **Atjaunināt**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
