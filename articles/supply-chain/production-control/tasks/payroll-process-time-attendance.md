---
title: Algas procesa iespējošana laikam un apmeklētībai
description: Šajā procedūrā ir parādīts, kā iespējot algu procesu attiecībā uz laiku un apmeklētību.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0174f438396d814d153befe4a59a79b6eebb2288
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "311109"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a>Algas procesa iespējošana laikam un apmeklētībai

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā iespējot algu procesu attiecībā uz laiku un apmeklētību. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.


## <a name="create-a-pay-type-with-a-related-pay-rate"></a>Izveidot apmaksas tipu ar saistītu apmaksas likmi
1. Laiks un apmeklētība > Iestatījumi > Alga > Apmaksas veidi
2. Noklikšķiniet uz Jauns.
3. Laukā Apmaksas tips ierakstiet kādu vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Noklikšķiniet uz Saglabāt.
6. Noklikšķiniet uz Likmes.
    * Apmaksas tipu likmes tiek iestatītas noteiktiem laika intervāliem, un darbiniekiem var izveidot individuālas likmes. Ne vienmēr ir nepieciešams apmaksas tipu likmes izveidot laikam un apmeklētībai. Šī informācija var jau pastāvēt algu sistēmā, kas tiek lietota algu ģenerēšanai.  
7. Noklikšķiniet uz Jauns.
8. Sarakstā atzīmējiet atlasīto rindu.
9. Lauka Likme ierakstiet kādu skaitli.
10. Noklikšķiniet uz Saglabāt.

## <a name="create-a-pay-agreement"></a>Apmaksas līguma izveide
1. Aizvērt lapu.
2. Aizvērt lapu.
3. Dodieties uz Apmaksas līgumi.
    * Laiks un apmeklētība > Iestatījumi > Apmaksas līgumi  
4. Noklikšķiniet uz Jauns.
5. Laukā Apmaksas līgums ierakstiet kādu vērtību.
6. Apraksta laukā ierakstiet vērtību.
7. Noklikšķiniet uz Saglabāt.
8. Noklikšķiniet uz Līguma rindas.
9. Noklikšķiniet uz Jauns.
10. Sarakstā atzīmējiet atlasīto rindu.
11. Laukā Profila tips ievadiet vai atlasiet kādu vērtību.
12. Laukā Apmaksas tips ievadiet vai atlasiet vērtību.

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a>Iestatīt apmaksas līgumu laika un reģistrācijas darbiniekam
1. Aizvērt lapu.
2. Aizvērt lapu.
3. Dodieties uz Laika reģistrācijas darbinieki.
    * Laiks un apmeklētība > Iestatījumi > Laika reģistrācijas darbinieki  
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Noklikšķiniet uz cilnes Nodarbinātība.
6. Izvērsiet sadaļu Laika reģistrācija.
7. Noklikšķiniet uz Rediģēt.
8. Laukā Apmaksas līgums ievadiet vai atlasiet kādu vērtību.

