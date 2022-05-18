---
title: Masveida finanšu periodu slēgšana
description: Šajā tēmā rādīts, kā apturēt periodu vai pastāvīgi slēgt periodu vairāk nekā vienai juridiskai personai vienlaikus.
author: aprilolson
ms.date: 08/16/2019
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
ms.openlocfilehash: 0acaad0d6e89fe7c81537e554b36ffb210e5abad
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722071"
---
# <a name="mass-financial-period-close"></a>Masveida finanšu periodu slēgšana

[!include [banner](../../includes/banner.md)]

Šajā tēmā rādīts, kā apturēt periodu vai pastāvīgi slēgt periodu vairāk nekā vienai juridiskai personai vienlaikus. Turklāt, šis uzdevums parāda, kā ierobežot lietotāju grupu grāmatošanu noteiktiem moduļiem.

1. Navigācijas rūtī dodieties uz Virsgrāmatas **> perioda slēgšanas > kalendāriem**. Ievērojiet, ka parādītais juridisko personu saraksts ir atkarīgs no finanšu kalendāra, kas ir atlasīts lapā. Tiks parādītas tikai juridiskās personas, kas izmanto atlasīto finanšu kalendāru.
2. Atlasiet **Rediģēt**.
3. Atlasiet periodu, kuram vēlaties mainīt statusu.
4. Atlasiet juridiskās personas, kurām vēlaties atjaunināt statusu. Jūs varat ātri atlasīt visas juridiskās personas, atlasot atzīmi režģa augšējā kreisajā pusē.  
5. Atlasiet **Atjaunināt moduļa piekļuvi**, lai definētu grāmatošanas piekļuvi atlasītajam modulim. Moduļa statusi var tikt atjaunināti viens pēc viena, rediģējot ierakstus režģī. Poga ir noderīgas ja vēlaties ātri atjaunināt vairākus juridisko personu ierakstus.  
6. Modulī **Lietojumprogramma** atlasiet moduli, kuram vēlaties atjaunināt statusu. Noklikšķiniet uz **Atlasīt**.
7. Līmenī **Piekļuve** atlasiet **Visi**, **Neviens** vai konkrētu lietotāju grupu. Noklikšķiniet uz **Atlasīt**.  
- **Visi** - visi lietotāji ar rediģēšanas piekļuvi modulim var grāmatot, ja periods ir atvērts. 
- **Neviens** - lietotāji nevar grāmatot šajā modulī, ja periods ir atvērts. Specifiska lietotāju grupa nozīmē, ka tikai grupas lietotāji var veikt grāmatošanu modulī, ja periods ir atvērts.  
8. Atlasiet **Atjaunināt**, 
9. Atlasīt citu periodu, lai atjauninātu statusu.
10. Atlasiet juridiskās personas, kurām vēlaties atjaunināt perioda statusu.
11. Atlasiet **Atjaunināt perioda statusu** un iestatiet statusu uz **Apturēts**, **Atvērts** vai **Pastāvīgi slēgts**. **Atvērts** norāda uz to, ka periodu var grāmatot, ja lietotājam ir piekļuve. **Apturēts** nozīmē, ka periodu nevar grāmatot, taču periodu var atvērt no jauna. **Pastāvīgi slēgts** nozīmē, ka periods ir slēgts un nevar tikt atvērts. Korekcijas nevar grāmatot. Mēs neiesakām iestatīt periodu uz **Pastāvīgi slēgts**, kamēr nav pabeigti visi pielāgojumi un auditi.  
12. Atlasiet **Atjaunināt**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
