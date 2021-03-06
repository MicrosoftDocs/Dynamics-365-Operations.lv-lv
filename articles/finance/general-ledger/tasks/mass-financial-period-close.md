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
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 54a5b16f731e850b468ea2e05e47b47774e45838
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826502"
---
# <a name="mass-financial-period-close"></a>Masveida finanšu periodu slēgšana

[!include [banner](../../includes/banner.md)]

Šajā tēmā rādīts, kā apturēt periodu vai pastāvīgi slēgt periodu vairāk nekā vienai juridiskai personai vienlaikus. Turklāt, šis uzdevums parāda, kā ierobežot lietotāju grupu grāmatošanu noteiktiem moduļiem.

1. Navigācijas rūtī dodieties uz **Moduļi > Virsgrāmata > Perioda slēgšana > Virsgrāmatas kalendāri**. Ievērojiet, ka parādītais juridisko personu saraksts ir atkarīgs no finanšu kalendāra, kas ir atlasīts lapā. Tiks parādītas tikai juridiskās personas, kas izmanto atlasīto finanšu kalendāru.
2. Atlasiet **Rediģēt**.
3. Atlasiet periodu, kuram vēlaties mainīt statusu.
4. Atlasiet juridiskās personas, kurām vēlaties atjaunināt statusu. Jūs varat ātri atlasīt visas juridiskās personas, atlasot atzīmi režģa augšējā kreisajā pusē.  
5. Atlasiet **Atjaunināt moduļa piekļuvi**, lai definētu grāmatošanas piekļuvi atlasītajam modulim. Moduļa statusi var tikt atjaunināti viens pēc viena, rediģējot ierakstus režģī. Poga ir noderīgas ja vēlaties ātri atjaunināt vairākus juridisko personu ierakstus.  
6. Modulī **Lietojumprogramma** atlasiet moduli, kuram vēlaties atjaunināt statusu. Noklikšķiniet uz **Atlasīt**.
7. Līmenī **Piekļuve** atlasiet **Visi**, **Neviens** vai konkrētu lietotāju grupu. Noklikšķiniet uz **Atlasīt**. Visi nozīmē, ka visi lietotāji ar rediģēšanas piekļuvi moduļiem var veikt grāmatošanu, ja periods ir atvērts. Neviens nozīmē, ka neviens lietotājs nevar veikt grāmatošanu modulī, ja periods ir atvērts. Specifiska lietotāju grupa nozīmē, ka tikai grupas lietotāji var veikt grāmatošanu modulī, ja periods ir atvērts.  
8. Atlasiet **Atjaunināt**.
9. Atlasīt citu periodu, lai atjauninātu statusu.
10. Atlasiet juridiskās personas, kurām vēlaties atjaunināt perioda statusu.
11. Atlasiet **Atjaunināt perioda statusu** un iestatiet statusu uz **Apturēts**, **Atvērts** vai **Pastāvīgi slēgts**. **Atvērts** norāda uz to, ka periodu var grāmatot, ja lietotājam ir piekļuve. **Apturēts** nozīmē, ka periodu nevar grāmatot, taču periodu var atvērt no jauna. **Pastāvīgi slēgts** nozīmē, ka periods ir slēgts un nevar tikt atvērts. Korekcijas nevar grāmatot. Mēs neiesakām iestatīt periodu uz **Pastāvīgi slēgts**, kamēr nav pabeigti visi pielāgojumi un auditi.  
12. Atlasiet **Atjaunināt**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]